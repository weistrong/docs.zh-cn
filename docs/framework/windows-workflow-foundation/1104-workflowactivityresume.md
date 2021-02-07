---
description: 了解详细信息： 1104-WorkflowActivityResume
title: 1104 - WorkflowActivityResume
ms.date: 03/30/2017
ms.assetid: 7fe95d1e-34bd-43ca-b92e-587d2d248fff
ms.openlocfilehash: 875bbae9bdfd772cc9156cf544b7069d8d0b791f
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99667494"
---
# <a name="1104---workflowactivityresume"></a><span data-ttu-id="67f33-103">1104 - WorkflowActivityResume</span><span class="sxs-lookup"><span data-stu-id="67f33-103">1104 - WorkflowActivityResume</span></span>

## <a name="properties"></a><span data-ttu-id="67f33-104">属性</span><span class="sxs-lookup"><span data-stu-id="67f33-104">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="67f33-105">ID</span><span class="sxs-lookup"><span data-stu-id="67f33-105">ID</span></span>|<span data-ttu-id="67f33-106">1104</span><span class="sxs-lookup"><span data-stu-id="67f33-106">1104</span></span>|  
|<span data-ttu-id="67f33-107">关键字</span><span class="sxs-lookup"><span data-stu-id="67f33-107">Keywords</span></span>|<span data-ttu-id="67f33-108">WFRuntime</span><span class="sxs-lookup"><span data-stu-id="67f33-108">WFRuntime</span></span>|  
|<span data-ttu-id="67f33-109">级别</span><span class="sxs-lookup"><span data-stu-id="67f33-109">Level</span></span>|<span data-ttu-id="67f33-110">信息</span><span class="sxs-lookup"><span data-stu-id="67f33-110">Information</span></span>|  
|<span data-ttu-id="67f33-111">通道</span><span class="sxs-lookup"><span data-stu-id="67f33-111">Channel</span></span>|<span data-ttu-id="67f33-112">Microsoft-Windows-应用程序服务器-应用程序/调试</span><span class="sxs-lookup"><span data-stu-id="67f33-112">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="67f33-113">说明</span><span class="sxs-lookup"><span data-stu-id="67f33-113">Description</span></span>  

 <span data-ttu-id="67f33-114">指示工作流活动已恢复。</span><span class="sxs-lookup"><span data-stu-id="67f33-114">Indicates a workflow activity has been resumed.</span></span>  
  
## <a name="message"></a><span data-ttu-id="67f33-115">消息</span><span class="sxs-lookup"><span data-stu-id="67f33-115">Message</span></span>  

 <span data-ttu-id="67f33-116">WorkflowInstance Id“%1”E2E 活动</span><span class="sxs-lookup"><span data-stu-id="67f33-116">WorkflowInstance Id: '%1' E2E Activity</span></span>  
  
## <a name="details"></a><span data-ttu-id="67f33-117">详细信息</span><span class="sxs-lookup"><span data-stu-id="67f33-117">Details</span></span>  
  
|<span data-ttu-id="67f33-118">数据项名称</span><span class="sxs-lookup"><span data-stu-id="67f33-118">Data Item Name</span></span>|<span data-ttu-id="67f33-119">数据项类型</span><span class="sxs-lookup"><span data-stu-id="67f33-119">Data Item Type</span></span>|<span data-ttu-id="67f33-120">说明</span><span class="sxs-lookup"><span data-stu-id="67f33-120">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="67f33-121">WorkflowInstanceId</span><span class="sxs-lookup"><span data-stu-id="67f33-121">WorkflowInstanceId</span></span>|<span data-ttu-id="67f33-122">xs:string</span><span class="sxs-lookup"><span data-stu-id="67f33-122">xs:string</span></span>|<span data-ttu-id="67f33-123">工作流实例 ID。</span><span class="sxs-lookup"><span data-stu-id="67f33-123">The workflow instance id.</span></span>|  
|<span data-ttu-id="67f33-124">应用程序域</span><span class="sxs-lookup"><span data-stu-id="67f33-124">AppDomain</span></span>|<span data-ttu-id="67f33-125">xs:string</span><span class="sxs-lookup"><span data-stu-id="67f33-125">xs:string</span></span>|<span data-ttu-id="67f33-126">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="67f33-126">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
