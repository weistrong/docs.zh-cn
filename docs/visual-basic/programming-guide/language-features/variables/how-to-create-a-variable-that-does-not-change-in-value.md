---
description: '了解有关详细信息，请参阅如何：创建在值中不更改的变量 (Visual Basic) '
title: 如何：创建固定值变量
ms.date: 07/20/2015
helpviewer_keywords:
- variables [Visual Basic], read-only
- variables [Visual Basic], constant value
ms.assetid: 86b59266-25df-4635-ae15-9b59c411d036
ms.openlocfilehash: 0392a27249de3bf604a73c8f8aaa16caf6f1c3e2
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100481930"
---
# <a name="how-to-create-a-variable-that-does-not-change-in-value-visual-basic"></a><span data-ttu-id="b9997-103">如何：创建固定值变量 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="b9997-103">How to: Create a Variable that Does Not Change in Value (Visual Basic)</span></span>

<span data-ttu-id="b9997-104">不更改其值的变量的概念可能看似矛盾。</span><span class="sxs-lookup"><span data-stu-id="b9997-104">The notion of a variable that does not change its value might appear to be contradictory.</span></span> <span data-ttu-id="b9997-105">但在某些情况下，常量并不可行，并且具有固定值的变量很有用。</span><span class="sxs-lookup"><span data-stu-id="b9997-105">But there are situations when a constant is not feasible and it is useful to have a variable with a fixed value.</span></span> <span data-ttu-id="b9997-106">在这种情况下，可以使用 [ReadOnly](../../../language-reference/modifiers/readonly.md) 关键字定义成员变量。</span><span class="sxs-lookup"><span data-stu-id="b9997-106">In such a case you can define a member variable with the [ReadOnly](../../../language-reference/modifiers/readonly.md) keyword.</span></span>

<span data-ttu-id="b9997-107">在以下情况下，不能使用 [Const 语句](../../../language-reference/statements/const-statement.md) 来声明和分配常量值：</span><span class="sxs-lookup"><span data-stu-id="b9997-107">You cannot use the [Const Statement](../../../language-reference/statements/const-statement.md) to declare and assign a constant value in the following circumstances:</span></span>

- <span data-ttu-id="b9997-108">`Const`语句不接受要使用的数据类型</span><span class="sxs-lookup"><span data-stu-id="b9997-108">The `Const` statement does not accept the data type you want to use</span></span>

- <span data-ttu-id="b9997-109">在编译时不知道值</span><span class="sxs-lookup"><span data-stu-id="b9997-109">You do not know the value at compile time</span></span>

- <span data-ttu-id="b9997-110">在编译时无法计算常量值</span><span class="sxs-lookup"><span data-stu-id="b9997-110">You are unable to compute the constant value at compile time</span></span>

### <a name="to-create-a-variable-that-does-not-change-in-value"></a><span data-ttu-id="b9997-111">创建在值中不变的变量</span><span class="sxs-lookup"><span data-stu-id="b9997-111">To create a variable that does not change in value</span></span>

1. <span data-ttu-id="b9997-112">在模块级别，用 [Dim 语句](../../../language-reference/statements/dim-statement.md)声明成员变量，并包括 [ReadOnly](../../../language-reference/modifiers/readonly.md) 关键字。</span><span class="sxs-lookup"><span data-stu-id="b9997-112">At module level, declare a member variable with the [Dim Statement](../../../language-reference/statements/dim-statement.md), and include the [ReadOnly](../../../language-reference/modifiers/readonly.md) keyword.</span></span>

    ```vb
    Dim ReadOnly timeStarted
    ```

    <span data-ttu-id="b9997-113">`ReadOnly`只能在成员变量上指定。</span><span class="sxs-lookup"><span data-stu-id="b9997-113">You can specify `ReadOnly` only on a member variable.</span></span> <span data-ttu-id="b9997-114">这意味着必须在任何过程之外的模块级别定义变量。</span><span class="sxs-lookup"><span data-stu-id="b9997-114">This means you must define the variable at module level, outside of any procedure.</span></span>

2. <span data-ttu-id="b9997-115">如果可以在编译时在单个语句中计算该值，请在语句中使用初始化子句 `Dim` 。</span><span class="sxs-lookup"><span data-stu-id="b9997-115">If you can compute the value in a single statement at compile time, use an initialization clause in the `Dim` statement.</span></span> <span data-ttu-id="b9997-116">在 [As](../../../language-reference/statements/as-clause.md) 子句后跟一个等号 (`=`) ，后跟一个表达式。</span><span class="sxs-lookup"><span data-stu-id="b9997-116">Follow the [As](../../../language-reference/statements/as-clause.md) clause with an equal sign (`=`), followed by an expression.</span></span> <span data-ttu-id="b9997-117">确保编译器可以将此表达式计算为常数值。</span><span class="sxs-lookup"><span data-stu-id="b9997-117">Be sure the compiler can evaluate this expression to a constant value.</span></span>

    ```vb
    Dim ReadOnly timeStarted As Date = Now
    ```

    <span data-ttu-id="b9997-118">只能将一个值分配给一个 `ReadOnly` 变量。</span><span class="sxs-lookup"><span data-stu-id="b9997-118">You can assign a value to a `ReadOnly` variable only once.</span></span> <span data-ttu-id="b9997-119">完成此操作后，任何代码都不能更改其值。</span><span class="sxs-lookup"><span data-stu-id="b9997-119">Once you do so, no code can ever change its value.</span></span>

    <span data-ttu-id="b9997-120">如果你不知道编译时的值，或在编译时不能在单个语句中计算该值，则仍可在构造函数中的运行时分配该值。</span><span class="sxs-lookup"><span data-stu-id="b9997-120">If you do not know the value at compile time, or cannot compute it at compile time in a single statement, you can still assign it at run time in a constructor.</span></span> <span data-ttu-id="b9997-121">为此，必须 `ReadOnly` 在类或结构级别声明变量。</span><span class="sxs-lookup"><span data-stu-id="b9997-121">To do this, you must declare the `ReadOnly` variable at class or structure level.</span></span> <span data-ttu-id="b9997-122">在该类或结构的构造函数中，计算变量的固定值，并将其分配给变量，然后再从构造函数返回。</span><span class="sxs-lookup"><span data-stu-id="b9997-122">In the constructor for that class or structure, compute the variable's fixed value, and assign it to the variable before returning from the constructor.</span></span>

## <a name="see-also"></a><span data-ttu-id="b9997-123">请参阅</span><span class="sxs-lookup"><span data-stu-id="b9997-123">See also</span></span>

- [<span data-ttu-id="b9997-124">WriteOnly</span><span class="sxs-lookup"><span data-stu-id="b9997-124">WriteOnly</span></span>](../../../language-reference/modifiers/writeonly.md)
- [<span data-ttu-id="b9997-125">Const 语句</span><span class="sxs-lookup"><span data-stu-id="b9997-125">Const Statement</span></span>](../../../language-reference/statements/const-statement.md)
