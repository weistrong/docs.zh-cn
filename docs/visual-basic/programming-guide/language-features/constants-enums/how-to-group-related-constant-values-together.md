---
description: '了解有关详细信息，请参阅如何：将相关的常量值组合在一起 (Visual Basic) '
title: 如何：将相关的常量值组合在一起
ms.date: 07/20/2015
helpviewer_keywords:
- enumerations [Visual Basic], constants
- constants [Visual Basic], grouping together
ms.assetid: 09d61da5-c940-4126-a79f-ba93c36653dc
ms.openlocfilehash: ddd60696d2c751810e49ecbcb537589bedc58abf
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100471586"
---
# <a name="how-to-group-related-constant-values-together-visual-basic"></a><span data-ttu-id="10c66-103">如何：将相关的常量值组合在一起 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="10c66-103">How to: Group Related Constant Values Together (Visual Basic)</span></span>

<span data-ttu-id="10c66-104">枚举是将相关常量组合在一起的最佳方式。</span><span class="sxs-lookup"><span data-stu-id="10c66-104">An enumeration is the best way to group related constants together.</span></span> <span data-ttu-id="10c66-105">使用 `Enum` 类或模块的声明部分中的语句创建枚举。</span><span class="sxs-lookup"><span data-stu-id="10c66-105">You create an enumeration with the `Enum` statement in the declarations section of a class or a module.</span></span> <span data-ttu-id="10c66-106">有关详细信息，请参阅 [如何：声明枚举](how-to-declare-enumerations.md)。</span><span class="sxs-lookup"><span data-stu-id="10c66-106">For more information, see [How to: Declare an Enumeration](how-to-declare-enumerations.md).</span></span>  
  
### <a name="to-group-related-constant-values"></a><span data-ttu-id="10c66-107">对相关常数值分组</span><span class="sxs-lookup"><span data-stu-id="10c66-107">To group related constant values</span></span>  
  
1. <span data-ttu-id="10c66-108">编写包含代码访问级别、 `Enum` 关键字和有效名称的声明。</span><span class="sxs-lookup"><span data-stu-id="10c66-108">Write a declaration that includes a code access level, the `Enum` keyword, and a valid name.</span></span> <span data-ttu-id="10c66-109">此示例创建 `Private` 枚举 `temperatureValues` 。</span><span class="sxs-lookup"><span data-stu-id="10c66-109">This example creates the `Private` enumeration, `temperatureValues`.</span></span>  
  
     [!code-vb[VbEnumsTask#21](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbEnumsTask/VB/Class2.vb#21)]  
  
2. <span data-ttu-id="10c66-110">定义枚举中的常量。</span><span class="sxs-lookup"><span data-stu-id="10c66-110">Define the constants in the enumeration.</span></span> <span data-ttu-id="10c66-111">此示例创建 `Public` 枚举 `temperatureValues` 并分配其值。</span><span class="sxs-lookup"><span data-stu-id="10c66-111">This example creates the `Public` enumeration `temperatureValues` and assigns its values.</span></span>  
  
     [!code-vb[VbEnumsTask#1](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbEnumsTask/VB/Class2.vb#1)]  
  
## <a name="see-also"></a><span data-ttu-id="10c66-112">请参阅</span><span class="sxs-lookup"><span data-stu-id="10c66-112">See also</span></span>

- [<span data-ttu-id="10c66-113">枚举和名称限定</span><span class="sxs-lookup"><span data-stu-id="10c66-113">Enumerations and Name Qualification</span></span>](enumerations-and-name-qualification.md)
- [<span data-ttu-id="10c66-114">如何：引用枚举成员</span><span class="sxs-lookup"><span data-stu-id="10c66-114">How to: Refer to an Enumeration Member</span></span>](how-to-refer-to-an-enumeration-member.md)
- [<span data-ttu-id="10c66-115">何时使用枚举</span><span class="sxs-lookup"><span data-stu-id="10c66-115">When to Use an Enumeration</span></span>](when-to-use-an-enumeration.md)
- [<span data-ttu-id="10c66-116">常量概述</span><span class="sxs-lookup"><span data-stu-id="10c66-116">Constants Overview</span></span>](constants-overview.md)
- [<span data-ttu-id="10c66-117">常数和文本数据类型</span><span class="sxs-lookup"><span data-stu-id="10c66-117">Constant and Literal Data Types</span></span>](constant-and-literal-data-types.md)
- [<span data-ttu-id="10c66-118">常量和枚举</span><span class="sxs-lookup"><span data-stu-id="10c66-118">Constants and Enumerations</span></span>](../../../language-reference/constants-and-enumerations.md)
