---
description: 了解详细信息： 208-MessageInspectorAfterReceiveInvoked
title: 208 - MessageInspectorAfterReceiveInvoked
ms.date: 03/30/2017
ms.assetid: dfb5f7b0-4346-4949-8104-351726b1f502
ms.openlocfilehash: 29935f5dc8c5dd53c0bf427bfdc9b3858d7fb8fd
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99728049"
---
# <a name="208---messageinspectorafterreceiveinvoked"></a><span data-ttu-id="c9f0e-103">208 - MessageInspectorAfterReceiveInvoked</span><span class="sxs-lookup"><span data-stu-id="c9f0e-103">208 - MessageInspectorAfterReceiveInvoked</span></span>

## <a name="properties"></a><span data-ttu-id="c9f0e-104">属性</span><span class="sxs-lookup"><span data-stu-id="c9f0e-104">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="c9f0e-105">ID</span><span class="sxs-lookup"><span data-stu-id="c9f0e-105">ID</span></span>|<span data-ttu-id="c9f0e-106">208</span><span class="sxs-lookup"><span data-stu-id="c9f0e-106">208</span></span>|  
|<span data-ttu-id="c9f0e-107">关键字</span><span class="sxs-lookup"><span data-stu-id="c9f0e-107">Keywords</span></span>|<span data-ttu-id="c9f0e-108">疑难解答，ServiceModel</span><span class="sxs-lookup"><span data-stu-id="c9f0e-108">Troubleshooting, ServiceModel</span></span>|  
|<span data-ttu-id="c9f0e-109">级别</span><span class="sxs-lookup"><span data-stu-id="c9f0e-109">Level</span></span>|<span data-ttu-id="c9f0e-110">信息</span><span class="sxs-lookup"><span data-stu-id="c9f0e-110">Information</span></span>|  
|<span data-ttu-id="c9f0e-111">通道</span><span class="sxs-lookup"><span data-stu-id="c9f0e-111">Channel</span></span>|<span data-ttu-id="c9f0e-112">Microsoft-Windows-应用程序服务器-应用程序/分析</span><span class="sxs-lookup"><span data-stu-id="c9f0e-112">Microsoft-Windows-Application Server-Applications/Analytic</span></span>|  
  
## <a name="description"></a><span data-ttu-id="c9f0e-113">说明</span><span class="sxs-lookup"><span data-stu-id="c9f0e-113">Description</span></span>  

 <span data-ttu-id="c9f0e-114">服务模型对消息检查器调用 `AfterReceive` 方法之后，将发出此事件。</span><span class="sxs-lookup"><span data-stu-id="c9f0e-114">This event is emitted after the Service Model has invoked the `AfterReceive` method on a message inspector.</span></span>  
  
## <a name="message"></a><span data-ttu-id="c9f0e-115">消息</span><span class="sxs-lookup"><span data-stu-id="c9f0e-115">Message</span></span>  

 <span data-ttu-id="c9f0e-116">调度程序对“%1”类型的 MessageInspector 调用了“AfterReceiveReply”。</span><span class="sxs-lookup"><span data-stu-id="c9f0e-116">The Dispatcher invoked 'AfterReceiveReply' on a MessageInspector of type '%1'.</span></span>  
  
## <a name="details"></a><span data-ttu-id="c9f0e-117">详细信息</span><span class="sxs-lookup"><span data-stu-id="c9f0e-117">Details</span></span>  
  
|<span data-ttu-id="c9f0e-118">数据项名称</span><span class="sxs-lookup"><span data-stu-id="c9f0e-118">Data Item Name</span></span>|<span data-ttu-id="c9f0e-119">数据项类型</span><span class="sxs-lookup"><span data-stu-id="c9f0e-119">Data Item Type</span></span>|<span data-ttu-id="c9f0e-120">说明</span><span class="sxs-lookup"><span data-stu-id="c9f0e-120">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="c9f0e-121">TypeName</span><span class="sxs-lookup"><span data-stu-id="c9f0e-121">TypeName</span></span>|`xs:string`|<span data-ttu-id="c9f0e-122">所调用 `MessageInspector` 的类型的 CLR FullName。</span><span class="sxs-lookup"><span data-stu-id="c9f0e-122">The CLR FullName of the type of the invoked `MessageInspector`.</span></span>|  
|<span data-ttu-id="c9f0e-123">HostReference</span><span class="sxs-lookup"><span data-stu-id="c9f0e-123">HostReference</span></span>|`xs:string`|<span data-ttu-id="c9f0e-124">对于 Web 承载的服务，此字段唯一标识 Web 层次结构中的服务。</span><span class="sxs-lookup"><span data-stu-id="c9f0e-124">For Web-hosted services, this field uniquely identifies the service in the Web hierarchy.</span></span> <span data-ttu-id="c9f0e-125">其格式定义为 "网站名称应用程序虚拟路径&#124;服务虚拟路径&#124;ServiceName"。</span><span class="sxs-lookup"><span data-stu-id="c9f0e-125">Its format is defined as 'Web Site Name Application Virtual Path&#124;Service Virtual Path&#124;ServiceName'.</span></span> <span data-ttu-id="c9f0e-126">示例： "Default Web Site//Calculatorapplication&#124;/CalculatorService.svc&#124;CalculatorService"。</span><span class="sxs-lookup"><span data-stu-id="c9f0e-126">Example: 'Default Web Site/CalculatorApplication&#124;/CalculatorService.svc&#124;CalculatorService'.</span></span>|  
|<span data-ttu-id="c9f0e-127">应用程序域</span><span class="sxs-lookup"><span data-stu-id="c9f0e-127">AppDomain</span></span>|`xs:string`|<span data-ttu-id="c9f0e-128">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="c9f0e-128">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
