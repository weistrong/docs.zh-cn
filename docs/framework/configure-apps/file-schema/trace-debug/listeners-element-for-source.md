---
description: 详细了解： <listeners> 的元素 <source>
title: <source> 的 <listeners> 元素
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/system.diagnostics/sources/source/listeners
helpviewer_keywords:
- listeners element for <source>
- <listeners> element for <source>
ms.assetid: a2991f43-b4d3-4614-a8e7-da392de9697f
ms.openlocfilehash: 6b857d4b114366d268eec1859afc7f33cc5b04a2
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99639635"
---
# <a name="listeners-element-for-source"></a><span data-ttu-id="b095e-103">\<source> 的 \<listeners> 元素</span><span class="sxs-lookup"><span data-stu-id="b095e-103">\<listeners> Element for \<source></span></span>

<span data-ttu-id="b095e-104">在的集合中添加或移除侦听器 <xref:System.Diagnostics.TraceSource.Listeners%2A> <xref:System.Diagnostics.TraceSource> 。</span><span class="sxs-lookup"><span data-stu-id="b095e-104">Adds or removes listeners in the <xref:System.Diagnostics.TraceSource.Listeners%2A> collection for a <xref:System.Diagnostics.TraceSource>.</span></span> <span data-ttu-id="b095e-105">侦听器将跟踪输出定向到适当的目标，如日志、窗口或文本文件。</span><span class="sxs-lookup"><span data-stu-id="b095e-105">A listener directs the tracing output to an appropriate target, such as a log, window, or text file.</span></span>  
  
[**\<configuration>**](../configuration-element.md)  
&nbsp;&nbsp;[**\<system.diagnostics>**](system-diagnostics-element.md)  
&nbsp;&nbsp;&nbsp;&nbsp;[**\<sources>**](sources-element.md)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<source>**](source-element.md)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<listeners>**  
  
## <a name="syntax"></a><span data-ttu-id="b095e-106">语法</span><span class="sxs-lookup"><span data-stu-id="b095e-106">Syntax</span></span>  
  
```xml  
<listeners>
  <add>...</add>  
  <remove ... />  
  <clear/>  
</listeners>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="b095e-107">特性和元素</span><span class="sxs-lookup"><span data-stu-id="b095e-107">Attributes and Elements</span></span>  

 <span data-ttu-id="b095e-108">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="b095e-108">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="b095e-109">特性</span><span class="sxs-lookup"><span data-stu-id="b095e-109">Attributes</span></span>  

 <span data-ttu-id="b095e-110">无。</span><span class="sxs-lookup"><span data-stu-id="b095e-110">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="b095e-111">子元素</span><span class="sxs-lookup"><span data-stu-id="b095e-111">Child Elements</span></span>  
  
|<span data-ttu-id="b095e-112">元素</span><span class="sxs-lookup"><span data-stu-id="b095e-112">Element</span></span>|<span data-ttu-id="b095e-113">说明</span><span class="sxs-lookup"><span data-stu-id="b095e-113">Description</span></span>|  
|-------------|-----------------|  
|[\<add>](add-element-for-listeners-for-source.md)|<span data-ttu-id="b095e-114">将侦听器添加到 `Listeners` 集合中。</span><span class="sxs-lookup"><span data-stu-id="b095e-114">Adds a listener to the `Listeners` collection.</span></span>|  
|[\<remove>](remove-element-for-listeners-for-source.md)|<span data-ttu-id="b095e-115">从集合中移除侦听器 `Listeners` 。</span><span class="sxs-lookup"><span data-stu-id="b095e-115">Removes a listener from the `Listeners` collection.</span></span>|  
|[\<clear>](clear-element-for-listeners-for-source.md)|<span data-ttu-id="b095e-116">清除跟踪源的 `Listeners` 集合。</span><span class="sxs-lookup"><span data-stu-id="b095e-116">Clears the `Listeners` collection for a trace source.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="b095e-117">父元素</span><span class="sxs-lookup"><span data-stu-id="b095e-117">Parent Elements</span></span>  
  
|<span data-ttu-id="b095e-118">元素</span><span class="sxs-lookup"><span data-stu-id="b095e-118">Element</span></span>|<span data-ttu-id="b095e-119">说明</span><span class="sxs-lookup"><span data-stu-id="b095e-119">Description</span></span>|  
|-------------|-----------------|  
|`configuration`|<span data-ttu-id="b095e-120">公共语言运行时和 .NET Framework 应用程序所使用的每个配置文件中的根元素。</span><span class="sxs-lookup"><span data-stu-id="b095e-120">The root element in every configuration file used by the common language runtime and .NET Framework applications.</span></span>|  
|`system.diagnostics`|<span data-ttu-id="b095e-121">指定用于收集、存储和路由消息的跟踪侦听器以及对跟踪开关设置的级别。</span><span class="sxs-lookup"><span data-stu-id="b095e-121">Specifies trace listeners that collect, store, and route messages and the level where a trace switch is set.</span></span>|  
|`sources`|<span data-ttu-id="b095e-122">包含用于启动跟踪消息的跟踪源。</span><span class="sxs-lookup"><span data-stu-id="b095e-122">Contains trace sources that initiate tracing messages.</span></span>|  
|`source`|<span data-ttu-id="b095e-123">指定用于启动跟踪消息的跟踪源。</span><span class="sxs-lookup"><span data-stu-id="b095e-123">Specifies a trace source that initiates tracing messages.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="b095e-124">备注</span><span class="sxs-lookup"><span data-stu-id="b095e-124">Remarks</span></span>  
  
## <a name="configuration-file"></a><span data-ttu-id="b095e-125">配置文件</span><span class="sxs-lookup"><span data-stu-id="b095e-125">Configuration File</span></span>  

 <span data-ttu-id="b095e-126">此元素可在计算机配置文件中使用 ( # A0) 和应用程序配置文件。</span><span class="sxs-lookup"><span data-stu-id="b095e-126">This element can be used in the machine configuration file (Machine.config) and the application configuration file.</span></span>  
  
## <a name="example"></a><span data-ttu-id="b095e-127">示例</span><span class="sxs-lookup"><span data-stu-id="b095e-127">Example</span></span>  

 <span data-ttu-id="b095e-128">下面的示例演示如何使用 `<listeners>` 元素将控制台跟踪侦听器添加到 `mySource` 源，并删除默认的跟踪侦听器。</span><span class="sxs-lookup"><span data-stu-id="b095e-128">The following example shows how to use the `<listeners>` element to add a console trace listener to the `mySource` source and to remove the default trace listener.</span></span>  
  
```xml  
<configuration>  
  <system.diagnostics>  
    <sources>  
      <source name="mySource" switchName="sourceSwitch"
        switchType="System.Diagnostics.SourceSwitch">  
        <listeners>  
          <add name="console"
            type="System.Diagnostics.ConsoleTraceListener">  
            <filter type="System.Diagnostics.EventTypeFilter"
              initializeData="Error"/>  
          </add>  
          <remove name="Default"/>  
        </listeners>  
      </source>  
    </sources>  
    <switches>  
      <add name="sourceSwitch" value="Warning"/>  
    </switches>  
  </system.diagnostics>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="b095e-129">请参阅</span><span class="sxs-lookup"><span data-stu-id="b095e-129">See also</span></span>

- <xref:System.Diagnostics.TraceListener>
- [<span data-ttu-id="b095e-130">跟踪和调试设置架构</span><span class="sxs-lookup"><span data-stu-id="b095e-130">Trace and Debug Settings Schema</span></span>](index.md)
- [<span data-ttu-id="b095e-131">跟踪侦听器</span><span class="sxs-lookup"><span data-stu-id="b095e-131">Trace Listeners</span></span>](../../../debug-trace-profile/trace-listeners.md)
