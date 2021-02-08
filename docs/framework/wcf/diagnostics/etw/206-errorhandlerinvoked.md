---
description: 了解详细信息： 206-ErrorHandlerInvoked
title: 206 - ErrorHandlerInvoked
ms.date: 03/30/2017
ms.assetid: 97340f4d-4e09-4e42-a17a-982b3868dbcf
ms.openlocfilehash: addbcbdea25c7f8e7515b743e98e426476fa0b28
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99783776"
---
# <a name="206---errorhandlerinvoked"></a><span data-ttu-id="37356-103">206 - ErrorHandlerInvoked</span><span class="sxs-lookup"><span data-stu-id="37356-103">206 - ErrorHandlerInvoked</span></span>

## <a name="properties"></a><span data-ttu-id="37356-104">属性</span><span class="sxs-lookup"><span data-stu-id="37356-104">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="37356-105">ID</span><span class="sxs-lookup"><span data-stu-id="37356-105">ID</span></span>|<span data-ttu-id="37356-106">206</span><span class="sxs-lookup"><span data-stu-id="37356-106">206</span></span>|  
|<span data-ttu-id="37356-107">关键字</span><span class="sxs-lookup"><span data-stu-id="37356-107">Keywords</span></span>|<span data-ttu-id="37356-108">疑难解答，ServiceModel</span><span class="sxs-lookup"><span data-stu-id="37356-108">Troubleshooting, ServiceModel</span></span>|  
|<span data-ttu-id="37356-109">级别</span><span class="sxs-lookup"><span data-stu-id="37356-109">Level</span></span>|<span data-ttu-id="37356-110">信息</span><span class="sxs-lookup"><span data-stu-id="37356-110">Information</span></span>|  
|<span data-ttu-id="37356-111">通道</span><span class="sxs-lookup"><span data-stu-id="37356-111">Channel</span></span>|<span data-ttu-id="37356-112">Microsoft-Windows-应用程序服务器-应用程序/分析</span><span class="sxs-lookup"><span data-stu-id="37356-112">Microsoft-Windows-Application Server-Applications/Analytic</span></span>|  
  
## <a name="description"></a><span data-ttu-id="37356-113">说明</span><span class="sxs-lookup"><span data-stu-id="37356-113">Description</span></span>  

 <span data-ttu-id="37356-114">当 `ErrorHandler` 有机会处理在服务操作中发生的异常后，将发出此事件。</span><span class="sxs-lookup"><span data-stu-id="37356-114">This event is emitted after an `ErrorHandler` has had an opportunity to handle an exception that occurred in a service operation.</span></span>  
  
## <a name="message"></a><span data-ttu-id="37356-115">消息</span><span class="sxs-lookup"><span data-stu-id="37356-115">Message</span></span>  

 <span data-ttu-id="37356-116">调度程序调用了类型为 "%1" 且类型为 "%3" 的 ErrorHandler 的类型为 "%1" 的。</span><span class="sxs-lookup"><span data-stu-id="37356-116">The Dispatcher invoked an ErrorHandler of type '%1' with an exception of type '%3'.</span></span> <span data-ttu-id="37356-117">ErrorHandled 为“%2”。</span><span class="sxs-lookup"><span data-stu-id="37356-117">ErrorHandled == '%2'.</span></span>  
  
## <a name="details"></a><span data-ttu-id="37356-118">详细信息</span><span class="sxs-lookup"><span data-stu-id="37356-118">Details</span></span>  
  
|<span data-ttu-id="37356-119">数据项名称</span><span class="sxs-lookup"><span data-stu-id="37356-119">Data Item Name</span></span>|<span data-ttu-id="37356-120">数据项类型</span><span class="sxs-lookup"><span data-stu-id="37356-120">Data Item Type</span></span>|<span data-ttu-id="37356-121">说明</span><span class="sxs-lookup"><span data-stu-id="37356-121">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="37356-122">TypeName</span><span class="sxs-lookup"><span data-stu-id="37356-122">TypeName</span></span>|`xs:string`|<span data-ttu-id="37356-123">所调用 `ErrorHandler` 的类型的 CLR FullName。</span><span class="sxs-lookup"><span data-stu-id="37356-123">The CLR FullName of the type of the invoked `ErrorHandler`.</span></span>|  
|<span data-ttu-id="37356-124">已处理</span><span class="sxs-lookup"><span data-stu-id="37356-124">Handled</span></span>|`xs:unsignedByte`|<span data-ttu-id="37356-125">如果错误处理程序已处理错误，则为 `true`；否则为 `false`。</span><span class="sxs-lookup"><span data-stu-id="37356-125">`true` if the error handler handled the error, otherwise `false`.</span></span>|  
|<span data-ttu-id="37356-126">ExceptionTypeName</span><span class="sxs-lookup"><span data-stu-id="37356-126">ExceptionTypeName</span></span>|`xs:string`|<span data-ttu-id="37356-127">待处理异常的 CLR FullName。</span><span class="sxs-lookup"><span data-stu-id="37356-127">The CLR FullName of the exception that was being handled.</span></span>|  
|<span data-ttu-id="37356-128">HostReference</span><span class="sxs-lookup"><span data-stu-id="37356-128">HostReference</span></span>|`xs:string`|<span data-ttu-id="37356-129">对于 Web 承载的服务，此字段唯一标识 Web 层次结构中的服务。</span><span class="sxs-lookup"><span data-stu-id="37356-129">For Web-hosted services, this field uniquely identifies the service in the Web hierarchy.</span></span> <span data-ttu-id="37356-130">其格式定义为 "网站名称应用程序虚拟路径&#124;服务虚拟路径&#124;ServiceName"。</span><span class="sxs-lookup"><span data-stu-id="37356-130">Its format is defined as 'Web Site Name Application Virtual Path&#124;Service Virtual Path&#124;ServiceName'.</span></span> <span data-ttu-id="37356-131">示例： "Default Web Site//Calculatorapplication&#124;/CalculatorService.svc&#124;CalculatorService"。</span><span class="sxs-lookup"><span data-stu-id="37356-131">Example: 'Default Web Site/CalculatorApplication&#124;/CalculatorService.svc&#124;CalculatorService'.</span></span>|  
|<span data-ttu-id="37356-132">应用程序域</span><span class="sxs-lookup"><span data-stu-id="37356-132">AppDomain</span></span>|`xs:string`|<span data-ttu-id="37356-133">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="37356-133">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
