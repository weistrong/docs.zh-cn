---
description: 了解详细信息： 220-MessageSentToTransport
title: 220 - MessageSentToTransport
ms.date: 03/30/2017
ms.assetid: aef4e781-240b-45bc-bff8-400053037e71
ms.openlocfilehash: 8d76f147c8a31a5aa08c21073cd03e63436095ff
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99794307"
---
# <a name="220---messagesenttotransport"></a><span data-ttu-id="c7d74-103">220 - MessageSentToTransport</span><span class="sxs-lookup"><span data-stu-id="c7d74-103">220 - MessageSentToTransport</span></span>

## <a name="properties"></a><span data-ttu-id="c7d74-104">属性</span><span class="sxs-lookup"><span data-stu-id="c7d74-104">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="c7d74-105">ID</span><span class="sxs-lookup"><span data-stu-id="c7d74-105">Id</span></span>|<span data-ttu-id="c7d74-106">220</span><span class="sxs-lookup"><span data-stu-id="c7d74-106">220</span></span>|  
|<span data-ttu-id="c7d74-107">关键字</span><span class="sxs-lookup"><span data-stu-id="c7d74-107">Keywords</span></span>|<span data-ttu-id="c7d74-108">EndToEndMonitoring，疑难解答，ServiceModel</span><span class="sxs-lookup"><span data-stu-id="c7d74-108">EndToEndMonitoring, Troubleshooting, ServiceModel</span></span>|  
|<span data-ttu-id="c7d74-109">级别</span><span class="sxs-lookup"><span data-stu-id="c7d74-109">Level</span></span>|<span data-ttu-id="c7d74-110">信息</span><span class="sxs-lookup"><span data-stu-id="c7d74-110">Information</span></span>|  
|<span data-ttu-id="c7d74-111">通道</span><span class="sxs-lookup"><span data-stu-id="c7d74-111">Channel</span></span>|<span data-ttu-id="c7d74-112">Microsoft-Windows-应用程序服务器-应用程序/分析</span><span class="sxs-lookup"><span data-stu-id="c7d74-112">Microsoft-Windows-Application Server-Applications/Analytic</span></span>|  
  
## <a name="description"></a><span data-ttu-id="c7d74-113">说明</span><span class="sxs-lookup"><span data-stu-id="c7d74-113">Description</span></span>  

 <span data-ttu-id="c7d74-114">服务模型向传输发送消息时将发出此事件。</span><span class="sxs-lookup"><span data-stu-id="c7d74-114">This event is emitted when the Service Model sends a message to the transport.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="c7d74-115">不会为单向传输发出此事件。</span><span class="sxs-lookup"><span data-stu-id="c7d74-115">This event will not be emitted for one-way transports.</span></span>  
  
## <a name="message"></a><span data-ttu-id="c7d74-116">消息</span><span class="sxs-lookup"><span data-stu-id="c7d74-116">Message</span></span>  

 <span data-ttu-id="c7d74-117">调度程序向传输发送了一条消息。</span><span class="sxs-lookup"><span data-stu-id="c7d74-117">The Dispatcher sent a message to the transport.</span></span> <span data-ttu-id="c7d74-118">相关 ID 为“%1”。</span><span class="sxs-lookup"><span data-stu-id="c7d74-118">Correlation ID == '%1'.</span></span>  
  
## <a name="details"></a><span data-ttu-id="c7d74-119">详细信息</span><span class="sxs-lookup"><span data-stu-id="c7d74-119">Details</span></span>  
  
|<span data-ttu-id="c7d74-120">数据项名称</span><span class="sxs-lookup"><span data-stu-id="c7d74-120">Data Item Name</span></span>|<span data-ttu-id="c7d74-121">数据项类型</span><span class="sxs-lookup"><span data-stu-id="c7d74-121">Data Item Type</span></span>|<span data-ttu-id="c7d74-122">说明</span><span class="sxs-lookup"><span data-stu-id="c7d74-122">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="c7d74-123">相关性 ID</span><span class="sxs-lookup"><span data-stu-id="c7d74-123">Correlation ID</span></span>|`xs:GUID`|<span data-ttu-id="c7d74-124">用于将服务或客户端的 `MessageSentToTransport` 事件与另一端的对应 `MessageReceivedFromTransport` 相关的活动 ID。</span><span class="sxs-lookup"><span data-stu-id="c7d74-124">The activity ID used to correlate a `MessageSentToTransport` event from a service or client to its corresponding `MessageReceivedFromTransport` on the other end.</span></span>|  
|<span data-ttu-id="c7d74-125">HostReference</span><span class="sxs-lookup"><span data-stu-id="c7d74-125">HostReference</span></span>|`xs:string`|<span data-ttu-id="c7d74-126">对于 Web 承载的服务，此字段唯一标识 Web 层次结构中的服务。</span><span class="sxs-lookup"><span data-stu-id="c7d74-126">For Web-hosted services, this field uniquely identifies the service in the Web hierarchy.</span></span> <span data-ttu-id="c7d74-127">其格式定义为 "网站名称应用程序虚拟路径&#124;服务虚拟路径&#124;ServiceName"。</span><span class="sxs-lookup"><span data-stu-id="c7d74-127">Its format is defined as 'Web Site Name Application Virtual Path&#124;Service Virtual Path&#124;ServiceName'.</span></span> <span data-ttu-id="c7d74-128">示例： "Default Web Site//Calculatorapplication&#124;/CalculatorService.svc&#124;CalculatorService"。</span><span class="sxs-lookup"><span data-stu-id="c7d74-128">Example: 'Default Web Site/CalculatorApplication&#124;/CalculatorService.svc&#124;CalculatorService'.</span></span>|  
|<span data-ttu-id="c7d74-129">应用程序域</span><span class="sxs-lookup"><span data-stu-id="c7d74-129">AppDomain</span></span>|`xs:string`|<span data-ttu-id="c7d74-130">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="c7d74-130">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
