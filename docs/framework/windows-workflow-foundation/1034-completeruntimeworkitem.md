---
description: 了解详细信息： 1034-CompleteRuntimeWorkItem
title: 1034 - CompleteRuntimeWorkItem
ms.date: 03/30/2017
ms.assetid: 45620011-8b04-4f87-ab5a-65b24145e17d
ms.openlocfilehash: dd8a9fcb2fb692ab3b69df8f07f6a96cf48fc806
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99667962"
---
# <a name="1034---completeruntimeworkitem"></a><span data-ttu-id="4787d-103">1034 - CompleteRuntimeWorkItem</span><span class="sxs-lookup"><span data-stu-id="4787d-103">1034 - CompleteRuntimeWorkItem</span></span>

## <a name="properties"></a><span data-ttu-id="4787d-104">属性</span><span class="sxs-lookup"><span data-stu-id="4787d-104">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="4787d-105">ID</span><span class="sxs-lookup"><span data-stu-id="4787d-105">ID</span></span>|<span data-ttu-id="4787d-106">1034</span><span class="sxs-lookup"><span data-stu-id="4787d-106">1034</span></span>|  
|<span data-ttu-id="4787d-107">关键字</span><span class="sxs-lookup"><span data-stu-id="4787d-107">Keywords</span></span>|<span data-ttu-id="4787d-108">WFRuntime</span><span class="sxs-lookup"><span data-stu-id="4787d-108">WFRuntime</span></span>|  
|<span data-ttu-id="4787d-109">级别</span><span class="sxs-lookup"><span data-stu-id="4787d-109">Level</span></span>|<span data-ttu-id="4787d-110">“详细”</span><span class="sxs-lookup"><span data-stu-id="4787d-110">Verbose</span></span>|  
|<span data-ttu-id="4787d-111">通道</span><span class="sxs-lookup"><span data-stu-id="4787d-111">Channel</span></span>|<span data-ttu-id="4787d-112">Microsoft-Windows-应用程序服务器-应用程序/调试</span><span class="sxs-lookup"><span data-stu-id="4787d-112">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="4787d-113">说明</span><span class="sxs-lookup"><span data-stu-id="4787d-113">Description</span></span>  

 <span data-ttu-id="4787d-114">指示 RuntimeWorkItem 已完成。</span><span class="sxs-lookup"><span data-stu-id="4787d-114">Indicates a RuntimeWorkItem has completed.</span></span>  
  
## <a name="message"></a><span data-ttu-id="4787d-115">消息</span><span class="sxs-lookup"><span data-stu-id="4787d-115">Message</span></span>  

 <span data-ttu-id="4787d-116">Activity“%1”、DisplayName“%2”、InstanceId“%3”的运行时工作项已经完成。</span><span class="sxs-lookup"><span data-stu-id="4787d-116">A runtime work item has completed for Activity '%1', DisplayName: '%2', InstanceId: '%3'.</span></span>  
  
## <a name="details"></a><span data-ttu-id="4787d-117">详细信息</span><span class="sxs-lookup"><span data-stu-id="4787d-117">Details</span></span>  
  
|<span data-ttu-id="4787d-118">数据项名称</span><span class="sxs-lookup"><span data-stu-id="4787d-118">Data Item Name</span></span>|<span data-ttu-id="4787d-119">数据项类型</span><span class="sxs-lookup"><span data-stu-id="4787d-119">Data Item Type</span></span>|<span data-ttu-id="4787d-120">说明</span><span class="sxs-lookup"><span data-stu-id="4787d-120">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="4787d-121">活动</span><span class="sxs-lookup"><span data-stu-id="4787d-121">Activity</span></span>|<span data-ttu-id="4787d-122">xs:string</span><span class="sxs-lookup"><span data-stu-id="4787d-122">xs:string</span></span>|<span data-ttu-id="4787d-123">活动的类型名称。</span><span class="sxs-lookup"><span data-stu-id="4787d-123">The type name of the activity.</span></span>|  
|<span data-ttu-id="4787d-124">DisplayName</span><span class="sxs-lookup"><span data-stu-id="4787d-124">DisplayName</span></span>|<span data-ttu-id="4787d-125">xs:string</span><span class="sxs-lookup"><span data-stu-id="4787d-125">xs:string</span></span>|<span data-ttu-id="4787d-126">活动的显示名称。</span><span class="sxs-lookup"><span data-stu-id="4787d-126">The display name of the activity.</span></span>|  
|<span data-ttu-id="4787d-127">InstanceId</span><span class="sxs-lookup"><span data-stu-id="4787d-127">InstanceId</span></span>|<span data-ttu-id="4787d-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="4787d-128">xs:string</span></span>|<span data-ttu-id="4787d-129">活动的实例 ID。</span><span class="sxs-lookup"><span data-stu-id="4787d-129">The instance id of the activity.</span></span>|  
|<span data-ttu-id="4787d-130">应用程序域</span><span class="sxs-lookup"><span data-stu-id="4787d-130">AppDomain</span></span>|<span data-ttu-id="4787d-131">xs:string</span><span class="sxs-lookup"><span data-stu-id="4787d-131">xs:string</span></span>|<span data-ttu-id="4787d-132">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="4787d-132">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
