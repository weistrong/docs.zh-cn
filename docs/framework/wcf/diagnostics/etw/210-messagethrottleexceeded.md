---
description: 了解详细信息： 210-MessageThrottleExceeded
title: 210 - MessageThrottleExceeded
ms.date: 03/30/2017
ms.assetid: 24ca08ea-c11c-4753-946e-98aa820f8711
ms.openlocfilehash: e02a115995fa0e18a2ed4582710881d30bb4b846
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99794437"
---
# <a name="210---messagethrottleexceeded"></a><span data-ttu-id="e8762-103">210 - MessageThrottleExceeded</span><span class="sxs-lookup"><span data-stu-id="e8762-103">210 - MessageThrottleExceeded</span></span>

## <a name="properties"></a><span data-ttu-id="e8762-104">属性</span><span class="sxs-lookup"><span data-stu-id="e8762-104">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="e8762-105">ID</span><span class="sxs-lookup"><span data-stu-id="e8762-105">ID</span></span>|<span data-ttu-id="e8762-106">210</span><span class="sxs-lookup"><span data-stu-id="e8762-106">210</span></span>|  
|<span data-ttu-id="e8762-107">关键字</span><span class="sxs-lookup"><span data-stu-id="e8762-107">Keywords</span></span>|<span data-ttu-id="e8762-108">EndToEndMonitoring、HealthMonitoring、疑难解答、ServiceModel</span><span class="sxs-lookup"><span data-stu-id="e8762-108">EndToEndMonitoring, HealthMonitoring, Troubleshooting, ServiceModel</span></span>|  
|<span data-ttu-id="e8762-109">级别</span><span class="sxs-lookup"><span data-stu-id="e8762-109">Level</span></span>|<span data-ttu-id="e8762-110">警告</span><span class="sxs-lookup"><span data-stu-id="e8762-110">Warning</span></span>|  
|<span data-ttu-id="e8762-111">通道</span><span class="sxs-lookup"><span data-stu-id="e8762-111">Channel</span></span>|<span data-ttu-id="e8762-112">Microsoft-Windows-应用程序服务器-应用程序/分析</span><span class="sxs-lookup"><span data-stu-id="e8762-112">Microsoft-Windows-Application Server-Applications/Analytic</span></span>|  
  
## <a name="description"></a><span data-ttu-id="e8762-113">说明</span><span class="sxs-lookup"><span data-stu-id="e8762-113">Description</span></span>  

 <span data-ttu-id="e8762-114">在超过三个主服务控制器中止值之一时，将发出此事件。</span><span class="sxs-lookup"><span data-stu-id="e8762-114">This event is emitted when one of the three main service throttles have been exceeded.</span></span> <span data-ttu-id="e8762-115">请注意，仅在首次超过中止值时才发出此事件。</span><span class="sxs-lookup"><span data-stu-id="e8762-115">Note that this event is only emitted when the throttle limit is initially exceeded.</span></span> <span data-ttu-id="e8762-116">例如，如果并发调用的中止值为 10，则第 11 个并发调用将导致 `MessageThrottleExceeded` 事件。</span><span class="sxs-lookup"><span data-stu-id="e8762-116">For example, if the throttle limit for concurrent calls is 10, the 11th concurrent call results in a `MessageThrottleExceeded` event.</span></span> <span data-ttu-id="e8762-117">第 12 个调用不会再次导致事件。</span><span class="sxs-lookup"><span data-stu-id="e8762-117">The 12th call does not result in another event.</span></span> <span data-ttu-id="e8762-118">此外，为避免噪声事件流，在中止值附近波动的活动不会导致其他事件。</span><span class="sxs-lookup"><span data-stu-id="e8762-118">Additionally, to avoid a noisy event stream, activity that hovers around the limit does not result in another event.</span></span> <span data-ttu-id="e8762-119">在本示例中，如果有 2 个调用完成，则还存在 9 个并发调用。</span><span class="sxs-lookup"><span data-stu-id="e8762-119">In this example, if a couple of calls complete then there are 9 concurrent calls.</span></span> <span data-ttu-id="e8762-120">如果随后再发出了 2 个调用，则当前值再次达到 11。</span><span class="sxs-lookup"><span data-stu-id="e8762-120">If subsequently two more calls come in, the current value is again 11.</span></span> <span data-ttu-id="e8762-121">不过，这不会再次引发事件。</span><span class="sxs-lookup"><span data-stu-id="e8762-121">This does not result in another event.</span></span> <span data-ttu-id="e8762-122">当前值下降到中止值的 70% 时，将发出一个不同的事件以指示活动已减少。</span><span class="sxs-lookup"><span data-stu-id="e8762-122">When the current value falls to 70 percent of the throttle limit a different event is emitted that indicates that the activity has slowed.</span></span> <span data-ttu-id="e8762-123">以后超出中止值的活动将导致发出另一个 `MessageThrottleExceeded` 事件。</span><span class="sxs-lookup"><span data-stu-id="e8762-123">Future activity that exceeds the limit results in another `MessageThrottleExceeded` event being emitted.</span></span> <span data-ttu-id="e8762-124">在本示例中，如果并发调用数下降到 7，然后再次达到 11，则发出另一个 `MessageThrottleExceeded` 事件。</span><span class="sxs-lookup"><span data-stu-id="e8762-124">In this example, if the amount of concurrent calls falls to 7 and then again reaches 11 and another `MessageThrottleExceeded` event is emitted.</span></span>  
  
## <a name="message"></a><span data-ttu-id="e8762-125">消息</span><span class="sxs-lookup"><span data-stu-id="e8762-125">Message</span></span>  

 <span data-ttu-id="e8762-126">达到了“%2”的中止值“%1”。</span><span class="sxs-lookup"><span data-stu-id="e8762-126">The '%1' throttle limit of '%2' was hit.</span></span>  
  
## <a name="details"></a><span data-ttu-id="e8762-127">详细信息</span><span class="sxs-lookup"><span data-stu-id="e8762-127">Details</span></span>  
  
|<span data-ttu-id="e8762-128">数据项名称</span><span class="sxs-lookup"><span data-stu-id="e8762-128">Data Item Name</span></span>|<span data-ttu-id="e8762-129">数据项类型</span><span class="sxs-lookup"><span data-stu-id="e8762-129">Data Item Type</span></span>|<span data-ttu-id="e8762-130">说明</span><span class="sxs-lookup"><span data-stu-id="e8762-130">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="e8762-131">中止值名称</span><span class="sxs-lookup"><span data-stu-id="e8762-131">Throttle Name</span></span>|`xs:string`|<span data-ttu-id="e8762-132">超过的中止值的名称。</span><span class="sxs-lookup"><span data-stu-id="e8762-132">The name of the throttle that has been exceeded.</span></span> <span data-ttu-id="e8762-133">`MaxConcurrentCalls`、`MaxConcurrentInstances` 或 `MaxConcurrentSessions`。</span><span class="sxs-lookup"><span data-stu-id="e8762-133">Either `MaxConcurrentCalls`, `MaxConcurrentInstances`, or `MaxConcurrentSessions`,</span></span>|  
|<span data-ttu-id="e8762-134">限制</span><span class="sxs-lookup"><span data-stu-id="e8762-134">Limit</span></span>|`xs:long`|<span data-ttu-id="e8762-135">当前配置的中止值限制。</span><span class="sxs-lookup"><span data-stu-id="e8762-135">The currently configured limit of the throttle.</span></span>|  
|<span data-ttu-id="e8762-136">HostReference</span><span class="sxs-lookup"><span data-stu-id="e8762-136">HostReference</span></span>|`xs:string`|<span data-ttu-id="e8762-137">对于 Web 承载的服务，此字段唯一标识 Web 层次结构中的服务。</span><span class="sxs-lookup"><span data-stu-id="e8762-137">For Web-hosted services, this field uniquely identifies the service in the Web hierarchy.</span></span> <span data-ttu-id="e8762-138">其格式定义为 "网站名称应用程序虚拟路径&#124;服务虚拟路径&#124;ServiceName"。</span><span class="sxs-lookup"><span data-stu-id="e8762-138">Its format is defined as 'Web Site Name Application Virtual Path&#124;Service Virtual Path&#124;ServiceName'.</span></span> <span data-ttu-id="e8762-139">示例： "Default Web Site//Calculatorapplication&#124;/CalculatorService.svc&#124;CalculatorService"。</span><span class="sxs-lookup"><span data-stu-id="e8762-139">Example: 'Default Web Site/CalculatorApplication&#124;/CalculatorService.svc&#124;CalculatorService'.</span></span>|  
|<span data-ttu-id="e8762-140">应用程序域</span><span class="sxs-lookup"><span data-stu-id="e8762-140">AppDomain</span></span>|`xs:string`|<span data-ttu-id="e8762-141">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="e8762-141">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
