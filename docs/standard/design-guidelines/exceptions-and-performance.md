---
description: 详细了解：异常和性能
title: 异常和性能
ms.date: 10/22/2008
helpviewer_keywords:
- tester-doer pattern
- TryParse pattern
- exceptions, throwing
- exceptions, performance
- throwing exceptions, performance
ms.assetid: 3ad6aad9-08e6-4232-b336-0e301f2493e6
ms.openlocfilehash: 72b35ccca5514e56dcc04fc0a07d1f9887c4a2f7
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99642118"
---
# <a name="exceptions-and-performance"></a>异常和性能

与异常相关的一个常见问题是，如果异常用于经常失败的代码，则实现的性能是不可接受的。 这是一个合理的担忧。 当一个成员引发一个异常时，其性能可能会慢几个数量级。 但是，在严格遵守不允许使用错误代码的异常准则的同时，也有可能获得良好的性能。 本部分中所述的两种模式提供了执行此操作的方法。

 ❌ 因为担心异常可能会对性能产生负面影响，因此请勿使用错误代码。

 若要提高性能，可以使用接下来的两个部分中所述的“测试者-执行者”模式或“尝试-分析”模式。

## <a name="tester-doer-pattern"></a>“测试者-执行者”模式

 有时，异常引发成员的性能可以通过将该成员分成两部分来提高。 让我们看看 <xref:System.Collections.Generic.ICollection%601> 接口的 <xref:System.Collections.Generic.ICollection%601.Add%2A> 方法。

```csharp
ICollection<int> numbers = ...
numbers.Add(1);
```

 如果集合是只读的，则 `Add` 方法引发。 在方法调用预计会经常失败的情况下，这可能是一个性能问题。 缓解此问题的一种方法是在尝试添加值之前测试集合是否可写。

```csharp
ICollection<int> numbers = ...
...
if (!numbers.IsReadOnly)
{
    numbers.Add(1);
}
```

 用于测试条件的成员（在本示例中为 `IsReadOnly` 属性）被称为测试者。 用于执行潜在引发操作的成员（在本示例中为 `Add` 方法）被称为执行者。

 ✔️ 请考虑对可能在常见场景中引发异常的成员使用“测试者-执行者”模式，以避免与异常相关的性能问题。

## <a name="try-parse-pattern"></a>“尝试-分析”模式

 对于对性能极其敏感的 API，应使用比前一部分中所述的“测试者-执行者”模式更快的模式。 该模式要求调整成员名称，使定义完善的测试用例成为成员语义的一部分。 例如，<xref:System.DateTime> 定义一个 <xref:System.DateTime.Parse%2A> 方法，当字符串的分析失败时，该方法将引发异常。 它还定义一个相应的 <xref:System.DateTime.TryParse%2A> 方法，该方法尝试进行分析，但如果分析不成功，则返回 false，而如果分析成功，则使用 `out` 参数返回分析结果。

```csharp
public struct DateTime
{
    public static DateTime Parse(string dateTime)
    {
        ...
    }
    public static bool TryParse(string dateTime, out DateTime result)
    {
        ...
    }
}
```

 使用此模式时，务必严格地定义“尝试”功能。 如果成员由于定义完善的“尝试”功能以外的任何原因失败，该成员仍必须引发相应的异常。

 ✔️ 请考虑对可能在常见场景中引发异常的成员使用“尝试-分析”模式，以避免与异常相关的性能问题。

 ✔️ 对于实现此模式的方法，请务必使用前缀“Try”和布尔返回类型。

 ✔️ 请务必使用“尝试-分析”模式为每个成员提供一个异常引发成员。

 *Portions © 2005, 2009 Microsoft Corporation 版权所有。保留所有权利。*

 在 Pearson Education, Inc. 授权下，由 Addison-Wesley Professional 作为 Microsoft Windows 开发系列的一部分再版自 [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619)（Framework 设计准则：可重用 .NET 库的约定、惯例和模式第 2 版），由 Krzysztof Cwalina 和 Brad Abrams 发布于 2008 年 10 月 22 日。

## <a name="see-also"></a>请参阅

- [框架设计指南](index.md)
- [异常设计准则](exceptions.md)
