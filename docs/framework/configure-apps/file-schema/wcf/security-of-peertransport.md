---
description: 了解详细 <security> 信息： <peerTransport>
title: <security> 的 <peerTransport>
ms.date: 03/30/2017
ms.assetid: f73634ed-f896-4968-bf74-5e5ac52d3b6b
ms.openlocfilehash: 592f886377a2d5f2008be900a9e7586385fb3782
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99786819"
---
# <a name="security-of-peertransport"></a><span data-ttu-id="917b1-103">\<security> 的 \<peerTransport></span><span class="sxs-lookup"><span data-stu-id="917b1-103">\<security> of \<peerTransport></span></span>

<span data-ttu-id="917b1-104">包含与对等通道相关的安全设置，包括使用的身份验证类型和用于消息传输的安全性。</span><span class="sxs-lookup"><span data-stu-id="917b1-104">Contains the security settings associated with a peer channel, including the type of authentication used and the security used for the message transport.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<bindings>**](bindings.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<customBinding>**](custombinding.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<binding>**\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<peerTransport>**](peertransport.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<security>**  
  
## <a name="syntax"></a><span data-ttu-id="917b1-105">语法</span><span class="sxs-lookup"><span data-stu-id="917b1-105">Syntax</span></span>  
  
```xml  
<security mode="None/Transport/Message/TransportWithMessageCredential">
  <transport clientCredentialType="None/Windows/UserName/Certificate/CardSpace" />
</security
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="917b1-106">特性和元素</span><span class="sxs-lookup"><span data-stu-id="917b1-106">Attributes and Elements</span></span>  

 <span data-ttu-id="917b1-107">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="917b1-107">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="917b1-108">特性</span><span class="sxs-lookup"><span data-stu-id="917b1-108">Attributes</span></span>  
  
|<span data-ttu-id="917b1-109">属性</span><span class="sxs-lookup"><span data-stu-id="917b1-109">Attribute</span></span>|<span data-ttu-id="917b1-110">说明</span><span class="sxs-lookup"><span data-stu-id="917b1-110">Description</span></span>|  
|---------------|-----------------|  
|`mode`|<span data-ttu-id="917b1-111">指定要应用的安全类型。</span><span class="sxs-lookup"><span data-stu-id="917b1-111">Specifies the type of security to be applied.</span></span> <span data-ttu-id="917b1-112">默认值为 Message。</span><span class="sxs-lookup"><span data-stu-id="917b1-112">The default value is Message.</span></span> <span data-ttu-id="917b1-113">此属性的类型为 <xref:System.ServiceModel.SecurityMode>。</span><span class="sxs-lookup"><span data-stu-id="917b1-113">This attribute is of type <xref:System.ServiceModel.SecurityMode>.</span></span>|  
  
## <a name="mode-attribute"></a><span data-ttu-id="917b1-114">mode 属性</span><span class="sxs-lookup"><span data-stu-id="917b1-114">mode Attribute</span></span>  
  
|<span data-ttu-id="917b1-115">值</span><span class="sxs-lookup"><span data-stu-id="917b1-115">Value</span></span>|<span data-ttu-id="917b1-116">说明</span><span class="sxs-lookup"><span data-stu-id="917b1-116">Description</span></span>|  
|-----------|-----------------|  
|`None`|<span data-ttu-id="917b1-117">禁用安全性。</span><span class="sxs-lookup"><span data-stu-id="917b1-117">Security is disabled.</span></span>|  
|`Transport`|<span data-ttu-id="917b1-118">使用 HTTPS 提供安全性。</span><span class="sxs-lookup"><span data-stu-id="917b1-118">Security is provided using HTTPS.</span></span>|  
|`Message`|<span data-ttu-id="917b1-119">SOAP 安全提供身份验证、完整性和保密性。</span><span class="sxs-lookup"><span data-stu-id="917b1-119">SOAP security provides authentication, integrity and confidentiality.</span></span>|  
|`TransportWithMessageCredential`|<span data-ttu-id="917b1-120">HTTPS 提供身份验证和保密性。</span><span class="sxs-lookup"><span data-stu-id="917b1-120">HTTPS provides authentication and confidentiality.</span></span> <span data-ttu-id="917b1-121">SOAP 消息提供丰富的凭据类型。</span><span class="sxs-lookup"><span data-stu-id="917b1-121">SOAP messages provide rich credential types.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="917b1-122">子元素</span><span class="sxs-lookup"><span data-stu-id="917b1-122">Child Elements</span></span>  
  
|<span data-ttu-id="917b1-123">元素</span><span class="sxs-lookup"><span data-stu-id="917b1-123">Element</span></span>|<span data-ttu-id="917b1-124">说明</span><span class="sxs-lookup"><span data-stu-id="917b1-124">Description</span></span>|  
|-------------|-----------------|  
|[\<transport>](transport-of-peertransport.md)|<span data-ttu-id="917b1-125">定义自定义绑定的对等传输。</span><span class="sxs-lookup"><span data-stu-id="917b1-125">Defines a peer transport for a custom binding.</span></span> <span data-ttu-id="917b1-126">此元素具有一个 `clientCredentialType` 属性，可指定与服务进行交互时要使用的凭据。</span><span class="sxs-lookup"><span data-stu-id="917b1-126">This element has a `clientCredentialType` attribute that specifies the credentials to be used when interacting with a service.</span></span> <span data-ttu-id="917b1-127">此属性的类型为 <xref:System.ServiceModel.PeerTransportCredentialType>。</span><span class="sxs-lookup"><span data-stu-id="917b1-127">This attribute is of type <xref:System.ServiceModel.PeerTransportCredentialType>.</span></span><br /><br /> <span data-ttu-id="917b1-128">此元素的类型为 <xref:System.ServiceModel.Configuration.PeerTransportSecurityElement>。</span><span class="sxs-lookup"><span data-stu-id="917b1-128">This element is of type <xref:System.ServiceModel.Configuration.PeerTransportSecurityElement>.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="917b1-129">父元素</span><span class="sxs-lookup"><span data-stu-id="917b1-129">Parent Elements</span></span>  
  
|<span data-ttu-id="917b1-130">元素</span><span class="sxs-lookup"><span data-stu-id="917b1-130">Element</span></span>|<span data-ttu-id="917b1-131">说明</span><span class="sxs-lookup"><span data-stu-id="917b1-131">Description</span></span>|  
|-------------|-----------------|  
|[\<peerTransport>](peertransport.md)|<span data-ttu-id="917b1-132">定义自定义绑定的对等传输。</span><span class="sxs-lookup"><span data-stu-id="917b1-132">Defines a peer transport for a custom binding.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="917b1-133">请参阅</span><span class="sxs-lookup"><span data-stu-id="917b1-133">See also</span></span>

- <xref:System.ServiceModel.Configuration.PeerSecurityElement>
- <xref:System.ServiceModel.PeerSecuritySettings>
- <xref:System.ServiceModel.Channels.CustomBinding>
- [<span data-ttu-id="917b1-134">传输安全</span><span class="sxs-lookup"><span data-stu-id="917b1-134">Transport Security</span></span>](../../../wcf/feature-details/transport-security.md)
- [<span data-ttu-id="917b1-135">传输</span><span class="sxs-lookup"><span data-stu-id="917b1-135">Transports</span></span>](../../../wcf/feature-details/transports.md)
- [<span data-ttu-id="917b1-136">选择传输方式</span><span class="sxs-lookup"><span data-stu-id="917b1-136">Choosing a Transport</span></span>](../../../wcf/feature-details/choosing-a-transport.md)
- [<span data-ttu-id="917b1-137">绑定</span><span class="sxs-lookup"><span data-stu-id="917b1-137">Bindings</span></span>](../../../wcf/bindings.md)
- [<span data-ttu-id="917b1-138">扩展绑定</span><span class="sxs-lookup"><span data-stu-id="917b1-138">Extending Bindings</span></span>](../../../wcf/extending/extending-bindings.md)
- [<span data-ttu-id="917b1-139">自定义绑定</span><span class="sxs-lookup"><span data-stu-id="917b1-139">Custom Bindings</span></span>](../../../wcf/extending/custom-bindings.md)
- [\<customBinding>](custombinding.md)
