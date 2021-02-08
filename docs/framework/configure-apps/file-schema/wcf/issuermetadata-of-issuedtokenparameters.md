---
description: 了解详细 <issuerMetadata> 信息： <issuedTokenParameters>
title: <issuerMetadata> 的 <issuedTokenParameters>
ms.date: 03/30/2017
ms.assetid: 1a85ca37-496d-4fa3-8d44-d6c9383d735c
ms.openlocfilehash: 6b0b5064254caf1c6bcf72c2e6d3449402853b98
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99802237"
---
# <a name="issuermetadata-of-issuedtokenparameters"></a><span data-ttu-id="3b57c-103">\<issuerMetadata> 的 \<issuedTokenParameters></span><span class="sxs-lookup"><span data-stu-id="3b57c-103">\<issuerMetadata> of \<issuedTokenParameters></span></span>

[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<bindings>**](bindings.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<customBinding>**](custombinding.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<binding>**\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<security>**](security-of-custombinding.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<issuedTokenParameters>**](issuedtokenparameters.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<issuerMetadata>**  
  
## <a name="syntax"></a><span data-ttu-id="3b57c-104">语法</span><span class="sxs-lookup"><span data-stu-id="3b57c-104">Syntax</span></span>  
  
```xml  
<issuerMetaData address="String" />
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="3b57c-105">特性和元素</span><span class="sxs-lookup"><span data-stu-id="3b57c-105">Attributes and Elements</span></span>  

 <span data-ttu-id="3b57c-106">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="3b57c-106">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="3b57c-107">特性</span><span class="sxs-lookup"><span data-stu-id="3b57c-107">Attributes</span></span>  
  
|<span data-ttu-id="3b57c-108">属性</span><span class="sxs-lookup"><span data-stu-id="3b57c-108">Attribute</span></span>|<span data-ttu-id="3b57c-109">说明</span><span class="sxs-lookup"><span data-stu-id="3b57c-109">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="3b57c-110">address</span><span class="sxs-lookup"><span data-stu-id="3b57c-110">address</span></span>|<span data-ttu-id="3b57c-111">必需。</span><span class="sxs-lookup"><span data-stu-id="3b57c-111">Required.</span></span> <span data-ttu-id="3b57c-112">一个指定终结点地址的字符串。</span><span class="sxs-lookup"><span data-stu-id="3b57c-112">A string that specifies the address of the endpoint.</span></span> <span data-ttu-id="3b57c-113">该地址必须为绝对 URI。</span><span class="sxs-lookup"><span data-stu-id="3b57c-113">The address must be an absolute URI.</span></span> <span data-ttu-id="3b57c-114">默认值为一个空字符串。</span><span class="sxs-lookup"><span data-stu-id="3b57c-114">The default value is an empty string.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="3b57c-115">子元素</span><span class="sxs-lookup"><span data-stu-id="3b57c-115">Child Elements</span></span>  
  
|<span data-ttu-id="3b57c-116">元素</span><span class="sxs-lookup"><span data-stu-id="3b57c-116">Element</span></span>|<span data-ttu-id="3b57c-117">说明</span><span class="sxs-lookup"><span data-stu-id="3b57c-117">Description</span></span>|  
|-------------|-----------------|  
|[\<headers>](headers-element.md)|<span data-ttu-id="3b57c-118">一个地址标头集合。</span><span class="sxs-lookup"><span data-stu-id="3b57c-118">A collection of address headers.</span></span>|  
|[\<identity>](identity.md)|<span data-ttu-id="3b57c-119">一个标识，与某个终结点交换消息的其他终结点可以使用该标识对该终结点进行身份验证。</span><span class="sxs-lookup"><span data-stu-id="3b57c-119">An identity that enables the authentication of an endpoint by other endpoints exchanging messages with it.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="3b57c-120">父元素</span><span class="sxs-lookup"><span data-stu-id="3b57c-120">Parent Elements</span></span>  
  
|<span data-ttu-id="3b57c-121">元素</span><span class="sxs-lookup"><span data-stu-id="3b57c-121">Element</span></span>|<span data-ttu-id="3b57c-122">说明</span><span class="sxs-lookup"><span data-stu-id="3b57c-122">Description</span></span>|  
|-------------|-----------------|  
|[\<issuedTokenParameters>](issuedtokenparameters.md)|<span data-ttu-id="3b57c-123">指定在联合安全方案中颁发的安全令牌的参数。</span><span class="sxs-lookup"><span data-stu-id="3b57c-123">Specifies the parameters for an security token issued in a Federated security scenario.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="3b57c-124">请参阅</span><span class="sxs-lookup"><span data-stu-id="3b57c-124">See also</span></span>

- <xref:System.ServiceModel.Security.Tokens.IssuedSecurityTokenParameters>
- <xref:System.ServiceModel.Configuration.IssuedTokenParametersElement>
- <xref:System.ServiceModel.Channels.CustomBinding>
- [<span data-ttu-id="3b57c-125">服务标识和身份验证</span><span class="sxs-lookup"><span data-stu-id="3b57c-125">Service Identity and Authentication</span></span>](../../../wcf/feature-details/service-identity-and-authentication.md)
- [<span data-ttu-id="3b57c-126">联合令牌与颁发的令牌</span><span class="sxs-lookup"><span data-stu-id="3b57c-126">Federation and Issued Tokens</span></span>](../../../wcf/feature-details/federation-and-issued-tokens.md)
- [<span data-ttu-id="3b57c-127">使用自定义绑定的安全功能</span><span class="sxs-lookup"><span data-stu-id="3b57c-127">Security Capabilities with Custom Bindings</span></span>](../../../wcf/feature-details/security-capabilities-with-custom-bindings.md)
- [<span data-ttu-id="3b57c-128">联合令牌与颁发的令牌</span><span class="sxs-lookup"><span data-stu-id="3b57c-128">Federation and Issued Tokens</span></span>](../../../wcf/feature-details/federation-and-issued-tokens.md)
- [<span data-ttu-id="3b57c-129">绑定</span><span class="sxs-lookup"><span data-stu-id="3b57c-129">Bindings</span></span>](../../../wcf/bindings.md)
- [<span data-ttu-id="3b57c-130">扩展绑定</span><span class="sxs-lookup"><span data-stu-id="3b57c-130">Extending Bindings</span></span>](../../../wcf/extending/extending-bindings.md)
- [<span data-ttu-id="3b57c-131">自定义绑定</span><span class="sxs-lookup"><span data-stu-id="3b57c-131">Custom Bindings</span></span>](../../../wcf/extending/custom-bindings.md)
- [\<customBinding>](custombinding.md)
- [<span data-ttu-id="3b57c-132">如何：使用 SecurityBindingElement 创建自定义绑定</span><span class="sxs-lookup"><span data-stu-id="3b57c-132">How to: Create a Custom Binding Using the SecurityBindingElement</span></span>](../../../wcf/feature-details/how-to-create-a-custom-binding-using-the-securitybindingelement.md)
- [<span data-ttu-id="3b57c-133">自定义绑定安全性</span><span class="sxs-lookup"><span data-stu-id="3b57c-133">Custom Binding Security</span></span>](../../../wcf/samples/custom-binding-security.md)
