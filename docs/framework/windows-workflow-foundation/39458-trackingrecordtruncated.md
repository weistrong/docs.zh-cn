---
description: 了解详细信息： 39458-TrackingRecordTruncated
title: 39458 - TrackingRecordTruncated
ms.date: 03/30/2017
ms.assetid: 5352f0eb-d571-454a-bab5-e2162888b218
ms.openlocfilehash: bb9a46dc5bd9bc4f4709a740dd0e7ec47ca826e3
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99631276"
---
# <a name="39458---trackingrecordtruncated"></a><span data-ttu-id="f3ec9-103">39458 - TrackingRecordTruncated</span><span class="sxs-lookup"><span data-stu-id="f3ec9-103">39458 - TrackingRecordTruncated</span></span>

## <a name="properties"></a><span data-ttu-id="f3ec9-104">属性</span><span class="sxs-lookup"><span data-stu-id="f3ec9-104">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="f3ec9-105">ID</span><span class="sxs-lookup"><span data-stu-id="f3ec9-105">ID</span></span>|<span data-ttu-id="f3ec9-106">39458</span><span class="sxs-lookup"><span data-stu-id="f3ec9-106">39458</span></span>|  
|<span data-ttu-id="f3ec9-107">关键字</span><span class="sxs-lookup"><span data-stu-id="f3ec9-107">Keywords</span></span>|<span data-ttu-id="f3ec9-108">WFTracking</span><span class="sxs-lookup"><span data-stu-id="f3ec9-108">WFTracking</span></span>|  
|<span data-ttu-id="f3ec9-109">级别</span><span class="sxs-lookup"><span data-stu-id="f3ec9-109">Level</span></span>|<span data-ttu-id="f3ec9-110">警告</span><span class="sxs-lookup"><span data-stu-id="f3ec9-110">Warning</span></span>|  
|<span data-ttu-id="f3ec9-111">通道</span><span class="sxs-lookup"><span data-stu-id="f3ec9-111">Channel</span></span>|<span data-ttu-id="f3ec9-112">Microsoft-Windows-应用程序服务器-应用程序/调试</span><span class="sxs-lookup"><span data-stu-id="f3ec9-112">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="f3ec9-113">说明</span><span class="sxs-lookup"><span data-stu-id="f3ec9-113">Description</span></span>  

 <span data-ttu-id="f3ec9-114">指示已截断跟踪记录。</span><span class="sxs-lookup"><span data-stu-id="f3ec9-114">Indicates a tracking record has been truncated.</span></span> <span data-ttu-id="f3ec9-115">已移除了变量/批注/用户数据。</span><span class="sxs-lookup"><span data-stu-id="f3ec9-115">Variables/annotations/user data have been removed.</span></span>  
  
## <a name="message"></a><span data-ttu-id="f3ec9-116">消息</span><span class="sxs-lookup"><span data-stu-id="f3ec9-116">Message</span></span>  

 <span data-ttu-id="f3ec9-117">用提供程序 %2 向 ETW 会话写入了截断的跟踪记录 %1。</span><span class="sxs-lookup"><span data-stu-id="f3ec9-117">Truncated tracking record %1 written to ETW session with provider %2.</span></span> <span data-ttu-id="f3ec9-118">已移除了变量/批注/用户数据</span><span class="sxs-lookup"><span data-stu-id="f3ec9-118">Variables/annotations/user data have been removed</span></span>  
  
## <a name="details"></a><span data-ttu-id="f3ec9-119">详细信息</span><span class="sxs-lookup"><span data-stu-id="f3ec9-119">Details</span></span>  
  
|<span data-ttu-id="f3ec9-120">数据项名称</span><span class="sxs-lookup"><span data-stu-id="f3ec9-120">Data Item Name</span></span>|<span data-ttu-id="f3ec9-121">数据项类型</span><span class="sxs-lookup"><span data-stu-id="f3ec9-121">Data Item Type</span></span>|<span data-ttu-id="f3ec9-122">说明</span><span class="sxs-lookup"><span data-stu-id="f3ec9-122">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="f3ec9-123">RecordNumber</span><span class="sxs-lookup"><span data-stu-id="f3ec9-123">RecordNumber</span></span>|<span data-ttu-id="f3ec9-124">xs:string</span><span class="sxs-lookup"><span data-stu-id="f3ec9-124">xs:string</span></span>|<span data-ttu-id="f3ec9-125">跟踪记录编号。</span><span class="sxs-lookup"><span data-stu-id="f3ec9-125">The tracking record number.</span></span>|  
|<span data-ttu-id="f3ec9-126">ProviderId</span><span class="sxs-lookup"><span data-stu-id="f3ec9-126">ProviderId</span></span>|<span data-ttu-id="f3ec9-127">xs:string</span><span class="sxs-lookup"><span data-stu-id="f3ec9-127">xs:string</span></span>|<span data-ttu-id="f3ec9-128">ETW 提供程序 ID。</span><span class="sxs-lookup"><span data-stu-id="f3ec9-128">The ETW provider id.</span></span>|  
|<span data-ttu-id="f3ec9-129">应用程序域</span><span class="sxs-lookup"><span data-stu-id="f3ec9-129">AppDomain</span></span>|<span data-ttu-id="f3ec9-130">xs:string</span><span class="sxs-lookup"><span data-stu-id="f3ec9-130">xs:string</span></span>|<span data-ttu-id="f3ec9-131">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="f3ec9-131">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
