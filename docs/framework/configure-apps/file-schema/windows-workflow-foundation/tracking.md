---
description: 了解详细信息： <tracking>
title: <tracking>
ms.date: 03/30/2017
ms.topic: reference
ms.assetid: fd9b50ed-98a1-4518-836d-e4e02c670822
ms.openlocfilehash: 6301d3c6e472010e3ab78f7d85193f17adb15a1d
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99739728"
---
# \<tracking>

<span data-ttu-id="02462-102">表示一个配置节，用于定义工作流服务的跟踪设置。</span><span class="sxs-lookup"><span data-stu-id="02462-102">Represents a configuration section for defining tracking settings for a workflow service.</span></span>  
  
 <span data-ttu-id="02462-103">有关工作流跟踪及其配置的详细信息，请参阅工作流 [跟踪和跟踪](../../../windows-workflow-foundation/workflow-tracking-and-tracing.md) 和 [配置工作流跟踪](../../../windows-workflow-foundation/configuring-tracking-for-a-workflow.md)。</span><span class="sxs-lookup"><span data-stu-id="02462-103">For more information in workflow tracking and its configuration, see [Workflow Tracking and Tracing](../../../windows-workflow-foundation/workflow-tracking-and-tracing.md) and [Configuring Tracking for a Workflow](../../../windows-workflow-foundation/configuring-tracking-for-a-workflow.md).</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.ServiceModel>**](system-servicemodel-of-workflow.md)\
&nbsp;&nbsp;&nbsp;&nbsp;**\<tracking>**  
  
## <a name="syntax"></a><span data-ttu-id="02462-104">语法</span><span class="sxs-lookup"><span data-stu-id="02462-104">Syntax</span></span>  
  
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
  
## <a name="attributes-and-elements"></a><span data-ttu-id="02462-105">特性和元素</span><span class="sxs-lookup"><span data-stu-id="02462-105">Attributes and Elements</span></span>  

 <span data-ttu-id="02462-106">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="02462-106">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="02462-107">特性</span><span class="sxs-lookup"><span data-stu-id="02462-107">Attributes</span></span>  

 <span data-ttu-id="02462-108">无。</span><span class="sxs-lookup"><span data-stu-id="02462-108">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="02462-109">子元素</span><span class="sxs-lookup"><span data-stu-id="02462-109">Child Elements</span></span>  
  
|<span data-ttu-id="02462-110">元素</span><span class="sxs-lookup"><span data-stu-id="02462-110">Element</span></span>|<span data-ttu-id="02462-111">说明</span><span class="sxs-lookup"><span data-stu-id="02462-111">Description</span></span>|  
|-------------|-----------------|  
|[\<participants>](participants.md)|<span data-ttu-id="02462-112">一个配置元素集合，这些元素定义了订阅跟踪记录的参与者。</span><span class="sxs-lookup"><span data-stu-id="02462-112">A collection of configuration elements defining participants that subscribe to tracking records.</span></span> <span data-ttu-id="02462-113">跟踪参与者包含用于处理跟踪记录中负载的逻辑（例如，它们可以选择向某个文件中写入）。</span><span class="sxs-lookup"><span data-stu-id="02462-113">The tracking participants contain the logic to process the payload from the tracking records (for example, they could choose to write to a file).</span></span>|  
|[\<trackingProfile>](trackingprofile.md)|<span data-ttu-id="02462-114">一个跟踪配置文件，用于筛选从工作流实例发出的跟踪记录。</span><span class="sxs-lookup"><span data-stu-id="02462-114">A tracking profile to filter tracking records emitted from a workflow instance.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="02462-115">父元素</span><span class="sxs-lookup"><span data-stu-id="02462-115">Parent Elements</span></span>  
  
|<span data-ttu-id="02462-116">元素</span><span class="sxs-lookup"><span data-stu-id="02462-116">Element</span></span>|<span data-ttu-id="02462-117">说明</span><span class="sxs-lookup"><span data-stu-id="02462-117">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="02462-118">system.ServiceModel</span><span class="sxs-lookup"><span data-stu-id="02462-118">system.ServiceModel</span></span>|<span data-ttu-id="02462-119">所有工作流配置元素的根元素。</span><span class="sxs-lookup"><span data-stu-id="02462-119">The root element of all workflow configuration elements.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="02462-120">备注</span><span class="sxs-lookup"><span data-stu-id="02462-120">Remarks</span></span>  

 <span data-ttu-id="02462-121">利用跟踪可以检查工作流的执行。</span><span class="sxs-lookup"><span data-stu-id="02462-121">Tracking provides you with the ability to examine the execution of a workflow.</span></span> <span data-ttu-id="02462-122">工作流跟踪基础结构检测工作流以发出反应执行期间关键事件的记录。</span><span class="sxs-lookup"><span data-stu-id="02462-122">The workflow tracking infrastructure instruments a workflow to emit records reflecting key events during the execution.</span></span> <span data-ttu-id="02462-123">例如，工作流实例开始或完成时会发出跟踪记录。</span><span class="sxs-lookup"><span data-stu-id="02462-123">For example, when a workflow instance starts or completes tracking records are emitted.</span></span> <span data-ttu-id="02462-124">跟踪还可以提取与工作流变量关联的相关业务数据。</span><span class="sxs-lookup"><span data-stu-id="02462-124">Tracking can also extract business relevant data associated with the workflow variables.</span></span> <span data-ttu-id="02462-125">例如，如果工作流表示一个订单处理系统，则可以提取订单 ID 以及跟踪记录。</span><span class="sxs-lookup"><span data-stu-id="02462-125">For example, if the workflow represents an order processing system the order id can be extracted along with the tracking record.</span></span> <span data-ttu-id="02462-126">一般来讲，启用 WF 跟踪便于对工作流的执行进行诊断或业务分析。</span><span class="sxs-lookup"><span data-stu-id="02462-126">In general, enabling WF tracking facilitates diagnostics or business analytics over a workflow execution.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="02462-127">请参阅</span><span class="sxs-lookup"><span data-stu-id="02462-127">See also</span></span>

- <xref:System.ServiceModel.Activities.Tracking.Configuration.TrackingSection?displayProperty=nameWithType>
- [<span data-ttu-id="02462-128">工作流跟踪</span><span class="sxs-lookup"><span data-stu-id="02462-128">Workflow Tracking and Tracing</span></span>](../../../windows-workflow-foundation/workflow-tracking-and-tracing.md)
