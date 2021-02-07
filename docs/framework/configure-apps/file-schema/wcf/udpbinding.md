---
description: 了解详细信息： <udpBinding>
title: <udpBinding>
ms.date: 03/30/2017
ms.assetid: fa291901-8340-45c6-9c44-5d9281c70bc3
ms.openlocfilehash: 33f8f6abaebe24364273ab43e7ef9ade39a969b0
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99749215"
---
# \<udpBinding>

<span data-ttu-id="5b5d4-102">用于配置 <xref:System.ServiceModel.UdpBinding> 绑定的配置元素。</span><span class="sxs-lookup"><span data-stu-id="5b5d4-102">A configuration element used to configure the <xref:System.ServiceModel.UdpBinding> binding.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<bindings>**](bindings.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<udpBinding>**  
  
## <a name="syntax"></a><span data-ttu-id="5b5d4-103">语法</span><span class="sxs-lookup"><span data-stu-id="5b5d4-103">Syntax</span></span>  
  
```xml  
<udpBinding>
  <binding closeTimeout="TimeSpan"
           duplicateMessageHistoryLength="Integer"
           maxBufferPoolSize="Integer"
           maxBufferSize="Integer"
           maxPendingMessagesTotalSize="Integer"
           maxReceivedMessageSize="Integer"
           maxRetransmitCount="Integer"
           multicastInterfaceId="Integer"
           name="String"
           openTimeout="TimeSpan"
           receiveTimeout="TimeSpan"
           sendTimeout="TimeSpan"
           textEncoding="UnicodeFffeTextEncoding/Utf16TextEncoding/Utf8TextEncoding"
           timeToLive="TimeSpan">
    <readerQuotas maxArrayLength="Integer"
                  maxBytesPerRead="Integer"
                  maxDepth="Integer"
                  maxNameTableCharCount="Integer"
                  maxStringContentLength="Integer" />
  </binding>
</basicHttpBinding>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="5b5d4-104">特性和元素</span><span class="sxs-lookup"><span data-stu-id="5b5d4-104">Attributes and Elements</span></span>  

 <span data-ttu-id="5b5d4-105">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="5b5d4-105">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="5b5d4-106">特性</span><span class="sxs-lookup"><span data-stu-id="5b5d4-106">Attributes</span></span>  
  
|<span data-ttu-id="5b5d4-107">属性</span><span class="sxs-lookup"><span data-stu-id="5b5d4-107">Attribute</span></span>|<span data-ttu-id="5b5d4-108">说明</span><span class="sxs-lookup"><span data-stu-id="5b5d4-108">Description</span></span>|  
|---------------|-----------------|  
|`closeTimeout`|<span data-ttu-id="5b5d4-109">一个 <xref:System.TimeSpan> 值，指定为完成关闭操作提供的时间间隔。</span><span class="sxs-lookup"><span data-stu-id="5b5d4-109">A <xref:System.TimeSpan> value that specifies the interval of time provided for a close operation to complete.</span></span> <span data-ttu-id="5b5d4-110">此值应大于或等于 <xref:System.TimeSpan.Zero>。</span><span class="sxs-lookup"><span data-stu-id="5b5d4-110">This value should be greater than or equal to <xref:System.TimeSpan.Zero>.</span></span> <span data-ttu-id="5b5d4-111">默认值为 00:01:00。</span><span class="sxs-lookup"><span data-stu-id="5b5d4-111">The default is 00:01:00.</span></span>|  
|`duplicateMessageHistoryLength`|<span data-ttu-id="5b5d4-112">一个整数值，指定重复消息历史记录长度。</span><span class="sxs-lookup"><span data-stu-id="5b5d4-112">An integer value that specifies the duplicate message history length.</span></span>|  
|`maxBufferPoolSize`|<span data-ttu-id="5b5d4-113">一个整数值，指定为从通道接收消息的消息缓冲区管理器分配并供其使用的最大内存量。</span><span class="sxs-lookup"><span data-stu-id="5b5d4-113">An integer value that specifies the maximum amount of memory that is allocated for use by the manager of the message buffers that receive messages from the channel.</span></span> <span data-ttu-id="5b5d4-114">默认值为 524288 (0x80000) 字节。</span><span class="sxs-lookup"><span data-stu-id="5b5d4-114">The default value is 524288 (0x80000) bytes.</span></span>|  
|`maxBufferSize`|<span data-ttu-id="5b5d4-115">一个整数值，指定为采用此绑定配置的终结点处理消息时存储消息的缓冲区的最大大小（字节）。</span><span class="sxs-lookup"><span data-stu-id="5b5d4-115">An integer value that specifies the maximum size, in bytes, of a buffer that stores messages while they are processed for an endpoint configured with this binding.</span></span> <span data-ttu-id="5b5d4-116">默认值为 65,536 字节。</span><span class="sxs-lookup"><span data-stu-id="5b5d4-116">The default value is 65,536 bytes.</span></span>|  
|`maxPendingMessagesTotalSize`|<span data-ttu-id="5b5d4-117">一个整数值，指定已经接收但尚未从单个通道实例的输入队列中移除的最大消息数。</span><span class="sxs-lookup"><span data-stu-id="5b5d4-117">An integer value that specifies the maximum number of messages that are received but not yet removed from the input queue for an individual channel instance.</span></span>|  
|`maxReceivedMessageSize`|<span data-ttu-id="5b5d4-118">一个正整数，定义在采用此绑定配置的通道上可以接收的消息的最大消息大小（字节），包括消息头。</span><span class="sxs-lookup"><span data-stu-id="5b5d4-118">A positive integer that defines the maximum message size, in bytes, including headers, for a message that can be received on a channel configured with this binding.</span></span> <span data-ttu-id="5b5d4-119">如果消息对于接收方而言太大，则发送方将收到 SOAP 错误。</span><span class="sxs-lookup"><span data-stu-id="5b5d4-119">The sender receives a SOAP fault if the message is too large for the receiver.</span></span> <span data-ttu-id="5b5d4-120">接收方将删除该消息，并在跟踪日志中创建事件项。</span><span class="sxs-lookup"><span data-stu-id="5b5d4-120">The receiver drops the message and creates an entry of the event in the trace log.</span></span> <span data-ttu-id="5b5d4-121">默认值为 65,536 字节。</span><span class="sxs-lookup"><span data-stu-id="5b5d4-121">The default is 65,536 bytes.</span></span>|  
|`maxRetransmitCount`|<span data-ttu-id="5b5d4-122">一个整数值，指定最大转发消息数。</span><span class="sxs-lookup"><span data-stu-id="5b5d4-122">An integer value that specifies the maximum number of retransmit messages.</span></span>|  
|`multicastInterfaceId`|<span data-ttu-id="5b5d4-123">一个整数值，指定多播接口 ID。</span><span class="sxs-lookup"><span data-stu-id="5b5d4-123">An integer value that specifies the multicast interface ID.</span></span>|  
|`name`|<span data-ttu-id="5b5d4-124">一个包含绑定的配置名称的字符串。</span><span class="sxs-lookup"><span data-stu-id="5b5d4-124">A string that contains the configuration name of the binding.</span></span> <span data-ttu-id="5b5d4-125">因为此值用作绑定的标识，所以它应该是唯一的。</span><span class="sxs-lookup"><span data-stu-id="5b5d4-125">This value should be unique because it is used as an identification for the binding.</span></span> <span data-ttu-id="5b5d4-126">从 .NET Framework 4 开始，绑定和行为不需要具有名称。</span><span class="sxs-lookup"><span data-stu-id="5b5d4-126">Starting with .NET Framework 4, bindings and behaviors are not required to have a name.</span></span> <span data-ttu-id="5b5d4-127">有关默认配置和无值绑定和行为的详细信息，请参阅[WCF 服务的](../../../wcf/samples/simplified-configuration-for-wcf-services.md)[简化配置](../../../wcf/simplified-configuration.md)和简化配置。</span><span class="sxs-lookup"><span data-stu-id="5b5d4-127">For more information about default configuration and nameless bindings and behaviors, see [Simplified Configuration](../../../wcf/simplified-configuration.md) and [Simplified Configuration for WCF Services](../../../wcf/samples/simplified-configuration-for-wcf-services.md).</span></span>|  
|`openTimeout`|<span data-ttu-id="5b5d4-128">一个 <xref:System.TimeSpan> 值，指定为完成打开操作提供的时间间隔。</span><span class="sxs-lookup"><span data-stu-id="5b5d4-128">A <xref:System.TimeSpan> value that specifies the interval of time provided for an open operation to complete.</span></span> <span data-ttu-id="5b5d4-129">此值应大于或等于 <xref:System.TimeSpan.Zero>。</span><span class="sxs-lookup"><span data-stu-id="5b5d4-129">This value should be greater than or equal to <xref:System.TimeSpan.Zero>.</span></span> <span data-ttu-id="5b5d4-130">默认值为 00:01:00。</span><span class="sxs-lookup"><span data-stu-id="5b5d4-130">The default is 00:01:00.</span></span>|  
|`receiveTimeout`|<span data-ttu-id="5b5d4-131">一个 <xref:System.TimeSpan> 值，指定为完成接收操作提供的时间间隔。</span><span class="sxs-lookup"><span data-stu-id="5b5d4-131">A <xref:System.TimeSpan> value that specifies the interval of time provided for a receive operation to complete.</span></span> <span data-ttu-id="5b5d4-132">此值应大于或等于 <xref:System.TimeSpan.Zero>。</span><span class="sxs-lookup"><span data-stu-id="5b5d4-132">This value should be greater than or equal to <xref:System.TimeSpan.Zero>.</span></span> <span data-ttu-id="5b5d4-133">默认值为 00:10:00。</span><span class="sxs-lookup"><span data-stu-id="5b5d4-133">The default is 00:10:00.</span></span>|  
|`sendTimeout`|<span data-ttu-id="5b5d4-134">一个 <xref:System.TimeSpan> 值，指定为完成发送操作提供的时间间隔。</span><span class="sxs-lookup"><span data-stu-id="5b5d4-134">A <xref:System.TimeSpan> value that specifies the interval of time provided for a send operation to complete.</span></span> <span data-ttu-id="5b5d4-135">此值应大于或等于 <xref:System.TimeSpan.Zero>。</span><span class="sxs-lookup"><span data-stu-id="5b5d4-135">This value should be greater than or equal to <xref:System.TimeSpan.Zero>.</span></span> <span data-ttu-id="5b5d4-136">默认值为 00:01:00。</span><span class="sxs-lookup"><span data-stu-id="5b5d4-136">The default is 00:01:00.</span></span>|  
|`textEncoding`|<span data-ttu-id="5b5d4-137">设置要用来在绑定上发出消息的字符集编码。</span><span class="sxs-lookup"><span data-stu-id="5b5d4-137">Sets the character set encoding to be used for emitting messages on the binding.</span></span> <span data-ttu-id="5b5d4-138">有效值包括以下值：</span><span class="sxs-lookup"><span data-stu-id="5b5d4-138">Valid values include the following:</span></span><br /><br /> <span data-ttu-id="5b5d4-139">-BigEndianUnicode： Unicode BigEndian 编码。</span><span class="sxs-lookup"><span data-stu-id="5b5d4-139">-   BigEndianUnicode: Unicode BigEndian encoding.</span></span><br /><span data-ttu-id="5b5d4-140">-Unicode：16位编码。</span><span class="sxs-lookup"><span data-stu-id="5b5d4-140">-   Unicode: 16-bit encoding.</span></span><br /><span data-ttu-id="5b5d4-141">-UTF8：8位编码</span><span class="sxs-lookup"><span data-stu-id="5b5d4-141">-   UTF8: 8-bit encoding</span></span><br /><br /> <span data-ttu-id="5b5d4-142">默认编码为 UTF8。</span><span class="sxs-lookup"><span data-stu-id="5b5d4-142">The default is UTF8.</span></span> <span data-ttu-id="5b5d4-143">此属性的类型为 <xref:System.Text.Encoding>。</span><span class="sxs-lookup"><span data-stu-id="5b5d4-143">This attribute is of type <xref:System.Text.Encoding>.</span></span>|  
|`timeToLive`|<span data-ttu-id="5b5d4-144">一个时间范围值，指定绑定处于活动状态的时间。</span><span class="sxs-lookup"><span data-stu-id="5b5d4-144">A timespan value that specifies the time to live for the binding.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="5b5d4-145">子元素</span><span class="sxs-lookup"><span data-stu-id="5b5d4-145">Child Elements</span></span>  
  
|<span data-ttu-id="5b5d4-146">元素</span><span class="sxs-lookup"><span data-stu-id="5b5d4-146">Element</span></span>|<span data-ttu-id="5b5d4-147">说明</span><span class="sxs-lookup"><span data-stu-id="5b5d4-147">Description</span></span>|  
|-------------|-----------------|  
|[\<readerQuotas>](/previous-versions/dotnet/netframework-4.0/ms731325(v=vs.100))|<span data-ttu-id="5b5d4-148">定义可由采用此绑定配置的终结点进行处理的 SOAP 消息的复杂性约束。</span><span class="sxs-lookup"><span data-stu-id="5b5d4-148">Defines the constraints on the complexity of SOAP messages that can be processed by endpoints configured with this binding.</span></span> <span data-ttu-id="5b5d4-149">此元素的类型为 <xref:System.ServiceModel.Configuration.XmlDictionaryReaderQuotasElement>。</span><span class="sxs-lookup"><span data-stu-id="5b5d4-149">This element is of type <xref:System.ServiceModel.Configuration.XmlDictionaryReaderQuotasElement>.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="5b5d4-150">父元素</span><span class="sxs-lookup"><span data-stu-id="5b5d4-150">Parent Elements</span></span>  
  
|<span data-ttu-id="5b5d4-151">元素</span><span class="sxs-lookup"><span data-stu-id="5b5d4-151">Element</span></span>|<span data-ttu-id="5b5d4-152">说明</span><span class="sxs-lookup"><span data-stu-id="5b5d4-152">Description</span></span>|  
|-------------|-----------------|  
|[\<bindings>](bindings.md)|<span data-ttu-id="5b5d4-153">此元素包含标准绑定和自定义绑定的集合。</span><span class="sxs-lookup"><span data-stu-id="5b5d4-153">This element holds a collection of standard and custom bindings.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="5b5d4-154">备注</span><span class="sxs-lookup"><span data-stu-id="5b5d4-154">Remarks</span></span>  

 <span data-ttu-id="5b5d4-155">UdpBinding 允许 WCF 服务通过 UDP 传输进行通信。</span><span class="sxs-lookup"><span data-stu-id="5b5d4-155">The UdpBinding allows WCF services to communicate over the UDP transport.</span></span> <span data-ttu-id="5b5d4-156">它允许 "火灾和遗忘" 消息交换，其中客户端向服务发送一条消息，而不希望返回响应。</span><span class="sxs-lookup"><span data-stu-id="5b5d4-156">It allows for "fire and forget" message exchanges where a client sends a message to a service and expects no response back.</span></span>  
  
## <a name="example"></a><span data-ttu-id="5b5d4-157">示例</span><span class="sxs-lookup"><span data-stu-id="5b5d4-157">Example</span></span>  

 <span data-ttu-id="5b5d4-158">下面的示例演示如何 <xref:System.ServiceModel.UdpBinding> 使用 <`udpBinding`> 元素配置。</span><span class="sxs-lookup"><span data-stu-id="5b5d4-158">The following example shows how to configure the <xref:System.ServiceModel.UdpBinding> using the <`udpBinding`> element.</span></span>  
  
```xml  
<udpBinding>
  <binding  closeTimeout="00:10:00"
            duplicateMessageHistoryLength="100"
            maxBufferPoolSize="100"
            maxPendingMessagesTotalSize="100000"
            maxReceivedMessageSize="65536"
            maxRetransmitCount="10"
            multicastInterfaceId="00000"
            name="myUdpBinding"
            openTimeout="00:10:00"
            receiveTimeout="00:10:00"
            sendTimeout="00:10:00"
            textEncoding="utf-8"
            timeToLive="00:10:00">
    <readerQuotas />
  </binding>
</udpBinding>
```  
  
## <a name="see-also"></a><span data-ttu-id="5b5d4-159">请参阅</span><span class="sxs-lookup"><span data-stu-id="5b5d4-159">See also</span></span>

- <xref:System.ServiceModel.Channels.Binding>
- <xref:System.ServiceModel.Channels.BindingElement>
- <xref:System.ServiceModel.BasicHttpBinding>
- <xref:System.ServiceModel.Configuration.BasicHttpBindingElement>
- [<span data-ttu-id="5b5d4-160">绑定</span><span class="sxs-lookup"><span data-stu-id="5b5d4-160">Bindings</span></span>](../../../wcf/bindings.md)
- [<span data-ttu-id="5b5d4-161">配置系统提供的绑定</span><span class="sxs-lookup"><span data-stu-id="5b5d4-161">Configuring System-Provided Bindings</span></span>](../../../wcf/feature-details/configuring-system-provided-bindings.md)
- [<span data-ttu-id="5b5d4-162">使用绑定配置服务和客户端</span><span class="sxs-lookup"><span data-stu-id="5b5d4-162">Using Bindings to Configure Services and Clients</span></span>](../../../wcf/using-bindings-to-configure-services-and-clients.md)
- [\<binding>](bindings.md)
