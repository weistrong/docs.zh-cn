---
description: '详细了解： Mod operator (Visual Basic) '
title: Mod 运算符
ms.date: 04/24/2018
f1_keywords:
- vb.Mod
helpviewer_keywords:
- remainder (Mod operator)
- division operator [Visual Basic], Mod operator
- modulus operator [Visual Basic], Visual Basic
- Mod operator [Visual Basic]
- operators [Visual Basic], division
- arithmetic operators [Visual Basic], Mod
- math operators [Visual Basic]
ms.assetid: 6ff7e40e-cec8-4c77-bff6-8ddd2791c25b
ms.openlocfilehash: bfec39f54041714258e21f087a044dce24edcb6b
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99665427"
---
# <a name="mod-operator-visual-basic"></a><span data-ttu-id="a4110-103">Mod 运算符 (Visual Basic) </span><span class="sxs-lookup"><span data-stu-id="a4110-103">Mod operator (Visual Basic)</span></span>

<span data-ttu-id="a4110-104">将两个数字相除，仅返回余数。</span><span class="sxs-lookup"><span data-stu-id="a4110-104">Divides two numbers and returns only the remainder.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4110-105">语法</span><span class="sxs-lookup"><span data-stu-id="a4110-105">Syntax</span></span>

```vb
result = number1 Mod number2
```

## <a name="parts"></a><span data-ttu-id="a4110-106">组成部分</span><span class="sxs-lookup"><span data-stu-id="a4110-106">Parts</span></span>

`result` \
<span data-ttu-id="a4110-107">必需。</span><span class="sxs-lookup"><span data-stu-id="a4110-107">Required.</span></span> <span data-ttu-id="a4110-108">任何数值变量或属性。</span><span class="sxs-lookup"><span data-stu-id="a4110-108">Any numeric variable or property.</span></span>

`number1` \
<span data-ttu-id="a4110-109">必需。</span><span class="sxs-lookup"><span data-stu-id="a4110-109">Required.</span></span> <span data-ttu-id="a4110-110">任何数值表达式。</span><span class="sxs-lookup"><span data-stu-id="a4110-110">Any numeric expression.</span></span>

`number2` \
<span data-ttu-id="a4110-111">必需。</span><span class="sxs-lookup"><span data-stu-id="a4110-111">Required.</span></span> <span data-ttu-id="a4110-112">任何数值表达式。</span><span class="sxs-lookup"><span data-stu-id="a4110-112">Any numeric expression.</span></span>

## <a name="supported-types"></a><span data-ttu-id="a4110-113">支持的类型</span><span class="sxs-lookup"><span data-stu-id="a4110-113">Supported types</span></span>

<span data-ttu-id="a4110-114">所有数值类型。</span><span class="sxs-lookup"><span data-stu-id="a4110-114">All numeric types.</span></span> <span data-ttu-id="a4110-115">这包括无符号和浮点类型和 `Decimal` 。</span><span class="sxs-lookup"><span data-stu-id="a4110-115">This includes the unsigned and floating-point types and `Decimal`.</span></span>

## <a name="result"></a><span data-ttu-id="a4110-116">结果</span><span class="sxs-lookup"><span data-stu-id="a4110-116">Result</span></span>

<span data-ttu-id="a4110-117">结果是除以后的余数 `number1` `number2` 。</span><span class="sxs-lookup"><span data-stu-id="a4110-117">The result is the remainder after `number1` is divided by `number2`.</span></span> <span data-ttu-id="a4110-118">例如，表达式的 `14 Mod 4` 计算结果为2。</span><span class="sxs-lookup"><span data-stu-id="a4110-118">For example, the expression `14 Mod 4` evaluates to 2.</span></span>

> [!NOTE]
> <span data-ttu-id="a4110-119">在数学中， *余数* 和 *模数* 之间存在差异，但负数的结果不同。</span><span class="sxs-lookup"><span data-stu-id="a4110-119">There is a difference between *remainder* and *modulus* in mathematics, with different results for negative numbers.</span></span> <span data-ttu-id="a4110-120">`Mod`Visual Basic、.NET Framework `op_Modulus` 运算符和基础[rem](<xref:System.Reflection.Emit.OpCodes.Rem>) IL 指令中的运算符都执行了余数运算。</span><span class="sxs-lookup"><span data-stu-id="a4110-120">The `Mod` operator in Visual Basic, the .NET Framework `op_Modulus` operator, and the underlying [rem](<xref:System.Reflection.Emit.OpCodes.Rem>) IL instruction all perform a remainder operation.</span></span>

<span data-ttu-id="a4110-121">操作的结果 `Mod` 保留被除数的符号， `number1` 因此它可以是正数也可以是负数。</span><span class="sxs-lookup"><span data-stu-id="a4110-121">The result of a `Mod` operation retains the sign of the dividend, `number1`, and so it may be positive or negative.</span></span> <span data-ttu-id="a4110-122">结果始终处于范围 (- `number2` 、 `number2`) 、独占。</span><span class="sxs-lookup"><span data-stu-id="a4110-122">The result is always in the range (-`number2`, `number2`), exclusive.</span></span> <span data-ttu-id="a4110-123">例如：</span><span class="sxs-lookup"><span data-stu-id="a4110-123">For example:</span></span>

```vb
Public Module Example
   Public Sub Main()
      Console.WriteLine($" 8 Mod  3 = {8 Mod 3}")
      Console.WriteLine($"-8 Mod  3 = {-8 Mod 3}")
      Console.WriteLine($" 8 Mod -3 = {8 Mod -3}")
      Console.WriteLine($"-8 Mod -3 = {-8 Mod -3}")
   End Sub
End Module
' The example displays the following output:
'       8 Mod  3 = 2
'      -8 Mod  3 = -2
'       8 Mod -3 = 2
'      -8 Mod -3 = -2
```

## <a name="remarks"></a><span data-ttu-id="a4110-124">备注</span><span class="sxs-lookup"><span data-stu-id="a4110-124">Remarks</span></span>

<span data-ttu-id="a4110-125">如果 `number1` 或 `number2` 是浮点值，则返回相除的浮点余数。</span><span class="sxs-lookup"><span data-stu-id="a4110-125">If either `number1` or `number2` is a floating-point value, the floating-point remainder of the division is returned.</span></span> <span data-ttu-id="a4110-126">结果的数据类型是最小的数据类型，该数据类型可以包含与和的数据类型相除所得的所有可能 `number1` 值 `number2` 。</span><span class="sxs-lookup"><span data-stu-id="a4110-126">The data type of the result is the smallest data type that can hold all possible values that result from division with the data types of `number1` and `number2`.</span></span>

<span data-ttu-id="a4110-127">如果 `number1` 或的 `number2` 计算结果不为 [空](../nothing.md)，则将其视为零。</span><span class="sxs-lookup"><span data-stu-id="a4110-127">If `number1` or `number2` evaluates to [Nothing](../nothing.md), it is treated as zero.</span></span>

<span data-ttu-id="a4110-128">相关运算符包括：</span><span class="sxs-lookup"><span data-stu-id="a4110-128">Related operators include the following:</span></span>

- <span data-ttu-id="a4110-129">[\ 运算符 (Visual Basic) ](integer-division-operator.md)返回相除的整数商。</span><span class="sxs-lookup"><span data-stu-id="a4110-129">The [\ Operator (Visual Basic)](integer-division-operator.md) returns the integer quotient of a division.</span></span> <span data-ttu-id="a4110-130">例如，表达式的 `14 \ 4` 计算结果为3。</span><span class="sxs-lookup"><span data-stu-id="a4110-130">For example, the expression `14 \ 4` evaluates to 3.</span></span>

- <span data-ttu-id="a4110-131">[/运算符 (Visual Basic) ](floating-point-division-operator.md)将完整商（包括余数）作为浮点数返回。</span><span class="sxs-lookup"><span data-stu-id="a4110-131">The [/ Operator (Visual Basic)](floating-point-division-operator.md) returns the full quotient, including the remainder, as a floating-point number.</span></span> <span data-ttu-id="a4110-132">例如，表达式的 `14 / 4` 计算结果为3.5。</span><span class="sxs-lookup"><span data-stu-id="a4110-132">For example, the expression `14 / 4` evaluates to 3.5.</span></span>

## <a name="attempted-division-by-zero"></a><span data-ttu-id="a4110-133">尝试被零除</span><span class="sxs-lookup"><span data-stu-id="a4110-133">Attempted division by zero</span></span>

<span data-ttu-id="a4110-134">如果 `number2` 计算结果为零，则运算符的行为 `Mod` 取决于操作数的数据类型：</span><span class="sxs-lookup"><span data-stu-id="a4110-134">If `number2` evaluates to zero, the behavior of the `Mod` operator depends on the data type of the operands:</span></span>

- <span data-ttu-id="a4110-135">如果在编译时无法确定，则整数除法会引发 <xref:System.DivideByZeroException> 异常 `number2` ，并在 `BC30542 Division by zero occurred while evaluating this expression` `number2` 编译时计算结果为零时生成编译时错误。</span><span class="sxs-lookup"><span data-stu-id="a4110-135">An integral division throws a <xref:System.DivideByZeroException> exception if `number2` cannot be determined in compile-time and generates a compile-time error `BC30542 Division by zero occurred while evaluating this expression` if `number2` is evaluated to zero at compile-time.</span></span>
- <span data-ttu-id="a4110-136">浮点除法返回 <xref:System.Double.NaN?displayProperty=nameWithType> 。</span><span class="sxs-lookup"><span data-stu-id="a4110-136">A floating-point division returns <xref:System.Double.NaN?displayProperty=nameWithType>.</span></span>

## <a name="equivalent-formula"></a><span data-ttu-id="a4110-137">等效公式</span><span class="sxs-lookup"><span data-stu-id="a4110-137">Equivalent formula</span></span>

<span data-ttu-id="a4110-138">表达式 `a Mod b` 等效于以下公式之一：</span><span class="sxs-lookup"><span data-stu-id="a4110-138">The expression `a Mod b` is equivalent to either of the following formulas:</span></span>

`a - (b * (a \ b))`

`a - (b * Fix(a / b))`

## <a name="floating-point-imprecision"></a><span data-ttu-id="a4110-139">浮点不精确性</span><span class="sxs-lookup"><span data-stu-id="a4110-139">Floating-point imprecision</span></span>

<span data-ttu-id="a4110-140">使用浮点数时，请记住，内存中不一定有精确的十进制表示形式。</span><span class="sxs-lookup"><span data-stu-id="a4110-140">When you work with floating-point numbers, remember that they do not always have a precise decimal representation in memory.</span></span> <span data-ttu-id="a4110-141">这可能会导致某些操作产生意外结果，如值比较和 `Mod` 运算符。</span><span class="sxs-lookup"><span data-stu-id="a4110-141">This can lead to unexpected results from certain operations, such as value comparison and the `Mod` operator.</span></span> <span data-ttu-id="a4110-142">有关详细信息，请参阅 [数据类型疑难解答](../../programming-guide/language-features/data-types/troubleshooting-data-types.md)。</span><span class="sxs-lookup"><span data-stu-id="a4110-142">For more information, see [Troubleshooting Data Types](../../programming-guide/language-features/data-types/troubleshooting-data-types.md).</span></span>

## <a name="overloading"></a><span data-ttu-id="a4110-143">重载</span><span class="sxs-lookup"><span data-stu-id="a4110-143">Overloading</span></span>

<span data-ttu-id="a4110-144">`Mod`运算符可以 *重载*，这意味着类或结构可以重新定义它的行为。</span><span class="sxs-lookup"><span data-stu-id="a4110-144">The `Mod` operator can be *overloaded*, which means that a class or structure can redefine its behavior.</span></span> <span data-ttu-id="a4110-145">如果你的代码应用于 `Mod` 包含此类重载的类或结构的实例，请确保了解其重新定义的行为。</span><span class="sxs-lookup"><span data-stu-id="a4110-145">If your code applies `Mod` to an instance of a class or structure that includes such an overload, be sure you understand its redefined behavior.</span></span> <span data-ttu-id="a4110-146">有关详细信息，请参阅 [Operator Procedures](../../programming-guide/language-features/procedures/operator-procedures.md)。</span><span class="sxs-lookup"><span data-stu-id="a4110-146">For more information, see [Operator Procedures](../../programming-guide/language-features/procedures/operator-procedures.md).</span></span>

## <a name="example"></a><span data-ttu-id="a4110-147">示例</span><span class="sxs-lookup"><span data-stu-id="a4110-147">Example</span></span>

<span data-ttu-id="a4110-148">下面的示例使用 `Mod` 运算符将两个数字相除，仅返回余数。</span><span class="sxs-lookup"><span data-stu-id="a4110-148">The following example uses the `Mod` operator to divide two numbers and return only the remainder.</span></span> <span data-ttu-id="a4110-149">如果其中一个数字为浮点数，则结果为一个表示余数的浮点数。</span><span class="sxs-lookup"><span data-stu-id="a4110-149">If either number is a floating-point number, the result is a floating-point number that represents the remainder.</span></span>

[!code-vb[VbVbalrOperators#31](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrOperators/VB/Class1.vb#31)]

## <a name="example"></a><span data-ttu-id="a4110-150">示例</span><span class="sxs-lookup"><span data-stu-id="a4110-150">Example</span></span>

<span data-ttu-id="a4110-151">下面的示例演示了浮点操作数的潜在不精确性。</span><span class="sxs-lookup"><span data-stu-id="a4110-151">The following example demonstrates the potential imprecision of floating-point operands.</span></span> <span data-ttu-id="a4110-152">在第一个语句中，操作数为 `Double` ，0.2 是一个无限重复的二进制小数，其存储值为0.20000000000000001。</span><span class="sxs-lookup"><span data-stu-id="a4110-152">In the first statement, the operands are `Double`, and 0.2 is an infinitely repeating binary fraction with a stored value of 0.20000000000000001.</span></span> <span data-ttu-id="a4110-153">在第二个语句中，文本类型字符 `D` 强制两个操作数为 `Decimal` ，0.2 具有精确的表示形式。</span><span class="sxs-lookup"><span data-stu-id="a4110-153">In the second statement, the literal type character `D` forces both operands to `Decimal`, and 0.2 has a precise representation.</span></span>

[!code-vb[VbVbalrOperators#32](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrOperators/VB/Class1.vb#32)]

## <a name="see-also"></a><span data-ttu-id="a4110-154">请参阅</span><span class="sxs-lookup"><span data-stu-id="a4110-154">See also</span></span>

- <xref:Microsoft.VisualBasic.Conversion.Int%2A>
- <xref:Microsoft.VisualBasic.Conversion.Fix%2A>
- [<span data-ttu-id="a4110-155">算术运算符</span><span class="sxs-lookup"><span data-stu-id="a4110-155">Arithmetic Operators</span></span>](arithmetic-operators.md)
- [<span data-ttu-id="a4110-156">Visual Basic 中的运算符优先级</span><span class="sxs-lookup"><span data-stu-id="a4110-156">Operator Precedence in Visual Basic</span></span>](operator-precedence.md)
- [<span data-ttu-id="a4110-157">按功能列出的运算符</span><span class="sxs-lookup"><span data-stu-id="a4110-157">Operators Listed by Functionality</span></span>](operators-listed-by-functionality.md)
- [<span data-ttu-id="a4110-158">数据类型疑难解答</span><span class="sxs-lookup"><span data-stu-id="a4110-158">Troubleshooting Data Types</span></span>](../../programming-guide/language-features/data-types/troubleshooting-data-types.md)
- [<span data-ttu-id="a4110-159">算术运算符 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="a4110-159">Arithmetic Operators in Visual Basic</span></span>](../../programming-guide/language-features/operators-and-expressions/arithmetic-operators.md)
- [<span data-ttu-id="a4110-160">\ 运算符 (Visual Basic) </span><span class="sxs-lookup"><span data-stu-id="a4110-160">\ Operator (Visual Basic)</span></span>](integer-division-operator.md)
