---
description: 了解详细信息：安全协商和超时
title: 安全协商和超时
ms.date: 03/30/2017
ms.assetid: 02a428f1-84e5-4d28-a11f-53ce31d63196
ms.openlocfilehash: 50055698f9a9946d0c0110a964cf9ce5b9f4fa28
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99632433"
---
# <a name="security-negotiation-and-timeouts"></a>安全协商和超时

当客户端和服务进行身份验证时，Windows Communication Foundation (WCF) 支持在身份验证过程中协商服务凭据的模式。 在这种情况下，客户端和服务之间将进行潜在多路交换，以便将服务凭据传播到客户端。 <xref:System.ServiceModel.Channels.LocalServiceSecuritySettings.NegotiationTimeout%2A> 属性控制多路交换需要多长时间才能完成。 但此超时仅在交换实际经过的时间超过单个请求响应的时间时才适用。 如果协商在一次往返中完成，则该超时不适用。  
  
## <a name="see-also"></a>请参阅

- <xref:System.ServiceModel.Channels.LocalServiceSecuritySettings>
- [如何：设置最大时钟偏差](how-to-set-a-max-clock-skew.md)
