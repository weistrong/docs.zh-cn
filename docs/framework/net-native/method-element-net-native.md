---
description: '了解详细信息： <Method> 元素 ( .NET Native) '
title: <Method>元素 (.NET Native)
ms.date: 03/30/2017
ms.assetid: 348b49e5-589d-4eb2-a597-d6ff60ab52d1
ms.openlocfilehash: 76c379ed81e721316e4293b20ba89acfbc9d174f
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99747518"
---
# <a name="method-element-net-native"></a><span data-ttu-id="ed9d7-103">\<Method>元素 (.NET Native)</span><span class="sxs-lookup"><span data-stu-id="ed9d7-103">\<Method> Element (.NET Native)</span></span>

<span data-ttu-id="ed9d7-104">将运行时反射策略应用到一个构造函数或方法。</span><span class="sxs-lookup"><span data-stu-id="ed9d7-104">Applies runtime reflection policy to a constructor or method.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ed9d7-105">语法</span><span class="sxs-lookup"><span data-stu-id="ed9d7-105">Syntax</span></span>  
  
```xml  
<Method Name="method_name"  
        Signature="method_signature"  
        Browse="policy_type"  
        Dynamic="policy_type" />  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="ed9d7-106">特性和元素</span><span class="sxs-lookup"><span data-stu-id="ed9d7-106">Attributes and Elements</span></span>  

 <span data-ttu-id="ed9d7-107">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="ed9d7-107">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="ed9d7-108">特性</span><span class="sxs-lookup"><span data-stu-id="ed9d7-108">Attributes</span></span>  
  
|<span data-ttu-id="ed9d7-109">属性</span><span class="sxs-lookup"><span data-stu-id="ed9d7-109">Attribute</span></span>|<span data-ttu-id="ed9d7-110">属性类型</span><span class="sxs-lookup"><span data-stu-id="ed9d7-110">Attribute type</span></span>|<span data-ttu-id="ed9d7-111">说明</span><span class="sxs-lookup"><span data-stu-id="ed9d7-111">Description</span></span>|  
|---------------|--------------------|-----------------|  
|`Name`|<span data-ttu-id="ed9d7-112">常规</span><span class="sxs-lookup"><span data-stu-id="ed9d7-112">General</span></span>|<span data-ttu-id="ed9d7-113">必需的特性。</span><span class="sxs-lookup"><span data-stu-id="ed9d7-113">Required attribute.</span></span> <span data-ttu-id="ed9d7-114">指定方法名称。</span><span class="sxs-lookup"><span data-stu-id="ed9d7-114">Specifies the method name.</span></span>|  
|`Signature`|<span data-ttu-id="ed9d7-115">常规</span><span class="sxs-lookup"><span data-stu-id="ed9d7-115">General</span></span>|<span data-ttu-id="ed9d7-116">可选特性。</span><span class="sxs-lookup"><span data-stu-id="ed9d7-116">Optional attribute.</span></span> <span data-ttu-id="ed9d7-117">指定方法签名。</span><span class="sxs-lookup"><span data-stu-id="ed9d7-117">Specifies the method signature.</span></span> <span data-ttu-id="ed9d7-118">如果存在多个参数，它们之间用逗号分割。</span><span class="sxs-lookup"><span data-stu-id="ed9d7-118">If multiple parameters are present, they are separated by commas.</span></span> <span data-ttu-id="ed9d7-119">例如，以下 `<Method>` 元素定义了 <xref:System.DateTimeOffset.ToString%28System.String%2CSystem.IFormatProvider%29> 方法的策略。</span><span class="sxs-lookup"><span data-stu-id="ed9d7-119">For example, the following `<Method>` element defines policy for the <xref:System.DateTimeOffset.ToString%28System.String%2CSystem.IFormatProvider%29> method.</span></span><br /><br /> `<Type Name="System.DateTime">    <Method Name="ToString" Signature="System.String,System.IFormatProvider"            Dynamic="Required" /> </Type>`<br /><br /> <span data-ttu-id="ed9d7-120">如果该特性不存在，运行时指令将应用到该方法的所有重载。</span><span class="sxs-lookup"><span data-stu-id="ed9d7-120">If the attribute is absent, the runtime directive applies to all overloads of the method.</span></span>|  
|`Browse`|<span data-ttu-id="ed9d7-121">反射</span><span class="sxs-lookup"><span data-stu-id="ed9d7-121">Reflection</span></span>|<span data-ttu-id="ed9d7-122">可选特性。</span><span class="sxs-lookup"><span data-stu-id="ed9d7-122">Optional attribute.</span></span> <span data-ttu-id="ed9d7-123">控制对该方法信息的查询或列举该方法，但并不在运行时间启用任何动态调用。</span><span class="sxs-lookup"><span data-stu-id="ed9d7-123">Controls querying for information about or enumerating a method but does not enable any dynamic invocation at run time.</span></span>|  
|`Dynamic`|<span data-ttu-id="ed9d7-124">反射</span><span class="sxs-lookup"><span data-stu-id="ed9d7-124">Reflection</span></span>|<span data-ttu-id="ed9d7-125">可选特性。</span><span class="sxs-lookup"><span data-stu-id="ed9d7-125">Optional attribute.</span></span> <span data-ttu-id="ed9d7-126">控制运行时对构造函数或方法的访问，以启用动态编程。</span><span class="sxs-lookup"><span data-stu-id="ed9d7-126">Controls runtime access to a constructor or method to enable dynamic programming.</span></span> <span data-ttu-id="ed9d7-127">该策略确保一个成员可在运行时间内得到调用。</span><span class="sxs-lookup"><span data-stu-id="ed9d7-127">This policy ensures that a member can be invoked dynamically at run time.</span></span>|  
  
## <a name="name-attribute"></a><span data-ttu-id="ed9d7-128">Name 特性</span><span class="sxs-lookup"><span data-stu-id="ed9d7-128">Name attribute</span></span>  
  
|<span data-ttu-id="ed9d7-129">值</span><span class="sxs-lookup"><span data-stu-id="ed9d7-129">Value</span></span>|<span data-ttu-id="ed9d7-130">说明</span><span class="sxs-lookup"><span data-stu-id="ed9d7-130">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="ed9d7-131">method_name</span><span class="sxs-lookup"><span data-stu-id="ed9d7-131">*method_name*</span></span>|<span data-ttu-id="ed9d7-132">方法名称。</span><span class="sxs-lookup"><span data-stu-id="ed9d7-132">The method name.</span></span> <span data-ttu-id="ed9d7-133">方法的类型由父级 [\<Type>](type-element-net-native.md) 或 [\<TypeInstantiation>](typeinstantiation-element-net-native.md) 元素定义。</span><span class="sxs-lookup"><span data-stu-id="ed9d7-133">The type of the method is defined by the parent [\<Type>](type-element-net-native.md) or [\<TypeInstantiation>](typeinstantiation-element-net-native.md) element.</span></span>|  
  
## <a name="signature-attribute"></a><span data-ttu-id="ed9d7-134">签名特性</span><span class="sxs-lookup"><span data-stu-id="ed9d7-134">Signature attribute</span></span>  
  
|<span data-ttu-id="ed9d7-135">值</span><span class="sxs-lookup"><span data-stu-id="ed9d7-135">Value</span></span>|<span data-ttu-id="ed9d7-136">说明</span><span class="sxs-lookup"><span data-stu-id="ed9d7-136">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="ed9d7-137">*method_signature*</span><span class="sxs-lookup"><span data-stu-id="ed9d7-137">*method_signature*</span></span>|<span data-ttu-id="ed9d7-138">形成方法签名的参数类型。</span><span class="sxs-lookup"><span data-stu-id="ed9d7-138">The parameter types that form the method signature.</span></span> <span data-ttu-id="ed9d7-139">多个参数由逗号分隔，例如，`"System.String,System.Int32,System.Int32)"`。</span><span class="sxs-lookup"><span data-stu-id="ed9d7-139">Multiple parameters are separated by commas, for example, `"System.String,System.Int32,System.Int32)"`.</span></span> <span data-ttu-id="ed9d7-140">参数类型名称应是完全限定的。</span><span class="sxs-lookup"><span data-stu-id="ed9d7-140">Parameter type names should be fully qualified.</span></span>|  
  
## <a name="all-other-attributes"></a><span data-ttu-id="ed9d7-141">所有其他特性</span><span class="sxs-lookup"><span data-stu-id="ed9d7-141">All other attributes</span></span>  
  
|<span data-ttu-id="ed9d7-142">值</span><span class="sxs-lookup"><span data-stu-id="ed9d7-142">Value</span></span>|<span data-ttu-id="ed9d7-143">说明</span><span class="sxs-lookup"><span data-stu-id="ed9d7-143">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="ed9d7-144">*策略_设置*</span><span class="sxs-lookup"><span data-stu-id="ed9d7-144">*policy_setting*</span></span>|<span data-ttu-id="ed9d7-145">该设置将应用到这种策略类型。</span><span class="sxs-lookup"><span data-stu-id="ed9d7-145">The setting to apply to this policy type.</span></span> <span data-ttu-id="ed9d7-146">可能值为 `Auto`、`Excluded`、`Included` 和 `Required`。</span><span class="sxs-lookup"><span data-stu-id="ed9d7-146">Possible values are `Auto`, `Excluded`, `Included`, and `Required`.</span></span> <span data-ttu-id="ed9d7-147">有关详细信息，请参阅[运行时指令策略设置](runtime-directive-policy-settings.md)。</span><span class="sxs-lookup"><span data-stu-id="ed9d7-147">For more information, see [Runtime Directive Policy Settings](runtime-directive-policy-settings.md).</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="ed9d7-148">子元素</span><span class="sxs-lookup"><span data-stu-id="ed9d7-148">Child Elements</span></span>  
  
|<span data-ttu-id="ed9d7-149">元素</span><span class="sxs-lookup"><span data-stu-id="ed9d7-149">Element</span></span>|<span data-ttu-id="ed9d7-150">说明</span><span class="sxs-lookup"><span data-stu-id="ed9d7-150">Description</span></span>|  
|-------------|-----------------|  
|[\<Parameter>](parameter-element-net-native.md)|<span data-ttu-id="ed9d7-151">将策略应用到传递到方法的参数类型。</span><span class="sxs-lookup"><span data-stu-id="ed9d7-151">Applies policy to the type of the argument passed to a method.</span></span>|  
|[\<GenericParameter>](genericparameter-element-net-native.md)|<span data-ttu-id="ed9d7-152">将策略应用到一个泛型类型或方法的参数类型。</span><span class="sxs-lookup"><span data-stu-id="ed9d7-152">Applies policy to the parameter type of a generic type or method.</span></span>|  
|[\<ImpliesType>](impliestype-element-net-native.md)|<span data-ttu-id="ed9d7-153">如果该策略已应用到以包含 `<Method>` 元素为代表的方法，将该策略应用到一个类型。</span><span class="sxs-lookup"><span data-stu-id="ed9d7-153">Applies policy to a type, if that policy has been applied to the method represented by the containing `<Method>` element.</span></span>|  
|[\<TypeParameter>](typeparameter-element-net-native.md)|<span data-ttu-id="ed9d7-154">将策略应用到以传递到方法为代表的 <xref:System.Type> 自变量类型。</span><span class="sxs-lookup"><span data-stu-id="ed9d7-154">Applies policy to the type represented by a <xref:System.Type> argument passed to a method.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="ed9d7-155">父元素</span><span class="sxs-lookup"><span data-stu-id="ed9d7-155">Parent Elements</span></span>  
  
|<span data-ttu-id="ed9d7-156">元素</span><span class="sxs-lookup"><span data-stu-id="ed9d7-156">Element</span></span>|<span data-ttu-id="ed9d7-157">说明</span><span class="sxs-lookup"><span data-stu-id="ed9d7-157">Description</span></span>|  
|-------------|-----------------|  
|[\<Type>](type-element-net-native.md)|<span data-ttu-id="ed9d7-158">将反射策略应用到一种类型及其所有成员。</span><span class="sxs-lookup"><span data-stu-id="ed9d7-158">Applies reflection policy to a type and all its members.</span></span>|  
|[\<TypeInstantiation>](typeinstantiation-element-net-native.md)|<span data-ttu-id="ed9d7-159">将反射策略应用到一种构造泛型类型及其所有成员。</span><span class="sxs-lookup"><span data-stu-id="ed9d7-159">Applies reflection policy to a constructed generic type and all its members.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="ed9d7-160">备注</span><span class="sxs-lookup"><span data-stu-id="ed9d7-160">Remarks</span></span>  

 <span data-ttu-id="ed9d7-161">一个泛型方法的 `<Method>` 元素会将其策略应用到所有不具有自身策略的实例化。</span><span class="sxs-lookup"><span data-stu-id="ed9d7-161">A `<Method>` element of a generic method applies its policy to all instantiations that do not have their own policy.</span></span>  
  
 <span data-ttu-id="ed9d7-162">你可以使用 `Signature` 特性为特定的方法重载指定策略。</span><span class="sxs-lookup"><span data-stu-id="ed9d7-162">You can use the `Signature` attribute to specify policy for a particular method overload.</span></span> <span data-ttu-id="ed9d7-163">如果 `Signature` 特性不存在，运行时指令将应用到该方法的所有重载。</span><span class="sxs-lookup"><span data-stu-id="ed9d7-163">Otherwise, if the `Signature` attribute is absent, the runtime directive applies to all overloads of the method.</span></span>  
  
 <span data-ttu-id="ed9d7-164">你无法通过使用 `<Method>` 元素为一个构造函数定义运行时反射策略。</span><span class="sxs-lookup"><span data-stu-id="ed9d7-164">You cannot define the runtime reflection policy for a constructor by using the `<Method>` element.</span></span> <span data-ttu-id="ed9d7-165">相反，请使用 `Activate`  [\<Assembly>](assembly-element-net-native.md) 、 [\<Namespace>](namespace-element-net-native.md) 、 [\<Type>](type-element-net-native.md) 或元素的特性 [\<TypeInstantiation>](typeinstantiation-element-net-native.md) 。</span><span class="sxs-lookup"><span data-stu-id="ed9d7-165">Instead, use the `Activate` attribute of the  [\<Assembly>](assembly-element-net-native.md), [\<Namespace>](namespace-element-net-native.md), [\<Type>](type-element-net-native.md), or [\<TypeInstantiation>](typeinstantiation-element-net-native.md) element.</span></span>  
  
## <a name="example"></a><span data-ttu-id="ed9d7-166">示例</span><span class="sxs-lookup"><span data-stu-id="ed9d7-166">Example</span></span>  

 <span data-ttu-id="ed9d7-167">以下实例中的 `Stringify` 方法是使用反射将一个对象转化为其字符串表示形式的一个通用格式化方法。</span><span class="sxs-lookup"><span data-stu-id="ed9d7-167">The `Stringify` method in the following example is a general-purpose formatting method that uses reflection to convert an object to its string representation.</span></span> <span data-ttu-id="ed9d7-168">除调用该对象的默认 `ToString` 方法外，该方法可以通过穿过一个对象的 `ToString` 方法格式字符车产生一个格式化的字符串或/和一个 <xref:System.IFormatProvider> 实现。</span><span class="sxs-lookup"><span data-stu-id="ed9d7-168">In addition to calling the object's default `ToString` method, the method can produce a formatted result string by passing an object's `ToString` method a format string, an <xref:System.IFormatProvider> implementation, or both.</span></span> <span data-ttu-id="ed9d7-169">它也可以调用将一个成员转化为其二进制、十六进制或八进制表示的 <xref:System.Convert.ToString%2A?displayProperty=nameWithType> 重载之一。</span><span class="sxs-lookup"><span data-stu-id="ed9d7-169">It can also call one of the <xref:System.Convert.ToString%2A?displayProperty=nameWithType> overloads that converts a number to its binary, hexadecimal, or octal representation.</span></span>  
  
 [!code-csharp[ProjectN_Reflection#7](../../../samples/snippets/csharp/VS_Snippets_CLR/projectn_reflection/cs/method1.cs#7)]  
  
 <span data-ttu-id="ed9d7-170">`Stringify` 方法可以通过类似以下的代码调用：</span><span class="sxs-lookup"><span data-stu-id="ed9d7-170">The `Stringify` method can be called by code like the following:</span></span>  
  
 [!code-csharp[ProjectN_Reflection#7](../../../samples/snippets/csharp/VS_Snippets_CLR/projectn_reflection/cs/method1.cs#7)]  
  
 <span data-ttu-id="ed9d7-171">然而，使用 .NET Native 编译时，该示例可能会在运行时引发一系列异常，包括 <xref:System.NullReferenceException> 和 [MissingRuntimeArtifactException](missingruntimeartifactexception-class-net-native.md) 异常。原因在于 `Stringify` 方法的本来目的是支持动态地设置 .NET Framework 类库中基元类型的格式。</span><span class="sxs-lookup"><span data-stu-id="ed9d7-171">However, when compiled with .NET Native, the example can throw an number of exceptions at runtime, including <xref:System.NullReferenceException> and [MissingRuntimeArtifactException](missingruntimeartifactexception-class-net-native.md) exceptions, This occurs because the `Stringify` method is intended primarily to support dynamically formatting the primitive types in the .NET Framework Class Library.</span></span> <span data-ttu-id="ed9d7-172">然而，它们的元数据不会通过默认指令文件变得可以使用。</span><span class="sxs-lookup"><span data-stu-id="ed9d7-172">However, their metadata is not made available by the default directives file.</span></span> <span data-ttu-id="ed9d7-173">即使在它们的元数据变得可用时，实例还会引发 [MissingRuntimeArtifactException](missingruntimeartifactexception-class-net-native.md) 异常，因为适当的 `ToString` 实现并未包含在本机代码之中。</span><span class="sxs-lookup"><span data-stu-id="ed9d7-173">Even when their metadata is made available, however, the example throws [MissingRuntimeArtifactException](missingruntimeartifactexception-class-net-native.md) exceptions because the appropriate `ToString` implementations have not been include in the native code.</span></span>  
  
 <span data-ttu-id="ed9d7-174">通过使用 [\<Type>](type-element-net-native.md) 元素定义其元数据必须存在的类型，以及通过添加 `<Method>` 元素来确保也存在可以动态调用的方法重载的实现，可以消除这些异常。</span><span class="sxs-lookup"><span data-stu-id="ed9d7-174">These exceptions can all be eliminated by using the [\<Type>](type-element-net-native.md) element to define the types whose metadata must be present, and by adding `<Method>` elements to ensure that the implementation of method overloads that can be called dynamically is also present.</span></span> <span data-ttu-id="ed9d7-175">以下的 default.rd.xml 文件可以清除这些异常并允许实例没有错误地执行。</span><span class="sxs-lookup"><span data-stu-id="ed9d7-175">The following is the default.rd.xml file that eliminates these exceptions and allows the example to execute without error.</span></span>  
  
```xml  
<Directives xmlns="http://schemas.microsoft.com/netfx/2013/01/metadata">  
  <Application>  
     <Assembly Name="*Application*" Dynamic="Required All" />  
  
     <Type Name = "System.Convert" Browse="Required Public" Dynamic="Required Public" >  
        <Method Name="ToString"    Dynamic ="Required" />  
     </Type>  
     <Type Name="System.Double" Browse="Required Public">  
        <Method Name="ToString" Dynamic="Required" />  
     </Type>  
     <Type Name ="System.Int32" Browse="Required Public" >  
        <Method Name="ToString" Dynamic="Required" />  
     </Type>  
     <Type Name ="System.Int64" Browse="Required Public" >  
        <Method Name="ToString" Dynamic="Required" />  
     </Type>  
     <Namespace Name="System" >  
        <Type Name="Byte" Browse="Required Public" >  
           <Method Name="ToString" Dynamic="Required" />  
        </Type>  
        <Type Name="DateTime" Browse="Required Public" >  
           <Method Name="ToString" Dynamic="Required" />  
        </Type>  
        <Type Name="Decimal" Browse="Required Public" >  
           <Method Name="ToString" Dynamic="Required" />  
        </Type>  
        <Type Name="Guid" Browse ="Required Public" >  
           <Method Name="ToString" Dynamic="Required" />  
        </Type>  
        <Type Name="Int16" Browse="Required Public" >  
           <Method Name="ToString" Dynamic="Required" />  
        </Type>  
        <Type Name="SByte" Browse="Required Public" >  
           <Method Name="ToString" Dynamic="Required" />  
        </Type>  
        <Type Name="Single" Browse="Required Public" >  
          <Method Name="ToString" Dynamic="Required" />
        </Type>  
        <Type Name="TimeSpan" Browse="Required Public" >  
          <Method Name="ToString" Dynamic="Required" />
        </Type>  
        <Type Name="UInt16" Browse="Required Public" >  
           <Method Name="ToString" Dynamic="Required" />  
        </Type>  
        <Type Name="UInt32" Browse="Required Public" >  
           <Method Name="ToString" Dynamic="Required" />  
        </Type>  
        <Type Name="UInt64" Browse="Required Public" >  
           <Method Name="ToString" Dynamic="Required" />  
        </Type>  
     </Namespace>  
  </Application>  
</Directives>  
```  
  
## <a name="see-also"></a><span data-ttu-id="ed9d7-176">请参阅</span><span class="sxs-lookup"><span data-stu-id="ed9d7-176">See also</span></span>

- [<span data-ttu-id="ed9d7-177">运行时指令 (rd.xml) 配置文件引用</span><span class="sxs-lookup"><span data-stu-id="ed9d7-177">Runtime Directives (rd.xml) Configuration File Reference</span></span>](runtime-directives-rd-xml-configuration-file-reference.md)
- [<span data-ttu-id="ed9d7-178">运行时指令元素</span><span class="sxs-lookup"><span data-stu-id="ed9d7-178">Runtime Directive Elements</span></span>](runtime-directive-elements.md)
- [<span data-ttu-id="ed9d7-179">运行时指令策略设置</span><span class="sxs-lookup"><span data-stu-id="ed9d7-179">Runtime Directive Policy Settings</span></span>](runtime-directive-policy-settings.md)
- [<span data-ttu-id="ed9d7-180">\<MethodInstantiation> 元素</span><span class="sxs-lookup"><span data-stu-id="ed9d7-180">\<MethodInstantiation> Element</span></span>](methodinstantiation-element-net-native.md)
