---
description: 了解详细信息： 1014-ScheduleCompletionWorkItem
title: 1014 - ScheduleCompletionWorkItem
ms.date: 03/30/2017
ms.assetid: 84203735-478d-42d8-a320-c175dbddcb38
ms.openlocfilehash: 85bbd9b749c1dd34d026d90d708ea7f880665fbb
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99792929"
---
# <a name="1014---schedulecompletionworkitem"></a><span data-ttu-id="753b1-103">1014 - ScheduleCompletionWorkItem</span><span class="sxs-lookup"><span data-stu-id="753b1-103">1014 - ScheduleCompletionWorkItem</span></span>

## <a name="properties"></a><span data-ttu-id="753b1-104">属性</span><span class="sxs-lookup"><span data-stu-id="753b1-104">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="753b1-105">ID</span><span class="sxs-lookup"><span data-stu-id="753b1-105">ID</span></span>|<span data-ttu-id="753b1-106">1014</span><span class="sxs-lookup"><span data-stu-id="753b1-106">1014</span></span>|  
|<span data-ttu-id="753b1-107">关键字</span><span class="sxs-lookup"><span data-stu-id="753b1-107">Keywords</span></span>|<span data-ttu-id="753b1-108">WFRuntime</span><span class="sxs-lookup"><span data-stu-id="753b1-108">WFRuntime</span></span>|  
|<span data-ttu-id="753b1-109">级别</span><span class="sxs-lookup"><span data-stu-id="753b1-109">Level</span></span>|<span data-ttu-id="753b1-110">“详细”</span><span class="sxs-lookup"><span data-stu-id="753b1-110">Verbose</span></span>|  
|<span data-ttu-id="753b1-111">通道</span><span class="sxs-lookup"><span data-stu-id="753b1-111">Channel</span></span>|<span data-ttu-id="753b1-112">Microsoft-Windows-应用程序服务器-应用程序/调试</span><span class="sxs-lookup"><span data-stu-id="753b1-112">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="753b1-113">说明</span><span class="sxs-lookup"><span data-stu-id="753b1-113">Description</span></span>  

 <span data-ttu-id="753b1-114">指示已安排 CompletionWorkItem。</span><span class="sxs-lookup"><span data-stu-id="753b1-114">Indicates a CompletionWorkItem has been scheduled.</span></span>  
  
## <a name="message"></a><span data-ttu-id="753b1-115">消息</span><span class="sxs-lookup"><span data-stu-id="753b1-115">Message</span></span>  

 <span data-ttu-id="753b1-116">已为父 Activity "%1"、DisplayName "%2"、InstanceId "%3" 安排了 CompletionWorkItem。</span><span class="sxs-lookup"><span data-stu-id="753b1-116">A CompletionWorkItem has been scheduled for parent Activity '%1', DisplayName: '%2', InstanceId: '%3'.</span></span>  <span data-ttu-id="753b1-117">已完成的活动“%4”、DisplayName：“%5”、InstanceId：“%6”。</span><span class="sxs-lookup"><span data-stu-id="753b1-117">Completed Activity '%4', DisplayName: '%5', InstanceId: '%6'.</span></span>  
  
## <a name="details"></a><span data-ttu-id="753b1-118">详细信息</span><span class="sxs-lookup"><span data-stu-id="753b1-118">Details</span></span>  
  
|<span data-ttu-id="753b1-119">数据项名称</span><span class="sxs-lookup"><span data-stu-id="753b1-119">Data Item Name</span></span>|<span data-ttu-id="753b1-120">数据项类型</span><span class="sxs-lookup"><span data-stu-id="753b1-120">Data Item Type</span></span>|<span data-ttu-id="753b1-121">说明</span><span class="sxs-lookup"><span data-stu-id="753b1-121">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="753b1-122">ParentActivity</span><span class="sxs-lookup"><span data-stu-id="753b1-122">ParentActivity</span></span>|<span data-ttu-id="753b1-123">xs:string</span><span class="sxs-lookup"><span data-stu-id="753b1-123">xs:string</span></span>|<span data-ttu-id="753b1-124">父活动的类型名称。</span><span class="sxs-lookup"><span data-stu-id="753b1-124">The type name of the parent activity.</span></span>|  
|<span data-ttu-id="753b1-125">ParentDisplayName</span><span class="sxs-lookup"><span data-stu-id="753b1-125">ParentDisplayName</span></span>|<span data-ttu-id="753b1-126">xs:string</span><span class="sxs-lookup"><span data-stu-id="753b1-126">xs:string</span></span>|<span data-ttu-id="753b1-127">父活动的显示名称。</span><span class="sxs-lookup"><span data-stu-id="753b1-127">The display name of the parent activity.</span></span>|  
|<span data-ttu-id="753b1-128">ParentInstanceId</span><span class="sxs-lookup"><span data-stu-id="753b1-128">ParentInstanceId</span></span>|<span data-ttu-id="753b1-129">xs:string</span><span class="sxs-lookup"><span data-stu-id="753b1-129">xs:string</span></span>|<span data-ttu-id="753b1-130">父活动的实例 ID。</span><span class="sxs-lookup"><span data-stu-id="753b1-130">The instance id of the parent activity.</span></span>|  
|<span data-ttu-id="753b1-131">CompletedActivity</span><span class="sxs-lookup"><span data-stu-id="753b1-131">CompletedActivity</span></span>|<span data-ttu-id="753b1-132">xs:string</span><span class="sxs-lookup"><span data-stu-id="753b1-132">xs:string</span></span>|<span data-ttu-id="753b1-133">已完成活动的类型名称。</span><span class="sxs-lookup"><span data-stu-id="753b1-133">The type name of the completed activity.</span></span>|  
|<span data-ttu-id="753b1-134">CompletedActivityDisplayName</span><span class="sxs-lookup"><span data-stu-id="753b1-134">CompletedActivityDisplayName</span></span>|<span data-ttu-id="753b1-135">xs:string</span><span class="sxs-lookup"><span data-stu-id="753b1-135">xs:string</span></span>|<span data-ttu-id="753b1-136">已完成活动的显示名称。</span><span class="sxs-lookup"><span data-stu-id="753b1-136">The display name of the completed activity.</span></span>|  
|<span data-ttu-id="753b1-137">CompletedActivityInstanceId</span><span class="sxs-lookup"><span data-stu-id="753b1-137">CompletedActivityInstanceId</span></span>|<span data-ttu-id="753b1-138">xs:string</span><span class="sxs-lookup"><span data-stu-id="753b1-138">xs:string</span></span>|<span data-ttu-id="753b1-139">已完成活动的实例 ID。</span><span class="sxs-lookup"><span data-stu-id="753b1-139">The instance id of the completed activity.</span></span>|  
|<span data-ttu-id="753b1-140">应用程序域</span><span class="sxs-lookup"><span data-stu-id="753b1-140">AppDomain</span></span>|<span data-ttu-id="753b1-141">xs:string</span><span class="sxs-lookup"><span data-stu-id="753b1-141">xs:string</span></span>|<span data-ttu-id="753b1-142">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="753b1-142">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
