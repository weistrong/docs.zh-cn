---
description: 了解详细信息： <scopes>
title: <scopes>
ms.date: 03/30/2017
ms.assetid: 9a0dd3ce-e383-4ac3-b7be-7d604388304a
ms.openlocfilehash: 2df1101beb5b1bc09c2d98eb89a8200303c5b456
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99786858"
---
# \<scopes>

<span data-ttu-id="27834-102">包含一个配置元素集合，这些元素指定可用于在查询时筛选服务终结点的自定义范围 URI。</span><span class="sxs-lookup"><span data-stu-id="27834-102">Contains a collection of configuration elements that specify custom scope Uris that can be used to filter service endpoints during query.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<behaviors>**](behaviors.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<endpointBehaviors>**](endpointbehaviors.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<behavior>**](behavior-of-endpointbehaviors.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<endpointDiscovery>**](endpointdiscovery.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<scopes>**  
  
## <a name="syntax"></a><span data-ttu-id="27834-103">语法</span><span class="sxs-lookup"><span data-stu-id="27834-103">Syntax</span></span>  
  
```xml  
<behaviors>
  <endpointBehaviors>
    <behavior name="String">
      <endpointDiscovery enable="Boolean">
        <scopes>
          <add scope="URI" />
        </scopes>
      </endpointDiscovery>
    </behavior>
  </endpointBehaviors>
</behaviors>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="27834-104">特性和元素</span><span class="sxs-lookup"><span data-stu-id="27834-104">Attributes and Elements</span></span>  

 <span data-ttu-id="27834-105">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="27834-105">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="27834-106">特性</span><span class="sxs-lookup"><span data-stu-id="27834-106">Attributes</span></span>  

 <span data-ttu-id="27834-107">无。</span><span class="sxs-lookup"><span data-stu-id="27834-107">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="27834-108">子元素</span><span class="sxs-lookup"><span data-stu-id="27834-108">Child Elements</span></span>  
  
|<span data-ttu-id="27834-109">Attribute</span><span class="sxs-lookup"><span data-stu-id="27834-109">Attribute</span></span>|<span data-ttu-id="27834-110">说明</span><span class="sxs-lookup"><span data-stu-id="27834-110">Description</span></span>|  
|---------------|-----------------|  
|[\<add>](add-of-scopes.md)|<span data-ttu-id="27834-111">添加可在匹配条件以查找服务时使用的终结点的范围信息。</span><span class="sxs-lookup"><span data-stu-id="27834-111">Adds the scope information for the endpoint that can be used in matching criteria for finding services.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="27834-112">父元素</span><span class="sxs-lookup"><span data-stu-id="27834-112">Parent Elements</span></span>  
  
|<span data-ttu-id="27834-113">元素</span><span class="sxs-lookup"><span data-stu-id="27834-113">Element</span></span>|<span data-ttu-id="27834-114">说明</span><span class="sxs-lookup"><span data-stu-id="27834-114">Description</span></span>|  
|-------------|-----------------|  
|[\<endpointDiscovery>](endpointdiscovery.md)|<span data-ttu-id="27834-115">指定终结点的各种发现设置，例如终结点的可发现性、范围以及对终结点元数据的任何自定义扩展。</span><span class="sxs-lookup"><span data-stu-id="27834-115">Specifies the various discovery settings for an endpoint, such as its discoverability, scopes, and any custom extensions to its metadata.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="27834-116">请参阅</span><span class="sxs-lookup"><span data-stu-id="27834-116">See also</span></span>

- <xref:System.ServiceModel.Discovery.EndpointDiscoveryBehavior>
