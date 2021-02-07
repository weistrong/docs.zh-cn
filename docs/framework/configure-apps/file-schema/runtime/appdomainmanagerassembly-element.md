---
description: 了解详细信息： <appDomainManagerAssembly> 元素
title: <appDomainManagerAssembly> 元素
ms.date: 03/30/2017
helpviewer_keywords:
- <appDomainManagerAssembly> element
- appDomainManagerAssembly element
ms.assetid: c7c56e39-a700-44f5-b94e-411bfce339d9
ms.openlocfilehash: fcd461a8c8727679df3974028ddbc4b689c73e5d
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99719300"
---
# <a name="appdomainmanagerassembly-element"></a><span data-ttu-id="a0d80-103">\<appDomainManagerAssembly> 元素</span><span class="sxs-lookup"><span data-stu-id="a0d80-103">\<appDomainManagerAssembly> Element</span></span>

<span data-ttu-id="a0d80-104">指定为过程中的默认应用程序域提供应用程序域管理器的程序集。</span><span class="sxs-lookup"><span data-stu-id="a0d80-104">Specifies the assembly that provides the application domain manager for the default application domain in the process.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<runtime>**](runtime-element.md)\
&nbsp;&nbsp;&nbsp;&nbsp;**\<appDomainManagerAssembly>**  
  
## <a name="syntax"></a><span data-ttu-id="a0d80-105">语法</span><span class="sxs-lookup"><span data-stu-id="a0d80-105">Syntax</span></span>  
  
```xml  
<appDomainManagerAssembly
   value="assembly display name" />  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="a0d80-106">特性和元素</span><span class="sxs-lookup"><span data-stu-id="a0d80-106">Attributes and Elements</span></span>  

 <span data-ttu-id="a0d80-107">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="a0d80-107">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="a0d80-108">特性</span><span class="sxs-lookup"><span data-stu-id="a0d80-108">Attributes</span></span>  
  
|<span data-ttu-id="a0d80-109">属性</span><span class="sxs-lookup"><span data-stu-id="a0d80-109">Attribute</span></span>|<span data-ttu-id="a0d80-110">描述</span><span class="sxs-lookup"><span data-stu-id="a0d80-110">Description</span></span>|  
|---------------|-----------------|  
|`value`|<span data-ttu-id="a0d80-111">必需的特性。</span><span class="sxs-lookup"><span data-stu-id="a0d80-111">Required attribute.</span></span> <span data-ttu-id="a0d80-112">指定为进程中的默认应用程序域提供应用程序域管理器的程序集的显示名称。</span><span class="sxs-lookup"><span data-stu-id="a0d80-112">Specifies the display name of the assembly that provides the application domain manager for the default application domain in the process.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="a0d80-113">子元素</span><span class="sxs-lookup"><span data-stu-id="a0d80-113">Child Elements</span></span>  

 <span data-ttu-id="a0d80-114">无。</span><span class="sxs-lookup"><span data-stu-id="a0d80-114">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="a0d80-115">父元素</span><span class="sxs-lookup"><span data-stu-id="a0d80-115">Parent Elements</span></span>  
  
|<span data-ttu-id="a0d80-116">元素</span><span class="sxs-lookup"><span data-stu-id="a0d80-116">Element</span></span>|<span data-ttu-id="a0d80-117">说明</span><span class="sxs-lookup"><span data-stu-id="a0d80-117">Description</span></span>|  
|-------------|-----------------|  
|`configuration`|<span data-ttu-id="a0d80-118">公共语言运行时和 .NET Framework 应用程序所使用的每个配置文件中的根元素。</span><span class="sxs-lookup"><span data-stu-id="a0d80-118">The root element in every configuration file used by the common language runtime and .NET Framework applications.</span></span>|  
|`runtime`|<span data-ttu-id="a0d80-119">包含有关程序集绑定和垃圾回收的信息。</span><span class="sxs-lookup"><span data-stu-id="a0d80-119">Contains information about assembly binding and garbage collection.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="a0d80-120">备注</span><span class="sxs-lookup"><span data-stu-id="a0d80-120">Remarks</span></span>  

 <span data-ttu-id="a0d80-121">若要指定应用程序域管理器的类型，必须同时指定此元素和 [\<appDomainManagerType>](appdomainmanagertype-element.md) 元素。</span><span class="sxs-lookup"><span data-stu-id="a0d80-121">To specify the type of the application domain manager, you must specify both this element and the [\<appDomainManagerType>](appdomainmanagertype-element.md) element.</span></span> <span data-ttu-id="a0d80-122">如果未指定这些元素中的任何一个，则会忽略另一个。</span><span class="sxs-lookup"><span data-stu-id="a0d80-122">If either of these elements is not specified, the other is ignored.</span></span>  
  
 <span data-ttu-id="a0d80-123">在加载默认应用程序域时， <xref:System.TypeLoadException> 如果指定的程序集不存在，或者如果程序集不包含元素指定的类型，则会引发 [\<appDomainManagerType>](appdomainmanagertype-element.md) ; 并且进程无法启动。</span><span class="sxs-lookup"><span data-stu-id="a0d80-123">When the default application domain is loaded, <xref:System.TypeLoadException> is thrown if the specified assembly does not exist or if the assembly does not contain the type specified by the [\<appDomainManagerType>](appdomainmanagertype-element.md) element; and the process fails to start.</span></span> <span data-ttu-id="a0d80-124">如果找到程序集，但版本信息不匹配， <xref:System.IO.FileLoadException> 则会引发。</span><span class="sxs-lookup"><span data-stu-id="a0d80-124">If the assembly is found but the version information does not match, a <xref:System.IO.FileLoadException> is thrown.</span></span>  
  
 <span data-ttu-id="a0d80-125">指定默认应用程序域的应用程序域管理器类型时，从默认应用程序域创建的其他应用程序域将继承应用程序域管理器类型。</span><span class="sxs-lookup"><span data-stu-id="a0d80-125">When you specify the application domain manager type for the default application domain, other application domains created from the default application domain inherit the application domain manager type.</span></span> <span data-ttu-id="a0d80-126">使用 <xref:System.AppDomainSetup.AppDomainManagerType%2A?displayProperty=nameWithType> 和 <xref:System.AppDomainSetup.AppDomainManagerAssembly%2A?displayProperty=nameWithType> 属性为新的应用程序域指定不同的应用程序域管理器类型。</span><span class="sxs-lookup"><span data-stu-id="a0d80-126">Use the <xref:System.AppDomainSetup.AppDomainManagerType%2A?displayProperty=nameWithType> and <xref:System.AppDomainSetup.AppDomainManagerAssembly%2A?displayProperty=nameWithType> properties to specify a different application domain manager type for a new application domain.</span></span>  
  
 <span data-ttu-id="a0d80-127">指定应用程序域管理器类型要求应用程序具有完全信任。</span><span class="sxs-lookup"><span data-stu-id="a0d80-127">Specifying the application domain manager type requires the application to have full trust.</span></span> <span data-ttu-id="a0d80-128"> (例如，在桌面上运行的应用程序具有完全信任。 ) 如果应用程序不具有完全信任， <xref:System.TypeLoadException> 则会引发。</span><span class="sxs-lookup"><span data-stu-id="a0d80-128">(For example, an application running on the desktop has full trust.) If the application does not have full trust, a <xref:System.TypeLoadException> is thrown.</span></span>  
  
 <span data-ttu-id="a0d80-129">有关程序集显示名称的格式，请参见 <xref:System.Reflection.Assembly.FullName%2A?displayProperty=nameWithType> 属性。</span><span class="sxs-lookup"><span data-stu-id="a0d80-129">For the format of the assembly display name, see the <xref:System.Reflection.Assembly.FullName%2A?displayProperty=nameWithType> property.</span></span>  
  
 <span data-ttu-id="a0d80-130">此配置元素仅在 .NET Framework 4 及更高版本中可用。</span><span class="sxs-lookup"><span data-stu-id="a0d80-130">This configuration element is available only in the .NET Framework 4 and later.</span></span>  
  
## <a name="example"></a><span data-ttu-id="a0d80-131">示例</span><span class="sxs-lookup"><span data-stu-id="a0d80-131">Example</span></span>  

 <span data-ttu-id="a0d80-132">下面的示例演示如何指定进程的默认应用程序域的应用程序域管理器是 `MyMgr` `AdMgrExample` 程序集中的类型。</span><span class="sxs-lookup"><span data-stu-id="a0d80-132">The following example shows how to specify that the application domain manager for the default application domain of a process is the `MyMgr` type in the `AdMgrExample` assembly.</span></span>  
  
```xml  
<configuration>  
   <runtime>  
      <appDomainManagerType value="MyMgr" />  
      <appDomainManagerAssembly
         value="AdMgrExample, Version=1.0.0.0, Culture=neutral, PublicKeyToken=6856bccf150f00b3" />  
   </runtime>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="a0d80-133">请参阅</span><span class="sxs-lookup"><span data-stu-id="a0d80-133">See also</span></span>

- <xref:System.AppDomainSetup.AppDomainManagerType%2A?displayProperty=nameWithType>
- <xref:System.AppDomainSetup.AppDomainManagerAssembly%2A?displayProperty=nameWithType>
- [<span data-ttu-id="a0d80-134">\<appDomainManagerType> 元素</span><span class="sxs-lookup"><span data-stu-id="a0d80-134">\<appDomainManagerType> Element</span></span>](appdomainmanagertype-element.md)
- [<span data-ttu-id="a0d80-135">运行时设置架构</span><span class="sxs-lookup"><span data-stu-id="a0d80-135">Runtime Settings Schema</span></span>](index.md)
- [<span data-ttu-id="a0d80-136">配置文件架构</span><span class="sxs-lookup"><span data-stu-id="a0d80-136">Configuration File Schema</span></span>](../index.md)
- [<span data-ttu-id="a0d80-137">SetAppDomainManagerType 方法</span><span class="sxs-lookup"><span data-stu-id="a0d80-137">SetAppDomainManagerType Method</span></span>](../../../unmanaged-api/hosting/iclrcontrol-setappdomainmanagertype-method.md)
