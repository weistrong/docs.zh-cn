---
description: '了解详细信息：如何：将十六进制字符串转换为数字 (Visual Basic) '
title: 如何：将十六进制字符串转换为数字
ms.date: 01/31/2018
helpviewer_keywords:
- numbers [Visual Basic], hexadecimals
- hexadecimals [Visual Basic], decimals
- examples [Visual Basic], string conversion
- decimals [Visual Basic], hexadecimals
- string conversion [Visual Basic], hexadecimal to numbers
ms.assetid: 76675807-eadb-4c08-bd50-e6c6ff4b8ced
ms.openlocfilehash: cf1648b5f85f189f203f56cf569041e4f2db5ac3
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100425538"
---
# <a name="how-to-convert-hexadecimal-strings-to-numbers-visual-basic"></a><span data-ttu-id="a1755-103">如何：将十六进制字符串转换为数字 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="a1755-103">How to: Convert Hexadecimal Strings to Numbers (Visual Basic)</span></span>

<span data-ttu-id="a1755-104">此示例使用方法将十六进制字符串转换为整数 <xref:System.Convert.ToInt32%2A?displayProperty=nameWithType> 。</span><span class="sxs-lookup"><span data-stu-id="a1755-104">This example converts a hexadecimal string to an integer using the <xref:System.Convert.ToInt32%2A?displayProperty=nameWithType> method.</span></span>

## <a name="to-convert-a-hexadecimal-string-to-a-number"></a><span data-ttu-id="a1755-105">将十六进制字符串转换为数字</span><span class="sxs-lookup"><span data-stu-id="a1755-105">To convert a hexadecimal string to a number</span></span>

- <span data-ttu-id="a1755-106">使用 <xref:System.Convert.ToInt32(System.String,System.Int32)> 方法将以16为基数的数字转换为整数。</span><span class="sxs-lookup"><span data-stu-id="a1755-106">Use the <xref:System.Convert.ToInt32(System.String,System.Int32)> method to convert the number expressed in base-16 to an integer.</span></span>

  <span data-ttu-id="a1755-107">该方法的第一个参数 <xref:System.Convert.ToInt32(System.String,System.Int32)> 是要转换的字符串。</span><span class="sxs-lookup"><span data-stu-id="a1755-107">The first argument of the <xref:System.Convert.ToInt32(System.String,System.Int32)> method is the string to convert.</span></span> <span data-ttu-id="a1755-108">第二个参数描述数字的表示形式;十六进制以16为基数。</span><span class="sxs-lookup"><span data-stu-id="a1755-108">The second argument describes what base the number is expressed in; hexadecimal is base 16.</span></span>

  [!code-vb[VbVbalrStrings#62](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStrings/VB/Class2.vb#62)]

- <span data-ttu-id="a1755-109">请注意，十六进制字符串具有以下限制：</span><span class="sxs-lookup"><span data-stu-id="a1755-109">Note that the hexadecimal string has the following restrictions:</span></span>

  - <span data-ttu-id="a1755-110">它不能包含 `&h` 前缀。</span><span class="sxs-lookup"><span data-stu-id="a1755-110">It cannot include the `&h` prefix.</span></span>
  - <span data-ttu-id="a1755-111">它不能包含 `_` 数字分隔符。</span><span class="sxs-lookup"><span data-stu-id="a1755-111">It cannot include the `_` digit separator.</span></span>

  <span data-ttu-id="a1755-112">如果前缀或数字分隔符存在，则对方法的调用将 <xref:System.Convert.ToInt32(System.String,System.Int32)> 引发 <xref:System.FormatException> 。</span><span class="sxs-lookup"><span data-stu-id="a1755-112">If the prefix or a digit separator is present, the call to the <xref:System.Convert.ToInt32(System.String,System.Int32)> method throws a <xref:System.FormatException>.</span></span>

## <a name="see-also"></a><span data-ttu-id="a1755-113">请参阅</span><span class="sxs-lookup"><span data-stu-id="a1755-113">See also</span></span>

- <xref:Microsoft.VisualBasic.Conversion.Hex%2A>
- <xref:System.Convert.ToInt32%2A?displayProperty=nameWithType>
