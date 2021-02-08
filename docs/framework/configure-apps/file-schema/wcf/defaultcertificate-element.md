---
description: 了解详细信息： <defaultCertificate> 元素
title: <defaultCertificate> 元素
ms.date: 03/30/2017
ms.assetid: f1ddf364-9a00-45d3-b989-ff381c154ce6
ms.openlocfilehash: 580236e521e91c8b475586f6c6378630960f233c
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99803914"
---
# <a name="defaultcertificate-element"></a><span data-ttu-id="d7db9-103">\<defaultCertificate> 元素</span><span class="sxs-lookup"><span data-stu-id="d7db9-103">\<defaultCertificate> Element</span></span>

<span data-ttu-id="d7db9-104">指定在服务或 STS 未通过协商协议提供证书时要使用的 X.509 证书。</span><span class="sxs-lookup"><span data-stu-id="d7db9-104">Specifies an X.509 certificate to be used when a service or STS does not provide one via a negotiation protocol.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<behaviors>**](behaviors.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<endpointBehaviors>**](endpointbehaviors.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<behavior>**](behavior-of-endpointbehaviors.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<clientCredentials>**](clientcredentials.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<serviceCertificate>**](servicecertificate-of-clientcredentials-element.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<defaultCertificate>**  
  
## <a name="syntax"></a><span data-ttu-id="d7db9-105">语法</span><span class="sxs-lookup"><span data-stu-id="d7db9-105">Syntax</span></span>  
  
```xml  
<defaultCertificate findValue="String"
                    storeLocation=" CurrentUser/LocalMachine"
                    storeName="AddressBook/AuthRoot/CertificateAuthority/Disallowed/My/Root/TrustedPeople/TrustedPublisher"
                    x509FindType="FindByThumbPrint/FindBySubjectName/FindBySubjectDistinguishedName/FindByIssuerName/FindByIssuerDistinguishedName/FindBySerialiNumber/FindByTimeValid/FindByTimeNotYetValid/FindByTimeExpired/FindByTemplateName/FindByApplicationPolicy/FindByCertificatePolicy/FindByExtension/FindByKeyUsage/FindBySubjectKeyIdentifier" />
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="d7db9-106">特性和元素</span><span class="sxs-lookup"><span data-stu-id="d7db9-106">Attributes and Elements</span></span>  

 <span data-ttu-id="d7db9-107">以下几节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="d7db9-107">The following sections describe attributes, child elements, and parent elements</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="d7db9-108">特性</span><span class="sxs-lookup"><span data-stu-id="d7db9-108">Attributes</span></span>  
  
|<span data-ttu-id="d7db9-109">属性</span><span class="sxs-lookup"><span data-stu-id="d7db9-109">Attribute</span></span>|<span data-ttu-id="d7db9-110">说明</span><span class="sxs-lookup"><span data-stu-id="d7db9-110">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="d7db9-111">findValue</span><span class="sxs-lookup"><span data-stu-id="d7db9-111">findValue</span></span>|<span data-ttu-id="d7db9-112">字符串。</span><span class="sxs-lookup"><span data-stu-id="d7db9-112">String.</span></span> <span data-ttu-id="d7db9-113">要搜索的值。</span><span class="sxs-lookup"><span data-stu-id="d7db9-113">The value to search for.</span></span>|  
|<span data-ttu-id="d7db9-114">x509FindType</span><span class="sxs-lookup"><span data-stu-id="d7db9-114">x509FindType</span></span>|<span data-ttu-id="d7db9-115">枚举。</span><span class="sxs-lookup"><span data-stu-id="d7db9-115">Enumeration.</span></span> <span data-ttu-id="d7db9-116">要搜索的证书字段之一。</span><span class="sxs-lookup"><span data-stu-id="d7db9-116">One of the certificate fields to search.</span></span>|  
|<span data-ttu-id="d7db9-117">storeLocation</span><span class="sxs-lookup"><span data-stu-id="d7db9-117">storeLocation</span></span>|<span data-ttu-id="d7db9-118">枚举。</span><span class="sxs-lookup"><span data-stu-id="d7db9-118">Enumeration.</span></span> <span data-ttu-id="d7db9-119">要搜索的两个系统存储位置之一。</span><span class="sxs-lookup"><span data-stu-id="d7db9-119">One of the two system store locations to search.</span></span>|  
|<span data-ttu-id="d7db9-120">storeName</span><span class="sxs-lookup"><span data-stu-id="d7db9-120">storeName</span></span>|<span data-ttu-id="d7db9-121">枚举。</span><span class="sxs-lookup"><span data-stu-id="d7db9-121">Enumeration.</span></span> <span data-ttu-id="d7db9-122">要搜索的系统存储之一。</span><span class="sxs-lookup"><span data-stu-id="d7db9-122">One of the system stores to search.</span></span>|  
  
## <a name="findvalue-attribute"></a><span data-ttu-id="d7db9-123">findValue 属性</span><span class="sxs-lookup"><span data-stu-id="d7db9-123">findValue Attribute</span></span>  
  
|<span data-ttu-id="d7db9-124">值</span><span class="sxs-lookup"><span data-stu-id="d7db9-124">Value</span></span>|<span data-ttu-id="d7db9-125">说明</span><span class="sxs-lookup"><span data-stu-id="d7db9-125">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="d7db9-126">字符串</span><span class="sxs-lookup"><span data-stu-id="d7db9-126">String</span></span>|<span data-ttu-id="d7db9-127">值取决于搜索的字段（由 X509FindType 属性指定）。</span><span class="sxs-lookup"><span data-stu-id="d7db9-127">The value depends on the field (specified by the X509FindType attribute) being searched.</span></span> <span data-ttu-id="d7db9-128">例如，如果搜索指纹，则此值必须为十六进制数字字符串。</span><span class="sxs-lookup"><span data-stu-id="d7db9-128">For example, if searching for a thumbprint, the value must be a string of hexadecimal numbers.</span></span>|  
  
## <a name="x509findtype-attribute"></a><span data-ttu-id="d7db9-129">x509FindType 属性</span><span class="sxs-lookup"><span data-stu-id="d7db9-129">x509FindType Attribute</span></span>  
  
|<span data-ttu-id="d7db9-130">值</span><span class="sxs-lookup"><span data-stu-id="d7db9-130">Value</span></span>|<span data-ttu-id="d7db9-131">说明</span><span class="sxs-lookup"><span data-stu-id="d7db9-131">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="d7db9-132">枚举</span><span class="sxs-lookup"><span data-stu-id="d7db9-132">Enumeration</span></span>|<span data-ttu-id="d7db9-133">值包括：FindByThumbprint、FindBySubjectName、FindBySubjectDistinguishedName、FindByIssuerName、FindByIssuerDistinguishedName、FindBySerialNumber、FindByTimeValid、FindByTimeNotYetValid、FindBySerialNumber、FindByTimeExpired、FindByTemplateName、FindByApplicationPolicy、FindByCertificatePolicy、FindByExtension、FindByKeyUsage 和 FindBySubjectKeyIdentifier。</span><span class="sxs-lookup"><span data-stu-id="d7db9-133">Values include: FindByThumbprint, FindBySubjectName, FindBySubjectDistinguishedName, FindByIssuerName, FindByIssuerDistinguishedName, FindBySerialNumber, FindByTimeValid, FindByTimeNotYetValid, FindBySerialNumber, FindByTimeExpired, FindByTemplateName, FindByApplicationPolicy, FindByCertificatePolicy, FindByExtension, FindByKeyUsage, FindBySubjectKeyIdentifier.</span></span>|  
  
## <a name="storelocation-attribute"></a><span data-ttu-id="d7db9-134">storeLocation 属性</span><span class="sxs-lookup"><span data-stu-id="d7db9-134">storeLocation Attribute</span></span>  
  
|<span data-ttu-id="d7db9-135">值</span><span class="sxs-lookup"><span data-stu-id="d7db9-135">Value</span></span>|<span data-ttu-id="d7db9-136">说明</span><span class="sxs-lookup"><span data-stu-id="d7db9-136">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="d7db9-137">枚举</span><span class="sxs-lookup"><span data-stu-id="d7db9-137">Enumeration</span></span>|<span data-ttu-id="d7db9-138">CurrentUser 或 LocalMachine。</span><span class="sxs-lookup"><span data-stu-id="d7db9-138">CurrentUser or LocalMachine.</span></span>|  
  
## <a name="storename-attribute"></a><span data-ttu-id="d7db9-139">storeName 属性</span><span class="sxs-lookup"><span data-stu-id="d7db9-139">storeName Attribute</span></span>  
  
|<span data-ttu-id="d7db9-140">值</span><span class="sxs-lookup"><span data-stu-id="d7db9-140">Value</span></span>|<span data-ttu-id="d7db9-141">说明</span><span class="sxs-lookup"><span data-stu-id="d7db9-141">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="d7db9-142">枚举</span><span class="sxs-lookup"><span data-stu-id="d7db9-142">Enumeration</span></span>|<span data-ttu-id="d7db9-143">值包括：AddressBook、AuthRoot、CertificateAuthority、Disallowed、My、Root、TrustedPeople 和 TrustedPublisher。</span><span class="sxs-lookup"><span data-stu-id="d7db9-143">Values include: AddressBook, AuthRoot, CertificateAuthority, Disallowed, My, Root, TrustedPeople, and TrustedPublisher.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="d7db9-144">子元素</span><span class="sxs-lookup"><span data-stu-id="d7db9-144">Child Elements</span></span>  

 <span data-ttu-id="d7db9-145">无。</span><span class="sxs-lookup"><span data-stu-id="d7db9-145">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="d7db9-146">父元素</span><span class="sxs-lookup"><span data-stu-id="d7db9-146">Parent Elements</span></span>  
  
|<span data-ttu-id="d7db9-147">元素</span><span class="sxs-lookup"><span data-stu-id="d7db9-147">Element</span></span>|<span data-ttu-id="d7db9-148">说明</span><span class="sxs-lookup"><span data-stu-id="d7db9-148">Description</span></span>|  
|-------------|-----------------|  
|[\<serviceCertificate>](servicecertificate-of-clientcredentials-element.md)|<span data-ttu-id="d7db9-149">指定客户端对服务进行身份验证时使用的证书。</span><span class="sxs-lookup"><span data-stu-id="d7db9-149">Specifies a certificate to use when authenticating a service to the client.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="d7db9-150">备注</span><span class="sxs-lookup"><span data-stu-id="d7db9-150">Remarks</span></span>  

 <span data-ttu-id="d7db9-151">对于使用基于证书的消息安全的绑定，此配置元素指定的证书用于加密发送给服务的消息，并期望服务用它来对客户端的应答进行签名。</span><span class="sxs-lookup"><span data-stu-id="d7db9-151">For bindings that use certificate-based message security, certificate specified by this configuration element is used to encrypt messages to the service and is expected to be used by the service for signing replies to the client.</span></span> <span data-ttu-id="d7db9-152">如果服务未指定任何证书，它只存储要使用的一个证书。</span><span class="sxs-lookup"><span data-stu-id="d7db9-152">It stores a single certificate to be used when no certificate is specified by a service.</span></span>  
  
## <a name="example"></a><span data-ttu-id="d7db9-153">示例</span><span class="sxs-lookup"><span data-stu-id="d7db9-153">Example</span></span>  

 <span data-ttu-id="d7db9-154">下面的示例指定一个证书，该证书用于其 URI 以开头的终结点 `http://www.contoso.com` ，以及用于所有不执行证书协商的其他终结点的证书。</span><span class="sxs-lookup"><span data-stu-id="d7db9-154">The following example specifies a certificate to use for endpoints whose URI begins with `http://www.contoso.com` and a certificate to use for all other endpoints that do not perform certificate negotiation.</span></span>  
  
```xml  
<serviceCertificate>
  <defaultCertificate findValue="www.contoso.com"
                      storeLocation="LocalMachine"
                      storeName="TrustedPeople"
                      x509FindType="FindByIssuerDistinguishedName" />
  <scopedCertificates>
    <add targetUri="http://www.contoso.com"
         findValue="www.contoso.com"
         storeLocation="LocalMachine"
         storeName="Root"
         x509FindType="FindByIssuerName" />
  </scopedCertificates>
  <authentication revocationMode="Online"
                  trustedStoreLocation="LocalMachine" />
</serviceCertificate>
```  
  
## <a name="see-also"></a><span data-ttu-id="d7db9-155">请参阅</span><span class="sxs-lookup"><span data-stu-id="d7db9-155">See also</span></span>

- <xref:System.ServiceModel.Configuration.X509DefaultServiceCertificateElement>
- <xref:System.ServiceModel.Security.X509CertificateRecipientClientCredential>
- <xref:System.ServiceModel.Security.X509CertificateRecipientClientCredential.DefaultCertificate%2A>
- [<span data-ttu-id="d7db9-156">使用证书</span><span class="sxs-lookup"><span data-stu-id="d7db9-156">Working with Certificates</span></span>](../../../wcf/feature-details/working-with-certificates.md)
- [\<authentication>](authentication-of-clientcertificate-element.md)
- [<span data-ttu-id="d7db9-157">保证客户端的安全</span><span class="sxs-lookup"><span data-stu-id="d7db9-157">Securing Clients</span></span>](../../../wcf/securing-clients.md)
- [<span data-ttu-id="d7db9-158">保护服务和客户端的安全</span><span class="sxs-lookup"><span data-stu-id="d7db9-158">Securing Services and Clients</span></span>](../../../wcf/feature-details/securing-services-and-clients.md)
