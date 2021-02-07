---
description: 了解详细信息： 116-WorkflowInstanceSuspendedRecordWithId
title: 116 - WorkflowInstanceSuspendedRecordWithId
ms.date: 03/30/2017
ms.assetid: 38232c03-6139-4494-a020-79bc83eb9dce
ms.openlocfilehash: 32746777d32ed0c8320d53da9f73ddb8d55a5573
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99703245"
---
# <a name="116---workflowinstancesuspendedrecordwithid"></a><span data-ttu-id="9a84e-103">116 - WorkflowInstanceSuspendedRecordWithId</span><span class="sxs-lookup"><span data-stu-id="9a84e-103">116 - WorkflowInstanceSuspendedRecordWithId</span></span>

## <a name="properties"></a><span data-ttu-id="9a84e-104">属性</span><span class="sxs-lookup"><span data-stu-id="9a84e-104">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="9a84e-105">ID</span><span class="sxs-lookup"><span data-stu-id="9a84e-105">ID</span></span>|<span data-ttu-id="9a84e-106">116</span><span class="sxs-lookup"><span data-stu-id="9a84e-106">116</span></span>|  
|<span data-ttu-id="9a84e-107">关键字</span><span class="sxs-lookup"><span data-stu-id="9a84e-107">Keywords</span></span>|<span data-ttu-id="9a84e-108">HealthMonitoring、WFTracking</span><span class="sxs-lookup"><span data-stu-id="9a84e-108">HealthMonitoring, WFTracking</span></span>|  
|<span data-ttu-id="9a84e-109">级别</span><span class="sxs-lookup"><span data-stu-id="9a84e-109">Level</span></span>|<span data-ttu-id="9a84e-110">信息</span><span class="sxs-lookup"><span data-stu-id="9a84e-110">Information</span></span>|  
|<span data-ttu-id="9a84e-111">通道</span><span class="sxs-lookup"><span data-stu-id="9a84e-111">Channel</span></span>|<span data-ttu-id="9a84e-112">Microsoft-Windows-应用程序服务器-应用程序/分析</span><span class="sxs-lookup"><span data-stu-id="9a84e-112">Microsoft-Windows-Application Server-Applications/Analytic</span></span>|  
  
## <a name="description"></a><span data-ttu-id="9a84e-113">说明</span><span class="sxs-lookup"><span data-stu-id="9a84e-113">Description</span></span>  

 <span data-ttu-id="9a84e-114">当工作流实例发出 WorkflowInstanceSuspended Record 时，ETW 跟踪参与者将发出此事件。</span><span class="sxs-lookup"><span data-stu-id="9a84e-114">This event is emitted by the ETW tracking participant when a workflow instance emits WorkflowInstanceSuspended Record.</span></span>  
  
## <a name="message"></a><span data-ttu-id="9a84e-115">消息</span><span class="sxs-lookup"><span data-stu-id="9a84e-115">Message</span></span>  

 <span data-ttu-id="9a84e-116">TrackRecord = WorkflowInstanceSuspendedRecord，InstanceID = %1，RecordNumber = %2，EventTime = %3，ActivityDefinitionId = %4，Reason = %5，Annotations = %6，ProfileName = %7，WorkflowDefinitionIdentity = %8</span><span class="sxs-lookup"><span data-stu-id="9a84e-116">TrackRecord = WorkflowInstanceSuspendedRecord, InstanceID = %1, RecordNumber = %2, EventTime = %3, ActivityDefinitionId = %4, Reason = %5, Annotations = %6, ProfileName = %7, WorkflowDefinitionIdentity = %8</span></span>  
  
## <a name="details"></a><span data-ttu-id="9a84e-117">详细信息</span><span class="sxs-lookup"><span data-stu-id="9a84e-117">Details</span></span>  
  
|<span data-ttu-id="9a84e-118">数据项名称</span><span class="sxs-lookup"><span data-stu-id="9a84e-118">Data Item Name</span></span>|<span data-ttu-id="9a84e-119">数据项类型</span><span class="sxs-lookup"><span data-stu-id="9a84e-119">Data Item Type</span></span>|<span data-ttu-id="9a84e-120">说明</span><span class="sxs-lookup"><span data-stu-id="9a84e-120">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="9a84e-121">InstanceId</span><span class="sxs-lookup"><span data-stu-id="9a84e-121">InstanceId</span></span>|<span data-ttu-id="9a84e-122">xs:GUID</span><span class="sxs-lookup"><span data-stu-id="9a84e-122">xs:GUID</span></span>|<span data-ttu-id="9a84e-123">工作流的实例 ID</span><span class="sxs-lookup"><span data-stu-id="9a84e-123">The instance id for the workflow</span></span>|  
|<span data-ttu-id="9a84e-124">RecordNumber</span><span class="sxs-lookup"><span data-stu-id="9a84e-124">RecordNumber</span></span>|<span data-ttu-id="9a84e-125">xs:long</span><span class="sxs-lookup"><span data-stu-id="9a84e-125">xs:long</span></span>|<span data-ttu-id="9a84e-126">发出的记录的序列号</span><span class="sxs-lookup"><span data-stu-id="9a84e-126">The sequence number of the emitted record</span></span>|  
|<span data-ttu-id="9a84e-127">EventTime</span><span class="sxs-lookup"><span data-stu-id="9a84e-127">EventTime</span></span>|<span data-ttu-id="9a84e-128">xs:dateTime</span><span class="sxs-lookup"><span data-stu-id="9a84e-128">xs:dateTime</span></span>|<span data-ttu-id="9a84e-129">发出该事件时的 UTC 时间</span><span class="sxs-lookup"><span data-stu-id="9a84e-129">The time in UTC when the event was emitted</span></span>|  
|<span data-ttu-id="9a84e-130">ActivityDefinitionId</span><span class="sxs-lookup"><span data-stu-id="9a84e-130">ActivityDefinitionId</span></span>|<span data-ttu-id="9a84e-131">xs:string</span><span class="sxs-lookup"><span data-stu-id="9a84e-131">xs:string</span></span>|<span data-ttu-id="9a84e-132">工作流中根活动的名称</span><span class="sxs-lookup"><span data-stu-id="9a84e-132">The name of the root activity in the workflow</span></span>|  
|<span data-ttu-id="9a84e-133">状态</span><span class="sxs-lookup"><span data-stu-id="9a84e-133">State</span></span>|<span data-ttu-id="9a84e-134">xs:string</span><span class="sxs-lookup"><span data-stu-id="9a84e-134">xs:string</span></span>|<span data-ttu-id="9a84e-135">工作流的当前状态。</span><span class="sxs-lookup"><span data-stu-id="9a84e-135">The current state of the Workflow.</span></span>|  
|<span data-ttu-id="9a84e-136">批注</span><span class="sxs-lookup"><span data-stu-id="9a84e-136">Annotations</span></span>|<span data-ttu-id="9a84e-137">xs:string</span><span class="sxs-lookup"><span data-stu-id="9a84e-137">xs:string</span></span>|<span data-ttu-id="9a84e-138">已添加到此事件中的批注。</span><span class="sxs-lookup"><span data-stu-id="9a84e-138">The annotations that were added to this event.</span></span> <span data-ttu-id="9a84e-139">值存储在 xml 元素中，格式为 \<items> \< item name = "annotationName" type="System.String"> a \</item> \</items> 。</span><span class="sxs-lookup"><span data-stu-id="9a84e-139">The values are stored in an xml element in the format \<items>\< item name = "annotationName" type="System.String">annotationValue\</item>\</items>.</span></span> <span data-ttu-id="9a84e-140">如果未指定任何批注，则该字符串包含 \<items/> 。</span><span class="sxs-lookup"><span data-stu-id="9a84e-140">If no annotations are specified then the string contains \<items/>.</span></span> <span data-ttu-id="9a84e-141">ETW 事件大小受到 ETW 缓冲区大小或 ETW 事件最大负载的限制。</span><span class="sxs-lookup"><span data-stu-id="9a84e-141">The ETW event size is limited by the ETW buffer size or the max payload for an ETW event.</span></span> <span data-ttu-id="9a84e-142">如果事件的大小超过 ETW 限制，则通过删除批注并将批注值替换为 ... 来截断事件。 \<items> \</items></span><span class="sxs-lookup"><span data-stu-id="9a84e-142">If the size of the event exceeds the ETW limits, then the event is truncated by dropping the annotations and replacing the annotation value with \<items>...\</items>.</span></span>|  
|<span data-ttu-id="9a84e-143">ProfileName</span><span class="sxs-lookup"><span data-stu-id="9a84e-143">ProfileName</span></span>|<span data-ttu-id="9a84e-144">xs:string</span><span class="sxs-lookup"><span data-stu-id="9a84e-144">xs:string</span></span>|<span data-ttu-id="9a84e-145">导致发出此事件的跟踪配置文件的名称</span><span class="sxs-lookup"><span data-stu-id="9a84e-145">The name or the tracking profile that resulted in this event being emitted</span></span>|  
|<span data-ttu-id="9a84e-146">WorkflowDefinitionIdentity</span><span class="sxs-lookup"><span data-stu-id="9a84e-146">WorkflowDefinitionIdentity</span></span>|<span data-ttu-id="9a84e-147">xs:string</span><span class="sxs-lookup"><span data-stu-id="9a84e-147">xs:string</span></span>|<span data-ttu-id="9a84e-148">工作流定义 ID</span><span class="sxs-lookup"><span data-stu-id="9a84e-148">The workflow definition id</span></span>|  
|<span data-ttu-id="9a84e-149">应用程序域</span><span class="sxs-lookup"><span data-stu-id="9a84e-149">AppDomain</span></span>|<span data-ttu-id="9a84e-150">xs:string</span><span class="sxs-lookup"><span data-stu-id="9a84e-150">xs:string</span></span>|<span data-ttu-id="9a84e-151">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="9a84e-151">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
