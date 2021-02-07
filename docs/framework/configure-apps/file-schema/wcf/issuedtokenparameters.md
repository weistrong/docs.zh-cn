---
description: 了解详细信息： <issuedTokenParameters>
title: <issuedTokenParameters>
ms.date: 03/30/2017
ms.assetid: 120b3f37-7331-4816-b712-d6aab39655a4
ms.openlocfilehash: 92c8f5aa25ddb71561eb702ba3eb0396456008a6
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99725657"
---
# \<issuedTokenParameters>

<span data-ttu-id="9e1ba-102">指定在联合安全方案中颁发的安全令牌的参数。</span><span class="sxs-lookup"><span data-stu-id="9e1ba-102">Specifies the parameters for a security token issued in a Federated security scenario.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<bindings>**](bindings.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<customBinding>**](custombinding.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<binding>**\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<security>**](security-of-custombinding.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<issuedTokenParameters>**  
  
## <a name="syntax"></a><span data-ttu-id="9e1ba-103">语法</span><span class="sxs-lookup"><span data-stu-id="9e1ba-103">Syntax</span></span>  
  
```xml  
<issuedTokenParameters defaultMessageSecurityVersion="System.ServiceModel.MessageSecurityVersion"
                       inclusionMode="AlwaysToInitiator/AlwaysToRecipient/Never/Once"
                       keySize="Integer"
                       keyType="AsymmetricKey/BearerKey/SymmetricKey"
                       tokenType="String">
  <additionalRequestParameters />
  <claimTypeRequirements>
    <add claimType="URI"
         isOptional="Boolean" />
  </claimTypeRequirements>
  <issuer address="String"
          binding="" />
  <issuerMetadata address="String" />
</issuedTokenParameters>
```  
  
## <a name="type"></a><span data-ttu-id="9e1ba-104">类型</span><span class="sxs-lookup"><span data-stu-id="9e1ba-104">Type</span></span>  

 `Type`  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="9e1ba-105">特性和元素</span><span class="sxs-lookup"><span data-stu-id="9e1ba-105">Attributes and Elements</span></span>  

 <span data-ttu-id="9e1ba-106">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="9e1ba-106">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="9e1ba-107">特性</span><span class="sxs-lookup"><span data-stu-id="9e1ba-107">Attributes</span></span>  
  
|<span data-ttu-id="9e1ba-108">属性</span><span class="sxs-lookup"><span data-stu-id="9e1ba-108">Attribute</span></span>|<span data-ttu-id="9e1ba-109">说明</span><span class="sxs-lookup"><span data-stu-id="9e1ba-109">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="9e1ba-110">defaultMessageSecurityVersion</span><span class="sxs-lookup"><span data-stu-id="9e1ba-110">defaultMessageSecurityVersion</span></span>|<span data-ttu-id="9e1ba-111">指定安全规范（WS-Security、WS-Trust、WS-Secure Conversation 和 WS-Security Policy）的版本，绑定必须支持这些安全规范。</span><span class="sxs-lookup"><span data-stu-id="9e1ba-111">Specifies the versions of the security specifications, (WS-Security, WS-Trust, WS-Secure Conversation and WS-Security Policy) that must be supported by the binding.</span></span> <span data-ttu-id="9e1ba-112">此值的类型为 <xref:System.ServiceModel.MessageSecurityVersion>。</span><span class="sxs-lookup"><span data-stu-id="9e1ba-112">This value is of type <xref:System.ServiceModel.MessageSecurityVersion>.</span></span>|  
|<span data-ttu-id="9e1ba-113">inclusionMode</span><span class="sxs-lookup"><span data-stu-id="9e1ba-113">inclusionMode</span></span>|<span data-ttu-id="9e1ba-114">指定令牌包含要求。</span><span class="sxs-lookup"><span data-stu-id="9e1ba-114">Specifies the token inclusion requirements.</span></span> <span data-ttu-id="9e1ba-115">此属性的类型为 <xref:System.ServiceModel.Security.Tokens.SecurityTokenInclusionMode>。</span><span class="sxs-lookup"><span data-stu-id="9e1ba-115">This attribute is of type <xref:System.ServiceModel.Security.Tokens.SecurityTokenInclusionMode>.</span></span>|  
|<span data-ttu-id="9e1ba-116">keySize</span><span class="sxs-lookup"><span data-stu-id="9e1ba-116">keySize</span></span>|<span data-ttu-id="9e1ba-117">一个指定令牌的密钥大小的整数。</span><span class="sxs-lookup"><span data-stu-id="9e1ba-117">An integer that specifies the token key size.</span></span> <span data-ttu-id="9e1ba-118">默认值为 256。</span><span class="sxs-lookup"><span data-stu-id="9e1ba-118">The default value is 256.</span></span>|  
|<span data-ttu-id="9e1ba-119">keyType</span><span class="sxs-lookup"><span data-stu-id="9e1ba-119">keyType</span></span>|<span data-ttu-id="9e1ba-120">一个指定密钥类型的 <xref:System.IdentityModel.Tokens.SecurityKeyType> 的有效值。</span><span class="sxs-lookup"><span data-stu-id="9e1ba-120">A valid value of <xref:System.IdentityModel.Tokens.SecurityKeyType> that specifies the key type.</span></span> <span data-ttu-id="9e1ba-121">默认值为 `SymmetricKey`。</span><span class="sxs-lookup"><span data-stu-id="9e1ba-121">The default is `SymmetricKey`.</span></span>|  
|<span data-ttu-id="9e1ba-122">tokenType</span><span class="sxs-lookup"><span data-stu-id="9e1ba-122">tokenType</span></span>|<span data-ttu-id="9e1ba-123">一个指定令牌类型的字符串。</span><span class="sxs-lookup"><span data-stu-id="9e1ba-123">A string that specifies the token type.</span></span> <span data-ttu-id="9e1ba-124">默认值为“http://docs.oasis-open.org/wss/oasis-wss-saml-token-profile-1.1#SAML”。</span><span class="sxs-lookup"><span data-stu-id="9e1ba-124">The default is "http://docs.oasis-open.org/wss/oasis-wss-saml-token-profile-1.1#SAML".</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="9e1ba-125">子元素</span><span class="sxs-lookup"><span data-stu-id="9e1ba-125">Child Elements</span></span>  
  
|<span data-ttu-id="9e1ba-126">元素</span><span class="sxs-lookup"><span data-stu-id="9e1ba-126">Element</span></span>|<span data-ttu-id="9e1ba-127">说明</span><span class="sxs-lookup"><span data-stu-id="9e1ba-127">Description</span></span>|  
|-------------|-----------------|  
|[\<additionalRequestParameters>](additionalrequestparameters-element.md)|<span data-ttu-id="9e1ba-128">一个用于指定附加请求参数的配置元素的集合。</span><span class="sxs-lookup"><span data-stu-id="9e1ba-128">A collection of configuration elements that specify additional request parameters.</span></span>|  
|[\<claimTypeRequirements>](claimtyperequirements-element.md)|<span data-ttu-id="9e1ba-129">指定所需声明类型的集合。</span><span class="sxs-lookup"><span data-stu-id="9e1ba-129">Specifies a collection of required claim types.</span></span><br /><br /> <span data-ttu-id="9e1ba-130">在联合方案中，服务规定有关传入凭据的要求。</span><span class="sxs-lookup"><span data-stu-id="9e1ba-130">In a federated scenario, services state the requirements on incoming credentials.</span></span> <span data-ttu-id="9e1ba-131">例如，传入凭据必须具有某组声明类型。</span><span class="sxs-lookup"><span data-stu-id="9e1ba-131">For example, the incoming credentials must possess a certain set of claim types.</span></span> <span data-ttu-id="9e1ba-132">此集合中的每个元素都指定希望出现在联合凭据中的必选和可选的声明类型。</span><span class="sxs-lookup"><span data-stu-id="9e1ba-132">Each element in this collection specifies the types of required and optional claims expected to appear in a federated credential.</span></span>|  
|[\<issuer>](issuer-of-issuedtokenparameters.md)|<span data-ttu-id="9e1ba-133">一个用于指定颁发当前令牌的终结点的配置元素。</span><span class="sxs-lookup"><span data-stu-id="9e1ba-133">A configuration element that specifies the endpoint that issues the current token.</span></span>|  
|[\<issuerMetadata>](issuermetadata-of-issuedtokenparameters.md)|<span data-ttu-id="9e1ba-134">一个用于指定令牌颁发者的元数据的终结点地址的配置元素。</span><span class="sxs-lookup"><span data-stu-id="9e1ba-134">A configuration element that specifies the endpoint address of the token issuer's metadata.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="9e1ba-135">父元素</span><span class="sxs-lookup"><span data-stu-id="9e1ba-135">Parent Elements</span></span>  
  
|<span data-ttu-id="9e1ba-136">元素</span><span class="sxs-lookup"><span data-stu-id="9e1ba-136">Element</span></span>|<span data-ttu-id="9e1ba-137">说明</span><span class="sxs-lookup"><span data-stu-id="9e1ba-137">Description</span></span>|  
|-------------|-----------------|  
|[\<secureConversationBootstrap>](secureconversationbootstrap.md)|<span data-ttu-id="9e1ba-138">指定用于启动安全对话服务的默认值。</span><span class="sxs-lookup"><span data-stu-id="9e1ba-138">Specifies the default values used for initiating a secure conversation service.</span></span>|  
|[\<security>](security-of-custombinding.md)|<span data-ttu-id="9e1ba-139">指定自定义绑定的安全选项。</span><span class="sxs-lookup"><span data-stu-id="9e1ba-139">Specifies the security options for a custom binding.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="9e1ba-140">请参阅</span><span class="sxs-lookup"><span data-stu-id="9e1ba-140">See also</span></span>

- <xref:System.ServiceModel.Security.Tokens.IssuedSecurityTokenParameters>
- <xref:System.ServiceModel.Configuration.IssuedTokenParametersElement>
- <xref:System.ServiceModel.Configuration.SecurityElementBase.IssuedTokenParameters%2A>
- <xref:System.ServiceModel.Channels.CustomBinding>
- [<span data-ttu-id="9e1ba-141">绑定</span><span class="sxs-lookup"><span data-stu-id="9e1ba-141">Bindings</span></span>](../../../wcf/bindings.md)
- [<span data-ttu-id="9e1ba-142">扩展绑定</span><span class="sxs-lookup"><span data-stu-id="9e1ba-142">Extending Bindings</span></span>](../../../wcf/extending/extending-bindings.md)
- [<span data-ttu-id="9e1ba-143">自定义绑定</span><span class="sxs-lookup"><span data-stu-id="9e1ba-143">Custom Bindings</span></span>](../../../wcf/extending/custom-bindings.md)
- [\<customBinding>](custombinding.md)
- [<span data-ttu-id="9e1ba-144">如何：使用 SecurityBindingElement 创建自定义绑定</span><span class="sxs-lookup"><span data-stu-id="9e1ba-144">How to: Create a Custom Binding Using the SecurityBindingElement</span></span>](../../../wcf/feature-details/how-to-create-a-custom-binding-using-the-securitybindingelement.md)
- [<span data-ttu-id="9e1ba-145">自定义绑定安全性</span><span class="sxs-lookup"><span data-stu-id="9e1ba-145">Custom Binding Security</span></span>](../../../wcf/samples/custom-binding-security.md)
- [<span data-ttu-id="9e1ba-146">服务标识和身份验证</span><span class="sxs-lookup"><span data-stu-id="9e1ba-146">Service Identity and Authentication</span></span>](../../../wcf/feature-details/service-identity-and-authentication.md)
- [<span data-ttu-id="9e1ba-147">联合令牌与颁发的令牌</span><span class="sxs-lookup"><span data-stu-id="9e1ba-147">Federation and Issued Tokens</span></span>](../../../wcf/feature-details/federation-and-issued-tokens.md)
- [<span data-ttu-id="9e1ba-148">使用自定义绑定的安全功能</span><span class="sxs-lookup"><span data-stu-id="9e1ba-148">Security Capabilities with Custom Bindings</span></span>](../../../wcf/feature-details/security-capabilities-with-custom-bindings.md)
- [<span data-ttu-id="9e1ba-149">联合令牌与颁发的令牌</span><span class="sxs-lookup"><span data-stu-id="9e1ba-149">Federation and Issued Tokens</span></span>](../../../wcf/feature-details/federation-and-issued-tokens.md)
