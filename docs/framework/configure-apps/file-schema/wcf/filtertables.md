---
description: 了解详细信息： <filterTables>
title: <filterTables>
ms.date: 03/30/2017
ms.assetid: 41f1ac35-f559-473a-b2c3-8cc83a6a3831
ms.openlocfilehash: 932d0e162c3fdeba8b166d3adaaa73cc3b5293a9
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99664582"
---
# \<filterTables>

<span data-ttu-id="ac1a2-102">表示一个用于定义路由表的配置节，这些路由表包含路由筛选器与在筛选器匹配时消息要发送到的目标终结点之间的映射。</span><span class="sxs-lookup"><span data-stu-id="ac1a2-102">Represents a configuration section for defining routing tables that contain mappings between the routing filters and the target endpoints to send messages to when the filter matches.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<routing>**](routing.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<filterTables>**  
  
## <a name="syntax"></a><span data-ttu-id="ac1a2-103">语法</span><span class="sxs-lookup"><span data-stu-id="ac1a2-103">Syntax</span></span>  
  
```xml  
<routing>
  <filterTables>
    <filterTable name="String">
      <entries>
        <add backupList="String"
             endpointName="String"
             filterName="String"
             priority="Integer" />
      </entries>
    </filterTable>
  </filterTables>
</routing>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="ac1a2-104">特性和元素</span><span class="sxs-lookup"><span data-stu-id="ac1a2-104">Attributes and Elements</span></span>  

 <span data-ttu-id="ac1a2-105">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="ac1a2-105">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="ac1a2-106">特性</span><span class="sxs-lookup"><span data-stu-id="ac1a2-106">Attributes</span></span>  

 <span data-ttu-id="ac1a2-107">无。</span><span class="sxs-lookup"><span data-stu-id="ac1a2-107">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="ac1a2-108">子元素</span><span class="sxs-lookup"><span data-stu-id="ac1a2-108">Child Elements</span></span>  
  
|<span data-ttu-id="ac1a2-109">元素</span><span class="sxs-lookup"><span data-stu-id="ac1a2-109">Element</span></span>|<span data-ttu-id="ac1a2-110">说明</span><span class="sxs-lookup"><span data-stu-id="ac1a2-110">Description</span></span>|  
|-------------|-----------------|  
|[\<filters>](filters-of-routing.md)|<span data-ttu-id="ac1a2-111">一个路由表，包含路由筛选器与在筛选器匹配时消息要发送到的目标终结点之间的映射。</span><span class="sxs-lookup"><span data-stu-id="ac1a2-111">A routing table that contain mappings between the routing filters and the target endpoints to send messages to when the filter matches.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="ac1a2-112">父元素</span><span class="sxs-lookup"><span data-stu-id="ac1a2-112">Parent Elements</span></span>  
  
|<span data-ttu-id="ac1a2-113">元素</span><span class="sxs-lookup"><span data-stu-id="ac1a2-113">Element</span></span>|<span data-ttu-id="ac1a2-114">说明</span><span class="sxs-lookup"><span data-stu-id="ac1a2-114">Description</span></span>|  
|-------------|-----------------|  
|[\<routing>](routing.md)|<span data-ttu-id="ac1a2-115">一个包含路由筛选器和路由表的配置节。</span><span class="sxs-lookup"><span data-stu-id="ac1a2-115">A configuration section that contains routing filters and routing tables.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="ac1a2-116">请参阅</span><span class="sxs-lookup"><span data-stu-id="ac1a2-116">See also</span></span>

- <xref:System.ServiceModel.Routing.Configuration.RoutingSection?displayProperty=nameWithType>
- <xref:System.ServiceModel.Routing.Configuration.FilterTableCollection?displayProperty=nameWithType>
