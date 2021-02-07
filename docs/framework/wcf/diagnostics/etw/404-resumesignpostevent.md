---
description: 了解详细信息： 404-ResumeSignpostEvent
title: 404 - ResumeSignpostEvent
ms.date: 03/30/2017
ms.assetid: 395cc7ca-f35f-4295-be97-39a077f99c97
ms.openlocfilehash: f735df6133c9708c05b2319e7ea17d7795e901b1
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99760285"
---
# <a name="404---resumesignpostevent"></a><span data-ttu-id="f02f3-103">404 - ResumeSignpostEvent</span><span class="sxs-lookup"><span data-stu-id="f02f3-103">404 - ResumeSignpostEvent</span></span>

## <a name="properties"></a><span data-ttu-id="f02f3-104">属性</span><span class="sxs-lookup"><span data-stu-id="f02f3-104">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="f02f3-105">ID</span><span class="sxs-lookup"><span data-stu-id="f02f3-105">ID</span></span>|<span data-ttu-id="f02f3-106">404</span><span class="sxs-lookup"><span data-stu-id="f02f3-106">404</span></span>|  
|<span data-ttu-id="f02f3-107">关键字</span><span class="sxs-lookup"><span data-stu-id="f02f3-107">Keywords</span></span>|<span data-ttu-id="f02f3-108">疑难解答</span><span class="sxs-lookup"><span data-stu-id="f02f3-108">Troubleshooting</span></span>|  
|<span data-ttu-id="f02f3-109">级别</span><span class="sxs-lookup"><span data-stu-id="f02f3-109">Level</span></span>|<span data-ttu-id="f02f3-110">信息</span><span class="sxs-lookup"><span data-stu-id="f02f3-110">Information</span></span>|  
|<span data-ttu-id="f02f3-111">通道</span><span class="sxs-lookup"><span data-stu-id="f02f3-111">Channel</span></span>|<span data-ttu-id="f02f3-112">Microsoft-Windows-应用程序服务器-应用程序/分析</span><span class="sxs-lookup"><span data-stu-id="f02f3-112">Microsoft-Windows-Application Server-Applications/Analytic</span></span>|  
  
## <a name="description"></a><span data-ttu-id="f02f3-113">说明</span><span class="sxs-lookup"><span data-stu-id="f02f3-113">Description</span></span>  

 <span data-ttu-id="f02f3-114">此事件标记端对端活动的恢复，</span><span class="sxs-lookup"><span data-stu-id="f02f3-114">This event marks the resumption of an end-to-end activity.</span></span> <span data-ttu-id="f02f3-115">它包含活动的名称。</span><span class="sxs-lookup"><span data-stu-id="f02f3-115">It contains the name of the activity.</span></span>  
  
## <a name="message"></a><span data-ttu-id="f02f3-116">消息</span><span class="sxs-lookup"><span data-stu-id="f02f3-116">Message</span></span>  

 <span data-ttu-id="f02f3-117">活动边界。</span><span class="sxs-lookup"><span data-stu-id="f02f3-117">Activity boundary.</span></span>  
  
## <a name="details"></a><span data-ttu-id="f02f3-118">详细信息</span><span class="sxs-lookup"><span data-stu-id="f02f3-118">Details</span></span>  
  
|<span data-ttu-id="f02f3-119">数据项名称</span><span class="sxs-lookup"><span data-stu-id="f02f3-119">Data Item Name</span></span>|<span data-ttu-id="f02f3-120">数据项类型</span><span class="sxs-lookup"><span data-stu-id="f02f3-120">Data Item Type</span></span>|<span data-ttu-id="f02f3-121">说明</span><span class="sxs-lookup"><span data-stu-id="f02f3-121">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="f02f3-122">扩展数据</span><span class="sxs-lookup"><span data-stu-id="f02f3-122">Extended Data</span></span>|`xs:string`|<span data-ttu-id="f02f3-123">活动的名称。</span><span class="sxs-lookup"><span data-stu-id="f02f3-123">The name of the activity.</span></span>|  
|<span data-ttu-id="f02f3-124">应用程序域</span><span class="sxs-lookup"><span data-stu-id="f02f3-124">AppDomain</span></span>|`xs:string`|<span data-ttu-id="f02f3-125">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="f02f3-125">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
