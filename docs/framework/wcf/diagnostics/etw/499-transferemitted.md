---
description: 了解详细信息： 499-TransferEmitted
title: 499 - TransferEmitted
ms.date: 03/30/2017
ms.assetid: 07a26434-a7a0-40fc-b5d0-3520a04328ae
ms.openlocfilehash: d9802ef718ce6091abe1d1092ad6bb7e7fff108a
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99783568"
---
# <a name="499---transferemitted"></a><span data-ttu-id="0b533-103">499 - TransferEmitted</span><span class="sxs-lookup"><span data-stu-id="0b533-103">499 - TransferEmitted</span></span>

## <a name="properties"></a><span data-ttu-id="0b533-104">属性</span><span class="sxs-lookup"><span data-stu-id="0b533-104">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="0b533-105">ID</span><span class="sxs-lookup"><span data-stu-id="0b533-105">ID</span></span>|<span data-ttu-id="0b533-106">499</span><span class="sxs-lookup"><span data-stu-id="0b533-106">499</span></span>|  
|<span data-ttu-id="0b533-107">关键字</span><span class="sxs-lookup"><span data-stu-id="0b533-107">Keywords</span></span>|<span data-ttu-id="0b533-108">疑难解答，UserEvents，EndToEndMonitoring，ServiceModel，WFTracking，ServiceHost，WCFMessageLogging</span><span class="sxs-lookup"><span data-stu-id="0b533-108">Troubleshooting, UserEvents, EndToEndMonitoring, ServiceModel, WFTracking, ServiceHost, WCFMessageLogging</span></span>|  
|<span data-ttu-id="0b533-109">级别</span><span class="sxs-lookup"><span data-stu-id="0b533-109">Level</span></span>|<span data-ttu-id="0b533-110">LogAlways</span><span class="sxs-lookup"><span data-stu-id="0b533-110">LogAlways</span></span>|  
|<span data-ttu-id="0b533-111">通道</span><span class="sxs-lookup"><span data-stu-id="0b533-111">Channel</span></span>|<span data-ttu-id="0b533-112">Microsoft-Windows-应用程序服务器-应用程序/分析</span><span class="sxs-lookup"><span data-stu-id="0b533-112">Microsoft-Windows-Application Server-Applications/Analytic</span></span>|  
  
## <a name="description"></a><span data-ttu-id="0b533-113">说明</span><span class="sxs-lookup"><span data-stu-id="0b533-113">Description</span></span>  

 <span data-ttu-id="0b533-114">此事件在发生传输事件时发出。</span><span class="sxs-lookup"><span data-stu-id="0b533-114">This event is emitted when the transfer event takes place.</span></span>  
  
## <a name="message"></a><span data-ttu-id="0b533-115">消息</span><span class="sxs-lookup"><span data-stu-id="0b533-115">Message</span></span>  

 <span data-ttu-id="0b533-116">发出了传输事件。</span><span class="sxs-lookup"><span data-stu-id="0b533-116">Transfer event emitted.</span></span>  
  
## <a name="details"></a><span data-ttu-id="0b533-117">详细信息</span><span class="sxs-lookup"><span data-stu-id="0b533-117">Details</span></span>  
  
|<span data-ttu-id="0b533-118">数据项名称</span><span class="sxs-lookup"><span data-stu-id="0b533-118">Data Item Name</span></span>|<span data-ttu-id="0b533-119">数据项类型</span><span class="sxs-lookup"><span data-stu-id="0b533-119">Data Item Type</span></span>|<span data-ttu-id="0b533-120">说明</span><span class="sxs-lookup"><span data-stu-id="0b533-120">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="0b533-121">HostReference</span><span class="sxs-lookup"><span data-stu-id="0b533-121">HostReference</span></span>|`xs:string`|<span data-ttu-id="0b533-122">对于 Web 承载的服务，此字段唯一标识 Web 层次结构中的服务。</span><span class="sxs-lookup"><span data-stu-id="0b533-122">For Web-hosted services, this field uniquely identifies the service in the Web hierarchy.</span></span> <span data-ttu-id="0b533-123">其格式定义为 "网站名称应用程序虚拟路径&#124;服务虚拟路径&#124;ServiceName"。</span><span class="sxs-lookup"><span data-stu-id="0b533-123">Its format is defined as 'Web Site Name Application Virtual Path&#124;Service Virtual Path&#124;ServiceName'.</span></span> <span data-ttu-id="0b533-124">示例： "Default Web Site//Calculatorapplication&#124;/CalculatorService.svc&#124;CalculatorService"。</span><span class="sxs-lookup"><span data-stu-id="0b533-124">Example: 'Default Web Site/CalculatorApplication&#124;/CalculatorService.svc&#124;CalculatorService'.</span></span>|  
|<span data-ttu-id="0b533-125">应用程序域</span><span class="sxs-lookup"><span data-stu-id="0b533-125">AppDomain</span></span>|`xs:string`|<span data-ttu-id="0b533-126">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="0b533-126">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
