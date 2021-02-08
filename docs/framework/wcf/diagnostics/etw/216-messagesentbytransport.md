---
description: 了解详细信息： 216-MessageSentByTransport
title: 216 - MessageSentByTransport
ms.date: 03/30/2017
ms.assetid: 150c3167-4154-4225-8d94-57cc94341233
ms.openlocfilehash: 34c10fbbf61adde102641cb44db6645ea648a646
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99794372"
---
# <a name="216---messagesentbytransport"></a><span data-ttu-id="80344-103">216 - MessageSentByTransport</span><span class="sxs-lookup"><span data-stu-id="80344-103">216 - MessageSentByTransport</span></span>

## <a name="properties"></a><span data-ttu-id="80344-104">属性</span><span class="sxs-lookup"><span data-stu-id="80344-104">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="80344-105">ID</span><span class="sxs-lookup"><span data-stu-id="80344-105">ID</span></span>|<span data-ttu-id="80344-106">216</span><span class="sxs-lookup"><span data-stu-id="80344-106">216</span></span>|  
|<span data-ttu-id="80344-107">关键字</span><span class="sxs-lookup"><span data-stu-id="80344-107">Keywords</span></span>|<span data-ttu-id="80344-108">疑难解答，ServiceModel</span><span class="sxs-lookup"><span data-stu-id="80344-108">Troubleshooting, ServiceModel</span></span>|  
|<span data-ttu-id="80344-109">级别</span><span class="sxs-lookup"><span data-stu-id="80344-109">Level</span></span>|<span data-ttu-id="80344-110">信息</span><span class="sxs-lookup"><span data-stu-id="80344-110">Information</span></span>|  
|<span data-ttu-id="80344-111">通道</span><span class="sxs-lookup"><span data-stu-id="80344-111">Channel</span></span>|<span data-ttu-id="80344-112">Microsoft-Windows-应用程序服务器-应用程序/分析</span><span class="sxs-lookup"><span data-stu-id="80344-112">Microsoft-Windows-Application Server-Applications/Analytic</span></span>|  
  
## <a name="description"></a><span data-ttu-id="80344-113">说明</span><span class="sxs-lookup"><span data-stu-id="80344-113">Description</span></span>  

 <span data-ttu-id="80344-114">使用基于 TCP 的传输发送消息时发生此事件。</span><span class="sxs-lookup"><span data-stu-id="80344-114">This event occurs when a TCP-based transport sends a message.</span></span> <span data-ttu-id="80344-115">请注意，在传输级别上，单个操作可在客户端和服务之间交换多条消息。</span><span class="sxs-lookup"><span data-stu-id="80344-115">Note that at the transport level multiple messages can be exchanged between clients and services for a single operation.</span></span> <span data-ttu-id="80344-116">这可能是由于基础结构行为的特点，在此方面，安全性是一个很好的例子。</span><span class="sxs-lookup"><span data-stu-id="80344-116">This may be due to infrastructure behavior, security being a good example.</span></span> <span data-ttu-id="80344-117">因此，发出的 **MessageSentByTransport** 事件数因服务的绑定和其配置而异。</span><span class="sxs-lookup"><span data-stu-id="80344-117">Therefore, the number of **MessageSentByTransport** events that are emitted vary based on your service's binding and its configuration.</span></span>  
  
## <a name="message"></a><span data-ttu-id="80344-118">消息</span><span class="sxs-lookup"><span data-stu-id="80344-118">Message</span></span>  

 <span data-ttu-id="80344-119">传输向“%1”发送了一条消息。</span><span class="sxs-lookup"><span data-stu-id="80344-119">The transport sent a message to '%1'.</span></span>  
  
## <a name="details"></a><span data-ttu-id="80344-120">详细信息</span><span class="sxs-lookup"><span data-stu-id="80344-120">Details</span></span>  
  
|<span data-ttu-id="80344-121">数据项名称</span><span class="sxs-lookup"><span data-stu-id="80344-121">Data Item Name</span></span>|<span data-ttu-id="80344-122">数据项类型</span><span class="sxs-lookup"><span data-stu-id="80344-122">Data Item Type</span></span>|<span data-ttu-id="80344-123">说明</span><span class="sxs-lookup"><span data-stu-id="80344-123">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="80344-124">目的地地址</span><span class="sxs-lookup"><span data-stu-id="80344-124">DestinationAddress</span></span>|`xs:string`|<span data-ttu-id="80344-125">将请求消息发送到的地址。</span><span class="sxs-lookup"><span data-stu-id="80344-125">The address that the request message was sent to.</span></span>|  
|<span data-ttu-id="80344-126">HostReference</span><span class="sxs-lookup"><span data-stu-id="80344-126">HostReference</span></span>|<span data-ttu-id="80344-127">xs:string</span><span class="sxs-lookup"><span data-stu-id="80344-127">xs:string</span></span>|<span data-ttu-id="80344-128">对于 Web 承载的服务，此字段唯一标识 Web 层次结构中的服务。</span><span class="sxs-lookup"><span data-stu-id="80344-128">For Web-hosted services, this field uniquely identifies the service in the Web hierarchy.</span></span> <span data-ttu-id="80344-129">其格式定义为 "网站名称应用程序虚拟路径&#124;服务虚拟路径&#124;ServiceName"。</span><span class="sxs-lookup"><span data-stu-id="80344-129">Its format is defined as 'Web Site Name Application Virtual Path&#124;Service Virtual Path&#124;ServiceName'.</span></span> <span data-ttu-id="80344-130">示例： "Default Web Site//Calculatorapplication&#124;/CalculatorService.svc&#124;CalculatorService"。</span><span class="sxs-lookup"><span data-stu-id="80344-130">Example: 'Default Web Site/CalculatorApplication&#124;/CalculatorService.svc&#124;CalculatorService'.</span></span>|  
|<span data-ttu-id="80344-131">应用程序域</span><span class="sxs-lookup"><span data-stu-id="80344-131">AppDomain</span></span>|`xs:string`|<span data-ttu-id="80344-132">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="80344-132">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
