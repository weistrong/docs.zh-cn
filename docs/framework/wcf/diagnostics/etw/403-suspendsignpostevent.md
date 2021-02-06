---
description: 了解详细信息： 403-SuspendSignpostEvent
title: 403 - SuspendSignpostEvent
ms.date: 03/30/2017
ms.assetid: fb2e6f29-e556-47b4-b4c1-acd6b8879702
ms.openlocfilehash: 4e601920c94ed99c25a1c969508798f65f5348bc
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99656418"
---
# <a name="403---suspendsignpostevent"></a><span data-ttu-id="13602-103">403 - SuspendSignpostEvent</span><span class="sxs-lookup"><span data-stu-id="13602-103">403 - SuspendSignpostEvent</span></span>

## <a name="properties"></a><span data-ttu-id="13602-104">属性</span><span class="sxs-lookup"><span data-stu-id="13602-104">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="13602-105">ID</span><span class="sxs-lookup"><span data-stu-id="13602-105">ID</span></span>|<span data-ttu-id="13602-106">403</span><span class="sxs-lookup"><span data-stu-id="13602-106">403</span></span>|  
|<span data-ttu-id="13602-107">关键字</span><span class="sxs-lookup"><span data-stu-id="13602-107">Keywords</span></span>|<span data-ttu-id="13602-108">疑难解答</span><span class="sxs-lookup"><span data-stu-id="13602-108">Troubleshooting</span></span>|  
|<span data-ttu-id="13602-109">级别</span><span class="sxs-lookup"><span data-stu-id="13602-109">Level</span></span>|<span data-ttu-id="13602-110">信息</span><span class="sxs-lookup"><span data-stu-id="13602-110">Information</span></span>|  
|<span data-ttu-id="13602-111">通道</span><span class="sxs-lookup"><span data-stu-id="13602-111">Channel</span></span>|<span data-ttu-id="13602-112">Microsoft-Windows-应用程序服务器-应用程序/分析</span><span class="sxs-lookup"><span data-stu-id="13602-112">Microsoft-Windows-Application Server-Applications/Analytic</span></span>|  
  
## <a name="description"></a><span data-ttu-id="13602-113">说明</span><span class="sxs-lookup"><span data-stu-id="13602-113">Description</span></span>  

 <span data-ttu-id="13602-114">此事件标记端对端活动的挂起，</span><span class="sxs-lookup"><span data-stu-id="13602-114">This event marks the suspension of an end-to-end activity.</span></span> <span data-ttu-id="13602-115">它包含活动的名称。</span><span class="sxs-lookup"><span data-stu-id="13602-115">It contains the name of the activity.</span></span>  
  
## <a name="message"></a><span data-ttu-id="13602-116">消息</span><span class="sxs-lookup"><span data-stu-id="13602-116">Message</span></span>  

 <span data-ttu-id="13602-117">活动边界。</span><span class="sxs-lookup"><span data-stu-id="13602-117">Activity boundary.</span></span>  
  
## <a name="details"></a><span data-ttu-id="13602-118">详细信息</span><span class="sxs-lookup"><span data-stu-id="13602-118">Details</span></span>  
  
|<span data-ttu-id="13602-119">数据项名称</span><span class="sxs-lookup"><span data-stu-id="13602-119">Data Item Name</span></span>|<span data-ttu-id="13602-120">数据项类型</span><span class="sxs-lookup"><span data-stu-id="13602-120">Data Item Type</span></span>|<span data-ttu-id="13602-121">说明</span><span class="sxs-lookup"><span data-stu-id="13602-121">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="13602-122">扩展数据</span><span class="sxs-lookup"><span data-stu-id="13602-122">Extended Data</span></span>|`xs:string`|<span data-ttu-id="13602-123">活动的名称。</span><span class="sxs-lookup"><span data-stu-id="13602-123">The name of the activity.</span></span>|  
|<span data-ttu-id="13602-124">应用程序域</span><span class="sxs-lookup"><span data-stu-id="13602-124">AppDomain</span></span>|`xs:string`|<span data-ttu-id="13602-125">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="13602-125">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
