---
description: 详细了解： <remove> 的元素 <namedCaches>
title: <namedCaches> 的 <remove> 元素
ms.date: 03/30/2017
helpviewer_keywords:
- remove element for namedCaches
- <remove> element for namedCaches
ms.assetid: 24211ea5-163e-4fe5-aed8-004d8499760c
ms.openlocfilehash: 5b39fc596735d746c52cdb5623962f5b9952fa3e
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99802455"
---
# <a name="remove-element-for-namedcaches"></a><span data-ttu-id="9650a-103">\<namedCaches> 的 \<remove> 元素</span><span class="sxs-lookup"><span data-stu-id="9650a-103">\<remove> Element for \<namedCaches></span></span>

<span data-ttu-id="9650a-104">从内存缓存的 `namedCaches` 集合中删除一个命名的缓存条目。</span><span class="sxs-lookup"><span data-stu-id="9650a-104">Removes a named cache entry from the `namedCaches` collection for a memory cache.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.runtime.caching>**](system-runtime-caching-element-cache-settings.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<memoryCache>**](memorycache-element-cache-settings.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<namedCaches>**](namedcaches-element-cache-settings.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<remove>**  
  
## <a name="syntax"></a><span data-ttu-id="9650a-105">语法</span><span class="sxs-lookup"><span data-stu-id="9650a-105">Syntax</span></span>  
  
```xml  
<namedCaches>  
    <remove name="default" />  
    <!-- child elements -->  
 </namedCaches>  
```  
  
## <a name="type"></a><span data-ttu-id="9650a-106">类型</span><span class="sxs-lookup"><span data-stu-id="9650a-106">Type</span></span>  

 `None`  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="9650a-107">特性和元素</span><span class="sxs-lookup"><span data-stu-id="9650a-107">Attributes and Elements</span></span>  

 <span data-ttu-id="9650a-108">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="9650a-108">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="9650a-109">特性</span><span class="sxs-lookup"><span data-stu-id="9650a-109">Attributes</span></span>  

 `None`  
  
### <a name="child-elements"></a><span data-ttu-id="9650a-110">子元素</span><span class="sxs-lookup"><span data-stu-id="9650a-110">Child Elements</span></span>  

 `None`  
  
### <a name="parent-elements"></a><span data-ttu-id="9650a-111">父元素</span><span class="sxs-lookup"><span data-stu-id="9650a-111">Parent Elements</span></span>  
  
|<span data-ttu-id="9650a-112">元素</span><span class="sxs-lookup"><span data-stu-id="9650a-112">Element</span></span>|<span data-ttu-id="9650a-113">说明</span><span class="sxs-lookup"><span data-stu-id="9650a-113">Description</span></span>|  
|-------------|-----------------|  
|[\<namedCaches>](namedcaches-element-cache-settings.md)|<span data-ttu-id="9650a-114">包含命名实例的配置设置的集合 <xref:System.Runtime.Caching.MemoryCache> 。</span><span class="sxs-lookup"><span data-stu-id="9650a-114">Contains a collection of configuration settings for the named <xref:System.Runtime.Caching.MemoryCache> instances.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="9650a-115">备注</span><span class="sxs-lookup"><span data-stu-id="9650a-115">Remarks</span></span>  

 <span data-ttu-id="9650a-116">`remove`元素 `namedCache` 从内存缓存的命名缓存集合中删除一个条目。</span><span class="sxs-lookup"><span data-stu-id="9650a-116">The `remove` element removes a `namedCache` entry from the named cache collection for a memory cache.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9650a-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="9650a-117">See also</span></span>

- [<span data-ttu-id="9650a-118">\<namedCaches> 元素 (缓存设置) </span><span class="sxs-lookup"><span data-stu-id="9650a-118">\<namedCaches> Element (Cache Settings)</span></span>](namedcaches-element-cache-settings.md)
