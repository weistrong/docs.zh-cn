---
title: 委托 - C# 编程指南
description: C# 中的委托是一种类型，它引用具有参数列表和返回类型的方法。 委托用于将方法作为参数传递给其他方法。
ms.date: 02/02/2021
helpviewer_keywords:
- C# language, delegates
- delegates [C#]
ms.assetid: 97de039b-c76b-4b9c-a27d-8c1e1c8d93da
ms.openlocfilehash: 86f7908501c075881786d16caffdd765b8aaf6b5
ms.sourcegitcommit: 4df8e005c074ceb1f978f007b222fe253be2baf3
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/04/2021
ms.locfileid: "99548066"
---
# <a name="delegates-c-programming-guide"></a><span data-ttu-id="dc659-104">委托（C# 编程指南）</span><span class="sxs-lookup"><span data-stu-id="dc659-104">Delegates (C# Programming Guide)</span></span>

<span data-ttu-id="dc659-105">[委托](../../language-reference/builtin-types/reference-types.md)是一种引用类型，表示对具有特定参数列表和返回类型的方法的引用。</span><span class="sxs-lookup"><span data-stu-id="dc659-105">A [delegate](../../language-reference/builtin-types/reference-types.md) is a type that represents references to methods with a particular parameter list and return type.</span></span> <span data-ttu-id="dc659-106">在实例化委托时，你可以将其实例与任何具有兼容签名和返回类型的方法相关联。</span><span class="sxs-lookup"><span data-stu-id="dc659-106">When you instantiate a delegate, you can associate its instance with any method with a compatible signature and return type.</span></span> <span data-ttu-id="dc659-107">你可以通过委托实例调用方法。</span><span class="sxs-lookup"><span data-stu-id="dc659-107">You can invoke (or call) the method through the delegate instance.</span></span>

<span data-ttu-id="dc659-108">委托用于将方法作为参数传递给其他方法。</span><span class="sxs-lookup"><span data-stu-id="dc659-108">Delegates are used to pass methods as arguments to other methods.</span></span> <span data-ttu-id="dc659-109">事件处理程序就是通过委托调用的方法。</span><span class="sxs-lookup"><span data-stu-id="dc659-109">Event handlers are nothing more than methods that are invoked through delegates.</span></span> <span data-ttu-id="dc659-110">你可以创建一个自定义方法，当发生特定事件时，某个类（如 Windows 控件）就可以调用你的方法。</span><span class="sxs-lookup"><span data-stu-id="dc659-110">You create a custom method, and a class such as a windows control can call your method when a certain event occurs.</span></span> <span data-ttu-id="dc659-111">下面的示例演示了一个委托声明：</span><span class="sxs-lookup"><span data-stu-id="dc659-111">The following example shows a delegate declaration:</span></span>

[!code-csharp[csProgGuideDelegates#20](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csProgGuideDelegates/CS/Delegates.cs#20)]

<span data-ttu-id="dc659-112">可将任何可访问类或结构中与委托类型匹配的任何方法分配给委托。</span><span class="sxs-lookup"><span data-stu-id="dc659-112">Any method from any accessible class or struct that matches the delegate type can be assigned to the delegate.</span></span> <span data-ttu-id="dc659-113">该方法可以是静态方法，也可以是实例方法。</span><span class="sxs-lookup"><span data-stu-id="dc659-113">The method can be either static or an instance method.</span></span> <span data-ttu-id="dc659-114">此灵活性意味着你可以通过编程方式来更改方法调用，还可以向现有类中插入新代码。</span><span class="sxs-lookup"><span data-stu-id="dc659-114">This flexibility means you can programmatically change method calls, or plug new code into existing classes.</span></span>

> [!NOTE]
> <span data-ttu-id="dc659-115">在方法重载的上下文中，方法的签名不包括返回值。</span><span class="sxs-lookup"><span data-stu-id="dc659-115">In the context of method overloading, the signature of a method does not include the return value.</span></span> <span data-ttu-id="dc659-116">但在委托的上下文中，签名包括返回值。</span><span class="sxs-lookup"><span data-stu-id="dc659-116">But in the context of delegates, the signature does include the return value.</span></span> <span data-ttu-id="dc659-117">换句话说，方法和委托必须具有相同的返回类型。</span><span class="sxs-lookup"><span data-stu-id="dc659-117">In other words, a method must have the same return type as the delegate.</span></span>

<span data-ttu-id="dc659-118">将方法作为参数进行引用的能力使委托成为定义回调方法的理想选择。</span><span class="sxs-lookup"><span data-stu-id="dc659-118">This ability to refer to a method as a parameter makes delegates ideal for defining callback methods.</span></span> <span data-ttu-id="dc659-119">可编写一个比较应用程序中两个对象的方法。</span><span class="sxs-lookup"><span data-stu-id="dc659-119">You can write a method that compares two objects in your application.</span></span> <span data-ttu-id="dc659-120">该方法可用在排序算法的委托中。</span><span class="sxs-lookup"><span data-stu-id="dc659-120">That method can be used in a delegate for a sort algoritym.</span></span> <span data-ttu-id="dc659-121">由于比较代码与库分离，因此排序方法可能更常见。</span><span class="sxs-lookup"><span data-stu-id="dc659-121">Because the comparison code is separate from the library, the sort method can be more general.</span></span>

<span data-ttu-id="dc659-122">对于类似的方案，已将[函数指针](~/_csharplang/proposals/csharp-9.0/function-pointers.md)添加到 C# 9，其中你需要对调用约定有更多的控制。</span><span class="sxs-lookup"><span data-stu-id="dc659-122">[Function pointers](~/_csharplang/proposals/csharp-9.0/function-pointers.md) were added to C# 9 for similar scenarios, where you need more control over the calling convention.</span></span> <span data-ttu-id="dc659-123">使用添加到委托类型的虚方法调用与委托关联的代码。</span><span class="sxs-lookup"><span data-stu-id="dc659-123">The code associated with a delegate is invoked using a virtual method added to a delegate type.</span></span> <span data-ttu-id="dc659-124">使用函数指针，可以指定不同的约定。</span><span class="sxs-lookup"><span data-stu-id="dc659-124">Using function pointers, you can specify different conventions.</span></span>

## <a name="delegates-overview"></a><span data-ttu-id="dc659-125">委托概述</span><span class="sxs-lookup"><span data-stu-id="dc659-125">Delegates Overview</span></span>

<span data-ttu-id="dc659-126">委托具有以下属性：</span><span class="sxs-lookup"><span data-stu-id="dc659-126">Delegates have the following properties:</span></span>

- <span data-ttu-id="dc659-127">委托类似于 C++ 函数指针，但委托完全面向对象，不像 C++ 指针会记住函数，委托会同时封装对象实例和方法。</span><span class="sxs-lookup"><span data-stu-id="dc659-127">Delegates are similar to C++ function pointers, but delegates are fully object-oriented, and unlike C++ pointers to member functions, delegates encapsulate both an object instance and a method.</span></span>
- <span data-ttu-id="dc659-128">委托允许将方法作为参数进行传递。</span><span class="sxs-lookup"><span data-stu-id="dc659-128">Delegates allow methods to be passed as parameters.</span></span>
- <span data-ttu-id="dc659-129">委托可用于定义回调方法。</span><span class="sxs-lookup"><span data-stu-id="dc659-129">Delegates can be used to define callback methods.</span></span>
- <span data-ttu-id="dc659-130">委托可以链接在一起；例如，可以对一个事件调用多个方法。</span><span class="sxs-lookup"><span data-stu-id="dc659-130">Delegates can be chained together; for example, multiple methods can be called on a single event.</span></span>
- <span data-ttu-id="dc659-131">方法不必与委托类型完全匹配。</span><span class="sxs-lookup"><span data-stu-id="dc659-131">Methods don't have to match the delegate type exactly.</span></span> <span data-ttu-id="dc659-132">有关详细信息，请参阅[使用委托中的变体](../concepts/covariance-contravariance/using-variance-in-delegates.md)。</span><span class="sxs-lookup"><span data-stu-id="dc659-132">For more information, see [Using Variance in Delegates](../concepts/covariance-contravariance/using-variance-in-delegates.md).</span></span>
- <span data-ttu-id="dc659-133">使用 Lambda 表达式可以更简练地编写内联代码块。</span><span class="sxs-lookup"><span data-stu-id="dc659-133">Lambda expressions are a more concise way of writing inline code blocks.</span></span> <span data-ttu-id="dc659-134">Lambda 表达式（在某些上下文中）可编译为委托类型。</span><span class="sxs-lookup"><span data-stu-id="dc659-134">Lambda expressions (in certain contexts) are compiled to delegate types.</span></span> <span data-ttu-id="dc659-135">若要详细了解 lambda 表达式，请参阅 [lambda 表达式](../../language-reference/operators/lambda-expressions.md)。</span><span class="sxs-lookup"><span data-stu-id="dc659-135">For more information about lambda expressions, see [Lambda expressions](../../language-reference/operators/lambda-expressions.md).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="dc659-136">本节内容</span><span class="sxs-lookup"><span data-stu-id="dc659-136">In This Section</span></span>

- [<span data-ttu-id="dc659-137">使用委托</span><span class="sxs-lookup"><span data-stu-id="dc659-137">Using Delegates</span></span>](./using-delegates.md)
- <span data-ttu-id="dc659-138">[何时使用委托，而不是接口（C# 编程指南）](/previous-versions/visualstudio/visual-studio-2010/ms173173(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="dc659-138">[When to Use Delegates Instead of Interfaces (C# Programming Guide)](/previous-versions/visualstudio/visual-studio-2010/ms173173(v=vs.100))</span></span>
- [<span data-ttu-id="dc659-139">带有命名方法的委托与带有匿名方法的委托</span><span class="sxs-lookup"><span data-stu-id="dc659-139">Delegates with Named vs. Anonymous Methods</span></span>](./delegates-with-named-vs-anonymous-methods.md)
- [<span data-ttu-id="dc659-140">使用委托中的变体</span><span class="sxs-lookup"><span data-stu-id="dc659-140">Using Variance in Delegates</span></span>](../concepts/covariance-contravariance/using-variance-in-delegates.md)
- [<span data-ttu-id="dc659-141">如何合并委托（多播委托）</span><span class="sxs-lookup"><span data-stu-id="dc659-141">How to combine delegates (Multicast Delegates)</span></span>](./how-to-combine-delegates-multicast-delegates.md)
- [<span data-ttu-id="dc659-142">如何声明、实例化和使用委托</span><span class="sxs-lookup"><span data-stu-id="dc659-142">How to declare, instantiate, and use a delegate</span></span>](./how-to-declare-instantiate-and-use-a-delegate.md)

## <a name="c-language-specification"></a><span data-ttu-id="dc659-143">C# 语言规范</span><span class="sxs-lookup"><span data-stu-id="dc659-143">C# Language Specification</span></span>

<span data-ttu-id="dc659-144">有关详细信息，请参阅 [C# 语言规范](/dotnet/csharp/language-reference/language-specification/introduction)中的[委托](~/_csharplang/spec/delegates.md)。</span><span class="sxs-lookup"><span data-stu-id="dc659-144">For more information, see [Delegates](~/_csharplang/spec/delegates.md) in the [C# Language Specification](/dotnet/csharp/language-reference/language-specification/introduction).</span></span> <span data-ttu-id="dc659-145">该语言规范是 C# 语法和用法的权威资料。</span><span class="sxs-lookup"><span data-stu-id="dc659-145">The language specification is the definitive source for C# syntax and usage.</span></span>

## <a name="featured-book-chapters"></a><span data-ttu-id="dc659-146">重要章节</span><span class="sxs-lookup"><span data-stu-id="dc659-146">Featured Book Chapters</span></span>

- <span data-ttu-id="dc659-147">[C# 3.0 手册（第三版）：面向 C# 3.0 程序员的超过 250 个解决方案](/previous-versions/visualstudio/visual-studio-2008/ff518995(v=orm.10))中的[委托、事件和 Lambda 表达式](/previous-versions/visualstudio/visual-studio-2008/ff518994(v=orm.10))</span><span class="sxs-lookup"><span data-stu-id="dc659-147">[Delegates, Events, and Lambda Expressions](/previous-versions/visualstudio/visual-studio-2008/ff518994(v=orm.10)) in [C# 3.0 Cookbook, Third Edition: More than 250 solutions for C# 3.0 programmers](/previous-versions/visualstudio/visual-studio-2008/ff518995(v=orm.10))</span></span>
- <span data-ttu-id="dc659-148">[学习 C# 3.0：掌握 C# 3.0 基础知识](/previous-versions/visualstudio/visual-studio-2008/ff652493(v=orm.10))中的[委托和事件](/previous-versions/visualstudio/visual-studio-2008/ff652490(v=orm.10))</span><span class="sxs-lookup"><span data-stu-id="dc659-148">[Delegates and Events](/previous-versions/visualstudio/visual-studio-2008/ff652490(v=orm.10)) in [Learning C# 3.0: Master the fundamentals of C# 3.0](/previous-versions/visualstudio/visual-studio-2008/ff652493(v=orm.10))</span></span>

## <a name="see-also"></a><span data-ttu-id="dc659-149">请参阅</span><span class="sxs-lookup"><span data-stu-id="dc659-149">See also</span></span>

- <xref:System.Delegate>
- [<span data-ttu-id="dc659-150">C# 编程指南</span><span class="sxs-lookup"><span data-stu-id="dc659-150">C# Programming Guide</span></span>](../index.md)
- [<span data-ttu-id="dc659-151">事件</span><span class="sxs-lookup"><span data-stu-id="dc659-151">Events</span></span>](../events/index.md)
