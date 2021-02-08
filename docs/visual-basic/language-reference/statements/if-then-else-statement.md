---
description: '了解详细信息： If .。。Then .。。Else 语句 (Visual Basic) '
title: If...Then...Else 语句
ms.date: 04/16/2018
f1_keywords:
- vb.ElseIf
- vb.Then
- vb.If
- vb.EndIf
helpviewer_keywords:
- ElseIf statement [Visual Basic], If...Then...Else
- Then statement [Visual Basic], If...Then...Else
- control flow [Visual Basic], branching
- execution [Visual Basic], conditional
- TypeOf...Is expression, and If...Then...Else statements
- If...Then...Else statements
- If statement [Visual Basic], If...Then...Else
- If statement [Visual Basic]
- Is operator [Visual Basic], in If...Then...Else statements
- If Operator [Visual Basic]
- branching [Visual Basic], conditional
- If function [Visual Basic], and If...Then...Else statements
- Else statement [Visual Basic]
ms.assetid: 790068a2-1307-4e28-8a72-be5ebda099e9
ms.openlocfilehash: 83850771354b95f0e2d9c1bf1360a61d5264fe2e
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99769008"
---
# <a name="ifthenelse-statement-visual-basic"></a><span data-ttu-id="406fa-103">If...Then...Else 语句 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="406fa-103">If...Then...Else Statement (Visual Basic)</span></span>

<span data-ttu-id="406fa-104">根据表达式的值有条件地执行一组语句。</span><span class="sxs-lookup"><span data-stu-id="406fa-104">Conditionally executes a group of statements, depending on the value of an expression.</span></span>

## <a name="syntax"></a><span data-ttu-id="406fa-105">语法</span><span class="sxs-lookup"><span data-stu-id="406fa-105">Syntax</span></span>

```vb
' Multiline syntax:
If condition [ Then ]
    [ statements ]
[ ElseIf elseifcondition [ Then ]
    [ elseifstatements ] ]
[ Else
    [ elsestatements ] ]
End If

' Single-line syntax:
If condition Then [ statements ] [ Else [ elsestatements ] ]
```

## <a name="quick-links-to-example-code"></a><span data-ttu-id="406fa-106">示例代码的快速链接</span><span class="sxs-lookup"><span data-stu-id="406fa-106">Quick links to example code</span></span>

<span data-ttu-id="406fa-107">本文包含一些示例，这些示例演示了 `If` ... `Then`...`Else` 损益</span><span class="sxs-lookup"><span data-stu-id="406fa-107">This article includes several examples that illustrate uses of the `If`...`Then`...`Else` statement:</span></span>

- [<span data-ttu-id="406fa-108">多行语法示例</span><span class="sxs-lookup"><span data-stu-id="406fa-108">Multiline syntax example</span></span>](#multi-line)
- [<span data-ttu-id="406fa-109">嵌套语法示例</span><span class="sxs-lookup"><span data-stu-id="406fa-109">Nested syntax example</span></span>](#nested)
- [<span data-ttu-id="406fa-110">单行语法示例</span><span class="sxs-lookup"><span data-stu-id="406fa-110">Single-line syntax example</span></span>](#single-line)

## <a name="parts"></a><span data-ttu-id="406fa-111">组成部分</span><span class="sxs-lookup"><span data-stu-id="406fa-111">Parts</span></span>

`condition` \
<span data-ttu-id="406fa-112">必需。</span><span class="sxs-lookup"><span data-stu-id="406fa-112">Required.</span></span> <span data-ttu-id="406fa-113">表达式。</span><span class="sxs-lookup"><span data-stu-id="406fa-113">Expression.</span></span> <span data-ttu-id="406fa-114">的计算结果必须为 `True` 或 `False` ，或者是可隐式转换为的数据类型 `Boolean` 。</span><span class="sxs-lookup"><span data-stu-id="406fa-114">Must evaluate to `True` or `False`, or to a data type that is implicitly convertible to `Boolean`.</span></span>

<span data-ttu-id="406fa-115">如果表达式是一个计算结果为[空的可以为 null](../../programming-guide/language-features/data-types/nullable-value-types.md)的 `Boolean` 变量，则将条件视为，如果表达式为，则将计算该表达式，如果[](../nothing.md) `False` `ElseIf` 这些块存在，则将对其进行计算 `Else` 。</span><span class="sxs-lookup"><span data-stu-id="406fa-115">If the expression is a [Nullable](../../programming-guide/language-features/data-types/nullable-value-types.md) `Boolean` variable that evaluates to [Nothing](../nothing.md), the condition is treated as if the expression is `False`, and the `ElseIf` blocks are evaluated if they exist, or the `Else` block is executed if it exists.</span></span>

`Then` \
<span data-ttu-id="406fa-116">在单行语法中为必需;在多行语法中是可选的。</span><span class="sxs-lookup"><span data-stu-id="406fa-116">Required in the single-line syntax; optional in the multiline syntax.</span></span>

`statements` \
<span data-ttu-id="406fa-117">可选。</span><span class="sxs-lookup"><span data-stu-id="406fa-117">Optional.</span></span> <span data-ttu-id="406fa-118">后面`If`的一个或多个语句 ...如果计算结果为`True`，则执行。 `condition``Then`</span><span class="sxs-lookup"><span data-stu-id="406fa-118">One or more statements following `If`...`Then` that are executed if `condition` evaluates to `True`.</span></span>

`elseifcondition` \
<span data-ttu-id="406fa-119">如果 `ElseIf` 存在，则为必需。</span><span class="sxs-lookup"><span data-stu-id="406fa-119">Required if `ElseIf` is present.</span></span> <span data-ttu-id="406fa-120">表达式。</span><span class="sxs-lookup"><span data-stu-id="406fa-120">Expression.</span></span> <span data-ttu-id="406fa-121">的计算结果必须为 `True` 或 `False` ，或者是可隐式转换为的数据类型 `Boolean` 。</span><span class="sxs-lookup"><span data-stu-id="406fa-121">Must evaluate to `True` or `False`, or to a data type that is implicitly convertible to `Boolean`.</span></span>

`elseifstatements` \
<span data-ttu-id="406fa-122">可选。</span><span class="sxs-lookup"><span data-stu-id="406fa-122">Optional.</span></span> <span data-ttu-id="406fa-123">后面`ElseIf`的一个或多个语句 ...如果计算结果为`True`，则执行。 `elseifcondition``Then`</span><span class="sxs-lookup"><span data-stu-id="406fa-123">One or more statements following `ElseIf`...`Then` that are executed if `elseifcondition` evaluates to `True`.</span></span>

`elsestatements` \
<span data-ttu-id="406fa-124">可选。</span><span class="sxs-lookup"><span data-stu-id="406fa-124">Optional.</span></span> <span data-ttu-id="406fa-125">如果上一个或 `condition` `elseifcondition` 表达式的计算结果为，则执行的一个或多个语句 `True` 。</span><span class="sxs-lookup"><span data-stu-id="406fa-125">One or more statements that are executed if no previous `condition` or `elseifcondition` expression evaluates to `True`.</span></span>

`End If` \
<span data-ttu-id="406fa-126">终止的多行版本 `If` ... `Then`...`Else` 模块.</span><span class="sxs-lookup"><span data-stu-id="406fa-126">Terminates the multiline version of `If`...`Then`...`Else` block.</span></span>

## <a name="remarks"></a><span data-ttu-id="406fa-127">备注</span><span class="sxs-lookup"><span data-stu-id="406fa-127">Remarks</span></span>

### <a name="multiline-syntax"></a><span data-ttu-id="406fa-128">多行语法</span><span class="sxs-lookup"><span data-stu-id="406fa-128">Multiline syntax</span></span>

<span data-ttu-id="406fa-129">当 `If` ... `Then`...`Else` 语句时，将对其 `condition` 进行测试。</span><span class="sxs-lookup"><span data-stu-id="406fa-129">When an `If`...`Then`...`Else` statement is encountered, `condition` is tested.</span></span> <span data-ttu-id="406fa-130">如果 `condition` 为 `True` ，则执行以下语句 `Then` 。</span><span class="sxs-lookup"><span data-stu-id="406fa-130">If `condition` is `True`, the statements following `Then` are executed.</span></span> <span data-ttu-id="406fa-131">如果 `condition` 为 `False` ，则每个 `ElseIf` 语句 (如果按顺序计算任何) 。</span><span class="sxs-lookup"><span data-stu-id="406fa-131">If `condition` is `False`, each `ElseIf` statement (if there are any) is evaluated in order.</span></span> <span data-ttu-id="406fa-132">找到后 `True` `elseifcondition` ，将执行紧随关联的后面的语句 `ElseIf` 。</span><span class="sxs-lookup"><span data-stu-id="406fa-132">When a `True` `elseifcondition` is found, the statements immediately following the associated `ElseIf` are executed.</span></span> <span data-ttu-id="406fa-133">如果 `elseifcondition` 计算结果不为 `True` ，或者没有语句，则将 `ElseIf` 执行下面的语句 `Else` 。</span><span class="sxs-lookup"><span data-stu-id="406fa-133">If no `elseifcondition` evaluates to `True`, or if there are no `ElseIf` statements, the statements following `Else` are executed.</span></span> <span data-ttu-id="406fa-134">执行完后的语句后， `Then` `ElseIf` `Else` 将继续执行后面的语句 `End If` 。</span><span class="sxs-lookup"><span data-stu-id="406fa-134">After executing the statements following `Then`, `ElseIf`, or `Else`, execution continues with the statement following `End If`.</span></span>

<span data-ttu-id="406fa-135">`ElseIf`和 `Else` 子句均可选。</span><span class="sxs-lookup"><span data-stu-id="406fa-135">The `ElseIf` and `Else` clauses are both optional.</span></span> <span data-ttu-id="406fa-136">你可以 `ElseIf` 在 `If` ... `Then` 中包含任意数量的子句...`Else` 语句后，子句中不 `ElseIf` 能出现子句 `Else` 。</span><span class="sxs-lookup"><span data-stu-id="406fa-136">You can have as many `ElseIf` clauses as you want in an `If`...`Then`...`Else` statement, but no `ElseIf` clause can appear after an `Else` clause.</span></span> <span data-ttu-id="406fa-137">`If`...`Then`...`Else` 语句可以相互嵌套。</span><span class="sxs-lookup"><span data-stu-id="406fa-137">`If`...`Then`...`Else` statements can be nested within each other.</span></span>

<span data-ttu-id="406fa-138">在多行语法中， `If` 语句必须是第一行中的唯一语句。</span><span class="sxs-lookup"><span data-stu-id="406fa-138">In the multiline syntax, the `If` statement must be the only statement on the first line.</span></span> <span data-ttu-id="406fa-139">`ElseIf`、 `Else` 和 `End If` 语句前面只能有一个行标签。</span><span class="sxs-lookup"><span data-stu-id="406fa-139">The `ElseIf`, `Else`, and `End If` statements can be preceded only by a line label.</span></span> <span data-ttu-id="406fa-140">`If`... `Then`...`Else`块必须以语句结束 `End If` 。</span><span class="sxs-lookup"><span data-stu-id="406fa-140">The `If`...`Then`...`Else` block must end with an `End If` statement.</span></span>

> [!TIP]
> <span data-ttu-id="406fa-141">[Select .。。](select-case-statement.md)当你评估具有多个可能值的单个表达式时，Case 语句可能更有用。</span><span class="sxs-lookup"><span data-stu-id="406fa-141">The [Select...Case Statement](select-case-statement.md) might be more useful when you evaluate a single expression that has several possible values.</span></span>

### <a name="single-line-syntax"></a><span data-ttu-id="406fa-142">Single-Line 语法</span><span class="sxs-lookup"><span data-stu-id="406fa-142">Single-Line syntax</span></span>

<span data-ttu-id="406fa-143">对于一个条件，可以使用单行语法，如果该条件为 true，则执行代码。</span><span class="sxs-lookup"><span data-stu-id="406fa-143">You can use the single-line syntax for a single condition with code to execute if it's true.</span></span> <span data-ttu-id="406fa-144">不过，多行语法提供更多的结构和灵活性，更易于读取、维护和调试。</span><span class="sxs-lookup"><span data-stu-id="406fa-144">However, the multiple-line syntax provides more structure and flexibility and is easier to read, maintain, and debug.</span></span>

<span data-ttu-id="406fa-145">检查关键字后面的内容 `Then` ，以确定语句是否为单行语句 `If` 。</span><span class="sxs-lookup"><span data-stu-id="406fa-145">What follows the `Then` keyword is examined to determine whether a statement is a single-line `If`.</span></span> <span data-ttu-id="406fa-146">如果在同一行之后出现注释以外的任何内容 `Then` ，则该语句将被视为单行 `If` 语句。</span><span class="sxs-lookup"><span data-stu-id="406fa-146">If anything other than a comment appears after `Then` on the same line, the statement is treated as a single-line `If` statement.</span></span> <span data-ttu-id="406fa-147">如果 `Then` 不存在，则必须为多行的开头 `If` ... `Then`...`Else`.</span><span class="sxs-lookup"><span data-stu-id="406fa-147">If `Then` is absent, it must be the start of a multiple-line `If`...`Then`...`Else`.</span></span>

<span data-ttu-id="406fa-148">在单行语法中，可以将多个语句作为 `If` ... 决策的结果来执行。 `Then`</span><span class="sxs-lookup"><span data-stu-id="406fa-148">In the single-line syntax, you can have multiple statements executed as the result of an `If`...`Then` decision.</span></span> <span data-ttu-id="406fa-149">所有语句必须位于同一行上，并由冒号分隔。</span><span class="sxs-lookup"><span data-stu-id="406fa-149">All statements must be on the same line and be separated by colons.</span></span>

## <a name="multiline-syntax-example"></a><span data-ttu-id="406fa-150">多行语法示例</span><span class="sxs-lookup"><span data-stu-id="406fa-150">Multiline syntax example</span></span>

<a name="multi-line"></a>

<span data-ttu-id="406fa-151">下面的示例演示如何使用的多行语法 `If` 。 `Then`...`Else` 损益.</span><span class="sxs-lookup"><span data-stu-id="406fa-151">The following example illustrates the use of the multiline syntax of the `If`...`Then`...`Else` statement.</span></span>

[!code-vb[VbVbalrStatements#101](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStatements/VB/class6.vb#101)]

## <a name="nested-syntax-example"></a><span data-ttu-id="406fa-152">嵌套语法示例</span><span class="sxs-lookup"><span data-stu-id="406fa-152">Nested syntax example</span></span>

<a name="nested"></a>

<span data-ttu-id="406fa-153">下面的示例包含嵌套 `If` ... `Then`...`Else` 前瞻性.</span><span class="sxs-lookup"><span data-stu-id="406fa-153">The following example contains nested `If`...`Then`...`Else` statements.</span></span>

[!code-vb[VbVbalrStatements#102](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStatements/VB/class6.vb#102)]

## <a name="single-line-syntax-example"></a><span data-ttu-id="406fa-154">Single-Line 语法示例</span><span class="sxs-lookup"><span data-stu-id="406fa-154">Single-Line syntax example</span></span>

<a name="single-line"></a> <span data-ttu-id="406fa-155">下面的示例演示单行语法的用法。</span><span class="sxs-lookup"><span data-stu-id="406fa-155">The following example illustrates the use of the single-line syntax.</span></span>

[!code-vb[VbVbalrStatements#103](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStatements/VB/class6.vb#103)]

## <a name="see-also"></a><span data-ttu-id="406fa-156">请参阅</span><span class="sxs-lookup"><span data-stu-id="406fa-156">See also</span></span>

- <xref:Microsoft.VisualBasic.Interaction.Choose%2A>
- <xref:Microsoft.VisualBasic.Interaction.Switch%2A>
- [<span data-ttu-id="406fa-157">#If...Then...#Else 指令</span><span class="sxs-lookup"><span data-stu-id="406fa-157">#If...Then...#Else Directives</span></span>](../directives/if-then-else-directives.md)
- [<span data-ttu-id="406fa-158">Select...Case 语句</span><span class="sxs-lookup"><span data-stu-id="406fa-158">Select...Case Statement</span></span>](select-case-statement.md)
- [<span data-ttu-id="406fa-159">嵌套的控件结构</span><span class="sxs-lookup"><span data-stu-id="406fa-159">Nested Control Structures</span></span>](../../programming-guide/language-features/control-flow/nested-control-structures.md)
- [<span data-ttu-id="406fa-160">决策结构</span><span class="sxs-lookup"><span data-stu-id="406fa-160">Decision Structures</span></span>](../../programming-guide/language-features/control-flow/decision-structures.md)
- [<span data-ttu-id="406fa-161">Visual Basic 中的逻辑运算符和位运算符</span><span class="sxs-lookup"><span data-stu-id="406fa-161">Logical and Bitwise Operators in Visual Basic</span></span>](../../programming-guide/language-features/operators-and-expressions/logical-and-bitwise-operators.md)
- [<span data-ttu-id="406fa-162">If 运算符</span><span class="sxs-lookup"><span data-stu-id="406fa-162">If Operator</span></span>](../operators/if-operator.md)
