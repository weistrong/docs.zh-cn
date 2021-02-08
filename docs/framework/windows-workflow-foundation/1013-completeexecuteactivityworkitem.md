---
description: 了解详细信息： 1013-CompleteExecuteActivityWorkItem
title: 1013 - CompleteExecuteActivityWorkItem
ms.date: 03/30/2017
ms.assetid: 31fc57b3-ef2f-48f0-a5de-b4e2c5c9ded7
ms.openlocfilehash: 815f859c40a02e8c06e44603a80ab964dc4e64bd
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99792942"
---
# <a name="1013---completeexecuteactivityworkitem"></a><span data-ttu-id="986a4-103">1013 - CompleteExecuteActivityWorkItem</span><span class="sxs-lookup"><span data-stu-id="986a4-103">1013 - CompleteExecuteActivityWorkItem</span></span>

## <a name="properties"></a><span data-ttu-id="986a4-104">属性</span><span class="sxs-lookup"><span data-stu-id="986a4-104">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="986a4-105">ID</span><span class="sxs-lookup"><span data-stu-id="986a4-105">ID</span></span>|<span data-ttu-id="986a4-106">1013</span><span class="sxs-lookup"><span data-stu-id="986a4-106">1013</span></span>|  
|<span data-ttu-id="986a4-107">关键字</span><span class="sxs-lookup"><span data-stu-id="986a4-107">Keywords</span></span>|<span data-ttu-id="986a4-108">WFRuntime</span><span class="sxs-lookup"><span data-stu-id="986a4-108">WFRuntime</span></span>|  
|<span data-ttu-id="986a4-109">级别</span><span class="sxs-lookup"><span data-stu-id="986a4-109">Level</span></span>|<span data-ttu-id="986a4-110">“详细”</span><span class="sxs-lookup"><span data-stu-id="986a4-110">Verbose</span></span>|  
|<span data-ttu-id="986a4-111">通道</span><span class="sxs-lookup"><span data-stu-id="986a4-111">Channel</span></span>|<span data-ttu-id="986a4-112">Microsoft-Windows-应用程序服务器-应用程序/调试</span><span class="sxs-lookup"><span data-stu-id="986a4-112">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="986a4-113">说明</span><span class="sxs-lookup"><span data-stu-id="986a4-113">Description</span></span>  

 <span data-ttu-id="986a4-114">指示 ExecuteActivityWorkItem 已完成</span><span class="sxs-lookup"><span data-stu-id="986a4-114">Indicates an ExecuteActivityWorkItem has completed</span></span>  
  
## <a name="message"></a><span data-ttu-id="986a4-115">消息</span><span class="sxs-lookup"><span data-stu-id="986a4-115">Message</span></span>  

 <span data-ttu-id="986a4-116">Activity“%1”、DisplayName“%2”、InstanceId“%3”的 ExecuteActivityWorkItem 已经完成。</span><span class="sxs-lookup"><span data-stu-id="986a4-116">An ExecuteActivityWorkItem has completed for Activity '%1', DisplayName: '%2', InstanceId: '%3'.</span></span>  
  
## <a name="details"></a><span data-ttu-id="986a4-117">详细信息</span><span class="sxs-lookup"><span data-stu-id="986a4-117">Details</span></span>  
  
|<span data-ttu-id="986a4-118">数据项名称</span><span class="sxs-lookup"><span data-stu-id="986a4-118">Data Item Name</span></span>|<span data-ttu-id="986a4-119">数据项类型</span><span class="sxs-lookup"><span data-stu-id="986a4-119">Data Item Type</span></span>|<span data-ttu-id="986a4-120">说明</span><span class="sxs-lookup"><span data-stu-id="986a4-120">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="986a4-121">活动</span><span class="sxs-lookup"><span data-stu-id="986a4-121">Activity</span></span>|<span data-ttu-id="986a4-122">xs:string</span><span class="sxs-lookup"><span data-stu-id="986a4-122">xs:string</span></span>|<span data-ttu-id="986a4-123">活动的类型名称。</span><span class="sxs-lookup"><span data-stu-id="986a4-123">The type name of the activity.</span></span>|  
|<span data-ttu-id="986a4-124">DisplayName</span><span class="sxs-lookup"><span data-stu-id="986a4-124">DisplayName</span></span>|<span data-ttu-id="986a4-125">xs:string</span><span class="sxs-lookup"><span data-stu-id="986a4-125">xs:string</span></span>|<span data-ttu-id="986a4-126">活动的显示名称。</span><span class="sxs-lookup"><span data-stu-id="986a4-126">The display name of the activity.</span></span>|  
|<span data-ttu-id="986a4-127">InstanceId</span><span class="sxs-lookup"><span data-stu-id="986a4-127">InstanceId</span></span>|<span data-ttu-id="986a4-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="986a4-128">xs:string</span></span>|<span data-ttu-id="986a4-129">活动的实例 ID。</span><span class="sxs-lookup"><span data-stu-id="986a4-129">The instance id of the activity.</span></span>|  
|<span data-ttu-id="986a4-130">应用程序域</span><span class="sxs-lookup"><span data-stu-id="986a4-130">AppDomain</span></span>|<span data-ttu-id="986a4-131">xs:string</span><span class="sxs-lookup"><span data-stu-id="986a4-131">xs:string</span></span>|<span data-ttu-id="986a4-132">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="986a4-132">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
