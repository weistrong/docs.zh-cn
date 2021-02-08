---
description: 了解详细信息：使用编辑范围
title: 使用编辑范围
ms.date: 03/30/2017
ms.assetid: 79306f9e-318b-4687-9863-8b93d1841716
ms.openlocfilehash: 9d91c787bb1b44d5cd07245fe48bd31ed2ccab3c
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99787768"
---
# <a name="using-editing-scope"></a><span data-ttu-id="2b14a-103">使用编辑范围</span><span class="sxs-lookup"><span data-stu-id="2b14a-103">Using Editing Scope</span></span>

<span data-ttu-id="2b14a-104">此示例演示如何对一组更改进行批处理，以便可以在一个原子单元中撤消它们。</span><span class="sxs-lookup"><span data-stu-id="2b14a-104">This sample demonstrates how to batch a set of changes so that they can be undone in a single atomic unit.</span></span> <span data-ttu-id="2b14a-105">默认情况下，活动设计器作者采取的操作会自动集成到撤消/重复系统中。</span><span class="sxs-lookup"><span data-stu-id="2b14a-105">By default, the actions taken by an activity designer author are automatically integrated into the Undo/Redo system.</span></span>  
  
## <a name="demonstrates"></a><span data-ttu-id="2b14a-106">演示</span><span class="sxs-lookup"><span data-stu-id="2b14a-106">Demonstrates</span></span>  

 <span data-ttu-id="2b14a-107">编辑范围域和撤消/重做。</span><span class="sxs-lookup"><span data-stu-id="2b14a-107">Editing scope and Undo and Redo.</span></span>  
  
## <a name="discussion"></a><span data-ttu-id="2b14a-108">讨论 (Discussion)</span><span class="sxs-lookup"><span data-stu-id="2b14a-108">Discussion</span></span>  

 <span data-ttu-id="2b14a-109">此示例演示如何在一个工作单元中对针对 <xref:System.Activities.Presentation.Model.ModelItem> 树的一组更改进行批处理。</span><span class="sxs-lookup"><span data-stu-id="2b14a-109">This sample demonstrates how to batch a set of changes to the <xref:System.Activities.Presentation.Model.ModelItem> tree within a single unit of work.</span></span> <span data-ttu-id="2b14a-110">请注意，直接从 WPF 设计器绑定到 <xref:System.Activities.Presentation.Model.ModelItem> 值时，将会自动应用更改。</span><span class="sxs-lookup"><span data-stu-id="2b14a-110">Note that when binding to <xref:System.Activities.Presentation.Model.ModelItem> values directly from a WPF designer, changes are applied automatically.</span></span> <span data-ttu-id="2b14a-111">此示例演示通过命令性代码进行要批处理的多个更改（而不是单个更改）时必须执行的操作。</span><span class="sxs-lookup"><span data-stu-id="2b14a-111">This sample demonstrates what must be done when multiple changes to be batched are being made through imperative code, rather than a single change.</span></span>  
  
 <span data-ttu-id="2b14a-112">在此示例中，添加了三个活动。</span><span class="sxs-lookup"><span data-stu-id="2b14a-112">In this sample, three activities are added.</span></span> <span data-ttu-id="2b14a-113">当编辑开始时，对 <xref:System.Activities.Presentation.Model.ModelItem.BeginEdit%2A> 的实例调用 <xref:System.Activities.Presentation.Model.ModelItem>。 </span><span class="sxs-lookup"><span data-stu-id="2b14a-113">When editing begins, <xref:System.Activities.Presentation.Model.ModelItem.BeginEdit%2A> is called on an instance of <xref:System.Activities.Presentation.Model.ModelItem>.</span></span> <span data-ttu-id="2b14a-114">将对在此编辑范围中对 <xref:System.Activities.Presentation.Model.ModelItem> 树所做的更改进行批处理。</span><span class="sxs-lookup"><span data-stu-id="2b14a-114">Changes made to the <xref:System.Activities.Presentation.Model.ModelItem> tree within this editing scope are batched.</span></span> <span data-ttu-id="2b14a-115"><xref:System.Activities.Presentation.Model.ModelItem.BeginEdit%2A> 命令返回一个可用于控制此实例的 <xref:System.Activities.Presentation.Model.EditingScope>。</span><span class="sxs-lookup"><span data-stu-id="2b14a-115">The <xref:System.Activities.Presentation.Model.ModelItem.BeginEdit%2A> command returns an <xref:System.Activities.Presentation.Model.EditingScope>, which can be used to control this instance.</span></span> <span data-ttu-id="2b14a-116">可以调用 <xref:System.Activities.Presentation.Model.EditingScope.OnComplete%2A> 提交编辑范围或调用 <xref:System.Activities.Presentation.Model.EditingScope.OnRevert%2A> 还原编辑范围。</span><span class="sxs-lookup"><span data-stu-id="2b14a-116">Either <xref:System.Activities.Presentation.Model.EditingScope.OnComplete%2A> or <xref:System.Activities.Presentation.Model.EditingScope.OnRevert%2A> can be called to either commit or revert the editing scope.</span></span>  
  
 <span data-ttu-id="2b14a-117">还可以嵌套 <xref:System.Activities.Presentation.Model.EditingScope> 对象，这样便可以将多个更改集作为一个更大的编辑范围的一部分进行跟踪，并单独控制。</span><span class="sxs-lookup"><span data-stu-id="2b14a-117">You can also nest <xref:System.Activities.Presentation.Model.EditingScope> objects, which allows for multiple sets of changes to be tracked as part of a larger editing scope and can be controlled individually.</span></span> <span data-ttu-id="2b14a-118">如果来自多个对话框的更改必须单独提交或还原，并且需要将所有更改视为单个原子操作，在这种场合下则可以使用此功能。</span><span class="sxs-lookup"><span data-stu-id="2b14a-118">A scenario that may use this feature would be when changes from multiple dialogs must be committed or reverted separately, with all changes being treated as a single atomic operation.</span></span> <span data-ttu-id="2b14a-119">在此示例中，使用 <xref:System.Collections.ObjectModel.ObservableCollection%601> 类型的 <xref:System.Activities.Presentation.Model.ModelEditingScope> 来对编辑范围进行堆栈处理。</span><span class="sxs-lookup"><span data-stu-id="2b14a-119">In this sample, the editing scopes are stacked using an <xref:System.Collections.ObjectModel.ObservableCollection%601> of type <xref:System.Activities.Presentation.Model.ModelEditingScope>.</span></span> <span data-ttu-id="2b14a-120">使用 <xref:System.Collections.ObjectModel.ObservableCollection%601> 的目的是为了能够在设计器图面上观察到嵌套的深度。</span><span class="sxs-lookup"><span data-stu-id="2b14a-120">The <xref:System.Collections.ObjectModel.ObservableCollection%601> is used so that the depth of the nesting can be observed on the designer surface.</span></span>  
  
## <a name="to-set-up-build-and-run-the-sample"></a><span data-ttu-id="2b14a-121">设置、生成和运行示例</span><span class="sxs-lookup"><span data-stu-id="2b14a-121">To set up, build, and run the sample</span></span>  
  
1. <span data-ttu-id="2b14a-122">生成和运行示例，然后使用左边的按钮修改工作流。</span><span class="sxs-lookup"><span data-stu-id="2b14a-122">Build and run the sample, and then use the buttons on the left to modify the workflow.</span></span>  
  
2. <span data-ttu-id="2b14a-123">单击 " **打开编辑范围**"。</span><span class="sxs-lookup"><span data-stu-id="2b14a-123">Click **Open Editing Scope**.</span></span>  
  
    1. <span data-ttu-id="2b14a-124">此命令将调用 <xref:System.Activities.Presentation.Model.ModelItem.BeginEdit%2A>；后者会创建一个编辑范围，并将其推入到编辑堆栈中。</span><span class="sxs-lookup"><span data-stu-id="2b14a-124">This command calls <xref:System.Activities.Presentation.Model.ModelItem.BeginEdit%2A> that creates an editing scope and pushes it onto the editing stack.</span></span>  
  
    2. <span data-ttu-id="2b14a-125">然后将三个活动添加到选定的 <xref:System.Activities.Presentation.Model.ModelItem> 中。</span><span class="sxs-lookup"><span data-stu-id="2b14a-125">Three activities are then added to the selected <xref:System.Activities.Presentation.Model.ModelItem>.</span></span> <span data-ttu-id="2b14a-126">请注意，如果尚未使用 <xref:System.Activities.Presentation.Model.ModelItem.BeginEdit%2A> 打开编辑范围，则这三个新活动将会显示在设计器画布上。</span><span class="sxs-lookup"><span data-stu-id="2b14a-126">Note that if the editing scope had not been opened with <xref:System.Activities.Presentation.Model.ModelItem.BeginEdit%2A>, three new activities would appear on the designer canvas.</span></span> <span data-ttu-id="2b14a-127">因为此操作仍然在 <xref:System.Activities.Presentation.Model.EditingScope> 中挂起，所以不会更新设计器。</span><span class="sxs-lookup"><span data-stu-id="2b14a-127">Because this operation is still pending within the <xref:System.Activities.Presentation.Model.EditingScope>, the designer is not yet updated.</span></span>  
  
3. <span data-ttu-id="2b14a-128">按 " **关闭编辑范围** " 以提交编辑范围。</span><span class="sxs-lookup"><span data-stu-id="2b14a-128">Press **Close Editing Scope** to commit the editing scope.</span></span> <span data-ttu-id="2b14a-129">三个活动出现在设计器中。</span><span class="sxs-lookup"><span data-stu-id="2b14a-129">Three activities appear in the designer.</span></span>  
  
> [!IMPORTANT]
> <span data-ttu-id="2b14a-130">您的计算机上可能已安装这些示例。</span><span class="sxs-lookup"><span data-stu-id="2b14a-130">The samples may already be installed on your machine.</span></span> <span data-ttu-id="2b14a-131">在继续操作之前，请先检查以下（默认）目录：</span><span class="sxs-lookup"><span data-stu-id="2b14a-131">Check for the following (default) directory before continuing.</span></span>  
>
> `<InstallDrive>:\WF_WCF_Samples`  
>
> <span data-ttu-id="2b14a-132">如果此目录不存在，请参阅[Windows Communication Foundation (wcf) ，并 Windows Workflow Foundation (的 WF](https://www.microsoft.com/download/details.aspx?id=21459)) .NET Framework Windows Communication Foundation ([!INCLUDE[wf1](../../../../includes/wf1-md.md)]</span><span class="sxs-lookup"><span data-stu-id="2b14a-132">If this directory does not exist, go to [Windows Communication Foundation (WCF) and Windows Workflow Foundation (WF) Samples for .NET Framework 4](https://www.microsoft.com/download/details.aspx?id=21459) to download all Windows Communication Foundation (WCF) and [!INCLUDE[wf1](../../../../includes/wf1-md.md)] samples.</span></span> <span data-ttu-id="2b14a-133">此示例位于以下目录：</span><span class="sxs-lookup"><span data-stu-id="2b14a-133">This sample is located in the following directory.</span></span>  
>
> `<InstallDrive>:\WF_WCF_Samples\WF\Basic\CustomActivities\CustomActivityDesigners\UsingEditingScope`
