---
description: 了解详细信息： 3557-TransactedReceiveScopeEndCommitFailed
title: 3557 - TransactedReceiveScopeEndCommitFailed
ms.date: 03/30/2017
ms.assetid: 079f0188-8146-49ee-b6ae-a08f4e4d2b9b
ms.openlocfilehash: 7865ae27e7ce5b3f13b3567f3f8aeebd6edf3fd4
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99777978"
---
# <a name="3557---transactedreceivescopeendcommitfailed"></a><span data-ttu-id="841ad-103">3557 - TransactedReceiveScopeEndCommitFailed</span><span class="sxs-lookup"><span data-stu-id="841ad-103">3557 - TransactedReceiveScopeEndCommitFailed</span></span>

## <a name="properties"></a><span data-ttu-id="841ad-104">属性</span><span class="sxs-lookup"><span data-stu-id="841ad-104">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="841ad-105">ID</span><span class="sxs-lookup"><span data-stu-id="841ad-105">ID</span></span>|<span data-ttu-id="841ad-106">3557</span><span class="sxs-lookup"><span data-stu-id="841ad-106">3557</span></span>|  
|<span data-ttu-id="841ad-107">关键字</span><span class="sxs-lookup"><span data-stu-id="841ad-107">Keywords</span></span>|<span data-ttu-id="841ad-108">WFServices</span><span class="sxs-lookup"><span data-stu-id="841ad-108">WFServices</span></span>|  
|<span data-ttu-id="841ad-109">级别</span><span class="sxs-lookup"><span data-stu-id="841ad-109">Level</span></span>|<span data-ttu-id="841ad-110">信息</span><span class="sxs-lookup"><span data-stu-id="841ad-110">Information</span></span>|  
|<span data-ttu-id="841ad-111">通道</span><span class="sxs-lookup"><span data-stu-id="841ad-111">Channel</span></span>|<span data-ttu-id="841ad-112">Microsoft-Windows-应用程序服务器-应用程序/分析</span><span class="sxs-lookup"><span data-stu-id="841ad-112">Microsoft-Windows-Application Server-Applications/Analytic</span></span>|  
  
## <a name="description"></a><span data-ttu-id="841ad-113">说明</span><span class="sxs-lookup"><span data-stu-id="841ad-113">Description</span></span>  

 <span data-ttu-id="841ad-114">指示对 CommittableTransaction 上的 EndCommit 的调用引发 TransactionException。</span><span class="sxs-lookup"><span data-stu-id="841ad-114">Indicates the call to EndCommit on a CommittableTransaction threw a TransactionException.</span></span>  
  
## <a name="message"></a><span data-ttu-id="841ad-115">消息</span><span class="sxs-lookup"><span data-stu-id="841ad-115">Message</span></span>  

 <span data-ttu-id="841ad-116">ID 为“%1”的 CommittableTransaction 上的 EndCommit 调用引发了具有以下消息的 TransactionException:“%2”。</span><span class="sxs-lookup"><span data-stu-id="841ad-116">The call to EndCommit on the CommittableTransaction with id = '%1' threw a TransactionException with the following message: '%2'.</span></span>  
  
## <a name="details"></a><span data-ttu-id="841ad-117">详细信息</span><span class="sxs-lookup"><span data-stu-id="841ad-117">Details</span></span>  
  
|<span data-ttu-id="841ad-118">数据项名称</span><span class="sxs-lookup"><span data-stu-id="841ad-118">Data Item Name</span></span>|<span data-ttu-id="841ad-119">数据项类型</span><span class="sxs-lookup"><span data-stu-id="841ad-119">Data Item Type</span></span>|<span data-ttu-id="841ad-120">说明</span><span class="sxs-lookup"><span data-stu-id="841ad-120">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="841ad-121">TransactionId</span><span class="sxs-lookup"><span data-stu-id="841ad-121">TransactionId</span></span>|<span data-ttu-id="841ad-122">xs:string</span><span class="sxs-lookup"><span data-stu-id="841ad-122">xs:string</span></span>|<span data-ttu-id="841ad-123">CommittableTransaction 的 ID。</span><span class="sxs-lookup"><span data-stu-id="841ad-123">The id of the CommittableTransaction.</span></span>|  
|<span data-ttu-id="841ad-124">异常</span><span class="sxs-lookup"><span data-stu-id="841ad-124">Exception</span></span>|<span data-ttu-id="841ad-125">xs:string</span><span class="sxs-lookup"><span data-stu-id="841ad-125">xs:string</span></span>|<span data-ttu-id="841ad-126">异常的异常详细信息</span><span class="sxs-lookup"><span data-stu-id="841ad-126">The exception details for the exception</span></span>|  
|<span data-ttu-id="841ad-127">应用程序域</span><span class="sxs-lookup"><span data-stu-id="841ad-127">AppDomain</span></span>|<span data-ttu-id="841ad-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="841ad-128">xs:string</span></span>|<span data-ttu-id="841ad-129">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="841ad-129">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
