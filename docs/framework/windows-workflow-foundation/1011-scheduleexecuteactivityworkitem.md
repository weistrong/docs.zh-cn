---
description: 了解详细信息： 1011-ScheduleExecuteActivityWorkItem
title: 1011 - ScheduleExecuteActivityWorkItem
ms.date: 03/30/2017
ms.assetid: e503ae46-ad6b-4fcb-8c0e-146d59a8eff1
ms.openlocfilehash: 81010390de2ad01ec3063f2ac89608b97dcb713e
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99703349"
---
# <a name="1011---scheduleexecuteactivityworkitem"></a><span data-ttu-id="c7762-103">1011 - ScheduleExecuteActivityWorkItem</span><span class="sxs-lookup"><span data-stu-id="c7762-103">1011 - ScheduleExecuteActivityWorkItem</span></span>

## <a name="properties"></a><span data-ttu-id="c7762-104">属性</span><span class="sxs-lookup"><span data-stu-id="c7762-104">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="c7762-105">ID</span><span class="sxs-lookup"><span data-stu-id="c7762-105">ID</span></span>|<span data-ttu-id="c7762-106">1011</span><span class="sxs-lookup"><span data-stu-id="c7762-106">1011</span></span>|  
|<span data-ttu-id="c7762-107">关键字</span><span class="sxs-lookup"><span data-stu-id="c7762-107">Keywords</span></span>|<span data-ttu-id="c7762-108">WFRuntime</span><span class="sxs-lookup"><span data-stu-id="c7762-108">WFRuntime</span></span>|  
|<span data-ttu-id="c7762-109">级别</span><span class="sxs-lookup"><span data-stu-id="c7762-109">Level</span></span>|<span data-ttu-id="c7762-110">“详细”</span><span class="sxs-lookup"><span data-stu-id="c7762-110">Verbose</span></span>|  
|<span data-ttu-id="c7762-111">通道</span><span class="sxs-lookup"><span data-stu-id="c7762-111">Channel</span></span>|<span data-ttu-id="c7762-112">Microsoft-Windows-应用程序服务器-应用程序/调试</span><span class="sxs-lookup"><span data-stu-id="c7762-112">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="c7762-113">说明</span><span class="sxs-lookup"><span data-stu-id="c7762-113">Description</span></span>  

 <span data-ttu-id="c7762-114">指示已安排 ExecuteActivityWorkItem。</span><span class="sxs-lookup"><span data-stu-id="c7762-114">Indicates an ExecuteActivityWorkItem has been scheduled.</span></span>  
  
## <a name="message"></a><span data-ttu-id="c7762-115">消息</span><span class="sxs-lookup"><span data-stu-id="c7762-115">Message</span></span>  

 <span data-ttu-id="c7762-116">已为 Activity“%1”、DisplayName“%2”、InstanceId“%3”安排了 ExecuteActivityWorkItem。</span><span class="sxs-lookup"><span data-stu-id="c7762-116">An ExecuteActivityWorkItem has been scheduled for Activity '%1', DisplayName: '%2', InstanceId: '%3'.</span></span>  
  
## <a name="details"></a><span data-ttu-id="c7762-117">详细信息</span><span class="sxs-lookup"><span data-stu-id="c7762-117">Details</span></span>  
  
|<span data-ttu-id="c7762-118">数据项名称</span><span class="sxs-lookup"><span data-stu-id="c7762-118">Data Item Name</span></span>|<span data-ttu-id="c7762-119">数据项类型</span><span class="sxs-lookup"><span data-stu-id="c7762-119">Data Item Type</span></span>|<span data-ttu-id="c7762-120">说明</span><span class="sxs-lookup"><span data-stu-id="c7762-120">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="c7762-121">活动</span><span class="sxs-lookup"><span data-stu-id="c7762-121">Activity</span></span>|<span data-ttu-id="c7762-122">xs:string</span><span class="sxs-lookup"><span data-stu-id="c7762-122">xs:string</span></span>|<span data-ttu-id="c7762-123">活动的类型名称。</span><span class="sxs-lookup"><span data-stu-id="c7762-123">The type name of the activity.</span></span>|  
|<span data-ttu-id="c7762-124">DisplayName</span><span class="sxs-lookup"><span data-stu-id="c7762-124">DisplayName</span></span>|<span data-ttu-id="c7762-125">xs:string</span><span class="sxs-lookup"><span data-stu-id="c7762-125">xs:string</span></span>|<span data-ttu-id="c7762-126">活动的显示名称。</span><span class="sxs-lookup"><span data-stu-id="c7762-126">The display name of the activity.</span></span>|  
|<span data-ttu-id="c7762-127">InstanceId</span><span class="sxs-lookup"><span data-stu-id="c7762-127">InstanceId</span></span>|<span data-ttu-id="c7762-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="c7762-128">xs:string</span></span>|<span data-ttu-id="c7762-129">活动的实例 ID。</span><span class="sxs-lookup"><span data-stu-id="c7762-129">The instance id of the activity.</span></span>|  
|<span data-ttu-id="c7762-130">应用程序域</span><span class="sxs-lookup"><span data-stu-id="c7762-130">AppDomain</span></span>|<span data-ttu-id="c7762-131">xs:string</span><span class="sxs-lookup"><span data-stu-id="c7762-131">xs:string</span></span>|<span data-ttu-id="c7762-132">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="c7762-132">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
