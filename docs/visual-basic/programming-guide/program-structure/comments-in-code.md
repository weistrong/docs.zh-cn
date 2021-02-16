---
description: '了解详细信息：代码中的注释 (Visual Basic) '
title: 代码中的注释
ms.date: 07/20/2015
helpviewer_keywords:
- Uncomment button
- REM statement [Visual Basic]
- comments [Visual Basic], in code
- comments [Visual Basic], Visual Basic code
- Comment button
- buttons [Visual Basic], Uncomment
- buttons [Visual Basic], Comment
- code comments [Visual Basic], Visual Basic
- Visual Basic code, comments
- comments
- code comments
ms.assetid: 90136fba-22eb-49f9-ba81-63db629b4a47
ms.openlocfilehash: 66e12a18c2532bb5b694affccb84153f01bcddd5
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100461926"
---
# <a name="comments-in-code-visual-basic"></a><span data-ttu-id="1cac1-103">代码中的注释 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="1cac1-103">Comments in Code (Visual Basic)</span></span>

<span data-ttu-id="1cac1-104">阅读代码示例时，经常会遇到注释符号 (`'`)。</span><span class="sxs-lookup"><span data-stu-id="1cac1-104">As you read the code examples, you often encounter the comment symbol (`'`).</span></span> <span data-ttu-id="1cac1-105">此符号指示 Visual Basic 编译器忽略它后面的文本或 *注释*。</span><span class="sxs-lookup"><span data-stu-id="1cac1-105">This symbol tells the Visual Basic compiler to ignore the text following it, or the *comment*.</span></span> <span data-ttu-id="1cac1-106">注释是为了方便阅读而为代码添加的简短的解释性说明。</span><span class="sxs-lookup"><span data-stu-id="1cac1-106">Comments are brief explanatory notes added to code for the benefit of those reading it.</span></span>  
  
 <span data-ttu-id="1cac1-107">在所有过程的开头加入一段说明过程功能特征（过程的作用）的简短注释是一个很好的编程做法。</span><span class="sxs-lookup"><span data-stu-id="1cac1-107">It is good programming practice to begin all procedures with a brief comment describing the functional characteristics of the procedure (what it does).</span></span> <span data-ttu-id="1cac1-108">这对你自己和检查代码的任何其他人都有好处。</span><span class="sxs-lookup"><span data-stu-id="1cac1-108">This is for your own benefit and the benefit of anyone else who examines the code.</span></span> <span data-ttu-id="1cac1-109">应该把实现的详细信息（过程实现的方式）与描述功能特征的注释分开。</span><span class="sxs-lookup"><span data-stu-id="1cac1-109">You should separate the implementation details (how the procedure does it) from comments that describe the functional characteristics.</span></span> <span data-ttu-id="1cac1-110">若给说明加入了实现的详细信息，切记在更新函数时对这些详细信息进行更新。</span><span class="sxs-lookup"><span data-stu-id="1cac1-110">When you include implementation details in the description, remember to update them when you update the function.</span></span>  
  
 <span data-ttu-id="1cac1-111">注释可以和语句同行并跟随其后，也可以另占一整行。</span><span class="sxs-lookup"><span data-stu-id="1cac1-111">Comments can follow a statement on the same line, or occupy an entire line.</span></span> <span data-ttu-id="1cac1-112">以下代码阐释了这两种情况。</span><span class="sxs-lookup"><span data-stu-id="1cac1-112">Both are illustrated in the following code.</span></span>  
  
 [!code-vb[VbVbcnConventions#16](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnConventions/VB/Class1.vb#16)]  
  
 <span data-ttu-id="1cac1-113">如果注释需要多行，请在每行的前面使用注释符号，如以下示例所示。</span><span class="sxs-lookup"><span data-stu-id="1cac1-113">If your comment requires more than one line, use the comment symbol on each line, as the following example illustrates.</span></span>  
  
 [!code-vb[VbVbcnConventions#17](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnConventions/VB/Class1.vb#17)]  
  
## <a name="commenting-guidelines"></a><span data-ttu-id="1cac1-114">注释原则</span><span class="sxs-lookup"><span data-stu-id="1cac1-114">Commenting Guidelines</span></span>  

 <span data-ttu-id="1cac1-115">下表提供了在一段代码前可以加上哪些类型的注释的一般原则。</span><span class="sxs-lookup"><span data-stu-id="1cac1-115">The following table provides general guidelines for what types of comments can precede a section of code.</span></span> <span data-ttu-id="1cac1-116">这些是建议;Visual Basic 不会强制添加注释规则。</span><span class="sxs-lookup"><span data-stu-id="1cac1-116">These are suggestions; Visual Basic does not enforce rules for adding comments.</span></span> <span data-ttu-id="1cac1-117">编写注释时，应编写对你和代码的任何其他读者都最为有效的注释。</span><span class="sxs-lookup"><span data-stu-id="1cac1-117">Write what works best, both for you and for anyone else who reads your code.</span></span>  
  
|||  
|---|---|  
|<span data-ttu-id="1cac1-118">注释类型</span><span class="sxs-lookup"><span data-stu-id="1cac1-118">Comment type</span></span>|<span data-ttu-id="1cac1-119">注释说明</span><span class="sxs-lookup"><span data-stu-id="1cac1-119">Comment description</span></span>|  
|<span data-ttu-id="1cac1-120">目的</span><span class="sxs-lookup"><span data-stu-id="1cac1-120">Purpose</span></span>|<span data-ttu-id="1cac1-121">描述过程的用途（而不是其实现方式）</span><span class="sxs-lookup"><span data-stu-id="1cac1-121">Describes what the procedure does (not how it does it)</span></span>|  
|<span data-ttu-id="1cac1-122">假设</span><span class="sxs-lookup"><span data-stu-id="1cac1-122">Assumptions</span></span>|<span data-ttu-id="1cac1-123">列举每个外部变量、控件、打开的文件或过程访问的其他元素</span><span class="sxs-lookup"><span data-stu-id="1cac1-123">Lists each external variable, control, open file, or other element accessed by the procedure</span></span>|  
|<span data-ttu-id="1cac1-124">效果</span><span class="sxs-lookup"><span data-stu-id="1cac1-124">Effects</span></span>|<span data-ttu-id="1cac1-125">列举每个受影响的外部变量、控件、文件以及它的作用（仅在作用不明显时列举）</span><span class="sxs-lookup"><span data-stu-id="1cac1-125">Lists each affected external variable, control, or file, and the effect it has (only if it is not obvious)</span></span>|  
|<span data-ttu-id="1cac1-126">输入</span><span class="sxs-lookup"><span data-stu-id="1cac1-126">Inputs</span></span>|<span data-ttu-id="1cac1-127">指定自变量的用途</span><span class="sxs-lookup"><span data-stu-id="1cac1-127">Specifies the purpose of the argument</span></span>|  
|<span data-ttu-id="1cac1-128">返回</span><span class="sxs-lookup"><span data-stu-id="1cac1-128">Returns</span></span>|<span data-ttu-id="1cac1-129">说明过程返回的值</span><span class="sxs-lookup"><span data-stu-id="1cac1-129">Explains the values returned by the procedure</span></span>|  
  
 <span data-ttu-id="1cac1-130">请记住以下几点：</span><span class="sxs-lookup"><span data-stu-id="1cac1-130">Remember the following points:</span></span>  
  
- <span data-ttu-id="1cac1-131">每个重要的变量声明前都应有注释，用以描述被声明变量的用途。</span><span class="sxs-lookup"><span data-stu-id="1cac1-131">Every important variable declaration should be preceded by a comment describing the use of the variable being declared.</span></span>  
  
- <span data-ttu-id="1cac1-132">变量、控件和过程的命名应当足够清楚，使得只在遇到复杂的实现详细情况时才使用注释。</span><span class="sxs-lookup"><span data-stu-id="1cac1-132">Variables, controls, and procedures should be named clearly enough that commenting is needed only for complex implementation details.</span></span>  
  
- <span data-ttu-id="1cac1-133">注释不能与行继续符同行。</span><span class="sxs-lookup"><span data-stu-id="1cac1-133">Comments cannot follow a line-continuation sequence on the same line.</span></span>  
  
 <span data-ttu-id="1cac1-134">您可以通过在 Visual Studio 中选择一个或多个代码行，然后选择 " **注释** " ("Visual Basic 注释" 按钮，为代码块添加或删除注释符号 ![ 。 ](./media/comments-in-code/visual-basic-comment-button.gif)) 和 **取消注释** (![ visual studio 中的 Visual Basic 取消注释按钮。 ](./media/comments-in-code/visual-basic-uncomment-button.gif) **编辑** 工具栏上的) 按钮。</span><span class="sxs-lookup"><span data-stu-id="1cac1-134">You can add or remove comment symbols for a block of code by selecting one or more lines of code and choosing the **Comment** (![The Visual Basic Comment button in Visual Studio.](./media/comments-in-code/visual-basic-comment-button.gif)) and **Uncomment** (![The Visual Basic Uncomment button in Visual Studio.](./media/comments-in-code/visual-basic-uncomment-button.gif)) buttons on the **Edit** toolbar.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="1cac1-135">也可以用在文本前加关键字 `REM` 的方式给代码添加注释。</span><span class="sxs-lookup"><span data-stu-id="1cac1-135">You can also add comments to your code by preceding the text with the `REM` keyword.</span></span> <span data-ttu-id="1cac1-136">但是， `'` 符号和注释的 / **取消** 注释按钮更易于使用，并且需要的空间和内存更少。</span><span class="sxs-lookup"><span data-stu-id="1cac1-136">However, the `'` symbol and the **Comment**/**Uncomment** buttons are easier to use and require less space and memory.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1cac1-137">请参阅</span><span class="sxs-lookup"><span data-stu-id="1cac1-137">See also</span></span>

- [<span data-ttu-id="1cac1-138">基本直觉-通过 XML 注释记录代码</span><span class="sxs-lookup"><span data-stu-id="1cac1-138">Basic Instincts - Documenting Your Code With XML Comments</span></span>](/archive/msdn-magazine/2009/may/documenting-your-code-with-xml-comments)
- [<span data-ttu-id="1cac1-139">如何：创建 XML 文档</span><span class="sxs-lookup"><span data-stu-id="1cac1-139">How to: Create XML Documentation</span></span>](how-to-create-xml-documentation.md)
- [<span data-ttu-id="1cac1-140">XML 注释标记</span><span class="sxs-lookup"><span data-stu-id="1cac1-140">XML Comment Tags</span></span>](../../language-reference/xmldoc/index.md)
- [<span data-ttu-id="1cac1-141">程序结构和代码约定</span><span class="sxs-lookup"><span data-stu-id="1cac1-141">Program Structure and Code Conventions</span></span>](program-structure-and-code-conventions.md)
- [<span data-ttu-id="1cac1-142">REM 语句</span><span class="sxs-lookup"><span data-stu-id="1cac1-142">REM Statement</span></span>](../../language-reference/statements/rem-statement.md)
