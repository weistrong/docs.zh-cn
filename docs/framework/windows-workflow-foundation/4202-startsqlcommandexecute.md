---
description: 了解详细信息： 4202-StartSqlCommandExecute
title: 4202 - StartSqlCommandExecute
ms.date: 03/30/2017
ms.assetid: 4559f64f-c824-4075-9e7e-4710bf30f805
ms.openlocfilehash: 1282f275933eff0effbda75851e33531c55adb36
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99755329"
---
# <a name="4202---startsqlcommandexecute"></a><span data-ttu-id="5a313-103">4202 - StartSqlCommandExecute</span><span class="sxs-lookup"><span data-stu-id="5a313-103">4202 - StartSqlCommandExecute</span></span>

## <a name="properties"></a><span data-ttu-id="5a313-104">属性</span><span class="sxs-lookup"><span data-stu-id="5a313-104">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="5a313-105">ID</span><span class="sxs-lookup"><span data-stu-id="5a313-105">ID</span></span>|<span data-ttu-id="5a313-106">4202</span><span class="sxs-lookup"><span data-stu-id="5a313-106">4202</span></span>|  
|<span data-ttu-id="5a313-107">关键字</span><span class="sxs-lookup"><span data-stu-id="5a313-107">Keywords</span></span>|<span data-ttu-id="5a313-108">WFInstanceStore</span><span class="sxs-lookup"><span data-stu-id="5a313-108">WFInstanceStore</span></span>|  
|<span data-ttu-id="5a313-109">级别</span><span class="sxs-lookup"><span data-stu-id="5a313-109">Level</span></span>|<span data-ttu-id="5a313-110">“详细”</span><span class="sxs-lookup"><span data-stu-id="5a313-110">Verbose</span></span>|  
|<span data-ttu-id="5a313-111">通道</span><span class="sxs-lookup"><span data-stu-id="5a313-111">Channel</span></span>|<span data-ttu-id="5a313-112">Microsoft-Windows-应用程序服务器-应用程序/调试</span><span class="sxs-lookup"><span data-stu-id="5a313-112">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="5a313-113">说明</span><span class="sxs-lookup"><span data-stu-id="5a313-113">Description</span></span>  

 <span data-ttu-id="5a313-114">指示 SQL 命令正在执行。</span><span class="sxs-lookup"><span data-stu-id="5a313-114">Indicates a SQL command is being executed.</span></span>  
  
## <a name="message"></a><span data-ttu-id="5a313-115">消息</span><span class="sxs-lookup"><span data-stu-id="5a313-115">Message</span></span>  

 <span data-ttu-id="5a313-116">正在开始 SQL 命令执行: %1</span><span class="sxs-lookup"><span data-stu-id="5a313-116">Starting SQL command execution: %1</span></span>  
  
## <a name="details"></a><span data-ttu-id="5a313-117">详细信息</span><span class="sxs-lookup"><span data-stu-id="5a313-117">Details</span></span>  
  
|<span data-ttu-id="5a313-118">数据项名称</span><span class="sxs-lookup"><span data-stu-id="5a313-118">Data Item Name</span></span>|<span data-ttu-id="5a313-119">数据项类型</span><span class="sxs-lookup"><span data-stu-id="5a313-119">Data Item Type</span></span>|<span data-ttu-id="5a313-120">说明</span><span class="sxs-lookup"><span data-stu-id="5a313-120">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="5a313-121">SqlCommand</span><span class="sxs-lookup"><span data-stu-id="5a313-121">SqlCommand</span></span>|<span data-ttu-id="5a313-122">xs:string</span><span class="sxs-lookup"><span data-stu-id="5a313-122">xs:string</span></span>|<span data-ttu-id="5a313-123">已执行的 SQL 命令。</span><span class="sxs-lookup"><span data-stu-id="5a313-123">The SQL command that was executed.</span></span>|  
|<span data-ttu-id="5a313-124">应用程序域</span><span class="sxs-lookup"><span data-stu-id="5a313-124">AppDomain</span></span>|<span data-ttu-id="5a313-125">xs:string</span><span class="sxs-lookup"><span data-stu-id="5a313-125">xs:string</span></span>|<span data-ttu-id="5a313-126">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="5a313-126">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
