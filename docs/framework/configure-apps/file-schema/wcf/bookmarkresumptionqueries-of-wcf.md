---
description: 了解有关 WCF 的详细信息： <bookmarkResumptionQueries>
title: <bookmarkResumptionQueries> WCF 的
ms.date: 03/30/2017
ms.assetid: ed086712-1dc7-4932-a592-d1116a0155f3
ms.openlocfilehash: dfe631865549915760255b1df22ee970b806e368
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99639362"
---
# <a name="bookmarkresumptionqueries-of-wcf"></a><span data-ttu-id="9affc-103">\<bookmarkResumptionQueries> WCF 的</span><span class="sxs-lookup"><span data-stu-id="9affc-103">\<bookmarkResumptionQueries> of WCF</span></span>
  
<span data-ttu-id="9affc-104">表示一个查询集合，这些查询用于跟踪工作流实例中的书签恢复。</span><span class="sxs-lookup"><span data-stu-id="9affc-104">Represents a collection of queries that are used to track resumption of a bookmark within a workflow instance.</span></span> <span data-ttu-id="9affc-105">跟踪参与者需要用此查询来订阅书签恢复记录。</span><span class="sxs-lookup"><span data-stu-id="9affc-105">The query is necessary for a tracking participant to subscribe to bookmark resumption records.</span></span>  
  
<span data-ttu-id="9affc-106">有关跟踪配置文件查询的详细信息，请参阅 [跟踪配置文件](../../../windows-workflow-foundation/tracking-profiles.md)。</span><span class="sxs-lookup"><span data-stu-id="9affc-106">For more information on tracking profile queries, see [Tracking Profiles](../../../windows-workflow-foundation/tracking-profiles.md).</span></span>
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<tracking>**](tracking-of-wcf.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<profiles>**\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<trackingProfile>**](trackingprofile-of-wcf.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<workflow>**](workflow-of-wcf.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<bookmarkResumptionQueries>**  

## <a name="syntax"></a><span data-ttu-id="9affc-107">语法</span><span class="sxs-lookup"><span data-stu-id="9affc-107">Syntax</span></span>  
  
```xml  
<tracking>
  <profiles>
    <trackingProfile name="Name">
      <workflow>
        <bookmarkResumptionQueries>
          <bookmarkResumptionQuery name="String" />
        </bookmarkResumptionQueries>
      </workflow>
    </trackingProfile>
  </profiles>
</tracking>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="9affc-108">特性和元素</span><span class="sxs-lookup"><span data-stu-id="9affc-108">Attributes and elements</span></span>  
  
<span data-ttu-id="9affc-109">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="9affc-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="9affc-110">特性</span><span class="sxs-lookup"><span data-stu-id="9affc-110">Attributes</span></span>  
  
<span data-ttu-id="9affc-111">无。</span><span class="sxs-lookup"><span data-stu-id="9affc-111">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="9affc-112">子元素</span><span class="sxs-lookup"><span data-stu-id="9affc-112">Child elements</span></span>  
  
|<span data-ttu-id="9affc-113">元素</span><span class="sxs-lookup"><span data-stu-id="9affc-113">Element</span></span>|<span data-ttu-id="9affc-114">说明</span><span class="sxs-lookup"><span data-stu-id="9affc-114">Description</span></span>|  
|-------------|-----------------|  
|[\<bookmarkResumptionQuery>](bookmarkresumptionquery-of-wcf.md)|<span data-ttu-id="9affc-115">一个查询，用于跟踪工作流实例中的书签恢复。</span><span class="sxs-lookup"><span data-stu-id="9affc-115">A query that is used to track resumption of a bookmark within a workflow instance.</span></span> <span data-ttu-id="9affc-116">跟踪参与者需要用此查询来订阅书签恢复记录。</span><span class="sxs-lookup"><span data-stu-id="9affc-116">The query is necessary for a tracking participant to subscribe to bookmark resumption records.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="9affc-117">父元素</span><span class="sxs-lookup"><span data-stu-id="9affc-117">Parent elements</span></span>  
  
|<span data-ttu-id="9affc-118">元素</span><span class="sxs-lookup"><span data-stu-id="9affc-118">Element</span></span>|<span data-ttu-id="9affc-119">说明</span><span class="sxs-lookup"><span data-stu-id="9affc-119">Description</span></span>|  
|-------------|-----------------|  
|[\<workflow>](../windows-workflow-foundation/workflow.md)|<span data-ttu-id="9affc-120">一个配置元素，包含 `activityDefinitionId` 属性所标识的特定工作流的所有查询。</span><span class="sxs-lookup"><span data-stu-id="9affc-120">A configuration element that contains all queries for a specific workflow identified by the `activityDefinitionId` property.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="9affc-121">请参阅</span><span class="sxs-lookup"><span data-stu-id="9affc-121">See also</span></span>

- <xref:System.ServiceModel.Activities.Tracking.Configuration.BookmarkResumptionQueryElementCollection?displayProperty=nameWithType>
- <xref:System.Activities.Tracking.BookmarkResumptionQuery?displayProperty=nameWithType>
- [<span data-ttu-id="9affc-122">工作流跟踪</span><span class="sxs-lookup"><span data-stu-id="9affc-122">Workflow Tracking and Tracing</span></span>](../../../windows-workflow-foundation/workflow-tracking-and-tracing.md)
- [<span data-ttu-id="9affc-123">跟踪配置文件</span><span class="sxs-lookup"><span data-stu-id="9affc-123">Tracking Profiles</span></span>](../../../windows-workflow-foundation/tracking-profiles.md)
