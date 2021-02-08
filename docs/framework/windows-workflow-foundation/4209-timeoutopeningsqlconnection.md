---
description: 了解详细信息： 4209-TimeoutOpeningSqlConnection
title: 4209 - TimeoutOpeningSqlConnection
ms.date: 03/30/2017
ms.assetid: f0e56518-9758-41dc-a760-50d1a10fba6e
ms.openlocfilehash: 9c7540e328530fdc01b9f065dfb75b92c467bd43
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99787989"
---
# <a name="4209---timeoutopeningsqlconnection"></a><span data-ttu-id="f45a8-103">4209 - TimeoutOpeningSqlConnection</span><span class="sxs-lookup"><span data-stu-id="f45a8-103">4209 - TimeoutOpeningSqlConnection</span></span>

## <a name="properties"></a><span data-ttu-id="f45a8-104">属性</span><span class="sxs-lookup"><span data-stu-id="f45a8-104">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="f45a8-105">ID</span><span class="sxs-lookup"><span data-stu-id="f45a8-105">ID</span></span>|<span data-ttu-id="f45a8-106">4209</span><span class="sxs-lookup"><span data-stu-id="f45a8-106">4209</span></span>|  
|<span data-ttu-id="f45a8-107">关键字</span><span class="sxs-lookup"><span data-stu-id="f45a8-107">Keywords</span></span>|<span data-ttu-id="f45a8-108">WFInstanceStore</span><span class="sxs-lookup"><span data-stu-id="f45a8-108">WFInstanceStore</span></span>|  
|<span data-ttu-id="f45a8-109">级别</span><span class="sxs-lookup"><span data-stu-id="f45a8-109">Level</span></span>|<span data-ttu-id="f45a8-110">错误</span><span class="sxs-lookup"><span data-stu-id="f45a8-110">Error</span></span>|  
|<span data-ttu-id="f45a8-111">通道</span><span class="sxs-lookup"><span data-stu-id="f45a8-111">Channel</span></span>|<span data-ttu-id="f45a8-112">Microsoft-Windows-应用程序服务器-应用程序/调试</span><span class="sxs-lookup"><span data-stu-id="f45a8-112">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="f45a8-113">说明</span><span class="sxs-lookup"><span data-stu-id="f45a8-113">Description</span></span>  

 <span data-ttu-id="f45a8-114">指示在尝试打开 SQL 连接时遇到了超时。</span><span class="sxs-lookup"><span data-stu-id="f45a8-114">Indicates a timeout was encountered when trying to open a SQL connection.</span></span>  
  
## <a name="message"></a><span data-ttu-id="f45a8-115">消息</span><span class="sxs-lookup"><span data-stu-id="f45a8-115">Message</span></span>  

 <span data-ttu-id="f45a8-116">尝试打开 SQL 连接时超时。</span><span class="sxs-lookup"><span data-stu-id="f45a8-116">Timeout trying to open a SQL connection.</span></span> <span data-ttu-id="f45a8-117">操作在分配的超时 %1 内没有完成。</span><span class="sxs-lookup"><span data-stu-id="f45a8-117">The operation did not complete within the allotted timeout of %1.</span></span> <span data-ttu-id="f45a8-118">分配给此操作的时间可能是更长超时的一部分。</span><span class="sxs-lookup"><span data-stu-id="f45a8-118">The time allotted to this operation may have been a portion of a longer timeout.</span></span>  
  
## <a name="details"></a><span data-ttu-id="f45a8-119">详细信息</span><span class="sxs-lookup"><span data-stu-id="f45a8-119">Details</span></span>  
  
|<span data-ttu-id="f45a8-120">数据项名称</span><span class="sxs-lookup"><span data-stu-id="f45a8-120">Data Item Name</span></span>|<span data-ttu-id="f45a8-121">数据项类型</span><span class="sxs-lookup"><span data-stu-id="f45a8-121">Data Item Type</span></span>|<span data-ttu-id="f45a8-122">说明</span><span class="sxs-lookup"><span data-stu-id="f45a8-122">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="f45a8-123">超时</span><span class="sxs-lookup"><span data-stu-id="f45a8-123">Timeout</span></span>|<span data-ttu-id="f45a8-124">xs:string</span><span class="sxs-lookup"><span data-stu-id="f45a8-124">xs:string</span></span>|<span data-ttu-id="f45a8-125">用于打开 SQL 连接的超时值。</span><span class="sxs-lookup"><span data-stu-id="f45a8-125">The timeout value for opening the SQL connection.</span></span>|  
|<span data-ttu-id="f45a8-126">应用程序域</span><span class="sxs-lookup"><span data-stu-id="f45a8-126">AppDomain</span></span>|<span data-ttu-id="f45a8-127">xs:string</span><span class="sxs-lookup"><span data-stu-id="f45a8-127">xs:string</span></span>|<span data-ttu-id="f45a8-128">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="f45a8-128">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
