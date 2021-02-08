---
description: 了解有关详细信息，请参阅如何：设置 ProtectionLevel 属性
title: 如何：设置 ProtectionLevel 属性
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- WCF, security
- ProtectionLevel property
ms.assetid: 3d4e8f80-0f9e-4a26-9899-beb6584e78df
ms.openlocfilehash: 526ed923d254f0312c9a2c6d17b7306973d88902
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99779239"
---
# <a name="how-to-set-the-protectionlevel-property"></a><span data-ttu-id="79b8d-103">如何：设置 ProtectionLevel 属性</span><span class="sxs-lookup"><span data-stu-id="79b8d-103">How to: Set the ProtectionLevel Property</span></span>

<span data-ttu-id="79b8d-104">通过应用相应的属性 (Attribute) 并设置该属性 (Property) 可设置保护级别。</span><span class="sxs-lookup"><span data-stu-id="79b8d-104">You can set the protection level by applying an appropriate attribute and setting the property.</span></span> <span data-ttu-id="79b8d-105">可在服务级设置保护以影响每条消息的所有部分，或者可以从方法到消息部分逐级递增地设置保护。</span><span class="sxs-lookup"><span data-stu-id="79b8d-105">You can set protection at the service level to affect all parts of every message, or you can set protection at increasingly granular levels, from methods to message parts.</span></span> <span data-ttu-id="79b8d-106">有关属性的详细信息 `ProtectionLevel` ，请参阅 [了解保护级别](understanding-protection-level.md)。</span><span class="sxs-lookup"><span data-stu-id="79b8d-106">For more information about the `ProtectionLevel` property, see [Understanding Protection Level](understanding-protection-level.md).</span></span>  
  
> [!NOTE]
> <span data-ttu-id="79b8d-107">只能在代码中，而不是在配置中设置保护级别。</span><span class="sxs-lookup"><span data-stu-id="79b8d-107">You can set protection levels only in code, not in configuration.</span></span>  
  
### <a name="to-sign-all-messages-for-a-service"></a><span data-ttu-id="79b8d-108">为服务签名所有消息</span><span class="sxs-lookup"><span data-stu-id="79b8d-108">To sign all messages for a service</span></span>  
  
1. <span data-ttu-id="79b8d-109">为服务创建一个接口。</span><span class="sxs-lookup"><span data-stu-id="79b8d-109">Create an interface for the service.</span></span>  
  
2. <span data-ttu-id="79b8d-110">将 <xref:System.ServiceModel.ServiceContractAttribute> 属性 (Attribute) 应用于服务，并将 <xref:System.ServiceModel.ServiceContractAttribute.ProtectionLevel%2A> 属性 (Property) 设置为 <xref:System.Net.Security.ProtectionLevel.Sign>，如下面的代码所示（默认级别为 <xref:System.Net.Security.ProtectionLevel.EncryptAndSign>）。</span><span class="sxs-lookup"><span data-stu-id="79b8d-110">Apply the <xref:System.ServiceModel.ServiceContractAttribute> attribute to the service and set the <xref:System.ServiceModel.ServiceContractAttribute.ProtectionLevel%2A> property to <xref:System.Net.Security.ProtectionLevel.Sign>, as shown in the following code (the default level is <xref:System.Net.Security.ProtectionLevel.EncryptAndSign>).</span></span>  
  
     [!code-csharp[C_ProtectionLevel#1](../../../samples/snippets/csharp/VS_Snippets_CFX/c_protectionlevel/cs/source.cs#1)]
     [!code-vb[C_ProtectionLevel#1](../../../samples/snippets/visualbasic/VS_Snippets_CFX/c_protectionlevel/vb/source.vb#1)]  
  
### <a name="to-sign-all-message-parts-for-an-operation"></a><span data-ttu-id="79b8d-111">为操作签名所有消息部分</span><span class="sxs-lookup"><span data-stu-id="79b8d-111">To sign all message parts for an operation</span></span>  
  
1. <span data-ttu-id="79b8d-112">为服务创建一个接口，并将 <xref:System.ServiceModel.ServiceContractAttribute> 属性应用于该接口。</span><span class="sxs-lookup"><span data-stu-id="79b8d-112">Create an interface for the service and apply the <xref:System.ServiceModel.ServiceContractAttribute> attribute to the interface.</span></span>  
  
2. <span data-ttu-id="79b8d-113">向该接口添加一个方法声明。</span><span class="sxs-lookup"><span data-stu-id="79b8d-113">Add a method declaration to the interface.</span></span>  
  
3. <span data-ttu-id="79b8d-114">将 <xref:System.ServiceModel.OperationContractAttribute> 属性 (Attribute) 应用于该方法，并将 <xref:System.ServiceModel.ServiceContractAttribute.ProtectionLevel%2A> 属性 (Property) 设置为 <xref:System.Net.Security.ProtectionLevel.Sign>，如下面的代码所示。</span><span class="sxs-lookup"><span data-stu-id="79b8d-114">Apply the <xref:System.ServiceModel.OperationContractAttribute> attribute to the method, and set the <xref:System.ServiceModel.ServiceContractAttribute.ProtectionLevel%2A> property to <xref:System.Net.Security.ProtectionLevel.Sign>, as shown in the following code.</span></span>  
  
     [!code-csharp[C_ProtectionLevel#2](../../../samples/snippets/csharp/VS_Snippets_CFX/c_protectionlevel/cs/source.cs#2)]
     [!code-vb[C_ProtectionLevel#2](../../../samples/snippets/visualbasic/VS_Snippets_CFX/c_protectionlevel/vb/source.vb#2)]  
  
## <a name="protecting-fault-messages"></a><span data-ttu-id="79b8d-115">保护错误消息</span><span class="sxs-lookup"><span data-stu-id="79b8d-115">Protecting Fault Messages</span></span>  

 <span data-ttu-id="79b8d-116">服务上引发的异常可以作为 SOAP 故障发送到客户端。</span><span class="sxs-lookup"><span data-stu-id="79b8d-116">Exceptions that are thrown on a service can be sent to a client as SOAP faults.</span></span> <span data-ttu-id="79b8d-117">有关创建强类型错误的详细信息，请参阅 [在协定和服务中指定和处理错误](specifying-and-handling-faults-in-contracts-and-services.md) 和 [如何：在服务协定中声明错误](how-to-declare-faults-in-service-contracts.md)。</span><span class="sxs-lookup"><span data-stu-id="79b8d-117">For more information about creating strongly typed faults, see [Specifying and Handling Faults in Contracts and Services](specifying-and-handling-faults-in-contracts-and-services.md) and [How to: Declare Faults in Service Contracts](how-to-declare-faults-in-service-contracts.md).</span></span>  
  
#### <a name="to-protect-a-fault-message"></a><span data-ttu-id="79b8d-118">保护错误消息</span><span class="sxs-lookup"><span data-stu-id="79b8d-118">To protect a fault message</span></span>  
  
1. <span data-ttu-id="79b8d-119">创建一个表示错误消息的类型。</span><span class="sxs-lookup"><span data-stu-id="79b8d-119">Create a type that represents the fault message.</span></span> <span data-ttu-id="79b8d-120">下面的示例创建一个含有两个字段的名为 `MathFault` 的类。</span><span class="sxs-lookup"><span data-stu-id="79b8d-120">The following example creates a class named `MathFault` with two fields.</span></span>  
  
2. <span data-ttu-id="79b8d-121">将 <xref:System.Runtime.Serialization.DataContractAttribute> 属性应用于该类型，并将 <xref:System.Runtime.Serialization.DataMemberAttribute> 属性应用于应该序列化的每个字段，如下面的代码所示。</span><span class="sxs-lookup"><span data-stu-id="79b8d-121">Apply the <xref:System.Runtime.Serialization.DataContractAttribute> attribute to the type and a <xref:System.Runtime.Serialization.DataMemberAttribute> attribute to each field that should be serialized, as shown in the following code.</span></span>  
  
     [!code-csharp[C_ProtectionLevel#3](../../../samples/snippets/csharp/VS_Snippets_CFX/c_protectionlevel/cs/source.cs#3)]
     [!code-vb[C_ProtectionLevel#3](../../../samples/snippets/visualbasic/VS_Snippets_CFX/c_protectionlevel/vb/source.vb#3)]  
  
3. <span data-ttu-id="79b8d-122">在将返回该错误的接口中，将 <xref:System.ServiceModel.FaultContractAttribute> 属性应用于将返回错误的方法，并将 `detailType` 参数设置为错误类的类型。</span><span class="sxs-lookup"><span data-stu-id="79b8d-122">In the interface that will return the fault, apply the <xref:System.ServiceModel.FaultContractAttribute> attribute to the method that will return the fault and set the `detailType` parameter to the type of the fault class.</span></span>  
  
4. <span data-ttu-id="79b8d-123">同样在构造函数中，将 <xref:System.ServiceModel.FaultContractAttribute.ProtectionLevel%2A> 属性设置为 <xref:System.Net.Security.ProtectionLevel.EncryptAndSign>，如下面的代码所示。</span><span class="sxs-lookup"><span data-stu-id="79b8d-123">Also in the constructor, set the <xref:System.ServiceModel.FaultContractAttribute.ProtectionLevel%2A> property to <xref:System.Net.Security.ProtectionLevel.EncryptAndSign>, as shown in the following code.</span></span>  
  
     [!code-csharp[C_ProtectionLevel#4](../../../samples/snippets/csharp/VS_Snippets_CFX/c_protectionlevel/cs/source.cs#4)]
     [!code-vb[C_ProtectionLevel#4](../../../samples/snippets/visualbasic/VS_Snippets_CFX/c_protectionlevel/vb/source.vb#4)]  
  
## <a name="protecting-message-parts"></a><span data-ttu-id="79b8d-124">保护消息部分</span><span class="sxs-lookup"><span data-stu-id="79b8d-124">Protecting Message Parts</span></span>  

 <span data-ttu-id="79b8d-125">使用消息协定来保护消息的各个部分。</span><span class="sxs-lookup"><span data-stu-id="79b8d-125">Use a message contract to protect parts of a message.</span></span> <span data-ttu-id="79b8d-126">有关消息约定的详细信息，请参阅 [使用消息协定](./feature-details/using-message-contracts.md)。</span><span class="sxs-lookup"><span data-stu-id="79b8d-126">For more information about message contracts, see [Using Message Contracts](./feature-details/using-message-contracts.md).</span></span>  
  
#### <a name="to-protect-a-message-body"></a><span data-ttu-id="79b8d-127">保护消息正文</span><span class="sxs-lookup"><span data-stu-id="79b8d-127">To protect a message body</span></span>  
  
1. <span data-ttu-id="79b8d-128">创建一个表示消息的类型。</span><span class="sxs-lookup"><span data-stu-id="79b8d-128">Create a type that represents the message.</span></span> <span data-ttu-id="79b8d-129">下面的示例创建一个 `Company` 类，其中有两个字段 `CompanyName` 和 `CompanyID`。</span><span class="sxs-lookup"><span data-stu-id="79b8d-129">The following example creates a `Company` class with two fields, `CompanyName` and `CompanyID`.</span></span>  
  
2. <span data-ttu-id="79b8d-130">将 <xref:System.ServiceModel.MessageContractAttribute> 属性 (Attribute) 应用于该类，并将 <xref:System.ServiceModel.MessageContractAttribute.ProtectionLevel%2A> 属性 (Property) 设置为 <xref:System.Net.Security.ProtectionLevel.EncryptAndSign>。</span><span class="sxs-lookup"><span data-stu-id="79b8d-130">Apply the <xref:System.ServiceModel.MessageContractAttribute> attribute to the class and set the <xref:System.ServiceModel.MessageContractAttribute.ProtectionLevel%2A> property to <xref:System.Net.Security.ProtectionLevel.EncryptAndSign>.</span></span>  
  
3. <span data-ttu-id="79b8d-131">将 <xref:System.ServiceModel.MessageHeaderAttribute> 属性 (Attribute) 应用于将表示为消息头的字段，并将 `ProtectionLevel` 属性 (Property) 设置为 <xref:System.Net.Security.ProtectionLevel.EncryptAndSign>。</span><span class="sxs-lookup"><span data-stu-id="79b8d-131">Apply the <xref:System.ServiceModel.MessageHeaderAttribute> attribute to a field that will be expressed as a message header and set the `ProtectionLevel` property to <xref:System.Net.Security.ProtectionLevel.EncryptAndSign>.</span></span>  
  
4. <span data-ttu-id="79b8d-132">将应用于 <xref:System.ServiceModel.MessageBodyMemberAttribute> 将表示为消息正文的一部分的任何字段，并将 `ProtectionLevel` 属性设置为 <xref:System.Net.Security.ProtectionLevel.EncryptAndSign> ，如下面的示例中所示。</span><span class="sxs-lookup"><span data-stu-id="79b8d-132">Apply the <xref:System.ServiceModel.MessageBodyMemberAttribute> to any field that will be expressed as part of the message body, and set the `ProtectionLevel` property to <xref:System.Net.Security.ProtectionLevel.EncryptAndSign>, as shown in the following example.</span></span>  
  
     [!code-csharp[C_ProtectionLevel#5](../../../samples/snippets/csharp/VS_Snippets_CFX/c_protectionlevel/cs/source.cs#5)]
     [!code-vb[C_ProtectionLevel#5](../../../samples/snippets/visualbasic/VS_Snippets_CFX/c_protectionlevel/vb/source.vb#5)]  
  
## <a name="example"></a><span data-ttu-id="79b8d-133">示例</span><span class="sxs-lookup"><span data-stu-id="79b8d-133">Example</span></span>  

 <span data-ttu-id="79b8d-134">下面的示例设置位于服务中不同位置的多个属性 (Attribute) 类的 `ProtectionLevel` 属性 (Property)。</span><span class="sxs-lookup"><span data-stu-id="79b8d-134">The following example sets the `ProtectionLevel` property of several attribute classes at various places in a service.</span></span>  
  
 [!code-csharp[C_ProtectionLevel#6](../../../samples/snippets/csharp/VS_Snippets_CFX/c_protectionlevel/cs/source.cs#6)]
 [!code-vb[C_ProtectionLevel#6](../../../samples/snippets/visualbasic/VS_Snippets_CFX/c_protectionlevel/vb/source.vb#6)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="79b8d-135">编译代码</span><span class="sxs-lookup"><span data-stu-id="79b8d-135">Compiling the Code</span></span>  

 <span data-ttu-id="79b8d-136">下面的代码显示编译该示例代码所必需的命名空间。</span><span class="sxs-lookup"><span data-stu-id="79b8d-136">The following code shows the namespaces required to compile the example code.</span></span>  
  
 [!code-csharp[C_ProtectionLevel#0](../../../samples/snippets/csharp/VS_Snippets_CFX/c_protectionlevel/cs/source.cs#0)]
 [!code-vb[C_ProtectionLevel#0](../../../samples/snippets/visualbasic/VS_Snippets_CFX/c_protectionlevel/vb/source.vb#0)]  
  
## <a name="see-also"></a><span data-ttu-id="79b8d-137">请参阅</span><span class="sxs-lookup"><span data-stu-id="79b8d-137">See also</span></span>

- <xref:System.ServiceModel.ServiceContractAttribute>
- <xref:System.ServiceModel.OperationContractAttribute>
- <xref:System.ServiceModel.FaultContractAttribute>
- <xref:System.ServiceModel.MessageContractAttribute>
- <xref:System.ServiceModel.MessageBodyMemberAttribute>
- [<span data-ttu-id="79b8d-138">了解保护级别</span><span class="sxs-lookup"><span data-stu-id="79b8d-138">Understanding Protection Level</span></span>](understanding-protection-level.md)
