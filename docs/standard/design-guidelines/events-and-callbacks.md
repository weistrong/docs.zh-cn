---
description: 详细了解：事件和回调
title: 事件和回调
ms.date: 10/22/2008
helpviewer_keywords:
- events [.NET Framework], extensibility
- methods [.NET Framework], callback
- callback methods
- callbacks
ms.assetid: 48b55c60-495f-4089-9396-97f9122bba7c
ms.openlocfilehash: 8a9049808ec0f7a490889ab1f17c4d8b8e8bd2b3
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99642144"
---
# <a name="events-and-callbacks"></a><span data-ttu-id="f22c7-103">事件和回调</span><span class="sxs-lookup"><span data-stu-id="f22c7-103">Events and Callbacks</span></span>

<span data-ttu-id="f22c7-104">回调是允许框架通过委托回调到用户代码的扩展点。</span><span class="sxs-lookup"><span data-stu-id="f22c7-104">Callbacks are extensibility points that allow a framework to call back into user code through a delegate.</span></span> <span data-ttu-id="f22c7-105">通常通过方法的参数将这些委托传递到框架。</span><span class="sxs-lookup"><span data-stu-id="f22c7-105">These delegates are usually passed to the framework through a parameter of a method.</span></span>

 <span data-ttu-id="f22c7-106">事件是回调的一种特例，它支持便捷且一致的语法，用于提供委托（事件处理程序）。</span><span class="sxs-lookup"><span data-stu-id="f22c7-106">Events are a special case of callbacks that supports convenient and consistent syntax for supplying the delegate (an event handler).</span></span> <span data-ttu-id="f22c7-107">此外，Visual Studio 的语句完成和设计器还提供了有关使用基于事件的 API 的帮助。</span><span class="sxs-lookup"><span data-stu-id="f22c7-107">In addition, Visual Studio's statement completion and designers provide help in using event-based APIs.</span></span> <span data-ttu-id="f22c7-108">（请参阅[事件设计](event.md)。）</span><span class="sxs-lookup"><span data-stu-id="f22c7-108">(See [Event Design](event.md).)</span></span>

 <span data-ttu-id="f22c7-109">✔️ 请考虑使用回调以允许用户提供要由框架执行的自定义代码。</span><span class="sxs-lookup"><span data-stu-id="f22c7-109">✔️ CONSIDER using callbacks to allow users to provide custom code to be executed by the framework.</span></span>

 <span data-ttu-id="f22c7-110">✔️ 请考虑使用事件以允许用户自定义框架的行为，而无需理解面向对象的设计。</span><span class="sxs-lookup"><span data-stu-id="f22c7-110">✔️ CONSIDER using events to allow users to customize the behavior of a framework without the need for understanding object-oriented design.</span></span>

 <span data-ttu-id="f22c7-111">✔️ 请务必首选使用事件而非普通回调，因为它们对于更广泛的开发人员来说更熟悉，并且与 Visual Studio 语句完成进行了集成。</span><span class="sxs-lookup"><span data-stu-id="f22c7-111">✔️ DO prefer events over plain callbacks, because they are more familiar to a broader range of developers and are integrated with Visual Studio statement completion.</span></span>

 <span data-ttu-id="f22c7-112">❌ 请避免在对性能敏感的 API 中使用回调。</span><span class="sxs-lookup"><span data-stu-id="f22c7-112">❌ AVOID using callbacks in performance-sensitive APIs.</span></span>

 <span data-ttu-id="f22c7-113">✔️ 在使用回调定义 API 时，请务必使用新的 `Func<...>`、`Action<...>` 或 `Expression<...>` 类型，而不是自定义委托。</span><span class="sxs-lookup"><span data-stu-id="f22c7-113">✔️ DO use the new `Func<...>`, `Action<...>`, or `Expression<...>` types instead of custom delegates, when defining APIs with callbacks.</span></span>

 <span data-ttu-id="f22c7-114">`Func<...>` 和 `Action<...>` 表示泛型委托。</span><span class="sxs-lookup"><span data-stu-id="f22c7-114">`Func<...>` and `Action<...>` represent generic delegates.</span></span> <span data-ttu-id="f22c7-115">`Expression<...>` 表示函数定义，这些定义可进行编译并随后在运行时进行调用，但也可进行序列化并传递到远程进程。</span><span class="sxs-lookup"><span data-stu-id="f22c7-115">`Expression<...>` represents function definitions that can be compiled and subsequently invoked at runtime but can also be serialized and passed to remote processes.</span></span>

 <span data-ttu-id="f22c7-116">✔️ 请务必衡量并了解使用 `Expression<...>`（而不是使用 `Func<...>` 和 `Action<...>` 委托）对性能的影响。</span><span class="sxs-lookup"><span data-stu-id="f22c7-116">✔️ DO measure and understand performance implications of using `Expression<...>`, instead of using `Func<...>` and `Action<...>` delegates.</span></span>

 <span data-ttu-id="f22c7-117">`Expression<...>` 类型在大多数情况下在逻辑上等同于 `Func<...>` 和 `Action<...>` 委托。</span><span class="sxs-lookup"><span data-stu-id="f22c7-117">`Expression<...>` types are in most cases logically equivalent to `Func<...>` and `Action<...>` delegates.</span></span> <span data-ttu-id="f22c7-118">它们之间的主要区别在于委托旨在用于本地流程场景，而表达式适用于在远程进程或计算机中对该表达式求值是有益的且可能的情况。</span><span class="sxs-lookup"><span data-stu-id="f22c7-118">The main difference between them is that the delegates are intended to be used in local process scenarios; expressions are intended for cases where it's beneficial and possible to evaluate the expression in a remote process or machine.</span></span>

 <span data-ttu-id="f22c7-119">✔️ 请务必要明白，调用委托即表示你将执行任意代码，而这可能会对安全性、正确性和兼容性产生影响。</span><span class="sxs-lookup"><span data-stu-id="f22c7-119">✔️ DO understand that by calling a delegate, you are executing arbitrary code and that could have security, correctness, and compatibility repercussions.</span></span>

 <span data-ttu-id="f22c7-120">*Portions &copy; 2005, 2009 Microsoft Corporation。保留所有权利。*</span><span class="sxs-lookup"><span data-stu-id="f22c7-120">*Portions &copy; 2005, 2009 Microsoft Corporation. All rights reserved.*</span></span>

 <span data-ttu-id="f22c7-121">在 Pearson Education, Inc. 授权下，由 Addison-Wesley Professional 作为 Microsoft Windows 开发系列的一部分再版自 [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619)（Framework 设计准则：可重用 .NET 库的约定、惯例和模式第 2 版），由 Krzysztof Cwalina 和 Brad Abrams 发布于 2008 年 10 月 22 日。</span><span class="sxs-lookup"><span data-stu-id="f22c7-121">*Reprinted by permission of Pearson Education, Inc. from [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) by Krzysztof Cwalina and Brad Abrams, published Oct 22, 2008 by Addison-Wesley Professional as part of the Microsoft Windows Development Series.*</span></span>

## <a name="see-also"></a><span data-ttu-id="f22c7-122">请参阅</span><span class="sxs-lookup"><span data-stu-id="f22c7-122">See also</span></span>

- [<span data-ttu-id="f22c7-123">扩展性设计</span><span class="sxs-lookup"><span data-stu-id="f22c7-123">Designing for Extensibility</span></span>](designing-for-extensibility.md)
- [<span data-ttu-id="f22c7-124">框架设计指南</span><span class="sxs-lookup"><span data-stu-id="f22c7-124">Framework Design Guidelines</span></span>](index.md)
