---
description: 了解详细信息： 303-UserDefinedInformationEventOccured
title: 303 - UserDefinedInformationEventOccured
ms.date: 03/30/2017
ms.assetid: 5ed5acaf-3755-4417-92c4-4ebc8e854ca1
ms.openlocfilehash: 51c4acd5d10a2d563dd7fbcebf90b75c64ff20ad
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99794229"
---
# <a name="303---userdefinedinformationeventoccured"></a><span data-ttu-id="11175-103">303 - UserDefinedInformationEventOccured</span><span class="sxs-lookup"><span data-stu-id="11175-103">303 - UserDefinedInformationEventOccured</span></span>

## <a name="properties"></a><span data-ttu-id="11175-104">属性</span><span class="sxs-lookup"><span data-stu-id="11175-104">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="11175-105">ID</span><span class="sxs-lookup"><span data-stu-id="11175-105">ID</span></span>|<span data-ttu-id="11175-106">303</span><span class="sxs-lookup"><span data-stu-id="11175-106">303</span></span>|  
|<span data-ttu-id="11175-107">关键字</span><span class="sxs-lookup"><span data-stu-id="11175-107">Keywords</span></span>|<span data-ttu-id="11175-108">疑难解答，HealthMonitoring，UserEvents，ServiceModel，EndToEndMonitoring</span><span class="sxs-lookup"><span data-stu-id="11175-108">Troubleshooting, HealthMonitoring, UserEvents, ServiceModel, EndToEndMonitoring</span></span>|  
|<span data-ttu-id="11175-109">级别</span><span class="sxs-lookup"><span data-stu-id="11175-109">Level</span></span>|<span data-ttu-id="11175-110">信息</span><span class="sxs-lookup"><span data-stu-id="11175-110">Information</span></span>|  
|<span data-ttu-id="11175-111">通道</span><span class="sxs-lookup"><span data-stu-id="11175-111">Channel</span></span>|<span data-ttu-id="11175-112">Microsoft-Windows-应用程序服务器-应用程序/分析</span><span class="sxs-lookup"><span data-stu-id="11175-112">Microsoft-Windows-Application Server-Applications/Analytic</span></span>|  
  
## <a name="description"></a><span data-ttu-id="11175-113">说明</span><span class="sxs-lookup"><span data-stu-id="11175-113">Description</span></span>  

 <span data-ttu-id="11175-114">此事件从用户代码发出。</span><span class="sxs-lookup"><span data-stu-id="11175-114">This event is emitted from user code.</span></span> <span data-ttu-id="11175-115">当开发人员的服务中出现自定义的信息性事件时，开发人员可以发出此事件。</span><span class="sxs-lookup"><span data-stu-id="11175-115">Developers can emit this event when a custom-defined informational event occurs in their service.</span></span> <span data-ttu-id="11175-116">可以使用 <xref:System.Diagnostics.Eventing> API 完成此操作。</span><span class="sxs-lookup"><span data-stu-id="11175-116">This can be done using the <xref:System.Diagnostics.Eventing> APIs.</span></span> <span data-ttu-id="11175-117">此外，还提供了一个 WCF 示例，该示例包装 API 并演示如何正确发出此事件。</span><span class="sxs-lookup"><span data-stu-id="11175-117">Additionally, there is a WCF sample that wraps that API and demonstrates how to properly emit this event.</span></span>  
  
## <a name="message"></a><span data-ttu-id="11175-118">消息</span><span class="sxs-lookup"><span data-stu-id="11175-118">Message</span></span>  

 <span data-ttu-id="11175-119">Name“%1”、Reference“%2”、Payload: %3</span><span class="sxs-lookup"><span data-stu-id="11175-119">Name:'%1', Reference:'%2', Payload:%3</span></span>  
  
## <a name="details"></a><span data-ttu-id="11175-120">详细信息</span><span class="sxs-lookup"><span data-stu-id="11175-120">Details</span></span>  
  
|<span data-ttu-id="11175-121">数据项名称</span><span class="sxs-lookup"><span data-stu-id="11175-121">Data Item Name</span></span>|<span data-ttu-id="11175-122">数据项类型</span><span class="sxs-lookup"><span data-stu-id="11175-122">Data Item Type</span></span>|<span data-ttu-id="11175-123">说明</span><span class="sxs-lookup"><span data-stu-id="11175-123">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="11175-124">名称</span><span class="sxs-lookup"><span data-stu-id="11175-124">Name</span></span>|`xs:string`|<span data-ttu-id="11175-125">事件的用户定义名称</span><span class="sxs-lookup"><span data-stu-id="11175-125">The user-defined name of the event</span></span>|  
|<span data-ttu-id="11175-126">HostReference</span><span class="sxs-lookup"><span data-stu-id="11175-126">HostReference</span></span>|`xs:string`|<span data-ttu-id="11175-127">对于 Web 承载的服务，此字段唯一标识 Web 层次结构中的服务。</span><span class="sxs-lookup"><span data-stu-id="11175-127">For Web hosted services, this field uniquely identifies the service in the Web hierarchy.</span></span> <span data-ttu-id="11175-128">其格式定义为 "网站名称应用程序虚拟路径&#124;服务虚拟路径&#124;ServiceName"。</span><span class="sxs-lookup"><span data-stu-id="11175-128">Its format is defined as 'Web Site Name Application Virtual Path&#124;Service Virtual Path&#124;ServiceName'.</span></span> <span data-ttu-id="11175-129">示例： "Default Web Site//Calculatorapplication&#124;/CalculatorService.svc&#124;CalculatorService"。</span><span class="sxs-lookup"><span data-stu-id="11175-129">Example: 'Default Web Site/CalculatorApplication&#124;/CalculatorService.svc&#124;CalculatorService'.</span></span>|  
|<span data-ttu-id="11175-130">Payload</span><span class="sxs-lookup"><span data-stu-id="11175-130">Payload</span></span>|`xs:string`|<span data-ttu-id="11175-131">事件的用户定义负载。</span><span class="sxs-lookup"><span data-stu-id="11175-131">The user-defined payload of the event.</span></span>|
