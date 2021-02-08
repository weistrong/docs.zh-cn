---
description: 了解详细信息：跟踪类型摘要
title: 跟踪类型摘要
ms.date: 03/30/2017
ms.assetid: e639410b-d1d1-479c-b78e-a4701d4e4085
ms.openlocfilehash: ebfe9de16766494a6aebe0a8d2501954855dc4df
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99803212"
---
# <a name="trace-type-summary"></a><span data-ttu-id="61d76-103">跟踪类型摘要</span><span class="sxs-lookup"><span data-stu-id="61d76-103">Trace Type Summary</span></span>

<span data-ttu-id="61d76-104">[源级别](xref:System.Diagnostics.SourceLevels) 定义各种跟踪级别：严重、错误、警告、信息和详细信息，并提供标志的说明 `ActivityTracing` ，该标志用于切换跟踪边界和活动传输事件的输出。</span><span class="sxs-lookup"><span data-stu-id="61d76-104">[Source Levels](xref:System.Diagnostics.SourceLevels) defines various trace levels: Critical, Error, Warning, Information, and Verbose, as well as provides a description of the `ActivityTracing` flag, which toggles the output of trace boundary and activity transfer events.</span></span>  
  
 <span data-ttu-id="61d76-105">你还可以查看 <xref:System.Diagnostics.TraceEventType> 可从发出的跟踪类型 <xref:System.Diagnostics> 。</span><span class="sxs-lookup"><span data-stu-id="61d76-105">You can also review <xref:System.Diagnostics.TraceEventType> for the types of traces which can be emitted from <xref:System.Diagnostics>.</span></span>  
  
 <span data-ttu-id="61d76-106">下表列出了最重要的跟踪类型。</span><span class="sxs-lookup"><span data-stu-id="61d76-106">The following table lists the most important ones.</span></span>  
  
|<span data-ttu-id="61d76-107">跟踪类型</span><span class="sxs-lookup"><span data-stu-id="61d76-107">Trace Type</span></span>|<span data-ttu-id="61d76-108">说明</span><span class="sxs-lookup"><span data-stu-id="61d76-108">Description</span></span>|  
|----------------|-----------------|  
|<span data-ttu-id="61d76-109">严重</span><span class="sxs-lookup"><span data-stu-id="61d76-109">Critical</span></span>|<span data-ttu-id="61d76-110">致命错误或应用程序崩溃。</span><span class="sxs-lookup"><span data-stu-id="61d76-110">Fatal error or application crash.</span></span>|  
|<span data-ttu-id="61d76-111">错误</span><span class="sxs-lookup"><span data-stu-id="61d76-111">Error</span></span>|<span data-ttu-id="61d76-112">可恢复的错误。</span><span class="sxs-lookup"><span data-stu-id="61d76-112">Recoverable error.</span></span>|  
|<span data-ttu-id="61d76-113">警告</span><span class="sxs-lookup"><span data-stu-id="61d76-113">Warning</span></span>|<span data-ttu-id="61d76-114">信息性消息。</span><span class="sxs-lookup"><span data-stu-id="61d76-114">Informational message.</span></span>|  
|<span data-ttu-id="61d76-115">信息</span><span class="sxs-lookup"><span data-stu-id="61d76-115">Information</span></span>|<span data-ttu-id="61d76-116">非严重问题。</span><span class="sxs-lookup"><span data-stu-id="61d76-116">Non-critical problem.</span></span>|  
|<span data-ttu-id="61d76-117">详细</span><span class="sxs-lookup"><span data-stu-id="61d76-117">Verbose</span></span>|<span data-ttu-id="61d76-118">调试跟踪。</span><span class="sxs-lookup"><span data-stu-id="61d76-118">Debugging trace.</span></span>|  
|<span data-ttu-id="61d76-119">开始</span><span class="sxs-lookup"><span data-stu-id="61d76-119">Start</span></span>|<span data-ttu-id="61d76-120">开始处理逻辑单元。</span><span class="sxs-lookup"><span data-stu-id="61d76-120">Starting of a logical unit of processing.</span></span>|  
|<span data-ttu-id="61d76-121">挂起</span><span class="sxs-lookup"><span data-stu-id="61d76-121">Suspend</span></span>|<span data-ttu-id="61d76-122">挂起逻辑单元处理。</span><span class="sxs-lookup"><span data-stu-id="61d76-122">Suspension of a logical unit of processing.</span></span>|  
|<span data-ttu-id="61d76-123">继续</span><span class="sxs-lookup"><span data-stu-id="61d76-123">Resume</span></span>|<span data-ttu-id="61d76-124">继续逻辑单元处理。</span><span class="sxs-lookup"><span data-stu-id="61d76-124">Resumption of a logical unit of processing.</span></span>|  
|<span data-ttu-id="61d76-125">停止</span><span class="sxs-lookup"><span data-stu-id="61d76-125">Stop</span></span>|<span data-ttu-id="61d76-126">停止处理逻辑单元。</span><span class="sxs-lookup"><span data-stu-id="61d76-126">Stopping of a logical unit of processing.</span></span>|  
|<span data-ttu-id="61d76-127">传输</span><span class="sxs-lookup"><span data-stu-id="61d76-127">Transfer</span></span>|<span data-ttu-id="61d76-128">更改相关标识。</span><span class="sxs-lookup"><span data-stu-id="61d76-128">Changing of correlation identity.</span></span>|  
  
 <span data-ttu-id="61d76-129">活动定义为上述跟踪类型的组合。</span><span class="sxs-lookup"><span data-stu-id="61d76-129">An activity is defined as a combination of the trace types above.</span></span>  
  
 <span data-ttu-id="61d76-130">下面的正则表达式用于定义本地（跟踪源）范围内的理想活动，</span><span class="sxs-lookup"><span data-stu-id="61d76-130">The following is a regular expression that defines an ideal activity in a local (trace source) scope,</span></span>  
  
 `R = Start (Critical | Error | Warning | Information | Verbose | Transfer | (Transfer Suspend Transfer Resume) )* Stop`  
  
 <span data-ttu-id="61d76-131">这意味着活动必须满足以下条件。</span><span class="sxs-lookup"><span data-stu-id="61d76-131">This means that an activity must satisfy the following conditions.</span></span>  
  
- <span data-ttu-id="61d76-132">它必须分别由开始跟踪和停止跟踪来启动和停止</span><span class="sxs-lookup"><span data-stu-id="61d76-132">It must start and stop respectively by a Start and Stop traces</span></span>  
  
- <span data-ttu-id="61d76-133">它必须刚好在挂起跟踪或恢复跟踪之前具有传输跟踪</span><span class="sxs-lookup"><span data-stu-id="61d76-133">It must have a Transfer trace immediately preceding a Suspend or Resume trace</span></span>  
  
- <span data-ttu-id="61d76-134">如果有挂起和恢复跟踪，则在挂起跟踪和恢复跟踪之间不能有任何跟踪</span><span class="sxs-lookup"><span data-stu-id="61d76-134">It must not have any traces between the Suspend and Resume traces if such traces exist</span></span>  
  
- <span data-ttu-id="61d76-135">只要符合上述条件，就可以有任意多个严重/错误/警告/信息/详细/传输跟踪</span><span class="sxs-lookup"><span data-stu-id="61d76-135">It can have any and as many of critical/Error/Warning/Information/Verbose/Transfer traces as long as the previous conditions are observed</span></span>  
  
 <span data-ttu-id="61d76-136">下面的正则表达式用于定义全局范围内的理想活动，</span><span class="sxs-lookup"><span data-stu-id="61d76-136">The following is a regular expression that defines an ideal activity in the global scope,</span></span>  
  
`R+`  
  
 <span data-ttu-id="61d76-137">R 是本地范围内活动的正则表达式。</span><span class="sxs-lookup"><span data-stu-id="61d76-137">with R being the regular expression for an activity in the local scope.</span></span> <span data-ttu-id="61d76-138">这将转换为，</span><span class="sxs-lookup"><span data-stu-id="61d76-138">This translates to,</span></span>  
  
`[R+ = Start ( Critical | Error | Warning | Information | Verbose | Transfer | (Transfer Suspend Transfer Resume) )* Stop]+`
