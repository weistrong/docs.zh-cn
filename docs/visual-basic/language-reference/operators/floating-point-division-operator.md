---
description: '详细了解：/Operator (Visual Basic) '
title: / 运算符
ms.date: 07/20/2015
f1_keywords:
- vb./
helpviewer_keywords:
- division operator [Visual Basic], floating point
- floating-point numbers [Visual Basic], division operator
- slash (/) operator
- zero, division by zero
- operators [Visual Basic], arithmetic
- arithmetic operators [Visual Basic], division
- division [Visual Basic], by zero
- operators [Visual Basic], division
- division operator [Visual Basic], syntax
- / operator [Visual Basic]
- math operators [Visual Basic]
ms.assetid: 335e97f2-c434-439e-9064-76973a051101
ms.openlocfilehash: 717c8fdc6abae02de555040a3aadb92fed2bfbee
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99665999"
---
# <a name="-operator-visual-basic"></a><span data-ttu-id="40cb7-103">/ 运算符 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="40cb7-103">/ Operator (Visual Basic)</span></span>

<span data-ttu-id="40cb7-104">使两个数字相除，返回浮点结果。</span><span class="sxs-lookup"><span data-stu-id="40cb7-104">Divides two numbers and returns a floating-point result.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="40cb7-105">语法</span><span class="sxs-lookup"><span data-stu-id="40cb7-105">Syntax</span></span>  
  
```vb  
expression1 / expression2  
```  
  
## <a name="parts"></a><span data-ttu-id="40cb7-106">组成部分</span><span class="sxs-lookup"><span data-stu-id="40cb7-106">Parts</span></span>  

 `expression1`  
 <span data-ttu-id="40cb7-107">必需。</span><span class="sxs-lookup"><span data-stu-id="40cb7-107">Required.</span></span> <span data-ttu-id="40cb7-108">任何数值表达式。</span><span class="sxs-lookup"><span data-stu-id="40cb7-108">Any numeric expression.</span></span>  
  
 `expression2`  
 <span data-ttu-id="40cb7-109">必需。</span><span class="sxs-lookup"><span data-stu-id="40cb7-109">Required.</span></span> <span data-ttu-id="40cb7-110">任何数值表达式。</span><span class="sxs-lookup"><span data-stu-id="40cb7-110">Any numeric expression.</span></span>  
  
## <a name="supported-types"></a><span data-ttu-id="40cb7-111">支持的类型</span><span class="sxs-lookup"><span data-stu-id="40cb7-111">Supported Types</span></span>  

 <span data-ttu-id="40cb7-112">所有数值类型，包括无符号和浮点类型和 `Decimal` 。</span><span class="sxs-lookup"><span data-stu-id="40cb7-112">All numeric types, including the unsigned and floating-point types and `Decimal`.</span></span>  
  
## <a name="result"></a><span data-ttu-id="40cb7-113">结果</span><span class="sxs-lookup"><span data-stu-id="40cb7-113">Result</span></span>  

 <span data-ttu-id="40cb7-114">结果是除以的全部商 `expression1` `expression2` ，包括余数。</span><span class="sxs-lookup"><span data-stu-id="40cb7-114">The result is the full quotient of `expression1` divided by `expression2`, including any remainder.</span></span>  
  
 <span data-ttu-id="40cb7-115">[\ 运算符 (Visual Basic) ](integer-division-operator.md)返回整数商，这会删除余数。</span><span class="sxs-lookup"><span data-stu-id="40cb7-115">The [\ Operator (Visual Basic)](integer-division-operator.md) returns the integer quotient, which drops the remainder.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="40cb7-116">备注</span><span class="sxs-lookup"><span data-stu-id="40cb7-116">Remarks</span></span>  

 <span data-ttu-id="40cb7-117">结果的数据类型取决于操作数的类型。</span><span class="sxs-lookup"><span data-stu-id="40cb7-117">The data type of the result depends on the types of the operands.</span></span> <span data-ttu-id="40cb7-118">下表显示了如何确定结果的数据类型。</span><span class="sxs-lookup"><span data-stu-id="40cb7-118">The following table shows how the data type of the result is determined.</span></span>  
  
|<span data-ttu-id="40cb7-119">操作数数据类型</span><span class="sxs-lookup"><span data-stu-id="40cb7-119">Operand data types</span></span>|<span data-ttu-id="40cb7-120">Result 数据类型</span><span class="sxs-lookup"><span data-stu-id="40cb7-120">Result data type</span></span>|  
|------------------------|----------------------|  
|<span data-ttu-id="40cb7-121">这两个表达式都是整型数据类型 ([SByte](../data-types/sbyte-data-type.md)、 [Byte](../data-types/byte-data-type.md)、 [Short](../data-types/short-data-type.md)、 [UShort](../data-types/ushort-data-type.md)、 [Integer](../data-types/integer-data-type.md)、 [UInteger](../data-types/uinteger-data-type.md)、 [Long](../data-types/long-data-type.md)、 [ULong](../data-types/ulong-data-type.md)) </span><span class="sxs-lookup"><span data-stu-id="40cb7-121">Both expressions are integral data types ([SByte](../data-types/sbyte-data-type.md), [Byte](../data-types/byte-data-type.md), [Short](../data-types/short-data-type.md), [UShort](../data-types/ushort-data-type.md), [Integer](../data-types/integer-data-type.md), [UInteger](../data-types/uinteger-data-type.md), [Long](../data-types/long-data-type.md), [ULong](../data-types/ulong-data-type.md))</span></span>|`Double`|  
|<span data-ttu-id="40cb7-122">一个表达式是[单一](../data-types/single-data-type.md)数据类型，另一个表达式不是[双精度](../data-types/double-data-type.md)型</span><span class="sxs-lookup"><span data-stu-id="40cb7-122">One expression is a [Single](../data-types/single-data-type.md) data type and the other is not a [Double](../data-types/double-data-type.md)</span></span>|`Single`|  
|<span data-ttu-id="40cb7-123">一个表达式是 [Decimal](../data-types/decimal-data-type.md) 数据类型，另一个表达式不是 [单个](../data-types/single-data-type.md) 或 [双精度](../data-types/double-data-type.md)</span><span class="sxs-lookup"><span data-stu-id="40cb7-123">One expression is a [Decimal](../data-types/decimal-data-type.md) data type and the other is not a [Single](../data-types/single-data-type.md) or a [Double](../data-types/double-data-type.md)</span></span>|`Decimal`|  
|<span data-ttu-id="40cb7-124">其中一个表达式为 [Double](../data-types/double-data-type.md) 数据类型</span><span class="sxs-lookup"><span data-stu-id="40cb7-124">Either expression is a [Double](../data-types/double-data-type.md) data type</span></span>|`Double`|  
  
 <span data-ttu-id="40cb7-125">在执行除法运算之前，所有整数数值表达式都将扩展到 `Double` 。</span><span class="sxs-lookup"><span data-stu-id="40cb7-125">Before division is performed, any integral numeric expressions are widened to `Double`.</span></span> <span data-ttu-id="40cb7-126">如果将结果赋给整数数据类型，Visual Basic 会尝试将结果从转换 `Double` 为该类型。</span><span class="sxs-lookup"><span data-stu-id="40cb7-126">If you assign the result to an integral data type, Visual Basic attempts to convert the result from `Double` to that type.</span></span> <span data-ttu-id="40cb7-127">如果结果不适合该类型，这可能会引发异常。</span><span class="sxs-lookup"><span data-stu-id="40cb7-127">This can throw an exception if the result does not fit in that type.</span></span> <span data-ttu-id="40cb7-128">具体而言，请参阅此帮助页上的 "尝试被零除"。</span><span class="sxs-lookup"><span data-stu-id="40cb7-128">In particular, see "Attempted Division by Zero" on this Help page.</span></span>  
  
 <span data-ttu-id="40cb7-129">如果 `expression1` 或的 `expression2` 计算结果不为 [空](../nothing.md)，则将其视为零。</span><span class="sxs-lookup"><span data-stu-id="40cb7-129">If `expression1` or `expression2` evaluates to [Nothing](../nothing.md), it is treated as zero.</span></span>  
  
## <a name="attempted-division-by-zero"></a><span data-ttu-id="40cb7-130">尝试被零除</span><span class="sxs-lookup"><span data-stu-id="40cb7-130">Attempted Division by Zero</span></span>  

 <span data-ttu-id="40cb7-131">如果 `expression2` 计算结果为零，则 `/` 运算符的行为不同于不同的操作数数据类型。</span><span class="sxs-lookup"><span data-stu-id="40cb7-131">If `expression2` evaluates to zero, the `/` operator behaves differently for different operand data types.</span></span> <span data-ttu-id="40cb7-132">下表显示了可能的行为。</span><span class="sxs-lookup"><span data-stu-id="40cb7-132">The following table shows the possible behaviors.</span></span>  
  
|<span data-ttu-id="40cb7-133">操作数数据类型</span><span class="sxs-lookup"><span data-stu-id="40cb7-133">Operand data types</span></span>|<span data-ttu-id="40cb7-134">`expression2`为零时的行为</span><span class="sxs-lookup"><span data-stu-id="40cb7-134">Behavior if `expression2` is zero</span></span>|  
|------------------------|---------------------------------------|  
|<span data-ttu-id="40cb7-135">浮点 (`Single` 或 `Double`) </span><span class="sxs-lookup"><span data-stu-id="40cb7-135">Floating-point (`Single` or `Double`)</span></span>|<span data-ttu-id="40cb7-136"><xref:System.Double.PositiveInfinity> <xref:System.Double.NegativeInfinity> 如果也为零，则返回无穷 (或) ，或者 <xref:System.Double.NaN> (不是数字) `expression1`</span><span class="sxs-lookup"><span data-stu-id="40cb7-136">Returns infinity (<xref:System.Double.PositiveInfinity> or <xref:System.Double.NegativeInfinity>), or <xref:System.Double.NaN> (not a number) if `expression1` is also zero</span></span>|  
|`Decimal`|<span data-ttu-id="40cb7-137">却 <xref:System.DivideByZeroException></span><span class="sxs-lookup"><span data-stu-id="40cb7-137">Throws <xref:System.DivideByZeroException></span></span>|  
|<span data-ttu-id="40cb7-138">整数 (有符号或无符号) </span><span class="sxs-lookup"><span data-stu-id="40cb7-138">Integral (signed or unsigned)</span></span>|<span data-ttu-id="40cb7-139">尝试转换回整型类型会引发 <xref:System.OverflowException> ，因为整型类型不能接受 <xref:System.Double.PositiveInfinity> 、 <xref:System.Double.NegativeInfinity> 或 <xref:System.Double.NaN></span><span class="sxs-lookup"><span data-stu-id="40cb7-139">Attempted conversion back to integral type throws <xref:System.OverflowException> because integral types cannot accept <xref:System.Double.PositiveInfinity>, <xref:System.Double.NegativeInfinity>, or <xref:System.Double.NaN></span></span>|  
  
> [!NOTE]
> <span data-ttu-id="40cb7-140">`/`运算符可以 *重载*，这意味着当操作数具有该类或结构的类型时，该类或结构可以重新定义其行为。</span><span class="sxs-lookup"><span data-stu-id="40cb7-140">The `/` operator can be *overloaded*, which means that a class or structure can redefine its behavior when an operand has the type of that class or structure.</span></span> <span data-ttu-id="40cb7-141">如果你的代码在该类或结构上使用此运算符，请确保了解其重新定义的行为。</span><span class="sxs-lookup"><span data-stu-id="40cb7-141">If your code uses this operator on such a class or structure, be sure you understand its redefined behavior.</span></span> <span data-ttu-id="40cb7-142">有关详细信息，请参阅 [Operator Procedures](../../programming-guide/language-features/procedures/operator-procedures.md)。</span><span class="sxs-lookup"><span data-stu-id="40cb7-142">For more information, see [Operator Procedures](../../programming-guide/language-features/procedures/operator-procedures.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="40cb7-143">示例</span><span class="sxs-lookup"><span data-stu-id="40cb7-143">Example</span></span>  

 <span data-ttu-id="40cb7-144">此示例使用 `/` 运算符来执行浮点除法。</span><span class="sxs-lookup"><span data-stu-id="40cb7-144">This example uses the `/` operator to perform floating-point division.</span></span> <span data-ttu-id="40cb7-145">结果是两个操作数的商。</span><span class="sxs-lookup"><span data-stu-id="40cb7-145">The result is the quotient of the two operands.</span></span>  
  
 [!code-vb[VbVbalrOperators#16](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrOperators/VB/Class1.vb#16)]  
  
 <span data-ttu-id="40cb7-146">前面的示例中的表达式返回值2.5 和3.333333。</span><span class="sxs-lookup"><span data-stu-id="40cb7-146">The expressions in the preceding example return values of 2.5 and 3.333333.</span></span> <span data-ttu-id="40cb7-147">请注意，结果始终是浮点 (`Double`) ，即使两个操作数都是整数常量。</span><span class="sxs-lookup"><span data-stu-id="40cb7-147">Note that the result is always floating-point (`Double`), even though both operands are integer constants.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="40cb7-148">请参阅</span><span class="sxs-lookup"><span data-stu-id="40cb7-148">See also</span></span>

- [<span data-ttu-id="40cb7-149">/= 运算符 (Visual Basic) </span><span class="sxs-lookup"><span data-stu-id="40cb7-149">/= Operator (Visual Basic)</span></span>](floating-point-division-assignment-operator.md)
- [<span data-ttu-id="40cb7-150">\ 运算符 (Visual Basic) </span><span class="sxs-lookup"><span data-stu-id="40cb7-150">\ Operator (Visual Basic)</span></span>](integer-division-operator.md)
- [<span data-ttu-id="40cb7-151">运算符结果的数据类型</span><span class="sxs-lookup"><span data-stu-id="40cb7-151">Data Types of Operator Results</span></span>](data-types-of-operator-results.md)
- [<span data-ttu-id="40cb7-152">算术运算符</span><span class="sxs-lookup"><span data-stu-id="40cb7-152">Arithmetic Operators</span></span>](arithmetic-operators.md)
- [<span data-ttu-id="40cb7-153">Visual Basic 中的运算符优先级</span><span class="sxs-lookup"><span data-stu-id="40cb7-153">Operator Precedence in Visual Basic</span></span>](operator-precedence.md)
- [<span data-ttu-id="40cb7-154">按功能列出的运算符</span><span class="sxs-lookup"><span data-stu-id="40cb7-154">Operators Listed by Functionality</span></span>](operators-listed-by-functionality.md)
- [<span data-ttu-id="40cb7-155">算术运算符 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="40cb7-155">Arithmetic Operators in Visual Basic</span></span>](../../programming-guide/language-features/operators-and-expressions/arithmetic-operators.md)
