---
description: '了解详细信息： <AttributeImplies> 元素 ( .NET Native) '
title: <AttributeImplies>元素 (.NET Native)
ms.date: 03/30/2017
ms.assetid: 82db7193-a860-418b-84fc-fff2fdf2e025
ms.openlocfilehash: 5af1f60f2c1e556281f2f1d392b1a046e52dd277
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99747902"
---
# <a name="attributeimplies-element-net-native"></a><span data-ttu-id="71f17-103">\<AttributeImplies>元素 (.NET Native)</span><span class="sxs-lookup"><span data-stu-id="71f17-103">\<AttributeImplies> Element (.NET Native)</span></span>

<span data-ttu-id="71f17-104">为包含特性应用的代码元素定义策略。</span><span class="sxs-lookup"><span data-stu-id="71f17-104">Defines policy for code elements the containing attribute is applied to.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="71f17-105">语法</span><span class="sxs-lookup"><span data-stu-id="71f17-105">Syntax</span></span>  
  
```xml  
<AttributeImplies Activate="policy_type"  
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
  
## <a name="attributes-and-elements"></a><span data-ttu-id="71f17-106">特性和元素</span><span class="sxs-lookup"><span data-stu-id="71f17-106">Attributes and Elements</span></span>  

 <span data-ttu-id="71f17-107">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="71f17-107">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="71f17-108">特性</span><span class="sxs-lookup"><span data-stu-id="71f17-108">Attributes</span></span>  
  
|<span data-ttu-id="71f17-109">属性</span><span class="sxs-lookup"><span data-stu-id="71f17-109">Attribute</span></span>|<span data-ttu-id="71f17-110">属性类型</span><span class="sxs-lookup"><span data-stu-id="71f17-110">Attribute type</span></span>|<span data-ttu-id="71f17-111">说明</span><span class="sxs-lookup"><span data-stu-id="71f17-111">Description</span></span>|  
|---------------|--------------------|-----------------|  
|`Activate`|<span data-ttu-id="71f17-112">反射</span><span class="sxs-lookup"><span data-stu-id="71f17-112">Reflection</span></span>|<span data-ttu-id="71f17-113">可选特性。</span><span class="sxs-lookup"><span data-stu-id="71f17-113">Optional attribute.</span></span> <span data-ttu-id="71f17-114">控制运行时对构造函数的访问，以启用实例激活。</span><span class="sxs-lookup"><span data-stu-id="71f17-114">Controls runtime access to constructors to enable activation of instances.</span></span>|  
|`Browse`|<span data-ttu-id="71f17-115">反射</span><span class="sxs-lookup"><span data-stu-id="71f17-115">Reflection</span></span>|<span data-ttu-id="71f17-116">可选特性。</span><span class="sxs-lookup"><span data-stu-id="71f17-116">Optional attribute.</span></span> <span data-ttu-id="71f17-117">控制对有关程序元素信息的查询，但并不启用任何运行时访问。</span><span class="sxs-lookup"><span data-stu-id="71f17-117">Controls querying for information about program elements, but does not enable any runtime access.</span></span>|  
|`Dynamic`|<span data-ttu-id="71f17-118">反射</span><span class="sxs-lookup"><span data-stu-id="71f17-118">Reflection</span></span>|<span data-ttu-id="71f17-119">可选特性。</span><span class="sxs-lookup"><span data-stu-id="71f17-119">Optional attribute.</span></span> <span data-ttu-id="71f17-120">控制运行时对所有类型成员的访问，包括构造函数、方法、字段、属性和事件，以启用动态编程。</span><span class="sxs-lookup"><span data-stu-id="71f17-120">Controls runtime access to all type members, including constructors, methods, fields, properties, and events, to enable dynamic programming.</span></span>|  
|`Serialize`|<span data-ttu-id="71f17-121">序列化</span><span class="sxs-lookup"><span data-stu-id="71f17-121">Serialization</span></span>|<span data-ttu-id="71f17-122">可选特性。</span><span class="sxs-lookup"><span data-stu-id="71f17-122">Optional attribute.</span></span> <span data-ttu-id="71f17-123">控制运行时对构造函数、字段和属性的访问，使类型实例得到序列化和反序列化处理，这是通过库进行的，例如 Newtonsoft JSON 序列化程序。</span><span class="sxs-lookup"><span data-stu-id="71f17-123">Controls runtime access to constructors, fields, and properties, to enable type instances to be serialized and deserialized by libraries such as the Newtonsoft JSON serializer.</span></span>|  
|`DataContractSerializer`|<span data-ttu-id="71f17-124">序列化</span><span class="sxs-lookup"><span data-stu-id="71f17-124">Serialization</span></span>|<span data-ttu-id="71f17-125">可选特性。</span><span class="sxs-lookup"><span data-stu-id="71f17-125">Optional attribute.</span></span> <span data-ttu-id="71f17-126">控制使用 <xref:System.Runtime.Serialization.DataContractSerializer?displayProperty=nameWithType> 类的序列化策略。</span><span class="sxs-lookup"><span data-stu-id="71f17-126">Controls policy for serialization that uses the <xref:System.Runtime.Serialization.DataContractSerializer?displayProperty=nameWithType> class.</span></span>|  
|`DataContractJsonSerializer`|<span data-ttu-id="71f17-127">序列化</span><span class="sxs-lookup"><span data-stu-id="71f17-127">Serialization</span></span>|<span data-ttu-id="71f17-128">可选特性。</span><span class="sxs-lookup"><span data-stu-id="71f17-128">Optional attribute.</span></span> <span data-ttu-id="71f17-129">控制使用 <xref:System.Runtime.Serialization.Json.DataContractJsonSerializer?displayProperty=nameWithType> 类的 JSON 序列化策略。</span><span class="sxs-lookup"><span data-stu-id="71f17-129">Controls policy for JSON serialization that uses the <xref:System.Runtime.Serialization.Json.DataContractJsonSerializer?displayProperty=nameWithType> class.</span></span>|  
|`XmlSerializer`|<span data-ttu-id="71f17-130">序列化</span><span class="sxs-lookup"><span data-stu-id="71f17-130">Serialization</span></span>|<span data-ttu-id="71f17-131">可选特性。</span><span class="sxs-lookup"><span data-stu-id="71f17-131">Optional attribute.</span></span> <span data-ttu-id="71f17-132">控制使用 <xref:System.Xml.Serialization.XmlSerializer?displayProperty=nameWithType> 类的 XML 序列化策略。</span><span class="sxs-lookup"><span data-stu-id="71f17-132">Controls policy for XML serialization that uses the <xref:System.Xml.Serialization.XmlSerializer?displayProperty=nameWithType> class.</span></span>|  
|`MarshalObject`|<span data-ttu-id="71f17-133">Interop</span><span class="sxs-lookup"><span data-stu-id="71f17-133">Interop</span></span>|<span data-ttu-id="71f17-134">可选特性。</span><span class="sxs-lookup"><span data-stu-id="71f17-134">Optional attribute.</span></span> <span data-ttu-id="71f17-135">控制封送引用类型到 Windows 运行时和 COM 的策略。</span><span class="sxs-lookup"><span data-stu-id="71f17-135">Controls policy for marshaling reference types to Windows Runtime and COM.</span></span>|  
|`MarshalDelegate`|<span data-ttu-id="71f17-136">Interop</span><span class="sxs-lookup"><span data-stu-id="71f17-136">Interop</span></span>|<span data-ttu-id="71f17-137">可选特性。</span><span class="sxs-lookup"><span data-stu-id="71f17-137">Optional attribute.</span></span> <span data-ttu-id="71f17-138">控制将委托类型作为函数指针封送到本机代码的策略。</span><span class="sxs-lookup"><span data-stu-id="71f17-138">Controls policy for marshaling delegate types as function pointers to native code.</span></span>|  
|`MarshalStructure`|<span data-ttu-id="71f17-139">Interop</span><span class="sxs-lookup"><span data-stu-id="71f17-139">Interop</span></span>|<span data-ttu-id="71f17-140">可选特性。</span><span class="sxs-lookup"><span data-stu-id="71f17-140">Optional attribute.</span></span> <span data-ttu-id="71f17-141">控制封送处理值类型到本机代码的策略。</span><span class="sxs-lookup"><span data-stu-id="71f17-141">Controls policy for marshaling value types to native code.</span></span>|  
  
## <a name="all-attributes"></a><span data-ttu-id="71f17-142">所有特性</span><span class="sxs-lookup"><span data-stu-id="71f17-142">All attributes</span></span>  
  
|<span data-ttu-id="71f17-143">值</span><span class="sxs-lookup"><span data-stu-id="71f17-143">Value</span></span>|<span data-ttu-id="71f17-144">说明</span><span class="sxs-lookup"><span data-stu-id="71f17-144">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="71f17-145">*策略_设置*</span><span class="sxs-lookup"><span data-stu-id="71f17-145">*policy_setting*</span></span>|<span data-ttu-id="71f17-146">该设置将应用到这种策略类型。</span><span class="sxs-lookup"><span data-stu-id="71f17-146">The setting to apply to this policy type.</span></span> <span data-ttu-id="71f17-147">可能值为 `All`、`Auto`、`Excluded`、`Public`、`PublicAndInternal`、`Required Public`、`Required PublicAndInternal` 以及 `Required All`。</span><span class="sxs-lookup"><span data-stu-id="71f17-147">Possible values are `All`, `Auto`, `Excluded`, `Public`, `PublicAndInternal`, `Required Public`, `Required PublicAndInternal`, and `Required All`.</span></span> <span data-ttu-id="71f17-148">有关详细信息，请参阅[运行时指令策略设置](runtime-directive-policy-settings.md)。</span><span class="sxs-lookup"><span data-stu-id="71f17-148">For more information, see [Runtime Directive Policy Settings](runtime-directive-policy-settings.md).</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="71f17-149">子元素</span><span class="sxs-lookup"><span data-stu-id="71f17-149">Child Elements</span></span>  

 <span data-ttu-id="71f17-150">无。</span><span class="sxs-lookup"><span data-stu-id="71f17-150">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="71f17-151">父元素</span><span class="sxs-lookup"><span data-stu-id="71f17-151">Parent Elements</span></span>  
  
|<span data-ttu-id="71f17-152">元素</span><span class="sxs-lookup"><span data-stu-id="71f17-152">Element</span></span>|<span data-ttu-id="71f17-153">说明</span><span class="sxs-lookup"><span data-stu-id="71f17-153">Description</span></span>|  
|-------------|-----------------|  
|[\<Type>](type-element-net-native.md)|<span data-ttu-id="71f17-154">将反射策略应用到一种类型及其所有成员。</span><span class="sxs-lookup"><span data-stu-id="71f17-154">Applies reflection policy to a type and all its members.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="71f17-155">备注</span><span class="sxs-lookup"><span data-stu-id="71f17-155">Remarks</span></span>  

 <span data-ttu-id="71f17-156">如果它的包含类型是一个特性（即，从 `<AttributeImplies>` 中派生出的一个类），则使用 <xref:System.Attribute?displayProperty=nameWithType> 元素。</span><span class="sxs-lookup"><span data-stu-id="71f17-156">The `<AttributeImplies>` element is used if its containing type is an attribute (that is, a class derived from <xref:System.Attribute?displayProperty=nameWithType>).</span></span> <span data-ttu-id="71f17-157">如果该特性被应用到特定的程序元素，由 `<AttributeImplies>` 元素定义的策略将应用到该程序元素。</span><span class="sxs-lookup"><span data-stu-id="71f17-157">If the attribute is applied to a particular program element, the policy defined by the `<AttributeImplies>` element applies to that program element.</span></span>  
  
 <span data-ttu-id="71f17-158">反射、序列化和互操作特性都是可选项，但必须存在至少一项。</span><span class="sxs-lookup"><span data-stu-id="71f17-158">The reflection, serialization, and interop attributes are all optional, although at least one should be present.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="71f17-159">请参阅</span><span class="sxs-lookup"><span data-stu-id="71f17-159">See also</span></span>

- [<span data-ttu-id="71f17-160">\<Type> 元素</span><span class="sxs-lookup"><span data-stu-id="71f17-160">\<Type> Element</span></span>](type-element-net-native.md)
- [<span data-ttu-id="71f17-161">运行时指令 (rd.xml) 配置文件引用</span><span class="sxs-lookup"><span data-stu-id="71f17-161">Runtime Directives (rd.xml) Configuration File Reference</span></span>](runtime-directives-rd-xml-configuration-file-reference.md)
- [<span data-ttu-id="71f17-162">运行时指令元素</span><span class="sxs-lookup"><span data-stu-id="71f17-162">Runtime Directive Elements</span></span>](runtime-directive-elements.md)
- [<span data-ttu-id="71f17-163">运行时指令策略设置</span><span class="sxs-lookup"><span data-stu-id="71f17-163">Runtime Directive Policy Settings</span></span>](runtime-directive-policy-settings.md)
