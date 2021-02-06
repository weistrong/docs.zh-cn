---
description: 了解详细 <certificate> 信息： <identity>
title: 若 <identity>，表示集 <certificate>
ms.date: 03/30/2017
ms.assetid: 4aeccaf7-8f23-495c-aa5f-5bd8b5d4a10c
ms.openlocfilehash: b1ccda7e8e84825cc0b2b2be123fe30be449189a
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99639102"
---
# <a name="certificate-for-identity"></a><span data-ttu-id="ad6ee-103">若 \<identity>，表示集 \<certificate></span><span class="sxs-lookup"><span data-stu-id="ad6ee-103">\<certificate> for \<identity></span></span>

<span data-ttu-id="ad6ee-104">指定用于向客户端验证服务器的 X.509 证书。</span><span class="sxs-lookup"><span data-stu-id="ad6ee-104">Specifies an X.509 certificate used to validate a server to a client.</span></span>  
  
<span data-ttu-id="ad6ee-105">有关设置元素值的详细信息，请参阅 [服务标识和身份验证](../../../wcf/feature-details/service-identity-and-authentication.md)。</span><span class="sxs-lookup"><span data-stu-id="ad6ee-105">For more information about setting the element value, see [Service Identity and Authentication](../../../wcf/feature-details/service-identity-and-authentication.md).</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<client>**](client.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<endpoint>**](endpoint-of-client.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<identity>**](identity.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<certificate>**  
  
## <a name="syntax"></a><span data-ttu-id="ad6ee-106">语法</span><span class="sxs-lookup"><span data-stu-id="ad6ee-106">Syntax</span></span>  
  
```xml  
<certificate encodedValue = "String" />
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="ad6ee-107">特性和元素</span><span class="sxs-lookup"><span data-stu-id="ad6ee-107">Attributes and Elements</span></span>  

 <span data-ttu-id="ad6ee-108">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="ad6ee-108">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="ad6ee-109">特性</span><span class="sxs-lookup"><span data-stu-id="ad6ee-109">Attributes</span></span>  
  
|<span data-ttu-id="ad6ee-110">属性</span><span class="sxs-lookup"><span data-stu-id="ad6ee-110">Attribute</span></span>|<span data-ttu-id="ad6ee-111">说明</span><span class="sxs-lookup"><span data-stu-id="ad6ee-111">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="ad6ee-112">encodedValue</span><span class="sxs-lookup"><span data-stu-id="ad6ee-112">encodedValue</span></span>|<span data-ttu-id="ad6ee-113">证书的 Base64 编码。</span><span class="sxs-lookup"><span data-stu-id="ad6ee-113">A Base64 encoding of the certificate.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="ad6ee-114">子元素</span><span class="sxs-lookup"><span data-stu-id="ad6ee-114">Child Elements</span></span>  

 <span data-ttu-id="ad6ee-115">无。</span><span class="sxs-lookup"><span data-stu-id="ad6ee-115">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="ad6ee-116">父元素</span><span class="sxs-lookup"><span data-stu-id="ad6ee-116">Parent Elements</span></span>  
  
|<span data-ttu-id="ad6ee-117">元素</span><span class="sxs-lookup"><span data-stu-id="ad6ee-117">Element</span></span>|<span data-ttu-id="ad6ee-118">说明</span><span class="sxs-lookup"><span data-stu-id="ad6ee-118">Description</span></span>|  
|-------------|-----------------|  
|[\<identity>](identity.md)|<span data-ttu-id="ad6ee-119">指定要由客户端进行身份验证的服务的标识。</span><span class="sxs-lookup"><span data-stu-id="ad6ee-119">Specifies the identity of the service to be authenticated by the client.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="ad6ee-120">示例</span><span class="sxs-lookup"><span data-stu-id="ad6ee-120">Example</span></span>  

 <span data-ttu-id="ad6ee-121">下面的代码指定用于向客户端验证服务器的证书的编码表示形式。</span><span class="sxs-lookup"><span data-stu-id="ad6ee-121">The following code specifies the encoded representation of a certificate used to validate a server to a client.</span></span>  
  
```xml  
<identity>
  <certificate encodedValue="MIIBxjCCAXSgAwIBAgIQmXJgyu9tro1M98GifjtuoDAJBgUrDgMCHQUAMBYxFDASBgNVBAMTC1Jvb3QgQWdlbmN5MB4XDTA2MDUxNzIxNDQyNVoXDTM5MTIzMTIzNTk1OVowKTEQMA4GA1UEChMHQ29udG9zbzEVMBMGA1UEAxMMaWRlbnRpdHkuY29tMIGfMA0GCSqGSIb3DQEBAQUAA4GNADCBiQKBgQDBmivcb8hYbh11hqVoDuB7zmJ2y230f" />
</identity>
```  
  
## <a name="see-also"></a><span data-ttu-id="ad6ee-122">请参阅</span><span class="sxs-lookup"><span data-stu-id="ad6ee-122">See also</span></span>

- <xref:System.ServiceModel.Configuration.IdentityElement>
- <xref:System.ServiceModel.EndpointAddress>
- <xref:System.ServiceModel.EndpointAddress.Identity%2A>
- <xref:System.ServiceModel.EndpointIdentity>
- [<span data-ttu-id="ad6ee-123">服务标识和身份验证</span><span class="sxs-lookup"><span data-stu-id="ad6ee-123">Service Identity and Authentication</span></span>](../../../wcf/feature-details/service-identity-and-authentication.md)
- [\<identity>](identity.md)
