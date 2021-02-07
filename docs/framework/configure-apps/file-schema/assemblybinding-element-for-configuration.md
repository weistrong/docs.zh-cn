---
description: 详细了解： <assemblyBinding> 的元素 <configuration>
title: <configuration> 的 <assemblyBinding> 元素
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/assemblyBinding
helpviewer_keywords:
- assemblyBinding Element
- <assemblyBinding> Element
ms.assetid: 6cc55983-b894-449b-8e26-b258e53939cd
ms.openlocfilehash: 5cc3fc7cccd4b9dc7b62815734ff76e32e2243d3
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99730104"
---
# <a name="assemblybinding-element-for-configuration"></a><span data-ttu-id="5f0ff-103">\<configuration> 的 \<assemblyBinding> 元素</span><span class="sxs-lookup"><span data-stu-id="5f0ff-103">\<assemblyBinding> element for \<configuration></span></span>

<span data-ttu-id="5f0ff-104">指定配置级的程序集绑定策略。</span><span class="sxs-lookup"><span data-stu-id="5f0ff-104">Specifies assembly binding policy at the configuration level.</span></span>

<span data-ttu-id="5f0ff-105">[**\<configuration>**](configuration-element.md) &nbsp;&nbsp;**\<assemblyBinding>**</span><span class="sxs-lookup"><span data-stu-id="5f0ff-105">[**\<configuration>**](configuration-element.md) &nbsp;&nbsp;**\<assemblyBinding>**</span></span>

## <a name="syntax"></a><span data-ttu-id="5f0ff-106">语法</span><span class="sxs-lookup"><span data-stu-id="5f0ff-106">Syntax</span></span>

```xml
<assemblyBinding xmlns="urn:schemas-microsoft-com:asm.v1">
  <!-- Configuration files to include. -->
</assemblyBinding>
```

## <a name="attribute"></a><span data-ttu-id="5f0ff-107">Attribute</span><span class="sxs-lookup"><span data-stu-id="5f0ff-107">Attribute</span></span>

|           | <span data-ttu-id="5f0ff-108">说明</span><span class="sxs-lookup"><span data-stu-id="5f0ff-108">Description</span></span> |
| --------- | ----------- |
| <span data-ttu-id="5f0ff-109">**xmlns**</span><span class="sxs-lookup"><span data-stu-id="5f0ff-109">**xmlns**</span></span> | <span data-ttu-id="5f0ff-110">必需的特性。</span><span class="sxs-lookup"><span data-stu-id="5f0ff-110">Required attribute.</span></span><br><br><span data-ttu-id="5f0ff-111">指定程序集绑定所需的 XML 命名空间。</span><span class="sxs-lookup"><span data-stu-id="5f0ff-111">Specifies the XML namespace required for assembly binding.</span></span> <span data-ttu-id="5f0ff-112">使用字符串“urn: 架构-microsoft-com:asm.v1”作为值。</span><span class="sxs-lookup"><span data-stu-id="5f0ff-112">Use the string "urn:schemas-microsoft-com:asm.v1" as the value.</span></span> |

## <a name="parent-element"></a><span data-ttu-id="5f0ff-113">父元素</span><span class="sxs-lookup"><span data-stu-id="5f0ff-113">Parent element</span></span>

|     | <span data-ttu-id="5f0ff-114">描述</span><span class="sxs-lookup"><span data-stu-id="5f0ff-114">Description</span></span> |
| --- | ----------- |
| [**\<configuration>**](configuration-element.md) | <span data-ttu-id="5f0ff-115">公共语言运行时和 .NET Framework 应用程序所使用的每个配置文件中的根元素。</span><span class="sxs-lookup"><span data-stu-id="5f0ff-115">The root element in every configuration file used by the common language runtime and .NET Framework applications.</span></span> |

## <a name="child-element"></a><span data-ttu-id="5f0ff-116">子元素</span><span class="sxs-lookup"><span data-stu-id="5f0ff-116">Child element</span></span>

|     | <span data-ttu-id="5f0ff-117">描述</span><span class="sxs-lookup"><span data-stu-id="5f0ff-117">Description</span></span> |
| --- | ----------- |
| [**\<linkedConfiguration>**](linkedconfiguration-element.md) | <span data-ttu-id="5f0ff-118">指定要包含的配置文件。</span><span class="sxs-lookup"><span data-stu-id="5f0ff-118">Specifies a configuration file to include.</span></span> |

## <a name="remarks"></a><span data-ttu-id="5f0ff-119">备注</span><span class="sxs-lookup"><span data-stu-id="5f0ff-119">Remarks</span></span>

<span data-ttu-id="5f0ff-120">[**\<linkedConfiguration>**](linkedconfiguration-element.md)元素通过允许应用程序配置文件在众所周知的位置包含程序集配置文件，而不是复制程序集配置设置，从而简化了组件程序集的管理。</span><span class="sxs-lookup"><span data-stu-id="5f0ff-120">The [**\<linkedConfiguration>**](linkedconfiguration-element.md) element simplifies the management of component assemblies by allowing application configuration files to include assembly configuration files in well-known locations, rather than duplicating assembly configuration settings.</span></span>

> [!NOTE]
> <span data-ttu-id="5f0ff-121">**\<linkedConfiguration>** 具有 Windows 并行清单的应用程序不支持该元素。</span><span class="sxs-lookup"><span data-stu-id="5f0ff-121">The **\<linkedConfiguration>** element is not supported for applications with Windows side-by-side manifests.</span></span>

## <a name="example"></a><span data-ttu-id="5f0ff-122">示例</span><span class="sxs-lookup"><span data-stu-id="5f0ff-122">Example</span></span>

<span data-ttu-id="5f0ff-123">下面的示例演示如何在本地硬盘上包含配置文件：</span><span class="sxs-lookup"><span data-stu-id="5f0ff-123">The following example shows how to include a configuration file on the local hard disk:</span></span>

```xml
<configuration>
  <assemblyBinding xmlns="urn:schemas-microsoft-com:asm.v1">
    <linkedConfiguration href="file://c:\Program Files\Contoso\sharedConfig.xml" />
  </assemblyBinding>
</configuration>
```

## <a name="see-also"></a><span data-ttu-id="5f0ff-124">请参阅</span><span class="sxs-lookup"><span data-stu-id="5f0ff-124">See also</span></span>

- [<span data-ttu-id="5f0ff-125">.NET Framework 的配置文件架构</span><span class="sxs-lookup"><span data-stu-id="5f0ff-125">Configuration file schema for the .NET Framework</span></span>](index.md)
