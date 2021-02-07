---
description: 了解详细 <issuer> 信息： <issuedTokenParameters>
title: <issuer> 的 <issuedTokenParameters>
ms.date: 03/30/2017
ms.assetid: d6a95f32-d58c-40fc-8658-dd92564d3c90
ms.openlocfilehash: 7d67583eda22414750631b6dff40f6e6ea8831e4
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99725644"
---
# <a name="issuer-of-issuedtokenparameters"></a><span data-ttu-id="0645c-103">\<issuer> 的 \<issuedTokenParameters></span><span class="sxs-lookup"><span data-stu-id="0645c-103">\<issuer> of \<issuedTokenParameters></span></span>

<span data-ttu-id="0645c-104">指定颁发安全令牌的安全令牌服务 (STS)。</span><span class="sxs-lookup"><span data-stu-id="0645c-104">Specifies the Security Token Service (STS) that issues security tokens.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<bindings>**](bindings.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<customBinding>**](custombinding.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<binding>**\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<security>**](security-of-custombinding.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<issuedTokenParameters>**](issuedtokenparameters.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<issuer>**  
  
## <a name="syntax"></a><span data-ttu-id="0645c-105">语法</span><span class="sxs-lookup"><span data-stu-id="0645c-105">Syntax</span></span>  
  
```xml  
<issuer address="Uri" />
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="0645c-106">特性和元素</span><span class="sxs-lookup"><span data-stu-id="0645c-106">Attributes and Elements</span></span>  

 <span data-ttu-id="0645c-107">以下几节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="0645c-107">The following sections describe attributes, child elements, and parent elements</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="0645c-108">特性</span><span class="sxs-lookup"><span data-stu-id="0645c-108">Attributes</span></span>  
  
|<span data-ttu-id="0645c-109">属性</span><span class="sxs-lookup"><span data-stu-id="0645c-109">Attribute</span></span>|<span data-ttu-id="0645c-110">说明</span><span class="sxs-lookup"><span data-stu-id="0645c-110">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="0645c-111">address</span><span class="sxs-lookup"><span data-stu-id="0645c-111">address</span></span>|<span data-ttu-id="0645c-112">必选字符串。</span><span class="sxs-lookup"><span data-stu-id="0645c-112">Required string.</span></span> <span data-ttu-id="0645c-113">STS 的 URL。</span><span class="sxs-lookup"><span data-stu-id="0645c-113">The URL of the STS.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="0645c-114">子元素</span><span class="sxs-lookup"><span data-stu-id="0645c-114">Child Elements</span></span>  
  
|<span data-ttu-id="0645c-115">元素</span><span class="sxs-lookup"><span data-stu-id="0645c-115">Element</span></span>|<span data-ttu-id="0645c-116">说明</span><span class="sxs-lookup"><span data-stu-id="0645c-116">Description</span></span>|  
|-------------|-----------------|  
|[\<headers>](headers-element.md)|<span data-ttu-id="0645c-117">生成器可以创建的终结点的地址标头的集合。</span><span class="sxs-lookup"><span data-stu-id="0645c-117">A collection of address headers for the endpoints that the builder can create.</span></span>|  
|[\<identity>](identity.md)|<span data-ttu-id="0645c-118">在使用颁发的令牌时，指定能够使客户端对服务器进行身份验证的设置。</span><span class="sxs-lookup"><span data-stu-id="0645c-118">When using an issued token, specifies settings that enable the client to authenticate the server.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="0645c-119">父元素</span><span class="sxs-lookup"><span data-stu-id="0645c-119">Parent Elements</span></span>  
  
|<span data-ttu-id="0645c-120">元素</span><span class="sxs-lookup"><span data-stu-id="0645c-120">Element</span></span>|<span data-ttu-id="0645c-121">说明</span><span class="sxs-lookup"><span data-stu-id="0645c-121">Description</span></span>|  
|-------------|-----------------|  
|[\<issuedTokenParameters>](issuedtokenparameters.md)|<span data-ttu-id="0645c-122">指定当前颁发的令牌。</span><span class="sxs-lookup"><span data-stu-id="0645c-122">Specifies the current issued token.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="0645c-123">请参阅</span><span class="sxs-lookup"><span data-stu-id="0645c-123">See also</span></span>

- <xref:System.ServiceModel.Security.Tokens.IssuedSecurityTokenParameters.AdditionalRequestParameters%2A>
- <xref:System.ServiceModel.Configuration.IssuedTokenParametersElement.AdditionalRequestParameters%2A>
- <xref:System.ServiceModel.Channels.CustomBinding>
- [<span data-ttu-id="0645c-124">服务标识和身份验证</span><span class="sxs-lookup"><span data-stu-id="0645c-124">Service Identity and Authentication</span></span>](../../../wcf/feature-details/service-identity-and-authentication.md)
- [<span data-ttu-id="0645c-125">联合令牌与颁发的令牌</span><span class="sxs-lookup"><span data-stu-id="0645c-125">Federation and Issued Tokens</span></span>](../../../wcf/feature-details/federation-and-issued-tokens.md)
- [<span data-ttu-id="0645c-126">使用自定义绑定的安全功能</span><span class="sxs-lookup"><span data-stu-id="0645c-126">Security Capabilities with Custom Bindings</span></span>](../../../wcf/feature-details/security-capabilities-with-custom-bindings.md)
- [<span data-ttu-id="0645c-127">联合令牌与颁发的令牌</span><span class="sxs-lookup"><span data-stu-id="0645c-127">Federation and Issued Tokens</span></span>](../../../wcf/feature-details/federation-and-issued-tokens.md)
- [<span data-ttu-id="0645c-128">绑定</span><span class="sxs-lookup"><span data-stu-id="0645c-128">Bindings</span></span>](../../../wcf/bindings.md)
- [<span data-ttu-id="0645c-129">扩展绑定</span><span class="sxs-lookup"><span data-stu-id="0645c-129">Extending Bindings</span></span>](../../../wcf/extending/extending-bindings.md)
- [<span data-ttu-id="0645c-130">自定义绑定</span><span class="sxs-lookup"><span data-stu-id="0645c-130">Custom Bindings</span></span>](../../../wcf/extending/custom-bindings.md)
- [\<customBinding>](custombinding.md)
- [<span data-ttu-id="0645c-131">如何：使用 SecurityBindingElement 创建自定义绑定</span><span class="sxs-lookup"><span data-stu-id="0645c-131">How to: Create a Custom Binding Using the SecurityBindingElement</span></span>](../../../wcf/feature-details/how-to-create-a-custom-binding-using-the-securitybindingelement.md)
- [<span data-ttu-id="0645c-132">自定义绑定安全性</span><span class="sxs-lookup"><span data-stu-id="0645c-132">Custom Binding Security</span></span>](../../../wcf/samples/custom-binding-security.md)
