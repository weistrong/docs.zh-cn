---
description: 了解详细信息：创建长时间运行的工作流服务
title: 创建长时间运行的工作流服务
ms.date: 03/30/2017
ms.assetid: 4c39bd04-5b8a-4562-a343-2c63c2821345
ms.openlocfilehash: 9d26e763e2515f9e9ec2b61201512f02eeaeb1bc
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99756898"
---
# <a name="create-a-long-running-workflow-service"></a><span data-ttu-id="940ab-103">创建长时间运行的工作流服务</span><span class="sxs-lookup"><span data-stu-id="940ab-103">Create a Long-running Workflow Service</span></span>

<span data-ttu-id="940ab-104">本主题描述如何创建长时间运行的工作流服务。</span><span class="sxs-lookup"><span data-stu-id="940ab-104">This topic describes how to create a long-running workflow service.</span></span> <span data-ttu-id="940ab-105">长时间运行的工作流服务可能会运行很长一段时间。</span><span class="sxs-lookup"><span data-stu-id="940ab-105">Long running workflow services may run for long periods of time.</span></span> <span data-ttu-id="940ab-106">在某一时刻，工作流可能会转入空闲状态，等待一些附加信息。</span><span class="sxs-lookup"><span data-stu-id="940ab-106">At some point the workflow may go idle waiting for some additional information.</span></span> <span data-ttu-id="940ab-107">当这种情况发生时，工作流将保存到 SQL 数据库并从内存中删除。</span><span class="sxs-lookup"><span data-stu-id="940ab-107">When this occurs the workflow is persisted to a SQL database and is removed from memory.</span></span> <span data-ttu-id="940ab-108">当附加信息变得可用时，工作流实例将重新加载回内存，继续执行。</span><span class="sxs-lookup"><span data-stu-id="940ab-108">When the additional information becomes available the workflow instance is loaded back into memory and continues executing.</span></span>  <span data-ttu-id="940ab-109">在此方案中，您将实现一个非常简化的订单系统。</span><span class="sxs-lookup"><span data-stu-id="940ab-109">In this scenario you are implementing a very simplified ordering system.</span></span>  <span data-ttu-id="940ab-110">客户端向工作流服务发送初始消息以启动订单。</span><span class="sxs-lookup"><span data-stu-id="940ab-110">The client sends an initial message to the workflow service to start the order.</span></span> <span data-ttu-id="940ab-111">此服务将订单 ID 返回给客户端。</span><span class="sxs-lookup"><span data-stu-id="940ab-111">It returns an order ID to the client.</span></span> <span data-ttu-id="940ab-112">此时，工作流服务要等待来自客户端的另一条消息，它转入空闲状态并保存到 SQL Server 数据库。</span><span class="sxs-lookup"><span data-stu-id="940ab-112">At this point the workflow service is waiting for another message from the client and goes into the idle state and is persisted to a SQL Server database.</span></span>  <span data-ttu-id="940ab-113">当客户端发送下一条消息订购项目时，工作流服务将重新加载回内存，完成处理此订单。</span><span class="sxs-lookup"><span data-stu-id="940ab-113">When the client sends the next message to order an item, the workflow service is loaded back into memory and finishes processing the order.</span></span> <span data-ttu-id="940ab-114">在代码示例中它将返回一个字符串，指示项目已添加到订单中。</span><span class="sxs-lookup"><span data-stu-id="940ab-114">In the code sample it returns a string stating the item has been added to the order.</span></span> <span data-ttu-id="940ab-115">代码示例并不是技术的现实应用，而是作为一个简单的示例来说明长时间运行的工作流服务。</span><span class="sxs-lookup"><span data-stu-id="940ab-115">The code sample is not meant to be a real world application of the technology, but rather a simple sample that illustrates long running workflow services.</span></span> <span data-ttu-id="940ab-116">本主题假定你知道如何创建 Visual Studio 2012 项目和解决方案。</span><span class="sxs-lookup"><span data-stu-id="940ab-116">This topic assumes you know how to create Visual Studio 2012 projects and solutions.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="940ab-117">先决条件</span><span class="sxs-lookup"><span data-stu-id="940ab-117">Prerequisites</span></span>

<span data-ttu-id="940ab-118">您必须安装了下列软件才能使用本演练：</span><span class="sxs-lookup"><span data-stu-id="940ab-118">You must have the following software installed to use this walkthrough:</span></span>

1. <span data-ttu-id="940ab-119">Microsoft SQL Server 2008</span><span class="sxs-lookup"><span data-stu-id="940ab-119">Microsoft SQL Server 2008</span></span>

2. <span data-ttu-id="940ab-120">Visual Studio 2012</span><span class="sxs-lookup"><span data-stu-id="940ab-120">Visual Studio 2012</span></span>

3. <span data-ttu-id="940ab-121">Microsoft [!INCLUDE[netfx_current_long](../../../../includes/netfx-current-long-md.md)]</span><span class="sxs-lookup"><span data-stu-id="940ab-121">Microsoft  [!INCLUDE[netfx_current_long](../../../../includes/netfx-current-long-md.md)]</span></span>

4. <span data-ttu-id="940ab-122">你熟悉 WCF 和 Visual Studio 2012，并且知道如何创建项目/解决方案。</span><span class="sxs-lookup"><span data-stu-id="940ab-122">You are familiar with WCF and Visual Studio 2012 and know how to create projects/solutions.</span></span>

## <a name="set-up-the-sql-database"></a><span data-ttu-id="940ab-123">设置 SQL 数据库</span><span class="sxs-lookup"><span data-stu-id="940ab-123">Set up the SQL Database</span></span>

1. <span data-ttu-id="940ab-124">为了使工作流服务实例能够持久化，您必须安装 Microsoft SQL Server，并配置一个数据库来存储持久化工作流实例。</span><span class="sxs-lookup"><span data-stu-id="940ab-124">In order for workflow service instances to be persisted you must have Microsoft SQL Server installed and you must configure a database to store the persisted workflow instances.</span></span> <span data-ttu-id="940ab-125">通过单击 " **开始** " 按钮，选择 " **所有程序**"、" **Microsoft SQL Server 2008**" 和 " **MICROSOFT sql Management Studio**" 来运行 microsoft sql Management Studio。</span><span class="sxs-lookup"><span data-stu-id="940ab-125">Run Microsoft SQL Management Studio by clicking the **Start** button, selecting **All Programs**, **Microsoft SQL Server 2008**, and **Microsoft SQL Management Studio**.</span></span>

2. <span data-ttu-id="940ab-126">单击 " **连接** " 按钮登录到 SQL Server 实例</span><span class="sxs-lookup"><span data-stu-id="940ab-126">Click the **Connect** button to log on to the SQL Server instance</span></span>

3. <span data-ttu-id="940ab-127">右键单击树视图中的 " **数据库** "，然后选择 " **新建数据库"。**</span><span class="sxs-lookup"><span data-stu-id="940ab-127">Right click **Databases** in the tree view and select **New Database..**</span></span> <span data-ttu-id="940ab-128">创建名为的新数据库 `SQLPersistenceStore` 。</span><span class="sxs-lookup"><span data-stu-id="940ab-128">to create a new database called `SQLPersistenceStore`.</span></span>

4. <span data-ttu-id="940ab-129">在 SQLPersistenceStore 数据库上运行位于 C:\Windows\Microsoft.NET\Framework\v4.0\SQL\en 目录中的 SqlWorkflowInstanceStoreSchema.sql 脚本文件，以设置所需的数据库架构。</span><span class="sxs-lookup"><span data-stu-id="940ab-129">Run the SqlWorkflowInstanceStoreSchema.sql script file located in the C:\Windows\Microsoft.NET\Framework\v4.0\SQL\en directory on the SQLPersistenceStore database to set up the needed database schemas.</span></span>

5. <span data-ttu-id="940ab-130">在 SQLPersistenceStore 数据库上运行位于 C:\Windows\Microsoft.NET\Framework\v4.0\SQL\en 目录中的 SqlWorkflowInstanceStoreLogic.sql 脚本文件，以设置所需的数据库逻辑。</span><span class="sxs-lookup"><span data-stu-id="940ab-130">Run the SqlWorkflowInstanceStoreLogic.sql script file located in the C:\Windows\Microsoft.NET\Framework\v4.0\SQL\en directory on the SQLPersistenceStore database to set up the needed database logic.</span></span>

## <a name="create-the-web-hosted-workflow-service"></a><span data-ttu-id="940ab-131">创建 Web 承载的工作流服务</span><span class="sxs-lookup"><span data-stu-id="940ab-131">Create the Web Hosted Workflow Service</span></span>

1. <span data-ttu-id="940ab-132">创建一个空的 Visual Studio 2012 解决方案，将其命名为 `OrderProcessing` 。</span><span class="sxs-lookup"><span data-stu-id="940ab-132">Create an empty Visual Studio 2012 solution, name it `OrderProcessing`.</span></span>

2. <span data-ttu-id="940ab-133">向该解决方案添加一个名为 `OrderService` 的新 WCF 工作流服务应用程序项目。</span><span class="sxs-lookup"><span data-stu-id="940ab-133">Add a new WCF Workflow Service Application project called `OrderService` to the solution.</span></span>

3. <span data-ttu-id="940ab-134">在 "项目属性" 对话框中，选择 " **Web** " 选项卡。</span><span class="sxs-lookup"><span data-stu-id="940ab-134">In the project properties dialog, select the **Web** tab.</span></span>

    1. <span data-ttu-id="940ab-135">在 " **启动操作** " 下，选择 " **特定页** " 并指定 `Service1.xamlx` 。</span><span class="sxs-lookup"><span data-stu-id="940ab-135">Under **Start Action** select **Specific Page** and specify `Service1.xamlx`.</span></span>

        <span data-ttu-id="940ab-136">![工作流服务项目 Web 属性](./media/creating-a-long-running-workflow-service/start-action-specific-page-option.png ""创建 web 承载的工作流服务特定页" 选项")</span><span class="sxs-lookup"><span data-stu-id="940ab-136">![Workflow Service Project Web Properties](./media/creating-a-long-running-workflow-service/start-action-specific-page-option.png "Create the web hosted workflow service - Specific Page option")</span></span>

    2. <span data-ttu-id="940ab-137">在 " **服务器** " 下选择 " **使用本地 IIS Web 服务器**"。</span><span class="sxs-lookup"><span data-stu-id="940ab-137">Under **Servers** select **Use Local IIS Web server**.</span></span>

        <span data-ttu-id="940ab-138">![本地 Web 服务器设置](./media/creating-a-long-running-workflow-service/use-local-web-server.png "创建 web 承载的工作流服务-使用本地 IIS Web 服务器选项")</span><span class="sxs-lookup"><span data-stu-id="940ab-138">![Local Web Server Settings](./media/creating-a-long-running-workflow-service/use-local-web-server.png "Create the web hosted workflow service - Use Local IIS Web Server option")</span></span>

        > [!WARNING]
        > <span data-ttu-id="940ab-139">若要进行此设置，必须在管理员模式下运行 Visual Studio 2012。</span><span class="sxs-lookup"><span data-stu-id="940ab-139">You must run Visual Studio 2012 in administrator mode to make this setting.</span></span>

        <span data-ttu-id="940ab-140">这两个步骤将工作流服务项目配置为由 IIS 承载。</span><span class="sxs-lookup"><span data-stu-id="940ab-140">These two steps configure the workflow service project to be hosted by IIS.</span></span>

4. <span data-ttu-id="940ab-141">`Service1.xamlx`如果尚未打开，请将其打开，并删除现有的 **ReceiveRequest** 和 **SendResponse** 活动。</span><span class="sxs-lookup"><span data-stu-id="940ab-141">Open `Service1.xamlx` if it is not open already and delete the existing **ReceiveRequest** and **SendResponse** activities.</span></span>

5. <span data-ttu-id="940ab-142">选择 " **顺序服务** " 活动，单击 " **变量** " 链接，并添加下图中显示的变量。</span><span class="sxs-lookup"><span data-stu-id="940ab-142">Select the **Sequential Service** activity and click the **Variables** link and add the variables shown in the following illustration.</span></span> <span data-ttu-id="940ab-143">通过执行此操作，会添加一些稍后将在工作流服务中使用的变量。</span><span class="sxs-lookup"><span data-stu-id="940ab-143">Doing this adds some variables that will be used later on in the workflow service.</span></span>

    > [!NOTE]
    > <span data-ttu-id="940ab-144">如果 CorrelationHandle 不在 "变量类型" 下拉下，请从下拉选择 " **浏览类型** "。</span><span class="sxs-lookup"><span data-stu-id="940ab-144">If CorrelationHandle is not in the Variable Type drop-down, select **Browse for types** from the drop-down.</span></span> <span data-ttu-id="940ab-145">在 " **类型名称** " 框中键入 CorrelationHandle，从列表框中选择 "CorrelationHandle"，然后单击 **"确定"**。</span><span class="sxs-lookup"><span data-stu-id="940ab-145">Type CorrelationHandle in the **Type name** box, select CorrelationHandle from the listbox and click **OK**.</span></span>

    <span data-ttu-id="940ab-146">![添加变量](./media/creating-a-long-running-workflow-service/add-variables-sequential-service-activity.gif "向顺序服务活动中添加变量。")</span><span class="sxs-lookup"><span data-stu-id="940ab-146">![Add Variables](./media/creating-a-long-running-workflow-service/add-variables-sequential-service-activity.gif "Add variables to the Sequential Service activity.")</span></span>

6. <span data-ttu-id="940ab-147">将 **ReceiveAndSendReply** 活动模板拖放到 **顺序服务** 活动中。</span><span class="sxs-lookup"><span data-stu-id="940ab-147">Drag and drop a **ReceiveAndSendReply** activity template into the **Sequential Service** activity.</span></span> <span data-ttu-id="940ab-148">这组活动将接收来自客户端的消息，并发送回复。</span><span class="sxs-lookup"><span data-stu-id="940ab-148">This set of activities will receive a message from a client and send a reply back.</span></span>

    1. <span data-ttu-id="940ab-149">选择 " **接收** " 活动，并设置下图中突出显示的属性。</span><span class="sxs-lookup"><span data-stu-id="940ab-149">Select the **Receive** activity and set the properties highlighted in the following illustration.</span></span>

        <span data-ttu-id="940ab-150">![设置 Receive 活动属性](./media/creating-a-long-running-workflow-service/set-receive-activity-properties.png "设置 "接收" 活动属性。")</span><span class="sxs-lookup"><span data-stu-id="940ab-150">![Set Receive Activity Properties](./media/creating-a-long-running-workflow-service/set-receive-activity-properties.png "Set the Receive activity properties.")</span></span>

        <span data-ttu-id="940ab-151">DisplayName 属性设置在设计器中显示的 Receive 活动的名称。</span><span class="sxs-lookup"><span data-stu-id="940ab-151">The DisplayName property sets the name displayed for the Receive activity in the designer.</span></span> <span data-ttu-id="940ab-152">ServiceContractName 和 OperationName 属性指定 Receive 活动实现的服务协定和操作的名称。</span><span class="sxs-lookup"><span data-stu-id="940ab-152">The ServiceContractName and OperationName properties specify the name of the service contract and operation that are implemented by the Receive activity.</span></span> <span data-ttu-id="940ab-153">有关如何在工作流服务中使用约定的详细信息，请参阅 [在工作流中使用约定](using-contracts-in-workflow.md)。</span><span class="sxs-lookup"><span data-stu-id="940ab-153">For more information about how contracts are used in Workflow services see [Using Contracts in Workflow](using-contracts-in-workflow.md).</span></span>

    2. <span data-ttu-id="940ab-154">单击 " **ReceiveStartOrder** " 活动中的 "**定义 ...** " 链接，并设置下图中显示的属性。</span><span class="sxs-lookup"><span data-stu-id="940ab-154">Click the **Define...** link in the **ReceiveStartOrder** activity and set the properties shown in the following illustration.</span></span>  <span data-ttu-id="940ab-155">请注意，" **参数** " 单选按钮已选中，名为的参数 `p_customerName` 绑定到 `customerName` 变量。</span><span class="sxs-lookup"><span data-stu-id="940ab-155">Notice that the **Parameters** radio button is selected, a parameter named `p_customerName` is bound to the `customerName` variable.</span></span> <span data-ttu-id="940ab-156">这会将 **receive** 活动配置为接收某些数据并将这些数据绑定到本地变量。</span><span class="sxs-lookup"><span data-stu-id="940ab-156">This configures the **Receive** activity to receive some data and bind that data to local variables.</span></span>

        <span data-ttu-id="940ab-157">![设置由 Receive 活动接收的数据](./media/creating-a-long-running-workflow-service/set-properties-for-receive-content.png "设置由 Receive 活动接收的数据的属性。")</span><span class="sxs-lookup"><span data-stu-id="940ab-157">![Setting the data received by the Receive activity](./media/creating-a-long-running-workflow-service/set-properties-for-receive-content.png "Set the properties for data received by the Receive activity.")</span></span>

    3. <span data-ttu-id="940ab-158">选择 **SendReplyToReceive** 活动，并设置下图中显示的突出显示的属性。</span><span class="sxs-lookup"><span data-stu-id="940ab-158">Select The **SendReplyToReceive** activity and set the highlighted property shown in the following illustration.</span></span>

        <span data-ttu-id="940ab-159">![设置 SendReply 活动的属性](./media/creating-a-long-running-workflow-service/set-properties-for-reply-activities.png "SetReplyProperties")</span><span class="sxs-lookup"><span data-stu-id="940ab-159">![Setting the properties of the SendReply activity](./media/creating-a-long-running-workflow-service/set-properties-for-reply-activities.png "SetReplyProperties")</span></span>

    4. <span data-ttu-id="940ab-160">单击 " **SendReplyToStartOrder** " 活动中的 "**定义 ...** " 链接，并设置下图中显示的属性。</span><span class="sxs-lookup"><span data-stu-id="940ab-160">Click the **Define...** link in the **SendReplyToStartOrder** activity and set the properties shown in the following illustration.</span></span> <span data-ttu-id="940ab-161">请注意，" **参数** " 单选按钮处于选中状态;名为的参数 `p_orderId` 绑定到 `orderId` 变量。</span><span class="sxs-lookup"><span data-stu-id="940ab-161">Notice that the **Parameters** radio button is selected; a parameter named `p_orderId` is bound to the `orderId` variable.</span></span> <span data-ttu-id="940ab-162">此设置指定 SendReplyToStartOrder 活动将类型字符串的值返回给调用方。</span><span class="sxs-lookup"><span data-stu-id="940ab-162">This setting specifies that the SendReplyToStartOrder activity will return a value of type string to the caller.</span></span>

        <span data-ttu-id="940ab-163">![配置 SendReply 活动内容数据](./media/creating-a-long-running-workflow-service/setreplycontent-for-sendreplytostartorder-activity.png "配置 SetReplyToStartOrder 活动的设置。")</span><span class="sxs-lookup"><span data-stu-id="940ab-163">![Configuring the SendReply activity content data](./media/creating-a-long-running-workflow-service/setreplycontent-for-sendreplytostartorder-activity.png "Configure setting for SetReplyToStartOrder activity.")</span></span>

    5. <span data-ttu-id="940ab-164">将 "Assign" 活动拖放到 " **Receive** " 和 " **SendReply** " 活动之间，并设置属性，如下图所示：</span><span class="sxs-lookup"><span data-stu-id="940ab-164">Drag and drop an Assign activity in between the **Receive** and **SendReply** activities and set the properties as shown in the following illustration:</span></span>

        <span data-ttu-id="940ab-165">![添加 Assign 活动](./media/creating-a-long-running-workflow-service/add-an-assign-activity.png "添加 "分配" 活动。")</span><span class="sxs-lookup"><span data-stu-id="940ab-165">![Adding an assign activity](./media/creating-a-long-running-workflow-service/add-an-assign-activity.png "Add an assign activity.")</span></span>

        <span data-ttu-id="940ab-166">这将创建一个新的订单 ID，并将该值放在 orderId 变量中。</span><span class="sxs-lookup"><span data-stu-id="940ab-166">This creates a new order ID and places the value in the orderId variable.</span></span>

    6. <span data-ttu-id="940ab-167">选择 " **ReplyToStartOrder** " 活动。</span><span class="sxs-lookup"><span data-stu-id="940ab-167">Select the **ReplyToStartOrder** activity.</span></span> <span data-ttu-id="940ab-168">在 "属性" 窗口中，单击 " **CorrelationInitializers**" 的省略号按钮。</span><span class="sxs-lookup"><span data-stu-id="940ab-168">In the properties window click the ellipsis button for **CorrelationInitializers**.</span></span> <span data-ttu-id="940ab-169">选择 " **添加初始值设定项** " 链接， `orderIdHandle` 在 "初始值设定项" 文本框中输入，为相关类型选择 "查询相关初始值设定项"，然后在 "XPATH 查询" 下拉框下选择 p_orderId。</span><span class="sxs-lookup"><span data-stu-id="940ab-169">Select the **Add initializer** link, enter `orderIdHandle` in the Initializer text box, select Query correlation initializer for the Correlation type, and select p_orderId under the XPATH Queries dropdown box.</span></span> <span data-ttu-id="940ab-170">这些设置如下图所示。</span><span class="sxs-lookup"><span data-stu-id="940ab-170">These settings are shown in the following illustration.</span></span> <span data-ttu-id="940ab-171">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="940ab-171">Click **OK**.</span></span>  <span data-ttu-id="940ab-172">这将初始化客户端与此工作流服务实例之间的相关性。</span><span class="sxs-lookup"><span data-stu-id="940ab-172">This initializes a correlation between the client and this instance of the workflow service.</span></span> <span data-ttu-id="940ab-173">当接收到包含此订单 ID 的消息时，将该消息路由至此工作流服务实例。</span><span class="sxs-lookup"><span data-stu-id="940ab-173">When a message containing this order ID is received it is routed to this instance of the workflow service.</span></span>

        <span data-ttu-id="940ab-174">![添加相关初始值设定项](./media/creating-a-long-running-workflow-service/add-correlationinitializers.png "添加相关初始值设定项。")</span><span class="sxs-lookup"><span data-stu-id="940ab-174">![Adding a correlation initializer](./media/creating-a-long-running-workflow-service/add-correlationinitializers.png "Add a correlation initializer.")</span></span>

7. <span data-ttu-id="940ab-175">将另一个 " **ReceiveAndSendReply** " 活动拖放到工作流的末尾 (包含) 的第一个 **接收** 和 **SendReply** 活动的 **序列** 外。</span><span class="sxs-lookup"><span data-stu-id="940ab-175">Drag and drop another **ReceiveAndSendReply** activity to the end of the workflow (outside the **Sequence** containing the first **Receive** and **SendReply** activities).</span></span> <span data-ttu-id="940ab-176">这将接收客户端发送的第二条消息，并对它做出响应。</span><span class="sxs-lookup"><span data-stu-id="940ab-176">This will receive the second message sent by the client and respond to it.</span></span>

    1. <span data-ttu-id="940ab-177">选择包含新添加的 **接收** 和 **SendReply** 活动的 **序列**，然后单击 "**变量**" 按钮。</span><span class="sxs-lookup"><span data-stu-id="940ab-177">Select the **Sequence** that contains the newly added **Receive** and **SendReply** activities and click the **Variables** button.</span></span> <span data-ttu-id="940ab-178">添加下图中突出显示的变量：</span><span class="sxs-lookup"><span data-stu-id="940ab-178">Add the variable highlighted in the following illustration:</span></span>

        <span data-ttu-id="940ab-179">![添加新变量](./media/creating-a-long-running-workflow-service/add-the-itemid-variable.png "添加 ItemId 变量。")</span><span class="sxs-lookup"><span data-stu-id="940ab-179">![Adding new variables](./media/creating-a-long-running-workflow-service/add-the-itemid-variable.png "Add the ItemId variable.")</span></span>

        <span data-ttu-id="940ab-180">还 `orderResult` 在范围内添加为 **字符串** `Sequence` 。</span><span class="sxs-lookup"><span data-stu-id="940ab-180">Also add `orderResult` as **String** in the `Sequence` scope.</span></span>

    2. <span data-ttu-id="940ab-181">选择 " **接收** " 活动，并设置下图中显示的属性：</span><span class="sxs-lookup"><span data-stu-id="940ab-181">Select the **Receive** activity and set the properties shown in the following illustration:</span></span>

        <span data-ttu-id="940ab-182">![设置接收活动属性](./media/creating-a-long-running-workflow-service/set-receive-activities-properties.png "设置 "接收活动" 属性。")</span><span class="sxs-lookup"><span data-stu-id="940ab-182">![Set the Receive activity properties](./media/creating-a-long-running-workflow-service/set-receive-activities-properties.png "Set the Receive activities properties.")</span></span>

        > [!NOTE]
        > <span data-ttu-id="940ab-183">别忘了用更改 **ServiceContractName** 字段 `../IAddItem` 。</span><span class="sxs-lookup"><span data-stu-id="940ab-183">Don't forget to change **ServiceContractName** field with `../IAddItem`.</span></span>

    3. <span data-ttu-id="940ab-184">单击 " **ReceiveAddItem** " 活动中的 "**定义 ...** " 链接，并添加下图中显示的参数：这将配置 receive 活动，以接受两个参数，即订单 ID 和所订购项的 id。</span><span class="sxs-lookup"><span data-stu-id="940ab-184">Click the **Define...** link in the **ReceiveAddItem** activity and add the parameters shown in the following illustration:This configures the receive activity to accept two parameters, the order ID and the ID of the item being ordered.</span></span>

        <span data-ttu-id="940ab-185">![为第二次接收指定参数](./media/creating-a-long-running-workflow-service/add-receive-two-parameters.png "配置 receive 活动以接收两个参数。")</span><span class="sxs-lookup"><span data-stu-id="940ab-185">![Specifying parameters for the second receive](./media/creating-a-long-running-workflow-service/add-receive-two-parameters.png "Configure the receive activity to receive two parameters.")</span></span>

    4. <span data-ttu-id="940ab-186">单击 " **CorrelateOn** " 省略号按钮，然后输入 `orderIdHandle` 。</span><span class="sxs-lookup"><span data-stu-id="940ab-186">Click the **CorrelateOn** ellipsis button and enter `orderIdHandle`.</span></span> <span data-ttu-id="940ab-187">在 " **XPath 查询**" 下，单击下拉箭头并选择 `p_orderId` 。</span><span class="sxs-lookup"><span data-stu-id="940ab-187">Under **XPath Queries**, click the drop down arrow and select `p_orderId`.</span></span> <span data-ttu-id="940ab-188">这将对第二个接收活动配置相关性。</span><span class="sxs-lookup"><span data-stu-id="940ab-188">This configures the correlation on the second receive activity.</span></span> <span data-ttu-id="940ab-189">有关关联的详细信息，请参阅 [关联](correlation.md)。</span><span class="sxs-lookup"><span data-stu-id="940ab-189">For more information about correlation see [Correlation](correlation.md).</span></span>

        <span data-ttu-id="940ab-190">![设置 CorrelatesOn 属性](./media/creating-a-long-running-workflow-service/correlateson-setting.png "设置 CorrelatesOn 属性。")</span><span class="sxs-lookup"><span data-stu-id="940ab-190">![Setting the CorrelatesOn property](./media/creating-a-long-running-workflow-service/correlateson-setting.png "Set the CorrelatesOn property.")</span></span>

    5. <span data-ttu-id="940ab-191">将一个 **If** 活动拖放到 **ReceiveAddItem** 活动后面。</span><span class="sxs-lookup"><span data-stu-id="940ab-191">Drag and drop an **If** activity immediately after the **ReceiveAddItem** activity.</span></span> <span data-ttu-id="940ab-192">此活动的行为与 if 语句类似。</span><span class="sxs-lookup"><span data-stu-id="940ab-192">This activity acts just like an if statement.</span></span>

        1. <span data-ttu-id="940ab-193">将 **Condition** 属性设置为 `itemId=="Zune HD" (itemId="Zune HD" for Visual Basic)`</span><span class="sxs-lookup"><span data-stu-id="940ab-193">Set the **Condition** property to `itemId=="Zune HD" (itemId="Zune HD" for Visual Basic)`</span></span>

        2. <span data-ttu-id="940ab-194">将 " **assign** " 活动拖放到 " **Then** " 部分，然后将另一个分配给 **Else** 节，按下图所示设置 " **分配** " 活动的属性。</span><span class="sxs-lookup"><span data-stu-id="940ab-194">Drag and drop an **Assign** activity in to the **Then** section and another into the **Else** section set the properties of the **Assign** activities as shown in the following illustration.</span></span>

            <span data-ttu-id="940ab-195">![分配服务调用的结果](./media/creating-a-long-running-workflow-service/assign-result-of-service-call.png "分配服务调用的结果。")</span><span class="sxs-lookup"><span data-stu-id="940ab-195">![Assigning the result of the service call](./media/creating-a-long-running-workflow-service/assign-result-of-service-call.png "Assign the result of the service call.")</span></span>

            <span data-ttu-id="940ab-196">如果条件为， `true` 则将执行 " **Then** " 部分。</span><span class="sxs-lookup"><span data-stu-id="940ab-196">If the condition is `true` the **Then** section will be executed.</span></span> <span data-ttu-id="940ab-197">如果条件为，则 `false` 执行 " **Else** " 部分。</span><span class="sxs-lookup"><span data-stu-id="940ab-197">If the condition is `false` the **Else** section is executed.</span></span>

        3. <span data-ttu-id="940ab-198">选择 **SendReplyToReceive** 活动，并设置下图中显示的 **DisplayName** 属性。</span><span class="sxs-lookup"><span data-stu-id="940ab-198">Select the **SendReplyToReceive** activity and set the **DisplayName** property shown in the following illustration.</span></span>

            <span data-ttu-id="940ab-199">![设置 SendReply 活动属性](./media/creating-a-long-running-workflow-service/send-reply-activity-property.png "设置 SendReply 活动属性。")</span><span class="sxs-lookup"><span data-stu-id="940ab-199">![Setting the SendReply activity properties](./media/creating-a-long-running-workflow-service/send-reply-activity-property.png "Set the SendReply activity property.")</span></span>

        4. <span data-ttu-id="940ab-200">单击 " **SetReplyToAddItem** " 活动中的 "**定义 ...** " 链接，并对其进行配置，如下图所示。</span><span class="sxs-lookup"><span data-stu-id="940ab-200">Click the **Define ...** link in the **SetReplyToAddItem** activity and configure it as shown in the following illustration.</span></span> <span data-ttu-id="940ab-201">这会将 **SendReplyToAddItem** 活动配置为返回变量中的值 `orderResult` 。</span><span class="sxs-lookup"><span data-stu-id="940ab-201">This configures the **SendReplyToAddItem** activity to return the value in the `orderResult` variable.</span></span>

            <span data-ttu-id="940ab-202">![设置 SendReply 活动的数据绑定](./media/creating-a-long-running-workflow-service/set-property-for-sendreplytoadditem.gif "设置 SendReplyToAddItem 活动的属性。")</span><span class="sxs-lookup"><span data-stu-id="940ab-202">![Setting the data binding for the SendReply activity](./media/creating-a-long-running-workflow-service/set-property-for-sendreplytoadditem.gif "Set property for SendReplyToAddItem activity.")</span></span>

8. <span data-ttu-id="940ab-203">打开 web.config 文件，并在部分中添加以下元素， \<behavior> 以启用工作流持久性。</span><span class="sxs-lookup"><span data-stu-id="940ab-203">Open the web.config file and add the following elements in the \<behavior> section to enable workflow persistence.</span></span>

    ```xml
    <sqlWorkflowInstanceStore connectionString="Data Source=your-machine\SQLExpress;Initial Catalog=SQLPersistenceStore;Integrated Security=True;Asynchronous Processing=True" instanceEncodingOption="None" instanceCompletionAction="DeleteAll" instanceLockedExceptionAction="BasicRetry" hostLockRenewalPeriod="00:00:30" runnableInstancesDetectionPeriod="00:00:02" />
              <workflowIdle timeToUnload="0"/>
    ```

    > [!WARNING]
    > <span data-ttu-id="940ab-204">确保替换上面代码段中的主机和 SQL Server 实例名称。</span><span class="sxs-lookup"><span data-stu-id="940ab-204">Make sure to replace your host and SQL server instance name in the previous code snippet.</span></span>

9. <span data-ttu-id="940ab-205">生成解决方案。</span><span class="sxs-lookup"><span data-stu-id="940ab-205">Build the solution.</span></span>

## <a name="create-a-client-application-to-call-the-workflow-service"></a><span data-ttu-id="940ab-206">创建用于调用工作流服务的客户端应用程序</span><span class="sxs-lookup"><span data-stu-id="940ab-206">Create a Client Application to Call the Workflow Service</span></span>

1. <span data-ttu-id="940ab-207">将一个名为 `OrderClient` 的新控制台应用程序项目添加到解决方案中。</span><span class="sxs-lookup"><span data-stu-id="940ab-207">Add a new Console application project called `OrderClient` to the solution.</span></span>

2. <span data-ttu-id="940ab-208">向 `OrderClient` 项目中添加对以下程序集的引用：</span><span class="sxs-lookup"><span data-stu-id="940ab-208">Add references to the following assemblies to the `OrderClient` project</span></span>

    1. <span data-ttu-id="940ab-209">System.ServiceModel.dll</span><span class="sxs-lookup"><span data-stu-id="940ab-209">System.ServiceModel.dll</span></span>

    2. <span data-ttu-id="940ab-210">System.ServiceModel.Activities.dll</span><span class="sxs-lookup"><span data-stu-id="940ab-210">System.ServiceModel.Activities.dll</span></span>

3. <span data-ttu-id="940ab-211">添加对工作流服务的服务引用，并将 `OrderService` 指定为命名空间。</span><span class="sxs-lookup"><span data-stu-id="940ab-211">Add a service reference to the workflow service and specify `OrderService` as the namespace.</span></span>

4. <span data-ttu-id="940ab-212">在客户端项目的 `Main()` 方法中，添加以下代码：</span><span class="sxs-lookup"><span data-stu-id="940ab-212">In the `Main()` method of the client project add the following code:</span></span>

    ```csharp
    static void Main(string[] args)
    {
       // Send initial message to start the workflow service
       Console.WriteLine("Sending start message");
       StartOrderClient startProxy = new StartOrderClient();
       string orderId = startProxy.StartOrder("Kim Abercrombie");

       // The workflow service is now waiting for the second message to be sent
       Console.WriteLine("Workflow service is idle...");
       Console.WriteLine("Press [ENTER] to send an add item message to reactivate the workflow service...");
       Console.ReadLine();

       // Send the second message
       Console.WriteLine("Sending add item message");
       AddItemClient addProxy = new AddItemClient();
       AddItem item = new AddItem();
       item.p_itemId = "Zune HD";
       item.p_orderId = orderId;

       string orderResult = addProxy.AddItem(item);
       Console.WriteLine("Service returned: " + orderResult);
    }
    ```

5. <span data-ttu-id="940ab-213">生成解决方案，并运行 `OrderClient` 应用程序。</span><span class="sxs-lookup"><span data-stu-id="940ab-213">Build the solution and run the `OrderClient` application.</span></span> <span data-ttu-id="940ab-214">客户端将显示以下文本：</span><span class="sxs-lookup"><span data-stu-id="940ab-214">The client will display the following text:</span></span>

    ```output
    Sending start messageWorkflow service is idle...Press [ENTER] to send an add item message to reactivate the workflow service...
    ```

6. <span data-ttu-id="940ab-215">若要验证工作流服务是否已持久化，请转到 " **开始** " 菜单，选择 " **所有程序**"， **Microsoft SQL Server 2008**， **SQL Server Management Studio**，开始 SQL Server Management Studio。</span><span class="sxs-lookup"><span data-stu-id="940ab-215">To verify that the workflow service has been persisted, start the SQL Server Management Studio by going to the **Start** menu, Selecting **All Programs**, **Microsoft SQL Server 2008**, **SQL Server Management Studio**.</span></span>

    1. <span data-ttu-id="940ab-216">在左侧窗格中，依次展开 **"数据库**"、"数据库"、" **SQLPersistenceStore**"、" **视图** " 和 " **DurableInstancing** "，然后选择 " **选择前1000行**"。</span><span class="sxs-lookup"><span data-stu-id="940ab-216">In the left hand pane expand, **Databases**, **SQLPersistenceStore**, **Views** and right click **System.Activities.DurableInstancing.Instances** and select **Select Top 1000 Rows**.</span></span> <span data-ttu-id="940ab-217">在 **结果** 窗格中，验证是否已列出至少一个实例。</span><span class="sxs-lookup"><span data-stu-id="940ab-217">In the **Results** pane verify you see at least one instance listed.</span></span> <span data-ttu-id="940ab-218">如果运行时出现异常，则可能存在先前运行的其他实例。</span><span class="sxs-lookup"><span data-stu-id="940ab-218">There may be other instances from prior runs if an exception occurred while running.</span></span> <span data-ttu-id="940ab-219">您可以通过右键单击 " **DurableInstancing** "，然后选择 " **编辑前200行**"，再按 " **执行** " 按钮，选择结果窗格中的所有行，然后选择 " **删除**" 来删除现有行。</span><span class="sxs-lookup"><span data-stu-id="940ab-219">You can delete existing rows by right clicking **System.Activities.DurableInstancing.Instances** and selecting **Edit Top 200 rows**, pressing the **Execute** button, selecting all rows in the results pane and selecting **delete**.</span></span>  <span data-ttu-id="940ab-220">若要验证数据库中显示的实例是否为应用程序创建的实例，请在运行客户端之前验证实例视图是否为空。</span><span class="sxs-lookup"><span data-stu-id="940ab-220">To verify the instance displayed in the database is the instance your application created, verify the instances view is empty prior to running the client.</span></span> <span data-ttu-id="940ab-221">客户端开始运行后，重新运行查询（选择前 1000 行），并确认已添加新实例。</span><span class="sxs-lookup"><span data-stu-id="940ab-221">Once the client is running re-run the query (Select Top 1000 Rows) and verify a new instance has been added.</span></span>

7. <span data-ttu-id="940ab-222">按 Enter 将添加项目消息发送至工作流服务。</span><span class="sxs-lookup"><span data-stu-id="940ab-222">Press enter to send the add item message to the workflow service.</span></span> <span data-ttu-id="940ab-223">客户端将显示以下文本：</span><span class="sxs-lookup"><span data-stu-id="940ab-223">The client will display the following text:</span></span>

    ```output
    Sending add item messageService returned: Item added to orderPress any key to continue . . .
    ```

## <a name="see-also"></a><span data-ttu-id="940ab-224">请参阅</span><span class="sxs-lookup"><span data-stu-id="940ab-224">See also</span></span>

- [<span data-ttu-id="940ab-225">工作流服务</span><span class="sxs-lookup"><span data-stu-id="940ab-225">Workflow Services</span></span>](workflow-services.md)
