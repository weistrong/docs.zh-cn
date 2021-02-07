---
description: 了解详细信息： <state>
title: <state>
ms.date: 03/30/2017
ms.topic: reference
ms.assetid: 619414f2-61c2-4427-9977-d05009e343db
ms.openlocfilehash: c04ba8a791d08e65337ffc28cd86f5a4a6af150f
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99729753"
---
# \<state>

<span data-ttu-id="2e3ca-102">表示创建跟踪记录时已跟踪工作流实例中已订阅状态的集合。</span><span class="sxs-lookup"><span data-stu-id="2e3ca-102">Represents a collection of subscribed states from the tracked workflow instance when the tracking records are created.</span></span>  
  
 <span data-ttu-id="2e3ca-103">有关跟踪配置文件查询的详细信息，请参阅 [跟踪配置文件](../../../windows-workflow-foundation/tracking-profiles.md)</span><span class="sxs-lookup"><span data-stu-id="2e3ca-103">For more information on tracking profile queries, see [Tracking Profiles](../../../windows-workflow-foundation/tracking-profiles.md)</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.ServiceModel>**](system-servicemodel-of-workflow.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<tracking>**](tracking.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<trackingProfile>**](trackingprofile.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<workflow>**](workflow.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<workflowInstanceQueries>**](workflowinstancequeries.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<workflowInstanceQuery>**](workflowinstancequery.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<states>**](states.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<state>**  
  
## <a name="syntax"></a><span data-ttu-id="2e3ca-104">语法</span><span class="sxs-lookup"><span data-stu-id="2e3ca-104">Syntax</span></span>  
  
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
  
## <a name="attributes-and-elements"></a><span data-ttu-id="2e3ca-105">特性和元素</span><span class="sxs-lookup"><span data-stu-id="2e3ca-105">Attributes and Elements</span></span>  

 <span data-ttu-id="2e3ca-106">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="2e3ca-106">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="2e3ca-107">特性</span><span class="sxs-lookup"><span data-stu-id="2e3ca-107">Attributes</span></span>  
  
|<span data-ttu-id="2e3ca-108">属性</span><span class="sxs-lookup"><span data-stu-id="2e3ca-108">Attribute</span></span>|<span data-ttu-id="2e3ca-109">说明</span><span class="sxs-lookup"><span data-stu-id="2e3ca-109">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="2e3ca-110">name</span><span class="sxs-lookup"><span data-stu-id="2e3ca-110">name</span></span>|<span data-ttu-id="2e3ca-111">一个字符串，指定创建跟踪记录时已跟踪工作流实例中的已订阅状态。</span><span class="sxs-lookup"><span data-stu-id="2e3ca-111">A string that specifies a subscribed state from the tracked workflow instance when the tracking record is created.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="2e3ca-112">子元素</span><span class="sxs-lookup"><span data-stu-id="2e3ca-112">Child Elements</span></span>  

 <span data-ttu-id="2e3ca-113">无。</span><span class="sxs-lookup"><span data-stu-id="2e3ca-113">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="2e3ca-114">父元素</span><span class="sxs-lookup"><span data-stu-id="2e3ca-114">Parent Elements</span></span>  
  
|<span data-ttu-id="2e3ca-115">元素</span><span class="sxs-lookup"><span data-stu-id="2e3ca-115">Element</span></span>|<span data-ttu-id="2e3ca-116">说明</span><span class="sxs-lookup"><span data-stu-id="2e3ca-116">Description</span></span>|  
|-------------|-----------------|  
|[\<states>](states.md)|<span data-ttu-id="2e3ca-117">创建跟踪记录时已跟踪工作流实例中已订阅状态的集合。</span><span class="sxs-lookup"><span data-stu-id="2e3ca-117">A collection of subscribed states from the tracked workflow instance when the tracking records are created.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="2e3ca-118">备注</span><span class="sxs-lookup"><span data-stu-id="2e3ca-118">Remarks</span></span>  

 <span data-ttu-id="2e3ca-119">返回的记录由此集合中的状态进行筛选。</span><span class="sxs-lookup"><span data-stu-id="2e3ca-119">The returned records are filtered by the states in this collection.</span></span>  
  
 <span data-ttu-id="2e3ca-120">下表中列出了可能的状态值。</span><span class="sxs-lookup"><span data-stu-id="2e3ca-120">Possible state values are described in the following table.</span></span>  
  
|<span data-ttu-id="2e3ca-121">状态</span><span class="sxs-lookup"><span data-stu-id="2e3ca-121">State</span></span>|<span data-ttu-id="2e3ca-122">说明</span><span class="sxs-lookup"><span data-stu-id="2e3ca-122">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="2e3ca-123">Aborted</span><span class="sxs-lookup"><span data-stu-id="2e3ca-123">Aborted</span></span>|<span data-ttu-id="2e3ca-124">工作流实例已中止。</span><span class="sxs-lookup"><span data-stu-id="2e3ca-124">The workflow instance is aborted.</span></span>|  
|<span data-ttu-id="2e3ca-125">已完成</span><span class="sxs-lookup"><span data-stu-id="2e3ca-125">Completed</span></span>|<span data-ttu-id="2e3ca-126">工作流实例已完成。</span><span class="sxs-lookup"><span data-stu-id="2e3ca-126">The workflow instance is completed.</span></span>|  
|<span data-ttu-id="2e3ca-127">Deleted</span><span class="sxs-lookup"><span data-stu-id="2e3ca-127">Deleted</span></span>|<span data-ttu-id="2e3ca-128">工作流实例已删除。</span><span class="sxs-lookup"><span data-stu-id="2e3ca-128">The workflow instance is deleted.</span></span>|  
|<span data-ttu-id="2e3ca-129">空闲</span><span class="sxs-lookup"><span data-stu-id="2e3ca-129">Idle</span></span>|<span data-ttu-id="2e3ca-130">工作流实例处于空闲状态。</span><span class="sxs-lookup"><span data-stu-id="2e3ca-130">The workflow instance is idle.</span></span>|  
|<span data-ttu-id="2e3ca-131">持久化</span><span class="sxs-lookup"><span data-stu-id="2e3ca-131">Persisted</span></span>|<span data-ttu-id="2e3ca-132">工作流实例已保留。</span><span class="sxs-lookup"><span data-stu-id="2e3ca-132">The workflow instance is persisted.</span></span>|  
|<span data-ttu-id="2e3ca-133">Resumed</span><span class="sxs-lookup"><span data-stu-id="2e3ca-133">Resumed</span></span>|<span data-ttu-id="2e3ca-134">工作流实例已恢复。</span><span class="sxs-lookup"><span data-stu-id="2e3ca-134">The workflow instance is resumed.</span></span>|  
|<span data-ttu-id="2e3ca-135">Started</span><span class="sxs-lookup"><span data-stu-id="2e3ca-135">Started</span></span>|<span data-ttu-id="2e3ca-136">工作流实例已启动。</span><span class="sxs-lookup"><span data-stu-id="2e3ca-136">The workflow instance is started.</span></span>|  
|<span data-ttu-id="2e3ca-137">UnhandledException</span><span class="sxs-lookup"><span data-stu-id="2e3ca-137">UnhandledException</span></span>|<span data-ttu-id="2e3ca-138">工作流实例遇到了未经处理的异常。</span><span class="sxs-lookup"><span data-stu-id="2e3ca-138">The workflow instance encountered an unhandled exception.</span></span>|  
|<span data-ttu-id="2e3ca-139">已卸载</span><span class="sxs-lookup"><span data-stu-id="2e3ca-139">Unloaded</span></span>|<span data-ttu-id="2e3ca-140">工作流实例已卸载。</span><span class="sxs-lookup"><span data-stu-id="2e3ca-140">The workflow instance is unloaded.</span></span>|  
|<span data-ttu-id="2e3ca-141">已取消</span><span class="sxs-lookup"><span data-stu-id="2e3ca-141">Canceled</span></span>|<span data-ttu-id="2e3ca-142">工作流实例已取消。</span><span class="sxs-lookup"><span data-stu-id="2e3ca-142">The workflow instance is canceled.</span></span>|  
|<span data-ttu-id="2e3ca-143">已挂起</span><span class="sxs-lookup"><span data-stu-id="2e3ca-143">Suspended</span></span>|<span data-ttu-id="2e3ca-144">工作流实例处于挂起状态。</span><span class="sxs-lookup"><span data-stu-id="2e3ca-144">The workflow instance is suspended.</span></span>|  
|<span data-ttu-id="2e3ca-145">终止</span><span class="sxs-lookup"><span data-stu-id="2e3ca-145">Terminated</span></span>|<span data-ttu-id="2e3ca-146">工作流实例已终止。</span><span class="sxs-lookup"><span data-stu-id="2e3ca-146">The workflow instance is terminated.</span></span>|  
|<span data-ttu-id="2e3ca-147">Unsuspended</span><span class="sxs-lookup"><span data-stu-id="2e3ca-147">Unsuspended</span></span>|<span data-ttu-id="2e3ca-148">工作流实例已取消挂起。</span><span class="sxs-lookup"><span data-stu-id="2e3ca-148">The workflow instance is unsuspended.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="2e3ca-149">示例</span><span class="sxs-lookup"><span data-stu-id="2e3ca-149">Example</span></span>  

 <span data-ttu-id="2e3ca-150">下面的配置使用此查询订阅 `Started` 实例状态的工作流实例级跟踪记录。</span><span class="sxs-lookup"><span data-stu-id="2e3ca-150">The following configuration subscribes to workflow instance-level tracking records for the `Started` instance state using this query.</span></span>  
  
```xml  
<workflowInstanceQueries>  
    <workflowInstanceQuery>  
      <states>  
        <state name="Started"/>  
      </states>  
    </workflowInstanceQuery>  
</workflowInstanceQueries>  
```  
  
## <a name="see-also"></a><span data-ttu-id="2e3ca-151">请参阅</span><span class="sxs-lookup"><span data-stu-id="2e3ca-151">See also</span></span>

- <xref:System.ServiceModel.Activities.Tracking.Configuration.WorkflowInstanceQueryElement?displayProperty=nameWithType>
- <xref:System.ServiceModel.Activities.Tracking.Configuration.StateElement?displayProperty=nameWithType>
- <xref:System.Activities.Tracking.WorkflowInstanceQuery?displayProperty=nameWithType>
- [<span data-ttu-id="2e3ca-152">工作流跟踪</span><span class="sxs-lookup"><span data-stu-id="2e3ca-152">Workflow Tracking and Tracing</span></span>](../../../windows-workflow-foundation/workflow-tracking-and-tracing.md)
- [<span data-ttu-id="2e3ca-153">跟踪配置文件</span><span class="sxs-lookup"><span data-stu-id="2e3ca-153">Tracking Profiles</span></span>](../../../windows-workflow-foundation/tracking-profiles.md)
