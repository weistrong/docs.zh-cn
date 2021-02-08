---
description: 了解详细信息： 223-OperationFaulted
title: 223 - OperationFaulted
ms.date: 03/30/2017
ms.assetid: 2f7d89d7-3a6a-40fe-9610-5424eb6bbf61
ms.openlocfilehash: e4155516e07568d4ee4ca76d63754ec4171e1064
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99794281"
---
# <a name="223---operationfaulted"></a><span data-ttu-id="270da-103">223 - OperationFaulted</span><span class="sxs-lookup"><span data-stu-id="270da-103">223 - OperationFaulted</span></span>

## <a name="properties"></a><span data-ttu-id="270da-104">属性</span><span class="sxs-lookup"><span data-stu-id="270da-104">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="270da-105">ID</span><span class="sxs-lookup"><span data-stu-id="270da-105">ID</span></span>|<span data-ttu-id="270da-106">223</span><span class="sxs-lookup"><span data-stu-id="270da-106">223</span></span>|  
|<span data-ttu-id="270da-107">关键字</span><span class="sxs-lookup"><span data-stu-id="270da-107">Keywords</span></span>|<span data-ttu-id="270da-108">EndToEndMonitoring、HealthMonitoring、疑难解答、ServiceModel</span><span class="sxs-lookup"><span data-stu-id="270da-108">EndToEndMonitoring, HealthMonitoring, Troubleshooting, ServiceModel</span></span>|  
|<span data-ttu-id="270da-109">级别</span><span class="sxs-lookup"><span data-stu-id="270da-109">Level</span></span>|<span data-ttu-id="270da-110">警告</span><span class="sxs-lookup"><span data-stu-id="270da-110">Warning</span></span>|  
|<span data-ttu-id="270da-111">通道</span><span class="sxs-lookup"><span data-stu-id="270da-111">Channel</span></span>|<span data-ttu-id="270da-112">Microsoft-Windows-应用程序服务器-应用程序/分析</span><span class="sxs-lookup"><span data-stu-id="270da-112">Microsoft-Windows-Application Server-Applications/Analytic</span></span>|  
  
## <a name="description"></a><span data-ttu-id="270da-113">说明</span><span class="sxs-lookup"><span data-stu-id="270da-113">Description</span></span>  

 <span data-ttu-id="270da-114">服务模型的默认 `OperationInvoker` 在调用其方法期间出现派生自 `FaultException` 的异常时，将发出此事件。</span><span class="sxs-lookup"><span data-stu-id="270da-114">This event is emitted when the Service Model's default `OperationInvoker` has encountered an exception deriving from `FaultException` while invoking its method.</span></span>  
  
## <a name="message"></a><span data-ttu-id="270da-115">消息</span><span class="sxs-lookup"><span data-stu-id="270da-115">Message</span></span>  

 <span data-ttu-id="270da-116">“%1”方法在由 OperationInvoker 调用时引发了一个 FaultException。</span><span class="sxs-lookup"><span data-stu-id="270da-116">The '%1' method threw a FaultException when invoked by the OperationInvoker.</span></span> <span data-ttu-id="270da-117">该方法调用持续了“%2”毫秒。</span><span class="sxs-lookup"><span data-stu-id="270da-117">The method call duration was '%2' ms.</span></span>  
  
## <a name="details"></a><span data-ttu-id="270da-118">详细信息</span><span class="sxs-lookup"><span data-stu-id="270da-118">Details</span></span>  
  
|<span data-ttu-id="270da-119">数据项名称</span><span class="sxs-lookup"><span data-stu-id="270da-119">Data Item Name</span></span>|<span data-ttu-id="270da-120">数据项类型</span><span class="sxs-lookup"><span data-stu-id="270da-120">Data Item Type</span></span>|<span data-ttu-id="270da-121">说明</span><span class="sxs-lookup"><span data-stu-id="270da-121">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="270da-122">MethodName</span><span class="sxs-lookup"><span data-stu-id="270da-122">MethodName</span></span>|`xs:string`|<span data-ttu-id="270da-123">由 `OperationInvoker` 调用的方法的 CLR 名称。</span><span class="sxs-lookup"><span data-stu-id="270da-123">The CLR name of the method that was invoked by the `OperationInvoker`.</span></span>|  
|<span data-ttu-id="270da-124">持续时间</span><span class="sxs-lookup"><span data-stu-id="270da-124">Duration</span></span>|`xs:long`|<span data-ttu-id="270da-125">`OperationInvoker` 调用方法所花费的时间（以毫秒为单位）。</span><span class="sxs-lookup"><span data-stu-id="270da-125">The time, in milliseconds, that it took the `OperationInvoker` to invoke the method.</span></span>|  
|<span data-ttu-id="270da-126">HostReference</span><span class="sxs-lookup"><span data-stu-id="270da-126">HostReference</span></span>|`xs:string`|<span data-ttu-id="270da-127">对于 Web 承载的服务，此字段唯一标识 Web 层次结构中的服务。</span><span class="sxs-lookup"><span data-stu-id="270da-127">For Web-hosted services, this field uniquely identifies the service in the Web hierarchy.</span></span> <span data-ttu-id="270da-128">其格式定义为 "网站名称应用程序虚拟路径&#124;服务虚拟路径&#124;ServiceName"。</span><span class="sxs-lookup"><span data-stu-id="270da-128">Its format is defined as 'Web Site Name Application Virtual Path&#124;Service Virtual Path&#124;ServiceName'.</span></span> <span data-ttu-id="270da-129">示例： "Default Web Site//Calculatorapplication&#124;/CalculatorService.svc&#124;CalculatorService"。</span><span class="sxs-lookup"><span data-stu-id="270da-129">Example: 'Default Web Site/CalculatorApplication&#124;/CalculatorService.svc&#124;CalculatorService'.</span></span>|  
|<span data-ttu-id="270da-130">应用程序域</span><span class="sxs-lookup"><span data-stu-id="270da-130">AppDomain</span></span>|`xs:string`|<span data-ttu-id="270da-131">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="270da-131">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
