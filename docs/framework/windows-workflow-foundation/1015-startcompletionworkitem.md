---
description: 了解详细信息： 1015-StartCompletionWorkItem
title: 1015 - StartCompletionWorkItem
ms.date: 03/30/2017
ms.assetid: 96fd1d4e-c5d0-46ad-8a71-4b4b49ac7262
ms.openlocfilehash: 6c79a02b144aa1176eb1cb334c8430c8f0babc3a
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99792916"
---
# <a name="1015---startcompletionworkitem"></a><span data-ttu-id="7edc7-103">1015 - StartCompletionWorkItem</span><span class="sxs-lookup"><span data-stu-id="7edc7-103">1015 - StartCompletionWorkItem</span></span>

## <a name="properties"></a><span data-ttu-id="7edc7-104">属性</span><span class="sxs-lookup"><span data-stu-id="7edc7-104">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="7edc7-105">ID</span><span class="sxs-lookup"><span data-stu-id="7edc7-105">ID</span></span>|<span data-ttu-id="7edc7-106">1015</span><span class="sxs-lookup"><span data-stu-id="7edc7-106">1015</span></span>|  
|<span data-ttu-id="7edc7-107">关键字</span><span class="sxs-lookup"><span data-stu-id="7edc7-107">Keywords</span></span>|<span data-ttu-id="7edc7-108">WFRuntime</span><span class="sxs-lookup"><span data-stu-id="7edc7-108">WFRuntime</span></span>|  
|<span data-ttu-id="7edc7-109">级别</span><span class="sxs-lookup"><span data-stu-id="7edc7-109">Level</span></span>|<span data-ttu-id="7edc7-110">“详细”</span><span class="sxs-lookup"><span data-stu-id="7edc7-110">Verbose</span></span>|  
|<span data-ttu-id="7edc7-111">通道</span><span class="sxs-lookup"><span data-stu-id="7edc7-111">Channel</span></span>|<span data-ttu-id="7edc7-112">Microsoft-Windows-应用程序服务器-应用程序/调试</span><span class="sxs-lookup"><span data-stu-id="7edc7-112">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="7edc7-113">说明</span><span class="sxs-lookup"><span data-stu-id="7edc7-113">Description</span></span>  

 <span data-ttu-id="7edc7-114">指示 CompletionWorkItem 正在开始执行。</span><span class="sxs-lookup"><span data-stu-id="7edc7-114">Indicates a CompletionWorkItem is starting execution.</span></span>  
  
## <a name="message"></a><span data-ttu-id="7edc7-115">消息</span><span class="sxs-lookup"><span data-stu-id="7edc7-115">Message</span></span>  

 <span data-ttu-id="7edc7-116">开始为父 Activity“%1”、DisplayName“%2”、InstanceId“%3”执行 CompletionWorkItem。</span><span class="sxs-lookup"><span data-stu-id="7edc7-116">Starting execution of a CompletionWorkItem for parent Activity '%1', DisplayName: '%2', InstanceId: '%3'.</span></span> <span data-ttu-id="7edc7-117">已完成的活动“%4”、DisplayName：“%5”、InstanceId：“%6”。</span><span class="sxs-lookup"><span data-stu-id="7edc7-117">Completed Activity '%4', DisplayName: '%5', InstanceId: '%6'.</span></span>  
  
## <a name="details"></a><span data-ttu-id="7edc7-118">详细信息</span><span class="sxs-lookup"><span data-stu-id="7edc7-118">Details</span></span>  
  
|<span data-ttu-id="7edc7-119">数据项名称</span><span class="sxs-lookup"><span data-stu-id="7edc7-119">Data Item Name</span></span>|<span data-ttu-id="7edc7-120">数据项类型</span><span class="sxs-lookup"><span data-stu-id="7edc7-120">Data Item Type</span></span>|<span data-ttu-id="7edc7-121">说明</span><span class="sxs-lookup"><span data-stu-id="7edc7-121">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="7edc7-122">ParentActivity</span><span class="sxs-lookup"><span data-stu-id="7edc7-122">ParentActivity</span></span>|<span data-ttu-id="7edc7-123">xs:string</span><span class="sxs-lookup"><span data-stu-id="7edc7-123">xs:string</span></span>|<span data-ttu-id="7edc7-124">父活动的类型名称。</span><span class="sxs-lookup"><span data-stu-id="7edc7-124">The type name of the parent activity.</span></span>|  
|<span data-ttu-id="7edc7-125">ParentDisplayName</span><span class="sxs-lookup"><span data-stu-id="7edc7-125">ParentDisplayName</span></span>|<span data-ttu-id="7edc7-126">xs:string</span><span class="sxs-lookup"><span data-stu-id="7edc7-126">xs:string</span></span>|<span data-ttu-id="7edc7-127">父活动的显示名称。</span><span class="sxs-lookup"><span data-stu-id="7edc7-127">The display name of the parent activity.</span></span>|  
|<span data-ttu-id="7edc7-128">ParentInstanceId</span><span class="sxs-lookup"><span data-stu-id="7edc7-128">ParentInstanceId</span></span>|<span data-ttu-id="7edc7-129">xs:string</span><span class="sxs-lookup"><span data-stu-id="7edc7-129">xs:string</span></span>|<span data-ttu-id="7edc7-130">父活动的实例 ID。</span><span class="sxs-lookup"><span data-stu-id="7edc7-130">The instance id of the parent activity.</span></span>|  
|<span data-ttu-id="7edc7-131">CompletedActivity</span><span class="sxs-lookup"><span data-stu-id="7edc7-131">CompletedActivity</span></span>|<span data-ttu-id="7edc7-132">xs:string</span><span class="sxs-lookup"><span data-stu-id="7edc7-132">xs:string</span></span>|<span data-ttu-id="7edc7-133">已完成活动的类型名称。</span><span class="sxs-lookup"><span data-stu-id="7edc7-133">The type name of the completed activity.</span></span>|  
|<span data-ttu-id="7edc7-134">CompletedActivityDisplayName</span><span class="sxs-lookup"><span data-stu-id="7edc7-134">CompletedActivityDisplayName</span></span>|<span data-ttu-id="7edc7-135">xs:string</span><span class="sxs-lookup"><span data-stu-id="7edc7-135">xs:string</span></span>|<span data-ttu-id="7edc7-136">已完成活动的显示名称。</span><span class="sxs-lookup"><span data-stu-id="7edc7-136">The display name of the completed activity.</span></span>|  
|<span data-ttu-id="7edc7-137">CompletedActivityInstanceId</span><span class="sxs-lookup"><span data-stu-id="7edc7-137">CompletedActivityInstanceId</span></span>|<span data-ttu-id="7edc7-138">xs:string</span><span class="sxs-lookup"><span data-stu-id="7edc7-138">xs:string</span></span>|<span data-ttu-id="7edc7-139">已完成活动的实例 ID。</span><span class="sxs-lookup"><span data-stu-id="7edc7-139">The instance id of the completed activity.</span></span>|  
|<span data-ttu-id="7edc7-140">应用程序域</span><span class="sxs-lookup"><span data-stu-id="7edc7-140">AppDomain</span></span>|<span data-ttu-id="7edc7-141">xs:string</span><span class="sxs-lookup"><span data-stu-id="7edc7-141">xs:string</span></span>|<span data-ttu-id="7edc7-142">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="7edc7-142">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
