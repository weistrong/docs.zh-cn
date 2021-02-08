---
description: 了解详细信息： 401-StopSignPostEvent
title: 401- StopSignPostEvent
ms.date: 03/30/2017
ms.assetid: e033d03a-510d-4300-aa65-ef02cb4807f2
ms.openlocfilehash: 99b6151d902f3f8059b0aa01e6cda290debafda6
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99793943"
---
# <a name="401--stopsignpostevent"></a><span data-ttu-id="fbd08-103">401- StopSignPostEvent</span><span class="sxs-lookup"><span data-stu-id="fbd08-103">401- StopSignPostEvent</span></span>

## <a name="properties"></a><span data-ttu-id="fbd08-104">属性</span><span class="sxs-lookup"><span data-stu-id="fbd08-104">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="fbd08-105">ID</span><span class="sxs-lookup"><span data-stu-id="fbd08-105">ID</span></span>|<span data-ttu-id="fbd08-106">401</span><span class="sxs-lookup"><span data-stu-id="fbd08-106">401</span></span>|  
|<span data-ttu-id="fbd08-107">关键字</span><span class="sxs-lookup"><span data-stu-id="fbd08-107">Keywords</span></span>|<span data-ttu-id="fbd08-108">疑难解答</span><span class="sxs-lookup"><span data-stu-id="fbd08-108">Troubleshooting</span></span>|  
|<span data-ttu-id="fbd08-109">级别</span><span class="sxs-lookup"><span data-stu-id="fbd08-109">Level</span></span>|<span data-ttu-id="fbd08-110">信息</span><span class="sxs-lookup"><span data-stu-id="fbd08-110">Information</span></span>|  
|<span data-ttu-id="fbd08-111">通道</span><span class="sxs-lookup"><span data-stu-id="fbd08-111">Channel</span></span>|<span data-ttu-id="fbd08-112">Microsoft-Windows-应用程序服务器-应用程序/分析</span><span class="sxs-lookup"><span data-stu-id="fbd08-112">Microsoft-Windows-Application Server-Applications/Analytic</span></span>|  
  
## <a name="description"></a><span data-ttu-id="fbd08-113">说明</span><span class="sxs-lookup"><span data-stu-id="fbd08-113">Description</span></span>  

 <span data-ttu-id="fbd08-114">此事件标记端对端活动的结束，</span><span class="sxs-lookup"><span data-stu-id="fbd08-114">This event marks the end of an end-to-end activity.</span></span> <span data-ttu-id="fbd08-115">它包含活动的名称。</span><span class="sxs-lookup"><span data-stu-id="fbd08-115">It contains the name of the activity.</span></span>  
  
## <a name="message"></a><span data-ttu-id="fbd08-116">消息</span><span class="sxs-lookup"><span data-stu-id="fbd08-116">Message</span></span>  

 <span data-ttu-id="fbd08-117">活动边界。</span><span class="sxs-lookup"><span data-stu-id="fbd08-117">Activity boundary.</span></span>  
  
## <a name="details"></a><span data-ttu-id="fbd08-118">详细信息</span><span class="sxs-lookup"><span data-stu-id="fbd08-118">Details</span></span>  
  
|<span data-ttu-id="fbd08-119">数据项名称</span><span class="sxs-lookup"><span data-stu-id="fbd08-119">Data Item Name</span></span>|<span data-ttu-id="fbd08-120">数据项类型</span><span class="sxs-lookup"><span data-stu-id="fbd08-120">Data Item Type</span></span>|<span data-ttu-id="fbd08-121">说明</span><span class="sxs-lookup"><span data-stu-id="fbd08-121">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="fbd08-122">扩展数据</span><span class="sxs-lookup"><span data-stu-id="fbd08-122">Extended Data</span></span>|`xs:string`|<span data-ttu-id="fbd08-123">活动的名称。</span><span class="sxs-lookup"><span data-stu-id="fbd08-123">The name of the activity.</span></span>|  
|<span data-ttu-id="fbd08-124">应用程序域</span><span class="sxs-lookup"><span data-stu-id="fbd08-124">AppDomain</span></span>|`xs:string`|<span data-ttu-id="fbd08-125">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="fbd08-125">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
