---
description: 了解详细信息： 4212-LockRetryTimeout
title: 4212 - LockRetryTimeout
ms.date: 03/30/2017
ms.assetid: d4ad415a-9871-49fc-85b8-8ee2ea149b1d
ms.openlocfilehash: a2299d0d9643fb60ff420519fb43199e3f747c69
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99667078"
---
# <a name="4212---lockretrytimeout"></a><span data-ttu-id="59371-103">4212 - LockRetryTimeout</span><span class="sxs-lookup"><span data-stu-id="59371-103">4212 - LockRetryTimeout</span></span>

## <a name="properties"></a><span data-ttu-id="59371-104">属性</span><span class="sxs-lookup"><span data-stu-id="59371-104">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="59371-105">ID</span><span class="sxs-lookup"><span data-stu-id="59371-105">ID</span></span>|<span data-ttu-id="59371-106">4212</span><span class="sxs-lookup"><span data-stu-id="59371-106">4212</span></span>|  
|<span data-ttu-id="59371-107">关键字</span><span class="sxs-lookup"><span data-stu-id="59371-107">Keywords</span></span>|<span data-ttu-id="59371-108">WFInstanceStore</span><span class="sxs-lookup"><span data-stu-id="59371-108">WFInstanceStore</span></span>|  
|<span data-ttu-id="59371-109">级别</span><span class="sxs-lookup"><span data-stu-id="59371-109">Level</span></span>|<span data-ttu-id="59371-110">警告</span><span class="sxs-lookup"><span data-stu-id="59371-110">Warning</span></span>|  
|<span data-ttu-id="59371-111">通道</span><span class="sxs-lookup"><span data-stu-id="59371-111">Channel</span></span>|<span data-ttu-id="59371-112">Microsoft-Windows-应用程序服务器-应用程序/调试</span><span class="sxs-lookup"><span data-stu-id="59371-112">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="59371-113">说明</span><span class="sxs-lookup"><span data-stu-id="59371-113">Description</span></span>  

 <span data-ttu-id="59371-114">尝试获取实例锁时 SQL 提供程序遇到了超时。</span><span class="sxs-lookup"><span data-stu-id="59371-114">SQL provider encountered a timeout trying to acquire the instance lock.</span></span>  
  
## <a name="message"></a><span data-ttu-id="59371-115">消息</span><span class="sxs-lookup"><span data-stu-id="59371-115">Message</span></span>  

 <span data-ttu-id="59371-116">尝试获取实例锁时超时。</span><span class="sxs-lookup"><span data-stu-id="59371-116">Timeout trying to acquire the instance lock.</span></span>  <span data-ttu-id="59371-117">操作在分配的超时 %1 内没有完成。</span><span class="sxs-lookup"><span data-stu-id="59371-117">The operation did not complete within the allotted timeout of %1.</span></span> <span data-ttu-id="59371-118">分配给此操作的时间可能是更长超时的一部分。</span><span class="sxs-lookup"><span data-stu-id="59371-118">The time allotted to this operation may have been a portion of a longer timeout.</span></span>  
  
## <a name="details"></a><span data-ttu-id="59371-119">详细信息</span><span class="sxs-lookup"><span data-stu-id="59371-119">Details</span></span>  
  
|<span data-ttu-id="59371-120">数据项名称</span><span class="sxs-lookup"><span data-stu-id="59371-120">Data Item Name</span></span>|<span data-ttu-id="59371-121">数据项类型</span><span class="sxs-lookup"><span data-stu-id="59371-121">Data Item Type</span></span>|<span data-ttu-id="59371-122">说明</span><span class="sxs-lookup"><span data-stu-id="59371-122">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="59371-123">Delay</span><span class="sxs-lookup"><span data-stu-id="59371-123">Delay</span></span>|<span data-ttu-id="59371-124">xs:string</span><span class="sxs-lookup"><span data-stu-id="59371-124">xs:string</span></span>|<span data-ttu-id="59371-125">重试之间的延迟。</span><span class="sxs-lookup"><span data-stu-id="59371-125">The delay between retries.</span></span>|  
|<span data-ttu-id="59371-126">应用程序域</span><span class="sxs-lookup"><span data-stu-id="59371-126">AppDomain</span></span>|<span data-ttu-id="59371-127">xs:string</span><span class="sxs-lookup"><span data-stu-id="59371-127">xs:string</span></span>|<span data-ttu-id="59371-128">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="59371-128">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
