---
description: 了解详细信息： 4211-QueuingSqlRetry
title: 4211 - QueuingSqlRetry
ms.date: 03/30/2017
ms.assetid: df569f88-c86b-4503-840d-1399b67f4df7
ms.openlocfilehash: 674914ee105bb0a48f8c32efbd573c685d22d9f7
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99742701"
---
# <a name="4211---queuingsqlretry"></a><span data-ttu-id="0373a-103">4211 - QueuingSqlRetry</span><span class="sxs-lookup"><span data-stu-id="0373a-103">4211 - QueuingSqlRetry</span></span>

## <a name="properties"></a><span data-ttu-id="0373a-104">属性</span><span class="sxs-lookup"><span data-stu-id="0373a-104">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="0373a-105">ID</span><span class="sxs-lookup"><span data-stu-id="0373a-105">ID</span></span>|<span data-ttu-id="0373a-106">4211</span><span class="sxs-lookup"><span data-stu-id="0373a-106">4211</span></span>|  
|<span data-ttu-id="0373a-107">关键字</span><span class="sxs-lookup"><span data-stu-id="0373a-107">Keywords</span></span>|<span data-ttu-id="0373a-108">WFInstanceStore</span><span class="sxs-lookup"><span data-stu-id="0373a-108">WFInstanceStore</span></span>|  
|<span data-ttu-id="0373a-109">级别</span><span class="sxs-lookup"><span data-stu-id="0373a-109">Level</span></span>|<span data-ttu-id="0373a-110">警告</span><span class="sxs-lookup"><span data-stu-id="0373a-110">Warning</span></span>|  
|<span data-ttu-id="0373a-111">通道</span><span class="sxs-lookup"><span data-stu-id="0373a-111">Channel</span></span>|<span data-ttu-id="0373a-112">Microsoft-Windows-应用程序服务器-应用程序/调试</span><span class="sxs-lookup"><span data-stu-id="0373a-112">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="0373a-113">说明</span><span class="sxs-lookup"><span data-stu-id="0373a-113">Description</span></span>  

 <span data-ttu-id="0373a-114">指示将 SQL 重试排队。</span><span class="sxs-lookup"><span data-stu-id="0373a-114">Indicates queuing SQL retry.</span></span>  
  
## <a name="message"></a><span data-ttu-id="0373a-115">消息</span><span class="sxs-lookup"><span data-stu-id="0373a-115">Message</span></span>  

 <span data-ttu-id="0373a-116">正在将 SQL 重试排队，延迟 %1 毫秒。</span><span class="sxs-lookup"><span data-stu-id="0373a-116">Queuing SQL retry with delay %1 milliseconds.</span></span>  
  
## <a name="details"></a><span data-ttu-id="0373a-117">详细信息</span><span class="sxs-lookup"><span data-stu-id="0373a-117">Details</span></span>  
  
|<span data-ttu-id="0373a-118">数据项名称</span><span class="sxs-lookup"><span data-stu-id="0373a-118">Data Item Name</span></span>|<span data-ttu-id="0373a-119">数据项类型</span><span class="sxs-lookup"><span data-stu-id="0373a-119">Data Item Type</span></span>|<span data-ttu-id="0373a-120">说明</span><span class="sxs-lookup"><span data-stu-id="0373a-120">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="0373a-121">Delay</span><span class="sxs-lookup"><span data-stu-id="0373a-121">Delay</span></span>|<span data-ttu-id="0373a-122">xs:string</span><span class="sxs-lookup"><span data-stu-id="0373a-122">xs:string</span></span>|<span data-ttu-id="0373a-123">重试之间的延迟。</span><span class="sxs-lookup"><span data-stu-id="0373a-123">The delay between retries.</span></span>|  
|<span data-ttu-id="0373a-124">应用程序域</span><span class="sxs-lookup"><span data-stu-id="0373a-124">AppDomain</span></span>|<span data-ttu-id="0373a-125">xs:string</span><span class="sxs-lookup"><span data-stu-id="0373a-125">xs:string</span></span>|<span data-ttu-id="0373a-126">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="0373a-126">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
