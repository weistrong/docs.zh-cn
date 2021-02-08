---
description: 了解详细信息： 225-TraceCorrelationKeys
title: 225 - TraceCorrelationKeys
ms.date: 03/30/2017
ms.assetid: d9083aaf-3816-4c1c-bae0-2d7f49628345
ms.openlocfilehash: c5fdb9305815cdc4df6bbae3e54209d2b5cffd9d
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99778108"
---
# <a name="225---tracecorrelationkeys"></a><span data-ttu-id="c11d3-103">225 - TraceCorrelationKeys</span><span class="sxs-lookup"><span data-stu-id="c11d3-103">225 - TraceCorrelationKeys</span></span>

## <a name="properties"></a><span data-ttu-id="c11d3-104">属性</span><span class="sxs-lookup"><span data-stu-id="c11d3-104">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="c11d3-105">ID</span><span class="sxs-lookup"><span data-stu-id="c11d3-105">ID</span></span>|<span data-ttu-id="c11d3-106">225</span><span class="sxs-lookup"><span data-stu-id="c11d3-106">225</span></span>|  
|<span data-ttu-id="c11d3-107">关键字</span><span class="sxs-lookup"><span data-stu-id="c11d3-107">Keywords</span></span>|<span data-ttu-id="c11d3-108">疑难解答，ServiceModel</span><span class="sxs-lookup"><span data-stu-id="c11d3-108">Troubleshooting, ServiceModel</span></span>|  
|<span data-ttu-id="c11d3-109">级别</span><span class="sxs-lookup"><span data-stu-id="c11d3-109">Level</span></span>|<span data-ttu-id="c11d3-110">信息</span><span class="sxs-lookup"><span data-stu-id="c11d3-110">Information</span></span>|  
|<span data-ttu-id="c11d3-111">通道</span><span class="sxs-lookup"><span data-stu-id="c11d3-111">Channel</span></span>|<span data-ttu-id="c11d3-112">Microsoft-Windows-应用程序服务器-应用程序/分析</span><span class="sxs-lookup"><span data-stu-id="c11d3-112">Microsoft-Windows-Application Server-Applications/Analytic</span></span>|  
  
## <a name="description"></a><span data-ttu-id="c11d3-113">说明</span><span class="sxs-lookup"><span data-stu-id="c11d3-113">Description</span></span>  

 <span data-ttu-id="c11d3-114">将基于内容的相关用于工作流服务时将发出此事件。</span><span class="sxs-lookup"><span data-stu-id="c11d3-114">This event is emitted when content-based correlation is used for a workflow service.</span></span> <span data-ttu-id="c11d3-115">该事件包含为关联消息和实例而应用的相关键。</span><span class="sxs-lookup"><span data-stu-id="c11d3-115">It contains the correlation keys that are applied to correlate a message to an instance.</span></span>  
  
## <a name="message"></a><span data-ttu-id="c11d3-116">消息</span><span class="sxs-lookup"><span data-stu-id="c11d3-116">Message</span></span>  

 <span data-ttu-id="c11d3-117">使用父作用域“%3”中的值“%2”计算出的相关键“%1”。</span><span class="sxs-lookup"><span data-stu-id="c11d3-117">Calculated correlation key '%1' using values '%2' in parent scope '%3'.</span></span>  
  
## <a name="details"></a><span data-ttu-id="c11d3-118">详细信息</span><span class="sxs-lookup"><span data-stu-id="c11d3-118">Details</span></span>  
  
|<span data-ttu-id="c11d3-119">数据项名称</span><span class="sxs-lookup"><span data-stu-id="c11d3-119">Data Item Name</span></span>|<span data-ttu-id="c11d3-120">数据项类型</span><span class="sxs-lookup"><span data-stu-id="c11d3-120">Data Item Type</span></span>|<span data-ttu-id="c11d3-121">说明</span><span class="sxs-lookup"><span data-stu-id="c11d3-121">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="c11d3-122">实例键</span><span class="sxs-lookup"><span data-stu-id="c11d3-122">Instance Key</span></span>|`xs:GUID`|<span data-ttu-id="c11d3-123">依据相关值生成的键。</span><span class="sxs-lookup"><span data-stu-id="c11d3-123">The key that was generated from the correlation values.</span></span>|  
|<span data-ttu-id="c11d3-124">值</span><span class="sxs-lookup"><span data-stu-id="c11d3-124">Values</span></span>|`xs:string`|<span data-ttu-id="c11d3-125">用于计算相关实例键的值。</span><span class="sxs-lookup"><span data-stu-id="c11d3-125">The values that were used to compute the correlation instance key.</span></span>|  
|<span data-ttu-id="c11d3-126">父作用域</span><span class="sxs-lookup"><span data-stu-id="c11d3-126">Parent Scope</span></span>|`xs:string`||  
|<span data-ttu-id="c11d3-127">HostReference</span><span class="sxs-lookup"><span data-stu-id="c11d3-127">HostReference</span></span>|`xs:string`|<span data-ttu-id="c11d3-128">对于 Web 承载的服务，此字段唯一标识 Web 层次结构中的服务。</span><span class="sxs-lookup"><span data-stu-id="c11d3-128">For Web hosted services, this field uniquely identifies the service in the Web hierarchy.</span></span> <span data-ttu-id="c11d3-129">其格式定义为 "网站名称应用程序虚拟路径&#124;服务虚拟路径&#124;ServiceName"。</span><span class="sxs-lookup"><span data-stu-id="c11d3-129">Its format is defined as 'Web Site Name Application Virtual Path&#124;Service Virtual Path&#124;ServiceName'.</span></span> <span data-ttu-id="c11d3-130">示例： "Default Web Site//Calculatorapplication&#124;/CalculatorService.svc&#124;CalculatorService"。</span><span class="sxs-lookup"><span data-stu-id="c11d3-130">Example: 'Default Web Site/CalculatorApplication&#124;/CalculatorService.svc&#124;CalculatorService'.</span></span>|  
|<span data-ttu-id="c11d3-131">应用程序域</span><span class="sxs-lookup"><span data-stu-id="c11d3-131">AppDomain</span></span>|`xs:string`|<span data-ttu-id="c11d3-132">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="c11d3-132">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
