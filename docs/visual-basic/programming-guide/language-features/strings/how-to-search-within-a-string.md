---
description: '了解有关详细信息，请参阅如何：在字符串 (Visual Basic 中搜索) '
title: 如何：在字符串内搜索
ms.date: 07/20/2015
helpviewer_keywords:
- strings [Visual Basic], finding
- strings [Visual Basic], searching
- examples [Visual Basic], strings
ms.assetid: ae4c79e0-08ea-489f-bdb2-5eb6d355f284
ms.openlocfilehash: dab9faf91eef2e6d845805693227e1a6735ec796
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100429723"
---
# <a name="how-to-search-within-a-string-visual-basic"></a><span data-ttu-id="43093-103">如何：在字符串 (Visual Basic 中搜索) </span><span class="sxs-lookup"><span data-stu-id="43093-103">How to: search within a string (Visual Basic)</span></span>

<span data-ttu-id="43093-104">本文举例说明如何在 Visual Basic 中的字符串内进行搜索。</span><span class="sxs-lookup"><span data-stu-id="43093-104">This article shows an example of how to search within a string in Visual Basic.</span></span>

## <a name="example"></a><span data-ttu-id="43093-105">示例</span><span class="sxs-lookup"><span data-stu-id="43093-105">Example</span></span>

<span data-ttu-id="43093-106">此示例对 <xref:System.String.IndexOf%2A> 对象调用方法 <xref:System.String> ，以报告子字符串的第一个匹配项的索引：</span><span class="sxs-lookup"><span data-stu-id="43093-106">This example calls the <xref:System.String.IndexOf%2A> method on a <xref:System.String> object to report the index of the first occurrence of a substring:</span></span>

 [!code-vb[VbVbalrStrings#71](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStrings/VB/Class2.vb#71)]

## <a name="robust-programming"></a><span data-ttu-id="43093-107">可靠编程</span><span class="sxs-lookup"><span data-stu-id="43093-107">Robust programming</span></span>

<span data-ttu-id="43093-108"><xref:System.String.IndexOf%2A>方法返回子字符串的第一个匹配项的第一个字符的位置。</span><span class="sxs-lookup"><span data-stu-id="43093-108">The <xref:System.String.IndexOf%2A> method returns the location of the first character of the first occurrence of the substring.</span></span> <span data-ttu-id="43093-109">索引从0开始，这意味着字符串的第一个字符的索引为0。</span><span class="sxs-lookup"><span data-stu-id="43093-109">The index is 0-based, which means the first character of a string has an index of 0.</span></span>

<span data-ttu-id="43093-110">如果 <xref:System.String.IndexOf%2A> 未找到子字符串，则返回-1。</span><span class="sxs-lookup"><span data-stu-id="43093-110">If <xref:System.String.IndexOf%2A> does not find the substring, it returns -1.</span></span>

<span data-ttu-id="43093-111"><xref:System.String.IndexOf%2A>方法区分大小写，并使用当前区域性。</span><span class="sxs-lookup"><span data-stu-id="43093-111">The <xref:System.String.IndexOf%2A> method is case-sensitive and uses the current culture.</span></span>

<span data-ttu-id="43093-112">为了获得最佳的错误控制，你可能需要将字符串搜索置于 `Try` [Try .。。Catch .。。Finally 语句](../../../language-reference/statements/try-catch-finally-statement.md) 构造。</span><span class="sxs-lookup"><span data-stu-id="43093-112">For optimal error control, you might want to enclose the string search in the `Try` block of a [Try...Catch...Finally Statement](../../../language-reference/statements/try-catch-finally-statement.md) construction.</span></span>

## <a name="see-also"></a><span data-ttu-id="43093-113">另请参阅</span><span class="sxs-lookup"><span data-stu-id="43093-113">See also</span></span>

- <xref:System.String.IndexOf%2A>
- [<span data-ttu-id="43093-114">Try...Catch...Finally 语句</span><span class="sxs-lookup"><span data-stu-id="43093-114">Try...Catch...Finally Statement</span></span>](../../../language-reference/statements/try-catch-finally-statement.md)
- [<span data-ttu-id="43093-115">字符串介绍 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="43093-115">Introduction to Strings in Visual Basic</span></span>](introduction-to-strings.md)
- [<span data-ttu-id="43093-116">字符串</span><span class="sxs-lookup"><span data-stu-id="43093-116">Strings</span></span>](index.md)
