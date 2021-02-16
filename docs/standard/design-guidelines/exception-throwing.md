---
description: 详细了解：异常引发
title: 异常引发
ms.date: 10/22/2008
helpviewer_keywords:
- exceptions, throwing
- explicitly throwing exceptions
- throwing exceptions, design guidelines
ms.assetid: 5388e02b-52f5-460e-a2b5-eeafe60eeebe
ms.openlocfilehash: b1cf7a4eecc32a9f76ea06c47dd6c16d3afe5470
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99642131"
---
# <a name="exception-throwing"></a><span data-ttu-id="d5813-103">异常引发</span><span class="sxs-lookup"><span data-stu-id="d5813-103">Exception Throwing</span></span>

<span data-ttu-id="d5813-104">本部分中所述的异常引发准则要求对执行失败的含义有一个很好的定义。</span><span class="sxs-lookup"><span data-stu-id="d5813-104">Exception-throwing guidelines described in this section require a good definition of the meaning of execution failure.</span></span> <span data-ttu-id="d5813-105">每当一个成员无法执行它旨在要执行的操作（成员名称所指的操作）时，执行失败就会发生。</span><span class="sxs-lookup"><span data-stu-id="d5813-105">Execution failure occurs whenever a member cannot do what it was designed to do (what the member name implies).</span></span> <span data-ttu-id="d5813-106">例如，如果 `OpenFile` 方法不能将打开的文件句柄返回给调用方，这将被视为执行失败。</span><span class="sxs-lookup"><span data-stu-id="d5813-106">For example, if the `OpenFile` method cannot return an opened file handle to the caller, it would be considered an execution failure.</span></span>

 <span data-ttu-id="d5813-107">大多数开发人员已经习惯将异常用于使用错误（例如被零除或空引用）。</span><span class="sxs-lookup"><span data-stu-id="d5813-107">Most developers have become comfortable with using exceptions for usage errors such as division by zero or null references.</span></span> <span data-ttu-id="d5813-108">在框架中，异常用于所有错误情况，包括执行错误。</span><span class="sxs-lookup"><span data-stu-id="d5813-108">In the Framework, exceptions are used for all error conditions, including execution errors.</span></span>

 <span data-ttu-id="d5813-109">❌ 请勿返回错误代码。</span><span class="sxs-lookup"><span data-stu-id="d5813-109">❌ DO NOT return error codes.</span></span>

 <span data-ttu-id="d5813-110">异常是在框架中报告错误的主要方法。</span><span class="sxs-lookup"><span data-stu-id="d5813-110">Exceptions are the primary means of reporting errors in frameworks.</span></span>

 <span data-ttu-id="d5813-111">✔️ 请务必通过引发异常来报告执行失败。</span><span class="sxs-lookup"><span data-stu-id="d5813-111">✔️ DO report execution failures by throwing exceptions.</span></span>

 <span data-ttu-id="d5813-112">✔️ 在代码遇到无法安全地进行进一步执行的情况时，请考虑通过调用 `System.Environment.FailFast`（.NET Framework 2.0 功能）来终止进程，而不是引发一个异常。</span><span class="sxs-lookup"><span data-stu-id="d5813-112">✔️ CONSIDER terminating the process by calling `System.Environment.FailFast` (.NET Framework 2.0 feature) instead of throwing an exception if your code encounters a situation where it is unsafe for further execution.</span></span>

 <span data-ttu-id="d5813-113">❌ 如果可能，请勿对正常控制流使用异常。</span><span class="sxs-lookup"><span data-stu-id="d5813-113">❌ DO NOT use exceptions for the normal flow of control, if possible.</span></span>

 <span data-ttu-id="d5813-114">除了可能出现争用条件的系统故障和操作之外，框架设计者还应设计 API，使用户能够编写不引发异常的代码。</span><span class="sxs-lookup"><span data-stu-id="d5813-114">Except for system failures and operations with potential race conditions, framework designers should design APIs so users can write code that does not throw exceptions.</span></span> <span data-ttu-id="d5813-115">例如，你可提供一种在调用成员之前检查前置条件的方法，使用户可以编写不引发异常的代码。</span><span class="sxs-lookup"><span data-stu-id="d5813-115">For example, you can provide a way to check preconditions before calling a member so users can write code that does not throw exceptions.</span></span>

 <span data-ttu-id="d5813-116">用于检查另一个成员的前置条件的成员通常称为测试者，而实际执行该工作的成员称为执行者。</span><span class="sxs-lookup"><span data-stu-id="d5813-116">The member used to check preconditions of another member is often referred to as a tester, and the member that actually does the work is called a doer.</span></span>

 <span data-ttu-id="d5813-117">在某些情况下，“测试者-执行者”模式可能会产生不可接受的性能开销。</span><span class="sxs-lookup"><span data-stu-id="d5813-117">There are cases when the Tester-Doer Pattern can have an unacceptable performance overhead.</span></span> <span data-ttu-id="d5813-118">在此类情况下，应考虑使用所谓的“尝试-分析”模式（有关详细信息，请参阅[异常和性能](exceptions-and-performance.md)）。</span><span class="sxs-lookup"><span data-stu-id="d5813-118">In such cases, the so-called Try-Parse Pattern should be considered (see [Exceptions and Performance](exceptions-and-performance.md) for more information).</span></span>

 <span data-ttu-id="d5813-119">✔️ 请考虑引发异常对性能的影响。</span><span class="sxs-lookup"><span data-stu-id="d5813-119">✔️ CONSIDER the performance implications of throwing exceptions.</span></span> <span data-ttu-id="d5813-120">每秒 100 次以上的引发率可能会显著影响大多数应用程序的性能。</span><span class="sxs-lookup"><span data-stu-id="d5813-120">Throw rates above 100 per second are likely to noticeably impact the performance of most applications.</span></span>

 <span data-ttu-id="d5813-121">✔️ 请务必记录所有由可公开调用的成员因违反成员协定（而不是系统故障）而引发的异常，并将它们视为你协定的一部分。</span><span class="sxs-lookup"><span data-stu-id="d5813-121">✔️ DO document all exceptions thrown by publicly callable members because of a violation of the member contract (rather than a system failure) and treat them as part of your contract.</span></span>

 <span data-ttu-id="d5813-122">作为协定一部分的异常不应从一个版本更改为下一个版本（即不应更改异常类型，也不应添加新异常）。</span><span class="sxs-lookup"><span data-stu-id="d5813-122">Exceptions that are a part of the contract should not change from one version to the next (i.e., exception type should not change, and new exceptions should not be added).</span></span>

 <span data-ttu-id="d5813-123">❌ 请勿包含可基于某些选项引发或不引发的公共成员。</span><span class="sxs-lookup"><span data-stu-id="d5813-123">❌ DO NOT have public members that can either throw or not based on some option.</span></span>

 <span data-ttu-id="d5813-124">❌ 请勿包含将异常作为返回值或 `out` 参数返回的公共成员。</span><span class="sxs-lookup"><span data-stu-id="d5813-124">❌ DO NOT have public members that return exceptions as the return value or an `out` parameter.</span></span>

 <span data-ttu-id="d5813-125">从公共 API 返回异常，而不是引发异常，这会使基于异常的错误报告的许多好处无法实现。</span><span class="sxs-lookup"><span data-stu-id="d5813-125">Returning exceptions from public APIs instead of throwing them defeats many of the benefits of exception-based error reporting.</span></span>

 <span data-ttu-id="d5813-126">✔️ 请考虑使用异常生成器方法。</span><span class="sxs-lookup"><span data-stu-id="d5813-126">✔️ CONSIDER using exception builder methods.</span></span>

 <span data-ttu-id="d5813-127">从不同的位置引发相同的异常是很常见的情况。</span><span class="sxs-lookup"><span data-stu-id="d5813-127">It is common to throw the same exception from different places.</span></span> <span data-ttu-id="d5813-128">若要避免代码膨胀，请使用创建异常并初始化其属性的帮助程序方法。</span><span class="sxs-lookup"><span data-stu-id="d5813-128">To avoid code bloat, use helper methods that create exceptions and initialize their properties.</span></span>

 <span data-ttu-id="d5813-129">此外，引发异常的成员不会被内联。</span><span class="sxs-lookup"><span data-stu-id="d5813-129">Also, members that throw exceptions are not getting inlined.</span></span> <span data-ttu-id="d5813-130">将 throw 语句移动到生成器中可能会允许该成员内联。</span><span class="sxs-lookup"><span data-stu-id="d5813-130">Moving the throw statement inside the builder might allow the member to be inlined.</span></span>

 <span data-ttu-id="d5813-131">❌ 请勿从异常筛选器块中引发异常。</span><span class="sxs-lookup"><span data-stu-id="d5813-131">❌ DO NOT throw exceptions from exception filter blocks.</span></span>

 <span data-ttu-id="d5813-132">当异常筛选器引发一个异常时，CLR 将捕获该异常，并且筛选器将返回 false。</span><span class="sxs-lookup"><span data-stu-id="d5813-132">When an exception filter raises an exception, the exception is caught by the CLR, and the filter returns false.</span></span> <span data-ttu-id="d5813-133">此行为与筛选器显式执行并返回 false 是无法区分的，因此很难进行调试。</span><span class="sxs-lookup"><span data-stu-id="d5813-133">This behavior is indistinguishable from the filter executing and returning false explicitly and is therefore very difficult to debug.</span></span>

 <span data-ttu-id="d5813-134">❌ 请避免从 finally 块显式引发异常。</span><span class="sxs-lookup"><span data-stu-id="d5813-134">❌ AVOID explicitly throwing exceptions from finally blocks.</span></span> <span data-ttu-id="d5813-135">由于调用引发的方法而隐式引发的异常是可以接受的。</span><span class="sxs-lookup"><span data-stu-id="d5813-135">Implicitly thrown exceptions resulting from calling methods that throw are acceptable.</span></span>

 <span data-ttu-id="d5813-136">*Portions © 2005, 2009 Microsoft Corporation 版权所有。保留所有权利。*</span><span class="sxs-lookup"><span data-stu-id="d5813-136">*Portions © 2005, 2009 Microsoft Corporation. All rights reserved.*</span></span>

 <span data-ttu-id="d5813-137">在 Pearson Education, Inc. 授权下，由 Addison-Wesley Professional 作为 Microsoft Windows 开发系列的一部分再版自 [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619)（Framework 设计准则：可重用 .NET 库的约定、惯例和模式第 2 版），由 Krzysztof Cwalina 和 Brad Abrams 发布于 2008 年 10 月 22 日。</span><span class="sxs-lookup"><span data-stu-id="d5813-137">*Reprinted by permission of Pearson Education, Inc. from [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) by Krzysztof Cwalina and Brad Abrams, published Oct 22, 2008 by Addison-Wesley Professional as part of the Microsoft Windows Development Series.*</span></span>

## <a name="see-also"></a><span data-ttu-id="d5813-138">请参阅</span><span class="sxs-lookup"><span data-stu-id="d5813-138">See also</span></span>

- [<span data-ttu-id="d5813-139">框架设计指南</span><span class="sxs-lookup"><span data-stu-id="d5813-139">Framework Design Guidelines</span></span>](index.md)
- [<span data-ttu-id="d5813-140">异常设计准则</span><span class="sxs-lookup"><span data-stu-id="d5813-140">Design Guidelines for Exceptions</span></span>](exceptions.md)
