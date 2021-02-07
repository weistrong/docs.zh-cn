---
description: '了解详细信息： <defaultHttpCachePolicy> 元素 (网络设置) '
title: <defaultHttpCachePolicy> 元素（网络设置）
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/system.net/requestCaching/defaultHttpCachePolicy
- http://schemas.microsoft.com/.NetConfiguration/v2.0#defaultHttpCachePolicy
helpviewer_keywords:
- defaultHttpCachePolicy element
- <defaultHttpCachePolicy> element
ms.assetid: 2c1247d0-39b0-4c12-919a-a925ce075c79
ms.openlocfilehash: d2df27c9b140c9bdb4def49aef7de1a3d80f4a11
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99740322"
---
# <a name="defaulthttpcachepolicy-element-network-settings"></a><span data-ttu-id="87ed4-103">\<defaultHttpCachePolicy> 元素（网络设置）</span><span class="sxs-lookup"><span data-stu-id="87ed4-103">\<defaultHttpCachePolicy> Element (Network Settings)</span></span>

<span data-ttu-id="87ed4-104">描述 HTTP 缓存是否处于活动状态，并描述默认缓存策略。</span><span class="sxs-lookup"><span data-stu-id="87ed4-104">Describes whether HTTP caching is active and describes the default caching policy.</span></span>  

[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.net>**](system-net-element-network-settings.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<requestCaching>**](requestcaching-element-network-settings.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<defaultHttpCachePolicy>**

## <a name="syntax"></a><span data-ttu-id="87ed4-105">语法</span><span class="sxs-lookup"><span data-stu-id="87ed4-105">Syntax</span></span>  
  
```xml  
<defaultHttpCachePolicy  
  policyLevel="BypassCache|Default"  
  minimumFresh="d.hh:mm:ss|minValue|maxValue"  
  maximumAge="d.hh:mm:ss|minValue|maxValue"  
  maximumStale="d.hh:mm:ss|minValue|maxValue"  
/>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="87ed4-106">特性和元素</span><span class="sxs-lookup"><span data-stu-id="87ed4-106">Attributes and Elements</span></span>  

 <span data-ttu-id="87ed4-107">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="87ed4-107">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="87ed4-108">特性</span><span class="sxs-lookup"><span data-stu-id="87ed4-108">Attributes</span></span>  
  
|<span data-ttu-id="87ed4-109">属性</span><span class="sxs-lookup"><span data-stu-id="87ed4-109">Attribute</span></span>|<span data-ttu-id="87ed4-110">说明</span><span class="sxs-lookup"><span data-stu-id="87ed4-110">Description</span></span>|  
|---------------|-----------------|  
|`maximumAge`|<span data-ttu-id="87ed4-111">指定将缓存的对象标记为过期之前的最大时间间隔。</span><span class="sxs-lookup"><span data-stu-id="87ed4-111">Specifies the maximum time interval before a cached object is marked as expired.</span></span>|  
|`maximumStale`|<span data-ttu-id="87ed4-112">指定在将缓存对象标记为过期之前计算的新鲜度时间之后的最长时间。</span><span class="sxs-lookup"><span data-stu-id="87ed4-112">Specifies the maximum time past the computed freshness time before a cached object is marked as expired.</span></span>|  
|`minimumFresh`|<span data-ttu-id="87ed4-113">指定将缓存的对象视为最新的最短时间。</span><span class="sxs-lookup"><span data-stu-id="87ed4-113">Specifies the minimum time for a cached object to be considered fresh.</span></span>|  
|`policyLevel`|<span data-ttu-id="87ed4-114">指定缓存策略是否为自动，或是否绕过缓存。</span><span class="sxs-lookup"><span data-stu-id="87ed4-114">Specifies whether the caching policy is automatic, or whether the cache is bypassed.</span></span> <span data-ttu-id="87ed4-115">默认值是 `BypassCache`。</span><span class="sxs-lookup"><span data-stu-id="87ed4-115">The default value is `BypassCache`.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="87ed4-116">子元素</span><span class="sxs-lookup"><span data-stu-id="87ed4-116">Child Elements</span></span>  

 <span data-ttu-id="87ed4-117">无</span><span class="sxs-lookup"><span data-stu-id="87ed4-117">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="87ed4-118">父元素</span><span class="sxs-lookup"><span data-stu-id="87ed4-118">Parent Elements</span></span>  
  
|<span data-ttu-id="87ed4-119">元素</span><span class="sxs-lookup"><span data-stu-id="87ed4-119">Element</span></span>|<span data-ttu-id="87ed4-120">说明</span><span class="sxs-lookup"><span data-stu-id="87ed4-120">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="87ed4-121">requestCaching</span><span class="sxs-lookup"><span data-stu-id="87ed4-121">requestCaching</span></span>](requestcaching-element-network-settings.md)|<span data-ttu-id="87ed4-122">控制网络请求的缓存机制。</span><span class="sxs-lookup"><span data-stu-id="87ed4-122">Controls the caching mechanism for network requests.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="87ed4-123">备注</span><span class="sxs-lookup"><span data-stu-id="87ed4-123">Remarks</span></span>  

 <span data-ttu-id="87ed4-124">特性的值 `policyLevel` 为 `BypassCache` 或 `Default` 。</span><span class="sxs-lookup"><span data-stu-id="87ed4-124">The value for the `policyLevel` attribute is either `BypassCache` or `Default`.</span></span>  
  
 <span data-ttu-id="87ed4-125">`maximumAge`、 `maximumStale` 和元素的值 `minimumFresh` 是格式为 *d* 的显式时间间隔。*hh*：*mm*：*ss* (天、小时、分钟和秒) ，或相应的常量 `minValue` 或 `maxValue` 。</span><span class="sxs-lookup"><span data-stu-id="87ed4-125">Values for the `maximumAge`, `maximumStale`, and `minimumFresh` elements are either an explicit time interval with a format of *d*.*hh*:*mm*:*ss* (days, hours, minutes, and seconds), or the constants `minValue` or `maxValue`, as appropriate.</span></span>  
  
## <a name="configuration-files"></a><span data-ttu-id="87ed4-126">配置文件</span><span class="sxs-lookup"><span data-stu-id="87ed4-126">Configuration Files</span></span>  

 <span data-ttu-id="87ed4-127">此元素可在应用程序配置文件或计算机配置文件 (Machine.config) 中使用。</span><span class="sxs-lookup"><span data-stu-id="87ed4-127">This element can be used in the application configuration file or the machine configuration file (Machine.config).</span></span>  
  
## <a name="example"></a><span data-ttu-id="87ed4-128">示例</span><span class="sxs-lookup"><span data-stu-id="87ed4-128">Example</span></span>  

 <span data-ttu-id="87ed4-129">下面的示例演示如何指定最小的最短时间为6小时，最长生存期为两天，最大陈旧时间为四小时。</span><span class="sxs-lookup"><span data-stu-id="87ed4-129">The following example shows how to specify a minimum fresh time of six hours, a maximum age time of two days, and a maximum stale time of four hours.</span></span>  
  
```xml  
<configuration>  
  <system.net>  
    <requestCaching>  
      <defaultHttpCachePolicy  
        minimumFresh="0.06:00:00"  
        maximumAge="2.00:00:00"  
        maximumStale="0.04:00:00"
      />  
    </requestCaching>  
  </system.net>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="87ed4-130">请参阅</span><span class="sxs-lookup"><span data-stu-id="87ed4-130">See also</span></span>

- <xref:System.Net.Cache>
- <xref:System.Net.WebRequest>
- <xref:System.Net.Cache.RequestCacheLevel>
- [<span data-ttu-id="87ed4-131">网络设置架构</span><span class="sxs-lookup"><span data-stu-id="87ed4-131">Network Settings Schema</span></span>](index.md)
