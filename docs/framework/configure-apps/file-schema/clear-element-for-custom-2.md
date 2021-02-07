---
description: 了解详细信息： <clear> NameValueSectionHandler 和 DictionarySectionHandler 的元素
title: <clear> NameValueSectionHandler 和 DictionarySectionHandler 的元素
ms.date: 05/01/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/sectionName/clear
helpviewer_keywords:
- clear Element
- <clear> Element
ms.assetid: ff2294ec-fb82-4b0c-933e-ae185433fc7b
ms.openlocfilehash: 896aa7e8f0e3b41574538fcd9e4be9d6155da889
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99699228"
---
# <a name="clear-element-for-namevaluesectionhandler-and-dictionarysectionhandler"></a><span data-ttu-id="fccd4-103">\<clear> NameValueSectionHandler 和 DictionarySectionHandler 的元素</span><span class="sxs-lookup"><span data-stu-id="fccd4-103">\<clear> element for NameValueSectionHandler and DictionarySectionHandler</span></span>

<span data-ttu-id="fccd4-104">清除节中所有先前定义的设置。</span><span class="sxs-lookup"><span data-stu-id="fccd4-104">Clears all previously defined settings in a section.</span></span>

[**\<configuration>**](configuration-element.md)\
&nbsp;&nbsp;[**\<sectionName>**](custom-element-2.md)\
&nbsp;&nbsp;&nbsp;&nbsp;**\<clear>**

## <a name="syntax"></a><span data-ttu-id="fccd4-105">语法</span><span class="sxs-lookup"><span data-stu-id="fccd4-105">Syntax</span></span>

```xml
<clear />
```

## <a name="attributes"></a><span data-ttu-id="fccd4-106">特性</span><span class="sxs-lookup"><span data-stu-id="fccd4-106">Attributes</span></span>

<span data-ttu-id="fccd4-107">无</span><span class="sxs-lookup"><span data-stu-id="fccd4-107">None</span></span>

## <a name="parent-element"></a><span data-ttu-id="fccd4-108">父元素</span><span class="sxs-lookup"><span data-stu-id="fccd4-108">Parent element</span></span>

|     | <span data-ttu-id="fccd4-109">描述</span><span class="sxs-lookup"><span data-stu-id="fccd4-109">Description</span></span> |
| --- | ------------|
| [<span data-ttu-id="fccd4-110">**\<sectionName>** 元素</span><span class="sxs-lookup"><span data-stu-id="fccd4-110">**\<sectionName>** Element</span></span>](custom-element-2.md) | <span data-ttu-id="fccd4-111">定义使用和类的自定义配置节的设置 <xref:System.Configuration.NameValueSectionHandler> <xref:System.Configuration.DictionarySectionHandler> 。</span><span class="sxs-lookup"><span data-stu-id="fccd4-111">Defines settings for custom configuration sections that use the <xref:System.Configuration.NameValueSectionHandler> and <xref:System.Configuration.DictionarySectionHandler> classes.</span></span> |

## <a name="child-elements"></a><span data-ttu-id="fccd4-112">子元素</span><span class="sxs-lookup"><span data-stu-id="fccd4-112">Child elements</span></span>

<span data-ttu-id="fccd4-113">无</span><span class="sxs-lookup"><span data-stu-id="fccd4-113">None</span></span>

## <a name="remarks"></a><span data-ttu-id="fccd4-114">备注</span><span class="sxs-lookup"><span data-stu-id="fccd4-114">Remarks</span></span>

<span data-ttu-id="fccd4-115">你可以使用 **\<clear>** 元素从你的应用程序中删除在配置文件层次结构中较高级别上定义的所有设置。</span><span class="sxs-lookup"><span data-stu-id="fccd4-115">You can use the **\<clear>** element to remove all settings from your application that were defined at a higher level in the configuration file hierarchy.</span></span>

## <a name="example"></a><span data-ttu-id="fccd4-116">示例</span><span class="sxs-lookup"><span data-stu-id="fccd4-116">Example</span></span>

<span data-ttu-id="fccd4-117">此示例定义了计算机配置文件和应用程序配置文件，并演示了如何使用 **\<clear>** 应用程序配置文件中的元素清除之前在计算机配置文件中定义的部分。</span><span class="sxs-lookup"><span data-stu-id="fccd4-117">This example defines a machine configuration file and an application configuration file and shows how to use the **\<clear>** element in an application configuration file to clear sections previously defined in the machine configuration file.</span></span>

<span data-ttu-id="fccd4-118">以下计算机配置文件代码声明了节 **\<mySection>** ：</span><span class="sxs-lookup"><span data-stu-id="fccd4-118">The following machine configuration file code declares the section **\<mySection>**:</span></span>

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

<span data-ttu-id="fccd4-119">以下应用程序配置文件代码将从中删除所有设置 **\<mySection>** 。</span><span class="sxs-lookup"><span data-stu-id="fccd4-119">The following application configuration file code removes all settings from **\<mySection>**.</span></span> <span data-ttu-id="fccd4-120">应用程序无法检索在计算机配置文件的部分中的中声明的任何设置 **\<mySection>** 。</span><span class="sxs-lookup"><span data-stu-id="fccd4-120">The application cannot retrieve any of the settings that were declared in the in the **\<mySection>** section of the machine configuration file.</span></span>

```xml
<!-- Application configuration file -->
<configuration>
  <mySection>
    <clear/>
  </mySection>
</configuration>
```

## <a name="configuration-file"></a><span data-ttu-id="fccd4-121">配置文件</span><span class="sxs-lookup"><span data-stu-id="fccd4-121">Configuration file</span></span>

<span data-ttu-id="fccd4-122">此元素可用于应用程序配置文件、计算机配置文件 (*Machine.config*) 和 *Web.config* 不在应用程序目录级别的文件。</span><span class="sxs-lookup"><span data-stu-id="fccd4-122">This element can be used in the application configuration file, machine configuration file (*Machine.config*), and *Web.config* files that are not at the application directory level.</span></span>

## <a name="see-also"></a><span data-ttu-id="fccd4-123">请参阅</span><span class="sxs-lookup"><span data-stu-id="fccd4-123">See also</span></span>

- [<span data-ttu-id="fccd4-124">.NET Framework 的配置文件架构</span><span class="sxs-lookup"><span data-stu-id="fccd4-124">Configuration file schema for the .NET Framework</span></span>](index.md)
