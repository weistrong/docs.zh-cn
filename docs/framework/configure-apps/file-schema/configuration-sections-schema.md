---
description: 了解详细信息：配置节架构
title: 配置节架构
ms.date: 05/02/2017
helpviewer_keywords:
- configuration settings [.NET Framework], custom
- schema configuration settings
- configuration sections [.NET Framework]
- custom elements
- configuration schema [.NET Framework], custom settings in configuration files
- elements [.NET Framework], custom settings in configuration files
ms.assetid: 6e4cc793-c526-4007-b4e9-37d56295f2cb
ms.openlocfilehash: f16ca16417da0b3ee7a7d0a5ebdd1a446ec0714a
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99698955"
---
# <a name="configuration-sections-schema"></a>配置节架构

配置节架构包含用于在配置文件中定义自定义设置的元素。 有关配置文件和架构的一般信息，请参阅 [.NET Framework 的配置文件架构](index.md)。

[**\<configuration>**](configuration-element.md)
[**\<configSections>**](configsections-element-for-configuration.md)
[**\<section>**](section-element.md)
[**\<sectionGroup>**](sectiongroup-element-for-configsections.md)

|     | 说明 |
| --- | ----------- |
| [**\<configSections>**](configsections-element-for-configuration.md) | 包含配置节和命名空间声明。 |
| [**\<section>** 对于 **\<configSections>** 和 **\<sectionGroup>**](section-element.md) | 包含配置节声明。 |
| [**\<sectionGroup>** 进行 **\<configSections>**](sectiongroup-element-for-configsections.md) | 定义配置节的命名空间。 |

<a name="dep"></a>

## <a name="unimplemented-elements"></a>未实现元素

以下元素不会有任何影响，因此不应使用：

* **\<clear>**
* **\<remove>**
