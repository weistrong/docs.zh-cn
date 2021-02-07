---
description: 了解有关 WCF 的详细信息： <workflowInstanceQuery>
title: <workflowInstanceQuery> WCF 的
ms.date: 03/30/2017
ms.assetid: 35c73f9d-474e-42eb-874d-ddc04b1987f3
ms.openlocfilehash: 30df1a6b4fc0aeac5b7094f1a1f7d9d02599c94d
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99682314"
---
# <a name="workflowinstancequery-of-wcf"></a><span data-ttu-id="81303-103">\<workflowInstanceQuery> WCF 的</span><span class="sxs-lookup"><span data-stu-id="81303-103">\<workflowInstanceQuery> of WCF</span></span>

<span data-ttu-id="81303-104">表示一个查询，该查询跟踪工作流实例生命周期的更改，例如已开始或已完成的事件。</span><span class="sxs-lookup"><span data-stu-id="81303-104">Represents a query that tracks workflow instance life cycle changes such as a started or completed event.</span></span>  
  
<span data-ttu-id="81303-105">有关跟踪配置文件查询的详细信息，请参阅 [跟踪配置文件](../../../windows-workflow-foundation/tracking-profiles.md)</span><span class="sxs-lookup"><span data-stu-id="81303-105">For more information on tracking profile queries, see [Tracking Profiles](../../../windows-workflow-foundation/tracking-profiles.md)</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<tracking>**](tracking-of-wcf.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<profiles>**\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<trackingProfile>**](trackingprofile-of-wcf.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<workflow>**](workflow-of-wcf.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<workflowInstanceQueries>**](workflowinstancequeries-of-wcf.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<workflowInstanceQuery>**  
  
## <a name="syntax"></a><span data-ttu-id="81303-106">语法</span><span class="sxs-lookup"><span data-stu-id="81303-106">Syntax</span></span>  
  
```xml  
<tracking>
  <profiles>
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
  </profiles>
</tracking>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="81303-107">特性和元素</span><span class="sxs-lookup"><span data-stu-id="81303-107">Attributes and elements</span></span>  

<span data-ttu-id="81303-108">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="81303-108">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="81303-109">特性</span><span class="sxs-lookup"><span data-stu-id="81303-109">Attributes</span></span>  

<span data-ttu-id="81303-110">无。</span><span class="sxs-lookup"><span data-stu-id="81303-110">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="81303-111">子元素</span><span class="sxs-lookup"><span data-stu-id="81303-111">Child elements</span></span>  
  
|<span data-ttu-id="81303-112">元素</span><span class="sxs-lookup"><span data-stu-id="81303-112">Element</span></span>|<span data-ttu-id="81303-113">说明</span><span class="sxs-lookup"><span data-stu-id="81303-113">Description</span></span>|  
|-------------|-----------------|  
|[\<states>](states-of-wcf-workflowinstancequery.md)|<span data-ttu-id="81303-114">创建跟踪记录时已跟踪工作流实例中已订阅状态的集合。</span><span class="sxs-lookup"><span data-stu-id="81303-114">A collection of subscribed states from the tracked workflow instance when the tracking records are created.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="81303-115">父元素</span><span class="sxs-lookup"><span data-stu-id="81303-115">Parent elements</span></span>  
  
|<span data-ttu-id="81303-116">元素</span><span class="sxs-lookup"><span data-stu-id="81303-116">Element</span></span>|<span data-ttu-id="81303-117">说明</span><span class="sxs-lookup"><span data-stu-id="81303-117">Description</span></span>|  
|-------------|-----------------|  
|[\<workflowInstanceQueries>](workflowinstancequeries-of-wcf.md)|<span data-ttu-id="81303-118">表示配置元素的集合，这些配置元素跟踪工作流实例生命周期的更改，例如已开始或已完成的事件。</span><span class="sxs-lookup"><span data-stu-id="81303-118">Represents a collection of configuration elements that track workflow instance life cycle changes such as a started or completed event.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="81303-119">备注</span><span class="sxs-lookup"><span data-stu-id="81303-119">Remarks</span></span>  

<span data-ttu-id="81303-120"><xref:System.Activities.Tracking.WorkflowInstanceQuery> 用于订阅以下 <xref:System.Activities.Tracking.TrackingRecord> 对象：</span><span class="sxs-lookup"><span data-stu-id="81303-120">The <xref:System.Activities.Tracking.WorkflowInstanceQuery> is used to subscribe to the following <xref:System.Activities.Tracking.TrackingRecord> objects:</span></span>  
  
- <xref:System.Activities.Tracking.WorkflowInstanceRecord>  
  
- <xref:System.Activities.Tracking.WorkflowInstanceAbortedRecord>  
  
- <xref:System.Activities.Tracking.WorkflowInstanceUnhandledExceptionRecord>  
  
- <xref:System.Activities.Tracking.WorkflowInstanceTerminatedRecord>  
  
- <xref:System.Activities.Tracking.WorkflowInstanceSuspendedRecord>  
  
## <a name="example"></a><span data-ttu-id="81303-121">示例</span><span class="sxs-lookup"><span data-stu-id="81303-121">Example</span></span>  

<span data-ttu-id="81303-122">下面的配置使用此查询订阅 `Started` 实例状态的工作流实例级跟踪记录。</span><span class="sxs-lookup"><span data-stu-id="81303-122">The following configuration subscribes to workflow instance-level tracking records for the `Started` instance state using this query.</span></span>  
  
```xml  
<workflowInstanceQueries>
  <workflowInstanceQuery>
    <states>
      <state name="Started" />
    </states>
  </workflowInstanceQuery>
</workflowInstanceQueries>
```  
  
## <a name="see-also"></a><span data-ttu-id="81303-123">请参阅</span><span class="sxs-lookup"><span data-stu-id="81303-123">See also</span></span>

- <xref:System.ServiceModel.Activities.Tracking.Configuration.WorkflowInstanceQueryElement?displayProperty=nameWithType>
- <xref:System.Activities.Tracking.WorkflowInstanceQuery?displayProperty=nameWithType>
- [<span data-ttu-id="81303-124">工作流跟踪</span><span class="sxs-lookup"><span data-stu-id="81303-124">Workflow Tracking and Tracing</span></span>](../../../windows-workflow-foundation/workflow-tracking-and-tracing.md)
- [<span data-ttu-id="81303-125">跟踪配置文件</span><span class="sxs-lookup"><span data-stu-id="81303-125">Tracking Profiles</span></span>](../../../windows-workflow-foundation/tracking-profiles.md)
