---
description: '了解详细信息： Xor 运算符 (Visual Basic) '
title: Xor 运算符
ms.date: 07/20/2015
f1_keywords:
- vb.Xor
helpviewer_keywords:
- exclusive OR operator [Visual Basic]
- logical exclusion
- operators [Visual Basic], exclusive or
- exclusion operator [Visual Basic]
- operators [Visual Basic], bitwise
- bitwise operators [Visual Basic], XOR operator
- Xor operator [Visual Basic]
- Xor keyword [Visual Basic]
- bitwise comparison [Visual Basic]
ms.assetid: 036000a9-3934-4e7f-a9d0-a816de3d84a6
ms.openlocfilehash: 313ff30ace91b1832c0d35df13294e570a8e410d
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99795217"
---
# <a name="xor-operator-visual-basic"></a><span data-ttu-id="f809a-103">异或运算符 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="f809a-103">Xor Operator (Visual Basic)</span></span>

<span data-ttu-id="f809a-104">对两个表达式执行逻辑异 `Boolean` 运算，或对两个数值表达式执行位异运算。</span><span class="sxs-lookup"><span data-stu-id="f809a-104">Performs a logical exclusion on two `Boolean` expressions, or a bitwise exclusion on two numeric expressions.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f809a-105">语法</span><span class="sxs-lookup"><span data-stu-id="f809a-105">Syntax</span></span>  
  
```vb  
result = expression1 Xor expression2  
```  
  
## <a name="parts"></a><span data-ttu-id="f809a-106">组成部分</span><span class="sxs-lookup"><span data-stu-id="f809a-106">Parts</span></span>  

 `result`  
 <span data-ttu-id="f809a-107">必需。</span><span class="sxs-lookup"><span data-stu-id="f809a-107">Required.</span></span> <span data-ttu-id="f809a-108">Any `Boolean` 或 numeric 变量。</span><span class="sxs-lookup"><span data-stu-id="f809a-108">Any `Boolean` or numeric variable.</span></span> <span data-ttu-id="f809a-109">对于布尔值比较， `result` 是指逻辑排除 (两个值的独占逻辑析取) `Boolean` 。</span><span class="sxs-lookup"><span data-stu-id="f809a-109">For Boolean comparison, `result` is the logical exclusion (exclusive logical disjunction) of two `Boolean` values.</span></span> <span data-ttu-id="f809a-110">对于按位运算， `result` 是一个数字值，它表示两个数值位模式的按位异 (排他) 。</span><span class="sxs-lookup"><span data-stu-id="f809a-110">For bitwise operations, `result` is a numeric value that represents the bitwise exclusion (exclusive bitwise disjunction) of two numeric bit patterns.</span></span>  
  
 `expression1`  
 <span data-ttu-id="f809a-111">必需。</span><span class="sxs-lookup"><span data-stu-id="f809a-111">Required.</span></span> <span data-ttu-id="f809a-112">任何 `Boolean` 或数值表达式。</span><span class="sxs-lookup"><span data-stu-id="f809a-112">Any `Boolean` or numeric expression.</span></span>  
  
 `expression2`  
 <span data-ttu-id="f809a-113">必需。</span><span class="sxs-lookup"><span data-stu-id="f809a-113">Required.</span></span> <span data-ttu-id="f809a-114">任何 `Boolean` 或数值表达式。</span><span class="sxs-lookup"><span data-stu-id="f809a-114">Any `Boolean` or numeric expression.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="f809a-115">备注</span><span class="sxs-lookup"><span data-stu-id="f809a-115">Remarks</span></span>  

 <span data-ttu-id="f809a-116">对于布尔值比较 `result` ， `True` 当且仅当和的 `expression1` `expression2` 计算结果都为时，才为 `True` 。</span><span class="sxs-lookup"><span data-stu-id="f809a-116">For Boolean comparison, `result` is `True` if and only if exactly one of `expression1` and `expression2` evaluates to `True`.</span></span> <span data-ttu-id="f809a-117">即，当且仅当和 `expression1` 的 `expression2` 计算结果为相反 `Boolean` 值时。</span><span class="sxs-lookup"><span data-stu-id="f809a-117">That is, if and only if `expression1` and `expression2` evaluate to opposite `Boolean` values.</span></span> <span data-ttu-id="f809a-118">下表说明了如何 `result` 确定。</span><span class="sxs-lookup"><span data-stu-id="f809a-118">The following table illustrates how `result` is determined.</span></span>  
  
|<span data-ttu-id="f809a-119">如果 `expression1` 为 </span><span class="sxs-lookup"><span data-stu-id="f809a-119">If `expression1` is</span></span>|<span data-ttu-id="f809a-120">并且 `expression2` 为</span><span class="sxs-lookup"><span data-stu-id="f809a-120">And `expression2` is</span></span>|<span data-ttu-id="f809a-121">的值 `result` 为</span><span class="sxs-lookup"><span data-stu-id="f809a-121">The value of `result` is</span></span>|  
|-------------------------|--------------------------|------------------------------|  
|`True`|`True`|`False`|  
|`True`|`False`|`True`|  
|`False`|`True`|`True`|  
|`False`|`False`|`False`|  
  
> [!NOTE]
> <span data-ttu-id="f809a-122">在布尔比较中， `Xor` 运算符始终计算两个表达式，这可能包括进行过程调用。</span><span class="sxs-lookup"><span data-stu-id="f809a-122">In a Boolean comparison, the `Xor` operator always evaluates both expressions, which could include making procedure calls.</span></span> <span data-ttu-id="f809a-123">没有与对应的短路 `Xor` ，因为结果总是依赖于这两个操作数。</span><span class="sxs-lookup"><span data-stu-id="f809a-123">There is no short-circuiting counterpart to `Xor`, because the result always depends on both operands.</span></span> <span data-ttu-id="f809a-124">对于 *短路* 逻辑运算符，请参阅 [AndAlso Operator](andalso-operator.md) and [OrElse 运算符](orelse-operator.md)。</span><span class="sxs-lookup"><span data-stu-id="f809a-124">For *short-circuiting* logical operators, see [AndAlso Operator](andalso-operator.md) and [OrElse Operator](orelse-operator.md).</span></span>  
  
 <span data-ttu-id="f809a-125">对于按位运算， `Xor` 运算符对两个数值表达式中的相同位置执行按位比较，并根据下表设置中的相应位 `result` 。</span><span class="sxs-lookup"><span data-stu-id="f809a-125">For bitwise operations, the `Xor` operator performs a bitwise comparison of identically positioned bits in two numeric expressions and sets the corresponding bit in `result` according to the following table.</span></span>  
  
|<span data-ttu-id="f809a-126">如果中的位 `expression1` 是</span><span class="sxs-lookup"><span data-stu-id="f809a-126">If bit in `expression1` is</span></span>|<span data-ttu-id="f809a-127">和中的位 `expression2` 是</span><span class="sxs-lookup"><span data-stu-id="f809a-127">And bit in `expression2` is</span></span>|<span data-ttu-id="f809a-128">中的位 `result` 是</span><span class="sxs-lookup"><span data-stu-id="f809a-128">The bit in `result` is</span></span>|  
|--------------------------------|---------------------------------|----------------------------|  
|<span data-ttu-id="f809a-129">1</span><span class="sxs-lookup"><span data-stu-id="f809a-129">1</span></span>|<span data-ttu-id="f809a-130">1</span><span class="sxs-lookup"><span data-stu-id="f809a-130">1</span></span>|<span data-ttu-id="f809a-131">0</span><span class="sxs-lookup"><span data-stu-id="f809a-131">0</span></span>|  
|<span data-ttu-id="f809a-132">1</span><span class="sxs-lookup"><span data-stu-id="f809a-132">1</span></span>|<span data-ttu-id="f809a-133">0</span><span class="sxs-lookup"><span data-stu-id="f809a-133">0</span></span>|<span data-ttu-id="f809a-134">1</span><span class="sxs-lookup"><span data-stu-id="f809a-134">1</span></span>|  
|<span data-ttu-id="f809a-135">0</span><span class="sxs-lookup"><span data-stu-id="f809a-135">0</span></span>|<span data-ttu-id="f809a-136">1</span><span class="sxs-lookup"><span data-stu-id="f809a-136">1</span></span>|<span data-ttu-id="f809a-137">1</span><span class="sxs-lookup"><span data-stu-id="f809a-137">1</span></span>|  
|<span data-ttu-id="f809a-138">0</span><span class="sxs-lookup"><span data-stu-id="f809a-138">0</span></span>|<span data-ttu-id="f809a-139">0</span><span class="sxs-lookup"><span data-stu-id="f809a-139">0</span></span>|<span data-ttu-id="f809a-140">0</span><span class="sxs-lookup"><span data-stu-id="f809a-140">0</span></span>|  
  
> [!NOTE]
> <span data-ttu-id="f809a-141">由于逻辑 and 位运算符的优先级低于其他算术运算符和关系运算符，因此应将任何按位运算括在括号中，以确保准确执行。</span><span class="sxs-lookup"><span data-stu-id="f809a-141">Since the logical and bitwise operators have a lower precedence than other arithmetic and relational operators, any bitwise operations should be enclosed in parentheses to ensure accurate execution.</span></span>  
  
 <span data-ttu-id="f809a-142">例如，5 `Xor` 3 为6。</span><span class="sxs-lookup"><span data-stu-id="f809a-142">For example, 5 `Xor` 3 is 6.</span></span> <span data-ttu-id="f809a-143">若要查看此操作的原因，请将5和3转换为其二进制表示形式101和011。</span><span class="sxs-lookup"><span data-stu-id="f809a-143">To see why this is so, convert 5 and 3 to their binary representations, 101 and 011.</span></span> <span data-ttu-id="f809a-144">然后，使用上表来确定 101 Xor 011 为110，这是十进制数字6的二进制表示形式。</span><span class="sxs-lookup"><span data-stu-id="f809a-144">Then use the previous table to determine that 101 Xor 011 is 110, which is the binary representation of the decimal number 6.</span></span>  
  
## <a name="data-types"></a><span data-ttu-id="f809a-145">数据类型</span><span class="sxs-lookup"><span data-stu-id="f809a-145">Data Types</span></span>  

 <span data-ttu-id="f809a-146">如果操作数由一个 `Boolean` 表达式和一个数值表达式组成，则 Visual Basic 会将 `Boolean` 表达式转换为数值， ( 为– 1; 对于) ，则将 `True` `False` 执行按位运算。</span><span class="sxs-lookup"><span data-stu-id="f809a-146">If the operands consist of one `Boolean` expression and one numeric expression, Visual Basic converts the `Boolean` expression to a numeric value (–1 for `True` and 0 for `False`) and performs a bitwise operation.</span></span>  
  
 <span data-ttu-id="f809a-147">对于 `Boolean` 比较，结果的数据类型为 `Boolean` 。</span><span class="sxs-lookup"><span data-stu-id="f809a-147">For a `Boolean` comparison, the data type of the result is `Boolean`.</span></span> <span data-ttu-id="f809a-148">对于按位比较，结果数据类型是适用于和的数据类型的数值类型 `expression1` `expression2` 。</span><span class="sxs-lookup"><span data-stu-id="f809a-148">For a bitwise comparison, the result data type is a numeric type appropriate for the data types of `expression1` and `expression2`.</span></span> <span data-ttu-id="f809a-149">请参阅 [运算符结果的数据类型](data-types-of-operator-results.md)中的 "关系和按位比较" 表。</span><span class="sxs-lookup"><span data-stu-id="f809a-149">See the "Relational and Bitwise Comparisons" table in [Data Types of Operator Results](data-types-of-operator-results.md).</span></span>  
  
## <a name="overloading"></a><span data-ttu-id="f809a-150">重载</span><span class="sxs-lookup"><span data-stu-id="f809a-150">Overloading</span></span>  

 <span data-ttu-id="f809a-151">`Xor`运算符可以 *重载*，这意味着当操作数具有该类或结构的类型时，该类或结构可以重新定义其行为。</span><span class="sxs-lookup"><span data-stu-id="f809a-151">The `Xor` operator can be *overloaded*, which means that a class or structure can redefine its behavior when an operand has the type of that class or structure.</span></span> <span data-ttu-id="f809a-152">如果代码对这样的类或结构使用此运算符，请确保了解其重新定义的行为。</span><span class="sxs-lookup"><span data-stu-id="f809a-152">If your code uses this operator on such a class or structure, make sure you understand its redefined behavior.</span></span> <span data-ttu-id="f809a-153">有关详细信息，请参阅 [Operator Procedures](../../programming-guide/language-features/procedures/operator-procedures.md)。</span><span class="sxs-lookup"><span data-stu-id="f809a-153">For more information, see [Operator Procedures](../../programming-guide/language-features/procedures/operator-procedures.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="f809a-154">示例</span><span class="sxs-lookup"><span data-stu-id="f809a-154">Example</span></span>  

 <span data-ttu-id="f809a-155">下面的示例使用 `Xor` 运算符对两个表达式执行逻辑异运算 (独占逻辑析取) 。</span><span class="sxs-lookup"><span data-stu-id="f809a-155">The following example uses the `Xor` operator to perform logical exclusion (exclusive logical disjunction) on two expressions.</span></span> <span data-ttu-id="f809a-156">结果是一个 `Boolean` 值，该值表示是否只有一个表达式是 `True` 。</span><span class="sxs-lookup"><span data-stu-id="f809a-156">The result is a `Boolean` value that represents whether exactly one of the expressions is `True`.</span></span>  
  
 [!code-vb[VbVbalrOperators#40](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrOperators/VB/Class1.vb#40)]  
  
 <span data-ttu-id="f809a-157">前面的示例 `False` 分别生成、 `True` 和的结果 `False` 。</span><span class="sxs-lookup"><span data-stu-id="f809a-157">The previous example produces results of `False`, `True`, and `False`, respectively.</span></span>  
  
## <a name="example"></a><span data-ttu-id="f809a-158">示例</span><span class="sxs-lookup"><span data-stu-id="f809a-158">Example</span></span>  

 <span data-ttu-id="f809a-159">下面的示例使用 `Xor` 运算符来对两个数值表达式的单个位执行逻辑异 () 独占逻辑析取。</span><span class="sxs-lookup"><span data-stu-id="f809a-159">The following example uses the `Xor` operator to perform logical exclusion (exclusive logical disjunction) on the individual bits of two numeric expressions.</span></span> <span data-ttu-id="f809a-160">如果操作数中的相应位中正好有一个设置为1，则结果模式中的位将设置为1。</span><span class="sxs-lookup"><span data-stu-id="f809a-160">The bit in the result pattern is set if exactly one of the corresponding bits in the operands is set to 1.</span></span>  
  
 [!code-vb[VbVbalrOperators#41](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrOperators/VB/Class1.vb#41)]  
  
 <span data-ttu-id="f809a-161">前面的示例分别产生2、12和14的结果。</span><span class="sxs-lookup"><span data-stu-id="f809a-161">The previous example produces results of 2, 12, and 14, respectively.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f809a-162">请参阅</span><span class="sxs-lookup"><span data-stu-id="f809a-162">See also</span></span>

- [<span data-ttu-id="f809a-163">逻辑/按位运算符 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="f809a-163">Logical/Bitwise Operators (Visual Basic)</span></span>](logical-bitwise-operators.md)
- [<span data-ttu-id="f809a-164">Visual Basic 中的运算符优先级</span><span class="sxs-lookup"><span data-stu-id="f809a-164">Operator Precedence in Visual Basic</span></span>](operator-precedence.md)
- [<span data-ttu-id="f809a-165">按功能列出的运算符</span><span class="sxs-lookup"><span data-stu-id="f809a-165">Operators Listed by Functionality</span></span>](operators-listed-by-functionality.md)
- [<span data-ttu-id="f809a-166">Visual Basic 中的逻辑运算符和位运算符</span><span class="sxs-lookup"><span data-stu-id="f809a-166">Logical and Bitwise Operators in Visual Basic</span></span>](../../programming-guide/language-features/operators-and-expressions/logical-and-bitwise-operators.md)
