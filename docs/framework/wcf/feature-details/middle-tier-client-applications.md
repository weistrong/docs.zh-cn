---
description: 了解详细信息： Middle-Tier 客户端应用程序
title: 中间层客户端应用程序
ms.date: 03/30/2017
ms.assetid: f9714a64-d0ae-4a98-bca0-5d370fdbd631
ms.openlocfilehash: 90de03bb72e14f023db86e6f8226ae84f7461bee
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99733809"
---
# <a name="middle-tier-client-applications"></a><span data-ttu-id="044ce-103">中间层客户端应用程序</span><span class="sxs-lookup"><span data-stu-id="044ce-103">Middle-Tier Client Applications</span></span>

<span data-ttu-id="044ce-104">本主题讨论了使用 Windows Communication Foundation (WCF) 的中间层客户端应用程序的各种问题。</span><span class="sxs-lookup"><span data-stu-id="044ce-104">This topic discusses various issues specific to middle-tier client applications that use Windows Communication Foundation (WCF).</span></span>  
  
## <a name="increasing-middle-tier-client-performance"></a><span data-ttu-id="044ce-105">提高中间层客户端应用程序的性能</span><span class="sxs-lookup"><span data-stu-id="044ce-105">Increasing Middle-Tier Client Performance</span></span>  

 <span data-ttu-id="044ce-106">与以前的通信技术（如使用 ASP.NET 的 Web 服务）相比，创建 WCF 客户端实例可能更为复杂，这是因为 WCF 的丰富功能集。</span><span class="sxs-lookup"><span data-stu-id="044ce-106">Compared to previous communications technologies, such as Web services using ASP.NET, the creation of a WCF client instance can be more complex due to the rich feature set of WCF.</span></span> <span data-ttu-id="044ce-107">例如，打开 <xref:System.ServiceModel.ChannelFactory%601> 对象时，该对象会与服务建立一个安全会话，该过程将增加客户端实例的启动时间。</span><span class="sxs-lookup"><span data-stu-id="044ce-107">For example, when a <xref:System.ServiceModel.ChannelFactory%601> object is opened it can establish a secure session with the service, a procedure that increases the startup time for the client instance.</span></span> <span data-ttu-id="044ce-108">通常，这些附加功能不会对客户端应用程序产生很大影响，因为 WCF 客户端发出多个调用，然后关闭。</span><span class="sxs-lookup"><span data-stu-id="044ce-108">Typically, these additional feature capabilities do not affect client applications greatly since the WCF client makes several calls, and then closes.</span></span>  
  
 <span data-ttu-id="044ce-109">但是，中间层客户端应用程序可以快速地创建许多 WCF 客户端对象，因此，体验会提高初始化需求。</span><span class="sxs-lookup"><span data-stu-id="044ce-109">Middle-tier client applications, however, can create many WCF client objects quickly and, as a result, experience increased initialization requirements.</span></span> <span data-ttu-id="044ce-110">调用服务时，有两种主要的方法可以提高中间层应用程序的性能：</span><span class="sxs-lookup"><span data-stu-id="044ce-110">There are two main approaches to increasing the performance of middle-tier applications when calling services:</span></span>  
  
- <span data-ttu-id="044ce-111">缓存 WCF 客户端对象，并在可能的情况下重用它。</span><span class="sxs-lookup"><span data-stu-id="044ce-111">Cache the WCF client object and reuse it for subsequent calls where possible.</span></span>  
  
- <span data-ttu-id="044ce-112">创建一个 <xref:System.ServiceModel.ChannelFactory%601> 对象，然后使用该对象为每个调用创建新的 WCF 客户端通道对象。</span><span class="sxs-lookup"><span data-stu-id="044ce-112">Create a <xref:System.ServiceModel.ChannelFactory%601> object and then use that object to create new WCF client channel objects for each call.</span></span>  
  
 <span data-ttu-id="044ce-113">使用这些方法时要考虑的问题包括：</span><span class="sxs-lookup"><span data-stu-id="044ce-113">Issues to consider when using these approaches include:</span></span>  
  
- <span data-ttu-id="044ce-114">如果服务使用会话维护客户端特定的状态，则无法将中间层 WCF 客户端与多客户端层请求一起使用，因为该服务的状态与中间层客户端的状态关联。</span><span class="sxs-lookup"><span data-stu-id="044ce-114">If the service is maintaining a client-specific state by using a session, then you cannot reuse the middle-tier WCF client with multiple-client tier requests because the service's state is tied to that of the middle-tier client.</span></span>  
  
- <span data-ttu-id="044ce-115">如果服务必须基于每个客户端执行身份验证，则必须在中间层为每个传入请求创建一个新的客户端，而不是重复使用中间层 WCF 客户端 (或 WCF 客户端信道对象) ，因为在创建 WCF 客户端后，不能修改中间层的客户端凭据 (或 <xref:System.ServiceModel.ChannelFactory%601>) 。</span><span class="sxs-lookup"><span data-stu-id="044ce-115">If the service must perform authentication on a per-client basis, you must create a new client for each incoming request on the middle tier instead of reusing the middle-tier WCF client (or WCF client channel object) because the client credentials of the middle tier cannot be modified after the WCF client (or <xref:System.ServiceModel.ChannelFactory%601>) has been created.</span></span>  
  
- <span data-ttu-id="044ce-116">由于通道及其创建的客户端是线程安全的，因此它们可能不支持同时向网络中写入多条消息。</span><span class="sxs-lookup"><span data-stu-id="044ce-116">While channels and clients created by the channels are thread-safe, they might not support writing more than one message to the wire concurrently.</span></span> <span data-ttu-id="044ce-117">如果要发送较大的消息，特别是消息流，则发送操作可能会阻塞，因为它要等待另一个发送操作完成。</span><span class="sxs-lookup"><span data-stu-id="044ce-117">If you are sending large messages, particularly if streaming, the send operation might block waiting for another send to complete.</span></span> <span data-ttu-id="044ce-118">这会导致两种问题：缺少并发性；当控制流返回到重用信道的服务（即，共享的客户端调用了一种服务，该服务的代码路径会导致对共享的客户端进行回调）时，存在死锁的可能性。</span><span class="sxs-lookup"><span data-stu-id="044ce-118">This causes two sorts of problems: a lack of concurrency and the possibility of deadlock if the flow of control returns to the service reusing the channel (that is, the shared client calls a service whose code path results in a callback to the shared client).</span></span> <span data-ttu-id="044ce-119">不管重用的 WCF 客户端的类型如何都是如此。</span><span class="sxs-lookup"><span data-stu-id="044ce-119">This is true regardless of the type of WCF client you reuse.</span></span>  
  
- <span data-ttu-id="044ce-120">无论您是否共享出错的通道，您都必须处理它。</span><span class="sxs-lookup"><span data-stu-id="044ce-120">You must handle faulted channels regardless of whether you share the channel.</span></span> <span data-ttu-id="044ce-121">然而，重用通道时，出错通道可以关闭多个挂起的请求或发送。</span><span class="sxs-lookup"><span data-stu-id="044ce-121">When channels are reused, however, a faulting channel can take down more than one pending request or send.</span></span>  
  
 <span data-ttu-id="044ce-122">有关为多个请求重复使用客户端的最佳实践的示例，请参阅 [ASP.NET 客户端中的数据绑定](../samples/data-binding-in-an-aspnet-client.md)。</span><span class="sxs-lookup"><span data-stu-id="044ce-122">For an example that demonstrates best practices for reusing a client for multiple requests, see [Data Binding in an ASP.NET Client](../samples/data-binding-in-an-aspnet-client.md).</span></span>  
  
 <span data-ttu-id="044ce-123">此外，如果客户端使用可用 <xref:System.Xml.Serialization.XmlSerializer> 进行序列化的数据类型，则会在运行时生成并编译这些数据类型的序列化代码，从而导致启动性能降低；但你可以提高那些客户端的启动性能。</span><span class="sxs-lookup"><span data-stu-id="044ce-123">In addition, you can increase the startup performance for those clients that use data types that are serializable using the <xref:System.Xml.Serialization.XmlSerializer> generate and compile serialization code for those data types at runtime, which can result in slow start-up performance.</span></span> <span data-ttu-id="044ce-124">通过从应用程序的编译的程序集生成必要的序列化代码， [ ( # A0) ](../servicemodel-metadata-utility-tool-svcutil-exe.md) 可提高这些应用程序的启动性能。</span><span class="sxs-lookup"><span data-stu-id="044ce-124">The [ServiceModel Metadata Utility Tool (Svcutil.exe)](../servicemodel-metadata-utility-tool-svcutil-exe.md) can improve start-up performance for these applications by generating the necessary serialization code from the compiled assemblies for the application.</span></span> <span data-ttu-id="044ce-125">有关详细信息，请参阅 [如何：使用 XmlSerializer 改善 WCF 客户端应用程序的启动时间](startup-time-of-wcf-client-applications-using-the-xmlserializer.md)。</span><span class="sxs-lookup"><span data-stu-id="044ce-125">For more information, see [How to: Improve the Startup Time of WCF Client Applications using the XmlSerializer](startup-time-of-wcf-client-applications-using-the-xmlserializer.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="044ce-126">请参阅</span><span class="sxs-lookup"><span data-stu-id="044ce-126">See also</span></span>

- [<span data-ttu-id="044ce-127">使用 WCF 客户端访问服务</span><span class="sxs-lookup"><span data-stu-id="044ce-127">Accessing Services Using a WCF Client</span></span>](accessing-services-using-a-client.md)
