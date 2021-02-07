---
description: 了解详细 <add> 信息： <issuerChannelBehaviors>
title: <add> 的 <issuerChannelBehaviors>
ms.date: 03/30/2017
ms.assetid: 50710506-e28f-45dd-ab7e-bff6f44173db
ms.openlocfilehash: ccd8ba015b7a6837c74ce2c051a794d36ce8ceaa
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99750294"
---
# <a name="add-of-issuerchannelbehaviors"></a><span data-ttu-id="bdb9e-103">\<add> 的 \<issuerChannelBehaviors></span><span class="sxs-lookup"><span data-stu-id="bdb9e-103">\<add> of \<issuerChannelBehaviors></span></span>

<span data-ttu-id="bdb9e-104">添加在与 STS 进行通信时要使用的终结点行为。</span><span class="sxs-lookup"><span data-stu-id="bdb9e-104">Adds an endpoint behavior to be used when communicating with an STS.</span></span>

> [!NOTE]
> <span data-ttu-id="bdb9e-105">如果任何终结点行为包含 [\<clientCredentials>](clientcredentials.md) 元素，则会引发异常。</span><span class="sxs-lookup"><span data-stu-id="bdb9e-105">If any endpoint behavior contains a [\<clientCredentials>](clientcredentials.md) element, an exception will be thrown.</span></span>

[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<behaviors>**](behaviors.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<endpointBehaviors>**](endpointbehaviors.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<behavior>**](behavior-of-endpointbehaviors.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<clientCredentials>**](clientcredentials.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<issuedToken>**](issuedtoken.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<issuerChannelBehaviors>**](issuerchannelbehaviors-element.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<add>**  

## <a name="syntax"></a><span data-ttu-id="bdb9e-106">语法</span><span class="sxs-lookup"><span data-stu-id="bdb9e-106">Syntax</span></span>

```xml
<add issuerAddress="string"
     behaviorConfiguration="string" />
```

## <a name="attributes-and-elements"></a><span data-ttu-id="bdb9e-107">特性和元素</span><span class="sxs-lookup"><span data-stu-id="bdb9e-107">Attributes and Elements</span></span>

<span data-ttu-id="bdb9e-108">以下几节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="bdb9e-108">The following sections describe attributes, child elements, and parent elements</span></span>

### <a name="attributes"></a><span data-ttu-id="bdb9e-109">特性</span><span class="sxs-lookup"><span data-stu-id="bdb9e-109">Attributes</span></span>

|<span data-ttu-id="bdb9e-110">属性</span><span class="sxs-lookup"><span data-stu-id="bdb9e-110">Attribute</span></span>|<span data-ttu-id="bdb9e-111">说明</span><span class="sxs-lookup"><span data-stu-id="bdb9e-111">Description</span></span>|
|---------------|-----------------|
|<span data-ttu-id="bdb9e-112">issuerAddress</span><span class="sxs-lookup"><span data-stu-id="bdb9e-112">issuerAddress</span></span>|<span data-ttu-id="bdb9e-113">要与之通信的安全令牌颁发者的 URI。</span><span class="sxs-lookup"><span data-stu-id="bdb9e-113">The URI of the security token issuer to communicate with.</span></span>|
|<span data-ttu-id="bdb9e-114">behaviorConfiguration</span><span class="sxs-lookup"><span data-stu-id="bdb9e-114">behaviorConfiguration</span></span>|<span data-ttu-id="bdb9e-115">在同一个配置文件中定义的终结点行为的名称。</span><span class="sxs-lookup"><span data-stu-id="bdb9e-115">The name of an endpoint behavior defined in the same configuration file.</span></span>|

### <a name="child-elements"></a><span data-ttu-id="bdb9e-116">子元素</span><span class="sxs-lookup"><span data-stu-id="bdb9e-116">Child Elements</span></span>

<span data-ttu-id="bdb9e-117">无。</span><span class="sxs-lookup"><span data-stu-id="bdb9e-117">None.</span></span>

### <a name="parent-elements"></a><span data-ttu-id="bdb9e-118">父元素</span><span class="sxs-lookup"><span data-stu-id="bdb9e-118">Parent Elements</span></span>

|<span data-ttu-id="bdb9e-119">元素</span><span class="sxs-lookup"><span data-stu-id="bdb9e-119">Element</span></span>|<span data-ttu-id="bdb9e-120">说明</span><span class="sxs-lookup"><span data-stu-id="bdb9e-120">Description</span></span>|
|-------------|-----------------|
|[\<issuerChannelBehaviors>](issuerchannelbehaviors-element.md)|<span data-ttu-id="bdb9e-121">包含与指定的服务令牌服务通信时要使用的 Windows Communication Foundation (WCF) 客户端终结点行为的集合。</span><span class="sxs-lookup"><span data-stu-id="bdb9e-121">Contains a collection of Windows Communication Foundation (WCF) client endpoint behaviors to be used when communicating with the specified Service Token Services.</span></span>|

## <a name="remarks"></a><span data-ttu-id="bdb9e-122">备注</span><span class="sxs-lookup"><span data-stu-id="bdb9e-122">Remarks</span></span>

<span data-ttu-id="bdb9e-123">`issuerAddress` 包含客户端希望与之进行通信的安全令牌服务的 URI。</span><span class="sxs-lookup"><span data-stu-id="bdb9e-123">`issuerAddress` contains the URI of the Security Token Service that the client wants to communicate with.</span></span> <span data-ttu-id="bdb9e-124">`behaviorConfiguration` 指向应用程序在 Windows Communication Foundation (WCF) 创建的通道中使用的终结点行为，以从安全令牌服务获取已颁发的令牌。</span><span class="sxs-lookup"><span data-stu-id="bdb9e-124">`behaviorConfiguration` points to an endpoint behavior that the application uses in the channels created by Windows Communication Foundation (WCF) to get the issued tokens from the Security Token Services.</span></span>

## <a name="see-also"></a><span data-ttu-id="bdb9e-125">请参阅</span><span class="sxs-lookup"><span data-stu-id="bdb9e-125">See also</span></span>

- <xref:System.ServiceModel.Configuration.IssuedTokenClientElement.IssuerChannelBehaviors%2A>
- <xref:System.ServiceModel.Configuration.IssuedTokenClientBehaviorsElement>
- <xref:System.ServiceModel.Configuration.IssuedTokenClientBehaviorsElementCollection>
- <xref:System.ServiceModel.Security.IssuedTokenClientCredential.IssuerChannelBehaviors%2A>
- [<span data-ttu-id="bdb9e-126">服务标识和身份验证</span><span class="sxs-lookup"><span data-stu-id="bdb9e-126">Service Identity and Authentication</span></span>](../../../wcf/feature-details/service-identity-and-authentication.md)
- [<span data-ttu-id="bdb9e-127">安全行为</span><span class="sxs-lookup"><span data-stu-id="bdb9e-127">Security Behaviors</span></span>](../../../wcf/feature-details/security-behaviors-in-wcf.md)
- [<span data-ttu-id="bdb9e-128">联合令牌与颁发的令牌</span><span class="sxs-lookup"><span data-stu-id="bdb9e-128">Federation and Issued Tokens</span></span>](../../../wcf/feature-details/federation-and-issued-tokens.md)
- [<span data-ttu-id="bdb9e-129">保护服务和客户端的安全</span><span class="sxs-lookup"><span data-stu-id="bdb9e-129">Securing Services and Clients</span></span>](../../../wcf/feature-details/securing-services-and-clients.md)
- [<span data-ttu-id="bdb9e-130">保证客户端的安全</span><span class="sxs-lookup"><span data-stu-id="bdb9e-130">Securing Clients</span></span>](../../../wcf/securing-clients.md)
- [<span data-ttu-id="bdb9e-131">如何：创建联合客户端</span><span class="sxs-lookup"><span data-stu-id="bdb9e-131">How to: Create a Federated Client</span></span>](../../../wcf/feature-details/how-to-create-a-federated-client.md)
- [<span data-ttu-id="bdb9e-132">如何：配置本地颁发者</span><span class="sxs-lookup"><span data-stu-id="bdb9e-132">How to: Configure a Local Issuer</span></span>](../../../wcf/feature-details/how-to-configure-a-local-issuer.md)
- [<span data-ttu-id="bdb9e-133">联合令牌与颁发的令牌</span><span class="sxs-lookup"><span data-stu-id="bdb9e-133">Federation and Issued Tokens</span></span>](../../../wcf/feature-details/federation-and-issued-tokens.md)
- [\<issuerChannelBehaviors>](issuerchannelbehaviors-element.md)
