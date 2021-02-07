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
# <a name="remove-element-for-namevaluesectionhandler-and-dictionarysectionhandler"></a><span data-ttu-id="297b3-103">\<remove> NameValueSectionHandler 和 DictionarySectionHandler 的元素</span><span class="sxs-lookup"><span data-stu-id="297b3-103">\<remove> element for NameValueSectionHandler and DictionarySectionHandler</span></span>

<span data-ttu-id="297b3-104">删除以前定义的设置。</span><span class="sxs-lookup"><span data-stu-id="297b3-104">Removes a previously defined setting.</span></span>

[**\<configuration>**](configuration-element.md)\
&nbsp;&nbsp;[**\<sectionName>**](custom-element-2.md)\
&nbsp;&nbsp;&nbsp;&nbsp;**\<remove>**

## <a name="syntax"></a><span data-ttu-id="297b3-105">语法</span><span class="sxs-lookup"><span data-stu-id="297b3-105">Syntax</span></span>

```xml
<add remove="key" />
```

## <a name="attribute"></a><span data-ttu-id="297b3-106">Attribute</span><span class="sxs-lookup"><span data-stu-id="297b3-106">Attribute</span></span>

|           | <span data-ttu-id="297b3-107">说明</span><span class="sxs-lookup"><span data-stu-id="297b3-107">Description</span></span> |
| --------- | ----------- |
| <span data-ttu-id="297b3-108">key </span><span class="sxs-lookup"><span data-stu-id="297b3-108">**key**</span></span>   | <span data-ttu-id="297b3-109">必需的特性。</span><span class="sxs-lookup"><span data-stu-id="297b3-109">Required attribute.</span></span><br><br><span data-ttu-id="297b3-110">指定要删除的设置的名称。</span><span class="sxs-lookup"><span data-stu-id="297b3-110">Specifies the name of the setting to remove.</span></span> |

## <a name="parent-element"></a><span data-ttu-id="297b3-111">父元素</span><span class="sxs-lookup"><span data-stu-id="297b3-111">Parent element</span></span>

| <span data-ttu-id="297b3-112">元素</span><span class="sxs-lookup"><span data-stu-id="297b3-112">Element</span></span> | <span data-ttu-id="297b3-113">说明</span><span class="sxs-lookup"><span data-stu-id="297b3-113">Description</span></span> |
| ------- | ------------|
| [<span data-ttu-id="297b3-114">**\<sectionName>** 元素</span><span class="sxs-lookup"><span data-stu-id="297b3-114">**\<sectionName>** Element</span></span>](custom-element-2.md) | <span data-ttu-id="297b3-115">定义使用和类的自定义配置节的设置 <xref:System.Configuration.NameValueSectionHandler> <xref:System.Configuration.DictionarySectionHandler> 。</span><span class="sxs-lookup"><span data-stu-id="297b3-115">Defines settings for custom configuration sections that use the <xref:System.Configuration.NameValueSectionHandler> and <xref:System.Configuration.DictionarySectionHandler> classes.</span></span> |

## <a name="child-elements"></a><span data-ttu-id="297b3-116">子元素</span><span class="sxs-lookup"><span data-stu-id="297b3-116">Child elements</span></span>

<span data-ttu-id="297b3-117">无</span><span class="sxs-lookup"><span data-stu-id="297b3-117">None</span></span>

## <a name="remarks"></a><span data-ttu-id="297b3-118">备注</span><span class="sxs-lookup"><span data-stu-id="297b3-118">Remarks</span></span>

<span data-ttu-id="297b3-119">你可以使用 **\<remove>** 元素从你的应用程序中删除在配置文件层次结构中较高级别上定义的设置。</span><span class="sxs-lookup"><span data-stu-id="297b3-119">You can use the **\<remove>** element to remove settings from your application that were defined at a higher level in the configuration file hierarchy.</span></span>

## <a name="example"></a><span data-ttu-id="297b3-120">示例</span><span class="sxs-lookup"><span data-stu-id="297b3-120">Example</span></span>

<span data-ttu-id="297b3-121">下面的示例演示如何使用 **\<remove>** 应用程序配置文件中的元素删除以前在计算机配置文件中定义的设置。</span><span class="sxs-lookup"><span data-stu-id="297b3-121">The following example shows how to use the **\<remove>** element in an application configuration file to remove settings previously defined in the machine configuration file.</span></span>

<span data-ttu-id="297b3-122">以下计算机配置文件代码声明节， **\<mySection>** 并向其中添加两个 `key1` 设置 `key2` ：</span><span class="sxs-lookup"><span data-stu-id="297b3-122">The following machine configuration file code declares the section **\<mySection>** and adds two settings, `key1` and `key2`, to it:</span></span>

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

<span data-ttu-id="297b3-123">以下应用程序配置文件代码将删除以下 `key2` 设置 **\<mySection>** ：</span><span class="sxs-lookup"><span data-stu-id="297b3-123">The following application configuration file code removes the `key2` setting from **\<mySection>**:</span></span>

```xml
<!--Application configuration file -->
<configuration>
  <mySection>
    <remove key="key2" />
  </mySection>
</configuration>
```

## <a name="configuration-file"></a><span data-ttu-id="297b3-124">配置文件</span><span class="sxs-lookup"><span data-stu-id="297b3-124">Configuration file</span></span>

<span data-ttu-id="297b3-125">此元素可用于应用程序配置文件、计算机配置文件 (*Machine.config*) 和 *Web.config* 不在应用程序目录级别的文件。</span><span class="sxs-lookup"><span data-stu-id="297b3-125">This element can be used in the application configuration file, machine configuration file (*Machine.config*), and *Web.config* files that are not at the application directory level.</span></span>

## <a name="see-also"></a><span data-ttu-id="297b3-126">请参阅</span><span class="sxs-lookup"><span data-stu-id="297b3-126">See also</span></span>

- [<span data-ttu-id="297b3-127">.NET Framework 的配置文件架构</span><span class="sxs-lookup"><span data-stu-id="297b3-127">Configuration file schema for the .NET Framework</span></span>](index.md)
