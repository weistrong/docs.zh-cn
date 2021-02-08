---
description: 了解有关以下内容的详细信息： Mid 语句
title: Mid 语句
ms.date: 07/20/2015
f1_keywords:
- vb.MidB
- vb.Mid
helpviewer_keywords:
- substrings [Visual Basic], Mid statement
- strings [Visual Basic], substrings
- Mid statement [Visual Basic]
- strings [Visual Basic], replacing
ms.assetid: 2b82d7a8-9646-4cb0-bec5-80abc98297bf
ms.openlocfilehash: 29cf933cb38fc6ef831570d0940b481abf9cfecf
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99768878"
---
# <a name="mid-statement"></a><span data-ttu-id="53557-103">Mid 语句</span><span class="sxs-lookup"><span data-stu-id="53557-103">Mid Statement</span></span>

<span data-ttu-id="53557-104">将变量中指定数量的字符替换 `String` 为另一个字符串中的字符。</span><span class="sxs-lookup"><span data-stu-id="53557-104">Replaces a specified number of characters in a `String` variable with characters from another string.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="53557-105">语法</span><span class="sxs-lookup"><span data-stu-id="53557-105">Syntax</span></span>  
  
```vb  
Mid( _  
   ByRef Target As String, _  
   ByVal Start As Integer, _  
   Optional ByVal Length As Integer _  
) = StringExpression  
```  
  
## <a name="parts"></a><span data-ttu-id="53557-106">组成部分</span><span class="sxs-lookup"><span data-stu-id="53557-106">Parts</span></span>  

 `Target`  
 <span data-ttu-id="53557-107">必需。</span><span class="sxs-lookup"><span data-stu-id="53557-107">Required.</span></span> <span data-ttu-id="53557-108">`String`要修改的变量的名称。</span><span class="sxs-lookup"><span data-stu-id="53557-108">Name of the `String` variable to modify.</span></span>  
  
 `Start`  
 <span data-ttu-id="53557-109">必需。</span><span class="sxs-lookup"><span data-stu-id="53557-109">Required.</span></span> <span data-ttu-id="53557-110">`Integer` 表达式。</span><span class="sxs-lookup"><span data-stu-id="53557-110">`Integer` expression.</span></span> <span data-ttu-id="53557-111">中 `Target` 开始替换文本的字符位置。</span><span class="sxs-lookup"><span data-stu-id="53557-111">Character position in `Target` where the replacement of text begins.</span></span> <span data-ttu-id="53557-112">`Start` 使用从1开始的索引。</span><span class="sxs-lookup"><span data-stu-id="53557-112">`Start` uses a one-based index.</span></span>  
  
 `Length`  
 <span data-ttu-id="53557-113">可选。</span><span class="sxs-lookup"><span data-stu-id="53557-113">Optional.</span></span> <span data-ttu-id="53557-114">`Integer` 表达式。</span><span class="sxs-lookup"><span data-stu-id="53557-114">`Integer` expression.</span></span> <span data-ttu-id="53557-115">要替换的字符数。</span><span class="sxs-lookup"><span data-stu-id="53557-115">Number of characters to replace.</span></span> <span data-ttu-id="53557-116">如果省略， `String` 则使用所有。</span><span class="sxs-lookup"><span data-stu-id="53557-116">If omitted, all of `String` is used.</span></span>  
  
 `StringExpression`  
 <span data-ttu-id="53557-117">必需。</span><span class="sxs-lookup"><span data-stu-id="53557-117">Required.</span></span> <span data-ttu-id="53557-118">`String` 替换部分的表达式 `Target` 。</span><span class="sxs-lookup"><span data-stu-id="53557-118">`String` expression that replaces part of `Target`.</span></span>  
  
## <a name="exceptions"></a><span data-ttu-id="53557-119">异常</span><span class="sxs-lookup"><span data-stu-id="53557-119">Exceptions</span></span>  
  
|<span data-ttu-id="53557-120">例外类型</span><span class="sxs-lookup"><span data-stu-id="53557-120">Exception type</span></span>|<span data-ttu-id="53557-121">条件</span><span class="sxs-lookup"><span data-stu-id="53557-121">Condition</span></span>|  
|--------------------|---------------|  
|<xref:System.ArgumentException>|<span data-ttu-id="53557-122">`Start` <= 0 或 `Length` < 0。</span><span class="sxs-lookup"><span data-stu-id="53557-122">`Start` <= 0 or `Length` < 0.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="53557-123">备注</span><span class="sxs-lookup"><span data-stu-id="53557-123">Remarks</span></span>  

 <span data-ttu-id="53557-124">替换的字符数始终小于或等于中的字符数 `Target` 。</span><span class="sxs-lookup"><span data-stu-id="53557-124">The number of characters replaced is always less than or equal to the number of characters in `Target`.</span></span>  
  
 <span data-ttu-id="53557-125">Visual Basic 具有 <xref:Microsoft.VisualBasic.Strings.Mid%2A> 函数和 `Mid` 语句。</span><span class="sxs-lookup"><span data-stu-id="53557-125">Visual Basic has a <xref:Microsoft.VisualBasic.Strings.Mid%2A> function and a `Mid` statement.</span></span> <span data-ttu-id="53557-126">这些元素对字符串中的指定数量的字符进行操作，但 `Mid` 当 `Mid` 语句替换这些字符时，函数将返回字符。</span><span class="sxs-lookup"><span data-stu-id="53557-126">These elements both operate on a specified number of characters in a string, but the `Mid` function returns the characters while the `Mid` statement replaces the characters.</span></span> <span data-ttu-id="53557-127">有关详细信息，请参阅 <xref:Microsoft.VisualBasic.Strings.Mid%2A>。</span><span class="sxs-lookup"><span data-stu-id="53557-127">For more information, see <xref:Microsoft.VisualBasic.Strings.Mid%2A>.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="53557-128">的 `MidB` 早期 Visual Basic 版本语句将以字节而不是字符来替换子字符串（而不是字符）。</span><span class="sxs-lookup"><span data-stu-id="53557-128">The `MidB` statement of earlier versions of Visual Basic replaces a substring in bytes, rather than characters.</span></span> <span data-ttu-id="53557-129">它主要用于在双字节字符集中将字符串转换 (DBCS) 应用程序。</span><span class="sxs-lookup"><span data-stu-id="53557-129">It is used primarily for converting strings in double-byte character set (DBCS) applications.</span></span> <span data-ttu-id="53557-130">所有 Visual Basic 字符串均采用 Unicode 格式， `MidB` 不再受支持。</span><span class="sxs-lookup"><span data-stu-id="53557-130">All Visual Basic strings are in Unicode, and `MidB` is no longer supported.</span></span>  
  
## <a name="example"></a><span data-ttu-id="53557-131">示例</span><span class="sxs-lookup"><span data-stu-id="53557-131">Example</span></span>  

 <span data-ttu-id="53557-132">此示例使用 `Mid` 语句将字符串变量中指定数量的字符替换为另一个字符串中的字符。</span><span class="sxs-lookup"><span data-stu-id="53557-132">This example uses the `Mid` statement to replace a specified number of characters in a string variable with characters from another string.</span></span>  
  
 [!code-vb[VbVbalrStrings#5](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStrings/VB/Class1.vb#5)]  
  
## <a name="requirements"></a><span data-ttu-id="53557-133">要求</span><span class="sxs-lookup"><span data-stu-id="53557-133">Requirements</span></span>  

 <span data-ttu-id="53557-134">**命名空间：** [Microsoft](../runtime-library-members.md)</span><span class="sxs-lookup"><span data-stu-id="53557-134">**Namespace:** [Microsoft.VisualBasic](../runtime-library-members.md)</span></span>  
  
 <span data-ttu-id="53557-135">**模块：**`Strings`</span><span class="sxs-lookup"><span data-stu-id="53557-135">**Module:** `Strings`</span></span>  
  
 <span data-ttu-id="53557-136">**程序集：** Microsoft.VisualBasic.dll) 中的 Visual Basic 运行时库 (</span><span class="sxs-lookup"><span data-stu-id="53557-136">**Assembly:** Visual Basic Runtime Library (in Microsoft.VisualBasic.dll)</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="53557-137">请参阅</span><span class="sxs-lookup"><span data-stu-id="53557-137">See also</span></span>

- <xref:Microsoft.VisualBasic.Strings.Mid%2A>
- [<span data-ttu-id="53557-138">字符串</span><span class="sxs-lookup"><span data-stu-id="53557-138">Strings</span></span>](../../programming-guide/language-features/strings/index.md)
- [<span data-ttu-id="53557-139">字符串介绍 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="53557-139">Introduction to Strings in Visual Basic</span></span>](../../programming-guide/language-features/strings/introduction-to-strings.md)
