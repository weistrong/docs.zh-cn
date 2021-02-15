---
description: 了解详细信息：中的变量声明 Visual Basic
title: 变量声明
ms.date: 07/20/2015
helpviewer_keywords:
- variables [Visual Basic], declaring
- member variables [Visual Basic], declarations
- Dim statement [Visual Basic], variable declaration
- declaring variables [Visual Basic]
- variables [Visual Basic], scope
- variables [Visual Basic], data types
- data types [Visual Basic], variable declarations
- lifetime [Visual Basic], variables
- variables [Visual Basic], lifetime
- access levels [Visual Basic], variables
- scope [Visual Basic], declaration statements
- variables [Visual Basic], access level
- local variables [Visual Basic], declarations
- scope [Visual Basic], variables
ms.assetid: d8f10226-92b1-480f-9f53-df377b2d7e15
ms.openlocfilehash: ef0e7bc7a99f320bd40788ef019b05c7ebf4ce46
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100462693"
---
# <a name="variable-declaration-in-visual-basic"></a><span data-ttu-id="fa388-103">Visual Basic 中的变量声明</span><span class="sxs-lookup"><span data-stu-id="fa388-103">Variable Declaration in Visual Basic</span></span>

<span data-ttu-id="fa388-104">声明一个变量来指定其名称和特征。</span><span class="sxs-lookup"><span data-stu-id="fa388-104">You declare a variable to specify its name and characteristics.</span></span> <span data-ttu-id="fa388-105">变量的声明语句是 [Dim 语句](../../../language-reference/statements/dim-statement.md)。</span><span class="sxs-lookup"><span data-stu-id="fa388-105">The declaration statement for variables is the [Dim Statement](../../../language-reference/statements/dim-statement.md).</span></span> <span data-ttu-id="fa388-106">其位置和内容确定变量的特征。</span><span class="sxs-lookup"><span data-stu-id="fa388-106">Its location and contents determine the variable's characteristics.</span></span>  
  
 <span data-ttu-id="fa388-107">有关变量命名规则和注意事项，请参阅已 [声明的元素名称](../declared-elements/declared-element-names.md)。</span><span class="sxs-lookup"><span data-stu-id="fa388-107">For variable naming rules and considerations, see [Declared Element Names](../declared-elements/declared-element-names.md).</span></span>  
  
## <a name="declaration-levels"></a><span data-ttu-id="fa388-108">声明级别</span><span class="sxs-lookup"><span data-stu-id="fa388-108">Declaration Levels</span></span>  
  
### <a name="local-and-member-variables"></a><span data-ttu-id="fa388-109">局部变量和成员变量</span><span class="sxs-lookup"><span data-stu-id="fa388-109">Local and Member Variables</span></span>  

 <span data-ttu-id="fa388-110">局部变量是在过程中声明的 *变量* 。</span><span class="sxs-lookup"><span data-stu-id="fa388-110">A *local variable* is one that is declared within a procedure.</span></span> <span data-ttu-id="fa388-111">*成员变量* 是 Visual Basic 类型的成员;它在模块级别、类、结构或模块中声明，但不在该类、结构或模块内部的任何过程中声明。</span><span class="sxs-lookup"><span data-stu-id="fa388-111">A *member variable* is a member of a Visual Basic type; it is declared at module level, inside a class, structure, or module, but not within any procedure internal to that class, structure, or module.</span></span>  
  
### <a name="shared-and-instance-variables"></a><span data-ttu-id="fa388-112">共享变量和实例变量</span><span class="sxs-lookup"><span data-stu-id="fa388-112">Shared and Instance Variables</span></span>  

 <span data-ttu-id="fa388-113">在类或结构中，成员变量的类别取决于它是否是共享的。</span><span class="sxs-lookup"><span data-stu-id="fa388-113">In a class or structure, the category of a member variable depends on whether or not it is shared.</span></span> <span data-ttu-id="fa388-114">如果使用 [shared](../../../language-reference/modifiers/shared.md) 关键字进行声明，则它是 *共享变量*，并且存在于在类或结构的所有实例中共享的单个副本。</span><span class="sxs-lookup"><span data-stu-id="fa388-114">If it is declared with the [Shared](../../../language-reference/modifiers/shared.md) keyword, it is a *shared variable*, and it exists in a single copy shared among all instances of the class or structure.</span></span>  
  
 <span data-ttu-id="fa388-115">否则，它是一个 *实例变量*，为类或结构的每个实例创建一个单独的副本。</span><span class="sxs-lookup"><span data-stu-id="fa388-115">Otherwise it is an *instance variable*, and a separate copy of it is created for each instance of the class or structure.</span></span> <span data-ttu-id="fa388-116">实例变量的给定副本仅可用于创建它的类或结构的实例。</span><span class="sxs-lookup"><span data-stu-id="fa388-116">A given copy of an instance variable is available only to the instance of the class or structure in which it was created.</span></span> <span data-ttu-id="fa388-117">它与类或结构的任何其他实例中的实例变量副本无关。</span><span class="sxs-lookup"><span data-stu-id="fa388-117">It is independent of a copy of the instance variable in any other instance of the class or structure.</span></span>  
  
## <a name="declaring-data-type"></a><span data-ttu-id="fa388-118">声明数据类型</span><span class="sxs-lookup"><span data-stu-id="fa388-118">Declaring Data Type</span></span>  

 <span data-ttu-id="fa388-119">声明语句中的 [As](../../../language-reference/statements/as-clause.md) 子句允许您定义要声明的变量的数据类型或对象类型。</span><span class="sxs-lookup"><span data-stu-id="fa388-119">The [As](../../../language-reference/statements/as-clause.md) clause in the declaration statement allows you to define the data type or object type of the variable you are declaring.</span></span> <span data-ttu-id="fa388-120">您可以为变量指定以下任意类型：</span><span class="sxs-lookup"><span data-stu-id="fa388-120">You can specify any of the following types for a variable:</span></span>  
  
- <span data-ttu-id="fa388-121">基本数据类型，如 `Boolean` 、 `Long` 或 `Decimal`</span><span class="sxs-lookup"><span data-stu-id="fa388-121">An elementary data type, such as `Boolean`, `Long`, or `Decimal`</span></span>  
  
- <span data-ttu-id="fa388-122">复合数据类型，例如数组或结构</span><span class="sxs-lookup"><span data-stu-id="fa388-122">A composite data type, such as an array or structure</span></span>  
  
- <span data-ttu-id="fa388-123">在应用程序或其他应用程序中定义的对象类型或类</span><span class="sxs-lookup"><span data-stu-id="fa388-123">An object type, or class, defined either in your application or in another application</span></span>  
  
- <span data-ttu-id="fa388-124">.NET Framework 类，如 <xref:System.Windows.Forms.Label> 或 <xref:System.Windows.Forms.TextBox></span><span class="sxs-lookup"><span data-stu-id="fa388-124">A .NET Framework class, such as <xref:System.Windows.Forms.Label> or <xref:System.Windows.Forms.TextBox></span></span>  
  
- <span data-ttu-id="fa388-125">接口类型，如 <xref:System.IComparable> 或 <xref:System.IDisposable></span><span class="sxs-lookup"><span data-stu-id="fa388-125">An interface type, such as <xref:System.IComparable> or <xref:System.IDisposable></span></span>  
  
 <span data-ttu-id="fa388-126">您可以在一个语句中声明多个变量，而不必重复该数据类型。</span><span class="sxs-lookup"><span data-stu-id="fa388-126">You can declare several variables in one statement without having to repeat the data type.</span></span> <span data-ttu-id="fa388-127">在下面的语句中，变量 `i` 、 `j` 和 `k` 被声明为类型 `Integer` ， `l` `m` `Long` `x` `y` `Single` and 和 and 作为：</span><span class="sxs-lookup"><span data-stu-id="fa388-127">In the following statements, the variables `i`, `j`, and `k` are declared as type `Integer`, `l` and `m` as `Long`, and `x` and `y` as `Single`:</span></span>  
  
```vb  
Dim i, j, k As Integer  
' All three variables in the preceding statement are declared as Integer.  
Dim l, m As Long, x, y As Single  
' In the preceding statement, l and m are Long, x and y are Single.  
```  
  
 <span data-ttu-id="fa388-128">有关数据类型的详细信息，请参阅 [数据类型](../data-types/index.md)。</span><span class="sxs-lookup"><span data-stu-id="fa388-128">For more information on data types, see [Data Types](../data-types/index.md).</span></span> <span data-ttu-id="fa388-129">有关对象的详细信息，请参阅 [对象和类](../objects-and-classes/index.md) 和 [对组件进行编程](/previous-versions/visualstudio/visual-studio-2013/0ffkdtkf(v=vs.120))。</span><span class="sxs-lookup"><span data-stu-id="fa388-129">For more information on objects, see [Objects and Classes](../objects-and-classes/index.md) and [Programming with Components](/previous-versions/visualstudio/visual-studio-2013/0ffkdtkf(v=vs.120)).</span></span>  
  
## <a name="local-type-inference"></a><span data-ttu-id="fa388-130">局部类型推理</span><span class="sxs-lookup"><span data-stu-id="fa388-130">Local Type Inference</span></span>  

 <span data-ttu-id="fa388-131">*类型推理* 用于确定没有子句声明的局部变量的数据类型 `As` 。</span><span class="sxs-lookup"><span data-stu-id="fa388-131">*Type inference* is used to determine the data types of local variables declared without an `As` clause.</span></span> <span data-ttu-id="fa388-132">编译器从初始化表达式的类型推断出变量的类型。</span><span class="sxs-lookup"><span data-stu-id="fa388-132">The compiler infers the type of the variable from the type of the initialization expression.</span></span> <span data-ttu-id="fa388-133">这样，便可以在不显式声明类型的情况下声明变量。</span><span class="sxs-lookup"><span data-stu-id="fa388-133">This enables you to declare variables without explicitly stating a type.</span></span> <span data-ttu-id="fa388-134">在下面的示例中， `num1` 和 `num2` 均强类型化为整数。</span><span class="sxs-lookup"><span data-stu-id="fa388-134">In the following example, both `num1` and `num2` are strongly typed as integers.</span></span>  
  
 [!code-vb[VbVbalrTypeInference#1](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrTypeInference/VB/Class1.vb#1)]  
  
 <span data-ttu-id="fa388-135">如果要使用局部类型推理，则 `Option Infer` 必须将设置为 `On` 。</span><span class="sxs-lookup"><span data-stu-id="fa388-135">If you want to use local type inference, `Option Infer` must be set to `On`.</span></span> <span data-ttu-id="fa388-136">有关详细信息，请参阅[本地类型推断](local-type-inference.md)和 [Option Infer 语句](../../../language-reference/statements/option-infer-statement.md)。</span><span class="sxs-lookup"><span data-stu-id="fa388-136">For more information, see [Local Type Inference](local-type-inference.md) and [Option Infer Statement](../../../language-reference/statements/option-infer-statement.md).</span></span>  
  
## <a name="characteristics-of-declared-variables"></a><span data-ttu-id="fa388-137">声明变量的特征</span><span class="sxs-lookup"><span data-stu-id="fa388-137">Characteristics of Declared Variables</span></span>  

 <span data-ttu-id="fa388-138">变量的 *生存期* 是指可供使用的时间段。</span><span class="sxs-lookup"><span data-stu-id="fa388-138">The *lifetime* of a variable is the period of time during which it is available for use.</span></span> <span data-ttu-id="fa388-139">通常情况下，只要变量的元素 (如过程或类) 继续存在，就会存在该变量。</span><span class="sxs-lookup"><span data-stu-id="fa388-139">In general, a variable exists as long as the element that declares it (such as a procedure or class) continues to exist.</span></span> <span data-ttu-id="fa388-140">如果变量不需要在其包含元素的生存期之外继续存在，则无需在声明中执行任何特殊操作。</span><span class="sxs-lookup"><span data-stu-id="fa388-140">If the variable does not need to continue existing beyond the lifetime of its containing element, you do not need to do anything special in the declaration.</span></span> <span data-ttu-id="fa388-141">如果变量需要比其包含元素更长的时间，则可以 `Static` `Shared` 在其语句中包含或关键字 `Dim` 。</span><span class="sxs-lookup"><span data-stu-id="fa388-141">If the variable needs to continue to exist longer than its containing element, you can include the `Static` or `Shared` keyword in its `Dim` statement.</span></span> <span data-ttu-id="fa388-142">有关详细信息，请参阅 [Visual Basic 中的生存期](../declared-elements/lifetime.md)。</span><span class="sxs-lookup"><span data-stu-id="fa388-142">For more information, see [Lifetime in Visual Basic](../declared-elements/lifetime.md).</span></span>  
  
 <span data-ttu-id="fa388-143">变量的 *作用域* 是指可以引用它的所有代码的集合，而无需限定其名称。</span><span class="sxs-lookup"><span data-stu-id="fa388-143">The *scope* of a variable is the set of all code that can refer to it without qualifying its name.</span></span> <span data-ttu-id="fa388-144">变量的作用域由声明它的位置确定。</span><span class="sxs-lookup"><span data-stu-id="fa388-144">A variable's scope is determined by where it is declared.</span></span> <span data-ttu-id="fa388-145">位于给定区域的代码可以使用该区域中定义的变量，而不必限定其名称。</span><span class="sxs-lookup"><span data-stu-id="fa388-145">Code located in a given region can use the variables defined in that region without having to qualify their names.</span></span> <span data-ttu-id="fa388-146">有关详细信息，请参阅 [Scope in Visual Basic](../declared-elements/scope.md)。</span><span class="sxs-lookup"><span data-stu-id="fa388-146">For more information, see [Scope in Visual Basic](../declared-elements/scope.md).</span></span>  
  
 <span data-ttu-id="fa388-147">变量的 *访问级别* 是有权访问它的代码的范围。</span><span class="sxs-lookup"><span data-stu-id="fa388-147">A variable's *access level* is the extent of code that has permission to access it.</span></span> <span data-ttu-id="fa388-148">这取决于访问修饰符 (例如，在语句中使用的 [Public](../../../language-reference/modifiers/public.md) 或 [Private](../../../language-reference/modifiers/private.md)) `Dim` 。</span><span class="sxs-lookup"><span data-stu-id="fa388-148">This is determined by the access modifier (such as [Public](../../../language-reference/modifiers/public.md) or [Private](../../../language-reference/modifiers/private.md)) that you use in the `Dim` statement.</span></span> <span data-ttu-id="fa388-149">有关详细信息，请参阅 [Visual Basic 中的访问级别](../declared-elements/access-levels.md)。</span><span class="sxs-lookup"><span data-stu-id="fa388-149">For more information, see [Access levels in Visual Basic](../declared-elements/access-levels.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="fa388-150">请参阅</span><span class="sxs-lookup"><span data-stu-id="fa388-150">See also</span></span>

- [<span data-ttu-id="fa388-151">如何：创建新变量</span><span class="sxs-lookup"><span data-stu-id="fa388-151">How to: Create a New Variable</span></span>](how-to-create-a-new-variable.md)
- [<span data-ttu-id="fa388-152">如何：将数据移入和移出变量</span><span class="sxs-lookup"><span data-stu-id="fa388-152">How to: Move Data Into and Out of a Variable</span></span>](how-to-move-data-into-and-out-of-a-variable.md)
- [<span data-ttu-id="fa388-153">数据类型</span><span class="sxs-lookup"><span data-stu-id="fa388-153">Data Types</span></span>](../../../language-reference/data-types/index.md)
- [<span data-ttu-id="fa388-154">Protected</span><span class="sxs-lookup"><span data-stu-id="fa388-154">Protected</span></span>](../../../language-reference/modifiers/protected.md)
- [<span data-ttu-id="fa388-155">Friend</span><span class="sxs-lookup"><span data-stu-id="fa388-155">Friend</span></span>](../../../language-reference/modifiers/friend.md)
- [<span data-ttu-id="fa388-156">静态</span><span class="sxs-lookup"><span data-stu-id="fa388-156">Static</span></span>](../../../language-reference/modifiers/static.md)
- [<span data-ttu-id="fa388-157">已声明元素的特性</span><span class="sxs-lookup"><span data-stu-id="fa388-157">Declared Element Characteristics</span></span>](../declared-elements/declared-element-characteristics.md)
- [<span data-ttu-id="fa388-158">局部类型推理</span><span class="sxs-lookup"><span data-stu-id="fa388-158">Local Type Inference</span></span>](local-type-inference.md)
- [<span data-ttu-id="fa388-159">Option Infer 语句</span><span class="sxs-lookup"><span data-stu-id="fa388-159">Option Infer Statement</span></span>](../../../language-reference/statements/option-infer-statement.md)
