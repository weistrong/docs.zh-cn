---
description: 了解详细信息：具有相互证书的消息安全
title: 使用相互证书的消息安全
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 99d7a528-7ae4-4d39-a0f9-3066ea237de0
ms.openlocfilehash: c894f457dcd0fdc449c2f94eaee15004300df5fa
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99726983"
---
# <a name="message-security-with-mutual-certificates"></a><span data-ttu-id="82083-103">使用相互证书的消息安全</span><span class="sxs-lookup"><span data-stu-id="82083-103">Message Security with Mutual Certificates</span></span>

<span data-ttu-id="82083-104">下面的方案演示使用消息安全模式 Windows Communication Foundation (WCF) 服务和客户端。</span><span class="sxs-lookup"><span data-stu-id="82083-104">The following scenario shows a Windows Communication Foundation (WCF) service and client secured using message security mode.</span></span> <span data-ttu-id="82083-105">使用证书对客户端和服务进行身份验证。</span><span class="sxs-lookup"><span data-stu-id="82083-105">The client and the service are authenticated with certificates.</span></span>  
  
 <span data-ttu-id="82083-106">本方案是可互操作的，因为它使用具有 X.509 证书令牌配置文件的 WS-Security。</span><span class="sxs-lookup"><span data-stu-id="82083-106">This scenario is interoperable because it uses WS-Security with the X.509 certificate token profile.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="82083-107">本方案不对服务证书执行协商。</span><span class="sxs-lookup"><span data-stu-id="82083-107">This scenario does not perform negotiation of the service certificate.</span></span> <span data-ttu-id="82083-108">在进行任何通信之前，必须先向客户端提供服务证书。</span><span class="sxs-lookup"><span data-stu-id="82083-108">The service certificate must be provided to the client in advance of any communication.</span></span> <span data-ttu-id="82083-109">服务器证书可以随应用程序一起分发，也可以通过带外通信来提供。</span><span class="sxs-lookup"><span data-stu-id="82083-109">The server certificate can be distributed with the application or provided in an out-of-band communication.</span></span>  
  
 <span data-ttu-id="82083-110">![具有相互证书的消息安全](media/f4157312-b17c-416c-a5ee-fa7b54db211b.gif "f4157312-b17c-416c-a5ee-fa7b54db211b")</span><span class="sxs-lookup"><span data-stu-id="82083-110">![Message security with mutual certificates](media/f4157312-b17c-416c-a5ee-fa7b54db211b.gif "f4157312-b17c-416c-a5ee-fa7b54db211b")</span></span>  
  
|<span data-ttu-id="82083-111">特征</span><span class="sxs-lookup"><span data-stu-id="82083-111">Characteristic</span></span>|<span data-ttu-id="82083-112">说明</span><span class="sxs-lookup"><span data-stu-id="82083-112">Description</span></span>|  
|--------------------|-----------------|  
|<span data-ttu-id="82083-113">安全模式</span><span class="sxs-lookup"><span data-stu-id="82083-113">Security Mode</span></span>|<span data-ttu-id="82083-114">消息</span><span class="sxs-lookup"><span data-stu-id="82083-114">Message</span></span>|  
|<span data-ttu-id="82083-115">互操作性</span><span class="sxs-lookup"><span data-stu-id="82083-115">Interoperability</span></span>|<span data-ttu-id="82083-116">是，使用 WS-Security 和 X.509 证书令牌配置文件兼容的客户端和服务。</span><span class="sxs-lookup"><span data-stu-id="82083-116">Yes, with WS-Security and X.509 certificate token profile compatible clients and services.</span></span>|  
|<span data-ttu-id="82083-117">身份验证</span><span class="sxs-lookup"><span data-stu-id="82083-117">Authentication</span></span>|<span data-ttu-id="82083-118">服务器和客户端的相互身份验证。</span><span class="sxs-lookup"><span data-stu-id="82083-118">Mutual authentication of the server and client.</span></span>|  
|<span data-ttu-id="82083-119">完整性</span><span class="sxs-lookup"><span data-stu-id="82083-119">Integrity</span></span>|<span data-ttu-id="82083-120">是</span><span class="sxs-lookup"><span data-stu-id="82083-120">Yes</span></span>|  
|<span data-ttu-id="82083-121">机密性</span><span class="sxs-lookup"><span data-stu-id="82083-121">Confidentiality</span></span>|<span data-ttu-id="82083-122">是</span><span class="sxs-lookup"><span data-stu-id="82083-122">Yes</span></span>|  
|<span data-ttu-id="82083-123">Transport</span><span class="sxs-lookup"><span data-stu-id="82083-123">Transport</span></span>|<span data-ttu-id="82083-124">HTTP</span><span class="sxs-lookup"><span data-stu-id="82083-124">HTTP</span></span>|  
|<span data-ttu-id="82083-125">绑定</span><span class="sxs-lookup"><span data-stu-id="82083-125">Binding</span></span>|<xref:System.ServiceModel.WSHttpBinding>|  
  
## <a name="service"></a><span data-ttu-id="82083-126">服务</span><span class="sxs-lookup"><span data-stu-id="82083-126">Service</span></span>  

 <span data-ttu-id="82083-127">下面的代码和配置应独立运行。</span><span class="sxs-lookup"><span data-stu-id="82083-127">The following code and configuration are meant to run independently.</span></span> <span data-ttu-id="82083-128">执行下列操作之一：</span><span class="sxs-lookup"><span data-stu-id="82083-128">Do one of the following:</span></span>  
  
- <span data-ttu-id="82083-129">使用代码（而不使用配置）创建独立服务。</span><span class="sxs-lookup"><span data-stu-id="82083-129">Create a stand-alone service using the code with no configuration.</span></span>  
  
- <span data-ttu-id="82083-130">使用提供的配置创建服务，但不定义任何终结点。</span><span class="sxs-lookup"><span data-stu-id="82083-130">Create a service using the supplied configuration, but do not define any endpoints.</span></span>  
  
### <a name="code"></a><span data-ttu-id="82083-131">代码</span><span class="sxs-lookup"><span data-stu-id="82083-131">Code</span></span>  

 <span data-ttu-id="82083-132">下面的代码演示如何创建使用消息安全的服务终结点。</span><span class="sxs-lookup"><span data-stu-id="82083-132">The following code shows creates a service endpoint that uses message security.</span></span> <span data-ttu-id="82083-133">服务请求一个证书来使自己通过身份验证。</span><span class="sxs-lookup"><span data-stu-id="82083-133">The service requires a certificate to authenticate itself.</span></span>  
  
 [!code-csharp[C_SecurityScenarios#13](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_securityscenarios/cs/source.cs#13)]
 [!code-vb[C_SecurityScenarios#13](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/c_securityscenarios/vb/source.vb#13)]  
  
### <a name="configuration"></a><span data-ttu-id="82083-134">Configuration</span><span class="sxs-lookup"><span data-stu-id="82083-134">Configuration</span></span>  

 <span data-ttu-id="82083-135">可以使用下面的配置，而不使用代码来创建同样的服务。</span><span class="sxs-lookup"><span data-stu-id="82083-135">The following configuration can be used instead of the code to create the same service.</span></span>  
  
```xml  
<?xml version="1.0" encoding="utf-8"?>  
<configuration>  
  <system.serviceModel>  
    <behaviors>  
      <serviceBehaviors>  
        <behavior name="serviceCredentialBehavior">  
          <serviceCredentials>  
            <serviceCertificate findValue="Contoso.com"
                                storeLocation="LocalMachine"  
                                storeName="My"
                                x509FindType="FindBySubjectName" />  
          </serviceCredentials>  
        </behavior>  
      </serviceBehaviors>  
    </behaviors>  
    <services>  
      <service behaviorConfiguration="serviceCredentialBehavior"
               name="ServiceModel.Calculator">  
        <endpoint address="http://localhost/Calculator"
                  binding="wsHttpBinding"  
                  bindingConfiguration="InteropCertificateBinding"  
                  name="WSHttpBinding_ICalculator"  
                  contract="ServiceModel.ICalculator" />  
      </service>  
    </services>  
    <bindings>  
      <wsHttpBinding>  
        <binding name="InteropCertificateBinding">  
          <security mode="Message">  
            <message clientCredentialType="Certificate"  
                     negotiateServiceCredential="false"  
                     establishSecurityContext="false" />  
          </security>  
        </binding>  
      </wsHttpBinding>  
    </bindings>  
    <client />  
  </system.serviceModel>  
</configuration>  
```  
  
## <a name="client"></a><span data-ttu-id="82083-136">客户端</span><span class="sxs-lookup"><span data-stu-id="82083-136">Client</span></span>  

 <span data-ttu-id="82083-137">下面的代码和配置应独立运行。</span><span class="sxs-lookup"><span data-stu-id="82083-137">The following code and configuration are meant to run independently.</span></span> <span data-ttu-id="82083-138">执行下列操作之一：</span><span class="sxs-lookup"><span data-stu-id="82083-138">Do one of the following:</span></span>  
  
- <span data-ttu-id="82083-139">使用代码（和客户端代码）创建独立客户端。</span><span class="sxs-lookup"><span data-stu-id="82083-139">Create a stand-alone client using the code (and client code).</span></span>  
  
- <span data-ttu-id="82083-140">创建不定义任何终结点地址的客户端。</span><span class="sxs-lookup"><span data-stu-id="82083-140">Create a client that does not define any endpoint addresses.</span></span> <span data-ttu-id="82083-141">而使用将配置名称作为自变量的客户端构造函数。</span><span class="sxs-lookup"><span data-stu-id="82083-141">Instead, use the client constructor that takes the configuration name as an argument.</span></span> <span data-ttu-id="82083-142">例如：</span><span class="sxs-lookup"><span data-stu-id="82083-142">For example:</span></span>  
  
     [!code-csharp[C_SecurityScenarios#0](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_securityscenarios/cs/source.cs#0)]
     [!code-vb[C_SecurityScenarios#0](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/c_securityscenarios/vb/source.vb#0)]  
  
### <a name="code"></a><span data-ttu-id="82083-143">代码</span><span class="sxs-lookup"><span data-stu-id="82083-143">Code</span></span>  

 <span data-ttu-id="82083-144">下面的代码创建客户端。</span><span class="sxs-lookup"><span data-stu-id="82083-144">The following code creates the client.</span></span> <span data-ttu-id="82083-145">安全模式设置为“消息”，客户端凭据类型设置为“证书”。</span><span class="sxs-lookup"><span data-stu-id="82083-145">The security mode is set to Message, and the client credential type is set to Certificate.</span></span>  
  
 [!code-csharp[C_SecurityScenarios#20](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_securityscenarios/cs/source.cs#20)]
 [!code-vb[C_SecurityScenarios#20](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/c_securityscenarios/vb/source.vb#20)]  
  
### <a name="configuration"></a><span data-ttu-id="82083-146">Configuration</span><span class="sxs-lookup"><span data-stu-id="82083-146">Configuration</span></span>  

 <span data-ttu-id="82083-147">下面配置客户端。</span><span class="sxs-lookup"><span data-stu-id="82083-147">The following configures the client.</span></span> <span data-ttu-id="82083-148">必须使用指定客户端证书 [\<clientCertificate>](../../configure-apps/file-schema/wcf/clientcertificate-of-clientcredentials-element.md) 。</span><span class="sxs-lookup"><span data-stu-id="82083-148">A client certificate must be specified using the [\<clientCertificate>](../../configure-apps/file-schema/wcf/clientcertificate-of-clientcredentials-element.md).</span></span> <span data-ttu-id="82083-149">此外，还使用指定服务证书 [\<defaultCertificate>](../../configure-apps/file-schema/wcf/defaultcertificate-element.md) 。</span><span class="sxs-lookup"><span data-stu-id="82083-149">Also, the service certificate is specified using the [\<defaultCertificate>](../../configure-apps/file-schema/wcf/defaultcertificate-element.md).</span></span>  
  
```xml  
<?xml version="1.0" encoding="utf-8"?>  
<configuration>  
  <system.serviceModel>  
    <behaviors>  
      <endpointBehaviors>  
        <behavior name="ClientCredentialsBehavior">  
          <clientCredentials>  
            <clientCertificate findValue="Cohowinery.com"
                 storeLocation="CurrentUser"  
                 storeName="My"  
                 x509FindType="FindBySubjectName" />  
            <serviceCertificate>  
              <defaultCertificate findValue="Contoso.com"
                                  storeLocation="CurrentUser"  
                                  storeName="TrustedPeople"  
                                  x509FindType="FindBySubjectName" />  
            </serviceCertificate>  
          </clientCredentials>  
        </behavior>  
      </endpointBehaviors>  
    </behaviors>  
    <bindings>  
      <wsHttpBinding>  
        <binding name="WSHttpBinding_ICalculator" >  
          <security mode="Message">  
            <message clientCredentialType="Certificate"
                     negotiateServiceCredential="false"  
                     establishSecurityContext="false" />  
          </security>  
        </binding>  
      </wsHttpBinding>  
    </bindings>  
    <client>  
      <endpoint address="http://machineName/Calculator"
                behaviorConfiguration="ClientCredentialsBehavior"  
                binding="wsHttpBinding"
                bindingConfiguration="WSHttpBinding_ICalculator"  
                contract="ICalculator"  
                name="WSHttpBinding_ICalculator">  
        <identity>  
          <certificate encodedValue="Encoded_Value_Not_Shown" />  
        </identity>  
      </endpoint>  
    </client>  
  </system.serviceModel>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="82083-150">请参阅</span><span class="sxs-lookup"><span data-stu-id="82083-150">See also</span></span>

- [<span data-ttu-id="82083-151">安全性概述</span><span class="sxs-lookup"><span data-stu-id="82083-151">Security Overview</span></span>](security-overview.md)
- <span data-ttu-id="82083-152">[Windows Server App Fabric 的安全模型](/previous-versions/appfabric/ee677202(v=azure.10))</span><span class="sxs-lookup"><span data-stu-id="82083-152">[Security Model for Windows Server App Fabric](/previous-versions/appfabric/ee677202(v=azure.10))</span></span>
- <span data-ttu-id="82083-153">[如何：在 WCF 中创建和安装用于传输安全的临时证书](/previous-versions/msp-n-p/ff648498(v=pandp.10))</span><span class="sxs-lookup"><span data-stu-id="82083-153">[How to: Create and Install Temporary Certificates in WCF for Transport Security During Development](/previous-versions/msp-n-p/ff648498(v=pandp.10))</span></span>
