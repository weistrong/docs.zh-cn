---
description: 了解详细信息： <identityConfiguration>
title: <identityConfiguration>
ms.date: 03/30/2017
ms.assetid: 1db76253-07da-447b-9e7a-3705c7228cf4
author: BrucePerlerMS
ms.openlocfilehash: 987dfb006984f757ad117157e915f1909ab3a8c2
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99773402"
---
# \<identityConfiguration>

<span data-ttu-id="49944-102">指定服务级别标识设置。</span><span class="sxs-lookup"><span data-stu-id="49944-102">Specifies service-level identity settings.</span></span>

[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.identityModel>**](system-identitymodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;**\<identityConfiguration>**  

## <a name="syntax"></a><span data-ttu-id="49944-103">语法</span><span class="sxs-lookup"><span data-stu-id="49944-103">Syntax</span></span>

```xml
<system.identityModel>
  <identityConfiguration
      name=xs:string
      saveBootstrapContext=xs:boolean>
      maximumClockSkew=TimeSpan >
  </identityConfiguration>
</system.identityModel>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="49944-104">特性和元素</span><span class="sxs-lookup"><span data-stu-id="49944-104">Attributes and Elements</span></span>

<span data-ttu-id="49944-105">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="49944-105">The following sections describe attributes, child elements, and parent elements.</span></span>

### <a name="attributes"></a><span data-ttu-id="49944-106">特性</span><span class="sxs-lookup"><span data-stu-id="49944-106">Attributes</span></span>

|<span data-ttu-id="49944-107">属性</span><span class="sxs-lookup"><span data-stu-id="49944-107">Attribute</span></span>|<span data-ttu-id="49944-108">说明</span><span class="sxs-lookup"><span data-stu-id="49944-108">Description</span></span>|
|---------------|-----------------|
|<span data-ttu-id="49944-109">name</span><span class="sxs-lookup"><span data-stu-id="49944-109">name</span></span>|<span data-ttu-id="49944-110">标识配置节的名称。</span><span class="sxs-lookup"><span data-stu-id="49944-110">The name of the identity configuration section.</span></span> <span data-ttu-id="49944-111">您可以使用此名称来引用特定的配置节。</span><span class="sxs-lookup"><span data-stu-id="49944-111">You can use this name to reference a specific configuration section.</span></span> <span data-ttu-id="49944-112">如果未 `name` 指定任何属性，则节将定义默认配置。</span><span class="sxs-lookup"><span data-stu-id="49944-112">If no `name` attribute is specified, the section defines the default configuration.</span></span> <span data-ttu-id="49944-113">默认配置始终用于被动联合身份验证方案。</span><span class="sxs-lookup"><span data-stu-id="49944-113">The default configuration is always used for passive federation scenarios.</span></span> <span data-ttu-id="49944-114">有关详细信息，请参阅 [\<federationConfiguration>](federationconfiguration.md) 元素。</span><span class="sxs-lookup"><span data-stu-id="49944-114">For more information, see the [\<federationConfiguration>](federationconfiguration.md) element.</span></span>|
|<span data-ttu-id="49944-115">saveBootstrapContext</span><span class="sxs-lookup"><span data-stu-id="49944-115">saveBootstrapContext</span></span>|<span data-ttu-id="49944-116">指定是否应在会话令牌中包含启动令牌。</span><span class="sxs-lookup"><span data-stu-id="49944-116">Specifies whether bootstrap tokens should be included in the session token.</span></span> <span data-ttu-id="49944-117">还可以通过在元素上设置属性，在令牌处理程序集合上设置值 `saveBootstrapContext` [\<securityTokenHandlerConfiguration>](securitytokenhandlerconfiguration.md) 。</span><span class="sxs-lookup"><span data-stu-id="49944-117">The value may also be set on a token handler collection by setting the `saveBootstrapContext` attribute on the [\<securityTokenHandlerConfiguration>](securitytokenhandlerconfiguration.md) element.</span></span> <span data-ttu-id="49944-118">标记处理程序集合上设置的值将覆盖在服务上设置的值。</span><span class="sxs-lookup"><span data-stu-id="49944-118">A value set on the token handler collection overrides the value set on the service.</span></span>|
|<span data-ttu-id="49944-119">maximumClockSkew</span><span class="sxs-lookup"><span data-stu-id="49944-119">maximumClockSkew</span></span>|<span data-ttu-id="49944-120">一个 <xref:System.TimeSpan> ，它指定允许的最大时钟偏差。</span><span class="sxs-lookup"><span data-stu-id="49944-120">A <xref:System.TimeSpan> that specifies the maximum allowed clock skew.</span></span> <span data-ttu-id="49944-121">控制执行区分时间的操作时允许的最大时钟偏差，如验证登录会话的过期时间。</span><span class="sxs-lookup"><span data-stu-id="49944-121">Controls the maximum allowed clock skew when performing time-sensitive operations, such as validating the expiration time of a sign-in session.</span></span> <span data-ttu-id="49944-122">默认值为5分钟 "00:05:00"。</span><span class="sxs-lookup"><span data-stu-id="49944-122">The default is 5 minutes, "00:05:00".</span></span> <span data-ttu-id="49944-123">有关如何指定值的详细信息 <xref:System.TimeSpan> ，请参阅 [Timespan 值](../windows-workflow-foundation/index.md)。</span><span class="sxs-lookup"><span data-stu-id="49944-123">For more information about how to specify <xref:System.TimeSpan> values, see [Timespan Values](../windows-workflow-foundation/index.md).</span></span> <span data-ttu-id="49944-124">通过在元素上设置属性，还可以对令牌处理程序集合设置最大时钟偏差 `maximumClockSkew` [\<securityTokenHandlerConfiguration>](securitytokenhandlerconfiguration.md) 。</span><span class="sxs-lookup"><span data-stu-id="49944-124">The maximum clock skew may also be set on a token handler collection by setting the `maximumClockSkew` attribute on the [\<securityTokenHandlerConfiguration>](securitytokenhandlerconfiguration.md) element.</span></span> <span data-ttu-id="49944-125">标记处理程序集合上设置的值将覆盖在服务上设置的值。</span><span class="sxs-lookup"><span data-stu-id="49944-125">A value set on the token handler collection overrides the value set on the service.</span></span>|

### <a name="child-elements"></a><span data-ttu-id="49944-126">子元素</span><span class="sxs-lookup"><span data-stu-id="49944-126">Child Elements</span></span>

|<span data-ttu-id="49944-127">元素</span><span class="sxs-lookup"><span data-stu-id="49944-127">Element</span></span>|<span data-ttu-id="49944-128">说明</span><span class="sxs-lookup"><span data-stu-id="49944-128">Description</span></span>|
|-------------|-----------------|
|[\<caches>](caches.md)|<span data-ttu-id="49944-129">注册用于会话令牌和令牌重播检测的缓存。</span><span class="sxs-lookup"><span data-stu-id="49944-129">Registers the caches used for session tokens and token replay detection.</span></span> <span data-ttu-id="49944-130">可在服务级别或安全标记处理程序集合上指定。</span><span class="sxs-lookup"><span data-stu-id="49944-130">Can be specified at the service-level or on a security token handler collection.</span></span> <span data-ttu-id="49944-131">可选。</span><span class="sxs-lookup"><span data-stu-id="49944-131">Optional.</span></span>|
|[\<certificateValidation>](certificatevalidation.md)|<span data-ttu-id="49944-132">控制标记处理程序用于验证证书的设置。</span><span class="sxs-lookup"><span data-stu-id="49944-132">Controls the settings that token handlers use to validate certificates.</span></span> <span data-ttu-id="49944-133">可在服务级别或安全标记处理程序集合上指定。</span><span class="sxs-lookup"><span data-stu-id="49944-133">Can be specified at the service-level or on a security token handler collection.</span></span> <span data-ttu-id="49944-134">可选。</span><span class="sxs-lookup"><span data-stu-id="49944-134">Optional.</span></span>|
|[\<claimsAuthenticationManager>](claimsauthenticationmanager.md)|<span data-ttu-id="49944-135">为传入声明注册声明身份验证管理器。</span><span class="sxs-lookup"><span data-stu-id="49944-135">Registers a claims authentication manager for the incoming claims.</span></span> <span data-ttu-id="49944-136">可选。</span><span class="sxs-lookup"><span data-stu-id="49944-136">Optional.</span></span>|
|[\<claimsAuthorizationManager>](claimsauthorizationmanager.md)|<span data-ttu-id="49944-137">为传入声明注册声明授权管理器。</span><span class="sxs-lookup"><span data-stu-id="49944-137">Registers a claims authorization manager for the incoming claims.</span></span> <span data-ttu-id="49944-138">可选。</span><span class="sxs-lookup"><span data-stu-id="49944-138">Optional.</span></span>|
|[\<claimTypeRequired>](claimtyperequired.md)|<span data-ttu-id="49944-139">指定传入安全令牌所需的声明集。</span><span class="sxs-lookup"><span data-stu-id="49944-139">Specifies the set of required claims for incoming security tokens.</span></span> <span data-ttu-id="49944-140">可选。</span><span class="sxs-lookup"><span data-stu-id="49944-140">Optional.</span></span>|
|[\<securityTokenHandlers>](securitytokenhandlers.md)|<span data-ttu-id="49944-141">指定安全令牌处理程序的集合。</span><span class="sxs-lookup"><span data-stu-id="49944-141">Specifies a collection of security token handlers.</span></span> <span data-ttu-id="49944-142">可以指定零个或多个安全标记处理程序集合。</span><span class="sxs-lookup"><span data-stu-id="49944-142">Zero or more collections of security token handlers can be specified.</span></span> <span data-ttu-id="49944-143">可选。</span><span class="sxs-lookup"><span data-stu-id="49944-143">Optional.</span></span>|
|[\<tokenReplayDetection>](tokenreplaydetection.md)|<span data-ttu-id="49944-144">启用令牌重播检测并指定令牌的过期时间。</span><span class="sxs-lookup"><span data-stu-id="49944-144">Enables token replay detection and specifies the expiration time for tokens.</span></span> <span data-ttu-id="49944-145">可在服务级别或安全标记处理程序集合上指定。</span><span class="sxs-lookup"><span data-stu-id="49944-145">Can be specified at the service-level or on a security token handler collection.</span></span> <span data-ttu-id="49944-146">可选。</span><span class="sxs-lookup"><span data-stu-id="49944-146">Optional.</span></span>|

### <a name="parent-elements"></a><span data-ttu-id="49944-147">父元素</span><span class="sxs-lookup"><span data-stu-id="49944-147">Parent Elements</span></span>

|<span data-ttu-id="49944-148">元素</span><span class="sxs-lookup"><span data-stu-id="49944-148">Element</span></span>|<span data-ttu-id="49944-149">说明</span><span class="sxs-lookup"><span data-stu-id="49944-149">Description</span></span>|
|-------------|-----------------|
|[\<system.identityModel>](system-identitymodel.md)|<span data-ttu-id="49944-150">提供用于在应用程序中启用 Windows Identity Foundation (WIF) 选项的配置。</span><span class="sxs-lookup"><span data-stu-id="49944-150">Provides configuration for enabling Windows Identity Foundation (WIF) options in applications.</span></span>|

## <a name="remarks"></a><span data-ttu-id="49944-151">备注</span><span class="sxs-lookup"><span data-stu-id="49944-151">Remarks</span></span>

<span data-ttu-id="49944-152">可以定义多个标识配置，每个配置都具有唯一的名称。</span><span class="sxs-lookup"><span data-stu-id="49944-152">Multiple identity configurations may be defined, each with a unique name.</span></span> <span data-ttu-id="49944-153">此行为如下所示：</span><span class="sxs-lookup"><span data-stu-id="49944-153">The behavior is as follows:</span></span>

1. <span data-ttu-id="49944-154">如果未 `<identityConfiguration>` 指定元素，则为。</span><span class="sxs-lookup"><span data-stu-id="49944-154">If no `<identityConfiguration>` element is specified.</span></span> <span data-ttu-id="49944-155">默认标识配置是在运行时创建的，并使用默认值进行填充。</span><span class="sxs-lookup"><span data-stu-id="49944-155">A default identity configuration is created at runtime and populated with default values.</span></span>

2. <span data-ttu-id="49944-156">如果指定单个 `<identityConfiguration>` 元素，则为。</span><span class="sxs-lookup"><span data-stu-id="49944-156">If a single `<identityConfiguration>` element is specified.</span></span> <span data-ttu-id="49944-157">这是默认的标识配置。</span><span class="sxs-lookup"><span data-stu-id="49944-157">It is the default identity configuration.</span></span> <span data-ttu-id="49944-158">这并不重要。</span><span class="sxs-lookup"><span data-stu-id="49944-158">It does not matter whether it is named or unnamed.</span></span>

3. <span data-ttu-id="49944-159">如果 `<identityConfiguration>` 指定了多个元素。</span><span class="sxs-lookup"><span data-stu-id="49944-159">If multiple `<identityConfiguration>` elements are specified.</span></span> <span data-ttu-id="49944-160">未命名元素指定默认标识配置。</span><span class="sxs-lookup"><span data-stu-id="49944-160">The unnamed element specifies the default identity configuration.</span></span> <span data-ttu-id="49944-161">建议在指定多个 `<identityConfiguration>` 元素时，其中一项应为未命名元素。</span><span class="sxs-lookup"><span data-stu-id="49944-161">It is recommended that when you specify multiple `<identityConfiguration>` elements, one of them should be unnamed.</span></span>

> [!WARNING]
> <span data-ttu-id="49944-162">如果指定多个 `<identityConfiguration>` 元素，则其中一个元素应该是未命名元素。</span><span class="sxs-lookup"><span data-stu-id="49944-162">If you specify multiple `<identityConfiguration>` elements, one of them should be unnamed.</span></span> <span data-ttu-id="49944-163">未命名的元素将是默认的标识配置。</span><span class="sxs-lookup"><span data-stu-id="49944-163">The unnamed element will be the default identity configuration.</span></span>

 <span data-ttu-id="49944-164">元素中指定的某些设置 `<identityConfiguration>` 可由安全令牌处理程序集合上的设置重写，或由单个安全令牌处理程序上的设置重写。</span><span class="sxs-lookup"><span data-stu-id="49944-164">Some of the settings specified in the `<identityConfiguration>` element can be overridden by settings on a security token handler collection or by settings on individual security token handlers.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="49944-165">当使用 <xref:System.IdentityModel.Services.ClaimsPrincipalPermission> 或 <xref:System.IdentityModel.Services.ClaimsPrincipalPermissionAttribute> 类在代码中提供基于声明的访问控制时，元素引用的标识配置将 `<federationConfiguration>` 配置用于做出授权决定的声明授权管理器和策略。</span><span class="sxs-lookup"><span data-stu-id="49944-165">When using the <xref:System.IdentityModel.Services.ClaimsPrincipalPermission> or the <xref:System.IdentityModel.Services.ClaimsPrincipalPermissionAttribute> class to provide claims-based access control in your code, the identity configuration that is referenced by the `<federationConfiguration>` element configures the claims authorization manager and policy that is used to make authorization decisions.</span></span> <span data-ttu-id="49944-166">即使在非被动 Web 应用场景的情况下（例如 Windows Communication Foundation (WCF) 应用程序或不是基于 Web 的应用程序），也是如此。</span><span class="sxs-lookup"><span data-stu-id="49944-166">This is true, even in scenarios that are not passive Web scenarios, for example Windows Communication Foundation (WCF) applications or an application that is not Web-based.</span></span> <span data-ttu-id="49944-167">如果应用程序不是被动 Web 应用程序，则 [\<claimsAuthorizationManager>](claimsauthorizationmanager.md) 元素 (及其子策略元素，如果只应用了引用的标识配置) 。</span><span class="sxs-lookup"><span data-stu-id="49944-167">If the application is not a passive Web application, the [\<claimsAuthorizationManager>](claimsauthorizationmanager.md) element (and its child policy elements, if present) of the referenced identity configuration are the only settings applied.</span></span> <span data-ttu-id="49944-168">忽略所有其他设置。</span><span class="sxs-lookup"><span data-stu-id="49944-168">All other settings are ignored.</span></span> <span data-ttu-id="49944-169">有关详细信息，请参阅 [\<federationConfiguration>](federationconfiguration.md) 元素。</span><span class="sxs-lookup"><span data-stu-id="49944-169">For more information, see the [\<federationConfiguration>](federationconfiguration.md) element.</span></span>

<span data-ttu-id="49944-170">`<identityConfiguration>`元素由 <xref:System.IdentityModel.Configuration.IdentityConfigurationElement> 类表示。</span><span class="sxs-lookup"><span data-stu-id="49944-170">The `<identityConfiguration>` element is represented by the <xref:System.IdentityModel.Configuration.IdentityConfigurationElement> class.</span></span> <span data-ttu-id="49944-171">标识配置部分由 <xref:System.IdentityModel.Configuration.IdentityConfiguration> 类表示。</span><span class="sxs-lookup"><span data-stu-id="49944-171">An identity configuration section is represented by the <xref:System.IdentityModel.Configuration.IdentityConfiguration> class.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="49944-172">将以下元素指定为元素的子元素 `<identityConfiguration>` 已被弃用，但仍支持此行为以实现向后兼容性。</span><span class="sxs-lookup"><span data-stu-id="49944-172">Specifying the following elements as child elements of the `<identityConfiguration>` element has been deprecated, although the behavior is still supported for backward compatibility.</span></span> <span data-ttu-id="49944-173">应改为在元素下指定这些元素 [\<securityTokenHandlerConfiguration>](securitytokenhandlerconfiguration.md) 。</span><span class="sxs-lookup"><span data-stu-id="49944-173">These elements should, instead, be specified under the [\<securityTokenHandlerConfiguration>](securitytokenhandlerconfiguration.md) element.</span></span>
>
> - [\<audienceUris>](audienceuris.md)
> - [\<issuerNameRegistry>](issuernameregistry.md)
> - [\<issuerTokenResolver>](issuertokenresolver.md)
> - [\<serviceTokenResolver>](servicetokenresolver.md)

## <a name="example"></a><span data-ttu-id="49944-174">示例</span><span class="sxs-lookup"><span data-stu-id="49944-174">Example</span></span>

<span data-ttu-id="49944-175">以下示例创建名为 "alternateConfiguration" 的标识配置。</span><span class="sxs-lookup"><span data-stu-id="49944-175">The following example creates an identity configuration named "alternateConfiguration".</span></span> <span data-ttu-id="49944-176">标识配置指定默认设置。</span><span class="sxs-lookup"><span data-stu-id="49944-176">The identity configuration specifies default settings.</span></span>

```xml
<system.identityModel>
    <identityConfiguration name="alternateConfiguration"/>
</system.identityModel>
```

## <a name="see-also"></a><span data-ttu-id="49944-177">请参阅</span><span class="sxs-lookup"><span data-stu-id="49944-177">See also</span></span>

- <xref:System.IdentityModel.Configuration.IdentityConfiguration>
- <xref:System.IdentityModel.Configuration.IdentityConfigurationElement>
