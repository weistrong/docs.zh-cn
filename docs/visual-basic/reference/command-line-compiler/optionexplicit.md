---
description: 详细了解：-optionexplicit
title: -optionexplicit
ms.date: 07/20/2015
f1_keywords:
- /optionexplicit
- -optionexplicit
helpviewer_keywords:
- /optionexplicit compiler option [Visual Basic]
- optionexplicit compiler option [Visual Basic]
- -optionexplicit compiler option [Visual Basic]
ms.assetid: 5d296ab3-bafe-4c4d-9887-78f162ed86c7
ms.openlocfilehash: 4d1ab14bbf9de176de17fb5077f4bb919f5472b4
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100433557"
---
# <a name="-optionexplicit"></a><span data-ttu-id="3f5a0-103">-optionexplicit</span><span class="sxs-lookup"><span data-stu-id="3f5a0-103">-optionexplicit</span></span>

<span data-ttu-id="3f5a0-104">如果变量在使用之前未被声明，则会导致编译器报告错误。</span><span class="sxs-lookup"><span data-stu-id="3f5a0-104">Causes the compiler to report errors if variables are not declared before they are used.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3f5a0-105">语法</span><span class="sxs-lookup"><span data-stu-id="3f5a0-105">Syntax</span></span>  
  
```console  
-optionexplicit[+ | -]  
```  
  
## <a name="arguments"></a><span data-ttu-id="3f5a0-106">自变量</span><span class="sxs-lookup"><span data-stu-id="3f5a0-106">Arguments</span></span>  

 <span data-ttu-id="3f5a0-107">`+` &#124; `-`</span><span class="sxs-lookup"><span data-stu-id="3f5a0-107">`+` &#124; `-`</span></span>  
 <span data-ttu-id="3f5a0-108">可选。</span><span class="sxs-lookup"><span data-stu-id="3f5a0-108">Optional.</span></span> <span data-ttu-id="3f5a0-109">指定 `-optionexplicit+` 可要求显式声明变量。</span><span class="sxs-lookup"><span data-stu-id="3f5a0-109">Specify `-optionexplicit+` to require explicit declaration of variables.</span></span> <span data-ttu-id="3f5a0-110">`-optionexplicit+` 选项是默认选项，与 `-optionexplicit` 相同。</span><span class="sxs-lookup"><span data-stu-id="3f5a0-110">The `-optionexplicit+` option is the default and is the same as `-optionexplicit`.</span></span> <span data-ttu-id="3f5a0-111">`-optionexplicit-` 选项启用变量的隐式声明。</span><span class="sxs-lookup"><span data-stu-id="3f5a0-111">The `-optionexplicit-` option enables implicit declaration of variables.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="3f5a0-112">备注</span><span class="sxs-lookup"><span data-stu-id="3f5a0-112">Remarks</span></span>  

 <span data-ttu-id="3f5a0-113">如果源代码文件包含 [Option Explicit 语句](../../language-reference/statements/option-explicit-statement.md)，则语句将重写 `-optionexplicit` 命令行编译器设置。</span><span class="sxs-lookup"><span data-stu-id="3f5a0-113">If the source code file contains an [Option Explicit statement](../../language-reference/statements/option-explicit-statement.md), the statement overrides the `-optionexplicit` command-line compiler setting.</span></span>  
  
### <a name="to-set--optionexplicit-in-the-visual-studio-ide"></a><span data-ttu-id="3f5a0-114">若要在 Visual Studio IDE 中设置 -optionexplicit</span><span class="sxs-lookup"><span data-stu-id="3f5a0-114">To set -optionexplicit in the Visual Studio IDE</span></span>  
  
1. <span data-ttu-id="3f5a0-115">在 **“解决方案资源管理器”** 中选择一个项目。</span><span class="sxs-lookup"><span data-stu-id="3f5a0-115">Have a project selected in **Solution Explorer**.</span></span> <span data-ttu-id="3f5a0-116">在“项目”菜单上，单击“属性”   。</span><span class="sxs-lookup"><span data-stu-id="3f5a0-116">On the **Project** menu, click **Properties**.</span></span>
  
2. <span data-ttu-id="3f5a0-117">单击“编译”  选项卡。</span><span class="sxs-lookup"><span data-stu-id="3f5a0-117">Click the **Compile** tab.</span></span>  
  
3. <span data-ttu-id="3f5a0-118">修改“Option Explicit”框中的值。 </span><span class="sxs-lookup"><span data-stu-id="3f5a0-118">Modify the value in the **Option Explicit** box.</span></span>  
  
## <a name="example"></a><span data-ttu-id="3f5a0-119">示例</span><span class="sxs-lookup"><span data-stu-id="3f5a0-119">Example</span></span>  

 <span data-ttu-id="3f5a0-120">以下代码在使用 `-optionexplicit-` 时进行编译。</span><span class="sxs-lookup"><span data-stu-id="3f5a0-120">The following code compiles when `-optionexplicit-` is used.</span></span>  
  
 [!code-vb[VbVbalrCompiler#5](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrCompiler/VB/OptionExplicitOff.vb#5)]  
  
## <a name="see-also"></a><span data-ttu-id="3f5a0-121">请参阅</span><span class="sxs-lookup"><span data-stu-id="3f5a0-121">See also</span></span>

- [<span data-ttu-id="3f5a0-122">Visual Basic 命令行编译器</span><span class="sxs-lookup"><span data-stu-id="3f5a0-122">Visual Basic Command-Line Compiler</span></span>](index.md)
- [<span data-ttu-id="3f5a0-123">-optioncompare</span><span class="sxs-lookup"><span data-stu-id="3f5a0-123">-optioncompare</span></span>](optioncompare.md)
- [<span data-ttu-id="3f5a0-124">-optionstrict</span><span class="sxs-lookup"><span data-stu-id="3f5a0-124">-optionstrict</span></span>](optionstrict.md)
- [<span data-ttu-id="3f5a0-125">-optioninfer</span><span class="sxs-lookup"><span data-stu-id="3f5a0-125">-optioninfer</span></span>](optioninfer.md)
- [<span data-ttu-id="3f5a0-126">示例编译命令行</span><span class="sxs-lookup"><span data-stu-id="3f5a0-126">Sample Compilation Command Lines</span></span>](sample-compilation-command-lines.md)
- [<span data-ttu-id="3f5a0-127">Option Explicit 语句</span><span class="sxs-lookup"><span data-stu-id="3f5a0-127">Option Explicit Statement</span></span>](../../language-reference/statements/option-explicit-statement.md)
- [<span data-ttu-id="3f5a0-128">“选项”对话框 ->“项目”->“Visual Basic 默认值”</span><span class="sxs-lookup"><span data-stu-id="3f5a0-128">Visual Basic Defaults, Projects, Options Dialog Box</span></span>](/visualstudio/ide/reference/visual-basic-defaults-projects-options-dialog-box)
