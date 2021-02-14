---
description: '了解 (Visual Basic 的函数过程的详细信息) '
title: Function 过程
ms.date: 07/20/2015
helpviewer_keywords:
- Function procedures
- return values [Visual Basic], function procedures
- Visual Basic code, procedures
- procedures [Visual Basic], calling
- procedures [Visual Basic], Function procedures
- syntax [Visual Basic], function procedures
ms.assetid: 1b9f632c-553b-4cb6-920a-ded117ead8c0
ms.openlocfilehash: 4997059fc33fb5d438519356b2c9fdd9e6a27cce
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100436144"
---
# <a name="function-procedures-visual-basic"></a><span data-ttu-id="051bc-103">函数过程 (Visual Basic) </span><span class="sxs-lookup"><span data-stu-id="051bc-103">Function procedures (Visual Basic)</span></span>

<span data-ttu-id="051bc-104">`Function`过程是由和语句括起来的一系列 Visual Basic `Function` 语句 `End Function` 。</span><span class="sxs-lookup"><span data-stu-id="051bc-104">A `Function` procedure is a series of Visual Basic statements enclosed by the `Function` and `End Function` statements.</span></span> <span data-ttu-id="051bc-105">该 `Function` 过程执行任务，然后将控制权返回给调用代码。</span><span class="sxs-lookup"><span data-stu-id="051bc-105">The `Function` procedure performs a task and then returns control to the calling code.</span></span> <span data-ttu-id="051bc-106">当它返回 control 时，它还会将值返回到调用代码。</span><span class="sxs-lookup"><span data-stu-id="051bc-106">When it returns control, it also returns a value to the calling code.</span></span>

<span data-ttu-id="051bc-107">每次调用该过程时，其语句都会运行，从语句后面的第一个可执行语句开始， `Function` 到遇到的第一个 `End Function` 、 `Exit Function` 或 `Return` 语句结束。</span><span class="sxs-lookup"><span data-stu-id="051bc-107">Each time the procedure is called, its statements run, starting with the first executable statement after the `Function` statement and ending with the first `End Function`, `Exit Function`, or `Return` statement encountered.</span></span>

<span data-ttu-id="051bc-108">您可以 `Function` 在模块、类或结构中定义过程。</span><span class="sxs-lookup"><span data-stu-id="051bc-108">You can define a `Function` procedure in a module, class, or structure.</span></span> <span data-ttu-id="051bc-109">`Public`默认情况下，这意味着您可以从应用程序中可以访问您定义它的模块、类或结构的任何位置调用它。</span><span class="sxs-lookup"><span data-stu-id="051bc-109">It is `Public` by default, which means you can call it from anywhere in your application that has access to the module, class, or structure in which you defined it.</span></span>

<span data-ttu-id="051bc-110">`Function`过程可以采用由调用代码传递给它的参数，如常量、变量或表达式。</span><span class="sxs-lookup"><span data-stu-id="051bc-110">A `Function` procedure can take arguments, such as constants, variables, or expressions, which are passed to it by the calling code.</span></span>

## <a name="declaration-syntax"></a><span data-ttu-id="051bc-111">声明语法</span><span class="sxs-lookup"><span data-stu-id="051bc-111">Declaration syntax</span></span>

<span data-ttu-id="051bc-112">声明过程的语法如下所示 `Function` ：</span><span class="sxs-lookup"><span data-stu-id="051bc-112">The syntax for declaring a `Function` procedure is as follows:</span></span>

```vb
[Modifiers] Function FunctionName [(ParameterList)] As ReturnType
    [Statements]
End Function
```

<span data-ttu-id="051bc-113">*修饰符* 可以指定有关重载、重写、共享和隐藏的访问级别和信息。</span><span class="sxs-lookup"><span data-stu-id="051bc-113">The *modifiers* can specify access level and information regarding overloading, overriding, sharing, and shadowing.</span></span> <span data-ttu-id="051bc-114">有关详细信息，请参阅 [函数语句](../../../language-reference/statements/function-statement.md)。</span><span class="sxs-lookup"><span data-stu-id="051bc-114">For more information, see [Function Statement](../../../language-reference/statements/function-statement.md).</span></span>

<span data-ttu-id="051bc-115">声明每个参数的方式与处理 [Sub 过程](./sub-procedures.md)的方式相同。</span><span class="sxs-lookup"><span data-stu-id="051bc-115">You declare each parameter the same way you do for [Sub Procedures](./sub-procedures.md).</span></span>

### <a name="data-type"></a><span data-ttu-id="051bc-116">数据类型</span><span class="sxs-lookup"><span data-stu-id="051bc-116">Data type</span></span>

<span data-ttu-id="051bc-117">每个 `Function` 过程都有一种数据类型，就像每个变量一样。</span><span class="sxs-lookup"><span data-stu-id="051bc-117">Every `Function` procedure has a data type, just as every variable does.</span></span> <span data-ttu-id="051bc-118">此数据类型由 `As` 语句中的子句指定 `Function` ，它确定函数返回到调用代码的值的数据类型。</span><span class="sxs-lookup"><span data-stu-id="051bc-118">This data type is specified by the `As` clause in the `Function` statement, and it determines the data type of the value the function returns to the calling code.</span></span> <span data-ttu-id="051bc-119">下面的示例声明阐释了这一点。</span><span class="sxs-lookup"><span data-stu-id="051bc-119">The following sample declarations illustrate this.</span></span>

```vb
Function Yesterday() As Date
End Function

Function FindSqrt(radicand As Single) As Single
End Function
```

<span data-ttu-id="051bc-120">有关详细信息，请参阅 [Function 语句](../../../language-reference/statements/function-statement.md)中的 "part"。</span><span class="sxs-lookup"><span data-stu-id="051bc-120">For more information, see "Parts" in [Function Statement](../../../language-reference/statements/function-statement.md).</span></span>

### <a name="returning-values"></a><span data-ttu-id="051bc-121">返回值</span><span class="sxs-lookup"><span data-stu-id="051bc-121">Returning values</span></span>

<span data-ttu-id="051bc-122">`Function`过程返回到调用代码的值称为其返回值。</span><span class="sxs-lookup"><span data-stu-id="051bc-122">The value a `Function` procedure sends back to the calling code is called its return value.</span></span> <span data-ttu-id="051bc-123">此过程通过以下两种方式之一返回此值：</span><span class="sxs-lookup"><span data-stu-id="051bc-123">The procedure returns this value in one of two ways:</span></span>

- <span data-ttu-id="051bc-124">它使用 `Return` 语句来指定返回值，并立即将控制权返回给调用程序。</span><span class="sxs-lookup"><span data-stu-id="051bc-124">It uses the `Return` statement to specify the return value, and returns control immediately to the calling program.</span></span> <span data-ttu-id="051bc-125">下面的示例对此进行了演示。</span><span class="sxs-lookup"><span data-stu-id="051bc-125">The following example illustrates this.</span></span>

  ```vb
  Function FunctionName [(ParameterList)] As ReturnType
      ' The following statement immediately transfers control back
      ' to the calling code and returns the value of Expression.
      Return Expression
  End Function
  ```

- <span data-ttu-id="051bc-126">它在过程的一个或多个语句中为其自己的函数名称赋值。</span><span class="sxs-lookup"><span data-stu-id="051bc-126">It assigns a value to its own function name in one or more statements of the procedure.</span></span> <span data-ttu-id="051bc-127">直到 `Exit Function` 执行或语句后，控件才会返回到调用程序 `End Function` 。</span><span class="sxs-lookup"><span data-stu-id="051bc-127">Control does not return to the calling program until an `Exit Function` or `End Function` statement is executed.</span></span> <span data-ttu-id="051bc-128">下面的示例对此进行了演示。</span><span class="sxs-lookup"><span data-stu-id="051bc-128">The following example illustrates this.</span></span>

  ```vb
  Function FunctionName [(ParameterList)] As ReturnType
      ' The following statement does not transfer control back to the calling code.
      FunctionName = Expression
      ' When control returns to the calling code, Expression is the return value.
  End Function
  ```

<span data-ttu-id="051bc-129">将返回值分配给函数名称的优点是，在遇到或语句之前，控件不会从过程返回 `Exit Function` `End Function` 。</span><span class="sxs-lookup"><span data-stu-id="051bc-129">The advantage of assigning the return value to the function name is that control does not return from the procedure until it encounters an `Exit Function` or `End Function` statement.</span></span> <span data-ttu-id="051bc-130">这使您可以分配一个初步的值并在以后必要时进行调整。</span><span class="sxs-lookup"><span data-stu-id="051bc-130">This allows you to assign a preliminary value and adjust it later if necessary.</span></span>

<span data-ttu-id="051bc-131">有关返回值的详细信息，请参阅 [函数语句](../../../language-reference/statements/function-statement.md)。</span><span class="sxs-lookup"><span data-stu-id="051bc-131">For more information about returning values, see [Function Statement](../../../language-reference/statements/function-statement.md).</span></span> <span data-ttu-id="051bc-132">有关返回数组的信息，请参阅 [数组](../arrays/index.md)。</span><span class="sxs-lookup"><span data-stu-id="051bc-132">For information about returning arrays, see [Arrays](../arrays/index.md).</span></span>

## <a name="calling-syntax"></a><span data-ttu-id="051bc-133">调用语法</span><span class="sxs-lookup"><span data-stu-id="051bc-133">Calling syntax</span></span>

<span data-ttu-id="051bc-134">`Function`通过在赋值语句或表达式的右侧包含其名称和参数来调用过程。</span><span class="sxs-lookup"><span data-stu-id="051bc-134">You invoke a `Function` procedure by including its name and arguments either on the right side of an assignment statement or in an expression.</span></span> <span data-ttu-id="051bc-135">必须为所有非可选参数提供值，并且必须将参数列表括在括号中。</span><span class="sxs-lookup"><span data-stu-id="051bc-135">You must provide values for all arguments that are not optional, and you must enclose the argument list in parentheses.</span></span> <span data-ttu-id="051bc-136">如果未提供任何参数，则可以选择省略括号。</span><span class="sxs-lookup"><span data-stu-id="051bc-136">If no arguments are supplied, you can optionally omit the parentheses.</span></span>

<span data-ttu-id="051bc-137">对过程的调用语法如下所示 `Function` 。</span><span class="sxs-lookup"><span data-stu-id="051bc-137">The syntax for a call to a `Function` procedure is as follows.</span></span>

<span data-ttu-id="051bc-138">*lvalue* `=`*functionname* `[(`*argumentlist*    `)]`</span><span class="sxs-lookup"><span data-stu-id="051bc-138">*lvalue*  `=`  *functionname* `[(` *argumentlist* `)]`</span></span>

<span data-ttu-id="051bc-139">`If ((`*functionname* `[(`*argumentlist* `)] / 3) <=`*表达式*  `) Then`</span><span class="sxs-lookup"><span data-stu-id="051bc-139">`If ((` *functionname* `[(` *argumentlist* `)] / 3) <=`  *expression* `) Then`</span></span>

<span data-ttu-id="051bc-140">调用 `Function` 过程时，无需使用其返回值。</span><span class="sxs-lookup"><span data-stu-id="051bc-140">When you call a `Function` procedure, you do not have to use its return value.</span></span> <span data-ttu-id="051bc-141">否则，将执行该函数的所有操作，但将忽略返回值。</span><span class="sxs-lookup"><span data-stu-id="051bc-141">If you do not, all the actions of the function are performed, but the return value is ignored.</span></span> <span data-ttu-id="051bc-142"><xref:Microsoft.VisualBasic.Interaction.MsgBox%2A> 通常以这种方式调用。</span><span class="sxs-lookup"><span data-stu-id="051bc-142"><xref:Microsoft.VisualBasic.Interaction.MsgBox%2A> is often called in this manner.</span></span>

### <a name="illustration-of-declaration-and-call"></a><span data-ttu-id="051bc-143">声明和调用的插图</span><span class="sxs-lookup"><span data-stu-id="051bc-143">Illustration of declaration and call</span></span>

<span data-ttu-id="051bc-144">下面的 `Function` 过程计算直角三角形的最长边（或斜边），并给出另一方的值。</span><span class="sxs-lookup"><span data-stu-id="051bc-144">The following `Function` procedure calculates the longest side, or hypotenuse, of a right triangle, given the values for the other two sides.</span></span>

[!code-vb[VbVbcnProcedures#1](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnProcedures/VB/Class1.vb#1)]

<span data-ttu-id="051bc-145">下面的示例演示对的典型调用 `hypotenuse` 。</span><span class="sxs-lookup"><span data-stu-id="051bc-145">The following example shows a typical call to `hypotenuse`.</span></span>

[!code-vb[VbVbcnProcedures#6](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnProcedures/VB/Class1.vb#6)]

## <a name="see-also"></a><span data-ttu-id="051bc-146">请参阅</span><span class="sxs-lookup"><span data-stu-id="051bc-146">See also</span></span>

- [<span data-ttu-id="051bc-147">过程</span><span class="sxs-lookup"><span data-stu-id="051bc-147">Procedures</span></span>](./index.md)
- [<span data-ttu-id="051bc-148">Sub 过程</span><span class="sxs-lookup"><span data-stu-id="051bc-148">Sub Procedures</span></span>](./sub-procedures.md)
- [<span data-ttu-id="051bc-149">Property 过程</span><span class="sxs-lookup"><span data-stu-id="051bc-149">Property Procedures</span></span>](./property-procedures.md)
- [<span data-ttu-id="051bc-150">运算符过程</span><span class="sxs-lookup"><span data-stu-id="051bc-150">Operator Procedures</span></span>](./operator-procedures.md)
- [<span data-ttu-id="051bc-151">过程形参和实参</span><span class="sxs-lookup"><span data-stu-id="051bc-151">Procedure Parameters and Arguments</span></span>](./procedure-parameters-and-arguments.md)
- [<span data-ttu-id="051bc-152">Function 语句</span><span class="sxs-lookup"><span data-stu-id="051bc-152">Function Statement</span></span>](../../../language-reference/statements/function-statement.md)
- [<span data-ttu-id="051bc-153">如何：创建返回值的过程</span><span class="sxs-lookup"><span data-stu-id="051bc-153">How to: Create a Procedure that Returns a Value</span></span>](./how-to-create-a-procedure-that-returns-a-value.md)
- [<span data-ttu-id="051bc-154">如何：从过程返回值</span><span class="sxs-lookup"><span data-stu-id="051bc-154">How to: Return a Value from a Procedure</span></span>](./how-to-return-a-value-from-a-procedure.md)
- [<span data-ttu-id="051bc-155">如何：调用返回值的过程</span><span class="sxs-lookup"><span data-stu-id="051bc-155">How to: Call a Procedure That Returns a Value</span></span>](./how-to-call-a-procedure-that-returns-a-value.md)
