---
description: '了解详细信息： <MethodInstantiation> 元素 ( .NET Native) '
title: <MethodInstantiation>元素 (.NET Native)
ms.date: 03/30/2017
ms.assetid: a3355d78-2a88-4109-8521-830d7cae260a
ms.openlocfilehash: 985d522a559dbbce936a2f29a9983c89ebd18a48
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99747486"
---
# <a name="methodinstantiation-element-net-native"></a><span data-ttu-id="466ac-103">\<MethodInstantiation>元素 (.NET Native)</span><span class="sxs-lookup"><span data-stu-id="466ac-103">\<MethodInstantiation> Element (.NET Native)</span></span>

<span data-ttu-id="466ac-104">将运行时反射策略应用到一个构造泛型方法。</span><span class="sxs-lookup"><span data-stu-id="466ac-104">Applies runtime reflection policy to a constructed generic method.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="466ac-105">语法</span><span class="sxs-lookup"><span data-stu-id="466ac-105">Syntax</span></span>  
  
```xml  
<MethodInstantiation Name="method_name"  
                     Signature="method_signature"  
                     Arguments="method_arguments"  
                     Browse="policy_type"  
                     Dynamic="policy_type" />  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="466ac-106">特性和元素</span><span class="sxs-lookup"><span data-stu-id="466ac-106">Attributes and Elements</span></span>  

 <span data-ttu-id="466ac-107">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="466ac-107">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="466ac-108">特性</span><span class="sxs-lookup"><span data-stu-id="466ac-108">Attributes</span></span>  
  
|<span data-ttu-id="466ac-109">属性</span><span class="sxs-lookup"><span data-stu-id="466ac-109">Attribute</span></span>|<span data-ttu-id="466ac-110">属性类型</span><span class="sxs-lookup"><span data-stu-id="466ac-110">Attribute type</span></span>|<span data-ttu-id="466ac-111">说明</span><span class="sxs-lookup"><span data-stu-id="466ac-111">Description</span></span>|  
|---------------|--------------------|-----------------|  
|`Name`|<span data-ttu-id="466ac-112">常规</span><span class="sxs-lookup"><span data-stu-id="466ac-112">General</span></span>|<span data-ttu-id="466ac-113">必需的特性。</span><span class="sxs-lookup"><span data-stu-id="466ac-113">Required attribute.</span></span> <span data-ttu-id="466ac-114">指定方法名称。</span><span class="sxs-lookup"><span data-stu-id="466ac-114">Specifies the method name.</span></span>|  
|`Signature`|<span data-ttu-id="466ac-115">常规</span><span class="sxs-lookup"><span data-stu-id="466ac-115">General</span></span>|<span data-ttu-id="466ac-116">可选特性。</span><span class="sxs-lookup"><span data-stu-id="466ac-116">Optional attribute.</span></span> <span data-ttu-id="466ac-117">指定该类型的命名参数。</span><span class="sxs-lookup"><span data-stu-id="466ac-117">Specifies named parameters of the method.</span></span> <span data-ttu-id="466ac-118">多个命名参数由逗号分隔。</span><span class="sxs-lookup"><span data-stu-id="466ac-118">Multiple named parameters are separated by commas.</span></span> <span data-ttu-id="466ac-119">`Signature` 特性用于区分重载方法。</span><span class="sxs-lookup"><span data-stu-id="466ac-119">The `Signature` attribute is used to differentiate overloaded methods.</span></span>|  
|`Arguments`|<span data-ttu-id="466ac-120">常规</span><span class="sxs-lookup"><span data-stu-id="466ac-120">General</span></span>|<span data-ttu-id="466ac-121">必需的特性。</span><span class="sxs-lookup"><span data-stu-id="466ac-121">Required attribute.</span></span> <span data-ttu-id="466ac-122">指定泛型类型参数。</span><span class="sxs-lookup"><span data-stu-id="466ac-122">Specifies the generic type arguments.</span></span> <span data-ttu-id="466ac-123">如果存在多个自变量，它们之间用逗号分割。</span><span class="sxs-lookup"><span data-stu-id="466ac-123">If multiple arguments are present, they are separated by commas.</span></span>|  
|`Browse`|<span data-ttu-id="466ac-124">反射</span><span class="sxs-lookup"><span data-stu-id="466ac-124">Reflection</span></span>|<span data-ttu-id="466ac-125">可选特性。</span><span class="sxs-lookup"><span data-stu-id="466ac-125">Optional attribute.</span></span> <span data-ttu-id="466ac-126">控制对该方法信息的查询或列举该方法，但并不在运行时间启用任何动态调用。</span><span class="sxs-lookup"><span data-stu-id="466ac-126">Controls querying for information about or enumerating a method but does not enable any dynamic invocation at run time.</span></span>|  
|`Dynamic`|<span data-ttu-id="466ac-127">反射</span><span class="sxs-lookup"><span data-stu-id="466ac-127">Reflection</span></span>|<span data-ttu-id="466ac-128">可选特性。</span><span class="sxs-lookup"><span data-stu-id="466ac-128">Optional attribute.</span></span> <span data-ttu-id="466ac-129">控制运行时对构造函数或方法的访问，以启用动态编程。</span><span class="sxs-lookup"><span data-stu-id="466ac-129">Controls runtime access to a constructor or method to enable dynamic programming.</span></span> <span data-ttu-id="466ac-130">该策略确保一个成员可在运行时间内得到调用。</span><span class="sxs-lookup"><span data-stu-id="466ac-130">This policy ensures that a member can be invoked dynamically at run time.</span></span>|  
  
## <a name="name-attribute"></a><span data-ttu-id="466ac-131">Name 特性</span><span class="sxs-lookup"><span data-stu-id="466ac-131">Name attribute</span></span>  
  
|<span data-ttu-id="466ac-132">值</span><span class="sxs-lookup"><span data-stu-id="466ac-132">Value</span></span>|<span data-ttu-id="466ac-133">说明</span><span class="sxs-lookup"><span data-stu-id="466ac-133">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="466ac-134">method_name</span><span class="sxs-lookup"><span data-stu-id="466ac-134">*method_name*</span></span>|<span data-ttu-id="466ac-135">方法名称。</span><span class="sxs-lookup"><span data-stu-id="466ac-135">The method name.</span></span> <span data-ttu-id="466ac-136">方法的类型由父级 [\<Type>](type-element-net-native.md) 或 [\<TypeInstantiation>](typeinstantiation-element-net-native.md) 元素定义。</span><span class="sxs-lookup"><span data-stu-id="466ac-136">The type of the method is defined by the parent [\<Type>](type-element-net-native.md) or [\<TypeInstantiation>](typeinstantiation-element-net-native.md) element.</span></span>|  
  
## <a name="signature-attribute"></a><span data-ttu-id="466ac-137">签名特性</span><span class="sxs-lookup"><span data-stu-id="466ac-137">Signature attribute</span></span>  
  
|<span data-ttu-id="466ac-138">值</span><span class="sxs-lookup"><span data-stu-id="466ac-138">Value</span></span>|<span data-ttu-id="466ac-139">说明</span><span class="sxs-lookup"><span data-stu-id="466ac-139">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="466ac-140">*method_signature*</span><span class="sxs-lookup"><span data-stu-id="466ac-140">*method_signature*</span></span>|<span data-ttu-id="466ac-141">指定该类型的命名参数。</span><span class="sxs-lookup"><span data-stu-id="466ac-141">Specifies the named parameters of the method.</span></span> <span data-ttu-id="466ac-142">如果存在多个参数，它们之间用逗号分割。</span><span class="sxs-lookup"><span data-stu-id="466ac-142">If multiple parameters are present, they are separated by commas.</span></span>|  
  
## <a name="arguments-attribute"></a><span data-ttu-id="466ac-143">自变量特性</span><span class="sxs-lookup"><span data-stu-id="466ac-143">Arguments attribute</span></span>  
  
|<span data-ttu-id="466ac-144">值</span><span class="sxs-lookup"><span data-stu-id="466ac-144">Value</span></span>|<span data-ttu-id="466ac-145">说明</span><span class="sxs-lookup"><span data-stu-id="466ac-145">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="466ac-146">method_arguments</span><span class="sxs-lookup"><span data-stu-id="466ac-146">*method_arguments*</span></span>|<span data-ttu-id="466ac-147">指定泛型类型参数。</span><span class="sxs-lookup"><span data-stu-id="466ac-147">Specifies the generic type arguments.</span></span> <span data-ttu-id="466ac-148">如果存在多个自变量，它们之间用逗号分割。</span><span class="sxs-lookup"><span data-stu-id="466ac-148">If multiple arguments are present, they are separated by commas.</span></span> <span data-ttu-id="466ac-149">每个自变量必须包含一个完全限定的类型名称。</span><span class="sxs-lookup"><span data-stu-id="466ac-149">Each argument must consist of the fully qualified type name.</span></span>|  
  
## <a name="all-other-attributes"></a><span data-ttu-id="466ac-150">所有其他特性</span><span class="sxs-lookup"><span data-stu-id="466ac-150">All other attributes</span></span>  
  
|<span data-ttu-id="466ac-151">值</span><span class="sxs-lookup"><span data-stu-id="466ac-151">Value</span></span>|<span data-ttu-id="466ac-152">说明</span><span class="sxs-lookup"><span data-stu-id="466ac-152">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="466ac-153">*策略_设置*</span><span class="sxs-lookup"><span data-stu-id="466ac-153">*policy_setting*</span></span>|<span data-ttu-id="466ac-154">该设置将应用到这个方法的策略类型。</span><span class="sxs-lookup"><span data-stu-id="466ac-154">The setting to apply to this policy type for the method.</span></span> <span data-ttu-id="466ac-155">可能值为 `Auto`、`Excluded`、`Included` 和 `Required`。</span><span class="sxs-lookup"><span data-stu-id="466ac-155">Possible values are `Auto`, `Excluded`, `Included`, and `Required`.</span></span> <span data-ttu-id="466ac-156">有关详细信息，请参阅[运行时指令策略设置](runtime-directive-policy-settings.md)。</span><span class="sxs-lookup"><span data-stu-id="466ac-156">For more information, see [Runtime Directive Policy Settings](runtime-directive-policy-settings.md).</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="466ac-157">子元素</span><span class="sxs-lookup"><span data-stu-id="466ac-157">Child Elements</span></span>  

 <span data-ttu-id="466ac-158">无。</span><span class="sxs-lookup"><span data-stu-id="466ac-158">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="466ac-159">父元素</span><span class="sxs-lookup"><span data-stu-id="466ac-159">Parent Elements</span></span>  
  
|<span data-ttu-id="466ac-160">元素</span><span class="sxs-lookup"><span data-stu-id="466ac-160">Element</span></span>|<span data-ttu-id="466ac-161">说明</span><span class="sxs-lookup"><span data-stu-id="466ac-161">Description</span></span>|  
|-------------|-----------------|  
|[\<Type>](type-element-net-native.md)|<span data-ttu-id="466ac-162">将反射策略应用到一种类型及其所有成员。</span><span class="sxs-lookup"><span data-stu-id="466ac-162">Applies reflection policy to a type and all its members.</span></span>|  
|[\<TypeInstantiation>](typeinstantiation-element-net-native.md)|<span data-ttu-id="466ac-163">将反射策略应用到一种构造泛型类型及其所有成员。</span><span class="sxs-lookup"><span data-stu-id="466ac-163">Applies reflection policy to a constructed generic type and all its members.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="466ac-164">备注</span><span class="sxs-lookup"><span data-stu-id="466ac-164">Remarks</span></span>  

 <span data-ttu-id="466ac-165">`<MethodInstantiation>` 元素替代其相应的开发泛型方法的运行时反射策略。</span><span class="sxs-lookup"><span data-stu-id="466ac-165">The `<MethodInstantiation>` element overrides the runtime reflection policy of its corresponding open generic method.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="466ac-166">请参阅</span><span class="sxs-lookup"><span data-stu-id="466ac-166">See also</span></span>

- [<span data-ttu-id="466ac-167">运行时指令 (rd.xml) 配置文件引用</span><span class="sxs-lookup"><span data-stu-id="466ac-167">Runtime Directives (rd.xml) Configuration File Reference</span></span>](runtime-directives-rd-xml-configuration-file-reference.md)
- [<span data-ttu-id="466ac-168">运行时指令元素</span><span class="sxs-lookup"><span data-stu-id="466ac-168">Runtime Directive Elements</span></span>](runtime-directive-elements.md)
- [<span data-ttu-id="466ac-169">运行时指令策略设置</span><span class="sxs-lookup"><span data-stu-id="466ac-169">Runtime Directive Policy Settings</span></span>](runtime-directive-policy-settings.md)
- [<span data-ttu-id="466ac-170">\<Method> 元素</span><span class="sxs-lookup"><span data-stu-id="466ac-170">\<Method> Element</span></span>](method-element-net-native.md)
