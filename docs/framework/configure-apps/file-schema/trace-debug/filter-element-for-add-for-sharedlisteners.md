---
description: 详细了解： <filter> <add> 的元素 <sharedListeners>
title: <filter>的元素 <add><sharedListeners>
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/system.diagnostics/sharedListeners/add/filter
helpviewer_keywords:
- filter element for <add> for <sharedListeners>
- initializeData attribute
- <filter> element for <add> for <sharedListeners>
- filters, trace listeners
- trace listeners, filters
ms.assetid: 7d4e7faa-2e4e-4379-ac76-f6cd7f2f8fac
ms.openlocfilehash: 5d6567ff029dea5ed98054dbc524bb7ed405324c
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99802367"
---
# <a name="filter-element-for-add-for-sharedlisteners"></a>\<filter>的元素 \<add>\<sharedListeners>

将筛选器添加到 `sharedListeners` 集合中的侦听器。  

[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.diagnostics>**](system-diagnostics-element.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<sharedListeners>**](sharedlisteners-element.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<add>**](add-element-for-sharedlisteners.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<filter>**

## <a name="syntax"></a>语法  
  
```xml  
<filter type="System.Diagnostics.EventTypeFilter"
  initializeData="Warning" />  
```  
  
## <a name="attributes-and-elements"></a>特性和元素  

 下列各节描述了特性、子元素和父元素。  
  
### <a name="attributes"></a>特性  
  
|属性|说明|  
|---------------|-----------------|  
|type |必需的特性。<br /><br /> 指定筛选器的类型。 只能使用) 属性格式 (类型的全名 <xref:System.Type.FullName%2A?displayProperty=nameWithType> ，也可以使用完全限定的类型名称，包括 (格式的程序集信息， <xref:System.Type.AssemblyQualifiedName%2A?displayProperty=nameWithType>) 属性。 有关创建完全限定类型名称的信息，请参阅 [指定完全限定的类型](../../../reflection-and-codedom/specifying-fully-qualified-type-names.md)名称。|  
|**initializeData**|可选特性。<br /><br /> 传递到指定类的构造函数的字符串。|  
  
### <a name="child-elements"></a>子元素  

 无。  
  
### <a name="parent-elements"></a>父元素  
  
|元素|说明|  
|-------------|-----------------|  
|`configuration`|公共语言运行时和 .NET Framework 应用程序所使用的每个配置文件中的根元素。|  
|`system.diagnostics`|指定用于收集、存储和路由消息的跟踪侦听器以及对跟踪开关设置的级别。|  
|`sharedListeners`|任何源或跟踪元素都可以引用的侦听器的集合。|  
|`add`|将侦听器添加到 **sharedListeners** 集合。|  
  
## <a name="remarks"></a>备注  

 如果侦听器是在 `<add>` 元素的元素中定义的 `<sharedListeners>` ，则应在作为元素的子元素的元素中定义该侦听器的筛选器 `<filter>` `<add>` 。  
  
 此元素可在计算机配置文件中使用 ( # A0) 和应用程序配置文件。  
  
## <a name="example"></a>示例  

 下面的示例演示如何使用 `<filter>` 元素将筛选器添加到集合中的跟踪侦听器 `console` `sharedListeners` 。  
  
```xml  
<configuration>  
  <system.diagnostics>  
    <sources>  
      <source name="myTraceSource" >  
        <listeners>  
          <add name="console" />  
          <remove name="Default" />  
        </listeners>  
      </source>  
    </sources>  
    <sharedListeners>  
      <add name="console"
        type="System.Diagnostics.ConsoleTraceListener" >  
        <filter type="System.Diagnostics.EventTypeFilter"
          initializeData="Error" />  
      </add>  
    </sharedListeners>  
  </system.diagnostics>  
</configuration>  
```  
  
## <a name="see-also"></a>请参阅

- <xref:System.Diagnostics.TraceFilter>
- <xref:System.Diagnostics.TraceListener>
- <xref:System.Diagnostics.TraceSource>
- [跟踪和调试设置架构](index.md)
