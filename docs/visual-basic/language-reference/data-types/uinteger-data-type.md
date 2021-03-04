---
description: 了解详细信息： UInteger 数据类型
title: UInteger 数据类型
ms.date: 01/31/2018
f1_keywords:
- vb.uinteger
helpviewer_keywords:
- numbers [Visual Basic], whole
- UInteger data type
- literal type characters [Visual Basic], UI
- whole numbers
- integral data types [Visual Basic]
- integer numbers
- numbers [Visual Basic], integer
- integers [Visual Basic], data types
- integers [Visual Basic], types
- UI literal type characters [Visual Basic]
- data types [Visual Basic], integral
ms.assetid: db7ddd34-4f23-46f5-84dd-8b0f83bb8729
ms.openlocfilehash: c3c04f746f0e2cf15bc1881544b93a538dbdc04e
ms.sourcegitcommit: 42d436ebc2a7ee02fc1848c7742bc7d80e13fc2f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/04/2021
ms.locfileid: "102104830"
---
# <a name="uinteger-data-type"></a><span data-ttu-id="1463c-103">UInteger 数据类型</span><span class="sxs-lookup"><span data-stu-id="1463c-103">UInteger data type</span></span>

<span data-ttu-id="1463c-104">保存32位无符号 (4 字节) 整数，范围介于0到4294967295之间。</span><span class="sxs-lookup"><span data-stu-id="1463c-104">Holds unsigned 32-bit (4-byte) integers ranging in value from 0 through 4,294,967,295.</span></span>

## <a name="remarks"></a><span data-ttu-id="1463c-105">备注</span><span class="sxs-lookup"><span data-stu-id="1463c-105">Remarks</span></span>

<span data-ttu-id="1463c-106">`UInteger`数据类型以最有效的数据宽度提供最大的无符号值。</span><span class="sxs-lookup"><span data-stu-id="1463c-106">The `UInteger` data type provides the largest unsigned value in the most efficient data width.</span></span>

<span data-ttu-id="1463c-107">`UInteger` 的默认值为 0。</span><span class="sxs-lookup"><span data-stu-id="1463c-107">The default value of `UInteger` is 0.</span></span>

## <a name="literal-assignments"></a><span data-ttu-id="1463c-108">文本赋值</span><span class="sxs-lookup"><span data-stu-id="1463c-108">Literal assignments</span></span>

<span data-ttu-id="1463c-109">可以声明和初始化 `UInteger` 变量，方法是向其分配十进制文本、十六进制文本、八进制文本，或者从 Visual Basic 2017) 二进制文本开始 (。</span><span class="sxs-lookup"><span data-stu-id="1463c-109">You can declare and initialize a `UInteger` variable by assigning it a decimal literal, a hexadecimal literal, an octal literal, or (starting with Visual Basic 2017) a binary literal.</span></span> <span data-ttu-id="1463c-110">如果整数文本在 `UInteger` 范围之外（即，如果它小于 <xref:System.UInt32.MinValue?displayProperty=nameWithType> 或大于 <xref:System.UInt32.MaxValue?displayProperty=nameWithType>），会发生编译错误。</span><span class="sxs-lookup"><span data-stu-id="1463c-110">If the integer literal is outside the range of `UInteger` (that is, if it is less than <xref:System.UInt32.MinValue?displayProperty=nameWithType> or greater than <xref:System.UInt32.MaxValue?displayProperty=nameWithType>, a compilation error occurs.</span></span>

<span data-ttu-id="1463c-111">在以下示例中，表示为十进制、十六进制和二进制文本且等于 3,000,000,000 的整数被分配给 `UInteger` 值。</span><span class="sxs-lookup"><span data-stu-id="1463c-111">In the following example, integers equal to 3,000,000,000 that are represented as decimal, hexadecimal, and binary literals are assigned to `UInteger` values.</span></span>

[!code-vb[UInteger](../../../../samples/snippets/visualbasic/language-reference/data-types/numeric-literals.vb#UInt)]

> [!NOTE]
> <span data-ttu-id="1463c-112">使用前缀 `&h` 或 `&H` 表示十六进制文本，使用前缀 `&b` 或表示 `&B` 二进制文本，使用前缀 `&o` 或 `&O` 表示八进制文本。</span><span class="sxs-lookup"><span data-stu-id="1463c-112">You use the prefix `&h` or `&H` to denote a hexadecimal literal, the prefix `&b` or `&B` to denote a binary literal, and the prefix `&o` or `&O` to denote an octal literal.</span></span> <span data-ttu-id="1463c-113">十进制文本没有前缀。</span><span class="sxs-lookup"><span data-stu-id="1463c-113">Decimal literals have no prefix.</span></span>

<span data-ttu-id="1463c-114">从 Visual Basic 2017 开始，还可以使用下划线字符 `_` 作为数字分隔符来增强可读性，如下面的示例所示。</span><span class="sxs-lookup"><span data-stu-id="1463c-114">Starting with Visual Basic 2017, you can also use the underscore character, `_`, as a digit separator to enhance readability, as the following example shows.</span></span>

[!code-vb[UInteger](../../../../samples/snippets/visualbasic/language-reference/data-types/numeric-literals.vb#UIntS)]

<span data-ttu-id="1463c-115">从 Visual Basic 15.5 开始，还可以使用下划线字符 (`_`) 作为前缀和十六进制、二进制或八进制数字之间的前导分隔符。</span><span class="sxs-lookup"><span data-stu-id="1463c-115">Starting with Visual Basic 15.5, you can also use the underscore character (`_`) as a leading separator between the prefix and the hexadecimal, binary, or octal digits.</span></span> <span data-ttu-id="1463c-116">例如：</span><span class="sxs-lookup"><span data-stu-id="1463c-116">For example:</span></span>

```vb
Dim number As UInteger = &H_0F8C_0326
```

[!INCLUDE [supporting-underscores](../../../../includes/vb-separator-langversion.md)]

<span data-ttu-id="1463c-117">数字文本还可以包含 `UI` 或 `ui` [类型字符](../../programming-guide/language-features/data-types/type-characters.md) 来表示 `UInteger` 数据类型，如下面的示例所示。</span><span class="sxs-lookup"><span data-stu-id="1463c-117">Numeric literals can also include the `UI` or `ui` [type character](../../programming-guide/language-features/data-types/type-characters.md) to denote the `UInteger` data type, as the following example shows.</span></span>

```vb
Dim number = &H_0FAC_14D7ui
```

## <a name="programming-tips"></a><span data-ttu-id="1463c-118">编程提示</span><span class="sxs-lookup"><span data-stu-id="1463c-118">Programming tips</span></span>

<span data-ttu-id="1463c-119">`UInteger`和 `Integer` 数据类型在32位处理器上提供最佳性能，因为较小的整数类型 (`UShort` 、 `Short` 、 `Byte` 和 `SByte`) ，即使它们使用较少的位，也需要更多的时间来加载、存储和提取。</span><span class="sxs-lookup"><span data-stu-id="1463c-119">The `UInteger` and `Integer` data types provide optimal performance on a 32-bit processor, because the smaller integer types (`UShort`, `Short`, `Byte`, and `SByte`), even though they use fewer bits, take more time to load, store, and fetch.</span></span>

- <span data-ttu-id="1463c-120">**负数。**</span><span class="sxs-lookup"><span data-stu-id="1463c-120">**Negative Numbers.**</span></span> <span data-ttu-id="1463c-121">由于 `UInteger` 是一个无符号类型，因此它不能表示负数。</span><span class="sxs-lookup"><span data-stu-id="1463c-121">Because `UInteger` is an unsigned type, it cannot represent a negative number.</span></span> <span data-ttu-id="1463c-122">如果 `-` 对计算结果为类型的表达式使用一元减号 () 运算符 `UInteger` ，Visual Basic 会将表达式转换为 `Long` 第一个表达式。</span><span class="sxs-lookup"><span data-stu-id="1463c-122">If you use the unary minus (`-`) operator on an expression that evaluates to type `UInteger`, Visual Basic converts the expression to `Long` first.</span></span>

- <span data-ttu-id="1463c-123">**CLS 遵从性。**</span><span class="sxs-lookup"><span data-stu-id="1463c-123">**CLS Compliance.**</span></span> <span data-ttu-id="1463c-124">`UInteger`数据类型不是[公共语言规范](https://www.ecma-international.org/publications-and-standards/standards/ecma-335/) (CLS) 的一部分，因此符合 cls 的代码不能使用使用它的组件。</span><span class="sxs-lookup"><span data-stu-id="1463c-124">The `UInteger` data type is not part of the [Common Language Specification](https://www.ecma-international.org/publications-and-standards/standards/ecma-335/) (CLS), so CLS-compliant code cannot consume a component that uses it.</span></span>

- <span data-ttu-id="1463c-125">**互操作注意事项。**</span><span class="sxs-lookup"><span data-stu-id="1463c-125">**Interop Considerations.**</span></span> <span data-ttu-id="1463c-126">如果你与不是为 .NET Framework 编写的组件（如自动化或 COM 对象）进行交互，请记住，如这样的类型 `uint` 可以在其他环境中具有不同的数据宽度 (16 位) 。</span><span class="sxs-lookup"><span data-stu-id="1463c-126">If you are interfacing with components not written for the .NET Framework, for example Automation or COM objects, keep in mind that types such as `uint` can have a different data width (16 bits) in other environments.</span></span> <span data-ttu-id="1463c-127">如果要将16位参数传递给此类组件，请 `UShort` `UInteger` 在托管的 Visual Basic 代码中将其声明为而不是。</span><span class="sxs-lookup"><span data-stu-id="1463c-127">If you are passing a 16-bit argument to such a component, declare it as `UShort` instead of `UInteger` in your managed Visual Basic code.</span></span>

- <span data-ttu-id="1463c-128">**扩大.**</span><span class="sxs-lookup"><span data-stu-id="1463c-128">**Widening.**</span></span> <span data-ttu-id="1463c-129">`UInteger`数据类型扩大到、、、 `Long` `ULong` `Decimal` `Single` 和 `Double` 。</span><span class="sxs-lookup"><span data-stu-id="1463c-129">The `UInteger` data type widens to `Long`, `ULong`, `Decimal`, `Single`, and `Double`.</span></span> <span data-ttu-id="1463c-130">这意味着你可以转换 `UInteger` 为这些类型中的任何一种，而不会遇到 <xref:System.OverflowException?displayProperty=nameWithType> 错误。</span><span class="sxs-lookup"><span data-stu-id="1463c-130">This means you can convert `UInteger` to any of these types without encountering a <xref:System.OverflowException?displayProperty=nameWithType> error.</span></span>

- <span data-ttu-id="1463c-131">**键入字符。**</span><span class="sxs-lookup"><span data-stu-id="1463c-131">**Type Characters.**</span></span> <span data-ttu-id="1463c-132">将文本类型字符追加 `UI` 到文本会将其强制转换为 `UInteger` 数据类型。</span><span class="sxs-lookup"><span data-stu-id="1463c-132">Appending the literal type characters `UI` to a literal forces it to the `UInteger` data type.</span></span> <span data-ttu-id="1463c-133">`UInteger` 没有标识符类型字符。</span><span class="sxs-lookup"><span data-stu-id="1463c-133">`UInteger` has no identifier type character.</span></span>

- <span data-ttu-id="1463c-134">**Framework 类型。**</span><span class="sxs-lookup"><span data-stu-id="1463c-134">**Framework Type.**</span></span> <span data-ttu-id="1463c-135">.NET Framework 中的对应类型是 <xref:System.UInt32?displayProperty=nameWithType> 结构。</span><span class="sxs-lookup"><span data-stu-id="1463c-135">The corresponding type in the .NET Framework is the <xref:System.UInt32?displayProperty=nameWithType> structure.</span></span>

## <a name="see-also"></a><span data-ttu-id="1463c-136">另请参阅</span><span class="sxs-lookup"><span data-stu-id="1463c-136">See also</span></span>

- <xref:System.UInt32>
- [<span data-ttu-id="1463c-137">数据类型</span><span class="sxs-lookup"><span data-stu-id="1463c-137">Data Types</span></span>](index.md)
- [<span data-ttu-id="1463c-138">Type Conversion Functions</span><span class="sxs-lookup"><span data-stu-id="1463c-138">Type Conversion Functions</span></span>](../functions/type-conversion-functions.md)
- [<span data-ttu-id="1463c-139">转换摘要</span><span class="sxs-lookup"><span data-stu-id="1463c-139">Conversion Summary</span></span>](../keywords/conversion-summary.md)
- [<span data-ttu-id="1463c-140">如何：调用需要使用无符号类型的 Windows 函数</span><span class="sxs-lookup"><span data-stu-id="1463c-140">How to: Call a Windows Function that Takes Unsigned Types</span></span>](../../programming-guide/com-interop/how-to-call-a-windows-function-that-takes-unsigned-types.md)
- [<span data-ttu-id="1463c-141">有效使用数据类型</span><span class="sxs-lookup"><span data-stu-id="1463c-141">Efficient Use of Data Types</span></span>](../../programming-guide/language-features/data-types/efficient-use-of-data-types.md)
