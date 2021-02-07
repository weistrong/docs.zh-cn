---
description: 了解详细信息： <certificateReference>
title: <certificateReference>
ms.date: 03/30/2017
ms.assetid: 2ac8bc14-e9f1-48fb-b662-f5991558fbe4
author: BrucePerlerMS
ms.openlocfilehash: 3404d44457849fb78ae88617d049a2199f2b5509
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99681781"
---
# \<certificateReference>

<span data-ttu-id="683cd-102">指定用于在证书存储中查找和验证 x.509 证书的设置。</span><span class="sxs-lookup"><span data-stu-id="683cd-102">Specifies settings that are used to find and validate an X.509 certificate in a certificate store.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.identityModel.services>**](system-identitymodel-services.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<federationConfiguration>**](federationconfiguration.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<serviceCertificate>**](servicecertificate.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<certificateReference>**  
  
## <a name="syntax"></a><span data-ttu-id="683cd-103">语法</span><span class="sxs-lookup"><span data-stu-id="683cd-103">Syntax</span></span>  
  
```xml  
<system.identityModel.services>  
  <federationConfiguration>  
    <serviceCertificate>  
      <certificateReference
        storeName="AddressBook||AuthRoot||CertificateAuthority||Disallowed||My||Root||TrustedPeople||TrustedPublisher"  
        storeLocation="CurrentUser||LocalMachine"  
        x509FindType="FindByThumbprint||FindBySubjectName||FindBySubjectDistinguishedName||FindByIssuerName||FindByIssuerDistinguishedName||FindBySerialNumber||FindByTimeValid||FindByTimeNotYetValid||FindByTimeExpired||FindByTemplateName||FindByApplicationPolicy||FindByCertificatePolicy||FindByExtension||FindByKeyUsage||FindBySubjectKeyIdentifier"  
        findValue=xs:String  
        isChainIncluded=xs:Boolean >  
      </certificateReference>  
    </serviceCertificate>  
  </federationConfiguration>  
</system.identityModel.services>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="683cd-104">特性和元素</span><span class="sxs-lookup"><span data-stu-id="683cd-104">Attributes and Elements</span></span>  

 <span data-ttu-id="683cd-105">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="683cd-105">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="683cd-106">特性</span><span class="sxs-lookup"><span data-stu-id="683cd-106">Attributes</span></span>  
  
|<span data-ttu-id="683cd-107">属性</span><span class="sxs-lookup"><span data-stu-id="683cd-107">Attribute</span></span>|<span data-ttu-id="683cd-108">说明</span><span class="sxs-lookup"><span data-stu-id="683cd-108">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="683cd-109">storeName</span><span class="sxs-lookup"><span data-stu-id="683cd-109">storeName</span></span>|<span data-ttu-id="683cd-110">X.509 证书存储区的名称。</span><span class="sxs-lookup"><span data-stu-id="683cd-110">The name of the X.509 certificate store.</span></span> <span data-ttu-id="683cd-111">默认值为 "My"。</span><span class="sxs-lookup"><span data-stu-id="683cd-111">The default is "My".</span></span> <span data-ttu-id="683cd-112">可选。</span><span class="sxs-lookup"><span data-stu-id="683cd-112">Optional.</span></span>|  
|<span data-ttu-id="683cd-113">storeLocation</span><span class="sxs-lookup"><span data-stu-id="683cd-113">storeLocation</span></span>|<span data-ttu-id="683cd-114">一个 <xref:System.Security.Cryptography.X509Certificates.StoreLocation> 值，该值指定 x.509 证书存储区的位置。</span><span class="sxs-lookup"><span data-stu-id="683cd-114">A <xref:System.Security.Cryptography.X509Certificates.StoreLocation> value that specifies the location of the X.509 certificate store.</span></span> <span data-ttu-id="683cd-115">默认值为 "LocalMachine"。</span><span class="sxs-lookup"><span data-stu-id="683cd-115">The default value is "LocalMachine".</span></span> <span data-ttu-id="683cd-116">可选。</span><span class="sxs-lookup"><span data-stu-id="683cd-116">Optional.</span></span>|  
|<span data-ttu-id="683cd-117">x509FindType</span><span class="sxs-lookup"><span data-stu-id="683cd-117">x509FindType</span></span>|<span data-ttu-id="683cd-118">一个 <xref:System.Security.Cryptography.X509Certificates.X509FindType> 值，该值指定要执行的搜索的类型。</span><span class="sxs-lookup"><span data-stu-id="683cd-118">An <xref:System.Security.Cryptography.X509Certificates.X509FindType> value that specifies the type of search that is to be executed.</span></span> <span data-ttu-id="683cd-119">默认值为 "FindBySubjectDistinguishedName"。</span><span class="sxs-lookup"><span data-stu-id="683cd-119">The default is "FindBySubjectDistinguishedName".</span></span> <span data-ttu-id="683cd-120">可选。</span><span class="sxs-lookup"><span data-stu-id="683cd-120">Optional.</span></span>|  
|<span data-ttu-id="683cd-121">findValue</span><span class="sxs-lookup"><span data-stu-id="683cd-121">findValue</span></span>|<span data-ttu-id="683cd-122">要在 X.509 证书存储区中搜索的值。</span><span class="sxs-lookup"><span data-stu-id="683cd-122">The value to search for in the X.509 certificate store.</span></span> <span data-ttu-id="683cd-123">可选。</span><span class="sxs-lookup"><span data-stu-id="683cd-123">Optional.</span></span>|  
|<span data-ttu-id="683cd-124">isChainIncluded</span><span class="sxs-lookup"><span data-stu-id="683cd-124">isChainIncluded</span></span>|<span data-ttu-id="683cd-125">指定是否应通过使用证书链来执行验证。</span><span class="sxs-lookup"><span data-stu-id="683cd-125">Specifies whether validation should be performed by using the certificate chain.</span></span> <span data-ttu-id="683cd-126">默认值为 "true";验证是通过使用证书链来执行的。</span><span class="sxs-lookup"><span data-stu-id="683cd-126">The default is "true"; validation is performed by using the certificate chain.</span></span> <span data-ttu-id="683cd-127">可选。</span><span class="sxs-lookup"><span data-stu-id="683cd-127">Optional.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="683cd-128">子元素</span><span class="sxs-lookup"><span data-stu-id="683cd-128">Child Elements</span></span>  

 <span data-ttu-id="683cd-129">无</span><span class="sxs-lookup"><span data-stu-id="683cd-129">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="683cd-130">父元素</span><span class="sxs-lookup"><span data-stu-id="683cd-130">Parent Elements</span></span>  
  
|<span data-ttu-id="683cd-131">元素</span><span class="sxs-lookup"><span data-stu-id="683cd-131">Element</span></span>|<span data-ttu-id="683cd-132">说明</span><span class="sxs-lookup"><span data-stu-id="683cd-132">Description</span></span>|  
|-------------|-----------------|  
|[\<serviceCertificate>](servicecertificate.md)|<span data-ttu-id="683cd-133">配置用于加密和解密令牌的证书。</span><span class="sxs-lookup"><span data-stu-id="683cd-133">Configures the certificate that is used to encrypt and decrypt tokens.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="683cd-134">备注</span><span class="sxs-lookup"><span data-stu-id="683cd-134">Remarks</span></span>  

 <span data-ttu-id="683cd-135">`<certificateReference>`元素指定用于在证书存储区中查找和验证 x.509 证书的设置。</span><span class="sxs-lookup"><span data-stu-id="683cd-135">The `<certificateReference>` element specifies settings that are used to find and validate an X.509 certificate in a certificate store.</span></span> <span data-ttu-id="683cd-136">指定为元素的子元素时 `<serviceCertificate>` ，它将指定用于加密和解密令牌的 x.509 证书的位置和验证设置。</span><span class="sxs-lookup"><span data-stu-id="683cd-136">When it is specified as the child element of the `<serviceCertificate>` element, it specifies the location and verification settings of the X.509 certificate that is used to encrypt and decrypt tokens.</span></span> <span data-ttu-id="683cd-137">`<certificateReference>`元素由 <xref:System.ServiceModel.Configuration.CertificateReferenceElement> 类表示。</span><span class="sxs-lookup"><span data-stu-id="683cd-137">The `<certificateReference>` element is represented by the <xref:System.ServiceModel.Configuration.CertificateReferenceElement> class.</span></span>
