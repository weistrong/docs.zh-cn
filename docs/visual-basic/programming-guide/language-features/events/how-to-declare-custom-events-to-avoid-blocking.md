---
description: '了解有关详细信息，请参阅如何：声明自定义事件以避免阻止 (Visual Basic) '
title: 如何：声明自定义事件以避免阻止
ms.date: 07/20/2015
helpviewer_keywords:
- declaring events [Visual Basic], custom
- events [Visual Basic], custom
- custom events [Visual Basic]
ms.assetid: 998b6a90-67c5-4d2c-8b11-366d3e355505
ms.openlocfilehash: a4ad3162e8f95ebbf7567d427ea00060b19b2235
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100469716"
---
# <a name="how-to-declare-custom-events-to-avoid-blocking-visual-basic"></a><span data-ttu-id="64715-103">如何：声明自定义事件以避免阻止 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="64715-103">How to: Declare Custom Events To Avoid Blocking (Visual Basic)</span></span>

<span data-ttu-id="64715-104">在某些情况下，很重要的一点是，一个事件处理程序不会阻止后续事件处理程序。</span><span class="sxs-lookup"><span data-stu-id="64715-104">There are several circumstances when it is important that one event handler not block subsequent event handlers.</span></span> <span data-ttu-id="64715-105">自定义事件允许事件异步调用其事件处理程序。</span><span class="sxs-lookup"><span data-stu-id="64715-105">Custom events allow the event to call its event handlers asynchronously.</span></span>  
  
 <span data-ttu-id="64715-106">默认情况下，事件声明的 "备份存储" 字段为一个多播委托，该委托按顺序合并所有事件处理程序。</span><span class="sxs-lookup"><span data-stu-id="64715-106">By default, the backing-store field for an event declaration is a multicast delegate that serially combines all the event handlers.</span></span> <span data-ttu-id="64715-107">这意味着，如果某个处理程序需要很长时间才能完成，则会阻止其他处理程序完成。</span><span class="sxs-lookup"><span data-stu-id="64715-107">This means that if one handler takes a long time to complete, it blocks the other handlers until it completes.</span></span> <span data-ttu-id="64715-108"> (操作良好的事件处理程序不应执行冗长或可能阻塞的操作。 ) </span><span class="sxs-lookup"><span data-stu-id="64715-108">(Well-behaved event handlers should never perform lengthy or potentially blocking operations.)</span></span>  
  
 <span data-ttu-id="64715-109">您可以使用自定义事件异步执行事件处理程序，而不是使用 Visual Basic 提供的事件的默认实现。</span><span class="sxs-lookup"><span data-stu-id="64715-109">Instead of using the default implementation of events that Visual Basic provides, you can use a custom event to execute the event handlers asynchronously.</span></span>  
  
## <a name="example"></a><span data-ttu-id="64715-110">示例</span><span class="sxs-lookup"><span data-stu-id="64715-110">Example</span></span>  

 <span data-ttu-id="64715-111">在此示例中， `AddHandler` 访问器将事件的每个处理程序的委托添加 `Click` 到 <xref:System.Collections.ArrayList> 存储在 `EventHandlerList` 字段中的。</span><span class="sxs-lookup"><span data-stu-id="64715-111">In this example, the `AddHandler` accessor adds the delegate for each handler of the `Click` event to an <xref:System.Collections.ArrayList> stored in the `EventHandlerList` field.</span></span>  
  
 <span data-ttu-id="64715-112">当代码引发 `Click` 事件时， `RaiseEvent` 访问器使用方法以异步方式调用所有事件处理程序委托 <xref:System.Web.Services.Protocols.LogicalMethodInfo.BeginInvoke%2A> 。</span><span class="sxs-lookup"><span data-stu-id="64715-112">When code raises the `Click` event, the `RaiseEvent` accessor invokes all the event handler delegates asynchronously using the <xref:System.Web.Services.Protocols.LogicalMethodInfo.BeginInvoke%2A> method.</span></span> <span data-ttu-id="64715-113">该方法调用工作线程上的每个处理程序并立即返回，因此处理程序不能彼此阻止。</span><span class="sxs-lookup"><span data-stu-id="64715-113">That method invokes each handler on a worker thread and returns immediately, so handlers cannot block one another.</span></span>  
  
 [!code-vb[VbVbalrEvents#27](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrEvents/VB/Class1.vb#27)]  
  
## <a name="see-also"></a><span data-ttu-id="64715-114">请参阅</span><span class="sxs-lookup"><span data-stu-id="64715-114">See also</span></span>

- <xref:System.Collections.ArrayList>
- <xref:System.Web.Services.Protocols.LogicalMethodInfo.BeginInvoke%2A>
- [<span data-ttu-id="64715-115">事件</span><span class="sxs-lookup"><span data-stu-id="64715-115">Events</span></span>](index.md)
- [<span data-ttu-id="64715-116">如何：声明自定义事件以节省内存</span><span class="sxs-lookup"><span data-stu-id="64715-116">How to: Declare Custom Events To Conserve Memory</span></span>](how-to-declare-custom-events-to-conserve-memory.md)
