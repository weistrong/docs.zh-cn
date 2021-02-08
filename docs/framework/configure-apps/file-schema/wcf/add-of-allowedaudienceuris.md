---
description: 了解详细 <add> 信息： <allowedAudienceUris>
title: <add> 的 <allowedAudienceUris>
ms.date: 03/30/2017
ms.assetid: 4e7b7637-e0ea-4a91-988f-6b6ef28d9fc3
ms.openlocfilehash: caa61da0ee7e00691213b95e31c943f5d81eea32
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99782192"
---
# <a name="add-of-allowedaudienceuris"></a><span data-ttu-id="8f2f5-103">\<add> 的 \<allowedAudienceUris></span><span class="sxs-lookup"><span data-stu-id="8f2f5-103">\<add> of \<allowedAudienceUris></span></span>

<span data-ttu-id="8f2f5-104">添加 <xref:System.IdentityModel.Tokens.SamlSecurityToken> 安全令牌的目标 URI，只有在使用该目标 URI 时，<xref:System.IdentityModel.Selectors.SamlSecurityTokenAuthenticator> 实例才会将该令牌视为有效令牌。</span><span class="sxs-lookup"><span data-stu-id="8f2f5-104">Adds a target Uri for which the <xref:System.IdentityModel.Tokens.SamlSecurityToken> security token can be targeted for in order to be considered valid by a <xref:System.IdentityModel.Selectors.SamlSecurityTokenAuthenticator> instance.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<behaviors>**](behaviors.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<serviceBehaviors>**](servicebehaviors.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<behavior>**](behavior-of-servicebehaviors.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<serviceCredentials>**](servicecredentials.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<issuedTokenAuthentication>**](issuedtokenauthentication-of-servicecredentials.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<allowedAudienceUris>**](allowedaudienceuris.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<add>**  
  
## <a name="syntax"></a><span data-ttu-id="8f2f5-105">语法</span><span class="sxs-lookup"><span data-stu-id="8f2f5-105">Syntax</span></span>  
  
```xml  
<allowedAudienceUris>
  <add allowedAudienceUri="String" />
</allowedAudienceUris>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="8f2f5-106">特性和元素</span><span class="sxs-lookup"><span data-stu-id="8f2f5-106">Attributes and Elements</span></span>  

 <span data-ttu-id="8f2f5-107">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="8f2f5-107">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="8f2f5-108">特性</span><span class="sxs-lookup"><span data-stu-id="8f2f5-108">Attributes</span></span>  
  
|<span data-ttu-id="8f2f5-109">属性</span><span class="sxs-lookup"><span data-stu-id="8f2f5-109">Attribute</span></span>|<span data-ttu-id="8f2f5-110">说明</span><span class="sxs-lookup"><span data-stu-id="8f2f5-110">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="8f2f5-111">allowedAudienceUri</span><span class="sxs-lookup"><span data-stu-id="8f2f5-111">allowedAudienceUri</span></span>|<span data-ttu-id="8f2f5-112">一个包含 <xref:System.IdentityModel.Tokens.SamlSecurityToken> 安全令牌的目标 URI 的字符串，只有在使用该目标 URI 时，<xref:System.IdentityModel.Selectors.SamlSecurityTokenAuthenticator> 实例才会将该令牌视为有效令牌。</span><span class="sxs-lookup"><span data-stu-id="8f2f5-112">A string that contains a target Uri for which the <xref:System.IdentityModel.Tokens.SamlSecurityToken> security token can be targeted for in order to be considered valid by a <xref:System.IdentityModel.Selectors.SamlSecurityTokenAuthenticator> instance.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="8f2f5-113">子元素</span><span class="sxs-lookup"><span data-stu-id="8f2f5-113">Child Elements</span></span>  

 <span data-ttu-id="8f2f5-114">无。</span><span class="sxs-lookup"><span data-stu-id="8f2f5-114">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="8f2f5-115">父元素</span><span class="sxs-lookup"><span data-stu-id="8f2f5-115">Parent Elements</span></span>  
  
|<span data-ttu-id="8f2f5-116">元素</span><span class="sxs-lookup"><span data-stu-id="8f2f5-116">Element</span></span>|<span data-ttu-id="8f2f5-117">说明</span><span class="sxs-lookup"><span data-stu-id="8f2f5-117">Description</span></span>|  
|-------------|-----------------|  
|[\<allowedAudienceUris>](allowedaudienceuris.md)|<span data-ttu-id="8f2f5-118">表示 <xref:System.IdentityModel.Tokens.SamlSecurityToken> 安全令牌的目标 URI 集合，只有在使用这些目标 URI 时，<xref:System.IdentityModel.Selectors.SamlSecurityTokenAuthenticator> 实例才会将该令牌视为有效令牌。</span><span class="sxs-lookup"><span data-stu-id="8f2f5-118">Represents a collection of target URIs for which the <xref:System.IdentityModel.Tokens.SamlSecurityToken> security token can be targeted for in order to be considered valid by a <xref:System.IdentityModel.Selectors.SamlSecurityTokenAuthenticator> instance.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="8f2f5-119">备注</span><span class="sxs-lookup"><span data-stu-id="8f2f5-119">Remarks</span></span>  

 <span data-ttu-id="8f2f5-120">在采用颁发 <xref:System.IdentityModel.Tokens.SamlSecurityToken> 安全令牌的安全令牌服务 (STS) 的联合应用程序中，应使用此集合。</span><span class="sxs-lookup"><span data-stu-id="8f2f5-120">You should use this collection in a federated application that utilizes a security token service (STS) that issues <xref:System.IdentityModel.Tokens.SamlSecurityToken> security tokens.</span></span> <span data-ttu-id="8f2f5-121">当 STS 颁发安全令牌时，它可以通过将 <xref:System.IdentityModel.Tokens.SamlAudienceRestrictionCondition> 添加到安全令牌中，来指定安全令牌的目标 Web 服务的 URI。</span><span class="sxs-lookup"><span data-stu-id="8f2f5-121">When the STS issues the security token, it can specify the URI of the Web services for which the security token is intended by adding a <xref:System.IdentityModel.Tokens.SamlAudienceRestrictionCondition> to the security token.</span></span> <span data-ttu-id="8f2f5-122">这样，通过指定应采用以下方式执行此检查，接收方 Web 服务的 <xref:System.IdentityModel.Selectors.SamlSecurityTokenAuthenticator> 将能够验证颁发的安全令牌是否针对此 Web 服务：</span><span class="sxs-lookup"><span data-stu-id="8f2f5-122">That allows the <xref:System.IdentityModel.Selectors.SamlSecurityTokenAuthenticator> for the recipient Web service to verify that the issued security token is intended for this Web service by specifying that this check should happen by doing the following:</span></span>  
  
- <span data-ttu-id="8f2f5-123">将 `audienceUriMode` 的 `<issuedTokenAuthentication>` 属性设置为 <xref:System.IdentityModel.Selectors.AudienceUriMode.Always> 或 <xref:System.IdentityModel.Selectors.AudienceUriMode.BearerKeyOnly>。</span><span class="sxs-lookup"><span data-stu-id="8f2f5-123">Set the `audienceUriMode` attribute of `<issuedTokenAuthentication>` to <xref:System.IdentityModel.Selectors.AudienceUriMode.Always> or <xref:System.IdentityModel.Selectors.AudienceUriMode.BearerKeyOnly>.</span></span>  
  
- <span data-ttu-id="8f2f5-124">将有效 URI 添加到此集合，以指定有效 URI 集。</span><span class="sxs-lookup"><span data-stu-id="8f2f5-124">Specify the set of valid URIs, by adding the URIs to this collection.</span></span>  
  
 <span data-ttu-id="8f2f5-125">有关详细信息，请参阅 <xref:System.IdentityModel.Selectors.SamlSecurityTokenAuthenticator>。</span><span class="sxs-lookup"><span data-stu-id="8f2f5-125">For more information, see <xref:System.IdentityModel.Selectors.SamlSecurityTokenAuthenticator>.</span></span>  
  
 <span data-ttu-id="8f2f5-126">有关使用此配置元素的详细信息，请参阅 [如何：在联合身份验证服务上配置凭据](../../../wcf/feature-details/how-to-configure-credentials-on-a-federation-service.md)。</span><span class="sxs-lookup"><span data-stu-id="8f2f5-126">For more information on using this configuration element, see [How to: Configure Credentials on a Federation Service](../../../wcf/feature-details/how-to-configure-credentials-on-a-federation-service.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8f2f5-127">请参阅</span><span class="sxs-lookup"><span data-stu-id="8f2f5-127">See also</span></span>

- <xref:System.IdentityModel.Selectors.SamlSecurityTokenAuthenticator>
- <xref:System.IdentityModel.Selectors.SamlSecurityTokenAuthenticator.AllowedAudienceUris%2A>
- <xref:System.IdentityModel.Selectors.SamlSecurityTokenAuthenticator.AudienceUriMode%2A>
- <xref:System.ServiceModel.Configuration.IssuedTokenServiceElement.AllowedAudienceUris%2A>
- <xref:System.ServiceModel.Configuration.AllowedAudienceUriElementCollection>
- <xref:System.ServiceModel.Configuration.AllowedAudienceUriElement>
- <xref:System.ServiceModel.Security.IssuedTokenServiceCredential.AllowedAudienceUris%2A>
- [\<allowedAudienceUris>](allowedaudienceuris.md)
- [\<issuedTokenAuthentication>](issuedtokenauthentication-of-servicecredentials.md)
- [<span data-ttu-id="8f2f5-128">安全行为</span><span class="sxs-lookup"><span data-stu-id="8f2f5-128">Security Behaviors</span></span>](../../../wcf/feature-details/security-behaviors-in-wcf.md)
- [<span data-ttu-id="8f2f5-129">保护服务和客户端的安全</span><span class="sxs-lookup"><span data-stu-id="8f2f5-129">Securing Services and Clients</span></span>](../../../wcf/feature-details/securing-services-and-clients.md)
- [<span data-ttu-id="8f2f5-130">如何：在联合身份验证服务上配置凭据</span><span class="sxs-lookup"><span data-stu-id="8f2f5-130">How to: Configure Credentials on a Federation Service</span></span>](../../../wcf/feature-details/how-to-configure-credentials-on-a-federation-service.md)
