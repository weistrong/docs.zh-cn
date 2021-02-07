---
description: 了解详细信息： SingleTagSectionHandler 的自定义元素
title: SingleTagSectionHandler 的自定义元素
ms.date: 05/01/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/sectionName
helpviewer_keywords:
- custom element
ms.assetid: e62056c6-b351-40eb-afc0-cc13fc44e45e
ms.openlocfilehash: 83022a1ebf295b89d5f868589e3d9a77c78e3fab
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99729974"
---
# <a name="custom-element-for-singletagsectionhandler"></a><span data-ttu-id="abeaa-103">SingleTagSectionHandler 的自定义元素</span><span class="sxs-lookup"><span data-stu-id="abeaa-103">Custom element for SingleTagSectionHandler</span></span>

<span data-ttu-id="abeaa-104">定义自定义配置节中由 \<section> 元素定义并使用类的设置 <xref:System.Configuration.SingleTagSectionHandler> 。</span><span class="sxs-lookup"><span data-stu-id="abeaa-104">Defines settings in a custom configuration section that is defined by a \<section> element and uses the <xref:System.Configuration.SingleTagSectionHandler> class.</span></span>

<span data-ttu-id="abeaa-105">[**\<configuration>**](configuration-element.md) &nbsp;&nbsp;*\<sectionName>*</span><span class="sxs-lookup"><span data-stu-id="abeaa-105">[**\<configuration>**](configuration-element.md) &nbsp;&nbsp;*\<sectionName>*</span></span>

## <a name="syntax"></a><span data-ttu-id="abeaa-106">语法</span><span class="sxs-lookup"><span data-stu-id="abeaa-106">Syntax</span></span>

```xml
<sectionName key="value" key2="value2" />
```

## <a name="attributes"></a><span data-ttu-id="abeaa-107">特性</span><span class="sxs-lookup"><span data-stu-id="abeaa-107">Attributes</span></span>

<span data-ttu-id="abeaa-108">属性和属性值是用户定义的。</span><span class="sxs-lookup"><span data-stu-id="abeaa-108">Attributes and attribute values are user defined.</span></span>

## <a name="parent-element"></a><span data-ttu-id="abeaa-109">父元素</span><span class="sxs-lookup"><span data-stu-id="abeaa-109">Parent element</span></span>

|     | <span data-ttu-id="abeaa-110">描述</span><span class="sxs-lookup"><span data-stu-id="abeaa-110">Description</span></span> |
| --- | ----------- |
| [**\<configuration>**](configuration-element.md) | <span data-ttu-id="abeaa-111">公共语言运行时和 .NET Framework 应用程序所使用的每个配置文件中的根元素。</span><span class="sxs-lookup"><span data-stu-id="abeaa-111">The root element in every configuration file used by the common language runtime and .NET Framework applications.</span></span> |

## <a name="child-elements"></a><span data-ttu-id="abeaa-112">子元素</span><span class="sxs-lookup"><span data-stu-id="abeaa-112">Child elements</span></span>

<span data-ttu-id="abeaa-113">无</span><span class="sxs-lookup"><span data-stu-id="abeaa-113">None</span></span>

## <a name="remarks"></a><span data-ttu-id="abeaa-114">备注</span><span class="sxs-lookup"><span data-stu-id="abeaa-114">Remarks</span></span>

<span data-ttu-id="abeaa-115">**\<sectionName>** 元素是由元素中的标记定义的自定义元素 [**\<section>**](section-element.md) [**\<configSections>**](configsections-element-for-configuration.md) 。</span><span class="sxs-lookup"><span data-stu-id="abeaa-115">The **\<sectionName>** element is a custom element defined by a [**\<section>**](section-element.md) tag in the [**\<configSections>**](configsections-element-for-configuration.md) element.</span></span> <span data-ttu-id="abeaa-116">调用时，配置系统返回 <xref:System.Collections.IDictionary> 对象 <xref:System.Configuration.Configuration.GetSection(System.String)?displayProperty=nameWithType> 。</span><span class="sxs-lookup"><span data-stu-id="abeaa-116">The configuration system returns a <xref:System.Collections.IDictionary> object when you call <xref:System.Configuration.Configuration.GetSection(System.String)?displayProperty=nameWithType>.</span></span>

## <a name="example"></a><span data-ttu-id="abeaa-117">示例</span><span class="sxs-lookup"><span data-stu-id="abeaa-117">Example</span></span>

<span data-ttu-id="abeaa-118">下面的示例声明一个名为的自定义元素 **\<sampleSection>** ，该元素包含由类读取的设置 <xref:System.Configuration.SingleTagSectionHandler> ：</span><span class="sxs-lookup"><span data-stu-id="abeaa-118">The following example declares a custom element called **\<sampleSection>** that contains settings read by the <xref:System.Configuration.SingleTagSectionHandler> class:</span></span>

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

## <a name="configuration-file"></a><span data-ttu-id="abeaa-119">配置文件</span><span class="sxs-lookup"><span data-stu-id="abeaa-119">Configuration file</span></span>

<span data-ttu-id="abeaa-120">此元素可用于应用程序配置文件、计算机配置文件 (*Machine.config*) 和 *Web.config* 不在应用程序目录级别的文件。</span><span class="sxs-lookup"><span data-stu-id="abeaa-120">This element can be used in the application configuration file, the machine configuration file (*Machine.config*), and *Web.config* files that aren't at the application directory level.</span></span>

## <a name="see-also"></a><span data-ttu-id="abeaa-121">请参阅</span><span class="sxs-lookup"><span data-stu-id="abeaa-121">See also</span></span>

- [<span data-ttu-id="abeaa-122">.NET Framework 的配置文件架构</span><span class="sxs-lookup"><span data-stu-id="abeaa-122">Configuration file schema for the .NET Framework</span></span>](index.md)
