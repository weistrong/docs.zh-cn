---
description: 了解详细信息： <samlSecurityTokenRequirement>
title: <samlSecurityTokenRequirement>
ms.date: 03/30/2017
ms.assetid: 09202d12-88d3-49cc-953b-703bcc1690eb
author: BrucePerlerMS
ms.openlocfilehash: 21e584480aae6f620e0809be77e02789536db426
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99786559"
---
# \<samlSecurityTokenRequirement>

<span data-ttu-id="806e2-102">为 <xref:System.IdentityModel.Tokens.SamlSecurityTokenHandler> 类、 <xref:System.IdentityModel.Tokens.Saml2SecurityTokenHandler> 类或其中任何一个类的派生类提供配置。</span><span class="sxs-lookup"><span data-stu-id="806e2-102">Provides configuration for the <xref:System.IdentityModel.Tokens.SamlSecurityTokenHandler> class, the <xref:System.IdentityModel.Tokens.Saml2SecurityTokenHandler> class, or a derived class of either of these classes.</span></span> <span data-ttu-id="806e2-103">由类表示 <xref:System.IdentityModel.Tokens.SamlSecurityTokenRequirement> 。</span><span class="sxs-lookup"><span data-stu-id="806e2-103">Represented by the <xref:System.IdentityModel.Tokens.SamlSecurityTokenRequirement> class.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.identityModel>**](system-identitymodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<identityConfiguration>**](identityconfiguration.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<securityTokenHandlers>**](securitytokenhandlers.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<add>**](add.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<samlSecurityTokenRequirement>**  
  
## <a name="syntax"></a><span data-ttu-id="806e2-104">语法</span><span class="sxs-lookup"><span data-stu-id="806e2-104">Syntax</span></span>  
  
```xml  
<system.identityModel>  
  <identityConfiguration>  
    <securityTokenHandlers>  
      <add>  
        <samlSecurityTokenRequirement
            issuerCertificateValidationMode="None||ChainTrust||PeerTrust||PeerOrChainTrust||Custom"  
            issuerCertificateRevocationMode="NoCheck||Offline||Online"  
            issuerCertificateTrustedStoreLocation="CurrentLocation||LocalMachine"  
            issuerCertificateValidator="Namespace.Class Assembly"  
            mapToWindows=xs:boolean  
          <nameClaimType value=xs:string />  
          <roleClaimType value=xs:string />  
        </samlSecurityTokenRequirement>  
      </add>  
    </securityTokenHandlers>  
  </identityConfiguration>  
</system.identityModel>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="806e2-105">特性和元素</span><span class="sxs-lookup"><span data-stu-id="806e2-105">Attributes and Elements</span></span>  

 <span data-ttu-id="806e2-106">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="806e2-106">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="806e2-107">特性</span><span class="sxs-lookup"><span data-stu-id="806e2-107">Attributes</span></span>  
  
|<span data-ttu-id="806e2-108">属性</span><span class="sxs-lookup"><span data-stu-id="806e2-108">Attribute</span></span>|<span data-ttu-id="806e2-109">说明</span><span class="sxs-lookup"><span data-stu-id="806e2-109">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="806e2-110">mapToWindows</span><span class="sxs-lookup"><span data-stu-id="806e2-110">mapToWindows</span></span>|<span data-ttu-id="806e2-111">指定令牌处理程序是否应使用传入 UPN 声明将验证令牌映射到 Windows 帐户。</span><span class="sxs-lookup"><span data-stu-id="806e2-111">Specifies whether the token handler should map the validating token to a Windows account by using the incoming UPN claim.</span></span> <span data-ttu-id="806e2-112">默认值为“false”。</span><span class="sxs-lookup"><span data-stu-id="806e2-112">The default is "false".</span></span>|  
|<span data-ttu-id="806e2-113">issuerCertificateRevocationMode</span><span class="sxs-lookup"><span data-stu-id="806e2-113">issuerCertificateRevocationMode</span></span>|<span data-ttu-id="806e2-114">一个 <xref:System.Security.Cryptography.X509Certificates.X509RevocationMode> 值，该值指定要用于 x.509 证书的吊销模式。</span><span class="sxs-lookup"><span data-stu-id="806e2-114">An <xref:System.Security.Cryptography.X509Certificates.X509RevocationMode> value that specifies the revocation mode to use for the X.509 certificate.</span></span> <span data-ttu-id="806e2-115">默认值为 "Online"。</span><span class="sxs-lookup"><span data-stu-id="806e2-115">The default value is "Online".</span></span>|  
|<span data-ttu-id="806e2-116">issuerCertificateValidationMode</span><span class="sxs-lookup"><span data-stu-id="806e2-116">issuerCertificateValidationMode</span></span>|<span data-ttu-id="806e2-117">一个 <xref:System.ServiceModel.Security.X509CertificateValidationMode> 值，该值指定要用于 x.509 证书的验证模式。</span><span class="sxs-lookup"><span data-stu-id="806e2-117">An <xref:System.ServiceModel.Security.X509CertificateValidationMode> value that specifies the validation mode to use for the X.509 certificate.</span></span> <span data-ttu-id="806e2-118">默认值为 "PeerOrChainTrust"。</span><span class="sxs-lookup"><span data-stu-id="806e2-118">The default value is "PeerOrChainTrust".</span></span>|  
|<span data-ttu-id="806e2-119">issuerCertificateTrustedStoreLocation</span><span class="sxs-lookup"><span data-stu-id="806e2-119">issuerCertificateTrustedStoreLocation</span></span>|<span data-ttu-id="806e2-120">一个 <xref:System.Security.Cryptography.X509Certificates.StoreLocation> 值，该值指定 x.509 证书存储区。</span><span class="sxs-lookup"><span data-stu-id="806e2-120">A <xref:System.Security.Cryptography.X509Certificates.StoreLocation> value that specifies the X.509 certificate store.</span></span> <span data-ttu-id="806e2-121">默认值为 "LocalMachine"。</span><span class="sxs-lookup"><span data-stu-id="806e2-121">The default value is "LocalMachine".</span></span>|  
|<span data-ttu-id="806e2-122">issuerCertificateValidator</span><span class="sxs-lookup"><span data-stu-id="806e2-122">issuerCertificateValidator</span></span>|<span data-ttu-id="806e2-123">派生自的自定义类型 <xref:System.IdentityModel.Selectors.X509CertificateValidator> 。</span><span class="sxs-lookup"><span data-stu-id="806e2-123">A custom type that derives from <xref:System.IdentityModel.Selectors.X509CertificateValidator>.</span></span> <span data-ttu-id="806e2-124">如果该 `issuerCertificateValidationMode` 属性为 "Custom"，则此类型的实例将用于颁发者证书验证。</span><span class="sxs-lookup"><span data-stu-id="806e2-124">If the `issuerCertificateValidationMode` attribute is "Custom", an instance of this type is used for issuer certificate validation.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="806e2-125">子元素</span><span class="sxs-lookup"><span data-stu-id="806e2-125">Child Elements</span></span>  
  
|<span data-ttu-id="806e2-126">元素</span><span class="sxs-lookup"><span data-stu-id="806e2-126">Element</span></span>|<span data-ttu-id="806e2-127">说明</span><span class="sxs-lookup"><span data-stu-id="806e2-127">Description</span></span>|  
|-------------|-----------------|  
|[\<nameClaimType>](nameclaimtype.md)|<span data-ttu-id="806e2-128">设置指定属性的声明类型 <xref:System.Security.Principal.IIdentity.Name%2A> 。</span><span class="sxs-lookup"><span data-stu-id="806e2-128">Sets the claim type that specifies the <xref:System.Security.Principal.IIdentity.Name%2A> property.</span></span>|  
|[\<roleClaimType>](roleclaimtype.md)|<span data-ttu-id="806e2-129">指定声明类型，该声明类型定义 <xref:System.Security.Claims.ClaimsIdentity> 由标记处理程序的方法返回的对象集合中的角色类型声明 <xref:System.IdentityModel.Tokens.SecurityTokenHandler.ValidateToken%2A> 。</span><span class="sxs-lookup"><span data-stu-id="806e2-129">Specifies the claim type that defines the role type claims in the collection of <xref:System.Security.Claims.ClaimsIdentity> objects returned by the <xref:System.IdentityModel.Tokens.SecurityTokenHandler.ValidateToken%2A> method of the token handler.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="806e2-130">父元素</span><span class="sxs-lookup"><span data-stu-id="806e2-130">Parent Elements</span></span>  
  
|<span data-ttu-id="806e2-131">元素</span><span class="sxs-lookup"><span data-stu-id="806e2-131">Element</span></span>|<span data-ttu-id="806e2-132">说明</span><span class="sxs-lookup"><span data-stu-id="806e2-132">Description</span></span>|  
|-------------|-----------------|  
|[\<add>](add.md)|<span data-ttu-id="806e2-133">将指定的安全令牌处理程序添加到令牌处理程序集合。</span><span class="sxs-lookup"><span data-stu-id="806e2-133">Adds the specified security token handler to the token handler collection.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="806e2-134">备注</span><span class="sxs-lookup"><span data-stu-id="806e2-134">Remarks</span></span>  

 <span data-ttu-id="806e2-135">`<samlSecurityTokenRequirement>`元素由 <xref:System.IdentityModel.Tokens.SamlSecurityTokenRequirement> 对象模型中的类表示，用于 `SamlSecurityTokenRequirement` 在或上配置属性 <xref:System.IdentityModel.Tokens.SamlSecurityTokenHandler> <xref:System.IdentityModel.Tokens.Saml2SecurityTokenHandler> 。</span><span class="sxs-lookup"><span data-stu-id="806e2-135">The `<samlSecurityTokenRequirement>` element is represented by the <xref:System.IdentityModel.Tokens.SamlSecurityTokenRequirement> class in the object model and is used to configure the `SamlSecurityTokenRequirement` property on a <xref:System.IdentityModel.Tokens.SamlSecurityTokenHandler> or a <xref:System.IdentityModel.Tokens.Saml2SecurityTokenHandler>.</span></span>  
  
## <a name="example"></a><span data-ttu-id="806e2-136">示例</span><span class="sxs-lookup"><span data-stu-id="806e2-136">Example</span></span>  
  
```xml  
<add type="System.IdentityModel.Tokens.SamlSecurityTokenHandler, System.IdentityModel">  
    <samlSecurityTokenRequirement issuerCertificateValidationMode="PeerOrChainTrust"  
                                  issuerCertificateRevocationMode="Online"  
                                  issuerCertificateTrustedStoreLocation="LocalMachine"  
                                  mapToWindows="false">  
  
        <nameClaimType value="http://schemas.xmlsoap.org/ws/2005/05/identity/claims/name" />  
        <roleClaimType value="schemas.microsoft.com/ws/2006/04/identity/claims/role" />  
    </samlSecurityTokenRequirement>  
</add>  
```
