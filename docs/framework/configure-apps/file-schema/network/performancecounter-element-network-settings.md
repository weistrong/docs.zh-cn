---
description: '了解详细信息： <performanceCounters> 元素 (网络设置) '
title: <performanceCounters> 元素（网络设置）
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/system.net/settings/performanceCounters
- http://schemas.microsoft.com/.NetConfiguration/v2.0#performanceCounters
helpviewer_keywords:
- performanceCounters element
ms.assetid: 3afa1586-e1b8-473d-8985-c3fc90cf561b
ms.openlocfilehash: a923ba2420bd15e33f4564a196854fdf9e130e12
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99804109"
---
# <a name="performancecounters-element-network-settings"></a><span data-ttu-id="5bc35-103">\<performanceCounters> 元素（网络设置）</span><span class="sxs-lookup"><span data-stu-id="5bc35-103">\<performanceCounters> Element (Network Settings)</span></span>

<span data-ttu-id="5bc35-104">启用或禁用网络性能计数器。</span><span class="sxs-lookup"><span data-stu-id="5bc35-104">Enables or disables networking performance counters.</span></span>  

[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.net>**](system-net-element-network-settings.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<settings>**](settings-element-network-settings.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<performanceCounters>**

## <a name="syntax"></a><span data-ttu-id="5bc35-105">语法</span><span class="sxs-lookup"><span data-stu-id="5bc35-105">Syntax</span></span>  
  
```xml  
<performanceCounters  
  enabled="true|false"  
/>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="5bc35-106">特性和元素</span><span class="sxs-lookup"><span data-stu-id="5bc35-106">Attributes and Elements</span></span>  

 <span data-ttu-id="5bc35-107">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="5bc35-107">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="5bc35-108">特性</span><span class="sxs-lookup"><span data-stu-id="5bc35-108">Attributes</span></span>  
  
|<span data-ttu-id="5bc35-109">属性</span><span class="sxs-lookup"><span data-stu-id="5bc35-109">Attribute</span></span>|<span data-ttu-id="5bc35-110">说明</span><span class="sxs-lookup"><span data-stu-id="5bc35-110">Description</span></span>|  
|---------------|-----------------|  
|`enabled`|<span data-ttu-id="5bc35-111">指定是否启用网络性能计数器。</span><span class="sxs-lookup"><span data-stu-id="5bc35-111">Specifies whether the networking performance counters are enabled.</span></span> <span data-ttu-id="5bc35-112">默认值是 `false`。</span><span class="sxs-lookup"><span data-stu-id="5bc35-112">The default value is `false`.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="5bc35-113">子元素</span><span class="sxs-lookup"><span data-stu-id="5bc35-113">Child Elements</span></span>  

 <span data-ttu-id="5bc35-114">无。</span><span class="sxs-lookup"><span data-stu-id="5bc35-114">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="5bc35-115">父元素</span><span class="sxs-lookup"><span data-stu-id="5bc35-115">Parent Elements</span></span>  
  
|<span data-ttu-id="5bc35-116">元素</span><span class="sxs-lookup"><span data-stu-id="5bc35-116">Element</span></span>|<span data-ttu-id="5bc35-117">说明</span><span class="sxs-lookup"><span data-stu-id="5bc35-117">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="5bc35-118">设置</span><span class="sxs-lookup"><span data-stu-id="5bc35-118">settings</span></span>](settings-element-network-settings.md)|<span data-ttu-id="5bc35-119">配置 <xref:System.Net> 命名空间的基本网络选项。</span><span class="sxs-lookup"><span data-stu-id="5bc35-119">Configures basic network options for the <xref:System.Net> namespace.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="5bc35-120">备注</span><span class="sxs-lookup"><span data-stu-id="5bc35-120">Remarks</span></span>  

 <span data-ttu-id="5bc35-121">此元素可在应用程序配置文件或计算机配置文件 (Machine.config) 中使用。</span><span class="sxs-lookup"><span data-stu-id="5bc35-121">This element can be used in the application configuration file or the machine configuration file (Machine.config).</span></span>  
  
 <span data-ttu-id="5bc35-122">需要在要使用的配置文件中启用网络性能计数器。</span><span class="sxs-lookup"><span data-stu-id="5bc35-122">Networking performance counters need to be enabled in the configuration file to be used.</span></span> <span data-ttu-id="5bc35-123">通过配置文件中的单个设置即可启用或禁用所有网络性能计数器。</span><span class="sxs-lookup"><span data-stu-id="5bc35-123">All networking performance counters are enabled or disabled with a single setting in the configuration file.</span></span> <span data-ttu-id="5bc35-124">不能启用或禁用单个网络性能计数器。</span><span class="sxs-lookup"><span data-stu-id="5bc35-124">Individual networking performance counters cannot be enabled or disabled.</span></span> <span data-ttu-id="5bc35-125">有关特定的网络性能计数器的详细信息，请参阅 [联网性能计数器](../../../debug-trace-profile/performance-counters.md#networking-performance-counters)。</span><span class="sxs-lookup"><span data-stu-id="5bc35-125">For more information on the specific networking performance counters, see [Networking performance counters](../../../debug-trace-profile/performance-counters.md#networking-performance-counters).</span></span>  
  
 <span data-ttu-id="5bc35-126">默认值是禁用网络性能计数器。</span><span class="sxs-lookup"><span data-stu-id="5bc35-126">The default value is that networking performance counters are disabled.</span></span>  
  
 <span data-ttu-id="5bc35-127"><xref:System.Net.Configuration.PerformanceCountersElement.Enabled%2A?displayProperty=nameWithType>属性可用于从适用的配置文件中获取 **已启用** 属性的当前值。</span><span class="sxs-lookup"><span data-stu-id="5bc35-127">The <xref:System.Net.Configuration.PerformanceCountersElement.Enabled%2A?displayProperty=nameWithType> property can be used to get the current value of the **enabled** attribute from applicable configuration files.</span></span>  
  
## <a name="example"></a><span data-ttu-id="5bc35-128">示例</span><span class="sxs-lookup"><span data-stu-id="5bc35-128">Example</span></span>  

 <span data-ttu-id="5bc35-129">下面的示例演示如何配置 <xref:System.Net> 和相关命名空间，以启用网络性能计数器。</span><span class="sxs-lookup"><span data-stu-id="5bc35-129">The following example shows how to configure the <xref:System.Net> and related namespaces to enable networking performance counters.</span></span>  
  
```xml  
<configuration>  
  <system.net>  
    <settings>  
      <performanceCounters  
        enabled="true"  
      />  
    </settings>  
  </system.net>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="5bc35-130">请参阅</span><span class="sxs-lookup"><span data-stu-id="5bc35-130">See also</span></span>

- <xref:System.Net.Configuration.PerformanceCountersElement?displayProperty=nameWithType>
- <xref:System.Net.Configuration.PerformanceCountersElement.Enabled%2A?displayProperty=nameWithType>
- [<span data-ttu-id="5bc35-131">网络设置架构</span><span class="sxs-lookup"><span data-stu-id="5bc35-131">Network Settings Schema</span></span>](index.md)
- [<span data-ttu-id="5bc35-132">网络性能计数器</span><span class="sxs-lookup"><span data-stu-id="5bc35-132">Networking Performance Counters</span></span>](../../../debug-trace-profile/performance-counters.md#networking-performance-counters)
