---
description: 了解详细信息： RemoveHandler 语句
title: RemoveHandler 语句
ms.date: 07/20/2015
f1_keywords:
- vb.RemoveHandlerMethod
- vb.RemoveHandler
- RemoveHandler
helpviewer_keywords:
- RemoveHandler keyword [Visual Basic]
- RemoveHandler statement [Visual Basic]
ms.assetid: 647cd825-e877-4910-b4f1-8d168beebe6a
ms.openlocfilehash: 699db9edfc029b4149246e8b654645040ae6d89e
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99741297"
---
# <a name="removehandler-statement"></a><span data-ttu-id="d7d46-103">RemoveHandler 语句</span><span class="sxs-lookup"><span data-stu-id="d7d46-103">RemoveHandler Statement</span></span>

<span data-ttu-id="d7d46-104">删除事件和事件处理程序之间的关联。</span><span class="sxs-lookup"><span data-stu-id="d7d46-104">Removes the association between an event and an event handler.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d7d46-105">语法</span><span class="sxs-lookup"><span data-stu-id="d7d46-105">Syntax</span></span>  
  
```vb  
RemoveHandler event, AddressOf eventhandler  
```  
  
## <a name="parts"></a><span data-ttu-id="d7d46-106">组成部分</span><span class="sxs-lookup"><span data-stu-id="d7d46-106">Parts</span></span>  
  
|<span data-ttu-id="d7d46-107">术语</span><span class="sxs-lookup"><span data-stu-id="d7d46-107">Term</span></span>|<span data-ttu-id="d7d46-108">定义</span><span class="sxs-lookup"><span data-stu-id="d7d46-108">Definition</span></span>|  
|---|---|  
|`event`|<span data-ttu-id="d7d46-109">正在处理的事件的名称。</span><span class="sxs-lookup"><span data-stu-id="d7d46-109">The name of the event being handled.</span></span>|  
|`eventhandler`|<span data-ttu-id="d7d46-110">当前处理事件的过程的名称。</span><span class="sxs-lookup"><span data-stu-id="d7d46-110">The name of the procedure currently handling the event.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="d7d46-111">备注</span><span class="sxs-lookup"><span data-stu-id="d7d46-111">Remarks</span></span>  

 <span data-ttu-id="d7d46-112">使用 `AddHandler` 和 `RemoveHandler` 语句，可以在程序执行过程中随时启动和停止特定事件的事件处理。</span><span class="sxs-lookup"><span data-stu-id="d7d46-112">The `AddHandler` and `RemoveHandler` statements allow you to start and stop event handling for a specific event at any time during program execution.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="d7d46-113">对于自定义事件，该 `RemoveHandler` 语句将调用事件的 `RemoveHandler` 访问器。</span><span class="sxs-lookup"><span data-stu-id="d7d46-113">For custom events, the `RemoveHandler` statement invokes the event's `RemoveHandler` accessor.</span></span> <span data-ttu-id="d7d46-114">有关自定义事件的详细信息，请参阅 [Event 语句](event-statement.md)。</span><span class="sxs-lookup"><span data-stu-id="d7d46-114">For more information on custom events, see [Event Statement](event-statement.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="d7d46-115">示例</span><span class="sxs-lookup"><span data-stu-id="d7d46-115">Example</span></span>  

 [!code-vb[VbVbalrEvents#17](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrEvents/VB/Class1.vb#17)]  
  
## <a name="see-also"></a><span data-ttu-id="d7d46-116">请参阅</span><span class="sxs-lookup"><span data-stu-id="d7d46-116">See also</span></span>

- [<span data-ttu-id="d7d46-117">AddHandler 语句</span><span class="sxs-lookup"><span data-stu-id="d7d46-117">AddHandler Statement</span></span>](addhandler-statement.md)
- [<span data-ttu-id="d7d46-118">句柄数</span><span class="sxs-lookup"><span data-stu-id="d7d46-118">Handles</span></span>](handles-clause.md)
- [<span data-ttu-id="d7d46-119">Event 语句</span><span class="sxs-lookup"><span data-stu-id="d7d46-119">Event Statement</span></span>](event-statement.md)
- [<span data-ttu-id="d7d46-120">事件</span><span class="sxs-lookup"><span data-stu-id="d7d46-120">Events</span></span>](../../programming-guide/language-features/events/index.md)
