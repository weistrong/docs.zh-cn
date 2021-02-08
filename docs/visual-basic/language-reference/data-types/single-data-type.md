---
description: '了解详细信息：单一数据类型 (Visual Basic) '
title: Single 数据类型
ms.date: 07/20/2015
f1_keywords:
- vb.Single
helpviewer_keywords:
- Single data type
- F literal type character [Visual Basic]
- trailing zeros
- real numbers
- literal type characters [Visual Basic], F
- trailing 0 characters [Visual Basic]
- identifier type characters [Visual Basic], !
- single-precision numbers
- '! identifier type character'
- 0 characters [Visual Basic], trailing
- data types [Visual Basic], assigning
- floating-point numbers [Visual Basic], Single data type
- numbers [Visual Basic], real
- zeros, trailing
- numbers [Visual Basic], floating point
ms.assetid: 224a2795-4cd5-496c-8f7a-a4f05a06d45d
ms.openlocfilehash: f30e21d3b2d2960a040609a9422ec71cc029f5be
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99792123"
---
# <a name="single-data-type-visual-basic"></a><span data-ttu-id="6a0c0-103">Single 数据类型 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="6a0c0-103">Single Data Type (Visual Basic)</span></span>

<span data-ttu-id="6a0c0-104">为正值，保留已签名的 IEEE 32 位 (4 个) 字节的单精度浮点数，范围为-3.4028235 E + 38 到-1.401298 E-45，表示负值，从 1.401298 E-45 到 3.4028235 E + 38。</span><span class="sxs-lookup"><span data-stu-id="6a0c0-104">Holds signed IEEE 32-bit (4-byte) single-precision floating-point numbers ranging in value from -3.4028235E+38 through -1.401298E-45 for negative values and from 1.401298E-45 through 3.4028235E+38 for positive values.</span></span> <span data-ttu-id="6a0c0-105">单精度数字存储实数的近似值。</span><span class="sxs-lookup"><span data-stu-id="6a0c0-105">Single-precision numbers store an approximation of a real number.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="6a0c0-106">备注</span><span class="sxs-lookup"><span data-stu-id="6a0c0-106">Remarks</span></span>  

 <span data-ttu-id="6a0c0-107">使用 `Single` 数据类型可包含不需要的完整数据宽度的浮点值 `Double` 。</span><span class="sxs-lookup"><span data-stu-id="6a0c0-107">Use the `Single` data type to contain floating-point values that do not require the full data width of `Double`.</span></span> <span data-ttu-id="6a0c0-108">在某些情况下，公共语言运行时可以将变量紧密地打包在 `Single` 一起，并节省内存消耗。</span><span class="sxs-lookup"><span data-stu-id="6a0c0-108">In some cases the common language runtime might be able to pack your `Single` variables closely together and save memory consumption.</span></span>  
  
 <span data-ttu-id="6a0c0-109">`Single` 的默认值为 0。</span><span class="sxs-lookup"><span data-stu-id="6a0c0-109">The default value of `Single` is 0.</span></span>  
  
## <a name="programming-tips"></a><span data-ttu-id="6a0c0-110">编程提示</span><span class="sxs-lookup"><span data-stu-id="6a0c0-110">Programming Tips</span></span>  
  
- <span data-ttu-id="6a0c0-111">**Precision.**</span><span class="sxs-lookup"><span data-stu-id="6a0c0-111">**Precision.**</span></span> <span data-ttu-id="6a0c0-112">使用浮点数时，请记住，它们在内存中不一定有精确的表示形式。</span><span class="sxs-lookup"><span data-stu-id="6a0c0-112">When you work with floating-point numbers, keep in mind that they do not always have a precise representation in memory.</span></span> <span data-ttu-id="6a0c0-113">这可能会导致某些操作产生意外结果，如值比较和 `Mod` 运算符。</span><span class="sxs-lookup"><span data-stu-id="6a0c0-113">This could lead to unexpected results from certain operations, such as value comparison and the `Mod` operator.</span></span> <span data-ttu-id="6a0c0-114">有关详细信息，请参阅 [数据类型疑难解答](../../programming-guide/language-features/data-types/troubleshooting-data-types.md)。</span><span class="sxs-lookup"><span data-stu-id="6a0c0-114">For more information, see [Troubleshooting Data Types](../../programming-guide/language-features/data-types/troubleshooting-data-types.md).</span></span>  
  
- <span data-ttu-id="6a0c0-115">**扩大.**</span><span class="sxs-lookup"><span data-stu-id="6a0c0-115">**Widening.**</span></span> <span data-ttu-id="6a0c0-116">`Single`数据类型扩大到 `Double` 。</span><span class="sxs-lookup"><span data-stu-id="6a0c0-116">The `Single` data type widens to `Double`.</span></span> <span data-ttu-id="6a0c0-117">这意味着你可以转换 `Single` 为， `Double` 而不会遇到 <xref:System.OverflowException?displayProperty=nameWithType> 错误。</span><span class="sxs-lookup"><span data-stu-id="6a0c0-117">This means you can convert `Single` to `Double` without encountering a <xref:System.OverflowException?displayProperty=nameWithType> error.</span></span>  
  
- <span data-ttu-id="6a0c0-118">**尾随零。**</span><span class="sxs-lookup"><span data-stu-id="6a0c0-118">**Trailing Zeros.**</span></span> <span data-ttu-id="6a0c0-119">浮点数据类型不包含尾随0字符的任何内部表示形式。</span><span class="sxs-lookup"><span data-stu-id="6a0c0-119">The floating-point data types do not have any internal representation of trailing 0 characters.</span></span> <span data-ttu-id="6a0c0-120">例如，它们不区分4.2000 和4.2。</span><span class="sxs-lookup"><span data-stu-id="6a0c0-120">For example, they do not distinguish between 4.2000 and 4.2.</span></span> <span data-ttu-id="6a0c0-121">因此，在显示或打印浮点值时，不会出现尾随0字符。</span><span class="sxs-lookup"><span data-stu-id="6a0c0-121">Consequently, trailing 0 characters do not appear when you display or print floating-point values.</span></span>  
  
- <span data-ttu-id="6a0c0-122">**键入字符。**</span><span class="sxs-lookup"><span data-stu-id="6a0c0-122">**Type Characters.**</span></span> <span data-ttu-id="6a0c0-123">将文本类型字符 `F` 追加到文本会将其强制转换为 `Single` 数据类型。</span><span class="sxs-lookup"><span data-stu-id="6a0c0-123">Appending the literal type character `F` to a literal forces it to the `Single` data type.</span></span> <span data-ttu-id="6a0c0-124">将标识符类型字符 `!` 追加到任何标识符会将其强制转换为 `Single`。</span><span class="sxs-lookup"><span data-stu-id="6a0c0-124">Appending the identifier type character `!` to any identifier forces it to `Single`.</span></span>  
  
- <span data-ttu-id="6a0c0-125">**Framework 类型。**</span><span class="sxs-lookup"><span data-stu-id="6a0c0-125">**Framework Type.**</span></span> <span data-ttu-id="6a0c0-126">.NET Framework 中的对应类型是 <xref:System.Single?displayProperty=nameWithType> 结构。</span><span class="sxs-lookup"><span data-stu-id="6a0c0-126">The corresponding type in the .NET Framework is the <xref:System.Single?displayProperty=nameWithType> structure.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6a0c0-127">请参阅</span><span class="sxs-lookup"><span data-stu-id="6a0c0-127">See also</span></span>

- <xref:System.Single?displayProperty=nameWithType>
- [<span data-ttu-id="6a0c0-128">数据类型</span><span class="sxs-lookup"><span data-stu-id="6a0c0-128">Data Types</span></span>](index.md)
- [<span data-ttu-id="6a0c0-129">Decimal 数据类型</span><span class="sxs-lookup"><span data-stu-id="6a0c0-129">Decimal Data Type</span></span>](decimal-data-type.md)
- [<span data-ttu-id="6a0c0-130">Double 数据类型</span><span class="sxs-lookup"><span data-stu-id="6a0c0-130">Double Data Type</span></span>](double-data-type.md)
- [<span data-ttu-id="6a0c0-131">Type Conversion Functions</span><span class="sxs-lookup"><span data-stu-id="6a0c0-131">Type Conversion Functions</span></span>](../functions/type-conversion-functions.md)
- [<span data-ttu-id="6a0c0-132">转换摘要</span><span class="sxs-lookup"><span data-stu-id="6a0c0-132">Conversion Summary</span></span>](../keywords/conversion-summary.md)
- [<span data-ttu-id="6a0c0-133">有效使用数据类型</span><span class="sxs-lookup"><span data-stu-id="6a0c0-133">Efficient Use of Data Types</span></span>](../../programming-guide/language-features/data-types/efficient-use-of-data-types.md)
- [<span data-ttu-id="6a0c0-134">数据类型疑难解答</span><span class="sxs-lookup"><span data-stu-id="6a0c0-134">Troubleshooting Data Types</span></span>](../../programming-guide/language-features/data-types/troubleshooting-data-types.md)
