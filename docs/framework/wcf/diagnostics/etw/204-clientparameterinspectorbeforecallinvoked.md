---
description: 了解详细信息： 204-ClientParameterInspectorBeforeCallInvoked
title: 204 - ClientParameterInspectorBeforeCallInvoked
ms.date: 03/30/2017
ms.assetid: 8253555a-9002-4565-8ede-33d7a33a895f
ms.openlocfilehash: fa5646da7c48f624dc40f4fcc54a890c0758b4ba
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99644991"
---
# <a name="204---clientparameterinspectorbeforecallinvoked"></a><span data-ttu-id="477a9-103">204 - ClientParameterInspectorBeforeCallInvoked</span><span class="sxs-lookup"><span data-stu-id="477a9-103">204 - ClientParameterInspectorBeforeCallInvoked</span></span>

## <a name="properties"></a><span data-ttu-id="477a9-104">属性</span><span class="sxs-lookup"><span data-stu-id="477a9-104">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="477a9-105">ID</span><span class="sxs-lookup"><span data-stu-id="477a9-105">ID</span></span>|<span data-ttu-id="477a9-106">204</span><span class="sxs-lookup"><span data-stu-id="477a9-106">204</span></span>|  
|<span data-ttu-id="477a9-107">关键字</span><span class="sxs-lookup"><span data-stu-id="477a9-107">Keywords</span></span>|<span data-ttu-id="477a9-108">疑难解答，ServiceModel</span><span class="sxs-lookup"><span data-stu-id="477a9-108">Troubleshooting, ServiceModel</span></span>|  
|<span data-ttu-id="477a9-109">级别</span><span class="sxs-lookup"><span data-stu-id="477a9-109">Level</span></span>|<span data-ttu-id="477a9-110">信息</span><span class="sxs-lookup"><span data-stu-id="477a9-110">Information</span></span>|  
|<span data-ttu-id="477a9-111">通道</span><span class="sxs-lookup"><span data-stu-id="477a9-111">Channel</span></span>|<span data-ttu-id="477a9-112">Microsoft-Windows-应用程序服务器-应用程序/分析</span><span class="sxs-lookup"><span data-stu-id="477a9-112">Microsoft-Windows-Application Server-Applications/Analytic</span></span>|  
  
## <a name="description"></a><span data-ttu-id="477a9-113">说明</span><span class="sxs-lookup"><span data-stu-id="477a9-113">Description</span></span>  

 <span data-ttu-id="477a9-114">服务模型在客户端参数检查器上调用 `BeforeCall` 方法之后，将发出此事件。</span><span class="sxs-lookup"><span data-stu-id="477a9-114">This event is emitted after the Service Model has invoked the `BeforeCall` method on a client parameter inspector.</span></span>  
  
## <a name="message"></a><span data-ttu-id="477a9-115">消息</span><span class="sxs-lookup"><span data-stu-id="477a9-115">Message</span></span>  

 <span data-ttu-id="477a9-116">调度程序对“%1”类型的 ClientParameterInspector 调用了“BeforeCall”。</span><span class="sxs-lookup"><span data-stu-id="477a9-116">The Dispatcher invoked 'BeforeCall' on a ClientParameterInspector of type '%1'.</span></span>  
  
## <a name="details"></a><span data-ttu-id="477a9-117">详细信息</span><span class="sxs-lookup"><span data-stu-id="477a9-117">Details</span></span>  
  
|<span data-ttu-id="477a9-118">数据项名称</span><span class="sxs-lookup"><span data-stu-id="477a9-118">Data Item Name</span></span>|<span data-ttu-id="477a9-119">数据项类型</span><span class="sxs-lookup"><span data-stu-id="477a9-119">Data Item Type</span></span>|<span data-ttu-id="477a9-120">说明</span><span class="sxs-lookup"><span data-stu-id="477a9-120">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="477a9-121">TypeName</span><span class="sxs-lookup"><span data-stu-id="477a9-121">TypeName</span></span>|`xs:string`|<span data-ttu-id="477a9-122">所调用检查器的类型的 CLR FullName。</span><span class="sxs-lookup"><span data-stu-id="477a9-122">The CLR FullName of the invoked inspector's type.</span></span>|  
|<span data-ttu-id="477a9-123">HostReference</span><span class="sxs-lookup"><span data-stu-id="477a9-123">HostReference</span></span>|`xs:string`|<span data-ttu-id="477a9-124">对于 Web 承载的服务，此字段唯一标识 Web 层次结构中的服务。</span><span class="sxs-lookup"><span data-stu-id="477a9-124">For Web-hosted services, this field uniquely identifies the service in the Web hierarchy.</span></span> <span data-ttu-id="477a9-125">其格式定义为 "网站名称应用程序虚拟路径&#124;服务虚拟路径&#124;ServiceName"。</span><span class="sxs-lookup"><span data-stu-id="477a9-125">Its format is defined as 'Web Site Name Application Virtual Path&#124;Service Virtual Path&#124;ServiceName'.</span></span> <span data-ttu-id="477a9-126">示例： "Default Web Site//Calculatorapplication&#124;/CalculatorService.svc&#124;CalculatorService"。</span><span class="sxs-lookup"><span data-stu-id="477a9-126">Example: 'Default Web Site/CalculatorApplication&#124;/CalculatorService.svc&#124;CalculatorService'.</span></span>|  
|<span data-ttu-id="477a9-127">应用程序域</span><span class="sxs-lookup"><span data-stu-id="477a9-127">AppDomain</span></span>|`xs:string`|<span data-ttu-id="477a9-128">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="477a9-128">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
