---
description: 了解详细信息： <endpointDiscovery>
title: <endpointDiscovery>
ms.date: 03/30/2017
ms.assetid: 70812717-888a-4748-9640-0df6715ff029
ms.openlocfilehash: 01913de37ae426484d5bb1ff6a815a64302024fb
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99782125"
---
# \<endpointDiscovery>

<span data-ttu-id="bf673-102">指定终结点的各种发现设置，例如终结点的可发现性、范围以及对终结点元数据的任何自定义扩展。</span><span class="sxs-lookup"><span data-stu-id="bf673-102">Specifies the various discovery settings for an endpoint, such as its discoverability, scopes, and any custom extensions to its metadata.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<behaviors>**](behaviors.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<endpointBehaviors>**](endpointbehaviors.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<behavior>**](behavior-of-endpointbehaviors.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<endpointDiscovery>**  
  
## <a name="syntax"></a><span data-ttu-id="bf673-103">语法</span><span class="sxs-lookup"><span data-stu-id="bf673-103">Syntax</span></span>  
  
```xml  
<behaviors>
  <endpointBehaviors>
    <behavior name="String">
      <endpointDiscovery enabled="Boolean">
        <scopes>
          <add scope="URI"/>
        </scopes>
        <extensions />
      </endpointDiscovery>
    </behavior>
  </endpointBehaviors>
</behaviors>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="bf673-104">特性和元素</span><span class="sxs-lookup"><span data-stu-id="bf673-104">Attributes and Elements</span></span>  

 <span data-ttu-id="bf673-105">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="bf673-105">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="bf673-106">特性</span><span class="sxs-lookup"><span data-stu-id="bf673-106">Attributes</span></span>  
  
|<span data-ttu-id="bf673-107">属性</span><span class="sxs-lookup"><span data-stu-id="bf673-107">Attribute</span></span>|<span data-ttu-id="bf673-108">说明</span><span class="sxs-lookup"><span data-stu-id="bf673-108">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="bf673-109">enabled</span><span class="sxs-lookup"><span data-stu-id="bf673-109">enabled</span></span>|<span data-ttu-id="bf673-110">一个布尔值，指定是否在此终结点上启用可发现性。</span><span class="sxs-lookup"><span data-stu-id="bf673-110">A Boolean value that specifies whether discoverability is enabled on this endpoint.</span></span> <span data-ttu-id="bf673-111">默认值为 `false`。</span><span class="sxs-lookup"><span data-stu-id="bf673-111">The default is `false`.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="bf673-112">子元素</span><span class="sxs-lookup"><span data-stu-id="bf673-112">Child Elements</span></span>  
  
|<span data-ttu-id="bf673-113">元素</span><span class="sxs-lookup"><span data-stu-id="bf673-113">Element</span></span>|<span data-ttu-id="bf673-114">说明</span><span class="sxs-lookup"><span data-stu-id="bf673-114">Description</span></span>|  
|-------------|-----------------|  
|[\<scopes>](scopes.md)|<span data-ttu-id="bf673-115">终结点的范围 URI 集合。</span><span class="sxs-lookup"><span data-stu-id="bf673-115">A collection of scope URIs for the endpoint.</span></span> <span data-ttu-id="bf673-116">一个终结点可以与多个范围 URI 关联。</span><span class="sxs-lookup"><span data-stu-id="bf673-116">More than one scope Uris can be associated with a single endpoint.</span></span>|  
|<span data-ttu-id="bf673-117">[\<extensions>](extensions.md) [of \<endpointDiscovery> ]</span><span class="sxs-lookup"><span data-stu-id="bf673-117">[\<extensions>](extensions.md) [of \<endpointDiscovery>]</span></span>|<span data-ttu-id="bf673-118">一个 XML 元素集合，用于指定要对终结点发布的自定义元数据。</span><span class="sxs-lookup"><span data-stu-id="bf673-118">A collection of XML elements that allows you to specify custom metadata to be published for an endpoint.</span></span>|  
|\<types>|<span data-ttu-id="bf673-119">要搜索的接口集合。</span><span class="sxs-lookup"><span data-stu-id="bf673-119">A collection of interfaces to search for.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="bf673-120">父元素</span><span class="sxs-lookup"><span data-stu-id="bf673-120">Parent Elements</span></span>  
  
|<span data-ttu-id="bf673-121">元素</span><span class="sxs-lookup"><span data-stu-id="bf673-121">Element</span></span>|<span data-ttu-id="bf673-122">说明</span><span class="sxs-lookup"><span data-stu-id="bf673-122">Description</span></span>|  
|-------------|-----------------|  
|[\<behavior>](behavior-of-endpointbehaviors.md)|<span data-ttu-id="bf673-123">指定行为元素。</span><span class="sxs-lookup"><span data-stu-id="bf673-123">Specifies a behavior element.</span></span>|  
|||  
  
## <a name="remarks"></a><span data-ttu-id="bf673-124">备注</span><span class="sxs-lookup"><span data-stu-id="bf673-124">Remarks</span></span>  

 <span data-ttu-id="bf673-125">如果将此配置元素添加到终结点的行为配置，并将 `enabled` 特性设置为 `true`，此配置元素将启用该终结点的可发现性。</span><span class="sxs-lookup"><span data-stu-id="bf673-125">When added to the endpoint’s behavior configuration and with the `enabled` attribute set to `true`, this configuration element enables its discoverability.</span></span> <span data-ttu-id="bf673-126">此外，还可以使用 [\<scopes>](scopes.md) 子元素指定可用于在查询期间筛选服务终结点的自定义范围 uri，并使用 [\<extensions>](extensions.md) 子元素指定应随标准可发现元数据一起发布的自定义元数据 (EPR、ContractTypeName、BindingName、Scope 和 ListenURI) 。</span><span class="sxs-lookup"><span data-stu-id="bf673-126">In addition, you can use the [\<scopes>](scopes.md)child element to specifying custom scope Uris that can be used to filter service endpoints during query, as well as the [\<extensions>](extensions.md) child element to specify custom metadata that should be published along with the standard discoverable metadata (EPR, ContractTypeName, BindingName, Scope and ListenURI).</span></span>  
  
 <span data-ttu-id="bf673-127">此配置元素依赖于 [\<serviceDiscovery>](servicediscovery.md) 提供可发现性服务级别控制的元素。</span><span class="sxs-lookup"><span data-stu-id="bf673-127">This configuration element is dependent on the [\<serviceDiscovery>](servicediscovery.md) element that provides the service level control of discoverability.</span></span> <span data-ttu-id="bf673-128">这意味着，如果 [\<serviceDiscovery>](servicediscovery.md) 配置中不存在此元素的设置，则会将其忽略。</span><span class="sxs-lookup"><span data-stu-id="bf673-128">This means that this element’s settings are ignored if [\<serviceDiscovery>](servicediscovery.md) is not present in the configuration.</span></span>  
  
## <a name="example"></a><span data-ttu-id="bf673-129">示例</span><span class="sxs-lookup"><span data-stu-id="bf673-129">Example</span></span>  

 <span data-ttu-id="bf673-130">下面的配置示例指定要对终结点发布的筛选范围和扩展元数据。</span><span class="sxs-lookup"><span data-stu-id="bf673-130">The following configuration example specifies filtering scopes and extension metadata to be published for an endpoint.</span></span>  
  
```xml  
<services>
  <service name="CalculatorService"
           behaviorConfiguration="CalculatorServiceBehavior">
    <endpoint binding="basicHttpBinding"
              address="calculator"
              contract="ICalculatorService"
              behaviorConfiguration="calculatorEndpointBehavior" />
  </service>
</services>
<behaviors>
  <serviceBehaviors>
    <behavior name="CalculatorServiceBehavior">
      <serviceDiscovery />
    </behavior>
  </serviceBehaviors>
  <endpointBehaviors>
    <behavior name="calculatorEndpointBehavior">
      <endpointDiscovery enabled="true">
        <scopes>
          <add scope="http://contoso/test1" />
          <add scope="http://contoso/test2" />
        </scopes>
        <extensions>
          <e:Publisher xmlns:e="http://example.org">
            <e:Name>The Example Organization</e:Name>
            <e:Address>One Example Way, ExampleTown, EX 12345</e:Address>
            <e:Contact>support@example.org</e:Contact>
          </e:Publisher>
          <AnotherCustomMetadata>Custom Metadata</AnotherCustomMetadata>
        </extensions>
      </endpointDiscovery>
    </behavior>
  </endpointBehaviors>
</behaviors>
```  
  
## <a name="see-also"></a><span data-ttu-id="bf673-131">请参阅</span><span class="sxs-lookup"><span data-stu-id="bf673-131">See also</span></span>

- <xref:System.ServiceModel.Discovery.EndpointDiscoveryBehavior>
