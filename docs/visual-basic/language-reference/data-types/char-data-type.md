---
description: '详细了解： Char 数据类型 (Visual Basic) '
title: Char 数据类型
ms.date: 07/20/2015
f1_keywords:
- vb.Char
helpviewer_keywords:
- literal type characters [Visual Basic], C
- Char data type
- C literal type character [Visual Basic]
- data types [Visual Basic], assigning
- Char data type [Visual Basic], character literals
ms.assetid: cd7547a9-7855-4e8e-b216-35d74a362657
ms.openlocfilehash: 371244ee4eae6d7dde20487dd7f38c09f3929cd8
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99792240"
---
# <a name="char-data-type-visual-basic"></a><span data-ttu-id="10559-103">Char 数据类型 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="10559-103">Char Data Type (Visual Basic)</span></span>

<span data-ttu-id="10559-104">保存16位无符号 (2 字节) 码位，范围介于0到65535之间。</span><span class="sxs-lookup"><span data-stu-id="10559-104">Holds unsigned 16-bit (2-byte) code points ranging in value from 0 through 65535.</span></span> <span data-ttu-id="10559-105">每个 *码位* 或字符代码都表示一个 Unicode 字符。</span><span class="sxs-lookup"><span data-stu-id="10559-105">Each *code point*, or character code, represents a single Unicode character.</span></span>

## <a name="remarks"></a><span data-ttu-id="10559-106">备注</span><span class="sxs-lookup"><span data-stu-id="10559-106">Remarks</span></span>

<span data-ttu-id="10559-107">`Char`当需要仅保存单个字符且无需开销时，请使用数据类型 `String` 。</span><span class="sxs-lookup"><span data-stu-id="10559-107">Use the `Char` data type when you need to hold only a single character and do not need the overhead of `String`.</span></span> <span data-ttu-id="10559-108">在某些情况下，可以使用 `Char()` （元素数组 `Char` ）保存多个字符。</span><span class="sxs-lookup"><span data-stu-id="10559-108">In some cases you can use `Char()`, an array of `Char` elements, to hold multiple characters.</span></span>

<span data-ttu-id="10559-109">的默认值 `Char` 为码位为0的字符。</span><span class="sxs-lookup"><span data-stu-id="10559-109">The default value of `Char` is the character with a code point of 0.</span></span>

## <a name="unicode-characters"></a><span data-ttu-id="10559-110">Unicode 字符</span><span class="sxs-lookup"><span data-stu-id="10559-110">Unicode Characters</span></span>

<span data-ttu-id="10559-111">第一个128码位 (0 – 127) Unicode 对应于标准美式键盘上的字母和符号。</span><span class="sxs-lookup"><span data-stu-id="10559-111">The first 128 code points (0–127) of Unicode correspond to the letters and symbols on a standard U.S. keyboard.</span></span> <span data-ttu-id="10559-112">这前128码位与 ASCII 字符集定义的代码点相同。</span><span class="sxs-lookup"><span data-stu-id="10559-112">These first 128 code points are the same as those the ASCII character set defines.</span></span> <span data-ttu-id="10559-113">第二个128码位 (128 – 255) 表示特殊字符，例如基于拉丁语的字母表号、重音、货币符号和分数。</span><span class="sxs-lookup"><span data-stu-id="10559-113">The second 128 code points (128–255) represent special characters, such as Latin-based alphabet letters, accents, currency symbols, and fractions.</span></span> <span data-ttu-id="10559-114">Unicode 为各种符号（包括全球文本字符、音调符号和数学符号和技术符号） (256-65535) 使用剩余的码位。</span><span class="sxs-lookup"><span data-stu-id="10559-114">Unicode uses the remaining code points (256-65535) for a wide variety of symbols, including worldwide textual characters, diacritics, and mathematical and technical symbols.</span></span>

<span data-ttu-id="10559-115">您可以对变量使用 <xref:System.Char.IsDigit%2A> 和等方法 <xref:System.Char.IsPunctuation%2A> `Char` 来确定其 Unicode 分类。</span><span class="sxs-lookup"><span data-stu-id="10559-115">You can use methods like <xref:System.Char.IsDigit%2A> and <xref:System.Char.IsPunctuation%2A> on a `Char` variable to determine its Unicode classification.</span></span>

## <a name="type-conversions"></a><span data-ttu-id="10559-116">类型转换</span><span class="sxs-lookup"><span data-stu-id="10559-116">Type Conversions</span></span>

<span data-ttu-id="10559-117">Visual Basic 不会直接在 `Char` 和数值类型之间转换。</span><span class="sxs-lookup"><span data-stu-id="10559-117">Visual Basic does not convert directly between `Char` and the numeric types.</span></span> <span data-ttu-id="10559-118">您可以使用 <xref:Microsoft.VisualBasic.Strings.Asc%2A> 或 <xref:Microsoft.VisualBasic.Strings.AscW%2A> 函数将 `Char` 值转换为 `Integer` 表示其码位的。</span><span class="sxs-lookup"><span data-stu-id="10559-118">You can use the <xref:Microsoft.VisualBasic.Strings.Asc%2A> or <xref:Microsoft.VisualBasic.Strings.AscW%2A> function to convert a `Char` value to an `Integer` that represents its code point.</span></span> <span data-ttu-id="10559-119">您可以使用 <xref:Microsoft.VisualBasic.Strings.Chr%2A> 或 <xref:Microsoft.VisualBasic.Strings.ChrW%2A> 函数将 `Integer` 值转换为 `Char` 具有该码位的。</span><span class="sxs-lookup"><span data-stu-id="10559-119">You can use the <xref:Microsoft.VisualBasic.Strings.Chr%2A> or <xref:Microsoft.VisualBasic.Strings.ChrW%2A> function to convert an `Integer` value to a `Char` that has that code point.</span></span>

<span data-ttu-id="10559-120">如果类型检查开关 ([选项 Strict 语句](../statements/option-strict-statement.md)) 为 on，则必须将文本类型字符追加到单字符字符串，以将其标识为 `Char` 数据类型。</span><span class="sxs-lookup"><span data-stu-id="10559-120">If the type checking switch (the [Option Strict Statement](../statements/option-strict-statement.md)) is on, you must append the literal type character to a single-character string literal to identify it as the `Char` data type.</span></span> <span data-ttu-id="10559-121">下面的示例阐释了这一点。</span><span class="sxs-lookup"><span data-stu-id="10559-121">The following example illustrates this.</span></span> <span data-ttu-id="10559-122">对变量的第一次赋值将 `charVar` 生成编译器错误 [BC30512](../../misc/bc30512.md) ，因为 `Option Strict` 处于打开。</span><span class="sxs-lookup"><span data-stu-id="10559-122">The first assignment to the `charVar` variable generates compiler error [BC30512](../../misc/bc30512.md) because `Option Strict` is on.</span></span> <span data-ttu-id="10559-123">第二个编译成功，因为 `c` 文本类型字符将文本标识为 `Char` 值。</span><span class="sxs-lookup"><span data-stu-id="10559-123">The second compiles successfully because the `c` literal type character identifies the literal as a `Char` value.</span></span>

```vb
Option Strict On

Module CharType
    Public Sub Main()
        Dim charVar As Char

        ' This statement generates compiler error BC30512 because Option Strict is On.  
        charVar = "Z"  

        ' The following statement succeeds because it specifies a Char literal.  
        charVar = "Z"c
    End Sub
End Module
```

## <a name="programming-tips"></a><span data-ttu-id="10559-124">编程提示</span><span class="sxs-lookup"><span data-stu-id="10559-124">Programming Tips</span></span>

- <span data-ttu-id="10559-125">**负数。**</span><span class="sxs-lookup"><span data-stu-id="10559-125">**Negative Numbers.**</span></span> <span data-ttu-id="10559-126">`Char` 是无符号类型，不能表示负值。</span><span class="sxs-lookup"><span data-stu-id="10559-126">`Char` is an unsigned type and cannot represent a negative value.</span></span> <span data-ttu-id="10559-127">在任何情况下，不应使用 `Char` 来保存数值。</span><span class="sxs-lookup"><span data-stu-id="10559-127">In any case, you should not use `Char` to hold numeric values.</span></span>

- <span data-ttu-id="10559-128">**互操作注意事项。**</span><span class="sxs-lookup"><span data-stu-id="10559-128">**Interop Considerations.**</span></span> <span data-ttu-id="10559-129">如果你使用不是为 .NET Framework 编写的组件（如自动化或 COM 对象）进行交互，请记住，在其他环境中，字符类型具有不同于 8) 位 (的数据宽度。</span><span class="sxs-lookup"><span data-stu-id="10559-129">If you interface with components not written for the .NET Framework, for example Automation or COM objects, remember that character types have a different data width (8 bits) in other environments.</span></span> <span data-ttu-id="10559-130">如果将一个8位参数传递给此类组件，请 `Byte` `Char` 在新的 Visual Basic 代码中将其声明为而不是。</span><span class="sxs-lookup"><span data-stu-id="10559-130">If you pass an 8-bit argument to such a component, declare it as `Byte` instead of `Char` in your new Visual Basic code.</span></span>

- <span data-ttu-id="10559-131">**扩大.**</span><span class="sxs-lookup"><span data-stu-id="10559-131">**Widening.**</span></span> <span data-ttu-id="10559-132">`Char`数据类型扩大到 `String` 。</span><span class="sxs-lookup"><span data-stu-id="10559-132">The `Char` data type widens to `String`.</span></span> <span data-ttu-id="10559-133">这意味着你可以将转换 `Char` 为 `String` ，而不会遇到 <xref:System.OverflowException?displayProperty=nameWithType> 。</span><span class="sxs-lookup"><span data-stu-id="10559-133">This means you can convert `Char` to `String` and will not encounter a <xref:System.OverflowException?displayProperty=nameWithType>.</span></span>

- <span data-ttu-id="10559-134">**键入字符。**</span><span class="sxs-lookup"><span data-stu-id="10559-134">**Type Characters.**</span></span> <span data-ttu-id="10559-135">将文本类型字符追加 `C` 到单字符字符串文本会将其强制转换为 `Char` 数据类型。</span><span class="sxs-lookup"><span data-stu-id="10559-135">Appending the literal type character `C` to a single-character string literal forces it to the `Char` data type.</span></span> <span data-ttu-id="10559-136">`Char` 没有标识符类型字符。</span><span class="sxs-lookup"><span data-stu-id="10559-136">`Char` has no identifier type character.</span></span>

- <span data-ttu-id="10559-137">**Framework 类型。**</span><span class="sxs-lookup"><span data-stu-id="10559-137">**Framework Type.**</span></span> <span data-ttu-id="10559-138">.NET Framework 中的对应类型是 <xref:System.Char?displayProperty=nameWithType> 结构。</span><span class="sxs-lookup"><span data-stu-id="10559-138">The corresponding type in the .NET Framework is the <xref:System.Char?displayProperty=nameWithType> structure.</span></span>

## <a name="see-also"></a><span data-ttu-id="10559-139">请参阅</span><span class="sxs-lookup"><span data-stu-id="10559-139">See also</span></span>

- <xref:System.Char?displayProperty=nameWithType>
- <xref:Microsoft.VisualBasic.Strings.Asc%2A>
- <xref:Microsoft.VisualBasic.Strings.AscW%2A>
- <xref:Microsoft.VisualBasic.Strings.Chr%2A>
- <xref:Microsoft.VisualBasic.Strings.ChrW%2A>
- [<span data-ttu-id="10559-140">数据类型</span><span class="sxs-lookup"><span data-stu-id="10559-140">Data Types</span></span>](index.md)
- [<span data-ttu-id="10559-141">String 数据类型</span><span class="sxs-lookup"><span data-stu-id="10559-141">String Data Type</span></span>](string-data-type.md)
- [<span data-ttu-id="10559-142">Type Conversion Functions</span><span class="sxs-lookup"><span data-stu-id="10559-142">Type Conversion Functions</span></span>](../functions/type-conversion-functions.md)
- [<span data-ttu-id="10559-143">转换摘要</span><span class="sxs-lookup"><span data-stu-id="10559-143">Conversion Summary</span></span>](../keywords/conversion-summary.md)
- [<span data-ttu-id="10559-144">如何：调用需要使用无符号类型的 Windows 函数</span><span class="sxs-lookup"><span data-stu-id="10559-144">How to: Call a Windows Function that Takes Unsigned Types</span></span>](../../programming-guide/com-interop/how-to-call-a-windows-function-that-takes-unsigned-types.md)
- [<span data-ttu-id="10559-145">有效使用数据类型</span><span class="sxs-lookup"><span data-stu-id="10559-145">Efficient Use of Data Types</span></span>](../../programming-guide/language-features/data-types/efficient-use-of-data-types.md)
