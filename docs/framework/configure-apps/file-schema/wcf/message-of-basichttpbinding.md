---
description: 了解详细 <message> 信息： <basicHttpBinding>
title: <message> 的 <basicHttpBinding>
ms.date: 03/30/2017
ms.assetid: 51cdd329-6461-471a-8747-56c2299b61e5
ms.openlocfilehash: 738d782aaac06366eec324b091cbda815a3ff98f
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99802146"
---
# <a name="message-of-basichttpbinding"></a><span data-ttu-id="fde81-103">\<message> 的 \<basicHttpBinding></span><span class="sxs-lookup"><span data-stu-id="fde81-103">\<message> of \<basicHttpBinding></span></span>

<span data-ttu-id="fde81-104">定义的消息级安全性设置 [\<basicHttpBinding>](basichttpbinding.md) 。</span><span class="sxs-lookup"><span data-stu-id="fde81-104">Defines the settings for message-level security of the [\<basicHttpBinding>](basichttpbinding.md).</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<bindings>**](bindings.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<basicHttpBinding>**](basichttpbinding.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<binding>**\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<security>**](security-of-basichttpbinding.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<message>**  
  
## <a name="syntax"></a><span data-ttu-id="fde81-105">语法</span><span class="sxs-lookup"><span data-stu-id="fde81-105">Syntax</span></span>  
  
```xml  
<message algorithmSuite="Basic128/Basic192/Basic256/Basic128Rsa15/Basic256Rsa15/TripleDes/TripleDesRsa15/Basic128Sha256/Basic192Sha256/TripleDesSha256/Basic128Sha256Rsa15/Basic192Sha256Rsa15/Basic256Sha256Rsa15/TripleDesSha256Rsa15"
         clientCredentialType="UserName/Certificate" />
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="fde81-106">特性和元素</span><span class="sxs-lookup"><span data-stu-id="fde81-106">Attributes and Elements</span></span>  

 <span data-ttu-id="fde81-107">以下几节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="fde81-107">The following sections describe attributes, child elements, and parent elements</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="fde81-108">特性</span><span class="sxs-lookup"><span data-stu-id="fde81-108">Attributes</span></span>  
  
|<span data-ttu-id="fde81-109">属性</span><span class="sxs-lookup"><span data-stu-id="fde81-109">Attribute</span></span>|<span data-ttu-id="fde81-110">说明</span><span class="sxs-lookup"><span data-stu-id="fde81-110">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="fde81-111">algorithmSuite</span><span class="sxs-lookup"><span data-stu-id="fde81-111">algorithmSuite</span></span>|<span data-ttu-id="fde81-112">设置消息加密和密钥包装算法。</span><span class="sxs-lookup"><span data-stu-id="fde81-112">Sets the message encryption and key-wrap algorithms.</span></span> <span data-ttu-id="fde81-113">此属性类型为 <xref:System.ServiceModel.Security.SecurityAlgorithmSuite>，用于指定算法和密钥大小。</span><span class="sxs-lookup"><span data-stu-id="fde81-113">This attribute is of type <xref:System.ServiceModel.Security.SecurityAlgorithmSuite>, which specifies the algorithms and the key sizes.</span></span> <span data-ttu-id="fde81-114">这些算法与“安全策略语言”(WS-SecurityPolicy) 规范中指定的算法一致。</span><span class="sxs-lookup"><span data-stu-id="fde81-114">These algorithms map to those specified in the Security Policy Language (WS-SecurityPolicy) specification.</span></span><br /><br /> <span data-ttu-id="fde81-115">默认值是 `Basic256`。</span><span class="sxs-lookup"><span data-stu-id="fde81-115">The default value is `Basic256`.</span></span>|  
|<span data-ttu-id="fde81-116">clientCredentialType</span><span class="sxs-lookup"><span data-stu-id="fde81-116">clientCredentialType</span></span>|<span data-ttu-id="fde81-117">指定要在使用基于消息的安全性执行客户端身份验证时使用的凭据类型。</span><span class="sxs-lookup"><span data-stu-id="fde81-117">Specifies the type of credential to be used when performing client authentication using message-based security.</span></span> <span data-ttu-id="fde81-118">默认值为 `UserName`。</span><span class="sxs-lookup"><span data-stu-id="fde81-118">The default is `UserName`.</span></span>|  
  
## <a name="clientcredentialtype-attribute"></a><span data-ttu-id="fde81-119">clientCredentialType 属性</span><span class="sxs-lookup"><span data-stu-id="fde81-119">clientCredentialType Attribute</span></span>  
  
|<span data-ttu-id="fde81-120">值</span><span class="sxs-lookup"><span data-stu-id="fde81-120">Value</span></span>|<span data-ttu-id="fde81-121">描述</span><span class="sxs-lookup"><span data-stu-id="fde81-121">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="fde81-122">UserName</span><span class="sxs-lookup"><span data-stu-id="fde81-122">UserName</span></span>|<span data-ttu-id="fde81-123">-要求使用用户名凭据对客户端进行身份验证。</span><span class="sxs-lookup"><span data-stu-id="fde81-123">-   Requires the client be authenticated to the server with a UserName credential.</span></span> <span data-ttu-id="fde81-124">需要使用来指定此凭据 [\<clientCredentials>](clientcredentials.md) 。</span><span class="sxs-lookup"><span data-stu-id="fde81-124">This credential needs to be specified using the [\<clientCredentials>](clientcredentials.md).</span></span><br /><span data-ttu-id="fde81-125">-WCF 不支持发送密码摘要，也不支持使用密码派生密钥并使用此类密钥来实现消息安全性。</span><span class="sxs-lookup"><span data-stu-id="fde81-125">-   WCF does not support sending a password digest or deriving keys using passwords and using such keys for message security.</span></span> <span data-ttu-id="fde81-126">因此，WCF 强制在使用用户名凭据时确保传输安全。</span><span class="sxs-lookup"><span data-stu-id="fde81-126">Therefore, WCF enforces that the transport be secured when using UserName credentials.</span></span> <span data-ttu-id="fde81-127">对于 `basicHttpBinding`，这要求设置一个 SSL 通道。</span><span class="sxs-lookup"><span data-stu-id="fde81-127">For the `basicHttpBinding`, this requires setting up an SSL channel.</span></span>|  
|<span data-ttu-id="fde81-128">证书</span><span class="sxs-lookup"><span data-stu-id="fde81-128">Certificate</span></span>|<span data-ttu-id="fde81-129">要求使用证书向服务器对客户端进行身份验证。</span><span class="sxs-lookup"><span data-stu-id="fde81-129">Requires that the client be authenticated to the server using a certificate.</span></span> <span data-ttu-id="fde81-130">在此情况下，需要使用和来指定客户端凭据 [\<clientCredentials>](clientcredentials.md) [\<clientCertificate>](clientcertificate-of-servicecredentials.md) 。</span><span class="sxs-lookup"><span data-stu-id="fde81-130">The client credential in this case needs to be specified using [\<clientCredentials>](clientcredentials.md) and the [\<clientCertificate>](clientcertificate-of-servicecredentials.md).</span></span> <span data-ttu-id="fde81-131">此外，在使用消息安全模式时，需要向客户端提供服务证书。</span><span class="sxs-lookup"><span data-stu-id="fde81-131">In addition, when using message security mode, the client needs to be provisioned with the service certificate.</span></span> <span data-ttu-id="fde81-132">在这种情况下，需要使用 <xref:System.ServiceModel.Description.ClientCredentials> 类或 `ClientCredentials` 行为元素并使用指定服务证书来指定服务凭据 [\<serviceCertificate>](servicecertificate-of-servicecredentials.md) 。</span><span class="sxs-lookup"><span data-stu-id="fde81-132">The service credential in this case needs to be specified using <xref:System.ServiceModel.Description.ClientCredentials> class or `ClientCredentials` behavior element and specifying the service certificate using the [\<serviceCertificate>](servicecertificate-of-servicecredentials.md).</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="fde81-133">子元素</span><span class="sxs-lookup"><span data-stu-id="fde81-133">Child Elements</span></span>  

 <span data-ttu-id="fde81-134">无</span><span class="sxs-lookup"><span data-stu-id="fde81-134">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="fde81-135">父元素</span><span class="sxs-lookup"><span data-stu-id="fde81-135">Parent Elements</span></span>  
  
|<span data-ttu-id="fde81-136">元素</span><span class="sxs-lookup"><span data-stu-id="fde81-136">Element</span></span>|<span data-ttu-id="fde81-137">说明</span><span class="sxs-lookup"><span data-stu-id="fde81-137">Description</span></span>|  
|-------------|-----------------|  
|[\<security>](security-of-basichttpbinding.md)|<span data-ttu-id="fde81-138">定义的安全功能 [\<basicHttpBinding>](basichttpbinding.md) 。</span><span class="sxs-lookup"><span data-stu-id="fde81-138">Defines the security capabilities for the [\<basicHttpBinding>](basichttpbinding.md).</span></span>|  
  
## <a name="example"></a><span data-ttu-id="fde81-139">示例</span><span class="sxs-lookup"><span data-stu-id="fde81-139">Example</span></span>  

 <span data-ttu-id="fde81-140">此示例演示如何实现使用 basicHttpBinding 和消息安全性的应用程序。</span><span class="sxs-lookup"><span data-stu-id="fde81-140">This sample demonstrates how to implement an application that uses the basicHttpBinding and message security.</span></span> <span data-ttu-id="fde81-141">在下面的服务配置示例中，终结点定义将指定 basicHttpBinding 并引用名为 `Binding1` 的绑定配置。</span><span class="sxs-lookup"><span data-stu-id="fde81-141">In the following configuration example for a service, the endpoint definition specifies the basicHttpBinding and references a binding configuration named `Binding1`.</span></span> <span data-ttu-id="fde81-142">服务用于向客户端验证自己身份的证书是在配置文件的 `behaviors` 节中 `serviceCredentials` 元素的下面设置的。</span><span class="sxs-lookup"><span data-stu-id="fde81-142">The certificate that the service uses to authenticate itself to the client is set in the `behaviors` section of the configuration file under the `serviceCredentials` element.</span></span> <span data-ttu-id="fde81-143">应用于证书（客户端使用该证书向服务验证自己的身份）的验证模式也是在 `behaviors` 节中 `clientCertificate` 元素的下面设置的。</span><span class="sxs-lookup"><span data-stu-id="fde81-143">The validation mode that applies to the certificate that the client uses to authenticate itself to the service is also set in the `behaviors` section under the `clientCertificate` element.</span></span>  
  
 <span data-ttu-id="fde81-144">在客户端配置文件中指定同样的绑定和安全详细信息。</span><span class="sxs-lookup"><span data-stu-id="fde81-144">The same binding and security details are specified in the client configuration file.</span></span>  
  
```xml  
<system.serviceModel>
  <services>
    <service name="Microsoft.ServiceModel.Samples.CalculatorService"
             behaviorConfiguration="CalculatorServiceBehavior">
      <host>
        <baseAddresses>
          <add baseAddress="http://localhost:8000/ServiceModelSamples/service" />
        </baseAddresses>
      </host>
      <!-- this endpoint is exposed at the base address provided by host: http://localhost:8000/ServiceModelSamples/service -->
      <endpoint address=""
                binding="basicHttpBinding"
                bindingConfiguration="Binding1"
                contract="Microsoft.ServiceModel.Samples.ICalculator" />
      <!-- the mex endpoint is exposed at http://localhost:8000/ServiceModelSamples/service/mex -->
      <endpoint address="mex"
                binding="mexHttpBinding"
                contract="IMetadataExchange" />
    </service>
  </services>
  <bindings>
    <basicHttpBinding>
    <!-- This configuration defines the SecurityMode as Message and
         the clientCredentialType as Certificate. -->
      <binding name="Binding1">
        <security mode = "Message">
          <message clientCredentialType="Certificate" />
        </security>
      </binding>
    </basicHttpBinding>
  </bindings>
  <!--For debugging purposes set the includeExceptionDetailInFaults attribute to true-->
  <behaviors>
    <serviceBehaviors>
      <behavior name="CalculatorServiceBehavior">
        <serviceMetadata httpGetEnabled="True" />
        <serviceDebug includeExceptionDetailInFaults="False" />
        <!-- The serviceCredentials behavior allows one to define a service certificate.
             A service certificate is used by a client to authenticate the service and provide message protection.
             This configuration references the "localhost" certificate installed during the setup instructions. -->
        <serviceCredentials>
          <serviceCertificate findValue="localhost"
                              storeLocation="LocalMachine"
                              storeName="My"
                              x509FindType="FindBySubjectName" />
          <clientCertificate>
            <!-- Setting the certificateValidationMode to PeerOrChainTrust means that if the certificate
               is in the user's Trusted People store, then it will be trusted without performing a
               validation of the certificate's issuer chain. This setting is used here for convenience so that the
               sample can be run without having to have certificates issued by a certification authority (CA).
               This setting is less secure than the default, ChainTrust. The security implications of this
               setting should be carefully considered before using PeerOrChainTrust in production code. -->
            <authentication certificateValidationMode="PeerOrChainTrust" />
          </clientCertificate>
        </serviceCredentials>
      </behavior>
    </serviceBehaviors>
  </behaviors>
</system.serviceModel>
```  
  
## <a name="see-also"></a><span data-ttu-id="fde81-145">请参阅</span><span class="sxs-lookup"><span data-stu-id="fde81-145">See also</span></span>

- <xref:System.ServiceModel.BasicHttpMessageSecurity>
- <xref:System.ServiceModel.Configuration.BasicHttpSecurityElement.Message%2A>
- <xref:System.ServiceModel.BasicHttpSecurity.Message%2A>
- <xref:System.ServiceModel.Configuration.BasicHttpMessageSecurityElement>
- [<span data-ttu-id="fde81-146">保护服务和客户端的安全</span><span class="sxs-lookup"><span data-stu-id="fde81-146">Securing Services and Clients</span></span>](../../../wcf/feature-details/securing-services-and-clients.md)
- [<span data-ttu-id="fde81-147">绑定</span><span class="sxs-lookup"><span data-stu-id="fde81-147">Bindings</span></span>](../../../wcf/bindings.md)
- [<span data-ttu-id="fde81-148">配置系统提供的绑定</span><span class="sxs-lookup"><span data-stu-id="fde81-148">Configuring System-Provided Bindings</span></span>](../../../wcf/feature-details/configuring-system-provided-bindings.md)
- [<span data-ttu-id="fde81-149">使用绑定配置服务和客户端</span><span class="sxs-lookup"><span data-stu-id="fde81-149">Using Bindings to Configure Services and Clients</span></span>](../../../wcf/using-bindings-to-configure-services-and-clients.md)
- [\<binding>](bindings.md)
