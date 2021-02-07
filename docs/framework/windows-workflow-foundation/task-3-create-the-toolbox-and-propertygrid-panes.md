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
# <a name="task-3-create-the-toolbox-and-propertygrid-panes"></a>任务 3：创建工具箱窗格和属性网格窗格

在此任务中，将创建 " **工具箱** " 和 " **PropertyGrid** " 窗格，并将其添加到重新承载 Windows 工作流设计器。

若要参考，MainWindow.xaml.cs 文件中的三个任务完成后，应在重新承载文件中的代码在本主题末尾提供了 [工作流设计器](rehosting-the-workflow-designer.md) 系列主题。

## <a name="to-create-the-toolbox-and-add-it-to-the-grid"></a>创建工具箱并将其添加到网格中

1. 按照 [任务2：承载工作流设计器](task-2-host-the-workflow-designer.md)中所述的过程操作，打开所获得的 HostingApplication 项目。

2. 在 **解决方案资源管理器** 窗格中，右键单击 *mainwindow.xaml* 文件，然后选择 " **查看代码**"。

3. 向 `GetToolboxControl` `MainWindow` 创建的类添加方法 <xref:System.Activities.Presentation.Toolbox.ToolboxControl> ，将新的 **"工具箱** " 类别添加到 " **工具箱**"，并将 <xref:System.Activities.Statements.Assign> 和 <xref:System.Activities.Statements.Sequence> 活动类型分配给该类别。

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

4. 向类添加一个私有 `AddToolbox` 方法 `MainWindow` ，该方法将 " **工具箱** " 放置在网格上的左列中。

    ```csharp
    private void AddToolBox()
    {
        ToolboxControl tc = GetToolboxControl();
        Grid.SetColumn(tc, 0);
        grid1.Children.Add(tc);
    }
    ```

5. `AddToolBox`在类构造函数中添加对方法的调用 `MainWindow()` ，如以下代码所示：

    ```csharp
    public MainWindow()
    {
        InitializeComponent();
        this.RegisterMetadata();
        this.AddDesigner();

        this.AddToolBox();
    }
    ```

6. 按 <kbd>F5</kbd> 生成并运行解决方案。 应显示包含和活动的 " **工具箱** " <xref:System.Activities.Statements.Assign> <xref:System.Activities.Statements.Sequence> 。

## <a name="to-create-the-propertygrid"></a>创建属性网格

1. 在 **解决方案资源管理器** 窗格中，右键单击 *mainwindow.xaml* 文件，然后选择 " **查看代码**"。

2. 将 `AddPropertyInspector` 方法添加到 `MainWindow` 类，以便将 " **PropertyGrid** " 窗格放置在网格上的最右侧列中：

    ```csharp
    private void AddPropertyInspector()
    {
        Grid.SetColumn(wd.PropertyInspectorView, 2);
        grid1.Children.Add(wd.PropertyInspectorView);
    }
    ```

3. `AddPropertyInspector`在类构造函数中添加对方法的调用 `MainWindow()` ，如以下代码所示：

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

4. 按 <kbd>F5</kbd> 生成并运行解决方案。 " **工具箱**"、"工作流设计画布" 和 " **PropertyGrid** " 窗格应全部显示，将 <xref:System.Activities.Statements.Assign> 活动或 <xref:System.Activities.Statements.Sequence> 活动拖到设计画布上时，属性网格应根据突出显示的活动进行更新。

## <a name="example"></a>示例

*MainWindow.xaml.cs* 文件现在应包含以下代码：

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

## <a name="see-also"></a>请参阅

- [重新承载工作流设计器](rehosting-the-workflow-designer.md)
- [任务 1：创建一个新的 Windows Presentation Foundation 应用程序](task-1-create-a-new-wpf-app.md)
- [任务 2：承载工作流设计器](task-2-host-the-workflow-designer.md)
