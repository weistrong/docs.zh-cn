---
description: 详细了解： <security> 的元素 <ws2007FederationHttpBinding>
title: <security> 的元素 <ws2007FederationHttpBinding>
ms.date: 03/30/2017
ms.assetid: 826219b4-3a16-45fc-832d-0cd7cbbd3b84
ms.openlocfilehash: 0caa2c3791c0dc3c8db0d9ee27175a28e52f6baa
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99683289"
---
# <a name="security-element-of-ws2007federationhttpbinding"></a><span data-ttu-id="4ad0e-103">\<security> 的元素 \<ws2007FederationHttpBinding></span><span class="sxs-lookup"><span data-stu-id="4ad0e-103">\<security> element of \<ws2007FederationHttpBinding></span></span>

<span data-ttu-id="4ad0e-104">定义元素的安全设置 [\<ws2007FederationHttpBinding>](ws2007federationhttpbinding.md) 。</span><span class="sxs-lookup"><span data-stu-id="4ad0e-104">Defines the security settings of the [\<ws2007FederationHttpBinding>](ws2007federationhttpbinding.md) element.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<bindings>**](bindings.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<ws2007FederationHttpBinding>**](ws2007federationhttpbinding.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<binding>**\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<security>**  
  
## <a name="syntax"></a><span data-ttu-id="4ad0e-105">语法</span><span class="sxs-lookup"><span data-stu-id="4ad0e-105">Syntax</span></span>  
  
```xml  
<ws2007FederationBinding>
  <binding>
    <security mode="None/Message/TransportWithMessageCredential">
      <message negotiateServiceCredential="Boolean"
               algorithmSuite="Basic128/Basic192/Basic256/Basic128Rsa15/  Basic256Rsa15/TripleDes/TripleDesRsa15/Basic128Sha256/Basic192Sha256/TripleDesSha256/Basic128Sha256Rsa15/Basic192Sha256Rsa15/Basic256Sha256Rsa15/TripleDesSha256Rsa15"
               defaultProtectionLevel="none/sign/EncryptAndSign"
               issuedTokenType="string"
               issuedKeyType="SymmetricKey/PublicKey">
      </message>
    </security>
  </binding>
</ws2007FederationBinding>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="4ad0e-106">特性和元素</span><span class="sxs-lookup"><span data-stu-id="4ad0e-106">Attributes and Elements</span></span>  

 <span data-ttu-id="4ad0e-107">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="4ad0e-107">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="4ad0e-108">特性</span><span class="sxs-lookup"><span data-stu-id="4ad0e-108">Attributes</span></span>  
  
|<span data-ttu-id="4ad0e-109">属性</span><span class="sxs-lookup"><span data-stu-id="4ad0e-109">Attribute</span></span>|<span data-ttu-id="4ad0e-110">说明</span><span class="sxs-lookup"><span data-stu-id="4ad0e-110">Description</span></span>|  
|---------------|-----------------|  
|`mode`|<span data-ttu-id="4ad0e-111">可选。</span><span class="sxs-lookup"><span data-stu-id="4ad0e-111">Optional.</span></span> <span data-ttu-id="4ad0e-112">指定所应用的安全类型。</span><span class="sxs-lookup"><span data-stu-id="4ad0e-112">Specifies the type of security that is applied.</span></span> <span data-ttu-id="4ad0e-113">默认值是 `Message`。</span><span class="sxs-lookup"><span data-stu-id="4ad0e-113">The default value is `Message`.</span></span> <span data-ttu-id="4ad0e-114">此属性的类型为 <xref:System.ServiceModel.WSFederationHttpSecurityMode>。</span><span class="sxs-lookup"><span data-stu-id="4ad0e-114">This attribute is of type <xref:System.ServiceModel.WSFederationHttpSecurityMode>.</span></span>|  
  
## <a name="mode-attribute"></a><span data-ttu-id="4ad0e-115">mode 属性</span><span class="sxs-lookup"><span data-stu-id="4ad0e-115">mode Attribute</span></span>  
  
|<span data-ttu-id="4ad0e-116">值</span><span class="sxs-lookup"><span data-stu-id="4ad0e-116">Value</span></span>|<span data-ttu-id="4ad0e-117">说明</span><span class="sxs-lookup"><span data-stu-id="4ad0e-117">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="4ad0e-118">无</span><span class="sxs-lookup"><span data-stu-id="4ad0e-118">None</span></span>|<span data-ttu-id="4ad0e-119">SOAP 消息在传输过程中并不安全。</span><span class="sxs-lookup"><span data-stu-id="4ad0e-119">The SOAP message is not secure during transfer.</span></span>|  
|<span data-ttu-id="4ad0e-120">消息</span><span class="sxs-lookup"><span data-stu-id="4ad0e-120">Message</span></span>|<span data-ttu-id="4ad0e-121">通过使用 SOAP 消息安全，可以提供完整性、保密性、服务器身份验证和客户端身份验证。</span><span class="sxs-lookup"><span data-stu-id="4ad0e-121">Integrity, confidentiality, server authentication and client authentication are provided using SOAP message security.</span></span> <span data-ttu-id="4ad0e-122">默认情况下，将对正文进行加密和签名。</span><span class="sxs-lookup"><span data-stu-id="4ad0e-122">By default, the body is encrypted and signed.</span></span> <span data-ttu-id="4ad0e-123">此服务必须使用证书进行配置。</span><span class="sxs-lookup"><span data-stu-id="4ad0e-123">The service must be configured with a certificate.</span></span> <span data-ttu-id="4ad0e-124">客户端根据由安全令牌服务颁发给客户端的令牌进行身份验证。</span><span class="sxs-lookup"><span data-stu-id="4ad0e-124">Client authentication is based on the token issued to the client by a security token service.</span></span>|  
|<span data-ttu-id="4ad0e-125">TransportWithMessageCredential</span><span class="sxs-lookup"><span data-stu-id="4ad0e-125">TransportWithMessageCredential</span></span>|<span data-ttu-id="4ad0e-126">完整性、保密性和服务器身份验证均由 HTTPS 提供。</span><span class="sxs-lookup"><span data-stu-id="4ad0e-126">Integrity, confidentiality and server authentication are provided by HTTPS.</span></span> <span data-ttu-id="4ad0e-127">此服务必须使用证书进行配置。</span><span class="sxs-lookup"><span data-stu-id="4ad0e-127">The service must be configured with a certificate.</span></span> <span data-ttu-id="4ad0e-128">客户端身份验证采用 SOAP 消息安全方式提供，并根据由安全令牌服务颁发给客户端的令牌进行。</span><span class="sxs-lookup"><span data-stu-id="4ad0e-128">Client authentication is provided by means of SOAP message security and is based on the token issued to the client by a security token service.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="4ad0e-129">子元素</span><span class="sxs-lookup"><span data-stu-id="4ad0e-129">Child Elements</span></span>  
  
|<span data-ttu-id="4ad0e-130">元素</span><span class="sxs-lookup"><span data-stu-id="4ad0e-130">Element</span></span>|<span data-ttu-id="4ad0e-131">说明</span><span class="sxs-lookup"><span data-stu-id="4ad0e-131">Description</span></span>|  
|-------------|-----------------|  
|[\<message>](message-of-ws2007httpbinding.md)|<span data-ttu-id="4ad0e-132">定义消息级安全性设置。</span><span class="sxs-lookup"><span data-stu-id="4ad0e-132">Defines the settings for the message-level security.</span></span> <span data-ttu-id="4ad0e-133">此元素的类型为 <xref:System.ServiceModel.Configuration.FederatedMessageSecurityOverHttpElement>。</span><span class="sxs-lookup"><span data-stu-id="4ad0e-133">This element is of type <xref:System.ServiceModel.Configuration.FederatedMessageSecurityOverHttpElement>.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="4ad0e-134">父元素</span><span class="sxs-lookup"><span data-stu-id="4ad0e-134">Parent Elements</span></span>  
  
|<span data-ttu-id="4ad0e-135">元素</span><span class="sxs-lookup"><span data-stu-id="4ad0e-135">Element</span></span>|<span data-ttu-id="4ad0e-136">说明</span><span class="sxs-lookup"><span data-stu-id="4ad0e-136">Description</span></span>|  
|-------------|-----------------|  
|[\<binding>](bindings.md)|<span data-ttu-id="4ad0e-137">定义的所有绑定功能 [\<wsDualHttpBinding>](wsdualhttpbinding.md) 。</span><span class="sxs-lookup"><span data-stu-id="4ad0e-137">Defines all binding capabilities of the [\<wsDualHttpBinding>](wsdualhttpbinding.md).</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="4ad0e-138">请参阅</span><span class="sxs-lookup"><span data-stu-id="4ad0e-138">See also</span></span>

- <xref:System.ServiceModel.WSFederationHttpSecurity>
- <xref:System.ServiceModel.WSFederationHttpBinding.Security%2A>
- <xref:System.ServiceModel.Configuration.WSFederationHttpBindingElement.Security%2A>
- <xref:System.ServiceModel.Configuration.WSFederationHttpSecurityElement>
- [<span data-ttu-id="4ad0e-139">如何：创建 WSFederationHttpBinding</span><span class="sxs-lookup"><span data-stu-id="4ad0e-139">How to: Create a WSFederationHttpBinding</span></span>](../../../wcf/feature-details/how-to-create-a-wsfederationhttpbinding.md)
- [<span data-ttu-id="4ad0e-140">保护服务和客户端的安全</span><span class="sxs-lookup"><span data-stu-id="4ad0e-140">Securing Services and Clients</span></span>](../../../wcf/feature-details/securing-services-and-clients.md)
- [<span data-ttu-id="4ad0e-141">选择凭据类型</span><span class="sxs-lookup"><span data-stu-id="4ad0e-141">Selecting a Credential Type</span></span>](../../../wcf/feature-details/selecting-a-credential-type.md)
- [<span data-ttu-id="4ad0e-142">绑定</span><span class="sxs-lookup"><span data-stu-id="4ad0e-142">Bindings</span></span>](../../../wcf/bindings.md)
- [<span data-ttu-id="4ad0e-143">配置系统提供的绑定</span><span class="sxs-lookup"><span data-stu-id="4ad0e-143">Configuring System-Provided Bindings</span></span>](../../../wcf/feature-details/configuring-system-provided-bindings.md)
- [<span data-ttu-id="4ad0e-144">使用绑定配置服务和客户端</span><span class="sxs-lookup"><span data-stu-id="4ad0e-144">Using Bindings to Configure Services and Clients</span></span>](../../../wcf/using-bindings-to-configure-services-and-clients.md)
- [\<binding>](bindings.md)
