---
description: 了解详细 <behavior> 信息： <endpointBehaviors>
title: <behavior> 的 <endpointBehaviors>
ms.date: 03/30/2017
ms.assetid: b90ca3bc-3c22-4174-b903-e3a39898bd27
ms.openlocfilehash: a72bb69cce96d72cdc00d48546244bdcde20271f
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99802328"
---
# <a name="behavior-of-endpointbehaviors"></a><span data-ttu-id="98839-103">\<behavior> 的 \<endpointBehaviors></span><span class="sxs-lookup"><span data-stu-id="98839-103">\<behavior> of \<endpointBehaviors></span></span>

<span data-ttu-id="98839-104">`behavior` 元素包含终结点行为的设置集合。</span><span class="sxs-lookup"><span data-stu-id="98839-104">The `behavior` element contains a collection of settings for the behavior of an endpoint.</span></span> <span data-ttu-id="98839-105">每个行为都按其 `name` 进行索引。</span><span class="sxs-lookup"><span data-stu-id="98839-105">Each behavior is indexed by its `name`.</span></span> <span data-ttu-id="98839-106">终结点可以通过此名称链接到每个行为。</span><span class="sxs-lookup"><span data-stu-id="98839-106">Endpoints can link to each behavior through this name.</span></span> <span data-ttu-id="98839-107">从 .NET Framework 4 开始，绑定和行为不需要具有名称。</span><span class="sxs-lookup"><span data-stu-id="98839-107">Starting with .NET Framework 4, bindings and behaviors are not required to have a name.</span></span> <span data-ttu-id="98839-108">有关默认配置和无值绑定和行为的详细信息，请参阅[WCF 服务的](../../../wcf/samples/simplified-configuration-for-wcf-services.md)[简化配置](../../../wcf/simplified-configuration.md)和简化配置。</span><span class="sxs-lookup"><span data-stu-id="98839-108">For more information about default configuration and nameless bindings and behaviors, see [Simplified Configuration](../../../wcf/simplified-configuration.md) and [Simplified Configuration for WCF Services](../../../wcf/samples/simplified-configuration-for-wcf-services.md).</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<behaviors>**](behaviors.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<endpointBehaviors>**](endpointbehaviors.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<behavior>**  
  
## <a name="syntax"></a><span data-ttu-id="98839-109">语法</span><span class="sxs-lookup"><span data-stu-id="98839-109">Syntax</span></span>  
  
```xml  
<system.ServiceModel>
  <behaviors>
    <endpointBehaviors>
      <behavior name="String" />
    </endpointBehaviors>
  </behaviors>
</system.ServiceModel>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="98839-110">特性和元素</span><span class="sxs-lookup"><span data-stu-id="98839-110">Attributes and Elements</span></span>  

 <span data-ttu-id="98839-111">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="98839-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="98839-112">特性</span><span class="sxs-lookup"><span data-stu-id="98839-112">Attributes</span></span>  
  
|<span data-ttu-id="98839-113">属性</span><span class="sxs-lookup"><span data-stu-id="98839-113">Attribute</span></span>|<span data-ttu-id="98839-114">说明</span><span class="sxs-lookup"><span data-stu-id="98839-114">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="98839-115">name</span><span class="sxs-lookup"><span data-stu-id="98839-115">name</span></span>|<span data-ttu-id="98839-116">一个包含行为的配置名称的唯一字符串。</span><span class="sxs-lookup"><span data-stu-id="98839-116">A unique string that contains the configuration name of the behavior.</span></span> <span data-ttu-id="98839-117">此值是用户定义的一个字符串，该字符串必须是唯一的，因为它将充当元素的标识字符串。</span><span class="sxs-lookup"><span data-stu-id="98839-117">This value is a user-defined string that must be unique, since it acts as the identification string for the element.</span></span> <span data-ttu-id="98839-118">从 .NET Framework 4 开始，绑定和行为不需要具有名称。</span><span class="sxs-lookup"><span data-stu-id="98839-118">Starting with .NET Framework 4, bindings and behaviors are not required to have a name.</span></span> <span data-ttu-id="98839-119">有关默认配置和无值绑定和行为的详细信息，请参阅[WCF 服务的](../../../wcf/samples/simplified-configuration-for-wcf-services.md)[简化配置](../../../wcf/simplified-configuration.md)和简化配置。</span><span class="sxs-lookup"><span data-stu-id="98839-119">For more information about default configuration and nameless bindings and behaviors, see [Simplified Configuration](../../../wcf/simplified-configuration.md) and [Simplified Configuration for WCF Services](../../../wcf/samples/simplified-configuration-for-wcf-services.md).</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="98839-120">子元素</span><span class="sxs-lookup"><span data-stu-id="98839-120">Child Elements</span></span>  
  
|<span data-ttu-id="98839-121">元素</span><span class="sxs-lookup"><span data-stu-id="98839-121">Element</span></span>|<span data-ttu-id="98839-122">说明</span><span class="sxs-lookup"><span data-stu-id="98839-122">Description</span></span>|  
|-------------|-----------------|  
|[\<clientCredentials>](clientcredentials.md)|<span data-ttu-id="98839-123">指定用于向服务验证客户端身份的凭据。</span><span class="sxs-lookup"><span data-stu-id="98839-123">Specifies the credentials used to authenticate the client to a service.</span></span>|  
|[\<callbackDebug>](callbackdebug.md)|<span data-ttu-id="98839-124">指定 Windows Communication Foundation (WCF) 回调对象的服务调试。</span><span class="sxs-lookup"><span data-stu-id="98839-124">Specifies service debugging for a Windows Communication Foundation (WCF) callback object.</span></span>|  
|[\<callbackTimeouts>](callbacktimeouts.md)|<span data-ttu-id="98839-125">指定客户端回调的超时。</span><span class="sxs-lookup"><span data-stu-id="98839-125">Specifies the timeout for the client callback.</span></span>|  
|[\<clientVia>](clientvia.md)|<span data-ttu-id="98839-126">指定消息应采用的路由。</span><span class="sxs-lookup"><span data-stu-id="98839-126">Specifies the route a message should take.</span></span>|  
|[\<dataContractSerializer>](datacontractserializer.md)|<span data-ttu-id="98839-127">包含 DataContractSerializer 的配置数据。</span><span class="sxs-lookup"><span data-stu-id="98839-127">Contains configuration data for the DataContractSerializer.</span></span>|  
|[\<dispatcherSynchronization>](dispatchersynchronization.md)|<span data-ttu-id="98839-128">指定允许服务进行异步答复的终结点行为。</span><span class="sxs-lookup"><span data-stu-id="98839-128">Specifies an endpoint behavior that enables a service to send replies asynchronously.</span></span>|  
|[\<enableWebScript>](enablewebscript.md)|<span data-ttu-id="98839-129">启用终结点行为，此行为使得可以使用 ASP.NET AJAX 网页中的服务。</span><span class="sxs-lookup"><span data-stu-id="98839-129">Enables the endpoint behavior that makes it possible to consume the service from ASP.NET AJAX web pages.</span></span> <span data-ttu-id="98839-130">该行为只应与 \<webHttpBinding> 标准绑定或 \<webMessageEncoding> 绑定元素一起使用。</span><span class="sxs-lookup"><span data-stu-id="98839-130">The behavior should only be used in conjunction with either the \<webHttpBinding> standard binding, or the \<webMessageEncoding> binding element.</span></span>|  
|[\<endpointDiscovery>](endpointdiscovery.md)|<span data-ttu-id="98839-131">指定终结点的各种发现设置，例如终结点的可发现性、范围以及对终结点元数据的任何自定义扩展。</span><span class="sxs-lookup"><span data-stu-id="98839-131">Specifies the various discovery settings for an endpoint, such as its discoverability, scopes, and any custom extensions to its metadata.</span></span>|  
|[\<soapProcessing>](soapprocessing.md)|<span data-ttu-id="98839-132">定义用于封送不同绑定类型和消息版本之间消息的客户端终结点行为。</span><span class="sxs-lookup"><span data-stu-id="98839-132">Defines the client endpoint behavior used to marshal messages between different binding types and message versions.</span></span>|  
|[\<synchronousReceive>](synchronousreceive-element.md)|<span data-ttu-id="98839-133">指定服务或客户端应用程序中用于接收消息的运行时行为。</span><span class="sxs-lookup"><span data-stu-id="98839-133">Specifies run-time behavior for receiving messages in either a service or client application.</span></span> <span data-ttu-id="98839-134">它不具有任何属性或子元素。</span><span class="sxs-lookup"><span data-stu-id="98839-134">It does not have any attributes or child elements.</span></span>|  
|[\<transactedBatching>](transactedbatching.md)|<span data-ttu-id="98839-135">指定接收操作是否支持事务批处理。</span><span class="sxs-lookup"><span data-stu-id="98839-135">Specifies whether transaction batching is supported for receive operations.</span></span>|  
|[\<webHttp>](webhttp.md)|<span data-ttu-id="98839-136">通过配置指定终结点上的 WebHttpBehavior。</span><span class="sxs-lookup"><span data-stu-id="98839-136">Specifies the WebHttpBehavior on an endpoint through configuration.</span></span> <span data-ttu-id="98839-137">此行为与标准绑定结合使用时 \<webHttpBinding> ，将为 WCF 服务启用 Web 编程模型。</span><span class="sxs-lookup"><span data-stu-id="98839-137">This behavior, when used in conjunction with the \<webHttpBinding> standard binding, enables the Web programming model for a WCF service.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="98839-138">父元素</span><span class="sxs-lookup"><span data-stu-id="98839-138">Parent Elements</span></span>  
  
|<span data-ttu-id="98839-139">元素</span><span class="sxs-lookup"><span data-stu-id="98839-139">Element</span></span>|<span data-ttu-id="98839-140">说明</span><span class="sxs-lookup"><span data-stu-id="98839-140">Description</span></span>|  
|-------------|-----------------|  
|[\<endpointBehaviors>](endpointbehaviors.md)|<span data-ttu-id="98839-141">终结点行为元素的集合。</span><span class="sxs-lookup"><span data-stu-id="98839-141">A collection of endpoint behavior elements.</span></span>|
