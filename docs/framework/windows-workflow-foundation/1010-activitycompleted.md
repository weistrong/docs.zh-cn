---
description: 了解详细信息： 1010-ActivityCompleted
title: 1010 - ActivityCompleted
ms.date: 03/30/2017
ms.assetid: d256284e-3fd2-4c33-82f4-abb617575706
ms.openlocfilehash: c72339449b94b0ea5d6d8fa227b606cc25c29704
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99755533"
---
# <a name="1010---activitycompleted"></a><span data-ttu-id="d8f12-103">1010 - ActivityCompleted</span><span class="sxs-lookup"><span data-stu-id="d8f12-103">1010 - ActivityCompleted</span></span>

## <a name="properties"></a><span data-ttu-id="d8f12-104">属性</span><span class="sxs-lookup"><span data-stu-id="d8f12-104">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="d8f12-105">ID</span><span class="sxs-lookup"><span data-stu-id="d8f12-105">ID</span></span>|<span data-ttu-id="d8f12-106">1010</span><span class="sxs-lookup"><span data-stu-id="d8f12-106">1010</span></span>|  
|<span data-ttu-id="d8f12-107">关键字</span><span class="sxs-lookup"><span data-stu-id="d8f12-107">Keywords</span></span>|<span data-ttu-id="d8f12-108">WFRuntime</span><span class="sxs-lookup"><span data-stu-id="d8f12-108">WFRuntime</span></span>|  
|<span data-ttu-id="d8f12-109">级别</span><span class="sxs-lookup"><span data-stu-id="d8f12-109">Level</span></span>|<span data-ttu-id="d8f12-110">信息</span><span class="sxs-lookup"><span data-stu-id="d8f12-110">Information</span></span>|  
|<span data-ttu-id="d8f12-111">通道</span><span class="sxs-lookup"><span data-stu-id="d8f12-111">Channel</span></span>|<span data-ttu-id="d8f12-112">Microsoft-Windows-应用程序服务器-应用程序/调试</span><span class="sxs-lookup"><span data-stu-id="d8f12-112">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="d8f12-113">说明</span><span class="sxs-lookup"><span data-stu-id="d8f12-113">Description</span></span>  

 <span data-ttu-id="d8f12-114">指示活动已完成执行。</span><span class="sxs-lookup"><span data-stu-id="d8f12-114">Indicates an activity has completed execution.</span></span>  
  
## <a name="message"></a><span data-ttu-id="d8f12-115">消息</span><span class="sxs-lookup"><span data-stu-id="d8f12-115">Message</span></span>  

 <span data-ttu-id="d8f12-116">Activity“%1”、DisplayName“%2”、InstanceId“%3”在“%4”状态下完成。</span><span class="sxs-lookup"><span data-stu-id="d8f12-116">Activity '%1', DisplayName: '%2', InstanceId: '%3' has completed in the '%4' state.</span></span>  
  
## <a name="details"></a><span data-ttu-id="d8f12-117">详细信息</span><span class="sxs-lookup"><span data-stu-id="d8f12-117">Details</span></span>  
  
|<span data-ttu-id="d8f12-118">数据项名称</span><span class="sxs-lookup"><span data-stu-id="d8f12-118">Data Item Name</span></span>|<span data-ttu-id="d8f12-119">数据项类型</span><span class="sxs-lookup"><span data-stu-id="d8f12-119">Data Item Type</span></span>|<span data-ttu-id="d8f12-120">说明</span><span class="sxs-lookup"><span data-stu-id="d8f12-120">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="d8f12-121">活动</span><span class="sxs-lookup"><span data-stu-id="d8f12-121">Activity</span></span>|<span data-ttu-id="d8f12-122">xs:string</span><span class="sxs-lookup"><span data-stu-id="d8f12-122">xs:string</span></span>|<span data-ttu-id="d8f12-123">活动的类型名称。</span><span class="sxs-lookup"><span data-stu-id="d8f12-123">The type name of the activity.</span></span>|  
|<span data-ttu-id="d8f12-124">DisplayName</span><span class="sxs-lookup"><span data-stu-id="d8f12-124">DisplayName</span></span>|<span data-ttu-id="d8f12-125">xs:string</span><span class="sxs-lookup"><span data-stu-id="d8f12-125">xs:string</span></span>|<span data-ttu-id="d8f12-126">活动的显示名称。</span><span class="sxs-lookup"><span data-stu-id="d8f12-126">The display name of the activity.</span></span>|  
|<span data-ttu-id="d8f12-127">InstanceId</span><span class="sxs-lookup"><span data-stu-id="d8f12-127">InstanceId</span></span>|<span data-ttu-id="d8f12-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="d8f12-128">xs:string</span></span>|<span data-ttu-id="d8f12-129">活动的实例 ID。</span><span class="sxs-lookup"><span data-stu-id="d8f12-129">The instance id of the activity.</span></span>|  
|<span data-ttu-id="d8f12-130">状态</span><span class="sxs-lookup"><span data-stu-id="d8f12-130">State</span></span>|<span data-ttu-id="d8f12-131">xs:string</span><span class="sxs-lookup"><span data-stu-id="d8f12-131">xs:string</span></span>|<span data-ttu-id="d8f12-132">活动的状态。</span><span class="sxs-lookup"><span data-stu-id="d8f12-132">The state of the activity.</span></span>|  
|<span data-ttu-id="d8f12-133">应用程序域</span><span class="sxs-lookup"><span data-stu-id="d8f12-133">AppDomain</span></span>|<span data-ttu-id="d8f12-134">xs:string</span><span class="sxs-lookup"><span data-stu-id="d8f12-134">xs:string</span></span>|<span data-ttu-id="d8f12-135">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="d8f12-135">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
