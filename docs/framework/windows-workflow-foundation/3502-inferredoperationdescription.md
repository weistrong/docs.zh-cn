---
description: 了解详细信息： 3502-InferredOperationDescription
title: 3502 - InferredOperationDescription
ms.date: 03/30/2017
ms.assetid: 6aebb614-3c72-4537-ba11-3cc7200ef1f1
ms.openlocfilehash: 5068a3553484b38242951ef985886190f8027035
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99631484"
---
# <a name="3502---inferredoperationdescription"></a><span data-ttu-id="f7ec2-103">3502 - InferredOperationDescription</span><span class="sxs-lookup"><span data-stu-id="f7ec2-103">3502 - InferredOperationDescription</span></span>

## <a name="properties"></a><span data-ttu-id="f7ec2-104">属性</span><span class="sxs-lookup"><span data-stu-id="f7ec2-104">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="f7ec2-105">ID</span><span class="sxs-lookup"><span data-stu-id="f7ec2-105">ID</span></span>|<span data-ttu-id="f7ec2-106">3502</span><span class="sxs-lookup"><span data-stu-id="f7ec2-106">3502</span></span>|  
|<span data-ttu-id="f7ec2-107">关键字</span><span class="sxs-lookup"><span data-stu-id="f7ec2-107">Keywords</span></span>|<span data-ttu-id="f7ec2-108">WFServices</span><span class="sxs-lookup"><span data-stu-id="f7ec2-108">WFServices</span></span>|  
|<span data-ttu-id="f7ec2-109">级别</span><span class="sxs-lookup"><span data-stu-id="f7ec2-109">Level</span></span>|<span data-ttu-id="f7ec2-110">信息</span><span class="sxs-lookup"><span data-stu-id="f7ec2-110">Information</span></span>|  
|<span data-ttu-id="f7ec2-111">通道</span><span class="sxs-lookup"><span data-stu-id="f7ec2-111">Channel</span></span>|<span data-ttu-id="f7ec2-112">Microsoft-Windows-应用程序服务器-应用程序/分析</span><span class="sxs-lookup"><span data-stu-id="f7ec2-112">Microsoft-Windows-Application Server-Applications/Analytic</span></span>|  
  
## <a name="description"></a><span data-ttu-id="f7ec2-113">说明</span><span class="sxs-lookup"><span data-stu-id="f7ec2-113">Description</span></span>  

 <span data-ttu-id="f7ec2-114">指示已从 WorkflowService 中推断出 OperationDescription。</span><span class="sxs-lookup"><span data-stu-id="f7ec2-114">Indicates an OperationDescription has been inferred from WorkflowService.</span></span>  
  
## <a name="message"></a><span data-ttu-id="f7ec2-115">消息</span><span class="sxs-lookup"><span data-stu-id="f7ec2-115">Message</span></span>  

 <span data-ttu-id="f7ec2-116">已从 WorkflowService 中推断出协定“%2”中含有 Name='%1' 的 OperationDescription。</span><span class="sxs-lookup"><span data-stu-id="f7ec2-116">OperationDescription with Name='%1' in contract '%2' has been inferred from WorkflowService.</span></span> <span data-ttu-id="f7ec2-117">IsOneWay=%3。</span><span class="sxs-lookup"><span data-stu-id="f7ec2-117">IsOneWay=%3.</span></span>  
  
## <a name="details"></a><span data-ttu-id="f7ec2-118">详细信息</span><span class="sxs-lookup"><span data-stu-id="f7ec2-118">Details</span></span>  
  
|<span data-ttu-id="f7ec2-119">数据项名称</span><span class="sxs-lookup"><span data-stu-id="f7ec2-119">Data Item Name</span></span>|<span data-ttu-id="f7ec2-120">数据项类型</span><span class="sxs-lookup"><span data-stu-id="f7ec2-120">Data Item Type</span></span>|<span data-ttu-id="f7ec2-121">说明</span><span class="sxs-lookup"><span data-stu-id="f7ec2-121">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="f7ec2-122">OperationName</span><span class="sxs-lookup"><span data-stu-id="f7ec2-122">OperationName</span></span>|<span data-ttu-id="f7ec2-123">xs:string</span><span class="sxs-lookup"><span data-stu-id="f7ec2-123">xs:string</span></span>|<span data-ttu-id="f7ec2-124">操作的名称。</span><span class="sxs-lookup"><span data-stu-id="f7ec2-124">The name of the operation.</span></span>|  
|<span data-ttu-id="f7ec2-125">ContractName</span><span class="sxs-lookup"><span data-stu-id="f7ec2-125">ContractName</span></span>|<span data-ttu-id="f7ec2-126">xs:string</span><span class="sxs-lookup"><span data-stu-id="f7ec2-126">xs:string</span></span>|<span data-ttu-id="f7ec2-127">协定的名称。</span><span class="sxs-lookup"><span data-stu-id="f7ec2-127">The name of the contract.</span></span>|  
|<span data-ttu-id="f7ec2-128">IsOneWay</span><span class="sxs-lookup"><span data-stu-id="f7ec2-128">IsOneWay</span></span>|<span data-ttu-id="f7ec2-129">xs:string</span><span class="sxs-lookup"><span data-stu-id="f7ec2-129">xs:string</span></span>|<span data-ttu-id="f7ec2-130">true 或 false 指示协定是否为单向。</span><span class="sxs-lookup"><span data-stu-id="f7ec2-130">True or False indicating if the contract is one-way.</span></span>|  
|<span data-ttu-id="f7ec2-131">应用程序域</span><span class="sxs-lookup"><span data-stu-id="f7ec2-131">AppDomain</span></span>|<span data-ttu-id="f7ec2-132">xs:string</span><span class="sxs-lookup"><span data-stu-id="f7ec2-132">xs:string</span></span>|<span data-ttu-id="f7ec2-133">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="f7ec2-133">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
