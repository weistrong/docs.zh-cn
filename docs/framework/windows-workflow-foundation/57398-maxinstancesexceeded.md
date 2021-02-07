---
description: 了解详细信息： 57398-MaxInstancesExceeded
title: 57398 - MaxInstancesExceeded
ms.date: 03/30/2017
ms.assetid: f943d209-dfeb-43e5-b572-c9a06217936e
ms.openlocfilehash: 104c466cb2e0ee8156e2b268caf5e757353dfb09
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99720223"
---
# <a name="57398---maxinstancesexceeded"></a><span data-ttu-id="31921-103">57398 - MaxInstancesExceeded</span><span class="sxs-lookup"><span data-stu-id="31921-103">57398 - MaxInstancesExceeded</span></span>

## <a name="properties"></a><span data-ttu-id="31921-104">属性</span><span class="sxs-lookup"><span data-stu-id="31921-104">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="31921-105">ID</span><span class="sxs-lookup"><span data-stu-id="31921-105">ID</span></span>|<span data-ttu-id="31921-106">57398</span><span class="sxs-lookup"><span data-stu-id="31921-106">57398</span></span>|  
|<span data-ttu-id="31921-107">关键字</span><span class="sxs-lookup"><span data-stu-id="31921-107">Keywords</span></span>|<span data-ttu-id="31921-108">WFServices</span><span class="sxs-lookup"><span data-stu-id="31921-108">WFServices</span></span>|  
|<span data-ttu-id="31921-109">级别</span><span class="sxs-lookup"><span data-stu-id="31921-109">Level</span></span>|<span data-ttu-id="31921-110">警告</span><span class="sxs-lookup"><span data-stu-id="31921-110">Warning</span></span>|  
|<span data-ttu-id="31921-111">通道</span><span class="sxs-lookup"><span data-stu-id="31921-111">Channel</span></span>|<span data-ttu-id="31921-112">Microsoft-Windows-应用程序服务器-应用程序/分析</span><span class="sxs-lookup"><span data-stu-id="31921-112">Microsoft-Windows-Application Server-Applications/Analytic</span></span>|  
  
## <a name="description"></a><span data-ttu-id="31921-113">说明</span><span class="sxs-lookup"><span data-stu-id="31921-113">Description</span></span>  

 <span data-ttu-id="31921-114">指示系统达到为限制“MaxConcurrentInstances”设置的限制值。</span><span class="sxs-lookup"><span data-stu-id="31921-114">Indicates the system hit the limit set for throttle 'MaxConcurrentInstances'.</span></span>  
  
## <a name="message"></a><span data-ttu-id="31921-115">消息</span><span class="sxs-lookup"><span data-stu-id="31921-115">Message</span></span>  

 <span data-ttu-id="31921-116">系统达到为限制“MaxConcurrentInstances”设置的限制值。</span><span class="sxs-lookup"><span data-stu-id="31921-116">The system hit the limit set for throttle 'MaxConcurrentInstances'.</span></span> <span data-ttu-id="31921-117">此限制的限制值设置为 %1。</span><span class="sxs-lookup"><span data-stu-id="31921-117">Limit for this throttle was set to %1.</span></span> <span data-ttu-id="31921-118">可通过修改 serviceThrottle 元素中的特性“maxConcurrentInstances”或修改行为 ServiceThrottlingBehavior 的“MaxConcurrentInstances”属性来更改限制值。</span><span class="sxs-lookup"><span data-stu-id="31921-118">Throttle value can be changed by modifying attribute 'maxConcurrentInstances' in serviceThrottle element or by modifying 'MaxConcurrentInstances' property on behavior ServiceThrottlingBehavior.</span></span>  
  
## <a name="details"></a><span data-ttu-id="31921-119">详细信息</span><span class="sxs-lookup"><span data-stu-id="31921-119">Details</span></span>  
  
|<span data-ttu-id="31921-120">数据项名称</span><span class="sxs-lookup"><span data-stu-id="31921-120">Data Item Name</span></span>|<span data-ttu-id="31921-121">数据项类型</span><span class="sxs-lookup"><span data-stu-id="31921-121">Data Item Type</span></span>|<span data-ttu-id="31921-122">说明</span><span class="sxs-lookup"><span data-stu-id="31921-122">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="31921-123">名称</span><span class="sxs-lookup"><span data-stu-id="31921-123">Name</span></span>|<span data-ttu-id="31921-124">xs:string</span><span class="sxs-lookup"><span data-stu-id="31921-124">xs:string</span></span>|<span data-ttu-id="31921-125">项的名称。</span><span class="sxs-lookup"><span data-stu-id="31921-125">The name of the item.</span></span>|  
|<span data-ttu-id="31921-126">应用程序域</span><span class="sxs-lookup"><span data-stu-id="31921-126">AppDomain</span></span>|<span data-ttu-id="31921-127">xs:string</span><span class="sxs-lookup"><span data-stu-id="31921-127">xs:string</span></span>|<span data-ttu-id="31921-128">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="31921-128">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
