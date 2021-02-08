---
description: 详细了解： <appSettings> 的元素 <configuration>
title: <configuration> 的 <appSettings> 元素
ms.date: 05/01/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/appSettings
helpviewer_keywords:
- appSettings Element
- <appSettings> Element
ms.assetid: 39694cc4-6b84-45a6-9329-385a0d8b48fe
ms.openlocfilehash: 74a25bb0dffd97057cda45575745b6f51ad2a675
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99802484"
---
# <a name="appsettings-element-for-configuration"></a><span data-ttu-id="475e4-103">\<configuration> 的 \<appSettings> 元素</span><span class="sxs-lookup"><span data-stu-id="475e4-103">\<appSettings> element for \<configuration></span></span>

<span data-ttu-id="475e4-104">包含自定义应用程序设置。</span><span class="sxs-lookup"><span data-stu-id="475e4-104">Contains custom application settings.</span></span> <span data-ttu-id="475e4-105">这是 .NET Framework 提供的预定义的配置节。</span><span class="sxs-lookup"><span data-stu-id="475e4-105">This is a predefined configuration section provided by the .NET Framework.</span></span>

[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;**\<appSettings>**

## <a name="syntax"></a><span data-ttu-id="475e4-106">语法</span><span class="sxs-lookup"><span data-stu-id="475e4-106">Syntax</span></span>

```xml
<appSettings>
  <!-- Elements to add, clear, or remove configuration settings -->
</appSettings>
```

## <a name="attribute"></a><span data-ttu-id="475e4-107">Attribute</span><span class="sxs-lookup"><span data-stu-id="475e4-107">Attribute</span></span>

|           | <span data-ttu-id="475e4-108">说明</span><span class="sxs-lookup"><span data-stu-id="475e4-108">Description</span></span> |
| --------- | ----------- |
| <span data-ttu-id="475e4-109">文件</span><span class="sxs-lookup"><span data-stu-id="475e4-109">**file**</span></span>  | <span data-ttu-id="475e4-110">可选特性。</span><span class="sxs-lookup"><span data-stu-id="475e4-110">Optional attribute.</span></span><br><br><span data-ttu-id="475e4-111">指定包含自定义应用程序配置设置的外部文件的相对路径。</span><span class="sxs-lookup"><span data-stu-id="475e4-111">Specifies a relative path to an external file containing custom application configuration settings.</span></span> <span data-ttu-id="475e4-112">指定的文件包含在、和元素中指定的相同类型的设置， **\<add>** **\<remove>** **\<clear>** 并使用与这些元素相同的键/值对格式。</span><span class="sxs-lookup"><span data-stu-id="475e4-112">The specified file contains the same kind of settings that are specified in the **\<add>**, **\<remove>**, and **\<clear>** elements and uses the same key/value pair format as those elements.</span></span><br><br><span data-ttu-id="475e4-113">指定的路径相对于主配置文件。</span><span class="sxs-lookup"><span data-stu-id="475e4-113">The path specified is relative to the main configuration file.</span></span> <span data-ttu-id="475e4-114">对于 Windows 窗体应用程序，这是二进制文件夹 (例如 */bin/debug*) ，而不是应用程序配置文件的位置。</span><span class="sxs-lookup"><span data-stu-id="475e4-114">For a Windows Forms application, this is the binary folder (such as */bin/debug*), not the location of the application configuration file.</span></span> <span data-ttu-id="475e4-115">对于 Web 窗体应用程序，路径相对于应用程序根目录，其中 *web.config* 文件位于该位置。</span><span class="sxs-lookup"><span data-stu-id="475e4-115">For Web Forms applications, the path is relative to the application root, where the *web.config* file is located.</span></span><br><br><span data-ttu-id="475e4-116">如果找不到指定的文件，则运行时将忽略该特性。</span><span class="sxs-lookup"><span data-stu-id="475e4-116">The runtime ignores the attribute if the specified file can't be found.</span></span> |

## <a name="parent-element"></a><span data-ttu-id="475e4-117">父元素</span><span class="sxs-lookup"><span data-stu-id="475e4-117">Parent element</span></span>

|     | <span data-ttu-id="475e4-118">描述</span><span class="sxs-lookup"><span data-stu-id="475e4-118">Description</span></span> |
| --- | ----------- |
| [<span data-ttu-id="475e4-119">**\<configuration>** 元素</span><span class="sxs-lookup"><span data-stu-id="475e4-119">**\<configuration>** Element</span></span>](../configuration-element.md) | <span data-ttu-id="475e4-120">公共语言运行时和 .NET Framework 应用程序所使用的每个配置文件中的根元素。</span><span class="sxs-lookup"><span data-stu-id="475e4-120">The root element in every configuration file used by the common language runtime and .NET Framework applications.</span></span> |

## <a name="child-elements"></a><span data-ttu-id="475e4-121">子元素</span><span class="sxs-lookup"><span data-stu-id="475e4-121">Child elements</span></span>

|     | <span data-ttu-id="475e4-122">说明</span><span class="sxs-lookup"><span data-stu-id="475e4-122">Description</span></span> |
| --- | ----------- |
| [**\<add>**](add-element-for-appsettings.md) | <span data-ttu-id="475e4-123">添加自定义应用程序设置。</span><span class="sxs-lookup"><span data-stu-id="475e4-123">Adds a custom application setting.</span></span> |
| [**\<clear>**](clear-element-for-appsettings.md) | <span data-ttu-id="475e4-124">清除以前定义的所有应用程序设置。</span><span class="sxs-lookup"><span data-stu-id="475e4-124">Clears all previously defined application settings.</span></span> |
| [**\<remove>**](remove-element-for-appsettings.md) | <span data-ttu-id="475e4-125">删除以前定义的应用程序设置。</span><span class="sxs-lookup"><span data-stu-id="475e4-125">Removes a previously defined application setting.</span></span> |

## <a name="remarks"></a><span data-ttu-id="475e4-126">备注</span><span class="sxs-lookup"><span data-stu-id="475e4-126">Remarks</span></span>

<span data-ttu-id="475e4-127">**\<appSettings>** 元素存储自定义应用程序配置信息，例如数据库连接字符串、文件路径、XML Web service url，或应用程序的任何其他自定义配置信息。</span><span class="sxs-lookup"><span data-stu-id="475e4-127">The **\<appSettings>** element stores custom application configuration information, such as database connection strings, file paths, XML Web service URLs, or any other custom configuration information for an application.</span></span> <span data-ttu-id="475e4-128">**\<appSettings>** 使用类在代码中访问元素中指定的键/值对 <xref:System.Configuration.ConfigurationSettings> 。</span><span class="sxs-lookup"><span data-stu-id="475e4-128">The key/value pairs specified in the **\<appSettings>** element are accessed in code using the <xref:System.Configuration.ConfigurationSettings> class.</span></span>

<span data-ttu-id="475e4-129">您可以使用 **\<appSettings>** *Web.config* 和应用程序配置文件的元素中的文件属性。</span><span class="sxs-lookup"><span data-stu-id="475e4-129">You can use the **file** attribute in the **\<appSettings>** element of the *Web.config* and application configuration files.</span></span> <span data-ttu-id="475e4-130">此特性指定提供其他设置或重写在元素中指定的设置的配置文件 **\<appSettings>** 。</span><span class="sxs-lookup"><span data-stu-id="475e4-130">This attribute specifies a configuration file that provides additional settings or overrides the settings specified in the **\<appSettings>** element.</span></span> <span data-ttu-id="475e4-131">**文件** 属性可用于源代码管理团队开发方案，例如当用户想要重写应用程序配置文件中指定的项目设置时。</span><span class="sxs-lookup"><span data-stu-id="475e4-131">The **file** attribute can be used in source control team development scenarios, such as when a user wants to override the project settings specified in an application configuration file.</span></span>

<span data-ttu-id="475e4-132">**文件** 属性指定的配置文件的根节点必须 **\<appSettings>** 是而不是 **\<configuration>** 。</span><span class="sxs-lookup"><span data-stu-id="475e4-132">Configuration files specified by the **file** attribute must have a root node of **\<appSettings>** rather than **\<configuration>**.</span></span>

## <a name="example"></a><span data-ttu-id="475e4-133">示例</span><span class="sxs-lookup"><span data-stu-id="475e4-133">Example</span></span>

<span data-ttu-id="475e4-134">下面的示例演示外部应用程序设置文件 (custom.config)，该文件定义自定义应用程序设置：</span><span class="sxs-lookup"><span data-stu-id="475e4-134">The following example shows an external application settings file (*custom.config*) that defines a custom application setting:</span></span>

```xml
<?xml version="1.0" encoding="utf-8" ?>
<appSettings>
  <add key="MyCustomSetting" value="MyCustomSettingValue" />
</appSettings>
```

<span data-ttu-id="475e4-135">下面的示例演示使用外部设置文件中的设置并自行设置应用程序设置的应用程序配置文件：</span><span class="sxs-lookup"><span data-stu-id="475e4-135">The following example shows an application configuration file that consumes the setting in the external settings file and sets an application setting of its own:</span></span>

```xml
<configuration>
  <appSettings file="custom.config">
    <add key="ApplicationName" value="MyApplication" />
  </appSettings>
</configuration>
```

## <a name="configuration-file"></a><span data-ttu-id="475e4-136">配置文件</span><span class="sxs-lookup"><span data-stu-id="475e4-136">Configuration file</span></span>

<span data-ttu-id="475e4-137">此元素可用于应用程序配置文件、计算机配置文件 (*Machine.config*) 和 *Web.config* 不在应用程序目录级别的文件。</span><span class="sxs-lookup"><span data-stu-id="475e4-137">This element can be used in the application configuration file, machine configuration file (*Machine.config*), and *Web.config* files that are not at the application directory level.</span></span>

## <a name="see-also"></a><span data-ttu-id="475e4-138">请参阅</span><span class="sxs-lookup"><span data-stu-id="475e4-138">See also</span></span>

- [<span data-ttu-id="475e4-139">.NET Framework 的配置文件架构</span><span class="sxs-lookup"><span data-stu-id="475e4-139">Configuration file schema for the .NET Framework</span></span>](../index.md)
