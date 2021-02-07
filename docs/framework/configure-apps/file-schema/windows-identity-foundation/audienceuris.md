---
description: 了解详细信息： <audienceUris>
title: <audienceUris>
ms.date: 03/30/2017
ms.assetid: 7a3d8515-d756-4afe-a22d-07cbe2217ee3
author: BrucePerlerMS
ms.openlocfilehash: 98b411e73d4b9941e65daaf5d1d63285cdc90fd0
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99681846"
---
# \<audienceUris>

<span data-ttu-id="b8038-102">指定一组 Uri，这些 Uri 是信赖方 (RP) 的可接受标识符。</span><span class="sxs-lookup"><span data-stu-id="b8038-102">Specifies the set of URIs that are acceptable identifiers of the relying party (RP).</span></span> <span data-ttu-id="b8038-103">除非已针对允许的某个受众 URI 确定了令牌的范围，否则不会接受令牌。</span><span class="sxs-lookup"><span data-stu-id="b8038-103">Tokens will not be accepted unless they are scoped for one of the allowed audience URIs.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.identityModel>**](system-identitymodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<identityConfiguration>**](identityconfiguration.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<securityTokenHandlers>**](securitytokenhandlers.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<securityTokenHandlerConfiguration>**](securitytokenhandlerconfiguration.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<audienceUris>**  
  
## <a name="syntax"></a><span data-ttu-id="b8038-104">语法</span><span class="sxs-lookup"><span data-stu-id="b8038-104">Syntax</span></span>  
  
```xml  
<system.identityModel>  
  <identityConfiguration>  
    <securityTokenHandlers>  
      <securityTokenHandlerConfiguration>  
        <audienceUris mode=xs:string>  
          <add value=xs:string />  
          <clear />  
          <remove value=xs:string />  
        </audienceUris>  
      </securityTokenHandlerConfiguration>  
    </securityTokenHandlers>  
  </identityConfiguration>  
</system.identityModel>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="b8038-105">特性和元素</span><span class="sxs-lookup"><span data-stu-id="b8038-105">Attributes and Elements</span></span>  

 <span data-ttu-id="b8038-106">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="b8038-106">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="b8038-107">特性</span><span class="sxs-lookup"><span data-stu-id="b8038-107">Attributes</span></span>  
  
|<span data-ttu-id="b8038-108">属性</span><span class="sxs-lookup"><span data-stu-id="b8038-108">Attribute</span></span>|<span data-ttu-id="b8038-109">说明</span><span class="sxs-lookup"><span data-stu-id="b8038-109">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="b8038-110">mode</span><span class="sxs-lookup"><span data-stu-id="b8038-110">mode</span></span>|<span data-ttu-id="b8038-111">一个 <xref:System.IdentityModel.Selectors.AudienceUriMode> 值，该值指定是否应将受众限制应用于传入令牌。</span><span class="sxs-lookup"><span data-stu-id="b8038-111">An <xref:System.IdentityModel.Selectors.AudienceUriMode> value that specifies whether the audience restriction should be applied to an incoming token.</span></span> <span data-ttu-id="b8038-112">可能的值为 "始终"、"从不" 和 "BearerKeyOnly"。</span><span class="sxs-lookup"><span data-stu-id="b8038-112">The possible values are "Always", "Never", and "BearerKeyOnly".</span></span> <span data-ttu-id="b8038-113">默认值为 "Always"。</span><span class="sxs-lookup"><span data-stu-id="b8038-113">The default is "Always".</span></span> <span data-ttu-id="b8038-114">可选。</span><span class="sxs-lookup"><span data-stu-id="b8038-114">Optional.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="b8038-115">子元素</span><span class="sxs-lookup"><span data-stu-id="b8038-115">Child Elements</span></span>  
  
|<span data-ttu-id="b8038-116">元素</span><span class="sxs-lookup"><span data-stu-id="b8038-116">Element</span></span>|<span data-ttu-id="b8038-117">说明</span><span class="sxs-lookup"><span data-stu-id="b8038-117">Description</span></span>|  
|-------------|-----------------|  
|`<add value=xs:string>`|<span data-ttu-id="b8038-118">将属性指定的 URI 添加 `value` 到 audienceUris 集合。</span><span class="sxs-lookup"><span data-stu-id="b8038-118">Adds the URI specified by the `value` attribute to the audienceUris collection.</span></span> <span data-ttu-id="b8038-119">需要 `value` 属性。</span><span class="sxs-lookup"><span data-stu-id="b8038-119">The `value` attribute is required.</span></span> <span data-ttu-id="b8038-120">URI 区分大小写。</span><span class="sxs-lookup"><span data-stu-id="b8038-120">The URI is case-sensitive.</span></span>|  
|`<clear>`|<span data-ttu-id="b8038-121">清除 audienceUris 集合。</span><span class="sxs-lookup"><span data-stu-id="b8038-121">Clears the audienceUris collection.</span></span> <span data-ttu-id="b8038-122">所有标识符都将从集合中删除。</span><span class="sxs-lookup"><span data-stu-id="b8038-122">All identifiers are removed from the collection.</span></span>|  
|`<remove value=xs:string>`|<span data-ttu-id="b8038-123">`value`从 audienceUris 集合中移除特性指定的 URI。</span><span class="sxs-lookup"><span data-stu-id="b8038-123">Removes the URI specified by the `value` attribute from the audienceUris collection.</span></span> <span data-ttu-id="b8038-124">需要 `value` 属性。</span><span class="sxs-lookup"><span data-stu-id="b8038-124">The `value` attribute is required.</span></span> <span data-ttu-id="b8038-125">URI 区分大小写。</span><span class="sxs-lookup"><span data-stu-id="b8038-125">The URI is case-sensitive.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="b8038-126">父元素</span><span class="sxs-lookup"><span data-stu-id="b8038-126">Parent Elements</span></span>  
  
|<span data-ttu-id="b8038-127">元素</span><span class="sxs-lookup"><span data-stu-id="b8038-127">Element</span></span>|<span data-ttu-id="b8038-128">说明</span><span class="sxs-lookup"><span data-stu-id="b8038-128">Description</span></span>|  
|-------------|-----------------|  
|[\<securityTokenHandlerConfiguration>](securitytokenhandlerconfiguration.md)|<span data-ttu-id="b8038-129">为安全标记处理程序的集合提供配置。</span><span class="sxs-lookup"><span data-stu-id="b8038-129">Provides configuration for a collection of security token handlers.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="b8038-130">备注</span><span class="sxs-lookup"><span data-stu-id="b8038-130">Remarks</span></span>  

 <span data-ttu-id="b8038-131">默认情况下，集合为空;使用 `<add>` 、 `<clear>` 和 `<remove>` 元素可修改集合。</span><span class="sxs-lookup"><span data-stu-id="b8038-131">By default, the collection is empty; use `<add>`, `<clear>`, and `<remove>` elements to modify the collection.</span></span> <span data-ttu-id="b8038-132"><xref:System.IdentityModel.Tokens.SamlSecurityTokenHandler> 和 <xref:System.IdentityModel.Tokens.Saml2SecurityTokenHandler> 对象使用受众 uri 集合中的值来配置对象中允许的受众 uri 限制 <xref:System.IdentityModel.Tokens.SamlSecurityTokenRequirement> 。</span><span class="sxs-lookup"><span data-stu-id="b8038-132"><xref:System.IdentityModel.Tokens.SamlSecurityTokenHandler> and <xref:System.IdentityModel.Tokens.Saml2SecurityTokenHandler> objects use the values in the audience URI collection to configure any allowed audience URI restrictions in <xref:System.IdentityModel.Tokens.SamlSecurityTokenRequirement> objects.</span></span>  
  
 <span data-ttu-id="b8038-133">`<audienceUris>`元素由 <xref:System.IdentityModel.Configuration.AudienceUriElementCollection> 类表示。</span><span class="sxs-lookup"><span data-stu-id="b8038-133">The `<audienceUris>` element is represented by the <xref:System.IdentityModel.Configuration.AudienceUriElementCollection> class.</span></span> <span data-ttu-id="b8038-134">添加到集合中的单个 URI 由 <xref:System.IdentityModel.Configuration.AudienceUriElement> 类表示。</span><span class="sxs-lookup"><span data-stu-id="b8038-134">An individual URI added to the collection is represented by the <xref:System.IdentityModel.Configuration.AudienceUriElement> class.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="b8038-135">使用 `<audienceUris>` 元素作为元素的子元素 [\<identityConfiguration>](identityconfiguration.md) 已被弃用，但仍支持向后兼容。</span><span class="sxs-lookup"><span data-stu-id="b8038-135">The use of the `<audienceUris>` element as a child element of the [\<identityConfiguration>](identityconfiguration.md) element has been deprecated, but is still supported for backward compatibility.</span></span> <span data-ttu-id="b8038-136">元素上的设置将 `<securityTokenHandlerConfiguration>` 替代元素上的设置 `<identityConfiguration>` 。</span><span class="sxs-lookup"><span data-stu-id="b8038-136">Settings on the `<securityTokenHandlerConfiguration>` element override those on the `<identityConfiguration>` element.</span></span>  
  
## <a name="example"></a><span data-ttu-id="b8038-137">示例</span><span class="sxs-lookup"><span data-stu-id="b8038-137">Example</span></span>  

 <span data-ttu-id="b8038-138">下面的 XML 演示如何配置应用程序的可接受受众 Uri。</span><span class="sxs-lookup"><span data-stu-id="b8038-138">The following XML shows how to configure the acceptable audience URIs for an application.</span></span> <span data-ttu-id="b8038-139">此示例配置单个 URI。</span><span class="sxs-lookup"><span data-stu-id="b8038-139">This example configures a single URI.</span></span> <span data-ttu-id="b8038-140">将接受范围为此 URI 的标记，所有其他标记将被拒绝。</span><span class="sxs-lookup"><span data-stu-id="b8038-140">Tokens scoped for this URI will be accepted, all others will be rejected.</span></span>  
  
```xml  
<audienceUris>  
  <add value="http://localhost:19851/"/>  
</audienceUris>  
```
