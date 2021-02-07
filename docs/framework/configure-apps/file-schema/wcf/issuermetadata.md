---
description: 了解详细信息： <issuerMetadata>
title: <issuerMetadata>
ms.date: 03/30/2017
ms.assetid: e7eae2c0-cc17-4281-af59-e4eb8d54f92a
ms.openlocfilehash: 86671b6b704f5753cf4bd45c2dfd90a368070b22
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99725527"
---
# \<issuerMetadata>

[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<bindings>**](bindings.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<wsFederationHttpBinding>**](wsfederationhttpbinding.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<binding>**\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<security>**](security-of-wsfederationhttpbinding.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<message>**](message-element-of-wsfederationhttpbinding.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<issuerMetadata>**  
  
## <a name="syntax"></a><span data-ttu-id="48d3a-102">语法</span><span class="sxs-lookup"><span data-stu-id="48d3a-102">Syntax</span></span>  
  
```xml  
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
                          x509FindType="System.Security.Cryptography.X509certificates.X509findtype" />
    <dns value="String" />
    <rsa value="String" />
    <servicePrincipalName value="String" />
    <usePrincipalName value="String" />
  </identity>
</issuerMetadata>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="48d3a-103">特性和元素</span><span class="sxs-lookup"><span data-stu-id="48d3a-103">Attributes and Elements</span></span>  

 <span data-ttu-id="48d3a-104">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="48d3a-104">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="48d3a-105">特性</span><span class="sxs-lookup"><span data-stu-id="48d3a-105">Attributes</span></span>  
  
|<span data-ttu-id="48d3a-106">属性</span><span class="sxs-lookup"><span data-stu-id="48d3a-106">Attribute</span></span>|<span data-ttu-id="48d3a-107">说明</span><span class="sxs-lookup"><span data-stu-id="48d3a-107">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="48d3a-108">address</span><span class="sxs-lookup"><span data-stu-id="48d3a-108">address</span></span>|<span data-ttu-id="48d3a-109">必选的 `string` 特性。</span><span class="sxs-lookup"><span data-stu-id="48d3a-109">Required `string` attribute.</span></span><br /><br /> <span data-ttu-id="48d3a-110">指定终结点的地址。</span><span class="sxs-lookup"><span data-stu-id="48d3a-110">Specifies the address of the endpoint.</span></span> <span data-ttu-id="48d3a-111">该地址必须为绝对 URI。</span><span class="sxs-lookup"><span data-stu-id="48d3a-111">The address must be an absolute URI.</span></span> <span data-ttu-id="48d3a-112">默认值为一个空字符串。</span><span class="sxs-lookup"><span data-stu-id="48d3a-112">The default value is an empty string.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="48d3a-113">子元素</span><span class="sxs-lookup"><span data-stu-id="48d3a-113">Child Elements</span></span>  
  
|<span data-ttu-id="48d3a-114">元素</span><span class="sxs-lookup"><span data-stu-id="48d3a-114">Element</span></span>|<span data-ttu-id="48d3a-115">说明</span><span class="sxs-lookup"><span data-stu-id="48d3a-115">Description</span></span>|  
|-------------|-----------------|  
|[\<headers>](headers-element.md)|<span data-ttu-id="48d3a-116">一个地址标头集合。</span><span class="sxs-lookup"><span data-stu-id="48d3a-116">A collection of address headers.</span></span>|  
|[\<identity>](identity.md)|<span data-ttu-id="48d3a-117">一个标识，与某个终结点交换消息的其他终结点可以使用该标识对该终结点进行身份验证。</span><span class="sxs-lookup"><span data-stu-id="48d3a-117">An identity that enables the authentication of an endpoint by other endpoints exchanging messages with it.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="48d3a-118">父元素</span><span class="sxs-lookup"><span data-stu-id="48d3a-118">Parent Elements</span></span>  
  
|<span data-ttu-id="48d3a-119">元素</span><span class="sxs-lookup"><span data-stu-id="48d3a-119">Element</span></span>|<span data-ttu-id="48d3a-120">说明</span><span class="sxs-lookup"><span data-stu-id="48d3a-120">Description</span></span>|  
|-------------|-----------------|  
|[\<message>](message-element-of-wsfederationhttpbinding.md)|<span data-ttu-id="48d3a-121">定义元素的消息级安全性设置 [\<wsFederationHttpBinding>](wsfederationhttpbinding.md) 。</span><span class="sxs-lookup"><span data-stu-id="48d3a-121">Defines the settings for the message-level security for the [\<wsFederationHttpBinding>](wsfederationhttpbinding.md) element.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="48d3a-122">请参阅</span><span class="sxs-lookup"><span data-stu-id="48d3a-122">See also</span></span>

- <xref:System.ServiceModel.FederatedMessageSecurityOverHttp.IssuerMetadataAddress%2A>
- <xref:System.ServiceModel.Configuration.FederatedMessageSecurityOverHttpElement.IssuerMetadata%2A>
- [<span data-ttu-id="48d3a-123">服务标识和身份验证</span><span class="sxs-lookup"><span data-stu-id="48d3a-123">Service Identity and Authentication</span></span>](../../../wcf/feature-details/service-identity-and-authentication.md)
- [<span data-ttu-id="48d3a-124">联合令牌与颁发的令牌</span><span class="sxs-lookup"><span data-stu-id="48d3a-124">Federation and Issued Tokens</span></span>](../../../wcf/feature-details/federation-and-issued-tokens.md)
- [<span data-ttu-id="48d3a-125">使用自定义绑定的安全功能</span><span class="sxs-lookup"><span data-stu-id="48d3a-125">Security Capabilities with Custom Bindings</span></span>](../../../wcf/feature-details/security-capabilities-with-custom-bindings.md)
- [<span data-ttu-id="48d3a-126">联合令牌与颁发的令牌</span><span class="sxs-lookup"><span data-stu-id="48d3a-126">Federation and Issued Tokens</span></span>](../../../wcf/feature-details/federation-and-issued-tokens.md)
