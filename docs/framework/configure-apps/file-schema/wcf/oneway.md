---
description: 了解详细信息： <oneWay>
title: <oneWay>
ms.date: 03/30/2017
ms.assetid: 00e67e0e-77c0-4695-9138-c0997b0e5f3c
ms.openlocfilehash: 8e3314dd14525b5f7585a7336c00b615da56d1c7
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99683835"
---
# \<oneWay>

<span data-ttu-id="d1b92-102">对自定义绑定启用数据包路由并使用单向方法。</span><span class="sxs-lookup"><span data-stu-id="d1b92-102">Enables packet routing and the use of one-way methods for a custom binding.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<bindings>**](bindings.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<customBinding>**](custombinding.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<binding>**\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<oneWay>**  
  
## <a name="syntax"></a><span data-ttu-id="d1b92-103">语法</span><span class="sxs-lookup"><span data-stu-id="d1b92-103">Syntax</span></span>  
  
```xml  
<oneWay packetRoutable="Boolean">
  <channelPoolSettings idleTimeout="TimeSpan"
                       leaseTimeout="TimeSpan"
                       maxOutboundConnectionsPerEndpoint="Integer" />
</oneWay>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="d1b92-104">特性和元素</span><span class="sxs-lookup"><span data-stu-id="d1b92-104">Attributes and Elements</span></span>  

 <span data-ttu-id="d1b92-105">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="d1b92-105">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="d1b92-106">特性</span><span class="sxs-lookup"><span data-stu-id="d1b92-106">Attributes</span></span>  
  
|<span data-ttu-id="d1b92-107">属性</span><span class="sxs-lookup"><span data-stu-id="d1b92-107">Attribute</span></span>|<span data-ttu-id="d1b92-108">说明</span><span class="sxs-lookup"><span data-stu-id="d1b92-108">Description</span></span>|  
|---------------|-----------------|  
|`packetRoutable`|<span data-ttu-id="d1b92-109">一个布尔值，指定是否启用数据包路由。</span><span class="sxs-lookup"><span data-stu-id="d1b92-109">A Boolean value that specifies whether packet routing is enabled.</span></span> <span data-ttu-id="d1b92-110">默认值为 `false`。</span><span class="sxs-lookup"><span data-stu-id="d1b92-110">The default is `false`.</span></span>|  
|`MaxAcceptedChannels`|<span data-ttu-id="d1b92-111">一个整数，指定可接受的最大通道数。</span><span class="sxs-lookup"><span data-stu-id="d1b92-111">An integer that specifies the maximum number of channels that can be accepted.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="d1b92-112">子元素</span><span class="sxs-lookup"><span data-stu-id="d1b92-112">Child Elements</span></span>  
  
|<span data-ttu-id="d1b92-113">元素</span><span class="sxs-lookup"><span data-stu-id="d1b92-113">Element</span></span>|<span data-ttu-id="d1b92-114">说明</span><span class="sxs-lookup"><span data-stu-id="d1b92-114">Description</span></span>|  
|-------------|-----------------|  
|[\<channelPoolSettings>](channelpoolsettings.md)|<span data-ttu-id="d1b92-115">一个 <xref:System.ServiceModel.Configuration.ChannelPoolSettingsElement> 对象，包含当前通道的通道池的属性。</span><span class="sxs-lookup"><span data-stu-id="d1b92-115">A <xref:System.ServiceModel.Configuration.ChannelPoolSettingsElement> object that contains properties of the channel pool for the current channel.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="d1b92-116">父元素</span><span class="sxs-lookup"><span data-stu-id="d1b92-116">Parent Elements</span></span>  
  
|<span data-ttu-id="d1b92-117">元素</span><span class="sxs-lookup"><span data-stu-id="d1b92-117">Element</span></span>|<span data-ttu-id="d1b92-118">说明</span><span class="sxs-lookup"><span data-stu-id="d1b92-118">Description</span></span>|  
|-------------|-----------------|  
|[\<binding>](bindings.md)|<span data-ttu-id="d1b92-119">定义自定义绑定的所有绑定功能。</span><span class="sxs-lookup"><span data-stu-id="d1b92-119">Defines all binding capabilities of the custom binding.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="d1b92-120">备注</span><span class="sxs-lookup"><span data-stu-id="d1b92-120">Remarks</span></span>  

 <span data-ttu-id="d1b92-121">若要启用数据包路由，必须使用此元素提供的单向转换层。</span><span class="sxs-lookup"><span data-stu-id="d1b92-121">To enable packet routing, a one-way conversion layer is required, which this element provides.</span></span> <span data-ttu-id="d1b92-122">用户可以创建一个自定义绑定，将此绑定置于具有会话功能或请求/答复传输的上层，使之可进行数据包路由。</span><span class="sxs-lookup"><span data-stu-id="d1b92-122">A user can create a custom binding that layers this binding over a session-aware or request-reply transport to make it packet routable.</span></span> <span data-ttu-id="d1b92-123">如果希望以更自然的方式公开单向方法，则此元素也十分有用。</span><span class="sxs-lookup"><span data-stu-id="d1b92-123">This element is also useful when you want to expose one-way methods in a more native fashion.</span></span> <span data-ttu-id="d1b92-124">在这一层上可应用更多的转换，如复合双工和可靠消息。</span><span class="sxs-lookup"><span data-stu-id="d1b92-124">More transformations can be applied over this layer, such as Composite Duplex and Reliable Messaging.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d1b92-125">请参阅</span><span class="sxs-lookup"><span data-stu-id="d1b92-125">See also</span></span>

- <xref:System.ServiceModel.Channels.OneWayBindingElement>
- <xref:System.ServiceModel.Configuration.OneWayElement>
- <xref:System.ServiceModel.Channels.CustomBinding>
- [<span data-ttu-id="d1b92-126">绑定</span><span class="sxs-lookup"><span data-stu-id="d1b92-126">Bindings</span></span>](../../../wcf/bindings.md)
- [<span data-ttu-id="d1b92-127">扩展绑定</span><span class="sxs-lookup"><span data-stu-id="d1b92-127">Extending Bindings</span></span>](../../../wcf/extending/extending-bindings.md)
- [<span data-ttu-id="d1b92-128">自定义绑定</span><span class="sxs-lookup"><span data-stu-id="d1b92-128">Custom Bindings</span></span>](../../../wcf/extending/custom-bindings.md)
- [\<customBinding>](custombinding.md)
