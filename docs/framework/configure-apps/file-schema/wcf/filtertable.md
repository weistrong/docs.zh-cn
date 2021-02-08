---
description: 了解详细信息： <filterTable>
title: <filterTable>
ms.date: 03/30/2017
ms.assetid: e9f05441-3ad1-49b9-a267-71724aa094b4
ms.openlocfilehash: 2051bb0e778e5676f39d91b7d7ba415fd7e523af
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99782034"
---
# \<filterTable>

<span data-ttu-id="730a1-102">表示一个路由表，此表包含计算消息所依据的筛选器的列表，以及当筛选器的计算结果为 true 时消息要路由到的客户端终结点。</span><span class="sxs-lookup"><span data-stu-id="730a1-102">Represents a routing table that contains a list of filters to evaluate messages against and the client endpoint to route messages to if the filter evaluates to true.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<routing>**](routing.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<filterTables>**](filtertables.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<filterTable>**  
  
## <a name="syntax"></a><span data-ttu-id="730a1-103">语法</span><span class="sxs-lookup"><span data-stu-id="730a1-103">Syntax</span></span>  
  
```xml  
<routing>
  <filterTables>
     name="String">
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
  
## <a name="attributes-and-elements"></a><span data-ttu-id="730a1-104">特性和元素</span><span class="sxs-lookup"><span data-stu-id="730a1-104">Attributes and Elements</span></span>  

 <span data-ttu-id="730a1-105">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="730a1-105">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="730a1-106">特性</span><span class="sxs-lookup"><span data-stu-id="730a1-106">Attributes</span></span>  
  
|<span data-ttu-id="730a1-107">元素</span><span class="sxs-lookup"><span data-stu-id="730a1-107">Element</span></span>|<span data-ttu-id="730a1-108">说明</span><span class="sxs-lookup"><span data-stu-id="730a1-108">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="730a1-109">name</span><span class="sxs-lookup"><span data-stu-id="730a1-109">name</span></span>|<span data-ttu-id="730a1-110">一个字符串，包含此配置元素的唯一名称。</span><span class="sxs-lookup"><span data-stu-id="730a1-110">A string that contains the unique name of this configuration element.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="730a1-111">子元素</span><span class="sxs-lookup"><span data-stu-id="730a1-111">Child Elements</span></span>  
  
|<span data-ttu-id="730a1-112">元素</span><span class="sxs-lookup"><span data-stu-id="730a1-112">Element</span></span>|<span data-ttu-id="730a1-113">说明</span><span class="sxs-lookup"><span data-stu-id="730a1-113">Description</span></span>|  
|-------------|-----------------|  
|[\<filters>](filters-of-routing.md)|<span data-ttu-id="730a1-114">路由筛选器与在筛选器匹配时消息要发送到的目标终结点之间的映射。</span><span class="sxs-lookup"><span data-stu-id="730a1-114">Mappings between the routing filters and the target endpoints to send messages to when the filter matches.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="730a1-115">父元素</span><span class="sxs-lookup"><span data-stu-id="730a1-115">Parent Elements</span></span>  
  
|<span data-ttu-id="730a1-116">元素</span><span class="sxs-lookup"><span data-stu-id="730a1-116">Element</span></span>|<span data-ttu-id="730a1-117">说明</span><span class="sxs-lookup"><span data-stu-id="730a1-117">Description</span></span>|  
|-------------|-----------------|  
|[\<routing>](routing.md)|<span data-ttu-id="730a1-118">一个包含路由表的配置节。</span><span class="sxs-lookup"><span data-stu-id="730a1-118">A configuration section that contains routing tables.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="730a1-119">请参阅</span><span class="sxs-lookup"><span data-stu-id="730a1-119">See also</span></span>

- <xref:System.ServiceModel.Routing.Configuration.RoutingSection?displayProperty=nameWithType>
