---
description: 了解详细信息：如何：使用 WCF 客户端访问 WSE 3.0 服务
title: 如何：使用 WCF 客户端访问 WSE 3.0 服务
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 1f9bcd9b-8f8f-47fa-8f1e-0d47236eb800
ms.openlocfilehash: 5a117b4c3d743d783c37ed3e27e3cf11e44abec3
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99742922"
---
# <a name="how-to-access-a-wse-30-service-with-a-wcf-client"></a><span data-ttu-id="375ca-103">如何：使用 WCF 客户端访问 WSE 3.0 服务</span><span class="sxs-lookup"><span data-stu-id="375ca-103">How to: Access a WSE 3.0 Service with a WCF Client</span></span>

<span data-ttu-id="375ca-104">当 WCF 客户端配置为使用) 规范的8月2004版时，Windows Communication Foundation (WCF) 客户端与 Web 服务增强功能兼容 (WSE Microsoft .NET 3.0。</span><span class="sxs-lookup"><span data-stu-id="375ca-104">Windows Communication Foundation (WCF) clients are wire-level compatible with Web Services Enhancements (WSE) 3.0 for Microsoft .NET services when WCF clients are configured to use the August 2004 version of the WS-Addressing specification.</span></span> <span data-ttu-id="375ca-105">但是，WSE 3.0 服务不支持 (MEX) 协议的元数据交换，因此，当你使用配置的 [元数据实用工具工具 ( # A0) ](../servicemodel-metadata-utility-tool-svcutil-exe.md) 创建 wcf 客户端类时，安全设置不会应用于生成的 wcf 客户端。</span><span class="sxs-lookup"><span data-stu-id="375ca-105">However, WSE 3.0 services do not support the metadata exchange (MEX) protocol, so when you use the [ServiceModel Metadata Utility Tool (Svcutil.exe)](../servicemodel-metadata-utility-tool-svcutil-exe.md) to create a WCF client class, the security settings are not applied to the generated WCF client.</span></span> <span data-ttu-id="375ca-106">因此，在生成 WCF 客户端之后，必须指定 WSE 3.0 服务所需的安全设置。</span><span class="sxs-lookup"><span data-stu-id="375ca-106">Therefore, you must specify the security settings that the WSE 3.0 service requires after the WCF client is generated.</span></span>  
  
 <span data-ttu-id="375ca-107">你可以通过使用自定义绑定来应用这些安全设置，以考虑 wse 3.0 服务的要求以及 WSE 3.0 服务和 WCF 客户端之间的互操作要求。</span><span class="sxs-lookup"><span data-stu-id="375ca-107">You can apply these security settings by using a custom binding to take into account the WSE 3.0 service's requirements and the interoperable requirements between a WSE 3.0 service and a WCF client.</span></span> <span data-ttu-id="375ca-108">这些互操作性需求包括前面提到的使用 2004 年 8 月版的 WS-Addressing 规范和 <xref:System.ServiceModel.Security.MessageProtectionOrder.SignBeforeEncrypt> 的 WSE 3.0 默认消息保护。</span><span class="sxs-lookup"><span data-stu-id="375ca-108">These interoperability requirements include the aforementioned use of the August 2004 WS-Addressing specification and the  WSE 3.0default message protection of <xref:System.ServiceModel.Security.MessageProtectionOrder.SignBeforeEncrypt>.</span></span> <span data-ttu-id="375ca-109">WCF 的默认消息保护为 <xref:System.ServiceModel.Security.MessageProtectionOrder.SignBeforeEncryptAndEncryptSignature> 。</span><span class="sxs-lookup"><span data-stu-id="375ca-109">The default message protection for WCF is <xref:System.ServiceModel.Security.MessageProtectionOrder.SignBeforeEncryptAndEncryptSignature>.</span></span> <span data-ttu-id="375ca-110">本主题详细说明如何创建与 WSE 3.0 服务互操作的 WCF 绑定。</span><span class="sxs-lookup"><span data-stu-id="375ca-110">This topic details how to create a WCF binding that interoperates with a WSE 3.0 service.</span></span> <span data-ttu-id="375ca-111">WCF 还提供了包含此绑定的示例。</span><span class="sxs-lookup"><span data-stu-id="375ca-111">WCF also provides a sample that incorporates this binding.</span></span> <span data-ttu-id="375ca-112">有关此示例的详细信息，请参阅 [与 .Asmx Web 服务互](../samples/interoperating-with-asmx-web-services.md)操作。</span><span class="sxs-lookup"><span data-stu-id="375ca-112">For more information about this sample, see [Interoperating with ASMX Web Services](../samples/interoperating-with-asmx-web-services.md).</span></span>  
  
### <a name="to-access-a-wse-30-web-service-with-a-wcf-client"></a><span data-ttu-id="375ca-113">使用 WCF 客户端访问 WSE 3.0 Web 服务</span><span class="sxs-lookup"><span data-stu-id="375ca-113">To access a WSE 3.0 Web service with a WCF client</span></span>  
  
1. <span data-ttu-id="375ca-114">运行 "工作网络 [元数据实用工具" 工具 ( # A0) ](../servicemodel-metadata-utility-tool-svcutil-exe.md) 为 WSE 3.0 Web 服务创建 WCF 客户端。</span><span class="sxs-lookup"><span data-stu-id="375ca-114">Run the [ServiceModel Metadata Utility Tool (Svcutil.exe)](../servicemodel-metadata-utility-tool-svcutil-exe.md) to create a WCF client for the WSE 3.0 Web service.</span></span>  
  
     <span data-ttu-id="375ca-115">对于 WSE 3.0 Web 服务，将创建 WCF 客户端。</span><span class="sxs-lookup"><span data-stu-id="375ca-115">For a WSE 3.0 Web service, a WCF client is created.</span></span> <span data-ttu-id="375ca-116">因为 WSE 3.0 不支持 MEX 协议，因此不能使用该工具检索 Web 服务的安全要求。</span><span class="sxs-lookup"><span data-stu-id="375ca-116">Because WSE 3.0 does not support the MEX protocol, you cannot use the tool to retrieve the security requirements for the Web service.</span></span> <span data-ttu-id="375ca-117">应用程序开发人员必须为客户端添加安全设置。</span><span class="sxs-lookup"><span data-stu-id="375ca-117">The application developer must add the security settings for the client.</span></span>  
  
     <span data-ttu-id="375ca-118">有关创建 WCF 客户端的详细信息，请参阅 [如何：创建客户端](../how-to-create-a-wcf-client.md)。</span><span class="sxs-lookup"><span data-stu-id="375ca-118">For more information about creating a WCF client, see the [How to: Create a Client](../how-to-create-a-wcf-client.md).</span></span>  
  
2. <span data-ttu-id="375ca-119">创建一个类，表示可与 WSE 3.0 Web 服务进行通信的绑定。</span><span class="sxs-lookup"><span data-stu-id="375ca-119">Create a class that represents a binding that can communicate with WSE 3.0 Web services.</span></span>  
  
     <span data-ttu-id="375ca-120">以下类是 [与 WSE 示例互](/previous-versions/dotnet/netframework-3.5/ms752257(v=vs.90)) 操作的一部分：</span><span class="sxs-lookup"><span data-stu-id="375ca-120">The following class is part of the [Interoperating with WSE](/previous-versions/dotnet/netframework-3.5/ms752257(v=vs.90)) sample:</span></span>  
  
    1. <span data-ttu-id="375ca-121">创建一个从 <xref:System.ServiceModel.Channels.Binding> 类派生的类。</span><span class="sxs-lookup"><span data-stu-id="375ca-121">Create a class that derives from the <xref:System.ServiceModel.Channels.Binding> class.</span></span>  
  
         <span data-ttu-id="375ca-122">下面的代码示例创建一个从 `WseHttpBinding` 类派生的名为 <xref:System.ServiceModel.Channels.Binding> 的类。</span><span class="sxs-lookup"><span data-stu-id="375ca-122">The following code example creates a class named `WseHttpBinding` that derives from the <xref:System.ServiceModel.Channels.Binding> class.</span></span>  
  
         [!code-csharp[c_WCFClientToWSEService#1](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_wcfclienttowseservice/cs/wsehttpbinding.cs#1)]
         [!code-vb[c_WCFClientToWSEService#1](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/c_wcfclienttowseservice/vb/wsehttpbinding.vb#1)]  
  
    2. <span data-ttu-id="375ca-123">向该类中添加属性，用以指定 WSE 服务使用的 WSE 完整断言、是否需要派生密钥、是否使用安全会话、是否需要签名确认以及消息保护设置。</span><span class="sxs-lookup"><span data-stu-id="375ca-123">Add properties to the class that specify the WSE turnkey assertion used by the WSE service, whether derived keys are required, whether secure sessions are used, whether signature confirmations are required, and the message protection settings.</span></span> <span data-ttu-id="375ca-124">在 WSE 3.0 中，交钥匙断言指定客户端或 Web 服务的安全要求，类似于 WCF 中绑定的身份验证模式。</span><span class="sxs-lookup"><span data-stu-id="375ca-124">In WSE 3.0, a turnkey assertion specifies the security requirements for a client or Web service—similar to the authentication mode of a binding in WCF.</span></span>  
  
         <span data-ttu-id="375ca-125">下面的代码示例定义了 `SecurityAssertion`、`RequireDerivedKeys`、`EstablishSecurityContext` 和 `MessageProtectionOrder` 属性，这些属性分别指定 WSE 完整断言、是否需要派生密钥、是否使用安全会话、是否需要签名确认以及消息保护设置。</span><span class="sxs-lookup"><span data-stu-id="375ca-125">The following code example defines the `SecurityAssertion`, `RequireDerivedKeys`, `EstablishSecurityContext`, and `MessageProtectionOrder` properties that specify the WSE turnkey assertion, whether derived keys are required, whether secure sessions are used, whether signature confirmations are required, and the message protection settings, respectively.</span></span>  
  
         [!code-csharp[c_WCFClientToWSEService#3](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_wcfclienttowseservice/cs/wsehttpbinding.cs#3)]
         [!code-vb[c_WCFClientToWSEService#3](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/c_wcfclienttowseservice/vb/wsehttpbinding.vb#3)]  
  
    3. <span data-ttu-id="375ca-126">重写 <xref:System.ServiceModel.Channels.Binding.CreateBindingElements%2A> 方法以设置绑定属性。</span><span class="sxs-lookup"><span data-stu-id="375ca-126">Override the <xref:System.ServiceModel.Channels.Binding.CreateBindingElements%2A> method to set the binding properties.</span></span>  
  
         <span data-ttu-id="375ca-127">下面的代码示例通过获取 `SecurityAssertion` 和 `MessageProtectionOrder` 属性的值来指定传输协议、消息编码和消息保护设置。</span><span class="sxs-lookup"><span data-stu-id="375ca-127">The following code example specifies the transport, message encoding, and message protection settings by getting the values of the `SecurityAssertion` and `MessageProtectionOrder` properties.</span></span>  
  
         [!code-csharp[c_WCFClientToWSEService#2](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_wcfclienttowseservice/cs/wsehttpbinding.cs#2)]
         [!code-vb[c_WCFClientToWSEService#2](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/c_wcfclienttowseservice/vb/wsehttpbinding.vb#2)]  
  
3. <span data-ttu-id="375ca-128">在客户端应用程序代码中，添加设置绑定属性的代码。</span><span class="sxs-lookup"><span data-stu-id="375ca-128">In the client application code, add code to set the binding properties.</span></span>  
  
     <span data-ttu-id="375ca-129">下面的代码示例指定 WCF 客户端必须使用由 WSE 3.0 `AnonymousForCertificate` 交钥匙安全声明定义的消息保护和身份验证。</span><span class="sxs-lookup"><span data-stu-id="375ca-129">The following code example specifies that the WCF client must use message protection and authentication as defined by the WSE 3.0 `AnonymousForCertificate` turnkey security assertion.</span></span> <span data-ttu-id="375ca-130">此外，还需要安全会话和派生密钥。</span><span class="sxs-lookup"><span data-stu-id="375ca-130">Additionally, secure sessions and derived keys are required.</span></span>  
  
     [!code-csharp[c_WCFClientToWSEService#4](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_wcfclienttowseservice/cs/client.cs#4)]
     [!code-vb[c_WCFClientToWSEService#4](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/c_wcfclienttowseservice/vb/client.vb#4)]  
  
## <a name="example"></a><span data-ttu-id="375ca-131">示例</span><span class="sxs-lookup"><span data-stu-id="375ca-131">Example</span></span>  

 <span data-ttu-id="375ca-132">下面的代码示例定义了一个自定义绑定，该绑定公开对应于 WSE 3.0 完整安全断言的各个属性的属性。</span><span class="sxs-lookup"><span data-stu-id="375ca-132">The following code example defines a custom binding that exposes properties that correspond to the properties of a WSE 3.0 turnkey security assertion.</span></span> <span data-ttu-id="375ca-133">然后，使用名为的自定义绑定 `WseHttpBinding` 来指定 WCF 客户端的绑定属性，该客户端与 WSSECURITYANONYMOUS WSE 3.0 快速入门示例进行通信。</span><span class="sxs-lookup"><span data-stu-id="375ca-133">That custom binding, which is named `WseHttpBinding`, is then used to specify the binding properties for a WCF client that communicates with the WSSecurityAnonymous WSE 3.0 QuickStart sample.</span></span>  

## <a name="see-also"></a><span data-ttu-id="375ca-134">请参阅</span><span class="sxs-lookup"><span data-stu-id="375ca-134">See also</span></span>

- <xref:System.ServiceModel.Channels.Binding>
- <span data-ttu-id="375ca-135">[与 WSE 互操作](/previous-versions/dotnet/netframework-3.5/ms752257(v=vs.90))</span><span class="sxs-lookup"><span data-stu-id="375ca-135">[Interoperating with WSE](/previous-versions/dotnet/netframework-3.5/ms752257(v=vs.90))</span></span>
