---
description: '了解有关详细信息，请参阅如何：创建过程 (Visual Basic) '
title: 如何：创建过程
ms.date: 07/20/2015
helpviewer_keywords:
- procedures [Visual Basic], defining
- Visual Basic code, procedures
- Visual Basic code, reusing
- procedure declarations
- procedures [Visual Basic], about procedures
ms.assetid: 4f779247-0b50-47e8-9e5c-ab5cf39ac0d2
ms.openlocfilehash: bca5ad24e845600642429273f6053787dd290b88
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100472535"
---
# <a name="how-to-create-a-procedure-visual-basic"></a><span data-ttu-id="38839-103">如何：创建过程 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="38839-103">How to: Create a Procedure (Visual Basic)</span></span>

<span data-ttu-id="38839-104">在开始声明语句 (`Sub` 或 `Function`) 以及结束声明语句 (`End Sub` 或) 之间包含过程 `End Function` 。</span><span class="sxs-lookup"><span data-stu-id="38839-104">You enclose a procedure between a starting declaration statement (`Sub` or `Function`) and an ending declaration statement (`End Sub` or `End Function`).</span></span> <span data-ttu-id="38839-105">过程的所有代码都位于这些语句之间。</span><span class="sxs-lookup"><span data-stu-id="38839-105">All the procedure's code lies between these statements.</span></span>

 <span data-ttu-id="38839-106">一个过程不能包含另一个过程，所以其开始和结束语句必须在其他任何过程之外。</span><span class="sxs-lookup"><span data-stu-id="38839-106">A procedure cannot contain another procedure, so its starting and ending statements must be outside any other procedure.</span></span>

 <span data-ttu-id="38839-107">如果你的代码在不同的位置执行相同的任务，则可以将该任务作为过程写入一次，然后从代码中的不同位置调用它。</span><span class="sxs-lookup"><span data-stu-id="38839-107">If you have code that performs the same task in different places, you can write the task once as a procedure and then call it from different places in your code.</span></span>

### <a name="to-create-a-procedure-that-does-not-return-a-value"></a><span data-ttu-id="38839-108">创建不返回值的过程</span><span class="sxs-lookup"><span data-stu-id="38839-108">To create a procedure that does not return a value</span></span>

1. <span data-ttu-id="38839-109">在任何其他过程之外，使用 `Sub` 语句，然后使用 `End Sub` 语句。</span><span class="sxs-lookup"><span data-stu-id="38839-109">Outside any other procedure, use a `Sub` statement, followed by an `End Sub` statement.</span></span>

2. <span data-ttu-id="38839-110">在 `Sub` 语句中，在关键字后面跟 `Sub` 过程的名称，然后是括号中的参数列表。</span><span class="sxs-lookup"><span data-stu-id="38839-110">In the `Sub` statement, follow the `Sub` keyword with the name of the procedure, then the parameter list in parentheses.</span></span>

3. <span data-ttu-id="38839-111">将过程的代码语句放置在 `Sub` 和 `End Sub` 语句之间。</span><span class="sxs-lookup"><span data-stu-id="38839-111">Place the procedure's code statements between the `Sub` and `End Sub` statements.</span></span>

### <a name="to-create-a-procedure-that-returns-a-value"></a><span data-ttu-id="38839-112">创建返回值的过程</span><span class="sxs-lookup"><span data-stu-id="38839-112">To create a procedure that returns a value</span></span>

1. <span data-ttu-id="38839-113">在任何其他过程之外，使用 `Function` 语句，然后使用 `End Function` 语句。</span><span class="sxs-lookup"><span data-stu-id="38839-113">Outside any other procedure, use a `Function` statement, followed by an `End Function` statement.</span></span>

2. <span data-ttu-id="38839-114">在 `Function` 语句中，在关键字后面跟 `Function` 过程的名称，然后是括号中的参数列表，然后是 `As` 指定返回值的数据类型的子句。</span><span class="sxs-lookup"><span data-stu-id="38839-114">In the `Function` statement, follow the `Function` keyword with the name of the procedure, then the parameter list in parentheses, and then an `As` clause specifying the data type of the return value.</span></span>

3. <span data-ttu-id="38839-115">将过程的代码语句放置在 `Function` 和 `End Function` 语句之间。</span><span class="sxs-lookup"><span data-stu-id="38839-115">Place the procedure's code statements between the `Function` and `End Function` statements.</span></span>

4. <span data-ttu-id="38839-116">使用 `Return` 语句将值返回到调用代码。</span><span class="sxs-lookup"><span data-stu-id="38839-116">Use a `Return` statement to return the value to the calling code.</span></span>

### <a name="to-connect-your-new-procedure-with-the-old-repetitive-blocks-of-code"></a><span data-ttu-id="38839-117">将新过程与旧的、重复的代码块连接起来</span><span class="sxs-lookup"><span data-stu-id="38839-117">To connect your new procedure with the old, repetitive blocks of code</span></span>

1. <span data-ttu-id="38839-118">请确保在旧代码有权访问的位置定义新过程。</span><span class="sxs-lookup"><span data-stu-id="38839-118">Make sure you define the new procedure in a place where the old code has access to it.</span></span>

2. <span data-ttu-id="38839-119">在旧的、重复的代码块中，使用调用或过程的单个语句替换执行重复任务的语句 `Sub` `Function` 。</span><span class="sxs-lookup"><span data-stu-id="38839-119">In your old, repetitive code block, replace the statements that perform the repetitive task with a single statement that calls the `Sub` or `Function` procedure.</span></span>

3. <span data-ttu-id="38839-120">如果你的过程是 `Function` 返回值的，请确保调用语句使用返回值执行操作（例如，将其存储在变量中），否则值将丢失。</span><span class="sxs-lookup"><span data-stu-id="38839-120">If your procedure is a `Function` that returns a value, ensure that your calling statement performs an action with the returned value, such as storing it in a variable, or else the value will be lost.</span></span>

## <a name="example"></a><span data-ttu-id="38839-121">示例</span><span class="sxs-lookup"><span data-stu-id="38839-121">Example</span></span>

 <span data-ttu-id="38839-122">以下 `Function` 过程将计算直角三角形的最长边（或斜边），并给出另两个边的值：</span><span class="sxs-lookup"><span data-stu-id="38839-122">The following `Function` procedure calculates the longest side, or hypotenuse, of a right triangle, given the values for the other two sides:</span></span>

 [!code-vb[VbVbcnProcedures#1](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnProcedures/VB/Class1.vb#1)]

## <a name="see-also"></a><span data-ttu-id="38839-123">请参阅</span><span class="sxs-lookup"><span data-stu-id="38839-123">See also</span></span>

- [<span data-ttu-id="38839-124">过程</span><span class="sxs-lookup"><span data-stu-id="38839-124">Procedures</span></span>](index.md)
- [<span data-ttu-id="38839-125">Sub 过程</span><span class="sxs-lookup"><span data-stu-id="38839-125">Sub Procedures</span></span>](sub-procedures.md)
- [<span data-ttu-id="38839-126">Function 过程</span><span class="sxs-lookup"><span data-stu-id="38839-126">Function Procedures</span></span>](function-procedures.md)
- [<span data-ttu-id="38839-127">Property 过程</span><span class="sxs-lookup"><span data-stu-id="38839-127">Property Procedures</span></span>](property-procedures.md)
- [<span data-ttu-id="38839-128">运算符过程</span><span class="sxs-lookup"><span data-stu-id="38839-128">Operator Procedures</span></span>](operator-procedures.md)
- [<span data-ttu-id="38839-129">过程形参和实参</span><span class="sxs-lookup"><span data-stu-id="38839-129">Procedure Parameters and Arguments</span></span>](procedure-parameters-and-arguments.md)
- [<span data-ttu-id="38839-130">递归过程</span><span class="sxs-lookup"><span data-stu-id="38839-130">Recursive Procedures</span></span>](recursive-procedures.md)
- [<span data-ttu-id="38839-131">过程重载</span><span class="sxs-lookup"><span data-stu-id="38839-131">Procedure Overloading</span></span>](procedure-overloading.md)
- [<span data-ttu-id="38839-132">对象和类</span><span class="sxs-lookup"><span data-stu-id="38839-132">Objects and Classes</span></span>](../objects-and-classes/index.md)
- [<span data-ttu-id="38839-133">面向对象的编程 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="38839-133">Object-Oriented Programming (Visual Basic)</span></span>](../../concepts/object-oriented-programming.md)
