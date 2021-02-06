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
# <a name="sectiongroup-element-for-configsections"></a><span data-ttu-id="b69db-103">\<configSections> 的 \<sectionGroup> 元素</span><span class="sxs-lookup"><span data-stu-id="b69db-103">\<sectionGroup> element for \<configSections></span></span>

<span data-ttu-id="b69db-104">定义配置节的命名空间。</span><span class="sxs-lookup"><span data-stu-id="b69db-104">Defines a namespace for configuration sections.</span></span>

[**\<configuration>**](configuration-element.md)\
&nbsp;&nbsp;[**\<configSections>**](configsections-element-for-configuration.md)\
&nbsp;&nbsp;&nbsp;&nbsp;**\<sectionGroup>**

## <a name="syntax"></a><span data-ttu-id="b69db-105">语法</span><span class="sxs-lookup"><span data-stu-id="b69db-105">Syntax</span></span>

```xml
<sectionGroup name="section group name">
  <!-- Configuration sections -->
</sectionGroup>
```

## <a name="attribute"></a><span data-ttu-id="b69db-106">Attribute</span><span class="sxs-lookup"><span data-stu-id="b69db-106">Attribute</span></span>

|           | <span data-ttu-id="b69db-107">说明</span><span class="sxs-lookup"><span data-stu-id="b69db-107">Description</span></span> |
| --------- | ----------- |
| <span data-ttu-id="b69db-108">**name**</span><span class="sxs-lookup"><span data-stu-id="b69db-108">**name**</span></span>  | <span data-ttu-id="b69db-109">必需的特性。</span><span class="sxs-lookup"><span data-stu-id="b69db-109">Required attribute.</span></span><br><br><span data-ttu-id="b69db-110">指定正在定义的节组的名称。</span><span class="sxs-lookup"><span data-stu-id="b69db-110">Specifies the name of the section group you are defining.</span></span> |

## <a name="parent-element"></a><span data-ttu-id="b69db-111">父元素</span><span class="sxs-lookup"><span data-stu-id="b69db-111">Parent element</span></span>

|     | <span data-ttu-id="b69db-112">描述</span><span class="sxs-lookup"><span data-stu-id="b69db-112">Description</span></span> |
| --- | ----------- |
| [<span data-ttu-id="b69db-113">**\<configSections>** 元素</span><span class="sxs-lookup"><span data-stu-id="b69db-113">**\<configSections>** Element</span></span>](configsections-element-for-configuration.md) | <span data-ttu-id="b69db-114">包含配置节和命名空间声明。</span><span class="sxs-lookup"><span data-stu-id="b69db-114">Contains configuration section and namespace declarations.</span></span> |

## <a name="child-elements"></a><span data-ttu-id="b69db-115">子元素</span><span class="sxs-lookup"><span data-stu-id="b69db-115">Child elements</span></span>

|     | <span data-ttu-id="b69db-116">说明</span><span class="sxs-lookup"><span data-stu-id="b69db-116">Description</span></span> |
| --- | ----------- |
| [**\<section>**](section-element.md) | <span data-ttu-id="b69db-117">包含配置节声明。</span><span class="sxs-lookup"><span data-stu-id="b69db-117">Contains a configuration section declaration.</span></span> |

## <a name="remarks"></a><span data-ttu-id="b69db-118">备注</span><span class="sxs-lookup"><span data-stu-id="b69db-118">Remarks</span></span>

<span data-ttu-id="b69db-119">声明节组将为配置节创建容器标记，并确保与其他人定义的配置节之间没有命名冲突。</span><span class="sxs-lookup"><span data-stu-id="b69db-119">Declaring a section group creates a container tag for configuration sections and ensures that there are no naming conflicts with configuration sections defined by someone else.</span></span> <span data-ttu-id="b69db-120">可以在彼此 **\<sectionGroup>** 之间嵌套元素。</span><span class="sxs-lookup"><span data-stu-id="b69db-120">You can nest **\<sectionGroup>** elements within each other.</span></span>

## <a name="example"></a><span data-ttu-id="b69db-121">示例</span><span class="sxs-lookup"><span data-stu-id="b69db-121">Example</span></span>

<span data-ttu-id="b69db-122">下面的示例演示如何声明一个节组，并在节组中声明部分：</span><span class="sxs-lookup"><span data-stu-id="b69db-122">The following example shows how to declare a section group and declare sections within a section group:</span></span>

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

## <a name="configuration-file"></a><span data-ttu-id="b69db-123">配置文件</span><span class="sxs-lookup"><span data-stu-id="b69db-123">Configuration file</span></span>

<span data-ttu-id="b69db-124">此元素可用于应用程序配置文件、计算机配置文件 (*Machine.config*) 和 *Web.config* 不在应用程序目录级别的文件。</span><span class="sxs-lookup"><span data-stu-id="b69db-124">This element can be used in the application configuration file, machine configuration file (*Machine.config*), and *Web.config* files that are not at the application directory level.</span></span>

## <a name="see-also"></a><span data-ttu-id="b69db-125">请参阅</span><span class="sxs-lookup"><span data-stu-id="b69db-125">See also</span></span>

- [<span data-ttu-id="b69db-126">.NET Framework 的配置文件架构</span><span class="sxs-lookup"><span data-stu-id="b69db-126">Configuration file schema for the .NET Framework</span></span>](index.md)
