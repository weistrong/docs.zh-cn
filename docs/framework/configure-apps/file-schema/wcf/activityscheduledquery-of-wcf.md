---
description: 了解有关 WCF 的详细信息： <activityScheduledQuery>
title: <activityScheduledQuery> WCF 的
ms.date: 03/30/2017
ms.assetid: 25f6eee1-3d98-4c39-b517-c0813f03f106
ms.openlocfilehash: b1b5f971dccfbc650ee12a08a9ae2fa7b745db50
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99802354"
---
# <a name="activityscheduledquery-of-wcf"></a><span data-ttu-id="beef1-103">\<activityScheduledQuery> WCF 的</span><span class="sxs-lookup"><span data-stu-id="beef1-103">\<activityScheduledQuery> of WCF</span></span>

<span data-ttu-id="beef1-104">表示一个查询集合，这些查询用于跟踪安排给父活动来执行的活动。</span><span class="sxs-lookup"><span data-stu-id="beef1-104">Represents a collection of queries that are used to track an activity scheduled for execution by a parent activity.</span></span> <span data-ttu-id="beef1-105">跟踪参与者需要用此查询来订阅活动安排记录。</span><span class="sxs-lookup"><span data-stu-id="beef1-105">The query is necessary for a tracking participant to subscribe to activity scheduled records.</span></span>  
  
<span data-ttu-id="beef1-106">有关跟踪配置文件查询的详细信息，请参阅 [跟踪配置文件](../../../windows-workflow-foundation/tracking-profiles.md)</span><span class="sxs-lookup"><span data-stu-id="beef1-106">For more information on tracking profile queries, see [Tracking Profiles](../../../windows-workflow-foundation/tracking-profiles.md)</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<tracking>**](tracking-of-wcf.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<profiles>**\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<trackingProfile>**](trackingprofile-of-wcf.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<workflow>**](workflow-of-wcf.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<activityScheduledQueries>**](activityscheduledqueries-of-wcf.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<activityScheduledQuery>**  
  
## <a name="syntax"></a><span data-ttu-id="beef1-107">语法</span><span class="sxs-lookup"><span data-stu-id="beef1-107">Syntax</span></span>  
  
```xml  
<tracking>
  <profiles>
    <trackingProfile name="Name">
      <workflow>
        <activityScheduledQueries>
          <activityScheduledQuery activityName="String"
                                  childActivityName="String" />
        </activityScheduledQueries>
      </workflow>
    </trackingProfile>
  </profiles>
</tracking>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="beef1-108">特性和元素</span><span class="sxs-lookup"><span data-stu-id="beef1-108">Attributes and elements</span></span>  

<span data-ttu-id="beef1-109">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="beef1-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="beef1-110">特性</span><span class="sxs-lookup"><span data-stu-id="beef1-110">Attributes</span></span>  
  
|<span data-ttu-id="beef1-111">属性</span><span class="sxs-lookup"><span data-stu-id="beef1-111">Attribute</span></span>|<span data-ttu-id="beef1-112">说明</span><span class="sxs-lookup"><span data-stu-id="beef1-112">Description</span></span>|  
|---------------|-----------------|  
|`activityName`|<span data-ttu-id="beef1-113">一个字符串，指定正在请求取消的活动的名称。</span><span class="sxs-lookup"><span data-stu-id="beef1-113">A string that specifies the name of the activity that is requesting the cancellation.</span></span>|  
|`childActivityName`|<span data-ttu-id="beef1-114">一个字符串，指定已请求将其取消的子活动的名称。</span><span class="sxs-lookup"><span data-stu-id="beef1-114">A string that specifies the name of the child activity for which cancellation was requested.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="beef1-115">子元素</span><span class="sxs-lookup"><span data-stu-id="beef1-115">Child elements</span></span>

<span data-ttu-id="beef1-116">无。</span><span class="sxs-lookup"><span data-stu-id="beef1-116">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="beef1-117">父元素</span><span class="sxs-lookup"><span data-stu-id="beef1-117">Parent elements</span></span>  
  
|<span data-ttu-id="beef1-118">元素</span><span class="sxs-lookup"><span data-stu-id="beef1-118">Element</span></span>|<span data-ttu-id="beef1-119">说明</span><span class="sxs-lookup"><span data-stu-id="beef1-119">Description</span></span>|  
|-------------|-----------------|  
|[\<activityScheduledQueries>](activityscheduledqueries-of-wcf.md)|<span data-ttu-id="beef1-120">查询的集合，这些查询用于跟踪计划的父活动执行的活动。</span><span class="sxs-lookup"><span data-stu-id="beef1-120">A collection of queries that are used to track an activity scheduled for execution by a parent activity.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="beef1-121">请参阅</span><span class="sxs-lookup"><span data-stu-id="beef1-121">See also</span></span>

- <xref:System.ServiceModel.Activities.Tracking.Configuration.ActivityScheduledQueryElement>
- <xref:System.Activities.Tracking.ActivityScheduledQuery>
- [<span data-ttu-id="beef1-122">工作流跟踪</span><span class="sxs-lookup"><span data-stu-id="beef1-122">Workflow Tracking and Tracing</span></span>](../../../windows-workflow-foundation/workflow-tracking-and-tracing.md)
- [<span data-ttu-id="beef1-123">跟踪配置文件</span><span class="sxs-lookup"><span data-stu-id="beef1-123">Tracking Profiles</span></span>](../../../windows-workflow-foundation/tracking-profiles.md)
