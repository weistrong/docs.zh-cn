---
description: 了解详细信息： <namedPipeTransport>
title: <namedPipeTransport>
ms.date: 03/30/2017
ms.assetid: 9fc3f42f-43e2-4ab1-8bc7-3c95a9220df1
ms.openlocfilehash: 68714404492be92ce789dbde95a39199f5de16d4
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99684095"
---
# \<namedPipeTransport>

<span data-ttu-id="0a4cb-102">定义传输，使通道在被包括到自定义绑定中时使用命名管道来传输消息。</span><span class="sxs-lookup"><span data-stu-id="0a4cb-102">Defines a transport that causes a channel to transfer messages using named pipes when it is included in a custom binding.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<bindings>**](bindings.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<customBinding>**](custombinding.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<binding>**\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<namedPipeTransport>**  
  
## <a name="syntax"></a><span data-ttu-id="0a4cb-103">语法</span><span class="sxs-lookup"><span data-stu-id="0a4cb-103">Syntax</span></span>  
  
```xml  
<namedPipeTransport channelInitializationTimeout="TimeSpan"
                    connectionBufferSize="Integer"
                    hostNameComparisonMode="StrongWildcard/Exact/WeakWildcard"
                    manualAddressing="Boolean"
                    maxBufferPoolSize="Integer"
                    maxBufferSize="Integer"
                    maxOutputDelay="TimeSpan"
                    maxPendingAccepts="Integer"
                    maxPendingConnections="Integer"
                    maxReceivedMessageSize="Integer"
                    transferMode="Buffered/Streamed/StreamedRequest/StreamedResponse">
  <connectionPoolSettings groupName="String"
                          idleTimeout="TimeSpan"
                          maxOutboundConnectionsPerEndpoint="Integer" />
</namedPipeTransport>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="0a4cb-104">特性和元素</span><span class="sxs-lookup"><span data-stu-id="0a4cb-104">Attributes and Elements</span></span>  

<span data-ttu-id="0a4cb-105">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="0a4cb-105">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="0a4cb-106">特性</span><span class="sxs-lookup"><span data-stu-id="0a4cb-106">Attributes</span></span>  

<span data-ttu-id="0a4cb-107">无。</span><span class="sxs-lookup"><span data-stu-id="0a4cb-107">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="0a4cb-108">子元素</span><span class="sxs-lookup"><span data-stu-id="0a4cb-108">Child Elements</span></span>  
  
|<span data-ttu-id="0a4cb-109">元素</span><span class="sxs-lookup"><span data-stu-id="0a4cb-109">Element</span></span>|<span data-ttu-id="0a4cb-110">说明</span><span class="sxs-lookup"><span data-stu-id="0a4cb-110">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="0a4cb-111">ChannelInitializationTimeout</span><span class="sxs-lookup"><span data-stu-id="0a4cb-111">ChannelInitializationTimeout</span></span>|<span data-ttu-id="0a4cb-112">获取或设置确定通道在断开连接前可处于初始化状态的最长时间的 <xref:System.TimeSpan>。</span><span class="sxs-lookup"><span data-stu-id="0a4cb-112">Gets or sets a <xref:System.TimeSpan> that determines the maximum time a channel can be in the initialization status before being disconnected.</span></span>|  
|<span data-ttu-id="0a4cb-113">ConnectionBufferSize</span><span class="sxs-lookup"><span data-stu-id="0a4cb-113">ConnectionBufferSize</span></span>|<span data-ttu-id="0a4cb-114">获取或设置用于从客户端或服务传输网络上的序列化消息块的缓冲区大小。</span><span class="sxs-lookup"><span data-stu-id="0a4cb-114">Gets or sets the size of the buffer used to transmit a chunk of the serialized message on the wire from the client or service.</span></span>|  
|<span data-ttu-id="0a4cb-115">hostNameComparisonMode</span><span class="sxs-lookup"><span data-stu-id="0a4cb-115">hostNameComparisonMode</span></span>|<span data-ttu-id="0a4cb-116">获取或设置一个值，该值指示在对 URI 进行匹配时，是否使用主机名来访问服务。</span><span class="sxs-lookup"><span data-stu-id="0a4cb-116">Gets or sets a value that indicates whether the hostname is used to reach the service when matching on the URI.</span></span>|  
|<span data-ttu-id="0a4cb-117">manualAddressing</span><span class="sxs-lookup"><span data-stu-id="0a4cb-117">manualAddressing</span></span>|<span data-ttu-id="0a4cb-118">获取或设置一个值，该值指示是否要求对消息进行手动寻址。</span><span class="sxs-lookup"><span data-stu-id="0a4cb-118">Gets or sets a value that indicates whether manual addressing of the message is required.</span></span>|  
|<span data-ttu-id="0a4cb-119">maxBufferPoolSize</span><span class="sxs-lookup"><span data-stu-id="0a4cb-119">maxBufferPoolSize</span></span>|<span data-ttu-id="0a4cb-120">获取或设置传输消息使用的任何缓冲池的最大字节大小。</span><span class="sxs-lookup"><span data-stu-id="0a4cb-120">Gets or sets the maximum size, in bytes, of any buffer pools used by the transport.</span></span>|  
|<span data-ttu-id="0a4cb-121">maxBufferSize</span><span class="sxs-lookup"><span data-stu-id="0a4cb-121">maxBufferSize</span></span>|<span data-ttu-id="0a4cb-122">获取或设置要使用的缓冲区的最大大小。</span><span class="sxs-lookup"><span data-stu-id="0a4cb-122">Gets or sets the maximum size of the buffer to use.</span></span> <span data-ttu-id="0a4cb-123">对于经过流处理的消息，该值最少应为以缓冲模式读取的消息头的最大可能大小。</span><span class="sxs-lookup"><span data-stu-id="0a4cb-123">For streamed messages, this value should be at least the maximum possible size of the message headers, which are read in buffered mode.</span></span>|  
|<span data-ttu-id="0a4cb-124">maxOutputDelay</span><span class="sxs-lookup"><span data-stu-id="0a4cb-124">maxOutputDelay</span></span>|<span data-ttu-id="0a4cb-125">获取或设置消息块或完整消息在发出之前可以在内存中保持缓冲的最大时间间隔。</span><span class="sxs-lookup"><span data-stu-id="0a4cb-125">Gets or sets the maximum interval of time that a chunk of a message or a full message can remain buffered in memory before being sent out.</span></span>|  
|<span data-ttu-id="0a4cb-126">maxPendingAccepts</span><span class="sxs-lookup"><span data-stu-id="0a4cb-126">maxPendingAccepts</span></span>|<span data-ttu-id="0a4cb-127">获取或设置服务可等待许可证处理至服务的传入连接的最大通道数量。</span><span class="sxs-lookup"><span data-stu-id="0a4cb-127">Gets or sets the maximum number of channels a service can have waiting on a listener for processing incoming connections to the service.</span></span>|  
|<span data-ttu-id="0a4cb-128">maxPendingConnections</span><span class="sxs-lookup"><span data-stu-id="0a4cb-128">maxPendingConnections</span></span>|<span data-ttu-id="0a4cb-129">获取或设置在服务上等待调度的最大连接数。</span><span class="sxs-lookup"><span data-stu-id="0a4cb-129">Gets or sets the maximum number of connections awaiting dispatch on the service.</span></span>|  
|<span data-ttu-id="0a4cb-130">maxReceivedMessageSize</span><span class="sxs-lookup"><span data-stu-id="0a4cb-130">maxReceivedMessageSize</span></span>|<span data-ttu-id="0a4cb-131">获取和设置允许接收的最大消息大小（以字节为单位）。</span><span class="sxs-lookup"><span data-stu-id="0a4cb-131">Gets and sets the maximum allowable message size, in bytes, that can be received.</span></span>|  
|<span data-ttu-id="0a4cb-132">transferMode</span><span class="sxs-lookup"><span data-stu-id="0a4cb-132">transferMode</span></span>|<span data-ttu-id="0a4cb-133">获取或设置一个值，该值指示通过面向连接的传输对消息进行缓冲还是流处理。</span><span class="sxs-lookup"><span data-stu-id="0a4cb-133">Gets or sets a value that indicates whether the messages are buffered or streamed with the connection-oriented transport.</span></span>|  
|[<span data-ttu-id="0a4cb-134">\<namedPipeTransport> 的 \<connectionPoolSettings></span><span class="sxs-lookup"><span data-stu-id="0a4cb-134">\<connectionPoolSettings> of \<namedPipeTransport></span></span>](connectionpoolsettings.md)|<span data-ttu-id="0a4cb-135">指定命名管道绑定的其他连接池设置。</span><span class="sxs-lookup"><span data-stu-id="0a4cb-135">Specifies additional connection pool settings for a Named Pipe binding.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="0a4cb-136">父元素</span><span class="sxs-lookup"><span data-stu-id="0a4cb-136">Parent Elements</span></span>  
  
|<span data-ttu-id="0a4cb-137">元素</span><span class="sxs-lookup"><span data-stu-id="0a4cb-137">Element</span></span>|<span data-ttu-id="0a4cb-138">说明</span><span class="sxs-lookup"><span data-stu-id="0a4cb-138">Description</span></span>|  
|-------------|-----------------|  
|[\<binding>](bindings.md)|<span data-ttu-id="0a4cb-139">定义自定义绑定的所有绑定功能。</span><span class="sxs-lookup"><span data-stu-id="0a4cb-139">Defines all binding capabilities of the custom binding.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="0a4cb-140">备注</span><span class="sxs-lookup"><span data-stu-id="0a4cb-140">Remarks</span></span>  

<span data-ttu-id="0a4cb-141">此传输使用“net.pipe://hostname/path”形式的 URI。</span><span class="sxs-lookup"><span data-stu-id="0a4cb-141">This transport uses URIs of the form "net.pipe://hostname/path".</span></span> <span data-ttu-id="0a4cb-142">其他 URI 组件是可选的。</span><span class="sxs-lookup"><span data-stu-id="0a4cb-142">Other URI components are optional.</span></span>  
  
<span data-ttu-id="0a4cb-143">`namedPipeTransport` 元素是创建实现命名管道传输协议的自定义绑定的起始点。</span><span class="sxs-lookup"><span data-stu-id="0a4cb-143">The `namedPipeTransport` element is the starting point for creating a custom binding that implements the named pipes transport protocol.</span></span> <span data-ttu-id="0a4cb-144">此传输用于计算机上的 WCF (Windows Communication Foundation) 到 WCF 的通信。</span><span class="sxs-lookup"><span data-stu-id="0a4cb-144">This transport is used for on-machine Windows Communication Foundation (WCF)-to-WCF communication.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0a4cb-145">请参阅</span><span class="sxs-lookup"><span data-stu-id="0a4cb-145">See also</span></span>

- <xref:System.ServiceModel.Configuration.NamedPipeTransportElement>
- <xref:System.ServiceModel.Channels.NamedPipeTransportBindingElement>
- <xref:System.ServiceModel.Channels.TransportBindingElement>
- <xref:System.ServiceModel.Channels.CustomBinding>
- [<span data-ttu-id="0a4cb-146">传输</span><span class="sxs-lookup"><span data-stu-id="0a4cb-146">Transports</span></span>](../../../wcf/feature-details/transports.md)
- [<span data-ttu-id="0a4cb-147">选择传输方式</span><span class="sxs-lookup"><span data-stu-id="0a4cb-147">Choosing a Transport</span></span>](../../../wcf/feature-details/choosing-a-transport.md)
- [<span data-ttu-id="0a4cb-148">绑定</span><span class="sxs-lookup"><span data-stu-id="0a4cb-148">Bindings</span></span>](../../../wcf/bindings.md)
- [<span data-ttu-id="0a4cb-149">扩展绑定</span><span class="sxs-lookup"><span data-stu-id="0a4cb-149">Extending Bindings</span></span>](../../../wcf/extending/extending-bindings.md)
- [<span data-ttu-id="0a4cb-150">自定义绑定</span><span class="sxs-lookup"><span data-stu-id="0a4cb-150">Custom Bindings</span></span>](../../../wcf/extending/custom-bindings.md)
- [\<customBinding>](custombinding.md)
