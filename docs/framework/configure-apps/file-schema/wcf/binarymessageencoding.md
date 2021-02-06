---
description: 了解详细信息： <binaryMessageEncoding>
title: <binaryMessageEncoding>
ms.date: 03/30/2017
ms.assetid: e4ae3cd4-6b67-4ce1-af4b-9400e0a38dba
ms.openlocfilehash: 910b8b70bab40c1eb099ed2b54c0545e73e96c6f
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99639492"
---
# \<binaryMessageEncoding>

<span data-ttu-id="6a82e-102">定义一个在网络上以二进制形式对 Windows Communication Foundation (WCF) 消息进行编码的二进制消息编码器。</span><span class="sxs-lookup"><span data-stu-id="6a82e-102">Defines a binary message encoder that encodes Windows Communication Foundation (WCF) messages in binary on the wire.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<bindings>**](bindings.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<customBinding>**](custombinding.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<binding>**\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<binaryMessageEncoding>**  
  
## <a name="syntax"></a><span data-ttu-id="6a82e-103">语法</span><span class="sxs-lookup"><span data-stu-id="6a82e-103">Syntax</span></span>  
  
```xml  
<binaryMessageEncoding maxReadPoolSize="Integer"
                       maxSessionSize="Integer"
                       maxWritePoolSize="Integer"
                       messageVersion="Soap11Addressing10/Soap12Addressing10" />
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="6a82e-104">特性和元素</span><span class="sxs-lookup"><span data-stu-id="6a82e-104">Attributes and Elements</span></span>  

 <span data-ttu-id="6a82e-105">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="6a82e-105">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="6a82e-106">特性</span><span class="sxs-lookup"><span data-stu-id="6a82e-106">Attributes</span></span>  
  
|<span data-ttu-id="6a82e-107">属性</span><span class="sxs-lookup"><span data-stu-id="6a82e-107">Attribute</span></span>|<span data-ttu-id="6a82e-108">说明</span><span class="sxs-lookup"><span data-stu-id="6a82e-108">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="6a82e-109">maxReadPoolSize</span><span class="sxs-lookup"><span data-stu-id="6a82e-109">maxReadPoolSize</span></span>|<span data-ttu-id="6a82e-110">一个整数，指定在无需分配新读取器的情况下可以同时读取的消息数。</span><span class="sxs-lookup"><span data-stu-id="6a82e-110">An integer that defines how many messages can be read simultaneously without allocating new readers.</span></span> <span data-ttu-id="6a82e-111">池越大，系统允许的活动峰值就越大，但工作集也会随之增大。</span><span class="sxs-lookup"><span data-stu-id="6a82e-111">Larger pool sizes make the system more tolerant to activity spikes at the cost of a larger working set.</span></span> <span data-ttu-id="6a82e-112">默认值为 64。</span><span class="sxs-lookup"><span data-stu-id="6a82e-112">The default is 64.</span></span>|  
|<span data-ttu-id="6a82e-113">maxSessionSize</span><span class="sxs-lookup"><span data-stu-id="6a82e-113">maxSessionSize</span></span>|<span data-ttu-id="6a82e-114">一个正整数，设置用于编码的缓冲区的大小（字节）。</span><span class="sxs-lookup"><span data-stu-id="6a82e-114">A positive integer that sets the size, in bytes, of the buffer used for encoding.</span></span> <span data-ttu-id="6a82e-115">较大的缓冲区能够提高编码速度，代价是增加了工作集的大小。</span><span class="sxs-lookup"><span data-stu-id="6a82e-115">A larger buffer increases encoding speed at the expense of the size of the working set.</span></span> <span data-ttu-id="6a82e-116">默认值为 2048。</span><span class="sxs-lookup"><span data-stu-id="6a82e-116">The default is 2048.</span></span>|  
|<span data-ttu-id="6a82e-117">maxWritePoolSize</span><span class="sxs-lookup"><span data-stu-id="6a82e-117">maxWritePoolSize</span></span>|<span data-ttu-id="6a82e-118">一个整数，指定在无需分配新编写器的情况下可以同时发送的消息数。</span><span class="sxs-lookup"><span data-stu-id="6a82e-118">An integer that defines how many messages can be sent simultaneously without allocating new writers.</span></span> <span data-ttu-id="6a82e-119">池越大，系统允许的活动峰值就越大，但工作集也会随之增大。</span><span class="sxs-lookup"><span data-stu-id="6a82e-119">Larger pool sizes make the system more tolerant to activity spikes at the cost of a larger working set.</span></span> <span data-ttu-id="6a82e-120">默认值为 16。</span><span class="sxs-lookup"><span data-stu-id="6a82e-120">The default is 16.</span></span>|  
|<span data-ttu-id="6a82e-121">messageVersion</span><span class="sxs-lookup"><span data-stu-id="6a82e-121">messageVersion</span></span>|<span data-ttu-id="6a82e-122">指定使用的或预期的 SOAP 消息和 WS-Addressing 版本。</span><span class="sxs-lookup"><span data-stu-id="6a82e-122">Specifies the SOAP message and WS-Addressing versions that are used or expected.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="6a82e-123">子元素</span><span class="sxs-lookup"><span data-stu-id="6a82e-123">Child Elements</span></span>  
  
|<span data-ttu-id="6a82e-124">元素</span><span class="sxs-lookup"><span data-stu-id="6a82e-124">Element</span></span>|<span data-ttu-id="6a82e-125">说明</span><span class="sxs-lookup"><span data-stu-id="6a82e-125">Description</span></span>|  
|-------------|-----------------|  
|[\<readerQuotas>](/previous-versions/dotnet/netframework-4.0/ms731325(v=vs.100))|<span data-ttu-id="6a82e-126">定义可由采用此绑定配置的终结点进行处理的 SOAP 消息的复杂性约束。</span><span class="sxs-lookup"><span data-stu-id="6a82e-126">Defines the constraints on the complexity of SOAP messages that can be processed by endpoints configured with this binding.</span></span> <span data-ttu-id="6a82e-127">此元素的类型为 <xref:System.ServiceModel.Configuration.XmlDictionaryReaderQuotasElement>。</span><span class="sxs-lookup"><span data-stu-id="6a82e-127">This element is of type <xref:System.ServiceModel.Configuration.XmlDictionaryReaderQuotasElement>.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="6a82e-128">父元素</span><span class="sxs-lookup"><span data-stu-id="6a82e-128">Parent Elements</span></span>  
  
|<span data-ttu-id="6a82e-129">元素</span><span class="sxs-lookup"><span data-stu-id="6a82e-129">Element</span></span>|<span data-ttu-id="6a82e-130">说明</span><span class="sxs-lookup"><span data-stu-id="6a82e-130">Description</span></span>|  
|-------------|-----------------|  
|[\<binding>](bindings.md)|<span data-ttu-id="6a82e-131">定义自定义绑定的所有绑定功能。</span><span class="sxs-lookup"><span data-stu-id="6a82e-131">Defines all binding capabilities of the custom binding.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="6a82e-132">备注</span><span class="sxs-lookup"><span data-stu-id="6a82e-132">Remarks</span></span>  

 <span data-ttu-id="6a82e-133">编码是将消息转换为一个字节序列的过程。</span><span class="sxs-lookup"><span data-stu-id="6a82e-133">Encoding is the process of transforming a message into a sequence of bytes.</span></span> <span data-ttu-id="6a82e-134">解码是反向过程。</span><span class="sxs-lookup"><span data-stu-id="6a82e-134">Decoding is the reverse process.</span></span> <span data-ttu-id="6a82e-135">Windows Communication Foundation (WCF) 包含三种类型的 SOAP 消息编码：文本、二进制和消息传输优化机制 (MTOM)。</span><span class="sxs-lookup"><span data-stu-id="6a82e-135">Windows Communication Foundation (WCF) includes three types of encoding for SOAP messages: Text, Binary and Message Transmission Optimization Mechanism (MTOM).</span></span>  
  
 <span data-ttu-id="6a82e-136">`binaryMessageEncoding` 元素为 XML 指定 .NET 二进制格式，且包含可用于指定要使用的字符编码以及 SOAP 和 WS-Addressing 版本的选项。</span><span class="sxs-lookup"><span data-stu-id="6a82e-136">The `binaryMessageEncoding` element specifies the .NET Binary Format for XML and has options to specify the character encoding and the SOAP and WS-Addressing version to be used.</span></span> <span data-ttu-id="6a82e-137">二进制消息编码器在网络上以二进制形式对 Windows Communication Foundation (WCF) 消息进行编码。</span><span class="sxs-lookup"><span data-stu-id="6a82e-137">The binary message encoder encodes Windows Communication Foundation (WCF) messages in binary on the wire.</span></span> <span data-ttu-id="6a82e-138">虽然这种编码有助于非常快速地传输消息，但是丢失了基于 WS-\* 标准的互操作性。</span><span class="sxs-lookup"><span data-stu-id="6a82e-138">While this encoding results in very fast transmission of messages, interoperability based on the WS-\* standards is lost.</span></span>  
  
## <a name="example"></a><span data-ttu-id="6a82e-139">示例</span><span class="sxs-lookup"><span data-stu-id="6a82e-139">Example</span></span>  
  
```xml  
<binaryMessageEncoding maxReadPoolSize="211"
                       maxWritePoolSize="2132"
                       maxSessionSize="3141" />
```  
  
## <a name="see-also"></a><span data-ttu-id="6a82e-140">请参阅</span><span class="sxs-lookup"><span data-stu-id="6a82e-140">See also</span></span>

- <xref:System.ServiceModel.Configuration.BinaryMessageEncodingElement>
- <xref:System.ServiceModel.Channels.CustomBinding>
- <xref:System.ServiceModel.Channels.MessageEncodingBindingElement>
- <xref:System.ServiceModel.Channels.BinaryMessageEncodingBindingElement>
- [<span data-ttu-id="6a82e-141">消息编码</span><span class="sxs-lookup"><span data-stu-id="6a82e-141">Message Encoding</span></span>](message-encoding.md)
- [<span data-ttu-id="6a82e-142">选择消息编码器</span><span class="sxs-lookup"><span data-stu-id="6a82e-142">Choosing a Message Encoder</span></span>](../../../wcf/feature-details/choosing-a-message-encoder.md)
- [<span data-ttu-id="6a82e-143">绑定</span><span class="sxs-lookup"><span data-stu-id="6a82e-143">Bindings</span></span>](../../../wcf/bindings.md)
- [<span data-ttu-id="6a82e-144">扩展绑定</span><span class="sxs-lookup"><span data-stu-id="6a82e-144">Extending Bindings</span></span>](../../../wcf/extending/extending-bindings.md)
- [<span data-ttu-id="6a82e-145">自定义绑定</span><span class="sxs-lookup"><span data-stu-id="6a82e-145">Custom Bindings</span></span>](../../../wcf/extending/custom-bindings.md)
- [\<customBinding>](custombinding.md)
