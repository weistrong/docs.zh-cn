---
description: '了解详细信息： Double 数据类型 (Visual Basic) '
title: Double 数据类型
ms.date: 07/20/2015
f1_keywords:
- vb.Double
helpviewer_keywords:
- 'identifier type characters [Visual Basic], #'
- trailing zeros
- real numbers
- trailing 0 characters [Visual Basic]
- 0 characters [Visual Basic], trailing
- literal type characters [Visual Basic], R
- data types [Visual Basic], assigning
- Double data type [Visual Basic]
- '# identifier type character'
- double-precision numbers
- floating-point numbers [Visual Basic], Double data type
- R literal type character [Visual Basic]
- zeros, trailing
- Double data type
ms.assetid: 0c5670f7-fcb1-453a-bef1-374730cd38fd
ms.openlocfilehash: ae7b87b392038c67ba47e09d7ca995562bf06c1d
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99792214"
---
# <a name="double-data-type-visual-basic"></a><span data-ttu-id="d8380-103">Double 数据类型 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="d8380-103">Double Data Type (Visual Basic)</span></span>

<span data-ttu-id="d8380-104">将已签名的 IEEE 64 位 (8) 字节的双精度浮点数，该值的范围为-1.79769313486231570 E + 308 到-4.94065645841246544 E-324 （对于负值），从 4.94065645841246544 E-324 到 1.79769313486231570 E + 308，用于正值。</span><span class="sxs-lookup"><span data-stu-id="d8380-104">Holds signed IEEE 64-bit (8-byte) double-precision floating-point numbers that range in value from -1.79769313486231570E+308 through -4.94065645841246544E-324 for negative values and from 4.94065645841246544E-324 through 1.79769313486231570E+308 for positive values.</span></span> <span data-ttu-id="d8380-105">双精度数字存储实数的近似值。</span><span class="sxs-lookup"><span data-stu-id="d8380-105">Double-precision numbers store an approximation of a real number.</span></span>

## <a name="remarks"></a><span data-ttu-id="d8380-106">备注</span><span class="sxs-lookup"><span data-stu-id="d8380-106">Remarks</span></span>

<span data-ttu-id="d8380-107">`Double`数据类型为数字提供最大和最小的度。</span><span class="sxs-lookup"><span data-stu-id="d8380-107">The `Double` data type provides the largest and smallest possible magnitudes for a number.</span></span>

<span data-ttu-id="d8380-108">`Double` 的默认值为 0。</span><span class="sxs-lookup"><span data-stu-id="d8380-108">The default value of `Double` is 0.</span></span>

## <a name="programming-tips"></a><span data-ttu-id="d8380-109">编程提示</span><span class="sxs-lookup"><span data-stu-id="d8380-109">Programming Tips</span></span>

- <span data-ttu-id="d8380-110">**Precision.**</span><span class="sxs-lookup"><span data-stu-id="d8380-110">**Precision.**</span></span> <span data-ttu-id="d8380-111">使用浮点数时，请记住，它们在内存中不一定有精确的表示形式。</span><span class="sxs-lookup"><span data-stu-id="d8380-111">When you work with floating-point numbers, remember that they do not always have a precise representation in memory.</span></span> <span data-ttu-id="d8380-112">这可能会导致某些操作产生意外结果，如值比较和 `Mod` 运算符。</span><span class="sxs-lookup"><span data-stu-id="d8380-112">This could lead to unexpected results from certain operations, such as value comparison and the `Mod` operator.</span></span> <span data-ttu-id="d8380-113">有关详细信息，请参阅 [数据类型疑难解答](../../programming-guide/language-features/data-types/troubleshooting-data-types.md)。</span><span class="sxs-lookup"><span data-stu-id="d8380-113">For more information, see [Troubleshooting Data Types](../../programming-guide/language-features/data-types/troubleshooting-data-types.md).</span></span>

- <span data-ttu-id="d8380-114">**尾随零。**</span><span class="sxs-lookup"><span data-stu-id="d8380-114">**Trailing Zeros.**</span></span> <span data-ttu-id="d8380-115">浮点数据类型不包含尾随零字符的任何内部表示形式。</span><span class="sxs-lookup"><span data-stu-id="d8380-115">The floating-point data types do not have any internal representation of trailing zero characters.</span></span> <span data-ttu-id="d8380-116">例如，它们不区分4.2000 和4.2。</span><span class="sxs-lookup"><span data-stu-id="d8380-116">For example, they do not distinguish between 4.2000 and 4.2.</span></span> <span data-ttu-id="d8380-117">因此，在显示或打印浮点值时，不会出现尾随零字符。</span><span class="sxs-lookup"><span data-stu-id="d8380-117">Consequently, trailing zero characters do not appear when you display or print floating-point values.</span></span>

- <span data-ttu-id="d8380-118">**键入字符。**</span><span class="sxs-lookup"><span data-stu-id="d8380-118">**Type Characters.**</span></span> <span data-ttu-id="d8380-119">将文本类型字符 `R` 追加到文本会将其强制转换为 `Double` 数据类型。</span><span class="sxs-lookup"><span data-stu-id="d8380-119">Appending the literal type character `R` to a literal forces it to the `Double` data type.</span></span> <span data-ttu-id="d8380-120">例如，如果整数值后跟 `R` ，则该值将更改为 `Double` 。</span><span class="sxs-lookup"><span data-stu-id="d8380-120">For example, if an integer value is followed by `R`, the value is changed to a `Double`.</span></span>

  ```vb
  ' Visual Basic expands the 4 in the statement Dim dub As Double = 4R to 4.0:
  Dim dub As Double = 4.0R
  ```

  <span data-ttu-id="d8380-121">将标识符类型字符 `#` 追加到任何标识符会将其强制转换为 `Double`。</span><span class="sxs-lookup"><span data-stu-id="d8380-121">Appending the identifier type character `#` to any identifier forces it to `Double`.</span></span> <span data-ttu-id="d8380-122">在下面的示例中，变量 `num` 被类型化为 `Double` ：</span><span class="sxs-lookup"><span data-stu-id="d8380-122">In the following example, the variable `num` is typed as a `Double`:</span></span>

  ```vb
  Dim num# = 3
  ```

- <span data-ttu-id="d8380-123">**Framework 类型。**</span><span class="sxs-lookup"><span data-stu-id="d8380-123">**Framework Type.**</span></span> <span data-ttu-id="d8380-124">.NET Framework 中的对应类型是 <xref:System.Double?displayProperty=nameWithType> 结构。</span><span class="sxs-lookup"><span data-stu-id="d8380-124">The corresponding type in the .NET Framework is the <xref:System.Double?displayProperty=nameWithType> structure.</span></span>

## <a name="see-also"></a><span data-ttu-id="d8380-125">请参阅</span><span class="sxs-lookup"><span data-stu-id="d8380-125">See also</span></span>

- <xref:System.Double?displayProperty=nameWithType>
- [<span data-ttu-id="d8380-126">数据类型</span><span class="sxs-lookup"><span data-stu-id="d8380-126">Data Types</span></span>](index.md)
- [<span data-ttu-id="d8380-127">Decimal 数据类型</span><span class="sxs-lookup"><span data-stu-id="d8380-127">Decimal Data Type</span></span>](decimal-data-type.md)
- [<span data-ttu-id="d8380-128">Single 数据类型</span><span class="sxs-lookup"><span data-stu-id="d8380-128">Single Data Type</span></span>](single-data-type.md)
- [<span data-ttu-id="d8380-129">Type Conversion Functions</span><span class="sxs-lookup"><span data-stu-id="d8380-129">Type Conversion Functions</span></span>](../functions/type-conversion-functions.md)
- [<span data-ttu-id="d8380-130">转换摘要</span><span class="sxs-lookup"><span data-stu-id="d8380-130">Conversion Summary</span></span>](../keywords/conversion-summary.md)
- [<span data-ttu-id="d8380-131">有效使用数据类型</span><span class="sxs-lookup"><span data-stu-id="d8380-131">Efficient Use of Data Types</span></span>](../../programming-guide/language-features/data-types/efficient-use-of-data-types.md)
- [<span data-ttu-id="d8380-132">数据类型疑难解答</span><span class="sxs-lookup"><span data-stu-id="d8380-132">Troubleshooting Data Types</span></span>](../../programming-guide/language-features/data-types/troubleshooting-data-types.md)
- [<span data-ttu-id="d8380-133">类型字符</span><span class="sxs-lookup"><span data-stu-id="d8380-133">Type Characters</span></span>](../../programming-guide/language-features/data-types/type-characters.md)
