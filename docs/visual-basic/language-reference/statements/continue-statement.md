---
description: '了解详细信息： Continue 语句 (Visual Basic) '
title: Continue 语句
ms.date: 07/20/2015
f1_keywords:
- vb.continue
helpviewer_keywords:
- Continue statement [Visual Basic]
- loops, transferring to next iteration
ms.assetid: 3ad00103-358b-4af3-a3a8-1b9ea0e995d3
ms.openlocfilehash: c6d67e766b2551956795803076efe639ba3c8c99
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99673864"
---
# <a name="continue-statement-visual-basic"></a><span data-ttu-id="d3c19-103">Continue 语句 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="d3c19-103">Continue Statement (Visual Basic)</span></span>

<span data-ttu-id="d3c19-104">将控制立即传输到循环的下一次迭代。</span><span class="sxs-lookup"><span data-stu-id="d3c19-104">Transfers control immediately to the next iteration of a loop.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d3c19-105">语法</span><span class="sxs-lookup"><span data-stu-id="d3c19-105">Syntax</span></span>  
  
```vb  
Continue { Do | For | While }  
```  
  
## <a name="remarks"></a><span data-ttu-id="d3c19-106">备注</span><span class="sxs-lookup"><span data-stu-id="d3c19-106">Remarks</span></span>  

 <span data-ttu-id="d3c19-107">可以从 `Do` 、或循环内传输 `For` `While` 到循环的下一次迭代。</span><span class="sxs-lookup"><span data-stu-id="d3c19-107">You can transfer from inside a `Do`, `For`, or `While` loop to the next iteration of that loop.</span></span> <span data-ttu-id="d3c19-108">控制权会立即传递到循环条件测试，这等效于将转换为 `For` 或 `While` 语句，或 `Do` `Loop` 包含或子句的或语句 `Until` `While` 。</span><span class="sxs-lookup"><span data-stu-id="d3c19-108">Control passes immediately to the loop condition test, which is equivalent to transferring to the `For` or `While` statement, or to the `Do` or `Loop` statement that contains the `Until` or `While` clause.</span></span>  
  
 <span data-ttu-id="d3c19-109">可以在 `Continue` 允许传输的循环中的任意位置使用。</span><span class="sxs-lookup"><span data-stu-id="d3c19-109">You can use `Continue` at any location in the loop that allows transfers.</span></span> <span data-ttu-id="d3c19-110">允许传输控件的规则与 [GoTo 语句](goto-statement.md)相同。</span><span class="sxs-lookup"><span data-stu-id="d3c19-110">The rules allowing transfer of control are the same as with the [GoTo Statement](goto-statement.md).</span></span>  
  
 <span data-ttu-id="d3c19-111">例如，如果循环完全包含在 `Try` 块、 `Catch` 块或 `Finally` 块中，则可以使用 `Continue` 来传出循环。</span><span class="sxs-lookup"><span data-stu-id="d3c19-111">For example, if a loop is totally contained within a `Try` block, a `Catch` block, or a `Finally` block, you can use `Continue` to transfer out of the loop.</span></span> <span data-ttu-id="d3c19-112">另一方面，如果 `Try` `End Try` 循环中包含 ... 结构，则不能使用 `Continue` 将控件从块中传输出去 `Finally` ，并且 `Try` `Catch` 仅当完全从 `Try` ... `End Try` 结构中传输时，才能使用它来传出或阻止。</span><span class="sxs-lookup"><span data-stu-id="d3c19-112">If, on the other hand, the `Try`...`End Try` structure is contained within the loop, you cannot use `Continue` to transfer control out of the `Finally` block, and you can use it to transfer out of a `Try` or `Catch` block only if you transfer completely out of the `Try`...`End Try` structure.</span></span>  
  
 <span data-ttu-id="d3c19-113">如果有相同类型的嵌套循环（例如 `Do` 另一个循环内的循环），则 `Do` 语句将 `Continue Do` 跳到包含它的最内层循环的下一次迭代 `Do` 。</span><span class="sxs-lookup"><span data-stu-id="d3c19-113">If you have nested loops of the same type, for example a `Do` loop within another `Do` loop, a `Continue Do` statement skips to the next iteration of the innermost `Do` loop that contains it.</span></span> <span data-ttu-id="d3c19-114">不能使用 `Continue` 跳到相同类型的包含循环的下一次迭代。</span><span class="sxs-lookup"><span data-stu-id="d3c19-114">You cannot use `Continue` to skip to the next iteration of a containing loop of the same type.</span></span>  
  
 <span data-ttu-id="d3c19-115">如果具有不同类型的嵌套循环（例如 `Do` 循环内的循环）， `For` 可以使用或跳到任一循环的下一次迭代 `Continue Do` `Continue For` 。</span><span class="sxs-lookup"><span data-stu-id="d3c19-115">If you have nested loops of different types, for example a `Do` loop within a `For` loop, you can skip to the next iteration of either loop by using either `Continue Do` or `Continue For`.</span></span>  
  
## <a name="example"></a><span data-ttu-id="d3c19-116">示例</span><span class="sxs-lookup"><span data-stu-id="d3c19-116">Example</span></span>  

 <span data-ttu-id="d3c19-117">下面的代码示例使用 `Continue While` 语句跳转到数组的下一列（如果除数为零）。</span><span class="sxs-lookup"><span data-stu-id="d3c19-117">The following code example uses the `Continue While` statement to skip to the next column of an array if a divisor is zero.</span></span> <span data-ttu-id="d3c19-118">在 `Continue While` `For` 循环内。</span><span class="sxs-lookup"><span data-stu-id="d3c19-118">The `Continue While` is inside a `For` loop.</span></span> <span data-ttu-id="d3c19-119">它转移到 `While col < lastcol` 语句，后者是包含循环的最内层循环的下一次迭代 `While` `For` 。</span><span class="sxs-lookup"><span data-stu-id="d3c19-119">It transfers to the `While col < lastcol` statement, which is the next iteration of the innermost `While` loop that contains the `For` loop.</span></span>  
  
 [!code-vb[VbVbalrStatements#14](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStatements/VB/Class1.vb#14)]  
  
## <a name="see-also"></a><span data-ttu-id="d3c19-120">请参阅</span><span class="sxs-lookup"><span data-stu-id="d3c19-120">See also</span></span>

- [<span data-ttu-id="d3c19-121">Do...Loop 语句</span><span class="sxs-lookup"><span data-stu-id="d3c19-121">Do...Loop Statement</span></span>](do-loop-statement.md)
- [<span data-ttu-id="d3c19-122">For...Next 语句</span><span class="sxs-lookup"><span data-stu-id="d3c19-122">For...Next Statement</span></span>](for-next-statement.md)
- [<span data-ttu-id="d3c19-123">While...End While 语句</span><span class="sxs-lookup"><span data-stu-id="d3c19-123">While...End While Statement</span></span>](while-end-while-statement.md)
- [<span data-ttu-id="d3c19-124">Try...Catch...Finally 语句</span><span class="sxs-lookup"><span data-stu-id="d3c19-124">Try...Catch...Finally Statement</span></span>](try-catch-finally-statement.md)
