---
description: 了解详细信息： <bookmarkResumptionQueries>
title: <bookmarkResumptionQueries>
ms.date: 03/30/2017
ms.topic: reference
ms.assetid: 8ed61a7f-4254-439c-bdd8-b474971533f7
ms.openlocfilehash: e8ff21e2183fe31411674e9d4de6bf3d99d14836
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99698149"
---
# \<bookmarkResumptionQueries>

<span data-ttu-id="ce8f6-102">表示一个查询集合，这些查询用于跟踪工作流实例中的书签恢复。</span><span class="sxs-lookup"><span data-stu-id="ce8f6-102">Represents a collection of queries that are used to track resumption of a bookmark within a workflow instance.</span></span> <span data-ttu-id="ce8f6-103">跟踪参与者需要用此查询来订阅书签恢复记录。</span><span class="sxs-lookup"><span data-stu-id="ce8f6-103">The query is necessary for a tracking participant to subscribe to bookmark resumption records.</span></span>  
  
 <span data-ttu-id="ce8f6-104">有关跟踪配置文件查询的详细信息，请参阅 [跟踪配置文件](../../../windows-workflow-foundation/tracking-profiles.md)</span><span class="sxs-lookup"><span data-stu-id="ce8f6-104">For more information on tracking profile queries, see [Tracking Profiles](../../../windows-workflow-foundation/tracking-profiles.md)</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.ServiceModel>**](system-servicemodel-of-workflow.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<tracking>**](tracking.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<trackingProfile>**](trackingprofile.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<workflow>**](workflow.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<bookmarkResumptionQueries>**  

## <a name="syntax"></a><span data-ttu-id="ce8f6-105">语法</span><span class="sxs-lookup"><span data-stu-id="ce8f6-105">Syntax</span></span>  
  
```xml  
<tracking>
  <trackingProfile name="Name">
    <workflow>
      <bookmarkResumptionQueries>
        <bookmarkResumptionQuery name="String" />
      </bookmarkResumptionQueries>
    </workflow>
  </trackingProfile>
</tracking>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="ce8f6-106">特性和元素</span><span class="sxs-lookup"><span data-stu-id="ce8f6-106">Attributes and Elements</span></span>  

 <span data-ttu-id="ce8f6-107">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="ce8f6-107">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="ce8f6-108">特性</span><span class="sxs-lookup"><span data-stu-id="ce8f6-108">Attributes</span></span>  

 <span data-ttu-id="ce8f6-109">无。</span><span class="sxs-lookup"><span data-stu-id="ce8f6-109">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="ce8f6-110">子元素</span><span class="sxs-lookup"><span data-stu-id="ce8f6-110">Child Elements</span></span>  
  
|<span data-ttu-id="ce8f6-111">元素</span><span class="sxs-lookup"><span data-stu-id="ce8f6-111">Element</span></span>|<span data-ttu-id="ce8f6-112">说明</span><span class="sxs-lookup"><span data-stu-id="ce8f6-112">Description</span></span>|  
|-------------|-----------------|  
|[\<bookmarkResumptionQuery>](bookmarkresumptionquery.md)|<span data-ttu-id="ce8f6-113">一个查询，用于跟踪工作流实例中的书签恢复。</span><span class="sxs-lookup"><span data-stu-id="ce8f6-113">A query that is used to track resumption of a bookmark within a workflow instance.</span></span> <span data-ttu-id="ce8f6-114">跟踪参与者需要用此查询来订阅书签恢复记录。</span><span class="sxs-lookup"><span data-stu-id="ce8f6-114">The query is necessary for a tracking participant to subscribe to bookmark resumption records.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="ce8f6-115">父元素</span><span class="sxs-lookup"><span data-stu-id="ce8f6-115">Parent Elements</span></span>  
  
|<span data-ttu-id="ce8f6-116">元素</span><span class="sxs-lookup"><span data-stu-id="ce8f6-116">Element</span></span>|<span data-ttu-id="ce8f6-117">说明</span><span class="sxs-lookup"><span data-stu-id="ce8f6-117">Description</span></span>|  
|-------------|-----------------|  
|[\<workflow>](workflow.md)|<span data-ttu-id="ce8f6-118">一个配置元素，该元素包含由 **activityDefinitionId** 属性标识的特定工作流的所有查询。</span><span class="sxs-lookup"><span data-stu-id="ce8f6-118">A configuration element that contains all queries for a specific workflow identified by the **activityDefinitionId** property.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="ce8f6-119">请参阅</span><span class="sxs-lookup"><span data-stu-id="ce8f6-119">See also</span></span>

- <xref:System.ServiceModel.Activities.Tracking.Configuration.BookmarkResumptionQueryElementCollection?displayProperty=nameWithType>
- <xref:System.Activities.Tracking.BookmarkResumptionQuery?displayProperty=nameWithType>
- [<span data-ttu-id="ce8f6-120">工作流跟踪</span><span class="sxs-lookup"><span data-stu-id="ce8f6-120">Workflow Tracking and Tracing</span></span>](../../../windows-workflow-foundation/workflow-tracking-and-tracing.md)
- [<span data-ttu-id="ce8f6-121">跟踪配置文件</span><span class="sxs-lookup"><span data-stu-id="ce8f6-121">Tracking Profiles</span></span>](../../../windows-workflow-foundation/tracking-profiles.md)
