---
description: 了解详细信息：通过 ETW 进行分析跟踪
title: 使用 ETW 进行分析跟踪
ms.date: 03/30/2017
helpviewer_keywords:
- diagnostics [WCF], analytic tracing
- administration [WCF], analytic tracing
- analytic tracing [WCF]
ms.assetid: 1d518e47-a38d-41e8-93d7-8c3b361f6a56
ms.openlocfilehash: fd40d40de2508fd251c793e4455c1e656a1cbbf6
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99798792"
---
# <a name="analytic-tracing-with-etw"></a><span data-ttu-id="e7e94-103">使用 ETW 进行分析跟踪</span><span class="sxs-lookup"><span data-stu-id="e7e94-103">Analytic Tracing with ETW</span></span>

<span data-ttu-id="e7e94-104">Windows Communication Foundation (WCF) 分析跟踪提供一种在执行 WCF 服务的过程中捕获诊断信息的方法。</span><span class="sxs-lookup"><span data-stu-id="e7e94-104">Windows Communication Foundation (WCF) analytic tracing offers a way to capture diagnostic information during the execution of a WCF service.</span></span> <span data-ttu-id="e7e94-105">在 WCF 堆栈中的关键点处发出 WCF 分析跟踪事件，以允许在生产环境中对 WCF 服务进行故障排除。</span><span class="sxs-lookup"><span data-stu-id="e7e94-105">WCF analytic tracing events are emitted at key points in the WCF stack to allow troubleshooting of WCF services in a production environment.</span></span> <span data-ttu-id="e7e94-106">WCF 服务的分析跟踪对承载 wcf 服务的产品服务器的性能的影响最小， [!INCLUDE[netfx_current_long](../../../../../includes/netfx-current-long-md.md)] 因为这些事件非常有效地发出到 Windows (ETW) 会话的事件跟踪。</span><span class="sxs-lookup"><span data-stu-id="e7e94-106">Analytic tracing for WCF services has minimal impact on the performance of a product server that hosts [!INCLUDE[netfx_current_long](../../../../../includes/netfx-current-long-md.md)] WCF services as these events are very efficiently emitted to an Event Tracing for Windows (ETW) session.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="e7e94-107">本节内容</span><span class="sxs-lookup"><span data-stu-id="e7e94-107">In This Section</span></span>  

 [<span data-ttu-id="e7e94-108">分析跟踪概述</span><span class="sxs-lookup"><span data-stu-id="e7e94-108">Analytic Tracing Overview</span></span>](analytic-tracing-overview.md)  
 <span data-ttu-id="e7e94-109">讨论 WCF 分析跟踪在中的工作方式 [!INCLUDE[netfx_current_long](../../../../../includes/netfx-current-long-md.md)] 。</span><span class="sxs-lookup"><span data-stu-id="e7e94-109">Discusses how WCF analytic tracing works in [!INCLUDE[netfx_current_long](../../../../../includes/netfx-current-long-md.md)].</span></span>  
  
 [<span data-ttu-id="e7e94-110">动态启用分析跟踪</span><span class="sxs-lookup"><span data-stu-id="e7e94-110">Dynamically Enabling Analytic Tracing</span></span>](dynamically-enabling-analytic-tracing.md)  
 <span data-ttu-id="e7e94-111">讨论如何使用 ETW 动态启用或禁用跟踪。</span><span class="sxs-lookup"><span data-stu-id="e7e94-111">Discusses how to enable or disable tracing dynamically using ETW.</span></span>  
  
 [<span data-ttu-id="e7e94-112">配置消息流跟踪</span><span class="sxs-lookup"><span data-stu-id="e7e94-112">Configuring Message Flow Tracing</span></span>](configuring-message-flow-tracing.md)  
 <span data-ttu-id="e7e94-113">描述如何配置消息流跟踪。</span><span class="sxs-lookup"><span data-stu-id="e7e94-113">Describes how to configure message flow tracing.</span></span>  
  
 [<span data-ttu-id="e7e94-114">分析跟踪事件参考</span><span class="sxs-lookup"><span data-stu-id="e7e94-114">Analytic Trace Event Reference</span></span>](analytic-trace-event-reference.md)  
 <span data-ttu-id="e7e94-115">显示一张表，其中包括事件 ID 及其事件级别、事件消息和关键字。</span><span class="sxs-lookup"><span data-stu-id="e7e94-115">Shows a table of event IDs with their event levels, event messages and keywords.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e7e94-116">请参阅</span><span class="sxs-lookup"><span data-stu-id="e7e94-116">See also</span></span>

- [<span data-ttu-id="e7e94-117">针对 Windows 的 WCF 服务和事件跟踪</span><span class="sxs-lookup"><span data-stu-id="e7e94-117">WCF Services and Event Tracing for Windows</span></span>](../../samples/wcf-services-and-event-tracing-for-windows.md)
- [<span data-ttu-id="e7e94-118">在 Windows 事件跟踪中跟踪事件</span><span class="sxs-lookup"><span data-stu-id="e7e94-118">Tracking Events into Event Tracing in Windows</span></span>](../../../windows-workflow-foundation/samples/tracking-events-into-event-tracing-in-windows.md)
