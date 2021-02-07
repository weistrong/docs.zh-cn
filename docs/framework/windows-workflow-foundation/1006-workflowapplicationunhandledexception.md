---
description: 了解详细信息： 1006-WorkflowApplicationUnhandledException
title: 1006 - WorkflowApplicationUnhandledException
ms.date: 03/30/2017
ms.assetid: dfe0f316-e03b-47fb-b6a3-622c56bfd753
ms.openlocfilehash: bfccd0d12c5dac4caad1e84e95f1cd096a551aa0
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99755585"
---
# <a name="1006---workflowapplicationunhandledexception"></a><span data-ttu-id="95e95-103">1006 - WorkflowApplicationUnhandledException</span><span class="sxs-lookup"><span data-stu-id="95e95-103">1006 - WorkflowApplicationUnhandledException</span></span>

## <a name="properties"></a><span data-ttu-id="95e95-104">属性</span><span class="sxs-lookup"><span data-stu-id="95e95-104">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="95e95-105">ID</span><span class="sxs-lookup"><span data-stu-id="95e95-105">ID</span></span>|<span data-ttu-id="95e95-106">1006</span><span class="sxs-lookup"><span data-stu-id="95e95-106">1006</span></span>|  
|<span data-ttu-id="95e95-107">关键字</span><span class="sxs-lookup"><span data-stu-id="95e95-107">Keywords</span></span>|<span data-ttu-id="95e95-108">WFRuntime</span><span class="sxs-lookup"><span data-stu-id="95e95-108">WFRuntime</span></span>|  
|<span data-ttu-id="95e95-109">级别</span><span class="sxs-lookup"><span data-stu-id="95e95-109">Level</span></span>|<span data-ttu-id="95e95-110">错误</span><span class="sxs-lookup"><span data-stu-id="95e95-110">Error</span></span>|  
|<span data-ttu-id="95e95-111">通道</span><span class="sxs-lookup"><span data-stu-id="95e95-111">Channel</span></span>|<span data-ttu-id="95e95-112">Microsoft-Windows-应用程序服务器-应用程序/调试</span><span class="sxs-lookup"><span data-stu-id="95e95-112">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="95e95-113">说明</span><span class="sxs-lookup"><span data-stu-id="95e95-113">Description</span></span>  

 <span data-ttu-id="95e95-114">指示工作流应用程序遇到了未经处理的异常。</span><span class="sxs-lookup"><span data-stu-id="95e95-114">Indicates a workflow application has encountered an unhandled exception.</span></span>  
  
## <a name="message"></a><span data-ttu-id="95e95-115">消息</span><span class="sxs-lookup"><span data-stu-id="95e95-115">Message</span></span>  

 <span data-ttu-id="95e95-116">WorkflowInstance Id "%1" 遇到未经处理的异常。</span><span class="sxs-lookup"><span data-stu-id="95e95-116">WorkflowInstance Id: '%1' has encountered an unhandled exception.</span></span>  <span data-ttu-id="95e95-117">此异常源自 Activity "%2"、DisplayName "%3"。</span><span class="sxs-lookup"><span data-stu-id="95e95-117">The exception originated from Activity '%2', DisplayName: '%3'.</span></span>  <span data-ttu-id="95e95-118">将执行以下操作： %4。</span><span class="sxs-lookup"><span data-stu-id="95e95-118">The following action will be taken: %4.</span></span>  
  
## <a name="details"></a><span data-ttu-id="95e95-119">详细信息</span><span class="sxs-lookup"><span data-stu-id="95e95-119">Details</span></span>  
  
|<span data-ttu-id="95e95-120">数据项名称</span><span class="sxs-lookup"><span data-stu-id="95e95-120">Data Item Name</span></span>|<span data-ttu-id="95e95-121">数据项类型</span><span class="sxs-lookup"><span data-stu-id="95e95-121">Data Item Type</span></span>|<span data-ttu-id="95e95-122">说明</span><span class="sxs-lookup"><span data-stu-id="95e95-122">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="95e95-123">WorkflowInstanceId</span><span class="sxs-lookup"><span data-stu-id="95e95-123">WorkflowInstanceId</span></span>|`xs:string`|<span data-ttu-id="95e95-124">工作流的实例 ID</span><span class="sxs-lookup"><span data-stu-id="95e95-124">The instance id for the workflow</span></span>|  
|<span data-ttu-id="95e95-125">异常</span><span class="sxs-lookup"><span data-stu-id="95e95-125">Exception</span></span>|`xs:string`|<span data-ttu-id="95e95-126">异常的异常详细信息</span><span class="sxs-lookup"><span data-stu-id="95e95-126">The exception details for the exception</span></span>|  
|<span data-ttu-id="95e95-127">应用程序域</span><span class="sxs-lookup"><span data-stu-id="95e95-127">AppDomain</span></span>|`xs:string`|<span data-ttu-id="95e95-128">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="95e95-128">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
