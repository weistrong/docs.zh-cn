---
description: 了解详细信息： 1021-ScheduleBookmarkWorkItem
title: 1021 - ScheduleBookmarkWorkItem
ms.date: 03/30/2017
ms.assetid: 2e0da311-b219-4637-9460-90cdafcc4ecd
ms.openlocfilehash: 5153d2e90a75bab90c76ee8786dc82d4ddac19a1
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99792812"
---
# <a name="1021---schedulebookmarkworkitem"></a><span data-ttu-id="90ff2-103">1021 - ScheduleBookmarkWorkItem</span><span class="sxs-lookup"><span data-stu-id="90ff2-103">1021 - ScheduleBookmarkWorkItem</span></span>

## <a name="properties"></a><span data-ttu-id="90ff2-104">属性</span><span class="sxs-lookup"><span data-stu-id="90ff2-104">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="90ff2-105">ID</span><span class="sxs-lookup"><span data-stu-id="90ff2-105">ID</span></span>|<span data-ttu-id="90ff2-106">1021</span><span class="sxs-lookup"><span data-stu-id="90ff2-106">1021</span></span>|  
|<span data-ttu-id="90ff2-107">关键字</span><span class="sxs-lookup"><span data-stu-id="90ff2-107">Keywords</span></span>|<span data-ttu-id="90ff2-108">WFRuntime</span><span class="sxs-lookup"><span data-stu-id="90ff2-108">WFRuntime</span></span>|  
|<span data-ttu-id="90ff2-109">级别</span><span class="sxs-lookup"><span data-stu-id="90ff2-109">Level</span></span>|<span data-ttu-id="90ff2-110">“详细”</span><span class="sxs-lookup"><span data-stu-id="90ff2-110">Verbose</span></span>|  
|<span data-ttu-id="90ff2-111">通道</span><span class="sxs-lookup"><span data-stu-id="90ff2-111">Channel</span></span>|<span data-ttu-id="90ff2-112">Microsoft-Windows-应用程序服务器-应用程序/调试</span><span class="sxs-lookup"><span data-stu-id="90ff2-112">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="90ff2-113">说明</span><span class="sxs-lookup"><span data-stu-id="90ff2-113">Description</span></span>  

 <span data-ttu-id="90ff2-114">指示已安排 BookmarkWorkItem。</span><span class="sxs-lookup"><span data-stu-id="90ff2-114">Indicates a BookmarkWorkItem has been scheduled.</span></span>  
  
## <a name="message"></a><span data-ttu-id="90ff2-115">消息</span><span class="sxs-lookup"><span data-stu-id="90ff2-115">Message</span></span>  

 <span data-ttu-id="90ff2-116">已为 Activity "%1"、DisplayName "%2"、InstanceId "%3" 安排了 BookmarkWorkItem。</span><span class="sxs-lookup"><span data-stu-id="90ff2-116">A BookmarkWorkItem has been scheduled for Activity '%1', DisplayName: '%2', InstanceId: '%3'.</span></span>  <span data-ttu-id="90ff2-117">BookmarkName: %4、BookmarkScope: %5。</span><span class="sxs-lookup"><span data-stu-id="90ff2-117">BookmarkName: %4, BookmarkScope: %5.</span></span>  
  
## <a name="details"></a><span data-ttu-id="90ff2-118">详细信息</span><span class="sxs-lookup"><span data-stu-id="90ff2-118">Details</span></span>  
  
|<span data-ttu-id="90ff2-119">数据项名称</span><span class="sxs-lookup"><span data-stu-id="90ff2-119">Data Item Name</span></span>|<span data-ttu-id="90ff2-120">数据项类型</span><span class="sxs-lookup"><span data-stu-id="90ff2-120">Data Item Type</span></span>|<span data-ttu-id="90ff2-121">说明</span><span class="sxs-lookup"><span data-stu-id="90ff2-121">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="90ff2-122">活动</span><span class="sxs-lookup"><span data-stu-id="90ff2-122">Activity</span></span>|<span data-ttu-id="90ff2-123">xs:string</span><span class="sxs-lookup"><span data-stu-id="90ff2-123">xs:string</span></span>|<span data-ttu-id="90ff2-124">活动的类型名称。</span><span class="sxs-lookup"><span data-stu-id="90ff2-124">The type name of the activity.</span></span>|  
|<span data-ttu-id="90ff2-125">DisplayName</span><span class="sxs-lookup"><span data-stu-id="90ff2-125">DisplayName</span></span>|<span data-ttu-id="90ff2-126">xs:string</span><span class="sxs-lookup"><span data-stu-id="90ff2-126">xs:string</span></span>|<span data-ttu-id="90ff2-127">活动的显示名称。</span><span class="sxs-lookup"><span data-stu-id="90ff2-127">The display name of the activity.</span></span>|  
|<span data-ttu-id="90ff2-128">InstanceId</span><span class="sxs-lookup"><span data-stu-id="90ff2-128">InstanceId</span></span>|<span data-ttu-id="90ff2-129">xs:string</span><span class="sxs-lookup"><span data-stu-id="90ff2-129">xs:string</span></span>|<span data-ttu-id="90ff2-130">活动的实例 ID。</span><span class="sxs-lookup"><span data-stu-id="90ff2-130">The instance id of the activity.</span></span>|  
|<span data-ttu-id="90ff2-131">BookmarkName</span><span class="sxs-lookup"><span data-stu-id="90ff2-131">BookmarkName</span></span>|<span data-ttu-id="90ff2-132">xs:string</span><span class="sxs-lookup"><span data-stu-id="90ff2-132">xs:string</span></span>|<span data-ttu-id="90ff2-133">书签的名称。</span><span class="sxs-lookup"><span data-stu-id="90ff2-133">The name of the bookmark.</span></span>|  
|<span data-ttu-id="90ff2-134">BookmarkScope</span><span class="sxs-lookup"><span data-stu-id="90ff2-134">BookmarkScope</span></span>|<span data-ttu-id="90ff2-135">xs:string</span><span class="sxs-lookup"><span data-stu-id="90ff2-135">xs:string</span></span>|<span data-ttu-id="90ff2-136">书签的范围。</span><span class="sxs-lookup"><span data-stu-id="90ff2-136">The scope of the bookmark.</span></span>|  
|<span data-ttu-id="90ff2-137">应用程序域</span><span class="sxs-lookup"><span data-stu-id="90ff2-137">AppDomain</span></span>|<span data-ttu-id="90ff2-138">xs:string</span><span class="sxs-lookup"><span data-stu-id="90ff2-138">xs:string</span></span>|<span data-ttu-id="90ff2-139">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="90ff2-139">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
