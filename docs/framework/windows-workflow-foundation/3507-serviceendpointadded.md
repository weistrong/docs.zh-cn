---
description: 了解详细信息： 3507-ServiceEndpointAdded
title: 3507 - ServiceEndpointAdded
ms.date: 03/30/2017
ms.assetid: c068fc0e-07ee-4551-9824-ea7216e1fe37
ms.openlocfilehash: 7de51cb8908d3bf4b450c545c1a4c0f2bdc6a453
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99631471"
---
# <a name="3507---serviceendpointadded"></a><span data-ttu-id="d8512-103">3507 - ServiceEndpointAdded</span><span class="sxs-lookup"><span data-stu-id="d8512-103">3507 - ServiceEndpointAdded</span></span>

## <a name="properties"></a><span data-ttu-id="d8512-104">属性</span><span class="sxs-lookup"><span data-stu-id="d8512-104">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="d8512-105">ID</span><span class="sxs-lookup"><span data-stu-id="d8512-105">ID</span></span>|<span data-ttu-id="d8512-106">3507</span><span class="sxs-lookup"><span data-stu-id="d8512-106">3507</span></span>|  
|<span data-ttu-id="d8512-107">关键字</span><span class="sxs-lookup"><span data-stu-id="d8512-107">Keywords</span></span>|<span data-ttu-id="d8512-108">WFServices</span><span class="sxs-lookup"><span data-stu-id="d8512-108">WFServices</span></span>|  
|<span data-ttu-id="d8512-109">级别</span><span class="sxs-lookup"><span data-stu-id="d8512-109">Level</span></span>|<span data-ttu-id="d8512-110">信息</span><span class="sxs-lookup"><span data-stu-id="d8512-110">Information</span></span>|  
|<span data-ttu-id="d8512-111">通道</span><span class="sxs-lookup"><span data-stu-id="d8512-111">Channel</span></span>|<span data-ttu-id="d8512-112">Microsoft-Windows-应用程序服务器-应用程序/分析</span><span class="sxs-lookup"><span data-stu-id="d8512-112">Microsoft-Windows-Application Server-Applications/Analytic</span></span>|  
  
## <a name="description"></a><span data-ttu-id="d8512-113">说明</span><span class="sxs-lookup"><span data-stu-id="d8512-113">Description</span></span>  

 <span data-ttu-id="d8512-114">指示添加了服务终结点。</span><span class="sxs-lookup"><span data-stu-id="d8512-114">Indicates a service endpoint has been added.</span></span>  
  
## <a name="message"></a><span data-ttu-id="d8512-115">消息</span><span class="sxs-lookup"><span data-stu-id="d8512-115">Message</span></span>  

 <span data-ttu-id="d8512-116">已为地址“%1”、绑定“%2”和协定“%3”添加了服务终结点。</span><span class="sxs-lookup"><span data-stu-id="d8512-116">A service endpoint has been added for address '%1', binding '%2', and contract '%3'.</span></span>  
  
## <a name="details"></a><span data-ttu-id="d8512-117">详细信息</span><span class="sxs-lookup"><span data-stu-id="d8512-117">Details</span></span>  
  
|<span data-ttu-id="d8512-118">数据项名称</span><span class="sxs-lookup"><span data-stu-id="d8512-118">Data Item Name</span></span>|<span data-ttu-id="d8512-119">数据项类型</span><span class="sxs-lookup"><span data-stu-id="d8512-119">Data Item Type</span></span>|<span data-ttu-id="d8512-120">说明</span><span class="sxs-lookup"><span data-stu-id="d8512-120">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="d8512-121">地址</span><span class="sxs-lookup"><span data-stu-id="d8512-121">Address</span></span>|<span data-ttu-id="d8512-122">xs:string</span><span class="sxs-lookup"><span data-stu-id="d8512-122">xs:string</span></span>|<span data-ttu-id="d8512-123">终结点的地址。</span><span class="sxs-lookup"><span data-stu-id="d8512-123">The address of the endpoint.</span></span>|  
|<span data-ttu-id="d8512-124">绑定</span><span class="sxs-lookup"><span data-stu-id="d8512-124">Binding</span></span>|<span data-ttu-id="d8512-125">xs:string</span><span class="sxs-lookup"><span data-stu-id="d8512-125">xs:string</span></span>|<span data-ttu-id="d8512-126">终结点的绑定。</span><span class="sxs-lookup"><span data-stu-id="d8512-126">The binding of the endpoint.</span></span>|  
|<span data-ttu-id="d8512-127">协定</span><span class="sxs-lookup"><span data-stu-id="d8512-127">Contract</span></span>|<span data-ttu-id="d8512-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="d8512-128">xs:string</span></span>|<span data-ttu-id="d8512-129">终结点的协定。</span><span class="sxs-lookup"><span data-stu-id="d8512-129">The contract of the endpoint.</span></span>|  
|<span data-ttu-id="d8512-130">应用程序域</span><span class="sxs-lookup"><span data-stu-id="d8512-130">AppDomain</span></span>|<span data-ttu-id="d8512-131">xs:string</span><span class="sxs-lookup"><span data-stu-id="d8512-131">xs:string</span></span>|<span data-ttu-id="d8512-132">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="d8512-132">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
