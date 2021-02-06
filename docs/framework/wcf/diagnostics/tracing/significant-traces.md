---
description: 了解详细信息：重大跟踪
title: 重要跟踪
ms.date: 03/30/2017
ms.assetid: 40a1770e-3b09-4142-b0dd-f9ef73642074
ms.openlocfilehash: 6d3e12c82312c2a8a3f0a19b4dc50e99e21b9730
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99635540"
---
# <a name="significant-traces"></a>重要跟踪

本主题列出了 Windows Communication Foundation (WCF) 发出的一些主要跟踪。  
  
## <a name="significant-traces"></a>重要跟踪  
  
|跟踪|说明|  
|-----------|-----------------|  
|消息日志跟踪|启用跟踪源时，通过消息日志记录功能记录 WCF 消息时，将发出跟踪 `System.ServiceModel.MessageLogging` 。 单击此跟踪可以显示消息。 一条消息有四个可配置的记录点：`ServiceLevelSendRequest`、`TransportSend`、`TransportReceive`、`ServiceLevelReceiveRequest`，消息日志跟踪的“消息源”属性中也指明了它们。|  
|已接收消息的跟踪|如果 `System.ServiceModel` 在信息级别或详细级别启用了跟踪源，则当接收到 WCF 消息时，将发出此跟踪。 此跟踪对于在活动图形视图中查看消息相关箭头而言是必需的。|  
|已发送消息的跟踪|如果 `System.ServiceModel` 在信息级别或详细级别启用了跟踪源，则发送 WCF 消息时，将发出此跟踪。 此跟踪对于在活动图形视图中查看消息相关箭头而言是必需的。|  
|获取 ChannelEndpointElement|在构建通道工厂时以信息级别发出此跟踪。 此跟踪提供对与客户端通信的终结点的说明（远程地址、绑定、协定名称）。|  
|获取 ServiceElement|在构建服务主机时以信息级别发出此跟踪。 此跟踪提供对服务协定和绑定的说明。|  
|SocketConnection 创建|在客户端执行的第一个处理操作中，以及在服务上的接收字节活动中发出此跟踪。 此跟踪提供本地和远程 IP 地址， 以信息级别发出。|
