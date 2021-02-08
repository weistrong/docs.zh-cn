---
description: 了解更多相关信息：自定义复合设计器-工作流项演示者
title: 自定义复合设计器 — 工作流项演示器
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 70055c4b-1173-47a3-be80-b5bce6f59e9a
ms.openlocfilehash: 07970763e12eccd981370f1241642cc28f675824
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99792578"
---
# <a name="custom-composite-designers---workflow-items-presenter"></a><span data-ttu-id="92d30-103">自定义复合设计器 — 工作流项演示器</span><span class="sxs-lookup"><span data-stu-id="92d30-103">Custom Composite Designers - Workflow Items Presenter</span></span>

<span data-ttu-id="92d30-104"><xref:System.Activities.Presentation.WorkflowItemsPresenter?displayProperty=nameWithType> 是 WF 设计器编程模型中的一个重要类型，可用于编辑包含元素的集合。</span><span class="sxs-lookup"><span data-stu-id="92d30-104">The <xref:System.Activities.Presentation.WorkflowItemsPresenter?displayProperty=nameWithType> is a key type in the WF designer programming model that allows for the editing of a collection of contained elements.</span></span> <span data-ttu-id="92d30-105">此示例演示如何生成一个呈现此类可编辑集合的活动设计器。</span><span class="sxs-lookup"><span data-stu-id="92d30-105">This sample shows how to build an activity designer that surfaces such an editable collection.</span></span>

<span data-ttu-id="92d30-106">此示例演示：</span><span class="sxs-lookup"><span data-stu-id="92d30-106">This sample demonstrates:</span></span>

- <span data-ttu-id="92d30-107">使用 <xref:System.Activities.Presentation.WorkflowItemsPresenter?displayProperty=nameWithType> 创建自定义活动设计器。</span><span class="sxs-lookup"><span data-stu-id="92d30-107">Creating a custom activity designer with a <xref:System.Activities.Presentation.WorkflowItemsPresenter?displayProperty=nameWithType>.</span></span>

- <span data-ttu-id="92d30-108">使用 "折叠" 视图和 "已扩展" 视图创建活动设计器。</span><span class="sxs-lookup"><span data-stu-id="92d30-108">Creating an activity designer with a "collapsed" and "expanded" view.</span></span>

- <span data-ttu-id="92d30-109">在重新承载的应用程序中重写默认设计器。</span><span class="sxs-lookup"><span data-stu-id="92d30-109">Overriding a default designer in a rehosted application.</span></span>

## <a name="set-up-build-and-run-the-sample"></a><span data-ttu-id="92d30-110">设置、生成和运行示例</span><span class="sxs-lookup"><span data-stu-id="92d30-110">Set up, build, and run the sample</span></span>

1. <span data-ttu-id="92d30-111">在 Visual Studio 2010 中打开适用于 c # 或 Visual Basic 的 **usingworkflowitemspresenter.sln** 示例解决方案。</span><span class="sxs-lookup"><span data-stu-id="92d30-111">Open the **UsingWorkflowItemsPresenter.sln** sample solution for C# or for Visual Basic in Visual Studio 2010.</span></span>

2. <span data-ttu-id="92d30-112">生成并运行解决方案。</span><span class="sxs-lookup"><span data-stu-id="92d30-112">Build and run the solution.</span></span>

   <span data-ttu-id="92d30-113">此时将打开一个重新承载工作流设计器应用程序，你可以将活动拖动到画布上。</span><span class="sxs-lookup"><span data-stu-id="92d30-113">A rehosted workflow designer application opens, and you can drag activities onto the canvas.</span></span>

## <a name="sample-highlights"></a><span data-ttu-id="92d30-114">示例重点</span><span class="sxs-lookup"><span data-stu-id="92d30-114">Sample Highlights</span></span>

<span data-ttu-id="92d30-115">此示例的代码演示了以下内容：</span><span class="sxs-lookup"><span data-stu-id="92d30-115">The code for this sample shows the following:</span></span>

- <span data-ttu-id="92d30-116">构建的设计器所针对的活动：`Parallel`</span><span class="sxs-lookup"><span data-stu-id="92d30-116">The activity a designer is built for:  `Parallel`</span></span>

- <span data-ttu-id="92d30-117">使用 <xref:System.Activities.Presentation.WorkflowItemsPresenter?displayProperty=nameWithType> 创建自定义活动设计器。</span><span class="sxs-lookup"><span data-stu-id="92d30-117">The creation of a custom activity designer with a <xref:System.Activities.Presentation.WorkflowItemsPresenter?displayProperty=nameWithType>.</span></span> <span data-ttu-id="92d30-118">需要指出的一些事项：</span><span class="sxs-lookup"><span data-stu-id="92d30-118">A few things to point out:</span></span>

  - <span data-ttu-id="92d30-119">请注意，应使用 WPF 数据绑定来绑定到 `ModelItem.Branches`。</span><span class="sxs-lookup"><span data-stu-id="92d30-119">Note the use of WPF data binding to bind to `ModelItem.Branches`.</span></span> <span data-ttu-id="92d30-120">`ModelItem` 是 `WorkflowElementDesigner` 的属性，它引用设计器所用于的基础对象，在此例中为 `Parallel`。</span><span class="sxs-lookup"><span data-stu-id="92d30-120">`ModelItem` is the property on `WorkflowElementDesigner` that refers to the underlying object the designer is being used for, in this case, our `Parallel`.</span></span>

  - <span data-ttu-id="92d30-121"><xref:System.Activities.Presentation.WorkflowItemsPresenter.SpacerTemplate?displayProperty=nameWithType> 可用于在集合中的各个项之间显示一个可视对象。</span><span class="sxs-lookup"><span data-stu-id="92d30-121">The <xref:System.Activities.Presentation.WorkflowItemsPresenter.SpacerTemplate?displayProperty=nameWithType> can be used to put a visual to display between the individual items in the collection.</span></span>

  - <span data-ttu-id="92d30-122"><xref:System.Activities.Presentation.WorkflowItemsPresenter.ItemsPanel?displayProperty=nameWithType> 是一个模板，可用于确定集合中的项的布局。</span><span class="sxs-lookup"><span data-stu-id="92d30-122"><xref:System.Activities.Presentation.WorkflowItemsPresenter.ItemsPanel?displayProperty=nameWithType> is a template that can be provided to determine the layout of the items in the collection.</span></span> <span data-ttu-id="92d30-123">在此例中，使用水平堆叠面板。</span><span class="sxs-lookup"><span data-stu-id="92d30-123">In this case, a horizontal stack panel is used.</span></span>

  <span data-ttu-id="92d30-124">下面的示例代码演示了此过程。</span><span class="sxs-lookup"><span data-stu-id="92d30-124">This following example code shows this.</span></span>

  ```xaml
  <sad:WorkflowItemsPresenter HintText="Drop Activities Here"
                                Items="{Binding Path=ModelItem.Branches}">
      <sad:WorkflowItemsPresenter.SpacerTemplate>
        <DataTemplate>
          <Ellipse Width="10" Height="10" Fill="Black"/>
        </DataTemplate>
      </sad:WorkflowItemsPresenter.SpacerTemplate>
      <sad:WorkflowItemsPresenter.ItemsPanel>
        <ItemsPanelTemplate>
          <StackPanel Orientation="Horizontal"/>
        </ItemsPanelTemplate>
      </sad:WorkflowItemsPresenter.ItemsPanel>
    </sad:WorkflowItemsPresenter>
  ```

- <span data-ttu-id="92d30-125">执行 `DesignerAttribute` 与 `Parallel` 类型的关联，然后输出报告的特性。</span><span class="sxs-lookup"><span data-stu-id="92d30-125">Perform an association of the `DesignerAttribute` to the `Parallel` type and then output the attributes reported.</span></span>

  - <span data-ttu-id="92d30-126">首先，注册所有默认的设计器。</span><span class="sxs-lookup"><span data-stu-id="92d30-126">First, register all of the default designers.</span></span>

    <span data-ttu-id="92d30-127">以下是代码示例。</span><span class="sxs-lookup"><span data-stu-id="92d30-127">The following is the code example.</span></span>

    ```csharp
    // register metadata
    (new DesignerMetadata()).Register();
    RegisterCustomMetadata();
    ```

    ```vb
    ' register metadata
    Dim metadata = New DesignerMetadata()
    metadata.Register()
    ' register custom metadata
    RegisterCustomMetadata()
    ```

  - <span data-ttu-id="92d30-128">然后，在 `RegisterCustomMetadata` 方法中重写此并行处理。</span><span class="sxs-lookup"><span data-stu-id="92d30-128">Then, override the parallel in `RegisterCustomMetadata` method.</span></span>

    <span data-ttu-id="92d30-129">下面的代码分别使用 C# 和 Visual Basic 演示了此过程。</span><span class="sxs-lookup"><span data-stu-id="92d30-129">The following code shows this in C# and Visual Basic.</span></span>

    ```csharp
    void RegisterCustomMetadata()
    {
          AttributeTableBuilder builder = new AttributeTableBuilder();
          builder.AddCustomAttributes(typeof(Parallel), new DesignerAttribute(typeof(CustomParallelDesigner)));
          MetadataStore.AddAttributeTable(builder.CreateTable());
    }
    ```

    ```vb
    Sub RegisterCustomMetadata()
       Dim builder As New AttributeTableBuilder()
       builder.AddCustomAttributes(GetType(Parallel), New DesignerAttribute(GetType(CustomParallelDesigner)))
       MetadataStore.AddAttributeTable(builder.CreateTable())
    End Sub
    ```

- <span data-ttu-id="92d30-130">最后，请注意使用不同的数据模板和触发器来基于 `IsRootDesigner` 属性选择适当的模板。</span><span class="sxs-lookup"><span data-stu-id="92d30-130">Finally, note the use of differing data templates and triggers to select the appropriate template based on the `IsRootDesigner` property.</span></span>

  <span data-ttu-id="92d30-131">以下是代码示例。</span><span class="sxs-lookup"><span data-stu-id="92d30-131">The following is the code example.</span></span>

  ```xaml
  <sad:ActivityDesigner x:Class="Microsoft.Samples.CustomParallelDesigner"
      xmlns="http://schemas.microsoft.com/winfx/2006/xaml/presentation"
      xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml"
      xmlns:sad="clr-namespace:System.Activities.Design;assembly=System.Activities.Design"
      xmlns:sadv="clr-namespace:System.Activities.Design.View;assembly=System.Activities.Design">
    <sad:ActivityDesigner.Resources>
      <DataTemplate x:Key="Expanded">
        <StackPanel>
          <TextBlock>This is the Expanded View</TextBlock>
          <sad:WorkflowItemsPresenter HintText="Drop Activities Here"
                                      Items="{Binding Path=ModelItem.Branches}">
            <sad:WorkflowItemsPresenter.SpacerTemplate>
              <DataTemplate>
                <Ellipse Width="10" Height="10" Fill="Black"/>
              </DataTemplate>
            </sad:WorkflowItemsPresenter.SpacerTemplate>
            <sad:WorkflowItemsPresenter.ItemsPanel>
              <ItemsPanelTemplate>
                <StackPanel Orientation="Horizontal"/>
              </ItemsPanelTemplate>
            </sad:WorkflowItemsPresenter.ItemsPanel>
          </sad:WorkflowItemsPresenter>
        </StackPanel>
      </DataTemplate>
      <DataTemplate x:Key="Collapsed">
        <TextBlock>This is the Collapsed View</TextBlock>
      </DataTemplate>
      <Style x:Key="ExpandOrCollapsedStyle" TargetType="{x:Type ContentPresenter}">
        <Setter Property="ContentTemplate" Value="{DynamicResource Collapsed}"/>
        <Style.Triggers>
          <DataTrigger Binding="{Binding Path=IsRootDesigner}" Value="true">
            <Setter Property="ContentTemplate" Value="{DynamicResource Expanded}"/>
          </DataTrigger>
        </Style.Triggers>
      </Style>
    </sad: ActivityDesigner.Resources>
    <Grid>
      <ContentPresenter Style="{DynamicResource ExpandOrCollapsedStyle}" Content="{Binding}"/>
    </Grid>
  </sad: ActivityDesigner>
  ```

> [!IMPORTANT]
> <span data-ttu-id="92d30-132">您的计算机上可能已安装这些示例。</span><span class="sxs-lookup"><span data-stu-id="92d30-132">The samples may already be installed on your machine.</span></span> <span data-ttu-id="92d30-133">在继续操作之前，请先检查以下（默认）目录：</span><span class="sxs-lookup"><span data-stu-id="92d30-133">Check for the following (default) directory before continuing.</span></span>
>
> `<InstallDrive>:\WF_WCF_Samples`
>
> <span data-ttu-id="92d30-134">如果此目录不存在，请参阅[Windows Communication Foundation (wcf) ，并 Windows Workflow Foundation (的 WF](https://www.microsoft.com/download/details.aspx?id=21459)) .NET Framework Windows Communication Foundation ([!INCLUDE[wf1](../../../../includes/wf1-md.md)]</span><span class="sxs-lookup"><span data-stu-id="92d30-134">If this directory does not exist, go to [Windows Communication Foundation (WCF) and Windows Workflow Foundation (WF) Samples for .NET Framework 4](https://www.microsoft.com/download/details.aspx?id=21459) to download all Windows Communication Foundation (WCF) and [!INCLUDE[wf1](../../../../includes/wf1-md.md)] samples.</span></span> <span data-ttu-id="92d30-135">此示例位于以下目录：</span><span class="sxs-lookup"><span data-stu-id="92d30-135">This sample is located in the following directory.</span></span>
>
> `<InstallDrive>:\WF_WCF_Samples\WF\Basic\CustomActivities\CustomActivityDesigners\WorkflowItemsPresenter`

## <a name="see-also"></a><span data-ttu-id="92d30-136">请参阅</span><span class="sxs-lookup"><span data-stu-id="92d30-136">See also</span></span>

- <xref:System.Activities.Presentation.WorkflowItemsPresenter>
- [<span data-ttu-id="92d30-137">使用工作流设计器开发应用程序</span><span class="sxs-lookup"><span data-stu-id="92d30-137">Developing Applications with the Workflow Designer</span></span>](/visualstudio/workflow-designer/developing-applications-with-the-workflow-designer)
