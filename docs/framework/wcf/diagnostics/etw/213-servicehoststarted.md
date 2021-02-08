---
description: 了解详细信息： 213-ServiceHostStarted
title: 213 - ServiceHostStarted
ms.date: 03/30/2017
ms.assetid: a6f7facc-342f-46bb-9d52-a470178ba6bb
ms.openlocfilehash: 5e2b5b7c633ef053c449ad62c4f8fee40798a386
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99794411"
---
# <a name="213---servicehoststarted"></a><span data-ttu-id="26d1f-103">213 - ServiceHostStarted</span><span class="sxs-lookup"><span data-stu-id="26d1f-103">213 - ServiceHostStarted</span></span>

## <a name="properties"></a><span data-ttu-id="26d1f-104">属性</span><span class="sxs-lookup"><span data-stu-id="26d1f-104">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="26d1f-105">ID</span><span class="sxs-lookup"><span data-stu-id="26d1f-105">ID</span></span>|<span data-ttu-id="26d1f-106">213</span><span class="sxs-lookup"><span data-stu-id="26d1f-106">213</span></span>|  
|<span data-ttu-id="26d1f-107">关键字</span><span class="sxs-lookup"><span data-stu-id="26d1f-107">Keywords</span></span>|<span data-ttu-id="26d1f-108">EndToEndMonitoring，HealthMonitoring，疑难解答，ServiceHost</span><span class="sxs-lookup"><span data-stu-id="26d1f-108">EndToEndMonitoring, HealthMonitoring, Troubleshooting, ServiceHost</span></span>|  
|<span data-ttu-id="26d1f-109">级别</span><span class="sxs-lookup"><span data-stu-id="26d1f-109">Level</span></span>|<span data-ttu-id="26d1f-110">LogAlways</span><span class="sxs-lookup"><span data-stu-id="26d1f-110">LogAlways</span></span>|  
|<span data-ttu-id="26d1f-111">通道</span><span class="sxs-lookup"><span data-stu-id="26d1f-111">Channel</span></span>|<span data-ttu-id="26d1f-112">Microsoft-Windows-应用程序服务器-应用程序/分析</span><span class="sxs-lookup"><span data-stu-id="26d1f-112">Microsoft-Windows-Application Server-Applications/Analytic</span></span>|  
  
## <a name="description"></a><span data-ttu-id="26d1f-113">说明</span><span class="sxs-lookup"><span data-stu-id="26d1f-113">Description</span></span>  

 <span data-ttu-id="26d1f-114">在启动 Web 承载的服务主机时发出此事件。</span><span class="sxs-lookup"><span data-stu-id="26d1f-114">This event is emitted when a Web-hosted service host is started.</span></span> <span data-ttu-id="26d1f-115">这通常在消息激活服务时发生。</span><span class="sxs-lookup"><span data-stu-id="26d1f-115">This typically happens when the service is activated by a message.</span></span> <span data-ttu-id="26d1f-116">如果将服务配置为自动启动，也可能发生此事件。</span><span class="sxs-lookup"><span data-stu-id="26d1f-116">It may also happen if the service is configured to be automatically started.</span></span>  
  
## <a name="message"></a><span data-ttu-id="26d1f-117">消息</span><span class="sxs-lookup"><span data-stu-id="26d1f-117">Message</span></span>  

 <span data-ttu-id="26d1f-118">ServiceHost 已启动:“%1”。</span><span class="sxs-lookup"><span data-stu-id="26d1f-118">ServiceHost started: '%1'.</span></span>  
  
## <a name="details"></a><span data-ttu-id="26d1f-119">详细信息</span><span class="sxs-lookup"><span data-stu-id="26d1f-119">Details</span></span>  
  
|<span data-ttu-id="26d1f-120">数据项名称</span><span class="sxs-lookup"><span data-stu-id="26d1f-120">Data Item Name</span></span>|<span data-ttu-id="26d1f-121">数据项类型</span><span class="sxs-lookup"><span data-stu-id="26d1f-121">Data Item Type</span></span>|<span data-ttu-id="26d1f-122">说明</span><span class="sxs-lookup"><span data-stu-id="26d1f-122">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="26d1f-123">服务类型名称</span><span class="sxs-lookup"><span data-stu-id="26d1f-123">Service Type Name</span></span>|`xs:string`|<span data-ttu-id="26d1f-124">服务实现的类型的 CLR FullName。</span><span class="sxs-lookup"><span data-stu-id="26d1f-124">The CLR FullName of the type of the service implementation.</span></span>|  
|<span data-ttu-id="26d1f-125">HostReference</span><span class="sxs-lookup"><span data-stu-id="26d1f-125">HostReference</span></span>|`xs:string`|<span data-ttu-id="26d1f-126">对于 Web 承载的服务，此字段唯一标识 Web 层次结构中的服务。</span><span class="sxs-lookup"><span data-stu-id="26d1f-126">For Web hosted services, this field uniquely identifies the service in the Web hierarchy.</span></span> <span data-ttu-id="26d1f-127">其格式定义为 "网站名称应用程序虚拟路径&#124;服务虚拟路径&#124;ServiceName"。</span><span class="sxs-lookup"><span data-stu-id="26d1f-127">Its format is defined as 'Web Site Name Application Virtual Path&#124;Service Virtual Path&#124;ServiceName'.</span></span> <span data-ttu-id="26d1f-128">示例： "Default Web Site//Calculatorapplication&#124;/CalculatorService.svc&#124;CalculatorService"。</span><span class="sxs-lookup"><span data-stu-id="26d1f-128">Example: 'Default Web Site/CalculatorApplication&#124;/CalculatorService.svc&#124;CalculatorService'.</span></span>|  
|<span data-ttu-id="26d1f-129">应用程序域</span><span class="sxs-lookup"><span data-stu-id="26d1f-129">AppDomain</span></span>|`xs:string`|<span data-ttu-id="26d1f-130">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="26d1f-130">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
