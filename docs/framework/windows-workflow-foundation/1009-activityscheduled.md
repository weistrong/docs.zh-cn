---
description: 了解详细信息： 1009-ActivityScheduled
title: 1009 - ActivityScheduled
ms.date: 03/30/2017
ms.assetid: 307e38b6-d47e-47a4-9708-e74d8314b1a1
ms.openlocfilehash: 80ee250955a03927fb9db2b1242d420be77a6df8
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99755546"
---
# <a name="1009---activityscheduled"></a><span data-ttu-id="ccec6-103">1009 - ActivityScheduled</span><span class="sxs-lookup"><span data-stu-id="ccec6-103">1009 - ActivityScheduled</span></span>

## <a name="properties"></a><span data-ttu-id="ccec6-104">属性</span><span class="sxs-lookup"><span data-stu-id="ccec6-104">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="ccec6-105">ID</span><span class="sxs-lookup"><span data-stu-id="ccec6-105">ID</span></span>|<span data-ttu-id="ccec6-106">1009</span><span class="sxs-lookup"><span data-stu-id="ccec6-106">1009</span></span>|  
|<span data-ttu-id="ccec6-107">关键字</span><span class="sxs-lookup"><span data-stu-id="ccec6-107">Keywords</span></span>|<span data-ttu-id="ccec6-108">WFRuntime</span><span class="sxs-lookup"><span data-stu-id="ccec6-108">WFRuntime</span></span>|  
|<span data-ttu-id="ccec6-109">级别</span><span class="sxs-lookup"><span data-stu-id="ccec6-109">Level</span></span>|<span data-ttu-id="ccec6-110">信息</span><span class="sxs-lookup"><span data-stu-id="ccec6-110">Information</span></span>|  
|<span data-ttu-id="ccec6-111">通道</span><span class="sxs-lookup"><span data-stu-id="ccec6-111">Channel</span></span>|<span data-ttu-id="ccec6-112">Microsoft-Windows-应用程序服务器-应用程序/调试</span><span class="sxs-lookup"><span data-stu-id="ccec6-112">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="ccec6-113">说明</span><span class="sxs-lookup"><span data-stu-id="ccec6-113">Description</span></span>  

 <span data-ttu-id="ccec6-114">指示正在安排某一活动的执行。</span><span class="sxs-lookup"><span data-stu-id="ccec6-114">Indicates an activity is being scheduled for execution.</span></span>  
  
## <a name="message"></a><span data-ttu-id="ccec6-115">消息</span><span class="sxs-lookup"><span data-stu-id="ccec6-115">Message</span></span>  

 <span data-ttu-id="ccec6-116">父 Activity“%1”、DisplayName“%2”、InstanceId“%3”安排了子 Activity“%4”、DisplayName“%5”、InstanceId“%6”。</span><span class="sxs-lookup"><span data-stu-id="ccec6-116">Parent Activity '%1', DisplayName: '%2', InstanceId: '%3' scheduled child Activity '%4', DisplayName: '%5', InstanceId: '%6'.</span></span>  
  
## <a name="details"></a><span data-ttu-id="ccec6-117">详细信息</span><span class="sxs-lookup"><span data-stu-id="ccec6-117">Details</span></span>  
  
|<span data-ttu-id="ccec6-118">数据项名称</span><span class="sxs-lookup"><span data-stu-id="ccec6-118">Data Item Name</span></span>|<span data-ttu-id="ccec6-119">数据项类型</span><span class="sxs-lookup"><span data-stu-id="ccec6-119">Data Item Type</span></span>|<span data-ttu-id="ccec6-120">说明</span><span class="sxs-lookup"><span data-stu-id="ccec6-120">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="ccec6-121">ParentActivity</span><span class="sxs-lookup"><span data-stu-id="ccec6-121">ParentActivity</span></span>|<span data-ttu-id="ccec6-122">xs:string</span><span class="sxs-lookup"><span data-stu-id="ccec6-122">xs:string</span></span>|<span data-ttu-id="ccec6-123">父活动的类型名称。</span><span class="sxs-lookup"><span data-stu-id="ccec6-123">The type name of the parent activity.</span></span>|  
|<span data-ttu-id="ccec6-124">ParentDisplayName</span><span class="sxs-lookup"><span data-stu-id="ccec6-124">ParentDisplayName</span></span>|<span data-ttu-id="ccec6-125">xs:string</span><span class="sxs-lookup"><span data-stu-id="ccec6-125">xs:string</span></span>|<span data-ttu-id="ccec6-126">父活动的显示名称。</span><span class="sxs-lookup"><span data-stu-id="ccec6-126">The display name of the parent activity.</span></span>|  
|<span data-ttu-id="ccec6-127">ParentInstanceId</span><span class="sxs-lookup"><span data-stu-id="ccec6-127">ParentInstanceId</span></span>|<span data-ttu-id="ccec6-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="ccec6-128">xs:string</span></span>|<span data-ttu-id="ccec6-129">父活动的实例 ID。</span><span class="sxs-lookup"><span data-stu-id="ccec6-129">The instance id of the parent activity.</span></span>|  
|<span data-ttu-id="ccec6-130">ChildActivity</span><span class="sxs-lookup"><span data-stu-id="ccec6-130">ChildActivity</span></span>|<span data-ttu-id="ccec6-131">xs:string</span><span class="sxs-lookup"><span data-stu-id="ccec6-131">xs:string</span></span>|<span data-ttu-id="ccec6-132">所安排子活动的类型名称。</span><span class="sxs-lookup"><span data-stu-id="ccec6-132">The type name of the scheduled child activity.</span></span>|  
|<span data-ttu-id="ccec6-133">ChildDisplayName</span><span class="sxs-lookup"><span data-stu-id="ccec6-133">ChildDisplayName</span></span>|<span data-ttu-id="ccec6-134">xs:string</span><span class="sxs-lookup"><span data-stu-id="ccec6-134">xs:string</span></span>|<span data-ttu-id="ccec6-135">所安排子活动的显示名称。</span><span class="sxs-lookup"><span data-stu-id="ccec6-135">The display name of the scheduled child activity.</span></span>|  
|<span data-ttu-id="ccec6-136">ChildInstanceId</span><span class="sxs-lookup"><span data-stu-id="ccec6-136">ChildInstanceId</span></span>|<span data-ttu-id="ccec6-137">xs:string</span><span class="sxs-lookup"><span data-stu-id="ccec6-137">xs:string</span></span>|<span data-ttu-id="ccec6-138">所安排子活动的实例 ID。</span><span class="sxs-lookup"><span data-stu-id="ccec6-138">The instance id of the scheduled child activity.</span></span>|  
|<span data-ttu-id="ccec6-139">应用程序域</span><span class="sxs-lookup"><span data-stu-id="ccec6-139">AppDomain</span></span>|<span data-ttu-id="ccec6-140">xs:string</span><span class="sxs-lookup"><span data-stu-id="ccec6-140">xs:string</span></span>|<span data-ttu-id="ccec6-141">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="ccec6-141">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
