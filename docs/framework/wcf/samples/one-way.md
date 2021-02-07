---
description: 了解详细信息： One-Way
title: 单向
ms.date: 03/30/2017
ms.assetid: 74e3e03d-cd15-4191-a6a5-1efa2dcb9e73
ms.openlocfilehash: fef940f6e0787b7dc91f02442597625b8c4cca50
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99726281"
---
# <a name="one-way"></a><span data-ttu-id="b948f-103">单向</span><span class="sxs-lookup"><span data-stu-id="b948f-103">One-Way</span></span>

<span data-ttu-id="b948f-104">此示例演示具有单向服务操作的服务协定。</span><span class="sxs-lookup"><span data-stu-id="b948f-104">This sample demonstrates a service contact with one-way service operations.</span></span> <span data-ttu-id="b948f-105">客户端不会像在双向服务操作中那样等待服务操作完成。</span><span class="sxs-lookup"><span data-stu-id="b948f-105">The client does not wait for service operations to complete as is the case with two-way service operations.</span></span> <span data-ttu-id="b948f-106">此示例基于 [入门](getting-started-sample.md) ，并使用 `wsHttpBinding` 绑定。</span><span class="sxs-lookup"><span data-stu-id="b948f-106">This sample is based on the [Getting Started](getting-started-sample.md) and uses the `wsHttpBinding` binding.</span></span> <span data-ttu-id="b948f-107">此示例中的服务是自承载控制台应用程序，通过它可以观察接收和处理请求的服务。</span><span class="sxs-lookup"><span data-stu-id="b948f-107">The service in this sample is a self-hosted console application to enable you to observe the service that receives and processes requests.</span></span> <span data-ttu-id="b948f-108">客户端也是一个控制台应用程序。</span><span class="sxs-lookup"><span data-stu-id="b948f-108">The client is also a console application.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="b948f-109">本主题的最后介绍了此示例的设置过程和生成说明。</span><span class="sxs-lookup"><span data-stu-id="b948f-109">The setup procedure and build instructions for this sample are located at the end of this topic.</span></span>  
  
 <span data-ttu-id="b948f-110">若要创建单向服务协定，请定义服务协定，将 <xref:System.ServiceModel.OperationContractAttribute> 类应用于每个操作，并将 <xref:System.ServiceModel.OperationContractAttribute.IsOneWay%2A> 设置为 `true`，如下面的示例代码所示：</span><span class="sxs-lookup"><span data-stu-id="b948f-110">To create a one-way service contract, define your service contract, apply the <xref:System.ServiceModel.OperationContractAttribute> class to each operation, and set <xref:System.ServiceModel.OperationContractAttribute.IsOneWay%2A> to `true` as shown in the following sample code:</span></span>  
  
```csharp
[ServiceContract(Namespace="http://Microsoft.ServiceModel.Samples")]  
public interface IOneWayCalculator  
{  
    [OperationContract(IsOneWay=true)]  
    void Add(double n1, double n2);  
    [OperationContract(IsOneWay = true)]  
    void Subtract(double n1, double n2);  
    [OperationContract(IsOneWay = true)]  
    void Multiply(double n1, double n2);  
    [OperationContract(IsOneWay = true)]  
    void Divide(double n1, double n2);  
}  
```  
  
 <span data-ttu-id="b948f-111">为了演示客户端不会等待服务操作完成，此示例中的服务代码实现了五秒钟的延迟，如下面的示例代码所示：</span><span class="sxs-lookup"><span data-stu-id="b948f-111">To demonstrate that the client does not wait for the service operations to complete, the service code in this sample implements a five-second delay, as shown in the following sample code:</span></span>  
  
```csharp
// This service class implements the service contract.  
// This code writes output to the console window.  
 [ServiceBehavior(ConcurrencyMode = ConcurrencyMode.Multiple,  
    InstanceContextMode = InstanceContextMode.PerCall)]  
public class CalculatorService : IOneWayCalculator  
{  
    public void Add(double n1, double n2)  
    {  
        Console.WriteLine("Received Add({0},{1}) - sleeping", n1, n2);  
        System.Threading.Thread.Sleep(1000 * 5);  
        double result = n1 + n2;  
        Console.WriteLine("Processing Add({0},{1}) - result: {2}", n1, n2, result);  
    }  
    ...  
}  
```  
  
 <span data-ttu-id="b948f-112">当客户端调用服务时，调用不等待服务操作完成即返回。</span><span class="sxs-lookup"><span data-stu-id="b948f-112">When the client calls the service, the call returns without waiting for the service operation to complete.</span></span>  
  
 <span data-ttu-id="b948f-113">运行示例时，客户端和服务活动将显示在服务和客户端控制台窗口中。</span><span class="sxs-lookup"><span data-stu-id="b948f-113">When you run the sample, the client and service activities are displayed in both the service and client console windows.</span></span> <span data-ttu-id="b948f-114">您可以看到服务从客户端接收消息。</span><span class="sxs-lookup"><span data-stu-id="b948f-114">You can see the service receive messages from the client.</span></span> <span data-ttu-id="b948f-115">在每个控制台窗口中按 Enter 可以同时关闭服务和客户端。</span><span class="sxs-lookup"><span data-stu-id="b948f-115">Press ENTER in each console window to shut down both the service and the client.</span></span>  
  
 <span data-ttu-id="b948f-116">客户端在服务之前完成，说明了客户端没有等待单向服务操作完成。</span><span class="sxs-lookup"><span data-stu-id="b948f-116">The client finishes ahead of the service, demonstrating that a client does not wait for one-way service operations to complete.</span></span> <span data-ttu-id="b948f-117">客户端输出如下所示：</span><span class="sxs-lookup"><span data-stu-id="b948f-117">The client output is as follows:</span></span>  
  
```console  
Add(100,15.99)  
Subtract(145,76.54)  
Multiply(9,81.25)  
Divide(22,7)  
  
Press <ENTER> to terminate client.  
```  
  
 <span data-ttu-id="b948f-118">服务输出如下所示：</span><span class="sxs-lookup"><span data-stu-id="b948f-118">The following service output is shown:</span></span>  
  
```console  
The service is ready.  
Press <ENTER> to terminate service.  
  
Received Add(100,15.99) - sleeping  
Received Subtract(145,76.54) - sleeping  
Received Multiply(9,81.25) - sleeping  
Received Divide(22,7) - sleeping  
Processing Add(100,15.99) - result: 115.99  
Processing Subtract(145,76.54) - result: 68.46  
Processing Multiply(9,81.25) - result: 731.25  
Processing Divide(22,7) - result: 3.14285714285714  
```  
  
> [!NOTE]
> <span data-ttu-id="b948f-119">HTTP 从定义上讲是一个请求/响应协议；当发出请求时，即返回响应。</span><span class="sxs-lookup"><span data-stu-id="b948f-119">HTTP is, by definition, a request/response protocol; when a request is made, a response is returned.</span></span> <span data-ttu-id="b948f-120">即使对于通过 HTTP 公开的单向服务操作，也是如此。</span><span class="sxs-lookup"><span data-stu-id="b948f-120">This is true even for a one-way service operation that is exposed over HTTP.</span></span> <span data-ttu-id="b948f-121">当调用操作时，服务在执行服务操作之前返回 HTTP 状态码 202。</span><span class="sxs-lookup"><span data-stu-id="b948f-121">When the operation is called, the service returns an HTTP status code of 202 before the service operation has executed.</span></span> <span data-ttu-id="b948f-122">此状态码表示请求已被接受进行处理，但处理尚未完成。</span><span class="sxs-lookup"><span data-stu-id="b948f-122">This status code means that the request has been accepted for processing, but the processing has not yet been completed.</span></span> <span data-ttu-id="b948f-123">调用操作的客户端在从服务收到 202 响应之前处于阻止状态。</span><span class="sxs-lookup"><span data-stu-id="b948f-123">The client that called the operation blocks until it receives the 202 response from the service.</span></span> <span data-ttu-id="b948f-124">当使用绑定（配置为使用会话）发送多个单向消息时，这可能会产生某些意外行为。</span><span class="sxs-lookup"><span data-stu-id="b948f-124">This can cause some unexpected behavior when multiple one-way messages are sent using a binding that is configured to use sessions.</span></span> <span data-ttu-id="b948f-125">此示例中使用的 `wsHttpBinding` 绑定配置为默认使用会话来建立安全上下文。</span><span class="sxs-lookup"><span data-stu-id="b948f-125">The `wsHttpBinding` binding used in this sample is configured to use sessions by default to establish a security context.</span></span> <span data-ttu-id="b948f-126">默认情况下，会话中的消息一定会按照它们的发送顺序到达。</span><span class="sxs-lookup"><span data-stu-id="b948f-126">By default, messages in a session are guaranteed to arrive in the order in which they are sent.</span></span> <span data-ttu-id="b948f-127">因此，当发送会话中的第二个消息时，在处理完第一个消息之前不会处理第二个消息。</span><span class="sxs-lookup"><span data-stu-id="b948f-127">Because of this, when the second message in a session is sent, it is not processed until the first message has been processed.</span></span> <span data-ttu-id="b948f-128">这样的结果是，在处理完上一个消息之前，客户端不会收到消息的 202 响应。</span><span class="sxs-lookup"><span data-stu-id="b948f-128">The result of this is that the client does not receive the 202 response for a message until the processing of the previous message has been completed.</span></span> <span data-ttu-id="b948f-129">因此，客户端似乎是阻止了每个后续的操作调用。</span><span class="sxs-lookup"><span data-stu-id="b948f-129">The client therefore appears to block on each subsequent operation call.</span></span> <span data-ttu-id="b948f-130">为了避免此行为，此示例对运行库进行了配置，以便将消息并发调度给不同的实例进行处理。</span><span class="sxs-lookup"><span data-stu-id="b948f-130">To avoid this behavior, this sample configures the runtime to dispatch messages concurrently to distinct instances for processing.</span></span> <span data-ttu-id="b948f-131">本示例将 <xref:System.ServiceModel.ServiceBehaviorAttribute.InstanceContextMode%2A> 设置为 `PerCall`，以使每条消息可以由不同的实例来处理。</span><span class="sxs-lookup"><span data-stu-id="b948f-131">The sample sets <xref:System.ServiceModel.ServiceBehaviorAttribute.InstanceContextMode%2A> to `PerCall` so that each message can be processed by a different instance.</span></span> <span data-ttu-id="b948f-132"><xref:System.ServiceModel.ServiceBehaviorAttribute.ConcurrencyMode%2A> 设置为 `Multiple`，以允许多个线程同时调度消息。</span><span class="sxs-lookup"><span data-stu-id="b948f-132"><xref:System.ServiceModel.ServiceBehaviorAttribute.ConcurrencyMode%2A> is set to `Multiple` to allow more than one thread to dispatch messages at a time.</span></span>  
  
### <a name="to-set-up-build-and-run-the-sample"></a><span data-ttu-id="b948f-133">设置、生成和运行示例</span><span class="sxs-lookup"><span data-stu-id="b948f-133">To set up, build, and run the sample</span></span>  
  
1. <span data-ttu-id="b948f-134">确保已对 [Windows Communication Foundation 示例执行了一次性安装过程](one-time-setup-procedure-for-the-wcf-samples.md)。</span><span class="sxs-lookup"><span data-stu-id="b948f-134">Ensure that you have performed the [One-Time Setup Procedure for the Windows Communication Foundation Samples](one-time-setup-procedure-for-the-wcf-samples.md).</span></span>  
  
2. <span data-ttu-id="b948f-135">若要生成 C# 或 Visual Basic .NET 版本的解决方案，请按照 [Building the Windows Communication Foundation Samples](building-the-samples.md)中的说明进行操作。</span><span class="sxs-lookup"><span data-stu-id="b948f-135">To build the C# or Visual Basic .NET edition of the solution, follow the instructions in [Building the Windows Communication Foundation Samples](building-the-samples.md).</span></span>  
  
3. <span data-ttu-id="b948f-136">若要以单机配置或跨计算机配置来运行示例，请按照 [运行 Windows Communication Foundation 示例](running-the-samples.md)中的说明进行操作。</span><span class="sxs-lookup"><span data-stu-id="b948f-136">To run the sample in a single- or cross-machine configuration, follow the instructions in [Running the Windows Communication Foundation Samples](running-the-samples.md).</span></span>  
  
> [!NOTE]
> <span data-ttu-id="b948f-137">请在运行客户端之前运行服务，并在关闭服务之前关闭客户端。</span><span class="sxs-lookup"><span data-stu-id="b948f-137">Run the service before you run the client and shut down the client before shutting down the service.</span></span> <span data-ttu-id="b948f-138">这样可以避免当客户端由于服务已关闭而无法彻底关闭安全会话时出现客户端异常。</span><span class="sxs-lookup"><span data-stu-id="b948f-138">This avoids a client exception when the client cannot close the security session cleanly because the service is gone.</span></span>  
  
> [!IMPORTANT]
> <span data-ttu-id="b948f-139">您的计算机上可能已安装这些示例。</span><span class="sxs-lookup"><span data-stu-id="b948f-139">The samples may already be installed on your machine.</span></span> <span data-ttu-id="b948f-140">在继续操作之前，请先检查以下（默认）目录：</span><span class="sxs-lookup"><span data-stu-id="b948f-140">Check for the following (default) directory before continuing.</span></span>  
>
> `<InstallDrive>:\WF_WCF_Samples`  
>
> <span data-ttu-id="b948f-141">如果此目录不存在，请参阅[Windows Communication Foundation (wcf) ，并 Windows Workflow Foundation (的 WF](https://www.microsoft.com/download/details.aspx?id=21459)) .NET Framework Windows Communication Foundation ([!INCLUDE[wf1](../../../../includes/wf1-md.md)]</span><span class="sxs-lookup"><span data-stu-id="b948f-141">If this directory does not exist, go to [Windows Communication Foundation (WCF) and Windows Workflow Foundation (WF) Samples for .NET Framework 4](https://www.microsoft.com/download/details.aspx?id=21459) to download all Windows Communication Foundation (WCF) and [!INCLUDE[wf1](../../../../includes/wf1-md.md)] samples.</span></span> <span data-ttu-id="b948f-142">此示例位于以下目录：</span><span class="sxs-lookup"><span data-stu-id="b948f-142">This sample is located in the following directory.</span></span>  
>
> `<InstallDrive>:\WF_WCF_Samples\WCF\Basic\Contract\Service\Oneway`  
