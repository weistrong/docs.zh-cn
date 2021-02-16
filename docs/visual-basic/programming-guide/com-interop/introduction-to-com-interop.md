---
description: '了解详细信息： COM 互操作简介 (Visual Basic) '
title: COM 互操作介绍
ms.date: 07/20/2015
helpviewer_keywords:
- interop assemblies
- COM interop [Visual Basic], about COM interop
ms.assetid: 8bd62e68-383d-407f-998b-29aa0ce0fd67
ms.openlocfilehash: 86741958e63263f0788384a1261063d71d16df16
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100480786"
---
# <a name="introduction-to-com-interop-visual-basic"></a><span data-ttu-id="669eb-103">COM 互操作介绍 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="669eb-103">Introduction to COM Interop (Visual Basic)</span></span>

<span data-ttu-id="669eb-104">组件对象模型 (COM) 使对象向其他组件和宿主应用程序公开其功能。</span><span class="sxs-lookup"><span data-stu-id="669eb-104">The Component Object Model (COM) lets an object expose its functionality to other components and to host applications.</span></span> <span data-ttu-id="669eb-105">虽然 COM 对象多年来一直是 Windows 编程的基础，但为公共语言运行时设计的应用程序 (CLR) 提供多种优势。</span><span class="sxs-lookup"><span data-stu-id="669eb-105">While COM objects have been fundamental to Windows programming for many years, applications designed for the common language runtime (CLR) offer many advantages.</span></span>  
  
 <span data-ttu-id="669eb-106">.NET Framework 应用程序最终将取代通过 COM 开发的应用程序。</span><span class="sxs-lookup"><span data-stu-id="669eb-106">.NET Framework applications will eventually replace those developed with COM.</span></span> <span data-ttu-id="669eb-107">在此之前，你可能必须使用 Visual Studio 来使用或创建 COM 对象。</span><span class="sxs-lookup"><span data-stu-id="669eb-107">Until then, you may have to use or create COM objects by using Visual Studio.</span></span> <span data-ttu-id="669eb-108">与 COM 或 *com 互操作* 的互操作性使你能够在按自己的节奏转换到 .NET Framework 时使用现有的 com 对象。</span><span class="sxs-lookup"><span data-stu-id="669eb-108">Interoperability with COM, or *COM interop*, enables you to use existing COM objects while transitioning to the .NET Framework at your own pace.</span></span>  
  
 <span data-ttu-id="669eb-109">通过使用 .NET Framework 创建 COM 组件，你可以使用无注册 COM 互操作。</span><span class="sxs-lookup"><span data-stu-id="669eb-109">By using the .NET Framework to create COM components, you can use registration-free COM interop.</span></span> <span data-ttu-id="669eb-110">这样，你就可以在计算机上安装了多个版本时控制启用了哪个 DLL 版本，并允许最终用户使用 XCOPY 或 FTP 将你的应用程序复制到其计算机上可以运行它的相应目录。</span><span class="sxs-lookup"><span data-stu-id="669eb-110">This lets you control which DLL version is enabled when more than one version is installed on a computer, and lets end users use XCOPY or FTP to copy your application to an appropriate directory on their computer where it can be run.</span></span> <span data-ttu-id="669eb-111">有关详细信息，请参阅 [免注册 COM 互操作](../../../framework/interop/registration-free-com-interop.md)。</span><span class="sxs-lookup"><span data-stu-id="669eb-111">For more information, see [Registration-Free COM Interop](../../../framework/interop/registration-free-com-interop.md).</span></span>  
  
## <a name="managed-code-and-data"></a><span data-ttu-id="669eb-112">托管代码和数据</span><span class="sxs-lookup"><span data-stu-id="669eb-112">Managed Code and Data</span></span>  

 <span data-ttu-id="669eb-113">为 .NET Framework 开发的代码称为 *托管代码*，并包含 CLR 使用的元数据。</span><span class="sxs-lookup"><span data-stu-id="669eb-113">Code developed for the .NET Framework is referred to as *managed code*, and contains metadata that is used by the CLR.</span></span> <span data-ttu-id="669eb-114">.NET Framework 应用程序使用的数据称为 *托管数据* ，因为运行时管理与数据相关的任务，例如分配和回收内存以及执行类型检查。</span><span class="sxs-lookup"><span data-stu-id="669eb-114">Data used by .NET Framework applications is called *managed data* because the runtime manages data-related tasks such as allocating and reclaiming memory and performing type checking.</span></span> <span data-ttu-id="669eb-115">默认情况下，Visual Basic .NET 使用托管代码和数据，但你可以使用互操作程序集访问 COM 对象的非托管代码和数据， (稍后) 此页中所述。</span><span class="sxs-lookup"><span data-stu-id="669eb-115">By default, Visual Basic .NET uses managed code and data, but you can access the unmanaged code and data of COM objects using interop assemblies (described later on this page).</span></span>  
  
## <a name="assemblies"></a><span data-ttu-id="669eb-116">程序集</span><span class="sxs-lookup"><span data-stu-id="669eb-116">Assemblies</span></span>  

 <span data-ttu-id="669eb-117">程序集是 .NET Framework 应用程序的主要构造块。</span><span class="sxs-lookup"><span data-stu-id="669eb-117">An assembly is the primary building block of a .NET Framework application.</span></span> <span data-ttu-id="669eb-118">它是一个功能集合，它作为包含一个或多个文件的单个实现单元进行生成、版本控制和部署。</span><span class="sxs-lookup"><span data-stu-id="669eb-118">It is a collection of functionality that is built, versioned, and deployed as a single implementation unit containing one or more files.</span></span> <span data-ttu-id="669eb-119">每个程序集都包含一个程序集清单。</span><span class="sxs-lookup"><span data-stu-id="669eb-119">Each assembly contains an assembly manifest.</span></span>  
  
## <a name="type-libraries-and-assembly-manifests"></a><span data-ttu-id="669eb-120">类型库和程序集清单</span><span class="sxs-lookup"><span data-stu-id="669eb-120">Type Libraries and Assembly Manifests</span></span>  

 <span data-ttu-id="669eb-121">类型库描述 COM 对象的特征，如成员名称和数据类型。</span><span class="sxs-lookup"><span data-stu-id="669eb-121">Type libraries describe characteristics of COM objects, such as member names and data types.</span></span> <span data-ttu-id="669eb-122">程序集清单对 .NET Framework 应用程序执行相同的功能。</span><span class="sxs-lookup"><span data-stu-id="669eb-122">Assembly manifests perform the same function for .NET Framework applications.</span></span> <span data-ttu-id="669eb-123">它们包括有关以下内容的信息：</span><span class="sxs-lookup"><span data-stu-id="669eb-123">They include information about the following:</span></span>  
  
- <span data-ttu-id="669eb-124">程序集标识、版本、区域性和数字签名。</span><span class="sxs-lookup"><span data-stu-id="669eb-124">Assembly identity, version, culture, and digital signature.</span></span>  
  
- <span data-ttu-id="669eb-125">组成程序集实现的文件。</span><span class="sxs-lookup"><span data-stu-id="669eb-125">Files that make up the assembly implementation.</span></span>  
  
- <span data-ttu-id="669eb-126">构成程序集的类型和资源。</span><span class="sxs-lookup"><span data-stu-id="669eb-126">Types and resources that make up the assembly.</span></span> <span data-ttu-id="669eb-127">这包括从它中导出的。</span><span class="sxs-lookup"><span data-stu-id="669eb-127">This includes those that are exported from it.</span></span>  
  
- <span data-ttu-id="669eb-128">对其他程序集的编译时依赖关系。</span><span class="sxs-lookup"><span data-stu-id="669eb-128">Compile-time dependencies on other assemblies.</span></span>  
  
- <span data-ttu-id="669eb-129">程序集正常运行所需的权限。</span><span class="sxs-lookup"><span data-stu-id="669eb-129">Permissions required for the assembly to run correctly.</span></span>  
  
 <span data-ttu-id="669eb-130">有关程序集和程序集清单的详细信息，请参阅 [.net 中的程序集](../../../standard/assembly/index.md)。</span><span class="sxs-lookup"><span data-stu-id="669eb-130">For more information about assemblies and assembly manifests, see [Assemblies in .NET](../../../standard/assembly/index.md).</span></span>  
  
### <a name="importing-and-exporting-type-libraries"></a><span data-ttu-id="669eb-131">导入和导出类型库</span><span class="sxs-lookup"><span data-stu-id="669eb-131">Importing and Exporting Type Libraries</span></span>  

 <span data-ttu-id="669eb-132">Visual Studio 包含一个实用工具 Tlbimp，使你可以将类型库中的信息导入到 .NET Framework 的应用程序中。</span><span class="sxs-lookup"><span data-stu-id="669eb-132">Visual Studio contains a utility, Tlbimp, that lets you import information from a type library into a .NET Framework application.</span></span> <span data-ttu-id="669eb-133">可以通过使用 Tlbexp.exe 实用工具从程序集生成类型库。</span><span class="sxs-lookup"><span data-stu-id="669eb-133">You can generate type libraries from assemblies by using the Tlbexp utility.</span></span>  
  
 <span data-ttu-id="669eb-134">有关 Tlbimp 和 Tlbexp.exe 的信息，请参阅 [Tlbimp.exe (类型库导入程序) ](../../../framework/tools/tlbimp-exe-type-library-importer.md) 和 [Tlbexp.exe (类型库导出程序) ](../../../framework/tools/tlbexp-exe-type-library-exporter.md)。</span><span class="sxs-lookup"><span data-stu-id="669eb-134">For information about Tlbimp and Tlbexp, see [Tlbimp.exe (Type Library Importer)](../../../framework/tools/tlbimp-exe-type-library-importer.md) and [Tlbexp.exe (Type Library Exporter)](../../../framework/tools/tlbexp-exe-type-library-exporter.md).</span></span>  
  
## <a name="interop-assemblies"></a><span data-ttu-id="669eb-135">互操作程序集</span><span class="sxs-lookup"><span data-stu-id="669eb-135">Interop Assemblies</span></span>  

 <span data-ttu-id="669eb-136">互操作程序集是在托管代码和非托管代码之间桥接的 .NET Framework 程序集，将 COM 对象成员映射到等效的 .NET Framework 托管成员。</span><span class="sxs-lookup"><span data-stu-id="669eb-136">Interop assemblies are .NET Framework assemblies that bridge between managed and unmanaged code, mapping COM object members to equivalent .NET Framework managed members.</span></span> <span data-ttu-id="669eb-137">Visual Basic .NET 创建的互操作程序集用于处理使用 COM 对象（如互操作性封送处理）的许多详细信息。</span><span class="sxs-lookup"><span data-stu-id="669eb-137">Interop assemblies created by Visual Basic .NET handle many of the details of working with COM objects, such as interoperability marshaling.</span></span>  
  
## <a name="interoperability-marshaling"></a><span data-ttu-id="669eb-138">互操作性封送</span><span class="sxs-lookup"><span data-stu-id="669eb-138">Interoperability Marshaling</span></span>  

 <span data-ttu-id="669eb-139">所有 .NET Framework 应用程序共享一组公共类型，这些类型可以实现对象的互操作性，而不考虑所使用的编程语言。</span><span class="sxs-lookup"><span data-stu-id="669eb-139">All .NET Framework applications share a set of common types that enable interoperability of objects, regardless of the programming language that is used.</span></span> <span data-ttu-id="669eb-140">COM 对象的参数和返回值有时使用的数据类型与托管代码中使用的数据类型不同。</span><span class="sxs-lookup"><span data-stu-id="669eb-140">The parameters and return values of COM objects sometimes use data types that differ from those used in managed code.</span></span> <span data-ttu-id="669eb-141">*互操作封送处理* 是一种将参数和返回值与 COM 对象来回移动的等效数据类型的过程。</span><span class="sxs-lookup"><span data-stu-id="669eb-141">*Interoperability marshaling* is the process of packaging parameters and return values into equivalent data types as they move to and from COM objects.</span></span> <span data-ttu-id="669eb-142">有关详细信息，请参阅 [互操作封送处理](../../../framework/interop/interop-marshaling.md)。</span><span class="sxs-lookup"><span data-stu-id="669eb-142">For more information, see [Interop Marshaling](../../../framework/interop/interop-marshaling.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="669eb-143">请参阅</span><span class="sxs-lookup"><span data-stu-id="669eb-143">See also</span></span>

- [<span data-ttu-id="669eb-144">COM 互操作</span><span class="sxs-lookup"><span data-stu-id="669eb-144">COM Interop</span></span>](index.md)
- [<span data-ttu-id="669eb-145">演练：使用 COM 对象实现继承</span><span class="sxs-lookup"><span data-stu-id="669eb-145">Walkthrough: Implementing Inheritance with COM Objects</span></span>](walkthrough-implementing-inheritance-with-com-objects.md)
- [<span data-ttu-id="669eb-146">与非托管代码交互操作</span><span class="sxs-lookup"><span data-stu-id="669eb-146">Interoperating with Unmanaged Code</span></span>](../../../framework/interop/index.md)
- [<span data-ttu-id="669eb-147">互操作性疑难解答</span><span class="sxs-lookup"><span data-stu-id="669eb-147">Troubleshooting Interoperability</span></span>](troubleshooting-interoperability.md)
- [<span data-ttu-id="669eb-148">.NET 中的程序集</span><span class="sxs-lookup"><span data-stu-id="669eb-148">Assemblies in .NET</span></span>](../../../standard/assembly/index.md)
- [<span data-ttu-id="669eb-149">Tlbimp.exe（类型库导入程序）</span><span class="sxs-lookup"><span data-stu-id="669eb-149">Tlbimp.exe (Type Library Importer)</span></span>](../../../framework/tools/tlbimp-exe-type-library-importer.md)
- [<span data-ttu-id="669eb-150">Tlbexp.exe（类型库导出程序）</span><span class="sxs-lookup"><span data-stu-id="669eb-150">Tlbexp.exe (Type Library Exporter)</span></span>](../../../framework/tools/tlbexp-exe-type-library-exporter.md)
- [<span data-ttu-id="669eb-151">互操作封送处理</span><span class="sxs-lookup"><span data-stu-id="669eb-151">Interop Marshaling</span></span>](../../../framework/interop/interop-marshaling.md)
- [<span data-ttu-id="669eb-152">免注册 COM 互操作</span><span class="sxs-lookup"><span data-stu-id="669eb-152">Registration-Free COM Interop</span></span>](../../../framework/interop/registration-free-com-interop.md)
