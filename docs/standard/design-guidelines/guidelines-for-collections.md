---
description: 详细了解：集合准则
title: 集合准则
ms.date: 10/22/2008
ms.assetid: 297b8f1d-b11f-4dc6-960a-8e990817304e
ms.openlocfilehash: fa189068e9f3e06b3e88999bd4b0ea0998cd16e3
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99642027"
---
# <a name="guidelines-for-collections"></a><span data-ttu-id="a09ae-103">集合准则</span><span class="sxs-lookup"><span data-stu-id="a09ae-103">Guidelines for Collections</span></span>

<span data-ttu-id="a09ae-104">专为操作一组具有某些共同特性的对象而设计的类型都可被视为一个集合。</span><span class="sxs-lookup"><span data-stu-id="a09ae-104">Any type designed specifically to manipulate a group of objects having some common characteristic can be considered a collection.</span></span> <span data-ttu-id="a09ae-105">这种类型几乎总是适合实现 <xref:System.Collections.IEnumerable> 或 <xref:System.Collections.Generic.IEnumerable%601>，因此在本部分中，我们仅将实现其中一个或全部两个接口的类型视为集合。</span><span class="sxs-lookup"><span data-stu-id="a09ae-105">It is almost always appropriate for such types to implement <xref:System.Collections.IEnumerable> or <xref:System.Collections.Generic.IEnumerable%601>, so in this section we only consider types implementing one or both of those interfaces to be collections.</span></span>

 <span data-ttu-id="a09ae-106">❌ 请勿在公共 API 中使用弱类型集合。</span><span class="sxs-lookup"><span data-stu-id="a09ae-106">❌ DO NOT use weakly typed collections in public APIs.</span></span>

 <span data-ttu-id="a09ae-107">表示集合项目的所有返回值和参数的类型都应该是确切的项目类型，而不是其任何基类型（这仅适用于集合的公共成员）。</span><span class="sxs-lookup"><span data-stu-id="a09ae-107">The type of all return values and parameters representing collection items should be the exact item type, not any of its base types (this applies only to public members of the collection).</span></span>

 <span data-ttu-id="a09ae-108">❌ 请勿在公共 API 中使用 <xref:System.Collections.ArrayList> 和 <xref:System.Collections.Generic.List%601>。</span><span class="sxs-lookup"><span data-stu-id="a09ae-108">❌ DO NOT use <xref:System.Collections.ArrayList> or <xref:System.Collections.Generic.List%601> in public APIs.</span></span>

 <span data-ttu-id="a09ae-109">这些类型是数据结构，根据设计可用于内部实现，不可用于公共 API。</span><span class="sxs-lookup"><span data-stu-id="a09ae-109">These types are data structures designed to be used in internal implementation, not in public APIs.</span></span> <span data-ttu-id="a09ae-110">`List<T>` 针对性能和功能进行了优化，代价是灵活性和 API 的简洁度。</span><span class="sxs-lookup"><span data-stu-id="a09ae-110">`List<T>` is optimized for performance and power at the cost of cleanness of the APIs and flexibility.</span></span> <span data-ttu-id="a09ae-111">例如，如果你返回 `List<T>`，则你将永远无法在客户端代码修改集合时收到通知。</span><span class="sxs-lookup"><span data-stu-id="a09ae-111">For example, if you return `List<T>`, you will not ever be able to receive notifications when client code modifies the collection.</span></span> <span data-ttu-id="a09ae-112">此外，`List<T>` 会公开很多成员（例如 <xref:System.Collections.Generic.List%601.BinarySearch%2A>），它们在很多方案中没有用或不适用。</span><span class="sxs-lookup"><span data-stu-id="a09ae-112">Also, `List<T>` exposes many members, such as <xref:System.Collections.Generic.List%601.BinarySearch%2A>, that are not useful or applicable in many scenarios.</span></span> <span data-ttu-id="a09ae-113">以下两部分描述了为在公共 API 中使用而专门设计的类型（抽象）。</span><span class="sxs-lookup"><span data-stu-id="a09ae-113">The following two sections describe types (abstractions) designed specifically for use in public APIs.</span></span>

 <span data-ttu-id="a09ae-114">❌ 请勿在公共 API 中使用 `Hashtable` 和 `Dictionary<TKey,TValue>`。</span><span class="sxs-lookup"><span data-stu-id="a09ae-114">❌ DO NOT use `Hashtable` or `Dictionary<TKey,TValue>` in public APIs.</span></span>

 <span data-ttu-id="a09ae-115">这些类型是数据结构，根据设计可用于内部实现。</span><span class="sxs-lookup"><span data-stu-id="a09ae-115">These types are data structures designed to be used in internal implementation.</span></span> <span data-ttu-id="a09ae-116">公共 API 应使用 <xref:System.Collections.IDictionary>、`IDictionary <TKey, TValue>`，或者使用实现其中一个或全部两个接口的自定义类型。</span><span class="sxs-lookup"><span data-stu-id="a09ae-116">Public APIs should use <xref:System.Collections.IDictionary>, `IDictionary <TKey, TValue>`, or a custom type implementing one or both of the interfaces.</span></span>

 <span data-ttu-id="a09ae-117">❌ 请勿使用 <xref:System.Collections.Generic.IEnumerator%601> 和 <xref:System.Collections.IEnumerator>，也不要使用其他实现上述任一接口的类型，作为 `GetEnumerator` 方法的返回类型的除外。</span><span class="sxs-lookup"><span data-stu-id="a09ae-117">❌ DO NOT use <xref:System.Collections.Generic.IEnumerator%601>, <xref:System.Collections.IEnumerator>, or any other type that implements either of these interfaces, except as the return type of a `GetEnumerator` method.</span></span>

 <span data-ttu-id="a09ae-118">从 `GetEnumerator` 之外的方法返回枚举器的类型不可与 `foreach` 语句一起使用。</span><span class="sxs-lookup"><span data-stu-id="a09ae-118">Types returning enumerators from methods other than `GetEnumerator` cannot be used with the `foreach` statement.</span></span>

 <span data-ttu-id="a09ae-119">❌ 请勿在同一类型上同时实现 `IEnumerator<T>` 和 `IEnumerable<T>`。</span><span class="sxs-lookup"><span data-stu-id="a09ae-119">❌ DO NOT implement both `IEnumerator<T>` and `IEnumerable<T>` on the same type.</span></span> <span data-ttu-id="a09ae-120">这同样适用于非泛型接口 `IEnumerator` 和 `IEnumerable`。</span><span class="sxs-lookup"><span data-stu-id="a09ae-120">The same applies to the nongeneric interfaces `IEnumerator` and `IEnumerable`.</span></span>

## <a name="collection-parameters"></a><span data-ttu-id="a09ae-121">集合参数</span><span class="sxs-lookup"><span data-stu-id="a09ae-121">Collection Parameters</span></span>

 <span data-ttu-id="a09ae-122">✔️ 请尽量使用专业化程度最小的类型作为参数类型。</span><span class="sxs-lookup"><span data-stu-id="a09ae-122">✔️ DO use the least-specialized type possible as a parameter type.</span></span> <span data-ttu-id="a09ae-123">将集合作为参数的大多数成员使用的是 `IEnumerable<T>` 接口。</span><span class="sxs-lookup"><span data-stu-id="a09ae-123">Most members taking collections as parameters use the `IEnumerable<T>` interface.</span></span>

 <span data-ttu-id="a09ae-124">❌ 如果仅是为了访问 `Count` 属性，请避免使用 <xref:System.Collections.Generic.ICollection%601> 和 <xref:System.Collections.ICollection>。</span><span class="sxs-lookup"><span data-stu-id="a09ae-124">❌ AVOID using <xref:System.Collections.Generic.ICollection%601> or <xref:System.Collections.ICollection> as a parameter just to access the `Count` property.</span></span>

 <span data-ttu-id="a09ae-125">转而请考虑使用 `IEnumerable<T>` 或 `IEnumerable`，并动态检查对象是否实现 `ICollection<T>` 或 `ICollection`。</span><span class="sxs-lookup"><span data-stu-id="a09ae-125">Instead, consider using `IEnumerable<T>` or `IEnumerable` and dynamically checking whether the object implements `ICollection<T>` or `ICollection`.</span></span>

## <a name="collection-properties-and-return-values"></a><span data-ttu-id="a09ae-126">集合属性和返回值</span><span class="sxs-lookup"><span data-stu-id="a09ae-126">Collection Properties and Return Values</span></span>

 <span data-ttu-id="a09ae-127">❌ 请勿提供可设置的集合属性。</span><span class="sxs-lookup"><span data-stu-id="a09ae-127">❌ DO NOT provide settable collection properties.</span></span>

 <span data-ttu-id="a09ae-128">用户可先清除集合，然后添加新内容来替换集合的内容。</span><span class="sxs-lookup"><span data-stu-id="a09ae-128">Users can replace the contents of the collection by clearing the collection first and then adding the new contents.</span></span> <span data-ttu-id="a09ae-129">如果常见的情况是替换整个集合，则请考虑对集合提供 `AddRange` 方法。</span><span class="sxs-lookup"><span data-stu-id="a09ae-129">If replacing the whole collection is a common scenario, consider providing the `AddRange` method on the collection.</span></span>

 <span data-ttu-id="a09ae-130">✔️ 请对表示读取/写入集合的属性或返回值使用 `Collection<T>` 或 `Collection<T>` 的子类。</span><span class="sxs-lookup"><span data-stu-id="a09ae-130">✔️ DO use `Collection<T>` or a subclass of `Collection<T>` for properties or return values representing read/write collections.</span></span>

 <span data-ttu-id="a09ae-131">如果 `Collection<T>` 不满足某些要求（例如集合不得实现 <xref:System.Collections.IList>），请通过实现 `IEnumerable<T>`、`ICollection<T>` 或 <xref:System.Collections.Generic.IList%601> 来使用自定义集合。</span><span class="sxs-lookup"><span data-stu-id="a09ae-131">If `Collection<T>` does not meet some requirement (e.g., the collection must not implement <xref:System.Collections.IList>), use a custom collection by implementing `IEnumerable<T>`, `ICollection<T>`, or <xref:System.Collections.Generic.IList%601>.</span></span>

 <span data-ttu-id="a09ae-132">✔️ 请对表示只读集合的属性或返回值使用 `ReadOnlyCollection<T>` 的子类或 <xref:System.Collections.ObjectModel.ReadOnlyCollection%601>，在极少的情况下请使用 `IEnumerable<T>`。</span><span class="sxs-lookup"><span data-stu-id="a09ae-132">✔️ DO use <xref:System.Collections.ObjectModel.ReadOnlyCollection%601>, a subclass of `ReadOnlyCollection<T>`, or in rare cases `IEnumerable<T>` for properties or return values representing read-only collections.</span></span>

 <span data-ttu-id="a09ae-133">通常，请优先选择 `ReadOnlyCollection<T>`。</span><span class="sxs-lookup"><span data-stu-id="a09ae-133">In general, prefer `ReadOnlyCollection<T>`.</span></span> <span data-ttu-id="a09ae-134">如果它不满足某些要求（例如集合不得实现 `IList`），请通过实现 `IEnumerable<T>`、`ICollection<T>` 或 `IList<T>` 来使用自定义集合。</span><span class="sxs-lookup"><span data-stu-id="a09ae-134">If it does not meet some requirement (e.g., the collection must not implement `IList`), use a custom collection by implementing `IEnumerable<T>`, `ICollection<T>`, or `IList<T>`.</span></span> <span data-ttu-id="a09ae-135">如果要实现自定义只读集合，请实现 `ICollection<T>.IsReadOnly` 来返回 `true`。</span><span class="sxs-lookup"><span data-stu-id="a09ae-135">If you do implement a custom read-only collection, implement `ICollection<T>.IsReadOnly` to return `true`.</span></span>

 <span data-ttu-id="a09ae-136">如果你确定你只想支持的方案是仅向前迭代，那么使用 `IEnumerable<T>` 即可。</span><span class="sxs-lookup"><span data-stu-id="a09ae-136">In cases where you are sure that the only scenario you will ever want to support is forward-only iteration, you can simply use `IEnumerable<T>`.</span></span>

 <span data-ttu-id="a09ae-137">✔️ 请考虑使用泛型基础集合的子类，而不是直接使用集合。</span><span class="sxs-lookup"><span data-stu-id="a09ae-137">✔️ CONSIDER using subclasses of generic base collections instead of using the collections directly.</span></span>

 <span data-ttu-id="a09ae-138">这样可进行更好的命名，还可添加基础集合类型上不存在的帮助程序成员。</span><span class="sxs-lookup"><span data-stu-id="a09ae-138">This allows for a better name and for adding helper members that are not present on the base collection types.</span></span> <span data-ttu-id="a09ae-139">这尤其适用于高级 API。</span><span class="sxs-lookup"><span data-stu-id="a09ae-139">This is especially applicable to high-level APIs.</span></span>

 <span data-ttu-id="a09ae-140">✔️ 请考虑从超级常用的方法和属性返回 `Collection<T>` 或 `ReadOnlyCollection<T>` 的子类。</span><span class="sxs-lookup"><span data-stu-id="a09ae-140">✔️ CONSIDER returning a subclass of `Collection<T>` or `ReadOnlyCollection<T>` from very commonly used methods and properties.</span></span>

 <span data-ttu-id="a09ae-141">这样，你就能在将来添加帮助程序方法或更改集合实现。</span><span class="sxs-lookup"><span data-stu-id="a09ae-141">This will make it possible for you to add helper methods or change the collection implementation in the future.</span></span>

 <span data-ttu-id="a09ae-142">✔️ 如果集合中存储的项目具有唯一键（名称、ID 等），请考虑使用键控集合。</span><span class="sxs-lookup"><span data-stu-id="a09ae-142">✔️ CONSIDER using a keyed collection if the items stored in the collection have unique keys (names, IDs, etc.).</span></span> <span data-ttu-id="a09ae-143">键控集合可同时由整数和键编制索引，它们通常通过从 `KeyedCollection<TKey,TItem>` 继承来实现。</span><span class="sxs-lookup"><span data-stu-id="a09ae-143">Keyed collections are collections that can be indexed by both an integer and a key and are usually implemented by inheriting from `KeyedCollection<TKey,TItem>`.</span></span>

 <span data-ttu-id="a09ae-144">键控集合通常会占用更大的内存，如果内存开销的权重比拥有键的优点高，那么不得使用这类集合。</span><span class="sxs-lookup"><span data-stu-id="a09ae-144">Keyed collections usually have larger memory footprints and should not be used if the memory overhead outweighs the benefits of having the keys.</span></span>

 <span data-ttu-id="a09ae-145">❌ 请勿从集合属性返回 NULL 值，也不要从返回集合的方法中返回 NULL 值。</span><span class="sxs-lookup"><span data-stu-id="a09ae-145">❌ DO NOT return null values from collection properties or from methods returning collections.</span></span> <span data-ttu-id="a09ae-146">转而请返回空集合或空数组。</span><span class="sxs-lookup"><span data-stu-id="a09ae-146">Return an empty collection or an empty array instead.</span></span>

 <span data-ttu-id="a09ae-147">一般规则是应将 NULL 集合和空（0 项目）集合/数组视为相同。</span><span class="sxs-lookup"><span data-stu-id="a09ae-147">The general rule is that null and empty (0 item) collections or arrays should be treated the same.</span></span>

### <a name="snapshots-versus-live-collections"></a><span data-ttu-id="a09ae-148">快照与活动集合</span><span class="sxs-lookup"><span data-stu-id="a09ae-148">Snapshots Versus Live Collections</span></span>

 <span data-ttu-id="a09ae-149">表示某时间点的某状态的集合被称为快照集合。</span><span class="sxs-lookup"><span data-stu-id="a09ae-149">Collections representing a state at some point in time are called snapshot collections.</span></span> <span data-ttu-id="a09ae-150">例如，包含从数据库查询返回的行的集合是一个快照。</span><span class="sxs-lookup"><span data-stu-id="a09ae-150">For example, a collection containing rows returned from a database query would be a snapshot.</span></span> <span data-ttu-id="a09ae-151">始终表示当前状态的集合被称为活动集合。</span><span class="sxs-lookup"><span data-stu-id="a09ae-151">Collections that always represent the current state are called live collections.</span></span> <span data-ttu-id="a09ae-152">例如，`ComboBox` 项目的集合是一个活动集合。</span><span class="sxs-lookup"><span data-stu-id="a09ae-152">For example, a collection of `ComboBox` items is a live collection.</span></span>

 <span data-ttu-id="a09ae-153">❌ 请勿从属性返回快照集合。</span><span class="sxs-lookup"><span data-stu-id="a09ae-153">❌ DO NOT return snapshot collections from properties.</span></span> <span data-ttu-id="a09ae-154">属性应返回活动集合。</span><span class="sxs-lookup"><span data-stu-id="a09ae-154">Properties should return live collections.</span></span>

 <span data-ttu-id="a09ae-155">属性 Getter 应该是非常轻量的操作。</span><span class="sxs-lookup"><span data-stu-id="a09ae-155">Property getters should be very lightweight operations.</span></span> <span data-ttu-id="a09ae-156">要返回快照，需要在 O(n) 操作中创建内部集合的副本。</span><span class="sxs-lookup"><span data-stu-id="a09ae-156">Returning a snapshot requires creating a copy of an internal collection in an O(n) operation.</span></span>

 <span data-ttu-id="a09ae-157">✔️ 请使用快照集合或活动 `IEnumerable<T>`（或其子类型）表示可变的集合（“可变”是指可在不显式修改集合的情况下进行更改）。</span><span class="sxs-lookup"><span data-stu-id="a09ae-157">✔️ DO use either a snapshot collection or a live `IEnumerable<T>` (or its subtype) to represent collections that are volatile (i.e., that can change without explicitly modifying the collection).</span></span>

 <span data-ttu-id="a09ae-158">通常，表示共享资源（例如目录中的文件）的所有集合都是可变的。</span><span class="sxs-lookup"><span data-stu-id="a09ae-158">In general, all collections representing a shared resource (e.g., files in a directory) are volatile.</span></span> <span data-ttu-id="a09ae-159">这种集合很难或不可能作为活动集合实现，除非实现只是一个仅前进枚举器。</span><span class="sxs-lookup"><span data-stu-id="a09ae-159">Such collections are very difficult or impossible to implement as live collections unless the implementation is simply a forward-only enumerator.</span></span>

## <a name="choosing-between-arrays-and-collections"></a><span data-ttu-id="a09ae-160">在数组和集合之间进行选择</span><span class="sxs-lookup"><span data-stu-id="a09ae-160">Choosing Between Arrays and Collections</span></span>

 <span data-ttu-id="a09ae-161">✔️ 相对于数组，请优选集合。</span><span class="sxs-lookup"><span data-stu-id="a09ae-161">✔️ DO prefer collections over arrays.</span></span>

 <span data-ttu-id="a09ae-162">集合可让你更大程度地控制内容，它们随时间的推移而变化，而且更易于使用。</span><span class="sxs-lookup"><span data-stu-id="a09ae-162">Collections provide more control over contents, can evolve over time, and are more usable.</span></span> <span data-ttu-id="a09ae-163">此外，不建议对只读方案使用数组，原因是克隆数组的成本过高。</span><span class="sxs-lookup"><span data-stu-id="a09ae-163">In addition, using arrays for read-only scenarios is discouraged because the cost of cloning the array is prohibitive.</span></span> <span data-ttu-id="a09ae-164">可用性调查显示，某些开发人员感觉更喜欢使用基于集合的 API。</span><span class="sxs-lookup"><span data-stu-id="a09ae-164">Usability studies have shown that some developers feel more comfortable using collection-based APIs.</span></span>

 <span data-ttu-id="a09ae-165">不过，如果你要开发低级 API，则对读写方案使用数组可能效果更好。</span><span class="sxs-lookup"><span data-stu-id="a09ae-165">However, if you are developing low-level APIs, it might be better to use arrays for read-write scenarios.</span></span> <span data-ttu-id="a09ae-166">数组的内存占用更小，这有助于减少工作集，而且由于数组已由运行时进行优化，因此可更快地访问数组中的元素。</span><span class="sxs-lookup"><span data-stu-id="a09ae-166">Arrays have a smaller memory footprint, which helps reduce the working set, and access to elements in an array is faster because it is optimized by the runtime.</span></span>

 <span data-ttu-id="a09ae-167">✔️ 请考虑在低级 API 中使用数组来尽量减少内存耗用和尽量提高性能。</span><span class="sxs-lookup"><span data-stu-id="a09ae-167">✔️ CONSIDER using arrays in low-level APIs to minimize memory consumption and maximize performance.</span></span>

 <span data-ttu-id="a09ae-168">✔️ 请使用字节数组而不是字节集合。</span><span class="sxs-lookup"><span data-stu-id="a09ae-168">✔️ DO use byte arrays instead of collections of bytes.</span></span>

 <span data-ttu-id="a09ae-169">❌ 如果每次调用属性 Getter 时，属性都必须返回新数组（例如内部数组的副本），那么请勿对属性使用数组。</span><span class="sxs-lookup"><span data-stu-id="a09ae-169">❌ DO NOT use arrays for properties if the property would have to return a new array (e.g., a copy of an internal array) every time the property getter is called.</span></span>

## <a name="implementing-custom-collections"></a><span data-ttu-id="a09ae-170">实现自定义集合</span><span class="sxs-lookup"><span data-stu-id="a09ae-170">Implementing Custom Collections</span></span>

 <span data-ttu-id="a09ae-171">✔️ 设计新集合时，请考虑从 `Collection<T>`、`ReadOnlyCollection<T>` 或 `KeyedCollection<TKey,TItem>` 中继承。</span><span class="sxs-lookup"><span data-stu-id="a09ae-171">✔️ CONSIDER inheriting from `Collection<T>`, `ReadOnlyCollection<T>`, or `KeyedCollection<TKey,TItem>` when designing new collections.</span></span>

 <span data-ttu-id="a09ae-172">✔️ 设计新集合时，请实现 `IEnumerable<T>`。</span><span class="sxs-lookup"><span data-stu-id="a09ae-172">✔️ DO implement `IEnumerable<T>` when designing new collections.</span></span> <span data-ttu-id="a09ae-173">请考虑实现 `ICollection<T>`或者甚至实现 `IList<T>`（如果合理的话）。</span><span class="sxs-lookup"><span data-stu-id="a09ae-173">Consider implementing `ICollection<T>` or even `IList<T>` where it makes sense.</span></span>

 <span data-ttu-id="a09ae-174">实现此类自定义集合时，请尽可能严格遵守由 `Collection<T>` 和 `ReadOnlyCollection<T>` 建立的 API 模式。</span><span class="sxs-lookup"><span data-stu-id="a09ae-174">When implementing such custom collection, follow the API pattern established by `Collection<T>` and `ReadOnlyCollection<T>` as closely as possible.</span></span> <span data-ttu-id="a09ae-175">也就是说，显式实现相同的成员，对如同这两个集合一样的参数进行命名等等。</span><span class="sxs-lookup"><span data-stu-id="a09ae-175">That is, implement the same members explicitly, name the parameters like these two collections name them, and so on.</span></span>

 <span data-ttu-id="a09ae-176">✔️ 如果集合通常会传递到将非泛型集合接口（`IList` 和 `ICollection`）视为输入的 API，那么请考虑实现这些接口。</span><span class="sxs-lookup"><span data-stu-id="a09ae-176">✔️ CONSIDER implementing nongeneric collection interfaces (`IList` and `ICollection`) if the collection will often be passed to APIs taking these interfaces as input.</span></span>

 <span data-ttu-id="a09ae-177">❌ 对于具有与集合概念无关的复杂 API 的类型，请避免实现集合接口。</span><span class="sxs-lookup"><span data-stu-id="a09ae-177">❌ AVOID implementing collection interfaces on types with complex APIs unrelated to the concept of a collection.</span></span>

 <span data-ttu-id="a09ae-178">❌ 请勿从非泛型基础集合（例如 `CollectionBase`）进行继承。</span><span class="sxs-lookup"><span data-stu-id="a09ae-178">❌ DO NOT inherit from nongeneric base collections such as `CollectionBase`.</span></span> <span data-ttu-id="a09ae-179">请改为使用 `Collection<T>`、`ReadOnlyCollection<T>` 和 `KeyedCollection<TKey,TItem>`。</span><span class="sxs-lookup"><span data-stu-id="a09ae-179">Use `Collection<T>`, `ReadOnlyCollection<T>`, and `KeyedCollection<TKey,TItem>` instead.</span></span>

### <a name="naming-custom-collections"></a><span data-ttu-id="a09ae-180">对自定义集合命名</span><span class="sxs-lookup"><span data-stu-id="a09ae-180">Naming Custom Collections</span></span>

 <span data-ttu-id="a09ae-181">创建集合（实现 `IEnumerable` 的类型）的原因主要有下面两种：(1) 为了创建这样一个新的数据结构，它具有结构特定的操作且性能特征通常与现有数据结构（例如 <xref:System.Collections.Generic.List%601>、<xref:System.Collections.Generic.LinkedList%601>、<xref:System.Collections.Generic.Stack%601>）不同；以及 (2) 为了创建一个专用于保存特定一组项目（例如 <xref:System.Collections.Specialized.StringCollection>）的集合。</span><span class="sxs-lookup"><span data-stu-id="a09ae-181">Collections (types that implement `IEnumerable`) are created mainly for two reasons: (1) to create a new data structure with structure-specific operations and often different performance characteristics than existing data structures (e.g.,  <xref:System.Collections.Generic.List%601>, <xref:System.Collections.Generic.LinkedList%601>, <xref:System.Collections.Generic.Stack%601>), and (2) to create a specialized collection for holding a specific set of items (e.g.,  <xref:System.Collections.Specialized.StringCollection>).</span></span> <span data-ttu-id="a09ae-182">数据结构最常用于应用程序和库的内部实现。</span><span class="sxs-lookup"><span data-stu-id="a09ae-182">Data structures are most often used in the internal implementation of applications and libraries.</span></span> <span data-ttu-id="a09ae-183">专用集合主要在 API 中（作为属性和参数类型）公开。</span><span class="sxs-lookup"><span data-stu-id="a09ae-183">Specialized collections are mainly to be exposed in APIs (as property and parameter types).</span></span>

 <span data-ttu-id="a09ae-184">✔️ 请在实现 `IDictionary` 或 `IDictionary<TKey,TValue>` 的抽象的名称中使用“Dictionary”后缀。</span><span class="sxs-lookup"><span data-stu-id="a09ae-184">✔️ DO use the "Dictionary" suffix in names of abstractions implementing `IDictionary` or `IDictionary<TKey,TValue>`.</span></span>

 <span data-ttu-id="a09ae-185">✔️ 请在实现 `IEnumerable`（或其任何后代）和表示项目列表的类型的名称中使用“Collection”后缀。</span><span class="sxs-lookup"><span data-stu-id="a09ae-185">✔️ DO use the "Collection" suffix in names of types implementing `IEnumerable` (or any of its descendants) and representing a list of items.</span></span>

 <span data-ttu-id="a09ae-186">✔️ 请为自定义数据结构使用适当的数据结构名称。</span><span class="sxs-lookup"><span data-stu-id="a09ae-186">✔️ DO use the appropriate data structure name for custom data structures.</span></span>

 <span data-ttu-id="a09ae-187">❌ 不要在集合抽象的名称中使用任何暗指特定实现的后缀，例如“LinkedList”或“Hashtable”。</span><span class="sxs-lookup"><span data-stu-id="a09ae-187">❌ AVOID using any suffixes implying particular implementation, such as "LinkedList" or "Hashtable," in names of collection abstractions.</span></span>

 <span data-ttu-id="a09ae-188">✔️ 请考虑对集合名称使用项目类型的名称作为前缀。</span><span class="sxs-lookup"><span data-stu-id="a09ae-188">✔️ CONSIDER prefixing collection names with the name of the item type.</span></span> <span data-ttu-id="a09ae-189">例如，存储类型为 `Address`（实现 `IEnumerable<Address>`）的项目的集合应被命名为 `AddressCollection`。</span><span class="sxs-lookup"><span data-stu-id="a09ae-189">For example, a collection storing items of type `Address` (implementing `IEnumerable<Address>`) should be named `AddressCollection`.</span></span> <span data-ttu-id="a09ae-190">如果项目类型为接口，则可省略项目类型的前缀“I”。</span><span class="sxs-lookup"><span data-stu-id="a09ae-190">If the item type is an interface, the "I" prefix of the item type can be omitted.</span></span> <span data-ttu-id="a09ae-191">因此，可将<xref:System.IDisposable> 项目的集合称为 `DisposableCollection`。</span><span class="sxs-lookup"><span data-stu-id="a09ae-191">Thus, a collection of <xref:System.IDisposable> items can be called `DisposableCollection`.</span></span>

 <span data-ttu-id="a09ae-192">✔️ 如果相应的可写集合可添加到框架中或者已存在于框架中，请考虑在只读集合的名称中使用“ReadOnly”前缀。</span><span class="sxs-lookup"><span data-stu-id="a09ae-192">✔️ CONSIDER using the "ReadOnly" prefix in names of read-only collections if a corresponding writeable collection might be added or already exists in the framework.</span></span>

 <span data-ttu-id="a09ae-193">例如，应将字符串的只读集合称为 `ReadOnlyStringCollection`。</span><span class="sxs-lookup"><span data-stu-id="a09ae-193">For example, a read-only collection of strings should be called `ReadOnlyStringCollection`.</span></span>

 <span data-ttu-id="a09ae-194">*Portions © 2005, 2009 Microsoft Corporation 版权所有。保留所有权利。*</span><span class="sxs-lookup"><span data-stu-id="a09ae-194">*Portions © 2005, 2009 Microsoft Corporation. All rights reserved.*</span></span>

 <span data-ttu-id="a09ae-195">*在 Pearson Education, Inc. 授权下，由 Addison-Wesley Professional 作为 Microsoft Windows 开发系列的一部分再版自 [Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619)（Framework 设计准则：可重用 .NET 库的约定、惯例和模式第 2 版），由 Krzysztof Cwalina 和 Brad Abrams 发布于 2008 年 10 月 22 日。*</span><span class="sxs-lookup"><span data-stu-id="a09ae-195">*Reprinted by permission of Pearson Education, Inc. from [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) by Krzysztof Cwalina and Brad Abrams, published Oct 22, 2008 by Addison-Wesley Professional as part of the Microsoft Windows Development Series.*</span></span>

## <a name="see-also"></a><span data-ttu-id="a09ae-196">请参阅</span><span class="sxs-lookup"><span data-stu-id="a09ae-196">See also</span></span>

- [<span data-ttu-id="a09ae-197">框架设计指南</span><span class="sxs-lookup"><span data-stu-id="a09ae-197">Framework Design Guidelines</span></span>](index.md)
- [<span data-ttu-id="a09ae-198">使用准则</span><span class="sxs-lookup"><span data-stu-id="a09ae-198">Usage Guidelines</span></span>](usage-guidelines.md)
