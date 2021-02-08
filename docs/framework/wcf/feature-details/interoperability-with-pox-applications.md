---
description: 了解详细信息：与 POX 应用程序的互操作性
title: 与 POX 应用程序的互操作性
ms.date: 03/30/2017
ms.assetid: 449276b8-4633-46f0-85c9-81f01d127636
ms.openlocfilehash: 832b9ae93f6046ca9995b57bdcbbfbfeb46d2a09
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99802705"
---
# <a name="interoperability-with-pox-applications"></a><span data-ttu-id="8ee96-103">与 POX 应用程序的互操作性</span><span class="sxs-lookup"><span data-stu-id="8ee96-103">Interoperability with POX applications</span></span>

<span data-ttu-id="8ee96-104">"纯旧 XML" (POX) 应用程序通过交换原始 HTTP 消息进行通信，这些消息仅包含未包含在 SOAP 信封中的 XML 应用程序数据。</span><span class="sxs-lookup"><span data-stu-id="8ee96-104">"Plain Old XML" (POX) applications communicate by exchanging raw HTTP messages that contain only XML application data that is not enclosed within a SOAP envelope.</span></span> <span data-ttu-id="8ee96-105">Windows Communication Foundation (WCF) 可以同时提供使用 POX 消息的服务和客户端。</span><span class="sxs-lookup"><span data-stu-id="8ee96-105">Windows Communication Foundation (WCF) can provide both services and clients that use POX messages.</span></span> <span data-ttu-id="8ee96-106">在服务上，WCF 可用于实现向客户端公开终结点的服务，如用于发送和接收 POX 消息的 Web 浏览器和脚本语言。</span><span class="sxs-lookup"><span data-stu-id="8ee96-106">On the service, WCF can be used to implement services that expose endpoints to clients such as Web browsers and scripting languages that send and receive POX messages.</span></span> <span data-ttu-id="8ee96-107">在客户端上，可以使用 WCF 编程模型实现与基于 POX 的服务进行通信的客户端。</span><span class="sxs-lookup"><span data-stu-id="8ee96-107">On the client, the WCF programming model can be used to implement clients that communicate with POX-based services.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="8ee96-108">本文档最初是为 .NET Framework 3.0 编写的。</span><span class="sxs-lookup"><span data-stu-id="8ee96-108">This document was originally written for the .NET Framework 3.0.</span></span>  <span data-ttu-id="8ee96-109">.NET Framework 3.5 内置了对 POX 应用程序的支持。</span><span class="sxs-lookup"><span data-stu-id="8ee96-109">.NET Framework 3.5 has built-in support for working with POX applications.</span></span> <span data-ttu-id="8ee96-110">有关详细信息，请参阅 [WCF WEB HTTP 编程模型](wcf-web-http-programming-model.md)。</span><span class="sxs-lookup"><span data-stu-id="8ee96-110">For more information about see [WCF Web HTTP Programming Model](wcf-web-http-programming-model.md).</span></span>
  
## <a name="pox-programming-with-wcf"></a><span data-ttu-id="8ee96-111">POX 编程和 WCF</span><span class="sxs-lookup"><span data-stu-id="8ee96-111">POX programming with WCF</span></span>

<span data-ttu-id="8ee96-112">使用 POX 消息通过 HTTP 进行通信的 WCF 服务使用 [\<customBinding>](../../configure-apps/file-schema/wcf/custombinding.md) 。</span><span class="sxs-lookup"><span data-stu-id="8ee96-112">WCF services that communicate over HTTP using POX messages use a [\<customBinding>](../../configure-apps/file-schema/wcf/custombinding.md).</span></span>

```xml
<customBinding>
   <binding name="poxServerBinding">
       <textMessageEncoding messageVersion="None" />
       <httpTransport />
   </binding>
</customBinding>
```

<span data-ttu-id="8ee96-113">此自定义绑定包含两个元素：</span><span class="sxs-lookup"><span data-stu-id="8ee96-113">This custom binding contains two elements:</span></span>

- [\<httpTransport>](../../configure-apps/file-schema/wcf/httptransport.md)

- [\<textMessageEncoding>](../../configure-apps/file-schema/wcf/textmessageencoding.md)

<span data-ttu-id="8ee96-114">标准 WCF 文本消息编码器专门配置为使用 <xref:System.ServiceModel.Channels.MessageVersion.None%2A> 值，这使它能够处理未包装在 SOAP 信封中的 XML 消息负载。</span><span class="sxs-lookup"><span data-stu-id="8ee96-114">The standard WCF Text Message Encoder is specially configured to use the <xref:System.ServiceModel.Channels.MessageVersion.None%2A> value, which allows it to process XML message payloads that do not arrive wrapped in a SOAP envelope.</span></span>

<span data-ttu-id="8ee96-115">使用 POX 消息通过 HTTP 进行通信的 WCF 客户端使用类似的绑定 (如下命令性代码) 中所示。</span><span class="sxs-lookup"><span data-stu-id="8ee96-115">WCF clients that communicate over HTTP using POX messages use a similar binding (shown in the following imperative code).</span></span>

```csharp
private static Binding CreatePoxBinding()
{
    TextMessageEncodingBindingElement encoder =
        new TextMessageEncodingBindingElement( MessageVersion.None, Encoding.UTF8 );
    HttpTransportBindingElement transport = new HttpTransportBindingElement();
    transport.ManualAddressing = true;
    return new CustomBinding( new BindingElement[] { encoder, transport } );
}
```

<span data-ttu-id="8ee96-116">因为 POX 客户端必须显式指定将消息发送到的 URI，所以它们通常必须将 <xref:System.ServiceModel.Channels.HttpTransportBindingElement> 配置为手动寻址模式，方法是将该元素的 <xref:System.ServiceModel.Channels.TransportBindingElement.ManualAddressing%2A> 属性设置为 `true`。</span><span class="sxs-lookup"><span data-stu-id="8ee96-116">Because POX clients must explicitly specify the URIs to which they send messages, they usually must configure the <xref:System.ServiceModel.Channels.HttpTransportBindingElement> to a manual addressing mode by setting the <xref:System.ServiceModel.Channels.TransportBindingElement.ManualAddressing%2A> property to `true` on the element.</span></span> <span data-ttu-id="8ee96-117">这样，应用程序代码就可以对消息进行显式寻址，因此，当应用程序将消息发送到不同的 HTTP URI 时，不必每次都创建一个新的 <xref:System.ServiceModel.ChannelFactory>。</span><span class="sxs-lookup"><span data-stu-id="8ee96-117">This allows messages to be addressed explicitly by application code and it is not necessary to create a new <xref:System.ServiceModel.ChannelFactory> every time an application sends a message to a different HTTP URI.</span></span>

<span data-ttu-id="8ee96-118">因为 POX 消息不使用 SOAP 标头传送重要的协议信息，所以 POX 客户端和服务通常必须操作用于发送或接收消息的基础 HTTP 请求片段。</span><span class="sxs-lookup"><span data-stu-id="8ee96-118">Because POX messages do not use SOAP headers to convey important protocol information, POX clients and services often must manipulate pieces of the underlying HTTP request used to send or receive a message.</span></span> <span data-ttu-id="8ee96-119">Http 特定的协议信息，如 HTTP 标头和状态代码通过两个类出现在 WCF 编程模型中：</span><span class="sxs-lookup"><span data-stu-id="8ee96-119">HTTP-specific protocol information such as the HTTP headers and status codes are surfaced in the WCF programming model through two classes:</span></span>

- <span data-ttu-id="8ee96-120"><xref:System.ServiceModel.Channels.HttpRequestMessageProperty>，包含有关 HTTP 请求的信息，例如 HTTP 方法和请求标头。</span><span class="sxs-lookup"><span data-stu-id="8ee96-120"><xref:System.ServiceModel.Channels.HttpRequestMessageProperty>, which contains information about the HTTP request, such as the HTTP method and request headers.</span></span>

- <span data-ttu-id="8ee96-121"><xref:System.ServiceModel.Channels.HttpResponseMessageProperty>，包含有关 HTTP 响应的信息（例如 HTTP 状态代码和状态说明）以及任何 HTTP 响应标头。</span><span class="sxs-lookup"><span data-stu-id="8ee96-121"><xref:System.ServiceModel.Channels.HttpResponseMessageProperty>, which contains information about the HTTP response, such as the HTTP status code and status description, as well as any HTTP response headers.</span></span>
  
<span data-ttu-id="8ee96-122">下面的代码示例演示如何创建一个发送到的 HTTP GET 请求消息 `http://localhost:8100/customers` 。</span><span class="sxs-lookup"><span data-stu-id="8ee96-122">The following code example shows how to create an HTTP GET request message that is addressed to `http://localhost:8100/customers`.</span></span>

```csharp
Message request = Message.CreateMessage( MessageVersion.None, String.Empty );
request.Headers.To = "http://localhost:8100/customers";

HttpRequestMessageProperty property = new HttpRequestMessageProperty();
property.Method = "GET";
property.SuppressEntityBody = true;
request.Properties.Add( HttpRequestMessageProperty.Name, property );
```

<span data-ttu-id="8ee96-123">首先，通过调用 <xref:System.ServiceModel.Channels.Message> 创建一个空请求 <xref:System.ServiceModel.Channels.Message.CreateMessage%28System.ServiceModel.Channels.MessageVersion%2CSystem.String%29>。</span><span class="sxs-lookup"><span data-stu-id="8ee96-123">First, an empty request <xref:System.ServiceModel.Channels.Message> is created by calling <xref:System.ServiceModel.Channels.Message.CreateMessage%28System.ServiceModel.Channels.MessageVersion%2CSystem.String%29>.</span></span> <span data-ttu-id="8ee96-124"><xref:System.ServiceModel.Channels.MessageVersion.None%2A> 参数用于指示 SOAP 信封不是必需的并且 <xref:System.String.Empty> 参数作为 Action 传递。</span><span class="sxs-lookup"><span data-stu-id="8ee96-124">The <xref:System.ServiceModel.Channels.MessageVersion.None%2A> parameter is used to indicate that a SOAP envelope is not required and <xref:System.String.Empty> parameter is passed as the Action.</span></span> <span data-ttu-id="8ee96-125">然后，通过将 <xref:System.ServiceModel.Channels.MessageHeaders.To%2A> 标头设置为所需的 URI，对请求消息进行寻址。</span><span class="sxs-lookup"><span data-stu-id="8ee96-125">The request message is then addressed by setting <xref:System.ServiceModel.Channels.MessageHeaders.To%2A> header to the desired URI.</span></span> <span data-ttu-id="8ee96-126">接下来，创建一个 <xref:System.ServiceModel.Channels.HttpRequestMessageProperty>，并将 <xref:System.ServiceModel.Channels.HttpRequestMessageProperty.Method%2A> 设置为 HTTP 谓词 GET 方法，将 <xref:System.ServiceModel.Channels.HttpRequestMessageProperty.SuppressEntityBody%2A> 设置为 `true`，以指示不应在传出 HTTP 请求消息的消息正文中发送任何数据。</span><span class="sxs-lookup"><span data-stu-id="8ee96-126">Next, an <xref:System.ServiceModel.Channels.HttpRequestMessageProperty> is created and the <xref:System.ServiceModel.Channels.HttpRequestMessageProperty.Method%2A> is set to the HTTP verb GET method and the <xref:System.ServiceModel.Channels.HttpRequestMessageProperty.SuppressEntityBody%2A> is set to `true` to indicate that no data should be sent in the body of the outgoing HTTP request message.</span></span> <span data-ttu-id="8ee96-127">最后，将请求属性添加到请求消息的 <xref:System.ServiceModel.Channels.Message.Properties%2A> 集合中，以便它能影响 HTTP 传输协议发送该请求的方式。</span><span class="sxs-lookup"><span data-stu-id="8ee96-127">Finally, the request property is added to the <xref:System.ServiceModel.Channels.Message.Properties%2A> collection of the request message so it can influence how the HTTP Transport sends the request.</span></span> <span data-ttu-id="8ee96-128">这样，该消息就准备好通过 <xref:System.ServiceModel.Channels.IRequestChannel> 的相应实例进行发送了。</span><span class="sxs-lookup"><span data-stu-id="8ee96-128">The message is then ready to be sent over an appropriate instance of the <xref:System.ServiceModel.Channels.IRequestChannel>.</span></span>

<span data-ttu-id="8ee96-129">可以对服务使用类似的技术，以便从传入的消息中提取 <xref:System.ServiceModel.Channels.HttpRequestMessageProperty> 并构造响应。</span><span class="sxs-lookup"><span data-stu-id="8ee96-129">Similar techniques can be used on the service to extract the <xref:System.ServiceModel.Channels.HttpRequestMessageProperty> from an incoming message and construct a response.</span></span>
