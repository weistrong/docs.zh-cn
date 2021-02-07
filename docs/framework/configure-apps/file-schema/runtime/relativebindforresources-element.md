---
description: 了解详细信息： <relativeBindForResources> 元素
title: <relativeBindForResources> 元素
ms.date: 03/30/2017
helpviewer_keywords:
- RelativeBindForResources element
- <relativeBindForResources> element
ms.assetid: 846ffa47-7257-4ce3-8cac-7ff627e0e34f
ms.openlocfilehash: f08d8f8a8fc4bb14d28762254dca99788d44a858
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99712917"
---
# <a name="relativebindforresources-element"></a><span data-ttu-id="f394d-103">\<relativeBindForResources> 元素</span><span class="sxs-lookup"><span data-stu-id="f394d-103">\<relativeBindForResources> Element</span></span>

<span data-ttu-id="f394d-104">优化附属程序集的探测。</span><span class="sxs-lookup"><span data-stu-id="f394d-104">Optimizes the probe for satellite assemblies.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<runtime>**](runtime-element.md)\
&nbsp;&nbsp;&nbsp;&nbsp;**\<relativeBindForResources>**  
  
## <a name="syntax"></a><span data-ttu-id="f394d-105">语法</span><span class="sxs-lookup"><span data-stu-id="f394d-105">Syntax</span></span>  
  
```xml
<relativeBindForResources
   enabled="true|false" />  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="f394d-106">特性和元素</span><span class="sxs-lookup"><span data-stu-id="f394d-106">Attributes and Elements</span></span>  

 <span data-ttu-id="f394d-107">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="f394d-107">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="f394d-108">特性</span><span class="sxs-lookup"><span data-stu-id="f394d-108">Attributes</span></span>  
  
|<span data-ttu-id="f394d-109">属性</span><span class="sxs-lookup"><span data-stu-id="f394d-109">Attribute</span></span>|<span data-ttu-id="f394d-110">描述</span><span class="sxs-lookup"><span data-stu-id="f394d-110">Description</span></span>|  
|---------------|-----------------|  
|`enabled`|<span data-ttu-id="f394d-111">必需的特性。</span><span class="sxs-lookup"><span data-stu-id="f394d-111">Required attribute.</span></span><br /><br /> <span data-ttu-id="f394d-112">指定公共语言运行时是否优化附属程序集的探测。</span><span class="sxs-lookup"><span data-stu-id="f394d-112">Specifies whether the common language runtime optimizes the probe for satellite assemblies.</span></span>|  
  
## <a name="enabled-attribute"></a><span data-ttu-id="f394d-113">enabled 特性</span><span class="sxs-lookup"><span data-stu-id="f394d-113">enabled Attribute</span></span>  
  
|<span data-ttu-id="f394d-114">值</span><span class="sxs-lookup"><span data-stu-id="f394d-114">Value</span></span>|<span data-ttu-id="f394d-115">说明</span><span class="sxs-lookup"><span data-stu-id="f394d-115">Description</span></span>|  
|-----------|-----------------|  
|`false`|<span data-ttu-id="f394d-116">运行时不会优化附属程序集的探测。</span><span class="sxs-lookup"><span data-stu-id="f394d-116">The runtime does not optimize the probe for satellite assemblies.</span></span> <span data-ttu-id="f394d-117">这是默认值。</span><span class="sxs-lookup"><span data-stu-id="f394d-117">This is the default value.</span></span>|  
|`true`|<span data-ttu-id="f394d-118">运行时优化附属程序集的探测。</span><span class="sxs-lookup"><span data-stu-id="f394d-118">The runtime optimizes the probe for satellite assemblies.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="f394d-119">子元素</span><span class="sxs-lookup"><span data-stu-id="f394d-119">Child Elements</span></span>  

 <span data-ttu-id="f394d-120">无。</span><span class="sxs-lookup"><span data-stu-id="f394d-120">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="f394d-121">父元素</span><span class="sxs-lookup"><span data-stu-id="f394d-121">Parent Elements</span></span>  
  
|<span data-ttu-id="f394d-122">元素</span><span class="sxs-lookup"><span data-stu-id="f394d-122">Element</span></span>|<span data-ttu-id="f394d-123">说明</span><span class="sxs-lookup"><span data-stu-id="f394d-123">Description</span></span>|  
|-------------|-----------------|  
|`configuration`|<span data-ttu-id="f394d-124">公共语言运行时和 .NET Framework 应用程序所使用的每个配置文件中的根元素。</span><span class="sxs-lookup"><span data-stu-id="f394d-124">The root element in every configuration file used by the common language runtime and .NET Framework applications.</span></span>|  
|`runtime`|<span data-ttu-id="f394d-125">包含有关运行时初始化选项的信息。</span><span class="sxs-lookup"><span data-stu-id="f394d-125">Contains information about runtime initialization options.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="f394d-126">备注</span><span class="sxs-lookup"><span data-stu-id="f394d-126">Remarks</span></span>  

 <span data-ttu-id="f394d-127">一般情况下，资源管理器探测资源，如 [打包和部署资源](../../../resources/packaging-and-deploying-resources-in-desktop-apps.md) 主题中所述。</span><span class="sxs-lookup"><span data-stu-id="f394d-127">In general, Resource Manager probes for resources, as documented in the [Packaging and Deploying Resources](../../../resources/packaging-and-deploying-resources-in-desktop-apps.md) topic.</span></span> <span data-ttu-id="f394d-128">这意味着，当资源管理器探测资源的特定本地化版本时，它可能会在全局程序集缓存中查找，在应用程序的基本代码中查找特定于区域性的文件夹，为附属程序集查询 Windows Installer，并引发 <xref:System.AppDomain.AssemblyResolve?displayProperty=nameWithType> 事件。</span><span class="sxs-lookup"><span data-stu-id="f394d-128">This means that when Resource Manager probes for a particular localized version of a resource, it may look in the global assembly cache, look in a culture-specific folder in the application's code base, query Windows Installer for satellite assemblies, and raise the <xref:System.AppDomain.AssemblyResolve?displayProperty=nameWithType> event.</span></span> <span data-ttu-id="f394d-129">`<relativeBindForResources>`元素优化资源管理器探测附属程序集的方式。</span><span class="sxs-lookup"><span data-stu-id="f394d-129">The `<relativeBindForResources>` element optimizes the way in which Resource Manager probes for satellite assemblies.</span></span> <span data-ttu-id="f394d-130">当在以下条件下探测资源时，它可以提高性能：</span><span class="sxs-lookup"><span data-stu-id="f394d-130">It can improve performance when probing for resources under the following conditions:</span></span>  
  
- <span data-ttu-id="f394d-131">当附属程序集部署在与代码程序集相同的位置时。</span><span class="sxs-lookup"><span data-stu-id="f394d-131">When the satellite assembly is deployed in the same location as the code assembly.</span></span> <span data-ttu-id="f394d-132">换言之，如果代码程序集安装在全局程序集缓存中，则还必须在该程序集中安装附属程序集。</span><span class="sxs-lookup"><span data-stu-id="f394d-132">In other words, if the code assembly is installed in the global assembly cache, the satellite assemblies must also be installed there.</span></span> <span data-ttu-id="f394d-133">如果代码程序集安装在应用程序的代码库中，则附属程序集还必须安装在基本代码的特定于区域性的文件夹中。</span><span class="sxs-lookup"><span data-stu-id="f394d-133">If the code assembly is installed in the application's code base, the satellite assemblies must also be installed in a culture-specific folder in the code base.</span></span>  
  
- <span data-ttu-id="f394d-134">如果未使用 Windows Installer 或只是很少使用附属程序集的按需安装。</span><span class="sxs-lookup"><span data-stu-id="f394d-134">When Windows Installer is not used or is used only rarely for on-demand installation of satellite assemblies.</span></span>  
  
- <span data-ttu-id="f394d-135">当应用程序代码不处理 <xref:System.AppDomain.AssemblyResolve?displayProperty=nameWithType> 事件时。</span><span class="sxs-lookup"><span data-stu-id="f394d-135">When application code does not handle the <xref:System.AppDomain.AssemblyResolve?displayProperty=nameWithType> event.</span></span>  
  
 <span data-ttu-id="f394d-136">设置 `enabled` 元素的属性 `<relativeBindForResources>` ，以 `true` 优化资源管理器的附属程序集探测，如下所示：</span><span class="sxs-lookup"><span data-stu-id="f394d-136">Setting the `enabled` attribute of the `<relativeBindForResources>` element to `true` optimizes Resource Manager's probe for satellite assemblies as follows:</span></span>  
  
- <span data-ttu-id="f394d-137">它使用父代码程序集的位置来探测附属程序集。</span><span class="sxs-lookup"><span data-stu-id="f394d-137">It uses the location of the parent code assembly to probe for the satellite assembly.</span></span>  
  
- <span data-ttu-id="f394d-138">它不会为附属程序集查询 Windows Installer。</span><span class="sxs-lookup"><span data-stu-id="f394d-138">It does not query Windows Installer for satellite assemblies.</span></span>  
  
- <span data-ttu-id="f394d-139">它不会引发 <xref:System.AppDomain.AssemblyResolve?displayProperty=nameWithType> 事件。</span><span class="sxs-lookup"><span data-stu-id="f394d-139">It does not raise the <xref:System.AppDomain.AssemblyResolve?displayProperty=nameWithType> event.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f394d-140">请参阅</span><span class="sxs-lookup"><span data-stu-id="f394d-140">See also</span></span>

- [<span data-ttu-id="f394d-141">打包和部署资源</span><span class="sxs-lookup"><span data-stu-id="f394d-141">Packaging and Deploying Resources</span></span>](../../../resources/packaging-and-deploying-resources-in-desktop-apps.md)
- [<span data-ttu-id="f394d-142">运行时设置架构</span><span class="sxs-lookup"><span data-stu-id="f394d-142">Runtime Settings Schema</span></span>](index.md)
- [<span data-ttu-id="f394d-143">配置文件架构</span><span class="sxs-lookup"><span data-stu-id="f394d-143">Configuration File Schema</span></span>](../index.md)
