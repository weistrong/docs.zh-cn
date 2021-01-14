---
title: 如何：创建工作流
description: 完成此部分中三个选项中的一个，以在此 Workflow Foundation 教程中创建工作流。
ms.date: 03/30/2017
ms.assetid: 87234108-8e21-4cb3-9340-4a1a13f3f98c
ms.openlocfilehash: ea9fd023ba15ae23a10f5b8cf6f82c49ca9af6c8
ms.sourcegitcommit: a4cecb7389f02c27e412b743f9189bd2a6dea4d6
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/14/2021
ms.locfileid: "98190437"
---
# <a name="how-to-create-a-workflow"></a><span data-ttu-id="80d2e-103">如何：创建工作流</span><span class="sxs-lookup"><span data-stu-id="80d2e-103">How to: Create a Workflow</span></span>

<span data-ttu-id="80d2e-104">工作流可基于内置活动以及自定义活动来构造。</span><span class="sxs-lookup"><span data-stu-id="80d2e-104">Workflows can be constructed from built-in activities as well as from custom activities.</span></span> <span data-ttu-id="80d2e-105">本节中的主题介绍如何创建一个工作流，该工作流使用内置活动（如 <xref:System.Activities.Statements.Flowchart> 活动）和前面的 [如何：创建活动](how-to-create-an-activity.md) 主题中的自定义活动。</span><span class="sxs-lookup"><span data-stu-id="80d2e-105">The topics in this section step through creating a workflow that uses both built-in activities such as the <xref:System.Activities.Statements.Flowchart> activity, and the custom activities from the previous [How to: Create an Activity](how-to-create-an-activity.md) topic.</span></span> <span data-ttu-id="80d2e-106">该工作流模拟猜数游戏。</span><span class="sxs-lookup"><span data-stu-id="80d2e-106">The workflow models a number guessing game.</span></span> <span data-ttu-id="80d2e-107">本节中只有一个主题是完成本教程所必需的；您应该选择感兴趣的样式并按照该步骤执行。</span><span class="sxs-lookup"><span data-stu-id="80d2e-107">Only one of the topics in this section is required to complete the tutorial; you should pick the style that interests you and follow that step.</span></span> <span data-ttu-id="80d2e-108">但是，您可以完成所有主题（如果需要）。</span><span class="sxs-lookup"><span data-stu-id="80d2e-108">However, you may complete all of the topics if desired.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="80d2e-109">入门教程中的每个主题都依赖于前面的主题。</span><span class="sxs-lookup"><span data-stu-id="80d2e-109">Each topic in the Getting Started tutorial depends on the previous topics.</span></span> <span data-ttu-id="80d2e-110">若要完成本主题，必须先完成 [操作方法：创建活动](how-to-create-an-activity.md)。</span><span class="sxs-lookup"><span data-stu-id="80d2e-110">To complete this topic, you must first complete [How to: Create an Activity](how-to-create-an-activity.md).</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="80d2e-111">本节内容</span><span class="sxs-lookup"><span data-stu-id="80d2e-111">In This Section</span></span>  

 [<span data-ttu-id="80d2e-112">如何：创建顺序工作流</span><span class="sxs-lookup"><span data-stu-id="80d2e-112">How to: Create a Sequential Workflow</span></span>](how-to-create-a-sequential-workflow.md)  
 <span data-ttu-id="80d2e-113">介绍如何使用 <xref:System.Activities.Statements.Sequence> 活动创建顺序工作流。</span><span class="sxs-lookup"><span data-stu-id="80d2e-113">Describes how to create a sequential workflow using the <xref:System.Activities.Statements.Sequence> activity.</span></span>  
  
 [<span data-ttu-id="80d2e-114">如何：创建 Flowchart 工作流</span><span class="sxs-lookup"><span data-stu-id="80d2e-114">How to: Create a Flowchart Workflow</span></span>](how-to-create-a-flowchart-workflow.md)  
 <span data-ttu-id="80d2e-115">介绍如何使用 <xref:System.Activities.Statements.Flowchart> 活动创建流程图工作流。</span><span class="sxs-lookup"><span data-stu-id="80d2e-115">Describes how to create a flowchart workflow using the <xref:System.Activities.Statements.Flowchart> activity.</span></span>  
  
 [<span data-ttu-id="80d2e-116">如何：创建状态机工作流</span><span class="sxs-lookup"><span data-stu-id="80d2e-116">How to: Create a State Machine Workflow</span></span>](how-to-create-a-state-machine-workflow.md)  
 <span data-ttu-id="80d2e-117">介绍如何使用 <xref:System.Activities.Statements.StateMachine> 活动创建状态机工作流。</span><span class="sxs-lookup"><span data-stu-id="80d2e-117">Describes how to create a state machine workflow using the <xref:System.Activities.Statements.StateMachine> activity.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="80d2e-118">另请参阅</span><span class="sxs-lookup"><span data-stu-id="80d2e-118">See also</span></span>

- [<span data-ttu-id="80d2e-119">Windows Workflow Foundation 编程</span><span class="sxs-lookup"><span data-stu-id="80d2e-119">Windows Workflow Foundation Programming</span></span>](programming.md)
