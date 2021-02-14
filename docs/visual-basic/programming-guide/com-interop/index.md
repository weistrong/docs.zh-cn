---
description: '详细了解： COM 互操作 (Visual Basic) '
title: COM 互操作
ms.date: 07/20/2015
helpviewer_keywords:
- Visual Basic code, COM interop
- COM interop [Visual Basic], in Visual Basic
ms.assetid: 3ffd1bdf-1b8d-47f5-87eb-75b659f64294
ms.openlocfilehash: 02ce21c6175f76bca17ae6ab57aa1569800167f4
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100460704"
---
# <a name="com-interop-visual-basic"></a><span data-ttu-id="c1605-103">COM 互操作 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="c1605-103">COM Interop (Visual Basic)</span></span>

<span data-ttu-id="c1605-104">组件对象模型 (COM) 允许对象向其他组件和主机应用公开自己的功能。</span><span class="sxs-lookup"><span data-stu-id="c1605-104">The Component Object Model (COM) allows an object to expose its functionality to other components and to host applications.</span></span> <span data-ttu-id="c1605-105">如今的大部分软件都包含 COM 对象。</span><span class="sxs-lookup"><span data-stu-id="c1605-105">Most of today's software includes COM objects.</span></span> <span data-ttu-id="c1605-106">尽管 .NET 程序集是新应用的最佳选择，有时也建议使用 COM 对象。</span><span class="sxs-lookup"><span data-stu-id="c1605-106">Although .NET assemblies are the best choice for new applications, you may at times need to employ COM objects.</span></span> <span data-ttu-id="c1605-107">本部分介绍与 Visual Basic 创建和使用 COM 对象相关的一些问题。</span><span class="sxs-lookup"><span data-stu-id="c1605-107">This section covers some of the issues associated with creating and using COM objects with Visual Basic.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="c1605-108">本节内容</span><span class="sxs-lookup"><span data-stu-id="c1605-108">In This Section</span></span>  

 [<span data-ttu-id="c1605-109">COM 互操作介绍</span><span class="sxs-lookup"><span data-stu-id="c1605-109">Introduction to COM Interop</span></span>](introduction-to-com-interop.md)  
 <span data-ttu-id="c1605-110">概述了 COM 互操作性。</span><span class="sxs-lookup"><span data-stu-id="c1605-110">Provides an overview of COM interoperability.</span></span>  
  
 [<span data-ttu-id="c1605-111">如何：从 Visual Basic 中引用 COM 对象</span><span class="sxs-lookup"><span data-stu-id="c1605-111">How to: Reference COM Objects from Visual Basic</span></span>](how-to-reference-com-objects.md)  
 <span data-ttu-id="c1605-112">介绍了如何添加对包含类型库的 COM 对象的引用。</span><span class="sxs-lookup"><span data-stu-id="c1605-112">Covers how to add references to COM objects that have type libraries.</span></span>  
  
 [<span data-ttu-id="c1605-113">如何：使用 ActiveX 控件</span><span class="sxs-lookup"><span data-stu-id="c1605-113">How to: Work with ActiveX Controls</span></span>](how-to-work-with-activex-controls.md)  
 <span data-ttu-id="c1605-114">演示如何使用现有 ActiveX 控件将功能添加到 Visual Studio "工具箱"。</span><span class="sxs-lookup"><span data-stu-id="c1605-114">Demonstrates how to use existing ActiveX controls to add features to the Visual Studio Toolbox.</span></span>  
  
 [<span data-ttu-id="c1605-115">演练：调用 Windows API</span><span class="sxs-lookup"><span data-stu-id="c1605-115">Walkthrough: Calling Windows APIs</span></span>](walkthrough-calling-windows-apis.md)  
 <span data-ttu-id="c1605-116">逐步介绍了如何调用属于 Windows 操作系统的 API。</span><span class="sxs-lookup"><span data-stu-id="c1605-116">Steps you through the process of calling the APIs that are part of the Windows operating system.</span></span>  
  
 [<span data-ttu-id="c1605-117">如何：调用 Windows API</span><span class="sxs-lookup"><span data-stu-id="c1605-117">How to: Call Windows APIs</span></span>](how-to-call-windows-apis.md)  
 <span data-ttu-id="c1605-118">展示了如何在 User32.dll 中定义和调用 `MessageBox` 函数。</span><span class="sxs-lookup"><span data-stu-id="c1605-118">Demonstrates how to define and call the `MessageBox` function in User32.dll.</span></span>  
  
 [<span data-ttu-id="c1605-119">如何：调用需要使用无符号类型的 Windows 函数</span><span class="sxs-lookup"><span data-stu-id="c1605-119">How to: Call a Windows Function that Takes Unsigned Types</span></span>](how-to-call-a-windows-function-that-takes-unsigned-types.md)  
 <span data-ttu-id="c1605-120">展示了如何调用包含无符号类型参数的 Windows 函数。</span><span class="sxs-lookup"><span data-stu-id="c1605-120">Demonstrates how to call a Windows function that has a parameter of an unsigned type.</span></span>  
  
 [<span data-ttu-id="c1605-121">演练：使用 Visual Basic 创建 COM 对象</span><span class="sxs-lookup"><span data-stu-id="c1605-121">Walkthrough: Creating COM Objects with Visual Basic</span></span>](walkthrough-creating-com-objects.md)  
 <span data-ttu-id="c1605-122">逐步介绍了如何使用和不使用 COM 类模板创建 COM 对象。</span><span class="sxs-lookup"><span data-stu-id="c1605-122">Steps you through the process of creating COM objects with and without the COM class template.</span></span>  
  
 [<span data-ttu-id="c1605-123">互操作性疑难解答</span><span class="sxs-lookup"><span data-stu-id="c1605-123">Troubleshooting Interoperability</span></span>](troubleshooting-interoperability.md)  
 <span data-ttu-id="c1605-124">介绍了一些在使用 COM 时可能会遇到的问题。</span><span class="sxs-lookup"><span data-stu-id="c1605-124">Covers some of the problems you may encounter when using COM.</span></span>  
  
 [<span data-ttu-id="c1605-125">.NET Framework 应用程序中的 COM 互操作性</span><span class="sxs-lookup"><span data-stu-id="c1605-125">COM Interoperability in .NET Framework Applications</span></span>](com-interoperability-in-net-framework-applications.md)  
 <span data-ttu-id="c1605-126">概述了如何在同一应用中使用 COM 对象和 .NET Framework 对象。</span><span class="sxs-lookup"><span data-stu-id="c1605-126">Provides an overview of how to use COM objects and .NET Framework objects in the same application.</span></span>  
  
 [<span data-ttu-id="c1605-127">演练：使用 COM 对象实现继承</span><span class="sxs-lookup"><span data-stu-id="c1605-127">Walkthrough: Implementing Inheritance with COM Objects</span></span>](walkthrough-implementing-inheritance-with-com-objects.md)  
 <span data-ttu-id="c1605-128">介绍了如何将现有 COM 对象用作新对象的基础。</span><span class="sxs-lookup"><span data-stu-id="c1605-128">Describes using existing COM objects as the basis for new objects.</span></span>  
  
## <a name="related-sections"></a><span data-ttu-id="c1605-129">相关章节</span><span class="sxs-lookup"><span data-stu-id="c1605-129">Related Sections</span></span>  

 [<span data-ttu-id="c1605-130">与非托管代码交互操作</span><span class="sxs-lookup"><span data-stu-id="c1605-130">Interoperating with Unmanaged Code</span></span>](../../../framework/interop/index.md)  
 <span data-ttu-id="c1605-131">描述由公共语言运行时提供的互操作性服务。</span><span class="sxs-lookup"><span data-stu-id="c1605-131">Describes interoperability services provided by the common language runtime.</span></span>  
  
 [<span data-ttu-id="c1605-132">向 .NET Framework 公开 COM 组件</span><span class="sxs-lookup"><span data-stu-id="c1605-132">Exposing COM Components to the .NET Framework</span></span>](../../../framework/interop/exposing-com-components.md)  
 <span data-ttu-id="c1605-133">介绍了如何通过 COM 互操作调用 COM 类型。</span><span class="sxs-lookup"><span data-stu-id="c1605-133">Describes the process of calling COM types through COM interop.</span></span>  
  
 [<span data-ttu-id="c1605-134">向 COM 公开 .NET Framework 组件</span><span class="sxs-lookup"><span data-stu-id="c1605-134">Exposing .NET Framework Components to COM</span></span>](../../../framework/interop/exposing-dotnet-components-to-com.md)  
 <span data-ttu-id="c1605-135">介绍了如何准备和使用 COM 中的托管类型。</span><span class="sxs-lookup"><span data-stu-id="c1605-135">Describes the preparation and use of managed types from COM.</span></span>  
  
 [<span data-ttu-id="c1605-136">应用互操作属性</span><span class="sxs-lookup"><span data-stu-id="c1605-136">Applying Interop Attributes</span></span>](../../../standard/native-interop/apply-interop-attributes.md)  
 <span data-ttu-id="c1605-137">介绍了在使用非托管代码时可以使用的属性。</span><span class="sxs-lookup"><span data-stu-id="c1605-137">Covers attributes you can use when working with unmanaged code.</span></span>
