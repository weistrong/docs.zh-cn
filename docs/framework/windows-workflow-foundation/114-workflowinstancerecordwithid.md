---
description: 了解详细信息： 114-WorkflowInstanceRecordWithId
title: 114 - WorkflowInstanceRecordWithId
ms.date: 03/30/2017
ms.assetid: 2bd8b4a1-b210-4c07-8156-f19392318c08
ms.openlocfilehash: 77d39cd91476d9de41bbb00b5df034fc79cdec08
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99667247"
---
# <a name="114---workflowinstancerecordwithid"></a><span data-ttu-id="08608-103">114 - WorkflowInstanceRecordWithId</span><span class="sxs-lookup"><span data-stu-id="08608-103">114 - WorkflowInstanceRecordWithId</span></span>

## <a name="properties"></a><span data-ttu-id="08608-104">属性</span><span class="sxs-lookup"><span data-stu-id="08608-104">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="08608-105">ID</span><span class="sxs-lookup"><span data-stu-id="08608-105">ID</span></span>|<span data-ttu-id="08608-106">114</span><span class="sxs-lookup"><span data-stu-id="08608-106">114</span></span>|  
|<span data-ttu-id="08608-107">关键字</span><span class="sxs-lookup"><span data-stu-id="08608-107">Keywords</span></span>|<span data-ttu-id="08608-108">HealthMonitoring、WFTracking</span><span class="sxs-lookup"><span data-stu-id="08608-108">HealthMonitoring, WFTracking</span></span>|  
|<span data-ttu-id="08608-109">级别</span><span class="sxs-lookup"><span data-stu-id="08608-109">Level</span></span>|<span data-ttu-id="08608-110">信息</span><span class="sxs-lookup"><span data-stu-id="08608-110">Information</span></span>|  
|<span data-ttu-id="08608-111">通道</span><span class="sxs-lookup"><span data-stu-id="08608-111">Channel</span></span>|<span data-ttu-id="08608-112">Microsoft-Windows-应用程序服务器-应用程序/分析</span><span class="sxs-lookup"><span data-stu-id="08608-112">Microsoft-Windows-Application Server-Applications/Analytic</span></span>|  
  
## <a name="description"></a><span data-ttu-id="08608-113">说明</span><span class="sxs-lookup"><span data-stu-id="08608-113">Description</span></span>  

 <span data-ttu-id="08608-114">工作流实例发出以下工作流状态的 WorkflowInstanceRecord 时，ETW 跟踪参与者将发出此事件：已启动、已继续、已持久保存、空闲、已删除、已完成、已取消、已卸载和已取消挂起。</span><span class="sxs-lookup"><span data-stu-id="08608-114">This event is emitted by the ETW tracking participant when a workflow instance emits WorkflowInstanceRecord for workflow states : Started, Resumed, Persisted, Idle, Deleted, Completed, Canceled, Unloaded, Unsuspended.</span></span>  
  
## <a name="message"></a><span data-ttu-id="08608-115">消息</span><span class="sxs-lookup"><span data-stu-id="08608-115">Message</span></span>  

 <span data-ttu-id="08608-116">TrackRecord= WorkflowInstanceRecord，InstanceID = %1，RecordNumber = %2，EventTime = %3，ActivityDefinitionId = %4，State = %5，Annotations = %6， ProfileName = %7，WorkflowDefinitionIdentity = %8</span><span class="sxs-lookup"><span data-stu-id="08608-116">TrackRecord= WorkflowInstanceRecord, InstanceID = %1, RecordNumber = %2, EventTime = %3, ActivityDefinitionId = %4, State = %5, Annotations = %6, ProfileName = %7, WorkflowDefinitionIdentity = %8</span></span>  
  
## <a name="details"></a><span data-ttu-id="08608-117">详细信息</span><span class="sxs-lookup"><span data-stu-id="08608-117">Details</span></span>  
  
|<span data-ttu-id="08608-118">数据项名称</span><span class="sxs-lookup"><span data-stu-id="08608-118">Data Item Name</span></span>|<span data-ttu-id="08608-119">数据项类型</span><span class="sxs-lookup"><span data-stu-id="08608-119">Data Item Type</span></span>|<span data-ttu-id="08608-120">说明</span><span class="sxs-lookup"><span data-stu-id="08608-120">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="08608-121">InstanceId</span><span class="sxs-lookup"><span data-stu-id="08608-121">InstanceId</span></span>|<span data-ttu-id="08608-122">xs:GUID</span><span class="sxs-lookup"><span data-stu-id="08608-122">xs:GUID</span></span>|<span data-ttu-id="08608-123">工作流的实例 ID</span><span class="sxs-lookup"><span data-stu-id="08608-123">The instance id for the workflow</span></span>|  
|<span data-ttu-id="08608-124">RecordNumber</span><span class="sxs-lookup"><span data-stu-id="08608-124">RecordNumber</span></span>|<span data-ttu-id="08608-125">xs:long</span><span class="sxs-lookup"><span data-stu-id="08608-125">xs:long</span></span>|<span data-ttu-id="08608-126">发出的记录的序列号</span><span class="sxs-lookup"><span data-stu-id="08608-126">The sequence number of the emitted record</span></span>|  
|<span data-ttu-id="08608-127">EventTime</span><span class="sxs-lookup"><span data-stu-id="08608-127">EventTime</span></span>|<span data-ttu-id="08608-128">xs:dateTime</span><span class="sxs-lookup"><span data-stu-id="08608-128">xs:dateTime</span></span>|<span data-ttu-id="08608-129">发出该事件时的 UTC 时间</span><span class="sxs-lookup"><span data-stu-id="08608-129">The time in UTC when the event was emitted</span></span>|  
|<span data-ttu-id="08608-130">ActivityDefinitionId</span><span class="sxs-lookup"><span data-stu-id="08608-130">ActivityDefinitionId</span></span>|<span data-ttu-id="08608-131">xs:string</span><span class="sxs-lookup"><span data-stu-id="08608-131">xs:string</span></span>|<span data-ttu-id="08608-132">工作流中根活动的名称</span><span class="sxs-lookup"><span data-stu-id="08608-132">The name of the root activity in the workflow</span></span>|  
|<span data-ttu-id="08608-133">状态</span><span class="sxs-lookup"><span data-stu-id="08608-133">State</span></span>|<span data-ttu-id="08608-134">xs:string</span><span class="sxs-lookup"><span data-stu-id="08608-134">xs:string</span></span>|<span data-ttu-id="08608-135">工作流的当前状态。</span><span class="sxs-lookup"><span data-stu-id="08608-135">The current state of the Workflow.</span></span>|  
|<span data-ttu-id="08608-136">批注</span><span class="sxs-lookup"><span data-stu-id="08608-136">Annotations</span></span>|<span data-ttu-id="08608-137">xs:string</span><span class="sxs-lookup"><span data-stu-id="08608-137">xs:string</span></span>|<span data-ttu-id="08608-138">已添加到此事件中的批注。</span><span class="sxs-lookup"><span data-stu-id="08608-138">The annotations that were added to this event.</span></span> <span data-ttu-id="08608-139">值存储在 xml 元素中，格式为 \<items> \< item name = "annotationName" type="System.String"> a \</item> \</items> 。</span><span class="sxs-lookup"><span data-stu-id="08608-139">The values are stored in an xml element in the format \<items>\< item name = "annotationName" type="System.String">annotationValue\</item>\</items>.</span></span> <span data-ttu-id="08608-140">如果未指定任何批注，则该字符串包含 \<items/> 。</span><span class="sxs-lookup"><span data-stu-id="08608-140">If no annotations are specified then the string contains \<items/>.</span></span> <span data-ttu-id="08608-141">ETW 事件大小受到 ETW 缓冲区大小或 ETW 事件最大负载的限制。</span><span class="sxs-lookup"><span data-stu-id="08608-141">The ETW event size is limited by the ETW buffer size or the max payload for an ETW event.</span></span> <span data-ttu-id="08608-142">如果事件的大小超过 ETW 限制，则通过删除批注并将批注值替换为 ... 来截断事件。 \<items> \</items></span><span class="sxs-lookup"><span data-stu-id="08608-142">If the size of the event exceeds the ETW limits, then the event is truncated by dropping the annotations and replacing the annotation value with \<items>...\</items>.</span></span>|  
|<span data-ttu-id="08608-143">ProfileName</span><span class="sxs-lookup"><span data-stu-id="08608-143">ProfileName</span></span>|<span data-ttu-id="08608-144">xs:string</span><span class="sxs-lookup"><span data-stu-id="08608-144">xs:string</span></span>|<span data-ttu-id="08608-145">导致发出此事件的跟踪配置文件的名称</span><span class="sxs-lookup"><span data-stu-id="08608-145">The name or the tracking profile that resulted in this event being emitted</span></span>|  
|<span data-ttu-id="08608-146">WorkflowDefinitionIdentity</span><span class="sxs-lookup"><span data-stu-id="08608-146">WorkflowDefinitionIdentity</span></span>|<span data-ttu-id="08608-147">xs:string</span><span class="sxs-lookup"><span data-stu-id="08608-147">xs:string</span></span>|<span data-ttu-id="08608-148">工作流定义 ID</span><span class="sxs-lookup"><span data-stu-id="08608-148">The workflow definition id</span></span>|  
|<span data-ttu-id="08608-149">应用程序域</span><span class="sxs-lookup"><span data-stu-id="08608-149">AppDomain</span></span>|<span data-ttu-id="08608-150">xs:string</span><span class="sxs-lookup"><span data-stu-id="08608-150">xs:string</span></span>|<span data-ttu-id="08608-151">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="08608-151">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
