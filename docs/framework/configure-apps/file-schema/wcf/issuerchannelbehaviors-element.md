---
description: 了解详细信息： <issuerChannelBehaviors> 元素
title: <issuerChannelBehaviors> 元素
ms.date: 03/30/2017
ms.assetid: f7378673-8e9b-45b2-98d1-cf5dccdd8c40
no-loc:
- <system.serviceModel>
- <behaviors>
- <endpointBehaviors>
- <behavior>
- <clientCredentials>
- <issuedToken>
- <issuerChannelBehaviors>
- <dataContractSerializer>
ms.openlocfilehash: 6be79f2ee6afb442a7a399ce49df4ad59dff2db5
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99725540"
---
# <a name="issuerchannelbehaviors-element"></a><span data-ttu-id="9ed99-103">\:：： no (<issuerChannelBehaviors>) ：：：元素</span><span class="sxs-lookup"><span data-stu-id="9ed99-103">\<issuerChannelBehaviors> Element</span></span>

<span data-ttu-id="9ed99-104">包含 Windows Communication Foundation (WCF) 客户端终结点行为的集合， (在与指定的服务令牌服务通信时要使用的配置) 中定义。</span><span class="sxs-lookup"><span data-stu-id="9ed99-104">Contains a collection of Windows Communication Foundation (WCF) client endpoint behaviors (defined in the configuration) to be used when communicating with the specified Service Token Services.</span></span> <span data-ttu-id="9ed99-105">定义的行为不能包含任何[ \: ：： no (<clientCredentials>) ：：](clientcredentials.md) ：元素。</span><span class="sxs-lookup"><span data-stu-id="9ed99-105">The defined behaviors cannot include any [\<clientCredentials>](clientcredentials.md) elements.</span></span>

[\<configuration>](../configuration-element.md)\
<span data-ttu-id="9ed99-106">&nbsp;&nbsp;[\:：： no ( # B0>) ：：：](system-servicemodel.md)</span><span class="sxs-lookup"><span data-stu-id="9ed99-106">&nbsp;&nbsp;[\<system.serviceModel>](system-servicemodel.md)</span></span>\
<span data-ttu-id="9ed99-107">&nbsp;&nbsp;&nbsp;&nbsp;[\:：： no (<behaviors>) ：：：](behaviors.md)</span><span class="sxs-lookup"><span data-stu-id="9ed99-107">&nbsp;&nbsp;&nbsp;&nbsp;[\<behaviors>](behaviors.md)</span></span>\
<span data-ttu-id="9ed99-108">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[\:：： no (<endpointBehaviors>) ：：：](endpointbehaviors.md)</span><span class="sxs-lookup"><span data-stu-id="9ed99-108">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[\<endpointBehaviors>](endpointbehaviors.md)</span></span>\
<span data-ttu-id="9ed99-109">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[\:：： no (<behavior>) ：：：](behavior-of-endpointbehaviors.md)</span><span class="sxs-lookup"><span data-stu-id="9ed99-109">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[\<behavior>](behavior-of-endpointbehaviors.md)</span></span>\
<span data-ttu-id="9ed99-110">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[\:：： no (<clientCredentials>) ：：：](clientcredentials.md)</span><span class="sxs-lookup"><span data-stu-id="9ed99-110">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[\<clientCredentials>](clientcredentials.md)</span></span>\
<span data-ttu-id="9ed99-111">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[\:：： no (<issuedToken>) ：：：](issuedtoken.md)</span><span class="sxs-lookup"><span data-stu-id="9ed99-111">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[\<issuedToken>](issuedtoken.md)</span></span>\
<span data-ttu-id="9ed99-112">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;\:：： no (<issuerChannelBehaviors>) ：：：</span><span class="sxs-lookup"><span data-stu-id="9ed99-112">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;\<issuerChannelBehaviors></span></span>

## <a name="syntax"></a><span data-ttu-id="9ed99-113">语法</span><span class="sxs-lookup"><span data-stu-id="9ed99-113">Syntax</span></span>

```xml
<issuerChannelBehaviors>
  <add behaviorConfiguration="string"
       issuerAddress="string" />
</issuerChannelBehaviors>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="9ed99-114">特性和元素</span><span class="sxs-lookup"><span data-stu-id="9ed99-114">Attributes and elements</span></span>

<span data-ttu-id="9ed99-115">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="9ed99-115">The following sections describe attributes, child elements, and parent elements.</span></span>

### <a name="attributes"></a><span data-ttu-id="9ed99-116">特性</span><span class="sxs-lookup"><span data-stu-id="9ed99-116">Attributes</span></span>

<span data-ttu-id="9ed99-117">无。</span><span class="sxs-lookup"><span data-stu-id="9ed99-117">None.</span></span>

### <a name="child-elements"></a><span data-ttu-id="9ed99-118">子元素</span><span class="sxs-lookup"><span data-stu-id="9ed99-118">Child elements</span></span>

|<span data-ttu-id="9ed99-119">元素</span><span class="sxs-lookup"><span data-stu-id="9ed99-119">Element</span></span>|<span data-ttu-id="9ed99-120">说明</span><span class="sxs-lookup"><span data-stu-id="9ed99-120">Description</span></span>|
|-------------|-----------------|
|[\<add>](add-of-issuerchannelbehaviors.md)|<span data-ttu-id="9ed99-121">向集合中添加行为。</span><span class="sxs-lookup"><span data-stu-id="9ed99-121">Adds a behavior to the collection.</span></span>|

### <a name="parent-elements"></a><span data-ttu-id="9ed99-122">父元素</span><span class="sxs-lookup"><span data-stu-id="9ed99-122">Parent elements</span></span>

|<span data-ttu-id="9ed99-123">元素</span><span class="sxs-lookup"><span data-stu-id="9ed99-123">Element</span></span>|<span data-ttu-id="9ed99-124">说明</span><span class="sxs-lookup"><span data-stu-id="9ed99-124">Description</span></span>|
|-------------|-----------------|
|[<span data-ttu-id="9ed99-125">\:：： no (<issuedToken>) ：：：</span><span class="sxs-lookup"><span data-stu-id="9ed99-125">\<issuedToken></span></span>](issuedtoken.md)|<span data-ttu-id="9ed99-126">指定用于向服务验证客户端身份的自定义令牌。</span><span class="sxs-lookup"><span data-stu-id="9ed99-126">Specifies a custom token used to authenticate a client to a service.</span></span>|

## <a name="remarks"></a><span data-ttu-id="9ed99-127">备注</span><span class="sxs-lookup"><span data-stu-id="9ed99-127">Remarks</span></span>

<span data-ttu-id="9ed99-128">当必须使用任何行为（包含 `<clientCredentials>` 元素的行为除外）与某个服务进行通信时，应使用此元素。</span><span class="sxs-lookup"><span data-stu-id="9ed99-128">Use this element when any behaviors (other than behaviors that include `<clientCredentials>` elements) must be used to communicate with a service.</span></span> <span data-ttu-id="9ed99-129">例如，如果必须包含[ \: ：： no (<dataContractSerializer>) ：：](datacontractserializer-element.md) ：行为元素。</span><span class="sxs-lookup"><span data-stu-id="9ed99-129">For example, if a [\<dataContractSerializer>](datacontractserializer-element.md) behavior element must be included.</span></span>

## <a name="see-also"></a><span data-ttu-id="9ed99-130">请参阅</span><span class="sxs-lookup"><span data-stu-id="9ed99-130">See also</span></span>

- <xref:System.ServiceModel.Configuration.IssuedTokenClientElement.IssuerChannelBehaviors%2A>
- <xref:System.ServiceModel.Configuration.IssuedTokenClientBehaviorsElement>
- <xref:System.ServiceModel.Configuration.IssuedTokenClientBehaviorsElementCollection>
- <xref:System.ServiceModel.Security.IssuedTokenClientCredential.IssuerChannelBehaviors%2A>
- [<span data-ttu-id="9ed99-131">服务标识和身份验证</span><span class="sxs-lookup"><span data-stu-id="9ed99-131">Service Identity and Authentication</span></span>](../../../wcf/feature-details/service-identity-and-authentication.md)
- [<span data-ttu-id="9ed99-132">安全行为</span><span class="sxs-lookup"><span data-stu-id="9ed99-132">Security Behaviors</span></span>](../../../wcf/feature-details/security-behaviors-in-wcf.md)
- [<span data-ttu-id="9ed99-133">联合令牌与颁发的令牌</span><span class="sxs-lookup"><span data-stu-id="9ed99-133">Federation and Issued Tokens</span></span>](../../../wcf/feature-details/federation-and-issued-tokens.md)
- [<span data-ttu-id="9ed99-134">保护服务和客户端的安全</span><span class="sxs-lookup"><span data-stu-id="9ed99-134">Securing Services and Clients</span></span>](../../../wcf/feature-details/securing-services-and-clients.md)
- [<span data-ttu-id="9ed99-135">保证客户端的安全</span><span class="sxs-lookup"><span data-stu-id="9ed99-135">Securing Clients</span></span>](../../../wcf/securing-clients.md)
- [<span data-ttu-id="9ed99-136">如何：创建联合客户端</span><span class="sxs-lookup"><span data-stu-id="9ed99-136">How to: Create a Federated Client</span></span>](../../../wcf/feature-details/how-to-create-a-federated-client.md)
- [<span data-ttu-id="9ed99-137">如何：配置本地颁发者</span><span class="sxs-lookup"><span data-stu-id="9ed99-137">How to: Configure a Local Issuer</span></span>](../../../wcf/feature-details/how-to-configure-a-local-issuer.md)
- [<span data-ttu-id="9ed99-138">联合令牌与颁发的令牌</span><span class="sxs-lookup"><span data-stu-id="9ed99-138">Federation and Issued Tokens</span></span>](../../../wcf/feature-details/federation-and-issued-tokens.md)
