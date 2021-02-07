---
description: 了解详细信息： <workflowInstanceQuery>
title: <workflowInstanceQuery>
ms.date: 03/30/2017
ms.topic: reference
ms.assetid: 9096e812-626a-409a-9eda-c31a60b84c55
ms.openlocfilehash: 39949b99e7c6c12ff8618e6aa3a43582d15d4133
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99697785"
---
# \<workflowInstanceQuery>

<span data-ttu-id="e9aca-102">表示一个查询，该查询跟踪工作流实例生命周期的更改，例如已开始或已完成的事件。</span><span class="sxs-lookup"><span data-stu-id="e9aca-102">Represents a query that tracks workflow instance life cycle changes such as a started or completed event.</span></span>  
  
 <span data-ttu-id="e9aca-103">有关跟踪配置文件查询的详细信息，请参阅 [跟踪配置文件](../../../windows-workflow-foundation/tracking-profiles.md)</span><span class="sxs-lookup"><span data-stu-id="e9aca-103">For more information on tracking profile queries, see [Tracking Profiles](../../../windows-workflow-foundation/tracking-profiles.md)</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.ServiceModel>**](system-servicemodel-of-workflow.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<tracking>**](tracking.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<trackingProfile>**](trackingprofile.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<workflow>**](workflow.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<workflowInstanceQueries>**](workflowinstancequeries.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<workflowInstanceQuery>**  
  
## <a name="syntax"></a><span data-ttu-id="e9aca-104">语法</span><span class="sxs-lookup"><span data-stu-id="e9aca-104">Syntax</span></span>  
  
```xml  
<tracking>
  <trackingProfile name="Name">
    <workflow>
      <workflowInstanceQueries>
        <workflowInstanceQuery>
          <states>
            <state name="Name" />
          </states>
        </workflowInstanceQuery>
      </workflowInstanceQueries>
    </workflow>
  </trackingProfile>
</tracking>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="e9aca-105">特性和元素</span><span class="sxs-lookup"><span data-stu-id="e9aca-105">Attributes and Elements</span></span>  

 <span data-ttu-id="e9aca-106">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="e9aca-106">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="e9aca-107">特性</span><span class="sxs-lookup"><span data-stu-id="e9aca-107">Attributes</span></span>  

 <span data-ttu-id="e9aca-108">无。</span><span class="sxs-lookup"><span data-stu-id="e9aca-108">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="e9aca-109">子元素</span><span class="sxs-lookup"><span data-stu-id="e9aca-109">Child Elements</span></span>  
  
|<span data-ttu-id="e9aca-110">元素</span><span class="sxs-lookup"><span data-stu-id="e9aca-110">Element</span></span>|<span data-ttu-id="e9aca-111">说明</span><span class="sxs-lookup"><span data-stu-id="e9aca-111">Description</span></span>|  
|-------------|-----------------|  
|[\<states>](states.md)|<span data-ttu-id="e9aca-112">创建跟踪记录时已跟踪工作流实例中已订阅状态的集合。</span><span class="sxs-lookup"><span data-stu-id="e9aca-112">A collection of subscribed states from the tracked workflow instance when the tracking records are created.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="e9aca-113">父元素</span><span class="sxs-lookup"><span data-stu-id="e9aca-113">Parent Elements</span></span>  
  
|<span data-ttu-id="e9aca-114">元素</span><span class="sxs-lookup"><span data-stu-id="e9aca-114">Element</span></span>|<span data-ttu-id="e9aca-115">说明</span><span class="sxs-lookup"><span data-stu-id="e9aca-115">Description</span></span>|  
|-------------|-----------------|  
|[\<workflowInstanceQueries>](workflowinstancequeries.md)|<span data-ttu-id="e9aca-116">表示配置元素的集合，这些配置元素跟踪工作流实例生命周期的更改，例如已开始或已完成的事件。</span><span class="sxs-lookup"><span data-stu-id="e9aca-116">Represents a collection of configuration elements that track workflow instance life cycle changes such as a started or completed event.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="e9aca-117">备注</span><span class="sxs-lookup"><span data-stu-id="e9aca-117">Remarks</span></span>  

 <span data-ttu-id="e9aca-118"><xref:System.Activities.Tracking.WorkflowInstanceQuery> 用于订阅以下 <xref:System.Activities.Tracking.TrackingRecord> 对象：</span><span class="sxs-lookup"><span data-stu-id="e9aca-118">The <xref:System.Activities.Tracking.WorkflowInstanceQuery> is used to subscribe to the following <xref:System.Activities.Tracking.TrackingRecord> objects:</span></span>  
  
- <xref:System.Activities.Tracking.WorkflowInstanceRecord>  
  
- <xref:System.Activities.Tracking.WorkflowInstanceAbortedRecord>  
  
- <xref:System.Activities.Tracking.WorkflowInstanceUnhandledExceptionRecord>  
  
- <xref:System.Activities.Tracking.WorkflowInstanceTerminatedRecord>  
  
- <xref:System.Activities.Tracking.WorkflowInstanceSuspendedRecord>  
  
## <a name="example"></a><span data-ttu-id="e9aca-119">示例</span><span class="sxs-lookup"><span data-stu-id="e9aca-119">Example</span></span>  

 <span data-ttu-id="e9aca-120">下面的配置使用此查询订阅 `Started` 实例状态的工作流实例级跟踪记录。</span><span class="sxs-lookup"><span data-stu-id="e9aca-120">The following configuration subscribes to workflow instance-level tracking records for the `Started` instance state using this query.</span></span>  
  
```xml  
<workflowInstanceQueries>  
    <workflowInstanceQuery>  
      <states>  
        <state name="Started"/>  
      </states>  
    </workflowInstanceQuery>  
</workflowInstanceQueries>  
```  
  
## <a name="see-also"></a><span data-ttu-id="e9aca-121">请参阅</span><span class="sxs-lookup"><span data-stu-id="e9aca-121">See also</span></span>

- <xref:System.ServiceModel.Activities.Tracking.Configuration.WorkflowInstanceQueryElement?displayProperty=nameWithType>
- <xref:System.Activities.Tracking.WorkflowInstanceQuery?displayProperty=nameWithType>
- [<span data-ttu-id="e9aca-122">工作流跟踪</span><span class="sxs-lookup"><span data-stu-id="e9aca-122">Workflow Tracking and Tracing</span></span>](../../../windows-workflow-foundation/workflow-tracking-and-tracing.md)
- [<span data-ttu-id="e9aca-123">跟踪配置文件</span><span class="sxs-lookup"><span data-stu-id="e9aca-123">Tracking Profiles</span></span>](../../../windows-workflow-foundation/tracking-profiles.md)
