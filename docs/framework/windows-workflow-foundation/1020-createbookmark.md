---
description: 了解详细信息： 1020-CreateBookmark
title: 1020 - CreateBookmark
ms.date: 03/30/2017
ms.assetid: 4bee948d-816f-4803-85cc-3883b5e23d10
ms.openlocfilehash: 39796eaf68d9cb52e9faa2605fc21955a2c167ac
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99792838"
---
# <a name="1020---createbookmark"></a><span data-ttu-id="899b9-103">1020 - CreateBookmark</span><span class="sxs-lookup"><span data-stu-id="899b9-103">1020 - CreateBookmark</span></span>

## <a name="properties"></a><span data-ttu-id="899b9-104">属性</span><span class="sxs-lookup"><span data-stu-id="899b9-104">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="899b9-105">ID</span><span class="sxs-lookup"><span data-stu-id="899b9-105">ID</span></span>|<span data-ttu-id="899b9-106">1020</span><span class="sxs-lookup"><span data-stu-id="899b9-106">1020</span></span>|  
|<span data-ttu-id="899b9-107">关键字</span><span class="sxs-lookup"><span data-stu-id="899b9-107">Keywords</span></span>|<span data-ttu-id="899b9-108">WFRuntime</span><span class="sxs-lookup"><span data-stu-id="899b9-108">WFRuntime</span></span>|  
|<span data-ttu-id="899b9-109">级别</span><span class="sxs-lookup"><span data-stu-id="899b9-109">Level</span></span>|<span data-ttu-id="899b9-110">“详细”</span><span class="sxs-lookup"><span data-stu-id="899b9-110">Verbose</span></span>|  
|<span data-ttu-id="899b9-111">通道</span><span class="sxs-lookup"><span data-stu-id="899b9-111">Channel</span></span>|<span data-ttu-id="899b9-112">Microsoft-Windows-应用程序服务器-应用程序/调试</span><span class="sxs-lookup"><span data-stu-id="899b9-112">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="899b9-113">说明</span><span class="sxs-lookup"><span data-stu-id="899b9-113">Description</span></span>  

 <span data-ttu-id="899b9-114">指示已为活动创建了书签。</span><span class="sxs-lookup"><span data-stu-id="899b9-114">Indicates a bookmark has been created for an activity.</span></span>  
  
## <a name="message"></a><span data-ttu-id="899b9-115">消息</span><span class="sxs-lookup"><span data-stu-id="899b9-115">Message</span></span>  

 <span data-ttu-id="899b9-116">已为 Activity "%1"、DisplayName "%2"、InstanceId "%3" 创建了书签。</span><span class="sxs-lookup"><span data-stu-id="899b9-116">A Bookmark has been created for Activity '%1', DisplayName: '%2', InstanceId: '%3'.</span></span>  <span data-ttu-id="899b9-117">BookmarkName: %4、BookmarkScope: %5。</span><span class="sxs-lookup"><span data-stu-id="899b9-117">BookmarkName: %4, BookmarkScope: %5.</span></span>  
  
## <a name="details"></a><span data-ttu-id="899b9-118">详细信息</span><span class="sxs-lookup"><span data-stu-id="899b9-118">Details</span></span>  
  
|<span data-ttu-id="899b9-119">数据项名称</span><span class="sxs-lookup"><span data-stu-id="899b9-119">Data Item Name</span></span>|<span data-ttu-id="899b9-120">数据项类型</span><span class="sxs-lookup"><span data-stu-id="899b9-120">Data Item Type</span></span>|<span data-ttu-id="899b9-121">说明</span><span class="sxs-lookup"><span data-stu-id="899b9-121">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="899b9-122">活动</span><span class="sxs-lookup"><span data-stu-id="899b9-122">Activity</span></span>|<span data-ttu-id="899b9-123">xs:string</span><span class="sxs-lookup"><span data-stu-id="899b9-123">xs:string</span></span>|<span data-ttu-id="899b9-124">活动的类型名称。</span><span class="sxs-lookup"><span data-stu-id="899b9-124">The type name of the activity.</span></span>|  
|<span data-ttu-id="899b9-125">DisplayName</span><span class="sxs-lookup"><span data-stu-id="899b9-125">DisplayName</span></span>|<span data-ttu-id="899b9-126">xs:string</span><span class="sxs-lookup"><span data-stu-id="899b9-126">xs:string</span></span>|<span data-ttu-id="899b9-127">活动的显示名称。</span><span class="sxs-lookup"><span data-stu-id="899b9-127">The display name of the activity.</span></span>|  
|<span data-ttu-id="899b9-128">InstanceId</span><span class="sxs-lookup"><span data-stu-id="899b9-128">InstanceId</span></span>|<span data-ttu-id="899b9-129">xs:string</span><span class="sxs-lookup"><span data-stu-id="899b9-129">xs:string</span></span>|<span data-ttu-id="899b9-130">活动的实例 ID。</span><span class="sxs-lookup"><span data-stu-id="899b9-130">The instance id of the activity.</span></span>|  
|<span data-ttu-id="899b9-131">BookmarkName</span><span class="sxs-lookup"><span data-stu-id="899b9-131">BookmarkName</span></span>|<span data-ttu-id="899b9-132">xs:string</span><span class="sxs-lookup"><span data-stu-id="899b9-132">xs:string</span></span>|<span data-ttu-id="899b9-133">书签的名称。</span><span class="sxs-lookup"><span data-stu-id="899b9-133">The name of the bookmark.</span></span>|  
|<span data-ttu-id="899b9-134">BookmarkScope</span><span class="sxs-lookup"><span data-stu-id="899b9-134">BookmarkScope</span></span>|<span data-ttu-id="899b9-135">xs:string</span><span class="sxs-lookup"><span data-stu-id="899b9-135">xs:string</span></span>|<span data-ttu-id="899b9-136">书签的范围。</span><span class="sxs-lookup"><span data-stu-id="899b9-136">The scope of the bookmark.</span></span>|  
|<span data-ttu-id="899b9-137">应用程序域</span><span class="sxs-lookup"><span data-stu-id="899b9-137">AppDomain</span></span>|<span data-ttu-id="899b9-138">xs:string</span><span class="sxs-lookup"><span data-stu-id="899b9-138">xs:string</span></span>|<span data-ttu-id="899b9-139">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="899b9-139">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
