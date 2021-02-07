---
description: '详细了解：函数表达式 (Visual Basic) '
title: 函数表达式
ms.date: 07/20/2015
helpviewer_keywords:
- Function expression [Visual Basic]
- functions [Visual Basic], function expressions
- lambda expressions [Visual Basic], function expression
ms.assetid: e8a47a45-4b8a-4f45-a623-7653625dffbc
ms.openlocfilehash: bef5db7f167b615c2a0c20539521c186683da985
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99666012"
---
# <a name="function-expression-visual-basic"></a><span data-ttu-id="b381b-103">函数表达式 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="b381b-103">Function Expression (Visual Basic)</span></span>

<span data-ttu-id="b381b-104">声明定义函数 lambda 表达式的参数和代码。</span><span class="sxs-lookup"><span data-stu-id="b381b-104">Declares the parameters and code that define a function lambda expression.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b381b-105">语法</span><span class="sxs-lookup"><span data-stu-id="b381b-105">Syntax</span></span>  
  
```vb  
Function ( [ parameterlist ] ) expression  
- or -  
Function ( [ parameterlist ] )  
  [ statements ]  
End Function  
```  
  
## <a name="parts"></a><span data-ttu-id="b381b-106">组成部分</span><span class="sxs-lookup"><span data-stu-id="b381b-106">Parts</span></span>  
  
|<span data-ttu-id="b381b-107">术语</span><span class="sxs-lookup"><span data-stu-id="b381b-107">Term</span></span>|<span data-ttu-id="b381b-108">定义</span><span class="sxs-lookup"><span data-stu-id="b381b-108">Definition</span></span>|  
|---|---|  
|`parameterlist`|<span data-ttu-id="b381b-109">可选。</span><span class="sxs-lookup"><span data-stu-id="b381b-109">Optional.</span></span> <span data-ttu-id="b381b-110">表示此过程参数的局部变量名称的列表。</span><span class="sxs-lookup"><span data-stu-id="b381b-110">A list of local variable names that represent the parameters of this procedure.</span></span> <span data-ttu-id="b381b-111">即使此列表为空，也必须存在括号。</span><span class="sxs-lookup"><span data-stu-id="b381b-111">The parentheses must be present even when the list is empty.</span></span> <span data-ttu-id="b381b-112">请参阅 [参数列表](../statements/parameter-list.md)。</span><span class="sxs-lookup"><span data-stu-id="b381b-112">See [Parameter List](../statements/parameter-list.md).</span></span>|  
|`expression`|<span data-ttu-id="b381b-113">必需。</span><span class="sxs-lookup"><span data-stu-id="b381b-113">Required.</span></span> <span data-ttu-id="b381b-114">单个表达式。</span><span class="sxs-lookup"><span data-stu-id="b381b-114">A single expression.</span></span> <span data-ttu-id="b381b-115">表达式的类型为函数的返回类型。</span><span class="sxs-lookup"><span data-stu-id="b381b-115">The type of the expression is the return type of the function.</span></span>|  
|`statements`|<span data-ttu-id="b381b-116">必需。</span><span class="sxs-lookup"><span data-stu-id="b381b-116">Required.</span></span> <span data-ttu-id="b381b-117">使用语句返回值的语句列表 `Return` 。</span><span class="sxs-lookup"><span data-stu-id="b381b-117">A list of statements that returns a value by using the `Return` statement.</span></span> <span data-ttu-id="b381b-118"> (参见 [Return 语句](../statements/return-statement.md)。 ) 返回值的类型为函数的返回类型。</span><span class="sxs-lookup"><span data-stu-id="b381b-118">(See [Return Statement](../statements/return-statement.md).) The type of the value returned is the return type of the function.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="b381b-119">备注</span><span class="sxs-lookup"><span data-stu-id="b381b-119">Remarks</span></span>  

 <span data-ttu-id="b381b-120">*Lambda 表达式* 是没有名称的函数，用于计算并返回值。</span><span class="sxs-lookup"><span data-stu-id="b381b-120">A *lambda expression* is a function without a name that calculates and returns a value.</span></span> <span data-ttu-id="b381b-121">可以在可以使用委托类型的任何位置使用 lambda 表达式，但不能使用作为的参数 `RemoveHandler` 。</span><span class="sxs-lookup"><span data-stu-id="b381b-121">You can use a lambda expression anywhere you can use a delegate type, except as an argument to `RemoveHandler`.</span></span> <span data-ttu-id="b381b-122">有关委托的详细信息以及对委托使用 lambda 表达式的详细信息，请参阅 [委托语句](../statements/delegate-statement.md) 和 [宽松委托转换](../../programming-guide/language-features/delegates/relaxed-delegate-conversion.md)。</span><span class="sxs-lookup"><span data-stu-id="b381b-122">For more information about delegates, and the use of lambda expressions with delegates, see [Delegate Statement](../statements/delegate-statement.md) and [Relaxed Delegate Conversion](../../programming-guide/language-features/delegates/relaxed-delegate-conversion.md).</span></span>  
  
## <a name="lambda-expression-syntax"></a><span data-ttu-id="b381b-123">Lambda 表达式语法</span><span class="sxs-lookup"><span data-stu-id="b381b-123">Lambda Expression Syntax</span></span>  

 <span data-ttu-id="b381b-124">Lambda 表达式的语法与标准函数的语法类似。</span><span class="sxs-lookup"><span data-stu-id="b381b-124">The syntax of a lambda expression resembles that of a standard function.</span></span> <span data-ttu-id="b381b-125">不同之处如下：</span><span class="sxs-lookup"><span data-stu-id="b381b-125">The differences are as follows:</span></span>  
  
- <span data-ttu-id="b381b-126">Lambda 表达式没有名称。</span><span class="sxs-lookup"><span data-stu-id="b381b-126">A lambda expression does not have a name.</span></span>  
  
- <span data-ttu-id="b381b-127">Lambda 表达式不能具有修饰符，如 `Overloads` 或 `Overrides` 。</span><span class="sxs-lookup"><span data-stu-id="b381b-127">Lambda expressions cannot have modifiers, such as `Overloads` or `Overrides`.</span></span>  
  
- <span data-ttu-id="b381b-128">Lambda 表达式不使用 `As` 子句来指定函数的返回类型。</span><span class="sxs-lookup"><span data-stu-id="b381b-128">Lambda expressions do not use an `As` clause to designate the return type of the function.</span></span> <span data-ttu-id="b381b-129">相反，该类型是从单行 lambda 表达式的主体计算得出的值推断出的，或是多行 lambda 表达式的返回值。</span><span class="sxs-lookup"><span data-stu-id="b381b-129">Instead, the type is inferred from the value that the body of a single-line lambda expression evaluates to, or the return value of a multiline lambda expression.</span></span> <span data-ttu-id="b381b-130">例如，如果单行 lambda 表达式的主体为 `Where cust.City = "London"` ，则其返回类型为 `Boolean` 。</span><span class="sxs-lookup"><span data-stu-id="b381b-130">For example, if the body of a single-line lambda expression is `Where cust.City = "London"`, its return type is `Boolean`.</span></span>  
  
- <span data-ttu-id="b381b-131">单行 lambda 表达式的主体必须是表达式，而不是语句。</span><span class="sxs-lookup"><span data-stu-id="b381b-131">The body of a single-line lambda expression must be an expression, not a statement.</span></span> <span data-ttu-id="b381b-132">正文可以包含对 function 过程的调用，但不能包含对 sub 过程的调用。</span><span class="sxs-lookup"><span data-stu-id="b381b-132">The body can consist of a call to a function procedure, but not a call to a sub procedure.</span></span>  
  
- <span data-ttu-id="b381b-133">所有参数都必须具有指定的数据类型，或者都必须被推断。</span><span class="sxs-lookup"><span data-stu-id="b381b-133">Either all parameters must have specified data types or all must be inferred.</span></span>  
  
- <span data-ttu-id="b381b-134">不允许使用可选参数和 Paramarray 参数。</span><span class="sxs-lookup"><span data-stu-id="b381b-134">Optional and Paramarray parameters are not permitted.</span></span>  
  
- <span data-ttu-id="b381b-135">不允许使用泛型参数。</span><span class="sxs-lookup"><span data-stu-id="b381b-135">Generic parameters are not permitted.</span></span>  
  
## <a name="example"></a><span data-ttu-id="b381b-136">示例</span><span class="sxs-lookup"><span data-stu-id="b381b-136">Example</span></span>  

 <span data-ttu-id="b381b-137">下面的示例演示了两种创建简单 lambda 表达式的方法。</span><span class="sxs-lookup"><span data-stu-id="b381b-137">The following examples show two ways to create simple lambda expressions.</span></span> <span data-ttu-id="b381b-138">第一个使用 `Dim` 来提供函数的名称。</span><span class="sxs-lookup"><span data-stu-id="b381b-138">The first uses a `Dim` to provide a name for the function.</span></span> <span data-ttu-id="b381b-139">若要调用函数，请发送参数的值。</span><span class="sxs-lookup"><span data-stu-id="b381b-139">To call the function, you send in a value for the parameter.</span></span>  
  
 [!code-vb[VbVbalrLambdas#1](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrLambdas/VB/Class1.vb#1)]  
  
 [!code-vb[VbVbalrLambdas#2](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrLambdas/VB/Class1.vb#2)]  
  
## <a name="example"></a><span data-ttu-id="b381b-140">示例</span><span class="sxs-lookup"><span data-stu-id="b381b-140">Example</span></span>  

 <span data-ttu-id="b381b-141">或者，可以同时声明和运行函数。</span><span class="sxs-lookup"><span data-stu-id="b381b-141">Alternatively, you can declare and run the function at the same time.</span></span>  
  
 [!code-vb[VbVbalrLambdas#3](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrLambdas/VB/Class1.vb#3)]  
  
## <a name="example"></a><span data-ttu-id="b381b-142">示例</span><span class="sxs-lookup"><span data-stu-id="b381b-142">Example</span></span>  

 <span data-ttu-id="b381b-143">下面是递增其参数并返回值的 lambda 表达式的示例。</span><span class="sxs-lookup"><span data-stu-id="b381b-143">Following is an example of a lambda expression that increments its argument and returns the value.</span></span> <span data-ttu-id="b381b-144">该示例显示了函数的单行和多行 lambda 表达式语法。</span><span class="sxs-lookup"><span data-stu-id="b381b-144">The example shows both the single-line and multiline lambda expression syntax for a function.</span></span> <span data-ttu-id="b381b-145">有关更多示例，请参阅 [Lambda 表达式](../../programming-guide/language-features/procedures/lambda-expressions.md)。</span><span class="sxs-lookup"><span data-stu-id="b381b-145">For more examples, see [Lambda Expressions](../../programming-guide/language-features/procedures/lambda-expressions.md).</span></span>  
  
 [!code-vb[VbVbalrLambdas#14](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrLambdas/VB/Class1.vb#14)]  
  
## <a name="example"></a><span data-ttu-id="b381b-146">示例</span><span class="sxs-lookup"><span data-stu-id="b381b-146">Example</span></span>  

 <span data-ttu-id="b381b-147">Lambda 表达式在 Language-Integrated 查询 (LINQ) 中采用了许多查询运算符，并且可在基于方法的查询中显式使用。</span><span class="sxs-lookup"><span data-stu-id="b381b-147">Lambda expressions underlie many of the query operators in Language-Integrated Query (LINQ), and can be used explicitly in method-based queries.</span></span> <span data-ttu-id="b381b-148">下面的示例演示一个典型的 LINQ 查询，然后将查询转换为方法格式。</span><span class="sxs-lookup"><span data-stu-id="b381b-148">The following example shows a typical LINQ query, followed by the translation of the query into method format.</span></span>  
  
```vb  
Dim londonCusts = From cust In db.Customers  
                       Where cust.City = "London"  
                       Select cust  
  
' This query is compiled to the following code:  
Dim londonCusts = db.Customers.  
                  Where(Function(cust) cust.City = "London").  
                  Select(Function(cust) cust)  
```  
  
 <span data-ttu-id="b381b-149">有关查询方法的详细信息，请参阅 [查询](../queries/index.md)。</span><span class="sxs-lookup"><span data-stu-id="b381b-149">For more information about query methods, see [Queries](../queries/index.md).</span></span> <span data-ttu-id="b381b-150">有关标准查询运算符的详细信息，请参阅 [标准查询运算符概述](../../programming-guide/concepts/linq/standard-query-operators-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="b381b-150">For more information about standard query operators, see [Standard Query Operators Overview](../../programming-guide/concepts/linq/standard-query-operators-overview.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b381b-151">请参阅</span><span class="sxs-lookup"><span data-stu-id="b381b-151">See also</span></span>

- [<span data-ttu-id="b381b-152">Function 语句</span><span class="sxs-lookup"><span data-stu-id="b381b-152">Function Statement</span></span>](../statements/function-statement.md)
- [<span data-ttu-id="b381b-153">Lambda 表达式</span><span class="sxs-lookup"><span data-stu-id="b381b-153">Lambda Expressions</span></span>](../../programming-guide/language-features/procedures/lambda-expressions.md)
- [<span data-ttu-id="b381b-154">运算符和表达式</span><span class="sxs-lookup"><span data-stu-id="b381b-154">Operators and Expressions</span></span>](../../programming-guide/language-features/operators-and-expressions/index.md)
- [<span data-ttu-id="b381b-155">语句</span><span class="sxs-lookup"><span data-stu-id="b381b-155">Statements</span></span>](../../programming-guide/language-features/statements.md)
- [<span data-ttu-id="b381b-156">值的比较</span><span class="sxs-lookup"><span data-stu-id="b381b-156">Value Comparisons</span></span>](../../programming-guide/language-features/operators-and-expressions/value-comparisons.md)
- [<span data-ttu-id="b381b-157">布尔表达式</span><span class="sxs-lookup"><span data-stu-id="b381b-157">Boolean Expressions</span></span>](../../programming-guide/language-features/operators-and-expressions/boolean-expressions.md)
- [<span data-ttu-id="b381b-158">If 运算符</span><span class="sxs-lookup"><span data-stu-id="b381b-158">If Operator</span></span>](if-operator.md)
- [<span data-ttu-id="b381b-159">宽松委托转换</span><span class="sxs-lookup"><span data-stu-id="b381b-159">Relaxed Delegate Conversion</span></span>](../../programming-guide/language-features/delegates/relaxed-delegate-conversion.md)
