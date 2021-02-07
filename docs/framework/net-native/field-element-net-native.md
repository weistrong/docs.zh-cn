---
description: '了解详细信息： <Field> 元素 ( .NET Native) '
title: <Field>元素 (.NET Native)
ms.date: 03/30/2017
ms.assetid: 6a14125f-1a8d-41a1-8a32-659ca0ad12de
ms.openlocfilehash: 1f8c8b6720fb90bdc5855da7b17694253bbb7629
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99747837"
---
# <a name="field-element-net-native"></a><span data-ttu-id="26bfe-103">\<Field>元素 (.NET Native)</span><span class="sxs-lookup"><span data-stu-id="26bfe-103">\<Field> Element (.NET Native)</span></span>

<span data-ttu-id="26bfe-104">将运行时反射策略应用到一个字段。</span><span class="sxs-lookup"><span data-stu-id="26bfe-104">Applies runtime reflection policy to a field.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="26bfe-105">语法</span><span class="sxs-lookup"><span data-stu-id="26bfe-105">Syntax</span></span>  
  
```xml  
<Field Name="field_name"  
       Browse="policy_type"  
       Dynamic="policy_type"  
       Serialize="policy_type" />  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="26bfe-106">特性和元素</span><span class="sxs-lookup"><span data-stu-id="26bfe-106">Attributes and Elements</span></span>  

 <span data-ttu-id="26bfe-107">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="26bfe-107">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="26bfe-108">特性</span><span class="sxs-lookup"><span data-stu-id="26bfe-108">Attributes</span></span>  
  
|<span data-ttu-id="26bfe-109">属性</span><span class="sxs-lookup"><span data-stu-id="26bfe-109">Attribute</span></span>|<span data-ttu-id="26bfe-110">属性类型</span><span class="sxs-lookup"><span data-stu-id="26bfe-110">Attribute type</span></span>|<span data-ttu-id="26bfe-111">说明</span><span class="sxs-lookup"><span data-stu-id="26bfe-111">Description</span></span>|  
|---------------|--------------------|-----------------|  
|`Name`|<span data-ttu-id="26bfe-112">常规</span><span class="sxs-lookup"><span data-stu-id="26bfe-112">General</span></span>|<span data-ttu-id="26bfe-113">必需的特性。</span><span class="sxs-lookup"><span data-stu-id="26bfe-113">Required attribute.</span></span> <span data-ttu-id="26bfe-114">指定字段名称。</span><span class="sxs-lookup"><span data-stu-id="26bfe-114">Specifies the field name.</span></span>|  
|`Browse`|<span data-ttu-id="26bfe-115">反射</span><span class="sxs-lookup"><span data-stu-id="26bfe-115">Reflection</span></span>|<span data-ttu-id="26bfe-116">可选特性。</span><span class="sxs-lookup"><span data-stu-id="26bfe-116">Optional attribute.</span></span> <span data-ttu-id="26bfe-117">控制对该字段信息的查询或列举该字段，但并不在运行时间启用任何动态访问。</span><span class="sxs-lookup"><span data-stu-id="26bfe-117">Controls querying for information about or enumerating the field but does not enable any dynamic access at run time.</span></span>|  
|`Dynamic`|<span data-ttu-id="26bfe-118">反射</span><span class="sxs-lookup"><span data-stu-id="26bfe-118">Reflection</span></span>|<span data-ttu-id="26bfe-119">可选特性。</span><span class="sxs-lookup"><span data-stu-id="26bfe-119">Optional attribute.</span></span> <span data-ttu-id="26bfe-120">控制运行时对该字段的访问，以启用动态编程。</span><span class="sxs-lookup"><span data-stu-id="26bfe-120">Controls runtime access to the field to enable dynamic programming.</span></span> <span data-ttu-id="26bfe-121">该策略确保一个字段可在运行时间内得到设置或动态检索。</span><span class="sxs-lookup"><span data-stu-id="26bfe-121">This policy ensures that a field can be set or retrieved dynamically at run time.</span></span>|  
|`Serialize`|<span data-ttu-id="26bfe-122">序列化</span><span class="sxs-lookup"><span data-stu-id="26bfe-122">Serialization</span></span>|<span data-ttu-id="26bfe-123">可选特性。</span><span class="sxs-lookup"><span data-stu-id="26bfe-123">Optional attribute.</span></span> <span data-ttu-id="26bfe-124">控制运行时对一个字段的访问以启用类型实例，使其通过程序库得到序列化，例如通过 Newtonsoft JSON 序列化程序，或被用于绑定数据。</span><span class="sxs-lookup"><span data-stu-id="26bfe-124">Controls runtime access to a field to enable type instances to be serialized by libraries such as the Newtonsoft JSON serializer or to be used for data binding.</span></span>|  
  
## <a name="name-attribute"></a><span data-ttu-id="26bfe-125">Name 特性</span><span class="sxs-lookup"><span data-stu-id="26bfe-125">Name attribute</span></span>  
  
|<span data-ttu-id="26bfe-126">值</span><span class="sxs-lookup"><span data-stu-id="26bfe-126">Value</span></span>|<span data-ttu-id="26bfe-127">说明</span><span class="sxs-lookup"><span data-stu-id="26bfe-127">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="26bfe-128">method_name</span><span class="sxs-lookup"><span data-stu-id="26bfe-128">*method_name*</span></span>|<span data-ttu-id="26bfe-129">字段名。</span><span class="sxs-lookup"><span data-stu-id="26bfe-129">The field name.</span></span> <span data-ttu-id="26bfe-130">字段的类型由父级 [\<Type>](type-element-net-native.md) 或 [\<TypeInstantiation>](typeinstantiation-element-net-native.md) 元素定义。</span><span class="sxs-lookup"><span data-stu-id="26bfe-130">The type of the field is defined by the parent [\<Type>](type-element-net-native.md) or [\<TypeInstantiation>](typeinstantiation-element-net-native.md) element.</span></span>|  
  
## <a name="all-other-attributes"></a><span data-ttu-id="26bfe-131">所有其他特性</span><span class="sxs-lookup"><span data-stu-id="26bfe-131">All other attributes</span></span>  
  
|<span data-ttu-id="26bfe-132">值</span><span class="sxs-lookup"><span data-stu-id="26bfe-132">Value</span></span>|<span data-ttu-id="26bfe-133">说明</span><span class="sxs-lookup"><span data-stu-id="26bfe-133">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="26bfe-134">*策略_设置*</span><span class="sxs-lookup"><span data-stu-id="26bfe-134">*policy_setting*</span></span>|<span data-ttu-id="26bfe-135">该设置将应用到这个字段的策略类型。</span><span class="sxs-lookup"><span data-stu-id="26bfe-135">The setting to apply to this policy type for the field.</span></span> <span data-ttu-id="26bfe-136">可能值为 `Auto`、`Excluded`、`Included` 和 `Required`。</span><span class="sxs-lookup"><span data-stu-id="26bfe-136">Possible values are `Auto`, `Excluded`, `Included`, and `Required`.</span></span> <span data-ttu-id="26bfe-137">有关详细信息，请参阅[运行时指令策略设置](runtime-directive-policy-settings.md)。</span><span class="sxs-lookup"><span data-stu-id="26bfe-137">For more information, see [Runtime Directive Policy Settings](runtime-directive-policy-settings.md).</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="26bfe-138">子元素</span><span class="sxs-lookup"><span data-stu-id="26bfe-138">Child Elements</span></span>  

 <span data-ttu-id="26bfe-139">无。</span><span class="sxs-lookup"><span data-stu-id="26bfe-139">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="26bfe-140">父元素</span><span class="sxs-lookup"><span data-stu-id="26bfe-140">Parent Elements</span></span>  
  
|<span data-ttu-id="26bfe-141">元素</span><span class="sxs-lookup"><span data-stu-id="26bfe-141">Element</span></span>|<span data-ttu-id="26bfe-142">说明</span><span class="sxs-lookup"><span data-stu-id="26bfe-142">Description</span></span>|  
|-------------|-----------------|  
|[\<Type>](type-element-net-native.md)|<span data-ttu-id="26bfe-143">将反射策略应用到一种类型及其所有成员。</span><span class="sxs-lookup"><span data-stu-id="26bfe-143">Applies reflection policy to a type and all its members.</span></span>|  
|[\<TypeInstantiation>](typeinstantiation-element-net-native.md)|<span data-ttu-id="26bfe-144">将反射策略应用到一种构造泛型类型及其所有成员。</span><span class="sxs-lookup"><span data-stu-id="26bfe-144">Applies reflection policy to a constructed generic type and all its members.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="26bfe-145">备注</span><span class="sxs-lookup"><span data-stu-id="26bfe-145">Remarks</span></span>  

 <span data-ttu-id="26bfe-146">如果一个字段的策略没有得到显式定义，它将继承其父元素的运行时策略。</span><span class="sxs-lookup"><span data-stu-id="26bfe-146">If a field's policy is not explicitly defined, it inherits the runtime policy of its parent element.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="26bfe-147">请参阅</span><span class="sxs-lookup"><span data-stu-id="26bfe-147">See also</span></span>

- [<span data-ttu-id="26bfe-148">运行时指令元素</span><span class="sxs-lookup"><span data-stu-id="26bfe-148">Runtime Directive Elements</span></span>](runtime-directive-elements.md)
- [<span data-ttu-id="26bfe-149">运行时指令 (rd.xml) 配置文件引用</span><span class="sxs-lookup"><span data-stu-id="26bfe-149">Runtime Directives (rd.xml) Configuration File Reference</span></span>](runtime-directives-rd-xml-configuration-file-reference.md)
- [<span data-ttu-id="26bfe-150">运行时指令策略设置</span><span class="sxs-lookup"><span data-stu-id="26bfe-150">Runtime Directive Policy Settings</span></span>](runtime-directive-policy-settings.md)
