---
description: 了解详细信息： <configuration> 元素
title: <configuration> 元素
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration
helpviewer_keywords:
- <configuration> element
- configuration element
- container tags, <configuration> element
ms.assetid: 2ec1c9dc-2e5c-4ef0-9958-81670ab88449
ms.openlocfilehash: ee48a45ddb987201e84213a0d7674da004951ab1
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99698990"
---
# <a name="configuration-element"></a><span data-ttu-id="13d84-103">\<configuration> 元素</span><span class="sxs-lookup"><span data-stu-id="13d84-103">\<configuration> element</span></span>

<span data-ttu-id="13d84-104">公共语言运行时和 .NET Framework 应用程序所使用的每个配置文件中的根元素。</span><span class="sxs-lookup"><span data-stu-id="13d84-104">The root element in every configuration file used by the common language runtime and .NET Framework applications.</span></span>

**\<configuration>**

## <a name="syntax"></a><span data-ttu-id="13d84-105">语法</span><span class="sxs-lookup"><span data-stu-id="13d84-105">Syntax</span></span>

```xml
<configuration>
  <!-- Configuration settings -->
</configuration>
```

## <a name="attributes"></a><span data-ttu-id="13d84-106">特性</span><span class="sxs-lookup"><span data-stu-id="13d84-106">Attributes</span></span>

<span data-ttu-id="13d84-107">无</span><span class="sxs-lookup"><span data-stu-id="13d84-107">None</span></span>

## <a name="parent-element"></a><span data-ttu-id="13d84-108">父元素</span><span class="sxs-lookup"><span data-stu-id="13d84-108">Parent element</span></span>

<span data-ttu-id="13d84-109">无</span><span class="sxs-lookup"><span data-stu-id="13d84-109">None</span></span>

## <a name="child-elements"></a><span data-ttu-id="13d84-110">子元素</span><span class="sxs-lookup"><span data-stu-id="13d84-110">Child elements</span></span>

|     | <span data-ttu-id="13d84-111">说明</span><span class="sxs-lookup"><span data-stu-id="13d84-111">Description</span></span> |
| --- | ----------- |
| [**\<assemblyBinding>**](assemblybinding-element-for-configuration.md) | <span data-ttu-id="13d84-112">指定配置级的程序集绑定策略。</span><span class="sxs-lookup"><span data-stu-id="13d84-112">Specifies assembly binding policy at the configuration level.</span></span>|
| [<span data-ttu-id="13d84-113">**\<startup>** 设置架构</span><span class="sxs-lookup"><span data-stu-id="13d84-113">**\<startup>** Settings Schema</span></span>](./startup/index.md) | <span data-ttu-id="13d84-114">启动设置架构中的所有元素。</span><span class="sxs-lookup"><span data-stu-id="13d84-114">All elements in the startup settings schema.</span></span> |
| [<span data-ttu-id="13d84-115">**\<runtime>** 设置架构</span><span class="sxs-lookup"><span data-stu-id="13d84-115">**\<runtime>** Settings Schema</span></span>](./runtime/index.md) | <span data-ttu-id="13d84-116">运行时设置架构中的所有元素。</span><span class="sxs-lookup"><span data-stu-id="13d84-116">All elements in the runtime settings schema.</span></span> |
| <span data-ttu-id="13d84-117">[**\<system.runtime.remoting>** 设置架构](/previous-versions/dotnet/netframework-4.0/z415cf9a(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="13d84-117">[**\<system.runtime.remoting>** Settings Schema](/previous-versions/dotnet/netframework-4.0/z415cf9a(v=vs.100))</span></span> | <span data-ttu-id="13d84-118">远程处理设置架构中的所有元素。</span><span class="sxs-lookup"><span data-stu-id="13d84-118">All elements in the remoting settings schema.</span></span> |
| [<span data-ttu-id="13d84-119">**\<system.Net>** 设置架构</span><span class="sxs-lookup"><span data-stu-id="13d84-119">**\<system.Net>** Settings Schema</span></span>](./network/index.md) | <span data-ttu-id="13d84-120">网络设置架构中的所有元素。</span><span class="sxs-lookup"><span data-stu-id="13d84-120">All elements in the network settings schema.</span></span> |
| [<span data-ttu-id="13d84-121">**\<cryptographySettings>** 设置架构</span><span class="sxs-lookup"><span data-stu-id="13d84-121">**\<cryptographySettings>** Settings Schema</span></span>](./cryptography/index.md) | <span data-ttu-id="13d84-122">加密设置架构中的所有元素。</span><span class="sxs-lookup"><span data-stu-id="13d84-122">All elements in the crypto settings schema.</span></span> |
| [<span data-ttu-id="13d84-123">**\<configuration>** 节架构</span><span class="sxs-lookup"><span data-stu-id="13d84-123">**\<configuration>** Sections Schema</span></span>](configuration-sections-schema.md) | <span data-ttu-id="13d84-124">配置节设置架构中的所有元素。</span><span class="sxs-lookup"><span data-stu-id="13d84-124">All elements in the configuration section settings schema.</span></span> |
| [<span data-ttu-id="13d84-125">跟踪和调试设置架构</span><span class="sxs-lookup"><span data-stu-id="13d84-125">Trace and Debug Settings Schema</span></span>](./trace-debug/index.md) | <span data-ttu-id="13d84-126">跟踪和调试设置架构中的所有元素。</span><span class="sxs-lookup"><span data-stu-id="13d84-126">All elements in the trace and debug settings schema.</span></span> |
| <span data-ttu-id="13d84-127">[ASP.NET 配置设置架构](/previous-versions/dotnet/netframework-4.0/b5ysx397(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="13d84-127">[ASP.NET Configuration Settings Schema](/previous-versions/dotnet/netframework-4.0/b5ysx397(v=vs.100))</span></span> | <span data-ttu-id="13d84-128">ASP.NET 配置架构中的所有元素，包括用于配置 ASP.NET 网站和应用程序的元素。</span><span class="sxs-lookup"><span data-stu-id="13d84-128">All elements in the ASP.NET configuration schema, which includes elements for configuring ASP.NET Web sites and applications.</span></span> <span data-ttu-id="13d84-129">用于 *Web.config* 文件中。</span><span class="sxs-lookup"><span data-stu-id="13d84-129">Used in *Web.config* files.</span></span> |
| <span data-ttu-id="13d84-130">[**\<webServices>** 设置架构](/previous-versions/dotnet/netframework-4.0/cctwteet(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="13d84-130">[**\<webServices>** Settings Schema](/previous-versions/dotnet/netframework-4.0/cctwteet(v=vs.100))</span></span> | <span data-ttu-id="13d84-131">Web 服务设置架构中的所有元素。</span><span class="sxs-lookup"><span data-stu-id="13d84-131">All elements in the Web services settings schema.</span></span> |
| [<span data-ttu-id="13d84-132">Web 设置架构</span><span class="sxs-lookup"><span data-stu-id="13d84-132">Web Settings Schema</span></span>](./web/index.md) | <span data-ttu-id="13d84-133">Web 设置架构中的所有元素，包括用于配置 ASP.NET 如何与主机应用程序（如 IIS）一起工作的元素。</span><span class="sxs-lookup"><span data-stu-id="13d84-133">All elements in the Web settings schema, which includes elements for configuring how ASP.NET works with a host application such as IIS.</span></span> <span data-ttu-id="13d84-134">用于 *aspnet.config* 文件中。</span><span class="sxs-lookup"><span data-stu-id="13d84-134">Used in *aspnet.config* files.</span></span> |

## <a name="remarks"></a><span data-ttu-id="13d84-135">备注</span><span class="sxs-lookup"><span data-stu-id="13d84-135">Remarks</span></span>

<span data-ttu-id="13d84-136">每个配置文件必须仅包含一个 **\<configuration>** 元素。</span><span class="sxs-lookup"><span data-stu-id="13d84-136">Each configuration file must contain exactly one **\<configuration>** element.</span></span>

## <a name="see-also"></a><span data-ttu-id="13d84-137">请参阅</span><span class="sxs-lookup"><span data-stu-id="13d84-137">See also</span></span>

- [<span data-ttu-id="13d84-138">.NET Framework 的配置文件架构</span><span class="sxs-lookup"><span data-stu-id="13d84-138">Configuration file schema for the .NET Framework</span></span>](index.md)
