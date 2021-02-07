---
description: 了解详细信息： 1028-CompleteTransactionContextWorkItem
title: 1028 - CompleteTransactionContextWorkItem
ms.date: 03/30/2017
ms.assetid: 95423f9d-d29a-460e-bcd8-096e80af5bd0
ms.openlocfilehash: ae66072769c24ce8d44f92a88cd4232d20bde5f6
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99755455"
---
# <a name="1028---completetransactioncontextworkitem"></a><span data-ttu-id="b8c9c-103">1028 - CompleteTransactionContextWorkItem</span><span class="sxs-lookup"><span data-stu-id="b8c9c-103">1028 - CompleteTransactionContextWorkItem</span></span>

## <a name="properties"></a><span data-ttu-id="b8c9c-104">属性</span><span class="sxs-lookup"><span data-stu-id="b8c9c-104">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="b8c9c-105">ID</span><span class="sxs-lookup"><span data-stu-id="b8c9c-105">ID</span></span>|<span data-ttu-id="b8c9c-106">1028</span><span class="sxs-lookup"><span data-stu-id="b8c9c-106">1028</span></span>|  
|<span data-ttu-id="b8c9c-107">关键字</span><span class="sxs-lookup"><span data-stu-id="b8c9c-107">Keywords</span></span>|<span data-ttu-id="b8c9c-108">WFRuntime</span><span class="sxs-lookup"><span data-stu-id="b8c9c-108">WFRuntime</span></span>|  
|<span data-ttu-id="b8c9c-109">级别</span><span class="sxs-lookup"><span data-stu-id="b8c9c-109">Level</span></span>|<span data-ttu-id="b8c9c-110">“详细”</span><span class="sxs-lookup"><span data-stu-id="b8c9c-110">Verbose</span></span>|  
|<span data-ttu-id="b8c9c-111">通道</span><span class="sxs-lookup"><span data-stu-id="b8c9c-111">Channel</span></span>|<span data-ttu-id="b8c9c-112">Microsoft-Windows-应用程序服务器-应用程序/调试</span><span class="sxs-lookup"><span data-stu-id="b8c9c-112">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="b8c9c-113">说明</span><span class="sxs-lookup"><span data-stu-id="b8c9c-113">Description</span></span>  

 <span data-ttu-id="b8c9c-114">指示 TransactionContextWorkItem 已完成。</span><span class="sxs-lookup"><span data-stu-id="b8c9c-114">Indicates a TransactionContextWorkItem has completed.</span></span>  
  
## <a name="message"></a><span data-ttu-id="b8c9c-115">消息</span><span class="sxs-lookup"><span data-stu-id="b8c9c-115">Message</span></span>  

 <span data-ttu-id="b8c9c-116">Activity“%1”、DisplayName“%2”、InstanceId“%3”的 TransactionContextWorkItem 已经完成。</span><span class="sxs-lookup"><span data-stu-id="b8c9c-116">A TransactionContextWorkItem has completed for Activity '%1', DisplayName: '%2', InstanceId: '%3'.</span></span>  
  
## <a name="details"></a><span data-ttu-id="b8c9c-117">详细信息</span><span class="sxs-lookup"><span data-stu-id="b8c9c-117">Details</span></span>  
  
|<span data-ttu-id="b8c9c-118">数据项名称</span><span class="sxs-lookup"><span data-stu-id="b8c9c-118">Data Item Name</span></span>|<span data-ttu-id="b8c9c-119">数据项类型</span><span class="sxs-lookup"><span data-stu-id="b8c9c-119">Data Item Type</span></span>|<span data-ttu-id="b8c9c-120">说明</span><span class="sxs-lookup"><span data-stu-id="b8c9c-120">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="b8c9c-121">活动</span><span class="sxs-lookup"><span data-stu-id="b8c9c-121">Activity</span></span>|<span data-ttu-id="b8c9c-122">xs:string</span><span class="sxs-lookup"><span data-stu-id="b8c9c-122">xs:string</span></span>|<span data-ttu-id="b8c9c-123">活动的类型名称。</span><span class="sxs-lookup"><span data-stu-id="b8c9c-123">The type name of the activity.</span></span>|  
|<span data-ttu-id="b8c9c-124">DisplayName</span><span class="sxs-lookup"><span data-stu-id="b8c9c-124">DisplayName</span></span>|<span data-ttu-id="b8c9c-125">xs:string</span><span class="sxs-lookup"><span data-stu-id="b8c9c-125">xs:string</span></span>|<span data-ttu-id="b8c9c-126">活动的显示名称。</span><span class="sxs-lookup"><span data-stu-id="b8c9c-126">The display name of the activity.</span></span>|  
|<span data-ttu-id="b8c9c-127">InstanceId</span><span class="sxs-lookup"><span data-stu-id="b8c9c-127">InstanceId</span></span>|<span data-ttu-id="b8c9c-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="b8c9c-128">xs:string</span></span>|<span data-ttu-id="b8c9c-129">活动的实例 ID。</span><span class="sxs-lookup"><span data-stu-id="b8c9c-129">The instance id of the activity.</span></span>|  
|<span data-ttu-id="b8c9c-130">应用程序域</span><span class="sxs-lookup"><span data-stu-id="b8c9c-130">AppDomain</span></span>|<span data-ttu-id="b8c9c-131">xs:string</span><span class="sxs-lookup"><span data-stu-id="b8c9c-131">xs:string</span></span>|<span data-ttu-id="b8c9c-132">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="b8c9c-132">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
