---
description: 了解详细信息：删除设计器添加到 XAML 文件的视图状态
title: 删除设计器添加到 XAML 文件的视图状态-WF
ms.date: 03/30/2017
ms.assetid: a801ce22-8699-483c-a392-7bb3834aae4f
ms.openlocfilehash: e6be1e8e4f754085b98f912923ad67cb12893910
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99741791"
---
# <a name="removing-the-view-state-the-designer-adds-to-an-xaml-file"></a><span data-ttu-id="da26e-103">删除设计器添加到 XAML 文件的视图状态</span><span class="sxs-lookup"><span data-stu-id="da26e-103">Removing the view state the designer adds to an XAML file</span></span>

<span data-ttu-id="da26e-104">此示例演示如何创建派生自 <xref:System.Xaml.XamlWriter> 的类以及如何从 XAML 文件中移除视图状态。</span><span class="sxs-lookup"><span data-stu-id="da26e-104">This sample demonstrates how to create a class that derives from <xref:System.Xaml.XamlWriter> and removes view state from a XAML file.</span></span> <span data-ttu-id="da26e-105">Windows 工作流设计器将信息写入 XAML 文档，该文档称为视图状态。</span><span class="sxs-lookup"><span data-stu-id="da26e-105">Windows Workflow Designer writes information into the XAML document, which is known as view state.</span></span> <span data-ttu-id="da26e-106">视图状态是指设计时所需的信息（如布局定位），运行时不需要此信息。</span><span class="sxs-lookup"><span data-stu-id="da26e-106">View state refers to the information that is required at design time, such as layout positioning, that is not required at runtime.</span></span> <span data-ttu-id="da26e-107">工作流设计器在编辑时将此信息插入到 XAML 文档中。</span><span class="sxs-lookup"><span data-stu-id="da26e-107">Workflow Designer inserts this information into the XAML document as it is edited.</span></span> <span data-ttu-id="da26e-108">工作流设计器用特性将视图状态写入 XAML 文件 `mc:Ignorable` 中，因此在运行时加载 XAML 文件时不会加载此信息。</span><span class="sxs-lookup"><span data-stu-id="da26e-108">Workflow Designer writes the view state into the XAML file with the `mc:Ignorable` attribute, so this information is not loaded when the runtime loads the XAML file.</span></span> <span data-ttu-id="da26e-109">此示例演示如何创建一个类，此类将在处理 XAML 节点时移除视图状态信息。</span><span class="sxs-lookup"><span data-stu-id="da26e-109">This sample demonstrates how to create a class that removes that view state information while processing XAML nodes.</span></span>

## <a name="discussion"></a><span data-ttu-id="da26e-110">讨论 (Discussion)</span><span class="sxs-lookup"><span data-stu-id="da26e-110">Discussion</span></span>

<span data-ttu-id="da26e-111">此示例演示如何创建自定义编写器。</span><span class="sxs-lookup"><span data-stu-id="da26e-111">This sample demonstrates how to create a custom writer.</span></span>

<span data-ttu-id="da26e-112">若要生成自定义 XAML 编写器，请创建一个从 <xref:System.Xaml.XamlWriter> 继承的类。</span><span class="sxs-lookup"><span data-stu-id="da26e-112">To build a custom XAML writer, create a class that inherits from <xref:System.Xaml.XamlWriter>.</span></span> <span data-ttu-id="da26e-113">由于 XAML 编写器经常嵌套，因此通常需要跟踪 "内部" XAML 编写器。</span><span class="sxs-lookup"><span data-stu-id="da26e-113">As XAML writers are often nested, it is typical to keep track of an "inner" XAML writer.</span></span> <span data-ttu-id="da26e-114">这些 "内部" 编写器可以被视为引用 XAML 编写器的剩余堆栈，使您可以有多个入口点来完成工作，然后将处理委托给堆栈的其余部分。</span><span class="sxs-lookup"><span data-stu-id="da26e-114">These "inner’ writers can be thought of as the reference to the remaining stack of XAML writers, allowing you to have multiple entry points to do work and then delegate processing to the remainder of the stack.</span></span>

<span data-ttu-id="da26e-115">在此示例中，有几个需要注意的地方。</span><span class="sxs-lookup"><span data-stu-id="da26e-115">In this sample, there are a few items of interest.</span></span> <span data-ttu-id="da26e-116">其中一个需要注意的是，检查要编写的项是否来自某个设计器命名空间。</span><span class="sxs-lookup"><span data-stu-id="da26e-116">One is the check to see whether the item being written is from a designer namespace.</span></span> <span data-ttu-id="da26e-117">请注意，此操作还将消除工作流中对该设计器命名空间的其他类型的使用。</span><span class="sxs-lookup"><span data-stu-id="da26e-117">Note that this also strips out the use of other types from the designer namespace in a workflow.</span></span>

```csharp
static Boolean IsDesignerAttachedProperty(XamlMember xamlMember)
{
    return xamlMember.IsAttachable &&
        xamlMember.PreferredXamlNamespace.Equals(c_sapNamespaceURI, StringComparison.OrdinalIgnoreCase);
}

const String c_sapNamespaceURI = "http://schemas.microsoft.com/netfx/2009/xaml/activities/presentation";

// The next item of interest is the constructor, where the utilization of the inner XAML writer is seen.
public ViewStateCleaningWriter(XamlWriter innerWriter)
{
    this.InnerWriter = innerWriter;
    this.MemberStack = new Stack<XamlMember>();
}

XamlWriter InnerWriter {get; set; }
Stack<XamlMember> MemberStack {get; set; }
```

<span data-ttu-id="da26e-118">另外，此操作还将创建在遍历节点流时使用的 XAML 成员的堆栈。</span><span class="sxs-lookup"><span data-stu-id="da26e-118">This also creates a stack of XAML members that are used while traversing the node stream.</span></span> <span data-ttu-id="da26e-119">此示例的剩余工作主要包含在 `WriteStartMember` 方法中。</span><span class="sxs-lookup"><span data-stu-id="da26e-119">The remaining work of this sample is largely contained in the `WriteStartMember` method.</span></span>

```csharp
public override void WriteStartMember(XamlMember xamlMember)
{
    MemberStack.Push(xamlMember);

    if (IsDesignerAttachedProperty(xamlMember))
    {
        m_attachedPropertyDepth++;
    }

    if (m_attachedPropertyDepth > 0)
    {
        return;
    }

    InnerWriter.WriteStartMember(xamlMember);
}
```

<span data-ttu-id="da26e-120">然后，后续方法将检查它们是否仍包含在视图状态容器中，如果是这样，则返回且不在编写器堆栈中向下传递节点。</span><span class="sxs-lookup"><span data-stu-id="da26e-120">Subsequent methods then check to see whether they are still contained in a view state container, and if so, return, and do not pass the node down the writer stack.</span></span>

```csharp
public override void WriteValue(Object value)
{
    if (m_attachedPropertyDepth > 0)
    {
        return;
    }

    InnerWriter.WriteValue(value);
}
```

<span data-ttu-id="da26e-121">若要使用自定义 XAML 编写器，则必须在 XAML 编写器堆栈中将其链接起来。</span><span class="sxs-lookup"><span data-stu-id="da26e-121">To use a custom XAML writer, you must chain it together in a stack of XAML writers.</span></span> <span data-ttu-id="da26e-122">下面的代码演示如何执行此操作。</span><span class="sxs-lookup"><span data-stu-id="da26e-122">The following code shows how this can be used.</span></span>

```csharp
XmlWriterSettings writerSettings = new XmlWriterSettings {  Indent = true };
XmlWriter xmlWriter = XmlWriter.Create(File.OpenWrite(args[1]), writerSettings);
XamlXmlWriter xamlWriter = new XamlXmlWriter(xmlWriter, new XamlSchemaContext());
XamlServices.Save(new ViewStateCleaningWriter(ActivityXamlServices.CreateBuilderWriter(xamlWriter)), ab);
```

## <a name="to-use-this-sample"></a><span data-ttu-id="da26e-123">使用此示例</span><span class="sxs-lookup"><span data-stu-id="da26e-123">To use this sample</span></span>

1. <span data-ttu-id="da26e-124">使用 Visual Studio 2010 打开 Viewstatecleaningwriter.exe 解决方案文件。</span><span class="sxs-lookup"><span data-stu-id="da26e-124">Using Visual Studio 2010, open the ViewStateCleaningWriter.sln solution file.</span></span>

2. <span data-ttu-id="da26e-125">打开命令提示符，导航到生成 ViewStageCleaningWriter.exe 的目录。</span><span class="sxs-lookup"><span data-stu-id="da26e-125">Open a command prompt and navigate to the directory where the ViewStageCleaningWriter.exe is built.</span></span>

3. <span data-ttu-id="da26e-126">在 Workflow1.xaml 文件上运行 ViewStateCleaningWriter.exe。</span><span class="sxs-lookup"><span data-stu-id="da26e-126">Run ViewStateCleaningWriter.exe on the Workflow1.xaml file.</span></span>

   <span data-ttu-id="da26e-127">下面的示例演示了可执行文件的语法。</span><span class="sxs-lookup"><span data-stu-id="da26e-127">The syntax for the executable is shown in the following example.</span></span>

   ```console
   ViewStateCleaningWriter.exe [input file] [output file]
   ```

   <span data-ttu-id="da26e-128">这会将 XAML 文件输出到 \[ outfile]，并删除其所有的视图状态信息。</span><span class="sxs-lookup"><span data-stu-id="da26e-128">This outputs a XAML file to \[outfile], which has all its view state information removed.</span></span>

> [!NOTE]
> <span data-ttu-id="da26e-129">已为 <xref:System.Activities.Statements.Sequence> 工作流移除大量虚拟化提示。</span><span class="sxs-lookup"><span data-stu-id="da26e-129">For a <xref:System.Activities.Statements.Sequence> workflow, a number of virtualization hints are removed.</span></span> <span data-ttu-id="da26e-130">这将导致设计器在下次加载时重新计算布局。</span><span class="sxs-lookup"><span data-stu-id="da26e-130">This causes the designer to recalculate layout the next time it is loaded.</span></span> <span data-ttu-id="da26e-131">在对 <xref:System.Activities.Statements.Flowchart> 使用此示例时，将移除所有定位和行路由信息，并且在后续加载到设计器中时，所有活动将在屏幕左侧堆叠。</span><span class="sxs-lookup"><span data-stu-id="da26e-131">When you use this sample for a <xref:System.Activities.Statements.Flowchart>, all positioning and line routing information are removed and on subsequent loading into the designer, all activities are stacked on the left side of the screen.</span></span>

## <a name="to-create-a-sample-xaml-file-for-use-with-this-sample"></a><span data-ttu-id="da26e-132">创建与此示例一起使用的示例 XAML 文件</span><span class="sxs-lookup"><span data-stu-id="da26e-132">To create a sample XAML file for use with this sample</span></span>

1. <span data-ttu-id="da26e-133">打开 Visual Studio 2010。</span><span class="sxs-lookup"><span data-stu-id="da26e-133">Open Visual Studio 2010.</span></span>

2. <span data-ttu-id="da26e-134">创建新的工作流控制台应用程序。</span><span class="sxs-lookup"><span data-stu-id="da26e-134">Create a new Workflow Console Application.</span></span>

3. <span data-ttu-id="da26e-135">将几个活动拖放到画布上。</span><span class="sxs-lookup"><span data-stu-id="da26e-135">Drag and drop a few activities onto the canvas</span></span>

4. <span data-ttu-id="da26e-136">保存工作流 XAML 文件。</span><span class="sxs-lookup"><span data-stu-id="da26e-136">Save the workflow XAML file.</span></span>

5. <span data-ttu-id="da26e-137">检测 XAML 文件以查看视图状态附加属性。</span><span class="sxs-lookup"><span data-stu-id="da26e-137">Inspect the XAML file to see the view state attached properties.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="da26e-138">您的计算机上可能已安装这些示例。</span><span class="sxs-lookup"><span data-stu-id="da26e-138">The samples may already be installed on your machine.</span></span> <span data-ttu-id="da26e-139">在继续操作之前，请先检查以下（默认）目录：</span><span class="sxs-lookup"><span data-stu-id="da26e-139">Check for the following (default) directory before continuing.</span></span>
>
> `<InstallDrive>:\WF_WCF_Samples`
>
> <span data-ttu-id="da26e-140">如果此目录不存在，请参阅[Windows Communication Foundation (wcf) ，并 Windows Workflow Foundation (的 WF](https://www.microsoft.com/download/details.aspx?id=21459)) .NET Framework Windows Communication Foundation ([!INCLUDE[wf1](../../../../includes/wf1-md.md)]</span><span class="sxs-lookup"><span data-stu-id="da26e-140">If this directory does not exist, go to [Windows Communication Foundation (WCF) and Windows Workflow Foundation (WF) Samples for .NET Framework 4](https://www.microsoft.com/download/details.aspx?id=21459) to download all Windows Communication Foundation (WCF) and [!INCLUDE[wf1](../../../../includes/wf1-md.md)] samples.</span></span> <span data-ttu-id="da26e-141">此示例位于以下目录：</span><span class="sxs-lookup"><span data-stu-id="da26e-141">This sample is located in the following directory.</span></span>
>
> `<InstallDrive>:\WF_WCF_Samples\WF\Basic\Designer\ViewStateCleaningWriter`
