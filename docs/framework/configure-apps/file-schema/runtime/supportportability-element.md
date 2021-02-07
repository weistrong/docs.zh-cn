---
description: 了解详细信息： <supportPortability> 元素
title: <supportPortability> 元素
ms.date: 03/30/2017
helpviewer_keywords:
- supportPortability element
- <supportPortability> element
ms.assetid: 6453ef66-19b4-41f3-b712-52d0c2abc9ca
ms.openlocfilehash: 5a39f946d5b3841af5f4254cc2f70142aa6c013d
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99754506"
---
# <a name="supportportability-element"></a><span data-ttu-id="343b6-103">\<supportPortability> 元素</span><span class="sxs-lookup"><span data-stu-id="343b6-103">\<supportPortability> Element</span></span>

<span data-ttu-id="343b6-104">通过禁用将程序集视为等效于应用程序可移植性用途的默认行为来指定应用程序可以在两种不同的 .NET Framework 实现中引用同一程序集。</span><span class="sxs-lookup"><span data-stu-id="343b6-104">Specifies that an application can reference the same assembly in two different implementations of the .NET Framework, by disabling the default behavior that treats the assemblies as equivalent for application portability purposes.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<runtime>**](runtime-element.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<assemblyBinding>**](assemblybinding-element-for-runtime.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<supportPortability>**  
  
## <a name="syntax"></a><span data-ttu-id="343b6-105">语法</span><span class="sxs-lookup"><span data-stu-id="343b6-105">Syntax</span></span>  
  
```xml  
<supportPortability PKT="public_key_token" enabled="true|false"/>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="343b6-106">特性和元素</span><span class="sxs-lookup"><span data-stu-id="343b6-106">Attributes and Elements</span></span>  

<span data-ttu-id="343b6-107">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="343b6-107">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="343b6-108">特性</span><span class="sxs-lookup"><span data-stu-id="343b6-108">Attributes</span></span>  
  
|<span data-ttu-id="343b6-109">属性</span><span class="sxs-lookup"><span data-stu-id="343b6-109">Attribute</span></span>|<span data-ttu-id="343b6-110">说明</span><span class="sxs-lookup"><span data-stu-id="343b6-110">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="343b6-111">PKT</span><span class="sxs-lookup"><span data-stu-id="343b6-111">PKT</span></span>|<span data-ttu-id="343b6-112">必需的特性。</span><span class="sxs-lookup"><span data-stu-id="343b6-112">Required attribute.</span></span><br /><br /> <span data-ttu-id="343b6-113">以字符串的形式指定受影响的程序集的公钥标记。</span><span class="sxs-lookup"><span data-stu-id="343b6-113">Specifies the public key token of the affected assembly, as a string.</span></span>|  
|<span data-ttu-id="343b6-114">enabled</span><span class="sxs-lookup"><span data-stu-id="343b6-114">enabled</span></span>|<span data-ttu-id="343b6-115">可选特性。</span><span class="sxs-lookup"><span data-stu-id="343b6-115">Optional attribute.</span></span><br /><br /> <span data-ttu-id="343b6-116">指定是否应启用指定 .NET Framework 程序集的实现之间的可移植性支持。</span><span class="sxs-lookup"><span data-stu-id="343b6-116">Specifies whether support for portability between implementations of the specified .NET Framework assembly should be enabled.</span></span>|  
  
## <a name="enabled-attribute"></a><span data-ttu-id="343b6-117">enabled 特性</span><span class="sxs-lookup"><span data-stu-id="343b6-117">enabled Attribute</span></span>  
  
|<span data-ttu-id="343b6-118">值</span><span class="sxs-lookup"><span data-stu-id="343b6-118">Value</span></span>|<span data-ttu-id="343b6-119">说明</span><span class="sxs-lookup"><span data-stu-id="343b6-119">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="343b6-120">是</span><span class="sxs-lookup"><span data-stu-id="343b6-120">true</span></span>|<span data-ttu-id="343b6-121">支持指定 .NET Framework 程序集的实现之间的可移植性。</span><span class="sxs-lookup"><span data-stu-id="343b6-121">Enable support for portability between implementations of the specified .NET Framework assembly.</span></span> <span data-ttu-id="343b6-122">这是默认设置。</span><span class="sxs-lookup"><span data-stu-id="343b6-122">This is the default.</span></span>|  
|<span data-ttu-id="343b6-123">false</span><span class="sxs-lookup"><span data-stu-id="343b6-123">false</span></span>|<span data-ttu-id="343b6-124">禁用支持指定 .NET Framework 程序集的实现之间的可移植性。</span><span class="sxs-lookup"><span data-stu-id="343b6-124">Disable support for portability between implementations of the specified .NET Framework assembly.</span></span> <span data-ttu-id="343b6-125">这使应用程序可以引用指定程序集的多个实现。</span><span class="sxs-lookup"><span data-stu-id="343b6-125">This enables the application to have references to multiple implementations of the specified assembly.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="343b6-126">子元素</span><span class="sxs-lookup"><span data-stu-id="343b6-126">Child Elements</span></span>  

<span data-ttu-id="343b6-127">无。</span><span class="sxs-lookup"><span data-stu-id="343b6-127">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="343b6-128">父元素</span><span class="sxs-lookup"><span data-stu-id="343b6-128">Parent Elements</span></span>  
  
|<span data-ttu-id="343b6-129">元素</span><span class="sxs-lookup"><span data-stu-id="343b6-129">Element</span></span>|<span data-ttu-id="343b6-130">说明</span><span class="sxs-lookup"><span data-stu-id="343b6-130">Description</span></span>|  
|-------------|-----------------|  
|`configuration`|<span data-ttu-id="343b6-131">公共语言运行时和 .NET Framework 应用程序所使用的每个配置文件中的根元素。</span><span class="sxs-lookup"><span data-stu-id="343b6-131">The root element in every configuration file used by the common language runtime and .NET Framework applications.</span></span>|  
|`runtime`|<span data-ttu-id="343b6-132">包含有关程序集绑定和垃圾回收的信息。</span><span class="sxs-lookup"><span data-stu-id="343b6-132">Contains information about assembly binding and garbage collection.</span></span>|  
|`assemblyBinding`|<span data-ttu-id="343b6-133">包含有关程序集版本重定向和程序集位置的信息。</span><span class="sxs-lookup"><span data-stu-id="343b6-133">Contains information about assembly version redirection and the locations of assemblies.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="343b6-134">备注</span><span class="sxs-lookup"><span data-stu-id="343b6-134">Remarks</span></span>  

<span data-ttu-id="343b6-135">从 .NET Framework 4 开始，将自动为可以使用两种 .NET Framework 实现的应用程序（例如，.NET Framework 实现或 Silverlight 实现的 .NET Framework）提供支持。</span><span class="sxs-lookup"><span data-stu-id="343b6-135">Beginning with the .NET Framework 4, support is automatically provided for applications that can use either of two implementations of the .NET Framework, for example either the .NET Framework implementation or the .NET Framework for Silverlight implementation.</span></span> <span data-ttu-id="343b6-136">特定 .NET Framework 程序集的两个实现被视为等效于程序集联编程序。</span><span class="sxs-lookup"><span data-stu-id="343b6-136">The two implementations of a particular .NET Framework assembly are seen as equivalent by the assembly binder.</span></span> <span data-ttu-id="343b6-137">在少数情况下，此应用程序可移植性功能会导致问题。</span><span class="sxs-lookup"><span data-stu-id="343b6-137">In a few scenarios, this application portability feature causes problems.</span></span> <span data-ttu-id="343b6-138">在这些情况下， `<supportPortability>` 可以使用元素来禁用该功能。</span><span class="sxs-lookup"><span data-stu-id="343b6-138">In those scenarios, the `<supportPortability>` element can be used to disable the feature.</span></span>  
  
<span data-ttu-id="343b6-139">这种情况是必须同时引用特定引用程序集的 Silverlight 实现的 .NET Framework 实现和 .NET Framework 的程序集。</span><span class="sxs-lookup"><span data-stu-id="343b6-139">One such scenario is an assembly that has to reference both the .NET Framework implementation and the .NET Framework for Silverlight implementation of a particular reference assembly.</span></span> <span data-ttu-id="343b6-140">例如，在 Windows Presentation Foundation () WPF 中编写的 XAML 设计器可能需要引用 WPF 桌面实现、设计器的用户界面和 Silverlight 实现中包含的 WPF 子集。</span><span class="sxs-lookup"><span data-stu-id="343b6-140">For example, a XAML designer written in Windows Presentation Foundation (WPF) might need to reference both the WPF Desktop implementation, for the designer's user interface, and the subset of WPF that is included in the Silverlight implementation.</span></span> <span data-ttu-id="343b6-141">默认情况下，单独引用会导致编译器错误，因为程序集绑定将这两个程序集视为等效。</span><span class="sxs-lookup"><span data-stu-id="343b6-141">By default, the separate references cause a compiler error, because assembly binding sees the two assemblies as equivalent.</span></span> <span data-ttu-id="343b6-142">此元素禁用默认行为，并允许编译成功。</span><span class="sxs-lookup"><span data-stu-id="343b6-142">This element disables the default behavior, and allows compilation to succeed.</span></span>  
  
> [!IMPORTANT]
> <span data-ttu-id="343b6-143">为了使编译器能够将信息传递到公共语言运行时的程序集绑定逻辑，必须使用 `/appconfig` 编译器选项来指定包含此元素的 app.config 文件的位置。</span><span class="sxs-lookup"><span data-stu-id="343b6-143">In order for the compiler to pass the information to the common language runtime's assembly-binding logic, you must use the `/appconfig` compiler option to specify the location of the app.config file that contains this element.</span></span>  
  
## <a name="example"></a><span data-ttu-id="343b6-144">示例</span><span class="sxs-lookup"><span data-stu-id="343b6-144">Example</span></span>  

<span data-ttu-id="343b6-145">下面的示例使应用程序能够同时引用在两个实现中都存在的任何 .NET Framework 程序集的 .NET Framework 实现和 Silverlight 实现 .NET Framework。</span><span class="sxs-lookup"><span data-stu-id="343b6-145">The following example enables an application to have references to both the .NET Framework implementation and the .NET Framework for Silverlight implementation of any .NET Framework assembly that exists in both implementations.</span></span> <span data-ttu-id="343b6-146">`/appconfig`必须使用编译器选项指定此 app.config 文件的位置。</span><span class="sxs-lookup"><span data-stu-id="343b6-146">The `/appconfig` compiler option must be used to specify the location of this app.config file.</span></span>  
  
```xml  
<configuration>  
   <runtime>  
      <assemblyBinding>  
         <supportPortability PKT="7cec85d7bea7798e" enable="false"/>  
         <supportPortability PKT="31bf3856ad364e35" enable="false"/>  
      </assemblyBinding>  
   </runtime>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="343b6-147">请参阅</span><span class="sxs-lookup"><span data-stu-id="343b6-147">See also</span></span>

- [<span data-ttu-id="343b6-148">-appconfig（C# 编译器选项）</span><span class="sxs-lookup"><span data-stu-id="343b6-148">-appconfig (C# Compiler Options)</span></span>](../../../../csharp/language-reference/compiler-options/appconfig-compiler-option.md)
- <span data-ttu-id="343b6-149">[.NET Framework 程序集统一概述](/previous-versions/dotnet/netframework-4.0/db7849ey(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="343b6-149">[.NET Framework Assembly Unification Overview](/previous-versions/dotnet/netframework-4.0/db7849ey(v=vs.100))</span></span>
