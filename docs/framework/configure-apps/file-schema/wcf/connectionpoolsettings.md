---
description: 了解详细信息： <connectionPoolSettings>
title: <connectionPoolSettings>
ms.date: 03/30/2017
ms.assetid: 6fa7fa65-2c6e-4eab-b8cf-7690112c0be5
ms.openlocfilehash: 5acf2d800f1a18f45750d0fabd23516f987b2c5e
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99782164"
---
# \<connectionPoolSettings>

<span data-ttu-id="bf211-102">指定命名管道绑定的其他连接池设置。</span><span class="sxs-lookup"><span data-stu-id="bf211-102">Specifies additional connection pool settings for a Named Pipe binding.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<bindings>**](bindings.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<customBinding>**](custombinding.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<binding>**\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<namedPipeTransport>**](namedpipetransport.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<connectionPoolSettings>**  
  
## <a name="syntax"></a><span data-ttu-id="bf211-103">语法</span><span class="sxs-lookup"><span data-stu-id="bf211-103">Syntax</span></span>  
  
```xml  
<connectionPoolSettings groupName="String"
                        idleTimeout="TimeSpan"
                        maxOutboundConnectionsPerEndpoint="Integer" />
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="bf211-104">特性和元素</span><span class="sxs-lookup"><span data-stu-id="bf211-104">Attributes and Elements</span></span>  

 <span data-ttu-id="bf211-105">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="bf211-105">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="bf211-106">特性</span><span class="sxs-lookup"><span data-stu-id="bf211-106">Attributes</span></span>  
  
|<span data-ttu-id="bf211-107">属性</span><span class="sxs-lookup"><span data-stu-id="bf211-107">Attribute</span></span>|<span data-ttu-id="bf211-108">说明</span><span class="sxs-lookup"><span data-stu-id="bf211-108">Description</span></span>|  
|---------------|-----------------|  
|`groupName`|<span data-ttu-id="bf211-109">一个字符串，定义用于传出通道的连接池的名称。</span><span class="sxs-lookup"><span data-stu-id="bf211-109">A string that defines the name of the connection pool used for outgoing channels.</span></span> <span data-ttu-id="bf211-110">在流处理模式中，不共享连接，这意味着禁用连接池。</span><span class="sxs-lookup"><span data-stu-id="bf211-110">In streamed mode, connections are not shared, meaning that connection pooling is disabled.</span></span> <span data-ttu-id="bf211-111">默认值为字符串 "default"。</span><span class="sxs-lookup"><span data-stu-id="bf211-111">The default is a "default" string.</span></span> <span data-ttu-id="bf211-112">可以修改此值，以便将特定客户端的连接隔离到不同的组中。</span><span class="sxs-lookup"><span data-stu-id="bf211-112">You can modify this value to isolate the connections for a particular client into separate groups.</span></span>|  
|`idleTimeout`|<span data-ttu-id="bf211-113">一个值为正的 <xref:System.TimeSpan>，指定连接在断开前可以空闲的最长时间。</span><span class="sxs-lookup"><span data-stu-id="bf211-113">A positive <xref:System.TimeSpan> that specifies the maximum time the connection can be idle before being disconnected.</span></span> <span data-ttu-id="bf211-114">默认值为 00:02:00。</span><span class="sxs-lookup"><span data-stu-id="bf211-114">The default is 00:02:00.</span></span>|  
|`maxOutboundConnectionsPerEndpoint`|<span data-ttu-id="bf211-115">一个正整数，指定由服务启动的与远程终结点的最大连接数。</span><span class="sxs-lookup"><span data-stu-id="bf211-115">A positive integer that specifies the maximum number of connections to a remote endpoint initiated by the service.</span></span> <span data-ttu-id="bf211-116">超出此限制的连接需要排队，直到连接数低于限制值。</span><span class="sxs-lookup"><span data-stu-id="bf211-116">Connections in excess of the limit are queued until a space below the limit becomes available.</span></span> <span data-ttu-id="bf211-117">`idleTimeout` 限制连接在引发异常前保持排队状态的持续时间。</span><span class="sxs-lookup"><span data-stu-id="bf211-117">The `idleTimeout` limits the duration in which connections remain queued before an exception is thrown.</span></span> <span data-ttu-id="bf211-118">默认值为 10。</span><span class="sxs-lookup"><span data-stu-id="bf211-118">The default is 10.</span></span><br /><br /> <span data-ttu-id="bf211-119">此属性限制从客户端到特定服务终结点的同时活动的连接数。</span><span class="sxs-lookup"><span data-stu-id="bf211-119">This attribute limits the number of simultaneous active connections from the client to a particular service endpoint.</span></span> <span data-ttu-id="bf211-120">如果由于具有更多的活动客户端连接而超出此值，则服务可能表现为对客户端无响应。</span><span class="sxs-lookup"><span data-stu-id="bf211-120">If this value is exceeded by having more active client connections, the service may appear unresponsive to the client.</span></span> <span data-ttu-id="bf211-121">在此情况下，应调整此值使之超过与特定终结点的同时活动的最大预期客户端连接数。</span><span class="sxs-lookup"><span data-stu-id="bf211-121">In this case, this value should be adjusted to exceed the maximum number of expected simultaneous client connections to a specific endpoint.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="bf211-122">子元素</span><span class="sxs-lookup"><span data-stu-id="bf211-122">Child Elements</span></span>  

 <span data-ttu-id="bf211-123">无。</span><span class="sxs-lookup"><span data-stu-id="bf211-123">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="bf211-124">父元素</span><span class="sxs-lookup"><span data-stu-id="bf211-124">Parent Elements</span></span>  
  
|<span data-ttu-id="bf211-125">元素</span><span class="sxs-lookup"><span data-stu-id="bf211-125">Element</span></span>|<span data-ttu-id="bf211-126">说明</span><span class="sxs-lookup"><span data-stu-id="bf211-126">Description</span></span>|  
|-------------|-----------------|  
|[\<namedPipeTransport>](namedpipetransport.md)|<span data-ttu-id="bf211-127">定义传输，该传输使通道使用命名管道传输消息。</span><span class="sxs-lookup"><span data-stu-id="bf211-127">Defines a transport that causes a channel to transfer messages using named pipes.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="bf211-128">请参阅</span><span class="sxs-lookup"><span data-stu-id="bf211-128">See also</span></span>

- <xref:System.ServiceModel.Configuration.NamedPipeConnectionPoolSettingsElement>
- <xref:System.ServiceModel.Channels.NamedPipeTransportBindingElement.ConnectionPoolSettings%2A>
- <xref:System.ServiceModel.Channels.NamedPipeConnectionPoolSettings>
- <xref:System.ServiceModel.Channels.TransportBindingElement>
- <xref:System.ServiceModel.Channels.CustomBinding>
- [<span data-ttu-id="bf211-129">传输</span><span class="sxs-lookup"><span data-stu-id="bf211-129">Transports</span></span>](../../../wcf/feature-details/transports.md)
- [<span data-ttu-id="bf211-130">选择传输方式</span><span class="sxs-lookup"><span data-stu-id="bf211-130">Choosing a Transport</span></span>](../../../wcf/feature-details/choosing-a-transport.md)
- [<span data-ttu-id="bf211-131">绑定</span><span class="sxs-lookup"><span data-stu-id="bf211-131">Bindings</span></span>](../../../wcf/bindings.md)
- [<span data-ttu-id="bf211-132">扩展绑定</span><span class="sxs-lookup"><span data-stu-id="bf211-132">Extending Bindings</span></span>](../../../wcf/extending/extending-bindings.md)
- [<span data-ttu-id="bf211-133">自定义绑定</span><span class="sxs-lookup"><span data-stu-id="bf211-133">Custom Bindings</span></span>](../../../wcf/extending/custom-bindings.md)
- [\<customBinding>](custombinding.md)
