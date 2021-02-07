---
description: 了解有关 <peer> 元素的详细 <clientCredentials> 信息
title: <peer> of <clientCredentials> 元素
ms.date: 03/30/2017
ms.assetid: 505bd987-0042-4622-b68e-94f439729d53
ms.openlocfilehash: 1ff9386ba51dcf6bab6df71bd345cdaa59f18e3a
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99683783"
---
# <a name="peer-of-clientcredentials-element"></a><span data-ttu-id="b331e-103">\<peer> of \<clientCredentials> 元素</span><span class="sxs-lookup"><span data-stu-id="b331e-103">\<peer> of \<clientCredentials> Element</span></span>

<span data-ttu-id="b331e-104">指定在向对等客户端进行身份验证时使用的凭据。</span><span class="sxs-lookup"><span data-stu-id="b331e-104">Specifies credentials used when authenticating peer-to-peer clients.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<behaviors>**](behaviors.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<endpointBehaviors>**](endpointbehaviors.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<behavior>**](behavior-of-endpointbehaviors.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<clientCredentials>**](clientcredentials.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<peer>**  
  
## <a name="syntax"></a><span data-ttu-id="b331e-105">语法</span><span class="sxs-lookup"><span data-stu-id="b331e-105">Syntax</span></span>  
  
```xml  
<peer>
  <certificate />
  <peerAuthentication />
  <messageSenderAuthentication />
</peer>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="b331e-106">特性和元素</span><span class="sxs-lookup"><span data-stu-id="b331e-106">Attributes and Elements</span></span>  

 <span data-ttu-id="b331e-107">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="b331e-107">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="b331e-108">特性</span><span class="sxs-lookup"><span data-stu-id="b331e-108">Attributes</span></span>  

 <span data-ttu-id="b331e-109">无。</span><span class="sxs-lookup"><span data-stu-id="b331e-109">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="b331e-110">子元素</span><span class="sxs-lookup"><span data-stu-id="b331e-110">Child Elements</span></span>  
  
|<span data-ttu-id="b331e-111">元素</span><span class="sxs-lookup"><span data-stu-id="b331e-111">Element</span></span>|<span data-ttu-id="b331e-112">说明</span><span class="sxs-lookup"><span data-stu-id="b331e-112">Description</span></span>|  
|-------------|-----------------|  
|[\<certificate>](certificate-element.md)|<span data-ttu-id="b331e-113">指定要用于为对等客户端的消息进行签名和加密的 X.509 证书。</span><span class="sxs-lookup"><span data-stu-id="b331e-113">Specifies an X.509 certificate to use for signing and encrypting messages for peer-to-peer clients.</span></span> <span data-ttu-id="b331e-114">.</span><span class="sxs-lookup"><span data-stu-id="b331e-114">.</span></span>|  
|[\<peerAuthentication>](peerauthentication-element.md)|<span data-ttu-id="b331e-115">指定用于对等客户端的身份验证选项。</span><span class="sxs-lookup"><span data-stu-id="b331e-115">Specifies authentication options for peer clients.</span></span>|  
|[\<messageSenderAuthentication>](messagesenderauthentication-element.md)|<span data-ttu-id="b331e-116">指定用于消息发送方的身份验证选项。</span><span class="sxs-lookup"><span data-stu-id="b331e-116">Specifies authentication options for message senders.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="b331e-117">父元素</span><span class="sxs-lookup"><span data-stu-id="b331e-117">Parent Elements</span></span>  
  
|<span data-ttu-id="b331e-118">元素</span><span class="sxs-lookup"><span data-stu-id="b331e-118">Element</span></span>|<span data-ttu-id="b331e-119">说明</span><span class="sxs-lookup"><span data-stu-id="b331e-119">Description</span></span>|  
|-------------|-----------------|  
|[\<clientCredentials>](clientcredentials.md)|<span data-ttu-id="b331e-120">指定用于向服务验证客户端身份的凭据。</span><span class="sxs-lookup"><span data-stu-id="b331e-120">Specifies the credentials used to authenticate a client to a service.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="b331e-121">备注</span><span class="sxs-lookup"><span data-stu-id="b331e-121">Remarks</span></span>  

 <span data-ttu-id="b331e-122">此配置元素指定对等节点用于向网格中的其他节点证明它自己的身份的凭据，以及对等节点用于验证其他对等节点的身份的身份验证设置。</span><span class="sxs-lookup"><span data-stu-id="b331e-122">This configuration element specifies the credentials that a peer node uses to authenticate itself to other nodes in the mesh, as well as authentication settings that a peer node uses to authenticate other peer nodes.</span></span> <span data-ttu-id="b331e-123">有关详细信息，请参阅 [对等通道消息身份验证](/previous-versions/dotnet/netframework-3.5/aa967730(v=vs.90)) 和 [保护对等通道应用程序](../../../wcf/feature-details/securing-peer-channel-applications.md)。</span><span class="sxs-lookup"><span data-stu-id="b331e-123">For more information, see [Peer Channel Message Authentication](/previous-versions/dotnet/netframework-3.5/aa967730(v=vs.90)) and [Securing Peer Channel Applications](../../../wcf/feature-details/securing-peer-channel-applications.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b331e-124">请参阅</span><span class="sxs-lookup"><span data-stu-id="b331e-124">See also</span></span>

- <xref:System.ServiceModel.Configuration.ClientCredentialsElement>
- <xref:System.ServiceModel.Description.ClientCredentials>
- <xref:System.ServiceModel.Configuration.PeerCredentialElement>
- <xref:System.ServiceModel.Configuration.ClientCredentialsElement.Peer%2A>
- <xref:System.ServiceModel.Description.ClientCredentials>
- <xref:System.ServiceModel.Description.ClientCredentials.Peer%2A>
- <xref:System.ServiceModel.Security.PeerCredential>
- [<span data-ttu-id="b331e-125">对等网络</span><span class="sxs-lookup"><span data-stu-id="b331e-125">Peer-to-Peer Networking</span></span>](../../../wcf/feature-details/peer-to-peer-networking.md)
- [<span data-ttu-id="b331e-126">保证客户端的安全</span><span class="sxs-lookup"><span data-stu-id="b331e-126">Securing Clients</span></span>](../../../wcf/securing-clients.md)
- <span data-ttu-id="b331e-127">[对等通道消息身份验证](/previous-versions/dotnet/netframework-3.5/aa967730(v=vs.90))</span><span class="sxs-lookup"><span data-stu-id="b331e-127">[Peer Channel Message Authentication](/previous-versions/dotnet/netframework-3.5/aa967730(v=vs.90))</span></span>
- <span data-ttu-id="b331e-128">[对等通道自定义身份验证](/previous-versions/dotnet/netframework-3.5/ms751447(v=vs.90))</span><span class="sxs-lookup"><span data-stu-id="b331e-128">[Peer Channel Custom Authentication](/previous-versions/dotnet/netframework-3.5/ms751447(v=vs.90))</span></span>
- [<span data-ttu-id="b331e-129">保护对等通道应用程序</span><span class="sxs-lookup"><span data-stu-id="b331e-129">Securing Peer Channel Applications</span></span>](../../../wcf/feature-details/securing-peer-channel-applications.md)
- [<span data-ttu-id="b331e-130">保护服务和客户端的安全</span><span class="sxs-lookup"><span data-stu-id="b331e-130">Securing Services and Clients</span></span>](../../../wcf/feature-details/securing-services-and-clients.md)
