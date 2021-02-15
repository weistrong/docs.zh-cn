---
description: 了解详细信息： Visual Basic 中的串联运算符
title: 串联运算符
ms.date: 07/20/2015
helpviewer_keywords:
- '& operator [Visual Basic], concatenation'
- concatenation operators [Visual Basic]
- operators [Visual Basic], concatenation
- Visual Basic code, operators
- + operator [Visual Basic], concatenation
- concatenation operators [Visual Basic]
ms.assetid: e59908c3-89e0-41ae-933d-3e8826c16a04
ms.openlocfilehash: 7d007a830e4547f87e937cc7313c248485b4b574
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100476392"
---
# <a name="concatenation-operators-in-visual-basic"></a><span data-ttu-id="4618b-103">串联运算符 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="4618b-103">Concatenation Operators in Visual Basic</span></span>

<span data-ttu-id="4618b-104">串联运算符将多个字符串联接为一个字符串。</span><span class="sxs-lookup"><span data-stu-id="4618b-104">Concatenation operators join multiple strings into a single string.</span></span> <span data-ttu-id="4618b-105">有两种串联运算符：`+` 和 `&`。</span><span class="sxs-lookup"><span data-stu-id="4618b-105">There are two concatenation operators, `+` and `&`.</span></span> <span data-ttu-id="4618b-106">这两种串联运算符都执行基本的串联运算，如下面的示例所示。</span><span class="sxs-lookup"><span data-stu-id="4618b-106">Both carry out the basic concatenation operation, as the following example shows.</span></span>

```vb
Dim x As String = "Mic" & "ro" & "soft"
Dim y As String = "Mic" + "ro" + "soft"
' The preceding statements set both x and y to "Microsoft".
```

<span data-ttu-id="4618b-107">这两种运算符还可以串联 `String` 变量，如下面的示例所示。</span><span class="sxs-lookup"><span data-stu-id="4618b-107">These operators can also concatenate `String` variables, as the following example shows.</span></span>

[!code-vb[VbVbalrOperators#76](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrOperators/VB/Class1.vb#76)]

## <a name="differences-between-the-two-concatenation-operators"></a><span data-ttu-id="4618b-108">两种串联运算符之间的区别</span><span class="sxs-lookup"><span data-stu-id="4618b-108">Differences Between the Two Concatenation Operators</span></span>

<span data-ttu-id="4618b-109">[+ 运算符](../../../language-reference/operators/addition-operator.md)的主要目的是添加两个数字。</span><span class="sxs-lookup"><span data-stu-id="4618b-109">The [+ Operator](../../../language-reference/operators/addition-operator.md) has the primary purpose of adding two numbers.</span></span> <span data-ttu-id="4618b-110">然而，它还可以将数值操作数与字符串操作数串联起来。</span><span class="sxs-lookup"><span data-stu-id="4618b-110">However, it can also concatenate numeric operands with string operands.</span></span> <span data-ttu-id="4618b-111">`+` 操作数具有一套复杂的规则，用来确定是相加、串联、指示编译器错误还是引发运行时的 <xref:System.InvalidCastException> 异常。</span><span class="sxs-lookup"><span data-stu-id="4618b-111">The `+` operator has a complex set of rules that determine whether to add, concatenate, signal a compiler error, or throw a run-time <xref:System.InvalidCastException> exception.</span></span>

<span data-ttu-id="4618b-112">仅为操作数定义 [& 运算符](../../../language-reference/operators/concatenation-operator.md) `String` ，并且无论的设置如何，它始终将其操作数扩大到 `String` `Option Strict` 。</span><span class="sxs-lookup"><span data-stu-id="4618b-112">The [& Operator](../../../language-reference/operators/concatenation-operator.md) is defined only for `String` operands, and it always widens its operands to `String`, regardless of the setting of `Option Strict`.</span></span> <span data-ttu-id="4618b-113">对于字符串串联操作，建议使用 `&` 运算符，原因是它以独占方式为字符串定义，并降低产生意外转换的可能性。</span><span class="sxs-lookup"><span data-stu-id="4618b-113">The `&` operator is recommended for string concatenation because it is defined exclusively for strings and reduces your chances of generating an unintended conversion.</span></span>

## <a name="performance-string-and-stringbuilder"></a><span data-ttu-id="4618b-114">性能：字符串和 StringBuilder</span><span class="sxs-lookup"><span data-stu-id="4618b-114">Performance: String and StringBuilder</span></span>

<span data-ttu-id="4618b-115">如果你对字符串执行大量操作（如串联、删除或替换），则通过 <xref:System.Text.StringBuilder> 命名空间中的 <xref:System.Text> 类可能会提高性能。</span><span class="sxs-lookup"><span data-stu-id="4618b-115">If you do a significant number of manipulations on a string, such as concatenations, deletions, and replacements, your performance might profit from the <xref:System.Text.StringBuilder> class in the <xref:System.Text> namespace.</span></span> <span data-ttu-id="4618b-116">该类采用额外指令来创建和初始化 <xref:System.Text.StringBuilder> 对象，并且使用其他指令将其最终值转换为 `String`，但此时你可能会恢复使用 <xref:System.Text.StringBuilder>，因为它的执行速度更快。</span><span class="sxs-lookup"><span data-stu-id="4618b-116">It takes an extra instruction to create and initialize a <xref:System.Text.StringBuilder> object, and another instruction to convert its final value to a `String`, but you might recover this time because <xref:System.Text.StringBuilder> can perform faster.</span></span>

## <a name="see-also"></a><span data-ttu-id="4618b-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="4618b-117">See also</span></span>

- [<span data-ttu-id="4618b-118">Option Strict 语句</span><span class="sxs-lookup"><span data-stu-id="4618b-118">Option Strict Statement</span></span>](../../../language-reference/statements/option-strict-statement.md)
- [<span data-ttu-id="4618b-119">字符串操作方法的类型 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="4618b-119">Types of String Manipulation Methods in Visual Basic</span></span>](../strings/types-of-string-manipulation-methods.md)
- [<span data-ttu-id="4618b-120">算术运算符 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="4618b-120">Arithmetic Operators in Visual Basic</span></span>](arithmetic-operators.md)
- [<span data-ttu-id="4618b-121">Comparison Operators in Visual Basic</span><span class="sxs-lookup"><span data-stu-id="4618b-121">Comparison Operators in Visual Basic</span></span>](comparison-operators.md)
- [<span data-ttu-id="4618b-122">Visual Basic 中的逻辑运算符和位运算符</span><span class="sxs-lookup"><span data-stu-id="4618b-122">Logical and Bitwise Operators in Visual Basic</span></span>](logical-and-bitwise-operators.md)
