---
description: 了解详细信息： 224-MessageThrottleAtSeventyPercent
title: 224 - MessageThrottleAtSeventyPercent
ms.date: 03/30/2017
ms.assetid: 82bbbfd7-10d2-41fd-805d-2443b0c1b96b
ms.openlocfilehash: 14c08371c5db7e6f7deb0a5851a1d24dfc94475e
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99794268"
---
# <a name="224---messagethrottleatseventypercent"></a><span data-ttu-id="b49af-103">224 - MessageThrottleAtSeventyPercent</span><span class="sxs-lookup"><span data-stu-id="b49af-103">224 - MessageThrottleAtSeventyPercent</span></span>

## <a name="properties"></a><span data-ttu-id="b49af-104">属性</span><span class="sxs-lookup"><span data-stu-id="b49af-104">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="b49af-105">ID</span><span class="sxs-lookup"><span data-stu-id="b49af-105">ID</span></span>|<span data-ttu-id="b49af-106">224</span><span class="sxs-lookup"><span data-stu-id="b49af-106">224</span></span>|  
|<span data-ttu-id="b49af-107">关键字</span><span class="sxs-lookup"><span data-stu-id="b49af-107">Keywords</span></span>|<span data-ttu-id="b49af-108">EndToEndMonitoring、HealthMonitoring、疑难解答、ServiceModel</span><span class="sxs-lookup"><span data-stu-id="b49af-108">EndToEndMonitoring, HealthMonitoring, Troubleshooting, ServiceModel</span></span>|  
|<span data-ttu-id="b49af-109">级别</span><span class="sxs-lookup"><span data-stu-id="b49af-109">Level</span></span>|<span data-ttu-id="b49af-110">警告</span><span class="sxs-lookup"><span data-stu-id="b49af-110">Warning</span></span>|  
|<span data-ttu-id="b49af-111">通道</span><span class="sxs-lookup"><span data-stu-id="b49af-111">Channel</span></span>|<span data-ttu-id="b49af-112">Microsoft-Windows-应用程序服务器-应用程序/分析</span><span class="sxs-lookup"><span data-stu-id="b49af-112">Microsoft-Windows-Application Server-Applications/Analytic</span></span>|  
  
## <a name="description"></a><span data-ttu-id="b49af-113">说明</span><span class="sxs-lookup"><span data-stu-id="b49af-113">Description</span></span>  

 <span data-ttu-id="b49af-114">当超出某个主服务中止值时，将发出 `MessageThrottleExceeded` 事件。</span><span class="sxs-lookup"><span data-stu-id="b49af-114">When one of the main service throttles has been exceeded, the `MessageThrottleExceeded` event is emitted.</span></span> <span data-ttu-id="b49af-115">当活动峰值变慢且当前中止值达到当前限制值的 70% 时，将发出此事件。</span><span class="sxs-lookup"><span data-stu-id="b49af-115">When the spike of activity slows and the current value of the throttle is at 70 percent of the current limit then this event is emitted.</span></span> <span data-ttu-id="b49af-116">请注意，仅在活动变慢时才发出一次此事件。</span><span class="sxs-lookup"><span data-stu-id="b49af-116">Note that this event is only emitted once as the activity is slowing.</span></span> <span data-ttu-id="b49af-117">如果当前值在 70% 标记的附近波动（例如，70,69,70,71,70,69），则只有第一次出现的 70% 会导致发出事件。</span><span class="sxs-lookup"><span data-stu-id="b49af-117">If the current value hovers at the 70 percent mark, (for example, 70,69,70,71,70,69), only the first occurrence of 70 percent results in an event.</span></span> <span data-ttu-id="b49af-118">在发出此事件后，如果将来出现超出中止值的情况，则也会导致发出 `MessageThrottleExceeded` 事件。</span><span class="sxs-lookup"><span data-stu-id="b49af-118">After this event is emitted, future occurrences of exceeding the throttle's limit result in a `MessageThrottleExceeded` event.</span></span>  
  
## <a name="message"></a><span data-ttu-id="b49af-119">消息</span><span class="sxs-lookup"><span data-stu-id="b49af-119">Message</span></span>  

 <span data-ttu-id="b49af-120">“%2”的“%1”中止值为 70%%。</span><span class="sxs-lookup"><span data-stu-id="b49af-120">The '%1' throttle limit of '%2' is at 70%%.</span></span>  
  
## <a name="details"></a><span data-ttu-id="b49af-121">详细信息</span><span class="sxs-lookup"><span data-stu-id="b49af-121">Details</span></span>  
  
|<span data-ttu-id="b49af-122">数据项名称</span><span class="sxs-lookup"><span data-stu-id="b49af-122">Data Item Name</span></span>|<span data-ttu-id="b49af-123">数据项类型</span><span class="sxs-lookup"><span data-stu-id="b49af-123">Data Item Type</span></span>|<span data-ttu-id="b49af-124">说明</span><span class="sxs-lookup"><span data-stu-id="b49af-124">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="b49af-125">中止值名称</span><span class="sxs-lookup"><span data-stu-id="b49af-125">Throttle Name</span></span>|`xs:string`|<span data-ttu-id="b49af-126">超过的中止值的名称。</span><span class="sxs-lookup"><span data-stu-id="b49af-126">The name of the throttle that has been exceeded.</span></span> <span data-ttu-id="b49af-127">`MaxConcurrentCalls`、`MaxConcurrentInstances` 或 `MaxConcurrentSessions`。</span><span class="sxs-lookup"><span data-stu-id="b49af-127">Either `MaxConcurrentCalls`, `MaxConcurrentInstances`, or `MaxConcurrentSessions`,</span></span>|  
|<span data-ttu-id="b49af-128">限制</span><span class="sxs-lookup"><span data-stu-id="b49af-128">Limit</span></span>|`xs:long`|<span data-ttu-id="b49af-129">当前配置的中止值限制。</span><span class="sxs-lookup"><span data-stu-id="b49af-129">The currently configured limit of the throttle.</span></span>|  
|<span data-ttu-id="b49af-130">HostReference</span><span class="sxs-lookup"><span data-stu-id="b49af-130">HostReference</span></span>|`xs:string`|<span data-ttu-id="b49af-131">对于 Web 承载的服务，此字段唯一标识 Web 层次结构中的服务。</span><span class="sxs-lookup"><span data-stu-id="b49af-131">For Web-hosted services, this field uniquely identifies the service in the Web hierarchy.</span></span> <span data-ttu-id="b49af-132">其格式定义为 "网站名称应用程序虚拟路径&#124;服务虚拟路径&#124;ServiceName"。</span><span class="sxs-lookup"><span data-stu-id="b49af-132">Its format is defined as 'Web Site Name Application Virtual Path&#124;Service Virtual Path&#124;ServiceName'.</span></span> <span data-ttu-id="b49af-133">示例： "Default Web Site//Calculatorapplication&#124;/CalculatorService.svc&#124;CalculatorService"。</span><span class="sxs-lookup"><span data-stu-id="b49af-133">Example: 'Default Web Site/CalculatorApplication&#124;/CalculatorService.svc&#124;CalculatorService'.</span></span>|  
|<span data-ttu-id="b49af-134">应用程序域</span><span class="sxs-lookup"><span data-stu-id="b49af-134">AppDomain</span></span>|`xs:string`|<span data-ttu-id="b49af-135">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="b49af-135">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
