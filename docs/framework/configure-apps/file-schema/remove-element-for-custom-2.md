---
description: 了解详细信息： <remove> NameValueSectionHandler 和 DictionarySectionHandler 的元素
title: <remove> NameValueSectionHandler 和 DictionarySectionHandler 的元素
ms.date: 05/01/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/sectionName/remove
helpviewer_keywords:
- remove Element
- <remove> Element
ms.assetid: 8d8af7f5-26c9-4db9-bbe4-b2a4e6949568
ms.openlocfilehash: bf1434b257aa014c8f46e34f2d57d109bd510452
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99740075"
---
# <a name="remove-element-for-namevaluesectionhandler-and-dictionarysectionhandler"></a>\<remove> NameValueSectionHandler 和 DictionarySectionHandler 的元素

删除以前定义的设置。

[**\<configuration>**](configuration-element.md)\
&nbsp;&nbsp;[**\<sectionName>**](custom-element-2.md)\
&nbsp;&nbsp;&nbsp;&nbsp;**\<remove>**

## <a name="syntax"></a>语法

```xml
<add remove="key" />
```

## <a name="attribute"></a>Attribute

|           | 说明 |
| --------- | ----------- |
| key    | 必需的特性。<br><br>指定要删除的设置的名称。 |

## <a name="parent-element"></a>父元素

| 元素 | 说明 |
| ------- | ------------|
| [**\<sectionName>** 元素](custom-element-2.md) | 定义使用和类的自定义配置节的设置 <xref:System.Configuration.NameValueSectionHandler> <xref:System.Configuration.DictionarySectionHandler> 。 |

## <a name="child-elements"></a>子元素

无

## <a name="remarks"></a>备注

你可以使用 **\<remove>** 元素从你的应用程序中删除在配置文件层次结构中较高级别上定义的设置。

## <a name="example"></a>示例

下面的示例演示如何使用 **\<remove>** 应用程序配置文件中的元素删除以前在计算机配置文件中定义的设置。

以下计算机配置文件代码声明节， **\<mySection>** 并向其中添加两个 `key1` 设置 `key2` ：

```xml
<!-- Machine.config file -->
<configuration>
  <configSections>
    <section name="mySection" type="System.Configuration.NameValueSectionHandler,System" />
  </configSections>
  <mySection>
    <add key="key1" value="value1" />
    <add key="key2" value="value2" />
  </mySection>
</configuration>
```

以下应用程序配置文件代码将删除以下 `key2` 设置 **\<mySection>** ：

```xml
<!--Application configuration file -->
<configuration>
  <mySection>
    <remove key="key2" />
  </mySection>
</configuration>
```

## <a name="configuration-file"></a>配置文件

此元素可用于应用程序配置文件、计算机配置文件 (*Machine.config*) 和 *Web.config* 不在应用程序目录级别的文件。

## <a name="see-also"></a>请参阅

- [.NET Framework 的配置文件架构](index.md)
