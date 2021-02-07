---
description: 了解详细信息： 1124-InvokeMethodIsStatic
title: 1124 - InvokeMethodIsStatic
ms.date: 03/30/2017
ms.assetid: b9643641-fb52-4fa8-b354-4dd6617d68f6
ms.openlocfilehash: 86febd9c94c2e4c533eb5ab4349855f6d048a5ae
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99667377"
---
# <a name="1124---invokemethodisstatic"></a><span data-ttu-id="c5831-103">1124 - InvokeMethodIsStatic</span><span class="sxs-lookup"><span data-stu-id="c5831-103">1124 - InvokeMethodIsStatic</span></span>

## <a name="properties"></a><span data-ttu-id="c5831-104">属性</span><span class="sxs-lookup"><span data-stu-id="c5831-104">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="c5831-105">ID</span><span class="sxs-lookup"><span data-stu-id="c5831-105">ID</span></span>|<span data-ttu-id="c5831-106">1124</span><span class="sxs-lookup"><span data-stu-id="c5831-106">1124</span></span>|  
|<span data-ttu-id="c5831-107">关键字</span><span class="sxs-lookup"><span data-stu-id="c5831-107">Keywords</span></span>|<span data-ttu-id="c5831-108">WFRuntime</span><span class="sxs-lookup"><span data-stu-id="c5831-108">WFRuntime</span></span>|  
|<span data-ttu-id="c5831-109">级别</span><span class="sxs-lookup"><span data-stu-id="c5831-109">Level</span></span>|<span data-ttu-id="c5831-110">信息</span><span class="sxs-lookup"><span data-stu-id="c5831-110">Information</span></span>|  
|<span data-ttu-id="c5831-111">通道</span><span class="sxs-lookup"><span data-stu-id="c5831-111">Channel</span></span>|<span data-ttu-id="c5831-112">Microsoft-Windows-应用程序服务器-应用程序/调试</span><span class="sxs-lookup"><span data-stu-id="c5831-112">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="c5831-113">说明</span><span class="sxs-lookup"><span data-stu-id="c5831-113">Description</span></span>  

 <span data-ttu-id="c5831-114">在 CacheMetadata 步骤中，InvokeMethod 活动指示要调用的方法是静态的。</span><span class="sxs-lookup"><span data-stu-id="c5831-114">During CacheMetadata step, InvokeMethod activity indicates the method to be invoked is static.</span></span>  
  
## <a name="message"></a><span data-ttu-id="c5831-115">消息</span><span class="sxs-lookup"><span data-stu-id="c5831-115">Message</span></span>  

 <span data-ttu-id="c5831-116">InvokeMethod“%1”- 方法为静态。</span><span class="sxs-lookup"><span data-stu-id="c5831-116">InvokeMethod '%1' - method is Static.</span></span>  
  
## <a name="details"></a><span data-ttu-id="c5831-117">详细信息</span><span class="sxs-lookup"><span data-stu-id="c5831-117">Details</span></span>  
  
|<span data-ttu-id="c5831-118">数据项名称</span><span class="sxs-lookup"><span data-stu-id="c5831-118">Data Item Name</span></span>|<span data-ttu-id="c5831-119">数据项类型</span><span class="sxs-lookup"><span data-stu-id="c5831-119">Data Item Type</span></span>|<span data-ttu-id="c5831-120">说明</span><span class="sxs-lookup"><span data-stu-id="c5831-120">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="c5831-121">InvokeMethod</span><span class="sxs-lookup"><span data-stu-id="c5831-121">InvokeMethod</span></span>|<span data-ttu-id="c5831-122">xs:string</span><span class="sxs-lookup"><span data-stu-id="c5831-122">xs:string</span></span>|<span data-ttu-id="c5831-123">InvokeMethod 活动的显示名称。</span><span class="sxs-lookup"><span data-stu-id="c5831-123">The display name of the InvokeMethod activity.</span></span>|  
|<span data-ttu-id="c5831-124">应用程序域</span><span class="sxs-lookup"><span data-stu-id="c5831-124">AppDomain</span></span>|<span data-ttu-id="c5831-125">xs:string</span><span class="sxs-lookup"><span data-stu-id="c5831-125">xs:string</span></span>|<span data-ttu-id="c5831-126">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="c5831-126">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
