---
description: 了解详细 <behavior> 信息： <serviceBehaviors>
title: <behavior> 的 <serviceBehaviors>
ms.date: 03/30/2017
ms.assetid: 78fc0a08-55de-416a-ac12-a5e6ffc9a987
ms.openlocfilehash: e34254661026ad6dcb3429ad1b381cc3e6718f27
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99639531"
---
# <a name="behavior-of-servicebehaviors"></a><span data-ttu-id="27fe4-103">\<behavior> 的 \<serviceBehaviors></span><span class="sxs-lookup"><span data-stu-id="27fe4-103">\<behavior> of \<serviceBehaviors></span></span>

<span data-ttu-id="27fe4-104">`behavior` 元素包含服务行为的设置集合。</span><span class="sxs-lookup"><span data-stu-id="27fe4-104">The `behavior` element contains a collection of settings for the behavior of a service.</span></span> <span data-ttu-id="27fe4-105">每个行为都按其 `name` 进行索引。</span><span class="sxs-lookup"><span data-stu-id="27fe4-105">Each behavior is indexed by its `name`.</span></span> <span data-ttu-id="27fe4-106">服务可以使用元素的特性通过此名称链接到每个行为 `behaviorConfiguration` [\<endpoint>](endpoint-element.md) 。</span><span class="sxs-lookup"><span data-stu-id="27fe4-106">Services can link to each behavior through this name using the `behaviorConfiguration` attribute of the [\<endpoint>](endpoint-element.md) element.</span></span> <span data-ttu-id="27fe4-107">这样，终结点可以共享公共行为配置而不用重新定义设置。</span><span class="sxs-lookup"><span data-stu-id="27fe4-107">This allows endpoints to share common behavior configurations without redefining the settings.</span></span> <span data-ttu-id="27fe4-108">从 .NET Framework 4 开始，绑定和行为不需要具有名称。</span><span class="sxs-lookup"><span data-stu-id="27fe4-108">Starting with .NET Framework 4, bindings and behaviors are not required to have a name.</span></span> <span data-ttu-id="27fe4-109">有关默认配置和无值绑定和行为的详细信息，请参阅[WCF 服务的](../../../wcf/samples/simplified-configuration-for-wcf-services.md)[简化配置](../../../wcf/simplified-configuration.md)和简化配置。</span><span class="sxs-lookup"><span data-stu-id="27fe4-109">For more information about default configuration and nameless bindings and behaviors, see [Simplified Configuration](../../../wcf/simplified-configuration.md) and [Simplified Configuration for WCF Services](../../../wcf/samples/simplified-configuration-for-wcf-services.md).</span></span>  
  
> [!NOTE]
> <span data-ttu-id="27fe4-110">特定于 Windows 工作流活动的行为元素（例如 [\<sendMessageChannelCache>](../windows-workflow-foundation/sendmessagechannelcache.md) 元素）记录在页的[ \<behavior> \<serviceBehaviors> ](../windows-workflow-foundation/behavior-of-servicebehaviors-of-workflow.md)中。</span><span class="sxs-lookup"><span data-stu-id="27fe4-110">Behavior elements specific to Windows Workflow activities, such as the [\<sendMessageChannelCache>](../windows-workflow-foundation/sendmessagechannelcache.md) element, are documented in the [\<behavior> of \<serviceBehaviors>](../windows-workflow-foundation/behavior-of-servicebehaviors-of-workflow.md) page.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<behaviors>**](behaviors.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<serviceBehaviors>**](servicebehaviors.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<behavior>**  
  
## <a name="syntax"></a><span data-ttu-id="27fe4-111">语法</span><span class="sxs-lookup"><span data-stu-id="27fe4-111">Syntax</span></span>  
  
```xml  
<system.ServiceModel>
  <behaviors>
    <serviceBehaviors>
       <behavior name="String" />
    </serviceBehaviors>
  </behaviors>
</system.ServiceModel>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="27fe4-112">特性和元素</span><span class="sxs-lookup"><span data-stu-id="27fe4-112">Attributes and Elements</span></span>  

 <span data-ttu-id="27fe4-113">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="27fe4-113">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="27fe4-114">特性</span><span class="sxs-lookup"><span data-stu-id="27fe4-114">Attributes</span></span>  
  
|<span data-ttu-id="27fe4-115">属性</span><span class="sxs-lookup"><span data-stu-id="27fe4-115">Attribute</span></span>|<span data-ttu-id="27fe4-116">说明</span><span class="sxs-lookup"><span data-stu-id="27fe4-116">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="27fe4-117">name</span><span class="sxs-lookup"><span data-stu-id="27fe4-117">name</span></span>|<span data-ttu-id="27fe4-118">一个包含行为的配置名称的唯一字符串。</span><span class="sxs-lookup"><span data-stu-id="27fe4-118">A unique string that contains the configuration name of the behavior.</span></span> <span data-ttu-id="27fe4-119">此值是用户定义的一个字符串，该字符串必须是唯一的，因为它将充当元素的标识字符串。</span><span class="sxs-lookup"><span data-stu-id="27fe4-119">This value is a user-defined string that must be unique, since it acts as the identification string for the element.</span></span> <span data-ttu-id="27fe4-120">从 .NET Framework 4 开始，绑定和行为不需要具有名称。</span><span class="sxs-lookup"><span data-stu-id="27fe4-120">Starting with .NET Framework 4, bindings and behaviors are not required to have a name.</span></span> <span data-ttu-id="27fe4-121">有关默认配置和无值绑定和行为的详细信息，请参阅[WCF 服务的](../../../wcf/samples/simplified-configuration-for-wcf-services.md)[简化配置](../../../wcf/simplified-configuration.md)和简化配置。</span><span class="sxs-lookup"><span data-stu-id="27fe4-121">For more information about default configuration and nameless bindings and behaviors, see [Simplified Configuration](../../../wcf/simplified-configuration.md) and [Simplified Configuration for WCF Services](../../../wcf/samples/simplified-configuration-for-wcf-services.md).</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="27fe4-122">子元素</span><span class="sxs-lookup"><span data-stu-id="27fe4-122">Child Elements</span></span>  
  
|<span data-ttu-id="27fe4-123">元素</span><span class="sxs-lookup"><span data-stu-id="27fe4-123">Element</span></span>|<span data-ttu-id="27fe4-124">说明</span><span class="sxs-lookup"><span data-stu-id="27fe4-124">Description</span></span>|  
|-------------|-----------------|  
|[\<dataContractSerializer>](datacontractserializer-element.md)|<span data-ttu-id="27fe4-125">包含 DataContractSerializer 的配置数据。</span><span class="sxs-lookup"><span data-stu-id="27fe4-125">Contains configuration data for the DataContractSerializer.</span></span>|  
|[\<persistenceProvider>](persistenceprovider.md)|<span data-ttu-id="27fe4-126">指定要使用的持久性提供程序实现的类型以及用于持久性操作的超时值。</span><span class="sxs-lookup"><span data-stu-id="27fe4-126">Specifies the type of the persistence provider implementation to use, as well as the time-out to use for persistence operations.</span></span>|  
|[\<routing>](routing-of-servicebehavior.md)|<span data-ttu-id="27fe4-127">提供对路由服务的运行时访问以允许对路由配置进行动态修改。</span><span class="sxs-lookup"><span data-stu-id="27fe4-127">Provides run-time access to the routing service to allow dynamic modification of the routing configuration.</span></span>|  
|[\<serviceAuthenticationManager>](serviceauthenticationmanager.md)|<span data-ttu-id="27fe4-128">提供一个工作流配置元素，该元素在服务级别建立传输、消息或发起方的有效性。</span><span class="sxs-lookup"><span data-stu-id="27fe4-128">Provides a workflow configuration element that establishes at the service level the validity of a transmission, message, or originator..</span></span>|  
|[\<serviceAuthorization>](serviceauthorization-element.md)|<span data-ttu-id="27fe4-129">指定用于授予服务操作访问权限的设置。</span><span class="sxs-lookup"><span data-stu-id="27fe4-129">Specifies settings that authorize access to service operations.</span></span>|  
|[\<serviceCredentials>](servicecredentials.md)|<span data-ttu-id="27fe4-130">指定要用于对服务进行身份验证的凭据以及与客户端凭据验证相关的设置。</span><span class="sxs-lookup"><span data-stu-id="27fe4-130">Specifies the credential to be used in authenticating the service and the client credential validation-related settings.</span></span>|  
|[\<serviceDebug>](servicedebug.md)|<span data-ttu-id="27fe4-131">指定 Windows Communication Foundation (WCF) 服务的调试和帮助信息功能。</span><span class="sxs-lookup"><span data-stu-id="27fe4-131">Specifies debugging and help information features for a Windows Communication Foundation (WCF) service.</span></span>|  
|[\<serviceDiscovery>](servicediscovery.md)|<span data-ttu-id="27fe4-132">指定服务终结点的可发现性。</span><span class="sxs-lookup"><span data-stu-id="27fe4-132">Specifies the discoverability of service endpoints.</span></span>|  
|[\<serviceMetadata>](servicemetadata.md)|<span data-ttu-id="27fe4-133">指定服务元数据的发布和相关信息。</span><span class="sxs-lookup"><span data-stu-id="27fe4-133">Specifies the publication of service metadata and associated information.</span></span>|  
|[\<serviceSecurityAudit>](servicesecurityaudit.md)|<span data-ttu-id="27fe4-134">指定用于在服务操作过程中启用安全事件审核的设置。</span><span class="sxs-lookup"><span data-stu-id="27fe4-134">Specifies settings that enable auditing of security events during service operations.</span></span>|  
|[\<serviceThrottling>](servicethrottling.md)|<span data-ttu-id="27fe4-135">指定 WCF 服务的限制机制。</span><span class="sxs-lookup"><span data-stu-id="27fe4-135">Specifies the throttling mechanism of a WCF service.</span></span>|  
|[\<serviceTimeouts>](servicetimeouts.md)|<span data-ttu-id="27fe4-136">指定服务的超时。</span><span class="sxs-lookup"><span data-stu-id="27fe4-136">Specifies the timeout for a service.</span></span>|  
|[\<workflowRuntime>](workflowruntime.md)|<span data-ttu-id="27fe4-137">指定用于承载基于工作流的 WCF 服务的 WorkflowRuntime 实例的设置。</span><span class="sxs-lookup"><span data-stu-id="27fe4-137">Specifies settings for an instance of WorkflowRuntime for hosting workflow-based WCF services.</span></span>|  
|[\<useRequestHeadersForMetadataAddress>](userequestheadersformetadataaddress.md)|<span data-ttu-id="27fe4-138">允许从请求消息头中检索元数据地址信息。</span><span class="sxs-lookup"><span data-stu-id="27fe4-138">Enables the retrieval of metadata address information from the request message headers.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="27fe4-139">父元素</span><span class="sxs-lookup"><span data-stu-id="27fe4-139">Parent Elements</span></span>  
  
|<span data-ttu-id="27fe4-140">元素</span><span class="sxs-lookup"><span data-stu-id="27fe4-140">Element</span></span>|<span data-ttu-id="27fe4-141">说明</span><span class="sxs-lookup"><span data-stu-id="27fe4-141">Description</span></span>|  
|-------------|-----------------|  
|[\<serviceBehaviors>](servicebehaviors.md)|<span data-ttu-id="27fe4-142">服务行为元素的集合。</span><span class="sxs-lookup"><span data-stu-id="27fe4-142">A collection of service behavior elements.</span></span>|
