---
description: 了解详细信息： <custom>
title: <custom>
ms.date: 03/30/2017
ms.assetid: a6f65a00-bd1a-4d4a-955a-fe009ec02ab8
ms.openlocfilehash: 327a5d7ff1bab88a1633d7a10095e708e6b1a533
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99725904"
---
# \<custom>

<span data-ttu-id="28c08-102">指定自定义对等解析程序服务的设置。</span><span class="sxs-lookup"><span data-stu-id="28c08-102">Specifies settings for a custom peer resolver service.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<bindings>**](bindings.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<netPeerTcpBinding>**](netpeertcpbinding.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<binding>**\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<resolver>**](resolver.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<custom>**  
  
## <a name="syntax"></a><span data-ttu-id="28c08-103">语法</span><span class="sxs-lookup"><span data-stu-id="28c08-103">Syntax</span></span>  
  
```xml  
<custom address="Uri"
        resolverType="String">
  <headers/>
  <identity/>
</custom>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="28c08-104">特性和元素</span><span class="sxs-lookup"><span data-stu-id="28c08-104">Attributes and Elements</span></span>  

 <span data-ttu-id="28c08-105">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="28c08-105">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="28c08-106">特性</span><span class="sxs-lookup"><span data-stu-id="28c08-106">Attributes</span></span>  
  
|<span data-ttu-id="28c08-107">属性</span><span class="sxs-lookup"><span data-stu-id="28c08-107">Attribute</span></span>|<span data-ttu-id="28c08-108">说明</span><span class="sxs-lookup"><span data-stu-id="28c08-108">Description</span></span>|  
|---------------|-----------------|  
|`address`|<span data-ttu-id="28c08-109">一个 URI，指定承载自定义对等解析程序服务的对等节点的终结点地址。</span><span class="sxs-lookup"><span data-stu-id="28c08-109">A URI that specifies the endpoint address of the peer node that hosts the custom peer resolver service.</span></span>|  
|`resolverType`|<span data-ttu-id="28c08-110">一个字符串值，指定自定义对等解析程序服务的类型。</span><span class="sxs-lookup"><span data-stu-id="28c08-110">A string that specifies the type of the custom peer resolver service.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="28c08-111">子元素</span><span class="sxs-lookup"><span data-stu-id="28c08-111">Child Elements</span></span>  
  
|<span data-ttu-id="28c08-112">元素</span><span class="sxs-lookup"><span data-stu-id="28c08-112">Element</span></span>|<span data-ttu-id="28c08-113">说明</span><span class="sxs-lookup"><span data-stu-id="28c08-113">Description</span></span>|  
|-------------|-----------------|  
|[\<identity>](identity.md)|<span data-ttu-id="28c08-114">指定配置了此元素的自定义对等解析程序的标识。</span><span class="sxs-lookup"><span data-stu-id="28c08-114">Specifies the identity for custom peer resolvers configured with this element.</span></span> <span data-ttu-id="28c08-115">此元素的类型为 <xref:System.ServiceModel.Configuration.IdentityElement>。</span><span class="sxs-lookup"><span data-stu-id="28c08-115">This element is of type <xref:System.ServiceModel.Configuration.IdentityElement>.</span></span>|  
|[\<headers>](headers-element.md)|<span data-ttu-id="28c08-116">一个地址标头集合，可用于由自定义对等解析程序处理的 SOAP 消息。</span><span class="sxs-lookup"><span data-stu-id="28c08-116">A collection of address header used for SOAP messages handled by the custom peer resolver.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="28c08-117">父元素</span><span class="sxs-lookup"><span data-stu-id="28c08-117">Parent Elements</span></span>  
  
|<span data-ttu-id="28c08-118">元素</span><span class="sxs-lookup"><span data-stu-id="28c08-118">Element</span></span>|<span data-ttu-id="28c08-119">说明</span><span class="sxs-lookup"><span data-stu-id="28c08-119">Description</span></span>|  
|-------------|-----------------|  
|[\<resolver>](resolver.md)|<span data-ttu-id="28c08-120">一个对等解析程序，可用于将对等网格 ID 解析为一组对等节点地址，这些地址表示参与网格的若干节点。</span><span class="sxs-lookup"><span data-stu-id="28c08-120">A peer resolver that is used to resolve a peer mesh ID to a set of peer node addresses that represents several nodes that participate in the mesh.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="28c08-121">备注</span><span class="sxs-lookup"><span data-stu-id="28c08-121">Remarks</span></span>  

 <span data-ttu-id="28c08-122">此元素可定义自定义对等解析程序服务的基本设置，其中包括执行服务的对等解析程序的终结点地址和所有特定绑定设置。</span><span class="sxs-lookup"><span data-stu-id="28c08-122">This element defines the basic settings for a custom peer resolver service, including the endpoint address of the peer hosting the service and any specific binding settings.</span></span> <span data-ttu-id="28c08-123">有关创建自定义冲突解决程序的详细信息，请参阅 [将自定义冲突解决程序添加到 PeerChannel 应用程序](/previous-versions/ms730105(v=vs.90))。</span><span class="sxs-lookup"><span data-stu-id="28c08-123">For more information on creating a custom resolver, see [Adding a Custom Resolver to a PeerChannel Application](/previous-versions/ms730105(v=vs.90)).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="28c08-124">请参阅</span><span class="sxs-lookup"><span data-stu-id="28c08-124">See also</span></span>

- <xref:System.ServiceModel.PeerResolvers.CustomPeerResolverService>
- <xref:System.ServiceModel.PeerResolvers.PeerCustomResolverSettings>
- <xref:System.ServiceModel.Configuration.PeerResolverElement.Custom%2A>
- <xref:System.ServiceModel.Configuration.PeerCustomResolverElement>
- [<span data-ttu-id="28c08-125">对等解析程序</span><span class="sxs-lookup"><span data-stu-id="28c08-125">Peer Resolvers</span></span>](../../../wcf/feature-details/peer-resolvers.md)
- <span data-ttu-id="28c08-126">[向对等通道应用程序添加自定义解析程序](/previous-versions/ms730105(v=vs.90))</span><span class="sxs-lookup"><span data-stu-id="28c08-126">[Adding a Custom Resolver to a PeerChannel Application](/previous-versions/ms730105(v=vs.90))</span></span>
