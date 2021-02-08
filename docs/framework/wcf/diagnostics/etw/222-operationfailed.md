---
description: 了解详细信息： 222-OperationFailed
title: 222 - OperationFailed
ms.date: 03/30/2017
ms.assetid: 6b530ded-8f20-4d78-8bfe-1875276df6ba
ms.openlocfilehash: ea07dbabb651413f213db6789f2af8059d2595c6
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99794294"
---
# <a name="222---operationfailed"></a><span data-ttu-id="c0d29-103">222 - OperationFailed</span><span class="sxs-lookup"><span data-stu-id="c0d29-103">222 - OperationFailed</span></span>

## <a name="properties"></a><span data-ttu-id="c0d29-104">属性</span><span class="sxs-lookup"><span data-stu-id="c0d29-104">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="c0d29-105">ID</span><span class="sxs-lookup"><span data-stu-id="c0d29-105">ID</span></span>|<span data-ttu-id="c0d29-106">222</span><span class="sxs-lookup"><span data-stu-id="c0d29-106">222</span></span>|  
|<span data-ttu-id="c0d29-107">关键字</span><span class="sxs-lookup"><span data-stu-id="c0d29-107">Keywords</span></span>|<span data-ttu-id="c0d29-108">EndToEndMonitoring、HealthMonitoring、疑难解答、ServiceModel</span><span class="sxs-lookup"><span data-stu-id="c0d29-108">EndToEndMonitoring, HealthMonitoring, Troubleshooting, ServiceModel</span></span>|  
|<span data-ttu-id="c0d29-109">级别</span><span class="sxs-lookup"><span data-stu-id="c0d29-109">Level</span></span>|<span data-ttu-id="c0d29-110">警告</span><span class="sxs-lookup"><span data-stu-id="c0d29-110">Warning</span></span>|  
|<span data-ttu-id="c0d29-111">通道</span><span class="sxs-lookup"><span data-stu-id="c0d29-111">Channel</span></span>|<span data-ttu-id="c0d29-112">Microsoft-Windows-应用程序服务器-应用程序/分析</span><span class="sxs-lookup"><span data-stu-id="c0d29-112">Microsoft-Windows-Application Server-Applications/Analytic</span></span>|  
  
## <a name="description"></a><span data-ttu-id="c0d29-113">说明</span><span class="sxs-lookup"><span data-stu-id="c0d29-113">Description</span></span>  

 <span data-ttu-id="c0d29-114">如果服务模型的默认 `OperationInvoker` 在调用其方法时遇到异常，则会发出此事件。</span><span class="sxs-lookup"><span data-stu-id="c0d29-114">This event is emitted when the Service Model's default `OperationInvoker` has encountered an exception while invoking its method.</span></span> <span data-ttu-id="c0d29-115">请注意，派生自 `FaultException` 的异常会导致不发出此事件。</span><span class="sxs-lookup"><span data-stu-id="c0d29-115">Note that exceptions that derive from `FaultException` cause this event to not be emitted.</span></span>  
  
## <a name="message"></a><span data-ttu-id="c0d29-116">消息</span><span class="sxs-lookup"><span data-stu-id="c0d29-116">Message</span></span>  

 <span data-ttu-id="c0d29-117">“%1”方法在由 OperationInvoker 调用时引发了未经处理的异常。</span><span class="sxs-lookup"><span data-stu-id="c0d29-117">The '%1' method threw an unhandled exception when invoked by the OperationInvoker.</span></span> <span data-ttu-id="c0d29-118">该方法调用持续了“%2”毫秒。</span><span class="sxs-lookup"><span data-stu-id="c0d29-118">The method call duration was '%2' ms.</span></span>  
  
## <a name="details"></a><span data-ttu-id="c0d29-119">详细信息</span><span class="sxs-lookup"><span data-stu-id="c0d29-119">Details</span></span>  
  
|<span data-ttu-id="c0d29-120">数据项名称</span><span class="sxs-lookup"><span data-stu-id="c0d29-120">Data Item Name</span></span>|<span data-ttu-id="c0d29-121">数据项类型</span><span class="sxs-lookup"><span data-stu-id="c0d29-121">Data Item Type</span></span>|<span data-ttu-id="c0d29-122">说明</span><span class="sxs-lookup"><span data-stu-id="c0d29-122">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="c0d29-123">方法名</span><span class="sxs-lookup"><span data-stu-id="c0d29-123">Method Name</span></span>|`xs:string`|<span data-ttu-id="c0d29-124">由 `OperationInvoker` 调用的方法的 CLR 名称。</span><span class="sxs-lookup"><span data-stu-id="c0d29-124">The CLR name of the method that was invoked by the `OperationInvoker`.</span></span>|  
|<span data-ttu-id="c0d29-125">持续时间</span><span class="sxs-lookup"><span data-stu-id="c0d29-125">Duration</span></span>|`xs:long`|<span data-ttu-id="c0d29-126">`OperationInvoker` 调用方法所花费的时间（以毫秒为单位）。</span><span class="sxs-lookup"><span data-stu-id="c0d29-126">The time, in milliseconds, that it took the `OperationInvoker` to invoke the method.</span></span>|  
|<span data-ttu-id="c0d29-127">HostReference</span><span class="sxs-lookup"><span data-stu-id="c0d29-127">HostReference</span></span>|`xs:string`|<span data-ttu-id="c0d29-128">对于 Web 承载的服务，此字段唯一标识 Web 层次结构中的服务。</span><span class="sxs-lookup"><span data-stu-id="c0d29-128">For Web-hosted services, this field uniquely identifies the service in the Web hierarchy.</span></span> <span data-ttu-id="c0d29-129">其格式定义为 "网站名称应用程序虚拟路径&#124;服务虚拟路径&#124;ServiceName"。</span><span class="sxs-lookup"><span data-stu-id="c0d29-129">Its format is defined as 'Web Site Name Application Virtual Path&#124;Service Virtual Path&#124;ServiceName'.</span></span> <span data-ttu-id="c0d29-130">示例： "Default Web Site//Calculatorapplication&#124;/CalculatorService.svc&#124;CalculatorService"。</span><span class="sxs-lookup"><span data-stu-id="c0d29-130">Example: 'Default Web Site/CalculatorApplication&#124;/CalculatorService.svc&#124;CalculatorService'.</span></span>|  
|<span data-ttu-id="c0d29-131">应用程序域</span><span class="sxs-lookup"><span data-stu-id="c0d29-131">AppDomain</span></span>|`xs:string`|<span data-ttu-id="c0d29-132">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="c0d29-132">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
