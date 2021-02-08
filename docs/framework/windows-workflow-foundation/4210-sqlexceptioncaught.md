---
description: 了解详细信息： 4210-SqlExceptionCaught
title: 4210 - SqlExceptionCaught
ms.date: 03/30/2017
ms.assetid: f0ce8af3-eb4c-48c8-b3d9-dd2f94b5574b
ms.openlocfilehash: 58846d02b6d1e388e3aef2bff76f51cba4990f2f
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99777874"
---
# <a name="4210---sqlexceptioncaught"></a><span data-ttu-id="cabb4-103">4210 - SqlExceptionCaught</span><span class="sxs-lookup"><span data-stu-id="cabb4-103">4210 - SqlExceptionCaught</span></span>

## <a name="properties"></a><span data-ttu-id="cabb4-104">属性</span><span class="sxs-lookup"><span data-stu-id="cabb4-104">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="cabb4-105">ID</span><span class="sxs-lookup"><span data-stu-id="cabb4-105">ID</span></span>|<span data-ttu-id="cabb4-106">4210</span><span class="sxs-lookup"><span data-stu-id="cabb4-106">4210</span></span>|  
|<span data-ttu-id="cabb4-107">关键字</span><span class="sxs-lookup"><span data-stu-id="cabb4-107">Keywords</span></span>|<span data-ttu-id="cabb4-108">WFInstanceStore</span><span class="sxs-lookup"><span data-stu-id="cabb4-108">WFInstanceStore</span></span>|  
|<span data-ttu-id="cabb4-109">级别</span><span class="sxs-lookup"><span data-stu-id="cabb4-109">Level</span></span>|<span data-ttu-id="cabb4-110">警告</span><span class="sxs-lookup"><span data-stu-id="cabb4-110">Warning</span></span>|  
|<span data-ttu-id="cabb4-111">通道</span><span class="sxs-lookup"><span data-stu-id="cabb4-111">Channel</span></span>|<span data-ttu-id="cabb4-112">Microsoft-Windows-应用程序服务器-应用程序/调试</span><span class="sxs-lookup"><span data-stu-id="cabb4-112">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="cabb4-113">说明</span><span class="sxs-lookup"><span data-stu-id="cabb4-113">Description</span></span>  

 <span data-ttu-id="cabb4-114">指示捕获了 SQL 异常。</span><span class="sxs-lookup"><span data-stu-id="cabb4-114">Indicates a SQL exception was caught.</span></span>  
  
## <a name="message"></a><span data-ttu-id="cabb4-115">消息</span><span class="sxs-lookup"><span data-stu-id="cabb4-115">Message</span></span>  

 <span data-ttu-id="cabb4-116">已捕获 SQL 异常编号为 %1 的消息 %2。</span><span class="sxs-lookup"><span data-stu-id="cabb4-116">Caught SQL Exception number %1 message %2.</span></span>  
  
## <a name="details"></a><span data-ttu-id="cabb4-117">详细信息</span><span class="sxs-lookup"><span data-stu-id="cabb4-117">Details</span></span>  
  
|<span data-ttu-id="cabb4-118">数据项名称</span><span class="sxs-lookup"><span data-stu-id="cabb4-118">Data Item Name</span></span>|<span data-ttu-id="cabb4-119">数据项类型</span><span class="sxs-lookup"><span data-stu-id="cabb4-119">Data Item Type</span></span>|<span data-ttu-id="cabb4-120">说明</span><span class="sxs-lookup"><span data-stu-id="cabb4-120">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="cabb4-121">ErrorNumber</span><span class="sxs-lookup"><span data-stu-id="cabb4-121">ErrorNumber</span></span>|<span data-ttu-id="cabb4-122">xs:string</span><span class="sxs-lookup"><span data-stu-id="cabb4-122">xs:string</span></span>|<span data-ttu-id="cabb4-123">SQL 错误号。</span><span class="sxs-lookup"><span data-stu-id="cabb4-123">The SQL error number.</span></span>|  
|<span data-ttu-id="cabb4-124">ExceptionMessage</span><span class="sxs-lookup"><span data-stu-id="cabb4-124">ExceptionMessage</span></span>|<span data-ttu-id="cabb4-125">xs:string</span><span class="sxs-lookup"><span data-stu-id="cabb4-125">xs:string</span></span>|<span data-ttu-id="cabb4-126">来自 SQL 异常的消息。</span><span class="sxs-lookup"><span data-stu-id="cabb4-126">The message from the SQL exception.</span></span>|  
|<span data-ttu-id="cabb4-127">应用程序域</span><span class="sxs-lookup"><span data-stu-id="cabb4-127">AppDomain</span></span>|<span data-ttu-id="cabb4-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="cabb4-128">xs:string</span></span>|<span data-ttu-id="cabb4-129">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="cabb4-129">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
