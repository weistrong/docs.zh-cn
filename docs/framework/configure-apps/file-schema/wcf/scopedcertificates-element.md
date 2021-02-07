---
description: 了解详细信息： <scopedCertificates> 元素
title: <scopedCertificates> 元素
ms.date: 03/30/2017
ms.assetid: c7b6fc35-d4b2-4c18-98bd-83e09591f1d3
ms.openlocfilehash: 7aa108031831539396e8f737a214982655dd6bb1
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99683328"
---
# <a name="scopedcertificates-element"></a><span data-ttu-id="1fbd1-103">\<scopedCertificates> 元素</span><span class="sxs-lookup"><span data-stu-id="1fbd1-103">\<scopedCertificates> Element</span></span>

<span data-ttu-id="1fbd1-104">表示特定服务为身份验证提供的 X.509（作用域）证书的集合。</span><span class="sxs-lookup"><span data-stu-id="1fbd1-104">Represents a collection of X.509 certificates provided by specific services (scoped) for authentication.</span></span> <span data-ttu-id="1fbd1-105">此集合通常用于指定联合方案中安全令牌服务的服务证书。</span><span class="sxs-lookup"><span data-stu-id="1fbd1-105">This collection is typically used to specify the service certificates for Security Token Services in a federated scenario.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<behaviors>**](behaviors.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<endpointBehaviors>**](endpointbehaviors.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<behavior>**](behavior-of-endpointbehaviors.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<clientCredentials>**](clientcredentials.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<serviceCertificate>**](servicecertificate-of-clientcredentials-element.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<scopedCertificates>**  
  
## <a name="syntax"></a><span data-ttu-id="1fbd1-106">语法</span><span class="sxs-lookup"><span data-stu-id="1fbd1-106">Syntax</span></span>  
  
```xml  
<scopedCertificates>
  <add findValue="String"
       storeLocation="CurrentUser/LocalMachine"
       storeName=" CurrentUser/LocalMachine"
       targetUri="string"
       x509Type="FindByThumbprint/FindBySubjectName/FindBySubjectDistinguishedName/FindByIssuerName/FindByIssuerDistinguishedName/FindBySerialNumber/FindByTimeValid/FindByTimeNotYetValid/FindBySerialNumber/FindByTimeExpired/FindByTemplateName/FindByApplicationPolicy/FindByCertificatePolicy/FindByExtension/FindByKeyUsage/FindBySubjectKeyIdentifier" />
</scopedCertificates>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="1fbd1-107">特性和元素</span><span class="sxs-lookup"><span data-stu-id="1fbd1-107">Attributes and Elements</span></span>  

 <span data-ttu-id="1fbd1-108">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="1fbd1-108">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="1fbd1-109">特性</span><span class="sxs-lookup"><span data-stu-id="1fbd1-109">Attributes</span></span>  

 <span data-ttu-id="1fbd1-110">无。</span><span class="sxs-lookup"><span data-stu-id="1fbd1-110">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="1fbd1-111">子元素</span><span class="sxs-lookup"><span data-stu-id="1fbd1-111">Child Elements</span></span>  
  
|<span data-ttu-id="1fbd1-112">元素</span><span class="sxs-lookup"><span data-stu-id="1fbd1-112">Element</span></span>|<span data-ttu-id="1fbd1-113">说明</span><span class="sxs-lookup"><span data-stu-id="1fbd1-113">Description</span></span>|  
|-------------|-----------------|  
|[\<add>](add-of-scopedcertificates-element.md)|<span data-ttu-id="1fbd1-114">向作用域证书集合添加 X.509 证书。</span><span class="sxs-lookup"><span data-stu-id="1fbd1-114">Adds an X.509 certificate to the collection of scoped certificates.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="1fbd1-115">父元素</span><span class="sxs-lookup"><span data-stu-id="1fbd1-115">Parent Elements</span></span>  
  
|<span data-ttu-id="1fbd1-116">元素</span><span class="sxs-lookup"><span data-stu-id="1fbd1-116">Element</span></span>|<span data-ttu-id="1fbd1-117">说明</span><span class="sxs-lookup"><span data-stu-id="1fbd1-117">Description</span></span>|  
|-------------|-----------------|  
|[\<serviceCertificate>](servicecertificate-of-servicecredentials.md)|<span data-ttu-id="1fbd1-118">指定客户端对服务进行身份验证时使用的证书。</span><span class="sxs-lookup"><span data-stu-id="1fbd1-118">Specifies a certificate to use when authenticating a service to the client.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="1fbd1-119">备注</span><span class="sxs-lookup"><span data-stu-id="1fbd1-119">Remarks</span></span>  

 <span data-ttu-id="1fbd1-120">此集合使客户端能够根据与它通信的服务的 URL 来配置要使用的服务证书。</span><span class="sxs-lookup"><span data-stu-id="1fbd1-120">This collection enables the client to configure the service certificates to use based on the URL of the service it communicates with.</span></span> <span data-ttu-id="1fbd1-121">这在已颁发令牌的方案中尤其有用，在这些方案中，客户端可与多个服务（终端服务以及中间的安全令牌服务）进行通信。</span><span class="sxs-lookup"><span data-stu-id="1fbd1-121">This is especially useful in issued token scenarios where a client can be communicating to multiple services (the end service as well as intermediary security token services).</span></span> <span data-ttu-id="1fbd1-122">对于使用基于证书的消息安全的绑定，此证书用于加密发送给服务的消息，并期望服务用它来对客户端的应答进行签名。</span><span class="sxs-lookup"><span data-stu-id="1fbd1-122">For bindings that use certificate-based message security, this certificate is used to encrypt messages to the service, and is expected to be used by the service for signing replies to the client.</span></span>  
  
 <span data-ttu-id="1fbd1-123">如果绑定需要服务的证书，但在 ScopedCertificates 中未找到服务 URL 的特定证书，则使用默认证书。</span><span class="sxs-lookup"><span data-stu-id="1fbd1-123">If a binding requires a certificate for the service and no specific certificate for the service URL is found in the ScopedCertificates, the default certificate is used.</span></span>  
  
 <span data-ttu-id="1fbd1-124">有关详细信息，请参阅 [如何：创建联合客户端](../../../wcf/feature-details/how-to-create-a-federated-client.md)中的 "范围内的证书" 一节。</span><span class="sxs-lookup"><span data-stu-id="1fbd1-124">For more information, see the "Scoped Certificates" section of [How to: Create a Federated Client](../../../wcf/feature-details/how-to-create-a-federated-client.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="1fbd1-125">示例</span><span class="sxs-lookup"><span data-stu-id="1fbd1-125">Example</span></span>  

 <span data-ttu-id="1fbd1-126">下面的示例指定一个服务证书，以便客户端与域名位于 HTTP 协议的终结点进行通信时使用 `http://www.contoso.com` 。</span><span class="sxs-lookup"><span data-stu-id="1fbd1-126">The following example specifies a service certificate for the client to use when communicating with endpoints whose domain name is `http://www.contoso.com` over the HTTP protocol.</span></span>  
  
```xml  
<serviceCertificate>
  <scopedCertificates>
    <add targetUri="http://www.contoso.com"
         findValue="www.contoso.com"
         storeLocation="LocalMachine"
         storeName="Root"
         x509FindType="FindByIssuerName" />
  </scopedCertificates>
</serviceCertificate>
```  
  
## <a name="see-also"></a><span data-ttu-id="1fbd1-127">请参阅</span><span class="sxs-lookup"><span data-stu-id="1fbd1-127">See also</span></span>

- <xref:System.ServiceModel.Configuration.X509RecipientCertificateClientElement.ScopedCertificates%2A>
- <xref:System.ServiceModel.Configuration.X509ScopedServiceCertificateElementCollection>
- <xref:System.ServiceModel.Configuration.X509ScopedServiceCertificateElement>
- <xref:System.ServiceModel.Security.X509CertificateRecipientClientCredential>
- <xref:System.ServiceModel.Security.X509CertificateRecipientClientCredential.ScopedCertificates%2A>
- [<span data-ttu-id="1fbd1-128">使用证书</span><span class="sxs-lookup"><span data-stu-id="1fbd1-128">Working with Certificates</span></span>](../../../wcf/feature-details/working-with-certificates.md)
- [<span data-ttu-id="1fbd1-129">如何：创建联合客户端</span><span class="sxs-lookup"><span data-stu-id="1fbd1-129">How to: Create a Federated Client</span></span>](../../../wcf/feature-details/how-to-create-a-federated-client.md)
- [\<add>](add-of-scopedcertificates-element.md)
- [<span data-ttu-id="1fbd1-130">保证客户端的安全</span><span class="sxs-lookup"><span data-stu-id="1fbd1-130">Securing Clients</span></span>](../../../wcf/securing-clients.md)
- [<span data-ttu-id="1fbd1-131">保护服务和客户端的安全</span><span class="sxs-lookup"><span data-stu-id="1fbd1-131">Securing Services and Clients</span></span>](../../../wcf/feature-details/securing-services-and-clients.md)
