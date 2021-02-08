---
description: 了解详细信息： <securityTokenHandlers>
title: <securityTokenHandlers>
ms.date: 03/30/2017
ms.assetid: f11a631d-4094-4e11-bb03-4ede74b30281
author: BrucePerlerMS
ms.openlocfilehash: 14937f6763644f9b7f43c0f7be71ea2352b21402
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99782021"
---
# \<securityTokenHandlers>

<span data-ttu-id="4cb0b-102">指定注册到终结点的安全令牌处理程序的集合。</span><span class="sxs-lookup"><span data-stu-id="4cb0b-102">Specifies a collection of security token handlers that are registered with the endpoint.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.identityModel>**](system-identitymodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<identityConfiguration>**](identityconfiguration.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<securityTokenHandlers>**  
  
## <a name="syntax"></a><span data-ttu-id="4cb0b-103">语法</span><span class="sxs-lookup"><span data-stu-id="4cb0b-103">Syntax</span></span>  
  
```xml  
<system.identityModel>  
  <identityConfiguration>  
    <securityTokenHandlers>  
    </securityTokenHandlers>  
  </identityConfiguration>  
</system.identityModel>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="4cb0b-104">特性和元素</span><span class="sxs-lookup"><span data-stu-id="4cb0b-104">Attributes and Elements</span></span>  

 <span data-ttu-id="4cb0b-105">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="4cb0b-105">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="4cb0b-106">特性</span><span class="sxs-lookup"><span data-stu-id="4cb0b-106">Attributes</span></span>  
  
|<span data-ttu-id="4cb0b-107">属性</span><span class="sxs-lookup"><span data-stu-id="4cb0b-107">Attribute</span></span>|<span data-ttu-id="4cb0b-108">说明</span><span class="sxs-lookup"><span data-stu-id="4cb0b-108">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="4cb0b-109">name</span><span class="sxs-lookup"><span data-stu-id="4cb0b-109">name</span></span>|<span data-ttu-id="4cb0b-110">指定令牌处理程序集合的名称。</span><span class="sxs-lookup"><span data-stu-id="4cb0b-110">Specifies the name of a token handler collection.</span></span> <span data-ttu-id="4cb0b-111">框架唯一识别的值为 "ActAs" 和 "OnBehalfOf"。</span><span class="sxs-lookup"><span data-stu-id="4cb0b-111">The only values recognized by the framework are "ActAs" and "OnBehalfOf".</span></span> <span data-ttu-id="4cb0b-112">如果使用上述任一名称指定了标记处理程序集合，则会在处理 ActAs 或 OnBehalfOf 令牌时使用该集合。</span><span class="sxs-lookup"><span data-stu-id="4cb0b-112">If token handler collections are specified with either of these names, the collection will be used when processing ActAs or OnBehalfOf tokens respectively.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="4cb0b-113">子元素</span><span class="sxs-lookup"><span data-stu-id="4cb0b-113">Child Elements</span></span>  
  
|<span data-ttu-id="4cb0b-114">元素</span><span class="sxs-lookup"><span data-stu-id="4cb0b-114">Element</span></span>|<span data-ttu-id="4cb0b-115">说明</span><span class="sxs-lookup"><span data-stu-id="4cb0b-115">Description</span></span>|  
|-------------|-----------------|  
|[\<add>](add.md)|<span data-ttu-id="4cb0b-116">将安全标记处理程序添加到令牌处理程序集合。</span><span class="sxs-lookup"><span data-stu-id="4cb0b-116">Adds a security token handler to the token handler collection.</span></span>|  
|[\<clear>](clear.md)|<span data-ttu-id="4cb0b-117">清除标记处理程序集合中的所有安全标记处理程序。</span><span class="sxs-lookup"><span data-stu-id="4cb0b-117">Clears all security token handlers from the token handler collection.</span></span>|  
|[\<remove>](remove.md)|<span data-ttu-id="4cb0b-118">从标记处理程序集合中移除安全标记处理程序。</span><span class="sxs-lookup"><span data-stu-id="4cb0b-118">Removes a security token handler from the token handler collection.</span></span>|  
|[\<securityTokenHandlerConfiguration>](securitytokenhandlerconfiguration.md)|<span data-ttu-id="4cb0b-119">为标记处理程序的集合提供配置。</span><span class="sxs-lookup"><span data-stu-id="4cb0b-119">Provides configuration for the collection of token handlers.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="4cb0b-120">父元素</span><span class="sxs-lookup"><span data-stu-id="4cb0b-120">Parent Elements</span></span>  
  
|<span data-ttu-id="4cb0b-121">元素</span><span class="sxs-lookup"><span data-stu-id="4cb0b-121">Element</span></span>|<span data-ttu-id="4cb0b-122">说明</span><span class="sxs-lookup"><span data-stu-id="4cb0b-122">Description</span></span>|  
|-------------|-----------------|  
|[\<identityConfiguration>](identityconfiguration.md)|<span data-ttu-id="4cb0b-123">指定服务级别标识设置。</span><span class="sxs-lookup"><span data-stu-id="4cb0b-123">Specifies service-level identity settings.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="4cb0b-124">备注</span><span class="sxs-lookup"><span data-stu-id="4cb0b-124">Remarks</span></span>  

 <span data-ttu-id="4cb0b-125">可以在服务配置中指定安全令牌处理程序的一个或多个命名集合。</span><span class="sxs-lookup"><span data-stu-id="4cb0b-125">You can specify one or more named collections of security token handlers in a service configuration.</span></span> <span data-ttu-id="4cb0b-126">可以通过使用属性来指定集合的名称 `name` 。</span><span class="sxs-lookup"><span data-stu-id="4cb0b-126">You can specify a name for a collection by using the `name` attribute.</span></span> <span data-ttu-id="4cb0b-127">框架处理的唯一名称为 "ActAs" 和 "OnBehalfOf"。</span><span class="sxs-lookup"><span data-stu-id="4cb0b-127">The only names that the framework handles are "ActAs" and "OnBehalfOf".</span></span> <span data-ttu-id="4cb0b-128">如果这些集合中存在处理程序，则 security token service (STS) ，而不是在处理和标记时使用默认处理程序 `ActAs` `OnBehalfOf` 。</span><span class="sxs-lookup"><span data-stu-id="4cb0b-128">If handlers exist in these collections, they are used by a security token service (STS) instead of the default handlers when processing `ActAs` and `OnBehalfOf` tokens.</span></span>  
  
 <span data-ttu-id="4cb0b-129">默认情况下，使用以下处理程序类型填充集合： <xref:System.IdentityModel.Tokens.SamlSecurityTokenHandler> 、 <xref:System.IdentityModel.Tokens.Saml2SecurityTokenHandler> 、 <xref:System.IdentityModel.Tokens.KerberosSecurityTokenHandler> 、、、 <xref:System.IdentityModel.Tokens.WindowsUserNameSecurityTokenHandler> <xref:System.IdentityModel.Tokens.RsaSecurityTokenHandler> <xref:System.IdentityModel.Tokens.X509SecurityTokenHandler> 和 <xref:System.IdentityModel.Tokens.EncryptedSecurityTokenHandler> 。</span><span class="sxs-lookup"><span data-stu-id="4cb0b-129">By default, the collection is populated with the following handler types: <xref:System.IdentityModel.Tokens.SamlSecurityTokenHandler>, <xref:System.IdentityModel.Tokens.Saml2SecurityTokenHandler>, <xref:System.IdentityModel.Tokens.KerberosSecurityTokenHandler>, <xref:System.IdentityModel.Tokens.WindowsUserNameSecurityTokenHandler>, <xref:System.IdentityModel.Tokens.RsaSecurityTokenHandler>, <xref:System.IdentityModel.Tokens.X509SecurityTokenHandler>, and <xref:System.IdentityModel.Tokens.EncryptedSecurityTokenHandler>.</span></span> <span data-ttu-id="4cb0b-130">您可以使用 `<add>` 、和元素来修改集合 `<remove>` `<clear>` 。</span><span class="sxs-lookup"><span data-stu-id="4cb0b-130">You can modify the collection by using the `<add>`, `<remove>`, and `<clear>` elements.</span></span> <span data-ttu-id="4cb0b-131">必须确保集合中只存在一个特定类型的处理程序。</span><span class="sxs-lookup"><span data-stu-id="4cb0b-131">You must ensure that only a single handler of any particular type exists in the collection.</span></span> <span data-ttu-id="4cb0b-132">例如，如果从类派生处理程序，则可以 <xref:System.IdentityModel.Tokens.Saml2SecurityTokenHandler> <xref:System.IdentityModel.Tokens.Saml2SecurityTokenHandler> 在单个集合中配置处理程序或，但不能同时配置两者。</span><span class="sxs-lookup"><span data-stu-id="4cb0b-132">For example, if you derive a handler from the <xref:System.IdentityModel.Tokens.Saml2SecurityTokenHandler> class, either your handler or the <xref:System.IdentityModel.Tokens.Saml2SecurityTokenHandler> may be configured in a single collection, but not both.</span></span>  
  
 <span data-ttu-id="4cb0b-133">使用 `<securityTokenHandlerConfiguration>` 元素指定集合中处理程序的配置设置。</span><span class="sxs-lookup"><span data-stu-id="4cb0b-133">Use the `<securityTokenHandlerConfiguration>` element to specify configuration settings for the handlers in the collection.</span></span> <span data-ttu-id="4cb0b-134">通过此元素指定的设置将通过元素重写服务上指定的设置 [\<identityConfiguration>](identityconfiguration.md) 。</span><span class="sxs-lookup"><span data-stu-id="4cb0b-134">Settings specified through this element override those specified on the service through the [\<identityConfiguration>](identityconfiguration.md) element.</span></span> <span data-ttu-id="4cb0b-135">某些处理程序 (包含若干内置处理程序类型) 可以通过元素的子元素支持其他配置 `<add>` 。</span><span class="sxs-lookup"><span data-stu-id="4cb0b-135">Some handlers (including several of the built-in handler types) can support additional configuration through a child element of the `<add>` element.</span></span> <span data-ttu-id="4cb0b-136">在处理程序上指定的设置将重写对集合或服务指定的等效设置。</span><span class="sxs-lookup"><span data-stu-id="4cb0b-136">Settings specified on a handler override equivalent settings specified on the collection or the service.</span></span>
