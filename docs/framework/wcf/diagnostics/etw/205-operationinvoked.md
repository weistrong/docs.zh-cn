---
description: 了解详细信息： 205-OperationInvoked
title: 205 - OperationInvoked
ms.date: 03/30/2017
ms.assetid: 9c8d6c90-dfa5-4ae0-a589-96679a8fb3ba
ms.openlocfilehash: 09afe4c29c5f56b06bbf524dd13d88ddf2319063
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99644965"
---
# <a name="205---operationinvoked"></a><span data-ttu-id="2698f-103">205 - OperationInvoked</span><span class="sxs-lookup"><span data-stu-id="2698f-103">205 - OperationInvoked</span></span>

## <a name="properties"></a><span data-ttu-id="2698f-104">属性</span><span class="sxs-lookup"><span data-stu-id="2698f-104">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="2698f-105">ID</span><span class="sxs-lookup"><span data-stu-id="2698f-105">ID</span></span>|<span data-ttu-id="2698f-106">205</span><span class="sxs-lookup"><span data-stu-id="2698f-106">205</span></span>|  
|<span data-ttu-id="2698f-107">关键字</span><span class="sxs-lookup"><span data-stu-id="2698f-107">Keywords</span></span>|<span data-ttu-id="2698f-108">疑难解答，ServiceModel</span><span class="sxs-lookup"><span data-stu-id="2698f-108">Troubleshooting, ServiceModel</span></span>|  
|<span data-ttu-id="2698f-109">级别</span><span class="sxs-lookup"><span data-stu-id="2698f-109">Level</span></span>|<span data-ttu-id="2698f-110">信息</span><span class="sxs-lookup"><span data-stu-id="2698f-110">Information</span></span>|  
|<span data-ttu-id="2698f-111">通道</span><span class="sxs-lookup"><span data-stu-id="2698f-111">Channel</span></span>|<span data-ttu-id="2698f-112">Microsoft-Windows-应用程序服务器-应用程序/分析</span><span class="sxs-lookup"><span data-stu-id="2698f-112">Microsoft-Windows-Application Server-Applications/Analytic</span></span>|  
  
## <a name="description"></a><span data-ttu-id="2698f-113">说明</span><span class="sxs-lookup"><span data-stu-id="2698f-113">Description</span></span>  

 <span data-ttu-id="2698f-114">恰好在服务模型的默认 `OperationInvoker` 开始调用方法之前发出此事件。</span><span class="sxs-lookup"><span data-stu-id="2698f-114">This event is emitted just before the Service Model's default `OperationInvoker` begins a call to a method.</span></span>  
  
## <a name="message"></a><span data-ttu-id="2698f-115">消息</span><span class="sxs-lookup"><span data-stu-id="2698f-115">Message</span></span>  

 <span data-ttu-id="2698f-116">OperationInvoker 调用了“%1”方法。</span><span class="sxs-lookup"><span data-stu-id="2698f-116">An OperationInvoker invoked the '%1' method.</span></span> <span data-ttu-id="2698f-117">调用方信息:“%2”。</span><span class="sxs-lookup"><span data-stu-id="2698f-117">Caller information: '%2'.</span></span>  
  
## <a name="details"></a><span data-ttu-id="2698f-118">详细信息</span><span class="sxs-lookup"><span data-stu-id="2698f-118">Details</span></span>  
  
|<span data-ttu-id="2698f-119">数据项名称</span><span class="sxs-lookup"><span data-stu-id="2698f-119">Data Item Name</span></span>|<span data-ttu-id="2698f-120">数据项类型</span><span class="sxs-lookup"><span data-stu-id="2698f-120">Data Item Type</span></span>|<span data-ttu-id="2698f-121">说明</span><span class="sxs-lookup"><span data-stu-id="2698f-121">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="2698f-122">方法名</span><span class="sxs-lookup"><span data-stu-id="2698f-122">Method Name</span></span>|`xs:string`|<span data-ttu-id="2698f-123">由 `OperationInvoker` 调用的方法的 CLR 名称。</span><span class="sxs-lookup"><span data-stu-id="2698f-123">The CLR name of the method that was invoked by the `OperationInvoker`.</span></span>|  
|<span data-ttu-id="2698f-124">调用方信息</span><span class="sxs-lookup"><span data-stu-id="2698f-124">Caller Information</span></span>|`xs:string`|<span data-ttu-id="2698f-125">客户端 IP 地址和端口号（格式为“IPAddress:PortNumber”）。</span><span class="sxs-lookup"><span data-stu-id="2698f-125">The IP address and port number of the client in the format 'IPAddress:PortNumber'.</span></span> <span data-ttu-id="2698f-126">需要从操作上下文的“System.ServiceModel.Channels.RemoteEndpointMessageProperty”消息属性中检索这两个值。</span><span class="sxs-lookup"><span data-stu-id="2698f-126">The two values are retrieved from the 'System.ServiceModel.Channels.RemoteEndpointMessageProperty' message property within the operation context.</span></span> <span data-ttu-id="2698f-127">请注意，对于非 TCP 绑定，该值为 `null`。</span><span class="sxs-lookup"><span data-stu-id="2698f-127">Note that for non-TCP bindings this value `null`.</span></span>|  
|<span data-ttu-id="2698f-128">HostReference</span><span class="sxs-lookup"><span data-stu-id="2698f-128">HostReference</span></span>|`xs:string`|<span data-ttu-id="2698f-129">对于 Web 承载的服务，此字段唯一标识 Web 层次结构中的服务。</span><span class="sxs-lookup"><span data-stu-id="2698f-129">For Web-hosted services, this field uniquely identifies the service in the Web hierarchy.</span></span> <span data-ttu-id="2698f-130">其格式定义为 "网站名称应用程序虚拟路径&#124;服务虚拟路径&#124;ServiceName"。</span><span class="sxs-lookup"><span data-stu-id="2698f-130">Its format is defined as 'Web Site Name Application Virtual Path&#124;Service Virtual Path&#124;ServiceName'.</span></span> <span data-ttu-id="2698f-131">示例： "Default Web Site//Calculatorapplication&#124;/CalculatorService.svc&#124;CalculatorService"。</span><span class="sxs-lookup"><span data-stu-id="2698f-131">Example: 'Default Web Site/CalculatorApplication&#124;/CalculatorService.svc&#124;CalculatorService'.</span></span>|  
|<span data-ttu-id="2698f-132">应用程序域</span><span class="sxs-lookup"><span data-stu-id="2698f-132">AppDomain</span></span>|`xs:string`|<span data-ttu-id="2698f-133">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="2698f-133">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
