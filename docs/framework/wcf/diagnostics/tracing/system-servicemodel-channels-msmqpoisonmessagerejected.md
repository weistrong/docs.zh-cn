---
description: 了解有关以下方面的详细信息： MsmqPoisonMessageRejected
title: System.ServiceModel.Channels.MsmqPoisonMessageRejected
ms.date: 03/30/2017
ms.assetid: 0e64b9bd-1f12-43df-a189-d7be3c2bace1
ms.openlocfilehash: 856c28dd313867de0661d4950dd67e6740e2b338
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99759297"
---
# <a name="systemservicemodelchannelsmsmqpoisonmessagerejected"></a><span data-ttu-id="5bfea-103">System.ServiceModel.Channels.MsmqPoisonMessageRejected</span><span class="sxs-lookup"><span data-stu-id="5bfea-103">System.ServiceModel.Channels.MsmqPoisonMessageRejected</span></span>

<span data-ttu-id="5bfea-104">拒绝的病毒消息。</span><span class="sxs-lookup"><span data-stu-id="5bfea-104">Poison message rejected.</span></span>  
  
## <a name="description"></a><span data-ttu-id="5bfea-105">说明</span><span class="sxs-lookup"><span data-stu-id="5bfea-105">Description</span></span>  

 <span data-ttu-id="5bfea-106">该跟踪指示遇到病毒消息并随后将其拒绝。</span><span class="sxs-lookup"><span data-stu-id="5bfea-106">The trace indicates that a poison message was encountered and subsequently rejected.</span></span> <span data-ttu-id="5bfea-107">当 NetMsmqBinding 或 MsmqIntegrationBinding 上的 `ReceiveErrorHandling` 属性设置为 `Reject` 时，将会出现此情况。</span><span class="sxs-lookup"><span data-stu-id="5bfea-107">This occurs when the `ReceiveErrorHandling` property on the NetMsmqBinding or MsmqIntegrationBinding is set to `Reject`.</span></span> <span data-ttu-id="5bfea-108">拒绝的消息将传递回发送方的 [死信队列](../../feature-details/using-dead-letter-queues-to-handle-message-transfer-failures.md)。</span><span class="sxs-lookup"><span data-stu-id="5bfea-108">A rejected message is delivered back to the sender’s [Dead-Letter Queue](../../feature-details/using-dead-letter-queues-to-handle-message-transfer-failures.md).</span></span>  
  
 <span data-ttu-id="5bfea-109">若要详细了解消息何时变为病毒以及如何配置服务以相应地处理这些消息，请参阅 [病毒消息处理](../../feature-details/poison-message-handling.md)。</span><span class="sxs-lookup"><span data-stu-id="5bfea-109">For more information on when messages become poison and how to configure your service to handle them appropriately, see [Poison-Message Handling](../../feature-details/poison-message-handling.md).</span></span> <span data-ttu-id="5bfea-110">有关 MSMQ 中的拒绝消息的含义的详细信息，请参阅 [MQMarkMessageRejected](/previous-versions/windows/desktop/msmq/ms707071(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="5bfea-110">For more information on what a rejected message means in MSMQ, see [MQMarkMessageRejected](/previous-versions/windows/desktop/msmq/ms707071(v=vs.85)).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5bfea-111">请参阅</span><span class="sxs-lookup"><span data-stu-id="5bfea-111">See also</span></span>

- [<span data-ttu-id="5bfea-112">跟踪</span><span class="sxs-lookup"><span data-stu-id="5bfea-112">Tracing</span></span>](index.md)
- [<span data-ttu-id="5bfea-113">使用跟踪来排除应用程序故障</span><span class="sxs-lookup"><span data-stu-id="5bfea-113">Using Tracing to Troubleshoot Your Application</span></span>](using-tracing-to-troubleshoot-your-application.md)
- [<span data-ttu-id="5bfea-114">管理和诊断</span><span class="sxs-lookup"><span data-stu-id="5bfea-114">Administration and Diagnostics</span></span>](../index.md)
- [<span data-ttu-id="5bfea-115">病毒消息处理</span><span class="sxs-lookup"><span data-stu-id="5bfea-115">Poison-Message Handling</span></span>](../../feature-details/poison-message-handling.md)
- <span data-ttu-id="5bfea-116">[MQMarkMessageRejected](/previous-versions/windows/desktop/msmq/ms707071(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="5bfea-116">[MQMarkMessageRejected](/previous-versions/windows/desktop/msmq/ms707071(v=vs.85))</span></span>
