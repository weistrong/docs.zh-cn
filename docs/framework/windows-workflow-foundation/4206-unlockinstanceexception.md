---
description: 了解详细信息： 4206-UnlockInstanceException
title: 4206 - UnlockInstanceException
ms.date: 03/30/2017
ms.assetid: 5a46dc5f-d517-4135-8905-25a42f01206b
ms.openlocfilehash: 7c281b7471869fc2361b1c7fb158559e4c9fae65
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99676269"
---
# <a name="4206---unlockinstanceexception"></a><span data-ttu-id="3bd3b-103">4206 - UnlockInstanceException</span><span class="sxs-lookup"><span data-stu-id="3bd3b-103">4206 - UnlockInstanceException</span></span>

## <a name="properties"></a><span data-ttu-id="3bd3b-104">属性</span><span class="sxs-lookup"><span data-stu-id="3bd3b-104">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="3bd3b-105">ID</span><span class="sxs-lookup"><span data-stu-id="3bd3b-105">ID</span></span>|<span data-ttu-id="3bd3b-106">4206</span><span class="sxs-lookup"><span data-stu-id="3bd3b-106">4206</span></span>|  
|<span data-ttu-id="3bd3b-107">关键字</span><span class="sxs-lookup"><span data-stu-id="3bd3b-107">Keywords</span></span>|<span data-ttu-id="3bd3b-108">WFInstanceStore</span><span class="sxs-lookup"><span data-stu-id="3bd3b-108">WFInstanceStore</span></span>|  
|<span data-ttu-id="3bd3b-109">级别</span><span class="sxs-lookup"><span data-stu-id="3bd3b-109">Level</span></span>|<span data-ttu-id="3bd3b-110">错误</span><span class="sxs-lookup"><span data-stu-id="3bd3b-110">Error</span></span>|  
|<span data-ttu-id="3bd3b-111">通道</span><span class="sxs-lookup"><span data-stu-id="3bd3b-111">Channel</span></span>|<span data-ttu-id="3bd3b-112">Microsoft-Windows-应用程序服务器-应用程序/调试</span><span class="sxs-lookup"><span data-stu-id="3bd3b-112">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="3bd3b-113">说明</span><span class="sxs-lookup"><span data-stu-id="3bd3b-113">Description</span></span>  

 <span data-ttu-id="3bd3b-114">指示在尝试解锁某一实例时遇到了异常。</span><span class="sxs-lookup"><span data-stu-id="3bd3b-114">Indicates an exception was encountered while trying to unlock an instance.</span></span>  
  
## <a name="message"></a><span data-ttu-id="3bd3b-115">消息</span><span class="sxs-lookup"><span data-stu-id="3bd3b-115">Message</span></span>  

 <span data-ttu-id="3bd3b-116">尝试解除实例锁定时遇到异常 %1。</span><span class="sxs-lookup"><span data-stu-id="3bd3b-116">Encountered exception %1 while attempting to unlock instance.</span></span>  
  
## <a name="details"></a><span data-ttu-id="3bd3b-117">详细信息</span><span class="sxs-lookup"><span data-stu-id="3bd3b-117">Details</span></span>  
  
|<span data-ttu-id="3bd3b-118">数据项名称</span><span class="sxs-lookup"><span data-stu-id="3bd3b-118">Data Item Name</span></span>|<span data-ttu-id="3bd3b-119">数据项类型</span><span class="sxs-lookup"><span data-stu-id="3bd3b-119">Data Item Type</span></span>|<span data-ttu-id="3bd3b-120">说明</span><span class="sxs-lookup"><span data-stu-id="3bd3b-120">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="3bd3b-121">ExceptionMessage</span><span class="sxs-lookup"><span data-stu-id="3bd3b-121">ExceptionMessage</span></span>|<span data-ttu-id="3bd3b-122">xs:string</span><span class="sxs-lookup"><span data-stu-id="3bd3b-122">xs:string</span></span>|<span data-ttu-id="3bd3b-123">来自 SQL 异常的消息。</span><span class="sxs-lookup"><span data-stu-id="3bd3b-123">The message from the SQL exception.</span></span>|  
|<span data-ttu-id="3bd3b-124">应用程序域</span><span class="sxs-lookup"><span data-stu-id="3bd3b-124">AppDomain</span></span>|<span data-ttu-id="3bd3b-125">xs:string</span><span class="sxs-lookup"><span data-stu-id="3bd3b-125">xs:string</span></span>|<span data-ttu-id="3bd3b-126">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="3bd3b-126">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
