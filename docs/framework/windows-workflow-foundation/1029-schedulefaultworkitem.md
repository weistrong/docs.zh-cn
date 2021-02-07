---
description: 了解详细信息： 1029-ScheduleFaultWorkItem
title: 1029 - ScheduleFaultWorkItem
ms.date: 03/30/2017
ms.assetid: 3a56b29e-f740-459d-8576-d81e58bf5a03
ms.openlocfilehash: e5f0463626882d6c8c48412326582fafa7be4670
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99755442"
---
# <a name="1029---schedulefaultworkitem"></a><span data-ttu-id="2b482-103">1029 - ScheduleFaultWorkItem</span><span class="sxs-lookup"><span data-stu-id="2b482-103">1029 - ScheduleFaultWorkItem</span></span>

## <a name="properties"></a><span data-ttu-id="2b482-104">属性</span><span class="sxs-lookup"><span data-stu-id="2b482-104">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="2b482-105">ID</span><span class="sxs-lookup"><span data-stu-id="2b482-105">ID</span></span>|<span data-ttu-id="2b482-106">1029</span><span class="sxs-lookup"><span data-stu-id="2b482-106">1029</span></span>|  
|<span data-ttu-id="2b482-107">关键字</span><span class="sxs-lookup"><span data-stu-id="2b482-107">Keywords</span></span>|<span data-ttu-id="2b482-108">WFRuntime</span><span class="sxs-lookup"><span data-stu-id="2b482-108">WFRuntime</span></span>|  
|<span data-ttu-id="2b482-109">级别</span><span class="sxs-lookup"><span data-stu-id="2b482-109">Level</span></span>|<span data-ttu-id="2b482-110">“详细”</span><span class="sxs-lookup"><span data-stu-id="2b482-110">Verbose</span></span>|  
|<span data-ttu-id="2b482-111">通道</span><span class="sxs-lookup"><span data-stu-id="2b482-111">Channel</span></span>|<span data-ttu-id="2b482-112">Microsoft-Windows-应用程序服务器-应用程序/调试</span><span class="sxs-lookup"><span data-stu-id="2b482-112">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="2b482-113">说明</span><span class="sxs-lookup"><span data-stu-id="2b482-113">Description</span></span>  

 <span data-ttu-id="2b482-114">指示已安排 FaultWorkItem。</span><span class="sxs-lookup"><span data-stu-id="2b482-114">Indicates a FaultWorkItem has been scheduled.</span></span>  
  
## <a name="message"></a><span data-ttu-id="2b482-115">消息</span><span class="sxs-lookup"><span data-stu-id="2b482-115">Message</span></span>  

 <span data-ttu-id="2b482-116">已为 Activity "%1"、DisplayName "%2"、InstanceId "%3" 安排了 FaultWorkItem。</span><span class="sxs-lookup"><span data-stu-id="2b482-116">A FaultWorkItem has been scheduled for Activity '%1', DisplayName: '%2', InstanceId: '%3'.</span></span>  <span data-ttu-id="2b482-117">异常是从 Activity“%4”、DisplayName“%5”、InstanceId“%6”传播的。</span><span class="sxs-lookup"><span data-stu-id="2b482-117">The exception was propagated from Activity '%4', DisplayName: '%5', InstanceId: '%6'.</span></span>  
  
## <a name="details"></a><span data-ttu-id="2b482-118">详细信息</span><span class="sxs-lookup"><span data-stu-id="2b482-118">Details</span></span>  
  
|<span data-ttu-id="2b482-119">数据项名称</span><span class="sxs-lookup"><span data-stu-id="2b482-119">Data Item Name</span></span>|<span data-ttu-id="2b482-120">数据项类型</span><span class="sxs-lookup"><span data-stu-id="2b482-120">Data Item Type</span></span>|<span data-ttu-id="2b482-121">说明</span><span class="sxs-lookup"><span data-stu-id="2b482-121">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="2b482-122">FaultActivity</span><span class="sxs-lookup"><span data-stu-id="2b482-122">FaultActivity</span></span>|<span data-ttu-id="2b482-123">xs:string</span><span class="sxs-lookup"><span data-stu-id="2b482-123">xs:string</span></span>|<span data-ttu-id="2b482-124">错误活动的类型名称。</span><span class="sxs-lookup"><span data-stu-id="2b482-124">The type name of the fault activity.</span></span>|  
|<span data-ttu-id="2b482-125">FaultActivityDisplayName</span><span class="sxs-lookup"><span data-stu-id="2b482-125">FaultActivityDisplayName</span></span>|<span data-ttu-id="2b482-126">xs:string</span><span class="sxs-lookup"><span data-stu-id="2b482-126">xs:string</span></span>|<span data-ttu-id="2b482-127">错误活动的显示名称。</span><span class="sxs-lookup"><span data-stu-id="2b482-127">The display name of the fault activity.</span></span>|  
|<span data-ttu-id="2b482-128">FaultActivityInstanceId</span><span class="sxs-lookup"><span data-stu-id="2b482-128">FaultActivityInstanceId</span></span>|<span data-ttu-id="2b482-129">xs:string</span><span class="sxs-lookup"><span data-stu-id="2b482-129">xs:string</span></span>|<span data-ttu-id="2b482-130">错误活动的实例 ID。</span><span class="sxs-lookup"><span data-stu-id="2b482-130">The instance id of the fault activity.</span></span>|  
|<span data-ttu-id="2b482-131">ExceptionActivity</span><span class="sxs-lookup"><span data-stu-id="2b482-131">ExceptionActivity</span></span>|<span data-ttu-id="2b482-132">xs:string</span><span class="sxs-lookup"><span data-stu-id="2b482-132">xs:string</span></span>|<span data-ttu-id="2b482-133">引发了异常的活动的类型名称。</span><span class="sxs-lookup"><span data-stu-id="2b482-133">The type name of the activity that threw the exception.</span></span>|  
|<span data-ttu-id="2b482-134">ExceptionActivityDisplayName</span><span class="sxs-lookup"><span data-stu-id="2b482-134">ExceptionActivityDisplayName</span></span>|<span data-ttu-id="2b482-135">xs:string</span><span class="sxs-lookup"><span data-stu-id="2b482-135">xs:string</span></span>|<span data-ttu-id="2b482-136">引发了异常的活动的显示名称。</span><span class="sxs-lookup"><span data-stu-id="2b482-136">The display name of the activity that threw the exception.</span></span>|  
|<span data-ttu-id="2b482-137">ExceptionActivityInstanceId</span><span class="sxs-lookup"><span data-stu-id="2b482-137">ExceptionActivityInstanceId</span></span>|<span data-ttu-id="2b482-138">xs:string</span><span class="sxs-lookup"><span data-stu-id="2b482-138">xs:string</span></span>|<span data-ttu-id="2b482-139">引发了异常的活动的实例 ID。</span><span class="sxs-lookup"><span data-stu-id="2b482-139">The instance id of the activity that threw the exception.</span></span>|  
|<span data-ttu-id="2b482-140">异常</span><span class="sxs-lookup"><span data-stu-id="2b482-140">Exception</span></span>|<span data-ttu-id="2b482-141">xs:string</span><span class="sxs-lookup"><span data-stu-id="2b482-141">xs:string</span></span>|<span data-ttu-id="2b482-142">异常的异常详细信息</span><span class="sxs-lookup"><span data-stu-id="2b482-142">The exception details for the exception</span></span>|  
|<span data-ttu-id="2b482-143">应用程序域</span><span class="sxs-lookup"><span data-stu-id="2b482-143">AppDomain</span></span>|<span data-ttu-id="2b482-144">xs:string</span><span class="sxs-lookup"><span data-stu-id="2b482-144">xs:string</span></span>|<span data-ttu-id="2b482-145">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="2b482-145">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
