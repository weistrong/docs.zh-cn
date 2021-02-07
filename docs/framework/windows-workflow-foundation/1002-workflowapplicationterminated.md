---
description: 了解详细信息： 1002-WorkflowApplicationTerminated
title: 1002 - WorkflowApplicationTerminated
ms.date: 03/30/2017
ms.assetid: 4e8b111f-79dc-4898-bb4a-e9b36f69420f
ms.openlocfilehash: 8ceef41515231833767fc7e2095ab3850bf80e41
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99755617"
---
# <a name="1002---workflowapplicationterminated"></a><span data-ttu-id="5b0ee-103">1002 - WorkflowApplicationTerminated</span><span class="sxs-lookup"><span data-stu-id="5b0ee-103">1002 - WorkflowApplicationTerminated</span></span>

## <a name="properties"></a><span data-ttu-id="5b0ee-104">属性</span><span class="sxs-lookup"><span data-stu-id="5b0ee-104">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="5b0ee-105">ID</span><span class="sxs-lookup"><span data-stu-id="5b0ee-105">ID</span></span>|<span data-ttu-id="5b0ee-106">1002</span><span class="sxs-lookup"><span data-stu-id="5b0ee-106">1002</span></span>|  
|<span data-ttu-id="5b0ee-107">关键字</span><span class="sxs-lookup"><span data-stu-id="5b0ee-107">Keywords</span></span>|<span data-ttu-id="5b0ee-108">WFRuntime</span><span class="sxs-lookup"><span data-stu-id="5b0ee-108">WFRuntime</span></span>|  
|<span data-ttu-id="5b0ee-109">级别</span><span class="sxs-lookup"><span data-stu-id="5b0ee-109">Level</span></span>|<span data-ttu-id="5b0ee-110">信息</span><span class="sxs-lookup"><span data-stu-id="5b0ee-110">Information</span></span>|  
|<span data-ttu-id="5b0ee-111">通道</span><span class="sxs-lookup"><span data-stu-id="5b0ee-111">Channel</span></span>|<span data-ttu-id="5b0ee-112">Microsoft-Windows-应用程序服务器-应用程序/调试</span><span class="sxs-lookup"><span data-stu-id="5b0ee-112">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="5b0ee-113">说明</span><span class="sxs-lookup"><span data-stu-id="5b0ee-113">Description</span></span>  

 <span data-ttu-id="5b0ee-114">指示工作流应用程序因出现异常而在“出错”状态下终止。</span><span class="sxs-lookup"><span data-stu-id="5b0ee-114">Indicates a workflow application has terminated in the Faulted state with an exception.</span></span>  
  
## <a name="message"></a><span data-ttu-id="5b0ee-115">消息</span><span class="sxs-lookup"><span data-stu-id="5b0ee-115">Message</span></span>  

 <span data-ttu-id="5b0ee-116">WorkflowApplication Id“%1”已终止。</span><span class="sxs-lookup"><span data-stu-id="5b0ee-116">WorkflowApplication Id: '%1' was terminated.</span></span> <span data-ttu-id="5b0ee-117">该应用程序因出现异常而在“出错”状态下完成。</span><span class="sxs-lookup"><span data-stu-id="5b0ee-117">It has completed in the Faulted state with an exception.</span></span>  
  
## <a name="details"></a><span data-ttu-id="5b0ee-118">详细信息</span><span class="sxs-lookup"><span data-stu-id="5b0ee-118">Details</span></span>  
  
|<span data-ttu-id="5b0ee-119">数据项名称</span><span class="sxs-lookup"><span data-stu-id="5b0ee-119">Data Item Name</span></span>|<span data-ttu-id="5b0ee-120">数据项类型</span><span class="sxs-lookup"><span data-stu-id="5b0ee-120">Data Item Type</span></span>|<span data-ttu-id="5b0ee-121">说明</span><span class="sxs-lookup"><span data-stu-id="5b0ee-121">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="5b0ee-122">WorkflowApplicationId</span><span class="sxs-lookup"><span data-stu-id="5b0ee-122">WorkflowApplicationId</span></span>|`xs:string`|<span data-ttu-id="5b0ee-123">工作流应用程序 ID</span><span class="sxs-lookup"><span data-stu-id="5b0ee-123">The workflow application id</span></span>|  
|<span data-ttu-id="5b0ee-124">异常</span><span class="sxs-lookup"><span data-stu-id="5b0ee-124">Exception</span></span>|`xs:string`|<span data-ttu-id="5b0ee-125">异常的异常详细信息</span><span class="sxs-lookup"><span data-stu-id="5b0ee-125">The exception details for the exception</span></span>|  
|<span data-ttu-id="5b0ee-126">应用程序域</span><span class="sxs-lookup"><span data-stu-id="5b0ee-126">AppDomain</span></span>|`xs:string`|<span data-ttu-id="5b0ee-127">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="5b0ee-127">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
