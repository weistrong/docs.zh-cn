---
description: '了解有关详细信息，请参阅如何：测试两个对象是否具有相同的 (Visual Basic) '
title: 如何：测试两个对象是否相同
ms.date: 07/20/2015
helpviewer_keywords:
- variables [Visual Basic], reference
- Is operator [Visual Basic], comparing objects
- reference variables [Visual Basic]
- variables [Visual Basic], referring to same object
- objects [Visual Basic], variables referring to same
- Visual Basic code, operators
ms.assetid: f760e828-8704-4256-bc2d-c22a4c93b524
ms.openlocfilehash: a0136d9db487ad0ce70b9d55ff8ee014ec30b05a
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100435533"
---
# <a name="how-to-test-whether-two-objects-are-the-same-visual-basic"></a><span data-ttu-id="a0a42-103">如何：测试两个对象是否相同 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="a0a42-103">How to: Test Whether Two Objects Are the Same (Visual Basic)</span></span>

<span data-ttu-id="a0a42-104">如果有两个引用对象的变量，则可以使用 `Is` 或 `IsNot` 运算符，或同时使用这两个变量来确定它们是否引用相同的实例。</span><span class="sxs-lookup"><span data-stu-id="a0a42-104">If you have two variables that refer to objects, you can use either the `Is` or `IsNot` operator, or both, to determine whether they refer to the same instance.</span></span>  
  
### <a name="to-test-whether-two-objects-are-the-same"></a><span data-ttu-id="a0a42-105">测试两个对象是否相同</span><span class="sxs-lookup"><span data-stu-id="a0a42-105">To test whether two objects are the same</span></span>  
  
- <span data-ttu-id="a0a42-106">使用 [Is 运算符](../../../language-reference/operators/is-operator.md) 或将两个变量作为操作数的 [IsNot 运算符](../../../language-reference/operators/isnot-operator.md) 。</span><span class="sxs-lookup"><span data-stu-id="a0a42-106">Use the [Is Operator](../../../language-reference/operators/is-operator.md) or the [IsNot Operator](../../../language-reference/operators/isnot-operator.md) with the two variables as operands.</span></span>  
  
     [!code-vb[VbVbalrOperators#69](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrOperators/VB/Class1.vb#69)]  
  
 <span data-ttu-id="a0a42-107">您可能想要执行特定的操作，具体取决于两个对象是否引用相同的实例。</span><span class="sxs-lookup"><span data-stu-id="a0a42-107">You might want to take a certain action depending on whether two objects refer to the same instance.</span></span> <span data-ttu-id="a0a42-108">前面的示例将控制 `c` 与窗体上的活动控件进行比较 `f` 。</span><span class="sxs-lookup"><span data-stu-id="a0a42-108">The preceding example compares control `c` against the active control on form `f`.</span></span> <span data-ttu-id="a0a42-109">如果没有活动的控件，或者存在，但它不是与相同的控件实例 `c` ，则 `If` 语句将失败，并且过程将返回，而不进行进一步的处理。</span><span class="sxs-lookup"><span data-stu-id="a0a42-109">If there is no active control, or if there is one but it is not the same control instance as `c`, then the `If` statement fails and the procedure returns without further processing.</span></span>  
  
 <span data-ttu-id="a0a42-110">你使用 `Is` 或是否 `IsNot` 是你的个人便利。</span><span class="sxs-lookup"><span data-stu-id="a0a42-110">Whether you use `Is` or `IsNot` is a matter of personal convenience to you.</span></span> <span data-ttu-id="a0a42-111">比给定表达式中的另一个更易于读取。</span><span class="sxs-lookup"><span data-stu-id="a0a42-111">One might be easier to read than the other in a given expression.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a0a42-112">请参阅</span><span class="sxs-lookup"><span data-stu-id="a0a42-112">See also</span></span>

- [<span data-ttu-id="a0a42-113">Comparison Operators in Visual Basic</span><span class="sxs-lookup"><span data-stu-id="a0a42-113">Comparison Operators in Visual Basic</span></span>](comparison-operators.md)
