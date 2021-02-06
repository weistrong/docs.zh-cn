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
# <a name="security-negotiation-and-timeouts"></a><span data-ttu-id="5ac49-103">安全协商和超时</span><span class="sxs-lookup"><span data-stu-id="5ac49-103">Security Negotiation and Timeouts</span></span>

<span data-ttu-id="5ac49-104">当客户端和服务进行身份验证时，Windows Communication Foundation (WCF) 支持在身份验证过程中协商服务凭据的模式。</span><span class="sxs-lookup"><span data-stu-id="5ac49-104">When clients and services authenticate, Windows Communication Foundation (WCF) supports a mode where the service credential is negotiated as part of authentication.</span></span> <span data-ttu-id="5ac49-105">在这种情况下，客户端和服务之间将进行潜在多路交换，以便将服务凭据传播到客户端。</span><span class="sxs-lookup"><span data-stu-id="5ac49-105">In such scenarios, a potentially multi-leg exchange occurs between the client and the service to propagate the service credential to the client.</span></span> <span data-ttu-id="5ac49-106"><xref:System.ServiceModel.Channels.LocalServiceSecuritySettings.NegotiationTimeout%2A> 属性控制多路交换需要多长时间才能完成。</span><span class="sxs-lookup"><span data-stu-id="5ac49-106">The <xref:System.ServiceModel.Channels.LocalServiceSecuritySettings.NegotiationTimeout%2A> property controls how long the multi-leg exchange can take to complete.</span></span> <span data-ttu-id="5ac49-107">但此超时仅在交换实际经过的时间超过单个请求响应的时间时才适用。</span><span class="sxs-lookup"><span data-stu-id="5ac49-107">However, this timeout only applies if the exchange actually takes more that a single request-response.</span></span> <span data-ttu-id="5ac49-108">如果协商在一次往返中完成，则该超时不适用。</span><span class="sxs-lookup"><span data-stu-id="5ac49-108">In cases where the negotiation completes in a single round trip, the timeout does not apply.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5ac49-109">请参阅</span><span class="sxs-lookup"><span data-stu-id="5ac49-109">See also</span></span>

- <xref:System.ServiceModel.Channels.LocalServiceSecuritySettings>
- [<span data-ttu-id="5ac49-110">如何：设置最大时钟偏差</span><span class="sxs-lookup"><span data-stu-id="5ac49-110">How to: Set a Max Clock Skew</span></span>](how-to-set-a-max-clock-skew.md)
