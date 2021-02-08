---
description: 了解详细信息： 215-MessageReceivedByTransport
title: 215 - MessageReceivedByTransport
ms.date: 03/30/2017
ms.assetid: bb32aa60-5207-4711-9f08-110e8ac327e5
ms.openlocfilehash: e9645cfc8c4013f8891cb645db7df35477a57412
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99794359"
---
# <a name="215---messagereceivedbytransport"></a><span data-ttu-id="d81b5-103">215 - MessageReceivedByTransport</span><span class="sxs-lookup"><span data-stu-id="d81b5-103">215 - MessageReceivedByTransport</span></span>

## <a name="properties"></a><span data-ttu-id="d81b5-104">属性</span><span class="sxs-lookup"><span data-stu-id="d81b5-104">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="d81b5-105">ID</span><span class="sxs-lookup"><span data-stu-id="d81b5-105">ID</span></span>|<span data-ttu-id="d81b5-106">215</span><span class="sxs-lookup"><span data-stu-id="d81b5-106">215</span></span>|  
|<span data-ttu-id="d81b5-107">关键字</span><span class="sxs-lookup"><span data-stu-id="d81b5-107">Keywords</span></span>|<span data-ttu-id="d81b5-108">疑难解答，ServiceModel</span><span class="sxs-lookup"><span data-stu-id="d81b5-108">Troubleshooting, ServiceModel</span></span>|  
|<span data-ttu-id="d81b5-109">级别</span><span class="sxs-lookup"><span data-stu-id="d81b5-109">Level</span></span>|<span data-ttu-id="d81b5-110">信息</span><span class="sxs-lookup"><span data-stu-id="d81b5-110">Information</span></span>|  
|<span data-ttu-id="d81b5-111">通道</span><span class="sxs-lookup"><span data-stu-id="d81b5-111">Channel</span></span>|<span data-ttu-id="d81b5-112">Microsoft-Windows-应用程序服务器-应用程序/分析</span><span class="sxs-lookup"><span data-stu-id="d81b5-112">Microsoft-Windows-Application Server-Applications/Analytic</span></span>|  
  
## <a name="description"></a><span data-ttu-id="d81b5-113">说明</span><span class="sxs-lookup"><span data-stu-id="d81b5-113">Description</span></span>  

 <span data-ttu-id="d81b5-114">基于 TCP 的传输接收消息时将发生此事件。</span><span class="sxs-lookup"><span data-stu-id="d81b5-114">This event occurs when a TCP-based transport receives a message.</span></span> <span data-ttu-id="d81b5-115">请注意，在传输级别上，单个操作可在客户端和服务之间交换多条消息。</span><span class="sxs-lookup"><span data-stu-id="d81b5-115">Note that at the transport level, multiple messages can be exchanged between clients and services for a single operation.</span></span> <span data-ttu-id="d81b5-116">这可能是由于基础结构行为的特点，在此方面，安全性是一个很好的例子。</span><span class="sxs-lookup"><span data-stu-id="d81b5-116">This can be due to infrastructure behavior, security is a good example.</span></span> <span data-ttu-id="d81b5-117">因此，发出的 `MessageReceivedByTransport` 事件数目根据服务绑定及其配置而变化。</span><span class="sxs-lookup"><span data-stu-id="d81b5-117">Therefore, the number of `MessageReceivedByTransport` events that are emitted vary based on your service's binding and its configuration.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="d81b5-118">不会为单向传输发出此事件。</span><span class="sxs-lookup"><span data-stu-id="d81b5-118">This event is not emitted for one-way transports.</span></span>  
  
## <a name="message"></a><span data-ttu-id="d81b5-119">消息</span><span class="sxs-lookup"><span data-stu-id="d81b5-119">Message</span></span>  

 <span data-ttu-id="d81b5-120">传输从“%1”收到了一条消息。</span><span class="sxs-lookup"><span data-stu-id="d81b5-120">The transport received a message from '%1'.</span></span>  
  
## <a name="details"></a><span data-ttu-id="d81b5-121">详细信息</span><span class="sxs-lookup"><span data-stu-id="d81b5-121">Details</span></span>  
  
|<span data-ttu-id="d81b5-122">数据项名称</span><span class="sxs-lookup"><span data-stu-id="d81b5-122">Data Item Name</span></span>|<span data-ttu-id="d81b5-123">数据项类型</span><span class="sxs-lookup"><span data-stu-id="d81b5-123">Data Item Type</span></span>|<span data-ttu-id="d81b5-124">说明</span><span class="sxs-lookup"><span data-stu-id="d81b5-124">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="d81b5-125">侦听地址</span><span class="sxs-lookup"><span data-stu-id="d81b5-125">Listen Address</span></span>|`xs:string`|<span data-ttu-id="d81b5-126">接收了消息的地址。</span><span class="sxs-lookup"><span data-stu-id="d81b5-126">The address that received the message.</span></span>|  
|<span data-ttu-id="d81b5-127">HostReference</span><span class="sxs-lookup"><span data-stu-id="d81b5-127">HostReference</span></span>|`xs:string`|<span data-ttu-id="d81b5-128">对于 Web 承载的服务，此字段唯一标识 Web 层次结构中的服务。</span><span class="sxs-lookup"><span data-stu-id="d81b5-128">For Web-hosted services, this field uniquely identifies the service in the Web hierarchy.</span></span> <span data-ttu-id="d81b5-129">其格式定义为 "网站名称应用程序虚拟路径&#124;服务虚拟路径&#124;ServiceName"。</span><span class="sxs-lookup"><span data-stu-id="d81b5-129">Its format is defined as 'Web Site Name Application Virtual Path&#124;Service Virtual Path&#124;ServiceName'.</span></span> <span data-ttu-id="d81b5-130">示例： "Default Web Site//Calculatorapplication&#124;/CalculatorService.svc&#124;CalculatorService"。</span><span class="sxs-lookup"><span data-stu-id="d81b5-130">Example: 'Default Web Site/CalculatorApplication&#124;/CalculatorService.svc&#124;CalculatorService'.</span></span>|  
|<span data-ttu-id="d81b5-131">应用程序域</span><span class="sxs-lookup"><span data-stu-id="d81b5-131">AppDomain</span></span>|`xs:string`|<span data-ttu-id="d81b5-132">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="d81b5-132">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
