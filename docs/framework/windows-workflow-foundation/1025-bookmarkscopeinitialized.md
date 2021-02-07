---
description: 了解详细信息： 1025-BookmarkScopeInitialized
title: 1025 - BookmarkScopeInitialized
ms.date: 03/30/2017
ms.assetid: 63584434-e709-471d-9e96-97d3d99e70d6
ms.openlocfilehash: 22e686253fc5d580fba453950825072667247fad
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99755494"
---
# <a name="1025---bookmarkscopeinitialized"></a><span data-ttu-id="16bd2-103">1025 - BookmarkScopeInitialized</span><span class="sxs-lookup"><span data-stu-id="16bd2-103">1025 - BookmarkScopeInitialized</span></span>

## <a name="properties"></a><span data-ttu-id="16bd2-104">属性</span><span class="sxs-lookup"><span data-stu-id="16bd2-104">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="16bd2-105">ID</span><span class="sxs-lookup"><span data-stu-id="16bd2-105">ID</span></span>|<span data-ttu-id="16bd2-106">1025</span><span class="sxs-lookup"><span data-stu-id="16bd2-106">1025</span></span>|  
|<span data-ttu-id="16bd2-107">关键字</span><span class="sxs-lookup"><span data-stu-id="16bd2-107">Keywords</span></span>|<span data-ttu-id="16bd2-108">WFRuntime</span><span class="sxs-lookup"><span data-stu-id="16bd2-108">WFRuntime</span></span>|  
|<span data-ttu-id="16bd2-109">级别</span><span class="sxs-lookup"><span data-stu-id="16bd2-109">Level</span></span>|<span data-ttu-id="16bd2-110">“详细”</span><span class="sxs-lookup"><span data-stu-id="16bd2-110">Verbose</span></span>|  
|<span data-ttu-id="16bd2-111">通道</span><span class="sxs-lookup"><span data-stu-id="16bd2-111">Channel</span></span>|<span data-ttu-id="16bd2-112">Microsoft-Windows-应用程序服务器-应用程序/调试</span><span class="sxs-lookup"><span data-stu-id="16bd2-112">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="16bd2-113">说明</span><span class="sxs-lookup"><span data-stu-id="16bd2-113">Description</span></span>  

 <span data-ttu-id="16bd2-114">指示已初始化 BookmarkScope。</span><span class="sxs-lookup"><span data-stu-id="16bd2-114">Indicates a BookmarkScope has been initialized.</span></span>  
  
## <a name="message"></a><span data-ttu-id="16bd2-115">消息</span><span class="sxs-lookup"><span data-stu-id="16bd2-115">Message</span></span>  

 <span data-ttu-id="16bd2-116">TemporaryId 为“%1”的 BookmarkScope 已初始化，ID 为:“%2”。</span><span class="sxs-lookup"><span data-stu-id="16bd2-116">The BookmarkScope that had TemporaryId: '%1' has been initialized with Id: '%2'.</span></span>  
  
## <a name="details"></a><span data-ttu-id="16bd2-117">详细信息</span><span class="sxs-lookup"><span data-stu-id="16bd2-117">Details</span></span>  
  
|<span data-ttu-id="16bd2-118">数据项名称</span><span class="sxs-lookup"><span data-stu-id="16bd2-118">Data Item Name</span></span>|<span data-ttu-id="16bd2-119">数据项类型</span><span class="sxs-lookup"><span data-stu-id="16bd2-119">Data Item Type</span></span>|<span data-ttu-id="16bd2-120">说明</span><span class="sxs-lookup"><span data-stu-id="16bd2-120">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="16bd2-121">TemporaryId</span><span class="sxs-lookup"><span data-stu-id="16bd2-121">TemporaryId</span></span>|<span data-ttu-id="16bd2-122">xs:string</span><span class="sxs-lookup"><span data-stu-id="16bd2-122">xs:string</span></span>|<span data-ttu-id="16bd2-123">书签的临时 ID。</span><span class="sxs-lookup"><span data-stu-id="16bd2-123">The temporary id of the bookmark.</span></span>|  
|<span data-ttu-id="16bd2-124">InitializedId</span><span class="sxs-lookup"><span data-stu-id="16bd2-124">InitializedId</span></span>|<span data-ttu-id="16bd2-125">xs:string</span><span class="sxs-lookup"><span data-stu-id="16bd2-125">xs:string</span></span>|<span data-ttu-id="16bd2-126">书签的初始化的 ID。</span><span class="sxs-lookup"><span data-stu-id="16bd2-126">The initialized id of the bookmark.</span></span>|  
|<span data-ttu-id="16bd2-127">应用程序域</span><span class="sxs-lookup"><span data-stu-id="16bd2-127">AppDomain</span></span>|<span data-ttu-id="16bd2-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="16bd2-128">xs:string</span></span>|<span data-ttu-id="16bd2-129">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="16bd2-129">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
