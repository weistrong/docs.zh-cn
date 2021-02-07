---
description: 了解详细信息：如何：与 WCF 终结点和消息队列应用程序交换消息
title: 如何：与 WCF 终结点和消息队列应用程序交换消息
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 62210fd8-a372-4d55-ab9b-c99827d1885e
ms.openlocfilehash: 0b8f315b00960ec87e68e9e2b11ac9b273dbbf93
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99704610"
---
# <a name="how-to-exchange-messages-with-wcf-endpoints-and-message-queuing-applications"></a><span data-ttu-id="13cf3-103">如何：与 WCF 终结点和消息队列应用程序交换消息</span><span class="sxs-lookup"><span data-stu-id="13cf3-103">How to: Exchange Messages with WCF Endpoints and Message Queuing Applications</span></span>

<span data-ttu-id="13cf3-104">您可以通过使用 MSMQ 集成绑定将 MSMQ 消息转换为 WCF 消息并将其从 WCF 消息集成，从而将 (MSMQ) 应用程序的现有消息队列与 Windows Communication Foundation (WCF) 应用程序集成。</span><span class="sxs-lookup"><span data-stu-id="13cf3-104">You can integrate existing Message Queuing (MSMQ) applications with Windows Communication Foundation (WCF) applications by using the MSMQ integration binding to convert MSMQ messages to and from WCF messages.</span></span> <span data-ttu-id="13cf3-105">这样，你就可以从 WCF 客户端调用 MSMQ 接收方应用程序，并从 MSMQ 发送方应用程序调用 WCF 服务。</span><span class="sxs-lookup"><span data-stu-id="13cf3-105">This allows you to call into MSMQ receiver applications from WCF clients as well as call into WCF services from MSMQ sender applications.</span></span>  
  
 <span data-ttu-id="13cf3-106">在本部分中，我们将介绍如何使用 <xref:System.ServiceModel.MsmqIntegration.MsmqIntegrationBinding> 来处理 (1) WCF 客户端与使用 System. 消息编写的 msmq 应用程序服务和 (2) msmq 应用程序客户端和 WCF 服务之间的排队通信。</span><span class="sxs-lookup"><span data-stu-id="13cf3-106">In this section, we explain how to use <xref:System.ServiceModel.MsmqIntegration.MsmqIntegrationBinding> for queued communication between (1) a WCF client and an MSMQ application service written using System.Messaging and (2) an MSMQ application client and a WCF service.</span></span>  
  
 <span data-ttu-id="13cf3-107">有关演示如何从 WCF 客户端调用 MSMQ 接收方应用程序的完整示例，请参阅 [Windows Communication Foundation 到消息队列](../samples/wcf-to-message-queuing.md) 的示例。</span><span class="sxs-lookup"><span data-stu-id="13cf3-107">For a complete sample that demonstrates how to call a MSMQ receiver application from a WCF client, see the [Windows Communication Foundation to Message Queuing](../samples/wcf-to-message-queuing.md) sample.</span></span>  
  
 <span data-ttu-id="13cf3-108">有关演示如何从 MSMQ 客户端调用 WCF 服务的完整示例，请参阅 [消息队列到 Windows Communication Foundation](../samples/message-queuing-to-wcf.md) 示例。</span><span class="sxs-lookup"><span data-stu-id="13cf3-108">For a complete sample that demonstrates how to call a WCF service from a MSMQ client, see the [Message Queuing to Windows Communication Foundation](../samples/message-queuing-to-wcf.md) sample.</span></span>  
  
### <a name="to-create-a-wcf-service-that-receives-messages-from-a-msmq-client"></a><span data-ttu-id="13cf3-109">创建从 MSMQ 客户端接收消息的 WCF 服务</span><span class="sxs-lookup"><span data-stu-id="13cf3-109">To create a WCF service that receives messages from a MSMQ client</span></span>  
  
1. <span data-ttu-id="13cf3-110">定义一个接口，该接口定义从 MSMQ 发送方应用程序接收排队消息的 WCF 服务的服务协定，如下面的示例代码所示。</span><span class="sxs-lookup"><span data-stu-id="13cf3-110">Define an interface that defines the service contract for the WCF service that receives queued messages from a MSMQ sender application, as shown in the following example code.</span></span>  
  
     [!code-csharp[S_MsmqToWcf#1](../../../../samples/snippets/csharp/VS_Snippets_CFX/s_msmqtowcf/cs/service.cs#1)]
     [!code-vb[S_MsmqToWcf#1](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/s_msmqtowcf/vb/service.vb#1)]  
  
2. <span data-ttu-id="13cf3-111">实现该接口，将 <xref:System.ServiceModel.ServiceBehaviorAttribute> 属性应用于该类，如下面示例代码所示。</span><span class="sxs-lookup"><span data-stu-id="13cf3-111">Implement the interface and apply the <xref:System.ServiceModel.ServiceBehaviorAttribute> attribute to the class, as shown in the following example code.</span></span>  
  
     [!code-csharp[S_MsmqToWcf#2](../../../../samples/snippets/csharp/VS_Snippets_CFX/s_msmqtowcf/cs/service.cs#2)]
     [!code-vb[S_MsmqToWcf#2](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/s_msmqtowcf/vb/service.vb#2)]  
  
3. <span data-ttu-id="13cf3-112">创建一个配置文件，在该配置文件中指定 <xref:System.ServiceModel.MsmqIntegration.MsmqIntegrationBinding>。</span><span class="sxs-lookup"><span data-stu-id="13cf3-112">Create a configuration file that specifies the <xref:System.ServiceModel.MsmqIntegration.MsmqIntegrationBinding>.</span></span>  

4. <span data-ttu-id="13cf3-113">实例化一个 <xref:System.ServiceModel.ServiceHost> 对象，该对象使用所配置的绑定。</span><span class="sxs-lookup"><span data-stu-id="13cf3-113">Instantiate a <xref:System.ServiceModel.ServiceHost> object that uses the configured binding.</span></span>  

### <a name="to-create-a-wcf-client-that-sends-messages-to-a-msmq-receiver-application"></a><span data-ttu-id="13cf3-114">创建向 MSMQ 接收方应用程序发送消息的 WCF 客户端</span><span class="sxs-lookup"><span data-stu-id="13cf3-114">To create a WCF client that sends messages to a MSMQ receiver application</span></span>  
  
1. <span data-ttu-id="13cf3-115">定义一个接口，该接口定义 WCF 客户端的服务协定，该服务协定向 MSMQ 接收方发送排队消息，如下面的示例代码所示。</span><span class="sxs-lookup"><span data-stu-id="13cf3-115">Define an interface that defines the service contract for the WCF client that sends queued messages to the MSMQ receiver, as shown in the following example code.</span></span>  
  
     [!code-csharp[S_WcfToMsmq#6](../../../../samples/snippets/csharp/VS_Snippets_CFX/s_wcftomsmq/cs/proxy.cs#6)]
     [!code-vb[S_WcfToMsmq#6](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/s_wcftomsmq/vb/proxy.vb#6)]  
  
2. <span data-ttu-id="13cf3-116">定义 WCF 客户端用于调用 MSMQ 接收方的客户端类。</span><span class="sxs-lookup"><span data-stu-id="13cf3-116">Define a client class that the WCF client uses to call the MSMQ receiver.</span></span>  
  
     [!code-csharp[S_WcfToMsmq#2](../../../../samples/snippets/csharp/VS_Snippets_CFX/s_wcftomsmq/cs/snippets.cs#2)]
     [!code-vb[S_WcfToMsmq#2](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/s_wcftomsmq/vb/snippets.vb#2)]  
  
3. <span data-ttu-id="13cf3-117">创建一个配置文件，在该配置文件中指定 MsmqIntegrationBinding 绑定的用法。</span><span class="sxs-lookup"><span data-stu-id="13cf3-117">Create a configuration that specifies use of the MsmqIntegrationBinding binding.</span></span>  
  
     [!code-csharp[S_WcfToMsmq#3](../../../../samples/snippets/csharp/VS_Snippets_CFX/s_wcftomsmq/cs/snippets.cs#3)]
     [!code-vb[S_WcfToMsmq#3](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/s_wcftomsmq/vb/snippets.vb#3)]  
  
4. <span data-ttu-id="13cf3-118">创建该客户端类的一个实例，并调用消息接收服务所定义的方法。</span><span class="sxs-lookup"><span data-stu-id="13cf3-118">Create an instance of the client class and call the method defined by the message receiving service.</span></span>  
  
     [!code-csharp[S_WcfToMsmq#4](../../../../samples/snippets/csharp/VS_Snippets_CFX/s_wcftomsmq/cs/client.cs#4)]  
  
## <a name="see-also"></a><span data-ttu-id="13cf3-119">请参阅</span><span class="sxs-lookup"><span data-stu-id="13cf3-119">See also</span></span>

- [<span data-ttu-id="13cf3-120">队列概述</span><span class="sxs-lookup"><span data-stu-id="13cf3-120">Queues Overview</span></span>](queues-overview.md)
- [<span data-ttu-id="13cf3-121">如何：使用 WCF 终结点交换排队消息</span><span class="sxs-lookup"><span data-stu-id="13cf3-121">How to: Exchange Queued Messages with WCF Endpoints</span></span>](how-to-exchange-queued-messages-with-wcf-endpoints.md)
- [<span data-ttu-id="13cf3-122">Windows Communication Foundation 到消息队列</span><span class="sxs-lookup"><span data-stu-id="13cf3-122">Windows Communication Foundation to Message Queuing</span></span>](../samples/wcf-to-message-queuing.md)
- [<span data-ttu-id="13cf3-123">安装“消息队列 (MSMQ)”</span><span class="sxs-lookup"><span data-stu-id="13cf3-123">Installing Message Queuing (MSMQ)</span></span>](../samples/installing-message-queuing-msmq.md)
- [<span data-ttu-id="13cf3-124">到 Windows Communication Foundation 的消息队列</span><span class="sxs-lookup"><span data-stu-id="13cf3-124">Message Queuing to Windows Communication Foundation</span></span>](../samples/message-queuing-to-wcf.md)
- [<span data-ttu-id="13cf3-125">基于消息队列的消息安全性</span><span class="sxs-lookup"><span data-stu-id="13cf3-125">Message Security over Message Queuing</span></span>](../samples/message-security-over-message-queuing.md)
