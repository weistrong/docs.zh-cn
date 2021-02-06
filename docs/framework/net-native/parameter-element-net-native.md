---
description: '了解详细信息： <Parameter> 元素 ( .NET Native) '
title: <Parameter>元素 (.NET Native)
ms.date: 03/30/2017
ms.assetid: 22aaa1f3-596f-4733-93db-f4bcabcb5240
ms.openlocfilehash: 53b84027e8393e0a799d9652767d173c2787cd27
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99662788"
---
# <a name="parameter-element-net-native"></a><span data-ttu-id="499fd-103">\<Parameter>元素 (.NET Native)</span><span class="sxs-lookup"><span data-stu-id="499fd-103">\<Parameter> Element (.NET Native)</span></span>

<span data-ttu-id="499fd-104">将反射策略应用到传递到方法的自变量类型。</span><span class="sxs-lookup"><span data-stu-id="499fd-104">Applies reflection policy to the type of the argument passed to a method.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="499fd-105">语法</span><span class="sxs-lookup"><span data-stu-id="499fd-105">Syntax</span></span>  
  
```xml  
<Parameter Name="parameter_name"  
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
  
## <a name="attributes-and-elements"></a><span data-ttu-id="499fd-106">特性和元素</span><span class="sxs-lookup"><span data-stu-id="499fd-106">Attributes and Elements</span></span>  

 <span data-ttu-id="499fd-107">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="499fd-107">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="499fd-108">特性</span><span class="sxs-lookup"><span data-stu-id="499fd-108">Attributes</span></span>  
  
|<span data-ttu-id="499fd-109">属性</span><span class="sxs-lookup"><span data-stu-id="499fd-109">Attribute</span></span>|<span data-ttu-id="499fd-110">属性类型</span><span class="sxs-lookup"><span data-stu-id="499fd-110">Attribute type</span></span>|<span data-ttu-id="499fd-111">说明</span><span class="sxs-lookup"><span data-stu-id="499fd-111">Description</span></span>|  
|---------------|--------------------|-----------------|  
|`Name`|<span data-ttu-id="499fd-112">常规</span><span class="sxs-lookup"><span data-stu-id="499fd-112">General</span></span>|<span data-ttu-id="499fd-113">必需的特性。</span><span class="sxs-lookup"><span data-stu-id="499fd-113">Required attribute.</span></span> <span data-ttu-id="499fd-114">参数名称。</span><span class="sxs-lookup"><span data-stu-id="499fd-114">The parameter name.</span></span> <span data-ttu-id="499fd-115">例如，对于方法签名 `String.CompareTo(Object value)`，`Name` 特性的值为“值”。</span><span class="sxs-lookup"><span data-stu-id="499fd-115">For example, for the method signature `String.CompareTo(Object value)`, the value of the `Name` attribute is "value".</span></span>|  
|`Activate`|<span data-ttu-id="499fd-116">反射</span><span class="sxs-lookup"><span data-stu-id="499fd-116">Reflection</span></span>|<span data-ttu-id="499fd-117">可选特性。</span><span class="sxs-lookup"><span data-stu-id="499fd-117">Optional attribute.</span></span> <span data-ttu-id="499fd-118">控制运行时对构造函数的访问，以启用实例激活。</span><span class="sxs-lookup"><span data-stu-id="499fd-118">Controls runtime access to constructors to enable activation of instances.</span></span>|  
|`Browse`|<span data-ttu-id="499fd-119">反射</span><span class="sxs-lookup"><span data-stu-id="499fd-119">Reflection</span></span>|<span data-ttu-id="499fd-120">可选特性。</span><span class="sxs-lookup"><span data-stu-id="499fd-120">Optional attribute.</span></span> <span data-ttu-id="499fd-121">控制对有关程序元素信息的查询，但并不启用任何运行时访问。</span><span class="sxs-lookup"><span data-stu-id="499fd-121">Controls querying for information about program elements, but does not enable any runtime access.</span></span>|  
|`Dynamic`|<span data-ttu-id="499fd-122">反射</span><span class="sxs-lookup"><span data-stu-id="499fd-122">Reflection</span></span>|<span data-ttu-id="499fd-123">可选特性。</span><span class="sxs-lookup"><span data-stu-id="499fd-123">Optional attribute.</span></span> <span data-ttu-id="499fd-124">控制运行时对所有类型成员的访问，包括构造函数、方法、字段、属性和事件，以启用动态编程。</span><span class="sxs-lookup"><span data-stu-id="499fd-124">Controls runtime access to all type members, including constructors, methods, fields, properties, and events, to enable dynamic programming.</span></span>|  
|`Serialize`|<span data-ttu-id="499fd-125">序列化</span><span class="sxs-lookup"><span data-stu-id="499fd-125">Serialization</span></span>|<span data-ttu-id="499fd-126">可选特性。</span><span class="sxs-lookup"><span data-stu-id="499fd-126">Optional attribute.</span></span> <span data-ttu-id="499fd-127">控制运行时对构造函数、字段和属性的访问，使类型实例得到序列化和反序列化处理，这是通过库进行的，例如 Newtonsoft JSON 序列化程序。</span><span class="sxs-lookup"><span data-stu-id="499fd-127">Controls runtime access to constructors, fields, and properties, to enable type instances to be serialized and deserialized by libraries such as the Newtonsoft JSON serializer.</span></span>|  
|`DataContractSerializer`|<span data-ttu-id="499fd-128">序列化</span><span class="sxs-lookup"><span data-stu-id="499fd-128">Serialization</span></span>|<span data-ttu-id="499fd-129">可选特性。</span><span class="sxs-lookup"><span data-stu-id="499fd-129">Optional attribute.</span></span> <span data-ttu-id="499fd-130">控制使用 <xref:System.Runtime.Serialization.DataContractSerializer?displayProperty=nameWithType> 类的序列化策略。</span><span class="sxs-lookup"><span data-stu-id="499fd-130">Controls policy for serialization that uses the <xref:System.Runtime.Serialization.DataContractSerializer?displayProperty=nameWithType> class.</span></span>|  
|`DataContractJsonSerializer`|<span data-ttu-id="499fd-131">序列化</span><span class="sxs-lookup"><span data-stu-id="499fd-131">Serialization</span></span>|<span data-ttu-id="499fd-132">可选特性。</span><span class="sxs-lookup"><span data-stu-id="499fd-132">Optional attribute.</span></span> <span data-ttu-id="499fd-133">控制使用 <xref:System.Runtime.Serialization.DataContractSerializer?displayProperty=nameWithType> 类的 JSON 序列化策略。</span><span class="sxs-lookup"><span data-stu-id="499fd-133">Controls policy for JSON serialization that uses the <xref:System.Runtime.Serialization.DataContractSerializer?displayProperty=nameWithType> class.</span></span>|  
|`XmlSerializer`|<span data-ttu-id="499fd-134">序列化</span><span class="sxs-lookup"><span data-stu-id="499fd-134">Serialization</span></span>|<span data-ttu-id="499fd-135">可选特性。</span><span class="sxs-lookup"><span data-stu-id="499fd-135">Optional attribute.</span></span> <span data-ttu-id="499fd-136">控制使用 <xref:System.Xml.Serialization.XmlSerializer?displayProperty=nameWithType> 类的 XML 序列化策略。</span><span class="sxs-lookup"><span data-stu-id="499fd-136">Controls policy for XML serialization that uses the <xref:System.Xml.Serialization.XmlSerializer?displayProperty=nameWithType> class.</span></span>|  
|`MarshalObject`|<span data-ttu-id="499fd-137">Interop</span><span class="sxs-lookup"><span data-stu-id="499fd-137">Interop</span></span>|<span data-ttu-id="499fd-138">可选特性。</span><span class="sxs-lookup"><span data-stu-id="499fd-138">Optional attribute.</span></span> <span data-ttu-id="499fd-139">控制将引用类型封送到 WinRT 和 COM 的策略。</span><span class="sxs-lookup"><span data-stu-id="499fd-139">Controls policy for marshaling reference types to WinRT and COM.</span></span>|  
|`MarshalDelegate`|<span data-ttu-id="499fd-140">Interop</span><span class="sxs-lookup"><span data-stu-id="499fd-140">Interop</span></span>|<span data-ttu-id="499fd-141">可选特性。</span><span class="sxs-lookup"><span data-stu-id="499fd-141">Optional attribute.</span></span> <span data-ttu-id="499fd-142">控制将委托类型作为函数指针封送到本机代码的策略。</span><span class="sxs-lookup"><span data-stu-id="499fd-142">Controls policy for marshaling delegate types as function pointers to native code.</span></span>|  
|`MarshalStructure`|<span data-ttu-id="499fd-143">Interop</span><span class="sxs-lookup"><span data-stu-id="499fd-143">Interop</span></span>|<span data-ttu-id="499fd-144">可选特性。</span><span class="sxs-lookup"><span data-stu-id="499fd-144">Optional attribute.</span></span> <span data-ttu-id="499fd-145">控制封送处理值类型到本机代码的策略。</span><span class="sxs-lookup"><span data-stu-id="499fd-145">Controls policy for marshaling value types to native code.</span></span>|  
  
## <a name="name-attribute"></a><span data-ttu-id="499fd-146">Name 特性</span><span class="sxs-lookup"><span data-stu-id="499fd-146">Name attribute</span></span>  
  
|<span data-ttu-id="499fd-147">值</span><span class="sxs-lookup"><span data-stu-id="499fd-147">Value</span></span>|<span data-ttu-id="499fd-148">说明</span><span class="sxs-lookup"><span data-stu-id="499fd-148">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="499fd-149">*parameter_name*</span><span class="sxs-lookup"><span data-stu-id="499fd-149">*parameter_name*</span></span>|<span data-ttu-id="499fd-150">策略应用到的方法参数的名称。</span><span class="sxs-lookup"><span data-stu-id="499fd-150">The name of the method parameter to which policy is applied.</span></span> <span data-ttu-id="499fd-151">例如，对于方法签名 `String.CompareTo(Object value)`，`Name` 特性的值为“值”。</span><span class="sxs-lookup"><span data-stu-id="499fd-151">For example, for the method signature `String.CompareTo(Object value)`, the value of the `Name` attribute is "value".</span></span>|  
  
## <a name="all-other-attributes"></a><span data-ttu-id="499fd-152">所有其他特性</span><span class="sxs-lookup"><span data-stu-id="499fd-152">All other attributes</span></span>  
  
|<span data-ttu-id="499fd-153">值</span><span class="sxs-lookup"><span data-stu-id="499fd-153">Value</span></span>|<span data-ttu-id="499fd-154">说明</span><span class="sxs-lookup"><span data-stu-id="499fd-154">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="499fd-155">*策略_设置*</span><span class="sxs-lookup"><span data-stu-id="499fd-155">*policy_setting*</span></span>|<span data-ttu-id="499fd-156">该设置将应用到这种策略类型。</span><span class="sxs-lookup"><span data-stu-id="499fd-156">The setting to apply to this policy type.</span></span> <span data-ttu-id="499fd-157">可能值为 `All`、`Public`、`PublicAndInternal`、`Required Public`、`Required PublicAndInternal` 以及 `Required All`。</span><span class="sxs-lookup"><span data-stu-id="499fd-157">Possible values are `All`, `Public`, `PublicAndInternal`, `Required Public`, `Required PublicAndInternal`, and `Required All`.</span></span> <span data-ttu-id="499fd-158">有关详细信息，请参阅[运行时指令策略设置](runtime-directive-policy-settings.md)。</span><span class="sxs-lookup"><span data-stu-id="499fd-158">For more information, see [Runtime Directive Policy Settings](runtime-directive-policy-settings.md).</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="499fd-159">子元素</span><span class="sxs-lookup"><span data-stu-id="499fd-159">Child Elements</span></span>  

 <span data-ttu-id="499fd-160">无。</span><span class="sxs-lookup"><span data-stu-id="499fd-160">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="499fd-161">父元素</span><span class="sxs-lookup"><span data-stu-id="499fd-161">Parent Elements</span></span>  
  
|<span data-ttu-id="499fd-162">元素</span><span class="sxs-lookup"><span data-stu-id="499fd-162">Element</span></span>|<span data-ttu-id="499fd-163">说明</span><span class="sxs-lookup"><span data-stu-id="499fd-163">Description</span></span>|  
|-------------|-----------------|  
|[\<Method>](method-element-net-native.md)|<span data-ttu-id="499fd-164">将运行时反射策略应用到一个构造函数或方法。</span><span class="sxs-lookup"><span data-stu-id="499fd-164">Applies runtime reflection policy to a constructor or method.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="499fd-165">备注</span><span class="sxs-lookup"><span data-stu-id="499fd-165">Remarks</span></span>  

 <span data-ttu-id="499fd-166">`<Parameter>`元素是元素的子元素 [\<Method>](method-element-net-native.md) ，用于将策略应用到特定的方法参数。</span><span class="sxs-lookup"><span data-stu-id="499fd-166">The `<Parameter>` element is a child of the [\<Method>](method-element-net-native.md) element and is used to apply policy to a particular method parameter.</span></span> <span data-ttu-id="499fd-167">特定的方法参数由名称而不是由类型指定。</span><span class="sxs-lookup"><span data-stu-id="499fd-167">The specific method parameter is specified by name rather than by type.</span></span> <span data-ttu-id="499fd-168">表示策略类型，比如 `Activate` 或 `Dynamic`，的至少一个特性必须存在。</span><span class="sxs-lookup"><span data-stu-id="499fd-168">At least one attribute that represents a policy type, such as `Activate` or `Dynamic`, must be present.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="499fd-169">请参阅</span><span class="sxs-lookup"><span data-stu-id="499fd-169">See also</span></span>

- [<span data-ttu-id="499fd-170">\<Method> 元素</span><span class="sxs-lookup"><span data-stu-id="499fd-170">\<Method> Element</span></span>](method-element-net-native.md)
- [<span data-ttu-id="499fd-171">运行时指令 (rd.xml) 配置文件引用</span><span class="sxs-lookup"><span data-stu-id="499fd-171">Runtime Directives (rd.xml) Configuration File Reference</span></span>](runtime-directives-rd-xml-configuration-file-reference.md)
- [<span data-ttu-id="499fd-172">运行时指令策略设置</span><span class="sxs-lookup"><span data-stu-id="499fd-172">Runtime Directive Policy Settings</span></span>](runtime-directive-policy-settings.md)
- [<span data-ttu-id="499fd-173">运行时指令元素</span><span class="sxs-lookup"><span data-stu-id="499fd-173">Runtime Directive Elements</span></span>](runtime-directive-elements.md)
