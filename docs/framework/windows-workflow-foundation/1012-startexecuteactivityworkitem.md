---
description: 了解详细信息： 1012-StartExecuteActivityWorkItem
title: 1012 - StartExecuteActivityWorkItem
ms.date: 03/30/2017
ms.assetid: 29e9b1c6-c5d7-4b58-b59d-a06a923d3c80
ms.openlocfilehash: 3b57fc6d37a6708a4e22537de87a2566612088e6
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99714880"
---
# <a name="1012---startexecuteactivityworkitem"></a><span data-ttu-id="c5083-103">1012 - StartExecuteActivityWorkItem</span><span class="sxs-lookup"><span data-stu-id="c5083-103">1012 - StartExecuteActivityWorkItem</span></span>

## <a name="properties"></a><span data-ttu-id="c5083-104">属性</span><span class="sxs-lookup"><span data-stu-id="c5083-104">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="c5083-105">ID</span><span class="sxs-lookup"><span data-stu-id="c5083-105">ID</span></span>|<span data-ttu-id="c5083-106">1012</span><span class="sxs-lookup"><span data-stu-id="c5083-106">1012</span></span>|  
|<span data-ttu-id="c5083-107">关键字</span><span class="sxs-lookup"><span data-stu-id="c5083-107">Keywords</span></span>|<span data-ttu-id="c5083-108">WFRuntime</span><span class="sxs-lookup"><span data-stu-id="c5083-108">WFRuntime</span></span>|  
|<span data-ttu-id="c5083-109">级别</span><span class="sxs-lookup"><span data-stu-id="c5083-109">Level</span></span>|<span data-ttu-id="c5083-110">“详细”</span><span class="sxs-lookup"><span data-stu-id="c5083-110">Verbose</span></span>|  
|<span data-ttu-id="c5083-111">通道</span><span class="sxs-lookup"><span data-stu-id="c5083-111">Channel</span></span>|<span data-ttu-id="c5083-112">Microsoft-Windows-应用程序服务器-应用程序/调试</span><span class="sxs-lookup"><span data-stu-id="c5083-112">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="c5083-113">说明</span><span class="sxs-lookup"><span data-stu-id="c5083-113">Description</span></span>  

 <span data-ttu-id="c5083-114">指示 ExecuteActivityWorkItem 正在开始执行。</span><span class="sxs-lookup"><span data-stu-id="c5083-114">Indicates an ExecuteActivityWorkItem is starting execution.</span></span>  
  
## <a name="message"></a><span data-ttu-id="c5083-115">消息</span><span class="sxs-lookup"><span data-stu-id="c5083-115">Message</span></span>  

 <span data-ttu-id="c5083-116">开始为 Activity“%1”、DisplayName“%2”、InstanceId“%3”执行 ExecuteActivityWorkItem。</span><span class="sxs-lookup"><span data-stu-id="c5083-116">Starting execution of an ExecuteActivityWorkItem for Activity '%1', DisplayName: '%2', InstanceId: '%3'.</span></span>  
  
## <a name="details"></a><span data-ttu-id="c5083-117">详细信息</span><span class="sxs-lookup"><span data-stu-id="c5083-117">Details</span></span>  
  
|<span data-ttu-id="c5083-118">数据项名称</span><span class="sxs-lookup"><span data-stu-id="c5083-118">Data Item Name</span></span>|<span data-ttu-id="c5083-119">数据项类型</span><span class="sxs-lookup"><span data-stu-id="c5083-119">Data Item Type</span></span>|<span data-ttu-id="c5083-120">说明</span><span class="sxs-lookup"><span data-stu-id="c5083-120">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="c5083-121">活动</span><span class="sxs-lookup"><span data-stu-id="c5083-121">Activity</span></span>|<span data-ttu-id="c5083-122">xs:string</span><span class="sxs-lookup"><span data-stu-id="c5083-122">xs:string</span></span>|<span data-ttu-id="c5083-123">活动的类型名称。</span><span class="sxs-lookup"><span data-stu-id="c5083-123">The type name of the activity.</span></span>|  
|<span data-ttu-id="c5083-124">DisplayName</span><span class="sxs-lookup"><span data-stu-id="c5083-124">DisplayName</span></span>|<span data-ttu-id="c5083-125">xs:string</span><span class="sxs-lookup"><span data-stu-id="c5083-125">xs:string</span></span>|<span data-ttu-id="c5083-126">活动的显示名称。</span><span class="sxs-lookup"><span data-stu-id="c5083-126">The display name of the activity.</span></span>|  
|<span data-ttu-id="c5083-127">InstanceId</span><span class="sxs-lookup"><span data-stu-id="c5083-127">InstanceId</span></span>|<span data-ttu-id="c5083-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="c5083-128">xs:string</span></span>|<span data-ttu-id="c5083-129">活动的实例 ID。</span><span class="sxs-lookup"><span data-stu-id="c5083-129">The instance id of the activity.</span></span>|  
|<span data-ttu-id="c5083-130">应用程序域</span><span class="sxs-lookup"><span data-stu-id="c5083-130">AppDomain</span></span>|<span data-ttu-id="c5083-131">xs:string</span><span class="sxs-lookup"><span data-stu-id="c5083-131">xs:string</span></span>|<span data-ttu-id="c5083-132">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="c5083-132">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
