---
description: 了解详细信息： 3503-DuplicateCorrelationQuery
title: 3503 - DuplicateCorrelationQuery
ms.date: 03/30/2017
ms.assetid: b857f8e6-ce4d-4da4-bc9d-6cd63fa558a4
ms.openlocfilehash: a8e1e41aad3aa1b273d8f8a5d7b0768fabe4e658
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99778069"
---
# <a name="3503---duplicatecorrelationquery"></a><span data-ttu-id="450b4-103">3503 - DuplicateCorrelationQuery</span><span class="sxs-lookup"><span data-stu-id="450b4-103">3503 - DuplicateCorrelationQuery</span></span>

## <a name="properties"></a><span data-ttu-id="450b4-104">属性</span><span class="sxs-lookup"><span data-stu-id="450b4-104">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="450b4-105">ID</span><span class="sxs-lookup"><span data-stu-id="450b4-105">ID</span></span>|<span data-ttu-id="450b4-106">3503</span><span class="sxs-lookup"><span data-stu-id="450b4-106">3503</span></span>|  
|<span data-ttu-id="450b4-107">关键字</span><span class="sxs-lookup"><span data-stu-id="450b4-107">Keywords</span></span>|<span data-ttu-id="450b4-108">WFServices</span><span class="sxs-lookup"><span data-stu-id="450b4-108">WFServices</span></span>|  
|<span data-ttu-id="450b4-109">级别</span><span class="sxs-lookup"><span data-stu-id="450b4-109">Level</span></span>|<span data-ttu-id="450b4-110">警告</span><span class="sxs-lookup"><span data-stu-id="450b4-110">Warning</span></span>|  
|<span data-ttu-id="450b4-111">通道</span><span class="sxs-lookup"><span data-stu-id="450b4-111">Channel</span></span>|<span data-ttu-id="450b4-112">Microsoft-Windows-应用程序服务器-应用程序/分析</span><span class="sxs-lookup"><span data-stu-id="450b4-112">Microsoft-Windows-Application Server-Applications/Analytic</span></span>|  
  
## <a name="description"></a><span data-ttu-id="450b4-113">说明</span><span class="sxs-lookup"><span data-stu-id="450b4-113">Description</span></span>  

 <span data-ttu-id="450b4-114">指示找到了重复 CorrelationQuery。</span><span class="sxs-lookup"><span data-stu-id="450b4-114">Indicates a duplicate CorrelationQuery was found.</span></span> <span data-ttu-id="450b4-115">计算相关性时将不使用重复查询。</span><span class="sxs-lookup"><span data-stu-id="450b4-115">The duplicate query will not be used when calculating correlation.</span></span>  
  
## <a name="message"></a><span data-ttu-id="450b4-116">消息</span><span class="sxs-lookup"><span data-stu-id="450b4-116">Message</span></span>  

 <span data-ttu-id="450b4-117">找到了含有 Where='%1' 的重复 CorrelationQuery。</span><span class="sxs-lookup"><span data-stu-id="450b4-117">A duplicate CorrelationQuery was found with Where='%1'.</span></span> <span data-ttu-id="450b4-118">计算相关性时将不使用此重复查询。</span><span class="sxs-lookup"><span data-stu-id="450b4-118">This duplicate query will not be used when calculating correlation.</span></span>  
  
## <a name="details"></a><span data-ttu-id="450b4-119">详细信息</span><span class="sxs-lookup"><span data-stu-id="450b4-119">Details</span></span>  
  
|<span data-ttu-id="450b4-120">数据项名称</span><span class="sxs-lookup"><span data-stu-id="450b4-120">Data Item Name</span></span>|<span data-ttu-id="450b4-121">数据项类型</span><span class="sxs-lookup"><span data-stu-id="450b4-121">Data Item Type</span></span>|<span data-ttu-id="450b4-122">说明</span><span class="sxs-lookup"><span data-stu-id="450b4-122">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="450b4-123">其中</span><span class="sxs-lookup"><span data-stu-id="450b4-123">Where</span></span>|<span data-ttu-id="450b4-124">xs:string</span><span class="sxs-lookup"><span data-stu-id="450b4-124">xs:string</span></span>|<span data-ttu-id="450b4-125">相关查询的 Where 部分。</span><span class="sxs-lookup"><span data-stu-id="450b4-125">The Where portion of the correlation query.</span></span>|  
|<span data-ttu-id="450b4-126">应用程序域</span><span class="sxs-lookup"><span data-stu-id="450b4-126">AppDomain</span></span>|<span data-ttu-id="450b4-127">xs:string</span><span class="sxs-lookup"><span data-stu-id="450b4-127">xs:string</span></span>|<span data-ttu-id="450b4-128">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="450b4-128">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
