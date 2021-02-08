---
description: 了解详细 <security> 信息： <wsFederationHttpBinding>
title: <security> 的 <wsFederationHttpBinding>
ms.date: 03/30/2017
ms.assetid: a8e5e854-b8dc-4921-843d-34b6a4a6a8ba
ms.openlocfilehash: 6c01c7a50b05f1723b3620407eb5e5761bae35cb
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99786793"
---
# <a name="security-of-wsfederationhttpbinding"></a><span data-ttu-id="5816f-103">\<security> 的 \<wsFederationHttpBinding></span><span class="sxs-lookup"><span data-stu-id="5816f-103">\<security> of \<wsFederationHttpBinding></span></span>

<span data-ttu-id="5816f-104">定义的安全设置 [\<wsFederationHttpBinding>](wsfederationhttpbinding.md) 。</span><span class="sxs-lookup"><span data-stu-id="5816f-104">Defines the security settings of the [\<wsFederationHttpBinding>](wsfederationhttpbinding.md).</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<bindings>**](bindings.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<wsFederationHttpBinding>**](wsfederationhttpbinding.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<binding>**\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<security>**  
  
## <a name="syntax"></a><span data-ttu-id="5816f-105">语法</span><span class="sxs-lookup"><span data-stu-id="5816f-105">Syntax</span></span>  
  
```xml  
<wsFederationBinding>
  <binding>
    <security mode="None/Message/TransportWithMessageCredential">
      <message algorithmSuite="Basic128/Basic192/Basic256/Basic128Rsa15/Basic256Rsa15/TripleDes/TripleDesRsa15/Basic128Sha256/Basic192Sha256/TripleDesSha256/Basic128Sha256Rsa15/Basic192Sha256Rsa15/Basic256Sha256Rsa15/TripleDesSha256Rsa15"
               issuedTokenType="string"
               issuedKeyType="SymmetricKey/PublicKey"
               negotiateServiceCredential="Boolean">
        <claimTypeRequirements>
          <add claimType="URI"
               isOptional="Boolean" />
        </claimTypeRequirements>
        <issuer address="Uri" >
          <headers>
            <add name="String"
                 namespace="String" />
          </headers>
          <identity>
            <certificate encodedValue="String" />
            <certificateReference findValue="String"
                                  isChainIncluded="Boolean"
                                  storeName="AddressBook/AuthRoot/CertificateAuthority/Disallowed/My/Root/TrustedPeople/TrustedPublisher"
                                  storeLocation="LocalMachine/CurrentUser"
                                  X509FindType="System.Security.Cryptography.X509certificates.X509findtype" />
            <dns value="String" />
            <rsa value="String" />
            <servicePrincipalName value="String" />
            <usePrincipalName value="String" />
          </identity>
        </issuer>
        <issuerMetadata address="String">
          <headers>
            <add name="String"
                 namespace="String" />
          </headers>
          <identity>
            <certificate encodedValue="String" />
            <certificateReference findValue="String"
                                  isChainIncluded="Boolean"
                                  storeName="AddressBook/AuthRoot/CertificateAuthority/Disallowed/My/Root/TrustedPeople/TrustedPublisher"
                                  storeLocation="LocalMachine/CurrentUser"
                                  X509FindType="System.Security.Cryptography.X509certificates.X509findtype" />
            <dns value="String" />
            <rsa value="String" />
            <servicePrincipalName value="String" />
            <usePrincipalName value="String" />
          </identity>
        </issuerMetadata>
        <tokenRequestParameters>
          <xmlElement>
          </xmlElement>
        </tokenRequestParameters>
      </message>
    </security>
  </binding>
</wsFederationBinding>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="5816f-106">特性和元素</span><span class="sxs-lookup"><span data-stu-id="5816f-106">Attributes and Elements</span></span>  

 <span data-ttu-id="5816f-107">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="5816f-107">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="5816f-108">特性</span><span class="sxs-lookup"><span data-stu-id="5816f-108">Attributes</span></span>  
  
|<span data-ttu-id="5816f-109">属性</span><span class="sxs-lookup"><span data-stu-id="5816f-109">Attribute</span></span>|<span data-ttu-id="5816f-110">说明</span><span class="sxs-lookup"><span data-stu-id="5816f-110">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="5816f-111">“模式”</span><span class="sxs-lookup"><span data-stu-id="5816f-111">Mode</span></span>|<span data-ttu-id="5816f-112">可选。</span><span class="sxs-lookup"><span data-stu-id="5816f-112">Optional.</span></span> <span data-ttu-id="5816f-113">指定所应用的安全类型。</span><span class="sxs-lookup"><span data-stu-id="5816f-113">Specifies the type of security that is applied.</span></span> <span data-ttu-id="5816f-114">默认值是 `Message`。</span><span class="sxs-lookup"><span data-stu-id="5816f-114">The default value is `Message`.</span></span> <span data-ttu-id="5816f-115">此属性的类型为 <xref:System.ServiceModel.WSFederationHttpSecurityMode>。</span><span class="sxs-lookup"><span data-stu-id="5816f-115">This attribute is of type <xref:System.ServiceModel.WSFederationHttpSecurityMode>.</span></span>|  
  
## <a name="mode-attribute"></a><span data-ttu-id="5816f-116">Mode 属性</span><span class="sxs-lookup"><span data-stu-id="5816f-116">Mode Attribute</span></span>  
  
|<span data-ttu-id="5816f-117">值</span><span class="sxs-lookup"><span data-stu-id="5816f-117">Value</span></span>|<span data-ttu-id="5816f-118">说明</span><span class="sxs-lookup"><span data-stu-id="5816f-118">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="5816f-119">无</span><span class="sxs-lookup"><span data-stu-id="5816f-119">None</span></span>|<span data-ttu-id="5816f-120">SOAP 消息在传输过程中并不安全。</span><span class="sxs-lookup"><span data-stu-id="5816f-120">The SOAP message is not secure during transfer.</span></span>|  
|<span data-ttu-id="5816f-121">消息</span><span class="sxs-lookup"><span data-stu-id="5816f-121">Message</span></span>|<span data-ttu-id="5816f-122">通过使用 SOAP 消息安全，可以提供完整性、保密性、服务器身份验证和客户端身份验证。</span><span class="sxs-lookup"><span data-stu-id="5816f-122">Integrity, confidentiality, server authentication and client authentication are provided using SOAP message security.</span></span> <span data-ttu-id="5816f-123">默认情况下，将对正文进行加密和签名。</span><span class="sxs-lookup"><span data-stu-id="5816f-123">By default, the body is encrypted and signed.</span></span> <span data-ttu-id="5816f-124">此服务需要使用证书进行配置。</span><span class="sxs-lookup"><span data-stu-id="5816f-124">The service needs to be configured with a certificate.</span></span> <span data-ttu-id="5816f-125">客户端根据由安全令牌服务颁发给客户端的令牌进行身份验证</span><span class="sxs-lookup"><span data-stu-id="5816f-125">Client authentication is based on the token issued to the client by a security token service</span></span>|  
|<span data-ttu-id="5816f-126">TransportWithMessageCredential</span><span class="sxs-lookup"><span data-stu-id="5816f-126">TransportWithMessageCredential</span></span>|<span data-ttu-id="5816f-127">完整性、保密性和服务器身份验证均由 HTTPS 提供。</span><span class="sxs-lookup"><span data-stu-id="5816f-127">Integrity, confidentiality and server authentication are provided by HTTPS.</span></span> <span data-ttu-id="5816f-128">此服务需要使用证书进行配置。</span><span class="sxs-lookup"><span data-stu-id="5816f-128">The service needs to be configured with a certificate.</span></span> <span data-ttu-id="5816f-129">客户端身份验证采用 SOAP 消息安全方式提供，并根据由安全令牌服务颁发给客户端的令牌进行。</span><span class="sxs-lookup"><span data-stu-id="5816f-129">Client authentication is provided by means of SOAP message security and is based on the token issued to the client by a security token service.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="5816f-130">子元素</span><span class="sxs-lookup"><span data-stu-id="5816f-130">Child Elements</span></span>  
  
|<span data-ttu-id="5816f-131">元素</span><span class="sxs-lookup"><span data-stu-id="5816f-131">Element</span></span>|<span data-ttu-id="5816f-132">说明</span><span class="sxs-lookup"><span data-stu-id="5816f-132">Description</span></span>|  
|-------------|-----------------|  
|[\<message>](message-element-of-wsfederationhttpbinding.md)|<span data-ttu-id="5816f-133">定义消息级安全性设置。</span><span class="sxs-lookup"><span data-stu-id="5816f-133">Defines the settings for the message-level security.</span></span> <span data-ttu-id="5816f-134">此元素的类型为 <xref:System.ServiceModel.Configuration.FederatedMessageSecurityOverHttpElement>。</span><span class="sxs-lookup"><span data-stu-id="5816f-134">This element is of type <xref:System.ServiceModel.Configuration.FederatedMessageSecurityOverHttpElement>.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="5816f-135">父元素</span><span class="sxs-lookup"><span data-stu-id="5816f-135">Parent Elements</span></span>  
  
|<span data-ttu-id="5816f-136">元素</span><span class="sxs-lookup"><span data-stu-id="5816f-136">Element</span></span>|<span data-ttu-id="5816f-137">说明</span><span class="sxs-lookup"><span data-stu-id="5816f-137">Description</span></span>|  
|-------------|-----------------|  
|[\<binding>](bindings.md)|<span data-ttu-id="5816f-138">定义的所有绑定功能 [\<wsDualHttpBinding>](wsdualhttpbinding.md) 。</span><span class="sxs-lookup"><span data-stu-id="5816f-138">Defines all binding capabilities of the [\<wsDualHttpBinding>](wsdualhttpbinding.md).</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="5816f-139">请参阅</span><span class="sxs-lookup"><span data-stu-id="5816f-139">See also</span></span>

- <xref:System.ServiceModel.WSFederationHttpSecurity>
- <xref:System.ServiceModel.WSFederationHttpBinding.Security%2A>
- <xref:System.ServiceModel.Configuration.WSFederationHttpBindingElement.Security%2A>
- <xref:System.ServiceModel.Configuration.WSFederationHttpSecurityElement>
- [<span data-ttu-id="5816f-140">如何：创建 WSFederationHttpBinding</span><span class="sxs-lookup"><span data-stu-id="5816f-140">How to: Create a WSFederationHttpBinding</span></span>](../../../wcf/feature-details/how-to-create-a-wsfederationhttpbinding.md)
- [<span data-ttu-id="5816f-141">保护服务和客户端的安全</span><span class="sxs-lookup"><span data-stu-id="5816f-141">Securing Services and Clients</span></span>](../../../wcf/feature-details/securing-services-and-clients.md)
- [<span data-ttu-id="5816f-142">选择凭据类型</span><span class="sxs-lookup"><span data-stu-id="5816f-142">Selecting a Credential Type</span></span>](../../../wcf/feature-details/selecting-a-credential-type.md)
- [<span data-ttu-id="5816f-143">绑定</span><span class="sxs-lookup"><span data-stu-id="5816f-143">Bindings</span></span>](../../../wcf/bindings.md)
- [<span data-ttu-id="5816f-144">配置系统提供的绑定</span><span class="sxs-lookup"><span data-stu-id="5816f-144">Configuring System-Provided Bindings</span></span>](../../../wcf/feature-details/configuring-system-provided-bindings.md)
- [<span data-ttu-id="5816f-145">使用绑定配置服务和客户端</span><span class="sxs-lookup"><span data-stu-id="5816f-145">Using Bindings to Configure Services and Clients</span></span>](../../../wcf/using-bindings-to-configure-services-and-clients.md)
- [\<binding>](bindings.md)
