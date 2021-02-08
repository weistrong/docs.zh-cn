---
description: 了解详细信息： <customTrackingQuery>
title: <customTrackingQuery>
ms.date: 03/30/2017
ms.topic: reference
ms.assetid: 4e108e89-1132-46b7-868a-c7f5c69dc89f
ms.openlocfilehash: 24857aca39aad825a3dd4eca83fa3a51ec440b25
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99795087"
---
# \<customTrackingQuery>

<span data-ttu-id="4276a-102">表示一个查询集合，这些查询用于跟踪你在代码活动中定义的事件。</span><span class="sxs-lookup"><span data-stu-id="4276a-102">Represents a collection of queries that are used to track events that you define in your code activities.</span></span> <span data-ttu-id="4276a-103">跟踪参与者需要用此查询来订阅自定义跟踪记录。</span><span class="sxs-lookup"><span data-stu-id="4276a-103">The query is necessary for a tracking participant to subscribe to custom tracking records.</span></span>  
  
 <span data-ttu-id="4276a-104">有关跟踪配置文件查询的详细信息，请参阅 [跟踪配置文件](../../../windows-workflow-foundation/tracking-profiles.md)</span><span class="sxs-lookup"><span data-stu-id="4276a-104">For more information on tracking profile queries, see [Tracking Profiles](../../../windows-workflow-foundation/tracking-profiles.md)</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.ServiceModel>**](system-servicemodel-of-workflow.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<tracking>**](tracking.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<trackingProfile>**](trackingprofile.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<workflow>**](workflow.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<customTrackingQueries>**](customtrackingqueries.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<customTrackingQuery>**  
  
## <a name="syntax"></a><span data-ttu-id="4276a-105">语法</span><span class="sxs-lookup"><span data-stu-id="4276a-105">Syntax</span></span>  
  
```xml  
<tracking>
  <trackingProfile name="Name">
    <workflow>
      <customTrackingQueries>
        <customTrackingQuery activityName="String"
                             name="String" />
      </customTrackingQueries>
    </workflow>
 </trackingProfile>
</tracking>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="4276a-106">特性和元素</span><span class="sxs-lookup"><span data-stu-id="4276a-106">Attributes and Elements</span></span>  

 <span data-ttu-id="4276a-107">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="4276a-107">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="4276a-108">特性</span><span class="sxs-lookup"><span data-stu-id="4276a-108">Attributes</span></span>  
  
|<span data-ttu-id="4276a-109">属性</span><span class="sxs-lookup"><span data-stu-id="4276a-109">Attribute</span></span>|<span data-ttu-id="4276a-110">说明</span><span class="sxs-lookup"><span data-stu-id="4276a-110">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="4276a-111">activityName</span><span class="sxs-lookup"><span data-stu-id="4276a-111">activityName</span></span>|<span data-ttu-id="4276a-112">一个字符串，指定生成跟踪记录的活动的名称。</span><span class="sxs-lookup"><span data-stu-id="4276a-112">A string that specifies the name of the activity that generated the tracking record.</span></span>|  
|<span data-ttu-id="4276a-113">name</span><span class="sxs-lookup"><span data-stu-id="4276a-113">name</span></span>|<span data-ttu-id="4276a-114">一个字符串，指定发出的自定义跟踪记录的名称。</span><span class="sxs-lookup"><span data-stu-id="4276a-114">A string that specifies the name of the custom tracking record that is emitted.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="4276a-115">子元素</span><span class="sxs-lookup"><span data-stu-id="4276a-115">Child Elements</span></span>  

 <span data-ttu-id="4276a-116">无。</span><span class="sxs-lookup"><span data-stu-id="4276a-116">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="4276a-117">父元素</span><span class="sxs-lookup"><span data-stu-id="4276a-117">Parent Elements</span></span>  
  
|<span data-ttu-id="4276a-118">元素</span><span class="sxs-lookup"><span data-stu-id="4276a-118">Element</span></span>|<span data-ttu-id="4276a-119">说明</span><span class="sxs-lookup"><span data-stu-id="4276a-119">Description</span></span>|  
|-------------|-----------------|  
|[\<customTrackingQuery>](customtrackingquery.md)|<span data-ttu-id="4276a-120">一个查询，用于跟踪你在代码活动中定义的事件。</span><span class="sxs-lookup"><span data-stu-id="4276a-120">A query that is used to track events that you define in your code activities.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="4276a-121">请参阅</span><span class="sxs-lookup"><span data-stu-id="4276a-121">See also</span></span>

- <xref:System.ServiceModel.Activities.Tracking.Configuration.CustomTrackingQueryElementCollection?displayProperty=nameWithType>
- <xref:System.Activities.Tracking.CustomTrackingQuery?displayProperty=nameWithType>
- [<span data-ttu-id="4276a-122">工作流跟踪</span><span class="sxs-lookup"><span data-stu-id="4276a-122">Workflow Tracking and Tracing</span></span>](../../../windows-workflow-foundation/workflow-tracking-and-tracing.md)
- [<span data-ttu-id="4276a-123">跟踪配置文件</span><span class="sxs-lookup"><span data-stu-id="4276a-123">Tracking Profiles</span></span>](../../../windows-workflow-foundation/tracking-profiles.md)
