---
description: 了解详细信息： 219-ServiceException
title: 219 - ServiceException
ms.date: 03/30/2017
ms.assetid: 81e2efac-39aa-4ed2-85a9-97eb8793b844
ms.openlocfilehash: b2ac12d6c5c68517b085b39dd7d0f81c39db9ebd
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99794320"
---
# <a name="219---serviceexception"></a><span data-ttu-id="70479-103">219 - ServiceException</span><span class="sxs-lookup"><span data-stu-id="70479-103">219 - ServiceException</span></span>

## <a name="properties"></a><span data-ttu-id="70479-104">属性</span><span class="sxs-lookup"><span data-stu-id="70479-104">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="70479-105">ID</span><span class="sxs-lookup"><span data-stu-id="70479-105">ID</span></span>|<span data-ttu-id="70479-106">219</span><span class="sxs-lookup"><span data-stu-id="70479-106">219</span></span>|  
|<span data-ttu-id="70479-107">关键字</span><span class="sxs-lookup"><span data-stu-id="70479-107">Keywords</span></span>|<span data-ttu-id="70479-108">EndToEndMonitoring、HealthMonitoring、疑难解答、ServiceModel</span><span class="sxs-lookup"><span data-stu-id="70479-108">EndToEndMonitoring, HealthMonitoring, Troubleshooting, ServiceModel</span></span>|  
|<span data-ttu-id="70479-109">级别</span><span class="sxs-lookup"><span data-stu-id="70479-109">Level</span></span>|<span data-ttu-id="70479-110">错误</span><span class="sxs-lookup"><span data-stu-id="70479-110">Error</span></span>|  
|<span data-ttu-id="70479-111">通道</span><span class="sxs-lookup"><span data-stu-id="70479-111">Channel</span></span>|<span data-ttu-id="70479-112">Microsoft-Windows-应用程序服务器-应用程序/分析</span><span class="sxs-lookup"><span data-stu-id="70479-112">Microsoft-Windows-Application Server-Applications/Analytic</span></span>|  
  
## <a name="description"></a><span data-ttu-id="70479-113">说明</span><span class="sxs-lookup"><span data-stu-id="70479-113">Description</span></span>  

 <span data-ttu-id="70479-114">当 WCF 服务遇到未经处理的异常时会发出此事件。</span><span class="sxs-lookup"><span data-stu-id="70479-114">This event is emitted when a WCF service encounters an unhandled exception.</span></span> <span data-ttu-id="70479-115">这包括在激活和消息处理期间以及在用户代码中出现的未经处理的异常。</span><span class="sxs-lookup"><span data-stu-id="70479-115">This includes unhandled exceptions during activation, during message processing, and in user code.</span></span>  
  
## <a name="message"></a><span data-ttu-id="70479-116">消息</span><span class="sxs-lookup"><span data-stu-id="70479-116">Message</span></span>  

 <span data-ttu-id="70479-117">消息处理过程中出现了“%2”类型的未经处理的异常。</span><span class="sxs-lookup"><span data-stu-id="70479-117">There was an unhandled exception of type '%2' during message processing.</span></span> <span data-ttu-id="70479-118">完整异常 ToString: %1。</span><span class="sxs-lookup"><span data-stu-id="70479-118">Full Exception ToString: %1.</span></span>  
  
## <a name="details"></a><span data-ttu-id="70479-119">详细信息</span><span class="sxs-lookup"><span data-stu-id="70479-119">Details</span></span>  
  
|<span data-ttu-id="70479-120">数据项名称</span><span class="sxs-lookup"><span data-stu-id="70479-120">Data Item Name</span></span>|<span data-ttu-id="70479-121">数据项类型</span><span class="sxs-lookup"><span data-stu-id="70479-121">Data Item Type</span></span>|<span data-ttu-id="70479-122">说明</span><span class="sxs-lookup"><span data-stu-id="70479-122">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="70479-123">ExceptionToString</span><span class="sxs-lookup"><span data-stu-id="70479-123">ExceptionToString</span></span>|`xs:string`|<span data-ttu-id="70479-124">对 CLR 异常调用 `ToString`() 的结果。</span><span class="sxs-lookup"><span data-stu-id="70479-124">The result of calling `ToString`() on the CLR exception.</span></span>|  
|<span data-ttu-id="70479-125">ExceptionTypeName</span><span class="sxs-lookup"><span data-stu-id="70479-125">ExceptionTypeName</span></span>|`xs:string`|<span data-ttu-id="70479-126">异常的类型的 CLR FullName。</span><span class="sxs-lookup"><span data-stu-id="70479-126">The CLR FullName of the exception's type.</span></span>|  
|<span data-ttu-id="70479-127">HostReference</span><span class="sxs-lookup"><span data-stu-id="70479-127">HostReference</span></span>|`xs:string`|<span data-ttu-id="70479-128">对于 Web 承载的服务，此字段唯一标识 Web 层次结构中的服务。</span><span class="sxs-lookup"><span data-stu-id="70479-128">For Web-hosted services, this field uniquely identifies the service in the Web hierarchy.</span></span> <span data-ttu-id="70479-129">其格式定义为 "网站名称应用程序虚拟路径&#124;服务虚拟路径&#124;ServiceName"。</span><span class="sxs-lookup"><span data-stu-id="70479-129">Its format is defined as 'Web Site Name Application Virtual Path&#124;Service Virtual Path&#124;ServiceName'.</span></span> <span data-ttu-id="70479-130">示例： "Default Web Site//Calculatorapplication&#124;/CalculatorService.svc&#124;CalculatorService"。</span><span class="sxs-lookup"><span data-stu-id="70479-130">Example: 'Default Web Site/CalculatorApplication&#124;/CalculatorService.svc&#124;CalculatorService'.</span></span>|  
|<span data-ttu-id="70479-131">应用程序域</span><span class="sxs-lookup"><span data-stu-id="70479-131">AppDomain</span></span>|`xs:string`|<span data-ttu-id="70479-132">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="70479-132">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
