---
description: 了解详细信息： 1004-WorkflowInstanceAborted
title: 1004 - WorkflowInstanceAborted
ms.date: 03/30/2017
ms.assetid: edb9ab8c-0b9a-488d-aa96-9c8c7984b53c
ms.openlocfilehash: 4aaa0899da9b0b8510684a13537a8cb8f9117ee1
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99755611"
---
# <a name="1004---workflowinstanceaborted"></a><span data-ttu-id="8f96d-103">1004 - WorkflowInstanceAborted</span><span class="sxs-lookup"><span data-stu-id="8f96d-103">1004 - WorkflowInstanceAborted</span></span>

## <a name="properties"></a><span data-ttu-id="8f96d-104">属性</span><span class="sxs-lookup"><span data-stu-id="8f96d-104">Properties</span></span>

|||
|-|-|
|<span data-ttu-id="8f96d-105">ID</span><span class="sxs-lookup"><span data-stu-id="8f96d-105">ID</span></span>|<span data-ttu-id="8f96d-106">1004</span><span class="sxs-lookup"><span data-stu-id="8f96d-106">1004</span></span>|
|<span data-ttu-id="8f96d-107">关键字</span><span class="sxs-lookup"><span data-stu-id="8f96d-107">Keywords</span></span>|<span data-ttu-id="8f96d-108">WFRuntime</span><span class="sxs-lookup"><span data-stu-id="8f96d-108">WFRuntime</span></span>|
|<span data-ttu-id="8f96d-109">级别</span><span class="sxs-lookup"><span data-stu-id="8f96d-109">Level</span></span>|<span data-ttu-id="8f96d-110">信息</span><span class="sxs-lookup"><span data-stu-id="8f96d-110">Information</span></span>|
|<span data-ttu-id="8f96d-111">通道</span><span class="sxs-lookup"><span data-stu-id="8f96d-111">Channel</span></span>|<span data-ttu-id="8f96d-112">Microsoft-Windows-应用程序服务器-应用程序/调试</span><span class="sxs-lookup"><span data-stu-id="8f96d-112">Microsoft-Windows-Application Server-Applications/Debug</span></span>|

## <a name="description"></a><span data-ttu-id="8f96d-113">说明</span><span class="sxs-lookup"><span data-stu-id="8f96d-113">Description</span></span>

<span data-ttu-id="8f96d-114">指示工作流实例已中止但出现异常。</span><span class="sxs-lookup"><span data-stu-id="8f96d-114">Indicates a workflow instance has aborted with an exception.</span></span>

## <a name="message"></a><span data-ttu-id="8f96d-115">消息</span><span class="sxs-lookup"><span data-stu-id="8f96d-115">Message</span></span>

<span data-ttu-id="8f96d-116">WorkflowInstance Id“%1”因出现异常而中止。</span><span class="sxs-lookup"><span data-stu-id="8f96d-116">WorkflowInstance Id: '%1' was aborted with an exception.</span></span>

## <a name="details"></a><span data-ttu-id="8f96d-117">详细信息</span><span class="sxs-lookup"><span data-stu-id="8f96d-117">Details</span></span>

|<span data-ttu-id="8f96d-118">数据项名称</span><span class="sxs-lookup"><span data-stu-id="8f96d-118">Data Item Name</span></span>|<span data-ttu-id="8f96d-119">数据项类型</span><span class="sxs-lookup"><span data-stu-id="8f96d-119">Data Item Type</span></span>|<span data-ttu-id="8f96d-120">说明</span><span class="sxs-lookup"><span data-stu-id="8f96d-120">Description</span></span>|
|--------------------|--------------------|-----------------|
|<span data-ttu-id="8f96d-121">WorkflowInstanceId</span><span class="sxs-lookup"><span data-stu-id="8f96d-121">WorkflowInstanceId</span></span>|`xs:string`|<span data-ttu-id="8f96d-122">工作流的实例 ID</span><span class="sxs-lookup"><span data-stu-id="8f96d-122">The instance id for the workflow</span></span>|
|<span data-ttu-id="8f96d-123">异常</span><span class="sxs-lookup"><span data-stu-id="8f96d-123">Exception</span></span>|`xs:string`|<span data-ttu-id="8f96d-124">异常的异常详细信息</span><span class="sxs-lookup"><span data-stu-id="8f96d-124">The exception details for the exception</span></span>|
|<span data-ttu-id="8f96d-125">应用程序域</span><span class="sxs-lookup"><span data-stu-id="8f96d-125">AppDomain</span></span>|`xs:string`|<span data-ttu-id="8f96d-126">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="8f96d-126">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
