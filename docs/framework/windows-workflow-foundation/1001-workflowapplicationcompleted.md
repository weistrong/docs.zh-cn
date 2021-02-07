---
description: 了解详细信息： 1001-WorkflowApplicationCompleted
title: 1001 - WorkflowApplicationCompleted
ms.date: 03/30/2017
ms.assetid: 7a2ab59a-cf66-437a-b01e-f8f7268a3f7a
ms.openlocfilehash: d32028bbe582f4a1e31796ed1f75e41c651e6c59
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99755637"
---
# <a name="1001---workflowapplicationcompleted"></a><span data-ttu-id="fc6a8-103">1001 - WorkflowApplicationCompleted</span><span class="sxs-lookup"><span data-stu-id="fc6a8-103">1001 - WorkflowApplicationCompleted</span></span>

## <a name="properties"></a><span data-ttu-id="fc6a8-104">属性</span><span class="sxs-lookup"><span data-stu-id="fc6a8-104">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="fc6a8-105">ID</span><span class="sxs-lookup"><span data-stu-id="fc6a8-105">ID</span></span>|<span data-ttu-id="fc6a8-106">1001</span><span class="sxs-lookup"><span data-stu-id="fc6a8-106">1001</span></span>|  
|<span data-ttu-id="fc6a8-107">关键字</span><span class="sxs-lookup"><span data-stu-id="fc6a8-107">Keywords</span></span>|<span data-ttu-id="fc6a8-108">WFRuntime</span><span class="sxs-lookup"><span data-stu-id="fc6a8-108">WFRuntime</span></span>|  
|<span data-ttu-id="fc6a8-109">级别</span><span class="sxs-lookup"><span data-stu-id="fc6a8-109">Level</span></span>|<span data-ttu-id="fc6a8-110">信息</span><span class="sxs-lookup"><span data-stu-id="fc6a8-110">Information</span></span>|  
|<span data-ttu-id="fc6a8-111">通道</span><span class="sxs-lookup"><span data-stu-id="fc6a8-111">Channel</span></span>|<span data-ttu-id="fc6a8-112">Microsoft-Windows-应用程序服务器-应用程序/调试</span><span class="sxs-lookup"><span data-stu-id="fc6a8-112">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="fc6a8-113">说明</span><span class="sxs-lookup"><span data-stu-id="fc6a8-113">Description</span></span>  

 <span data-ttu-id="fc6a8-114">指示工作流应用程序在“已关闭”状态下完成。</span><span class="sxs-lookup"><span data-stu-id="fc6a8-114">Indicates a workflow application has completed in the Closed state.</span></span>  
  
## <a name="message"></a><span data-ttu-id="fc6a8-115">消息</span><span class="sxs-lookup"><span data-stu-id="fc6a8-115">Message</span></span>  

 <span data-ttu-id="fc6a8-116">WorkflowInstance Id“%1”在“已关闭”状态下完成。</span><span class="sxs-lookup"><span data-stu-id="fc6a8-116">WorkflowInstance Id: '%1' has completed in the Closed state.</span></span>  
  
## <a name="details"></a><span data-ttu-id="fc6a8-117">详细信息</span><span class="sxs-lookup"><span data-stu-id="fc6a8-117">Details</span></span>  
  
|<span data-ttu-id="fc6a8-118">数据项名称</span><span class="sxs-lookup"><span data-stu-id="fc6a8-118">Data Item Name</span></span>|<span data-ttu-id="fc6a8-119">数据项类型</span><span class="sxs-lookup"><span data-stu-id="fc6a8-119">Data Item Type</span></span>|<span data-ttu-id="fc6a8-120">说明</span><span class="sxs-lookup"><span data-stu-id="fc6a8-120">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="fc6a8-121">WorkflowInstanceId</span><span class="sxs-lookup"><span data-stu-id="fc6a8-121">WorkflowInstanceId</span></span>|`xs:string`|<span data-ttu-id="fc6a8-122">工作流的实例 ID</span><span class="sxs-lookup"><span data-stu-id="fc6a8-122">The instance id for the workflow</span></span>|  
|<span data-ttu-id="fc6a8-123">应用程序域</span><span class="sxs-lookup"><span data-stu-id="fc6a8-123">AppDomain</span></span>|`xs:string`|<span data-ttu-id="fc6a8-124">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="fc6a8-124">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
