---
description: 了解详细信息： 201-ClientMessageInspectorAfterReceiveInvoked
title: 201 - ClientMessageInspectorAfterReceiveInvoked
ms.date: 03/30/2017
ms.assetid: 9ff637f1-cc26-4400-ab9b-546f70e5057d
ms.openlocfilehash: 511f8bd039219d031c311f7def7b360b74df1a0a
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99645147"
---
# <a name="201---clientmessageinspectorafterreceiveinvoked"></a><span data-ttu-id="e9aae-103">201 - ClientMessageInspectorAfterReceiveInvoked</span><span class="sxs-lookup"><span data-stu-id="e9aae-103">201 - ClientMessageInspectorAfterReceiveInvoked</span></span>

## <a name="properties"></a><span data-ttu-id="e9aae-104">属性</span><span class="sxs-lookup"><span data-stu-id="e9aae-104">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="e9aae-105">ID</span><span class="sxs-lookup"><span data-stu-id="e9aae-105">ID</span></span>|<span data-ttu-id="e9aae-106">201</span><span class="sxs-lookup"><span data-stu-id="e9aae-106">201</span></span>|  
|<span data-ttu-id="e9aae-107">关键字</span><span class="sxs-lookup"><span data-stu-id="e9aae-107">Keywords</span></span>|<span data-ttu-id="e9aae-108">疑难解答，ServiceModel</span><span class="sxs-lookup"><span data-stu-id="e9aae-108">Troubleshooting, ServiceModel</span></span>|  
|<span data-ttu-id="e9aae-109">级别</span><span class="sxs-lookup"><span data-stu-id="e9aae-109">Level</span></span>|<span data-ttu-id="e9aae-110">信息</span><span class="sxs-lookup"><span data-stu-id="e9aae-110">Information</span></span>|  
|<span data-ttu-id="e9aae-111">通道</span><span class="sxs-lookup"><span data-stu-id="e9aae-111">Channel</span></span>|<span data-ttu-id="e9aae-112">Microsoft-Windows-应用程序服务器-应用程序/分析</span><span class="sxs-lookup"><span data-stu-id="e9aae-112">Microsoft-Windows-Application Server-Applications/Analytic</span></span>|  
  
## <a name="description"></a><span data-ttu-id="e9aae-113">说明</span><span class="sxs-lookup"><span data-stu-id="e9aae-113">Description</span></span>  

 <span data-ttu-id="e9aae-114">服务模型在客户端消息检查器上调用 `AfterReceiveReply` 方法之后，将发出此事件。</span><span class="sxs-lookup"><span data-stu-id="e9aae-114">This event is emitted after the Service Model has invoked the `AfterReceiveReply` method on a client message inspector.</span></span>  
  
## <a name="message"></a><span data-ttu-id="e9aae-115">消息</span><span class="sxs-lookup"><span data-stu-id="e9aae-115">Message</span></span>  

 <span data-ttu-id="e9aae-116">调度程序对“%1”类型的 ClientMessageInspector 调用了“AfterReceiveReply”。</span><span class="sxs-lookup"><span data-stu-id="e9aae-116">The Dispatcher invoked 'AfterReceiveReply' on a ClientMessageInspector of type '%1'.</span></span>  
  
## <a name="details"></a><span data-ttu-id="e9aae-117">详细信息</span><span class="sxs-lookup"><span data-stu-id="e9aae-117">Details</span></span>  
  
|<span data-ttu-id="e9aae-118">数据项名称</span><span class="sxs-lookup"><span data-stu-id="e9aae-118">Data Item Name</span></span>|<span data-ttu-id="e9aae-119">数据项类型</span><span class="sxs-lookup"><span data-stu-id="e9aae-119">Data Item Type</span></span>|<span data-ttu-id="e9aae-120">说明</span><span class="sxs-lookup"><span data-stu-id="e9aae-120">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="e9aae-121">TypeName</span><span class="sxs-lookup"><span data-stu-id="e9aae-121">TypeName</span></span>|`xs:string`|<span data-ttu-id="e9aae-122">所调用检查器的类型的 CLR FullName。</span><span class="sxs-lookup"><span data-stu-id="e9aae-122">The CLR FullName of the invoked inspector's type.</span></span>|  
|<span data-ttu-id="e9aae-123">HostReference</span><span class="sxs-lookup"><span data-stu-id="e9aae-123">HostReference</span></span>|`xs:string`|<span data-ttu-id="e9aae-124">对于 Web 承载的服务，此字段唯一标识 Web 层次结构中的服务。</span><span class="sxs-lookup"><span data-stu-id="e9aae-124">For Web-hosted services, this field uniquely identifies the service in the Web hierarchy.</span></span> <span data-ttu-id="e9aae-125">其格式定义为 "网站名称应用程序虚拟路径&#124;服务虚拟路径&#124;ServiceName"。</span><span class="sxs-lookup"><span data-stu-id="e9aae-125">Its format is defined as 'Web Site Name Application Virtual Path&#124;Service Virtual Path&#124;ServiceName'.</span></span> <span data-ttu-id="e9aae-126">示例： "Default Web Site//Calculatorapplication&#124;/CalculatorService.svc&#124;CalculatorService"。</span><span class="sxs-lookup"><span data-stu-id="e9aae-126">Example: 'Default Web Site/CalculatorApplication&#124;/CalculatorService.svc&#124;CalculatorService'.</span></span>|  
|<span data-ttu-id="e9aae-127">应用程序域</span><span class="sxs-lookup"><span data-stu-id="e9aae-127">AppDomain</span></span>|`xs:string`|<span data-ttu-id="e9aae-128">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="e9aae-128">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
