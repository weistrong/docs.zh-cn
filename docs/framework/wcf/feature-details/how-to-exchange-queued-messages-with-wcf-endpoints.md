---
description: 了解详细信息：如何：与 WCF 终结点交换排队消息
title: 如何：使用 WCF 终结点交换排队消息
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 938e7825-f63a-4c3d-b603-63772fabfdb3
ms.openlocfilehash: fe7195719c57454cb0035c1b6f06134cf3380a46
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99802887"
---
# <a name="how-to-exchange-queued-messages-with-wcf-endpoints"></a><span data-ttu-id="97da1-103">如何：使用 WCF 终结点交换排队消息</span><span class="sxs-lookup"><span data-stu-id="97da1-103">How to: Exchange Queued Messages with WCF Endpoints</span></span>

<span data-ttu-id="97da1-104">队列确保客户端与 Windows Communication Foundation (WCF) 服务之间可以发生可靠消息传送，即使该服务在通信时不可用。</span><span class="sxs-lookup"><span data-stu-id="97da1-104">Queues ensure that reliable messaging can occur between a client and a Windows Communication Foundation (WCF) service, even if the service is not available at the time of communication.</span></span> <span data-ttu-id="97da1-105">下面的过程演示如何通过在实现 WCF 服务时使用标准排队绑定来确保客户端和服务之间的持久通信。</span><span class="sxs-lookup"><span data-stu-id="97da1-105">The following procedures show how to ensure durable communication between a client and a service by using the standard queued binding when implementing the WCF service.</span></span>  
  
 <span data-ttu-id="97da1-106">本部分介绍如何将 <xref:System.ServiceModel.NetMsmqBinding> 用于 wcf 客户端和 wcf 服务之间的排队通信。</span><span class="sxs-lookup"><span data-stu-id="97da1-106">This section explains how to use <xref:System.ServiceModel.NetMsmqBinding> for queued communication between a WCF client and a WCF service.</span></span>  
  
### <a name="to-use-queuing-in-a-wcf-service"></a><span data-ttu-id="97da1-107">在 WCF 服务中使用队列</span><span class="sxs-lookup"><span data-stu-id="97da1-107">To use queuing in a WCF service</span></span>  
  
1. <span data-ttu-id="97da1-108">使用用 <xref:System.ServiceModel.ServiceContractAttribute> 标记的接口定义服务协定。</span><span class="sxs-lookup"><span data-stu-id="97da1-108">Define a service contract using an interface marked with the <xref:System.ServiceModel.ServiceContractAttribute>.</span></span> <span data-ttu-id="97da1-109">用 <xref:System.ServiceModel.OperationContractAttribute> 来标记属于服务协定一部分的接口中的操作，并将它们指定为单向操作（因为不返回对该方法的任何响应）。</span><span class="sxs-lookup"><span data-stu-id="97da1-109">Mark the operations in the interface that are part of the service contract with the <xref:System.ServiceModel.OperationContractAttribute> and specify them as one-way because no response to the method is returned.</span></span> <span data-ttu-id="97da1-110">下面的代码提供了示例服务协定及其操作定义。</span><span class="sxs-lookup"><span data-stu-id="97da1-110">The following code provides an example service contract and its operation definition.</span></span>  
  
     [!code-csharp[S_Msmq_Transacted#1](../../../../samples/snippets/csharp/VS_Snippets_CFX/s_msmq_transacted/cs/service.cs#1)]
     [!code-vb[S_Msmq_Transacted#1](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/s_msmq_transacted/vb/service.vb#1)]  
  
2. <span data-ttu-id="97da1-111">当服务协定传递用户定义的类型时，您必须为这些类型定义数据协定。</span><span class="sxs-lookup"><span data-stu-id="97da1-111">When the service contract passes user-defined types, you must define data contracts for those types.</span></span> <span data-ttu-id="97da1-112">下面的代码演示了两个数据协定，`PurchaseOrder` 和 `PurchaseOrderLineItem`。</span><span class="sxs-lookup"><span data-stu-id="97da1-112">The following code shows two data contracts, `PurchaseOrder` and `PurchaseOrderLineItem`.</span></span> <span data-ttu-id="97da1-113">这两种类型定义了发送给服务的数据。</span><span class="sxs-lookup"><span data-stu-id="97da1-113">These two types define data that is sent to the service.</span></span> <span data-ttu-id="97da1-114">（请注意，定义该数据协定的类也定义了大量方法。</span><span class="sxs-lookup"><span data-stu-id="97da1-114">(Note that the classes that define this data contract also define a number of methods.</span></span> <span data-ttu-id="97da1-115">这些方法不被视为数据协定的一部分。</span><span class="sxs-lookup"><span data-stu-id="97da1-115">These methods are not considered part of the data contract.</span></span> <span data-ttu-id="97da1-116">只有那些使用 <xref:System.Runtime.Serialization.DataMemberAttribute> 属性声明的成员才是数据协定的一部分。）</span><span class="sxs-lookup"><span data-stu-id="97da1-116">Only those members that are declared with the <xref:System.Runtime.Serialization.DataMemberAttribute> attribute are part of the data contract.)</span></span>  
  
     [!code-csharp[S_Msmq_Transacted#2](../../../../samples/snippets/csharp/VS_Snippets_CFX/s_msmq_transacted/cs/service.cs#2)]
     [!code-vb[S_Msmq_Transacted#2](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/s_msmq_transacted/vb/service.vb#2)]  
  
3. <span data-ttu-id="97da1-117">实现在类中接口中定义的服务协定的方法。</span><span class="sxs-lookup"><span data-stu-id="97da1-117">Implement the methods of the service contract defined in the interface in a class.</span></span>  
  
     [!code-csharp[S_Msmq_Transacted#3](../../../../samples/snippets/csharp/VS_Snippets_CFX/s_msmq_transacted/cs/service.cs#3)]
     [!code-vb[S_Msmq_Transacted#3](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/s_msmq_transacted/vb/service.vb#3)]  
  
     <span data-ttu-id="97da1-118">请注意放置在 <xref:System.ServiceModel.OperationBehaviorAttribute> 方法上的 `SubmitPurchaseOrder`。</span><span class="sxs-lookup"><span data-stu-id="97da1-118">Notice the <xref:System.ServiceModel.OperationBehaviorAttribute> placed on the `SubmitPurchaseOrder` method.</span></span> <span data-ttu-id="97da1-119">它指定了必须在某个事务内调用此操作，且当方法完成后，该事务会自动完成。</span><span class="sxs-lookup"><span data-stu-id="97da1-119">This specifies that this operation must be called within a transaction and that the transaction automatically completes when the method completes.</span></span>  
  
4. <span data-ttu-id="97da1-120">使用 <xref:System.Messaging> 创建一个事务性队列。</span><span class="sxs-lookup"><span data-stu-id="97da1-120">Create a transactional queue using <xref:System.Messaging>.</span></span> <span data-ttu-id="97da1-121">可以选择使用 Microsoft 消息队列 (MSMQ) Microsoft 管理控制台 (MMC) 来创建队列。</span><span class="sxs-lookup"><span data-stu-id="97da1-121">You can choose to create the queue using Microsoft Message Queuing (MSMQ) Microsoft Management Console (MMC) instead.</span></span> <span data-ttu-id="97da1-122">如果这样，将确保创建事务性队列。</span><span class="sxs-lookup"><span data-stu-id="97da1-122">If so, make sure you create a transactional queue.</span></span>  
  
     [!code-csharp[S_Msmq_Transacted#4](../../../../samples/snippets/csharp/VS_Snippets_CFX/s_msmq_transacted/cs/hostapp.cs#4)]
     [!code-vb[S_Msmq_Transacted#4](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/s_msmq_transacted/vb/hostapp.vb#4)]  
  
5. <span data-ttu-id="97da1-123">在指定服务地址并使用标准 <xref:System.ServiceModel.Description.ServiceEndpoint> 绑定的配置中定义 <xref:System.ServiceModel.NetMsmqBinding>。</span><span class="sxs-lookup"><span data-stu-id="97da1-123">Define a <xref:System.ServiceModel.Description.ServiceEndpoint> in configuration that specifies the service address and uses the standard <xref:System.ServiceModel.NetMsmqBinding> binding.</span></span> <span data-ttu-id="97da1-124">有关使用 WCF 配置的详细信息，请参阅 [配置 wcf 服务](../configuring-services.md)。</span><span class="sxs-lookup"><span data-stu-id="97da1-124">For more information about using WCF configuration, see [Configuring WCF services](../configuring-services.md).</span></span>  

6. <span data-ttu-id="97da1-125">使用 `OrderProcessing` 为 <xref:System.ServiceModel.ServiceHost> 服务创建一个主机，该主机从队列读取消息并处理这些消息。</span><span class="sxs-lookup"><span data-stu-id="97da1-125">Create a host for the `OrderProcessing` service using <xref:System.ServiceModel.ServiceHost> that reads messages from the queue and processes them.</span></span> <span data-ttu-id="97da1-126">打开服务主机使服务处于可用状态。</span><span class="sxs-lookup"><span data-stu-id="97da1-126">Open the service host to make the service available.</span></span> <span data-ttu-id="97da1-127">显示一条消息，告知用户按任何键以终止服务。</span><span class="sxs-lookup"><span data-stu-id="97da1-127">Display a message that tells the user to press any key to terminate the service.</span></span> <span data-ttu-id="97da1-128">调用 `ReadLine` 等待按键，然后关闭服务。</span><span class="sxs-lookup"><span data-stu-id="97da1-128">Call `ReadLine` to wait for the key to be pressed and then close the service.</span></span>  
  
     [!code-csharp[S_Msmq_Transacted#6](../../../../samples/snippets/csharp/VS_Snippets_CFX/s_msmq_transacted/cs/hostapp.cs#6)]
     [!code-vb[S_Msmq_Transacted#6](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/s_msmq_transacted/vb/hostapp.vb#6)]  
  
### <a name="to-create-a-client-for-the-queued-service"></a><span data-ttu-id="97da1-129">为排队服务创建客户端</span><span class="sxs-lookup"><span data-stu-id="97da1-129">To create a client for the queued service</span></span>  
  
1. <span data-ttu-id="97da1-130">下面的示例演示如何运行宿主应用程序并使用 Svcutil.exe 工具创建 WCF 客户端。</span><span class="sxs-lookup"><span data-stu-id="97da1-130">The following example shows how to run the hosting application and use the Svcutil.exe tool to create the WCF client.</span></span>  
  
    ```console
    svcutil http://localhost:8000/ServiceModelSamples/service  
    ```  
  
2. <span data-ttu-id="97da1-131">在配置中定义 <xref:System.ServiceModel.Description.ServiceEndpoint>，指定地址并使用标准 <xref:System.ServiceModel.NetMsmqBinding> 绑定，如下面的示例所示。</span><span class="sxs-lookup"><span data-stu-id="97da1-131">Define a <xref:System.ServiceModel.Description.ServiceEndpoint> in configuration that specifies the address and uses the standard <xref:System.ServiceModel.NetMsmqBinding> binding, as shown in the following example.</span></span>  

3. <span data-ttu-id="97da1-132">创建事务范围以写入到事务性队列，调用 `SubmitPurchaseOrder` 操作并关闭 WCF 客户端，如下面的示例中所示。</span><span class="sxs-lookup"><span data-stu-id="97da1-132">Create a transaction scope to write to the transactional queue, call the `SubmitPurchaseOrder` operation and close the WCF client, as shown in the following example.</span></span>  
  
     [!code-csharp[S_Msmq_Transacted#8](../../../../samples/snippets/csharp/VS_Snippets_CFX/s_msmq_transacted/cs/client.cs#8)]
     [!code-vb[S_Msmq_Transacted#8](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/s_msmq_transacted/vb/client.vb#8)]  
  
## <a name="example"></a><span data-ttu-id="97da1-133">示例</span><span class="sxs-lookup"><span data-stu-id="97da1-133">Example</span></span>  

 <span data-ttu-id="97da1-134">下面的示例演示了服务代码、主机应用程序、App.config 文件以及为此示例包含的客户端代码。</span><span class="sxs-lookup"><span data-stu-id="97da1-134">The following examples show the service code, hosting application, App.config file, and client code included for this example.</span></span>  
  
 [!code-csharp[S_Msmq_Transacted#9](../../../../samples/snippets/csharp/VS_Snippets_CFX/s_msmq_transacted/cs/service.cs#9)]
 [!code-vb[S_Msmq_Transacted#9](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/s_msmq_transacted/vb/service.vb#9)]  
  
 [!code-csharp[S_Msmq_Transacted#10](../../../../samples/snippets/csharp/VS_Snippets_CFX/s_msmq_transacted/cs/hostapp.cs#10)]
 [!code-vb[S_Msmq_Transacted#10](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/s_msmq_transacted/vb/hostapp.vb#10)]  

 [!code-csharp[S_Msmq_Transacted#12](../../../../samples/snippets/csharp/VS_Snippets_CFX/s_msmq_transacted/cs/client.cs#12)]
 [!code-vb[S_Msmq_Transacted#12](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/s_msmq_transacted/vb/client.vb#12)]  

## <a name="see-also"></a><span data-ttu-id="97da1-135">请参阅</span><span class="sxs-lookup"><span data-stu-id="97da1-135">See also</span></span>

- <xref:System.ServiceModel.NetMsmqBinding>
- [<span data-ttu-id="97da1-136">已经过事务处理的 MSMQ 绑定</span><span class="sxs-lookup"><span data-stu-id="97da1-136">Transacted MSMQ Binding</span></span>](../samples/transacted-msmq-binding.md)
- [<span data-ttu-id="97da1-137">在 WCF 中排队</span><span class="sxs-lookup"><span data-stu-id="97da1-137">Queuing in WCF</span></span>](queuing-in-wcf.md)
- [<span data-ttu-id="97da1-138">如何：与 WCF 终结点和消息队列应用程序交换消息</span><span class="sxs-lookup"><span data-stu-id="97da1-138">How to: Exchange Messages with WCF Endpoints and Message Queuing Applications</span></span>](how-to-exchange-messages-with-wcf-endpoints-and-message-queuing-applications.md)
- [<span data-ttu-id="97da1-139">Windows Communication Foundation 到消息队列</span><span class="sxs-lookup"><span data-stu-id="97da1-139">Windows Communication Foundation to Message Queuing</span></span>](../samples/wcf-to-message-queuing.md)
- [<span data-ttu-id="97da1-140">安装“消息队列 (MSMQ)”</span><span class="sxs-lookup"><span data-stu-id="97da1-140">Installing Message Queuing (MSMQ)</span></span>](../samples/installing-message-queuing-msmq.md)
- [<span data-ttu-id="97da1-141">到 Windows Communication Foundation 的消息队列</span><span class="sxs-lookup"><span data-stu-id="97da1-141">Message Queuing to Windows Communication Foundation</span></span>](../samples/message-queuing-to-wcf.md)
- [<span data-ttu-id="97da1-142">基于消息队列的消息安全性</span><span class="sxs-lookup"><span data-stu-id="97da1-142">Message Security over Message Queuing</span></span>](../samples/message-security-over-message-queuing.md)
