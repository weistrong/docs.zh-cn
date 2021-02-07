---
description: 了解详细信息： <peerTransport>
title: <peerTransport>
ms.date: 03/30/2017
ms.assetid: c1a5013a-9dd4-4a27-b114-795b8b323177
ms.openlocfilehash: babc4196c63d46b7515ac67812d5d584eb3ffcac
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99683614"
---
# \<peerTransport>

<span data-ttu-id="43509-102">定义自定义绑定的对等传输。</span><span class="sxs-lookup"><span data-stu-id="43509-102">Defines a peer transport for a custom binding.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<bindings>**](bindings.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<customBinding>**](custombinding.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<binding>**\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<peerTransport>**  
  
## <a name="syntax"></a><span data-ttu-id="43509-103">语法</span><span class="sxs-lookup"><span data-stu-id="43509-103">Syntax</span></span>  
  
```xml  
<peerTransport listenIpAddress="String"
               maxBufferPoolSize="Integer"
               maxReceivedMessageSize="Integer"
               port="Integer">
  <security>
  </security>
</peerTransport>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="43509-104">特性和元素</span><span class="sxs-lookup"><span data-stu-id="43509-104">Attributes and Elements</span></span>  

 <span data-ttu-id="43509-105">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="43509-105">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="43509-106">特性</span><span class="sxs-lookup"><span data-stu-id="43509-106">Attributes</span></span>  
  
|<span data-ttu-id="43509-107">属性</span><span class="sxs-lookup"><span data-stu-id="43509-107">Attribute</span></span>|<span data-ttu-id="43509-108">说明</span><span class="sxs-lookup"><span data-stu-id="43509-108">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="43509-109">listenIpAddress</span><span class="sxs-lookup"><span data-stu-id="43509-109">listenIpAddress</span></span>|<span data-ttu-id="43509-110">一个字符串，指定对等节点将在其上侦听 TCP 消息的 IP 地址。</span><span class="sxs-lookup"><span data-stu-id="43509-110">A string that specifies an IP address on which the peer node will listen for TCP messages.</span></span> <span data-ttu-id="43509-111">默认值为 `null`。</span><span class="sxs-lookup"><span data-stu-id="43509-111">The default is `null`.</span></span>|  
|<span data-ttu-id="43509-112">maxBufferPoolSize</span><span class="sxs-lookup"><span data-stu-id="43509-112">maxBufferPoolSize</span></span>|<span data-ttu-id="43509-113">一个正整数，指定缓冲池的最大大小。</span><span class="sxs-lookup"><span data-stu-id="43509-113">A positive integer that specifies the maximum size of the buffer pool.</span></span> <span data-ttu-id="43509-114">默认值为 524288。</span><span class="sxs-lookup"><span data-stu-id="43509-114">The default is 524288.</span></span><br /><br /> <span data-ttu-id="43509-115">WCF 的许多组件使用缓冲区。</span><span class="sxs-lookup"><span data-stu-id="43509-115">Many parts of WCF use buffers.</span></span> <span data-ttu-id="43509-116">每次使用缓冲区时，创建和销毁它们都将占用大量资源，而缓冲区的垃圾回收过程也是如此。</span><span class="sxs-lookup"><span data-stu-id="43509-116">Creating and destroying buffers each time they are used is expensive, and garbage collection for buffers is also expensive.</span></span> <span data-ttu-id="43509-117">利用缓冲池，可以从缓冲池中获得缓冲区，使用缓冲区，然后在完成工作后将其返回给缓冲池。</span><span class="sxs-lookup"><span data-stu-id="43509-117">With buffer pools, you can take a buffer from the pool, use it, and return it to the pool once you are done.</span></span> <span data-ttu-id="43509-118">这样就避免了创建和销毁缓冲区的系统开销。</span><span class="sxs-lookup"><span data-stu-id="43509-118">Thus the overhead in creating and destroying buffers is avoided.</span></span>|  
|<span data-ttu-id="43509-119">maxReceivedMessageSize</span><span class="sxs-lookup"><span data-stu-id="43509-119">maxReceivedMessageSize</span></span>|<span data-ttu-id="43509-120">一个正整数，定义包括标头在内的最大消息大小（以字节为单位）。</span><span class="sxs-lookup"><span data-stu-id="43509-120">A positive integer that defines the maximum message size in bytes including headers.</span></span> <span data-ttu-id="43509-121">如果消息对于接收方而言太大，则消息发送方将收到 SOAP 错误。</span><span class="sxs-lookup"><span data-stu-id="43509-121">The sender of a message receives a SOAP fault when the message is too large for the receiver.</span></span> <span data-ttu-id="43509-122">接收方将删除该消息，并在跟踪日志中创建事件项。</span><span class="sxs-lookup"><span data-stu-id="43509-122">The receiver drops the message and creates an entry of the event in the trace log.</span></span> <span data-ttu-id="43509-123">默认值为 65536。</span><span class="sxs-lookup"><span data-stu-id="43509-123">The default is 65536.</span></span>|  
|<span data-ttu-id="43509-124">port</span><span class="sxs-lookup"><span data-stu-id="43509-124">port</span></span>|<span data-ttu-id="43509-125">一个整数，指定此绑定将用于处理对等通道 TCP 消息的网络接口端口。</span><span class="sxs-lookup"><span data-stu-id="43509-125">An integer that specifies the network interface port on which this binding will process peer channel TCP messages.</span></span> <span data-ttu-id="43509-126">该值必须介于 <xref:System.Net.IPEndPoint.MinPort> 和 <xref:System.Net.IPEndPoint.MaxPort> 之间。</span><span class="sxs-lookup"><span data-stu-id="43509-126">This value must be between <xref:System.Net.IPEndPoint.MinPort> and <xref:System.Net.IPEndPoint.MaxPort>.</span></span> <span data-ttu-id="43509-127">默认值为 0。</span><span class="sxs-lookup"><span data-stu-id="43509-127">The default is 0.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="43509-128">子元素</span><span class="sxs-lookup"><span data-stu-id="43509-128">Child Elements</span></span>  
  
|<span data-ttu-id="43509-129">元素</span><span class="sxs-lookup"><span data-stu-id="43509-129">Element</span></span>|<span data-ttu-id="43509-130">说明</span><span class="sxs-lookup"><span data-stu-id="43509-130">Description</span></span>|  
|-------------|-----------------|  
|[\<security>](security-of-peertransport.md)|<span data-ttu-id="43509-131">定义此传输的安全设置。</span><span class="sxs-lookup"><span data-stu-id="43509-131">Defines the security settings for this transport.</span></span> <span data-ttu-id="43509-132">此元素的类型为 <xref:System.ServiceModel.Configuration.PeerSecurityElement>。</span><span class="sxs-lookup"><span data-stu-id="43509-132">This element is of type <xref:System.ServiceModel.Configuration.PeerSecurityElement>.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="43509-133">父元素</span><span class="sxs-lookup"><span data-stu-id="43509-133">Parent Elements</span></span>  
  
|<span data-ttu-id="43509-134">元素</span><span class="sxs-lookup"><span data-stu-id="43509-134">Element</span></span>|<span data-ttu-id="43509-135">说明</span><span class="sxs-lookup"><span data-stu-id="43509-135">Description</span></span>|  
|-------------|-----------------|  
|[\<binding>](bindings.md)|<span data-ttu-id="43509-136">定义自定义绑定的所有绑定功能。</span><span class="sxs-lookup"><span data-stu-id="43509-136">Defines all binding capabilities of the custom binding.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="43509-137">备注</span><span class="sxs-lookup"><span data-stu-id="43509-137">Remarks</span></span>  

 <span data-ttu-id="43509-138">此传输不可用于包含请求/答复操作的协定。</span><span class="sxs-lookup"><span data-stu-id="43509-138">This transport cannot be used with contracts that have request/reply operations.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="43509-139">请参阅</span><span class="sxs-lookup"><span data-stu-id="43509-139">See also</span></span>

- <xref:System.ServiceModel.Configuration.PeerTransportElement>
- <xref:System.ServiceModel.Channels.PeerTransportBindingElement>
- <xref:System.ServiceModel.Channels.TransportBindingElement>
- <xref:System.ServiceModel.Channels.CustomBinding>
- [<span data-ttu-id="43509-140">传输</span><span class="sxs-lookup"><span data-stu-id="43509-140">Transports</span></span>](../../../wcf/feature-details/transports.md)
- [<span data-ttu-id="43509-141">选择传输方式</span><span class="sxs-lookup"><span data-stu-id="43509-141">Choosing a Transport</span></span>](../../../wcf/feature-details/choosing-a-transport.md)
- [<span data-ttu-id="43509-142">绑定</span><span class="sxs-lookup"><span data-stu-id="43509-142">Bindings</span></span>](../../../wcf/bindings.md)
- [<span data-ttu-id="43509-143">扩展绑定</span><span class="sxs-lookup"><span data-stu-id="43509-143">Extending Bindings</span></span>](../../../wcf/extending/extending-bindings.md)
- [<span data-ttu-id="43509-144">自定义绑定</span><span class="sxs-lookup"><span data-stu-id="43509-144">Custom Bindings</span></span>](../../../wcf/extending/custom-bindings.md)
- [\<customBinding>](custombinding.md)
