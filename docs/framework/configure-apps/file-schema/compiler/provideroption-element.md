---
description: 了解详细信息： <providerOption> 元素
title: <providerOption> 元素
ms.date: 03/30/2017
f1_keywords:
- provideroption
helpviewer_keywords:
- <provideroption> element
- providerOptions
- provideroption element
ms.assetid: 014f2e0b-c0b5-4fc4-92d3-73f02978b2a1
ms.openlocfilehash: 1fdca58830e8563ef28cbca28857127252928fd4
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99699033"
---
# <a name="provideroption-element"></a><span data-ttu-id="ee1a3-103">\<providerOption> 元素</span><span class="sxs-lookup"><span data-stu-id="ee1a3-103">\<providerOption> Element</span></span>

<span data-ttu-id="ee1a3-104">指定语言提供程序的编译器版本特性。</span><span class="sxs-lookup"><span data-stu-id="ee1a3-104">Specifies the compiler version attributes for a language provider.</span></span>  

[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.codedom>**](system-codedom-element.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<compilers>**](compilers-element.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<compiler>**](compiler-element.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<providerOption>**

## <a name="syntax"></a><span data-ttu-id="ee1a3-105">语法</span><span class="sxs-lookup"><span data-stu-id="ee1a3-105">Syntax</span></span>  
  
```xml  
<providerOption  
  name="option-name"  
  value="option-value"  
/>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="ee1a3-106">特性和元素</span><span class="sxs-lookup"><span data-stu-id="ee1a3-106">Attributes and Elements</span></span>  

 <span data-ttu-id="ee1a3-107">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="ee1a3-107">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="ee1a3-108">特性</span><span class="sxs-lookup"><span data-stu-id="ee1a3-108">Attributes</span></span>  
  
|<span data-ttu-id="ee1a3-109">属性</span><span class="sxs-lookup"><span data-stu-id="ee1a3-109">Attribute</span></span>|<span data-ttu-id="ee1a3-110">描述</span><span class="sxs-lookup"><span data-stu-id="ee1a3-110">Description</span></span>|  
|---------------|-----------------|  
|`name`|<span data-ttu-id="ee1a3-111">必需的特性。</span><span class="sxs-lookup"><span data-stu-id="ee1a3-111">Required attribute.</span></span><br /><br /> <span data-ttu-id="ee1a3-112">指定选项的名称;例如 "CompilerVersion"。</span><span class="sxs-lookup"><span data-stu-id="ee1a3-112">Specifies the name of the option; for example, "CompilerVersion".</span></span>|  
|`value`|<span data-ttu-id="ee1a3-113">必需的特性。</span><span class="sxs-lookup"><span data-stu-id="ee1a3-113">Required attribute.</span></span><br /><br /> <span data-ttu-id="ee1a3-114">指定选项的值;例如，"v 3.5"。</span><span class="sxs-lookup"><span data-stu-id="ee1a3-114">Specifies the value for the option; for example, "v3.5".</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="ee1a3-115">子元素</span><span class="sxs-lookup"><span data-stu-id="ee1a3-115">Child Elements</span></span>  

 <span data-ttu-id="ee1a3-116">无。</span><span class="sxs-lookup"><span data-stu-id="ee1a3-116">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="ee1a3-117">父元素</span><span class="sxs-lookup"><span data-stu-id="ee1a3-117">Parent Elements</span></span>  
  
|<span data-ttu-id="ee1a3-118">元素</span><span class="sxs-lookup"><span data-stu-id="ee1a3-118">Element</span></span>|<span data-ttu-id="ee1a3-119">描述</span><span class="sxs-lookup"><span data-stu-id="ee1a3-119">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="ee1a3-120">\<configuration> 元素</span><span class="sxs-lookup"><span data-stu-id="ee1a3-120">\<configuration> Element</span></span>](../configuration-element.md)|<span data-ttu-id="ee1a3-121">公共语言运行库和 .NET Framework 应用程序所使用的每个配置文件中的根元素。</span><span class="sxs-lookup"><span data-stu-id="ee1a3-121">The root element in every configuration file that is used by the common language runtime and .NET Framework applications.</span></span>|  
|[<span data-ttu-id="ee1a3-122">\<system.codedom> 元素</span><span class="sxs-lookup"><span data-stu-id="ee1a3-122">\<system.codedom> Element</span></span>](system-codedom-element.md)|<span data-ttu-id="ee1a3-123">指定可用语言提供程序的编译器配置设置。</span><span class="sxs-lookup"><span data-stu-id="ee1a3-123">Specifies compiler configuration settings for available language providers.</span></span>|  
|[<span data-ttu-id="ee1a3-124">\<compilers> 元素</span><span class="sxs-lookup"><span data-stu-id="ee1a3-124">\<compilers> Element</span></span>](compilers-element.md)|<span data-ttu-id="ee1a3-125">编译器配置元素的容器;包含零个或多个 `<compiler>` 元素。</span><span class="sxs-lookup"><span data-stu-id="ee1a3-125">Container for compiler configuration elements; contains zero or more `<compiler>` elements.</span></span>|  
|[<span data-ttu-id="ee1a3-126">\<compiler> 元素</span><span class="sxs-lookup"><span data-stu-id="ee1a3-126">\<compiler> Element</span></span>](compiler-element.md)|<span data-ttu-id="ee1a3-127">指定语言提供程序的编译器配置属性。</span><span class="sxs-lookup"><span data-stu-id="ee1a3-127">Specifies the compiler configuration attributes for a language provider.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="ee1a3-128">备注</span><span class="sxs-lookup"><span data-stu-id="ee1a3-128">Remarks</span></span>  

 <span data-ttu-id="ee1a3-129">在 .NET Framework 版本3.5 中，代码文档对象模型 (CodeDOM) 代码提供程序可以使用元素支持特定于提供程序的选项 `<providerOption>` 。</span><span class="sxs-lookup"><span data-stu-id="ee1a3-129">In the .NET Framework version 3.5, Code Document Object Model (CodeDOM) code providers can support provider-specific options by using the `<providerOption>` element.</span></span>  
  
 <span data-ttu-id="ee1a3-130">3.5 .NET Framework 包括更新的 .NET Framework 2.0 程序集，并提供包含新类型的3.5 版本的新程序集。</span><span class="sxs-lookup"><span data-stu-id="ee1a3-130">The .NET Framework 3.5 includes updated .NET Framework 2.0 assemblies and provides new version 3.5 assemblies that contain new types.</span></span> <span data-ttu-id="ee1a3-131">Microsoft c # 和 Visual Basic 代码提供程序包含在 .NET Framework 2.0 程序集中，但已更新为支持版本3.5 编译器。</span><span class="sxs-lookup"><span data-stu-id="ee1a3-131">The Microsoft C# and Visual Basic code providers are contained in .NET Framework 2.0 assemblies but have been updated to support version 3.5 compilers.</span></span> <span data-ttu-id="ee1a3-132">默认情况下，更新的代码提供程序为版本2.0 编译器生成代码。</span><span class="sxs-lookup"><span data-stu-id="ee1a3-132">By default, the updated code providers generate code for version 2.0 compilers.</span></span> <span data-ttu-id="ee1a3-133">您可以使用 `<providerOption>` 元素将目标编译器版本更改为3.5。</span><span class="sxs-lookup"><span data-stu-id="ee1a3-133">You can use the `<providerOption>` element to change the target compiler version to 3.5.</span></span> <span data-ttu-id="ee1a3-134">为此，请将属性指定为 "CompilerVersion" `name` ，并为属性指定 "v 3.5" `value` 。</span><span class="sxs-lookup"><span data-stu-id="ee1a3-134">To do this, specify "CompilerVersion" for the `name` attribute and "v3.5" for the `value` attribute.</span></span> <span data-ttu-id="ee1a3-135">必须在版本号前面加上小写 "v"。</span><span class="sxs-lookup"><span data-stu-id="ee1a3-135">You must precede the version number with a lower-case "v".</span></span>  
  
 <span data-ttu-id="ee1a3-136">可以通过将 `<providerOption>` 元素添加到 .NET Framework 2.0 Machine.config 或根 Web.config 文件来使版本规范成为全局版本。</span><span class="sxs-lookup"><span data-stu-id="ee1a3-136">You can make the version specification global by adding the `<providerOption>` element to the .NET Framework 2.0 Machine.config or root Web.config file.</span></span> <span data-ttu-id="ee1a3-137">如果将 Machine.config 文件中的默认编译器版本更新为3.5，则可以通过使用 `<providerOption>` 应用程序配置文件中的元素，将其更改为每个应用程序2.0。</span><span class="sxs-lookup"><span data-stu-id="ee1a3-137">If you update the default compiler version to 3.5 in the Machine.config file, you can change it back to 2.0 on a per-application basis by using the `<providerOption>` element in the application configuration file.</span></span>  
  
 <span data-ttu-id="ee1a3-138">CodeDOM 代码提供程序实现者可以通过提供采用类型为的参数的构造函数来处理自定义选项 `providerOptions` <xref:System.Collections.Generic.IDictionary%602> 。</span><span class="sxs-lookup"><span data-stu-id="ee1a3-138">CodeDOM code provider implementers can process custom options by providing a constructor that takes a `providerOptions` parameter of type <xref:System.Collections.Generic.IDictionary%602>.</span></span>  
  
## <a name="example"></a><span data-ttu-id="ee1a3-139">示例</span><span class="sxs-lookup"><span data-stu-id="ee1a3-139">Example</span></span>  

 <span data-ttu-id="ee1a3-140">下面的示例演示如何指定应使用 c # 代码提供程序的3.5 版。</span><span class="sxs-lookup"><span data-stu-id="ee1a3-140">The following example demonstrates how to specify that version 3.5 of the C# code provider should be used.</span></span>  
  
```xml  
<configuration>  
  <system.codedom>  
    <compilers>  
      <!-- zero or more compiler elements -->  
      <compiler  
        language="c#;cs;csharp"  
        extension=".cs"  
        type="Microsoft.CSharp.CSharpCodeProvider, System,
          Version=2.0.3600.0, Culture=neutral,
          PublicKeyToken=b77a5c561934e089"  
        compilerOptions="/optimize"  
        warningLevel="1" >  
          <providerOption  
            name="CompilerVersion"  
            value="v3.5" />  
      </compiler>  
    </compilers>  
  </system.codedom>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="ee1a3-141">请参阅</span><span class="sxs-lookup"><span data-stu-id="ee1a3-141">See also</span></span>

- <xref:System.CodeDom.Compiler.CompilerInfo>
- <xref:System.CodeDom.Compiler.CodeDomProvider>
- [<span data-ttu-id="ee1a3-142">配置文件架构</span><span class="sxs-lookup"><span data-stu-id="ee1a3-142">Configuration File Schema</span></span>](../index.md)
- [<span data-ttu-id="ee1a3-143">\<compilers> 元素</span><span class="sxs-lookup"><span data-stu-id="ee1a3-143">\<compilers> Element</span></span>](compilers-element.md)
- [<span data-ttu-id="ee1a3-144">指定完全限定的类型名称</span><span class="sxs-lookup"><span data-stu-id="ee1a3-144">Specifying Fully Qualified Type Names</span></span>](../../../reflection-and-codedom/specifying-fully-qualified-type-names.md)
- <span data-ttu-id="ee1a3-145">[compilation 的 compilers 的 compiler 元素（ASP.NET 设置架构）](/previous-versions/dotnet/netframework-4.0/a15ebt6c(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="ee1a3-145">[compiler Element for compilers for compilation (ASP.NET Settings Schema)](/previous-versions/dotnet/netframework-4.0/a15ebt6c(v=vs.100))</span></span>
