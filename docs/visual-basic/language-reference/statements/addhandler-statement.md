---
description: 了解详细信息： AddHandler 语句
title: AddHandler 语句
ms.date: 07/20/2015
f1_keywords:
- vb.AddHandlerMethod
- addhandler
- vb.addhandler
helpviewer_keywords:
- AddHandler statement [Visual Basic]
ms.assetid: cfe69799-2a0f-42c0-a99e-09fed954da01
ms.openlocfilehash: c0c34abd7ff225765ab36278825a555e2b84b0d1
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99674098"
---
# <a name="addhandler-statement"></a><span data-ttu-id="8aa11-103">AddHandler 语句</span><span class="sxs-lookup"><span data-stu-id="8aa11-103">AddHandler Statement</span></span>

<span data-ttu-id="8aa11-104">在运行时将事件与事件处理程序相关联。</span><span class="sxs-lookup"><span data-stu-id="8aa11-104">Associates an event with an event handler at run time.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="8aa11-105">语法</span><span class="sxs-lookup"><span data-stu-id="8aa11-105">Syntax</span></span>  
  
```vb  
AddHandler event, AddressOf eventhandler  
```  
  
## <a name="parts"></a><span data-ttu-id="8aa11-106">组成部分</span><span class="sxs-lookup"><span data-stu-id="8aa11-106">Parts</span></span>  

|||
|---|---|
|<span data-ttu-id="8aa11-107">event</span><span class="sxs-lookup"><span data-stu-id="8aa11-107">event</span></span>|<span data-ttu-id="8aa11-108">要处理的事件的名称。</span><span class="sxs-lookup"><span data-stu-id="8aa11-108">The name of the event to handle.</span></span>|  
|`eventhandler`|<span data-ttu-id="8aa11-109">处理事件的过程的名称。</span><span class="sxs-lookup"><span data-stu-id="8aa11-109">The name of a procedure that handles the event.</span></span>|
|||
  
## <a name="remarks"></a><span data-ttu-id="8aa11-110">备注</span><span class="sxs-lookup"><span data-stu-id="8aa11-110">Remarks</span></span>  

 <span data-ttu-id="8aa11-111">`AddHandler`和 `RemoveHandler` 语句允许您在程序执行过程中随时启动和停止事件处理。</span><span class="sxs-lookup"><span data-stu-id="8aa11-111">The `AddHandler` and `RemoveHandler` statements allow you to start and stop event handling at any time during program execution.</span></span>  
  
 <span data-ttu-id="8aa11-112">过程的签名 `eventhandler` 必须与事件的签名相匹配 `event` 。</span><span class="sxs-lookup"><span data-stu-id="8aa11-112">The signature of the `eventhandler` procedure must match the signature of the event `event`.</span></span>  
  
 <span data-ttu-id="8aa11-113">`Handles` 关键字和 `AddHandler` 语句都允许你指定特定过程处理特定事件，但存在差异。</span><span class="sxs-lookup"><span data-stu-id="8aa11-113">The `Handles` keyword and the `AddHandler` statement both allow you to specify that particular procedures handle particular events, but there are differences.</span></span> <span data-ttu-id="8aa11-114">`AddHandler` 语句在运行时将过程连接到事件。</span><span class="sxs-lookup"><span data-stu-id="8aa11-114">The `AddHandler` statement connects procedures to events at run time.</span></span> <span data-ttu-id="8aa11-115">定义过程时使用 `Handles` 关键字，以指定它处理特定事件。</span><span class="sxs-lookup"><span data-stu-id="8aa11-115">Use the `Handles` keyword when defining a procedure to specify that it handles a particular event.</span></span> <span data-ttu-id="8aa11-116">有关详细信息，请参阅 [句柄](handles-clause.md)。</span><span class="sxs-lookup"><span data-stu-id="8aa11-116">For more information, see [Handles](handles-clause.md).</span></span>  
  
> [!NOTE]
> <span data-ttu-id="8aa11-117">对于自定义事件，该 `AddHandler` 语句将调用事件的 `AddHandler` 访问器。</span><span class="sxs-lookup"><span data-stu-id="8aa11-117">For custom events, the `AddHandler` statement invokes the event's `AddHandler` accessor.</span></span> <span data-ttu-id="8aa11-118">有关自定义事件的详细信息，请参阅 [Event 语句](event-statement.md)。</span><span class="sxs-lookup"><span data-stu-id="8aa11-118">For more information on custom events, see [Event Statement](event-statement.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="8aa11-119">示例</span><span class="sxs-lookup"><span data-stu-id="8aa11-119">Example</span></span>  

 [!code-vb[VbVbalrEvents#17](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrEvents/VB/Class1.vb#17)]  
  
## <a name="see-also"></a><span data-ttu-id="8aa11-120">请参阅</span><span class="sxs-lookup"><span data-stu-id="8aa11-120">See also</span></span>

- [<span data-ttu-id="8aa11-121">RemoveHandler 语句</span><span class="sxs-lookup"><span data-stu-id="8aa11-121">RemoveHandler Statement</span></span>](removehandler-statement.md)
- [<span data-ttu-id="8aa11-122">句柄数</span><span class="sxs-lookup"><span data-stu-id="8aa11-122">Handles</span></span>](handles-clause.md)
- [<span data-ttu-id="8aa11-123">Event 语句</span><span class="sxs-lookup"><span data-stu-id="8aa11-123">Event Statement</span></span>](event-statement.md)
- [<span data-ttu-id="8aa11-124">事件</span><span class="sxs-lookup"><span data-stu-id="8aa11-124">Events</span></span>](../../programming-guide/language-features/events/index.md)
