---
description: 了解详细信息： <identity>
title: <identity>
ms.date: 03/30/2017
ms.assetid: c1d2ae56-e231-4a07-9c3f-9f13381dc0d8
ms.openlocfilehash: ceb4dc0e7efa6cd01204253001432ed1ef2c048e
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99802250"
---
# \<identity>

<span data-ttu-id="d0816-102">标识元素允许客户端开发人员在设计时指定服务的期望标识。</span><span class="sxs-lookup"><span data-stu-id="d0816-102">The identity element allows a client developer to specify at design time the expected identity of the service.</span></span> <span data-ttu-id="d0816-103">在客户端与服务之间的握手过程中，Windows Communication Foundation (WCF) 基础结构将确保预期服务的标识与此元素的值相匹配，因而可以进行身份验证。</span><span class="sxs-lookup"><span data-stu-id="d0816-103">In the handshake process between the client and service, the Windows Communication Foundation (WCF) infrastructure will ensure that the identity of the expected service matches the values of this element, and thus can be authenticated.</span></span> <span data-ttu-id="d0816-104">有关详细信息，请参阅 [服务标识和身份验证](../../../wcf/feature-details/service-identity-and-authentication.md)。</span><span class="sxs-lookup"><span data-stu-id="d0816-104">For more information, see [Service Identity and Authentication](../../../wcf/feature-details/service-identity-and-authentication.md).</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<client>**](client.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<endpoint>**](endpoint-of-client.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<identity>**  
  
## <a name="syntax"></a><span data-ttu-id="d0816-105">语法</span><span class="sxs-lookup"><span data-stu-id="d0816-105">Syntax</span></span>  
  
```xml  
<identity>
  <certificate encodedValue="String" />
  <certificateReference findValue="String"
                        isChainIncluded="Boolean"
                        storeName="AddressBook/AuthRoot/CertificateAuthority/Disallowed/My/Root/TrustedPeople/TrustedPublisher"
                        storeLocation="LocalMachine/CurrentUser"
                        X509FindType="Enumeration" />
  <dns value="String" />
  <rsa value="String" />
  <servicePrincipalName value="String" />
  <userPrincipalName value="String" />
</identity>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="d0816-106">特性和元素</span><span class="sxs-lookup"><span data-stu-id="d0816-106">Attributes and Elements</span></span>  

 <span data-ttu-id="d0816-107">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="d0816-107">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="d0816-108">特性</span><span class="sxs-lookup"><span data-stu-id="d0816-108">Attributes</span></span>  

 <span data-ttu-id="d0816-109">无。</span><span class="sxs-lookup"><span data-stu-id="d0816-109">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="d0816-110">子元素</span><span class="sxs-lookup"><span data-stu-id="d0816-110">Child Elements</span></span>  
  
|<span data-ttu-id="d0816-111">元素</span><span class="sxs-lookup"><span data-stu-id="d0816-111">Element</span></span>|<span data-ttu-id="d0816-112">说明</span><span class="sxs-lookup"><span data-stu-id="d0816-112">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="d0816-113">证书 (certificate)</span><span class="sxs-lookup"><span data-stu-id="d0816-113">certificate</span></span>|<span data-ttu-id="d0816-114">指定 X.509 证书的设置。</span><span class="sxs-lookup"><span data-stu-id="d0816-114">Specifies settings of an X.509 certificate.</span></span> <span data-ttu-id="d0816-115">此元素的类型为 <xref:System.ServiceModel.Configuration.CertificateElement>。</span><span class="sxs-lookup"><span data-stu-id="d0816-115">This element is of type <xref:System.ServiceModel.Configuration.CertificateElement>.</span></span> <span data-ttu-id="d0816-116">它包含一个 `encodedValue` 属性，该属性是一个字符串，用于指定此证书编码的值。</span><span class="sxs-lookup"><span data-stu-id="d0816-116">It contains an attribute `encodedValue` that is a string, which specifies the value encoded by this certificate.</span></span>|  
|<span data-ttu-id="d0816-117">certificateReference</span><span class="sxs-lookup"><span data-stu-id="d0816-117">certificateReference</span></span>|<span data-ttu-id="d0816-118">指定 X.509 证书验证的设置。</span><span class="sxs-lookup"><span data-stu-id="d0816-118">Specifies settings for X.509 certificate validation.</span></span> <span data-ttu-id="d0816-119">此元素的类型为 <xref:System.ServiceModel.Configuration.CertificateReferenceElement>。</span><span class="sxs-lookup"><span data-stu-id="d0816-119">This element is of type <xref:System.ServiceModel.Configuration.CertificateReferenceElement>.</span></span>|  
|<span data-ttu-id="d0816-120">dns</span><span class="sxs-lookup"><span data-stu-id="d0816-120">dns</span></span>|<span data-ttu-id="d0816-121">指定用于对服务进行身份验证的 X.509 证书的 DNS。</span><span class="sxs-lookup"><span data-stu-id="d0816-121">Specifies the DNS of an X.509 certificate used to authenticate a service.</span></span> <span data-ttu-id="d0816-122">此元素包含一个字符串属性 `value`，并包含实际的标识。</span><span class="sxs-lookup"><span data-stu-id="d0816-122">This element contains an attribute `value` that is a string, and contains the actual identity.</span></span>|  
|<span data-ttu-id="d0816-123">rsa</span><span class="sxs-lookup"><span data-stu-id="d0816-123">rsa</span></span>|<span data-ttu-id="d0816-124">指定用于向客户端验证服务身份的 X.509 证书的 RSA 字段的值。</span><span class="sxs-lookup"><span data-stu-id="d0816-124">Specifies the value of the RSA field of an X.509 certificate used to authenticate a service to a client.</span></span> <span data-ttu-id="d0816-125">此元素包含一个字符串属性 `value`，并包含实际的标识。</span><span class="sxs-lookup"><span data-stu-id="d0816-125">This element contains an attribute `value` that is a string, and contains the actual identity</span></span>|  
|<span data-ttu-id="d0816-126">servicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="d0816-126">servicePrincipalName</span></span>|<span data-ttu-id="d0816-127">指定服务器主体名称 (SPN) 标识，它是客户端用来唯一标识一个服务实例的主体名称。</span><span class="sxs-lookup"><span data-stu-id="d0816-127">Specifies a server principal name (SPN) identity, which is the principal name used by a client to uniquely identify an instance of a service.</span></span> <span data-ttu-id="d0816-128">此元素包含一个 `value` 属性，该属性是一个字符串，其中包含实际的主体名称。</span><span class="sxs-lookup"><span data-stu-id="d0816-128">This element contains an attribute `value` that is a string, and contains the actual principal name.</span></span> <span data-ttu-id="d0816-129">此元素的类型为 <xref:System.ServiceModel.Configuration.ServicePrincipalNameElement>。</span><span class="sxs-lookup"><span data-stu-id="d0816-129">This element is of type <xref:System.ServiceModel.Configuration.ServicePrincipalNameElement>.</span></span>|  
|<span data-ttu-id="d0816-130">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="d0816-130">userPrincipalName</span></span>|<span data-ttu-id="d0816-131">指定用户主体名称 (UPN) 标识，它是网络上的用户登录名类型。</span><span class="sxs-lookup"><span data-stu-id="d0816-131">Specifies a user principal name (UPN) identity, which is the logon name type of a user on a network.</span></span> <span data-ttu-id="d0816-132">用户主体名称包含 Active Directory 中使用的用户对象名称，后跟符号 (\@) 然后通常是域名系统父域。</span><span class="sxs-lookup"><span data-stu-id="d0816-132">The user principal name consists of the user object name used in Active Directory, followed by the at symbol (\@) and then, typically, the Domain Name System parent domain.</span></span> <span data-ttu-id="d0816-133">例如，Fabrikam.com 域树中的 Jeff 可能具有用户主体名称 [jeff@fabrikam.com](mailto:jeffsmith@fabrikam.com) 。</span><span class="sxs-lookup"><span data-stu-id="d0816-133">For example, Jeff in the Fabrikam.com domain tree might have the user principal name [jeff@fabrikam.com](mailto:jeffsmith@fabrikam.com).</span></span>  <span data-ttu-id="d0816-134">此元素包含一个 `value` 属性，该属性是一个字符串，其中包含实际的主体名称。</span><span class="sxs-lookup"><span data-stu-id="d0816-134">This element contains an attribute `value` that is a string, and contains the actual principal name.</span></span> <span data-ttu-id="d0816-135">此元素的类型为 <xref:System.ServiceModel.Configuration.UserPrincipalNameElement>。</span><span class="sxs-lookup"><span data-stu-id="d0816-135">This element is of type <xref:System.ServiceModel.Configuration.UserPrincipalNameElement>.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="d0816-136">父元素</span><span class="sxs-lookup"><span data-stu-id="d0816-136">Parent Elements</span></span>  
  
|<span data-ttu-id="d0816-137">元素</span><span class="sxs-lookup"><span data-stu-id="d0816-137">Element</span></span>|<span data-ttu-id="d0816-138">说明</span><span class="sxs-lookup"><span data-stu-id="d0816-138">Description</span></span>|  
|-------------|-----------------|  
|[\<custom>](custom.md)|<span data-ttu-id="d0816-139">指定 netPeerTcpBinding 的自定义对等解析程序。</span><span class="sxs-lookup"><span data-stu-id="d0816-139">Specifies a custom peer resolver for a netPeerTcpBinding.</span></span>|  
|[\<endpoint>](endpoint-element.md)|<span data-ttu-id="d0816-140">配置服务终结点。</span><span class="sxs-lookup"><span data-stu-id="d0816-140">Configures service endpoints.</span></span>|  
|[<span data-ttu-id="d0816-141">\<client> 的 \<endpoint></span><span class="sxs-lookup"><span data-stu-id="d0816-141">\<endpoint> of \<client></span></span>](endpoint-of-client.md)|<span data-ttu-id="d0816-142">配置通道终结点。</span><span class="sxs-lookup"><span data-stu-id="d0816-142">Configures channel endpoints.</span></span>|  
|[\<issuer>](issuer.md)|<span data-ttu-id="d0816-143">指定联合服务的安全令牌服务 (STS)。</span><span class="sxs-lookup"><span data-stu-id="d0816-143">Specifies the Security Token Service (STS) for the federated service.</span></span>|  
|[\<issuerMetadata>](issuermetadata.md)|<span data-ttu-id="d0816-144">指定联合服务的安全令牌服务 (STS) 的元数据终结点。</span><span class="sxs-lookup"><span data-stu-id="d0816-144">Specifies the metadata endpoint for the Security Token Service (STS) of a federated service.</span></span>|  
|[\<issuedTokenParameters>](issuedtokenparameters.md)|<span data-ttu-id="d0816-145">定义自定义绑定中的已颁发令牌的参数。</span><span class="sxs-lookup"><span data-stu-id="d0816-145">Defines parameters for an issued token in a custom binding.</span></span>|  
|[\<localIssuer>](localissuer.md)|<span data-ttu-id="d0816-146">指定本地安全令牌服务 (STS)。</span><span class="sxs-lookup"><span data-stu-id="d0816-146">Specifies a local Security Token Service (STS).</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="d0816-147">请参阅</span><span class="sxs-lookup"><span data-stu-id="d0816-147">See also</span></span>

- <xref:System.ServiceModel.Configuration.IdentityElement>
- <xref:System.ServiceModel.EndpointAddress>
- <xref:System.ServiceModel.EndpointAddress.Identity%2A>
- [<span data-ttu-id="d0816-148">服务标识和身份验证</span><span class="sxs-lookup"><span data-stu-id="d0816-148">Service Identity and Authentication</span></span>](../../../wcf/feature-details/service-identity-and-authentication.md)
- [<span data-ttu-id="d0816-149">终结点：地址、绑定和协定</span><span class="sxs-lookup"><span data-stu-id="d0816-149">Endpoints: Addresses, Bindings, and Contracts</span></span>](../../../wcf/feature-details/endpoints-addresses-bindings-and-contracts.md)
