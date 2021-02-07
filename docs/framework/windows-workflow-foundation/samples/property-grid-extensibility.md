---
description: 了解详细信息：属性网格扩展性
title: 属性网格扩展性-WF 示例
ms.date: 03/30/2017
ms.assetid: 3530c3a3-756d-4712-9f10-fb2897414d3a
ms.openlocfilehash: 784705146974ffca5cd2e6c21dba722598544771
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99741804"
---
# <a name="property-grid-extensibility"></a><span data-ttu-id="5f757-103">属性网格扩展性</span><span class="sxs-lookup"><span data-stu-id="5f757-103">Property grid extensibility</span></span>

<span data-ttu-id="5f757-104">开发人员可以自定义属性网格，此网格将在设计器中选择给定活动时显示。</span><span class="sxs-lookup"><span data-stu-id="5f757-104">A developer can customize the property grid that is displayed when a given activity is selected within the designer.</span></span> <span data-ttu-id="5f757-105">执行此操作可获得丰富的编辑体验。</span><span class="sxs-lookup"><span data-stu-id="5f757-105">This can be done to create a rich editing experience.</span></span> <span data-ttu-id="5f757-106">此示例演示如何完成此操作。</span><span class="sxs-lookup"><span data-stu-id="5f757-106">This sample shows how this can be done.</span></span>

## <a name="demonstrates"></a><span data-ttu-id="5f757-107">演示</span><span class="sxs-lookup"><span data-stu-id="5f757-107">Demonstrates</span></span>

<span data-ttu-id="5f757-108">工作流设计器属性网格的扩展性。</span><span class="sxs-lookup"><span data-stu-id="5f757-108">Workflow designer property grid extensibility.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5f757-109">您的计算机上可能已安装这些示例。</span><span class="sxs-lookup"><span data-stu-id="5f757-109">The samples may already be installed on your machine.</span></span> <span data-ttu-id="5f757-110">在继续操作之前，请先检查以下（默认）目录：</span><span class="sxs-lookup"><span data-stu-id="5f757-110">Check for the following (default) directory before continuing.</span></span>
>
> `<InstallDrive>:\WF_WCF_Samples`
>
> <span data-ttu-id="5f757-111">如果此目录不存在，请参阅[Windows Communication Foundation (wcf) ，并 Windows Workflow Foundation (的 WF](https://www.microsoft.com/download/details.aspx?id=21459)) .NET Framework Windows Communication Foundation ([!INCLUDE[wf1](../../../../includes/wf1-md.md)]</span><span class="sxs-lookup"><span data-stu-id="5f757-111">If this directory does not exist, go to [Windows Communication Foundation (WCF) and Windows Workflow Foundation (WF) Samples for .NET Framework 4](https://www.microsoft.com/download/details.aspx?id=21459) to download all Windows Communication Foundation (WCF) and [!INCLUDE[wf1](../../../../includes/wf1-md.md)] samples.</span></span> <span data-ttu-id="5f757-112">此示例位于以下目录：</span><span class="sxs-lookup"><span data-stu-id="5f757-112">This sample is located in the following directory.</span></span>
>
> `<InstallDrive>:\WF_WCF_Samples\WF\Basic\Designer\PropertyGridExtensibility`

## <a name="discussion"></a><span data-ttu-id="5f757-113">讨论 (Discussion)</span><span class="sxs-lookup"><span data-stu-id="5f757-113">Discussion</span></span>

<span data-ttu-id="5f757-114">若要扩展属性网格，开发人员可以选择自定义属性网格编辑器的内联外观或提供一个为更高级的编辑图面显示的对话框。</span><span class="sxs-lookup"><span data-stu-id="5f757-114">To extend the property grid, a developer has options to customize the inline appearance of a property grid editor or provide a dialog that appears for a more advanced editing surface.</span></span> <span data-ttu-id="5f757-115">此示例中演示了两类不同的编辑器；即内联编辑器和对话框编辑器。</span><span class="sxs-lookup"><span data-stu-id="5f757-115">There are two different editors demonstrated in this sample; an inline editor and a dialog editor.</span></span>

## <a name="inline-editor"></a><span data-ttu-id="5f757-116">内联编辑器</span><span class="sxs-lookup"><span data-stu-id="5f757-116">Inline editor</span></span>

<span data-ttu-id="5f757-117">内联编辑器示例将演示如下内容：</span><span class="sxs-lookup"><span data-stu-id="5f757-117">The inline editor sample demonstrates the following:</span></span>

- <span data-ttu-id="5f757-118">创建一个从 <xref:System.Activities.Presentation.PropertyEditing.PropertyValueEditor> 派生的类型。</span><span class="sxs-lookup"><span data-stu-id="5f757-118">Creates a type that derives from <xref:System.Activities.Presentation.PropertyEditing.PropertyValueEditor>.</span></span>

- <span data-ttu-id="5f757-119">在构造函数中， <xref:System.Activities.Presentation.PropertyEditing.PropertyValueEditor.InlineEditorTemplate%2A> 使用 Windows Presentation Foundation (WPF) 数据模板设置值。</span><span class="sxs-lookup"><span data-stu-id="5f757-119">In the constructor, the <xref:System.Activities.Presentation.PropertyEditing.PropertyValueEditor.InlineEditorTemplate%2A> value is set with a Windows Presentation Foundation (WPF) data template.</span></span> <span data-ttu-id="5f757-120">虽然可以将其绑定到 XAML 模板，但在此示例中，代码用于初始化数据绑定。</span><span class="sxs-lookup"><span data-stu-id="5f757-120">This can be bound to a XAML template, but in this sample, code is used to initialize data binding.</span></span>

- <span data-ttu-id="5f757-121">数据模板具有在属性网格中呈现的项的 <xref:System.Activities.Presentation.PropertyEditing.PropertyValue> 的数据上下文。</span><span class="sxs-lookup"><span data-stu-id="5f757-121">The data template has a data context of the <xref:System.Activities.Presentation.PropertyEditing.PropertyValue> of the item rendered in the property grid.</span></span> <span data-ttu-id="5f757-122">请注意，在下面的代码（此代码来自 CustomInlineEditor.cs）中，稍后会将此上下文绑定到 `Value` 属性。</span><span class="sxs-lookup"><span data-stu-id="5f757-122">Note in the following code (from CustomInlineEditor.cs) that this context then binds to the `Value` property.</span></span>

    ```csharp
    FrameworkElementFactory stack = new FrameworkElementFactory(typeof(StackPanel));
    FrameworkElementFactory slider = new FrameworkElementFactory(typeof(Slider));
    Binding sliderBinding = new Binding("Value");
    sliderBinding.Mode = BindingMode.TwoWay;
    slider.SetValue(Slider.MinimumProperty, 0.0);
    slider.SetValue(Slider.MaximumProperty, 100.0);
    slider.SetValue(Slider.ValueProperty, sliderBinding);
    stack.AppendChild(slider);
    ```

- <span data-ttu-id="5f757-123">由于活动和设计器位于同一个程序集中，因此将在活动自身的静态构造函数中完成对活动设计器特性的注册，如 SimpleCodeActivity.cs 中的以下示例所示。</span><span class="sxs-lookup"><span data-stu-id="5f757-123">Because the activity and the designer are in the same assembly, registration of the activity designer attributes are accomplished in the static constructor of the activity itself, as shown in the following example from SimpleCodeActivity.cs.</span></span>

    ```csharp
    static SimpleCodeActivity()
    {
        AttributeTableBuilder builder = new AttributeTableBuilder();
        builder.AddCustomAttributes(typeof(SimpleCodeActivity), "RepeatCount", new EditorAttribute(typeof(CustomInlineEditor), typeof(PropertyValueEditor)));
        builder.AddCustomAttributes(typeof(SimpleCodeActivity), "FileName", new EditorAttribute(typeof(FilePickerEditor), typeof(DialogPropertyValueEditor)));
        MetadataStore.AddAttributeTable(builder.CreateTable());
    }
    ```

## <a name="dialog-editor"></a><span data-ttu-id="5f757-124">对话框编辑器</span><span class="sxs-lookup"><span data-stu-id="5f757-124">Dialog editor</span></span>

<span data-ttu-id="5f757-125">对话框编辑器示例将演示如下内容：</span><span class="sxs-lookup"><span data-stu-id="5f757-125">The dialog editor sample demonstrates the following:</span></span>

1. <span data-ttu-id="5f757-126">创建一个从 <xref:System.Activities.Presentation.PropertyEditing.DialogPropertyValueEditor> 派生的类型。</span><span class="sxs-lookup"><span data-stu-id="5f757-126">Creates a type that derives from <xref:System.Activities.Presentation.PropertyEditing.DialogPropertyValueEditor>.</span></span>

2. <span data-ttu-id="5f757-127"><xref:System.Activities.Presentation.PropertyEditing.PropertyValueEditor.InlineEditorTemplate%2A>使用 WPF 数据模板设置构造函数中的值。</span><span class="sxs-lookup"><span data-stu-id="5f757-127">Sets the <xref:System.Activities.Presentation.PropertyEditing.PropertyValueEditor.InlineEditorTemplate%2A> value in the constructor with a WPF data template.</span></span> <span data-ttu-id="5f757-128">可以在 XAML 中创建该值，但在此示例中，将在代码中创建它。</span><span class="sxs-lookup"><span data-stu-id="5f757-128">This can be created in XAML, but in this sample, this is created in code.</span></span>

3. <span data-ttu-id="5f757-129">数据模板具有在属性网格中呈现的项的 <xref:System.Activities.Presentation.PropertyEditing.PropertyValue> 的数据上下文。</span><span class="sxs-lookup"><span data-stu-id="5f757-129">The data template has a data context of the <xref:System.Activities.Presentation.PropertyEditing.PropertyValue> of the item rendered in the property grid.</span></span> <span data-ttu-id="5f757-130">在下面的代码中，稍后会将其绑定到 `Value` 属性。</span><span class="sxs-lookup"><span data-stu-id="5f757-130">In the following code, this then binds to the `Value` property.</span></span> <span data-ttu-id="5f757-131">此外，包含 <xref:System.Activities.Presentation.PropertyEditing.EditModeSwitchButton> 以提供引发 FilePickerEditor.cs 中的对话框的按钮也很重要。</span><span class="sxs-lookup"><span data-stu-id="5f757-131">It is critical to also include an <xref:System.Activities.Presentation.PropertyEditing.EditModeSwitchButton> to provide the button that raises the dialog in FilePickerEditor.cs.</span></span>

    ```csharp
    this.InlineEditorTemplate = new DataTemplate();

    FrameworkElementFactory stack = new FrameworkElementFactory(typeof(StackPanel));
    stack.SetValue(StackPanel.OrientationProperty, Orientation.Horizontal);
    FrameworkElementFactory label = new FrameworkElementFactory(typeof(Label));
    Binding labelBinding = new Binding("Value");
    label.SetValue(Label.ContentProperty, labelBinding);
    label.SetValue(Label.MaxWidthProperty, 90.0);

    stack.AppendChild(label);

    FrameworkElementFactory editModeSwitch = new FrameworkElementFactory(typeof(EditModeSwitchButton));

    editModeSwitch.SetValue(EditModeSwitchButton.TargetEditModeProperty, PropertyContainerEditMode.Dialog);

    stack.AppendChild(editModeSwitch);

    this.InlineEditorTemplate.VisualTree = stack;
    ```

4. <span data-ttu-id="5f757-132">重写设计器类型中的 <xref:System.Activities.Presentation.PropertyEditing.DialogPropertyValueEditor.ShowDialog%2A> 方法以处理对话框的显示。</span><span class="sxs-lookup"><span data-stu-id="5f757-132">Overrides the <xref:System.Activities.Presentation.PropertyEditing.DialogPropertyValueEditor.ShowDialog%2A> method in the designer type to handle the display of the dialog.</span></span> <span data-ttu-id="5f757-133">在此示例中，显示了基本 <xref:System.Windows.Forms.FileDialog>。</span><span class="sxs-lookup"><span data-stu-id="5f757-133">In this sample, a basic <xref:System.Windows.Forms.FileDialog> is shown.</span></span>

    ```csharp
    public override void ShowDialog(PropertyValue propertyValue, IInputElement commandSource)
    {
        Microsoft.Win32.OpenFileDialog ofd = new Microsoft.Win32.OpenFileDialog();
        if (ofd.ShowDialog() == true)
        {
            propertyValue.Value = ofd.FileName;
        }
    }
    ```

5. <span data-ttu-id="5f757-134">由于活动和设计器位于同一个程序集中，因此将在活动自身的静态构造函数中完成对活动设计器特性的注册，如 SimpleCodeActivity.cs 中的以下示例所示。</span><span class="sxs-lookup"><span data-stu-id="5f757-134">Because the activity and the designer are in the same assembly, registration of the activity designer attributes are accomplished in the static constructor of the activity itself, as shown in the following example from SimpleCodeActivity.cs.</span></span>

    ```csharp
    static SimpleCodeActivity()
    {
        AttributeTableBuilder builder = new AttributeTableBuilder();
        builder.AddCustomAttributes(typeof(SimpleCodeActivity), "RepeatCount", new EditorAttribute(typeof(CustomInlineEditor), typeof(PropertyValueEditor)));
        builder.AddCustomAttributes(typeof(SimpleCodeActivity), "FileName", new EditorAttribute(typeof(FilePickerEditor), typeof(DialogPropertyValueEditor)));
        MetadataStore.AddAttributeTable(builder.CreateTable());
    }
    ```

## <a name="to-set-up-build-and-run-the-sample"></a><span data-ttu-id="5f757-135">设置、生成和运行示例</span><span class="sxs-lookup"><span data-stu-id="5f757-135">To set up, build, and run the sample</span></span>

1. <span data-ttu-id="5f757-136">生成解决方案，然后打开 Workflow1.xaml。</span><span class="sxs-lookup"><span data-stu-id="5f757-136">Build the solution, and then open Workflow1.xaml.</span></span>

2. <span data-ttu-id="5f757-137">将 **SimpleCodeActivity** 从工具箱拖到设计器画布上。</span><span class="sxs-lookup"><span data-stu-id="5f757-137">Drag a **SimpleCodeActivity** from the toolbox onto the designer canvas.</span></span>

3. <span data-ttu-id="5f757-138">单击 " **SimpleCodeActivity** "，然后打开属性网格，其中有滑块控件和文件选取控件。</span><span class="sxs-lookup"><span data-stu-id="5f757-138">Click the **SimpleCodeActivity** and then open the property grid where there is a slider control and a file picking control.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5f757-139">您的计算机上可能已安装这些示例。</span><span class="sxs-lookup"><span data-stu-id="5f757-139">The samples may already be installed on your machine.</span></span> <span data-ttu-id="5f757-140">在继续操作之前，请先检查以下（默认）目录：</span><span class="sxs-lookup"><span data-stu-id="5f757-140">Check for the following (default) directory before continuing.</span></span>
>
> `<InstallDrive>:\WF_WCF_Samples`
>
> <span data-ttu-id="5f757-141">如果此目录不存在，请参阅[Windows Communication Foundation (wcf) ，并 Windows Workflow Foundation (的 WF](https://www.microsoft.com/download/details.aspx?id=21459)) .NET Framework Windows Communication Foundation ([!INCLUDE[wf1](../../../../includes/wf1-md.md)]</span><span class="sxs-lookup"><span data-stu-id="5f757-141">If this directory does not exist, go to [Windows Communication Foundation (WCF) and Windows Workflow Foundation (WF) Samples for .NET Framework 4](https://www.microsoft.com/download/details.aspx?id=21459) to download all Windows Communication Foundation (WCF) and [!INCLUDE[wf1](../../../../includes/wf1-md.md)] samples.</span></span> <span data-ttu-id="5f757-142">此示例位于以下目录：</span><span class="sxs-lookup"><span data-stu-id="5f757-142">This sample is located in the following directory.</span></span>
>
> `<InstallDrive>:\WF_WCF_Samples\WF\Basic\Designer\PropertyGridExtensibility`
