---
description: 了解详细信息： 1027-StartTransactionContextWorkItem
title: 1027 - StartTransactionContextWorkItem
ms.date: 03/30/2017
ms.assetid: 116ae5ec-b9d5-4231-824e-270d00eea7b8
ms.openlocfilehash: e7f81a5998d948d3042b51dcdf20fbb1c88ad266
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99755468"
---
# <a name="1027---starttransactioncontextworkitem"></a><span data-ttu-id="e7ea7-103">1027 - StartTransactionContextWorkItem</span><span class="sxs-lookup"><span data-stu-id="e7ea7-103">1027 - StartTransactionContextWorkItem</span></span>

## <a name="properties"></a><span data-ttu-id="e7ea7-104">属性</span><span class="sxs-lookup"><span data-stu-id="e7ea7-104">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="e7ea7-105">ID</span><span class="sxs-lookup"><span data-stu-id="e7ea7-105">ID</span></span>|<span data-ttu-id="e7ea7-106">1027</span><span class="sxs-lookup"><span data-stu-id="e7ea7-106">1027</span></span>|  
|<span data-ttu-id="e7ea7-107">关键字</span><span class="sxs-lookup"><span data-stu-id="e7ea7-107">Keywords</span></span>|<span data-ttu-id="e7ea7-108">WFRuntime</span><span class="sxs-lookup"><span data-stu-id="e7ea7-108">WFRuntime</span></span>|  
|<span data-ttu-id="e7ea7-109">级别</span><span class="sxs-lookup"><span data-stu-id="e7ea7-109">Level</span></span>|<span data-ttu-id="e7ea7-110">“详细”</span><span class="sxs-lookup"><span data-stu-id="e7ea7-110">Verbose</span></span>|  
|<span data-ttu-id="e7ea7-111">通道</span><span class="sxs-lookup"><span data-stu-id="e7ea7-111">Channel</span></span>|<span data-ttu-id="e7ea7-112">Microsoft-Windows-应用程序服务器-应用程序/调试</span><span class="sxs-lookup"><span data-stu-id="e7ea7-112">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="e7ea7-113">说明</span><span class="sxs-lookup"><span data-stu-id="e7ea7-113">Description</span></span>  

 <span data-ttu-id="e7ea7-114">指示 TransactionContextWorkItem 正在开始执行。</span><span class="sxs-lookup"><span data-stu-id="e7ea7-114">Indicates a TransactionContextWorkItem is starting execution.</span></span>  
  
## <a name="message"></a><span data-ttu-id="e7ea7-115">消息</span><span class="sxs-lookup"><span data-stu-id="e7ea7-115">Message</span></span>  

 <span data-ttu-id="e7ea7-116">开始为 Activity“%1”、DisplayName“%2”、InstanceId“%3”执行 TransactionContextWorkItem。</span><span class="sxs-lookup"><span data-stu-id="e7ea7-116">Starting execution of a TransactionContextWorkItem for Activity '%1', DisplayName: '%2', InstanceId: '%3'.</span></span>  
  
## <a name="details"></a><span data-ttu-id="e7ea7-117">详细信息</span><span class="sxs-lookup"><span data-stu-id="e7ea7-117">Details</span></span>  
  
|<span data-ttu-id="e7ea7-118">数据项名称</span><span class="sxs-lookup"><span data-stu-id="e7ea7-118">Data Item Name</span></span>|<span data-ttu-id="e7ea7-119">数据项类型</span><span class="sxs-lookup"><span data-stu-id="e7ea7-119">Data Item Type</span></span>|<span data-ttu-id="e7ea7-120">说明</span><span class="sxs-lookup"><span data-stu-id="e7ea7-120">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="e7ea7-121">活动</span><span class="sxs-lookup"><span data-stu-id="e7ea7-121">Activity</span></span>|<span data-ttu-id="e7ea7-122">xs:string</span><span class="sxs-lookup"><span data-stu-id="e7ea7-122">xs:string</span></span>|<span data-ttu-id="e7ea7-123">活动的类型名称。</span><span class="sxs-lookup"><span data-stu-id="e7ea7-123">The type name of the activity.</span></span>|  
|<span data-ttu-id="e7ea7-124">DisplayName</span><span class="sxs-lookup"><span data-stu-id="e7ea7-124">DisplayName</span></span>|<span data-ttu-id="e7ea7-125">xs:string</span><span class="sxs-lookup"><span data-stu-id="e7ea7-125">xs:string</span></span>|<span data-ttu-id="e7ea7-126">活动的显示名称。</span><span class="sxs-lookup"><span data-stu-id="e7ea7-126">The display name of the activity.</span></span>|  
|<span data-ttu-id="e7ea7-127">InstanceId</span><span class="sxs-lookup"><span data-stu-id="e7ea7-127">InstanceId</span></span>|<span data-ttu-id="e7ea7-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="e7ea7-128">xs:string</span></span>|<span data-ttu-id="e7ea7-129">活动的实例 ID。</span><span class="sxs-lookup"><span data-stu-id="e7ea7-129">The instance id of the activity.</span></span>|  
|<span data-ttu-id="e7ea7-130">应用程序域</span><span class="sxs-lookup"><span data-stu-id="e7ea7-130">AppDomain</span></span>|<span data-ttu-id="e7ea7-131">xs:string</span><span class="sxs-lookup"><span data-stu-id="e7ea7-131">xs:string</span></span>|<span data-ttu-id="e7ea7-132">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="e7ea7-132">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
