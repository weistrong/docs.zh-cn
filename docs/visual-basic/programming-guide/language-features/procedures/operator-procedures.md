---
description: '详细了解：运算符过程 (Visual Basic) '
title: 运算符过程
ms.date: 07/20/2015
helpviewer_keywords:
- Visual Basic code, procedures
- procedures [Visual Basic], operator
- Visual Basic code, operators
- syntax [Visual Basic], Operator procedures
- operators [Visual Basic], overloading
- overloaded operators [Visual Basic]
- operator overloading
- operator procedures
ms.assetid: 8c513d38-246b-4fb7-8b75-29e1364e555b
ms.openlocfilehash: 836eeb2e705a96c49b5fa53e277ccf025d1915b2
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100479954"
---
# <a name="operator-procedures-visual-basic"></a><span data-ttu-id="1d286-103">运算符过程 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="1d286-103">Operator Procedures (Visual Basic)</span></span>

<span data-ttu-id="1d286-104">运算符过程是一系列 Visual Basic 语句，这些语句定义标准 (运算符的行为（例如 `*` ， `<>` 或 `And` 已定义的类或结构中的、或) ）。</span><span class="sxs-lookup"><span data-stu-id="1d286-104">An operator procedure is a series of Visual Basic statements that define the behavior of a standard operator (such as `*`, `<>`, or `And`) on a class or structure you have defined.</span></span> <span data-ttu-id="1d286-105">这也称为 *运算符重载*。</span><span class="sxs-lookup"><span data-stu-id="1d286-105">This is also called *operator overloading*.</span></span>

## <a name="when-to-define-operator-procedures"></a><span data-ttu-id="1d286-106">何时定义操作员过程</span><span class="sxs-lookup"><span data-stu-id="1d286-106">When to Define Operator Procedures</span></span>

<span data-ttu-id="1d286-107">定义了类或结构后，可以将变量声明为该类或结构的类型。</span><span class="sxs-lookup"><span data-stu-id="1d286-107">When you have defined a class or structure, you can declare variables to be of the type of that class or structure.</span></span> <span data-ttu-id="1d286-108">有时，此类变量需要作为表达式的一部分参与操作。</span><span class="sxs-lookup"><span data-stu-id="1d286-108">Sometimes such a variable needs to participate in an operation as part of an expression.</span></span> <span data-ttu-id="1d286-109">为此，它必须是运算符的操作数。</span><span class="sxs-lookup"><span data-stu-id="1d286-109">To do this, it must be an operand of an operator.</span></span>

<span data-ttu-id="1d286-110">Visual Basic 仅定义其基本数据类型的运算符。</span><span class="sxs-lookup"><span data-stu-id="1d286-110">Visual Basic defines operators only on its fundamental data types.</span></span> <span data-ttu-id="1d286-111">如果两个操作数或其中一个操作数为类或结构的类型，则可以定义运算符的行为。</span><span class="sxs-lookup"><span data-stu-id="1d286-111">You can define the behavior of an operator when one or both of the operands are of the type of your class or structure.</span></span>

<span data-ttu-id="1d286-112">有关详细信息，请参阅 [Operator 语句](../../../language-reference/statements/operator-statement.md)。</span><span class="sxs-lookup"><span data-stu-id="1d286-112">For more information, see [Operator Statement](../../../language-reference/statements/operator-statement.md).</span></span>

## <a name="types-of-operator-procedure"></a><span data-ttu-id="1d286-113">运算符过程的类型</span><span class="sxs-lookup"><span data-stu-id="1d286-113">Types of Operator Procedure</span></span>

<span data-ttu-id="1d286-114">操作员过程可以是以下类型之一：</span><span class="sxs-lookup"><span data-stu-id="1d286-114">An operator procedure can be one of the following types:</span></span>

- <span data-ttu-id="1d286-115">一元运算符的定义，其中的参数是你的类或结构的类型。</span><span class="sxs-lookup"><span data-stu-id="1d286-115">A definition of a unary operator where the argument is of the type of your class or structure.</span></span>

- <span data-ttu-id="1d286-116">二元运算符的定义，其中至少有一个参数是你的类或结构的类型。</span><span class="sxs-lookup"><span data-stu-id="1d286-116">A definition of a binary operator where at least one of the arguments is of the type of your class or structure.</span></span>

- <span data-ttu-id="1d286-117">转换运算符的定义，其中的参数属于你的类或结构的类型。</span><span class="sxs-lookup"><span data-stu-id="1d286-117">A definition of a conversion operator where the argument is of the type of your class or structure.</span></span>

- <span data-ttu-id="1d286-118">返回类或结构的类型的转换运算符的定义。</span><span class="sxs-lookup"><span data-stu-id="1d286-118">A definition of a conversion operator that returns the type of your class or structure.</span></span>

 <span data-ttu-id="1d286-119">转换运算符始终为一元运算符，并且你始终使用 `CType` 作为正在定义的运算符。</span><span class="sxs-lookup"><span data-stu-id="1d286-119">Conversion operators are always unary, and you always use `CType` as the operator you are defining.</span></span>

## <a name="declaration-syntax"></a><span data-ttu-id="1d286-120">声明语法</span><span class="sxs-lookup"><span data-stu-id="1d286-120">Declaration Syntax</span></span>

<span data-ttu-id="1d286-121">声明运算符过程的语法如下所示：</span><span class="sxs-lookup"><span data-stu-id="1d286-121">The syntax for declaring an operator procedure is as follows:</span></span>

```vb
Public Shared [Widening | Narrowing] Operator operatorsymbol ( operand1 [,  operand2 ]) As datatype

' Statements of the operator procedure.

End Operator
```

<span data-ttu-id="1d286-122">`Widening` `Narrowing` 仅对类型转换运算符使用或关键字。</span><span class="sxs-lookup"><span data-stu-id="1d286-122">You use the `Widening` or `Narrowing` keyword only on a type conversion operator.</span></span> <span data-ttu-id="1d286-123">对于类型转换运算符，运算符符号始终是 [CType 函数](../../../language-reference/functions/ctype-function.md) 。</span><span class="sxs-lookup"><span data-stu-id="1d286-123">The operator symbol is always [CType Function](../../../language-reference/functions/ctype-function.md) for a type conversion operator.</span></span>

<span data-ttu-id="1d286-124">您可以声明两个操作数来定义一个二元运算符，并声明一个操作数来定义一元运算符，包括类型转换运算符。</span><span class="sxs-lookup"><span data-stu-id="1d286-124">You declare two operands to define a binary operator, and you declare one operand to define a unary operator, including a type conversion operator.</span></span> <span data-ttu-id="1d286-125">必须声明所有操作数 `ByVal` 。</span><span class="sxs-lookup"><span data-stu-id="1d286-125">All operands must be declared `ByVal`.</span></span>

<span data-ttu-id="1d286-126">声明每个操作数的方式与声明 [Sub 过程](./sub-procedures.md)的参数的方式相同。</span><span class="sxs-lookup"><span data-stu-id="1d286-126">You declare each operand the same way you declare parameters for [Sub Procedures](./sub-procedures.md).</span></span>

### <a name="data-type"></a><span data-ttu-id="1d286-127">数据类型</span><span class="sxs-lookup"><span data-stu-id="1d286-127">Data Type</span></span>

<span data-ttu-id="1d286-128">由于你在定义的类或结构上定义运算符，因此至少一个操作数必须是该类或结构的数据类型。</span><span class="sxs-lookup"><span data-stu-id="1d286-128">Because you are defining an operator on a class or structure you have defined, at least one of the operands must be of the data type of that class or structure.</span></span> <span data-ttu-id="1d286-129">对于类型转换运算符，操作数或返回类型必须是类或结构的数据类型。</span><span class="sxs-lookup"><span data-stu-id="1d286-129">For a type conversion operator, either the operand or the return type must be of the data type of the class or structure.</span></span>

<span data-ttu-id="1d286-130">有关更多详细信息，请参阅 [Operator 语句](../../../language-reference/statements/operator-statement.md)。</span><span class="sxs-lookup"><span data-stu-id="1d286-130">For more details, see [Operator Statement](../../../language-reference/statements/operator-statement.md).</span></span>

## <a name="calling-syntax"></a><span data-ttu-id="1d286-131">调用语法</span><span class="sxs-lookup"><span data-stu-id="1d286-131">Calling Syntax</span></span>

<span data-ttu-id="1d286-132">通过在表达式中使用运算符符号，可以隐式调用运算符过程。</span><span class="sxs-lookup"><span data-stu-id="1d286-132">You invoke an operator procedure implicitly by using the operator symbol in an expression.</span></span> <span data-ttu-id="1d286-133">提供操作数的方式与预定义运算符相同。</span><span class="sxs-lookup"><span data-stu-id="1d286-133">You supply the operands the same way you do for predefined operators.</span></span>

<span data-ttu-id="1d286-134">对运算符过程的隐式调用的语法如下所示：</span><span class="sxs-lookup"><span data-stu-id="1d286-134">The syntax for an implicit call to an operator procedure is as follows:</span></span>

<span data-ttu-id="1d286-135">`Dim testStruct As`  *structurename*</span><span class="sxs-lookup"><span data-stu-id="1d286-135">`Dim testStruct As`  *structurename*</span></span>

<span data-ttu-id="1d286-136">`Dim testNewStruct As`  *structurename* `= testStruct`*operatorsymbol*      `10`</span><span class="sxs-lookup"><span data-stu-id="1d286-136">`Dim testNewStruct As`  *structurename*  `= testStruct`  *operatorsymbol*  `10`</span></span>

### <a name="illustration-of-declaration-and-call"></a><span data-ttu-id="1d286-137">声明和调用的插图</span><span class="sxs-lookup"><span data-stu-id="1d286-137">Illustration of Declaration and Call</span></span>

<span data-ttu-id="1d286-138">下面的结构将已签名的128位整数值存储为构成的高序位和低序位部分。</span><span class="sxs-lookup"><span data-stu-id="1d286-138">The following structure stores a signed 128-bit integer value as the constituent high-order and low-order parts.</span></span> <span data-ttu-id="1d286-139">它定义 `+` 运算符以添加两个 `veryLong` 值并生成一个结果 `veryLong` 值。</span><span class="sxs-lookup"><span data-stu-id="1d286-139">It defines the `+` operator to add two `veryLong` values and generate a resulting `veryLong` value.</span></span>

[!code-vb[VbVbcnProcedures#23](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnProcedures/VB/Class1.vb#23)]

<span data-ttu-id="1d286-140">下面的示例演示对 `+` 上定义的运算符的典型调用 `veryLong` 。</span><span class="sxs-lookup"><span data-stu-id="1d286-140">The following example shows a typical call to the `+` operator defined on `veryLong`.</span></span>

[!code-vb[VbVbcnProcedures#24](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnProcedures/VB/Class1.vb#24)]

## <a name="see-also"></a><span data-ttu-id="1d286-141">请参阅</span><span class="sxs-lookup"><span data-stu-id="1d286-141">See also</span></span>

- [<span data-ttu-id="1d286-142">过程</span><span class="sxs-lookup"><span data-stu-id="1d286-142">Procedures</span></span>](./index.md)
- [<span data-ttu-id="1d286-143">Sub 过程</span><span class="sxs-lookup"><span data-stu-id="1d286-143">Sub Procedures</span></span>](./sub-procedures.md)
- [<span data-ttu-id="1d286-144">Function 过程</span><span class="sxs-lookup"><span data-stu-id="1d286-144">Function Procedures</span></span>](./function-procedures.md)
- [<span data-ttu-id="1d286-145">Property 过程</span><span class="sxs-lookup"><span data-stu-id="1d286-145">Property Procedures</span></span>](./property-procedures.md)
- [<span data-ttu-id="1d286-146">过程形参和实参</span><span class="sxs-lookup"><span data-stu-id="1d286-146">Procedure Parameters and Arguments</span></span>](./procedure-parameters-and-arguments.md)
- [<span data-ttu-id="1d286-147">Operator Statement</span><span class="sxs-lookup"><span data-stu-id="1d286-147">Operator Statement</span></span>](../../../language-reference/statements/operator-statement.md)
- [<span data-ttu-id="1d286-148">如何：定义运算符</span><span class="sxs-lookup"><span data-stu-id="1d286-148">How to: Define an Operator</span></span>](./how-to-define-an-operator.md)
- [<span data-ttu-id="1d286-149">如何：定义转换运算符</span><span class="sxs-lookup"><span data-stu-id="1d286-149">How to: Define a Conversion Operator</span></span>](./how-to-define-a-conversion-operator.md)
- [<span data-ttu-id="1d286-150">如何：调用运算符过程</span><span class="sxs-lookup"><span data-stu-id="1d286-150">How to: Call an Operator Procedure</span></span>](./how-to-call-an-operator-procedure.md)
- [<span data-ttu-id="1d286-151">如何：使用定义运算符的类</span><span class="sxs-lookup"><span data-stu-id="1d286-151">How to: Use a Class that Defines Operators</span></span>](./how-to-use-a-class-that-defines-operators.md)
