---
description: 了解详细信息： <activityStateQuery>
title: <activityStateQuery>
ms.date: 03/30/2017
ms.topic: reference
ms.assetid: 9f8c3e4f-e2e3-4402-9760-03bf918ece7b
ms.openlocfilehash: 1fff356436e5c55ba8b423b20589d234050fcda1
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99748942"
---
# \<activityStateQuery>

<span data-ttu-id="9c0c5-102">表示一个查询，该查询用于跟踪构成工作流实例的活动的生命周期更改。</span><span class="sxs-lookup"><span data-stu-id="9c0c5-102">Represents a query that is used to track life cycle changes of the activities that make up a workflow instance.</span></span> <span data-ttu-id="9c0c5-103">例如，你可能想要跟踪每次在工作流实例中完成 "发送电子邮件" 活动的时间。</span><span class="sxs-lookup"><span data-stu-id="9c0c5-103">For example, you may want to keep track of every time the "Send E-Mail" activity completes within a workflow instance.</span></span> <span data-ttu-id="9c0c5-104">跟踪参与者需要用此查询来订阅活动状态记录对象。</span><span class="sxs-lookup"><span data-stu-id="9c0c5-104">This query is necessary for a tracking participant to subscribe to activity state record objects.</span></span> <span data-ttu-id="9c0c5-105">在 ActivityStates 中指定了要订阅的可用状态。</span><span class="sxs-lookup"><span data-stu-id="9c0c5-105">The available states to subscribe to are specified in ActivityStates.</span></span>  
  
 <span data-ttu-id="9c0c5-106">有关跟踪配置文件查询的详细信息，请参阅 [跟踪配置文件](../../../windows-workflow-foundation/tracking-profiles.md)。</span><span class="sxs-lookup"><span data-stu-id="9c0c5-106">For more information on tracking profile queries, see [Tracking Profiles](../../../windows-workflow-foundation/tracking-profiles.md).</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.ServiceModel>**](system-servicemodel-of-workflow.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<tracking>**](tracking.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<trackingProfile>**](trackingprofile.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<workflow>**](workflow.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<activityStateQueries>**](activitystatequeries.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<activityStateQuery>**  
  
## <a name="syntax"></a><span data-ttu-id="9c0c5-107">语法</span><span class="sxs-lookup"><span data-stu-id="9c0c5-107">Syntax</span></span>  
  
```xml
<tracking>
  <trackingProfile name="Name">
    <workflow>
      <activityStateQueries>
        <activityStateQuery activityName="String" />
        <arguments>
          <argument name="String"/>
        </arguments>
        <states>
          <state name="String"/>
        </states>
        <variables>
          <variable name="String"/>
        </variables>
      </activityStateQueries>
    </workflow>
  </trackingProfile>
</tracking>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="9c0c5-108">特性和元素</span><span class="sxs-lookup"><span data-stu-id="9c0c5-108">Attributes and Elements</span></span>  

 <span data-ttu-id="9c0c5-109">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="9c0c5-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="9c0c5-110">特性</span><span class="sxs-lookup"><span data-stu-id="9c0c5-110">Attributes</span></span>  
  
|<span data-ttu-id="9c0c5-111">属性</span><span class="sxs-lookup"><span data-stu-id="9c0c5-111">Attribute</span></span>|<span data-ttu-id="9c0c5-112">说明</span><span class="sxs-lookup"><span data-stu-id="9c0c5-112">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="9c0c5-113">activityName</span><span class="sxs-lookup"><span data-stu-id="9c0c5-113">activityName</span></span>|<span data-ttu-id="9c0c5-114">一个字符串，指定要对其筛选 <xref:System.Activities.Tracking.ActivityStateRecord> 实例的活动的名称。</span><span class="sxs-lookup"><span data-stu-id="9c0c5-114">A string that specifies the name of the activity to filter <xref:System.Activities.Tracking.ActivityStateRecord> instances on.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="9c0c5-115">子元素</span><span class="sxs-lookup"><span data-stu-id="9c0c5-115">Child Elements</span></span>  
  
|<span data-ttu-id="9c0c5-116">元素</span><span class="sxs-lookup"><span data-stu-id="9c0c5-116">Element</span></span>|<span data-ttu-id="9c0c5-117">说明</span><span class="sxs-lookup"><span data-stu-id="9c0c5-117">Description</span></span>|  
|-------------|-----------------|  
|[\<arguments>](arguments.md)|<span data-ttu-id="9c0c5-118">与此活动查询关联的自变量的集合。</span><span class="sxs-lookup"><span data-stu-id="9c0c5-118">A collection of arguments associated with this activity query.</span></span>|  
|[\<states>](states.md)|<span data-ttu-id="9c0c5-119">一个配置元素集合，这些元素包含应为其发出跟踪记录的已订阅活动的状态。</span><span class="sxs-lookup"><span data-stu-id="9c0c5-119">A collection of configuration elements that contain the states of the subscribed activity for which a tracking record should be emitted.</span></span>|  
|[\<states>](states.md)|<span data-ttu-id="9c0c5-120">与此活动查询关联的变量的集合。</span><span class="sxs-lookup"><span data-stu-id="9c0c5-120">A collection of variables associated with this activity query.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="9c0c5-121">父元素</span><span class="sxs-lookup"><span data-stu-id="9c0c5-121">Parent Elements</span></span>  
  
|<span data-ttu-id="9c0c5-122">元素</span><span class="sxs-lookup"><span data-stu-id="9c0c5-122">Element</span></span>|<span data-ttu-id="9c0c5-123">说明</span><span class="sxs-lookup"><span data-stu-id="9c0c5-123">Description</span></span>|  
|-------------|-----------------|  
|[\<faultPropagationQuery>](faultpropagationquery.md)|<span data-ttu-id="9c0c5-124">表示一个配置元素列表，这些元素用于跟踪父活动取消子活动的请求。</span><span class="sxs-lookup"><span data-stu-id="9c0c5-124">Represents a list of configuration elements that are used to track requests to cancel a child activity by the parent activity.</span></span> <span data-ttu-id="9c0c5-125">跟踪参与者需要用此查询来订阅取消请求记录对象。</span><span class="sxs-lookup"><span data-stu-id="9c0c5-125">The query is necessary for a tracking participant to subscribe to cancel request record objects.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="9c0c5-126">备注</span><span class="sxs-lookup"><span data-stu-id="9c0c5-126">Remarks</span></span>  

 <span data-ttu-id="9c0c5-127">ActivityStateQuery 的一项独特功能是能够在跟踪工作流的执行时提取数据。</span><span class="sxs-lookup"><span data-stu-id="9c0c5-127">One unique feature of an ActivityStateQuery is the ability to extract data when tracking the execution of a workflow.</span></span> <span data-ttu-id="9c0c5-128">这在访问跟踪记录后续执行时可提供其他上下文。</span><span class="sxs-lookup"><span data-stu-id="9c0c5-128">This provides additional context when accessing the tracking records post execution.</span></span> <span data-ttu-id="9c0c5-129">您可以使用 [\<arguments>](arguments.md) 、 [\<states>](states.md) 和 [\<states>](states.md) 元素从工作流中的任何活动提取任何变量或参数。</span><span class="sxs-lookup"><span data-stu-id="9c0c5-129">You can use the [\<arguments>](arguments.md), [\<states>](states.md) and [\<states>](states.md) elements to extract any variable or argument from any activity in a workflow.</span></span> <span data-ttu-id="9c0c5-130">下面的示例演示用于在发出活动的 `Closed` 跟踪记录时提取变量和自变量的活动状态查询。</span><span class="sxs-lookup"><span data-stu-id="9c0c5-130">The following example shows an activity state query that extracts variables and arguments when the activity’s `Closed` tracking record is emitted.</span></span> <span data-ttu-id="9c0c5-131">变量和参数只能通过 ActivityStateRecord 提取，因此使用在跟踪配置文件内进行订阅 [\<activityStateQuery>](activitystatequery.md) 。</span><span class="sxs-lookup"><span data-stu-id="9c0c5-131">Variables and arguments can be extracted only with an ActivityStateRecord and thus are subscribed to within a tracking profile using [\<activityStateQuery>](activitystatequery.md).</span></span>  
  
```xml  
<activityStateQuery activityName="SendEmailActivity">  
  <states>  
    <state name="Closed"/>  
  </states>  
  <variables>  
    <variable name="FromAddress"/>  
  </variables>  
  <arguments>  
    <argument name="Result"/>  
  </arguments>  
</activityStateQuery>  
```  
  
## <a name="see-also"></a><span data-ttu-id="9c0c5-132">请参阅</span><span class="sxs-lookup"><span data-stu-id="9c0c5-132">See also</span></span>

- <xref:System.ServiceModel.Activities.Tracking.Configuration.ActivityStateQueryElement?displayProperty=nameWithType>
- <xref:System.Activities.Tracking.ActivityStateQuery?displayProperty=nameWithType>
- [<span data-ttu-id="9c0c5-133">工作流跟踪</span><span class="sxs-lookup"><span data-stu-id="9c0c5-133">Workflow Tracking and Tracing</span></span>](../../../windows-workflow-foundation/workflow-tracking-and-tracing.md)
- [<span data-ttu-id="9c0c5-134">跟踪配置文件</span><span class="sxs-lookup"><span data-stu-id="9c0c5-134">Tracking Profiles</span></span>](../../../windows-workflow-foundation/tracking-profiles.md)
