---
description: 了解详细 <states> 信息： <activityStateQuery>
title: <states> 的 <activityStateQuery>
ms.date: 03/30/2017
ms.topic: reference
ms.assetid: a7cc2018-2b79-44f1-825a-bb7ca08690a3
ms.openlocfilehash: 16a0af865508f0ebc50d16728c35188310c95043
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99773272"
---
# <a name="states-of-activitystatequery"></a><span data-ttu-id="a340c-103">\<states> 的 \<activityStateQuery></span><span class="sxs-lookup"><span data-stu-id="a340c-103">\<states> of \<activityStateQuery></span></span>

<span data-ttu-id="a340c-104">一个配置元素集合，这些元素包含应为其发出跟踪记录的已订阅活动的状态。</span><span class="sxs-lookup"><span data-stu-id="a340c-104">A collection of configuration elements that contain the states of the subscribed activity for which a tracking record should be emitted.</span></span>  
  
 <span data-ttu-id="a340c-105">有关跟踪配置文件查询的详细信息，请参阅 [跟踪配置文件](../../../windows-workflow-foundation/tracking-profiles.md)。</span><span class="sxs-lookup"><span data-stu-id="a340c-105">For more information on tracking profile queries, see [Tracking Profiles](../../../windows-workflow-foundation/tracking-profiles.md).</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.ServiceModel>**](system-servicemodel-of-workflow.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<tracking>**](tracking.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<trackingProfile>**](trackingprofile.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<workflow>**](workflow.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<activityStateQueries>**](activitystatequeries.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<activityStateQuery>**](activitystatequery.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<states>**  
  
## <a name="syntax"></a><span data-ttu-id="a340c-106">语法</span><span class="sxs-lookup"><span data-stu-id="a340c-106">Syntax</span></span>  
  
```xml  
<tracking>
  <trackingProfile name="Name">
    <workflow>
      <activityStateQueries>
        <activityStateQuery activityName="String" />
        <states>
          <state name="String" />
        </states>
      </activityStateQueries>
    </workflow>
  </trackingProfile>
</tracking>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="a340c-107">特性和元素</span><span class="sxs-lookup"><span data-stu-id="a340c-107">Attributes and Elements</span></span>  

 <span data-ttu-id="a340c-108">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="a340c-108">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="a340c-109">特性</span><span class="sxs-lookup"><span data-stu-id="a340c-109">Attributes</span></span>  

 <span data-ttu-id="a340c-110">无。</span><span class="sxs-lookup"><span data-stu-id="a340c-110">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="a340c-111">子元素</span><span class="sxs-lookup"><span data-stu-id="a340c-111">Child Elements</span></span>  
  
|<span data-ttu-id="a340c-112">元素</span><span class="sxs-lookup"><span data-stu-id="a340c-112">Element</span></span>|<span data-ttu-id="a340c-113">说明</span><span class="sxs-lookup"><span data-stu-id="a340c-113">Description</span></span>|  
|-------------|-----------------|  
|[\<state>](state-of-states.md)|<span data-ttu-id="a340c-114">一个配置元素，该元素包含应为其发出跟踪记录的已订阅活动的状态。</span><span class="sxs-lookup"><span data-stu-id="a340c-114">A configuration element that contains the states of the subscribed activity for which a tracking record should be emitted.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="a340c-115">父元素</span><span class="sxs-lookup"><span data-stu-id="a340c-115">Parent Elements</span></span>  
  
|<span data-ttu-id="a340c-116">元素</span><span class="sxs-lookup"><span data-stu-id="a340c-116">Element</span></span>|<span data-ttu-id="a340c-117">说明</span><span class="sxs-lookup"><span data-stu-id="a340c-117">Description</span></span>|  
|-------------|-----------------|  
|[\<activityStateQuery>](activitystatequery.md)|<span data-ttu-id="a340c-118">表示一个配置元素，该元素用于跟踪父活动取消子活动的请求。</span><span class="sxs-lookup"><span data-stu-id="a340c-118">Represents a configuration element that is used to track requests to cancel a child activity by the parent activity.</span></span> <span data-ttu-id="a340c-119">跟踪参与者需要用此查询来订阅取消请求记录对象。</span><span class="sxs-lookup"><span data-stu-id="a340c-119">The query is necessary for a tracking participant to subscribe to cancel request record objects.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="a340c-120">备注</span><span class="sxs-lookup"><span data-stu-id="a340c-120">Remarks</span></span>  

 <span data-ttu-id="a340c-121">ActivityStateQuery 的一项独特功能是能够在跟踪工作流的执行时提取数据。</span><span class="sxs-lookup"><span data-stu-id="a340c-121">One unique feature of an ActivityStateQuery is the ability to extract data when tracking the execution of a workflow.</span></span> <span data-ttu-id="a340c-122">这在访问跟踪记录后续执行时可提供其他上下文。</span><span class="sxs-lookup"><span data-stu-id="a340c-122">This provides additional context when accessing the tracking records post execution.</span></span> <span data-ttu-id="a340c-123">您可以使用 [\<arguments>](arguments.md) 、 [\<states>](states.md) 和 [\<states>](states.md) 元素从工作流中的任何活动提取任何变量或参数。</span><span class="sxs-lookup"><span data-stu-id="a340c-123">You can use the [\<arguments>](arguments.md), [\<states>](states.md) and [\<states>](states.md) elements to extract any variable or argument from any activity in a workflow.</span></span> <span data-ttu-id="a340c-124">下面的示例演示用于在发出活动的 `Closed` 跟踪记录时提取变量和自变量的活动状态查询。</span><span class="sxs-lookup"><span data-stu-id="a340c-124">The following example shows an activity state query that extracts variables and arguments when the activity’s `Closed` tracking record is emitted.</span></span> <span data-ttu-id="a340c-125">变量和参数只能通过 ActivityStateRecord 提取，因此使用在跟踪配置文件内进行订阅 [\<activityStateQuery>](activitystatequery.md) 。</span><span class="sxs-lookup"><span data-stu-id="a340c-125">Variables and arguments can be extracted only with an ActivityStateRecord and thus are subscribed to within a tracking profile using [\<activityStateQuery>](activitystatequery.md).</span></span>  
  
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
  
## <a name="see-also"></a><span data-ttu-id="a340c-126">请参阅</span><span class="sxs-lookup"><span data-stu-id="a340c-126">See also</span></span>

- <xref:System.ServiceModel.Activities.Tracking.Configuration.StateElementCollection?displayProperty=nameWithType>
- <xref:System.Activities.Tracking.ActivityStateQuery?displayProperty=nameWithType>
- [<span data-ttu-id="a340c-127">工作流跟踪</span><span class="sxs-lookup"><span data-stu-id="a340c-127">Workflow Tracking and Tracing</span></span>](../../../windows-workflow-foundation/workflow-tracking-and-tracing.md)
- [<span data-ttu-id="a340c-128">跟踪配置文件</span><span class="sxs-lookup"><span data-stu-id="a340c-128">Tracking Profiles</span></span>](../../../windows-workflow-foundation/tracking-profiles.md)
