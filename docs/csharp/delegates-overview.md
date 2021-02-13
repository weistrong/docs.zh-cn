---
title: 委托简介
description: 本概述文章介绍委托的基本概念，并讨论委托的语言设计目标。
ms.date: 02/02/2021
ms.technology: csharp-fundamentals
ms.assetid: 59b61d77-84e5-457b-8da5-fb5f24ca6ed6
ms.openlocfilehash: 72086301a6dd0552ab25baf732978802ad62669b
ms.sourcegitcommit: 4df8e005c074ceb1f978f007b222fe253be2baf3
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/04/2021
ms.locfileid: "99548339"
---
# <a name="introduction-to-delegates"></a><span data-ttu-id="40210-103">委托简介</span><span class="sxs-lookup"><span data-stu-id="40210-103">Introduction to Delegates</span></span>

<span data-ttu-id="40210-104">在 .NET 中委托提供 *后期绑定* 机制。</span><span class="sxs-lookup"><span data-stu-id="40210-104">Delegates provide a *late binding* mechanism in .NET.</span></span> <span data-ttu-id="40210-105">后期绑定意味着调用方在你所创建的算法中至少提供一个方法来实现算法的一部分。</span><span class="sxs-lookup"><span data-stu-id="40210-105">Late Binding means that you create an algorithm where the caller also supplies at least one method that implements part of the algorithm.</span></span>

<span data-ttu-id="40210-106">例如，在天文应用程序中对恒星列表进行排序。</span><span class="sxs-lookup"><span data-stu-id="40210-106">For example, consider sorting a list of stars in an astronomy application.</span></span>
<span data-ttu-id="40210-107">你可以选择按照恒星与地球的距离、恒星的大小或者可以感知的亮度来对它们进行排序。</span><span class="sxs-lookup"><span data-stu-id="40210-107">You may choose to sort those stars by their distance from the earth, or the magnitude of the star, or their perceived brightness.</span></span>

<span data-ttu-id="40210-108">在所有这些情况下，Sort() 方法本质上执行的是同一操作：基于某种比较方法对列表中的项目进行排序。</span><span class="sxs-lookup"><span data-stu-id="40210-108">In all those cases, the Sort() method does essentially the same thing: arranges the items in the list based on some comparison.</span></span> <span data-ttu-id="40210-109">对于每个排序顺序，比较两种恒星的代码是不同的。</span><span class="sxs-lookup"><span data-stu-id="40210-109">The code that compares two stars is different for each of the sort orderings.</span></span>

<span data-ttu-id="40210-110">这些类型的解决方案已在软件中使用了半个世纪。</span><span class="sxs-lookup"><span data-stu-id="40210-110">These kinds of solutions have been used in software for half a century.</span></span>
<span data-ttu-id="40210-111">C# 语言的委托概念提供一流的语言支持和以此概念为中心的类型安全性。</span><span class="sxs-lookup"><span data-stu-id="40210-111">The C# language delegate concept provides first class language support, and type safety around the concept.</span></span>

<span data-ttu-id="40210-112">正如你稍后将在此系列文章中看到的，为与此类似的算法编写的 C# 代码是类型安全的，它使用语言规则和编译器来确保类型与参数匹配，并返回类型。</span><span class="sxs-lookup"><span data-stu-id="40210-112">As you'll see later in this series, the C# code you write for algorithms like this is type safe, and uses the language rules and the compiler to ensure that the types match for arguments and return types.</span></span>

<span data-ttu-id="40210-113">对于类似的方案，已将[函数指针](~/_csharplang/proposals/csharp-9.0/function-pointers.md)添加到 C# 9，其中你需要对调用约定有更多的控制。</span><span class="sxs-lookup"><span data-stu-id="40210-113">[Function pointers](~/_csharplang/proposals/csharp-9.0/function-pointers.md) were added to C# 9 for similar scenarios, where you need more control over the calling convention.</span></span> <span data-ttu-id="40210-114">使用添加到委托类型的虚方法调用与委托关联的代码。</span><span class="sxs-lookup"><span data-stu-id="40210-114">The code associated with a delegate is invoked using a virtual method added to a delegate type.</span></span> <span data-ttu-id="40210-115">使用函数指针，可以指定不同的约定。</span><span class="sxs-lookup"><span data-stu-id="40210-115">Using function pointers, you can specify different conventions.</span></span>

## <a name="language-design-goals-for-delegates"></a><span data-ttu-id="40210-116">委托的语言设计目标</span><span class="sxs-lookup"><span data-stu-id="40210-116">Language Design Goals for Delegates</span></span>

<span data-ttu-id="40210-117">语言设计人员针对最终成为委托的功能列举了一些目标。</span><span class="sxs-lookup"><span data-stu-id="40210-117">The language designers enumerated several goals for the feature that eventually became delegates.</span></span>

<span data-ttu-id="40210-118">团队想要拥有可用于任何后期绑定算法的公共语言构造。</span><span class="sxs-lookup"><span data-stu-id="40210-118">The team wanted a common language construct that could be used for any late binding algorithms.</span></span> <span data-ttu-id="40210-119">委托促使开发人员学习一个概念，并在许多不同的软件问题中使用这同一概念。</span><span class="sxs-lookup"><span data-stu-id="40210-119">Delegates enable developers to learn one concept, and use that same concept across many different software problems.</span></span>

<span data-ttu-id="40210-120">其次，该团队希望支持单一和多播方法调用。</span><span class="sxs-lookup"><span data-stu-id="40210-120">Second, the team wanted to support both single and multicast method calls.</span></span> <span data-ttu-id="40210-121">（多播委托是将多个方法调用链接在一起的委托。</span><span class="sxs-lookup"><span data-stu-id="40210-121">(Multicast delegates are delegates that chain together multiple method calls.</span></span>
<span data-ttu-id="40210-122">你将[在本系列文章的后面部分](delegate-class.md)看到示例。）</span><span class="sxs-lookup"><span data-stu-id="40210-122">You'll see examples [later in this series](delegate-class.md).)</span></span>

<span data-ttu-id="40210-123">团队想要委托在所有 C# 构造中支持开发人员所预期的相同的类型安全性。</span><span class="sxs-lookup"><span data-stu-id="40210-123">The team wanted delegates to support the same type safety that developers expect from all C# constructs.</span></span>

<span data-ttu-id="40210-124">最后，团队认识到事件模式是一个特定模式，委托或任何后期绑定算法在这种模式下都非常有用。</span><span class="sxs-lookup"><span data-stu-id="40210-124">Finally, the team recognized an event pattern is one specific pattern where delegates, or any late binding algorithm, is very useful.</span></span> <span data-ttu-id="40210-125">团队需要确保委托的代码可以为 .NET 事件模式提供基础。</span><span class="sxs-lookup"><span data-stu-id="40210-125">The team wanted to ensure the code for delegates could provide the basis for the .NET event pattern.</span></span>

<span data-ttu-id="40210-126">所有这些工作的结果是 C# 和 .NET 中的委托和事件支持。</span><span class="sxs-lookup"><span data-stu-id="40210-126">The result of all that work was the delegate and event support in C# and .NET.</span></span> <span data-ttu-id="40210-127">本文剩余部分将介绍语言功能、库支持和使用委托时使用的通用语法结构。</span><span class="sxs-lookup"><span data-stu-id="40210-127">The remaining articles in this section will cover language features, library support, and common idioms used when you work with delegates.</span></span>

<span data-ttu-id="40210-128">你将了解 `delegate` 关键字和它所生成的代码。</span><span class="sxs-lookup"><span data-stu-id="40210-128">You'll learn about the `delegate` keyword and what code it generates.</span></span> <span data-ttu-id="40210-129">你将了解 `System.Delegate` 类中的功能，以及如何使用这些功能。</span><span class="sxs-lookup"><span data-stu-id="40210-129">You'll learn about the features in the `System.Delegate` class, and how those features are used.</span></span> <span data-ttu-id="40210-130">你将了解如何创建类型安全的委托，以及如何创建可以通过委托调用的方法。</span><span class="sxs-lookup"><span data-stu-id="40210-130">You'll learn how to create type safe delegates, and how to create methods that can be invoked through delegates.</span></span> <span data-ttu-id="40210-131">你还将了解如何使用 Lambda 表达式来处理委托和事件。</span><span class="sxs-lookup"><span data-stu-id="40210-131">You'll also learn how to work with delegates and events by using Lambda expressions.</span></span> <span data-ttu-id="40210-132">你将看到作为 LINQ 的构建基块的委托的用途。</span><span class="sxs-lookup"><span data-stu-id="40210-132">You'll see where delegates become one of the building blocks for LINQ.</span></span> <span data-ttu-id="40210-133">你将了解委托如何成为 .NET 事件模式的基础，以及委托和事件之间的区别。</span><span class="sxs-lookup"><span data-stu-id="40210-133">You'll learn how delegates are the basis for the .NET event pattern, and how they're different.</span></span>

<span data-ttu-id="40210-134">让我们开始吧。</span><span class="sxs-lookup"><span data-stu-id="40210-134">Let's get started.</span></span>

[<span data-ttu-id="40210-135">下一页</span><span class="sxs-lookup"><span data-stu-id="40210-135">Next</span></span>](delegate-class.md)
