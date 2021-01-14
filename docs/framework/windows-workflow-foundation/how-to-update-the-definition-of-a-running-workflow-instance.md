---
title: 如何：更新正在运行的工作流实例的定义
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 26dfac36-ae23-4909-9867-62495b55fb5e
ms.openlocfilehash: b94c7564b1ce87695f82f28eb6daf7686203b41f
ms.sourcegitcommit: a4cecb7389f02c27e412b743f9189bd2a6dea4d6
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/14/2021
ms.locfileid: "98190424"
---
# <a name="how-to-update-the-definition-of-a-running-workflow-instance"></a><span data-ttu-id="b17b6-102">如何：更新正在运行的工作流实例的定义</span><span class="sxs-lookup"><span data-stu-id="b17b6-102">How to: Update the Definition of a Running Workflow Instance</span></span>

<span data-ttu-id="b17b6-103">动态更新为工作流应用程序开发人员提供了一种机制，可用于更新持久化工作流实例的工作流定义。</span><span class="sxs-lookup"><span data-stu-id="b17b6-103">Dynamic update provides a mechanism for workflow application developers to update the workflow definition of a persisted workflow instance.</span></span> <span data-ttu-id="b17b6-104">所需的更改可以实施 Bug 修复、新的要求以适应意外变化。</span><span class="sxs-lookup"><span data-stu-id="b17b6-104">The required change can be to implement a bug fix, new requirements, or to accommodate unexpected changes.</span></span> <span data-ttu-id="b17b6-105">本教程中的此步骤演示如何使用动态更新来修改 `v1` 数量推测工作流的持久化实例，以匹配 [如何：并行承载多个版本的工作流](how-to-host-multiple-versions-of-a-workflow-side-by-side.md)中引入的新功能。</span><span class="sxs-lookup"><span data-stu-id="b17b6-105">This step in the tutorial demonstrates how to use dynamic update to modify  persisted instances of the `v1` number guessing workflow to match the new functionality introduced in [How to: Host Multiple Versions of a Workflow Side-by-Side](how-to-host-multiple-versions-of-a-workflow-side-by-side.md).</span></span>

## <a name="in-this-topic"></a><span data-ttu-id="b17b6-106">本主题内容</span><span class="sxs-lookup"><span data-stu-id="b17b6-106">In this topic</span></span>

- [<span data-ttu-id="b17b6-107">创建 CreateUpdateMaps 项目</span><span class="sxs-lookup"><span data-stu-id="b17b6-107">To create the CreateUpdateMaps project</span></span>](how-to-update-the-definition-of-a-running-workflow-instance.md#BKMK_CreateProject)

- [<span data-ttu-id="b17b6-108">更新 StateMachineNumberGuessWorkflow</span><span class="sxs-lookup"><span data-stu-id="b17b6-108">To update StateMachineNumberGuessWorkflow</span></span>](how-to-update-the-definition-of-a-running-workflow-instance.md#BKMK_StateMachine)

- [<span data-ttu-id="b17b6-109">更新 FlowchartNumberGuessWorkflow</span><span class="sxs-lookup"><span data-stu-id="b17b6-109">To update FlowchartNumberGuessWorkflow</span></span>](how-to-update-the-definition-of-a-running-workflow-instance.md#BKMK_Flowchart)

- [<span data-ttu-id="b17b6-110">更新 SequentialNumberGuessWorkflow</span><span class="sxs-lookup"><span data-stu-id="b17b6-110">To update SequentialNumberGuessWorkflow</span></span>](how-to-update-the-definition-of-a-running-workflow-instance.md#BKMK_Sequential)

- [<span data-ttu-id="b17b6-111">生成并运行 CreateUpdateMaps 应用程序</span><span class="sxs-lookup"><span data-stu-id="b17b6-111">To build and run the CreateUpdateMaps application</span></span>](how-to-update-the-definition-of-a-running-workflow-instance.md#BKMK_CreateUpdateMaps)

- [<span data-ttu-id="b17b6-112">生成更新的工作流程序集</span><span class="sxs-lookup"><span data-stu-id="b17b6-112">To build the updated workflow assembly</span></span>](how-to-update-the-definition-of-a-running-workflow-instance.md#BKMK_BuildAssembly)

- [<span data-ttu-id="b17b6-113">使用新版本更新 WorkflowVersionMap</span><span class="sxs-lookup"><span data-stu-id="b17b6-113">To update WorkflowVersionMap with the new versions</span></span>](how-to-update-the-definition-of-a-running-workflow-instance.md#BKMK_UpdateWorkflowVersionMap)

- [<span data-ttu-id="b17b6-114">应用动态更新</span><span class="sxs-lookup"><span data-stu-id="b17b6-114">To apply the dynamic updates</span></span>](how-to-update-the-definition-of-a-running-workflow-instance.md#BKMK_ApplyUpdate)

- [<span data-ttu-id="b17b6-115">运行包含已更新工作流的应用程序</span><span class="sxs-lookup"><span data-stu-id="b17b6-115">To run the application with the updated workflows</span></span>](how-to-update-the-definition-of-a-running-workflow-instance.md#BKMK_BuildAndRun)

- [<span data-ttu-id="b17b6-116">允许启动以前版本的工作流</span><span class="sxs-lookup"><span data-stu-id="b17b6-116">To enable starting previous versions of the workflows</span></span>](how-to-update-the-definition-of-a-running-workflow-instance.md#BKMK_StartPreviousVersions)

### <a name="to-create-the-createupdatemaps-project"></a><a name="BKMK_CreateProject"></a> <span data-ttu-id="b17b6-117">创建 CreateUpdateMaps 项目</span><span class="sxs-lookup"><span data-stu-id="b17b6-117">To create the CreateUpdateMaps project</span></span>

1. <span data-ttu-id="b17b6-118">在 **解决方案资源管理器** 中右键单击 " **WF45GettingStartedTutorial** "，然后选择 "**添加**"、"**新建项目**"。</span><span class="sxs-lookup"><span data-stu-id="b17b6-118">Right-click **WF45GettingStartedTutorial** in **Solution Explorer** and choose **Add**, **New Project**.</span></span>

2. <span data-ttu-id="b17b6-119">在 " **已安装** " 节点中，选择 " **Visual c #**、 **windows** (或 **Visual Basic**"、" **windows**) "。</span><span class="sxs-lookup"><span data-stu-id="b17b6-119">In the **Installed** node, select **Visual C#**, **Windows** (or **Visual Basic**, **Windows**).</span></span>

    > [!NOTE]
    > <span data-ttu-id="b17b6-120">**Visual C#** 或 **Visual Basic** 节点可能位于 **“已安装”** 节点中的 **“其他语言”** 节点下，具体取决于哪种编程语言被配置为 Visual Studio 中的主语言。</span><span class="sxs-lookup"><span data-stu-id="b17b6-120">Depending on which programming language is configured as the primary language in Visual Studio, the **Visual C#** or **Visual Basic** node may be under the **Other Languages** node in the **Installed** node.</span></span>

     <span data-ttu-id="b17b6-121">确保在 .NET Framework 版本下拉列表中选择 **“.NET Framework 4.5”**。</span><span class="sxs-lookup"><span data-stu-id="b17b6-121">Ensure that **.NET Framework 4.5** is selected in the .NET Framework version drop-down list.</span></span> <span data-ttu-id="b17b6-122">从 **Windows** 列表中选择 "**控制台应用程序**"。</span><span class="sxs-lookup"><span data-stu-id="b17b6-122">Select **Console Application** from the **Windows** list.</span></span> <span data-ttu-id="b17b6-123">在 "**名称**" 框中键入 **CreateUpdateMaps** ，然后单击 **"确定"**。</span><span class="sxs-lookup"><span data-stu-id="b17b6-123">Type **CreateUpdateMaps** into the **Name** box and click **OK**.</span></span>

3. <span data-ttu-id="b17b6-124">在 **解决方案资源管理器** 中右键单击 " **CreateUpdateMaps** "，然后选择 "**添加引用**"。</span><span class="sxs-lookup"><span data-stu-id="b17b6-124">Right-click **CreateUpdateMaps** in **Solution Explorer** and choose **Add Reference**.</span></span>

4. <span data-ttu-id="b17b6-125">从 "**添加引用**" 列表中的 "**程序集**" 节点选择 "**框架**"。</span><span class="sxs-lookup"><span data-stu-id="b17b6-125">Select **Framework** from the **Assemblies** node in the **Add Reference** list.</span></span> <span data-ttu-id="b17b6-126">在 "**搜索程序集**" 框 **中键入 system.string** ，以筛选程序集，并使所需的引用更易于选择。</span><span class="sxs-lookup"><span data-stu-id="b17b6-126">Type **System.Activities** into the **Search Assemblies** box to filter the assemblies and make the desired references easier to select.</span></span>

5. <span data-ttu-id="b17b6-127">选中 "**搜索结果**" 列表中的 "**系统**" 旁边的复选框。</span><span class="sxs-lookup"><span data-stu-id="b17b6-127">Check the checkbox beside **System.Activities** from the **Search Results** list.</span></span>

6. <span data-ttu-id="b17b6-128">在 "**搜索程序集**" 框中键入 **序列化**，并选中 **搜索结果** 列表中的 " **system.web** " 旁边的复选框。</span><span class="sxs-lookup"><span data-stu-id="b17b6-128">Type **Serialization** into the **Search Assemblies** box, and check the checkbox beside **System.Runtime.Serialization** from the **Search Results** list.</span></span>

7. <span data-ttu-id="b17b6-129">在 "**搜索程序集**" 框 **中键入 system.exception** ，并选中 **搜索结果** 列表 **中的 "system.exception" 旁边的** 复选框。</span><span class="sxs-lookup"><span data-stu-id="b17b6-129">Type **System.Xaml** into the **Search Assemblies** box, and check the checkbox beside **System.Xaml** from the **Search Results** list.</span></span>

8. <span data-ttu-id="b17b6-130">单击 **"确定" 关闭 "** **引用管理器** " 并添加引用。</span><span class="sxs-lookup"><span data-stu-id="b17b6-130">Click **OK** to close **Reference Manager** and add the references.</span></span>

9. <span data-ttu-id="b17b6-131">在包含其他 `using`（或 `Imports`）语句的文件的顶部添加以下 `using`（或 `Imports`）语句。</span><span class="sxs-lookup"><span data-stu-id="b17b6-131">Add the following `using` (or `Imports`) statements at the top of the file with the other `using` (or `Imports`) statements.</span></span>

    ```vb
    Imports System.Activities
    Imports System.Activities.Statements
    Imports System.Xaml
    Imports System.Reflection
    Imports System.IO
    Imports System.Activities.XamlIntegration
    Imports System.Activities.DynamicUpdate
    Imports System.Runtime.Serialization
    Imports Microsoft.VisualBasic.Activities
    ```

    ```csharp
    using System.Activities;
    using System.Activities.Statements;
    using System.IO;
    using System.Xaml;
    using System.Reflection;
    using System.Activities.XamlIntegration;
    using System.Activities.DynamicUpdate;
    using System.Runtime.Serialization;
    using Microsoft.CSharp.Activities;
    ```

10. <span data-ttu-id="b17b6-132">将以下两个字符串成员添加到 `Program` 类（或 `Module1`）。</span><span class="sxs-lookup"><span data-stu-id="b17b6-132">Add the following two string members to the `Program` class (or `Module1`).</span></span>

    ```vb
    Const mapPath = "..\..\..\PreviousVersions"
    Const definitionPath = "..\..\..\NumberGuessWorkflowActivities_du"
    ```

    ```csharp
    const string mapPath = @"..\..\..\PreviousVersions";
    const string definitionPath = @"..\..\..\NumberGuessWorkflowActivities_du";
    ```

11. <span data-ttu-id="b17b6-133">将以下 `StartUpdate` 方法添加到 `Program` 类（或 `Module1`）。</span><span class="sxs-lookup"><span data-stu-id="b17b6-133">Add the following `StartUpdate` method to the `Program` class (or `Module1`).</span></span> <span data-ttu-id="b17b6-134">此方法将指定的 xaml 工作流定义加载到 `ActivityBuilder`，然后调用 `DynamicUpdate.PrepareForUpdate`。</span><span class="sxs-lookup"><span data-stu-id="b17b6-134">This method loads up the specified xaml workflow definition into an `ActivityBuilder`, and then calls `DynamicUpdate.PrepareForUpdate`.</span></span> <span data-ttu-id="b17b6-135">`PrepareForUpdate` 为 `ActivityBuilder` 中的工作流定义创建副本。 </span><span class="sxs-lookup"><span data-stu-id="b17b6-135">`PrepareForUpdate` makes a copy of the workflow definition inside the `ActivityBuilder`.</span></span> <span data-ttu-id="b17b6-136">修改工作流定义后，会将此副本与修改的工作流定义一起使用以创建更新映射。</span><span class="sxs-lookup"><span data-stu-id="b17b6-136">After the workflow definition is modified, this copy is used along with the modified workflow definition to create the update map.</span></span>

    ```vb
    Private Function StartUpdate(name As String) As ActivityBuilder
        'Create the XamlXmlReaderSettings.
        Dim readerSettings As XamlReaderSettings = New XamlXmlReaderSettings()
        'In the XAML the "local" namespace refers to artifacts that come from
        'the same project as the XAML. When loading XAML if the currently executing
        'assembly is not the same assembly that was referred to as "local" in the XAML
        'LocalAssembly must be set to the assembly containing the artifacts.
        'Assembly.LoadFile requires an absolute path so convert this relative path
        'to an absolute path.
        readerSettings.LocalAssembly = Assembly.LoadFile(
            Path.GetFullPath(Path.Combine(mapPath, "NumberGuessWorkflowActivities_v1.dll")))

        Dim fullPath As String = Path.Combine(definitionPath, name)
        Dim xamlReader As XamlXmlReader = New XamlXmlReader(fullPath, readerSettings)

        'Load the workflow definition into an ActivityBuilder.
        Dim wf As ActivityBuilder = XamlServices.Load(
            ActivityXamlServices.CreateBuilderReader(xamlReader))

        'PrepareForUpdate makes a copy of the workflow definition in the
        'ActivityBuilder that is used for comparison when the update
        'map is created.
        DynamicUpdateServices.PrepareForUpdate(wf)

        Return wf
    End Function
    ```

    ```csharp
    private static ActivityBuilder StartUpdate(string name)
    {
        // Create the XamlXmlReaderSettings.
        XamlXmlReaderSettings readerSettings = new XamlXmlReaderSettings()
        {
            // In the XAML the "local" namespace refers to artifacts that come from
            // the same project as the XAML. When loading XAML if the currently executing
            // assembly is not the same assembly that was referred to as "local" in the XAML
            // LocalAssembly must be set to the assembly containing the artifacts.
            // Assembly.LoadFile requires an absolute path so convert this relative path
            // to an absolute path.
            LocalAssembly = Assembly.LoadFile(
                Path.GetFullPath(Path.Combine(mapPath, "NumberGuessWorkflowActivities_v1.dll")))
        };

        string path = Path.Combine(definitionPath, name);
        XamlXmlReader xamlReader = new XamlXmlReader(path, readerSettings);

        // Load the workflow definition into an ActivityBuilder.
        ActivityBuilder wf = XamlServices.Load(
            ActivityXamlServices.CreateBuilderReader(xamlReader))
            as ActivityBuilder;

        // PrepareForUpdate makes a copy of the workflow definition in the
        // ActivityBuilder that is used for comparison when the update
        // map is created.
        DynamicUpdateServices.PrepareForUpdate(wf);

        return wf;
    }
    ```

12. <span data-ttu-id="b17b6-137">接下来，将以下 `CreateUpdateMethod` 添加到 `Program` 类（或 `Module1`）。</span><span class="sxs-lookup"><span data-stu-id="b17b6-137">Next, add the following `CreateUpdateMethod` to the `Program` class (or `Module1`).</span></span> <span data-ttu-id="b17b6-138">这会通过调用 DynamicUpdateServices.CreateUpdateMap 创建一个动态更新映射，然后使用指定名称保存该更新映射。</span><span class="sxs-lookup"><span data-stu-id="b17b6-138">This creates a dynamic update map by calling DynamicUpdateServices.CreateUpdateMap, and then saves the update map using the specified name.</span></span> <span data-ttu-id="b17b6-139">此更新映射包含工作流运行时更新持久化工作流实例所需的信息（该实例是使用包含在 `ActivityBuilder` 中的原始工作流定义启动的），以便可以使用更新的工作流定义完成。</span><span class="sxs-lookup"><span data-stu-id="b17b6-139">This update map contains the information needed by the workflow runtime to update a persisted workflow instance that was started using the original workflow definition contained in the `ActivityBuilder` so that it completes using the updated workflow definition.</span></span>

    ```vb
    Private Sub CreateUpdateMaps(wf As ActivityBuilder, name As String)
        'Create the UpdateMap.
        Dim map As DynamicUpdateMap =
            DynamicUpdateServices.CreateUpdateMap(wf)

        'Serialize it to a file.
        Dim mapFullPath As String = Path.Combine(mapPath, name)
        Dim sz As DataContractSerializer = New DataContractSerializer(GetType(DynamicUpdateMap))
        Using fs As FileStream = File.Open(mapFullPath, FileMode.Create)
            sz.WriteObject(fs, map)
        End Using
    End Sub
    ```

    ```csharp
    private static void CreateUpdateMaps(ActivityBuilder wf, string name)
    {
        // Create the UpdateMap.
        DynamicUpdateMap map =
            DynamicUpdateServices.CreateUpdateMap(wf);

        // Serialize it to a file.
        string path = Path.Combine(mapPath, name);
        DataContractSerializer sz = new DataContractSerializer(typeof(DynamicUpdateMap));
        using (FileStream fs = System.IO.File.Open(path, FileMode.Create))
        {
            sz.WriteObject(fs, map);
        }
    }
    ```

13. <span data-ttu-id="b17b6-140">将以下 `SaveUpdatedDefinition` 方法添加到 `Program` 类（或 `Module1`）。</span><span class="sxs-lookup"><span data-stu-id="b17b6-140">Add the following `SaveUpdatedDefinition` method to the `Program` class (or `Module1`).</span></span> <span data-ttu-id="b17b6-141">此方法在创建更新映射后保存更新的工作流定义。</span><span class="sxs-lookup"><span data-stu-id="b17b6-141">This method saves the updated workflow definition once the update map is created.</span></span>

    ```vb
    Private Sub SaveUpdatedDefinition(wf As ActivityBuilder, name As String)
        Dim xamlPath As String = Path.Combine(definitionPath, name)
        Dim sw As StreamWriter = File.CreateText(xamlPath)
        Dim xw As XamlWriter = ActivityXamlServices.CreateBuilderWriter(
            New XamlXmlWriter(sw, New XamlSchemaContext()))
        XamlServices.Save(xw, wf)
        sw.Close()
    End Sub
    ```

    ```csharp
    private static void SaveUpdatedDefinition(ActivityBuilder wf, string name)
    {
        string xamlPath = Path.Combine(definitionPath, name);
        StreamWriter sw = File.CreateText(xamlPath);
        XamlWriter xw = ActivityXamlServices.CreateBuilderWriter(
            new XamlXmlWriter(sw, new XamlSchemaContext()));
        XamlServices.Save(xw, wf);
        sw.Close();
    }
    ```

### <a name="to-update-statemachinenumberguessworkflow"></a><a name="BKMK_StateMachine"></a> <span data-ttu-id="b17b6-142">更新 Statemachinenumberguessworkflow.xaml</span><span class="sxs-lookup"><span data-stu-id="b17b6-142">To update StateMachineNumberGuessWorkflow</span></span>

1. <span data-ttu-id="b17b6-143">将 `CreateStateMachineUpdateMap` 添加到 `Program` 类（或 `Module1`）。</span><span class="sxs-lookup"><span data-stu-id="b17b6-143">Add a `CreateStateMachineUpdateMap` to the `Program` class (or `Module1`).</span></span>

    ```vb
    Private Sub CreateStateMachineUpdateMap()

    End Sub
    ```

    ```csharp
    private static void CreateStateMachineUpdateMap()
    {
    }
    ```

2. <span data-ttu-id="b17b6-144">调用 `StartUpdate`，然后获取对工作流的根 `StateMachine` 活动的引用。</span><span class="sxs-lookup"><span data-stu-id="b17b6-144">Make a call to `StartUpdate` and then get a reference to the root `StateMachine` activity of the workflow.</span></span>

    ```vb
    Dim wf As ActivityBuilder = StartUpdate("StateMachineNumberGuessWorkflow.xaml")

    'Get a reference to the root StateMachine activity.
    Dim sm As StateMachine = wf.Implementation
    ```

    ```csharp
    ActivityBuilder wf = StartUpdate("StateMachineNumberGuessWorkflow.xaml");

    // Get a reference to the root StateMachine activity.
    StateMachine sm = wf.Implementation as StateMachine;
    ```

3. <span data-ttu-id="b17b6-145">接下来，更新两个活动的表达式， `WriteLine` 这些活动显示用户的推测是否过高或过低，以便它们匹配 [如何：并行承载多个版本的工作流](how-to-host-multiple-versions-of-a-workflow-side-by-side.md)中的更新。</span><span class="sxs-lookup"><span data-stu-id="b17b6-145">Next, update the expressions of the two `WriteLine` activities that display whether the user's guess is too high or too low so that they match the updates made in [How to: Host Multiple Versions of a Workflow Side-by-Side](how-to-host-multiple-versions-of-a-workflow-side-by-side.md).</span></span>

    ```vb
    'Update the Text of the two WriteLine activities that write the
    'results of the user's guess. They are contained in the workflow as the
    'Then and Else action of the If activity in sm.States[1].Transitions[1].Action.
    Dim guessLow As Statements.If = sm.States(1).Transitions(1).Action

    'Update the "too low" message.
    Dim tooLow As WriteLine = guessLow.Then
    tooLow.Text = New VisualBasicValue(Of String)("Guess.ToString() & "" is too low.""")

    'Update the "too high" message.
    Dim tooHigh As WriteLine = guessLow.Else
    tooHigh.Text = New VisualBasicValue(Of String)("Guess.ToString() & "" is too high.""")
    ```

    ```csharp
    // Update the Text of the two WriteLine activities that write the
    // results of the user's guess. They are contained in the workflow as the
    // Then and Else action of the If activity in sm.States[1].Transitions[1].Action.
    If guessLow = sm.States[1].Transitions[1].Action as If;

    // Update the "too low" message.
    WriteLine tooLow = guessLow.Then as WriteLine;
    tooLow.Text = new CSharpValue<string>("Guess.ToString() + \" is too low.\"");

    // Update the "too high" message.
    WriteLine tooHigh = guessLow.Else as WriteLine;
    tooHigh.Text = new CSharpValue<string>("Guess.ToString() + \" is too high.\"");
    ```

4. <span data-ttu-id="b17b6-146">接下来，添加显示关闭消息的新 `WriteLine` 活动。</span><span class="sxs-lookup"><span data-stu-id="b17b6-146">Next, add the new `WriteLine` activity that displays the closing message.</span></span>

    ```vb
    'Create the new WriteLine that displays the closing message.
    Dim wl As New WriteLine() With
    {
        .Text = New VisualBasicValue(Of String) _
            ("Guess.ToString() + "" is correct. You guessed it in "" & Turns.ToString() & "" turns.""")
    }

    'Add it as the Action for the Guess Correct transition. The Guess Correct
    'transition is the first transition of States[1]. The transitions are listed
    'at the bottom of the State activity designer.
    sm.States(1).Transitions(0).Action = wl
    ```

    ```csharp
    // Create the new WriteLine that displays the closing message.
    WriteLine wl = new WriteLine
    {
        Text = new CSharpValue<string>("Guess.ToString() + \" is correct. You guessed it in \" + Turns.ToString() + \" turns.\"")
    };

    // Add it as the Action for the Guess Correct transition. The Guess Correct
    // transition is the first transition of States[1]. The transitions are listed
    // at the bottom of the State activity designer.
    sm.States[1].Transitions[0].Action = wl;
    ```

5. <span data-ttu-id="b17b6-147">更新工作流后，调用 `CreateUpdateMaps` 和 `SaveUpdatedDefinition`。</span><span class="sxs-lookup"><span data-stu-id="b17b6-147">After the workflow is updated, call `CreateUpdateMaps` and `SaveUpdatedDefinition`.</span></span> <span data-ttu-id="b17b6-148">`CreateUpdateMaps` 创建并保存 `DynamicUpdateMap`，而 `SaveUpdatedDefinition` 保存更新的工作流定义。</span><span class="sxs-lookup"><span data-stu-id="b17b6-148">`CreateUpdateMaps` creates and saves the `DynamicUpdateMap`, and `SaveUpdatedDefinition` saves the updated workflow definition.</span></span>

    ```vb
    'Create the update map.
    CreateUpdateMaps(wf, "StateMachineNumberGuessWorkflow.map")

    'Save the updated workflow definition.
    SaveUpdatedDefinition(wf, "StateMachineNumberGuessWorkflow_du.xaml")
    ```

    ```csharp
    // Create the update map.
    CreateUpdateMaps(wf, "StateMachineNumberGuessWorkflow.map");

    // Save the updated workflow definition.
    SaveUpdatedDefinition(wf, "StateMachineNumberGuessWorkflow_du.xaml");
    ```

    <span data-ttu-id="b17b6-149">以下示例是完成的 `CreateStateMachineUpdateMap` 方法。</span><span class="sxs-lookup"><span data-stu-id="b17b6-149">The following example is the completed `CreateStateMachineUpdateMap` method.</span></span>

    ```vb
    Private Sub CreateStateMachineUpdateMap()
        Dim wf As ActivityBuilder = StartUpdate("StateMachineNumberGuessWorkflow.xaml")

        'Get a reference to the root StateMachine activity.
        Dim sm As StateMachine = wf.Implementation

        'Update the Text of the two WriteLine activities that write the
        'results of the user's guess. They are contained in the workflow as the
        'Then and Else action of the If activity in sm.States[1].Transitions[1].Action.
        Dim guessLow As Statements.If = sm.States(1).Transitions(1).Action

        'Update the "too low" message.
        Dim tooLow As WriteLine = guessLow.Then
        tooLow.Text = New VisualBasicValue(Of String)("Guess.ToString() & "" is too low.""")

        'Update the "too high" message.
        Dim tooHigh As WriteLine = guessLow.Else
        tooHigh.Text = New VisualBasicValue(Of String)("Guess.ToString() & "" is too high.""")

        'Create the new WriteLine that displays the closing message.
        Dim wl As New WriteLine() With
        {
            .Text = New VisualBasicValue(Of String) _
                ("Guess.ToString() + "" is correct. You guessed it in "" & Turns.ToString() & "" turns.""")
        }

        'Add it as the Action for the Guess Correct transition. The Guess Correct
        'transition is the first transition of States[1]. The transitions are listed
        'at the bottom of the State activity designer.
        sm.States(1).Transitions(0).Action = wl

        'Create the update map.
        CreateUpdateMaps(wf, "StateMachineNumberGuessWorkflow.map")

        'Save the updated workflow definition.
        SaveUpdatedDefinition(wf, "StateMachineNumberGuessWorkflow_du.xaml")
    End Sub
    ```

    ```csharp
    private static void CreateStateMachineUpdateMap()
    {
        ActivityBuilder wf = StartUpdate("StateMachineNumberGuessWorkflow.xaml");

        // Get a reference to the root StateMachine activity.
        StateMachine sm = wf.Implementation as StateMachine;

        // Update the Text of the two WriteLine activities that write the
        // results of the user's guess. They are contained in the workflow as the
        // Then and Else action of the If activity in sm.States[1].Transitions[1].Action.
        If guessLow = sm.States[1].Transitions[1].Action as If;

        // Update the "too low" message.
        WriteLine tooLow = guessLow.Then as WriteLine;
        tooLow.Text = new CSharpValue<string>("Guess.ToString() + \" is too low.\"");

        // Update the "too high" message.
        WriteLine tooHigh = guessLow.Else as WriteLine;
        tooHigh.Text = new CSharpValue<string>("Guess.ToString() + \" is too high.\"");

        // Create the new WriteLine that displays the closing message.
        WriteLine wl = new WriteLine
        {
            Text = new CSharpValue<string>("Guess.ToString() + \" is correct. You guessed it in \" + Turns.ToString() + \" turns.\"")
        };

        // Add it as the Action for the Guess Correct transition. The Guess Correct
        // transition is the first transition of States[1]. The transitions are listed
        // at the bottom of the State activity designer.
        sm.States[1].Transitions[0].Action = wl;

        // Create the update map.
        CreateUpdateMaps(wf, "StateMachineNumberGuessWorkflow.map");

        // Save the updated workflow definition.
        SaveUpdatedDefinition(wf, "StateMachineNumberGuessWorkflow_du.xaml");
    }
    ```

### <a name="to-update-flowchartnumberguessworkflow"></a><a name="BKMK_Flowchart"></a> <span data-ttu-id="b17b6-150">更新 Flowchartnumberguessworkflow.xaml</span><span class="sxs-lookup"><span data-stu-id="b17b6-150">To update FlowchartNumberGuessWorkflow</span></span>

1. <span data-ttu-id="b17b6-151">将以下 `CreateFlowchartUpdateMethod` 添加到 `Program` 类（或 `Module1`）。</span><span class="sxs-lookup"><span data-stu-id="b17b6-151">Add the following `CreateFlowchartUpdateMethod` to the `Program` class (or `Module1`).</span></span> <span data-ttu-id="b17b6-152">此方法与 `CreateStateMachineUpdateMap` 类似。</span><span class="sxs-lookup"><span data-stu-id="b17b6-152">This method is similar to `CreateStateMachineUpdateMap`.</span></span> <span data-ttu-id="b17b6-153">它最初调用 `StartUpdate`，然后更新流程图工作流定义，最后保存更新映射和更新的工作流定义。</span><span class="sxs-lookup"><span data-stu-id="b17b6-153">It starts with a call to `StartUpdate`, updates the flowchart workflow definition, and finishes by saving the update map and the updated workflow definition.</span></span>

    ```vb
    Private Sub CreateFlowchartUpdateMap()
        Dim wf As ActivityBuilder = StartUpdate("FlowchartNumberGuessWorkflow.xaml")

        'Get a reference to the root Flowchart activity.
        Dim fc As Flowchart = wf.Implementation

        'Update the Text of the two WriteLine activities that write the
        'results of the user's guess. They are contained in the workflow as the
        'True and False action of the "Guess < Target" FlowDecision, which is
        'Nodes[4].
        Dim guessLow As FlowDecision = fc.Nodes(4)

        'Update the "too low" message.
        Dim trueStep As FlowStep = guessLow.True
        Dim tooLow As WriteLine = trueStep.Action
        tooLow.Text = New VisualBasicValue(Of String)("Guess.ToString() & "" is too low.""")

        'Update the "too high" message.
        Dim falseStep As FlowStep = guessLow.False
        Dim tooHigh As WriteLine = falseStep.Action
        tooHigh.Text = New VisualBasicValue(Of String)("Guess.ToString() & "" is too high.""")

        'Create the new WriteLine that displays the closing message.
        Dim wl As New WriteLine() With
        {
            .Text = New VisualBasicValue(Of String) _
                ("Guess.ToString() + "" is correct. You guessed it in "" & Turns.ToString() & "" turns.""")
        }

        'Create a FlowStep to hold the WriteLine.
        Dim closingStep As New FlowStep() With
        {
            .Action = wl
        }

        'Add this new FlowStep to the True action of the
        '"Guess = Guess" FlowDecision
        Dim guessCorrect As FlowDecision = fc.Nodes(3)
        guessCorrect.True = closingStep

        'Add the new FlowStep to the Nodes collection.
        'If closingStep was replacing an existing node then
        'we would need to remove that Step from the collection.
        'In this example there was no existing True step to remove.
        fc.Nodes.Add(closingStep)

        'Create the update map.
        CreateUpdateMaps(wf, "FlowchartNumberGuessWorkflow.map")

        'Save the updated workflow definition.
        SaveUpdatedDefinition(wf, "FlowchartNumberGuessWorkflow_du.xaml")
    End Sub
    ```

    ```csharp
    private static void CreateFlowchartUpdateMap()
    {
        ActivityBuilder wf = StartUpdate("FlowchartNumberGuessWorkflow.xaml");

        // Get a reference to the root Flowchart activity.
        Flowchart fc = wf.Implementation as Flowchart;

        // Update the Text of the two WriteLine activities that write the
        // results of the user's guess. They are contained in the workflow as the
        // True and False action of the "Guess < Target" FlowDecision, which is
        // Nodes[4].
        FlowDecision guessLow = fc.Nodes[4] as FlowDecision;

        // Update the "too low" message.
        FlowStep trueStep = guessLow.True as FlowStep;
        WriteLine tooLow = trueStep.Action as WriteLine;
        tooLow.Text = new CSharpValue<string>("Guess.ToString() + \" is too low.\"");

        // Update the "too high" message.
        FlowStep falseStep = guessLow.False as FlowStep;
        WriteLine tooHigh = falseStep.Action as WriteLine;
        tooHigh.Text = new CSharpValue<string>("Guess.ToString() + \" is too high.\"");

        // Add the new WriteLine that displays the closing message.
        WriteLine wl = new WriteLine
        {
            Text = new CSharpValue<string>("Guess.ToString() + \" is correct. You guessed it in \" + Turns.ToString() + \" turns.\"")
        };

        // Create a FlowStep to hold the WriteLine.
        FlowStep closingStep = new FlowStep
        {
            Action = wl
        };

        // Add this new FlowStep to the True action of the
        // "Guess == Guess" FlowDecision
        FlowDecision guessCorrect = fc.Nodes[3] as FlowDecision;
        guessCorrect.True = closingStep;

        // Add the new FlowStep to the Nodes collection.
        // If closingStep was replacing an existing node then
        // we would need to remove that Step from the collection.
        // In this example there was no existing True step to remove.
        fc.Nodes.Add(closingStep);

        // Create the update map.
        CreateUpdateMaps(wf, "FlowchartNumberGuessWorkflow.map");

        //  Save the updated workflow definition.
        SaveUpdatedDefinition(wf, "FlowchartNumberGuessWorkflow_du.xaml");
    }
    ```

### <a name="to-update-sequentialnumberguessworkflow"></a><a name="BKMK_Sequential"></a> <span data-ttu-id="b17b6-154">更新 Sequentialnumberguessworkflow.xaml</span><span class="sxs-lookup"><span data-stu-id="b17b6-154">To update SequentialNumberGuessWorkflow</span></span>

1. <span data-ttu-id="b17b6-155">将以下 `CreateSequentialUpdateMethod` 添加到 `Program` 类（或 `Module1`）。</span><span class="sxs-lookup"><span data-stu-id="b17b6-155">Add the following `CreateSequentialUpdateMethod` to the `Program` class (or `Module1`).</span></span> <span data-ttu-id="b17b6-156">此方法与其他两个方法类似。</span><span class="sxs-lookup"><span data-stu-id="b17b6-156">This method is similar to the other two methods.</span></span> <span data-ttu-id="b17b6-157">它最初调用 `StartUpdate`，然后更新顺序工作流定义，最后保存更新映射和更新的工作流定义。</span><span class="sxs-lookup"><span data-stu-id="b17b6-157">It starts with a call to `StartUpdate`, updates the sequential workflow definition, and finishes by saving the update map and the updated workflow definition.</span></span>

    ```vb
    Private Sub CreateSequentialUpdateMap()
        Dim wf As ActivityBuilder = StartUpdate("SequentialNumberGuessWorkflow.xaml")

        'Get a reference to the root activity in the workflow.
        Dim rootSequence As Sequence = wf.Implementation

        'Update the Text of the two WriteLine activities that write the
        'results of the user's guess. They are contained in the workflow as the
        'Then and Else action of the "Guess < Target" If activity.
        'Sequence[1]->DoWhile->Body->Sequence[2]->If->Then->If
        Dim gameLoop As Statements.DoWhile = rootSequence.Activities(1)
        Dim gameBody As Sequence = gameLoop.Body
        Dim guessCorrect As Statements.If = gameBody.Activities(2)
        Dim guessLow As Statements.If = guessCorrect.Then
        Dim tooLow As WriteLine = guessLow.Then
        tooLow.Text = New VisualBasicValue(Of String)("Guess.ToString() & "" is too low.""")
        Dim tooHigh As WriteLine = guessLow.Else
        tooHigh.Text = New VisualBasicValue(Of String)("Guess.ToString() & "" is too high.""")

        'Create the new WriteLine that displays the closing message.
        Dim wl As New WriteLine() With
        {
            .Text = New VisualBasicValue(Of String) _
                ("Guess.ToString() + "" is correct. You guessed it in "" & Turns.ToString() & "" turns.""")
        }

        'Insert it as the third activity in the root sequence
        rootSequence.Activities.Insert(2, wl)

        'Create the update map.
        CreateUpdateMaps(wf, "SequentialNumberGuessWorkflow.map")

        'Save the updated workflow definition.
        SaveUpdatedDefinition(wf, "SequentialNumberGuessWorkflow_du.xaml")
    End Sub
    ```

    ```csharp
    private static void CreateSequentialUpdateMap()
    {
        ActivityBuilder wf = StartUpdate("SequentialNumberGuessWorkflow.xaml");

        // Get a reference to the root activity in the workflow.
        Sequence rootSequence = wf.Implementation as Sequence;

        // Update the Text of the two WriteLine activities that write the
        // results of the user's guess. They are contained in the workflow as the
        // Then and Else action of the "Guess < Target" If activity.
        // Sequence[1]->DoWhile->Body->Sequence[2]->If->Then->If
        DoWhile gameLoop = rootSequence.Activities[1] as DoWhile;
        Sequence gameBody = gameLoop.Body as Sequence;
        If guessCorrect = gameBody.Activities[2] as If;
        If guessLow = guessCorrect.Then as If;
        WriteLine tooLow = guessLow.Then as WriteLine;
        tooLow.Text = new CSharpValue<string>("Guess.ToString() + \" is too low.\"");
        WriteLine tooHigh = guessLow.Else as WriteLine;
        tooHigh.Text = new CSharpValue<string>("Guess.ToString() + \" is too high.\"");

        // Add the new WriteLine that displays the closing message.
        WriteLine wl = new WriteLine
        {
            Text = new CSharpValue<string>("Guess.ToString() + \" is correct. You guessed it in \" + Turns.ToString() + \" turns.\"")
        };

        // Insert it as the third activity in the root sequence
        rootSequence.Activities.Insert(2, wl);

        // Create the update map.
        CreateUpdateMaps(wf, "SequentialNumberGuessWorkflow.map");

        // Save the updated workflow definition.
        SaveUpdatedDefinition(wf, "SequentialNumberGuessWorkflow_du.xaml");
    }
    ```

### <a name="to-build-and-run-the-createupdatemaps-application"></a><a name="BKMK_CreateUpdateMaps"></a> <span data-ttu-id="b17b6-158">生成并运行 CreateUpdateMaps 应用程序</span><span class="sxs-lookup"><span data-stu-id="b17b6-158">To build and run the CreateUpdateMaps application</span></span>

1. <span data-ttu-id="b17b6-159">更新 `Main` 方法并添加以下三个方法调用。</span><span class="sxs-lookup"><span data-stu-id="b17b6-159">Update the `Main` method and add the following three method calls.</span></span> <span data-ttu-id="b17b6-160">这些方法将添加到以下各节中。</span><span class="sxs-lookup"><span data-stu-id="b17b6-160">These methods are added in the following sections.</span></span> <span data-ttu-id="b17b6-161">每个方法都更新对应的猜数工作流并创建一个描述这些更新的 `DynamicUpdateMap`。</span><span class="sxs-lookup"><span data-stu-id="b17b6-161">Each method updates the corresponding number guess workflow and creates a `DynamicUpdateMap` that describes the updates.</span></span>

    ```vb
    Sub Main()
        'Create the update maps for the changes needed to the v1 activities
        'so they match the v2 activities.
        CreateSequentialUpdateMap()
        CreateFlowchartUpdateMap()
        CreateStateMachineUpdateMap()
    End Sub
    ```

    ```csharp
    static void Main(string[] args)
    {
        // Create the update maps for the changes needed to the v1 activities
        // so they match the v2 activities.
        CreateSequentialUpdateMap();
        CreateFlowchartUpdateMap();
        CreateStateMachineUpdateMap();
    }
    ```

2. <span data-ttu-id="b17b6-162">在 **解决方案资源管理器** 中右键单击 " **CreateUpdateMaps** "，然后选择 "**设为启动项目**"。</span><span class="sxs-lookup"><span data-stu-id="b17b6-162">Right-click **CreateUpdateMaps** in **Solution Explorer** and choose **Set as StartUp Project**.</span></span>

3. <span data-ttu-id="b17b6-163">按 Ctrl+Shift+B 生成解决方案，然后按 Ctrl+F5 运行 `CreateUpdateMaps` 应用程序。</span><span class="sxs-lookup"><span data-stu-id="b17b6-163">Press CTRL+SHIFT+B to build the solution, and then CTRL+F5 to run the `CreateUpdateMaps` application.</span></span>

    > [!NOTE]
    > <span data-ttu-id="b17b6-164">`CreateUpdateMaps`应用程序在运行时不显示任何状态信息，但如果你查找 **NumberGuessWorkflowActivities_du** 文件夹和 **PreviousVersions** 文件夹，你将看到更新的工作流定义文件和更新映射。</span><span class="sxs-lookup"><span data-stu-id="b17b6-164">The `CreateUpdateMaps` application does not display any status information while running, but if you look in the **NumberGuessWorkflowActivities_du** folder and the **PreviousVersions** folder you will see the updated workflow definition files and the update maps.</span></span>

    <span data-ttu-id="b17b6-165">创建更新映射并更新工作流定义后，下一步是生成包含已更新定义的已更新工作流程序集。</span><span class="sxs-lookup"><span data-stu-id="b17b6-165">Once the update maps are created and the workflow definitions updated, the next step is to build an updated workflow assembly containing the updated definitions.</span></span>

### <a name="to-build-the-updated-workflow-assembly"></a><a name="BKMK_BuildAssembly"></a> <span data-ttu-id="b17b6-166">生成更新的工作流程序集</span><span class="sxs-lookup"><span data-stu-id="b17b6-166">To build the updated workflow assembly</span></span>

1. <span data-ttu-id="b17b6-167">打开 Visual Studio 2012 的第二个实例。</span><span class="sxs-lookup"><span data-stu-id="b17b6-167">Open a second instance of Visual Studio 2012.</span></span>

2. <span data-ttu-id="b17b6-168">从 "**文件**" 菜单中选择 "**打开**"、"**项目/解决方案**"。</span><span class="sxs-lookup"><span data-stu-id="b17b6-168">Choose **Open**, **Project/Solution** from the **File** menu.</span></span>

3. <span data-ttu-id="b17b6-169">导航到 [如何：并行承载多个版本的工作流](how-to-host-multiple-versions-of-a-workflow-side-by-side.md)的 **NumberGuessWorkflowActivities_du** 文件夹，选择 " **NumberGuessWorkflowActivities** " (或 **.vbproj**) ，并单击 "**打开**"。</span><span class="sxs-lookup"><span data-stu-id="b17b6-169">Navigate to the **NumberGuessWorkflowActivities_du** folder you created in [How to: Host Multiple Versions of a Workflow Side-by-Side](how-to-host-multiple-versions-of-a-workflow-side-by-side.md), select **NumberGuessWorkflowActivities.csproj** (or **vbproj**), and click **Open**.</span></span>

4. <span data-ttu-id="b17b6-170">在 **解决方案资源管理器** 中，右键单击 **sequentialnumberguessworkflow.xaml** ，然后选择 " **从项目中排除**"。</span><span class="sxs-lookup"><span data-stu-id="b17b6-170">In **Solution Explorer**, right click **SequentialNumberGuessWorkflow.xaml** and choose **Exclude From Project**.</span></span> <span data-ttu-id="b17b6-171">对于 **flowchartnumberguessworkflow.xaml** 和 **statemachinenumberguessworkflow.xaml**，执行相同的操作。</span><span class="sxs-lookup"><span data-stu-id="b17b6-171">Do the same thing for **FlowchartNumberGuessWorkflow.xaml** and **StateMachineNumberGuessWorkflow.xaml**.</span></span> <span data-ttu-id="b17b6-172">此步骤从项目中删除以前版本的工作流定义。</span><span class="sxs-lookup"><span data-stu-id="b17b6-172">This step removes the previous versions of the workflow definitions from the project.</span></span>

5. <span data-ttu-id="b17b6-173">从 "**项目**" 菜单中选择 "**添加现有项**"。</span><span class="sxs-lookup"><span data-stu-id="b17b6-173">Choose **Add Existing Item** from the **Project** menu.</span></span>

6. <span data-ttu-id="b17b6-174">导航到在 [如何：并行承载工作流的多个版本](how-to-host-multiple-versions-of-a-workflow-side-by-side.md)中创建的 **NumberGuessWorkflowActivities_du** 文件夹。</span><span class="sxs-lookup"><span data-stu-id="b17b6-174">Navigate to the **NumberGuessWorkflowActivities_du** folder you created in [How to: Host Multiple Versions of a Workflow Side-by-Side](how-to-host-multiple-versions-of-a-workflow-side-by-side.md).</span></span>

7. <span data-ttu-id="b17b6-175">选择 **Xaml 文件 (\* 。 \*xoml** 从 " **文件类型** " 下拉列表中) 。</span><span class="sxs-lookup"><span data-stu-id="b17b6-175">Choose **XAML Files (\*.xaml;\*.xoml)** from the **Files of type** drop-down list.</span></span>

8. <span data-ttu-id="b17b6-176">选择 **SequentialNumberGuessWorkflow_du .xaml**， **FlowchartNumberGuessWorkflow_du .xaml**， **StateMachineNumberGuessWorkflow_du** 并单击 " **添加**"。</span><span class="sxs-lookup"><span data-stu-id="b17b6-176">Select **SequentialNumberGuessWorkflow_du.xaml**, **FlowchartNumberGuessWorkflow_du.xaml**, and **StateMachineNumberGuessWorkflow_du.xaml** and click **Add**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="b17b6-177">按住 Ctrl 并单击可同时选择多个项。</span><span class="sxs-lookup"><span data-stu-id="b17b6-177">CTRL+Click to select multiple items at a time.</span></span>

    <span data-ttu-id="b17b6-178">此步骤将已更新版本的工作流定义添加到项目中。</span><span class="sxs-lookup"><span data-stu-id="b17b6-178">This step adds the updated versions of the workflow definitions to the project.</span></span>

9. <span data-ttu-id="b17b6-179">按 Ctrl+Shift+B 生成项目。</span><span class="sxs-lookup"><span data-stu-id="b17b6-179">Press CTRL+SHIFT+B to build the project.</span></span>

10. <span data-ttu-id="b17b6-180">从 "**文件**" 菜单中选择 "**关闭解决方案**"。</span><span class="sxs-lookup"><span data-stu-id="b17b6-180">Choose **Close Solution** from the **File** menu.</span></span> <span data-ttu-id="b17b6-181">项目的解决方案文件不是必需的，因此，请单击 " **否** " 以关闭 Visual Studio 而不保存解决方案文件。</span><span class="sxs-lookup"><span data-stu-id="b17b6-181">A solution file for the project is not required, so click **No** to close Visual Studio without saving a solution file.</span></span> <span data-ttu-id="b17b6-182">从 "**文件**" 菜单中选择 "**退出**" 以关闭 Visual Studio。</span><span class="sxs-lookup"><span data-stu-id="b17b6-182">Choose **Exit** from the **File** menu to close Visual Studio.</span></span>

11. <span data-ttu-id="b17b6-183">打开 Windows 资源管理器并导航到 **NumberGuessWorkflowActivities_du \bin\debug** 文件夹 (或 **bin\Release** ，具体取决于你的项目设置) 。</span><span class="sxs-lookup"><span data-stu-id="b17b6-183">Open Windows Explorer and navigate to the **NumberGuessWorkflowActivities_du\bin\Debug** folder (or **bin\Release** depending on your project settings).</span></span>

12. <span data-ttu-id="b17b6-184">将 **NumberGuessWorkflowActivities.dll** 重命名为 **NumberGuessWorkflowActivities_v15.dll**，并将其复制到 [如何：并行承载多个版本的工作流](how-to-host-multiple-versions-of-a-workflow-side-by-side.md)的 **PreviousVersions** 文件夹中。</span><span class="sxs-lookup"><span data-stu-id="b17b6-184">Rename **NumberGuessWorkflowActivities.dll** to **NumberGuessWorkflowActivities_v15.dll**, and copy it to the **PreviousVersions** folder you created in [How to: Host Multiple Versions of a Workflow Side-by-Side](how-to-host-multiple-versions-of-a-workflow-side-by-side.md).</span></span>

### <a name="to-update-workflowversionmap-with-the-new-versions"></a><a name="BKMK_UpdateWorkflowVersionMap"></a> <span data-ttu-id="b17b6-185">用新版本更新 WorkflowVersionMap</span><span class="sxs-lookup"><span data-stu-id="b17b6-185">To update WorkflowVersionMap with the new versions</span></span>

1. <span data-ttu-id="b17b6-186">切换回 Visual Studio 2012 的初始实例。</span><span class="sxs-lookup"><span data-stu-id="b17b6-186">Switch back to the initial instance of Visual Studio 2012.</span></span>

2. <span data-ttu-id="b17b6-187">双击 **NumberGuessWorkflowHost** 项目下的 " **WorkflowVersionMap.cs** (" 或 " **WorkflowVersionMap** ") 将其打开。</span><span class="sxs-lookup"><span data-stu-id="b17b6-187">Double-click **WorkflowVersionMap.cs** (or **WorkflowVersionMap.vb**) under the **NumberGuessWorkflowHost** project to open it.</span></span>

3. <span data-ttu-id="b17b6-188">添加三个新工作流标识，紧接在现有的六个工作流标识声明下面。</span><span class="sxs-lookup"><span data-stu-id="b17b6-188">Add three new workflow identities just below the six existing workflow identity declarations.</span></span> <span data-ttu-id="b17b6-189">在本教程中，`1.5.0.0` 将用作动态更新标识的 `WorkflowIdentity.Version`。</span><span class="sxs-lookup"><span data-stu-id="b17b6-189">In this tutorial, `1.5.0.0` is used as the `WorkflowIdentity.Version` for the dynamic update identities.</span></span> <span data-ttu-id="b17b6-190">这些新 `v15` 工作流标识将用于为动态更新的持久化工作流实例提供正确的工作流定义。</span><span class="sxs-lookup"><span data-stu-id="b17b6-190">These new `v15` workflow identities will be used provide the correct workflow definition for the dynamically updated persisted workflow instances.</span></span>

    ```vb
    'Current version identities.
    Public StateMachineNumberGuessIdentity As WorkflowIdentity
    Public FlowchartNumberGuessIdentity As WorkflowIdentity
    Public SequentialNumberGuessIdentity As WorkflowIdentity

    'v1 identities.
    Public StateMachineNumberGuessIdentity_v1 As WorkflowIdentity
    Public FlowchartNumberGuessIdentity_v1 As WorkflowIdentity
    Public SequentialNumberGuessIdentity_v1 As WorkflowIdentity

    'v1.5 (Dynamic Update) identities.
    Public StateMachineNumberGuessIdentity_v15 As WorkflowIdentity
    Public FlowchartNumberGuessIdentity_v15 As WorkflowIdentity
    Public SequentialNumberGuessIdentity_v15 As WorkflowIdentity
    ```

    ```csharp
    // Current version identities.
    static public WorkflowIdentity StateMachineNumberGuessIdentity;
    static public WorkflowIdentity FlowchartNumberGuessIdentity;
    static public WorkflowIdentity SequentialNumberGuessIdentity;

    // v1 identities.
    static public WorkflowIdentity StateMachineNumberGuessIdentity_v1;
    static public WorkflowIdentity FlowchartNumberGuessIdentity_v1;
    static public WorkflowIdentity SequentialNumberGuessIdentity_v1;

    // v1.5 (Dynamic Update) identities.
    static public WorkflowIdentity StateMachineNumberGuessIdentity_v15;
    static public WorkflowIdentity FlowchartNumberGuessIdentity_v15;
    static public WorkflowIdentity SequentialNumberGuessIdentity_v15;
    ```

4. <span data-ttu-id="b17b6-191">在构造函数末尾，添加以下代码。</span><span class="sxs-lookup"><span data-stu-id="b17b6-191">Add the following code at the end of the constructor.</span></span> <span data-ttu-id="b17b6-192">此代码将初始化动态更新工作流标识，加载相应的工作流定义，并将其添加到工作流版本字典中。</span><span class="sxs-lookup"><span data-stu-id="b17b6-192">This code initializes the dynamic update workflow identities, loads the corresponding workflow definitions, and adds them to the workflow version dictionary.</span></span>

    ```vb
    'Initialize the dynamic update workflow identities.
    StateMachineNumberGuessIdentity_v15 = New WorkflowIdentity With
    {
        .Name = "StateMachineNumberGuessWorkflow",
        .Version = New Version(1, 5, 0, 0)
    }

    FlowchartNumberGuessIdentity_v15 = New WorkflowIdentity With
    {
        .Name = "FlowchartNumberGuessWorkflow",
        .Version = New Version(1, 5, 0, 0)
    }

    SequentialNumberGuessIdentity_v15 = New WorkflowIdentity With
    {
        .Name = "SequentialNumberGuessWorkflow",
        .Version = New Version(1, 5, 0, 0)
    }

    'Add the dynamic update workflow identities to the dictionary along with
    'the corresponding workflow definitions loaded from the v15 assembly.
    'Assembly.LoadFile requires an absolute path so convert this relative path
    'to an absolute path.
    Dim v15AssemblyPath As String = "..\..\..\PreviousVersions\NumberGuessWorkflowActivities_v15.dll"
    v15AssemblyPath = Path.GetFullPath(v15AssemblyPath)
    Dim v15Assembly As Assembly = Assembly.LoadFile(v15AssemblyPath)

    map.Add(StateMachineNumberGuessIdentity_v15,
        v15Assembly.CreateInstance("NumberGuessWorkflowActivities.StateMachineNumberGuessWorkflow"))

    map.Add(SequentialNumberGuessIdentity_v15,
        v15Assembly.CreateInstance("NumberGuessWorkflowActivities.SequentialNumberGuessWorkflow"))

    map.Add(FlowchartNumberGuessIdentity_v15,
        v15Assembly.CreateInstance("NumberGuessWorkflowActivities.FlowchartNumberGuessWorkflow"))
    ```

    ```csharp
    // Initialize the dynamic update workflow identities.
    StateMachineNumberGuessIdentity_v15 = new WorkflowIdentity
    {
        Name = "StateMachineNumberGuessWorkflow",
        Version = new Version(1, 5, 0, 0)
    };

    FlowchartNumberGuessIdentity_v15 = new WorkflowIdentity
    {
        Name = "FlowchartNumberGuessWorkflow",
        Version = new Version(1, 5, 0, 0)
    };

    SequentialNumberGuessIdentity_v15 = new WorkflowIdentity
    {
        Name = "SequentialNumberGuessWorkflow",
        Version = new Version(1, 5, 0, 0)
    };

    // Add the dynamic update workflow identities to the dictionary along with
    // the corresponding workflow definitions loaded from the v15 assembly.
    // Assembly.LoadFile requires an absolute path so convert this relative path
    // to an absolute path.
    string v15AssemblyPath = @"..\..\..\PreviousVersions\NumberGuessWorkflowActivities_v15.dll";
    v15AssemblyPath = Path.GetFullPath(v15AssemblyPath);
    Assembly v15Assembly = Assembly.LoadFile(v15AssemblyPath);

    map.Add(StateMachineNumberGuessIdentity_v15,
        v15Assembly.CreateInstance("NumberGuessWorkflowActivities.StateMachineNumberGuessWorkflow") as Activity);

    map.Add(SequentialNumberGuessIdentity_v15,
        v15Assembly.CreateInstance("NumberGuessWorkflowActivities.SequentialNumberGuessWorkflow") as Activity);

    map.Add(FlowchartNumberGuessIdentity_v15,
        v15Assembly.CreateInstance("NumberGuessWorkflowActivities.FlowchartNumberGuessWorkflow") as Activity);
    ```

     <span data-ttu-id="b17b6-193">以下示例是完成的 `WorkflowVersionMap` 类。</span><span class="sxs-lookup"><span data-stu-id="b17b6-193">The following example is the completed `WorkflowVersionMap` class.</span></span>

    ```vb
    Public Module WorkflowVersionMap
        Dim map As Dictionary(Of WorkflowIdentity, Activity)

        'Current version identities.
        Public StateMachineNumberGuessIdentity As WorkflowIdentity
        Public FlowchartNumberGuessIdentity As WorkflowIdentity
        Public SequentialNumberGuessIdentity As WorkflowIdentity

        'v1 identities.
        Public StateMachineNumberGuessIdentity_v1 As WorkflowIdentity
        Public FlowchartNumberGuessIdentity_v1 As WorkflowIdentity
        Public SequentialNumberGuessIdentity_v1 As WorkflowIdentity

        'v1.5 (Dynamic Update) identities.
        Public StateMachineNumberGuessIdentity_v15 As WorkflowIdentity
        Public FlowchartNumberGuessIdentity_v15 As WorkflowIdentity
        Public SequentialNumberGuessIdentity_v15 As WorkflowIdentity

        Sub New()
            map = New Dictionary(Of WorkflowIdentity, Activity)

            'Add the current workflow version identities.
            StateMachineNumberGuessIdentity = New WorkflowIdentity With
            {
                .Name = "StateMachineNumberGuessWorkflow",
                .Version = New Version(2, 0, 0, 0)
            }

            FlowchartNumberGuessIdentity = New WorkflowIdentity With
            {
                .Name = "FlowchartNumberGuessWorkflow",
                .Version = New Version(2, 0, 0, 0)
            }

            SequentialNumberGuessIdentity = New WorkflowIdentity With
            {
                .Name = "SequentialNumberGuessWorkflow",
                .Version = New Version(2, 0, 0, 0)
            }

            map.Add(StateMachineNumberGuessIdentity, New StateMachineNumberGuessWorkflow())
            map.Add(FlowchartNumberGuessIdentity, New FlowchartNumberGuessWorkflow())
            map.Add(SequentialNumberGuessIdentity, New SequentialNumberGuessWorkflow())

            'Initialize the previous workflow version identities.
            StateMachineNumberGuessIdentity_v1 = New WorkflowIdentity With
            {
                .Name = "StateMachineNumberGuessWorkflow",
                .Version = New Version(1, 0, 0, 0)
            }

            FlowchartNumberGuessIdentity_v1 = New WorkflowIdentity With
            {
                .Name = "FlowchartNumberGuessWorkflow",
                .Version = New Version(1, 0, 0, 0)
            }

            SequentialNumberGuessIdentity_v1 = New WorkflowIdentity With
            {
                .Name = "SequentialNumberGuessWorkflow",
                .Version = New Version(1, 0, 0, 0)
            }

            'Add the previous version workflow identities to the dictionary along with
            'the corresponding workflow definitions loaded from the v1 assembly.
            'Assembly.LoadFile requires an absolute path so convert this relative path
            'to an absolute path.
            Dim v1AssemblyPath As String = "..\..\..\PreviousVersions\NumberGuessWorkflowActivities_v1.dll"
            v1AssemblyPath = Path.GetFullPath(v1AssemblyPath)
            Dim v1Assembly As Assembly = Assembly.LoadFile(v1AssemblyPath)

            map.Add(StateMachineNumberGuessIdentity_v1,
                v1Assembly.CreateInstance("NumberGuessWorkflowActivities.StateMachineNumberGuessWorkflow"))

            map.Add(SequentialNumberGuessIdentity_v1,
                v1Assembly.CreateInstance("NumberGuessWorkflowActivities.SequentialNumberGuessWorkflow"))

            map.Add(FlowchartNumberGuessIdentity_v1,
                v1Assembly.CreateInstance("NumberGuessWorkflowActivities.FlowchartNumberGuessWorkflow"))

            'Initialize the dynamic update workflow identities.
            StateMachineNumberGuessIdentity_v15 = New WorkflowIdentity With
            {
                .Name = "StateMachineNumberGuessWorkflow",
                .Version = New Version(1, 5, 0, 0)
            }

            FlowchartNumberGuessIdentity_v15 = New WorkflowIdentity With
            {
                .Name = "FlowchartNumberGuessWorkflow",
                .Version = New Version(1, 5, 0, 0)
            }

            SequentialNumberGuessIdentity_v15 = New WorkflowIdentity With
            {
                .Name = "SequentialNumberGuessWorkflow",
                .Version = New Version(1, 5, 0, 0)
            }

            'Add the dynamic update workflow identities to the dictionary along with
            'the corresponding workflow definitions loaded from the v15 assembly.
            'Assembly.LoadFile requires an absolute path so convert this relative path
            'to an absolute path.
            Dim v15AssemblyPath As String = "..\..\..\PreviousVersions\NumberGuessWorkflowActivities_v15.dll"
            v15AssemblyPath = Path.GetFullPath(v15AssemblyPath)
            Dim v15Assembly As Assembly = Assembly.LoadFile(v15AssemblyPath)

            map.Add(StateMachineNumberGuessIdentity_v15,
                v15Assembly.CreateInstance("NumberGuessWorkflowActivities.StateMachineNumberGuessWorkflow"))

            map.Add(SequentialNumberGuessIdentity_v15,
                v15Assembly.CreateInstance("NumberGuessWorkflowActivities.SequentialNumberGuessWorkflow"))

            map.Add(FlowchartNumberGuessIdentity_v15,
                v15Assembly.CreateInstance("NumberGuessWorkflowActivities.FlowchartNumberGuessWorkflow"))
        End Sub

        Public Function GetWorkflowDefinition(identity As WorkflowIdentity) As Activity
            Return map(identity)
        End Function

        Public Function GetIdentityDescription(identity As WorkflowIdentity) As String
            Return identity.ToString()
        End Function
    End Module
    ```

    ```csharp
    public static class WorkflowVersionMap
    {
        static Dictionary<WorkflowIdentity, Activity> map;

        // Current version identities.
        static public WorkflowIdentity StateMachineNumberGuessIdentity;
        static public WorkflowIdentity FlowchartNumberGuessIdentity;
        static public WorkflowIdentity SequentialNumberGuessIdentity;

        // v1 identities.
        static public WorkflowIdentity StateMachineNumberGuessIdentity_v1;
        static public WorkflowIdentity FlowchartNumberGuessIdentity_v1;
        static public WorkflowIdentity SequentialNumberGuessIdentity_v1;

        // v1.5 (Dynamic Update) identities.
        static public WorkflowIdentity StateMachineNumberGuessIdentity_v15;
        static public WorkflowIdentity FlowchartNumberGuessIdentity_v15;
        static public WorkflowIdentity SequentialNumberGuessIdentity_v15;

        static WorkflowVersionMap()
        {
            map = new Dictionary<WorkflowIdentity, Activity>();

            // Add the current workflow version identities.
            StateMachineNumberGuessIdentity = new WorkflowIdentity
            {
                Name = "StateMachineNumberGuessWorkflow",
                // Version = new Version(1, 0, 0, 0),
                Version = new Version(2, 0, 0, 0)
            };

            FlowchartNumberGuessIdentity = new WorkflowIdentity
            {
                Name = "FlowchartNumberGuessWorkflow",
                // Version = new Version(1, 0, 0, 0),
                Version = new Version(2, 0, 0, 0)
            };

            SequentialNumberGuessIdentity = new WorkflowIdentity
            {
                Name = "SequentialNumberGuessWorkflow",
                // Version = new Version(1, 0, 0, 0),
                Version = new Version(2, 0, 0, 0)
            };

            map.Add(StateMachineNumberGuessIdentity, new StateMachineNumberGuessWorkflow());
            map.Add(FlowchartNumberGuessIdentity, new FlowchartNumberGuessWorkflow());
            map.Add(SequentialNumberGuessIdentity, new SequentialNumberGuessWorkflow());

            // Initialize the previous workflow version identities.
            StateMachineNumberGuessIdentity_v1 = new WorkflowIdentity
            {
                Name = "StateMachineNumberGuessWorkflow",
                Version = new Version(1, 0, 0, 0)
            };

            FlowchartNumberGuessIdentity_v1 = new WorkflowIdentity
            {
                Name = "FlowchartNumberGuessWorkflow",
                Version = new Version(1, 0, 0, 0)
            };

            SequentialNumberGuessIdentity_v1 = new WorkflowIdentity
            {
                Name = "SequentialNumberGuessWorkflow",
                Version = new Version(1, 0, 0, 0)
            };

            // Add the previous version workflow identities to the dictionary along with
            // the corresponding workflow definitions loaded from the v1 assembly.
            // Assembly.LoadFile requires an absolute path so convert this relative path
            // to an absolute path.
            string v1AssemblyPath = @"..\..\..\PreviousVersions\NumberGuessWorkflowActivities_v1.dll";
            v1AssemblyPath = Path.GetFullPath(v1AssemblyPath);
            Assembly v1Assembly = Assembly.LoadFile(v1AssemblyPath);

            map.Add(StateMachineNumberGuessIdentity_v1,
                v1Assembly.CreateInstance("NumberGuessWorkflowActivities.StateMachineNumberGuessWorkflow") as Activity);

            map.Add(SequentialNumberGuessIdentity_v1,
                v1Assembly.CreateInstance("NumberGuessWorkflowActivities.SequentialNumberGuessWorkflow") as Activity);

            map.Add(FlowchartNumberGuessIdentity_v1,
                v1Assembly.CreateInstance("NumberGuessWorkflowActivities.FlowchartNumberGuessWorkflow") as Activity);

            // Initialize the dynamic update workflow identities.
            StateMachineNumberGuessIdentity_v15 = new WorkflowIdentity
            {
                Name = "StateMachineNumberGuessWorkflow",
                Version = new Version(1, 5, 0, 0)
            };

            FlowchartNumberGuessIdentity_v15 = new WorkflowIdentity
            {
                Name = "FlowchartNumberGuessWorkflow",
                Version = new Version(1, 5, 0, 0)
            };

            SequentialNumberGuessIdentity_v15 = new WorkflowIdentity
            {
                Name = "SequentialNumberGuessWorkflow",
                Version = new Version(1, 5, 0, 0)
            };

            // Add the dynamic update workflow identities to the dictionary along with
            // the corresponding workflow definitions loaded from the v15 assembly.
            // Assembly.LoadFile requires an absolute path so convert this relative path
            // to an absolute path.
            string v15AssemblyPath = @"..\..\..\PreviousVersions\NumberGuessWorkflowActivities_v15.dll";
            v15AssemblyPath = Path.GetFullPath(v15AssemblyPath);
            Assembly v15Assembly = Assembly.LoadFile(v15AssemblyPath);

            map.Add(StateMachineNumberGuessIdentity_v15,
                v15Assembly.CreateInstance("NumberGuessWorkflowActivities.StateMachineNumberGuessWorkflow") as Activity);

            map.Add(SequentialNumberGuessIdentity_v15,
                v15Assembly.CreateInstance("NumberGuessWorkflowActivities.SequentialNumberGuessWorkflow") as Activity);

            map.Add(FlowchartNumberGuessIdentity_v15,
                v15Assembly.CreateInstance("NumberGuessWorkflowActivities.FlowchartNumberGuessWorkflow") as Activity);
        }

        public static Activity GetWorkflowDefinition(WorkflowIdentity identity)
        {
            return map[identity];
        }

        public static string GetIdentityDescription(WorkflowIdentity identity)
        {
            return identity.ToString();
        }
    }
    ```

5. <span data-ttu-id="b17b6-194">按 Ctrl+Shift+B 生成项目。</span><span class="sxs-lookup"><span data-stu-id="b17b6-194">Press CTRL+SHIFT+B to build the project.</span></span>

### <a name="to-apply-the-dynamic-updates"></a><a name="BKMK_ApplyUpdate"></a> <span data-ttu-id="b17b6-195">应用动态更新</span><span class="sxs-lookup"><span data-stu-id="b17b6-195">To apply the dynamic updates</span></span>

1. <span data-ttu-id="b17b6-196">在 **解决方案资源管理器** 中右键单击 " **WF45GettingStartedTutorial** "，然后选择 "**添加**"、"**新建项目**"。</span><span class="sxs-lookup"><span data-stu-id="b17b6-196">Right-click **WF45GettingStartedTutorial** in **Solution Explorer** and choose **Add**, **New Project**.</span></span>

2. <span data-ttu-id="b17b6-197">在 " **已安装** " 节点中，选择 " **Visual c #**、 **windows** (或 **Visual Basic**"、" **windows**) "。</span><span class="sxs-lookup"><span data-stu-id="b17b6-197">In the **Installed** node, select **Visual C#**, **Windows** (or **Visual Basic**, **Windows**).</span></span>

    > [!NOTE]
    > <span data-ttu-id="b17b6-198">**Visual C#** 或 **Visual Basic** 节点可能位于 **“已安装”** 节点中的 **“其他语言”** 节点下，具体取决于哪种编程语言被配置为 Visual Studio 中的主语言。</span><span class="sxs-lookup"><span data-stu-id="b17b6-198">Depending on which programming language is configured as the primary language in Visual Studio, the **Visual C#** or **Visual Basic** node may be under the **Other Languages** node in the **Installed** node.</span></span>

    <span data-ttu-id="b17b6-199">确保在 .NET Framework 版本下拉列表中选择 **“.NET Framework 4.5”**。</span><span class="sxs-lookup"><span data-stu-id="b17b6-199">Ensure that **.NET Framework 4.5** is selected in the .NET Framework version drop-down list.</span></span> <span data-ttu-id="b17b6-200">从 **Windows** 列表中选择 "**控制台应用程序**"。</span><span class="sxs-lookup"><span data-stu-id="b17b6-200">Select **Console Application** from the **Windows** list.</span></span> <span data-ttu-id="b17b6-201">在 "**名称**" 框中键入 **ApplyDynamicUpdate** ，然后单击 **"确定"**。</span><span class="sxs-lookup"><span data-stu-id="b17b6-201">Type **ApplyDynamicUpdate** into the **Name** box and click **OK**.</span></span>

3. <span data-ttu-id="b17b6-202">在 **解决方案资源管理器** 中右键单击 " **ApplyDynamicUpdate** "，然后选择 "**添加引用**"。</span><span class="sxs-lookup"><span data-stu-id="b17b6-202">Right-click **ApplyDynamicUpdate** in **Solution Explorer** and choose **Add Reference**.</span></span>

4. <span data-ttu-id="b17b6-203">单击 " **解决方案** " 并选中 " **NumberGuessWorkflowHost**" 旁边的复选框。</span><span class="sxs-lookup"><span data-stu-id="b17b6-203">Click **Solution** and check the box next to **NumberGuessWorkflowHost**.</span></span> <span data-ttu-id="b17b6-204">需要此引用是为了让 `ApplyDynamicUpdate` 可以使用 `NumberGuessWorkflowHost.WorkflowVersionMap` 类。</span><span class="sxs-lookup"><span data-stu-id="b17b6-204">This reference is needed so that `ApplyDynamicUpdate` can use the `NumberGuessWorkflowHost.WorkflowVersionMap` class.</span></span>

5. <span data-ttu-id="b17b6-205">从 "**添加引用**" 列表中的 "**程序集**" 节点选择 "**框架**"。</span><span class="sxs-lookup"><span data-stu-id="b17b6-205">Select **Framework** from the **Assemblies** node in the **Add Reference** list.</span></span> <span data-ttu-id="b17b6-206">在 "**搜索程序集**" 框中键入 **system.object** 。</span><span class="sxs-lookup"><span data-stu-id="b17b6-206">Type **System.Activities** into the **Search Assemblies** box.</span></span> <span data-ttu-id="b17b6-207">这将筛选程序集，并更容易选择所需的引用。</span><span class="sxs-lookup"><span data-stu-id="b17b6-207">This will filter the assemblies and make the desired references easier to select.</span></span>

6. <span data-ttu-id="b17b6-208">选中 "**搜索结果**" 列表中的 "**系统**" 旁边的复选框。</span><span class="sxs-lookup"><span data-stu-id="b17b6-208">Check the checkbox beside **System.Activities** from the **Search Results** list.</span></span>

7. <span data-ttu-id="b17b6-209">在 "**搜索程序集**" 框中键入 **序列化**，并选中 **搜索结果** 列表中的 " **system.web** " 旁边的复选框。</span><span class="sxs-lookup"><span data-stu-id="b17b6-209">Type **Serialization** into the **Search Assemblies** box, and check the checkbox beside **System.Runtime.Serialization** from the **Search Results** list.</span></span>

8. <span data-ttu-id="b17b6-210">在 "**搜索程序集**" 框中键入 **DurableInstancing** ，并选中 **搜索结果** 列表中的 " **DurableInstancing** " 和 " **DurableInstancing** " 旁边的复选框。</span><span class="sxs-lookup"><span data-stu-id="b17b6-210">Type **DurableInstancing** into the **Search Assemblies** box, and check the checkbox beside **System.Activities.DurableInstancing** and **System.Runtime.DurableInstancing** from the **Search Results** list.</span></span>

9. <span data-ttu-id="b17b6-211">单击 **"确定" 关闭 "** **引用管理器** " 并添加引用。</span><span class="sxs-lookup"><span data-stu-id="b17b6-211">Click **OK** to close **Reference Manager** and add the references.</span></span>

10. <span data-ttu-id="b17b6-212">在解决方案资源管理器中右键单击 " **ApplyDynamicUpdate** "，然后选择 " **添加**"、" **类**"。</span><span class="sxs-lookup"><span data-stu-id="b17b6-212">Right-click **ApplyDynamicUpdate** in Solution Explorer and choose **Add**, **Class**.</span></span> <span data-ttu-id="b17b6-213">`DynamicUpdateInfo`在 "**名称**" 框中键入，然后单击 "**添加**"。</span><span class="sxs-lookup"><span data-stu-id="b17b6-213">Type `DynamicUpdateInfo` into the **Name** box and click **Add**.</span></span>

11. <span data-ttu-id="b17b6-214">将以下两个成员添加到 `DynamicUpdateInfo` 类中。</span><span class="sxs-lookup"><span data-stu-id="b17b6-214">Add the following two members to the `DynamicUpdateInfo` class.</span></span> <span data-ttu-id="b17b6-215">以下示例是完成的 `DynamicUpdateInfo` 类。</span><span class="sxs-lookup"><span data-stu-id="b17b6-215">The following example is the completed `DynamicUpdateInfo` class.</span></span> <span data-ttu-id="b17b6-216">此类包含有关更新工作流实例时使用的更新映射和新工作流标识的信息。</span><span class="sxs-lookup"><span data-stu-id="b17b6-216">This class contains information on the update map and new workflow identity used when a workflow instance is updated.</span></span>

    ```vb
    Public Class DynamicUpdateInfo
        Public updateMap As DynamicUpdateMap
        Public newIdentity As WorkflowIdentity
    End Class
    ```

    ```csharp
    class DynamicUpdateInfo
    {
        public DynamicUpdateMap updateMap;
        public WorkflowIdentity newIdentity;
    }
    ```

12. <span data-ttu-id="b17b6-217">在包含其他 `using`（或 `Imports`）语句的文件的顶部添加以下 `using`（或 `Imports`）语句。</span><span class="sxs-lookup"><span data-stu-id="b17b6-217">Add the following `using` (or `Imports`) statements at the top of the file with the other `using` (or `Imports`) statements.</span></span>

    ```vb
    Imports System.Activities
    Imports System.Activities.DynamicUpdate
    ```

    ```csharp
    using System.Activities;
    using System.Activities.DynamicUpdate;
    ```

13. <span data-ttu-id="b17b6-218">双击解决方案资源管理器中的 " **Program.cs** (或 **Module1**) 。</span><span class="sxs-lookup"><span data-stu-id="b17b6-218">Double-click **Program.cs** (or **Module1.vb**) in Solution Explorer.</span></span>

14. <span data-ttu-id="b17b6-219">在包含其他 `using`（或 `Imports`）语句的文件的顶部添加以下 `using`（或 `Imports`）语句。</span><span class="sxs-lookup"><span data-stu-id="b17b6-219">Add the following `using` (or `Imports`) statements at the top of the file with the other `using` (or `Imports`) statements.</span></span>

    ```vb
    Imports NumberGuessWorkflowHost
    Imports System.Data.SqlClient
    Imports System.Activities.DynamicUpdate
    Imports System.IO
    Imports System.Runtime.Serialization
    Imports System.Activities
    Imports System.Activities.DurableInstancing
    ```

    ```csharp
    using NumberGuessWorkflowHost;
    using System.Data;
    using System.Data.SqlClient;
    using System.Activities;
    using System.Activities.DynamicUpdate;
    using System.IO;
    using System.Runtime.Serialization;
    using System.Activities.DurableInstancing;
    ```

15. <span data-ttu-id="b17b6-220">将以下连接字符串成员添加到 `Program` 类（或 `Module1`）。</span><span class="sxs-lookup"><span data-stu-id="b17b6-220">Add the following connection string member to the `Program` class (or `Module1`).</span></span>

    ```vb
    Const connectionString = "Server=.\SQLEXPRESS;Initial Catalog=WF45GettingStartedTutorial;Integrated Security=SSPI"
    ```

    ```csharp
    const string connectionString = "Server=.\\SQLEXPRESS;Initial Catalog=WF45GettingStartedTutorial;Integrated Security=SSPI";
    ```

    > [!NOTE]
    > <span data-ttu-id="b17b6-221">根据您的 SQL Server 版本，该连接字符串服务器的名称可能有所不同。</span><span class="sxs-lookup"><span data-stu-id="b17b6-221">Depending on your edition of SQL Server, the connection string server name may be different.</span></span>

16. <span data-ttu-id="b17b6-222">将以下 `GetIDs` 方法添加到 `Program` 类（或 `Module1`）。</span><span class="sxs-lookup"><span data-stu-id="b17b6-222">Add the following `GetIDs` method to the `Program` class (or `Module1`).</span></span> <span data-ttu-id="b17b6-223">此方法返回持久化工作流实例 ID 的列表。</span><span class="sxs-lookup"><span data-stu-id="b17b6-223">This method returns a list of persisted workflow instance ids.</span></span>

    ```vb
    Function GetIds() As IList(Of Guid)
        Dim Ids As New List(Of Guid)
        Dim localCmd = _
            String.Format("Select [InstanceId] from [System.Activities.DurableInstancing].[Instances] Order By [CreationTime]")
        Using localCon = New SqlConnection(connectionString)
            Dim cmd As SqlCommand = localCon.CreateCommand()
            cmd.CommandText = localCmd
            localCon.Open()
            Using reader = cmd.ExecuteReader(CommandBehavior.CloseConnection)
                While reader.Read()
                    'Get the InstanceId of the persisted Workflow
                    Dim id As Guid = Guid.Parse(reader(0).ToString())

                    'Add it to the list.
                    Ids.Add(id)
                End While
            End Using
        End Using

        Return Ids
    End Function
    ```

    ```csharp
    static IList<Guid> GetIds()
    {
        List<Guid> Ids = new List<Guid>();
        string localCmd = string.Format("Select [InstanceId] from [System.Activities.DurableInstancing].[Instances] Order By [CreationTime]");
        using (SqlConnection localCon = new SqlConnection(connectionString))
        {
            SqlCommand cmd = localCon.CreateCommand();
            cmd.CommandText = localCmd;
            localCon.Open();
            using (SqlDataReader reader = cmd.ExecuteReader(CommandBehavior.CloseConnection))
            {
                while (reader.Read())
                {
                    // Get the InstanceId of the persisted Workflow
                    Guid id = Guid.Parse(reader[0].ToString());

                    // Add it to the list.
                    Ids.Add(id);
                }
            }
        }

        return Ids;
    }
    ```

17. <span data-ttu-id="b17b6-224">将以下 `LoadMap` 方法添加到 `Program` 类（或 `Module1`）。</span><span class="sxs-lookup"><span data-stu-id="b17b6-224">Add the following `LoadMap` method to the `Program` class (or `Module1`).</span></span> <span data-ttu-id="b17b6-225">此方法创建一个字典，该字典将 `v1` 工作流标识映射到用于更新相应持久化工作流实例的更新映射和新工作流标识。</span><span class="sxs-lookup"><span data-stu-id="b17b6-225">This method creates a dictionary that maps `v1` workflow identities to the update maps and new workflow identities used to update the corresponding persisted workflow instances.</span></span>

    ```vb
    Function LoadMap(mapName As String) As DynamicUpdateMap
        Dim mapPath As String = Path.Combine("..\..\..\PreviousVersions", mapName)

        Dim map As DynamicUpdateMap
        Using fs As FileStream = File.Open(mapPath, FileMode.Open)
            Dim serializer As DataContractSerializer = New DataContractSerializer(GetType(DynamicUpdateMap))
            Dim updateMap = serializer.ReadObject(fs)
            If updateMap Is Nothing Then
                Throw New ApplicationException("DynamicUpdateMap is null.")
            End If

            map = updateMap
        End Using

        Return map
    End Function
    ```

    ```csharp
    static DynamicUpdateMap LoadMap(string mapName)
    {
        string path = Path.Combine(@"..\..\..\PreviousVersions", mapName);

        DynamicUpdateMap map;
        using (FileStream fs = File.Open(path, FileMode.Open))
        {
            DataContractSerializer serializer = new DataContractSerializer(typeof(DynamicUpdateMap));
            object updateMap = serializer.ReadObject(fs);
            if (updateMap == null)
            {
                throw new ApplicationException("DynamicUpdateMap is null.");
            }

            map = updateMap as DynamicUpdateMap;
        }

        return map;
    }
    ```

18. <span data-ttu-id="b17b6-226">将以下 `LoadMaps` 方法添加到 `Program` 类（或 `Module1`）。</span><span class="sxs-lookup"><span data-stu-id="b17b6-226">Add the following `LoadMaps` method to the `Program` class (or `Module1`).</span></span> <span data-ttu-id="b17b6-227">此方法加载三个更新映射，并创建一个将 `v1` 工作流标识映射到这些更新映射的字典。</span><span class="sxs-lookup"><span data-stu-id="b17b6-227">This method loads the three update maps and creates a dictionary that maps `v1` workflow identities to the update maps.</span></span>

    ```vb
    Function LoadMaps() As IDictionary(Of WorkflowIdentity, DynamicUpdateInfo)
        'There are 3 update maps to describe the changes to update v1 workflows,
        'one for reach of the 3 workflow types in the tutorial.
        Dim maps = New Dictionary(Of WorkflowIdentity, DynamicUpdateInfo)()

        Dim sequentialMap As DynamicUpdateMap = LoadMap("SequentialNumberGuessWorkflow.map")
        Dim sequentialInfo = New DynamicUpdateInfo With
        {
            .updateMap = sequentialMap,
            .newIdentity = WorkflowVersionMap.SequentialNumberGuessIdentity_v15
        }
        maps.Add(WorkflowVersionMap.SequentialNumberGuessIdentity_v1, sequentialInfo)

        Dim stateMap As DynamicUpdateMap = LoadMap("StateMachineNumberGuessWorkflow.map")
        Dim stateInfo = New DynamicUpdateInfo With
        {
            .updateMap = stateMap,
            .newIdentity = WorkflowVersionMap.StateMachineNumberGuessIdentity_v15
        }
        maps.Add(WorkflowVersionMap.StateMachineNumberGuessIdentity_v1, stateInfo)

        Dim flowchartMap As DynamicUpdateMap = LoadMap("FlowchartNumberGuessWorkflow.map")
        Dim flowchartInfo = New DynamicUpdateInfo With
        {
            .updateMap = flowchartMap,
            .newIdentity = WorkflowVersionMap.FlowchartNumberGuessIdentity_v15
        }
        maps.Add(WorkflowVersionMap.FlowchartNumberGuessIdentity_v1, flowchartInfo)

        Return maps
    End Function
    ```

    ```csharp
    static IDictionary<WorkflowIdentity, DynamicUpdateInfo> LoadMaps()
    {
        // There are 3 update maps to describe the changes to update v1 workflows,
        // one for reach of the 3 workflow types in the tutorial.
        Dictionary<WorkflowIdentity, DynamicUpdateInfo> maps =
            new Dictionary<WorkflowIdentity, DynamicUpdateInfo>();

        DynamicUpdateMap sequentialMap = LoadMap("SequentialNumberGuessWorkflow.map");
        DynamicUpdateInfo sequentialInfo = new DynamicUpdateInfo
        {
            updateMap = sequentialMap,
            newIdentity = WorkflowVersionMap.SequentialNumberGuessIdentity_v15
        };
        maps.Add(WorkflowVersionMap.SequentialNumberGuessIdentity_v1, sequentialInfo);

        DynamicUpdateMap stateMap = LoadMap("StateMachineNumberGuessWorkflow.map");
        DynamicUpdateInfo stateInfo = new DynamicUpdateInfo
        {
            updateMap = stateMap,
            newIdentity = WorkflowVersionMap.StateMachineNumberGuessIdentity_v15
        };
        maps.Add(WorkflowVersionMap.StateMachineNumberGuessIdentity_v1, stateInfo);

        DynamicUpdateMap flowchartMap = LoadMap("FlowchartNumberGuessWorkflow.map");
        DynamicUpdateInfo flowchartInfo = new DynamicUpdateInfo
        {
            updateMap = flowchartMap,
            newIdentity = WorkflowVersionMap.FlowchartNumberGuessIdentity_v15
        };
        maps.Add(WorkflowVersionMap.FlowchartNumberGuessIdentity_v1, flowchartInfo);

        return maps;
    }
    ```

19. <span data-ttu-id="b17b6-228">将以下代码添加到 `Main`。</span><span class="sxs-lookup"><span data-stu-id="b17b6-228">Add the following code to `Main`.</span></span> <span data-ttu-id="b17b6-229">此代码循环访问持久化工作流实例并检查每个 `WorkflowIdentity`。</span><span class="sxs-lookup"><span data-stu-id="b17b6-229">This code iterates the persisted workflow instances and examines each `WorkflowIdentity`.</span></span> <span data-ttu-id="b17b6-230">如果 `WorkflowIdentity` 映射到 `v1` 工作流实例，则将使用更新的工作流定义和更新的工作流标识配置 `WorkflowApplication`。</span><span class="sxs-lookup"><span data-stu-id="b17b6-230">If the `WorkflowIdentity` maps to a `v1` workflow instance, a `WorkflowApplication` is configured with the updated workflow definition and an updated workflow identity.</span></span> <span data-ttu-id="b17b6-231">接下来，使用该实例和更新映射调用 `WorkflowApplication.Load`，这将应用动态更新映射。</span><span class="sxs-lookup"><span data-stu-id="b17b6-231">Next, `WorkflowApplication.Load` is called with the instance and the update map, which applies the dynamic update map.</span></span> <span data-ttu-id="b17b6-232">应用更新后，将通过调用 `Unload` 来持久化更新的实例。</span><span class="sxs-lookup"><span data-stu-id="b17b6-232">Once the update is applied, the updated instance is persisted with a call to `Unload`.</span></span>

    ```vb
    Dim store = New SqlWorkflowInstanceStore(connectionString)
    WorkflowApplication.CreateDefaultInstanceOwner(store, Nothing, WorkflowIdentityFilter.Any)

    Dim updateMaps As IDictionary(Of WorkflowIdentity, DynamicUpdateInfo) = LoadMaps()

    For Each id As Guid In GetIds()
        'Get a proxy to the instance.
        Dim instance As WorkflowApplicationInstance = WorkflowApplication.GetInstance(id, store)

        Console.WriteLine("Inspecting: {0}", instance.DefinitionIdentity)

        'Only update v1 workflows.
        If Not instance.DefinitionIdentity Is Nothing AndAlso _
            instance.DefinitionIdentity.Version.Equals(New Version(1, 0, 0, 0)) Then

            Dim info As DynamicUpdateInfo = updateMaps(instance.DefinitionIdentity)

            'Associate the persisted WorkflowApplicationInstance with
            'a WorkflowApplication that is configured with the updated
            'definition and updated WorkflowIdentity.
            Dim wf As Activity = WorkflowVersionMap.GetWorkflowDefinition(info.newIdentity)
            Dim wfApp = New WorkflowApplication(wf, info.newIdentity)

            'Apply the Dynamic Update.
            wfApp.Load(instance, info.updateMap)

            'Persist the updated instance.
            wfApp.Unload()

            Console.WriteLine("Updated to: {0}", info.newIdentity)
        Else
            'Not updating this instance, so unload it.
            instance.Abandon()
        End If
    Next
    ```

    ```csharp
    SqlWorkflowInstanceStore store = new SqlWorkflowInstanceStore(connectionString);
    WorkflowApplication.CreateDefaultInstanceOwner(store, null, WorkflowIdentityFilter.Any);

    IDictionary<WorkflowIdentity, DynamicUpdateInfo> updateMaps = LoadMaps();

    foreach (Guid id in GetIds())
    {
        // Get a proxy to the instance.
        WorkflowApplicationInstance instance =
            WorkflowApplication.GetInstance(id, store);

        Console.WriteLine("Inspecting: {0}", instance.DefinitionIdentity);

        // Only update v1 workflows.
        if (instance.DefinitionIdentity != null &&
            instance.DefinitionIdentity.Version.Equals(new Version(1, 0, 0, 0)))
        {
            DynamicUpdateInfo info = updateMaps[instance.DefinitionIdentity];

            // Associate the persisted WorkflowApplicationInstance with
            // a WorkflowApplication that is configured with the updated
            // definition and updated WorkflowIdentity.
            Activity wf = WorkflowVersionMap.GetWorkflowDefinition(info.newIdentity);
            WorkflowApplication wfApp =
                new WorkflowApplication(wf, info.newIdentity);

            // Apply the Dynamic Update.
            wfApp.Load(instance, info.updateMap);

            // Persist the updated instance.
            wfApp.Unload();

            Console.WriteLine("Updated to: {0}", info.newIdentity);
        }
        else
        {
            // Not updating this instance, so unload it.
            instance.Abandon();
        }
    }
    ```

20. <span data-ttu-id="b17b6-233">在 **解决方案资源管理器** 中右键单击 " **ApplyDynamicUpdate** "，然后选择 "**设为启动项目**"。</span><span class="sxs-lookup"><span data-stu-id="b17b6-233">Right-click **ApplyDynamicUpdate** in **Solution Explorer** and choose **Set as StartUp Project**.</span></span>

21. <span data-ttu-id="b17b6-234">按 Ctrl+Shift+B 生成解决方案，然后按 Ctrl+F5 运行 `ApplyDynamicUpdate` 应用程序并更新持久化工作流实例。</span><span class="sxs-lookup"><span data-stu-id="b17b6-234">Press CTRL+SHIFT+B to build the solution, and then press CTRL+F5 to run the `ApplyDynamicUpdate` application and update the persisted workflow instances.</span></span> <span data-ttu-id="b17b6-235">应该会看到与下面类似的输出。</span><span class="sxs-lookup"><span data-stu-id="b17b6-235">You should see output similar to the following.</span></span> <span data-ttu-id="b17b6-236">The version 1.0.0.0 workflows are updated to version 1.5.0.0, while the version 2.0.0.0 workflows are not updated.</span><span class="sxs-lookup"><span data-stu-id="b17b6-236">The version 1.0.0.0 workflows are updated to version 1.5.0.0, while the version 2.0.0.0 workflows are not updated.</span></span>

    <span data-ttu-id="b17b6-237">**正在检查： Statemachinenumberguessworkflow.xaml;版本 = 1.0.0。0**</span><span class="sxs-lookup"><span data-stu-id="b17b6-237">**Inspecting: StateMachineNumberGuessWorkflow; Version=1.0.0.0**</span></span>\
    <span data-ttu-id="b17b6-238">**已更新为： Statemachinenumberguessworkflow.xaml;Version = 1.5.0。0**</span><span class="sxs-lookup"><span data-stu-id="b17b6-238">**Updated to: StateMachineNumberGuessWorkflow; Version=1.5.0.0**</span></span>\
    <span data-ttu-id="b17b6-239">**正在检查： Statemachinenumberguessworkflow.xaml;版本 = 1.0.0。0**</span><span class="sxs-lookup"><span data-stu-id="b17b6-239">**Inspecting: StateMachineNumberGuessWorkflow; Version=1.0.0.0**</span></span>\
    <span data-ttu-id="b17b6-240">**已更新为： Statemachinenumberguessworkflow.xaml;Version = 1.5.0。0**</span><span class="sxs-lookup"><span data-stu-id="b17b6-240">**Updated to: StateMachineNumberGuessWorkflow; Version=1.5.0.0**</span></span>\
    <span data-ttu-id="b17b6-241">**正在检查： Flowchartnumberguessworkflow.xaml;版本 = 1.0.0。0**</span><span class="sxs-lookup"><span data-stu-id="b17b6-241">**Inspecting: FlowchartNumberGuessWorkflow; Version=1.0.0.0**</span></span>\
    <span data-ttu-id="b17b6-242">**已更新为： Flowchartnumberguessworkflow.xaml;Version = 1.5.0。0**</span><span class="sxs-lookup"><span data-stu-id="b17b6-242">**Updated to: FlowchartNumberGuessWorkflow; Version=1.5.0.0**</span></span>\
    <span data-ttu-id="b17b6-243">**正在检查： Flowchartnumberguessworkflow.xaml;版本 = 1.0.0。0**</span><span class="sxs-lookup"><span data-stu-id="b17b6-243">**Inspecting: FlowchartNumberGuessWorkflow; Version=1.0.0.0**</span></span>\
    <span data-ttu-id="b17b6-244">**已更新为： Flowchartnumberguessworkflow.xaml;Version = 1.5.0。0**</span><span class="sxs-lookup"><span data-stu-id="b17b6-244">**Updated to: FlowchartNumberGuessWorkflow; Version=1.5.0.0**</span></span>\
    <span data-ttu-id="b17b6-245">**正在检查： Sequentialnumberguessworkflow.xaml;版本 = 1.0.0。0**</span><span class="sxs-lookup"><span data-stu-id="b17b6-245">**Inspecting: SequentialNumberGuessWorkflow; Version=1.0.0.0**</span></span>\
    <span data-ttu-id="b17b6-246">**已更新为： Sequentialnumberguessworkflow.xaml;Version = 1.5.0。0**</span><span class="sxs-lookup"><span data-stu-id="b17b6-246">**Updated to: SequentialNumberGuessWorkflow; Version=1.5.0.0**</span></span>\
    <span data-ttu-id="b17b6-247">**正在检查： Sequentialnumberguessworkflow.xaml;版本 = 1.0.0。0**</span><span class="sxs-lookup"><span data-stu-id="b17b6-247">**Inspecting: SequentialNumberGuessWorkflow; Version=1.0.0.0**</span></span>\
    <span data-ttu-id="b17b6-248">**已更新为： Sequentialnumberguessworkflow.xaml;Version = 1.5.0。0**</span><span class="sxs-lookup"><span data-stu-id="b17b6-248">**Updated to: SequentialNumberGuessWorkflow; Version=1.5.0.0**</span></span>\
    <span data-ttu-id="b17b6-249">**正在检查： Sequentialnumberguessworkflow.xaml;版本 = 1.0.0。0**</span><span class="sxs-lookup"><span data-stu-id="b17b6-249">**Inspecting: SequentialNumberGuessWorkflow; Version=1.0.0.0**</span></span>\
    <span data-ttu-id="b17b6-250">**已更新为： Sequentialnumberguessworkflow.xaml;Version = 1.5.0。0**</span><span class="sxs-lookup"><span data-stu-id="b17b6-250">**Updated to: SequentialNumberGuessWorkflow; Version=1.5.0.0**</span></span>\
    <span data-ttu-id="b17b6-251">**正在检查： Statemachinenumberguessworkflow.xaml;版本 = 1.0.0。0**</span><span class="sxs-lookup"><span data-stu-id="b17b6-251">**Inspecting: StateMachineNumberGuessWorkflow; Version=1.0.0.0**</span></span>\
    <span data-ttu-id="b17b6-252">**已更新为： Statemachinenumberguessworkflow.xaml;Version = 1.5.0。0**</span><span class="sxs-lookup"><span data-stu-id="b17b6-252">**Updated to: StateMachineNumberGuessWorkflow; Version=1.5.0.0**</span></span>\
    <span data-ttu-id="b17b6-253">**正在检查： Flowchartnumberguessworkflow.xaml;版本 = 1.0.0。0**</span><span class="sxs-lookup"><span data-stu-id="b17b6-253">**Inspecting: FlowchartNumberGuessWorkflow; Version=1.0.0.0**</span></span>\
    <span data-ttu-id="b17b6-254">**已更新为： Flowchartnumberguessworkflow.xaml;Version = 1.5.0。0**</span><span class="sxs-lookup"><span data-stu-id="b17b6-254">**Updated to: FlowchartNumberGuessWorkflow; Version=1.5.0.0**</span></span>\
    <span data-ttu-id="b17b6-255">**正在检查： Statemachinenumberguessworkflow.xaml;Version = 2.0.0。0**</span><span class="sxs-lookup"><span data-stu-id="b17b6-255">**Inspecting: StateMachineNumberGuessWorkflow; Version=2.0.0.0**</span></span>\
    <span data-ttu-id="b17b6-256">**正在检查： Statemachinenumberguessworkflow.xaml;Version = 2.0.0。0**</span><span class="sxs-lookup"><span data-stu-id="b17b6-256">**Inspecting: StateMachineNumberGuessWorkflow; Version=2.0.0.0**</span></span>\
    <span data-ttu-id="b17b6-257">**正在检查： Flowchartnumberguessworkflow.xaml;Version = 2.0.0。0**</span><span class="sxs-lookup"><span data-stu-id="b17b6-257">**Inspecting: FlowchartNumberGuessWorkflow; Version=2.0.0.0**</span></span>\
    <span data-ttu-id="b17b6-258">**正在检查： Flowchartnumberguessworkflow.xaml;Version = 2.0.0。0**</span><span class="sxs-lookup"><span data-stu-id="b17b6-258">**Inspecting: FlowchartNumberGuessWorkflow; Version=2.0.0.0**</span></span>\
    <span data-ttu-id="b17b6-259">**正在检查： Sequentialnumberguessworkflow.xaml;Version = 2.0.0。0**</span><span class="sxs-lookup"><span data-stu-id="b17b6-259">**Inspecting: SequentialNumberGuessWorkflow; Version=2.0.0.0**</span></span>\
    <span data-ttu-id="b17b6-260">**正在检查： Sequentialnumberguessworkflow.xaml;Version = 2.0.0。0**</span><span class="sxs-lookup"><span data-stu-id="b17b6-260">**Inspecting: SequentialNumberGuessWorkflow; Version=2.0.0.0**</span></span>\
    <span data-ttu-id="b17b6-261">**按任意键继续 .。。**</span><span class="sxs-lookup"><span data-stu-id="b17b6-261">**Press any key to continue . . .**</span></span>

### <a name="to-run-the-application-with-the-updated-workflows"></a><a name="BKMK_BuildAndRun"></a> <span data-ttu-id="b17b6-262">运行具有更新的工作流的应用程序</span><span class="sxs-lookup"><span data-stu-id="b17b6-262">To run the application with the updated workflows</span></span>

1. <span data-ttu-id="b17b6-263">在 **解决方案资源管理器** 中右键单击 " **NumberGuessWorkflowHost** "，然后选择 "**设为启动项目**"。</span><span class="sxs-lookup"><span data-stu-id="b17b6-263">Right-click **NumberGuessWorkflowHost** in **Solution Explorer** and choose **Set as StartUp Project**.</span></span>

2. <span data-ttu-id="b17b6-264">按 Ctrl+F5 运行应用程序。</span><span class="sxs-lookup"><span data-stu-id="b17b6-264">Press CTRL+F5 to run the application.</span></span>

3. <span data-ttu-id="b17b6-265">单击 " **新游戏** " 以启动新工作流，并记下状态窗口下的版本信息，指示工作流为 `v2` 工作流。</span><span class="sxs-lookup"><span data-stu-id="b17b6-265">Click **New Game** to start a new workflow and note the version information below the status window that indicates the workflow is a `v2` workflow.</span></span>

4. <span data-ttu-id="b17b6-266">选择一个在 " `v1` [如何：托管多个版本的工作流" 并行](how-to-host-multiple-versions-of-a-workflow-side-by-side.md) 主题开头启动的工作流。</span><span class="sxs-lookup"><span data-stu-id="b17b6-266">Select one of the `v1` workflows you started at the beginning of the [How to: Host Multiple Versions of a Workflow Side-by-Side](how-to-host-multiple-versions-of-a-workflow-side-by-side.md) topic.</span></span> <span data-ttu-id="b17b6-267">请注意，状态窗口下的版本信息指示该工作流是版本 **1.5.0.0** 工作流。</span><span class="sxs-lookup"><span data-stu-id="b17b6-267">Note that the version information under the status window indicates that the workflow is a version **1.5.0.0** workflow.</span></span> <span data-ttu-id="b17b6-268">可以看到，除了指出猜数过高或过低的信息以外，没有有关猜数的其他信息。</span><span class="sxs-lookup"><span data-stu-id="b17b6-268">Note that there is no information indicated about previous guesses other than whether they were too high or too low.</span></span>

    <span data-ttu-id="b17b6-269">**请输入一个介于1和10之间的数字**</span><span class="sxs-lookup"><span data-stu-id="b17b6-269">**Please enter a number between 1 and 10**</span></span>\
    <span data-ttu-id="b17b6-270">**Your guess is too low.**</span><span class="sxs-lookup"><span data-stu-id="b17b6-270">**Your guess is too low.**</span></span>

5. <span data-ttu-id="b17b6-271">记下 `InstanceId`，然后输入猜数，直到工作流完成。</span><span class="sxs-lookup"><span data-stu-id="b17b6-271">Make a note of the `InstanceId` and then enter guesses until the workflow completes.</span></span> <span data-ttu-id="b17b6-272">状态窗口会有关猜数内容的信息，因为 `WriteLine` 活动已由动态更新进行了更新。</span><span class="sxs-lookup"><span data-stu-id="b17b6-272">The status window displays information about the content of the guess because the `WriteLine` activities were updated by the dynamic update.</span></span>

    <span data-ttu-id="b17b6-273">**请输入一个介于1和10之间的数字**</span><span class="sxs-lookup"><span data-stu-id="b17b6-273">**Please enter a number between 1 and 10**</span></span>\
    <span data-ttu-id="b17b6-274">**你的推测太低。**</span><span class="sxs-lookup"><span data-stu-id="b17b6-274">**Your guess is too low.**</span></span>\
    <span data-ttu-id="b17b6-275">**请输入一个介于1和10之间的数字**</span><span class="sxs-lookup"><span data-stu-id="b17b6-275">**Please enter a number between 1 and 10**</span></span>\
    <span data-ttu-id="b17b6-276">**5过低。**</span><span class="sxs-lookup"><span data-stu-id="b17b6-276">**5 is too low.**</span></span>\
    <span data-ttu-id="b17b6-277">**请输入一个介于1和10之间的数字**</span><span class="sxs-lookup"><span data-stu-id="b17b6-277">**Please enter a number between 1 and 10**</span></span>\
    <span data-ttu-id="b17b6-278">**7太高。**</span><span class="sxs-lookup"><span data-stu-id="b17b6-278">**7 is too high.**</span></span>\
    <span data-ttu-id="b17b6-279">**请输入一个介于1和10之间的数字**</span><span class="sxs-lookup"><span data-stu-id="b17b6-279">**Please enter a number between 1 and 10**</span></span>\
    <span data-ttu-id="b17b6-280">**Congratulations, you guessed the number in 4 turns.**</span><span class="sxs-lookup"><span data-stu-id="b17b6-280">**Congratulations, you guessed the number in 4 turns.**</span></span>

6. <span data-ttu-id="b17b6-281">打开 Windows 资源管理器并导航到 **NumberGuessWorkflowHost\bin\debug** 文件夹 (或 **bin\release** ，具体取决于你的项目设置) 并使用与已完成的工作流相对应的 Notepad 打开跟踪文件。</span><span class="sxs-lookup"><span data-stu-id="b17b6-281">Open Windows Explorer and navigate to the **NumberGuessWorkflowHost\bin\debug** folder (or **bin\release** depending on your project settings) and open the tracking file using Notepad that corresponds to the completed workflow.</span></span> <span data-ttu-id="b17b6-282">如果未记下，可以 `InstanceId` 使用 Windows 资源管理器中的 " **修改日期** " 信息来识别正确的跟踪文件。</span><span class="sxs-lookup"><span data-stu-id="b17b6-282">If you did not make a note of the `InstanceId` you may be able to identify the correct tracking file by using the **Date modified** information in Windows Explorer.</span></span> <span data-ttu-id="b17b6-283">跟踪信息的最后一行包含新添加的 `WriteLine` 活动的输出。</span><span class="sxs-lookup"><span data-stu-id="b17b6-283">The last line of the tracking information contains the output of the newly added `WriteLine` activity.</span></span>

    <span data-ttu-id="b17b6-284">**请输入一个介于1和10之间的数字**</span><span class="sxs-lookup"><span data-stu-id="b17b6-284">**Please enter a number between 1 and 10**</span></span>\
    <span data-ttu-id="b17b6-285">**你的推测太低。**</span><span class="sxs-lookup"><span data-stu-id="b17b6-285">**Your guess is too low.**</span></span>\
    <span data-ttu-id="b17b6-286">**请输入一个介于1和10之间的数字**</span><span class="sxs-lookup"><span data-stu-id="b17b6-286">**Please enter a number between 1 and 10**</span></span>\
    <span data-ttu-id="b17b6-287">**5过低。**</span><span class="sxs-lookup"><span data-stu-id="b17b6-287">**5 is too low.**</span></span>\
    <span data-ttu-id="b17b6-288">**请输入一个介于1和10之间的数字**</span><span class="sxs-lookup"><span data-stu-id="b17b6-288">**Please enter a number between 1 and 10**</span></span>\
    <span data-ttu-id="b17b6-289">**7太高。**</span><span class="sxs-lookup"><span data-stu-id="b17b6-289">**7 is too high.**</span></span>\
    <span data-ttu-id="b17b6-290">**请输入一个介于1和10之间的数字**</span><span class="sxs-lookup"><span data-stu-id="b17b6-290">**Please enter a number between 1 and 10**</span></span>\
    <span data-ttu-id="b17b6-291">**6是正确的。您猜到了4轮。**</span><span class="sxs-lookup"><span data-stu-id="b17b6-291">**6 is correct. You guessed it in 4 turns.**</span></span>

### <a name="to-enable-starting-previous-versions-of-the-workflows"></a><a name="BKMK_StartPreviousVersions"></a> <span data-ttu-id="b17b6-292">启用启动以前版本的工作流</span><span class="sxs-lookup"><span data-stu-id="b17b6-292">To enable starting previous versions of the workflows</span></span>

<span data-ttu-id="b17b6-293">如果已用完工作流而无法更新，可以修改 `NumberGuessWorkflowHost` 以允许启动以前版本的工作流。</span><span class="sxs-lookup"><span data-stu-id="b17b6-293">If you run out of workflows to update, you can modify the `NumberGuessWorkflowHost` application to enable starting previous versions of the workflows.</span></span>

1. <span data-ttu-id="b17b6-294">在 **解决方案资源管理器** 中双击 " **WorkflowHostForm** "，然后选择 " **WorkflowType** " 组合框。</span><span class="sxs-lookup"><span data-stu-id="b17b6-294">Double-click **WorkflowHostForm** in **Solution Explorer**, and select the **WorkflowType** combo box.</span></span>

2. <span data-ttu-id="b17b6-295">在 " **属性** " 窗口中，选择 " **items** " 属性，然后单击省略号按钮以编辑 **items** 集合。</span><span class="sxs-lookup"><span data-stu-id="b17b6-295">In the **Properties** window, select the **Items** property and click the ellipsis button to edit the **Items** collection.</span></span>

3. <span data-ttu-id="b17b6-296">将以下三个项添加到集合中。</span><span class="sxs-lookup"><span data-stu-id="b17b6-296">Add the following three items to the collection.</span></span>

    ```
    StateMachineNumberGuessWorkflow v1
    FlowchartNumberGuessWorkflow v1
    SequentialNumberGuessWorkflow v1
    ```

    <span data-ttu-id="b17b6-297">完成的 `Items` 集合将有六个项。</span><span class="sxs-lookup"><span data-stu-id="b17b6-297">The completed `Items` collection will have six items.</span></span>

    ```
    StateMachineNumberGuessWorkflow
    FlowchartNumberGuessWorkflow
    SequentialNumberGuessWorkflow
    StateMachineNumberGuessWorkflow v1
    FlowchartNumberGuessWorkflow v1
    SequentialNumberGuessWorkflow v1
    ```

4. <span data-ttu-id="b17b6-298">在 **解决方案资源管理器** 中双击 " **WorkflowHostForm** "，然后选择 "**查看代码**"。</span><span class="sxs-lookup"><span data-stu-id="b17b6-298">Double-click **WorkflowHostForm** in **Solution Explorer**, and select **View Code**.</span></span>

5. <span data-ttu-id="b17b6-299">在处理程序中将三个新事例添加到 `switch` (或 `Select Case`) 语句， `NewGame_Click` 以便将 **WorkflowType** 组合框中的新项映射到匹配的工作流标识。</span><span class="sxs-lookup"><span data-stu-id="b17b6-299">Add three new cases to the `switch` (or `Select Case`) statement in the `NewGame_Click` handler to map the new items in the **WorkflowType** combo box to the matching workflow identities.</span></span>

    ```vb
    Case "SequentialNumberGuessWorkflow v1"
        identity = WorkflowVersionMap.SequentialNumberGuessIdentity_v1

    Case "StateMachineNumberGuessWorkflow v1"
        identity = WorkflowVersionMap.StateMachineNumberGuessIdentity_v1

    Case "FlowchartNumberGuessWorkflow v1"
        identity = WorkflowVersionMap.FlowchartNumberGuessIdentity_v1
    ```

    ```csharp
    case "SequentialNumberGuessWorkflow v1":
        identity = WorkflowVersionMap.SequentialNumberGuessIdentity_v1;
        break;

    case "StateMachineNumberGuessWorkflow v1":
        identity = WorkflowVersionMap.StateMachineNumberGuessIdentity_v1;
        break;

    case "FlowchartNumberGuessWorkflow v1":
        identity = WorkflowVersionMap.FlowchartNumberGuessIdentity_v1;
        break;
    ```

    <span data-ttu-id="b17b6-300">以下示例包含完整的 `switch`（或 `Select Case`）语句。</span><span class="sxs-lookup"><span data-stu-id="b17b6-300">The following example contains the complete `switch` (or `Select Case`) statement.</span></span>

    ```vb
    Select Case WorkflowType.SelectedItem.ToString()
        Case "SequentialNumberGuessWorkflow"
            identity = WorkflowVersionMap.SequentialNumberGuessIdentity

        Case "StateMachineNumberGuessWorkflow"
            identity = WorkflowVersionMap.StateMachineNumberGuessIdentity

        Case "FlowchartNumberGuessWorkflow"
            identity = WorkflowVersionMap.FlowchartNumberGuessIdentity

        Case "SequentialNumberGuessWorkflow v1"
            identity = WorkflowVersionMap.SequentialNumberGuessIdentity_v1

        Case "StateMachineNumberGuessWorkflow v1"
            identity = WorkflowVersionMap.StateMachineNumberGuessIdentity_v1

        Case "FlowchartNumberGuessWorkflow v1"
            identity = WorkflowVersionMap.FlowchartNumberGuessIdentity_v1
    End Select
    ```

    ```csharp
    switch (WorkflowType.SelectedItem.ToString())
    {
        case "SequentialNumberGuessWorkflow":
            identity = WorkflowVersionMap.SequentialNumberGuessIdentity;
            break;

        case "StateMachineNumberGuessWorkflow":
            identity = WorkflowVersionMap.StateMachineNumberGuessIdentity;
            break;

        case "FlowchartNumberGuessWorkflow":
            identity = WorkflowVersionMap.FlowchartNumberGuessIdentity;
            break;

        case "SequentialNumberGuessWorkflow v1":
            identity = WorkflowVersionMap.SequentialNumberGuessIdentity_v1;
            break;

        case "StateMachineNumberGuessWorkflow v1":
            identity = WorkflowVersionMap.StateMachineNumberGuessIdentity_v1;
            break;

        case "FlowchartNumberGuessWorkflow v1":
            identity = WorkflowVersionMap.FlowchartNumberGuessIdentity_v1;
            break;
    };
    ```

6. <span data-ttu-id="b17b6-301">按 Ctrl+F5 生成并运行应用程序。</span><span class="sxs-lookup"><span data-stu-id="b17b6-301">Press CTRL+F5 to build and run the application.</span></span> <span data-ttu-id="b17b6-302">现在可以启动工作流的 `v1` 版本以及当前版本。</span><span class="sxs-lookup"><span data-stu-id="b17b6-302">You can now start the `v1` versions of the workflow as well as the current versions.</span></span> <span data-ttu-id="b17b6-303">若要动态更新这些新实例，请运行 **ApplyDynamicUpdate** 应用程序。</span><span class="sxs-lookup"><span data-stu-id="b17b6-303">To dynamically update these new instances, run the **ApplyDynamicUpdate** application.</span></span>
