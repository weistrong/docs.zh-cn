---
description: 了解详细信息：如何：确定探测请求的发现版本
title: 如何：确定探测请求的发现版本
ms.date: 03/30/2017
ms.assetid: b3c4e2e2-2957-4074-ae6a-776a5ca84278
ms.openlocfilehash: c41283cb84d75dd2dbf7e86da0dec075ab8b6635
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99793787"
---
# <a name="how-todetermine-the-discovery-version-of-a-probe-request"></a><span data-ttu-id="44f73-103">如何：确定探测请求的发现版本</span><span class="sxs-lookup"><span data-stu-id="44f73-103">How to:Determine the Discovery Version of a Probe Request</span></span>

<span data-ttu-id="44f73-104">发现代理可能会公开使用不同发现版本的多个发现终结点。</span><span class="sxs-lookup"><span data-stu-id="44f73-104">A discovery proxy may expose multiple discovery endpoints using different discovery versions.</span></span> <span data-ttu-id="44f73-105">当 UDP 多播探测请求到达代理时，代理应使用多播禁止消息进行响应。</span><span class="sxs-lookup"><span data-stu-id="44f73-105">When a UDP multicast Probe request arrives at the proxy, the proxy should respond with a multicast suppression message.</span></span> <span data-ttu-id="44f73-106">为此，必须知道请求的发现版本。</span><span class="sxs-lookup"><span data-stu-id="44f73-106">In order to do this, it would have to know the discovery version of the request.</span></span>

## <a name="to-determine-the-discovery-version-of-a-probe-request"></a><span data-ttu-id="44f73-107">确定探测请求的发现版本</span><span class="sxs-lookup"><span data-stu-id="44f73-107">To Determine the Discovery Version of a Probe Request</span></span>

<span data-ttu-id="44f73-108">在响应探测请求的方法中 (例如 <xref:System.ServiceModel.Discovery.DiscoveryProxy.OnBeginFind%2A?displayProperty=nameWithType>) 使用静态 <xref:System.ServiceModel.OperationContext.Current%2A?displayProperty=nameWithType> 属性来搜索 <xref:System.ServiceModel.Discovery.DiscoveryOperationContextExtension> ，如下面的代码所示。</span><span class="sxs-lookup"><span data-stu-id="44f73-108">In the method that responds to a Probe request (for example <xref:System.ServiceModel.Discovery.DiscoveryProxy.OnBeginFind%2A?displayProperty=nameWithType>) use the static <xref:System.ServiceModel.OperationContext.Current%2A?displayProperty=nameWithType> property to search for a <xref:System.ServiceModel.Discovery.DiscoveryOperationContextExtension>, as shown in the following code.</span></span>

```csharp
DiscoveryOperationContextExtension doce = OperationContext.Current.Extensions.Find<DiscoveryOperationContextExtension>();
// Access the discovery version from the DiscoveryOperationContextExtension
doce.DiscoveryVersion;
```

## <a name="see-also"></a><span data-ttu-id="44f73-109">请参阅</span><span class="sxs-lookup"><span data-stu-id="44f73-109">See also</span></span>

- <xref:System.ServiceModel.Discovery.Configuration.AnnouncementEndpointElement.DiscoveryVersion%2A>
- [<span data-ttu-id="44f73-110">实现发现代理</span><span class="sxs-lookup"><span data-stu-id="44f73-110">Implementing a Discovery Proxy</span></span>](implementing-a-discovery-proxy.md)
