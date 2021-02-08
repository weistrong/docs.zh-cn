---
description: 了解详细信息： 3551-BufferOutOfOrderMessageNoBookmark
title: 3551 - BufferOutOfOrderMessageNoBookmark
ms.date: 03/30/2017
ms.assetid: 7930d6c4-c843-4a83-933a-cecd71b80d1e
ms.openlocfilehash: 573056fed1753ac55c51d9a074047e8eea15e229
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99777991"
---
# <a name="3551---bufferoutofordermessagenobookmark"></a><span data-ttu-id="db96d-103">3551 - BufferOutOfOrderMessageNoBookmark</span><span class="sxs-lookup"><span data-stu-id="db96d-103">3551 - BufferOutOfOrderMessageNoBookmark</span></span>

## <a name="properties"></a><span data-ttu-id="db96d-104">属性</span><span class="sxs-lookup"><span data-stu-id="db96d-104">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="db96d-105">ID</span><span class="sxs-lookup"><span data-stu-id="db96d-105">ID</span></span>|<span data-ttu-id="db96d-106">3551</span><span class="sxs-lookup"><span data-stu-id="db96d-106">3551</span></span>|  
|<span data-ttu-id="db96d-107">关键字</span><span class="sxs-lookup"><span data-stu-id="db96d-107">Keywords</span></span>|<span data-ttu-id="db96d-108">WFServices</span><span class="sxs-lookup"><span data-stu-id="db96d-108">WFServices</span></span>|  
|<span data-ttu-id="db96d-109">级别</span><span class="sxs-lookup"><span data-stu-id="db96d-109">Level</span></span>|<span data-ttu-id="db96d-110">信息</span><span class="sxs-lookup"><span data-stu-id="db96d-110">Information</span></span>|  
|<span data-ttu-id="db96d-111">通道</span><span class="sxs-lookup"><span data-stu-id="db96d-111">Channel</span></span>|<span data-ttu-id="db96d-112">Microsoft-Windows-应用程序服务器-应用程序/分析</span><span class="sxs-lookup"><span data-stu-id="db96d-112">Microsoft-Windows-Application Server-Applications/Analytic</span></span>|  
  
## <a name="description"></a><span data-ttu-id="db96d-113">说明</span><span class="sxs-lookup"><span data-stu-id="db96d-113">Description</span></span>  

 <span data-ttu-id="db96d-114">指示书签恢复已失败。</span><span class="sxs-lookup"><span data-stu-id="db96d-114">Indicates a bookmark resumption has failed.</span></span> <span data-ttu-id="db96d-115">服务实例准备好处理此特定操作时，将再次尝试该缓冲的接收操作。</span><span class="sxs-lookup"><span data-stu-id="db96d-115">The buffered receive operation will be attempted again when the service instance is ready to process this particular operation.</span></span>  
  
## <a name="message"></a><span data-ttu-id="db96d-116">消息</span><span class="sxs-lookup"><span data-stu-id="db96d-116">Message</span></span>  

 <span data-ttu-id="db96d-117">此时不能执行服务实例“%1”上的操作“%2”。</span><span class="sxs-lookup"><span data-stu-id="db96d-117">Operation '%2' on service instance '%1' cannot be performed at this time.</span></span> <span data-ttu-id="db96d-118">服务实例准备好处理此特定操作时，将进行另一个尝试。</span><span class="sxs-lookup"><span data-stu-id="db96d-118">Another attempt will be made when the service instance is ready to process this particular operation.</span></span>  
  
## <a name="details"></a><span data-ttu-id="db96d-119">详细信息</span><span class="sxs-lookup"><span data-stu-id="db96d-119">Details</span></span>  
  
|<span data-ttu-id="db96d-120">数据项名称</span><span class="sxs-lookup"><span data-stu-id="db96d-120">Data Item Name</span></span>|<span data-ttu-id="db96d-121">数据项类型</span><span class="sxs-lookup"><span data-stu-id="db96d-121">Data Item Type</span></span>|<span data-ttu-id="db96d-122">说明</span><span class="sxs-lookup"><span data-stu-id="db96d-122">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="db96d-123">OperationName</span><span class="sxs-lookup"><span data-stu-id="db96d-123">OperationName</span></span>|<span data-ttu-id="db96d-124">xs:string</span><span class="sxs-lookup"><span data-stu-id="db96d-124">xs:string</span></span>|<span data-ttu-id="db96d-125">操作的名称。</span><span class="sxs-lookup"><span data-stu-id="db96d-125">The name of the operation.</span></span>|  
|<span data-ttu-id="db96d-126">ServiceInstanceId</span><span class="sxs-lookup"><span data-stu-id="db96d-126">ServiceInstanceId</span></span>|<span data-ttu-id="db96d-127">xs:string</span><span class="sxs-lookup"><span data-stu-id="db96d-127">xs:string</span></span>|<span data-ttu-id="db96d-128">服务实例的 ID。</span><span class="sxs-lookup"><span data-stu-id="db96d-128">The id of the service instance.</span></span>|  
|<span data-ttu-id="db96d-129">应用程序域</span><span class="sxs-lookup"><span data-stu-id="db96d-129">AppDomain</span></span>|<span data-ttu-id="db96d-130">xs:string</span><span class="sxs-lookup"><span data-stu-id="db96d-130">xs:string</span></span>|<span data-ttu-id="db96d-131">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="db96d-131">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
