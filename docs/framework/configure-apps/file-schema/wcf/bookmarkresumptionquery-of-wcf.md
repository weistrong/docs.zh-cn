---
description: 了解有关 WCF 的详细信息： <bookmarkResumptionQuery>
title: <bookmarkResumptionQuery> WCF 的
ms.date: 03/30/2017
ms.assetid: 755a34f0-87c9-4a1e-ae4d-0fb8a6fbdc0e
ms.openlocfilehash: 9dadab3e304a2507a404bf43c377df46d5b33dda
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99639323"
---
# <a name="bookmarkresumptionquery-of-wcf"></a><span data-ttu-id="97be9-103">\<bookmarkResumptionQuery> WCF 的</span><span class="sxs-lookup"><span data-stu-id="97be9-103">\<bookmarkResumptionQuery> of WCF</span></span>

<span data-ttu-id="97be9-104">表示一个查询，该查询用于跟踪工作流实例中的书签恢复。</span><span class="sxs-lookup"><span data-stu-id="97be9-104">Represents a query that is used to track resumption of a bookmark within a workflow instance.</span></span> <span data-ttu-id="97be9-105">跟踪参与者需要用此查询来订阅书签恢复记录。</span><span class="sxs-lookup"><span data-stu-id="97be9-105">The query is necessary for a tracking participant to subscribe to bookmark resumption records.</span></span>  
  
<span data-ttu-id="97be9-106">有关跟踪配置文件查询的详细信息，请参阅 [跟踪配置文件](../../../windows-workflow-foundation/tracking-profiles.md)。</span><span class="sxs-lookup"><span data-stu-id="97be9-106">For more information on tracking profile queries, see [Tracking Profiles](../../../windows-workflow-foundation/tracking-profiles.md).</span></span>
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<tracking>**](tracking-of-wcf.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<profiles>**\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<trackingProfile>**](trackingprofile-of-wcf.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<workflow>**](workflow-of-wcf.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<bookmarkResumptionQueries>**](bookmarkresumptionqueries-of-wcf.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<bookmarkResumptionQuery>**  
  
## <a name="syntax"></a><span data-ttu-id="97be9-107">语法</span><span class="sxs-lookup"><span data-stu-id="97be9-107">Syntax</span></span>  
  
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
  
## <a name="attributes-and-elements"></a><span data-ttu-id="97be9-108">特性和元素</span><span class="sxs-lookup"><span data-stu-id="97be9-108">Attributes and elements</span></span>

<span data-ttu-id="97be9-109">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="97be9-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="97be9-110">特性</span><span class="sxs-lookup"><span data-stu-id="97be9-110">Attributes</span></span>  
  
|<span data-ttu-id="97be9-111">属性</span><span class="sxs-lookup"><span data-stu-id="97be9-111">Attribute</span></span>|<span data-ttu-id="97be9-112">说明</span><span class="sxs-lookup"><span data-stu-id="97be9-112">Description</span></span>|  
|---------------|-----------------|  
|`name`|<span data-ttu-id="97be9-113">一个字符串，指定要订阅的书签记录的名称。</span><span class="sxs-lookup"><span data-stu-id="97be9-113">A string that specifies the name of the bookmark record to subscribe to.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="97be9-114">子元素</span><span class="sxs-lookup"><span data-stu-id="97be9-114">Child elements</span></span>

<span data-ttu-id="97be9-115">无。</span><span class="sxs-lookup"><span data-stu-id="97be9-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="97be9-116">父元素</span><span class="sxs-lookup"><span data-stu-id="97be9-116">Parent elements</span></span>  
  
|<span data-ttu-id="97be9-117">元素</span><span class="sxs-lookup"><span data-stu-id="97be9-117">Element</span></span>|<span data-ttu-id="97be9-118">说明</span><span class="sxs-lookup"><span data-stu-id="97be9-118">Description</span></span>|  
|-------------|-----------------|  
|[\<bookmarkResumptionQueries>](bookmarkresumptionqueries-of-wcf.md)|<span data-ttu-id="97be9-119">表示一个查询集合，这些查询用于跟踪工作流实例中的书签恢复。</span><span class="sxs-lookup"><span data-stu-id="97be9-119">Represents a collection of queries that are used to track resumption of a bookmark within a workflow instance.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="97be9-120">请参阅</span><span class="sxs-lookup"><span data-stu-id="97be9-120">See also</span></span>

- <xref:System.ServiceModel.Activities.Tracking.Configuration.BookmarkResumptionQueryElementCollection?displayProperty=nameWithType>
- <xref:System.Activities.Tracking.BookmarkResumptionQuery?displayProperty=nameWithType>
- [<span data-ttu-id="97be9-121">工作流跟踪</span><span class="sxs-lookup"><span data-stu-id="97be9-121">Workflow Tracking and Tracing</span></span>](../../../windows-workflow-foundation/workflow-tracking-and-tracing.md)
- [<span data-ttu-id="97be9-122">跟踪配置文件</span><span class="sxs-lookup"><span data-stu-id="97be9-122">Tracking Profiles</span></span>](../../../windows-workflow-foundation/tracking-profiles.md)
