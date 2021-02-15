---
description: 了解有关详细信息，请参阅如何：在 Visual Basic 中循环访问枚举
title: 如何：循环访问枚举
ms.date: 07/20/2015
helpviewer_keywords:
- arrays [Visual Basic], iterating
- enumerations [Visual Basic], iterating
- ListBox control [Windows Forms], populating from an enumeration
ms.assetid: e5aa10eb-cfcd-4a3b-8e76-f06b8f2002be
ms.openlocfilehash: a14d65a33e8a2f7872203a6a332dec1e753704f8
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100471560"
---
# <a name="how-to-iterate-through-an-enumeration-in-visual-basic"></a><span data-ttu-id="0fe74-103">如何：在 Visual Basic 中循环访问枚举</span><span class="sxs-lookup"><span data-stu-id="0fe74-103">How to: Iterate Through An Enumeration in Visual Basic</span></span>

<span data-ttu-id="0fe74-104">枚举提供了使用相关常量集以及将常量值与名称相关联的一个便捷方法。</span><span class="sxs-lookup"><span data-stu-id="0fe74-104">Enumerations provide a convenient way to work with sets of related constants, and to associate constant values with names.</span></span> <span data-ttu-id="0fe74-105">若要循环访问枚举，可以使用方法将它移动到数组中 <xref:System.Enum.GetValues%2A> 。</span><span class="sxs-lookup"><span data-stu-id="0fe74-105">To iterate through an enumeration, you can move it into an array using the <xref:System.Enum.GetValues%2A> method.</span></span> <span data-ttu-id="0fe74-106">你还可以使用语句来循环访问枚举 `For...Each` ，方法是使用 <xref:System.Enum.GetNames%2A> 或 <xref:System.Enum.GetValues%2A> 方法来提取字符串或数字值。</span><span class="sxs-lookup"><span data-stu-id="0fe74-106">You could also iterate through an enumeration using a `For...Each` statement, using the <xref:System.Enum.GetNames%2A> or <xref:System.Enum.GetValues%2A> method to extract the string or numeric value.</span></span>  
  
### <a name="to-iterate-through-an-enumeration"></a><span data-ttu-id="0fe74-107">循环访问枚举</span><span class="sxs-lookup"><span data-stu-id="0fe74-107">To iterate through an enumeration</span></span>  
  
- <span data-ttu-id="0fe74-108">声明一个数组，然后使用方法将枚举转换为它，就 <xref:System.Enum.GetValues%2A> 像传递任何其他变量一样。</span><span class="sxs-lookup"><span data-stu-id="0fe74-108">Declare an array and convert the enumeration to it with the <xref:System.Enum.GetValues%2A> method before passing the array as you would any other variable.</span></span> <span data-ttu-id="0fe74-109">下面的示例在 <xref:Microsoft.VisualBasic.FirstDayOfWeek> 循环访问枚举时显示枚举的每个成员。</span><span class="sxs-lookup"><span data-stu-id="0fe74-109">The following example displays each member of the enumeration <xref:Microsoft.VisualBasic.FirstDayOfWeek> as it iterates through the enumeration.</span></span>  
  
     [!code-vb[VbEnumsTask#7](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbEnumsTask/VB/Class2.vb#7)]  
  
## <a name="see-also"></a><span data-ttu-id="0fe74-110">请参阅</span><span class="sxs-lookup"><span data-stu-id="0fe74-110">See also</span></span>

- [<span data-ttu-id="0fe74-111">枚举概述</span><span class="sxs-lookup"><span data-stu-id="0fe74-111">Enumerations Overview</span></span>](enumerations-overview.md)
- [<span data-ttu-id="0fe74-112">如何：声明枚举</span><span class="sxs-lookup"><span data-stu-id="0fe74-112">How to: Declare an Enumeration</span></span>](how-to-declare-enumerations.md)
- [<span data-ttu-id="0fe74-113">何时使用枚举</span><span class="sxs-lookup"><span data-stu-id="0fe74-113">When to Use an Enumeration</span></span>](when-to-use-an-enumeration.md)
- [<span data-ttu-id="0fe74-114">如何：确定与枚举值关联的字符串</span><span class="sxs-lookup"><span data-stu-id="0fe74-114">How to: Determine the String Associated with an Enumeration Value</span></span>](how-to-determine-the-string-associated-with-an-enumeration-value.md)
- [<span data-ttu-id="0fe74-115">如何：引用枚举成员</span><span class="sxs-lookup"><span data-stu-id="0fe74-115">How to: Refer to an Enumeration Member</span></span>](how-to-refer-to-an-enumeration-member.md)
- [<span data-ttu-id="0fe74-116">枚举和名称限定</span><span class="sxs-lookup"><span data-stu-id="0fe74-116">Enumerations and Name Qualification</span></span>](enumerations-and-name-qualification.md)
- [<span data-ttu-id="0fe74-117">数组</span><span class="sxs-lookup"><span data-stu-id="0fe74-117">Arrays</span></span>](../arrays/index.md)
