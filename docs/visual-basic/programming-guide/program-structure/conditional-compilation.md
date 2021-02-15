---
description: 了解详细信息： Visual Basic 中的条件编译
title: 条件编译
ms.date: 07/20/2015
helpviewer_keywords:
- conditional compilation [Visual Basic], about conditional compilation
- compilation [Visual Basic], conditional
ms.assetid: 9c35e55e-7eee-44fb-a586-dad1f1884848
ms.openlocfilehash: e9cb8a5af4dfbf2ffadef8edd8f6583614188391
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100476132"
---
# <a name="conditional-compilation-in-visual-basic"></a><span data-ttu-id="66753-103">Visual Basic 中的条件编译</span><span class="sxs-lookup"><span data-stu-id="66753-103">Conditional Compilation in Visual Basic</span></span>

<span data-ttu-id="66753-104">在 *条件编译* 中，程序中的特定代码块会有选择地编译，而其他代码块会被忽略。</span><span class="sxs-lookup"><span data-stu-id="66753-104">In *conditional compilation*, particular blocks of code in a program are compiled selectively while others are ignored.</span></span>  
  
 <span data-ttu-id="66753-105">例如，你可能想要编写调试语句来比较不同方法对相同编程任务的速度，或者可能想要针对多种语言对应用程序进行本地化。</span><span class="sxs-lookup"><span data-stu-id="66753-105">For example, you may want to write debugging statements that compare the speed of different approaches to the same programming task, or you may want to localize an application for multiple languages.</span></span> <span data-ttu-id="66753-106">条件编译语句设计为在编译时运行，而不是在运行时运行。</span><span class="sxs-lookup"><span data-stu-id="66753-106">Conditional compilation statements are designed to run during compile time, not at run time.</span></span>  
  
 <span data-ttu-id="66753-107">您可以用指令指示要有条件地编译的代码块 `#If...Then...#Else` 。</span><span class="sxs-lookup"><span data-stu-id="66753-107">You denote blocks of code to be conditionally compiled with the `#If...Then...#Else` directive.</span></span> <span data-ttu-id="66753-108">例如，若要从相同的源代码创建法语和德语版本的同一应用程序，可以 `#If...Then` 使用预定义的常量和将平台特定的代码段嵌入到语句中 `FrenchVersion` `GermanVersion` 。</span><span class="sxs-lookup"><span data-stu-id="66753-108">For example, to create French- and German-language versions of the same application from the same source code, you embed platform-specific code segments in `#If...Then` statements using the predefined constants `FrenchVersion` and `GermanVersion`.</span></span> <span data-ttu-id="66753-109">下面的示例演示如何执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="66753-109">The following example demonstrates how:</span></span>  
  
 [!code-vb[VbVbalrConditionalComp#5](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrConditionalComp/VB/Class1.vb#5)]  
  
 <span data-ttu-id="66753-110">如果在 `FrenchVersion` 编译时将条件编译常量的值设置为 `True` ，则编译法语版本的条件代码。</span><span class="sxs-lookup"><span data-stu-id="66753-110">If you set the value of the `FrenchVersion` conditional compilation constant to `True` at compile time, the conditional code for the French version is compiled.</span></span> <span data-ttu-id="66753-111">如果将常量的值设置 `GermanVersion` 为 `True` ，则编译器将使用德语版本。</span><span class="sxs-lookup"><span data-stu-id="66753-111">If you set the value of the `GermanVersion` constant to `True`, the compiler uses the German version.</span></span> <span data-ttu-id="66753-112">如果两者均未设置为 `True` ，则最后一个块中的代码将 `Else` 运行。</span><span class="sxs-lookup"><span data-stu-id="66753-112">If neither is set to `True`, the code in the last `Else` block runs.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="66753-113">当编辑代码时，自动完成功能将无法正常工作，如果代码不是当前分支的一部分，则使用条件编译指令。</span><span class="sxs-lookup"><span data-stu-id="66753-113">Autocompletion will not function when editing code and using conditional compilation directives if the code is not part of the current branch.</span></span>  
  
## <a name="declaring-conditional-compilation-constants"></a><span data-ttu-id="66753-114">声明条件编译常量</span><span class="sxs-lookup"><span data-stu-id="66753-114">Declaring Conditional Compilation Constants</span></span>  

 <span data-ttu-id="66753-115">可以通过以下三种方式之一来设置条件编译常量：</span><span class="sxs-lookup"><span data-stu-id="66753-115">You can set conditional compilation constants in one of three ways:</span></span>  
  
- <span data-ttu-id="66753-116">在 **项目设计器** 中</span><span class="sxs-lookup"><span data-stu-id="66753-116">In the **Project Designer**</span></span>  
  
- <span data-ttu-id="66753-117">使用命令行编译器时在命令行上</span><span class="sxs-lookup"><span data-stu-id="66753-117">At the command line when using the command-line compiler</span></span>  
  
- <span data-ttu-id="66753-118">在代码中</span><span class="sxs-lookup"><span data-stu-id="66753-118">In your code</span></span>  
  
 <span data-ttu-id="66753-119">条件编译常量具有特殊作用域，不能从标准代码进行访问。</span><span class="sxs-lookup"><span data-stu-id="66753-119">Conditional compilation constants have a special scope and cannot be accessed from standard code.</span></span> <span data-ttu-id="66753-120">条件编译常量的作用域取决于其设置方式。</span><span class="sxs-lookup"><span data-stu-id="66753-120">The scope of a conditional compilation constant is dependent on the way it is set.</span></span> <span data-ttu-id="66753-121">下表列出了使用上述三种方法声明的常量的作用域。</span><span class="sxs-lookup"><span data-stu-id="66753-121">The following table lists the scope of constants declared using each of the three ways mentioned above.</span></span>  
  
|<span data-ttu-id="66753-122">如何设置常量</span><span class="sxs-lookup"><span data-stu-id="66753-122">How constant is set</span></span>|<span data-ttu-id="66753-123">常量范围</span><span class="sxs-lookup"><span data-stu-id="66753-123">Scope of constant</span></span>|  
|---|---|  
|<span data-ttu-id="66753-124">**项目设计器**</span><span class="sxs-lookup"><span data-stu-id="66753-124">**Project Designer**</span></span>|<span data-ttu-id="66753-125">公共到项目中的所有文件</span><span class="sxs-lookup"><span data-stu-id="66753-125">Public to all files in the project</span></span>|  
|<span data-ttu-id="66753-126">命令行</span><span class="sxs-lookup"><span data-stu-id="66753-126">Command line</span></span>|<span data-ttu-id="66753-127">向传递到命令行编译器的所有文件公开</span><span class="sxs-lookup"><span data-stu-id="66753-127">Public to all files passed to the command-line compiler</span></span>|  
|<span data-ttu-id="66753-128">`#Const` 代码中的语句</span><span class="sxs-lookup"><span data-stu-id="66753-128">`#Const` statement in code</span></span>|<span data-ttu-id="66753-129">专用于声明它的文件</span><span class="sxs-lookup"><span data-stu-id="66753-129">Private to the file in which it is declared</span></span>|  
  
|<span data-ttu-id="66753-130">在项目设计器中设置常量</span><span class="sxs-lookup"><span data-stu-id="66753-130">To set constants in the Project Designer</span></span>|  
|---|  
|<span data-ttu-id="66753-131">-在创建可执行文件之前，请按照 [管理项目和解决方案属性](/visualstudio/ide/managing-project-and-solution-properties)中提供的步骤在 "**项目设计器**" 中设置常量。</span><span class="sxs-lookup"><span data-stu-id="66753-131">-   Before creating your executable file, set constants in the **Project Designer** by following the steps provided in [Managing Project and Solution Properties](/visualstudio/ide/managing-project-and-solution-properties).</span></span>|  
  
|<span data-ttu-id="66753-132">在命令行中设置常量</span><span class="sxs-lookup"><span data-stu-id="66753-132">To set constants at the command line</span></span>|  
|---|  
|<span data-ttu-id="66753-133">-使用 **-d** 开关输入条件编译常量，如以下示例中所示：</span><span class="sxs-lookup"><span data-stu-id="66753-133">-   Use the **-d** switch to enter conditional compilation constants, as in the following example:</span></span><br />     `vbc MyProj.vb /d:conFrenchVersion=–1:conANSI=0`<br />     <span data-ttu-id="66753-134">**-D** 开关和第一个常数之间不需要空格。</span><span class="sxs-lookup"><span data-stu-id="66753-134">No space is required between the **-d** switch and the first constant.</span></span> <span data-ttu-id="66753-135">有关详细信息，请参阅 [-定义 (Visual Basic) ](../../reference/command-line-compiler/define.md)。</span><span class="sxs-lookup"><span data-stu-id="66753-135">For more information, see [-define (Visual Basic)](../../reference/command-line-compiler/define.md).</span></span><br />     <span data-ttu-id="66753-136">命令行声明会重写在 **项目设计器** 中输入的声明，但不会将其删除。</span><span class="sxs-lookup"><span data-stu-id="66753-136">Command-line declarations override declarations entered in the **Project Designer**, but do not erase them.</span></span> <span data-ttu-id="66753-137">在 **项目设计器** 中设置的参数对于后续编译仍有效。</span><span class="sxs-lookup"><span data-stu-id="66753-137">Arguments set in **Project Designer** remain in effect for subsequent compilations.</span></span><br />     <span data-ttu-id="66753-138">在代码本身中编写常量时，没有严格的规则与它们的位置相关，因为它们的作用域是在其中声明它们的整个模块。</span><span class="sxs-lookup"><span data-stu-id="66753-138">When writing constants in the code itself, there are no strict rules as to their placement, since their scope is the entire module in which they are declared.</span></span>|  
  
|<span data-ttu-id="66753-139">若要在代码中设置常量</span><span class="sxs-lookup"><span data-stu-id="66753-139">To set constants in your code</span></span>|  
|---|  
|<span data-ttu-id="66753-140">-将常量放置在使用它们的模块的声明块中。</span><span class="sxs-lookup"><span data-stu-id="66753-140">-   Place the constants in the declaration block of the module in which they are used.</span></span> <span data-ttu-id="66753-141">这有助于保持代码的组织和可读性。</span><span class="sxs-lookup"><span data-stu-id="66753-141">This helps keep your code organized and easier to read.</span></span>|  
  
## <a name="related-topics"></a><span data-ttu-id="66753-142">相关主题</span><span class="sxs-lookup"><span data-stu-id="66753-142">Related Topics</span></span>  
  
|<span data-ttu-id="66753-143">Title</span><span class="sxs-lookup"><span data-stu-id="66753-143">Title</span></span>|<span data-ttu-id="66753-144">说明</span><span class="sxs-lookup"><span data-stu-id="66753-144">Description</span></span>|  
|---|---|  
|[<span data-ttu-id="66753-145">程序结构和代码约定</span><span class="sxs-lookup"><span data-stu-id="66753-145">Program Structure and Code Conventions</span></span>](program-structure-and-code-conventions.md)|<span data-ttu-id="66753-146">提供使代码易于阅读和维护的建议。</span><span class="sxs-lookup"><span data-stu-id="66753-146">Provides suggestions for making your code easy to read and maintain.</span></span>|  
  
## <a name="reference"></a><span data-ttu-id="66753-147">参考</span><span class="sxs-lookup"><span data-stu-id="66753-147">Reference</span></span>  

 [<span data-ttu-id="66753-148">#Const 指令</span><span class="sxs-lookup"><span data-stu-id="66753-148">#Const Directive</span></span>](../../language-reference/directives/const-directive.md)  
  
 [<span data-ttu-id="66753-149">#If...Then...#Else 指令</span><span class="sxs-lookup"><span data-stu-id="66753-149">#If...Then...#Else Directives</span></span>](../../language-reference/directives/if-then-else-directives.md)  
  
 [<span data-ttu-id="66753-150">-define (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="66753-150">-define (Visual Basic)</span></span>](../../reference/command-line-compiler/define.md)
