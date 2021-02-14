---
description: '了解详细信息：扩展方法 (Visual Basic) '
title: 扩展方法
ms.date: 07/20/2015
f1_keywords:
- vb.ExtensionMethods
helpviewer_keywords:
- extending data types [Visual Basic]
- extension methods [Visual Basic]
ms.assetid: b8020aae-374d-46a9-bcb7-8cc2390b93b6
ms.openlocfilehash: 5a1482502b144524c0be90e1c83a38f49b4a4d26
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100434350"
---
# <a name="extension-methods-visual-basic"></a><span data-ttu-id="83069-103">扩展方法 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="83069-103">Extension Methods (Visual Basic)</span></span>

<span data-ttu-id="83069-104">通过扩展方法，开发人员可以向已定义的数据类型添加自定义功能，而无需创建新的派生类型。</span><span class="sxs-lookup"><span data-stu-id="83069-104">Extension methods enable developers to add custom functionality to data types that are already defined without creating a new derived type.</span></span> <span data-ttu-id="83069-105">通过扩展方法，可以编写一个方法，该方法可以像调用现有类型的实例方法一样进行调用。</span><span class="sxs-lookup"><span data-stu-id="83069-105">Extension methods make it possible to write a method that can be called as if it were an instance method of the existing type.</span></span>

## <a name="remarks"></a><span data-ttu-id="83069-106">备注</span><span class="sxs-lookup"><span data-stu-id="83069-106">Remarks</span></span>

<span data-ttu-id="83069-107">扩展方法只能是 `Sub` 过程或 `Function` 过程。</span><span class="sxs-lookup"><span data-stu-id="83069-107">An extension method can be only a `Sub` procedure or a `Function` procedure.</span></span> <span data-ttu-id="83069-108">不能定义扩展属性、字段或事件。</span><span class="sxs-lookup"><span data-stu-id="83069-108">You cannot define an extension property, field, or event.</span></span> <span data-ttu-id="83069-109">所有扩展方法都必须使用命名空间中的扩展属性进行标记 `<Extension>` <xref:System.Runtime.CompilerServices?displayProperty=nameWithType> ，且必须在 [模块](../../../language-reference/statements/module-statement.md)中定义。</span><span class="sxs-lookup"><span data-stu-id="83069-109">All extension methods must be marked with the extension attribute `<Extension>` from the <xref:System.Runtime.CompilerServices?displayProperty=nameWithType> namespace and must be defined in a [Module](../../../language-reference/statements/module-statement.md).</span></span> <span data-ttu-id="83069-110">如果在模块之外定义扩展方法，则 Visual Basic 编译器将生成错误 [BC36551](../../../misc/bc36551.md)"只能在模块中定义扩展方法"。</span><span class="sxs-lookup"><span data-stu-id="83069-110">If an extension method is defined outside a module, the Visual Basic compiler generates error [BC36551](../../../misc/bc36551.md), "Extension methods can be defined only in modules".</span></span>

<span data-ttu-id="83069-111">扩展方法定义中的第一个参数指定该方法扩展的数据类型。</span><span class="sxs-lookup"><span data-stu-id="83069-111">The first parameter in an extension method definition specifies which data type the method extends.</span></span> <span data-ttu-id="83069-112">当方法运行时，第一个参数绑定到调用方法的数据类型的实例。</span><span class="sxs-lookup"><span data-stu-id="83069-112">When the method is run, the first parameter is bound to the instance of the data type that invokes the method.</span></span>

<span data-ttu-id="83069-113">`Extension`特性只能应用于 Visual Basic [`Module`](../../../language-reference/statements/module-statement.md) 、 [`Sub`](../../../language-reference/statements/sub-statement.md) 或 [`Function`](../../../language-reference/statements/function-statement.md) 。</span><span class="sxs-lookup"><span data-stu-id="83069-113">The `Extension` attribute can only be applied to a Visual Basic [`Module`](../../../language-reference/statements/module-statement.md), [`Sub`](../../../language-reference/statements/sub-statement.md), or [`Function`](../../../language-reference/statements/function-statement.md).</span></span> <span data-ttu-id="83069-114">如果将它应用于 `Class` 或 `Structure` ，则 Visual Basic 编译器将生成错误 [BC36550](../../../language-reference/error-messages/extension-attribute-can-be-applied-only-to-module-sub-or-function-declarations.md)，"Extension" 特性只能应用于 "Module"、"Sub" 或 "Function" 声明。</span><span class="sxs-lookup"><span data-stu-id="83069-114">If you apply it to a `Class` or a `Structure`, the Visual Basic compiler generates error [BC36550](../../../language-reference/error-messages/extension-attribute-can-be-applied-only-to-module-sub-or-function-declarations.md), "'Extension' attribute can be applied only to 'Module', 'Sub', or 'Function' declarations".</span></span>

## <a name="example"></a><span data-ttu-id="83069-115">示例</span><span class="sxs-lookup"><span data-stu-id="83069-115">Example</span></span>

<span data-ttu-id="83069-116">下面的示例定义了 `Print` <xref:System.String> 数据类型的扩展。</span><span class="sxs-lookup"><span data-stu-id="83069-116">The following example defines a `Print` extension to the <xref:System.String> data type.</span></span> <span data-ttu-id="83069-117">方法使用 `Console.WriteLine` 显示字符串。</span><span class="sxs-lookup"><span data-stu-id="83069-117">The method uses `Console.WriteLine` to display a string.</span></span> <span data-ttu-id="83069-118">方法的参数 `Print` `aString` 确定方法扩展 <xref:System.String> 类。</span><span class="sxs-lookup"><span data-stu-id="83069-118">The parameter of the `Print` method, `aString`, establishes that the method extends the <xref:System.String> class.</span></span>

[!code-vb[VbVbalrExtensionMethods#1](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrExtensionMethods/VB/StringExtensions.vb#1)]

<span data-ttu-id="83069-119">请注意，扩展方法定义标记有扩展属性 `<Extension()>` 。</span><span class="sxs-lookup"><span data-stu-id="83069-119">Notice that the extension method definition is marked with the extension attribute `<Extension()>`.</span></span> <span data-ttu-id="83069-120">标记定义方法的模块是可选的，但必须标记每个扩展方法。</span><span class="sxs-lookup"><span data-stu-id="83069-120">Marking the module in which the method is defined is optional, but each extension method must be marked.</span></span> <span data-ttu-id="83069-121"><xref:System.Runtime.CompilerServices> 必须导入才能访问扩展属性。</span><span class="sxs-lookup"><span data-stu-id="83069-121"><xref:System.Runtime.CompilerServices> must be imported in order to access the extension attribute.</span></span>

<span data-ttu-id="83069-122">扩展方法只能在模块中声明。</span><span class="sxs-lookup"><span data-stu-id="83069-122">Extension methods can be declared only within modules.</span></span> <span data-ttu-id="83069-123">通常，在其中定义扩展方法的模块与在其中调用扩展方法的模块不同。</span><span class="sxs-lookup"><span data-stu-id="83069-123">Typically, the module in which an extension method is defined is not the same module as the one in which it is called.</span></span> <span data-ttu-id="83069-124">如果需要，将导入包含扩展方法的模块，使其进入范围。</span><span class="sxs-lookup"><span data-stu-id="83069-124">Instead, the module that contains the extension method is imported, if it needs to be, to bring it into scope.</span></span> <span data-ttu-id="83069-125">在包含的模块位于 `Print` 范围内后，可以调用方法，就像它是一个不采用任何参数的普通实例方法，例如 `ToUpper` ：</span><span class="sxs-lookup"><span data-stu-id="83069-125">After the module that contains `Print` is in scope, the method can be called as if it were an ordinary instance method that takes no arguments, such as `ToUpper`:</span></span>

[!code-vb[VbVbalrExtensionMethods#2](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrExtensionMethods/VB/Class1.vb#2)]

<span data-ttu-id="83069-126">下一个示例（ `PrintAndPunctuate` ）也是对的扩展 <xref:System.String> ，这一次使用两个参数定义。</span><span class="sxs-lookup"><span data-stu-id="83069-126">The next example, `PrintAndPunctuate`, is also an extension to <xref:System.String>, this time defined with two parameters.</span></span> <span data-ttu-id="83069-127">第一个参数 `aString` 确定扩展方法扩展 <xref:System.String> 。</span><span class="sxs-lookup"><span data-stu-id="83069-127">The first parameter, `aString`, establishes that the extension method extends <xref:System.String>.</span></span> <span data-ttu-id="83069-128">第二个参数将是 `punc` 一串标点符号，在调用方法时作为参数传入。</span><span class="sxs-lookup"><span data-stu-id="83069-128">The second parameter, `punc`, is intended to be a string of punctuation marks that is passed in as an argument when the method is called.</span></span> <span data-ttu-id="83069-129">方法显示后跟标点符号的字符串。</span><span class="sxs-lookup"><span data-stu-id="83069-129">The method displays the string followed by the punctuation marks.</span></span>

[!code-vb[VbVbalrExtensionMethods#3](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrExtensionMethods/VB/Class2.vb#3)]

<span data-ttu-id="83069-130">通过在的字符串自变量中发送来调用方法 `punc` ： `example.PrintAndPunctuate(".")`</span><span class="sxs-lookup"><span data-stu-id="83069-130">The method is called by sending in a string argument for `punc`: `example.PrintAndPunctuate(".")`</span></span>

<span data-ttu-id="83069-131">下面的示例演示 `Print` 并 `PrintAndPunctuate` 定义和调用。</span><span class="sxs-lookup"><span data-stu-id="83069-131">The following example shows `Print` and `PrintAndPunctuate` defined and called.</span></span> <span data-ttu-id="83069-132"><xref:System.Runtime.CompilerServices> 在定义模块中导入，以便能够访问扩展属性。</span><span class="sxs-lookup"><span data-stu-id="83069-132"><xref:System.Runtime.CompilerServices> is imported in the definition module in order to enable access to the extension attribute.</span></span>

```vb
Imports System.Runtime.CompilerServices

Module StringExtensions

    <Extension()>
    Public Sub Print(aString As String)
        Console.WriteLine(aString)
    End Sub

    <Extension()>
    Public Sub PrintAndPunctuate(aString As String, punc As String)
        Console.WriteLine(aString & punc)
    End Sub
End Module
```

<span data-ttu-id="83069-133">接下来，扩展方法将进入范围并被调用：</span><span class="sxs-lookup"><span data-stu-id="83069-133">Next, the extension methods are brought into scope and called:</span></span>

```vb
Imports ConsoleApplication2.StringExtensions

Module Module1

    Sub Main()
        Dim example As String = "Example string"
        example.Print()

        example = "Hello"
        example.PrintAndPunctuate(".")
        example.PrintAndPunctuate("!!!!")
    End Sub
End Module
```

<span data-ttu-id="83069-134">运行这些或类似扩展方法所需的全部都是在范围内。</span><span class="sxs-lookup"><span data-stu-id="83069-134">All that is required to be able to run these or similar extension methods is that they be in scope.</span></span> <span data-ttu-id="83069-135">如果包含扩展方法的模块位于范围内，则它将显示在 IntelliSense 中，并可作为普通的实例方法调用。</span><span class="sxs-lookup"><span data-stu-id="83069-135">If the module that contains an extension method is in scope, it is visible in IntelliSense and can be called as if it were an ordinary instance method.</span></span>

<span data-ttu-id="83069-136">请注意，当调用方法时，不会在中为第一个参数发送参数。</span><span class="sxs-lookup"><span data-stu-id="83069-136">Notice that when the methods are invoked, no argument is sent in for the first parameter.</span></span> <span data-ttu-id="83069-137">`aString`前面方法定义中的参数绑定到 `example` ， `String` 后者调用它们。</span><span class="sxs-lookup"><span data-stu-id="83069-137">Parameter `aString` in the previous method definitions is bound to `example`, the instance of `String` that calls them.</span></span> <span data-ttu-id="83069-138">编译器将使用 `example` 作为发送到第一个参数的参数。</span><span class="sxs-lookup"><span data-stu-id="83069-138">The compiler will use `example` as the argument sent to the first parameter.</span></span>

<span data-ttu-id="83069-139">如果为设置为的对象调用扩展方法 `Nothing` ，则将执行扩展方法。</span><span class="sxs-lookup"><span data-stu-id="83069-139">If an extension method is called for an object that is set to `Nothing`, the extension method executes.</span></span> <span data-ttu-id="83069-140">这不适用于普通实例方法。</span><span class="sxs-lookup"><span data-stu-id="83069-140">This does not apply to ordinary instance methods.</span></span> <span data-ttu-id="83069-141">可以 `Nothing` 在扩展方法中显式检查。</span><span class="sxs-lookup"><span data-stu-id="83069-141">You can explicitly check for `Nothing` in the extension method.</span></span>

## <a name="types-that-can-be-extended"></a><span data-ttu-id="83069-142">可扩展的类型</span><span class="sxs-lookup"><span data-stu-id="83069-142">Types that can be extended</span></span>

<span data-ttu-id="83069-143">可以在可在 Visual Basic 参数列表中表示的大多数类型上定义扩展方法，其中包括：</span><span class="sxs-lookup"><span data-stu-id="83069-143">You can define an extension method on most types that can be represented in a Visual Basic parameter list, including the following:</span></span>

- <span data-ttu-id="83069-144">引用类型 (类) </span><span class="sxs-lookup"><span data-stu-id="83069-144">Classes (reference types)</span></span>
- <span data-ttu-id="83069-145">结构 (值类型) </span><span class="sxs-lookup"><span data-stu-id="83069-145">Structures (value types)</span></span>
- <span data-ttu-id="83069-146">接口</span><span class="sxs-lookup"><span data-stu-id="83069-146">Interfaces</span></span>
- <span data-ttu-id="83069-147">委托</span><span class="sxs-lookup"><span data-stu-id="83069-147">Delegates</span></span>
- <span data-ttu-id="83069-148">ByRef 和 ByVal 参数</span><span class="sxs-lookup"><span data-stu-id="83069-148">ByRef and ByVal arguments</span></span>
- <span data-ttu-id="83069-149">泛型方法参数</span><span class="sxs-lookup"><span data-stu-id="83069-149">Generic method parameters</span></span>
- <span data-ttu-id="83069-150">数组</span><span class="sxs-lookup"><span data-stu-id="83069-150">Arrays</span></span>

<span data-ttu-id="83069-151">因为第一个参数指定扩展方法扩展的数据类型，所以它是必需的，并且不能是可选的。</span><span class="sxs-lookup"><span data-stu-id="83069-151">Because the first parameter specifies the data type that the extension method extends, it is required and cannot be optional.</span></span> <span data-ttu-id="83069-152">出于此原因， `Optional` 参数和 `ParamArray` 参数不能是参数列表中的第一个参数。</span><span class="sxs-lookup"><span data-stu-id="83069-152">For that reason, `Optional` parameters and `ParamArray` parameters cannot be the first parameter in the parameter list.</span></span>

<span data-ttu-id="83069-153">在后期绑定中不考虑扩展方法。</span><span class="sxs-lookup"><span data-stu-id="83069-153">Extension methods are not considered in late binding.</span></span> <span data-ttu-id="83069-154">在下面的示例中，语句 `anObject.PrintMe()` 引发 <xref:System.MissingMemberException> 异常，如果已删除第二个 `PrintMe` 扩展方法定义，则会看到相同的异常。</span><span class="sxs-lookup"><span data-stu-id="83069-154">In the following example, the statement `anObject.PrintMe()` raises a <xref:System.MissingMemberException> exception, the same exception you would see if the second `PrintMe` extension method definition were deleted.</span></span>

[!code-vb[VbVbalrExtensionMethods#9](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrExtensionMethods/VB/Class6.vb#9)]

## <a name="best-practices"></a><span data-ttu-id="83069-155">最佳实践</span><span class="sxs-lookup"><span data-stu-id="83069-155">Best practices</span></span>

<span data-ttu-id="83069-156">扩展方法提供了一种方便且功能强大的方法来扩展现有类型。</span><span class="sxs-lookup"><span data-stu-id="83069-156">Extension methods provide a convenient and powerful way to extend an existing type.</span></span> <span data-ttu-id="83069-157">但是，若要成功使用它们，需要考虑一些要点。</span><span class="sxs-lookup"><span data-stu-id="83069-157">However, to use them successfully, there are some points to consider.</span></span> <span data-ttu-id="83069-158">这些注意事项主要适用于类库的作者，但它们可能会影响任何使用扩展方法的应用程序。</span><span class="sxs-lookup"><span data-stu-id="83069-158">These considerations apply mainly to authors of class libraries, but they might affect any application that uses extension methods.</span></span>

<span data-ttu-id="83069-159">最常见的情况是，您添加到不属于您的类型的扩展方法比添加到您控制的类型的扩展方法更易受到攻击。</span><span class="sxs-lookup"><span data-stu-id="83069-159">Most generally, extension methods that you add to types that you do not own are more vulnerable than extension methods added to types that you control.</span></span> <span data-ttu-id="83069-160">您不拥有的类可能会干扰您的扩展方法。</span><span class="sxs-lookup"><span data-stu-id="83069-160">A number of things can occur in classes you do not own that can interfere with your extension methods.</span></span>

- <span data-ttu-id="83069-161">如果存在一个签名与调用语句中的参数兼容的可访问实例成员，并且不需要将自变量转换为参数，则将优先使用该实例方法来处理任何扩展方法。</span><span class="sxs-lookup"><span data-stu-id="83069-161">If any accessible instance member exists that has a signature that is compatible with the arguments in the calling statement, with no narrowing conversions required from argument to parameter, the instance method will be used in preference to any extension method.</span></span> <span data-ttu-id="83069-162">因此，如果在某个时间点向类添加了相应的实例方法，则您依赖的现有扩展成员可能会变得不可访问。</span><span class="sxs-lookup"><span data-stu-id="83069-162">Therefore, if an appropriate instance method is added to a class at some point, an existing extension member that you rely on may become inaccessible.</span></span>

- <span data-ttu-id="83069-163">扩展方法的作者无法阻止其他程序员编写可能优先于原始扩展的冲突扩展方法。</span><span class="sxs-lookup"><span data-stu-id="83069-163">The author of an extension method cannot prevent other programmers from writing conflicting extension methods that may have precedence over the original extension.</span></span>

- <span data-ttu-id="83069-164">您可以通过将扩展方法置于其自己的命名空间中来提高可靠性。</span><span class="sxs-lookup"><span data-stu-id="83069-164">You can improve robustness by putting extension methods in their own namespace.</span></span> <span data-ttu-id="83069-165">然后，你的库的使用者可以包括命名空间或排除命名空间，或在命名空间中进行选择，与库的其余部分分开。</span><span class="sxs-lookup"><span data-stu-id="83069-165">Consumers of your library can then include a namespace or exclude it, or select among namespaces, separately from the rest of the library.</span></span>

- <span data-ttu-id="83069-166">扩展接口可能比扩展类更安全，特别是在你不拥有接口或类时。</span><span class="sxs-lookup"><span data-stu-id="83069-166">It may be safer to extend interfaces than it is to extend classes, especially if you do not own the interface or class.</span></span> <span data-ttu-id="83069-167">接口的更改将影响实现它的每个类。</span><span class="sxs-lookup"><span data-stu-id="83069-167">A change in an interface affects every class that implements it.</span></span> <span data-ttu-id="83069-168">因此，作者在接口中添加或更改方法可能会降低。</span><span class="sxs-lookup"><span data-stu-id="83069-168">Therefore, the author may be less likely to add or change methods in an interface.</span></span> <span data-ttu-id="83069-169">但是，如果某个类实现了两个具有相同签名的扩展方法的接口，则这两个扩展方法都不可见。</span><span class="sxs-lookup"><span data-stu-id="83069-169">However, if a class implements two interfaces that have extension methods with the same signature, neither extension method is visible.</span></span>

- <span data-ttu-id="83069-170">扩展您可以的最特定类型。</span><span class="sxs-lookup"><span data-stu-id="83069-170">Extend the most specific type you can.</span></span> <span data-ttu-id="83069-171">在类型的层次结构中，如果你选择派生了许多其他类型的类型，则引入实例方法或其他可能会干扰你的方法的扩展方法可能有一些层。</span><span class="sxs-lookup"><span data-stu-id="83069-171">In a hierarchy of types, if you select a type from which many other types are derived, there are layers of possibilities for the introduction of instance methods or other extension methods that might interfere with yours.</span></span>

## <a name="extension-methods-instance-methods-and-properties"></a><span data-ttu-id="83069-172">扩展方法、实例方法和属性</span><span class="sxs-lookup"><span data-stu-id="83069-172">Extension methods, instance methods, and properties</span></span>

<span data-ttu-id="83069-173">如果范围内实例方法的签名与调用语句的参数兼容，则将优先选择该实例方法作为任何扩展方法。</span><span class="sxs-lookup"><span data-stu-id="83069-173">When an in-scope instance method has a signature that is compatible with the arguments of a calling statement, the instance method is chosen in preference to any extension method.</span></span> <span data-ttu-id="83069-174">即使扩展方法更匹配，实例方法也具有优先权。</span><span class="sxs-lookup"><span data-stu-id="83069-174">The instance method has precedence even if the extension method is a better match.</span></span> <span data-ttu-id="83069-175">在下面的示例中， `ExampleClass` 包含一个名为 `ExampleMethod` 的实例方法，该方法具有一个类型为的参数 `Integer` 。</span><span class="sxs-lookup"><span data-stu-id="83069-175">In the following example, `ExampleClass` contains an instance method named `ExampleMethod` that has one parameter of type `Integer`.</span></span> <span data-ttu-id="83069-176">扩展方法 `ExampleMethod` 扩展 `ExampleClass` 了，并具有一个类型为的参数 `Long` 。</span><span class="sxs-lookup"><span data-stu-id="83069-176">Extension method `ExampleMethod` extends `ExampleClass`, and has one parameter of type `Long`.</span></span>

[!code-vb[VbVbalrExtensionMethods#4](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrExtensionMethods/VB/Class4.vb#4)]

<span data-ttu-id="83069-177">在下面的代码中，对的第一次调用将 `ExampleMethod` 调用扩展方法，因为 `arg1` 为 `Long` ，并且仅与 `Long` 扩展方法中的参数兼容。</span><span class="sxs-lookup"><span data-stu-id="83069-177">The first call to `ExampleMethod` in the following code calls the extension method, because `arg1` is `Long` and is compatible only with the `Long` parameter in the extension method.</span></span> <span data-ttu-id="83069-178">对的第二次调用 `ExampleMethod` 具有 `Integer` 参数， `arg2` 并调用实例方法。</span><span class="sxs-lookup"><span data-stu-id="83069-178">The second call to `ExampleMethod` has an `Integer` argument, `arg2`, and it calls the instance method.</span></span>

[!code-vb[VbVbalrExtensionMethods#5](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrExtensionMethods/VB/Class4.vb#5)]

<span data-ttu-id="83069-179">现在反转两种方法中参数的数据类型：</span><span class="sxs-lookup"><span data-stu-id="83069-179">Now reverse the data types of the parameters in the two methods:</span></span>

[!code-vb[VbVbalrExtensionMethods#6](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrExtensionMethods/VB/Class5.vb#6)]

<span data-ttu-id="83069-180">这次，中的代码 `Main` 同时调用实例方法。</span><span class="sxs-lookup"><span data-stu-id="83069-180">This time the code in `Main` calls the instance method both times.</span></span> <span data-ttu-id="83069-181">这是因为 `arg1` 和都 `arg2` 具有到的扩大转换 `Long` ，并且在这两种情况下，实例方法优先于扩展方法。</span><span class="sxs-lookup"><span data-stu-id="83069-181">This is because both `arg1` and `arg2` have a widening conversion to `Long`, and the instance method takes precedence over the extension method in both cases.</span></span>

[!code-vb[VbVbalrExtensionMethods#7](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrExtensionMethods/VB/Class5.vb#7)]

<span data-ttu-id="83069-182">因此，扩展方法不能替换现有的实例方法。</span><span class="sxs-lookup"><span data-stu-id="83069-182">Therefore, an extension method cannot replace an existing instance method.</span></span> <span data-ttu-id="83069-183">但是，当扩展方法与实例方法同名但签名不冲突时，这两种方法都可以访问。</span><span class="sxs-lookup"><span data-stu-id="83069-183">However, when an extension method has the same name as an instance method but the signatures do not conflict, both methods can be accessed.</span></span> <span data-ttu-id="83069-184">例如，如果类 `ExampleClass` 包含一个名为的方法， `ExampleMethod` 该方法不使用参数，则允许具有相同名称但不同签名的扩展方法，如下面的代码所示。</span><span class="sxs-lookup"><span data-stu-id="83069-184">For example, if class `ExampleClass` contains a method named `ExampleMethod` that takes no arguments, extension methods with the same name but different signatures are permitted, as shown in the following code.</span></span>

[!code-vb[VbVbalrExtensionMethods#8](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrExtensionMethods/VB/Module3.vb#8)]

<span data-ttu-id="83069-185">此代码的输出如下所示：</span><span class="sxs-lookup"><span data-stu-id="83069-185">The output from this code is as follows:</span></span>

```console
Extension method
Instance method
```

<span data-ttu-id="83069-186">对于属性，这种情况更简单：如果扩展方法与它所扩展的类的属性具有相同的名称，则扩展方法不可见且无法访问。</span><span class="sxs-lookup"><span data-stu-id="83069-186">The situation is simpler with properties: if an extension method has the same name as a property of the class it extends, the extension method is not visible and cannot be accessed.</span></span>

## <a name="extension-method-precedence"></a><span data-ttu-id="83069-187">扩展方法的优先级</span><span class="sxs-lookup"><span data-stu-id="83069-187">Extension method precedence</span></span>

<span data-ttu-id="83069-188">如果两个具有相同签名的扩展方法处于范围内并且可访问，则将调用优先级较高的扩展方法。</span><span class="sxs-lookup"><span data-stu-id="83069-188">When two extension methods that have identical signatures are in scope and accessible, the one with higher precedence will be invoked.</span></span> <span data-ttu-id="83069-189">扩展方法的优先级基于用于使方法进入范围的机制。</span><span class="sxs-lookup"><span data-stu-id="83069-189">An extension method's precedence is based on the mechanism used to bring the method into scope.</span></span> <span data-ttu-id="83069-190">以下列表显示优先层次结构（从高到低）。</span><span class="sxs-lookup"><span data-stu-id="83069-190">The following list shows the precedence hierarchy, from highest to lowest.</span></span>

1. <span data-ttu-id="83069-191">在当前模块内定义的扩展方法。</span><span class="sxs-lookup"><span data-stu-id="83069-191">Extension methods defined inside the current module.</span></span>

2. <span data-ttu-id="83069-192">在当前命名空间中的数据类型或其父命名空间中定义的扩展方法，其优先级高于父命名空间的子命名空间。</span><span class="sxs-lookup"><span data-stu-id="83069-192">Extension methods defined inside data types in the current namespace or any one of its parents, with child namespaces having higher precedence than parent namespaces.</span></span>

3. <span data-ttu-id="83069-193">在当前文件的任何类型导入中定义的扩展方法。</span><span class="sxs-lookup"><span data-stu-id="83069-193">Extension methods defined inside any type imports in the current file.</span></span>

4. <span data-ttu-id="83069-194">在当前文件中的任何命名空间导入中定义的扩展方法。</span><span class="sxs-lookup"><span data-stu-id="83069-194">Extension methods defined inside any namespace imports in the current file.</span></span>

5. <span data-ttu-id="83069-195">在任何项目级类型导入中定义的扩展方法。</span><span class="sxs-lookup"><span data-stu-id="83069-195">Extension methods defined inside any project-level type imports.</span></span>

6. <span data-ttu-id="83069-196">在任何项目级命名空间导入中定义的扩展方法。</span><span class="sxs-lookup"><span data-stu-id="83069-196">Extension methods defined inside any project-level namespace imports.</span></span>

<span data-ttu-id="83069-197">如果优先顺序不能解析多义性，则可以使用完全限定名称来指定要调用的方法。</span><span class="sxs-lookup"><span data-stu-id="83069-197">If precedence does not resolve the ambiguity, you can use the fully qualified name to specify the method that you are calling.</span></span> <span data-ttu-id="83069-198">如果 `Print` 前面的示例中的方法是在名为的模块中定义的 `StringExtensions` ，则完全限定的名称为 `StringExtensions.Print(example)` 而不是 `example.Print()` 。</span><span class="sxs-lookup"><span data-stu-id="83069-198">If the `Print` method in the earlier example is defined in a module named `StringExtensions`, the fully qualified name is `StringExtensions.Print(example)` instead of `example.Print()`.</span></span>

## <a name="see-also"></a><span data-ttu-id="83069-199">请参阅</span><span class="sxs-lookup"><span data-stu-id="83069-199">See also</span></span>

- <xref:System.Runtime.CompilerServices>
- <xref:System.Runtime.CompilerServices.ExtensionAttribute>
- [<span data-ttu-id="83069-200">扩展方法</span><span class="sxs-lookup"><span data-stu-id="83069-200">Extension Methods</span></span>](../../../../csharp/programming-guide/classes-and-structs/extension-methods.md)
- [<span data-ttu-id="83069-201">Module 语句</span><span class="sxs-lookup"><span data-stu-id="83069-201">Module Statement</span></span>](../../../language-reference/statements/module-statement.md)
- [<span data-ttu-id="83069-202">过程形参和实参</span><span class="sxs-lookup"><span data-stu-id="83069-202">Procedure Parameters and Arguments</span></span>](procedure-parameters-and-arguments.md)
- [<span data-ttu-id="83069-203">可选参数</span><span class="sxs-lookup"><span data-stu-id="83069-203">Optional Parameters</span></span>](optional-parameters.md)
- [<span data-ttu-id="83069-204">参数数组</span><span class="sxs-lookup"><span data-stu-id="83069-204">Parameter Arrays</span></span>](parameter-arrays.md)
- [<span data-ttu-id="83069-205">属性概述</span><span class="sxs-lookup"><span data-stu-id="83069-205">Attributes overview</span></span>](../../concepts/attributes/index.md)
- [<span data-ttu-id="83069-206">Visual Basic 中的范围</span><span class="sxs-lookup"><span data-stu-id="83069-206">Scope in Visual Basic</span></span>](../declared-elements/scope.md)
