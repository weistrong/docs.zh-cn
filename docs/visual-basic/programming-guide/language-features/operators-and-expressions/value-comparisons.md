---
description: '了解详细信息：值比较 (Visual Basic) '
title: 值的比较
ms.date: 07/20/2015
helpviewer_keywords:
- variables [Visual Basic], comparing values
- Visual Basic code, operators
- Visual Basic code, expressions
- comparison operators [Visual Basic], comparing expressions
- numeric expressions
- operators [Visual Basic], comparison
- expressions [Visual Basic], comparing
ms.assetid: 60da0c76-9458-4afc-97e9-44a7939c064c
ms.openlocfilehash: b5d2228b5bb6be18aecebcd0247a1e29e29df9ec
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100472704"
---
# <a name="value-comparisons-visual-basic"></a><span data-ttu-id="2189a-103">值的比较 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="2189a-103">Value Comparisons (Visual Basic)</span></span>

<span data-ttu-id="2189a-104">比较运算符可用于构造比较数值变量的值的表达式。</span><span class="sxs-lookup"><span data-stu-id="2189a-104">Comparison operators can be used to construct expressions that compare the values of numeric variables.</span></span> <span data-ttu-id="2189a-105">这些表达式 `Boolean` 根据比较结果为 true 或 false 返回值。</span><span class="sxs-lookup"><span data-stu-id="2189a-105">These expressions return a `Boolean` value based on whether the comparison is true or false.</span></span> <span data-ttu-id="2189a-106">此类表达式的示例如下所示。</span><span class="sxs-lookup"><span data-stu-id="2189a-106">Examples of such an expression are as follows.</span></span>  
  
 `45 > 26`  
  
 `26 > 45`  
  
 <span data-ttu-id="2189a-107">第一个表达式的计算结果为 `True` ，因为45大于26。</span><span class="sxs-lookup"><span data-stu-id="2189a-107">The first expression evaluates to `True`, because 45 is greater than 26.</span></span> <span data-ttu-id="2189a-108">第二个示例的计算结果为 `False` ，因为26不大于45。</span><span class="sxs-lookup"><span data-stu-id="2189a-108">The second example evaluates to `False`, because 26 is not greater than 45.</span></span>  
  
 <span data-ttu-id="2189a-109">您还可以采用这种方式比较数值表达式。</span><span class="sxs-lookup"><span data-stu-id="2189a-109">You can also compare numeric expressions in this fashion.</span></span> <span data-ttu-id="2189a-110">比较的表达式本身就是复杂表达式，如下面的示例中所示。</span><span class="sxs-lookup"><span data-stu-id="2189a-110">The expressions you compare can themselves be complex expressions, as in the following example.</span></span>  
  
 `x / 45 * (y +17) >= System.Math.Sqrt(z) / (p - (x * 16))`  
  
 <span data-ttu-id="2189a-111">前面的复杂表达式包括文本、变量和函数调用。</span><span class="sxs-lookup"><span data-stu-id="2189a-111">The preceding complex expression includes literals, variables, and function calls.</span></span> <span data-ttu-id="2189a-112">将计算比较运算符两侧的表达式，然后使用比较运算符比较结果值 `>=` 。</span><span class="sxs-lookup"><span data-stu-id="2189a-112">The expressions on both sides of the comparison operator are evaluated, and the resulting values are then compared using the `>=` comparison operator.</span></span> <span data-ttu-id="2189a-113">如果左侧表达式的值大于或等于右侧表达式的值，则整个表达式的计算结果为 `True` ; 否则，其计算结果为 `False` 。</span><span class="sxs-lookup"><span data-stu-id="2189a-113">If the value of the expression on the left side is greater than or equal to the value of the expression on the right, the entire expression evaluates to `True`; otherwise, it evaluates to `False`.</span></span>  
  
 <span data-ttu-id="2189a-114">用于比较值的表达式最常用于 `If...Then` 构造中，如下面的示例中所示。</span><span class="sxs-lookup"><span data-stu-id="2189a-114">Expressions that compare values are most commonly used in `If...Then` constructions, as in the following example.</span></span>  
  
 [!code-vb[VbVbalrOperators#84](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrOperators/VB/Class1.vb#84)]  
  
 <span data-ttu-id="2189a-115">`=`符号是比较运算符以及赋值运算符。</span><span class="sxs-lookup"><span data-stu-id="2189a-115">The `=` sign is a comparison operator as well as an assignment operator.</span></span> <span data-ttu-id="2189a-116">用作比较运算符时，它计算左侧的值是否等于右侧的值，如下面的示例中所示。</span><span class="sxs-lookup"><span data-stu-id="2189a-116">When used as a comparison operator, it evaluates whether the value on the left is equal to the value on the right, as shown in the following example.</span></span>  
  
 [!code-vb[VbVbalrOperators#85](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrOperators/VB/Class1.vb#85)]  
  
 <span data-ttu-id="2189a-117">你还可以在需要值的任何位置使用比较表达式 `Boolean` ，如在 `If` 、 `While` 、 `Loop` 或 `ElseIf` 语句中，或者在赋值或向变量传递值时使用 `Boolean` 。</span><span class="sxs-lookup"><span data-stu-id="2189a-117">You can also use a comparison expression anywhere a `Boolean` value is needed, such as in an `If`, `While`, `Loop`, or `ElseIf` statement, or when assigning to or passing a value to a `Boolean` variable.</span></span> <span data-ttu-id="2189a-118">在下面的示例中，比较表达式返回的值被分配给一个 `Boolean` 变量。</span><span class="sxs-lookup"><span data-stu-id="2189a-118">In the following example, the value returned by the comparison expression is assigned to a `Boolean` variable.</span></span>  
  
 [!code-vb[VbVbalrOperators#86](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrOperators/VB/Class1.vb#86)]  
  
## <a name="see-also"></a><span data-ttu-id="2189a-119">请参阅</span><span class="sxs-lookup"><span data-stu-id="2189a-119">See also</span></span>

- [<span data-ttu-id="2189a-120">布尔表达式</span><span class="sxs-lookup"><span data-stu-id="2189a-120">Boolean Expressions</span></span>](boolean-expressions.md)
- [<span data-ttu-id="2189a-121">运算符和表达式</span><span class="sxs-lookup"><span data-stu-id="2189a-121">Operators and Expressions</span></span>](index.md)
- [<span data-ttu-id="2189a-122">Comparison Operators in Visual Basic</span><span class="sxs-lookup"><span data-stu-id="2189a-122">Comparison Operators in Visual Basic</span></span>](comparison-operators.md)
- [<span data-ttu-id="2189a-123">如何：计算数值</span><span class="sxs-lookup"><span data-stu-id="2189a-123">How to: Calculate Numeric Values</span></span>](how-to-calculate-numeric-values.md)
- [<span data-ttu-id="2189a-124">Visual Basic 中的运算符优先级</span><span class="sxs-lookup"><span data-stu-id="2189a-124">Operator Precedence in Visual Basic</span></span>](../../../language-reference/operators/operator-precedence.md)
