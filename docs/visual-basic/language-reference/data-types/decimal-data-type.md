---
description: '详细了解： Decimal 数据类型 (Visual Basic) '
title: Decimal 数据类型
ms.date: 07/20/2015
f1_keywords:
- vb.Decimal
helpviewer_keywords:
- literal type characters [Visual Basic], D
- trailing zeros
- real numbers
- trailing 0 characters [Visual Basic]
- Decimal data type
- D literal type character [Visual Basic]
- decimals, Decimal data type
- 0 characters [Visual Basic], trailing
- data types [Visual Basic], assigning
- decimal keyword [Visual Basic]
- numbers [Visual Basic], real
- variable-precision numbers
- zeros, trailing
- '@ identifier type character'
- identifier type characters [Visual Basic], @
ms.assetid: 1d855b45-afe2-45b0-a623-96b6f63a43d5
ms.openlocfilehash: 5806041e7737b8fe0f1c7ffa63f6cbadcbf92e42
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99792227"
---
# <a name="decimal-data-type-visual-basic"></a><span data-ttu-id="e1e8a-103">Decimal 数据类型 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="e1e8a-103">Decimal Data Type (Visual Basic)</span></span>

<span data-ttu-id="e1e8a-104">保存由表示 96 位（12 字节）整数按 10 的可变次幂缩放所得的 128 位（16 字节）值。</span><span class="sxs-lookup"><span data-stu-id="e1e8a-104">Holds signed 128-bit (16-byte) values representing 96-bit (12-byte) integer numbers scaled by a variable power of 10.</span></span> <span data-ttu-id="e1e8a-105">缩放系数指定小数点右侧的数字位数;范围为0到28。</span><span class="sxs-lookup"><span data-stu-id="e1e8a-105">The scaling factor specifies the number of digits to the right of the decimal point; it ranges from 0 through 28.</span></span> <span data-ttu-id="e1e8a-106">如果小数位数为 0 () ，则可能的最大值为 +/-79228162514264337593543950335 (+/-7.9228162514264337593543950335E + 28) 。</span><span class="sxs-lookup"><span data-stu-id="e1e8a-106">With a scale of 0 (no decimal places), the largest possible value is +/-79,228,162,514,264,337,593,543,950,335 (+/-7.9228162514264337593543950335E+28).</span></span> <span data-ttu-id="e1e8a-107">如果有28个小数位数，则最大值为 +/-7.9228162514264337593543950335，最小非零值为 +/-0.0000000000000000000000000001 (+/-1E-28) 。</span><span class="sxs-lookup"><span data-stu-id="e1e8a-107">With 28 decimal places, the largest value is +/-7.9228162514264337593543950335, and the smallest nonzero value is +/-0.0000000000000000000000000001 (+/-1E-28).</span></span>

## <a name="remarks"></a><span data-ttu-id="e1e8a-108">备注</span><span class="sxs-lookup"><span data-stu-id="e1e8a-108">Remarks</span></span>

<span data-ttu-id="e1e8a-109">`Decimal`数据类型为数字提供的有效位数最多。</span><span class="sxs-lookup"><span data-stu-id="e1e8a-109">The `Decimal` data type provides the greatest number of significant digits for a number.</span></span> <span data-ttu-id="e1e8a-110">它最多支持29个有效位数，并可表示超过 7.9228 x 10 ^ 28 的值。</span><span class="sxs-lookup"><span data-stu-id="e1e8a-110">It supports up to 29 significant digits and can represent values in excess of 7.9228 x 10^28.</span></span> <span data-ttu-id="e1e8a-111">它特别适用于需要大量数字但不允许舍入误差的计算（例如财务）。</span><span class="sxs-lookup"><span data-stu-id="e1e8a-111">It is particularly suitable for calculations, such as financial, that require a large number of digits but cannot tolerate rounding errors.</span></span>

<span data-ttu-id="e1e8a-112">`Decimal` 的默认值为 0。</span><span class="sxs-lookup"><span data-stu-id="e1e8a-112">The default value of `Decimal` is 0.</span></span>

## <a name="programming-tips"></a><span data-ttu-id="e1e8a-113">编程提示</span><span class="sxs-lookup"><span data-stu-id="e1e8a-113">Programming Tips</span></span>

- <span data-ttu-id="e1e8a-114">**Precision.**</span><span class="sxs-lookup"><span data-stu-id="e1e8a-114">**Precision.**</span></span> <span data-ttu-id="e1e8a-115">`Decimal` 不是浮点数据类型。</span><span class="sxs-lookup"><span data-stu-id="e1e8a-115">`Decimal` is not a floating-point data type.</span></span> <span data-ttu-id="e1e8a-116">`Decimal`结构包含一个二进制整数值以及一个符号位和一个整数比例因子，用于指定值的哪一部分是小数部分。</span><span class="sxs-lookup"><span data-stu-id="e1e8a-116">The `Decimal` structure holds a binary integer value, together with a sign bit and an integer scaling factor that specifies what portion of the value is a decimal fraction.</span></span> <span data-ttu-id="e1e8a-117">因此， `Decimal` 在内存中，数字的表示形式比浮点类型 (和) 更精确 `Single` `Double` 。</span><span class="sxs-lookup"><span data-stu-id="e1e8a-117">Because of this, `Decimal` numbers have a more precise representation in memory than floating-point types (`Single` and `Double`).</span></span>

- <span data-ttu-id="e1e8a-118">**性能。**</span><span class="sxs-lookup"><span data-stu-id="e1e8a-118">**Performance.**</span></span> <span data-ttu-id="e1e8a-119">`Decimal`数据类型是所有数值类型的最慢。</span><span class="sxs-lookup"><span data-stu-id="e1e8a-119">The `Decimal` data type is the slowest of all the numeric types.</span></span> <span data-ttu-id="e1e8a-120">在选择数据类型之前，应权衡精度与性能的重要性。</span><span class="sxs-lookup"><span data-stu-id="e1e8a-120">You should weigh the importance of precision against performance before choosing a data type.</span></span>

- <span data-ttu-id="e1e8a-121">**扩大.**</span><span class="sxs-lookup"><span data-stu-id="e1e8a-121">**Widening.**</span></span> <span data-ttu-id="e1e8a-122">`Decimal`数据类型扩大到 `Single` 或 `Double` 。</span><span class="sxs-lookup"><span data-stu-id="e1e8a-122">The `Decimal` data type widens to `Single` or `Double`.</span></span> <span data-ttu-id="e1e8a-123">这意味着你可以转换 `Decimal` 为这些类型中的任何一种，而不会遇到 <xref:System.OverflowException?displayProperty=nameWithType> 错误。</span><span class="sxs-lookup"><span data-stu-id="e1e8a-123">This means you can convert `Decimal` to either of these types without encountering a <xref:System.OverflowException?displayProperty=nameWithType> error.</span></span>

- <span data-ttu-id="e1e8a-124">**尾随零。**</span><span class="sxs-lookup"><span data-stu-id="e1e8a-124">**Trailing Zeros.**</span></span> <span data-ttu-id="e1e8a-125">Visual Basic 不会在文本中存储尾随零 `Decimal` 。</span><span class="sxs-lookup"><span data-stu-id="e1e8a-125">Visual Basic does not store trailing zeros in a `Decimal` literal.</span></span> <span data-ttu-id="e1e8a-126">但是， `Decimal` 变量保留了任何尾随零获取计算。</span><span class="sxs-lookup"><span data-stu-id="e1e8a-126">However, a `Decimal` variable preserves any trailing zeros acquired computationally.</span></span> <span data-ttu-id="e1e8a-127">下面的示例阐释了这一点。</span><span class="sxs-lookup"><span data-stu-id="e1e8a-127">The following example illustrates this.</span></span>

  ```vb
  Dim d1, d2, d3, d4 As Decimal
  d1 = 2.375D
  d2 = 1.625D
  d3 = d1 + d2
  d4 = 4.000D
  MsgBox("d1 = " & CStr(d1) & ", d2 = " & CStr(d2) &
        ", d3 = " & CStr(d3) & ", d4 = " & CStr(d4))
  ```

  <span data-ttu-id="e1e8a-128">`MsgBox`上一示例中的输出如下所示：</span><span class="sxs-lookup"><span data-stu-id="e1e8a-128">The output of `MsgBox` in the preceding example is as follows:</span></span>

  ```console
  d1 = 2.375, d2 = 1.625, d3 = 4.000, d4 = 4
  ```

- <span data-ttu-id="e1e8a-129">**键入字符。**</span><span class="sxs-lookup"><span data-stu-id="e1e8a-129">**Type Characters.**</span></span> <span data-ttu-id="e1e8a-130">将文本类型字符 `D` 追加到文本会将其强制转换为 `Decimal` 数据类型。</span><span class="sxs-lookup"><span data-stu-id="e1e8a-130">Appending the literal type character `D` to a literal forces it to the `Decimal` data type.</span></span> <span data-ttu-id="e1e8a-131">将标识符类型字符 `@` 追加到任何标识符会将其强制转换为 `Decimal`。</span><span class="sxs-lookup"><span data-stu-id="e1e8a-131">Appending the identifier type character `@` to any identifier forces it to `Decimal`.</span></span>

- <span data-ttu-id="e1e8a-132">**Framework 类型。**</span><span class="sxs-lookup"><span data-stu-id="e1e8a-132">**Framework Type.**</span></span> <span data-ttu-id="e1e8a-133">.NET Framework 中的对应类型是 <xref:System.Decimal?displayProperty=nameWithType> 结构。</span><span class="sxs-lookup"><span data-stu-id="e1e8a-133">The corresponding type in the .NET Framework is the <xref:System.Decimal?displayProperty=nameWithType> structure.</span></span>

## <a name="range"></a><span data-ttu-id="e1e8a-134">范围</span><span class="sxs-lookup"><span data-stu-id="e1e8a-134">Range</span></span>

 <span data-ttu-id="e1e8a-135">你可能需要使用 `D` 类型字符将较大的值分配给 `Decimal` 变量或常数。</span><span class="sxs-lookup"><span data-stu-id="e1e8a-135">You might need to use the `D` type character to assign a large value to a `Decimal` variable or constant.</span></span> <span data-ttu-id="e1e8a-136">此要求是因为编译器会将文本解释为 `Long` ，除非文本类型字符跟在文本后，如下面的示例所示。</span><span class="sxs-lookup"><span data-stu-id="e1e8a-136">This requirement is because the compiler interprets a literal as `Long` unless a literal type character follows the literal, as the following example shows.</span></span>

```vb
Dim bigDec1 As Decimal = 9223372036854775807   ' No overflow.
Dim bigDec2 As Decimal = 9223372036854775808   ' Overflow.
Dim bigDec3 As Decimal = 9223372036854775808D  ' No overflow.
```

<span data-ttu-id="e1e8a-137">的声明 `bigDec1` 不会产生溢出，因为赋给它的值落在范围内 `Long` 。</span><span class="sxs-lookup"><span data-stu-id="e1e8a-137">The declaration for `bigDec1` doesn't produce an overflow because the value that's assigned to it falls within the range for `Long`.</span></span> <span data-ttu-id="e1e8a-138">`Long`可以将值分配给 `Decimal` 变量。</span><span class="sxs-lookup"><span data-stu-id="e1e8a-138">The `Long` value can be assigned to the `Decimal` variable.</span></span>

<span data-ttu-id="e1e8a-139">的声明 `bigDec2` 会生成溢出错误，因为赋给它的值太大 `Long` 。</span><span class="sxs-lookup"><span data-stu-id="e1e8a-139">The declaration for `bigDec2` generates an overflow error because the value that's assigned to it is too large for `Long`.</span></span> <span data-ttu-id="e1e8a-140">由于不能首先将数字文本解释为 `Long` ，因此不能将其分配给 `Decimal` 变量。</span><span class="sxs-lookup"><span data-stu-id="e1e8a-140">Because the numeric literal can't first be interpreted as a `Long`, it can't be assigned to the `Decimal` variable.</span></span>

<span data-ttu-id="e1e8a-141">对于 `bigDec3` ，文本类型字符 `D` 通过强制编译器将文本解释为而不是，来解决此问题 `Decimal` `Long` 。</span><span class="sxs-lookup"><span data-stu-id="e1e8a-141">For `bigDec3`, the literal type character `D` solves the problem by forcing the compiler to interpret the literal as a `Decimal` instead of as a `Long`.</span></span>

## <a name="see-also"></a><span data-ttu-id="e1e8a-142">请参阅</span><span class="sxs-lookup"><span data-stu-id="e1e8a-142">See also</span></span>

- <xref:System.Decimal?displayProperty=nameWithType>
- <xref:System.Decimal.%23ctor%2A>
- <xref:System.Math.Round%2A?displayProperty=nameWithType>
- [<span data-ttu-id="e1e8a-143">数据类型</span><span class="sxs-lookup"><span data-stu-id="e1e8a-143">Data Types</span></span>](index.md)
- [<span data-ttu-id="e1e8a-144">Single 数据类型</span><span class="sxs-lookup"><span data-stu-id="e1e8a-144">Single Data Type</span></span>](single-data-type.md)
- [<span data-ttu-id="e1e8a-145">Double 数据类型</span><span class="sxs-lookup"><span data-stu-id="e1e8a-145">Double Data Type</span></span>](double-data-type.md)
- [<span data-ttu-id="e1e8a-146">Type Conversion Functions</span><span class="sxs-lookup"><span data-stu-id="e1e8a-146">Type Conversion Functions</span></span>](../functions/type-conversion-functions.md)
- [<span data-ttu-id="e1e8a-147">转换摘要</span><span class="sxs-lookup"><span data-stu-id="e1e8a-147">Conversion Summary</span></span>](../keywords/conversion-summary.md)
- [<span data-ttu-id="e1e8a-148">有效使用数据类型</span><span class="sxs-lookup"><span data-stu-id="e1e8a-148">Efficient Use of Data Types</span></span>](../../programming-guide/language-features/data-types/efficient-use-of-data-types.md)
