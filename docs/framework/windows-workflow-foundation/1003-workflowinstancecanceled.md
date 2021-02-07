---
description: 了解详细信息： 1003-WorkflowInstanceCanceled
title: 1003 - WorkflowInstanceCanceled
ms.date: 03/30/2017
ms.assetid: 64754dc2-c160-4bf3-869a-13d56694e2dc
ms.openlocfilehash: ef7b7c6849e96866204fe53deadce8302d18e0d8
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99703362"
---
# <a name="1003---workflowinstancecanceled"></a><span data-ttu-id="a8e55-103">1003 - WorkflowInstanceCanceled</span><span class="sxs-lookup"><span data-stu-id="a8e55-103">1003 - WorkflowInstanceCanceled</span></span>

## <a name="properties"></a><span data-ttu-id="a8e55-104">属性</span><span class="sxs-lookup"><span data-stu-id="a8e55-104">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="a8e55-105">ID</span><span class="sxs-lookup"><span data-stu-id="a8e55-105">ID</span></span>|<span data-ttu-id="a8e55-106">1003</span><span class="sxs-lookup"><span data-stu-id="a8e55-106">1003</span></span>|  
|<span data-ttu-id="a8e55-107">关键字</span><span class="sxs-lookup"><span data-stu-id="a8e55-107">Keywords</span></span>|<span data-ttu-id="a8e55-108">WFRuntime</span><span class="sxs-lookup"><span data-stu-id="a8e55-108">WFRuntime</span></span>|  
|<span data-ttu-id="a8e55-109">级别</span><span class="sxs-lookup"><span data-stu-id="a8e55-109">Level</span></span>|<span data-ttu-id="a8e55-110">信息</span><span class="sxs-lookup"><span data-stu-id="a8e55-110">Information</span></span>|  
|<span data-ttu-id="a8e55-111">通道</span><span class="sxs-lookup"><span data-stu-id="a8e55-111">Channel</span></span>|<span data-ttu-id="a8e55-112">Microsoft-Windows-应用程序服务器-应用程序/调试</span><span class="sxs-lookup"><span data-stu-id="a8e55-112">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="a8e55-113">说明</span><span class="sxs-lookup"><span data-stu-id="a8e55-113">Description</span></span>  

 <span data-ttu-id="a8e55-114">指示工作流实例在“已取消”状态下完成。</span><span class="sxs-lookup"><span data-stu-id="a8e55-114">Indicates a workflow instance has completed in the Canceled state.</span></span>  
  
## <a name="message"></a><span data-ttu-id="a8e55-115">消息</span><span class="sxs-lookup"><span data-stu-id="a8e55-115">Message</span></span>  

 <span data-ttu-id="a8e55-116">WorkflowInstance Id“%1”在“已取消”状态下完成。</span><span class="sxs-lookup"><span data-stu-id="a8e55-116">WorkflowInstance Id: '%1' has completed in the Canceled state.</span></span>  
  
## <a name="details"></a><span data-ttu-id="a8e55-117">详细信息</span><span class="sxs-lookup"><span data-stu-id="a8e55-117">Details</span></span>  
  
|<span data-ttu-id="a8e55-118">数据项名称</span><span class="sxs-lookup"><span data-stu-id="a8e55-118">Data Item Name</span></span>|<span data-ttu-id="a8e55-119">数据项类型</span><span class="sxs-lookup"><span data-stu-id="a8e55-119">Data Item Type</span></span>|<span data-ttu-id="a8e55-120">说明</span><span class="sxs-lookup"><span data-stu-id="a8e55-120">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="a8e55-121">WorkflowInstanceId</span><span class="sxs-lookup"><span data-stu-id="a8e55-121">WorkflowInstanceId</span></span>|`xs:string`|<span data-ttu-id="a8e55-122">工作流的实例 ID</span><span class="sxs-lookup"><span data-stu-id="a8e55-122">The instance id for the workflow</span></span>|  
|<span data-ttu-id="a8e55-123">应用程序域</span><span class="sxs-lookup"><span data-stu-id="a8e55-123">AppDomain</span></span>|`xs:string`|<span data-ttu-id="a8e55-124">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="a8e55-124">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
