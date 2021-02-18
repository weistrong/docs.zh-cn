---
description: 详细了解：-addmodule
title: -addmodule
ms.date: 03/09/2018
helpviewer_keywords:
- /addmodule compiler option [Visual Basic]
- addmodule compiler option [Visual Basic]
- -addmodule compiler option [Visual Basic]
ms.assetid: fb4b89d4-4926-4f20-868d-427fa28497b2
ms.openlocfilehash: ca08aa599003897e680240af21c4a0eb568e31d8
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100468286"
---
# <a name="-addmodule"></a><span data-ttu-id="0aeed-103">-addmodule</span><span class="sxs-lookup"><span data-stu-id="0aeed-103">-addmodule</span></span>

<span data-ttu-id="0aeed-104">使编译器让指定文件中的所有类型信息可供当前正在编译的项目使用。</span><span class="sxs-lookup"><span data-stu-id="0aeed-104">Causes the compiler to make all type information from the specified file(s) available to the project you are currently compiling.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0aeed-105">语法</span><span class="sxs-lookup"><span data-stu-id="0aeed-105">Syntax</span></span>  
  
```console  
-addmodule:fileList  
```  
  
## <a name="arguments"></a><span data-ttu-id="0aeed-106">自变量</span><span class="sxs-lookup"><span data-stu-id="0aeed-106">Arguments</span></span>  

 `fileList`  
 <span data-ttu-id="0aeed-107">必需。</span><span class="sxs-lookup"><span data-stu-id="0aeed-107">Required.</span></span> <span data-ttu-id="0aeed-108">包含元数据但不包含程序集清单的文件的逗号分隔列表。</span><span class="sxs-lookup"><span data-stu-id="0aeed-108">Comma-delimited list of files that contain metadata but do not contain assembly manifests.</span></span> <span data-ttu-id="0aeed-109">包含空格的文件名称应括在引号 (" ") 中。</span><span class="sxs-lookup"><span data-stu-id="0aeed-109">File names containing spaces should be surrounded by quotation marks (" ").</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="0aeed-110">备注</span><span class="sxs-lookup"><span data-stu-id="0aeed-110">Remarks</span></span>  

 <span data-ttu-id="0aeed-111">由 `fileList` 参数列出的文件必须使用 `-target:module` 选项生成，或者使用其它编译器的 `-target:module` 等效项。</span><span class="sxs-lookup"><span data-stu-id="0aeed-111">The files listed by the `fileList` parameter must be created with the `-target:module` option, or with another compiler's equivalent to `-target:module`.</span></span>  
  
 <span data-ttu-id="0aeed-112">通过 `-addmodule` 添加的所有模块在运行时必须位于与输出文件相同的目录中。</span><span class="sxs-lookup"><span data-stu-id="0aeed-112">All modules added with `-addmodule` must be in the same directory as the output file at run time.</span></span> <span data-ttu-id="0aeed-113">也就是说，在编译时可在任何目录中指定模块，但在运行时该模块必须位于应用程序目录中。</span><span class="sxs-lookup"><span data-stu-id="0aeed-113">That is, you can specify a module in any directory at compile time, but the module must be in the application directory at run time.</span></span> <span data-ttu-id="0aeed-114">若非如此，你会获得 <xref:System.TypeLoadException> 错误。</span><span class="sxs-lookup"><span data-stu-id="0aeed-114">If it is not, you get a <xref:System.TypeLoadException> error.</span></span>  
  
 <span data-ttu-id="0aeed-115">若你使用 `-addmodule` 指定（隐式或显式）除 `-target:module` 之外的任何 [-target (Visual Basic)](target.md) 选项，传递给 `-addmodule` 的文件会成为该项目的程序集的一部分。</span><span class="sxs-lookup"><span data-stu-id="0aeed-115">If you specify (implicitly or explicitly) any[-target (Visual Basic)](target.md) option other than `-target:module` with `-addmodule`, the files you pass to `-addmodule` become part of the project's assembly.</span></span> <span data-ttu-id="0aeed-116">必须具有程序集，才能运行包含一个或多个由 `-addmodule` 添加的文件的输出文件。</span><span class="sxs-lookup"><span data-stu-id="0aeed-116">An assembly is required to run an output file that has one or more files added with `-addmodule`.</span></span>  
  
 <span data-ttu-id="0aeed-117">使用 [-reference (Visual Basic)](reference.md) 从包含程序集的文件导入元数据。</span><span class="sxs-lookup"><span data-stu-id="0aeed-117">Use [-reference (Visual Basic)](reference.md) to import metadata from a file that contains an assembly.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="0aeed-118">`-addmodule` 选项在 Visual Studio 开发环境内无法使用；仅当从命令行编译时才可用。</span><span class="sxs-lookup"><span data-stu-id="0aeed-118">The `-addmodule` option is not available from within the Visual Studio development environment; it is available only when compiling from the command line.</span></span>  
  
## <a name="example"></a><span data-ttu-id="0aeed-119">示例</span><span class="sxs-lookup"><span data-stu-id="0aeed-119">Example</span></span>  

 <span data-ttu-id="0aeed-120">下面的代码创建模块。</span><span class="sxs-lookup"><span data-stu-id="0aeed-120">The following code creates a module.</span></span>  
  
 [!code-vb[VbVbalrCompiler#47](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrCompiler/VB/OptionStrictOff.vb#47)]  
  
 <span data-ttu-id="0aeed-121">下面的代码导入模块的类型。</span><span class="sxs-lookup"><span data-stu-id="0aeed-121">The following code imports the module's types.</span></span>  
  
 [!code-vb[VbVbalrCompiler#48](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrCompiler/VB/OptionStrictOff.vb#48)]  
  
 <span data-ttu-id="0aeed-122">运行 `t1` 时，它会输出 `802`。</span><span class="sxs-lookup"><span data-stu-id="0aeed-122">When you run `t1`, it outputs `802`.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0aeed-123">请参阅</span><span class="sxs-lookup"><span data-stu-id="0aeed-123">See also</span></span>

- [<span data-ttu-id="0aeed-124">Visual Basic 命令行编译器</span><span class="sxs-lookup"><span data-stu-id="0aeed-124">Visual Basic Command-Line Compiler</span></span>](index.md)
- [<span data-ttu-id="0aeed-125">-target (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="0aeed-125">-target (Visual Basic)</span></span>](target.md)
- [<span data-ttu-id="0aeed-126">-reference (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="0aeed-126">-reference (Visual Basic)</span></span>](reference.md)
- [<span data-ttu-id="0aeed-127">示例编译命令行</span><span class="sxs-lookup"><span data-stu-id="0aeed-127">Sample Compilation Command Lines</span></span>](sample-compilation-command-lines.md)
