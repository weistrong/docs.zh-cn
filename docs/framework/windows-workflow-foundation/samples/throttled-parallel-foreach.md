---
description: 了解详细信息：受限并行 ForEach
title: 限制并行 ForEach
ms.date: 03/30/2017
ms.assetid: f2855b5f-e9a7-433d-96a4-40fc31025215
ms.openlocfilehash: 2c1d1386f0b8c5b3c68d60bc83386ccfdf5e7875
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99741674"
---
# <a name="throttled-parallel-foreach"></a><span data-ttu-id="dd7db-103">限制并行 ForEach</span><span class="sxs-lookup"><span data-stu-id="dd7db-103">Throttled Parallel ForEach</span></span>

<span data-ttu-id="dd7db-104">`ThrottleParallelForEach` 活动类似于 <xref:System.Activities.Statements.ParallelForEach%601> 活动，不同之处在于前者允许设置并发系数来限制要执行的并发分支的数目。</span><span class="sxs-lookup"><span data-stu-id="dd7db-104">The `ThrottleParallelForEach` activity is similar to the <xref:System.Activities.Statements.ParallelForEach%601> activity with the one exception that it allows setting a concurrency factor to restrict the number of simultaneous branches to execute.</span></span> <span data-ttu-id="dd7db-105">`ThrottleParallelForEach` 活动派生自 <xref:System.Activities.NativeActivity>，因为该活动需要对其他活动（子活动）进行计划，并且只有通过 <xref:System.Activities.NativeActivityContext> 类才能对此进行访问。</span><span class="sxs-lookup"><span data-stu-id="dd7db-105">The `ThrottleParallelForEach` activity derives from <xref:System.Activities.NativeActivity>, because it needs to schedule other activities (the child activities) and this is only accessible through the <xref:System.Activities.NativeActivityContext> class.</span></span>

## <a name="projects"></a><span data-ttu-id="dd7db-106">项目</span><span class="sxs-lookup"><span data-stu-id="dd7db-106">Projects</span></span>

|<span data-ttu-id="dd7db-107">**ProjectName**</span><span class="sxs-lookup"><span data-stu-id="dd7db-107">**ProjectName**</span></span>|<span data-ttu-id="dd7db-108">**说明**</span><span class="sxs-lookup"><span data-stu-id="dd7db-108">**Description**</span></span>|<span data-ttu-id="dd7db-109">**主要文件**</span><span class="sxs-lookup"><span data-stu-id="dd7db-109">**Main Files**</span></span>|
|-|-|-|
|<span data-ttu-id="dd7db-110">ThrottledParallelForEach</span><span class="sxs-lookup"><span data-stu-id="dd7db-110">ThrottledParallelForEach</span></span>|<span data-ttu-id="dd7db-111">包含 `ThrottledParallelForEach` 活动及其设计器。</span><span class="sxs-lookup"><span data-stu-id="dd7db-111">Contains `ThrottledParallelForEach` activity and its designer.</span></span>|<span data-ttu-id="dd7db-112">ThrottledParallelForEach.cs</span><span class="sxs-lookup"><span data-stu-id="dd7db-112">ThrottledParallelForEach.cs</span></span><br /><br /> <span data-ttu-id="dd7db-113">`ThrottledParallelForEach` 活动定义。</span><span class="sxs-lookup"><span data-stu-id="dd7db-113">The `ThrottledParallelForEach` activity definition.</span></span>|
|<span data-ttu-id="dd7db-114">CodeTestClient</span><span class="sxs-lookup"><span data-stu-id="dd7db-114">CodeTestClient</span></span>|<span data-ttu-id="dd7db-115">示例客户端应用程序，通过使用命令性代码的 `ThrottledParallelForEach` 来配置和运行工作流。</span><span class="sxs-lookup"><span data-stu-id="dd7db-115">Sample client application that configures and runs a workflow with a `ThrottledParallelForEach` using imperative code.</span></span>|<span data-ttu-id="dd7db-116">Program.cs</span><span class="sxs-lookup"><span data-stu-id="dd7db-116">Program.cs</span></span><br /><br /> <span data-ttu-id="dd7db-117">定义和运行示例工作流的实例。</span><span class="sxs-lookup"><span data-stu-id="dd7db-117">Defines and runs an instance of the sample workflow.</span></span>|

## <a name="to-use-this-sample"></a><span data-ttu-id="dd7db-118">使用此示例</span><span class="sxs-lookup"><span data-stu-id="dd7db-118">To use this sample</span></span>

1. <span data-ttu-id="dd7db-119">使用 Visual Studio 2010 打开 ThrottledParallelForEach 文件。</span><span class="sxs-lookup"><span data-stu-id="dd7db-119">Using Visual Studio 2010, open the ThrottledParallelForEach.sln file.</span></span>

2. <span data-ttu-id="dd7db-120">要生成解决方案，按 Ctrl+Shift+B。</span><span class="sxs-lookup"><span data-stu-id="dd7db-120">To build the solution, press CTRL+SHIFT+B.</span></span>

3. <span data-ttu-id="dd7db-121">若要运行解决方案，请按 F5。</span><span class="sxs-lookup"><span data-stu-id="dd7db-121">To run the solution, press F5.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="dd7db-122">您的计算机上可能已安装这些示例。</span><span class="sxs-lookup"><span data-stu-id="dd7db-122">The samples may already be installed on your machine.</span></span> <span data-ttu-id="dd7db-123">在继续操作之前，请先检查以下（默认）目录：</span><span class="sxs-lookup"><span data-stu-id="dd7db-123">Check for the following (default) directory before continuing.</span></span>
>
> `<InstallDrive>:\WF_WCF_Samples`
>
> <span data-ttu-id="dd7db-124">如果此目录不存在，请参阅[Windows Communication Foundation (wcf) ，并 Windows Workflow Foundation (的 WF](https://www.microsoft.com/download/details.aspx?id=21459)) .NET Framework Windows Communication Foundation ([!INCLUDE[wf1](../../../../includes/wf1-md.md)]</span><span class="sxs-lookup"><span data-stu-id="dd7db-124">If this directory does not exist, go to [Windows Communication Foundation (WCF) and Windows Workflow Foundation (WF) Samples for .NET Framework 4](https://www.microsoft.com/download/details.aspx?id=21459) to download all Windows Communication Foundation (WCF) and [!INCLUDE[wf1](../../../../includes/wf1-md.md)] samples.</span></span> <span data-ttu-id="dd7db-125">此示例位于以下目录：</span><span class="sxs-lookup"><span data-stu-id="dd7db-125">This sample is located in the following directory.</span></span>
>
> `<InstallDrive>:\WF_WCF_Samples\WF\Scenario\ActivityLibrary\ThrottledParallelForEach`
