---
description: 了解详细信息：挂起的实例管理
title: 挂起的实例管理
ms.date: 03/30/2017
ms.assetid: f5ca3faa-ba1f-4857-b92c-d927e4b29598
ms.openlocfilehash: d68dd8b61b6e0e7a618cf05f1df07e58ab75e27f
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99741713"
---
# <a name="suspended-instance-management"></a><span data-ttu-id="3f316-103">挂起的实例管理</span><span class="sxs-lookup"><span data-stu-id="3f316-103">Suspended Instance Management</span></span>

<span data-ttu-id="3f316-104">此示例演示如何管理已挂起的工作流实例。</span><span class="sxs-lookup"><span data-stu-id="3f316-104">This sample demonstrates how to manage workflow instances that have been suspended.</span></span>  <span data-ttu-id="3f316-105"><xref:System.ServiceModel.Activities.Description.WorkflowUnhandledExceptionBehavior> 的默认操作为 `AbandonAndSuspend`。</span><span class="sxs-lookup"><span data-stu-id="3f316-105">The default action for <xref:System.ServiceModel.Activities.Description.WorkflowUnhandledExceptionBehavior> is `AbandonAndSuspend`.</span></span> <span data-ttu-id="3f316-106">这意味着，在默认情况下，从 <xref:System.ServiceModel.WorkflowServiceHost> 中承载的某个工作流实例抛出的未处理异常会导致从内存中释放（放弃）该实例，而该实例的持久版本将被标记为已挂起。</span><span class="sxs-lookup"><span data-stu-id="3f316-106">This means that by default, unhandled exceptions thrown from a workflow instance hosted in the <xref:System.ServiceModel.WorkflowServiceHost> will cause the instance to be disposed from memory (abandoned) and the durable/persisted version of the instance to be marked as suspended.</span></span> <span data-ttu-id="3f316-107">已挂起的工作流实例在取消挂起之前无法运行。</span><span class="sxs-lookup"><span data-stu-id="3f316-107">A suspended workflow instance will not be able to run until it has been unsuspended.</span></span>

 <span data-ttu-id="3f316-108">此示例演示如何实现用于查询已挂起实例的命令行实用工具，以及如何为用户提供恢复或终止实例的选项。</span><span class="sxs-lookup"><span data-stu-id="3f316-108">The sample shows how a command-line utility can be implemented to query for suspended instances, and how to give the user the option to resume or terminate the instance.</span></span> <span data-ttu-id="3f316-109">在此示例中，一个工作流服务有意引发异常，从而使该服务挂起。</span><span class="sxs-lookup"><span data-stu-id="3f316-109">In this sample, a workflow service intentionally throws an exception, causing it to become suspended.</span></span> <span data-ttu-id="3f316-110">然后可以使用命令行实用工具查询该实例，并随后恢复或终止该实例。</span><span class="sxs-lookup"><span data-stu-id="3f316-110">The command-line utility can then be used to query for the instance and subsequently resume or terminate the instance.</span></span>

## <a name="demonstrates"></a><span data-ttu-id="3f316-111">演示</span><span class="sxs-lookup"><span data-stu-id="3f316-111">Demonstrates</span></span>

 <span data-ttu-id="3f316-112"><xref:System.ServiceModel.WorkflowServiceHost><xref:System.ServiceModel.Activities.Description.WorkflowUnhandledExceptionBehavior> <xref:System.ServiceModel.Activities.WorkflowControlEndpoint> 在 WINDOWS WORKFLOW FOUNDATION (WF) 中。</span><span class="sxs-lookup"><span data-stu-id="3f316-112"><xref:System.ServiceModel.WorkflowServiceHost> with <xref:System.ServiceModel.Activities.Description.WorkflowUnhandledExceptionBehavior> and <xref:System.ServiceModel.Activities.WorkflowControlEndpoint> in Windows Workflow Foundation (WF).</span></span>

## <a name="discussion"></a><span data-ttu-id="3f316-113">讨论 (Discussion)</span><span class="sxs-lookup"><span data-stu-id="3f316-113">Discussion</span></span>

 <span data-ttu-id="3f316-114">本示例中实现的命令行实用工具特定于 [!INCLUDE[netfx_current_long](../../../../includes/netfx-current-long-md.md)] 中附带的 SQL 实例存储区实现。</span><span class="sxs-lookup"><span data-stu-id="3f316-114">The command-line utility implemented in this sample is specific to the SQL instance store implementation that ships in [!INCLUDE[netfx_current_long](../../../../includes/netfx-current-long-md.md)].</span></span> <span data-ttu-id="3f316-115">如果您具有该实例存储区的自定义实现，则可以使用特定于您实例存储区的实现替换示例中的 `WorkflowInstanceCommand` 实现，来改编此实用工具。</span><span class="sxs-lookup"><span data-stu-id="3f316-115">If you have a custom implementation of the instance store, then you can adapt this utility by replacing the `WorkflowInstanceCommand` implementations in the sample with implementations that are specific to your instance store.</span></span>

 <span data-ttu-id="3f316-116">所提供的实现直接针对 SQL 实例存储区来运行 SQL 命令以列出挂起的实例，并依赖于添加到 <xref:System.ServiceModel.Activities.WorkflowControlEndpoint> 的 <xref:System.ServiceModel.WorkflowServiceHost>，以便恢复或终止实例。</span><span class="sxs-lookup"><span data-stu-id="3f316-116">The provided implementation runs SQL commands against the SQL instance store directly to list suspended instances, and it relies on a <xref:System.ServiceModel.Activities.WorkflowControlEndpoint> added to the <xref:System.ServiceModel.WorkflowServiceHost> in order to resume or terminate the instances.</span></span>

#### <a name="to-set-up-build-and-run-the-sample"></a><span data-ttu-id="3f316-117">设置、生成和运行示例</span><span class="sxs-lookup"><span data-stu-id="3f316-117">To set up, build, and run the sample</span></span>

1. <span data-ttu-id="3f316-118">此示例要求启用以下 Windows 组件：</span><span class="sxs-lookup"><span data-stu-id="3f316-118">This sample requires that the following Windows components are enabled:</span></span>

    1. <span data-ttu-id="3f316-119">Microsoft Message Queues (MSMQ) Server</span><span class="sxs-lookup"><span data-stu-id="3f316-119">Microsoft Message Queues (MSMQ) Server</span></span>

    2. <span data-ttu-id="3f316-120">SQL Server Express</span><span class="sxs-lookup"><span data-stu-id="3f316-120">SQL Server Express</span></span>

2. <span data-ttu-id="3f316-121">设置 SQL Server 数据库。</span><span class="sxs-lookup"><span data-stu-id="3f316-121">Set up the SQL Server database.</span></span>

    1. <span data-ttu-id="3f316-122">在 Visual Studio 2010 命令提示符下，运行 SuspendedInstanceManagement 示例目录中的 "setup .cmd"，此操作执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="3f316-122">From a Visual Studio 2010 command prompt, run "setup.cmd" from the SuspendedInstanceManagement sample directory, which does the following:</span></span>

        1. <span data-ttu-id="3f316-123">使用 SQL Server Express 创建持久性数据库。</span><span class="sxs-lookup"><span data-stu-id="3f316-123">Creates a persistence database using SQL Server Express.</span></span> <span data-ttu-id="3f316-124">如果持久性数据库已存在，则删除该数据库并重新创建一个</span><span class="sxs-lookup"><span data-stu-id="3f316-124">If the persistence database already exists, then it is dropped and re-created</span></span>

        2. <span data-ttu-id="3f316-125">设置持久性数据库。</span><span class="sxs-lookup"><span data-stu-id="3f316-125">Sets up the database for persistence.</span></span>

        3. <span data-ttu-id="3f316-126">将 IIS APPPOOL\DefaultAppPool 和 NT AUTHORITY\Network Service 添加到设置持久性数据库时定义的 InstanceStoreUsers 角色。</span><span class="sxs-lookup"><span data-stu-id="3f316-126">Adds IIS APPPOOL\DefaultAppPool and NT AUTHORITY\Network Service to the InstanceStoreUsers role that was defined when setting up the database for persistence.</span></span>

3. <span data-ttu-id="3f316-127">设置服务队列。</span><span class="sxs-lookup"><span data-stu-id="3f316-127">Set up the service queue.</span></span>

    1. <span data-ttu-id="3f316-128">在 Visual Studio 2010 中，右键单击 **SampleWorkflowApp** 项目，然后单击 " **设为启动项目**"。</span><span class="sxs-lookup"><span data-stu-id="3f316-128">In Visual Studio 2010, right-click the **SampleWorkflowApp** project and click **Set as Startup Project**.</span></span>

    2. <span data-ttu-id="3f316-129">按 **F5** 编译并运行 SampleWorkflowApp。</span><span class="sxs-lookup"><span data-stu-id="3f316-129">Compile and run the SampleWorkflowApp by pressing **F5**.</span></span> <span data-ttu-id="3f316-130">这将创建所需队列。</span><span class="sxs-lookup"><span data-stu-id="3f316-130">This will create the required queue.</span></span>

    3. <span data-ttu-id="3f316-131">按 **enter** 停止 SampleWorkflowApp。</span><span class="sxs-lookup"><span data-stu-id="3f316-131">Press **Enter** to stop the SampleWorkflowApp.</span></span>

    4. <span data-ttu-id="3f316-132">通过在命令提示符下运行 Compmgmt.msc 来打开计算机管理控制台。</span><span class="sxs-lookup"><span data-stu-id="3f316-132">Open the Computer Management console by running Compmgmt.msc from a command prompt.</span></span>

    5. <span data-ttu-id="3f316-133">展开 " **服务和应用程序**"、" **消息队列**" 和 " **专用队列**"。</span><span class="sxs-lookup"><span data-stu-id="3f316-133">Expand **Service and Applications**, **Message Queuing**, **Private Queues**.</span></span>

    6. <span data-ttu-id="3f316-134">右键单击 " **ReceiveTx** " 队列，然后选择 " **属性**"。</span><span class="sxs-lookup"><span data-stu-id="3f316-134">Right click the **ReceiveTx** queue and select **Properties**.</span></span>

    7. <span data-ttu-id="3f316-135">选择 " **安全** " 选项卡，"允许 **每个人** " 具有 **接收消息**、 **扫视消息** 和 **发送消息** 的权限。</span><span class="sxs-lookup"><span data-stu-id="3f316-135">Select the **Security** tab and allow **Everyone** to have permissions to **Receive Message**, **Peek Message**, and **Send Message**.</span></span>

4. <span data-ttu-id="3f316-136">现在运行示例。</span><span class="sxs-lookup"><span data-stu-id="3f316-136">Now, run the sample.</span></span>

    1. <span data-ttu-id="3f316-137">在 Visual Studio 2010 中，按 **Ctrl + F5** 再次运行 SampleWorkflowApp 项目而不进行调试。</span><span class="sxs-lookup"><span data-stu-id="3f316-137">In Visual Studio 2010, run the SampleWorkflowApp project again without debugging by pressing **Ctrl+F5**.</span></span> <span data-ttu-id="3f316-138">将在控制台窗口中输出两个终结点地址：一个用于应用程序终结点，另一个来自 <xref:System.ServiceModel.Activities.WorkflowControlEndpoint>。</span><span class="sxs-lookup"><span data-stu-id="3f316-138">Two endpoint addresses will be printed in the console window: one for the application endpoint and then other from the <xref:System.ServiceModel.Activities.WorkflowControlEndpoint>.</span></span> <span data-ttu-id="3f316-139">随后会创建一个工作流实例，该实例的跟踪记录会出现在控制台窗口中。</span><span class="sxs-lookup"><span data-stu-id="3f316-139">A workflow instance is then created, and tracking records for that instance will appear in the console window.</span></span> <span data-ttu-id="3f316-140">该工作流实例会引发异常，从而导致该实例挂起或中止。</span><span class="sxs-lookup"><span data-stu-id="3f316-140">The workflow instance will throw an exception causing the instance to be suspended and aborted.</span></span>

    2. <span data-ttu-id="3f316-141">随后可以使用命令行实用工具对这些实例中的任何一个进行进一步操作。</span><span class="sxs-lookup"><span data-stu-id="3f316-141">The command-line utility can then be used to take further action on any of these instances.</span></span> <span data-ttu-id="3f316-142">命令行参数的语法如下：</span><span class="sxs-lookup"><span data-stu-id="3f316-142">The syntax for command line arguments is as follows::</span></span>

         `SuspendedInstanceManagement -Command:[CommandName] -Server:[ServerName] -Database:[DatabaseName] -InstanceId:[InstanceId]`

         <span data-ttu-id="3f316-143">支持的命令为：`Query`、`Resume` 和 `Terminate`。</span><span class="sxs-lookup"><span data-stu-id="3f316-143">The supported commands are: `Query`, `Resume`, and `Terminate`.</span></span>  <span data-ttu-id="3f316-144">只有 `Resume` 和 `Terminate` 才需要 InstanceId 开关。</span><span class="sxs-lookup"><span data-stu-id="3f316-144">The InstanceId switch is only required for `Resume` and `Terminate` operations.</span></span>

#### <a name="to-cleanup-optional"></a><span data-ttu-id="3f316-145">清理（可选）</span><span class="sxs-lookup"><span data-stu-id="3f316-145">To cleanup (Optional)</span></span>

1. <span data-ttu-id="3f316-146">通过在 `vs2010` 命令提示符下运行 Compmgmt.msc 来打开计算机管理控制台。</span><span class="sxs-lookup"><span data-stu-id="3f316-146">Open the Computer Management console by running Compmgmt.msc from a `vs2010` command prompt.</span></span>

2. <span data-ttu-id="3f316-147">展开 " **服务和应用程序**"、" **消息队列**" 和 " **专用队列**"。</span><span class="sxs-lookup"><span data-stu-id="3f316-147">Expand **Service and Applications**, **Message Queuing**, **Private Queues**.</span></span>

3. <span data-ttu-id="3f316-148">删除 **ReceiveTx** 队列。</span><span class="sxs-lookup"><span data-stu-id="3f316-148">Delete the **ReceiveTx** queue.</span></span>

4. <span data-ttu-id="3f316-149">若要删除持久性数据库，请运行 cleanup.cmd。</span><span class="sxs-lookup"><span data-stu-id="3f316-149">To remove the persistence database, run cleanup.cmd.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3f316-150">您的计算机上可能已安装这些示例。</span><span class="sxs-lookup"><span data-stu-id="3f316-150">The samples may already be installed on your machine.</span></span> <span data-ttu-id="3f316-151">在继续操作之前，请先检查以下（默认）目录：</span><span class="sxs-lookup"><span data-stu-id="3f316-151">Check for the following (default) directory before continuing.</span></span>  
>
> `<InstallDrive>:\WF_WCF_Samples`  
>
> <span data-ttu-id="3f316-152">如果此目录不存在，请参阅[Windows Communication Foundation (wcf) ，并 Windows Workflow Foundation (的 WF](https://www.microsoft.com/download/details.aspx?id=21459)) .NET Framework Windows Communication Foundation ([!INCLUDE[wf1](../../../../includes/wf1-md.md)]</span><span class="sxs-lookup"><span data-stu-id="3f316-152">If this directory does not exist, go to [Windows Communication Foundation (WCF) and Windows Workflow Foundation (WF) Samples for .NET Framework 4](https://www.microsoft.com/download/details.aspx?id=21459) to download all Windows Communication Foundation (WCF) and [!INCLUDE[wf1](../../../../includes/wf1-md.md)] samples.</span></span> <span data-ttu-id="3f316-153">此示例位于以下目录：</span><span class="sxs-lookup"><span data-stu-id="3f316-153">This sample is located in the following directory.</span></span>  
>
> `<InstallDrive>:\WF_WCF_Samples\WF\Application\SuspendedInstanceManagement`
