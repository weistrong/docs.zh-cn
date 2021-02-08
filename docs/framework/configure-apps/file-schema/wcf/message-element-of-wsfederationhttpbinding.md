---
description: 详细了解： <message> 的元素 <wsFederationHttpBinding>
title: <message> 的元素 <wsFederationHttpBinding>
ms.date: 03/30/2017
ms.assetid: 9d710389-d9d8-4454-9bf2-da4ccda31cec
ms.openlocfilehash: 64978902081ec9e5a603804fed3b378da12fe42e
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99802185"
---
# <a name="message-element-of-wsfederationhttpbinding"></a><span data-ttu-id="1ed2f-103">\<message> 的元素 \<wsFederationHttpBinding></span><span class="sxs-lookup"><span data-stu-id="1ed2f-103">\<message> element of \<wsFederationHttpBinding></span></span>

<span data-ttu-id="1ed2f-104">定义的消息级安全性设置 [\<wsFederationHttpBinding>](wsfederationhttpbinding.md) 。</span><span class="sxs-lookup"><span data-stu-id="1ed2f-104">Defines the settings for the message-level security for the [\<wsFederationHttpBinding>](wsfederationhttpbinding.md).</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<bindings>**](bindings.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<wsFederationHttpBinding>**](wsfederationhttpbinding.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<binding>**\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<security>**](security-of-wsfederationhttpbinding.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<message>**  
  
## <a name="syntax"></a><span data-ttu-id="1ed2f-105">语法</span><span class="sxs-lookup"><span data-stu-id="1ed2f-105">Syntax</span></span>  
  
```xml  
<wsFederationBinding>
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
</wsFederationBinding>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="1ed2f-106">特性和元素</span><span class="sxs-lookup"><span data-stu-id="1ed2f-106">Attributes and Elements</span></span>  

 <span data-ttu-id="1ed2f-107">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="1ed2f-107">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="1ed2f-108">特性</span><span class="sxs-lookup"><span data-stu-id="1ed2f-108">Attributes</span></span>  
  
|<span data-ttu-id="1ed2f-109">属性</span><span class="sxs-lookup"><span data-stu-id="1ed2f-109">Attribute</span></span>|<span data-ttu-id="1ed2f-110">说明</span><span class="sxs-lookup"><span data-stu-id="1ed2f-110">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="1ed2f-111">algorithmSuite</span><span class="sxs-lookup"><span data-stu-id="1ed2f-111">algorithmSuite</span></span>|<span data-ttu-id="1ed2f-112">设置消息加密和密钥包装算法。</span><span class="sxs-lookup"><span data-stu-id="1ed2f-112">Sets the message encryption and key-wrap algorithms.</span></span> <span data-ttu-id="1ed2f-113">有关此属性的有效值，请参见“algorithmSuite 属性”表。</span><span class="sxs-lookup"><span data-stu-id="1ed2f-113">See the "algorithmSuite attribute" table for valid values of this attribute.</span></span> <span data-ttu-id="1ed2f-114">默认值是 `Basic256`。</span><span class="sxs-lookup"><span data-stu-id="1ed2f-114">The default value is `Basic256`.</span></span><br /><br /> <span data-ttu-id="1ed2f-115">此属性的类型为 <xref:System.ServiceModel.Security.SecurityAlgorithmSuite>。</span><span class="sxs-lookup"><span data-stu-id="1ed2f-115">This attribute is of type <xref:System.ServiceModel.Security.SecurityAlgorithmSuite>.</span></span> <span data-ttu-id="1ed2f-116">这些算法与“安全策略语言”(WS-SecurityPolicy) 规范中指定的算法一致。</span><span class="sxs-lookup"><span data-stu-id="1ed2f-116">These algorithms map to those specified in the Security Policy Language (WS-SecurityPolicy) specification.</span></span>|  
|<span data-ttu-id="1ed2f-117">issuedKeyType</span><span class="sxs-lookup"><span data-stu-id="1ed2f-117">issuedKeyType</span></span>|<span data-ttu-id="1ed2f-118">指定要颁发的密钥类型。</span><span class="sxs-lookup"><span data-stu-id="1ed2f-118">Specifies the type of key to be issued.</span></span> <span data-ttu-id="1ed2f-119">有效值包括以下值：</span><span class="sxs-lookup"><span data-stu-id="1ed2f-119">Valid values include the following:</span></span><br /><br /> <span data-ttu-id="1ed2f-120">-SymmetricKey</span><span class="sxs-lookup"><span data-stu-id="1ed2f-120">-   SymmetricKey</span></span><br /><span data-ttu-id="1ed2f-121">-PublicKey</span><span class="sxs-lookup"><span data-stu-id="1ed2f-121">-   PublicKey</span></span><br /><br /> <span data-ttu-id="1ed2f-122">默认值为 `SymmetricKey`。</span><span class="sxs-lookup"><span data-stu-id="1ed2f-122">The default is `SymmetricKey`.</span></span> <span data-ttu-id="1ed2f-123">此属性的类型为 <xref:System.IdentityModel.Tokens.SecurityKeyType>。</span><span class="sxs-lookup"><span data-stu-id="1ed2f-123">This attribute is of type <xref:System.IdentityModel.Tokens.SecurityKeyType>.</span></span>|  
|<span data-ttu-id="1ed2f-124">issuedTokenType</span><span class="sxs-lookup"><span data-stu-id="1ed2f-124">issuedTokenType</span></span>|<span data-ttu-id="1ed2f-125">一个字符串，它所包含的 URI 指定要颁发的令牌的类型。</span><span class="sxs-lookup"><span data-stu-id="1ed2f-125">A string that contains a URI that specifies the type of token to be issued.</span></span> <span data-ttu-id="1ed2f-126">默认值为 `null`。</span><span class="sxs-lookup"><span data-stu-id="1ed2f-126">The default is `null`.</span></span>|  
|<span data-ttu-id="1ed2f-127">negotiateServiceCredential</span><span class="sxs-lookup"><span data-stu-id="1ed2f-127">negotiateServiceCredential</span></span>|<span data-ttu-id="1ed2f-128">一个布尔值，指定是否应在协商过程中交换服务凭据，或者是否可在带外使用服务凭据。</span><span class="sxs-lookup"><span data-stu-id="1ed2f-128">A Boolean value that specifies whether the service credential should be exchanged as part of negotiation or is available out of band.</span></span> <span data-ttu-id="1ed2f-129">默认值为 `true`，这意味着对服务凭据进行协商。</span><span class="sxs-lookup"><span data-stu-id="1ed2f-129">The default is `true`, which means that the service credential is negotiated.</span></span>|  
  
## <a name="algorithmsuite-attribute"></a><span data-ttu-id="1ed2f-130">algorithmSuite 属性</span><span class="sxs-lookup"><span data-stu-id="1ed2f-130">algorithmSuite Attribute</span></span>  
  
|<span data-ttu-id="1ed2f-131">值</span><span class="sxs-lookup"><span data-stu-id="1ed2f-131">Value</span></span>|<span data-ttu-id="1ed2f-132">说明</span><span class="sxs-lookup"><span data-stu-id="1ed2f-132">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="1ed2f-133">Basic128</span><span class="sxs-lookup"><span data-stu-id="1ed2f-133">Basic128</span></span>|<span data-ttu-id="1ed2f-134">使用 Basic128 加密，对消息摘要使用 Sha1，对密钥包装使用 Rsa-oaep-mgf1p。</span><span class="sxs-lookup"><span data-stu-id="1ed2f-134">Use Basic128 encryption, Sha1 for message digest, and Rsa-oaep-mgf1p for key wrap.</span></span>|  
|<span data-ttu-id="1ed2f-135">Basic192</span><span class="sxs-lookup"><span data-stu-id="1ed2f-135">Basic192</span></span>|<span data-ttu-id="1ed2f-136">使用 Basic192 加密，对消息摘要使用 Sha1，对密钥包装使用 Rsa-oaep-mgf1p。</span><span class="sxs-lookup"><span data-stu-id="1ed2f-136">Use Basic192 encryption, Sha1 for message digest, Rsa-oaep-mgf1p for key wrap.</span></span>|  
|<span data-ttu-id="1ed2f-137">Basic256</span><span class="sxs-lookup"><span data-stu-id="1ed2f-137">Basic256</span></span>|<span data-ttu-id="1ed2f-138">使用 Basic256 加密，对消息摘要使用 Sha1，对密钥包装使用 Rsa-oaep-mgf1p。</span><span class="sxs-lookup"><span data-stu-id="1ed2f-138">Use Basic256 encryption, Sha1 for message digest, Rsa-oaep-mgf1p for key wrap.</span></span>|  
|<span data-ttu-id="1ed2f-139">Basic256Rsa15</span><span class="sxs-lookup"><span data-stu-id="1ed2f-139">Basic256Rsa15</span></span>|<span data-ttu-id="1ed2f-140">对消息加密使用 Basic256，对消息摘要使用 Sha1，对密钥包装使用 Rsa15。</span><span class="sxs-lookup"><span data-stu-id="1ed2f-140">Use Basic256 for message encryption, Sha1 for message digest and Rsa15 for key wrap.</span></span>|  
|<span data-ttu-id="1ed2f-141">Basic192Rsa15</span><span class="sxs-lookup"><span data-stu-id="1ed2f-141">Basic192Rsa15</span></span>|<span data-ttu-id="1ed2f-142">对消息加密使用 Basic192，对消息摘要使用 Sha1，对密钥包装使用 Rsa15。</span><span class="sxs-lookup"><span data-stu-id="1ed2f-142">Use Basic192 for message encryption, Sha1 for message digest and Rsa15 for key wrap.</span></span>|  
|<span data-ttu-id="1ed2f-143">TripleDes</span><span class="sxs-lookup"><span data-stu-id="1ed2f-143">TripleDes</span></span>|<span data-ttu-id="1ed2f-144">使用 TripleDes 加密，对消息摘要使用 Sha1，对密钥包装使用 Rsa-oaep-mgf1p。</span><span class="sxs-lookup"><span data-stu-id="1ed2f-144">Use TripleDes encryption, Sha1 for message digest, Rsa-oaep-mgf1p for key wrap.</span></span>|  
|<span data-ttu-id="1ed2f-145">Basic128Rsa15</span><span class="sxs-lookup"><span data-stu-id="1ed2f-145">Basic128Rsa15</span></span>|<span data-ttu-id="1ed2f-146">对消息加密使用 Basic128，对消息摘要使用 Sha1，对密钥包装使用 Rsa15。</span><span class="sxs-lookup"><span data-stu-id="1ed2f-146">Use Basic128 for message encryption, Sha1 for message digest and Rsa15 for key wrap.</span></span>|  
|<span data-ttu-id="1ed2f-147">TripleDesRsa15</span><span class="sxs-lookup"><span data-stu-id="1ed2f-147">TripleDesRsa15</span></span>|<span data-ttu-id="1ed2f-148">使用 TripleDes 加密，对消息摘要使用 Sha1，对密钥包装使用 Rsa15。</span><span class="sxs-lookup"><span data-stu-id="1ed2f-148">Use TripleDes encryption, Sha1 for message digest and Rsa15 for key wrap.</span></span>|  
|<span data-ttu-id="1ed2f-149">Basic128Sha256</span><span class="sxs-lookup"><span data-stu-id="1ed2f-149">Basic128Sha256</span></span>|<span data-ttu-id="1ed2f-150">对消息加密使用 Basic128，对消息摘要使用 Sha256，对密钥包装使用 Rsa-oaep-mgf1p。</span><span class="sxs-lookup"><span data-stu-id="1ed2f-150">Use Basic128 for message encryption, Sha256 for message digest and Rsa-oaep-mgf1p for key wrap.</span></span>|  
|<span data-ttu-id="1ed2f-151">Basic192Sha256</span><span class="sxs-lookup"><span data-stu-id="1ed2f-151">Basic192Sha256</span></span>|<span data-ttu-id="1ed2f-152">对消息加密使用 Basic192，对消息摘要使用 Sha256，对密钥包装使用 Rsa-oaep-mgf1p。</span><span class="sxs-lookup"><span data-stu-id="1ed2f-152">Use Basic192 for message encryption, Sha256 for message digest and Rsa-oaep-mgf1p for key wrap.</span></span>|  
|<span data-ttu-id="1ed2f-153">Basic256Sha256</span><span class="sxs-lookup"><span data-stu-id="1ed2f-153">Basic256Sha256</span></span>|<span data-ttu-id="1ed2f-154">对消息加密使用 Basic256，对消息摘要使用 Sha256，对密钥包装使用 Rsa-oaep-mgf1p。</span><span class="sxs-lookup"><span data-stu-id="1ed2f-154">Use Basic256 for message encryption, Sha256 for message digest and Rsa-oaep-mgf1p for key wrap.</span></span>|  
|<span data-ttu-id="1ed2f-155">TripleDesSha256</span><span class="sxs-lookup"><span data-stu-id="1ed2f-155">TripleDesSha256</span></span>|<span data-ttu-id="1ed2f-156">对消息加密使用 TripleDes，对消息摘要使用 Sha256，对密钥包装使用 Rsa-oaep-mgf1p。</span><span class="sxs-lookup"><span data-stu-id="1ed2f-156">Use TripleDes for message encryption, Sha256 for message digest and Rsa-oaep-mgf1p for key wrap.</span></span>|  
|<span data-ttu-id="1ed2f-157">Basic128Sha256Rsa15</span><span class="sxs-lookup"><span data-stu-id="1ed2f-157">Basic128Sha256Rsa15</span></span>|<span data-ttu-id="1ed2f-158">对消息加密使用 Basic128，对消息摘要使用 Sha256，对密钥包装使用 Rsa15。</span><span class="sxs-lookup"><span data-stu-id="1ed2f-158">Use Basic128 for message encryption, Sha256 for message digest and Rsa15 for key wrap.</span></span>|  
|<span data-ttu-id="1ed2f-159">Basic192Sha256Rsa15</span><span class="sxs-lookup"><span data-stu-id="1ed2f-159">Basic192Sha256Rsa15</span></span>|<span data-ttu-id="1ed2f-160">对消息加密使用 Aes192，对消息摘要使用 Sha256，对密钥包装使用 Rsa15。</span><span class="sxs-lookup"><span data-stu-id="1ed2f-160">Use Aes192 for message encryption, Sha256 for message digest and Rsa15 for key wrap.</span></span>|  
|<span data-ttu-id="1ed2f-161">Basic256Sha256Rsa15</span><span class="sxs-lookup"><span data-stu-id="1ed2f-161">Basic256Sha256Rsa15</span></span>|<span data-ttu-id="1ed2f-162">对消息加密使用 Basic256，对消息摘要使用 Sha256，对密钥包装使用 Rsa15。</span><span class="sxs-lookup"><span data-stu-id="1ed2f-162">Use Basic256 for message encryption, Sha256 for message digest and Rsa15 for key wrap.</span></span>|  
|<span data-ttu-id="1ed2f-163">TripleDesSha256Rsa15</span><span class="sxs-lookup"><span data-stu-id="1ed2f-163">TripleDesSha256Rsa15</span></span>|<span data-ttu-id="1ed2f-164">对消息加密使用 TripleDes，对消息摘要使用 Sha256，对密钥包装使用 Rsa15。</span><span class="sxs-lookup"><span data-stu-id="1ed2f-164">Use TripleDes for message encryption, Sha256 for message digest and Rsa15 for key wrap.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="1ed2f-165">子元素</span><span class="sxs-lookup"><span data-stu-id="1ed2f-165">Child Elements</span></span>  
  
|<span data-ttu-id="1ed2f-166">元素</span><span class="sxs-lookup"><span data-stu-id="1ed2f-166">Element</span></span>|<span data-ttu-id="1ed2f-167">说明</span><span class="sxs-lookup"><span data-stu-id="1ed2f-167">Description</span></span>|  
|-------------|-----------------|  
|[\<claimTypeRequirements>](claimtyperequirements-element.md)|<span data-ttu-id="1ed2f-168">指定此绑定的声明类型集合。</span><span class="sxs-lookup"><span data-stu-id="1ed2f-168">Specifies a collection of claim types for this binding.</span></span> <span data-ttu-id="1ed2f-169">每个元素的类型都为 <xref:System.ServiceModel.Configuration.ClaimTypeElement>。</span><span class="sxs-lookup"><span data-stu-id="1ed2f-169">Each element is of type <xref:System.ServiceModel.Configuration.ClaimTypeElement>.</span></span>|  
|<span data-ttu-id="1ed2f-170">颁发者</span><span class="sxs-lookup"><span data-stu-id="1ed2f-170">issuer</span></span>|<span data-ttu-id="1ed2f-171">指定颁发安全令牌的终结点。</span><span class="sxs-lookup"><span data-stu-id="1ed2f-171">Specifies an endpoint that issues a security token.</span></span> <span data-ttu-id="1ed2f-172">此元素的类型为 <xref:System.ServiceModel.Configuration.IssuedTokenParametersEndpointAddressElement>。</span><span class="sxs-lookup"><span data-stu-id="1ed2f-172">This element is of type <xref:System.ServiceModel.Configuration.IssuedTokenParametersEndpointAddressElement>.</span></span>|  
|<span data-ttu-id="1ed2f-173">issuerMetadata</span><span class="sxs-lookup"><span data-stu-id="1ed2f-173">issuerMetadata</span></span>|<span data-ttu-id="1ed2f-174">指定颁发者的终结点地址。</span><span class="sxs-lookup"><span data-stu-id="1ed2f-174">Specifies the endpoint address of the issuer.</span></span>|  
|[\<tokenRequestParameters>](tokenrequestparameters.md)|<span data-ttu-id="1ed2f-175">令牌请求参数的集合。</span><span class="sxs-lookup"><span data-stu-id="1ed2f-175">A collection of token request parameters.</span></span> <span data-ttu-id="1ed2f-176">每个参数都是一个 XML 元素。</span><span class="sxs-lookup"><span data-stu-id="1ed2f-176">Each parameter is an XML element.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="1ed2f-177">父元素</span><span class="sxs-lookup"><span data-stu-id="1ed2f-177">Parent Elements</span></span>  
  
|<span data-ttu-id="1ed2f-178">元素</span><span class="sxs-lookup"><span data-stu-id="1ed2f-178">Element</span></span>|<span data-ttu-id="1ed2f-179">说明</span><span class="sxs-lookup"><span data-stu-id="1ed2f-179">Description</span></span>|  
|-------------|-----------------|  
|[\<security>](security-of-wsfederationhttpbinding.md)|<span data-ttu-id="1ed2f-180">定义绑定的安全设置。</span><span class="sxs-lookup"><span data-stu-id="1ed2f-180">Defines the security settings for a binding.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="1ed2f-181">请参阅</span><span class="sxs-lookup"><span data-stu-id="1ed2f-181">See also</span></span>

- <xref:System.ServiceModel.FederatedMessageSecurityOverHttp>
- <xref:System.ServiceModel.Configuration.WSFederationHttpSecurityElement.Message%2A>
- <xref:System.ServiceModel.WSFederationHttpSecurity.Message%2A>
- <xref:System.ServiceModel.Configuration.FederatedMessageSecurityOverHttpElement>
- [<span data-ttu-id="1ed2f-182">保护服务和客户端的安全</span><span class="sxs-lookup"><span data-stu-id="1ed2f-182">Securing Services and Clients</span></span>](../../../wcf/feature-details/securing-services-and-clients.md)
- [<span data-ttu-id="1ed2f-183">绑定</span><span class="sxs-lookup"><span data-stu-id="1ed2f-183">Bindings</span></span>](../../../wcf/bindings.md)
- [<span data-ttu-id="1ed2f-184">配置系统提供的绑定</span><span class="sxs-lookup"><span data-stu-id="1ed2f-184">Configuring System-Provided Bindings</span></span>](../../../wcf/feature-details/configuring-system-provided-bindings.md)
- [<span data-ttu-id="1ed2f-185">使用绑定配置服务和客户端</span><span class="sxs-lookup"><span data-stu-id="1ed2f-185">Using Bindings to Configure Services and Clients</span></span>](../../../wcf/using-bindings-to-configure-services-and-clients.md)
- [\<binding>](bindings.md)
