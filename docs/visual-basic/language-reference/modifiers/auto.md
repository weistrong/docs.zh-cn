---
description: '了解详细信息：自动 (Visual Basic) '
title: 自动
ms.date: 07/20/2015
f1_keywords:
- vb.Auto
helpviewer_keywords:
- Auto keyword [Visual Basic], external references
- Declare statement [Visual Basic], marshaling strings
- Auto keyword [Visual Basic]
- Auto keyword [Visual Basic], marshaling strings
ms.assetid: bf79ba95-a62c-48a5-916f-0ac7a52c13ec
ms.openlocfilehash: 9601b6c253d4366c453950b4d8f3c5b2caf3805f
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99774676"
---
# <a name="auto-visual-basic"></a><span data-ttu-id="fbfe3-103">Auto (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="fbfe3-103">Auto (Visual Basic)</span></span>

<span data-ttu-id="fbfe3-104">指定 Visual Basic 应根据正在声明的外部过程的外部名称按 .NET Framework 规则封送字符串。</span><span class="sxs-lookup"><span data-stu-id="fbfe3-104">Specifies that Visual Basic should marshal strings according to .NET Framework rules based on the external name of the external procedure being declared.</span></span>  
  
 <span data-ttu-id="fbfe3-105">调用在项目外部定义的过程时，Visual Basic 编译器不能访问正确调用过程所必须具有的信息。</span><span class="sxs-lookup"><span data-stu-id="fbfe3-105">When you call a procedure defined outside your project, the Visual Basic compiler does not have access to the information it must have to call the procedure correctly.</span></span> <span data-ttu-id="fbfe3-106">此信息包括过程的位置、标识方法、调用序列和返回类型，以及它使用的字符串字符集。</span><span class="sxs-lookup"><span data-stu-id="fbfe3-106">This information includes where the procedure is located, how it is identified, its calling sequence and return type, and the string character set it uses.</span></span> <span data-ttu-id="fbfe3-107">[Declare 语句](../statements/declare-statement.md)创建对外部过程的引用并提供此必要信息。</span><span class="sxs-lookup"><span data-stu-id="fbfe3-107">The [Declare Statement](../statements/declare-statement.md) creates a reference to an external procedure and supplies this necessary information.</span></span>  
  
 <span data-ttu-id="fbfe3-108">`charsetmodifier`语句中的部分 `Declare` 提供在调用外部过程期间封送处理字符串的字符集信息。</span><span class="sxs-lookup"><span data-stu-id="fbfe3-108">The `charsetmodifier` part in the `Declare` statement supplies the character set information for marshaling strings during a call to the external procedure.</span></span> <span data-ttu-id="fbfe3-109">它还会影响 Visual Basic 搜索外部文件的外部过程名称的方式。</span><span class="sxs-lookup"><span data-stu-id="fbfe3-109">It also affects how Visual Basic searches the external file for the external procedure name.</span></span> <span data-ttu-id="fbfe3-110">`Auto`修饰符指定 Visual Basic 应根据 .NET Framework 规则封送字符串，并且应确定运行时平台的基本字符集，并可能在初始搜索失败时修改外部过程名称。</span><span class="sxs-lookup"><span data-stu-id="fbfe3-110">The `Auto` modifier specifies that Visual Basic should marshal strings according to .NET Framework rules, and that it should determine the base character set of the run-time platform and possibly modify the external procedure name if the initial search fails.</span></span> <span data-ttu-id="fbfe3-111">有关详细信息，请参阅 [Declare 语句](../statements/declare-statement.md)中的 "字符集"。</span><span class="sxs-lookup"><span data-stu-id="fbfe3-111">For more information, see "Character Sets" in [Declare Statement](../statements/declare-statement.md).</span></span>  
  
 <span data-ttu-id="fbfe3-112">如果未指定字符集修饰符， `Ansi` 则默认为。</span><span class="sxs-lookup"><span data-stu-id="fbfe3-112">If no character set modifier is specified, `Ansi` is the default.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="fbfe3-113">备注</span><span class="sxs-lookup"><span data-stu-id="fbfe3-113">Remarks</span></span>  

 <span data-ttu-id="fbfe3-114">`Auto`可以在此上下文中使用修饰符：</span><span class="sxs-lookup"><span data-stu-id="fbfe3-114">The `Auto` modifier can be used in this context:</span></span>  
  
 [<span data-ttu-id="fbfe3-115">Declare Statement</span><span class="sxs-lookup"><span data-stu-id="fbfe3-115">Declare Statement</span></span>](../statements/declare-statement.md)  
  
## <a name="smart-device-developer-notes"></a><span data-ttu-id="fbfe3-116">智能设备开发人员说明</span><span class="sxs-lookup"><span data-stu-id="fbfe3-116">Smart Device Developer Notes</span></span>  

 <span data-ttu-id="fbfe3-117">不支持此关键字。</span><span class="sxs-lookup"><span data-stu-id="fbfe3-117">This keyword is not supported.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="fbfe3-118">请参阅</span><span class="sxs-lookup"><span data-stu-id="fbfe3-118">See also</span></span>

- [<span data-ttu-id="fbfe3-119">Ansi</span><span class="sxs-lookup"><span data-stu-id="fbfe3-119">Ansi</span></span>](ansi.md)
- [<span data-ttu-id="fbfe3-120">Unicode</span><span class="sxs-lookup"><span data-stu-id="fbfe3-120">Unicode</span></span>](unicode.md)
- [<span data-ttu-id="fbfe3-121">关键字</span><span class="sxs-lookup"><span data-stu-id="fbfe3-121">Keywords</span></span>](../keywords/index.md)
