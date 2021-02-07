---
description: 了解详细 <add> 信息： <scopes>
title: <add> 的 <scopes>
ms.date: 03/30/2017
ms.assetid: 0563a7d8-fc84-4c85-9066-af32665857c2
ms.openlocfilehash: e5582a7599c221e9ac00e03178911290e18ff536
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99750229"
---
# <a name="add-of-scopes"></a><span data-ttu-id="68d4f-103">\<add> 的 \<scopes></span><span class="sxs-lookup"><span data-stu-id="68d4f-103">\<add> of \<scopes></span></span>

<span data-ttu-id="68d4f-104">添加可用于在查询时筛选服务终结点的自定义范围 URI。</span><span class="sxs-lookup"><span data-stu-id="68d4f-104">Adds a custom scope Uri that can be used to filter service endpoints during query.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<behaviors>**](behaviors.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<endpointBehaviors>**](endpointbehaviors.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<behavior>**](behavior-of-endpointbehaviors.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<endpointDiscovery>**](endpointdiscovery.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<scopes>**](scopes.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<add>**  
  
## <a name="syntax"></a><span data-ttu-id="68d4f-105">语法</span><span class="sxs-lookup"><span data-stu-id="68d4f-105">Syntax</span></span>  
  
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
  
## <a name="attributes-and-elements"></a><span data-ttu-id="68d4f-106">特性和元素</span><span class="sxs-lookup"><span data-stu-id="68d4f-106">Attributes and Elements</span></span>  

 <span data-ttu-id="68d4f-107">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="68d4f-107">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="68d4f-108">特性</span><span class="sxs-lookup"><span data-stu-id="68d4f-108">Attributes</span></span>  
  
|<span data-ttu-id="68d4f-109">属性</span><span class="sxs-lookup"><span data-stu-id="68d4f-109">Attribute</span></span>|<span data-ttu-id="68d4f-110">描述</span><span class="sxs-lookup"><span data-stu-id="68d4f-110">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="68d4f-111">scope</span><span class="sxs-lookup"><span data-stu-id="68d4f-111">scope</span></span>|<span data-ttu-id="68d4f-112">一个 URI，包含在匹配条件以查找服务时可使用的终结点的范围信息。</span><span class="sxs-lookup"><span data-stu-id="68d4f-112">A URI that contains scope information for the endpoint that can be used in matching criteria for finding services.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="68d4f-113">子元素</span><span class="sxs-lookup"><span data-stu-id="68d4f-113">Child Elements</span></span>  

 <span data-ttu-id="68d4f-114">无。</span><span class="sxs-lookup"><span data-stu-id="68d4f-114">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="68d4f-115">父元素</span><span class="sxs-lookup"><span data-stu-id="68d4f-115">Parent Elements</span></span>  
  
|<span data-ttu-id="68d4f-116">元素</span><span class="sxs-lookup"><span data-stu-id="68d4f-116">Element</span></span>|<span data-ttu-id="68d4f-117">说明</span><span class="sxs-lookup"><span data-stu-id="68d4f-117">Description</span></span>|  
|-------------|-----------------|  
|[\<scopes>](scopes.md)|<span data-ttu-id="68d4f-118">包含一个配置元素集合，这些元素指定可用于在查询时筛选服务终结点的自定义范围 URI。</span><span class="sxs-lookup"><span data-stu-id="68d4f-118">Contains a collection of configuration elements that specify custom scope Uris that can be used to filter service endpoints during query.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="68d4f-119">请参阅</span><span class="sxs-lookup"><span data-stu-id="68d4f-119">See also</span></span>

- <xref:System.ServiceModel.Discovery.EndpointDiscoveryBehavior>
