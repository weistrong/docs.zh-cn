---
description: '了解详细信息： <Event> 元素 ( .NET Native) '
title: <Event>元素 (.NET Native)
ms.date: 03/30/2017
ms.assetid: e53b029c-9d6d-4c0a-9cdc-5cfca8a5ca47
ms.openlocfilehash: 16ef4376e5953da514598bd7cdcbe0c196ee4da5
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99747876"
---
# <a name="event-element-net-native"></a><span data-ttu-id="57fab-103">\<Event>元素 (.NET Native)</span><span class="sxs-lookup"><span data-stu-id="57fab-103">\<Event> Element (.NET Native)</span></span>

<span data-ttu-id="57fab-104">将运行时反射策略应用到一个事件。</span><span class="sxs-lookup"><span data-stu-id="57fab-104">Applies runtime reflection policy to an event.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="57fab-105">语法</span><span class="sxs-lookup"><span data-stu-id="57fab-105">Syntax</span></span>  
  
```xml  
<Event Name="event_name"
       Browse="policy_type"
       Dynamic="policy_type" />  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="57fab-106">特性和元素</span><span class="sxs-lookup"><span data-stu-id="57fab-106">Attributes and Elements</span></span>  

 <span data-ttu-id="57fab-107">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="57fab-107">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="57fab-108">特性</span><span class="sxs-lookup"><span data-stu-id="57fab-108">Attributes</span></span>  
  
|<span data-ttu-id="57fab-109">属性</span><span class="sxs-lookup"><span data-stu-id="57fab-109">Attribute</span></span>|<span data-ttu-id="57fab-110">属性类型</span><span class="sxs-lookup"><span data-stu-id="57fab-110">Attribute type</span></span>|<span data-ttu-id="57fab-111">说明</span><span class="sxs-lookup"><span data-stu-id="57fab-111">Description</span></span>|  
|---------------|--------------------|-----------------|  
|`Name`|<span data-ttu-id="57fab-112">常规</span><span class="sxs-lookup"><span data-stu-id="57fab-112">General</span></span>|<span data-ttu-id="57fab-113">必需的特性。</span><span class="sxs-lookup"><span data-stu-id="57fab-113">Required attribute.</span></span> <span data-ttu-id="57fab-114">指定事件名称。</span><span class="sxs-lookup"><span data-stu-id="57fab-114">Specifies the event name.</span></span>|  
|`Browse`|<span data-ttu-id="57fab-115">反射</span><span class="sxs-lookup"><span data-stu-id="57fab-115">Reflection</span></span>|<span data-ttu-id="57fab-116">可选特性。</span><span class="sxs-lookup"><span data-stu-id="57fab-116">Optional attribute.</span></span> <span data-ttu-id="57fab-117">控制对该事件信息的查询或列举该事件，但并不在运行时间启用任何动态访问。</span><span class="sxs-lookup"><span data-stu-id="57fab-117">Controls querying for information about or enumerating the event but does not enable any dynamic access at run time.</span></span>|  
|`Dynamic`|<span data-ttu-id="57fab-118">反射</span><span class="sxs-lookup"><span data-stu-id="57fab-118">Reflection</span></span>|<span data-ttu-id="57fab-119">可选特性。</span><span class="sxs-lookup"><span data-stu-id="57fab-119">Optional attribute.</span></span> <span data-ttu-id="57fab-120">控制运行时对该事件的访问，以启用动态编程。</span><span class="sxs-lookup"><span data-stu-id="57fab-120">Controls runtime access to the event to enable dynamic programming.</span></span> <span data-ttu-id="57fab-121">该策略确保一个事件可在运行时间内得到处理。</span><span class="sxs-lookup"><span data-stu-id="57fab-121">This policy ensures that an event can be handled dynamically at run time.</span></span>|  
  
## <a name="name-attribute"></a><span data-ttu-id="57fab-122">Name 特性</span><span class="sxs-lookup"><span data-stu-id="57fab-122">Name attribute</span></span>  
  
|<span data-ttu-id="57fab-123">值</span><span class="sxs-lookup"><span data-stu-id="57fab-123">Value</span></span>|<span data-ttu-id="57fab-124">说明</span><span class="sxs-lookup"><span data-stu-id="57fab-124">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="57fab-125">method_name</span><span class="sxs-lookup"><span data-stu-id="57fab-125">*method_name*</span></span>|<span data-ttu-id="57fab-126">事件名称。</span><span class="sxs-lookup"><span data-stu-id="57fab-126">The event name.</span></span> <span data-ttu-id="57fab-127">事件的类型由父级 [\<Type>](type-element-net-native.md) 或 [\<TypeInstantiation>](typeinstantiation-element-net-native.md) 元素定义。</span><span class="sxs-lookup"><span data-stu-id="57fab-127">The type of the event is defined by the parent [\<Type>](type-element-net-native.md) or [\<TypeInstantiation>](typeinstantiation-element-net-native.md) element.</span></span>|  
  
## <a name="all-other-attributes"></a><span data-ttu-id="57fab-128">所有其他特性</span><span class="sxs-lookup"><span data-stu-id="57fab-128">All other attributes</span></span>  
  
|<span data-ttu-id="57fab-129">值</span><span class="sxs-lookup"><span data-stu-id="57fab-129">Value</span></span>|<span data-ttu-id="57fab-130">说明</span><span class="sxs-lookup"><span data-stu-id="57fab-130">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="57fab-131">*策略_设置*</span><span class="sxs-lookup"><span data-stu-id="57fab-131">*policy_setting*</span></span>|<span data-ttu-id="57fab-132">该设置将应用到这个事件的策略类型。</span><span class="sxs-lookup"><span data-stu-id="57fab-132">The setting to apply to this policy type for the event.</span></span> <span data-ttu-id="57fab-133">可能值为 `Auto`、`Excluded`、`Included` 和 `Required`。</span><span class="sxs-lookup"><span data-stu-id="57fab-133">Possible values are `Auto`, `Excluded`, `Included`, and `Required`.</span></span> <span data-ttu-id="57fab-134">有关详细信息，请参阅[运行时指令策略设置](runtime-directive-policy-settings.md)。</span><span class="sxs-lookup"><span data-stu-id="57fab-134">For more information, see [Runtime Directive Policy Settings](runtime-directive-policy-settings.md).</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="57fab-135">子元素</span><span class="sxs-lookup"><span data-stu-id="57fab-135">Child Elements</span></span>  

 <span data-ttu-id="57fab-136">无。</span><span class="sxs-lookup"><span data-stu-id="57fab-136">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="57fab-137">父元素</span><span class="sxs-lookup"><span data-stu-id="57fab-137">Parent Elements</span></span>  
  
|<span data-ttu-id="57fab-138">元素</span><span class="sxs-lookup"><span data-stu-id="57fab-138">Element</span></span>|<span data-ttu-id="57fab-139">说明</span><span class="sxs-lookup"><span data-stu-id="57fab-139">Description</span></span>|  
|-------------|-----------------|  
|[\<Type>](type-element-net-native.md)|<span data-ttu-id="57fab-140">将反射策略应用到一种类型及其所有成员。</span><span class="sxs-lookup"><span data-stu-id="57fab-140">Applies reflection policy to a type and all its members.</span></span>|  
|[\<TypeInstantiation>](typeinstantiation-element-net-native.md)|<span data-ttu-id="57fab-141">将反射策略应用到一种构造泛型类型及其所有成员。</span><span class="sxs-lookup"><span data-stu-id="57fab-141">Applies reflection policy to a constructed generic type and all its members.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="57fab-142">备注</span><span class="sxs-lookup"><span data-stu-id="57fab-142">Remarks</span></span>  

 <span data-ttu-id="57fab-143">如果一个事件的策略没有得到显式定义，它将继承其父元素的运行时策略。</span><span class="sxs-lookup"><span data-stu-id="57fab-143">If an event's policy is not explicitly defined, it inherits the runtime policy of its parent element.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="57fab-144">请参阅</span><span class="sxs-lookup"><span data-stu-id="57fab-144">See also</span></span>

- [<span data-ttu-id="57fab-145">运行时指令 (rd.xml) 配置文件引用</span><span class="sxs-lookup"><span data-stu-id="57fab-145">Runtime Directives (rd.xml) Configuration File Reference</span></span>](runtime-directives-rd-xml-configuration-file-reference.md)
- [<span data-ttu-id="57fab-146">运行时指令元素</span><span class="sxs-lookup"><span data-stu-id="57fab-146">Runtime Directive Elements</span></span>](runtime-directive-elements.md)
- [<span data-ttu-id="57fab-147">运行时指令策略设置</span><span class="sxs-lookup"><span data-stu-id="57fab-147">Runtime Directive Policy Settings</span></span>](runtime-directive-policy-settings.md)
