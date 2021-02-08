---
description: 了解详细信息：如何：配置 WCF 客户端以与 WSE 3.0 服务互操作
title: 如何：配置 WCF 客户端以与 WSE3.0 服务进行互操作
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 3dadd7f1-d207-4ea5-a73b-3e8aa44407f8
ms.openlocfilehash: 97de90c491a29cdacf881a92013a11db6aea416f
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99780123"
---
# <a name="how-to-configure-a-wcf-client-to-interoperate-with-wse30-services"></a><span data-ttu-id="427ec-103">如何：配置 WCF 客户端以与 WSE3.0 服务进行互操作</span><span class="sxs-lookup"><span data-stu-id="427ec-103">How to: Configure a WCF Client to interoperate with WSE3.0 Services</span></span>

<span data-ttu-id="427ec-104">将 WCF 客户端配置为使用 (规范的8月2004版时，Windows Communication Foundation (WCF) 客户端与 Web 服务增强 3.0 Microsoft .NET 的线路级别兼容。</span><span class="sxs-lookup"><span data-stu-id="427ec-104">Windows Communication Foundation (WCF) clients are wire-level compatible with Web Services Enhancements 3.0 for Microsoft .NET (WSE) services when WCF clients are configured to use the August 2004 version of the WS-Addressing specification.</span></span>  
  
### <a name="to-configure-a-wcf-client-to-interoperate-with-a-wse-30-web-service"></a><span data-ttu-id="427ec-105">配置 WCF 客户端以与 WSE 3.0 Web 服务进行互操作</span><span class="sxs-lookup"><span data-stu-id="427ec-105">To configure a WCF client to interoperate with a WSE 3.0 Web service</span></span>  
  
1. <span data-ttu-id="427ec-106">运行 "工作网络 [元数据实用工具" 工具 ( # A0) ](../servicemodel-metadata-utility-tool-svcutil-exe.md) 为 WSE 3.0 Web 服务创建 WCF 客户端。</span><span class="sxs-lookup"><span data-stu-id="427ec-106">Run the [ServiceModel Metadata Utility Tool (Svcutil.exe)](../servicemodel-metadata-utility-tool-svcutil-exe.md) to create a WCF client for the WSE 3.0 Web service.</span></span>  
  
     <span data-ttu-id="427ec-107">对于 WSE Web 服务，将创建 WCF 客户端类。</span><span class="sxs-lookup"><span data-stu-id="427ec-107">For a WSE Web service, a WCF client class is created.</span></span>  
  
     <span data-ttu-id="427ec-108">有关创建 WCF 客户端的详细信息，请参阅 [如何：创建客户端](../how-to-create-a-wcf-client.md)。</span><span class="sxs-lookup"><span data-stu-id="427ec-108">For details about creating a WCF client, see the [How to: Create a Client](../how-to-create-a-wcf-client.md).</span></span>  
  
2. <span data-ttu-id="427ec-109">创建一个类，表示可与 WSE 3.0 Web 服务进行通信的绑定。</span><span class="sxs-lookup"><span data-stu-id="427ec-109">Create a class that represents a binding that can communicate with WSE 3.0 Web services.</span></span>  
  
     <span data-ttu-id="427ec-110">下面的类是 [与 WSE 示例互](/previous-versions/dotnet/netframework-3.5/ms752257(v=vs.90)) 操作的一部分。</span><span class="sxs-lookup"><span data-stu-id="427ec-110">The following class is part of the [Interoperating with WSE](/previous-versions/dotnet/netframework-3.5/ms752257(v=vs.90)) sample.</span></span>  
  
    1. <span data-ttu-id="427ec-111">创建一个从 <xref:System.ServiceModel.Channels.Binding> 类派生的类。</span><span class="sxs-lookup"><span data-stu-id="427ec-111">Create a class that derives from the <xref:System.ServiceModel.Channels.Binding> class.</span></span>  
  
         <span data-ttu-id="427ec-112">下面的代码示例创建一个从 `WseHttpBinding` 类派生的名为 <xref:System.ServiceModel.Channels.Binding> 的类。</span><span class="sxs-lookup"><span data-stu-id="427ec-112">The following code example creates a class named `WseHttpBinding` that derives from the <xref:System.ServiceModel.Channels.Binding> class.</span></span>  
  
         [!code-csharp[c_WCFClientToWSEService#1](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_wcfclienttowseservice/cs/wsehttpbinding.cs#1)]
         [!code-vb[c_WCFClientToWSEService#1](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/c_wcfclienttowseservice/vb/wsehttpbinding.vb#1)]  
  
    2. <span data-ttu-id="427ec-113">向该类添加指定 WSE 完整声明、是否需要派生密钥、是否使用安全会话、是否需要签名确认以及消息保护设置的属性。</span><span class="sxs-lookup"><span data-stu-id="427ec-113">Add properties to the class that specify the WSE turnkey assertion, whether derived keys are required, whether secure sessions are used, whether signature confirmations are required, and the message protection settings.</span></span>  
  
         <span data-ttu-id="427ec-114">下面的代码示例定义了 `SecurityAssertion` 、 `RequireDerivedKeys` 、 `EstablishSecurityContext` 和 `MessageProtectionOrder` 属性。</span><span class="sxs-lookup"><span data-stu-id="427ec-114">The following code example defines the `SecurityAssertion`, `RequireDerivedKeys`, `EstablishSecurityContext`, and `MessageProtectionOrder` properties.</span></span> <span data-ttu-id="427ec-115">它们指定 WSE 全包式断言、是否需要派生密钥、是否使用安全会话、是否需要签名确认以及消息保护设置。</span><span class="sxs-lookup"><span data-stu-id="427ec-115">They specify the WSE turnkey assertion, whether derived keys are required, whether secure sessions are used, whether signature confirmations are required, and the message protection settings, respectively.</span></span>  
  
         [!code-csharp[c_WCFClientToWSEService#3](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_wcfclienttowseservice/cs/wsehttpbinding.cs#3)]
         [!code-vb[c_WCFClientToWSEService#3](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/c_wcfclienttowseservice/vb/wsehttpbinding.vb#3)]  
  
    3. <span data-ttu-id="427ec-116">重写 <xref:System.ServiceModel.Channels.Binding.CreateBindingElements%2A> 方法以设置绑定属性。</span><span class="sxs-lookup"><span data-stu-id="427ec-116">Override the <xref:System.ServiceModel.Channels.Binding.CreateBindingElements%2A> method to set the binding properties.</span></span>  
  
         <span data-ttu-id="427ec-117">下面的代码示例通过获取 `SecurityAssertion` 和 `MessageProtectionOrder` 属性的值来指定传输协议、消息编码和消息保护设置。</span><span class="sxs-lookup"><span data-stu-id="427ec-117">The following code example specifies the transport, message encoding, and message protection settings by getting the values of the `SecurityAssertion` and `MessageProtectionOrder` properties.</span></span>  
  
         [!code-csharp[c_WCFClientToWSEService#2](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_wcfclienttowseservice/cs/wsehttpbinding.cs#2)]
         [!code-vb[c_WCFClientToWSEService#2](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/c_wcfclienttowseservice/vb/wsehttpbinding.vb#2)]  
  
3. <span data-ttu-id="427ec-118">在客户端应用程序代码中，添加设置绑定属性的代码。</span><span class="sxs-lookup"><span data-stu-id="427ec-118">In the client application code, add code to set the binding properties.</span></span>  
  
     <span data-ttu-id="427ec-119">下面的代码示例指定 WCF 客户端必须使用由 WSE 3.0 `AnonymousForCertificate` 交钥匙安全声明定义的消息保护和身份验证。</span><span class="sxs-lookup"><span data-stu-id="427ec-119">The following code example specifies that the WCF client must use message protection and authentication as defined by the WSE 3.0 `AnonymousForCertificate` turnkey security assertion.</span></span> <span data-ttu-id="427ec-120">此外，还需要安全会话和派生密钥。</span><span class="sxs-lookup"><span data-stu-id="427ec-120">Additionally, secure sessions and derived keys are required.</span></span>  
  
     [!code-csharp[c_WCFClientToWSEService#4](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_wcfclienttowseservice/cs/client.cs#4)]
     [!code-vb[c_WCFClientToWSEService#4](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/c_wcfclienttowseservice/vb/client.vb#4)]  
  
## <a name="example"></a><span data-ttu-id="427ec-121">示例</span><span class="sxs-lookup"><span data-stu-id="427ec-121">Example</span></span>  

 <span data-ttu-id="427ec-122">下面的代码示例定义了一个自定义绑定，该绑定公开对应于 WSE 3.0 完整安全断言的各个属性的属性。</span><span class="sxs-lookup"><span data-stu-id="427ec-122">The following code example defines a custom binding that exposes properties that correspond to the properties of a WSE 3.0 turnkey security assertion.</span></span> <span data-ttu-id="427ec-123">然后，将使用名为的自定义绑定 `WseHttpBinding` 来指定 WCF 客户端的绑定属性。</span><span class="sxs-lookup"><span data-stu-id="427ec-123">The custom binding, which is named `WseHttpBinding`, is then used to specify the binding properties for a WCF client.</span></span>  

[!code-csharp[c_WCFClientToWSEService#0](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_wcfclienttowseservice/cs/client.cs#0)]
[!code-vb[c_WCFClientToWSEService#0](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/c_wcfclienttowseservice/vb/client.vb#0)]  
  
## <a name="see-also"></a><span data-ttu-id="427ec-124">请参阅</span><span class="sxs-lookup"><span data-stu-id="427ec-124">See also</span></span>

- <xref:System.ServiceModel.Channels.Binding>
- <span data-ttu-id="427ec-125">[与 WSE 互操作](/previous-versions/dotnet/netframework-3.5/ms752257(v=vs.90))</span><span class="sxs-lookup"><span data-stu-id="427ec-125">[Interoperating with WSE](/previous-versions/dotnet/netframework-3.5/ms752257(v=vs.90))</span></span>
