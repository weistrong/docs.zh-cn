---
title: F# 中的函数编程简介
description: 了解 F# 中的函数编程的基础知识。
ms.date: 10/29/2018
ms.openlocfilehash: 44242a4319a331312a003a555d1483f2a3f1a90d
ms.sourcegitcommit: 9b877e160c326577e8aa5ead22a937110d80fa44
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/11/2020
ms.locfileid: "97110580"
---
# <a name="introduction-to-functional-programming-in-f"></a><span data-ttu-id="5abf8-103">F\# 中的函数编程简介</span><span class="sxs-lookup"><span data-stu-id="5abf8-103">Introduction to Functional Programming in F\#</span></span>

<span data-ttu-id="5abf8-104">函数编程是一种编程方式，这种方式强调函数和不可变数据的使用。</span><span class="sxs-lookup"><span data-stu-id="5abf8-104">Functional programming is a style of programming that emphasizes the use of functions and immutable data.</span></span> <span data-ttu-id="5abf8-105">类型化函数编程是指将函数编程与静态类型（如 F#）结合使用。</span><span class="sxs-lookup"><span data-stu-id="5abf8-105">Typed functional programming is when functional programming is combined with static types, such as with F#.</span></span> <span data-ttu-id="5abf8-106">通常，函数编程中强调了以下概念：</span><span class="sxs-lookup"><span data-stu-id="5abf8-106">In general, the following concepts are emphasized in functional programming:</span></span>

* <span data-ttu-id="5abf8-107">函数作为你使用的主构造</span><span class="sxs-lookup"><span data-stu-id="5abf8-107">Functions as the primary constructs you use</span></span>
* <span data-ttu-id="5abf8-108">表达式，而不是语句</span><span class="sxs-lookup"><span data-stu-id="5abf8-108">Expressions instead of statements</span></span>
* <span data-ttu-id="5abf8-109">不可变值优于变量</span><span class="sxs-lookup"><span data-stu-id="5abf8-109">Immutable values over variables</span></span>
* <span data-ttu-id="5abf8-110">声明性编程优于命令式编程</span><span class="sxs-lookup"><span data-stu-id="5abf8-110">Declarative programming over imperative programming</span></span>

<span data-ttu-id="5abf8-111">在此系列中，你将了解使用 F# 的函数编程中的概念和模式。</span><span class="sxs-lookup"><span data-stu-id="5abf8-111">Throughout this series, you'll explore concepts and patterns in functional programming using F#.</span></span> <span data-ttu-id="5abf8-112">在此过程中，你也将了解一些 F#。</span><span class="sxs-lookup"><span data-stu-id="5abf8-112">Along the way, you'll learn some F# too.</span></span>

## <a name="terminology"></a><span data-ttu-id="5abf8-113">术语</span><span class="sxs-lookup"><span data-stu-id="5abf8-113">Terminology</span></span>

<span data-ttu-id="5abf8-114">函数编程与其他编程范例一样附带词汇，你最终需要学习该词汇。</span><span class="sxs-lookup"><span data-stu-id="5abf8-114">Functional programming, like other programming paradigms, comes with a vocabulary that you will eventually need to learn.</span></span> <span data-ttu-id="5abf8-115">下面是你将看到的一些常见术语：</span><span class="sxs-lookup"><span data-stu-id="5abf8-115">Here are some common terms you'll see all of the time:</span></span>

* <span data-ttu-id="5abf8-116">函数 - 函数是在给定输入时将生成输出的构造。</span><span class="sxs-lookup"><span data-stu-id="5abf8-116">**Function** - A function is a construct that will produce an output when given an input.</span></span> <span data-ttu-id="5abf8-117">更正式地说，它将项从一个集映射到另一个集。</span><span class="sxs-lookup"><span data-stu-id="5abf8-117">More formally, it _maps_ an item from one set to another set.</span></span> <span data-ttu-id="5abf8-118">这种形式通过许多方式变得具体，尤其是在使用对数据集合进行操作的函数时。</span><span class="sxs-lookup"><span data-stu-id="5abf8-118">This formalism is lifted into the concrete in many ways, especially when using functions that operate on collections of data.</span></span> <span data-ttu-id="5abf8-119">它是函数编程中最基本（且最重要）的概念。</span><span class="sxs-lookup"><span data-stu-id="5abf8-119">It is the most basic (and important) concept in functional programming.</span></span>
* <span data-ttu-id="5abf8-120">表达式 - 表达式是代码中生成值的构造。</span><span class="sxs-lookup"><span data-stu-id="5abf8-120">**Expression** - An expression is a construct in code that produces a value.</span></span> <span data-ttu-id="5abf8-121">在 F# 中，此值必须绑定或被显式忽略。</span><span class="sxs-lookup"><span data-stu-id="5abf8-121">In F#, this value must be bound or explicitly ignored.</span></span> <span data-ttu-id="5abf8-122">表达式可以完全替换为函数调用。</span><span class="sxs-lookup"><span data-stu-id="5abf8-122">An expression can be trivially replaced by a function call.</span></span>
* <span data-ttu-id="5abf8-123">纯度 - 纯度是函数的属性，以致相同参数的返回值总是相同的，并且其计算没有任何副作用。</span><span class="sxs-lookup"><span data-stu-id="5abf8-123">**Purity** - Purity is a property of a function such that its return value is always the same for the same arguments, and that its evaluation has no side effects.</span></span> <span data-ttu-id="5abf8-124">纯函数完全取决于其参数。</span><span class="sxs-lookup"><span data-stu-id="5abf8-124">A pure function depends entirely on its arguments.</span></span>
* <span data-ttu-id="5abf8-125">引用透明度 - 引用透明度是表达式的属性，以便可以不影响程序行为的情况下将表达式替换为其输出。</span><span class="sxs-lookup"><span data-stu-id="5abf8-125">**Referential Transparency** - Referential Transparency is a property of expressions such that they can be replaced with their output without affecting a program's behavior.</span></span>
* <span data-ttu-id="5abf8-126">不可变性 - 不可变性表示值不能就地更改。</span><span class="sxs-lookup"><span data-stu-id="5abf8-126">**Immutability** - Immutability means that a value cannot be changed in-place.</span></span> <span data-ttu-id="5abf8-127">这与变量不同，后者可以就地更改。</span><span class="sxs-lookup"><span data-stu-id="5abf8-127">This is in contrast with variables, which can change in place.</span></span>

## <a name="examples"></a><span data-ttu-id="5abf8-128">示例</span><span class="sxs-lookup"><span data-stu-id="5abf8-128">Examples</span></span>

<span data-ttu-id="5abf8-129">以下示例说明了这些核心概念。</span><span class="sxs-lookup"><span data-stu-id="5abf8-129">The following examples demonstrate these core concepts.</span></span>

### <a name="functions"></a><span data-ttu-id="5abf8-130">函数</span><span class="sxs-lookup"><span data-stu-id="5abf8-130">Functions</span></span>

<span data-ttu-id="5abf8-131">函数编程中最常见且最基本的构造是函数。</span><span class="sxs-lookup"><span data-stu-id="5abf8-131">The most common and fundamental construct in functional programming is the function.</span></span> <span data-ttu-id="5abf8-132">下面是向整数添加 1 的简单函数：</span><span class="sxs-lookup"><span data-stu-id="5abf8-132">Here's a simple function that adds 1 to an integer:</span></span>

```fsharp
let addOne x = x + 1
```

<span data-ttu-id="5abf8-133">其类型签名如下所示：</span><span class="sxs-lookup"><span data-stu-id="5abf8-133">Its type signature is as follows:</span></span>

```fsharp
val addOne: x:int -> int
```

<span data-ttu-id="5abf8-134">签名可以显示为“`addOne` 接受名为 `x` 的 `int` 并生成 `int`”。</span><span class="sxs-lookup"><span data-stu-id="5abf8-134">The signature can be read as, "`addOne` accepts an `int` named `x` and will produce an `int`".</span></span> <span data-ttu-id="5abf8-135">更正式地说，`addOne` 将值从一个整数集映射到另一个整数集。</span><span class="sxs-lookup"><span data-stu-id="5abf8-135">More formally, `addOne` is _mapping_ a value from the set of integers to the set of integers.</span></span> <span data-ttu-id="5abf8-136">`->` 令牌表示此映射。</span><span class="sxs-lookup"><span data-stu-id="5abf8-136">The `->` token signifies this mapping.</span></span> <span data-ttu-id="5abf8-137">在 F# 中，通常可以查看函数签名以了解它的作用。</span><span class="sxs-lookup"><span data-stu-id="5abf8-137">In F#, you can usually look at the function signature to get a sense for what it does.</span></span>

<span data-ttu-id="5abf8-138">那么，为什么签名非常重要？</span><span class="sxs-lookup"><span data-stu-id="5abf8-138">So, why is the signature important?</span></span> <span data-ttu-id="5abf8-139">在类型化函数编程中，函数的实现通常没有实际类型签名那么重要！</span><span class="sxs-lookup"><span data-stu-id="5abf8-139">In typed functional programming, the implementation of a function is often less important than the actual type signature!</span></span> <span data-ttu-id="5abf8-140">`addOne` 向整数添加值 1 的事实在运行时很有趣，但当你构造程序时，接受并返回 `int` 的事实说明了你实际使用此函数的方式。</span><span class="sxs-lookup"><span data-stu-id="5abf8-140">The fact that `addOne` adds the value 1 to an integer is interesting at runtime, but when you are constructing a program, the fact that it accepts and returns an `int` is what informs how you will actually use this function.</span></span> <span data-ttu-id="5abf8-141">此外，一旦正确使用此函数（在类型签名方面），诊断任何问题就只能在 `addOne` 函数的主体中完成。</span><span class="sxs-lookup"><span data-stu-id="5abf8-141">Furthermore, once you use this function correctly (with respect to its type signature), diagnosing any problems can be done only within the body of the `addOne` function.</span></span> <span data-ttu-id="5abf8-142">这是类型化函数编程的推动力。</span><span class="sxs-lookup"><span data-stu-id="5abf8-142">This is the impetus behind typed functional programming.</span></span>

### <a name="expressions"></a><span data-ttu-id="5abf8-143">表达式</span><span class="sxs-lookup"><span data-stu-id="5abf8-143">Expressions</span></span>

<span data-ttu-id="5abf8-144">表达式是计算结果为值的构造。</span><span class="sxs-lookup"><span data-stu-id="5abf8-144">Expressions are constructs that evaluate to a value.</span></span> <span data-ttu-id="5abf8-145">与执行操作的语句不同，表达式可以被视为执行返回值的操作。</span><span class="sxs-lookup"><span data-stu-id="5abf8-145">In contrast to statements, which perform an action, expressions can be thought of performing an action that gives back a value.</span></span> <span data-ttu-id="5abf8-146">表达式几乎始终用在函数编程中而不是语句中。</span><span class="sxs-lookup"><span data-stu-id="5abf8-146">Expressions are almost always used in functional programming instead of statements.</span></span>

<span data-ttu-id="5abf8-147">请考虑上一个函数 `addOne`。</span><span class="sxs-lookup"><span data-stu-id="5abf8-147">Consider the previous function, `addOne`.</span></span> <span data-ttu-id="5abf8-148">`addOne` 的主体是一个表达式：</span><span class="sxs-lookup"><span data-stu-id="5abf8-148">The body of `addOne` is an expression:</span></span>

```fsharp
// 'x + 1' is an expression!
let addOne x = x + 1
```

<span data-ttu-id="5abf8-149">这是此表达式的结果，用于定义 `addOne` 函数的结果类型。</span><span class="sxs-lookup"><span data-stu-id="5abf8-149">It is the result of this expression that defines the result type of the `addOne` function.</span></span> <span data-ttu-id="5abf8-150">例如，构成此函数的表达式可以更改为其他类型，例如 `string`：</span><span class="sxs-lookup"><span data-stu-id="5abf8-150">For example, the expression that makes up this function could be changed to be a different type, such as a `string`:</span></span>

```fsharp
let addOne x = x.ToString() + "1"
```

<span data-ttu-id="5abf8-151">函数的签名现在：</span><span class="sxs-lookup"><span data-stu-id="5abf8-151">The signature of the function is now:</span></span>

```fsharp
val addOne: x:'a -> string
```

<span data-ttu-id="5abf8-152">由于 F# 中的任何类型都可以对其调用 `ToString()`，因此 `x` 的类型已变为泛型（称为[自动泛化](../language-reference/generics/automatic-generalization.md)），并且结果类型为 `string`。</span><span class="sxs-lookup"><span data-stu-id="5abf8-152">Since any type in F# can have `ToString()` called on it, the type of `x` has been made generic (called [Automatic Generalization](../language-reference/generics/automatic-generalization.md)), and the resultant type is a `string`.</span></span>

<span data-ttu-id="5abf8-153">表达式不仅仅是函数的主体。</span><span class="sxs-lookup"><span data-stu-id="5abf8-153">Expressions are not just the bodies of functions.</span></span> <span data-ttu-id="5abf8-154">可以使用表达式来生成在其他位置使用的值。</span><span class="sxs-lookup"><span data-stu-id="5abf8-154">You can have expressions that produce a value you use elsewhere.</span></span> <span data-ttu-id="5abf8-155">一个常见表达式为 `if`：</span><span class="sxs-lookup"><span data-stu-id="5abf8-155">A common one is `if`:</span></span>

```fsharp
// Checks if 'x' is odd by using the mod operator
let isOdd x = x % 2 <> 0

let addOneIfOdd input =
    let result =
        if isOdd input then
            input + 1
        else
            input

    result
```

<span data-ttu-id="5abf8-156">`if` 表达式将生成一个名为 `result` 的值。</span><span class="sxs-lookup"><span data-stu-id="5abf8-156">The `if` expression produces a value called `result`.</span></span> <span data-ttu-id="5abf8-157">请注意，你可以完全省略 `result`，使 `if` 表达式成为 `addOneIfOdd` 函数的主体。</span><span class="sxs-lookup"><span data-stu-id="5abf8-157">Note that you could omit `result` entirely, making the `if` expression the body of the `addOneIfOdd` function.</span></span> <span data-ttu-id="5abf8-158">需要记住的重要一点是，表达式会生成值。</span><span class="sxs-lookup"><span data-stu-id="5abf8-158">The key thing to remember about expressions is that they produce a value.</span></span>

<span data-ttu-id="5abf8-159">有一种特殊类型 `unit`，它在没有返回任何内容时使用。</span><span class="sxs-lookup"><span data-stu-id="5abf8-159">There is a special type, `unit`, that is used when there is nothing to return.</span></span> <span data-ttu-id="5abf8-160">例如，考虑此简单函数：</span><span class="sxs-lookup"><span data-stu-id="5abf8-160">For example, consider this simple function:</span></span>

```fsharp
let printString (str: string) =
    printfn $"String is: {str}"
```

<span data-ttu-id="5abf8-161">签名如下所示：</span><span class="sxs-lookup"><span data-stu-id="5abf8-161">The signature looks like this:</span></span>

```fsharp
val printString: str:string -> unit
```

<span data-ttu-id="5abf8-162">`unit` 类型指示没有返回实际值。</span><span class="sxs-lookup"><span data-stu-id="5abf8-162">The `unit` type indicates that there is no actual value being returned.</span></span> <span data-ttu-id="5abf8-163">这在尽管工作没有返回任何值，但通常必须“工作”的情况下非常有用。</span><span class="sxs-lookup"><span data-stu-id="5abf8-163">This is useful when you have a routine that must "do work" despite having no value to return as a result of that work.</span></span>

<span data-ttu-id="5abf8-164">这与命令式编程形成鲜明对比，其中等效的 `if` 构造是一个语句，生成值通常是使用转变变量来完成的。</span><span class="sxs-lookup"><span data-stu-id="5abf8-164">This is in sharp contrast to imperative programming, where the equivalent `if` construct is a statement, and producing values is often done with mutating variables.</span></span> <span data-ttu-id="5abf8-165">例如，在 C# 中，代码可能如下所示：</span><span class="sxs-lookup"><span data-stu-id="5abf8-165">For example, in C#, the code might be written like this:</span></span>

```csharp
bool IsOdd(int x) => x % 2 != 0;

int AddOneIfOdd(int input)
{
    var result = input;

    if (IsOdd(input))
    {
        result = input + 1;
    }

    return result;
}
```

<span data-ttu-id="5abf8-166">值得注意的是，C# 和其他 C 样式语言都支持[三元表达式](../../csharp/language-reference/operators/conditional-operator.md)，以进行基于表达式的条件编程。</span><span class="sxs-lookup"><span data-stu-id="5abf8-166">It's worth noting that C# and other C-style languages do support the [ternary expression](../../csharp/language-reference/operators/conditional-operator.md), which allows for expression-based conditional programming.</span></span>

<span data-ttu-id="5abf8-167">在函数编程中，很少使用语句转变值。</span><span class="sxs-lookup"><span data-stu-id="5abf8-167">In functional programming, it is rare to mutate values with statements.</span></span> <span data-ttu-id="5abf8-168">尽管某些函数语言支持语句和转变，但在函数编程中使用这些概念并不常见。</span><span class="sxs-lookup"><span data-stu-id="5abf8-168">Although some functional languages support statements and mutation, it is not common to use these concepts in functional programming.</span></span>

### <a name="pure-functions"></a><span data-ttu-id="5abf8-169">纯函数</span><span class="sxs-lookup"><span data-stu-id="5abf8-169">Pure functions</span></span>

<span data-ttu-id="5abf8-170">如前文所述，纯函数是满足以下情况的函数：</span><span class="sxs-lookup"><span data-stu-id="5abf8-170">As previously mentioned, pure functions are functions that:</span></span>

* <span data-ttu-id="5abf8-171">相同输入的计算结果始终为相同的值。</span><span class="sxs-lookup"><span data-stu-id="5abf8-171">Always evaluate to the same value for the same input.</span></span>
* <span data-ttu-id="5abf8-172">没有任何副作用。</span><span class="sxs-lookup"><span data-stu-id="5abf8-172">Have no side effects.</span></span>

<span data-ttu-id="5abf8-173">在此上下文中考虑数学函数非常有用。</span><span class="sxs-lookup"><span data-stu-id="5abf8-173">It is helpful to think of mathematical functions in this context.</span></span> <span data-ttu-id="5abf8-174">在数学中，函数仅取决于其参数，并且没有任何副作用。</span><span class="sxs-lookup"><span data-stu-id="5abf8-174">In mathematics, functions depend only on their arguments and do not have any side effects.</span></span> <span data-ttu-id="5abf8-175">在数学函数 `f(x) = x + 1` 中，`f(x)` 的值仅取决于 `x` 的值。</span><span class="sxs-lookup"><span data-stu-id="5abf8-175">In the mathematical function `f(x) = x + 1`, the value of `f(x)` depends only on the value of `x`.</span></span> <span data-ttu-id="5abf8-176">函数编程中的纯函数是相同的。</span><span class="sxs-lookup"><span data-stu-id="5abf8-176">Pure functions in functional programming are the same way.</span></span>

<span data-ttu-id="5abf8-177">编写纯函数时，该函数必须仅取决于其参数，并且不会执行导致副作用的任何操作。</span><span class="sxs-lookup"><span data-stu-id="5abf8-177">When writing a pure function, the function must depend only on its arguments and not perform any action that results in a side effect.</span></span>

<span data-ttu-id="5abf8-178">下面是非纯函数的一个示例，因为它取决于可变的全局状态：</span><span class="sxs-lookup"><span data-stu-id="5abf8-178">Here is an example of a non-pure function because it depends on global, mutable state:</span></span>

```fsharp
let mutable value = 1

let addOneToValue x = x + value
```

<span data-ttu-id="5abf8-179">`addOneToValue` 函数明显是非纯函数，因为可以随时更改 `value`，使其值不同于 1。</span><span class="sxs-lookup"><span data-stu-id="5abf8-179">The `addOneToValue` function is clearly impure, because `value` could be changed at any time to have a different value than 1.</span></span> <span data-ttu-id="5abf8-180">应避免在函数编程中使用取决于全局值的模式。</span><span class="sxs-lookup"><span data-stu-id="5abf8-180">This pattern of depending on a global value is to be avoided in functional programming.</span></span>

<span data-ttu-id="5abf8-181">下面是非纯函数的另一个示例，因为它产生副作用：</span><span class="sxs-lookup"><span data-stu-id="5abf8-181">Here is another example of a non-pure function, because it performs a side effect:</span></span>

```fsharp
let addOneToValue x =
    printfn $"x is %d{x}"
    x + 1
```

<span data-ttu-id="5abf8-182">尽管此函数不取决于全局值，但它会将 `x` 的值写入程序的输出。</span><span class="sxs-lookup"><span data-stu-id="5abf8-182">Although this function does not depend on a global value, it writes the value of `x` to the output of the program.</span></span> <span data-ttu-id="5abf8-183">尽管这样做在本质上没有错误，但意味着函数是非纯函数。</span><span class="sxs-lookup"><span data-stu-id="5abf8-183">Although there is nothing inherently wrong with doing this, it does mean that the function is not pure.</span></span> <span data-ttu-id="5abf8-184">如果程序的其他部分取决于程序的外部内容（如输出缓冲区），则调用此函数可能会影响程序的其他部分。</span><span class="sxs-lookup"><span data-stu-id="5abf8-184">If another part of your program depends on something external to the program, such as the output buffer, then calling this function can affect that other part of your program.</span></span>

<span data-ttu-id="5abf8-185">删除 `printfn` 语句会使函数变纯：</span><span class="sxs-lookup"><span data-stu-id="5abf8-185">Removing the `printfn` statement makes the function pure:</span></span>

```fsharp
let addOneToValue x = x + 1
```

<span data-ttu-id="5abf8-186">尽管此函数在本质上比不上带有 `printfn` 语句的先前版本，但它保证了此函数确实会返回值。</span><span class="sxs-lookup"><span data-stu-id="5abf8-186">Although this function is not inherently _better_ than the previous version with the `printfn` statement, it does guarantee that all this function does is return a value.</span></span> <span data-ttu-id="5abf8-187">调用此函数任意次数都会产生相同的结果：仅生成值。</span><span class="sxs-lookup"><span data-stu-id="5abf8-187">Calling this function any number of times produces the same result: it just produces a value.</span></span> <span data-ttu-id="5abf8-188">纯度提供的可预测性是许多函数程序员寻求的目标。</span><span class="sxs-lookup"><span data-stu-id="5abf8-188">The predictability given by purity is something many functional programmers strive for.</span></span>

### <a name="immutability"></a><span data-ttu-id="5abf8-189">不可变性</span><span class="sxs-lookup"><span data-stu-id="5abf8-189">Immutability</span></span>

<span data-ttu-id="5abf8-190">最后，类型化函数编程的最基本概念之一是不可变性。</span><span class="sxs-lookup"><span data-stu-id="5abf8-190">Finally, one of the most fundamental concepts of typed functional programming is immutability.</span></span> <span data-ttu-id="5abf8-191">在 F# 中，所有值在默认情况下都是不可变的。</span><span class="sxs-lookup"><span data-stu-id="5abf8-191">In F#, all values are immutable by default.</span></span> <span data-ttu-id="5abf8-192">这意味着，除非显式将它们标记为可变，否则无法就地转变它们。</span><span class="sxs-lookup"><span data-stu-id="5abf8-192">That means they cannot be mutated in-place unless you explicitly mark them as mutable.</span></span>

<span data-ttu-id="5abf8-193">实际上，使用不可变值是指将编程方式从“我需要更改某些内容”更改为“我需要生成新值”。</span><span class="sxs-lookup"><span data-stu-id="5abf8-193">In practice, working with immutable values means that you change your approach to programming from, "I need to change something", to "I need to produce a new value".</span></span>

<span data-ttu-id="5abf8-194">例如，向某个值添加 1 意味着生成值，而不是转变现有值：</span><span class="sxs-lookup"><span data-stu-id="5abf8-194">For example, adding 1 to a value means producing a new value, not mutating the existing one:</span></span>

```fsharp
let value = 1
let secondValue = value + 1
```

<span data-ttu-id="5abf8-195">在 F# 中，以下代码不会转变 `value` 函数；而是执行相等性检查：</span><span class="sxs-lookup"><span data-stu-id="5abf8-195">In F#, the following code does **not** mutate the `value` function; instead, it performs an equality check:</span></span>

```fsharp
let value = 1
value = value + 1 // Produces a 'bool' value!
```

<span data-ttu-id="5abf8-196">一些函数编程语言根本不支持转变。</span><span class="sxs-lookup"><span data-stu-id="5abf8-196">Some functional programming languages do not support mutation at all.</span></span> <span data-ttu-id="5abf8-197">在 F# 中，它是受支持的，但它不是值的默认行为。</span><span class="sxs-lookup"><span data-stu-id="5abf8-197">In F#, it is supported, but it is not the default behavior for values.</span></span>

<span data-ttu-id="5abf8-198">此概念甚至进一步扩展到数据结构。</span><span class="sxs-lookup"><span data-stu-id="5abf8-198">This concept extends even further to data structures.</span></span> <span data-ttu-id="5abf8-199">在函数编程中，不可变的数据结构（如集等）的实现方式不同于最初预期的实现。</span><span class="sxs-lookup"><span data-stu-id="5abf8-199">In functional programming, immutable data structures such as sets (and many more) have a different implementation than you might initially expect.</span></span> <span data-ttu-id="5abf8-200">从概念上讲，将项添加到集的操作不会更改集，而会生成添加了值的新集。</span><span class="sxs-lookup"><span data-stu-id="5abf8-200">Conceptually, something like adding an item to a set does not change the set, it produces a _new_ set with the added value.</span></span> <span data-ttu-id="5abf8-201">在这种情况下，这通常是通过不同的数据结构来完成的，该结构允许有效地跟踪值，从而可以为数据提供适当的表示形式。</span><span class="sxs-lookup"><span data-stu-id="5abf8-201">Under the covers, this is often accomplished by a different data structure that allows for efficiently tracking a value so that the appropriate representation of the data can be given as a result.</span></span>

<span data-ttu-id="5abf8-202">这种使用值和数据结构的方式非常重要，因为它强制你将任何修改操作视为创建新版本。</span><span class="sxs-lookup"><span data-stu-id="5abf8-202">This style of working with values and data structures is critical, as it forces you to treat any operation that modifies something as if it creates a new version of that thing.</span></span> <span data-ttu-id="5abf8-203">这样，相等性和可比性等情况在程序中保持一致。</span><span class="sxs-lookup"><span data-stu-id="5abf8-203">This allows for things like equality and comparability to be consistent in your programs.</span></span>

## <a name="next-steps"></a><span data-ttu-id="5abf8-204">后续步骤</span><span class="sxs-lookup"><span data-stu-id="5abf8-204">Next steps</span></span>

<span data-ttu-id="5abf8-205">下一部分将全面介绍函数，探索在函数编程中使用它们的不同方式。</span><span class="sxs-lookup"><span data-stu-id="5abf8-205">The next section will thoroughly cover functions, exploring different ways you can use them in functional programming.</span></span>

<span data-ttu-id="5abf8-206">[第一类函数](first-class-functions.md)深入探讨函数，演示如何在各种上下文中使用它们。</span><span class="sxs-lookup"><span data-stu-id="5abf8-206">[First-class functions](first-class-functions.md) explores functions deeply, showing how you can use them in various contexts.</span></span>

## <a name="further-reading"></a><span data-ttu-id="5abf8-207">延伸阅读</span><span class="sxs-lookup"><span data-stu-id="5abf8-207">Further reading</span></span>

<span data-ttu-id="5abf8-208">[功能性思考](https://fsharpforfunandprofit.com/posts/thinking-functionally-intro/)系列是另一个有用的资源，可了解使用 F# 的函数编程。</span><span class="sxs-lookup"><span data-stu-id="5abf8-208">The [Thinking Functionally](https://fsharpforfunandprofit.com/posts/thinking-functionally-intro/) series is another great resource to learn about functional programming with F#.</span></span> <span data-ttu-id="5abf8-209">它以一种实用且易于读取的方式介绍函数编程的基础知识，使用 F# 功能来说明这些概念。</span><span class="sxs-lookup"><span data-stu-id="5abf8-209">It covers fundamentals of functional programming in a pragmatic and easy-to-read way, using F# features to illustrate the concepts.</span></span>
