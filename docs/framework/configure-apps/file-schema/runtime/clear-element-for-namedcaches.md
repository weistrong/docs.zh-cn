---
description: 详细了解： <clear> 的元素 <namedCaches>
title: <namedCaches> 的 <clear> 元素
ms.date: 03/30/2017
helpviewer_keywords:
- <clear> element for <namedCaches>
- clear element for <namedCaches>
ms.assetid: ea01a858-65da-4348-800f-5e3df59d4d79
ms.openlocfilehash: 9d883c102fc76875ce155f353920f730bf9700c4
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99719092"
---
# <a name="clear-element-for-namedcaches"></a><span data-ttu-id="71d7c-103">\<namedCaches> 的 \<clear> 元素</span><span class="sxs-lookup"><span data-stu-id="71d7c-103">\<clear> Element for \<namedCaches></span></span>

<span data-ttu-id="71d7c-104">清除 `namedCache` 内存缓存的集合中的所有项 `namedCaches` 。</span><span class="sxs-lookup"><span data-stu-id="71d7c-104">Clears all `namedCache` entries in the `namedCaches` collection for a memory cache.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.runtime.caching>**](system-runtime-caching-element-cache-settings.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<memoryCache>**](memorycache-element-cache-settings.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<namedCaches>**](namedcaches-element-cache-settings.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<clear>**  
  
## <a name="syntax"></a><span data-ttu-id="71d7c-105">语法</span><span class="sxs-lookup"><span data-stu-id="71d7c-105">Syntax</span></span>  
  
```xml  
<namedCaches>  
    <clear name="Default" />  
    <!-- child elements -->  
 </namedCaches>  
```  
  
## <a name="type"></a><span data-ttu-id="71d7c-106">类型</span><span class="sxs-lookup"><span data-stu-id="71d7c-106">Type</span></span>  

 `Type`  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="71d7c-107">特性和元素</span><span class="sxs-lookup"><span data-stu-id="71d7c-107">Attributes and Elements</span></span>  

 <span data-ttu-id="71d7c-108">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="71d7c-108">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="71d7c-109">特性</span><span class="sxs-lookup"><span data-stu-id="71d7c-109">Attributes</span></span>  

 `None`  
  
### <a name="child-elements"></a><span data-ttu-id="71d7c-110">子元素</span><span class="sxs-lookup"><span data-stu-id="71d7c-110">Child Elements</span></span>  

 `None`  
  
### <a name="parent-elements"></a><span data-ttu-id="71d7c-111">父元素</span><span class="sxs-lookup"><span data-stu-id="71d7c-111">Parent Elements</span></span>  
  
|<span data-ttu-id="71d7c-112">元素</span><span class="sxs-lookup"><span data-stu-id="71d7c-112">Element</span></span>|<span data-ttu-id="71d7c-113">说明</span><span class="sxs-lookup"><span data-stu-id="71d7c-113">Description</span></span>|  
|-------------|-----------------|  
|[\<namedCaches>](namedcaches-element-cache-settings.md)|<span data-ttu-id="71d7c-114">包含命名实例的配置设置的集合 <xref:System.Runtime.Caching.MemoryCache> 。</span><span class="sxs-lookup"><span data-stu-id="71d7c-114">Contains a collection of configuration settings for the named <xref:System.Runtime.Caching.MemoryCache> instances.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="71d7c-115">备注</span><span class="sxs-lookup"><span data-stu-id="71d7c-115">Remarks</span></span>  

 <span data-ttu-id="71d7c-116">`clear`元素清除 `namedCache` 内存缓存的命名缓存集合中的所有项。</span><span class="sxs-lookup"><span data-stu-id="71d7c-116">The `clear` element clears all `namedCache` entries in the named cache collection for a memory cache.</span></span> <span data-ttu-id="71d7c-117">在 `clear` 使用 `add` 元素添加新的命名缓存条目之前，可以使用元素，以便确定集合中没有其他命名缓存。</span><span class="sxs-lookup"><span data-stu-id="71d7c-117">You can use the `clear` element before you use the `add` element to add a new named cache entry in order to be certain there are no other named caches in the collection.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="71d7c-118">请参阅</span><span class="sxs-lookup"><span data-stu-id="71d7c-118">See also</span></span>

- [<span data-ttu-id="71d7c-119">\<namedCaches> 元素 (缓存设置) </span><span class="sxs-lookup"><span data-stu-id="71d7c-119">\<namedCaches> Element (Cache Settings)</span></span>](namedcaches-element-cache-settings.md)
