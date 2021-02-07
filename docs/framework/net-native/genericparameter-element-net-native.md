---
description: '了解详细信息： <GenericParameter> 元素 ( .NET Native) '
title: <GenericParameter>元素 (.NET Native)
ms.date: 03/30/2017
ms.assetid: cbd49732-3615-49a5-a900-f96947cdc3e6
ms.openlocfilehash: 57cbb3418289d7da4f25577188299acd55ce6c94
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99747824"
---
# <a name="genericparameter-element-net-native"></a><span data-ttu-id="9eb74-103">\<GenericParameter>元素 (.NET Native)</span><span class="sxs-lookup"><span data-stu-id="9eb74-103">\<GenericParameter> Element (.NET Native)</span></span>

<span data-ttu-id="9eb74-104">将策略应用到一个泛型类型或方法的参数类型。</span><span class="sxs-lookup"><span data-stu-id="9eb74-104">Applies policy to the parameter type of a generic type or method.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9eb74-105">语法</span><span class="sxs-lookup"><span data-stu-id="9eb74-105">Syntax</span></span>  
  
```xml  
<GenericParameter Name="generic_parameter_name"  
                  Activate="policy_type"  
                  Browse="policy_type"  
                  Dynamic="policy_type"  
                  Serialize="policy_type"  
                  DataContractSerializer="policy_type"  
                  DataContractJsonSerializer="policy_type"  
                  XmlSerializer="policy_type"  
                  MarshalObject="policy_type"  
                  MarshalDelegate="policy_type"  
                  MarshalStructure="policy_type" />
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="9eb74-106">特性和元素</span><span class="sxs-lookup"><span data-stu-id="9eb74-106">Attributes and Elements</span></span>  

 <span data-ttu-id="9eb74-107">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="9eb74-107">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="9eb74-108">特性</span><span class="sxs-lookup"><span data-stu-id="9eb74-108">Attributes</span></span>  
  
|<span data-ttu-id="9eb74-109">属性</span><span class="sxs-lookup"><span data-stu-id="9eb74-109">Attribute</span></span>|<span data-ttu-id="9eb74-110">属性类型</span><span class="sxs-lookup"><span data-stu-id="9eb74-110">Attribute type</span></span>|<span data-ttu-id="9eb74-111">说明</span><span class="sxs-lookup"><span data-stu-id="9eb74-111">Description</span></span>|  
|---------------|--------------------|-----------------|  
|`Name`|<span data-ttu-id="9eb74-112">常规</span><span class="sxs-lookup"><span data-stu-id="9eb74-112">General</span></span>|<span data-ttu-id="9eb74-113">必需的特性。</span><span class="sxs-lookup"><span data-stu-id="9eb74-113">Required attribute.</span></span> <span data-ttu-id="9eb74-114">泛型参数的名称。</span><span class="sxs-lookup"><span data-stu-id="9eb74-114">The name of the generic parameter.</span></span> <span data-ttu-id="9eb74-115">例如，对于泛型委托 <xref:System.Func%603>，`Name` 特性的值为“TResult”，从而将运行时策略应用到该委托的返回值。</span><span class="sxs-lookup"><span data-stu-id="9eb74-115">For example, for the generic delegate <xref:System.Func%603>, the value of the `Name` attribute is "TResult" to apply runtime policy to the delegate's return value.</span></span>|  
|`Activate`|<span data-ttu-id="9eb74-116">反射</span><span class="sxs-lookup"><span data-stu-id="9eb74-116">Reflection</span></span>|<span data-ttu-id="9eb74-117">可选特性。</span><span class="sxs-lookup"><span data-stu-id="9eb74-117">Optional attribute.</span></span> <span data-ttu-id="9eb74-118">控制运行时对构造函数的访问，以启用实例激活。</span><span class="sxs-lookup"><span data-stu-id="9eb74-118">Controls runtime access to constructors to enable activation of instances.</span></span>|  
|`Browse`|<span data-ttu-id="9eb74-119">反射</span><span class="sxs-lookup"><span data-stu-id="9eb74-119">Reflection</span></span>|<span data-ttu-id="9eb74-120">可选特性。</span><span class="sxs-lookup"><span data-stu-id="9eb74-120">Optional attribute.</span></span> <span data-ttu-id="9eb74-121">控制对有关程序元素信息的查询，但并不启用任何运行时访问。</span><span class="sxs-lookup"><span data-stu-id="9eb74-121">Controls querying for information about program elements, but does not enable any runtime access.</span></span>|  
|`Dynamic`|<span data-ttu-id="9eb74-122">反射</span><span class="sxs-lookup"><span data-stu-id="9eb74-122">Reflection</span></span>|<span data-ttu-id="9eb74-123">可选特性。</span><span class="sxs-lookup"><span data-stu-id="9eb74-123">Optional attribute.</span></span> <span data-ttu-id="9eb74-124">控制运行时对所有类型成员的访问，包括构造函数、方法、字段、属性和事件，以启用动态编程。</span><span class="sxs-lookup"><span data-stu-id="9eb74-124">Controls runtime access to all type members, including constructors, methods, fields, properties, and events, to enable dynamic programming.</span></span>|  
|`Serialize`|<span data-ttu-id="9eb74-125">序列化</span><span class="sxs-lookup"><span data-stu-id="9eb74-125">Serialization</span></span>|<span data-ttu-id="9eb74-126">可选特性。</span><span class="sxs-lookup"><span data-stu-id="9eb74-126">Optional attribute.</span></span> <span data-ttu-id="9eb74-127">控制运行时对构造函数、字段和属性的访问，使类型实例得到序列化和反序列化处理，这是通过库进行的，例如 Newtonsoft JSON 序列化程序。</span><span class="sxs-lookup"><span data-stu-id="9eb74-127">Controls runtime access to constructors, fields, and properties, to enable type instances to be serialized and deserialized by libraries such as the Newtonsoft JSON serializer.</span></span>|  
|`DataContractSerializer`|<span data-ttu-id="9eb74-128">序列化</span><span class="sxs-lookup"><span data-stu-id="9eb74-128">Serialization</span></span>|<span data-ttu-id="9eb74-129">可选特性。</span><span class="sxs-lookup"><span data-stu-id="9eb74-129">Optional attribute.</span></span> <span data-ttu-id="9eb74-130">控制使用 <xref:System.Runtime.Serialization.DataContractSerializer?displayProperty=nameWithType> 类的序列化策略。</span><span class="sxs-lookup"><span data-stu-id="9eb74-130">Controls policy for serialization that uses the <xref:System.Runtime.Serialization.DataContractSerializer?displayProperty=nameWithType> class.</span></span>|  
|`DataContractJsonSerializer`|<span data-ttu-id="9eb74-131">序列化</span><span class="sxs-lookup"><span data-stu-id="9eb74-131">Serialization</span></span>|<span data-ttu-id="9eb74-132">可选特性。</span><span class="sxs-lookup"><span data-stu-id="9eb74-132">Optional attribute.</span></span> <span data-ttu-id="9eb74-133">控制使用 <xref:System.Runtime.Serialization.Json.DataContractJsonSerializer?displayProperty=nameWithType> 类的 JSON 序列化策略。</span><span class="sxs-lookup"><span data-stu-id="9eb74-133">Controls policy for JSON serialization that uses the <xref:System.Runtime.Serialization.Json.DataContractJsonSerializer?displayProperty=nameWithType> class.</span></span>|  
|`XmlSerializer`|<span data-ttu-id="9eb74-134">序列化</span><span class="sxs-lookup"><span data-stu-id="9eb74-134">Serialization</span></span>|<span data-ttu-id="9eb74-135">可选特性。</span><span class="sxs-lookup"><span data-stu-id="9eb74-135">Optional attribute.</span></span> <span data-ttu-id="9eb74-136">控制使用 <xref:System.Xml.Serialization.XmlSerializer?displayProperty=nameWithType> 类的 XML 序列化策略。</span><span class="sxs-lookup"><span data-stu-id="9eb74-136">Controls policy for XML serialization that uses the <xref:System.Xml.Serialization.XmlSerializer?displayProperty=nameWithType> class.</span></span>|  
|`MarshalObject`|<span data-ttu-id="9eb74-137">Interop</span><span class="sxs-lookup"><span data-stu-id="9eb74-137">Interop</span></span>|<span data-ttu-id="9eb74-138">可选特性。</span><span class="sxs-lookup"><span data-stu-id="9eb74-138">Optional attribute.</span></span> <span data-ttu-id="9eb74-139">控制封送引用类型到 Windows 运行时和 COM 的策略。</span><span class="sxs-lookup"><span data-stu-id="9eb74-139">Controls policy for marshaling reference types to Windows Runtime and COM.</span></span>|  
|`MarshalDelegate`|<span data-ttu-id="9eb74-140">Interop</span><span class="sxs-lookup"><span data-stu-id="9eb74-140">Interop</span></span>|<span data-ttu-id="9eb74-141">可选特性。</span><span class="sxs-lookup"><span data-stu-id="9eb74-141">Optional attribute.</span></span> <span data-ttu-id="9eb74-142">控制将委托类型作为函数指针封送到本机代码的策略。</span><span class="sxs-lookup"><span data-stu-id="9eb74-142">Controls policy for marshaling delegate types as function pointers to native code.</span></span>|  
|`MarshalStructure`|<span data-ttu-id="9eb74-143">Interop</span><span class="sxs-lookup"><span data-stu-id="9eb74-143">Interop</span></span>|<span data-ttu-id="9eb74-144">可选特性。</span><span class="sxs-lookup"><span data-stu-id="9eb74-144">Optional attribute.</span></span> <span data-ttu-id="9eb74-145">控制封送处理值类型到本机代码的策略。</span><span class="sxs-lookup"><span data-stu-id="9eb74-145">Controls policy for marshaling value types to native code.</span></span>|  
  
## <a name="name-attribute"></a><span data-ttu-id="9eb74-146">Name 特性</span><span class="sxs-lookup"><span data-stu-id="9eb74-146">Name attribute</span></span>  
  
|<span data-ttu-id="9eb74-147">值</span><span class="sxs-lookup"><span data-stu-id="9eb74-147">Value</span></span>|<span data-ttu-id="9eb74-148">说明</span><span class="sxs-lookup"><span data-stu-id="9eb74-148">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="9eb74-149">generic_parameter_name</span><span class="sxs-lookup"><span data-stu-id="9eb74-149">*generic_parameter_name*</span></span>|<span data-ttu-id="9eb74-150">必需的特性。</span><span class="sxs-lookup"><span data-stu-id="9eb74-150">Required attribute.</span></span> <span data-ttu-id="9eb74-151">泛型类型参数的名称。</span><span class="sxs-lookup"><span data-stu-id="9eb74-151">The name of the generic type parameter.</span></span> <span data-ttu-id="9eb74-152">例如，对于泛型委托 <xref:System.Func%603>，“TResult”的一个 generic_parameter_name 值将运行时策略应用到该委托的返回值。</span><span class="sxs-lookup"><span data-stu-id="9eb74-152">For example, for the generic delegate <xref:System.Func%603>, a *generic_parameter_name* value of "TResult" applies runtime policy to the delegate's return value.</span></span>|  
  
## <a name="all-other-attributes"></a><span data-ttu-id="9eb74-153">所有其他特性</span><span class="sxs-lookup"><span data-stu-id="9eb74-153">All other attributes</span></span>  
  
|<span data-ttu-id="9eb74-154">值</span><span class="sxs-lookup"><span data-stu-id="9eb74-154">Value</span></span>|<span data-ttu-id="9eb74-155">说明</span><span class="sxs-lookup"><span data-stu-id="9eb74-155">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="9eb74-156">*策略_设置*</span><span class="sxs-lookup"><span data-stu-id="9eb74-156">*policy_setting*</span></span>|<span data-ttu-id="9eb74-157">该设置将应用到这种策略类型。</span><span class="sxs-lookup"><span data-stu-id="9eb74-157">The setting to apply to this policy type.</span></span> <span data-ttu-id="9eb74-158">可能值为 `All`、`Public`、`PublicAndInternal`、`Required Public`、`Required PublicAndInternal` 以及 `Required All`。</span><span class="sxs-lookup"><span data-stu-id="9eb74-158">Possible values are `All`, `Public`, `PublicAndInternal`, `Required Public`, `Required PublicAndInternal`, and `Required All`.</span></span> <span data-ttu-id="9eb74-159">有关详细信息，请参阅[运行时指令策略设置](runtime-directive-policy-settings.md)。</span><span class="sxs-lookup"><span data-stu-id="9eb74-159">For more information, see [Runtime Directive Policy Settings](runtime-directive-policy-settings.md).</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="9eb74-160">子元素</span><span class="sxs-lookup"><span data-stu-id="9eb74-160">Child Elements</span></span>  

 <span data-ttu-id="9eb74-161">无。</span><span class="sxs-lookup"><span data-stu-id="9eb74-161">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="9eb74-162">父元素</span><span class="sxs-lookup"><span data-stu-id="9eb74-162">Parent Elements</span></span>  
  
|<span data-ttu-id="9eb74-163">元素</span><span class="sxs-lookup"><span data-stu-id="9eb74-163">Element</span></span>|<span data-ttu-id="9eb74-164">说明</span><span class="sxs-lookup"><span data-stu-id="9eb74-164">Description</span></span>|  
|-------------|-----------------|  
|[\<Method>](method-element-net-native.md)|<span data-ttu-id="9eb74-165">将运行时反射策略应用到一个构造函数或方法。</span><span class="sxs-lookup"><span data-stu-id="9eb74-165">Applies runtime reflection policy to a constructor or method.</span></span>|  
|[\<Type>](type-element-net-native.md)|<span data-ttu-id="9eb74-166">将运行时反射策略应用到一个特定类型，例如一个类或结构。</span><span class="sxs-lookup"><span data-stu-id="9eb74-166">Applies runtime reflection policy to a particular type, such as a class or structure.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="9eb74-167">备注</span><span class="sxs-lookup"><span data-stu-id="9eb74-167">Remarks</span></span>  

 <span data-ttu-id="9eb74-168">`<GenericParameter>`元素是或元素的子元素 [\<Method>](method-element-net-native.md) [\<Type>](type-element-net-native.md) ，用于将策略应用于特定的泛型类型参数，该参数由泛型类型或方法签名中的名称指定。</span><span class="sxs-lookup"><span data-stu-id="9eb74-168">The `<GenericParameter>` element is a child of either the [\<Method>](method-element-net-native.md) or [\<Type>](type-element-net-native.md) element and is used to apply policy to a particular generic type parameter, which is specified by its name in the generic type or method signature.</span></span>  
  
 <span data-ttu-id="9eb74-169">`<GenericParameter>` 元素在同序列化程序一起使用时非常有用。</span><span class="sxs-lookup"><span data-stu-id="9eb74-169">The `<GenericParameter>` element is most useful when used with serializers.</span></span> <span data-ttu-id="9eb74-170">下面的示例使用 `<GenericParameter>` 元素将策略应用于对 `T` newtonsoft.json JSON 序列化程序的 JsonConvert 的调用中的类型 [。 DeserializeObject \<T> (字符串) ](https://www.newtonsoft.com/json/help/html/M_Newtonsoft_Json_JsonConvert_DeserializeObject__1.htm) 方法重载。</span><span class="sxs-lookup"><span data-stu-id="9eb74-170">The following example uses the `<GenericParameter>` element to apply policy to the type `T` in calls to the NewtonSoft JSON serializer's [JsonConvert.DeserializeObject\<T>(String)](https://www.newtonsoft.com/json/help/html/M_Newtonsoft_Json_JsonConvert_DeserializeObject__1.htm) method overloads.</span></span>  
  
```xml  
<Directives xmlns="http://schemas.microsoft.com/netfx/2013/01/metadata">  
   <Type Name="Newtonsoft.Json.JsonConvert" >  
      <Method Name="DeserializeObject{T}">  
         <GenericParameter Name="T" Serialize="Required All" />  
      </Method>  
   </Type>  
</Directives>  
```  
  
## <a name="see-also"></a><span data-ttu-id="9eb74-171">请参阅</span><span class="sxs-lookup"><span data-stu-id="9eb74-171">See also</span></span>

- [<span data-ttu-id="9eb74-172">\<Method> 元素</span><span class="sxs-lookup"><span data-stu-id="9eb74-172">\<Method> Element</span></span>](method-element-net-native.md)
- [<span data-ttu-id="9eb74-173">\<Type> 元素</span><span class="sxs-lookup"><span data-stu-id="9eb74-173">\<Type> Element</span></span>](type-element-net-native.md)
- [<span data-ttu-id="9eb74-174">运行时指令 (rd.xml) 配置文件引用</span><span class="sxs-lookup"><span data-stu-id="9eb74-174">Runtime Directives (rd.xml) Configuration File Reference</span></span>](runtime-directives-rd-xml-configuration-file-reference.md)
- [<span data-ttu-id="9eb74-175">运行时指令策略设置</span><span class="sxs-lookup"><span data-stu-id="9eb74-175">Runtime Directive Policy Settings</span></span>](runtime-directive-policy-settings.md)
- [<span data-ttu-id="9eb74-176">运行时指令元素</span><span class="sxs-lookup"><span data-stu-id="9eb74-176">Runtime Directive Elements</span></span>](runtime-directive-elements.md)
