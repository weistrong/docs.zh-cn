---
description: 了解详细信息： <dependentAssembly> 元素
title: <dependentAssembly> 元素
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/runtime/assemblyBinding/dependentAssembly
- http://schemas.microsoft.com/.NetConfiguration/v2.0#dependentAssembly
helpviewer_keywords:
- container tags, <dependentAssembly> element
- dependentAssembly element
- <dependentAssembly> element
ms.assetid: 14e95627-dd79-4b82-ac85-e682aa3a31d8
ms.openlocfilehash: c804920de961fc609fd04a0853ecbdbc9202e5be
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99719079"
---
# <a name="dependentassembly-element"></a><span data-ttu-id="6f682-103">\<dependentAssembly> 元素</span><span class="sxs-lookup"><span data-stu-id="6f682-103">\<dependentAssembly> Element</span></span>

<span data-ttu-id="6f682-104">封装每个程序集的绑定策略和程序集位置。</span><span class="sxs-lookup"><span data-stu-id="6f682-104">Encapsulates binding policy and assembly location for each assembly.</span></span> <span data-ttu-id="6f682-105">`dependentAssembly`为每个程序集使用一个元素。</span><span class="sxs-lookup"><span data-stu-id="6f682-105">Use one `dependentAssembly` element for each assembly.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<runtime>**](runtime-element.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<assemblyBinding>**](assemblybinding-element-for-runtime.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<dependentAssembly>**  
  
## <a name="syntax"></a><span data-ttu-id="6f682-106">语法</span><span class="sxs-lookup"><span data-stu-id="6f682-106">Syntax</span></span>  
  
```xml  
<dependentAssembly>
</dependentAssembly>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="6f682-107">特性和元素</span><span class="sxs-lookup"><span data-stu-id="6f682-107">Attributes and Elements</span></span>  

 <span data-ttu-id="6f682-108">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="6f682-108">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="6f682-109">特性</span><span class="sxs-lookup"><span data-stu-id="6f682-109">Attributes</span></span>  

 <span data-ttu-id="6f682-110">无。</span><span class="sxs-lookup"><span data-stu-id="6f682-110">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="6f682-111">子元素</span><span class="sxs-lookup"><span data-stu-id="6f682-111">Child Elements</span></span>  
  
|<span data-ttu-id="6f682-112">元素</span><span class="sxs-lookup"><span data-stu-id="6f682-112">Element</span></span>|<span data-ttu-id="6f682-113">说明</span><span class="sxs-lookup"><span data-stu-id="6f682-113">Description</span></span>|  
|-------------|-----------------|  
|`assemblyIdentity`|<span data-ttu-id="6f682-114">包含有关程序集的标识信息。</span><span class="sxs-lookup"><span data-stu-id="6f682-114">Contains identifying information about the assembly.</span></span> <span data-ttu-id="6f682-115">此元素必须包含在每个 `dependentAssembly` 元素中。</span><span class="sxs-lookup"><span data-stu-id="6f682-115">This element must be included in each `dependentAssembly` element.</span></span>|  
|`codeBase`|<span data-ttu-id="6f682-116">指定运行时在计算机上未安装共享程序集的情况下可以找到该程序集的位置。</span><span class="sxs-lookup"><span data-stu-id="6f682-116">Specifies where the runtime can find a shared assembly if it is not installed on the computer.</span></span>|  
|`bindingRedirect`|<span data-ttu-id="6f682-117">将一个程序集版本重定向到另一个版本。</span><span class="sxs-lookup"><span data-stu-id="6f682-117">Redirects one assembly version to another.</span></span>|  
|`publisherPolicy`|<span data-ttu-id="6f682-118">指定运行时是否应用此程序集的发布服务器策略。</span><span class="sxs-lookup"><span data-stu-id="6f682-118">Specifies whether the runtime applies publisher policy for this assembly.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="6f682-119">父元素</span><span class="sxs-lookup"><span data-stu-id="6f682-119">Parent Elements</span></span>  
  
|<span data-ttu-id="6f682-120">元素</span><span class="sxs-lookup"><span data-stu-id="6f682-120">Element</span></span>|<span data-ttu-id="6f682-121">说明</span><span class="sxs-lookup"><span data-stu-id="6f682-121">Description</span></span>|  
|-------------|-----------------|  
|`assemblyBinding`|<span data-ttu-id="6f682-122">包含有关程序集版本重定向和程序集位置的信息。</span><span class="sxs-lookup"><span data-stu-id="6f682-122">Contains information about assembly version redirection and the locations of assemblies.</span></span>|  
|`configuration`|<span data-ttu-id="6f682-123">公共语言运行时和 .NET Framework 应用程序所使用的每个配置文件中的根元素。</span><span class="sxs-lookup"><span data-stu-id="6f682-123">The root element in every configuration file used by the common language runtime and .NET Framework applications.</span></span>|  
|`runtime`|<span data-ttu-id="6f682-124">包含有关程序集绑定和垃圾回收的信息。</span><span class="sxs-lookup"><span data-stu-id="6f682-124">Contains information about assembly binding and garbage collection.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="6f682-125">示例</span><span class="sxs-lookup"><span data-stu-id="6f682-125">Example</span></span>  

 <span data-ttu-id="6f682-126">下面的示例演示如何封装两个程序集的程序集信息。</span><span class="sxs-lookup"><span data-stu-id="6f682-126">The following example shows how to encapsulate assembly information for two assemblies.</span></span>  
  
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
         <dependentAssembly>  
            <assemblyIdentity name="mySecondAssembly"  
                              publicKeyToken="32ab4ba45e0a69a1"  
                              culture="neutral" />  
            <!--Redirection and codeBase policy for mySecondAssembly.-->  
         </dependentAssembly>  
      </assemblyBinding>  
   </runtime>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="6f682-127">请参阅</span><span class="sxs-lookup"><span data-stu-id="6f682-127">See also</span></span>

- [<span data-ttu-id="6f682-128">运行时设置架构</span><span class="sxs-lookup"><span data-stu-id="6f682-128">Runtime Settings Schema</span></span>](index.md)
- [<span data-ttu-id="6f682-129">配置文件架构</span><span class="sxs-lookup"><span data-stu-id="6f682-129">Configuration File Schema</span></span>](../index.md)
- [<span data-ttu-id="6f682-130">重定向程序集版本</span><span class="sxs-lookup"><span data-stu-id="6f682-130">Redirecting Assembly Versions</span></span>](../../redirect-assembly-versions.md)
