---
description: 详细了解： <clear> 的元素 <appSettings>
title: <appSettings> 的 <clear> 元素
ms.date: 05/01/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/appSettings/clear
helpviewer_keywords:
- clear Element
- <clear> Element
ms.assetid: 6d18c7be-27db-438b-8fb5-765d396b0b7b
ms.openlocfilehash: 88c6a02441c038619cb74947c024de7712189915
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99699332"
---
# <a name="clear-element-for-appsettings"></a><span data-ttu-id="3e7af-103">\<appSettings> 的 \<clear> 元素</span><span class="sxs-lookup"><span data-stu-id="3e7af-103">\<clear> element for \<appSettings></span></span>

<span data-ttu-id="3e7af-104">清除自定义应用程序设置。</span><span class="sxs-lookup"><span data-stu-id="3e7af-104">Clears custom application settings.</span></span>

[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<appSettings>**](appsettings-element-for-configuration.md)\
&nbsp;&nbsp;&nbsp;&nbsp;**\<clear>**

## <a name="syntax"></a><span data-ttu-id="3e7af-105">语法</span><span class="sxs-lookup"><span data-stu-id="3e7af-105">Syntax</span></span>

```xml
<appSettings>
  <clear />
</appSettings>
```

## <a name="attributes"></a><span data-ttu-id="3e7af-106">特性</span><span class="sxs-lookup"><span data-stu-id="3e7af-106">Attributes</span></span>

<span data-ttu-id="3e7af-107">无</span><span class="sxs-lookup"><span data-stu-id="3e7af-107">None</span></span>

## <a name="parent-element"></a><span data-ttu-id="3e7af-108">父元素</span><span class="sxs-lookup"><span data-stu-id="3e7af-108">Parent element</span></span>

|     | <span data-ttu-id="3e7af-109">描述</span><span class="sxs-lookup"><span data-stu-id="3e7af-109">Description</span></span> |
| --- | ----------- |
| [**\<appSettings>**](appsettings-element-for-configuration.md) | <span data-ttu-id="3e7af-110">包含自定义应用程序设置，如文件路径、XML Web service Url 或任何其他自定义应用程序配置信息。</span><span class="sxs-lookup"><span data-stu-id="3e7af-110">Contains custom application settings, such as file paths, XML Web service URLs, or any other custom application configuration information.</span></span> |

## <a name="child-elements"></a><span data-ttu-id="3e7af-111">子元素</span><span class="sxs-lookup"><span data-stu-id="3e7af-111">Child elements</span></span>

<span data-ttu-id="3e7af-112">无</span><span class="sxs-lookup"><span data-stu-id="3e7af-112">None</span></span>

## <a name="example"></a><span data-ttu-id="3e7af-113">示例</span><span class="sxs-lookup"><span data-stu-id="3e7af-113">Example</span></span>

<span data-ttu-id="3e7af-114">下面的示例演示如何清除自定义配置设置：</span><span class="sxs-lookup"><span data-stu-id="3e7af-114">The following example shows how to clear custom configuration settings:</span></span>

```xml
<appSettings>
  <clear />
</appSettings>
```

## <a name="see-also"></a><span data-ttu-id="3e7af-115">请参阅</span><span class="sxs-lookup"><span data-stu-id="3e7af-115">See also</span></span>

- [<span data-ttu-id="3e7af-116">.NET Framework 的配置文件架构</span><span class="sxs-lookup"><span data-stu-id="3e7af-116">Configuration file schema for the .NET Framework</span></span>](../index.md)
