---
description: 详细了解：属性设计
title: 属性设计
ms.date: 10/22/2008
helpviewer_keywords:
- member design guidelines, properties
- properties [.NET Framework], design guidelines
ms.assetid: 127cbc0c-cbed-48fd-9c89-7c5d4f98f163
ms.openlocfilehash: b2f776a5fb651f8b2e61b750a556704fa6c8c366
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99731794"
---
# <a name="property-design"></a><span data-ttu-id="c13db-103">属性设计</span><span class="sxs-lookup"><span data-stu-id="c13db-103">Property Design</span></span>

<span data-ttu-id="c13db-104">虽然从技术上来说，属性与方法很相似，但它们在使用方案方面大不一样。</span><span class="sxs-lookup"><span data-stu-id="c13db-104">Although properties are technically very similar to methods, they are quite different in terms of their usage scenarios.</span></span> <span data-ttu-id="c13db-105">它们应被视作智能字段。</span><span class="sxs-lookup"><span data-stu-id="c13db-105">They should be seen as smart fields.</span></span> <span data-ttu-id="c13db-106">它们具有字段的调用语法，同时兼备方法的灵活性。</span><span class="sxs-lookup"><span data-stu-id="c13db-106">They have the calling syntax of fields, and the flexibility of methods.</span></span>

 <span data-ttu-id="c13db-107">✔️ 如果调用方不能更改属性的值，则要创建 get-only 属性。</span><span class="sxs-lookup"><span data-stu-id="c13db-107">✔️ DO create get-only properties if the caller should not be able to change the value of the property.</span></span>

 <span data-ttu-id="c13db-108">请记住，如果属性属于可变引用类型，则即使属性是 get-only，也可更改属性值。</span><span class="sxs-lookup"><span data-stu-id="c13db-108">Keep in mind that if the type of the property is a mutable reference type, the property value can be changed even if the property is get-only.</span></span>

 <span data-ttu-id="c13db-109">❌ 请勿提供 set-only 属性，也不要提供其 Setter 可访问性范围比 Getter 大的属性。</span><span class="sxs-lookup"><span data-stu-id="c13db-109">❌ DO NOT provide set-only properties or properties with the setter having broader accessibility than the getter.</span></span>

 <span data-ttu-id="c13db-110">例如，不要使用具有公共 Setter 和受保护的 Getter 的属性。</span><span class="sxs-lookup"><span data-stu-id="c13db-110">For example, do not use properties with a public setter and a protected getter.</span></span>

 <span data-ttu-id="c13db-111">如果无法提供属性 Getter，请改为以方法的形式实现功能。</span><span class="sxs-lookup"><span data-stu-id="c13db-111">If the property getter cannot be provided, implement the functionality as a method instead.</span></span> <span data-ttu-id="c13db-112">请考虑将 `Set` 作为方法名称的开头，后跟你向属性赋予的名称。</span><span class="sxs-lookup"><span data-stu-id="c13db-112">Consider starting the method name with `Set` and follow with what you would have named the property.</span></span> <span data-ttu-id="c13db-113">例如，<xref:System.AppDomain> 有一个名为 `SetCachePath` 的方法，而不是有一个名为 `CachePath` 的 set-only 属性。</span><span class="sxs-lookup"><span data-stu-id="c13db-113">For example, <xref:System.AppDomain> has a method called `SetCachePath` instead of having a set-only property called `CachePath`.</span></span>

 <span data-ttu-id="c13db-114">✔️ 请为所有属性提供敏感默认值，确保默认值不会导致安全漏洞或超级低效的代码。</span><span class="sxs-lookup"><span data-stu-id="c13db-114">✔️ DO provide sensible default values for all properties, ensuring that the defaults do not result in a security hole or terribly inefficient code.</span></span>

 <span data-ttu-id="c13db-115">✔️ 允许以任意顺序设置属性，即使这会导致对象的状态暂时无效也是如此。</span><span class="sxs-lookup"><span data-stu-id="c13db-115">✔️ DO allow properties to be set in any order even if this results in a temporary invalid state of the object.</span></span>

 <span data-ttu-id="c13db-116">普遍的情况是两个或更多属性在一个点上相互关联；在这个点上，鉴于同一对象上其他属性的值，某一属性的某些值可能无效。</span><span class="sxs-lookup"><span data-stu-id="c13db-116">It is common for two or more properties to be interrelated to a point where some values of one property might be invalid given the values of other properties on the same object.</span></span> <span data-ttu-id="c13db-117">在这种情况下，因无效状态导致的异常应当延迟，直到相互关联的属性实际上由该对象一起使用为止。</span><span class="sxs-lookup"><span data-stu-id="c13db-117">In such cases, exceptions resulting from the invalid state should be postponed until the interrelated properties are actually used together by the object.</span></span>

 <span data-ttu-id="c13db-118">✔️ 如果属性 Setter 引发异常，则要保留先前的值。</span><span class="sxs-lookup"><span data-stu-id="c13db-118">✔️ DO preserve the previous value if a property setter throws an exception.</span></span>

 <span data-ttu-id="c13db-119">❌ 避免从属性 Getter 引发异常。</span><span class="sxs-lookup"><span data-stu-id="c13db-119">❌ AVOID throwing exceptions from property getters.</span></span>

 <span data-ttu-id="c13db-120">属性 Getter 应为简单操作，不得具有任何前置条件。</span><span class="sxs-lookup"><span data-stu-id="c13db-120">Property getters should be simple operations and should not have any preconditions.</span></span> <span data-ttu-id="c13db-121">如果 Getter 可能会引发异常，则它可能会被重新设计为方法。</span><span class="sxs-lookup"><span data-stu-id="c13db-121">If a getter can throw an exception, it should probably be redesigned to be a method.</span></span> <span data-ttu-id="c13db-122">请注意，此规则不适用于索引器；在索引器中，我们预计验证参数时会引发异常。</span><span class="sxs-lookup"><span data-stu-id="c13db-122">Notice that this rule does not apply to indexers, where we do expect exceptions as a result of validating the arguments.</span></span>

### <a name="indexed-property-design"></a><span data-ttu-id="c13db-123">索引属性设计</span><span class="sxs-lookup"><span data-stu-id="c13db-123">Indexed Property Design</span></span>

 <span data-ttu-id="c13db-124">索引属性是一种特殊属性，它可具有参数，且可使用与数组索引类似的特殊语法进行调用。</span><span class="sxs-lookup"><span data-stu-id="c13db-124">An indexed property is a special property that can have parameters and can be called with special syntax similar to array indexing.</span></span>

 <span data-ttu-id="c13db-125">索引属性通常被称为索引器。</span><span class="sxs-lookup"><span data-stu-id="c13db-125">Indexed properties are commonly referred to as indexers.</span></span> <span data-ttu-id="c13db-126">索引器应仅在提供对逻辑集合中项目的访问的 API 中使用。</span><span class="sxs-lookup"><span data-stu-id="c13db-126">Indexers should be used only in APIs that provide access to items in a logical collection.</span></span> <span data-ttu-id="c13db-127">例如，字符串是字符的集合，并且已添加了 <xref:System.String?displayProperty=nameWithType> 上的索引器来访问其字符。</span><span class="sxs-lookup"><span data-stu-id="c13db-127">For example, a string is a collection of characters, and the indexer on <xref:System.String?displayProperty=nameWithType> was added to access its characters.</span></span>

 <span data-ttu-id="c13db-128">✔️ 请考虑使用索引器来提供对内部数组中存储的数据的访问。</span><span class="sxs-lookup"><span data-stu-id="c13db-128">✔️ CONSIDER using indexers to provide access to data stored in an internal array.</span></span>

 <span data-ttu-id="c13db-129">✔️ 请考虑对表示项目集合的类型提供索引器。</span><span class="sxs-lookup"><span data-stu-id="c13db-129">✔️ CONSIDER providing indexers on types representing collections of items.</span></span>

 <span data-ttu-id="c13db-130">❌ 不要使用带有多个参数的索引属性。</span><span class="sxs-lookup"><span data-stu-id="c13db-130">❌ AVOID using indexed properties with more than one parameter.</span></span>

 <span data-ttu-id="c13db-131">如果设计需要多个参数，请重新考虑属性是否真的表示逻辑集合的访问器。</span><span class="sxs-lookup"><span data-stu-id="c13db-131">If the design requires multiple parameters, reconsider whether the property really represents an accessor to a logical collection.</span></span> <span data-ttu-id="c13db-132">如果不表示此内容，请改为使用方法。</span><span class="sxs-lookup"><span data-stu-id="c13db-132">If it does not, use methods instead.</span></span> <span data-ttu-id="c13db-133">请考虑以 `Get` 或 `Set` 作为方法名称的开头。</span><span class="sxs-lookup"><span data-stu-id="c13db-133">Consider starting the method name with `Get` or `Set`.</span></span>

 <span data-ttu-id="c13db-134">❌ 避免使用参数类型不是 <xref:System.Int32?displayProperty=nameWithType>、<xref:System.Int64?displayProperty=nameWithType>、<xref:System.String?displayProperty=nameWithType>、<xref:System.Object?displayProperty=nameWithType> 或枚举的索引器。</span><span class="sxs-lookup"><span data-stu-id="c13db-134">❌ AVOID indexers with parameter types other than <xref:System.Int32?displayProperty=nameWithType>, <xref:System.Int64?displayProperty=nameWithType>, <xref:System.String?displayProperty=nameWithType>, <xref:System.Object?displayProperty=nameWithType>, or an enum.</span></span>

 <span data-ttu-id="c13db-135">如果设计需要其他类型的参数，强烈建议重新评估 API 是否真的表示逻辑集合的访问器。</span><span class="sxs-lookup"><span data-stu-id="c13db-135">If the design requires other types of parameters, strongly reevaluate whether the API really represents an accessor to a logical collection.</span></span> <span data-ttu-id="c13db-136">如果不表示此内容，请使用方法。</span><span class="sxs-lookup"><span data-stu-id="c13db-136">If it does not, use a method.</span></span> <span data-ttu-id="c13db-137">请考虑以 `Get` 或 `Set` 作为方法名称的开头。</span><span class="sxs-lookup"><span data-stu-id="c13db-137">Consider starting the method name with `Get` or `Set`.</span></span>

 <span data-ttu-id="c13db-138">✔️ 请对索引属性使用名称 `Item`，除非有明显更好的名称（例如，参见 `System.String` 上的 <xref:System.String.Chars%2A> 属性）。</span><span class="sxs-lookup"><span data-stu-id="c13db-138">✔️ DO use the name `Item` for indexed properties unless there is an obviously better name (e.g., see the <xref:System.String.Chars%2A> property on `System.String`).</span></span>

 <span data-ttu-id="c13db-139">在 C# 中，索引器的默认名称为 Item。</span><span class="sxs-lookup"><span data-stu-id="c13db-139">In C#, indexers are by default named Item.</span></span> <span data-ttu-id="c13db-140"><xref:System.Runtime.CompilerServices.IndexerNameAttribute> 可用于自定义此名称。</span><span class="sxs-lookup"><span data-stu-id="c13db-140">The <xref:System.Runtime.CompilerServices.IndexerNameAttribute> can be used to customize this name.</span></span>

 <span data-ttu-id="c13db-141">❌ 请勿同时提供在语义上等效的索引器和方法。</span><span class="sxs-lookup"><span data-stu-id="c13db-141">❌ DO NOT provide both an indexer and methods that are semantically equivalent.</span></span>

 <span data-ttu-id="c13db-142">❌ 请勿在一个类型中提供多个系列的重载索引器。</span><span class="sxs-lookup"><span data-stu-id="c13db-142">❌ DO NOT provide more than one family of overloaded indexers in one type.</span></span>

 <span data-ttu-id="c13db-143">这是由 C# 编译器实施的。</span><span class="sxs-lookup"><span data-stu-id="c13db-143">This is enforced by the C# compiler.</span></span>

 <span data-ttu-id="c13db-144">❌ 请勿使用非默认的索引属性。</span><span class="sxs-lookup"><span data-stu-id="c13db-144">❌ DO NOT use nondefault indexed properties.</span></span>

 <span data-ttu-id="c13db-145">这是由 C# 编译器实施的。</span><span class="sxs-lookup"><span data-stu-id="c13db-145">This is enforced by the C# compiler.</span></span>

### <a name="property-change-notification-events"></a><span data-ttu-id="c13db-146">属性更改通知事件</span><span class="sxs-lookup"><span data-stu-id="c13db-146">Property Change Notification Events</span></span>

 <span data-ttu-id="c13db-147">有时，提供事件来通知用户属性值出现更改很有用。</span><span class="sxs-lookup"><span data-stu-id="c13db-147">Sometimes it is useful to provide an event notifying the user of changes in a property value.</span></span> <span data-ttu-id="c13db-148">例如，`System.Windows.Forms.Control` 在其 `Text` 属性的值更改后会引发 `TextChanged` 事件。</span><span class="sxs-lookup"><span data-stu-id="c13db-148">For example, `System.Windows.Forms.Control` raises a `TextChanged` event after the value of its `Text` property has changed.</span></span>

 <span data-ttu-id="c13db-149">✔️ 请考虑在高级 API（通常是设计器组件）中的属性值修改时引发更改通知事件。</span><span class="sxs-lookup"><span data-stu-id="c13db-149">✔️ CONSIDER raising change notification events when property values in high-level APIs (usually designer components) are modified.</span></span>

 <span data-ttu-id="c13db-150">如果用户需要在某对象的某个属性出现更改时知道该情况，则该对象应对该属性引发更改通知事件。</span><span class="sxs-lookup"><span data-stu-id="c13db-150">If there is a good scenario for a user to know when a property of an object is changing, the object should raise a change notification event for the property.</span></span>

 <span data-ttu-id="c13db-151">不过，对于基类型或基础集合等低级 API，引发此类事件的开销太大，不太值得这样做。</span><span class="sxs-lookup"><span data-stu-id="c13db-151">However, it is unlikely to be worth the overhead to raise such events for low-level APIs such as base types or collections.</span></span> <span data-ttu-id="c13db-152">例如，当新项目添加到列表且 `Count` 属性更改时，<xref:System.Collections.Generic.List%601> 不会引发此类事件。</span><span class="sxs-lookup"><span data-stu-id="c13db-152">For example, <xref:System.Collections.Generic.List%601> would not raise such events when a new item is added to the list and the `Count` property changes.</span></span>

 <span data-ttu-id="c13db-153">✔️ 请考虑当属性的值通过外部强制操作发生更改时引发更改通知事件。</span><span class="sxs-lookup"><span data-stu-id="c13db-153">✔️ CONSIDER raising change notification events when the value of a property changes via external forces.</span></span>

 <span data-ttu-id="c13db-154">如果某属性值通过某个外部强制操作（通过在对象上调用方法之外的方式），则会引发事件，向开发人员指出该值正在更改且已经更改。</span><span class="sxs-lookup"><span data-stu-id="c13db-154">If a property value changes via some external force (in a way other than by calling methods on the object), raise events indicate to the developer that the value is changing and has changed.</span></span> <span data-ttu-id="c13db-155">文本框控件的 `Text` 属性就是一个很好的例子。</span><span class="sxs-lookup"><span data-stu-id="c13db-155">A good example is the `Text` property of a text box control.</span></span> <span data-ttu-id="c13db-156">当用户在 `TextBox` 中键入文本时，属性值会自动更改。</span><span class="sxs-lookup"><span data-stu-id="c13db-156">When the user types text in a `TextBox`, the property value automatically changes.</span></span>

 <span data-ttu-id="c13db-157">*Portions © 2005, 2009 Microsoft Corporation 版权所有。保留所有权利。*</span><span class="sxs-lookup"><span data-stu-id="c13db-157">*Portions © 2005, 2009 Microsoft Corporation. All rights reserved.*</span></span>

 <span data-ttu-id="c13db-158">*在 Pearson Education, Inc. 授权下，由 Addison-Wesley Professional 作为 Microsoft Windows 开发系列的一部分再版自 [Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619)（Framework 设计准则：可重用 .NET 库的约定、惯例和模式第 2 版），由 Krzysztof Cwalina 和 Brad Abrams 发布于 2008 年 10 月 22 日。*</span><span class="sxs-lookup"><span data-stu-id="c13db-158">*Reprinted by permission of Pearson Education, Inc. from [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) by Krzysztof Cwalina and Brad Abrams, published Oct 22, 2008 by Addison-Wesley Professional as part of the Microsoft Windows Development Series.*</span></span>

## <a name="see-also"></a><span data-ttu-id="c13db-159">请参阅</span><span class="sxs-lookup"><span data-stu-id="c13db-159">See also</span></span>

- [<span data-ttu-id="c13db-160">成员设计准则</span><span class="sxs-lookup"><span data-stu-id="c13db-160">Member Design Guidelines</span></span>](member.md)
- [<span data-ttu-id="c13db-161">框架设计指南</span><span class="sxs-lookup"><span data-stu-id="c13db-161">Framework Design Guidelines</span></span>](index.md)
