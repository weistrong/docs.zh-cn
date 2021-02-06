---
description: 详细了解： <listeners> 的元素 <trace>
title: <trace> 的 <listeners> 元素
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/system.diagnostics/trace/listeners
helpviewer_keywords:
- <listeners> element
- listeners element
ms.assetid: 1394c2c3-6304-46db-87c1-8e8b16f5ad5b
ms.openlocfilehash: 25f6d4b49eeb57b25b4afbbdfdba484d6d7eea3e
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99639622"
---
# <a name="listeners-element-for-trace"></a><span data-ttu-id="5fd4e-103">\<trace> 的 \<listeners> 元素</span><span class="sxs-lookup"><span data-stu-id="5fd4e-103">\<listeners> Element for \<trace></span></span>

<span data-ttu-id="5fd4e-104">指定用于收集、存储和路由消息的侦听器。</span><span class="sxs-lookup"><span data-stu-id="5fd4e-104">Specifies a listener that collects, stores, and routes messages.</span></span> <span data-ttu-id="5fd4e-105">侦听器将跟踪输出定向到适当的目标。</span><span class="sxs-lookup"><span data-stu-id="5fd4e-105">Listeners direct the tracing output to an appropriate target.</span></span>  

[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.diagnostics>**](system-diagnostics-element.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<trace>**](trace-element.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<listeners>**

## <a name="syntax"></a><span data-ttu-id="5fd4e-106">语法</span><span class="sxs-lookup"><span data-stu-id="5fd4e-106">Syntax</span></span>  
  
```xml  
<listeners>
  <add>...</add>  
  <clear/>  
  <remove ... />  
</listeners>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="5fd4e-107">特性和元素</span><span class="sxs-lookup"><span data-stu-id="5fd4e-107">Attributes and Elements</span></span>  

 <span data-ttu-id="5fd4e-108">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="5fd4e-108">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="5fd4e-109">特性</span><span class="sxs-lookup"><span data-stu-id="5fd4e-109">Attributes</span></span>  

 <span data-ttu-id="5fd4e-110">无。</span><span class="sxs-lookup"><span data-stu-id="5fd4e-110">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="5fd4e-111">子元素</span><span class="sxs-lookup"><span data-stu-id="5fd4e-111">Child Elements</span></span>  
  
|<span data-ttu-id="5fd4e-112">元素</span><span class="sxs-lookup"><span data-stu-id="5fd4e-112">Element</span></span>|<span data-ttu-id="5fd4e-113">说明</span><span class="sxs-lookup"><span data-stu-id="5fd4e-113">Description</span></span>|  
|-------------|-----------------|  
|[\<add>](add-element-for-listeners-for-trace.md)|<span data-ttu-id="5fd4e-114">将侦听器添加到 `Listeners` 集合中。</span><span class="sxs-lookup"><span data-stu-id="5fd4e-114">Adds a listener to the `Listeners` collection.</span></span>|  
|[\<clear>](clear-element-for-listeners-for-trace.md)|<span data-ttu-id="5fd4e-115">清除跟踪的 `Listeners` 集合。</span><span class="sxs-lookup"><span data-stu-id="5fd4e-115">Clears the `Listeners` collection for trace.</span></span>|  
|[\<remove>](remove-element-for-listeners-for-trace.md)|<span data-ttu-id="5fd4e-116">从集合中移除侦听器 `Listeners` 。</span><span class="sxs-lookup"><span data-stu-id="5fd4e-116">Removes a listener from the `Listeners` collection.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="5fd4e-117">父元素</span><span class="sxs-lookup"><span data-stu-id="5fd4e-117">Parent Elements</span></span>  
  
|<span data-ttu-id="5fd4e-118">元素</span><span class="sxs-lookup"><span data-stu-id="5fd4e-118">Element</span></span>|<span data-ttu-id="5fd4e-119">说明</span><span class="sxs-lookup"><span data-stu-id="5fd4e-119">Description</span></span>|  
|-------------|-----------------|  
|`configuration`|<span data-ttu-id="5fd4e-120">公共语言运行时和 .NET Framework 应用程序所使用的每个配置文件中的根元素。</span><span class="sxs-lookup"><span data-stu-id="5fd4e-120">The root element in every configuration file used by the common language runtime and .NET Framework applications.</span></span>|  
|`system.diagnostics`|<span data-ttu-id="5fd4e-121">为 ASP.NET 配置节指定根元素。</span><span class="sxs-lookup"><span data-stu-id="5fd4e-121">Specifies the root element for the ASP.NET configuration section.</span></span>|  
|`trace`|<span data-ttu-id="5fd4e-122">包含用于收集、存储和路由跟踪消息的侦听器。</span><span class="sxs-lookup"><span data-stu-id="5fd4e-122">Contains listeners that collect, store, and route tracing messages.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="5fd4e-123">备注</span><span class="sxs-lookup"><span data-stu-id="5fd4e-123">Remarks</span></span>  

 <span data-ttu-id="5fd4e-124"><xref:System.Diagnostics.Debug>和 <xref:System.Diagnostics.Trace> 类共享相同的 **侦听器** 集合。</span><span class="sxs-lookup"><span data-stu-id="5fd4e-124">The <xref:System.Diagnostics.Debug> and <xref:System.Diagnostics.Trace> classes share the same **Listeners** collection.</span></span> <span data-ttu-id="5fd4e-125">如果将侦听器对象添加到其中一个类的集合中，则其他类将使用同一侦听器。</span><span class="sxs-lookup"><span data-stu-id="5fd4e-125">If you add a listener object to the collection in one of these classes, the other class uses the same listener.</span></span> <span data-ttu-id="5fd4e-126">随 .NET Framework 附带的侦听器类派生自 <xref:System.Diagnostics.TraceListener> 类。</span><span class="sxs-lookup"><span data-stu-id="5fd4e-126">The listener classes shipped with the .NET Framework derive from the <xref:System.Diagnostics.TraceListener> class.</span></span>  
  
## <a name="configuration-file"></a><span data-ttu-id="5fd4e-127">配置文件</span><span class="sxs-lookup"><span data-stu-id="5fd4e-127">Configuration File</span></span>  

 <span data-ttu-id="5fd4e-128">此元素可在计算机配置文件中使用 ( # A0) 和应用程序配置文件。</span><span class="sxs-lookup"><span data-stu-id="5fd4e-128">This element can be used in the machine configuration file (Machine.config) and the application configuration file.</span></span>  
  
## <a name="example"></a><span data-ttu-id="5fd4e-129">示例</span><span class="sxs-lookup"><span data-stu-id="5fd4e-129">Example</span></span>  

 <span data-ttu-id="5fd4e-130">下面的示例演示如何使用 **\<listeners>** 元素将侦听器 `MyListener` 和添加 `MyEventListener` 到 **侦听器** 集合。</span><span class="sxs-lookup"><span data-stu-id="5fd4e-130">The following example shows how to use the **\<listeners>** element to add the listeners `MyListener` and `MyEventListener` to the **Listeners** collection.</span></span> <span data-ttu-id="5fd4e-131">`MyListener` 创建一个名为的文件 `MyListener.log` ，并将输出写入文件。</span><span class="sxs-lookup"><span data-stu-id="5fd4e-131">`MyListener` creates a file called `MyListener.log` and writes the output to the file.</span></span> <span data-ttu-id="5fd4e-132">`MyEventListener` 在事件日志中创建一个条目。</span><span class="sxs-lookup"><span data-stu-id="5fd4e-132">`MyEventListener` creates an entry in the event log.</span></span>  
  
```xml  
<configuration>  
  <system.diagnostics>  
    <trace autoflush="true" indentsize="0">  
      <listeners>  
        <add name="myListener"
          type="System.Diagnostics.TextWriterTraceListener,
            system, version=1.0.3300.0, Culture=neutral,
            PublicKeyToken=b77a5c561934e089"
          initializeData="c:\myListener.log" />  
        <add name="MyEventListener"  
          type="System.Diagnostics.EventLogTraceListener,
            system, version=1.0.3300.0, Culture=neutral,
            PublicKeyToken=b77a5c561934e089"  
          initializeData="MyConfigEventLog"/>  
      </listeners>  
    </trace>  
  </system.diagnostics>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="5fd4e-133">请参阅</span><span class="sxs-lookup"><span data-stu-id="5fd4e-133">See also</span></span>

- <xref:System.Diagnostics.TraceListener>
- [<span data-ttu-id="5fd4e-134">跟踪和调试设置架构</span><span class="sxs-lookup"><span data-stu-id="5fd4e-134">Trace and Debug Settings Schema</span></span>](index.md)
