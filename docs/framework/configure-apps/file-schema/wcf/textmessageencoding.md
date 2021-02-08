---
description: 了解详细信息： <textMessageEncoding>
title: <textMessageEncoding>
ms.date: 03/30/2017
ms.assetid: e6d834d0-356e-45eb-b530-bbefbb9ec3f0
ms.openlocfilehash: a8c7820b2e22152850d6d21c5091e328feb7a9f3
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99786598"
---
# \<textMessageEncoding>

<span data-ttu-id="488e9-102">指定用于基于文本的 XML 消息的字符编码和消息版本控制。</span><span class="sxs-lookup"><span data-stu-id="488e9-102">Specifies the character encoding and message versioning used for text-based XML messages.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<bindings>**](bindings.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<customBinding>**](custombinding.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<binding>**\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<textMessageEncoding>**  
  
## <a name="syntax"></a><span data-ttu-id="488e9-103">语法</span><span class="sxs-lookup"><span data-stu-id="488e9-103">Syntax</span></span>  
  
```xml  
<textMessageEncoding maxReadPoolSize="Integer"
                     maxWritePoolSize="Integer"
                     messageVersion="Soap11Addressing10/Soap12Addressing10"
                     writeEncoding="UnicodeFffeTextEncoding/Utf16TextEncoding/Utf8TextEncoding" />
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="488e9-104">特性和元素</span><span class="sxs-lookup"><span data-stu-id="488e9-104">Attributes and Elements</span></span>  

 <span data-ttu-id="488e9-105">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="488e9-105">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="488e9-106">特性</span><span class="sxs-lookup"><span data-stu-id="488e9-106">Attributes</span></span>  
  
|<span data-ttu-id="488e9-107">属性</span><span class="sxs-lookup"><span data-stu-id="488e9-107">Attribute</span></span>|<span data-ttu-id="488e9-108">说明</span><span class="sxs-lookup"><span data-stu-id="488e9-108">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="488e9-109">maxReadPoolSize</span><span class="sxs-lookup"><span data-stu-id="488e9-109">maxReadPoolSize</span></span>|<span data-ttu-id="488e9-110">一个整数，指定在无需分配新读取器的情况下可以同时读取的消息数。</span><span class="sxs-lookup"><span data-stu-id="488e9-110">An integer that specifies how many messages can be read simultaneously without allocating new readers.</span></span> <span data-ttu-id="488e9-111">池越大，系统允许的活动峰值就越大，但工作集也会随之增大。</span><span class="sxs-lookup"><span data-stu-id="488e9-111">Larger pool sizes make the system more tolerant to activity spikes at the cost of a larger working set.</span></span> <span data-ttu-id="488e9-112">默认值为 64。</span><span class="sxs-lookup"><span data-stu-id="488e9-112">The default is 64.</span></span>|  
|<span data-ttu-id="488e9-113">maxWritePoolSize</span><span class="sxs-lookup"><span data-stu-id="488e9-113">maxWritePoolSize</span></span>|<span data-ttu-id="488e9-114">一个整数，指定在无需分配新编写器的情况下可以同时发送的消息数。</span><span class="sxs-lookup"><span data-stu-id="488e9-114">An integer that specifies how many messages can be sent simultaneously without allocating new writers.</span></span> <span data-ttu-id="488e9-115">池越大，系统允许的活动峰值就越大，但工作集也会随之增大。</span><span class="sxs-lookup"><span data-stu-id="488e9-115">Larger pool sizes make the system more tolerant to activity spikes at the cost of a larger working set.</span></span> <span data-ttu-id="488e9-116">默认值为 16。</span><span class="sxs-lookup"><span data-stu-id="488e9-116">The default is 16.</span></span>|  
|<span data-ttu-id="488e9-117">messageVersion</span><span class="sxs-lookup"><span data-stu-id="488e9-117">messageVersion</span></span>|<span data-ttu-id="488e9-118">指定使用此绑定发送的消息的 SOAP 版本。</span><span class="sxs-lookup"><span data-stu-id="488e9-118">Specifies the SOAP version of the messages sent using the binding.</span></span> <span data-ttu-id="488e9-119">有效值为</span><span class="sxs-lookup"><span data-stu-id="488e9-119">Valid values are</span></span><br /><br /> <span data-ttu-id="488e9-120">- Soap11Addressing10</span><span class="sxs-lookup"><span data-stu-id="488e9-120">-   Soap11Addressing10</span></span><br /><span data-ttu-id="488e9-121">- Soap12Addressing10</span><span class="sxs-lookup"><span data-stu-id="488e9-121">-   Soap12Addressing10</span></span><br /><span data-ttu-id="488e9-122">- Soap11</span><span class="sxs-lookup"><span data-stu-id="488e9-122">-   Soap11</span></span><br /><span data-ttu-id="488e9-123">- Soap12</span><span class="sxs-lookup"><span data-stu-id="488e9-123">-  Soap12</span></span><br /><br /><span data-ttu-id="488e9-124">默认值为 Soap12Addressing10。</span><span class="sxs-lookup"><span data-stu-id="488e9-124">The default is Soap12Addressing10.</span></span> <span data-ttu-id="488e9-125">此属性的类型为 <xref:System.ServiceModel.Channels.MessageVersion>。</span><span class="sxs-lookup"><span data-stu-id="488e9-125">This attribute is of type <xref:System.ServiceModel.Channels.MessageVersion>.</span></span>|  
|<span data-ttu-id="488e9-126">writeEncoding</span><span class="sxs-lookup"><span data-stu-id="488e9-126">writeEncoding</span></span>|<span data-ttu-id="488e9-127">指定要用来在绑定上发出消息的字符集编码。</span><span class="sxs-lookup"><span data-stu-id="488e9-127">Specifies the character set encoding to be used for emitting messages on the binding.</span></span> <span data-ttu-id="488e9-128">有效值为</span><span class="sxs-lookup"><span data-stu-id="488e9-128">Valid values are</span></span><br /><br /> <span data-ttu-id="488e9-129">-UnicodeFffeTextEncoding： Unicode BigEndian 编码</span><span class="sxs-lookup"><span data-stu-id="488e9-129">-   UnicodeFffeTextEncoding: Unicode BigEndian encoding</span></span><br /><span data-ttu-id="488e9-130">-Utf16TextEncoding： Unicode 编码</span><span class="sxs-lookup"><span data-stu-id="488e9-130">-   Utf16TextEncoding: Unicode encoding</span></span><br /><span data-ttu-id="488e9-131">-Utf8TextEncoding：8位编码</span><span class="sxs-lookup"><span data-stu-id="488e9-131">-   Utf8TextEncoding: 8-bit encoding</span></span><br /><br /> <span data-ttu-id="488e9-132">默认值为 Utf8TextEncoding。</span><span class="sxs-lookup"><span data-stu-id="488e9-132">The default is Utf8TextEncoding.</span></span> <span data-ttu-id="488e9-133">此属性的类型为 <xref:System.Text.Encoding>。</span><span class="sxs-lookup"><span data-stu-id="488e9-133">This attribute is of type <xref:System.Text.Encoding>.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="488e9-134">子元素</span><span class="sxs-lookup"><span data-stu-id="488e9-134">Child Elements</span></span>  
  
|<span data-ttu-id="488e9-135">元素</span><span class="sxs-lookup"><span data-stu-id="488e9-135">Element</span></span>|<span data-ttu-id="488e9-136">说明</span><span class="sxs-lookup"><span data-stu-id="488e9-136">Description</span></span>|  
|-------------|-----------------|  
|[\<readerQuotas>](/previous-versions/dotnet/netframework-4.0/ms731325(v=vs.100))|<span data-ttu-id="488e9-137">定义可由采用此绑定配置的终结点进行处理的 SOAP 消息的复杂性约束。</span><span class="sxs-lookup"><span data-stu-id="488e9-137">Defines the constraints on the complexity of SOAP messages that can be processed by endpoints configured with this binding.</span></span> <span data-ttu-id="488e9-138">此元素的类型为 <xref:System.ServiceModel.Configuration.XmlDictionaryReaderQuotasElement>。</span><span class="sxs-lookup"><span data-stu-id="488e9-138">This element is of type <xref:System.ServiceModel.Configuration.XmlDictionaryReaderQuotasElement>.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="488e9-139">父元素</span><span class="sxs-lookup"><span data-stu-id="488e9-139">Parent Elements</span></span>  
  
|<span data-ttu-id="488e9-140">元素</span><span class="sxs-lookup"><span data-stu-id="488e9-140">Element</span></span>|<span data-ttu-id="488e9-141">说明</span><span class="sxs-lookup"><span data-stu-id="488e9-141">Description</span></span>|  
|-------------|-----------------|  
|[\<binding>](bindings.md)|<span data-ttu-id="488e9-142">定义自定义绑定的所有绑定功能。</span><span class="sxs-lookup"><span data-stu-id="488e9-142">Defines all binding capabilities of the custom binding.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="488e9-143">备注</span><span class="sxs-lookup"><span data-stu-id="488e9-143">Remarks</span></span>  

 <span data-ttu-id="488e9-144">编码是将消息转换为一个字节序列的过程。</span><span class="sxs-lookup"><span data-stu-id="488e9-144">Encoding is the process of transforming a message into a sequence of bytes.</span></span> <span data-ttu-id="488e9-145">解码是反向过程。</span><span class="sxs-lookup"><span data-stu-id="488e9-145">Decoding is the reverse process.</span></span> <span data-ttu-id="488e9-146">Windows Communication Foundation (WCF) 包含三种类型的 SOAP 消息编码：文本、二进制和消息传输优化机制 (MTOM)。</span><span class="sxs-lookup"><span data-stu-id="488e9-146">Windows Communication Foundation (WCF) includes three types of encoding for SOAP messages: Text, Binary and Message Transmission Optimization Mechanism (MTOM).</span></span>  
  
 <span data-ttu-id="488e9-147">由 `textMessageEncoding` 元素表示的文本编码互操作性最强，但却是效率最低的 XML 消息编码器。</span><span class="sxs-lookup"><span data-stu-id="488e9-147">The text encoding represented by the `textMessageEncoding` element is the most interoperable, but the least efficient encoder for XML messages.</span></span>  <span data-ttu-id="488e9-148">文本编码器在网络上创建基于文本的消息。</span><span class="sxs-lookup"><span data-stu-id="488e9-148">The text encoder creates text-based messages on the wire.</span></span> <span data-ttu-id="488e9-149">此编码器产生的消息适合于基于 WS-\* 的互操作性。</span><span class="sxs-lookup"><span data-stu-id="488e9-149">Messages produced by this encoder are suitable for WS-\* based interop.</span></span> <span data-ttu-id="488e9-150">Web 服务或 Web 服务客户端通常可以理解文本 XML。</span><span class="sxs-lookup"><span data-stu-id="488e9-150">Web service or Web service client can generally understand textual XML.</span></span> <span data-ttu-id="488e9-151">但是，对于 XML 消息编码来说，以文本形式传输较大的二进制数据块是最低效的方法。</span><span class="sxs-lookup"><span data-stu-id="488e9-151">However, transmitting large blocks of binary data as text is the least efficient method for encoding XML messages.</span></span>  
  
## <a name="example"></a><span data-ttu-id="488e9-152">示例</span><span class="sxs-lookup"><span data-stu-id="488e9-152">Example</span></span>  
  
```xml  
<textMessageEncoding maxReadPoolSize="211"
                     maxWritePoolSize="2132"
                     messageVersion="Soap12Addressing10"
                     textEncoding="utf-8" />
```  
  
## <a name="see-also"></a><span data-ttu-id="488e9-153">请参阅</span><span class="sxs-lookup"><span data-stu-id="488e9-153">See also</span></span>

- <xref:System.ServiceModel.Configuration.TextMessageEncodingElement>
- <xref:System.ServiceModel.Channels.CustomBinding>
- <xref:System.ServiceModel.Channels.MessageEncodingBindingElement>
- <xref:System.ServiceModel.Channels.TextMessageEncodingBindingElement>
- [<span data-ttu-id="488e9-154">选择消息编码器</span><span class="sxs-lookup"><span data-stu-id="488e9-154">Choosing a Message Encoder</span></span>](../../../wcf/feature-details/choosing-a-message-encoder.md)
- [<span data-ttu-id="488e9-155">消息编码</span><span class="sxs-lookup"><span data-stu-id="488e9-155">Message Encoding</span></span>](message-encoding.md)
- [<span data-ttu-id="488e9-156">绑定</span><span class="sxs-lookup"><span data-stu-id="488e9-156">Bindings</span></span>](../../../wcf/bindings.md)
- [<span data-ttu-id="488e9-157">扩展绑定</span><span class="sxs-lookup"><span data-stu-id="488e9-157">Extending Bindings</span></span>](../../../wcf/extending/extending-bindings.md)
- [<span data-ttu-id="488e9-158">自定义绑定</span><span class="sxs-lookup"><span data-stu-id="488e9-158">Custom Bindings</span></span>](../../../wcf/extending/custom-bindings.md)
- [\<customBinding>](custombinding.md)
