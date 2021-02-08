---
description: 了解有关以下方面的详细信息： MsmqMoveOrDeleteAttemptFailed
title: System.ServiceModel.Channels.MsmqMoveOrDeleteAttemptFailed
ms.date: 03/30/2017
ms.assetid: d75d39da-7502-4a6a-91b9-eaa05b8e24d5
ms.openlocfilehash: 7b3c8dad9e3a3e88dff72706917f3729d55b3799
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99769736"
---
# <a name="systemservicemodelchannelsmsmqmoveordeleteattemptfailed"></a><span data-ttu-id="b32ee-103">System.ServiceModel.Channels.MsmqMoveOrDeleteAttemptFailed</span><span class="sxs-lookup"><span data-stu-id="b32ee-103">System.ServiceModel.Channels.MsmqMoveOrDeleteAttemptFailed</span></span>

<span data-ttu-id="b32ee-104">无法移动或删除消息。</span><span class="sxs-lookup"><span data-stu-id="b32ee-104">Cannot move or delete message.</span></span>  
  
## <a name="description"></a><span data-ttu-id="b32ee-105">说明</span><span class="sxs-lookup"><span data-stu-id="b32ee-105">Description</span></span>  

 <span data-ttu-id="b32ee-106">跟踪指示当尝试移动、删除或拒绝 MSMQ 消息时出错。</span><span class="sxs-lookup"><span data-stu-id="b32ee-106">The trace indicates that a failure occurred when attempting to move, delete, or reject an MSMQ message.</span></span>  
  
 <span data-ttu-id="b32ee-107">当与 NetMsmqBinding 或 MsmqIntegrationBinding) 一起使用时，MSMQ 消息 Windows Communication Foundation)  ( (WCF。此跟踪与 `ReceiveErrorHandling` NetMsmqBinding 或 MsmqIntegrationBinding 上的属性的选定值相关。</span><span class="sxs-lookup"><span data-stu-id="b32ee-107">MSMQ messages are employed by Windows Communication Foundation (WCF) (when used with either the NetMsmqBinding or the MsmqIntegrationBinding).This trace is related to the chosen value of the `ReceiveErrorHandling` property on the NetMsmqBinding or MsmqIntegrationBinding.</span></span>  
  
 <span data-ttu-id="b32ee-108">此跟踪不会指示出全部的系统失败。</span><span class="sxs-lookup"><span data-stu-id="b32ee-108">This trace is not indicative of an overall system failure.</span></span> <span data-ttu-id="b32ee-109">但是，它会指示某条消息的选定病毒消息处理失败。</span><span class="sxs-lookup"><span data-stu-id="b32ee-109">However, it indicates that the chosen poison message disposition failed for a message.</span></span> <span data-ttu-id="b32ee-110">若要详细了解消息何时变为病毒以及如何配置服务以相应地处理这些消息，请参阅 [病毒消息处理](../../feature-details/poison-message-handling.md)。</span><span class="sxs-lookup"><span data-stu-id="b32ee-110">For more information on when messages become poison and how to configure your service to handle them appropriately, see [Poison-Message Handling](../../feature-details/poison-message-handling.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b32ee-111">请参阅</span><span class="sxs-lookup"><span data-stu-id="b32ee-111">See also</span></span>

- [<span data-ttu-id="b32ee-112">跟踪</span><span class="sxs-lookup"><span data-stu-id="b32ee-112">Tracing</span></span>](index.md)
- [<span data-ttu-id="b32ee-113">使用跟踪来排除应用程序故障</span><span class="sxs-lookup"><span data-stu-id="b32ee-113">Using Tracing to Troubleshoot Your Application</span></span>](using-tracing-to-troubleshoot-your-application.md)
- [<span data-ttu-id="b32ee-114">管理和诊断</span><span class="sxs-lookup"><span data-stu-id="b32ee-114">Administration and Diagnostics</span></span>](../index.md)
