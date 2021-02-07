---
description: '了解详细信息： <requestCaching> 元素 (网络设置) '
title: <requestCaching> 元素（网络设置）
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#requestCaching
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/system.net/requestCaching
helpviewer_keywords:
- requestCaching element
- <requestCaching> element
ms.assetid: 9962a2fe-cbda-41a6-9377-571811eaea84
ms.openlocfilehash: d09da8ad7a38ac363aaa740cca4de25e33fa8c56
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99698552"
---
# <a name="requestcaching-element-network-settings"></a><span data-ttu-id="bcc2c-103">\<requestCaching> 元素（网络设置）</span><span class="sxs-lookup"><span data-stu-id="bcc2c-103">\<requestCaching> Element (Network Settings)</span></span>

<span data-ttu-id="bcc2c-104">控制网络请求的缓存机制。</span><span class="sxs-lookup"><span data-stu-id="bcc2c-104">Controls the caching mechanism for network requests.</span></span>  
  
[**\<configuration>**](../configuration-element.md)  
&nbsp;&nbsp;[**\<system.net>**](system-net-element-network-settings.md)  
&nbsp;&nbsp;&nbsp;&nbsp;**\<requestCaching>**  
  
## <a name="syntax"></a><span data-ttu-id="bcc2c-105">语法</span><span class="sxs-lookup"><span data-stu-id="bcc2c-105">Syntax</span></span>  
  
```xml  
<requestCaching  
  isPrivateCache ="true|false"  
  disableAllCaching="true|false"  
  defaultPolicyLevel="BypassCache|Default|CacheOnly|CacheIfAvailable|Revalidate|Reload|NoCacheNoStore|Revalidate"  
  unspecifiedMaximumAge= "d.hh:mm:ss">  
    <defaultHttpCachePolicy>...</defaultHttpCachePolicy>  
    <defaultFtpCachePolicy>...</defaultFtpCachePolicy>  
</requestCaching>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="bcc2c-106">特性和元素</span><span class="sxs-lookup"><span data-stu-id="bcc2c-106">Attributes and Elements</span></span>  

 <span data-ttu-id="bcc2c-107">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="bcc2c-107">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="bcc2c-108">特性</span><span class="sxs-lookup"><span data-stu-id="bcc2c-108">Attributes</span></span>  
  
|<span data-ttu-id="bcc2c-109">属性</span><span class="sxs-lookup"><span data-stu-id="bcc2c-109">Attribute</span></span>|<span data-ttu-id="bcc2c-110">说明</span><span class="sxs-lookup"><span data-stu-id="bcc2c-110">Description</span></span>|  
|---------------|-----------------|  
|`isPrivateCache`|<span data-ttu-id="bcc2c-111">指定缓存是否在不同用户的信息之间提供隔离。</span><span class="sxs-lookup"><span data-stu-id="bcc2c-111">Specifies whether the cache provides isolation between the information of different users.</span></span> <span data-ttu-id="bcc2c-112">默认值是 `true`。</span><span class="sxs-lookup"><span data-stu-id="bcc2c-112">The default value is `true`.</span></span> <span data-ttu-id="bcc2c-113">此值应该 `false` 适用于中间层应用程序。</span><span class="sxs-lookup"><span data-stu-id="bcc2c-113">This value should be `false` for middle tier applications.</span></span>|  
|`disableAllCaching`|<span data-ttu-id="bcc2c-114">指定为所有 Web 响应禁用缓存，且不能以编程方式重写。</span><span class="sxs-lookup"><span data-stu-id="bcc2c-114">Specifies that caching is disabled for all Web responses, and cannot be overridden programmatically.</span></span>|  
|`defaultPolicyLevel`|<span data-ttu-id="bcc2c-115"><xref:System.Net.Cache.RequestCacheLevel> 枚举中的值之一。</span><span class="sxs-lookup"><span data-stu-id="bcc2c-115">One of the values in the <xref:System.Net.Cache.RequestCacheLevel> enumeration.</span></span> <span data-ttu-id="bcc2c-116">默认值是 `BypassCache`。</span><span class="sxs-lookup"><span data-stu-id="bcc2c-116">The default value is `BypassCache`.</span></span>|  
|`unspecifiedMaximumAge`|<span data-ttu-id="bcc2c-117">指定将内容标记为过期的默认时间。</span><span class="sxs-lookup"><span data-stu-id="bcc2c-117">Specifies the default time after which content is marked as expired.</span></span>|  
  
## <a name="policylevel-attribute"></a><span data-ttu-id="bcc2c-118">policyLevel 特性</span><span class="sxs-lookup"><span data-stu-id="bcc2c-118">policyLevel Attribute</span></span>  
  
|<span data-ttu-id="bcc2c-119">值</span><span class="sxs-lookup"><span data-stu-id="bcc2c-119">Value</span></span>|<span data-ttu-id="bcc2c-120">说明</span><span class="sxs-lookup"><span data-stu-id="bcc2c-120">Description</span></span>|  
|-----------|-----------------|  
|`Default`|<span data-ttu-id="bcc2c-121">如果资源是最新的，则返回缓存的资源，内容长度准确，并且存在过期、修改和内容长度属性。</span><span class="sxs-lookup"><span data-stu-id="bcc2c-121">Returns the cached resource if the resource is fresh, the content length is accurate, and the expiration, modification, and content length attributes are present.</span></span>|  
|`BypassCache`|<span data-ttu-id="bcc2c-122">从服务器返回资源。</span><span class="sxs-lookup"><span data-stu-id="bcc2c-122">Returns the resource from the server.</span></span>|  
|`CacheOnly`|<span data-ttu-id="bcc2c-123">如果内容长度存在并且与条目大小匹配，则返回缓存的资源。</span><span class="sxs-lookup"><span data-stu-id="bcc2c-123">Returns the cached resource if the content length is present and matches the entry size.</span></span>|  
|`CacheIfAvailable`|<span data-ttu-id="bcc2c-124">如果提供了内容长度并与条目大小匹配，则返回缓存的资源;否则，将从服务器下载资源，并将其返回给调用方。</span><span class="sxs-lookup"><span data-stu-id="bcc2c-124">Returns the cached resource if the content length is provided and matches the entry size; otherwise, the resource is downloaded from the server and is returned to the caller.</span></span>|  
|`Revalidate`|<span data-ttu-id="bcc2c-125">如果缓存资源的时间戳与服务器上资源的时间戳相同，则返回缓存的资源;否则，将从服务器下载资源，并将其存储在缓存中，并将其返回给调用方。</span><span class="sxs-lookup"><span data-stu-id="bcc2c-125">Returns the cached resource if the timestamp of the cached resource is the same as the timestamp of the resource on the server; otherwise, the resource is downloaded from the server, stored in the cache, and is returned to the caller.</span></span>|  
|`Reload`|<span data-ttu-id="bcc2c-126">从服务器下载资源，将其存储在缓存中，并将资源返回给调用方。</span><span class="sxs-lookup"><span data-stu-id="bcc2c-126">Downloads the resource from the server, stores it in the cache, and returns the resource to the caller.</span></span>|  
|`NoCacheNoStore`|<span data-ttu-id="bcc2c-127">如果缓存的资源存在，则将其删除。</span><span class="sxs-lookup"><span data-stu-id="bcc2c-127">If a cached resource exists, it is deleted.</span></span> <span data-ttu-id="bcc2c-128">从服务器下载资源，并将其返回给调用方。</span><span class="sxs-lookup"><span data-stu-id="bcc2c-128">The resource is downloaded from the server and is returned to the caller.</span></span>|  
|`Revalidate`|<span data-ttu-id="bcc2c-129">如果时间戳与服务器上资源的时间戳相同，则使用资源的缓存副本满足请求;否则，会从服务器下载资源，并将其提供给调用方，并存储在缓存中。</span><span class="sxs-lookup"><span data-stu-id="bcc2c-129">Satisfies a request by using the cached copy of the resource if the timestamp is the same as the timestamp of the resource on the server; otherwise, the resource is downloaded from the server, presented to the caller, and is stored in the cache,</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="bcc2c-130">子元素</span><span class="sxs-lookup"><span data-stu-id="bcc2c-130">Child Elements</span></span>  
  
|<span data-ttu-id="bcc2c-131">元素</span><span class="sxs-lookup"><span data-stu-id="bcc2c-131">Element</span></span>|<span data-ttu-id="bcc2c-132">说明</span><span class="sxs-lookup"><span data-stu-id="bcc2c-132">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="bcc2c-133">defaultHttpCachePolicy</span><span class="sxs-lookup"><span data-stu-id="bcc2c-133">defaultHttpCachePolicy</span></span>](defaulthttpcachepolicy-element-network-settings.md)|<span data-ttu-id="bcc2c-134">可选元素。</span><span class="sxs-lookup"><span data-stu-id="bcc2c-134">Optional element.</span></span><br /><br /> <span data-ttu-id="bcc2c-135">描述 HTTP 缓存是否处于活动状态，并描述默认缓存策略。</span><span class="sxs-lookup"><span data-stu-id="bcc2c-135">Describes whether HTTP caching is active and describes the default caching policy.</span></span>|  
|[<span data-ttu-id="bcc2c-136">\<defaultFtpCachePolicy> 元素（网络设置）</span><span class="sxs-lookup"><span data-stu-id="bcc2c-136">\<defaultFtpCachePolicy> Element (Network Settings)</span></span>](defaultftpcachepolicy-element-network-settings.md)|<span data-ttu-id="bcc2c-137">可选元素。</span><span class="sxs-lookup"><span data-stu-id="bcc2c-137">Optional element.</span></span><br /><br /> <span data-ttu-id="bcc2c-138">介绍 FTP 缓存是否处于活动状态，并描述默认缓存策略。</span><span class="sxs-lookup"><span data-stu-id="bcc2c-138">Describes whether FTP caching is active and describes the default caching policy.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="bcc2c-139">父元素</span><span class="sxs-lookup"><span data-stu-id="bcc2c-139">Parent Elements</span></span>  
  
|<span data-ttu-id="bcc2c-140">元素</span><span class="sxs-lookup"><span data-stu-id="bcc2c-140">Element</span></span>|<span data-ttu-id="bcc2c-141">说明</span><span class="sxs-lookup"><span data-stu-id="bcc2c-141">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="bcc2c-142">system.net</span><span class="sxs-lookup"><span data-stu-id="bcc2c-142">system.net</span></span>](system-net-element-network-settings.md)|<span data-ttu-id="bcc2c-143">包含指定 .NET Framework 如何连接到网络的设置。</span><span class="sxs-lookup"><span data-stu-id="bcc2c-143">Contains settings that specify how the .NET Framework connects to the network.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="bcc2c-144">示例</span><span class="sxs-lookup"><span data-stu-id="bcc2c-144">Example</span></span>  

 <span data-ttu-id="bcc2c-145">下面的示例演示如何禁用所有缓存。</span><span class="sxs-lookup"><span data-stu-id="bcc2c-145">The following example shows how to disable all caching.</span></span>  
  
```xml  
<configuration>  
  <system.net>  
    <requestCaching  
      disableAllCaching="true"  
    />  
  </system.net>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="bcc2c-146">请参阅</span><span class="sxs-lookup"><span data-stu-id="bcc2c-146">See also</span></span>

- <xref:System.Net.Cache?displayProperty=nameWithType>
- [<span data-ttu-id="bcc2c-147">网络设置架构</span><span class="sxs-lookup"><span data-stu-id="bcc2c-147">Network Settings Schema</span></span>](index.md)
