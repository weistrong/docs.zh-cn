---
description: 了解详细信息： 1150-CompensationState
title: 1150 - CompensationState
ms.date: 03/30/2017
ms.assetid: eb015842-cc5a-47be-bce5-6af39e567723
ms.openlocfilehash: 4adc246cbe46dee3594bc6c0330c8e0306489219
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99703336"
---
# <a name="1150---compensationstate"></a><span data-ttu-id="a2205-103">1150 - CompensationState</span><span class="sxs-lookup"><span data-stu-id="a2205-103">1150 - CompensationState</span></span>

## <a name="properties"></a><span data-ttu-id="a2205-104">属性</span><span class="sxs-lookup"><span data-stu-id="a2205-104">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="a2205-105">ID</span><span class="sxs-lookup"><span data-stu-id="a2205-105">ID</span></span>|<span data-ttu-id="a2205-106">1150</span><span class="sxs-lookup"><span data-stu-id="a2205-106">1150</span></span>|  
|<span data-ttu-id="a2205-107">关键字</span><span class="sxs-lookup"><span data-stu-id="a2205-107">Keywords</span></span>|<span data-ttu-id="a2205-108">WFActivities</span><span class="sxs-lookup"><span data-stu-id="a2205-108">WFActivities</span></span>|  
|<span data-ttu-id="a2205-109">级别</span><span class="sxs-lookup"><span data-stu-id="a2205-109">Level</span></span>|<span data-ttu-id="a2205-110">信息</span><span class="sxs-lookup"><span data-stu-id="a2205-110">Information</span></span>|  
|<span data-ttu-id="a2205-111">通道</span><span class="sxs-lookup"><span data-stu-id="a2205-111">Channel</span></span>|<span data-ttu-id="a2205-112">Microsoft-Windows-应用程序服务器-应用程序/调试</span><span class="sxs-lookup"><span data-stu-id="a2205-112">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="a2205-113">说明</span><span class="sxs-lookup"><span data-stu-id="a2205-113">Description</span></span>  

 <span data-ttu-id="a2205-114">指示状态在 CompensableActivity 中发生更改。</span><span class="sxs-lookup"><span data-stu-id="a2205-114">Indicates a change of state in a CompensableActivity.</span></span>  
  
## <a name="message"></a><span data-ttu-id="a2205-115">消息</span><span class="sxs-lookup"><span data-stu-id="a2205-115">Message</span></span>  

 <span data-ttu-id="a2205-116">CompensableActivity“%1”的状态为“%2”。</span><span class="sxs-lookup"><span data-stu-id="a2205-116">CompensableActivity '%1' is in the '%2' state.</span></span>  
  
## <a name="details"></a><span data-ttu-id="a2205-117">详细信息</span><span class="sxs-lookup"><span data-stu-id="a2205-117">Details</span></span>  
  
|<span data-ttu-id="a2205-118">数据项名称</span><span class="sxs-lookup"><span data-stu-id="a2205-118">Data Item Name</span></span>|<span data-ttu-id="a2205-119">数据项类型</span><span class="sxs-lookup"><span data-stu-id="a2205-119">Data Item Type</span></span>|<span data-ttu-id="a2205-120">说明</span><span class="sxs-lookup"><span data-stu-id="a2205-120">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="a2205-121">DisplayName</span><span class="sxs-lookup"><span data-stu-id="a2205-121">DisplayName</span></span>|<span data-ttu-id="a2205-122">xs:string</span><span class="sxs-lookup"><span data-stu-id="a2205-122">xs:string</span></span>|<span data-ttu-id="a2205-123">活动的显示名称。</span><span class="sxs-lookup"><span data-stu-id="a2205-123">The display name of the activity.</span></span>|  
|<span data-ttu-id="a2205-124">状态</span><span class="sxs-lookup"><span data-stu-id="a2205-124">State</span></span>|<span data-ttu-id="a2205-125">xs:string</span><span class="sxs-lookup"><span data-stu-id="a2205-125">xs:string</span></span>|<span data-ttu-id="a2205-126">补偿状态。</span><span class="sxs-lookup"><span data-stu-id="a2205-126">The compensation state.</span></span>|  
|<span data-ttu-id="a2205-127">应用程序域</span><span class="sxs-lookup"><span data-stu-id="a2205-127">AppDomain</span></span>|<span data-ttu-id="a2205-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="a2205-128">xs:string</span></span>|<span data-ttu-id="a2205-129">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="a2205-129">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
