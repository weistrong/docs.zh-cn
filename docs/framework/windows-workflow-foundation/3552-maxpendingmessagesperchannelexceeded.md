---
description: 了解详细信息： 3552-MaxPendingMessagesPerChannelExceeded
title: 3552 - MaxPendingMessagesPerChannelExceeded
ms.date: 03/30/2017
ms.assetid: fc8309d9-eb3a-4636-a6f0-dd0018c1361d
ms.openlocfilehash: 5fb2d27f7d68716cebf2cfaafd21851226a456e6
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99631432"
---
# <a name="3552---maxpendingmessagesperchannelexceeded"></a><span data-ttu-id="1682c-103">3552 - MaxPendingMessagesPerChannelExceeded</span><span class="sxs-lookup"><span data-stu-id="1682c-103">3552 - MaxPendingMessagesPerChannelExceeded</span></span>

## <a name="properties"></a><span data-ttu-id="1682c-104">属性</span><span class="sxs-lookup"><span data-stu-id="1682c-104">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="1682c-105">ID</span><span class="sxs-lookup"><span data-stu-id="1682c-105">ID</span></span>|<span data-ttu-id="1682c-106">3552</span><span class="sxs-lookup"><span data-stu-id="1682c-106">3552</span></span>|  
|<span data-ttu-id="1682c-107">关键字</span><span class="sxs-lookup"><span data-stu-id="1682c-107">Keywords</span></span>|<span data-ttu-id="1682c-108">配额、WFServices</span><span class="sxs-lookup"><span data-stu-id="1682c-108">Quota, WFServices</span></span>|  
|<span data-ttu-id="1682c-109">级别</span><span class="sxs-lookup"><span data-stu-id="1682c-109">Level</span></span>|<span data-ttu-id="1682c-110">警告</span><span class="sxs-lookup"><span data-stu-id="1682c-110">Warning</span></span>|  
|<span data-ttu-id="1682c-111">通道</span><span class="sxs-lookup"><span data-stu-id="1682c-111">Channel</span></span>|<span data-ttu-id="1682c-112">Microsoft-Windows-应用程序服务器-应用程序/分析</span><span class="sxs-lookup"><span data-stu-id="1682c-112">Microsoft-Windows-Application Server-Applications/Analytic</span></span>|  
  
## <a name="description"></a><span data-ttu-id="1682c-113">说明</span><span class="sxs-lookup"><span data-stu-id="1682c-113">Description</span></span>  

 <span data-ttu-id="1682c-114">指示达到了中止值“MaxPendingMessagesPerChannel”。</span><span class="sxs-lookup"><span data-stu-id="1682c-114">Indicates the throttle 'MaxPendingMessagesPerChannel' limit was hit.</span></span>  
  
## <a name="message"></a><span data-ttu-id="1682c-115">消息</span><span class="sxs-lookup"><span data-stu-id="1682c-115">Message</span></span>  

 <span data-ttu-id="1682c-116">达到了“%1”的中止值“MaxPendingMessagesPerChannel”。</span><span class="sxs-lookup"><span data-stu-id="1682c-116">The throttle 'MaxPendingMessagesPerChannel' limit of  '%1' was hit.</span></span> <span data-ttu-id="1682c-117">若要增加此限制，请调整 BufferedReceiveServiceBehavior 中的 MaxPendingMessagesPerChannel 属性。</span><span class="sxs-lookup"><span data-stu-id="1682c-117">To increase this limit, adjust the MaxPendingMessagesPerChannel property on BufferedReceiveServiceBehavior.</span></span>  
  
## <a name="details"></a><span data-ttu-id="1682c-118">详细信息</span><span class="sxs-lookup"><span data-stu-id="1682c-118">Details</span></span>  
  
|<span data-ttu-id="1682c-119">数据项名称</span><span class="sxs-lookup"><span data-stu-id="1682c-119">Data Item Name</span></span>|<span data-ttu-id="1682c-120">数据项类型</span><span class="sxs-lookup"><span data-stu-id="1682c-120">Data Item Type</span></span>|<span data-ttu-id="1682c-121">说明</span><span class="sxs-lookup"><span data-stu-id="1682c-121">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="1682c-122">限制</span><span class="sxs-lookup"><span data-stu-id="1682c-122">Limit</span></span>|<span data-ttu-id="1682c-123">xs:string</span><span class="sxs-lookup"><span data-stu-id="1682c-123">xs:string</span></span>|<span data-ttu-id="1682c-124">中止值 MaxPendingMessagesPerChannel。</span><span class="sxs-lookup"><span data-stu-id="1682c-124">The limit of the MaxPendingMessagesPerChannel throttle.</span></span>|  
|<span data-ttu-id="1682c-125">应用程序域</span><span class="sxs-lookup"><span data-stu-id="1682c-125">AppDomain</span></span>|<span data-ttu-id="1682c-126">xs:string</span><span class="sxs-lookup"><span data-stu-id="1682c-126">xs:string</span></span>|<span data-ttu-id="1682c-127">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="1682c-127">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
