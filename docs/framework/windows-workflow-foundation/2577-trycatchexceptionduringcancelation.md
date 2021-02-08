---
description: 了解详细信息： 2577-TryCatchExceptionDuringCancelation
title: 2577 - TryCatchExceptionDuringCancelation
ms.date: 03/30/2017
ms.assetid: 35ee9f55-227f-4566-bcb4-4c7c75dea85b
ms.openlocfilehash: e02e7722dadfe38b9fc1fbb92e809ae8f80cbd2f
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99778095"
---
# <a name="2577---trycatchexceptionduringcancelation"></a><span data-ttu-id="70cf8-103">2577 - TryCatchExceptionDuringCancelation</span><span class="sxs-lookup"><span data-stu-id="70cf8-103">2577 - TryCatchExceptionDuringCancelation</span></span>

## <a name="properties"></a><span data-ttu-id="70cf8-104">属性</span><span class="sxs-lookup"><span data-stu-id="70cf8-104">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="70cf8-105">ID</span><span class="sxs-lookup"><span data-stu-id="70cf8-105">ID</span></span>|<span data-ttu-id="70cf8-106">2577</span><span class="sxs-lookup"><span data-stu-id="70cf8-106">2577</span></span>|  
|<span data-ttu-id="70cf8-107">关键字</span><span class="sxs-lookup"><span data-stu-id="70cf8-107">Keywords</span></span>|<span data-ttu-id="70cf8-108">WFActivities</span><span class="sxs-lookup"><span data-stu-id="70cf8-108">WFActivities</span></span>|  
|<span data-ttu-id="70cf8-109">级别</span><span class="sxs-lookup"><span data-stu-id="70cf8-109">Level</span></span>|<span data-ttu-id="70cf8-110">警告</span><span class="sxs-lookup"><span data-stu-id="70cf8-110">Warning</span></span>|  
|<span data-ttu-id="70cf8-111">通道</span><span class="sxs-lookup"><span data-stu-id="70cf8-111">Channel</span></span>|<span data-ttu-id="70cf8-112">Microsoft-Windows-应用程序服务器-应用程序/调试</span><span class="sxs-lookup"><span data-stu-id="70cf8-112">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="70cf8-113">说明</span><span class="sxs-lookup"><span data-stu-id="70cf8-113">Description</span></span>  

 <span data-ttu-id="70cf8-114">支持 TryCatch 活动的子活动在取消过程中引发了异常。</span><span class="sxs-lookup"><span data-stu-id="70cf8-114">Indicates a child activity of the TryCatch activity has thrown an exception during cancelation.</span></span>  
  
## <a name="message"></a><span data-ttu-id="70cf8-115">消息</span><span class="sxs-lookup"><span data-stu-id="70cf8-115">Message</span></span>  

 <span data-ttu-id="70cf8-116">TryCatch 活动“%1”的子活动在取消过程中引发了异常。</span><span class="sxs-lookup"><span data-stu-id="70cf8-116">A child activity of the TryCatch activity '%1' has thrown an exception during cancelation.</span></span>  
  
## <a name="details"></a><span data-ttu-id="70cf8-117">详细信息</span><span class="sxs-lookup"><span data-stu-id="70cf8-117">Details</span></span>  
  
|<span data-ttu-id="70cf8-118">数据项名称</span><span class="sxs-lookup"><span data-stu-id="70cf8-118">Data Item Name</span></span>|<span data-ttu-id="70cf8-119">数据项类型</span><span class="sxs-lookup"><span data-stu-id="70cf8-119">Data Item Type</span></span>|<span data-ttu-id="70cf8-120">说明</span><span class="sxs-lookup"><span data-stu-id="70cf8-120">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="70cf8-121">DisplayName</span><span class="sxs-lookup"><span data-stu-id="70cf8-121">DisplayName</span></span>|<span data-ttu-id="70cf8-122">xs:string</span><span class="sxs-lookup"><span data-stu-id="70cf8-122">xs:string</span></span>|<span data-ttu-id="70cf8-123">活动的显示名称。</span><span class="sxs-lookup"><span data-stu-id="70cf8-123">The display name of the activity.</span></span>|  
|<span data-ttu-id="70cf8-124">应用程序域</span><span class="sxs-lookup"><span data-stu-id="70cf8-124">AppDomain</span></span>|<span data-ttu-id="70cf8-125">xs:string</span><span class="sxs-lookup"><span data-stu-id="70cf8-125">xs:string</span></span>|<span data-ttu-id="70cf8-126">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="70cf8-126">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
