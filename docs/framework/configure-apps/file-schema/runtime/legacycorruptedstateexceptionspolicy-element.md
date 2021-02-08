---
description: 了解详细信息： <legacyCorruptedStateExceptionsPolicy> 元素
title: <legacyCorruptedStateExceptionsPolicy> 元素
ms.date: 03/30/2017
helpviewer_keywords:
- <legacyCorruptedStateExceptionsPolicy> element
- legacyCorruptedStateExceptionsPolicy element
ms.assetid: e0a55ddc-bfa8-4f3e-ac14-d1fc3330e4bb
ms.openlocfilehash: 34082c0779b09400a875894359cf7cf501173508
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99786949"
---
# <a name="legacycorruptedstateexceptionspolicy-element"></a>\<legacyCorruptedStateExceptionsPolicy> 元素

指定公共语言运行时是否允许托管代码捕获访问冲突和其他损坏状态异常。  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<runtime>**](runtime-element.md)\
&nbsp;&nbsp;&nbsp;&nbsp;**\<legacyCorruptedStateExceptionsPolicy>**  
  
## <a name="syntax"></a>语法  
  
```xml  
<legacyCorruptedStateExceptionsPolicy enabled="true|false"/>  
```  
  
## <a name="attributes-and-elements"></a>特性和元素  

 下列各节描述了特性、子元素和父元素。  
  
### <a name="attributes"></a>特性  
  
|属性|描述|  
|---------------|-----------------|  
|`enabled`|必需的特性。<br /><br /> 指定应用程序将捕获损坏状态异常故障，例如访问冲突。|  
  
## <a name="enabled-attribute"></a>enabled 特性  
  
|值|说明|  
|-----------|-----------------|  
|`false`|应用程序不会捕获损坏状态异常故障，例如访问冲突。 这是默认设置。|  
|`true`|应用程序将捕获损坏状态异常故障，例如访问冲突。|  
  
### <a name="child-elements"></a>子元素  

 无。  
  
### <a name="parent-elements"></a>父元素  
  
|元素|说明|  
|-------------|-----------------|  
|`configuration`|公共语言运行时和 .NET Framework 应用程序所使用的每个配置文件中的根元素。|  
|`runtime`|包含有关程序集绑定和垃圾回收的信息。|  
  
## <a name="remarks"></a>备注  

 在 .NET Framework 版本3.5 及更早版本中，公共语言运行时允许托管代码捕获由损坏的进程状态引发的异常。 访问冲突就是这种类型的异常的一个示例。  
  
 从 .NET Framework 4 开始，托管代码不再在块中捕获这些类型的异常 `catch` 。 不过，你可以通过两种方式重写此更改并保持对损坏状态异常的处理：  
  
- 将 `<legacyCorruptedStateExceptionsPolicy>` 元素的 `enabled` 属性设置为 `true` 。 此配置设置将应用 processwide 并影响所有方法。  
  
 \- 或 -  
  
- 将特性应用于 <xref:System.Runtime.ExceptionServices.HandleProcessCorruptedStateExceptionsAttribute?displayProperty=nameWithType> 包含异常块的方法 `catch` 。  
  
 此配置元素仅在 .NET Framework 4 及更高版本中可用。  
  
## <a name="example"></a>示例  

 下面的示例演示如何指定应用程序应恢复到 .NET Framework 4 之前的行为，并捕获所有损坏状态异常错误。  
  
```xml  
<configuration>  
   <runtime>  
      <legacyCorruptedStateExceptionsPolicy enabled="true" />  
   </runtime>  
</configuration>  
```  
  
## <a name="see-also"></a>请参阅

- <xref:System.Runtime.ExceptionServices.HandleProcessCorruptedStateExceptionsAttribute>
- [运行时设置架构](index.md)
- [配置文件架构](../index.md)
