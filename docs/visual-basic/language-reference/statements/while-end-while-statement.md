---
description: '了解详细信息： .。。End While 语句 (Visual Basic) '
title: While...End While 语句
ms.date: 07/20/2015
f1_keywords:
- vb.While
- vb.While...EndWhile
helpviewer_keywords:
- While statement [Visual Basic], While...End While
- While statement [Visual Basic]
- While...End While statements [Visual Basic]
ms.assetid: b931d1ce-e8ed-44d8-a13d-92a4f5458a1e
ms.openlocfilehash: ab452e2d9446c9c44b952c6ebf026f7a6f9080cd
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99787573"
---
# <a name="whileend-while-statement-visual-basic"></a><span data-ttu-id="c473a-103">While...End While 语句 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="c473a-103">While...End While Statement (Visual Basic)</span></span>

<span data-ttu-id="c473a-104">只要给定条件为，则运行一系列语句 `True` 。</span><span class="sxs-lookup"><span data-stu-id="c473a-104">Runs a series of statements as long as a given condition is `True`.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c473a-105">语法</span><span class="sxs-lookup"><span data-stu-id="c473a-105">Syntax</span></span>  
  
```vb  
While condition  
    [ statements ]  
    [ Continue While ]  
    [ statements ]  
    [ Exit While ]  
    [ statements ]  
End While  
```  
  
## <a name="parts"></a><span data-ttu-id="c473a-106">组成部分</span><span class="sxs-lookup"><span data-stu-id="c473a-106">Parts</span></span>  
  
|<span data-ttu-id="c473a-107">术语</span><span class="sxs-lookup"><span data-stu-id="c473a-107">Term</span></span>|<span data-ttu-id="c473a-108">定义</span><span class="sxs-lookup"><span data-stu-id="c473a-108">Definition</span></span>|  
|---|---|  
|`condition`|<span data-ttu-id="c473a-109">必需。</span><span class="sxs-lookup"><span data-stu-id="c473a-109">Required.</span></span> <span data-ttu-id="c473a-110">`Boolean` 表达式。</span><span class="sxs-lookup"><span data-stu-id="c473a-110">`Boolean` expression.</span></span> <span data-ttu-id="c473a-111">如果 `condition` 为 `Nothing` ，则 Visual Basic 将其视为 `False` 。</span><span class="sxs-lookup"><span data-stu-id="c473a-111">If `condition` is `Nothing`, Visual Basic treats it as `False`.</span></span>|  
|`statements`|<span data-ttu-id="c473a-112">可选。</span><span class="sxs-lookup"><span data-stu-id="c473a-112">Optional.</span></span> <span data-ttu-id="c473a-113">后面的一个或多个语句 `While` ，每次运行 `condition` 都是 `True` 。</span><span class="sxs-lookup"><span data-stu-id="c473a-113">One or more statements following `While`, which run every time `condition` is `True`.</span></span>|  
|`Continue While`|<span data-ttu-id="c473a-114">可选。</span><span class="sxs-lookup"><span data-stu-id="c473a-114">Optional.</span></span> <span data-ttu-id="c473a-115">将控制转移到块的下一次迭代 `While` 。</span><span class="sxs-lookup"><span data-stu-id="c473a-115">Transfers control to the next iteration of the `While` block.</span></span>|  
|`Exit While`|<span data-ttu-id="c473a-116">可选。</span><span class="sxs-lookup"><span data-stu-id="c473a-116">Optional.</span></span> <span data-ttu-id="c473a-117">将控制转移到 `While` 块。</span><span class="sxs-lookup"><span data-stu-id="c473a-117">Transfers control out of the `While` block.</span></span>|  
|`End While`|<span data-ttu-id="c473a-118">必需。</span><span class="sxs-lookup"><span data-stu-id="c473a-118">Required.</span></span> <span data-ttu-id="c473a-119">终止 `While` 块的定义。</span><span class="sxs-lookup"><span data-stu-id="c473a-119">Terminates the definition of the `While` block.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="c473a-120">备注</span><span class="sxs-lookup"><span data-stu-id="c473a-120">Remarks</span></span>  

 <span data-ttu-id="c473a-121">`While...End While`如果您想要重复一组不确定次数的语句，只要存在条件，就可以使用结构 `True` 。</span><span class="sxs-lookup"><span data-stu-id="c473a-121">Use a `While...End While` structure when you want to repeat a set of statements an indefinite number of times, as long as a condition remains `True`.</span></span> <span data-ttu-id="c473a-122">如果你想要更灵活地对条件进行测试或测试的结果，你可能更倾向 [于 .。。循环语句](do-loop-statement.md)。</span><span class="sxs-lookup"><span data-stu-id="c473a-122">If you want more flexibility with where you test the condition or what result you test it for, you might prefer the [Do...Loop Statement](do-loop-statement.md).</span></span> <span data-ttu-id="c473a-123">如果要将语句重复一组次数 [，则下一条语句](for-next-statement.md) 通常是更好的选择。</span><span class="sxs-lookup"><span data-stu-id="c473a-123">If you want to repeat the statements a set number of times, the [For...Next Statement](for-next-statement.md) is usually a better choice.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="c473a-124">`While`关键字还用于[Do .。。Loop 语句](do-loop-statement.md)、 [Skip while 子句](../queries/skip-while-clause.md)和[Take while 子句](../queries/take-while-clause.md)。</span><span class="sxs-lookup"><span data-stu-id="c473a-124">The `While` keyword is also used in the [Do...Loop Statement](do-loop-statement.md), the [Skip While Clause](../queries/skip-while-clause.md) and the [Take While Clause](../queries/take-while-clause.md).</span></span>  
  
 <span data-ttu-id="c473a-125">如果 `condition` 为 `True` ，则在 `statements` 遇到语句之前，所有运行 `End While` 。</span><span class="sxs-lookup"><span data-stu-id="c473a-125">If `condition` is `True`, all of the `statements` run until the `End While` statement is encountered.</span></span> <span data-ttu-id="c473a-126">控件会返回到 `While` 语句，并 `condition` 再次选中。</span><span class="sxs-lookup"><span data-stu-id="c473a-126">Control then returns to the `While` statement, and `condition` is again checked.</span></span> <span data-ttu-id="c473a-127">如果 `condition` 仍为 `True` ，则将重复该过程。</span><span class="sxs-lookup"><span data-stu-id="c473a-127">If `condition` is still `True`, the process is repeated.</span></span> <span data-ttu-id="c473a-128">如果是 `False` ，控制将传递到语句后面的语句 `End While` 。</span><span class="sxs-lookup"><span data-stu-id="c473a-128">If it’s `False`, control passes to the statement that follows the `End While` statement.</span></span>  
  
 <span data-ttu-id="c473a-129">`While`语句在开始循环之前始终检查条件。</span><span class="sxs-lookup"><span data-stu-id="c473a-129">The `While` statement always checks the condition before it starts the loop.</span></span> <span data-ttu-id="c473a-130">当条件保留时，循环将继续 `True` 。</span><span class="sxs-lookup"><span data-stu-id="c473a-130">Looping continues while the condition remains `True`.</span></span> <span data-ttu-id="c473a-131">如果 `condition` 是 `False` 第一次进入循环，则它不会运行一次。</span><span class="sxs-lookup"><span data-stu-id="c473a-131">If `condition` is `False` when you first enter the loop, it doesn’t run even once.</span></span>  
  
 <span data-ttu-id="c473a-132">`condition`通常，比较两个值，但它可以是计算结果为[布尔数据类型](../data-types/boolean-data-type.md)值 (或) 的任何表达式 `True` `False` 。</span><span class="sxs-lookup"><span data-stu-id="c473a-132">The `condition` usually results from a comparison of two values, but it can be any expression that evaluates to a [Boolean Data Type](../data-types/boolean-data-type.md) value (`True` or `False`).</span></span> <span data-ttu-id="c473a-133">此表达式可以包含已转换为的另一种数据类型的值，例如，数值类型 `Boolean` 。</span><span class="sxs-lookup"><span data-stu-id="c473a-133">This expression can include a value of another data type, such as a numeric type, that has been converted to `Boolean`.</span></span>  
  
 <span data-ttu-id="c473a-134">可以 `While` 通过在另一个循环中放置循环来嵌套循环。</span><span class="sxs-lookup"><span data-stu-id="c473a-134">You can nest `While` loops by placing one loop within another.</span></span> <span data-ttu-id="c473a-135">您还可以将不同种类的控制结构相互嵌套。</span><span class="sxs-lookup"><span data-stu-id="c473a-135">You can also nest different kinds of control structures within one another.</span></span> <span data-ttu-id="c473a-136">有关详细信息，请参阅 [嵌套控制结构](../../programming-guide/language-features/control-flow/nested-control-structures.md)。</span><span class="sxs-lookup"><span data-stu-id="c473a-136">For more information, see [Nested Control Structures](../../programming-guide/language-features/control-flow/nested-control-structures.md).</span></span>  
  
## <a name="exit-while"></a><span data-ttu-id="c473a-137">退出时间</span><span class="sxs-lookup"><span data-stu-id="c473a-137">Exit While</span></span>  

 <span data-ttu-id="c473a-138">[Exit While](exit-statement.md)语句可以提供另一种退出循环的方法 `While` 。</span><span class="sxs-lookup"><span data-stu-id="c473a-138">The [Exit While](exit-statement.md) statement can provide another way to exit a `While` loop.</span></span> <span data-ttu-id="c473a-139">`Exit While` 立即将控制转移到语句后面的语句 `End While` 。</span><span class="sxs-lookup"><span data-stu-id="c473a-139">`Exit While` immediately transfers control to the statement that follows the `End While` statement.</span></span>  
  
 <span data-ttu-id="c473a-140">`Exit While` (例如，在结构) 中计算某些条件后，通常使用 `If...Then...Else` 。</span><span class="sxs-lookup"><span data-stu-id="c473a-140">You typically use `Exit While` after some condition is evaluated (for example, in an `If...Then...Else` structure).</span></span> <span data-ttu-id="c473a-141">如果检测到可能导致不必要或无法继续迭代的条件（如错误值或终止请求），则可能需要退出循环。</span><span class="sxs-lookup"><span data-stu-id="c473a-141">You might want to exit a loop if you detect a condition that makes it unnecessary or impossible to continue iterating, such as an erroneous value or a termination request.</span></span> <span data-ttu-id="c473a-142">`Exit While`当您测试可能导致 *无限循环* 的情况时，可以使用，这是一个循环，该循环可以运行极大规模甚至无限次。</span><span class="sxs-lookup"><span data-stu-id="c473a-142">You can use `Exit While` when you test for a condition that could cause an *endless loop*, which is a loop that could run an extremely large or even infinite number of times.</span></span> <span data-ttu-id="c473a-143">然后，可以使用 `Exit While` 来转义循环。</span><span class="sxs-lookup"><span data-stu-id="c473a-143">You can then use `Exit While` to escape the loop.</span></span>  
  
 <span data-ttu-id="c473a-144">可以将任意数量的 `Exit While` 语句置于循环中的任意位置 `While` 。</span><span class="sxs-lookup"><span data-stu-id="c473a-144">You can place any number of `Exit While` statements anywhere in the `While` loop.</span></span>  
  
 <span data-ttu-id="c473a-145">在嵌套循环内使用时 `While` ， `Exit While` 将控制转移出最内层循环，并将其转移到下一个更高的嵌套级别。</span><span class="sxs-lookup"><span data-stu-id="c473a-145">When used within nested `While` loops, `Exit While` transfers control out of the innermost loop and into the next higher level of nesting.</span></span>  
  
 <span data-ttu-id="c473a-146">`Continue While`语句会立即将控制转移到循环的下一次迭代。</span><span class="sxs-lookup"><span data-stu-id="c473a-146">The `Continue While` statement immediately transfers control to the next iteration of the loop.</span></span> <span data-ttu-id="c473a-147">有关详细信息，请参阅 [Continue 语句](continue-statement.md)。</span><span class="sxs-lookup"><span data-stu-id="c473a-147">For more information, see [Continue Statement](continue-statement.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="c473a-148">示例</span><span class="sxs-lookup"><span data-stu-id="c473a-148">Example</span></span>  

 <span data-ttu-id="c473a-149">在下面的示例中，循环中的语句将继续运行，直到 `index` 变量大于10。</span><span class="sxs-lookup"><span data-stu-id="c473a-149">In the following example, the statements in the loop continue to run until the `index` variable is greater than 10.</span></span>  
  
 [!code-vb[VbVbalrStatements#171](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStatements/VB/class14.vb#171)]  
  
## <a name="example"></a><span data-ttu-id="c473a-150">示例</span><span class="sxs-lookup"><span data-stu-id="c473a-150">Example</span></span>  

 <span data-ttu-id="c473a-151">下面的示例演示如何使用 `Continue While` 和 `Exit While` 语句。</span><span class="sxs-lookup"><span data-stu-id="c473a-151">The following example illustrates the use of the `Continue While` and `Exit While` statements.</span></span>  
  
 [!code-vb[VbVbalrStatements#172](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStatements/VB/class14.vb#172)]  
  
## <a name="example"></a><span data-ttu-id="c473a-152">示例</span><span class="sxs-lookup"><span data-stu-id="c473a-152">Example</span></span>  

 <span data-ttu-id="c473a-153">下面的示例读取文本文件中的所有行。</span><span class="sxs-lookup"><span data-stu-id="c473a-153">The following example reads all lines in a text file.</span></span> <span data-ttu-id="c473a-154"><xref:System.IO.File.OpenText%2A>方法打开文件并返回 <xref:System.IO.StreamReader> 读取字符的。</span><span class="sxs-lookup"><span data-stu-id="c473a-154">The <xref:System.IO.File.OpenText%2A> method opens the file and returns a <xref:System.IO.StreamReader> that reads the characters.</span></span> <span data-ttu-id="c473a-155">在 `While` 条件中，的 <xref:System.IO.StreamReader.Peek%2A> 方法 `StreamReader` 确定文件是否包含其他字符。</span><span class="sxs-lookup"><span data-stu-id="c473a-155">In the `While` condition, the <xref:System.IO.StreamReader.Peek%2A> method of the `StreamReader` determines whether the file contains additional characters.</span></span>  
  
 [!code-vb[VbVbalrStatements#173](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStatements/VB/class14.vb#173)]  
  
## <a name="see-also"></a><span data-ttu-id="c473a-156">请参阅</span><span class="sxs-lookup"><span data-stu-id="c473a-156">See also</span></span>

- [<span data-ttu-id="c473a-157">循环结构</span><span class="sxs-lookup"><span data-stu-id="c473a-157">Loop Structures</span></span>](../../programming-guide/language-features/control-flow/loop-structures.md)
- [<span data-ttu-id="c473a-158">Do...Loop 语句</span><span class="sxs-lookup"><span data-stu-id="c473a-158">Do...Loop Statement</span></span>](do-loop-statement.md)
- [<span data-ttu-id="c473a-159">For...Next 语句</span><span class="sxs-lookup"><span data-stu-id="c473a-159">For...Next Statement</span></span>](for-next-statement.md)
- [<span data-ttu-id="c473a-160">布尔数据类型</span><span class="sxs-lookup"><span data-stu-id="c473a-160">Boolean Data Type</span></span>](../data-types/boolean-data-type.md)
- [<span data-ttu-id="c473a-161">嵌套的控件结构</span><span class="sxs-lookup"><span data-stu-id="c473a-161">Nested Control Structures</span></span>](../../programming-guide/language-features/control-flow/nested-control-structures.md)
- [<span data-ttu-id="c473a-162">Exit 语句</span><span class="sxs-lookup"><span data-stu-id="c473a-162">Exit Statement</span></span>](exit-statement.md)
- [<span data-ttu-id="c473a-163">Continue 语句</span><span class="sxs-lookup"><span data-stu-id="c473a-163">Continue Statement</span></span>](continue-statement.md)
