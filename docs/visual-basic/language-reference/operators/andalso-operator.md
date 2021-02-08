---
description: '详细了解： AndAlso Operator (Visual Basic) '
title: AndAlso 运算符
ms.date: 07/20/2015
f1_keywords:
- vb.AndAlso
- AndAlso
helpviewer_keywords:
- short-circuiting
- AndAlso operator [Visual Basic]
- operators [Visual Basic], short-circuiting
- operators [Visual Basic], conjunction
- short-circuit evaluation
ms.assetid: bbc15191-b374-495b-9b8f-7b8c2f4388eb
ms.openlocfilehash: dcf6c2685bf8f9ffee27b00543786cd3b315b327
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99774260"
---
# <a name="andalso-operator-visual-basic"></a><span data-ttu-id="93c31-103">AndAlso 运算符 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="93c31-103">AndAlso Operator (Visual Basic)</span></span>

<span data-ttu-id="93c31-104">对两个表达式执行短路逻辑与运算。</span><span class="sxs-lookup"><span data-stu-id="93c31-104">Performs short-circuiting logical conjunction on two expressions.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="93c31-105">语法</span><span class="sxs-lookup"><span data-stu-id="93c31-105">Syntax</span></span>  
  
```vb
result = expression1 AndAlso expression2  
```  
  
## <a name="parts"></a><span data-ttu-id="93c31-106">组成部分</span><span class="sxs-lookup"><span data-stu-id="93c31-106">Parts</span></span>  
  
|<span data-ttu-id="93c31-107">术语</span><span class="sxs-lookup"><span data-stu-id="93c31-107">Term</span></span>|<span data-ttu-id="93c31-108">定义</span><span class="sxs-lookup"><span data-stu-id="93c31-108">Definition</span></span>|  
|---|---|  
|`result`|<span data-ttu-id="93c31-109">必需。</span><span class="sxs-lookup"><span data-stu-id="93c31-109">Required.</span></span> <span data-ttu-id="93c31-110">任何 `Boolean` 表达式。</span><span class="sxs-lookup"><span data-stu-id="93c31-110">Any `Boolean` expression.</span></span> <span data-ttu-id="93c31-111">结果是 `Boolean` 这两个表达式的比较结果。</span><span class="sxs-lookup"><span data-stu-id="93c31-111">The result is the `Boolean` result of comparison of the two expressions.</span></span>|  
|`expression1`|<span data-ttu-id="93c31-112">必需。</span><span class="sxs-lookup"><span data-stu-id="93c31-112">Required.</span></span> <span data-ttu-id="93c31-113">任何 `Boolean` 表达式。</span><span class="sxs-lookup"><span data-stu-id="93c31-113">Any `Boolean` expression.</span></span>|  
|`expression2`|<span data-ttu-id="93c31-114">必需。</span><span class="sxs-lookup"><span data-stu-id="93c31-114">Required.</span></span> <span data-ttu-id="93c31-115">任何 `Boolean` 表达式。</span><span class="sxs-lookup"><span data-stu-id="93c31-115">Any `Boolean` expression.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="93c31-116">备注</span><span class="sxs-lookup"><span data-stu-id="93c31-116">Remarks</span></span>  

 <span data-ttu-id="93c31-117">如果编译后的代码可以根据另一个表达式的结果跳过对一个表达式的计算，则将逻辑运算称为 *短路* 。</span><span class="sxs-lookup"><span data-stu-id="93c31-117">A logical operation is said to be *short-circuiting* if the compiled code can bypass the evaluation of one expression depending on the result of another expression.</span></span> <span data-ttu-id="93c31-118">如果第一个表达式的计算结果确定了运算的最终结果，则不需要计算第二个表达式，因为它不能更改最终结果。</span><span class="sxs-lookup"><span data-stu-id="93c31-118">If the result of the first expression evaluated determines the final result of the operation, there is no need to evaluate the second expression, because it cannot change the final result.</span></span> <span data-ttu-id="93c31-119">如果绕过的表达式较复杂，或者它涉及过程调用，则短路可以提高性能。</span><span class="sxs-lookup"><span data-stu-id="93c31-119">Short-circuiting can improve performance if the bypassed expression is complex, or if it involves procedure calls.</span></span>  
  
 <span data-ttu-id="93c31-120">如果两个表达式的计算结果均为 `True` ， `result` 则为 `True` 。</span><span class="sxs-lookup"><span data-stu-id="93c31-120">If both expressions evaluate to `True`, `result` is `True`.</span></span> <span data-ttu-id="93c31-121">下表说明了如何 `result` 确定。</span><span class="sxs-lookup"><span data-stu-id="93c31-121">The following table illustrates how `result` is determined.</span></span>  
  
|<span data-ttu-id="93c31-122">如果 `expression1` 为 </span><span class="sxs-lookup"><span data-stu-id="93c31-122">If `expression1` is</span></span>|<span data-ttu-id="93c31-123">并且 `expression2` 为</span><span class="sxs-lookup"><span data-stu-id="93c31-123">And `expression2` is</span></span>|<span data-ttu-id="93c31-124">的值 `result` 为</span><span class="sxs-lookup"><span data-stu-id="93c31-124">The value of `result` is</span></span>|  
|---|---|---|  
|`True`|`True`|`True`|  
|`True`|`False`|`False`|  
|`False`|<span data-ttu-id="93c31-125">不计算 () </span><span class="sxs-lookup"><span data-stu-id="93c31-125">(not evaluated)</span></span>|`False`|  
  
## <a name="data-types"></a><span data-ttu-id="93c31-126">数据类型</span><span class="sxs-lookup"><span data-stu-id="93c31-126">Data Types</span></span>  

 <span data-ttu-id="93c31-127">`AndAlso`仅为[布尔数据类型](../data-types/boolean-data-type.md)定义运算符。</span><span class="sxs-lookup"><span data-stu-id="93c31-127">The `AndAlso` operator is defined only for the [Boolean Data Type](../data-types/boolean-data-type.md).</span></span> <span data-ttu-id="93c31-128">Visual Basic 在计算表达式之前，根据需要将每个操作数转换为 `Boolean` 。</span><span class="sxs-lookup"><span data-stu-id="93c31-128">Visual Basic converts each operand as necessary to `Boolean` before evaluating the expression.</span></span> <span data-ttu-id="93c31-129">如果将结果赋给数值类型，Visual Basic 会将其从转换 `Boolean` 为该类型，使其 `False` 成为 `0` 并 `True` 变成 `-1` 。</span><span class="sxs-lookup"><span data-stu-id="93c31-129">If you assign the result to a numeric type, Visual Basic converts it from `Boolean` to that type such that `False` becomes `0` and `True` becomes `-1`.</span></span>
<span data-ttu-id="93c31-130">有关详细信息，请参阅 [布尔类型转换](../data-types/boolean-data-type.md#type-conversions)。</span><span class="sxs-lookup"><span data-stu-id="93c31-130">For more information, see [Boolean Type Conversions](../data-types/boolean-data-type.md#type-conversions).</span></span>
  
## <a name="overloading"></a><span data-ttu-id="93c31-131">重载</span><span class="sxs-lookup"><span data-stu-id="93c31-131">Overloading</span></span>  

 <span data-ttu-id="93c31-132">[And 运算符](and-operator.md)和 [IsFalse 运算符](isfalse-operator.md)可以 *重载*，这意味着当操作数具有该类或结构的类型时，该类或结构可以重新定义它们的行为。</span><span class="sxs-lookup"><span data-stu-id="93c31-132">The [And Operator](and-operator.md) and the [IsFalse Operator](isfalse-operator.md) can be *overloaded*, which means that a class or structure can redefine their behavior when an operand has the type of that class or structure.</span></span> <span data-ttu-id="93c31-133">重载 `And` 和 `IsFalse` 运算符会影响运算符的行为 `AndAlso` 。</span><span class="sxs-lookup"><span data-stu-id="93c31-133">Overloading the `And` and `IsFalse` operators affects the behavior of the `AndAlso` operator.</span></span> <span data-ttu-id="93c31-134">如果你的代码 `AndAlso` 在重载和的类或结构上使用 `And` `IsFalse` ，请确保你了解其重新定义的行为。</span><span class="sxs-lookup"><span data-stu-id="93c31-134">If your code uses `AndAlso` on a class or structure that overloads `And` and `IsFalse`, be sure you understand their redefined behavior.</span></span> <span data-ttu-id="93c31-135">有关详细信息，请参阅 [Operator Procedures](../../programming-guide/language-features/procedures/operator-procedures.md)。</span><span class="sxs-lookup"><span data-stu-id="93c31-135">For more information, see [Operator Procedures](../../programming-guide/language-features/procedures/operator-procedures.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="93c31-136">示例</span><span class="sxs-lookup"><span data-stu-id="93c31-136">Example</span></span>  

 <span data-ttu-id="93c31-137">下面的示例使用 `AndAlso` 运算符对两个表达式执行逻辑与运算。</span><span class="sxs-lookup"><span data-stu-id="93c31-137">The following example uses the `AndAlso` operator to perform a logical conjunction on two expressions.</span></span> <span data-ttu-id="93c31-138">结果是一个 `Boolean` 值，该值表示整个联合表达式是否为 true。</span><span class="sxs-lookup"><span data-stu-id="93c31-138">The result is a `Boolean` value that represents whether the entire conjoined expression is true.</span></span> <span data-ttu-id="93c31-139">如果第一个表达式为 `False` ，则不计算第二个表达式。</span><span class="sxs-lookup"><span data-stu-id="93c31-139">If the first expression is `False`, the second is not evaluated.</span></span>  
  
 [!code-vb[VbVbalrOperators#24](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrOperators/VB/Class1.vb#24)]  
  
 <span data-ttu-id="93c31-140">前面的示例 `True` 分别生成、 `False` 和的结果 `False` 。</span><span class="sxs-lookup"><span data-stu-id="93c31-140">The preceding example produces results of `True`, `False`, and `False`, respectively.</span></span> <span data-ttu-id="93c31-141">在的计算中 `secondCheck` ，不计算第二个表达式，因为第一个表达式已经存在 `False` 。</span><span class="sxs-lookup"><span data-stu-id="93c31-141">In the calculation of `secondCheck`, the second expression is not evaluated because the first is already `False`.</span></span> <span data-ttu-id="93c31-142">但是，在的计算中计算第二个表达式 `thirdCheck` 。</span><span class="sxs-lookup"><span data-stu-id="93c31-142">However, the second expression is evaluated in the calculation of `thirdCheck`.</span></span>  
  
## <a name="example"></a><span data-ttu-id="93c31-143">示例</span><span class="sxs-lookup"><span data-stu-id="93c31-143">Example</span></span>  

 <span data-ttu-id="93c31-144">下面的示例演示了在 `Function` 数组的元素中搜索给定值的过程。</span><span class="sxs-lookup"><span data-stu-id="93c31-144">The following example shows a `Function` procedure that searches for a given value among the elements of an array.</span></span> <span data-ttu-id="93c31-145">如果数组为空，或超出了数组长度，则该 `While` 语句不会对照搜索值测试数组元素。</span><span class="sxs-lookup"><span data-stu-id="93c31-145">If the array is empty, or if the array length has been exceeded, the `While` statement does not test the array element against the search value.</span></span>  
  
 [!code-vb[VbVbalrOperators#25](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrOperators/VB/Class1.vb#25)]  
  
## <a name="see-also"></a><span data-ttu-id="93c31-146">请参阅</span><span class="sxs-lookup"><span data-stu-id="93c31-146">See also</span></span>

- [<span data-ttu-id="93c31-147">逻辑/按位运算符 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="93c31-147">Logical/Bitwise Operators (Visual Basic)</span></span>](logical-bitwise-operators.md)
- [<span data-ttu-id="93c31-148">Visual Basic 中的运算符优先级</span><span class="sxs-lookup"><span data-stu-id="93c31-148">Operator Precedence in Visual Basic</span></span>](operator-precedence.md)
- [<span data-ttu-id="93c31-149">按功能列出的运算符</span><span class="sxs-lookup"><span data-stu-id="93c31-149">Operators Listed by Functionality</span></span>](operators-listed-by-functionality.md)
- [<span data-ttu-id="93c31-150">And 运算符</span><span class="sxs-lookup"><span data-stu-id="93c31-150">And Operator</span></span>](and-operator.md)
- [<span data-ttu-id="93c31-151">IsFalse 运算符</span><span class="sxs-lookup"><span data-stu-id="93c31-151">IsFalse Operator</span></span>](isfalse-operator.md)
- [<span data-ttu-id="93c31-152">Visual Basic 中的逻辑运算符和位运算符</span><span class="sxs-lookup"><span data-stu-id="93c31-152">Logical and Bitwise Operators in Visual Basic</span></span>](../../programming-guide/language-features/operators-and-expressions/logical-and-bitwise-operators.md)
