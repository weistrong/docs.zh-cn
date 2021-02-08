---
description: 了解详细信息： <etwEnable> 元素
title: <etwEnable> 元素
ms.date: 03/30/2017
helpviewer_keywords:
- etwEnable element
- <etwEnable> element
ms.assetid: 29dde982-6d8b-4099-8867-ad0d7733f6dc
ms.openlocfilehash: 224784f47d15788ded41a5756e1d179a5a25907b
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99787040"
---
# <a name="etwenable-element"></a>\<etwEnable> 元素

指定是否为公共语言运行时事件启用 Windows 事件跟踪 (ETW)。  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<runtime>**](runtime-element.md)\
&nbsp;&nbsp;&nbsp;&nbsp;**\<etwEnabled>**  
  
## <a name="syntax"></a>语法  
  
```xml  
<etwEnable enabled="true|false"/>  
```  
  
## <a name="attributes-and-elements"></a>特性和元素  

 下列各节描述了特性、子元素和父元素。  
  
### <a name="attributes"></a>特性  
  
|属性|说明|  
|---------------|-----------------|  
|enabled|必需的特性。<br /><br /> 指定是否应启用 ETW。|  
  
## <a name="enabled-attribute"></a>enabled 特性  
  
|值|说明|  
|-----------|-----------------|  
|是|启用 ETW。 这是从 Windows Vista 和 Windows Server 2008 操作系统开始的 Windows 版本的默认值。|  
|false|禁用 ETW。 这是早期版本的 Windows 的默认设置。|  
  
### <a name="child-elements"></a>子元素  

 无。  
  
### <a name="parent-elements"></a>父元素  
  
|元素|说明|  
|-------------|-----------------|  
|`configuration`|公共语言运行时和 .NET Framework 应用程序所使用的每个配置文件中的根元素。|  
|`runtime`|包含有关程序集绑定和垃圾回收的信息。|  
  
## <a name="remarks"></a>备注  

 从 Windows Vista 开始，默认情况下启用 ETW。 使用此元素可禁用应用程序的 ETW。 在早期版本的 Windows 中，使用此元素为应用程序启用 ETW。  
  
> [!NOTE]
> 可以通过使用注册表设置在服务器上全局启用或禁用 ETW。 请参阅 [控制 .NET Framework 日志记录](../../../performance/controlling-logging.md)。  
  
## <a name="example"></a>示例  

 下面的示例演示如何为应用程序启用 ETW 跟踪。  
  
```xml  
<configuration>  
   <runtime>  
      <etwEnable enabled="true" />  
   </runtime>  
</configuration>  
```  
  
## <a name="see-also"></a>请参阅

- [运行时设置架构](index.md)
- [配置文件架构](../index.md)
- [控制 .NET Framework 日志记录](../../../performance/controlling-logging.md)
