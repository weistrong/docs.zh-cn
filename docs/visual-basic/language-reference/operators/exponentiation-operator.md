---
description: '详细了解： ^ 操作员 (Visual Basic) '
title: ^ 运算符
ms.date: 07/20/2015
f1_keywords:
- vb.^
helpviewer_keywords:
- raising numbers to powers
- ^ operator [Visual Basic], exponentiation
- square operator [Visual Basic]
- ^ operator [Visual Basic]
- exponentiation operator [Visual Basic]
- exponent
- numbers [Visual Basic], rasing
- powers
- arithmetic operators [Visual Basic], exponentiation
ms.assetid: d89a1ca8-83da-4784-a87b-a9d7dceb3f62
ms.openlocfilehash: 9333eec7236c363417be7323b673231509da8f1f
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99666038"
---
# <a name="-operator-visual-basic"></a><span data-ttu-id="2f4d8-103">^ 运算符 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="2f4d8-103">^ Operator (Visual Basic)</span></span>

<span data-ttu-id="2f4d8-104">以一个数字为底、另一数字为幂求值。</span><span class="sxs-lookup"><span data-stu-id="2f4d8-104">Raises a number to the power of another number.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f4d8-105">语法</span><span class="sxs-lookup"><span data-stu-id="2f4d8-105">Syntax</span></span>

```vb
number ^ exponent
```

## <a name="parts"></a><span data-ttu-id="2f4d8-106">组成部分</span><span class="sxs-lookup"><span data-stu-id="2f4d8-106">Parts</span></span>

`number`\
<span data-ttu-id="2f4d8-107">必需。</span><span class="sxs-lookup"><span data-stu-id="2f4d8-107">Required.</span></span> <span data-ttu-id="2f4d8-108">任何数值表达式。</span><span class="sxs-lookup"><span data-stu-id="2f4d8-108">Any numeric expression.</span></span>

`exponent`\
<span data-ttu-id="2f4d8-109">必需。</span><span class="sxs-lookup"><span data-stu-id="2f4d8-109">Required.</span></span> <span data-ttu-id="2f4d8-110">任何数值表达式。</span><span class="sxs-lookup"><span data-stu-id="2f4d8-110">Any numeric expression.</span></span>

## <a name="result"></a><span data-ttu-id="2f4d8-111">结果</span><span class="sxs-lookup"><span data-stu-id="2f4d8-111">Result</span></span>

<span data-ttu-id="2f4d8-112">结果会 `number` 引发的次幂 `exponent` ，总是作为 `Double` 值。</span><span class="sxs-lookup"><span data-stu-id="2f4d8-112">The result is `number` raised to the power of `exponent`, always as a `Double` value.</span></span>

## <a name="supported-types"></a><span data-ttu-id="2f4d8-113">支持的类型</span><span class="sxs-lookup"><span data-stu-id="2f4d8-113">Supported Types</span></span>

<span data-ttu-id="2f4d8-114">`Double`.</span><span class="sxs-lookup"><span data-stu-id="2f4d8-114">`Double`.</span></span> <span data-ttu-id="2f4d8-115">任何不同类型的操作数都转换为 `Double` 。</span><span class="sxs-lookup"><span data-stu-id="2f4d8-115">Operands of any different type are converted to `Double`.</span></span>

## <a name="remarks"></a><span data-ttu-id="2f4d8-116">备注</span><span class="sxs-lookup"><span data-stu-id="2f4d8-116">Remarks</span></span>

<span data-ttu-id="2f4d8-117">Visual Basic 总是对 [Double 数据类型](../data-types/double-data-type.md)执行幂运算。</span><span class="sxs-lookup"><span data-stu-id="2f4d8-117">Visual Basic always performs exponentiation in the [Double Data Type](../data-types/double-data-type.md).</span></span>

<span data-ttu-id="2f4d8-118">的值 `exponent` 可以是小数、负数或同时为两者。</span><span class="sxs-lookup"><span data-stu-id="2f4d8-118">The value of `exponent` can be fractional, negative, or both.</span></span>

<span data-ttu-id="2f4d8-119">如果在单个表达式中执行了多个幂运算，则会 `^` 按从左至右的顺序计算运算符。</span><span class="sxs-lookup"><span data-stu-id="2f4d8-119">When more than one exponentiation is performed in a single expression, the `^` operator is evaluated as it is encountered from left to right.</span></span>

> [!NOTE]
> <span data-ttu-id="2f4d8-120">`^`运算符可以 *重载*，这意味着当操作数具有该类或结构的类型时，该类或结构可以重新定义其行为。</span><span class="sxs-lookup"><span data-stu-id="2f4d8-120">The `^` operator can be *overloaded*, which means that a class or structure can redefine its behavior when an operand has the type of that class or structure.</span></span> <span data-ttu-id="2f4d8-121">如果你的代码在该类或结构上使用此运算符，请确保了解其重新定义的行为。</span><span class="sxs-lookup"><span data-stu-id="2f4d8-121">If your code uses this operator on such a class or structure, be sure you understand its redefined behavior.</span></span> <span data-ttu-id="2f4d8-122">有关详细信息，请参阅 [Operator Procedures](../../programming-guide/language-features/procedures/operator-procedures.md)。</span><span class="sxs-lookup"><span data-stu-id="2f4d8-122">For more information, see [Operator Procedures](../../programming-guide/language-features/procedures/operator-procedures.md).</span></span>

## <a name="example"></a><span data-ttu-id="2f4d8-123">示例</span><span class="sxs-lookup"><span data-stu-id="2f4d8-123">Example</span></span>

<span data-ttu-id="2f4d8-124">下面的示例使用运算符来计算 `^` 指数的幂。</span><span class="sxs-lookup"><span data-stu-id="2f4d8-124">The following example uses the `^` operator to raise a number to the power of an exponent.</span></span> <span data-ttu-id="2f4d8-125">结果是第一个操作数的次幂。</span><span class="sxs-lookup"><span data-stu-id="2f4d8-125">The result is the first operand raised to the power of the second.</span></span>

[!code-vb[VbVbalrOperators#20](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrOperators/VB/Class1.vb#20)]

<span data-ttu-id="2f4d8-126">前面的示例生成了以下结果：</span><span class="sxs-lookup"><span data-stu-id="2f4d8-126">The preceding example produces the following results:</span></span>

<span data-ttu-id="2f4d8-127">`exp1` 设置为 4 (2 squared) 。</span><span class="sxs-lookup"><span data-stu-id="2f4d8-127">`exp1` is set to 4 (2 squared).</span></span>

<span data-ttu-id="2f4d8-128">`exp2` 设置为 19683 (3 的立方值，则该值) 的立方值。</span><span class="sxs-lookup"><span data-stu-id="2f4d8-128">`exp2` is set to 19683 (3 cubed, then that value cubed).</span></span>

<span data-ttu-id="2f4d8-129">`exp3` 设置为-125 (-5) 的立方。</span><span class="sxs-lookup"><span data-stu-id="2f4d8-129">`exp3` is set to -125 (-5 cubed).</span></span>

<span data-ttu-id="2f4d8-130">`exp4` 设置为 625 ( 为第四个电源) 。</span><span class="sxs-lookup"><span data-stu-id="2f4d8-130">`exp4` is set to 625 (-5 to the fourth power).</span></span>

<span data-ttu-id="2f4d8-131">`exp5` 设置为 2 (8) 的立方根。</span><span class="sxs-lookup"><span data-stu-id="2f4d8-131">`exp5` is set to 2 (cube root of 8).</span></span>

<span data-ttu-id="2f4d8-132">`exp6` 设置为 0.5 (1.0 除以 8) 的立方根。</span><span class="sxs-lookup"><span data-stu-id="2f4d8-132">`exp6` is set to 0.5 (1.0 divided by the cube root of 8).</span></span>

<span data-ttu-id="2f4d8-133">请注意前面示例的表达式中的括号的重要性。</span><span class="sxs-lookup"><span data-stu-id="2f4d8-133">Note the importance of the parentheses in the expressions in the preceding example.</span></span> <span data-ttu-id="2f4d8-134">由于 *运算符优先级*，Visual Basic 通常在 `^` 任何其他运算符（甚至一元运算符）之前执行运算符 `–` 。</span><span class="sxs-lookup"><span data-stu-id="2f4d8-134">Because of *operator precedence*, Visual Basic normally performs the `^` operator before any others, even the unary `–` operator.</span></span> <span data-ttu-id="2f4d8-135">如果 `exp4` 和的 `exp6` 计算结果没有括号，则会生成以下结果：</span><span class="sxs-lookup"><span data-stu-id="2f4d8-135">If `exp4` and `exp6` had been calculated without parentheses, they would have produced the following results:</span></span>

<span data-ttu-id="2f4d8-136">`exp4 = -5 ^ 4` 将计算为– (5 到第四个幂) ，这会导致-625。</span><span class="sxs-lookup"><span data-stu-id="2f4d8-136">`exp4 = -5 ^ 4` would be calculated as –(5 to the fourth power), which would result in -625.</span></span>

<span data-ttu-id="2f4d8-137">`exp6 = 8 ^ -1.0 / 3.0` 计算结果为 (8 到-1 的幂或 0.125) 除以3.0，这将导致0.041666666666666666666666666666667。</span><span class="sxs-lookup"><span data-stu-id="2f4d8-137">`exp6 = 8 ^ -1.0 / 3.0` would be calculated as (8 to the –1 power, or 0.125) divided by 3.0, which would result in 0.041666666666666666666666666666667.</span></span>

## <a name="see-also"></a><span data-ttu-id="2f4d8-138">请参阅</span><span class="sxs-lookup"><span data-stu-id="2f4d8-138">See also</span></span>

- [<span data-ttu-id="2f4d8-139">^ = 运算符</span><span class="sxs-lookup"><span data-stu-id="2f4d8-139">^= Operator</span></span>](exponentiation-assignment-operator.md)
- [<span data-ttu-id="2f4d8-140">算术运算符</span><span class="sxs-lookup"><span data-stu-id="2f4d8-140">Arithmetic Operators</span></span>](arithmetic-operators.md)
- [<span data-ttu-id="2f4d8-141">Visual Basic 中的运算符优先级</span><span class="sxs-lookup"><span data-stu-id="2f4d8-141">Operator Precedence in Visual Basic</span></span>](operator-precedence.md)
- [<span data-ttu-id="2f4d8-142">按功能列出的运算符</span><span class="sxs-lookup"><span data-stu-id="2f4d8-142">Operators Listed by Functionality</span></span>](operators-listed-by-functionality.md)
- [<span data-ttu-id="2f4d8-143">算术运算符 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="2f4d8-143">Arithmetic Operators in Visual Basic</span></span>](../../programming-guide/language-features/operators-and-expressions/arithmetic-operators.md)
