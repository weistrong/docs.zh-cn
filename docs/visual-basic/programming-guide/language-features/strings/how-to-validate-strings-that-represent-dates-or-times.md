---
description: '了解有关详细信息，请参阅如何：验证表示日期或时间的字符串 (Visual Basic) '
title: 如何：验证表示日期或时间的字符串
ms.date: 07/20/2015
helpviewer_keywords:
- strings [Visual Basic], validating
- String data type [Visual Basic], validation
ms.assetid: ae7d4b29-3436-4032-bdbf-4650eb1c8e19
ms.openlocfilehash: 4e9255717d1711d8e9839c218a78b359549d9eef
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100424250"
---
# <a name="how-to-validate-strings-that-represent-dates-or-times-visual-basic"></a><span data-ttu-id="b2a7d-103">如何：验证表示日期或时间的字符串 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="b2a7d-103">How to: Validate Strings That Represent Dates or Times (Visual Basic)</span></span>

<span data-ttu-id="b2a7d-104">下面的代码示例设置一个 `Boolean` 值，该值指示字符串是否表示有效的日期或时间。</span><span class="sxs-lookup"><span data-stu-id="b2a7d-104">The following code example sets a `Boolean` value that indicates whether a string represents a valid date or time.</span></span>  
  
## <a name="example"></a><span data-ttu-id="b2a7d-105">示例</span><span class="sxs-lookup"><span data-stu-id="b2a7d-105">Example</span></span>  

 [!code-vb[VbVbcnRegEx#2](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnRegEx/VB/Class1.vb#2)]  
  
## <a name="compile-the-code"></a><span data-ttu-id="b2a7d-106">编译代码</span><span class="sxs-lookup"><span data-stu-id="b2a7d-106">Compile the code</span></span>  

 <span data-ttu-id="b2a7d-107">`("01/01/03")`将和替换为 `"9:30 PM"` 要验证的日期和时间。</span><span class="sxs-lookup"><span data-stu-id="b2a7d-107">Replace `("01/01/03")` and `"9:30 PM"` with the date and time you want to validate.</span></span> <span data-ttu-id="b2a7d-108">您可以使用 `String` 变量或返回字符串的方法（如）将字符串替换为另一个硬编码字符串 `InputBox` 。</span><span class="sxs-lookup"><span data-stu-id="b2a7d-108">You can replace the string with another hard-coded string, with a `String` variable, or with a method that returns a string, such as `InputBox`.</span></span>  
  
## <a name="robust-programming"></a><span data-ttu-id="b2a7d-109">可靠编程</span><span class="sxs-lookup"><span data-stu-id="b2a7d-109">Robust Programming</span></span>  

 <span data-ttu-id="b2a7d-110">使用此方法在尝试将转换为变量之前验证字符串 `String` `DateTime` 。</span><span class="sxs-lookup"><span data-stu-id="b2a7d-110">Use this method to validate the string before trying to convert the `String` to a `DateTime` variable.</span></span> <span data-ttu-id="b2a7d-111">首先检查日期或时间，您可以避免在运行时生成异常。</span><span class="sxs-lookup"><span data-stu-id="b2a7d-111">By checking the date or time first, you can avoid generating an exception at run time.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b2a7d-112">请参阅</span><span class="sxs-lookup"><span data-stu-id="b2a7d-112">See also</span></span>

- <xref:Microsoft.VisualBasic.Information.IsDate%2A>
- <xref:Microsoft.VisualBasic.Interaction.InputBox%2A>
- [<span data-ttu-id="b2a7d-113">验证字符串 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="b2a7d-113">Validating Strings in Visual Basic</span></span>](validating-strings.md)
