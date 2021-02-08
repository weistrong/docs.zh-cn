---
description: 了解详细信息： <publisherPolicy> 元素
title: <publisherPolicy> 元素
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/runtime/assemblyBinding/publisherPolicy
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/runtime/assemblyBinding/dependentAssembly/publisherPolicy
- http://schemas.microsoft.com/.NetConfiguration/v2.0#publisherPolicy
helpviewer_keywords:
- publisherPolicy element
- container tags, <publisherPolicy> element
- <publisherPolicy> element
ms.assetid: 4613407e-d0a8-4ef2-9f81-a6acb9fdc7d4
ms.openlocfilehash: 35d729d5b195e010a80e7272312f14ac5802001b
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99802431"
---
# <a name="publisherpolicy-element"></a><span data-ttu-id="6bac4-103">\<publisherPolicy> 元素</span><span class="sxs-lookup"><span data-stu-id="6bac4-103">\<publisherPolicy> Element</span></span>

<span data-ttu-id="6bac4-104">指定运行时是否使用发布者策略。</span><span class="sxs-lookup"><span data-stu-id="6bac4-104">Specifies whether the runtime applies publisher policy.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<runtime>**](runtime-element.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<assemblyBinding>**](assemblybinding-element-for-runtime.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<dependentAssembly>**](dependentassembly-element.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<publisherPolicy>**  
  
## <a name="syntax"></a><span data-ttu-id="6bac4-105">语法</span><span class="sxs-lookup"><span data-stu-id="6bac4-105">Syntax</span></span>  
  
```xml  
<publisherPolicy apply="yes|no"/>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="6bac4-106">特性和元素</span><span class="sxs-lookup"><span data-stu-id="6bac4-106">Attributes and Elements</span></span>  

 <span data-ttu-id="6bac4-107">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="6bac4-107">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="6bac4-108">特性</span><span class="sxs-lookup"><span data-stu-id="6bac4-108">Attributes</span></span>  
  
|<span data-ttu-id="6bac4-109">属性</span><span class="sxs-lookup"><span data-stu-id="6bac4-109">Attribute</span></span>|<span data-ttu-id="6bac4-110">说明</span><span class="sxs-lookup"><span data-stu-id="6bac4-110">Description</span></span>|  
|---------------|-----------------|  
|`apply`|<span data-ttu-id="6bac4-111">指定是否应用发布者策略。</span><span class="sxs-lookup"><span data-stu-id="6bac4-111">Specifies whether to apply publisher policy.</span></span>|  
  
## <a name="apply-attribute"></a><span data-ttu-id="6bac4-112">应用属性</span><span class="sxs-lookup"><span data-stu-id="6bac4-112">apply Attribute</span></span>  
  
|<span data-ttu-id="6bac4-113">值</span><span class="sxs-lookup"><span data-stu-id="6bac4-113">Value</span></span>|<span data-ttu-id="6bac4-114">说明</span><span class="sxs-lookup"><span data-stu-id="6bac4-114">Description</span></span>|  
|-----------|-----------------|  
|`yes`|<span data-ttu-id="6bac4-115">应用发布者策略。</span><span class="sxs-lookup"><span data-stu-id="6bac4-115">Applies publisher policy.</span></span> <span data-ttu-id="6bac4-116">此为默认设置。</span><span class="sxs-lookup"><span data-stu-id="6bac4-116">This is the default setting.</span></span>|  
|`no`|<span data-ttu-id="6bac4-117">不应用发布者策略。</span><span class="sxs-lookup"><span data-stu-id="6bac4-117">Does not apply publisher policy.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="6bac4-118">子元素</span><span class="sxs-lookup"><span data-stu-id="6bac4-118">Child Elements</span></span>  

<span data-ttu-id="6bac4-119">无。</span><span class="sxs-lookup"><span data-stu-id="6bac4-119">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="6bac4-120">父元素</span><span class="sxs-lookup"><span data-stu-id="6bac4-120">Parent Elements</span></span>  
  
|<span data-ttu-id="6bac4-121">元素</span><span class="sxs-lookup"><span data-stu-id="6bac4-121">Element</span></span>|<span data-ttu-id="6bac4-122">说明</span><span class="sxs-lookup"><span data-stu-id="6bac4-122">Description</span></span>|  
|-------------|-----------------|  
|`assemblyBinding`|<span data-ttu-id="6bac4-123">包含有关程序集版本重定向和程序集位置的信息。</span><span class="sxs-lookup"><span data-stu-id="6bac4-123">Contains information about assembly version redirection and the locations of assemblies.</span></span>|  
|`configuration`|<span data-ttu-id="6bac4-124">公共语言运行时和 .NET Framework 应用程序所使用的每个配置文件中的根元素。</span><span class="sxs-lookup"><span data-stu-id="6bac4-124">The root element in every configuration file used by the common language runtime and .NET Framework applications.</span></span>|  
|`dependentAssembly`|<span data-ttu-id="6bac4-125">封装每个程序集的绑定策略和程序集位置。</span><span class="sxs-lookup"><span data-stu-id="6bac4-125">Encapsulates binding policy and assembly location for each assembly.</span></span> <span data-ttu-id="6bac4-126">`<dependentAssembly>`为每个程序集使用一个元素。</span><span class="sxs-lookup"><span data-stu-id="6bac4-126">Use one `<dependentAssembly>` element for each assembly.</span></span>|  
|`runtime`|<span data-ttu-id="6bac4-127">包含有关程序集绑定和垃圾回收的信息。</span><span class="sxs-lookup"><span data-stu-id="6bac4-127">Contains information about assembly binding and garbage collection.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="6bac4-128">备注</span><span class="sxs-lookup"><span data-stu-id="6bac4-128">Remarks</span></span>  

 <span data-ttu-id="6bac4-129">当组件供应商发布程序集的新版本时，供应商可以包括发行者策略，以便使用旧版本的应用程序现在使用新版本。</span><span class="sxs-lookup"><span data-stu-id="6bac4-129">When a component vendor releases a new version of an assembly, the vendor can include a publisher policy so applications that use the old version now use the new version.</span></span> <span data-ttu-id="6bac4-130">若要指定是否将发布服务器策略应用于特定程序集，请将该 **\<publisherPolicy>** 元素放在 **\<dependentAssembly>** 元素中。</span><span class="sxs-lookup"><span data-stu-id="6bac4-130">To specify whether to apply publisher policy for a particular assembly, put the **\<publisherPolicy>** element in the **\<dependentAssembly>** element.</span></span>  
  
 <span data-ttu-id="6bac4-131">**Apply** 属性的默认设置为 **"是"**。</span><span class="sxs-lookup"><span data-stu-id="6bac4-131">The default setting for the **apply** attribute is **yes**.</span></span> <span data-ttu-id="6bac4-132">如果将 **apply** 特性设置为 " **否** "，则将替代程序集以前的 **"是"** 设置。</span><span class="sxs-lookup"><span data-stu-id="6bac4-132">Setting the **apply** attribute to **no** overrides any previous **yes** settings for an assembly.</span></span>  
  
 <span data-ttu-id="6bac4-133">若要让应用程序使用 [\<publisherPolicy apply="no"/>](publisherpolicy-element.md) 应用程序配置文件中的元素显式忽略发行者策略，则需要权限。</span><span class="sxs-lookup"><span data-stu-id="6bac4-133">Permission is required for an application to explicitly ignore publisher policy using the [\<publisherPolicy apply="no"/>](publisherpolicy-element.md) element in the application configuration file.</span></span> <span data-ttu-id="6bac4-134">通过在上设置标志来授予权限 <xref:System.Security.Permissions.SecurityPermissionFlag> <xref:System.Security.Permissions.SecurityPermission> 。</span><span class="sxs-lookup"><span data-stu-id="6bac4-134">The permission is granted by setting the <xref:System.Security.Permissions.SecurityPermissionFlag> flag on the <xref:System.Security.Permissions.SecurityPermission>.</span></span> <span data-ttu-id="6bac4-135">有关详细信息，请参阅 [程序集绑定重定向安全权限](../../assembly-binding-redirection-security-permission.md)。</span><span class="sxs-lookup"><span data-stu-id="6bac4-135">For more information, see [Assembly Binding Redirection Security Permission](../../assembly-binding-redirection-security-permission.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="6bac4-136">示例</span><span class="sxs-lookup"><span data-stu-id="6bac4-136">Example</span></span>  

 <span data-ttu-id="6bac4-137">下面的示例将关闭程序集的发布服务器策略 `myAssembly` 。</span><span class="sxs-lookup"><span data-stu-id="6bac4-137">The following example turns off publisher policy for the assembly, `myAssembly`.</span></span>  
  
```xml  
<configuration>  
   <runtime>  
      <assemblyBinding xmlns="urn:schemas-microsoft-com:asm.v1">  
         <dependentAssembly>  
            <assemblyIdentity name="myAssembly"  
                                    publicKeyToken="32ab4ba45e0a69a1"  
                                    culture="neutral" />  
            <publisherPolicy apply="no"/>  
         </dependentAssembly>  
      </assemblyBinding>  
   </runtime>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="6bac4-138">请参阅</span><span class="sxs-lookup"><span data-stu-id="6bac4-138">See also</span></span>

- [<span data-ttu-id="6bac4-139">运行时设置架构</span><span class="sxs-lookup"><span data-stu-id="6bac4-139">Runtime Settings Schema</span></span>](index.md)
- [<span data-ttu-id="6bac4-140">配置文件架构</span><span class="sxs-lookup"><span data-stu-id="6bac4-140">Configuration File Schema</span></span>](../index.md)
- [<span data-ttu-id="6bac4-141">运行时如何定位程序集</span><span class="sxs-lookup"><span data-stu-id="6bac4-141">How the Runtime Locates Assemblies</span></span>](../../../deployment/how-the-runtime-locates-assemblies.md)
- [<span data-ttu-id="6bac4-142">重定向程序集版本</span><span class="sxs-lookup"><span data-stu-id="6bac4-142">Redirecting Assembly Versions</span></span>](../../redirect-assembly-versions.md)
