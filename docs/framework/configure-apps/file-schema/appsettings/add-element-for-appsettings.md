---
description: 详细了解： <add> 的元素 <appSettings>
title: <appSettings> 的 <add> 元素
ms.date: 05/01/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/appSettings/add
helpviewer_keywords:
- add Element
- <add> Element
ms.assetid: 8734efdc-00f6-4a65-bba6-084c5bc65246
ms.openlocfilehash: f10ffe517b3b25543bc7baed0c7d2af13f48ab02
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99652882"
---
# <a name="add-element-for-appsettings"></a><span data-ttu-id="89676-103">\<appSettings> 的 \<add> 元素</span><span class="sxs-lookup"><span data-stu-id="89676-103">\<add> element for \<appSettings></span></span>

<span data-ttu-id="89676-104">添加自定义应用程序设置。</span><span class="sxs-lookup"><span data-stu-id="89676-104">Adds a custom application setting.</span></span>

[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<appSettings>**](appsettings-element-for-configuration.md)\
&nbsp;&nbsp;&nbsp;&nbsp;**\<add>**

## <a name="syntax"></a><span data-ttu-id="89676-105">语法</span><span class="sxs-lookup"><span data-stu-id="89676-105">Syntax</span></span>

```xml
<appSettings>
  <add key="Key of custom setting" value="Value of custom setting" />
</appSettings>
```

## <a name="attributes"></a><span data-ttu-id="89676-106">特性</span><span class="sxs-lookup"><span data-stu-id="89676-106">Attributes</span></span>

|           | <span data-ttu-id="89676-107">说明</span><span class="sxs-lookup"><span data-stu-id="89676-107">Description</span></span> |
| --------- | ----------- |
| <span data-ttu-id="89676-108">key </span><span class="sxs-lookup"><span data-stu-id="89676-108">**key**</span></span>   | <span data-ttu-id="89676-109">必需的特性。</span><span class="sxs-lookup"><span data-stu-id="89676-109">Required attribute.</span></span><br><br><span data-ttu-id="89676-110">指定要添加的密钥的名称。</span><span class="sxs-lookup"><span data-stu-id="89676-110">Specifies the name of the key to add.</span></span> |
| <span data-ttu-id="89676-111">**value**</span><span class="sxs-lookup"><span data-stu-id="89676-111">**value**</span></span> | <span data-ttu-id="89676-112">必需的特性。</span><span class="sxs-lookup"><span data-stu-id="89676-112">Required attribute.</span></span><br><br><span data-ttu-id="89676-113">指定要添加的键的值。</span><span class="sxs-lookup"><span data-stu-id="89676-113">Specifies the value of the key to add.</span></span> |

## <a name="parent-element"></a><span data-ttu-id="89676-114">父元素</span><span class="sxs-lookup"><span data-stu-id="89676-114">Parent element</span></span>

|     | <span data-ttu-id="89676-115">描述</span><span class="sxs-lookup"><span data-stu-id="89676-115">Description</span></span> |
| --- | ----------- |
| [**\<appSettings>**](appsettings-element-for-configuration.md) | <span data-ttu-id="89676-116">包含自定义应用程序设置，如文件路径、XML Web service URL 或应用程序的任何其他自定义配置信息。</span><span class="sxs-lookup"><span data-stu-id="89676-116">Contains custom application settings, such as file paths, XML Web service URLs, or any other custom configuration information for an application.</span></span> |

## <a name="child-elements"></a><span data-ttu-id="89676-117">子元素</span><span class="sxs-lookup"><span data-stu-id="89676-117">Child elements</span></span>

<span data-ttu-id="89676-118">无</span><span class="sxs-lookup"><span data-stu-id="89676-118">None</span></span>

## <a name="example"></a><span data-ttu-id="89676-119">示例</span><span class="sxs-lookup"><span data-stu-id="89676-119">Example</span></span>

<span data-ttu-id="89676-120">下面的示例演示如何为应用程序名称添加自定义配置设置：</span><span class="sxs-lookup"><span data-stu-id="89676-120">The following example shows how to add a custom configuration setting for the application's name:</span></span>

```xml
<appSettings>
  <add key="ApplicationName" value="MyApplication" />
</appSettings>
```

<span data-ttu-id="89676-121">下面的示例使用 `<add>` 元素定义 ASP.NET 应用程序中的两个兼容性设置：</span><span class="sxs-lookup"><span data-stu-id="89676-121">The following example uses the `<add>` element to define two compatibility settings in an ASP.NET application:</span></span>

```xml
<appSettings>
  <add key="AppContext.SetSwitch:Switch.System.Globalization.NoAsyncCurrentCulture" value="true" />
  <add key="AppContext.SetSwitch:Switch.System.Uri.DontEnableStrictRFC3986ReservedCharacterSets" value="true" />
</appSettings>
```

## <a name="see-also"></a><span data-ttu-id="89676-122">请参阅</span><span class="sxs-lookup"><span data-stu-id="89676-122">See also</span></span>

- [<span data-ttu-id="89676-123">.NET Framework 的配置文件架构</span><span class="sxs-lookup"><span data-stu-id="89676-123">Configuration file schema for the .NET Framework</span></span>](../index.md)
