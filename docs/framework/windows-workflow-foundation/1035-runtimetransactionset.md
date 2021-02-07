---
description: 了解详细信息： 1035-RuntimeTransactionSet
title: 1035 - RuntimeTransactionSet
ms.date: 03/30/2017
ms.assetid: 03b37de9-778c-4beb-b0e3-de73ece6088e
ms.openlocfilehash: 513ba49962a8f02ab47b8e5b762949cd09154a3c
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99667897"
---
# <a name="1035---runtimetransactionset"></a><span data-ttu-id="86bcb-103">1035 - RuntimeTransactionSet</span><span class="sxs-lookup"><span data-stu-id="86bcb-103">1035 - RuntimeTransactionSet</span></span>

## <a name="properties"></a><span data-ttu-id="86bcb-104">属性</span><span class="sxs-lookup"><span data-stu-id="86bcb-104">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="86bcb-105">ID</span><span class="sxs-lookup"><span data-stu-id="86bcb-105">ID</span></span>|<span data-ttu-id="86bcb-106">1035</span><span class="sxs-lookup"><span data-stu-id="86bcb-106">1035</span></span>|  
|<span data-ttu-id="86bcb-107">关键字</span><span class="sxs-lookup"><span data-stu-id="86bcb-107">Keywords</span></span>|<span data-ttu-id="86bcb-108">WFRuntime</span><span class="sxs-lookup"><span data-stu-id="86bcb-108">WFRuntime</span></span>|  
|<span data-ttu-id="86bcb-109">级别</span><span class="sxs-lookup"><span data-stu-id="86bcb-109">Level</span></span>|<span data-ttu-id="86bcb-110">“详细”</span><span class="sxs-lookup"><span data-stu-id="86bcb-110">Verbose</span></span>|  
|<span data-ttu-id="86bcb-111">通道</span><span class="sxs-lookup"><span data-stu-id="86bcb-111">Channel</span></span>|<span data-ttu-id="86bcb-112">Microsoft-Windows-应用程序服务器-应用程序/调试</span><span class="sxs-lookup"><span data-stu-id="86bcb-112">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="86bcb-113">说明</span><span class="sxs-lookup"><span data-stu-id="86bcb-113">Description</span></span>  

 <span data-ttu-id="86bcb-114">指示活动已设置为运行时事务。</span><span class="sxs-lookup"><span data-stu-id="86bcb-114">Indicates an activity has set the runtime transaction.</span></span>  
  
## <a name="message"></a><span data-ttu-id="86bcb-115">消息</span><span class="sxs-lookup"><span data-stu-id="86bcb-115">Message</span></span>  

 <span data-ttu-id="86bcb-116">运行时事务已由 Activity "%1"、DisplayName "%2"、InstanceId "%3" 设置。</span><span class="sxs-lookup"><span data-stu-id="86bcb-116">The runtime transaction has been set by Activity '%1', DisplayName: '%2', InstanceId: '%3'.</span></span>  <span data-ttu-id="86bcb-117">执行操作与 Activity "%4"、DisplayName "%5"、InstanceId "%6" 隔离。</span><span class="sxs-lookup"><span data-stu-id="86bcb-117">Execution isolated to Activity '%4', DisplayName: '%5', InstanceId: '%6'.</span></span>  
  
## <a name="details"></a><span data-ttu-id="86bcb-118">详细信息</span><span class="sxs-lookup"><span data-stu-id="86bcb-118">Details</span></span>  
  
|<span data-ttu-id="86bcb-119">数据项名称</span><span class="sxs-lookup"><span data-stu-id="86bcb-119">Data Item Name</span></span>|<span data-ttu-id="86bcb-120">数据项类型</span><span class="sxs-lookup"><span data-stu-id="86bcb-120">Data Item Type</span></span>|<span data-ttu-id="86bcb-121">说明</span><span class="sxs-lookup"><span data-stu-id="86bcb-121">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="86bcb-122">活动</span><span class="sxs-lookup"><span data-stu-id="86bcb-122">Activity</span></span>|<span data-ttu-id="86bcb-123">xs:string</span><span class="sxs-lookup"><span data-stu-id="86bcb-123">xs:string</span></span>|<span data-ttu-id="86bcb-124">活动的类型名称。</span><span class="sxs-lookup"><span data-stu-id="86bcb-124">The type name of the activity.</span></span>|  
|<span data-ttu-id="86bcb-125">DisplayName</span><span class="sxs-lookup"><span data-stu-id="86bcb-125">DisplayName</span></span>|<span data-ttu-id="86bcb-126">xs:string</span><span class="sxs-lookup"><span data-stu-id="86bcb-126">xs:string</span></span>|<span data-ttu-id="86bcb-127">活动的显示名称。</span><span class="sxs-lookup"><span data-stu-id="86bcb-127">The display name of the activity.</span></span>|  
|<span data-ttu-id="86bcb-128">InstanceId</span><span class="sxs-lookup"><span data-stu-id="86bcb-128">InstanceId</span></span>|<span data-ttu-id="86bcb-129">xs:string</span><span class="sxs-lookup"><span data-stu-id="86bcb-129">xs:string</span></span>|<span data-ttu-id="86bcb-130">活动的实例 ID。</span><span class="sxs-lookup"><span data-stu-id="86bcb-130">The instance id of the activity.</span></span>|  
|<span data-ttu-id="86bcb-131">IsolatedActivity</span><span class="sxs-lookup"><span data-stu-id="86bcb-131">IsolatedActivity</span></span>|<span data-ttu-id="86bcb-132">xs:string</span><span class="sxs-lookup"><span data-stu-id="86bcb-132">xs:string</span></span>|<span data-ttu-id="86bcb-133">事务隔离到的活动的类型名称。</span><span class="sxs-lookup"><span data-stu-id="86bcb-133">The type name of the activity that the transaction is isolated to.</span></span>|  
|<span data-ttu-id="86bcb-134">IsolatedActivityDisplayName</span><span class="sxs-lookup"><span data-stu-id="86bcb-134">IsolatedActivityDisplayName</span></span>|<span data-ttu-id="86bcb-135">xs:string</span><span class="sxs-lookup"><span data-stu-id="86bcb-135">xs:string</span></span>|<span data-ttu-id="86bcb-136">事务隔离到的活动的显示名称。</span><span class="sxs-lookup"><span data-stu-id="86bcb-136">The display name of the activity that the transaction is isolated to.</span></span>|  
|<span data-ttu-id="86bcb-137">IsolatedActivityInstanceId</span><span class="sxs-lookup"><span data-stu-id="86bcb-137">IsolatedActivityInstanceId</span></span>|<span data-ttu-id="86bcb-138">xs:string</span><span class="sxs-lookup"><span data-stu-id="86bcb-138">xs:string</span></span>|<span data-ttu-id="86bcb-139">事务隔离到的活动的实例 ID。</span><span class="sxs-lookup"><span data-stu-id="86bcb-139">The instance id of the activity that the transaction is isolated to.</span></span>|  
|<span data-ttu-id="86bcb-140">应用程序域</span><span class="sxs-lookup"><span data-stu-id="86bcb-140">AppDomain</span></span>|<span data-ttu-id="86bcb-141">xs:string</span><span class="sxs-lookup"><span data-stu-id="86bcb-141">xs:string</span></span>|<span data-ttu-id="86bcb-142">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="86bcb-142">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
