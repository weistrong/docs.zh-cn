---
description: 了解有关 WCF 的详细信息： <activityScheduledQueries>
title: <activityScheduledQueries> WCF 的
ms.date: 03/30/2017
ms.assetid: e351329f-9676-4f11-9b19-f4bac82f36fc
ms.openlocfilehash: b92bb2827b4c8bce43e4ee0b8dc03c7be124e3da
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99782242"
---
# <a name="activityscheduledqueries-of-wcf"></a><span data-ttu-id="93d9e-103">\<activityScheduledQueries> WCF 的</span><span class="sxs-lookup"><span data-stu-id="93d9e-103">\<activityScheduledQueries> of WCF</span></span>

<span data-ttu-id="93d9e-104">表示一个查询集合，这些查询用于跟踪安排给父活动来执行的活动。</span><span class="sxs-lookup"><span data-stu-id="93d9e-104">Represents a collection of queries that are used to track an activity scheduled for execution by a parent activity.</span></span> <span data-ttu-id="93d9e-105">跟踪参与者需要用此查询来订阅活动安排记录。</span><span class="sxs-lookup"><span data-stu-id="93d9e-105">The query is necessary for a tracking participant to subscribe to activity scheduled records.</span></span>  
  
<span data-ttu-id="93d9e-106">有关跟踪配置文件查询的详细信息，请参阅 [跟踪配置文件](../../../windows-workflow-foundation/tracking-profiles.md)</span><span class="sxs-lookup"><span data-stu-id="93d9e-106">For more information on tracking profile queries, see [Tracking Profiles](../../../windows-workflow-foundation/tracking-profiles.md)</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<tracking>**](tracking-of-wcf.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<profiles>**\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<trackingProfile>**](trackingprofile-of-wcf.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<workflow>**](workflow-of-wcf.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<activityScheduledQueries>**  
  
## <a name="syntax"></a><span data-ttu-id="93d9e-107">语法</span><span class="sxs-lookup"><span data-stu-id="93d9e-107">Syntax</span></span>  
  
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
  
## <a name="attributes-and-elements"></a><span data-ttu-id="93d9e-108">特性和元素</span><span class="sxs-lookup"><span data-stu-id="93d9e-108">Attributes and elements</span></span>  

<span data-ttu-id="93d9e-109">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="93d9e-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="93d9e-110">特性</span><span class="sxs-lookup"><span data-stu-id="93d9e-110">Attributes</span></span>  

<span data-ttu-id="93d9e-111">无。</span><span class="sxs-lookup"><span data-stu-id="93d9e-111">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="93d9e-112">子元素</span><span class="sxs-lookup"><span data-stu-id="93d9e-112">Child elements</span></span>  
  
|<span data-ttu-id="93d9e-113">元素</span><span class="sxs-lookup"><span data-stu-id="93d9e-113">Element</span></span>|<span data-ttu-id="93d9e-114">说明</span><span class="sxs-lookup"><span data-stu-id="93d9e-114">Description</span></span>|  
|-------------|-----------------|  
|[\<activityScheduledQuery>](activityscheduledquery-of-wcf.md)|<span data-ttu-id="93d9e-115">一个查询，用于跟踪安排给父活动来执行的活动。</span><span class="sxs-lookup"><span data-stu-id="93d9e-115">A query that is used to track an activity scheduled for execution by a parent activity.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="93d9e-116">父元素</span><span class="sxs-lookup"><span data-stu-id="93d9e-116">Parent elements</span></span>  
  
|<span data-ttu-id="93d9e-117">元素</span><span class="sxs-lookup"><span data-stu-id="93d9e-117">Element</span></span>|<span data-ttu-id="93d9e-118">说明</span><span class="sxs-lookup"><span data-stu-id="93d9e-118">Description</span></span>|  
|-------------|-----------------|  
|[\<workflow>](../windows-workflow-foundation/workflow.md)|<span data-ttu-id="93d9e-119">一个配置元素，包含 `activityDefinitionId` 属性所标识的特定工作流的所有查询。</span><span class="sxs-lookup"><span data-stu-id="93d9e-119">A configuration element that contains all queries for a specific workflow identified by the `activityDefinitionId` property.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="93d9e-120">请参阅</span><span class="sxs-lookup"><span data-stu-id="93d9e-120">See also</span></span>

- <xref:System.ServiceModel.Activities.Tracking.Configuration.ActivityScheduledQueryElementCollection>
- <xref:System.Activities.Tracking.ActivityScheduledQuery>
- [<span data-ttu-id="93d9e-121">工作流跟踪</span><span class="sxs-lookup"><span data-stu-id="93d9e-121">Workflow Tracking and Tracing</span></span>](../../../windows-workflow-foundation/workflow-tracking-and-tracing.md)
- [<span data-ttu-id="93d9e-122">跟踪配置文件</span><span class="sxs-lookup"><span data-stu-id="93d9e-122">Tracking Profiles</span></span>](../../../windows-workflow-foundation/tracking-profiles.md)
