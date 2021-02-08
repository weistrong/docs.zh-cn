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
# <a name="systemservicemodelchannelsmsmqmessagerejected"></a>System.ServiceModel.Channels.MsmqMessageRejected

MSMQ 已拒绝该消息。  
  
## <a name="description"></a>说明  

 此跟踪指示已拒绝 MSMQ 消息。  
  
 Windows Communication Foundation 与 NetMsmqBinding 或 MsmqIntegrationBinding) 一起使用 (WCF)  (无法处理 MSMQ 消息时，MSMQ 消息可能会被拒绝。 这些消息称为病毒消息。 当 NetMsmqBinding 或 MsmqIntegrationBinding 上的 `ReceiveErrorHandling` 属性设置为 `Reject` 时，将拒绝病毒消息。 拒绝的消息将传递回发送方的 [死信队列](../../feature-details/using-dead-letter-queues-to-handle-message-transfer-failures.md)。  
  
 若要详细了解消息何时变为病毒以及如何配置服务以相应地处理这些消息，请参阅 [病毒消息处理](../../feature-details/poison-message-handling.md)。  
  
 有关 MSMQ 中的拒绝消息的含义的详细信息，请参阅 [MQMarkMessageRejected](/previous-versions/windows/desktop/msmq/ms707071(v=vs.85))。  
  
## <a name="see-also"></a>请参阅

- [跟踪](index.md)
- [使用跟踪来排除应用程序故障](using-tracing-to-troubleshoot-your-application.md)
- [管理和诊断](../index.md)
- [病毒消息处理](../../feature-details/poison-message-handling.md)
- [MQMarkMessageRejected](/previous-versions/windows/desktop/msmq/ms707071(v=vs.85))
