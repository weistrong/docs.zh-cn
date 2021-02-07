---
description: 了解详细信息：预期异常
title: 预期异常
ms.date: 03/30/2017
ms.assetid: 299a6987-ae6b-43c6-987f-12b034b583ae
ms.openlocfilehash: 9ccb857da76143a37ed520f2fac8c515b332a565
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99752400"
---
# <a name="expected-exceptions"></a><span data-ttu-id="9dd9c-103">预期异常</span><span class="sxs-lookup"><span data-stu-id="9dd9c-103">Expected Exceptions</span></span>

<span data-ttu-id="9dd9c-104">此示例演示如何在使用类型化客户端时捕获预期异常。</span><span class="sxs-lookup"><span data-stu-id="9dd9c-104">This sample demonstrates how to catch expected exceptions when using a typed client.</span></span> <span data-ttu-id="9dd9c-105">此示例基于实现计算器服务的 [入门](getting-started-sample.md) 。</span><span class="sxs-lookup"><span data-stu-id="9dd9c-105">This sample is based on the [Getting Started](getting-started-sample.md) that implements a calculator service.</span></span> <span data-ttu-id="9dd9c-106">在此示例中，客户端是一个控制台应用程序 (.exe)，服务是由 Internet 信息服务 (IIS) 承载的。</span><span class="sxs-lookup"><span data-stu-id="9dd9c-106">In this sample, the client is a console application (.exe) and the service is hosted by Internet Information Services (IIS).</span></span>  
  
> [!NOTE]
> <span data-ttu-id="9dd9c-107">本主题的最后介绍了此示例的设置过程和生成说明。</span><span class="sxs-lookup"><span data-stu-id="9dd9c-107">The setup procedure and build instructions for this sample are located at the end of this topic.</span></span>  
  
 <span data-ttu-id="9dd9c-108">此示例演示如何捕获和处理正确的程序所必须处理的两个预期异常类型：`TimeoutException` 和 `CommunicationException`。</span><span class="sxs-lookup"><span data-stu-id="9dd9c-108">This sample demonstrates catching and handling the two expected exception types that correct programs must handle: `TimeoutException` and `CommunicationException`.</span></span>  
  
 <span data-ttu-id="9dd9c-109">Windows Communication Foundation (WCF) 客户端的通信方法引发的异常可能是预期的，也可能是意外的。</span><span class="sxs-lookup"><span data-stu-id="9dd9c-109">Exceptions that are thrown from communication methods on a Windows Communication Foundation (WCF) client are either expected or unexpected.</span></span> <span data-ttu-id="9dd9c-110">意外异常包括灾难性故障（如 `OutOfMemoryException`）和编程错误（如 `ArgumentNullException` 或 `InvalidOperationException`）。</span><span class="sxs-lookup"><span data-stu-id="9dd9c-110">Unexpected exceptions include catastrophic failures like `OutOfMemoryException` and programming errors like `ArgumentNullException` or `InvalidOperationException`.</span></span> <span data-ttu-id="9dd9c-111">通常不会有任何有用的方法来处理意外错误，因此，通常不应在调用 WCF 客户端通信方法时捕获它们。</span><span class="sxs-lookup"><span data-stu-id="9dd9c-111">Typically there is no useful way to handle unexpected errors, so typically you should not catch them when calling a WCF client communication method.</span></span>  
  
 <span data-ttu-id="9dd9c-112">WCF 客户端上通信方法的预期异常包括 `TimeoutException` 、 `CommunicationException` 和的任何派生类 `CommunicationException` 。</span><span class="sxs-lookup"><span data-stu-id="9dd9c-112">Expected exceptions from communication methods on a WCF client include `TimeoutException`, `CommunicationException`, and any derived class of `CommunicationException`.</span></span> <span data-ttu-id="9dd9c-113">这表示在通信过程中出现的问题，可通过中止 WCF 客户端并报告通信故障来安全地处理这些问题。</span><span class="sxs-lookup"><span data-stu-id="9dd9c-113">These indicate a problem during communication that can be safely handled by aborting the WCF client and reporting a communication failure.</span></span> <span data-ttu-id="9dd9c-114">因为外部因素可能导致任何应用程序中出现这些错误，所以正确的应用程序必须捕获这些异常并在发生异常时进行恢复。</span><span class="sxs-lookup"><span data-stu-id="9dd9c-114">Because external factors can cause these errors in any application, correct applications must catch these exceptions and recover when they occur.</span></span>  
  
 <span data-ttu-id="9dd9c-115">客户端可以引发 `CommunicationException` 的几个派生类。</span><span class="sxs-lookup"><span data-stu-id="9dd9c-115">There are several derived classes of `CommunicationException` that a client can throw.</span></span> <span data-ttu-id="9dd9c-116">在某些情况下，应用程序也会捕获其中的某些类以执行特殊的处理，而让其他类作为 `CommunicationException` 进行处理。</span><span class="sxs-lookup"><span data-stu-id="9dd9c-116">In some cases, applications also catch some of these to do special handling, but let the others be handled as a `CommunicationException`.</span></span> <span data-ttu-id="9dd9c-117">这可以通过先捕获比较具体的异常类型，然后在稍后的 catch 子句中捕获 `CommunicationException` 来完成。</span><span class="sxs-lookup"><span data-stu-id="9dd9c-117">This can be accomplished by catching the more specific exception type first and then catching `CommunicationException` in a later catch-clause.</span></span>  
  
 <span data-ttu-id="9dd9c-118">调用客户端通信方法的代码必须捕获 `TimeoutException` 和 `CommunicationException`。</span><span class="sxs-lookup"><span data-stu-id="9dd9c-118">Code that calls a client communication method must catch the `TimeoutException` and `CommunicationException`.</span></span> <span data-ttu-id="9dd9c-119">处理此类错误的一种方法是中止客户端并报告通信故障。</span><span class="sxs-lookup"><span data-stu-id="9dd9c-119">One way to handle such errors is to abort the client and report the communication failure.</span></span>  
  
```csharp
try  
{  
    ...  
    double result = client.Add(value1, value2);  
    ...  
    client.Close();  
}  
catch (TimeoutException exception)  
{  
    Console.WriteLine("Got {0}", exception.GetType());  
    client.Abort();  
}  
catch (CommunicationException exception)  
{  
    Console.WriteLine("Got {0}", exception.GetType());  
    client.Abort();  
}  
```  
  
 <span data-ttu-id="9dd9c-120">如果发生预期异常，客户端或许可以继续使用，或许无法继续使用。</span><span class="sxs-lookup"><span data-stu-id="9dd9c-120">If an expected exception occurs, the client may or may not be usable afterwards.</span></span> <span data-ttu-id="9dd9c-121">若要确定客户端是否仍然可以使用，请检查 `State` 属性是否为 `CommunicationState`.Opened。</span><span class="sxs-lookup"><span data-stu-id="9dd9c-121">To determine if the client is still usable, check that the `State` property is `CommunicationState`.Opened.</span></span> <span data-ttu-id="9dd9c-122">如果此属性仍然处于打开状态，则客户端仍然可以使用。</span><span class="sxs-lookup"><span data-stu-id="9dd9c-122">If it is still opened, then it is still usable.</span></span> <span data-ttu-id="9dd9c-123">否则，则应中止客户端并释放对其的所有引用。</span><span class="sxs-lookup"><span data-stu-id="9dd9c-123">Otherwise you should abort the client and release all references to it.</span></span>  
  
> [!CAUTION]
> <span data-ttu-id="9dd9c-124">您可能注意到具有会话的客户端在出现异常后常常不能再使用，而没有会话的客户端在出现异常后常常可以继续使用。</span><span class="sxs-lookup"><span data-stu-id="9dd9c-124">You may observe that clients that have a session are often no longer usable after an exception, and clients that do not have a session are often still usable after an exception.</span></span> <span data-ttu-id="9dd9c-125">但是，这些情况都是不能保证的，因此如果您希望在出现异常后继续使用客户端，您的应用程序应检查 `State` 属性以验证客户端是否仍然处于打开状态。</span><span class="sxs-lookup"><span data-stu-id="9dd9c-125">However, neither of these is guaranteed, so if you want to try to continue using the client after an exception your application should check the `State` property to verify the client is still opened.</span></span>  
  
 <span data-ttu-id="9dd9c-126">运行示例时，在客户端控制台窗口中显示操作响应和异常。</span><span class="sxs-lookup"><span data-stu-id="9dd9c-126">When you run the sample, the operation responses and exceptions are displayed in the client console window.</span></span>  
  
 <span data-ttu-id="9dd9c-127">客户端进程运行两个方案，每个方案都尝试先调用 `Add`，再调用 `Divide`。</span><span class="sxs-lookup"><span data-stu-id="9dd9c-127">The client process runs two scenarios, each of which attempts to call `Add` followed by `Divide`.</span></span> <span data-ttu-id="9dd9c-128">第一个方案通过在调用 `Divide` 之前中止客户端来模拟网络问题。</span><span class="sxs-lookup"><span data-stu-id="9dd9c-128">The first scenario simulates a network issue by aborting the client before making the call to `Divide`.</span></span> <span data-ttu-id="9dd9c-129">第二个方案通过将超时设置为太短的时间而使方法无法完成，从而导致超时情况的发生。</span><span class="sxs-lookup"><span data-stu-id="9dd9c-129">The second scenario causes a timeout condition by setting the timeout too short for the method to complete.</span></span> <span data-ttu-id="9dd9c-130">客户端进程的预期输出为：</span><span class="sxs-lookup"><span data-stu-id="9dd9c-130">The expected output from the client process is:</span></span>  
  
```output
Add(100,15.99) = 115.99  
Simulated network problem occurs...  
Got System.ServiceModel.CommunicationObjectAbortedException  
Add(100,15.99) = 115.99  
Set timeout too short for method to complete...  
Got System.TimeoutException  
```  
  
### <a name="to-set-up-build-and-run-the-sample"></a><span data-ttu-id="9dd9c-131">设置、生成和运行示例</span><span class="sxs-lookup"><span data-stu-id="9dd9c-131">To set up, build, and run the sample</span></span>  
  
1. <span data-ttu-id="9dd9c-132">确保已对 [Windows Communication Foundation 示例执行了一次性安装过程](one-time-setup-procedure-for-the-wcf-samples.md)。</span><span class="sxs-lookup"><span data-stu-id="9dd9c-132">Ensure that you have performed the [One-Time Setup Procedure for the Windows Communication Foundation Samples](one-time-setup-procedure-for-the-wcf-samples.md).</span></span>  
  
2. <span data-ttu-id="9dd9c-133">若要生成 C# 或 Visual Basic .NET 版本的解决方案，请按照 [Building the Windows Communication Foundation Samples](building-the-samples.md)中的说明进行操作。</span><span class="sxs-lookup"><span data-stu-id="9dd9c-133">To build the C# or Visual Basic .NET edition of the solution, follow the instructions in [Building the Windows Communication Foundation Samples](building-the-samples.md).</span></span>  
  
3. <span data-ttu-id="9dd9c-134">若要以单机配置或跨计算机配置来运行示例，请按照 [运行 Windows Communication Foundation 示例](running-the-samples.md)中的说明进行操作。</span><span class="sxs-lookup"><span data-stu-id="9dd9c-134">To run the sample in a single- or cross-machine configuration, follow the instructions in [Running the Windows Communication Foundation Samples](running-the-samples.md).</span></span>  
  
> [!IMPORTANT]
> <span data-ttu-id="9dd9c-135">您的计算机上可能已安装这些示例。</span><span class="sxs-lookup"><span data-stu-id="9dd9c-135">The samples may already be installed on your machine.</span></span> <span data-ttu-id="9dd9c-136">在继续操作之前，请先检查以下（默认）目录：</span><span class="sxs-lookup"><span data-stu-id="9dd9c-136">Check for the following (default) directory before continuing.</span></span>  
>
> `<InstallDrive>:\WF_WCF_Samples`  
>
> <span data-ttu-id="9dd9c-137">如果此目录不存在，请参阅[Windows Communication Foundation (wcf) ，并 Windows Workflow Foundation (的 WF](https://www.microsoft.com/download/details.aspx?id=21459)) .NET Framework Windows Communication Foundation ([!INCLUDE[wf1](../../../../includes/wf1-md.md)]</span><span class="sxs-lookup"><span data-stu-id="9dd9c-137">If this directory does not exist, go to [Windows Communication Foundation (WCF) and Windows Workflow Foundation (WF) Samples for .NET Framework 4](https://www.microsoft.com/download/details.aspx?id=21459) to download all Windows Communication Foundation (WCF) and [!INCLUDE[wf1](../../../../includes/wf1-md.md)] samples.</span></span> <span data-ttu-id="9dd9c-138">此示例位于以下目录：</span><span class="sxs-lookup"><span data-stu-id="9dd9c-138">This sample is located in the following directory.</span></span>  
>
> `<InstallDrive>:\WF_WCF_Samples\WCF\Basic\Client\ExpectedExceptions`  
