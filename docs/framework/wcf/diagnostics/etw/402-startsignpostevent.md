---
description: 了解详细信息： 402-StartSignpostEvent
title: 402 - StartSignpostEvent
ms.date: 03/30/2017
ms.assetid: 5e5be126-765d-4ac9-88e7-008e9ef4f0e5
ms.openlocfilehash: e77cac50be2a2e96fabe1301aaeab7ff74142e5a
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99656678"
---
# <a name="402---startsignpostevent"></a><span data-ttu-id="37caf-103">402 - StartSignpostEvent</span><span class="sxs-lookup"><span data-stu-id="37caf-103">402 - StartSignpostEvent</span></span>

## <a name="properties"></a><span data-ttu-id="37caf-104">属性</span><span class="sxs-lookup"><span data-stu-id="37caf-104">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="37caf-105">ID</span><span class="sxs-lookup"><span data-stu-id="37caf-105">ID</span></span>|<span data-ttu-id="37caf-106">402</span><span class="sxs-lookup"><span data-stu-id="37caf-106">402</span></span>|  
|<span data-ttu-id="37caf-107">关键字</span><span class="sxs-lookup"><span data-stu-id="37caf-107">Keywords</span></span>|<span data-ttu-id="37caf-108">疑难解答</span><span class="sxs-lookup"><span data-stu-id="37caf-108">Troubleshooting</span></span>|  
|<span data-ttu-id="37caf-109">级别</span><span class="sxs-lookup"><span data-stu-id="37caf-109">Level</span></span>|<span data-ttu-id="37caf-110">信息</span><span class="sxs-lookup"><span data-stu-id="37caf-110">Information</span></span>|  
|<span data-ttu-id="37caf-111">通道</span><span class="sxs-lookup"><span data-stu-id="37caf-111">Channel</span></span>|<span data-ttu-id="37caf-112">Microsoft-Windows-应用程序服务器-应用程序/分析</span><span class="sxs-lookup"><span data-stu-id="37caf-112">Microsoft-Windows-Application Server-Applications/Analytic</span></span>|  
  
## <a name="description"></a><span data-ttu-id="37caf-113">说明</span><span class="sxs-lookup"><span data-stu-id="37caf-113">Description</span></span>  

 <span data-ttu-id="37caf-114">此事件标记端对端活动的开始。</span><span class="sxs-lookup"><span data-stu-id="37caf-114">This event marks the beginning of an end-to-end activity.</span></span> <span data-ttu-id="37caf-115">它包含活动的名称。</span><span class="sxs-lookup"><span data-stu-id="37caf-115">It contains the name of the activity.</span></span>  
  
## <a name="message"></a><span data-ttu-id="37caf-116">消息</span><span class="sxs-lookup"><span data-stu-id="37caf-116">Message</span></span>  

 <span data-ttu-id="37caf-117">活动边界。</span><span class="sxs-lookup"><span data-stu-id="37caf-117">Activity boundary.</span></span>  
  
## <a name="details"></a><span data-ttu-id="37caf-118">详细信息</span><span class="sxs-lookup"><span data-stu-id="37caf-118">Details</span></span>  
  
|<span data-ttu-id="37caf-119">数据项名称</span><span class="sxs-lookup"><span data-stu-id="37caf-119">Data Item Name</span></span>|<span data-ttu-id="37caf-120">数据项类型</span><span class="sxs-lookup"><span data-stu-id="37caf-120">Data Item Type</span></span>|<span data-ttu-id="37caf-121">说明</span><span class="sxs-lookup"><span data-stu-id="37caf-121">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="37caf-122">扩展数据</span><span class="sxs-lookup"><span data-stu-id="37caf-122">Extended Data</span></span>|`xs:string`|<span data-ttu-id="37caf-123">活动的名称。</span><span class="sxs-lookup"><span data-stu-id="37caf-123">The name of the activity.</span></span>|  
|<span data-ttu-id="37caf-124">应用程序域</span><span class="sxs-lookup"><span data-stu-id="37caf-124">AppDomain</span></span>|`xs:string`|<span data-ttu-id="37caf-125">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="37caf-125">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
