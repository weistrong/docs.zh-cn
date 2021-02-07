---
description: 了解有关 <add> 元素的详细 <scopedCertificates> 信息
title: <add> of <scopedCertificates> 元素
ms.date: 03/30/2017
ms.assetid: e21c1ef8-d6d6-4bca-ac5a-6fbf4bd77412
ms.openlocfilehash: 4c267164ccf065edee79a6aaaa9aaddc14d95909
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99750268"
---
# <a name="add-of-scopedcertificates-element"></a><span data-ttu-id="262be-103">\<add> of \<scopedCertificates> 元素</span><span class="sxs-lookup"><span data-stu-id="262be-103">\<add> of \<scopedCertificates> Element</span></span>

<span data-ttu-id="262be-104">向作用域证书集合添加 X.509 证书。</span><span class="sxs-lookup"><span data-stu-id="262be-104">Adds an X.509 certificate to the collection of scoped certificates.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<behaviors>**](behaviors.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<endpointBehaviors>**](endpointbehaviors.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<behavior>**](behavior-of-endpointbehaviors.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<clientCredentials>**](clientcredentials.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<serviceCertificate>**](servicecertificate-of-clientcredentials-element.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<scopedCertificates>**](scopedcertificates-element.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<add>**  
  
## <a name="syntax"></a><span data-ttu-id="262be-105">语法</span><span class="sxs-lookup"><span data-stu-id="262be-105">Syntax</span></span>  
  
```xml  
<add findValue="String"
     storeLocation="CurrentUser/LocalMachine"
     storeName=" CurrentUser/LocalMachine"
     targetUri="string"
     x509Type="FindByThumbprint/FindBySubjectName/FindBySubjectDistinguishedName/FindByIssuerName/FindByIssuerDistinguishedName/FindBySerialNumber/FindByTimeValid/FindByTimeNotYetValid/FindBySerialNumber/FindByTimeExpired/FindByTemplateName/FindByApplicationPolicy/FindByCertificatePolicy/FindByExtension/FindByKeyUsage/FindBySubjectKeyIdentifier" />
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="262be-106">特性和元素</span><span class="sxs-lookup"><span data-stu-id="262be-106">Attributes and Elements</span></span>  

 <span data-ttu-id="262be-107">以下几节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="262be-107">The following sections describe attributes, child elements, and parent elements</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="262be-108">特性</span><span class="sxs-lookup"><span data-stu-id="262be-108">Attributes</span></span>  
  
|<span data-ttu-id="262be-109">属性</span><span class="sxs-lookup"><span data-stu-id="262be-109">Attribute</span></span>|<span data-ttu-id="262be-110">说明</span><span class="sxs-lookup"><span data-stu-id="262be-110">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="262be-111">targetUri</span><span class="sxs-lookup"><span data-stu-id="262be-111">targetUri</span></span>|<span data-ttu-id="262be-112">字符串。</span><span class="sxs-lookup"><span data-stu-id="262be-112">String.</span></span> <span data-ttu-id="262be-113">指定与证书相关的服务的 URI。</span><span class="sxs-lookup"><span data-stu-id="262be-113">Specifies the URI of the service associated with the certificate.</span></span>|  
|<span data-ttu-id="262be-114">findValue</span><span class="sxs-lookup"><span data-stu-id="262be-114">findValue</span></span>|<span data-ttu-id="262be-115">字符串。</span><span class="sxs-lookup"><span data-stu-id="262be-115">String.</span></span> <span data-ttu-id="262be-116">要搜索的值。</span><span class="sxs-lookup"><span data-stu-id="262be-116">The value to search for.</span></span>|  
|<span data-ttu-id="262be-117">x509FindType</span><span class="sxs-lookup"><span data-stu-id="262be-117">x509FindType</span></span>|<span data-ttu-id="262be-118">枚举。</span><span class="sxs-lookup"><span data-stu-id="262be-118">Enumeration.</span></span> <span data-ttu-id="262be-119">要搜索的证书字段之一。</span><span class="sxs-lookup"><span data-stu-id="262be-119">One of the certificate fields to search.</span></span>|  
|<span data-ttu-id="262be-120">storeLocation</span><span class="sxs-lookup"><span data-stu-id="262be-120">storeLocation</span></span>|<span data-ttu-id="262be-121">枚举。</span><span class="sxs-lookup"><span data-stu-id="262be-121">Enumeration.</span></span> <span data-ttu-id="262be-122">要搜索的两个存储位置之一。</span><span class="sxs-lookup"><span data-stu-id="262be-122">One of the two store locations to search.</span></span>|  
|<span data-ttu-id="262be-123">storeName</span><span class="sxs-lookup"><span data-stu-id="262be-123">storeName</span></span>|<span data-ttu-id="262be-124">枚举。</span><span class="sxs-lookup"><span data-stu-id="262be-124">Enumeration.</span></span> <span data-ttu-id="262be-125">要搜索的系统存储之一。</span><span class="sxs-lookup"><span data-stu-id="262be-125">One of the system stores to search.</span></span>|  
  
## <a name="findvalue-attribute"></a><span data-ttu-id="262be-126">findValue 属性</span><span class="sxs-lookup"><span data-stu-id="262be-126">findValue Attribute</span></span>  
  
|<span data-ttu-id="262be-127">值</span><span class="sxs-lookup"><span data-stu-id="262be-127">Value</span></span>|<span data-ttu-id="262be-128">说明</span><span class="sxs-lookup"><span data-stu-id="262be-128">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="262be-129">字符串</span><span class="sxs-lookup"><span data-stu-id="262be-129">String</span></span>|<span data-ttu-id="262be-130">值取决于搜索的字段（由 X509FindType 属性指定）。</span><span class="sxs-lookup"><span data-stu-id="262be-130">The value depends on the field (specified by the X509FindType attribute) being searched.</span></span> <span data-ttu-id="262be-131">例如，如果搜索指纹，则此值必须为十六进制数字字符串。</span><span class="sxs-lookup"><span data-stu-id="262be-131">For example, if searching for a thumbprint, the value must be a string of hexadecimal numbers.</span></span>|  
  
## <a name="x509findtype-attribute"></a><span data-ttu-id="262be-132">x509FindType 属性</span><span class="sxs-lookup"><span data-stu-id="262be-132">x509FindType Attribute</span></span>  
  
|<span data-ttu-id="262be-133">值</span><span class="sxs-lookup"><span data-stu-id="262be-133">Value</span></span>|<span data-ttu-id="262be-134">说明</span><span class="sxs-lookup"><span data-stu-id="262be-134">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="262be-135">枚举</span><span class="sxs-lookup"><span data-stu-id="262be-135">Enumeration</span></span>|<span data-ttu-id="262be-136">值包括：FindByThumbprint、FindBySubjectName、FindBySubjectDistinguishedName、FindByIssuerName、FindByIssuerDistinguishedName、FindBySerialNumber、FindByTimeValid、FindByTimeNotYetValid、FindBySerialNumber、FindByTimeExpired、FindByTemplateName、FindByApplicationPolicy、FindByCertificatePolicy、FindByExtension、FindByKeyUsage 和 FindBySubjectKeyIdentifier。</span><span class="sxs-lookup"><span data-stu-id="262be-136">Values include: FindByThumbprint, FindBySubjectName, FindBySubjectDistinguishedName, FindByIssuerName, FindByIssuerDistinguishedName, FindBySerialNumber, FindByTimeValid, FindByTimeNotYetValid, FindBySerialNumber, FindByTimeExpired, FindByTemplateName, FindByApplicationPolicy, FindByCertificatePolicy, FindByExtension, FindByKeyUsage, FindBySubjectKeyIdentifier.</span></span>|  
  
## <a name="storelocation-attribute"></a><span data-ttu-id="262be-137">storeLocation 属性</span><span class="sxs-lookup"><span data-stu-id="262be-137">storeLocation Attribute</span></span>  
  
|<span data-ttu-id="262be-138">值</span><span class="sxs-lookup"><span data-stu-id="262be-138">Value</span></span>|<span data-ttu-id="262be-139">说明</span><span class="sxs-lookup"><span data-stu-id="262be-139">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="262be-140">枚举</span><span class="sxs-lookup"><span data-stu-id="262be-140">Enumeration</span></span>|<span data-ttu-id="262be-141">CurrentUser 或 LocalMachine。</span><span class="sxs-lookup"><span data-stu-id="262be-141">CurrentUser or LocalMachine.</span></span>|  
  
## <a name="storename-attribute"></a><span data-ttu-id="262be-142">storeName 属性</span><span class="sxs-lookup"><span data-stu-id="262be-142">storeName Attribute</span></span>  
  
|<span data-ttu-id="262be-143">值</span><span class="sxs-lookup"><span data-stu-id="262be-143">Value</span></span>|<span data-ttu-id="262be-144">说明</span><span class="sxs-lookup"><span data-stu-id="262be-144">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="262be-145">枚举</span><span class="sxs-lookup"><span data-stu-id="262be-145">Enumeration</span></span>|<span data-ttu-id="262be-146">值包括：AddressBook、AuthRoot、CertificateAuthority、Disallowed、My、Root、TrustedPeople 和 TrustedPublisher。</span><span class="sxs-lookup"><span data-stu-id="262be-146">Values include: AddressBook, AuthRoot, CertificateAuthority, Disallowed, My, Root, TrustedPeople, and TrustedPublisher.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="262be-147">子元素</span><span class="sxs-lookup"><span data-stu-id="262be-147">Child Elements</span></span>  

 <span data-ttu-id="262be-148">无。</span><span class="sxs-lookup"><span data-stu-id="262be-148">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="262be-149">父元素</span><span class="sxs-lookup"><span data-stu-id="262be-149">Parent Elements</span></span>  
  
|<span data-ttu-id="262be-150">元素</span><span class="sxs-lookup"><span data-stu-id="262be-150">Element</span></span>|<span data-ttu-id="262be-151">说明</span><span class="sxs-lookup"><span data-stu-id="262be-151">Description</span></span>|  
|-------------|-----------------|  
|[\<scopedCertificates>](scopedcertificates-element.md)|<span data-ttu-id="262be-152">表示特定服务为身份验证提供的 X.509（作用域）证书的集合。</span><span class="sxs-lookup"><span data-stu-id="262be-152">Represents a collection of X.509 certificates provided by specific services (scoped) for authentication.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="262be-153">备注</span><span class="sxs-lookup"><span data-stu-id="262be-153">Remarks</span></span>  

 <span data-ttu-id="262be-154">此元素使客户端能够根据与它通信的服务的 URL 来配置要使用的服务证书。</span><span class="sxs-lookup"><span data-stu-id="262be-154">This element enables the client to configure a service certificate to use based on the URL of the service it communicates with.</span></span> <span data-ttu-id="262be-155">这在已颁发令牌的方案中尤其有用，在这些方案中，客户端可与多个服务（终端服务以及中间的安全令牌服务）进行通信。</span><span class="sxs-lookup"><span data-stu-id="262be-155">This is especially useful in issued token scenarios where a client can be communicating to multiple services (the end service as well as intermediary security token services).</span></span> <span data-ttu-id="262be-156">对于使用基于证书的消息安全的绑定，此证书用于加密发送给服务的消息，并期望服务用它来对客户端的应答进行签名。</span><span class="sxs-lookup"><span data-stu-id="262be-156">For bindings that use certificate-based message security, this certificate is used to encrypt messages to the service, and is expected to be used by the service for signing replies to the client.</span></span>  
  
 <span data-ttu-id="262be-157">如果绑定需要服务的证书，但在 ScopedCertificates 中未找到服务 URL 的特定证书，则使用默认证书。</span><span class="sxs-lookup"><span data-stu-id="262be-157">If a binding requires a certificate for the service and no specific certificate for the service URL is found in the ScopedCertificates, the default certificate is used.</span></span>  
  
 <span data-ttu-id="262be-158">有关详细信息，请参阅 [如何：创建联合客户端](../../../wcf/feature-details/how-to-create-a-federated-client.md)中的 "范围内的证书" 一节。</span><span class="sxs-lookup"><span data-stu-id="262be-158">For more information, see the "Scoped Certificates" section of [How to: Create a Federated Client](../../../wcf/feature-details/how-to-create-a-federated-client.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="262be-159">示例</span><span class="sxs-lookup"><span data-stu-id="262be-159">Example</span></span>  

 <span data-ttu-id="262be-160">下面的示例向集合中添加一个 X.509 证书。</span><span class="sxs-lookup"><span data-stu-id="262be-160">The following example adds an X.509 certificate the collection.</span></span>  
  
```xml  
<behaviors>
  <endpointBehaviors>
    <behavior name="MyEndpointBehavior">
      <clientCredentials>
        <serviceCertificate>
          <scopedCertificates>
            <add targetUri="http://www.contoso.com"
                 findValue="www.Contoso.com"
                 storeLocation="LocalMachine"
                 storeName="Root"
                 x509FindType="FindByIssuerName" />
          </scopedCertificates>
        </serviceCertificate>
      </clientCredentials>
    </behavior>
  </endpointBehaviors>
</behaviors>
```  
  
## <a name="see-also"></a><span data-ttu-id="262be-161">请参阅</span><span class="sxs-lookup"><span data-stu-id="262be-161">See also</span></span>

- <xref:System.ServiceModel.Configuration.X509RecipientCertificateClientElement.ScopedCertificates%2A>
- <xref:System.ServiceModel.Configuration.X509ScopedServiceCertificateElementCollection>
- <xref:System.ServiceModel.Configuration.X509ScopedServiceCertificateElement>
- <xref:System.ServiceModel.Security.X509CertificateRecipientClientCredential>
- <xref:System.ServiceModel.Security.X509CertificateRecipientClientCredential.ScopedCertificates%2A>
- [<span data-ttu-id="262be-162">如何：创建联合客户端</span><span class="sxs-lookup"><span data-stu-id="262be-162">How to: Create a Federated Client</span></span>](../../../wcf/feature-details/how-to-create-a-federated-client.md)
- [<span data-ttu-id="262be-163">使用证书</span><span class="sxs-lookup"><span data-stu-id="262be-163">Working with Certificates</span></span>](../../../wcf/feature-details/working-with-certificates.md)
- [<span data-ttu-id="262be-164">保证客户端的安全</span><span class="sxs-lookup"><span data-stu-id="262be-164">Securing Clients</span></span>](../../../wcf/securing-clients.md)
- [<span data-ttu-id="262be-165">保护服务和客户端的安全</span><span class="sxs-lookup"><span data-stu-id="262be-165">Securing Services and Clients</span></span>](../../../wcf/feature-details/securing-services-and-clients.md)
