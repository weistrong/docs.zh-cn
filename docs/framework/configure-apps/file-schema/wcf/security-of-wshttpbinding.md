---
description: 了解详细 <security> 信息： <wsHttpBinding>
title: <security> 的 <wsHttpBinding>
ms.date: 03/30/2017
ms.assetid: 8658b162-2ddf-4162-a869-aa517a42288a
ms.openlocfilehash: 646d49bd67b2b544ae2616f206bfdeabf7806579
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99683055"
---
# <a name="security-of-wshttpbinding"></a><span data-ttu-id="be006-103">\<security> 的 \<wsHttpBinding></span><span class="sxs-lookup"><span data-stu-id="be006-103">\<security> of \<wsHttpBinding></span></span>

<span data-ttu-id="be006-104">表示的安全功能 [\<wsHttpBinding>](wshttpbinding.md) 。</span><span class="sxs-lookup"><span data-stu-id="be006-104">Represents the security capabilities of the [\<wsHttpBinding>](wshttpbinding.md).</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<bindings>**](bindings.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<wsHttpBinding>**](wshttpbinding.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<binding>**\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<security>**  
  
## <a name="syntax"></a><span data-ttu-id="be006-105">语法</span><span class="sxs-lookup"><span data-stu-id="be006-105">Syntax</span></span>  
  
```xml  
<security mode="Message/None/Transport/TransportWithMessageCredential">
  <transport clientCredentialType="Basic/Certificate/Digest/None/Ntlm/Windows"
             proxyCredentialType="Basic/Digest/None/Ntlm/Windows"
             realm="String"
             defaultClientCredentialType="Basic/Certificate/Digest/None/Ntlm/Windows"
             defaultProxyCredentialType="Basic/Digest/None/Ntlm/Windows"
             defaultRealm="String" />
  <message clientCredentialType="Certificate/IssuedToken/None/UserName/Windows"
           algorithmSuite="Basic128/Basic192/Basic256/Basic128Rsa15/Basic256Rsa15/TripleDes/TripleDesRsa15/Basic128Sha256/Basic192Sha256/TripleDesSha256/Basic128Sha256Rsa15/Basic192Sha256Rsa15/Basic256Sha256Rsa15/TripleDesSha256Rsa15"
           establishSecurityContext="Boolean"
           negotiateServiceCredential="Boolean" />
</security>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="be006-106">特性和元素</span><span class="sxs-lookup"><span data-stu-id="be006-106">Attributes and Elements</span></span>  

 <span data-ttu-id="be006-107">以下几节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="be006-107">The following sections describe attributes, child elements, and parent elements</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="be006-108">特性</span><span class="sxs-lookup"><span data-stu-id="be006-108">Attributes</span></span>  
  
|<span data-ttu-id="be006-109">属性</span><span class="sxs-lookup"><span data-stu-id="be006-109">Attribute</span></span>|<span data-ttu-id="be006-110">说明</span><span class="sxs-lookup"><span data-stu-id="be006-110">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="be006-111">mode</span><span class="sxs-lookup"><span data-stu-id="be006-111">mode</span></span>|<span data-ttu-id="be006-112">可有可无.</span><span class="sxs-lookup"><span data-stu-id="be006-112">-   Optional.</span></span> <span data-ttu-id="be006-113">指定所应用的安全类型。</span><span class="sxs-lookup"><span data-stu-id="be006-113">Specifies the type of security that is applied.</span></span> <span data-ttu-id="be006-114">默认值为 `Message`。</span><span class="sxs-lookup"><span data-stu-id="be006-114">The default is `Message`.</span></span><br /><span data-ttu-id="be006-115">-此属性的类型为 <xref:System.ServiceModel.SecurityMode> 。</span><span class="sxs-lookup"><span data-stu-id="be006-115">-   This attribute is of type <xref:System.ServiceModel.SecurityMode>.</span></span>|  
  
## <a name="mode-attribute"></a><span data-ttu-id="be006-116">Mode 属性</span><span class="sxs-lookup"><span data-stu-id="be006-116">Mode Attribute</span></span>  
  
|<span data-ttu-id="be006-117">值</span><span class="sxs-lookup"><span data-stu-id="be006-117">Value</span></span>|<span data-ttu-id="be006-118">说明</span><span class="sxs-lookup"><span data-stu-id="be006-118">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="be006-119">无</span><span class="sxs-lookup"><span data-stu-id="be006-119">None</span></span>|<span data-ttu-id="be006-120">禁用安全性。</span><span class="sxs-lookup"><span data-stu-id="be006-120">Security is disabled.</span></span>|  
|<span data-ttu-id="be006-121">Transport</span><span class="sxs-lookup"><span data-stu-id="be006-121">Transport</span></span>|<span data-ttu-id="be006-122">使用 HTTPS 提供安全性。</span><span class="sxs-lookup"><span data-stu-id="be006-122">Security is provided using HTTPS.</span></span> <span data-ttu-id="be006-123">此服务需要使用 SSL 证书进行配置。</span><span class="sxs-lookup"><span data-stu-id="be006-123">The service needs to be configured with SSL certificates.</span></span> <span data-ttu-id="be006-124">消息使用 HTTPS 得到了全面保护，客户端使用服务的 SSL 证书对消息进行身份验证。</span><span class="sxs-lookup"><span data-stu-id="be006-124">The message is entirely secured using HTTPS and is authenticated by the client using the service’s SSL certificate.</span></span> <span data-ttu-id="be006-125">客户端身份验证通过</span><span class="sxs-lookup"><span data-stu-id="be006-125">The client authentication is controlled through the `ClientCredentials` attribute.</span></span> <span data-ttu-id="be006-126">的 [\<transport>](transport-of-wshttpbinding.md) 。</span><span class="sxs-lookup"><span data-stu-id="be006-126">of the [\<transport>](transport-of-wshttpbinding.md).</span></span>|  
|<span data-ttu-id="be006-127">消息</span><span class="sxs-lookup"><span data-stu-id="be006-127">Message</span></span>|<span data-ttu-id="be006-128">使用 SOAP 消息安全提供安全性。</span><span class="sxs-lookup"><span data-stu-id="be006-128">Security is provided using SOAP message security.</span></span> <span data-ttu-id="be006-129">默认情况下，将对 SOAP 正文进行加密和签名。</span><span class="sxs-lookup"><span data-stu-id="be006-129">By default, the SOAP body is Encrypted and Signed.</span></span> <span data-ttu-id="be006-130">此模式提供了各种各样的功能，例如服务凭据在带外客户端是否可用、要使用的算法套件以及通过 Security.Message 属性要应用于消息正文的保护级别。</span><span class="sxs-lookup"><span data-stu-id="be006-130">This mode offers a variety of features, such as whether the service credentials are available at the client out of band, the algorithm suite to use, and what level of protection to apply to the message body through the Security.Message property.</span></span> <span data-ttu-id="be006-131">每个会话将执行一次客户端身份验证，身份验证的结果在会话过程中将被缓存。</span><span class="sxs-lookup"><span data-stu-id="be006-131">Client authentication is performed once per session and the results of authentication are cached for the duration of the session.</span></span>|  
|<span data-ttu-id="be006-132">TransportWithMessageCredential</span><span class="sxs-lookup"><span data-stu-id="be006-132">TransportWithMessageCredential</span></span>|<span data-ttu-id="be006-133">在此模式下，HTTPS 将提供完整性、保密性和服务器身份验证，SOAP 消息安全将提供客户端身份验证。</span><span class="sxs-lookup"><span data-stu-id="be006-133">In this mode, HTTPS provides integrity, confidentiality, and server authentication, and SOAP message security provides client authentication.</span></span> <span data-ttu-id="be006-134">默认情况下，每个会话将执行一次客户端身份验证，身份验证的结果在会话过程中将被缓存。</span><span class="sxs-lookup"><span data-stu-id="be006-134">By default, client authentication is performed once per session and the results of authentication are cached for the duration of the session.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="be006-135">子元素</span><span class="sxs-lookup"><span data-stu-id="be006-135">Child Elements</span></span>  
  
|<span data-ttu-id="be006-136">元素</span><span class="sxs-lookup"><span data-stu-id="be006-136">Element</span></span>|<span data-ttu-id="be006-137">说明</span><span class="sxs-lookup"><span data-stu-id="be006-137">Description</span></span>|  
|-------------|-----------------|  
|[\<transport>](transport-of-wshttpbinding.md)|<span data-ttu-id="be006-138">定义传输安全设置。</span><span class="sxs-lookup"><span data-stu-id="be006-138">Defines the transport security settings.</span></span> <span data-ttu-id="be006-139">此元素与 <xref:System.ServiceModel.Configuration.HttpTransportSecurityElement> 类型相对应。</span><span class="sxs-lookup"><span data-stu-id="be006-139">This element corresponds to the <xref:System.ServiceModel.Configuration.HttpTransportSecurityElement> type.</span></span>|  
|[\<message>](message-of-wshttpbinding.md)|<span data-ttu-id="be006-140">定义消息的安全设置。</span><span class="sxs-lookup"><span data-stu-id="be006-140">Defines the security settings for the message.</span></span> <span data-ttu-id="be006-141">此元素与 <xref:System.ServiceModel.Configuration.MessageSecurityOverHttpElement> 类型相对应。</span><span class="sxs-lookup"><span data-stu-id="be006-141">This element corresponds to the <xref:System.ServiceModel.Configuration.MessageSecurityOverHttpElement> type.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="be006-142">父元素</span><span class="sxs-lookup"><span data-stu-id="be006-142">Parent Elements</span></span>  
  
|<span data-ttu-id="be006-143">元素</span><span class="sxs-lookup"><span data-stu-id="be006-143">Element</span></span>|<span data-ttu-id="be006-144">说明</span><span class="sxs-lookup"><span data-stu-id="be006-144">Description</span></span>|  
|-------------|-----------------|  
|[\<wsHttpBinding>](wshttpbinding.md)|<span data-ttu-id="be006-145">HTTP 传输应用程序的安全绑定。</span><span class="sxs-lookup"><span data-stu-id="be006-145">A secure binding for HTTP transport applications.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="be006-146">备注</span><span class="sxs-lookup"><span data-stu-id="be006-146">Remarks</span></span>  

 <span data-ttu-id="be006-147">WSHttpBinding 类专用于与实现 WS-\* 规范的服务进行互操作。</span><span class="sxs-lookup"><span data-stu-id="be006-147">The WSHttpBinding class is designed for interoperation with services that implement WS-\* specifications.</span></span> <span data-ttu-id="be006-148">此绑定的传输安全为 HTTP 上的安全套接字层 (SSL)，即 HTTPS。</span><span class="sxs-lookup"><span data-stu-id="be006-148">The transport security for this binding is Secure Sockets Layer (SSL) over HTTP, or HTTPS.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="be006-149">请参阅</span><span class="sxs-lookup"><span data-stu-id="be006-149">See also</span></span>

- <xref:System.ServiceModel.WSHttpSecurity>
- <xref:System.ServiceModel.WSHttpBinding.Security%2A>
- <xref:System.ServiceModel.Configuration.WSHttpBindingElement.Security%2A>
- <xref:System.ServiceModel.Configuration.WSHttpSecurityElement>
- [<span data-ttu-id="be006-150">保护服务和客户端的安全</span><span class="sxs-lookup"><span data-stu-id="be006-150">Securing Services and Clients</span></span>](../../../wcf/feature-details/securing-services-and-clients.md)
- [<span data-ttu-id="be006-151">绑定</span><span class="sxs-lookup"><span data-stu-id="be006-151">Bindings</span></span>](../../../wcf/bindings.md)
- [<span data-ttu-id="be006-152">配置系统提供的绑定</span><span class="sxs-lookup"><span data-stu-id="be006-152">Configuring System-Provided Bindings</span></span>](../../../wcf/feature-details/configuring-system-provided-bindings.md)
- [<span data-ttu-id="be006-153">使用绑定配置服务和客户端</span><span class="sxs-lookup"><span data-stu-id="be006-153">Using Bindings to Configure Services and Clients</span></span>](../../../wcf/using-bindings-to-configure-services-and-clients.md)
- [\<binding>](bindings.md)
