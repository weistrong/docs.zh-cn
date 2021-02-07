---
description: 详细了解： <message> 的元素 <ws2007FederationHttpBinding>
title: <message> 的元素 <ws2007FederationHttpBinding>
ms.date: 03/30/2017
ms.assetid: 52cd941d-e230-4c82-8b29-333a7d20eca8
ms.openlocfilehash: f9116a5075f30421dfb26adc29ec0b167db33673
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99725448"
---
# <a name="message-element-of-ws2007federationhttpbinding"></a><span data-ttu-id="8d118-103">\<message> 的元素 \<ws2007FederationHttpBinding></span><span class="sxs-lookup"><span data-stu-id="8d118-103">\<message> element of \<ws2007FederationHttpBinding></span></span>

<span data-ttu-id="8d118-104">定义元素的消息级安全性设置 [\<ws2007FederationHttpBinding>](ws2007federationhttpbinding.md) 。</span><span class="sxs-lookup"><span data-stu-id="8d118-104">Defines settings for the message-level security for the [\<ws2007FederationHttpBinding>](ws2007federationhttpbinding.md) element.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<bindings>**](bindings.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<ws2007FederationHttpBinding>**](ws2007federationhttpbinding.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<binding>**\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<security>**](security-element-of-ws2007federationhttpbinding.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<message>**  
  
## <a name="syntax"></a><span data-ttu-id="8d118-105">语法</span><span class="sxs-lookup"><span data-stu-id="8d118-105">Syntax</span></span>  
  
```xml  
<ws2007FederationBinding>
  <binding>
    <security>
      <message algorithmSuite="Basic128/Basic192/Basic256/Basic128Rsa15/Basic256Rsa15/TripleDes/TripleDesRsa15/Basic128Sha256/Basic192Sha256/TripleDesSha256/Basic128Sha256Rsa15/Basic192Sha256Rsa15/Basic256Sha256Rsa15/TripleDesSha256Rsa15"
               issuedTokenType="string"
               issuedKeyType="SymmetricKey/PublicKey"
               negotiateServiceCredential="Boolean">
        <claimTypeRequirements>
          <add claimType="URI"
               isOptional="Boolean" />
        </claimTypeRequirements>
        <issuer address="Uri">
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
                                  x509FindType="System.Security.Cryptography.X509certificates.X509findtype" />
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
</ws2007FederationBinding>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="8d118-106">特性和元素</span><span class="sxs-lookup"><span data-stu-id="8d118-106">Attributes and Elements</span></span>  

 <span data-ttu-id="8d118-107">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="8d118-107">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="8d118-108">特性</span><span class="sxs-lookup"><span data-stu-id="8d118-108">Attributes</span></span>  
  
|<span data-ttu-id="8d118-109">属性</span><span class="sxs-lookup"><span data-stu-id="8d118-109">Attribute</span></span>|<span data-ttu-id="8d118-110">说明</span><span class="sxs-lookup"><span data-stu-id="8d118-110">Description</span></span>|  
|---------------|-----------------|  
|`algorithmSuite`|<span data-ttu-id="8d118-111">可选。</span><span class="sxs-lookup"><span data-stu-id="8d118-111">Optional.</span></span> <span data-ttu-id="8d118-112">设置消息加密、签名和密钥包装算法。</span><span class="sxs-lookup"><span data-stu-id="8d118-112">Sets the message encryption, signature, and key-wrap algorithms.</span></span> <span data-ttu-id="8d118-113">算法和密钥大小由 <xref:System.ServiceModel.Security.SecurityAlgorithmSuite> 类确定。</span><span class="sxs-lookup"><span data-stu-id="8d118-113">The algorithms and the key sizes are determined by the <xref:System.ServiceModel.Security.SecurityAlgorithmSuite> class.</span></span> <span data-ttu-id="8d118-114">这些算法与“安全策略语言”(WS-SecurityPolicy) 规范中指定的算法一致。</span><span class="sxs-lookup"><span data-stu-id="8d118-114">These algorithms map to those specified in the Security Policy Language (WS-SecurityPolicy) specification.</span></span><br /><br /> <span data-ttu-id="8d118-115">有关可能的值，请参见下表。</span><span class="sxs-lookup"><span data-stu-id="8d118-115">See the following table for possible values.</span></span> <span data-ttu-id="8d118-116">默认值为 Basic256。</span><span class="sxs-lookup"><span data-stu-id="8d118-116">The default value is Basic256.</span></span>|  
|`issuedKeyType`|<span data-ttu-id="8d118-117">指定要颁发的密钥类型。</span><span class="sxs-lookup"><span data-stu-id="8d118-117">Specifies the type of key to be issued.</span></span> <span data-ttu-id="8d118-118">有效值包括以下值：</span><span class="sxs-lookup"><span data-stu-id="8d118-118">Valid values include the following:</span></span><br /><br /> <span data-ttu-id="8d118-119">-SymmetricKey</span><span class="sxs-lookup"><span data-stu-id="8d118-119">-   SymmetricKey</span></span><br /><span data-ttu-id="8d118-120">-PublicKey</span><span class="sxs-lookup"><span data-stu-id="8d118-120">-   PublicKey</span></span><br /><span data-ttu-id="8d118-121">-为 bearerkey 并且</span><span class="sxs-lookup"><span data-stu-id="8d118-121">-   BearerKey</span></span><br /><br /> <span data-ttu-id="8d118-122">默认值为 SymmetricKey。</span><span class="sxs-lookup"><span data-stu-id="8d118-122">The default is SymmetricKey.</span></span> <span data-ttu-id="8d118-123">此属性的类型为 <xref:System.IdentityModel.Tokens.SecurityKeyType>。</span><span class="sxs-lookup"><span data-stu-id="8d118-123">This attribute is of type <xref:System.IdentityModel.Tokens.SecurityKeyType>.</span></span>|  
|`issuedTokenType`|<span data-ttu-id="8d118-124">一个 URI，指定要颁发的令牌的类型。</span><span class="sxs-lookup"><span data-stu-id="8d118-124">A URI that specifies the type of token to be issued.</span></span> <span data-ttu-id="8d118-125">默认值为 `null`。</span><span class="sxs-lookup"><span data-stu-id="8d118-125">The default is `null`.</span></span>|  
|`negotiateServiceCredential`|<span data-ttu-id="8d118-126">一个值，指定是否应在协商过程中交换服务凭据，或者是否可在带外使用服务凭据。</span><span class="sxs-lookup"><span data-stu-id="8d118-126">A value that specifies whether the service credential should be exchanged as part of negotiation or is available out of band.</span></span> <span data-ttu-id="8d118-127">默认值为 `true`，这意味着对服务凭据进行协商。</span><span class="sxs-lookup"><span data-stu-id="8d118-127">The default is `true`, which means that the service credential is negotiated.</span></span>|  
  
## <a name="algorithmsuite-attribute"></a><span data-ttu-id="8d118-128">algorithmSuite 属性</span><span class="sxs-lookup"><span data-stu-id="8d118-128">algorithmSuite Attribute</span></span>  
  
|<span data-ttu-id="8d118-129">值</span><span class="sxs-lookup"><span data-stu-id="8d118-129">Value</span></span>|<span data-ttu-id="8d118-130">说明</span><span class="sxs-lookup"><span data-stu-id="8d118-130">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="8d118-131">Basic128</span><span class="sxs-lookup"><span data-stu-id="8d118-131">Basic128</span></span>|<span data-ttu-id="8d118-132">使用 Aes128 加密，对消息摘要使用 Sha1，对密钥包装使用 Rsa-oaep-mgf1p。</span><span class="sxs-lookup"><span data-stu-id="8d118-132">Use Aes128 encryption, Sha1 for message digest, and Rsa-oaep-mgf1p for key wrap.</span></span>|  
|<span data-ttu-id="8d118-133">Basic192</span><span class="sxs-lookup"><span data-stu-id="8d118-133">Basic192</span></span>|<span data-ttu-id="8d118-134">使用 Aes192 加密，对消息摘要使用 Sha1，对密钥包装使用 Rsa-oaep-mgf1p。</span><span class="sxs-lookup"><span data-stu-id="8d118-134">Use Aes192 encryption, Sha1 for message digest, Rsa-oaep-mgf1p for key wrap.</span></span>|  
|<span data-ttu-id="8d118-135">Basic256</span><span class="sxs-lookup"><span data-stu-id="8d118-135">Basic256</span></span>|<span data-ttu-id="8d118-136">使用 Aes256 加密，对消息摘要使用 Sha1，对密钥包装使用 Rsa-oaep-mgf1p。</span><span class="sxs-lookup"><span data-stu-id="8d118-136">Use Aes256 encryption, Sha1 for message digest, Rsa-oaep-mgf1p for key wrap.</span></span>|  
|<span data-ttu-id="8d118-137">Basic256Rsa15</span><span class="sxs-lookup"><span data-stu-id="8d118-137">Basic256Rsa15</span></span>|<span data-ttu-id="8d118-138">对消息加密使用 Aes256，对消息摘要使用 Sha1，对密钥包装使用 Rsa15。</span><span class="sxs-lookup"><span data-stu-id="8d118-138">Use Aes256 for message encryption, Sha1 for message digest and Rsa15 for key wrap.</span></span>|  
|<span data-ttu-id="8d118-139">Basic192Rsa15</span><span class="sxs-lookup"><span data-stu-id="8d118-139">Basic192Rsa15</span></span>|<span data-ttu-id="8d118-140">对消息加密使用 Aes192，对消息摘要使用 Sha1，对密钥包装使用 Rsa15。</span><span class="sxs-lookup"><span data-stu-id="8d118-140">Use Aes192 for message encryption, Sha1 for message digest and Rsa15 for key wrap.</span></span>|  
|<span data-ttu-id="8d118-141">TripleDes</span><span class="sxs-lookup"><span data-stu-id="8d118-141">TripleDes</span></span>|<span data-ttu-id="8d118-142">使用 TripleDes 加密，对消息摘要使用 Sha1，对密钥包装使用 Rsa-oaep-mgf1p。</span><span class="sxs-lookup"><span data-stu-id="8d118-142">Use TripleDes encryption, Sha1 for message digest, Rsa-oaep-mgf1p for key wrap.</span></span>|  
|<span data-ttu-id="8d118-143">Basic128Rsa15</span><span class="sxs-lookup"><span data-stu-id="8d118-143">Basic128Rsa15</span></span>|<span data-ttu-id="8d118-144">对消息加密使用 Aes128，对消息摘要使用 Sha1，对密钥包装使用 Rsa15。</span><span class="sxs-lookup"><span data-stu-id="8d118-144">Use Aes128 for message encryption, Sha1 for message digest and Rsa15 for key wrap.</span></span>|  
|<span data-ttu-id="8d118-145">TripleDesRsa15</span><span class="sxs-lookup"><span data-stu-id="8d118-145">TripleDesRsa15</span></span>|<span data-ttu-id="8d118-146">使用 TripleDes 加密，对消息摘要使用 Sha1，对密钥包装使用 Rsa15。</span><span class="sxs-lookup"><span data-stu-id="8d118-146">Use TripleDes encryption, Sha1 for message digest and Rsa15 for key wrap.</span></span>|  
|<span data-ttu-id="8d118-147">Basic128Sha256</span><span class="sxs-lookup"><span data-stu-id="8d118-147">Basic128Sha256</span></span>|<span data-ttu-id="8d118-148">对消息加密使用 Aes256，对消息摘要使用 Sha256，对密钥包装使用 Rsa-oaep-mgf1p。</span><span class="sxs-lookup"><span data-stu-id="8d118-148">Use Aes256 for message encryption, Sha256 for message digest and Rsa-oaep-mgf1p for key wrap.</span></span>|  
|<span data-ttu-id="8d118-149">Basic192Sha256</span><span class="sxs-lookup"><span data-stu-id="8d118-149">Basic192Sha256</span></span>|<span data-ttu-id="8d118-150">对消息加密使用 Aes192，对消息摘要使用 Sha256，对密钥包装使用 Rsa-oaep-mgf1p。</span><span class="sxs-lookup"><span data-stu-id="8d118-150">Use Aes192 for message encryption, Sha256 for message digest and Rsa-oaep-mgf1p for key wrap.</span></span>|  
|<span data-ttu-id="8d118-151">Basic256Sha256</span><span class="sxs-lookup"><span data-stu-id="8d118-151">Basic256Sha256</span></span>|<span data-ttu-id="8d118-152">对消息加密使用 Aes256，对消息摘要使用 Sha256，对密钥包装使用 Rsa-oaep-mgf1p。</span><span class="sxs-lookup"><span data-stu-id="8d118-152">Use Aes256 for message encryption, Sha256 for message digest and Rsa-oaep-mgf1p for key wrap.</span></span>|  
|<span data-ttu-id="8d118-153">TripleDesSha256</span><span class="sxs-lookup"><span data-stu-id="8d118-153">TripleDesSha256</span></span>|<span data-ttu-id="8d118-154">对消息加密使用 TripleDes，对消息摘要使用 Sha256，对密钥包装使用 Rsa-oaep-mgf1p。</span><span class="sxs-lookup"><span data-stu-id="8d118-154">Use TripleDes for message encryption, Sha256 for message digest and Rsa-oaep-mgf1p for key wrap.</span></span>|  
|<span data-ttu-id="8d118-155">Basic128Sha256Rsa15</span><span class="sxs-lookup"><span data-stu-id="8d118-155">Basic128Sha256Rsa15</span></span>|<span data-ttu-id="8d118-156">对消息加密使用 Aes128，对消息摘要使用 Sha256，对密钥包装使用 Rsa15。</span><span class="sxs-lookup"><span data-stu-id="8d118-156">Use Aes128 for message encryption, Sha256 for message digest and Rsa15 for key wrap.</span></span>|  
|<span data-ttu-id="8d118-157">Basic192Sha256Rsa15</span><span class="sxs-lookup"><span data-stu-id="8d118-157">Basic192Sha256Rsa15</span></span>|<span data-ttu-id="8d118-158">对消息加密使用 Aes192，对消息摘要使用 Sha256，对密钥包装使用 Rsa15。</span><span class="sxs-lookup"><span data-stu-id="8d118-158">Use Aes192 for message encryption, Sha256 for message digest and Rsa15 for key wrap.</span></span>|  
|<span data-ttu-id="8d118-159">Basic256Sha256Rsa15</span><span class="sxs-lookup"><span data-stu-id="8d118-159">Basic256Sha256Rsa15</span></span>|<span data-ttu-id="8d118-160">对消息加密使用 Aes256，对消息摘要使用 Sha256，对密钥包装使用 Rsa15。</span><span class="sxs-lookup"><span data-stu-id="8d118-160">Use Aes256 for message encryption, Sha256 for message digest and Rsa15 for key wrap.</span></span>|  
|<span data-ttu-id="8d118-161">TripleDesSha256Rsa15</span><span class="sxs-lookup"><span data-stu-id="8d118-161">TripleDesSha256Rsa15</span></span>|<span data-ttu-id="8d118-162">对消息加密使用 TripleDes，对消息摘要使用 Sha256，对密钥包装使用 Rsa15。</span><span class="sxs-lookup"><span data-stu-id="8d118-162">Use TripleDes for message encryption, Sha256 for message digest and Rsa15 for key wrap.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="8d118-163">子元素</span><span class="sxs-lookup"><span data-stu-id="8d118-163">Child Elements</span></span>  
  
|<span data-ttu-id="8d118-164">元素</span><span class="sxs-lookup"><span data-stu-id="8d118-164">Element</span></span>|<span data-ttu-id="8d118-165">说明</span><span class="sxs-lookup"><span data-stu-id="8d118-165">Description</span></span>|  
|-------------|-----------------|  
|[\<claimTypeRequirements>](claimtyperequirements-element.md)|<span data-ttu-id="8d118-166">指定此绑定的声明类型集合。</span><span class="sxs-lookup"><span data-stu-id="8d118-166">Specifies a collection of claim types for this binding.</span></span> <span data-ttu-id="8d118-167">每个元素的类型都为 <xref:System.ServiceModel.Configuration.ClaimTypeElement>。</span><span class="sxs-lookup"><span data-stu-id="8d118-167">Each element is of type <xref:System.ServiceModel.Configuration.ClaimTypeElement>.</span></span>|  
|[\<issuer>](issuer.md)|<span data-ttu-id="8d118-168">指定颁发安全令牌的终结点。</span><span class="sxs-lookup"><span data-stu-id="8d118-168">Specifies an endpoint that issues a security token.</span></span> <span data-ttu-id="8d118-169">此元素的类型为 <xref:System.ServiceModel.Configuration.IssuedTokenParametersEndpointAddressElement>。</span><span class="sxs-lookup"><span data-stu-id="8d118-169">This element is of type <xref:System.ServiceModel.Configuration.IssuedTokenParametersEndpointAddressElement>.</span></span>|  
|[\<issuerMetadata>](issuermetadata.md)|<span data-ttu-id="8d118-170">指定颁发者的终结点地址。</span><span class="sxs-lookup"><span data-stu-id="8d118-170">Specifies the endpoint address of the issuer.</span></span>|  
|[\<tokenRequestParameters>](tokenrequestparameters.md)|<span data-ttu-id="8d118-171">令牌请求参数的集合。</span><span class="sxs-lookup"><span data-stu-id="8d118-171">A collection of token request parameters.</span></span> <span data-ttu-id="8d118-172">每个参数都是一个 XML 元素。</span><span class="sxs-lookup"><span data-stu-id="8d118-172">Each parameter is an XML element.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="8d118-173">父元素</span><span class="sxs-lookup"><span data-stu-id="8d118-173">Parent Elements</span></span>  
  
|<span data-ttu-id="8d118-174">元素</span><span class="sxs-lookup"><span data-stu-id="8d118-174">Element</span></span>|<span data-ttu-id="8d118-175">说明</span><span class="sxs-lookup"><span data-stu-id="8d118-175">Description</span></span>|  
|-------------|-----------------|  
|[\<security>](security-element-of-ws2007federationhttpbinding.md)|<span data-ttu-id="8d118-176">定义绑定的安全设置。</span><span class="sxs-lookup"><span data-stu-id="8d118-176">Defines the security settings for a binding.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="8d118-177">请参阅</span><span class="sxs-lookup"><span data-stu-id="8d118-177">See also</span></span>

- <xref:System.ServiceModel.FederatedMessageSecurityOverHttp>
- <xref:System.ServiceModel.Configuration.WSFederationHttpSecurityElement.Message%2A>
- <xref:System.ServiceModel.WSFederationHttpSecurity.Message%2A>
- <xref:System.ServiceModel.Configuration.FederatedMessageSecurityOverHttpElement>
- [<span data-ttu-id="8d118-178">保护服务和客户端的安全</span><span class="sxs-lookup"><span data-stu-id="8d118-178">Securing Services and Clients</span></span>](../../../wcf/feature-details/securing-services-and-clients.md)
- [<span data-ttu-id="8d118-179">绑定</span><span class="sxs-lookup"><span data-stu-id="8d118-179">Bindings</span></span>](../../../wcf/bindings.md)
- [<span data-ttu-id="8d118-180">配置系统提供的绑定</span><span class="sxs-lookup"><span data-stu-id="8d118-180">Configuring System-Provided Bindings</span></span>](../../../wcf/feature-details/configuring-system-provided-bindings.md)
- [<span data-ttu-id="8d118-181">使用绑定配置服务和客户端</span><span class="sxs-lookup"><span data-stu-id="8d118-181">Using Bindings to Configure Services and Clients</span></span>](../../../wcf/using-bindings-to-configure-services-and-clients.md)
- [\<binding>](bindings.md)
