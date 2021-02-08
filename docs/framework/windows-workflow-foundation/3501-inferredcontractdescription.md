---
description: 了解详细信息： 3501-InferredContractDescription
title: 3501 - InferredContractDescription
ms.date: 03/30/2017
ms.assetid: 21a70849-4fc0-41d2-b9a4-db5aa2acdf1a
ms.openlocfilehash: 2eab180780a1475bff421441b7cef23f58f627c6
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99778082"
---
# <a name="3501---inferredcontractdescription"></a><span data-ttu-id="278ea-103">3501 - InferredContractDescription</span><span class="sxs-lookup"><span data-stu-id="278ea-103">3501 - InferredContractDescription</span></span>

## <a name="properties"></a><span data-ttu-id="278ea-104">属性</span><span class="sxs-lookup"><span data-stu-id="278ea-104">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="278ea-105">ID</span><span class="sxs-lookup"><span data-stu-id="278ea-105">ID</span></span>|<span data-ttu-id="278ea-106">3501</span><span class="sxs-lookup"><span data-stu-id="278ea-106">3501</span></span>|  
|<span data-ttu-id="278ea-107">关键字</span><span class="sxs-lookup"><span data-stu-id="278ea-107">Keywords</span></span>|<span data-ttu-id="278ea-108">WFServices</span><span class="sxs-lookup"><span data-stu-id="278ea-108">WFServices</span></span>|  
|<span data-ttu-id="278ea-109">级别</span><span class="sxs-lookup"><span data-stu-id="278ea-109">Level</span></span>|<span data-ttu-id="278ea-110">信息</span><span class="sxs-lookup"><span data-stu-id="278ea-110">Information</span></span>|  
|<span data-ttu-id="278ea-111">通道</span><span class="sxs-lookup"><span data-stu-id="278ea-111">Channel</span></span>|<span data-ttu-id="278ea-112">Microsoft-Windows-应用程序服务器-应用程序/分析</span><span class="sxs-lookup"><span data-stu-id="278ea-112">Microsoft-Windows-Application Server-Applications/Analytic</span></span>|  
  
## <a name="description"></a><span data-ttu-id="278ea-113">说明</span><span class="sxs-lookup"><span data-stu-id="278ea-113">Description</span></span>  

 <span data-ttu-id="278ea-114">指示已从 WorkflowService 中推断出 ContractDescription。</span><span class="sxs-lookup"><span data-stu-id="278ea-114">Indicates a ContractDescription has been inferred from WorkflowService.</span></span>  
  
## <a name="message"></a><span data-ttu-id="278ea-115">消息</span><span class="sxs-lookup"><span data-stu-id="278ea-115">Message</span></span>  

 <span data-ttu-id="278ea-116">已从 WorkflowService 中推断出含有 Name 为“%1”和 Namespace 为“%2”的 ContractDescription。</span><span class="sxs-lookup"><span data-stu-id="278ea-116">ContractDescription with Name='%1' and Namespace='%2' has been inferred from WorkflowService.</span></span>  
  
## <a name="details"></a><span data-ttu-id="278ea-117">详细信息</span><span class="sxs-lookup"><span data-stu-id="278ea-117">Details</span></span>  
  
|<span data-ttu-id="278ea-118">数据项名称</span><span class="sxs-lookup"><span data-stu-id="278ea-118">Data Item Name</span></span>|<span data-ttu-id="278ea-119">数据项类型</span><span class="sxs-lookup"><span data-stu-id="278ea-119">Data Item Type</span></span>|<span data-ttu-id="278ea-120">说明</span><span class="sxs-lookup"><span data-stu-id="278ea-120">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="278ea-121">名称</span><span class="sxs-lookup"><span data-stu-id="278ea-121">Name</span></span>|<span data-ttu-id="278ea-122">xs:string</span><span class="sxs-lookup"><span data-stu-id="278ea-122">xs:string</span></span>|<span data-ttu-id="278ea-123">ContractDescription 的名称。</span><span class="sxs-lookup"><span data-stu-id="278ea-123">The name of the ContractDescription.</span></span>|  
|<span data-ttu-id="278ea-124">命名空间</span><span class="sxs-lookup"><span data-stu-id="278ea-124">Namespace</span></span>|<span data-ttu-id="278ea-125">xs:string</span><span class="sxs-lookup"><span data-stu-id="278ea-125">xs:string</span></span>|<span data-ttu-id="278ea-126">ContractDescription 的命名空间。</span><span class="sxs-lookup"><span data-stu-id="278ea-126">The namespace of the ContractDescription.</span></span>|  
|<span data-ttu-id="278ea-127">应用程序域</span><span class="sxs-lookup"><span data-stu-id="278ea-127">AppDomain</span></span>|<span data-ttu-id="278ea-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="278ea-128">xs:string</span></span>|<span data-ttu-id="278ea-129">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="278ea-129">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
