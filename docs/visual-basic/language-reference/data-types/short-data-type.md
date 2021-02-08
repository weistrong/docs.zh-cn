---
description: '了解详细信息： Short 数据类型 (Visual Basic) '
title: Short 数据类型
ms.date: 01/31/2018
f1_keywords:
- vb.Short
helpviewer_keywords:
- numbers [Visual Basic], whole
- whole numbers
- integral data types [Visual Basic]
- integer numbers
- numbers [Visual Basic], integer
- integers [Visual Basic], data types
- integers [Visual Basic], types
- data types [Visual Basic], integral
- S literal type character [Visual Basic]
- Short data type
- literal type characters [Visual Basic], S
ms.assetid: 65fcbcf3-a841-400e-885e-301497729a8b
ms.openlocfilehash: 8c6bee45355548b3a32d74d059159918b4009fbb
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99792136"
---
# <a name="short-data-type-visual-basic"></a><span data-ttu-id="1cbe7-103">Short 数据类型 (Visual Basic) </span><span class="sxs-lookup"><span data-stu-id="1cbe7-103">Short data type (Visual Basic)</span></span>

<span data-ttu-id="1cbe7-104">保存16位有符号 (2 字节) 整数，范围为-32768 到32767。</span><span class="sxs-lookup"><span data-stu-id="1cbe7-104">Holds signed 16-bit (2-byte) integers that range in value from -32,768 through 32,767.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="1cbe7-105">备注</span><span class="sxs-lookup"><span data-stu-id="1cbe7-105">Remarks</span></span>  

 <span data-ttu-id="1cbe7-106">使用 `Short` 数据类型可包含不需要完整数据宽度的整数值 `Integer` 。</span><span class="sxs-lookup"><span data-stu-id="1cbe7-106">Use the `Short` data type to contain integer values that do not require the full data width of `Integer`.</span></span> <span data-ttu-id="1cbe7-107">在某些情况下，公共语言运行时可以将 `Short` 变量紧密地打包在一起，并节省内存消耗。</span><span class="sxs-lookup"><span data-stu-id="1cbe7-107">In some cases, the common language runtime can pack your `Short` variables closely together and save memory consumption.</span></span>  
  
 <span data-ttu-id="1cbe7-108">`Short` 的默认值为 0。</span><span class="sxs-lookup"><span data-stu-id="1cbe7-108">The default value of `Short` is 0.</span></span>  
  
## <a name="literal-assignments"></a><span data-ttu-id="1cbe7-109">文本赋值</span><span class="sxs-lookup"><span data-stu-id="1cbe7-109">Literal assignments</span></span>

<span data-ttu-id="1cbe7-110">可以声明和初始化 `Short` 变量，方法是向其分配十进制文本、十六进制文本、八进制文本，或者从 Visual Basic 2017) 二进制文本开始 (。</span><span class="sxs-lookup"><span data-stu-id="1cbe7-110">You can declare and initialize a `Short` variable by assigning it a decimal literal, a hexadecimal literal, an octal literal, or (starting with Visual Basic 2017) a binary literal.</span></span> <span data-ttu-id="1cbe7-111">如果整数文本在 `Short` 范围之外（即，如果它小于 <xref:System.Int16.MinValue?displayProperty=nameWithType> 或大于 <xref:System.Int16.MaxValue?displayProperty=nameWithType>），会发生编译错误。</span><span class="sxs-lookup"><span data-stu-id="1cbe7-111">If the integer literal is outside the range of `Short` (that is, if it is less than <xref:System.Int16.MinValue?displayProperty=nameWithType> or greater than <xref:System.Int16.MaxValue?displayProperty=nameWithType>, a compilation error occurs.</span></span>

<span data-ttu-id="1cbe7-112">在下面的示例中，表示为十进制、十六进制和二进制文本的整数等于1034将从 [整数](integer-data-type.md) 隐式转换为 `Short` 值。</span><span class="sxs-lookup"><span data-stu-id="1cbe7-112">In the following example, integers equal to 1,034 that are represented as decimal, hexadecimal, and binary literals are implicitly converted from [Integer](integer-data-type.md) to `Short` values.</span></span>

[!code-vb[Short](../../../../samples/snippets/visualbasic/language-reference/data-types/numeric-literals.vb#Short)]

> [!NOTE]
> <span data-ttu-id="1cbe7-113">使用前缀 `&h` 或 `&H` 表示十六进制文本，使用前缀 `&b` 或表示 `&B` 二进制文本，使用前缀 `&o` 或 `&O` 表示八进制文本。</span><span class="sxs-lookup"><span data-stu-id="1cbe7-113">You use the prefix `&h` or `&H` to denote a hexadecimal literal, the prefix `&b` or `&B` to denote a binary literal, and the prefix `&o` or `&O` to denote an octal literal.</span></span> <span data-ttu-id="1cbe7-114">十进制文本没有前缀。</span><span class="sxs-lookup"><span data-stu-id="1cbe7-114">Decimal literals have no prefix.</span></span>

<span data-ttu-id="1cbe7-115">从 Visual Basic 2017 开始，还可以使用下划线字符 `_` 作为数字分隔符来增强可读性，如下面的示例所示。</span><span class="sxs-lookup"><span data-stu-id="1cbe7-115">Starting with Visual Basic 2017, you can also use the underscore character, `_`, as a digit separator to enhance readability, as the following example shows.</span></span>

[!code-vb[Short](../../../../samples/snippets/visualbasic/language-reference/data-types/numeric-literals.vb#ShortS)]

<span data-ttu-id="1cbe7-116">从 Visual Basic 15.5 开始，还可以使用下划线字符 (`_`) 作为前缀和十六进制、二进制或八进制数字之间的前导分隔符。</span><span class="sxs-lookup"><span data-stu-id="1cbe7-116">Starting with Visual Basic 15.5, you can also use the underscore character (`_`) as a leading separator between the prefix and the hexadecimal, binary, or octal digits.</span></span> <span data-ttu-id="1cbe7-117">例如：</span><span class="sxs-lookup"><span data-stu-id="1cbe7-117">For example:</span></span>

```vb
Dim number As Short = &H_3264
```

[!INCLUDE [supporting-underscores](../../../../includes/vb-separator-langversion.md)]

<span data-ttu-id="1cbe7-118">数字文本还可包含 `S` 用于表示数据类型的 [类型字符](../../programming-guide/language-features/data-types/type-characters.md) `Short` ，如下面的示例所示。</span><span class="sxs-lookup"><span data-stu-id="1cbe7-118">Numeric literals can also include the `S` [type character](../../programming-guide/language-features/data-types/type-characters.md) to denote the `Short` data type, as the following example shows.</span></span>

```vb
Dim number = &H_3264S
```

## <a name="programming-tips"></a><span data-ttu-id="1cbe7-119">编程提示</span><span class="sxs-lookup"><span data-stu-id="1cbe7-119">Programming tips</span></span>

- <span data-ttu-id="1cbe7-120">**扩大.**</span><span class="sxs-lookup"><span data-stu-id="1cbe7-120">**Widening.**</span></span> <span data-ttu-id="1cbe7-121">`Short`数据类型扩大到、、、 `Integer` `Long` `Decimal` `Single` 或 `Double` 。</span><span class="sxs-lookup"><span data-stu-id="1cbe7-121">The `Short` data type widens to `Integer`, `Long`, `Decimal`, `Single`, or `Double`.</span></span> <span data-ttu-id="1cbe7-122">这意味着，你可以将 `Short` 转换为这些类型中的任意类型，而不会遇到 <xref:System.OverflowException?displayProperty=nameWithType> 错误。</span><span class="sxs-lookup"><span data-stu-id="1cbe7-122">This means you can convert `Short` to any one of these types without encountering a <xref:System.OverflowException?displayProperty=nameWithType> error.</span></span>  
  
- <span data-ttu-id="1cbe7-123">**键入字符。**</span><span class="sxs-lookup"><span data-stu-id="1cbe7-123">**Type Characters.**</span></span> <span data-ttu-id="1cbe7-124">将文本类型字符 `S` 追加到文本会将其强制转换为 `Short` 数据类型。</span><span class="sxs-lookup"><span data-stu-id="1cbe7-124">Appending the literal type character `S` to a literal forces it to the `Short` data type.</span></span> <span data-ttu-id="1cbe7-125">`Short` 没有标识符类型字符。</span><span class="sxs-lookup"><span data-stu-id="1cbe7-125">`Short` has no identifier type character.</span></span>  
  
- <span data-ttu-id="1cbe7-126">**Framework 类型。**</span><span class="sxs-lookup"><span data-stu-id="1cbe7-126">**Framework Type.**</span></span> <span data-ttu-id="1cbe7-127">.NET Framework 中的对应类型是 <xref:System.Int16?displayProperty=nameWithType> 结构。</span><span class="sxs-lookup"><span data-stu-id="1cbe7-127">The corresponding type in the .NET Framework is the <xref:System.Int16?displayProperty=nameWithType> structure.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1cbe7-128">请参阅</span><span class="sxs-lookup"><span data-stu-id="1cbe7-128">See also</span></span>

- <xref:System.Int16?displayProperty=nameWithType>
- [<span data-ttu-id="1cbe7-129">数据类型</span><span class="sxs-lookup"><span data-stu-id="1cbe7-129">Data Types</span></span>](index.md)
- [<span data-ttu-id="1cbe7-130">Type Conversion Functions</span><span class="sxs-lookup"><span data-stu-id="1cbe7-130">Type Conversion Functions</span></span>](../functions/type-conversion-functions.md)
- [<span data-ttu-id="1cbe7-131">转换摘要</span><span class="sxs-lookup"><span data-stu-id="1cbe7-131">Conversion Summary</span></span>](../keywords/conversion-summary.md)
- [<span data-ttu-id="1cbe7-132">Integer 数据类型</span><span class="sxs-lookup"><span data-stu-id="1cbe7-132">Integer Data Type</span></span>](integer-data-type.md)
- [<span data-ttu-id="1cbe7-133">Long 数据类型</span><span class="sxs-lookup"><span data-stu-id="1cbe7-133">Long Data Type</span></span>](long-data-type.md)
- [<span data-ttu-id="1cbe7-134">有效使用数据类型</span><span class="sxs-lookup"><span data-stu-id="1cbe7-134">Efficient Use of Data Types</span></span>](../../programming-guide/language-features/data-types/efficient-use-of-data-types.md)
