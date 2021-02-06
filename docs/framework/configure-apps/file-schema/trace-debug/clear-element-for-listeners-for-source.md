---
description: 详细了解： <clear> <listeners> 的元素 <source>
title: <clear>的元素 <listeners><source>
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/system.diagnostics/sources/source/listeners/clear
helpviewer_keywords:
- <clear> element for <listeners> for <source>
- clear element for <listeners> for <source>
ms.assetid: 76796bb2-9c0b-4526-8135-8bf18b16d8d9
ms.openlocfilehash: 731c23c73b6d149bd37672e91eca1d70431b2789
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99639700"
---
# <a name="clear-element-for-listeners-for-source"></a><span data-ttu-id="6544a-103">\<clear>的元素 \<listeners>\<source></span><span class="sxs-lookup"><span data-stu-id="6544a-103">\<clear> Element for \<listeners> for \<source></span></span>

<span data-ttu-id="6544a-104">清除跟踪源的 `Listeners` 集合。</span><span class="sxs-lookup"><span data-stu-id="6544a-104">Clears the `Listeners` collection for a trace source.</span></span>  

[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.diagnostics>**](system-diagnostics-element.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<sources>**](sources-element.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<source>**](source-element.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<listeners>**](listeners-element-for-source.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<clear>**

## <a name="syntax"></a><span data-ttu-id="6544a-105">语法</span><span class="sxs-lookup"><span data-stu-id="6544a-105">Syntax</span></span>  
  
```xml  
<clear/>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="6544a-106">特性和元素</span><span class="sxs-lookup"><span data-stu-id="6544a-106">Attributes and Elements</span></span>  

 <span data-ttu-id="6544a-107">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="6544a-107">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="6544a-108">特性</span><span class="sxs-lookup"><span data-stu-id="6544a-108">Attributes</span></span>  

 <span data-ttu-id="6544a-109">无。</span><span class="sxs-lookup"><span data-stu-id="6544a-109">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="6544a-110">子元素</span><span class="sxs-lookup"><span data-stu-id="6544a-110">Child Elements</span></span>  

 <span data-ttu-id="6544a-111">无。</span><span class="sxs-lookup"><span data-stu-id="6544a-111">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="6544a-112">父元素</span><span class="sxs-lookup"><span data-stu-id="6544a-112">Parent Elements</span></span>  
  
|<span data-ttu-id="6544a-113">元素</span><span class="sxs-lookup"><span data-stu-id="6544a-113">Element</span></span>|<span data-ttu-id="6544a-114">说明</span><span class="sxs-lookup"><span data-stu-id="6544a-114">Description</span></span>|  
|-------------|-----------------|  
|`configuration`|<span data-ttu-id="6544a-115">公共语言运行时和 .NET Framework 应用程序所使用的每个配置文件中的根元素。</span><span class="sxs-lookup"><span data-stu-id="6544a-115">The root element in every configuration file used by the common language runtime and .NET Framework applications.</span></span>|  
|`system.diagnostics`|<span data-ttu-id="6544a-116">指定用于收集、存储和路由消息的跟踪侦听器以及对跟踪开关设置的级别。</span><span class="sxs-lookup"><span data-stu-id="6544a-116">Specifies trace listeners that collect, store, and route messages and the level where a trace switch is set.</span></span>|  
|`sources`|<span data-ttu-id="6544a-117">包含用于启动跟踪消息的跟踪源。</span><span class="sxs-lookup"><span data-stu-id="6544a-117">Contains trace sources that initiate tracing messages.</span></span>|  
|`source`|<span data-ttu-id="6544a-118">指定用于启动跟踪消息的跟踪源。</span><span class="sxs-lookup"><span data-stu-id="6544a-118">Specifies a trace source that initiates tracing messages.</span></span>|  
|`listeners`|<span data-ttu-id="6544a-119">指定用于收集、存储和路由消息的侦听器。</span><span class="sxs-lookup"><span data-stu-id="6544a-119">Specifies listeners that collect, store, and route messages.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="6544a-120">备注</span><span class="sxs-lookup"><span data-stu-id="6544a-120">Remarks</span></span>  

 <span data-ttu-id="6544a-121">`<clear>`元素从跟踪源的集合中移除所有侦听器 `Listeners` ，包括 <xref:System.Diagnostics.DefaultTraceListener> 。</span><span class="sxs-lookup"><span data-stu-id="6544a-121">The `<clear>` element removes all listeners from the `Listeners` collection for a trace source, including the <xref:System.Diagnostics.DefaultTraceListener>.</span></span> <span data-ttu-id="6544a-122">可以在使用元素 `<clear>` 之前使用元素 `<add>` ，以确定集合中没有其他活动的侦听器。</span><span class="sxs-lookup"><span data-stu-id="6544a-122">You can use the `<clear>` element before using the `<add>` element to be certain there are no other active listeners in the collection.</span></span>  
  
## <a name="configuration-file"></a><span data-ttu-id="6544a-123">配置文件</span><span class="sxs-lookup"><span data-stu-id="6544a-123">Configuration File</span></span>  

 <span data-ttu-id="6544a-124">此元素可在计算机配置文件中使用 ( # A0) 和应用程序配置文件。</span><span class="sxs-lookup"><span data-stu-id="6544a-124">This element can be used in the machine configuration file (Machine.config) and the application configuration file.</span></span>  
  
## <a name="example"></a><span data-ttu-id="6544a-125">示例</span><span class="sxs-lookup"><span data-stu-id="6544a-125">Example</span></span>  

 <span data-ttu-id="6544a-126">下面的示例演示如何 `<clear>` 在使用 `<add>` 元素将侦听器 `console` 和 `textListener` 集合添加到 `Listeners` 跟踪源之前使用元素 `TraceSourceApp` 。</span><span class="sxs-lookup"><span data-stu-id="6544a-126">The following example shows how to use the `<clear>` element before using the `<add>` elements to add the listeners `console` and `textListener` to the `Listeners` collection for the trace source `TraceSourceApp`.</span></span>  
  
```xml  
<configuration>  
  <system.diagnostics>  
    <sources>  
       <source name="TraceSourceApp" switchName="sourceSwitch"
         switchType="System.Diagnostics.SourceSwitch">  
        <listeners>  
          <clear/>  
          <add name="console"
            type="System.Diagnostics.ConsoleTraceListener"/>  
          <add name="textListener"/>  
        </listeners>  
      </source>  
    </sources>  
    <sharedListeners>  
      <add name="textListener"
        type="System.Diagnostics.TextWriterTraceListener"
        initializeData="myListener.log"/>  
    </sharedListeners>  
    <switches>  
      <add name="sourceSwitch" value="Warning"/>  
    </switches>  
  </system.diagnostics>  
</configuration>
```  
  
## <a name="see-also"></a><span data-ttu-id="6544a-127">请参阅</span><span class="sxs-lookup"><span data-stu-id="6544a-127">See also</span></span>

- <xref:System.Diagnostics.TraceSource>
- <xref:System.Diagnostics.TraceListener>
- [<span data-ttu-id="6544a-128">跟踪和调试设置架构</span><span class="sxs-lookup"><span data-stu-id="6544a-128">Trace and Debug Settings Schema</span></span>](index.md)
- [<span data-ttu-id="6544a-129">跟踪侦听器</span><span class="sxs-lookup"><span data-stu-id="6544a-129">Trace Listeners</span></span>](../../../debug-trace-profile/trace-listeners.md)
