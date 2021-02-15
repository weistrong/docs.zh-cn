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
# <a name="property-design"></a>属性设计

虽然从技术上来说，属性与方法很相似，但它们在使用方案方面大不一样。 它们应被视作智能字段。 它们具有字段的调用语法，同时兼备方法的灵活性。

 ✔️ 如果调用方不能更改属性的值，则要创建 get-only 属性。

 请记住，如果属性属于可变引用类型，则即使属性是 get-only，也可更改属性值。

 ❌ 请勿提供 set-only 属性，也不要提供其 Setter 可访问性范围比 Getter 大的属性。

 例如，不要使用具有公共 Setter 和受保护的 Getter 的属性。

 如果无法提供属性 Getter，请改为以方法的形式实现功能。 请考虑将 `Set` 作为方法名称的开头，后跟你向属性赋予的名称。 例如，<xref:System.AppDomain> 有一个名为 `SetCachePath` 的方法，而不是有一个名为 `CachePath` 的 set-only 属性。

 ✔️ 请为所有属性提供敏感默认值，确保默认值不会导致安全漏洞或超级低效的代码。

 ✔️ 允许以任意顺序设置属性，即使这会导致对象的状态暂时无效也是如此。

 普遍的情况是两个或更多属性在一个点上相互关联；在这个点上，鉴于同一对象上其他属性的值，某一属性的某些值可能无效。 在这种情况下，因无效状态导致的异常应当延迟，直到相互关联的属性实际上由该对象一起使用为止。

 ✔️ 如果属性 Setter 引发异常，则要保留先前的值。

 ❌ 避免从属性 Getter 引发异常。

 属性 Getter 应为简单操作，不得具有任何前置条件。 如果 Getter 可能会引发异常，则它可能会被重新设计为方法。 请注意，此规则不适用于索引器；在索引器中，我们预计验证参数时会引发异常。

### <a name="indexed-property-design"></a>索引属性设计

 索引属性是一种特殊属性，它可具有参数，且可使用与数组索引类似的特殊语法进行调用。

 索引属性通常被称为索引器。 索引器应仅在提供对逻辑集合中项目的访问的 API 中使用。 例如，字符串是字符的集合，并且已添加了 <xref:System.String?displayProperty=nameWithType> 上的索引器来访问其字符。

 ✔️ 请考虑使用索引器来提供对内部数组中存储的数据的访问。

 ✔️ 请考虑对表示项目集合的类型提供索引器。

 ❌ 不要使用带有多个参数的索引属性。

 如果设计需要多个参数，请重新考虑属性是否真的表示逻辑集合的访问器。 如果不表示此内容，请改为使用方法。 请考虑以 `Get` 或 `Set` 作为方法名称的开头。

 ❌ 避免使用参数类型不是 <xref:System.Int32?displayProperty=nameWithType>、<xref:System.Int64?displayProperty=nameWithType>、<xref:System.String?displayProperty=nameWithType>、<xref:System.Object?displayProperty=nameWithType> 或枚举的索引器。

 如果设计需要其他类型的参数，强烈建议重新评估 API 是否真的表示逻辑集合的访问器。 如果不表示此内容，请使用方法。 请考虑以 `Get` 或 `Set` 作为方法名称的开头。

 ✔️ 请对索引属性使用名称 `Item`，除非有明显更好的名称（例如，参见 `System.String` 上的 <xref:System.String.Chars%2A> 属性）。

 在 C# 中，索引器的默认名称为 Item。 <xref:System.Runtime.CompilerServices.IndexerNameAttribute> 可用于自定义此名称。

 ❌ 请勿同时提供在语义上等效的索引器和方法。

 ❌ 请勿在一个类型中提供多个系列的重载索引器。

 这是由 C# 编译器实施的。

 ❌ 请勿使用非默认的索引属性。

 这是由 C# 编译器实施的。

### <a name="property-change-notification-events"></a>属性更改通知事件

 有时，提供事件来通知用户属性值出现更改很有用。 例如，`System.Windows.Forms.Control` 在其 `Text` 属性的值更改后会引发 `TextChanged` 事件。

 ✔️ 请考虑在高级 API（通常是设计器组件）中的属性值修改时引发更改通知事件。

 如果用户需要在某对象的某个属性出现更改时知道该情况，则该对象应对该属性引发更改通知事件。

 不过，对于基类型或基础集合等低级 API，引发此类事件的开销太大，不太值得这样做。 例如，当新项目添加到列表且 `Count` 属性更改时，<xref:System.Collections.Generic.List%601> 不会引发此类事件。

 ✔️ 请考虑当属性的值通过外部强制操作发生更改时引发更改通知事件。

 如果某属性值通过某个外部强制操作（通过在对象上调用方法之外的方式），则会引发事件，向开发人员指出该值正在更改且已经更改。 文本框控件的 `Text` 属性就是一个很好的例子。 当用户在 `TextBox` 中键入文本时，属性值会自动更改。

 *Portions © 2005, 2009 Microsoft Corporation 版权所有。保留所有权利。*

 *在 Pearson Education, Inc. 授权下，由 Addison-Wesley Professional 作为 Microsoft Windows 开发系列的一部分再版自 [Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619)（Framework 设计准则：可重用 .NET 库的约定、惯例和模式第 2 版），由 Krzysztof Cwalina 和 Brad Abrams 发布于 2008 年 10 月 22 日。*

## <a name="see-also"></a>请参阅

- [成员设计准则](member.md)
- [框架设计指南](index.md)
