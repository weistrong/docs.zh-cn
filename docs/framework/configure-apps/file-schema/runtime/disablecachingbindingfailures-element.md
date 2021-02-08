---
description: 了解详细信息： <disableCachingBindingFailures> 元素
title: <disableCachingBindingFailures> 元素
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#disableCachingBindingFailures
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/runtime/disableCachingBindingFailures
helpviewer_keywords:
- assemblies [.NET Framework],caching binding failures
- caching assembly binding failures
- <disableCachingBindingFailures> element
- disableCachingBindingFailures element
ms.assetid: bf598873-83b7-48de-8955-00b0504fbad0
ms.openlocfilehash: b1f36f6a8fc7c78a0dc90ecc78ad725b677fdf40
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99787105"
---
# <a name="disablecachingbindingfailures-element"></a><span data-ttu-id="17d80-103">\<disableCachingBindingFailures> 元素</span><span class="sxs-lookup"><span data-stu-id="17d80-103">\<disableCachingBindingFailures> Element</span></span>

<span data-ttu-id="17d80-104">指定是否禁止缓存发生的绑定故障，因为探查找不到该程序集。</span><span class="sxs-lookup"><span data-stu-id="17d80-104">Specifies whether to disable the caching of binding failures that occur because the assembly was not found by probing.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<runtime>**](runtime-element.md)\
&nbsp;&nbsp;&nbsp;&nbsp;**\<disableCachingBindingFailures>**  
  
## <a name="syntax"></a><span data-ttu-id="17d80-105">语法</span><span class="sxs-lookup"><span data-stu-id="17d80-105">Syntax</span></span>  
  
```xml  
<disableCachingBindingFailures enabled="0|1"/>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="17d80-106">特性和元素</span><span class="sxs-lookup"><span data-stu-id="17d80-106">Attributes and Elements</span></span>  

 <span data-ttu-id="17d80-107">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="17d80-107">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="17d80-108">特性</span><span class="sxs-lookup"><span data-stu-id="17d80-108">Attributes</span></span>  
  
|<span data-ttu-id="17d80-109">属性</span><span class="sxs-lookup"><span data-stu-id="17d80-109">Attribute</span></span>|<span data-ttu-id="17d80-110">说明</span><span class="sxs-lookup"><span data-stu-id="17d80-110">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="17d80-111">enabled</span><span class="sxs-lookup"><span data-stu-id="17d80-111">enabled</span></span>|<span data-ttu-id="17d80-112">必需的特性。</span><span class="sxs-lookup"><span data-stu-id="17d80-112">Required attribute.</span></span><br /><br /> <span data-ttu-id="17d80-113">指定是否禁止缓存发生的绑定故障，因为探查找不到该程序集。</span><span class="sxs-lookup"><span data-stu-id="17d80-113">Specifies whether to disable the caching of binding failures that occur because the assembly was not found by probing.</span></span>|  
  
## <a name="enabled-attribute"></a><span data-ttu-id="17d80-114">enabled 特性</span><span class="sxs-lookup"><span data-stu-id="17d80-114">enabled Attribute</span></span>  
  
|<span data-ttu-id="17d80-115">值</span><span class="sxs-lookup"><span data-stu-id="17d80-115">Value</span></span>|<span data-ttu-id="17d80-116">说明</span><span class="sxs-lookup"><span data-stu-id="17d80-116">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="17d80-117">0</span><span class="sxs-lookup"><span data-stu-id="17d80-117">0</span></span>|<span data-ttu-id="17d80-118">请勿禁止缓存发生的绑定故障，因为探查找不到该程序集。</span><span class="sxs-lookup"><span data-stu-id="17d80-118">Do not disable the caching of binding failures that occur because the assembly was not found by probing.</span></span> <span data-ttu-id="17d80-119">这是默认绑定行为，从 .NET Framework 版本2.0 开始。</span><span class="sxs-lookup"><span data-stu-id="17d80-119">This is the default binding behavior starting with the .NET Framework version 2.0.</span></span>|  
|<span data-ttu-id="17d80-120">1</span><span class="sxs-lookup"><span data-stu-id="17d80-120">1</span></span>|<span data-ttu-id="17d80-121">禁止缓存发生的绑定故障，因为探查找不到该程序集。</span><span class="sxs-lookup"><span data-stu-id="17d80-121">Disable the caching of binding failures that occur because the assembly was not found by probing.</span></span> <span data-ttu-id="17d80-122">此设置将恢复为 .NET Framework 版本1.1 的绑定行为。</span><span class="sxs-lookup"><span data-stu-id="17d80-122">This setting reverts to the binding behavior of the .NET Framework version 1.1.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="17d80-123">子元素</span><span class="sxs-lookup"><span data-stu-id="17d80-123">Child Elements</span></span>  

 <span data-ttu-id="17d80-124">无。</span><span class="sxs-lookup"><span data-stu-id="17d80-124">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="17d80-125">父元素</span><span class="sxs-lookup"><span data-stu-id="17d80-125">Parent Elements</span></span>  
  
|<span data-ttu-id="17d80-126">元素</span><span class="sxs-lookup"><span data-stu-id="17d80-126">Element</span></span>|<span data-ttu-id="17d80-127">说明</span><span class="sxs-lookup"><span data-stu-id="17d80-127">Description</span></span>|  
|-------------|-----------------|  
|`configuration`|<span data-ttu-id="17d80-128">公共语言运行时和 .NET Framework 应用程序所使用的每个配置文件中的根元素。</span><span class="sxs-lookup"><span data-stu-id="17d80-128">The root element in every configuration file used by the common language runtime and .NET Framework applications.</span></span>|  
|`runtime`|<span data-ttu-id="17d80-129">包含有关程序集绑定和垃圾回收的信息。</span><span class="sxs-lookup"><span data-stu-id="17d80-129">Contains information about assembly binding and garbage collection.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="17d80-130">备注</span><span class="sxs-lookup"><span data-stu-id="17d80-130">Remarks</span></span>  

 <span data-ttu-id="17d80-131">从 .NET Framework 版本2.0 开始，加载程序集的默认行为是缓存所有绑定和加载失败。</span><span class="sxs-lookup"><span data-stu-id="17d80-131">Starting with the .NET Framework version 2.0, the default behavior for loading assemblies is to cache all binding and loading failures.</span></span> <span data-ttu-id="17d80-132">也就是说，如果尝试加载程序集失败，则加载同一程序集的后续请求将立即失败，而不会尝试查找程序集。</span><span class="sxs-lookup"><span data-stu-id="17d80-132">That is, if an attempt to load an assembly fails, subsequent requests to load the same assembly fail immediately, without any attempt to locate the assembly.</span></span> <span data-ttu-id="17d80-133">此元素将禁用发生的绑定故障的默认行为，因为在探测路径中找不到该程序集。</span><span class="sxs-lookup"><span data-stu-id="17d80-133">This element disables that default behavior for binding failures that occur because the assembly could not be found in the probing path.</span></span> <span data-ttu-id="17d80-134">这些失败会引发 <xref:System.IO.FileNotFoundException> 。</span><span class="sxs-lookup"><span data-stu-id="17d80-134">These failures throw <xref:System.IO.FileNotFoundException>.</span></span>  
  
 <span data-ttu-id="17d80-135">某些绑定和加载失败不受此元素影响，并且始终会进行缓存。</span><span class="sxs-lookup"><span data-stu-id="17d80-135">Some binding and loading failures are not affected by this element, and are always cached.</span></span> <span data-ttu-id="17d80-136">出现这些失败是因为程序集已找到，但无法加载。</span><span class="sxs-lookup"><span data-stu-id="17d80-136">These failures occur because the assembly was found but could not be loaded.</span></span> <span data-ttu-id="17d80-137">它们引发 <xref:System.BadImageFormatException> 或 <xref:System.IO.FileLoadException> 。</span><span class="sxs-lookup"><span data-stu-id="17d80-137">They throw <xref:System.BadImageFormatException> or <xref:System.IO.FileLoadException>.</span></span> <span data-ttu-id="17d80-138">以下列表包括此类故障的一些示例。</span><span class="sxs-lookup"><span data-stu-id="17d80-138">The following list includes some examples of such failures.</span></span>  
  
- <span data-ttu-id="17d80-139">如果尝试加载文件不是有效的程序集，则即使将错误文件替换为正确的程序集，以后尝试加载程序集也会失败。</span><span class="sxs-lookup"><span data-stu-id="17d80-139">If you attempt to load a file is not a valid assembly, subsequent attempts to load the assembly will fail even if the bad file is replaced with the correct assembly.</span></span>  
  
- <span data-ttu-id="17d80-140">如果尝试加载文件系统锁定的程序集，则即使在文件系统释放程序集之后，加载程序集的后续尝试也将失败。</span><span class="sxs-lookup"><span data-stu-id="17d80-140">If you attempt to load an assembly that is locked by the file system, subsequent attempts to load the assembly will fail even after the assembly is released by the file system.</span></span>  
  
- <span data-ttu-id="17d80-141">如果尝试加载的程序集的一个或多个版本位于探测路径中，但你请求的特定版本不在其中，则即使将正确的版本移入探测路径，后续尝试加载该版本也会失败。</span><span class="sxs-lookup"><span data-stu-id="17d80-141">If one or more versions of the assembly that you are attempting to load is in the probing path, but the specific version you are requesting is not among them, subsequent attempts to load that version will fail even if the correct version is moved into the probing path.</span></span>  
  
## <a name="example"></a><span data-ttu-id="17d80-142">示例</span><span class="sxs-lookup"><span data-stu-id="17d80-142">Example</span></span>  

 <span data-ttu-id="17d80-143">下面的示例演示如何禁止缓存发生的程序集绑定故障，因为探查找不到该程序集。</span><span class="sxs-lookup"><span data-stu-id="17d80-143">The following example shows how to disable the caching of assembly binding failures that occur because the assembly was not found by probing.</span></span>  
  
```xml  
<configuration>  
   <runtime>  
      <disableCachingBindingFailures enabled="1" />  
   </runtime>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="17d80-144">请参阅</span><span class="sxs-lookup"><span data-stu-id="17d80-144">See also</span></span>

- [<span data-ttu-id="17d80-145">运行时设置架构</span><span class="sxs-lookup"><span data-stu-id="17d80-145">Runtime Settings Schema</span></span>](index.md)
- [<span data-ttu-id="17d80-146">配置文件架构</span><span class="sxs-lookup"><span data-stu-id="17d80-146">Configuration File Schema</span></span>](../index.md)
- [<span data-ttu-id="17d80-147">运行时如何定位程序集</span><span class="sxs-lookup"><span data-stu-id="17d80-147">How the Runtime Locates Assemblies</span></span>](../../../deployment/how-the-runtime-locates-assemblies.md)
