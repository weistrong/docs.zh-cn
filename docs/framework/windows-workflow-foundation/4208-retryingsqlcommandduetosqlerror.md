---
description: 了解详细信息： 4208-RetryingSqlCommandDueToSqlError
title: 4208 - RetryingSqlCommandDueToSqlError
ms.date: 03/30/2017
ms.assetid: a8e6483a-a6e4-4bbf-82ec-cd8b6e711aad
ms.openlocfilehash: 11ea2260f6a2ceffc1ffdbfce2cb3e3ce784076d
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99755299"
---
# <a name="4208---retryingsqlcommandduetosqlerror"></a><span data-ttu-id="1dae4-103">4208 - RetryingSqlCommandDueToSqlError</span><span class="sxs-lookup"><span data-stu-id="1dae4-103">4208 - RetryingSqlCommandDueToSqlError</span></span>

## <a name="properties"></a><span data-ttu-id="1dae4-104">属性</span><span class="sxs-lookup"><span data-stu-id="1dae4-104">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="1dae4-105">ID</span><span class="sxs-lookup"><span data-stu-id="1dae4-105">ID</span></span>|<span data-ttu-id="1dae4-106">4208</span><span class="sxs-lookup"><span data-stu-id="1dae4-106">4208</span></span>|  
|<span data-ttu-id="1dae4-107">关键字</span><span class="sxs-lookup"><span data-stu-id="1dae4-107">Keywords</span></span>|<span data-ttu-id="1dae4-108">WFInstanceStore</span><span class="sxs-lookup"><span data-stu-id="1dae4-108">WFInstanceStore</span></span>|  
|<span data-ttu-id="1dae4-109">级别</span><span class="sxs-lookup"><span data-stu-id="1dae4-109">Level</span></span>|<span data-ttu-id="1dae4-110">信息</span><span class="sxs-lookup"><span data-stu-id="1dae4-110">Information</span></span>|  
|<span data-ttu-id="1dae4-111">通道</span><span class="sxs-lookup"><span data-stu-id="1dae4-111">Channel</span></span>|<span data-ttu-id="1dae4-112">Microsoft-Windows-应用程序服务器-应用程序/调试</span><span class="sxs-lookup"><span data-stu-id="1dae4-112">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="1dae4-113">说明</span><span class="sxs-lookup"><span data-stu-id="1dae4-113">Description</span></span>  

 <span data-ttu-id="1dae4-114">指示 SQL 提供程序由于 SQL 错误正在重试 SQL 命令。</span><span class="sxs-lookup"><span data-stu-id="1dae4-114">Indicates the SQL provider is retrying a SQL command due to a SQL error.</span></span>  
  
## <a name="message"></a><span data-ttu-id="1dae4-115">消息</span><span class="sxs-lookup"><span data-stu-id="1dae4-115">Message</span></span>  

 <span data-ttu-id="1dae4-116">因 SQL 错误号 %1，正在重试 SQL 命令。</span><span class="sxs-lookup"><span data-stu-id="1dae4-116">Retrying a SQL command due to SQL error number %1.</span></span>  
  
## <a name="details"></a><span data-ttu-id="1dae4-117">详细信息</span><span class="sxs-lookup"><span data-stu-id="1dae4-117">Details</span></span>  
  
|<span data-ttu-id="1dae4-118">数据项名称</span><span class="sxs-lookup"><span data-stu-id="1dae4-118">Data Item Name</span></span>|<span data-ttu-id="1dae4-119">数据项类型</span><span class="sxs-lookup"><span data-stu-id="1dae4-119">Data Item Type</span></span>|<span data-ttu-id="1dae4-120">说明</span><span class="sxs-lookup"><span data-stu-id="1dae4-120">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="1dae4-121">ErrorNumber</span><span class="sxs-lookup"><span data-stu-id="1dae4-121">ErrorNumber</span></span>|<span data-ttu-id="1dae4-122">xs:string</span><span class="sxs-lookup"><span data-stu-id="1dae4-122">xs:string</span></span>|<span data-ttu-id="1dae4-123">SQL 错误号。</span><span class="sxs-lookup"><span data-stu-id="1dae4-123">The SQL error number.</span></span>|  
|<span data-ttu-id="1dae4-124">应用程序域</span><span class="sxs-lookup"><span data-stu-id="1dae4-124">AppDomain</span></span>|<span data-ttu-id="1dae4-125">xs:string</span><span class="sxs-lookup"><span data-stu-id="1dae4-125">xs:string</span></span>|<span data-ttu-id="1dae4-126">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="1dae4-126">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
