---
description: 了解详细信息： <byteStreamMessageEncoding>
title: <byteStreamMessageEncoding>
ms.date: 03/30/2017
ms.assetid: bbadd8dd-60a2-4007-b959-89373a8a7d60
ms.openlocfilehash: 9cbb4eacb1a960481ee262db662160b5a342e27f
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99639284"
---
# \<byteStreamMessageEncoding>

<span data-ttu-id="d45ca-102">指定消息编码作为字节流，也可以选择指定字符编码。</span><span class="sxs-lookup"><span data-stu-id="d45ca-102">Specifies the message encoding as a stream of bytes, with the option to specify the character encoding.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<bindings>**](bindings.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<customBinding>**](custombinding.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<binding>**\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<byteStreamMessageEncoding>**  
  
## <a name="syntax"></a><span data-ttu-id="d45ca-103">语法</span><span class="sxs-lookup"><span data-stu-id="d45ca-103">Syntax</span></span>  
  
```xml  
<byteStreamMessageEncoding />
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="d45ca-104">特性和元素</span><span class="sxs-lookup"><span data-stu-id="d45ca-104">Attributes and Elements</span></span>  

 <span data-ttu-id="d45ca-105">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="d45ca-105">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="d45ca-106">特性</span><span class="sxs-lookup"><span data-stu-id="d45ca-106">Attributes</span></span>  
  
|<span data-ttu-id="d45ca-107">属性</span><span class="sxs-lookup"><span data-stu-id="d45ca-107">Attribute</span></span>|<span data-ttu-id="d45ca-108">说明</span><span class="sxs-lookup"><span data-stu-id="d45ca-108">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="d45ca-109">messageVersion</span><span class="sxs-lookup"><span data-stu-id="d45ca-109">messageVersion</span></span>|<span data-ttu-id="d45ca-110">指定使用此绑定发送的消息的 SOAP 版本。</span><span class="sxs-lookup"><span data-stu-id="d45ca-110">Specifies the SOAP version of the messages sent using the binding.</span></span> <span data-ttu-id="d45ca-111">此属性只能设置为 <xref:System.ServiceModel.Channels.MessageVersion.None%2A> 的消息版本值。</span><span class="sxs-lookup"><span data-stu-id="d45ca-111">This property can only be set to the message version value of <xref:System.ServiceModel.Channels.MessageVersion.None%2A>.</span></span> <span data-ttu-id="d45ca-112">字节流消息编码器不支持其他任何消息版本。</span><span class="sxs-lookup"><span data-stu-id="d45ca-112">The byte stream message encoder does not support any other message versions.</span></span><br /><br /> <span data-ttu-id="d45ca-113">此属性的类型为 <xref:System.ServiceModel.Channels.MessageVersion>。</span><span class="sxs-lookup"><span data-stu-id="d45ca-113">This attribute is of type <xref:System.ServiceModel.Channels.MessageVersion>.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="d45ca-114">子元素</span><span class="sxs-lookup"><span data-stu-id="d45ca-114">Child Elements</span></span>  
  
|<span data-ttu-id="d45ca-115">元素</span><span class="sxs-lookup"><span data-stu-id="d45ca-115">Element</span></span>|<span data-ttu-id="d45ca-116">说明</span><span class="sxs-lookup"><span data-stu-id="d45ca-116">Description</span></span>|  
|-------------|-----------------|  
|[\<readerQuotas>](/previous-versions/dotnet/netframework-4.0/ms731325(v=vs.100))|<span data-ttu-id="d45ca-117">定义可由采用此绑定配置的终结点进行处理的 SOAP 消息的复杂性约束。</span><span class="sxs-lookup"><span data-stu-id="d45ca-117">Defines the constraints on the complexity of SOAP messages that can be processed by endpoints configured with this binding.</span></span> <span data-ttu-id="d45ca-118">此元素的类型为 <xref:System.ServiceModel.Configuration.XmlDictionaryReaderQuotasElement>。</span><span class="sxs-lookup"><span data-stu-id="d45ca-118">This element is of type <xref:System.ServiceModel.Configuration.XmlDictionaryReaderQuotasElement>.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="d45ca-119">父元素</span><span class="sxs-lookup"><span data-stu-id="d45ca-119">Parent Elements</span></span>  
  
|<span data-ttu-id="d45ca-120">元素</span><span class="sxs-lookup"><span data-stu-id="d45ca-120">Element</span></span>|<span data-ttu-id="d45ca-121">说明</span><span class="sxs-lookup"><span data-stu-id="d45ca-121">Description</span></span>|  
|-------------|-----------------|  
|[\<binding>](bindings.md)|<span data-ttu-id="d45ca-122">定义自定义绑定的所有绑定功能。</span><span class="sxs-lookup"><span data-stu-id="d45ca-122">Defines all binding capabilities of the custom binding.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="d45ca-123">请参阅</span><span class="sxs-lookup"><span data-stu-id="d45ca-123">See also</span></span>

- <xref:System.ServiceModel.Configuration.ByteStreamMessageEncodingElement>
- <xref:System.ServiceModel.Channels.CustomBinding>
- <xref:System.ServiceModel.Channels.MessageEncodingBindingElement>
- <xref:System.ServiceModel.Channels.ByteStreamMessageEncodingBindingElement>
- [<span data-ttu-id="d45ca-124">消息编码</span><span class="sxs-lookup"><span data-stu-id="d45ca-124">Message Encoding</span></span>](message-encoding.md)
- [<span data-ttu-id="d45ca-125">选择消息编码器</span><span class="sxs-lookup"><span data-stu-id="d45ca-125">Choosing a Message Encoder</span></span>](../../../wcf/feature-details/choosing-a-message-encoder.md)
- [<span data-ttu-id="d45ca-126">绑定</span><span class="sxs-lookup"><span data-stu-id="d45ca-126">Bindings</span></span>](../../../wcf/bindings.md)
- [<span data-ttu-id="d45ca-127">扩展绑定</span><span class="sxs-lookup"><span data-stu-id="d45ca-127">Extending Bindings</span></span>](../../../wcf/extending/extending-bindings.md)
- [<span data-ttu-id="d45ca-128">自定义绑定</span><span class="sxs-lookup"><span data-stu-id="d45ca-128">Custom Bindings</span></span>](../../../wcf/extending/custom-bindings.md)
- [\<customBinding>](custombinding.md)
