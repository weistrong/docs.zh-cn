---
description: 了解详细信息： 4203-RenewLockSystemError
title: 4203 - RenewLockSystemError
ms.date: 03/30/2017
ms.assetid: 6ec9ec6f-4ae2-45cf-b99b-02cdb9dc9ec9
ms.openlocfilehash: 0e62c501391fcaec56f2016631707832170775ed
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99792773"
---
# <a name="4203---renewlocksystemerror"></a><span data-ttu-id="f84d7-103">4203 - RenewLockSystemError</span><span class="sxs-lookup"><span data-stu-id="f84d7-103">4203 - RenewLockSystemError</span></span>

## <a name="properties"></a><span data-ttu-id="f84d7-104">属性</span><span class="sxs-lookup"><span data-stu-id="f84d7-104">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="f84d7-105">ID</span><span class="sxs-lookup"><span data-stu-id="f84d7-105">ID</span></span>|<span data-ttu-id="f84d7-106">4203</span><span class="sxs-lookup"><span data-stu-id="f84d7-106">4203</span></span>|  
|<span data-ttu-id="f84d7-107">关键字</span><span class="sxs-lookup"><span data-stu-id="f84d7-107">Keywords</span></span>|<span data-ttu-id="f84d7-108">WFInstanceStore</span><span class="sxs-lookup"><span data-stu-id="f84d7-108">WFInstanceStore</span></span>|  
|<span data-ttu-id="f84d7-109">级别</span><span class="sxs-lookup"><span data-stu-id="f84d7-109">Level</span></span>|<span data-ttu-id="f84d7-110">错误</span><span class="sxs-lookup"><span data-stu-id="f84d7-110">Error</span></span>|  
|<span data-ttu-id="f84d7-111">通道</span><span class="sxs-lookup"><span data-stu-id="f84d7-111">Channel</span></span>|<span data-ttu-id="f84d7-112">Microsoft-Windows-应用程序服务器-应用程序/调试</span><span class="sxs-lookup"><span data-stu-id="f84d7-112">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="f84d7-113">说明</span><span class="sxs-lookup"><span data-stu-id="f84d7-113">Description</span></span>  

 <span data-ttu-id="f84d7-114">指示 SQL 提供程序由于锁定到期日已过或者已删除锁定所有者，未能延长锁定到期日。</span><span class="sxs-lookup"><span data-stu-id="f84d7-114">Indicates SQL provider has failed to extend lock expiration due to either lock expiration already passed or the lock owner was deleted.</span></span> <span data-ttu-id="f84d7-115">SqlWorkflowInstanceStore 将被中止。</span><span class="sxs-lookup"><span data-stu-id="f84d7-115">The SqlWorkflowInstanceStore will be aborted.</span></span>  
  
## <a name="message"></a><span data-ttu-id="f84d7-116">消息</span><span class="sxs-lookup"><span data-stu-id="f84d7-116">Message</span></span>  

 <span data-ttu-id="f84d7-117">未能延长锁定到期日，锁定到期日已过，或者已删除锁定所有者。</span><span class="sxs-lookup"><span data-stu-id="f84d7-117">Failed to extend lock expiration, lock expiration already passed or the lock owner was deleted.</span></span> <span data-ttu-id="f84d7-118">正在中止 SqlWorkflowInstanceStore。</span><span class="sxs-lookup"><span data-stu-id="f84d7-118">Aborting SqlWorkflowInstanceStore.</span></span>  
  
## <a name="details"></a><span data-ttu-id="f84d7-119">详细信息</span><span class="sxs-lookup"><span data-stu-id="f84d7-119">Details</span></span>  
  
|<span data-ttu-id="f84d7-120">数据项名称</span><span class="sxs-lookup"><span data-stu-id="f84d7-120">Data Item Name</span></span>|<span data-ttu-id="f84d7-121">数据项类型</span><span class="sxs-lookup"><span data-stu-id="f84d7-121">Data Item Type</span></span>|<span data-ttu-id="f84d7-122">说明</span><span class="sxs-lookup"><span data-stu-id="f84d7-122">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="f84d7-123">应用程序域</span><span class="sxs-lookup"><span data-stu-id="f84d7-123">AppDomain</span></span>|<span data-ttu-id="f84d7-124">xs:string</span><span class="sxs-lookup"><span data-stu-id="f84d7-124">xs:string</span></span>|<span data-ttu-id="f84d7-125">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="f84d7-125">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
