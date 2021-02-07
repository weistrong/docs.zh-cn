---
description: 详细了解： <configSections> 的元素 <configuration>
title: <configuration> 的 <configSections> 元素
ms.date: 05/01/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/configSections
helpviewer_keywords:
- configSections Element
- <configSections> Element
ms.assetid: 9f963c1b-dc3f-4220-a8b6-2dd7a5a8e039
ms.openlocfilehash: 543ceed8d53fd299e8a0b65594592b64d6b833a8
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99698981"
---
# <a name="configsections-element-for-configuration"></a><span data-ttu-id="2aa95-103">\<configuration> 的 \<configSections> 元素</span><span class="sxs-lookup"><span data-stu-id="2aa95-103">\<configSections> element for \<configuration></span></span>

<span data-ttu-id="2aa95-104">包含配置节和命名空间声明。</span><span class="sxs-lookup"><span data-stu-id="2aa95-104">Contains configuration section and namespace declarations.</span></span>

<span data-ttu-id="2aa95-105">[**\<configuration>**](configuration-element.md) &nbsp;&nbsp;**\<configSections>**</span><span class="sxs-lookup"><span data-stu-id="2aa95-105">[**\<configuration>**](configuration-element.md) &nbsp;&nbsp;**\<configSections>**</span></span>

## <a name="attributes"></a><span data-ttu-id="2aa95-106">特性</span><span class="sxs-lookup"><span data-stu-id="2aa95-106">Attributes</span></span>

<span data-ttu-id="2aa95-107">无</span><span class="sxs-lookup"><span data-stu-id="2aa95-107">None</span></span>

## <a name="parent-element"></a><span data-ttu-id="2aa95-108">父元素</span><span class="sxs-lookup"><span data-stu-id="2aa95-108">Parent element</span></span>

|     | <span data-ttu-id="2aa95-109">描述</span><span class="sxs-lookup"><span data-stu-id="2aa95-109">Description</span></span> |
| --- | ----------- |
| [**\<configuration>**](configuration-element.md) | <span data-ttu-id="2aa95-110">公共语言运行时和 .NET Framework 应用程序所使用的每个配置文件中的根元素。</span><span class="sxs-lookup"><span data-stu-id="2aa95-110">The root element in every configuration file used by the common language runtime and .NET Framework applications.</span></span> |

## <a name="child-elements"></a><span data-ttu-id="2aa95-111">子元素</span><span class="sxs-lookup"><span data-stu-id="2aa95-111">Child elements</span></span>

|     | <span data-ttu-id="2aa95-112">说明</span><span class="sxs-lookup"><span data-stu-id="2aa95-112">Description</span></span> |
| --- | ----------- |
| [**\<section>**](section-element.md) | <span data-ttu-id="2aa95-113">包含配置节声明。</span><span class="sxs-lookup"><span data-stu-id="2aa95-113">Contains a configuration section declaration.</span></span> |
| [**\<sectionGroup>**](sectiongroup-element-for-configsections.md) | <span data-ttu-id="2aa95-114">定义配置节的命名空间。</span><span class="sxs-lookup"><span data-stu-id="2aa95-114">Defines a namespace for configuration sections.</span></span> |

## <a name="remarks"></a><span data-ttu-id="2aa95-115">备注</span><span class="sxs-lookup"><span data-stu-id="2aa95-115">Remarks</span></span>

<span data-ttu-id="2aa95-116">如果此元素在配置文件中，则它必须是元素的第一个子元素 **\<configuration>** 。</span><span class="sxs-lookup"><span data-stu-id="2aa95-116">If this element is in a configuration file, it must be the first child element of the **\<configuration>** element.</span></span>

## <a name="example"></a><span data-ttu-id="2aa95-117">示例</span><span class="sxs-lookup"><span data-stu-id="2aa95-117">Example</span></span>

<span data-ttu-id="2aa95-118">下面的示例演示如何定义配置节并定义该部分的设置：</span><span class="sxs-lookup"><span data-stu-id="2aa95-118">The following example shows how to define a configuration section and define settings for that section:</span></span>

```xml
<configuration>
  <configSections>
    <section name="sampleSection"
             type="System.Configuration.SingleTagSectionHandler" />
  </configSections>
  <sampleSection setting1="Value1"
                 setting2="value two"
                 setting3="third value" />
</configuration>
```

## <a name="configuration-file"></a><span data-ttu-id="2aa95-119">配置文件</span><span class="sxs-lookup"><span data-stu-id="2aa95-119">Configuration file</span></span>

<span data-ttu-id="2aa95-120">此元素可用于应用程序配置文件、计算机配置文件 (*Machine.config*) 和 *Web.config* 不在应用程序目录级别的文件。</span><span class="sxs-lookup"><span data-stu-id="2aa95-120">This element can be used in the application configuration file, machine configuration file (*Machine.config*), and *Web.config* files that are not at the application directory level.</span></span>

## <a name="see-also"></a><span data-ttu-id="2aa95-121">请参阅</span><span class="sxs-lookup"><span data-stu-id="2aa95-121">See also</span></span>

- [<span data-ttu-id="2aa95-122">.NET Framework 的配置文件架构</span><span class="sxs-lookup"><span data-stu-id="2aa95-122">Configuration file schema for the .NET Framework</span></span>](index.md)
