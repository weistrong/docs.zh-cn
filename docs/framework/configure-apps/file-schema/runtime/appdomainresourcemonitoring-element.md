---
description: 了解详细信息： <appDomainResourceMonitoring> 元素
title: <appDomainResourceMonitoring> 元素
ms.date: 03/30/2017
helpviewer_keywords:
- appDomainResourceMonitoring element
- <appDomainResourceMonitoring> element
ms.assetid: 02119ab6-1e91-448e-97ad-e7b2e5c4bbbd
ms.openlocfilehash: aee85386e6d0af2ca4fd30c0ad8fe69bae240315
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99719287"
---
# <a name="appdomainresourcemonitoring-element"></a><span data-ttu-id="5b72c-103">\<appDomainResourceMonitoring> 元素</span><span class="sxs-lookup"><span data-stu-id="5b72c-103">\<appDomainResourceMonitoring> Element</span></span>

<span data-ttu-id="5b72c-104">指示运行时在过程的生命周期过程中收集所有应用程序域的统计数据。</span><span class="sxs-lookup"><span data-stu-id="5b72c-104">Instructs the runtime to collect statistics on all application domains in the process for the life of the process.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<runtime>**](runtime-element.md)\
&nbsp;&nbsp;&nbsp;&nbsp;**\<appDomainResourceMonitoring>**  
  
## <a name="syntax"></a><span data-ttu-id="5b72c-105">语法</span><span class="sxs-lookup"><span data-stu-id="5b72c-105">Syntax</span></span>  
  
```xml  
<appDomainResourceMonitoring
   enabled="true|false"/>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="5b72c-106">特性和元素</span><span class="sxs-lookup"><span data-stu-id="5b72c-106">Attributes and Elements</span></span>  

 <span data-ttu-id="5b72c-107">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="5b72c-107">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="5b72c-108">特性</span><span class="sxs-lookup"><span data-stu-id="5b72c-108">Attributes</span></span>  
  
|<span data-ttu-id="5b72c-109">属性</span><span class="sxs-lookup"><span data-stu-id="5b72c-109">Attribute</span></span>|<span data-ttu-id="5b72c-110">描述</span><span class="sxs-lookup"><span data-stu-id="5b72c-110">Description</span></span>|  
|---------------|-----------------|  
|`enabled`|<span data-ttu-id="5b72c-111">必需的特性。</span><span class="sxs-lookup"><span data-stu-id="5b72c-111">Required attribute.</span></span><br /><br /> <span data-ttu-id="5b72c-112">指定运行时是否收集应用程序域资源监视的统计信息。</span><span class="sxs-lookup"><span data-stu-id="5b72c-112">Specifies whether the runtime collects statistics for application domain resource monitoring.</span></span>|  
  
## <a name="enabled-attribute"></a><span data-ttu-id="5b72c-113">enabled 特性</span><span class="sxs-lookup"><span data-stu-id="5b72c-113">enabled Attribute</span></span>  
  
|<span data-ttu-id="5b72c-114">值</span><span class="sxs-lookup"><span data-stu-id="5b72c-114">Value</span></span>|<span data-ttu-id="5b72c-115">说明</span><span class="sxs-lookup"><span data-stu-id="5b72c-115">Description</span></span>|  
|-----------|-----------------|  
|`true`|<span data-ttu-id="5b72c-116">收集应用程序域资源监视的统计信息。</span><span class="sxs-lookup"><span data-stu-id="5b72c-116">Statistics for application domain resource monitoring are collected.</span></span>|  
|`false`|<span data-ttu-id="5b72c-117">不收集应用程序域资源监视的统计信息。</span><span class="sxs-lookup"><span data-stu-id="5b72c-117">Statistics for application domain resource monitoring are not collected.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="5b72c-118">子元素</span><span class="sxs-lookup"><span data-stu-id="5b72c-118">Child Elements</span></span>  

 <span data-ttu-id="5b72c-119">无。</span><span class="sxs-lookup"><span data-stu-id="5b72c-119">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="5b72c-120">父元素</span><span class="sxs-lookup"><span data-stu-id="5b72c-120">Parent Elements</span></span>  
  
|<span data-ttu-id="5b72c-121">元素</span><span class="sxs-lookup"><span data-stu-id="5b72c-121">Element</span></span>|<span data-ttu-id="5b72c-122">说明</span><span class="sxs-lookup"><span data-stu-id="5b72c-122">Description</span></span>|  
|-------------|-----------------|  
|`configuration`|<span data-ttu-id="5b72c-123">公共语言运行时和 .NET Framework 应用程序所使用的每个配置文件中的根元素。</span><span class="sxs-lookup"><span data-stu-id="5b72c-123">The root element in every configuration file used by the common language runtime and .NET Framework applications.</span></span>|  
|`runtime`|<span data-ttu-id="5b72c-124">包含有关程序集绑定和垃圾回收的信息。</span><span class="sxs-lookup"><span data-stu-id="5b72c-124">Contains information about assembly binding and garbage collection.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="5b72c-125">备注</span><span class="sxs-lookup"><span data-stu-id="5b72c-125">Remarks</span></span>  

 <span data-ttu-id="5b72c-126">应用程序域资源监视可通过托管应用程序域类、托管 [ICLRAppDomainResourceMonitor](../../../unmanaged-api/hosting/iclrappdomainresourcemonitor-interface.md) 接口和 WINDOWS (ETW) 的事件跟踪获得。</span><span class="sxs-lookup"><span data-stu-id="5b72c-126">Application domain resource monitoring is available through the managed application domain class, the hosting [ICLRAppDomainResourceMonitor](../../../unmanaged-api/hosting/iclrappdomainresourcemonitor-interface.md) interface, and event tracing for Windows (ETW).</span></span> <span data-ttu-id="5b72c-127">启用监视后，会在进程的生存期内收集进程中所有应用程序域的统计信息。</span><span class="sxs-lookup"><span data-stu-id="5b72c-127">When monitoring is enabled, statistics are collected for all application domains in the process for the life of the process.</span></span>  
  
 <span data-ttu-id="5b72c-128">若要从托管代码启用监视，请使用 <xref:System.AppDomain.MonitoringIsEnabled%2A> 属性。</span><span class="sxs-lookup"><span data-stu-id="5b72c-128">To enable monitoring from managed code, use the <xref:System.AppDomain.MonitoringIsEnabled%2A> property.</span></span>  
  
 <span data-ttu-id="5b72c-129">此配置元素仅在 .NET Framework 4 及更高版本中可用。</span><span class="sxs-lookup"><span data-stu-id="5b72c-129">This configuration element is available only in the .NET Framework 4 and later.</span></span>  
  
## <a name="example"></a><span data-ttu-id="5b72c-130">示例</span><span class="sxs-lookup"><span data-stu-id="5b72c-130">Example</span></span>  

 <span data-ttu-id="5b72c-131">下面的示例演示如何启用应用程序域资源监视。</span><span class="sxs-lookup"><span data-stu-id="5b72c-131">The following example shows how to enable application domain resource monitoring.</span></span>  
  
```xml  
<configuration>  
   <runtime>  
      <appDomainResourceMonitoring enabled="true"/>  
   </runtime>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="5b72c-132">请参阅</span><span class="sxs-lookup"><span data-stu-id="5b72c-132">See also</span></span>

- <xref:System.AppDomain.MonitoringIsEnabled%2A?displayProperty=nameWithType>
- [<span data-ttu-id="5b72c-133">运行时设置架构</span><span class="sxs-lookup"><span data-stu-id="5b72c-133">Runtime Settings Schema</span></span>](index.md)
- [<span data-ttu-id="5b72c-134">配置文件架构</span><span class="sxs-lookup"><span data-stu-id="5b72c-134">Configuration File Schema</span></span>](../index.md)
