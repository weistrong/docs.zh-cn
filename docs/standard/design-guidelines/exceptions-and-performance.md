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
# <a name="exceptions-and-performance"></a><span data-ttu-id="dd236-103">异常和性能</span><span class="sxs-lookup"><span data-stu-id="dd236-103">Exceptions and Performance</span></span>

<span data-ttu-id="dd236-104">与异常相关的一个常见问题是，如果异常用于经常失败的代码，则实现的性能是不可接受的。</span><span class="sxs-lookup"><span data-stu-id="dd236-104">One common concern related to exceptions is that if exceptions are used for code that routinely fails, the performance of the implementation will be unacceptable.</span></span> <span data-ttu-id="dd236-105">这是一个合理的担忧。</span><span class="sxs-lookup"><span data-stu-id="dd236-105">This is a valid concern.</span></span> <span data-ttu-id="dd236-106">当一个成员引发一个异常时，其性能可能会慢几个数量级。</span><span class="sxs-lookup"><span data-stu-id="dd236-106">When a member throws an exception, its performance can be orders of magnitude slower.</span></span> <span data-ttu-id="dd236-107">但是，在严格遵守不允许使用错误代码的异常准则的同时，也有可能获得良好的性能。</span><span class="sxs-lookup"><span data-stu-id="dd236-107">However, it is possible to achieve good performance while strictly adhering to the exception guidelines that disallow using error codes.</span></span> <span data-ttu-id="dd236-108">本部分中所述的两种模式提供了执行此操作的方法。</span><span class="sxs-lookup"><span data-stu-id="dd236-108">Two patterns described in this section suggest ways to do this.</span></span>

 <span data-ttu-id="dd236-109">❌ 因为担心异常可能会对性能产生负面影响，因此请勿使用错误代码。</span><span class="sxs-lookup"><span data-stu-id="dd236-109">❌ DO NOT use error codes because of concerns that exceptions might affect performance negatively.</span></span>

 <span data-ttu-id="dd236-110">若要提高性能，可以使用接下来的两个部分中所述的“测试者-执行者”模式或“尝试-分析”模式。</span><span class="sxs-lookup"><span data-stu-id="dd236-110">To improve performance, it is possible to use either the Tester-Doer Pattern or the Try-Parse Pattern, described in the next two sections.</span></span>

## <a name="tester-doer-pattern"></a><span data-ttu-id="dd236-111">“测试者-执行者”模式</span><span class="sxs-lookup"><span data-stu-id="dd236-111">Tester-Doer Pattern</span></span>

 <span data-ttu-id="dd236-112">有时，异常引发成员的性能可以通过将该成员分成两部分来提高。</span><span class="sxs-lookup"><span data-stu-id="dd236-112">Sometimes performance of an exception-throwing member can be improved by breaking the member into two.</span></span> <span data-ttu-id="dd236-113">让我们看看 <xref:System.Collections.Generic.ICollection%601> 接口的 <xref:System.Collections.Generic.ICollection%601.Add%2A> 方法。</span><span class="sxs-lookup"><span data-stu-id="dd236-113">Let’s look at the <xref:System.Collections.Generic.ICollection%601.Add%2A> method of the <xref:System.Collections.Generic.ICollection%601> interface.</span></span>

```csharp
ICollection<int> numbers = ...
numbers.Add(1);
```

 <span data-ttu-id="dd236-114">如果集合是只读的，则 `Add` 方法引发。</span><span class="sxs-lookup"><span data-stu-id="dd236-114">The method `Add` throws if the collection is read-only.</span></span> <span data-ttu-id="dd236-115">在方法调用预计会经常失败的情况下，这可能是一个性能问题。</span><span class="sxs-lookup"><span data-stu-id="dd236-115">This can be a performance problem in scenarios where the method call is expected to fail often.</span></span> <span data-ttu-id="dd236-116">缓解此问题的一种方法是在尝试添加值之前测试集合是否可写。</span><span class="sxs-lookup"><span data-stu-id="dd236-116">One of the ways to mitigate the problem is to test whether the collection is writable before trying to add a value.</span></span>

```csharp
ICollection<int> numbers = ...
...
if (!numbers.IsReadOnly)
{
    numbers.Add(1);
}
```

 <span data-ttu-id="dd236-117">用于测试条件的成员（在本示例中为 `IsReadOnly` 属性）被称为测试者。</span><span class="sxs-lookup"><span data-stu-id="dd236-117">The member used to test a condition, which in our example is the property `IsReadOnly`, is referred to as the tester.</span></span> <span data-ttu-id="dd236-118">用于执行潜在引发操作的成员（在本示例中为 `Add` 方法）被称为执行者。</span><span class="sxs-lookup"><span data-stu-id="dd236-118">The member used to perform a potentially throwing operation, the `Add` method in our example, is referred to as the doer.</span></span>

 <span data-ttu-id="dd236-119">✔️ 请考虑对可能在常见场景中引发异常的成员使用“测试者-执行者”模式，以避免与异常相关的性能问题。</span><span class="sxs-lookup"><span data-stu-id="dd236-119">✔️ CONSIDER the Tester-Doer Pattern for members that might throw exceptions in common scenarios to avoid performance problems related to exceptions.</span></span>

## <a name="try-parse-pattern"></a><span data-ttu-id="dd236-120">“尝试-分析”模式</span><span class="sxs-lookup"><span data-stu-id="dd236-120">Try-Parse Pattern</span></span>

 <span data-ttu-id="dd236-121">对于对性能极其敏感的 API，应使用比前一部分中所述的“测试者-执行者”模式更快的模式。</span><span class="sxs-lookup"><span data-stu-id="dd236-121">For extremely performance-sensitive APIs, an even faster pattern than the Tester-Doer Pattern described in the previous section should be used.</span></span> <span data-ttu-id="dd236-122">该模式要求调整成员名称，使定义完善的测试用例成为成员语义的一部分。</span><span class="sxs-lookup"><span data-stu-id="dd236-122">The pattern calls for adjusting the member name to make a well-defined test case a part of the member semantics.</span></span> <span data-ttu-id="dd236-123">例如，<xref:System.DateTime> 定义一个 <xref:System.DateTime.Parse%2A> 方法，当字符串的分析失败时，该方法将引发异常。</span><span class="sxs-lookup"><span data-stu-id="dd236-123">For example, <xref:System.DateTime> defines a <xref:System.DateTime.Parse%2A> method that throws an exception if parsing of a string fails.</span></span> <span data-ttu-id="dd236-124">它还定义一个相应的 <xref:System.DateTime.TryParse%2A> 方法，该方法尝试进行分析，但如果分析不成功，则返回 false，而如果分析成功，则使用 `out` 参数返回分析结果。</span><span class="sxs-lookup"><span data-stu-id="dd236-124">It also defines a corresponding <xref:System.DateTime.TryParse%2A> method that attempts to parse, but returns false if parsing is unsuccessful and returns the result of a successful parsing using an `out` parameter.</span></span>

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

 <span data-ttu-id="dd236-125">使用此模式时，务必严格地定义“尝试”功能。</span><span class="sxs-lookup"><span data-stu-id="dd236-125">When using this pattern, it is important to define the try functionality in strict terms.</span></span> <span data-ttu-id="dd236-126">如果成员由于定义完善的“尝试”功能以外的任何原因失败，该成员仍必须引发相应的异常。</span><span class="sxs-lookup"><span data-stu-id="dd236-126">If the member fails for any reason other than the well-defined try, the member must still throw a corresponding exception.</span></span>

 <span data-ttu-id="dd236-127">✔️ 请考虑对可能在常见场景中引发异常的成员使用“尝试-分析”模式，以避免与异常相关的性能问题。</span><span class="sxs-lookup"><span data-stu-id="dd236-127">✔️ CONSIDER the Try-Parse Pattern for members that might throw exceptions in common scenarios to avoid performance problems related to exceptions.</span></span>

 <span data-ttu-id="dd236-128">✔️ 对于实现此模式的方法，请务必使用前缀“Try”和布尔返回类型。</span><span class="sxs-lookup"><span data-stu-id="dd236-128">✔️ DO use the prefix "Try" and Boolean return type for methods implementing this pattern.</span></span>

 <span data-ttu-id="dd236-129">✔️ 请务必使用“尝试-分析”模式为每个成员提供一个异常引发成员。</span><span class="sxs-lookup"><span data-stu-id="dd236-129">✔️ DO provide an exception-throwing member for each member using the Try-Parse Pattern.</span></span>

 <span data-ttu-id="dd236-130">*Portions © 2005, 2009 Microsoft Corporation 版权所有。保留所有权利。*</span><span class="sxs-lookup"><span data-stu-id="dd236-130">*Portions © 2005, 2009 Microsoft Corporation. All rights reserved.*</span></span>

 <span data-ttu-id="dd236-131">在 Pearson Education, Inc. 授权下，由 Addison-Wesley Professional 作为 Microsoft Windows 开发系列的一部分再版自 [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619)（Framework 设计准则：可重用 .NET 库的约定、惯例和模式第 2 版），由 Krzysztof Cwalina 和 Brad Abrams 发布于 2008 年 10 月 22 日。</span><span class="sxs-lookup"><span data-stu-id="dd236-131">*Reprinted by permission of Pearson Education, Inc. from [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) by Krzysztof Cwalina and Brad Abrams, published Oct 22, 2008 by Addison-Wesley Professional as part of the Microsoft Windows Development Series.*</span></span>

## <a name="see-also"></a><span data-ttu-id="dd236-132">请参阅</span><span class="sxs-lookup"><span data-stu-id="dd236-132">See also</span></span>

- [<span data-ttu-id="dd236-133">框架设计指南</span><span class="sxs-lookup"><span data-stu-id="dd236-133">Framework Design Guidelines</span></span>](index.md)
- [<span data-ttu-id="dd236-134">异常设计准则</span><span class="sxs-lookup"><span data-stu-id="dd236-134">Design Guidelines for Exceptions</span></span>](exceptions.md)
