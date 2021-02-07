---
description: 了解详细信息： 1026-ScheduleTransactionContextWorkItem
title: 1026 - ScheduleTransactionContextWorkItem
ms.date: 03/30/2017
ms.assetid: 0d5f86ba-ec21-4129-a726-5432e425384c
ms.openlocfilehash: 913af6903d38cea8f5c8d3e6e72dff04ff706195
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99755481"
---
# <a name="1026---scheduletransactioncontextworkitem"></a><span data-ttu-id="cb1aa-103">1026 - ScheduleTransactionContextWorkItem</span><span class="sxs-lookup"><span data-stu-id="cb1aa-103">1026 - ScheduleTransactionContextWorkItem</span></span>

## <a name="properties"></a><span data-ttu-id="cb1aa-104">属性</span><span class="sxs-lookup"><span data-stu-id="cb1aa-104">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="cb1aa-105">ID</span><span class="sxs-lookup"><span data-stu-id="cb1aa-105">ID</span></span>|<span data-ttu-id="cb1aa-106">1026</span><span class="sxs-lookup"><span data-stu-id="cb1aa-106">1026</span></span>|  
|<span data-ttu-id="cb1aa-107">关键字</span><span class="sxs-lookup"><span data-stu-id="cb1aa-107">Keywords</span></span>|<span data-ttu-id="cb1aa-108">WFRuntime</span><span class="sxs-lookup"><span data-stu-id="cb1aa-108">WFRuntime</span></span>|  
|<span data-ttu-id="cb1aa-109">级别</span><span class="sxs-lookup"><span data-stu-id="cb1aa-109">Level</span></span>|<span data-ttu-id="cb1aa-110">“详细”</span><span class="sxs-lookup"><span data-stu-id="cb1aa-110">Verbose</span></span>|  
|<span data-ttu-id="cb1aa-111">通道</span><span class="sxs-lookup"><span data-stu-id="cb1aa-111">Channel</span></span>|<span data-ttu-id="cb1aa-112">Microsoft-Windows-应用程序服务器-应用程序/调试</span><span class="sxs-lookup"><span data-stu-id="cb1aa-112">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="cb1aa-113">说明</span><span class="sxs-lookup"><span data-stu-id="cb1aa-113">Description</span></span>  

 <span data-ttu-id="cb1aa-114">指示已安排 TransactionContextWorkItem。</span><span class="sxs-lookup"><span data-stu-id="cb1aa-114">Indicates a TransactionContextWorkItem has been scheduled.</span></span>  
  
## <a name="message"></a><span data-ttu-id="cb1aa-115">消息</span><span class="sxs-lookup"><span data-stu-id="cb1aa-115">Message</span></span>  

 <span data-ttu-id="cb1aa-116">已为 Activity“%1”、DisplayName“%2”、InstanceId“%3”安排了 TransactionContextWorkItem。</span><span class="sxs-lookup"><span data-stu-id="cb1aa-116">A TransactionContextWorkItem has been scheduled for Activity '%1', DisplayName: '%2', InstanceId: '%3'.</span></span>  
  
## <a name="details"></a><span data-ttu-id="cb1aa-117">详细信息</span><span class="sxs-lookup"><span data-stu-id="cb1aa-117">Details</span></span>  
  
|<span data-ttu-id="cb1aa-118">数据项名称</span><span class="sxs-lookup"><span data-stu-id="cb1aa-118">Data Item Name</span></span>|<span data-ttu-id="cb1aa-119">数据项类型</span><span class="sxs-lookup"><span data-stu-id="cb1aa-119">Data Item Type</span></span>|<span data-ttu-id="cb1aa-120">说明</span><span class="sxs-lookup"><span data-stu-id="cb1aa-120">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="cb1aa-121">活动</span><span class="sxs-lookup"><span data-stu-id="cb1aa-121">Activity</span></span>|<span data-ttu-id="cb1aa-122">xs:string</span><span class="sxs-lookup"><span data-stu-id="cb1aa-122">xs:string</span></span>|<span data-ttu-id="cb1aa-123">活动的类型名称。</span><span class="sxs-lookup"><span data-stu-id="cb1aa-123">The type name of the activity.</span></span>|  
|<span data-ttu-id="cb1aa-124">DisplayName</span><span class="sxs-lookup"><span data-stu-id="cb1aa-124">DisplayName</span></span>|<span data-ttu-id="cb1aa-125">xs:string</span><span class="sxs-lookup"><span data-stu-id="cb1aa-125">xs:string</span></span>|<span data-ttu-id="cb1aa-126">活动的显示名称。</span><span class="sxs-lookup"><span data-stu-id="cb1aa-126">The display name of the activity.</span></span>|  
|<span data-ttu-id="cb1aa-127">InstanceId</span><span class="sxs-lookup"><span data-stu-id="cb1aa-127">InstanceId</span></span>|<span data-ttu-id="cb1aa-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="cb1aa-128">xs:string</span></span>|<span data-ttu-id="cb1aa-129">活动的实例 ID。</span><span class="sxs-lookup"><span data-stu-id="cb1aa-129">The instance id of the activity.</span></span>|  
|<span data-ttu-id="cb1aa-130">应用程序域</span><span class="sxs-lookup"><span data-stu-id="cb1aa-130">AppDomain</span></span>|<span data-ttu-id="cb1aa-131">xs:string</span><span class="sxs-lookup"><span data-stu-id="cb1aa-131">xs:string</span></span>|<span data-ttu-id="cb1aa-132">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="cb1aa-132">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
