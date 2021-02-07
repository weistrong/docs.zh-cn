---
description: 了解详细信息： 1036-RuntimeTransactionCompletionRequested
title: 1036 - RuntimeTransactionCompletionRequested
ms.date: 03/30/2017
ms.assetid: d36b9f44-7c0f-4083-9d3a-9034dd2b98de
ms.openlocfilehash: e07400902d5c3e08732385ab30e1be0d72d3e997
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99667884"
---
# <a name="1036---runtimetransactioncompletionrequested"></a><span data-ttu-id="b4d6b-103">1036 - RuntimeTransactionCompletionRequested</span><span class="sxs-lookup"><span data-stu-id="b4d6b-103">1036 - RuntimeTransactionCompletionRequested</span></span>

## <a name="properties"></a><span data-ttu-id="b4d6b-104">属性</span><span class="sxs-lookup"><span data-stu-id="b4d6b-104">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="b4d6b-105">ID</span><span class="sxs-lookup"><span data-stu-id="b4d6b-105">ID</span></span>|<span data-ttu-id="b4d6b-106">1036</span><span class="sxs-lookup"><span data-stu-id="b4d6b-106">1036</span></span>|  
|<span data-ttu-id="b4d6b-107">关键字</span><span class="sxs-lookup"><span data-stu-id="b4d6b-107">Keywords</span></span>|<span data-ttu-id="b4d6b-108">WFRuntime</span><span class="sxs-lookup"><span data-stu-id="b4d6b-108">WFRuntime</span></span>|  
|<span data-ttu-id="b4d6b-109">级别</span><span class="sxs-lookup"><span data-stu-id="b4d6b-109">Level</span></span>|<span data-ttu-id="b4d6b-110">“详细”</span><span class="sxs-lookup"><span data-stu-id="b4d6b-110">Verbose</span></span>|  
|<span data-ttu-id="b4d6b-111">通道</span><span class="sxs-lookup"><span data-stu-id="b4d6b-111">Channel</span></span>|<span data-ttu-id="b4d6b-112">Microsoft-Windows-应用程序服务器-应用程序/调试</span><span class="sxs-lookup"><span data-stu-id="b4d6b-112">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="b4d6b-113">说明</span><span class="sxs-lookup"><span data-stu-id="b4d6b-113">Description</span></span>  

 <span data-ttu-id="b4d6b-114">指示活动已安排了运行时事务的完成。</span><span class="sxs-lookup"><span data-stu-id="b4d6b-114">Indicates an activity has scheduled the completion of the runtime transaction.</span></span>  
  
## <a name="message"></a><span data-ttu-id="b4d6b-115">消息</span><span class="sxs-lookup"><span data-stu-id="b4d6b-115">Message</span></span>  

 <span data-ttu-id="b4d6b-116">Activity“%1”、DisplayName“%2”、InstanceId“%3”已安排了运行时事务的完成。</span><span class="sxs-lookup"><span data-stu-id="b4d6b-116">Activity '%1', DisplayName: '%2', InstanceId: '%3' has scheduled completion of the runtime transaction.</span></span>  
  
## <a name="details"></a><span data-ttu-id="b4d6b-117">详细信息</span><span class="sxs-lookup"><span data-stu-id="b4d6b-117">Details</span></span>  
  
|<span data-ttu-id="b4d6b-118">数据项名称</span><span class="sxs-lookup"><span data-stu-id="b4d6b-118">Data Item Name</span></span>|<span data-ttu-id="b4d6b-119">数据项类型</span><span class="sxs-lookup"><span data-stu-id="b4d6b-119">Data Item Type</span></span>|<span data-ttu-id="b4d6b-120">说明</span><span class="sxs-lookup"><span data-stu-id="b4d6b-120">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="b4d6b-121">活动</span><span class="sxs-lookup"><span data-stu-id="b4d6b-121">Activity</span></span>|<span data-ttu-id="b4d6b-122">xs:string</span><span class="sxs-lookup"><span data-stu-id="b4d6b-122">xs:string</span></span>|<span data-ttu-id="b4d6b-123">活动的类型名称。</span><span class="sxs-lookup"><span data-stu-id="b4d6b-123">The type name of the activity.</span></span>|  
|<span data-ttu-id="b4d6b-124">DisplayName</span><span class="sxs-lookup"><span data-stu-id="b4d6b-124">DisplayName</span></span>|<span data-ttu-id="b4d6b-125">xs:string</span><span class="sxs-lookup"><span data-stu-id="b4d6b-125">xs:string</span></span>|<span data-ttu-id="b4d6b-126">活动的显示名称。</span><span class="sxs-lookup"><span data-stu-id="b4d6b-126">The display name of the activity.</span></span>|  
|<span data-ttu-id="b4d6b-127">InstanceId</span><span class="sxs-lookup"><span data-stu-id="b4d6b-127">InstanceId</span></span>|<span data-ttu-id="b4d6b-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="b4d6b-128">xs:string</span></span>|<span data-ttu-id="b4d6b-129">活动的实例 ID。</span><span class="sxs-lookup"><span data-stu-id="b4d6b-129">The instance id of the activity.</span></span>|  
|<span data-ttu-id="b4d6b-130">应用程序域</span><span class="sxs-lookup"><span data-stu-id="b4d6b-130">AppDomain</span></span>|<span data-ttu-id="b4d6b-131">xs:string</span><span class="sxs-lookup"><span data-stu-id="b4d6b-131">xs:string</span></span>|<span data-ttu-id="b4d6b-132">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="b4d6b-132">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
