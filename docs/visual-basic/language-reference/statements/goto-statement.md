---
description: 了解详细信息： GoTo 语句
title: GoTo 语句
ms.date: 07/20/2015
f1_keywords:
- vb.GoTo
helpviewer_keywords:
- GoTo statement [Visual Basic]
- control flow [Visual Basic], branching
- unconditional branching [Visual Basic]
- branching [Visual Basic]
- branching [Visual Basic], unconditional
- branching [Visual Basic], conditional
- conditional statements [Visual Basic], GoTo statement
- GoTo statement [Visual Basic], syntax
ms.assetid: 313274c2-8ab3-4b9c-9ba3-0fd6798e4f6d
ms.openlocfilehash: 804baec130111562225b09cbdc7b5fb2d73adba5
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99769047"
---
# <a name="goto-statement"></a><span data-ttu-id="53485-103">GoTo 语句</span><span class="sxs-lookup"><span data-stu-id="53485-103">GoTo Statement</span></span>

<span data-ttu-id="53485-104">无条件地分支到过程中的指定行。</span><span class="sxs-lookup"><span data-stu-id="53485-104">Branches unconditionally to a specified line in a procedure.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="53485-105">语法</span><span class="sxs-lookup"><span data-stu-id="53485-105">Syntax</span></span>  
  
```vb  
GoTo line  
```  
  
## <a name="part"></a><span data-ttu-id="53485-106">组成部分</span><span class="sxs-lookup"><span data-stu-id="53485-106">Part</span></span>  

 `line`  
 <span data-ttu-id="53485-107">必需。</span><span class="sxs-lookup"><span data-stu-id="53485-107">Required.</span></span> <span data-ttu-id="53485-108">任何行标签。</span><span class="sxs-lookup"><span data-stu-id="53485-108">Any line label.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="53485-109">备注</span><span class="sxs-lookup"><span data-stu-id="53485-109">Remarks</span></span>  

 <span data-ttu-id="53485-110">`GoTo`语句只能分支到其出现的过程中的行。</span><span class="sxs-lookup"><span data-stu-id="53485-110">The `GoTo` statement can branch only to lines in the procedure in which it appears.</span></span> <span data-ttu-id="53485-111">该行必须具有可引用的行标签 `GoTo` 。</span><span class="sxs-lookup"><span data-stu-id="53485-111">The line must have a line label that `GoTo` can refer to.</span></span> <span data-ttu-id="53485-112">有关详细信息，请参阅 [如何：标签语句](../../programming-guide/program-structure/how-to-label-statements.md)。</span><span class="sxs-lookup"><span data-stu-id="53485-112">For more information, see [How to: Label Statements](../../programming-guide/program-structure/how-to-label-statements.md).</span></span>  
  
> [!NOTE]
> <span data-ttu-id="53485-113">`GoTo` 语句可以使代码难以阅读和维护。</span><span class="sxs-lookup"><span data-stu-id="53485-113">`GoTo` statements can make code difficult to read and maintain.</span></span> <span data-ttu-id="53485-114">请尽可能使用控制结构。</span><span class="sxs-lookup"><span data-stu-id="53485-114">Whenever possible, use a control structure instead.</span></span> <span data-ttu-id="53485-115">有关详细信息，请参阅 [Control Flow](../../programming-guide/language-features/control-flow/index.md)。</span><span class="sxs-lookup"><span data-stu-id="53485-115">For more information, see [Control Flow](../../programming-guide/language-features/control-flow/index.md).</span></span>  
  
 <span data-ttu-id="53485-116">不能使用 `GoTo` 语句从 `For` ...、 `Next` `For Each` ... `Next` `SyncLock` `End SyncLock` `Try` `Catch` 、... ... ... ... ... ... .。。... `Finally` 、 `With` ... `End With` 或 `Using` ... `End Using` 构造中的标签。</span><span class="sxs-lookup"><span data-stu-id="53485-116">You cannot use a `GoTo` statement to branch from outside a `For`...`Next`, `For Each`...`Next`, `SyncLock`...`End SyncLock`, `Try`...`Catch`...`Finally`, `With`...`End With`, or `Using`...`End Using` construction to a label inside.</span></span>  
  
## <a name="branching-and-try-constructions"></a><span data-ttu-id="53485-117">分支和尝试构造</span><span class="sxs-lookup"><span data-stu-id="53485-117">Branching and Try Constructions</span></span>  

 <span data-ttu-id="53485-118">在 `Try` ... `Catch`...`Finally` 构造，以下规则适用于使用语句的分支 `GoTo` 。</span><span class="sxs-lookup"><span data-stu-id="53485-118">Within a `Try`...`Catch`...`Finally` construction, the following rules apply to branching with the `GoTo` statement.</span></span>  
  
|<span data-ttu-id="53485-119">块或区域</span><span class="sxs-lookup"><span data-stu-id="53485-119">Block or region</span></span>|<span data-ttu-id="53485-120">从外部分支</span><span class="sxs-lookup"><span data-stu-id="53485-120">Branching in from outside</span></span>|<span data-ttu-id="53485-121">从内部分支出</span><span class="sxs-lookup"><span data-stu-id="53485-121">Branching out from inside</span></span>|  
|---------------------|-------------------------------|-------------------------------|  
|<span data-ttu-id="53485-122">`Try` 模块</span><span class="sxs-lookup"><span data-stu-id="53485-122">`Try` block</span></span>|<span data-ttu-id="53485-123">仅从 `Catch` 同一构造的块 <sup>1</sup></span><span class="sxs-lookup"><span data-stu-id="53485-123">Only from a `Catch` block of the same construction <sup>1</sup></span></span>|<span data-ttu-id="53485-124">仅限于整个构造之外</span><span class="sxs-lookup"><span data-stu-id="53485-124">Only to outside the whole construction</span></span>|  
|<span data-ttu-id="53485-125">`Catch` 模块</span><span class="sxs-lookup"><span data-stu-id="53485-125">`Catch` block</span></span>|<span data-ttu-id="53485-126">不允许</span><span class="sxs-lookup"><span data-stu-id="53485-126">Never allowed</span></span>|<span data-ttu-id="53485-127">仅对整个构造以外的或 `Try` 相同构造<sup>1</sup>的块</span><span class="sxs-lookup"><span data-stu-id="53485-127">Only to outside the whole construction, or to the `Try` block of the same construction <sup>1</sup></span></span>|  
|<span data-ttu-id="53485-128">`Finally` 模块</span><span class="sxs-lookup"><span data-stu-id="53485-128">`Finally` block</span></span>|<span data-ttu-id="53485-129">不允许</span><span class="sxs-lookup"><span data-stu-id="53485-129">Never allowed</span></span>|<span data-ttu-id="53485-130">不允许</span><span class="sxs-lookup"><span data-stu-id="53485-130">Never allowed</span></span>|  
  
 <span data-ttu-id="53485-131"><sup>1</sup> （如果 `Try` 有 `Catch` ） .。。...`Finally` 构造嵌套在另一个块中， `Catch` 块可以 `Try` 在其自身的嵌套级别（而不是其他块）分支到块 `Try` 。</span><span class="sxs-lookup"><span data-stu-id="53485-131"><sup>1</sup> If one `Try`...`Catch`...`Finally` construction is nested within another, a `Catch` block can branch into the `Try` block at its own nesting level, but not into any other `Try` block.</span></span> <span data-ttu-id="53485-132">嵌套 `Try` ... `Catch`...`Finally` 构造必须完全包含在 `Try` `Catch` 它所嵌套到的构造内或块中。</span><span class="sxs-lookup"><span data-stu-id="53485-132">A nested `Try`...`Catch`...`Finally` construction must be contained completely in a `Try` or `Catch` block of the construction within which it is nested.</span></span>  
  
 <span data-ttu-id="53485-133">下图显示了一个 `Try` 嵌套在另一个构造内的构造。</span><span class="sxs-lookup"><span data-stu-id="53485-133">The following illustration shows one `Try` construction nested within another.</span></span> <span data-ttu-id="53485-134">这两个构造的块中的各种分支都指示为有效或无效。</span><span class="sxs-lookup"><span data-stu-id="53485-134">Various branches among the blocks of the two constructions are indicated as valid or invalid.</span></span>  
  
 ![Try 结构分支示意图](./media/goto-statement/try-construction-branching.gif)  
  
## <a name="example"></a><span data-ttu-id="53485-136">示例</span><span class="sxs-lookup"><span data-stu-id="53485-136">Example</span></span>  

 <span data-ttu-id="53485-137">下面的示例使用 `GoTo` 语句分支到过程中的行标签。</span><span class="sxs-lookup"><span data-stu-id="53485-137">The following example uses the `GoTo` statement to branch to line labels in a procedure.</span></span>  
  
 [!code-vb[VbVbalrStatements#31](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStatements/VB/Class1.vb#31)]  
  
## <a name="see-also"></a><span data-ttu-id="53485-138">请参阅</span><span class="sxs-lookup"><span data-stu-id="53485-138">See also</span></span>

- [<span data-ttu-id="53485-139">Do...Loop 语句</span><span class="sxs-lookup"><span data-stu-id="53485-139">Do...Loop Statement</span></span>](do-loop-statement.md)
- [<span data-ttu-id="53485-140">For...Next 语句</span><span class="sxs-lookup"><span data-stu-id="53485-140">For...Next Statement</span></span>](for-next-statement.md)
- [<span data-ttu-id="53485-141">For Each...Next 语句</span><span class="sxs-lookup"><span data-stu-id="53485-141">For Each...Next Statement</span></span>](for-each-next-statement.md)
- [<span data-ttu-id="53485-142">If...Then...Else 语句</span><span class="sxs-lookup"><span data-stu-id="53485-142">If...Then...Else Statement</span></span>](if-then-else-statement.md)
- [<span data-ttu-id="53485-143">Select...Case 语句</span><span class="sxs-lookup"><span data-stu-id="53485-143">Select...Case Statement</span></span>](select-case-statement.md)
- [<span data-ttu-id="53485-144">Try...Catch...Finally 语句</span><span class="sxs-lookup"><span data-stu-id="53485-144">Try...Catch...Finally Statement</span></span>](try-catch-finally-statement.md)
- [<span data-ttu-id="53485-145">While...End While 语句</span><span class="sxs-lookup"><span data-stu-id="53485-145">While...End While Statement</span></span>](while-end-while-statement.md)
- [<span data-ttu-id="53485-146">With...End With 语句</span><span class="sxs-lookup"><span data-stu-id="53485-146">With...End With Statement</span></span>](with-end-with-statement.md)
