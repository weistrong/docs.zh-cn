---
title: 类型扩展
description: '了解 F # 类型扩展如何允许您向以前定义的对象类型添加新成员。'
ms.date: 02/05/2020
ms.openlocfilehash: c9adddb3133a4af57a12be0b09c22954a8bff6a7
ms.sourcegitcommit: c3093e9d106d8ca87cc86eef1f2ae4ecfb392118
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/22/2020
ms.locfileid: "97737263"
---
# <a name="type-extensions"></a><span data-ttu-id="10429-103">类型扩展</span><span class="sxs-lookup"><span data-stu-id="10429-103">Type extensions</span></span>

<span data-ttu-id="10429-104">类型扩展 (也称为 _扩大_) 是一系列功能，可让你向之前定义的对象类型添加新成员。</span><span class="sxs-lookup"><span data-stu-id="10429-104">Type extensions (also called _augmentations_) are a family of features that let you add new members to a previously defined object type.</span></span> <span data-ttu-id="10429-105">这三种功能包括：</span><span class="sxs-lookup"><span data-stu-id="10429-105">The three features are:</span></span>

- <span data-ttu-id="10429-106">内部类型扩展</span><span class="sxs-lookup"><span data-stu-id="10429-106">Intrinsic type extensions</span></span>
- <span data-ttu-id="10429-107">可选类型扩展</span><span class="sxs-lookup"><span data-stu-id="10429-107">Optional type extensions</span></span>
- <span data-ttu-id="10429-108">扩展方法</span><span class="sxs-lookup"><span data-stu-id="10429-108">Extension methods</span></span>

<span data-ttu-id="10429-109">每个可以在不同的方案中使用，并且具有不同的折衷。</span><span class="sxs-lookup"><span data-stu-id="10429-109">Each can be used in different scenarios and has different tradeoffs.</span></span>

## <a name="syntax"></a><span data-ttu-id="10429-110">语法</span><span class="sxs-lookup"><span data-stu-id="10429-110">Syntax</span></span>

```fsharp
// Intrinsic and optional extensions
type typename with
    member self-identifier.member-name =
        body
    ...

// Extension methods
open System.Runtime.CompilerServices

[<Extension>]
type Extensions() =
    [<Extension>]
    static member extension-name (ty: typename, [args]) =
        body
    ...
```

## <a name="intrinsic-type-extensions"></a><span data-ttu-id="10429-111">内部类型扩展</span><span class="sxs-lookup"><span data-stu-id="10429-111">Intrinsic type extensions</span></span>

<span data-ttu-id="10429-112">内部类型扩展是扩展用户定义类型的类型扩展。</span><span class="sxs-lookup"><span data-stu-id="10429-112">An intrinsic type extension is a type extension that extends a user-defined type.</span></span>

<span data-ttu-id="10429-113">内部类型扩展必须在同一文件中定义 **，并** 在与它们所扩展的类型相同的命名空间或模块中定义。</span><span class="sxs-lookup"><span data-stu-id="10429-113">Intrinsic type extensions must be defined in the same file **and** in the same namespace or module as the type they're extending.</span></span> <span data-ttu-id="10429-114">任何其他定义都将导致其成为 [可选类型扩展](type-extensions.md#optional-type-extensions)。</span><span class="sxs-lookup"><span data-stu-id="10429-114">Any other definition will result in them being [optional type extensions](type-extensions.md#optional-type-extensions).</span></span>

<span data-ttu-id="10429-115">内部类型扩展有时是将功能与类型声明分开的更清晰的方式。</span><span class="sxs-lookup"><span data-stu-id="10429-115">Intrinsic type extensions are sometimes a cleaner way to separate functionality from the type declaration.</span></span> <span data-ttu-id="10429-116">下面的示例演示如何定义内部类型扩展：</span><span class="sxs-lookup"><span data-stu-id="10429-116">The following example shows how to define an intrinsic type extension:</span></span>

```fsharp
namespace Example

type Variant =
    | Num of int
    | Str of string
  
module Variant =
    let print v =
        match v with
        | Num n -> printf "Num %d" n
        | Str s -> printf "Str %s" s

// Add a member to Variant as an extension
type Variant with
    member x.Print() = Variant.print x
```

<span data-ttu-id="10429-117">使用类型扩展可以分隔以下各项：</span><span class="sxs-lookup"><span data-stu-id="10429-117">Using a type extension allows you to separate each of the following:</span></span>

- <span data-ttu-id="10429-118">类型的声明 `Variant`</span><span class="sxs-lookup"><span data-stu-id="10429-118">The declaration of a `Variant` type</span></span>
- <span data-ttu-id="10429-119">`Variant`根据类的 "形状" 打印类的功能</span><span class="sxs-lookup"><span data-stu-id="10429-119">Functionality to print the `Variant` class depending on its "shape"</span></span>
- <span data-ttu-id="10429-120">使用对象样式表示法访问打印功能的一种方法 `.`</span><span class="sxs-lookup"><span data-stu-id="10429-120">A way to access the printing functionality with object-style `.`-notation</span></span>

<span data-ttu-id="10429-121">这是将所有内容定义为成员的替代方法 `Variant` 。</span><span class="sxs-lookup"><span data-stu-id="10429-121">This is an alternative to defining everything as a member on `Variant`.</span></span> <span data-ttu-id="10429-122">尽管它不是原本更好的方法，但在某些情况下，它可能是功能的更清晰表示形式。</span><span class="sxs-lookup"><span data-stu-id="10429-122">Although it is not an inherently better approach, it can be a cleaner representation of functionality in some situations.</span></span>

<span data-ttu-id="10429-123">内部类型扩展将编译为它们增加的类型的成员，并在反射检查类型时在类型上显示。</span><span class="sxs-lookup"><span data-stu-id="10429-123">Intrinsic type extensions are compiled as members of the type they augment, and appear on the type when the type is examined by reflection.</span></span>

## <a name="optional-type-extensions"></a><span data-ttu-id="10429-124">可选类型扩展</span><span class="sxs-lookup"><span data-stu-id="10429-124">Optional type extensions</span></span>

<span data-ttu-id="10429-125">可选类型扩展是在要扩展的类型的原始模块、命名空间或程序集的外部显示的扩展。</span><span class="sxs-lookup"><span data-stu-id="10429-125">An optional type extension is an extension that appears outside the original module, namespace, or assembly of the type being extended.</span></span>

<span data-ttu-id="10429-126">可选类型扩展对于扩展你自己尚未定义的类型很有用。</span><span class="sxs-lookup"><span data-stu-id="10429-126">Optional type extensions are useful for extending a type that you have not defined yourself.</span></span> <span data-ttu-id="10429-127">例如：</span><span class="sxs-lookup"><span data-stu-id="10429-127">For example:</span></span>

```fsharp
module Extensions

type IEnumerable<'T> with
    /// Repeat each element of the sequence n times
    member xs.RepeatElements(n: int) =
        seq {
            for x in xs do
                for _ in 1 .. n -> x
        }
```

<span data-ttu-id="10429-128">你现在可以访问，就像它是的成员，只要 `RepeatElements` <xref:System.Collections.Generic.IEnumerable%601> `Extensions` 模块是在你所使用的范围中打开的。</span><span class="sxs-lookup"><span data-stu-id="10429-128">You can now access `RepeatElements` as if it's a member of <xref:System.Collections.Generic.IEnumerable%601> as long as the `Extensions` module is opened in the scope that you are working in.</span></span>

<span data-ttu-id="10429-129">可选扩展在由反射检查时不会出现在扩展类型上。</span><span class="sxs-lookup"><span data-stu-id="10429-129">Optional extensions do not appear on the extended type when examined by reflection.</span></span> <span data-ttu-id="10429-130">可选扩展必须在模块中，且仅当包含该扩展的模块处于打开状态或处于范围内时，它们才在范围内。</span><span class="sxs-lookup"><span data-stu-id="10429-130">Optional extensions must be in modules, and they're only in scope when the module that contains the extension is open or is otherwise in scope.</span></span>

<span data-ttu-id="10429-131">可选扩展成员将编译为静态成员，其对象实例将被隐式传递为第一个参数。</span><span class="sxs-lookup"><span data-stu-id="10429-131">Optional extension members are compiled to static members for which the object instance is passed implicitly as the first parameter.</span></span> <span data-ttu-id="10429-132">但是，它们的作用就像是实例成员或静态成员的声明方式。</span><span class="sxs-lookup"><span data-stu-id="10429-132">However, they act as if they're instance members or static members according to how they're declared.</span></span>

<span data-ttu-id="10429-133">可选扩展成员也不适用于 c # 或 Visual Basic 使用者。</span><span class="sxs-lookup"><span data-stu-id="10429-133">Optional extension members are also not visible to C# or Visual Basic consumers.</span></span> <span data-ttu-id="10429-134">它们只能在其他 F # 代码中使用。</span><span class="sxs-lookup"><span data-stu-id="10429-134">They can only be consumed in other F# code.</span></span>

## <a name="generic-limitation-of-intrinsic-and-optional-type-extensions"></a><span data-ttu-id="10429-135">内部和可选类型扩展的泛型限制</span><span class="sxs-lookup"><span data-stu-id="10429-135">Generic limitation of intrinsic and optional type extensions</span></span>

<span data-ttu-id="10429-136">可以在类型变量受到约束的泛型类型上声明类型扩展。</span><span class="sxs-lookup"><span data-stu-id="10429-136">It's possible to declare a type extension on a generic type where the type variable is constrained.</span></span> <span data-ttu-id="10429-137">要求是扩展声明的约束与声明类型的约束匹配。</span><span class="sxs-lookup"><span data-stu-id="10429-137">The requirement is that the constraint of the extension declaration matches the constraint of the declared type.</span></span>

<span data-ttu-id="10429-138">但是，即使在声明的类型和类型扩展之间进行了匹配，约束仍有可能由扩展成员的主体推断，该扩展成员在类型参数上施加不同于声明类型的要求。</span><span class="sxs-lookup"><span data-stu-id="10429-138">However, even when constraints are matched between a declared type and a type extension, it's possible for a constraint to be inferred by the body of an extended member that imposes a different requirement on the type parameter than the declared type.</span></span> <span data-ttu-id="10429-139">例如：</span><span class="sxs-lookup"><span data-stu-id="10429-139">For example:</span></span>

```fsharp
open System.Collections.Generic

// NOT POSSIBLE AND FAILS TO COMPILE!
//
// The member 'Sum' has a different requirement on 'T than the type IEnumerable<'T>
type IEnumerable<'T> with
    member this.Sum() = Seq.sum this
```

<span data-ttu-id="10429-140">无法获取此代码以使用可选类型扩展：</span><span class="sxs-lookup"><span data-stu-id="10429-140">There is no way to get this code to work with an optional type extension:</span></span>

- <span data-ttu-id="10429-141">同样， `Sum` 成员对 `'T` (`static member get_Zero` 和) 具有不同 `static member (+)` 于类型扩展所定义的约束。</span><span class="sxs-lookup"><span data-stu-id="10429-141">As is, the `Sum` member has a different constraint on `'T` (`static member get_Zero` and `static member (+)`) than what the type extension defines.</span></span>
- <span data-ttu-id="10429-142">修改类型扩展以使相同的约束不再 `Sum` 与中定义的约束匹配 `IEnumerable<'T>` 。</span><span class="sxs-lookup"><span data-stu-id="10429-142">Modifying the type extension to have the same constraint as `Sum` will no longer match the defined constraint on `IEnumerable<'T>`.</span></span>
- <span data-ttu-id="10429-143">更改 `member this.Sum` 为 `member inline this.Sum` 将发出错误，指出类型约束不匹配。</span><span class="sxs-lookup"><span data-stu-id="10429-143">Changing `member this.Sum` to `member inline this.Sum` will give an error that type constraints are mismatched.</span></span>

<span data-ttu-id="10429-144">所需的是 "在空间中浮动" 的静态方法，并可以显示为扩展类型。</span><span class="sxs-lookup"><span data-stu-id="10429-144">What is desired are static methods that "float in space" and can be presented as if they're extending a type.</span></span> <span data-ttu-id="10429-145">这就是需要扩展方法的地方。</span><span class="sxs-lookup"><span data-stu-id="10429-145">This is where extension methods become necessary.</span></span>

## <a name="extension-methods"></a><span data-ttu-id="10429-146">扩展方法</span><span class="sxs-lookup"><span data-stu-id="10429-146">Extension methods</span></span>

<span data-ttu-id="10429-147">最后，扩展方法 (有时称为 "c # 样式扩展成员" ) 可在 F # 中声明为类上的静态成员方法。</span><span class="sxs-lookup"><span data-stu-id="10429-147">Finally, extension methods (sometimes called "C# style extension members") can be declared in F# as a static member method on a class.</span></span>

<span data-ttu-id="10429-148">当您希望在将约束类型变量的泛型类型上定义扩展时，扩展方法非常有用。</span><span class="sxs-lookup"><span data-stu-id="10429-148">Extension methods are useful for when you wish to define extensions on a generic type that will constrain the type variable.</span></span> <span data-ttu-id="10429-149">例如：</span><span class="sxs-lookup"><span data-stu-id="10429-149">For example:</span></span>

```fsharp
namespace Extensions

open System.Collections.Generic
open System.Runtime.CompilerServices

[<Extension>]
type IEnumerableExtensions =
    [<Extension>]
    static member inline Sum(xs: IEnumerable<'T>) = Seq.sum xs
```

<span data-ttu-id="10429-150">使用时，此代码将使其看起来像 `Sum` 是在上定义的 <xref:System.Collections.Generic.IEnumerable%601> ，只要 `Extensions` 打开或在范围内。</span><span class="sxs-lookup"><span data-stu-id="10429-150">When used, this code will make it appear as if `Sum` is defined on <xref:System.Collections.Generic.IEnumerable%601>, so long as `Extensions` has been opened or is in scope.</span></span>

<span data-ttu-id="10429-151">为了使扩展可用于 VB.NET 代码，在 `ExtensionAttribute` 程序集级别需要额外的内容：</span><span class="sxs-lookup"><span data-stu-id="10429-151">For the extension to be available to VB.NET code, an extra `ExtensionAttribute` is required at the assembly level:</span></span>

```fsharp
module AssemblyInfo
open System.Runtime.CompilerServices
[<assembly:Extension>]
do ()
```

## <a name="other-remarks"></a><span data-ttu-id="10429-152">其他备注</span><span class="sxs-lookup"><span data-stu-id="10429-152">Other remarks</span></span>

<span data-ttu-id="10429-153">类型扩展还具有以下属性：</span><span class="sxs-lookup"><span data-stu-id="10429-153">Type extensions also have the following attributes:</span></span>

- <span data-ttu-id="10429-154">可访问的任何类型都可以进行扩展。</span><span class="sxs-lookup"><span data-stu-id="10429-154">Any type that can be accessed can be extended.</span></span>
- <span data-ttu-id="10429-155">内部和可选类型扩展可以定义 _任何_ 成员类型，而不仅仅是方法。</span><span class="sxs-lookup"><span data-stu-id="10429-155">Intrinsic and optional type extensions can define _any_ member type, not just methods.</span></span> <span data-ttu-id="10429-156">例如，也可以扩展属性。</span><span class="sxs-lookup"><span data-stu-id="10429-156">So extension properties are also possible, for example.</span></span>
- <span data-ttu-id="10429-157">`self-identifier`[语法](type-extensions.md#syntax)中的标记表示正在调用的类型的实例，就像普通成员一样。</span><span class="sxs-lookup"><span data-stu-id="10429-157">The `self-identifier` token in the [syntax](type-extensions.md#syntax) represents the instance of the type being invoked, just like ordinary members.</span></span>
- <span data-ttu-id="10429-158">扩展成员可以是静态成员或实例成员。</span><span class="sxs-lookup"><span data-stu-id="10429-158">Extended members can be static or instance members.</span></span>
- <span data-ttu-id="10429-159">类型扩展上的类型变量必须与声明类型的约束匹配。</span><span class="sxs-lookup"><span data-stu-id="10429-159">Type variables on a type extension must match the constraints of the declared type.</span></span>

<span data-ttu-id="10429-160">对于类型扩展也存在以下限制：</span><span class="sxs-lookup"><span data-stu-id="10429-160">The following limitations also exist for type extensions:</span></span>

- <span data-ttu-id="10429-161">类型扩展不支持虚拟或抽象方法。</span><span class="sxs-lookup"><span data-stu-id="10429-161">Type extensions do not support virtual or abstract methods.</span></span>
- <span data-ttu-id="10429-162">类型扩展不支持作为扩大的重写方法。</span><span class="sxs-lookup"><span data-stu-id="10429-162">Type extensions do not support override methods as augmentations.</span></span>
- <span data-ttu-id="10429-163">类型扩展不支持 [静态解析的类型参数](./generics/statically-resolved-type-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="10429-163">Type extensions do not support [Statically Resolved Type Parameters](./generics/statically-resolved-type-parameters.md).</span></span>
- <span data-ttu-id="10429-164">可选类型扩展不支持作为扩大的构造函数。</span><span class="sxs-lookup"><span data-stu-id="10429-164">Optional Type extensions do not support constructors as augmentations.</span></span>
- <span data-ttu-id="10429-165">不能对 [类型缩写](type-abbreviations.md)定义类型扩展。</span><span class="sxs-lookup"><span data-stu-id="10429-165">Type extensions cannot be defined on [type abbreviations](type-abbreviations.md).</span></span>
- <span data-ttu-id="10429-166">类型扩展对于 (无效， `byref<'T>` 但它们可以) 声明。</span><span class="sxs-lookup"><span data-stu-id="10429-166">Type extensions are not valid for `byref<'T>` (though they can be declared).</span></span>
- <span data-ttu-id="10429-167">类型扩展对于特性 (无效，但它们可以) 声明。</span><span class="sxs-lookup"><span data-stu-id="10429-167">Type extensions are not valid for attributes (though they can be declared).</span></span>
- <span data-ttu-id="10429-168">你可以定义重载同名的其他方法的扩展，但 F # 编译器会在出现不明确的调用时为非扩展方法提供首选项。</span><span class="sxs-lookup"><span data-stu-id="10429-168">You can define extensions that overload other methods of the same name, but the F# compiler gives preference to non-extension methods if there is an ambiguous call.</span></span>

<span data-ttu-id="10429-169">最后，如果一种类型存在多个内部类型扩展，则所有成员都必须是唯一的。</span><span class="sxs-lookup"><span data-stu-id="10429-169">Finally, if multiple intrinsic type extensions exist for one type, all members must be unique.</span></span> <span data-ttu-id="10429-170">对于可选类型扩展，不同类型扩展中具有相同类型的成员可以具有相同的名称。</span><span class="sxs-lookup"><span data-stu-id="10429-170">For optional type extensions, members in different type extensions to the same type can have the same names.</span></span> <span data-ttu-id="10429-171">仅当客户端代码打开两个不同的作用域定义相同的成员名称时，才会发生多义性错误。</span><span class="sxs-lookup"><span data-stu-id="10429-171">Ambiguity errors occur only if client code opens two different scopes that define the same member names.</span></span>

## <a name="see-also"></a><span data-ttu-id="10429-172">另请参阅</span><span class="sxs-lookup"><span data-stu-id="10429-172">See also</span></span>

- [<span data-ttu-id="10429-173">F# 语言参考</span><span class="sxs-lookup"><span data-stu-id="10429-173">F# Language Reference</span></span>](index.md)
- [<span data-ttu-id="10429-174">成员</span><span class="sxs-lookup"><span data-stu-id="10429-174">Members</span></span>](./members/index.md)
