---
description: '了解更多相关信息： Like Operator (Visual Basic) '
title: Like 运算符
ms.date: 07/20/2015
f1_keywords:
- Like
- vb.Like
helpviewer_keywords:
- similar to
- pattern matching
- Like operator [Visual Basic]
- '? symbol, wildcard character'
- string comparison [Visual Basic], Like operator
- strings [Visual Basic], comparing
- comparison operators [Visual Basic]
- symbols, wildcard
- wildcards, Like operator
- strings [Visual Basic], matching
- string comparison [Visual Basic], sorting data
- data [Visual Basic], sorting
- text [Visual Basic], comparing
- operators [Visual Basic], pattern-matching
- data [Visual Basic], string comparisons
- string comparison [Visual Basic], Like operators
ms.assetid: 966283ec-80e2-4294-baa8-c75baff804f9
ms.openlocfilehash: f1be174010b7acae5bface4fc0a2d0e606a90fca
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99665583"
---
# <a name="like-operator-visual-basic"></a><span data-ttu-id="a391f-103">Like 运算符 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="a391f-103">Like Operator (Visual Basic)</span></span>

<span data-ttu-id="a391f-104">将字符串与模式进行比较。</span><span class="sxs-lookup"><span data-stu-id="a391f-104">Compares a string against a pattern.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="a391f-105">`Like`.Net Core 和 .NET Standard 项目目前不支持运算符。</span><span class="sxs-lookup"><span data-stu-id="a391f-105">The `Like` operator is currently not supported in .NET Core and .NET Standard projects.</span></span>

## <a name="syntax"></a><span data-ttu-id="a391f-106">语法</span><span class="sxs-lookup"><span data-stu-id="a391f-106">Syntax</span></span>  
  
```vb  
result = string Like pattern  
```  
  
## <a name="parts"></a><span data-ttu-id="a391f-107">组成部分</span><span class="sxs-lookup"><span data-stu-id="a391f-107">Parts</span></span>  

 `result`  
 <span data-ttu-id="a391f-108">必需。</span><span class="sxs-lookup"><span data-stu-id="a391f-108">Required.</span></span> <span data-ttu-id="a391f-109">任何 `Boolean` 变量。</span><span class="sxs-lookup"><span data-stu-id="a391f-109">Any `Boolean` variable.</span></span> <span data-ttu-id="a391f-110">结果是一个 `Boolean` 值，该值指示是否 `string` 满足 `pattern` 。</span><span class="sxs-lookup"><span data-stu-id="a391f-110">The result is a `Boolean` value indicating whether or not the `string` satisfies the `pattern`.</span></span>  
  
 `string`  
 <span data-ttu-id="a391f-111">必需。</span><span class="sxs-lookup"><span data-stu-id="a391f-111">Required.</span></span> <span data-ttu-id="a391f-112">任何 `String` 表达式。</span><span class="sxs-lookup"><span data-stu-id="a391f-112">Any `String` expression.</span></span>  
  
 `pattern`  
 <span data-ttu-id="a391f-113">必需。</span><span class="sxs-lookup"><span data-stu-id="a391f-113">Required.</span></span> <span data-ttu-id="a391f-114">`String`符合 "备注" 中所述的模式匹配约定的任何表达式。</span><span class="sxs-lookup"><span data-stu-id="a391f-114">Any `String` expression conforming to the pattern-matching conventions described in "Remarks."</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="a391f-115">备注</span><span class="sxs-lookup"><span data-stu-id="a391f-115">Remarks</span></span>  

 <span data-ttu-id="a391f-116">如果中的值 `string` 满足中包含的模式 `pattern` ， `result` 则为 `True` 。</span><span class="sxs-lookup"><span data-stu-id="a391f-116">If the value in `string` satisfies the pattern contained in `pattern`, `result` is `True`.</span></span> <span data-ttu-id="a391f-117">如果字符串不满足模式， `result` 则为 `False` 。</span><span class="sxs-lookup"><span data-stu-id="a391f-117">If the string does not satisfy the pattern, `result` is `False`.</span></span> <span data-ttu-id="a391f-118">如果 `string` 和 `pattern` 都为空字符串，则结果为 `True` 。</span><span class="sxs-lookup"><span data-stu-id="a391f-118">If both `string` and `pattern` are empty strings, the result is `True`.</span></span>  
  
## <a name="comparison-method"></a><span data-ttu-id="a391f-119">比较方法</span><span class="sxs-lookup"><span data-stu-id="a391f-119">Comparison Method</span></span>  

 <span data-ttu-id="a391f-120">运算符的行为 `Like` 取决于 [Option Compare 语句](../statements/option-compare-statement.md)。</span><span class="sxs-lookup"><span data-stu-id="a391f-120">The behavior of the `Like` operator depends on the [Option Compare Statement](../statements/option-compare-statement.md).</span></span> <span data-ttu-id="a391f-121">每个源文件的默认字符串比较方法为 `Option Compare Binary` 。</span><span class="sxs-lookup"><span data-stu-id="a391f-121">The default string comparison method for each source file is `Option Compare Binary`.</span></span>  
  
## <a name="pattern-options"></a><span data-ttu-id="a391f-122">模式选项</span><span class="sxs-lookup"><span data-stu-id="a391f-122">Pattern Options</span></span>  

 <span data-ttu-id="a391f-123">内置模式匹配为字符串比较提供了多种工具。</span><span class="sxs-lookup"><span data-stu-id="a391f-123">Built-in pattern matching provides a versatile tool for string comparisons.</span></span> <span data-ttu-id="a391f-124">使用模式匹配功能，可以将中的每个字符与 `string` 特定字符、通配符、字符列表或字符范围匹配。</span><span class="sxs-lookup"><span data-stu-id="a391f-124">The pattern-matching features allow you to match each character in `string` against a specific character, a wildcard character, a character list, or a character range.</span></span> <span data-ttu-id="a391f-125">下表显示了中允许的字符 `pattern` 以及它们匹配的内容。</span><span class="sxs-lookup"><span data-stu-id="a391f-125">The following table shows the characters allowed in `pattern` and what they match.</span></span>  
  
|<span data-ttu-id="a391f-126">字符 `pattern`</span><span class="sxs-lookup"><span data-stu-id="a391f-126">Characters in `pattern`</span></span>|<span data-ttu-id="a391f-127">匹配项 `string`</span><span class="sxs-lookup"><span data-stu-id="a391f-127">Matches in `string`</span></span>|  
|-----------------------------|-------------------------|  
|`?`|<span data-ttu-id="a391f-128">任何单个字符</span><span class="sxs-lookup"><span data-stu-id="a391f-128">Any single character</span></span>|  
|`*`|<span data-ttu-id="a391f-129">零个或多个字符</span><span class="sxs-lookup"><span data-stu-id="a391f-129">Zero or more characters</span></span>|  
|`#`|<span data-ttu-id="a391f-130">任何单个数字 (0 – 9) </span><span class="sxs-lookup"><span data-stu-id="a391f-130">Any single digit (0–9)</span></span>|  
|`[charlist]`|<span data-ttu-id="a391f-131">中的任何单个字符 `charlist`</span><span class="sxs-lookup"><span data-stu-id="a391f-131">Any single character in `charlist`</span></span>|  
|`[!charlist]`|<span data-ttu-id="a391f-132">不在中的任何单个字符 `charlist`</span><span class="sxs-lookup"><span data-stu-id="a391f-132">Any single character not in `charlist`</span></span>|  
  
## <a name="character-lists"></a><span data-ttu-id="a391f-133">字符列表</span><span class="sxs-lookup"><span data-stu-id="a391f-133">Character Lists</span></span>  

 <span data-ttu-id="a391f-134">括在括号中的一个或多个字符组 (`charlist`)  (`[ ]`) 可用于匹配中的任何单个字符 `string` ，并可包括几乎所有字符代码（包括数字）。</span><span class="sxs-lookup"><span data-stu-id="a391f-134">A group of one or more characters (`charlist`) enclosed in brackets (`[ ]`) can be used to match any single character in `string` and can include almost any character code, including digits.</span></span>  
  
 <span data-ttu-id="a391f-135">开始时 () 的感叹号 `!` 表示在中 `charlist` 找到除中的字符以外的任何字符时进行匹配 `charlist` `string` 。</span><span class="sxs-lookup"><span data-stu-id="a391f-135">An exclamation point (`!`) at the beginning of `charlist` means that a match is made if any character except the characters in `charlist` is found in `string`.</span></span> <span data-ttu-id="a391f-136">当在方括号外使用时，感叹号与自身匹配。</span><span class="sxs-lookup"><span data-stu-id="a391f-136">When used outside brackets, the exclamation point matches itself.</span></span>  
  
## <a name="special-characters"></a><span data-ttu-id="a391f-137">特殊字符</span><span class="sxs-lookup"><span data-stu-id="a391f-137">Special Characters</span></span>  

 <span data-ttu-id="a391f-138">若要匹配特殊字符左方括号 (`[`) 、问号 (`?`) 、数字符号 () `#` 和星号 () `*` ，请将它们括在括号中。</span><span class="sxs-lookup"><span data-stu-id="a391f-138">To match the special characters left bracket (`[`), question mark (`?`), number sign (`#`), and asterisk (`*`), enclose them in brackets.</span></span> <span data-ttu-id="a391f-139">`]`不能在组内使用右方括号 () ，而是可以将其作为单个字符在组外使用。</span><span class="sxs-lookup"><span data-stu-id="a391f-139">The right bracket (`]`) cannot be used within a group to match itself, but it can be used outside a group as an individual character.</span></span>  
  
 <span data-ttu-id="a391f-140">字符序列 `[]` 被视为 () 长度为零的字符串 `""` 。</span><span class="sxs-lookup"><span data-stu-id="a391f-140">The character sequence `[]` is considered a zero-length string (`""`).</span></span> <span data-ttu-id="a391f-141">但是，它不能是括在括号中的字符列表的一部分。</span><span class="sxs-lookup"><span data-stu-id="a391f-141">However, it cannot be part of a character list enclosed in brackets.</span></span> <span data-ttu-id="a391f-142">如果要检查中的某个位置是否 `string` 包含一组字符或不包含任何字符，可以使用 `Like` 两次。</span><span class="sxs-lookup"><span data-stu-id="a391f-142">If you want to check whether a position in `string` contains one of a group of characters or no character at all, you can use `Like` twice.</span></span> <span data-ttu-id="a391f-143">有关示例，请参阅 [如何：将字符串与模式匹配](../../programming-guide/language-features/operators-and-expressions/how-to-match-a-string-against-a-pattern.md)。</span><span class="sxs-lookup"><span data-stu-id="a391f-143">For an example, see [How to: Match a String against a Pattern](../../programming-guide/language-features/operators-and-expressions/how-to-match-a-string-against-a-pattern.md).</span></span>  
  
## <a name="character-ranges"></a><span data-ttu-id="a391f-144">字符范围</span><span class="sxs-lookup"><span data-stu-id="a391f-144">Character Ranges</span></span>  

 <span data-ttu-id="a391f-145">通过使用连字符 (`–`) 来分隔范围的下限和上限， `charlist` 可以指定字符范围。</span><span class="sxs-lookup"><span data-stu-id="a391f-145">By using a hyphen (`–`) to separate the lower and upper bounds of the range, `charlist` can specify a range of characters.</span></span> <span data-ttu-id="a391f-146">例如， `[A–Z]` 如果中的相应字符位置 `string` 包含范围内的任何字符，则会导致匹配 `A` `Z` ; `[!H–L]` 如果相应的字符位置包含范围之外的任何字符， `H` `L` 则结果将生成匹配项。</span><span class="sxs-lookup"><span data-stu-id="a391f-146">For example, `[A–Z]` results in a match if the corresponding character position in `string` contains any character within the range `A`–`Z`, and `[!H–L]` results in a match if the corresponding character position contains any character outside the range `H`–`L`.</span></span>  
  
 <span data-ttu-id="a391f-147">指定字符范围时，它们必须按升序排序，即从最低到最高。</span><span class="sxs-lookup"><span data-stu-id="a391f-147">When you specify a range of characters, they must appear in ascending sort order, that is, from lowest to highest.</span></span> <span data-ttu-id="a391f-148">因此， `[A–Z]` 是有效的模式，但 `[Z–A]` 不是。</span><span class="sxs-lookup"><span data-stu-id="a391f-148">Thus, `[A–Z]` is a valid pattern, but `[Z–A]` is not.</span></span>  
  
### <a name="multiple-character-ranges"></a><span data-ttu-id="a391f-149">多字符范围</span><span class="sxs-lookup"><span data-stu-id="a391f-149">Multiple Character Ranges</span></span>  

 <span data-ttu-id="a391f-150">若要为同一字符位置指定多个范围，请将它们放在不带分隔符的相同括号中。</span><span class="sxs-lookup"><span data-stu-id="a391f-150">To specify multiple ranges for the same character position, put them within the same brackets without delimiters.</span></span> <span data-ttu-id="a391f-151">例如， `[A–CX–Z]` 如果中的相应字符位置 `string` 包含范围或范围内的任何字符，则会导致 `A` 匹配 `C` `X` `Z` 。</span><span class="sxs-lookup"><span data-stu-id="a391f-151">For example, `[A–CX–Z]` results in a match if the corresponding character position in `string` contains any character within either the range `A`–`C` or the range `X`–`Z`.</span></span>  
  
### <a name="usage-of-the-hyphen"></a><span data-ttu-id="a391f-152">连字符的用法</span><span class="sxs-lookup"><span data-stu-id="a391f-152">Usage of the Hyphen</span></span>  

 <span data-ttu-id="a391f-153">连字符 (`–`) 可以出现在感叹号后的开头 (，如果有任何) 或末尾，则 `charlist` 为。</span><span class="sxs-lookup"><span data-stu-id="a391f-153">A hyphen (`–`) can appear either at the beginning (after an exclamation point, if any) or at the end of `charlist` to match itself.</span></span> <span data-ttu-id="a391f-154">在其他任何位置，连字符标识由连字符两侧的字符分隔的一系列字符。</span><span class="sxs-lookup"><span data-stu-id="a391f-154">In any other location, the hyphen identifies a range of characters delimited by the characters on either side of the hyphen.</span></span>  
  
## <a name="collating-sequence"></a><span data-ttu-id="a391f-155">排序顺序</span><span class="sxs-lookup"><span data-stu-id="a391f-155">Collating Sequence</span></span>  

 <span data-ttu-id="a391f-156">指定范围的含义取决于运行时的字符排序，由确定， `Option Compare` 以及运行代码的系统的区域设置。</span><span class="sxs-lookup"><span data-stu-id="a391f-156">The meaning of a specified range depends on the character ordering at run time, as determined by `Option Compare` and the locale setting of the system the code is running on.</span></span> <span data-ttu-id="a391f-157">对于 `Option Compare Binary` ，范围 `[A–E]` 匹配、、、 `A` `B` `C` `D` 和 `E` 。</span><span class="sxs-lookup"><span data-stu-id="a391f-157">With `Option Compare Binary`, the range `[A–E]` matches `A`, `B`, `C`, `D`, and `E`.</span></span> <span data-ttu-id="a391f-158">With、匹配、、、、、、、、、、 `Option Compare Text` `[A–E]` `A` `a` `À` `à` `B` `b` `C` `c` `D` `d` `E` 和 `e` 。</span><span class="sxs-lookup"><span data-stu-id="a391f-158">With `Option Compare Text`, `[A–E]` matches `A`, `a`, `À`, `à`, `B`, `b`, `C`, `c`, `D`, `d`, `E`, and `e`.</span></span> <span data-ttu-id="a391f-159">该范围不匹配， `Ê` 也不是 `ê` 因为重音字符在排序顺序中逐重音字符排序。</span><span class="sxs-lookup"><span data-stu-id="a391f-159">The range does not match `Ê` or `ê` because accented characters collate after unaccented characters in the sort order.</span></span>  
  
## <a name="digraph-characters"></a><span data-ttu-id="a391f-160">连字符</span><span class="sxs-lookup"><span data-stu-id="a391f-160">Digraph Characters</span></span>  

 <span data-ttu-id="a391f-161">在某些语言中，有表示两个不同字符的字母字符。</span><span class="sxs-lookup"><span data-stu-id="a391f-161">In some languages, there are alphabetic characters that represent two separate characters.</span></span> <span data-ttu-id="a391f-162">例如，几种语言使用字符 `æ` 来表示字符 `a` 以及 `e` 它们一起显示的字符。</span><span class="sxs-lookup"><span data-stu-id="a391f-162">For example, several languages use the character `æ` to represent the characters `a` and `e` when they appear together.</span></span> <span data-ttu-id="a391f-163">`Like`运算符识别单个连字符和两个单个字符是否等效。</span><span class="sxs-lookup"><span data-stu-id="a391f-163">The `Like` operator recognizes that the single digraph character and the two individual characters are equivalent.</span></span>  
  
 <span data-ttu-id="a391f-164">如果在系统区域设置中指定了使用连字符的语言，则或中的单个连字符的出现位置 `pattern` `string` 与另一个字符串中的等效双字符序列匹配。</span><span class="sxs-lookup"><span data-stu-id="a391f-164">When a language that uses a digraph character is specified in the system locale settings, an occurrence of the single digraph character in either `pattern` or `string` matches the equivalent two-character sequence in the other string.</span></span> <span data-ttu-id="a391f-165">同样， `pattern` 括在括号中的一条带区字符 (自身、列表或范围中) 与中等效的双字符序列匹配 `string` 。</span><span class="sxs-lookup"><span data-stu-id="a391f-165">Similarly, a digraph character in `pattern` enclosed in brackets (by itself, in a list, or in a range) matches the equivalent two-character sequence in `string`.</span></span>  
  
## <a name="overloading"></a><span data-ttu-id="a391f-166">重载</span><span class="sxs-lookup"><span data-stu-id="a391f-166">Overloading</span></span>  

 <span data-ttu-id="a391f-167">`Like`运算符可以 *重载*，这意味着当操作数具有该类或结构的类型时，该类或结构可以重新定义其行为。</span><span class="sxs-lookup"><span data-stu-id="a391f-167">The `Like` operator can be *overloaded*, which means that a class or structure can redefine its behavior when an operand has the type of that class or structure.</span></span> <span data-ttu-id="a391f-168">如果你的代码在该类或结构上使用此运算符，请确保了解其重新定义的行为。</span><span class="sxs-lookup"><span data-stu-id="a391f-168">If your code uses this operator on such a class or structure, be sure you understand its redefined behavior.</span></span> <span data-ttu-id="a391f-169">有关详细信息，请参阅 [Operator Procedures](../../programming-guide/language-features/procedures/operator-procedures.md)。</span><span class="sxs-lookup"><span data-stu-id="a391f-169">For more information, see [Operator Procedures](../../programming-guide/language-features/procedures/operator-procedures.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="a391f-170">示例</span><span class="sxs-lookup"><span data-stu-id="a391f-170">Example</span></span>  

 <span data-ttu-id="a391f-171">此示例使用 `Like` 运算符将字符串与各种模式进行比较。</span><span class="sxs-lookup"><span data-stu-id="a391f-171">This example uses the `Like` operator to compare strings to various patterns.</span></span> <span data-ttu-id="a391f-172">结果将进入一个 `Boolean` 变量，该变量指示每个字符串是否满足此模式。</span><span class="sxs-lookup"><span data-stu-id="a391f-172">The results go into a `Boolean` variable indicating whether each string satisfies the pattern.</span></span>  
  
 [!code-vb[VbVbalrOperators#30](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrOperators/VB/Class1.vb#30)]  
  
## <a name="see-also"></a><span data-ttu-id="a391f-173">请参阅</span><span class="sxs-lookup"><span data-stu-id="a391f-173">See also</span></span>

- <xref:Microsoft.VisualBasic.Strings.InStr%2A>
- <xref:Microsoft.VisualBasic.Strings.StrComp%2A>
- [<span data-ttu-id="a391f-174">比较运算符</span><span class="sxs-lookup"><span data-stu-id="a391f-174">Comparison Operators</span></span>](comparison-operators.md)
- [<span data-ttu-id="a391f-175">Visual Basic 中的运算符优先级</span><span class="sxs-lookup"><span data-stu-id="a391f-175">Operator Precedence in Visual Basic</span></span>](operator-precedence.md)
- [<span data-ttu-id="a391f-176">按功能列出的运算符</span><span class="sxs-lookup"><span data-stu-id="a391f-176">Operators Listed by Functionality</span></span>](operators-listed-by-functionality.md)
- [<span data-ttu-id="a391f-177">Option Compare 语句</span><span class="sxs-lookup"><span data-stu-id="a391f-177">Option Compare Statement</span></span>](../statements/option-compare-statement.md)
- [<span data-ttu-id="a391f-178">运算符和表达式</span><span class="sxs-lookup"><span data-stu-id="a391f-178">Operators and Expressions</span></span>](../../programming-guide/language-features/operators-and-expressions/index.md)
- [<span data-ttu-id="a391f-179">如何：将字符串与模式相匹配</span><span class="sxs-lookup"><span data-stu-id="a391f-179">How to: Match a String against a Pattern</span></span>](../../programming-guide/language-features/operators-and-expressions/how-to-match-a-string-against-a-pattern.md)
