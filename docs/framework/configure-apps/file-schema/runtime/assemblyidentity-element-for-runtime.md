---
description: 详细了解： <assemblyIdentity> 的元素 <runtime>
title: <runtime> 的 <assemblyIdentity> 元素
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/runtime/assemblyBinding/dependentAssembly/assemblyIdentity
- http://schemas.microsoft.com/.NetConfiguration/v2.0#assemblyIdentity
helpviewer_keywords:
- <assemblyIdentity> element
- container tags, <assemblyIdentity> element
- assemblyIdentity element
ms.assetid: cea4d187-6398-4da4-af09-c1abc6a349c1
ms.openlocfilehash: d53c4f7f5207fbcf9ad4a8f82667eacc1f57f5e2
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99719183"
---
# <a name="assemblyidentity-element-for-runtime"></a><span data-ttu-id="33ce9-103">\<runtime> 的 \<assemblyIdentity> 元素</span><span class="sxs-lookup"><span data-stu-id="33ce9-103">\<assemblyIdentity> Element for \<runtime></span></span>

<span data-ttu-id="33ce9-104">包含有关程序集的标识信息。</span><span class="sxs-lookup"><span data-stu-id="33ce9-104">Contains identifying information about the assembly.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<runtime>**](runtime-element.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<assemblyBinding>**](assemblybinding-element-for-runtime.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<dependentAssembly>**](dependentassembly-element.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<assemblyIdentity>**  
  
## <a name="syntax"></a><span data-ttu-id="33ce9-105">语法</span><span class="sxs-lookup"><span data-stu-id="33ce9-105">Syntax</span></span>  
  
```xml  
   <assemblyIdentity
name="assembly name"  
publicKeyToken="public key token"  
culture="assembly culture"/>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="33ce9-106">特性和元素</span><span class="sxs-lookup"><span data-stu-id="33ce9-106">Attributes and Elements</span></span>  

 <span data-ttu-id="33ce9-107">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="33ce9-107">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="33ce9-108">特性</span><span class="sxs-lookup"><span data-stu-id="33ce9-108">Attributes</span></span>  
  
|<span data-ttu-id="33ce9-109">属性</span><span class="sxs-lookup"><span data-stu-id="33ce9-109">Attribute</span></span>|<span data-ttu-id="33ce9-110">描述</span><span class="sxs-lookup"><span data-stu-id="33ce9-110">Description</span></span>|  
|---------------|-----------------|  
|`name`|<span data-ttu-id="33ce9-111">必需的特性。</span><span class="sxs-lookup"><span data-stu-id="33ce9-111">Required attribute.</span></span><br /><br /> <span data-ttu-id="33ce9-112">程序集的名称</span><span class="sxs-lookup"><span data-stu-id="33ce9-112">The name of the assembly</span></span>|  
|`culture`|<span data-ttu-id="33ce9-113">可选特性。</span><span class="sxs-lookup"><span data-stu-id="33ce9-113">Optional attribute.</span></span><br /><br /> <span data-ttu-id="33ce9-114">一个字符串，指定程序集的语言和国家/地区。</span><span class="sxs-lookup"><span data-stu-id="33ce9-114">A string that specifies the language and country/region of the assembly.</span></span>|  
|`publicKeyToken`|<span data-ttu-id="33ce9-115">可选特性。</span><span class="sxs-lookup"><span data-stu-id="33ce9-115">Optional attribute.</span></span><br /><br /> <span data-ttu-id="33ce9-116">一个十六进制值，该值指定程序集的强名称。</span><span class="sxs-lookup"><span data-stu-id="33ce9-116">A hexadecimal value that specifies the strong name of the assembly.</span></span>|  
|`processorArchitecture`|<span data-ttu-id="33ce9-117">可选特性。</span><span class="sxs-lookup"><span data-stu-id="33ce9-117">Optional attribute.</span></span><br /><br /> <span data-ttu-id="33ce9-118">值 "x86"、"amd64"、"msil" 或 "ia64" 之一，为包含特定于处理器的代码的程序集指定处理器体系结构。</span><span class="sxs-lookup"><span data-stu-id="33ce9-118">One of the values "x86", "amd64", "msil", or "ia64", specifying the processor architecture for an assembly that contains processor-specific code.</span></span> <span data-ttu-id="33ce9-119">这些值不区分大小写。</span><span class="sxs-lookup"><span data-stu-id="33ce9-119">The values are not case-sensitive.</span></span> <span data-ttu-id="33ce9-120">如果为该属性分配了其他任何值，则将 `<assemblyIdentity>` 忽略整个元素。</span><span class="sxs-lookup"><span data-stu-id="33ce9-120">If the attribute is assigned any other value, the entire `<assemblyIdentity>` element is ignored.</span></span> <span data-ttu-id="33ce9-121">请参阅 <xref:System.Reflection.ProcessorArchitecture>。</span><span class="sxs-lookup"><span data-stu-id="33ce9-121">See <xref:System.Reflection.ProcessorArchitecture>.</span></span>|  
  
## <a name="processorarchitecture-attribute"></a><span data-ttu-id="33ce9-122">processorArchitecture 特性</span><span class="sxs-lookup"><span data-stu-id="33ce9-122">processorArchitecture Attribute</span></span>  
  
|<span data-ttu-id="33ce9-123">值</span><span class="sxs-lookup"><span data-stu-id="33ce9-123">Value</span></span>|<span data-ttu-id="33ce9-124">说明</span><span class="sxs-lookup"><span data-stu-id="33ce9-124">Description</span></span>|  
|-----------|-----------------|  
|`amd64`|<span data-ttu-id="33ce9-125">仅适用于 AMD x86-64 体系结构。</span><span class="sxs-lookup"><span data-stu-id="33ce9-125">AMD x86-64 architecture only.</span></span>|  
|`ia64`|<span data-ttu-id="33ce9-126">仅限 Intel Itanium 体系结构。</span><span class="sxs-lookup"><span data-stu-id="33ce9-126">Intel Itanium architecture only.</span></span>|  
|`msil`|<span data-ttu-id="33ce9-127">不特定于处理器和每字位数。</span><span class="sxs-lookup"><span data-stu-id="33ce9-127">Neutral with respect to processor and bits-per-word.</span></span>|  
|`x86`|<span data-ttu-id="33ce9-128">32位 x86 处理器，在 Windows on Windows (WOW) 环境的64位平台上。</span><span class="sxs-lookup"><span data-stu-id="33ce9-128">A 32-bit x86 processor, either native or in the Windows on Windows (WOW) environment on a 64-bit platform.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="33ce9-129">子元素</span><span class="sxs-lookup"><span data-stu-id="33ce9-129">Child Elements</span></span>  

 <span data-ttu-id="33ce9-130">无。</span><span class="sxs-lookup"><span data-stu-id="33ce9-130">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="33ce9-131">父元素</span><span class="sxs-lookup"><span data-stu-id="33ce9-131">Parent Elements</span></span>  
  
|<span data-ttu-id="33ce9-132">元素</span><span class="sxs-lookup"><span data-stu-id="33ce9-132">Element</span></span>|<span data-ttu-id="33ce9-133">说明</span><span class="sxs-lookup"><span data-stu-id="33ce9-133">Description</span></span>|  
|-------------|-----------------|  
|`assemblyBinding`|<span data-ttu-id="33ce9-134">包含有关程序集版本重定向和程序集位置的信息。</span><span class="sxs-lookup"><span data-stu-id="33ce9-134">Contains information about assembly version redirection and the locations of assemblies.</span></span>|  
|`configuration`|<span data-ttu-id="33ce9-135">公共语言运行时和 .NET Framework 应用程序所使用的每个配置文件中的根元素。</span><span class="sxs-lookup"><span data-stu-id="33ce9-135">The root element in every configuration file used by the common language runtime and .NET Framework applications.</span></span>|  
|`dependentAssembly`|<span data-ttu-id="33ce9-136">封装每个程序集的绑定策略和程序集位置。</span><span class="sxs-lookup"><span data-stu-id="33ce9-136">Encapsulates binding policy and assembly location for each assembly.</span></span> <span data-ttu-id="33ce9-137">`<dependentAssembly>`为每个程序集使用一个元素。</span><span class="sxs-lookup"><span data-stu-id="33ce9-137">Use one `<dependentAssembly>` element for each assembly.</span></span>|  
|`runtime`|<span data-ttu-id="33ce9-138">包含有关程序集绑定和垃圾回收的信息。</span><span class="sxs-lookup"><span data-stu-id="33ce9-138">Contains information about assembly binding and garbage collection.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="33ce9-139">备注</span><span class="sxs-lookup"><span data-stu-id="33ce9-139">Remarks</span></span>  

 <span data-ttu-id="33ce9-140">每个 **\<dependentAssembly>** 元素必须有一个 **\<assemblyIdentity>** 子元素。</span><span class="sxs-lookup"><span data-stu-id="33ce9-140">Every **\<dependentAssembly>** element must have one **\<assemblyIdentity>** child element.</span></span>  
  
 <span data-ttu-id="33ce9-141">如果该 `processorArchitecture` 属性存在，则 `<assemblyIdentity>` 元素仅适用于具有相应处理器体系结构的程序集。</span><span class="sxs-lookup"><span data-stu-id="33ce9-141">If the `processorArchitecture` attribute is present, the `<assemblyIdentity>` element applies only to the assembly with the corresponding processor architecture.</span></span> <span data-ttu-id="33ce9-142">如果该 `processorArchitecture` 属性不存在，则该 `<assemblyIdentity>` 元素可应用于具有任何处理器体系结构的程序集。</span><span class="sxs-lookup"><span data-stu-id="33ce9-142">If the `processorArchitecture` attribute is not present, the `<assemblyIdentity>` element can apply to an assembly with any processor architecture.</span></span>  
  
 <span data-ttu-id="33ce9-143">下面的示例显示了两个程序集的配置文件，这些程序集具有两个不同的两个处理器体系结构，并且其版本尚未保持同步。当应用程序在 x86 平台上执行时，第一个 `<assemblyIdentity>` 元素应用，另一个元素将被忽略。</span><span class="sxs-lookup"><span data-stu-id="33ce9-143">The following example shows a configuration file for two assemblies with the same name that target two different two processor architectures, and whose versions have not been maintained in synch. When the application executes on the x86 platform the first `<assemblyIdentity>` element applies and the other is ignored.</span></span> <span data-ttu-id="33ce9-144">如果应用程序在 x86 或 ia64 以外的平台上执行，则会忽略这两者。</span><span class="sxs-lookup"><span data-stu-id="33ce9-144">If the application executes on a platform other than x86 or ia64, both are ignored.</span></span>  
  
```xml  
<configuration>  
   <runtime>  
      <assemblyBinding xmlns="urn:schemas-microsoft-com:asm.v1">  
         <dependentAssembly>  
            <assemblyIdentity name="MyAssembly"  
                  publicKeyToken="14a739be0244c389"  
                  culture="neutral"  
                  processorArchitecture="x86" />  
            <bindingRedirect oldVersion= "1.0.0.0"
                  newVersion="1.1.0.0" />  
         </dependentAssembly>  
         <dependentAssembly>  
            <assemblyIdentity name="MyAssembly"  
                  publicKeyToken="14a739be0244c389"  
                  culture="neutral"
                  processorArchitecture="ia64" />  
            <bindingRedirect oldVersion="1.0.0.0"
                  newVersion="2.0.0.0" />  
         </dependentAssembly>  
      </assemblyBinding>  
   </runtime>  
</configuration>  
```  
  
 <span data-ttu-id="33ce9-145">如果配置文件包含 `<assemblyIdentity>` 没有属性的元素 `processorArchitecture` ，并且不包含与平台相匹配的元素，则使用没有属性的元素 `processorArchitecture` 。</span><span class="sxs-lookup"><span data-stu-id="33ce9-145">If a configuration file contains an `<assemblyIdentity>` element with no `processorArchitecture` attribute, and does not contain an element that matches the platform, the element without the `processorArchitecture` attribute is used.</span></span>  
  
## <a name="example"></a><span data-ttu-id="33ce9-146">示例</span><span class="sxs-lookup"><span data-stu-id="33ce9-146">Example</span></span>  

 <span data-ttu-id="33ce9-147">下面的示例演示如何提供有关程序集的信息。</span><span class="sxs-lookup"><span data-stu-id="33ce9-147">The following example shows how to provide information about an assembly.</span></span>  
  
```xml  
<configuration>  
   <runtime>  
      <assemblyBinding xmlns="urn:schemas-microsoft-com:asm.v1">  
         <dependentAssembly>  
            <assemblyIdentity name="myAssembly"  
                              publicKeyToken="32ab4ba45e0a69a1"  
                              culture="neutral" />  
            <!--Redirection and codeBase policy for myAssembly.-->  
         </dependentAssembly>  
      </assemblyBinding>  
   </runtime>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="33ce9-148">请参阅</span><span class="sxs-lookup"><span data-stu-id="33ce9-148">See also</span></span>

- [<span data-ttu-id="33ce9-149">运行时设置架构</span><span class="sxs-lookup"><span data-stu-id="33ce9-149">Runtime Settings Schema</span></span>](index.md)
- [<span data-ttu-id="33ce9-150">配置文件架构</span><span class="sxs-lookup"><span data-stu-id="33ce9-150">Configuration File Schema</span></span>](../index.md)
- [<span data-ttu-id="33ce9-151">重定向程序集版本</span><span class="sxs-lookup"><span data-stu-id="33ce9-151">Redirecting Assembly Versions</span></span>](../../redirect-assembly-versions.md)
