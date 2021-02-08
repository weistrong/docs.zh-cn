---
description: 了解详细 <add> 信息： <baseAddresses>
title: <add> 的 <baseAddresses>
ms.date: 03/30/2017
ms.assetid: 1bd7426f-5f4f-43fc-b8e9-de842219aa32
ms.openlocfilehash: b25a4b5551784ecd8e67569c82c1388a144a9c9f
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99804057"
---
# <a name="add-of-baseaddresses"></a><span data-ttu-id="56af2-103">\<add> 的 \<baseAddresses></span><span class="sxs-lookup"><span data-stu-id="56af2-103">\<add> of \<baseAddresses></span></span>

<span data-ttu-id="56af2-104">表示一个配置元素，该元素指定服务主机所使用的基址。</span><span class="sxs-lookup"><span data-stu-id="56af2-104">Represents a configuration element that specifies the base addresses used by the service host.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<services>**](services.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<service>**](service.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<host>**](host.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<baseAddresses>**](baseaddresses.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<add>**  
  
## <a name="syntax"></a><span data-ttu-id="56af2-105">语法</span><span class="sxs-lookup"><span data-stu-id="56af2-105">Syntax</span></span>  
  
```xml  
<add baseAddress="string" />
```  
  
## <a name="type"></a><span data-ttu-id="56af2-106">类型</span><span class="sxs-lookup"><span data-stu-id="56af2-106">Type</span></span>  

 `Type`  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="56af2-107">特性和元素</span><span class="sxs-lookup"><span data-stu-id="56af2-107">Attributes and Elements</span></span>  

 <span data-ttu-id="56af2-108">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="56af2-108">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="56af2-109">特性</span><span class="sxs-lookup"><span data-stu-id="56af2-109">Attributes</span></span>  
  
|<span data-ttu-id="56af2-110">属性</span><span class="sxs-lookup"><span data-stu-id="56af2-110">Attribute</span></span>|<span data-ttu-id="56af2-111">说明</span><span class="sxs-lookup"><span data-stu-id="56af2-111">Description</span></span>|  
|---------------|-----------------|  
|`baseAddress`|<span data-ttu-id="56af2-112">一个字符串，指定服务主机所使用的基址。</span><span class="sxs-lookup"><span data-stu-id="56af2-112">A string that specifies a base address used by the service host.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="56af2-113">子元素</span><span class="sxs-lookup"><span data-stu-id="56af2-113">Child Elements</span></span>  

 <span data-ttu-id="56af2-114">无。</span><span class="sxs-lookup"><span data-stu-id="56af2-114">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="56af2-115">父元素</span><span class="sxs-lookup"><span data-stu-id="56af2-115">Parent Elements</span></span>  
  
|<span data-ttu-id="56af2-116">元素</span><span class="sxs-lookup"><span data-stu-id="56af2-116">Element</span></span>|<span data-ttu-id="56af2-117">说明</span><span class="sxs-lookup"><span data-stu-id="56af2-117">Description</span></span>|  
|-------------|-----------------|  
|[\<baseAddresses>](baseaddresses.md)|<span data-ttu-id="56af2-118">一个 `baseAddress` 元素集合。</span><span class="sxs-lookup"><span data-stu-id="56af2-118">A collection of `baseAddress` elements.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="56af2-119">请参阅</span><span class="sxs-lookup"><span data-stu-id="56af2-119">See also</span></span>

- <xref:System.ServiceModel.Configuration.HostElement>
- <xref:System.ServiceModel.ServiceHost>
- <xref:System.ServiceModel.ServiceHostBase.BaseAddresses%2A>
- [<span data-ttu-id="56af2-120">承载</span><span class="sxs-lookup"><span data-stu-id="56af2-120">Hosting</span></span>](../../../wcf/feature-details/hosting.md)
