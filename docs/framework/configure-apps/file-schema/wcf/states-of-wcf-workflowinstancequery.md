---
description: 了解有关 WCF 的详细信息： <states><workflowInstanceQuery>
title: <states> WCF， <workflowInstanceQuery>
ms.date: 03/30/2017
ms.assetid: d17f7525-8035-4e9e-85a0-4cddae59f85d
ms.openlocfilehash: 66b3008b352d1f76c30aab9a0ec038836f33d408
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99786637"
---
# <a name="states-of-wcf-workflowinstancequery"></a><span data-ttu-id="7fb50-103">\<states> WCF， \<workflowInstanceQuery></span><span class="sxs-lookup"><span data-stu-id="7fb50-103">\<states> of WCF, \<workflowInstanceQuery></span></span>

<span data-ttu-id="7fb50-104">表示创建跟踪记录时已跟踪工作流实例中已订阅状态的集合。</span><span class="sxs-lookup"><span data-stu-id="7fb50-104">Represents a collection of subscribed states from the tracked workflow instance when the tracking records are created.</span></span>  
  
<span data-ttu-id="7fb50-105">有关跟踪配置文件查询的详细信息，请参阅 [跟踪配置文件](../../../windows-workflow-foundation/tracking-profiles.md)</span><span class="sxs-lookup"><span data-stu-id="7fb50-105">For more information on tracking profile queries, see [Tracking Profiles](../../../windows-workflow-foundation/tracking-profiles.md)</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<tracking>**](tracking-of-wcf.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<profiles>**\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<trackingProfile>**](trackingprofile-of-wcf.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<workflow>**](workflow-of-wcf.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<workflowInstanceQueries>**](workflowinstancequeries-of-wcf.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<workflowInstanceQuery>**](workflowinstancequery-of-wcf.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<states>**  
  
## <a name="syntax"></a><span data-ttu-id="7fb50-106">语法</span><span class="sxs-lookup"><span data-stu-id="7fb50-106">Syntax</span></span>  
  
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
  
## <a name="attributes-and-elements"></a><span data-ttu-id="7fb50-107">特性和元素</span><span class="sxs-lookup"><span data-stu-id="7fb50-107">Attributes and elements</span></span>

<span data-ttu-id="7fb50-108">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="7fb50-108">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="7fb50-109">特性</span><span class="sxs-lookup"><span data-stu-id="7fb50-109">Attributes</span></span>  

<span data-ttu-id="7fb50-110">无。</span><span class="sxs-lookup"><span data-stu-id="7fb50-110">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="7fb50-111">子元素</span><span class="sxs-lookup"><span data-stu-id="7fb50-111">Child elements</span></span>
  
|<span data-ttu-id="7fb50-112">元素</span><span class="sxs-lookup"><span data-stu-id="7fb50-112">Element</span></span>|<span data-ttu-id="7fb50-113">说明</span><span class="sxs-lookup"><span data-stu-id="7fb50-113">Description</span></span>|  
|-------------|-----------------|  
|[\<states>](state-of-wcf-workflowinstancequery.md)|<span data-ttu-id="7fb50-114">创建跟踪记录时已跟踪工作流实例中的一个已订阅状态。</span><span class="sxs-lookup"><span data-stu-id="7fb50-114">A subscribed state from the tracked workflow instance when the tracking record is created.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="7fb50-115">父元素</span><span class="sxs-lookup"><span data-stu-id="7fb50-115">Parent elements</span></span>  
  
|<span data-ttu-id="7fb50-116">元素</span><span class="sxs-lookup"><span data-stu-id="7fb50-116">Element</span></span>|<span data-ttu-id="7fb50-117">说明</span><span class="sxs-lookup"><span data-stu-id="7fb50-117">Description</span></span>|  
|-------------|-----------------|  
|[\<workflowInstanceQuery>](../windows-workflow-foundation/workflowinstancequery.md)|<span data-ttu-id="7fb50-118">一个查询，该查询跟踪工作流实例生命周期的更改，例如已开始或已完成的事件。</span><span class="sxs-lookup"><span data-stu-id="7fb50-118">A query that tracks workflow instance life cycle changes such as a started or completed event.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="7fb50-119">备注</span><span class="sxs-lookup"><span data-stu-id="7fb50-119">Remarks</span></span>

<span data-ttu-id="7fb50-120">返回的记录由此集合中的状态进行筛选。</span><span class="sxs-lookup"><span data-stu-id="7fb50-120">The returned records are filtered by the states in this collection.</span></span>  
  
<span data-ttu-id="7fb50-121">下表中列出了可能的状态值。</span><span class="sxs-lookup"><span data-stu-id="7fb50-121">Possible state values are described in the following table.</span></span>  
  
|<span data-ttu-id="7fb50-122">状态</span><span class="sxs-lookup"><span data-stu-id="7fb50-122">State</span></span>|<span data-ttu-id="7fb50-123">说明</span><span class="sxs-lookup"><span data-stu-id="7fb50-123">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="7fb50-124">Aborted</span><span class="sxs-lookup"><span data-stu-id="7fb50-124">Aborted</span></span>|<span data-ttu-id="7fb50-125">工作流实例已中止。</span><span class="sxs-lookup"><span data-stu-id="7fb50-125">The workflow instance is aborted.</span></span>|  
|<span data-ttu-id="7fb50-126">已完成</span><span class="sxs-lookup"><span data-stu-id="7fb50-126">Completed</span></span>|<span data-ttu-id="7fb50-127">工作流实例已完成。</span><span class="sxs-lookup"><span data-stu-id="7fb50-127">The workflow instance is completed.</span></span>|  
|<span data-ttu-id="7fb50-128">Deleted</span><span class="sxs-lookup"><span data-stu-id="7fb50-128">Deleted</span></span>|<span data-ttu-id="7fb50-129">工作流实例已删除。</span><span class="sxs-lookup"><span data-stu-id="7fb50-129">The workflow instance is deleted.</span></span>|  
|<span data-ttu-id="7fb50-130">空闲</span><span class="sxs-lookup"><span data-stu-id="7fb50-130">Idle</span></span>|<span data-ttu-id="7fb50-131">工作流实例处于空闲状态。</span><span class="sxs-lookup"><span data-stu-id="7fb50-131">The workflow instance is idle.</span></span>|  
|<span data-ttu-id="7fb50-132">持久化</span><span class="sxs-lookup"><span data-stu-id="7fb50-132">Persisted</span></span>|<span data-ttu-id="7fb50-133">工作流实例已保留。</span><span class="sxs-lookup"><span data-stu-id="7fb50-133">The workflow instance is persisted.</span></span>|  
|<span data-ttu-id="7fb50-134">Resumed</span><span class="sxs-lookup"><span data-stu-id="7fb50-134">Resumed</span></span>|<span data-ttu-id="7fb50-135">工作流实例已恢复。</span><span class="sxs-lookup"><span data-stu-id="7fb50-135">The workflow instance is resumed.</span></span>|  
|<span data-ttu-id="7fb50-136">Started</span><span class="sxs-lookup"><span data-stu-id="7fb50-136">Started</span></span>|<span data-ttu-id="7fb50-137">工作流实例已启动。</span><span class="sxs-lookup"><span data-stu-id="7fb50-137">The workflow instance is started.</span></span>|  
|<span data-ttu-id="7fb50-138">UnhandledException</span><span class="sxs-lookup"><span data-stu-id="7fb50-138">UnhandledException</span></span>|<span data-ttu-id="7fb50-139">工作流实例遇到了未经处理的异常。</span><span class="sxs-lookup"><span data-stu-id="7fb50-139">The workflow instance encountered an unhandled exception.</span></span>|  
|<span data-ttu-id="7fb50-140">已卸载</span><span class="sxs-lookup"><span data-stu-id="7fb50-140">Unloaded</span></span>|<span data-ttu-id="7fb50-141">工作流实例已卸载。</span><span class="sxs-lookup"><span data-stu-id="7fb50-141">The workflow instance is unloaded.</span></span>|  
|<span data-ttu-id="7fb50-142">已取消</span><span class="sxs-lookup"><span data-stu-id="7fb50-142">Canceled</span></span>|<span data-ttu-id="7fb50-143">工作流实例已取消。</span><span class="sxs-lookup"><span data-stu-id="7fb50-143">The workflow instance is canceled.</span></span>|  
|<span data-ttu-id="7fb50-144">已挂起</span><span class="sxs-lookup"><span data-stu-id="7fb50-144">Suspended</span></span>|<span data-ttu-id="7fb50-145">工作流实例处于挂起状态。</span><span class="sxs-lookup"><span data-stu-id="7fb50-145">The workflow instance is suspended.</span></span>|  
|<span data-ttu-id="7fb50-146">终止</span><span class="sxs-lookup"><span data-stu-id="7fb50-146">Terminated</span></span>|<span data-ttu-id="7fb50-147">工作流实例已终止。</span><span class="sxs-lookup"><span data-stu-id="7fb50-147">The workflow instance is terminated.</span></span>|  
|<span data-ttu-id="7fb50-148">Unsuspended</span><span class="sxs-lookup"><span data-stu-id="7fb50-148">Unsuspended</span></span>|<span data-ttu-id="7fb50-149">工作流实例已取消挂起。</span><span class="sxs-lookup"><span data-stu-id="7fb50-149">The workflow instance is unsuspended.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="7fb50-150">示例</span><span class="sxs-lookup"><span data-stu-id="7fb50-150">Example</span></span>

<span data-ttu-id="7fb50-151">下面的配置使用此查询订阅 `Started` 实例状态的工作流实例级跟踪记录。</span><span class="sxs-lookup"><span data-stu-id="7fb50-151">The following configuration subscribes to workflow instance-level tracking records for the `Started` instance state using this query.</span></span>  
  
```xml  
<workflowInstanceQueries>
  <workflowInstanceQuery>
    <states>
      <state name="Started" />
    </states>
  </workflowInstanceQuery>
</workflowInstanceQueries>
```  
  
## <a name="see-also"></a><span data-ttu-id="7fb50-152">请参阅</span><span class="sxs-lookup"><span data-stu-id="7fb50-152">See also</span></span>

- <xref:System.ServiceModel.Activities.Tracking.Configuration.WorkflowInstanceQueryElement?displayProperty=nameWithType>
- <xref:System.ServiceModel.Activities.Tracking.Configuration.StateElementCollection?displayProperty=nameWithType>
- <xref:System.Activities.Tracking.WorkflowInstanceQuery?displayProperty=nameWithType>
- [<span data-ttu-id="7fb50-153">工作流跟踪</span><span class="sxs-lookup"><span data-stu-id="7fb50-153">Workflow Tracking and Tracing</span></span>](../../../windows-workflow-foundation/workflow-tracking-and-tracing.md)
- [<span data-ttu-id="7fb50-154">跟踪配置文件</span><span class="sxs-lookup"><span data-stu-id="7fb50-154">Tracking Profiles</span></span>](../../../windows-workflow-foundation/tracking-profiles.md)
