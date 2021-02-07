---
description: 了解详细信息： 1008-WorkflowApplicationUnloaded
title: 1008 - WorkflowApplicationUnloaded
ms.date: 03/30/2017
ms.assetid: a605b780-4a7e-43ab-92e7-0a3b01d053b0
ms.openlocfilehash: 5e906c0daae525accc3b8b13c907479d18f2fc8c
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99755559"
---
# <a name="1008---workflowapplicationunloaded"></a><span data-ttu-id="0d5ea-103">1008 - WorkflowApplicationUnloaded</span><span class="sxs-lookup"><span data-stu-id="0d5ea-103">1008 - WorkflowApplicationUnloaded</span></span>

## <a name="properties"></a><span data-ttu-id="0d5ea-104">属性</span><span class="sxs-lookup"><span data-stu-id="0d5ea-104">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="0d5ea-105">ID</span><span class="sxs-lookup"><span data-stu-id="0d5ea-105">ID</span></span>|<span data-ttu-id="0d5ea-106">1008</span><span class="sxs-lookup"><span data-stu-id="0d5ea-106">1008</span></span>|  
|<span data-ttu-id="0d5ea-107">关键字</span><span class="sxs-lookup"><span data-stu-id="0d5ea-107">Keywords</span></span>|<span data-ttu-id="0d5ea-108">WFRuntime</span><span class="sxs-lookup"><span data-stu-id="0d5ea-108">WFRuntime</span></span>|  
|<span data-ttu-id="0d5ea-109">级别</span><span class="sxs-lookup"><span data-stu-id="0d5ea-109">Level</span></span>|<span data-ttu-id="0d5ea-110">信息</span><span class="sxs-lookup"><span data-stu-id="0d5ea-110">Information</span></span>|  
|<span data-ttu-id="0d5ea-111">通道</span><span class="sxs-lookup"><span data-stu-id="0d5ea-111">Channel</span></span>|<span data-ttu-id="0d5ea-112">Microsoft-Windows-应用程序服务器-应用程序/调试</span><span class="sxs-lookup"><span data-stu-id="0d5ea-112">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="0d5ea-113">说明</span><span class="sxs-lookup"><span data-stu-id="0d5ea-113">Description</span></span>  

 <span data-ttu-id="0d5ea-114">指示工作流应用程序已卸载。</span><span class="sxs-lookup"><span data-stu-id="0d5ea-114">Indicates a workflow application has unloaded.</span></span>  
  
## <a name="message"></a><span data-ttu-id="0d5ea-115">消息</span><span class="sxs-lookup"><span data-stu-id="0d5ea-115">Message</span></span>  

 <span data-ttu-id="0d5ea-116">WorkflowInstance Id“%1”已卸载。</span><span class="sxs-lookup"><span data-stu-id="0d5ea-116">WorkflowInstance Id: '%1' was Unloaded.</span></span>  
  
## <a name="details"></a><span data-ttu-id="0d5ea-117">详细信息</span><span class="sxs-lookup"><span data-stu-id="0d5ea-117">Details</span></span>  
  
|<span data-ttu-id="0d5ea-118">数据项名称</span><span class="sxs-lookup"><span data-stu-id="0d5ea-118">Data Item Name</span></span>|<span data-ttu-id="0d5ea-119">数据项类型</span><span class="sxs-lookup"><span data-stu-id="0d5ea-119">Data Item Type</span></span>|<span data-ttu-id="0d5ea-120">说明</span><span class="sxs-lookup"><span data-stu-id="0d5ea-120">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="0d5ea-121">WorkflowInstanceId</span><span class="sxs-lookup"><span data-stu-id="0d5ea-121">WorkflowInstanceId</span></span>|`xs:string`|<span data-ttu-id="0d5ea-122">工作流的实例 ID</span><span class="sxs-lookup"><span data-stu-id="0d5ea-122">The instance id for the workflow</span></span>|  
|<span data-ttu-id="0d5ea-123">应用程序域</span><span class="sxs-lookup"><span data-stu-id="0d5ea-123">AppDomain</span></span>|`xs:string`|<span data-ttu-id="0d5ea-124">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="0d5ea-124">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
