---
description: 详细了解： <remove> 的元素 <appSettings>
title: <appSettings> 的 <remove> 元素
ms.date: 05/01/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/appSettings/remove
helpviewer_keywords:
- remove Element
- <remove> Element
ms.assetid: 218c4464-e007-4539-803f-7c8b0a909fd8
ms.openlocfilehash: a67003d310377ee4b896843003306201353dae91
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99699267"
---
# <a name="remove-element-for-appsettings"></a><span data-ttu-id="87de8-103">\<appSettings> 的 \<remove> 元素</span><span class="sxs-lookup"><span data-stu-id="87de8-103">\<remove> element for \<appSettings></span></span>

<span data-ttu-id="87de8-104">删除自定义应用程序设置。</span><span class="sxs-lookup"><span data-stu-id="87de8-104">Removes custom application settings.</span></span>

[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<appSettings>**](appsettings-element-for-configuration.md)\
&nbsp;&nbsp;&nbsp;&nbsp;**\<remove>**

## <a name="syntax"></a><span data-ttu-id="87de8-105">语法</span><span class="sxs-lookup"><span data-stu-id="87de8-105">Syntax</span></span>

```xml
<appSettings>
  <remove key="Key of custom setting" />
</appSettings>
```

### <a name="attribute"></a><span data-ttu-id="87de8-106">Attribute</span><span class="sxs-lookup"><span data-stu-id="87de8-106">Attribute</span></span>

|         | <span data-ttu-id="87de8-107">说明</span><span class="sxs-lookup"><span data-stu-id="87de8-107">Description</span></span> |
| ------- | ----------- |
| <span data-ttu-id="87de8-108">key </span><span class="sxs-lookup"><span data-stu-id="87de8-108">**key**</span></span> | <span data-ttu-id="87de8-109">必需的特性。</span><span class="sxs-lookup"><span data-stu-id="87de8-109">Required attribute.</span></span><br><br><span data-ttu-id="87de8-110">指定要删除的密钥的名称。</span><span class="sxs-lookup"><span data-stu-id="87de8-110">Specifies the name of the key to remove.</span></span> |

### <a name="parent-element"></a><span data-ttu-id="87de8-111">父元素</span><span class="sxs-lookup"><span data-stu-id="87de8-111">Parent element</span></span>

|     | <span data-ttu-id="87de8-112">描述</span><span class="sxs-lookup"><span data-stu-id="87de8-112">Description</span></span> |
| --- | ----------- |
| [**\<appSettings>**](appsettings-element-for-configuration.md) | <span data-ttu-id="87de8-113">包含自定义应用程序设置，如文件路径、XML Web service URL 或应用程序的任何其他自定义配置信息。</span><span class="sxs-lookup"><span data-stu-id="87de8-113">Contains custom application settings, such as file paths, XML Web service URLs, or any other custom configuration information for an application.</span></span> |

## <a name="child-elements"></a><span data-ttu-id="87de8-114">子元素</span><span class="sxs-lookup"><span data-stu-id="87de8-114">Child elements</span></span>

<span data-ttu-id="87de8-115">无</span><span class="sxs-lookup"><span data-stu-id="87de8-115">None</span></span>

## <a name="example"></a><span data-ttu-id="87de8-116">示例</span><span class="sxs-lookup"><span data-stu-id="87de8-116">Example</span></span>

<span data-ttu-id="87de8-117">下面的示例演示如何删除的自定义配置设置 `ApplicationName` ：</span><span class="sxs-lookup"><span data-stu-id="87de8-117">The following example shows how to remove a custom configuration setting for `ApplicationName`:</span></span>

```xml
<appSettings>
  <remove key="ApplicationName" />
</appSettings>
```

## <a name="see-also"></a><span data-ttu-id="87de8-118">请参阅</span><span class="sxs-lookup"><span data-stu-id="87de8-118">See also</span></span>

- [<span data-ttu-id="87de8-119">.NET Framework 的配置文件架构</span><span class="sxs-lookup"><span data-stu-id="87de8-119">Configuration file schema for the .NET Framework</span></span>](../index.md)
