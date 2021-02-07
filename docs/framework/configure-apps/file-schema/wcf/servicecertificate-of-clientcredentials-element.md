---
description: 了解有关 <serviceCertificate> 元素的详细 <clientCredentials> 信息
title: <serviceCertificate> of <clientCredentials> 元素
ms.date: 03/30/2017
ms.assetid: e50c0ac5-f0df-4c90-b54b-fc602c1f84ea
ms.openlocfilehash: 5503c1a60b2d37f4f9359a2f49c019c37df71619
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99682899"
---
# <a name="servicecertificate-of-clientcredentials-element"></a><span data-ttu-id="cd12c-103">\<serviceCertificate> of \<clientCredentials> 元素</span><span class="sxs-lookup"><span data-stu-id="cd12c-103">\<serviceCertificate> of \<clientCredentials> Element</span></span>

<span data-ttu-id="cd12c-104">指定客户端对服务进行身份验证时使用的证书。</span><span class="sxs-lookup"><span data-stu-id="cd12c-104">Specifies a certificate to use when authenticating a service to the client.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<behaviors>**](behaviors.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<endpointBehaviors>**](endpointbehaviors.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<behavior>**](behavior-of-endpointbehaviors.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<clientCredentials>**](clientcredentials.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<serviceCertificate>**  
  
## <a name="syntax"></a><span data-ttu-id="cd12c-105">语法</span><span class="sxs-lookup"><span data-stu-id="cd12c-105">Syntax</span></span>  
  
```xml  
<serviceCertificate />
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="cd12c-106">特性和元素</span><span class="sxs-lookup"><span data-stu-id="cd12c-106">Attributes and Elements</span></span>  

 <span data-ttu-id="cd12c-107">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="cd12c-107">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="cd12c-108">特性</span><span class="sxs-lookup"><span data-stu-id="cd12c-108">Attributes</span></span>  

 <span data-ttu-id="cd12c-109">无。</span><span class="sxs-lookup"><span data-stu-id="cd12c-109">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="cd12c-110">子元素</span><span class="sxs-lookup"><span data-stu-id="cd12c-110">Child Elements</span></span>  
  
|<span data-ttu-id="cd12c-111">元素</span><span class="sxs-lookup"><span data-stu-id="cd12c-111">Element</span></span>|<span data-ttu-id="cd12c-112">说明</span><span class="sxs-lookup"><span data-stu-id="cd12c-112">Description</span></span>|  
|-------------|-----------------|  
|[\<defaultCertificate>](defaultcertificate-element.md)|<span data-ttu-id="cd12c-113">指定在服务或 STS 未通过协商协议提供证书时要使用的 X.509 证书。</span><span class="sxs-lookup"><span data-stu-id="cd12c-113">Specifies an X.509 certificate to be used when a service or STS does not provide one via a negotiation protocol.</span></span>|  
|[\<scopedCertificates>](scopedcertificates-element.md)|<span data-ttu-id="cd12c-114">表示特定服务为身份验证提供的 X.509（作用域）证书的集合。</span><span class="sxs-lookup"><span data-stu-id="cd12c-114">Represents a collection of X.509 certificates provided by specific services (scoped) for authentication.</span></span> <span data-ttu-id="cd12c-115">此集合通常用于指定联合方案中安全令牌服务的服务证书。</span><span class="sxs-lookup"><span data-stu-id="cd12c-115">This collection is typically used to specify the service certificates for Security Token Services in a federated scenario.</span></span>|  
|[\<authentication>](authentication-of-servicecertificate-element.md)|<span data-ttu-id="cd12c-116">指定客户端使用的服务证书的身份验证行为。</span><span class="sxs-lookup"><span data-stu-id="cd12c-116">Specifies authentication behaviors for service certificates used by a client.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="cd12c-117">父元素</span><span class="sxs-lookup"><span data-stu-id="cd12c-117">Parent Elements</span></span>  
  
|<span data-ttu-id="cd12c-118">元素</span><span class="sxs-lookup"><span data-stu-id="cd12c-118">Element</span></span>|<span data-ttu-id="cd12c-119">说明</span><span class="sxs-lookup"><span data-stu-id="cd12c-119">Description</span></span>|  
|-------------|-----------------|  
|[\<clientCredentials>](clientcredentials.md)|<span data-ttu-id="cd12c-120">指定客户端用于向服务证明自己的身份的凭据。</span><span class="sxs-lookup"><span data-stu-id="cd12c-120">Specifies the credentials used by the client to authenticate itself to a service.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="cd12c-121">备注</span><span class="sxs-lookup"><span data-stu-id="cd12c-121">Remarks</span></span>  

 <span data-ttu-id="cd12c-122">此配置元素指定客户端在验证使用 SSL 身份验证的服务所出示的证书时使用的设置。</span><span class="sxs-lookup"><span data-stu-id="cd12c-122">This configuration element specifies the settings used by the client to validate the certificate presented by the service using SSL authentication.</span></span> <span data-ttu-id="cd12c-123">它还包含在客户端上显式配置为对发送给使用消息安全的服务的消息进行加密的服务的所有证书。</span><span class="sxs-lookup"><span data-stu-id="cd12c-123">It also contains any certificate for the service that is explicitly configured on the client to use for encrypting messages to the service using message security.</span></span>  
  
 <span data-ttu-id="cd12c-124">元素的特性与 `serviceCertificate` 的特性相同 [\<clientCertificate>](clientcertificate-of-clientcredentials-element.md) 。</span><span class="sxs-lookup"><span data-stu-id="cd12c-124">The attributes of the `serviceCertificate` element are identical to the attributes of the [\<clientCertificate>](clientcertificate-of-clientcredentials-element.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="cd12c-125">请参阅</span><span class="sxs-lookup"><span data-stu-id="cd12c-125">See also</span></span>

- <xref:System.ServiceModel.Configuration.ClientCredentialsElement>
- <xref:System.ServiceModel.Configuration.ClientCredentialsElement.ServiceCertificate%2A>
- <xref:System.ServiceModel.Description.ClientCredentials>
- <xref:System.ServiceModel.Description.ClientCredentials.ServiceCertificate%2A>
- <xref:System.ServiceModel.Configuration.X509RecipientCertificateClientElement>
- <xref:System.ServiceModel.Security.X509CertificateRecipientClientCredential>
- [<span data-ttu-id="cd12c-126">安全行为</span><span class="sxs-lookup"><span data-stu-id="cd12c-126">Security Behaviors</span></span>](../../../wcf/feature-details/security-behaviors-in-wcf.md)
- [<span data-ttu-id="cd12c-127">保证客户端的安全</span><span class="sxs-lookup"><span data-stu-id="cd12c-127">Securing Clients</span></span>](../../../wcf/securing-clients.md)
- [<span data-ttu-id="cd12c-128">使用证书</span><span class="sxs-lookup"><span data-stu-id="cd12c-128">Working with Certificates</span></span>](../../../wcf/feature-details/working-with-certificates.md)
- [<span data-ttu-id="cd12c-129">保护服务和客户端的安全</span><span class="sxs-lookup"><span data-stu-id="cd12c-129">Securing Services and Clients</span></span>](../../../wcf/feature-details/securing-services-and-clients.md)
