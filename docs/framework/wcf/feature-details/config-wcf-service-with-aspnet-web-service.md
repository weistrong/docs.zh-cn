---
description: 了解详细信息：如何：配置 WCF 服务以便与 ASP.NET Web 服务客户端进行互操作
title: 如何：配置 WCF 服务以与 ASP.NET Web 服务客户端进行互操作
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 48e1cd90-de80-4d6c-846e-631878955762
ms.openlocfilehash: 180307763054f8dfe5696fb0bbf294ec2b5ee3db
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99743390"
---
# <a name="how-to-configure-wcf-service-to-interoperate-with-aspnet-web-service-clients"></a><span data-ttu-id="9a51e-103">如何：配置 WCF 服务以与 ASP.NET Web 服务客户端进行互操作</span><span class="sxs-lookup"><span data-stu-id="9a51e-103">How to: Configure WCF Service to Interoperate with ASP.NET Web Service Clients</span></span>

<span data-ttu-id="9a51e-104">若要将 Windows Communication Foundation (WCF) 服务终结点配置为可与 ASP.NET Web 服务客户端进行互操作，请使用 <xref:System.ServiceModel.BasicHttpBinding?displayProperty=nameWithType> 类型作为服务终结点的绑定类型。</span><span class="sxs-lookup"><span data-stu-id="9a51e-104">To configure a Windows Communication Foundation (WCF) service endpoint to be interoperable with ASP.NET Web service clients, use the <xref:System.ServiceModel.BasicHttpBinding?displayProperty=nameWithType> type as the binding type for your service endpoint.</span></span>  
  
 <span data-ttu-id="9a51e-105">你可以根据需要在该绑定上启用对 HTTPS 和传输级客户端身份验证的支持。</span><span class="sxs-lookup"><span data-stu-id="9a51e-105">You can optionally enable support for HTTPS and transport-level client authentication on the binding.</span></span> <span data-ttu-id="9a51e-106">ASP.NET Web 服务客户端不支持 MTOM 消息编码，因此 <xref:System.ServiceModel.BasicHttpBinding.MessageEncoding%2A?displayProperty=nameWithType> 属性应保留为其默认值，即 <xref:System.ServiceModel.WSMessageEncoding.Text?displayProperty=nameWithType> 。</span><span class="sxs-lookup"><span data-stu-id="9a51e-106">ASP.NET Web service clients do not support MTOM message encoding, so the <xref:System.ServiceModel.BasicHttpBinding.MessageEncoding%2A?displayProperty=nameWithType> property should be left as its default value, which is <xref:System.ServiceModel.WSMessageEncoding.Text?displayProperty=nameWithType>.</span></span> <span data-ttu-id="9a51e-107">ASP.NET Web 服务客户端不支持 WS 安全，因此 <xref:System.ServiceModel.BasicHttpBinding.Security%2A?displayProperty=nameWithType> 应将设置为 <xref:System.ServiceModel.BasicHttpSecurityMode.Transport> 。</span><span class="sxs-lookup"><span data-stu-id="9a51e-107">ASP.NET Web Service clients do not support WS-Security, so the <xref:System.ServiceModel.BasicHttpBinding.Security%2A?displayProperty=nameWithType> should be set to <xref:System.ServiceModel.BasicHttpSecurityMode.Transport>.</span></span>  
  
 <span data-ttu-id="9a51e-108">若要使 WCF 服务的元数据可用于 ASP.NET Web 服务代理生成工具 (即， [Web 服务描述语言工具 ( # A0)](/previous-versions/dotnet/netframework-4.0/7h3ystb6(v=vs.100))、 [Web 服务发现工具 ( # A1)](/previous-versions/dotnet/netframework-4.0/cy2a3ybs(v=vs.100))以及 Visual Studio 中的 " **添加 Web 引用** " 功能) ，你应公开 HTTP/GET 元数据终结点。</span><span class="sxs-lookup"><span data-stu-id="9a51e-108">To make the metadata for a WCF service available to ASP.NET Web service proxy generation tools (that is, [Web Services Description Language Tool (Wsdl.exe)](/previous-versions/dotnet/netframework-4.0/7h3ystb6(v=vs.100)), [Web Services Discovery Tool (Disco.exe)](/previous-versions/dotnet/netframework-4.0/cy2a3ybs(v=vs.100)), and the **Add Web Reference** feature in Visual Studio), you should expose an HTTP/GET metadata endpoint.</span></span>  
  
## <a name="add-an-endpoint-in-code"></a><span data-ttu-id="9a51e-109">在代码中添加终结点</span><span class="sxs-lookup"><span data-stu-id="9a51e-109">Add an endpoint in code</span></span>  
  
1. <span data-ttu-id="9a51e-110">创建一个新的 <xref:System.ServiceModel.BasicHttpBinding> 实例。</span><span class="sxs-lookup"><span data-stu-id="9a51e-110">Create a new <xref:System.ServiceModel.BasicHttpBinding> instance</span></span>  
  
2. <span data-ttu-id="9a51e-111">（可选）将此服务终结点绑定的安全模式设置为 <xref:System.ServiceModel.BasicHttpSecurityMode.Transport>，从而为此绑定启用传输安全。</span><span class="sxs-lookup"><span data-stu-id="9a51e-111">Optionally enable transport security for this service endpoint binding by setting the security mode for the binding to <xref:System.ServiceModel.BasicHttpSecurityMode.Transport>.</span></span> <span data-ttu-id="9a51e-112">有关详细信息，请参阅 [传输安全性](transport-security.md)。</span><span class="sxs-lookup"><span data-stu-id="9a51e-112">For details, see [Transport Security](transport-security.md).</span></span>  
  
3. <span data-ttu-id="9a51e-113">使用刚创建的绑定实例，向服务主机添加一个新的应用程序终结点。</span><span class="sxs-lookup"><span data-stu-id="9a51e-113">Add a new application endpoint to your service host using the binding instance that you just created.</span></span> <span data-ttu-id="9a51e-114">有关如何在代码中添加服务终结点的详细信息，请参阅 [如何：在代码中创建服务终结点](how-to-create-a-service-endpoint-in-code.md)。</span><span class="sxs-lookup"><span data-stu-id="9a51e-114">For details about how to add a service endpoint in code, see the [How to: Create a Service Endpoint in Code](how-to-create-a-service-endpoint-in-code.md).</span></span>  
  
4. <span data-ttu-id="9a51e-115">为服务启用一个 HTTP/GET 元数据终结点。</span><span class="sxs-lookup"><span data-stu-id="9a51e-115">Enable an HTTP/GET metadata endpoint for your service.</span></span> <span data-ttu-id="9a51e-116">有关详细信息，请参阅 [如何：使用代码发布服务的元数据](how-to-publish-metadata-for-a-service-using-code.md)。</span><span class="sxs-lookup"><span data-stu-id="9a51e-116">For details see [How to: Publish Metadata for a Service Using Code](how-to-publish-metadata-for-a-service-using-code.md).</span></span>  
  
## <a name="add-an-endpoint-in-a-configuration-file"></a><span data-ttu-id="9a51e-117">在配置文件中添加终结点</span><span class="sxs-lookup"><span data-stu-id="9a51e-117">Add an endpoint in a configuration file</span></span>  
  
1. <span data-ttu-id="9a51e-118">创建一个新的 <xref:System.ServiceModel.BasicHttpBinding> 绑定配置。</span><span class="sxs-lookup"><span data-stu-id="9a51e-118">Create a new <xref:System.ServiceModel.BasicHttpBinding> binding configuration.</span></span> <span data-ttu-id="9a51e-119">有关详细信息，请参阅 [如何：在配置中指定服务绑定](../how-to-specify-a-service-binding-in-configuration.md)。</span><span class="sxs-lookup"><span data-stu-id="9a51e-119">For details, see the [How to: Specify a Service Binding in Configuration](../how-to-specify-a-service-binding-in-configuration.md).</span></span>  
  
2. <span data-ttu-id="9a51e-120">（可选）将此服务终结点绑定的安全模式设置为 <xref:System.ServiceModel.BasicHttpSecurityMode.Transport>，从而为此绑定配置启用传输安全。</span><span class="sxs-lookup"><span data-stu-id="9a51e-120">Optionally enable transport security for this service endpoint binding configuration by setting the security mode for the binding to <xref:System.ServiceModel.BasicHttpSecurityMode.Transport>.</span></span> <span data-ttu-id="9a51e-121">有关详细信息，请参阅 [传输安全性](transport-security.md)。</span><span class="sxs-lookup"><span data-stu-id="9a51e-121">For details, see [Transport Security](transport-security.md).</span></span>  
  
3. <span data-ttu-id="9a51e-122">使用刚创建的绑定配置，为服务配置一个新的应用程序终结点。</span><span class="sxs-lookup"><span data-stu-id="9a51e-122">Configure a new application endpoint for your service using the binding configuration that you just created.</span></span> <span data-ttu-id="9a51e-123">有关如何在配置文件中添加服务终结点的详细信息，请参阅 [如何：在配置中创建服务终结点](how-to-create-a-service-endpoint-in-configuration.md)。</span><span class="sxs-lookup"><span data-stu-id="9a51e-123">For details about how to add a service endpoint in a configuration file, see the [How to: Create a Service Endpoint in Configuration](how-to-create-a-service-endpoint-in-configuration.md).</span></span>  
  
4. <span data-ttu-id="9a51e-124">为服务启用一个 HTTP/GET 元数据终结点。</span><span class="sxs-lookup"><span data-stu-id="9a51e-124">Enable an HTTP/GET metadata endpoint for your service.</span></span> <span data-ttu-id="9a51e-125">有关详细信息，请参阅 [如何：使用配置文件发布服务的元数据](how-to-publish-metadata-for-a-service-using-a-configuration-file.md)。</span><span class="sxs-lookup"><span data-stu-id="9a51e-125">For details see the [How to: Publish Metadata for a Service Using a Configuration File](how-to-publish-metadata-for-a-service-using-a-configuration-file.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="9a51e-126">示例</span><span class="sxs-lookup"><span data-stu-id="9a51e-126">Example</span></span>  

 <span data-ttu-id="9a51e-127">下面的代码示例演示如何在代码中或在配置文件中添加与 ASP.NET Web 服务客户端兼容的 WCF 终结点。</span><span class="sxs-lookup"><span data-stu-id="9a51e-127">The following example code demonstrates how to add a WCF endpoint that is compatible with ASP.NET Web service clients in code and alternatively in configuration files.</span></span>  
  
 [!code-csharp[C_HowTo-WCFServiceAndASMXClient#0](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_howto-wcfserviceandasmxclient/cs/program.cs#0)]
 [!code-vb[C_HowTo-WCFServiceAndASMXClient#0](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/c_howto-wcfserviceandasmxclient/vb/program.vb#0)]
 [!code-xml[C_HowTo-WCFServiceAndASMXClient#1](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_howto-wcfserviceandasmxclient/common/app.config#1)]
  
## <a name="see-also"></a><span data-ttu-id="9a51e-128">请参阅</span><span class="sxs-lookup"><span data-stu-id="9a51e-128">See also</span></span>

- [<span data-ttu-id="9a51e-129">如何：在代码中创建服务终结点</span><span class="sxs-lookup"><span data-stu-id="9a51e-129">How to: Create a Service Endpoint in Code</span></span>](how-to-create-a-service-endpoint-in-code.md)
- [<span data-ttu-id="9a51e-130">如何：使用代码发布服务的元数据</span><span class="sxs-lookup"><span data-stu-id="9a51e-130">How to: Publish Metadata for a Service Using Code</span></span>](how-to-publish-metadata-for-a-service-using-code.md)
- [<span data-ttu-id="9a51e-131">如何：在配置中指定服务绑定</span><span class="sxs-lookup"><span data-stu-id="9a51e-131">How to: Specify a Service Binding in Configuration</span></span>](../how-to-specify-a-service-binding-in-configuration.md)
- [<span data-ttu-id="9a51e-132">如何：在配置中创建服务终结点</span><span class="sxs-lookup"><span data-stu-id="9a51e-132">How to: Create a Service Endpoint in Configuration</span></span>](how-to-create-a-service-endpoint-in-configuration.md)
- [<span data-ttu-id="9a51e-133">如何：使用配置文件发布服务的元数据</span><span class="sxs-lookup"><span data-stu-id="9a51e-133">How to: Publish Metadata for a Service Using a Configuration File</span></span>](how-to-publish-metadata-for-a-service-using-a-configuration-file.md)
- [<span data-ttu-id="9a51e-134">传输安全</span><span class="sxs-lookup"><span data-stu-id="9a51e-134">Transport Security</span></span>](transport-security.md)
- [<span data-ttu-id="9a51e-135">使用元数据</span><span class="sxs-lookup"><span data-stu-id="9a51e-135">Using Metadata</span></span>](using-metadata.md)
