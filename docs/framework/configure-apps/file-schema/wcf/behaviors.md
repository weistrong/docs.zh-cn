---
description: 了解详细信息： <behaviors>
title: <behaviors>
ms.date: 03/30/2017
ms.assetid: 0e5da4e6-1aa5-466c-924e-f10efee57f0b
ms.openlocfilehash: 3cb8edea76f6e7af3c3b387e5b04b89e58a28305
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99639505"
---
# \<behaviors>

<span data-ttu-id="bdf70-102">此元素定义名为 `endpointBehaviors` 和 `serviceBehaviors` 的两个子集合。</span><span class="sxs-lookup"><span data-stu-id="bdf70-102">This element defines two child collections named `endpointBehaviors` and `serviceBehaviors`.</span></span>  <span data-ttu-id="bdf70-103">每个集合分别定义终结点和服务所使用的行为元素。</span><span class="sxs-lookup"><span data-stu-id="bdf70-103">Each collection defines behavior elements consumed by endpoints and services respectively.</span></span> <span data-ttu-id="bdf70-104">每个行为元素由其唯一的 `name` 属性标识。</span><span class="sxs-lookup"><span data-stu-id="bdf70-104">Each behavior element is identified by its unique `name` attribute.</span></span> <span data-ttu-id="bdf70-105">从 .NET Framework 4 开始，绑定和行为不需要具有名称。</span><span class="sxs-lookup"><span data-stu-id="bdf70-105">Starting with .NET Framework 4, bindings and behaviors are not required to have a name.</span></span> <span data-ttu-id="bdf70-106">有关默认配置和无值绑定和行为的详细信息，请参阅[WCF 服务的](../../../wcf/samples/simplified-configuration-for-wcf-services.md)[简化配置](../../../wcf/simplified-configuration.md)和简化配置。</span><span class="sxs-lookup"><span data-stu-id="bdf70-106">For more information about default configuration and nameless bindings and behaviors, see [Simplified Configuration](../../../wcf/simplified-configuration.md) and [Simplified Configuration for WCF Services](../../../wcf/samples/simplified-configuration-for-wcf-services.md).</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;**\<behaviors>**  
  
## <a name="syntax"></a><span data-ttu-id="bdf70-107">语法</span><span class="sxs-lookup"><span data-stu-id="bdf70-107">Syntax</span></span>  
  
```xml  
<behaviors>
  <serviceBehaviors>
  </serviceBehaviors>
  <endpointBehaviors>
  </endpointBehaviors>
</behaviors>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="bdf70-108">特性和元素</span><span class="sxs-lookup"><span data-stu-id="bdf70-108">Attributes and Elements</span></span>  

 <span data-ttu-id="bdf70-109">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="bdf70-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="bdf70-110">特性</span><span class="sxs-lookup"><span data-stu-id="bdf70-110">Attributes</span></span>  

 <span data-ttu-id="bdf70-111">无</span><span class="sxs-lookup"><span data-stu-id="bdf70-111">None</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="bdf70-112">子元素</span><span class="sxs-lookup"><span data-stu-id="bdf70-112">Child Elements</span></span>  
  
|<span data-ttu-id="bdf70-113">元素</span><span class="sxs-lookup"><span data-stu-id="bdf70-113">Element</span></span>|<span data-ttu-id="bdf70-114">说明</span><span class="sxs-lookup"><span data-stu-id="bdf70-114">Description</span></span>|  
|-------------|-----------------|  
|[\<endpointBehaviors>](endpointbehaviors.md)|<span data-ttu-id="bdf70-115">此配置节描述为特定终结点定义的所有行为。</span><span class="sxs-lookup"><span data-stu-id="bdf70-115">This configuration section represents all the behaviors defined for a specific endpoint.</span></span>|  
|[\<serviceBehaviors>](servicebehaviors.md)|<span data-ttu-id="bdf70-116">此配置节描述为特定服务定义的所有行为。</span><span class="sxs-lookup"><span data-stu-id="bdf70-116">This configuration section represents all the behaviors defined for a specific service.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="bdf70-117">父元素</span><span class="sxs-lookup"><span data-stu-id="bdf70-117">Parent Elements</span></span>  
  
|<span data-ttu-id="bdf70-118">元素</span><span class="sxs-lookup"><span data-stu-id="bdf70-118">Element</span></span>|<span data-ttu-id="bdf70-119">说明</span><span class="sxs-lookup"><span data-stu-id="bdf70-119">Description</span></span>|  
|-------------|-----------------|  
|[\<system.serviceModel>](system-servicemodel.md)|<span data-ttu-id="bdf70-120">所有 Windows Communication Foundation (WCF) 配置元素的根元素。</span><span class="sxs-lookup"><span data-stu-id="bdf70-120">The root element of all Windows Communication Foundation (WCF) configuration elements.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="bdf70-121">备注</span><span class="sxs-lookup"><span data-stu-id="bdf70-121">Remarks</span></span>  

 <span data-ttu-id="bdf70-122">使用 `<remove>` 元素可以从集合中移除特定行为。</span><span class="sxs-lookup"><span data-stu-id="bdf70-122">You can use the `<remove>` element to remove a particular behavior from the collection.</span></span> <span data-ttu-id="bdf70-123">为此，您只需在 `name` 元素的 `<remove>` 特性中提供要移除的行为的名称。</span><span class="sxs-lookup"><span data-stu-id="bdf70-123">To do so, simply supply the name of the behavior to remove in the `name` attribute of the `<remove>` element.</span></span>  <span data-ttu-id="bdf70-124">还可以使用 `<clear>` 元素清除集合中的所有内容，来确保行为集合最初为空。</span><span class="sxs-lookup"><span data-stu-id="bdf70-124">You can also use the `<clear>` element to insure that a behavior collection starts empty by clearing out all the content of the collection.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="bdf70-125">请参阅</span><span class="sxs-lookup"><span data-stu-id="bdf70-125">See also</span></span>

- <xref:System.ServiceModel.Configuration.BehaviorsSection>
- <xref:System.ServiceModel.Configuration.EndpointBehaviorElementCollection>
- <xref:System.ServiceModel.Configuration.EndpointBehaviorElement>
- <xref:System.ServiceModel.Configuration.ServiceBehaviorElementCollection>
- <xref:System.ServiceModel.Configuration.ServiceBehaviorElement>
- [<span data-ttu-id="bdf70-126">使用行为配置和扩展运行时</span><span class="sxs-lookup"><span data-stu-id="bdf70-126">Configuring and Extending the Runtime with Behaviors</span></span>](../../../wcf/extending/configuring-and-extending-the-runtime-with-behaviors.md)
- [<span data-ttu-id="bdf70-127">配置客户端行为</span><span class="sxs-lookup"><span data-stu-id="bdf70-127">Configuring Client Behaviors</span></span>](../../../wcf/configuring-client-behaviors.md)
- [<span data-ttu-id="bdf70-128">指定客户端运行时行为</span><span class="sxs-lookup"><span data-stu-id="bdf70-128">Specifying Client Run-Time Behavior</span></span>](../../../wcf/specifying-client-run-time-behavior.md)
- [<span data-ttu-id="bdf70-129">指定服务运行时行为</span><span class="sxs-lookup"><span data-stu-id="bdf70-129">Specifying Service Run-Time Behavior</span></span>](../../../wcf/specifying-service-run-time-behavior.md)
- [<span data-ttu-id="bdf70-130">安全行为</span><span class="sxs-lookup"><span data-stu-id="bdf70-130">Security Behaviors</span></span>](../../../wcf/feature-details/security-behaviors-in-wcf.md)
