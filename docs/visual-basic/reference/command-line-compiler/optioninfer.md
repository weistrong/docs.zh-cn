---
description: 详细了解：-optioninfer
title: -optioninfer
ms.date: 07/20/2015
f1_keywords:
- -optioninfer
helpviewer_keywords:
- -optioninfer compiler option [Visual Basic]
- /optioninfer compiler option [Visual Basic]
- optioninfer compiler option [Visual Basic]
ms.assetid: f6c09db1-0553-464a-abe3-d4510c61d6ed
ms.openlocfilehash: d45761914612a28788cc5c1a848d92238f05c162
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100475911"
---
# <a name="-optioninfer"></a><span data-ttu-id="a3067-103">-optioninfer</span><span class="sxs-lookup"><span data-stu-id="a3067-103">-optioninfer</span></span>

<span data-ttu-id="a3067-104">允许在变量声明中使用局部类型推理。</span><span class="sxs-lookup"><span data-stu-id="a3067-104">Enables the use of local type inference in variable declarations.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a3067-105">语法</span><span class="sxs-lookup"><span data-stu-id="a3067-105">Syntax</span></span>  
  
```console  
-optioninfer[+ | -]  
```  
  
## <a name="arguments"></a><span data-ttu-id="a3067-106">自变量</span><span class="sxs-lookup"><span data-stu-id="a3067-106">Arguments</span></span>  
  
|<span data-ttu-id="a3067-107">术语</span><span class="sxs-lookup"><span data-stu-id="a3067-107">Term</span></span>|<span data-ttu-id="a3067-108">定义</span><span class="sxs-lookup"><span data-stu-id="a3067-108">Definition</span></span>|  
|---|---|  
|<span data-ttu-id="a3067-109">`+` &#124; `-`</span><span class="sxs-lookup"><span data-stu-id="a3067-109">`+` &#124; `-`</span></span>|<span data-ttu-id="a3067-110">可选。</span><span class="sxs-lookup"><span data-stu-id="a3067-110">Optional.</span></span> <span data-ttu-id="a3067-111">指定 `-optioninfer+` 来启用局部类型推理，或指定 `-optioninfer-` 来阻止它。</span><span class="sxs-lookup"><span data-stu-id="a3067-111">Specify `-optioninfer+` to enable local type inference, or `-optioninfer-` to block it.</span></span> <span data-ttu-id="a3067-112">没有指定值的 `-optioninfer` 选项等同于 `-optioninfer+`。</span><span class="sxs-lookup"><span data-stu-id="a3067-112">The `-optioninfer` option, with no value specified, is the same as `-optioninfer+`.</span></span> <span data-ttu-id="a3067-113">不存在 `-optioninfer` 切换时，默认值也是 `-optioninfer+`。</span><span class="sxs-lookup"><span data-stu-id="a3067-113">The default value when the `-optioninfer` switch is not present is also `-optioninfer+`.</span></span> <span data-ttu-id="a3067-114">在 Vbc.rsp 响应文件中设置了默认值。</span><span class="sxs-lookup"><span data-stu-id="a3067-114">The default value is set in the Vbc.rsp response file.</span></span>|  
  
> [!NOTE]
> <span data-ttu-id="a3067-115">你可使用 `-noconfig` 选项来保留编译器的内部默认值(而非在 vbc.rsp 中指定的那些值）。</span><span class="sxs-lookup"><span data-stu-id="a3067-115">You can use the `-noconfig` option to retain the compiler's internal defaults instead of those specified in vbc.rsp.</span></span> <span data-ttu-id="a3067-116">此选项默认的编译器是 `-optioninfer-`。</span><span class="sxs-lookup"><span data-stu-id="a3067-116">The compiler default for this option is `-optioninfer-`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="a3067-117">备注</span><span class="sxs-lookup"><span data-stu-id="a3067-117">Remarks</span></span>  

 <span data-ttu-id="a3067-118">如果源代码文件包含 [Option Infer 语句](../../language-reference/statements/option-infer-statement.md)，则语句将重写 `-optioninfer` 命令行编译器设置。</span><span class="sxs-lookup"><span data-stu-id="a3067-118">If the source code file contains an [Option Infer Statement](../../language-reference/statements/option-infer-statement.md), the statement overrides the `-optioninfer` command-line compiler setting.</span></span>  
  
### <a name="to-set--optioninfer-in-the-visual-studio-ide"></a><span data-ttu-id="a3067-119">若要在 Visual Studio IDE 中设置 -optioninfer</span><span class="sxs-lookup"><span data-stu-id="a3067-119">To set -optioninfer in the Visual Studio IDE</span></span>  
  
1. <span data-ttu-id="a3067-120">在“解决方案资源管理器”  中选择项目。</span><span class="sxs-lookup"><span data-stu-id="a3067-120">Select a project in **Solution Explorer**.</span></span> <span data-ttu-id="a3067-121">在“项目”菜单上，单击“属性”   。</span><span class="sxs-lookup"><span data-stu-id="a3067-121">On the **Project** menu, click **Properties**.</span></span>  
  
2. <span data-ttu-id="a3067-122">在“编译”  选项卡上，修改“Option infer”  框中的值。</span><span class="sxs-lookup"><span data-stu-id="a3067-122">On the **Compile** tab, modify the value in the **Option infer** box.</span></span>  
  
## <a name="example"></a><span data-ttu-id="a3067-123">示例</span><span class="sxs-lookup"><span data-stu-id="a3067-123">Example</span></span>  

 <span data-ttu-id="a3067-124">以下代码在启用局部类型推理的情况下编译 `test.vb`。</span><span class="sxs-lookup"><span data-stu-id="a3067-124">The following code compiles `test.vb` with local type inference enabled.</span></span>  
  
```console
vbc -optioninfer+ test.vb  
```  
  
## <a name="see-also"></a><span data-ttu-id="a3067-125">请参阅</span><span class="sxs-lookup"><span data-stu-id="a3067-125">See also</span></span>

- [<span data-ttu-id="a3067-126">Visual Basic 命令行编译器</span><span class="sxs-lookup"><span data-stu-id="a3067-126">Visual Basic Command-Line Compiler</span></span>](index.md)
- [<span data-ttu-id="a3067-127">-optioncompare</span><span class="sxs-lookup"><span data-stu-id="a3067-127">-optioncompare</span></span>](optioncompare.md)
- [<span data-ttu-id="a3067-128">-optionexplicit</span><span class="sxs-lookup"><span data-stu-id="a3067-128">-optionexplicit</span></span>](optionexplicit.md)
- [<span data-ttu-id="a3067-129">-optionstrict</span><span class="sxs-lookup"><span data-stu-id="a3067-129">-optionstrict</span></span>](optionstrict.md)
- [<span data-ttu-id="a3067-130">示例编译命令行</span><span class="sxs-lookup"><span data-stu-id="a3067-130">Sample Compilation Command Lines</span></span>](sample-compilation-command-lines.md)
- [<span data-ttu-id="a3067-131">Option Infer 语句</span><span class="sxs-lookup"><span data-stu-id="a3067-131">Option Infer Statement</span></span>](../../language-reference/statements/option-infer-statement.md)
- [<span data-ttu-id="a3067-132">局部类型推理</span><span class="sxs-lookup"><span data-stu-id="a3067-132">Local Type Inference</span></span>](../../programming-guide/language-features/variables/local-type-inference.md)
- [<span data-ttu-id="a3067-133">“选项”对话框 ->“项目”->“Visual Basic 默认值”</span><span class="sxs-lookup"><span data-stu-id="a3067-133">Visual Basic Defaults, Projects, Options Dialog Box</span></span>](/visualstudio/ide/reference/visual-basic-defaults-projects-options-dialog-box)
- [<span data-ttu-id="a3067-134">“项目设计器”->“编译”页 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="a3067-134">Compile Page, Project Designer (Visual Basic)</span></span>](/visualstudio/ide/reference/compile-page-project-designer-visual-basic)
- [<span data-ttu-id="a3067-135">-noconfig</span><span class="sxs-lookup"><span data-stu-id="a3067-135">-noconfig</span></span>](noconfig.md)
- [<span data-ttu-id="a3067-136">从命令行生成</span><span class="sxs-lookup"><span data-stu-id="a3067-136">Building from the Command Line</span></span>](building-from-the-command-line.md)
