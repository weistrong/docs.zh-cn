---
description: 了解详细信息： 2578-TryCatchExceptionFromCatchOrFinally
title: 2578 - TryCatchExceptionFromCatchOrFinally
ms.date: 03/30/2017
ms.assetid: 4803fee6-b8d8-4937-9907-d5c5fd5299db
ms.openlocfilehash: 7a159d096307d3354695d831db168990be18a236
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99631497"
---
# <a name="2578---trycatchexceptionfromcatchorfinally"></a><span data-ttu-id="8faa7-103">2578 - TryCatchExceptionFromCatchOrFinally</span><span class="sxs-lookup"><span data-stu-id="8faa7-103">2578 - TryCatchExceptionFromCatchOrFinally</span></span>

## <a name="properties"></a><span data-ttu-id="8faa7-104">属性</span><span class="sxs-lookup"><span data-stu-id="8faa7-104">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="8faa7-105">ID</span><span class="sxs-lookup"><span data-stu-id="8faa7-105">ID</span></span>|<span data-ttu-id="8faa7-106">2578</span><span class="sxs-lookup"><span data-stu-id="8faa7-106">2578</span></span>|  
|<span data-ttu-id="8faa7-107">关键字</span><span class="sxs-lookup"><span data-stu-id="8faa7-107">Keywords</span></span>|<span data-ttu-id="8faa7-108">WFActivities</span><span class="sxs-lookup"><span data-stu-id="8faa7-108">WFActivities</span></span>|  
|<span data-ttu-id="8faa7-109">级别</span><span class="sxs-lookup"><span data-stu-id="8faa7-109">Level</span></span>|<span data-ttu-id="8faa7-110">警告</span><span class="sxs-lookup"><span data-stu-id="8faa7-110">Warning</span></span>|  
|<span data-ttu-id="8faa7-111">通道</span><span class="sxs-lookup"><span data-stu-id="8faa7-111">Channel</span></span>|<span data-ttu-id="8faa7-112">Microsoft-Windows-应用程序服务器-应用程序/调试</span><span class="sxs-lookup"><span data-stu-id="8faa7-112">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="8faa7-113">说明</span><span class="sxs-lookup"><span data-stu-id="8faa7-113">Description</span></span>  

 <span data-ttu-id="8faa7-114">指示 Catch 或 Finally 活动引发了异常。</span><span class="sxs-lookup"><span data-stu-id="8faa7-114">Indicates a Catch or Finally activity has thrown an exception.</span></span>  
  
## <a name="message"></a><span data-ttu-id="8faa7-115">消息</span><span class="sxs-lookup"><span data-stu-id="8faa7-115">Message</span></span>  

 <span data-ttu-id="8faa7-116">与 TryCatch 活动“%1”关联的 Catch 或 Finally 活动引发了异常。</span><span class="sxs-lookup"><span data-stu-id="8faa7-116">A Catch or Finally activity that is associated with the TryCatch activity '%1' has thrown an exception.</span></span>  
  
## <a name="details"></a><span data-ttu-id="8faa7-117">详细信息</span><span class="sxs-lookup"><span data-stu-id="8faa7-117">Details</span></span>  
  
|<span data-ttu-id="8faa7-118">数据项名称</span><span class="sxs-lookup"><span data-stu-id="8faa7-118">Data Item Name</span></span>|<span data-ttu-id="8faa7-119">数据项类型</span><span class="sxs-lookup"><span data-stu-id="8faa7-119">Data Item Type</span></span>|<span data-ttu-id="8faa7-120">说明</span><span class="sxs-lookup"><span data-stu-id="8faa7-120">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="8faa7-121">DisplayName</span><span class="sxs-lookup"><span data-stu-id="8faa7-121">DisplayName</span></span>|<span data-ttu-id="8faa7-122">xs:string</span><span class="sxs-lookup"><span data-stu-id="8faa7-122">xs:string</span></span>|<span data-ttu-id="8faa7-123">活动的显示名称。</span><span class="sxs-lookup"><span data-stu-id="8faa7-123">The display name of the activity.</span></span>|  
|<span data-ttu-id="8faa7-124">应用程序域</span><span class="sxs-lookup"><span data-stu-id="8faa7-124">AppDomain</span></span>|<span data-ttu-id="8faa7-125">xs:string</span><span class="sxs-lookup"><span data-stu-id="8faa7-125">xs:string</span></span>|<span data-ttu-id="8faa7-126">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="8faa7-126">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
