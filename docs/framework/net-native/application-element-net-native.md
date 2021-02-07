---
description: '了解详细信息： <Application> 元素 ( .NET Native) '
title: <Application>元素 (.NET Native)
ms.date: 03/30/2017
ms.assetid: b4e9b37a-059b-4076-8f56-cb3f9cef0cd9
ms.openlocfilehash: ebbc6292b5936e6b7d54666070b33df2da80f57f
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99747941"
---
# <a name="application-element-net-native"></a><span data-ttu-id="054ad-103">\<Application>元素 (.NET Native)</span><span class="sxs-lookup"><span data-stu-id="054ad-103">\<Application> Element (.NET Native)</span></span>

<span data-ttu-id="054ad-104">作为应用程序范围内的类型和元数据可以反应在运行时间的类型成员的容器而服务，并将运行时反射策略应用到一个应用的所有程序元素。</span><span class="sxs-lookup"><span data-stu-id="054ad-104">Serves as a container for application-wide types and type members whose metadata is available for reflection at run time, and applies runtime reflection policy to all the program elements in an app.</span></span>  
  
 <span data-ttu-id="054ad-105">\<Directives> 元素</span><span class="sxs-lookup"><span data-stu-id="054ad-105">\<Directives> Element</span></span>  
<span data-ttu-id="054ad-106">\<Application> 元素 ( # A0) </span><span class="sxs-lookup"><span data-stu-id="054ad-106">\<Application> Element (rd.xml)</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="054ad-107">语法</span><span class="sxs-lookup"><span data-stu-id="054ad-107">Syntax</span></span>  
  
```xml  
<Application Activate="policy_setting"  
             Browse="policy_setting"  
             Dynamic="policy_setting"  
             Serialize="policy_setting"  
             DataContractSerializer="policy_setting"  
             DataContractJsonSerializer="policy_setting"  
             XmlSerializer="policy_setting"  
             MarshalObject="policy_setting"  
             MarshalDelegate="policy_setting"  
             MarshalStructure="policy_setting" />  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="054ad-108">特性和元素</span><span class="sxs-lookup"><span data-stu-id="054ad-108">Attributes and Elements</span></span>  

 <span data-ttu-id="054ad-109">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="054ad-109">The following sections describe attributes, child elements, and parent elements.</span></span> <span data-ttu-id="054ad-110">在子元素表格中，策略指向在运行时间针对特定程序元素可用的一类元数据。</span><span class="sxs-lookup"><span data-stu-id="054ad-110">In the Child Elements table, policy refers to the kind of metadata that is made available for particular program elements at run time.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="054ad-111">特性</span><span class="sxs-lookup"><span data-stu-id="054ad-111">Attributes</span></span>  
  
|<span data-ttu-id="054ad-112">属性</span><span class="sxs-lookup"><span data-stu-id="054ad-112">Attribute</span></span>|<span data-ttu-id="054ad-113">属性类型</span><span class="sxs-lookup"><span data-stu-id="054ad-113">Attribute type</span></span>|<span data-ttu-id="054ad-114">说明</span><span class="sxs-lookup"><span data-stu-id="054ad-114">Description</span></span>|  
|---------------|--------------------|-----------------|  
|`Activate`|<span data-ttu-id="054ad-115">反射</span><span class="sxs-lookup"><span data-stu-id="054ad-115">Reflection</span></span>|<span data-ttu-id="054ad-116">可选特性。</span><span class="sxs-lookup"><span data-stu-id="054ad-116">Optional attribute.</span></span> <span data-ttu-id="054ad-117">控制运行时对构造函数的访问，以启用实例激活。</span><span class="sxs-lookup"><span data-stu-id="054ad-117">Controls runtime access to constructors to enable activation of instances.</span></span>|  
|`Browse`|<span data-ttu-id="054ad-118">反射</span><span class="sxs-lookup"><span data-stu-id="054ad-118">Reflection</span></span>|<span data-ttu-id="054ad-119">可选特性。</span><span class="sxs-lookup"><span data-stu-id="054ad-119">Optional attribute.</span></span> <span data-ttu-id="054ad-120">控制对该类型信息的查询或列举该类型，但并不在运行时间启用任何动态访问。</span><span class="sxs-lookup"><span data-stu-id="054ad-120">Controls querying for information about or enumerating the types, but does not enable any dynamic access at run time.</span></span>|  
|`Dynamic`|<span data-ttu-id="054ad-121">反射</span><span class="sxs-lookup"><span data-stu-id="054ad-121">Reflection</span></span>|<span data-ttu-id="054ad-122">可选特性。</span><span class="sxs-lookup"><span data-stu-id="054ad-122">Optional attribute.</span></span> <span data-ttu-id="054ad-123">控制运行时对所有类型成员的访问，包括构造函数、方法、字段、属性和事件，以启用动态编程。</span><span class="sxs-lookup"><span data-stu-id="054ad-123">Controls runtime access to all type members, including constructors, methods, fields, properties, and events, to enable dynamic programming.</span></span>|  
|`Serialize`|<span data-ttu-id="054ad-124">序列化</span><span class="sxs-lookup"><span data-stu-id="054ad-124">Serialization</span></span>|<span data-ttu-id="054ad-125">可选特性。</span><span class="sxs-lookup"><span data-stu-id="054ad-125">Optional attribute.</span></span> <span data-ttu-id="054ad-126">控制运行时对构造函数、字段和属性的访问，使类型实例得到序列化和反序列化处理，这是通过库进行的，例如 Newtonsoft JSON 序列化程序。</span><span class="sxs-lookup"><span data-stu-id="054ad-126">Controls runtime access to constructors, fields, and properties, to enable type instances to be serialized and deserialized by libraries such as the Newtonsoft JSON serializer.</span></span>|  
|`DataContractSerializer`|<span data-ttu-id="054ad-127">序列化</span><span class="sxs-lookup"><span data-stu-id="054ad-127">Serialization</span></span>|<span data-ttu-id="054ad-128">可选特性。</span><span class="sxs-lookup"><span data-stu-id="054ad-128">Optional Attribute.</span></span> <span data-ttu-id="054ad-129">控制使用 <xref:System.Runtime.Serialization.DataContractSerializer?displayProperty=nameWithType> 类的序列化策略。</span><span class="sxs-lookup"><span data-stu-id="054ad-129">Controls policy for serialization that uses the <xref:System.Runtime.Serialization.DataContractSerializer?displayProperty=nameWithType> class.</span></span>|  
|`DataContractJsonSerializer`|<span data-ttu-id="054ad-130">序列化</span><span class="sxs-lookup"><span data-stu-id="054ad-130">Serialization</span></span>|<span data-ttu-id="054ad-131">可选特性。</span><span class="sxs-lookup"><span data-stu-id="054ad-131">Optional Attribute.</span></span> <span data-ttu-id="054ad-132">控制使用 <xref:System.Runtime.Serialization.Json.DataContractJsonSerializer?displayProperty=nameWithType> 类的 JSON 序列化策略。</span><span class="sxs-lookup"><span data-stu-id="054ad-132">Controls policy for JSON serialization that uses the <xref:System.Runtime.Serialization.Json.DataContractJsonSerializer?displayProperty=nameWithType> class.</span></span>|  
|`XmlSerializer`|<span data-ttu-id="054ad-133">序列化</span><span class="sxs-lookup"><span data-stu-id="054ad-133">Serialization</span></span>|<span data-ttu-id="054ad-134">可选特性。</span><span class="sxs-lookup"><span data-stu-id="054ad-134">Optional Attribute.</span></span> <span data-ttu-id="054ad-135">控制使用 <xref:System.Xml.Serialization.XmlSerializer?displayProperty=nameWithType> 类的 XML 序列化策略。</span><span class="sxs-lookup"><span data-stu-id="054ad-135">Controls policy for XML serialization that uses the <xref:System.Xml.Serialization.XmlSerializer?displayProperty=nameWithType> class.</span></span>|  
|`MarshalObject`|<span data-ttu-id="054ad-136">Interop</span><span class="sxs-lookup"><span data-stu-id="054ad-136">Interop</span></span>|<span data-ttu-id="054ad-137">可选特性。</span><span class="sxs-lookup"><span data-stu-id="054ad-137">Optional Attribute.</span></span> <span data-ttu-id="054ad-138">控制封送引用类型到 Windows 运行时和 COM 的策略。</span><span class="sxs-lookup"><span data-stu-id="054ad-138">Controls policy for marshaling reference types to Windows Runtime and COM.</span></span>|  
|`MarshalDelegate`|<span data-ttu-id="054ad-139">Interop</span><span class="sxs-lookup"><span data-stu-id="054ad-139">Interop</span></span>|<span data-ttu-id="054ad-140">可选特性。</span><span class="sxs-lookup"><span data-stu-id="054ad-140">Optional Attribute.</span></span> <span data-ttu-id="054ad-141">控制将委托类型作为函数指针封送到本机代码的策略。</span><span class="sxs-lookup"><span data-stu-id="054ad-141">Controls policy for marshaling delegate types as function pointers to native code.</span></span>|  
|`MarshalStructure`|<span data-ttu-id="054ad-142">Interop</span><span class="sxs-lookup"><span data-stu-id="054ad-142">Interop</span></span>|<span data-ttu-id="054ad-143">可选特性。</span><span class="sxs-lookup"><span data-stu-id="054ad-143">Optional Attribute.</span></span> <span data-ttu-id="054ad-144">控制封送结构到本机代码的策略。</span><span class="sxs-lookup"><span data-stu-id="054ad-144">Controls policy for marshaling structures to native code.</span></span>|  
  
## <a name="all-attributes"></a><span data-ttu-id="054ad-145">所有特性</span><span class="sxs-lookup"><span data-stu-id="054ad-145">All attributes</span></span>  
  
|<span data-ttu-id="054ad-146">值</span><span class="sxs-lookup"><span data-stu-id="054ad-146">Value</span></span>|<span data-ttu-id="054ad-147">说明</span><span class="sxs-lookup"><span data-stu-id="054ad-147">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="054ad-148">*策略_设置*</span><span class="sxs-lookup"><span data-stu-id="054ad-148">*policy_setting*</span></span>|<span data-ttu-id="054ad-149">该策略的设置将应用到该应用中的所有类型。</span><span class="sxs-lookup"><span data-stu-id="054ad-149">The setting for this policy to apply to the types in the app.</span></span> <span data-ttu-id="054ad-150">可能值为 `All`、`Auto`、`Excluded`、`Public`、`PublicAndInternal`、`Required Public`、`Required PublicAndInternal` 以及 `Required All`。</span><span class="sxs-lookup"><span data-stu-id="054ad-150">Possible values are `All`, `Auto`, `Excluded`, `Public`, `PublicAndInternal`, `Required Public`, `Required PublicAndInternal`, and `Required All`.</span></span> <span data-ttu-id="054ad-151">有关详细信息，请参阅[运行时指令策略设置](runtime-directive-policy-settings.md)。</span><span class="sxs-lookup"><span data-stu-id="054ad-151">For more information, see [Runtime Directive Policy Settings](runtime-directive-policy-settings.md).</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="054ad-152">子元素</span><span class="sxs-lookup"><span data-stu-id="054ad-152">Child Elements</span></span>  
  
|<span data-ttu-id="054ad-153">元素</span><span class="sxs-lookup"><span data-stu-id="054ad-153">Element</span></span>|<span data-ttu-id="054ad-154">说明</span><span class="sxs-lookup"><span data-stu-id="054ad-154">Description</span></span>|  
|-------------|-----------------|  
|[\<Assembly>](assembly-element-net-native.md)|<span data-ttu-id="054ad-155">将策略应用到特定程序集中的所有类型。</span><span class="sxs-lookup"><span data-stu-id="054ad-155">Applies policy to all the types in a particular assembly.</span></span>|  
|[\<Namespace>](namespace-element-net-native.md)|<span data-ttu-id="054ad-156">将策略应用到特定命名空间中的所有类型。</span><span class="sxs-lookup"><span data-stu-id="054ad-156">Applies policy to all the types in a particular namespace.</span></span>|  
|[\<Type>](type-element-net-native.md)|<span data-ttu-id="054ad-157">将策略应用到一个特定类型，例如一个类或结构。</span><span class="sxs-lookup"><span data-stu-id="054ad-157">Applies policy to a particular type, such as a class or structure.</span></span>|  
|[\<TypeInstantiation>](typeinstantiation-element-net-native.md)|<span data-ttu-id="054ad-158">将策略应用到一个构造泛型类型。</span><span class="sxs-lookup"><span data-stu-id="054ad-158">Applies policy to a constructed generic type.</span></span> <span data-ttu-id="054ad-159">例如， [\<TypeInstantiation>](typeinstantiation-element-net-native.md) 元素可以用于定义类型的策略 `List<String>` 。</span><span class="sxs-lookup"><span data-stu-id="054ad-159">For example, a [\<TypeInstantiation>](typeinstantiation-element-net-native.md) element could be used to define policy for a `List<String>` type.</span></span>|  
|[\<Method>](method-element-net-native.md)|<span data-ttu-id="054ad-160">将策略应用到一个特定类型上的方法。</span><span class="sxs-lookup"><span data-stu-id="054ad-160">Applies policy to a method on a particular type.</span></span>|  
|[\<MethodInstantiation>](methodinstantiation-element-net-native.md)|<span data-ttu-id="054ad-161">将策略应用到一个构造泛型方法。</span><span class="sxs-lookup"><span data-stu-id="054ad-161">Applies policy to a constructed generic method.</span></span>|  
|[\<Property>](property-element-net-native.md)|<span data-ttu-id="054ad-162">将策略应用到一个特定类型上的属性。</span><span class="sxs-lookup"><span data-stu-id="054ad-162">Applies policy to a property on a particular type.</span></span>|  
|[\<Field>](field-element-net-native.md)|<span data-ttu-id="054ad-163">将策略应用到一个特定类型上的字段。</span><span class="sxs-lookup"><span data-stu-id="054ad-163">Applies policy to a field on a particular type.</span></span>|  
|[\<Event>](event-element-net-native.md)|<span data-ttu-id="054ad-164">将策略应用到一个特定类型上的事件。</span><span class="sxs-lookup"><span data-stu-id="054ad-164">Applies policy to an event on a particular type.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="054ad-165">父元素</span><span class="sxs-lookup"><span data-stu-id="054ad-165">Parent Elements</span></span>  
  
|<span data-ttu-id="054ad-166">元素</span><span class="sxs-lookup"><span data-stu-id="054ad-166">Element</span></span>|<span data-ttu-id="054ad-167">说明</span><span class="sxs-lookup"><span data-stu-id="054ad-167">Description</span></span>|  
|-------------|-----------------|  
|[\<Directives>](directives-element-net-native.md)|<span data-ttu-id="054ad-168">运行时指令文件的根元素。</span><span class="sxs-lookup"><span data-stu-id="054ad-168">The root element of a runtime directives file.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="054ad-169">备注</span><span class="sxs-lookup"><span data-stu-id="054ad-169">Remarks</span></span>  

 <span data-ttu-id="054ad-170">[\<Directives>](directives-element-net-native.md)元素可以包含零个或一个 `<Application>` 元素。</span><span class="sxs-lookup"><span data-stu-id="054ad-170">The [\<Directives>](directives-element-net-native.md) element can contain zero or one `<Application>` element.</span></span> <span data-ttu-id="054ad-171">单独一个反射指令文件中出现的多个 `<Application>` 元素不受支持。</span><span class="sxs-lookup"><span data-stu-id="054ad-171">Multiple `<Application>` elements in a single reflection directives file are not supported.</span></span>  
  
 <span data-ttu-id="054ad-172">`<Application>` 元素可通过以下方法之一使用：</span><span class="sxs-lookup"><span data-stu-id="054ad-172">The `<Application>` element can be used in one of two ways:</span></span>  
  
- <span data-ttu-id="054ad-173">作为定义在运行时间需要元数据的程序元素的容器。</span><span class="sxs-lookup"><span data-stu-id="054ad-173">As a container to define the program elements whose metadata is needed at run time.</span></span> <span data-ttu-id="054ad-174">在这种情况下，`<Application>` 元素不需要具有任何特性。</span><span class="sxs-lookup"><span data-stu-id="054ad-174">In this case, the `<Application>` element need not have any attributes.</span></span> <span data-ttu-id="054ad-175">在编译时间，编译器工具搜索 .NET Framework 核心库等所有库，以查找由 `<Application>` 元素的子元素识别出的程序元素。</span><span class="sxs-lookup"><span data-stu-id="054ad-175">At compile time, compiler tools search all libraries, including .NET Framework core libraries, for program elements identified by child elements of the `<Application>` element.</span></span> <span data-ttu-id="054ad-176">与此相反，编译器工具仅搜索由的 [\<Library>](library-element-net-native.md) 子元素标识的程序元素所指定的库 [\<Library>](library-element-net-native.md) 。</span><span class="sxs-lookup"><span data-stu-id="054ad-176">In contrast, compiler tools search only the library designated by the [\<Library>](library-element-net-native.md) element for program elements identified by the child elements of [\<Library>](library-element-net-native.md).</span></span>  
  
- <span data-ttu-id="054ad-177">作为为反射、序列化和互操作设置应用程序范围的策略的元素。</span><span class="sxs-lookup"><span data-stu-id="054ad-177">As an element that sets application-wide policy for reflection, serialization, and interop.</span></span> <span data-ttu-id="054ad-178">元素的特性 `<Application>` 定义应用程序范围的策略，该策略可能由或元素定义的子元素重写 `<Application>` [\<Library>](library-element-net-native.md) 。</span><span class="sxs-lookup"><span data-stu-id="054ad-178">The attributes of the `<Application>` element define application-wide policy, which may be overridden by the child elements defined by the `<Application>` or [\<Library>](library-element-net-native.md) element.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="054ad-179">请参阅</span><span class="sxs-lookup"><span data-stu-id="054ad-179">See also</span></span>

- [<span data-ttu-id="054ad-180">\<Library> 元素</span><span class="sxs-lookup"><span data-stu-id="054ad-180">\<Library> Element</span></span>](library-element-net-native.md)
- [<span data-ttu-id="054ad-181">\<Directives> 元素</span><span class="sxs-lookup"><span data-stu-id="054ad-181">\<Directives> Element</span></span>](directives-element-net-native.md)
- [<span data-ttu-id="054ad-182">运行时指令元素</span><span class="sxs-lookup"><span data-stu-id="054ad-182">Runtime Directive Elements</span></span>](runtime-directive-elements.md)
- [<span data-ttu-id="054ad-183">运行时指令 (rd.xml) 配置文件引用</span><span class="sxs-lookup"><span data-stu-id="054ad-183">Runtime Directives (rd.xml) Configuration File Reference</span></span>](runtime-directives-rd-xml-configuration-file-reference.md)
