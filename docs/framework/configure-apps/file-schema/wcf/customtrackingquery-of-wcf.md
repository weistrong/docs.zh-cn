---
description: 了解有关 WCF 的详细信息： <customTrackingQuery>
title: <customTrackingQuery> WCF 的
ms.date: 03/30/2017
ms.assetid: 164446ae-8440-4b67-b217-6786cfae1e01
ms.openlocfilehash: 3eac26ee94a95b480d743e3c6ec554a84b8747a3
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99754454"
---
# <a name="customtrackingquery-of-wcf"></a><span data-ttu-id="bc99b-103">\<customTrackingQuery> WCF 的</span><span class="sxs-lookup"><span data-stu-id="bc99b-103">\<customTrackingQuery> of WCF</span></span>

<span data-ttu-id="bc99b-104">表示一个查询，该查询用于跟踪您在代码活动中定义的事件。</span><span class="sxs-lookup"><span data-stu-id="bc99b-104">Represents a query that is used to track events that you define in your code activities.</span></span> <span data-ttu-id="bc99b-105">跟踪参与者需要用此查询来订阅自定义跟踪记录。</span><span class="sxs-lookup"><span data-stu-id="bc99b-105">The query is necessary for a tracking participant to subscribe to custom tracking records.</span></span>

<span data-ttu-id="bc99b-106">有关跟踪配置文件查询的详细信息，请参阅 [跟踪配置文件](../../../windows-workflow-foundation/tracking-profiles.md)</span><span class="sxs-lookup"><span data-stu-id="bc99b-106">For more information on tracking profile queries, see [Tracking Profiles](../../../windows-workflow-foundation/tracking-profiles.md)</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<tracking>**](tracking-of-wcf.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<profiles>**\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<trackingProfile>**](trackingprofile-of-wcf.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<workflow>**](workflow-of-wcf.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<customTrackingQueries>**](customtrackingqueries-of-wcf.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<customTrackingQuery>**  
  
## <a name="syntax"></a><span data-ttu-id="bc99b-107">语法</span><span class="sxs-lookup"><span data-stu-id="bc99b-107">Syntax</span></span>  
  
```xml  
<tracking>
  <profiles>
    <trackingProfile name="Name">
      <workflow>
        <customTrackingQueries>
          <customTrackingQuery activityName="String"
                               name="String"/>
        </customTrackingQueries>
      </workflow>
    </trackingProfile>
  </profiles>
</tracking>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="bc99b-108">特性和元素</span><span class="sxs-lookup"><span data-stu-id="bc99b-108">Attributes and elements</span></span>  

<span data-ttu-id="bc99b-109">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="bc99b-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="bc99b-110">特性</span><span class="sxs-lookup"><span data-stu-id="bc99b-110">Attributes</span></span>  
  
|<span data-ttu-id="bc99b-111">属性</span><span class="sxs-lookup"><span data-stu-id="bc99b-111">Attribute</span></span>|<span data-ttu-id="bc99b-112">说明</span><span class="sxs-lookup"><span data-stu-id="bc99b-112">Description</span></span>|  
|---------------|-----------------|  
|`activityName`|<span data-ttu-id="bc99b-113">一个字符串，指定生成跟踪记录的活动的名称。</span><span class="sxs-lookup"><span data-stu-id="bc99b-113">A string that specifies the name of the activity that generated the tracking record.</span></span>|  
|`name`|<span data-ttu-id="bc99b-114">一个字符串，指定发出的自定义跟踪记录的名称。</span><span class="sxs-lookup"><span data-stu-id="bc99b-114">A string that specifies the name of the custom tracking record that is emitted.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="bc99b-115">子元素</span><span class="sxs-lookup"><span data-stu-id="bc99b-115">Child elements</span></span>

<span data-ttu-id="bc99b-116">无。</span><span class="sxs-lookup"><span data-stu-id="bc99b-116">None.</span></span>

### <a name="parent-elements"></a><span data-ttu-id="bc99b-117">父元素</span><span class="sxs-lookup"><span data-stu-id="bc99b-117">Parent elements</span></span>

|<span data-ttu-id="bc99b-118">元素</span><span class="sxs-lookup"><span data-stu-id="bc99b-118">Element</span></span>|<span data-ttu-id="bc99b-119">说明</span><span class="sxs-lookup"><span data-stu-id="bc99b-119">Description</span></span>|  
|-------------|-----------------|  
|[\<customTrackingQueries>](customtrackingqueries-of-wcf.md)|<span data-ttu-id="bc99b-120">表示一个查询集合，这些查询用于跟踪你在代码活动中定义的事件。</span><span class="sxs-lookup"><span data-stu-id="bc99b-120">Represents a collection of queries that are used to track events that you define in your code activities.</span></span>|
  
## <a name="see-also"></a><span data-ttu-id="bc99b-121">请参阅</span><span class="sxs-lookup"><span data-stu-id="bc99b-121">See also</span></span>

- <xref:System.ServiceModel.Activities.Tracking.Configuration.CustomTrackingQueryElementCollection?displayProperty=nameWithType>
- <xref:System.Activities.Tracking.CustomTrackingQuery?displayProperty=nameWithType>
- [<span data-ttu-id="bc99b-122">工作流跟踪</span><span class="sxs-lookup"><span data-stu-id="bc99b-122">Workflow Tracking and Tracing</span></span>](../../../windows-workflow-foundation/workflow-tracking-and-tracing.md)
- [<span data-ttu-id="bc99b-123">跟踪配置文件</span><span class="sxs-lookup"><span data-stu-id="bc99b-123">Tracking Profiles</span></span>](../../../windows-workflow-foundation/tracking-profiles.md)
