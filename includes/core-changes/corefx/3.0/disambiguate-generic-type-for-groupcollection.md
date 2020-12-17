---
ms.openlocfilehash: 97fab784acac4331894547eea27fc21b485597fb
ms.sourcegitcommit: fcbe432482464b1639decad78cc4dc8387c6269e
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/12/2020
ms.locfileid: "97366879"
---
### <a name="passing-groupcollection-to-extension-methods-taking-ienumerablet-requires-disambiguation"></a><span data-ttu-id="b53a4-101">将 GroupCollection 传递到采用 IEnumerable\<T> 的扩展方法需要消除歧义</span><span class="sxs-lookup"><span data-stu-id="b53a4-101">Passing GroupCollection to extension methods taking IEnumerable\<T> requires disambiguation</span></span>

<span data-ttu-id="b53a4-102">调用在 <xref:System.Text.RegularExpressions.GroupCollection> 上采用 `IEnumerable<T>` 的扩展方法时，必须使用强制转换来消除该类型的歧义。</span><span class="sxs-lookup"><span data-stu-id="b53a4-102">When calling an extension method that takes an `IEnumerable<T>` on a <xref:System.Text.RegularExpressions.GroupCollection>, you must disambiguate the type using a cast.</span></span>

#### <a name="change-description"></a><span data-ttu-id="b53a4-103">更改说明</span><span class="sxs-lookup"><span data-stu-id="b53a4-103">Change description</span></span>

<span data-ttu-id="b53a4-104">从 .NET Core 3.0 开始，<xref:System.Text.RegularExpressions.GroupCollection?displayProperty=nameWithType> 除了实现 `IEnumerable<Group>` 等类型之外，还会实现 `IEnumerable<KeyValuePair<String,Group>>`。</span><span class="sxs-lookup"><span data-stu-id="b53a4-104">Starting in .NET Core 3.0, <xref:System.Text.RegularExpressions.GroupCollection?displayProperty=nameWithType> implements `IEnumerable<KeyValuePair<String,Group>>` in addition to the other types it implements, including `IEnumerable<Group>`.</span></span> <span data-ttu-id="b53a4-105">调用采用 <xref:System.Collections.Generic.IEnumerable%601> 的扩展方法时，这会导致歧义。</span><span class="sxs-lookup"><span data-stu-id="b53a4-105">This results in ambiguity when calling an extension method that takes an <xref:System.Collections.Generic.IEnumerable%601>.</span></span> <span data-ttu-id="b53a4-106">如果在 <xref:System.Text.RegularExpressions.GroupCollection> 实例上调用此类扩展方法，例如 <xref:System.Linq.Enumerable.Count%2A?displayProperty=nameWithType>，你将看到以下编译器错误：</span><span class="sxs-lookup"><span data-stu-id="b53a4-106">If you call such an extension method on a <xref:System.Text.RegularExpressions.GroupCollection> instance, for example, <xref:System.Linq.Enumerable.Count%2A?displayProperty=nameWithType>, you'll see the following compiler error:</span></span>

<span data-ttu-id="b53a4-107">CS1061：“GroupCollection”未包含“Count”的定义，并且找不到可接受第一个“GroupCollection”类型参数的可访问扩展方法“Count”（是否缺少 using 指令或程序集引用？）</span><span class="sxs-lookup"><span data-stu-id="b53a4-107">**CS1061: 'GroupCollection' does not contain a definition for 'Count' and no accessible extension method 'Count' accepting a first argument of type 'GroupCollection' could be found (are you missing a using directive or an assembly reference?)**</span></span>

<span data-ttu-id="b53a4-108">在早期版本的 .NET 中，没有歧义，也没有编译器错误。</span><span class="sxs-lookup"><span data-stu-id="b53a4-108">In previous versions of .NET, there was no ambiguity and no compiler error.</span></span>

#### <a name="version-introduced"></a><span data-ttu-id="b53a4-109">引入的版本</span><span class="sxs-lookup"><span data-stu-id="b53a4-109">Version introduced</span></span>

<span data-ttu-id="b53a4-110">3.0</span><span class="sxs-lookup"><span data-stu-id="b53a4-110">3.0</span></span>

#### <a name="reason-for-change"></a><span data-ttu-id="b53a4-111">更改原因</span><span class="sxs-lookup"><span data-stu-id="b53a4-111">Reason for change</span></span>

<span data-ttu-id="b53a4-112">这是[意外的中断性变更](https://github.com/dotnet/corefx/pull/30077)。</span><span class="sxs-lookup"><span data-stu-id="b53a4-112">This was an [unintentional breaking change](https://github.com/dotnet/corefx/pull/30077).</span></span> <span data-ttu-id="b53a4-113">由于此更改已经有一段时间了，所以我们不打算将其还原。</span><span class="sxs-lookup"><span data-stu-id="b53a4-113">Because it has been like this for some time, we don't plan to revert it.</span></span> <span data-ttu-id="b53a4-114">此外，此类更改本身就会造成中断。</span><span class="sxs-lookup"><span data-stu-id="b53a4-114">In addition, such a change would itself be breaking.</span></span>

#### <a name="recommended-action"></a><span data-ttu-id="b53a4-115">建议操作</span><span class="sxs-lookup"><span data-stu-id="b53a4-115">Recommended action</span></span>

<span data-ttu-id="b53a4-116">对于 <xref:System.Text.RegularExpressions.GroupCollection> 实例，使用强制转换对接受 `IEnumerable<T>` 的扩展方法的调用消除歧义。</span><span class="sxs-lookup"><span data-stu-id="b53a4-116">For <xref:System.Text.RegularExpressions.GroupCollection> instances, disambiguate calls to extension methods that accept an `IEnumerable<T>` with a cast.</span></span>

```csharp
// Without a cast - causes CS1061.
match.Groups.Count(_ => true)

// With a disambiguating cast.
((IEnumerable<Group>)m.Groups).Count(_ => true);
```

#### <a name="category"></a><span data-ttu-id="b53a4-117">类别</span><span class="sxs-lookup"><span data-stu-id="b53a4-117">Category</span></span>

<span data-ttu-id="b53a4-118">Core .NET 库</span><span class="sxs-lookup"><span data-stu-id="b53a4-118">Core .NET libraries</span></span>

#### <a name="affected-apis"></a><span data-ttu-id="b53a4-119">受影响的 API</span><span class="sxs-lookup"><span data-stu-id="b53a4-119">Affected APIs</span></span>

<span data-ttu-id="b53a4-120">任何接受 <xref:System.Collections.Generic.IEnumerable%601> 的扩展方法都会受到影响。</span><span class="sxs-lookup"><span data-stu-id="b53a4-120">Any extension method that accepts an <xref:System.Collections.Generic.IEnumerable%601> is affected.</span></span> <span data-ttu-id="b53a4-121">例如：</span><span class="sxs-lookup"><span data-stu-id="b53a4-121">For example:</span></span>

- <xref:System.Collections.Immutable.ImmutableArray.ToImmutableArray%60%601(System.Collections.Generic.IEnumerable{%60%600})?displayProperty=fullName>
- <xref:System.Collections.Immutable.ImmutableDictionary.ToImmutableDictionary%2A?displayProperty=fullName>
- <xref:System.Collections.Immutable.ImmutableHashSet.ToImmutableHashSet%2A?displayProperty=fullName>
- <xref:System.Collections.Immutable.ImmutableList.ToImmutableList%60%601(System.Collections.Generic.IEnumerable{%60%600})?displayProperty=fullName>
- <xref:System.Collections.Immutable.ImmutableSortedDictionary.ToImmutableSortedDictionary%2A?displayProperty=fullName>
- <xref:System.Collections.Immutable.ImmutableSortedSet.ToImmutableSortedSet%2A?displayProperty=fullName>
- <xref:System.Data.DataTableExtensions.CopyToDataTable%2A?displayProperty=fullName>
- <span data-ttu-id="b53a4-122">大多数 `System.Linq.Enumerable` 方法，例如 <xref:System.Linq.Enumerable.Count%2A?displayProperty=fullName></span><span class="sxs-lookup"><span data-stu-id="b53a4-122">Most of the `System.Linq.Enumerable` methods, for example, <xref:System.Linq.Enumerable.Count%2A?displayProperty=fullName></span></span>
- <xref:System.Linq.ParallelEnumerable.AsParallel%2A?displayProperty=fullName>
- <xref:System.Linq.Queryable.AsQueryable%2A?displayProperty=fullName>

<!--

#### Affected APIs

- ``M:System.Collections.Immutable.ImmutableArray.ToImmutableArray``1(System.Collections.Generic.IEnumerable{``0})``
- `Overload:System.Collections.Immutable.ImmutableDictionary.ToImmutableDictionary`
- `Overload:System.Collections.Immutable.ImmutableHashSet.ToImmutableHashSet`
- ``M:System.Collections.Immutable.ImmutableList.ToImmutableList``1(System.Collections.Generic.IEnumerable{``0})``
- `Overload:System.Collections.Immutable.ImmutableSortedDictionary.ToImmutableSortedDictionary`
- `Overload:System.Collections.Immutable.ImmutableSortedSet.ToImmutableSortedSet`
- `Overload:System.Data.DataTableExtensions.CopyToDataTable`
- `Overload:System.Linq.Enumerable.Count`
- `Overload:System.Linq.ParallelEnumerable.AsParallel`
- `Overload:System.Linq.Queryable.AsQueryable`

-->
