---
description: 了解详细 <peer> 信息： <serviceCredentials>
title: <peer> 的 <serviceCredentials>
ms.date: 03/30/2017
ms.assetid: b134e21d-e5b5-458e-9309-626dbf8db4ed
ms.openlocfilehash: 4d959f5061bb8069623b277219576dbd77ea52c3
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99683731"
---
# <a name="peer-of-servicecredentials"></a><span data-ttu-id="47240-103">\<peer> 的 \<serviceCredentials></span><span class="sxs-lookup"><span data-stu-id="47240-103">\<peer> of \<serviceCredentials></span></span>

<span data-ttu-id="47240-104">指定对等节点的当前凭据。</span><span class="sxs-lookup"><span data-stu-id="47240-104">Specifies the current credentials for a peer node.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<behaviors>**](behaviors.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<serviceBehaviors>**](servicebehaviors.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<behavior>**](behavior-of-servicebehaviors.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<serviceCredentials>**](servicecredentials.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<peer>**  
  
## <a name="syntax"></a><span data-ttu-id="47240-105">语法</span><span class="sxs-lookup"><span data-stu-id="47240-105">Syntax</span></span>  
  
```xml  
<peer>
  <certificate />
  <peerAuthentication />
  <messageSenderAuthentication />
</peer>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="47240-106">特性和元素</span><span class="sxs-lookup"><span data-stu-id="47240-106">Attributes and Elements</span></span>  

 <span data-ttu-id="47240-107">以下几节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="47240-107">The following sections describe attributes, child elements, and parent elements</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="47240-108">特性</span><span class="sxs-lookup"><span data-stu-id="47240-108">Attributes</span></span>  

 <span data-ttu-id="47240-109">无。</span><span class="sxs-lookup"><span data-stu-id="47240-109">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="47240-110">子元素</span><span class="sxs-lookup"><span data-stu-id="47240-110">Child Elements</span></span>  
  
|<span data-ttu-id="47240-111">元素</span><span class="sxs-lookup"><span data-stu-id="47240-111">Element</span></span>|<span data-ttu-id="47240-112">说明</span><span class="sxs-lookup"><span data-stu-id="47240-112">Description</span></span>|  
|-------------|-----------------|  
|[\<certificate>](certificate-of-peer.md)|<span data-ttu-id="47240-113">指定要用于为对等服务的消息进行签名和加密的 X.509 证书。</span><span class="sxs-lookup"><span data-stu-id="47240-113">Specifies an X.509 certificate to use for signing and encrypting messages for peer-to-peer services.</span></span> <span data-ttu-id="47240-114">.</span><span class="sxs-lookup"><span data-stu-id="47240-114">.</span></span>|  
|[\<messageSenderAuthentication>](messagesenderauthentication.md)|<span data-ttu-id="47240-115">指定用于消息发送方的身份验证选项。</span><span class="sxs-lookup"><span data-stu-id="47240-115">Specifies authentication options for message senders.</span></span>|  
|[\<peerAuthentication>](peerauthentication.md)|<span data-ttu-id="47240-116">指定用于对等服务的身份验证选项。</span><span class="sxs-lookup"><span data-stu-id="47240-116">Specifies authentication options for peer services.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="47240-117">父元素</span><span class="sxs-lookup"><span data-stu-id="47240-117">Parent Elements</span></span>  
  
|<span data-ttu-id="47240-118">元素</span><span class="sxs-lookup"><span data-stu-id="47240-118">Element</span></span>|<span data-ttu-id="47240-119">说明</span><span class="sxs-lookup"><span data-stu-id="47240-119">Description</span></span>|  
|-------------|-----------------|  
|[\<serviceCredentials>](servicecredentials.md)|<span data-ttu-id="47240-120">指定要用于对服务进行身份验证的凭据以及与客户端凭据验证相关的设置。</span><span class="sxs-lookup"><span data-stu-id="47240-120">Specifies the credential to be used in authenticating the service, and the client credential validation-related settings.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="47240-121">请参阅</span><span class="sxs-lookup"><span data-stu-id="47240-121">See also</span></span>

- <xref:System.ServiceModel.Configuration.PeerCredentialElement>
- <xref:System.ServiceModel.Configuration.ServiceCredentialsElement.Peer%2A>
- <xref:System.ServiceModel.Description.ServiceCredentials.Peer%2A>
- <xref:System.ServiceModel.Security.PeerCredential>
- [<span data-ttu-id="47240-122">对等网络</span><span class="sxs-lookup"><span data-stu-id="47240-122">Peer-to-Peer Networking</span></span>](../../../wcf/feature-details/peer-to-peer-networking.md)
- <span data-ttu-id="47240-123">[对等通道消息身份验证](/previous-versions/dotnet/netframework-3.5/aa967730(v=vs.90))</span><span class="sxs-lookup"><span data-stu-id="47240-123">[Peer Channel Message Authentication](/previous-versions/dotnet/netframework-3.5/aa967730(v=vs.90))</span></span>
- <span data-ttu-id="47240-124">[对等通道自定义身份验证](/previous-versions/dotnet/netframework-3.5/ms751447(v=vs.90))</span><span class="sxs-lookup"><span data-stu-id="47240-124">[Peer Channel Custom Authentication](/previous-versions/dotnet/netframework-3.5/ms751447(v=vs.90))</span></span>
- [<span data-ttu-id="47240-125">保护对等通道应用程序</span><span class="sxs-lookup"><span data-stu-id="47240-125">Securing Peer Channel Applications</span></span>](../../../wcf/feature-details/securing-peer-channel-applications.md)
- [<span data-ttu-id="47240-126">保护服务和客户端的安全</span><span class="sxs-lookup"><span data-stu-id="47240-126">Securing Services and Clients</span></span>](../../../wcf/feature-details/securing-services-and-clients.md)
