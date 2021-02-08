---
description: 了解详细信息： 211-ParameterInspectorAfterCallInvoked
title: 211 - ParameterInspectorAfterCallInvoked
ms.date: 03/30/2017
ms.assetid: c0e21297-10b8-4456-a0e1-e019145cd5ac
ms.openlocfilehash: 6168528fb001b5669e80595c8327dc57651e815e
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99794424"
---
# <a name="211---parameterinspectoraftercallinvoked"></a><span data-ttu-id="145ad-103">211 - ParameterInspectorAfterCallInvoked</span><span class="sxs-lookup"><span data-stu-id="145ad-103">211 - ParameterInspectorAfterCallInvoked</span></span>

## <a name="properties"></a><span data-ttu-id="145ad-104">属性</span><span class="sxs-lookup"><span data-stu-id="145ad-104">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="145ad-105">ID</span><span class="sxs-lookup"><span data-stu-id="145ad-105">ID</span></span>|<span data-ttu-id="145ad-106">211</span><span class="sxs-lookup"><span data-stu-id="145ad-106">211</span></span>|  
|<span data-ttu-id="145ad-107">关键字</span><span class="sxs-lookup"><span data-stu-id="145ad-107">Keywords</span></span>|<span data-ttu-id="145ad-108">疑难解答，ServiceModel</span><span class="sxs-lookup"><span data-stu-id="145ad-108">Troubleshooting, ServiceModel</span></span>|  
|<span data-ttu-id="145ad-109">级别</span><span class="sxs-lookup"><span data-stu-id="145ad-109">Level</span></span>|<span data-ttu-id="145ad-110">信息</span><span class="sxs-lookup"><span data-stu-id="145ad-110">Information</span></span>|  
|<span data-ttu-id="145ad-111">通道</span><span class="sxs-lookup"><span data-stu-id="145ad-111">Channel</span></span>|<span data-ttu-id="145ad-112">Microsoft-Windows-应用程序服务器-应用程序/分析</span><span class="sxs-lookup"><span data-stu-id="145ad-112">Microsoft-Windows-Application Server-Applications/Analytic</span></span>|  
  
## <a name="description"></a><span data-ttu-id="145ad-113">说明</span><span class="sxs-lookup"><span data-stu-id="145ad-113">Description</span></span>  

 <span data-ttu-id="145ad-114">服务模型对 `AfterCall` 调用 `ParameterInspector` 方法之后，将发出此事件。</span><span class="sxs-lookup"><span data-stu-id="145ad-114">This event is emitted after the Service Model has invoked the `AfterCall` method on a `ParameterInspector`.</span></span>  
  
## <a name="message"></a><span data-ttu-id="145ad-115">消息</span><span class="sxs-lookup"><span data-stu-id="145ad-115">Message</span></span>  

 <span data-ttu-id="145ad-116">调度程序对“%1”类型的 ParameterInspector 调用了“AfterCall”。</span><span class="sxs-lookup"><span data-stu-id="145ad-116">The Dispatcher invoked 'AfterCall' on a ParameterInspector of type '%1'.</span></span>  
  
## <a name="details"></a><span data-ttu-id="145ad-117">详细信息</span><span class="sxs-lookup"><span data-stu-id="145ad-117">Details</span></span>  
  
|<span data-ttu-id="145ad-118">数据项名称</span><span class="sxs-lookup"><span data-stu-id="145ad-118">Data Item Name</span></span>|<span data-ttu-id="145ad-119">数据项类型</span><span class="sxs-lookup"><span data-stu-id="145ad-119">Data Item Type</span></span>|<span data-ttu-id="145ad-120">说明</span><span class="sxs-lookup"><span data-stu-id="145ad-120">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="145ad-121">类型名称</span><span class="sxs-lookup"><span data-stu-id="145ad-121">Type Name</span></span>|`xs:string`|<span data-ttu-id="145ad-122">所调用 `ParameterInspector` 的类型的 CLR FullName。</span><span class="sxs-lookup"><span data-stu-id="145ad-122">The CLR FullName of the type of the invoked `ParameterInspector`.</span></span>|  
|<span data-ttu-id="145ad-123">HostReference</span><span class="sxs-lookup"><span data-stu-id="145ad-123">HostReference</span></span>|`xs:string`|<span data-ttu-id="145ad-124">对于 Web 承载的服务，此字段唯一标识 Web 层次结构中的服务。</span><span class="sxs-lookup"><span data-stu-id="145ad-124">For Web-hosted services, this field uniquely identifies the service in the Web hierarchy.</span></span> <span data-ttu-id="145ad-125">其格式定义为 "网站名称应用程序虚拟路径&#124;服务虚拟路径&#124;ServiceName"。</span><span class="sxs-lookup"><span data-stu-id="145ad-125">Its format is defined as 'Web Site Name Application Virtual Path&#124;Service Virtual Path&#124;ServiceName'.</span></span> <span data-ttu-id="145ad-126">示例： "Default Web Site//Calculatorapplication&#124;/CalculatorService.svc&#124;CalculatorService"。</span><span class="sxs-lookup"><span data-stu-id="145ad-126">Example: 'Default Web Site/CalculatorApplication&#124;/CalculatorService.svc&#124;CalculatorService'.</span></span>|  
|<span data-ttu-id="145ad-127">应用程序域</span><span class="sxs-lookup"><span data-stu-id="145ad-127">AppDomain</span></span>|`xs:string`|<span data-ttu-id="145ad-128">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="145ad-128">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
