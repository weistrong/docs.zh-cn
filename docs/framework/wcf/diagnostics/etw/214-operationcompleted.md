---
description: 了解详细信息： 214-OperationCompleted
title: 214 - OperationCompleted
ms.date: 03/30/2017
ms.assetid: a6287eef-023f-4816-813c-1802c82366df
ms.openlocfilehash: aad1ac49667a2ebbf172b5132507584e05d0f03e
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99794385"
---
# <a name="214---operationcompleted"></a><span data-ttu-id="c732f-103">214 - OperationCompleted</span><span class="sxs-lookup"><span data-stu-id="c732f-103">214 - OperationCompleted</span></span>

## <a name="properties"></a><span data-ttu-id="c732f-104">属性</span><span class="sxs-lookup"><span data-stu-id="c732f-104">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="c732f-105">ID</span><span class="sxs-lookup"><span data-stu-id="c732f-105">ID</span></span>|<span data-ttu-id="c732f-106">214</span><span class="sxs-lookup"><span data-stu-id="c732f-106">214</span></span>|  
|<span data-ttu-id="c732f-107">关键字</span><span class="sxs-lookup"><span data-stu-id="c732f-107">Keywords</span></span>|<span data-ttu-id="c732f-108">HealthMonitoring，EndToEndMonitoring，疑难解答，ServiceModel</span><span class="sxs-lookup"><span data-stu-id="c732f-108">HealthMonitoring, EndToEndMonitoring, Troubleshooting, ServiceModel</span></span>|  
|<span data-ttu-id="c732f-109">级别</span><span class="sxs-lookup"><span data-stu-id="c732f-109">Level</span></span>|<span data-ttu-id="c732f-110">信息</span><span class="sxs-lookup"><span data-stu-id="c732f-110">Information</span></span>|  
|<span data-ttu-id="c732f-111">通道</span><span class="sxs-lookup"><span data-stu-id="c732f-111">Channel</span></span>|<span data-ttu-id="c732f-112">Microsoft-Windows-应用程序服务器-应用程序/分析</span><span class="sxs-lookup"><span data-stu-id="c732f-112">Microsoft-Windows-Application Server-Applications/Analytic</span></span>|  
  
## <a name="description"></a><span data-ttu-id="c732f-113">说明</span><span class="sxs-lookup"><span data-stu-id="c732f-113">Description</span></span>  

 <span data-ttu-id="c732f-114">如果服务模型的默认 `OperationInvoker` 已完成对某一方法的调用且未导致该方法引发异常，将发出此事件。</span><span class="sxs-lookup"><span data-stu-id="c732f-114">This event is emitted when the Service Model's default `OperationInvoker` has completed a call to a method without that method throwing an exception.</span></span>  
  
## <a name="message"></a><span data-ttu-id="c732f-115">消息</span><span class="sxs-lookup"><span data-stu-id="c732f-115">Message</span></span>  

 <span data-ttu-id="c732f-116">OperationInvoker 已完成对“%1”方法的调用。</span><span class="sxs-lookup"><span data-stu-id="c732f-116">An OperationInvoker completed the call to the '%1' method.</span></span> <span data-ttu-id="c732f-117">该方法调用持续了“%2”毫秒。</span><span class="sxs-lookup"><span data-stu-id="c732f-117">The method call duration was '%2' ms.</span></span>  
  
## <a name="details"></a><span data-ttu-id="c732f-118">详细信息</span><span class="sxs-lookup"><span data-stu-id="c732f-118">Details</span></span>  
  
|<span data-ttu-id="c732f-119">数据项名称</span><span class="sxs-lookup"><span data-stu-id="c732f-119">Data Item Name</span></span>|<span data-ttu-id="c732f-120">数据项类型</span><span class="sxs-lookup"><span data-stu-id="c732f-120">Data Item Type</span></span>|<span data-ttu-id="c732f-121">说明</span><span class="sxs-lookup"><span data-stu-id="c732f-121">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="c732f-122">方法名</span><span class="sxs-lookup"><span data-stu-id="c732f-122">Method Name</span></span>|`xs:string`|<span data-ttu-id="c732f-123">由 `OperationInvoker` 调用的方法的 CLR 名称。</span><span class="sxs-lookup"><span data-stu-id="c732f-123">The CLR name of the method that was invoked by the `OperationInvoker`.</span></span>|  
|<span data-ttu-id="c732f-124">持续时间</span><span class="sxs-lookup"><span data-stu-id="c732f-124">Duration</span></span>|`xs:long`|<span data-ttu-id="c732f-125">`OperationInvoker` 调用方法所花费的时间（以毫秒为单位）。</span><span class="sxs-lookup"><span data-stu-id="c732f-125">The time, in milliseconds, that it took the `OperationInvoker` to invoke the method.</span></span>|  
|<span data-ttu-id="c732f-126">HostReference</span><span class="sxs-lookup"><span data-stu-id="c732f-126">HostReference</span></span>|`xs:string`|<span data-ttu-id="c732f-127">对于 Web 承载的服务，此字段唯一标识 Web 层次结构中的服务。</span><span class="sxs-lookup"><span data-stu-id="c732f-127">For web-hosted services, this field uniquely identifies the service in the Web hierarchy.</span></span> <span data-ttu-id="c732f-128">其格式定义为 "网站名称应用程序虚拟路径&#124;服务虚拟路径&#124;ServiceName"。</span><span class="sxs-lookup"><span data-stu-id="c732f-128">Its format is defined as 'Web Site Name Application Virtual Path&#124;Service Virtual Path&#124;ServiceName'.</span></span> <span data-ttu-id="c732f-129">示例： "Default Web Site//Calculatorapplication&#124;/CalculatorService.svc&#124;CalculatorService"。</span><span class="sxs-lookup"><span data-stu-id="c732f-129">Example: 'Default Web Site/CalculatorApplication&#124;/CalculatorService.svc&#124;CalculatorService'.</span></span>|  
|<span data-ttu-id="c732f-130">应用程序域</span><span class="sxs-lookup"><span data-stu-id="c732f-130">AppDomain</span></span>|`xs:string`|<span data-ttu-id="c732f-131">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="c732f-131">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
