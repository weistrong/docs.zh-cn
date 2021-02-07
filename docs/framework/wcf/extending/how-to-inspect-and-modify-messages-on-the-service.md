---
description: 了解详细信息：如何：检查和修改服务上的消息
title: 如何：检查和修改服务上的消息
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 9c5b1cc7-84f3-45f8-9226-d59c278e8c42
ms.openlocfilehash: 5fd3a5e49bdd35a3095e5855b399533337e133a9
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99668872"
---
# <a name="how-to-inspect-and-modify-messages-on-the-service"></a><span data-ttu-id="00170-103">如何：检查和修改服务上的消息</span><span class="sxs-lookup"><span data-stu-id="00170-103">How to: Inspect and Modify Messages on the Service</span></span>

<span data-ttu-id="00170-104">通过实现 <xref:System.ServiceModel.Dispatcher.IDispatchMessageInspector?displayProperty=nameWithType> 并将其插入到服务运行时中，可以通过 Windows Communication Foundation (WCF) 客户端检查或修改传入或传出消息。</span><span class="sxs-lookup"><span data-stu-id="00170-104">You can inspect or modify the incoming or outgoing messages across a Windows Communication Foundation (WCF) client by implementing a <xref:System.ServiceModel.Dispatcher.IDispatchMessageInspector?displayProperty=nameWithType> and inserting it into the service runtime.</span></span> <span data-ttu-id="00170-105">有关详细信息，请参阅 [扩展调度](extending-dispatchers.md)程序。</span><span class="sxs-lookup"><span data-stu-id="00170-105">For more information, see [Extending Dispatchers](extending-dispatchers.md).</span></span> <span data-ttu-id="00170-106">服务上的等效功能为 <xref:System.ServiceModel.Dispatcher.IClientMessageInspector?displayProperty=nameWithType>。</span><span class="sxs-lookup"><span data-stu-id="00170-106">The equivalent feature on the service is the <xref:System.ServiceModel.Dispatcher.IClientMessageInspector?displayProperty=nameWithType>.</span></span>  
  
### <a name="to-inspect-or-modify-messages"></a><span data-ttu-id="00170-107">检查或修改消息</span><span class="sxs-lookup"><span data-stu-id="00170-107">To inspect or modify messages</span></span>  
  
1. <span data-ttu-id="00170-108">实现 <xref:System.ServiceModel.Dispatcher.IDispatchMessageInspector?displayProperty=nameWithType> 接口。</span><span class="sxs-lookup"><span data-stu-id="00170-108">Implement the <xref:System.ServiceModel.Dispatcher.IDispatchMessageInspector?displayProperty=nameWithType> interface.</span></span>  
  
2. <span data-ttu-id="00170-109">根据您希望轻松插入服务消息检查器的范围，实现 <xref:System.ServiceModel.Description.IServiceBehavior?displayProperty=nameWithType>、<xref:System.ServiceModel.Description.IEndpointBehavior?displayProperty=nameWithType> 或 <xref:System.ServiceModel.Description.IContractBehavior?displayProperty=nameWithType> 接口。</span><span class="sxs-lookup"><span data-stu-id="00170-109">Implement a <xref:System.ServiceModel.Description.IServiceBehavior?displayProperty=nameWithType>, <xref:System.ServiceModel.Description.IEndpointBehavior?displayProperty=nameWithType>, or <xref:System.ServiceModel.Description.IContractBehavior?displayProperty=nameWithType> interface depending upon the scope at which you want to easily insert your service message inspector.</span></span>  
  
3. <span data-ttu-id="00170-110">在 <xref:System.ServiceModel.ICommunicationObject.Open%2A?displayProperty=nameWithType> 上调用 <xref:System.ServiceModel.ServiceHost?displayProperty=nameWithType> 方法之前，先插入行为。</span><span class="sxs-lookup"><span data-stu-id="00170-110">Insert your behavior prior to calling the <xref:System.ServiceModel.ICommunicationObject.Open%2A?displayProperty=nameWithType> method on the <xref:System.ServiceModel.ServiceHost?displayProperty=nameWithType>.</span></span> <span data-ttu-id="00170-111">有关详细信息，请参阅 [配置和扩展运行时的行为](configuring-and-extending-the-runtime-with-behaviors.md)。</span><span class="sxs-lookup"><span data-stu-id="00170-111">For details, see [Configuring and Extending the Runtime with Behaviors](configuring-and-extending-the-runtime-with-behaviors.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="00170-112">示例</span><span class="sxs-lookup"><span data-stu-id="00170-112">Example</span></span>  

 <span data-ttu-id="00170-113">下面的代码示例按顺序演示以下各项：</span><span class="sxs-lookup"><span data-stu-id="00170-113">The following code examples show, in order:</span></span>  
  
- <span data-ttu-id="00170-114">服务检查器实现。</span><span class="sxs-lookup"><span data-stu-id="00170-114">A service inspector implementation.</span></span>  
  
- <span data-ttu-id="00170-115">插入检查器的服务行为。</span><span class="sxs-lookup"><span data-stu-id="00170-115">A service behavior that inserts the inspector.</span></span>  
  
- <span data-ttu-id="00170-116">在服务应用程序中加载和运行该行为的配置文件。</span><span class="sxs-lookup"><span data-stu-id="00170-116">A configuration file that loads and runs the behavior in a service application.</span></span>  
  
 [!code-csharp[Interceptors#7](../../../../samples/snippets/csharp/VS_Snippets_CFX/interceptors/cs/interceptors.cs#7)]
 [!code-vb[Interceptors#7](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/interceptors/vb/interceptors.vb#7)]  
  
 [!code-csharp[Interceptors#8](../../../../samples/snippets/csharp/VS_Snippets_CFX/interceptors/cs/insertingbehaviors.cs#8)]
 [!code-vb[Interceptors#8](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/interceptors/vb/insertingbehaviors.vb#8)]  
  
 [!code-xml[Interceptors#9](../../../../samples/snippets/csharp/VS_Snippets_CFX/interceptors/cs/hostapplication.exe.config#9)]  
  
## <a name="see-also"></a><span data-ttu-id="00170-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="00170-117">See also</span></span>

- <xref:System.ServiceModel.Dispatcher.IClientMessageInspector?displayProperty=nameWithType>
- <xref:System.ServiceModel.Dispatcher.IDispatchMessageInspector?displayProperty=nameWithType>
- [<span data-ttu-id="00170-118">使用行为配置和扩展运行时</span><span class="sxs-lookup"><span data-stu-id="00170-118">Configuring and Extending the Runtime with Behaviors</span></span>](configuring-and-extending-the-runtime-with-behaviors.md)
