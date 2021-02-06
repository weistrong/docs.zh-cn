---
description: 了解有关详细信息，请参阅如何：使用 x.509 证书保护服务
title: 如何：使用 X.509 证书保证服务的安全
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 2d06c2aa-d0d7-4e5e-ad7e-77416aa1c10b
ms.openlocfilehash: 57c8e78777c620fd3078651dbafbbf010fbd3768
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99643379"
---
# <a name="how-to-secure-a-service-with-an-x509-certificate"></a><span data-ttu-id="76290-103">如何：使用 X.509 证书保证服务的安全</span><span class="sxs-lookup"><span data-stu-id="76290-103">How to: Secure a Service with an X.509 Certificate</span></span>

<span data-ttu-id="76290-104">使用 x.509 证书保护服务是一项基本技术，其中 Windows Communication Foundation (WCF 中的大多数绑定) 使用。</span><span class="sxs-lookup"><span data-stu-id="76290-104">Securing a service with an X.509 certificate is a basic technique that most bindings in Windows Communication Foundation (WCF) use.</span></span> <span data-ttu-id="76290-105">本主题演练使用 X.509 证书配置自承载服务的步骤。</span><span class="sxs-lookup"><span data-stu-id="76290-105">This topic walks through the steps of configuring a self-hosted service with an X.509 certificate.</span></span>  
  
 <span data-ttu-id="76290-106">先决条件是具有可用于对服务器进行身份验证的有效证书。</span><span class="sxs-lookup"><span data-stu-id="76290-106">A prerequisite is a valid certificate that can be used to authenticate the server.</span></span> <span data-ttu-id="76290-107">证书必须由受信任的证书颁发机构颁发给服务器。</span><span class="sxs-lookup"><span data-stu-id="76290-107">The certificate must be issued to the server by a trusted certificate authority.</span></span> <span data-ttu-id="76290-108">如果证书无效，则尝试使用该服务的任何客户端都不会信任该服务，因此不会建立连接。</span><span class="sxs-lookup"><span data-stu-id="76290-108">If the certificate is not valid, any client trying to use the service will not trust the service, and consequently no connection will be made.</span></span> <span data-ttu-id="76290-109">有关使用证书的详细信息，请参阅使用 [证书](working-with-certificates.md)。</span><span class="sxs-lookup"><span data-stu-id="76290-109">For more information about using certificates, see [Working with Certificates](working-with-certificates.md).</span></span>  
  
### <a name="to-configure-a-service-with-a-certificate-using-code"></a><span data-ttu-id="76290-110">使用代码用证书配置服务</span><span class="sxs-lookup"><span data-stu-id="76290-110">To configure a service with a certificate using code</span></span>  
  
1. <span data-ttu-id="76290-111">创建服务协定和实现的服务。</span><span class="sxs-lookup"><span data-stu-id="76290-111">Create the service contract and the implemented service.</span></span> <span data-ttu-id="76290-112">有关详细信息，请参阅 [设计和实现服务](../designing-and-implementing-services.md)。</span><span class="sxs-lookup"><span data-stu-id="76290-112">For more information, see [Designing and Implementing Services](../designing-and-implementing-services.md).</span></span>  
  
2. <span data-ttu-id="76290-113">创建 <xref:System.ServiceModel.WSHttpBinding> 类的一个实例，并将其安全模式设置为 <xref:System.ServiceModel.SecurityMode.Message>，如下面的代码所示。</span><span class="sxs-lookup"><span data-stu-id="76290-113">Create an instance of the <xref:System.ServiceModel.WSHttpBinding> class and set its security mode to <xref:System.ServiceModel.SecurityMode.Message>, as shown in the following code.</span></span>  
  
     [!code-csharp[C_SecureWithCertificate#1](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_securewithcertificate/cs/source.cs#1)]
     [!code-vb[C_SecureWithCertificate#1](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/c_securewithcertificate/vb/source.vb#1)]  
  
3. <span data-ttu-id="76290-114">创建两个 <xref:System.Type> 变量，分别用于协定类型和实现的协定，如下面的代码所示。</span><span class="sxs-lookup"><span data-stu-id="76290-114">Create two <xref:System.Type> variables, one each for the contract type and the implemented contract, as shown in the following code.</span></span>  
  
     [!code-csharp[C_SecureWithCertificate#2](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_securewithcertificate/cs/source.cs#2)]
     [!code-vb[C_SecureWithCertificate#2](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/c_securewithcertificate/vb/source.vb#2)]  
  
4. <span data-ttu-id="76290-115">为服务的基址创建 <xref:System.Uri> 类的一个实例。</span><span class="sxs-lookup"><span data-stu-id="76290-115">Create an instance of the <xref:System.Uri> class for the base address of the service.</span></span> <span data-ttu-id="76290-116">由于 `WSHttpBinding` 使用 HTTP 传输，因此)  (URI 的统一资源标识符必须以该架构开头，否则在打开该服务时，Windows Communication Foundation (WCF) 会引发异常。</span><span class="sxs-lookup"><span data-stu-id="76290-116">Because the `WSHttpBinding` uses the HTTP transport, the Uniform Resource Identifier (URI) must begin with that schema, or Windows Communication Foundation (WCF) will throw an exception when the service is opened.</span></span>  
  
     [!code-csharp[C_SecureWithCertificate#3](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_securewithcertificate/cs/source.cs#3)]
     [!code-vb[C_SecureWithCertificate#3](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/c_securewithcertificate/vb/source.vb#3)]  
  
5. <span data-ttu-id="76290-117">使用实现的协定类型变量和 URI 创建 <xref:System.ServiceModel.ServiceHost> 类的新实例。</span><span class="sxs-lookup"><span data-stu-id="76290-117">Create a new instance of the <xref:System.ServiceModel.ServiceHost> class with the implemented contract type variable and the URI.</span></span>  
  
     [!code-csharp[C_SecureWithCertificate#4](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_securewithcertificate/cs/source.cs#4)]
     [!code-vb[C_SecureWithCertificate#4](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/c_securewithcertificate/vb/source.vb#4)]  
  
6. <span data-ttu-id="76290-118">使用 <xref:System.ServiceModel.Description.ServiceEndpoint> 方法向服务中添加一个 <xref:System.ServiceModel.ServiceHost.AddServiceEndpoint%2A>。</span><span class="sxs-lookup"><span data-stu-id="76290-118">Add a <xref:System.ServiceModel.Description.ServiceEndpoint> to the service using the <xref:System.ServiceModel.ServiceHost.AddServiceEndpoint%2A> method.</span></span> <span data-ttu-id="76290-119">将协定、绑定和终结点地址传递给构造函数，如下面的代码所示。</span><span class="sxs-lookup"><span data-stu-id="76290-119">Pass the contract, binding, and an endpoint address to the constructor, as shown in the following code.</span></span>  
  
     [!code-csharp[C_SecureWithCertificate#5](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_securewithcertificate/cs/source.cs#5)]
     [!code-vb[C_SecureWithCertificate#5](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/c_securewithcertificate/vb/source.vb#5)]  
  
7. <span data-ttu-id="76290-120">可选。</span><span class="sxs-lookup"><span data-stu-id="76290-120">Optional.</span></span> <span data-ttu-id="76290-121">若要从服务中检索元数据，请创建一个新的 <xref:System.ServiceModel.Description.ServiceMetadataBehavior> 对象并将 <xref:System.ServiceModel.Description.ServiceMetadataBehavior.HttpGetEnabled%2A> 属性设置为 `true`。</span><span class="sxs-lookup"><span data-stu-id="76290-121">To retrieve metadata from the service, create a new <xref:System.ServiceModel.Description.ServiceMetadataBehavior> object and set the <xref:System.ServiceModel.Description.ServiceMetadataBehavior.HttpGetEnabled%2A> property to `true`.</span></span>  
  
     [!code-csharp[C_SecureWithCertificate#6](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_securewithcertificate/cs/source.cs#6)]
     [!code-vb[C_SecureWithCertificate#6](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/c_securewithcertificate/vb/source.vb#6)]  
  
8. <span data-ttu-id="76290-122">使用 <xref:System.ServiceModel.Security.X509CertificateRecipientServiceCredential.SetCertificate%2A> 类的 <xref:System.ServiceModel.Security.X509CertificateRecipientServiceCredential> 方法将有效证书添加到服务中。</span><span class="sxs-lookup"><span data-stu-id="76290-122">Use the <xref:System.ServiceModel.Security.X509CertificateRecipientServiceCredential.SetCertificate%2A> method of the <xref:System.ServiceModel.Security.X509CertificateRecipientServiceCredential> class to add the valid certificate to the service.</span></span> <span data-ttu-id="76290-123">该方法可以使用多个方法之一查找证书。</span><span class="sxs-lookup"><span data-stu-id="76290-123">The method can use one of several methods to find a certificate.</span></span> <span data-ttu-id="76290-124">本示例使用 <xref:System.Security.Cryptography.X509Certificates.X509FindType.FindBySubjectName> 枚举。</span><span class="sxs-lookup"><span data-stu-id="76290-124">This example uses the <xref:System.Security.Cryptography.X509Certificates.X509FindType.FindBySubjectName> enumeration.</span></span> <span data-ttu-id="76290-125">该枚举指定提供的值是为其颁发证书的实体的名称。</span><span class="sxs-lookup"><span data-stu-id="76290-125">The enumeration specifies that the supplied value is the name of the entity that the certificate was issued to.</span></span>  
  
     [!code-csharp[C_SecureWithCertificate#7](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_securewithcertificate/cs/source.cs#7)]
     [!code-vb[C_SecureWithCertificate#7](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/c_securewithcertificate/vb/source.vb#7)]  
  
9. <span data-ttu-id="76290-126">调用 <xref:System.ServiceModel.Channels.CommunicationObject.Open%2A> 方法以开始服务侦听。</span><span class="sxs-lookup"><span data-stu-id="76290-126">Call the <xref:System.ServiceModel.Channels.CommunicationObject.Open%2A> method to start the service listening.</span></span> <span data-ttu-id="76290-127">如果您要创建控制台应用程序，请调用 <xref:System.Console.ReadLine%2A> 方法以保持服务处于侦听状态。</span><span class="sxs-lookup"><span data-stu-id="76290-127">If you are creating a console application, call the <xref:System.Console.ReadLine%2A> method to keep the service in the listening state.</span></span>  
  
     [!code-csharp[C_SecureWithCertificate#8](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_securewithcertificate/cs/source.cs#8)]
     [!code-vb[C_SecureWithCertificate#8](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/c_securewithcertificate/vb/source.vb#8)]  
  
## <a name="example"></a><span data-ttu-id="76290-128">示例</span><span class="sxs-lookup"><span data-stu-id="76290-128">Example</span></span>  

 <span data-ttu-id="76290-129">下面的示例使用 <xref:System.ServiceModel.Security.X509CertificateRecipientServiceCredential.SetCertificate%2A> 方法用 X.509 证书配置服务。</span><span class="sxs-lookup"><span data-stu-id="76290-129">The following example uses the <xref:System.ServiceModel.Security.X509CertificateRecipientServiceCredential.SetCertificate%2A> method to configure a service with an X.509 certificate.</span></span>  
  
 [!code-csharp[C_SecureWithCertificate#9](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_securewithcertificate/cs/source.cs#9)]
 [!code-vb[C_SecureWithCertificate#9](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/c_securewithcertificate/vb/source.vb#9)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="76290-130">编译代码</span><span class="sxs-lookup"><span data-stu-id="76290-130">Compiling the Code</span></span>  

 <span data-ttu-id="76290-131">编译该代码需要以下命名空间：</span><span class="sxs-lookup"><span data-stu-id="76290-131">The following namespaces are required to compile the code:</span></span>  
  
- <xref:System>  
  
- <xref:System.ServiceModel>  
  
- <xref:System.ServiceModel.Channels>  
  
- <xref:System.Web.Services.Description>  
  
- <xref:System.Security.Cryptography.X509Certificates>  
  
- <xref:System.Runtime.Serialization>  
  
## <a name="see-also"></a><span data-ttu-id="76290-132">请参阅</span><span class="sxs-lookup"><span data-stu-id="76290-132">See also</span></span>

- [<span data-ttu-id="76290-133">使用证书</span><span class="sxs-lookup"><span data-stu-id="76290-133">Working with Certificates</span></span>](working-with-certificates.md)
