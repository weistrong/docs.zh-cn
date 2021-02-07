---
description: 了解详细信息： 1131-InvokeMethodUseAsyncPattern
title: 1131 - InvokeMethodUseAsyncPattern
ms.date: 03/30/2017
ms.assetid: eca50fa7-5276-4759-ad1c-e490b9bd1f82
ms.openlocfilehash: 59d8e5e1fe7c5b038df6fce3211fd01977abc4f9
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99667312"
---
# <a name="1131---invokemethoduseasyncpattern"></a><span data-ttu-id="83d63-103">1131 - InvokeMethodUseAsyncPattern</span><span class="sxs-lookup"><span data-stu-id="83d63-103">1131 - InvokeMethodUseAsyncPattern</span></span>

## <a name="properties"></a><span data-ttu-id="83d63-104">属性</span><span class="sxs-lookup"><span data-stu-id="83d63-104">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="83d63-105">ID</span><span class="sxs-lookup"><span data-stu-id="83d63-105">ID</span></span>|<span data-ttu-id="83d63-106">1131</span><span class="sxs-lookup"><span data-stu-id="83d63-106">1131</span></span>|  
|<span data-ttu-id="83d63-107">关键字</span><span class="sxs-lookup"><span data-stu-id="83d63-107">Keywords</span></span>|<span data-ttu-id="83d63-108">WFRuntime</span><span class="sxs-lookup"><span data-stu-id="83d63-108">WFRuntime</span></span>|  
|<span data-ttu-id="83d63-109">级别</span><span class="sxs-lookup"><span data-stu-id="83d63-109">Level</span></span>|<span data-ttu-id="83d63-110">信息</span><span class="sxs-lookup"><span data-stu-id="83d63-110">Information</span></span>|  
|<span data-ttu-id="83d63-111">通道</span><span class="sxs-lookup"><span data-stu-id="83d63-111">Channel</span></span>|<span data-ttu-id="83d63-112">Microsoft-Windows-应用程序服务器-应用程序/调试</span><span class="sxs-lookup"><span data-stu-id="83d63-112">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="83d63-113">说明</span><span class="sxs-lookup"><span data-stu-id="83d63-113">Description</span></span>  

 <span data-ttu-id="83d63-114">在 CacheMetadata 步骤中，InvokeMethod 活动指示它在调用方法时使用异步模式。</span><span class="sxs-lookup"><span data-stu-id="83d63-114">During CacheMetadata step, InvokeMethod activity indicates that it is using the async pattern when invoking the method.</span></span>  
  
## <a name="message"></a><span data-ttu-id="83d63-115">消息</span><span class="sxs-lookup"><span data-stu-id="83d63-115">Message</span></span>  

 <span data-ttu-id="83d63-116">InvokeMethod“%1”- 方法使用“%2”和“%3”的异步模式。</span><span class="sxs-lookup"><span data-stu-id="83d63-116">InvokeMethod '%1' - method uses asynchronous pattern of '%2' and '%3'.</span></span>  
  
## <a name="details"></a><span data-ttu-id="83d63-117">详细信息</span><span class="sxs-lookup"><span data-stu-id="83d63-117">Details</span></span>  
  
|<span data-ttu-id="83d63-118">数据项名称</span><span class="sxs-lookup"><span data-stu-id="83d63-118">Data Item Name</span></span>|<span data-ttu-id="83d63-119">数据项类型</span><span class="sxs-lookup"><span data-stu-id="83d63-119">Data Item Type</span></span>|<span data-ttu-id="83d63-120">说明</span><span class="sxs-lookup"><span data-stu-id="83d63-120">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="83d63-121">InvokeMethod</span><span class="sxs-lookup"><span data-stu-id="83d63-121">InvokeMethod</span></span>|<span data-ttu-id="83d63-122">xs:string</span><span class="sxs-lookup"><span data-stu-id="83d63-122">xs:string</span></span>|<span data-ttu-id="83d63-123">InvokeMethod 活动的显示名称。</span><span class="sxs-lookup"><span data-stu-id="83d63-123">The display name of the InvokeMethod activity.</span></span>|  
|<span data-ttu-id="83d63-124">BeginMethod</span><span class="sxs-lookup"><span data-stu-id="83d63-124">BeginMethod</span></span>|<span data-ttu-id="83d63-125">xs:string</span><span class="sxs-lookup"><span data-stu-id="83d63-125">xs:string</span></span>|<span data-ttu-id="83d63-126">begin 方法的名称。</span><span class="sxs-lookup"><span data-stu-id="83d63-126">The name of the begin method.</span></span>|  
|<span data-ttu-id="83d63-127">EndMethod</span><span class="sxs-lookup"><span data-stu-id="83d63-127">EndMethod</span></span>|<span data-ttu-id="83d63-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="83d63-128">xs:string</span></span>|<span data-ttu-id="83d63-129">end 方法的名称。</span><span class="sxs-lookup"><span data-stu-id="83d63-129">The name of the end method.</span></span>|  
|<span data-ttu-id="83d63-130">应用程序域</span><span class="sxs-lookup"><span data-stu-id="83d63-130">AppDomain</span></span>|<span data-ttu-id="83d63-131">xs:string</span><span class="sxs-lookup"><span data-stu-id="83d63-131">xs:string</span></span>|<span data-ttu-id="83d63-132">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="83d63-132">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
