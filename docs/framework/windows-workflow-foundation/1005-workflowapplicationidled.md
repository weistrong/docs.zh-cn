---
description: 了解详细信息： 1005-WorkflowApplicationIdled
title: 1005 - WorkflowApplicationIdled
ms.date: 03/30/2017
ms.assetid: 74d77dfa-f20d-4fe9-a6ae-e6d1b5fe4182
ms.openlocfilehash: ee8d0b7ff2155333213a718a04c3966024fda89d
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99755598"
---
# <a name="1005---workflowapplicationidled"></a><span data-ttu-id="0eb1a-103">1005 - WorkflowApplicationIdled</span><span class="sxs-lookup"><span data-stu-id="0eb1a-103">1005 - WorkflowApplicationIdled</span></span>

## <a name="properties"></a><span data-ttu-id="0eb1a-104">属性</span><span class="sxs-lookup"><span data-stu-id="0eb1a-104">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="0eb1a-105">ID</span><span class="sxs-lookup"><span data-stu-id="0eb1a-105">ID</span></span>|<span data-ttu-id="0eb1a-106">1005</span><span class="sxs-lookup"><span data-stu-id="0eb1a-106">1005</span></span>|  
|<span data-ttu-id="0eb1a-107">关键字</span><span class="sxs-lookup"><span data-stu-id="0eb1a-107">Keywords</span></span>|<span data-ttu-id="0eb1a-108">WFRuntime</span><span class="sxs-lookup"><span data-stu-id="0eb1a-108">WFRuntime</span></span>|  
|<span data-ttu-id="0eb1a-109">级别</span><span class="sxs-lookup"><span data-stu-id="0eb1a-109">Level</span></span>|<span data-ttu-id="0eb1a-110">信息</span><span class="sxs-lookup"><span data-stu-id="0eb1a-110">Information</span></span>|  
|<span data-ttu-id="0eb1a-111">通道</span><span class="sxs-lookup"><span data-stu-id="0eb1a-111">Channel</span></span>|<span data-ttu-id="0eb1a-112">Microsoft-Windows-应用程序服务器-应用程序/调试</span><span class="sxs-lookup"><span data-stu-id="0eb1a-112">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="0eb1a-113">说明</span><span class="sxs-lookup"><span data-stu-id="0eb1a-113">Description</span></span>  

 <span data-ttu-id="0eb1a-114">指示工作流应用程序已处于空闲状态。</span><span class="sxs-lookup"><span data-stu-id="0eb1a-114">Indicates a workflow application has idled.</span></span>  
  
## <a name="message"></a><span data-ttu-id="0eb1a-115">消息</span><span class="sxs-lookup"><span data-stu-id="0eb1a-115">Message</span></span>  

 <span data-ttu-id="0eb1a-116">WorkflowApplication ID“%1”变为空闲状态。</span><span class="sxs-lookup"><span data-stu-id="0eb1a-116">WorkflowApplication Id: '%1' went idle.</span></span>  
  
## <a name="details"></a><span data-ttu-id="0eb1a-117">详细信息</span><span class="sxs-lookup"><span data-stu-id="0eb1a-117">Details</span></span>  
  
|<span data-ttu-id="0eb1a-118">数据项名称</span><span class="sxs-lookup"><span data-stu-id="0eb1a-118">Data Item Name</span></span>|<span data-ttu-id="0eb1a-119">数据项类型</span><span class="sxs-lookup"><span data-stu-id="0eb1a-119">Data Item Type</span></span>|<span data-ttu-id="0eb1a-120">说明</span><span class="sxs-lookup"><span data-stu-id="0eb1a-120">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="0eb1a-121">WorkflowInstanceId</span><span class="sxs-lookup"><span data-stu-id="0eb1a-121">WorkflowInstanceId</span></span>|`xs:string`|<span data-ttu-id="0eb1a-122">工作流应用程序 ID</span><span class="sxs-lookup"><span data-stu-id="0eb1a-122">The workflow application id</span></span>|  
|<span data-ttu-id="0eb1a-123">应用程序域</span><span class="sxs-lookup"><span data-stu-id="0eb1a-123">AppDomain</span></span>|`xs:string`|<span data-ttu-id="0eb1a-124">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="0eb1a-124">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
