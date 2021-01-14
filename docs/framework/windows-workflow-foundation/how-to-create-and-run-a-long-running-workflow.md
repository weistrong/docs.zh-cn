---
title: 如何创建和运行长时间运行的工作流
description: 本文介绍如何创建支持启动和恢复多个工作流实例和工作流持久性的 Windows 窗体主机应用程序。
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: c0043c89-2192-43c9-986d-3ecec4dd8c9c
ms.openlocfilehash: 701788ac5575ad671afd56db3af4bd247efac8b1
ms.sourcegitcommit: a4cecb7389f02c27e412b743f9189bd2a6dea4d6
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/14/2021
ms.locfileid: "98188460"
---
# <a name="how-to-create-and-run-a-long-running-workflow"></a><span data-ttu-id="60025-103">如何创建和运行长时间运行的工作流</span><span class="sxs-lookup"><span data-stu-id="60025-103">How to create and run a long-running workflow</span></span>

<span data-ttu-id="60025-104">Windows Workflow Foundation (WF) 的一个中心功能是运行时能够将空闲工作流保存并卸载到数据库。</span><span class="sxs-lookup"><span data-stu-id="60025-104">One of the central features of Windows Workflow Foundation (WF) is the runtime’s ability to persist and unload idle workflows to a database.</span></span> <span data-ttu-id="60025-105">[如何：运行工作流](how-to-run-a-workflow.md)中的步骤演示了如何使用控制台应用程序托管工作流。</span><span class="sxs-lookup"><span data-stu-id="60025-105">The steps in [How to: Run a Workflow](how-to-run-a-workflow.md) demonstrated the basics of workflow hosting using a console application.</span></span> <span data-ttu-id="60025-106">示例演示了启动工作流、工作流生命周期处理程序和恢复书签。</span><span class="sxs-lookup"><span data-stu-id="60025-106">Examples were shown of starting workflows, workflow lifecycle handlers, and resuming bookmarks.</span></span> <span data-ttu-id="60025-107">为了有效演示工作流持久性，需要一个支持启动和恢复多个工作流实例的更为复杂的工作流主机。</span><span class="sxs-lookup"><span data-stu-id="60025-107">In order to demonstrate workflow persistence effectively, a more complex workflow host is required that supports starting and resuming multiple workflow instances.</span></span> <span data-ttu-id="60025-108">教程中此步骤演示了如何创建 Windows 窗体主机应用程序，此 Windows 窗体主机应用程序支持启动和恢复多个工作流实例、工作流持久性，并为高级功能（如在后续教程步骤中演示的跟踪和版本控制）提供基础。</span><span class="sxs-lookup"><span data-stu-id="60025-108">This step in the tutorial demonstrates how to create a Windows form host application that supports starting and resuming multiple workflow instances, workflow persistence, and provides a basis for the advanced features such as tracking and versioning that are demonstrated in subsequent tutorial steps.</span></span>

> [!NOTE]
> <span data-ttu-id="60025-109">此教程步骤和后续步骤使用 [如何：创建工作流](how-to-create-a-workflow.md)中的所有三个工作流类型。</span><span class="sxs-lookup"><span data-stu-id="60025-109">This tutorial step and the subsequent steps use all three workflow types from [How to: Create a Workflow](how-to-create-a-workflow.md).</span></span>

## <a name="to-create-the-persistence-database"></a><span data-ttu-id="60025-110">创建持久性数据库</span><span class="sxs-lookup"><span data-stu-id="60025-110">To create the persistence database</span></span>

1. <span data-ttu-id="60025-111">打开 SQL Server Management Studio 并连接到本地服务器，例如 **.\SQLEXPRESS**。</span><span class="sxs-lookup"><span data-stu-id="60025-111">Open SQL Server Management Studio and connect to the local server, for example **.\SQLEXPRESS**.</span></span> <span data-ttu-id="60025-112">右键单击本地服务器上的 " **数据库** " 节点，然后选择 " **新建数据库**"。</span><span class="sxs-lookup"><span data-stu-id="60025-112">Right-click the **Databases** node on the local server, and select **New Database**.</span></span> <span data-ttu-id="60025-113">将新数据库命名为 **WF45GettingStartedTutorial**，接受所有其他值，然后选择 **"确定"**。</span><span class="sxs-lookup"><span data-stu-id="60025-113">Name the new database **WF45GettingStartedTutorial**, accept all other values, and select **OK**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="60025-114">在创建数据库之前，请确保在本地服务器上具有 **Create database** 权限。</span><span class="sxs-lookup"><span data-stu-id="60025-114">Ensure that you have **Create Database** permission on the local server before creating the database.</span></span>

2. <span data-ttu-id="60025-115">从 "**文件**" 菜单中 **选择 "** **打开**"。</span><span class="sxs-lookup"><span data-stu-id="60025-115">Choose **Open**, **File** from the **File** menu.</span></span> <span data-ttu-id="60025-116">浏览到以下文件夹： *C:\Windows\Microsoft.NET\Framework\v4.0.30319\sql\en*</span><span class="sxs-lookup"><span data-stu-id="60025-116">Browse to the following folder: *C:\Windows\Microsoft.NET\Framework\v4.0.30319\sql\en*</span></span>

    <span data-ttu-id="60025-117">选择以下两个文件，并单击 " **打开**"。</span><span class="sxs-lookup"><span data-stu-id="60025-117">Select the following two files and click **Open**.</span></span>

    - <span data-ttu-id="60025-118">*SqlWorkflowInstanceStoreLogic.sql*</span><span class="sxs-lookup"><span data-stu-id="60025-118">*SqlWorkflowInstanceStoreLogic.sql*</span></span>

    - <span data-ttu-id="60025-119">*SqlWorkflowInstanceStoreSchema.sql*</span><span class="sxs-lookup"><span data-stu-id="60025-119">*SqlWorkflowInstanceStoreSchema.sql*</span></span>

3. <span data-ttu-id="60025-120">从 "**窗口**" 菜单中选择 " **sqlworkflowinstancestoreschema.sql** "。</span><span class="sxs-lookup"><span data-stu-id="60025-120">Choose **SqlWorkflowInstanceStoreSchema.sql** from the **Window** menu.</span></span> <span data-ttu-id="60025-121">确保在 "**可用数据库**" 下拉 WF45GettingStartedTutorial 中选择 "  "，并从 "**查询**" 菜单中选择 "**执行**"。</span><span class="sxs-lookup"><span data-stu-id="60025-121">Ensure that **WF45GettingStartedTutorial** is selected in the **Available Databases** drop-down and choose **Execute** from the **Query** menu.</span></span>

4. <span data-ttu-id="60025-122">从 "**窗口**" 菜单中选择 " **sqlworkflowinstancestorelogic.sql** "。</span><span class="sxs-lookup"><span data-stu-id="60025-122">Choose **SqlWorkflowInstanceStoreLogic.sql** from the **Window** menu.</span></span> <span data-ttu-id="60025-123">确保在 "**可用数据库**" 下拉 WF45GettingStartedTutorial 中选择 "  "，并从 "**查询**" 菜单中选择 "**执行**"。</span><span class="sxs-lookup"><span data-stu-id="60025-123">Ensure that **WF45GettingStartedTutorial** is selected in the **Available Databases** drop-down and choose **Execute** from the **Query** menu.</span></span>

    > [!WARNING]
    > <span data-ttu-id="60025-124">请务必按正确顺序执行前面两个步骤。</span><span class="sxs-lookup"><span data-stu-id="60025-124">It is important to perform the previous two steps in the correct order.</span></span> <span data-ttu-id="60025-125">如果不按顺序执行查询，系统会发生错误，并且持久性数据库会配置不正确。</span><span class="sxs-lookup"><span data-stu-id="60025-125">If the queries are executed out of order, errors occur and the persistence database is not configured correctly.</span></span>

## <a name="to-add-the-reference-to-the-durableinstancing-assemblies"></a><span data-ttu-id="60025-126">添加对 DurableInstancing 程序集的引用</span><span class="sxs-lookup"><span data-stu-id="60025-126">To add the reference to the DurableInstancing assemblies</span></span>

1. <span data-ttu-id="60025-127">在 **解决方案资源管理器** 中右键单击 " **NumberGuessWorkflowHost** "，然后选择 "**添加引用**"。</span><span class="sxs-lookup"><span data-stu-id="60025-127">Right-click **NumberGuessWorkflowHost** in **Solution Explorer** and select **Add Reference**.</span></span>

2. <span data-ttu-id="60025-128">从 "**添加引用**" 列表中选择 **程序集**，然后 `DurableInstancing` 在 "**搜索程序集**" 框中键入。</span><span class="sxs-lookup"><span data-stu-id="60025-128">Select **Assemblies** from the **Add Reference** list, and type `DurableInstancing` into the **Search Assemblies** box.</span></span> <span data-ttu-id="60025-129">这将筛选程序集，使您更易于选择所需引用。</span><span class="sxs-lookup"><span data-stu-id="60025-129">This filters the assemblies and makes the desired references easier to select.</span></span>

3. <span data-ttu-id="60025-130">选中 " **DurableInstancing** " 和 " **DurableInstancing** **" 旁边** 的复选框，然后单击 **"确定"**。</span><span class="sxs-lookup"><span data-stu-id="60025-130">Check the checkbox beside **System.Activities.DurableInstancing** and **System.Runtime.DurableInstancing** from the **Search Results** list, and click **OK**.</span></span>

## <a name="to-create-the-workflow-host-form"></a><span data-ttu-id="60025-131">创建工作流主机窗体</span><span class="sxs-lookup"><span data-stu-id="60025-131">To create the workflow host form</span></span>

1. <span data-ttu-id="60025-132">在 **解决方案资源管理器** 中右键单击 " **NumberGuessWorkflowHost** "，然后选择 "**添加**"、"**新建项**"。</span><span class="sxs-lookup"><span data-stu-id="60025-132">Right-click **NumberGuessWorkflowHost** in **Solution Explorer** and choose **Add**, **New Item**.</span></span>

2. <span data-ttu-id="60025-133">在 " **已安装** 的模板" 列表中，选择 **Windows 窗体**， `WorkflowHostForm` 在 " **名称** " 框中键入，然后单击 " **添加**"。</span><span class="sxs-lookup"><span data-stu-id="60025-133">In the **Installed** templates list, choose **Windows Form**, type `WorkflowHostForm` in the **Name** box, and click **Add**.</span></span>

3. <span data-ttu-id="60025-134">在窗体上配置以下属性。</span><span class="sxs-lookup"><span data-stu-id="60025-134">Configure the following properties on the form.</span></span>

    |<span data-ttu-id="60025-135">properties</span><span class="sxs-lookup"><span data-stu-id="60025-135">Property</span></span>|<span data-ttu-id="60025-136">Value</span><span class="sxs-lookup"><span data-stu-id="60025-136">Value</span></span>|
    |--------------|-----------|
    |<span data-ttu-id="60025-137">FormBorderStyle</span><span class="sxs-lookup"><span data-stu-id="60025-137">FormBorderStyle</span></span>|<span data-ttu-id="60025-138">FixedSingle</span><span class="sxs-lookup"><span data-stu-id="60025-138">FixedSingle</span></span>|
    |<span data-ttu-id="60025-139">MaximizeBox</span><span class="sxs-lookup"><span data-stu-id="60025-139">MaximizeBox</span></span>|<span data-ttu-id="60025-140">False</span><span class="sxs-lookup"><span data-stu-id="60025-140">False</span></span>|
    |<span data-ttu-id="60025-141">大小</span><span class="sxs-lookup"><span data-stu-id="60025-141">Size</span></span>|<span data-ttu-id="60025-142">400, 420</span><span class="sxs-lookup"><span data-stu-id="60025-142">400, 420</span></span>|

4. <span data-ttu-id="60025-143">按照指定顺序将以下控件添加到窗体，并根据指示配置这些属性。</span><span class="sxs-lookup"><span data-stu-id="60025-143">Add the following controls to the form in the order specified and configure the properties as directed.</span></span>

    |<span data-ttu-id="60025-144">控件</span><span class="sxs-lookup"><span data-stu-id="60025-144">Control</span></span>|<span data-ttu-id="60025-145">属性：值</span><span class="sxs-lookup"><span data-stu-id="60025-145">Property: Value</span></span>|
    |-------------|---------------------|
    |<span data-ttu-id="60025-146">**Button**</span><span class="sxs-lookup"><span data-stu-id="60025-146">**Button**</span></span>|<span data-ttu-id="60025-147">名称： NewGame</span><span class="sxs-lookup"><span data-stu-id="60025-147">Name: NewGame</span></span><br /><br /> <span data-ttu-id="60025-148">位置：13、13</span><span class="sxs-lookup"><span data-stu-id="60025-148">Location: 13, 13</span></span><br /><br /> <span data-ttu-id="60025-149">大小：75，23</span><span class="sxs-lookup"><span data-stu-id="60025-149">Size: 75, 23</span></span><br /><br /> <span data-ttu-id="60025-150">文本：新建游戏</span><span class="sxs-lookup"><span data-stu-id="60025-150">Text: New Game</span></span>|
    |<span data-ttu-id="60025-151">**标签**</span><span class="sxs-lookup"><span data-stu-id="60025-151">**Label**</span></span>|<span data-ttu-id="60025-152">位置：94、18</span><span class="sxs-lookup"><span data-stu-id="60025-152">Location: 94, 18</span></span><br /><br /> <span data-ttu-id="60025-153">Text：推测一个从1到</span><span class="sxs-lookup"><span data-stu-id="60025-153">Text: Guess a number from 1 to</span></span>|
    |<span data-ttu-id="60025-154">**ComboBox**</span><span class="sxs-lookup"><span data-stu-id="60025-154">**ComboBox**</span></span>|<span data-ttu-id="60025-155">名称： NumberRange</span><span class="sxs-lookup"><span data-stu-id="60025-155">Name: NumberRange</span></span><br /><br /> <span data-ttu-id="60025-156">DropDownStyle： DropDownList</span><span class="sxs-lookup"><span data-stu-id="60025-156">DropDownStyle: DropDownList</span></span><br /><br /> <span data-ttu-id="60025-157">项：10，100，1000</span><span class="sxs-lookup"><span data-stu-id="60025-157">Items: 10, 100, 1000</span></span><br /><br /> <span data-ttu-id="60025-158">位置：228、12</span><span class="sxs-lookup"><span data-stu-id="60025-158">Location: 228, 12</span></span><br /><br /> <span data-ttu-id="60025-159">大小：143，21</span><span class="sxs-lookup"><span data-stu-id="60025-159">Size: 143, 21</span></span>|
    |<span data-ttu-id="60025-160">**标签**</span><span class="sxs-lookup"><span data-stu-id="60025-160">**Label**</span></span>|<span data-ttu-id="60025-161">位置：13，43</span><span class="sxs-lookup"><span data-stu-id="60025-161">Location: 13, 43</span></span><br /><br /> <span data-ttu-id="60025-162">文本：工作流类型</span><span class="sxs-lookup"><span data-stu-id="60025-162">Text: Workflow type</span></span>|
    |<span data-ttu-id="60025-163">**ComboBox**</span><span class="sxs-lookup"><span data-stu-id="60025-163">**ComboBox**</span></span>|<span data-ttu-id="60025-164">名称： WorkflowType</span><span class="sxs-lookup"><span data-stu-id="60025-164">Name: WorkflowType</span></span><br /><br /> <span data-ttu-id="60025-165">DropDownStyle： DropDownList</span><span class="sxs-lookup"><span data-stu-id="60025-165">DropDownStyle: DropDownList</span></span><br /><br /> <span data-ttu-id="60025-166">Items： Statemachinenumberguessworkflow.xaml、Flowchartnumberguessworkflow.xaml、Sequentialnumberguessworkflow.xaml</span><span class="sxs-lookup"><span data-stu-id="60025-166">Items: StateMachineNumberGuessWorkflow, FlowchartNumberGuessWorkflow, SequentialNumberGuessWorkflow</span></span><br /><br /> <span data-ttu-id="60025-167">位置：94、40</span><span class="sxs-lookup"><span data-stu-id="60025-167">Location: 94, 40</span></span><br /><br /> <span data-ttu-id="60025-168">大小：277，21</span><span class="sxs-lookup"><span data-stu-id="60025-168">Size: 277, 21</span></span>|
    |<span data-ttu-id="60025-169">**标签**</span><span class="sxs-lookup"><span data-stu-id="60025-169">**Label**</span></span>|<span data-ttu-id="60025-170">名称： WorkflowVersion</span><span class="sxs-lookup"><span data-stu-id="60025-170">Name: WorkflowVersion</span></span><br /><br /> <span data-ttu-id="60025-171">位置：13，362</span><span class="sxs-lookup"><span data-stu-id="60025-171">Location: 13, 362</span></span><br /><br /> <span data-ttu-id="60025-172">文本：工作流版本</span><span class="sxs-lookup"><span data-stu-id="60025-172">Text: Workflow version</span></span>|
    |<span data-ttu-id="60025-173">**GroupBox**</span><span class="sxs-lookup"><span data-stu-id="60025-173">**GroupBox**</span></span>|<span data-ttu-id="60025-174">位置：13，67</span><span class="sxs-lookup"><span data-stu-id="60025-174">Location: 13, 67</span></span><br /><br /> <span data-ttu-id="60025-175">大小：358、287</span><span class="sxs-lookup"><span data-stu-id="60025-175">Size: 358, 287</span></span><br /><br /> <span data-ttu-id="60025-176">文本：游戏</span><span class="sxs-lookup"><span data-stu-id="60025-176">Text: Game</span></span>|

    > [!NOTE]
    > <span data-ttu-id="60025-177">添加以下控件时，将其放入分组框。</span><span class="sxs-lookup"><span data-stu-id="60025-177">When adding the following controls, put them into the GroupBox.</span></span>

    |<span data-ttu-id="60025-178">控件</span><span class="sxs-lookup"><span data-stu-id="60025-178">Control</span></span>|<span data-ttu-id="60025-179">属性：值</span><span class="sxs-lookup"><span data-stu-id="60025-179">Property: Value</span></span>|
    |-------------|---------------------|
    |<span data-ttu-id="60025-180">**标签**</span><span class="sxs-lookup"><span data-stu-id="60025-180">**Label**</span></span>|<span data-ttu-id="60025-181">位置：7、20</span><span class="sxs-lookup"><span data-stu-id="60025-181">Location: 7, 20</span></span><br /><br /> <span data-ttu-id="60025-182">文本：工作流实例 Id</span><span class="sxs-lookup"><span data-stu-id="60025-182">Text: Workflow Instance Id</span></span>|
    |<span data-ttu-id="60025-183">**ComboBox**</span><span class="sxs-lookup"><span data-stu-id="60025-183">**ComboBox**</span></span>|<span data-ttu-id="60025-184">名称： InstanceId</span><span class="sxs-lookup"><span data-stu-id="60025-184">Name: InstanceId</span></span><br /><br /> <span data-ttu-id="60025-185">DropDownStyle： DropDownList</span><span class="sxs-lookup"><span data-stu-id="60025-185">DropDownStyle: DropDownList</span></span><br /><br /> <span data-ttu-id="60025-186">位置：121、17</span><span class="sxs-lookup"><span data-stu-id="60025-186">Location: 121, 17</span></span><br /><br /> <span data-ttu-id="60025-187">大小：227，21</span><span class="sxs-lookup"><span data-stu-id="60025-187">Size: 227, 21</span></span>|
    |<span data-ttu-id="60025-188">**标签**</span><span class="sxs-lookup"><span data-stu-id="60025-188">**Label**</span></span>|<span data-ttu-id="60025-189">位置：7，47</span><span class="sxs-lookup"><span data-stu-id="60025-189">Location: 7, 47</span></span><br /><br /> <span data-ttu-id="60025-190">文本：推测</span><span class="sxs-lookup"><span data-stu-id="60025-190">Text: Guess</span></span>|
    |<span data-ttu-id="60025-191">**TextBox**</span><span class="sxs-lookup"><span data-stu-id="60025-191">**TextBox**</span></span>|<span data-ttu-id="60025-192">名称：推测</span><span class="sxs-lookup"><span data-stu-id="60025-192">Name: Guess</span></span><br /><br /> <span data-ttu-id="60025-193">位置：50、44</span><span class="sxs-lookup"><span data-stu-id="60025-193">Location: 50, 44</span></span><br /><br /> <span data-ttu-id="60025-194">大小：65，20</span><span class="sxs-lookup"><span data-stu-id="60025-194">Size: 65, 20</span></span>|
    |<span data-ttu-id="60025-195">**Button**</span><span class="sxs-lookup"><span data-stu-id="60025-195">**Button**</span></span>|<span data-ttu-id="60025-196">名称： EnterGuess</span><span class="sxs-lookup"><span data-stu-id="60025-196">Name: EnterGuess</span></span><br /><br /> <span data-ttu-id="60025-197">位置：121、42</span><span class="sxs-lookup"><span data-stu-id="60025-197">Location: 121, 42</span></span><br /><br /> <span data-ttu-id="60025-198">大小：75，23</span><span class="sxs-lookup"><span data-stu-id="60025-198">Size: 75, 23</span></span><br /><br /> <span data-ttu-id="60025-199">文本：输入推测</span><span class="sxs-lookup"><span data-stu-id="60025-199">Text: Enter Guess</span></span>|
    |<span data-ttu-id="60025-200">**Button**</span><span class="sxs-lookup"><span data-stu-id="60025-200">**Button**</span></span>|<span data-ttu-id="60025-201">名称： QuitGame</span><span class="sxs-lookup"><span data-stu-id="60025-201">Name: QuitGame</span></span><br /><br /> <span data-ttu-id="60025-202">位置：274、42</span><span class="sxs-lookup"><span data-stu-id="60025-202">Location: 274, 42</span></span><br /><br /> <span data-ttu-id="60025-203">大小：75，23</span><span class="sxs-lookup"><span data-stu-id="60025-203">Size: 75, 23</span></span><br /><br /> <span data-ttu-id="60025-204">文本： Quit</span><span class="sxs-lookup"><span data-stu-id="60025-204">Text: Quit</span></span>|
    |<span data-ttu-id="60025-205">**TextBox**</span><span class="sxs-lookup"><span data-stu-id="60025-205">**TextBox**</span></span>|<span data-ttu-id="60025-206">名称： WorkflowStatus</span><span class="sxs-lookup"><span data-stu-id="60025-206">Name: WorkflowStatus</span></span><br /><br /> <span data-ttu-id="60025-207">位置：10，73</span><span class="sxs-lookup"><span data-stu-id="60025-207">Location: 10, 73</span></span><br /><br /> <span data-ttu-id="60025-208">多行： True</span><span class="sxs-lookup"><span data-stu-id="60025-208">Multiline: True</span></span><br /><br /> <span data-ttu-id="60025-209">ReadOnly： True</span><span class="sxs-lookup"><span data-stu-id="60025-209">ReadOnly: True</span></span><br /><br /> <span data-ttu-id="60025-210">滚动条：垂直</span><span class="sxs-lookup"><span data-stu-id="60025-210">ScrollBars: Vertical</span></span><br /><br /> <span data-ttu-id="60025-211">大小：338、208</span><span class="sxs-lookup"><span data-stu-id="60025-211">Size: 338, 208</span></span>|

5. <span data-ttu-id="60025-212">将窗体的 **AcceptButton** 属性设置为 **EnterGuess**。</span><span class="sxs-lookup"><span data-stu-id="60025-212">Set the **AcceptButton** property of the form to **EnterGuess**.</span></span>

 <span data-ttu-id="60025-213">以下示例展示了完成的窗体。</span><span class="sxs-lookup"><span data-stu-id="60025-213">The following example illustrates the completed form.</span></span>

 ![Windows Workflow Foundation 工作流宿主窗体的屏幕截图。](./media/how-to-create-and-run-a-long-running-workflow/windows-workflow-foundation-workflowhostform.png)

## <a name="to-add-the-properties-and-helper-methods-of-the-form"></a><span data-ttu-id="60025-215">添加窗体的属性和帮助器方法</span><span class="sxs-lookup"><span data-stu-id="60025-215">To add the properties and helper methods of the form</span></span>

<span data-ttu-id="60025-216">本节的步骤将属性和帮助器添加至窗体类，此窗体类将配置窗体的 UI，以支持运行和恢复数字猜测工作流。</span><span class="sxs-lookup"><span data-stu-id="60025-216">The steps in this section add properties and helper methods to the form class that configure the UI of the form to support running and resuming number guess workflows.</span></span>

1. <span data-ttu-id="60025-217">在 **解决方案资源管理器** 中右键单击 " **WorkflowHostForm** "，然后选择 "**查看代码**"。</span><span class="sxs-lookup"><span data-stu-id="60025-217">Right-click **WorkflowHostForm** in **Solution Explorer** and choose **View Code**.</span></span>

2. <span data-ttu-id="60025-218">在包含其他 `using`（或 `Imports`）语句的文件的顶部添加以下 `using`（或 `Imports`）语句。</span><span class="sxs-lookup"><span data-stu-id="60025-218">Add the following `using` (or `Imports`) statements at the top of the file with the other `using` (or `Imports`) statements.</span></span>

    ```vb
    Imports System.Activities
    Imports System.Activities.DurableInstancing
    Imports System.Data.SqlClient
    Imports System.IO
    Imports System.Windows.Forms
    ```

    ```csharp
    using System.Activities;
    using System.Activities.DurableInstancing;
    using System.Data.SqlClient;
    using System.IO;
    using System.Windows.Forms;
    ```

3. <span data-ttu-id="60025-219">将以下成员声明添加到 **WorkflowHostForm** 类。</span><span class="sxs-lookup"><span data-stu-id="60025-219">Add the following member declarations to the **WorkflowHostForm** class.</span></span>

    ```vb
    Const connectionString = "Server=.\SQLEXPRESS;Initial Catalog=WF45GettingStartedTutorial;Integrated Security=SSPI"
    Dim store As SqlWorkflowInstanceStore
    Dim workflowStarting As Boolean
    ```

    ```csharp
    const string connectionString = "Server=.\\SQLEXPRESS;Initial Catalog=WF45GettingStartedTutorial;Integrated Security=SSPI";
    SqlWorkflowInstanceStore store;
    bool workflowStarting;
    ```

    > [!NOTE]
    > <span data-ttu-id="60025-220">如果您的连接字符串不同，请更新 `connectionString` 引用数据库。</span><span class="sxs-lookup"><span data-stu-id="60025-220">If your connection string is different, update `connectionString` to refer to your database.</span></span>

4. <span data-ttu-id="60025-221">将 `WorkflowInstanceId` 属性添加到 `WorkflowFormHost` 类中。</span><span class="sxs-lookup"><span data-stu-id="60025-221">Add a `WorkflowInstanceId` property to the `WorkflowFormHost` class.</span></span>

    ```vb
    Public ReadOnly Property WorkflowInstanceId() As Guid
        Get
            If InstanceId.SelectedIndex = -1 Then
                Return Guid.Empty
            Else
                Return New Guid(InstanceId.SelectedItem.ToString())
            End If
        End Get
    End Property
    ```

    ```csharp
    public Guid WorkflowInstanceId
    {
        get
        {
            return InstanceId.SelectedIndex == -1 ? Guid.Empty : (Guid)InstanceId.SelectedItem;
        }
    }
    ```

    <span data-ttu-id="60025-222">`InstanceId`组合框显示持久化工作流实例 id 的列表， `WorkflowInstanceId` 属性返回当前选择的工作流。</span><span class="sxs-lookup"><span data-stu-id="60025-222">The `InstanceId` combo box displays a list of persisted workflow instance ids, and the `WorkflowInstanceId` property returns the currently selected workflow.</span></span>

5. <span data-ttu-id="60025-223">为窗体 `Load` 事件添加处理程序。</span><span class="sxs-lookup"><span data-stu-id="60025-223">Add a handler for the form `Load` event.</span></span> <span data-ttu-id="60025-224">若要添加该处理程序，请切换到窗体的 **设计视图**，单击 "**属性**" 窗口顶部的 "**事件**" 图标，然后双击 "**加载**"。</span><span class="sxs-lookup"><span data-stu-id="60025-224">To add the handler, switch to **Design View** for the form, click the **Events** icon at the top of the **Properties** window, and double-click **Load**.</span></span>

    ```vb
    Private Sub WorkflowHostForm_Load(sender As Object, e As EventArgs) Handles Me.Load

    End Sub
    ```

    ```csharp
    private void WorkflowHostForm_Load(object sender, EventArgs e)
    {

    }
    ```

6. <span data-ttu-id="60025-225">将以下代码添加到 `WorkflowHostForm_Load`。</span><span class="sxs-lookup"><span data-stu-id="60025-225">Add the following code to `WorkflowHostForm_Load`.</span></span>

    ```vb
    ' Initialize the store and configure it so that it can be used for
    ' multiple WorkflowApplication instances.
    store = New SqlWorkflowInstanceStore(connectionString)
    WorkflowApplication.CreateDefaultInstanceOwner(store, Nothing, WorkflowIdentityFilter.Any)

    ' Set default ComboBox selections.
    NumberRange.SelectedIndex = 0
    WorkflowType.SelectedIndex = 0

    ListPersistedWorkflows()
    ```

    ```csharp
    // Initialize the store and configure it so that it can be used for
    // multiple WorkflowApplication instances.
    store = new SqlWorkflowInstanceStore(connectionString);
    WorkflowApplication.CreateDefaultInstanceOwner(store, null, WorkflowIdentityFilter.Any);

    // Set default ComboBox selections.
    NumberRange.SelectedIndex = 0;
    WorkflowType.SelectedIndex = 0;

    ListPersistedWorkflows();
    ```

    <span data-ttu-id="60025-226">窗体加载时，将配置 `SqlWorkflowInstanceStore`，范围和工作流类型组合框将设置为默认值，持久性工作流实例将添加到 `InstanceId` 组合框。</span><span class="sxs-lookup"><span data-stu-id="60025-226">When the form loads, the `SqlWorkflowInstanceStore` is configured, the range and workflow type combo boxes are set to default values, and the persisted workflow instances are added to the `InstanceId` combo box.</span></span>

7. <span data-ttu-id="60025-227">为 `SelectedIndexChanged` 添加 `InstanceId` 处理程序。</span><span class="sxs-lookup"><span data-stu-id="60025-227">Add a `SelectedIndexChanged` handler for `InstanceId`.</span></span> <span data-ttu-id="60025-228">若要添加该处理程序，请切换到窗体的 **设计视图**，选择 `InstanceId` 组合框，单击 "**属性**" 窗口顶部的 "**事件**" 图标，然后双击 " **SelectedIndexChanged**"。</span><span class="sxs-lookup"><span data-stu-id="60025-228">To add the handler, switch to **Design View** for the form, select the `InstanceId` combo box, click the **Events** icon at the top of the **Properties** window, and double-click **SelectedIndexChanged**.</span></span>

    ```vb
    Private Sub InstanceId_SelectedIndexChanged(sender As Object, e As EventArgs) Handles InstanceId.SelectedIndexChanged

    End Sub
    ```

    ```csharp
    private void InstanceId_SelectedIndexChanged(object sender, EventArgs e)
    {

    }
    ```

8. <span data-ttu-id="60025-229">将以下代码添加到 `InstanceId_SelectedIndexChanged`。</span><span class="sxs-lookup"><span data-stu-id="60025-229">Add the following code to `InstanceId_SelectedIndexChanged`.</span></span> <span data-ttu-id="60025-230">只要用户使用组合框选择一个工作流，此处理程序就会更新状态窗口。</span><span class="sxs-lookup"><span data-stu-id="60025-230">Whenever the user selects a workflow by using the combo box this handler updates the status window.</span></span>

    ```vb
    If InstanceId.SelectedIndex = -1 Then
        Return
    End If

    ' Clear the status window.
    WorkflowStatus.Clear()

    ' Get the workflow version and display it.
    ' If the workflow is just starting then this info will not
    ' be available in the persistence store so do not try and retrieve it.
    If Not workflowStarting Then
        Dim instance As WorkflowApplicationInstance = _
            WorkflowApplication.GetInstance(WorkflowInstanceId, store)

        WorkflowVersion.Text = _
            WorkflowVersionMap.GetIdentityDescription(instance.DefinitionIdentity)

        ' Unload the instance.
        instance.Abandon()
    End If
    ```

    ```csharp
    if (InstanceId.SelectedIndex == -1)
    {
        return;
    }

    // Clear the status window.
    WorkflowStatus.Clear();

    // Get the workflow version and display it.
    // If the workflow is just starting then this info will not
    // be available in the persistence store so do not try and retrieve it.
    if (!workflowStarting)
    {
        WorkflowApplicationInstance instance =
            WorkflowApplication.GetInstance(this.WorkflowInstanceId, store);

        WorkflowVersion.Text =
            WorkflowVersionMap.GetIdentityDescription(instance.DefinitionIdentity);

        // Unload the instance.
        instance.Abandon();
    }
    ```

9. <span data-ttu-id="60025-231">将下面的 `ListPersistedWorkflows` 方法添加到窗体类中。</span><span class="sxs-lookup"><span data-stu-id="60025-231">Add the following `ListPersistedWorkflows` method to the form class.</span></span>

    ```vb
    Private Sub ListPersistedWorkflows()
        Using localCon As New SqlConnection(connectionString)
            Dim localCmd As String = _
                "SELECT [InstanceId] FROM [System.Activities.DurableInstancing].[Instances] ORDER BY [CreationTime]"

            Dim cmd As SqlCommand = localCon.CreateCommand()
            cmd.CommandText = localCmd
            localCon.Open()
            Using reader As SqlDataReader = cmd.ExecuteReader(CommandBehavior.CloseConnection)

                While (reader.Read())
                    ' Get the InstanceId of the persisted Workflow.
                    Dim id As Guid = Guid.Parse(reader(0).ToString())
                    InstanceId.Items.Add(id)
                End While
            End Using
        End Using
    End Sub
    ```

    ```csharp
    using (var localCon = new SqlConnection(connectionString))
    {
        string localCmd =
            "SELECT [InstanceId] FROM [System.Activities.DurableInstancing].[Instances] ORDER BY [CreationTime]";

        SqlCommand cmd = localCon.CreateCommand();
        cmd.CommandText = localCmd;
        localCon.Open();
        using (SqlDataReader reader = cmd.ExecuteReader(CommandBehavior.CloseConnection))
        {
            while (reader.Read())
            {
                // Get the InstanceId of the persisted Workflow.
                Guid id = Guid.Parse(reader[0].ToString());
                InstanceId.Items.Add(id);
            }
        }
    }
    ```

    <span data-ttu-id="60025-232">`ListPersistedWorkflows` 查询持久性工作流实例的实例存储，并将实例 ID 添加到 `cboInstanceId` 组合框。</span><span class="sxs-lookup"><span data-stu-id="60025-232">`ListPersistedWorkflows` queries the instance store for persisted workflow instances, and adds the instance ids to the `cboInstanceId` combo box.</span></span>

10. <span data-ttu-id="60025-233">将下面的 `UpdateStatus` 方法和对应的委托添加到窗体类中。</span><span class="sxs-lookup"><span data-stu-id="60025-233">Add the following `UpdateStatus` method and corresponding delegate to the form class.</span></span> <span data-ttu-id="60025-234">此方法使用当前正在运行的工作流的状态来更新窗体上的状态窗口。</span><span class="sxs-lookup"><span data-stu-id="60025-234">This method updates the status window on the form with the status of the currently running workflow.</span></span>

    ```vb
    Private Delegate Sub UpdateStatusDelegate(msg As String)
    Public Sub UpdateStatus(msg As String)
        ' We may be on a different thread so we need to
        ' make this call using BeginInvoke.
        If InvokeRequired Then
            BeginInvoke(New UpdateStatusDelegate(AddressOf UpdateStatus), msg)
        Else
            If Not msg.EndsWith(vbCrLf) Then
                msg = msg & vbCrLf
            End If

            WorkflowStatus.AppendText(msg)

            ' Ensure that the newly added status is visible.
            WorkflowStatus.SelectionStart = WorkflowStatus.Text.Length
            WorkflowStatus.ScrollToCaret()
        End If
    End Sub
    ```

    ```csharp
    private delegate void UpdateStatusDelegate(string msg);
    public void UpdateStatus(string msg)
    {
        // We may be on a different thread so we need to
        // make this call using BeginInvoke.
        if (InvokeRequired)
        {
            BeginInvoke(new UpdateStatusDelegate(UpdateStatus), msg);
        }
        else
        {
            if (!msg.EndsWith("\r\n"))
            {
                msg += "\r\n";
            }
            WorkflowStatus.AppendText(msg);

            WorkflowStatus.SelectionStart = WorkflowStatus.Text.Length;
            WorkflowStatus.ScrollToCaret();
        }
    }
    ```

11. <span data-ttu-id="60025-235">将下面的 `GameOver` 方法和对应的委托添加到窗体类中。</span><span class="sxs-lookup"><span data-stu-id="60025-235">Add the following `GameOver` method and corresponding delegate to the form class.</span></span> <span data-ttu-id="60025-236">当工作流完成时，此方法将通过从 **InstanceId** 组合框中删除已完成工作流的实例 id 来更新窗体 UI。</span><span class="sxs-lookup"><span data-stu-id="60025-236">When a workflow completes, this method updates the form UI by removing the instance id of the completed workflow from the **InstanceId** combo box.</span></span>

    ```vb
    Private Delegate Sub GameOverDelegate()
    Private Sub GameOver()
        If InvokeRequired Then
            BeginInvoke(New GameOverDelegate(AddressOf GameOver))
        Else
            ' Remove this instance from the InstanceId combo box.
            InstanceId.Items.Remove(InstanceId.SelectedItem)
            InstanceId.SelectedIndex = -1
        End If
    End Sub
    ```

    ```csharp
    private delegate void GameOverDelegate();
    private void GameOver()
    {
        if (InvokeRequired)
        {
            BeginInvoke(new GameOverDelegate(GameOver));
        }
        else
        {
            // Remove this instance from the combo box.
            InstanceId.Items.Remove(InstanceId.SelectedItem);
            InstanceId.SelectedIndex = -1;
        }
    }
    ```

## <a name="to-configure-the-instance-store-workflow-lifecycle-handlers-and-extensions"></a><span data-ttu-id="60025-237">配置实例存储、工作流生命周期处理程序和扩展</span><span class="sxs-lookup"><span data-stu-id="60025-237">To configure the instance store, workflow lifecycle handlers, and extensions</span></span>

1. <span data-ttu-id="60025-238">向窗体类添加 `ConfigureWorkflowApplication` 方法。</span><span class="sxs-lookup"><span data-stu-id="60025-238">Add a `ConfigureWorkflowApplication` method to the form class.</span></span>

    ```vb
    Private Sub ConfigureWorkflowApplication(wfApp As WorkflowApplication)

    End Sub
    ```

    ```csharp
    private void ConfigureWorkflowApplication(WorkflowApplication wfApp)
    {
    }
    ```

    <span data-ttu-id="60025-239">此方法配置 `WorkflowApplication`、添加所需扩展并添加工作流生命周期事件的处理程序。</span><span class="sxs-lookup"><span data-stu-id="60025-239">This method configures the `WorkflowApplication`, adds the desired extensions, and adds handlers for the workflow lifecycle events.</span></span>

2. <span data-ttu-id="60025-240">在 `ConfigureWorkflowApplication` 中，指定 `SqlWorkflowInstanceStore` 的 `WorkflowApplication`。</span><span class="sxs-lookup"><span data-stu-id="60025-240">In `ConfigureWorkflowApplication`, specify the `SqlWorkflowInstanceStore` for the `WorkflowApplication`.</span></span>

    ```vb
    ' Configure the persistence store.
    wfApp.InstanceStore = store
    ```

    ```csharp
    // Configure the persistence store.
    wfApp.InstanceStore = store;
    ```

3. <span data-ttu-id="60025-241">接下来，创建一个 `StringWriter` 实例，并将它添加到 `Extensions` 的 `WorkflowApplication` 集合中。</span><span class="sxs-lookup"><span data-stu-id="60025-241">Next, create a `StringWriter` instance and add it to the `Extensions` collection of the `WorkflowApplication`.</span></span> <span data-ttu-id="60025-242">当将 `StringWriter` 添加到扩展时，它将捕获所有 `WriteLine` 活动输出。</span><span class="sxs-lookup"><span data-stu-id="60025-242">When a `StringWriter` is added to the extensions it captures all `WriteLine` activity output.</span></span> <span data-ttu-id="60025-243">当工作流进入空闲状态时，`WriteLine` 输出可从 `StringWriter` 提取并显示在窗体上。</span><span class="sxs-lookup"><span data-stu-id="60025-243">When the workflow becomes idle, the `WriteLine` output can be extracted from the `StringWriter` and displayed on the form.</span></span>

    ```vb
    ' Add a StringWriter to the extensions. This captures the output
    ' from the WriteLine activities so we can display it in the form.
    Dim sw As New StringWriter()
    wfApp.Extensions.Add(sw)
    ```

    ```csharp
    // Add a StringWriter to the extensions. This captures the output
    // from the WriteLine activities so we can display it in the form.
    var sw = new StringWriter();
    wfApp.Extensions.Add(sw);
    ```

4. <span data-ttu-id="60025-244">为 `Completed` 事件添加以下处理程序。</span><span class="sxs-lookup"><span data-stu-id="60025-244">Add the following handler for the `Completed` event.</span></span> <span data-ttu-id="60025-245">在工作流成功完成时，执行猜测数字的轮数会显示到状态窗口。</span><span class="sxs-lookup"><span data-stu-id="60025-245">When a workflow successfully completes, the number of turns taken to guess the number is displayed to the status window.</span></span> <span data-ttu-id="60025-246">如果工作流终止，系统会显示导致终止的异常信息。</span><span class="sxs-lookup"><span data-stu-id="60025-246">If the workflow terminates, the exception information that caused the termination is displayed.</span></span> <span data-ttu-id="60025-247">在处理程序结尾处调用了 `GameOver` 方法，该方法从工作流列表中删除已完成的工作流。</span><span class="sxs-lookup"><span data-stu-id="60025-247">At the end of the handler the `GameOver` method is called, which removes the completed workflow from the workflow list.</span></span>

    ```vb
    wfApp.Completed = _
        Sub(e As WorkflowApplicationCompletedEventArgs)
            If e.CompletionState = ActivityInstanceState.Faulted Then
                UpdateStatus($"Workflow Terminated. Exception: {e.TerminationException.GetType().FullName}{vbCrLf}{e.TerminationException.Message}")
            ElseIf e.CompletionState = ActivityInstanceState.Canceled Then
                UpdateStatus("Workflow Canceled.")
            Else
                Dim turns As Integer = Convert.ToInt32(e.Outputs("Turns"))
                UpdateStatus($"Congratulations, you guessed the number in {turns} turns.")
            End If
            GameOver()
        End Sub
    ```

    ```csharp
    wfApp.Completed = delegate(WorkflowApplicationCompletedEventArgs e)
    {
        if (e.CompletionState == ActivityInstanceState.Faulted)
        {
            UpdateStatus($"Workflow Terminated. Exception: {e.TerminationException.GetType().FullName}\r\n{e.TerminationException.Message}");
        }
        else if (e.CompletionState == ActivityInstanceState.Canceled)
        {
            UpdateStatus("Workflow Canceled.");
        }
        else
        {
            int turns = Convert.ToInt32(e.Outputs["Turns"]);
            UpdateStatus($"Congratulations, you guessed the number in {turns} turns.");
        }
        GameOver();
    };
    ```

5. <span data-ttu-id="60025-248">添加以下 `Aborted` 和 `OnUnhandledException` 处理程序。</span><span class="sxs-lookup"><span data-stu-id="60025-248">Add the following `Aborted` and `OnUnhandledException` handlers.</span></span> <span data-ttu-id="60025-249">`GameOver` 方法不从 `Aborted` 处理程序中调用，因为在工作流实例中止时，它并未终止，且以后可能恢复实例。</span><span class="sxs-lookup"><span data-stu-id="60025-249">The `GameOver` method is not called from the `Aborted` handler because when a workflow instance is aborted, it does not terminate, and it is possible to resume the instance at a later time.</span></span>

    ```vb
    wfApp.Aborted = _
        Sub(e As WorkflowApplicationAbortedEventArgs)
            UpdateStatus($"Workflow Aborted. Exception: {e.Reason.GetType().FullName}{vbCrLf}{e.Reason.Message}")
        End Sub

    wfApp.OnUnhandledException = _
        Function(e As WorkflowApplicationUnhandledExceptionEventArgs)
            UpdateStatus($"Unhandled Exception: {e.UnhandledException.GetType().FullName}{vbCrLf}{e.UnhandledException.Message}")
            GameOver()
            Return UnhandledExceptionAction.Terminate
        End Function
    ```

    ```csharp
    wfApp.Aborted = delegate(WorkflowApplicationAbortedEventArgs e)
    {
        UpdateStatus($"Workflow Aborted. Exception: {e.Reason.GetType().FullName}\r\n{e.Reason.Message}");
    };

    wfApp.OnUnhandledException = delegate(WorkflowApplicationUnhandledExceptionEventArgs e)
    {
        UpdateStatus($"Unhandled Exception: {e.UnhandledException.GetType().FullName}\r\n{e.UnhandledException.Message}");
        GameOver();
        return UnhandledExceptionAction.Terminate;
    };
    ```

6. <span data-ttu-id="60025-250">添加以下 `PersistableIdle` 处理程序。</span><span class="sxs-lookup"><span data-stu-id="60025-250">Add the following `PersistableIdle` handler.</span></span> <span data-ttu-id="60025-251">此处理程序检索添加的 `StringWriter` 扩展，提取 `WriteLine` 活动的输出，并将它显示在状态窗口中。</span><span class="sxs-lookup"><span data-stu-id="60025-251">This handler retrieves the `StringWriter` extension that was added, extracts the output from the `WriteLine` activities, and displays it in the status window.</span></span>

    ```vb
    wfApp.PersistableIdle = _
        Function(e As WorkflowApplicationIdleEventArgs)
            ' Send the current WriteLine outputs to the status window.
            Dim writers = e.GetInstanceExtensions(Of StringWriter)()
            For Each writer In writers
                UpdateStatus(writer.ToString())
            Next
            Return PersistableIdleAction.Unload
        End Function
    ```

    ```csharp
    wfApp.PersistableIdle = delegate(WorkflowApplicationIdleEventArgs e)
    {
        // Send the current WriteLine outputs to the status window.
        var writers = e.GetInstanceExtensions<StringWriter>();
        foreach (var writer in writers)
        {
            UpdateStatus(writer.ToString());
        }
        return PersistableIdleAction.Unload;
    };
    ```

    <span data-ttu-id="60025-252"><xref:System.Activities.PersistableIdleAction> 枚举有三个值：<xref:System.Activities.PersistableIdleAction.None>、 <xref:System.Activities.PersistableIdleAction.Persist> 和 <xref:System.Activities.PersistableIdleAction.Unload>。</span><span class="sxs-lookup"><span data-stu-id="60025-252">The <xref:System.Activities.PersistableIdleAction> enumeration has three values: <xref:System.Activities.PersistableIdleAction.None>, <xref:System.Activities.PersistableIdleAction.Persist>, and <xref:System.Activities.PersistableIdleAction.Unload>.</span></span> <span data-ttu-id="60025-253"><xref:System.Activities.PersistableIdleAction.Persist> 会导致工作流持久保存，但不会导致工作流卸载。</span><span class="sxs-lookup"><span data-stu-id="60025-253"><xref:System.Activities.PersistableIdleAction.Persist> causes the workflow to persist but it does not cause the workflow to unload.</span></span> <span data-ttu-id="60025-254"><xref:System.Activities.PersistableIdleAction.Unload> 会导致工作流持久保存并卸载。</span><span class="sxs-lookup"><span data-stu-id="60025-254"><xref:System.Activities.PersistableIdleAction.Unload> causes the workflow to persist and be unloaded.</span></span>

    <span data-ttu-id="60025-255">以下示例是完成的 `ConfigureWorkflowApplication` 方法。</span><span class="sxs-lookup"><span data-stu-id="60025-255">The following example is the completed `ConfigureWorkflowApplication` method.</span></span>

    ```vb
    Private Sub ConfigureWorkflowApplication(wfApp As WorkflowApplication)
        ' Configure the persistence store.
        wfApp.InstanceStore = store

        ' Add a StringWriter to the extensions. This captures the output
        ' from the WriteLine activities so we can display it in the form.
        Dim sw As New StringWriter()
        wfApp.Extensions.Add(sw)

        wfApp.Completed = _
            Sub(e As WorkflowApplicationCompletedEventArgs)
                If e.CompletionState = ActivityInstanceState.Faulted Then
                    UpdateStatus($"Workflow Terminated. Exception: {e.TerminationException.GetType().FullName}{vbCrLf}{e.TerminationException.Message}")
                ElseIf e.CompletionState = ActivityInstanceState.Canceled Then
                    UpdateStatus("Workflow Canceled.")
                Else
                    Dim turns As Integer = Convert.ToInt32(e.Outputs("Turns"))
                    UpdateStatus($"Congratulations, you guessed the number in {turns} turns.")
                End If
                GameOver()
            End Sub

        wfApp.Aborted = _
            Sub(e As WorkflowApplicationAbortedEventArgs)
                UpdateStatus($"Workflow Aborted. Exception: {e.Reason.GetType().FullName}{vbCrLf}{e.Reason.Message}")
            End Sub

        wfApp.OnUnhandledException = _
            Function(e As WorkflowApplicationUnhandledExceptionEventArgs)
                UpdateStatus($"Unhandled Exception: {e.UnhandledException.GetType().FullName}{vbCrLf}{e.UnhandledException.Message}")
                GameOver()
                Return UnhandledExceptionAction.Terminate
            End Function

        wfApp.PersistableIdle = _
            Function(e As WorkflowApplicationIdleEventArgs)
                ' Send the current WriteLine outputs to the status window.
                Dim writers = e.GetInstanceExtensions(Of StringWriter)()
                For Each writer In writers
                    UpdateStatus(writer.ToString())
                Next
                Return PersistableIdleAction.Unload
            End Function
    End Sub
    ```

    ```csharp
    private void ConfigureWorkflowApplication(WorkflowApplication wfApp)
    {
        // Configure the persistence store.
        wfApp.InstanceStore = store;

        // Add a StringWriter to the extensions. This captures the output
        // from the WriteLine activities so we can display it in the form.
        var sw = new StringWriter();
        wfApp.Extensions.Add(sw);

        wfApp.Completed = delegate(WorkflowApplicationCompletedEventArgs e)
        {
            if (e.CompletionState == ActivityInstanceState.Faulted)
            {
                UpdateStatus($"Workflow Terminated. Exception: {e.TerminationException.GetType().FullName}\r\n{e.TerminationException.Message}");
            }
            else if (e.CompletionState == ActivityInstanceState.Canceled)
            {
                UpdateStatus("Workflow Canceled.");
            }
            else
            {
                int turns = Convert.ToInt32(e.Outputs["Turns"]);
                UpdateStatus($"Congratulations, you guessed the number in {turns} turns.");
            }
            GameOver();
        };

        wfApp.Aborted = delegate(WorkflowApplicationAbortedEventArgs e)
        {
            UpdateStatus($"Workflow Aborted. Exception: {e.Reason.GetType().FullName}\r\n{e.Reason.Message}");
        };

        wfApp.OnUnhandledException = delegate(WorkflowApplicationUnhandledExceptionEventArgs e)
        {
            UpdateStatus($"Unhandled Exception: {e.UnhandledException.GetType().FullName}\r\n{e.UnhandledException.Message}");
            GameOver();
            return UnhandledExceptionAction.Terminate;
        };

        wfApp.PersistableIdle = delegate(WorkflowApplicationIdleEventArgs e)
        {
            // Send the current WriteLine outputs to the status window.
            var writers = e.GetInstanceExtensions<StringWriter>();
            foreach (var writer in writers)
            {
                UpdateStatus(writer.ToString());
            }
            return PersistableIdleAction.Unload;
        };
    }
    ```

## <a name="to-enable-starting-and-resuming-multiple-workflow-types"></a><span data-ttu-id="60025-256">支持启动和恢复多个工作流类型</span><span class="sxs-lookup"><span data-stu-id="60025-256">To enable starting and resuming multiple workflow types</span></span>

<span data-ttu-id="60025-257">要恢复工作流实例，主机必须提供工作流定义。</span><span class="sxs-lookup"><span data-stu-id="60025-257">In order to resume a workflow instance, the host has to provide the workflow definition.</span></span> <span data-ttu-id="60025-258">在此教程中有三个工作流类型，且后续教程步骤会介绍这些类型的多个版本。</span><span class="sxs-lookup"><span data-stu-id="60025-258">In this tutorial there are three workflow types, and subsequent tutorial steps introduce multiple versions of these types.</span></span> <span data-ttu-id="60025-259">主机应用程序可通过 `WorkflowIdentity` 将标识信息与持久化工作流实例相关联。</span><span class="sxs-lookup"><span data-stu-id="60025-259">`WorkflowIdentity` provides a way for a host application to associate identifying information with a persisted workflow instance.</span></span> <span data-ttu-id="60025-260">本节中的步骤演示了如何创建一个实用工具类，以帮助将工作流标识从持久化工作流实例映射到对应的工作流定义。</span><span class="sxs-lookup"><span data-stu-id="60025-260">The steps in this section demonstrate how to create a utility class to assist with mapping the workflow identity from a persisted workflow instance to the corresponding workflow definition.</span></span> <span data-ttu-id="60025-261">有关 `WorkflowIdentity` 和版本控制的详细信息，请参阅 [使用 WorkflowIdentity 和版本控制](using-workflowidentity-and-versioning.md)。</span><span class="sxs-lookup"><span data-stu-id="60025-261">For more information about `WorkflowIdentity` and versioning, see [Using WorkflowIdentity and Versioning](using-workflowidentity-and-versioning.md).</span></span>

1. <span data-ttu-id="60025-262">在 **解决方案资源管理器** 中右键单击 " **NumberGuessWorkflowHost** "，然后选择 "**添加**"、"**类**"。</span><span class="sxs-lookup"><span data-stu-id="60025-262">Right-click **NumberGuessWorkflowHost** in **Solution Explorer** and choose **Add**, **Class**.</span></span> <span data-ttu-id="60025-263">`WorkflowVersionMap`在 "**名称**" 框中键入，然后单击 "**添加**"。</span><span class="sxs-lookup"><span data-stu-id="60025-263">Type `WorkflowVersionMap` into the **Name** box and click **Add**.</span></span>

2. <span data-ttu-id="60025-264">在包含其他 `using` 或 `Imports` 语句的文件的顶部添加以下 `using` 或 `Imports` 语句。</span><span class="sxs-lookup"><span data-stu-id="60025-264">Add the following `using` or `Imports` statements at the top of the file with the other `using` or `Imports` statements.</span></span>

    ```vb
    Imports System.Activities
    Imports NumberGuessWorkflowActivities
    ```

    ```csharp
    using System.Activities;
    using NumberGuessWorkflowActivities;
    ```

3. <span data-ttu-id="60025-265">使用以下声明替换 `WorkflowVersionMap` 类声明。</span><span class="sxs-lookup"><span data-stu-id="60025-265">Replace the `WorkflowVersionMap` class declaration with the following declaration.</span></span>

    ```vb
    Public Module WorkflowVersionMap
        Dim map As Dictionary(Of WorkflowIdentity, Activity)

        ' Current version identities.
        Public StateMachineNumberGuessIdentity As WorkflowIdentity
        Public FlowchartNumberGuessIdentity As WorkflowIdentity
        Public SequentialNumberGuessIdentity As WorkflowIdentity

        Sub New()
            map = New Dictionary(Of WorkflowIdentity, Activity)

            ' Add the current workflow version identities.
            StateMachineNumberGuessIdentity = New WorkflowIdentity With
            {
                .Name = "StateMachineNumberGuessWorkflow",
                .Version = New Version(1, 0, 0, 0)
            }

            FlowchartNumberGuessIdentity = New WorkflowIdentity With
            {
                .Name = "FlowchartNumberGuessWorkflow",
                .Version = New Version(1, 0, 0, 0)
            }

            SequentialNumberGuessIdentity = New WorkflowIdentity With
            {
                .Name = "SequentialNumberGuessWorkflow",
                .Version = New Version(1, 0, 0, 0)
            }

            map.Add(StateMachineNumberGuessIdentity, New StateMachineNumberGuessWorkflow())
            map.Add(FlowchartNumberGuessIdentity, New FlowchartNumberGuessWorkflow())
            map.Add(SequentialNumberGuessIdentity, New SequentialNumberGuessWorkflow())
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

        static WorkflowVersionMap()
        {
            map = new Dictionary<WorkflowIdentity, Activity>();

            // Add the current workflow version identities.
            StateMachineNumberGuessIdentity = new WorkflowIdentity
            {
                Name = "StateMachineNumberGuessWorkflow",
                Version = new Version(1, 0, 0, 0)
            };

            FlowchartNumberGuessIdentity = new WorkflowIdentity
            {
                Name = "FlowchartNumberGuessWorkflow",
                Version = new Version(1, 0, 0, 0)
            };

            SequentialNumberGuessIdentity = new WorkflowIdentity
            {
                Name = "SequentialNumberGuessWorkflow",
                Version = new Version(1, 0, 0, 0)
            };

            map.Add(StateMachineNumberGuessIdentity, new StateMachineNumberGuessWorkflow());
            map.Add(FlowchartNumberGuessIdentity, new FlowchartNumberGuessWorkflow());
            map.Add(SequentialNumberGuessIdentity, new SequentialNumberGuessWorkflow());
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

    <span data-ttu-id="60025-266">`WorkflowVersionMap` 包含与此教程中的三个工作流定义对应的三个工作流标识，并在以下各节中工作流启动和恢复时使用。</span><span class="sxs-lookup"><span data-stu-id="60025-266">`WorkflowVersionMap` contains three workflow identities that map to the three workflow definitions from this tutorial and is used in the following sections when workflows are started and resumed.</span></span>

## <a name="to-start-a-new-workflow"></a><span data-ttu-id="60025-267">启动新工作流</span><span class="sxs-lookup"><span data-stu-id="60025-267">To start a new workflow</span></span>

1. <span data-ttu-id="60025-268">为 `Click` 添加 `NewGame` 处理程序。</span><span class="sxs-lookup"><span data-stu-id="60025-268">Add a `Click` handler for `NewGame`.</span></span> <span data-ttu-id="60025-269">若要添加该处理程序，请切换到窗体的 **设计视图** ，然后双击 `NewGame` 。</span><span class="sxs-lookup"><span data-stu-id="60025-269">To add the handler, switch to **Design View** for the form, and double-click `NewGame`.</span></span> <span data-ttu-id="60025-270">此时将添加 `NewGame_Click` 处理程序，视图将切换为窗体的代码视图。</span><span class="sxs-lookup"><span data-stu-id="60025-270">A `NewGame_Click` handler is added and the view switches to code view for the form.</span></span> <span data-ttu-id="60025-271">每当用户单击此按钮时，就会启动新工作流。</span><span class="sxs-lookup"><span data-stu-id="60025-271">Whenever the user clicks this button a new workflow is started.</span></span>

    ```vb
    Private Sub NewGame_Click(sender As Object, e As EventArgs) Handles NewGame.Click

    End Sub
    ```

    ```csharp
    private void NewGame_Click(object sender, EventArgs e)
    {

    }
    ```

2. <span data-ttu-id="60025-272">将以下代码添加到 click 处理程序。</span><span class="sxs-lookup"><span data-stu-id="60025-272">Add the following code to the click handler.</span></span> <span data-ttu-id="60025-273">此代码创建工作流输入自变量的字典，以变量名称作为键。</span><span class="sxs-lookup"><span data-stu-id="60025-273">This code creates a dictionary of input arguments for the workflow, keyed by argument name.</span></span> <span data-ttu-id="60025-274">此字典有一个条目，其中包含从范围组合框检索到的随机生成的数字范围。</span><span class="sxs-lookup"><span data-stu-id="60025-274">This dictionary has one entry that contains the range of the randomly generated number retrieved from the range combo box.</span></span>

    ```vb
    Dim inputs As New Dictionary(Of String, Object)()
    inputs.Add("MaxNumber", Convert.ToInt32(NumberRange.SelectedItem))
    ```

    ```csharp
    var inputs = new Dictionary<string, object>();
    inputs.Add("MaxNumber", Convert.ToInt32(NumberRange.SelectedItem));
    ```

3. <span data-ttu-id="60025-275">接下来，添加以下用于启动工作流的代码。</span><span class="sxs-lookup"><span data-stu-id="60025-275">Next, add the following code that starts the workflow.</span></span> <span data-ttu-id="60025-276">对应于所选工作流类型的 `WorkflowIdentity` 和工作流定义通过 `WorkflowVersionMap` 帮助器类进行检索。</span><span class="sxs-lookup"><span data-stu-id="60025-276">The `WorkflowIdentity` and workflow definition corresponding to the type of workflow selected are retrieved using the `WorkflowVersionMap` helper class.</span></span> <span data-ttu-id="60025-277">接下来，将使用工作流定义、`WorkflowApplication` 和输入变量字典创建新的 `WorkflowIdentity` 实例。</span><span class="sxs-lookup"><span data-stu-id="60025-277">Next, a new `WorkflowApplication` instance is created using the workflow definition, `WorkflowIdentity`, and dictionary of input arguments.</span></span>

    ```vb
    Dim identity As WorkflowIdentity = Nothing
    Select Case WorkflowType.SelectedItem.ToString()
        Case "SequentialNumberGuessWorkflow"
            identity = WorkflowVersionMap.SequentialNumberGuessIdentity

        Case "StateMachineNumberGuessWorkflow"
            identity = WorkflowVersionMap.StateMachineNumberGuessIdentity

        Case "FlowchartNumberGuessWorkflow"
            identity = WorkflowVersionMap.FlowchartNumberGuessIdentity
    End Select

    Dim wf As Activity = WorkflowVersionMap.GetWorkflowDefinition(identity)

    Dim wfApp = New WorkflowApplication(wf, inputs, identity)
    ```

    ```csharp
    WorkflowIdentity identity = null;
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
    };

    Activity wf = WorkflowVersionMap.GetWorkflowDefinition(identity);

    WorkflowApplication wfApp = new WorkflowApplication(wf, inputs, identity);
    ```

4. <span data-ttu-id="60025-278">接下来，添加以下代码，此代码将工作流添加到工作流列表中，并在窗体上显示工作流的版本信息。</span><span class="sxs-lookup"><span data-stu-id="60025-278">Next, add the following code which adds the workflow to the workflow list and displays the workflow's version information on the form.</span></span>

    ```vb
    ' Add the workflow to the list and display the version information.
    workflowStarting = True
    InstanceId.SelectedIndex = InstanceId.Items.Add(wfApp.Id)
    WorkflowVersion.Text = identity.ToString()
    workflowStarting = False
    ```

    ```csharp
    // Add the workflow to the list and display the version information.
    workflowStarting = true;
    InstanceId.SelectedIndex = InstanceId.Items.Add(wfApp.Id);
    WorkflowVersion.Text = identity.ToString();
    workflowStarting = false;
    ```

5. <span data-ttu-id="60025-279">调用 `ConfigureWorkflowApplication` 为此 `WorkflowApplication` 实例配置实例存储、扩展以及工作流生命周期处理程序。</span><span class="sxs-lookup"><span data-stu-id="60025-279">Call `ConfigureWorkflowApplication` to configure the instance store, extensions, and workflow lifecycle handlers for this `WorkflowApplication` instance.</span></span>

    ```vb
    ' Configure the instance store, extensions, and
    ' workflow lifecycle handlers.
    ConfigureWorkflowApplication(wfApp)
    ```

    ```csharp
    // Configure the instance store, extensions, and
    // workflow lifecycle handlers.
    ConfigureWorkflowApplication(wfApp);
    ```

6. <span data-ttu-id="60025-280">最后，调用 `Run`。</span><span class="sxs-lookup"><span data-stu-id="60025-280">Finally, call `Run`.</span></span>

    ```vb
    ' Start the workflow.
    wfApp.Run()
    ```

    ```csharp
    // Start the workflow.
    wfApp.Run();
    ```

     <span data-ttu-id="60025-281">以下示例是完成的 `NewGame_Click` 处理程序。</span><span class="sxs-lookup"><span data-stu-id="60025-281">The following example is the completed `NewGame_Click` handler.</span></span>

    ```vb
    Private Sub NewGame_Click(sender As Object, e As EventArgs) Handles NewGame.Click
        ' Start a new workflow.
        Dim inputs As New Dictionary(Of String, Object)()
        inputs.Add("MaxNumber", Convert.ToInt32(NumberRange.SelectedItem))

        Dim identity As WorkflowIdentity = Nothing
        Select Case WorkflowType.SelectedItem.ToString()
            Case "SequentialNumberGuessWorkflow"
                identity = WorkflowVersionMap.SequentialNumberGuessIdentity

            Case "StateMachineNumberGuessWorkflow"
                identity = WorkflowVersionMap.StateMachineNumberGuessIdentity

            Case "FlowchartNumberGuessWorkflow"
                identity = WorkflowVersionMap.FlowchartNumberGuessIdentity
        End Select

        Dim wf As Activity = WorkflowVersionMap.GetWorkflowDefinition(identity)

        Dim wfApp = New WorkflowApplication(wf, inputs, identity)

        ' Add the workflow to the list and display the version information.
        workflowStarting = True
        InstanceId.SelectedIndex = InstanceId.Items.Add(wfApp.Id)
        WorkflowVersion.Text = identity.ToString()
        workflowStarting = False

        ' Configure the instance store, extensions, and
        ' workflow lifecycle handlers.
        ConfigureWorkflowApplication(wfApp)

        ' Start the workflow.
        wfApp.Run()
    End Sub
    ```

    ```csharp
    private void NewGame_Click(object sender, EventArgs e)
    {
        var inputs = new Dictionary<string, object>();
        inputs.Add("MaxNumber", Convert.ToInt32(NumberRange.SelectedItem));

        WorkflowIdentity identity = null;
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
        };

        Activity wf = WorkflowVersionMap.GetWorkflowDefinition(identity);

        var wfApp = new WorkflowApplication(wf, inputs, identity);

        // Add the workflow to the list and display the version information.
        workflowStarting = true;
        InstanceId.SelectedIndex = InstanceId.Items.Add(wfApp.Id);
        WorkflowVersion.Text = identity.ToString();
        workflowStarting = false;

        // Configure the instance store, extensions, and
        // workflow lifecycle handlers.
        ConfigureWorkflowApplication(wfApp);

        // Start the workflow.
        wfApp.Run();
    }
    ```

## <a name="to-resume-a-workflow"></a><span data-ttu-id="60025-282">恢复工作流</span><span class="sxs-lookup"><span data-stu-id="60025-282">To resume a workflow</span></span>

1. <span data-ttu-id="60025-283">为 `Click` 添加 `EnterGuess` 处理程序。</span><span class="sxs-lookup"><span data-stu-id="60025-283">Add a `Click` handler for `EnterGuess`.</span></span> <span data-ttu-id="60025-284">若要添加该处理程序，请切换到窗体的 **设计视图** ，然后双击 `EnterGuess` 。</span><span class="sxs-lookup"><span data-stu-id="60025-284">To add the handler, switch to **Design View** for the form, and double-click `EnterGuess`.</span></span> <span data-ttu-id="60025-285">每当用户单击此按钮时，就会恢复工作流。</span><span class="sxs-lookup"><span data-stu-id="60025-285">Whenever the user clicks this button a workflow is resumed.</span></span>

    ```vb
    Private Sub EnterGuess_Click(sender As Object, e As EventArgs) Handles EnterGuess.Click

    End Sub
    ```

    ```csharp
    private void EnterGuess_Click(object sender, EventArgs e)
    {

    }
    ```

2. <span data-ttu-id="60025-286">添加以下代码，以确保在工作流列表中选择了一个工作流，且用户的猜测有效。</span><span class="sxs-lookup"><span data-stu-id="60025-286">Add the following code to ensure that a workflow is selected in the workflow list, and that the user's guess is valid.</span></span>

    ```vb
    If WorkflowInstanceId = Guid.Empty Then
        MessageBox.Show("Please select a workflow.")
        Return
    End If

    Dim userGuess As Integer
    If Not Int32.TryParse(Guess.Text, userGuess) Then
        MessageBox.Show("Please enter an integer.")
        Guess.SelectAll()
        Guess.Focus()
        Return
    End If
    ```

    ```csharp
    if (WorkflowInstanceId == Guid.Empty)
    {
        MessageBox.Show("Please select a workflow.");
        return;
    }

    int guess;
    if (!Int32.TryParse(Guess.Text, out guess))
    {
        MessageBox.Show("Please enter an integer.");
        Guess.SelectAll();
        Guess.Focus();
        return;
    }
    ```

3. <span data-ttu-id="60025-287">接下来，检索持久化工作流实例的 `WorkflowApplicationInstance`。</span><span class="sxs-lookup"><span data-stu-id="60025-287">Next, retrieve the `WorkflowApplicationInstance` of the persisted workflow instance.</span></span> <span data-ttu-id="60025-288">`WorkflowApplicationInstance` 表示尚未与工作流定义关联的持久化工作流实例。</span><span class="sxs-lookup"><span data-stu-id="60025-288">A `WorkflowApplicationInstance` represents a persisted workflow instance that has not yet been associated with a workflow definition.</span></span> <span data-ttu-id="60025-289">`DefinitionIdentity` 的 `WorkflowApplicationInstance` 包含持久化工作流实例的 `WorkflowIdentity`。</span><span class="sxs-lookup"><span data-stu-id="60025-289">The `DefinitionIdentity` of the `WorkflowApplicationInstance` contains the `WorkflowIdentity` of the persisted workflow instance.</span></span> <span data-ttu-id="60025-290">本教程中使用 `WorkflowVersionMap` 实用工具类，将 `WorkflowIdentity` 映射到正确的工作流定义。</span><span class="sxs-lookup"><span data-stu-id="60025-290">In this tutorial, the `WorkflowVersionMap` utility class is used to map the `WorkflowIdentity` to the correct workflow definition.</span></span> <span data-ttu-id="60025-291">检索工作流定义后，即使用正确的工作流定义创建 `WorkflowApplication`。</span><span class="sxs-lookup"><span data-stu-id="60025-291">Once the workflow definition is retrieved, a `WorkflowApplication` is created, using the correct workflow definition.</span></span>

    ```vb
    Dim instance As WorkflowApplicationInstance = _
        WorkflowApplication.GetInstance(WorkflowInstanceId, store)

    ' Use the persisted WorkflowIdentity to retrieve the correct workflow
    ' definition from the dictionary.
    Dim wf As Activity = _
        WorkflowVersionMap.GetWorkflowDefinition(instance.DefinitionIdentity)

    ' Associate the WorkflowApplication with the correct definition
    Dim wfApp As New WorkflowApplication(wf, instance.DefinitionIdentity)
    ```

    ```csharp
    WorkflowApplicationInstance instance =
        WorkflowApplication.GetInstance(WorkflowInstanceId, store);

    // Use the persisted WorkflowIdentity to retrieve the correct workflow
    // definition from the dictionary.
    Activity wf =
        WorkflowVersionMap.GetWorkflowDefinition(instance.DefinitionIdentity);

    // Associate the WorkflowApplication with the correct definition
    var wfApp = new WorkflowApplication(wf, instance.DefinitionIdentity);
    ```

4. <span data-ttu-id="60025-292">创建 `WorkflowApplication` 后，请调用 `ConfigureWorkflowApplication` 以配置实例存储、工作流生命周期处理程序以及扩展。</span><span class="sxs-lookup"><span data-stu-id="60025-292">Once the `WorkflowApplication` is created, configure the instance store, workflow lifecycle handlers, and extensions by calling `ConfigureWorkflowApplication`.</span></span> <span data-ttu-id="60025-293">每次创建新 `WorkflowApplication` 时都必须执行这些步骤，并且必须在将工作流实例加载到 `WorkflowApplication` 中之前完成。</span><span class="sxs-lookup"><span data-stu-id="60025-293">These steps must be done every time a new `WorkflowApplication` is created, and they must be done before the workflow instance is loaded into the `WorkflowApplication`.</span></span> <span data-ttu-id="60025-294">在加载工作流后，此工作流通过用户的猜测恢复执行。</span><span class="sxs-lookup"><span data-stu-id="60025-294">After the workflow is loaded, it is resumed with the user's guess.</span></span>

    ```vb
    ' Configure the extensions and lifecycle handlers.
    ' Do this before the instance is loaded. Once the instance is
    ' loaded it is too late to add extensions.
    ConfigureWorkflowApplication(wfApp)

    ' Load the workflow.
    wfApp.Load(instance)

    ' Resume the workflow.
    wfApp.ResumeBookmark("EnterGuess", userGuess)
    ```

    ```csharp
    // Configure the extensions and lifecycle handlers.
    // Do this before the instance is loaded. Once the instance is
    // loaded it is too late to add extensions.
    ConfigureWorkflowApplication(wfApp);

    // Load the workflow.
    wfApp.Load(instance);

    // Resume the workflow.
    wfApp.ResumeBookmark("EnterGuess", guess);
    ```

5. <span data-ttu-id="60025-295">最后，清除猜测文本框，并使窗体准备接受其他猜测。</span><span class="sxs-lookup"><span data-stu-id="60025-295">Finally, clear the guess textbox and prepare the form to accept another guess.</span></span>

    ```vb
    ' Clear the Guess textbox.
    Guess.Clear()
    Guess.Focus()
    ```

    ```csharp
    // Clear the Guess textbox.
    Guess.Clear();
    Guess.Focus();
    ```

    <span data-ttu-id="60025-296">以下示例是完成的 `EnterGuess_Click` 处理程序。</span><span class="sxs-lookup"><span data-stu-id="60025-296">The following example is the completed `EnterGuess_Click` handler.</span></span>

    ```vb
    Private Sub EnterGuess_Click(sender As Object, e As EventArgs) Handles EnterGuess.Click
        If WorkflowInstanceId = Guid.Empty Then
            MessageBox.Show("Please select a workflow.")
            Return
        End If

        Dim userGuess As Integer
        If Not Int32.TryParse(Guess.Text, userGuess) Then
            MessageBox.Show("Please enter an integer.")
            Guess.SelectAll()
            Guess.Focus()
            Return
        End If

        Dim instance As WorkflowApplicationInstance = _
            WorkflowApplication.GetInstance(WorkflowInstanceId, store)

        ' Use the persisted WorkflowIdentity to retrieve the correct workflow
        ' definition from the dictionary.
        Dim wf As Activity = _
            WorkflowVersionMap.GetWorkflowDefinition(instance.DefinitionIdentity)

        ' Associate the WorkflowApplication with the correct definition
        Dim wfApp As New WorkflowApplication(wf, instance.DefinitionIdentity)

        ' Configure the extensions and lifecycle handlers.
        ' Do this before the instance is loaded. Once the instance is
        ' loaded it is too late to add extensions.
        ConfigureWorkflowApplication(wfApp)

        ' Load the workflow.
        wfApp.Load(instance)

        ' Resume the workflow.
        wfApp.ResumeBookmark("EnterGuess", userGuess)

        ' Clear the Guess textbox.
        Guess.Clear()
        Guess.Focus()
    End Sub
    ```

    ```csharp
    private void EnterGuess_Click(object sender, EventArgs e)
    {
        if (WorkflowInstanceId == Guid.Empty)
        {
            MessageBox.Show("Please select a workflow.");
            return;
        }

        int guess;
        if (!Int32.TryParse(Guess.Text, out guess))
        {
            MessageBox.Show("Please enter an integer.");
            Guess.SelectAll();
            Guess.Focus();
            return;
        }

        WorkflowApplicationInstance instance =
            WorkflowApplication.GetInstance(WorkflowInstanceId, store);

        // Use the persisted WorkflowIdentity to retrieve the correct workflow
        // definition from the dictionary.
        Activity wf =
            WorkflowVersionMap.GetWorkflowDefinition(instance.DefinitionIdentity);

        // Associate the WorkflowApplication with the correct definition
        var wfApp = new WorkflowApplication(wf, instance.DefinitionIdentity);

        // Configure the extensions and lifecycle handlers.
        // Do this before the instance is loaded. Once the instance is
        // loaded it is too late to add extensions.
        ConfigureWorkflowApplication(wfApp);

        // Load the workflow.
        wfApp.Load(instance);

        // Resume the workflow.
        wfApp.ResumeBookmark("EnterGuess", guess);

        // Clear the Guess textbox.
        Guess.Clear();
        Guess.Focus();
    }
    ```

## <a name="to-terminate-a-workflow"></a><span data-ttu-id="60025-297">终止工作流</span><span class="sxs-lookup"><span data-stu-id="60025-297">To terminate a workflow</span></span>

1. <span data-ttu-id="60025-298">为 `Click` 添加 `QuitGame` 处理程序。</span><span class="sxs-lookup"><span data-stu-id="60025-298">Add a `Click` handler for `QuitGame`.</span></span> <span data-ttu-id="60025-299">若要添加该处理程序，请切换到窗体的 **设计视图** ，然后双击 `QuitGame` 。</span><span class="sxs-lookup"><span data-stu-id="60025-299">To add the handler, switch to **Design View** for the form, and double-click `QuitGame`.</span></span> <span data-ttu-id="60025-300">每当用户单击此按钮，即终止当前选择的工作流。</span><span class="sxs-lookup"><span data-stu-id="60025-300">Whenever the user clicks this button the currently selected workflow is terminated.</span></span>

    ```vb
    Private Sub QuitGame_Click(sender As Object, e As EventArgs) Handles QuitGame.Click

    End Sub
    ```

    ```csharp
    private void QuitGame_Click(object sender, EventArgs e)
    {

    }
    ```

2. <span data-ttu-id="60025-301">将以下代码添加到 `QuitGame_Click` 处理程序。</span><span class="sxs-lookup"><span data-stu-id="60025-301">Add the following code to the `QuitGame_Click` handler.</span></span> <span data-ttu-id="60025-302">此代码首先进行检查，以确保在工作流列表中选择了一个工作流。</span><span class="sxs-lookup"><span data-stu-id="60025-302">This code first checks to ensure that a workflow is selected in the workflow list.</span></span> <span data-ttu-id="60025-303">然后，它将该持久化实例加载到 `WorkflowApplicationInstance` 中，使用 `DefinitionIdentity` 确定正确的工作流定义，然后初始化 `WorkflowApplication`。</span><span class="sxs-lookup"><span data-stu-id="60025-303">Then it loads the persisted instance into a `WorkflowApplicationInstance`, uses the `DefinitionIdentity` to determine the correct workflow definition, and then initializes the `WorkflowApplication`.</span></span> <span data-ttu-id="60025-304">接下来，通过调用 `ConfigureWorkflowApplication` 来配置扩展和工作流生命周期处理程序。</span><span class="sxs-lookup"><span data-stu-id="60025-304">Next the extensions and workflow lifecycle handlers are configured with a call to `ConfigureWorkflowApplication`.</span></span> <span data-ttu-id="60025-305">`WorkflowApplication` 配置好后，将加载它，然后调用 `Terminate`。</span><span class="sxs-lookup"><span data-stu-id="60025-305">Once the `WorkflowApplication` is configured, it is loaded, and then `Terminate` is called.</span></span>

    ```vb
    If WorkflowInstanceId = Guid.Empty Then
        MessageBox.Show("Please select a workflow.")
        Return
    End If

    Dim instance As WorkflowApplicationInstance = _
        WorkflowApplication.GetInstance(WorkflowInstanceId, store)

    ' Use the persisted WorkflowIdentity to retrieve the correct workflow
    ' definition from the dictionary.
    Dim wf As Activity = WorkflowVersionMap.GetWorkflowDefinition(instance.DefinitionIdentity)

    ' Associate the WorkflowApplication with the correct definition.
    Dim wfApp As New WorkflowApplication(wf, instance.DefinitionIdentity)

    ' Configure the extensions and lifecycle handlers.
    ConfigureWorkflowApplication(wfApp)

    ' Load the workflow.
    wfApp.Load(instance)

    ' Terminate the workflow.
    wfApp.Terminate("User resigns.")
    ```

    ```csharp
    if (WorkflowInstanceId == Guid.Empty)
    {
        MessageBox.Show("Please select a workflow.");
        return;
    }

    WorkflowApplicationInstance instance =
        WorkflowApplication.GetInstance(WorkflowInstanceId, store);

    // Use the persisted WorkflowIdentity to retrieve the correct workflow
    // definition from the dictionary.
    Activity wf = WorkflowVersionMap.GetWorkflowDefinition(instance.DefinitionIdentity);

    // Associate the WorkflowApplication with the correct definition
    var wfApp = new WorkflowApplication(wf, instance.DefinitionIdentity);

    // Configure the extensions and lifecycle handlers
    ConfigureWorkflowApplication(wfApp);

    // Load the workflow.
    wfApp.Load(instance);

    // Terminate the workflow.
    wfApp.Terminate("User resigns.");
    ```

## <a name="to-build-and-run-the-application"></a><span data-ttu-id="60025-306">生成并运行应用程序</span><span class="sxs-lookup"><span data-stu-id="60025-306">To build and run the application</span></span>

1. <span data-ttu-id="60025-307">双击 **解决方案资源管理器** 中的 " **Program.cs** (或 **Module1**) 以显示代码。</span><span class="sxs-lookup"><span data-stu-id="60025-307">Double-click **Program.cs** (or **Module1.vb**) in **Solution Explorer** to display the code.</span></span>

2. <span data-ttu-id="60025-308">在包含其他 `using`（或 `Imports`）语句的文件的顶部添加以下 `using`（或 `Imports`）语句。</span><span class="sxs-lookup"><span data-stu-id="60025-308">Add the following `using` (or `Imports`) statement at the top of the file with the other `using` (or `Imports`) statements.</span></span>

    ```vb
    Imports System.Windows.Forms
    ```

    ```csharp
    using System.Windows.Forms;
    ```

3. <span data-ttu-id="60025-309">从 [如何：运行工作流](how-to-run-a-workflow.md)，删除或注释掉现有工作流宿主代码，并将其替换为以下代码。</span><span class="sxs-lookup"><span data-stu-id="60025-309">Remove or comment out the existing workflow hosting code from [How to: Run a Workflow](how-to-run-a-workflow.md), and replace it with the following code.</span></span>

    ```vb
    Sub Main()
        Application.EnableVisualStyles()
        Application.Run(New WorkflowHostForm())
    End Sub
    ```

    ```csharp
    static void Main(string[] args)
    {
        Application.EnableVisualStyles();
        Application.Run(new WorkflowHostForm());
    }
    ```

4. <span data-ttu-id="60025-310">在 **解决方案资源管理器** 中右键单击 " **NumberGuessWorkflowHost** "，然后选择 "**属性**"。</span><span class="sxs-lookup"><span data-stu-id="60025-310">Right-click **NumberGuessWorkflowHost** in **Solution Explorer** and choose **Properties**.</span></span> <span data-ttu-id="60025-311">在 "**应用程序**" 选项卡中，为 **输出类型** 指定 **Windows 应用程序**。</span><span class="sxs-lookup"><span data-stu-id="60025-311">In the **Application** tab, specify **Windows Application** for the **Output type**.</span></span> <span data-ttu-id="60025-312">此步骤是可选的，但如果不执行此步骤，则除了窗体之外还会显示控制台窗口。</span><span class="sxs-lookup"><span data-stu-id="60025-312">This step is optional, but if it is not followed the console window is displayed in addition to the form.</span></span>

5. <span data-ttu-id="60025-313">按 Ctrl+Shift+B 生成应用程序。</span><span class="sxs-lookup"><span data-stu-id="60025-313">Press Ctrl+Shift+B to build the application.</span></span>

6. <span data-ttu-id="60025-314">确保将 **NumberGuessWorkflowHost** 设置为启动应用程序，然后按 Ctrl + F5 启动该应用程序。</span><span class="sxs-lookup"><span data-stu-id="60025-314">Ensure that **NumberGuessWorkflowHost** is set as the startup application, and press Ctrl+F5 to start the application.</span></span>

7. <span data-ttu-id="60025-315">为推测游戏选择一个范围，并选择要启动的工作流类型，然后单击 " **新建游戏**"。</span><span class="sxs-lookup"><span data-stu-id="60025-315">Select a range for the guessing game and the type of workflow to start, and click **New Game**.</span></span> <span data-ttu-id="60025-316">在 **推测** 框中输入推测，然后单击 " **开始** " 以提交推测。</span><span class="sxs-lookup"><span data-stu-id="60025-316">Enter a guess in the **Guess** box and click **Go** to submit your guess.</span></span> <span data-ttu-id="60025-317">请注意，`WriteLine` 活动的输出将显示在窗体上。</span><span class="sxs-lookup"><span data-stu-id="60025-317">Note that the output from the `WriteLine` activities is displayed on the form.</span></span>

8. <span data-ttu-id="60025-318">使用不同的工作流类型和编号范围启动多个工作流，输入一些推测，并通过从 " **工作流实例 Id** " 列表中进行选择来在工作流之间进行切换。</span><span class="sxs-lookup"><span data-stu-id="60025-318">Start several workflows using different workflow types and number ranges, enter some guesses, and switch between the workflows by selecting from the **Workflow Instance Id** list.</span></span>

    <span data-ttu-id="60025-319">请注意，当切换到新工作流时，状态窗口中不会显示以前的猜测值和工作流进度。</span><span class="sxs-lookup"><span data-stu-id="60025-319">Note that when you switch to a new workflow, the previous guesses and progress of the workflow are not displayed in the status window.</span></span> <span data-ttu-id="60025-320">状态不可用的原因是未将它捕获并保存在任何位置。</span><span class="sxs-lookup"><span data-stu-id="60025-320">The reason the status is not available is because it is not captured and saved anywhere.</span></span> <span data-ttu-id="60025-321">在本教程的后续步骤中， [如何：创建自定义跟踪参与者](how-to-create-a-custom-tracking-participant.md)，创建用于保存此信息的自定义跟踪参与者。</span><span class="sxs-lookup"><span data-stu-id="60025-321">In the next step of the tutorial, [How to: Create a Custom Tracking Participant](how-to-create-a-custom-tracking-participant.md), you create a custom tracking participant that saves this information.</span></span>
