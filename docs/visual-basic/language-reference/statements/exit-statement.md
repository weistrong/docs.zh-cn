---
description: '了解有关以下内容的详细信息： Exit 语句 (Visual Basic) '
title: Exit 语句
ms.date: 07/20/2015
f1_keywords:
- vb.Exit
helpviewer_keywords:
- execution [Visual Basic], ending
- files [Visual Basic], closing
- programs [Visual Basic], quitting
- code, exiting
- Exit statement [Visual Basic]
- program termination
- execution [Visual Basic], stopping
ms.assetid: 760bfb32-5c3f-4bdb-a432-9a6001c92db7
ms.openlocfilehash: 54af7fbf908dbad829cf6f08bf442dfe85e35610
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99769114"
---
# <a name="exit-statement-visual-basic"></a><span data-ttu-id="96c0c-103">Exit 语句 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="96c0c-103">Exit Statement (Visual Basic)</span></span>

<span data-ttu-id="96c0c-104">退出过程或块并将控制立即传输到过程调用或块定义后面的语句。</span><span class="sxs-lookup"><span data-stu-id="96c0c-104">Exits a procedure or block and transfers control immediately to the statement following the procedure call or the block definition.</span></span>

## <a name="syntax"></a><span data-ttu-id="96c0c-105">语法</span><span class="sxs-lookup"><span data-stu-id="96c0c-105">Syntax</span></span>

```vb
Exit { Do | For | Function | Property | Select | Sub | Try | While }
```

## <a name="statements"></a><span data-ttu-id="96c0c-106">语句</span><span class="sxs-lookup"><span data-stu-id="96c0c-106">Statements</span></span>

 `Exit Do`  
 <span data-ttu-id="96c0c-107">立即退出 `Do` 出现该循环的循环。</span><span class="sxs-lookup"><span data-stu-id="96c0c-107">Immediately exits the `Do` loop in which it appears.</span></span> <span data-ttu-id="96c0c-108">继续执行语句后面的语句 `Loop` 。</span><span class="sxs-lookup"><span data-stu-id="96c0c-108">Execution continues with the statement following the `Loop` statement.</span></span> <span data-ttu-id="96c0c-109">`Exit Do` 只能在循环内使用 `Do` 。</span><span class="sxs-lookup"><span data-stu-id="96c0c-109">`Exit Do` can be used only inside a `Do` loop.</span></span> <span data-ttu-id="96c0c-110">在嵌套循环内使用时 `Do` ， `Exit Do` 将退出最内层循环，并将控制转移到下一个更高的嵌套级别。</span><span class="sxs-lookup"><span data-stu-id="96c0c-110">When used within nested `Do` loops, `Exit Do` exits the innermost loop and transfers control to the next higher level of nesting.</span></span>

 `Exit For`  
 <span data-ttu-id="96c0c-111">立即退出 `For` 出现该循环的循环。</span><span class="sxs-lookup"><span data-stu-id="96c0c-111">Immediately exits the `For` loop in which it appears.</span></span> <span data-ttu-id="96c0c-112">继续执行语句后面的语句 `Next` 。</span><span class="sxs-lookup"><span data-stu-id="96c0c-112">Execution continues with the statement following the `Next` statement.</span></span> <span data-ttu-id="96c0c-113">`Exit For` 只能在 `For` ... `Next` 或 `For Each` ... `Next` 循环内使用。</span><span class="sxs-lookup"><span data-stu-id="96c0c-113">`Exit For` can be used only inside a `For`...`Next` or `For Each`...`Next` loop.</span></span> <span data-ttu-id="96c0c-114">在嵌套循环内使用时 `For` ， `Exit For` 将退出最内层循环，并将控制转移到下一个更高的嵌套级别。</span><span class="sxs-lookup"><span data-stu-id="96c0c-114">When used within nested `For` loops, `Exit For` exits the innermost loop and transfers control to the next higher level of nesting.</span></span>

 `Exit Function`  
 <span data-ttu-id="96c0c-115">会立即退出 `Function` 显示该过程。</span><span class="sxs-lookup"><span data-stu-id="96c0c-115">Immediately exits the `Function` procedure in which it appears.</span></span> <span data-ttu-id="96c0c-116">继续执行调用过程的语句后面的语句 `Function` 。</span><span class="sxs-lookup"><span data-stu-id="96c0c-116">Execution continues with the statement following the statement that called the `Function` procedure.</span></span> <span data-ttu-id="96c0c-117">`Exit Function` 只能在过程中使用 `Function` 。</span><span class="sxs-lookup"><span data-stu-id="96c0c-117">`Exit Function` can be used only inside a `Function` procedure.</span></span>

 <span data-ttu-id="96c0c-118">若要指定一个返回值，可以在语句前面的行上向函数名称赋值 `Exit Function` 。</span><span class="sxs-lookup"><span data-stu-id="96c0c-118">To specify a return value, you can assign the value to the function name on a line before the `Exit Function` statement.</span></span> <span data-ttu-id="96c0c-119">若要分配返回值并在一个语句中退出函数，可以改为使用 [Return 语句](return-statement.md)。</span><span class="sxs-lookup"><span data-stu-id="96c0c-119">To assign the return value and exit the function in one statement, you can instead use the [Return Statement](return-statement.md).</span></span>

 `Exit Property`  
 <span data-ttu-id="96c0c-120">会立即退出 `Property` 显示该过程。</span><span class="sxs-lookup"><span data-stu-id="96c0c-120">Immediately exits the `Property` procedure in which it appears.</span></span> <span data-ttu-id="96c0c-121">执行将继续执行调用过程的语句 `Property` ，即，语句请求或设置属性的值。</span><span class="sxs-lookup"><span data-stu-id="96c0c-121">Execution continues with the statement that called the `Property` procedure, that is, with the statement requesting or setting the property's value.</span></span> <span data-ttu-id="96c0c-122">`Exit Property` 只能在属性的或过程内使用 `Get` `Set` 。</span><span class="sxs-lookup"><span data-stu-id="96c0c-122">`Exit Property` can be used only inside a property's `Get` or `Set` procedure.</span></span>

 <span data-ttu-id="96c0c-123">若要在过程中指定返回值 `Get` ，可以在语句之前的行上将值分配给函数名称 `Exit Property` 。</span><span class="sxs-lookup"><span data-stu-id="96c0c-123">To specify a return value in a `Get` procedure, you can assign the value to the function name on a line before the `Exit Property` statement.</span></span> <span data-ttu-id="96c0c-124">若要分配返回值并 `Get` 在一个语句中退出该过程，可以改为使用 `Return` 语句。</span><span class="sxs-lookup"><span data-stu-id="96c0c-124">To assign the return value and exit the `Get` procedure in one statement, you can instead use the `Return` statement.</span></span>

 <span data-ttu-id="96c0c-125">在 `Set` 过程中， `Exit Property` 语句与语句等效 `Return` 。</span><span class="sxs-lookup"><span data-stu-id="96c0c-125">In a `Set` procedure, the `Exit Property` statement is equivalent to the `Return` statement.</span></span>

 `Exit Select`  
 <span data-ttu-id="96c0c-126">立即退出 `Select Case` 出现它的块。</span><span class="sxs-lookup"><span data-stu-id="96c0c-126">Immediately exits the `Select Case` block in which it appears.</span></span> <span data-ttu-id="96c0c-127">继续执行语句后面的语句 `End Select` 。</span><span class="sxs-lookup"><span data-stu-id="96c0c-127">Execution continues with the statement following the `End Select` statement.</span></span> <span data-ttu-id="96c0c-128">`Exit Select` 只能在语句内使用 `Select Case` 。</span><span class="sxs-lookup"><span data-stu-id="96c0c-128">`Exit Select` can be used only inside a `Select Case` statement.</span></span>

 `Exit Sub`  
 <span data-ttu-id="96c0c-129">会立即退出 `Sub` 显示该过程。</span><span class="sxs-lookup"><span data-stu-id="96c0c-129">Immediately exits the `Sub` procedure in which it appears.</span></span> <span data-ttu-id="96c0c-130">继续执行调用过程的语句后面的语句 `Sub` 。</span><span class="sxs-lookup"><span data-stu-id="96c0c-130">Execution continues with the statement following the statement that called the `Sub` procedure.</span></span> <span data-ttu-id="96c0c-131">`Exit Sub` 只能在过程中使用 `Sub` 。</span><span class="sxs-lookup"><span data-stu-id="96c0c-131">`Exit Sub` can be used only inside a `Sub` procedure.</span></span>

 <span data-ttu-id="96c0c-132">在 `Sub` 过程中， `Exit Sub` 语句与语句等效 `Return` 。</span><span class="sxs-lookup"><span data-stu-id="96c0c-132">In a `Sub` procedure, the `Exit Sub` statement is equivalent to the `Return` statement.</span></span>

 `Exit Try`  
 <span data-ttu-id="96c0c-133">立即退出 `Try` `Catch` 出现它的或块。</span><span class="sxs-lookup"><span data-stu-id="96c0c-133">Immediately exits the `Try` or `Catch` block in which it appears.</span></span> <span data-ttu-id="96c0c-134">`Finally`如果存在块，则继续执行，否则语句后跟语句后面的语句 `End Try` 。</span><span class="sxs-lookup"><span data-stu-id="96c0c-134">Execution continues with the `Finally` block if there is one, or with the statement following the `End Try` statement otherwise.</span></span> <span data-ttu-id="96c0c-135">`Exit Try` 只能在或块中使用 `Try` `Catch` ，不能在块内使用 `Finally` 。</span><span class="sxs-lookup"><span data-stu-id="96c0c-135">`Exit Try` can be used only inside a `Try` or `Catch` block, and not inside a `Finally` block.</span></span>

 `Exit While`  
 <span data-ttu-id="96c0c-136">立即退出 `While` 出现该循环的循环。</span><span class="sxs-lookup"><span data-stu-id="96c0c-136">Immediately exits the `While` loop in which it appears.</span></span> <span data-ttu-id="96c0c-137">继续执行语句后面的语句 `End While` 。</span><span class="sxs-lookup"><span data-stu-id="96c0c-137">Execution continues with the statement following the `End While` statement.</span></span> <span data-ttu-id="96c0c-138">`Exit While` 只能在循环内使用 `While` 。</span><span class="sxs-lookup"><span data-stu-id="96c0c-138">`Exit While` can be used only inside a `While` loop.</span></span> <span data-ttu-id="96c0c-139">在嵌套循环内使用时 `While` ，将 `Exit While` 控制转移到循环中的一个嵌套级别（发生时） `Exit While` 。</span><span class="sxs-lookup"><span data-stu-id="96c0c-139">When used within nested `While` loops, `Exit While` transfers control to the loop that is one nested level above the loop where `Exit While` occurs.</span></span>

## <a name="remarks"></a><span data-ttu-id="96c0c-140">备注</span><span class="sxs-lookup"><span data-stu-id="96c0c-140">Remarks</span></span>

<span data-ttu-id="96c0c-141">不要将 `Exit` 语句与 `End` 语句混淆。</span><span class="sxs-lookup"><span data-stu-id="96c0c-141">Do not confuse `Exit` statements with `End` statements.</span></span> <span data-ttu-id="96c0c-142">`Exit` 不定义语句的末尾。</span><span class="sxs-lookup"><span data-stu-id="96c0c-142">`Exit` does not define the end of a statement.</span></span>

## <a name="example"></a><span data-ttu-id="96c0c-143">示例</span><span class="sxs-lookup"><span data-stu-id="96c0c-143">Example</span></span>

<span data-ttu-id="96c0c-144">在下面的示例中，当变量大于100时，循环条件将停止循环 `index` 。</span><span class="sxs-lookup"><span data-stu-id="96c0c-144">In the following example, the loop condition stops the loop when the `index` variable is greater than 100.</span></span> <span data-ttu-id="96c0c-145">`If`但是，循环中的语句会导致语句在 `Exit Do` 索引变量大于10时停止循环。</span><span class="sxs-lookup"><span data-stu-id="96c0c-145">The `If` statement in the loop, however, causes the `Exit Do` statement to stop the loop when the index variable is greater than 10.</span></span>

[!code-vb[VbVbalrStatements#133](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStatements/VB/class10.vb#133)]

## <a name="example"></a><span data-ttu-id="96c0c-146">示例</span><span class="sxs-lookup"><span data-stu-id="96c0c-146">Example</span></span>

<span data-ttu-id="96c0c-147">下面的示例将返回值分配给函数名称 `myFunction` ，然后使用 `Exit Function` 从函数返回：</span><span class="sxs-lookup"><span data-stu-id="96c0c-147">The following example assigns the return value to the function name `myFunction`, and then uses `Exit Function` to return from the function:</span></span>

[!code-vb[VbVbalrStatements#23](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStatements/VB/Class1.vb#23)]

## <a name="example"></a><span data-ttu-id="96c0c-148">示例</span><span class="sxs-lookup"><span data-stu-id="96c0c-148">Example</span></span>

<span data-ttu-id="96c0c-149">下面的示例使用 [Return 语句](return-statement.md) 来分配返回值并退出函数：</span><span class="sxs-lookup"><span data-stu-id="96c0c-149">The following example uses the [Return Statement](return-statement.md) to assign the return value and exit the function:</span></span>

[!code-vb[VbVbalrStatements#24](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStatements/VB/Class1.vb#24)]

## <a name="see-also"></a><span data-ttu-id="96c0c-150">请参阅</span><span class="sxs-lookup"><span data-stu-id="96c0c-150">See also</span></span>

- [<span data-ttu-id="96c0c-151">Continue 语句</span><span class="sxs-lookup"><span data-stu-id="96c0c-151">Continue Statement</span></span>](continue-statement.md)
- [<span data-ttu-id="96c0c-152">Do...Loop 语句</span><span class="sxs-lookup"><span data-stu-id="96c0c-152">Do...Loop Statement</span></span>](do-loop-statement.md)
- [<span data-ttu-id="96c0c-153">End 语句</span><span class="sxs-lookup"><span data-stu-id="96c0c-153">End Statement</span></span>](end-statement.md)
- [<span data-ttu-id="96c0c-154">For Each...Next 语句</span><span class="sxs-lookup"><span data-stu-id="96c0c-154">For Each...Next Statement</span></span>](for-each-next-statement.md)
- [<span data-ttu-id="96c0c-155">For...Next 语句</span><span class="sxs-lookup"><span data-stu-id="96c0c-155">For...Next Statement</span></span>](for-next-statement.md)
- [<span data-ttu-id="96c0c-156">Function 语句</span><span class="sxs-lookup"><span data-stu-id="96c0c-156">Function Statement</span></span>](function-statement.md)
- [<span data-ttu-id="96c0c-157">Return 语句</span><span class="sxs-lookup"><span data-stu-id="96c0c-157">Return Statement</span></span>](return-statement.md)
- [<span data-ttu-id="96c0c-158">Stop 语句</span><span class="sxs-lookup"><span data-stu-id="96c0c-158">Stop Statement</span></span>](stop-statement.md)
- [<span data-ttu-id="96c0c-159">Sub 语句</span><span class="sxs-lookup"><span data-stu-id="96c0c-159">Sub Statement</span></span>](sub-statement.md)
- [<span data-ttu-id="96c0c-160">Try...Catch...Finally 语句</span><span class="sxs-lookup"><span data-stu-id="96c0c-160">Try...Catch...Finally Statement</span></span>](try-catch-finally-statement.md)
