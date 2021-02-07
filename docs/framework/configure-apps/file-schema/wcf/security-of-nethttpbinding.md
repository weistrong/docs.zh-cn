---
description: 了解详细 <security> 信息： <netHttpBinding>
title: <security> 的 <netHttpBinding>
ms.date: 03/30/2017
ms.assetid: dc41f6f7-cabc-4a64-9fa0-ceabf861b348
ms.openlocfilehash: 70d6363c0ac7fa00d83880ddc8c873548b385a29
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99683120"
---
# <a name="security-of-nethttpbinding"></a><span data-ttu-id="9fe77-103">\<security> 的 \<netHttpBinding></span><span class="sxs-lookup"><span data-stu-id="9fe77-103">\<security> of \<netHttpBinding></span></span>

<span data-ttu-id="9fe77-104">定义的安全功能 [\<netHttpBinding>](nethttpbinding.md) 。</span><span class="sxs-lookup"><span data-stu-id="9fe77-104">Defines the security capabilities of the [\<netHttpBinding>](nethttpbinding.md).</span></span>

[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<bindings>**](bindings.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<netHttpBinding>**](nethttpbinding.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<binding>**\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<security>**  

## <a name="syntax"></a><span data-ttu-id="9fe77-105">语法</span><span class="sxs-lookup"><span data-stu-id="9fe77-105">Syntax</span></span>

```xml
<security mode="Message/None/Transport/TransportWithCredential">
  <transport clientCredentialType="Basic/Certificate/Digest/None/Ntlm/Windows"
             proxyCredentialType="Basic/Digest/None/Ntlm/Windows"
             realm="string" />
  <message algorithmSuite="Basic128/Basic192/Basic256/Basic128Rsa15/Basic256Rsa15/TripleDes/TripleDesRsa15/Basic128Sha256/Basic192Sha256/TripleDesSha256/Basic128Sha256Rsa15/Basic192Sha256Rsa15/Basic256Sha256Rsa15/TripleDesSha256Rsa15"
           clientCredentialType="Certificate/IssuedToken/None/UserName/Windows" />
</security>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="9fe77-106">特性和元素</span><span class="sxs-lookup"><span data-stu-id="9fe77-106">Attributes and elements</span></span>

<span data-ttu-id="9fe77-107">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="9fe77-107">The following sections describe attributes, child elements, and parent elements.</span></span>

### <a name="attributes"></a><span data-ttu-id="9fe77-108">特性</span><span class="sxs-lookup"><span data-stu-id="9fe77-108">Attributes</span></span>

|<span data-ttu-id="9fe77-109">属性</span><span class="sxs-lookup"><span data-stu-id="9fe77-109">Attribute</span></span>|<span data-ttu-id="9fe77-110">说明</span><span class="sxs-lookup"><span data-stu-id="9fe77-110">Description</span></span>|
|---------------|-----------------|
|<span data-ttu-id="9fe77-111">mode</span><span class="sxs-lookup"><span data-stu-id="9fe77-111">mode</span></span>|<span data-ttu-id="9fe77-112">可选。</span><span class="sxs-lookup"><span data-stu-id="9fe77-112">Optional.</span></span> <span data-ttu-id="9fe77-113">指定所使用的安全类型。</span><span class="sxs-lookup"><span data-stu-id="9fe77-113">Specifies the type of security that is used.</span></span> <span data-ttu-id="9fe77-114">默认值为 `None`。</span><span class="sxs-lookup"><span data-stu-id="9fe77-114">The default is `None`.</span></span> <span data-ttu-id="9fe77-115">此属性的类型为 <xref:System.ServiceModel.BasicHttpSecurityMode>。</span><span class="sxs-lookup"><span data-stu-id="9fe77-115">This attribute is of type <xref:System.ServiceModel.BasicHttpSecurityMode>.</span></span>|

## <a name="mode-attribute"></a><span data-ttu-id="9fe77-116">mode 特性</span><span class="sxs-lookup"><span data-stu-id="9fe77-116">mode attribute</span></span>

|<span data-ttu-id="9fe77-117">值</span><span class="sxs-lookup"><span data-stu-id="9fe77-117">Value</span></span>|<span data-ttu-id="9fe77-118">说明</span><span class="sxs-lookup"><span data-stu-id="9fe77-118">Description</span></span>|
|-----------|-----------------|
|<span data-ttu-id="9fe77-119">无</span><span class="sxs-lookup"><span data-stu-id="9fe77-119">None</span></span>|<span data-ttu-id="9fe77-120">-传输过程中消息不受保护。</span><span class="sxs-lookup"><span data-stu-id="9fe77-120">-   Messages are not secured during transfer.</span></span>|
|<span data-ttu-id="9fe77-121">Transport</span><span class="sxs-lookup"><span data-stu-id="9fe77-121">Transport</span></span>|<span data-ttu-id="9fe77-122">使用 HTTPS 传输提供安全性。</span><span class="sxs-lookup"><span data-stu-id="9fe77-122">Security is provided using HTTPS transport.</span></span> <span data-ttu-id="9fe77-123">使用 HTTPS 对 SOAP 消息进行保护。</span><span class="sxs-lookup"><span data-stu-id="9fe77-123">The SOAP messages are secured using HTTPS.</span></span> <span data-ttu-id="9fe77-124">使用服务的 X.509 证书向客户端对服务进行身份验证。</span><span class="sxs-lookup"><span data-stu-id="9fe77-124">The service is authenticated to the client using the service's X.509 certificate.</span></span> <span data-ttu-id="9fe77-125">使用所提供的 ClientCredentialType 对客户端进行身份验证。</span><span class="sxs-lookup"><span data-stu-id="9fe77-125">The client is authenticated using the ClientCredentialType supplied.</span></span>|
|<span data-ttu-id="9fe77-126">消息</span><span class="sxs-lookup"><span data-stu-id="9fe77-126">Message</span></span>|<span data-ttu-id="9fe77-127">使用 SOAP 消息安全提供安全性。</span><span class="sxs-lookup"><span data-stu-id="9fe77-127">Security is provided using SOAP message security.</span></span> <span data-ttu-id="9fe77-128">默认情况下，将对正文进行加密和签名。</span><span class="sxs-lookup"><span data-stu-id="9fe77-128">By default, the body is encrypted and signed.</span></span> <span data-ttu-id="9fe77-129">对于此绑定，系统要求向带外客户端提供服务器证书。</span><span class="sxs-lookup"><span data-stu-id="9fe77-129">For this binding, the system requires that the server certificate be provided to the client out of band.</span></span> <span data-ttu-id="9fe77-130">此绑定仅有的有效 `ClientCredentialType` 为 `Certificate`。</span><span class="sxs-lookup"><span data-stu-id="9fe77-130">The only valid `ClientCredentialType` for this binding is `Certificate`.</span></span>|
|<span data-ttu-id="9fe77-131">TransportWithMessageCredential</span><span class="sxs-lookup"><span data-stu-id="9fe77-131">TransportWithMessageCredential</span></span>|<span data-ttu-id="9fe77-132">完整性、保密性和服务器身份验证由传输安全来提供。</span><span class="sxs-lookup"><span data-stu-id="9fe77-132">Integrity, confidentiality and server authentication are provided by transport security.</span></span> <span data-ttu-id="9fe77-133">客户端身份验证采用 SOAP 消息安全方式提供。</span><span class="sxs-lookup"><span data-stu-id="9fe77-133">Client authentication is provided by means of SOAP message security.</span></span> <span data-ttu-id="9fe77-134">如果要使用用户名/密码对用户进行身份验证，并且存在用于保护消息传输的现有 HTTP 部署，则适用此模式。</span><span class="sxs-lookup"><span data-stu-id="9fe77-134">This mode is relevant when the user is authenticating using username/password and there is an existing HTTP deployment for securing message transfer.</span></span>|
|<span data-ttu-id="9fe77-135">TransportCredentialOnly</span><span class="sxs-lookup"><span data-stu-id="9fe77-135">TransportCredentialOnly</span></span>|<span data-ttu-id="9fe77-136">此模式并不提供消息的完整性和保密性，</span><span class="sxs-lookup"><span data-stu-id="9fe77-136">This mode does not provide message integrity and confidentiality.</span></span> <span data-ttu-id="9fe77-137">而是提供基于 http 的客户端身份验证。</span><span class="sxs-lookup"><span data-stu-id="9fe77-137">It provides http-based client authentication.</span></span> <span data-ttu-id="9fe77-138">使用此模式时应当小心。</span><span class="sxs-lookup"><span data-stu-id="9fe77-138">This mode should be used with caution.</span></span> <span data-ttu-id="9fe77-139">它应该用于通过其他 (方式（如 IPSec) ）提供传输安全的环境中，并且 WCF 基础结构只提供客户端身份验证。</span><span class="sxs-lookup"><span data-stu-id="9fe77-139">It should be used in environments where the transport security is being provided by other means (such as IPSec) and only client authentication is provided by the WCF infrastructure.</span></span>|

### <a name="child-elements"></a><span data-ttu-id="9fe77-140">子元素</span><span class="sxs-lookup"><span data-stu-id="9fe77-140">Child elements</span></span>

|<span data-ttu-id="9fe77-141">元素</span><span class="sxs-lookup"><span data-stu-id="9fe77-141">Element</span></span>|<span data-ttu-id="9fe77-142">说明</span><span class="sxs-lookup"><span data-stu-id="9fe77-142">Description</span></span>|
|-------------|-----------------|
|[\<transport>](transport-of-nethttpbinding.md)|<span data-ttu-id="9fe77-143">定义基本 HTTP 服务的传输安全设置。</span><span class="sxs-lookup"><span data-stu-id="9fe77-143">Defines the transport security settings for a basic HTTP service.</span></span> <span data-ttu-id="9fe77-144">此元素与 <xref:System.ServiceModel.HttpTransportSecurity> 相对应。</span><span class="sxs-lookup"><span data-stu-id="9fe77-144">This element corresponds to <xref:System.ServiceModel.HttpTransportSecurity>.</span></span>|
|[\<message>](message-of-nethttpbinding.md)|<span data-ttu-id="9fe77-145">定义基本 HTTP 服务的消息安全设置。</span><span class="sxs-lookup"><span data-stu-id="9fe77-145">Defines the message security settings for a basic HTTP service.</span></span> <span data-ttu-id="9fe77-146">此元素与 <xref:System.ServiceModel.BasicHttpMessageSecurity> 相对应。</span><span class="sxs-lookup"><span data-stu-id="9fe77-146">This element corresponds to <xref:System.ServiceModel.BasicHttpMessageSecurity>.</span></span>|

### <a name="parent-elements"></a><span data-ttu-id="9fe77-147">父元素</span><span class="sxs-lookup"><span data-stu-id="9fe77-147">Parent elements</span></span>

|<span data-ttu-id="9fe77-148">元素</span><span class="sxs-lookup"><span data-stu-id="9fe77-148">Element</span></span>|<span data-ttu-id="9fe77-149">说明</span><span class="sxs-lookup"><span data-stu-id="9fe77-149">Description</span></span>|
|-------------|-----------------|
|<span data-ttu-id="9fe77-150">binding</span><span class="sxs-lookup"><span data-stu-id="9fe77-150">binding</span></span>|<span data-ttu-id="9fe77-151">的绑定元素 [\<basicHttpBinding>](basichttpbinding.md) 。</span><span class="sxs-lookup"><span data-stu-id="9fe77-151">The binding element of the [\<basicHttpBinding>](basichttpbinding.md).</span></span>|

## <a name="remarks"></a><span data-ttu-id="9fe77-152">备注</span><span class="sxs-lookup"><span data-stu-id="9fe77-152">Remarks</span></span>

 <span data-ttu-id="9fe77-153">默认情况下，不会对 SOAP 消息进行保护，也不会对客户端进行身份验证。</span><span class="sxs-lookup"><span data-stu-id="9fe77-153">By default, the SOAP message is not secured and the client is not authenticated.</span></span> <span data-ttu-id="9fe77-154">使用此元素，您可以配置 `netHttpBinding` 元素的其他安全设置。</span><span class="sxs-lookup"><span data-stu-id="9fe77-154">This element enables you to configure additional security settings for the `netHttpBinding` element.</span></span>

## <a name="see-also"></a><span data-ttu-id="9fe77-155">请参阅</span><span class="sxs-lookup"><span data-stu-id="9fe77-155">See also</span></span>

- <xref:System.ServiceModel.NetHttpBinding.Security%2A>
- <xref:System.ServiceModel.Configuration.NetHttpBindingElement.Security%2A>  
- [<span data-ttu-id="9fe77-156">保护服务和客户端的安全</span><span class="sxs-lookup"><span data-stu-id="9fe77-156">Securing Services and Clients</span></span>](../../../wcf/feature-details/securing-services-and-clients.md)
- [<span data-ttu-id="9fe77-157">选择凭据类型</span><span class="sxs-lookup"><span data-stu-id="9fe77-157">Selecting a Credential Type</span></span>](../../../wcf/feature-details/selecting-a-credential-type.md)
- [<span data-ttu-id="9fe77-158">绑定</span><span class="sxs-lookup"><span data-stu-id="9fe77-158">Bindings</span></span>](../../../wcf/bindings.md)
- [<span data-ttu-id="9fe77-159">配置系统提供的绑定</span><span class="sxs-lookup"><span data-stu-id="9fe77-159">Configuring System-Provided Bindings</span></span>](../../../wcf/feature-details/configuring-system-provided-bindings.md)
- [<span data-ttu-id="9fe77-160">使用绑定配置服务和客户端</span><span class="sxs-lookup"><span data-stu-id="9fe77-160">Using Bindings to Configure Services and Clients</span></span>](../../../wcf/using-bindings-to-configure-services-and-clients.md)
- [\<binding>](bindings.md)
