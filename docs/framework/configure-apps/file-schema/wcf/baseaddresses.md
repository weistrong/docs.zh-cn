---
description: 了解详细信息： <baseAddresses>
title: <baseAddresses>
ms.date: 03/30/2017
ms.assetid: 78918102-2898-46e0-9ea8-6b8afe65603e
ms.openlocfilehash: a32afc23d4332bad149765a318c3ecdc73f99be0
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99749683"
---
# \<baseAddresses>

<span data-ttu-id="6d4ab-102">表示一个 `baseAddress` 元素集合，这些元素是自承载环境中服务主机的基址。</span><span class="sxs-lookup"><span data-stu-id="6d4ab-102">Represents a collection of `baseAddress` elements, which are base addresses for a service host in a self-hosted environment.</span></span> <span data-ttu-id="6d4ab-103">如果存在基址，则可以使用相对于基址的地址配置终结点。</span><span class="sxs-lookup"><span data-stu-id="6d4ab-103">If a base address is present, endpoints can be configured with addresses relative to the base address.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<services>**](services.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<service>**](service.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<host>**](host.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<baseAddresses>**  
  
## <a name="syntax"></a><span data-ttu-id="6d4ab-104">语法</span><span class="sxs-lookup"><span data-stu-id="6d4ab-104">Syntax</span></span>  
  
```xml  
<baseAddresses>
  <add baseAddress="string" />
</baseAddresses>
```  
  
## <a name="type"></a><span data-ttu-id="6d4ab-105">类型</span><span class="sxs-lookup"><span data-stu-id="6d4ab-105">Type</span></span>  

 `Type`  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="6d4ab-106">特性和元素</span><span class="sxs-lookup"><span data-stu-id="6d4ab-106">Attributes and Elements</span></span>  

 <span data-ttu-id="6d4ab-107">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="6d4ab-107">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="6d4ab-108">特性</span><span class="sxs-lookup"><span data-stu-id="6d4ab-108">Attributes</span></span>  

 <span data-ttu-id="6d4ab-109">无。</span><span class="sxs-lookup"><span data-stu-id="6d4ab-109">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="6d4ab-110">子元素</span><span class="sxs-lookup"><span data-stu-id="6d4ab-110">Child Elements</span></span>  
  
|<span data-ttu-id="6d4ab-111">元素</span><span class="sxs-lookup"><span data-stu-id="6d4ab-111">Element</span></span>|<span data-ttu-id="6d4ab-112">说明</span><span class="sxs-lookup"><span data-stu-id="6d4ab-112">Description</span></span>|  
|-------------|-----------------|  
|[\<add>](add-of-baseaddresses.md)|<span data-ttu-id="6d4ab-113">一个配置元素，指定服务主机所使用的基址。</span><span class="sxs-lookup"><span data-stu-id="6d4ab-113">A configuration element that specifies the base addresses used by the service host.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="6d4ab-114">父元素</span><span class="sxs-lookup"><span data-stu-id="6d4ab-114">Parent Elements</span></span>  
  
|<span data-ttu-id="6d4ab-115">元素</span><span class="sxs-lookup"><span data-stu-id="6d4ab-115">Element</span></span>|<span data-ttu-id="6d4ab-116">说明</span><span class="sxs-lookup"><span data-stu-id="6d4ab-116">Description</span></span>|  
|-------------|-----------------|  
|[\<host>](host.md)|<span data-ttu-id="6d4ab-117">一个指定服务主机设置的配置元素。</span><span class="sxs-lookup"><span data-stu-id="6d4ab-117">A configuration element that specifies settings for a service host.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="6d4ab-118">请参阅</span><span class="sxs-lookup"><span data-stu-id="6d4ab-118">See also</span></span>

- <xref:System.ServiceModel.Configuration.HostElement>
- <xref:System.ServiceModel.ServiceHost>
- <xref:System.ServiceModel.ServiceHostBase.BaseAddresses%2A>
- [<span data-ttu-id="6d4ab-119">承载</span><span class="sxs-lookup"><span data-stu-id="6d4ab-119">Hosting</span></span>](../../../wcf/feature-details/hosting.md)
