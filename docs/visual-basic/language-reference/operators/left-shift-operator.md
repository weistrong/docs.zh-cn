---
description: '了解详细信息：  << 运算符 (Visual Basic) '
title: << 运算符
ms.date: 07/20/2015
f1_keywords:
- vb.<<
helpviewer_keywords:
- bit shift operators [Visual Basic]
- << operator [Visual Basic]
- operator <<, Visual Basic left shift operator
ms.assetid: fdb93d25-81ba-417f-b808-41207bfb8440
ms.openlocfilehash: 079af61e5c4ce3834db0877feace724c74c8169c
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99665622"
---
# <a name="-operator-visual-basic"></a><span data-ttu-id="c0e52-103">\<\< 操作员 (Visual Basic) </span><span class="sxs-lookup"><span data-stu-id="c0e52-103">\<\< Operator (Visual Basic)</span></span>

<span data-ttu-id="c0e52-104">对位模式执行算术左移位运算。</span><span class="sxs-lookup"><span data-stu-id="c0e52-104">Performs an arithmetic left shift on a bit pattern.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c0e52-105">语法</span><span class="sxs-lookup"><span data-stu-id="c0e52-105">Syntax</span></span>  
  
```vb  
result = pattern << amount  
```  
  
## <a name="parts"></a><span data-ttu-id="c0e52-106">组成部分</span><span class="sxs-lookup"><span data-stu-id="c0e52-106">Parts</span></span>  

 `result`  
 <span data-ttu-id="c0e52-107">必需。</span><span class="sxs-lookup"><span data-stu-id="c0e52-107">Required.</span></span> <span data-ttu-id="c0e52-108">整数数值。</span><span class="sxs-lookup"><span data-stu-id="c0e52-108">Integral numeric value.</span></span> <span data-ttu-id="c0e52-109">对该位模式进行移位的结果。</span><span class="sxs-lookup"><span data-stu-id="c0e52-109">The result of shifting the bit pattern.</span></span> <span data-ttu-id="c0e52-110">数据类型与 `pattern` 的数据类型相同。</span><span class="sxs-lookup"><span data-stu-id="c0e52-110">The data type is the same as that of `pattern`.</span></span>  
  
 `pattern`  
 <span data-ttu-id="c0e52-111">必需。</span><span class="sxs-lookup"><span data-stu-id="c0e52-111">Required.</span></span> <span data-ttu-id="c0e52-112">整型数值表达式。</span><span class="sxs-lookup"><span data-stu-id="c0e52-112">Integral numeric expression.</span></span> <span data-ttu-id="c0e52-113">要进行移位的位模式。</span><span class="sxs-lookup"><span data-stu-id="c0e52-113">The bit pattern to be shifted.</span></span> <span data-ttu-id="c0e52-114">数据类型必须为整型（`SByte`、`Byte`、`Short`、`UShort`、`Integer`、`UInteger`、`Long` 或 `ULong`）。</span><span class="sxs-lookup"><span data-stu-id="c0e52-114">The data type must be an integral type (`SByte`, `Byte`, `Short`, `UShort`, `Integer`, `UInteger`, `Long`, or `ULong`).</span></span>  
  
 `amount`  
 <span data-ttu-id="c0e52-115">必需。</span><span class="sxs-lookup"><span data-stu-id="c0e52-115">Required.</span></span> <span data-ttu-id="c0e52-116">数值表达式。</span><span class="sxs-lookup"><span data-stu-id="c0e52-116">Numeric expression.</span></span> <span data-ttu-id="c0e52-117">要将该位模式移位的位数。</span><span class="sxs-lookup"><span data-stu-id="c0e52-117">The number of bits to shift the bit pattern.</span></span> <span data-ttu-id="c0e52-118">数据类型必须为 `Integer` 或扩展到 `Integer`。</span><span class="sxs-lookup"><span data-stu-id="c0e52-118">The data type must be `Integer` or widen to `Integer`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="c0e52-119">备注</span><span class="sxs-lookup"><span data-stu-id="c0e52-119">Remarks</span></span>  

 <span data-ttu-id="c0e52-120">算术移位不是循环的，这意味着，不会在另一端重新引入结果的末尾以外的位。</span><span class="sxs-lookup"><span data-stu-id="c0e52-120">Arithmetic shifts are not circular, which means the bits shifted off one end of the result are not reintroduced at the other end.</span></span> <span data-ttu-id="c0e52-121">在算术左移位中，将丢弃超出结果数据类型范围的位，并将在右侧空出的位位置设置为零。</span><span class="sxs-lookup"><span data-stu-id="c0e52-121">In an arithmetic left shift, the bits shifted beyond the range of the result data type are discarded, and the bit positions vacated on the right are set to zero.</span></span>  
  
 <span data-ttu-id="c0e52-122">若要防止移位比结果可以容纳的位数多，Visual Basic 用与的 `amount` 数据类型相对应的大小掩码来屏蔽的值 `pattern` 。</span><span class="sxs-lookup"><span data-stu-id="c0e52-122">To prevent a shift by more bits than the result can hold, Visual Basic masks the value of `amount` with a size mask that corresponds to the data type of `pattern`.</span></span> <span data-ttu-id="c0e52-123">这些值的二进制和均用于移位量。</span><span class="sxs-lookup"><span data-stu-id="c0e52-123">The binary AND of these values is used for the shift amount.</span></span> <span data-ttu-id="c0e52-124">大小掩码如下：</span><span class="sxs-lookup"><span data-stu-id="c0e52-124">The size masks are as follows:</span></span>  
  
|<span data-ttu-id="c0e52-125">数据类型 `pattern`</span><span class="sxs-lookup"><span data-stu-id="c0e52-125">Data type of `pattern`</span></span>|<span data-ttu-id="c0e52-126">大小掩码 (decimal) </span><span class="sxs-lookup"><span data-stu-id="c0e52-126">Size mask (decimal)</span></span>|<span data-ttu-id="c0e52-127">大小掩码 (十六进制) </span><span class="sxs-lookup"><span data-stu-id="c0e52-127">Size mask (hexadecimal)</span></span>|  
|----------------------------|---------------------------|-------------------------------|  
|<span data-ttu-id="c0e52-128">`SByte`, `Byte`</span><span class="sxs-lookup"><span data-stu-id="c0e52-128">`SByte`, `Byte`</span></span>|<span data-ttu-id="c0e52-129">7</span><span class="sxs-lookup"><span data-stu-id="c0e52-129">7</span></span>|<span data-ttu-id="c0e52-130">&H00000007</span><span class="sxs-lookup"><span data-stu-id="c0e52-130">&H00000007</span></span>|  
|<span data-ttu-id="c0e52-131">`Short`, `UShort`</span><span class="sxs-lookup"><span data-stu-id="c0e52-131">`Short`, `UShort`</span></span>|<span data-ttu-id="c0e52-132">15</span><span class="sxs-lookup"><span data-stu-id="c0e52-132">15</span></span>|<span data-ttu-id="c0e52-133">&H0000000F</span><span class="sxs-lookup"><span data-stu-id="c0e52-133">&H0000000F</span></span>|  
|<span data-ttu-id="c0e52-134">`Integer`, `UInteger`</span><span class="sxs-lookup"><span data-stu-id="c0e52-134">`Integer`, `UInteger`</span></span>|<span data-ttu-id="c0e52-135">31</span><span class="sxs-lookup"><span data-stu-id="c0e52-135">31</span></span>|<span data-ttu-id="c0e52-136">&H0000001F</span><span class="sxs-lookup"><span data-stu-id="c0e52-136">&H0000001F</span></span>|  
|<span data-ttu-id="c0e52-137">`Long`, `ULong`</span><span class="sxs-lookup"><span data-stu-id="c0e52-137">`Long`, `ULong`</span></span>|<span data-ttu-id="c0e52-138">63</span><span class="sxs-lookup"><span data-stu-id="c0e52-138">63</span></span>|<span data-ttu-id="c0e52-139">&H0000003F</span><span class="sxs-lookup"><span data-stu-id="c0e52-139">&H0000003F</span></span>|  
  
 <span data-ttu-id="c0e52-140">如果 `amount` 为零，则的值与的 `result` 值相同 `pattern` 。</span><span class="sxs-lookup"><span data-stu-id="c0e52-140">If `amount` is zero, the value of `result` is identical to the value of `pattern`.</span></span> <span data-ttu-id="c0e52-141">如果 `amount` 为负，则将其视为无符号值并使用适当的大小掩码屏蔽。</span><span class="sxs-lookup"><span data-stu-id="c0e52-141">If `amount` is negative, it is taken as an unsigned value and masked with the appropriate size mask.</span></span>  
  
 <span data-ttu-id="c0e52-142">算术移位从不产生溢出异常。</span><span class="sxs-lookup"><span data-stu-id="c0e52-142">Arithmetic shifts never generate overflow exceptions.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="c0e52-143">`<<`运算符可以 *重载*，这意味着当操作数具有该类或结构的类型时，该类或结构可以重新定义其行为。</span><span class="sxs-lookup"><span data-stu-id="c0e52-143">The `<<` operator can be *overloaded*, which means that a class or structure can redefine its behavior when an operand has the type of that class or structure.</span></span> <span data-ttu-id="c0e52-144">如果代码对这样的类或结构使用此运算符，请确保了解其重新定义的行为。</span><span class="sxs-lookup"><span data-stu-id="c0e52-144">If your code uses this operator on such a class or structure, be sure that you understand its redefined behavior.</span></span> <span data-ttu-id="c0e52-145">有关详细信息，请参阅 [Operator Procedures](../../programming-guide/language-features/procedures/operator-procedures.md)。</span><span class="sxs-lookup"><span data-stu-id="c0e52-145">For more information, see [Operator Procedures](../../programming-guide/language-features/procedures/operator-procedures.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="c0e52-146">示例</span><span class="sxs-lookup"><span data-stu-id="c0e52-146">Example</span></span>  

 <span data-ttu-id="c0e52-147">下面的示例使用 `<<` 运算符对整数值执行算术左移位。</span><span class="sxs-lookup"><span data-stu-id="c0e52-147">The following example uses the `<<` operator to perform arithmetic left shifts on integral values.</span></span> <span data-ttu-id="c0e52-148">结果始终与要移动的表达式的数据类型相同。</span><span class="sxs-lookup"><span data-stu-id="c0e52-148">The result always has the same data type as that of the expression being shifted.</span></span>  
  
 [!code-vb[VbVbalrOperators#12](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrOperators/VB/Class1.vb#12)]  
  
 <span data-ttu-id="c0e52-149">上述示例的结果如下所示：</span><span class="sxs-lookup"><span data-stu-id="c0e52-149">The results of the previous example are as follows:</span></span>  
  
- <span data-ttu-id="c0e52-150">`result1` 为 192 (0000 0000 1100 0000) 。</span><span class="sxs-lookup"><span data-stu-id="c0e52-150">`result1` is 192 (0000 0000 1100 0000).</span></span>  
  
- <span data-ttu-id="c0e52-151">`result2` 为 3072 (0000 1100 0000 0000) 。</span><span class="sxs-lookup"><span data-stu-id="c0e52-151">`result2` is 3072 (0000 1100 0000 0000).</span></span>  
  
- <span data-ttu-id="c0e52-152">`result3` 为-32768 (1000 0000 0000 0000) 。</span><span class="sxs-lookup"><span data-stu-id="c0e52-152">`result3` is -32768 (1000 0000 0000 0000).</span></span>  
  
- <span data-ttu-id="c0e52-153">`result4` 为 384 (0000 0001 1000 0000) 。</span><span class="sxs-lookup"><span data-stu-id="c0e52-153">`result4` is 384 (0000 0001 1000 0000).</span></span>  
  
- <span data-ttu-id="c0e52-154">`result5` 为 0 (将15个位置向左移动) 。</span><span class="sxs-lookup"><span data-stu-id="c0e52-154">`result5` is 0 (shifted 15 places to the left).</span></span>  
  
 <span data-ttu-id="c0e52-155">的移位量 `result4` 计算为17和15，这等于1。</span><span class="sxs-lookup"><span data-stu-id="c0e52-155">The shift amount for `result4` is calculated as 17 AND 15, which equals 1.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c0e52-156">请参阅</span><span class="sxs-lookup"><span data-stu-id="c0e52-156">See also</span></span>

- [<span data-ttu-id="c0e52-157">移位运算符</span><span class="sxs-lookup"><span data-stu-id="c0e52-157">Bit Shift Operators</span></span>](bit-shift-operators.md)
- [<span data-ttu-id="c0e52-158">赋值运算符</span><span class="sxs-lookup"><span data-stu-id="c0e52-158">Assignment Operators</span></span>](assignment-operators.md)
- [<span data-ttu-id="c0e52-159"><<= 运算符</span><span class="sxs-lookup"><span data-stu-id="c0e52-159"><<= Operator</span></span>](left-shift-assignment-operator.md)
- [<span data-ttu-id="c0e52-160">Visual Basic 中的运算符优先级</span><span class="sxs-lookup"><span data-stu-id="c0e52-160">Operator Precedence in Visual Basic</span></span>](operator-precedence.md)
- [<span data-ttu-id="c0e52-161">按功能列出的运算符</span><span class="sxs-lookup"><span data-stu-id="c0e52-161">Operators Listed by Functionality</span></span>](operators-listed-by-functionality.md)
- [<span data-ttu-id="c0e52-162">算术运算符 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="c0e52-162">Arithmetic Operators in Visual Basic</span></span>](../../programming-guide/language-features/operators-and-expressions/arithmetic-operators.md)
