---
description: '了解详细信息： <TypeInstantiation> 元素 ( .NET Native) '
title: <TypeInstantiation>元素 (.NET Native)
ms.date: 03/30/2017
ms.assetid: a5eada64-075b-4162-9655-ded84e4681f2
ms.openlocfilehash: 8939767e016283ea525fbd74554fe30b1cca952a
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99801925"
---
# <a name="typeinstantiation-element-net-native"></a><span data-ttu-id="8c563-103">\<TypeInstantiation>元素 (.NET Native)</span><span class="sxs-lookup"><span data-stu-id="8c563-103">\<TypeInstantiation> Element (.NET Native)</span></span>

<span data-ttu-id="8c563-104">将运行时反射策略应用到一个构造泛型类型。</span><span class="sxs-lookup"><span data-stu-id="8c563-104">Applies runtime reflection policy to a constructed generic type.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="8c563-105">语法</span><span class="sxs-lookup"><span data-stu-id="8c563-105">Syntax</span></span>  
  
```xml  
<TypeInstantiation Name="type_name"  
                   Arguments="type_arguments"  
                   Activate="policy_type"  
                   Browse="policy_type"  
                   Dynamic="policy_type"  
                   Serialize="policy_type"  
                   DataContractSerializer="policy_setting"  
                   DataContractJsonSerializer="policy_setting"  
                   XmlSerializer="policy_setting"  
                   MarshalObject="policy_setting"  
                   MarshalDelegate="policy_setting"  
                   MarshalStructure="policy_setting" />  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="8c563-106">特性和元素</span><span class="sxs-lookup"><span data-stu-id="8c563-106">Attributes and Elements</span></span>  

 <span data-ttu-id="8c563-107">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="8c563-107">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="8c563-108">特性</span><span class="sxs-lookup"><span data-stu-id="8c563-108">Attributes</span></span>  
  
|<span data-ttu-id="8c563-109">属性</span><span class="sxs-lookup"><span data-stu-id="8c563-109">Attribute</span></span>|<span data-ttu-id="8c563-110">属性类型</span><span class="sxs-lookup"><span data-stu-id="8c563-110">Attribute type</span></span>|<span data-ttu-id="8c563-111">说明</span><span class="sxs-lookup"><span data-stu-id="8c563-111">Description</span></span>|  
|---------------|--------------------|-----------------|  
|`Name`|<span data-ttu-id="8c563-112">常规</span><span class="sxs-lookup"><span data-stu-id="8c563-112">General</span></span>|<span data-ttu-id="8c563-113">必需的特性。</span><span class="sxs-lookup"><span data-stu-id="8c563-113">Required attribute.</span></span> <span data-ttu-id="8c563-114">指定类型名称。</span><span class="sxs-lookup"><span data-stu-id="8c563-114">Specifies the type name.</span></span>|  
|`Arguments`|<span data-ttu-id="8c563-115">常规</span><span class="sxs-lookup"><span data-stu-id="8c563-115">General</span></span>|<span data-ttu-id="8c563-116">必需的特性。</span><span class="sxs-lookup"><span data-stu-id="8c563-116">Required attribute.</span></span> <span data-ttu-id="8c563-117">指定泛型类型参数。</span><span class="sxs-lookup"><span data-stu-id="8c563-117">Specifies the generic type arguments.</span></span> <span data-ttu-id="8c563-118">如果存在多个自变量，它们之间用逗号分割。</span><span class="sxs-lookup"><span data-stu-id="8c563-118">If multiple arguments are present, they are separated by commas.</span></span>|  
|`Activate`|<span data-ttu-id="8c563-119">反射</span><span class="sxs-lookup"><span data-stu-id="8c563-119">Reflection</span></span>|<span data-ttu-id="8c563-120">可选特性。</span><span class="sxs-lookup"><span data-stu-id="8c563-120">Optional attribute.</span></span> <span data-ttu-id="8c563-121">控制运行时对构造函数的访问，以启用实例激活。</span><span class="sxs-lookup"><span data-stu-id="8c563-121">Controls runtime access to constructors to enable activation of instances.</span></span>|  
|`Browse`|<span data-ttu-id="8c563-122">反射</span><span class="sxs-lookup"><span data-stu-id="8c563-122">Reflection</span></span>|<span data-ttu-id="8c563-123">可选特性。</span><span class="sxs-lookup"><span data-stu-id="8c563-123">Optional attribute.</span></span> <span data-ttu-id="8c563-124">控制对有关程序元素信息的查询，但并不启用任何运行时访问。</span><span class="sxs-lookup"><span data-stu-id="8c563-124">Controls querying for information about program elements, but does not enable any runtime access.</span></span>|  
|`Dynamic`|<span data-ttu-id="8c563-125">反射</span><span class="sxs-lookup"><span data-stu-id="8c563-125">Reflection</span></span>|<span data-ttu-id="8c563-126">可选特性。</span><span class="sxs-lookup"><span data-stu-id="8c563-126">Optional attribute.</span></span> <span data-ttu-id="8c563-127">控制运行时对所有类型成员的访问，包括构造函数、方法、字段、属性和事件，以启用动态编程。</span><span class="sxs-lookup"><span data-stu-id="8c563-127">Controls runtime access to all type members, including constructors, methods, fields, properties, and events, to enable dynamic programming.</span></span>|  
|`Serialize`|<span data-ttu-id="8c563-128">序列化</span><span class="sxs-lookup"><span data-stu-id="8c563-128">Serialization</span></span>|<span data-ttu-id="8c563-129">可选特性。</span><span class="sxs-lookup"><span data-stu-id="8c563-129">Optional attribute.</span></span> <span data-ttu-id="8c563-130">控制运行时对构造函数、字段和属性的访问，使类型实例得到序列化和反序列化处理，这是通过库进行的，例如 Newtonsoft JSON 序列化程序。</span><span class="sxs-lookup"><span data-stu-id="8c563-130">Controls runtime access to constructors, fields, and properties, to enable type instances to be serialized and deserialized by libraries such as the Newtonsoft JSON serializer.</span></span>|  
|`DataContractSerializer`|<span data-ttu-id="8c563-131">序列化</span><span class="sxs-lookup"><span data-stu-id="8c563-131">Serialization</span></span>|<span data-ttu-id="8c563-132">可选特性。</span><span class="sxs-lookup"><span data-stu-id="8c563-132">Optional attribute.</span></span> <span data-ttu-id="8c563-133">控制使用 <xref:System.Runtime.Serialization.DataContractSerializer?displayProperty=nameWithType> 类的序列化策略。</span><span class="sxs-lookup"><span data-stu-id="8c563-133">Controls policy for serialization that uses the <xref:System.Runtime.Serialization.DataContractSerializer?displayProperty=nameWithType> class.</span></span>|  
|`DataContractJsonSerializer`|<span data-ttu-id="8c563-134">序列化</span><span class="sxs-lookup"><span data-stu-id="8c563-134">Serialization</span></span>|<span data-ttu-id="8c563-135">可选特性。</span><span class="sxs-lookup"><span data-stu-id="8c563-135">Optional attribute.</span></span> <span data-ttu-id="8c563-136">控制使用 <xref:System.Runtime.Serialization.Json.DataContractJsonSerializer?displayProperty=nameWithType> 类的 JSON 序列化策略。</span><span class="sxs-lookup"><span data-stu-id="8c563-136">Controls policy for JSON serialization that uses the <xref:System.Runtime.Serialization.Json.DataContractJsonSerializer?displayProperty=nameWithType> class.</span></span>|  
|`XmlSerializer`|<span data-ttu-id="8c563-137">序列化</span><span class="sxs-lookup"><span data-stu-id="8c563-137">Serialization</span></span>|<span data-ttu-id="8c563-138">可选特性。</span><span class="sxs-lookup"><span data-stu-id="8c563-138">Optional attribute.</span></span> <span data-ttu-id="8c563-139">控制使用 <xref:System.Xml.Serialization.XmlSerializer?displayProperty=nameWithType> 类的 XML 序列化策略。</span><span class="sxs-lookup"><span data-stu-id="8c563-139">Controls policy for XML serialization that uses the <xref:System.Xml.Serialization.XmlSerializer?displayProperty=nameWithType> class.</span></span>|  
|`MarshalObject`|<span data-ttu-id="8c563-140">Interop</span><span class="sxs-lookup"><span data-stu-id="8c563-140">Interop</span></span>|<span data-ttu-id="8c563-141">可选特性。</span><span class="sxs-lookup"><span data-stu-id="8c563-141">Optional attribute.</span></span> <span data-ttu-id="8c563-142">控制封送引用类型到 Windows 运行时和 COM 的策略。</span><span class="sxs-lookup"><span data-stu-id="8c563-142">Controls policy for marshaling reference types to Windows Runtime and COM.</span></span>|  
|`MarshalDelegate`|<span data-ttu-id="8c563-143">Interop</span><span class="sxs-lookup"><span data-stu-id="8c563-143">Interop</span></span>|<span data-ttu-id="8c563-144">可选特性。</span><span class="sxs-lookup"><span data-stu-id="8c563-144">Optional attribute.</span></span> <span data-ttu-id="8c563-145">控制将委托类型作为函数指针封送到本机代码的策略。</span><span class="sxs-lookup"><span data-stu-id="8c563-145">Controls policy for marshaling delegate types as function pointers to native code.</span></span>|  
|`MarshalStructure`|<span data-ttu-id="8c563-146">Interop</span><span class="sxs-lookup"><span data-stu-id="8c563-146">Interop</span></span>|<span data-ttu-id="8c563-147">可选特性。</span><span class="sxs-lookup"><span data-stu-id="8c563-147">Optional attribute.</span></span> <span data-ttu-id="8c563-148">控制封送结构到本机代码的策略。</span><span class="sxs-lookup"><span data-stu-id="8c563-148">Controls policy for marshaling structures to native code.</span></span>|  
  
## <a name="name-attribute"></a><span data-ttu-id="8c563-149">Name 特性</span><span class="sxs-lookup"><span data-stu-id="8c563-149">Name attribute</span></span>  
  
|<span data-ttu-id="8c563-150">值</span><span class="sxs-lookup"><span data-stu-id="8c563-150">Value</span></span>|<span data-ttu-id="8c563-151">说明</span><span class="sxs-lookup"><span data-stu-id="8c563-151">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="8c563-152">type_name</span><span class="sxs-lookup"><span data-stu-id="8c563-152">*type_name*</span></span>|<span data-ttu-id="8c563-153">类型名称。</span><span class="sxs-lookup"><span data-stu-id="8c563-153">The type name.</span></span> <span data-ttu-id="8c563-154">如果此 `<TypeInstantiation>` 元素是 [\<Namespace>](namespace-element-net-native.md) 元素、元素或另一个元素的子元素，则 [\<Type>](type-element-net-native.md) `<TypeInstantiation>` *type_name* 可以指定该类型的名称，而无需命名空间。</span><span class="sxs-lookup"><span data-stu-id="8c563-154">If this `<TypeInstantiation>` element is the child of a [\<Namespace>](namespace-element-net-native.md) element, a [\<Type>](type-element-net-native.md) element, or another `<TypeInstantiation>` element, *type_name* can specify the name of the type without its namespace.</span></span> <span data-ttu-id="8c563-155">否则，type_name 必须包含完全限定的类型名称。</span><span class="sxs-lookup"><span data-stu-id="8c563-155">Otherwise, *type_name* must include the fully qualified type name.</span></span> <span data-ttu-id="8c563-156">该类型名称没有经过修饰。</span><span class="sxs-lookup"><span data-stu-id="8c563-156">The type name isn't decorated.</span></span> <span data-ttu-id="8c563-157">例如，对于一个 <xref:System.Collections.Generic.List%601?displayProperty=nameWithType> 对象，`<TypeInstantiation>` 元素可能显示如下：</span><span class="sxs-lookup"><span data-stu-id="8c563-157">For example, for a <xref:System.Collections.Generic.List%601?displayProperty=nameWithType> object, the `<TypeInstantiation>` element might appear as follows:</span></span><br /><br /> `\<TypeInstantiation Name=System.Collections.Generic.List Dynamic="Required Public" />`|  
  
## <a name="arguments-attribute"></a><span data-ttu-id="8c563-158">自变量特性</span><span class="sxs-lookup"><span data-stu-id="8c563-158">Arguments attribute</span></span>  
  
|<span data-ttu-id="8c563-159">值</span><span class="sxs-lookup"><span data-stu-id="8c563-159">Value</span></span>|<span data-ttu-id="8c563-160">说明</span><span class="sxs-lookup"><span data-stu-id="8c563-160">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="8c563-161">type_argument</span><span class="sxs-lookup"><span data-stu-id="8c563-161">*type_argument*</span></span>|<span data-ttu-id="8c563-162">指定泛型类型参数。</span><span class="sxs-lookup"><span data-stu-id="8c563-162">Specifies the generic type arguments.</span></span> <span data-ttu-id="8c563-163">如果存在多个自变量，它们之间用逗号分割。</span><span class="sxs-lookup"><span data-stu-id="8c563-163">If multiple arguments are present, they are separated by commas.</span></span> <span data-ttu-id="8c563-164">每个自变量必须包含一个完全限定的类型名称。</span><span class="sxs-lookup"><span data-stu-id="8c563-164">Each argument must consist of the fully qualified type name.</span></span>|  
  
## <a name="all-other-attributes"></a><span data-ttu-id="8c563-165">所有其他特性</span><span class="sxs-lookup"><span data-stu-id="8c563-165">All other attributes</span></span>  
  
|<span data-ttu-id="8c563-166">值</span><span class="sxs-lookup"><span data-stu-id="8c563-166">Value</span></span>|<span data-ttu-id="8c563-167">说明</span><span class="sxs-lookup"><span data-stu-id="8c563-167">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="8c563-168">*策略_设置*</span><span class="sxs-lookup"><span data-stu-id="8c563-168">*policy_setting*</span></span>|<span data-ttu-id="8c563-169">该设置将应用到这个构造泛型类型的策略类型。</span><span class="sxs-lookup"><span data-stu-id="8c563-169">The setting to apply to this policy type for the constructed generic type.</span></span> <span data-ttu-id="8c563-170">可能值为 `All`、`Auto`、`Excluded`、`Public`、`PublicAndInternal`、`Required Public`、`Required PublicAndInternal` 以及 `Required All`。</span><span class="sxs-lookup"><span data-stu-id="8c563-170">Possible values are `All`, `Auto`, `Excluded`, `Public`, `PublicAndInternal`, `Required Public`, `Required PublicAndInternal`, and `Required All`.</span></span> <span data-ttu-id="8c563-171">有关详细信息，请参阅[运行时指令策略设置](runtime-directive-policy-settings.md)。</span><span class="sxs-lookup"><span data-stu-id="8c563-171">For more information, see [Runtime Directive Policy Settings](runtime-directive-policy-settings.md).</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="8c563-172">子元素</span><span class="sxs-lookup"><span data-stu-id="8c563-172">Child Elements</span></span>  
  
|<span data-ttu-id="8c563-173">元素</span><span class="sxs-lookup"><span data-stu-id="8c563-173">Element</span></span>|<span data-ttu-id="8c563-174">说明</span><span class="sxs-lookup"><span data-stu-id="8c563-174">Description</span></span>|  
|-------------|-----------------|  
|[\<Event>](event-element-net-native.md)|<span data-ttu-id="8c563-175">将反射策略应用到属于这种类型的一个事件。</span><span class="sxs-lookup"><span data-stu-id="8c563-175">Applies reflection policy to an event belonging to this type.</span></span>|  
|[\<Field>](field-element-net-native.md)|<span data-ttu-id="8c563-176">将反射策略应用到属于这种类型的一个字段。</span><span class="sxs-lookup"><span data-stu-id="8c563-176">Applies reflection policy to a field belonging to this type.</span></span>|  
|[\<ImpliesType>](impliestype-element-net-native.md)|<span data-ttu-id="8c563-177">如果该策略已应用到以包含 `<TypeInstantiation>` 元素为代表的类型，将该策略应用到一个类型。</span><span class="sxs-lookup"><span data-stu-id="8c563-177">Applies policy to a type, if that policy has been applied to the type represented by the containing `<TypeInstantiation>` element.</span></span>|  
|[\<Method>](method-element-net-native.md)|<span data-ttu-id="8c563-178">将反射策略应用到属于这种类型的一个方法。</span><span class="sxs-lookup"><span data-stu-id="8c563-178">Applies reflection policy to a method belonging to this type.</span></span>|  
|[\<MethodInstantiation>](methodinstantiation-element-net-native.md)|<span data-ttu-id="8c563-179">将反射策略应用到属于这种类型的一个构造泛型方法。</span><span class="sxs-lookup"><span data-stu-id="8c563-179">Applies reflection policy to a constructed generic method belonging to this type.</span></span>|  
|[\<Property>](property-element-net-native.md)|<span data-ttu-id="8c563-180">将反射策略应用到属于这种类型的一个属性。</span><span class="sxs-lookup"><span data-stu-id="8c563-180">Applies reflection policy to a property belonging to this type.</span></span>|  
|[\<Type>](type-element-net-native.md)|<span data-ttu-id="8c563-181">将反射策略应用到一个嵌套类型。</span><span class="sxs-lookup"><span data-stu-id="8c563-181">Applies reflection policy to a nested type.</span></span>|  
|`<TypeInstantiation>`|<span data-ttu-id="8c563-182">将反射策略应用到一个嵌套的构造泛型类型。</span><span class="sxs-lookup"><span data-stu-id="8c563-182">Applies reflection policy to a nested constructed generic type.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="8c563-183">父元素</span><span class="sxs-lookup"><span data-stu-id="8c563-183">Parent Elements</span></span>  
  
|<span data-ttu-id="8c563-184">元素</span><span class="sxs-lookup"><span data-stu-id="8c563-184">Element</span></span>|<span data-ttu-id="8c563-185">说明</span><span class="sxs-lookup"><span data-stu-id="8c563-185">Description</span></span>|  
|-------------|-----------------|  
|[\<Application>](application-element-net-native.md)|<span data-ttu-id="8c563-186">作为应用程序范围内的类型和元数据可以反应在运行时间的类型成员的容器而服务。</span><span class="sxs-lookup"><span data-stu-id="8c563-186">Serves as a container for application-wide types and type members whose metadata is available for reflection at run time.</span></span>|  
|[\<Assembly>](assembly-element-net-native.md)|<span data-ttu-id="8c563-187">将反射策略应用到指定程序集中的所有类型。</span><span class="sxs-lookup"><span data-stu-id="8c563-187">Applies reflection policy to all the types in a specified assembly.</span></span>|  
|[\<Library>](library-element-net-native.md)|<span data-ttu-id="8c563-188">定义包含元数据在运行时间可以用于反射的类型和类型成员的程序集。</span><span class="sxs-lookup"><span data-stu-id="8c563-188">Defines the assembly that contains types and type members whose metadata is available for reflection at run time.</span></span>|  
|[\<Namespace>](namespace-element-net-native.md)|<span data-ttu-id="8c563-189">将反射策略应用到命名空间中的所有类型。</span><span class="sxs-lookup"><span data-stu-id="8c563-189">Applies reflection policy to all the types in a namespace.</span></span>|  
|[\<Type>](type-element-net-native.md)|<span data-ttu-id="8c563-190">将反射策略应用到一种类型及其所有成员。</span><span class="sxs-lookup"><span data-stu-id="8c563-190">Applies reflection policy to a type and all its members.</span></span>|  
|`<TypeInstantiation>`|<span data-ttu-id="8c563-191">将反射策略应用到一种构造泛型类型及其所有成员。</span><span class="sxs-lookup"><span data-stu-id="8c563-191">Applies reflection policy to a constructed generic type and all its members.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="8c563-192">备注</span><span class="sxs-lookup"><span data-stu-id="8c563-192">Remarks</span></span>  

 <span data-ttu-id="8c563-193">反射、序列化和互操作特性都是可选项。</span><span class="sxs-lookup"><span data-stu-id="8c563-193">The reflection, serialization, and interop attributes are all optional.</span></span> <span data-ttu-id="8c563-194">然而，至少一个特性必须存在。</span><span class="sxs-lookup"><span data-stu-id="8c563-194">However, at least one must be present.</span></span>  
  
 <span data-ttu-id="8c563-195">如果 `<TypeInstantiation>` 元素是 [\<Assembly>](assembly-element-net-native.md) 、 [\<Namespace>](namespace-element-net-native.md) 、或元素的子元素 [\<Type>](type-element-net-native.md) ，则它会重写由父元素定义的策略设置。</span><span class="sxs-lookup"><span data-stu-id="8c563-195">If a `<TypeInstantiation>` element is the child of an [\<Assembly>](assembly-element-net-native.md), [\<Namespace>](namespace-element-net-native.md), or [\<Type>](type-element-net-native.md), element, it overrides the policy settings defined by the parent element.</span></span> <span data-ttu-id="8c563-196">如果 [\<Type>](type-element-net-native.md) 元素定义了一个相应的泛型类型定义，则 `<TypeInstantiation>` 元素只会重写指定的构造泛型类型的实例化的运行时反射策略。</span><span class="sxs-lookup"><span data-stu-id="8c563-196">If a [\<Type>](type-element-net-native.md) element defines a corresponding generic type definition, the `<TypeInstantiation>` element overrides runtime reflection policy only for instantiations of the specified constructed generic type.</span></span>  
  
## <a name="example"></a><span data-ttu-id="8c563-197">示例</span><span class="sxs-lookup"><span data-stu-id="8c563-197">Example</span></span>  

 <span data-ttu-id="8c563-198">以下实例使用反射从一个构造的 <xref:System.Collections.Generic.Dictionary%602> 对象取回了泛型类型定义。</span><span class="sxs-lookup"><span data-stu-id="8c563-198">The following example uses reflection to retrieve the generic type definition from a constructed <xref:System.Collections.Generic.Dictionary%602> object.</span></span> <span data-ttu-id="8c563-199">它还使用反射显示了代表构造泛型类型和构造类型定义的有关 <xref:System.Type> 对象的信息。</span><span class="sxs-lookup"><span data-stu-id="8c563-199">It also uses reflection to display information about <xref:System.Type> objects that represent constructed generic types and generic type definitions.</span></span> <span data-ttu-id="8c563-200">`b`示例中的变量是一个 <xref:Windows.UI.Xaml.Controls.TextBlock> 控件。</span><span class="sxs-lookup"><span data-stu-id="8c563-200">The variable `b` in the example is a <xref:Windows.UI.Xaml.Controls.TextBlock> control.</span></span>  
  
 [!code-csharp[ProjectN_Reflection#2](../../../samples/snippets/csharp/VS_Snippets_CLR/projectn_reflection/cs/makegenerictype1.cs#2)]  
  
 <span data-ttu-id="8c563-201">使用 .NET Native 工具链进行编译之后，该示例在调用方法的行上引发 [MissingMetadataException](missingmetadataexception-class-net-native.md) 异常 <xref:System.Type.GetGenericTypeDefinition%2A?displayProperty=nameWithType> 。</span><span class="sxs-lookup"><span data-stu-id="8c563-201">After compilation with the .NET Native tool chain, the example throws a [MissingMetadataException](missingmetadataexception-class-net-native.md) exception on the line that calls the <xref:System.Type.GetGenericTypeDefinition%2A?displayProperty=nameWithType> method.</span></span> <span data-ttu-id="8c563-202">你可通过将以下 `<TypeInstantiation>` 元素添加到运行时指令文件来消除异常并提供必需的元数据：</span><span class="sxs-lookup"><span data-stu-id="8c563-202">You can eliminate the exception and provide the necessary metadata by adding the following `<TypeInstantiation>` element to the runtime directives file:</span></span>  
  
```xml  
<Directives xmlns="http://schemas.microsoft.com/netfx/2013/01/metadata">  
  <Application>  
    <Assembly Name="*Application*" Dynamic="Required All" />  
     <TypeInstantiation Name="System.Collections.Generic.Dictionary"  
                        Arguments="System.String,GenericType.Example"  
                        Dynamic="Required Public" />  
  </Application>  
</Directives>  
```  
  
## <a name="see-also"></a><span data-ttu-id="8c563-203">请参阅</span><span class="sxs-lookup"><span data-stu-id="8c563-203">See also</span></span>

- [<span data-ttu-id="8c563-204">运行时指令 (rd.xml) 配置文件引用</span><span class="sxs-lookup"><span data-stu-id="8c563-204">Runtime Directives (rd.xml) Configuration File Reference</span></span>](runtime-directives-rd-xml-configuration-file-reference.md)
- [<span data-ttu-id="8c563-205">运行时指令元素</span><span class="sxs-lookup"><span data-stu-id="8c563-205">Runtime Directive Elements</span></span>](runtime-directive-elements.md)
- [<span data-ttu-id="8c563-206">运行时指令策略设置</span><span class="sxs-lookup"><span data-stu-id="8c563-206">Runtime Directive Policy Settings</span></span>](runtime-directive-policy-settings.md)
