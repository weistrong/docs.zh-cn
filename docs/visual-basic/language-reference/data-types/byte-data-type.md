---
description: '了解详细信息： Byte 数据类型 (Visual Basic) '
title: Byte 数据类型
ms.date: 01/31/2018
f1_keywords:
- vb.Byte
helpviewer_keywords:
- Byte data type
- data types [Visual Basic], assigning
ms.assetid: eed44dff-eaee-4937-a89f-444e418e74f6
ms.openlocfilehash: 983af36d8340b5df7ac44782bf56349901460c20
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99731222"
---
# <a name="byte-data-type-visual-basic"></a><span data-ttu-id="b21e1-103">Byte 数据类型 (Visual Basic) </span><span class="sxs-lookup"><span data-stu-id="b21e1-103">Byte data type (Visual Basic)</span></span>

<span data-ttu-id="b21e1-104">将无符号的8位 (1 字节) 整数，范围介于0到255之间。</span><span class="sxs-lookup"><span data-stu-id="b21e1-104">Holds unsigned 8-bit (1-byte) integers that range in value from 0 through 255.</span></span>

## <a name="remarks"></a><span data-ttu-id="b21e1-105">备注</span><span class="sxs-lookup"><span data-stu-id="b21e1-105">Remarks</span></span>

<span data-ttu-id="b21e1-106">使用 `Byte` 数据类型来包含二进制数据。</span><span class="sxs-lookup"><span data-stu-id="b21e1-106">Use the `Byte` data type to contain binary data.</span></span>  
  
<span data-ttu-id="b21e1-107">`Byte` 的默认值为 0。</span><span class="sxs-lookup"><span data-stu-id="b21e1-107">The default value of `Byte` is 0.</span></span>

## <a name="literal-assignments"></a><span data-ttu-id="b21e1-108">文本赋值</span><span class="sxs-lookup"><span data-stu-id="b21e1-108">Literal assignments</span></span>

<span data-ttu-id="b21e1-109">可以声明和初始化 `Byte` 变量，方法是向其分配十进制文本、十六进制文本、八进制文本，或者从 Visual Basic 2017) 二进制文本开始 (。</span><span class="sxs-lookup"><span data-stu-id="b21e1-109">You can declare and initialize a `Byte` variable by assigning it a decimal literal, a hexadecimal literal, an octal literal, or (starting with Visual Basic 2017) a binary literal.</span></span> <span data-ttu-id="b21e1-110">如果整数文本超出 `Byte` (的范围（即，如果它小于 <xref:System.Byte.MinValue?displayProperty=nameWithType> 或大于 <xref:System.Byte.MaxValue?displayProperty=nameWithType>) ），则会发生编译错误。</span><span class="sxs-lookup"><span data-stu-id="b21e1-110">If the integral literal is outside the range of a `Byte` (that is, if it is less than <xref:System.Byte.MinValue?displayProperty=nameWithType> or greater than <xref:System.Byte.MaxValue?displayProperty=nameWithType>), a compilation error occurs.</span></span>

<span data-ttu-id="b21e1-111">在下面的示例中，表示为十进制、十六进制和二进制文本的整数等于201将从 [整数](integer-data-type.md) 隐式转换为 `byte` 值。</span><span class="sxs-lookup"><span data-stu-id="b21e1-111">In the following example, integers equal to 201 that are represented as decimal, hexadecimal, and binary literals are implicitly converted from [Integer](integer-data-type.md) to `byte` values.</span></span>

[!code-vb[Byte](../../../../samples/snippets/visualbasic/language-reference/data-types/numeric-literals.vb#Byte)]

> [!NOTE]
> <span data-ttu-id="b21e1-112">使用前缀 `&h` 或 `&H` 表示十六进制文本，使用前缀 `&b` 或表示 `&B` 二进制文本，使用前缀 `&o` 或 `&O` 表示八进制文本。</span><span class="sxs-lookup"><span data-stu-id="b21e1-112">You use the prefix `&h` or `&H` to denote a hexadecimal literal, the prefix `&b` or `&B` to denote a binary literal, and the prefix `&o` or `&O` to denote an octal literal.</span></span> <span data-ttu-id="b21e1-113">十进制文本没有前缀。</span><span class="sxs-lookup"><span data-stu-id="b21e1-113">Decimal literals have no prefix.</span></span>

<span data-ttu-id="b21e1-114">从 Visual Basic 2017 开始，还可以使用下划线字符 `_` 作为数字分隔符来增强可读性，如下面的示例所示。</span><span class="sxs-lookup"><span data-stu-id="b21e1-114">Starting with Visual Basic 2017, you can also use the underscore character, `_`, as a digit separator to enhance readability, as the following example shows.</span></span>

[!code-vb[Byte](../../../../samples/snippets/visualbasic/language-reference/data-types/numeric-literals.vb#ByteS)]  

<span data-ttu-id="b21e1-115">从 Visual Basic 15.5 开始，还可以使用下划线字符 (`_`) 作为前缀和十六进制、二进制或八进制数字之间的前导分隔符。</span><span class="sxs-lookup"><span data-stu-id="b21e1-115">Starting with Visual Basic 15.5, you can also use the underscore character (`_`) as a leading separator between the prefix and the hexadecimal, binary, or octal digits.</span></span> <span data-ttu-id="b21e1-116">例如：</span><span class="sxs-lookup"><span data-stu-id="b21e1-116">For example:</span></span>

```vb
Dim number As Byte = &H_6A
```

[!INCLUDE [supporting-underscores](../../../../includes/vb-separator-langversion.md)]

## <a name="programming-tips"></a><span data-ttu-id="b21e1-117">编程提示</span><span class="sxs-lookup"><span data-stu-id="b21e1-117">Programming tips</span></span>

- <span data-ttu-id="b21e1-118">**负数。**</span><span class="sxs-lookup"><span data-stu-id="b21e1-118">**Negative Numbers.**</span></span> <span data-ttu-id="b21e1-119">由于 `Byte` 是一个无符号类型，因此它不能表示负数。</span><span class="sxs-lookup"><span data-stu-id="b21e1-119">Because `Byte` is an unsigned type, it cannot represent a negative number.</span></span> <span data-ttu-id="b21e1-120">如果 `-` 对计算结果为类型的表达式使用一元减号 () 运算符 `Byte` ，Visual Basic 会将表达式转换为 `Short` 第一个表达式。</span><span class="sxs-lookup"><span data-stu-id="b21e1-120">If you use the unary minus (`-`) operator on an expression that evaluates to type `Byte`, Visual Basic converts the expression to `Short` first.</span></span>
  
- <span data-ttu-id="b21e1-121">**格式转换。**</span><span class="sxs-lookup"><span data-stu-id="b21e1-121">**Format Conversions.**</span></span> <span data-ttu-id="b21e1-122">当 Visual Basic 读取或写入文件，或者在调用 Dll、方法和属性时，它可以在数据格式之间自动转换。</span><span class="sxs-lookup"><span data-stu-id="b21e1-122">When Visual Basic reads or writes files, or when it calls DLLs, methods, and properties, it can automatically convert between data formats.</span></span> <span data-ttu-id="b21e1-123">在 `Byte` 此类格式转换过程中将保留存储在变量和数组中的二进制数据。</span><span class="sxs-lookup"><span data-stu-id="b21e1-123">Binary data stored in `Byte` variables and arrays is preserved during such format conversions.</span></span> <span data-ttu-id="b21e1-124">不应将 `String` 变量用于二进制数据，因为在 ANSI 和 Unicode 格式之间进行转换时，可能会损坏其内容。</span><span class="sxs-lookup"><span data-stu-id="b21e1-124">You should not use a `String` variable for binary data, because its contents can be corrupted during conversion between ANSI and Unicode formats.</span></span>

- <span data-ttu-id="b21e1-125">**扩大.**</span><span class="sxs-lookup"><span data-stu-id="b21e1-125">**Widening.**</span></span> <span data-ttu-id="b21e1-126">`Byte`数据类型扩大到、、、 `Short` `UShort` 、、、、 `Integer` `UInteger` `Long` `ULong` `Decimal` `Single` 或 `Double` 。</span><span class="sxs-lookup"><span data-stu-id="b21e1-126">The `Byte` data type widens to `Short`, `UShort`, `Integer`, `UInteger`, `Long`, `ULong`, `Decimal`, `Single`, or `Double`.</span></span> <span data-ttu-id="b21e1-127">这意味着你可以转换 `Byte` 为这些类型中的任何一种，而不会遇到 <xref:System.OverflowException?displayProperty=nameWithType> 错误。</span><span class="sxs-lookup"><span data-stu-id="b21e1-127">This means you can convert `Byte` to any of these types without encountering a <xref:System.OverflowException?displayProperty=nameWithType> error.</span></span>
  
- <span data-ttu-id="b21e1-128">**键入字符。**</span><span class="sxs-lookup"><span data-stu-id="b21e1-128">**Type Characters.**</span></span> <span data-ttu-id="b21e1-129">`Byte` 没有文本类型字符或标识符类型字符。</span><span class="sxs-lookup"><span data-stu-id="b21e1-129">`Byte` has no literal type character or identifier type character.</span></span>

- <span data-ttu-id="b21e1-130">**Framework 类型。**</span><span class="sxs-lookup"><span data-stu-id="b21e1-130">**Framework Type.**</span></span> <span data-ttu-id="b21e1-131">.NET Framework 中的对应类型是 <xref:System.Byte?displayProperty=nameWithType> 结构。</span><span class="sxs-lookup"><span data-stu-id="b21e1-131">The corresponding type in the .NET Framework is the <xref:System.Byte?displayProperty=nameWithType> structure.</span></span>

## <a name="example"></a><span data-ttu-id="b21e1-132">示例</span><span class="sxs-lookup"><span data-stu-id="b21e1-132">Example</span></span>

 <span data-ttu-id="b21e1-133">在下面的示例中， `b` 是一个 `Byte` 变量。</span><span class="sxs-lookup"><span data-stu-id="b21e1-133">In the following example, `b` is a `Byte` variable.</span></span> <span data-ttu-id="b21e1-134">语句说明变量的范围以及对其应用移位运算符的应用程序。</span><span class="sxs-lookup"><span data-stu-id="b21e1-134">The statements demonstrate the range of the variable and the application of bit-shift operators to it.</span></span>

 [!code-vb[VbVbalrDataTypes#16](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrDataTypes/VB/Class1.vb#16)]  

## <a name="see-also"></a><span data-ttu-id="b21e1-135">请参阅</span><span class="sxs-lookup"><span data-stu-id="b21e1-135">See also</span></span>

- <xref:System.Byte?displayProperty=nameWithType>
- [<span data-ttu-id="b21e1-136">数据类型</span><span class="sxs-lookup"><span data-stu-id="b21e1-136">Data Types</span></span>](index.md)
- [<span data-ttu-id="b21e1-137">Type Conversion Functions</span><span class="sxs-lookup"><span data-stu-id="b21e1-137">Type Conversion Functions</span></span>](../functions/type-conversion-functions.md)
- [<span data-ttu-id="b21e1-138">转换摘要</span><span class="sxs-lookup"><span data-stu-id="b21e1-138">Conversion Summary</span></span>](../keywords/conversion-summary.md)
- [<span data-ttu-id="b21e1-139">有效使用数据类型</span><span class="sxs-lookup"><span data-stu-id="b21e1-139">Efficient Use of Data Types</span></span>](../../programming-guide/language-features/data-types/efficient-use-of-data-types.md)
