---
description: 了解详细 <security> 信息： <webHttpBinding>
title: <security> 的 <webHttpBinding>
ms.date: 03/30/2017
ms.assetid: 727cf3d2-6f56-48ad-a59f-ba423edb9c83
ms.openlocfilehash: a80a919ef877f01503e5ceaeb4fe7432e46f288c
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99683042"
---
# <a name="security-of-webhttpbinding"></a><span data-ttu-id="2d619-103">\<security> 的 \<webHttpBinding></span><span class="sxs-lookup"><span data-stu-id="2d619-103">\<security> of \<webHttpBinding></span></span>

<span data-ttu-id="2d619-104">指定用配置的终结点的安全要求 [\<webHttpBinding>](webhttpbinding.md) 。</span><span class="sxs-lookup"><span data-stu-id="2d619-104">Specifies the security requirements for an endpoint configured with a [\<webHttpBinding>](webhttpbinding.md).</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<bindings>**](bindings.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<webHttpBinding>**](webhttpbinding.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<binding>**\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<security>**  
  
## <a name="syntax"></a><span data-ttu-id="2d619-105">语法</span><span class="sxs-lookup"><span data-stu-id="2d619-105">Syntax</span></span>  
  
```xml  
<system.ServiceModel>
  <bindings>
    <webHttpBinding>
      <binding name = "String">
        <security mode="None/Transport/TransportCredentialOnly">
          <transport clientCredentialType="Basic/Certificate/Digest/None/Ntlm/Windows"
                     proxyCredentialType="Basic/Digest/None/Ntlm/Windows"
                     realm="String" />
        </security>
      </binding>
    </webHttpBinding>
  </bindings>
</system.ServiceModel>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="2d619-106">特性和元素</span><span class="sxs-lookup"><span data-stu-id="2d619-106">Attributes and Elements</span></span>  

 <span data-ttu-id="2d619-107">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="2d619-107">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="2d619-108">特性</span><span class="sxs-lookup"><span data-stu-id="2d619-108">Attributes</span></span>  
  
|<span data-ttu-id="2d619-109">属性</span><span class="sxs-lookup"><span data-stu-id="2d619-109">Attribute</span></span>|<span data-ttu-id="2d619-110">说明</span><span class="sxs-lookup"><span data-stu-id="2d619-110">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="2d619-111">mode</span><span class="sxs-lookup"><span data-stu-id="2d619-111">mode</span></span>|<span data-ttu-id="2d619-112">指定终结点是使用传输级安全模式还是不使用安全模式。</span><span class="sxs-lookup"><span data-stu-id="2d619-112">Specifies whether transport-level security or no security is used by an endpoint.</span></span> <span data-ttu-id="2d619-113">默认值为 `None`。</span><span class="sxs-lookup"><span data-stu-id="2d619-113">The default is `None`.</span></span> <span data-ttu-id="2d619-114">此属性的类型为 <xref:System.ServiceModel.WebHttpSecurityMode>。</span><span class="sxs-lookup"><span data-stu-id="2d619-114">This attribute is of type <xref:System.ServiceModel.WebHttpSecurityMode>.</span></span>|  
  
## <a name="mode-attribute"></a><span data-ttu-id="2d619-115">Mode 属性</span><span class="sxs-lookup"><span data-stu-id="2d619-115">Mode Attribute</span></span>  
  
|<span data-ttu-id="2d619-116">值</span><span class="sxs-lookup"><span data-stu-id="2d619-116">Value</span></span>|<span data-ttu-id="2d619-117">说明</span><span class="sxs-lookup"><span data-stu-id="2d619-117">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="2d619-118">无</span><span class="sxs-lookup"><span data-stu-id="2d619-118">None</span></span>|<span data-ttu-id="2d619-119">禁用安全性。</span><span class="sxs-lookup"><span data-stu-id="2d619-119">Security is disabled.</span></span>|  
|<span data-ttu-id="2d619-120">Transport</span><span class="sxs-lookup"><span data-stu-id="2d619-120">Transport</span></span>|<span data-ttu-id="2d619-121">使用 HTTPS 提供安全性。</span><span class="sxs-lookup"><span data-stu-id="2d619-121">Security is provided using HTTPS.</span></span> <span data-ttu-id="2d619-122">此服务需要使用 SSL 证书进行配置。</span><span class="sxs-lookup"><span data-stu-id="2d619-122">The service needs to be configured with SSL certificates.</span></span> <span data-ttu-id="2d619-123">消息使用 HTTPS 获得全面保护，而且客户端使用服务的 SSL 证书对服务进行身份验证。</span><span class="sxs-lookup"><span data-stu-id="2d619-123">The message is entirely secured using HTTPS and the service is authenticated by the client using the service’s SSL certificate.</span></span> <span data-ttu-id="2d619-124">客户端身份验证通过 `ClientCredentialType` 的属性进行控制 [\<transport>](transport-of-webhttpbinding.md) 。</span><span class="sxs-lookup"><span data-stu-id="2d619-124">The client authentication is controlled through the `ClientCredentialType` attribute of the [\<transport>](transport-of-webhttpbinding.md).</span></span>|  
|<span data-ttu-id="2d619-125">TransportCredentialOnly</span><span class="sxs-lookup"><span data-stu-id="2d619-125">TransportCredentialOnly</span></span>|<span data-ttu-id="2d619-126">此模式并不提供消息的完整性和保密性，</span><span class="sxs-lookup"><span data-stu-id="2d619-126">This mode does not provide message integrity and confidentiality.</span></span> <span data-ttu-id="2d619-127">而是提供基于 HTTP 的客户端身份验证。</span><span class="sxs-lookup"><span data-stu-id="2d619-127">It provides HTTP-based client authentication.</span></span> <span data-ttu-id="2d619-128">使用此模式时应当小心。</span><span class="sxs-lookup"><span data-stu-id="2d619-128">This mode should be used with caution.</span></span> <span data-ttu-id="2d619-129">它应该用于通过其他 (方式（如 IPSec) ）提供传输安全的环境中，并且 WCF 基础结构只提供客户端身份验证。</span><span class="sxs-lookup"><span data-stu-id="2d619-129">It should be used in environments where the transport security is being provided by other means (such as IPSec) and only client authentication is provided by the WCF infrastructure.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="2d619-130">子元素</span><span class="sxs-lookup"><span data-stu-id="2d619-130">Child Elements</span></span>  
  
|<span data-ttu-id="2d619-131">元素</span><span class="sxs-lookup"><span data-stu-id="2d619-131">Element</span></span>|<span data-ttu-id="2d619-132">说明</span><span class="sxs-lookup"><span data-stu-id="2d619-132">Description</span></span>|  
|-------------|-----------------|  
|[\<transport>](transport-of-webhttpbinding.md)|<span data-ttu-id="2d619-133">定义传输安全设置。</span><span class="sxs-lookup"><span data-stu-id="2d619-133">Defines the transport security settings.</span></span> <span data-ttu-id="2d619-134">此元素与 <xref:System.ServiceModel.Configuration.HttpTransportSecurityElement> 类型相对应。</span><span class="sxs-lookup"><span data-stu-id="2d619-134">This element corresponds to the <xref:System.ServiceModel.Configuration.HttpTransportSecurityElement> type.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="2d619-135">父元素</span><span class="sxs-lookup"><span data-stu-id="2d619-135">Parent Elements</span></span>  
  
|<span data-ttu-id="2d619-136">元素</span><span class="sxs-lookup"><span data-stu-id="2d619-136">Element</span></span>|<span data-ttu-id="2d619-137">说明</span><span class="sxs-lookup"><span data-stu-id="2d619-137">Description</span></span>|  
|-------------|-----------------|  
|[\<webHttpBinding>](webhttpbinding.md)|<span data-ttu-id="2d619-138">一个绑定元素，用于为响应 HTTP 请求（而不是 SOAP 消息）的 Windows Communication Foundation (WCF) Web 服务配置终结点。</span><span class="sxs-lookup"><span data-stu-id="2d619-138">A binding element that is used to configure endpoints for Windows Communication Foundation (WCF) Web services that respond to HTTP requests instead of SOAP messages.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="2d619-139">请参阅</span><span class="sxs-lookup"><span data-stu-id="2d619-139">See also</span></span>

- <xref:System.ServiceModel.Configuration.WebHttpBindingElement>
- <xref:System.ServiceModel.Configuration.WSHttpSecurityElement>
- <xref:System.ServiceModel.WebHttpBinding.Security%2A>
- <xref:System.ServiceModel.Configuration.WebHttpBindingElement.Security%2A>
- <xref:System.ServiceModel.WebHttpSecurity>
- [<span data-ttu-id="2d619-140">保护服务和客户端的安全</span><span class="sxs-lookup"><span data-stu-id="2d619-140">Securing Services and Clients</span></span>](../../../wcf/feature-details/securing-services-and-clients.md)
- [<span data-ttu-id="2d619-141">选择凭据类型</span><span class="sxs-lookup"><span data-stu-id="2d619-141">Selecting a Credential Type</span></span>](../../../wcf/feature-details/selecting-a-credential-type.md)
- [<span data-ttu-id="2d619-142">绑定</span><span class="sxs-lookup"><span data-stu-id="2d619-142">Bindings</span></span>](../../../wcf/bindings.md)
- [<span data-ttu-id="2d619-143">配置系统提供的绑定</span><span class="sxs-lookup"><span data-stu-id="2d619-143">Configuring System-Provided Bindings</span></span>](../../../wcf/feature-details/configuring-system-provided-bindings.md)
- [<span data-ttu-id="2d619-144">使用绑定配置服务和客户端</span><span class="sxs-lookup"><span data-stu-id="2d619-144">Using Bindings to Configure Services and Clients</span></span>](../../../wcf/using-bindings-to-configure-services-and-clients.md)
- [\<binding>](bindings.md)
- [<span data-ttu-id="2d619-145">WCF Web HTTP 编程模型</span><span class="sxs-lookup"><span data-stu-id="2d619-145">WCF Web HTTP Programming Model</span></span>](../../../wcf/feature-details/wcf-web-http-programming-model.md)
