---
description: 了解详细信息： 1148-FlowchartSwitchCaseNotFound
title: 1148 - FlowchartSwitchCaseNotFound
ms.date: 03/30/2017
ms.assetid: 9ee7fcee-e040-4306-968e-ed840a1cb00c
ms.openlocfilehash: 067dff850a67f1b235bf9c1903757eefa912bd92
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99720405"
---
# <a name="1148---flowchartswitchcasenotfound"></a><span data-ttu-id="9db4b-103">1148 - FlowchartSwitchCaseNotFound</span><span class="sxs-lookup"><span data-stu-id="9db4b-103">1148 - FlowchartSwitchCaseNotFound</span></span>

## <a name="properties"></a><span data-ttu-id="9db4b-104">属性</span><span class="sxs-lookup"><span data-stu-id="9db4b-104">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="9db4b-105">ID</span><span class="sxs-lookup"><span data-stu-id="9db4b-105">ID</span></span>|<span data-ttu-id="9db4b-106">1148</span><span class="sxs-lookup"><span data-stu-id="9db4b-106">1148</span></span>|  
|<span data-ttu-id="9db4b-107">关键字</span><span class="sxs-lookup"><span data-stu-id="9db4b-107">Keywords</span></span>|<span data-ttu-id="9db4b-108">WFActivities</span><span class="sxs-lookup"><span data-stu-id="9db4b-108">WFActivities</span></span>|  
|<span data-ttu-id="9db4b-109">级别</span><span class="sxs-lookup"><span data-stu-id="9db4b-109">Level</span></span>|<span data-ttu-id="9db4b-110">信息</span><span class="sxs-lookup"><span data-stu-id="9db4b-110">Information</span></span>|  
|<span data-ttu-id="9db4b-111">通道</span><span class="sxs-lookup"><span data-stu-id="9db4b-111">Channel</span></span>|<span data-ttu-id="9db4b-112">Microsoft-Windows-应用程序服务器-应用程序/调试</span><span class="sxs-lookup"><span data-stu-id="9db4b-112">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="9db4b-113">说明</span><span class="sxs-lookup"><span data-stu-id="9db4b-113">Description</span></span>  

 <span data-ttu-id="9db4b-114">指示在 Flowchart 开关中找不到匹配大小写，也找不到默认大小写。</span><span class="sxs-lookup"><span data-stu-id="9db4b-114">Indicates that neither a matching case or a default case in a Flowchart switch could be found.</span></span> <span data-ttu-id="9db4b-115">Flowchart 执行将结束。</span><span class="sxs-lookup"><span data-stu-id="9db4b-115">Flowchart execution will end.</span></span>  
  
## <a name="message"></a><span data-ttu-id="9db4b-116">消息</span><span class="sxs-lookup"><span data-stu-id="9db4b-116">Message</span></span>  

 <span data-ttu-id="9db4b-117">Flowchart“%1”/FlowSwitch - 找不到 Case 活动，也找不到与 Expression 结果匹配的 Default Case。</span><span class="sxs-lookup"><span data-stu-id="9db4b-117">Flowchart '%1'/FlowSwitch - could find neither a Case activity nor a Default Case matching the Expression result.</span></span> <span data-ttu-id="9db4b-118">Flowchart 执行将结束。</span><span class="sxs-lookup"><span data-stu-id="9db4b-118">Flowchart execution will end.</span></span>  
  
## <a name="details"></a><span data-ttu-id="9db4b-119">详细信息</span><span class="sxs-lookup"><span data-stu-id="9db4b-119">Details</span></span>  
  
|<span data-ttu-id="9db4b-120">数据项名称</span><span class="sxs-lookup"><span data-stu-id="9db4b-120">Data Item Name</span></span>|<span data-ttu-id="9db4b-121">数据项类型</span><span class="sxs-lookup"><span data-stu-id="9db4b-121">Data Item Type</span></span>|<span data-ttu-id="9db4b-122">说明</span><span class="sxs-lookup"><span data-stu-id="9db4b-122">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="9db4b-123">FlowChart</span><span class="sxs-lookup"><span data-stu-id="9db4b-123">FlowChart</span></span>|<span data-ttu-id="9db4b-124">xs:string</span><span class="sxs-lookup"><span data-stu-id="9db4b-124">xs:string</span></span>|<span data-ttu-id="9db4b-125">FlowChart 的显示名称。</span><span class="sxs-lookup"><span data-stu-id="9db4b-125">The display name of the FlowChart.</span></span>|  
|<span data-ttu-id="9db4b-126">应用程序域</span><span class="sxs-lookup"><span data-stu-id="9db4b-126">AppDomain</span></span>|<span data-ttu-id="9db4b-127">xs:string</span><span class="sxs-lookup"><span data-stu-id="9db4b-127">xs:string</span></span>|<span data-ttu-id="9db4b-128">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="9db4b-128">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
