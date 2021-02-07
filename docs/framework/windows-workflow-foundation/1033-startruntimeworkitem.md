---
description: 了解详细信息： 1033-StartRuntimeWorkItem
title: 1033 - StartRuntimeWorkItem
ms.date: 03/30/2017
ms.assetid: 172b5346-9f3b-46ae-bc06-39872022376a
ms.openlocfilehash: 31e664070b7592d3350a2f6f84f0493cc8f11ea1
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99668001"
---
# <a name="1033---startruntimeworkitem"></a><span data-ttu-id="d66f6-103">1033 - StartRuntimeWorkItem</span><span class="sxs-lookup"><span data-stu-id="d66f6-103">1033 - StartRuntimeWorkItem</span></span>

## <a name="properties"></a><span data-ttu-id="d66f6-104">属性</span><span class="sxs-lookup"><span data-stu-id="d66f6-104">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="d66f6-105">ID</span><span class="sxs-lookup"><span data-stu-id="d66f6-105">ID</span></span>|<span data-ttu-id="d66f6-106">2052</span><span class="sxs-lookup"><span data-stu-id="d66f6-106">1033</span></span>|  
|<span data-ttu-id="d66f6-107">关键字</span><span class="sxs-lookup"><span data-stu-id="d66f6-107">Keywords</span></span>|<span data-ttu-id="d66f6-108">WFRuntime</span><span class="sxs-lookup"><span data-stu-id="d66f6-108">WFRuntime</span></span>|  
|<span data-ttu-id="d66f6-109">级别</span><span class="sxs-lookup"><span data-stu-id="d66f6-109">Level</span></span>|<span data-ttu-id="d66f6-110">“详细”</span><span class="sxs-lookup"><span data-stu-id="d66f6-110">Verbose</span></span>|  
|<span data-ttu-id="d66f6-111">通道</span><span class="sxs-lookup"><span data-stu-id="d66f6-111">Channel</span></span>|<span data-ttu-id="d66f6-112">Microsoft-Windows-应用程序服务器-应用程序/调试</span><span class="sxs-lookup"><span data-stu-id="d66f6-112">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="d66f6-113">说明</span><span class="sxs-lookup"><span data-stu-id="d66f6-113">Description</span></span>  

 <span data-ttu-id="d66f6-114">指示 RuntimeWorkItem 正在开始执行。</span><span class="sxs-lookup"><span data-stu-id="d66f6-114">Indicates a RuntimeWorkItem is starting execution.</span></span>  
  
## <a name="message"></a><span data-ttu-id="d66f6-115">消息</span><span class="sxs-lookup"><span data-stu-id="d66f6-115">Message</span></span>  

 <span data-ttu-id="d66f6-116">开始为 Activity“%1”、DisplayName“%2”、InstanceId“%3”执行运行时工作项。</span><span class="sxs-lookup"><span data-stu-id="d66f6-116">Starting execution of a runtime work item for Activity '%1', DisplayName: '%2', InstanceId: '%3'.</span></span>  
  
## <a name="details"></a><span data-ttu-id="d66f6-117">详细信息</span><span class="sxs-lookup"><span data-stu-id="d66f6-117">Details</span></span>  
  
|<span data-ttu-id="d66f6-118">数据项名称</span><span class="sxs-lookup"><span data-stu-id="d66f6-118">Data Item Name</span></span>|<span data-ttu-id="d66f6-119">数据项类型</span><span class="sxs-lookup"><span data-stu-id="d66f6-119">Data Item Type</span></span>|<span data-ttu-id="d66f6-120">说明</span><span class="sxs-lookup"><span data-stu-id="d66f6-120">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="d66f6-121">活动</span><span class="sxs-lookup"><span data-stu-id="d66f6-121">Activity</span></span>|<span data-ttu-id="d66f6-122">xs:string</span><span class="sxs-lookup"><span data-stu-id="d66f6-122">xs:string</span></span>|<span data-ttu-id="d66f6-123">活动的类型名称。</span><span class="sxs-lookup"><span data-stu-id="d66f6-123">The type name of the activity.</span></span>|  
|<span data-ttu-id="d66f6-124">DisplayName</span><span class="sxs-lookup"><span data-stu-id="d66f6-124">DisplayName</span></span>|<span data-ttu-id="d66f6-125">xs:string</span><span class="sxs-lookup"><span data-stu-id="d66f6-125">xs:string</span></span>|<span data-ttu-id="d66f6-126">活动的显示名称。</span><span class="sxs-lookup"><span data-stu-id="d66f6-126">The display name of the activity.</span></span>|  
|<span data-ttu-id="d66f6-127">InstanceId</span><span class="sxs-lookup"><span data-stu-id="d66f6-127">InstanceId</span></span>|<span data-ttu-id="d66f6-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="d66f6-128">xs:string</span></span>|<span data-ttu-id="d66f6-129">活动的实例 ID。</span><span class="sxs-lookup"><span data-stu-id="d66f6-129">The instance id of the activity.</span></span>|  
|<span data-ttu-id="d66f6-130">应用程序域</span><span class="sxs-lookup"><span data-stu-id="d66f6-130">AppDomain</span></span>|<span data-ttu-id="d66f6-131">xs:string</span><span class="sxs-lookup"><span data-stu-id="d66f6-131">xs:string</span></span>|<span data-ttu-id="d66f6-132">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="d66f6-132">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
