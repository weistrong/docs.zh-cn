---
description: 了解有关详细信息，请参阅如何：将字符串转换为 Visual Basic 中的字符数组
title: 如何：将字符串转换为字符数组
ms.date: 07/20/2015
helpviewer_keywords:
- character arrays [Visual Basic], converting strings
- arrays [Visual Basic], converting strings to
- examples [Visual Basic], string conversion
- strings [Visual Basic], converting to arrays
- string conversion [Visual Basic], arrays
ms.assetid: 1b54b686-ab29-413b-adce-6bd5422376eb
ms.openlocfilehash: f85b0801cf013e207eacd70a256a3ed0a8dc7887
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100476145"
---
# <a name="how-to-convert-a-string-to-an-array-of-characters-in-visual-basic"></a><span data-ttu-id="1c50c-103">如何：在 Visual Basic 中将字符串转换为字符数组</span><span class="sxs-lookup"><span data-stu-id="1c50c-103">How to: Convert a String to an Array of Characters in Visual Basic</span></span>

<span data-ttu-id="1c50c-104">有时，对字符串中的字符和这些字符在字符串中的位置（例如在分析字符串时）使用数据是非常有用的。</span><span class="sxs-lookup"><span data-stu-id="1c50c-104">Sometimes it is useful to have data about the characters in your string and the positions of those characters within your string, such as when you are parsing a string.</span></span> <span data-ttu-id="1c50c-105">此示例演示如何通过调用字符串的方法来获取字符串中的字符数组 <xref:System.String.ToCharArray%2A> 。</span><span class="sxs-lookup"><span data-stu-id="1c50c-105">This example shows how you can get an array of the characters in a string by calling the string's <xref:System.String.ToCharArray%2A> method.</span></span>  
  
## <a name="example"></a><span data-ttu-id="1c50c-106">示例</span><span class="sxs-lookup"><span data-stu-id="1c50c-106">Example</span></span>  

 <span data-ttu-id="1c50c-107">此示例演示如何将字符串拆分为 `Char` 数组，以及如何将字符串拆分为 `String` 其 Unicode 文本字符的数组。</span><span class="sxs-lookup"><span data-stu-id="1c50c-107">This example demonstrates how to split a string into a `Char` array, and how to split a string into a `String` array of its Unicode text characters.</span></span> <span data-ttu-id="1c50c-108">此区别的原因是 Unicode 文本字符可以由两个或更多字符组成 `Char` (如代理项对或组合字符序列) 。</span><span class="sxs-lookup"><span data-stu-id="1c50c-108">The reason for this distinction is that Unicode text characters can be composed of two or more `Char` characters (such as a surrogate pair or a combining character sequence).</span></span> <span data-ttu-id="1c50c-109">有关详细信息，请参阅 <xref:System.Globalization.TextElementEnumerator> 和 [Unicode 标准](https://www.unicode.org/standard/standard.html)。</span><span class="sxs-lookup"><span data-stu-id="1c50c-109">For more information, see <xref:System.Globalization.TextElementEnumerator> and [The Unicode Standard](https://www.unicode.org/standard/standard.html).</span></span>  
  
 [!code-vb[VbVbalrStrings#75](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStrings/VB/Class4.vb#75)]  
  
## <a name="example"></a><span data-ttu-id="1c50c-110">示例</span><span class="sxs-lookup"><span data-stu-id="1c50c-110">Example</span></span>  

 <span data-ttu-id="1c50c-111">更难将字符串拆分为其 Unicode 文本字符，但如果需要有关字符串的可视化表示形式的信息，则这是必需的。</span><span class="sxs-lookup"><span data-stu-id="1c50c-111">It is more difficult to split a string into its Unicode text characters, but this is necessary if you need information about the visual representation of a string.</span></span> <span data-ttu-id="1c50c-112">此示例使用 <xref:System.Globalization.StringInfo.SubstringByTextElements%2A> 方法获取有关构成字符串的 Unicode 文本字符的信息。</span><span class="sxs-lookup"><span data-stu-id="1c50c-112">This example uses the <xref:System.Globalization.StringInfo.SubstringByTextElements%2A> method to get information about the Unicode text characters that make up a string.</span></span>  
  
 [!code-vb[VbVbalrStrings#76](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStrings/VB/Class4.vb#76)]  
  
## <a name="see-also"></a><span data-ttu-id="1c50c-113">请参阅</span><span class="sxs-lookup"><span data-stu-id="1c50c-113">See also</span></span>

- <xref:System.String.Chars%2A>
- <xref:System.Globalization.StringInfo?displayProperty=nameWithType>
- [<span data-ttu-id="1c50c-114">如何：访问字符串中的字符</span><span class="sxs-lookup"><span data-stu-id="1c50c-114">How to: Access Characters in Strings</span></span>](how-to-access-characters-in-strings.md)
- [<span data-ttu-id="1c50c-115">Visual Basic 中字符串和其他数据类型间的转换</span><span class="sxs-lookup"><span data-stu-id="1c50c-115">Converting Between Strings and Other Data Types in Visual Basic</span></span>](converting-between-strings-and-other-data-types.md)
- [<span data-ttu-id="1c50c-116">字符串</span><span class="sxs-lookup"><span data-stu-id="1c50c-116">Strings</span></span>](index.md)
