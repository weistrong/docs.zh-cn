---
description: 了解详细信息： 39456-TrackingRecordDropped
title: 39456 - TrackingRecordDropped
ms.date: 03/30/2017
ms.assetid: da13d5bc-1736-47a4-b3fd-064ca8040326
ms.openlocfilehash: 0f6920ef85327318f4ea8662ae36f26c7494bcb2
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99631289"
---
# <a name="39456---trackingrecorddropped"></a><span data-ttu-id="212bd-103">39456 - TrackingRecordDropped</span><span class="sxs-lookup"><span data-stu-id="212bd-103">39456 - TrackingRecordDropped</span></span>

## <a name="properties"></a><span data-ttu-id="212bd-104">属性</span><span class="sxs-lookup"><span data-stu-id="212bd-104">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="212bd-105">ID</span><span class="sxs-lookup"><span data-stu-id="212bd-105">ID</span></span>|<span data-ttu-id="212bd-106">39456</span><span class="sxs-lookup"><span data-stu-id="212bd-106">39456</span></span>|  
|<span data-ttu-id="212bd-107">关键字</span><span class="sxs-lookup"><span data-stu-id="212bd-107">Keywords</span></span>|<span data-ttu-id="212bd-108">WFTracking</span><span class="sxs-lookup"><span data-stu-id="212bd-108">WFTracking</span></span>|  
|<span data-ttu-id="212bd-109">级别</span><span class="sxs-lookup"><span data-stu-id="212bd-109">Level</span></span>|<span data-ttu-id="212bd-110">警告</span><span class="sxs-lookup"><span data-stu-id="212bd-110">Warning</span></span>|  
|<span data-ttu-id="212bd-111">通道</span><span class="sxs-lookup"><span data-stu-id="212bd-111">Channel</span></span>|<span data-ttu-id="212bd-112">Microsoft-Windows-应用程序服务器-应用程序/调试</span><span class="sxs-lookup"><span data-stu-id="212bd-112">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="212bd-113">说明</span><span class="sxs-lookup"><span data-stu-id="212bd-113">Description</span></span>  

 <span data-ttu-id="212bd-114">指示一个跟踪记录已被丢弃，因为其大小超过 ETW 提供程序会话允许的最大大小。</span><span class="sxs-lookup"><span data-stu-id="212bd-114">Indicates a tracking record has been dropped because its size exceeds maximum allowed by the ETW session provider.</span></span>  
  
## <a name="message"></a><span data-ttu-id="212bd-115">消息</span><span class="sxs-lookup"><span data-stu-id="212bd-115">Message</span></span>  

 <span data-ttu-id="212bd-116">跟踪记录 %1 的大小超出了 ETW 会话对提供程序 %2 允许的最大值</span><span class="sxs-lookup"><span data-stu-id="212bd-116">Size of tracking record %1 exceeds maximum allowed by the ETW session for provider %2</span></span>  
  
## <a name="details"></a><span data-ttu-id="212bd-117">详细信息</span><span class="sxs-lookup"><span data-stu-id="212bd-117">Details</span></span>  
  
|<span data-ttu-id="212bd-118">数据项名称</span><span class="sxs-lookup"><span data-stu-id="212bd-118">Data Item Name</span></span>|<span data-ttu-id="212bd-119">数据项类型</span><span class="sxs-lookup"><span data-stu-id="212bd-119">Data Item Type</span></span>|<span data-ttu-id="212bd-120">说明</span><span class="sxs-lookup"><span data-stu-id="212bd-120">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="212bd-121">异常</span><span class="sxs-lookup"><span data-stu-id="212bd-121">Exception</span></span>|<span data-ttu-id="212bd-122">xs:string</span><span class="sxs-lookup"><span data-stu-id="212bd-122">xs:string</span></span>|<span data-ttu-id="212bd-123">异常的异常详细信息</span><span class="sxs-lookup"><span data-stu-id="212bd-123">The exception details for the exception</span></span>|  
|<span data-ttu-id="212bd-124">应用程序域</span><span class="sxs-lookup"><span data-stu-id="212bd-124">AppDomain</span></span>|<span data-ttu-id="212bd-125">xs:string</span><span class="sxs-lookup"><span data-stu-id="212bd-125">xs:string</span></span>|<span data-ttu-id="212bd-126">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="212bd-126">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
