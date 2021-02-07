---
description: '了解详细信息：参数列表 (Visual Basic) '
title: 参数列表
ms.date: 07/20/2015
helpviewer_keywords:
- Visual Basic code, procedures
- parameters [Visual Basic], Visual Basic
- parameters [Visual Basic], lists
- parameter lists [Visual Basic]
- Visual Basic code, parameter lists
- arguments [Visual Basic], Visual Basic
- procedures [Visual Basic], parameter lists
ms.assetid: 5d737319-0c34-4df9-a23d-188fc840becd
ms.openlocfilehash: f69063fac82887ba4da3119d8ec4fcac11b7f4c9
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99741401"
---
# <a name="parameter-list-visual-basic"></a><span data-ttu-id="59bf5-103">参数列表 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="59bf5-103">Parameter List (Visual Basic)</span></span>

<span data-ttu-id="59bf5-104">指定在调用过程时过程需要的参数。</span><span class="sxs-lookup"><span data-stu-id="59bf5-104">Specifies the parameters a procedure expects when it is called.</span></span> <span data-ttu-id="59bf5-105">多个参数之间用逗号分隔。</span><span class="sxs-lookup"><span data-stu-id="59bf5-105">Multiple parameters are separated by commas.</span></span> <span data-ttu-id="59bf5-106">下面是一个参数的语法。</span><span class="sxs-lookup"><span data-stu-id="59bf5-106">The following is the syntax for one parameter.</span></span>

## <a name="syntax"></a><span data-ttu-id="59bf5-107">语法</span><span class="sxs-lookup"><span data-stu-id="59bf5-107">Syntax</span></span>

```vb
[ <attributelist> ] [ Optional ] [{ ByVal | ByRef }] [ ParamArray ]
parametername[( )] [ As parametertype ] [ = defaultvalue ]
```

## <a name="parts"></a><span data-ttu-id="59bf5-108">组成部分</span><span class="sxs-lookup"><span data-stu-id="59bf5-108">Parts</span></span>

`attributelist`  
<span data-ttu-id="59bf5-109">可选。</span><span class="sxs-lookup"><span data-stu-id="59bf5-109">Optional.</span></span> <span data-ttu-id="59bf5-110">应用于此参数的特性列表。</span><span class="sxs-lookup"><span data-stu-id="59bf5-110">List of attributes that apply to this parameter.</span></span> <span data-ttu-id="59bf5-111">必须将 [属性列表](attribute-list.md) 用尖括号括起来 ( " `<` " 和 " `>` " ) 。</span><span class="sxs-lookup"><span data-stu-id="59bf5-111">You must enclose the [Attribute List](attribute-list.md) in angle brackets ("`<`" and "`>`").</span></span>

`Optional`  
<span data-ttu-id="59bf5-112">可选。</span><span class="sxs-lookup"><span data-stu-id="59bf5-112">Optional.</span></span> <span data-ttu-id="59bf5-113">指定在调用过程时不需要此参数。</span><span class="sxs-lookup"><span data-stu-id="59bf5-113">Specifies that this parameter is not required when the procedure is called.</span></span>

`ByVal`  
<span data-ttu-id="59bf5-114">可选。</span><span class="sxs-lookup"><span data-stu-id="59bf5-114">Optional.</span></span> <span data-ttu-id="59bf5-115">指定过程不能替换或重新分配调用代码中的相应参数的基础变量元素。</span><span class="sxs-lookup"><span data-stu-id="59bf5-115">Specifies that the procedure cannot replace or reassign the variable element underlying the corresponding argument in the calling code.</span></span>

`ByRef`  
<span data-ttu-id="59bf5-116">可选。</span><span class="sxs-lookup"><span data-stu-id="59bf5-116">Optional.</span></span> <span data-ttu-id="59bf5-117">指定过程可以采用与调用代码本身相同的方式来修改调用代码中的基础变量元素。</span><span class="sxs-lookup"><span data-stu-id="59bf5-117">Specifies that the procedure can modify the underlying variable element in the calling code the same way the calling code itself can.</span></span>

`ParamArray`  
<span data-ttu-id="59bf5-118">可选。</span><span class="sxs-lookup"><span data-stu-id="59bf5-118">Optional.</span></span> <span data-ttu-id="59bf5-119">指定参数列表中的最后一个参数是指定数据类型的元素的可选数组。</span><span class="sxs-lookup"><span data-stu-id="59bf5-119">Specifies that the last parameter in the parameter list is an optional array of elements of the specified data type.</span></span> <span data-ttu-id="59bf5-120">这样，调用代码就可以将任意数量的参数传递给该过程。</span><span class="sxs-lookup"><span data-stu-id="59bf5-120">This lets the calling code pass an arbitrary number of arguments to the procedure.</span></span>

`parametername`  
<span data-ttu-id="59bf5-121">必需。</span><span class="sxs-lookup"><span data-stu-id="59bf5-121">Required.</span></span> <span data-ttu-id="59bf5-122">表示参数的局部变量的名称。</span><span class="sxs-lookup"><span data-stu-id="59bf5-122">Name of the local variable representing the parameter.</span></span>

`parametertype`  
<span data-ttu-id="59bf5-123">如果 `Option Strict` 为，则为必需 `On` 。</span><span class="sxs-lookup"><span data-stu-id="59bf5-123">Required if `Option Strict` is `On`.</span></span> <span data-ttu-id="59bf5-124">表示参数的局部变量的数据类型。</span><span class="sxs-lookup"><span data-stu-id="59bf5-124">Data type of the local variable representing the parameter.</span></span>

`defaultvalue`  
<span data-ttu-id="59bf5-125">参数需要 `Optional` 。</span><span class="sxs-lookup"><span data-stu-id="59bf5-125">Required for `Optional` parameters.</span></span> <span data-ttu-id="59bf5-126">计算结果为参数的数据类型的任何常量或常量表达式。</span><span class="sxs-lookup"><span data-stu-id="59bf5-126">Any constant or constant expression that evaluates to the data type of the parameter.</span></span> <span data-ttu-id="59bf5-127">如果类型为 `Object` ，或类、接口、数组或结构，则默认值只能是 `Nothing` 。</span><span class="sxs-lookup"><span data-stu-id="59bf5-127">If the type is `Object`, or a class, interface, array, or structure, the default value can only be `Nothing`.</span></span>

## <a name="remarks"></a><span data-ttu-id="59bf5-128">备注</span><span class="sxs-lookup"><span data-stu-id="59bf5-128">Remarks</span></span>

<span data-ttu-id="59bf5-129">参数括在括号内并用逗号分隔。</span><span class="sxs-lookup"><span data-stu-id="59bf5-129">Parameters are surrounded by parentheses and separated by commas.</span></span> <span data-ttu-id="59bf5-130">参数可以使用任何数据类型进行声明。</span><span class="sxs-lookup"><span data-stu-id="59bf5-130">A parameter can be declared with any data type.</span></span> <span data-ttu-id="59bf5-131">如果不指定 `parametertype` ，则默认为 `Object` 。</span><span class="sxs-lookup"><span data-stu-id="59bf5-131">If you do not specify `parametertype`, it defaults to `Object`.</span></span>

<span data-ttu-id="59bf5-132">当调用代码调用过程时，它会将 *参数* 传递给每个必需的参数。</span><span class="sxs-lookup"><span data-stu-id="59bf5-132">When the calling code calls the procedure, it passes an *argument* to each required parameter.</span></span> <span data-ttu-id="59bf5-133">有关详细信息，请参阅 [参数和参数之间的差异](../../programming-guide/language-features/procedures/differences-between-parameters-and-arguments.md)。</span><span class="sxs-lookup"><span data-stu-id="59bf5-133">For more information, see [Differences Between Parameters and Arguments](../../programming-guide/language-features/procedures/differences-between-parameters-and-arguments.md).</span></span>

<span data-ttu-id="59bf5-134">调用代码传递给每个参数的参数是指向调用代码中的基础元素的指针。</span><span class="sxs-lookup"><span data-stu-id="59bf5-134">The argument the calling code passes to each parameter is a pointer to an underlying element in the calling code.</span></span> <span data-ttu-id="59bf5-135">如果此元素不是常量、文字、枚举或表达式的 *变量* () ，则任何代码都无法更改它。</span><span class="sxs-lookup"><span data-stu-id="59bf5-135">If this element is *nonvariable* (a constant, literal, enumeration, or expression), it is impossible for any code to change it.</span></span> <span data-ttu-id="59bf5-136">如果它是 (声明的变量、字段、属性、数组元素或结构元素) 的 *可变* 元素，则调用代码可以更改它。</span><span class="sxs-lookup"><span data-stu-id="59bf5-136">If it is a *variable* element (a declared variable, field, property, array element, or structure element), the calling code can change it.</span></span> <span data-ttu-id="59bf5-137">有关详细信息，请参阅可 [修改和不可修改参数之间的差异](../../programming-guide/language-features/procedures/differences-between-modifiable-and-nonmodifiable-arguments.md)。</span><span class="sxs-lookup"><span data-stu-id="59bf5-137">For more information, see [Differences Between Modifiable and Nonmodifiable Arguments](../../programming-guide/language-features/procedures/differences-between-modifiable-and-nonmodifiable-arguments.md).</span></span>

<span data-ttu-id="59bf5-138">如果传递了 variable 元素 `ByRef` ，则该过程也可以更改它。</span><span class="sxs-lookup"><span data-stu-id="59bf5-138">If a variable element is passed `ByRef`, the procedure can change it as well.</span></span> <span data-ttu-id="59bf5-139">有关详细信息，请参阅 [按值传递参数和通过引用传递参数之间的差异](../../programming-guide/language-features/procedures/differences-between-passing-an-argument-by-value-and-by-reference.md)。</span><span class="sxs-lookup"><span data-stu-id="59bf5-139">For more information, see [Differences Between Passing an Argument By Value and By Reference](../../programming-guide/language-features/procedures/differences-between-passing-an-argument-by-value-and-by-reference.md).</span></span>

## <a name="rules"></a><span data-ttu-id="59bf5-140">规则</span><span class="sxs-lookup"><span data-stu-id="59bf5-140">Rules</span></span>

- <span data-ttu-id="59bf5-141">**括号.**</span><span class="sxs-lookup"><span data-stu-id="59bf5-141">**Parentheses.**</span></span> <span data-ttu-id="59bf5-142">如果指定参数列表，则必须将其括在括号中。</span><span class="sxs-lookup"><span data-stu-id="59bf5-142">If you specify a parameter list, you must enclose it in parentheses.</span></span> <span data-ttu-id="59bf5-143">如果没有参数，仍可使用括空列表的括号。</span><span class="sxs-lookup"><span data-stu-id="59bf5-143">If there are no parameters, you can still use parentheses enclosing an empty list.</span></span> <span data-ttu-id="59bf5-144">这可以通过阐明元素是一个过程来提高代码的可读性。</span><span class="sxs-lookup"><span data-stu-id="59bf5-144">This improves the readability of your code by clarifying that the element is a procedure.</span></span>

- <span data-ttu-id="59bf5-145">**可选参数。**</span><span class="sxs-lookup"><span data-stu-id="59bf5-145">**Optional Parameters.**</span></span> <span data-ttu-id="59bf5-146">如果对参数使用 `Optional` 修饰符，则列表中的所有后续参数也必须是可选的，并且可以使用修饰符进行声明 `Optional` 。</span><span class="sxs-lookup"><span data-stu-id="59bf5-146">If you use the `Optional` modifier on a parameter, all subsequent parameters in the list must also be optional and be declared by using the `Optional` modifier.</span></span>

     <span data-ttu-id="59bf5-147">每个可选参数声明都必须提供 `defaultvalue` 子句。</span><span class="sxs-lookup"><span data-stu-id="59bf5-147">Every optional parameter declaration must supply the `defaultvalue` clause.</span></span>

     <span data-ttu-id="59bf5-148">有关详细信息，请参阅 [可选参数](../../programming-guide/language-features/procedures/optional-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="59bf5-148">For more information, see [Optional Parameters](../../programming-guide/language-features/procedures/optional-parameters.md).</span></span>

- <span data-ttu-id="59bf5-149">**参数数组。**</span><span class="sxs-lookup"><span data-stu-id="59bf5-149">**Parameter Arrays.**</span></span> <span data-ttu-id="59bf5-150">必须 `ByVal` 为 `ParamArray` 参数指定。</span><span class="sxs-lookup"><span data-stu-id="59bf5-150">You must specify `ByVal` for a `ParamArray` parameter.</span></span>

     <span data-ttu-id="59bf5-151">`Optional` `ParamArray` 在同一参数列表中不能同时使用和。</span><span class="sxs-lookup"><span data-stu-id="59bf5-151">You cannot use both `Optional` and `ParamArray` in the same parameter list.</span></span>

     <span data-ttu-id="59bf5-152">有关详细信息，请参阅 [参数数组](../../programming-guide/language-features/procedures/parameter-arrays.md)。</span><span class="sxs-lookup"><span data-stu-id="59bf5-152">For more information, see [Parameter Arrays](../../programming-guide/language-features/procedures/parameter-arrays.md).</span></span>

- <span data-ttu-id="59bf5-153">**传递机制。**</span><span class="sxs-lookup"><span data-stu-id="59bf5-153">**Passing Mechanism.**</span></span> <span data-ttu-id="59bf5-154">每个参数的默认机制为 `ByVal` ，这意味着过程无法更改基础变量元素。</span><span class="sxs-lookup"><span data-stu-id="59bf5-154">The default mechanism for every argument is `ByVal`, which means the procedure cannot change the underlying variable element.</span></span> <span data-ttu-id="59bf5-155">但是，如果该元素是引用类型，则该过程可以修改基础对象的内容或成员，即使它无法替换或重新分配对象本身。</span><span class="sxs-lookup"><span data-stu-id="59bf5-155">However, if the element is a reference type, the procedure can modify the contents or members of the underlying object, even though it cannot replace or reassign the object itself.</span></span>

- <span data-ttu-id="59bf5-156">**参数名称。**</span><span class="sxs-lookup"><span data-stu-id="59bf5-156">**Parameter Names.**</span></span> <span data-ttu-id="59bf5-157">如果参数的数据类型为数组，请在后面 `parametername` 紧跟括号。</span><span class="sxs-lookup"><span data-stu-id="59bf5-157">If the parameter's data type is an array, follow `parametername` immediately by parentheses.</span></span> <span data-ttu-id="59bf5-158">有关参数名称的详细信息，请参阅已 [声明的元素名称](../../programming-guide/language-features/declared-elements/declared-element-names.md)。</span><span class="sxs-lookup"><span data-stu-id="59bf5-158">For more information on parameter names, see [Declared Element Names](../../programming-guide/language-features/declared-elements/declared-element-names.md).</span></span>

## <a name="example"></a><span data-ttu-id="59bf5-159">示例</span><span class="sxs-lookup"><span data-stu-id="59bf5-159">Example</span></span>

<span data-ttu-id="59bf5-160">下面的示例演示了一个 `Function` 用于定义两个参数的过程。</span><span class="sxs-lookup"><span data-stu-id="59bf5-160">The following example shows a `Function` procedure that defines two parameters.</span></span>

[!code-vb[VbVbalrStatements#2](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStatements/VB/Class1.vb#2)]

## <a name="see-also"></a><span data-ttu-id="59bf5-161">请参阅</span><span class="sxs-lookup"><span data-stu-id="59bf5-161">See also</span></span>

- <xref:System.Runtime.InteropServices.DllImportAttribute>
- [<span data-ttu-id="59bf5-162">Function 语句</span><span class="sxs-lookup"><span data-stu-id="59bf5-162">Function Statement</span></span>](function-statement.md)
- [<span data-ttu-id="59bf5-163">Sub 语句</span><span class="sxs-lookup"><span data-stu-id="59bf5-163">Sub Statement</span></span>](sub-statement.md)
- [<span data-ttu-id="59bf5-164">Declare Statement</span><span class="sxs-lookup"><span data-stu-id="59bf5-164">Declare Statement</span></span>](declare-statement.md)
- [<span data-ttu-id="59bf5-165">Structure 语句</span><span class="sxs-lookup"><span data-stu-id="59bf5-165">Structure Statement</span></span>](structure-statement.md)
- [<span data-ttu-id="59bf5-166">Option Strict 语句</span><span class="sxs-lookup"><span data-stu-id="59bf5-166">Option Strict Statement</span></span>](option-strict-statement.md)
- [<span data-ttu-id="59bf5-167">属性概述</span><span class="sxs-lookup"><span data-stu-id="59bf5-167">Attributes overview</span></span>](../../programming-guide/concepts/attributes/index.md)
- [<span data-ttu-id="59bf5-168">如何：在代码中拆分和合并语句</span><span class="sxs-lookup"><span data-stu-id="59bf5-168">How to: Break and Combine Statements in Code</span></span>](../../programming-guide/program-structure/how-to-break-and-combine-statements-in-code.md)
