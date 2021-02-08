---
description: 了解详细信息： 221-MessageReceivedFromTransport
title: 221 - MessageReceivedFromTransport
ms.date: 03/30/2017
ms.assetid: 4995f0d5-c182-4d97-981f-6951da6df1fb
ms.openlocfilehash: 0cc15fa95ae321083afa2792810807971e909e6b
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99803498"
---
# <a name="221---messagereceivedfromtransport"></a><span data-ttu-id="164a4-103">221 - MessageReceivedFromTransport</span><span class="sxs-lookup"><span data-stu-id="164a4-103">221 - MessageReceivedFromTransport</span></span>

## <a name="properties"></a><span data-ttu-id="164a4-104">属性</span><span class="sxs-lookup"><span data-stu-id="164a4-104">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="164a4-105">ID</span><span class="sxs-lookup"><span data-stu-id="164a4-105">ID</span></span>|<span data-ttu-id="164a4-106">221</span><span class="sxs-lookup"><span data-stu-id="164a4-106">221</span></span>|  
|<span data-ttu-id="164a4-107">关键字</span><span class="sxs-lookup"><span data-stu-id="164a4-107">Keywords</span></span>|<span data-ttu-id="164a4-108">EndToEndMonitoring，疑难解答，ServiceModel</span><span class="sxs-lookup"><span data-stu-id="164a4-108">EndToEndMonitoring, Troubleshooting, ServiceModel</span></span>|  
|<span data-ttu-id="164a4-109">级别</span><span class="sxs-lookup"><span data-stu-id="164a4-109">Level</span></span>|<span data-ttu-id="164a4-110">信息</span><span class="sxs-lookup"><span data-stu-id="164a4-110">Information</span></span>|  
|<span data-ttu-id="164a4-111">通道</span><span class="sxs-lookup"><span data-stu-id="164a4-111">Channel</span></span>|<span data-ttu-id="164a4-112">Microsoft-Windows-应用程序服务器-应用程序/分析</span><span class="sxs-lookup"><span data-stu-id="164a4-112">Microsoft-Windows-Application Server-Applications/Analytic</span></span>|  
  
## <a name="description"></a><span data-ttu-id="164a4-113">说明</span><span class="sxs-lookup"><span data-stu-id="164a4-113">Description</span></span>  

 <span data-ttu-id="164a4-114">服务模型从传输中接收消息时将发出此事件。</span><span class="sxs-lookup"><span data-stu-id="164a4-114">This event is emitted when the Service Model receives a message from the transport.</span></span>  
  
## <a name="message"></a><span data-ttu-id="164a4-115">消息</span><span class="sxs-lookup"><span data-stu-id="164a4-115">Message</span></span>  

 <span data-ttu-id="164a4-116">调度程序从传输收到一条消息。</span><span class="sxs-lookup"><span data-stu-id="164a4-116">The Dispatcher received a message from the transport.</span></span> <span data-ttu-id="164a4-117">相关 ID 为“%1”。</span><span class="sxs-lookup"><span data-stu-id="164a4-117">Correlation ID == '%1'.</span></span>  
  
## <a name="details"></a><span data-ttu-id="164a4-118">详细信息</span><span class="sxs-lookup"><span data-stu-id="164a4-118">Details</span></span>  
  
|<span data-ttu-id="164a4-119">数据项名称</span><span class="sxs-lookup"><span data-stu-id="164a4-119">Data Item Name</span></span>|<span data-ttu-id="164a4-120">数据项类型</span><span class="sxs-lookup"><span data-stu-id="164a4-120">Data Item Type</span></span>|<span data-ttu-id="164a4-121">说明</span><span class="sxs-lookup"><span data-stu-id="164a4-121">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="164a4-122">相关性 ID</span><span class="sxs-lookup"><span data-stu-id="164a4-122">Correlation ID</span></span>|`xs:GUID`|<span data-ttu-id="164a4-123">用于将服务或客户端的 `MessageSentToTransport` 事件与另一端的对应 `MessageReceivedFromTransport` 相关的活动 ID。</span><span class="sxs-lookup"><span data-stu-id="164a4-123">The activity ID used to correlate a `MessageSentToTransport` event from a service or client to its corresponding `MessageReceivedFromTransport` on the other end.</span></span>|  
|<span data-ttu-id="164a4-124">HostReference</span><span class="sxs-lookup"><span data-stu-id="164a4-124">HostReference</span></span>|`xs:string`|<span data-ttu-id="164a4-125">对于 Web 承载的服务，此字段唯一标识 Web 层次结构中的服务。</span><span class="sxs-lookup"><span data-stu-id="164a4-125">For Web-hosted services, this field uniquely identifies the service in the Web hierarchy.</span></span> <span data-ttu-id="164a4-126">其格式定义为 "网站名称应用程序虚拟路径&#124;服务虚拟路径&#124;ServiceName"。</span><span class="sxs-lookup"><span data-stu-id="164a4-126">Its format is defined as 'Web Site Name Application Virtual Path&#124;Service Virtual Path&#124;ServiceName'.</span></span> <span data-ttu-id="164a4-127">示例： "Default Web Site//Calculatorapplication&#124;/CalculatorService.svc&#124;CalculatorService"。</span><span class="sxs-lookup"><span data-stu-id="164a4-127">Example: 'Default Web Site/CalculatorApplication&#124;/CalculatorService.svc&#124;CalculatorService'.</span></span>|  
|<span data-ttu-id="164a4-128">应用程序域</span><span class="sxs-lookup"><span data-stu-id="164a4-128">AppDomain</span></span>|`xs:string`|<span data-ttu-id="164a4-129">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="164a4-129">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
