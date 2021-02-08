---
description: 了解详细信息：如何：使用协定接口创建服务
title: 如何：使用协定接口创建服务
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 7b6803f6-d6f9-4cc2-9f1b-6f4c920475d5
ms.openlocfilehash: 5080f6bb45030811b87f952fb62a74801bc1ef88
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99793826"
---
# <a name="how-to-create-a-service-with-a-contract-interface"></a><span data-ttu-id="212fd-103">如何：使用协定接口创建服务</span><span class="sxs-lookup"><span data-stu-id="212fd-103">How to: Create a Service with a Contract Interface</span></span>

<span data-ttu-id="212fd-104">创建 Windows Communication Foundation (WCF) 协定的首选方式是使用接口。</span><span class="sxs-lookup"><span data-stu-id="212fd-104">The preferred way to create a Windows Communication Foundation (WCF) contract is by using an interface.</span></span> <span data-ttu-id="212fd-105">此协定指定访问服务提供的操作所必需的消息的集合和结构。</span><span class="sxs-lookup"><span data-stu-id="212fd-105">This contract specifies the collection and structure of messages required to access the operations the service offers.</span></span> <span data-ttu-id="212fd-106">此接口通过将 <xref:System.ServiceModel.ServiceContractAttribute> 类应用到该接口并将 <xref:System.ServiceModel.OperationContractAttribute> 类应用到要公开的方法来定义输入和输出类型。</span><span class="sxs-lookup"><span data-stu-id="212fd-106">This interface defines the input and output types by applying the <xref:System.ServiceModel.ServiceContractAttribute> class to the interface and the <xref:System.ServiceModel.OperationContractAttribute> class to the methods that you want to expose.</span></span>  
  
 <span data-ttu-id="212fd-107">有关服务协定的详细信息，请参阅 [设计服务协定](../designing-service-contracts.md)。</span><span class="sxs-lookup"><span data-stu-id="212fd-107">For more information about service contracts, see [Designing Service Contracts](../designing-service-contracts.md).</span></span>  
  
### <a name="creating-a-wcf-contract-with-an-interface"></a><span data-ttu-id="212fd-108">使用接口创建 WCF 协定</span><span class="sxs-lookup"><span data-stu-id="212fd-108">Creating a WCF contract with an interface</span></span>  
  
1. <span data-ttu-id="212fd-109">使用 Visual Basic、c # 或任何其他公共语言运行时语言创建新的接口。</span><span class="sxs-lookup"><span data-stu-id="212fd-109">Create a new interface using Visual Basic, C#, or any other common language runtime language.</span></span>  
  
2. <span data-ttu-id="212fd-110">将 <xref:System.ServiceModel.ServiceContractAttribute> 类应用到该接口。</span><span class="sxs-lookup"><span data-stu-id="212fd-110">Apply the <xref:System.ServiceModel.ServiceContractAttribute> class to the interface.</span></span>  
  
3. <span data-ttu-id="212fd-111">定义该接口中的方法。</span><span class="sxs-lookup"><span data-stu-id="212fd-111">Define the methods in the interface.</span></span>  
  
4. <span data-ttu-id="212fd-112">将类应用于 <xref:System.ServiceModel.OperationContractAttribute> 必须作为公共 WCF 协定的一部分公开的每个方法。</span><span class="sxs-lookup"><span data-stu-id="212fd-112">Apply the <xref:System.ServiceModel.OperationContractAttribute> class to each method that must be exposed as part of the public WCF contract.</span></span>  
  
## <a name="example"></a><span data-ttu-id="212fd-113">示例</span><span class="sxs-lookup"><span data-stu-id="212fd-113">Example</span></span>  

 <span data-ttu-id="212fd-114">下面的代码示例演示一个定义服务协定的接口。</span><span class="sxs-lookup"><span data-stu-id="212fd-114">The following code example shows an interface that defines a service contract.</span></span>  
  
 [!code-csharp[c_HowTo_CreateContractWithInterface#1](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_howto_createcontractwithinterface/cs/source.cs#1)]
 [!code-vb[c_HowTo_CreateContractWithInterface#1](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/c_howto_createcontractwithinterface/vb/source.vb#1)]  
  
 <span data-ttu-id="212fd-115">默认情况下，应用了 <xref:System.ServiceModel.OperationContractAttribute> 类的方法使用请求-答复消息模式。</span><span class="sxs-lookup"><span data-stu-id="212fd-115">The methods that have the <xref:System.ServiceModel.OperationContractAttribute> class applied use a request-reply message pattern by default.</span></span> <span data-ttu-id="212fd-116">有关此消息模式的详细信息，请参阅 [如何：创建 Request-Reply 协定](how-to-create-a-request-reply-contract.md)。</span><span class="sxs-lookup"><span data-stu-id="212fd-116">For more information about this message pattern, see [How to: Create a Request-Reply Contract](how-to-create-a-request-reply-contract.md).</span></span> <span data-ttu-id="212fd-117">您还可以通过设置属性 (Attribute) 的属性 (Property) 来创建和使用其他消息模式。</span><span class="sxs-lookup"><span data-stu-id="212fd-117">You can also create and use other message patterns by setting properties of the attribute.</span></span> <span data-ttu-id="212fd-118">有关更多示例，请参阅 [如何：创建 One-Way 协定](how-to-create-a-one-way-contract.md) 和 [如何：创建双工协定](how-to-create-a-duplex-contract.md)。</span><span class="sxs-lookup"><span data-stu-id="212fd-118">For more examples, see [How to: Create a One-Way Contract](how-to-create-a-one-way-contract.md) and [How to: Create a Duplex Contract](how-to-create-a-duplex-contract.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="212fd-119">请参阅</span><span class="sxs-lookup"><span data-stu-id="212fd-119">See also</span></span>

- <xref:System.ServiceModel.ServiceContractAttribute>
- <xref:System.ServiceModel.OperationContractAttribute>
