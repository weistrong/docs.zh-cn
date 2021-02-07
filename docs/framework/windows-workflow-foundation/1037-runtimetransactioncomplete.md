---
description: 了解详细信息： 1037-RuntimeTransactionComplete
title: 1037 - RuntimeTransactionComplete
ms.date: 03/30/2017
ms.assetid: 2c8c31e0-42a9-4f46-865b-2da9ab16a0ba
ms.openlocfilehash: 5784dc1b0eede5ddad0e6aae4cb79c6e859f325e
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99667858"
---
# <a name="1037---runtimetransactioncomplete"></a><span data-ttu-id="0f212-103">1037 - RuntimeTransactionComplete</span><span class="sxs-lookup"><span data-stu-id="0f212-103">1037 - RuntimeTransactionComplete</span></span>

## <a name="properties"></a><span data-ttu-id="0f212-104">属性</span><span class="sxs-lookup"><span data-stu-id="0f212-104">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="0f212-105">ID</span><span class="sxs-lookup"><span data-stu-id="0f212-105">ID</span></span>|<span data-ttu-id="0f212-106">1037</span><span class="sxs-lookup"><span data-stu-id="0f212-106">1037</span></span>|  
|<span data-ttu-id="0f212-107">关键字</span><span class="sxs-lookup"><span data-stu-id="0f212-107">Keywords</span></span>|<span data-ttu-id="0f212-108">WFRuntime</span><span class="sxs-lookup"><span data-stu-id="0f212-108">WFRuntime</span></span>|  
|<span data-ttu-id="0f212-109">级别</span><span class="sxs-lookup"><span data-stu-id="0f212-109">Level</span></span>|<span data-ttu-id="0f212-110">“详细”</span><span class="sxs-lookup"><span data-stu-id="0f212-110">Verbose</span></span>|  
|<span data-ttu-id="0f212-111">通道</span><span class="sxs-lookup"><span data-stu-id="0f212-111">Channel</span></span>|<span data-ttu-id="0f212-112">Microsoft-Windows-应用程序服务器-应用程序/调试</span><span class="sxs-lookup"><span data-stu-id="0f212-112">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="0f212-113">说明</span><span class="sxs-lookup"><span data-stu-id="0f212-113">Description</span></span>  

 <span data-ttu-id="0f212-114">指示运行时事务已完成。</span><span class="sxs-lookup"><span data-stu-id="0f212-114">Indicates the runtime transaction has completed.</span></span>  
  
## <a name="message"></a><span data-ttu-id="0f212-115">消息</span><span class="sxs-lookup"><span data-stu-id="0f212-115">Message</span></span>  

 <span data-ttu-id="0f212-116">运行时事务已完成，状态为“%1”。</span><span class="sxs-lookup"><span data-stu-id="0f212-116">The runtime transaction has completed with the state '%1'.</span></span>  
  
## <a name="details"></a><span data-ttu-id="0f212-117">详细信息</span><span class="sxs-lookup"><span data-stu-id="0f212-117">Details</span></span>  
  
|<span data-ttu-id="0f212-118">数据项名称</span><span class="sxs-lookup"><span data-stu-id="0f212-118">Data Item Name</span></span>|<span data-ttu-id="0f212-119">数据项类型</span><span class="sxs-lookup"><span data-stu-id="0f212-119">Data Item Type</span></span>|<span data-ttu-id="0f212-120">说明</span><span class="sxs-lookup"><span data-stu-id="0f212-120">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="0f212-121">状态</span><span class="sxs-lookup"><span data-stu-id="0f212-121">State</span></span>|<span data-ttu-id="0f212-122">xs:string</span><span class="sxs-lookup"><span data-stu-id="0f212-122">xs:string</span></span>|<span data-ttu-id="0f212-123">事务的状态。</span><span class="sxs-lookup"><span data-stu-id="0f212-123">The state of the transaction.</span></span>|  
|<span data-ttu-id="0f212-124">应用程序域</span><span class="sxs-lookup"><span data-stu-id="0f212-124">AppDomain</span></span>|<span data-ttu-id="0f212-125">xs:string</span><span class="sxs-lookup"><span data-stu-id="0f212-125">xs:string</span></span>|<span data-ttu-id="0f212-126">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="0f212-126">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
