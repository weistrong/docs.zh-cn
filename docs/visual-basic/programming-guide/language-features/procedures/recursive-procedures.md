---
description: '了解详细信息：递归过程 (Visual Basic) '
title: 递归过程
ms.date: 07/20/2015
helpviewer_keywords:
- Visual Basic code, procedures
- procedures [Visual Basic], that call themselves
- procedures [Visual Basic], recursive
- procedures [Visual Basic], calling
- recursive procedures
- functions [Visual Basic], calling recursively
- recursion
ms.assetid: ba1d3962-b4c3-48d3-875e-96fdb4198327
ms.openlocfilehash: 378b279a6664cd494fb2e26ff3276afcea56cc16
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100466557"
---
# <a name="recursive-procedures-visual-basic"></a><span data-ttu-id="fd8ca-103">递归过程 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="fd8ca-103">Recursive Procedures (Visual Basic)</span></span>

<span data-ttu-id="fd8ca-104">*递归* 过程是指调用自身的过程。</span><span class="sxs-lookup"><span data-stu-id="fd8ca-104">A *recursive* procedure is one that calls itself.</span></span> <span data-ttu-id="fd8ca-105">通常，这并不是编写 Visual Basic 代码的最有效方法。</span><span class="sxs-lookup"><span data-stu-id="fd8ca-105">In general, this is not the most effective way to write Visual Basic code.</span></span>  
  
 <span data-ttu-id="fd8ca-106">下面的过程使用递归来计算其原始参数的阶乘。</span><span class="sxs-lookup"><span data-stu-id="fd8ca-106">The following procedure uses recursion to calculate the factorial of its original argument.</span></span>  
  
 [!code-vb[VbVbcnProcedures#51](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnProcedures/VB/Class1.vb#51)]  
  
## <a name="considerations-with-recursive-procedures"></a><span data-ttu-id="fd8ca-107">递归过程的注意事项</span><span class="sxs-lookup"><span data-stu-id="fd8ca-107">Considerations with Recursive Procedures</span></span>

 <span data-ttu-id="fd8ca-108">**限制条件**。</span><span class="sxs-lookup"><span data-stu-id="fd8ca-108">**Limiting Conditions**.</span></span> <span data-ttu-id="fd8ca-109">必须设计一个递归过程来测试至少一个可以终止递归的条件，并且还必须处理在合理的递归调用中不满足此类条件的情况。</span><span class="sxs-lookup"><span data-stu-id="fd8ca-109">You must design a recursive procedure to test for at least one condition that can terminate the recursion, and you must also handle the case where no such condition is satisfied within a reasonable number of recursive calls.</span></span> <span data-ttu-id="fd8ca-110">如果至少有一种情况不会失败，则您的过程会在无限循环中运行。</span><span class="sxs-lookup"><span data-stu-id="fd8ca-110">Without at least one condition that can be met without fail, your procedure runs a high risk of executing in an infinite loop.</span></span>

 <span data-ttu-id="fd8ca-111">**内存使用率**。</span><span class="sxs-lookup"><span data-stu-id="fd8ca-111">**Memory Usage**.</span></span> <span data-ttu-id="fd8ca-112">应用程序的本地变量空间量有限。</span><span class="sxs-lookup"><span data-stu-id="fd8ca-112">Your application has a limited amount of space for local variables.</span></span> <span data-ttu-id="fd8ca-113">当过程每次调用自身时，它会使用更多的空间来获取其局部变量的其他副本。</span><span class="sxs-lookup"><span data-stu-id="fd8ca-113">Each time a procedure calls itself, it uses more of that space for additional copies of its local variables.</span></span> <span data-ttu-id="fd8ca-114">如果此过程持续下去，最终会导致 <xref:System.StackOverflowException> 错误。</span><span class="sxs-lookup"><span data-stu-id="fd8ca-114">If this process continues indefinitely, it eventually causes a <xref:System.StackOverflowException> error.</span></span>

 <span data-ttu-id="fd8ca-115">**效率**。</span><span class="sxs-lookup"><span data-stu-id="fd8ca-115">**Efficiency**.</span></span> <span data-ttu-id="fd8ca-116">几乎始终可以将递归替换为循环。</span><span class="sxs-lookup"><span data-stu-id="fd8ca-116">You can almost always substitute a loop for recursion.</span></span> <span data-ttu-id="fd8ca-117">循环不会产生传递参数的开销、初始化附加存储以及返回值。</span><span class="sxs-lookup"><span data-stu-id="fd8ca-117">A loop does not have the overhead of passing arguments, initializing additional storage, and returning values.</span></span> <span data-ttu-id="fd8ca-118">如果没有递归调用，性能可能会更好。</span><span class="sxs-lookup"><span data-stu-id="fd8ca-118">Your performance can be much better without recursive calls.</span></span>

 <span data-ttu-id="fd8ca-119">**相互递归**。</span><span class="sxs-lookup"><span data-stu-id="fd8ca-119">**Mutual Recursion**.</span></span> <span data-ttu-id="fd8ca-120">如果两个过程相互调用，你可能会发现性能非常差，甚至会出现无限循环。</span><span class="sxs-lookup"><span data-stu-id="fd8ca-120">You might observe very poor performance, or even an infinite loop, if two procedures call each other.</span></span> <span data-ttu-id="fd8ca-121">此类设计与单个递归过程表现出相同的问题，但可以更难检测和调试。</span><span class="sxs-lookup"><span data-stu-id="fd8ca-121">Such a design presents the same problems as a single recursive procedure, but can be harder to detect and debug.</span></span>

 <span data-ttu-id="fd8ca-122">**调用括号**。</span><span class="sxs-lookup"><span data-stu-id="fd8ca-122">**Calling with Parentheses**.</span></span> <span data-ttu-id="fd8ca-123">如果 `Function` 过程以递归方式调用自身，则必须在过程名称后面加上括号，即使没有参数列表也是如此。</span><span class="sxs-lookup"><span data-stu-id="fd8ca-123">When a `Function` procedure calls itself recursively, you must follow the procedure name with parentheses, even if there is no argument list.</span></span> <span data-ttu-id="fd8ca-124">否则，函数名称将采用表示函数的返回值的形式。</span><span class="sxs-lookup"><span data-stu-id="fd8ca-124">Otherwise, the function name is taken as representing the return value of the function.</span></span>

 <span data-ttu-id="fd8ca-125">**测试**。</span><span class="sxs-lookup"><span data-stu-id="fd8ca-125">**Testing**.</span></span> <span data-ttu-id="fd8ca-126">如果编写递归过程，应仔细测试该过程，以确保它始终满足某些限制条件。</span><span class="sxs-lookup"><span data-stu-id="fd8ca-126">If you write a recursive procedure, you should test it very carefully to make sure it always meets some limiting condition.</span></span> <span data-ttu-id="fd8ca-127">你还应确保不会因为有太多递归调用而耗尽内存。</span><span class="sxs-lookup"><span data-stu-id="fd8ca-127">You should also ensure that you cannot run out of memory due to having too many recursive calls.</span></span>

## <a name="see-also"></a><span data-ttu-id="fd8ca-128">请参阅</span><span class="sxs-lookup"><span data-stu-id="fd8ca-128">See also</span></span>

- <xref:System.StackOverflowException>
- [<span data-ttu-id="fd8ca-129">过程</span><span class="sxs-lookup"><span data-stu-id="fd8ca-129">Procedures</span></span>](index.md)
- [<span data-ttu-id="fd8ca-130">Sub 过程</span><span class="sxs-lookup"><span data-stu-id="fd8ca-130">Sub Procedures</span></span>](sub-procedures.md)
- [<span data-ttu-id="fd8ca-131">Function 过程</span><span class="sxs-lookup"><span data-stu-id="fd8ca-131">Function Procedures</span></span>](function-procedures.md)
- [<span data-ttu-id="fd8ca-132">Property 过程</span><span class="sxs-lookup"><span data-stu-id="fd8ca-132">Property Procedures</span></span>](property-procedures.md)
- [<span data-ttu-id="fd8ca-133">运算符过程</span><span class="sxs-lookup"><span data-stu-id="fd8ca-133">Operator Procedures</span></span>](operator-procedures.md)
- [<span data-ttu-id="fd8ca-134">过程形参和实参</span><span class="sxs-lookup"><span data-stu-id="fd8ca-134">Procedure Parameters and Arguments</span></span>](procedure-parameters-and-arguments.md)
- [<span data-ttu-id="fd8ca-135">过程重载</span><span class="sxs-lookup"><span data-stu-id="fd8ca-135">Procedure Overloading</span></span>](procedure-overloading.md)
- [<span data-ttu-id="fd8ca-136">过程疑难解答</span><span class="sxs-lookup"><span data-stu-id="fd8ca-136">Troubleshooting Procedures</span></span>](troubleshooting-procedures.md)
- [<span data-ttu-id="fd8ca-137">循环结构</span><span class="sxs-lookup"><span data-stu-id="fd8ca-137">Loop Structures</span></span>](../control-flow/loop-structures.md)
