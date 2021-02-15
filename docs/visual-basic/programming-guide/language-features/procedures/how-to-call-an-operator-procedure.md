---
description: '了解有关详细信息，请参阅如何：调用 Operator Procedure (Visual Basic) '
title: 如何：调用运算符过程
ms.date: 07/20/2015
helpviewer_keywords:
- operator procedures [Visual Basic], calling
- procedures [Visual Basic], operator
- procedure calls [Visual Basic], operator overloading
- syntax [Visual Basic], Operator procedures
- operators [Visual Basic], overloading
- return values [Visual Basic], Operator procedures
- overloaded operators [Visual Basic], calling
- operator overloading
ms.assetid: 0dce42cc-f0b0-4c14-9f62-018b21f33497
ms.openlocfilehash: f58d12ac5e4c9071646073184f7824946c00b39b
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100472600"
---
# <a name="how-to-call-an-operator-procedure-visual-basic"></a><span data-ttu-id="b40d9-103">如何：调用运算符过程 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="b40d9-103">How to: Call an Operator Procedure (Visual Basic)</span></span>

<span data-ttu-id="b40d9-104">在表达式中使用运算符符号调用运算符过程。</span><span class="sxs-lookup"><span data-stu-id="b40d9-104">You call an operator procedure by using the operator symbol in an expression.</span></span> <span data-ttu-id="b40d9-105">在转换运算符的情况下，调用 [CType 函数](../../../language-reference/functions/ctype-function.md) 将值从一种数据类型转换为另一种数据类型。</span><span class="sxs-lookup"><span data-stu-id="b40d9-105">In the case of a conversion operator, you call the [CType Function](../../../language-reference/functions/ctype-function.md) to convert a value from one data type to another.</span></span>  
  
 <span data-ttu-id="b40d9-106">不要显式调用运算符过程。</span><span class="sxs-lookup"><span data-stu-id="b40d9-106">You do not call operator procedures explicitly.</span></span> <span data-ttu-id="b40d9-107">只需在 `CType` 赋值语句或表达式中使用运算符（或函数），就像通常使用运算符的方法一样。</span><span class="sxs-lookup"><span data-stu-id="b40d9-107">You just use the operator, or the `CType` function, in an assignment statement or an expression, the same way you ordinarily use an operator.</span></span> <span data-ttu-id="b40d9-108">Visual Basic 调用运算符过程。</span><span class="sxs-lookup"><span data-stu-id="b40d9-108">Visual Basic makes the call to the operator procedure.</span></span>  
  
 <span data-ttu-id="b40d9-109">在类或结构上定义运算符也称为 *重载* 运算符。</span><span class="sxs-lookup"><span data-stu-id="b40d9-109">Defining an operator on a class or structure is also called *overloading* the operator.</span></span>  
  
### <a name="to-call-an-operator-procedure"></a><span data-ttu-id="b40d9-110">调用运算符过程</span><span class="sxs-lookup"><span data-stu-id="b40d9-110">To call an operator procedure</span></span>  
  
1. <span data-ttu-id="b40d9-111">用普通方法在表达式中使用运算符符号。</span><span class="sxs-lookup"><span data-stu-id="b40d9-111">Use the operator symbol in an expression in the ordinary way.</span></span>  
  
2. <span data-ttu-id="b40d9-112">确保操作数的数据类型适用于运算符，并按正确的顺序排列。</span><span class="sxs-lookup"><span data-stu-id="b40d9-112">Be sure the data types of the operands are appropriate for the operator, and in the correct order.</span></span>  
  
3. <span data-ttu-id="b40d9-113">运算符会按预期方式分配表达式的值。</span><span class="sxs-lookup"><span data-stu-id="b40d9-113">The operator contributes to the value of the expression as expected.</span></span>  
  
### <a name="to-call-a-conversion-operator-procedure"></a><span data-ttu-id="b40d9-114">调用转换运算符过程</span><span class="sxs-lookup"><span data-stu-id="b40d9-114">To call a conversion operator procedure</span></span>  
  
1. <span data-ttu-id="b40d9-115">`CType`在表达式中使用。</span><span class="sxs-lookup"><span data-stu-id="b40d9-115">Use `CType` inside an expression.</span></span>  
  
2. <span data-ttu-id="b40d9-116">确保操作数的数据类型适用于转换，并按正确的顺序排列。</span><span class="sxs-lookup"><span data-stu-id="b40d9-116">Be sure the data types of the operands are appropriate for the conversion, and in the correct order.</span></span>  
  
3. <span data-ttu-id="b40d9-117">`CType` 调用转换运算符过程，并返回转换后的值。</span><span class="sxs-lookup"><span data-stu-id="b40d9-117">`CType` calls the conversion operator procedure and returns the converted value.</span></span>  
  
## <a name="example"></a><span data-ttu-id="b40d9-118">示例</span><span class="sxs-lookup"><span data-stu-id="b40d9-118">Example</span></span>  

 <span data-ttu-id="b40d9-119">下面的示例创建两个 <xref:System.TimeSpan> 结构，将它们相加，然后将结果存储在第三个 <xref:System.TimeSpan> 结构中。</span><span class="sxs-lookup"><span data-stu-id="b40d9-119">The following example creates two <xref:System.TimeSpan> structures, adds them together, and stores the result in a third <xref:System.TimeSpan> structure.</span></span> <span data-ttu-id="b40d9-120"><xref:System.TimeSpan>结构定义运算符过程以重载多个标准运算符。</span><span class="sxs-lookup"><span data-stu-id="b40d9-120">The <xref:System.TimeSpan> structure defines operator procedures to overload several standard operators.</span></span>  
  
 [!code-vb[VbVbcnProcedures#29](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnProcedures/VB/Class1.vb#29)]  
  
 <span data-ttu-id="b40d9-121">由于 <xref:System.TimeSpan> 重载标准 `+` 运算符，因此当计算的值时，上面的示例将调用一个运算符过程 `combinedSpan` 。</span><span class="sxs-lookup"><span data-stu-id="b40d9-121">Because <xref:System.TimeSpan> overloads the standard `+` operator, the previous example calls an operator procedure when it calculates the value of `combinedSpan`.</span></span>  
  
 <span data-ttu-id="b40d9-122">有关调用会话运算符过程的示例，请参阅 [如何：使用定义运算符的类](./how-to-use-a-class-that-defines-operators.md)。</span><span class="sxs-lookup"><span data-stu-id="b40d9-122">For an example of calling a conversation operator procedure, see [How to: Use a Class that Defines Operators](./how-to-use-a-class-that-defines-operators.md).</span></span>  
  
## <a name="compile-the-code"></a><span data-ttu-id="b40d9-123">编译代码</span><span class="sxs-lookup"><span data-stu-id="b40d9-123">Compile the code</span></span>  

 <span data-ttu-id="b40d9-124">请确保所用的类或结构定义要使用的运算符。</span><span class="sxs-lookup"><span data-stu-id="b40d9-124">Be sure the class or structure you are using defines the operator you want to use.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b40d9-125">请参阅</span><span class="sxs-lookup"><span data-stu-id="b40d9-125">See also</span></span>

- [<span data-ttu-id="b40d9-126">运算符过程</span><span class="sxs-lookup"><span data-stu-id="b40d9-126">Operator Procedures</span></span>](./operator-procedures.md)
- [<span data-ttu-id="b40d9-127">如何：定义运算符</span><span class="sxs-lookup"><span data-stu-id="b40d9-127">How to: Define an Operator</span></span>](./how-to-define-an-operator.md)
- [<span data-ttu-id="b40d9-128">如何：定义转换运算符</span><span class="sxs-lookup"><span data-stu-id="b40d9-128">How to: Define a Conversion Operator</span></span>](./how-to-define-a-conversion-operator.md)
- [<span data-ttu-id="b40d9-129">Operator Statement</span><span class="sxs-lookup"><span data-stu-id="b40d9-129">Operator Statement</span></span>](../../../language-reference/statements/operator-statement.md)
- [<span data-ttu-id="b40d9-130">Widening</span><span class="sxs-lookup"><span data-stu-id="b40d9-130">Widening</span></span>](../../../language-reference/modifiers/widening.md)
- [<span data-ttu-id="b40d9-131">Narrowing</span><span class="sxs-lookup"><span data-stu-id="b40d9-131">Narrowing</span></span>](../../../language-reference/modifiers/narrowing.md)
- [<span data-ttu-id="b40d9-132">Structure 语句</span><span class="sxs-lookup"><span data-stu-id="b40d9-132">Structure Statement</span></span>](../../../language-reference/statements/structure-statement.md)
- [<span data-ttu-id="b40d9-133">如何：声明结构</span><span class="sxs-lookup"><span data-stu-id="b40d9-133">How to: Declare a Structure</span></span>](../data-types/how-to-declare-a-structure.md)
- [<span data-ttu-id="b40d9-134">隐式转换和显式转换</span><span class="sxs-lookup"><span data-stu-id="b40d9-134">Implicit and Explicit Conversions</span></span>](../data-types/implicit-and-explicit-conversions.md)
- [<span data-ttu-id="b40d9-135">Widening and Narrowing Conversions</span><span class="sxs-lookup"><span data-stu-id="b40d9-135">Widening and Narrowing Conversions</span></span>](../data-types/widening-and-narrowing-conversions.md)
