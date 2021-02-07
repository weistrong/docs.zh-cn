---
description: 了解详细信息： <workflow>
title: <workflow>
ms.date: 03/30/2017
ms.topic: reference
ms.assetid: 560aa9b6-9cf3-460e-b798-f87d14b1d2de
ms.openlocfilehash: 2d35f03c2715fcba7cf868a3550855066d747d82
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99697967"
---
# \<workflow>

<span data-ttu-id="5427c-102">一个配置元素，包含 <xref:System.ServiceModel.Activities.Tracking.Configuration.ProfileWorkflowElement.ActivityDefinitionId?displayProperty=nameWithType> 属性所标识的特定工作流的所有查询。</span><span class="sxs-lookup"><span data-stu-id="5427c-102">A configuration element that contains all queries for a specific workflow identified by the <xref:System.ServiceModel.Activities.Tracking.Configuration.ProfileWorkflowElement.ActivityDefinitionId?displayProperty=nameWithType> property.</span></span>  
  
 <span data-ttu-id="5427c-103">有关工作流跟踪及其配置的详细信息，请参阅 [工作流跟踪和跟踪](../../../windows-workflow-foundation/workflow-tracking-and-tracing.md) 和 [跟踪配置文件](../../../windows-workflow-foundation/tracking-profiles.md)。</span><span class="sxs-lookup"><span data-stu-id="5427c-103">For more information in workflow tracking and its configuration, see [Workflow Tracking and Tracing](../../../windows-workflow-foundation/workflow-tracking-and-tracing.md) and [Tracking Profiles](../../../windows-workflow-foundation/tracking-profiles.md).</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.ServiceModel>**](system-servicemodel-of-workflow.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<tracking>**](tracking.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<trackingProfile>**](trackingprofile.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<workflow>**  
  
## <a name="syntax"></a><span data-ttu-id="5427c-104">语法</span><span class="sxs-lookup"><span data-stu-id="5427c-104">Syntax</span></span>  
  
```xml  
<system.serviceModel>
  <tracking>
    <profiles>
      <participants>
        <add name="String"
             profileName="String"
             type="String" />
      </participants>
      <trackingProfile name="String">
        <workflow activityDefinitionId="String">
          <activityScheduledQueries>
            <activityScheduledQuery activityName="String"
                                    childActivityName="String"/>
          </activityScheduledQueries>
          <activityStateQueries>
            <activityStateQuery activityName="String" />
            <arguments>
              <argument name="String" />
            </arguments>
            <states>
              <state name="String"  />
            </states>
            <variables>
              <variable name="String" />
            </variables>
          </activityStateQueries>
          <bookmarkResumptionQueries>
            <bookmarkResumptionQuery name="String" />
          </bookmarkResumptionQueries>
          <cancelRequestQueries>
            <cancelRequestQuery activityName="String"
                                childActivityName="String"/>
          </cancelRequestQueries>
          <customTrackingQueries>
            <customTrackingQuery activityName="String"
                                 name="String"/>
          </customTrackingQueries>
          <faultPropagationQueries>
            <faultPropagationQuery activityName="String"
                                   faultHandlerActivityName="String" />
          </faultPropagationQueries>
          <workflowInstanceQueries>
            <workflowInstanceQuery>
              <states>
                <state name="String" />
              </states>
            </workflowInstanceQuery>
          </workflowInstanceQueries>
        </workflow>
      </trackingProfile>
    </profiles>
  </tracking>
</system.serviceModel>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="5427c-105">特性和元素</span><span class="sxs-lookup"><span data-stu-id="5427c-105">Attributes and Elements</span></span>  

 <span data-ttu-id="5427c-106">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="5427c-106">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="5427c-107">特性</span><span class="sxs-lookup"><span data-stu-id="5427c-107">Attributes</span></span>  
  
|<span data-ttu-id="5427c-108">属性</span><span class="sxs-lookup"><span data-stu-id="5427c-108">Attribute</span></span>|<span data-ttu-id="5427c-109">说明</span><span class="sxs-lookup"><span data-stu-id="5427c-109">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="5427c-110">activityDefinitionId</span><span class="sxs-lookup"><span data-stu-id="5427c-110">activityDefinitionId</span></span>|<span data-ttu-id="5427c-111">一个字符串，指定所跟踪的工作流的活动定义 ID。</span><span class="sxs-lookup"><span data-stu-id="5427c-111">A string that specifies the activity definition ID of the workflow being tracked.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="5427c-112">子元素</span><span class="sxs-lookup"><span data-stu-id="5427c-112">Child Elements</span></span>  
  
|<span data-ttu-id="5427c-113">元素</span><span class="sxs-lookup"><span data-stu-id="5427c-113">Element</span></span>|<span data-ttu-id="5427c-114">说明</span><span class="sxs-lookup"><span data-stu-id="5427c-114">Description</span></span>|  
|-------------|-----------------|  
|[\<activityScheduledQueries>](activityscheduledqueries.md)|<span data-ttu-id="5427c-115">表示一个查询集合，这些查询用于跟踪安排给父活动来执行的活动。</span><span class="sxs-lookup"><span data-stu-id="5427c-115">Represents a collection of queries that are used to track an activity scheduled for execution by a parent activity.</span></span> <span data-ttu-id="5427c-116">跟踪参与者需要用此查询来订阅活动安排记录。</span><span class="sxs-lookup"><span data-stu-id="5427c-116">The query is necessary for a tracking participant to subscribe to activity scheduled records.</span></span>|  
|[\<activityStateQueries>](activitystatequeries.md)|<span data-ttu-id="5427c-117">表示一个查询集合，这些查询用于跟踪构成工作流实例的活动的生命周期更改。</span><span class="sxs-lookup"><span data-stu-id="5427c-117">Represents a collection of queries that are used to track life cycle changes of the activities that make up a workflow instance.</span></span> <span data-ttu-id="5427c-118">例如，你可能想要跟踪每次在工作流实例中完成 "发送电子邮件" 活动的时间。</span><span class="sxs-lookup"><span data-stu-id="5427c-118">For example, you may want to keep track of every time the "Send E-Mail" activity completes within a workflow instance.</span></span> <span data-ttu-id="5427c-119">跟踪参与者需要用此查询来订阅活动状态记录对象。</span><span class="sxs-lookup"><span data-stu-id="5427c-119">This query is necessary for a tracking participant to subscribe to activity state record objects.</span></span> <span data-ttu-id="5427c-120">在 ActivityStates 中指定了要订阅的可用状态。</span><span class="sxs-lookup"><span data-stu-id="5427c-120">The available states to subscribe to are specified in ActivityStates.</span></span>|  
|[\<bookmarkResumptionQueries>](bookmarkresumptionqueries.md)|<span data-ttu-id="5427c-121">表示一个查询集合，这些查询用于跟踪工作流实例中的书签恢复。</span><span class="sxs-lookup"><span data-stu-id="5427c-121">Represents a collection of queries that are used to track resumption of a bookmark within a workflow instance.</span></span> <span data-ttu-id="5427c-122">跟踪参与者需要用此查询来订阅书签恢复记录。</span><span class="sxs-lookup"><span data-stu-id="5427c-122">The query is necessary for a tracking participant to subscribe to bookmark resumption records.</span></span>|  
|[\<cancelRequestedQueries>](cancelrequestedqueries.md)|<span data-ttu-id="5427c-123">表示一个查询集合，这些查询用于跟踪父活动取消子活动的请求。</span><span class="sxs-lookup"><span data-stu-id="5427c-123">Represents a collection of queries that are used to track requests to cancel a child activity by the parent activity.</span></span> <span data-ttu-id="5427c-124">跟踪参与者需要用此查询来订阅取消请求记录对象。</span><span class="sxs-lookup"><span data-stu-id="5427c-124">The query is necessary for a tracking participant to subscribe to cancel request record objects.</span></span>|  
|[\<customTrackingQueries>](customtrackingqueries.md)|<span data-ttu-id="5427c-125">表示一个查询集合，这些查询用于跟踪你在代码活动中定义的事件。</span><span class="sxs-lookup"><span data-stu-id="5427c-125">Represents a collection of queries that are used to track events that you define in your code activities.</span></span> <span data-ttu-id="5427c-126">跟踪参与者需要用此查询来订阅自定义跟踪记录。</span><span class="sxs-lookup"><span data-stu-id="5427c-126">The query is necessary for a tracking participant to subscribe to custom tracking records.</span></span>|  
|[\<faultPropagationQueries>](faultpropagationqueries.md)|<span data-ttu-id="5427c-127">表示一个查询集合，这些查询用于跟踪在某个活动中发生的错误的处理。</span><span class="sxs-lookup"><span data-stu-id="5427c-127">Represents a collection of queries that are used to track the handling of faults that occur within an activity.</span></span>  <span data-ttu-id="5427c-128">每次 FaultHandler 处理错误时，都会发生此事件。</span><span class="sxs-lookup"><span data-stu-id="5427c-128">This event occurs each time a FaultHandler processes a fault.</span></span> <span data-ttu-id="5427c-129">应使用此类查询来跟踪对在活动中出现的错误进行的处理。</span><span class="sxs-lookup"><span data-stu-id="5427c-129">You should use such query to track the handling of faults that occur within an activity.</span></span> <span data-ttu-id="5427c-130">跟踪参与者需要用此查询来订阅错误传播记录。</span><span class="sxs-lookup"><span data-stu-id="5427c-130">The query is necessary for a  tracking participant to subscribe to fault propagation records.</span></span>|  
|[\<workflowInstanceQueries>](workflowinstancequeries.md)|<span data-ttu-id="5427c-131">表示配置元素的集合，这些配置元素跟踪工作流实例生命周期的更改，例如已开始或已完成的事件。</span><span class="sxs-lookup"><span data-stu-id="5427c-131">Represents a collection of configuration elements that track workflow instance life cycle changes such as a started or completed event.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="5427c-132">父元素</span><span class="sxs-lookup"><span data-stu-id="5427c-132">Parent Elements</span></span>  
  
|<span data-ttu-id="5427c-133">元素</span><span class="sxs-lookup"><span data-stu-id="5427c-133">Element</span></span>|<span data-ttu-id="5427c-134">说明</span><span class="sxs-lookup"><span data-stu-id="5427c-134">Description</span></span>|  
|-------------|-----------------|  
|[\<trackingProfile>](trackingprofile.md)|<span data-ttu-id="5427c-135">表示一个配置节，用于创建对跟踪参与者中的工作流跟踪记录的订阅。</span><span class="sxs-lookup"><span data-stu-id="5427c-135">Represents a configuration section for creating a subscription to workflow tracking records in a tracking participant.</span></span> <span data-ttu-id="5427c-136">跟踪配置文件包含跟踪查询，这些查询允许跟踪参与者订阅当工作流实例的状态在运行时发生更改时发出的工作流事件。</span><span class="sxs-lookup"><span data-stu-id="5427c-136">A tracking profile contains tracking queries that permit a tracking participant to subscribe to workflow events that are emitted when the state of a workflow instance changes at runtime.</span></span> <span data-ttu-id="5427c-137">跟踪配置文件节中定义的查询用于定义订阅返回的事件类型。</span><span class="sxs-lookup"><span data-stu-id="5427c-137">The queries defined within the tracking profile section define the kinds of events that are returned by the subscription.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="5427c-138">备注</span><span class="sxs-lookup"><span data-stu-id="5427c-138">Remarks</span></span>  

 <span data-ttu-id="5427c-139">跟踪配置文件包含跟踪查询，这些查询允许跟踪参与者订阅当特定工作流实例的状态在运行时发生更改时发出的工作流事件。</span><span class="sxs-lookup"><span data-stu-id="5427c-139">Tracking profiles contains tracking queries that permit a tracking participant to subscribe to workflow events that are emitted when the state of a particular workflow instance changes at runtime.</span></span> <span data-ttu-id="5427c-140">所跟踪的工作流实例由此配置元素来标识。</span><span class="sxs-lookup"><span data-stu-id="5427c-140">The workflow instance being tracked is identified by this configuration element.</span></span>  
  
 <span data-ttu-id="5427c-141">根据您的监视需求，可以编写一个非常粗陋的配置文件，用来订阅对工作流进行的一小组高级状态更改。</span><span class="sxs-lookup"><span data-stu-id="5427c-141">Depending on your monitoring requirements you may write a profile that is very coarse, which subscribes to a small set of high-level state changes on a workflow.</span></span> <span data-ttu-id="5427c-142">相反，也可以创建一个非常具体的配置文件，其生成的事件足够丰富，可在以后重新构造详细的执行流。</span><span class="sxs-lookup"><span data-stu-id="5427c-142">Conversely, you may create a very specific profile whose resulting events are rich enough to reconstruct a detailed execution flow later.</span></span>  
  
 <span data-ttu-id="5427c-143">跟踪配置文件组织为跟踪记录的声明性订阅，利用这些订阅可以查询特定跟踪记录的工作流运行时。</span><span class="sxs-lookup"><span data-stu-id="5427c-143">Tracking profiles are structured as declarative subscriptions for tracking records that allow you to query the workflow runtime for specific tracking records.</span></span> <span data-ttu-id="5427c-144">查询类型有多种，可用于订阅跟踪记录的不同类。</span><span class="sxs-lookup"><span data-stu-id="5427c-144">There are a handful of query types that allow you subscribe to different classes of tracking records.</span></span> <span data-ttu-id="5427c-145">有关查询的完整列表，请参阅本主题的子元素列表和 [跟踪配置文件](../../../windows-workflow-foundation/tracking-profiles.md)。</span><span class="sxs-lookup"><span data-stu-id="5427c-145">For a complete list of queries, see the child element list of this topic and [Tracking Profiles](../../../windows-workflow-foundation/tracking-profiles.md).</span></span>  
  
 <span data-ttu-id="5427c-146">下面的示例演示配置文件中的跟踪配置文件，该配置文件允许跟踪参与者订阅 `Started` 和 `Completed` 工作流事件。</span><span class="sxs-lookup"><span data-stu-id="5427c-146">The following example shows a tracking profile in a configuration file that allows a tracking participant to subscribe to the `Started` and `Completed` workflow events.</span></span>  
  
```xml  
<system.serviceModel>  
  <tracking>
    <trackingProfile name="Sample Tracking Profile">  
      <workflow activityDefinitionId="*">  
         <workflowInstanceQueries>  
            <workflowInstanceQuery>  
            <states>  
              <state name="Started"/>  
              <state name="Completed"/>  
            </states>  
          </workflowInstanceQuery>  
        </workflowInstanceQueries>  
      </workflow>  
    </trackingProfile>
   </profiles>  
  </tracking>  
</system.serviceModel>  
```  
  
## <a name="see-also"></a><span data-ttu-id="5427c-147">请参阅</span><span class="sxs-lookup"><span data-stu-id="5427c-147">See also</span></span>

- <xref:System.ServiceModel.Activities.Tracking.Configuration.ProfileWorkflowElement>
- <xref:System.Activities.Tracking.TrackingProfile>
- [<span data-ttu-id="5427c-148">工作流跟踪</span><span class="sxs-lookup"><span data-stu-id="5427c-148">Workflow Tracking and Tracing</span></span>](../../../windows-workflow-foundation/workflow-tracking-and-tracing.md)
- [<span data-ttu-id="5427c-149">跟踪配置文件</span><span class="sxs-lookup"><span data-stu-id="5427c-149">Tracking Profiles</span></span>](../../../windows-workflow-foundation/tracking-profiles.md)
