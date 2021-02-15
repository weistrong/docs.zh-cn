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
# <a name="guidelines-for-collections"></a>集合准则

专为操作一组具有某些共同特性的对象而设计的类型都可被视为一个集合。 这种类型几乎总是适合实现 <xref:System.Collections.IEnumerable> 或 <xref:System.Collections.Generic.IEnumerable%601>，因此在本部分中，我们仅将实现其中一个或全部两个接口的类型视为集合。

 ❌ 请勿在公共 API 中使用弱类型集合。

 表示集合项目的所有返回值和参数的类型都应该是确切的项目类型，而不是其任何基类型（这仅适用于集合的公共成员）。

 ❌ 请勿在公共 API 中使用 <xref:System.Collections.ArrayList> 和 <xref:System.Collections.Generic.List%601>。

 这些类型是数据结构，根据设计可用于内部实现，不可用于公共 API。 `List<T>` 针对性能和功能进行了优化，代价是灵活性和 API 的简洁度。 例如，如果你返回 `List<T>`，则你将永远无法在客户端代码修改集合时收到通知。 此外，`List<T>` 会公开很多成员（例如 <xref:System.Collections.Generic.List%601.BinarySearch%2A>），它们在很多方案中没有用或不适用。 以下两部分描述了为在公共 API 中使用而专门设计的类型（抽象）。

 ❌ 请勿在公共 API 中使用 `Hashtable` 和 `Dictionary<TKey,TValue>`。

 这些类型是数据结构，根据设计可用于内部实现。 公共 API 应使用 <xref:System.Collections.IDictionary>、`IDictionary <TKey, TValue>`，或者使用实现其中一个或全部两个接口的自定义类型。

 ❌ 请勿使用 <xref:System.Collections.Generic.IEnumerator%601> 和 <xref:System.Collections.IEnumerator>，也不要使用其他实现上述任一接口的类型，作为 `GetEnumerator` 方法的返回类型的除外。

 从 `GetEnumerator` 之外的方法返回枚举器的类型不可与 `foreach` 语句一起使用。

 ❌ 请勿在同一类型上同时实现 `IEnumerator<T>` 和 `IEnumerable<T>`。 这同样适用于非泛型接口 `IEnumerator` 和 `IEnumerable`。

## <a name="collection-parameters"></a>集合参数

 ✔️ 请尽量使用专业化程度最小的类型作为参数类型。 将集合作为参数的大多数成员使用的是 `IEnumerable<T>` 接口。

 ❌ 如果仅是为了访问 `Count` 属性，请避免使用 <xref:System.Collections.Generic.ICollection%601> 和 <xref:System.Collections.ICollection>。

 转而请考虑使用 `IEnumerable<T>` 或 `IEnumerable`，并动态检查对象是否实现 `ICollection<T>` 或 `ICollection`。

## <a name="collection-properties-and-return-values"></a>集合属性和返回值

 ❌ 请勿提供可设置的集合属性。

 用户可先清除集合，然后添加新内容来替换集合的内容。 如果常见的情况是替换整个集合，则请考虑对集合提供 `AddRange` 方法。

 ✔️ 请对表示读取/写入集合的属性或返回值使用 `Collection<T>` 或 `Collection<T>` 的子类。

 如果 `Collection<T>` 不满足某些要求（例如集合不得实现 <xref:System.Collections.IList>），请通过实现 `IEnumerable<T>`、`ICollection<T>` 或 <xref:System.Collections.Generic.IList%601> 来使用自定义集合。

 ✔️ 请对表示只读集合的属性或返回值使用 `ReadOnlyCollection<T>` 的子类或 <xref:System.Collections.ObjectModel.ReadOnlyCollection%601>，在极少的情况下请使用 `IEnumerable<T>`。

 通常，请优先选择 `ReadOnlyCollection<T>`。 如果它不满足某些要求（例如集合不得实现 `IList`），请通过实现 `IEnumerable<T>`、`ICollection<T>` 或 `IList<T>` 来使用自定义集合。 如果要实现自定义只读集合，请实现 `ICollection<T>.IsReadOnly` 来返回 `true`。

 如果你确定你只想支持的方案是仅向前迭代，那么使用 `IEnumerable<T>` 即可。

 ✔️ 请考虑使用泛型基础集合的子类，而不是直接使用集合。

 这样可进行更好的命名，还可添加基础集合类型上不存在的帮助程序成员。 这尤其适用于高级 API。

 ✔️ 请考虑从超级常用的方法和属性返回 `Collection<T>` 或 `ReadOnlyCollection<T>` 的子类。

 这样，你就能在将来添加帮助程序方法或更改集合实现。

 ✔️ 如果集合中存储的项目具有唯一键（名称、ID 等），请考虑使用键控集合。 键控集合可同时由整数和键编制索引，它们通常通过从 `KeyedCollection<TKey,TItem>` 继承来实现。

 键控集合通常会占用更大的内存，如果内存开销的权重比拥有键的优点高，那么不得使用这类集合。

 ❌ 请勿从集合属性返回 NULL 值，也不要从返回集合的方法中返回 NULL 值。 转而请返回空集合或空数组。

 一般规则是应将 NULL 集合和空（0 项目）集合/数组视为相同。

### <a name="snapshots-versus-live-collections"></a>快照与活动集合

 表示某时间点的某状态的集合被称为快照集合。 例如，包含从数据库查询返回的行的集合是一个快照。 始终表示当前状态的集合被称为活动集合。 例如，`ComboBox` 项目的集合是一个活动集合。

 ❌ 请勿从属性返回快照集合。 属性应返回活动集合。

 属性 Getter 应该是非常轻量的操作。 要返回快照，需要在 O(n) 操作中创建内部集合的副本。

 ✔️ 请使用快照集合或活动 `IEnumerable<T>`（或其子类型）表示可变的集合（“可变”是指可在不显式修改集合的情况下进行更改）。

 通常，表示共享资源（例如目录中的文件）的所有集合都是可变的。 这种集合很难或不可能作为活动集合实现，除非实现只是一个仅前进枚举器。

## <a name="choosing-between-arrays-and-collections"></a>在数组和集合之间进行选择

 ✔️ 相对于数组，请优选集合。

 集合可让你更大程度地控制内容，它们随时间的推移而变化，而且更易于使用。 此外，不建议对只读方案使用数组，原因是克隆数组的成本过高。 可用性调查显示，某些开发人员感觉更喜欢使用基于集合的 API。

 不过，如果你要开发低级 API，则对读写方案使用数组可能效果更好。 数组的内存占用更小，这有助于减少工作集，而且由于数组已由运行时进行优化，因此可更快地访问数组中的元素。

 ✔️ 请考虑在低级 API 中使用数组来尽量减少内存耗用和尽量提高性能。

 ✔️ 请使用字节数组而不是字节集合。

 ❌ 如果每次调用属性 Getter 时，属性都必须返回新数组（例如内部数组的副本），那么请勿对属性使用数组。

## <a name="implementing-custom-collections"></a>实现自定义集合

 ✔️ 设计新集合时，请考虑从 `Collection<T>`、`ReadOnlyCollection<T>` 或 `KeyedCollection<TKey,TItem>` 中继承。

 ✔️ 设计新集合时，请实现 `IEnumerable<T>`。 请考虑实现 `ICollection<T>`或者甚至实现 `IList<T>`（如果合理的话）。

 实现此类自定义集合时，请尽可能严格遵守由 `Collection<T>` 和 `ReadOnlyCollection<T>` 建立的 API 模式。 也就是说，显式实现相同的成员，对如同这两个集合一样的参数进行命名等等。

 ✔️ 如果集合通常会传递到将非泛型集合接口（`IList` 和 `ICollection`）视为输入的 API，那么请考虑实现这些接口。

 ❌ 对于具有与集合概念无关的复杂 API 的类型，请避免实现集合接口。

 ❌ 请勿从非泛型基础集合（例如 `CollectionBase`）进行继承。 请改为使用 `Collection<T>`、`ReadOnlyCollection<T>` 和 `KeyedCollection<TKey,TItem>`。

### <a name="naming-custom-collections"></a>对自定义集合命名

 创建集合（实现 `IEnumerable` 的类型）的原因主要有下面两种：(1) 为了创建这样一个新的数据结构，它具有结构特定的操作且性能特征通常与现有数据结构（例如 <xref:System.Collections.Generic.List%601>、<xref:System.Collections.Generic.LinkedList%601>、<xref:System.Collections.Generic.Stack%601>）不同；以及 (2) 为了创建一个专用于保存特定一组项目（例如 <xref:System.Collections.Specialized.StringCollection>）的集合。 数据结构最常用于应用程序和库的内部实现。 专用集合主要在 API 中（作为属性和参数类型）公开。

 ✔️ 请在实现 `IDictionary` 或 `IDictionary<TKey,TValue>` 的抽象的名称中使用“Dictionary”后缀。

 ✔️ 请在实现 `IEnumerable`（或其任何后代）和表示项目列表的类型的名称中使用“Collection”后缀。

 ✔️ 请为自定义数据结构使用适当的数据结构名称。

 ❌ 不要在集合抽象的名称中使用任何暗指特定实现的后缀，例如“LinkedList”或“Hashtable”。

 ✔️ 请考虑对集合名称使用项目类型的名称作为前缀。 例如，存储类型为 `Address`（实现 `IEnumerable<Address>`）的项目的集合应被命名为 `AddressCollection`。 如果项目类型为接口，则可省略项目类型的前缀“I”。 因此，可将<xref:System.IDisposable> 项目的集合称为 `DisposableCollection`。

 ✔️ 如果相应的可写集合可添加到框架中或者已存在于框架中，请考虑在只读集合的名称中使用“ReadOnly”前缀。

 例如，应将字符串的只读集合称为 `ReadOnlyStringCollection`。

 *Portions © 2005, 2009 Microsoft Corporation 版权所有。保留所有权利。*

 *在 Pearson Education, Inc. 授权下，由 Addison-Wesley Professional 作为 Microsoft Windows 开发系列的一部分再版自 [Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619)（Framework 设计准则：可重用 .NET 库的约定、惯例和模式第 2 版），由 Krzysztof Cwalina 和 Brad Abrams 发布于 2008 年 10 月 22 日。*

## <a name="see-also"></a>请参阅

- [框架设计指南](index.md)
- [使用准则](usage-guidelines.md)
