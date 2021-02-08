---
description: 了解详细信息：活动 ID 传播
title: 活动 ID 传播
ms.date: 03/30/2017
ms.assetid: cd1c1ae5-cc8a-4f51-90c9-f7b476bcfe70
ms.openlocfilehash: d407af04304298bcc04a7aa4264eb6fc46563d3a
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99770893"
---
# <a name="activity-id-propagation"></a><span data-ttu-id="65788-103">活动 ID 传播</span><span class="sxs-lookup"><span data-stu-id="65788-103">Activity ID Propagation</span></span>

<span data-ttu-id="65788-104">当 ServiceModel 活动跟踪启用（ServiceModel 传播）或禁用（用户对用户活动跟踪）时，都会发生传播。</span><span class="sxs-lookup"><span data-stu-id="65788-104">Propagation happens when ServiceModel activity tracing is enabled (ServiceModel propagation) or disabled (User-to-User activity propagation).</span></span>  
  
## <a name="servicemodel-activity-tracing-is-enabled"></a><span data-ttu-id="65788-105">ServiceModel 活动跟踪启用</span><span class="sxs-lookup"><span data-stu-id="65788-105">ServiceModel Activity Tracing is Enabled</span></span>  

 <span data-ttu-id="65788-106">如果启用 ServiceModel ActivityTracing，传播将在 ProcessAction 活动之间发生。</span><span class="sxs-lookup"><span data-stu-id="65788-106">If ServiceModel ActivityTracing is enabled, propagation happens between ProcessAction activities.</span></span>  
  
### <a name="server"></a><span data-ttu-id="65788-107">服务器</span><span class="sxs-lookup"><span data-stu-id="65788-107">Server</span></span>  

 <span data-ttu-id="65788-108">当 `propagateActivity` `true` 客户端和服务器上的属性设置为时， `ProcessAction` 服务器中的活动 id 与传播的消息头中的 id 相同 `ActivityId` 。</span><span class="sxs-lookup"><span data-stu-id="65788-108">When the `propagateActivity` attribute is set to `true` on both the client and server, the ID of the `ProcessAction` activity in the server is identical to the ID in the propagated `ActivityId` message header.</span></span>  
  
 <span data-ttu-id="65788-109">如果 `ActivityId` 消息中不存在任何标头 (即， `propagateActivity` = `false` 在客户端) 上或 `propagateActivity` = `false` 在服务器上时，服务器将生成新的活动 ID。</span><span class="sxs-lookup"><span data-stu-id="65788-109">When no `ActivityId` header is present in the message (that is, `propagateActivity`=`false` on the client), or when `propagateActivity`=`false` on the server, the server generates a new activity ID.</span></span>  
  
### <a name="client"></a><span data-ttu-id="65788-110">客户端</span><span class="sxs-lookup"><span data-stu-id="65788-110">Client</span></span>  

 <span data-ttu-id="65788-111">如果客户端是同步单线程，则客户端忽略客户端或服务器上 `propagateActivity` 的任何设置。</span><span class="sxs-lookup"><span data-stu-id="65788-111">If the client is synchronously single threaded, the client disregards any settings of `propagateActivity` at the client or server.</span></span> <span data-ttu-id="65788-112">响应则改为在请求活动中处理。</span><span class="sxs-lookup"><span data-stu-id="65788-112">Instead, the response is handled in the request activity.</span></span> <span data-ttu-id="65788-113">如果客户端是异步或同步多线程，则 `propagateActivity` = `true` 在客户端中，服务器发送的消息中有活动 id 标头，客户端将从消息中检索活动 id，并传输到包含传播的活动 ID 的 "进程操作" 活动。</span><span class="sxs-lookup"><span data-stu-id="65788-113">If the client is asynchronous or synchronous multithreaded, `propagateActivity`=`true` in the client, and there is an activity ID header in the message sent by the server, the client retrieves the activity ID from the message, and transfers to the Process Action activity that contains the propagated activity ID.</span></span> <span data-ttu-id="65788-114">否则，客户端从“进程管理”活动转移到新的“进程操作”活动。</span><span class="sxs-lookup"><span data-stu-id="65788-114">Otherwise, the client transfers from Process Message activity to a new Process Action activity.</span></span> <span data-ttu-id="65788-115">完成到新“进程操作”活动的这一额外转移是为了实现一致性。</span><span class="sxs-lookup"><span data-stu-id="65788-115">This extra transfer to a new Process Action activity is done for consistency.</span></span> <span data-ttu-id="65788-116">在此活动内，如果为响应消息处理分配了线程，则客户端从本地线程上下文检索 BeginCall 活动的活动 ID。</span><span class="sxs-lookup"><span data-stu-id="65788-116">Inside this activity, the client retrieves the activity ID of the BeginCall activity from the local thread context, when the thread is allocated for response message processing.</span></span> <span data-ttu-id="65788-117">然后，客户端转移到初始“进程操作”活动。</span><span class="sxs-lookup"><span data-stu-id="65788-117">It then transfers to the initial Process Action activity.</span></span>  
  
 <span data-ttu-id="65788-118">如果客户端为双工，则客户端在接收消息时用作服务器。</span><span class="sxs-lookup"><span data-stu-id="65788-118">If the client is duplex, the client acts as server on receiving the message.</span></span>  
  
### <a name="propagation-in-fault-messages"></a><span data-ttu-id="65788-119">错误消息中的传播</span><span class="sxs-lookup"><span data-stu-id="65788-119">Propagation in Fault Messages</span></span>  

 <span data-ttu-id="65788-120">有效消息和错误消息的处理没有任何区别。</span><span class="sxs-lookup"><span data-stu-id="65788-120">There is no difference in handling valid and fault messages.</span></span> <span data-ttu-id="65788-121">如果为 `propagateActivity` = `true` ，则添加到 SOAP 错误消息标头的活动 ID 等同于环境活动。</span><span class="sxs-lookup"><span data-stu-id="65788-121">If `propagateActivity`=`true`, the activity ID added to the SOAP fault message headers is identical to the ambient activity.</span></span>  
  
## <a name="servicemodel-activity-tracing-is-disabled"></a><span data-ttu-id="65788-122">ServiceModel 活动跟踪禁用</span><span class="sxs-lookup"><span data-stu-id="65788-122">ServiceModel Activity Tracing is Disabled</span></span>  

 <span data-ttu-id="65788-123">如果 ServiceModel ActivityTracing 禁用，传播将在用户代码活动之间直接发生，而不经过 ServiceModel 活动。</span><span class="sxs-lookup"><span data-stu-id="65788-123">If ServiceModel ActivityTracing is disabled, propagation occurs between user code activities directly without going through ServiceModel activities.</span></span> <span data-ttu-id="65788-124">用户定义的活动 ID 也通过消息活动 ID 标头传播。</span><span class="sxs-lookup"><span data-stu-id="65788-124">A user-defined activity ID is also propagated through the message activity ID header.</span></span>  
  
 <span data-ttu-id="65788-125">如果对 `propagateActivity` = `true` `ActivityTracing` = `off` 工作的跟踪 (侦听器，无论是否在 system.servicemodel) 上启用跟踪，无论是否启用了跟踪，都将发生以下情况：</span><span class="sxs-lookup"><span data-stu-id="65788-125">If `propagateActivity`=`true` and `ActivityTracing`=`off` for a ServiceModel trace listener (regardless of whether tracing is enabled on ServiceModel), the following happen on either the client or server:</span></span>  
  
- <span data-ttu-id="65788-126">在操作请求或发送响应时，TLS 中的活动 ID 从用户代码传播出去，直至构成消息。</span><span class="sxs-lookup"><span data-stu-id="65788-126">On operation request or sending response, the activity ID in TLS is propagated out of user code until a message is formed.</span></span> <span data-ttu-id="65788-127">活动 ID 标头也在消息发送之前插入消息中。</span><span class="sxs-lookup"><span data-stu-id="65788-127">An activity ID header is also inserted into the message before it is sent.</span></span>  
  
- <span data-ttu-id="65788-128">接收到请求或响应时，只要创建了接收的消息对象，即从消息头中检索活动 ID。</span><span class="sxs-lookup"><span data-stu-id="65788-128">On receiving request or receiving response, the activity ID is retrieved from the message header as soon as the received message object is created.</span></span> <span data-ttu-id="65788-129">消息从作用域中一消失，TLS 中的活动 ID 就会进行传播，直至达到用户代码。</span><span class="sxs-lookup"><span data-stu-id="65788-129">The activity ID in TLS is propagated as soon as the message disappears from scope until user code is reached.</span></span>  
  
 <span data-ttu-id="65788-130">这些操作保证了在启用传播的情况下，用户跟踪将出现在相同的活动中。</span><span class="sxs-lookup"><span data-stu-id="65788-130">These actions guarantee that user traces will appear in the same activity if propagation is on.</span></span> <span data-ttu-id="65788-131">但是，这不保证 ServiceModel 跟踪。</span><span class="sxs-lookup"><span data-stu-id="65788-131">However, it makes no guarantee on ServiceModel traces.</span></span> <span data-ttu-id="65788-132">仅当 ServiceModel 跟踪处理是在设置用户代码活动的线程中执行时，这些跟踪才会出现在用户代码活动中。</span><span class="sxs-lookup"><span data-stu-id="65788-132">ServiceModel traces occur in a user code activity only if the processing of those traces is executed on the same thread where the user code activity was set.</span></span>  
  
 <span data-ttu-id="65788-133">一般而言，在以下位置可以观察到 ServiceModel 跟踪：</span><span class="sxs-lookup"><span data-stu-id="65788-133">In general, ServiceModel traces can be observed in the following places:</span></span>  
  
- <span data-ttu-id="65788-134">如果禁用 ServiceModel 跟踪，则发出的所有跟踪都将出现在用户活动中。</span><span class="sxs-lookup"><span data-stu-id="65788-134">If ServiceModel tracing is disabled, all emitted traces appear in user activities.</span></span> <span data-ttu-id="65788-135">如果服务器和客户端上都启用传播，则这些跟踪将在同一个活动中。</span><span class="sxs-lookup"><span data-stu-id="65788-135">If propagation is enabled at both the server and client, these traces will be in the same activity.</span></span>  
  
- <span data-ttu-id="65788-136">如果启用了 ServiceModel 跟踪，但禁用了 ActivityTracing，并且服务器和客户端都启用传播，则用户跟踪将出现在同一个活动中。</span><span class="sxs-lookup"><span data-stu-id="65788-136">If ServiceModel tracing is enabled, but ActivityTracing is disabled, user traces appear in the same activity if propagation is enabled on both ends.</span></span> <span data-ttu-id="65788-137">ServiceModel 跟踪出现在默认的 0000 活动中，除非这些跟踪发生在与最初设置该活动的用户代码处理相同的线程中。</span><span class="sxs-lookup"><span data-stu-id="65788-137">ServiceModel traces appear in the default 0000 activity, unless they occur in the same thread as the user code processing where the activity is initially set.</span></span>  
  
- <span data-ttu-id="65788-138">如果启用了 ServiceModel 跟踪和 ActivityTracing，则用户跟踪将出现在用户定义的活动中，而 ServiceModel 跟踪则出现在 ServiceModel 定义的活动中。</span><span class="sxs-lookup"><span data-stu-id="65788-138">If both ServiceModel tracing and ActivityTracing are enabled, user traces appear in user-defined activities, and ServiceModel traces appear in ServiceModel-defined activities.</span></span> <span data-ttu-id="65788-139">传播在 ServiceModel 级别发生。</span><span class="sxs-lookup"><span data-stu-id="65788-139">Propagation happens at ServiceModel level.</span></span>
