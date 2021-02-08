---
description: 了解详细信息：如何：使用通道工厂以异步方式调用操作
title: 如何：使用通道工厂以异步方式调用操作
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: cc17dd47-b9ad-451c-a362-e36e0aac7ba0
ms.openlocfilehash: 081211d0202550e93e3aabb5c8b5b5b5adbcdcde
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99780188"
---
# <a name="how-to-call-operations-asynchronously-using-a-channel-factory"></a><span data-ttu-id="fbcf4-103">如何：使用通道工厂以异步方式调用操作</span><span class="sxs-lookup"><span data-stu-id="fbcf4-103">How to: Call Operations Asynchronously Using a Channel Factory</span></span>

<span data-ttu-id="fbcf4-104">本主题介绍客户端如何在使用基于 <xref:System.ServiceModel.ChannelFactory%601> 的客户端应用程序时以异步方式访问服务操作。</span><span class="sxs-lookup"><span data-stu-id="fbcf4-104">This topic covers how a client can access a service operation asynchronously when using a <xref:System.ServiceModel.ChannelFactory%601>-based client application.</span></span> <span data-ttu-id="fbcf4-105">（当使用 <xref:System.ServiceModel.ClientBase%601?displayProperty=nameWithType> 对象调用服务时，可以使用事件驱动的异步调用模型。</span><span class="sxs-lookup"><span data-stu-id="fbcf4-105">(When using a <xref:System.ServiceModel.ClientBase%601?displayProperty=nameWithType> object to invoke a service you can use the event-driven asynchronous calling model.</span></span> <span data-ttu-id="fbcf4-106">有关详细信息，请参阅 [如何：异步调用服务操作](how-to-call-wcf-service-operations-asynchronously.md)。</span><span class="sxs-lookup"><span data-stu-id="fbcf4-106">For more information, see [How to: Call Service Operations Asynchronously](how-to-call-wcf-service-operations-asynchronously.md).</span></span> <span data-ttu-id="fbcf4-107">有关基于事件的异步调用模型的详细信息，请参阅 [基于事件的异步模式 (EAP) ](../../../standard/asynchronous-programming-patterns/event-based-asynchronous-pattern-eap.md)。 ) </span><span class="sxs-lookup"><span data-stu-id="fbcf4-107">For more information about the event-based asynchronous calling model, see [Event-based Asynchronous Pattern (EAP)](../../../standard/asynchronous-programming-patterns/event-based-asynchronous-pattern-eap.md).)</span></span>  
  
 <span data-ttu-id="fbcf4-108">本主题中的服务可实现 `ICalculator` 接口。</span><span class="sxs-lookup"><span data-stu-id="fbcf4-108">The service in this topic implements the `ICalculator` interface.</span></span> <span data-ttu-id="fbcf4-109">客户端可以在此接口上以异步方式调用操作，这意味着像 `Add` 这样的操作将拆分为两个方法：`BeginAdd` 和 `EndAdd`。前一个方法启动调用，而后一个方法在操作完成时检索结果。</span><span class="sxs-lookup"><span data-stu-id="fbcf4-109">The client can call the operations on this interface asynchronously, which means that operations like `Add` are split into two methods, `BeginAdd` and `EndAdd`, the former of which initiates the call and the latter of which retrieves the result when the operation completes.</span></span> <span data-ttu-id="fbcf4-110">有关演示如何在服务中异步实现操作的示例，请参阅 [如何：实现异步服务操作](../how-to-implement-an-asynchronous-service-operation.md)。</span><span class="sxs-lookup"><span data-stu-id="fbcf4-110">For an example showing how to implement an operation asynchronously in a service, see [How to: Implement an Asynchronous Service Operation](../how-to-implement-an-asynchronous-service-operation.md).</span></span> <span data-ttu-id="fbcf4-111">有关同步和异步操作的详细信息，请参阅 [同步和异步操作](../synchronous-and-asynchronous-operations.md)。</span><span class="sxs-lookup"><span data-stu-id="fbcf4-111">For details about synchronous and asynchronous operations, see [Synchronous and Asynchronous Operations](../synchronous-and-asynchronous-operations.md).</span></span>  
  
## <a name="procedure"></a><span data-ttu-id="fbcf4-112">过程</span><span class="sxs-lookup"><span data-stu-id="fbcf4-112">Procedure</span></span>  
  
#### <a name="to-call-wcf-service-operations-asynchronously"></a><span data-ttu-id="fbcf4-113">以异步方式调用 WCF 服务操作</span><span class="sxs-lookup"><span data-stu-id="fbcf4-113">To call WCF service operations asynchronously</span></span>  
  
1. <span data-ttu-id="fbcf4-114">运行 "工作身份 [数据" 实用工具工具 ( # A0) ](../servicemodel-metadata-utility-tool-svcutil-exe.md) 工具和 `/async` 选项，如以下命令中所示。</span><span class="sxs-lookup"><span data-stu-id="fbcf4-114">Run the [ServiceModel Metadata Utility Tool (Svcutil.exe)](../servicemodel-metadata-utility-tool-svcutil-exe.md) tool with the `/async` option as shown in the following command.</span></span>  
  
    ```console
    svcutil /n:http://Microsoft.ServiceModel.Samples,Microsoft.ServiceModel.Samples http://localhost:8000/servicemodelsamples/service/mex /a  
    ```  
  
     <span data-ttu-id="fbcf4-115">这将生成该操作的服务协定的异步客户端版本。</span><span class="sxs-lookup"><span data-stu-id="fbcf4-115">This generates an asynchronous client version of the service contract for the operation.</span></span>  
  
2. <span data-ttu-id="fbcf4-116">创建一个异步操作完成时将要调用的回调函数，如下面的示例代码所示。</span><span class="sxs-lookup"><span data-stu-id="fbcf4-116">Create a callback function to be called when the asynchronous operation is complete, as shown in the following sample code.</span></span>  
  
     [!code-csharp[C_How_To_CF_Async#2](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_how_to_cf_async/cs/client.cs#2)]
     [!code-vb[C_How_To_CF_Async#2](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/c_how_to_cf_async/vb/client.vb#2)]  
  
3. <span data-ttu-id="fbcf4-117">若要以异步方式访问服务操作，请创建客户端、调用 `Begin[Operation]`（例如 `BeginAdd`），并指定一个回调函数，如下面的示例代码所示。</span><span class="sxs-lookup"><span data-stu-id="fbcf4-117">To access a service operation asynchronously, create the client and call the `Begin[Operation]` (for example, `BeginAdd`) and specify a callback function, as shown in the following sample code.</span></span>  
  
     [!code-csharp[C_How_To_CF_Async#3](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_how_to_cf_async/cs/client.cs#3)]
     [!code-vb[C_How_To_CF_Async#3](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/c_how_to_cf_async/vb/client.vb#3)]  
  
     <span data-ttu-id="fbcf4-118">执行该回调函数时，客户端将调用 `End<operation>`（例如 `EndAdd`）以检索结果。</span><span class="sxs-lookup"><span data-stu-id="fbcf4-118">When the callback function executes, the client calls `End<operation>` (for example, `EndAdd`) to retrieve the result.</span></span>  
  
## <a name="example"></a><span data-ttu-id="fbcf4-119">示例</span><span class="sxs-lookup"><span data-stu-id="fbcf4-119">Example</span></span>  

 <span data-ttu-id="fbcf4-120">上面过程中的客户端代码使用的服务可实现 `ICalculator` 接口，如下面的代码所示。</span><span class="sxs-lookup"><span data-stu-id="fbcf4-120">The service that is used with the client code that is used in the preceding procedure implements the `ICalculator` interface as shown in the following code.</span></span> <span data-ttu-id="fbcf4-121">在服务端， `Add` `Subtract` 通过 WINDOWS COMMUNICATION FOUNDATION (WCF) 运行时同步调用协定的和操作，即使在客户端上异步调用了前面的客户端步骤。</span><span class="sxs-lookup"><span data-stu-id="fbcf4-121">On the service side, the `Add` and `Subtract` operations of the contract are invoked synchronously by the Windows Communication Foundation (WCF) run time, even though the preceding client steps are invoked asynchronously on the client.</span></span> <span data-ttu-id="fbcf4-122">在服务端，`Multiply` 和 `Divide` 操作用于在服务端以异步方式调用服务，即使客户端以同步方式调用这两个操作也是如此。</span><span class="sxs-lookup"><span data-stu-id="fbcf4-122">The `Multiply` and `Divide` operations are used to invoke the service asynchronously on the service side, even if the client invokes them synchronously.</span></span> <span data-ttu-id="fbcf4-123">此示例将 <xref:System.ServiceModel.OperationContractAttribute.AsyncPattern%2A> 属性设置为 `true`。</span><span class="sxs-lookup"><span data-stu-id="fbcf4-123">This example sets the <xref:System.ServiceModel.OperationContractAttribute.AsyncPattern%2A> property to `true`.</span></span> <span data-ttu-id="fbcf4-124">此属性设置与 .NET Framework 异步模式的实现相结合，告诉运行时异步调用操作。</span><span class="sxs-lookup"><span data-stu-id="fbcf4-124">This property setting, in combination with the implementation of the .NET Framework asynchronous pattern, tells the run time to invoke the operation asynchronously.</span></span>  
  
 [!code-csharp[C_How_To_CF_Async#4](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_how_to_cf_async/cs/service.cs#4)]
 [!code-vb[C_How_To_CF_Async#4](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/c_how_to_cf_async/vb/service.vb#4)]  
