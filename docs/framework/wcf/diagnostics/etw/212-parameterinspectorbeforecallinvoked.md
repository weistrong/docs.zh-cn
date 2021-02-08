---
description: 了解详细信息： 212-ParameterInspectorBeforeCallInvoked
title: 212 - ParameterInspectorBeforeCallInvoked
ms.date: 03/30/2017
ms.assetid: 063fc8d2-ceac-4c18-8368-de84f2c78035
ms.openlocfilehash: aa02ff22b533855716c212d312396e6de23ace42
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99794398"
---
# <a name="212---parameterinspectorbeforecallinvoked"></a><span data-ttu-id="87b4c-103">212 - ParameterInspectorBeforeCallInvoked</span><span class="sxs-lookup"><span data-stu-id="87b4c-103">212 - ParameterInspectorBeforeCallInvoked</span></span>

## <a name="properties"></a><span data-ttu-id="87b4c-104">属性</span><span class="sxs-lookup"><span data-stu-id="87b4c-104">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="87b4c-105">ID</span><span class="sxs-lookup"><span data-stu-id="87b4c-105">ID</span></span>|<span data-ttu-id="87b4c-106">212</span><span class="sxs-lookup"><span data-stu-id="87b4c-106">212</span></span>|  
|<span data-ttu-id="87b4c-107">关键字</span><span class="sxs-lookup"><span data-stu-id="87b4c-107">Keywords</span></span>|<span data-ttu-id="87b4c-108">疑难解答，ServiceModel</span><span class="sxs-lookup"><span data-stu-id="87b4c-108">Troubleshooting, ServiceModel</span></span>|  
|<span data-ttu-id="87b4c-109">级别</span><span class="sxs-lookup"><span data-stu-id="87b4c-109">Level</span></span>|<span data-ttu-id="87b4c-110">信息</span><span class="sxs-lookup"><span data-stu-id="87b4c-110">Information</span></span>|  
|<span data-ttu-id="87b4c-111">通道</span><span class="sxs-lookup"><span data-stu-id="87b4c-111">Channel</span></span>|<span data-ttu-id="87b4c-112">Microsoft-Windows-应用程序服务器-应用程序/分析</span><span class="sxs-lookup"><span data-stu-id="87b4c-112">Microsoft-Windows-Application Server-Applications/Analytic</span></span>|  
  
## <a name="description"></a><span data-ttu-id="87b4c-113">说明</span><span class="sxs-lookup"><span data-stu-id="87b4c-113">Description</span></span>  

 <span data-ttu-id="87b4c-114">服务模型对 `BeforeCall` 调用 `ParameterInspector` 方法之后，将发出此事件。</span><span class="sxs-lookup"><span data-stu-id="87b4c-114">This event is emitted after the Service Model has invoked the `BeforeCall` method on a `ParameterInspector`.</span></span>  
  
## <a name="message"></a><span data-ttu-id="87b4c-115">消息</span><span class="sxs-lookup"><span data-stu-id="87b4c-115">Message</span></span>  

 <span data-ttu-id="87b4c-116">调度程序对“%1”类型的 ParameterInspector 调用了“BeforeCall”。</span><span class="sxs-lookup"><span data-stu-id="87b4c-116">The Dispatcher invoked 'BeforeCall' on a ParameterInspector of type '%1'.</span></span>  
  
## <a name="details"></a><span data-ttu-id="87b4c-117">详细信息</span><span class="sxs-lookup"><span data-stu-id="87b4c-117">Details</span></span>  
  
|<span data-ttu-id="87b4c-118">数据项名称</span><span class="sxs-lookup"><span data-stu-id="87b4c-118">Data Item Name</span></span>|<span data-ttu-id="87b4c-119">数据项类型</span><span class="sxs-lookup"><span data-stu-id="87b4c-119">Data Item Type</span></span>|<span data-ttu-id="87b4c-120">说明</span><span class="sxs-lookup"><span data-stu-id="87b4c-120">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="87b4c-121">TypeName</span><span class="sxs-lookup"><span data-stu-id="87b4c-121">TypeName</span></span>|`xs:string`|<span data-ttu-id="87b4c-122">所调用检查器的类型的 CLR FullName。</span><span class="sxs-lookup"><span data-stu-id="87b4c-122">The CLR FullName of the invoked inspector's type.</span></span>|  
|<span data-ttu-id="87b4c-123">HostReference</span><span class="sxs-lookup"><span data-stu-id="87b4c-123">HostReference</span></span>|`xs:string`|<span data-ttu-id="87b4c-124">对于 Web 承载的服务，此字段唯一标识 Web 层次结构中的服务。</span><span class="sxs-lookup"><span data-stu-id="87b4c-124">For Web-hosted services, this field uniquely identifies the service in the Web hierarchy.</span></span> <span data-ttu-id="87b4c-125">其格式定义为 "网站名称应用程序虚拟路径&#124;服务虚拟路径&#124;ServiceName"。</span><span class="sxs-lookup"><span data-stu-id="87b4c-125">Its format is defined as 'Web Site Name Application Virtual Path&#124;Service Virtual Path&#124;ServiceName'.</span></span> <span data-ttu-id="87b4c-126">示例： "Default Web Site//Calculatorapplication&#124;/CalculatorService.svc&#124;CalculatorService"。</span><span class="sxs-lookup"><span data-stu-id="87b4c-126">Example: 'Default Web Site/CalculatorApplication&#124;/CalculatorService.svc&#124;CalculatorService'.</span></span>|  
|<span data-ttu-id="87b4c-127">应用程序域</span><span class="sxs-lookup"><span data-stu-id="87b4c-127">AppDomain</span></span>|`xs:string`|<span data-ttu-id="87b4c-128">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="87b4c-128">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
