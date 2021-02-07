---
description: '详细了解： * Operator (Visual Basic) '
title: '* 操作员'
ms.date: 07/20/2015
f1_keywords:
- vb.*
helpviewer_keywords:
- arithmetic operators [Visual Basic], multiplication
- operators [Visual Basic], multiplication
- '* operator [Visual Basic]'
- multiplication operator [Visual Basic], syntax
- math operators [Visual Basic]
ms.assetid: 2b210382-99da-4195-89ba-b1d06f5e89ad
ms.openlocfilehash: 9a9f7eff9468fd6784b705a50871bc79fd6c1faa
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99665388"
---
# <a name="-operator-visual-basic"></a><span data-ttu-id="ec1f8-103">\* 运算符 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="ec1f8-103">\* Operator (Visual Basic)</span></span>

<span data-ttu-id="ec1f8-104">使两个数字相乘。</span><span class="sxs-lookup"><span data-stu-id="ec1f8-104">Multiplies two numbers.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ec1f8-105">语法</span><span class="sxs-lookup"><span data-stu-id="ec1f8-105">Syntax</span></span>  
  
```vb  
number1 * number2  
```  
  
## <a name="parts"></a><span data-ttu-id="ec1f8-106">组成部分</span><span class="sxs-lookup"><span data-stu-id="ec1f8-106">Parts</span></span>  
  
|<span data-ttu-id="ec1f8-107">术语</span><span class="sxs-lookup"><span data-stu-id="ec1f8-107">Term</span></span>|<span data-ttu-id="ec1f8-108">定义</span><span class="sxs-lookup"><span data-stu-id="ec1f8-108">Definition</span></span>|  
|---|---|  
|`number1`|<span data-ttu-id="ec1f8-109">必需。</span><span class="sxs-lookup"><span data-stu-id="ec1f8-109">Required.</span></span> <span data-ttu-id="ec1f8-110">任何数值表达式。</span><span class="sxs-lookup"><span data-stu-id="ec1f8-110">Any numeric expression.</span></span>|  
|`number2`|<span data-ttu-id="ec1f8-111">必需。</span><span class="sxs-lookup"><span data-stu-id="ec1f8-111">Required.</span></span> <span data-ttu-id="ec1f8-112">任何数值表达式。</span><span class="sxs-lookup"><span data-stu-id="ec1f8-112">Any numeric expression.</span></span>|  
  
## <a name="result"></a><span data-ttu-id="ec1f8-113">结果</span><span class="sxs-lookup"><span data-stu-id="ec1f8-113">Result</span></span>  

 <span data-ttu-id="ec1f8-114">结果是和的乘积 `number1` `number2` 。</span><span class="sxs-lookup"><span data-stu-id="ec1f8-114">The result is the product of `number1` and `number2`.</span></span>  
  
## <a name="supported-types"></a><span data-ttu-id="ec1f8-115">支持的类型</span><span class="sxs-lookup"><span data-stu-id="ec1f8-115">Supported Types</span></span>  

 <span data-ttu-id="ec1f8-116">所有数值类型，包括无符号和浮点类型和 `Decimal` 。</span><span class="sxs-lookup"><span data-stu-id="ec1f8-116">All numeric types, including the unsigned and floating-point types and `Decimal`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="ec1f8-117">备注</span><span class="sxs-lookup"><span data-stu-id="ec1f8-117">Remarks</span></span>  

 <span data-ttu-id="ec1f8-118">结果的数据类型取决于操作数的类型。</span><span class="sxs-lookup"><span data-stu-id="ec1f8-118">The data type of the result depends on the types of the operands.</span></span> <span data-ttu-id="ec1f8-119">下表显示了如何确定结果的数据类型。</span><span class="sxs-lookup"><span data-stu-id="ec1f8-119">The following table shows how the data type of the result is determined.</span></span>  
  
|<span data-ttu-id="ec1f8-120">操作数数据类型</span><span class="sxs-lookup"><span data-stu-id="ec1f8-120">Operand data types</span></span>|<span data-ttu-id="ec1f8-121">Result 数据类型</span><span class="sxs-lookup"><span data-stu-id="ec1f8-121">Result data type</span></span>|  
|---|---|  
|<span data-ttu-id="ec1f8-122">这两个表达式都是整型数据类型 ([SByte](../data-types/sbyte-data-type.md)、 [Byte](../data-types/byte-data-type.md)、 [Short](../data-types/short-data-type.md)、 [UShort](../data-types/ushort-data-type.md)、 [Integer](../data-types/integer-data-type.md)、 [UInteger](../data-types/uinteger-data-type.md)、 [Long](../data-types/long-data-type.md)、 [ULong](../data-types/ulong-data-type.md)) </span><span class="sxs-lookup"><span data-stu-id="ec1f8-122">Both expressions are integral data types ([SByte](../data-types/sbyte-data-type.md), [Byte](../data-types/byte-data-type.md), [Short](../data-types/short-data-type.md), [UShort](../data-types/ushort-data-type.md), [Integer](../data-types/integer-data-type.md), [UInteger](../data-types/uinteger-data-type.md), [Long](../data-types/long-data-type.md), [ULong](../data-types/ulong-data-type.md))</span></span>|<span data-ttu-id="ec1f8-123">适用于和的数据类型的数值数据类型 `number1` `number2` 。</span><span class="sxs-lookup"><span data-stu-id="ec1f8-123">A numeric data type appropriate for the data types of `number1` and `number2`.</span></span> <span data-ttu-id="ec1f8-124">请参阅 [运算符结果的数据类型](data-types-of-operator-results.md)中的 "整数算法" 表。</span><span class="sxs-lookup"><span data-stu-id="ec1f8-124">See the "Integer Arithmetic" tables in [Data Types of Operator Results](data-types-of-operator-results.md).</span></span>|  
|<span data-ttu-id="ec1f8-125">两个表达式都是 [小数](../data-types/decimal-data-type.md)</span><span class="sxs-lookup"><span data-stu-id="ec1f8-125">Both expressions are [Decimal](../data-types/decimal-data-type.md)</span></span>|`Decimal`|  
|<span data-ttu-id="ec1f8-126">这两个表达式都是 [单](../data-types/single-data-type.md)</span><span class="sxs-lookup"><span data-stu-id="ec1f8-126">Both expressions are [Single](../data-types/single-data-type.md)</span></span>|`Single`|  
|<span data-ttu-id="ec1f8-127">这两个表达式都是浮点数据类型 (`Single` 或 [Double](../data-types/double-data-type.md)) ，但不是两者 (都不是 `Single` `Decimal` 浮点数据类型) </span><span class="sxs-lookup"><span data-stu-id="ec1f8-127">Either expression is a floating-point data type (`Single` or [Double](../data-types/double-data-type.md)) but not both `Single` (note `Decimal` is not a floating-point data type)</span></span>|`Double`|  
  
 <span data-ttu-id="ec1f8-128">如果表达式的计算结果不为 [空](../nothing.md)，则将其视为零。</span><span class="sxs-lookup"><span data-stu-id="ec1f8-128">If an expression evaluates to [Nothing](../nothing.md), it is treated as zero.</span></span>  
  
## <a name="overloading"></a><span data-ttu-id="ec1f8-129">重载</span><span class="sxs-lookup"><span data-stu-id="ec1f8-129">Overloading</span></span>  

 <span data-ttu-id="ec1f8-130">`*`运算符可以 *重载*，这意味着当操作数具有该类或结构的类型时，该类或结构可以重新定义其行为。</span><span class="sxs-lookup"><span data-stu-id="ec1f8-130">The `*` operator can be *overloaded*, which means that a class or structure can redefine its behavior when an operand has the type of that class or structure.</span></span> <span data-ttu-id="ec1f8-131">如果你的代码在该类或结构上使用此运算符，请确保了解其重新定义的行为。</span><span class="sxs-lookup"><span data-stu-id="ec1f8-131">If your code uses this operator on such a class or structure, be sure you understand its redefined behavior.</span></span> <span data-ttu-id="ec1f8-132">有关详细信息，请参阅 [Operator Procedures](../../programming-guide/language-features/procedures/operator-procedures.md)。</span><span class="sxs-lookup"><span data-stu-id="ec1f8-132">For more information, see [Operator Procedures](../../programming-guide/language-features/procedures/operator-procedures.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="ec1f8-133">示例</span><span class="sxs-lookup"><span data-stu-id="ec1f8-133">Example</span></span>  

 <span data-ttu-id="ec1f8-134">此示例使用 `*` 运算符将两个数字相乘。</span><span class="sxs-lookup"><span data-stu-id="ec1f8-134">This example uses the `*` operator to multiply two numbers.</span></span> <span data-ttu-id="ec1f8-135">结果就是两个操作数的乘积。</span><span class="sxs-lookup"><span data-stu-id="ec1f8-135">The result is the product of the two operands.</span></span>  
  
 [!code-vb[VbVbalrOperators#4](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrOperators/VB/Class1.vb#4)]  
  
## <a name="see-also"></a><span data-ttu-id="ec1f8-136">请参阅</span><span class="sxs-lookup"><span data-stu-id="ec1f8-136">See also</span></span>

- [<span data-ttu-id="ec1f8-137">\* = 运算符</span><span class="sxs-lookup"><span data-stu-id="ec1f8-137">\*= Operator</span></span>](multiplication-assignment-operator.md)
- [<span data-ttu-id="ec1f8-138">算术运算符</span><span class="sxs-lookup"><span data-stu-id="ec1f8-138">Arithmetic Operators</span></span>](arithmetic-operators.md)
- [<span data-ttu-id="ec1f8-139">Visual Basic 中的运算符优先级</span><span class="sxs-lookup"><span data-stu-id="ec1f8-139">Operator Precedence in Visual Basic</span></span>](operator-precedence.md)
- [<span data-ttu-id="ec1f8-140">按功能列出的运算符</span><span class="sxs-lookup"><span data-stu-id="ec1f8-140">Operators Listed by Functionality</span></span>](operators-listed-by-functionality.md)
- [<span data-ttu-id="ec1f8-141">算术运算符 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="ec1f8-141">Arithmetic Operators in Visual Basic</span></span>](../../programming-guide/language-features/operators-and-expressions/arithmetic-operators.md)
