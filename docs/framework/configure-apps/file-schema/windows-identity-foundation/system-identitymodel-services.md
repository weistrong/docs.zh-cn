---
description: 了解详细信息： <System.identitymodel>
title: <system.identityModel.services>
ms.date: 03/30/2017
ms.assetid: fa1624dd-2d74-4ae3-942e-498cee261ac5
author: BrucePerlerMS
ms.openlocfilehash: 037a96c2620e06ef6aed85d1dbaba62aca72e9eb
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99786546"
---
# \<system.identityModel.services>

<span data-ttu-id="fd3f6-103">使用 WS-Federation 协议进行身份验证的配置节。</span><span class="sxs-lookup"><span data-stu-id="fd3f6-103">Configuration section for authentication using the WS-Federation protocol.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;**\<system.identityModel.services>**  
  
## <a name="syntax"></a><span data-ttu-id="fd3f6-104">语法</span><span class="sxs-lookup"><span data-stu-id="fd3f6-104">Syntax</span></span>  
  
```xml  
<system.identityModel.services>  
  <federationConfiguration name=xs:string identityConfigurationName=xs:string>  
  </federationConfiguration>  
</system.identityModel.services>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="fd3f6-105">特性和元素</span><span class="sxs-lookup"><span data-stu-id="fd3f6-105">Attributes and Elements</span></span>  

 <span data-ttu-id="fd3f6-106">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="fd3f6-106">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="fd3f6-107">特性</span><span class="sxs-lookup"><span data-stu-id="fd3f6-107">Attributes</span></span>  

 <span data-ttu-id="fd3f6-108">无</span><span class="sxs-lookup"><span data-stu-id="fd3f6-108">None</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="fd3f6-109">子元素</span><span class="sxs-lookup"><span data-stu-id="fd3f6-109">Child Elements</span></span>  
  
|<span data-ttu-id="fd3f6-110">元素</span><span class="sxs-lookup"><span data-stu-id="fd3f6-110">Element</span></span>|<span data-ttu-id="fd3f6-111">说明</span><span class="sxs-lookup"><span data-stu-id="fd3f6-111">Description</span></span>|  
|-------------|-----------------|  
|[\<federationConfiguration>](federationconfiguration.md)|<span data-ttu-id="fd3f6-112">包含配置 <xref:System.IdentityModel.Services.WSFederationAuthenticationModule> (WSFAM) 和 <xref:System.IdentityModel.Services.SessionAuthenticationModule> (SAM) HTTP 模块的设置。</span><span class="sxs-lookup"><span data-stu-id="fd3f6-112">Contains the settings that configure the <xref:System.IdentityModel.Services.WSFederationAuthenticationModule> (WSFAM) and the <xref:System.IdentityModel.Services.SessionAuthenticationModule> (SAM) HTTP modules.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="fd3f6-113">父元素</span><span class="sxs-lookup"><span data-stu-id="fd3f6-113">Parent Elements</span></span>  

 <span data-ttu-id="fd3f6-114">无</span><span class="sxs-lookup"><span data-stu-id="fd3f6-114">None</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="fd3f6-115">备注</span><span class="sxs-lookup"><span data-stu-id="fd3f6-115">Remarks</span></span>  

 <span data-ttu-id="fd3f6-116">将 `<system.identityModel.services>` 部分添加到应用程序的配置文件，以提供 SAM 和 WSFAM 的设置。</span><span class="sxs-lookup"><span data-stu-id="fd3f6-116">Add a `<system.identityModel.services>` section to your application’s configuration file to provide settings for the SAM and WSFAM.</span></span>  
  
> [!IMPORTANT]
> <span data-ttu-id="fd3f6-117">当使用 <xref:System.IdentityModel.Services.ClaimsPrincipalPermission> 或 <xref:System.IdentityModel.Services.ClaimsPrincipalPermissionAttribute> 类在代码中提供基于声明的访问控制时，将 <xref:System.Security.Claims.ClaimsAuthorizationManager> 通过 `<identityConfiguration>` `<federationConfiguration>` 此部分中的元素隐式或显式引用的元素来配置用于做出授权决策的声明授权管理器 () 和策略。</span><span class="sxs-lookup"><span data-stu-id="fd3f6-117">When using the <xref:System.IdentityModel.Services.ClaimsPrincipalPermission> or the <xref:System.IdentityModel.Services.ClaimsPrincipalPermissionAttribute> class to provide claims-based access control in your code, the claims authorization manager (<xref:System.Security.Claims.ClaimsAuthorizationManager>) and policy that is used to make authorization decisions are configured through an `<identityConfiguration>` element that is implicitly or explicitly referenced from a `<federationConfiguration>` element in this section.</span></span> <span data-ttu-id="fd3f6-118">有关详细信息，请参阅元素下的 " **备注** " [\<federationConfiguration>](federationconfiguration.md) 。</span><span class="sxs-lookup"><span data-stu-id="fd3f6-118">For more information, see the **Remarks** under the [\<federationConfiguration>](federationconfiguration.md) element.</span></span>  
  
 <span data-ttu-id="fd3f6-119">`<system.identityModel.services>`部分由 <xref:System.IdentityModel.Services.Configuration.SystemIdentityModelServicesSection> 类表示。</span><span class="sxs-lookup"><span data-stu-id="fd3f6-119">The `<system.identityModel.services>` section is represented by the <xref:System.IdentityModel.Services.Configuration.SystemIdentityModelServicesSection> class.</span></span> <span data-ttu-id="fd3f6-120">`<federationConfiguration>`在部分中配置的子元素的集合由 <xref:System.IdentityModel.Services.Configuration.FederationConfigurationElementCollection> 类表示。</span><span class="sxs-lookup"><span data-stu-id="fd3f6-120">The collection of child `<federationConfiguration>` elements configured in the section is represented by the <xref:System.IdentityModel.Services.Configuration.FederationConfigurationElementCollection> class.</span></span>  
  
## <a name="example"></a><span data-ttu-id="fd3f6-121">示例</span><span class="sxs-lookup"><span data-stu-id="fd3f6-121">Example</span></span>  

 <span data-ttu-id="fd3f6-122">下面的 XML 演示如何将节添加 `<system.identityModel.services>` 到配置文件。</span><span class="sxs-lookup"><span data-stu-id="fd3f6-122">The following XML shows how to add a `<system.identityModel.services>` section to a configuration file.</span></span> <span data-ttu-id="fd3f6-123">必须首先为节和部分添加节声明 `<system.identityModel.services>` `<system.identityModel>` 。</span><span class="sxs-lookup"><span data-stu-id="fd3f6-123">You must first add section declarations for both the `<system.identityModel.services>` section and the `<system.identityModel>` sections.</span></span> <span data-ttu-id="fd3f6-124"> (在添加节时 `<system.identityModel.services>` ，还应为节添加声明， `<system.identityModel>` 以确保 `<identityConfiguration>` 运行时可根据需要创建默认节 ) 。在添加部分声明后，可以在元素下配置联合身份验证设置 `<system.identityModel.services>` 。</span><span class="sxs-lookup"><span data-stu-id="fd3f6-124">(When you add a `<system.identityModel.services>` section, you should also add a declaration for the `<system.identityModel>` section to ensure that a default `<identityConfiguration>` section can be created by the runtime if necessary.) After the section declarations have been added, you can configure federated authentication settings under the `<system.identityModel.services>` element.</span></span>  
  
```xml  
<configuration>  
  <configSections>  
    <section name="system.identityModel" type="System.IdentityModel.Configuration.SystemIdentityModelSection, System.IdentityModel, Version=4.0.0.0, Culture=neutral, PublicKeyToken=B77A5C561934E089" />  
    <section name="system.identityModel.services" type="System.IdentityModel.Services.Configuration.SystemIdentityModelServicesSection, System.IdentityModel.Services, Version=4.0.0.0, Culture=neutral, PublicKeyToken=B77A5C561934E089" />  
  </configSections>  
  
  <!-- Additional elements (not shown) -->  
  
  <system.identityModel.services>  
    <federationConfiguration>  
      <wsFederation passiveRedirectEnabled="true"
        issuer="http://localhost:15839/wsFederationSTS/Issue"
        realm="http://localhost:50969/" reply="http://localhost:50969/"
        requireHttps="false"
        signOutReply="http://localhost:50969/SignedOutPage.html"
        signOutQueryString="Param1=value2&Param2=value2"
        persistentCookiesOnPassiveRedirects="true" />  
      <cookieHandler requireSsl="false" />  
    </federationConfiguration>  
  </system.identityModel.services>  
  
</configuration>  
```
