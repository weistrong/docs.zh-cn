---
description: 了解详细信息： <compilers> 元素
title: <compilers> 元素
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#compilers
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/system.codedom/compilers
helpviewer_keywords:
- compiler configuration elements, <compilers> element
- <compilers> element
- compilers element
ms.assetid: d40fba59-98f9-4783-ae0c-2ebea27ce77b
ms.openlocfilehash: 6ced6bc81bc7d829ccebab50e0a361985c970f5e
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99699163"
---
# <a name="compilers-element"></a><span data-ttu-id="a96cb-103">\<compilers> 元素</span><span class="sxs-lookup"><span data-stu-id="a96cb-103">\<compilers> Element</span></span>

<span data-ttu-id="a96cb-104">编译器配置元素的容器;包含零个或多个 [\<compiler>](compiler-element.md) 元素。</span><span class="sxs-lookup"><span data-stu-id="a96cb-104">Container for compiler configuration elements; contains zero or more [\<compiler>](compiler-element.md) elements.</span></span>  

[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.codedom>**](system-codedom-element.md)\
&nbsp;&nbsp;&nbsp;&nbsp;**\<compilers>**

## <a name="syntax"></a><span data-ttu-id="a96cb-105">语法</span><span class="sxs-lookup"><span data-stu-id="a96cb-105">Syntax</span></span>  
  
```xml  
<compilers>  
  <compiler ... />  
</compilers>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="a96cb-106">特性和元素</span><span class="sxs-lookup"><span data-stu-id="a96cb-106">Attributes and Elements</span></span>  

 <span data-ttu-id="a96cb-107">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="a96cb-107">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="a96cb-108">特性</span><span class="sxs-lookup"><span data-stu-id="a96cb-108">Attributes</span></span>  

 <span data-ttu-id="a96cb-109">无。</span><span class="sxs-lookup"><span data-stu-id="a96cb-109">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="a96cb-110">子元素</span><span class="sxs-lookup"><span data-stu-id="a96cb-110">Child Elements</span></span>  
  
|<span data-ttu-id="a96cb-111">元素</span><span class="sxs-lookup"><span data-stu-id="a96cb-111">Element</span></span>|<span data-ttu-id="a96cb-112">描述</span><span class="sxs-lookup"><span data-stu-id="a96cb-112">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="a96cb-113">\<compiler> 元素</span><span class="sxs-lookup"><span data-stu-id="a96cb-113">\<compiler> Element</span></span>](compiler-element.md)|<span data-ttu-id="a96cb-114">指定语言提供程序的编译器配置属性。</span><span class="sxs-lookup"><span data-stu-id="a96cb-114">Specifies the compiler configuration attributes for a language provider.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="a96cb-115">父元素</span><span class="sxs-lookup"><span data-stu-id="a96cb-115">Parent Elements</span></span>  
  
|<span data-ttu-id="a96cb-116">元素</span><span class="sxs-lookup"><span data-stu-id="a96cb-116">Element</span></span>|<span data-ttu-id="a96cb-117">描述</span><span class="sxs-lookup"><span data-stu-id="a96cb-117">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="a96cb-118">\<configuration> 元素</span><span class="sxs-lookup"><span data-stu-id="a96cb-118">\<configuration> Element</span></span>](../configuration-element.md)|<span data-ttu-id="a96cb-119">公共语言运行时和 .NET Framework 应用程序所使用的每个配置文件中的根元素。</span><span class="sxs-lookup"><span data-stu-id="a96cb-119">The root element in every configuration file used by the common language runtime and .NET Framework applications.</span></span>|  
|[<span data-ttu-id="a96cb-120">\<system.codedom> 元素</span><span class="sxs-lookup"><span data-stu-id="a96cb-120">\<system.codedom> Element</span></span>](system-codedom-element.md)|<span data-ttu-id="a96cb-121">指定可用语言提供程序的编译器配置设置。</span><span class="sxs-lookup"><span data-stu-id="a96cb-121">Specifies compiler configuration settings for available language providers.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="a96cb-122">备注</span><span class="sxs-lookup"><span data-stu-id="a96cb-122">Remarks</span></span>  

 <span data-ttu-id="a96cb-123">[\<compilers>](compilers-element.md)元素包含计算机上的语言提供程序的编译器配置设置。</span><span class="sxs-lookup"><span data-stu-id="a96cb-123">The [\<compilers>](compilers-element.md) element contains the compiler configuration settings for language providers on a computer.</span></span> <span data-ttu-id="a96cb-124">每个 [\<compiler>](compiler-element.md) 元素指定特定语言提供程序的编译器配置特性。</span><span class="sxs-lookup"><span data-stu-id="a96cb-124">Each [\<compiler>](compiler-element.md) element specifies the compiler configuration attributes for a specific language provider.</span></span>  
  
 <span data-ttu-id="a96cb-125">.NET Framework 在计算机配置文件中定义初始编译器和语言提供程序设置 ( # A0) 。</span><span class="sxs-lookup"><span data-stu-id="a96cb-125">The .NET Framework defines the initial compiler and language provider settings in the machine configuration file (Machine.config).</span></span> <span data-ttu-id="a96cb-126">开发人员和编译器供应商可以添加新 <xref:System.CodeDom.Compiler.CodeDomProvider?displayProperty=nameWithType> 实现的配置设置。</span><span class="sxs-lookup"><span data-stu-id="a96cb-126">Developers and compiler vendors can add configuration settings for a new <xref:System.CodeDom.Compiler.CodeDomProvider?displayProperty=nameWithType> implementation.</span></span> <span data-ttu-id="a96cb-127">使用 <xref:System.CodeDom.Compiler.CodeDomProvider.GetAllCompilerInfo%2A?displayProperty=nameWithType> 方法，以编程方式枚举计算机上的语言提供程序和编译器配置设置。</span><span class="sxs-lookup"><span data-stu-id="a96cb-127">Use the <xref:System.CodeDom.Compiler.CodeDomProvider.GetAllCompilerInfo%2A?displayProperty=nameWithType> method to programmatically enumerate language provider and compiler configuration settings on a computer.</span></span>  
  
## <a name="configuration-file"></a><span data-ttu-id="a96cb-128">配置文件</span><span class="sxs-lookup"><span data-stu-id="a96cb-128">Configuration File</span></span>  

 <span data-ttu-id="a96cb-129">此元素可在计算机配置文件和应用程序配置文件中使用。</span><span class="sxs-lookup"><span data-stu-id="a96cb-129">This element can be used in the machine configuration file and the application configuration file.</span></span>  
  
## <a name="example"></a><span data-ttu-id="a96cb-130">示例</span><span class="sxs-lookup"><span data-stu-id="a96cb-130">Example</span></span>  

 <span data-ttu-id="a96cb-131">以下示例说明典型的编译器配置元素。</span><span class="sxs-lookup"><span data-stu-id="a96cb-131">The following example illustrates a typical compiler configuration element.</span></span>  
  
```xml  
<configuration>  
   <system.codedom>  
     <compilers>  
       <!-- zero or more compiler elements -->  
       <compiler
          language="c#;cs;csharp"
          extension=".cs"  
          type="Microsoft.CSharp.CSharpCodeProvider, System, Version=1.0.5000.0, Culture=neutral, PublicKeyToken=b77a5c561934e089"  
          compilerOptions=""
          warningLevel="1" />  
     </compilers>  
   </system.codedom>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="a96cb-132">请参阅</span><span class="sxs-lookup"><span data-stu-id="a96cb-132">See also</span></span>

- <xref:System.CodeDom.Compiler.CompilerInfo>
- <xref:System.CodeDom.Compiler.CodeDomProvider>
- [<span data-ttu-id="a96cb-133">配置文件架构</span><span class="sxs-lookup"><span data-stu-id="a96cb-133">Configuration File Schema</span></span>](../index.md)
- [<span data-ttu-id="a96cb-134">编译器和语言提供程序设置架构</span><span class="sxs-lookup"><span data-stu-id="a96cb-134">Compiler and Language Provider Settings Schema</span></span>](index.md)
- [<span data-ttu-id="a96cb-135">\<compiler> 元素</span><span class="sxs-lookup"><span data-stu-id="a96cb-135">\<compiler> Element</span></span>](compiler-element.md)
