---
description: 了解详细信息： 218-ClientOperationCompleted
title: 218 - ClientOperationCompleted
ms.date: 03/30/2017
ms.assetid: b069bced-7bb2-4e01-8227-e5dbda17af09
ms.openlocfilehash: 3719b77ce653c5177cf7b92901ecd51982504b83
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99794333"
---
# <a name="218---clientoperationcompleted"></a><span data-ttu-id="b412e-103">218 - ClientOperationCompleted</span><span class="sxs-lookup"><span data-stu-id="b412e-103">218 - ClientOperationCompleted</span></span>

## <a name="properties"></a><span data-ttu-id="b412e-104">属性</span><span class="sxs-lookup"><span data-stu-id="b412e-104">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="b412e-105">ID</span><span class="sxs-lookup"><span data-stu-id="b412e-105">ID</span></span>|<span data-ttu-id="b412e-106">218</span><span class="sxs-lookup"><span data-stu-id="b412e-106">218</span></span>|  
|<span data-ttu-id="b412e-107">关键字</span><span class="sxs-lookup"><span data-stu-id="b412e-107">Keywords</span></span>|<span data-ttu-id="b412e-108">疑难解答，ServiceModel</span><span class="sxs-lookup"><span data-stu-id="b412e-108">Troubleshooting, ServiceModel</span></span>|  
|<span data-ttu-id="b412e-109">级别</span><span class="sxs-lookup"><span data-stu-id="b412e-109">Level</span></span>|<span data-ttu-id="b412e-110">信息</span><span class="sxs-lookup"><span data-stu-id="b412e-110">Information</span></span>|  
|<span data-ttu-id="b412e-111">通道</span><span class="sxs-lookup"><span data-stu-id="b412e-111">Channel</span></span>|<span data-ttu-id="b412e-112">Microsoft-Windows-应用程序服务器-应用程序/分析</span><span class="sxs-lookup"><span data-stu-id="b412e-112">Microsoft-Windows-Application Server-Applications/Analytic</span></span>|  
  
## <a name="description"></a><span data-ttu-id="b412e-113">说明</span><span class="sxs-lookup"><span data-stu-id="b412e-113">Description</span></span>  

 <span data-ttu-id="b412e-114">此事件恰好在操作完成之后由客户端发出。</span><span class="sxs-lookup"><span data-stu-id="b412e-114">This event is emitted by clients just after an operation completes.</span></span> <span data-ttu-id="b412e-115">对于单向操作，此事件恰好在成功发送消息之后发送。</span><span class="sxs-lookup"><span data-stu-id="b412e-115">For one-way operations, this is just after the message is sent successfully.</span></span> <span data-ttu-id="b412e-116">对于请求-响应操作，此事件在接收响应之后发送。</span><span class="sxs-lookup"><span data-stu-id="b412e-116">For request-response operations this is after the response is received.</span></span>  
  
## <a name="message"></a><span data-ttu-id="b412e-117">消息</span><span class="sxs-lookup"><span data-stu-id="b412e-117">Message</span></span>  

 <span data-ttu-id="b412e-118">客户端已执行完与协定“%2”相关联的操作“%1”。</span><span class="sxs-lookup"><span data-stu-id="b412e-118">The Client completed executing Action '%1' associated with the '%2' contract.</span></span> <span data-ttu-id="b412e-119">消息已发送到“%3”。</span><span class="sxs-lookup"><span data-stu-id="b412e-119">The message was sent to '%3'.</span></span>  
  
## <a name="details"></a><span data-ttu-id="b412e-120">详细信息</span><span class="sxs-lookup"><span data-stu-id="b412e-120">Details</span></span>  
  
|<span data-ttu-id="b412e-121">数据项名称</span><span class="sxs-lookup"><span data-stu-id="b412e-121">Data Item Name</span></span>|<span data-ttu-id="b412e-122">数据项类型</span><span class="sxs-lookup"><span data-stu-id="b412e-122">Data Item Type</span></span>|<span data-ttu-id="b412e-123">说明</span><span class="sxs-lookup"><span data-stu-id="b412e-123">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="b412e-124">操作</span><span class="sxs-lookup"><span data-stu-id="b412e-124">Action</span></span>|<span data-ttu-id="b412e-125">xs:string</span><span class="sxs-lookup"><span data-stu-id="b412e-125">xs:string</span></span>|<span data-ttu-id="b412e-126">传出消息的 SOAP 操作标头。</span><span class="sxs-lookup"><span data-stu-id="b412e-126">The SOAP action header of the outgoing message.</span></span>|  
|<span data-ttu-id="b412e-127">协定名称</span><span class="sxs-lookup"><span data-stu-id="b412e-127">Contract Name</span></span>|`xs:string`|<span data-ttu-id="b412e-128">协定的名称。</span><span class="sxs-lookup"><span data-stu-id="b412e-128">The name of the contract.</span></span> <span data-ttu-id="b412e-129">示例：ICalculator。</span><span class="sxs-lookup"><span data-stu-id="b412e-129">Example: ICalculator.</span></span>|  
|<span data-ttu-id="b412e-130">目标</span><span class="sxs-lookup"><span data-stu-id="b412e-130">Destination</span></span>|`xs:string`|<span data-ttu-id="b412e-131">消息已发送到的服务终结点的地址。</span><span class="sxs-lookup"><span data-stu-id="b412e-131">The address of the service endpoint that the message was sent to.</span></span>|  
|<span data-ttu-id="b412e-132">HostReference</span><span class="sxs-lookup"><span data-stu-id="b412e-132">HostReference</span></span>|`xs:string`|<span data-ttu-id="b412e-133">对于 Web 承载的服务，此字段唯一标识 Web 层次结构中的服务。</span><span class="sxs-lookup"><span data-stu-id="b412e-133">For Web-hosted services, this field uniquely identifies the service in the Web hierarchy.</span></span> <span data-ttu-id="b412e-134">其格式定义为 "网站名称应用程序虚拟路径&#124;服务虚拟路径&#124;ServiceName"。</span><span class="sxs-lookup"><span data-stu-id="b412e-134">Its format is defined as 'Web Site Name Application Virtual Path&#124;Service Virtual Path&#124;ServiceName'.</span></span> <span data-ttu-id="b412e-135">示例： "Default Web Site//Calculatorapplication&#124;/CalculatorService.svc&#124;CalculatorService"。</span><span class="sxs-lookup"><span data-stu-id="b412e-135">Example: 'Default Web Site/CalculatorApplication&#124;/CalculatorService.svc&#124;CalculatorService'.</span></span>|  
|<span data-ttu-id="b412e-136">应用程序域</span><span class="sxs-lookup"><span data-stu-id="b412e-136">AppDomain</span></span>|`xs:string`|<span data-ttu-id="b412e-137">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="b412e-137">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
