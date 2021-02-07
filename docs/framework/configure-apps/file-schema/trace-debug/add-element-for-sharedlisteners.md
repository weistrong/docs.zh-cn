---
description: 详细了解： <add> 的元素 <sharedListeners>
title: <sharedListeners> 的 <add> 元素
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/system.diagnostics/sharedListeners/add
helpviewer_keywords:
- initializeData attribute
- <add> element for <sharedListeners>
- add element for <sharedListeners>
ms.assetid: 1595e1bc-2492-421f-8384-7f382eb8eb57
ms.openlocfilehash: df3348fa0cbb357b2ceeb5d9db940a1ae3ae102c
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99726073"
---
# <a name="add-element-for-sharedlisteners"></a><span data-ttu-id="387e9-103">\<sharedListeners> 的 \<add> 元素</span><span class="sxs-lookup"><span data-stu-id="387e9-103">\<add> Element for \<sharedListeners></span></span>

<span data-ttu-id="387e9-104">将侦听器添加到 `sharedListeners` 集合中。</span><span class="sxs-lookup"><span data-stu-id="387e9-104">Adds a listener to the `sharedListeners` collection.</span></span> <span data-ttu-id="387e9-105">`sharedListeners` 是任何 [\<source>](source-element.md) 或可引用的侦听器的集合 [\<trace>](trace-element.md) 。</span><span class="sxs-lookup"><span data-stu-id="387e9-105">`sharedListeners` is a collection of listeners that any [\<source>](source-element.md) or [\<trace>](trace-element.md) can reference.</span></span>  <span data-ttu-id="387e9-106">默认情况下，集合中的侦听器 `sharedListeners` 不会放置在 `Listeners` 集合中。</span><span class="sxs-lookup"><span data-stu-id="387e9-106">By default, listeners in the `sharedListeners` collection are not placed in a `Listeners` collection.</span></span> <span data-ttu-id="387e9-107">必须按名称将它们添加到 [\<source>](source-element.md) 或 [\<trace>](trace-element.md) 。</span><span class="sxs-lookup"><span data-stu-id="387e9-107">They must be added by name to the [\<source>](source-element.md) or [\<trace>](trace-element.md).</span></span> <span data-ttu-id="387e9-108">在运行时，不能 `sharedListeners` 在代码中获取集合中的侦听器。</span><span class="sxs-lookup"><span data-stu-id="387e9-108">It is not possible to get the listeners in the `sharedListeners` collection in code at run time.</span></span>  

[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.diagnostics>**](system-diagnostics-element.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<sharedListeners>**](sharedlisteners-element.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<add>**

## <a name="syntax"></a><span data-ttu-id="387e9-109">语法</span><span class="sxs-lookup"><span data-stu-id="387e9-109">Syntax</span></span>  
  
```xml  
<add name="name"
  type="TraceListenerClassName, Version, Culture, PublicKeyToken"  
  initializeData="data"
  traceOutputOptions = "None"
/>  
```
  
## <a name="attributes-and-elements"></a><span data-ttu-id="387e9-110">特性和元素</span><span class="sxs-lookup"><span data-stu-id="387e9-110">Attributes and Elements</span></span>  

 <span data-ttu-id="387e9-111">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="387e9-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="387e9-112">特性</span><span class="sxs-lookup"><span data-stu-id="387e9-112">Attributes</span></span>  
  
|<span data-ttu-id="387e9-113">属性</span><span class="sxs-lookup"><span data-stu-id="387e9-113">Attribute</span></span>|<span data-ttu-id="387e9-114">描述</span><span class="sxs-lookup"><span data-stu-id="387e9-114">Description</span></span>|  
|---------------|-----------------|  
|`name`|<span data-ttu-id="387e9-115">必需的特性。</span><span class="sxs-lookup"><span data-stu-id="387e9-115">Required attribute.</span></span><br /><br /> <span data-ttu-id="387e9-116">指定用于将共享侦听器添加到集合中的侦听器的名称 `Listeners` 。</span><span class="sxs-lookup"><span data-stu-id="387e9-116">Specifies the name of the listener that is used to add the shared listener to a `Listeners` collection.</span></span>|  
|`type`|<span data-ttu-id="387e9-117">必需的特性。</span><span class="sxs-lookup"><span data-stu-id="387e9-117">Required attribute.</span></span><br /><br /> <span data-ttu-id="387e9-118">指定侦听器的类型。</span><span class="sxs-lookup"><span data-stu-id="387e9-118">Specifies the type of the listener.</span></span> <span data-ttu-id="387e9-119">必须使用满足指定 [完全限定的类型名称](../../../reflection-and-codedom/specifying-fully-qualified-type-names.md)中指定的要求的字符串。</span><span class="sxs-lookup"><span data-stu-id="387e9-119">You must use a string that meets the requirements specified in [Specifying Fully Qualified Type Names](../../../reflection-and-codedom/specifying-fully-qualified-type-names.md).</span></span>|  
|`initializeData`|<span data-ttu-id="387e9-120">可选特性。</span><span class="sxs-lookup"><span data-stu-id="387e9-120">Optional attribute.</span></span><br /><br /> <span data-ttu-id="387e9-121">传递到指定类的构造函数的字符串。</span><span class="sxs-lookup"><span data-stu-id="387e9-121">The string passed to the constructor for the specified class.</span></span>|  
|`traceOutputOptions`|<span data-ttu-id="387e9-122">可选特性。</span><span class="sxs-lookup"><span data-stu-id="387e9-122">Optional attribute.</span></span><br/><br/><span data-ttu-id="387e9-123">指示要写入跟踪输出的数据的一个或多个枚举成员的字符串表示形式 <xref:System.Diagnostics.TraceOptions> 。</span><span class="sxs-lookup"><span data-stu-id="387e9-123">The string representation of one or more <xref:System.Diagnostics.TraceOptions> enumeration members that indicates the data to be written to the trace output.</span></span> <span data-ttu-id="387e9-124">多个项之间以逗号分隔。</span><span class="sxs-lookup"><span data-stu-id="387e9-124">Multiple items are separated by commas.</span></span> <span data-ttu-id="387e9-125">默认值为 "None"。</span><span class="sxs-lookup"><span data-stu-id="387e9-125">The default value is "None".</span></span>|

### <a name="child-elements"></a><span data-ttu-id="387e9-126">子元素</span><span class="sxs-lookup"><span data-stu-id="387e9-126">Child Elements</span></span>  
  
|<span data-ttu-id="387e9-127">元素</span><span class="sxs-lookup"><span data-stu-id="387e9-127">Element</span></span>|<span data-ttu-id="387e9-128">说明</span><span class="sxs-lookup"><span data-stu-id="387e9-128">Description</span></span>|  
|-------------|-----------------|  
|[\<filter>](filter-element-for-add-for-sharedlisteners.md)|<span data-ttu-id="387e9-129">将筛选器添加到 `sharedListeners` 集合中的侦听器。</span><span class="sxs-lookup"><span data-stu-id="387e9-129">Adds a filter to a listener in the `sharedListeners` collection.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="387e9-130">父元素</span><span class="sxs-lookup"><span data-stu-id="387e9-130">Parent Elements</span></span>  
  
|<span data-ttu-id="387e9-131">元素</span><span class="sxs-lookup"><span data-stu-id="387e9-131">Element</span></span>|<span data-ttu-id="387e9-132">说明</span><span class="sxs-lookup"><span data-stu-id="387e9-132">Description</span></span>|  
|-------------|-----------------|  
|`configuration`|<span data-ttu-id="387e9-133">公共语言运行时和 .NET Framework 应用程序所使用的每个配置文件中的根元素。</span><span class="sxs-lookup"><span data-stu-id="387e9-133">The root element in every configuration file used by the common language runtime and .NET Framework applications.</span></span>|  
|`system.diagnostics`|<span data-ttu-id="387e9-134">指定用于收集、存储和路由消息的跟踪侦听器以及对跟踪开关设置的级别。</span><span class="sxs-lookup"><span data-stu-id="387e9-134">Specifies trace listeners that collect, store, and route messages and the level where a trace switch is set.</span></span>|  
|`sharedListeners`|<span data-ttu-id="387e9-135">任何源或跟踪元素都可以引用的侦听器的集合。</span><span class="sxs-lookup"><span data-stu-id="387e9-135">A collection of listeners that any source or trace element can reference.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="387e9-136">备注</span><span class="sxs-lookup"><span data-stu-id="387e9-136">Remarks</span></span>  

 <span data-ttu-id="387e9-137">随 .NET Framework 附带的侦听器类派生自 <xref:System.Diagnostics.TraceListener> 类。</span><span class="sxs-lookup"><span data-stu-id="387e9-137">The listener classes shipped with the .NET Framework derive from the <xref:System.Diagnostics.TraceListener> class.</span></span> <span data-ttu-id="387e9-138">特性的值 `name` 用于将共享侦听器添加到 `Listeners` 跟踪源或跟踪源的集合中。</span><span class="sxs-lookup"><span data-stu-id="387e9-138">The value for the `name` attribute is used to add the shared listener to a `Listeners` collection for either a trace or a trace source.</span></span> <span data-ttu-id="387e9-139">该属性的值 `initializeData` 取决于所创建的侦听器的类型。</span><span class="sxs-lookup"><span data-stu-id="387e9-139">The value for the `initializeData` attribute depends on the type of listener you create.</span></span> <span data-ttu-id="387e9-140">并非所有跟踪侦听器都要求您指定 `initializeData` 。</span><span class="sxs-lookup"><span data-stu-id="387e9-140">Not all trace listeners require that you specify `initializeData`.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="387e9-141">使用 `initializeData` 属性时，可能会收到编译器警告 "未声明 ' initializeData ' 特性"。</span><span class="sxs-lookup"><span data-stu-id="387e9-141">When you use the `initializeData` attribute, you may get the compiler warning "The 'initializeData' attribute is not declared."</span></span> <span data-ttu-id="387e9-142">之所以出现此警告，是因为配置设置是针对抽象基类验证的 <xref:System.Diagnostics.TraceListener> ，后者不识别 `initializeData` 属性。</span><span class="sxs-lookup"><span data-stu-id="387e9-142">This warning occurs because the configuration settings are validated against the abstract base class <xref:System.Diagnostics.TraceListener>, which does not recognize the `initializeData` attribute.</span></span> <span data-ttu-id="387e9-143">通常，对于具有采用参数的构造函数的跟踪侦听器实现，你可以忽略此警告。</span><span class="sxs-lookup"><span data-stu-id="387e9-143">Typically, you can ignore this warning for trace listener implementations that have a constructor that takes a parameter.</span></span>  
  
 <span data-ttu-id="387e9-144">下表显示了 .NET Framework 附带的跟踪侦听器，并描述了其属性的值 `initializeData` 。</span><span class="sxs-lookup"><span data-stu-id="387e9-144">The following table shows the trace listeners that are included with the .NET Framework and describes the value of their `initializeData` attributes.</span></span>  
  
|<span data-ttu-id="387e9-145">跟踪侦听器类</span><span class="sxs-lookup"><span data-stu-id="387e9-145">Trace listener class</span></span>|<span data-ttu-id="387e9-146">initializeData 特性值</span><span class="sxs-lookup"><span data-stu-id="387e9-146">initializeData attribute value</span></span>|  
|--------------------------|------------------------------------|  
|<xref:System.Diagnostics.ConsoleTraceListener>|<span data-ttu-id="387e9-147">`useErrorStream`构造函数的值 <xref:System.Diagnostics.ConsoleTraceListener.%23ctor%2A> 。</span><span class="sxs-lookup"><span data-stu-id="387e9-147">The `useErrorStream` value for the <xref:System.Diagnostics.ConsoleTraceListener.%23ctor%2A> constructor.</span></span>  <span data-ttu-id="387e9-148">将 `initializeData` 属性设置为 " `true` " 可将跟踪和调试输出写入标准错误流; 将该属性设置为 " `false` " 可写入标准输出流。</span><span class="sxs-lookup"><span data-stu-id="387e9-148">Set the `initializeData` attribute to "`true`" to write trace and debug output to the standard error stream; set it to "`false`" to write to the standard output stream.</span></span>|  
|<xref:System.Diagnostics.DelimitedListTraceListener>|<span data-ttu-id="387e9-149"><xref:System.Diagnostics.DelimitedListTraceListener> 写入的文件名。</span><span class="sxs-lookup"><span data-stu-id="387e9-149">The name of the file the <xref:System.Diagnostics.DelimitedListTraceListener> writes to.</span></span>|  
|<xref:System.Diagnostics.EventLogTraceListener?displayProperty=nameWithType>|<span data-ttu-id="387e9-150">现有的事件日志源的名称。</span><span class="sxs-lookup"><span data-stu-id="387e9-150">The name of an existing event log source.</span></span>|  
|<xref:System.Diagnostics.EventSchemaTraceListener?displayProperty=nameWithType>|<span data-ttu-id="387e9-151">写入的文件的名称 <xref:System.Diagnostics.EventSchemaTraceListener> 。</span><span class="sxs-lookup"><span data-stu-id="387e9-151">The name of the file that the <xref:System.Diagnostics.EventSchemaTraceListener> writes to.</span></span>|  
|<xref:System.Diagnostics.TextWriterTraceListener?displayProperty=nameWithType>|<span data-ttu-id="387e9-152">写入的文件的名称 <xref:System.Diagnostics.TextWriterTraceListener> 。</span><span class="sxs-lookup"><span data-stu-id="387e9-152">The name of the file that the <xref:System.Diagnostics.TextWriterTraceListener> writes to.</span></span>|  
|<xref:System.Diagnostics.XmlWriterTraceListener>|<span data-ttu-id="387e9-153">写入的文件的名称 <xref:System.Diagnostics.XmlWriterTraceListener> 。</span><span class="sxs-lookup"><span data-stu-id="387e9-153">The name of the file that the <xref:System.Diagnostics.XmlWriterTraceListener> writes to.</span></span>|  
  
## <a name="configuration-file"></a><span data-ttu-id="387e9-154">配置文件</span><span class="sxs-lookup"><span data-stu-id="387e9-154">Configuration File</span></span>  

 <span data-ttu-id="387e9-155">此元素可在计算机配置文件中使用 ( # A0) 和应用程序配置文件。</span><span class="sxs-lookup"><span data-stu-id="387e9-155">This element can be used in the machine configuration file (Machine.config) and the application configuration file.</span></span>  
  
## <a name="example"></a><span data-ttu-id="387e9-156">示例</span><span class="sxs-lookup"><span data-stu-id="387e9-156">Example</span></span>  

 <span data-ttu-id="387e9-157">下面的示例演示如何使用 `<add>` 元素将添加 <xref:System.Diagnostics.TextWriterTraceListener> `textListener` 到 `sharedListeners` 集合中。</span><span class="sxs-lookup"><span data-stu-id="387e9-157">The following example shows how to use `<add>` elements to add the <xref:System.Diagnostics.TextWriterTraceListener>`textListener` to the `sharedListeners` collection.</span></span>   <span data-ttu-id="387e9-158">`textListener` 按名称添加到 `Listeners` 跟踪源的集合中 `TraceSourceApp` 。</span><span class="sxs-lookup"><span data-stu-id="387e9-158">`textListener` is added by name to the `Listeners` collection for the trace source `TraceSourceApp`.</span></span> <span data-ttu-id="387e9-159">`textListener`侦听器将跟踪输出写入文件 myListener。</span><span class="sxs-lookup"><span data-stu-id="387e9-159">The `textListener` listener writes trace output to the file myListener.log.</span></span>  
  
```xml  
<configuration>  
  <system.diagnostics>  
    <sources>  
      <source name="TraceSourceApp" switchName="sourceSwitch"
        switchType="System.Diagnostics.SourceSwitch">  
        <listeners>  
          <add name="console"
            type="System.Diagnostics.ConsoleTraceListener"/>  
          <add name="textListener"/>  
          <remove name="Default"/>  
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
  
## <a name="see-also"></a><span data-ttu-id="387e9-160">请参阅</span><span class="sxs-lookup"><span data-stu-id="387e9-160">See also</span></span>

- <xref:System.Diagnostics.TraceSource>
- <xref:System.Diagnostics.TraceListener>
- [<span data-ttu-id="387e9-161">跟踪和调试设置架构</span><span class="sxs-lookup"><span data-stu-id="387e9-161">Trace and Debug Settings Schema</span></span>](index.md)
- [<span data-ttu-id="387e9-162">跟踪侦听器</span><span class="sxs-lookup"><span data-stu-id="387e9-162">Trace Listeners</span></span>](../../../debug-trace-profile/trace-listeners.md)
