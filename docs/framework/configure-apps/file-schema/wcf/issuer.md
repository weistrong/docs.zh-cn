---
description: 了解详细信息： <issuer>
title: <issuer>
ms.date: 03/30/2017
ms.assetid: 8c49c6ae-fa1a-4179-a84b-613c3216dcde
ms.openlocfilehash: 771fb8d0bee4e78b598bd20c4d99ec5180f9fb1c
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99725631"
---
# \<issuer>

<span data-ttu-id="b9650-102">指定颁发安全令牌的安全令牌服务 (STS)。</span><span class="sxs-lookup"><span data-stu-id="b9650-102">Specifies the Security Token Service (STS) that issues security tokens.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<bindings>**](bindings.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<wsFederationHttpBinding>**](wsfederationhttpbinding.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<binding>**\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<security>**](security-of-wsfederationhttpbinding.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<message>**](message-element-of-wsfederationhttpbinding.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<issuer>**  
  
## <a name="syntax"></a><span data-ttu-id="b9650-103">语法</span><span class="sxs-lookup"><span data-stu-id="b9650-103">Syntax</span></span>  
  
```xml  
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
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="b9650-104">特性和元素</span><span class="sxs-lookup"><span data-stu-id="b9650-104">Attributes and Elements</span></span>  

 <span data-ttu-id="b9650-105">以下几节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="b9650-105">The following sections describe attributes, child elements, and parent elements</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="b9650-106">特性</span><span class="sxs-lookup"><span data-stu-id="b9650-106">Attributes</span></span>  
  
|<span data-ttu-id="b9650-107">属性</span><span class="sxs-lookup"><span data-stu-id="b9650-107">Attribute</span></span>|<span data-ttu-id="b9650-108">说明</span><span class="sxs-lookup"><span data-stu-id="b9650-108">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="b9650-109">address</span><span class="sxs-lookup"><span data-stu-id="b9650-109">address</span></span>|<span data-ttu-id="b9650-110">必选字符串。</span><span class="sxs-lookup"><span data-stu-id="b9650-110">Required string.</span></span> <span data-ttu-id="b9650-111">STS 的 URL。</span><span class="sxs-lookup"><span data-stu-id="b9650-111">The URL of the STS.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="b9650-112">子元素</span><span class="sxs-lookup"><span data-stu-id="b9650-112">Child Elements</span></span>  
  
|<span data-ttu-id="b9650-113">元素</span><span class="sxs-lookup"><span data-stu-id="b9650-113">Element</span></span>|<span data-ttu-id="b9650-114">说明</span><span class="sxs-lookup"><span data-stu-id="b9650-114">Description</span></span>|  
|-------------|-----------------|  
|[\<headers>](headers-element.md)|<span data-ttu-id="b9650-115">生成器可以创建的终结点的地址标头的集合。</span><span class="sxs-lookup"><span data-stu-id="b9650-115">A collection of address headers for the endpoints that the builder can create.</span></span>|  
|[\<identity>](identity.md)|<span data-ttu-id="b9650-116">在使用颁发的令牌时，指定能够使客户端对服务器进行身份验证的设置。</span><span class="sxs-lookup"><span data-stu-id="b9650-116">When using an issued token, specifies settings that enable the client to authenticate the server.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="b9650-117">父元素</span><span class="sxs-lookup"><span data-stu-id="b9650-117">Parent Elements</span></span>  
  
|<span data-ttu-id="b9650-118">元素</span><span class="sxs-lookup"><span data-stu-id="b9650-118">Element</span></span>|<span data-ttu-id="b9650-119">说明</span><span class="sxs-lookup"><span data-stu-id="b9650-119">Description</span></span>|  
|-------------|-----------------|  
|[\<message>](message-element-of-wsfederationhttpbinding.md)|<span data-ttu-id="b9650-120">定义元素的消息级安全性设置 [\<wsFederationHttpBinding>](wsfederationhttpbinding.md) 。</span><span class="sxs-lookup"><span data-stu-id="b9650-120">Defines the settings for the message-level security for the [\<wsFederationHttpBinding>](wsfederationhttpbinding.md) element.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="b9650-121">请参阅</span><span class="sxs-lookup"><span data-stu-id="b9650-121">See also</span></span>

- <xref:System.ServiceModel.FederatedMessageSecurityOverHttp>
- <xref:System.ServiceModel.Configuration.FederatedMessageSecurityOverHttpElement.Issuer%2A>
- <xref:System.ServiceModel.Configuration.IssuedTokenParametersEndpointAddressElement>
- [<span data-ttu-id="b9650-122">服务标识和身份验证</span><span class="sxs-lookup"><span data-stu-id="b9650-122">Service Identity and Authentication</span></span>](../../../wcf/feature-details/service-identity-and-authentication.md)
- [<span data-ttu-id="b9650-123">联合令牌与颁发的令牌</span><span class="sxs-lookup"><span data-stu-id="b9650-123">Federation and Issued Tokens</span></span>](../../../wcf/feature-details/federation-and-issued-tokens.md)
- [<span data-ttu-id="b9650-124">服务标识和身份验证</span><span class="sxs-lookup"><span data-stu-id="b9650-124">Service Identity and Authentication</span></span>](../../../wcf/feature-details/service-identity-and-authentication.md)
- [<span data-ttu-id="b9650-125">联合令牌与颁发的令牌</span><span class="sxs-lookup"><span data-stu-id="b9650-125">Federation and Issued Tokens</span></span>](../../../wcf/feature-details/federation-and-issued-tokens.md)
- [<span data-ttu-id="b9650-126">使用自定义绑定的安全功能</span><span class="sxs-lookup"><span data-stu-id="b9650-126">Security Capabilities with Custom Bindings</span></span>](../../../wcf/feature-details/security-capabilities-with-custom-bindings.md)
- [<span data-ttu-id="b9650-127">联合令牌与颁发的令牌</span><span class="sxs-lookup"><span data-stu-id="b9650-127">Federation and Issued Tokens</span></span>](../../../wcf/feature-details/federation-and-issued-tokens.md)
