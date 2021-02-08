---
description: 了解详细信息： 217-ClientOperationPrepared
title: 217 - ClientOperationPrepared
ms.date: 03/30/2017
ms.assetid: ad207f04-b038-4f33-95e9-27a361df8ecd
ms.openlocfilehash: eab6a9a654e6e48a8831f238cdf3a3bf7a9f62d2
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99794346"
---
# <a name="217---clientoperationprepared"></a><span data-ttu-id="23a3d-103">217 - ClientOperationPrepared</span><span class="sxs-lookup"><span data-stu-id="23a3d-103">217 - ClientOperationPrepared</span></span>

## <a name="properties"></a><span data-ttu-id="23a3d-104">属性</span><span class="sxs-lookup"><span data-stu-id="23a3d-104">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="23a3d-105">ID</span><span class="sxs-lookup"><span data-stu-id="23a3d-105">ID</span></span>|<span data-ttu-id="23a3d-106">217</span><span class="sxs-lookup"><span data-stu-id="23a3d-106">217</span></span>|  
|<span data-ttu-id="23a3d-107">关键字</span><span class="sxs-lookup"><span data-stu-id="23a3d-107">Keywords</span></span>|<span data-ttu-id="23a3d-108">疑难解答，ServiceModel</span><span class="sxs-lookup"><span data-stu-id="23a3d-108">Troubleshooting, ServiceModel</span></span>|  
|<span data-ttu-id="23a3d-109">级别</span><span class="sxs-lookup"><span data-stu-id="23a3d-109">Level</span></span>|<span data-ttu-id="23a3d-110">信息</span><span class="sxs-lookup"><span data-stu-id="23a3d-110">Information</span></span>|  
|<span data-ttu-id="23a3d-111">通道</span><span class="sxs-lookup"><span data-stu-id="23a3d-111">Channel</span></span>|<span data-ttu-id="23a3d-112">Microsoft-Windows-应用程序服务器-应用程序/分析</span><span class="sxs-lookup"><span data-stu-id="23a3d-112">Microsoft-Windows-Application Server-Applications/Analytic</span></span>|  
  
## <a name="description"></a><span data-ttu-id="23a3d-113">说明</span><span class="sxs-lookup"><span data-stu-id="23a3d-113">Description</span></span>  

 <span data-ttu-id="23a3d-114">此事件恰好在将操作发送到服务之前由客户端发出。</span><span class="sxs-lookup"><span data-stu-id="23a3d-114">This event is emitted by clients just before an operation is sent to the service.</span></span>  
  
## <a name="message"></a><span data-ttu-id="23a3d-115">消息</span><span class="sxs-lookup"><span data-stu-id="23a3d-115">Message</span></span>  

 <span data-ttu-id="23a3d-116">客户端正在执行与协定“%2”相关联的操作“%1”。</span><span class="sxs-lookup"><span data-stu-id="23a3d-116">The Client is executing Action '%1' associated with the '%2' contract.</span></span> <span data-ttu-id="23a3d-117">消息将发送到“%3”。</span><span class="sxs-lookup"><span data-stu-id="23a3d-117">The message will be sent to '%3'.</span></span>  
  
## <a name="details"></a><span data-ttu-id="23a3d-118">详细信息</span><span class="sxs-lookup"><span data-stu-id="23a3d-118">Details</span></span>  
  
|<span data-ttu-id="23a3d-119">数据项名称</span><span class="sxs-lookup"><span data-stu-id="23a3d-119">Data Item Name</span></span>|<span data-ttu-id="23a3d-120">数据项类型</span><span class="sxs-lookup"><span data-stu-id="23a3d-120">Data Item Type</span></span>|<span data-ttu-id="23a3d-121">说明</span><span class="sxs-lookup"><span data-stu-id="23a3d-121">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="23a3d-122">操作</span><span class="sxs-lookup"><span data-stu-id="23a3d-122">Action</span></span>|`xs:string`|<span data-ttu-id="23a3d-123">传出消息的 SOAP 操作标头。</span><span class="sxs-lookup"><span data-stu-id="23a3d-123">The SOAP action header of the outgoing message.</span></span>|  
|<span data-ttu-id="23a3d-124">协定名称</span><span class="sxs-lookup"><span data-stu-id="23a3d-124">Contract Name</span></span>|`xs:string`|<span data-ttu-id="23a3d-125">协定的名称。</span><span class="sxs-lookup"><span data-stu-id="23a3d-125">The name of the contract.</span></span> <span data-ttu-id="23a3d-126">示例：ICalculator。</span><span class="sxs-lookup"><span data-stu-id="23a3d-126">Example: ICalculator.</span></span>|  
|<span data-ttu-id="23a3d-127">目标</span><span class="sxs-lookup"><span data-stu-id="23a3d-127">Destination</span></span>|`xs:string`|<span data-ttu-id="23a3d-128">消息发送到的服务终结点的地址。</span><span class="sxs-lookup"><span data-stu-id="23a3d-128">The address of the service endpoint that the message is sent to.</span></span>|  
|<span data-ttu-id="23a3d-129">HostReference</span><span class="sxs-lookup"><span data-stu-id="23a3d-129">HostReference</span></span>|`xs:string`|<span data-ttu-id="23a3d-130">对于 Web 承载的服务，此字段唯一标识 Web 层次结构中的服务。</span><span class="sxs-lookup"><span data-stu-id="23a3d-130">For Web-hosted services, this field uniquely identifies the service in the Web hierarchy.</span></span> <span data-ttu-id="23a3d-131">其格式定义为 "网站名称应用程序虚拟路径&#124;服务虚拟路径&#124;ServiceName"。</span><span class="sxs-lookup"><span data-stu-id="23a3d-131">Its format is defined as 'Web Site Name Application Virtual Path&#124;Service Virtual Path&#124;ServiceName'.</span></span> <span data-ttu-id="23a3d-132">示例： "Default Web Site//Calculatorapplication&#124;/CalculatorService.svc&#124;CalculatorService"。</span><span class="sxs-lookup"><span data-stu-id="23a3d-132">Example: 'Default Web Site/CalculatorApplication&#124;/CalculatorService.svc&#124;CalculatorService'.</span></span>|  
|<span data-ttu-id="23a3d-133">应用程序域</span><span class="sxs-lookup"><span data-stu-id="23a3d-133">AppDomain</span></span>|`xs:string`|<span data-ttu-id="23a3d-134">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="23a3d-134">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
