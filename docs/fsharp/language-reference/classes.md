---
title: 类
description: '了解 F # 类的类型，这些类型表示可以具有属性、方法和事件的对象。'
ms.date: 05/16/2016
ms.openlocfilehash: fd6638e0f1c08cf667a73582e19b2bb5bba46e20
ms.sourcegitcommit: 7ef96827b161ef3fcde75f79d839885632e26ef1
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/07/2021
ms.locfileid: "97970162"
---
# <a name="classes"></a><span data-ttu-id="18e7a-103">类</span><span class="sxs-lookup"><span data-stu-id="18e7a-103">Classes</span></span>

<span data-ttu-id="18e7a-104">*类* 是表示可以具有属性、方法和事件的对象的类型。</span><span class="sxs-lookup"><span data-stu-id="18e7a-104">*Classes* are types that represent objects that can have properties, methods, and events.</span></span>

## <a name="syntax"></a><span data-ttu-id="18e7a-105">语法</span><span class="sxs-lookup"><span data-stu-id="18e7a-105">Syntax</span></span>

```fsharp
// Class definition:
type [access-modifier] type-name [type-params] [access-modifier] ( parameter-list ) [ as identifier ] =
[ class ]
[ inherit base-type-name(base-constructor-args) ]
[ let-bindings ]
[ do-bindings ]
member-list
...
[ end ]
// Mutually recursive class definitions:
type [access-modifier] type-name1 ...
and [access-modifier] type-name2 ...
...
```

## <a name="remarks"></a><span data-ttu-id="18e7a-106">备注</span><span class="sxs-lookup"><span data-stu-id="18e7a-106">Remarks</span></span>

<span data-ttu-id="18e7a-107">类表示 .NET 对象类型的基本说明;类是在 F # 中支持面向对象的编程的主要类型概念。</span><span class="sxs-lookup"><span data-stu-id="18e7a-107">Classes represent the fundamental description of .NET object types; the class is the primary type concept that supports object-oriented programming in F#.</span></span>

<span data-ttu-id="18e7a-108">在上述语法中， `type-name` 是任何有效的标识符。</span><span class="sxs-lookup"><span data-stu-id="18e7a-108">In the preceding syntax, the `type-name` is any valid identifier.</span></span> <span data-ttu-id="18e7a-109">`type-params`描述可选的泛型类型参数。</span><span class="sxs-lookup"><span data-stu-id="18e7a-109">The `type-params` describes optional generic type parameters.</span></span> <span data-ttu-id="18e7a-110">它包含类型参数名称和括在尖括号中的约束 (`<` 和 `>`) 。</span><span class="sxs-lookup"><span data-stu-id="18e7a-110">It consists of type parameter names and constraints enclosed in angle brackets (`<` and `>`).</span></span> <span data-ttu-id="18e7a-111">有关详细信息，请参阅 [泛型](./generics/index.md) 和 [约束](./generics/constraints.md)。</span><span class="sxs-lookup"><span data-stu-id="18e7a-111">For more information, see [Generics](./generics/index.md) and [Constraints](./generics/constraints.md).</span></span> <span data-ttu-id="18e7a-112">`parameter-list`描述构造函数参数。</span><span class="sxs-lookup"><span data-stu-id="18e7a-112">The `parameter-list` describes constructor parameters.</span></span> <span data-ttu-id="18e7a-113">第一个访问修饰符适用于类型;第二种情况适用于主构造函数。</span><span class="sxs-lookup"><span data-stu-id="18e7a-113">The first access modifier pertains to the type; the second pertains to the primary constructor.</span></span> <span data-ttu-id="18e7a-114">在这两种情况下，默认值为 `public` 。</span><span class="sxs-lookup"><span data-stu-id="18e7a-114">In both cases, the default is `public`.</span></span>

<span data-ttu-id="18e7a-115">使用关键字指定类的基类 `inherit` 。</span><span class="sxs-lookup"><span data-stu-id="18e7a-115">You specify the base class for a class by using the `inherit` keyword.</span></span> <span data-ttu-id="18e7a-116">您必须为基类构造函数提供参数（在括号中）。</span><span class="sxs-lookup"><span data-stu-id="18e7a-116">You must supply arguments, in parentheses, for the base class constructor.</span></span>

<span data-ttu-id="18e7a-117">使用绑定声明类的本地字段或函数值 `let` ，并且必须遵循绑定的通用规则 `let` 。</span><span class="sxs-lookup"><span data-stu-id="18e7a-117">You declare fields or function values that are local to the class by using `let` bindings, and you must follow the general rules for `let` bindings.</span></span> <span data-ttu-id="18e7a-118">`do-bindings`部分包含在对象构造时要执行的代码。</span><span class="sxs-lookup"><span data-stu-id="18e7a-118">The `do-bindings` section includes code to be executed upon object construction.</span></span>

<span data-ttu-id="18e7a-119">`member-list`包含其他构造函数、实例和静态方法声明、接口声明、抽象绑定以及属性和事件声明。</span><span class="sxs-lookup"><span data-stu-id="18e7a-119">The `member-list` consists of additional constructors, instance and static method declarations, interface declarations, abstract bindings, and property and event declarations.</span></span> <span data-ttu-id="18e7a-120">[成员](./members/index.md)中对它们进行了介绍。</span><span class="sxs-lookup"><span data-stu-id="18e7a-120">These are described in [Members](./members/index.md).</span></span>

<span data-ttu-id="18e7a-121">`identifier`与可选关键字一起使用的可为 `as` 实例变量提供名称，也可以在类型定义中使用它来引用类型的实例。</span><span class="sxs-lookup"><span data-stu-id="18e7a-121">The `identifier` that is used with the optional `as` keyword gives a name to the instance variable, or self identifier, which can be used in the type definition to refer to the instance of the type.</span></span> <span data-ttu-id="18e7a-122">有关详细信息，请参阅本主题后面的自我标识符部分。</span><span class="sxs-lookup"><span data-stu-id="18e7a-122">For more information, see the section Self Identifiers later in this topic.</span></span>

<span data-ttu-id="18e7a-123">`class` `end` 标记定义的开头和结尾的关键字和都是可选的。</span><span class="sxs-lookup"><span data-stu-id="18e7a-123">The keywords `class` and `end` that mark the start and end of the definition are optional.</span></span>

<span data-ttu-id="18e7a-124">相互引用的相互递归类型与关键字联接在一起， `and` 就像相互递归函数一样。</span><span class="sxs-lookup"><span data-stu-id="18e7a-124">Mutually recursive types, which are types that reference each other, are joined together with the `and` keyword just as mutually recursive functions are.</span></span> <span data-ttu-id="18e7a-125">有关示例，请参阅 "互相递归类型" 一节。</span><span class="sxs-lookup"><span data-stu-id="18e7a-125">For an example, see the section Mutually Recursive Types.</span></span>

## <a name="constructors"></a><span data-ttu-id="18e7a-126">构造函数</span><span class="sxs-lookup"><span data-stu-id="18e7a-126">Constructors</span></span>

<span data-ttu-id="18e7a-127">构造函数是创建类类型的实例的代码。</span><span class="sxs-lookup"><span data-stu-id="18e7a-127">The constructor is code that creates an instance of the class type.</span></span> <span data-ttu-id="18e7a-128">类的构造函数在 F # 中的工作方式与在其他 .NET 语言中的工作方式有所不同。</span><span class="sxs-lookup"><span data-stu-id="18e7a-128">Constructors for classes work somewhat differently in F# than they do in other .NET languages.</span></span> <span data-ttu-id="18e7a-129">在 F # 类中，始终存在一个主构造函数，该构造函数的参数在类型名称后面的中进行了描述 `parameter-list` ，并且其正文包含 `let` `let rec` 类声明和下面的绑定开头的 (和) 绑定 `do` 。</span><span class="sxs-lookup"><span data-stu-id="18e7a-129">In an F# class, there is always a primary constructor whose arguments are described in the `parameter-list` that follows the type name, and whose body consists of the `let` (and `let rec`) bindings at the start of the class declaration and the `do` bindings that follow.</span></span> <span data-ttu-id="18e7a-130">主构造函数的参数在整个类声明的范围内。</span><span class="sxs-lookup"><span data-stu-id="18e7a-130">The arguments of the primary constructor are in scope throughout the class declaration.</span></span>

<span data-ttu-id="18e7a-131">您可以使用关键字添加其他构造函数 `new` 来添加成员，如下所示：</span><span class="sxs-lookup"><span data-stu-id="18e7a-131">You can add additional constructors by using the `new` keyword to add a member, as follows:</span></span>

<span data-ttu-id="18e7a-132">`new`(`argument-list`) = `constructor-body`</span><span class="sxs-lookup"><span data-stu-id="18e7a-132">`new`(`argument-list`) = `constructor-body`</span></span>

<span data-ttu-id="18e7a-133">新构造函数的主体必须调用在类声明顶部指定的主构造函数。</span><span class="sxs-lookup"><span data-stu-id="18e7a-133">The body of the new constructor must invoke the primary constructor that is specified at the top of the class declaration.</span></span>

<span data-ttu-id="18e7a-134">下面的示例阐释了这一概念。</span><span class="sxs-lookup"><span data-stu-id="18e7a-134">The following example illustrates this concept.</span></span> <span data-ttu-id="18e7a-135">在下面的代码中， `MyClass` 有两个构造函数，这是一个带有两个自变量的主构造函数，另一个不采用参数的构造函数。</span><span class="sxs-lookup"><span data-stu-id="18e7a-135">In the following code, `MyClass` has two constructors, a primary constructor that takes two arguments and another constructor that takes no arguments.</span></span>

[!code-fsharp[Main](~/samples/snippets/fsharp/lang-ref-1/snippet2401.fs)]

## <a name="let-and-do-bindings"></a><span data-ttu-id="18e7a-136">let 和 do Bindings</span><span class="sxs-lookup"><span data-stu-id="18e7a-136">let and do Bindings</span></span>

<span data-ttu-id="18e7a-137">`let` `do` 类定义中的和绑定构成了主类构造函数的主体，因此每当创建类实例时它们都将运行。</span><span class="sxs-lookup"><span data-stu-id="18e7a-137">The `let` and `do` bindings in a class definition form the body of the primary class constructor, and therefore they run whenever a class instance is created.</span></span> <span data-ttu-id="18e7a-138">如果 `let` 绑定是函数，则将其编译到成员中。</span><span class="sxs-lookup"><span data-stu-id="18e7a-138">If a `let` binding is a function, then it is compiled into a member.</span></span> <span data-ttu-id="18e7a-139">如果 `let` 绑定是未在任何函数或成员中使用的值，则将其编译为构造函数的局部变量。</span><span class="sxs-lookup"><span data-stu-id="18e7a-139">If the `let` binding is a value that is not used in any function or member, then it is compiled into a variable that is local to the constructor.</span></span> <span data-ttu-id="18e7a-140">否则，将编译为类的字段。</span><span class="sxs-lookup"><span data-stu-id="18e7a-140">Otherwise, it is compiled into a field of the class.</span></span> <span data-ttu-id="18e7a-141">`do`接下来的表达式编译到主构造函数中，并为每个实例执行初始化代码。</span><span class="sxs-lookup"><span data-stu-id="18e7a-141">The `do` expressions that follow are compiled into the primary constructor and execute initialization code for every instance.</span></span> <span data-ttu-id="18e7a-142">由于任何其他构造函数始终调用主构造函数，因此 `let` 绑定和 `do` 绑定始终执行，而不考虑调用哪个构造函数。</span><span class="sxs-lookup"><span data-stu-id="18e7a-142">Because any additional constructors always call the primary constructor, the `let` bindings and `do` bindings always execute regardless of which constructor is called.</span></span>

<span data-ttu-id="18e7a-143">通过绑定创建的字段 `let` 可以在类的方法和属性中进行访问; 但是，即使静态方法采用实例变量作为参数，也不能从静态方法访问这些字段。</span><span class="sxs-lookup"><span data-stu-id="18e7a-143">Fields that are created by `let` bindings can be accessed throughout the methods and properties of the class; however, they cannot be accessed from static methods, even if the static methods take an instance variable as a parameter.</span></span> <span data-ttu-id="18e7a-144">不能使用 self 标识符（如果存在）访问这些项。</span><span class="sxs-lookup"><span data-stu-id="18e7a-144">They cannot be accessed by using the self identifier, if one exists.</span></span>

## <a name="self-identifiers"></a><span data-ttu-id="18e7a-145">自我标识符</span><span class="sxs-lookup"><span data-stu-id="18e7a-145">Self Identifiers</span></span>

<span data-ttu-id="18e7a-146">*自我标识符* 是表示当前实例的名称。</span><span class="sxs-lookup"><span data-stu-id="18e7a-146">A *self identifier* is a name that represents the current instance.</span></span> <span data-ttu-id="18e7a-147">自标识符类似于 `this` c # 或 c + + 中的关键字或 `Me` Visual Basic。</span><span class="sxs-lookup"><span data-stu-id="18e7a-147">Self identifiers resemble the `this` keyword in C# or C++ or `Me` in Visual Basic.</span></span> <span data-ttu-id="18e7a-148">您可以通过两种不同的方式来定义自我标识符，具体情况取决于您是希望自标识符在整个类定义的范围内还是仅适用于单个方法。</span><span class="sxs-lookup"><span data-stu-id="18e7a-148">You can define a self identifier in two different ways, depending on whether you want the self identifier to be in scope for the whole class definition or just for an individual method.</span></span>

<span data-ttu-id="18e7a-149">若要为整个类定义自我标识符，请在 `as` 构造函数参数列表的右括号后使用关键字，并指定标识符名称。</span><span class="sxs-lookup"><span data-stu-id="18e7a-149">To define a self identifier for the whole class, use the `as` keyword after the closing parentheses of the constructor parameter list, and specify the identifier name.</span></span>

<span data-ttu-id="18e7a-150">若要仅为一个方法定义一个自标识符，请在成员声明中提供自标识符，就在方法名称和句点 (。 ) 作为分隔符。</span><span class="sxs-lookup"><span data-stu-id="18e7a-150">To define a self identifier for just one method, provide the self identifier in the member declaration, just before the method name and a period (.) as a separator.</span></span>

<span data-ttu-id="18e7a-151">下面的代码示例演示了创建自我标识符的两种方法。</span><span class="sxs-lookup"><span data-stu-id="18e7a-151">The following code example illustrates the two ways to create a self identifier.</span></span> <span data-ttu-id="18e7a-152">在第一行中， `as` 关键字用于定义自我标识符。</span><span class="sxs-lookup"><span data-stu-id="18e7a-152">In the first line, the `as` keyword is used to define the self identifier.</span></span> <span data-ttu-id="18e7a-153">在第五行，标识符 `this` 用于定义其作用域限制为方法的自定义标识符 `PrintMessage` 。</span><span class="sxs-lookup"><span data-stu-id="18e7a-153">In the fifth line, the identifier `this` is used to define a self identifier whose scope is restricted to the method `PrintMessage`.</span></span>

```fsharp
type MyClass2(dataIn) as self =
    let data = dataIn
    do
        self.PrintMessage()
    member this.PrintMessage() =
        printf "Creating MyClass2 with Data %d" data
```

<span data-ttu-id="18e7a-154">与其他 .NET 语言不同，你可以将自己的标识符命名为你所需的名称;你不能只限于、或之类的名称 `self` `Me` `this` 。</span><span class="sxs-lookup"><span data-stu-id="18e7a-154">Unlike in other .NET languages, you can name the self identifier however you want; you are not restricted to names such as `self`, `Me`, or `this`.</span></span>

<span data-ttu-id="18e7a-155">在基构造函数之后，才会初始化用关键字声明的 self 标识符 `as` 。</span><span class="sxs-lookup"><span data-stu-id="18e7a-155">The self identifier that is declared with the `as` keyword is not initialized until after the base constructor.</span></span> <span data-ttu-id="18e7a-156">因此，在基构造函数的前面或内部使用时， `System.InvalidOperationException: The initialization of an object or value resulted in an object or value being accessed recursively before it was fully initialized.` 将在运行时引发。</span><span class="sxs-lookup"><span data-stu-id="18e7a-156">Therefore, when used before or inside the base constructor, `System.InvalidOperationException: The initialization of an object or value resulted in an object or value being accessed recursively before it was fully initialized.` will be raised during runtime.</span></span> <span data-ttu-id="18e7a-157">在基构造函数之后（如绑定或绑定），可以自由地使用 self 标识符 `let` `do` 。</span><span class="sxs-lookup"><span data-stu-id="18e7a-157">You can use the self identifier freely after the base constructor, such as in `let` bindings or `do` bindings.</span></span>

## <a name="generic-type-parameters"></a><span data-ttu-id="18e7a-158">泛型类型参数</span><span class="sxs-lookup"><span data-stu-id="18e7a-158">Generic Type Parameters</span></span>

<span data-ttu-id="18e7a-159">泛型类型参数在尖括号中指定 (`<` 和 `>`) ，其形式为一个引号，后跟一个标识符。</span><span class="sxs-lookup"><span data-stu-id="18e7a-159">Generic type parameters are specified in angle brackets (`<` and `>`), in the form of a single quotation mark followed by an identifier.</span></span> <span data-ttu-id="18e7a-160">多个泛型类型参数由逗号分隔。</span><span class="sxs-lookup"><span data-stu-id="18e7a-160">Multiple generic type parameters are separated by commas.</span></span> <span data-ttu-id="18e7a-161">泛型类型参数在整个声明范围内。</span><span class="sxs-lookup"><span data-stu-id="18e7a-161">The generic type parameter is in scope throughout the declaration.</span></span> <span data-ttu-id="18e7a-162">下面的代码示例演示如何指定泛型类型参数。</span><span class="sxs-lookup"><span data-stu-id="18e7a-162">The following code example shows how to specify generic type parameters.</span></span>

[!code-fsharp[Main](~/samples/snippets/fsharp/lang-ref-1/snippet2403.fs)]

<span data-ttu-id="18e7a-163">当使用类型时，将推理类型参数。</span><span class="sxs-lookup"><span data-stu-id="18e7a-163">Type arguments are inferred when the type is used.</span></span> <span data-ttu-id="18e7a-164">在下面的代码中，推理出的类型是元组的序列。</span><span class="sxs-lookup"><span data-stu-id="18e7a-164">In the following code, the inferred type is a sequence of tuples.</span></span>

[!code-fsharp[Main](~/samples/snippets/fsharp/lang-ref-1/snippet24031.fs)]

## <a name="specifying-inheritance"></a><span data-ttu-id="18e7a-165">指定继承</span><span class="sxs-lookup"><span data-stu-id="18e7a-165">Specifying Inheritance</span></span>

<span data-ttu-id="18e7a-166">`inherit`子句标识直接基类（如果有）。</span><span class="sxs-lookup"><span data-stu-id="18e7a-166">The `inherit` clause identifies the direct base class, if there is one.</span></span> <span data-ttu-id="18e7a-167">在 F # 中，只允许一个直接基类。</span><span class="sxs-lookup"><span data-stu-id="18e7a-167">In F#, only one direct base class is allowed.</span></span> <span data-ttu-id="18e7a-168">类实现的接口不是基类。</span><span class="sxs-lookup"><span data-stu-id="18e7a-168">Interfaces that a class implements are not considered base classes.</span></span> <span data-ttu-id="18e7a-169">[接口主题中](Interfaces.md)讨论了接口。</span><span class="sxs-lookup"><span data-stu-id="18e7a-169">Interfaces are discussed in the [Interfaces](Interfaces.md) topic.</span></span>

<span data-ttu-id="18e7a-170">可以通过使用 language 关键字作为标识符来访问派生类中的基类的方法和属性 `base` ，后跟一个句点 (。 ) 和成员的名称。</span><span class="sxs-lookup"><span data-stu-id="18e7a-170">You can access the methods and properties of the base class from the derived class by using the language keyword `base` as an identifier, followed by a period (.) and the name of the member.</span></span>

<span data-ttu-id="18e7a-171">有关详细信息，请参阅[继承](inheritance.md)。</span><span class="sxs-lookup"><span data-stu-id="18e7a-171">For more information, see [Inheritance](inheritance.md).</span></span>

## <a name="members-section"></a><span data-ttu-id="18e7a-172">成员部分</span><span class="sxs-lookup"><span data-stu-id="18e7a-172">Members Section</span></span>

<span data-ttu-id="18e7a-173">您可以在此部分中定义静态方法、属性、接口实现、抽象成员、事件声明和其他构造函数。</span><span class="sxs-lookup"><span data-stu-id="18e7a-173">You can define static or instance methods, properties, interface implementations, abstract members, event declarations, and additional constructors in this section.</span></span> <span data-ttu-id="18e7a-174">此部分中不能出现 Let 和 do 绑定。</span><span class="sxs-lookup"><span data-stu-id="18e7a-174">Let and do bindings cannot appear in this section.</span></span> <span data-ttu-id="18e7a-175">由于除类外，成员还可以添加到各种 F # 类型，因此，它们将在单独的主题 [成员](./members/index.md)中进行讨论。</span><span class="sxs-lookup"><span data-stu-id="18e7a-175">Because members can be added to a variety of F# types in addition to classes, they are discussed in a separate topic, [Members](./members/index.md).</span></span>

## <a name="mutually-recursive-types"></a><span data-ttu-id="18e7a-176">相互递归类型</span><span class="sxs-lookup"><span data-stu-id="18e7a-176">Mutually Recursive Types</span></span>

<span data-ttu-id="18e7a-177">如果以循环方式定义彼此引用的类型，则可以使用关键字将类型定义组合在一起 `and` 。</span><span class="sxs-lookup"><span data-stu-id="18e7a-177">When you define types that reference each other in a circular way, you string together the type definitions by using the `and` keyword.</span></span> <span data-ttu-id="18e7a-178">`and`关键字替换 `type` 除第一个定义外的所有关键字，如下所示。</span><span class="sxs-lookup"><span data-stu-id="18e7a-178">The `and` keyword replaces the `type` keyword on all except the first definition, as follows.</span></span>

[!code-fsharp[Main](~/samples/snippets/fsharp/lang-ref-1/snippet2404.fs)]

<span data-ttu-id="18e7a-179">输出为当前目录中的所有文件的列表。</span><span class="sxs-lookup"><span data-stu-id="18e7a-179">The output is a list of all the files in the current directory.</span></span>

## <a name="when-to-use-classes-unions-records-and-structures"></a><span data-ttu-id="18e7a-180">何时使用类、联合、记录和结构</span><span class="sxs-lookup"><span data-stu-id="18e7a-180">When to Use Classes, Unions, Records, and Structures</span></span>

<span data-ttu-id="18e7a-181">由于要选择各种类型，您需要充分了解每种类型的设计目的，以便为特定情况选择适当的类型。</span><span class="sxs-lookup"><span data-stu-id="18e7a-181">Given the variety of types to choose from, you need to have a good understanding of what each type is designed for to select the appropriate type for a particular situation.</span></span> <span data-ttu-id="18e7a-182">类设计用于面向对象的编程上下文。</span><span class="sxs-lookup"><span data-stu-id="18e7a-182">Classes are designed for use in object-oriented programming contexts.</span></span> <span data-ttu-id="18e7a-183">面向对象的编程是在为 .NET Framework 编写的应用程序中使用的主要范例。</span><span class="sxs-lookup"><span data-stu-id="18e7a-183">Object-oriented programming is the dominant paradigm used in applications that are written for the .NET Framework.</span></span> <span data-ttu-id="18e7a-184">如果 F # 代码必须与 .NET Framework 或其他面向对象的库密切合作，尤其是在需要从面向对象的类型系统（如 UI 库）中进行扩展时，类可能是合适的。</span><span class="sxs-lookup"><span data-stu-id="18e7a-184">If your F# code has to work closely with the .NET Framework or another object-oriented library, and especially if you have to extend from an object-oriented type system such as a UI library, classes are probably appropriate.</span></span>

<span data-ttu-id="18e7a-185">如果你不与面向对象的代码密切互操作，或者如果你正在编写自包含的代码，从而保护其不受面向对象代码的频繁交互，则应考虑使用记录和可区分联合。</span><span class="sxs-lookup"><span data-stu-id="18e7a-185">If you are not interoperating closely with object-oriented code, or if you are writing code that is self-contained and therefore protected from frequent interaction with object-oriented code, you should consider using records and discriminated unions.</span></span> <span data-ttu-id="18e7a-186">与相应的模式匹配代码一起使用的一种非常好的方法是，通常可以将其用作对象层次结构的更简单的替代方法。</span><span class="sxs-lookup"><span data-stu-id="18e7a-186">A single, well thought–out discriminated union, together with appropriate pattern matching code, can often be used as a simpler alternative to an object hierarchy.</span></span> <span data-ttu-id="18e7a-187">有关可区分联合的详细信息，请参阅可 [区分联合](discriminated-unions.md)。</span><span class="sxs-lookup"><span data-stu-id="18e7a-187">For more information about discriminated unions, see [Discriminated Unions](discriminated-unions.md).</span></span>

<span data-ttu-id="18e7a-188">记录的优点是比类简单，但当类型的需求超过了可通过其简易性实现的需求时，记录不适当。</span><span class="sxs-lookup"><span data-stu-id="18e7a-188">Records have the advantage of being simpler than classes, but records are not appropriate when the demands of a type exceed what can be accomplished with their simplicity.</span></span> <span data-ttu-id="18e7a-189">记录基本上是值的简单聚合，无需单独的构造函数来执行自定义操作，无需隐藏字段，并且无需继承或接口实现。</span><span class="sxs-lookup"><span data-stu-id="18e7a-189">Records are basically simple aggregates of values, without separate constructors that can perform custom actions, without hidden fields, and without inheritance or interface implementations.</span></span> <span data-ttu-id="18e7a-190">尽管可以将属性和方法等成员添加到记录中以使它们的行为更加复杂，但存储在记录中的字段仍是值的简单聚合。</span><span class="sxs-lookup"><span data-stu-id="18e7a-190">Although members such as properties and methods can be added to records to make their behavior more complex, the fields stored in a record are still a simple aggregate of values.</span></span> <span data-ttu-id="18e7a-191">有关记录的详细信息，请参阅 [记录](records.md)。</span><span class="sxs-lookup"><span data-stu-id="18e7a-191">For more information about records, see [Records](records.md).</span></span>

<span data-ttu-id="18e7a-192">对于少量的数据聚合，结构也很有用，但它们不同于类和记录，因为它们是 .NET 值类型。</span><span class="sxs-lookup"><span data-stu-id="18e7a-192">Structures are also useful for small aggregates of data, but they differ from classes and records in that they are .NET value types.</span></span> <span data-ttu-id="18e7a-193">类和记录是 .NET 引用类型。</span><span class="sxs-lookup"><span data-stu-id="18e7a-193">Classes and records are .NET reference types.</span></span> <span data-ttu-id="18e7a-194">值类型和引用类型的语义不同于值类型通过值传递。</span><span class="sxs-lookup"><span data-stu-id="18e7a-194">The semantics of value types and reference types are different in that value types are passed by value.</span></span> <span data-ttu-id="18e7a-195">这意味着，在将它们作为参数传递或从函数返回时，它们将被复制到位。</span><span class="sxs-lookup"><span data-stu-id="18e7a-195">This means that they are copied bit for bit when they are passed as a parameter or returned from a function.</span></span> <span data-ttu-id="18e7a-196">它们还存储在堆栈上，或者，如果用作字段，则嵌入到父对象中，而不是存储在堆上各自不同的位置。</span><span class="sxs-lookup"><span data-stu-id="18e7a-196">They are also stored on the stack or, if they are used as a field, embedded inside the parent object instead of stored in their own separate location on the heap.</span></span> <span data-ttu-id="18e7a-197">因此，当访问堆的开销是一个问题时，结构适用于经常访问的数据。</span><span class="sxs-lookup"><span data-stu-id="18e7a-197">Therefore, structures are appropriate for frequently accessed data when the overhead of accessing the heap is a problem.</span></span> <span data-ttu-id="18e7a-198">有关结构的详细信息，请参阅 [结构](structures.md)。</span><span class="sxs-lookup"><span data-stu-id="18e7a-198">For more information about structures, see [Structures](structures.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="18e7a-199">另请参阅</span><span class="sxs-lookup"><span data-stu-id="18e7a-199">See also</span></span>

- [<span data-ttu-id="18e7a-200">F# 语言参考</span><span class="sxs-lookup"><span data-stu-id="18e7a-200">F# Language Reference</span></span>](index.md)
- [<span data-ttu-id="18e7a-201">成员</span><span class="sxs-lookup"><span data-stu-id="18e7a-201">Members</span></span>](./members/index.md)
- [<span data-ttu-id="18e7a-202">继承</span><span class="sxs-lookup"><span data-stu-id="18e7a-202">Inheritance</span></span>](inheritance.md)
- [<span data-ttu-id="18e7a-203">接口</span><span class="sxs-lookup"><span data-stu-id="18e7a-203">Interfaces</span></span>](interfaces.md)
