---
description: 了解详细信息：范围 Visual Basic
title: 范围
ms.date: 07/20/2015
helpviewer_keywords:
- module scope [Visual Basic]
- scope [Visual Basic], levels
- module level
- procedures [Visual Basic], scope
- declared elements [Visual Basic], scope
- namespaces [Visual Basic], scope
- scope [Visual Basic], declared elements
- scope [Visual Basic], about scope
- levels of scope [Visual Basic]
- block scope [Visual Basic]
- scope [Visual Basic], Visual Basic
- procedure scope [Visual Basic]
ms.assetid: 208106fe-79c9-4eec-93c6-55f08548895f
ms.openlocfilehash: 5b5412f5743162bb91fc3651d08f5c7ff9ba8abd
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100480201"
---
# <a name="scope-in-visual-basic"></a><span data-ttu-id="7724b-103">Visual Basic 中的范围</span><span class="sxs-lookup"><span data-stu-id="7724b-103">Scope in Visual Basic</span></span>

<span data-ttu-id="7724b-104">已声明元素的 *作用域* 是所有可引用它的代码的集合，而无需限定其名称，也不能通过 [导入语句 ( .net 命名空间和类型)](../../../language-reference/statements/imports-statement-net-namespace-and-type.md)提供。</span><span class="sxs-lookup"><span data-stu-id="7724b-104">The *scope* of a declared element is the set of all code that can refer to it without qualifying its name or making it available through an [Imports Statement (.NET Namespace and Type)](../../../language-reference/statements/imports-statement-net-namespace-and-type.md).</span></span> <span data-ttu-id="7724b-105">元素可以具有以下级别之一的作用域：</span><span class="sxs-lookup"><span data-stu-id="7724b-105">An element can have scope at one of the following levels:</span></span>

|<span data-ttu-id="7724b-106">级别</span><span class="sxs-lookup"><span data-stu-id="7724b-106">Level</span></span>|<span data-ttu-id="7724b-107">说明</span><span class="sxs-lookup"><span data-stu-id="7724b-107">Description</span></span>|
|-----------|-----------------|
|<span data-ttu-id="7724b-108">块范围</span><span class="sxs-lookup"><span data-stu-id="7724b-108">Block scope</span></span>|<span data-ttu-id="7724b-109">仅在声明它的代码块内可用</span><span class="sxs-lookup"><span data-stu-id="7724b-109">Available only within the code block in which it is declared</span></span>|
|<span data-ttu-id="7724b-110">过程范围</span><span class="sxs-lookup"><span data-stu-id="7724b-110">Procedure scope</span></span>|<span data-ttu-id="7724b-111">对声明它的过程中的所有代码可用</span><span class="sxs-lookup"><span data-stu-id="7724b-111">Available to all code within the procedure in which it is declared</span></span>|
|<span data-ttu-id="7724b-112">模块范围</span><span class="sxs-lookup"><span data-stu-id="7724b-112">Module scope</span></span>|<span data-ttu-id="7724b-113">适用于声明它的模块、类或结构中的所有代码</span><span class="sxs-lookup"><span data-stu-id="7724b-113">Available to all code within the module, class, or structure in which it is declared</span></span>|
|<span data-ttu-id="7724b-114">命名空间范围</span><span class="sxs-lookup"><span data-stu-id="7724b-114">Namespace scope</span></span>|<span data-ttu-id="7724b-115">可用于声明它的命名空间中的所有代码</span><span class="sxs-lookup"><span data-stu-id="7724b-115">Available to all code in the namespace in which it is declared</span></span>|

<span data-ttu-id="7724b-116">这些范围内的范围进度从最小的 (块) 到最广泛的 (命名空间) ，其中最 *窄的范围* 指的是可以引用元素而不进行限定的最小代码集。</span><span class="sxs-lookup"><span data-stu-id="7724b-116">These levels of scope progress from the narrowest (block) to the widest (namespace), where *narrowest scope* means the smallest set of code that can refer to the element without qualification.</span></span> <span data-ttu-id="7724b-117">有关详细信息，请参阅本页上的 "范围级别"。</span><span class="sxs-lookup"><span data-stu-id="7724b-117">For more information, see "Levels of Scope" on this page.</span></span>

## <a name="specifying-scope-and-defining-variables"></a><span data-ttu-id="7724b-118">指定作用域和定义变量</span><span class="sxs-lookup"><span data-stu-id="7724b-118">Specifying Scope and Defining Variables</span></span>

<span data-ttu-id="7724b-119">在声明元素时指定其作用域。</span><span class="sxs-lookup"><span data-stu-id="7724b-119">You specify the scope of an element when you declare it.</span></span> <span data-ttu-id="7724b-120">范围可能取决于以下因素：</span><span class="sxs-lookup"><span data-stu-id="7724b-120">The scope can depend on the following factors:</span></span>

- <span data-ttu-id="7724b-121">区域 (块、过程、模块、类或结构中声明元素) </span><span class="sxs-lookup"><span data-stu-id="7724b-121">The region (block, procedure, module, class, or structure) in which you declare the element</span></span>

- <span data-ttu-id="7724b-122">包含元素声明的命名空间</span><span class="sxs-lookup"><span data-stu-id="7724b-122">The namespace containing the element's declaration</span></span>

- <span data-ttu-id="7724b-123">为元素声明的访问级别</span><span class="sxs-lookup"><span data-stu-id="7724b-123">The access level you declare for the element</span></span>

<span data-ttu-id="7724b-124">定义名称相同但范围不同的变量时请小心，因为这样做可能会导致意外的结果。</span><span class="sxs-lookup"><span data-stu-id="7724b-124">Use care when you define variables with the same name but different scope, because doing so can lead to unexpected results.</span></span> <span data-ttu-id="7724b-125">有关详细信息，请参阅 [References to Declared Elements](references-to-declared-elements.md)。</span><span class="sxs-lookup"><span data-stu-id="7724b-125">For more information, see [References to Declared Elements](references-to-declared-elements.md).</span></span>

## <a name="levels-of-scope"></a><span data-ttu-id="7724b-126">范围级别</span><span class="sxs-lookup"><span data-stu-id="7724b-126">Levels of Scope</span></span>

<span data-ttu-id="7724b-127">编程元素可在声明它的整个区域内使用。</span><span class="sxs-lookup"><span data-stu-id="7724b-127">A programming element is available throughout the region in which you declare it.</span></span> <span data-ttu-id="7724b-128">同一区域中的所有代码都可以引用元素，而无需限定其名称。</span><span class="sxs-lookup"><span data-stu-id="7724b-128">All code in the same region can refer to the element without qualifying its name.</span></span>

### <a name="block-scope"></a><span data-ttu-id="7724b-129">块范围</span><span class="sxs-lookup"><span data-stu-id="7724b-129">Block Scope</span></span>

<span data-ttu-id="7724b-130">块是包含在启动和终止声明语句中的一组语句，如下所示：</span><span class="sxs-lookup"><span data-stu-id="7724b-130">A block is a set of statements enclosed within initiating and terminating declaration statements, such as the following:</span></span>

- <span data-ttu-id="7724b-131">`Do` 和 `Loop`</span><span class="sxs-lookup"><span data-stu-id="7724b-131">`Do` and `Loop`</span></span>

- <span data-ttu-id="7724b-132">`For` [ `Each` ] 和 `Next`</span><span class="sxs-lookup"><span data-stu-id="7724b-132">`For` [`Each`] and `Next`</span></span>

- <span data-ttu-id="7724b-133">`If` 和 `End If`</span><span class="sxs-lookup"><span data-stu-id="7724b-133">`If` and `End If`</span></span>

- <span data-ttu-id="7724b-134">`Select` 和 `End Select`</span><span class="sxs-lookup"><span data-stu-id="7724b-134">`Select` and `End Select`</span></span>

- <span data-ttu-id="7724b-135">`SyncLock` 和 `End SyncLock`</span><span class="sxs-lookup"><span data-stu-id="7724b-135">`SyncLock` and `End SyncLock`</span></span>

- <span data-ttu-id="7724b-136">`Try` 和 `End Try`</span><span class="sxs-lookup"><span data-stu-id="7724b-136">`Try` and `End Try`</span></span>

- <span data-ttu-id="7724b-137">`While` 和 `End While`</span><span class="sxs-lookup"><span data-stu-id="7724b-137">`While` and `End While`</span></span>

- <span data-ttu-id="7724b-138">`With` 和 `End With`</span><span class="sxs-lookup"><span data-stu-id="7724b-138">`With` and `End With`</span></span>

<span data-ttu-id="7724b-139">如果在块中声明一个变量，则只能在该块内使用它。</span><span class="sxs-lookup"><span data-stu-id="7724b-139">If you declare a variable within a block, you can use it only within that block.</span></span> <span data-ttu-id="7724b-140">在下面的示例中，整数变量的作用域 `cube` 是介于和之间的块 `If` `End If` ， `cube` 当执行传递到块时，你将无法再引用。</span><span class="sxs-lookup"><span data-stu-id="7724b-140">In the following example, the scope of the integer variable `cube` is the block between `If` and `End If`, and you can no longer refer to `cube` when execution passes out of the block.</span></span>

```vb
If n < 1291 Then
    Dim cube As Integer
    cube = n ^ 3
End If
```

> [!NOTE]
> <span data-ttu-id="7724b-141">即使变量的作用域限制为块，其生存期仍是整个过程的生存期。</span><span class="sxs-lookup"><span data-stu-id="7724b-141">Even if the scope of a variable is limited to a block, its lifetime is still that of the entire procedure.</span></span> <span data-ttu-id="7724b-142">如果在过程中多次输入块，则每个块变量将保留其以前的值。</span><span class="sxs-lookup"><span data-stu-id="7724b-142">If you enter the block more than once during the procedure, each block variable retains its previous value.</span></span> <span data-ttu-id="7724b-143">若要避免在这种情况下出现意外结果，最好在块的开头初始化块变量。</span><span class="sxs-lookup"><span data-stu-id="7724b-143">To avoid unexpected results in such a case, it is wise to initialize block variables at the beginning of the block.</span></span>

### <a name="procedure-scope"></a><span data-ttu-id="7724b-144">过程范围</span><span class="sxs-lookup"><span data-stu-id="7724b-144">Procedure Scope</span></span>

<span data-ttu-id="7724b-145">在过程中声明的元素在该过程之外不可用。</span><span class="sxs-lookup"><span data-stu-id="7724b-145">An element declared within a procedure is not available outside that procedure.</span></span> <span data-ttu-id="7724b-146">只有包含声明的过程可以使用它。</span><span class="sxs-lookup"><span data-stu-id="7724b-146">Only the procedure that contains the declaration can use it.</span></span> <span data-ttu-id="7724b-147">此级别的变量也称为 *局部变量*。</span><span class="sxs-lookup"><span data-stu-id="7724b-147">Variables at this level are also known as *local variables*.</span></span> <span data-ttu-id="7724b-148">用 [Dim 语句](../../../language-reference/statements/dim-statement.md)声明它们，无论是还是不带 [Static](../../../language-reference/modifiers/static.md) 关键字。</span><span class="sxs-lookup"><span data-stu-id="7724b-148">You declare them with the [Dim Statement](../../../language-reference/statements/dim-statement.md), with or without the [Static](../../../language-reference/modifiers/static.md) keyword.</span></span>

<span data-ttu-id="7724b-149">过程和块范围密切相关。</span><span class="sxs-lookup"><span data-stu-id="7724b-149">Procedure and block scope are closely related.</span></span> <span data-ttu-id="7724b-150">如果在过程内但在该过程中的任何块外声明变量，则可以将变量视为具有块范围，其中块是整个过程。</span><span class="sxs-lookup"><span data-stu-id="7724b-150">If you declare a variable inside a procedure but outside any block within that procedure, you can think of the variable as having block scope, where the block is the entire procedure.</span></span>

> [!NOTE]
> <span data-ttu-id="7724b-151">所有本地元素（即使它们是 `Static` 变量）都专用于它们出现的过程。</span><span class="sxs-lookup"><span data-stu-id="7724b-151">All local elements, even if they are `Static` variables, are private to the procedure in which they appear.</span></span> <span data-ttu-id="7724b-152">不能在过程中使用 [Public](../../../language-reference/modifiers/public.md) 关键字声明任何元素。</span><span class="sxs-lookup"><span data-stu-id="7724b-152">You cannot declare any element using the [Public](../../../language-reference/modifiers/public.md) keyword within a procedure.</span></span>

### <a name="module-scope"></a><span data-ttu-id="7724b-153">模块范围</span><span class="sxs-lookup"><span data-stu-id="7724b-153">Module Scope</span></span>

<span data-ttu-id="7724b-154">为方便起见，单术语 *模块级别* 同样适用于模块、类和结构。</span><span class="sxs-lookup"><span data-stu-id="7724b-154">For convenience, the single term *module level* applies equally to modules, classes, and structures.</span></span> <span data-ttu-id="7724b-155">您可以通过将声明语句置于任何过程或块的外部，但在模块、类或结构中，在此级别声明元素。</span><span class="sxs-lookup"><span data-stu-id="7724b-155">You can declare elements at this level by placing the declaration statement outside of any procedure or block but within the module, class, or structure.</span></span>

<span data-ttu-id="7724b-156">在模块级别进行声明时，所选的访问级别将确定范围。</span><span class="sxs-lookup"><span data-stu-id="7724b-156">When you make a declaration at the module level, the access level you choose determines the scope.</span></span> <span data-ttu-id="7724b-157">包含模块、类或结构的命名空间还会影响范围。</span><span class="sxs-lookup"><span data-stu-id="7724b-157">The namespace that contains the module, class, or structure also affects the scope.</span></span>

<span data-ttu-id="7724b-158">声明 [专用](../../../language-reference/modifiers/private.md) 访问级别的元素可用于该模块中的每个过程，但不能用于不同模块中的任何代码。</span><span class="sxs-lookup"><span data-stu-id="7724b-158">Elements for which you declare [Private](../../../language-reference/modifiers/private.md) access level are available to every procedure in that module, but not to any code in a different module.</span></span> <span data-ttu-id="7724b-159">`Dim` `Private` 如果不使用任何访问级别关键字，模块级别的语句将默认为。</span><span class="sxs-lookup"><span data-stu-id="7724b-159">The `Dim` statement at module level defaults to `Private` if you do not use any access level keywords.</span></span> <span data-ttu-id="7724b-160">但是，可以在语句中使用关键字，使作用域和访问级别更明显 `Private` `Dim` 。</span><span class="sxs-lookup"><span data-stu-id="7724b-160">However, you can make the scope and access level more obvious by using the `Private` keyword in the `Dim` statement.</span></span>

<span data-ttu-id="7724b-161">在下面的示例中，模块中定义的所有过程都可以引用字符串变量 `strMsg` 。</span><span class="sxs-lookup"><span data-stu-id="7724b-161">In the following example, all procedures defined in the module can refer to the string variable `strMsg`.</span></span> <span data-ttu-id="7724b-162">调用第二个过程时，将在对话框中显示字符串变量的内容 `strMsg` 。</span><span class="sxs-lookup"><span data-stu-id="7724b-162">When the second procedure is called, it displays the contents of the string variable `strMsg` in a dialog box.</span></span>

```vb
' Put the following declaration at module level (not in any procedure).
Private strMsg As String
' Put the following Sub procedure in the same module.
Sub initializePrivateVariable()
    strMsg = "This variable cannot be used outside this module."
End Sub
' Put the following Sub procedure in the same module.
Sub usePrivateVariable()
    MsgBox(strMsg)
End Sub
```

### <a name="namespace-scope"></a><span data-ttu-id="7724b-163">命名空间范围</span><span class="sxs-lookup"><span data-stu-id="7724b-163">Namespace Scope</span></span>

<span data-ttu-id="7724b-164">如果使用 [Friend](../../../language-reference/modifiers/friend.md) 或 [Public](../../../language-reference/modifiers/public.md) 关键字在模块级别声明一个元素，则该元素将可用于声明该元素的整个命名空间中的所有过程。</span><span class="sxs-lookup"><span data-stu-id="7724b-164">If you declare an element at module level using the [Friend](../../../language-reference/modifiers/friend.md) or [Public](../../../language-reference/modifiers/public.md) keyword, it becomes available to all procedures throughout the namespace in which the element is declared.</span></span> <span data-ttu-id="7724b-165">对于前面的示例的以下更改，字符串变量 `strMsg` 可以在其声明的命名空间中的任何位置通过代码引用。</span><span class="sxs-lookup"><span data-stu-id="7724b-165">With the following alteration to the preceding example, the string variable `strMsg` can be referred to by code anywhere in the namespace of its declaration.</span></span>

```vb
' Include this declaration at module level (not inside any procedure).
Public strMsg As String
```

<span data-ttu-id="7724b-166">命名空间范围包括嵌套命名空间。</span><span class="sxs-lookup"><span data-stu-id="7724b-166">Namespace scope includes nested namespaces.</span></span> <span data-ttu-id="7724b-167">命名空间中的可用元素也可以从嵌套在该命名空间中的任何命名空间中使用。</span><span class="sxs-lookup"><span data-stu-id="7724b-167">An element available from within a namespace is also available from within any namespace nested inside that namespace.</span></span>

<span data-ttu-id="7724b-168">如果你的项目不包含任何 [命名空间语句](../../../language-reference/statements/namespace-statement.md)，则项目中的所有内容都在相同的命名空间中。</span><span class="sxs-lookup"><span data-stu-id="7724b-168">If your project does not contain any [Namespace Statement](../../../language-reference/statements/namespace-statement.md)s, everything in the project is in the same namespace.</span></span> <span data-ttu-id="7724b-169">在这种情况下，可以将命名空间范围视为项目范围。</span><span class="sxs-lookup"><span data-stu-id="7724b-169">In this case, namespace scope can be thought of as project scope.</span></span> <span data-ttu-id="7724b-170">`Public` 模块、类或结构中的元素也可用于引用其项目的任何项目。</span><span class="sxs-lookup"><span data-stu-id="7724b-170">`Public` elements in a module, class, or structure are also available to any project that references their project.</span></span>

## <a name="choice-of-scope"></a><span data-ttu-id="7724b-171">范围选择</span><span class="sxs-lookup"><span data-stu-id="7724b-171">Choice of Scope</span></span>

<span data-ttu-id="7724b-172">当你声明变量时，在选择其作用域时应牢记以下几点。</span><span class="sxs-lookup"><span data-stu-id="7724b-172">When you declare a variable, you should keep in mind the following points when choosing its scope.</span></span>

### <a name="advantages-of-local-variables"></a><span data-ttu-id="7724b-173">局部变量的优点</span><span class="sxs-lookup"><span data-stu-id="7724b-173">Advantages of Local Variables</span></span>

<span data-ttu-id="7724b-174">局部变量对于任何类型的临时计算都是一个不错的选择，原因如下：</span><span class="sxs-lookup"><span data-stu-id="7724b-174">Local variables are a good choice for any kind of temporary calculation, for the following reasons:</span></span>

- <span data-ttu-id="7724b-175">**避免名称冲突。**</span><span class="sxs-lookup"><span data-stu-id="7724b-175">**Name Conflict Avoidance.**</span></span> <span data-ttu-id="7724b-176">局部变量名称不容易发生冲突。</span><span class="sxs-lookup"><span data-stu-id="7724b-176">Local variable names are not susceptible to conflict.</span></span> <span data-ttu-id="7724b-177">例如，可以创建几个不同的过程，其中包含一个名为的变量 `intTemp` 。</span><span class="sxs-lookup"><span data-stu-id="7724b-177">For example, you can create several different procedures containing a variable called `intTemp`.</span></span> <span data-ttu-id="7724b-178">只要每个 `intTemp` 都声明为局部变量，每个过程就只能识别自己的版本 `intTemp` 。</span><span class="sxs-lookup"><span data-stu-id="7724b-178">As long as each `intTemp` is declared as a local variable, each procedure recognizes only its own version of `intTemp`.</span></span> <span data-ttu-id="7724b-179">任何一个过程都可以更改其本地中的值， `intTemp` 而不会影响 `intTemp` 其他过程中的变量。</span><span class="sxs-lookup"><span data-stu-id="7724b-179">Any one procedure can alter the value in its local `intTemp` without affecting `intTemp` variables in other procedures.</span></span>

- <span data-ttu-id="7724b-180">**内存消耗。**</span><span class="sxs-lookup"><span data-stu-id="7724b-180">**Memory Consumption.**</span></span> <span data-ttu-id="7724b-181">局部变量仅在其过程正在运行时占用内存。</span><span class="sxs-lookup"><span data-stu-id="7724b-181">Local variables consume memory only while their procedure is running.</span></span> <span data-ttu-id="7724b-182">当过程返回到调用代码时，将释放其内存。</span><span class="sxs-lookup"><span data-stu-id="7724b-182">Their memory is released when the procedure returns to the calling code.</span></span> <span data-ttu-id="7724b-183">相反， [共享](../../../language-reference/modifiers/shared.md) 和 [静态](../../../language-reference/modifiers/static.md) 变量将消耗内存资源，直到应用程序停止运行，因此仅在必要时才使用它们。</span><span class="sxs-lookup"><span data-stu-id="7724b-183">By contrast, [Shared](../../../language-reference/modifiers/shared.md) and [Static](../../../language-reference/modifiers/static.md) variables consume memory resources until your application stops running, so use them only when necessary.</span></span> <span data-ttu-id="7724b-184">*实例变量* 会在其实例继续存在时使用内存，这使得它们的效率低于局部变量，但可能更高效 `Shared` `Static` 。</span><span class="sxs-lookup"><span data-stu-id="7724b-184">*Instance variables* consume memory while their instance continues to exist, which makes them less efficient than local variables, but potentially more efficient than `Shared` or `Static` variables.</span></span>

### <a name="minimizing-scope"></a><span data-ttu-id="7724b-185">最小化范围</span><span class="sxs-lookup"><span data-stu-id="7724b-185">Minimizing Scope</span></span>

<span data-ttu-id="7724b-186">通常情况下，在声明任何变量或常量时，最好将范围设置为 "窄" (块范围是最窄的) 。</span><span class="sxs-lookup"><span data-stu-id="7724b-186">In general, when declaring any variable or constant, it is good programming practice to make the scope as narrow as possible (block scope is the narrowest).</span></span> <span data-ttu-id="7724b-187">这有助于节省内存，并最大程度地减少代码错误引用错误变量的几率。</span><span class="sxs-lookup"><span data-stu-id="7724b-187">This helps conserve memory and minimizes the chances of your code erroneously referring to the wrong variable.</span></span> <span data-ttu-id="7724b-188">同样，仅当需要在过程调用之间保留变量值时，才应将该变量声明为 [静态](../../../language-reference/modifiers/static.md) 。</span><span class="sxs-lookup"><span data-stu-id="7724b-188">Similarly, you should declare a variable to be [Static](../../../language-reference/modifiers/static.md) only when it is necessary to preserve its value between procedure calls.</span></span>

## <a name="see-also"></a><span data-ttu-id="7724b-189">请参阅</span><span class="sxs-lookup"><span data-stu-id="7724b-189">See also</span></span>

- [<span data-ttu-id="7724b-190">已声明元素的特性</span><span class="sxs-lookup"><span data-stu-id="7724b-190">Declared Element Characteristics</span></span>](declared-element-characteristics.md)
- [<span data-ttu-id="7724b-191">如何：控制变量的范围</span><span class="sxs-lookup"><span data-stu-id="7724b-191">How to: Control the Scope of a Variable</span></span>](how-to-control-the-scope-of-a-variable.md)
- [<span data-ttu-id="7724b-192">Visual Basic 中的生存期</span><span class="sxs-lookup"><span data-stu-id="7724b-192">Lifetime in Visual Basic</span></span>](lifetime.md)
- [<span data-ttu-id="7724b-193">Visual Basic 中的访问级别</span><span class="sxs-lookup"><span data-stu-id="7724b-193">Access levels in Visual Basic</span></span>](access-levels.md)
- [<span data-ttu-id="7724b-194">References to Declared Elements</span><span class="sxs-lookup"><span data-stu-id="7724b-194">References to Declared Elements</span></span>](references-to-declared-elements.md)
- [<span data-ttu-id="7724b-195">变量声明</span><span class="sxs-lookup"><span data-stu-id="7724b-195">Variable Declaration</span></span>](../variables/variable-declaration.md)
