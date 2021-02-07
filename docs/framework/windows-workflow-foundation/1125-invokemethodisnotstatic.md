---
description: 了解详细信息： 1125-InvokeMethodIsNotStatic
title: 1125 - InvokeMethodIsNotStatic
ms.date: 03/30/2017
ms.assetid: ea2b3827-63da-497b-b2c3-d5cebefe57a1
ms.openlocfilehash: cd63b7b75121a70f7d7bad6a799827971aa4eae9
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99667364"
---
# <a name="1125---invokemethodisnotstatic"></a><span data-ttu-id="48d27-103">1125 - InvokeMethodIsNotStatic</span><span class="sxs-lookup"><span data-stu-id="48d27-103">1125 - InvokeMethodIsNotStatic</span></span>

## <a name="properties"></a><span data-ttu-id="48d27-104">属性</span><span class="sxs-lookup"><span data-stu-id="48d27-104">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="48d27-105">ID</span><span class="sxs-lookup"><span data-stu-id="48d27-105">ID</span></span>|<span data-ttu-id="48d27-106">1125</span><span class="sxs-lookup"><span data-stu-id="48d27-106">1125</span></span>|  
|<span data-ttu-id="48d27-107">关键字</span><span class="sxs-lookup"><span data-stu-id="48d27-107">Keywords</span></span>|<span data-ttu-id="48d27-108">WFRuntime</span><span class="sxs-lookup"><span data-stu-id="48d27-108">WFRuntime</span></span>|  
|<span data-ttu-id="48d27-109">级别</span><span class="sxs-lookup"><span data-stu-id="48d27-109">Level</span></span>|<span data-ttu-id="48d27-110">信息</span><span class="sxs-lookup"><span data-stu-id="48d27-110">Information</span></span>|  
|<span data-ttu-id="48d27-111">通道</span><span class="sxs-lookup"><span data-stu-id="48d27-111">Channel</span></span>|<span data-ttu-id="48d27-112">Microsoft-Windows-应用程序服务器-应用程序/调试</span><span class="sxs-lookup"><span data-stu-id="48d27-112">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="48d27-113">说明</span><span class="sxs-lookup"><span data-stu-id="48d27-113">Description</span></span>  

 <span data-ttu-id="48d27-114">在 CacheMetadata 步骤中，InvokeMethod 活动指示要调用的方法是非静态的。</span><span class="sxs-lookup"><span data-stu-id="48d27-114">During CacheMetadata step, InvokeMethod activity indicates the method to be invoked is not static.</span></span>  
  
## <a name="message"></a><span data-ttu-id="48d27-115">消息</span><span class="sxs-lookup"><span data-stu-id="48d27-115">Message</span></span>  

 <span data-ttu-id="48d27-116">InvokeMethod“%1”- 方法非静态。</span><span class="sxs-lookup"><span data-stu-id="48d27-116">InvokeMethod '%1' - method is not Static.</span></span>  
  
## <a name="details"></a><span data-ttu-id="48d27-117">详细信息</span><span class="sxs-lookup"><span data-stu-id="48d27-117">Details</span></span>  
  
|<span data-ttu-id="48d27-118">数据项名称</span><span class="sxs-lookup"><span data-stu-id="48d27-118">Data Item Name</span></span>|<span data-ttu-id="48d27-119">数据项类型</span><span class="sxs-lookup"><span data-stu-id="48d27-119">Data Item Type</span></span>|<span data-ttu-id="48d27-120">说明</span><span class="sxs-lookup"><span data-stu-id="48d27-120">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="48d27-121">InvokeMethod</span><span class="sxs-lookup"><span data-stu-id="48d27-121">InvokeMethod</span></span>|<span data-ttu-id="48d27-122">xs:string</span><span class="sxs-lookup"><span data-stu-id="48d27-122">xs:string</span></span>|<span data-ttu-id="48d27-123">InvokeMethod 活动的显示名称。</span><span class="sxs-lookup"><span data-stu-id="48d27-123">The display name of the InvokeMethod activity.</span></span>|  
|<span data-ttu-id="48d27-124">应用程序域</span><span class="sxs-lookup"><span data-stu-id="48d27-124">AppDomain</span></span>|<span data-ttu-id="48d27-125">xs:string</span><span class="sxs-lookup"><span data-stu-id="48d27-125">xs:string</span></span>|<span data-ttu-id="48d27-126">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="48d27-126">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
