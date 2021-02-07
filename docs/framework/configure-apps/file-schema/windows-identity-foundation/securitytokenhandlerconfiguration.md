---
description: 了解详细信息： <securityTokenHandlerConfiguration>
title: <securityTokenHandlerConfiguration>
ms.date: 03/30/2017
ms.assetid: 28724cc6-020c-4a06-9a1f-d7594f315019
author: BrucePerlerMS
ms.openlocfilehash: 8c014d971d3e8cc640a3b7042e3a0266d902de7d
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99698305"
---
# \<securityTokenHandlerConfiguration>

<span data-ttu-id="c5d44-102">为标记处理程序的集合提供配置。</span><span class="sxs-lookup"><span data-stu-id="c5d44-102">Provides configuration for the collection of token handlers.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.identityModel>**](system-identitymodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<identityConfiguration>**](identityconfiguration.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<securityTokenHandlers>**](securitytokenhandlers.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<securityTokenHandlerConfiguration>**  
  
## <a name="syntax"></a><span data-ttu-id="c5d44-103">语法</span><span class="sxs-lookup"><span data-stu-id="c5d44-103">Syntax</span></span>  
  
```xml  
<system.identityModel>  
  <identityConfiguration>  
    <securityTokenHandlers>  
      <securityTokenHandlerConfiguration saveBootstrapContext=xs:boolean  
          maximumClockSkew=TimeSpan>  
      </securityTokenHandlerConfiguration>  
    </securityTokenHandlers>  
  </identityConfiguration>  
</system.identityModel>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="c5d44-104">特性和元素</span><span class="sxs-lookup"><span data-stu-id="c5d44-104">Attributes and Elements</span></span>  

 <span data-ttu-id="c5d44-105">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="c5d44-105">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="c5d44-106">特性</span><span class="sxs-lookup"><span data-stu-id="c5d44-106">Attributes</span></span>  
  
|<span data-ttu-id="c5d44-107">属性</span><span class="sxs-lookup"><span data-stu-id="c5d44-107">Attribute</span></span>|<span data-ttu-id="c5d44-108">说明</span><span class="sxs-lookup"><span data-stu-id="c5d44-108">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="c5d44-109">saveBootstrapContext</span><span class="sxs-lookup"><span data-stu-id="c5d44-109">saveBootstrapContext</span></span>|<span data-ttu-id="c5d44-110">指定是否应在会话令牌中包含启动令牌。</span><span class="sxs-lookup"><span data-stu-id="c5d44-110">Specifies whether bootstrap tokens should be included in the session token.</span></span> <span data-ttu-id="c5d44-111">还可以通过在元素上设置属性，在令牌处理程序集合上设置值 `saveBootstrapContext` [\<identityConfiguration>](identityconfiguration.md) 。</span><span class="sxs-lookup"><span data-stu-id="c5d44-111">The value may also be set on a token handler collection by setting the `saveBootstrapContext` attribute on the [\<identityConfiguration>](identityconfiguration.md) element.</span></span> <span data-ttu-id="c5d44-112">标记处理程序集合上设置的值将覆盖在服务上设置的值。</span><span class="sxs-lookup"><span data-stu-id="c5d44-112">A value set on the token handler collection overrides the value set on the service.</span></span>|  
|<span data-ttu-id="c5d44-113">maximumClockSkew</span><span class="sxs-lookup"><span data-stu-id="c5d44-113">maximumClockSkew</span></span>|<span data-ttu-id="c5d44-114">一个 <xref:System.TimeSpan> ，它指定允许的最大时钟偏差。</span><span class="sxs-lookup"><span data-stu-id="c5d44-114">A <xref:System.TimeSpan> that specifies the maximum allowed clock skew.</span></span> <span data-ttu-id="c5d44-115">控制执行区分时间的操作时允许的最大时钟偏差，如验证登录会话的过期时间。</span><span class="sxs-lookup"><span data-stu-id="c5d44-115">Controls the maximum allowed clock skew when performing time-sensitive operations, such as validating the expiration time of a sign-in session.</span></span> <span data-ttu-id="c5d44-116">默认值为5分钟 "00:05:00"。</span><span class="sxs-lookup"><span data-stu-id="c5d44-116">The default is 5 minutes, "00:05:00".</span></span> <span data-ttu-id="c5d44-117">有关如何指定值的详细信息 <xref:System.TimeSpan> ，请参阅 [Timespan 值](../windows-workflow-foundation/index.md)。</span><span class="sxs-lookup"><span data-stu-id="c5d44-117">For more information about how to specify <xref:System.TimeSpan> values, see [Timespan Values](../windows-workflow-foundation/index.md).</span></span> <span data-ttu-id="c5d44-118">通过在元素上设置属性，还可以在服务级别设置最大时钟偏差 `maximumClockSkew` [\<identityConfiguration>](identityconfiguration.md) 。</span><span class="sxs-lookup"><span data-stu-id="c5d44-118">The maximum clock skew may also be set at the service level by setting the `maximumClockSkew` attribute on the [\<identityConfiguration>](identityconfiguration.md) element.</span></span> <span data-ttu-id="c5d44-119">标记处理程序集合上设置的值将覆盖在服务上设置的值。</span><span class="sxs-lookup"><span data-stu-id="c5d44-119">A value set on the token handler collection overrides the value set on the service.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="c5d44-120">子元素</span><span class="sxs-lookup"><span data-stu-id="c5d44-120">Child Elements</span></span>  
  
|<span data-ttu-id="c5d44-121">元素</span><span class="sxs-lookup"><span data-stu-id="c5d44-121">Element</span></span>|<span data-ttu-id="c5d44-122">说明</span><span class="sxs-lookup"><span data-stu-id="c5d44-122">Description</span></span>|  
|-------------|-----------------|  
|[\<audienceUris>](audienceuris.md)|<span data-ttu-id="c5d44-123">指定作为此信赖方的可接受标识符的 Uri 集。</span><span class="sxs-lookup"><span data-stu-id="c5d44-123">Specifies the set of URIs that are acceptable identifiers of this relying party.</span></span> <span data-ttu-id="c5d44-124">可选。</span><span class="sxs-lookup"><span data-stu-id="c5d44-124">Optional.</span></span>|  
|[\<caches>](caches.md)|<span data-ttu-id="c5d44-125">注册用于会话令牌和令牌重播检测的缓存。</span><span class="sxs-lookup"><span data-stu-id="c5d44-125">Registers the caches used for session tokens and token replay detection.</span></span> <span data-ttu-id="c5d44-126">可在服务级别或安全标记处理程序集合上指定。</span><span class="sxs-lookup"><span data-stu-id="c5d44-126">Can be specified at the service-level or on a security token handler collection.</span></span> <span data-ttu-id="c5d44-127">可选。</span><span class="sxs-lookup"><span data-stu-id="c5d44-127">Optional.</span></span>|  
|[\<certificateValidation>](certificatevalidation.md)|<span data-ttu-id="c5d44-128">控制标记处理程序用于验证证书的设置。</span><span class="sxs-lookup"><span data-stu-id="c5d44-128">Controls the settings that token handlers use to validate certificates.</span></span> <span data-ttu-id="c5d44-129">可在服务级别或安全标记处理程序集合上指定。</span><span class="sxs-lookup"><span data-stu-id="c5d44-129">Can be specified at the service-level or on a security token handler collection.</span></span> <span data-ttu-id="c5d44-130">如果为特定处理程序配置了其自己的验证程序，则会重写这些设置。</span><span class="sxs-lookup"><span data-stu-id="c5d44-130">These settings are overridden if a specific handler is configured with its own validator.</span></span> <span data-ttu-id="c5d44-131">可选。</span><span class="sxs-lookup"><span data-stu-id="c5d44-131">Optional.</span></span>|  
|[\<issuerNameRegistry>](issuernameregistry.md)|<span data-ttu-id="c5d44-132">配置标记处理程序集合中的处理程序使用的颁发者名称注册表。</span><span class="sxs-lookup"><span data-stu-id="c5d44-132">Configures the issuer name registry that is used by handlers in the token handler collection.</span></span> <span data-ttu-id="c5d44-133">可选。</span><span class="sxs-lookup"><span data-stu-id="c5d44-133">Optional.</span></span>|  
|[\<issuerTokenResolver>](issuertokenresolver.md)|<span data-ttu-id="c5d44-134">注册由标记处理程序集合中的处理程序使用的颁发者令牌解析程序。</span><span class="sxs-lookup"><span data-stu-id="c5d44-134">Registers the issuer token resolver that is used by handlers in the token handler collection.</span></span> <span data-ttu-id="c5d44-135">颁发者令牌解析器用于解析传入令牌和消息的签名令牌。</span><span class="sxs-lookup"><span data-stu-id="c5d44-135">The issuer token resolver is used to resolve the signing token on incoming tokens and messages.</span></span> <span data-ttu-id="c5d44-136">可选。</span><span class="sxs-lookup"><span data-stu-id="c5d44-136">Optional.</span></span>|  
|[\<serviceTokenResolver>](servicetokenresolver.md)|<span data-ttu-id="c5d44-137">注册令牌处理程序集合中的处理程序使用的服务令牌解析程序。</span><span class="sxs-lookup"><span data-stu-id="c5d44-137">Registers the service token resolver that is used by handlers in the token handler collection.</span></span> <span data-ttu-id="c5d44-138">服务令牌解析器用于解析传入令牌和消息的加密令牌。</span><span class="sxs-lookup"><span data-stu-id="c5d44-138">The service token resolver is used to resolve the encryption token on incoming tokens and messages.</span></span> <span data-ttu-id="c5d44-139">可选。</span><span class="sxs-lookup"><span data-stu-id="c5d44-139">Optional.</span></span>|  
|[\<tokenReplayDetection>](tokenreplaydetection.md)|<span data-ttu-id="c5d44-140">启用令牌重播检测并指定令牌的过期时间。</span><span class="sxs-lookup"><span data-stu-id="c5d44-140">Enables token replay detection and specifies the expiration time for tokens.</span></span> <span data-ttu-id="c5d44-141">可在服务级别或安全标记处理程序集合上指定。</span><span class="sxs-lookup"><span data-stu-id="c5d44-141">Can be specified at the service-level or on a security token handler collection.</span></span> <span data-ttu-id="c5d44-142">可选。</span><span class="sxs-lookup"><span data-stu-id="c5d44-142">Optional.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="c5d44-143">父元素</span><span class="sxs-lookup"><span data-stu-id="c5d44-143">Parent Elements</span></span>  
  
|<span data-ttu-id="c5d44-144">元素</span><span class="sxs-lookup"><span data-stu-id="c5d44-144">Element</span></span>|<span data-ttu-id="c5d44-145">说明</span><span class="sxs-lookup"><span data-stu-id="c5d44-145">Description</span></span>|  
|-------------|-----------------|  
|[\<securityTokenHandlers>](securitytokenhandlers.md)|<span data-ttu-id="c5d44-146">指定注册到终结点的安全令牌处理程序的集合。</span><span class="sxs-lookup"><span data-stu-id="c5d44-146">Specifies a collection of security token handlers that are registered with the endpoint.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="c5d44-147">备注</span><span class="sxs-lookup"><span data-stu-id="c5d44-147">Remarks</span></span>  

 <span data-ttu-id="c5d44-148">本部分提供对象的属性值 <xref:System.IdentityModel.Tokens.SecurityTokenHandlerConfiguration> 。</span><span class="sxs-lookup"><span data-stu-id="c5d44-148">This section provides property values for a <xref:System.IdentityModel.Tokens.SecurityTokenHandlerConfiguration> object.</span></span> <span data-ttu-id="c5d44-149">此部分中配置的设置将覆盖在服务上配置的设置。</span><span class="sxs-lookup"><span data-stu-id="c5d44-149">Settings configured in this section override those configured on the service.</span></span> <span data-ttu-id="c5d44-150">其中的某些设置可以通过在将处理程序添加到安全标记处理程序集合时指定的设置重写。</span><span class="sxs-lookup"><span data-stu-id="c5d44-150">Some of these settings can, in turn, be overridden by settings that are specified when a handler is added to the security token handler collection.</span></span>  
  
## <a name="example"></a><span data-ttu-id="c5d44-151">示例</span><span class="sxs-lookup"><span data-stu-id="c5d44-151">Example</span></span>  
  
```xml  
<system.identityModel>  
  <identityConfiguration>  
    <securityTokenHandlers>
      <securityTokenHandlerConfiguration>  
  
        <audienceUris>  
          <clear/>  
          <add value="http://www.example.com/myapp/" />  
        </audienceUris>  
  
        <issuerNameRegistry type="System.IdentityModel.Tokens.ConfigurationBasedIssuerNameRegistry, System.IdentityModel">  
          <trustedIssuers>  
            <add thumbprint="97249e1a … 4c9158de" name="contoso.com" />  
          </trustedIssuers>  
        </issuerNameRegistry>  
  
        <issuerTokenResolver type="MyNamespace.CustomTokenResolver, MyAssembly" />  
  
        <serviceTokenResolver type="MyNamespace.CustomTokenResolver, MyAssembly" />  
  
      </securityTokenHandlerConfiguration>  
    </securityTokenHandlers>  
  </identityConfiguration>  
</system.identityModel>  
```
