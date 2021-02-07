---
description: 了解详细信息： 1103-WorkflowActivitySuspend
title: 1103 - WorkflowActivitySuspend
ms.date: 03/30/2017
ms.assetid: b64e15c2-cb2c-4314-9074-ce2c6717232e
ms.openlocfilehash: 2d46c31ee86dd39216294e6b7cd3785f2361f18b
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99667520"
---
# <a name="1103---workflowactivitysuspend"></a><span data-ttu-id="8d01f-103">1103 - WorkflowActivitySuspend</span><span class="sxs-lookup"><span data-stu-id="8d01f-103">1103 - WorkflowActivitySuspend</span></span>

## <a name="properties"></a><span data-ttu-id="8d01f-104">属性</span><span class="sxs-lookup"><span data-stu-id="8d01f-104">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="8d01f-105">ID</span><span class="sxs-lookup"><span data-stu-id="8d01f-105">ID</span></span>|<span data-ttu-id="8d01f-106">1103</span><span class="sxs-lookup"><span data-stu-id="8d01f-106">1103</span></span>|  
|<span data-ttu-id="8d01f-107">关键字</span><span class="sxs-lookup"><span data-stu-id="8d01f-107">Keywords</span></span>|<span data-ttu-id="8d01f-108">WFRuntime</span><span class="sxs-lookup"><span data-stu-id="8d01f-108">WFRuntime</span></span>|  
|<span data-ttu-id="8d01f-109">级别</span><span class="sxs-lookup"><span data-stu-id="8d01f-109">Level</span></span>|<span data-ttu-id="8d01f-110">信息</span><span class="sxs-lookup"><span data-stu-id="8d01f-110">Information</span></span>|  
|<span data-ttu-id="8d01f-111">通道</span><span class="sxs-lookup"><span data-stu-id="8d01f-111">Channel</span></span>|<span data-ttu-id="8d01f-112">Microsoft-Windows-应用程序服务器-应用程序/调试</span><span class="sxs-lookup"><span data-stu-id="8d01f-112">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="8d01f-113">说明</span><span class="sxs-lookup"><span data-stu-id="8d01f-113">Description</span></span>  

 <span data-ttu-id="8d01f-114">指示工作流活动已挂起。</span><span class="sxs-lookup"><span data-stu-id="8d01f-114">Indicates a workflow activity has been suspended.</span></span>  
  
## <a name="message"></a><span data-ttu-id="8d01f-115">消息</span><span class="sxs-lookup"><span data-stu-id="8d01f-115">Message</span></span>  

 <span data-ttu-id="8d01f-116">WorkflowInstance Id“%1”E2E 活动</span><span class="sxs-lookup"><span data-stu-id="8d01f-116">WorkflowInstance Id: '%1' E2E Activity</span></span>  
  
## <a name="details"></a><span data-ttu-id="8d01f-117">详细信息</span><span class="sxs-lookup"><span data-stu-id="8d01f-117">Details</span></span>  
  
|<span data-ttu-id="8d01f-118">数据项名称</span><span class="sxs-lookup"><span data-stu-id="8d01f-118">Data Item Name</span></span>|<span data-ttu-id="8d01f-119">数据项类型</span><span class="sxs-lookup"><span data-stu-id="8d01f-119">Data Item Type</span></span>|<span data-ttu-id="8d01f-120">说明</span><span class="sxs-lookup"><span data-stu-id="8d01f-120">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="8d01f-121">WorkflowInstanceId</span><span class="sxs-lookup"><span data-stu-id="8d01f-121">WorkflowInstanceId</span></span>|<span data-ttu-id="8d01f-122">xs:string</span><span class="sxs-lookup"><span data-stu-id="8d01f-122">xs:string</span></span>|<span data-ttu-id="8d01f-123">工作流实例 ID。</span><span class="sxs-lookup"><span data-stu-id="8d01f-123">The workflow instance id.</span></span>|  
|<span data-ttu-id="8d01f-124">应用程序域</span><span class="sxs-lookup"><span data-stu-id="8d01f-124">AppDomain</span></span>|<span data-ttu-id="8d01f-125">xs:string</span><span class="sxs-lookup"><span data-stu-id="8d01f-125">xs:string</span></span>|<span data-ttu-id="8d01f-126">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="8d01f-126">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
