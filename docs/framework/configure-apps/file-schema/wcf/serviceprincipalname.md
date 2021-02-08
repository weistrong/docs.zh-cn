---
description: 了解详细信息： <servicePrincipalName>
title: <servicePrincipalName>
ms.date: 03/30/2017
ms.assetid: 3f3b85d3-20f2-4cd8-8a6a-ee18befbd165
ms.openlocfilehash: 494368f1f47f10aac8009e47a9219966c87e5eda
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99786689"
---
# \<servicePrincipalName>

<span data-ttu-id="7c520-102">利用对应的服务主体名称 (SPN) 指定服务的标识。</span><span class="sxs-lookup"><span data-stu-id="7c520-102">Specifies the identity of a service by its Service Principal Name (SPN).</span></span>  
  
<span data-ttu-id="7c520-103">有关设置 SPN 的详细信息，请参阅 [服务标识和身份验证](../../../wcf/feature-details/service-identity-and-authentication.md)。</span><span class="sxs-lookup"><span data-stu-id="7c520-103">For more information about setting the SPN, see [Service Identity and Authentication](../../../wcf/feature-details/service-identity-and-authentication.md).</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<client>**](client.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<endpoint>**](endpoint-of-client.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<identity>**](identity.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<servicePrincipalName>**  
  
## <a name="syntax"></a><span data-ttu-id="7c520-104">语法</span><span class="sxs-lookup"><span data-stu-id="7c520-104">Syntax</span></span>  
  
```xml  
<servicePrincipalName value="String" />
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="7c520-105">特性和元素</span><span class="sxs-lookup"><span data-stu-id="7c520-105">Attributes and Elements</span></span>  

 <span data-ttu-id="7c520-106">以下几节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="7c520-106">The following sections describe attributes, child elements, and parent elements</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="7c520-107">特性</span><span class="sxs-lookup"><span data-stu-id="7c520-107">Attributes</span></span>  
  
|<span data-ttu-id="7c520-108">属性</span><span class="sxs-lookup"><span data-stu-id="7c520-108">Attribute</span></span>|<span data-ttu-id="7c520-109">说明</span><span class="sxs-lookup"><span data-stu-id="7c520-109">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="7c520-110">value</span><span class="sxs-lookup"><span data-stu-id="7c520-110">value</span></span>|<span data-ttu-id="7c520-111">客户端用于唯一标识服务实例的名称。</span><span class="sxs-lookup"><span data-stu-id="7c520-111">The name by which a client uniquely identifies an instance of a service.</span></span> <span data-ttu-id="7c520-112">如果在计算机的整个目录林上安装多个服务实例，那么每个实例都必须有自己的 SPN。</span><span class="sxs-lookup"><span data-stu-id="7c520-112">If you install multiple instances of a service on computers throughout a forest, each instance must have its own SPN.</span></span> <span data-ttu-id="7c520-113">如果客户端有多个名称可用于身份验证，则给定的服务实例可以有多个 SPN。</span><span class="sxs-lookup"><span data-stu-id="7c520-113">A given service instance can have multiple SPNs if there are multiple names that clients might use for authentication.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="7c520-114">子元素</span><span class="sxs-lookup"><span data-stu-id="7c520-114">Child Elements</span></span>  

 <span data-ttu-id="7c520-115">无。</span><span class="sxs-lookup"><span data-stu-id="7c520-115">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="7c520-116">父元素</span><span class="sxs-lookup"><span data-stu-id="7c520-116">Parent Elements</span></span>  
  
|<span data-ttu-id="7c520-117">元素</span><span class="sxs-lookup"><span data-stu-id="7c520-117">Element</span></span>|<span data-ttu-id="7c520-118">说明</span><span class="sxs-lookup"><span data-stu-id="7c520-118">Description</span></span>|  
|-------------|-----------------|  
|[\<identity>](identity.md)|<span data-ttu-id="7c520-119">指定要由客户端进行身份验证的服务的标识。</span><span class="sxs-lookup"><span data-stu-id="7c520-119">Specifies the identity of the service to be authenticated by the client.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="7c520-120">备注</span><span class="sxs-lookup"><span data-stu-id="7c520-120">Remarks</span></span>  

 <span data-ttu-id="7c520-121">使用此标识连接到终结点的安全 Windows Communication Foundation (WCF) 客户端在使用终结点进行 SSPI 身份验证时使用 SPN。</span><span class="sxs-lookup"><span data-stu-id="7c520-121">A secure Windows Communication Foundation (WCF) client that connects to an endpoint with this identity uses the SPN when performing SSPI authentication with the endpoint.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7c520-122">请参阅</span><span class="sxs-lookup"><span data-stu-id="7c520-122">See also</span></span>

- <xref:System.ServiceModel.Configuration.IdentityElement>
- <xref:System.ServiceModel.EndpointAddress>
- <xref:System.ServiceModel.EndpointAddress.Identity%2A>
- <xref:System.ServiceModel.SpnEndpointIdentity>
- [<span data-ttu-id="7c520-123">服务标识和身份验证</span><span class="sxs-lookup"><span data-stu-id="7c520-123">Service Identity and Authentication</span></span>](../../../wcf/feature-details/service-identity-and-authentication.md)
- [\<identity>](identity.md)
