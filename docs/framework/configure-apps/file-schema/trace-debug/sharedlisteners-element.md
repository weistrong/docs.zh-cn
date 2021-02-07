---
description: 了解详细信息： <sharedListeners> 元素
title: <sharedListeners> 元素
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#sharedListeners
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/system.diagnostics/sharedListeners
helpviewer_keywords:
- <sharedListeners> element
- listeners
- shared listeners
- trace listeners, <sharedListeners> element
- sharedListeners element
ms.assetid: de200534-19dd-4156-86cf-c50521802c4c
ms.openlocfilehash: 904648754c99464e1109a04a5a19b52ec1a1cace
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99750554"
---
# <a name="sharedlisteners-element"></a><span data-ttu-id="44106-103">\<sharedListeners> 元素</span><span class="sxs-lookup"><span data-stu-id="44106-103">\<sharedListeners> Element</span></span>

<span data-ttu-id="44106-104">包含任何源或跟踪元素可以引用的侦听器。</span><span class="sxs-lookup"><span data-stu-id="44106-104">Contains listeners that any source or trace element can reference.</span></span>  <span data-ttu-id="44106-105">默认情况下，这些侦听器不会接收任何跟踪，而且不能在运行时检索这些侦听器。</span><span class="sxs-lookup"><span data-stu-id="44106-105">These listeners do not receive any traces by default, and it is not possible to retrieve these listeners at run time.</span></span> <span data-ttu-id="44106-106">可以按名称将标识为共享侦听器的侦听器添加到源或跟踪。</span><span class="sxs-lookup"><span data-stu-id="44106-106">Listeners identified as shared listeners can be added to sources or traces by name.</span></span>  
  
[**\<configuration>**](../configuration-element.md)  
&nbsp;&nbsp;[**\<system.diagnostics>**](system-diagnostics-element.md)  
&nbsp;&nbsp;&nbsp;&nbsp;**\<sharedListeners>**  
  
## <a name="syntax"></a><span data-ttu-id="44106-107">语法</span><span class="sxs-lookup"><span data-stu-id="44106-107">Syntax</span></span>  
  
```xml  
<sharedListeners>
  <add>...</add>  
</sharedListeners>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="44106-108">特性和元素</span><span class="sxs-lookup"><span data-stu-id="44106-108">Attributes and Elements</span></span>  

 <span data-ttu-id="44106-109">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="44106-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="44106-110">特性</span><span class="sxs-lookup"><span data-stu-id="44106-110">Attributes</span></span>  

 <span data-ttu-id="44106-111">无。</span><span class="sxs-lookup"><span data-stu-id="44106-111">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="44106-112">子元素</span><span class="sxs-lookup"><span data-stu-id="44106-112">Child Elements</span></span>  
  
|<span data-ttu-id="44106-113">元素</span><span class="sxs-lookup"><span data-stu-id="44106-113">Element</span></span>|<span data-ttu-id="44106-114">说明</span><span class="sxs-lookup"><span data-stu-id="44106-114">Description</span></span>|  
|-------------|-----------------|  
|[\<add>](add-element-for-listeners-for-trace.md)|<span data-ttu-id="44106-115">将侦听器添加到 `sharedListeners` 集合中。</span><span class="sxs-lookup"><span data-stu-id="44106-115">Adds a listener to the `sharedListeners` collection.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="44106-116">父元素</span><span class="sxs-lookup"><span data-stu-id="44106-116">Parent Elements</span></span>  
  
|<span data-ttu-id="44106-117">元素</span><span class="sxs-lookup"><span data-stu-id="44106-117">Element</span></span>|<span data-ttu-id="44106-118">说明</span><span class="sxs-lookup"><span data-stu-id="44106-118">Description</span></span>|  
|-------------|-----------------|  
|`Configuration`|<span data-ttu-id="44106-119">公共语言运行时和 .NET Framework 应用程序所使用的每个配置文件中的根元素。</span><span class="sxs-lookup"><span data-stu-id="44106-119">The root element in every configuration file used by the common language runtime and .NET Framework applications.</span></span>|  
|`system.diagnostics`|<span data-ttu-id="44106-120">为 ASP.NET 配置节指定根元素。</span><span class="sxs-lookup"><span data-stu-id="44106-120">Specifies the root element for the ASP.NET configuration section.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="44106-121">备注</span><span class="sxs-lookup"><span data-stu-id="44106-121">Remarks</span></span>  

 <span data-ttu-id="44106-122">将侦听器添加到共享侦听器集合并不会使其成为活动侦听器。</span><span class="sxs-lookup"><span data-stu-id="44106-122">Adding a listener to the shared listeners collection does not make it an active listener.</span></span> <span data-ttu-id="44106-123">还必须将其添加到跟踪源或跟踪，方法是将其添加到跟踪 `Listeners` 元素的集合。</span><span class="sxs-lookup"><span data-stu-id="44106-123">It must still be added to a trace source or a trace by adding it to the `Listeners` collection for that trace element.</span></span> <span data-ttu-id="44106-124">.NET Framework 中的侦听器类派生自 <xref:System.Diagnostics.TraceListener> 类。</span><span class="sxs-lookup"><span data-stu-id="44106-124">The listener classes in the .NET Framework derive from the <xref:System.Diagnostics.TraceListener> class.</span></span>  
  
 <span data-ttu-id="44106-125">此元素可在计算机配置文件中使用 ( # A0) 和应用程序配置文件。</span><span class="sxs-lookup"><span data-stu-id="44106-125">This element can be used in the machine configuration file (Machine.config) and the application configuration file.</span></span>  
  
## <a name="example"></a><span data-ttu-id="44106-126">示例</span><span class="sxs-lookup"><span data-stu-id="44106-126">Example</span></span>  

 <span data-ttu-id="44106-127">下面的示例演示如何使用 `<sharedListeners>` 元素将侦听器添加 `console` 到 `Listeners` <xref:System.Diagnostics.TraceSource> 和类的集合 <xref:System.Diagnostics.Trace> 。</span><span class="sxs-lookup"><span data-stu-id="44106-127">The following example shows how to use the `<sharedListeners>` element to add the listener `console` to the `Listeners` collection for both the <xref:System.Diagnostics.TraceSource> and <xref:System.Diagnostics.Trace> classes.</span></span> <span data-ttu-id="44106-128">控制台跟踪侦听器通过对或的调用将跟踪信息写入控制台 <xref:System.Diagnostics.TraceSource> <xref:System.Diagnostics.Trace> 。</span><span class="sxs-lookup"><span data-stu-id="44106-128">The console trace listener writes trace information to the console through calls to either <xref:System.Diagnostics.TraceSource> or <xref:System.Diagnostics.Trace>.</span></span>  
  
```xml  
<configuration>  
  <system.diagnostics>  
    <sharedListeners>  
      <add name="console" type="System.Diagnostics.ConsoleTraceListener" >  
        <filter type="System.Diagnostics.EventTypeFilter"  
          initializeData="Warning" />  
      </add>  
    </sharedListeners>  
    <sources>  
      <source name="mySource" switchName="sourceSwitch"  >  
        <listeners>  
          <add name="console" />  
        </listeners>  
      </source>  
    </sources>  
    <switches>  
      <add name="sourceSwitch" value="Verbose"/>  
    </switches>  
    <trace>  
      <listeners>  
        <add name="console" />  
      </listeners>  
    </trace>  
  </system.diagnostics>  
</configuration>
```  
  
## <a name="see-also"></a><span data-ttu-id="44106-129">请参阅</span><span class="sxs-lookup"><span data-stu-id="44106-129">See also</span></span>

- <xref:System.Diagnostics.TraceListener>
- [<span data-ttu-id="44106-130">跟踪和调试设置架构</span><span class="sxs-lookup"><span data-stu-id="44106-130">Trace and Debug Settings Schema</span></span>](index.md)
- [<span data-ttu-id="44106-131">跟踪侦听器</span><span class="sxs-lookup"><span data-stu-id="44106-131">Trace Listeners</span></span>](../../../debug-trace-profile/trace-listeners.md)
