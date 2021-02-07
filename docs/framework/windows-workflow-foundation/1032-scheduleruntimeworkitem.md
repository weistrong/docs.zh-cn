---
description: 了解详细信息： 1032-ScheduleRuntimeWorkItem
title: 1032 - ScheduleRuntimeWorkItem
ms.date: 03/30/2017
ms.assetid: 54688101-becf-42f3-80ca-f53a7b527620
ms.openlocfilehash: d96226b4ab0f856218d292c9c2481bca6c463c8a
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99668040"
---
# <a name="1032---scheduleruntimeworkitem"></a><span data-ttu-id="5f398-103">1032 - ScheduleRuntimeWorkItem</span><span class="sxs-lookup"><span data-stu-id="5f398-103">1032 - ScheduleRuntimeWorkItem</span></span>

## <a name="properties"></a><span data-ttu-id="5f398-104">属性</span><span class="sxs-lookup"><span data-stu-id="5f398-104">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="5f398-105">ID</span><span class="sxs-lookup"><span data-stu-id="5f398-105">ID</span></span>|<span data-ttu-id="5f398-106">1032</span><span class="sxs-lookup"><span data-stu-id="5f398-106">1032</span></span>|  
|<span data-ttu-id="5f398-107">关键字</span><span class="sxs-lookup"><span data-stu-id="5f398-107">Keywords</span></span>|<span data-ttu-id="5f398-108">WFRuntime</span><span class="sxs-lookup"><span data-stu-id="5f398-108">WFRuntime</span></span>|  
|<span data-ttu-id="5f398-109">级别</span><span class="sxs-lookup"><span data-stu-id="5f398-109">Level</span></span>|<span data-ttu-id="5f398-110">“详细”</span><span class="sxs-lookup"><span data-stu-id="5f398-110">Verbose</span></span>|  
|<span data-ttu-id="5f398-111">通道</span><span class="sxs-lookup"><span data-stu-id="5f398-111">Channel</span></span>|<span data-ttu-id="5f398-112">Microsoft-Windows-应用程序服务器-应用程序/调试</span><span class="sxs-lookup"><span data-stu-id="5f398-112">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="5f398-113">说明</span><span class="sxs-lookup"><span data-stu-id="5f398-113">Description</span></span>  

 <span data-ttu-id="5f398-114">指示已安排 RuntimeWorkItem。</span><span class="sxs-lookup"><span data-stu-id="5f398-114">Indicates a RuntimeWorkItem has been scheduled.</span></span>  
  
## <a name="message"></a><span data-ttu-id="5f398-115">消息</span><span class="sxs-lookup"><span data-stu-id="5f398-115">Message</span></span>  

 <span data-ttu-id="5f398-116">已为 Activity“%1”、DisplayName“%2”、InstanceId“%3”安排了运行时工作项。</span><span class="sxs-lookup"><span data-stu-id="5f398-116">A runtime work item has been scheduled for Activity '%1', DisplayName: '%2', InstanceId: '%3'.</span></span>  
  
## <a name="details"></a><span data-ttu-id="5f398-117">详细信息</span><span class="sxs-lookup"><span data-stu-id="5f398-117">Details</span></span>  
  
|<span data-ttu-id="5f398-118">数据项名称</span><span class="sxs-lookup"><span data-stu-id="5f398-118">Data Item Name</span></span>|<span data-ttu-id="5f398-119">数据项类型</span><span class="sxs-lookup"><span data-stu-id="5f398-119">Data Item Type</span></span>|<span data-ttu-id="5f398-120">说明</span><span class="sxs-lookup"><span data-stu-id="5f398-120">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="5f398-121">活动</span><span class="sxs-lookup"><span data-stu-id="5f398-121">Activity</span></span>|<span data-ttu-id="5f398-122">xs:string</span><span class="sxs-lookup"><span data-stu-id="5f398-122">xs:string</span></span>|<span data-ttu-id="5f398-123">活动的类型名称。</span><span class="sxs-lookup"><span data-stu-id="5f398-123">The type name of the activity.</span></span>|  
|<span data-ttu-id="5f398-124">DisplayName</span><span class="sxs-lookup"><span data-stu-id="5f398-124">DisplayName</span></span>|<span data-ttu-id="5f398-125">xs:string</span><span class="sxs-lookup"><span data-stu-id="5f398-125">xs:string</span></span>|<span data-ttu-id="5f398-126">活动的显示名称。</span><span class="sxs-lookup"><span data-stu-id="5f398-126">The display name of the activity.</span></span>|  
|<span data-ttu-id="5f398-127">InstanceId</span><span class="sxs-lookup"><span data-stu-id="5f398-127">InstanceId</span></span>|<span data-ttu-id="5f398-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="5f398-128">xs:string</span></span>|<span data-ttu-id="5f398-129">活动的实例 ID。</span><span class="sxs-lookup"><span data-stu-id="5f398-129">The instance id of the activity.</span></span>|  
|<span data-ttu-id="5f398-130">应用程序域</span><span class="sxs-lookup"><span data-stu-id="5f398-130">AppDomain</span></span>|<span data-ttu-id="5f398-131">xs:string</span><span class="sxs-lookup"><span data-stu-id="5f398-131">xs:string</span></span>|<span data-ttu-id="5f398-132">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="5f398-132">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
