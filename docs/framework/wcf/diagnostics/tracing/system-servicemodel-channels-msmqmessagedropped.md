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
# <a name="systemservicemodelchannelsmsmqmessagedropped"></a>System.ServiceModel.Channels.MsmqMessageDropped

MSMQ 已删除该消息。  
  
## <a name="description"></a>说明  

 该跟踪指示已丢弃 MSMQ 消息。 如果 Windows Communication Foundation (WCF)  (与 NetMsmqBinding 或 MsmqIntegrationBinding) 一起使用时，MSMQ 消息就无法处理它们。 这些消息称为病毒消息。  
  
 当 NetMsmqBinding 或 MsmqIntegrationBinding 上的 `ReceiveErrorHandling` 属性设置为 `Drop` 时，将丢弃病毒消息。 丢弃的消息会从队列中移除而不再可恢复。  
  
 若要详细了解消息何时变为病毒以及如何配置服务以相应地处理这些消息，请参阅 [病毒消息处理](../../feature-details/poison-message-handling.md)。  
  
## <a name="see-also"></a>请参阅

- [跟踪](index.md)
- [使用跟踪来排除应用程序故障](using-tracing-to-troubleshoot-your-application.md)
- [管理和诊断](../index.md)
- [病毒消息处理](../../feature-details/poison-message-handling.md)
