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
# <a name="custom-element-for-namevaluesectionhandler-and-dictionarysectionhandler"></a><span data-ttu-id="f60e2-103">NameValueSectionHandler 和 DictionarySectionHandler 的自定义元素</span><span class="sxs-lookup"><span data-stu-id="f60e2-103">Custom element for NameValueSectionHandler and DictionarySectionHandler</span></span>

<span data-ttu-id="f60e2-104">定义使用和类的自定义配置节的设置 <xref:System.Configuration.NameValueSectionHandler> <xref:System.Configuration.DictionarySectionHandler> 。</span><span class="sxs-lookup"><span data-stu-id="f60e2-104">Defines settings for custom configuration sections that use the <xref:System.Configuration.NameValueSectionHandler> and <xref:System.Configuration.DictionarySectionHandler> classes.</span></span>

[**\<configuration>**](configuration-element.md)\
&nbsp;&nbsp;**\<sectionName>**

## <a name="attributes"></a><span data-ttu-id="f60e2-105">特性</span><span class="sxs-lookup"><span data-stu-id="f60e2-105">Attributes</span></span>

<span data-ttu-id="f60e2-106">无</span><span class="sxs-lookup"><span data-stu-id="f60e2-106">None</span></span>

## <a name="parent-element"></a><span data-ttu-id="f60e2-107">父元素</span><span class="sxs-lookup"><span data-stu-id="f60e2-107">Parent element</span></span>

|     | <span data-ttu-id="f60e2-108">描述</span><span class="sxs-lookup"><span data-stu-id="f60e2-108">Description</span></span> |
| --- | ----------- |
| [**\<configuration>**](configuration-element.md) | <span data-ttu-id="f60e2-109">公共语言运行时和 .NET Framework 应用程序所使用的每个配置文件中的根元素。</span><span class="sxs-lookup"><span data-stu-id="f60e2-109">The root element in every configuration file used by the common language runtime and .NET Framework applications.</span></span> |

## <a name="child-elements"></a><span data-ttu-id="f60e2-110">子元素</span><span class="sxs-lookup"><span data-stu-id="f60e2-110">Child elements</span></span>

|     | <span data-ttu-id="f60e2-111">说明</span><span class="sxs-lookup"><span data-stu-id="f60e2-111">Description</span></span> |
| --- | ----------- |
| <span data-ttu-id="f60e2-112">[**\<add>**](add-element-for-custom-2.md) 对于 <xref:System.Configuration.NameValueSectionHandler> 和 <xref:System.Configuration.DictionarySectionHandler></span><span class="sxs-lookup"><span data-stu-id="f60e2-112">[**\<add>**](add-element-for-custom-2.md) for <xref:System.Configuration.NameValueSectionHandler> and <xref:System.Configuration.DictionarySectionHandler></span></span>  | <span data-ttu-id="f60e2-113">添加自定义应用程序设置。</span><span class="sxs-lookup"><span data-stu-id="f60e2-113">Adds custom application settings.</span></span> |
| <span data-ttu-id="f60e2-114">[**\<remove>**](remove-element-for-custom-2.md) 对于 <xref:System.Configuration.NameValueSectionHandler> 和 <xref:System.Configuration.DictionarySectionHandler></span><span class="sxs-lookup"><span data-stu-id="f60e2-114">[**\<remove>**](remove-element-for-custom-2.md) for <xref:System.Configuration.NameValueSectionHandler> and <xref:System.Configuration.DictionarySectionHandler></span></span> | <span data-ttu-id="f60e2-115">删除以前定义的设置。</span><span class="sxs-lookup"><span data-stu-id="f60e2-115">Removes a previously defined setting.</span></span> |
| <span data-ttu-id="f60e2-116">[**\<clear>**](clear-element-for-custom-2.md) 对于 <xref:System.Configuration.NameValueSectionHandler> 和 <xref:System.Configuration.DictionarySectionHandler></span><span class="sxs-lookup"><span data-stu-id="f60e2-116">[**\<clear>**](clear-element-for-custom-2.md) for <xref:System.Configuration.NameValueSectionHandler> and <xref:System.Configuration.DictionarySectionHandler></span></span> | <span data-ttu-id="f60e2-117">清除节中所有先前定义的设置。</span><span class="sxs-lookup"><span data-stu-id="f60e2-117">Clears all previously defined settings in a section.</span></span> |

## <a name="remarks"></a><span data-ttu-id="f60e2-118">备注</span><span class="sxs-lookup"><span data-stu-id="f60e2-118">Remarks</span></span>

<span data-ttu-id="f60e2-119">**\<sectionName>** 元素是由元素中的标记定义的自定义元素 **\<section>** **\<configSections>** 。</span><span class="sxs-lookup"><span data-stu-id="f60e2-119">The **\<sectionName>** element is a custom element defined by a **\<section>** tag in the **\<configSections>** element.</span></span>

<span data-ttu-id="f60e2-120">下表显示 ConfigurationSettings. GetConfig 方法为每个配置节处理程序返回的对象类型：</span><span class="sxs-lookup"><span data-stu-id="f60e2-120">The following table shows the type of object the ConfigurationSettings.GetConfig method returns for each configuration section handler:</span></span>

| <span data-ttu-id="f60e2-121">配置节处理程序</span><span class="sxs-lookup"><span data-stu-id="f60e2-121">Configuration section handler</span></span>                        | <span data-ttu-id="f60e2-122">返回类型</span><span class="sxs-lookup"><span data-stu-id="f60e2-122">Return type</span></span>                                                |
| ---------------------------------------------------- | ---------------------------------------------------------- |
| <xref:System.Configuration.NameValueSectionHandler>  | <xref:System.Collections.Specialized.NameValueCollection>  |
| <xref:System.Configuration.DictionarySectionHandler> | <xref:System.Collections.IDictionary>                      |

## <a name="example"></a><span data-ttu-id="f60e2-123">示例</span><span class="sxs-lookup"><span data-stu-id="f60e2-123">Example</span></span>

<span data-ttu-id="f60e2-124">下面的示例演示如何声明使用和类的节 <xref:System.Configuration.DictionarySectionHandler> <xref:System.Configuration.NameValueSectionHandler> 。</span><span class="sxs-lookup"><span data-stu-id="f60e2-124">The following example shows how to declare sections that use the <xref:System.Configuration.DictionarySectionHandler> and <xref:System.Configuration.NameValueSectionHandler> classes.</span></span>

<span data-ttu-id="f60e2-125">第一个自定义元素为 **\<dictionarySample>** ，其中包含由 <xref:System.Configuration.DictionarySectionHandler> 程序集中的类读取的设置 `System.dll` 。</span><span class="sxs-lookup"><span data-stu-id="f60e2-125">The first custom element is **\<dictionarySample>**, which contains settings read by the <xref:System.Configuration.DictionarySectionHandler> class in the `System.dll` assembly.</span></span> <span data-ttu-id="f60e2-126">第二个自定义元素为 **\<mySection>** ，其中包含由 <xref:System.Configuration.NameValueSectionHandler> 程序集中的类读取的设置 `System.dll` 。</span><span class="sxs-lookup"><span data-stu-id="f60e2-126">The second custom element is **\<mySection>**, which contains settings read by the <xref:System.Configuration.NameValueSectionHandler> class in the `System.dll` assembly.</span></span>

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

## <a name="configuration-file"></a><span data-ttu-id="f60e2-127">配置文件</span><span class="sxs-lookup"><span data-stu-id="f60e2-127">Configuration file</span></span>

<span data-ttu-id="f60e2-128">此元素可用于应用程序配置文件、计算机配置文件 (*Machine.config*) 和 *Web.config* 不在应用程序目录级别的文件。</span><span class="sxs-lookup"><span data-stu-id="f60e2-128">This element can be used in the application configuration file, machine configuration file (*Machine.config*), and *Web.config* files that are not at the application directory level.</span></span>

## <a name="see-also"></a><span data-ttu-id="f60e2-129">请参阅</span><span class="sxs-lookup"><span data-stu-id="f60e2-129">See also</span></span>

- [<span data-ttu-id="f60e2-130">.NET Framework 的配置文件架构</span><span class="sxs-lookup"><span data-stu-id="f60e2-130">Configuration file schema for the .NET Framework</span></span>](index.md)
