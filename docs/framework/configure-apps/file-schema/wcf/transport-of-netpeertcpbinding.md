---
description: 了解详细 <transport> 信息： <netPeerTcpBinding>
title: <transport> 的 <netPeerTcpBinding>
ms.date: 03/30/2017
ms.assetid: c44d86d2-1160-44d7-9c7a-297b12eccc7f
ms.openlocfilehash: e93885234577e4f3c7a99be66e4798d33ffb5893
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99664569"
---
# <a name="transport-of-netpeertcpbinding"></a><span data-ttu-id="ee3f8-103">\<transport> 的 \<netPeerTcpBinding></span><span class="sxs-lookup"><span data-stu-id="ee3f8-103">\<transport> of \<netPeerTcpBinding></span></span>

<span data-ttu-id="ee3f8-104">指定使用时的传输级安全性设置 [\<netPeerTcpBinding>](netpeertcpbinding.md) 。</span><span class="sxs-lookup"><span data-stu-id="ee3f8-104">Specifies settings for transport level security when using the [\<netPeerTcpBinding>](netpeertcpbinding.md).</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<bindings>**](bindings.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<netPeerTcpBinding>**](netpeertcpbinding.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<binding>**\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<security>**](security-of-netpeerbinding.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<transport>**  
  
## <a name="syntax"></a><span data-ttu-id="ee3f8-105">语法</span><span class="sxs-lookup"><span data-stu-id="ee3f8-105">Syntax</span></span>  
  
```xml  
<netPeerTcpBinding>
  <binding>
    <security>
      <transport credentialType="Certificate/Password" />
    </security>
  </binding>
</netPeerTcpBinding>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="ee3f8-106">特性和元素</span><span class="sxs-lookup"><span data-stu-id="ee3f8-106">Attributes and Elements</span></span>  

 <span data-ttu-id="ee3f8-107">以下几节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="ee3f8-107">The following sections describe attributes, child elements, and parent elements</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="ee3f8-108">特性</span><span class="sxs-lookup"><span data-stu-id="ee3f8-108">Attributes</span></span>  
  
|<span data-ttu-id="ee3f8-109">属性</span><span class="sxs-lookup"><span data-stu-id="ee3f8-109">Attribute</span></span>|<span data-ttu-id="ee3f8-110">说明</span><span class="sxs-lookup"><span data-stu-id="ee3f8-110">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="ee3f8-111">credentialType</span><span class="sxs-lookup"><span data-stu-id="ee3f8-111">credentialType</span></span>|<span data-ttu-id="ee3f8-112">可选。</span><span class="sxs-lookup"><span data-stu-id="ee3f8-112">Optional.</span></span> <span data-ttu-id="ee3f8-113">指定用于验证通过对等传输发送的消息的凭据的类型。</span><span class="sxs-lookup"><span data-stu-id="ee3f8-113">Specifies the type of credentials used to verify messages sent with the peer transport.</span></span> <span data-ttu-id="ee3f8-114">此属性的类型为 <xref:System.ServiceModel.PeerTransportCredentialType>。</span><span class="sxs-lookup"><span data-stu-id="ee3f8-114">This attribute is of type <xref:System.ServiceModel.PeerTransportCredentialType>.</span></span>|  
  
## <a name="credentialtype-attribute"></a><span data-ttu-id="ee3f8-115">credentialType 属性</span><span class="sxs-lookup"><span data-stu-id="ee3f8-115">credentialType Attribute</span></span>  
  
|<span data-ttu-id="ee3f8-116">值</span><span class="sxs-lookup"><span data-stu-id="ee3f8-116">Value</span></span>|<span data-ttu-id="ee3f8-117">说明</span><span class="sxs-lookup"><span data-stu-id="ee3f8-117">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="ee3f8-118">证书</span><span class="sxs-lookup"><span data-stu-id="ee3f8-118">Certificate</span></span>|<span data-ttu-id="ee3f8-119">对等通道传输的身份验证需要 X509 证书。</span><span class="sxs-lookup"><span data-stu-id="ee3f8-119">Authentication of the peer channel transport requires an X509 certificate.</span></span>|  
|<span data-ttu-id="ee3f8-120">密码</span><span class="sxs-lookup"><span data-stu-id="ee3f8-120">Password</span></span>|<span data-ttu-id="ee3f8-121">对等通道传输的身份验证需要正确的密码。</span><span class="sxs-lookup"><span data-stu-id="ee3f8-121">Authentication of the peer channel transport requires a correct password.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="ee3f8-122">子元素</span><span class="sxs-lookup"><span data-stu-id="ee3f8-122">Child Elements</span></span>  

 <span data-ttu-id="ee3f8-123">无</span><span class="sxs-lookup"><span data-stu-id="ee3f8-123">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="ee3f8-124">父元素</span><span class="sxs-lookup"><span data-stu-id="ee3f8-124">Parent Elements</span></span>  
  
|<span data-ttu-id="ee3f8-125">元素</span><span class="sxs-lookup"><span data-stu-id="ee3f8-125">Element</span></span>|<span data-ttu-id="ee3f8-126">说明</span><span class="sxs-lookup"><span data-stu-id="ee3f8-126">Description</span></span>|  
|-------------|-----------------|  
|[\<security>](security-of-netpeerbinding.md)|<span data-ttu-id="ee3f8-127">定义的安全设置 [\<netPeerTcpBinding>](netpeertcpbinding.md) 。</span><span class="sxs-lookup"><span data-stu-id="ee3f8-127">Defines the security settings for the [\<netPeerTcpBinding>](netpeertcpbinding.md).</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="ee3f8-128">请参阅</span><span class="sxs-lookup"><span data-stu-id="ee3f8-128">See also</span></span>

- <xref:System.ServiceModel.Configuration.PeerTransportSecurityElement>
- <xref:System.ServiceModel.PeerSecuritySettings.Transport%2A>
- <xref:System.ServiceModel.Configuration.PeerSecurityElement.Transport%2A>
- <xref:System.ServiceModel.PeerTransportSecuritySettings>
- [<span data-ttu-id="ee3f8-129">保护服务和客户端的安全</span><span class="sxs-lookup"><span data-stu-id="ee3f8-129">Securing Services and Clients</span></span>](../../../wcf/feature-details/securing-services-and-clients.md)
- [<span data-ttu-id="ee3f8-130">绑定</span><span class="sxs-lookup"><span data-stu-id="ee3f8-130">Bindings</span></span>](../../../wcf/bindings.md)
- [<span data-ttu-id="ee3f8-131">配置系统提供的绑定</span><span class="sxs-lookup"><span data-stu-id="ee3f8-131">Configuring System-Provided Bindings</span></span>](../../../wcf/feature-details/configuring-system-provided-bindings.md)
- [<span data-ttu-id="ee3f8-132">使用绑定配置服务和客户端</span><span class="sxs-lookup"><span data-stu-id="ee3f8-132">Using Bindings to Configure Services and Clients</span></span>](../../../wcf/using-bindings-to-configure-services-and-clients.md)
- [\<binding>](bindings.md)
