---
description: 了解详细信息： <channelPoolSettings>
title: <channelPoolSettings>
ms.date: 03/30/2017
ms.assetid: 4755f3d3-4213-4c68-ae7f-45b67d744459
ms.openlocfilehash: 85220cac360aaf32195c0b0f1d2866729e11c442
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99638972"
---
# \<channelPoolSettings>

<span data-ttu-id="1bbdd-102">指定自定义绑定的通道池设置。</span><span class="sxs-lookup"><span data-stu-id="1bbdd-102">Specifies the channel pool settings for a custom binding.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<bindings>**](bindings.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<customBinding>**](custombinding.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<binding>**\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<oneWay>**](oneway.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<channelPoolSettings>**  
  
## <a name="syntax"></a><span data-ttu-id="1bbdd-103">语法</span><span class="sxs-lookup"><span data-stu-id="1bbdd-103">Syntax</span></span>  
  
```xml  
<channelPoolSettings idleTimeout="TimeSpan"
                     leaseTimeout="TimeSpan"
                     maxOutboundConnectionsPerEndpoint="Integer" />
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="1bbdd-104">特性和元素</span><span class="sxs-lookup"><span data-stu-id="1bbdd-104">Attributes and Elements</span></span>  

 <span data-ttu-id="1bbdd-105">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="1bbdd-105">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="1bbdd-106">特性</span><span class="sxs-lookup"><span data-stu-id="1bbdd-106">Attributes</span></span>  
  
|<span data-ttu-id="1bbdd-107">属性</span><span class="sxs-lookup"><span data-stu-id="1bbdd-107">Attribute</span></span>|<span data-ttu-id="1bbdd-108">说明</span><span class="sxs-lookup"><span data-stu-id="1bbdd-108">Description</span></span>|  
|---------------|-----------------|  
|`idleTimeout`|<span data-ttu-id="1bbdd-109">一个值为正的 <xref:System.TimeSpan>，指定池中的通道在断开前可以空闲的最长时间。</span><span class="sxs-lookup"><span data-stu-id="1bbdd-109">A positive <xref:System.TimeSpan> that specifies the maximum time the channels in the pool can be idle before being disconnected.</span></span> <span data-ttu-id="1bbdd-110">默认值为 00:02:00。</span><span class="sxs-lookup"><span data-stu-id="1bbdd-110">The default is 00:02:00.</span></span>|  
|`leaseTimeout`|<span data-ttu-id="1bbdd-111"><xref:System.TimeSpan>，用于指定从通道返回池到通道关闭之间的时间间隔。</span><span class="sxs-lookup"><span data-stu-id="1bbdd-111">A <xref:System.TimeSpan> that specifies the interval of time after which a channel, when returned to the pool, is closed.</span></span> <span data-ttu-id="1bbdd-112">默认值为 00:10:00。</span><span class="sxs-lookup"><span data-stu-id="1bbdd-112">The default is 00:10:00.</span></span>|  
|`maxOutboundChannelsPerEndpoint`|<span data-ttu-id="1bbdd-113">一个正整数，指定对于每个远程端点可以存储在池中的通道的最大数目。</span><span class="sxs-lookup"><span data-stu-id="1bbdd-113">A positive integer that specifies the maximum number of channels that can be stored in the pool for each remote endpoint.</span></span> <span data-ttu-id="1bbdd-114">默认值为 10。</span><span class="sxs-lookup"><span data-stu-id="1bbdd-114">The default is 10.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="1bbdd-115">子元素</span><span class="sxs-lookup"><span data-stu-id="1bbdd-115">Child Elements</span></span>  

 <span data-ttu-id="1bbdd-116">无。</span><span class="sxs-lookup"><span data-stu-id="1bbdd-116">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="1bbdd-117">父元素</span><span class="sxs-lookup"><span data-stu-id="1bbdd-117">Parent Elements</span></span>  
  
|<span data-ttu-id="1bbdd-118">元素</span><span class="sxs-lookup"><span data-stu-id="1bbdd-118">Element</span></span>|<span data-ttu-id="1bbdd-119">说明</span><span class="sxs-lookup"><span data-stu-id="1bbdd-119">Description</span></span>|  
|-------------|-----------------|  
|[\<oneWay>](oneway.md)|<span data-ttu-id="1bbdd-120">针对自定义绑定启用数据包路由。</span><span class="sxs-lookup"><span data-stu-id="1bbdd-120">Enables packet routing for a custom binding.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="1bbdd-121">备注</span><span class="sxs-lookup"><span data-stu-id="1bbdd-121">Remarks</span></span>  

 <span data-ttu-id="1bbdd-122">配额用作一种策略机制，防止消耗过多资源。</span><span class="sxs-lookup"><span data-stu-id="1bbdd-122">Quotas are used as a policy mechanism to prevent the consumption of excessive resources.</span></span> <span data-ttu-id="1bbdd-123">它们可防止恶意或无意的拒绝服务 (DOS) 攻击。</span><span class="sxs-lookup"><span data-stu-id="1bbdd-123">They prevent Denial of Service (DOS) attacks that are either malicious or unintentional.</span></span> <span data-ttu-id="1bbdd-124">在设置自定义通道的通道配额时使用此元素。</span><span class="sxs-lookup"><span data-stu-id="1bbdd-124">Use this element when setting channel quotas on a custom channel.</span></span>  
  
 <span data-ttu-id="1bbdd-125">`ChannelPoolSettings` 指定三项配额：</span><span class="sxs-lookup"><span data-stu-id="1bbdd-125">`ChannelPoolSettings` specifies three quotas:</span></span>  
  
- <span data-ttu-id="1bbdd-126">`idleTimeout` 配额用于减少通过长时间占用资源来对服务器实施的拒绝服务 (DOS) 攻击。</span><span class="sxs-lookup"><span data-stu-id="1bbdd-126">The `idleTimeout` quota is used to mitigate Denial of Service (DOS) attacks on the server that rely on tying up resources for an extended period of time.</span></span> <span data-ttu-id="1bbdd-127">在客户端，设置正确的值可增加与服务连接的可靠性。</span><span class="sxs-lookup"><span data-stu-id="1bbdd-127">On the client, setting the correct value can increase the reliability of connecting with the service.</span></span> <span data-ttu-id="1bbdd-128">默认值基于资源的保守适度分配。</span><span class="sxs-lookup"><span data-stu-id="1bbdd-128">The default value is based on a conservatively modest allocation of resources.</span></span> <span data-ttu-id="1bbdd-129">该值适用于开发环境和小型安装方案。</span><span class="sxs-lookup"><span data-stu-id="1bbdd-129">It is suitable for a development environment and small installation scenarios.</span></span> <span data-ttu-id="1bbdd-130">如果某个安装耗尽了资源或是连接受到限制，则无论是否还有其他资源可用，服务管理员都应检查该值。</span><span class="sxs-lookup"><span data-stu-id="1bbdd-130">Service administrators should review the value if an installation is running out of resources or if connections are being limited despite the availability of additional resources.</span></span>  
  
- <span data-ttu-id="1bbdd-131">`leaseTimeout` 配额用于与负载均衡器的集成以及提高可靠性。</span><span class="sxs-lookup"><span data-stu-id="1bbdd-131">The `leaseTimeout` quota is used to for integration with load balancers and for improving reliability.</span></span> <span data-ttu-id="1bbdd-132">默认值基于资源的保守分配。</span><span class="sxs-lookup"><span data-stu-id="1bbdd-132">The default value is based on a conservative allocation of resources.</span></span> <span data-ttu-id="1bbdd-133">该值适用于开发环境和小型安装方案。</span><span class="sxs-lookup"><span data-stu-id="1bbdd-133">It is suitable for a development environment and small installation scenarios.</span></span> <span data-ttu-id="1bbdd-134">如果某个安装耗尽了资源或是连接受到限制，则无论是否还有其他资源可用，服务管理员都应检查该值。</span><span class="sxs-lookup"><span data-stu-id="1bbdd-134">Service administrators should review the value if an installation is running out of resources or if connections are being limited despite the availability of additional resources.</span></span>  
  
- <span data-ttu-id="1bbdd-135">`maxOutboundChannelsPerEndpoint` 配额设置服务器与客户端上的缓存限制，用于提高可靠性。</span><span class="sxs-lookup"><span data-stu-id="1bbdd-135">The `maxOutboundChannelsPerEndpoint` quota sets cache limits on both the server and the client and is used to improve reliability.</span></span> <span data-ttu-id="1bbdd-136">其默认值基于资源的保守适度分配，适用于开发环境和小型安装方案。</span><span class="sxs-lookup"><span data-stu-id="1bbdd-136">The default value is based on a conservatively modest allocation of resources that is suitable for a development environment and small installation scenarios.</span></span> <span data-ttu-id="1bbdd-137">如果某个安装耗尽了资源或是连接受到限制，则无论是否还有其他资源可用，服务管理员都应检查该值。</span><span class="sxs-lookup"><span data-stu-id="1bbdd-137">Service administrators should review the value if an installation is running out of resources or if connections are being limited despite the availability of additional resources.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1bbdd-138">请参阅</span><span class="sxs-lookup"><span data-stu-id="1bbdd-138">See also</span></span>

- <xref:System.ServiceModel.Channels.OneWayBindingElement.ChannelPoolSettings%2A>
- <xref:System.ServiceModel.Channels.ChannelPoolSettings>
- <xref:System.ServiceModel.Configuration.OneWayElement.ChannelPoolSettings%2A>
- <xref:System.ServiceModel.Configuration.ChannelPoolSettingsElement>
- <xref:System.ServiceModel.Channels.CustomBinding>
- [\<oneWay>](oneway.md)
- [<span data-ttu-id="1bbdd-139">绑定</span><span class="sxs-lookup"><span data-stu-id="1bbdd-139">Bindings</span></span>](../../../wcf/bindings.md)
- [<span data-ttu-id="1bbdd-140">扩展绑定</span><span class="sxs-lookup"><span data-stu-id="1bbdd-140">Extending Bindings</span></span>](../../../wcf/extending/extending-bindings.md)
- [<span data-ttu-id="1bbdd-141">自定义绑定</span><span class="sxs-lookup"><span data-stu-id="1bbdd-141">Custom Bindings</span></span>](../../../wcf/extending/custom-bindings.md)
- [\<customBinding>](custombinding.md)
