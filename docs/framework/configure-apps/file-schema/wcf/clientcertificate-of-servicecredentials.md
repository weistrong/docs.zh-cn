---
description: 了解详细 <clientCertificate> 信息： <serviceCredentials>
title: <clientCertificate> 的 <serviceCredentials>
ms.date: 03/30/2017
ms.assetid: 90ad03aa-2317-43dd-8a72-6d24cdcad15c
ms.openlocfilehash: c3e6378f9646ec30188e2de3d1c832f363904ad0
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99638816"
---
# <a name="clientcertificate-of-servicecredentials"></a><span data-ttu-id="945f9-103">\<clientCertificate> 的 \<serviceCredentials></span><span class="sxs-lookup"><span data-stu-id="945f9-103">\<clientCertificate> of \<serviceCredentials></span></span>

<span data-ttu-id="945f9-104">定义一个用于在双工通信模式中对从服务发送到客户端的消息进行签名和加密的 X.509 证书。</span><span class="sxs-lookup"><span data-stu-id="945f9-104">Defines an X.509 certificate used to sign and encrypt messages to a client form a service in a duplex communication pattern.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<behaviors>**](behaviors.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<serviceBehaviors>**](servicebehaviors.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<behavior>**](behavior-of-servicebehaviors.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<serviceCredentials>**](servicecredentials.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<clientCertificate>**  
  
## <a name="syntax"></a><span data-ttu-id="945f9-105">语法</span><span class="sxs-lookup"><span data-stu-id="945f9-105">Syntax</span></span>  
  
```xml  
<clientCertificate>
  <certificate />
  <authentication />
</clientCertificate>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="945f9-106">特性和元素</span><span class="sxs-lookup"><span data-stu-id="945f9-106">Attributes and Elements</span></span>  

 <span data-ttu-id="945f9-107">以下几节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="945f9-107">The following sections describe attributes, child elements, and parent elements</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="945f9-108">特性</span><span class="sxs-lookup"><span data-stu-id="945f9-108">Attributes</span></span>  

 <span data-ttu-id="945f9-109">无。</span><span class="sxs-lookup"><span data-stu-id="945f9-109">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="945f9-110">子元素</span><span class="sxs-lookup"><span data-stu-id="945f9-110">Child Elements</span></span>  
  
|<span data-ttu-id="945f9-111">元素</span><span class="sxs-lookup"><span data-stu-id="945f9-111">Element</span></span>|<span data-ttu-id="945f9-112">说明</span><span class="sxs-lookup"><span data-stu-id="945f9-112">Description</span></span>|  
|-------------|-----------------|  
|[\<authentication>](authentication-of-clientcertificate-element.md)|<span data-ttu-id="945f9-113">指定客户端证书的身份验证选项。</span><span class="sxs-lookup"><span data-stu-id="945f9-113">Specifies authentication options for the client certificate.</span></span>|  
|[\<certificate>](certificate-of-clientcertificate-element.md)|<span data-ttu-id="945f9-114">指定要使用的证书。</span><span class="sxs-lookup"><span data-stu-id="945f9-114">Specifies the certificate to use.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="945f9-115">父元素</span><span class="sxs-lookup"><span data-stu-id="945f9-115">Parent Elements</span></span>  
  
|<span data-ttu-id="945f9-116">元素</span><span class="sxs-lookup"><span data-stu-id="945f9-116">Element</span></span>|<span data-ttu-id="945f9-117">说明</span><span class="sxs-lookup"><span data-stu-id="945f9-117">Description</span></span>|  
|-------------|-----------------|  
|[\<serviceCredentials>](servicecredentials.md)|<span data-ttu-id="945f9-118">指定要用于对服务进行身份验证的凭据以及与客户端凭据验证相关的设置。</span><span class="sxs-lookup"><span data-stu-id="945f9-118">Specifies the credentials to be used in authenticating the service, and the client credential validation related settings.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="945f9-119">备注</span><span class="sxs-lookup"><span data-stu-id="945f9-119">Remarks</span></span>  

 <span data-ttu-id="945f9-120">如果服务必须事先拥有客户端的证书才能与该客户端进行安全通信，则需要使用此元素。</span><span class="sxs-lookup"><span data-stu-id="945f9-120">This element is used when the service must have the client's certificate in advance to communicate securely with the client.</span></span> <span data-ttu-id="945f9-121">使用双工通信模式时，会出现这种情况。</span><span class="sxs-lookup"><span data-stu-id="945f9-121">This occurs when using the duplex communication pattern.</span></span> <span data-ttu-id="945f9-122">在更为典型的请求/响应模式中，客户端会将其证书包含在请求中，服务将使用该证书对发送回客户端的响应进行加密和签名。</span><span class="sxs-lookup"><span data-stu-id="945f9-122">In the more typical request/response pattern, the client includes its certificate in the request, which the service uses to encrypt and sign its response back to the client.</span></span> <span data-ttu-id="945f9-123">但是，在双工通信模式中，服务没有来自客户端的请求，因此服务需要事先具有客户端的证书以确保发送到客户端的消息的安全。</span><span class="sxs-lookup"><span data-stu-id="945f9-123">In the duplex communication pattern, however, the service does not have a request from the client and therefore it needs the client's certificate in advance to secure the message to the client.</span></span> <span data-ttu-id="945f9-124">因此，您必须通过带外协商来获取客户端的证书，并使用此元素指定该证书。</span><span class="sxs-lookup"><span data-stu-id="945f9-124">Therefore you must obtain the client's certificate in an out-of-band negotiation, and specify the certificate using this element.</span></span> <span data-ttu-id="945f9-125">有关双工服务的详细信息，请参阅 [如何：创建双工协定](../../../wcf/feature-details/how-to-create-a-duplex-contract.md)。</span><span class="sxs-lookup"><span data-stu-id="945f9-125">For more information about duplex services, see [How to: Create a Duplex Contract](../../../wcf/feature-details/how-to-create-a-duplex-contract.md).</span></span>  
  
 <span data-ttu-id="945f9-126">在此元素中设置的证书用于仅针对配置有 `MutualCertificateDuplex` 消息安全身份验证模式的绑定加密发送到客户端的消息。</span><span class="sxs-lookup"><span data-stu-id="945f9-126">The certificate set in this element is used to encrypt messages to the client only for bindings that are configured with `MutualCertificateDuplex` message security authentication mode.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="945f9-127">请参阅</span><span class="sxs-lookup"><span data-stu-id="945f9-127">See also</span></span>

- <xref:System.ServiceModel.Configuration.X509InitiatorCertificateServiceElement>
- <xref:System.ServiceModel.Configuration.ServiceCredentialsElement.ClientCertificate%2A>
- <xref:System.ServiceModel.Configuration.X509InitiatorCertificateServiceElement>
- <xref:System.ServiceModel.Description.ServiceCredentials.ClientCertificate%2A>
- <xref:System.ServiceModel.Security.X509CertificateInitiatorServiceCredential>
- [<span data-ttu-id="945f9-128">如何：创建双工协定</span><span class="sxs-lookup"><span data-stu-id="945f9-128">How to: Create a Duplex Contract</span></span>](../../../wcf/feature-details/how-to-create-a-duplex-contract.md)
- [<span data-ttu-id="945f9-129">安全行为</span><span class="sxs-lookup"><span data-stu-id="945f9-129">Security Behaviors</span></span>](../../../wcf/feature-details/security-behaviors-in-wcf.md)
- [<span data-ttu-id="945f9-130">使用证书</span><span class="sxs-lookup"><span data-stu-id="945f9-130">Working with Certificates</span></span>](../../../wcf/feature-details/working-with-certificates.md)
