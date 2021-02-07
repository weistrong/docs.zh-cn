---
description: 了解详细信息：负载均衡
title: 负载平衡
ms.date: 03/30/2017
helpviewer_keywords:
- load balancing [WCF]
ms.assetid: 148e0168-c08d-4886-8769-776d0953b80f
ms.openlocfilehash: 9f7946793fb9a9eec9baf531e4650f68b92151d9
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99732808"
---
# <a name="load-balancing"></a><span data-ttu-id="db56c-103">负载平衡</span><span class="sxs-lookup"><span data-stu-id="db56c-103">Load Balancing</span></span>

<span data-ttu-id="db56c-104"> (WCF) 应用程序增加 Windows Communication Foundation 容量的一种方法是通过将其部署到负载平衡的服务器场来扩展它们。</span><span class="sxs-lookup"><span data-stu-id="db56c-104">One way to increase the capacity of Windows Communication Foundation (WCF) applications is to scale them out by deploying them into a load-balanced server farm.</span></span> <span data-ttu-id="db56c-105">可以使用标准负载平衡技术（包括软件负载平衡器，例如 Windows 网络负载平衡）以及基于硬件的负载平衡设备对 WCF 应用程序进行负载平衡。</span><span class="sxs-lookup"><span data-stu-id="db56c-105">WCF applications can be load balanced using standard load balancing techniques, including software load balancers such as Windows Network Load Balancing as well as hardware-based load balancing appliances.</span></span>  
  
 <span data-ttu-id="db56c-106">以下各节讨论有关使用各种系统提供的绑定生成的 WCF 应用程序的负载平衡注意事项。</span><span class="sxs-lookup"><span data-stu-id="db56c-106">The following sections discuss considerations for load balancing WCF applications built using various system-provided bindings.</span></span>  
  
## <a name="load-balancing-with-the-basic-http-binding"></a><span data-ttu-id="db56c-107">基本 HTTP 绑定的负载平衡</span><span class="sxs-lookup"><span data-stu-id="db56c-107">Load Balancing with the Basic HTTP Binding</span></span>  

 <span data-ttu-id="db56c-108">从负载平衡的角度来看，使用进行通信的 WCF 应用程序与 <xref:System.ServiceModel.BasicHttpBinding> 其他常见类型的 HTTP 网络流量（ (静态 HTML 内容、ASP.NET 页或 .Asmx Web 服务) ）没有什么不同。</span><span class="sxs-lookup"><span data-stu-id="db56c-108">From the perspective of load balancing, WCF applications that communicate using the <xref:System.ServiceModel.BasicHttpBinding> are no different than other common types of HTTP network traffic (static HTML content, ASP.NET pages, or ASMX Web Services).</span></span> <span data-ttu-id="db56c-109">使用此绑定的 WCF 通道本质上是无状态的，当通道关闭时，它们会终止其连接。</span><span class="sxs-lookup"><span data-stu-id="db56c-109">WCF channels that use this binding are inherently stateless, and terminate their connections when the channel closes.</span></span> <span data-ttu-id="db56c-110">因此，<xref:System.ServiceModel.BasicHttpBinding> 可以很好地与现有的 HTTP 负载平衡技术一起使用。</span><span class="sxs-lookup"><span data-stu-id="db56c-110">As such, the <xref:System.ServiceModel.BasicHttpBinding> works well with existing HTTP load balancing techniques.</span></span>  
  
 <span data-ttu-id="db56c-111">默认情况下，<xref:System.ServiceModel.BasicHttpBinding> 会在消息中发送一个具有 `Keep-Alive` 值的连接 HTTP 标头，该标头可让客户端建立到支持这些客户端的服务的持续连接。</span><span class="sxs-lookup"><span data-stu-id="db56c-111">By default, the <xref:System.ServiceModel.BasicHttpBinding> sends a connection HTTP header in messages with a `Keep-Alive` value, which enables clients to establish persistent connections to the services that support them.</span></span> <span data-ttu-id="db56c-112">这种配置具有高的吞吐量，因为可以重新使用以前建立的连接向同一个服务器发送后续消息。</span><span class="sxs-lookup"><span data-stu-id="db56c-112">This configuration offers enhanced throughput because previously established connections can be reused to send subsequent messages to the same server.</span></span> <span data-ttu-id="db56c-113">然而，重新使用连接可能导致客户端与负载平衡场中的特定服务器密切关联，从而降低循环负载平衡的效率。</span><span class="sxs-lookup"><span data-stu-id="db56c-113">However, connection reuse may cause clients to become strongly associated to a specific server within the load-balanced farm, which reduces the effectiveness of round-robin load balancing.</span></span> <span data-ttu-id="db56c-114">如果不需要此行为，则可以使用 `Keep-Alive` 或用户定义的 <xref:System.ServiceModel.Channels.HttpTransportBindingElement.KeepAliveEnabled%2A> 在使用 <xref:System.ServiceModel.Channels.CustomBinding> 属性的服务器上禁用 HTTP <xref:System.ServiceModel.Channels.Binding>。</span><span class="sxs-lookup"><span data-stu-id="db56c-114">If this behavior is undesirable, HTTP `Keep-Alive` can be disabled on the server using the <xref:System.ServiceModel.Channels.HttpTransportBindingElement.KeepAliveEnabled%2A> property with a <xref:System.ServiceModel.Channels.CustomBinding> or user-defined <xref:System.ServiceModel.Channels.Binding>.</span></span> <span data-ttu-id="db56c-115">下面的示例演示如何使用配置来执行该操作。</span><span class="sxs-lookup"><span data-stu-id="db56c-115">The following example shows how to do this using configuration.</span></span>  
  
```xml  
<?xml version="1.0" encoding="utf-8" ?>  
<configuration>  
  
 <system.serviceModel>  
  <services>  
   <service
     name="Microsoft.ServiceModel.Samples.CalculatorService"  
     behaviorConfiguration="CalculatorServiceBehavior">  
     <host>  
      <baseAddresses>  
       <add baseAddress="http://localhost:8000/servicemodelsamples/service"/>  
      </baseAddresses>  
     </host>  
    <!-- configure http endpoint, use base address provided by host  
         And the customBinding -->  
     <endpoint address=""  
           binding="customBinding"  
           bindingConfiguration="HttpBinding"
           contract="Microsoft.ServiceModel.Samples.ICalculator" />  
   </service>  
  </services>  
  
  <bindings>  
    <customBinding>  
  
    <!-- Configure a CustomBinding that disables keepAliveEnabled-->  
      <binding name="HttpBinding" keepAliveEnabled="False"/>  
  
    </customBinding>  
  </bindings>  
 </system.serviceModel>  
</configuration>  
```  
  
 <span data-ttu-id="db56c-116">使用 .NET Framework 4 中引入的简化配置，可以使用以下简化的配置来实现相同的行为。</span><span class="sxs-lookup"><span data-stu-id="db56c-116">Using the simplified configuration introduced in .NET Framework 4, the same behavior can be accomplished using the following simplified configuration.</span></span>  
  
```xml  
<?xml version="1.0" encoding="utf-8" ?>  
<configuration>  
 <system.serviceModel>  
    <protocolMapping>  
      <add scheme="http" binding="customBinding" />  
    </protocolMapping>  
    <bindings>  
      <customBinding>  
  
      <!-- Configure a CustomBinding that disables keepAliveEnabled-->  
        <binding keepAliveEnabled="False"/>  
  
      </customBinding>  
    </bindings>  
 </system.serviceModel>  
</configuration>  
```  
  
 <span data-ttu-id="db56c-117">有关默认终结点、绑定和行为的详细信息，请参阅[简化配置](simplified-configuration.md)和 [WCF 服务的简化配置](./samples/simplified-configuration-for-wcf-services.md)。</span><span class="sxs-lookup"><span data-stu-id="db56c-117">For more information about default endpoints, bindings, and behaviors, see [Simplified Configuration](simplified-configuration.md) and [Simplified Configuration for WCF Services](./samples/simplified-configuration-for-wcf-services.md).</span></span>  
  
## <a name="load-balancing-with-the-wshttp-binding-and-the-wsdualhttp-binding"></a><span data-ttu-id="db56c-118">WSHttp 绑定和 WSDualHttp 绑定的负载平衡</span><span class="sxs-lookup"><span data-stu-id="db56c-118">Load Balancing with the WSHttp Binding and the WSDualHttp Binding</span></span>  

 <span data-ttu-id="db56c-119">如果对默认的绑定配置进行一些修改，则 <xref:System.ServiceModel.WSHttpBinding> 和 <xref:System.ServiceModel.WSDualHttpBinding> 都可以使用 HTTP 负载平衡技术来实现负载平衡。</span><span class="sxs-lookup"><span data-stu-id="db56c-119">Both the <xref:System.ServiceModel.WSHttpBinding> and the <xref:System.ServiceModel.WSDualHttpBinding> can be load balanced using HTTP load balancing techniques provided several modifications are made to the default binding configuration.</span></span>  
  
- <span data-ttu-id="db56c-120">关闭安全上下文建立或使用有状态的安全会话。</span><span class="sxs-lookup"><span data-stu-id="db56c-120">Turn off Security Context Establishment or use stateful security sessions.</span></span> <span data-ttu-id="db56c-121">通过将 <xref:System.ServiceModel.NonDualMessageSecurityOverHttp.EstablishSecurityContext%2A> 的属性设置为，可以关闭安全上下文的建立 <xref:System.ServiceModel.WSHttpBinding> `false` 。</span><span class="sxs-lookup"><span data-stu-id="db56c-121">Security Context Establishment can be turned off by setting the <xref:System.ServiceModel.NonDualMessageSecurityOverHttp.EstablishSecurityContext%2A> property on the <xref:System.ServiceModel.WSHttpBinding> to `false`.</span></span> <span data-ttu-id="db56c-122">如果你使用的是 <xref:System.ServiceModel.WSDualHttpBinding> 或需要安全会话，则可以使用 [安全会话](./feature-details/secure-sessions.md)中所述的有状态安全会话。</span><span class="sxs-lookup"><span data-stu-id="db56c-122">If you are using <xref:System.ServiceModel.WSDualHttpBinding> or security sessions are required, it is possible to use stateful security sessions as described in [Secure Sessions](./feature-details/secure-sessions.md).</span></span> <span data-ttu-id="db56c-123">有状态安全会话使服务保持无状态，因为安全会话的所有状态都作为保护安全令牌的一部分与每个请求一起传输。</span><span class="sxs-lookup"><span data-stu-id="db56c-123">Stateful security sessions enable the service to remain stateless, as all of the state for the security session is transmitted with each request as a part of the protection security token.</span></span> <span data-ttu-id="db56c-124">若要启用有状态安全会话，你必须使用 <xref:System.ServiceModel.Channels.CustomBinding> 或用户定义的 <xref:System.ServiceModel.Channels.Binding> ，因为所需的配置设置不会在系统提供的和中公开 <xref:System.ServiceModel.WSHttpBinding> <xref:System.ServiceModel.WSDualHttpBinding> 。</span><span class="sxs-lookup"><span data-stu-id="db56c-124">To enable a stateful security session, you must use a <xref:System.ServiceModel.Channels.CustomBinding> or user-defined <xref:System.ServiceModel.Channels.Binding>, as the necessary configuration settings are not exposed on the system-provided <xref:System.ServiceModel.WSHttpBinding> and <xref:System.ServiceModel.WSDualHttpBinding>.</span></span>

- <span data-ttu-id="db56c-125">如果关闭安全上下文建立，还需要关闭服务凭据协商。</span><span class="sxs-lookup"><span data-stu-id="db56c-125">If you turn off Security Context Establishment, you also need to turn off Service Credential Negotiation.</span></span> <span data-ttu-id="db56c-126">若要将其关闭，请将 <xref:System.ServiceModel.MessageSecurityOverHttp.NegotiateServiceCredential> 的属性设置 <xref:System.ServiceModel.WSHttpBinding> 为 `false` 。</span><span class="sxs-lookup"><span data-stu-id="db56c-126">To turn it off, set the <xref:System.ServiceModel.MessageSecurityOverHttp.NegotiateServiceCredential> property on the <xref:System.ServiceModel.WSHttpBinding> to `false`.</span></span> <span data-ttu-id="db56c-127">若要禁用服务凭据协商，你可能需要在客户端上显式指定终结点标识。</span><span class="sxs-lookup"><span data-stu-id="db56c-127">To disable Service Credential Negotiation, you may need to explicitly specify the endpoint identity on the client.</span></span>
  
- <span data-ttu-id="db56c-128">不要使用可靠会话。</span><span class="sxs-lookup"><span data-stu-id="db56c-128">Do not use reliable sessions.</span></span> <span data-ttu-id="db56c-129">默认情况下此功能处于关闭状态。</span><span class="sxs-lookup"><span data-stu-id="db56c-129">This feature is off by default.</span></span>  
  
## <a name="load-balancing-the-nettcp-binding"></a><span data-ttu-id="db56c-130">使 Net.TCP 绑定实现负载平衡</span><span class="sxs-lookup"><span data-stu-id="db56c-130">Load Balancing the Net.TCP Binding</span></span>  

 <span data-ttu-id="db56c-131">可以使用 IP 层负载平衡技术实现 <xref:System.ServiceModel.NetTcpBinding> 的负载平衡。</span><span class="sxs-lookup"><span data-stu-id="db56c-131">The <xref:System.ServiceModel.NetTcpBinding> can be load balanced using IP-layer load balancing techniques.</span></span> <span data-ttu-id="db56c-132">不过，默认情况下，<xref:System.ServiceModel.NetTcpBinding> 会汇集 TCP 连接以减少连接延迟。</span><span class="sxs-lookup"><span data-stu-id="db56c-132">However, the <xref:System.ServiceModel.NetTcpBinding> pools TCP connections by default to reduce connection latency.</span></span> <span data-ttu-id="db56c-133">这是一种干扰负载平衡基本机制的优化。</span><span class="sxs-lookup"><span data-stu-id="db56c-133">This is an optimization that interferes with the basic mechanism of load balancing.</span></span> <span data-ttu-id="db56c-134">用于优化 <xref:System.ServiceModel.NetTcpBinding> 的主配置值是租约超时，它是连接池设置的一部分。</span><span class="sxs-lookup"><span data-stu-id="db56c-134">The primary configuration value for optimizing the <xref:System.ServiceModel.NetTcpBinding> is the lease timeout, which is part of the Connection Pool Settings.</span></span> <span data-ttu-id="db56c-135">连接池导致客户端连接与场内特定的服务器关联。</span><span class="sxs-lookup"><span data-stu-id="db56c-135">Connection pooling causes client connections to become associated to specific servers within the farm.</span></span> <span data-ttu-id="db56c-136">随着这些连接的生存期的增加（一个受租约超时设置控制的因素），场内不同服务器上的负载分布会变得不平衡。</span><span class="sxs-lookup"><span data-stu-id="db56c-136">As the lifetime of those connections increase (a factor controlled by the lease timeout setting), the load distribution across various servers in the farm becomes unbalanced.</span></span> <span data-ttu-id="db56c-137">结果使平均调用时间增加。</span><span class="sxs-lookup"><span data-stu-id="db56c-137">As a result the average call time increases.</span></span> <span data-ttu-id="db56c-138">因此，在负载平衡方案中使用 <xref:System.ServiceModel.NetTcpBinding> 时，应考虑减少由绑定使用的默认租约超时。</span><span class="sxs-lookup"><span data-stu-id="db56c-138">So when using the <xref:System.ServiceModel.NetTcpBinding> in load-balanced scenarios, consider reducing the default lease timeout used by the binding.</span></span> <span data-ttu-id="db56c-139">虽然租约超时的最佳值取决于应用程序，但 30 秒的租约超时对于负载平衡方案不失为一个合理的始点。</span><span class="sxs-lookup"><span data-stu-id="db56c-139">A 30-second lease timeout is a reasonable starting point for load-balanced scenarios, although the optimal value is application-dependent.</span></span> <span data-ttu-id="db56c-140">有关通道租约超时和其他传输配额的详细信息，请参阅 [传输配额](./feature-details/transport-quotas.md)。</span><span class="sxs-lookup"><span data-stu-id="db56c-140">For more information about the channel lease timeout and other transport quotas, see [Transport Quotas](./feature-details/transport-quotas.md).</span></span>  
  
 <span data-ttu-id="db56c-141">若要在负载平衡方案中获得最佳性能，请考虑使用 <xref:System.ServiceModel.NetTcpSecurity>（<xref:System.ServiceModel.SecurityMode.Transport> 或 <xref:System.ServiceModel.SecurityMode.TransportWithMessageCredential>）。</span><span class="sxs-lookup"><span data-stu-id="db56c-141">For best performance in load-balanced scenarios, consider using <xref:System.ServiceModel.NetTcpSecurity> (either <xref:System.ServiceModel.SecurityMode.Transport> or <xref:System.ServiceModel.SecurityMode.TransportWithMessageCredential>).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="db56c-142">请参阅</span><span class="sxs-lookup"><span data-stu-id="db56c-142">See also</span></span>

- [<span data-ttu-id="db56c-143">Internet 信息服务承载最佳实践</span><span class="sxs-lookup"><span data-stu-id="db56c-143">Internet Information Services Hosting Best Practices</span></span>](./feature-details/internet-information-services-hosting-best-practices.md)
