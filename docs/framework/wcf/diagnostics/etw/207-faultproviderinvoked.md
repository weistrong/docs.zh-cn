---
description: 了解详细信息： 207-FaultProviderInvoked
title: 207 - FaultProviderInvoked
ms.date: 03/30/2017
ms.assetid: b730d903-01c2-4deb-85a4-da12f8a21fe4
ms.openlocfilehash: 03c4f1669fc61019ccf4d23d2994f136e231fbec
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99728062"
---
# <a name="207---faultproviderinvoked"></a><span data-ttu-id="9211d-103">207 - FaultProviderInvoked</span><span class="sxs-lookup"><span data-stu-id="9211d-103">207 - FaultProviderInvoked</span></span>

## <a name="properties"></a><span data-ttu-id="9211d-104">属性</span><span class="sxs-lookup"><span data-stu-id="9211d-104">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="9211d-105">ID</span><span class="sxs-lookup"><span data-stu-id="9211d-105">ID</span></span>|<span data-ttu-id="9211d-106">207</span><span class="sxs-lookup"><span data-stu-id="9211d-106">207</span></span>|  
|<span data-ttu-id="9211d-107">关键字</span><span class="sxs-lookup"><span data-stu-id="9211d-107">Keywords</span></span>|<span data-ttu-id="9211d-108">疑难解答，ServiceModel</span><span class="sxs-lookup"><span data-stu-id="9211d-108">Troubleshooting, ServiceModel</span></span>|  
|<span data-ttu-id="9211d-109">级别</span><span class="sxs-lookup"><span data-stu-id="9211d-109">Level</span></span>|<span data-ttu-id="9211d-110">信息</span><span class="sxs-lookup"><span data-stu-id="9211d-110">Information</span></span>|  
|<span data-ttu-id="9211d-111">通道</span><span class="sxs-lookup"><span data-stu-id="9211d-111">Channel</span></span>|<span data-ttu-id="9211d-112">Microsoft-Windows-应用程序服务器-应用程序/分析</span><span class="sxs-lookup"><span data-stu-id="9211d-112">Microsoft-Windows-Application Server-Applications/Analytic</span></span>|  
  
## <a name="description"></a><span data-ttu-id="9211d-113">说明</span><span class="sxs-lookup"><span data-stu-id="9211d-113">Description</span></span>  

 <span data-ttu-id="9211d-114">此事件在调用 `FaultProvider` 之后发出。</span><span class="sxs-lookup"><span data-stu-id="9211d-114">This event is emitted after a `FaultProvider` has been invoked.</span></span>  
  
## <a name="message"></a><span data-ttu-id="9211d-115">消息</span><span class="sxs-lookup"><span data-stu-id="9211d-115">Message</span></span>  

 <span data-ttu-id="9211d-116">调度程序调用了“%1”类型的 FaultProvider 来处理“%2”类型的异常。</span><span class="sxs-lookup"><span data-stu-id="9211d-116">The Dispatcher invoked a FaultProvider of type '%1' with an exception of type '%2'.</span></span>  
  
## <a name="details"></a><span data-ttu-id="9211d-117">详细信息</span><span class="sxs-lookup"><span data-stu-id="9211d-117">Details</span></span>  
  
|<span data-ttu-id="9211d-118">数据项名称</span><span class="sxs-lookup"><span data-stu-id="9211d-118">Data Item Name</span></span>|<span data-ttu-id="9211d-119">数据项类型</span><span class="sxs-lookup"><span data-stu-id="9211d-119">Data Item Type</span></span>|<span data-ttu-id="9211d-120">说明</span><span class="sxs-lookup"><span data-stu-id="9211d-120">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="9211d-121">TypeName</span><span class="sxs-lookup"><span data-stu-id="9211d-121">TypeName</span></span>|`xs:string`|<span data-ttu-id="9211d-122">所调用 `FaultProvider` 的类型的 CLR FullName。</span><span class="sxs-lookup"><span data-stu-id="9211d-122">The CLR FullName of the type of the invoked `FaultProvider`.</span></span>|  
|<span data-ttu-id="9211d-123">ExceptionTypeName</span><span class="sxs-lookup"><span data-stu-id="9211d-123">ExceptionTypeName</span></span>|`xs:string`|<span data-ttu-id="9211d-124">`FaultProvider` 处理的异常的 CLR FullName。</span><span class="sxs-lookup"><span data-stu-id="9211d-124">The CLR FullName of the exception that the `FaultProvider` has operated on.</span></span>|  
|<span data-ttu-id="9211d-125">HostReference</span><span class="sxs-lookup"><span data-stu-id="9211d-125">HostReference</span></span>|`xs:string`|<span data-ttu-id="9211d-126">对于 Web 承载的服务，此字段唯一标识 Web 层次结构中的服务。</span><span class="sxs-lookup"><span data-stu-id="9211d-126">For Web-hosted services, this field uniquely identifies the service in the Web hierarchy.</span></span> <span data-ttu-id="9211d-127">其格式定义为 "网站名称应用程序虚拟路径&#124;服务虚拟路径&#124;ServiceName"。</span><span class="sxs-lookup"><span data-stu-id="9211d-127">Its format is defined as 'Web Site Name Application Virtual Path&#124;Service Virtual Path&#124;ServiceName'.</span></span> <span data-ttu-id="9211d-128">示例： "Default Web Site//Calculatorapplication&#124;/CalculatorService.svc&#124;CalculatorService"。</span><span class="sxs-lookup"><span data-stu-id="9211d-128">Example: 'Default Web Site/CalculatorApplication&#124;/CalculatorService.svc&#124;CalculatorService'.</span></span>|  
|<span data-ttu-id="9211d-129">应用程序域</span><span class="sxs-lookup"><span data-stu-id="9211d-129">AppDomain</span></span>|`xs:string`|<span data-ttu-id="9211d-130">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="9211d-130">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
