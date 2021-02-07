---
description: '了解详细信息： (Visual Basic 的字符串函数) '
title: 字符串函数
ms.date: 07/20/2015
helpviewer_keywords:
- string functions
ms.assetid: f1bf9ac2-cbcf-4298-ae51-53182076bdc8
ms.openlocfilehash: 1c121bc3de66caf748426b5cd04d049b30bf78bb
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99731102"
---
# <a name="string-functions-visual-basic"></a><span data-ttu-id="f6347-103">字符串函数 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="f6347-103">String Functions (Visual Basic)</span></span>

<span data-ttu-id="f6347-104">下表列出了 Visual Basic 在类中提供的 <xref:Microsoft.VisualBasic.Strings?displayProperty=nameWithType> 用于搜索和操作字符串的函数。</span><span class="sxs-lookup"><span data-stu-id="f6347-104">The following table lists the functions that Visual Basic provides in the <xref:Microsoft.VisualBasic.Strings?displayProperty=nameWithType> class to search and manipulate strings.</span></span> <span data-ttu-id="f6347-105">它们可以视为 Visual Basic 内部函数;也就是说，您不必将它们作为类的显式成员进行调用，如示例所示。</span><span class="sxs-lookup"><span data-stu-id="f6347-105">They can be regarded as Visual Basic intrinsic functions; that is, you do not have to call them as explicit members of a class, as the examples show.</span></span> <span data-ttu-id="f6347-106">类中提供了其他方法，在某些情况下为互补方法 <xref:System.String?displayProperty=nameWithType> 。</span><span class="sxs-lookup"><span data-stu-id="f6347-106">Additional methods, and in some cases complementary methods, are available in the <xref:System.String?displayProperty=nameWithType> class.</span></span>

|<span data-ttu-id="f6347-107">.NET Framework 方法</span><span class="sxs-lookup"><span data-stu-id="f6347-107">.NET Framework method</span></span>|<span data-ttu-id="f6347-108">说明</span><span class="sxs-lookup"><span data-stu-id="f6347-108">Description</span></span>|
|---------------------------|-----------------|
|<span data-ttu-id="f6347-109"><xref:Microsoft.VisualBasic.Strings.Asc%2A>, <xref:Microsoft.VisualBasic.Strings.AscW%2A></span><span class="sxs-lookup"><span data-stu-id="f6347-109"><xref:Microsoft.VisualBasic.Strings.Asc%2A>, <xref:Microsoft.VisualBasic.Strings.AscW%2A></span></span>|<span data-ttu-id="f6347-110">返回一个 `Integer` 值，该值表示与某个字符相对应的字符代码。</span><span class="sxs-lookup"><span data-stu-id="f6347-110">Returns an `Integer` value representing the character code corresponding to a character.</span></span>|
|<span data-ttu-id="f6347-111"><xref:Microsoft.VisualBasic.Strings.Chr%2A>, <xref:Microsoft.VisualBasic.Strings.ChrW%2A></span><span class="sxs-lookup"><span data-stu-id="f6347-111"><xref:Microsoft.VisualBasic.Strings.Chr%2A>, <xref:Microsoft.VisualBasic.Strings.ChrW%2A></span></span>|<span data-ttu-id="f6347-112">返回与指定字符代码相关联的字符。</span><span class="sxs-lookup"><span data-stu-id="f6347-112">Returns the character associated with the specified character code.</span></span>|
|<xref:Microsoft.VisualBasic.Strings.Filter%2A>|<span data-ttu-id="f6347-113">返回一个从零开始的数组，该数组包含基于指定筛选条件的 `String` 数组的子集。</span><span class="sxs-lookup"><span data-stu-id="f6347-113">Returns a zero-based array containing a subset of a `String` array based on specified filter criteria.</span></span>|
|<xref:Microsoft.VisualBasic.Strings.Format%2A>|<span data-ttu-id="f6347-114">返回根据格式 `String` 表达式中包含的指令设置格式的字符串。</span><span class="sxs-lookup"><span data-stu-id="f6347-114">Returns a string formatted according to instructions contained in a format `String` expression.</span></span>|
|<xref:Microsoft.VisualBasic.Strings.FormatCurrency%2A>|<span data-ttu-id="f6347-115">返回一个格式为货币值的表达式，该货币值使用系统控制面板中定义的货币符号。</span><span class="sxs-lookup"><span data-stu-id="f6347-115">Returns an expression formatted as a currency value using the currency symbol defined in the system control panel.</span></span>|
|<xref:Microsoft.VisualBasic.Strings.FormatDateTime%2A>|<span data-ttu-id="f6347-116">返回一个表示日期/时间值的字符串表达式。</span><span class="sxs-lookup"><span data-stu-id="f6347-116">Returns a string expression representing a date/time value.</span></span>|
|<xref:Microsoft.VisualBasic.Strings.FormatNumber%2A>|<span data-ttu-id="f6347-117">返回格式化为数字的表达式。</span><span class="sxs-lookup"><span data-stu-id="f6347-117">Returns an expression formatted as a number.</span></span>|
|<xref:Microsoft.VisualBasic.Strings.FormatPercent%2A>|<span data-ttu-id="f6347-118">返回以 % 字符结尾的百分比格式的表达式（即乘以 100）。</span><span class="sxs-lookup"><span data-stu-id="f6347-118">Returns an expression formatted as a percentage (that is, multiplied by 100) with a trailing % character.</span></span>|
|<xref:Microsoft.VisualBasic.Strings.InStr%2A>|<span data-ttu-id="f6347-119">返回一个整数，该整数指定一个字符串在另一个字符串中的第一个匹配项的起始位置。</span><span class="sxs-lookup"><span data-stu-id="f6347-119">Returns an integer specifying the start position of the first occurrence of one string within another.</span></span>|
|<xref:Microsoft.VisualBasic.Strings.InStrRev%2A>|<span data-ttu-id="f6347-120">返回某一字符串从另一字符串的右侧开始算起第一次出现的位置。</span><span class="sxs-lookup"><span data-stu-id="f6347-120">Returns the position of the first occurrence of one string within another, starting from the right side of the string.</span></span>|
|<xref:Microsoft.VisualBasic.Strings.Join%2A>|<span data-ttu-id="f6347-121">返回通过连接一个数组中包含的若干子字符串创建的字符串。</span><span class="sxs-lookup"><span data-stu-id="f6347-121">Returns a string created by joining a number of substrings contained in an array.</span></span>|
|<xref:Microsoft.VisualBasic.Strings.LCase%2A>|<span data-ttu-id="f6347-122">返回将转换为小写的字符串或字符。</span><span class="sxs-lookup"><span data-stu-id="f6347-122">Returns a string or character converted to lowercase.</span></span>|
|<xref:Microsoft.VisualBasic.Strings.Left%2A>|<span data-ttu-id="f6347-123">返回一个字符串，该字符串包含从某字符串左侧算起的指定数量的字符。</span><span class="sxs-lookup"><span data-stu-id="f6347-123">Returns a string containing a specified number of characters from the left side of a string.</span></span>|
|<xref:Microsoft.VisualBasic.Strings.Len%2A>|<span data-ttu-id="f6347-124">返回一个整数，该整数包含字符串中的字符数。</span><span class="sxs-lookup"><span data-stu-id="f6347-124">Returns an integer that contains the number of characters in a string.</span></span>|
|<xref:Microsoft.VisualBasic.Strings.LSet%2A>|<span data-ttu-id="f6347-125">返回一个左对齐字符串，该字符串包含调整为指定长度的指定的字符串。</span><span class="sxs-lookup"><span data-stu-id="f6347-125">Returns a left-aligned string containing the specified string adjusted to the specified length.</span></span>|
|<xref:Microsoft.VisualBasic.Strings.LTrim%2A>|<span data-ttu-id="f6347-126">返回一个字符串，该字符串包含不带前导空格的指定字符串的副本。</span><span class="sxs-lookup"><span data-stu-id="f6347-126">Returns a string containing a copy of a specified string with no leading spaces.</span></span>|
|<xref:Microsoft.VisualBasic.Strings.Mid%2A>|<span data-ttu-id="f6347-127">返回一个字符串，该字符串包含字符串中指定数目的字符。</span><span class="sxs-lookup"><span data-stu-id="f6347-127">Returns a string containing a specified number of characters from a string.</span></span>|
|<xref:Microsoft.VisualBasic.Strings.Replace%2A>|<span data-ttu-id="f6347-128">返回一个字符串，其中的指定子字符串已由另一个子字符串替换了指定的次数。</span><span class="sxs-lookup"><span data-stu-id="f6347-128">Returns a string in which a specified substring has been replaced with another substring a specified number of times.</span></span>|
|<xref:Microsoft.VisualBasic.Strings.Right%2A>|<span data-ttu-id="f6347-129">返回一个字符串，其中包含从某个字符串右端开始的指定数量的字符。</span><span class="sxs-lookup"><span data-stu-id="f6347-129">Returns a string containing a specified number of characters from the right side of a string.</span></span>|
|<xref:Microsoft.VisualBasic.Strings.RSet%2A>|<span data-ttu-id="f6347-130">返回包含调整为指定长度的指定字符串的右对齐字符串。</span><span class="sxs-lookup"><span data-stu-id="f6347-130">Returns a right-aligned string containing the specified string adjusted to the specified length.</span></span>|
|<xref:Microsoft.VisualBasic.Strings.RTrim%2A>|<span data-ttu-id="f6347-131">返回一个字符串，该字符串包含不带尾随空格的指定字符串的副本。</span><span class="sxs-lookup"><span data-stu-id="f6347-131">Returns a string containing a copy of a specified string with no trailing spaces.</span></span>|
|<xref:Microsoft.VisualBasic.Strings.Space%2A>|<span data-ttu-id="f6347-132">返回由指定数量空格组成的字符串。</span><span class="sxs-lookup"><span data-stu-id="f6347-132">Returns a string consisting of the specified number of spaces.</span></span>|
|<xref:Microsoft.VisualBasic.Strings.Split%2A>|<span data-ttu-id="f6347-133">返回一个从零开始的一维数组，其中包含指定数量的子字符串。</span><span class="sxs-lookup"><span data-stu-id="f6347-133">Returns a zero-based, one-dimensional array containing a specified number of substrings.</span></span>|
|<xref:Microsoft.VisualBasic.Strings.StrComp%2A>|<span data-ttu-id="f6347-134">根据字符串的比较结果返回 -1、0 或 1。</span><span class="sxs-lookup"><span data-stu-id="f6347-134">Returns -1, 0, or 1, based on the result of a string comparison.</span></span>|
|<xref:Microsoft.VisualBasic.Strings.StrConv%2A>|<span data-ttu-id="f6347-135">返回按照指定方式转换的字符串。</span><span class="sxs-lookup"><span data-stu-id="f6347-135">Returns a string converted as specified.</span></span>|
|<xref:Microsoft.VisualBasic.Strings.StrDup%2A>|<span data-ttu-id="f6347-136">返回由指定字符重复指定次数后形成的字符串或对象。</span><span class="sxs-lookup"><span data-stu-id="f6347-136">Returns a string or object consisting of the specified character repeated the specified number of times.</span></span>|
|<xref:Microsoft.VisualBasic.Strings.StrReverse%2A>|<span data-ttu-id="f6347-137">返回指定字符串的字符顺序是相反的字符串。</span><span class="sxs-lookup"><span data-stu-id="f6347-137">Returns a string in which the character order of a specified string is reversed.</span></span>|
|<xref:Microsoft.VisualBasic.Strings.Trim%2A>|<span data-ttu-id="f6347-138">返回一个字符串，该字符串包含不带前导空格或尾随空格的指定字符串的副本。</span><span class="sxs-lookup"><span data-stu-id="f6347-138">Returns a string containing a copy of a specified string with no leading or trailing spaces.</span></span>|
|<xref:Microsoft.VisualBasic.Strings.UCase%2A>|<span data-ttu-id="f6347-139">返回一个字符串或字符，其中包含转换为大写的指定字符串。</span><span class="sxs-lookup"><span data-stu-id="f6347-139">Returns a string or character containing the specified string converted to uppercase.</span></span>|

<span data-ttu-id="f6347-140">您可以使用 [Option Compare](../statements/option-compare-statement.md) 语句来设置是否使用由您的系统区域设置确定的不区分大小写的文本排序顺序对字符串进行比较 (`Text`) 或 () 字符的内部二进制表示形式 `Binary` 。</span><span class="sxs-lookup"><span data-stu-id="f6347-140">You can use the [Option Compare](../statements/option-compare-statement.md) statement to set whether strings are compared using a case-insensitive text sort order determined by your system's locale (`Text`) or by the internal binary representations of the characters (`Binary`).</span></span> <span data-ttu-id="f6347-141">默认的文本比较方法是 `Binary`。</span><span class="sxs-lookup"><span data-stu-id="f6347-141">The default text comparison method is `Binary`.</span></span>

## <a name="example-ucase"></a><span data-ttu-id="f6347-142">示例： UCase</span><span class="sxs-lookup"><span data-stu-id="f6347-142">Example: UCase</span></span>

<span data-ttu-id="f6347-143">本例使用 `UCase` 函数返回字符串的大写版本。</span><span class="sxs-lookup"><span data-stu-id="f6347-143">This example uses the `UCase` function to return an uppercase version of a string.</span></span>
[!code-vb[VbVbalrStrings#31](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStrings/VB/Class1.vb#31)]

## <a name="example-ltrim"></a><span data-ttu-id="f6347-144">示例： LTrim</span><span class="sxs-lookup"><span data-stu-id="f6347-144">Example: LTrim</span></span>

<span data-ttu-id="f6347-145">此示例使用 `LTrim` 函数去除字符串变量的前导空格，使用 `RTrim` 函数去除尾随空格，</span><span class="sxs-lookup"><span data-stu-id="f6347-145">This example uses the `LTrim` function to strip leading spaces and the `RTrim` function to strip trailing spaces from a string variable.</span></span> <span data-ttu-id="f6347-146">并使用 `Trim` 函数同时去除这两种类型的空格。</span><span class="sxs-lookup"><span data-stu-id="f6347-146">It uses the `Trim` function to strip both types of spaces.</span></span>

[!code-vb[VbVbalrStrings#25](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStrings/VB/Class1.vb#25)]

## <a name="example-mid"></a><span data-ttu-id="f6347-147">示例： Mid</span><span class="sxs-lookup"><span data-stu-id="f6347-147">Example: Mid</span></span>

<span data-ttu-id="f6347-148">此示例使用 `Mid` 函数从字符串返回指定数目的字符。</span><span class="sxs-lookup"><span data-stu-id="f6347-148">This example uses the `Mid` function to return a specified number of characters from a string.</span></span>

[!code-vb[VbVbalrStrings#17](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStrings/VB/Class1.vb#17)]

## <a name="example-len"></a><span data-ttu-id="f6347-149">示例： Len</span><span class="sxs-lookup"><span data-stu-id="f6347-149">Example: Len</span></span>

<span data-ttu-id="f6347-150">本例使用 `Len` 返回字符串中的字符数。</span><span class="sxs-lookup"><span data-stu-id="f6347-150">This example uses `Len` to return the number of characters in a string.</span></span>

[!code-vb[VbVbalrStrings#33](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStrings/VB/Class1.vb#33)]

## <a name="example-instr"></a><span data-ttu-id="f6347-151">示例： InStr</span><span class="sxs-lookup"><span data-stu-id="f6347-151">Example: InStr</span></span>

<span data-ttu-id="f6347-152">本例使用 `InStr` 函数返回一个字符串在另一个字符串中的第一个匹配项的位置。</span><span class="sxs-lookup"><span data-stu-id="f6347-152">This example uses the `InStr` function to return the position of the first occurrence of one string within another.</span></span>

[!code-vb[VbVbalrStrings#8](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStrings/VB/Class1.vb#8)]

## <a name="example-format"></a><span data-ttu-id="f6347-153">示例：格式</span><span class="sxs-lookup"><span data-stu-id="f6347-153">Example: Format</span></span>

<span data-ttu-id="f6347-154">此示例演示同时使用 `Format` 格式和用户定义格式格式化值的 `String` 函数的各种用法。</span><span class="sxs-lookup"><span data-stu-id="f6347-154">This example shows various uses of the `Format` function to format values using both `String` formats and user-defined formats.</span></span> <span data-ttu-id="f6347-155">对于日期分隔符 (`/`)、时间分隔符 (`:`) 和 AM/PM 指示符（`t` 和 `tt`），系统显示的实际格式化输出取决于代码使用的区域设置。</span><span class="sxs-lookup"><span data-stu-id="f6347-155">For the date separator (`/`), time separator (`:`), and the AM/PM indicators (`t` and `tt`), the actual formatted output displayed by your system depends on the locale settings the code is using.</span></span> <span data-ttu-id="f6347-156">当在开发环境中显示时间和日期时，使用代码区域设置的短时间格式和短日期格式。</span><span class="sxs-lookup"><span data-stu-id="f6347-156">When times and dates are displayed in the development environment, the short time format and short date format of the code locale are used.</span></span>

> [!NOTE]
> <span data-ttu-id="f6347-157">对于使用 24 小时制的区域设置，AM/PM 指示符（`t` 和 `tt`）不显示任何内容。</span><span class="sxs-lookup"><span data-stu-id="f6347-157">For locales that use a 24-hour clock, the AM/PM indicators (`t` and `tt`) display nothing.</span></span>

[!code-vb[VbVbalrStrings#27](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStrings/VB/Class1.vb#27)]

## <a name="see-also"></a><span data-ttu-id="f6347-158">请参阅</span><span class="sxs-lookup"><span data-stu-id="f6347-158">See also</span></span>

- [<span data-ttu-id="f6347-159">关键字</span><span class="sxs-lookup"><span data-stu-id="f6347-159">Keywords</span></span>](../keywords/index.md)
- [<span data-ttu-id="f6347-160">Visual Basic 运行库成员</span><span class="sxs-lookup"><span data-stu-id="f6347-160">Visual Basic Runtime Library Members</span></span>](../runtime-library-members.md)
- [<span data-ttu-id="f6347-161">字符串操作摘要</span><span class="sxs-lookup"><span data-stu-id="f6347-161">String Manipulation Summary</span></span>](../keywords/string-manipulation-summary.md)
- [<span data-ttu-id="f6347-162">System.string 类方法</span><span class="sxs-lookup"><span data-stu-id="f6347-162">System.String class methods</span></span>](xref:System.String#methods)
