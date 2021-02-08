---
description: 了解详细 <state> 信息： <states>
title: <state> 的 <states>
ms.date: 03/30/2017
ms.topic: reference
ms.assetid: ab483c7f-a091-4933-ba6b-708d96846d38
ms.openlocfilehash: 748044986143f182faa0edafb0cfe299a79a704e
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99781982"
---
# <a name="state-of-states"></a><span data-ttu-id="ee4dc-103">\<state> 的 \<states></span><span class="sxs-lookup"><span data-stu-id="ee4dc-103">\<state> of \<states></span></span>

<span data-ttu-id="ee4dc-104">一个配置元素，该元素包含应为其发出跟踪记录的已订阅活动的状态。</span><span class="sxs-lookup"><span data-stu-id="ee4dc-104">A configuration element that contains the state of the subscribed activity for which a tracking record should be emitted.</span></span>  
  
 <span data-ttu-id="ee4dc-105">有关跟踪配置文件查询的详细信息，请参阅 [跟踪配置文件](../../../windows-workflow-foundation/tracking-profiles.md)。</span><span class="sxs-lookup"><span data-stu-id="ee4dc-105">For more information on tracking profile queries, see [Tracking Profiles](../../../windows-workflow-foundation/tracking-profiles.md).</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.ServiceModel>**](system-servicemodel-of-workflow.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<tracking>**](tracking.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<trackingProfile>**](trackingprofile.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<workflow>**](workflow.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<activityStateQueries>**](activitystatequeries.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<activityStateQuery>**](activitystatequery.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<states>**](states-of-activitystatequery.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<state>**  
  
## <a name="syntax"></a><span data-ttu-id="ee4dc-106">语法</span><span class="sxs-lookup"><span data-stu-id="ee4dc-106">Syntax</span></span>  
  
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
  
## <a name="attributes-and-elements"></a><span data-ttu-id="ee4dc-107">特性和元素</span><span class="sxs-lookup"><span data-stu-id="ee4dc-107">Attributes and Elements</span></span>  

 <span data-ttu-id="ee4dc-108">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="ee4dc-108">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="ee4dc-109">特性</span><span class="sxs-lookup"><span data-stu-id="ee4dc-109">Attributes</span></span>  
  
|<span data-ttu-id="ee4dc-110">属性</span><span class="sxs-lookup"><span data-stu-id="ee4dc-110">Attribute</span></span>|<span data-ttu-id="ee4dc-111">说明</span><span class="sxs-lookup"><span data-stu-id="ee4dc-111">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="ee4dc-112">name</span><span class="sxs-lookup"><span data-stu-id="ee4dc-112">name</span></span>|<span data-ttu-id="ee4dc-113">一个字符串，指定应为其发出跟踪记录的已订阅活动的状态。</span><span class="sxs-lookup"><span data-stu-id="ee4dc-113">A string that specifies the state of the subscribed activity for which a tracking record should be emitted.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="ee4dc-114">子元素</span><span class="sxs-lookup"><span data-stu-id="ee4dc-114">Child Elements</span></span>  

 <span data-ttu-id="ee4dc-115">无。</span><span class="sxs-lookup"><span data-stu-id="ee4dc-115">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="ee4dc-116">父元素</span><span class="sxs-lookup"><span data-stu-id="ee4dc-116">Parent Elements</span></span>  
  
|<span data-ttu-id="ee4dc-117">元素</span><span class="sxs-lookup"><span data-stu-id="ee4dc-117">Element</span></span>|<span data-ttu-id="ee4dc-118">说明</span><span class="sxs-lookup"><span data-stu-id="ee4dc-118">Description</span></span>|  
|-------------|-----------------|  
|[\<states>](states-of-activitystatequery.md)|<span data-ttu-id="ee4dc-119">一个配置元素集合，这些元素包含应为其发出跟踪记录的已订阅活动的状态。</span><span class="sxs-lookup"><span data-stu-id="ee4dc-119">A collection of configuration elements that contain the states of the subscribed activity for which a tracking record should be emitted.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="ee4dc-120">备注</span><span class="sxs-lookup"><span data-stu-id="ee4dc-120">Remarks</span></span>  

 <span data-ttu-id="ee4dc-121">ActivityStateQuery 的一项独特功能是能够在跟踪工作流的执行时提取数据。</span><span class="sxs-lookup"><span data-stu-id="ee4dc-121">One unique feature of an ActivityStateQuery is the ability to extract data when tracking the execution of a workflow.</span></span> <span data-ttu-id="ee4dc-122">这在访问跟踪记录后续执行时可提供其他上下文。</span><span class="sxs-lookup"><span data-stu-id="ee4dc-122">This provides additional context when accessing the tracking records post execution.</span></span> <span data-ttu-id="ee4dc-123">您可以使用 [\<arguments>](arguments.md) 、 [\<states>](states.md) 和 [\<states>](states.md) 元素从工作流中的任何活动提取任何变量或参数。</span><span class="sxs-lookup"><span data-stu-id="ee4dc-123">You can use the [\<arguments>](arguments.md), [\<states>](states.md) and [\<states>](states.md) elements to extract any variable or argument from any activity in a workflow.</span></span> <span data-ttu-id="ee4dc-124">下面的示例演示用于在发出活动的 `Closed` 跟踪记录时提取变量和自变量的活动状态查询。</span><span class="sxs-lookup"><span data-stu-id="ee4dc-124">The following example shows an activity state query that extracts variables and arguments when the activity’s `Closed` tracking record is emitted.</span></span> <span data-ttu-id="ee4dc-125">变量和参数只能通过 ActivityStateRecord 提取，因此使用在跟踪配置文件内进行订阅 [\<activityStateQuery>](activitystatequery.md) 。</span><span class="sxs-lookup"><span data-stu-id="ee4dc-125">Variables and arguments can be extracted only with an ActivityStateRecord and thus are subscribed to within a tracking profile using [\<activityStateQuery>](activitystatequery.md).</span></span>  
  
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
  
## <a name="see-also"></a><span data-ttu-id="ee4dc-126">请参阅</span><span class="sxs-lookup"><span data-stu-id="ee4dc-126">See also</span></span>

- <xref:System.ServiceModel.Activities.Tracking.Configuration.StateElement?displayProperty=nameWithType>
- <xref:System.Activities.Tracking.ActivityStateQuery?displayProperty=nameWithType>
- [<span data-ttu-id="ee4dc-127">工作流跟踪</span><span class="sxs-lookup"><span data-stu-id="ee4dc-127">Workflow Tracking and Tracing</span></span>](../../../windows-workflow-foundation/workflow-tracking-and-tracing.md)
- [<span data-ttu-id="ee4dc-128">跟踪配置文件</span><span class="sxs-lookup"><span data-stu-id="ee4dc-128">Tracking Profiles</span></span>](../../../windows-workflow-foundation/tracking-profiles.md)
