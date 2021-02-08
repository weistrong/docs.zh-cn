---
description: 了解有关以下内容的详细信息：创建和运行工作流实例
title: 创建和运行工作流实例
ms.date: 03/30/2017
ms.assetid: 19d27f47-0491-4569-8f53-51bc1d940e80
ms.openlocfilehash: 2efd4a0017f450c21954e363af33be69c659624e
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99787846"
---
# <a name="creating-and-running-a-workflow-instance"></a><span data-ttu-id="a6a11-103">创建和运行工作流实例</span><span class="sxs-lookup"><span data-stu-id="a6a11-103">Creating and Running a Workflow Instance</span></span>

<span data-ttu-id="a6a11-104">此示例演示如何运行工作流实例。</span><span class="sxs-lookup"><span data-stu-id="a6a11-104">This sample shows how to run a workflow instance.</span></span> <span data-ttu-id="a6a11-105">它演示如何以同步方式和异步方式执行这一操作。</span><span class="sxs-lookup"><span data-stu-id="a6a11-105">It shows how to execute it synchronously and asynchronously.</span></span>

## <a name="demonstrates"></a><span data-ttu-id="a6a11-106">演示</span><span class="sxs-lookup"><span data-stu-id="a6a11-106">Demonstrates</span></span>

<span data-ttu-id="a6a11-107"><xref:System.Activities.WorkflowInvoker>, <xref:System.Activities.WorkflowApplication>.</span><span class="sxs-lookup"><span data-stu-id="a6a11-107"><xref:System.Activities.WorkflowInvoker>, <xref:System.Activities.WorkflowApplication>.</span></span>

## <a name="discussion"></a><span data-ttu-id="a6a11-108">讨论 (Discussion)</span><span class="sxs-lookup"><span data-stu-id="a6a11-108">Discussion</span></span>

<span data-ttu-id="a6a11-109">此示例的第一部分使用 <xref:System.Activities.WorkflowInvoker.Invoke%2A>。</span><span class="sxs-lookup"><span data-stu-id="a6a11-109">The first part of the sample uses <xref:System.Activities.WorkflowInvoker.Invoke%2A>.</span></span> <span data-ttu-id="a6a11-110">这是执行工作流的最基本方法。</span><span class="sxs-lookup"><span data-stu-id="a6a11-110">This is the most basic way to execute a workflow.</span></span> <span data-ttu-id="a6a11-111">使用 <xref:System.Activities.WorkflowInvoker.Invoke%2A> 执行的工作流以同步方式执行。</span><span class="sxs-lookup"><span data-stu-id="a6a11-111">Workflows executed with <xref:System.Activities.WorkflowInvoker.Invoke%2A> are executed synchronously.</span></span>

<span data-ttu-id="a6a11-112">该示例的第二部分使用 <xref:System.Activities.WorkflowApplication> 类。</span><span class="sxs-lookup"><span data-stu-id="a6a11-112">The second part of the sample uses the <xref:System.Activities.WorkflowApplication> class.</span></span> <span data-ttu-id="a6a11-113">利用 <xref:System.Activities.WorkflowApplication>，您可以对每个实例进行更多控制，包括与正在运行的工作流进行交互的能力和异步运行工作流的能力。</span><span class="sxs-lookup"><span data-stu-id="a6a11-113"><xref:System.Activities.WorkflowApplication> enables you to have more control over each instance, including the ability to interact with the running workflow and to run the workflow asynchronously.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a6a11-114">您的计算机上可能已安装这些示例。</span><span class="sxs-lookup"><span data-stu-id="a6a11-114">The samples may already be installed on your machine.</span></span> <span data-ttu-id="a6a11-115">在继续操作之前，请先检查以下（默认）目录：</span><span class="sxs-lookup"><span data-stu-id="a6a11-115">Check for the following (default) directory before continuing.</span></span>
>
> `<InstallDrive>:\WF_WCF_Samples`
>
> <span data-ttu-id="a6a11-116">如果此目录不存在，请参阅[Windows Communication Foundation (wcf) ，并 Windows Workflow Foundation (的 WF](https://www.microsoft.com/download/details.aspx?id=21459)) .NET Framework Windows Communication Foundation ([!INCLUDE[wf1](../../../../includes/wf1-md.md)]</span><span class="sxs-lookup"><span data-stu-id="a6a11-116">If this directory does not exist, go to [Windows Communication Foundation (WCF) and Windows Workflow Foundation (WF) Samples for .NET Framework 4](https://www.microsoft.com/download/details.aspx?id=21459) to download all Windows Communication Foundation (WCF) and [!INCLUDE[wf1](../../../../includes/wf1-md.md)] samples.</span></span> <span data-ttu-id="a6a11-117">此示例位于以下目录：</span><span class="sxs-lookup"><span data-stu-id="a6a11-117">This sample is located in the following directory.</span></span>
>
> `<InstallDrive>:\WF_WCF_Samples\WF\Basic\Execution\CreatingWorkflowInstances`

## <a name="see-also"></a><span data-ttu-id="a6a11-118">请参阅</span><span class="sxs-lookup"><span data-stu-id="a6a11-118">See also</span></span>

- [<span data-ttu-id="a6a11-119">使用 WorkflowInvoker 和 WorkflowApplication</span><span class="sxs-lookup"><span data-stu-id="a6a11-119">Using WorkflowInvoker and WorkflowApplication</span></span>](../using-workflowinvoker-and-workflowapplication.md)
