---
description: 了解详细信息： 3508-TrackingProfileNotFound
title: 3508 - TrackingProfileNotFound
ms.date: 03/30/2017
ms.assetid: 4cee3c4a-0490-4c94-aa19-ef7ce7287c02
ms.openlocfilehash: 3e97af1689a868fb103b06413a0c4f28b0c1f652
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99778004"
---
# <a name="3508---trackingprofilenotfound"></a><span data-ttu-id="69c28-103">3508 - TrackingProfileNotFound</span><span class="sxs-lookup"><span data-stu-id="69c28-103">3508 - TrackingProfileNotFound</span></span>

## <a name="properties"></a><span data-ttu-id="69c28-104">属性</span><span class="sxs-lookup"><span data-stu-id="69c28-104">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="69c28-105">ID</span><span class="sxs-lookup"><span data-stu-id="69c28-105">ID</span></span>|<span data-ttu-id="69c28-106">3508</span><span class="sxs-lookup"><span data-stu-id="69c28-106">3508</span></span>|  
|<span data-ttu-id="69c28-107">关键字</span><span class="sxs-lookup"><span data-stu-id="69c28-107">Keywords</span></span>|<span data-ttu-id="69c28-108">WFServices</span><span class="sxs-lookup"><span data-stu-id="69c28-108">WFServices</span></span>|  
|<span data-ttu-id="69c28-109">级别</span><span class="sxs-lookup"><span data-stu-id="69c28-109">Level</span></span>|<span data-ttu-id="69c28-110">“详细”</span><span class="sxs-lookup"><span data-stu-id="69c28-110">Verbose</span></span>|  
|<span data-ttu-id="69c28-111">通道</span><span class="sxs-lookup"><span data-stu-id="69c28-111">Channel</span></span>|<span data-ttu-id="69c28-112">Microsoft-Windows-应用程序服务器-应用程序/分析</span><span class="sxs-lookup"><span data-stu-id="69c28-112">Microsoft-Windows-Application Server-Applications/Analytic</span></span>|  
  
## <a name="description"></a><span data-ttu-id="69c28-113">说明</span><span class="sxs-lookup"><span data-stu-id="69c28-113">Description</span></span>  

 <span data-ttu-id="69c28-114">指示在配置文件中找不到 TrackingProfile，或 ActivityDefinitionId 与配置文件不匹配。</span><span class="sxs-lookup"><span data-stu-id="69c28-114">Indicates either a TrackingProfile is not found in the config file or the ActivityDefinitionId does not match the profile.</span></span>  
  
## <a name="message"></a><span data-ttu-id="69c28-115">消息</span><span class="sxs-lookup"><span data-stu-id="69c28-115">Message</span></span>  

 <span data-ttu-id="69c28-116">未找到 ActivityDefinitionId“%2”的 TrackingProfile“%1”。</span><span class="sxs-lookup"><span data-stu-id="69c28-116">TrackingProfile '%1' for the ActivityDefinitionId '%2' not found.</span></span> <span data-ttu-id="69c28-117">在配置文件中找不到 TrackingProfile，或 ActivityDefinitionId 不匹配。</span><span class="sxs-lookup"><span data-stu-id="69c28-117">Either the TrackingProfile is not found in the config file or the ActivityDefinitionId does not match.</span></span>  
  
## <a name="details"></a><span data-ttu-id="69c28-118">详细信息</span><span class="sxs-lookup"><span data-stu-id="69c28-118">Details</span></span>  
  
|<span data-ttu-id="69c28-119">数据项名称</span><span class="sxs-lookup"><span data-stu-id="69c28-119">Data Item Name</span></span>|<span data-ttu-id="69c28-120">数据项类型</span><span class="sxs-lookup"><span data-stu-id="69c28-120">Data Item Type</span></span>|<span data-ttu-id="69c28-121">说明</span><span class="sxs-lookup"><span data-stu-id="69c28-121">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="69c28-122">TrackingProfile</span><span class="sxs-lookup"><span data-stu-id="69c28-122">TrackingProfile</span></span>|<span data-ttu-id="69c28-123">xs:string</span><span class="sxs-lookup"><span data-stu-id="69c28-123">xs:string</span></span>|<span data-ttu-id="69c28-124">跟踪配置文件的名称。</span><span class="sxs-lookup"><span data-stu-id="69c28-124">The name of the tracking profile.</span></span>|  
|<span data-ttu-id="69c28-125">ActivityDefinitionId</span><span class="sxs-lookup"><span data-stu-id="69c28-125">ActivityDefinitionId</span></span>|<span data-ttu-id="69c28-126">xs:string</span><span class="sxs-lookup"><span data-stu-id="69c28-126">xs:string</span></span>|<span data-ttu-id="69c28-127">活动定义 ID。</span><span class="sxs-lookup"><span data-stu-id="69c28-127">The activity definition id.</span></span>|  
|<span data-ttu-id="69c28-128">应用程序域</span><span class="sxs-lookup"><span data-stu-id="69c28-128">AppDomain</span></span>|<span data-ttu-id="69c28-129">xs:string</span><span class="sxs-lookup"><span data-stu-id="69c28-129">xs:string</span></span>|<span data-ttu-id="69c28-130">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="69c28-130">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
