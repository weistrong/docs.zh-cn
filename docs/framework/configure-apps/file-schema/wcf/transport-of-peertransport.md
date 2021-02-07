---
description: 了解详细 <transport> 信息： <peerTransport>
title: <transport> 的 <peerTransport>
ms.date: 03/30/2017
ms.assetid: d7116240-845c-4b6f-b203-262de6b597ef
ms.openlocfilehash: ba3405c5dfadb513f92ebd537409a3f7b12fa291
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99664504"
---
# <a name="transport-of-peertransport"></a><span data-ttu-id="fc218-103">\<transport> 的 \<peerTransport></span><span class="sxs-lookup"><span data-stu-id="fc218-103">\<transport> of \<peerTransport></span></span>

<span data-ttu-id="fc218-104">指定采用此绑定配置的对等方所发送的安全消息的传输类型。</span><span class="sxs-lookup"><span data-stu-id="fc218-104">Specifies the transport type for secured messages sent by peers configured with this binding.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<bindings>**](bindings.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<customBinding>**](custombinding.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<binding>**\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<peerTransport>**](peertransport.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<security>**](security-of-peertransport.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<transport>**  
  
## <a name="syntax"></a><span data-ttu-id="fc218-105">语法</span><span class="sxs-lookup"><span data-stu-id="fc218-105">Syntax</span></span>  
  
```xml  
<security>
  <transport credentialType="Certificate/Password" />
</security>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="fc218-106">特性和元素</span><span class="sxs-lookup"><span data-stu-id="fc218-106">Attributes and Elements</span></span>  

 <span data-ttu-id="fc218-107">以下几节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="fc218-107">The following sections describe attributes, child elements, and parent elements</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="fc218-108">特性</span><span class="sxs-lookup"><span data-stu-id="fc218-108">Attributes</span></span>  
  
|<span data-ttu-id="fc218-109">属性</span><span class="sxs-lookup"><span data-stu-id="fc218-109">Attribute</span></span>|<span data-ttu-id="fc218-110">说明</span><span class="sxs-lookup"><span data-stu-id="fc218-110">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="fc218-111">credentialType</span><span class="sxs-lookup"><span data-stu-id="fc218-111">credentialType</span></span>|<span data-ttu-id="fc218-112">可选。</span><span class="sxs-lookup"><span data-stu-id="fc218-112">Optional.</span></span> <span data-ttu-id="fc218-113">指定用于验证通过对等传输发送的消息的凭据的类型。</span><span class="sxs-lookup"><span data-stu-id="fc218-113">Specifies the type of credentials used to verify messages sent with the peer transport.</span></span> <span data-ttu-id="fc218-114">此属性的类型为 <xref:System.ServiceModel.PeerTransportCredentialType>。</span><span class="sxs-lookup"><span data-stu-id="fc218-114">This attribute is of type <xref:System.ServiceModel.PeerTransportCredentialType>.</span></span>|  
  
## <a name="credentialtype-attribute"></a><span data-ttu-id="fc218-115">credentialType 属性</span><span class="sxs-lookup"><span data-stu-id="fc218-115">credentialType Attribute</span></span>  
  
|<span data-ttu-id="fc218-116">值</span><span class="sxs-lookup"><span data-stu-id="fc218-116">Value</span></span>|<span data-ttu-id="fc218-117">说明</span><span class="sxs-lookup"><span data-stu-id="fc218-117">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="fc218-118">证书</span><span class="sxs-lookup"><span data-stu-id="fc218-118">Certificate</span></span>|<span data-ttu-id="fc218-119">对等通道传输的身份验证需要 X509 证书。</span><span class="sxs-lookup"><span data-stu-id="fc218-119">Authentication of the peer channel transport requires an X509 certificate.</span></span>|  
|<span data-ttu-id="fc218-120">密码</span><span class="sxs-lookup"><span data-stu-id="fc218-120">Password</span></span>|<span data-ttu-id="fc218-121">对等通道传输的身份验证需要正确的密码。</span><span class="sxs-lookup"><span data-stu-id="fc218-121">Authentication of the peer channel transport requires a correct password.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="fc218-122">子元素</span><span class="sxs-lookup"><span data-stu-id="fc218-122">Child Elements</span></span>  

 <span data-ttu-id="fc218-123">无</span><span class="sxs-lookup"><span data-stu-id="fc218-123">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="fc218-124">父元素</span><span class="sxs-lookup"><span data-stu-id="fc218-124">Parent Elements</span></span>  
  
|<span data-ttu-id="fc218-125">元素</span><span class="sxs-lookup"><span data-stu-id="fc218-125">Element</span></span>|<span data-ttu-id="fc218-126">说明</span><span class="sxs-lookup"><span data-stu-id="fc218-126">Description</span></span>|  
|-------------|-----------------|  
|[\<security>](security-of-peertransport.md)|<span data-ttu-id="fc218-127">定义对等传输的安全设置。</span><span class="sxs-lookup"><span data-stu-id="fc218-127">Defines the security settings for a peer transport.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="fc218-128">备注</span><span class="sxs-lookup"><span data-stu-id="fc218-128">Remarks</span></span>  

 <span data-ttu-id="fc218-129">仅当的 mode 属性设置为或时，才设置此元素 [\<security>](security-of-peertransport.md) `Transport` `TransportWithMessageCredential` 。</span><span class="sxs-lookup"><span data-stu-id="fc218-129">This element is set only if the mode attribute of [\<security>](security-of-peertransport.md) is set to `Transport` or `TransportWithMessageCredential`.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="fc218-130">请参阅</span><span class="sxs-lookup"><span data-stu-id="fc218-130">See also</span></span>

- <xref:System.ServiceModel.Configuration.PeerTransportSecurityElement>
- <xref:System.ServiceModel.PeerSecuritySettings.Transport%2A>
- <xref:System.ServiceModel.PeerTransportSecuritySettings>
- <xref:System.ServiceModel.Channels.CustomBinding>
- [<span data-ttu-id="fc218-131">传输安全</span><span class="sxs-lookup"><span data-stu-id="fc218-131">Transport Security</span></span>](../../../wcf/feature-details/transport-security.md)
- [<span data-ttu-id="fc218-132">传输</span><span class="sxs-lookup"><span data-stu-id="fc218-132">Transports</span></span>](../../../wcf/feature-details/transports.md)
- [<span data-ttu-id="fc218-133">选择传输方式</span><span class="sxs-lookup"><span data-stu-id="fc218-133">Choosing a Transport</span></span>](../../../wcf/feature-details/choosing-a-transport.md)
- [<span data-ttu-id="fc218-134">绑定</span><span class="sxs-lookup"><span data-stu-id="fc218-134">Bindings</span></span>](../../../wcf/bindings.md)
- [<span data-ttu-id="fc218-135">扩展绑定</span><span class="sxs-lookup"><span data-stu-id="fc218-135">Extending Bindings</span></span>](../../../wcf/extending/extending-bindings.md)
- [<span data-ttu-id="fc218-136">自定义绑定</span><span class="sxs-lookup"><span data-stu-id="fc218-136">Custom Bindings</span></span>](../../../wcf/extending/custom-bindings.md)
- [\<customBinding>](custombinding.md)
