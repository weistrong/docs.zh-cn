---
description: '了解有关详细信息，请参阅如何：从 Char 值的数组创建字符串 (Visual Basic) '
title: 如何：从 Char 值的数组创建字符串
ms.date: 07/20/2015
helpviewer_keywords:
- examples [Visual Basic], arrays
- examples [Visual Basic], Char data type
ms.assetid: 69f94e85-d57c-4ccc-a62a-426e829f5c5e
ms.openlocfilehash: 67b675f5f02c92b785e374b99f49248d43d12fb4
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100429827"
---
# <a name="how-to-create-a-string-from-an-array-of-char-values-visual-basic"></a><span data-ttu-id="817db-103">如何：从 Char 值的数组创建字符串 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="817db-103">How to: Create a String from An Array of Char Values (Visual Basic)</span></span>

<span data-ttu-id="817db-104">此示例从单个字符创建字符串 "abcd"。</span><span class="sxs-lookup"><span data-stu-id="817db-104">This example creates the string "abcd" from individual characters.</span></span>  
  
## <a name="example"></a><span data-ttu-id="817db-105">示例</span><span class="sxs-lookup"><span data-stu-id="817db-105">Example</span></span>  

 [!code-vb[VbVbalrStrings#61](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStrings/VB/Class2.vb#61)]  
  
## <a name="compile-the-code"></a><span data-ttu-id="817db-106">编译代码</span><span class="sxs-lookup"><span data-stu-id="817db-106">Compile the code</span></span>  

 <span data-ttu-id="817db-107">此方法没有特殊要求。</span><span class="sxs-lookup"><span data-stu-id="817db-107">This method has no special requirements.</span></span>  
  
 <span data-ttu-id="817db-108">语法 `"a"c` （其中单个 `c` 字符后跟引号中的单个字符）用于创建字符文本。</span><span class="sxs-lookup"><span data-stu-id="817db-108">The syntax `"a"c`, where a single `c` follows a single character in quotation marks, is used to create a character literal.</span></span>  
  
## <a name="robust-programming"></a><span data-ttu-id="817db-109">可靠编程</span><span class="sxs-lookup"><span data-stu-id="817db-109">Robust Programming</span></span>  

 <span data-ttu-id="817db-110">Null 字符 (等效于 `Chr(0)` 字符串中的) 在使用字符串时导致意外的结果。</span><span class="sxs-lookup"><span data-stu-id="817db-110">Null characters (equivalent to `Chr(0)`) in the string lead to unexpected results when using the string.</span></span> <span data-ttu-id="817db-111">字符串中将包含 null 字符，但在某些情况下，将不会显示空字符后面的字符。</span><span class="sxs-lookup"><span data-stu-id="817db-111">The null character will be included with the string, but characters following the null character will not be displayed in some situations.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="817db-112">请参阅</span><span class="sxs-lookup"><span data-stu-id="817db-112">See also</span></span>

- <xref:System.String>
- [<span data-ttu-id="817db-113">Char 数据类型</span><span class="sxs-lookup"><span data-stu-id="817db-113">Char Data Type</span></span>](../../../language-reference/data-types/char-data-type.md)
- [<span data-ttu-id="817db-114">数据类型</span><span class="sxs-lookup"><span data-stu-id="817db-114">Data Types</span></span>](../data-types/index.md)
