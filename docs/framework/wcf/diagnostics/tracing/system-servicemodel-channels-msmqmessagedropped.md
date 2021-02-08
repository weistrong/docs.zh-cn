---
description: 了解有关以下方面的详细信息： MsmqMessageDropped
title: System.ServiceModel.Channels.MsmqMessageDropped
ms.date: 03/30/2017
ms.assetid: 8b6e644d-fa68-4be7-abe9-3659671a37c1
ms.openlocfilehash: 41b9c6d5399f0f6b458404ee4b64624e5863c777
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99780955"
---
# <a name="systemservicemodelchannelsmsmqmessagedropped"></a><span data-ttu-id="644fb-103">System.ServiceModel.Channels.MsmqMessageDropped</span><span class="sxs-lookup"><span data-stu-id="644fb-103">System.ServiceModel.Channels.MsmqMessageDropped</span></span>

<span data-ttu-id="644fb-104">MSMQ 已删除该消息。</span><span class="sxs-lookup"><span data-stu-id="644fb-104">MSMQ dropped the message.</span></span>  
  
## <a name="description"></a><span data-ttu-id="644fb-105">说明</span><span class="sxs-lookup"><span data-stu-id="644fb-105">Description</span></span>  

 <span data-ttu-id="644fb-106">该跟踪指示已丢弃 MSMQ 消息。</span><span class="sxs-lookup"><span data-stu-id="644fb-106">The trace indicates that an MSMQ message was dropped.</span></span> <span data-ttu-id="644fb-107">如果 Windows Communication Foundation (WCF)  (与 NetMsmqBinding 或 MsmqIntegrationBinding) 一起使用时，MSMQ 消息就无法处理它们。</span><span class="sxs-lookup"><span data-stu-id="644fb-107">MSMQ messages can be dropped when Windows Communication Foundation (WCF) (used with either the NetMsmqBinding or MsmqIntegrationBinding) is unable to process them.</span></span> <span data-ttu-id="644fb-108">这些消息称为病毒消息。</span><span class="sxs-lookup"><span data-stu-id="644fb-108">Such messages are referred to as poison messages.</span></span>  
  
 <span data-ttu-id="644fb-109">当 NetMsmqBinding 或 MsmqIntegrationBinding 上的 `ReceiveErrorHandling` 属性设置为 `Drop` 时，将丢弃病毒消息。</span><span class="sxs-lookup"><span data-stu-id="644fb-109">A poison message is dropped when the `ReceiveErrorHandling` property on the NetMsmqBinding or MsmqIntegrationBinding is set to `Drop`.</span></span> <span data-ttu-id="644fb-110">丢弃的消息会从队列中移除而不再可恢复。</span><span class="sxs-lookup"><span data-stu-id="644fb-110">A dropped message is removed from the queue and is no longer recoverable.</span></span>  
  
 <span data-ttu-id="644fb-111">若要详细了解消息何时变为病毒以及如何配置服务以相应地处理这些消息，请参阅 [病毒消息处理](../../feature-details/poison-message-handling.md)。</span><span class="sxs-lookup"><span data-stu-id="644fb-111">For more information on when messages become poison and how to configure your service to handle them appropriately, see [Poison-Message Handling](../../feature-details/poison-message-handling.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="644fb-112">请参阅</span><span class="sxs-lookup"><span data-stu-id="644fb-112">See also</span></span>

- [<span data-ttu-id="644fb-113">跟踪</span><span class="sxs-lookup"><span data-stu-id="644fb-113">Tracing</span></span>](index.md)
- [<span data-ttu-id="644fb-114">使用跟踪来排除应用程序故障</span><span class="sxs-lookup"><span data-stu-id="644fb-114">Using Tracing to Troubleshoot Your Application</span></span>](using-tracing-to-troubleshoot-your-application.md)
- [<span data-ttu-id="644fb-115">管理和诊断</span><span class="sxs-lookup"><span data-stu-id="644fb-115">Administration and Diagnostics</span></span>](../index.md)
- [<span data-ttu-id="644fb-116">病毒消息处理</span><span class="sxs-lookup"><span data-stu-id="644fb-116">Poison-Message Handling</span></span>](../../feature-details/poison-message-handling.md)
