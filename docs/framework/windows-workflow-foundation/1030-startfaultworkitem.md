---
description: 了解详细信息： 1030-StartFaultWorkItem
title: 1030 - StartFaultWorkItem
ms.date: 03/30/2017
ms.assetid: e1601fb9-0bc6-4dbe-816f-f24914063d34
ms.openlocfilehash: 2d148277b2d593cfcf75e17662626f1f486e7c1c
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99668092"
---
# <a name="1030---startfaultworkitem"></a><span data-ttu-id="3603c-103">1030 - StartFaultWorkItem</span><span class="sxs-lookup"><span data-stu-id="3603c-103">1030 - StartFaultWorkItem</span></span>

## <a name="properties"></a><span data-ttu-id="3603c-104">属性</span><span class="sxs-lookup"><span data-stu-id="3603c-104">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="3603c-105">ID</span><span class="sxs-lookup"><span data-stu-id="3603c-105">ID</span></span>|<span data-ttu-id="3603c-106">1030</span><span class="sxs-lookup"><span data-stu-id="3603c-106">1030</span></span>|  
|<span data-ttu-id="3603c-107">关键字</span><span class="sxs-lookup"><span data-stu-id="3603c-107">Keywords</span></span>|<span data-ttu-id="3603c-108">WFRuntime</span><span class="sxs-lookup"><span data-stu-id="3603c-108">WFRuntime</span></span>|  
|<span data-ttu-id="3603c-109">级别</span><span class="sxs-lookup"><span data-stu-id="3603c-109">Level</span></span>|<span data-ttu-id="3603c-110">“详细”</span><span class="sxs-lookup"><span data-stu-id="3603c-110">Verbose</span></span>|  
|<span data-ttu-id="3603c-111">通道</span><span class="sxs-lookup"><span data-stu-id="3603c-111">Channel</span></span>|<span data-ttu-id="3603c-112">Microsoft-Windows-应用程序服务器-应用程序/调试</span><span class="sxs-lookup"><span data-stu-id="3603c-112">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="3603c-113">说明</span><span class="sxs-lookup"><span data-stu-id="3603c-113">Description</span></span>  

 <span data-ttu-id="3603c-114">指示 FaultWorkItem 正在开始执行。</span><span class="sxs-lookup"><span data-stu-id="3603c-114">Indicates a FaultWorkItem is starting execution.</span></span>  
  
## <a name="message"></a><span data-ttu-id="3603c-115">消息</span><span class="sxs-lookup"><span data-stu-id="3603c-115">Message</span></span>  

 <span data-ttu-id="3603c-116">开始为 Activity "%1"、DisplayName "%2"、InstanceId "%3" 执行 FaultWorkItem。</span><span class="sxs-lookup"><span data-stu-id="3603c-116">Starting execution of a FaultWorkItem for Activity '%1', DisplayName: '%2', InstanceId: '%3'.</span></span>  <span data-ttu-id="3603c-117">异常是从 Activity“%4”、DisplayName“%5”、InstanceId“%6”传播的。</span><span class="sxs-lookup"><span data-stu-id="3603c-117">The exception was propagated from Activity '%4', DisplayName: '%5', InstanceId: '%6'.</span></span>  
  
## <a name="details"></a><span data-ttu-id="3603c-118">详细信息</span><span class="sxs-lookup"><span data-stu-id="3603c-118">Details</span></span>  
  
|<span data-ttu-id="3603c-119">数据项名称</span><span class="sxs-lookup"><span data-stu-id="3603c-119">Data Item Name</span></span>|<span data-ttu-id="3603c-120">数据项类型</span><span class="sxs-lookup"><span data-stu-id="3603c-120">Data Item Type</span></span>|<span data-ttu-id="3603c-121">说明</span><span class="sxs-lookup"><span data-stu-id="3603c-121">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="3603c-122">FaultActivity</span><span class="sxs-lookup"><span data-stu-id="3603c-122">FaultActivity</span></span>|<span data-ttu-id="3603c-123">xs:string</span><span class="sxs-lookup"><span data-stu-id="3603c-123">xs:string</span></span>|<span data-ttu-id="3603c-124">错误活动的类型名称。</span><span class="sxs-lookup"><span data-stu-id="3603c-124">The type name of the fault activity.</span></span>|  
|<span data-ttu-id="3603c-125">FaultActivityDisplayName</span><span class="sxs-lookup"><span data-stu-id="3603c-125">FaultActivityDisplayName</span></span>|<span data-ttu-id="3603c-126">xs:string</span><span class="sxs-lookup"><span data-stu-id="3603c-126">xs:string</span></span>|<span data-ttu-id="3603c-127">错误活动的显示名称。</span><span class="sxs-lookup"><span data-stu-id="3603c-127">The display name of the fault activity.</span></span>|  
|<span data-ttu-id="3603c-128">FaultActivityInstanceId</span><span class="sxs-lookup"><span data-stu-id="3603c-128">FaultActivityInstanceId</span></span>|<span data-ttu-id="3603c-129">xs:string</span><span class="sxs-lookup"><span data-stu-id="3603c-129">xs:string</span></span>|<span data-ttu-id="3603c-130">错误活动的实例 ID。</span><span class="sxs-lookup"><span data-stu-id="3603c-130">The instance id of the fault activity.</span></span>|  
|<span data-ttu-id="3603c-131">ExceptionActivity</span><span class="sxs-lookup"><span data-stu-id="3603c-131">ExceptionActivity</span></span>|<span data-ttu-id="3603c-132">xs:string</span><span class="sxs-lookup"><span data-stu-id="3603c-132">xs:string</span></span>|<span data-ttu-id="3603c-133">引发了异常的活动的类型名称。</span><span class="sxs-lookup"><span data-stu-id="3603c-133">The type name of the activity that threw the exception.</span></span>|  
|<span data-ttu-id="3603c-134">ExceptionActivityDisplayName</span><span class="sxs-lookup"><span data-stu-id="3603c-134">ExceptionActivityDisplayName</span></span>|<span data-ttu-id="3603c-135">xs:string</span><span class="sxs-lookup"><span data-stu-id="3603c-135">xs:string</span></span>|<span data-ttu-id="3603c-136">引发了异常的活动的显示名称。</span><span class="sxs-lookup"><span data-stu-id="3603c-136">The display name of the activity that threw the exception.</span></span>|  
|<span data-ttu-id="3603c-137">ExceptionActivityInstanceId</span><span class="sxs-lookup"><span data-stu-id="3603c-137">ExceptionActivityInstanceId</span></span>|<span data-ttu-id="3603c-138">xs:string</span><span class="sxs-lookup"><span data-stu-id="3603c-138">xs:string</span></span>|<span data-ttu-id="3603c-139">引发了异常的活动的实例 ID。</span><span class="sxs-lookup"><span data-stu-id="3603c-139">The instance id of the activity that threw the exception.</span></span>|  
|<span data-ttu-id="3603c-140">异常</span><span class="sxs-lookup"><span data-stu-id="3603c-140">Exception</span></span>|<span data-ttu-id="3603c-141">xs:string</span><span class="sxs-lookup"><span data-stu-id="3603c-141">xs:string</span></span>|<span data-ttu-id="3603c-142">异常的异常详细信息</span><span class="sxs-lookup"><span data-stu-id="3603c-142">The exception details for the exception</span></span>|  
|<span data-ttu-id="3603c-143">应用程序域</span><span class="sxs-lookup"><span data-stu-id="3603c-143">AppDomain</span></span>|<span data-ttu-id="3603c-144">xs:string</span><span class="sxs-lookup"><span data-stu-id="3603c-144">xs:string</span></span>|<span data-ttu-id="3603c-145">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="3603c-145">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
