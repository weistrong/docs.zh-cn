---
description: 了解详细信息： 4201-EndSqlCommandExecute
title: 4201 - EndSqlCommandExecute
ms.date: 03/30/2017
ms.assetid: ae0dbc15-f98c-4096-a8d9-fbe4dc36f1cd
ms.openlocfilehash: e0b98e8da5a0a284bfa55e97f5dde25a2ce42b42
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99755364"
---
# <a name="4201---endsqlcommandexecute"></a><span data-ttu-id="e7aa2-103">4201 - EndSqlCommandExecute</span><span class="sxs-lookup"><span data-stu-id="e7aa2-103">4201 - EndSqlCommandExecute</span></span>

## <a name="properties"></a><span data-ttu-id="e7aa2-104">属性</span><span class="sxs-lookup"><span data-stu-id="e7aa2-104">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="e7aa2-105">ID</span><span class="sxs-lookup"><span data-stu-id="e7aa2-105">ID</span></span>|<span data-ttu-id="e7aa2-106">4201</span><span class="sxs-lookup"><span data-stu-id="e7aa2-106">4201</span></span>|  
|<span data-ttu-id="e7aa2-107">关键字</span><span class="sxs-lookup"><span data-stu-id="e7aa2-107">Keywords</span></span>|<span data-ttu-id="e7aa2-108">WFInstanceStore</span><span class="sxs-lookup"><span data-stu-id="e7aa2-108">WFInstanceStore</span></span>|  
|<span data-ttu-id="e7aa2-109">级别</span><span class="sxs-lookup"><span data-stu-id="e7aa2-109">Level</span></span>|<span data-ttu-id="e7aa2-110">“详细”</span><span class="sxs-lookup"><span data-stu-id="e7aa2-110">Verbose</span></span>|  
|<span data-ttu-id="e7aa2-111">通道</span><span class="sxs-lookup"><span data-stu-id="e7aa2-111">Channel</span></span>|<span data-ttu-id="e7aa2-112">Microsoft-Windows-应用程序服务器-应用程序/调试</span><span class="sxs-lookup"><span data-stu-id="e7aa2-112">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="e7aa2-113">说明</span><span class="sxs-lookup"><span data-stu-id="e7aa2-113">Description</span></span>  

 <span data-ttu-id="e7aa2-114">指示 SQL 命令已完成执行。</span><span class="sxs-lookup"><span data-stu-id="e7aa2-114">Indicates a SQL command has finished executing.</span></span>  
  
## <a name="message"></a><span data-ttu-id="e7aa2-115">消息</span><span class="sxs-lookup"><span data-stu-id="e7aa2-115">Message</span></span>  

 <span data-ttu-id="e7aa2-116">结束 SQL 命令执行: %1</span><span class="sxs-lookup"><span data-stu-id="e7aa2-116">End SQL command execution: %1</span></span>  
  
## <a name="details"></a><span data-ttu-id="e7aa2-117">详细信息</span><span class="sxs-lookup"><span data-stu-id="e7aa2-117">Details</span></span>  
  
|<span data-ttu-id="e7aa2-118">数据项名称</span><span class="sxs-lookup"><span data-stu-id="e7aa2-118">Data Item Name</span></span>|<span data-ttu-id="e7aa2-119">数据项类型</span><span class="sxs-lookup"><span data-stu-id="e7aa2-119">Data Item Type</span></span>|<span data-ttu-id="e7aa2-120">说明</span><span class="sxs-lookup"><span data-stu-id="e7aa2-120">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="e7aa2-121">SqlCommand</span><span class="sxs-lookup"><span data-stu-id="e7aa2-121">SqlCommand</span></span>|<span data-ttu-id="e7aa2-122">xs:string</span><span class="sxs-lookup"><span data-stu-id="e7aa2-122">xs:string</span></span>|<span data-ttu-id="e7aa2-123">已执行的 SQL 命令。</span><span class="sxs-lookup"><span data-stu-id="e7aa2-123">The SQL command that was executed.</span></span>|  
|<span data-ttu-id="e7aa2-124">应用程序域</span><span class="sxs-lookup"><span data-stu-id="e7aa2-124">AppDomain</span></span>|<span data-ttu-id="e7aa2-125">xs:string</span><span class="sxs-lookup"><span data-stu-id="e7aa2-125">xs:string</span></span>|<span data-ttu-id="e7aa2-126">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="e7aa2-126">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
