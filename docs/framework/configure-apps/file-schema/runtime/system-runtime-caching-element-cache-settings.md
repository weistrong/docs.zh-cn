---
description: '了解详细信息： <> 元素 (缓存设置) '
title: <system.runtime.caching> 元素（缓存设置）
ms.date: 03/30/2017
helpviewer_keywords:
- <system.runtime.caching> element
- caching [.NET Framework], configuration
- system.runtime.caching element
ms.assetid: 9b44daee-874a-4bd1-954e-83bf53565590
ms.openlocfilehash: 602d863caedef5c1334948b25b0caa2b0e35f685
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99652726"
---
# <a name="systemruntimecaching-element-cache-settings"></a><span data-ttu-id="10ffe-103">\<system.runtime.caching> 元素（缓存设置）</span><span class="sxs-lookup"><span data-stu-id="10ffe-103">\<system.runtime.caching> Element (Cache Settings)</span></span>

<span data-ttu-id="10ffe-104">通过配置文件中的 <xref:System.Runtime.Caching.ObjectCache> 条目为默认内存中的 `memoryCache` 实现提供配置。</span><span class="sxs-lookup"><span data-stu-id="10ffe-104">Provides configuration for the default in-memory <xref:System.Runtime.Caching.ObjectCache> implementation through the `memoryCache` entry in the configuration file.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;**\<system.runtime.caching>**  
  
## <a name="syntax"></a><span data-ttu-id="10ffe-105">语法</span><span class="sxs-lookup"><span data-stu-id="10ffe-105">Syntax</span></span>  
  
```xml  
<system.runtime.caching >  
   <!-- child elements -->  
</system.runtime.caching >  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="10ffe-106">特性和元素</span><span class="sxs-lookup"><span data-stu-id="10ffe-106">Attributes and Elements</span></span>

<span data-ttu-id="10ffe-107">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="10ffe-107">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="10ffe-108">特性</span><span class="sxs-lookup"><span data-stu-id="10ffe-108">Attributes</span></span>

`None`  

### <a name="child-elements"></a><span data-ttu-id="10ffe-109">子元素</span><span class="sxs-lookup"><span data-stu-id="10ffe-109">Child Elements</span></span>

|<span data-ttu-id="10ffe-110">元素</span><span class="sxs-lookup"><span data-stu-id="10ffe-110">Element</span></span>|<span data-ttu-id="10ffe-111">说明</span><span class="sxs-lookup"><span data-stu-id="10ffe-111">Description</span></span>|  
|-------------|-----------------|  
|[\<memoryCache>](memorycache-element-cache-settings.md)|<span data-ttu-id="10ffe-112">定义一个用于配置基于 <xref:System.Runtime.Caching.MemoryCache> 类的缓存的元素。</span><span class="sxs-lookup"><span data-stu-id="10ffe-112">Defines an element that is used to configure a cache that is based on the <xref:System.Runtime.Caching.MemoryCache> class.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="10ffe-113">父元素</span><span class="sxs-lookup"><span data-stu-id="10ffe-113">Parent Elements</span></span>  
  
|<span data-ttu-id="10ffe-114">元素</span><span class="sxs-lookup"><span data-stu-id="10ffe-114">Element</span></span>|<span data-ttu-id="10ffe-115">说明</span><span class="sxs-lookup"><span data-stu-id="10ffe-115">Description</span></span>|  
|-------------|-----------------|  
|[\<configuration>](../configuration-element.md)|<span data-ttu-id="10ffe-116">指定公共语言运行时和 .NET Framework 应用程序所使用的每个配置文件中的根元素。</span><span class="sxs-lookup"><span data-stu-id="10ffe-116">Specifies the root element in every configuration file that is used by the common language runtime and .NET Framework applications.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="10ffe-117">备注</span><span class="sxs-lookup"><span data-stu-id="10ffe-117">Remarks</span></span>

<span data-ttu-id="10ffe-118">此命名空间中的类提供一种使用诸如 ASP.NET 中缓存功能的方法，但不会在 `System.Web` 程序集上产生依赖。</span><span class="sxs-lookup"><span data-stu-id="10ffe-118">The classes in this namespace provide a way to use caching facilities like those in ASP.NET, but without a dependency on the `System.Web` assembly.</span></span> <span data-ttu-id="10ffe-119">有关详细信息，请参阅 [Caching in .NET Framework Applications](../../../performance/caching-in-net-framework-applications.md)。</span><span class="sxs-lookup"><span data-stu-id="10ffe-119">For more information, see [Caching in .NET Framework Applications](../../../performance/caching-in-net-framework-applications.md).</span></span>  
  
> [!NOTE]
> <span data-ttu-id="10ffe-120">命名空间中的输出缓存功能和类型 <xref:System.Runtime.Caching> 是 .NET Framework 4 中的新增功能。</span><span class="sxs-lookup"><span data-stu-id="10ffe-120">The output caching functionality and types in the <xref:System.Runtime.Caching> namespace are new in .NET Framework 4.</span></span>  
  
## <a name="example"></a><span data-ttu-id="10ffe-121">示例</span><span class="sxs-lookup"><span data-stu-id="10ffe-121">Example</span></span>

<span data-ttu-id="10ffe-122">下面的示例演示如何配置基于 <xref:System.Runtime.Caching.MemoryCache> 类的缓存。</span><span class="sxs-lookup"><span data-stu-id="10ffe-122">The following example shows how to configure a cache that is based on the <xref:System.Runtime.Caching.MemoryCache> class.</span></span> <span data-ttu-id="10ffe-123">该示例演示如何为内存缓存配置 `namedCaches` 条目实例。</span><span class="sxs-lookup"><span data-stu-id="10ffe-123">The example shows how to configure an instance of the `namedCaches` entry for memory cache.</span></span> <span data-ttu-id="10ffe-124">缓存的名称设置为默认缓存项名称，方法是将 `name` 属性设置为 "default"。</span><span class="sxs-lookup"><span data-stu-id="10ffe-124">The name of the cache is set to the default cache entry name by setting the `name` attribute to "Default".</span></span>  
  
<span data-ttu-id="10ffe-125">将 `cacheMemoryLimitMegabytes` 属性和 `physicalMemoryPercentage` 属性设置为零。</span><span class="sxs-lookup"><span data-stu-id="10ffe-125">The `cacheMemoryLimitMegabytes` attribute and the `physicalMemoryPercentage` attribute are set to zero.</span></span> <span data-ttu-id="10ffe-126">将这些特性设置为零意味着默认情况下使用 <xref:System.Runtime.Caching.MemoryCache> 自动调整大小试探法。</span><span class="sxs-lookup"><span data-stu-id="10ffe-126">Setting these attributes to zero means that the <xref:System.Runtime.Caching.MemoryCache> autosizing heuristics are used by default.</span></span> <span data-ttu-id="10ffe-127">每隔两分钟，缓存实现应对当前内存负载和基于百分比的绝对内存限制进行比较。</span><span class="sxs-lookup"><span data-stu-id="10ffe-127">The cache implementation should compare the current memory load against the absolute and percentage-based memory limits every two minutes.</span></span>  
  
```xml  
<configuration>  
  <system.runtime.caching>  
    <memoryCache>  
      <namedCaches>  
          <add name="Default"
               cacheMemoryLimitMegabytes="0"
               physicalMemoryLimitPercentage="0"  
               pollingInterval="00:02:00" />  
      </namedCaches>  
    </memoryCache>  
  </system.runtime.caching>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="10ffe-128">请参阅</span><span class="sxs-lookup"><span data-stu-id="10ffe-128">See also</span></span>

- [<span data-ttu-id="10ffe-129">\<memoryCache> 元素 (缓存设置) </span><span class="sxs-lookup"><span data-stu-id="10ffe-129">\<memoryCache> Element (Cache Settings)</span></span>](memorycache-element-cache-settings.md)
