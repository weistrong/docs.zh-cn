---
description: 了解详细信息： <add> NameValueSectionHandler 和 DictionarySectionHandler 的元素
title: <add> NameValueSectionHandler 和 DictionarySectionHandler 的元素
ms.date: 05/01/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/sectionName/add
helpviewer_keywords:
- add Element
- <add> Element
ms.assetid: 0d4ddb53-eb2b-49c0-9c33-a8dec5c39b46
ms.openlocfilehash: 5a8cf22b21370e60086408f792f8137386d07aa3
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99713047"
---
# <a name="add-element-for-namevaluesectionhandler-and-dictionarysectionhandler"></a><span data-ttu-id="bd60b-103">\<add> NameValueSectionHandler 和 DictionarySectionHandler 的元素</span><span class="sxs-lookup"><span data-stu-id="bd60b-103">\<add> element for NameValueSectionHandler and DictionarySectionHandler</span></span>

<span data-ttu-id="bd60b-104">添加自定义应用程序设置。</span><span class="sxs-lookup"><span data-stu-id="bd60b-104">Adds custom application settings.</span></span> <span data-ttu-id="bd60b-105">每个 **\<add>** 标记包含一个键/值对。</span><span class="sxs-lookup"><span data-stu-id="bd60b-105">Each **\<add>** tag contains a key/value pair.</span></span>

[**\<configuration>**](configuration-element.md)\
&nbsp;&nbsp;[**\<sectionName>**](custom-element-2.md)\
&nbsp;&nbsp;&nbsp;&nbsp;**\<add>**

## <a name="syntax"></a><span data-ttu-id="bd60b-106">语法</span><span class="sxs-lookup"><span data-stu-id="bd60b-106">Syntax</span></span>

```xml
<add key="key" value="value" />
```

## <a name="attributes"></a><span data-ttu-id="bd60b-107">特性</span><span class="sxs-lookup"><span data-stu-id="bd60b-107">Attributes</span></span>

| <span data-ttu-id="bd60b-108">属性</span><span class="sxs-lookup"><span data-stu-id="bd60b-108">Attribute</span></span> | <span data-ttu-id="bd60b-109">说明</span><span class="sxs-lookup"><span data-stu-id="bd60b-109">Description</span></span> |
| --------- | ----------- |
| <span data-ttu-id="bd60b-110">key </span><span class="sxs-lookup"><span data-stu-id="bd60b-110">**key**</span></span>   | <span data-ttu-id="bd60b-111">必需的特性。</span><span class="sxs-lookup"><span data-stu-id="bd60b-111">Required attribute.</span></span><br><br><span data-ttu-id="bd60b-112">指定设置的名称。</span><span class="sxs-lookup"><span data-stu-id="bd60b-112">Specifies the name of the setting.</span></span> |
| <span data-ttu-id="bd60b-113">**value**</span><span class="sxs-lookup"><span data-stu-id="bd60b-113">**value**</span></span> | <span data-ttu-id="bd60b-114">必需的特性。</span><span class="sxs-lookup"><span data-stu-id="bd60b-114">Required attribute.</span></span><br><br><span data-ttu-id="bd60b-115">指定设置的值。</span><span class="sxs-lookup"><span data-stu-id="bd60b-115">Specifies the value of the setting.</span></span> |

## <a name="parent-element"></a><span data-ttu-id="bd60b-116">父元素</span><span class="sxs-lookup"><span data-stu-id="bd60b-116">Parent element</span></span>

| <span data-ttu-id="bd60b-117">元素</span><span class="sxs-lookup"><span data-stu-id="bd60b-117">Element</span></span> | <span data-ttu-id="bd60b-118">说明</span><span class="sxs-lookup"><span data-stu-id="bd60b-118">Description</span></span> |
| ------- | ------------|
| [<span data-ttu-id="bd60b-119">**\<sectionName>** 元素</span><span class="sxs-lookup"><span data-stu-id="bd60b-119">**\<sectionName>** Element</span></span>](custom-element-2.md) | <span data-ttu-id="bd60b-120">定义使用和类的自定义配置节的设置 <xref:System.Configuration.NameValueSectionHandler> <xref:System.Configuration.DictionarySectionHandler> 。</span><span class="sxs-lookup"><span data-stu-id="bd60b-120">Defines settings for custom configuration sections that use the <xref:System.Configuration.NameValueSectionHandler> and <xref:System.Configuration.DictionarySectionHandler> classes.</span></span> |

## <a name="child-elements"></a><span data-ttu-id="bd60b-121">子元素</span><span class="sxs-lookup"><span data-stu-id="bd60b-121">Child elements</span></span>

<span data-ttu-id="bd60b-122">无</span><span class="sxs-lookup"><span data-stu-id="bd60b-122">None</span></span>

## <a name="example"></a><span data-ttu-id="bd60b-123">示例</span><span class="sxs-lookup"><span data-stu-id="bd60b-123">Example</span></span>

<span data-ttu-id="bd60b-124">下面的示例演示如何定义自定义配置节，并使用 **\<add>** 元素将设置放入部分：</span><span class="sxs-lookup"><span data-stu-id="bd60b-124">The following example shows how to define a custom configuration section and use the **\<add>** element to put settings into the section:</span></span>

```xml
<configuration>
  <configSections>
    <section name="dictionarySample" type="System.Configuration.DictionarySectionHandler,System" />
  </configSections>
  <dictionarySample>
    <add key="myKey" value="myValue" />
  </dictionarySample>
</configuration>
```

## <a name="configuration-file"></a><span data-ttu-id="bd60b-125">配置文件</span><span class="sxs-lookup"><span data-stu-id="bd60b-125">Configuration file</span></span>

<span data-ttu-id="bd60b-126">此元素可用于应用程序配置文件、计算机配置文件 (*Machine.config*) 和 *Web.config* 不在应用程序目录级别的文件。</span><span class="sxs-lookup"><span data-stu-id="bd60b-126">This element can be used in the application configuration file, machine configuration file (*Machine.config*), and *Web.config* files that are not at the application directory level.</span></span>

## <a name="see-also"></a><span data-ttu-id="bd60b-127">请参阅</span><span class="sxs-lookup"><span data-stu-id="bd60b-127">See also</span></span>

- [<span data-ttu-id="bd60b-128">.NET Framework 的配置文件架构</span><span class="sxs-lookup"><span data-stu-id="bd60b-128">Configuration file schema for the .NET Framework</span></span>](index.md)
