---
description: 了解详细信息： 1126-InvokedMethodThrewException
title: 1126 - InvokedMethodThrewException
ms.date: 03/30/2017
ms.assetid: 0d3cff1a-97e6-4b6c-be18-108c6881bfc0
ms.openlocfilehash: 35c4311a4ab7750cc54a5c9ffb379f34b1cb12aa
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99667351"
---
# <a name="1126---invokedmethodthrewexception"></a><span data-ttu-id="3c92e-103">1126 - InvokedMethodThrewException</span><span class="sxs-lookup"><span data-stu-id="3c92e-103">1126 - InvokedMethodThrewException</span></span>

## <a name="properties"></a><span data-ttu-id="3c92e-104">属性</span><span class="sxs-lookup"><span data-stu-id="3c92e-104">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="3c92e-105">ID</span><span class="sxs-lookup"><span data-stu-id="3c92e-105">ID</span></span>|<span data-ttu-id="3c92e-106">1126</span><span class="sxs-lookup"><span data-stu-id="3c92e-106">1126</span></span>|  
|<span data-ttu-id="3c92e-107">关键字</span><span class="sxs-lookup"><span data-stu-id="3c92e-107">Keywords</span></span>|<span data-ttu-id="3c92e-108">WFRuntime</span><span class="sxs-lookup"><span data-stu-id="3c92e-108">WFRuntime</span></span>|  
|<span data-ttu-id="3c92e-109">级别</span><span class="sxs-lookup"><span data-stu-id="3c92e-109">Level</span></span>|<span data-ttu-id="3c92e-110">信息</span><span class="sxs-lookup"><span data-stu-id="3c92e-110">Information</span></span>|  
|<span data-ttu-id="3c92e-111">通道</span><span class="sxs-lookup"><span data-stu-id="3c92e-111">Channel</span></span>|<span data-ttu-id="3c92e-112">Microsoft-Windows-应用程序服务器-应用程序/调试</span><span class="sxs-lookup"><span data-stu-id="3c92e-112">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="3c92e-113">说明</span><span class="sxs-lookup"><span data-stu-id="3c92e-113">Description</span></span>  

 <span data-ttu-id="3c92e-114">指示 InvokeMethod 活动调用的方法引发了异常。</span><span class="sxs-lookup"><span data-stu-id="3c92e-114">Indicates an exception was thrown by the method called by the InvokeMethod activity.</span></span>  
  
## <a name="message"></a><span data-ttu-id="3c92e-115">消息</span><span class="sxs-lookup"><span data-stu-id="3c92e-115">Message</span></span>  

 <span data-ttu-id="3c92e-116">在活动“%1”调用的方法中，引发了异常。</span><span class="sxs-lookup"><span data-stu-id="3c92e-116">An exception was thrown in the method called by the activity '%1'.</span></span> <span data-ttu-id="3c92e-117">%2</span><span class="sxs-lookup"><span data-stu-id="3c92e-117">%2</span></span>  
  
## <a name="details"></a><span data-ttu-id="3c92e-118">详细信息</span><span class="sxs-lookup"><span data-stu-id="3c92e-118">Details</span></span>  
  
|<span data-ttu-id="3c92e-119">数据项名称</span><span class="sxs-lookup"><span data-stu-id="3c92e-119">Data Item Name</span></span>|<span data-ttu-id="3c92e-120">数据项类型</span><span class="sxs-lookup"><span data-stu-id="3c92e-120">Data Item Type</span></span>|<span data-ttu-id="3c92e-121">说明</span><span class="sxs-lookup"><span data-stu-id="3c92e-121">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="3c92e-122">InvokeMethod</span><span class="sxs-lookup"><span data-stu-id="3c92e-122">InvokeMethod</span></span>|<span data-ttu-id="3c92e-123">xs:string</span><span class="sxs-lookup"><span data-stu-id="3c92e-123">xs:string</span></span>|<span data-ttu-id="3c92e-124">InvokeMethod 活动的显示名称。</span><span class="sxs-lookup"><span data-stu-id="3c92e-124">The display name of the InvokeMethod activity.</span></span>|  
|<span data-ttu-id="3c92e-125">异常</span><span class="sxs-lookup"><span data-stu-id="3c92e-125">Exception</span></span>|<span data-ttu-id="3c92e-126">xs:string</span><span class="sxs-lookup"><span data-stu-id="3c92e-126">xs:string</span></span>|<span data-ttu-id="3c92e-127">异常的异常详细信息</span><span class="sxs-lookup"><span data-stu-id="3c92e-127">The exception details for the exception</span></span>|  
|<span data-ttu-id="3c92e-128">应用程序域</span><span class="sxs-lookup"><span data-stu-id="3c92e-128">AppDomain</span></span>|<span data-ttu-id="3c92e-129">xs:string</span><span class="sxs-lookup"><span data-stu-id="3c92e-129">xs:string</span></span>|<span data-ttu-id="3c92e-130">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="3c92e-130">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
