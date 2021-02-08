---
description: 了解详细信息： 1017-ScheduleCancelActivityWorkItem
title: 1017 - ScheduleCancelActivityWorkItem
ms.date: 03/30/2017
ms.assetid: 864546ab-d65c-4989-8fcb-537ba03a3cdd
ms.openlocfilehash: 04dc4f663ceed1d7350dd14867e4926042bd11af
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99792890"
---
# <a name="1017---schedulecancelactivityworkitem"></a><span data-ttu-id="8c8e7-103">1017 - ScheduleCancelActivityWorkItem</span><span class="sxs-lookup"><span data-stu-id="8c8e7-103">1017 - ScheduleCancelActivityWorkItem</span></span>

## <a name="properties"></a><span data-ttu-id="8c8e7-104">属性</span><span class="sxs-lookup"><span data-stu-id="8c8e7-104">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="8c8e7-105">ID</span><span class="sxs-lookup"><span data-stu-id="8c8e7-105">ID</span></span>|<span data-ttu-id="8c8e7-106">1017</span><span class="sxs-lookup"><span data-stu-id="8c8e7-106">1017</span></span>|  
|<span data-ttu-id="8c8e7-107">关键字</span><span class="sxs-lookup"><span data-stu-id="8c8e7-107">Keywords</span></span>|<span data-ttu-id="8c8e7-108">WFRuntime</span><span class="sxs-lookup"><span data-stu-id="8c8e7-108">WFRuntime</span></span>|  
|<span data-ttu-id="8c8e7-109">级别</span><span class="sxs-lookup"><span data-stu-id="8c8e7-109">Level</span></span>|<span data-ttu-id="8c8e7-110">“详细”</span><span class="sxs-lookup"><span data-stu-id="8c8e7-110">Verbose</span></span>|  
|<span data-ttu-id="8c8e7-111">通道</span><span class="sxs-lookup"><span data-stu-id="8c8e7-111">Channel</span></span>|<span data-ttu-id="8c8e7-112">Microsoft-Windows-应用程序服务器-应用程序/调试</span><span class="sxs-lookup"><span data-stu-id="8c8e7-112">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="8c8e7-113">说明</span><span class="sxs-lookup"><span data-stu-id="8c8e7-113">Description</span></span>  

 <span data-ttu-id="8c8e7-114">指示已安排 CancelActivityWorkItem。</span><span class="sxs-lookup"><span data-stu-id="8c8e7-114">Indicates a CancelActivityWorkItem has been scheduled.</span></span>  
  
## <a name="message"></a><span data-ttu-id="8c8e7-115">消息</span><span class="sxs-lookup"><span data-stu-id="8c8e7-115">Message</span></span>  

 <span data-ttu-id="8c8e7-116">已为 Activity“%1”、DisplayName“%2”、InstanceId“%3”安排了 CancelActivityWorkItem。</span><span class="sxs-lookup"><span data-stu-id="8c8e7-116">A CancelActivityWorkItem has been scheduled for Activity '%1', DisplayName: '%2', InstanceId: '%3'.</span></span>  
  
## <a name="details"></a><span data-ttu-id="8c8e7-117">详细信息</span><span class="sxs-lookup"><span data-stu-id="8c8e7-117">Details</span></span>  
  
|<span data-ttu-id="8c8e7-118">数据项名称</span><span class="sxs-lookup"><span data-stu-id="8c8e7-118">Data Item Name</span></span>|<span data-ttu-id="8c8e7-119">数据项类型</span><span class="sxs-lookup"><span data-stu-id="8c8e7-119">Data Item Type</span></span>|<span data-ttu-id="8c8e7-120">说明</span><span class="sxs-lookup"><span data-stu-id="8c8e7-120">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="8c8e7-121">活动</span><span class="sxs-lookup"><span data-stu-id="8c8e7-121">Activity</span></span>|<span data-ttu-id="8c8e7-122">xs:string</span><span class="sxs-lookup"><span data-stu-id="8c8e7-122">xs:string</span></span>|<span data-ttu-id="8c8e7-123">活动的类型名称。</span><span class="sxs-lookup"><span data-stu-id="8c8e7-123">The type name of the activity.</span></span>|  
|<span data-ttu-id="8c8e7-124">DisplayName</span><span class="sxs-lookup"><span data-stu-id="8c8e7-124">DisplayName</span></span>|<span data-ttu-id="8c8e7-125">xs:string</span><span class="sxs-lookup"><span data-stu-id="8c8e7-125">xs:string</span></span>|<span data-ttu-id="8c8e7-126">活动的显示名称。</span><span class="sxs-lookup"><span data-stu-id="8c8e7-126">The display name of the activity.</span></span>|  
|<span data-ttu-id="8c8e7-127">InstanceId</span><span class="sxs-lookup"><span data-stu-id="8c8e7-127">InstanceId</span></span>|<span data-ttu-id="8c8e7-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="8c8e7-128">xs:string</span></span>|<span data-ttu-id="8c8e7-129">活动的实例 ID。</span><span class="sxs-lookup"><span data-stu-id="8c8e7-129">The instance id of the activity.</span></span>|  
|<span data-ttu-id="8c8e7-130">应用程序域</span><span class="sxs-lookup"><span data-stu-id="8c8e7-130">AppDomain</span></span>|<span data-ttu-id="8c8e7-131">xs:string</span><span class="sxs-lookup"><span data-stu-id="8c8e7-131">xs:string</span></span>|<span data-ttu-id="8c8e7-132">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="8c8e7-132">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
