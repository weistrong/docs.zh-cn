---
description: 了解详细信息： 440-StartSignpostEvent1
title: 440 - StartSignpostEvent1
ms.date: 03/30/2017
ms.assetid: 27b551b5-ae76-49f8-bab8-6300009eb4c1
ms.openlocfilehash: 462ad54c9dd8230632d76d88f2b779eaea3b43ee
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99720366"
---
# <a name="440---startsignpostevent1"></a><span data-ttu-id="8cbd8-103">440 - StartSignpostEvent1</span><span class="sxs-lookup"><span data-stu-id="8cbd8-103">440 - StartSignpostEvent1</span></span>

## <a name="properties"></a><span data-ttu-id="8cbd8-104">属性</span><span class="sxs-lookup"><span data-stu-id="8cbd8-104">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="8cbd8-105">ID</span><span class="sxs-lookup"><span data-stu-id="8cbd8-105">ID</span></span>|<span data-ttu-id="8cbd8-106">440</span><span class="sxs-lookup"><span data-stu-id="8cbd8-106">440</span></span>|  
|<span data-ttu-id="8cbd8-107">关键字</span><span class="sxs-lookup"><span data-stu-id="8cbd8-107">Keywords</span></span>|<span data-ttu-id="8cbd8-108">疑难解答</span><span class="sxs-lookup"><span data-stu-id="8cbd8-108">Troubleshooting</span></span>|  
|<span data-ttu-id="8cbd8-109">级别</span><span class="sxs-lookup"><span data-stu-id="8cbd8-109">Level</span></span>|<span data-ttu-id="8cbd8-110">信息</span><span class="sxs-lookup"><span data-stu-id="8cbd8-110">Information</span></span>|  
|<span data-ttu-id="8cbd8-111">通道</span><span class="sxs-lookup"><span data-stu-id="8cbd8-111">Channel</span></span>|<span data-ttu-id="8cbd8-112">Microsoft-Windows-应用程序服务器-应用程序/分析</span><span class="sxs-lookup"><span data-stu-id="8cbd8-112">Microsoft-Windows-Application Server-Applications/Analytic</span></span>|  
  
## <a name="description"></a><span data-ttu-id="8cbd8-113">说明</span><span class="sxs-lookup"><span data-stu-id="8cbd8-113">Description</span></span>  

 <span data-ttu-id="8cbd8-114">在活动跟踪中，指示消息是否已开始跨越发送或接收中的活动边界。</span><span class="sxs-lookup"><span data-stu-id="8cbd8-114">In activity tracing, indicates a message has started crossing an activity boundary in send or receive.</span></span>  
  
## <a name="message"></a><span data-ttu-id="8cbd8-115">消息</span><span class="sxs-lookup"><span data-stu-id="8cbd8-115">Message</span></span>  

 <span data-ttu-id="8cbd8-116">活动边界。</span><span class="sxs-lookup"><span data-stu-id="8cbd8-116">Activity boundary.</span></span>  
  
## <a name="details"></a><span data-ttu-id="8cbd8-117">详细信息</span><span class="sxs-lookup"><span data-stu-id="8cbd8-117">Details</span></span>  
  
|<span data-ttu-id="8cbd8-118">数据项名称</span><span class="sxs-lookup"><span data-stu-id="8cbd8-118">Data Item Name</span></span>|<span data-ttu-id="8cbd8-119">数据项类型</span><span class="sxs-lookup"><span data-stu-id="8cbd8-119">Data Item Type</span></span>|<span data-ttu-id="8cbd8-120">说明</span><span class="sxs-lookup"><span data-stu-id="8cbd8-120">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="8cbd8-121">ExtendedData</span><span class="sxs-lookup"><span data-stu-id="8cbd8-121">ExtendedData</span></span>|`xs:string`|<span data-ttu-id="8cbd8-122">活动的名称。</span><span class="sxs-lookup"><span data-stu-id="8cbd8-122">The name of the activity.</span></span>|  
|<span data-ttu-id="8cbd8-123">应用程序域</span><span class="sxs-lookup"><span data-stu-id="8cbd8-123">AppDomain</span></span>|`xs:string`|<span data-ttu-id="8cbd8-124">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="8cbd8-124">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
