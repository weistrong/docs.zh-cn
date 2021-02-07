---
description: 了解详细信息： NameValueSectionHandler 和 DictionarySectionHandler 的自定义元素
title: NameValueSectionHandler 和 DictionarySectionHandler 的自定义元素
ms.date: 05/01/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/sectionName
helpviewer_keywords:
- custom element
ms.assetid: 2303031f-4c1d-4df4-bca1-e9bd96ca40dc
ms.openlocfilehash: c1bb5b2fb321e2cc9235e02be2158c0875d42032
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99698721"
---
# <a name="custom-element-for-namevaluesectionhandler-and-dictionarysectionhandler"></a>NameValueSectionHandler 和 DictionarySectionHandler 的自定义元素

定义使用和类的自定义配置节的设置 <xref:System.Configuration.NameValueSectionHandler> <xref:System.Configuration.DictionarySectionHandler> 。

[**\<configuration>**](configuration-element.md)\
&nbsp;&nbsp;**\<sectionName>**

## <a name="attributes"></a>特性

无

## <a name="parent-element"></a>父元素

|     | 描述 |
| --- | ----------- |
| [**\<configuration>**](configuration-element.md) | 公共语言运行时和 .NET Framework 应用程序所使用的每个配置文件中的根元素。 |

## <a name="child-elements"></a>子元素

|     | 说明 |
| --- | ----------- |
| [**\<add>**](add-element-for-custom-2.md) 对于 <xref:System.Configuration.NameValueSectionHandler> 和 <xref:System.Configuration.DictionarySectionHandler>  | 添加自定义应用程序设置。 |
| [**\<remove>**](remove-element-for-custom-2.md) 对于 <xref:System.Configuration.NameValueSectionHandler> 和 <xref:System.Configuration.DictionarySectionHandler> | 删除以前定义的设置。 |
| [**\<clear>**](clear-element-for-custom-2.md) 对于 <xref:System.Configuration.NameValueSectionHandler> 和 <xref:System.Configuration.DictionarySectionHandler> | 清除节中所有先前定义的设置。 |

## <a name="remarks"></a>备注

**\<sectionName>** 元素是由元素中的标记定义的自定义元素 **\<section>** **\<configSections>** 。

下表显示 ConfigurationSettings. GetConfig 方法为每个配置节处理程序返回的对象类型：

| 配置节处理程序                        | 返回类型                                                |
| ---------------------------------------------------- | ---------------------------------------------------------- |
| <xref:System.Configuration.NameValueSectionHandler>  | <xref:System.Collections.Specialized.NameValueCollection>  |
| <xref:System.Configuration.DictionarySectionHandler> | <xref:System.Collections.IDictionary>                      |

## <a name="example"></a>示例

下面的示例演示如何声明使用和类的节 <xref:System.Configuration.DictionarySectionHandler> <xref:System.Configuration.NameValueSectionHandler> 。

第一个自定义元素为 **\<dictionarySample>** ，其中包含由 <xref:System.Configuration.DictionarySectionHandler> 程序集中的类读取的设置 `System.dll` 。 第二个自定义元素为 **\<mySection>** ，其中包含由 <xref:System.Configuration.NameValueSectionHandler> 程序集中的类读取的设置 `System.dll` 。

```xml
<configuration>
  <configSections>
    <section name="dictionarySample" type="System.Configuration.DictionarySectionHandler,System" />
    <sectionGroup name="mySectionGroup">
      <section name="mySection" type="System.Configuration.NameValueSectionHandler,System" />
    </sectionGroup>
  </configSections>
  <dictionarySample>
    <add key="myKey" value="myValue" />
  </dictionarySample>
  <mySectionGroup>
    <mySection>
      <add key="key1" value="value1" />
    </mySection>
  </mySectionGroup>
</configuration>
```

## <a name="configuration-file"></a>配置文件

此元素可用于应用程序配置文件、计算机配置文件 (*Machine.config*) 和 *Web.config* 不在应用程序目录级别的文件。

## <a name="see-also"></a>请参阅

- [.NET Framework 的配置文件架构](index.md)
