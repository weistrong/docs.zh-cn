---
description: 了解详细 <add> 信息： <entries>
title: <add> 的 <entries>
ms.date: 03/30/2017
ms.assetid: 3af4805b-dc72-4f68-b168-da4fba8c6170
ms.openlocfilehash: 0be24fb9d2327d411368dd05afc21156dfaf3d3a
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99803966"
---
# <a name="add-of-entries"></a><span data-ttu-id="642c5-103">\<add> 的 \<entries></span><span class="sxs-lookup"><span data-stu-id="642c5-103">\<add> of \<entries></span></span>

<span data-ttu-id="642c5-104">表示将筛选器映射到以前定义的客户端终结点的路由项。</span><span class="sxs-lookup"><span data-stu-id="642c5-104">Represents a routing entry that maps a filter to a client endpoint that was previously defined.</span></span> <span data-ttu-id="642c5-105">与此筛选器匹配的消息将发送到此目标。</span><span class="sxs-lookup"><span data-stu-id="642c5-105">Messages matching this filter will be sent to this destination.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<routing>**](routing.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<filterTables>**](filtertables.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<filterTable>**](filtertable.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<entries>**](entries.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<add>**  
  
## <a name="syntax"></a><span data-ttu-id="642c5-106">语法</span><span class="sxs-lookup"><span data-stu-id="642c5-106">Syntax</span></span>  
  
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
  
## <a name="attributes-and-elements"></a><span data-ttu-id="642c5-107">特性和元素</span><span class="sxs-lookup"><span data-stu-id="642c5-107">Attributes and Elements</span></span>  

 <span data-ttu-id="642c5-108">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="642c5-108">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="642c5-109">特性</span><span class="sxs-lookup"><span data-stu-id="642c5-109">Attributes</span></span>  
  
|<span data-ttu-id="642c5-110">属性</span><span class="sxs-lookup"><span data-stu-id="642c5-110">Attribute</span></span>|<span data-ttu-id="642c5-111">说明</span><span class="sxs-lookup"><span data-stu-id="642c5-111">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="642c5-112">backupList</span><span class="sxs-lookup"><span data-stu-id="642c5-112">backupList</span></span>|<span data-ttu-id="642c5-113">一个字符串，指定对终结点备份列表的引用。</span><span class="sxs-lookup"><span data-stu-id="642c5-113">A string that specifies a reference to a backup list of endpoints.</span></span>|  
|<span data-ttu-id="642c5-114">endpoint</span><span class="sxs-lookup"><span data-stu-id="642c5-114">endpoint</span></span>|<span data-ttu-id="642c5-115">一个字符串，指定对客户端终结点的引用，该终结点将接收与 `filterName` 特性所指定的筛选器匹配的消息。</span><span class="sxs-lookup"><span data-stu-id="642c5-115">A string that specifies a reference to a client endpoint that will receive messages that match the filter specified by the `filterName` attribute.</span></span>|  
|<span data-ttu-id="642c5-116">filterName</span><span class="sxs-lookup"><span data-stu-id="642c5-116">filterName</span></span>|<span data-ttu-id="642c5-117">一个字符串，指定对筛选器元素的引用。</span><span class="sxs-lookup"><span data-stu-id="642c5-117">A string that specifies a reference to a filter element.</span></span>|  
|<span data-ttu-id="642c5-118">priority</span><span class="sxs-lookup"><span data-stu-id="642c5-118">priority</span></span>|<span data-ttu-id="642c5-119">一个整数，指定此项的优先级。</span><span class="sxs-lookup"><span data-stu-id="642c5-119">An integer that specifies the priority of this entry.</span></span><br /><br /> <span data-ttu-id="642c5-120">将根据优先级计算路由表中的项，0 表示优先级最低。</span><span class="sxs-lookup"><span data-stu-id="642c5-120">Entries in the routing table will be evaluated based on priority, with 0 being the lowest priority.</span></span> <span data-ttu-id="642c5-121">将同时计算某个特定优先级的所有项，如果未找到当前优先级的匹配项，将计算下一个优先级。</span><span class="sxs-lookup"><span data-stu-id="642c5-121">All entries for a specific priority are evaluated simultaneously, if no matching entry is found for the current priority, the next priority level will be evaluated.</span></span><br /><br /> <span data-ttu-id="642c5-122">此值是可选的。</span><span class="sxs-lookup"><span data-stu-id="642c5-122">This value is optional.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="642c5-123">子元素</span><span class="sxs-lookup"><span data-stu-id="642c5-123">Child Elements</span></span>  

 <span data-ttu-id="642c5-124">无。</span><span class="sxs-lookup"><span data-stu-id="642c5-124">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="642c5-125">父元素</span><span class="sxs-lookup"><span data-stu-id="642c5-125">Parent Elements</span></span>  
  
|<span data-ttu-id="642c5-126">元素</span><span class="sxs-lookup"><span data-stu-id="642c5-126">Element</span></span>|<span data-ttu-id="642c5-127">说明</span><span class="sxs-lookup"><span data-stu-id="642c5-127">Description</span></span>|  
|-------------|-----------------|  
|[\<routing>](routing.md)|<span data-ttu-id="642c5-128">一个包含路由映射项的配置节。</span><span class="sxs-lookup"><span data-stu-id="642c5-128">A configuration section that contains routing mapping entries.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="642c5-129">请参阅</span><span class="sxs-lookup"><span data-stu-id="642c5-129">See also</span></span>

- <xref:System.ServiceModel.Routing.Configuration.RoutingSection?displayProperty=nameWithType>
- <xref:System.ServiceModel.Routing.Configuration.FilterTableEntryElement?displayProperty=nameWithType>
