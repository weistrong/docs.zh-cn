---
description: '了解有关以下方面的详细信息： If Operator (Visual Basic) '
title: If 运算符
ms.date: 07/20/2015
f1_keywords:
- vb.IfOperator
- IfOperator
helpviewer_keywords:
- ternary operators [Visual Basic]
- conditional execution
- If expressions [Visual Basic]
- conditional operator [Visual Basic]
- If Operator [Visual Basic]
ms.assetid: dd56c9df-7cd4-442c-9ba6-20c70ee44c8f
ms.openlocfilehash: 3b25ab4b6c5f0d2608644adb6e35ff4ad5128f42
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99665869"
---
# <a name="if-operator-visual-basic"></a><span data-ttu-id="64e8e-103">If 运算符 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="64e8e-103">If Operator (Visual Basic)</span></span>

<span data-ttu-id="64e8e-104">使用短路计算有条件地返回两个值中的一个值。</span><span class="sxs-lookup"><span data-stu-id="64e8e-104">Uses short-circuit evaluation to conditionally return one of two values.</span></span> <span data-ttu-id="64e8e-105">`If`可以用三个参数或两个参数调用运算符。</span><span class="sxs-lookup"><span data-stu-id="64e8e-105">The `If` operator can be called with three arguments or with two arguments.</span></span>

## <a name="syntax"></a><span data-ttu-id="64e8e-106">语法</span><span class="sxs-lookup"><span data-stu-id="64e8e-106">Syntax</span></span>

```vb
If( [argument1,] argument2, argument3 )
```

## <a name="if-operator-called-with-three-arguments"></a><span data-ttu-id="64e8e-107">如果调用运算符时有三个参数</span><span class="sxs-lookup"><span data-stu-id="64e8e-107">If operator called with three arguments</span></span>

<span data-ttu-id="64e8e-108">`If`使用三个参数调用时，第一个参数的计算结果必须为可强制转换为的值 `Boolean` 。</span><span class="sxs-lookup"><span data-stu-id="64e8e-108">When `If` is called by using three arguments, the first argument must evaluate to a value that can be cast as a `Boolean`.</span></span> <span data-ttu-id="64e8e-109">`Boolean`该值将确定计算并返回其他两个参数中的哪一个。</span><span class="sxs-lookup"><span data-stu-id="64e8e-109">That `Boolean` value will determine which of the other two arguments is evaluated and returned.</span></span> <span data-ttu-id="64e8e-110">以下列表仅适用于 `If` 使用三个参数调用运算符的情况。</span><span class="sxs-lookup"><span data-stu-id="64e8e-110">The following list applies only when the `If` operator is called by using three arguments.</span></span>

### <a name="parts"></a><span data-ttu-id="64e8e-111">组成部分</span><span class="sxs-lookup"><span data-stu-id="64e8e-111">Parts</span></span>

|<span data-ttu-id="64e8e-112">术语</span><span class="sxs-lookup"><span data-stu-id="64e8e-112">Term</span></span>|<span data-ttu-id="64e8e-113">定义</span><span class="sxs-lookup"><span data-stu-id="64e8e-113">Definition</span></span>|
|---|---|
|`argument1`|<span data-ttu-id="64e8e-114">必需。</span><span class="sxs-lookup"><span data-stu-id="64e8e-114">Required.</span></span> <span data-ttu-id="64e8e-115">`Boolean`.</span><span class="sxs-lookup"><span data-stu-id="64e8e-115">`Boolean`.</span></span> <span data-ttu-id="64e8e-116">确定要计算和返回的其他参数的值。</span><span class="sxs-lookup"><span data-stu-id="64e8e-116">Determines which of the other arguments to evaluate and return.</span></span>|
|`argument2`|<span data-ttu-id="64e8e-117">必需。</span><span class="sxs-lookup"><span data-stu-id="64e8e-117">Required.</span></span> <span data-ttu-id="64e8e-118">`Object`.</span><span class="sxs-lookup"><span data-stu-id="64e8e-118">`Object`.</span></span> <span data-ttu-id="64e8e-119">如果计算结果为，则计算并返回 `argument1` `True` 。</span><span class="sxs-lookup"><span data-stu-id="64e8e-119">Evaluated and returned if `argument1` evaluates to `True`.</span></span>|
|`argument3`|<span data-ttu-id="64e8e-120">必需。</span><span class="sxs-lookup"><span data-stu-id="64e8e-120">Required.</span></span> <span data-ttu-id="64e8e-121">`Object`.</span><span class="sxs-lookup"><span data-stu-id="64e8e-121">`Object`.</span></span> <span data-ttu-id="64e8e-122">如果计算结果为，则计算并返回， `argument1` `False` 如果 `argument1` 为[可为空](../../programming-guide/language-features/data-types/nullable-value-types.md)的 `Boolean` 变量， [](../nothing.md)则为。</span><span class="sxs-lookup"><span data-stu-id="64e8e-122">Evaluated and returned if `argument1` evaluates to `False` or if `argument1` is a [Nullable](../../programming-guide/language-features/data-types/nullable-value-types.md)`Boolean` variable that evaluates to [Nothing](../nothing.md).</span></span>|

<span data-ttu-id="64e8e-123">`If`使用三个参数调用的运算符的工作方式类似于 `IIf` 函数，只不过它使用短路计算。</span><span class="sxs-lookup"><span data-stu-id="64e8e-123">An `If` operator that is called with three arguments works like an `IIf` function except that it uses short-circuit evaluation.</span></span> <span data-ttu-id="64e8e-124">`IIf`函数始终计算其所有三个参数，而 `If` 具有三个参数的运算符只计算两个参数中的两个。</span><span class="sxs-lookup"><span data-stu-id="64e8e-124">An `IIf` function always evaluates all three of its arguments, whereas an `If` operator that has three arguments evaluates only two of them.</span></span> <span data-ttu-id="64e8e-125">计算第一个 `If` 参数，并将结果强制转换为 `Boolean` 值， `True` 或 `False` 。</span><span class="sxs-lookup"><span data-stu-id="64e8e-125">The first `If` argument is evaluated and the result is cast as a `Boolean` value, `True` or `False`.</span></span> <span data-ttu-id="64e8e-126">如果值为 `True` ， `argument2` 则计算，并返回其值，但不会对其值进行 `argument3` 求值。</span><span class="sxs-lookup"><span data-stu-id="64e8e-126">If the value is `True`, `argument2` is evaluated and its value is returned, but `argument3` is not evaluated.</span></span> <span data-ttu-id="64e8e-127">如果表达式的值 `Boolean` 为 `False` ， `argument3` 则计算，并返回其值，但不会对其值进行 `argument2` 求值。</span><span class="sxs-lookup"><span data-stu-id="64e8e-127">If the value of the `Boolean` expression is `False`, `argument3` is evaluated and its value is returned, but `argument2` is not evaluated.</span></span> <span data-ttu-id="64e8e-128">下面的示例演示使用 `If` 三个参数时的用法：</span><span class="sxs-lookup"><span data-stu-id="64e8e-128">The following examples illustrate the use of `If` when three arguments are used:</span></span>

[!code-vb[VbVbalrOperators#100](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrOperators/VB/Class4.vb#100)]

<span data-ttu-id="64e8e-129">下面的示例说明了短路计算的值。</span><span class="sxs-lookup"><span data-stu-id="64e8e-129">The following example illustrates the value of short-circuit evaluation.</span></span> <span data-ttu-id="64e8e-130">该示例显示两次 `number` `divisor` 除为零时，尝试将变量除以变量 `divisor` 。</span><span class="sxs-lookup"><span data-stu-id="64e8e-130">The example shows two attempts to divide variable `number` by variable `divisor` except when `divisor` is zero.</span></span> <span data-ttu-id="64e8e-131">在这种情况下，应返回0，并且不会尝试执行除法，因为将导致运行时错误。</span><span class="sxs-lookup"><span data-stu-id="64e8e-131">In that case, a 0 should be returned, and no attempt should be made to perform the division because a run-time error would result.</span></span> <span data-ttu-id="64e8e-132">由于 `If` 表达式使用短路计算，因此它将计算第二个或第三个参数，具体取决于第一个参数的值。</span><span class="sxs-lookup"><span data-stu-id="64e8e-132">Because the `If` expression uses short-circuit evaluation, it evaluates either the second or the third argument, depending on the value of the first argument.</span></span> <span data-ttu-id="64e8e-133">如果第一个参数为 true，则除数不为零，并且可以安全地计算第二个参数并执行除法运算。</span><span class="sxs-lookup"><span data-stu-id="64e8e-133">If the first argument is true, the divisor is not zero and it is safe to evaluate the second argument and perform the division.</span></span> <span data-ttu-id="64e8e-134">如果第一个参数为 false，则只计算第三个参数，并返回0。</span><span class="sxs-lookup"><span data-stu-id="64e8e-134">If the first argument is false, only the third argument is evaluated and a 0 is returned.</span></span> <span data-ttu-id="64e8e-135">因此，当除数为0时，将不会尝试执行除法，也不会产生错误结果。</span><span class="sxs-lookup"><span data-stu-id="64e8e-135">Therefore, when the divisor is 0, no attempt is made to perform the division and no error results.</span></span> <span data-ttu-id="64e8e-136">但是，由于不 `IIf` 使用短路计算，因此即使第一个参数为 false，也会计算第二个参数。</span><span class="sxs-lookup"><span data-stu-id="64e8e-136">However, because `IIf` does not use short-circuit evaluation, the second argument is evaluated even when the first argument is false.</span></span> <span data-ttu-id="64e8e-137">这将导致运行时被零除错误。</span><span class="sxs-lookup"><span data-stu-id="64e8e-137">This causes a run-time divide-by-zero error.</span></span>

[!code-vb[VbVbalrOperators#101](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrOperators/VB/Class4.vb#101)]

## <a name="if-operator-called-with-two-arguments"></a><span data-ttu-id="64e8e-138">如果运算符调用了两个自变量</span><span class="sxs-lookup"><span data-stu-id="64e8e-138">If operator called with two arguments</span></span>

<span data-ttu-id="64e8e-139">可以省略的第一个参数 `If` 。</span><span class="sxs-lookup"><span data-stu-id="64e8e-139">The first argument to `If` can be omitted.</span></span> <span data-ttu-id="64e8e-140">这使得仅使用两个参数即可调用运算符。</span><span class="sxs-lookup"><span data-stu-id="64e8e-140">This enables the operator to be called by using only two arguments.</span></span> <span data-ttu-id="64e8e-141">以下列表仅适用于 `If` 通过两个参数调用运算符的情况。</span><span class="sxs-lookup"><span data-stu-id="64e8e-141">The following list applies only when the `If` operator is called with two arguments.</span></span>

### <a name="parts"></a><span data-ttu-id="64e8e-142">组成部分</span><span class="sxs-lookup"><span data-stu-id="64e8e-142">Parts</span></span>

|<span data-ttu-id="64e8e-143">术语</span><span class="sxs-lookup"><span data-stu-id="64e8e-143">Term</span></span>|<span data-ttu-id="64e8e-144">定义</span><span class="sxs-lookup"><span data-stu-id="64e8e-144">Definition</span></span>|
|---|---|
|`argument2`|<span data-ttu-id="64e8e-145">必需。</span><span class="sxs-lookup"><span data-stu-id="64e8e-145">Required.</span></span> <span data-ttu-id="64e8e-146">`Object`.</span><span class="sxs-lookup"><span data-stu-id="64e8e-146">`Object`.</span></span> <span data-ttu-id="64e8e-147">必须是引用或可以为 null 的值类型。</span><span class="sxs-lookup"><span data-stu-id="64e8e-147">Must be a reference or nullable value type.</span></span> <span data-ttu-id="64e8e-148">当计算结果为之外的任何值时，计算并返回 `Nothing` 。</span><span class="sxs-lookup"><span data-stu-id="64e8e-148">Evaluated and returned when it evaluates to anything other than `Nothing`.</span></span>|
|`argument3`|<span data-ttu-id="64e8e-149">必需。</span><span class="sxs-lookup"><span data-stu-id="64e8e-149">Required.</span></span> <span data-ttu-id="64e8e-150">`Object`.</span><span class="sxs-lookup"><span data-stu-id="64e8e-150">`Object`.</span></span> <span data-ttu-id="64e8e-151">如果计算结果为，则计算并返回 `argument2` `Nothing` 。</span><span class="sxs-lookup"><span data-stu-id="64e8e-151">Evaluated and returned if `argument2` evaluates to `Nothing`.</span></span>|

<span data-ttu-id="64e8e-152">如果 `Boolean` 省略该参数，则第一个参数必须是引用或可以为 null 的值类型。</span><span class="sxs-lookup"><span data-stu-id="64e8e-152">When the `Boolean` argument is omitted, the first argument must be a reference or nullable value type.</span></span> <span data-ttu-id="64e8e-153">如果第一个参数的计算结果为 `Nothing` ，则返回第二个参数的值。</span><span class="sxs-lookup"><span data-stu-id="64e8e-153">If the first argument evaluates to `Nothing`, the value of the second argument is returned.</span></span> <span data-ttu-id="64e8e-154">在所有其他情况下，返回第一个参数的值。</span><span class="sxs-lookup"><span data-stu-id="64e8e-154">In all other cases, the value of the first argument is returned.</span></span> <span data-ttu-id="64e8e-155">下面的示例演示了此计算的工作原理：</span><span class="sxs-lookup"><span data-stu-id="64e8e-155">The following example illustrates how this evaluation works:</span></span>

[!code-vb[VbVbalrOperators#102](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrOperators/VB/Class4.vb#102)]

## <a name="see-also"></a><span data-ttu-id="64e8e-156">请参阅</span><span class="sxs-lookup"><span data-stu-id="64e8e-156">See also</span></span>

- <xref:Microsoft.VisualBasic.Interaction.IIf%2A>
- [<span data-ttu-id="64e8e-157">可以为 null 的值类型</span><span class="sxs-lookup"><span data-stu-id="64e8e-157">Nullable Value Types</span></span>](../../programming-guide/language-features/data-types/nullable-value-types.md)
- [<span data-ttu-id="64e8e-158">Nothing</span><span class="sxs-lookup"><span data-stu-id="64e8e-158">Nothing</span></span>](../nothing.md)
