---
description: 了解详细信息： 1041-WorkflowApplicationPersistableIdle
title: 1041 - WorkflowApplicationPersistableIdle
ms.date: 03/30/2017
ms.assetid: 966adf2f-e21d-44df-a3ec-a8e285e0a316
ms.openlocfilehash: eb004077a36ed3e78229df92a73972ed5feda665
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99667754"
---
# <a name="1041---workflowapplicationpersistableidle"></a><span data-ttu-id="fa19d-103">1041 - WorkflowApplicationPersistableIdle</span><span class="sxs-lookup"><span data-stu-id="fa19d-103">1041 - WorkflowApplicationPersistableIdle</span></span>

## <a name="properties"></a><span data-ttu-id="fa19d-104">属性</span><span class="sxs-lookup"><span data-stu-id="fa19d-104">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="fa19d-105">ID</span><span class="sxs-lookup"><span data-stu-id="fa19d-105">ID</span></span>|<span data-ttu-id="fa19d-106">1041</span><span class="sxs-lookup"><span data-stu-id="fa19d-106">1041</span></span>|  
|<span data-ttu-id="fa19d-107">关键字</span><span class="sxs-lookup"><span data-stu-id="fa19d-107">Keywords</span></span>|<span data-ttu-id="fa19d-108">WFRuntime</span><span class="sxs-lookup"><span data-stu-id="fa19d-108">WFRuntime</span></span>|  
|<span data-ttu-id="fa19d-109">级别</span><span class="sxs-lookup"><span data-stu-id="fa19d-109">Level</span></span>|<span data-ttu-id="fa19d-110">信息</span><span class="sxs-lookup"><span data-stu-id="fa19d-110">Information</span></span>|  
|<span data-ttu-id="fa19d-111">通道</span><span class="sxs-lookup"><span data-stu-id="fa19d-111">Channel</span></span>|<span data-ttu-id="fa19d-112">Microsoft-Windows-应用程序服务器-应用程序/调试</span><span class="sxs-lookup"><span data-stu-id="fa19d-112">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="fa19d-113">说明</span><span class="sxs-lookup"><span data-stu-id="fa19d-113">Description</span></span>  

 <span data-ttu-id="fa19d-114">指示工作流应用程序空闲且可持久化。</span><span class="sxs-lookup"><span data-stu-id="fa19d-114">Indicates that a workflow application is idle and persistable.</span></span> <span data-ttu-id="fa19d-115">工作流应用程序将是空闲且可持久化的。</span><span class="sxs-lookup"><span data-stu-id="fa19d-115">The workflow application will be idled or persisted.</span></span>  
  
## <a name="message"></a><span data-ttu-id="fa19d-116">消息</span><span class="sxs-lookup"><span data-stu-id="fa19d-116">Message</span></span>  

 <span data-ttu-id="fa19d-117">WorkflowApplication Id "%1" 处于空闲和可持久状态。</span><span class="sxs-lookup"><span data-stu-id="fa19d-117">WorkflowApplication Id: '%1' is idle and persistable.</span></span>  <span data-ttu-id="fa19d-118">将执行以下操作： %2。</span><span class="sxs-lookup"><span data-stu-id="fa19d-118">The following action will be taken: %2.</span></span>  
  
## <a name="details"></a><span data-ttu-id="fa19d-119">详细信息</span><span class="sxs-lookup"><span data-stu-id="fa19d-119">Details</span></span>  
  
|<span data-ttu-id="fa19d-120">数据项名称</span><span class="sxs-lookup"><span data-stu-id="fa19d-120">Data Item Name</span></span>|<span data-ttu-id="fa19d-121">数据项类型</span><span class="sxs-lookup"><span data-stu-id="fa19d-121">Data Item Type</span></span>|<span data-ttu-id="fa19d-122">说明</span><span class="sxs-lookup"><span data-stu-id="fa19d-122">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="fa19d-123">WorkflowApplicationId</span><span class="sxs-lookup"><span data-stu-id="fa19d-123">WorkflowApplicationId</span></span>|<span data-ttu-id="fa19d-124">xs:string</span><span class="sxs-lookup"><span data-stu-id="fa19d-124">xs:string</span></span>|<span data-ttu-id="fa19d-125">工作流应用程序 ID</span><span class="sxs-lookup"><span data-stu-id="fa19d-125">The workflow application id</span></span>|  
|<span data-ttu-id="fa19d-126">ActionTaken</span><span class="sxs-lookup"><span data-stu-id="fa19d-126">ActionTaken</span></span>|<span data-ttu-id="fa19d-127">xs:string</span><span class="sxs-lookup"><span data-stu-id="fa19d-127">xs:string</span></span>|<span data-ttu-id="fa19d-128">将对工作流应用程序执行的操作。</span><span class="sxs-lookup"><span data-stu-id="fa19d-128">The action that will be taken on the workflow application.</span></span>|  
|<span data-ttu-id="fa19d-129">应用程序域</span><span class="sxs-lookup"><span data-stu-id="fa19d-129">AppDomain</span></span>|<span data-ttu-id="fa19d-130">xs:string</span><span class="sxs-lookup"><span data-stu-id="fa19d-130">xs:string</span></span>|<span data-ttu-id="fa19d-131">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="fa19d-131">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
