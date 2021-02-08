---
description: 了解详细 <security> 信息： <netPeerBinding>
title: <security> 的 <netPeerBinding>
ms.date: 03/30/2017
ms.assetid: 1ef40d8c-f903-4426-9b08-da81462766d8
ms.openlocfilehash: f67cfa445a5a605b99783cfd67dd1bae6e17b51e
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99786832"
---
# <a name="security-of-netpeerbinding"></a><span data-ttu-id="f4c1e-103">\<security> 的 \<netPeerBinding></span><span class="sxs-lookup"><span data-stu-id="f4c1e-103">\<security> of \<netPeerBinding></span></span>

<span data-ttu-id="f4c1e-104">定义的安全设置 [\<netPeerTcpBinding>](netpeertcpbinding.md) ，包括使用的身份验证类型和用于消息传输的安全性。</span><span class="sxs-lookup"><span data-stu-id="f4c1e-104">Defines the security settings of the [\<netPeerTcpBinding>](netpeertcpbinding.md), including the type of authentication used and the security used for the message transport.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<bindings>**](bindings.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<netPeerTcpBinding>**](netpeertcpbinding.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<binding>**\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<security>**  
  
## <a name="syntax"></a><span data-ttu-id="f4c1e-105">语法</span><span class="sxs-lookup"><span data-stu-id="f4c1e-105">Syntax</span></span>  
  
```xml  
<netPeerBinding>
  <binding>
    <security mode="Message/None/Transport//TransportWithMessageCredential">
      <transport credentialType="Certificate/Password" />
    </security>
  </binding>
</netPeerBinding>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="f4c1e-106">特性和元素</span><span class="sxs-lookup"><span data-stu-id="f4c1e-106">Attributes and Elements</span></span>  

 <span data-ttu-id="f4c1e-107">以下几节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="f4c1e-107">The following sections describe attributes, child elements, and parent elements</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="f4c1e-108">特性</span><span class="sxs-lookup"><span data-stu-id="f4c1e-108">Attributes</span></span>  
  
|<span data-ttu-id="f4c1e-109">属性</span><span class="sxs-lookup"><span data-stu-id="f4c1e-109">Attribute</span></span>|<span data-ttu-id="f4c1e-110">说明</span><span class="sxs-lookup"><span data-stu-id="f4c1e-110">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="f4c1e-111">mode</span><span class="sxs-lookup"><span data-stu-id="f4c1e-111">mode</span></span>|<span data-ttu-id="f4c1e-112">可选。</span><span class="sxs-lookup"><span data-stu-id="f4c1e-112">Optional.</span></span> <span data-ttu-id="f4c1e-113">指定采用此绑定配置的对等端所使用的安全类型。</span><span class="sxs-lookup"><span data-stu-id="f4c1e-113">Specifies the type of security used by peers configured with this binding.</span></span> <span data-ttu-id="f4c1e-114">默认值是 `Message`。</span><span class="sxs-lookup"><span data-stu-id="f4c1e-114">The default value is `Message`.</span></span> <span data-ttu-id="f4c1e-115">此属性的类型为 <xref:System.ServiceModel.SecurityMode>。</span><span class="sxs-lookup"><span data-stu-id="f4c1e-115">This attribute is of type <xref:System.ServiceModel.SecurityMode>.</span></span>|  
  
## <a name="mode-attribute"></a><span data-ttu-id="f4c1e-116">mode 属性</span><span class="sxs-lookup"><span data-stu-id="f4c1e-116">mode Attribute</span></span>  
  
|<span data-ttu-id="f4c1e-117">值</span><span class="sxs-lookup"><span data-stu-id="f4c1e-117">Value</span></span>|<span data-ttu-id="f4c1e-118">说明</span><span class="sxs-lookup"><span data-stu-id="f4c1e-118">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="f4c1e-119">消息</span><span class="sxs-lookup"><span data-stu-id="f4c1e-119">Message</span></span>|<span data-ttu-id="f4c1e-120">SOAP 安全提供身份验证、完整性和保密性。</span><span class="sxs-lookup"><span data-stu-id="f4c1e-120">SOAP security provides authentication, integrity and confidentiality.</span></span>|  
|<span data-ttu-id="f4c1e-121">无</span><span class="sxs-lookup"><span data-stu-id="f4c1e-121">None</span></span>|<span data-ttu-id="f4c1e-122">禁用安全性。</span><span class="sxs-lookup"><span data-stu-id="f4c1e-122">Security is disabled.</span></span>|  
|<span data-ttu-id="f4c1e-123">Transport</span><span class="sxs-lookup"><span data-stu-id="f4c1e-123">Transport</span></span>|<span data-ttu-id="f4c1e-124">使用 HTTPS 提供安全性。</span><span class="sxs-lookup"><span data-stu-id="f4c1e-124">Security is provided using HTTPS.</span></span>|  
|<span data-ttu-id="f4c1e-125">TransportWithMessageCredential</span><span class="sxs-lookup"><span data-stu-id="f4c1e-125">TransportWithMessageCredential</span></span>|<span data-ttu-id="f4c1e-126">HTTPS 提供身份验证和保密性。</span><span class="sxs-lookup"><span data-stu-id="f4c1e-126">HTTPS provides authentication and confidentiality.</span></span> <span data-ttu-id="f4c1e-127">SOAP 消息提供丰富的凭据类型。</span><span class="sxs-lookup"><span data-stu-id="f4c1e-127">SOAP messages provide rich credential types.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="f4c1e-128">子元素</span><span class="sxs-lookup"><span data-stu-id="f4c1e-128">Child Elements</span></span>  
  
|<span data-ttu-id="f4c1e-129">元素</span><span class="sxs-lookup"><span data-stu-id="f4c1e-129">Element</span></span>|<span data-ttu-id="f4c1e-130">说明</span><span class="sxs-lookup"><span data-stu-id="f4c1e-130">Description</span></span>|  
|-------------|-----------------|  
|[\<transport>](transport-of-netpeertcpbinding.md)|<span data-ttu-id="f4c1e-131">定义采用此绑定配置的对等端所发送的安全消息的传输类型。</span><span class="sxs-lookup"><span data-stu-id="f4c1e-131">Defines the transport type for secured messages sent by peers configured with this binding.</span></span> <span data-ttu-id="f4c1e-132">此元素的类型为 <xref:System.ServiceModel.Configuration.PeerTransportSecurityElement>。</span><span class="sxs-lookup"><span data-stu-id="f4c1e-132">This element is of type <xref:System.ServiceModel.Configuration.PeerTransportSecurityElement>.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="f4c1e-133">父元素</span><span class="sxs-lookup"><span data-stu-id="f4c1e-133">Parent Elements</span></span>  
  
|<span data-ttu-id="f4c1e-134">元素</span><span class="sxs-lookup"><span data-stu-id="f4c1e-134">Element</span></span>|<span data-ttu-id="f4c1e-135">说明</span><span class="sxs-lookup"><span data-stu-id="f4c1e-135">Description</span></span>|  
|-------------|-----------------|  
|[\<binding>](bindings.md)|<span data-ttu-id="f4c1e-136">定义的所有绑定功能 [\<netPeerTcpBinding>](netpeertcpbinding.md) 。</span><span class="sxs-lookup"><span data-stu-id="f4c1e-136">Defines all binding capabilities of the [\<netPeerTcpBinding>](netpeertcpbinding.md).</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="f4c1e-137">备注</span><span class="sxs-lookup"><span data-stu-id="f4c1e-137">Remarks</span></span>  

 <span data-ttu-id="f4c1e-138">安全性可以是特定于消息的，也可以是特定于传输的。</span><span class="sxs-lookup"><span data-stu-id="f4c1e-138">Security can be either message- or transport-specific.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f4c1e-139">请参阅</span><span class="sxs-lookup"><span data-stu-id="f4c1e-139">See also</span></span>

- <xref:System.ServiceModel.Configuration.PeerSecurityElement>
- <xref:System.ServiceModel.NetPeerTcpBinding.Security%2A>
- <xref:System.ServiceModel.Configuration.NetPeerTcpBindingElement.Security%2A>
- <xref:System.ServiceModel.PeerSecuritySettings>
- [<span data-ttu-id="f4c1e-140">保护服务和客户端的安全</span><span class="sxs-lookup"><span data-stu-id="f4c1e-140">Securing Services and Clients</span></span>](../../../wcf/feature-details/securing-services-and-clients.md)
- [<span data-ttu-id="f4c1e-141">选择凭据类型</span><span class="sxs-lookup"><span data-stu-id="f4c1e-141">Selecting a Credential Type</span></span>](../../../wcf/feature-details/selecting-a-credential-type.md)
- [<span data-ttu-id="f4c1e-142">绑定</span><span class="sxs-lookup"><span data-stu-id="f4c1e-142">Bindings</span></span>](../../../wcf/bindings.md)
- [<span data-ttu-id="f4c1e-143">配置系统提供的绑定</span><span class="sxs-lookup"><span data-stu-id="f4c1e-143">Configuring System-Provided Bindings</span></span>](../../../wcf/feature-details/configuring-system-provided-bindings.md)
- [<span data-ttu-id="f4c1e-144">使用绑定配置服务和客户端</span><span class="sxs-lookup"><span data-stu-id="f4c1e-144">Using Bindings to Configure Services and Clients</span></span>](../../../wcf/using-bindings-to-configure-services-and-clients.md)
- [\<binding>](bindings.md)
