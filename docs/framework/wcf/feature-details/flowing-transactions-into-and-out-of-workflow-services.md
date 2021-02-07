---
description: 了解详细信息：将事务流入和流出工作流服务
title: 使事务流入和流出工作流服务
ms.date: 03/30/2017
ms.assetid: 03ced70e-b540-4dd9-86c8-87f7bd61f609
ms.openlocfilehash: f39740c45dd70fbc06963b8e842f9a01a0393f7e
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99704961"
---
# <a name="flowing-transactions-into-and-out-of-workflow-services"></a><span data-ttu-id="c2948-103">使事务流入和流出工作流服务</span><span class="sxs-lookup"><span data-stu-id="c2948-103">Flowing Transactions into and out of Workflow Services</span></span>

<span data-ttu-id="c2948-104">工作流服务和客户端可以参与事务。</span><span class="sxs-lookup"><span data-stu-id="c2948-104">Workflow services and clients can participate in transactions.</span></span>  <span data-ttu-id="c2948-105">对于将成为环境事务一部分的服务操作，将 <xref:System.ServiceModel.Activities.Receive> 活动放到 <xref:System.ServiceModel.Activities.TransactedReceiveScope> 活动内。</span><span class="sxs-lookup"><span data-stu-id="c2948-105">For a service operation to become part of an ambient transaction, place a <xref:System.ServiceModel.Activities.Receive> activity within a <xref:System.ServiceModel.Activities.TransactedReceiveScope> activity.</span></span> <span data-ttu-id="c2948-106">由 <xref:System.ServiceModel.Activities.Send> 内的 <xref:System.ServiceModel.Activities.SendReply> 或 <xref:System.ServiceModel.Activities.TransactedReceiveScope> 活动所做的任何调用也将在环境事务中进行。</span><span class="sxs-lookup"><span data-stu-id="c2948-106">Any calls made by a <xref:System.ServiceModel.Activities.Send> or a <xref:System.ServiceModel.Activities.SendReply> activity within the <xref:System.ServiceModel.Activities.TransactedReceiveScope> will also be made within the ambient transaction.</span></span> <span data-ttu-id="c2948-107">工作流客户端应用程序可以通过使用 <xref:System.Activities.Statements.TransactionScope> 活动来创建环境事务，并通过使用该环境事务来调用服务操作。</span><span class="sxs-lookup"><span data-stu-id="c2948-107">A workflow client application can create an ambient transaction by using the <xref:System.Activities.Statements.TransactionScope> activity and call service operations using the ambient transaction.</span></span> <span data-ttu-id="c2948-108">本主题将指导您创建参与事务的工作流服务和工作流客户端。</span><span class="sxs-lookup"><span data-stu-id="c2948-108">This topic walks you through creating a workflow service and workflow client that participate in transactions.</span></span>  
  
> [!WARNING]
> <span data-ttu-id="c2948-109">如果在事务内加载工作流服务实例，且工作流包含 <xref:System.Activities.Statements.Persist> 活动，则工作流实例将被阻止，直到事务超时。</span><span class="sxs-lookup"><span data-stu-id="c2948-109">If a workflow service instance is loaded within a transaction and the workflow contains a <xref:System.Activities.Statements.Persist> activity, the workflow instance will block until the transaction times out.</span></span>  
  
> [!IMPORTANT]
> <span data-ttu-id="c2948-110">无论何时使用 <xref:System.ServiceModel.Activities.TransactedReceiveScope>，都建议将所有接收都置于工作流内的 <xref:System.ServiceModel.Activities.TransactedReceiveScope> 活动中。</span><span class="sxs-lookup"><span data-stu-id="c2948-110">Whenever you use a <xref:System.ServiceModel.Activities.TransactedReceiveScope> it is recommended to place all Receives in the workflow within <xref:System.ServiceModel.Activities.TransactedReceiveScope> activities.</span></span>  
  
> [!IMPORTANT]
> <span data-ttu-id="c2948-111">如果 <xref:System.ServiceModel.Activities.TransactedReceiveScope> 且消息按错误顺序到达，则在尝试提交第一个不按顺序的消息时，工作流会中止。</span><span class="sxs-lookup"><span data-stu-id="c2948-111">When using <xref:System.ServiceModel.Activities.TransactedReceiveScope> and messages arrive in the incorrect order, the workflow will be aborted when trying to deliver the first out of order message.</span></span> <span data-ttu-id="c2948-112">必须确保工作流在空闲时始终处于一致的停止点。</span><span class="sxs-lookup"><span data-stu-id="c2948-112">You must make sure your workflow is always at a consistent stopping point when the workflow idles.</span></span> <span data-ttu-id="c2948-113">这会使您可以在工作流中止时，从以前的持久点重新启动工作流。</span><span class="sxs-lookup"><span data-stu-id="c2948-113">This will allow you to restart the workflow from a previous persistence point should the workflow be aborted.</span></span>  
  
### <a name="create-a-shared-library"></a><span data-ttu-id="c2948-114">创建共享库</span><span class="sxs-lookup"><span data-stu-id="c2948-114">Create a shared library</span></span>  
  
1. <span data-ttu-id="c2948-115">创建新的空 Visual Studio 解决方案。</span><span class="sxs-lookup"><span data-stu-id="c2948-115">Create a new empty Visual Studio Solution.</span></span>  
  
2. <span data-ttu-id="c2948-116">添加一个名为 `Common` 的新类库项目。</span><span class="sxs-lookup"><span data-stu-id="c2948-116">Add a new class library project called `Common`.</span></span> <span data-ttu-id="c2948-117">添加对下列程序集的引用：</span><span class="sxs-lookup"><span data-stu-id="c2948-117">Add references to the following assemblies:</span></span>  
  
    - <span data-ttu-id="c2948-118">System.Activities.dll</span><span class="sxs-lookup"><span data-stu-id="c2948-118">System.Activities.dll</span></span>  
  
    - <span data-ttu-id="c2948-119">System.ServiceModel.dll</span><span class="sxs-lookup"><span data-stu-id="c2948-119">System.ServiceModel.dll</span></span>  
  
    - <span data-ttu-id="c2948-120">System.ServiceModel.Activities.dll</span><span class="sxs-lookup"><span data-stu-id="c2948-120">System.ServiceModel.Activities.dll</span></span>  
  
    - <span data-ttu-id="c2948-121">System.Transactions.dll</span><span class="sxs-lookup"><span data-stu-id="c2948-121">System.Transactions.dll</span></span>  
  
3. <span data-ttu-id="c2948-122">将一个名为 `PrintTransactionInfo` 的新类添加到 `Common` 项目。</span><span class="sxs-lookup"><span data-stu-id="c2948-122">Add a new class called `PrintTransactionInfo` to the `Common` project.</span></span> <span data-ttu-id="c2948-123">此类派生自 <xref:System.Activities.NativeActivity>，并重载 <xref:System.Activities.NativeActivity.Execute%2A> 方法。</span><span class="sxs-lookup"><span data-stu-id="c2948-123">This class is derived from <xref:System.Activities.NativeActivity> and overloads the <xref:System.Activities.NativeActivity.Execute%2A> method.</span></span>  
  
    ```csharp
    using System;  
    using System;  
    using System.Activities;  
    using System.Transactions;  
  
    namespace Common  
    {  
        public class PrintTransactionInfo : NativeActivity  
        {  
            protected override void Execute(NativeActivityContext context)  
            {  
                RuntimeTransactionHandle rth = context.Properties.Find(typeof(RuntimeTransactionHandle).FullName) as RuntimeTransactionHandle;  
  
                if (rth == null)  
                {  
                    Console.WriteLine("There is no ambient RuntimeTransactionHandle");  
                }  
  
                Transaction t = rth.GetCurrentTransaction(context);  
  
                if (t == null)  
                {  
                    Console.WriteLine("There is no ambient transaction");  
                }  
                else  
                {  
                    Console.WriteLine("Transaction: {0} is {1}", t.TransactionInformation.DistributedIdentifier, t.TransactionInformation.Status);  
                }  
            }  
        }  
  
    }  
    ```  
  
     <span data-ttu-id="c2948-124">这是一个本机活动，用于显示有关环境事务的信息，它将在本主题中使用的服务工作流和客户端工作流中使用。</span><span class="sxs-lookup"><span data-stu-id="c2948-124">This is a native activity that displays information about the ambient transaction and is used in both the service and client workflows used in this topic.</span></span> <span data-ttu-id="c2948-125">生成解决方案以使此活动在 **工具箱** 的 "**常用**" 部分中可用。</span><span class="sxs-lookup"><span data-stu-id="c2948-125">Build the solution to make this activity available in the **Common** section of the **Toolbox**.</span></span>  
  
### <a name="implement-the-workflow-service"></a><span data-ttu-id="c2948-126">实现工作流服务</span><span class="sxs-lookup"><span data-stu-id="c2948-126">Implement the workflow service</span></span>  
  
1. <span data-ttu-id="c2948-127">向项目添加一个名为的新 WCF 工作流服务 `WorkflowService` `Common` 。</span><span class="sxs-lookup"><span data-stu-id="c2948-127">Add a new WCF Workflow Service, called `WorkflowService` to the `Common` project.</span></span> <span data-ttu-id="c2948-128">为此，请右键单击 `Common` 项目，选择 "**添加**"、"**新建项 ...**"，选择 "**已安装模板**" 下的 "**工作流**"，然后选择 " **WCF 工作流服务**"</span><span class="sxs-lookup"><span data-stu-id="c2948-128">To do this right click the `Common` project, select **Add**, **New Item ...**, Select **Workflow** under **Installed Templates** and select **WCF Workflow Service**.</span></span>  
  
     ![添加工作流服务](./media/flowing-transactions-into-and-out-of-workflow-services/add-workflow-service.jpg)  
  
2. <span data-ttu-id="c2948-130">删除默认的 `ReceiveRequest` 和 `SendResponse` 活动。</span><span class="sxs-lookup"><span data-stu-id="c2948-130">Delete the default `ReceiveRequest` and `SendResponse` activities.</span></span>  
  
3. <span data-ttu-id="c2948-131">将 <xref:System.Activities.Statements.WriteLine> 活动拖放到 `Sequential Service` 活动中。</span><span class="sxs-lookup"><span data-stu-id="c2948-131">Drag and drop a <xref:System.Activities.Statements.WriteLine> activity into the `Sequential Service` activity.</span></span> <span data-ttu-id="c2948-132">将文本属性设置为 `"Workflow Service starting ..."`，如下面的示例所示。</span><span class="sxs-lookup"><span data-stu-id="c2948-132">Set the text property to `"Workflow Service starting ..."` as shown in the following example.</span></span>  
  
     <span data-ttu-id="c2948-133">![向顺序服务活动中添加 WriteLine 活动 (。/media/flowing-transactions-into-and-out-of-workflow-services/add-writeline-sequential-service.jpg) </span><span class="sxs-lookup"><span data-stu-id="c2948-133">![Adding a WriteLine activity to the Sequential Service activity(./media/flowing-transactions-into-and-out-of-workflow-services/add-writeline-sequential-service.jpg)</span></span>  
  
4. <span data-ttu-id="c2948-134">将 <xref:System.ServiceModel.Activities.TransactedReceiveScope> 拖放到 <xref:System.Activities.Statements.WriteLine> 活动后面。</span><span class="sxs-lookup"><span data-stu-id="c2948-134">Drag and drop a <xref:System.ServiceModel.Activities.TransactedReceiveScope> after the <xref:System.Activities.Statements.WriteLine> activity.</span></span> <span data-ttu-id="c2948-135"><xref:System.ServiceModel.Activities.TransactedReceiveScope>可以在 "**工具箱**" 的 "**消息传送**" 部分找到活动。</span><span class="sxs-lookup"><span data-stu-id="c2948-135">The <xref:System.ServiceModel.Activities.TransactedReceiveScope> activity can be found in the **Messaging** section of the **Toolbox**.</span></span> <span data-ttu-id="c2948-136"><xref:System.ServiceModel.Activities.TransactedReceiveScope>活动由两部分组成：**请求** 和 **正文**。</span><span class="sxs-lookup"><span data-stu-id="c2948-136">The <xref:System.ServiceModel.Activities.TransactedReceiveScope> activity is composed of two sections **Request** and **Body**.</span></span> <span data-ttu-id="c2948-137">" **请求** " 部分包含 <xref:System.ServiceModel.Activities.Receive> 活动。</span><span class="sxs-lookup"><span data-stu-id="c2948-137">The **Request** section contains the <xref:System.ServiceModel.Activities.Receive> activity.</span></span> <span data-ttu-id="c2948-138">**Body** 节包含在收到消息后在事务中执行的活动。</span><span class="sxs-lookup"><span data-stu-id="c2948-138">The **Body** section contains the activities to execute within a transaction after a message has been received.</span></span>  
  
     ![添加 TransactedReceiveScope 活动](./media/flowing-transactions-into-and-out-of-workflow-services/transactedreceivescope-activity.jpg)  
  
5. <span data-ttu-id="c2948-140">选择 <xref:System.ServiceModel.Activities.TransactedReceiveScope> 活动，然后单击 " **变量** " 按钮。</span><span class="sxs-lookup"><span data-stu-id="c2948-140">Select the <xref:System.ServiceModel.Activities.TransactedReceiveScope> activity and click the **Variables** button.</span></span> <span data-ttu-id="c2948-141">添加以下变量。</span><span class="sxs-lookup"><span data-stu-id="c2948-141">Add the following variables.</span></span>  
  
     ![向 TransactedReceiveScope 添加变量](./media/flowing-transactions-into-and-out-of-workflow-services/add-transactedreceivescope-variables.jpg)  
  
    > [!NOTE]
    > <span data-ttu-id="c2948-143">可以删除默认情况下在该处的数据变量。</span><span class="sxs-lookup"><span data-stu-id="c2948-143">You can delete the data variable that is there by default.</span></span> <span data-ttu-id="c2948-144">还可以使用现有句柄变量。</span><span class="sxs-lookup"><span data-stu-id="c2948-144">You can also use the existing handle variable.</span></span>  
  
6. <span data-ttu-id="c2948-145">将活动拖放到 <xref:System.ServiceModel.Activities.Receive> 活动的 " **请求** " 部分中 <xref:System.ServiceModel.Activities.TransactedReceiveScope> 。</span><span class="sxs-lookup"><span data-stu-id="c2948-145">Drag and drop a <xref:System.ServiceModel.Activities.Receive> activity within the **Request** section of the <xref:System.ServiceModel.Activities.TransactedReceiveScope> activity.</span></span> <span data-ttu-id="c2948-146">设置以下属性：</span><span class="sxs-lookup"><span data-stu-id="c2948-146">Set the following properties:</span></span>  
  
    |<span data-ttu-id="c2948-147">属性</span><span class="sxs-lookup"><span data-stu-id="c2948-147">Property</span></span>|<span data-ttu-id="c2948-148">值</span><span class="sxs-lookup"><span data-stu-id="c2948-148">Value</span></span>|  
    |--------------|-----------|  
    |<span data-ttu-id="c2948-149">CanCreateInstance</span><span class="sxs-lookup"><span data-stu-id="c2948-149">CanCreateInstance</span></span>|<span data-ttu-id="c2948-150">True（选中复选框）</span><span class="sxs-lookup"><span data-stu-id="c2948-150">True (check the checkbox)</span></span>|  
    |<span data-ttu-id="c2948-151">OperationName</span><span class="sxs-lookup"><span data-stu-id="c2948-151">OperationName</span></span>|<span data-ttu-id="c2948-152">StartSample</span><span class="sxs-lookup"><span data-stu-id="c2948-152">StartSample</span></span>|  
    |<span data-ttu-id="c2948-153">ServiceContractName</span><span class="sxs-lookup"><span data-stu-id="c2948-153">ServiceContractName</span></span>|<span data-ttu-id="c2948-154">ITransactionSample</span><span class="sxs-lookup"><span data-stu-id="c2948-154">ITransactionSample</span></span>|  
  
     <span data-ttu-id="c2948-155">该工作流应如下所示：</span><span class="sxs-lookup"><span data-stu-id="c2948-155">The workflow should look like this:</span></span>  
  
     ![添加 Receive 活动](./media/flowing-transactions-into-and-out-of-workflow-services/add-receive-activity.jpg)  
  
7. <span data-ttu-id="c2948-157">单击活动中的 " **定义 ...** " 链接 <xref:System.ServiceModel.Activities.Receive> ，然后进行以下设置：</span><span class="sxs-lookup"><span data-stu-id="c2948-157">Click the **Define...** link in the <xref:System.ServiceModel.Activities.Receive> activity and make the following settings:</span></span>  
  
     ![设置 Receive 活动的消息设置](./media/flowing-transactions-into-and-out-of-workflow-services/receive-message-settings.jpg)  
  
8. <span data-ttu-id="c2948-159">将 <xref:System.Activities.Statements.Sequence> 活动拖放到 <xref:System.ServiceModel.Activities.TransactedReceiveScope> 的“正文”部分内。</span><span class="sxs-lookup"><span data-stu-id="c2948-159">Drag and drop a <xref:System.Activities.Statements.Sequence> activity into the Body section of the <xref:System.ServiceModel.Activities.TransactedReceiveScope>.</span></span> <span data-ttu-id="c2948-160">在 <xref:System.Activities.Statements.Sequence> 活动内，拖放两个 <xref:System.Activities.Statements.WriteLine> 活动并设置 <xref:System.Activities.Statements.WriteLine.Text%2A> 属性，如下表所示。</span><span class="sxs-lookup"><span data-stu-id="c2948-160">Within the <xref:System.Activities.Statements.Sequence> activity drag and drop two <xref:System.Activities.Statements.WriteLine> activities and set the <xref:System.Activities.Statements.WriteLine.Text%2A> properties as shown in the following table.</span></span>  
  
    |<span data-ttu-id="c2948-161">活动</span><span class="sxs-lookup"><span data-stu-id="c2948-161">Activity</span></span>|<span data-ttu-id="c2948-162">值</span><span class="sxs-lookup"><span data-stu-id="c2948-162">Value</span></span>|  
    |--------------|-----------|  
    |<span data-ttu-id="c2948-163">第一个 WriteLine</span><span class="sxs-lookup"><span data-stu-id="c2948-163">1st WriteLine</span></span>|<span data-ttu-id="c2948-164">"服务：接收已完成"</span><span class="sxs-lookup"><span data-stu-id="c2948-164">"Service: Receive Completed"</span></span>|  
    |<span data-ttu-id="c2948-165">第二个 WriteLine</span><span class="sxs-lookup"><span data-stu-id="c2948-165">2nd WriteLine</span></span>|<span data-ttu-id="c2948-166">"Service: Received = " + requestMessage</span><span class="sxs-lookup"><span data-stu-id="c2948-166">"Service: Received = " + requestMessage</span></span>|  
  
     <span data-ttu-id="c2948-167">现在，该工作流应如下所示：</span><span class="sxs-lookup"><span data-stu-id="c2948-167">The workflow should now look like this:</span></span>  
  
     ![添加 WriteLine 活动后的序列](./media/flowing-transactions-into-and-out-of-workflow-services/after-adding-writelines.jpg)  
  
9. <span data-ttu-id="c2948-169">将活动拖放到 `PrintTransactionInfo` 活动的主体中的第二个 <xref:System.Activities.Statements.WriteLine> 活动之后 <xref:System.ServiceModel.Activities.TransactedReceiveScope> 。</span><span class="sxs-lookup"><span data-stu-id="c2948-169">Drag and drop the `PrintTransactionInfo` activity after the second <xref:System.Activities.Statements.WriteLine> activity in the **Body** in the <xref:System.ServiceModel.Activities.TransactedReceiveScope> activity.</span></span>  
  
     ![添加 PrintTransactionInfo 后的序列](./media/flowing-transactions-into-and-out-of-workflow-services/after-adding-printtransactioninfo.jpg )  
  
10. <span data-ttu-id="c2948-171">将 <xref:System.Activities.Statements.Assign> 活动拖放到 `PrintTransactionInfo` 活动后面，然后根据下表设置其属性。</span><span class="sxs-lookup"><span data-stu-id="c2948-171">Drag and drop an <xref:System.Activities.Statements.Assign> activity after the `PrintTransactionInfo` activity and set its properties according to the following table.</span></span>  
  
    |<span data-ttu-id="c2948-172">属性</span><span class="sxs-lookup"><span data-stu-id="c2948-172">Property</span></span>|<span data-ttu-id="c2948-173">值</span><span class="sxs-lookup"><span data-stu-id="c2948-173">Value</span></span>|  
    |--------------|-----------|  
    |<span data-ttu-id="c2948-174">功能</span><span class="sxs-lookup"><span data-stu-id="c2948-174">To</span></span>|<span data-ttu-id="c2948-175">replyMessage</span><span class="sxs-lookup"><span data-stu-id="c2948-175">replyMessage</span></span>|  
    |<span data-ttu-id="c2948-176">值</span><span class="sxs-lookup"><span data-stu-id="c2948-176">Value</span></span>|<span data-ttu-id="c2948-177">"Service: Sending reply."</span><span class="sxs-lookup"><span data-stu-id="c2948-177">"Service: Sending reply."</span></span>|  
  
11. <span data-ttu-id="c2948-178">将 <xref:System.Activities.Statements.WriteLine> 活动拖放到 <xref:System.Activities.Statements.Assign> 活动后面，然后将它的 <xref:System.Activities.Statements.WriteLine.Text%2A> 属性设置为 "Service: Begin reply."</span><span class="sxs-lookup"><span data-stu-id="c2948-178">Drag and drop a <xref:System.Activities.Statements.WriteLine> activity after the <xref:System.Activities.Statements.Assign> activity and set its <xref:System.Activities.Statements.WriteLine.Text%2A> property to "Service: Begin reply."</span></span>  
  
     <span data-ttu-id="c2948-179">现在，该工作流应如下所示：</span><span class="sxs-lookup"><span data-stu-id="c2948-179">The workflow should now look like this:</span></span>  
  
     ![添加 Assign 和 WriteLine 后](./media/flowing-transactions-into-and-out-of-workflow-services/after-adding-sbr-writeline.jpg)  
  
12. <span data-ttu-id="c2948-181">右键单击该 <xref:System.ServiceModel.Activities.Receive> 活动，然后选择 " **创建 SendReply** " 并将其粘贴到最后一个 <xref:System.Activities.Statements.WriteLine> 活动后面。</span><span class="sxs-lookup"><span data-stu-id="c2948-181">Right click the <xref:System.ServiceModel.Activities.Receive> activity and select **Create SendReply** and paste it after the last <xref:System.Activities.Statements.WriteLine> activity.</span></span> <span data-ttu-id="c2948-182">单击活动中的 " **定义 ...** " 链接 `SendReplyToReceive` ，然后进行以下设置。</span><span class="sxs-lookup"><span data-stu-id="c2948-182">Click the **Define...** link in the `SendReplyToReceive` activity and make the following settings.</span></span>  
  
     ![回复消息设置](./media/flowing-transactions-into-and-out-of-workflow-services/reply-message-settings.jpg)  
  
13. <span data-ttu-id="c2948-184">将活动拖放 <xref:System.Activities.Statements.WriteLine> `SendReplyToReceive` 到活动后面，并将其 <xref:System.Activities.Statements.WriteLine.Text%2A> 属性设置为 "Service： Reply sent"。</span><span class="sxs-lookup"><span data-stu-id="c2948-184">Drag and drop a <xref:System.Activities.Statements.WriteLine> activity after the `SendReplyToReceive` activity and set it’s <xref:System.Activities.Statements.WriteLine.Text%2A> property to "Service: Reply sent."</span></span>  
  
14. <span data-ttu-id="c2948-185">将 <xref:System.Activities.Statements.WriteLine> 活动拖放到工作流底部，然后将它的 <xref:System.Activities.Statements.WriteLine.Text%2A> 属性设置为 "Service: Workflow ends, press ENTER to exit."</span><span class="sxs-lookup"><span data-stu-id="c2948-185">Drag and drop a <xref:System.Activities.Statements.WriteLine> activity at the bottom of the workflow and set its <xref:System.Activities.Statements.WriteLine.Text%2A> property to "Service: Workflow ends, press ENTER to exit."</span></span>  
  
     <span data-ttu-id="c2948-186">完成的服务工作流应如下所示：</span><span class="sxs-lookup"><span data-stu-id="c2948-186">The completed service workflow should look like this:</span></span>  
  
     ![完成服务工作流](./media/flowing-transactions-into-and-out-of-workflow-services/service-complete-workflow.jpg)  
  
### <a name="implement-the-workflow-client"></a><span data-ttu-id="c2948-188">实现工作流客户端</span><span class="sxs-lookup"><span data-stu-id="c2948-188">Implement the workflow client</span></span>  
  
1. <span data-ttu-id="c2948-189">将一个名为 `WorkflowClient` 的新 WCF 工作流应用程序添加到 `Common` 项目。</span><span class="sxs-lookup"><span data-stu-id="c2948-189">Add a new WCF Workflow application, called `WorkflowClient` to the `Common` project.</span></span> <span data-ttu-id="c2948-190">要执行此操作，请右键单击 `Common` 项目，选择 "**添加**" "**新建项 ...**"，选择 "**已安装模板**" 下的 "**工作流**"，然后选择 "**活动**</span><span class="sxs-lookup"><span data-stu-id="c2948-190">To do this right click the `Common` project, select **Add**, **New Item ...**, Select **Workflow** under **Installed Templates** and select **Activity**.</span></span>  
  
     ![添加活动项目](./media/flowing-transactions-into-and-out-of-workflow-services/add-activity-project.jpg)  
  
2. <span data-ttu-id="c2948-192">将 <xref:System.Activities.Statements.Sequence> 活动拖放到设计图面上。</span><span class="sxs-lookup"><span data-stu-id="c2948-192">Drag and drop a <xref:System.Activities.Statements.Sequence> activity onto the design surface.</span></span>  
  
3. <span data-ttu-id="c2948-193">在 <xref:System.Activities.Statements.Sequence> 活动内拖放一个 <xref:System.Activities.Statements.WriteLine> 活动，然后将它的 <xref:System.Activities.Statements.WriteLine.Text%2A> 属性设置为 `"Client: Workflow starting"`。</span><span class="sxs-lookup"><span data-stu-id="c2948-193">Within the <xref:System.Activities.Statements.Sequence> activity drag and drop a <xref:System.Activities.Statements.WriteLine> activity and set its <xref:System.Activities.Statements.WriteLine.Text%2A> property to `"Client: Workflow starting"`.</span></span> <span data-ttu-id="c2948-194">现在，该工作流应如下所示：</span><span class="sxs-lookup"><span data-stu-id="c2948-194">The workflow should now look like this:</span></span>  
  
     ![添加 WriteLine 活动](./media/flowing-transactions-into-and-out-of-workflow-services/add-writeline-activity.jpg)  
  
4. <span data-ttu-id="c2948-196">将 <xref:System.Activities.Statements.TransactionScope> 活动拖放到 <xref:System.Activities.Statements.WriteLine> 活动后面。</span><span class="sxs-lookup"><span data-stu-id="c2948-196">Drag and drop a <xref:System.Activities.Statements.TransactionScope> activity after the <xref:System.Activities.Statements.WriteLine> activity.</span></span>  <span data-ttu-id="c2948-197">选择 <xref:System.Activities.Statements.TransactionScope> 活动，单击“变量”按钮，然后添加以下变量。</span><span class="sxs-lookup"><span data-stu-id="c2948-197">Select the <xref:System.Activities.Statements.TransactionScope> activity, click the Variables button and add the following variables.</span></span>  
  
     ![向 TransactionScope 添加变量](./media/flowing-transactions-into-and-out-of-workflow-services/transactionscope-variables.jpg)  
  
5. <span data-ttu-id="c2948-199">将 <xref:System.Activities.Statements.Sequence> 活动拖放到 <xref:System.Activities.Statements.TransactionScope> 活动的正文内。</span><span class="sxs-lookup"><span data-stu-id="c2948-199">Drag and drop a <xref:System.Activities.Statements.Sequence> activity into the body of the <xref:System.Activities.Statements.TransactionScope> activity.</span></span>  
  
6. <span data-ttu-id="c2948-200">在 `PrintTransactionInfo` 内拖放 <xref:System.Activities.Statements.Sequence> 活动</span><span class="sxs-lookup"><span data-stu-id="c2948-200">Drag and drop a `PrintTransactionInfo` activity within the <xref:System.Activities.Statements.Sequence></span></span>  
  
7. <span data-ttu-id="c2948-201">将活动拖放 <xref:System.Activities.Statements.WriteLine> `PrintTransactionInfo` 到活动后面，并将其 <xref:System.Activities.Statements.WriteLine.Text%2A> 属性设置为 "Client：开始发送"。</span><span class="sxs-lookup"><span data-stu-id="c2948-201">Drag and drop a <xref:System.Activities.Statements.WriteLine> activity after the `PrintTransactionInfo` activity and set its <xref:System.Activities.Statements.WriteLine.Text%2A> property to "Client: Beginning Send".</span></span> <span data-ttu-id="c2948-202">现在，该工作流应如下所示：</span><span class="sxs-lookup"><span data-stu-id="c2948-202">The workflow should now look like this:</span></span>  
  
     ![添加客户端：开始发送活动](./media/flowing-transactions-into-and-out-of-workflow-services/client-add-cbs-writeline.jpg)  
  
8. <span data-ttu-id="c2948-204">将 <xref:System.ServiceModel.Activities.Send> 活动拖放到 <xref:System.Activities.Statements.Assign> 活动后面，并设置以下属性：</span><span class="sxs-lookup"><span data-stu-id="c2948-204">Drag and drop a <xref:System.ServiceModel.Activities.Send> activity after the <xref:System.Activities.Statements.Assign> activity and set the following properties:</span></span>  
  
    |<span data-ttu-id="c2948-205">属性</span><span class="sxs-lookup"><span data-stu-id="c2948-205">Property</span></span>|<span data-ttu-id="c2948-206">值</span><span class="sxs-lookup"><span data-stu-id="c2948-206">Value</span></span>|  
    |--------------|-----------|  
    |<span data-ttu-id="c2948-207">EndpointConfigurationName</span><span class="sxs-lookup"><span data-stu-id="c2948-207">EndpointConfigurationName</span></span>|<span data-ttu-id="c2948-208">workflowServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="c2948-208">workflowServiceEndpoint</span></span>|  
    |<span data-ttu-id="c2948-209">OperationName</span><span class="sxs-lookup"><span data-stu-id="c2948-209">OperationName</span></span>|<span data-ttu-id="c2948-210">StartSample</span><span class="sxs-lookup"><span data-stu-id="c2948-210">StartSample</span></span>|  
    |<span data-ttu-id="c2948-211">ServiceContractName</span><span class="sxs-lookup"><span data-stu-id="c2948-211">ServiceContractName</span></span>|<span data-ttu-id="c2948-212">ITransactionSample</span><span class="sxs-lookup"><span data-stu-id="c2948-212">ITransactionSample</span></span>|  
  
     <span data-ttu-id="c2948-213">现在，该工作流应如下所示：</span><span class="sxs-lookup"><span data-stu-id="c2948-213">The workflow should now look like this:</span></span>  
  
     ![设置 Send 活动属性](./media/flowing-transactions-into-and-out-of-workflow-services/client-send-activity-settings.jpg)  
  
9. <span data-ttu-id="c2948-215">单击 " **定义 ...** " 链接，然后进行以下设置：</span><span class="sxs-lookup"><span data-stu-id="c2948-215">Click the **Define...** link and make the following settings:</span></span>  
  
     ![发送活动的消息设置](./media/flowing-transactions-into-and-out-of-workflow-services/send-message-settings.jpg)  
  
10. <span data-ttu-id="c2948-217">右键单击该 <xref:System.ServiceModel.Activities.Send> 活动，然后选择 " **创建 ReceiveReply**"。</span><span class="sxs-lookup"><span data-stu-id="c2948-217">Right click the <xref:System.ServiceModel.Activities.Send> activity and select **Create ReceiveReply**.</span></span> <span data-ttu-id="c2948-218"><xref:System.ServiceModel.Activities.ReceiveReply> 活动将自动放在 <xref:System.ServiceModel.Activities.Send> 活动后面。</span><span class="sxs-lookup"><span data-stu-id="c2948-218">The <xref:System.ServiceModel.Activities.ReceiveReply> activity will be automatically placed after the <xref:System.ServiceModel.Activities.Send> activity.</span></span>  
  
11. <span data-ttu-id="c2948-219">单击 ReceiveReplyForSend 活动上的“定义...”链接，然后进行以下设置：</span><span class="sxs-lookup"><span data-stu-id="c2948-219">Click the Define... link on the ReceiveReplyForSend activity and make the following settings:</span></span>  
  
     ![设置 ReceiveForSend 消息的设置](./media/flowing-transactions-into-and-out-of-workflow-services/client-reply-message-settings.jpg)  
  
12. <span data-ttu-id="c2948-221">将 <xref:System.Activities.Statements.WriteLine> 活动拖放到 <xref:System.ServiceModel.Activities.Send> 和 <xref:System.ServiceModel.Activities.ReceiveReply> 活动之间，然后将它的 <xref:System.Activities.Statements.WriteLine.Text%2A> 属性设置为 "Client: Send complete."</span><span class="sxs-lookup"><span data-stu-id="c2948-221">Drag and drop a <xref:System.Activities.Statements.WriteLine> activity between the <xref:System.ServiceModel.Activities.Send> and <xref:System.ServiceModel.Activities.ReceiveReply> activities and set its <xref:System.Activities.Statements.WriteLine.Text%2A> property to "Client: Send complete."</span></span>  
  
13. <span data-ttu-id="c2948-222">将 <xref:System.Activities.Statements.WriteLine> 活动拖放到 <xref:System.ServiceModel.Activities.ReceiveReply> 活动后面，然后将它的 <xref:System.Activities.Statements.WriteLine.Text%2A> 属性设置为 "Client side: Reply received = " + replyMessage</span><span class="sxs-lookup"><span data-stu-id="c2948-222">Drag and drop a <xref:System.Activities.Statements.WriteLine> activity after the <xref:System.ServiceModel.Activities.ReceiveReply> activity and set its <xref:System.Activities.Statements.WriteLine.Text%2A> property to "Client side: Reply received = " + replyMessage</span></span>  
  
14. <span data-ttu-id="c2948-223">将 `PrintTransactionInfo` 活动拖放到 <xref:System.Activities.Statements.WriteLine> 活动后面。</span><span class="sxs-lookup"><span data-stu-id="c2948-223">Drag and drop a `PrintTransactionInfo` activity after the <xref:System.Activities.Statements.WriteLine> activity.</span></span>  
  
15. <span data-ttu-id="c2948-224">将 <xref:System.Activities.Statements.WriteLine> 活动拖放到工作流末尾，然后将它的 <xref:System.Activities.Statements.WriteLine.Text%2A> 属性设置为 "Client workflow ends."</span><span class="sxs-lookup"><span data-stu-id="c2948-224">Drag and drop a <xref:System.Activities.Statements.WriteLine> activity at the end of the workflow and set its <xref:System.Activities.Statements.WriteLine.Text%2A> property to "Client workflow ends."</span></span> <span data-ttu-id="c2948-225">完成的客户端工作流应如下图所示。</span><span class="sxs-lookup"><span data-stu-id="c2948-225">The completed client workflow should look like the following diagram.</span></span>  
  
     ![已完成的客户端工作流](./media/flowing-transactions-into-and-out-of-workflow-services/client-complete-workflow.jpg)  
  
16. <span data-ttu-id="c2948-227">生成解决方案。</span><span class="sxs-lookup"><span data-stu-id="c2948-227">Build the solution.</span></span>  
  
### <a name="create-the-service-application"></a><span data-ttu-id="c2948-228">创建服务应用程序</span><span class="sxs-lookup"><span data-stu-id="c2948-228">Create the Service application</span></span>  
  
1. <span data-ttu-id="c2948-229">将一个名为 `Service` 的新控制台应用程序项目添加到该解决方案。</span><span class="sxs-lookup"><span data-stu-id="c2948-229">Add a new Console Application project called `Service` to the solution.</span></span> <span data-ttu-id="c2948-230">添加对下列程序集的引用：</span><span class="sxs-lookup"><span data-stu-id="c2948-230">Add references to the following assemblies:</span></span>  
  
    1. <span data-ttu-id="c2948-231">System.Activities.dll</span><span class="sxs-lookup"><span data-stu-id="c2948-231">System.Activities.dll</span></span>  
  
    2. <span data-ttu-id="c2948-232">System.ServiceModel.dll</span><span class="sxs-lookup"><span data-stu-id="c2948-232">System.ServiceModel.dll</span></span>  
  
    3. <span data-ttu-id="c2948-233">System.ServiceModel.Activities.dll</span><span class="sxs-lookup"><span data-stu-id="c2948-233">System.ServiceModel.Activities.dll</span></span>  
  
2. <span data-ttu-id="c2948-234">打开生成的 Program.cs 文件并添加以下代码：</span><span class="sxs-lookup"><span data-stu-id="c2948-234">Open the generated Program.cs file and the following code:</span></span>  
  
    ```csharp
          static void Main()  
          {  
              Console.WriteLine("Building the server.");  
              using (WorkflowServiceHost host = new WorkflowServiceHost(new DeclarativeServiceWorkflow(), new Uri("net.tcp://localhost:8000/TransactedReceiveService/Declarative")))  
              {
                  //Start the server  
                  host.Open();  
                  Console.WriteLine("Service started.");  
  
                  Console.WriteLine();  
                  Console.ReadLine();  
                  //Shutdown  
                  host.Close();  
              };
          }  
    ```  
  
3. <span data-ttu-id="c2948-235">将以下 app.config 文件添加到项目。</span><span class="sxs-lookup"><span data-stu-id="c2948-235">Add the following app.config file to the project.</span></span>  
  
    ```xml  
    <?xml version="1.0" encoding="utf-8" ?>  
    <!-- Copyright © Microsoft Corporation.  All rights reserved. -->  
    <configuration>  
        <system.serviceModel>  
            <bindings>  
                <netTcpBinding>  
                    <binding transactionFlow="true" />  
                </netTcpBinding>  
            </bindings>  
        </system.serviceModel>  
    </configuration>  
    ```  
  
### <a name="create-the-client-application"></a><span data-ttu-id="c2948-236">创建客户端应用程序</span><span class="sxs-lookup"><span data-stu-id="c2948-236">Create the client application</span></span>  
  
1. <span data-ttu-id="c2948-237">将一个名为 `Client` 的新控制台应用程序项目添加到该解决方案。</span><span class="sxs-lookup"><span data-stu-id="c2948-237">Add a new Console Application project called `Client` to the solution.</span></span> <span data-ttu-id="c2948-238">添加对 System.Activities.dll 的引用。</span><span class="sxs-lookup"><span data-stu-id="c2948-238">Add a reference to System.Activities.dll.</span></span>  
  
2. <span data-ttu-id="c2948-239">打开 program.cs 文件并添加以下代码。</span><span class="sxs-lookup"><span data-stu-id="c2948-239">Open the program.cs file and add the following code.</span></span>  
  
    ```csharp
    class Program  
    {  

        private static AutoResetEvent syncEvent = new AutoResetEvent(false);  
  
        static void Main(string[] args)  
        {  
            //Build client  
            Console.WriteLine("Building the client.");  
            WorkflowApplication client = new WorkflowApplication(new DeclarativeClientWorkflow());  
            client.Completed = Program.Completed;  
            client.Aborted = Program.Aborted;  
            client.OnUnhandledException = Program.OnUnhandledException;  
            //Wait for service to start  
            Console.WriteLine("Press ENTER once service is started.");  
            Console.ReadLine();  
  
            //Start the client
            Console.WriteLine("Starting the client.");  
            client.Run();  
            syncEvent.WaitOne();  
  
            //Sample complete  
            Console.WriteLine();  
            Console.WriteLine("Client complete. Press ENTER to exit.");  
            Console.ReadLine();  
        }  
  
        private static void Completed(WorkflowApplicationCompletedEventArgs e)  
        {  
            Program.syncEvent.Set();  
        }  
  
        private static void Aborted(WorkflowApplicationAbortedEventArgs e)  
        {  
            Console.WriteLine("Client Aborted: {0}", e.Reason);  
            Program.syncEvent.Set();  
        }  
  
        private static UnhandledExceptionAction OnUnhandledException(WorkflowApplicationUnhandledExceptionEventArgs e)  
        {  
            Console.WriteLine("Client had an unhandled exception: {0}", e.UnhandledException);  
            return UnhandledExceptionAction.Cancel;  
        }  
    }  
    ```  
  
## <a name="see-also"></a><span data-ttu-id="c2948-240">请参阅</span><span class="sxs-lookup"><span data-stu-id="c2948-240">See also</span></span>

- [<span data-ttu-id="c2948-241">工作流服务</span><span class="sxs-lookup"><span data-stu-id="c2948-241">Workflow Services</span></span>](workflow-services.md)
- [<span data-ttu-id="c2948-242">Windows Communication Foundation 事务概述</span><span class="sxs-lookup"><span data-stu-id="c2948-242">Windows Communication Foundation Transactions Overview</span></span>](transactions-overview.md)
