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
# <a name="how-todetermine-the-discovery-version-of-a-probe-request"></a>如何：确定探测请求的发现版本

发现代理可能会公开使用不同发现版本的多个发现终结点。 当 UDP 多播探测请求到达代理时，代理应使用多播禁止消息进行响应。 为此，必须知道请求的发现版本。

## <a name="to-determine-the-discovery-version-of-a-probe-request"></a>确定探测请求的发现版本

在响应探测请求的方法中 (例如 <xref:System.ServiceModel.Discovery.DiscoveryProxy.OnBeginFind%2A?displayProperty=nameWithType>) 使用静态 <xref:System.ServiceModel.OperationContext.Current%2A?displayProperty=nameWithType> 属性来搜索 <xref:System.ServiceModel.Discovery.DiscoveryOperationContextExtension> ，如下面的代码所示。

```csharp
DiscoveryOperationContextExtension doce = OperationContext.Current.Extensions.Find<DiscoveryOperationContextExtension>();
// Access the discovery version from the DiscoveryOperationContextExtension
doce.DiscoveryVersion;
```

## <a name="see-also"></a>请参阅

- <xref:System.ServiceModel.Discovery.Configuration.AnnouncementEndpointElement.DiscoveryVersion%2A>
- [实现发现代理](implementing-a-discovery-proxy.md)
