---
description: 详细了解：-vbruntime
title: -vbruntime
ms.date: 03/13/2018
f1_keywords:
- vbruntime
- -vbruntime
helpviewer_keywords:
- vbruntime compiler option [Visual Basic]
- -vbruntime compiler option [Visual Basic]
- /vbruntime compiler option [Visual Basic]
ms.assetid: 1aa0239e-511a-4c29-957d-fd72877b350a
ms.openlocfilehash: d542324e64ce31224aa75f164f121898a25f7be9
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100470144"
---
# <a name="-vbruntime"></a><span data-ttu-id="1266f-103">-vbruntime</span><span class="sxs-lookup"><span data-stu-id="1266f-103">-vbruntime</span></span>

<span data-ttu-id="1266f-104">指定编译器应在不引用 Visual Basic 运行库的情况下进行编译，或在引用特定运行库的情况下进行编译。</span><span class="sxs-lookup"><span data-stu-id="1266f-104">Specifies that the compiler should compile without a reference to the Visual Basic Runtime Library, or with a reference to a specific runtime library.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="1266f-105">语法</span><span class="sxs-lookup"><span data-stu-id="1266f-105">Syntax</span></span>  
  
```console  
-vbruntime:{ - | + | * | path }  
```  
  
## <a name="arguments"></a><span data-ttu-id="1266f-106">自变量</span><span class="sxs-lookup"><span data-stu-id="1266f-106">Arguments</span></span>  

 \-  
 <span data-ttu-id="1266f-107">在不引用 Visual Basic 运行时库的情况下进行编译。</span><span class="sxs-lookup"><span data-stu-id="1266f-107">Compile without a reference to the Visual Basic Runtime Library.</span></span>  
  
 \+  
 <span data-ttu-id="1266f-108">在引用默认 Visual Basic 运行时库的情况下进行编译。</span><span class="sxs-lookup"><span data-stu-id="1266f-108">Compile with a reference to the default Visual Basic Runtime Library.</span></span>  
  
 \*  
 <span data-ttu-id="1266f-109">在不引用 Visual Basic 运行时库的情况下进行编译，并将 Visual Basic 运行时库中的核心功能嵌入到程序集中。</span><span class="sxs-lookup"><span data-stu-id="1266f-109">Compile without a reference to the Visual Basic Runtime Library, and embed core functionality from the Visual Basic Runtime Library into the assembly.</span></span>  
  
 `path`  
 <span data-ttu-id="1266f-110">在引用指定库 (DLL) 的情况下进行编译。</span><span class="sxs-lookup"><span data-stu-id="1266f-110">Compile with a reference to the specified library (DLL).</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="1266f-111">备注</span><span class="sxs-lookup"><span data-stu-id="1266f-111">Remarks</span></span>  

 <span data-ttu-id="1266f-112">通过 `-vbruntime` 编译器选项可以指定应在不引用 Visual Basic 运行时库的情况下进行编译。</span><span class="sxs-lookup"><span data-stu-id="1266f-112">The `-vbruntime` compiler option enables you to specify that the compiler should compile without a reference to the Visual Basic Runtime Library.</span></span> <span data-ttu-id="1266f-113">如果在不引用 Visual Basic 运行时库的情况下进行编译，则会对生成 Visual Basic 运行时帮助程序调用的代码或语言构造记录错误或警告。</span><span class="sxs-lookup"><span data-stu-id="1266f-113">If you compile without a reference to the Visual Basic Runtime Library, errors or warnings are logged on code or language constructs that generate a call to a Visual Basic runtime helper.</span></span> <span data-ttu-id="1266f-114">（*Visual Basic 运行时帮助程序* 是 Microsoft.VisualBasic.dll 中定义的一个函数，在运行时调用以执行特定语言语义。）</span><span class="sxs-lookup"><span data-stu-id="1266f-114">(A *Visual Basic runtime helper* is a function defined in Microsoft.VisualBasic.dll that is called at runtime to execute a specific language semantic.)</span></span>  
  
 <span data-ttu-id="1266f-115">`-vbruntime+` 选项会生成在未指定 `-vbruntime` 开关时发生的相同行为。</span><span class="sxs-lookup"><span data-stu-id="1266f-115">The `-vbruntime+` option produces the same behavior that occurs if no `-vbruntime` switch is specified.</span></span> <span data-ttu-id="1266f-116">可以使用 `-vbruntime+` 选项重写以前的 `-vbruntime` 开关。</span><span class="sxs-lookup"><span data-stu-id="1266f-116">You can use the `-vbruntime+` option to override previous `-vbruntime` switches.</span></span>  
  
 <span data-ttu-id="1266f-117">使用 `-vbruntime-` 或 `-vbruntime:path` 选项时，`My` 类型的大多数对象不可用。</span><span class="sxs-lookup"><span data-stu-id="1266f-117">Most objects of the `My` type are unavailable when you use the `-vbruntime-` or `-vbruntime:path` options.</span></span>  
  
## <a name="embedding-visual-basic-runtime-core-functionality"></a><span data-ttu-id="1266f-118">嵌入 Visual Basic 运行时核心功能</span><span class="sxs-lookup"><span data-stu-id="1266f-118">Embedding Visual Basic Runtime core functionality</span></span>  

 <span data-ttu-id="1266f-119">通过 `-vbruntime*` 选项可以在不引用运行时库的情况下进行编译。</span><span class="sxs-lookup"><span data-stu-id="1266f-119">The `-vbruntime*` option enables you to compile without a reference to a runtime library.</span></span> <span data-ttu-id="1266f-120">而是将 Visual Basic 运行时库中的核心功能嵌入在用户程序集中。</span><span class="sxs-lookup"><span data-stu-id="1266f-120">Instead, core functionality from the Visual Basic Runtime Library is embedded in the user assembly.</span></span> <span data-ttu-id="1266f-121">如果应用程序在不包含 Visual Basic 运行时的平台上运行，则可以使用此选项。</span><span class="sxs-lookup"><span data-stu-id="1266f-121">You can use this option if your application runs on platforms that do not contain the Visual Basic runtime.</span></span>  
  
 <span data-ttu-id="1266f-122">会嵌入以下运行时成员：</span><span class="sxs-lookup"><span data-stu-id="1266f-122">The following runtime members are embedded:</span></span>  
  
- <span data-ttu-id="1266f-123"><xref:Microsoft.VisualBasic.CompilerServices.Conversions> 类</span><span class="sxs-lookup"><span data-stu-id="1266f-123"><xref:Microsoft.VisualBasic.CompilerServices.Conversions> class</span></span>  
  
- <span data-ttu-id="1266f-124"><xref:Microsoft.VisualBasic.Strings.AscW%28System.Char%29> 方法</span><span class="sxs-lookup"><span data-stu-id="1266f-124"><xref:Microsoft.VisualBasic.Strings.AscW%28System.Char%29> method</span></span>  
  
- <span data-ttu-id="1266f-125"><xref:Microsoft.VisualBasic.Strings.AscW%28System.String%29> 方法</span><span class="sxs-lookup"><span data-stu-id="1266f-125"><xref:Microsoft.VisualBasic.Strings.AscW%28System.String%29> method</span></span>  
  
- <span data-ttu-id="1266f-126"><xref:Microsoft.VisualBasic.Strings.ChrW%28System.Int32%29> 方法</span><span class="sxs-lookup"><span data-stu-id="1266f-126"><xref:Microsoft.VisualBasic.Strings.ChrW%28System.Int32%29> method</span></span>  
  
- <span data-ttu-id="1266f-127"><xref:Microsoft.VisualBasic.Constants.vbBack> 常数</span><span class="sxs-lookup"><span data-stu-id="1266f-127"><xref:Microsoft.VisualBasic.Constants.vbBack> constant</span></span>  
  
- <span data-ttu-id="1266f-128"><xref:Microsoft.VisualBasic.Constants.vbCr> 常数</span><span class="sxs-lookup"><span data-stu-id="1266f-128"><xref:Microsoft.VisualBasic.Constants.vbCr> constant</span></span>  
  
- <span data-ttu-id="1266f-129"><xref:Microsoft.VisualBasic.Constants.vbCrLf> 常数</span><span class="sxs-lookup"><span data-stu-id="1266f-129"><xref:Microsoft.VisualBasic.Constants.vbCrLf> constant</span></span>  
  
- <span data-ttu-id="1266f-130"><xref:Microsoft.VisualBasic.Constants.vbFormFeed> 常数</span><span class="sxs-lookup"><span data-stu-id="1266f-130"><xref:Microsoft.VisualBasic.Constants.vbFormFeed> constant</span></span>  
  
- <span data-ttu-id="1266f-131"><xref:Microsoft.VisualBasic.Constants.vbLf> 常数</span><span class="sxs-lookup"><span data-stu-id="1266f-131"><xref:Microsoft.VisualBasic.Constants.vbLf> constant</span></span>  
  
- <span data-ttu-id="1266f-132"><xref:Microsoft.VisualBasic.Constants.vbNewLine> 常数</span><span class="sxs-lookup"><span data-stu-id="1266f-132"><xref:Microsoft.VisualBasic.Constants.vbNewLine> constant</span></span>  
  
- <span data-ttu-id="1266f-133"><xref:Microsoft.VisualBasic.Constants.vbNullChar> 常数</span><span class="sxs-lookup"><span data-stu-id="1266f-133"><xref:Microsoft.VisualBasic.Constants.vbNullChar> constant</span></span>  
  
- <span data-ttu-id="1266f-134"><xref:Microsoft.VisualBasic.Constants.vbNullString> 常数</span><span class="sxs-lookup"><span data-stu-id="1266f-134"><xref:Microsoft.VisualBasic.Constants.vbNullString> constant</span></span>  
  
- <span data-ttu-id="1266f-135"><xref:Microsoft.VisualBasic.Constants.vbTab> 常数</span><span class="sxs-lookup"><span data-stu-id="1266f-135"><xref:Microsoft.VisualBasic.Constants.vbTab> constant</span></span>  
  
- <span data-ttu-id="1266f-136"><xref:Microsoft.VisualBasic.Constants.vbVerticalTab> 常数</span><span class="sxs-lookup"><span data-stu-id="1266f-136"><xref:Microsoft.VisualBasic.Constants.vbVerticalTab> constant</span></span>  
  
- <span data-ttu-id="1266f-137">`My` 类型的某些对象</span><span class="sxs-lookup"><span data-stu-id="1266f-137">Some objects of the `My` type</span></span>  
  
 <span data-ttu-id="1266f-138">如果使用 `-vbruntime*` 选项进行编译，并且代码从没有嵌入核心功能的 Visual Basic 运行时库中引用了一个成员，则编译器会返回错误，指示该成员不可用。</span><span class="sxs-lookup"><span data-stu-id="1266f-138">If you compile using the `-vbruntime*` option and your code references a member from the Visual Basic Runtime Library that is not embedded with the core functionality, the compiler returns an error that indicates that the member is not available.</span></span>  
  
## <a name="referencing-a-specified-library"></a><span data-ttu-id="1266f-139">引用指定库</span><span class="sxs-lookup"><span data-stu-id="1266f-139">Referencing a specified library</span></span>  

 <span data-ttu-id="1266f-140">可以使用 `path` 参数在引用自定义运行时库（而不是默认 Visual Basic 运行时库）的情况下进行编译。</span><span class="sxs-lookup"><span data-stu-id="1266f-140">You can use the `path` argument to compile with a reference to a custom runtime library instead of the default Visual Basic Runtime Library.</span></span>  
  
 <span data-ttu-id="1266f-141">如果 `path` 参数的值是 DLL 的完全限定路径，则编译器将使用该文件作为运行时库。</span><span class="sxs-lookup"><span data-stu-id="1266f-141">If the value for the `path` argument is a fully qualified path to a DLL, the compiler will use that file as the runtime library.</span></span> <span data-ttu-id="1266f-142">如果 `path` 参数的值不是 DLL 的完全限定路径，则 Visual Basic 编译器将首先在当前文件夹中搜索标识的 DLL。</span><span class="sxs-lookup"><span data-stu-id="1266f-142">If the value for the `path` argument is not a fully qualified path to a DLL, the Visual Basic compiler will search for the identified DLL in the current folder first.</span></span> <span data-ttu-id="1266f-143">随后它将在使用 [-sdkpath](sdkpath.md) 编译器选项指定的路径中进行搜索。</span><span class="sxs-lookup"><span data-stu-id="1266f-143">It will then search in the path that you have specified by using the [-sdkpath](sdkpath.md) compiler option.</span></span> <span data-ttu-id="1266f-144">如果未使用 `-sdkpath` 编译器选项，则编译器将在 .NET Framework 文件夹 (`%systemroot%\Microsoft.NET\Framework\versionNumber`) 中搜索标识的 DLL。</span><span class="sxs-lookup"><span data-stu-id="1266f-144">If the `-sdkpath` compiler option is not used, the compiler will search for the identified DLL in the .NET Framework folder (`%systemroot%\Microsoft.NET\Framework\versionNumber`).</span></span>  
  
## <a name="example"></a><span data-ttu-id="1266f-145">示例</span><span class="sxs-lookup"><span data-stu-id="1266f-145">Example</span></span>  

 <span data-ttu-id="1266f-146">下面的示例演示如何使用 `-vbruntime` 选项在引用自定义库的情况下进行编译。</span><span class="sxs-lookup"><span data-stu-id="1266f-146">The following example shows how to use the `-vbruntime` option to compile with a reference to a custom library.</span></span>  
  
```console
vbc -vbruntime:C:\VBLibraries\CustomVBLibrary.dll  
```  
  
## <a name="see-also"></a><span data-ttu-id="1266f-147">请参阅</span><span class="sxs-lookup"><span data-stu-id="1266f-147">See also</span></span>

- [<span data-ttu-id="1266f-148">Visual Basic 核心 – Visual Studio 2010 SP1 中的新编译模式</span><span class="sxs-lookup"><span data-stu-id="1266f-148">Visual Basic Core – New compilation mode in Visual Studio 2010 SP1</span></span>](https://devblogs.microsoft.com/vbteam/vb-core-new-compilation-mode-in-visual-studio-2010-sp1/)
- [<span data-ttu-id="1266f-149">Visual Basic 命令行编译器</span><span class="sxs-lookup"><span data-stu-id="1266f-149">Visual Basic Command-Line Compiler</span></span>](index.md)
- [<span data-ttu-id="1266f-150">示例编译命令行</span><span class="sxs-lookup"><span data-stu-id="1266f-150">Sample Compilation Command Lines</span></span>](sample-compilation-command-lines.md)
- [<span data-ttu-id="1266f-151">-sdkpath</span><span class="sxs-lookup"><span data-stu-id="1266f-151">-sdkpath</span></span>](sdkpath.md)
