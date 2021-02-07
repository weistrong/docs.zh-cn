---
description: 了解详细信息： <webSocketSettings>
title: <webSocketSettings>
ms.date: 03/30/2017
ms.assetid: bbf97e02-8dd1-4922-acac-3cd33397b249
ms.openlocfilehash: a0b67a0088491c73ed0214191283ae5292a654b0
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99682483"
---
# \<webSocketSettings>

<span data-ttu-id="c66cb-102">用来指定 Web Socket 设置的配置元素。</span><span class="sxs-lookup"><span data-stu-id="c66cb-102">A configuration element used to specify Web Socket settings.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<bindings>**](bindings.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<netHttpBinding>**](nethttpbinding.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<binding>**\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<webSocketSettings>**  
  
## <a name="syntax"></a><span data-ttu-id="c66cb-103">语法</span><span class="sxs-lookup"><span data-stu-id="c66cb-103">Syntax</span></span>  
  
```xml  
<netHttpBinding>
  <binding>
    <webSocketSettings createNotificationOnConnection="Boolean"
                       disablePayloadMasking="Boolean"
                       keepAliveInterval="TimeSpan"
                       maxPendingConnections="Integer"
                       receiveBufferSize="Integer"
                       sendBufferSize="Integer"
                       subProtocol="String"
                       transportUsage="WhenDuplex/Always/Never" />
  </binding>
</netHttpBinding>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="c66cb-104">特性和元素</span><span class="sxs-lookup"><span data-stu-id="c66cb-104">Attributes and Elements</span></span>  

 <span data-ttu-id="c66cb-105">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="c66cb-105">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="c66cb-106">特性</span><span class="sxs-lookup"><span data-stu-id="c66cb-106">Attributes</span></span>  
  
|<span data-ttu-id="c66cb-107">属性</span><span class="sxs-lookup"><span data-stu-id="c66cb-107">Attribute</span></span>|<span data-ttu-id="c66cb-108">说明</span><span class="sxs-lookup"><span data-stu-id="c66cb-108">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="c66cb-109">createNotificationOnConnection</span><span class="sxs-lookup"><span data-stu-id="c66cb-109">createNotificationOnConnection</span></span>|<span data-ttu-id="c66cb-110">指定是否在连接时发送通知。</span><span class="sxs-lookup"><span data-stu-id="c66cb-110">Specifies whether a notification is sent upon connection.</span></span>|  
|<span data-ttu-id="c66cb-111">disablePayloadMasking</span><span class="sxs-lookup"><span data-stu-id="c66cb-111">disablePayloadMasking</span></span>|<span data-ttu-id="c66cb-112">指定是否禁用 Web Socket 掩码。</span><span class="sxs-lookup"><span data-stu-id="c66cb-112">Specifies whether Web Socket masking is disabled.</span></span>|  
|<span data-ttu-id="c66cb-113">keepAliveInterval</span><span class="sxs-lookup"><span data-stu-id="c66cb-113">keepAliveInterval</span></span>|<span data-ttu-id="c66cb-114">指定保持活动状态的间隔。</span><span class="sxs-lookup"><span data-stu-id="c66cb-114">Specifies the keep alive interval.</span></span>|  
|<span data-ttu-id="c66cb-115">maxPendingConnections</span><span class="sxs-lookup"><span data-stu-id="c66cb-115">maxPendingConnections</span></span>|<span data-ttu-id="c66cb-116">指定服务上等待调度的最大连接数。</span><span class="sxs-lookup"><span data-stu-id="c66cb-116">Specifies the maximum number of connections awaiting dispatch on the service.</span></span>|  
|<span data-ttu-id="c66cb-117">receiveBufferSize</span><span class="sxs-lookup"><span data-stu-id="c66cb-117">receiveBufferSize</span></span>|<span data-ttu-id="c66cb-118">指定接收缓冲区的大小。</span><span class="sxs-lookup"><span data-stu-id="c66cb-118">Specifies the size of the receive buffer.</span></span>|  
|<span data-ttu-id="c66cb-119">sendBufferSize</span><span class="sxs-lookup"><span data-stu-id="c66cb-119">sendBufferSize</span></span>|<span data-ttu-id="c66cb-120">指定发送缓冲区的大小。</span><span class="sxs-lookup"><span data-stu-id="c66cb-120">Specifies the size of the send buffer.</span></span>|  
|<span data-ttu-id="c66cb-121">subProtocol</span><span class="sxs-lookup"><span data-stu-id="c66cb-121">subProtocol</span></span>|<span data-ttu-id="c66cb-122">指定 Web Socket 子协议。</span><span class="sxs-lookup"><span data-stu-id="c66cb-122">Specifies the Web Socket subprotocol.</span></span>|  
|<span data-ttu-id="c66cb-123">transportUsage</span><span class="sxs-lookup"><span data-stu-id="c66cb-123">transportUsage</span></span>|<span data-ttu-id="c66cb-124">指定何时使用 Web Socket。</span><span class="sxs-lookup"><span data-stu-id="c66cb-124">Specifies when to use Web Sockets.</span></span>|  
  
## <a name="transportusage-attribute"></a><span data-ttu-id="c66cb-125">transportUsage 特性</span><span class="sxs-lookup"><span data-stu-id="c66cb-125">transportUsage Attribute</span></span>  
  
|<span data-ttu-id="c66cb-126">值</span><span class="sxs-lookup"><span data-stu-id="c66cb-126">Value</span></span>|<span data-ttu-id="c66cb-127">说明</span><span class="sxs-lookup"><span data-stu-id="c66cb-127">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="c66cb-128">WhenDuplex</span><span class="sxs-lookup"><span data-stu-id="c66cb-128">WhenDuplex</span></span>|<span data-ttu-id="c66cb-129">如果为双工协定，则使用 Web Socket 协议。</span><span class="sxs-lookup"><span data-stu-id="c66cb-129">Use the Web Socket protocol when the contract is duplex.</span></span>|  
|<span data-ttu-id="c66cb-130">Always</span><span class="sxs-lookup"><span data-stu-id="c66cb-130">Always</span></span>|<span data-ttu-id="c66cb-131">始终使用 Web Socket 协议，而不管协定类型。</span><span class="sxs-lookup"><span data-stu-id="c66cb-131">Always use the Web Socket protocol regardless of the contract.</span></span>|  
|<span data-ttu-id="c66cb-132">从不</span><span class="sxs-lookup"><span data-stu-id="c66cb-132">Never</span></span>|<span data-ttu-id="c66cb-133">永远不使用 Web Socket 协议。</span><span class="sxs-lookup"><span data-stu-id="c66cb-133">Never use the Web Socket protocol.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="c66cb-134">子元素</span><span class="sxs-lookup"><span data-stu-id="c66cb-134">Child Elements</span></span>  

 <span data-ttu-id="c66cb-135">无</span><span class="sxs-lookup"><span data-stu-id="c66cb-135">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="c66cb-136">父元素</span><span class="sxs-lookup"><span data-stu-id="c66cb-136">Parent Elements</span></span>  
  
|<span data-ttu-id="c66cb-137">元素</span><span class="sxs-lookup"><span data-stu-id="c66cb-137">Element</span></span>|<span data-ttu-id="c66cb-138">说明</span><span class="sxs-lookup"><span data-stu-id="c66cb-138">Description</span></span>|  
|-------------|-----------------|  
|\<netHttpBinding>|<span data-ttu-id="c66cb-139">指定 NetHttpBinding</span><span class="sxs-lookup"><span data-stu-id="c66cb-139">Specifies the NetHttpBinding</span></span>|  
  
## <a name="example"></a><span data-ttu-id="c66cb-140">示例</span><span class="sxs-lookup"><span data-stu-id="c66cb-140">Example</span></span>  

 <span data-ttu-id="c66cb-141">下面的示例演示如何使用 \<webSocketSettings> 元素。</span><span class="sxs-lookup"><span data-stu-id="c66cb-141">The following example shows how to use the \<webSocketSettings> element.</span></span>  
  
```xml  
<netHttpBinding>
  <binding>
    <webSocketSettings createNotificationOnConnection="true"
                       disablePayloadMasking="false"
                       keepAliveInterval="00:10:00"
                       maxPendingConnections="100"
                       receiveBufferSize="1000"
                       sendBufferSize="1000"
                       subProtocol="Soap"
                       transportUsage="WhenDuplex/Always/Never" />
  </binding>
</netHttpBinding>
```  
  
## <a name="see-also"></a><span data-ttu-id="c66cb-142">另请参阅</span><span class="sxs-lookup"><span data-stu-id="c66cb-142">See also</span></span>

- <xref:System.ServiceModel.Channels.Binding>
- <xref:System.ServiceModel.Channels.BindingElement>
- <xref:System.ServiceModel.BasicHttpBinding>
- <xref:System.ServiceModel.Configuration.BasicHttpBindingElement>
- [<span data-ttu-id="c66cb-143">绑定</span><span class="sxs-lookup"><span data-stu-id="c66cb-143">Bindings</span></span>](../../../wcf/bindings.md)
- [<span data-ttu-id="c66cb-144">配置系统提供的绑定</span><span class="sxs-lookup"><span data-stu-id="c66cb-144">Configuring System-Provided Bindings</span></span>](../../../wcf/feature-details/configuring-system-provided-bindings.md)
- [<span data-ttu-id="c66cb-145">使用绑定配置服务和客户端</span><span class="sxs-lookup"><span data-stu-id="c66cb-145">Using Bindings to Configure Services and Clients</span></span>](../../../wcf/using-bindings-to-configure-services-and-clients.md)
- [\<binding>](bindings.md)
