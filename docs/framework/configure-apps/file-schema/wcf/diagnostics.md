---
description: 了解详细信息： <diagnostics>
title: <diagnostics>
ms.date: 03/30/2017
ms.assetid: 0c2f95c4-cc12-4fb5-a70c-7fc6fa95db58
ms.openlocfilehash: d1651d949cdc095e630e9cde0bacbe51a5eb6062
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99782151"
---
# \<diagnostics>

<span data-ttu-id="669de-102">`diagnostics` 元素定义管理员可以用来进行运行时检查和控制的设置。</span><span class="sxs-lookup"><span data-stu-id="669de-102">The `diagnostics` element defines settings that can be used by an administrator for run-time inspection and control.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;**\<diagnostics>**  
  
## <a name="syntax"></a><span data-ttu-id="669de-103">语法</span><span class="sxs-lookup"><span data-stu-id="669de-103">Syntax</span></span>  
  
```xml  
<system.serviceModel>
  <diagnostics etwProviderId="String"
               performanceCounters="Off/ServiceOnly/All/Default"
               wmiProviderEnabled="Boolean">
    <endToEndTracing activityTracing="Boolean"
                     messageFlowTracing="Boolean"
                     propagateActivity="Boolean" />
    <messageLogging logEntireMessage="Boolean"
                    logMalformedMessages="Boolean"
                    logMessagesAtServiceLevel="Boolean"
                    logMessagesAtTransportLevel="Boolean"
                    maxMessagesToLog="Integer"
                    maxSizeOfMessageToLog="Integer">
      <filters>
        <clear />
      </filters>
    </messageLogging>
  </diagnostics>
</system.serviceModel>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="669de-104">特性和元素</span><span class="sxs-lookup"><span data-stu-id="669de-104">Attributes and Elements</span></span>  

 <span data-ttu-id="669de-105">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="669de-105">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="669de-106">特性</span><span class="sxs-lookup"><span data-stu-id="669de-106">Attributes</span></span>  
  
|<span data-ttu-id="669de-107">属性</span><span class="sxs-lookup"><span data-stu-id="669de-107">Attribute</span></span>|<span data-ttu-id="669de-108">说明</span><span class="sxs-lookup"><span data-stu-id="669de-108">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="669de-109">etwProviderId</span><span class="sxs-lookup"><span data-stu-id="669de-109">etwProviderId</span></span>|<span data-ttu-id="669de-110">一个字符串，指定将事件写入到 ETW 会话的事件跟踪提供程序的标识符。</span><span class="sxs-lookup"><span data-stu-id="669de-110">A string that specifies the identifier for the Event-Tracing provider, which writes events to ETW sessions.</span></span>|  
|<span data-ttu-id="669de-111">performanceCounters</span><span class="sxs-lookup"><span data-stu-id="669de-111">performanceCounters</span></span>|<span data-ttu-id="669de-112">指定是否启用程序集的性能计数器。</span><span class="sxs-lookup"><span data-stu-id="669de-112">Specifies whether performance counters for the assembly are enabled.</span></span> <span data-ttu-id="669de-113">有效值为</span><span class="sxs-lookup"><span data-stu-id="669de-113">Valid values are</span></span><br /><br /> <span data-ttu-id="669de-114">-Off：性能计数器已禁用。</span><span class="sxs-lookup"><span data-stu-id="669de-114">-   Off: Performance counters are disabled.</span></span><br /><span data-ttu-id="669de-115">-ServiceOnly：只启用与此服务相关的性能计数器。</span><span class="sxs-lookup"><span data-stu-id="669de-115">-   ServiceOnly: Only performance counters relevant to this service is enabled.</span></span><br /><span data-ttu-id="669de-116">-All：可在运行时查看性能计数器。</span><span class="sxs-lookup"><span data-stu-id="669de-116">-   All: Performance counters can be viewed at runtime.</span></span><br /><span data-ttu-id="669de-117">-默认：创建 _WCF_Admin 单个性能计数器实例。</span><span class="sxs-lookup"><span data-stu-id="669de-117">-   Default: A single performance counter instance _WCF_Admin is created.</span></span> <span data-ttu-id="669de-118">此实例用于启用基础结构所使用的 SQM 数据的集合。</span><span class="sxs-lookup"><span data-stu-id="669de-118">This instance is used to enable the collection of SQM data for used by the infrastructure.</span></span> <span data-ttu-id="669de-119">此实例的计数器值均未进行更新，因此将保持为零。</span><span class="sxs-lookup"><span data-stu-id="669de-119">None of the counter values for this instance are updated and therefore will remain at zero.</span></span> <span data-ttu-id="669de-120">这是在 WCF 没有配置的情况下的默认值。</span><span class="sxs-lookup"><span data-stu-id="669de-120">This is the default value if no configuration is present for WCF.</span></span>|  
|<span data-ttu-id="669de-121">wmiProviderEnabled</span><span class="sxs-lookup"><span data-stu-id="669de-121">wmiProviderEnabled</span></span>|<span data-ttu-id="669de-122">一个布尔值，指定是否启用程序集的 WMI 提供程序。</span><span class="sxs-lookup"><span data-stu-id="669de-122">A Boolean value that specifies whether the WMI provider for the assembly is enabled.</span></span> <span data-ttu-id="669de-123">用户要获得在运行时访问 Windows Communication Foundation (WCF) 的检查和控制功能的权限，需要使用 WMI 提供程序。</span><span class="sxs-lookup"><span data-stu-id="669de-123">The WMI provider is required for user to gain run-time access to the inspection and control features of Windows Communication Foundation (WCF).</span></span> <span data-ttu-id="669de-124">默认值为 `false`。</span><span class="sxs-lookup"><span data-stu-id="669de-124">The default is `false`.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="669de-125">子元素</span><span class="sxs-lookup"><span data-stu-id="669de-125">Child Elements</span></span>  
  
|<span data-ttu-id="669de-126">元素</span><span class="sxs-lookup"><span data-stu-id="669de-126">Element</span></span>|<span data-ttu-id="669de-127">说明</span><span class="sxs-lookup"><span data-stu-id="669de-127">Description</span></span>|  
|-------------|-----------------|  
|[\<endToEndTracing>](endtoendtracing.md)|<span data-ttu-id="669de-128">一个配置元素，用于启用和禁用服务应用程序运行过程中端对端跟踪的不同方面。</span><span class="sxs-lookup"><span data-stu-id="669de-128">A configuration element that allows you to enable and disable different aspects of end-to-end tracing during the running of a service application.</span></span>|  
|[\<messageLogging>](messagelogging.md)|<span data-ttu-id="669de-129">描述 WCF 消息日志记录的设置。</span><span class="sxs-lookup"><span data-stu-id="669de-129">Describes the settings for WCF message logging.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="669de-130">父元素</span><span class="sxs-lookup"><span data-stu-id="669de-130">Parent Elements</span></span>  
  
|<span data-ttu-id="669de-131">元素</span><span class="sxs-lookup"><span data-stu-id="669de-131">Element</span></span>|<span data-ttu-id="669de-132">说明</span><span class="sxs-lookup"><span data-stu-id="669de-132">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="669de-133">serviceModel</span><span class="sxs-lookup"><span data-stu-id="669de-133">serviceModel</span></span>|<span data-ttu-id="669de-134">所有 WCF 配置元素的根元素。</span><span class="sxs-lookup"><span data-stu-id="669de-134">The root element of all WCF configuration elements.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="669de-135">备注</span><span class="sxs-lookup"><span data-stu-id="669de-135">Remarks</span></span>  

 <span data-ttu-id="669de-136">`diagnostics` 节定义了位于程序集中的所有服务的诊断设置。</span><span class="sxs-lookup"><span data-stu-id="669de-136">The `diagnostics` section defines the diagnostics settings for all services located in an assembly.</span></span> <span data-ttu-id="669de-137">无法在服务级别定义单独的诊断设置，除非程序集中只有一个服务。</span><span class="sxs-lookup"><span data-stu-id="669de-137">It is not possible to define separate diagnostics settings at the service level unless there is only one service in the assembly.</span></span> <span data-ttu-id="669de-138">将根据本节的需求来设置属性。</span><span class="sxs-lookup"><span data-stu-id="669de-138">Attributes are set according to the requirements of the section.</span></span>  
  
## <a name="example"></a><span data-ttu-id="669de-139">示例</span><span class="sxs-lookup"><span data-stu-id="669de-139">Example</span></span>  
  
```xml  
<diagnostics wmiProviderEnabled="false"
             performanceCounters="all">
  <messageLogging logEntireMessage="true"
                  logMalformedMessages="true"
                  logMessagesAtServiceLevel="true"
                  logMessagesAtTransportLevel="true"
                  maxMessagesToLog="42"
                  maxSizeOfMessageToLog="42">
    <filters>
      <clear />
    </filters>
  </messageLogging>
</diagnostics>
```  
  
## <a name="see-also"></a><span data-ttu-id="669de-140">请参阅</span><span class="sxs-lookup"><span data-stu-id="669de-140">See also</span></span>

- <xref:System.ServiceModel.Configuration.DiagnosticSection>
- <xref:System.ServiceModel.Diagnostics>
