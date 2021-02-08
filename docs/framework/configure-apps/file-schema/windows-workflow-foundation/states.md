---
description: 了解详细信息： <states>
title: <states>
ms.date: 03/30/2017
ms.topic: reference
ms.assetid: ebea5e7c-ad58-43c5-8f2d-cca25ae1b721
ms.openlocfilehash: 9a66a1ce460db1f5f55fb99a191368635220f32f
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99781969"
---
# \<states>

<span data-ttu-id="34d73-102">表示创建跟踪记录时已跟踪工作流实例中已订阅状态的集合。</span><span class="sxs-lookup"><span data-stu-id="34d73-102">Represents a collection of subscribed states from the tracked workflow instance when the tracking records are created.</span></span>  
  
 <span data-ttu-id="34d73-103">有关跟踪配置文件查询的详细信息，请参阅 [跟踪配置文件](../../../windows-workflow-foundation/tracking-profiles.md)</span><span class="sxs-lookup"><span data-stu-id="34d73-103">For more information on tracking profile queries, see [Tracking Profiles](../../../windows-workflow-foundation/tracking-profiles.md)</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.ServiceModel>**](system-servicemodel-of-workflow.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<tracking>**](tracking.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<trackingProfile>**](trackingprofile.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<workflow>**](workflow.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<workflowInstanceQueries>**](workflowinstancequeries.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<workflowInstanceQuery>**](workflowinstancequery.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<states>**  
  
## <a name="syntax"></a><span data-ttu-id="34d73-104">语法</span><span class="sxs-lookup"><span data-stu-id="34d73-104">Syntax</span></span>  
  
```xml  
<tracking>
  <trackingProfile name="Name">
    <workflow>
      <workflowInstanceQueries>
        <workflowInstanceQuery>
          <states>
            <state name="Name"/>
          </states>
        </workflowInstanceQuery>
      </workflowInstanceQueries>
    </workflow>
  </trackingProfile>
</tracking>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="34d73-105">特性和元素</span><span class="sxs-lookup"><span data-stu-id="34d73-105">Attributes and Elements</span></span>  

 <span data-ttu-id="34d73-106">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="34d73-106">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="34d73-107">特性</span><span class="sxs-lookup"><span data-stu-id="34d73-107">Attributes</span></span>  

 <span data-ttu-id="34d73-108">无。</span><span class="sxs-lookup"><span data-stu-id="34d73-108">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="34d73-109">子元素</span><span class="sxs-lookup"><span data-stu-id="34d73-109">Child Elements</span></span>  
  
|<span data-ttu-id="34d73-110">元素</span><span class="sxs-lookup"><span data-stu-id="34d73-110">Element</span></span>|<span data-ttu-id="34d73-111">说明</span><span class="sxs-lookup"><span data-stu-id="34d73-111">Description</span></span>|  
|-------------|-----------------|  
|[\<state>](states.md)|<span data-ttu-id="34d73-112">创建跟踪记录时已跟踪工作流实例中的一个已订阅状态。</span><span class="sxs-lookup"><span data-stu-id="34d73-112">A subscribed state from the tracked workflow instance when the tracking record is created.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="34d73-113">父元素</span><span class="sxs-lookup"><span data-stu-id="34d73-113">Parent Elements</span></span>  
  
|<span data-ttu-id="34d73-114">元素</span><span class="sxs-lookup"><span data-stu-id="34d73-114">Element</span></span>|<span data-ttu-id="34d73-115">说明</span><span class="sxs-lookup"><span data-stu-id="34d73-115">Description</span></span>|  
|-------------|-----------------|  
|[\<workflowInstanceQuery>](workflowinstancequery.md)|<span data-ttu-id="34d73-116">一个查询，该查询跟踪工作流实例生命周期的更改，例如已开始或已完成的事件。</span><span class="sxs-lookup"><span data-stu-id="34d73-116">A query that tracks workflow instance life cycle changes such as a started or completed event.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="34d73-117">备注</span><span class="sxs-lookup"><span data-stu-id="34d73-117">Remarks</span></span>  

 <span data-ttu-id="34d73-118">返回的记录由此集合中的状态进行筛选。</span><span class="sxs-lookup"><span data-stu-id="34d73-118">The returned records are filtered by the states in this collection.</span></span>  
  
 <span data-ttu-id="34d73-119">下表中列出了可能的状态值。</span><span class="sxs-lookup"><span data-stu-id="34d73-119">Possible state values are described in the following table.</span></span>  
  
|<span data-ttu-id="34d73-120">状态</span><span class="sxs-lookup"><span data-stu-id="34d73-120">State</span></span>|<span data-ttu-id="34d73-121">说明</span><span class="sxs-lookup"><span data-stu-id="34d73-121">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="34d73-122">Aborted</span><span class="sxs-lookup"><span data-stu-id="34d73-122">Aborted</span></span>|<span data-ttu-id="34d73-123">工作流实例已中止。</span><span class="sxs-lookup"><span data-stu-id="34d73-123">The workflow instance is aborted.</span></span>|  
|<span data-ttu-id="34d73-124">已完成</span><span class="sxs-lookup"><span data-stu-id="34d73-124">Completed</span></span>|<span data-ttu-id="34d73-125">工作流实例已完成。</span><span class="sxs-lookup"><span data-stu-id="34d73-125">The workflow instance is completed.</span></span>|  
|<span data-ttu-id="34d73-126">Deleted</span><span class="sxs-lookup"><span data-stu-id="34d73-126">Deleted</span></span>|<span data-ttu-id="34d73-127">工作流实例已删除。</span><span class="sxs-lookup"><span data-stu-id="34d73-127">The workflow instance is deleted.</span></span>|  
|<span data-ttu-id="34d73-128">空闲</span><span class="sxs-lookup"><span data-stu-id="34d73-128">Idle</span></span>|<span data-ttu-id="34d73-129">工作流实例处于空闲状态。</span><span class="sxs-lookup"><span data-stu-id="34d73-129">The workflow instance is idle.</span></span>|  
|<span data-ttu-id="34d73-130">持久化</span><span class="sxs-lookup"><span data-stu-id="34d73-130">Persisted</span></span>|<span data-ttu-id="34d73-131">工作流实例已保留。</span><span class="sxs-lookup"><span data-stu-id="34d73-131">The workflow instance is persisted.</span></span>|  
|<span data-ttu-id="34d73-132">Resumed</span><span class="sxs-lookup"><span data-stu-id="34d73-132">Resumed</span></span>|<span data-ttu-id="34d73-133">工作流实例已恢复。</span><span class="sxs-lookup"><span data-stu-id="34d73-133">The workflow instance is resumed.</span></span>|  
|<span data-ttu-id="34d73-134">Started</span><span class="sxs-lookup"><span data-stu-id="34d73-134">Started</span></span>|<span data-ttu-id="34d73-135">工作流实例已启动。</span><span class="sxs-lookup"><span data-stu-id="34d73-135">The workflow instance is started.</span></span>|  
|<span data-ttu-id="34d73-136">UnhandledException</span><span class="sxs-lookup"><span data-stu-id="34d73-136">UnhandledException</span></span>|<span data-ttu-id="34d73-137">工作流实例遇到了未经处理的异常。</span><span class="sxs-lookup"><span data-stu-id="34d73-137">The workflow instance encountered an unhandled exception.</span></span>|  
|<span data-ttu-id="34d73-138">已卸载</span><span class="sxs-lookup"><span data-stu-id="34d73-138">Unloaded</span></span>|<span data-ttu-id="34d73-139">工作流实例已卸载。</span><span class="sxs-lookup"><span data-stu-id="34d73-139">The workflow instance is unloaded.</span></span>|  
|<span data-ttu-id="34d73-140">已取消</span><span class="sxs-lookup"><span data-stu-id="34d73-140">Canceled</span></span>|<span data-ttu-id="34d73-141">工作流实例已取消。</span><span class="sxs-lookup"><span data-stu-id="34d73-141">The workflow instance is canceled.</span></span>|  
|<span data-ttu-id="34d73-142">已挂起</span><span class="sxs-lookup"><span data-stu-id="34d73-142">Suspended</span></span>|<span data-ttu-id="34d73-143">工作流实例处于挂起状态。</span><span class="sxs-lookup"><span data-stu-id="34d73-143">The workflow instance is suspended.</span></span>|  
|<span data-ttu-id="34d73-144">终止</span><span class="sxs-lookup"><span data-stu-id="34d73-144">Terminated</span></span>|<span data-ttu-id="34d73-145">工作流实例已终止。</span><span class="sxs-lookup"><span data-stu-id="34d73-145">The workflow instance is terminated.</span></span>|  
|<span data-ttu-id="34d73-146">Unsuspended</span><span class="sxs-lookup"><span data-stu-id="34d73-146">Unsuspended</span></span>|<span data-ttu-id="34d73-147">工作流实例已取消挂起。</span><span class="sxs-lookup"><span data-stu-id="34d73-147">The workflow instance is unsuspended.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="34d73-148">示例</span><span class="sxs-lookup"><span data-stu-id="34d73-148">Example</span></span>  

 <span data-ttu-id="34d73-149">下面的配置使用此查询订阅 `Started` 实例状态的工作流实例级跟踪记录。</span><span class="sxs-lookup"><span data-stu-id="34d73-149">The following configuration subscribes to workflow instance-level tracking records for the `Started` instance state using this query.</span></span>  
  
```xml  
<workflowInstanceQueries>  
    <workflowInstanceQuery>  
      <states>  
        <state name="Started"/>  
      </states>  
    </workflowInstanceQuery>  
</workflowInstanceQueries>  
```  
  
## <a name="see-also"></a><span data-ttu-id="34d73-150">请参阅</span><span class="sxs-lookup"><span data-stu-id="34d73-150">See also</span></span>

- <xref:System.ServiceModel.Activities.Tracking.Configuration.WorkflowInstanceQueryElement?displayProperty=nameWithType>
- <xref:System.ServiceModel.Activities.Tracking.Configuration.StateElementCollection?displayProperty=nameWithType>
- <xref:System.Activities.Tracking.WorkflowInstanceQuery?displayProperty=nameWithType>
- [<span data-ttu-id="34d73-151">工作流跟踪</span><span class="sxs-lookup"><span data-stu-id="34d73-151">Workflow Tracking and Tracing</span></span>](../../../windows-workflow-foundation/workflow-tracking-and-tracing.md)
- [<span data-ttu-id="34d73-152">跟踪配置文件</span><span class="sxs-lookup"><span data-stu-id="34d73-152">Tracking Profiles</span></span>](../../../windows-workflow-foundation/tracking-profiles.md)
