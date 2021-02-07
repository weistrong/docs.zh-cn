---
description: 了解详细信息：应用设置架构
title: 应用设置架构
ms.date: 05/01/2017
helpviewer_keywords:
- schema app settings
- app settings, schema [Windows Forms]
- Windows Forms, app settings schema
- configuration schema [.NET Framework], app settings
ms.assetid: 99347d62-3ea5-40b6-bfec-c31431011422
ms.openlocfilehash: a98a60b0470e0fa2c03313f25de9b310f5fce785
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99699345"
---
# <a name="app-settings-schema"></a><span data-ttu-id="ee6c1-103">应用设置架构</span><span class="sxs-lookup"><span data-stu-id="ee6c1-103">App Settings schema</span></span>

<span data-ttu-id="ee6c1-104">包含自定义应用程序设置，如文件路径、XML Web service URL 或应用程序的任何其他自定义配置信息。</span><span class="sxs-lookup"><span data-stu-id="ee6c1-104">Contains custom application settings, such as file paths, XML Web service URLs, or any other custom configuration information for an application.</span></span>

[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<appSettings>**](appsettings-element-for-configuration.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<add>**](add-element-for-appsettings.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<clear>**](clear-element-for-appsettings.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<remove>**](remove-element-for-appsettings.md)

| <span data-ttu-id="ee6c1-105">元素</span><span class="sxs-lookup"><span data-stu-id="ee6c1-105">Element</span></span> | <span data-ttu-id="ee6c1-106">说明</span><span class="sxs-lookup"><span data-stu-id="ee6c1-106">Description</span></span> |
| ------- | ----------- |
| [**\<appSettings>**](appsettings-element-for-configuration.md) | <span data-ttu-id="ee6c1-107">包含 **\<add>** 、 **\<clear>** 和 **\<remove>** 标记以控制应用程序设置。</span><span class="sxs-lookup"><span data-stu-id="ee6c1-107">Contains **\<add>**, **\<clear>**, and **\<remove>** tags to control application settings.</span></span> <span data-ttu-id="ee6c1-108">具有可选的“file”属性。</span><span class="sxs-lookup"><span data-stu-id="ee6c1-108">Has an optional **file** attribute.</span></span> |
| [**\<add>**](add-element-for-appsettings.md) | <span data-ttu-id="ee6c1-109">定义设置。</span><span class="sxs-lookup"><span data-stu-id="ee6c1-109">Defines a setting.</span></span> <span data-ttu-id="ee6c1-110">的子项 **\<appSettings>** 。</span><span class="sxs-lookup"><span data-stu-id="ee6c1-110">Child of **\<appSettings>**.</span></span> <span data-ttu-id="ee6c1-111">需要“key”和“value”属性。</span><span class="sxs-lookup"><span data-stu-id="ee6c1-111">Requires **key** and **value** attributes.</span></span> |
| [**\<clear>**](clear-element-for-appsettings.md) | <span data-ttu-id="ee6c1-112">清除所有设置。</span><span class="sxs-lookup"><span data-stu-id="ee6c1-112">Clears all settings.</span></span> <span data-ttu-id="ee6c1-113">的子项 **\<appSettings>** 。</span><span class="sxs-lookup"><span data-stu-id="ee6c1-113">Child of **\<appSettings>**.</span></span> <span data-ttu-id="ee6c1-114">不具有属性。</span><span class="sxs-lookup"><span data-stu-id="ee6c1-114">Has no attributes.</span></span> |
| [**\<remove>**](remove-element-for-appsettings.md) | <span data-ttu-id="ee6c1-115">删除设置。</span><span class="sxs-lookup"><span data-stu-id="ee6c1-115">Removes a setting.</span></span> <span data-ttu-id="ee6c1-116">的子项 **\<appSettings>** 。</span><span class="sxs-lookup"><span data-stu-id="ee6c1-116">Child of **\<appSettings>**.</span></span> <span data-ttu-id="ee6c1-117">需要“key”属性。</span><span class="sxs-lookup"><span data-stu-id="ee6c1-117">Requires a **key** attribute.</span></span> |

## <a name="appsettings-element"></a><span data-ttu-id="ee6c1-118">\<appSettings> 元素</span><span class="sxs-lookup"><span data-stu-id="ee6c1-118">\<appSettings> element</span></span>

<span data-ttu-id="ee6c1-119">此元素包含 **\<add>** 、 **\<clear>** 和 **\<remove>** 标记以控制应用程序设置。</span><span class="sxs-lookup"><span data-stu-id="ee6c1-119">This element contains **\<add>**, **\<clear>**, and **\<remove>** tags to control application settings.</span></span> <span data-ttu-id="ee6c1-120">它定义“file”的一个可选属性。</span><span class="sxs-lookup"><span data-stu-id="ee6c1-120">It defines an optional attribute for **file**.</span></span>

## <a name="add-element"></a><span data-ttu-id="ee6c1-121">\<add> 元素</span><span class="sxs-lookup"><span data-stu-id="ee6c1-121">\<add> element</span></span>

<span data-ttu-id="ee6c1-122">将自定义应用程序设置作为名称/值对添加到应用程序设置集合。</span><span class="sxs-lookup"><span data-stu-id="ee6c1-122">Adds a custom application setting as a name/value pair to the application settings collection.</span></span> <span data-ttu-id="ee6c1-123">它定义“key”和“value”的属性。</span><span class="sxs-lookup"><span data-stu-id="ee6c1-123">It defines attributes for **key** and **value**.</span></span>

## <a name="clear-element"></a><span data-ttu-id="ee6c1-124">\<clear> 元素</span><span class="sxs-lookup"><span data-stu-id="ee6c1-124">\<clear> element</span></span>

<span data-ttu-id="ee6c1-125">删除所有对继承的自定义应用程序设置的引用，并仅允许元素后面由元素添加的引用 **\<add>** **\<clear>** 。</span><span class="sxs-lookup"><span data-stu-id="ee6c1-125">Removes all references to inherited custom application settings and allows only the references that are added by **\<add>** elements following the **\<clear>** element.</span></span> <span data-ttu-id="ee6c1-126">未定义任何属性。</span><span class="sxs-lookup"><span data-stu-id="ee6c1-126">It defines no attributes.</span></span>

## <a name="remove-element"></a><span data-ttu-id="ee6c1-127">\<remove> 元素</span><span class="sxs-lookup"><span data-stu-id="ee6c1-127">\<remove> element</span></span>

<span data-ttu-id="ee6c1-128">删除对应用程序设置集合中继承的自定义应用程序设置的引用。</span><span class="sxs-lookup"><span data-stu-id="ee6c1-128">Removes a reference to an inherited custom application setting from the application settings collection.</span></span> <span data-ttu-id="ee6c1-129">定义“key”的属性。</span><span class="sxs-lookup"><span data-stu-id="ee6c1-129">It defines an attribute for **key**.</span></span>

## <a name="example"></a><span data-ttu-id="ee6c1-130">示例</span><span class="sxs-lookup"><span data-stu-id="ee6c1-130">Example</span></span>

<span data-ttu-id="ee6c1-131">下面的示例演示外部应用程序设置文件 (custom.config)，该文件定义自定义应用程序设置：</span><span class="sxs-lookup"><span data-stu-id="ee6c1-131">The following example shows an external application settings file (*custom.config*) that defines a custom application setting:</span></span>

```xml
<?xml version="1.0" encoding="utf-8" ?>
<appSettings>
  <add key="MyCustomSetting" value="MyCustomSettingValue" />
</appSettings>
```

<span data-ttu-id="ee6c1-132">下面的示例演示使用外部设置文件中的设置并自行设置应用程序设置的应用程序配置文件：</span><span class="sxs-lookup"><span data-stu-id="ee6c1-132">The following example shows an application configuration file that consumes the setting in the external settings file and sets an application setting of its own:</span></span>

```xml
<configuration>
  <appSettings file="custom.config">
    <add key="ApplicationName" value="MyApplication" />
  </appSettings>
</configuration>
```

## <a name="see-also"></a><span data-ttu-id="ee6c1-133">请参阅</span><span class="sxs-lookup"><span data-stu-id="ee6c1-133">See also</span></span>

- [<span data-ttu-id="ee6c1-134">应用程序设置概述</span><span class="sxs-lookup"><span data-stu-id="ee6c1-134">Application Settings Overview</span></span>](/dotnet/desktop/winforms/advanced/application-settings-overview)
- [<span data-ttu-id="ee6c1-135">应用程序设置体系结构</span><span class="sxs-lookup"><span data-stu-id="ee6c1-135">Application Settings Architecture</span></span>](/dotnet/desktop/winforms/advanced/application-settings-architecture)
