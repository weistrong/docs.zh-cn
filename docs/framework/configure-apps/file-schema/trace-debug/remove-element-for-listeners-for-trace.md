---
description: 详细了解： <remove> <listeners> 的元素 <trace>
title: <remove>的元素 <listeners><trace>
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/system.diagnostics/trace/listeners/remove
helpviewer_keywords:
- remove element
- <remove> element
ms.assetid: 9a5cd1b5-be1a-485f-8f0c-2890ad3ef3e0
ms.openlocfilehash: 8b863cb535c28f090374e284717d5bf38f22e881
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99750593"
---
# <a name="remove-element-for-listeners-for-trace"></a><span data-ttu-id="842e8-103">\<remove>的元素 \<listeners>\<trace></span><span class="sxs-lookup"><span data-stu-id="842e8-103">\<remove> Element for \<listeners> for \<trace></span></span>

<span data-ttu-id="842e8-104">从 **侦听器** 集合中删除侦听器。</span><span class="sxs-lookup"><span data-stu-id="842e8-104">Removes a listener from the **Listeners** collection.</span></span>  

[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.diagnostics>**](system-diagnostics-element.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<trace>**](trace-element.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<listeners>**](listeners-element-for-trace.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<remove>**

## <a name="syntax"></a><span data-ttu-id="842e8-105">语法</span><span class="sxs-lookup"><span data-stu-id="842e8-105">Syntax</span></span>  
  
```xml  
<remove name="listener name" />  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="842e8-106">特性和元素</span><span class="sxs-lookup"><span data-stu-id="842e8-106">Attributes and Elements</span></span>  

 <span data-ttu-id="842e8-107">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="842e8-107">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="842e8-108">特性</span><span class="sxs-lookup"><span data-stu-id="842e8-108">Attributes</span></span>  
  
|<span data-ttu-id="842e8-109">属性</span><span class="sxs-lookup"><span data-stu-id="842e8-109">Attribute</span></span>|<span data-ttu-id="842e8-110">说明</span><span class="sxs-lookup"><span data-stu-id="842e8-110">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="842e8-111">**name**</span><span class="sxs-lookup"><span data-stu-id="842e8-111">**name**</span></span>|<span data-ttu-id="842e8-112">必需的特性。</span><span class="sxs-lookup"><span data-stu-id="842e8-112">Required attribute.</span></span><br /><br /> <span data-ttu-id="842e8-113">要从 **侦听器** 集合中删除的侦听器的名称。</span><span class="sxs-lookup"><span data-stu-id="842e8-113">The name of the listener to remove from the **Listeners** collection.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="842e8-114">子元素</span><span class="sxs-lookup"><span data-stu-id="842e8-114">Child Elements</span></span>  

 <span data-ttu-id="842e8-115">无。</span><span class="sxs-lookup"><span data-stu-id="842e8-115">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="842e8-116">父元素</span><span class="sxs-lookup"><span data-stu-id="842e8-116">Parent Elements</span></span>  
  
|<span data-ttu-id="842e8-117">元素</span><span class="sxs-lookup"><span data-stu-id="842e8-117">Element</span></span>|<span data-ttu-id="842e8-118">说明</span><span class="sxs-lookup"><span data-stu-id="842e8-118">Description</span></span>|  
|-------------|-----------------|  
|`configuration`|<span data-ttu-id="842e8-119">公共语言运行时和 .NET Framework 应用程序所使用的每个配置文件中的根元素。</span><span class="sxs-lookup"><span data-stu-id="842e8-119">The root element in every configuration file used by the common language runtime and .NET Framework applications.</span></span>|  
|`listeners`|<span data-ttu-id="842e8-120">指定用于收集、存储和路由消息的侦听器。</span><span class="sxs-lookup"><span data-stu-id="842e8-120">Specifies a listener that collects, stores, and routes messages.</span></span> <span data-ttu-id="842e8-121">侦听器将跟踪输出定向到适当的目标。</span><span class="sxs-lookup"><span data-stu-id="842e8-121">Listeners direct the tracing output to an appropriate target.</span></span>|  
|`system.diagnostics`|<span data-ttu-id="842e8-122">指定用于收集、存储和路由消息的跟踪侦听器以及对跟踪开关设置的级别。</span><span class="sxs-lookup"><span data-stu-id="842e8-122">Specifies trace listeners that collect, store, and route messages and the level where a trace switch is set.</span></span>|  
|`trace`|<span data-ttu-id="842e8-123">配置 ASP.NET 跟踪服务。</span><span class="sxs-lookup"><span data-stu-id="842e8-123">Configures the ASP.NET trace service.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="842e8-124">备注</span><span class="sxs-lookup"><span data-stu-id="842e8-124">Remarks</span></span>  
  
> [!NOTE]
> <span data-ttu-id="842e8-125"><xref:System.Diagnostics.DefaultTraceListener>从集合中移除会 `Listeners` 改变 <xref:System.Diagnostics.Debug.Assert%2A?displayProperty=nameWithType> 、 <xref:System.Diagnostics.Trace.Assert%2A?displayProperty=nameWithType> 、 <xref:System.Diagnostics.Debug.Fail%2A?displayProperty=nameWithType> 和方法的行为 <xref:System.Diagnostics.Trace.Fail%2A?displayProperty=nameWithType> 。</span><span class="sxs-lookup"><span data-stu-id="842e8-125">Removing the <xref:System.Diagnostics.DefaultTraceListener> from the `Listeners` collection alters the behavior of the <xref:System.Diagnostics.Debug.Assert%2A?displayProperty=nameWithType>, <xref:System.Diagnostics.Trace.Assert%2A?displayProperty=nameWithType>, <xref:System.Diagnostics.Debug.Fail%2A?displayProperty=nameWithType>, and <xref:System.Diagnostics.Trace.Fail%2A?displayProperty=nameWithType> methods.</span></span> <span data-ttu-id="842e8-126">`Assert` `Fail` 通常，调用或方法会导致显示消息框，但是，如果不 <xref:System.Diagnostics.DefaultTraceListener> 在集合中，则不会显示消息框 `Listeners` 。</span><span class="sxs-lookup"><span data-stu-id="842e8-126">Calling an `Assert` or `Fail` method normally results in the display of a message box, however the message box is not displayed if the <xref:System.Diagnostics.DefaultTraceListener> is not in the `Listeners` collection.</span></span>  
  
## <a name="example"></a><span data-ttu-id="842e8-127">示例</span><span class="sxs-lookup"><span data-stu-id="842e8-127">Example</span></span>  

 <span data-ttu-id="842e8-128">下面的示例演示如何从跟踪 **侦听器** 集合中删除默认的跟踪侦听器。</span><span class="sxs-lookup"><span data-stu-id="842e8-128">The following example shows how to remove the default trace listener from the trace **Listeners** collection.</span></span>  
  
```xml  
<configuration>  
   <system.diagnostics>  
      <trace autoflush="true" indentsize="0">  
         <listeners>  
            <remove name="Default" />  
         </listeners>  
      </trace>  
   </system.diagnostics>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="842e8-129">请参阅</span><span class="sxs-lookup"><span data-stu-id="842e8-129">See also</span></span>

- <xref:System.Diagnostics.TraceListener>
- <xref:System.Diagnostics.DefaultTraceListener>
- <xref:System.Diagnostics.TextWriterTraceListener>
- <xref:System.Diagnostics.EventLogTraceListener>
- [<span data-ttu-id="842e8-130">跟踪和调试设置架构</span><span class="sxs-lookup"><span data-stu-id="842e8-130">Trace and Debug Settings Schema</span></span>](index.md)
