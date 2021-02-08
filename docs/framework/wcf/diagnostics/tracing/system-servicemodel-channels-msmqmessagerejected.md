---
description: 了解有关以下方面的详细信息： MsmqMessageRejected
title: System.ServiceModel.Channels.MsmqMessageRejected
ms.date: 03/30/2017
ms.assetid: 9b7c10a7-2af6-44a2-8b1a-90bba0c7cf26
ms.openlocfilehash: 4400519c814627fd2a2f2585359d6d6376798ac0
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99780942"
---
# <a name="systemservicemodelchannelsmsmqmessagerejected"></a><span data-ttu-id="4c147-103">System.ServiceModel.Channels.MsmqMessageRejected</span><span class="sxs-lookup"><span data-stu-id="4c147-103">System.ServiceModel.Channels.MsmqMessageRejected</span></span>

<span data-ttu-id="4c147-104">MSMQ 已拒绝该消息。</span><span class="sxs-lookup"><span data-stu-id="4c147-104">MSMQ rejected the message.</span></span>  
  
## <a name="description"></a><span data-ttu-id="4c147-105">说明</span><span class="sxs-lookup"><span data-stu-id="4c147-105">Description</span></span>  

 <span data-ttu-id="4c147-106">此跟踪指示已拒绝 MSMQ 消息。</span><span class="sxs-lookup"><span data-stu-id="4c147-106">This trace indicates that an MSMQ message was rejected.</span></span>  
  
 <span data-ttu-id="4c147-107">Windows Communication Foundation 与 NetMsmqBinding 或 MsmqIntegrationBinding) 一起使用 (WCF)  (无法处理 MSMQ 消息时，MSMQ 消息可能会被拒绝。</span><span class="sxs-lookup"><span data-stu-id="4c147-107">MSMQ messages can be rejected when Windows Communication Foundation (WCF) (used with either the NetMsmqBinding or MsmqIntegrationBinding) is unable to process them.</span></span> <span data-ttu-id="4c147-108">这些消息称为病毒消息。</span><span class="sxs-lookup"><span data-stu-id="4c147-108">Such messages are referred to as poison messages.</span></span> <span data-ttu-id="4c147-109">当 NetMsmqBinding 或 MsmqIntegrationBinding 上的 `ReceiveErrorHandling` 属性设置为 `Reject` 时，将拒绝病毒消息。</span><span class="sxs-lookup"><span data-stu-id="4c147-109">A poison message is rejected when the `ReceiveErrorHandling` property on the NetMsmqBinding or MsmqIntegrationBinding is set to `Reject`.</span></span> <span data-ttu-id="4c147-110">拒绝的消息将传递回发送方的 [死信队列](../../feature-details/using-dead-letter-queues-to-handle-message-transfer-failures.md)。</span><span class="sxs-lookup"><span data-stu-id="4c147-110">A rejected message is delivered back to the sender’s [Dead-Letter Queue](../../feature-details/using-dead-letter-queues-to-handle-message-transfer-failures.md).</span></span>  
  
 <span data-ttu-id="4c147-111">若要详细了解消息何时变为病毒以及如何配置服务以相应地处理这些消息，请参阅 [病毒消息处理](../../feature-details/poison-message-handling.md)。</span><span class="sxs-lookup"><span data-stu-id="4c147-111">For more information on when messages become poison and how to configure your service to handle them appropriately, see [Poison-Message Handling](../../feature-details/poison-message-handling.md).</span></span>  
  
 <span data-ttu-id="4c147-112">有关 MSMQ 中的拒绝消息的含义的详细信息，请参阅 [MQMarkMessageRejected](/previous-versions/windows/desktop/msmq/ms707071(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="4c147-112">For more information on what a rejected message means in MSMQ, see [MQMarkMessageRejected](/previous-versions/windows/desktop/msmq/ms707071(v=vs.85)).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4c147-113">请参阅</span><span class="sxs-lookup"><span data-stu-id="4c147-113">See also</span></span>

- [<span data-ttu-id="4c147-114">跟踪</span><span class="sxs-lookup"><span data-stu-id="4c147-114">Tracing</span></span>](index.md)
- [<span data-ttu-id="4c147-115">使用跟踪来排除应用程序故障</span><span class="sxs-lookup"><span data-stu-id="4c147-115">Using Tracing to Troubleshoot Your Application</span></span>](using-tracing-to-troubleshoot-your-application.md)
- [<span data-ttu-id="4c147-116">管理和诊断</span><span class="sxs-lookup"><span data-stu-id="4c147-116">Administration and Diagnostics</span></span>](../index.md)
- [<span data-ttu-id="4c147-117">病毒消息处理</span><span class="sxs-lookup"><span data-stu-id="4c147-117">Poison-Message Handling</span></span>](../../feature-details/poison-message-handling.md)
- <span data-ttu-id="4c147-118">[MQMarkMessageRejected](/previous-versions/windows/desktop/msmq/ms707071(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="4c147-118">[MQMarkMessageRejected](/previous-versions/windows/desktop/msmq/ms707071(v=vs.85))</span></span>
