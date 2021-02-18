---
description: 详细了解：-linkresource (Visual Basic)
title: -linkresource
ms.date: 03/10/2018
helpviewer_keywords:
- /linkresource compiler option [Visual Basic]
- -linkresource compiler option [Visual Basic]
- linkresource compiler option [Visual Basic]
- /linkres compiler option [Visual Basic]
- linkres compiler option [Visual Basic]
- -linkres compiler option [Visual Basic]
ms.assetid: cf4dcad8-17b7-404c-9184-29358aa05b15
ms.openlocfilehash: 21fc47ecff44230bda0f445bc695706b5ae91eff
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100463697"
---
# <a name="-linkresource-visual-basic"></a><span data-ttu-id="f626b-103">-linkresource (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="f626b-103">-linkresource (Visual Basic)</span></span>

<span data-ttu-id="f626b-104">创建指向托管资源的链接。</span><span class="sxs-lookup"><span data-stu-id="f626b-104">Creates a link to a managed resource.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f626b-105">语法</span><span class="sxs-lookup"><span data-stu-id="f626b-105">Syntax</span></span>  
  
```console  
-linkresource:filename[,identifier[,public|private]]  
```

<span data-ttu-id="f626b-106">or</span><span class="sxs-lookup"><span data-stu-id="f626b-106">or</span></span>  

```console
-linkres:filename[,identifier[,public|private]]  
```  
  
## <a name="arguments"></a><span data-ttu-id="f626b-107">自变量</span><span class="sxs-lookup"><span data-stu-id="f626b-107">Arguments</span></span>  

 `filename`  
 <span data-ttu-id="f626b-108">必需。</span><span class="sxs-lookup"><span data-stu-id="f626b-108">Required.</span></span> <span data-ttu-id="f626b-109">要链接到程序集的资源文件。</span><span class="sxs-lookup"><span data-stu-id="f626b-109">The resource file to link to the assembly.</span></span> <span data-ttu-id="f626b-110">如果文件名包含空格，则将名称括在引号内 (" ")。</span><span class="sxs-lookup"><span data-stu-id="f626b-110">If the file name contains a space, enclose the name in quotation marks (" ").</span></span>  
  
 `identifier`  
 <span data-ttu-id="f626b-111">可选。</span><span class="sxs-lookup"><span data-stu-id="f626b-111">Optional.</span></span> <span data-ttu-id="f626b-112">资源的逻辑名称。</span><span class="sxs-lookup"><span data-stu-id="f626b-112">The logical name for the resource.</span></span> <span data-ttu-id="f626b-113">用于加载资源的名称。</span><span class="sxs-lookup"><span data-stu-id="f626b-113">The name that is used to load the resource.</span></span> <span data-ttu-id="f626b-114">默认值是文件的名称。</span><span class="sxs-lookup"><span data-stu-id="f626b-114">The default is the name of the file.</span></span> <span data-ttu-id="f626b-115">可以选择在程序集清单中指定文件是公共还是专用的，示例：`-linkres:filename.res,myname.res,public`。</span><span class="sxs-lookup"><span data-stu-id="f626b-115">Optionally, you can specify whether the file is public or private in the assembly manifest, for example: `-linkres:filename.res,myname.res,public`.</span></span> <span data-ttu-id="f626b-116">默认情况下，`filename` 在程序集中是公共的。</span><span class="sxs-lookup"><span data-stu-id="f626b-116">By default, `filename` is public in the assembly.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="f626b-117">备注</span><span class="sxs-lookup"><span data-stu-id="f626b-117">Remarks</span></span>  

 <span data-ttu-id="f626b-118">`-linkresource` 选项不会将资源文件嵌入到输出文件中；使用 `-resource` 选项来执行此操作。</span><span class="sxs-lookup"><span data-stu-id="f626b-118">The `-linkresource` option does not embed the resource file in the output file; use the `-resource` option to do this.</span></span>  
  
 <span data-ttu-id="f626b-119">`-linkresource` 选项需要除 `-target:module` 之外的任一 `-target` 选项。</span><span class="sxs-lookup"><span data-stu-id="f626b-119">The `-linkresource` option requires one of the `-target` options other than `-target:module`.</span></span>  
  
 <span data-ttu-id="f626b-120">例如，如果 `filename` 是由 [Resgen.exe（资源文件生成器）](../../../framework/tools/resgen-exe-resource-file-generator.md)创建的或在开发环境中创建的 .NET Framework 资源文件，则可使用 <xref:System.Resources> 命名空间中的成员来访问它。</span><span class="sxs-lookup"><span data-stu-id="f626b-120">If `filename` is a .NET Framework resource file created, for example, by the [Resgen.exe (Resource File Generator)](../../../framework/tools/resgen-exe-resource-file-generator.md) or in the development environment, it can be accessed with members in the <xref:System.Resources> namespace.</span></span> <span data-ttu-id="f626b-121">（有关详细信息，请参阅 <xref:System.Resources.ResourceManager>。）若要在运行时访问所有其他资源，请使用 <xref:System.Reflection.Assembly> 类中以 `GetManifestResource` 开头的方法。</span><span class="sxs-lookup"><span data-stu-id="f626b-121">(For more information, see <xref:System.Resources.ResourceManager>.) To access all other resources at run time, use the methods that begin with `GetManifestResource` in the <xref:System.Reflection.Assembly> class.</span></span>  
  
 <span data-ttu-id="f626b-122">文件名可以是任何文件格式。</span><span class="sxs-lookup"><span data-stu-id="f626b-122">The file name can be any file format.</span></span> <span data-ttu-id="f626b-123">例如，你可能希望生成程序集的本机 DLL 部分，从而可将它安装到全局程序集缓存中，并且可从该程序集中的托管代码访问它。</span><span class="sxs-lookup"><span data-stu-id="f626b-123">For example, you may want to make a native DLL part of the assembly, so that it can be installed into the global assembly cache and accessed from managed code in the assembly.</span></span>  
  
 <span data-ttu-id="f626b-124">`-linkresource` 的缩写形式是 `-linkres`。</span><span class="sxs-lookup"><span data-stu-id="f626b-124">The short form of `-linkresource` is `-linkres`.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="f626b-125">`-linkresource` 选项在Visual Studio 开发环境内无法使用；仅当从命令行编译时才可用。</span><span class="sxs-lookup"><span data-stu-id="f626b-125">The `-linkresource` option is not available from the Visual Studio development environment; it is available only when you compile from the command line.</span></span>  
  
## <a name="example"></a><span data-ttu-id="f626b-126">示例</span><span class="sxs-lookup"><span data-stu-id="f626b-126">Example</span></span>  

 <span data-ttu-id="f626b-127">下面的代码编译 `in.vb` 并链接到资源文件 `rf.resource`。</span><span class="sxs-lookup"><span data-stu-id="f626b-127">The following code compiles `in.vb` and links to resource file `rf.resource`.</span></span>  
  
```console  
vbc -linkresource:rf.resource in.vb  
```  
  
## <a name="see-also"></a><span data-ttu-id="f626b-128">请参阅</span><span class="sxs-lookup"><span data-stu-id="f626b-128">See also</span></span>

- [<span data-ttu-id="f626b-129">Visual Basic 命令行编译器</span><span class="sxs-lookup"><span data-stu-id="f626b-129">Visual Basic Command-Line Compiler</span></span>](index.md)
- [<span data-ttu-id="f626b-130">-target (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="f626b-130">-target (Visual Basic)</span></span>](target.md)
- [<span data-ttu-id="f626b-131">-resource (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="f626b-131">-resource (Visual Basic)</span></span>](resource.md)
- [<span data-ttu-id="f626b-132">示例编译命令行</span><span class="sxs-lookup"><span data-stu-id="f626b-132">Sample Compilation Command Lines</span></span>](sample-compilation-command-lines.md)
