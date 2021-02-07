---
description: 了解详细信息： 209-MessageInspectorBeforeSendInvoked
title: 209 - MessageInspectorBeforeSendInvoked
ms.date: 03/30/2017
ms.assetid: 7d710875-fb77-4463-978b-bc86d59d84cd
ms.openlocfilehash: 337ed7d4c62d41d72cb2b4710c9f98f863305aee
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99727997"
---
# <a name="209---messageinspectorbeforesendinvoked"></a><span data-ttu-id="3be2d-103">209 - MessageInspectorBeforeSendInvoked</span><span class="sxs-lookup"><span data-stu-id="3be2d-103">209 - MessageInspectorBeforeSendInvoked</span></span>

## <a name="properties"></a><span data-ttu-id="3be2d-104">属性</span><span class="sxs-lookup"><span data-stu-id="3be2d-104">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="3be2d-105">ID</span><span class="sxs-lookup"><span data-stu-id="3be2d-105">ID</span></span>|<span data-ttu-id="3be2d-106">209</span><span class="sxs-lookup"><span data-stu-id="3be2d-106">209</span></span>|  
|<span data-ttu-id="3be2d-107">关键字</span><span class="sxs-lookup"><span data-stu-id="3be2d-107">Keywords</span></span>|<span data-ttu-id="3be2d-108">疑难解答，ServiceModel</span><span class="sxs-lookup"><span data-stu-id="3be2d-108">Troubleshooting, ServiceModel</span></span>|  
|<span data-ttu-id="3be2d-109">级别</span><span class="sxs-lookup"><span data-stu-id="3be2d-109">Level</span></span>|<span data-ttu-id="3be2d-110">信息</span><span class="sxs-lookup"><span data-stu-id="3be2d-110">Information</span></span>|  
|<span data-ttu-id="3be2d-111">通道</span><span class="sxs-lookup"><span data-stu-id="3be2d-111">Channel</span></span>|<span data-ttu-id="3be2d-112">Microsoft-Windows-应用程序服务器-应用程序/分析</span><span class="sxs-lookup"><span data-stu-id="3be2d-112">Microsoft-Windows-Application Server-Applications/Analytic</span></span>|  
  
## <a name="description"></a><span data-ttu-id="3be2d-113">说明</span><span class="sxs-lookup"><span data-stu-id="3be2d-113">Description</span></span>  

 <span data-ttu-id="3be2d-114">服务模型对消息检查器调用 `BeforeSend` 方法之后，将发出此事件。</span><span class="sxs-lookup"><span data-stu-id="3be2d-114">This event is emitted after the Service Model has invoked the `BeforeSend` method on a message inspector.</span></span>  
  
## <a name="message"></a><span data-ttu-id="3be2d-115">消息</span><span class="sxs-lookup"><span data-stu-id="3be2d-115">Message</span></span>  

 <span data-ttu-id="3be2d-116">调度程序对“%1”类型的 MessageInspector 调用了“BeforeSendRequest”。</span><span class="sxs-lookup"><span data-stu-id="3be2d-116">The Dispatcher invoked 'BeforeSendRequest' on a MessageInspector of type '%1'.</span></span>  
  
## <a name="details"></a><span data-ttu-id="3be2d-117">详细信息</span><span class="sxs-lookup"><span data-stu-id="3be2d-117">Details</span></span>  
  
|<span data-ttu-id="3be2d-118">数据项名称</span><span class="sxs-lookup"><span data-stu-id="3be2d-118">Data Item Name</span></span>|<span data-ttu-id="3be2d-119">数据项类型</span><span class="sxs-lookup"><span data-stu-id="3be2d-119">Data Item Type</span></span>|<span data-ttu-id="3be2d-120">说明</span><span class="sxs-lookup"><span data-stu-id="3be2d-120">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="3be2d-121">TypeName</span><span class="sxs-lookup"><span data-stu-id="3be2d-121">TypeName</span></span>|`xs:string`|<span data-ttu-id="3be2d-122">所调用 `MessageInspector` 的类型的 CLR FullName。</span><span class="sxs-lookup"><span data-stu-id="3be2d-122">The CLR FullName of the type of the invoked `MessageInspector`.</span></span>|  
|<span data-ttu-id="3be2d-123">HostReference</span><span class="sxs-lookup"><span data-stu-id="3be2d-123">HostReference</span></span>|`xs:string`|<span data-ttu-id="3be2d-124">对于 Web 承载的服务，此字段唯一标识 Web 层次结构中的服务。</span><span class="sxs-lookup"><span data-stu-id="3be2d-124">For Web-hosted services, this field uniquely identifies the service in the Web hierarchy.</span></span> <span data-ttu-id="3be2d-125">其格式定义为 "网站名称应用程序虚拟路径&#124;服务虚拟路径&#124;ServiceName"。</span><span class="sxs-lookup"><span data-stu-id="3be2d-125">Its format is defined as 'Web Site Name Application Virtual Path&#124;Service Virtual Path&#124;ServiceName'.</span></span> <span data-ttu-id="3be2d-126">示例： "Default Web Site//Calculatorapplication&#124;/CalculatorService.svc&#124;CalculatorService"。</span><span class="sxs-lookup"><span data-stu-id="3be2d-126">Example: 'Default Web Site/CalculatorApplication&#124;/CalculatorService.svc&#124;CalculatorService'.</span></span>|  
|<span data-ttu-id="3be2d-127">应用程序域</span><span class="sxs-lookup"><span data-stu-id="3be2d-127">AppDomain</span></span>|`xs:string`|<span data-ttu-id="3be2d-128">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="3be2d-128">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
