---
description: 了解详细信息： 4207-MaximumRetriesExceededForSqlCommand
title: 4207 - MaximumRetriesExceededForSqlCommand
ms.date: 03/30/2017
ms.assetid: 8c8bee26-9ad4-4e01-bd16-0e1fd510fb6b
ms.openlocfilehash: e831da08e37010afaa33f3a52cd7cf7a9b4d713b
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99742714"
---
# <a name="4207---maximumretriesexceededforsqlcommand"></a><span data-ttu-id="c6441-103">4207 - MaximumRetriesExceededForSqlCommand</span><span class="sxs-lookup"><span data-stu-id="c6441-103">4207 - MaximumRetriesExceededForSqlCommand</span></span>

## <a name="properties"></a><span data-ttu-id="c6441-104">属性</span><span class="sxs-lookup"><span data-stu-id="c6441-104">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="c6441-105">ID</span><span class="sxs-lookup"><span data-stu-id="c6441-105">ID</span></span>|<span data-ttu-id="c6441-106">4207</span><span class="sxs-lookup"><span data-stu-id="c6441-106">4207</span></span>|  
|<span data-ttu-id="c6441-107">关键字</span><span class="sxs-lookup"><span data-stu-id="c6441-107">Keywords</span></span>|<span data-ttu-id="c6441-108">配额，FInstanceStore</span><span class="sxs-lookup"><span data-stu-id="c6441-108">Quota, WFInstanceStore</span></span>|  
|<span data-ttu-id="c6441-109">级别</span><span class="sxs-lookup"><span data-stu-id="c6441-109">Level</span></span>|<span data-ttu-id="c6441-110">信息</span><span class="sxs-lookup"><span data-stu-id="c6441-110">Information</span></span>|  
|<span data-ttu-id="c6441-111">通道</span><span class="sxs-lookup"><span data-stu-id="c6441-111">Channel</span></span>|<span data-ttu-id="c6441-112">Microsoft-Windows-应用程序服务器-应用程序/调试</span><span class="sxs-lookup"><span data-stu-id="c6441-112">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="c6441-113">说明</span><span class="sxs-lookup"><span data-stu-id="c6441-113">Description</span></span>  

 <span data-ttu-id="c6441-114">指示 SQL 提供程序正在放弃重试 SQL 命令，因为执行次数已达到了允许的最多重试次数。</span><span class="sxs-lookup"><span data-stu-id="c6441-114">Indicates SQL provider is giving up retrying a SQL command as the maximum number of retries have been performed.</span></span>  
  
## <a name="message"></a><span data-ttu-id="c6441-115">消息</span><span class="sxs-lookup"><span data-stu-id="c6441-115">Message</span></span>  

 <span data-ttu-id="c6441-116">正在放弃重试 SQL 命令，因为执行次数已达到了允许的最多重试次数。</span><span class="sxs-lookup"><span data-stu-id="c6441-116">Giving up retrying a SQL command as the maximum number of retries have been performed.</span></span>  
  
## <a name="details"></a><span data-ttu-id="c6441-117">详细信息</span><span class="sxs-lookup"><span data-stu-id="c6441-117">Details</span></span>  
  
|<span data-ttu-id="c6441-118">数据项名称</span><span class="sxs-lookup"><span data-stu-id="c6441-118">Data Item Name</span></span>|<span data-ttu-id="c6441-119">数据项类型</span><span class="sxs-lookup"><span data-stu-id="c6441-119">Data Item Type</span></span>|<span data-ttu-id="c6441-120">说明</span><span class="sxs-lookup"><span data-stu-id="c6441-120">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="c6441-121">应用程序域</span><span class="sxs-lookup"><span data-stu-id="c6441-121">AppDomain</span></span>|<span data-ttu-id="c6441-122">xs:string</span><span class="sxs-lookup"><span data-stu-id="c6441-122">xs:string</span></span>|<span data-ttu-id="c6441-123">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="c6441-123">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
