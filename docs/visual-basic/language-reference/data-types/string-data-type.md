---
description: '了解详细信息：字符串数据类型 (Visual Basic) '
title: String 数据类型
ms.date: 07/20/2015
f1_keywords:
- vb.String
helpviewer_keywords:
- strings [Visual Basic], character
- strings [Visual Basic], fixed-length
- string keyword [Visual Basic]
- fixed-length strings [Visual Basic], string data type
- literals [Visual Basic], string
- text [Visual Basic], String data type
- $ identifier type character
- String data type
- fixed-length strings
- string literals [Visual Basic]
- data types [Visual Basic], assigning
- String literals [Visual Basic]
- identifier type characters [Visual Basic], $
ms.assetid: 15ac03f5-cabd-42cc-a754-1df3893c25d9
ms.openlocfilehash: 6597a5c4b8ee0eb961d3e33bee52ae493068da35
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99792110"
---
# <a name="string-data-type-visual-basic"></a><span data-ttu-id="fbe1d-103">String 数据类型 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="fbe1d-103">String Data Type (Visual Basic)</span></span>

<span data-ttu-id="fbe1d-104">保存16位无符号16位 (2 字节) 码位的序列，范围介于0到65535之间。</span><span class="sxs-lookup"><span data-stu-id="fbe1d-104">Holds sequences of unsigned 16-bit (2-byte) code points that range in value from 0 through 65535.</span></span> <span data-ttu-id="fbe1d-105">每个 *码位* 或字符代码都表示一个 Unicode 字符。</span><span class="sxs-lookup"><span data-stu-id="fbe1d-105">Each *code point*, or character code, represents a single Unicode character.</span></span> <span data-ttu-id="fbe1d-106">字符串可以包含0到约 2000000000 (2 ^ 31) Unicode 字符。</span><span class="sxs-lookup"><span data-stu-id="fbe1d-106">A string can contain from 0 to approximately two billion (2 ^ 31) Unicode characters.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="fbe1d-107">备注</span><span class="sxs-lookup"><span data-stu-id="fbe1d-107">Remarks</span></span>  

 <span data-ttu-id="fbe1d-108">使用 `String` 数据类型来存储多个字符，而无需数组管理开销 `Char()` ，即 `Char` 元素数组。</span><span class="sxs-lookup"><span data-stu-id="fbe1d-108">Use the `String` data type to hold multiple characters without the array management overhead of `Char()`, an array of `Char` elements.</span></span>  
  
 <span data-ttu-id="fbe1d-109">的默认值 `String` 为 `Nothing` (空引用) 。</span><span class="sxs-lookup"><span data-stu-id="fbe1d-109">The default value of `String` is `Nothing` (a null reference).</span></span> <span data-ttu-id="fbe1d-110">请注意，这不同于空字符串 (值 `""`) 。</span><span class="sxs-lookup"><span data-stu-id="fbe1d-110">Note that this is not the same as the empty string (value `""`).</span></span>  
  
## <a name="unicode-characters"></a><span data-ttu-id="fbe1d-111">Unicode 字符</span><span class="sxs-lookup"><span data-stu-id="fbe1d-111">Unicode Characters</span></span>  

 <span data-ttu-id="fbe1d-112">第一个128码位 (0 – 127) Unicode 对应于标准美式键盘上的字母和符号。</span><span class="sxs-lookup"><span data-stu-id="fbe1d-112">The first 128 code points (0–127) of Unicode correspond to the letters and symbols on a standard U.S. keyboard.</span></span> <span data-ttu-id="fbe1d-113">这前128码位与 ASCII 字符集定义的代码点相同。</span><span class="sxs-lookup"><span data-stu-id="fbe1d-113">These first 128 code points are the same as those the ASCII character set defines.</span></span> <span data-ttu-id="fbe1d-114">第二个128码位 (128 – 255) 表示特殊字符，例如基于拉丁语的字母表号、重音、货币符号和分数。</span><span class="sxs-lookup"><span data-stu-id="fbe1d-114">The second 128 code points (128–255) represent special characters, such as Latin-based alphabet letters, accents, currency symbols, and fractions.</span></span> <span data-ttu-id="fbe1d-115">Unicode 将 (256-65535) 的剩余代码点用于各种符号。</span><span class="sxs-lookup"><span data-stu-id="fbe1d-115">Unicode uses the remaining code points (256-65535) for a wide variety of symbols.</span></span> <span data-ttu-id="fbe1d-116">这包括全球文本字符、音调符号、数学和技术符号。</span><span class="sxs-lookup"><span data-stu-id="fbe1d-116">This includes worldwide textual characters, diacritics, and mathematical and technical symbols.</span></span>  
  
 <span data-ttu-id="fbe1d-117">可以在 <xref:System.Char.IsDigit%2A> <xref:System.Char.IsPunctuation%2A> 变量中的单个字符上使用和等方法 `String` 来确定其 Unicode 分类。</span><span class="sxs-lookup"><span data-stu-id="fbe1d-117">You can use methods such as <xref:System.Char.IsDigit%2A> and <xref:System.Char.IsPunctuation%2A> on an individual character in a `String` variable to determine its Unicode classification.</span></span>  
  
## <a name="format-requirements"></a><span data-ttu-id="fbe1d-118">格式要求</span><span class="sxs-lookup"><span data-stu-id="fbe1d-118">Format Requirements</span></span>  

 <span data-ttu-id="fbe1d-119">必须将文本括 `String` 在引号内 (`" "`) 。</span><span class="sxs-lookup"><span data-stu-id="fbe1d-119">You must enclose a `String` literal within quotation marks (`" "`).</span></span> <span data-ttu-id="fbe1d-120">如果必须包括引号作为字符串中的字符之一，请使用两个连续的引号 (`""`) 。</span><span class="sxs-lookup"><span data-stu-id="fbe1d-120">If you must include a quotation mark as one of the characters in the string, you use two contiguous quotation marks (`""`).</span></span> <span data-ttu-id="fbe1d-121">下面的示例阐释了这一点。</span><span class="sxs-lookup"><span data-stu-id="fbe1d-121">The following example illustrates this.</span></span>  
  
```vb  
Dim j As String = "Joe said ""Hello"" to me."  
Dim h As String = "Hello"  
' The following messages all display the same thing:  
' "Joe said "Hello" to me."  
MsgBox(j)  
MsgBox("Joe said " & """" & h & """" & " to me.")  
MsgBox("Joe said """ & h & """ to me.")  
```  
  
 <span data-ttu-id="fbe1d-122">请注意，表示字符串中的引号的连续引号与开始和结束文本的引号无关 `String` 。</span><span class="sxs-lookup"><span data-stu-id="fbe1d-122">Note that the contiguous quotation marks that represent a quotation mark in the string are independent of the quotation marks that begin and end the `String` literal.</span></span>  
  
## <a name="string-manipulations"></a><span data-ttu-id="fbe1d-123">字符串操作</span><span class="sxs-lookup"><span data-stu-id="fbe1d-123">String Manipulations</span></span>  

 <span data-ttu-id="fbe1d-124">将字符串分配给变量后， `String` 该字符串是 *不可变* 的，这意味着你无法更改其长度或内容。</span><span class="sxs-lookup"><span data-stu-id="fbe1d-124">Once you assign a string to a `String` variable, that string is *immutable*, which means you cannot change its length or contents.</span></span> <span data-ttu-id="fbe1d-125">以任何方式更改字符串时，Visual Basic 会创建一个新字符串，并放弃上一个字符串。</span><span class="sxs-lookup"><span data-stu-id="fbe1d-125">When you alter a string in any way, Visual Basic creates a new string and abandons the previous one.</span></span> <span data-ttu-id="fbe1d-126">然后，该 `String` 变量指向新的字符串。</span><span class="sxs-lookup"><span data-stu-id="fbe1d-126">The `String` variable then points to the new string.</span></span>  
  
 <span data-ttu-id="fbe1d-127">您可以 `String` 使用各种字符串函数来处理变量的内容。</span><span class="sxs-lookup"><span data-stu-id="fbe1d-127">You can manipulate the contents of a `String` variable by using a variety of string functions.</span></span> <span data-ttu-id="fbe1d-128">下面的示例阐释了 <xref:Microsoft.VisualBasic.Strings.Left%2A> 函数</span><span class="sxs-lookup"><span data-stu-id="fbe1d-128">The following example illustrates the <xref:Microsoft.VisualBasic.Strings.Left%2A> function</span></span>  
  
```vb  
Dim S As String = "Database"  
' The following statement sets S to a new string containing "Data".  
S = Microsoft.VisualBasic.Left(S, 4)  
```  
  
 <span data-ttu-id="fbe1d-129">其他组件创建的字符串可能用前导空格或尾随空格填充。</span><span class="sxs-lookup"><span data-stu-id="fbe1d-129">A string created by another component might be padded with leading or trailing spaces.</span></span> <span data-ttu-id="fbe1d-130">如果收到这样的字符串，可以使用 <xref:Microsoft.VisualBasic.Strings.Trim%2A> 、 <xref:Microsoft.VisualBasic.Strings.LTrim%2A> 和 <xref:Microsoft.VisualBasic.Strings.RTrim%2A> 函数来删除这些空格。</span><span class="sxs-lookup"><span data-stu-id="fbe1d-130">If you receive such a string, you can use the <xref:Microsoft.VisualBasic.Strings.Trim%2A>, <xref:Microsoft.VisualBasic.Strings.LTrim%2A>, and <xref:Microsoft.VisualBasic.Strings.RTrim%2A> functions to remove these spaces.</span></span>  
  
 <span data-ttu-id="fbe1d-131">有关字符串操作的详细信息，请参阅 [字符串](../../programming-guide/language-features/strings/index.md)。</span><span class="sxs-lookup"><span data-stu-id="fbe1d-131">For more information about string manipulations, see [Strings](../../programming-guide/language-features/strings/index.md).</span></span>  
  
## <a name="programming-tips"></a><span data-ttu-id="fbe1d-132">编程提示</span><span class="sxs-lookup"><span data-stu-id="fbe1d-132">Programming Tips</span></span>  
  
- <span data-ttu-id="fbe1d-133">**负数。**</span><span class="sxs-lookup"><span data-stu-id="fbe1d-133">**Negative Numbers.**</span></span> <span data-ttu-id="fbe1d-134">请记住，保留的字符 `String` 是无符号的，不能表示负值。</span><span class="sxs-lookup"><span data-stu-id="fbe1d-134">Remember that the characters held by `String` are unsigned and cannot represent negative values.</span></span> <span data-ttu-id="fbe1d-135">在任何情况下，不应使用 `String` 来保存数值。</span><span class="sxs-lookup"><span data-stu-id="fbe1d-135">In any case, you should not use `String` to hold numeric values.</span></span>  
  
- <span data-ttu-id="fbe1d-136">**互操作注意事项。**</span><span class="sxs-lookup"><span data-stu-id="fbe1d-136">**Interop Considerations.**</span></span> <span data-ttu-id="fbe1d-137">如果与不是为 .NET Framework 编写的组件（如自动化或 COM 对象）进行交互，请记住，在其他环境中，字符串字符具有不同的数据宽度 (8 位数) 。</span><span class="sxs-lookup"><span data-stu-id="fbe1d-137">If you are interfacing with components not written for the .NET Framework, for example Automation or COM objects, remember that string characters have a different data width (8 bits) in other environments.</span></span> <span data-ttu-id="fbe1d-138">如果将8位字符的字符串参数传递给此类组件，则将其声明为 `Byte()` 元素数组， `Byte` 而不是 `String` 新的 Visual Basic 代码。</span><span class="sxs-lookup"><span data-stu-id="fbe1d-138">If you are passing a string argument of 8-bit characters to such a component, declare it as `Byte()`, an array of `Byte` elements, instead of `String` in your new Visual Basic code.</span></span>  
  
- <span data-ttu-id="fbe1d-139">**键入字符。**</span><span class="sxs-lookup"><span data-stu-id="fbe1d-139">**Type Characters.**</span></span> <span data-ttu-id="fbe1d-140">如果将标识符类型字符追加 `$` 到任何标识符，则会将其强制转换为 `String` 数据类型。</span><span class="sxs-lookup"><span data-stu-id="fbe1d-140">Appending the identifier type character `$` to any identifier forces it to the `String` data type.</span></span> <span data-ttu-id="fbe1d-141">`String` 没有文本类型字符。</span><span class="sxs-lookup"><span data-stu-id="fbe1d-141">`String` has no literal type character.</span></span> <span data-ttu-id="fbe1d-142">但是，编译器会将括在引号中的文本视为 (`" "`) `String` 。</span><span class="sxs-lookup"><span data-stu-id="fbe1d-142">However, the compiler treats literals enclosed in quotation marks (`" "`) as `String`.</span></span>  
  
- <span data-ttu-id="fbe1d-143">**Framework 类型。**</span><span class="sxs-lookup"><span data-stu-id="fbe1d-143">**Framework Type.**</span></span> <span data-ttu-id="fbe1d-144">.NET Framework 中的相应类型是 <xref:System.String?displayProperty=nameWithType> 类。</span><span class="sxs-lookup"><span data-stu-id="fbe1d-144">The corresponding type in the .NET Framework is the <xref:System.String?displayProperty=nameWithType> class.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="fbe1d-145">请参阅</span><span class="sxs-lookup"><span data-stu-id="fbe1d-145">See also</span></span>

- <xref:System.String?displayProperty=nameWithType>
- [<span data-ttu-id="fbe1d-146">数据类型</span><span class="sxs-lookup"><span data-stu-id="fbe1d-146">Data Types</span></span>](index.md)
- [<span data-ttu-id="fbe1d-147">Char 数据类型</span><span class="sxs-lookup"><span data-stu-id="fbe1d-147">Char Data Type</span></span>](char-data-type.md)
- [<span data-ttu-id="fbe1d-148">Type Conversion Functions</span><span class="sxs-lookup"><span data-stu-id="fbe1d-148">Type Conversion Functions</span></span>](../functions/type-conversion-functions.md)
- [<span data-ttu-id="fbe1d-149">转换摘要</span><span class="sxs-lookup"><span data-stu-id="fbe1d-149">Conversion Summary</span></span>](../keywords/conversion-summary.md)
- [<span data-ttu-id="fbe1d-150">如何：调用需要使用无符号类型的 Windows 函数</span><span class="sxs-lookup"><span data-stu-id="fbe1d-150">How to: Call a Windows Function that Takes Unsigned Types</span></span>](../../programming-guide/com-interop/how-to-call-a-windows-function-that-takes-unsigned-types.md)
- [<span data-ttu-id="fbe1d-151">有效使用数据类型</span><span class="sxs-lookup"><span data-stu-id="fbe1d-151">Efficient Use of Data Types</span></span>](../../programming-guide/language-features/data-types/efficient-use-of-data-types.md)
