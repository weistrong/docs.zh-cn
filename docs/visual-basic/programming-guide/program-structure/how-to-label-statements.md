---
description: '了解有关详细信息，请参阅如何：标记语句 (Visual Basic) '
title: 如何：标记语句
ms.date: 07/20/2015
helpviewer_keywords:
- colons (:)
- statements [Visual Basic], labels
- ': separator character'
- Visual Basic code, labeling statements
ms.assetid: 38f1ff43-2054-42cb-963b-1998e60c6ed4
ms.openlocfilehash: 4efb320dad7d52f6e9b94f6e6f81730f94b5966b
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100433247"
---
# <a name="how-to-label-statements-visual-basic"></a><span data-ttu-id="839ee-103">如何：标记语句 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="839ee-103">How to: Label Statements (Visual Basic)</span></span>

<span data-ttu-id="839ee-104">语句块由用冒号分隔的代码行组成。</span><span class="sxs-lookup"><span data-stu-id="839ee-104">Statement blocks are made up of lines of code delimited by colons.</span></span> <span data-ttu-id="839ee-105">以标识字符串或整数开头的代码行称为 " *标记*"。</span><span class="sxs-lookup"><span data-stu-id="839ee-105">Lines of code preceded by an identifying string or integer are said to be *labeled*.</span></span> <span data-ttu-id="839ee-106">语句标签用于标记代码行，以将其标识为与等语句一起使用 `On Error Goto` 。</span><span class="sxs-lookup"><span data-stu-id="839ee-106">Statement labels are used to mark a line of code to identify it for use with statements such as `On Error Goto`.</span></span>

<span data-ttu-id="839ee-107">标签可以是有效 Visual Basic 标识符（如标识编程元素的标识符），也可以是整数文本。</span><span class="sxs-lookup"><span data-stu-id="839ee-107">Labels may be either valid Visual Basic identifiers—such as those that identify programming elements—or integer literals.</span></span> <span data-ttu-id="839ee-108">标签必须出现在源代码行的开头，并且必须后跟一个冒号，而不考虑它是否后跟同一行中的语句。</span><span class="sxs-lookup"><span data-stu-id="839ee-108">A label must appear at the beginning of a line of source code and must be followed by a colon, regardless of whether it is followed by a statement on the same line.</span></span>

<span data-ttu-id="839ee-109">编译器通过检查行首是否与任何已定义的标识符匹配来标识标签。</span><span class="sxs-lookup"><span data-stu-id="839ee-109">The compiler identifies labels by checking whether the beginning of the line matches any already-defined identifier.</span></span> <span data-ttu-id="839ee-110">如果不是，编译器将假定它是一个标签。</span><span class="sxs-lookup"><span data-stu-id="839ee-110">If it does not, the compiler assumes it is a label.</span></span>

<span data-ttu-id="839ee-111">标签具有自己的声明空间，不会干扰其他标识符。</span><span class="sxs-lookup"><span data-stu-id="839ee-111">Labels have their own declaration space and do not interfere with other identifiers.</span></span> <span data-ttu-id="839ee-112">标签的范围是方法的主体。</span><span class="sxs-lookup"><span data-stu-id="839ee-112">A label's scope is the body of the method.</span></span> <span data-ttu-id="839ee-113">标签声明优先于任何不明确的情况。</span><span class="sxs-lookup"><span data-stu-id="839ee-113">Label declaration takes precedence in any ambiguous situation.</span></span>

> [!NOTE]
> <span data-ttu-id="839ee-114">标签只能用于方法中的可执行语句。</span><span class="sxs-lookup"><span data-stu-id="839ee-114">Labels can be used only on executable statements inside methods.</span></span>

## <a name="to-label-a-line-of-code"></a><span data-ttu-id="839ee-115">为代码行添加标签</span><span class="sxs-lookup"><span data-stu-id="839ee-115">To label a line of code</span></span>

<span data-ttu-id="839ee-116">在源代码行的开头放置一个标识符，后跟一个冒号。</span><span class="sxs-lookup"><span data-stu-id="839ee-116">Place an identifier, followed by a colon, at the beginning of the line of source code.</span></span>

<span data-ttu-id="839ee-117">例如，以下代码行分别标记有 `Jump` 和 `120` ：</span><span class="sxs-lookup"><span data-stu-id="839ee-117">For example, the following lines of code are labeled with `Jump` and `120`, respectively:</span></span>

[!code-vb[VbVbalrStatements#708](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStatements/VB/Class1.vb#708)]

## <a name="see-also"></a><span data-ttu-id="839ee-118">请参阅</span><span class="sxs-lookup"><span data-stu-id="839ee-118">See also</span></span>

- [<span data-ttu-id="839ee-119">语句</span><span class="sxs-lookup"><span data-stu-id="839ee-119">Statements</span></span>](../language-features/statements.md)
- [<span data-ttu-id="839ee-120">Declared Element Names</span><span class="sxs-lookup"><span data-stu-id="839ee-120">Declared Element Names</span></span>](../language-features/declared-elements/declared-element-names.md)
- [<span data-ttu-id="839ee-121">程序结构和代码约定</span><span class="sxs-lookup"><span data-stu-id="839ee-121">Program Structure and Code Conventions</span></span>](program-structure-and-code-conventions.md)
