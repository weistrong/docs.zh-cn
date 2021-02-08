---
description: 了解有关 WCF 的详细信息： <tracking>
title: <tracking> WCF 的
ms.date: 03/30/2017
ms.assetid: 70cfaf24-a91c-4e56-ac47-d2ed87a963b3
ms.openlocfilehash: e372139623cd0b92bde74a6b19761d8a4c5ad6db
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99773818"
---
# <a name="tracking-of-wcf"></a><span data-ttu-id="592cd-103">\<tracking> WCF 的</span><span class="sxs-lookup"><span data-stu-id="592cd-103">\<tracking> of WCF</span></span>

<span data-ttu-id="592cd-104">表示一个配置节，用于定义工作流服务的跟踪设置。</span><span class="sxs-lookup"><span data-stu-id="592cd-104">Represents a configuration section for defining tracking settings for a workflow service.</span></span>  
  
 <span data-ttu-id="592cd-105">有关工作流跟踪及其配置的详细信息，请参阅工作流 [跟踪和跟踪](../../../windows-workflow-foundation/workflow-tracking-and-tracing.md) 和 [配置工作流跟踪](../../../windows-workflow-foundation/configuring-tracking-for-a-workflow.md)。</span><span class="sxs-lookup"><span data-stu-id="592cd-105">For more information in workflow tracking and its configuration, see [Workflow Tracking and Tracing](../../../windows-workflow-foundation/workflow-tracking-and-tracing.md) and [Configuring Tracking for a Workflow](../../../windows-workflow-foundation/configuring-tracking-for-a-workflow.md).</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;**\<tracking>**  
  
## <a name="syntax"></a><span data-ttu-id="592cd-106">语法</span><span class="sxs-lookup"><span data-stu-id="592cd-106">Syntax</span></span>  
  
```xml  
<system.serviceModel>
  <tracking>
    <participants>
      <add name="String"
           profileName="String"
           type="String" />
    </participants>
    <profiles>
      <trackingProfile name="String">
        <workflow activityDefinitionId="String">
          <activityScheduledQueries>
            <activityScheduledQuery activityName="String"
                                    childActivityName="String"/>
          </activityScheduledQueries>
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
                                   faultHandlerActivityName="String"/>
          </faultPropagationQueries>
          <workflowInstanceQueries>
            <workflowInstanceQuery>
              <states>
                <state name="String"/>
              </states>
            </workflowInstanceQuery>
          </workflowInstanceQueries>
        </workflow>
      </trackingProfile>
    </profiles>
  </tracking>
</system.serviceModel>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="592cd-107">特性和元素</span><span class="sxs-lookup"><span data-stu-id="592cd-107">Attributes and Elements</span></span>  

 <span data-ttu-id="592cd-108">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="592cd-108">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="592cd-109">特性</span><span class="sxs-lookup"><span data-stu-id="592cd-109">Attributes</span></span>  

 <span data-ttu-id="592cd-110">无。</span><span class="sxs-lookup"><span data-stu-id="592cd-110">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="592cd-111">子元素</span><span class="sxs-lookup"><span data-stu-id="592cd-111">Child Elements</span></span>  
  
|<span data-ttu-id="592cd-112">元素</span><span class="sxs-lookup"><span data-stu-id="592cd-112">Element</span></span>|<span data-ttu-id="592cd-113">说明</span><span class="sxs-lookup"><span data-stu-id="592cd-113">Description</span></span>|  
|-------------|-----------------|  
|[\<participants>](../windows-workflow-foundation/participants.md)|<span data-ttu-id="592cd-114">一个配置元素集合，这些元素定义了订阅跟踪记录的参与者。</span><span class="sxs-lookup"><span data-stu-id="592cd-114">A collection of configuration elements defining participants that subscribe to tracking records.</span></span> <span data-ttu-id="592cd-115">跟踪参与者包含用于处理跟踪记录中负载的逻辑（例如，它们可以选择向某个文件中写入）。</span><span class="sxs-lookup"><span data-stu-id="592cd-115">The tracking participants contain the logic to process the payload from the tracking records (for example, they could choose to write to a file).</span></span>|  
|[\<trackingProfile>](../windows-workflow-foundation/trackingprofile.md)|<span data-ttu-id="592cd-116">一个跟踪配置文件，用于筛选从工作流实例发出的跟踪记录。</span><span class="sxs-lookup"><span data-stu-id="592cd-116">A tracking profile to filter tracking records emitted from a workflow instance.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="592cd-117">父元素</span><span class="sxs-lookup"><span data-stu-id="592cd-117">Parent Elements</span></span>  
  
|<span data-ttu-id="592cd-118">元素</span><span class="sxs-lookup"><span data-stu-id="592cd-118">Element</span></span>|<span data-ttu-id="592cd-119">说明</span><span class="sxs-lookup"><span data-stu-id="592cd-119">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="592cd-120">system.ServiceModel</span><span class="sxs-lookup"><span data-stu-id="592cd-120">system.ServiceModel</span></span>|<span data-ttu-id="592cd-121">所有工作流配置元素的根元素。</span><span class="sxs-lookup"><span data-stu-id="592cd-121">The root element of all workflow configuration elements.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="592cd-122">备注</span><span class="sxs-lookup"><span data-stu-id="592cd-122">Remarks</span></span>  

 <span data-ttu-id="592cd-123">利用跟踪可以检查工作流的执行。</span><span class="sxs-lookup"><span data-stu-id="592cd-123">Tracking provides you with the ability to examine the execution of a workflow.</span></span> <span data-ttu-id="592cd-124">工作流跟踪基础结构检测工作流以发出反应执行期间关键事件的记录。</span><span class="sxs-lookup"><span data-stu-id="592cd-124">The workflow tracking infrastructure instruments a workflow to emit records reflecting key events during the execution.</span></span> <span data-ttu-id="592cd-125">例如，工作流实例开始或完成时会发出跟踪记录。</span><span class="sxs-lookup"><span data-stu-id="592cd-125">For example, when a workflow instance starts or completes tracking records are emitted.</span></span> <span data-ttu-id="592cd-126">跟踪还可以提取与工作流变量关联的相关业务数据。</span><span class="sxs-lookup"><span data-stu-id="592cd-126">Tracking can also extract business relevant data associated with the workflow variables.</span></span> <span data-ttu-id="592cd-127">例如，如果工作流表示一个订单处理系统，则可以提取订单 ID 以及跟踪记录。</span><span class="sxs-lookup"><span data-stu-id="592cd-127">For example, if the workflow represents an order processing system the order id can be extracted along with the tracking record.</span></span> <span data-ttu-id="592cd-128">一般来讲，启用 WF 跟踪便于对工作流的执行进行诊断或业务分析。</span><span class="sxs-lookup"><span data-stu-id="592cd-128">In general, enabling WF tracking facilitates diagnostics or business analytics over a workflow execution.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="592cd-129">请参阅</span><span class="sxs-lookup"><span data-stu-id="592cd-129">See also</span></span>

- <xref:System.ServiceModel.Activities.Tracking.Configuration.TrackingSection?displayProperty=nameWithType>
- [<span data-ttu-id="592cd-130">工作流跟踪</span><span class="sxs-lookup"><span data-stu-id="592cd-130">Workflow Tracking and Tracing</span></span>](../../../windows-workflow-foundation/workflow-tracking-and-tracing.md)
