---
description: 详细了解：抽象（抽象类型和接口）
title: 抽象（抽象类型和接口）
ms.date: 10/22/2008
helpviewer_keywords:
- interfaces [.NET Framework], abstract
- abstract interfaces [.NET Framework]
- abstract types [.NET Framework]
- types [.NET Framework], abstract
ms.assetid: 0a632bc7-9b03-44ee-8842-c82f88672a45
ms.openlocfilehash: 8dc82f004d655429e842c63fab4defff0fd74ab2
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99642432"
---
# <a name="abstractions-abstract-types-and-interfaces"></a><span data-ttu-id="9ce02-103">抽象（抽象类型和接口）</span><span class="sxs-lookup"><span data-stu-id="9ce02-103">Abstractions (Abstract Types and Interfaces)</span></span>

<span data-ttu-id="9ce02-104">抽象是一种描述协定但不提供协定的完整实现的类型。</span><span class="sxs-lookup"><span data-stu-id="9ce02-104">An abstraction is a type that describes a contract but does not provide a full implementation of the contract.</span></span> <span data-ttu-id="9ce02-105">抽象通常作为抽象类或接口实现，并且它们附带一组定义明确的引用文档，其中描述了实现协定的类型所需的语义。</span><span class="sxs-lookup"><span data-stu-id="9ce02-105">Abstractions are usually implemented as abstract classes or interfaces, and they come with a well-defined set of reference documentation describing the required semantics of the types implementing the contract.</span></span> <span data-ttu-id="9ce02-106">.NET Framework 中的一些最重要的抽象包括 <xref:System.IO.Stream>、<xref:System.Collections.Generic.IEnumerable%601> 和 <xref:System.Object>。</span><span class="sxs-lookup"><span data-stu-id="9ce02-106">Some of the most important abstractions in the .NET Framework include <xref:System.IO.Stream>, <xref:System.Collections.Generic.IEnumerable%601>, and <xref:System.Object>.</span></span>

 <span data-ttu-id="9ce02-107">你可实现支持抽象协定的具体类型并将此具体类型与使用该抽象的（针对该抽象操作的）框架 API 结合使用，从而扩展框架。</span><span class="sxs-lookup"><span data-stu-id="9ce02-107">You can extend frameworks by implementing a concrete type that supports the contract of an abstraction and using this concrete type with framework APIs consuming (operating on) the abstraction.</span></span>

 <span data-ttu-id="9ce02-108">很难设计一种能够经受时间考验、有意义且有用的抽象。</span><span class="sxs-lookup"><span data-stu-id="9ce02-108">A meaningful and useful abstraction that is able to withstand the test of time is very difficult to design.</span></span> <span data-ttu-id="9ce02-109">主要难点是获得正确的成员集，不能多也不能少。</span><span class="sxs-lookup"><span data-stu-id="9ce02-109">The main difficulty is getting the right set of members, no more and no fewer.</span></span> <span data-ttu-id="9ce02-110">如果一个抽象有太多的成员，它就会变得难以（甚至不可能）实现。</span><span class="sxs-lookup"><span data-stu-id="9ce02-110">If an abstraction has too many members, it becomes difficult or even impossible to implement.</span></span> <span data-ttu-id="9ce02-111">如果它的成员对于承诺的功能而言太少，则在许多令人感兴趣的场景中，它就变得毫无用处。</span><span class="sxs-lookup"><span data-stu-id="9ce02-111">If it has too few members for the promised functionality, it becomes useless in many interesting scenarios.</span></span>

 <span data-ttu-id="9ce02-112">框架中的抽象太多也会对框架的可用性产生负面影响。</span><span class="sxs-lookup"><span data-stu-id="9ce02-112">Too many abstractions in a framework also negatively affect usability of the framework.</span></span> <span data-ttu-id="9ce02-113">如果不理解抽象如何融入具体实现及针对该抽象操作的 API 的大环境，通常就很难理解该抽象。</span><span class="sxs-lookup"><span data-stu-id="9ce02-113">It is often quite difficult to understand an abstraction without understanding how it fits into the larger picture of the concrete implementations and the APIs operating on the abstraction.</span></span> <span data-ttu-id="9ce02-114">此外，抽象及其成员的名称都必然是抽象的，在没有首先理解它们更广泛的使用上下文的情况下，这通常使得它们难以理解、令人捉摸不透。</span><span class="sxs-lookup"><span data-stu-id="9ce02-114">Also, names of abstractions and their members are necessarily abstract, which often makes them cryptic and unapproachable without first understanding the broader context of their usage.</span></span>

 <span data-ttu-id="9ce02-115">不过，抽象提供极其强大的扩展性，这是其他扩展性机制所不能比拟的。</span><span class="sxs-lookup"><span data-stu-id="9ce02-115">However, abstractions provide extremely powerful extensibility that the other extensibility mechanisms cannot often match.</span></span> <span data-ttu-id="9ce02-116">它们是插件、控制反转 (IoC)、管道等多个体系结构模式的核心。</span><span class="sxs-lookup"><span data-stu-id="9ce02-116">They are at the core of many architectural patterns, such as plug-ins, inversion of control (IoC), pipelines, and so on.</span></span> <span data-ttu-id="9ce02-117">它们对于框架的可测试性也极其重要。</span><span class="sxs-lookup"><span data-stu-id="9ce02-117">They are also extremely important for testability of frameworks.</span></span> <span data-ttu-id="9ce02-118">良好的抽象使你可以出于单元测试的目的，剔除大量的依赖项。</span><span class="sxs-lookup"><span data-stu-id="9ce02-118">Good abstractions make it possible to stub out heavy dependencies for the purpose of unit testing.</span></span> <span data-ttu-id="9ce02-119">总之，抽象是面向对象的新式框架所追求的丰富性的原因。</span><span class="sxs-lookup"><span data-stu-id="9ce02-119">In summary, abstractions are responsible for the sought-after richness of the modern object-oriented frameworks.</span></span>

 <span data-ttu-id="9ce02-120">❌ 请勿提供抽象，除非通过开发一些具体实现及使用该抽象的 API 对它们进行了测试。</span><span class="sxs-lookup"><span data-stu-id="9ce02-120">❌ DO NOT provide abstractions unless they are tested by developing several concrete implementations and APIs consuming the abstractions.</span></span>

 <span data-ttu-id="9ce02-121">✔️ 设计抽象时，请务必要在抽象类和接口之间进行仔细地选择。</span><span class="sxs-lookup"><span data-stu-id="9ce02-121">✔️ DO choose carefully between an abstract class and an interface when designing an abstraction.</span></span>

 <span data-ttu-id="9ce02-122">✔️ 考虑为抽象的具体实现提供引用测试。</span><span class="sxs-lookup"><span data-stu-id="9ce02-122">✔️ CONSIDER providing reference tests for concrete implementations of abstractions.</span></span> <span data-ttu-id="9ce02-123">此类测试应该允许用户测试其实现是否正确实现了协定。</span><span class="sxs-lookup"><span data-stu-id="9ce02-123">Such tests should allow users to test whether their implementations correctly implement the contract.</span></span>

 <span data-ttu-id="9ce02-124">*Portions © 2005, 2009 Microsoft Corporation 版权所有。保留所有权利。*</span><span class="sxs-lookup"><span data-stu-id="9ce02-124">*Portions © 2005, 2009 Microsoft Corporation. All rights reserved.*</span></span>

 <span data-ttu-id="9ce02-125">在 Pearson Education, Inc. 授权下，由 Addison-Wesley Professional 作为 Microsoft Windows 开发系列的一部分再版自 [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619)（Framework 设计准则：可重用 .NET 库的约定、惯例和模式第 2 版），由 Krzysztof Cwalina 和 Brad Abrams 发布于 2008 年 10 月 22 日。</span><span class="sxs-lookup"><span data-stu-id="9ce02-125">*Reprinted by permission of Pearson Education, Inc. from [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) by Krzysztof Cwalina and Brad Abrams, published Oct 22, 2008 by Addison-Wesley Professional as part of the Microsoft Windows Development Series.*</span></span>

## <a name="see-also"></a><span data-ttu-id="9ce02-126">请参阅</span><span class="sxs-lookup"><span data-stu-id="9ce02-126">See also</span></span>

- [<span data-ttu-id="9ce02-127">框架设计指南</span><span class="sxs-lookup"><span data-stu-id="9ce02-127">Framework Design Guidelines</span></span>](index.md)
- [<span data-ttu-id="9ce02-128">扩展性设计</span><span class="sxs-lookup"><span data-stu-id="9ce02-128">Designing for Extensibility</span></span>](designing-for-extensibility.md)
