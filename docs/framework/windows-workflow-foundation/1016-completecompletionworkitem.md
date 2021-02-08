---
description: 了解详细信息： 1016-CompleteCompletionWorkItem
title: 1016 - CompleteCompletionWorkItem
ms.date: 03/30/2017
ms.assetid: 246929fb-6f14-440a-814b-cd8349350644
ms.openlocfilehash: 849e192d63b5db19e5beea31befcdc38d4340c6e
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99792903"
---
# <a name="1016---completecompletionworkitem"></a><span data-ttu-id="5d8f2-103">1016 - CompleteCompletionWorkItem</span><span class="sxs-lookup"><span data-stu-id="5d8f2-103">1016 - CompleteCompletionWorkItem</span></span>

## <a name="properties"></a><span data-ttu-id="5d8f2-104">属性</span><span class="sxs-lookup"><span data-stu-id="5d8f2-104">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="5d8f2-105">ID</span><span class="sxs-lookup"><span data-stu-id="5d8f2-105">ID</span></span>|<span data-ttu-id="5d8f2-106">1016</span><span class="sxs-lookup"><span data-stu-id="5d8f2-106">1016</span></span>|  
|<span data-ttu-id="5d8f2-107">关键字</span><span class="sxs-lookup"><span data-stu-id="5d8f2-107">Keywords</span></span>|<span data-ttu-id="5d8f2-108">WFRuntime</span><span class="sxs-lookup"><span data-stu-id="5d8f2-108">WFRuntime</span></span>|  
|<span data-ttu-id="5d8f2-109">级别</span><span class="sxs-lookup"><span data-stu-id="5d8f2-109">Level</span></span>|<span data-ttu-id="5d8f2-110">“详细”</span><span class="sxs-lookup"><span data-stu-id="5d8f2-110">Verbose</span></span>|  
|<span data-ttu-id="5d8f2-111">通道</span><span class="sxs-lookup"><span data-stu-id="5d8f2-111">Channel</span></span>|<span data-ttu-id="5d8f2-112">Microsoft-Windows-应用程序服务器-应用程序/调试</span><span class="sxs-lookup"><span data-stu-id="5d8f2-112">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="5d8f2-113">说明</span><span class="sxs-lookup"><span data-stu-id="5d8f2-113">Description</span></span>  

 <span data-ttu-id="5d8f2-114">指示 CompletionWorkItem 已完成。</span><span class="sxs-lookup"><span data-stu-id="5d8f2-114">Indicates a CompletionWorkItem has completed.</span></span>  
  
## <a name="message"></a><span data-ttu-id="5d8f2-115">消息</span><span class="sxs-lookup"><span data-stu-id="5d8f2-115">Message</span></span>  

 <span data-ttu-id="5d8f2-116">父 Activity“%1”、DisplayName“'%2”、InstanceId“%3”已完成了 CompletionWorkItem。</span><span class="sxs-lookup"><span data-stu-id="5d8f2-116">A CompletionWorkItem has completed for parent Activity '%1', DisplayName: '%2', InstanceId: '%3'.</span></span> <span data-ttu-id="5d8f2-117">已完成的活动“%4”、DisplayName：“%5”、InstanceId：“%6”。</span><span class="sxs-lookup"><span data-stu-id="5d8f2-117">Completed Activity '%4', DisplayName: '%5', InstanceId: '%6'.</span></span>  
  
## <a name="details"></a><span data-ttu-id="5d8f2-118">详细信息</span><span class="sxs-lookup"><span data-stu-id="5d8f2-118">Details</span></span>  
  
|<span data-ttu-id="5d8f2-119">数据项名称</span><span class="sxs-lookup"><span data-stu-id="5d8f2-119">Data Item Name</span></span>|<span data-ttu-id="5d8f2-120">数据项类型</span><span class="sxs-lookup"><span data-stu-id="5d8f2-120">Data Item Type</span></span>|<span data-ttu-id="5d8f2-121">说明</span><span class="sxs-lookup"><span data-stu-id="5d8f2-121">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="5d8f2-122">ParentActivity</span><span class="sxs-lookup"><span data-stu-id="5d8f2-122">ParentActivity</span></span>|<span data-ttu-id="5d8f2-123">xs:string</span><span class="sxs-lookup"><span data-stu-id="5d8f2-123">xs:string</span></span>|<span data-ttu-id="5d8f2-124">父活动的类型名称。</span><span class="sxs-lookup"><span data-stu-id="5d8f2-124">The type name of the parent activity.</span></span>|  
|<span data-ttu-id="5d8f2-125">ParentDisplayName</span><span class="sxs-lookup"><span data-stu-id="5d8f2-125">ParentDisplayName</span></span>|<span data-ttu-id="5d8f2-126">xs:string</span><span class="sxs-lookup"><span data-stu-id="5d8f2-126">xs:string</span></span>|<span data-ttu-id="5d8f2-127">父活动的显示名称。</span><span class="sxs-lookup"><span data-stu-id="5d8f2-127">The display name of the parent activity.</span></span>|  
|<span data-ttu-id="5d8f2-128">ParentInstanceId</span><span class="sxs-lookup"><span data-stu-id="5d8f2-128">ParentInstanceId</span></span>|<span data-ttu-id="5d8f2-129">xs:string</span><span class="sxs-lookup"><span data-stu-id="5d8f2-129">xs:string</span></span>|<span data-ttu-id="5d8f2-130">父活动的实例 ID。</span><span class="sxs-lookup"><span data-stu-id="5d8f2-130">The instance id of the parent activity.</span></span>|  
|<span data-ttu-id="5d8f2-131">CompletedActivity</span><span class="sxs-lookup"><span data-stu-id="5d8f2-131">CompletedActivity</span></span>|<span data-ttu-id="5d8f2-132">xs:string</span><span class="sxs-lookup"><span data-stu-id="5d8f2-132">xs:string</span></span>|<span data-ttu-id="5d8f2-133">已完成活动的类型名称。</span><span class="sxs-lookup"><span data-stu-id="5d8f2-133">The type name of the completed activity.</span></span>|  
|<span data-ttu-id="5d8f2-134">CompletedActivityDisplayName</span><span class="sxs-lookup"><span data-stu-id="5d8f2-134">CompletedActivityDisplayName</span></span>|<span data-ttu-id="5d8f2-135">xs:string</span><span class="sxs-lookup"><span data-stu-id="5d8f2-135">xs:string</span></span>|<span data-ttu-id="5d8f2-136">已完成活动的显示名称。</span><span class="sxs-lookup"><span data-stu-id="5d8f2-136">The display name of the completed activity.</span></span>|  
|<span data-ttu-id="5d8f2-137">CompletedActivityInstanceId</span><span class="sxs-lookup"><span data-stu-id="5d8f2-137">CompletedActivityInstanceId</span></span>|<span data-ttu-id="5d8f2-138">xs:string</span><span class="sxs-lookup"><span data-stu-id="5d8f2-138">xs:string</span></span>|<span data-ttu-id="5d8f2-139">已完成活动的实例 ID。</span><span class="sxs-lookup"><span data-stu-id="5d8f2-139">The instance id of the completed activity.</span></span>|  
|<span data-ttu-id="5d8f2-140">应用程序域</span><span class="sxs-lookup"><span data-stu-id="5d8f2-140">AppDomain</span></span>|<span data-ttu-id="5d8f2-141">xs:string</span><span class="sxs-lookup"><span data-stu-id="5d8f2-141">xs:string</span></span>|<span data-ttu-id="5d8f2-142">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="5d8f2-142">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
