---
description: 了解详细信息： <activityScheduledQuery>
title: <activityScheduledQuery>
ms.date: 03/30/2017
ms.topic: reference
ms.assetid: a8bcd6d4-b389-4daf-86bf-1ade85fec114
ms.openlocfilehash: 72aa9c2d3480488d4468d008fa8a4306929c190d
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99802107"
---
# \<activityScheduledQuery>

<span data-ttu-id="5472c-102">表示一个查询集合，这些查询用于跟踪安排给父活动来执行的活动。</span><span class="sxs-lookup"><span data-stu-id="5472c-102">Represents a collection of queries that are used to track an activity scheduled for execution by a parent activity.</span></span> <span data-ttu-id="5472c-103">跟踪参与者需要用此查询来订阅活动安排记录。</span><span class="sxs-lookup"><span data-stu-id="5472c-103">The query is necessary for a tracking participant to subscribe to activity scheduled records.</span></span>  
  
 <span data-ttu-id="5472c-104">有关跟踪配置文件查询的详细信息，请参阅 [跟踪配置文件](../../../windows-workflow-foundation/tracking-profiles.md)</span><span class="sxs-lookup"><span data-stu-id="5472c-104">For more information on tracking profile queries, see [Tracking Profiles](../../../windows-workflow-foundation/tracking-profiles.md)</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.ServiceModel>**](system-servicemodel-of-workflow.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<tracking>**](tracking.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<trackingProfile>**](trackingprofile.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<workflow>**](workflow.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<activityScheduledQueries>**](activityscheduledqueries.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<activityScheduledQuery>**  
  
## <a name="syntax"></a><span data-ttu-id="5472c-105">语法</span><span class="sxs-lookup"><span data-stu-id="5472c-105">Syntax</span></span>  
  
```xml
<tracking>
  <trackingProfile name="Name">
    <workflow>
      <activityScheduledQueries>
        <activityScheduledQuery activityName="String"
                                childActivityName="String"/>
      </activityScheduledQueries>
    </workflow>
  </trackingProfile>
</tracking>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="5472c-106">特性和元素</span><span class="sxs-lookup"><span data-stu-id="5472c-106">Attributes and Elements</span></span>  

 <span data-ttu-id="5472c-107">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="5472c-107">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="5472c-108">特性</span><span class="sxs-lookup"><span data-stu-id="5472c-108">Attributes</span></span>  
  
|<span data-ttu-id="5472c-109">属性</span><span class="sxs-lookup"><span data-stu-id="5472c-109">Attribute</span></span>|<span data-ttu-id="5472c-110">说明</span><span class="sxs-lookup"><span data-stu-id="5472c-110">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="5472c-111">activityName</span><span class="sxs-lookup"><span data-stu-id="5472c-111">activityName</span></span>|<span data-ttu-id="5472c-112">一个字符串，指定正在请求取消的活动的名称。</span><span class="sxs-lookup"><span data-stu-id="5472c-112">A string that specifies the name of the activity that is requesting the cancellation.</span></span>|  
|<span data-ttu-id="5472c-113">childActivityName</span><span class="sxs-lookup"><span data-stu-id="5472c-113">childActivityName</span></span>|<span data-ttu-id="5472c-114">一个字符串，指定已请求将其取消的子活动的名称。</span><span class="sxs-lookup"><span data-stu-id="5472c-114">A string that specifies the name of the child activity for which cancellation was requested.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="5472c-115">子元素</span><span class="sxs-lookup"><span data-stu-id="5472c-115">Child Elements</span></span>  

 <span data-ttu-id="5472c-116">无。</span><span class="sxs-lookup"><span data-stu-id="5472c-116">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="5472c-117">父元素</span><span class="sxs-lookup"><span data-stu-id="5472c-117">Parent Elements</span></span>  
  
|<span data-ttu-id="5472c-118">元素</span><span class="sxs-lookup"><span data-stu-id="5472c-118">Element</span></span>|<span data-ttu-id="5472c-119">说明</span><span class="sxs-lookup"><span data-stu-id="5472c-119">Description</span></span>|  
|-------------|-----------------|  
|[\<activityScheduledQuery>](activityscheduledquery.md)|<span data-ttu-id="5472c-120">一个查询，用于跟踪安排给父活动来执行的活动。</span><span class="sxs-lookup"><span data-stu-id="5472c-120">A query that is used to track an activity scheduled for execution by a parent activity.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="5472c-121">请参阅</span><span class="sxs-lookup"><span data-stu-id="5472c-121">See also</span></span>

- <xref:System.ServiceModel.Activities.Tracking.Configuration.ActivityScheduledQueryElement?displayProperty=nameWithType>
- <xref:System.Activities.Tracking.ActivityScheduledQuery?displayProperty=nameWithType>
- [<span data-ttu-id="5472c-122">工作流跟踪</span><span class="sxs-lookup"><span data-stu-id="5472c-122">Workflow Tracking and Tracing</span></span>](../../../windows-workflow-foundation/workflow-tracking-and-tracing.md)
- [<span data-ttu-id="5472c-123">跟踪配置文件</span><span class="sxs-lookup"><span data-stu-id="5472c-123">Tracking Profiles</span></span>](../../../windows-workflow-foundation/tracking-profiles.md)
