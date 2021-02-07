---
description: 了解详细信息：任务3：创建工具箱和 PropertyGrid 窗格
title: 任务 3：创建工具箱窗格和属性网格窗格
ms.date: 03/30/2017
ms.assetid: 72c1546a-eed5-4f0f-a616-719a163414f4
ms.openlocfilehash: c07bfc2f974018cb0d789a6cc1181f9bed861382
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99755157"
---
# <a name="task-3-create-the-toolbox-and-propertygrid-panes"></a><span data-ttu-id="f364a-103">任务 3：创建工具箱窗格和属性网格窗格</span><span class="sxs-lookup"><span data-stu-id="f364a-103">Task 3: Create the Toolbox and PropertyGrid Panes</span></span>

<span data-ttu-id="f364a-104">在此任务中，将创建 " **工具箱** " 和 " **PropertyGrid** " 窗格，并将其添加到重新承载 Windows 工作流设计器。</span><span class="sxs-lookup"><span data-stu-id="f364a-104">In this task, you will create the **Toolbox** and **PropertyGrid** panes and add them to the rehosted Windows Workflow Designer.</span></span>

<span data-ttu-id="f364a-105">若要参考，MainWindow.xaml.cs 文件中的三个任务完成后，应在重新承载文件中的代码在本主题末尾提供了 [工作流设计器](rehosting-the-workflow-designer.md) 系列主题。</span><span class="sxs-lookup"><span data-stu-id="f364a-105">For reference, the code that should be in the MainWindow.xaml.cs file after completing the three tasks in the [Rehosting the Workflow Designer](rehosting-the-workflow-designer.md) series of topics is provided at the end of this topic.</span></span>

## <a name="to-create-the-toolbox-and-add-it-to-the-grid"></a><span data-ttu-id="f364a-106">创建工具箱并将其添加到网格中</span><span class="sxs-lookup"><span data-stu-id="f364a-106">To create the Toolbox and add it to the grid</span></span>

1. <span data-ttu-id="f364a-107">按照 [任务2：承载工作流设计器](task-2-host-the-workflow-designer.md)中所述的过程操作，打开所获得的 HostingApplication 项目。</span><span class="sxs-lookup"><span data-stu-id="f364a-107">Open the HostingApplication project you obtained by following the procedure described in [Task 2: Host the Workflow Designer](task-2-host-the-workflow-designer.md).</span></span>

2. <span data-ttu-id="f364a-108">在 **解决方案资源管理器** 窗格中，右键单击 *mainwindow.xaml* 文件，然后选择 " **查看代码**"。</span><span class="sxs-lookup"><span data-stu-id="f364a-108">In the **Solution Explorer** pane, right-click the *MainWindow.xaml* file and select **View Code**.</span></span>

3. <span data-ttu-id="f364a-109">向 `GetToolboxControl` `MainWindow` 创建的类添加方法 <xref:System.Activities.Presentation.Toolbox.ToolboxControl> ，将新的 **"工具箱** " 类别添加到 " **工具箱**"，并将 <xref:System.Activities.Statements.Assign> 和 <xref:System.Activities.Statements.Sequence> 活动类型分配给该类别。</span><span class="sxs-lookup"><span data-stu-id="f364a-109">Add a `GetToolboxControl` method to the `MainWindow` class that creates a <xref:System.Activities.Presentation.Toolbox.ToolboxControl>, adds a new **Toolbox** category to the **Toolbox**, and assigns the <xref:System.Activities.Statements.Assign> and <xref:System.Activities.Statements.Sequence> activity types to that category.</span></span>

    ```csharp
    private ToolboxControl GetToolboxControl()
    {
        // Create the ToolBoxControl.
        var ctrl = new ToolboxControl();

        // Create a category.
        var category = new ToolboxCategory("category1");

        // Create Toolbox items.
        var tool1 =
            new ToolboxItemWrapper("System.Activities.Statements.Assign",
            typeof(Assign).Assembly.FullName, null, "Assign");

        var tool2 = new ToolboxItemWrapper("System.Activities.Statements.Sequence",
            typeof(Sequence).Assembly.FullName, null, "Sequence");

        // Add the Toolbox items to the category.
        category.Add(tool1);
        category.Add(tool2);

        // Add the category to the ToolBox control.
        ctrl.Categories.Add(category);
        return ctrl;
    }
    ```

4. <span data-ttu-id="f364a-110">向类添加一个私有 `AddToolbox` 方法 `MainWindow` ，该方法将 " **工具箱** " 放置在网格上的左列中。</span><span class="sxs-lookup"><span data-stu-id="f364a-110">Add a private `AddToolbox` method to the `MainWindow` class that places the **Toolbox** in the left column on the grid.</span></span>

    ```csharp
    private void AddToolBox()
    {
        ToolboxControl tc = GetToolboxControl();
        Grid.SetColumn(tc, 0);
        grid1.Children.Add(tc);
    }
    ```

5. <span data-ttu-id="f364a-111">`AddToolBox`在类构造函数中添加对方法的调用 `MainWindow()` ，如以下代码所示：</span><span class="sxs-lookup"><span data-stu-id="f364a-111">Add a call to the `AddToolBox` method in the `MainWindow()` class constructor as shown in the following code:</span></span>

    ```csharp
    public MainWindow()
    {
        InitializeComponent();
        this.RegisterMetadata();
        this.AddDesigner();

        this.AddToolBox();
    }
    ```

6. <span data-ttu-id="f364a-112">按 <kbd>F5</kbd> 生成并运行解决方案。</span><span class="sxs-lookup"><span data-stu-id="f364a-112">Press <kbd>F5</kbd> to build and run your solution.</span></span> <span data-ttu-id="f364a-113">应显示包含和活动的 " **工具箱** " <xref:System.Activities.Statements.Assign> <xref:System.Activities.Statements.Sequence> 。</span><span class="sxs-lookup"><span data-stu-id="f364a-113">The **Toolbox** containing the <xref:System.Activities.Statements.Assign> and <xref:System.Activities.Statements.Sequence> activities should be displayed.</span></span>

## <a name="to-create-the-propertygrid"></a><span data-ttu-id="f364a-114">创建属性网格</span><span class="sxs-lookup"><span data-stu-id="f364a-114">To create the PropertyGrid</span></span>

1. <span data-ttu-id="f364a-115">在 **解决方案资源管理器** 窗格中，右键单击 *mainwindow.xaml* 文件，然后选择 " **查看代码**"。</span><span class="sxs-lookup"><span data-stu-id="f364a-115">In the **Solution Explorer** pane, right-click the *MainWindow.xaml* file and select **View Code**.</span></span>

2. <span data-ttu-id="f364a-116">将 `AddPropertyInspector` 方法添加到 `MainWindow` 类，以便将 " **PropertyGrid** " 窗格放置在网格上的最右侧列中：</span><span class="sxs-lookup"><span data-stu-id="f364a-116">Add the `AddPropertyInspector` method to the `MainWindow` class to place the **PropertyGrid** pane in the rightmost column on the grid:</span></span>

    ```csharp
    private void AddPropertyInspector()
    {
        Grid.SetColumn(wd.PropertyInspectorView, 2);
        grid1.Children.Add(wd.PropertyInspectorView);
    }
    ```

3. <span data-ttu-id="f364a-117">`AddPropertyInspector`在类构造函数中添加对方法的调用 `MainWindow()` ，如以下代码所示：</span><span class="sxs-lookup"><span data-stu-id="f364a-117">Add a call to the `AddPropertyInspector` method in the `MainWindow()` class constructor as shown in the following code:</span></span>

    ```csharp
    public MainWindow()
    {
        InitializeComponent();
        this.RegisterMetadata();
        this.AddDesigner();
        this.AddToolBox();

        this.AddPropertyInspector();
    }
    ```

4. <span data-ttu-id="f364a-118">按 <kbd>F5</kbd> 生成并运行解决方案。</span><span class="sxs-lookup"><span data-stu-id="f364a-118">Press <kbd>F5</kbd> to build and run the solution.</span></span> <span data-ttu-id="f364a-119">" **工具箱**"、"工作流设计画布" 和 " **PropertyGrid** " 窗格应全部显示，将 <xref:System.Activities.Statements.Assign> 活动或 <xref:System.Activities.Statements.Sequence> 活动拖到设计画布上时，属性网格应根据突出显示的活动进行更新。</span><span class="sxs-lookup"><span data-stu-id="f364a-119">The **Toolbox**, workflow design canvas, and **PropertyGrid** panes should all be displayed, and when you drag an <xref:System.Activities.Statements.Assign> activity or a <xref:System.Activities.Statements.Sequence> activity onto the design canvas, the property grid should update depending on the highlighted activity.</span></span>

## <a name="example"></a><span data-ttu-id="f364a-120">示例</span><span class="sxs-lookup"><span data-stu-id="f364a-120">Example</span></span>

<span data-ttu-id="f364a-121">*MainWindow.xaml.cs* 文件现在应包含以下代码：</span><span class="sxs-lookup"><span data-stu-id="f364a-121">The *MainWindow.xaml.cs* file should now contain the following code:</span></span>

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Windows;
using System.Windows.Controls;
using System.Windows.Data;
using System.Windows.Documents;
using System.Windows.Input;
using System.Windows.Media;
using System.Windows.Media.Imaging;
using System.Windows.Navigation;
using System.Windows.Shapes;
// dlls added.
using System.Activities;
using System.Activities.Core.Presentation;
using System.Activities.Presentation;
using System.Activities.Presentation.Metadata;
using System.Activities.Presentation.Toolbox;
using System.Activities.Statements;
using System.ComponentModel;

namespace HostingApplication
{
    /// <summary>
    /// Interaction logic for MainWindow.xaml
    /// </summary>
    public partial class MainWindow : Window
    {
        private WorkflowDesigner wd;

        public MainWindow()
        {
            InitializeComponent();
            RegisterMetadata();
            AddDesigner();
            this.AddToolBox();
            this.AddPropertyInspector();
        }

        private void AddDesigner()
        {
            // Create an instance of WorkflowDesigner class.
            this.wd = new WorkflowDesigner();

            // Place the designer canvas in the middle column of the grid.
            Grid.SetColumn(this.wd.View, 1);

            // Load a new Sequence as default.
            this.wd.Load(new Sequence());

            // Add the designer canvas to the grid.
            grid1.Children.Add(this.wd.View);
        }

        private void RegisterMetadata()
        {
            var dm = new DesignerMetadata();
            dm.Register();
        }

        private ToolboxControl GetToolboxControl()
        {
            // Create the ToolBoxControl.
            var ctrl = new ToolboxControl();

            // Create a category.
            var category = new ToolboxCategory("category1");

            // Create Toolbox items.
            var tool1 =
                new ToolboxItemWrapper("System.Activities.Statements.Assign",
                typeof(Assign).Assembly.FullName, null, "Assign");

            var tool2 = new ToolboxItemWrapper("System.Activities.Statements.Sequence",
                typeof(Sequence).Assembly.FullName, null, "Sequence");

            // Add the Toolbox items to the category.
            category.Add(tool1);
            category.Add(tool2);

            // Add the category to the ToolBox control.
            ctrl.Categories.Add(category);
            return ctrl;
        }

        private void AddToolBox()
        {
            ToolboxControl tc = GetToolboxControl();
            Grid.SetColumn(tc, 0);
            grid1.Children.Add(tc);
        }

        private void AddPropertyInspector()
        {
            Grid.SetColumn(wd.PropertyInspectorView, 2);
            grid1.Children.Add(wd.PropertyInspectorView);
        }

    }
}
```

## <a name="see-also"></a><span data-ttu-id="f364a-122">请参阅</span><span class="sxs-lookup"><span data-stu-id="f364a-122">See also</span></span>

- [<span data-ttu-id="f364a-123">重新承载工作流设计器</span><span class="sxs-lookup"><span data-stu-id="f364a-123">Rehosting the Workflow Designer</span></span>](rehosting-the-workflow-designer.md)
- [<span data-ttu-id="f364a-124">任务 1：创建一个新的 Windows Presentation Foundation 应用程序</span><span class="sxs-lookup"><span data-stu-id="f364a-124">Task 1: Create a New Windows Presentation Foundation Application</span></span>](task-1-create-a-new-wpf-app.md)
- [<span data-ttu-id="f364a-125">任务 2：承载工作流设计器</span><span class="sxs-lookup"><span data-stu-id="f364a-125">Task 2: Host the Workflow Designer</span></span>](task-2-host-the-workflow-designer.md)
