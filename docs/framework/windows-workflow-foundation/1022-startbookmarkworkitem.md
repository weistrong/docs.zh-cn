---
description: 了解详细信息： 1022-StartBookmarkWorkItem
title: 1022 - StartBookmarkWorkItem
ms.date: 03/30/2017
ms.assetid: 4415fbdb-0329-4019-803f-aea66e75f3da
ms.openlocfilehash: 37d1ec1216df26a928b39189ca299dbb5b6c3d4b
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99792825"
---
# <a name="1022---startbookmarkworkitem"></a><span data-ttu-id="2505d-103">1022 - StartBookmarkWorkItem</span><span class="sxs-lookup"><span data-stu-id="2505d-103">1022 - StartBookmarkWorkItem</span></span>

## <a name="properties"></a><span data-ttu-id="2505d-104">属性</span><span class="sxs-lookup"><span data-stu-id="2505d-104">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="2505d-105">ID</span><span class="sxs-lookup"><span data-stu-id="2505d-105">ID</span></span>|<span data-ttu-id="2505d-106">1022</span><span class="sxs-lookup"><span data-stu-id="2505d-106">1022</span></span>|  
|<span data-ttu-id="2505d-107">关键字</span><span class="sxs-lookup"><span data-stu-id="2505d-107">Keywords</span></span>|<span data-ttu-id="2505d-108">WFRuntime</span><span class="sxs-lookup"><span data-stu-id="2505d-108">WFRuntime</span></span>|  
|<span data-ttu-id="2505d-109">级别</span><span class="sxs-lookup"><span data-stu-id="2505d-109">Level</span></span>|<span data-ttu-id="2505d-110">“详细”</span><span class="sxs-lookup"><span data-stu-id="2505d-110">Verbose</span></span>|  
|<span data-ttu-id="2505d-111">通道</span><span class="sxs-lookup"><span data-stu-id="2505d-111">Channel</span></span>|<span data-ttu-id="2505d-112">Microsoft-Windows-应用程序服务器-应用程序/调试</span><span class="sxs-lookup"><span data-stu-id="2505d-112">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="2505d-113">说明</span><span class="sxs-lookup"><span data-stu-id="2505d-113">Description</span></span>  

 <span data-ttu-id="2505d-114">指示 BookmarkWorkItem 正在开始执行。</span><span class="sxs-lookup"><span data-stu-id="2505d-114">Indicates a BookmarkWorkItem is starting execution.</span></span>  
  
## <a name="message"></a><span data-ttu-id="2505d-115">消息</span><span class="sxs-lookup"><span data-stu-id="2505d-115">Message</span></span>  

 <span data-ttu-id="2505d-116">开始为 Activity "%1"、DisplayName "%2"、InstanceId "%3" 执行 BookmarkWorkItem。</span><span class="sxs-lookup"><span data-stu-id="2505d-116">Starting execution of a BookmarkWorkItem for Activity '%1', DisplayName: '%2', InstanceId: '%3'.</span></span>  <span data-ttu-id="2505d-117">BookmarkName: %4、BookmarkScope: %5。</span><span class="sxs-lookup"><span data-stu-id="2505d-117">BookmarkName: %4, BookmarkScope: %5.</span></span>  
  
## <a name="details"></a><span data-ttu-id="2505d-118">详细信息</span><span class="sxs-lookup"><span data-stu-id="2505d-118">Details</span></span>  
  
|<span data-ttu-id="2505d-119">数据项名称</span><span class="sxs-lookup"><span data-stu-id="2505d-119">Data Item Name</span></span>|<span data-ttu-id="2505d-120">数据项类型</span><span class="sxs-lookup"><span data-stu-id="2505d-120">Data Item Type</span></span>|<span data-ttu-id="2505d-121">说明</span><span class="sxs-lookup"><span data-stu-id="2505d-121">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="2505d-122">活动</span><span class="sxs-lookup"><span data-stu-id="2505d-122">Activity</span></span>|<span data-ttu-id="2505d-123">xs:string</span><span class="sxs-lookup"><span data-stu-id="2505d-123">xs:string</span></span>|<span data-ttu-id="2505d-124">活动的类型名称。</span><span class="sxs-lookup"><span data-stu-id="2505d-124">The type name of the activity.</span></span>|  
|<span data-ttu-id="2505d-125">DisplayName</span><span class="sxs-lookup"><span data-stu-id="2505d-125">DisplayName</span></span>|<span data-ttu-id="2505d-126">xs:string</span><span class="sxs-lookup"><span data-stu-id="2505d-126">xs:string</span></span>|<span data-ttu-id="2505d-127">活动的显示名称。</span><span class="sxs-lookup"><span data-stu-id="2505d-127">The display name of the activity.</span></span>|  
|<span data-ttu-id="2505d-128">InstanceId</span><span class="sxs-lookup"><span data-stu-id="2505d-128">InstanceId</span></span>|<span data-ttu-id="2505d-129">xs:string</span><span class="sxs-lookup"><span data-stu-id="2505d-129">xs:string</span></span>|<span data-ttu-id="2505d-130">活动的实例 ID。</span><span class="sxs-lookup"><span data-stu-id="2505d-130">The instance id of the activity.</span></span>|  
|<span data-ttu-id="2505d-131">BookmarkName</span><span class="sxs-lookup"><span data-stu-id="2505d-131">BookmarkName</span></span>|<span data-ttu-id="2505d-132">xs:string</span><span class="sxs-lookup"><span data-stu-id="2505d-132">xs:string</span></span>|<span data-ttu-id="2505d-133">书签的名称。</span><span class="sxs-lookup"><span data-stu-id="2505d-133">The name of the bookmark.</span></span>|  
|<span data-ttu-id="2505d-134">BookmarkScope</span><span class="sxs-lookup"><span data-stu-id="2505d-134">BookmarkScope</span></span>|<span data-ttu-id="2505d-135">xs:string</span><span class="sxs-lookup"><span data-stu-id="2505d-135">xs:string</span></span>|<span data-ttu-id="2505d-136">书签的范围。</span><span class="sxs-lookup"><span data-stu-id="2505d-136">The scope of the bookmark.</span></span>|  
|<span data-ttu-id="2505d-137">应用程序域</span><span class="sxs-lookup"><span data-stu-id="2505d-137">AppDomain</span></span>|<span data-ttu-id="2505d-138">xs:string</span><span class="sxs-lookup"><span data-stu-id="2505d-138">xs:string</span></span>|<span data-ttu-id="2505d-139">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="2505d-139">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
