---
description: 了解详细信息： 2576-TryCatchExceptionFromTry
title: 2576 - TryCatchExceptionFromTry
ms.date: 03/30/2017
ms.assetid: 47e48973-b17c-4a16-8338-c84b54aa0a6e
ms.openlocfilehash: 83e26726377a9f8bbedda2a310dcf4ee6928d3a2
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99631512"
---
# <a name="2576---trycatchexceptionfromtry"></a><span data-ttu-id="2891f-103">2576 - TryCatchExceptionFromTry</span><span class="sxs-lookup"><span data-stu-id="2891f-103">2576 - TryCatchExceptionFromTry</span></span>

## <a name="properties"></a><span data-ttu-id="2891f-104">属性</span><span class="sxs-lookup"><span data-stu-id="2891f-104">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="2891f-105">ID</span><span class="sxs-lookup"><span data-stu-id="2891f-105">ID</span></span>|<span data-ttu-id="2891f-106">2576</span><span class="sxs-lookup"><span data-stu-id="2891f-106">2576</span></span>|  
|<span data-ttu-id="2891f-107">关键字</span><span class="sxs-lookup"><span data-stu-id="2891f-107">Keywords</span></span>|<span data-ttu-id="2891f-108">WFActivities</span><span class="sxs-lookup"><span data-stu-id="2891f-108">WFActivities</span></span>|  
|<span data-ttu-id="2891f-109">级别</span><span class="sxs-lookup"><span data-stu-id="2891f-109">Level</span></span>|<span data-ttu-id="2891f-110">信息</span><span class="sxs-lookup"><span data-stu-id="2891f-110">Information</span></span>|  
|<span data-ttu-id="2891f-111">通道</span><span class="sxs-lookup"><span data-stu-id="2891f-111">Channel</span></span>|<span data-ttu-id="2891f-112">Microsoft-Windows-应用程序服务器-应用程序/调试</span><span class="sxs-lookup"><span data-stu-id="2891f-112">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="2891f-113">说明</span><span class="sxs-lookup"><span data-stu-id="2891f-113">Description</span></span>  

 <span data-ttu-id="2891f-114">指示 TryCatch 活动捕获了异常。</span><span class="sxs-lookup"><span data-stu-id="2891f-114">Indicates the TryCatch activity has caught an exception.</span></span>  
  
## <a name="message"></a><span data-ttu-id="2891f-115">消息</span><span class="sxs-lookup"><span data-stu-id="2891f-115">Message</span></span>  

 <span data-ttu-id="2891f-116">TryCatch 活动“%1”捕获了“%2”类型的异常。</span><span class="sxs-lookup"><span data-stu-id="2891f-116">The TryCatch activity '%1' has caught an exception of type '%2'.</span></span>  
  
## <a name="details"></a><span data-ttu-id="2891f-117">详细信息</span><span class="sxs-lookup"><span data-stu-id="2891f-117">Details</span></span>  
  
|<span data-ttu-id="2891f-118">数据项名称</span><span class="sxs-lookup"><span data-stu-id="2891f-118">Data Item Name</span></span>|<span data-ttu-id="2891f-119">数据项类型</span><span class="sxs-lookup"><span data-stu-id="2891f-119">Data Item Type</span></span>|<span data-ttu-id="2891f-120">说明</span><span class="sxs-lookup"><span data-stu-id="2891f-120">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="2891f-121">DisplayName</span><span class="sxs-lookup"><span data-stu-id="2891f-121">DisplayName</span></span>|<span data-ttu-id="2891f-122">xs:string</span><span class="sxs-lookup"><span data-stu-id="2891f-122">xs:string</span></span>|<span data-ttu-id="2891f-123">活动的显示名称。</span><span class="sxs-lookup"><span data-stu-id="2891f-123">The display name of the activity.</span></span>|  
|<span data-ttu-id="2891f-124">异常</span><span class="sxs-lookup"><span data-stu-id="2891f-124">Exception</span></span>|<span data-ttu-id="2891f-125">xs:string</span><span class="sxs-lookup"><span data-stu-id="2891f-125">xs:string</span></span>|<span data-ttu-id="2891f-126">异常的类型名称。</span><span class="sxs-lookup"><span data-stu-id="2891f-126">The type name of the exception.</span></span>|  
|<span data-ttu-id="2891f-127">应用程序域</span><span class="sxs-lookup"><span data-stu-id="2891f-127">AppDomain</span></span>|<span data-ttu-id="2891f-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="2891f-128">xs:string</span></span>|<span data-ttu-id="2891f-129">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="2891f-129">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
