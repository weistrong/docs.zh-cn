---
description: 了解详细信息： 1031-CompleteFaultWorkItem
title: 1031 - CompleteFaultWorkItem
ms.date: 03/30/2017
ms.assetid: 95f4ccb0-6be4-41f3-9330-fae43165828f
ms.openlocfilehash: dc5cb4988df2aab9710fd7ec875d9b4004bfa7af
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99668066"
---
# <a name="1031---completefaultworkitem"></a><span data-ttu-id="99d73-103">1031 - CompleteFaultWorkItem</span><span class="sxs-lookup"><span data-stu-id="99d73-103">1031 - CompleteFaultWorkItem</span></span>

## <a name="properties"></a><span data-ttu-id="99d73-104">属性</span><span class="sxs-lookup"><span data-stu-id="99d73-104">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="99d73-105">ID</span><span class="sxs-lookup"><span data-stu-id="99d73-105">ID</span></span>|<span data-ttu-id="99d73-106">1031</span><span class="sxs-lookup"><span data-stu-id="99d73-106">1031</span></span>|  
|<span data-ttu-id="99d73-107">关键字</span><span class="sxs-lookup"><span data-stu-id="99d73-107">Keywords</span></span>|<span data-ttu-id="99d73-108">WFRuntime</span><span class="sxs-lookup"><span data-stu-id="99d73-108">WFRuntime</span></span>|  
|<span data-ttu-id="99d73-109">级别</span><span class="sxs-lookup"><span data-stu-id="99d73-109">Level</span></span>|<span data-ttu-id="99d73-110">“详细”</span><span class="sxs-lookup"><span data-stu-id="99d73-110">Verbose</span></span>|  
|<span data-ttu-id="99d73-111">通道</span><span class="sxs-lookup"><span data-stu-id="99d73-111">Channel</span></span>|<span data-ttu-id="99d73-112">Microsoft-Windows-应用程序服务器-应用程序/调试</span><span class="sxs-lookup"><span data-stu-id="99d73-112">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="99d73-113">说明</span><span class="sxs-lookup"><span data-stu-id="99d73-113">Description</span></span>  

 <span data-ttu-id="99d73-114">指示 FaultWorkItem 已完成。</span><span class="sxs-lookup"><span data-stu-id="99d73-114">Indicates a FaultWorkItem has completed.</span></span>  
  
## <a name="message"></a><span data-ttu-id="99d73-115">消息</span><span class="sxs-lookup"><span data-stu-id="99d73-115">Message</span></span>  

 <span data-ttu-id="99d73-116">Activity“%1”、DisplayName“%2”、InstanceId“%3”的 FaultWorkItem 已经完成。</span><span class="sxs-lookup"><span data-stu-id="99d73-116">A FaultWorkItem has completed for Activity '%1', DisplayName: '%2', InstanceId: '%3'.</span></span> <span data-ttu-id="99d73-117">异常是从 Activity“%4”、DisplayName“%5”、InstanceId“%6”传播的。</span><span class="sxs-lookup"><span data-stu-id="99d73-117">The exception was propagated from Activity '%4', DisplayName: '%5', InstanceId: '%6'.</span></span>  
  
## <a name="details"></a><span data-ttu-id="99d73-118">详细信息</span><span class="sxs-lookup"><span data-stu-id="99d73-118">Details</span></span>  
  
|<span data-ttu-id="99d73-119">数据项名称</span><span class="sxs-lookup"><span data-stu-id="99d73-119">Data Item Name</span></span>|<span data-ttu-id="99d73-120">数据项类型</span><span class="sxs-lookup"><span data-stu-id="99d73-120">Data Item Type</span></span>|<span data-ttu-id="99d73-121">说明</span><span class="sxs-lookup"><span data-stu-id="99d73-121">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="99d73-122">FaultActivity</span><span class="sxs-lookup"><span data-stu-id="99d73-122">FaultActivity</span></span>|<span data-ttu-id="99d73-123">xs:string</span><span class="sxs-lookup"><span data-stu-id="99d73-123">xs:string</span></span>|<span data-ttu-id="99d73-124">错误活动的类型名称。</span><span class="sxs-lookup"><span data-stu-id="99d73-124">The type name of the fault activity.</span></span>|  
|<span data-ttu-id="99d73-125">FaultActivityDisplayName</span><span class="sxs-lookup"><span data-stu-id="99d73-125">FaultActivityDisplayName</span></span>|<span data-ttu-id="99d73-126">xs:string</span><span class="sxs-lookup"><span data-stu-id="99d73-126">xs:string</span></span>|<span data-ttu-id="99d73-127">错误活动的显示名称。</span><span class="sxs-lookup"><span data-stu-id="99d73-127">The display name of the fault activity.</span></span>|  
|<span data-ttu-id="99d73-128">FaultActivityInstanceId</span><span class="sxs-lookup"><span data-stu-id="99d73-128">FaultActivityInstanceId</span></span>|<span data-ttu-id="99d73-129">xs:string</span><span class="sxs-lookup"><span data-stu-id="99d73-129">xs:string</span></span>|<span data-ttu-id="99d73-130">错误活动的实例 ID。</span><span class="sxs-lookup"><span data-stu-id="99d73-130">The instance id of the fault activity.</span></span>|  
|<span data-ttu-id="99d73-131">ExceptionActivity</span><span class="sxs-lookup"><span data-stu-id="99d73-131">ExceptionActivity</span></span>|<span data-ttu-id="99d73-132">xs:string</span><span class="sxs-lookup"><span data-stu-id="99d73-132">xs:string</span></span>|<span data-ttu-id="99d73-133">引发了异常的活动的类型名称。</span><span class="sxs-lookup"><span data-stu-id="99d73-133">The type name of the activity that threw the exception.</span></span>|  
|<span data-ttu-id="99d73-134">ExceptionActivityDisplayName</span><span class="sxs-lookup"><span data-stu-id="99d73-134">ExceptionActivityDisplayName</span></span>|<span data-ttu-id="99d73-135">xs:string</span><span class="sxs-lookup"><span data-stu-id="99d73-135">xs:string</span></span>|<span data-ttu-id="99d73-136">引发了异常的活动的显示名称。</span><span class="sxs-lookup"><span data-stu-id="99d73-136">The display name of the activity that threw the exception.</span></span>|  
|<span data-ttu-id="99d73-137">ExceptionActivityInstanceId</span><span class="sxs-lookup"><span data-stu-id="99d73-137">ExceptionActivityInstanceId</span></span>|<span data-ttu-id="99d73-138">xs:string</span><span class="sxs-lookup"><span data-stu-id="99d73-138">xs:string</span></span>|<span data-ttu-id="99d73-139">引发了异常的活动的实例 ID。</span><span class="sxs-lookup"><span data-stu-id="99d73-139">The instance id of the activity that threw the exception.</span></span>|  
|<span data-ttu-id="99d73-140">异常</span><span class="sxs-lookup"><span data-stu-id="99d73-140">Exception</span></span>|<span data-ttu-id="99d73-141">xs:string</span><span class="sxs-lookup"><span data-stu-id="99d73-141">xs:string</span></span>|<span data-ttu-id="99d73-142">异常的异常详细信息</span><span class="sxs-lookup"><span data-stu-id="99d73-142">The exception details for the exception</span></span>|  
|<span data-ttu-id="99d73-143">应用程序域</span><span class="sxs-lookup"><span data-stu-id="99d73-143">AppDomain</span></span>|<span data-ttu-id="99d73-144">xs:string</span><span class="sxs-lookup"><span data-stu-id="99d73-144">xs:string</span></span>|<span data-ttu-id="99d73-145">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="99d73-145">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
