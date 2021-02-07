---
description: 了解详细信息： <certificateValidation>
title: <certificateValidation>
ms.date: 03/30/2017
ms.assetid: 6c54c704-b55e-4631-88ff-4d4a5621554c
author: BrucePerlerMS
ms.openlocfilehash: a12e46487b4fb2ac8071ba1cf9bc5c6057ded060
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99740062"
---
# \<certificateValidation>

<span data-ttu-id="be655-102">控制标记处理程序用于验证证书的设置。</span><span class="sxs-lookup"><span data-stu-id="be655-102">Controls the settings that token handlers use to validate certificates.</span></span> <span data-ttu-id="be655-103">如果为特定处理程序配置了其自己的验证程序，则会重写这些设置。</span><span class="sxs-lookup"><span data-stu-id="be655-103">These settings are overridden if a specific handler is configured with its own validator.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.identityModel>**](system-identitymodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<identityConfiguration>**](identityconfiguration.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<certificateValidation>**  
  
## <a name="syntax"></a><span data-ttu-id="be655-104">语法</span><span class="sxs-lookup"><span data-stu-id="be655-104">Syntax</span></span>  
  
```xml  
<system.identityModel>  
  <identityConfiguration>  
    <certificateValidation  
      certificateValidationMode="None||ChainTrust||PeerTrust||PeerOrChainTrust||Custom"  
      revocationMode="NoCheck||Offline||Online"  
      trustedStoreLocation="CurrentLocation||LocalMachine" >  
    </certificateValidation>  
  </identityConfiguration>  
</system.identityModel>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="be655-105">特性和元素</span><span class="sxs-lookup"><span data-stu-id="be655-105">Attributes and Elements</span></span>  

 <span data-ttu-id="be655-106">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="be655-106">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="be655-107">特性</span><span class="sxs-lookup"><span data-stu-id="be655-107">Attributes</span></span>  
  
|<span data-ttu-id="be655-108">属性</span><span class="sxs-lookup"><span data-stu-id="be655-108">Attribute</span></span>|<span data-ttu-id="be655-109">说明</span><span class="sxs-lookup"><span data-stu-id="be655-109">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="be655-110">certificateValidationMode</span><span class="sxs-lookup"><span data-stu-id="be655-110">certificateValidationMode</span></span>|<span data-ttu-id="be655-111">一个 <xref:System.ServiceModel.Security.X509CertificateValidationMode> 值，该值指定要用于 x.509 证书的验证模式。</span><span class="sxs-lookup"><span data-stu-id="be655-111">An <xref:System.ServiceModel.Security.X509CertificateValidationMode> value that specifies the validation mode to use for the X.509 certificate.</span></span> <span data-ttu-id="be655-112">默认值为 "PeerOrChainTrust"。</span><span class="sxs-lookup"><span data-stu-id="be655-112">The default value is "PeerOrChainTrust".</span></span> <span data-ttu-id="be655-113">若要指定自定义验证程序，请将此特性设置为 "Custom"，并使用元素指定验证程序 [\<certificateValidator>](certificatevalidator.md) 。</span><span class="sxs-lookup"><span data-stu-id="be655-113">To specify a custom validator, set this attribute to "Custom" and specify the validator using the [\<certificateValidator>](certificatevalidator.md) element.</span></span> <span data-ttu-id="be655-114">可选。</span><span class="sxs-lookup"><span data-stu-id="be655-114">Optional.</span></span>|  
|<span data-ttu-id="be655-115">revocationMode</span><span class="sxs-lookup"><span data-stu-id="be655-115">revocationMode</span></span>|<span data-ttu-id="be655-116">一个 <xref:System.Security.Cryptography.X509Certificates.X509RevocationMode> 值，该值指定要用于 x.509 证书的吊销模式。</span><span class="sxs-lookup"><span data-stu-id="be655-116">An <xref:System.Security.Cryptography.X509Certificates.X509RevocationMode> value that specifies the revocation mode to use for the X.509 certificate.</span></span> <span data-ttu-id="be655-117">默认值为 "Online"。</span><span class="sxs-lookup"><span data-stu-id="be655-117">The default value is "Online".</span></span> <span data-ttu-id="be655-118">可选。</span><span class="sxs-lookup"><span data-stu-id="be655-118">Optional.</span></span>|  
|<span data-ttu-id="be655-119">trustedStoreLocation</span><span class="sxs-lookup"><span data-stu-id="be655-119">trustedStoreLocation</span></span>|<span data-ttu-id="be655-120">一个 <xref:System.Security.Cryptography.X509Certificates.StoreLocation> 值，该值指定 x.509 证书存储区。</span><span class="sxs-lookup"><span data-stu-id="be655-120">A <xref:System.Security.Cryptography.X509Certificates.StoreLocation> value that specifies the X.509 certificate store.</span></span> <span data-ttu-id="be655-121">默认值为 "LocalMachine"。</span><span class="sxs-lookup"><span data-stu-id="be655-121">The default value is "LocalMachine".</span></span> <span data-ttu-id="be655-122">可选。</span><span class="sxs-lookup"><span data-stu-id="be655-122">Optional.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="be655-123">子元素</span><span class="sxs-lookup"><span data-stu-id="be655-123">Child Elements</span></span>  
  
|<span data-ttu-id="be655-124">元素</span><span class="sxs-lookup"><span data-stu-id="be655-124">Element</span></span>|<span data-ttu-id="be655-125">说明</span><span class="sxs-lookup"><span data-stu-id="be655-125">Description</span></span>|  
|-------------|-----------------|  
|[\<certificateValidator>](certificatevalidator.md)|<span data-ttu-id="be655-126">指定证书验证的自定义类型。</span><span class="sxs-lookup"><span data-stu-id="be655-126">Specifies a custom type for certificate validation.</span></span> <span data-ttu-id="be655-127">仅当 `certificateValidationMode` 元素的属性 [\<certificateValidation>](certificatevalidation.md) 设置为 "Custom" 时才使用此类型。</span><span class="sxs-lookup"><span data-stu-id="be655-127">This type is used only if the `certificateValidationMode` attribute of the [\<certificateValidation>](certificatevalidation.md) element is set to "Custom".</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="be655-128">父元素</span><span class="sxs-lookup"><span data-stu-id="be655-128">Parent Elements</span></span>  
  
|<span data-ttu-id="be655-129">元素</span><span class="sxs-lookup"><span data-stu-id="be655-129">Element</span></span>|<span data-ttu-id="be655-130">说明</span><span class="sxs-lookup"><span data-stu-id="be655-130">Description</span></span>|  
|-------------|-----------------|  
|[\<identityConfiguration>](identityconfiguration.md)|<span data-ttu-id="be655-131">指定服务级别标识设置。</span><span class="sxs-lookup"><span data-stu-id="be655-131">Specifies service-level identity settings.</span></span>|  
|[\<securityTokenHandlerConfiguration>](securitytokenhandlerconfiguration.md)|<span data-ttu-id="be655-132">为安全标记处理程序的集合提供配置。</span><span class="sxs-lookup"><span data-stu-id="be655-132">Provides configuration for a collection of security token handlers.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="be655-133">备注</span><span class="sxs-lookup"><span data-stu-id="be655-133">Remarks</span></span>  

 <span data-ttu-id="be655-134">可以在元素 `<certificateValidation>` 下的服务级别指定元素， `<identityConfiguration>` 或在元素下的安全令牌处理程序集合级别指定元素 `<securityTokenHandlerConfiguration>` 。</span><span class="sxs-lookup"><span data-stu-id="be655-134">A `<certificateValidation>` element can be specified at the service level under the `<identityConfiguration>` element or on the security token handler collection level under the `<securityTokenHandlerConfiguration>` element.</span></span> <span data-ttu-id="be655-135">标记处理程序集合上的设置将重写服务上指定的设置。</span><span class="sxs-lookup"><span data-stu-id="be655-135">Settings on a token handler collection override those specified on the service.</span></span> <span data-ttu-id="be655-136">某些标记处理程序允许您在配置中指定证书验证设置。</span><span class="sxs-lookup"><span data-stu-id="be655-136">Some token handlers allow you to specify certificate validation settings in configuration.</span></span> <span data-ttu-id="be655-137">各个标记处理程序上的设置将覆盖在服务级别和安全令牌处理程序集合上指定的设置。</span><span class="sxs-lookup"><span data-stu-id="be655-137">Settings on individual token handlers override those specified both at the service level and on the security token handler collection.</span></span>  
  
## <a name="example"></a><span data-ttu-id="be655-138">示例</span><span class="sxs-lookup"><span data-stu-id="be655-138">Example</span></span>  
  
```xml  
<certificateValidation certificateValidationMode="PeerOrChainTrust"  
                       revocationMode="Online"  
                       trustedStoreLocation="LocalMachine" />  
```
