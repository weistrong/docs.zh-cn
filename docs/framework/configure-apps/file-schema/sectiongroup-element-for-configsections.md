---
description: 详细了解： <sectionGroup> 的元素 <configSections>
title: <configSections> 的 <sectionGroup> 元素
ms.date: 05/01/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/configSections/sectionGroup
helpviewer_keywords:
- sectionGroup Element
- <sectionGroup> Element
ms.assetid: 6c27f9e2-809c-4bc9-aca9-72f90360e7a3
ms.openlocfilehash: 0d822b98acbc041b9d6e146e9cd15848a73d2f88
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99639882"
---
# <a name="sectiongroup-element-for-configsections"></a>\<configSections> 的 \<sectionGroup> 元素

定义配置节的命名空间。

[**\<configuration>**](configuration-element.md)\
&nbsp;&nbsp;[**\<configSections>**](configsections-element-for-configuration.md)\
&nbsp;&nbsp;&nbsp;&nbsp;**\<sectionGroup>**

## <a name="syntax"></a>语法

```xml
<sectionGroup name="section group name">
  <!-- Configuration sections -->
</sectionGroup>
```

## <a name="attribute"></a>Attribute

|           | 说明 |
| --------- | ----------- |
| **name**  | 必需的特性。<br><br>指定正在定义的节组的名称。 |

## <a name="parent-element"></a>父元素

|     | 描述 |
| --- | ----------- |
| [**\<configSections>** 元素](configsections-element-for-configuration.md) | 包含配置节和命名空间声明。 |

## <a name="child-elements"></a>子元素

|     | 说明 |
| --- | ----------- |
| [**\<section>**](section-element.md) | 包含配置节声明。 |

## <a name="remarks"></a>备注

声明节组将为配置节创建容器标记，并确保与其他人定义的配置节之间没有命名冲突。 可以在彼此 **\<sectionGroup>** 之间嵌套元素。

## <a name="example"></a>示例

下面的示例演示如何声明一个节组，并在节组中声明部分：

```xml
<configuration>
  <configSections>
    <sectionGroup name="mySectionGroup">
      <section name="mySection"
               type="System.Configuration.NameValueSectionHandler,System" />
    </sectionGroup>
  </configSections>
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
