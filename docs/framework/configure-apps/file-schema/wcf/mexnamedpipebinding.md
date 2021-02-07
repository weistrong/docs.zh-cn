---
description: 了解详细信息： <mexNamedPipeBinding>
title: <mexNamedPipeBinding>
ms.date: 03/30/2017
ms.assetid: 193412fa-3260-414c-92c6-b32ed3b94a34
ms.openlocfilehash: a7d1c6b10ed436d5ec1b20092d042d6b0a80bd34
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99684316"
---
# \<mexNamedPipeBinding>

<span data-ttu-id="1542b-102">指定用于通过命名管道进行的 WS-MetadataExchange (WS-MEX) 消息交换的绑定的设置。</span><span class="sxs-lookup"><span data-stu-id="1542b-102">Specifies the settings for a binding used for the WS-MetadataExchange (WS-MEX) message exchange over named pipe.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<bindings>**](bindings.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<mexNamedPipeBinding>**  
  
## <a name="syntax"></a><span data-ttu-id="1542b-103">语法</span><span class="sxs-lookup"><span data-stu-id="1542b-103">Syntax</span></span>  
  
```xml  
<mexNamedPipeBinding>
  <binding closeTimeout="TimeSpan"
           name="string"
           openTimeout="TimeSpan"
           receiveTimeout="TimeSpan"
           sendTimeout="TimeSpan">
  </binding>
</mexNamedPipeBinding>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="1542b-104">特性和元素</span><span class="sxs-lookup"><span data-stu-id="1542b-104">Attributes and Elements</span></span>  

 <span data-ttu-id="1542b-105">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="1542b-105">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="1542b-106">特性</span><span class="sxs-lookup"><span data-stu-id="1542b-106">Attributes</span></span>  
  
|<span data-ttu-id="1542b-107">属性</span><span class="sxs-lookup"><span data-stu-id="1542b-107">Attribute</span></span>|<span data-ttu-id="1542b-108">说明</span><span class="sxs-lookup"><span data-stu-id="1542b-108">Description</span></span>|  
|---------------|-----------------|  
|`closeTimeout`|<span data-ttu-id="1542b-109">一个 <xref:System.TimeSpan> 值，指定为完成关闭操作提供的时间间隔。</span><span class="sxs-lookup"><span data-stu-id="1542b-109">A <xref:System.TimeSpan> value that specifies the interval of time provided for a close operation to complete.</span></span> <span data-ttu-id="1542b-110">此值应大于或等于 <xref:System.TimeSpan.Zero>。</span><span class="sxs-lookup"><span data-stu-id="1542b-110">This value should be greater than or equal to <xref:System.TimeSpan.Zero>.</span></span> <span data-ttu-id="1542b-111">默认值为 00:01:00。</span><span class="sxs-lookup"><span data-stu-id="1542b-111">The default is 00:01:00.</span></span>|  
|`name`|<span data-ttu-id="1542b-112">一个包含绑定的配置名称的字符串。</span><span class="sxs-lookup"><span data-stu-id="1542b-112">A string that contains the configuration name of the binding.</span></span> <span data-ttu-id="1542b-113">因为此值用作绑定的标识，所以它应该是唯一的。</span><span class="sxs-lookup"><span data-stu-id="1542b-113">This value should be unique because it is used as an identification for the binding.</span></span> <span data-ttu-id="1542b-114">从 .NET Framework 4 开始，绑定和行为不需要具有名称。</span><span class="sxs-lookup"><span data-stu-id="1542b-114">Starting with .NET Framework 4, bindings and behaviors are not required to have a name.</span></span> <span data-ttu-id="1542b-115">有关默认配置和无值绑定和行为的详细信息，请参阅[WCF 服务的](../../../wcf/samples/simplified-configuration-for-wcf-services.md)[简化配置](../../../wcf/simplified-configuration.md)和简化配置。</span><span class="sxs-lookup"><span data-stu-id="1542b-115">For more information about default configuration and nameless bindings and behaviors, see [Simplified Configuration](../../../wcf/simplified-configuration.md) and [Simplified Configuration for WCF Services](../../../wcf/samples/simplified-configuration-for-wcf-services.md).</span></span>|  
|`openTimeout`|<span data-ttu-id="1542b-116">一个 <xref:System.TimeSpan> 值，指定为完成打开操作提供的时间间隔。</span><span class="sxs-lookup"><span data-stu-id="1542b-116">A <xref:System.TimeSpan> value that specifies the interval of time provided for an open operation to complete.</span></span> <span data-ttu-id="1542b-117">此值应大于或等于 <xref:System.TimeSpan.Zero>。</span><span class="sxs-lookup"><span data-stu-id="1542b-117">This value should be greater than or equal to <xref:System.TimeSpan.Zero>.</span></span> <span data-ttu-id="1542b-118">默认值为 00:01:00。</span><span class="sxs-lookup"><span data-stu-id="1542b-118">The default is 00:01:00.</span></span>|  
|`receiveTimeout`|<span data-ttu-id="1542b-119">一个 <xref:System.TimeSpan> 值，指定为完成接收操作提供的时间间隔。</span><span class="sxs-lookup"><span data-stu-id="1542b-119">A <xref:System.TimeSpan> value that specifies the interval of time provided for a receive operation to complete.</span></span> <span data-ttu-id="1542b-120">此值应大于或等于 <xref:System.TimeSpan.Zero>。</span><span class="sxs-lookup"><span data-stu-id="1542b-120">This value should be greater than or equal to <xref:System.TimeSpan.Zero>.</span></span> <span data-ttu-id="1542b-121">默认值为 00:10:00。</span><span class="sxs-lookup"><span data-stu-id="1542b-121">The default is 00:10:00.</span></span>|  
|`sendTimeout`|<span data-ttu-id="1542b-122">一个 <xref:System.TimeSpan> 值，指定为完成发送操作提供的时间间隔。</span><span class="sxs-lookup"><span data-stu-id="1542b-122">A <xref:System.TimeSpan> value that specifies the interval of time provided for a send operation to complete.</span></span> <span data-ttu-id="1542b-123">此值应大于或等于 <xref:System.TimeSpan.Zero>。</span><span class="sxs-lookup"><span data-stu-id="1542b-123">This value should be greater than or equal to <xref:System.TimeSpan.Zero>.</span></span> <span data-ttu-id="1542b-124">默认值为 00:01:00。</span><span class="sxs-lookup"><span data-stu-id="1542b-124">The default is 00:01:00.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="1542b-125">子元素</span><span class="sxs-lookup"><span data-stu-id="1542b-125">Child Elements</span></span>  

 <span data-ttu-id="1542b-126">无。</span><span class="sxs-lookup"><span data-stu-id="1542b-126">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="1542b-127">父元素</span><span class="sxs-lookup"><span data-stu-id="1542b-127">Parent Elements</span></span>  
  
|<span data-ttu-id="1542b-128">元素</span><span class="sxs-lookup"><span data-stu-id="1542b-128">Element</span></span>|<span data-ttu-id="1542b-129">说明</span><span class="sxs-lookup"><span data-stu-id="1542b-129">Description</span></span>|  
|-------------|-----------------|  
|[\<bindings>](bindings.md)|<span data-ttu-id="1542b-130">此元素包含标准绑定和自定义绑定的集合。</span><span class="sxs-lookup"><span data-stu-id="1542b-130">This element holds a collection of standard and custom bindings.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="1542b-131">请参阅</span><span class="sxs-lookup"><span data-stu-id="1542b-131">See also</span></span>

- <xref:System.ServiceModel.Description.MetadataExchangeBindings.CreateMexNamedPipeBinding%2A>
- <xref:System.ServiceModel.Configuration.MexNamedPipeBindingElement>
- [<span data-ttu-id="1542b-132">如何：使用配置文件发布服务的元数据</span><span class="sxs-lookup"><span data-stu-id="1542b-132">How to: Publish Metadata for a Service Using a Configuration File</span></span>](../../../wcf/feature-details/how-to-publish-metadata-for-a-service-using-a-configuration-file.md)
- [<span data-ttu-id="1542b-133">通过自定义绑定发布和检索元数据</span><span class="sxs-lookup"><span data-stu-id="1542b-133">Publishing and Retrieving Metadata Over a Custom Binding</span></span>](../../../wcf/extending/publishing-and-retrieving-metadata-over-a-custom-binding.md)
- <span data-ttu-id="1542b-134">Metadata </span><span class="sxs-lookup"><span data-stu-id="1542b-134">[Metadata](../../../wcf/feature-details/metadata.md)</span></span>
- [<span data-ttu-id="1542b-135">绑定</span><span class="sxs-lookup"><span data-stu-id="1542b-135">Bindings</span></span>](../../../wcf/bindings.md)
- [<span data-ttu-id="1542b-136">配置系统提供的绑定</span><span class="sxs-lookup"><span data-stu-id="1542b-136">Configuring System-Provided Bindings</span></span>](../../../wcf/feature-details/configuring-system-provided-bindings.md)
- [<span data-ttu-id="1542b-137">使用绑定配置服务和客户端</span><span class="sxs-lookup"><span data-stu-id="1542b-137">Using Bindings to Configure Services and Clients</span></span>](../../../wcf/using-bindings-to-configure-services-and-clients.md)
- [\<binding>](bindings.md)
