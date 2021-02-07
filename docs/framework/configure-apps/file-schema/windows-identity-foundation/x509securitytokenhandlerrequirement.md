---
description: 了解详细信息： <x509SecurityTokenHandlerRequirement>
title: <x509SecurityTokenHandlerRequirement>
ms.date: 03/30/2017
ms.assetid: aca22c2c-5ae7-42af-9bbd-15c2524692ce
author: BrucePerlerMS
ms.openlocfilehash: 21a05cfeee6365bd677a6f35e984cb64fa4dd078
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99748968"
---
# \<x509SecurityTokenHandlerRequirement>

<span data-ttu-id="4017c-102">提供 <xref:System.IdentityModel.Tokens.X509SecurityTokenHandler> 类或派生类的可选配置。</span><span class="sxs-lookup"><span data-stu-id="4017c-102">Provides optional configuration for the <xref:System.IdentityModel.Tokens.X509SecurityTokenHandler> class or derived classes.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.identityModel>**](system-identitymodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<identityConfiguration>**](identityconfiguration.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<securityTokenHandlers>**](securitytokenhandlers.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<add>**](add.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<x509SecurityTokenHandlerRequirement>**  
  
## <a name="syntax"></a><span data-ttu-id="4017c-103">语法</span><span class="sxs-lookup"><span data-stu-id="4017c-103">Syntax</span></span>  
  
```xml  
<system.identityModel>  
  <identityConfiguration>  
    <securityTokenHandlers>  
      <add type="System.IdentityModel.Tokens.X509SecurityTokenHandler, System.IdentityModel">  
        <x509SecurityTokenHandlerRequirement>  
          mapToWindows=xs:boolean  
          certificateValidationMode="None||ChainTrust||PeerTrust||PeerOrChainTrust||Custom"  
          certificateValidator="Namespace.Class, Assembly"  
          revocationMode="NoCheck||Offline||Online"  
          trustedStoreLocation="CurrentUser||LocalMachine"  
        </x509SecurityTokenHandlerRequirement>  
      </add>  
    </securityTokenHandlers>  
  </identityConfiguration>  
</system.identityModel>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="4017c-104">特性和元素</span><span class="sxs-lookup"><span data-stu-id="4017c-104">Attributes and Elements</span></span>  

 <span data-ttu-id="4017c-105">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="4017c-105">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="4017c-106">特性</span><span class="sxs-lookup"><span data-stu-id="4017c-106">Attributes</span></span>  
  
|<span data-ttu-id="4017c-107">属性</span><span class="sxs-lookup"><span data-stu-id="4017c-107">Attribute</span></span>|<span data-ttu-id="4017c-108">说明</span><span class="sxs-lookup"><span data-stu-id="4017c-108">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="4017c-109">certificateValidationMode</span><span class="sxs-lookup"><span data-stu-id="4017c-109">certificateValidationMode</span></span>|<span data-ttu-id="4017c-110">一个 <xref:System.ServiceModel.Security.X509CertificateValidationMode> 值，该值指定要用于 x.509 证书的验证模式。</span><span class="sxs-lookup"><span data-stu-id="4017c-110">An <xref:System.ServiceModel.Security.X509CertificateValidationMode> value that specifies the validation mode to use for the X.509 certificate.</span></span> <span data-ttu-id="4017c-111">默认值为 "PeerOrChainTrust"。</span><span class="sxs-lookup"><span data-stu-id="4017c-111">The default value is "PeerOrChainTrust".</span></span>|  
|<span data-ttu-id="4017c-112">mapToWindows</span><span class="sxs-lookup"><span data-stu-id="4017c-112">mapToWindows</span></span>|<span data-ttu-id="4017c-113">指定令牌处理程序是否应使用传入 UPN 声明将验证令牌映射到 Windows 帐户。</span><span class="sxs-lookup"><span data-stu-id="4017c-113">Specifies whether the token handler should map the validating token to a Windows account by using the incoming UPN claim.</span></span> <span data-ttu-id="4017c-114">默认值为“false”。</span><span class="sxs-lookup"><span data-stu-id="4017c-114">The default is "false".</span></span>|  
|<span data-ttu-id="4017c-115">revocationMode</span><span class="sxs-lookup"><span data-stu-id="4017c-115">revocationMode</span></span>|<span data-ttu-id="4017c-116">一个 <xref:System.Security.Cryptography.X509Certificates.X509RevocationMode> 值，该值指定要用于 x.509 证书的吊销模式。</span><span class="sxs-lookup"><span data-stu-id="4017c-116">An <xref:System.Security.Cryptography.X509Certificates.X509RevocationMode> value that specifies the revocation mode to use for the X.509 certificate.</span></span> <span data-ttu-id="4017c-117">默认值为 "Online"。</span><span class="sxs-lookup"><span data-stu-id="4017c-117">The default value is "Online".</span></span>|  
|<span data-ttu-id="4017c-118">trustedStoreLocation</span><span class="sxs-lookup"><span data-stu-id="4017c-118">trustedStoreLocation</span></span>|<span data-ttu-id="4017c-119">一个 <xref:System.Security.Cryptography.X509Certificates.StoreLocation> 值，该值指定 x.509 证书存储区。</span><span class="sxs-lookup"><span data-stu-id="4017c-119">A <xref:System.Security.Cryptography.X509Certificates.StoreLocation> value that specifies the X.509 certificate store.</span></span> <span data-ttu-id="4017c-120">默认值为 "LocalMachine"。</span><span class="sxs-lookup"><span data-stu-id="4017c-120">The default value is "LocalMachine".</span></span>|  
|<span data-ttu-id="4017c-121">certificateValidator</span><span class="sxs-lookup"><span data-stu-id="4017c-121">certificateValidator</span></span>|<span data-ttu-id="4017c-122">派生自的自定义类型 <xref:System.IdentityModel.Selectors.X509CertificateValidator> 。</span><span class="sxs-lookup"><span data-stu-id="4017c-122">A custom type that derives from <xref:System.IdentityModel.Selectors.X509CertificateValidator>.</span></span> <span data-ttu-id="4017c-123">如果该 `certificateValidationMode` 属性为 "Custom"，则此类型的实例将用于颁发者证书验证。</span><span class="sxs-lookup"><span data-stu-id="4017c-123">If the `certificateValidationMode` attribute is "Custom", an instance of this type is used for issuer certificate validation.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="4017c-124">子元素</span><span class="sxs-lookup"><span data-stu-id="4017c-124">Child Elements</span></span>  

 <span data-ttu-id="4017c-125">无</span><span class="sxs-lookup"><span data-stu-id="4017c-125">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="4017c-126">父元素</span><span class="sxs-lookup"><span data-stu-id="4017c-126">Parent Elements</span></span>  
  
|<span data-ttu-id="4017c-127">元素</span><span class="sxs-lookup"><span data-stu-id="4017c-127">Element</span></span>|<span data-ttu-id="4017c-128">说明</span><span class="sxs-lookup"><span data-stu-id="4017c-128">Description</span></span>|  
|-------------|-----------------|  
|[\<add>](add.md)|<span data-ttu-id="4017c-129">将指定的安全令牌处理程序添加到令牌处理程序集合。</span><span class="sxs-lookup"><span data-stu-id="4017c-129">Adds the specified security token handler to the token handler collection.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="4017c-130">示例</span><span class="sxs-lookup"><span data-stu-id="4017c-130">Example</span></span>  
  
```xml  
<add type="System.IdentityModel.Tokens.X509SecurityTokenHandler, System.IdentityModel">  
    <x509SecurityTokenHandlerRequirement mapToWindows="true"
                                         certificateValidationMode="PeerOrChainTrust"
                                         revocationMode="Online"
                                         trustedStoreLocation="LocalMachine" />  
</add>  
```
