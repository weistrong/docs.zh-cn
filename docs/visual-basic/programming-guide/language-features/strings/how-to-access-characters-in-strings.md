---
description: 了解有关详细信息，请参阅如何：在 Visual Basic 中的字符串中访问字符
title: 如何：访问字符串中的字符
ms.date: 07/20/2015
helpviewer_keywords:
- strings [Visual Basic], accessing characters
- characters [Visual Basic], accessing in strings
ms.assetid: 02c5206c-ffab-494d-b648-3b2ea358dc34
ms.openlocfilehash: 373005699483dbae92df3a6fe73cc9b6318a9c61
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100476158"
---
# <a name="how-to-access-characters-in-strings-in-visual-basic"></a><span data-ttu-id="d6842-103">如何：在 Visual Basic 中访问字符串中的字符</span><span class="sxs-lookup"><span data-stu-id="d6842-103">How to: Access Characters in Strings in Visual Basic</span></span>

<span data-ttu-id="d6842-104">此示例演示如何使用 <xref:System.String.Chars%2A> 属性访问字符串中指定位置处的字符。</span><span class="sxs-lookup"><span data-stu-id="d6842-104">This example demonstrates how to use the <xref:System.String.Chars%2A> property to access the character at the specified location in a string.</span></span>  
  
## <a name="example"></a><span data-ttu-id="d6842-105">示例</span><span class="sxs-lookup"><span data-stu-id="d6842-105">Example</span></span>  

 <span data-ttu-id="d6842-106">有时，请在字符串中包含有关字符串中的字符和这些字符的位置的数据。</span><span class="sxs-lookup"><span data-stu-id="d6842-106">Sometimes it is useful to have data about the characters in your string and the positions of those characters within your string.</span></span> <span data-ttu-id="d6842-107">你可以将字符串视为)  (实例的字符数组 `Char` ; 你可以通过属性引用该字符的索引来检索特定字符 <xref:System.String.Chars%2A> 。</span><span class="sxs-lookup"><span data-stu-id="d6842-107">You can think of a string as an array of characters (`Char` instances); you can retrieve a particular character by referencing the index of that character through the <xref:System.String.Chars%2A> property.</span></span>  
  
 [!code-vb[VbVbalrStrings#49](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStrings/VB/Class2.vb#49)]  
  
 <span data-ttu-id="d6842-108">`index`属性的参数 <xref:System.String.Chars%2A> 是从零开始的。</span><span class="sxs-lookup"><span data-stu-id="d6842-108">The `index` parameter of the <xref:System.String.Chars%2A> property is zero-based.</span></span>  
  
## <a name="robust-programming"></a><span data-ttu-id="d6842-109">可靠编程</span><span class="sxs-lookup"><span data-stu-id="d6842-109">Robust Programming</span></span>  

 <span data-ttu-id="d6842-110"><xref:System.String.Chars%2A>属性返回指定位置处的字符。</span><span class="sxs-lookup"><span data-stu-id="d6842-110">The <xref:System.String.Chars%2A> property returns the character at the specified position.</span></span> <span data-ttu-id="d6842-111">但是，某些 Unicode 字符可以由多个字符表示。</span><span class="sxs-lookup"><span data-stu-id="d6842-111">However, some Unicode characters can be represented by more than one character.</span></span> <span data-ttu-id="d6842-112">有关如何使用 Unicode 字符的详细信息，请参阅 [如何：将字符串转换为字符数组](how-to-convert-a-string-to-an-array-of-characters.md)。</span><span class="sxs-lookup"><span data-stu-id="d6842-112">For more information on how to work with Unicode characters, see [How to: Convert a String to an Array of Characters](how-to-convert-a-string-to-an-array-of-characters.md).</span></span>  
  
 <span data-ttu-id="d6842-113"><xref:System.String.Chars%2A> <xref:System.IndexOutOfRangeException> 如果 `index` 参数大于或等于字符串的长度，则属性引发异常; 如果小于零，则引发异常。</span><span class="sxs-lookup"><span data-stu-id="d6842-113">The <xref:System.String.Chars%2A> property throws an <xref:System.IndexOutOfRangeException> exception if the `index` parameter is greater than or equal to the length of the string, or if it is less than zero</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d6842-114">请参阅</span><span class="sxs-lookup"><span data-stu-id="d6842-114">See also</span></span>

- <xref:System.String.Chars%2A>
- [<span data-ttu-id="d6842-115">如何：将字符串转换为字符数组</span><span class="sxs-lookup"><span data-stu-id="d6842-115">How to: Convert a String to an Array of Characters</span></span>](how-to-convert-a-string-to-an-array-of-characters.md)
- [<span data-ttu-id="d6842-116">Visual Basic 中字符串和其他数据类型间的转换</span><span class="sxs-lookup"><span data-stu-id="d6842-116">Converting Between Strings and Other Data Types in Visual Basic</span></span>](converting-between-strings-and-other-data-types.md)
- [<span data-ttu-id="d6842-117">字符串</span><span class="sxs-lookup"><span data-stu-id="d6842-117">Strings</span></span>](index.md)
