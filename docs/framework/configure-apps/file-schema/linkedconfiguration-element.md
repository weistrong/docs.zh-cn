---
description: 了解详细信息： <linkedConfiguration> 元素
title: <linkedConfiguration> 元素
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/assemblyBinding/linkedConfiguration
- http://schemas.microsoft.com/.NetConfiguration/v2.0#linkedConfiguration
helpviewer_keywords:
- configuration files [.NET Framework],linked configuration files
- <linkedConfiguration> element
- including configuration files
- linked configuration files
- linkedConfiguration Element
ms.assetid: 8eb34f3b-427e-4288-a7ff-c73f489deb45
ms.openlocfilehash: e4312cf788784241efc35304b632dfe1fdef1bc4
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99698656"
---
# <a name="linkedconfiguration-element"></a><span data-ttu-id="5ff7e-103">\<linkedConfiguration> 元素</span><span class="sxs-lookup"><span data-stu-id="5ff7e-103">\<linkedConfiguration> element</span></span>

<span data-ttu-id="5ff7e-104">指定要包含的配置文件。</span><span class="sxs-lookup"><span data-stu-id="5ff7e-104">Specifies a configuration file to include.</span></span>

[**\<configuration>**](configuration-element.md)\
&nbsp;&nbsp;[**\<assemblyBinding>**](assemblybinding-element-for-configuration.md)\
&nbsp;&nbsp;&nbsp;&nbsp;**\<linkedConfiguration>**

## <a name="syntax"></a><span data-ttu-id="5ff7e-105">语法</span><span class="sxs-lookup"><span data-stu-id="5ff7e-105">Syntax</span></span>

```xml
<linkedConfiguration href="URL of linked configuration file" />
```

## <a name="attribute"></a><span data-ttu-id="5ff7e-106">Attribute</span><span class="sxs-lookup"><span data-stu-id="5ff7e-106">Attribute</span></span>

|           | <span data-ttu-id="5ff7e-107">说明</span><span class="sxs-lookup"><span data-stu-id="5ff7e-107">Description</span></span> |
| --------- | ----------- |
| <span data-ttu-id="5ff7e-108">**href**</span><span class="sxs-lookup"><span data-stu-id="5ff7e-108">**href**</span></span>  | <span data-ttu-id="5ff7e-109">必需的特性。</span><span class="sxs-lookup"><span data-stu-id="5ff7e-109">Required attribute.</span></span><br><br><span data-ttu-id="5ff7e-110">要包含的配置文件的 URL。</span><span class="sxs-lookup"><span data-stu-id="5ff7e-110">The URL of the configuration file to include.</span></span> <span data-ttu-id="5ff7e-111">**Href** 特性支持的唯一格式为 `file://` 。</span><span class="sxs-lookup"><span data-stu-id="5ff7e-111">The only format supported for the **href** attribute is `file://`.</span></span> <span data-ttu-id="5ff7e-112">支持本地文件和 UNC 文件。</span><span class="sxs-lookup"><span data-stu-id="5ff7e-112">Local files and UNC files are supported.</span></span> |

## <a name="parent-element"></a><span data-ttu-id="5ff7e-113">父元素</span><span class="sxs-lookup"><span data-stu-id="5ff7e-113">Parent element</span></span>

|     | <span data-ttu-id="5ff7e-114">描述</span><span class="sxs-lookup"><span data-stu-id="5ff7e-114">Description</span></span> |
| --- | ----------- |
| [<span data-ttu-id="5ff7e-115">**\<assemblyBinding>** 元素</span><span class="sxs-lookup"><span data-stu-id="5ff7e-115">**\<assemblyBinding>** Element</span></span>](assemblybinding-element-for-configuration.md) | <span data-ttu-id="5ff7e-116">指定配置级的程序集绑定策略。</span><span class="sxs-lookup"><span data-stu-id="5ff7e-116">Specifies assembly binding policy at the configuration level.</span></span> |

## <a name="child-elements"></a><span data-ttu-id="5ff7e-117">子元素</span><span class="sxs-lookup"><span data-stu-id="5ff7e-117">Child elements</span></span>

<span data-ttu-id="5ff7e-118">无</span><span class="sxs-lookup"><span data-stu-id="5ff7e-118">None</span></span>

## <a name="remarks"></a><span data-ttu-id="5ff7e-119">备注</span><span class="sxs-lookup"><span data-stu-id="5ff7e-119">Remarks</span></span>

<span data-ttu-id="5ff7e-120">**\<linkedConfiguration>** 元素简化了组件程序集的服务。</span><span class="sxs-lookup"><span data-stu-id="5ff7e-120">The **\<linkedConfiguration>** element simplifies servicing for component assemblies.</span></span> <span data-ttu-id="5ff7e-121">如果一个或多个应用程序使用的程序集具有驻留在众所周知位置的配置文件，则使用该程序集的应用程序的配置文件可以使用 **\<linkedConfiguration>** 元素来包含程序集配置文件，而不是直接包含配置信息。</span><span class="sxs-lookup"><span data-stu-id="5ff7e-121">If one or more applications use an assembly that has a configuration file residing in a well-known location, the configuration files of the applications that use the assembly can use the **\<linkedConfiguration>** element to include the assembly configuration file, rather than including configuration information directly.</span></span> <span data-ttu-id="5ff7e-122">处理组件程序集时，更新公共配置文件会为使用该程序集的所有应用程序提供更新的配置信息。</span><span class="sxs-lookup"><span data-stu-id="5ff7e-122">When the component assembly is serviced, updating the common configuration file provides updated configuration information to all applications that use the assembly.</span></span>

> [!NOTE]
> <span data-ttu-id="5ff7e-123">**\<linkedConfiguration>** 具有 Windows 并行清单的应用程序不支持该元素。</span><span class="sxs-lookup"><span data-stu-id="5ff7e-123">The **\<linkedConfiguration>** element is not supported for applications with Windows side-by-side manifests.</span></span>

<span data-ttu-id="5ff7e-124">以下规则控制链接配置文件的使用：</span><span class="sxs-lookup"><span data-stu-id="5ff7e-124">The following rules govern the use of linked configuration files:</span></span>

- <span data-ttu-id="5ff7e-125">包含的配置文件中的设置只会影响加载程序绑定策略并仅由加载程序使用。</span><span class="sxs-lookup"><span data-stu-id="5ff7e-125">The settings in included configuration files only affect loader binding policy and are used only by the loader.</span></span> <span data-ttu-id="5ff7e-126">包含的配置文件可以包含绑定策略以外的设置，但这些设置不会产生任何影响。</span><span class="sxs-lookup"><span data-stu-id="5ff7e-126">The included configuration files can have settings other than binding policies, but those settings don't have any effect.</span></span>

- <span data-ttu-id="5ff7e-127">特性支持的唯一格式 `href` 为 `file://` 。</span><span class="sxs-lookup"><span data-stu-id="5ff7e-127">The only format supported for the `href` attribute is `file://`.</span></span> <span data-ttu-id="5ff7e-128">支持本地文件和 UNC 文件。</span><span class="sxs-lookup"><span data-stu-id="5ff7e-128">Local files and UNC files are supported.</span></span>

- <span data-ttu-id="5ff7e-129">每个配置文件的链接配置数没有限制。</span><span class="sxs-lookup"><span data-stu-id="5ff7e-129">There is no constraint on the number of linked configurations per configuration file.</span></span>

- <span data-ttu-id="5ff7e-130">所有链接的配置文件合并到一个文件中，这与 `#include` c/c + + 中指令的行为类似。</span><span class="sxs-lookup"><span data-stu-id="5ff7e-130">All linked configuration files are merged to form one file, similar to the behavior of the `#include` directive in C/C++.</span></span>

- <span data-ttu-id="5ff7e-131">**\<linkedConfiguration>** 仅允许在应用程序配置文件中使用元素; 它在 *Machine.config* 中将被忽略。</span><span class="sxs-lookup"><span data-stu-id="5ff7e-131">The **\<linkedConfiguration>** element is allowed only in application configuration files; it's ignored in *Machine.config*.</span></span>

- <span data-ttu-id="5ff7e-132">检测和终止循环引用。</span><span class="sxs-lookup"><span data-stu-id="5ff7e-132">Circular references are detected and terminated.</span></span> <span data-ttu-id="5ff7e-133">也就是说，如果 **\<linkedConfiguration>** 一系列配置文件的元素形成循环，则检测并停止循环。</span><span class="sxs-lookup"><span data-stu-id="5ff7e-133">That is, if the **\<linkedConfiguration>** elements of a series of configuration files form a loop, the loop is detected and stopped.</span></span>

## <a name="example"></a><span data-ttu-id="5ff7e-134">示例</span><span class="sxs-lookup"><span data-stu-id="5ff7e-134">Example</span></span>

<span data-ttu-id="5ff7e-135">下面的示例演示如何包括本地硬盘中的配置文件：</span><span class="sxs-lookup"><span data-stu-id="5ff7e-135">The following example shows how to include configuration file from the local hard disk:</span></span>

```xml
<configuration>
  <assemblyBinding xmlns="urn:schemas-microsoft-com:asm.v1">
    <linkedConfiguration href="file://c:\Program Files\Contoso\sharedConfig.xml"/>
  </assemblyBinding>
</configuration>
```

## <a name="see-also"></a><span data-ttu-id="5ff7e-136">请参阅</span><span class="sxs-lookup"><span data-stu-id="5ff7e-136">See also</span></span>

- [<span data-ttu-id="5ff7e-137">**\<assemblyBinding>** 元素</span><span class="sxs-lookup"><span data-stu-id="5ff7e-137">**\<assemblyBinding>** Element</span></span>](assemblybinding-element-for-configuration.md)
- [<span data-ttu-id="5ff7e-138">.NET Framework 的配置文件架构</span><span class="sxs-lookup"><span data-stu-id="5ff7e-138">Configuration file schema for the .NET Framework</span></span>](index.md)
