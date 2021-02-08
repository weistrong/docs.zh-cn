---
description: 了解详细信息：服务事务行为
title: 服务事务行为
ms.date: 03/30/2017
helpviewer_keywords:
- Service Transaction Behavior Sample [Windows Communication Foundation]
ms.assetid: 1a9842a3-e84d-427c-b6ac-6999cbbc2612
ms.openlocfilehash: 1f8b76de250ef87ec5ca2d4ea4353a9a28bac248
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99793059"
---
# <a name="service-transaction-behavior"></a><span data-ttu-id="4fda4-103">服务事务行为</span><span class="sxs-lookup"><span data-stu-id="4fda4-103">Service Transaction Behavior</span></span>

<span data-ttu-id="4fda4-104">此示例演示客户端协调事务的用法，以及为了控制服务事务行为而对 ServiceBehaviorAttribute 和 OperationBehaviorAttribute 进行的设置。</span><span class="sxs-lookup"><span data-stu-id="4fda4-104">This sample demonstrates the use of a client-coordinated transaction and the settings of ServiceBehaviorAttribute and OperationBehaviorAttribute to control service transaction behavior.</span></span> <span data-ttu-id="4fda4-105">此示例基于实现计算器服务的 [入门](getting-started-sample.md) ，但扩展为维护数据库表中所执行操作的服务器日志和计算器操作的有状态运行总计。</span><span class="sxs-lookup"><span data-stu-id="4fda4-105">This sample is based on the [Getting Started](getting-started-sample.md) that implements a calculator service, but is extended to maintain a server log of the performed operations in a database table and a stateful running total for the calculator operations.</span></span> <span data-ttu-id="4fda4-106">持久写入服务器日志表依赖于客户端协调事务的结果 - 如果客户端事务未完成，Web 服务事务可以确保不会提交对数据库的更新。</span><span class="sxs-lookup"><span data-stu-id="4fda4-106">Persisted writes to the server log table are dependent upon the outcome of a client coordinated transaction - if the client transaction does not complete, the Web service transaction ensures that the updates to the database are not committed.</span></span>

> [!NOTE]
> <span data-ttu-id="4fda4-107">本主题的最后介绍了此示例的设置过程和生成说明。</span><span class="sxs-lookup"><span data-stu-id="4fda4-107">The setup procedure and build instructions for this sample are located at the end of this topic.</span></span>

<span data-ttu-id="4fda4-108">服务协定定义所有操作都要求通过请求对事务进行流处理：</span><span class="sxs-lookup"><span data-stu-id="4fda4-108">The contract for the service defines that all of the operations require a transaction to be flowed with requests:</span></span>

```csharp
[ServiceContract(Namespace = "http://Microsoft.ServiceModel.Samples",
                    SessionMode = SessionMode.Required)]
public interface ICalculator
{
    [OperationContract]
    [TransactionFlow(TransactionFlowOption.Mandatory)]
    double Add(double n);
    [OperationContract]
    [TransactionFlow(TransactionFlowOption.Mandatory)]
    double Subtract(double n);
    [OperationContract]
    [TransactionFlow(TransactionFlowOption.Mandatory)]
    double Multiply(double n);
    [OperationContract]
    [TransactionFlow(TransactionFlowOption.Mandatory)]
    double Divide(double n);
}
```

<span data-ttu-id="4fda4-109">为了启用传入事务流，使用系统提供的 wsHttpBinding 对服务进行了配置，并将 transactionFlow 属性设置为 `true`。</span><span class="sxs-lookup"><span data-stu-id="4fda4-109">To enable the incoming transaction flow, the service is configured with the system-provided wsHttpBinding with the transactionFlow attribute set to `true`.</span></span> <span data-ttu-id="4fda4-110">此绑定使用可互操作的 WSAtomicTransactionOctober2004 协议：</span><span class="sxs-lookup"><span data-stu-id="4fda4-110">This binding uses the interoperable WSAtomicTransactionOctober2004 protocol:</span></span>

```xml
<bindings>
  <wsHttpBinding>
    <binding name="transactionalBinding" transactionFlow="true" />
  </wsHttpBinding>
</bindings>
```

<span data-ttu-id="4fda4-111">启动与服务和事务的连接后，客户端访问该事务范围内的几个服务操作，然后完成该事务并断开连接：</span><span class="sxs-lookup"><span data-stu-id="4fda4-111">After initiating both a connection to the service and a transaction, the client accesses several service operations within the scope of that transaction and then completes the transaction and closes the connection:</span></span>

```csharp
// Create a client
CalculatorClient client = new CalculatorClient();

// Create a transaction scope with the default isolation level of Serializable
using (TransactionScope tx = new TransactionScope())
{
    Console.WriteLine("Starting transaction");

    // Call the Add service operation.
    double value = 100.00D;
    Console.WriteLine("  Adding {0}, running total={1}",
                                        value, client.Add(value));

    // Call the Subtract service operation.
    value = 45.00D;
    Console.WriteLine("  Subtracting {0}, running total={1}",
                                        value, client.Subtract(value));

    // Call the Multiply service operation.
    value = 9.00D;
    Console.WriteLine("  Multiplying by {0}, running total={1}",
                                        value, client.Multiply(value));

    // Call the Divide service operation.
    value = 15.00D;
    Console.WriteLine("  Dividing by {0}, running total={1}",
                                        value, client.Divide(value));

    Console.WriteLine("  Completing transaction");
    tx.Complete();
}

Console.WriteLine("Transaction committed");

// Closing the client gracefully closes the connection and cleans up resources
client.Close();
```

<span data-ttu-id="4fda4-112">服务上有三个属性通过以下方式影响服务事务行为：</span><span class="sxs-lookup"><span data-stu-id="4fda4-112">On the service, there are three attributes that affect the service transaction behavior, and they do so in the following ways:</span></span>

- <span data-ttu-id="4fda4-113">在 `ServiceBehaviorAttribute` 上：</span><span class="sxs-lookup"><span data-stu-id="4fda4-113">On the `ServiceBehaviorAttribute`:</span></span>

  - <span data-ttu-id="4fda4-114">`TransactionTimeout` 属性指定必须完成事务的时间段。</span><span class="sxs-lookup"><span data-stu-id="4fda4-114">The `TransactionTimeout` property specifies the time period within which a transaction must complete.</span></span> <span data-ttu-id="4fda4-115">在此示例中，此属性设置为 30 秒。</span><span class="sxs-lookup"><span data-stu-id="4fda4-115">In this sample it is set to 30 seconds.</span></span>

  - <span data-ttu-id="4fda4-116">`TransactionIsolationLevel` 属性指定服务支持的隔离级别。</span><span class="sxs-lookup"><span data-stu-id="4fda4-116">The `TransactionIsolationLevel` property specifies the isolation level that the service supports.</span></span> <span data-ttu-id="4fda4-117">这是与客户端隔离级别相匹配所必需的。</span><span class="sxs-lookup"><span data-stu-id="4fda4-117">This is required to match the client's isolation level.</span></span>

  - <span data-ttu-id="4fda4-118">`ReleaseServiceInstanceOnTransactionComplete` 属性指定当事务完成后是否回收服务实例。</span><span class="sxs-lookup"><span data-stu-id="4fda4-118">The `ReleaseServiceInstanceOnTransactionComplete` property specifies whether the service instance is recycled when a transaction completes.</span></span> <span data-ttu-id="4fda4-119">如果将此属性设置为 `false`，服务将在所有操作请求中维护相同的服务实例。</span><span class="sxs-lookup"><span data-stu-id="4fda4-119">By setting it to `false`, the service maintains the same service instance across the operation requests.</span></span> <span data-ttu-id="4fda4-120">这是维护运行总数所必需的。</span><span class="sxs-lookup"><span data-stu-id="4fda4-120">This is required to maintain the running total.</span></span> <span data-ttu-id="4fda4-121">如果设置为 `true`，每完成一个操作就会生成一个新实例。</span><span class="sxs-lookup"><span data-stu-id="4fda4-121">If set to `true`, a new instance is generated after each completed action.</span></span>

  - <span data-ttu-id="4fda4-122">`TransactionAutoCompleteOnSessionClose` 属性指定会话关闭时是否完成未处理的事务。</span><span class="sxs-lookup"><span data-stu-id="4fda4-122">The `TransactionAutoCompleteOnSessionClose` property specifies whether outstanding transactions are completed when the session closes.</span></span> <span data-ttu-id="4fda4-123">通过将其设置为 `false` ，每个操作都需要将属性设置 <xref:System.ServiceModel.OperationBehaviorAttribute.TransactionAutoComplete?displayProperty=nameWithType> 为 `true` 或显式要求调用 <xref:System.ServiceModel.OperationContext.SetTransactionComplete?displayProperty=nameWithType> 方法才能完成事务。</span><span class="sxs-lookup"><span data-stu-id="4fda4-123">By setting it to `false`, the individual operations are required to either set the <xref:System.ServiceModel.OperationBehaviorAttribute.TransactionAutoComplete?displayProperty=nameWithType> property to `true` or to explicitly require a call to the <xref:System.ServiceModel.OperationContext.SetTransactionComplete?displayProperty=nameWithType> method to complete transactions.</span></span> <span data-ttu-id="4fda4-124">此示例对这两种方法进行了演示。</span><span class="sxs-lookup"><span data-stu-id="4fda4-124">This sample demonstrates both approaches.</span></span>

- <span data-ttu-id="4fda4-125">在 `ServiceContractAttribute` 上：</span><span class="sxs-lookup"><span data-stu-id="4fda4-125">On the `ServiceContractAttribute`:</span></span>

  - <span data-ttu-id="4fda4-126">`SessionMode` 属性指定服务是否将相应的请求相互关联，从而形成一个逻辑会话。</span><span class="sxs-lookup"><span data-stu-id="4fda4-126">The `SessionMode` property specifies whether the service correlates the appropriate requests into a logical session.</span></span> <span data-ttu-id="4fda4-127">因为此服务包括将 OperationBehaviorAttribute TransactionAutoComplete 属性设置为 `false` 时的操作（Multiply 和 Divide），所以必须指定 `SessionMode.Required`。</span><span class="sxs-lookup"><span data-stu-id="4fda4-127">Because this service includes operations where the OperationBehaviorAttribute TransactionAutoComplete property is set to `false` (Multiply and Divide), `SessionMode.Required` must be specified.</span></span> <span data-ttu-id="4fda4-128">例如，Multiply 操作不会完成其事务，而是依赖稍后使用 `SetTransactionComplete` 方法对 Divide 操作的调用；服务必须能够确定这些服务是在同一个会话中发生的。</span><span class="sxs-lookup"><span data-stu-id="4fda4-128">For example, the Multiply operation does not complete its transaction and instead relies upon a later call to Divide to complete using the `SetTransactionComplete` method; the service must be able to determine that these operations are occurring within the same session.</span></span>

- <span data-ttu-id="4fda4-129">在 `OperationBehaviorAttribute` 上：</span><span class="sxs-lookup"><span data-stu-id="4fda4-129">On the `OperationBehaviorAttribute`:</span></span>

  - <span data-ttu-id="4fda4-130">`TransactionScopeRequired` 属性指定是否应在事务范围内执行操作。</span><span class="sxs-lookup"><span data-stu-id="4fda4-130">The `TransactionScopeRequired` property specifies whether the operation's actions should be executed within a transaction scope.</span></span> <span data-ttu-id="4fda4-131">在此示例中，此属性对于所有操作都设置为 `true`，同时由于客户端将其事务流向所有操作，所以操作是在该客户端事务的范围内发生的。</span><span class="sxs-lookup"><span data-stu-id="4fda4-131">This is set to `true` for all operations in this sample and, because the client flows its transaction to all operations, the actions occur within the scope of that client transaction.</span></span>

  - <span data-ttu-id="4fda4-132">`TransactionAutoComplete` 属性指定如果没有发生未处理的异常，是否自动完成在其中执行方法的事务。</span><span class="sxs-lookup"><span data-stu-id="4fda4-132">The `TransactionAutoComplete` property specifies whether the transaction in which the method executes is automatically completed if no unhandled exceptions occur.</span></span> <span data-ttu-id="4fda4-133">如前面所讲，此属性对于 Add 和 Subtract 操作设置为 `true`，但对于 Multiply 和 Divide 操作则设置为 `false`。</span><span class="sxs-lookup"><span data-stu-id="4fda4-133">As previously described, this is set to `true` for the Add and Subtract operations but `false` for the Multiply and Divide operations.</span></span> <span data-ttu-id="4fda4-134">Add 和 Subtract 操作自动完成操作，Divide 操作通过显式调用 `SetTransactionComplete` 方法完成操作，Multiply 操作不会完成，而是依赖并请求稍后的调用（例如，调用 Divide）来完成操作。</span><span class="sxs-lookup"><span data-stu-id="4fda4-134">The Add and Subtract operations complete their actions automatically, the Divide completes its actions through an explicit call to the `SetTransactionComplete` method, and the Multiply does not complete its actions but instead relies upon and requires a later call, such as to Divide, to complete the actions.</span></span>

<span data-ttu-id="4fda4-135">属性化服务实现如下：</span><span class="sxs-lookup"><span data-stu-id="4fda4-135">The attributed service implementation is as follows:</span></span>

```csharp
[ServiceBehavior(
    TransactionIsolationLevel = System.Transactions.IsolationLevel.Serializable,
    TransactionTimeout = "00:00:30",
    ReleaseServiceInstanceOnTransactionComplete = false,
    TransactionAutoCompleteOnSessionClose = false)]
public class CalculatorService : ICalculator
{
    double runningTotal;

    public CalculatorService()
    {
        Console.WriteLine("Creating new service instance...");
    }

    [OperationBehavior(TransactionScopeRequired = true, TransactionAutoComplete = true)]
    public double Add(double n)
    {
        RecordToLog(String.Format(CultureInfo.CurrentCulture, "Adding {0} to {1}", n, runningTotal));
        runningTotal = runningTotal + n;
        return runningTotal;
    }

    [OperationBehavior(TransactionScopeRequired = true, TransactionAutoComplete = true)]
    public double Subtract(double n)
    {
        RecordToLog(String.Format(CultureInfo.CurrentCulture, "Subtracting {0} from {1}", n, runningTotal));
        runningTotal = runningTotal - n;
        return runningTotal;
    }

    [OperationBehavior(TransactionScopeRequired = true, TransactionAutoComplete = false)]
    public double Multiply(double n)
    {
        RecordToLog(String.Format(CultureInfo.CurrentCulture, "Multiplying {0} by {1}", runningTotal, n));
        runningTotal = runningTotal * n;
        return runningTotal;
    }

    [OperationBehavior(TransactionScopeRequired = true, TransactionAutoComplete = false)]
    public double Divide(double n)
    {
        RecordToLog(String.Format(CultureInfo.CurrentCulture, "Dividing {0} by {1}", runningTotal, n));
        runningTotal = runningTotal / n;
        OperationContext.Current.SetTransactionComplete();
        return runningTotal;
    }

    // Logging method omitted for brevity
}
```

<span data-ttu-id="4fda4-136">运行示例时，操作请求和响应将显示在客户端控制台窗口中。</span><span class="sxs-lookup"><span data-stu-id="4fda4-136">When you run the sample, the operation requests and responses are displayed in the client console window.</span></span> <span data-ttu-id="4fda4-137">在客户端窗口中按 Enter 可以关闭客户端。</span><span class="sxs-lookup"><span data-stu-id="4fda4-137">Press ENTER in the client window to shut down the client.</span></span>

```console
Starting transaction
Performing calculations...
  Adding 100, running total=100
  Subtracting 45, running total=55
  Multiplying by 9, running total=495
  Dividing by 15, running total=33
  Completing transaction
Transaction committed
Press <ENTER> to terminate client.
```

<span data-ttu-id="4fda4-138">服务操作请求的日志记录显示在服务的控制台窗口中。</span><span class="sxs-lookup"><span data-stu-id="4fda4-138">The logging of the service operation requests are displayed in the service's console window.</span></span> <span data-ttu-id="4fda4-139">在客户端窗口中按 Enter 可以关闭客户端。</span><span class="sxs-lookup"><span data-stu-id="4fda4-139">Press ENTER in the client window to shut down the client.</span></span>

```console
Press <ENTER> to terminate service.
Creating new service instance...
  Writing row 1 to database: Adding 100 to 0
  Writing row 2 to database: Subtracting 45 from 100
  Writing row 3 to database: Multiplying 55 by 9
  Writing row 4 to database: Dividing 495 by 15
```

<span data-ttu-id="4fda4-140">请注意，除了维护计算的运行总数外，服务还报告实例的创建（此示例中有一个实例）并将操作请求记录到数据库中。</span><span class="sxs-lookup"><span data-stu-id="4fda4-140">Note that in addition to keeping the running total of the calculations, the service reports the creation of instances (one instance for this sample) and logs the operation requests to a database.</span></span> <span data-ttu-id="4fda4-141">因为所有请求都对客户端事务进行流处理，所以只要未完成事务就会导致所有数据库操作回滚。</span><span class="sxs-lookup"><span data-stu-id="4fda4-141">Because all of the requests flow the client's transaction, any failure to complete that transaction results in all of the database operations being rolled back.</span></span> <span data-ttu-id="4fda4-142">这可以通过几种方式进行演示：</span><span class="sxs-lookup"><span data-stu-id="4fda4-142">This can be demonstrated in a number of ways:</span></span>

- <span data-ttu-id="4fda4-143">注释掉客户端对 `tx.Complete`() 的调用并重新运行 - 这将导致客户端在未完成其事务的情况下退出事务范围。</span><span class="sxs-lookup"><span data-stu-id="4fda4-143">Comment out the client's call to `tx.Complete`() and rerun - this results in the client exiting the transaction scope without completing its transaction.</span></span>

- <span data-ttu-id="4fda4-144">注释掉对 Divide 服务操作的调用 - 这将导致由 Multiply 操作启动的操作无法完成，从而使客户端事务最终也无法完成。</span><span class="sxs-lookup"><span data-stu-id="4fda4-144">Comment out the call to the Divide service operation - this results prevent the action initiated by the Multiply operation from completing and thus the client's transaction ultimately also fails to complete.</span></span>

- <span data-ttu-id="4fda4-145">在客户端事务范围内的任意位置引发未处理的异常 - 这同样会阻止客户端完成其事务。</span><span class="sxs-lookup"><span data-stu-id="4fda4-145">Throw an unhandled exception anywhere in the client's transaction scope - this similarly prevents the client from completing its transaction.</span></span>

<span data-ttu-id="4fda4-146">上述任一情况下的结果都是在该范围内执行的任何操作不会提交，持久化到数据库中的行计数也不会增加。</span><span class="sxs-lookup"><span data-stu-id="4fda4-146">The result of any of these is that none of the operations performed within that scope are committed and the count of rows persisted to the database do not increment.</span></span>

> [!NOTE]
> <span data-ttu-id="4fda4-147">作为生成过程的一部分，数据库文件被复制到 bin 文件夹中。</span><span class="sxs-lookup"><span data-stu-id="4fda4-147">As part of the build process the database file is copied to the bin folder.</span></span> <span data-ttu-id="4fda4-148">您必须查看数据库文件的副本以观察持久化到日志中的行数，而不是 Visual Studio 项目中包括的文件。</span><span class="sxs-lookup"><span data-stu-id="4fda4-148">You must look at that copy of the database file to observe the rows that are persisted to the log rather than the file that is included in the Visual Studio project.</span></span>

### <a name="to-set-up-build-and-run-the-sample"></a><span data-ttu-id="4fda4-149">设置、生成和运行示例</span><span class="sxs-lookup"><span data-stu-id="4fda4-149">To set up, build, and run the sample</span></span>

1. <span data-ttu-id="4fda4-150">确保已安装 SQL Server 2005 Express Edition 或 SQL Server 2005。</span><span class="sxs-lookup"><span data-stu-id="4fda4-150">Ensure that you have installed SQL Server 2005 Express Edition or SQL Server 2005.</span></span> <span data-ttu-id="4fda4-151">在服务的 App.config 文件中，可能设置了数据库 `connectionString`，或者通过将 appSettings `usingSql` 值设置为 `false` 而禁用了数据库交互。</span><span class="sxs-lookup"><span data-stu-id="4fda4-151">In the service's App.config file, the database `connectionString` may be set or the database interactions may be disabled by setting the appSettings `usingSql` value to `false`.</span></span>

2. <span data-ttu-id="4fda4-152">若要生成 C# 或 Visual Basic .NET 版本的解决方案，请按照 [Building the Windows Communication Foundation Samples](building-the-samples.md)中的说明进行操作。</span><span class="sxs-lookup"><span data-stu-id="4fda4-152">To build the C# or Visual Basic .NET edition of the solution, follow the instructions in [Building the Windows Communication Foundation Samples](building-the-samples.md).</span></span>

3. <span data-ttu-id="4fda4-153">若要以单机配置或跨计算机配置来运行示例，请按照 [运行 Windows Communication Foundation 示例](running-the-samples.md)中的说明进行操作。</span><span class="sxs-lookup"><span data-stu-id="4fda4-153">To run the sample in a single- or cross-machine configuration, follow the instructions in [Running the Windows Communication Foundation Samples](running-the-samples.md).</span></span>

<span data-ttu-id="4fda4-154">如果跨计算机运行此示例，则必须配置 Microsoft 分布式事务处理协调器 (MSDTC) ，以启用网络事务流，并使用 WsatConfig.exe 工具启用 Windows Communication Foundation (WCF) 事务网络支持。</span><span class="sxs-lookup"><span data-stu-id="4fda4-154">If you run the sample across machines, you must configure the Microsoft Distributed Transaction Coordinator (MSDTC) to enable network transaction flow and use the WsatConfig.exe tool to enable Windows Communication Foundation (WCF) transactions network support.</span></span>

### <a name="to-configure-the-microsoft-distributed-transaction-coordinator-msdtc-to-support-running-the-sample-across-machines"></a><span data-ttu-id="4fda4-155">配置 Microsoft 分布式事务处理协调器 (MSDTC) 以支持跨计算机运行示例</span><span class="sxs-lookup"><span data-stu-id="4fda4-155">To configure the Microsoft Distributed Transaction Coordinator (MSDTC) to support running the sample across machines</span></span>

1. <span data-ttu-id="4fda4-156">在服务计算机上，配置 MSDTC 以允许传入网络事务。</span><span class="sxs-lookup"><span data-stu-id="4fda4-156">On the service machine, configure MSDTC to allow incoming network transactions.</span></span>

    1. <span data-ttu-id="4fda4-157">从 " **开始** " 菜单，导航到 **"控制面板**"，然后依次导航到 " **管理工具**" 和 " **组件服务**"。</span><span class="sxs-lookup"><span data-stu-id="4fda4-157">From the **Start** menu, navigate to **Control Panel**, then **Administrative Tools**, and then **Component Services**.</span></span>

    2. <span data-ttu-id="4fda4-158">右键单击 **我的电脑** ，然后选择 " **属性**"。</span><span class="sxs-lookup"><span data-stu-id="4fda4-158">Right-click **My Computer** and select **Properties**.</span></span>

    3. <span data-ttu-id="4fda4-159">在 " **MSDTC** " 选项卡上，单击 " **安全配置**"。</span><span class="sxs-lookup"><span data-stu-id="4fda4-159">On the **MSDTC** tab, click **Security Configuration**.</span></span>

    4. <span data-ttu-id="4fda4-160">检查 " **网络 DTC 访问** " 和 " **允许入站**"。</span><span class="sxs-lookup"><span data-stu-id="4fda4-160">Check **Network DTC Access** and **Allow Inbound**.</span></span>

    5. <span data-ttu-id="4fda4-161">单击 **"是"** 以重新启动 MS DTC 服务，然后单击 **"确定"**。</span><span class="sxs-lookup"><span data-stu-id="4fda4-161">Click **Yes** to restart the MS DTC service and then click **OK**.</span></span>

    6. <span data-ttu-id="4fda4-162">单击 **“确定”** 关闭对话框。</span><span class="sxs-lookup"><span data-stu-id="4fda4-162">Click **OK** to close the dialog box.</span></span>

2. <span data-ttu-id="4fda4-163">在服务计算机和客户端计算机上，配置 Windows 防火墙以便在例外应用程序列表中包括 Microsoft 分布式事务处理协调器 (MSDTC)：</span><span class="sxs-lookup"><span data-stu-id="4fda4-163">On the service machine and the client machine, configure the Windows Firewall to include the Microsoft Distributed Transaction Coordinator (MSDTC) to the list of excepted applications:</span></span>

    1. <span data-ttu-id="4fda4-164">从“控制面板”上运行 Windows 防火墙应用程序。</span><span class="sxs-lookup"><span data-stu-id="4fda4-164">Run the Windows Firewall application from Control Panel.</span></span>

    2. <span data-ttu-id="4fda4-165">在 " **例外** " 选项卡中，单击 " **添加程序**"。</span><span class="sxs-lookup"><span data-stu-id="4fda4-165">From the **Exceptions** tab, click **Add Program**.</span></span>

    3. <span data-ttu-id="4fda4-166">浏览到文件夹 C:\WINDOWS\System32。</span><span class="sxs-lookup"><span data-stu-id="4fda4-166">Browse to the folder C:\WINDOWS\System32.</span></span>

    4. <span data-ttu-id="4fda4-167">选择 Msdtc.exe 并单击 " **打开**"。</span><span class="sxs-lookup"><span data-stu-id="4fda4-167">Select Msdtc.exe and click **Open**.</span></span>

    5. <span data-ttu-id="4fda4-168">单击 **"确定"** 关闭 " **添加程序** " 对话框，然后再次单击 **"确定"** 关闭 Windows 防火墙小程序。</span><span class="sxs-lookup"><span data-stu-id="4fda4-168">Click **OK** to close the **Add Program** dialog box, and click **OK** again to close the Windows Firewall applet.</span></span>

3. <span data-ttu-id="4fda4-169">在客户端计算机上，配置 MSDTC 以允许传出网络事务：</span><span class="sxs-lookup"><span data-stu-id="4fda4-169">On the client machine, configure MSDTC to allow outgoing network transactions:</span></span>

    1. <span data-ttu-id="4fda4-170">从 " **开始** " 菜单，导航到 **"控制面板**"，然后依次导航到 " **管理工具**" 和 " **组件服务**"。</span><span class="sxs-lookup"><span data-stu-id="4fda4-170">From the **Start** menu, navigate to **Control Panel**, then **Administrative Tools**, and then **Component Services**.</span></span>

    2. <span data-ttu-id="4fda4-171">右键单击 **我的电脑** ，然后选择 " **属性**"。</span><span class="sxs-lookup"><span data-stu-id="4fda4-171">Right-click **My Computer** and select **Properties**.</span></span>

    3. <span data-ttu-id="4fda4-172">在 " **MSDTC** " 选项卡上，单击 " **安全配置**"。</span><span class="sxs-lookup"><span data-stu-id="4fda4-172">On the **MSDTC** tab, click **Security Configuration**.</span></span>

    4. <span data-ttu-id="4fda4-173">检查 " **网络 DTC 访问** " 和 " **允许出站**"。</span><span class="sxs-lookup"><span data-stu-id="4fda4-173">Check **Network DTC Access** and **Allow Outbound**.</span></span>

    5. <span data-ttu-id="4fda4-174">单击 **"是"** 以重新启动 MS DTC 服务，然后单击 **"确定"**。</span><span class="sxs-lookup"><span data-stu-id="4fda4-174">Click **Yes** to restart the MS DTC service and then click **OK**.</span></span>

    6. <span data-ttu-id="4fda4-175">单击 **“确定”** 关闭对话框。</span><span class="sxs-lookup"><span data-stu-id="4fda4-175">Click **OK** to close the dialog box.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4fda4-176">您的计算机上可能已安装这些示例。</span><span class="sxs-lookup"><span data-stu-id="4fda4-176">The samples may already be installed on your machine.</span></span> <span data-ttu-id="4fda4-177">在继续操作之前，请先检查以下（默认）目录：</span><span class="sxs-lookup"><span data-stu-id="4fda4-177">Check for the following (default) directory before continuing.</span></span>
>
> `<InstallDrive>:\WF_WCF_Samples`
>
> <span data-ttu-id="4fda4-178">如果此目录不存在，请参阅[Windows Communication Foundation (wcf) ，并 Windows Workflow Foundation (的 WF](https://www.microsoft.com/download/details.aspx?id=21459)) .NET Framework Windows Communication Foundation ([!INCLUDE[wf1](../../../../includes/wf1-md.md)]</span><span class="sxs-lookup"><span data-stu-id="4fda4-178">If this directory does not exist, go to [Windows Communication Foundation (WCF) and Windows Workflow Foundation (WF) Samples for .NET Framework 4](https://www.microsoft.com/download/details.aspx?id=21459) to download all Windows Communication Foundation (WCF) and [!INCLUDE[wf1](../../../../includes/wf1-md.md)] samples.</span></span> <span data-ttu-id="4fda4-179">此示例位于以下目录：</span><span class="sxs-lookup"><span data-stu-id="4fda4-179">This sample is located in the following directory.</span></span>
>
> `<InstallDrive>:\WF_WCF_Samples\WCF\Basic\Services\Behaviors\Transactions`
