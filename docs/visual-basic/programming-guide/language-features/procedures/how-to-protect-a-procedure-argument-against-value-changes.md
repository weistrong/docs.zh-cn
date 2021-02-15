---
description: '了解有关详细信息，请参阅如何：针对值更改保护过程参数 (Visual Basic) '
title: 如何：防止过程参数的值被更改
ms.date: 07/20/2015
helpviewer_keywords:
- procedures [Visual Basic], arguments
- procedures [Visual Basic], parameters
- procedure arguments
- arguments [Visual Basic], passing by reference
- Visual Basic code, procedures
- arguments [Visual Basic], ByVal
- arguments [Visual Basic], passing by value
- procedure parameters
- procedures [Visual Basic], calling
- arguments [Visual Basic], ByRef
- arguments [Visual Basic], changing value
ms.assetid: d2b7c766-ce16-4d2c-8d79-3fc0e7ba2227
ms.openlocfilehash: 2e47a584632f124a001617770aeae5104ef20abe
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100476210"
---
# <a name="how-to-protect-a-procedure-argument-against-value-changes-visual-basic"></a><span data-ttu-id="c619a-103">如何：防止过程自变量的值被更改 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="c619a-103">How to: Protect a Procedure Argument Against Value Changes (Visual Basic)</span></span>

<span data-ttu-id="c619a-104">如果过程将参数声明为 [ByRef](../../../language-reference/modifiers/byref.md)，Visual Basic 将为过程代码提供对调用代码中参数的基础编程元素的直接引用。</span><span class="sxs-lookup"><span data-stu-id="c619a-104">If a procedure declares a parameter as [ByRef](../../../language-reference/modifiers/byref.md), Visual Basic gives the procedure code a direct reference to the programming element underlying the argument in the calling code.</span></span> <span data-ttu-id="c619a-105">这允许过程更改调用代码中参数的基础值。</span><span class="sxs-lookup"><span data-stu-id="c619a-105">This permits the procedure to change the value underlying the argument in the calling code.</span></span> <span data-ttu-id="c619a-106">在某些情况下，调用代码可能需要防止这种更改。</span><span class="sxs-lookup"><span data-stu-id="c619a-106">In some cases the calling code might want to protect against such a change.</span></span>  
  
 <span data-ttu-id="c619a-107">始终可以通过在过程中声明相应的参数 [ByVal](../../../language-reference/modifiers/byval.md) ，来保护参数不受更改。</span><span class="sxs-lookup"><span data-stu-id="c619a-107">You can always protect an argument from change by declaring the corresponding parameter [ByVal](../../../language-reference/modifiers/byval.md) in the procedure.</span></span> <span data-ttu-id="c619a-108">如果希望能够在某些情况下更改给定的自变量，而不是其他情况，则可以声明该参数， `ByRef` 并让调用代码确定每个调用中的传递机制。</span><span class="sxs-lookup"><span data-stu-id="c619a-108">If you want to be able to change a given argument in some cases but not others, you can declare it `ByRef` and let the calling code determine the passing mechanism in each call.</span></span> <span data-ttu-id="c619a-109">为此，可将相应的自变量括在括号中，以便按值传递它，或者不将其括在括号中，以便通过引用传递它。</span><span class="sxs-lookup"><span data-stu-id="c619a-109">It does this by enclosing the corresponding argument in parentheses to pass it by value, or not enclosing it in parentheses to pass it by reference.</span></span> <span data-ttu-id="c619a-110">有关详细信息，请参阅 [如何：强制通过值传递参数](./how-to-force-an-argument-to-be-passed-by-value.md)。</span><span class="sxs-lookup"><span data-stu-id="c619a-110">For more information, see [How to: Force an Argument to Be Passed by Value](./how-to-force-an-argument-to-be-passed-by-value.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="c619a-111">示例</span><span class="sxs-lookup"><span data-stu-id="c619a-111">Example</span></span>  

 <span data-ttu-id="c619a-112">下面的示例演示了两个过程，这些过程使用数组变量并对其元素进行操作。</span><span class="sxs-lookup"><span data-stu-id="c619a-112">The following example shows two procedures that take an array variable and operate on its elements.</span></span> <span data-ttu-id="c619a-113">此 `increase` 过程只是向每个元素添加一个元素。</span><span class="sxs-lookup"><span data-stu-id="c619a-113">The `increase` procedure simply adds one to each element.</span></span> <span data-ttu-id="c619a-114">此 `replace` 过程将新数组分配给参数 `a()` ，然后将一个数组添加到每个元素。</span><span class="sxs-lookup"><span data-stu-id="c619a-114">The `replace` procedure assigns a new array to the parameter `a()` and then adds one to each element.</span></span> <span data-ttu-id="c619a-115">但是，重新分配不会影响调用代码中的基础数组变量。</span><span class="sxs-lookup"><span data-stu-id="c619a-115">However, the reassignment does not affect the underlying array variable in the calling code.</span></span>  
  
 [!code-vb[VbVbcnProcedures#35](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnProcedures/VB/Class1.vb#35)]  
  
 [!code-vb[VbVbcnProcedures#38](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnProcedures/VB/Class1.vb#38)]  
  
 [!code-vb[VbVbcnProcedures#37](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnProcedures/VB/Class1.vb#37)]  
  
 <span data-ttu-id="c619a-116">第一次 `MsgBox` 调用显示 "增加 (n) ：11，21，31，41" 之后。</span><span class="sxs-lookup"><span data-stu-id="c619a-116">The first `MsgBox` call displays "After increase(n): 11, 21, 31, 41".</span></span> <span data-ttu-id="c619a-117">由于数组 `n` 是引用类型，因此 `increase` 即使传递机制为，也可以更改其成员 `ByVal` 。</span><span class="sxs-lookup"><span data-stu-id="c619a-117">Because the array `n` is a reference type, `increase` can change its members, even though the passing mechanism is `ByVal`.</span></span>  
  
 <span data-ttu-id="c619a-118">第二次 `MsgBox` 调用显示 "replace (n) ：11，21，31，41" 之后。</span><span class="sxs-lookup"><span data-stu-id="c619a-118">The second `MsgBox` call displays "After replace(n): 11, 21, 31, 41".</span></span> <span data-ttu-id="c619a-119">由于 `n` 已传递 `ByVal` ，因此 `replace` 无法 `n` 通过向其分配新数组来修改调用代码中的变量。</span><span class="sxs-lookup"><span data-stu-id="c619a-119">Because `n` is passed `ByVal`, `replace` cannot modify the variable `n` in the calling code by assigning a new array to it.</span></span> <span data-ttu-id="c619a-120">当 `replace` 创建新的数组实例 `k` 并将其分配给本地变量时 `a` ，它将失去 `n` 调用代码传入的引用。</span><span class="sxs-lookup"><span data-stu-id="c619a-120">When `replace` creates the new array instance `k` and assigns it to the local variable `a`, it loses the reference to `n` passed in by the calling code.</span></span> <span data-ttu-id="c619a-121">当它更改的成员时 `a` ，只 `k` 会影响本地数组。</span><span class="sxs-lookup"><span data-stu-id="c619a-121">When it changes the members of `a`, only the local array `k` is affected.</span></span> <span data-ttu-id="c619a-122">因此，不 `replace` 会 `n` 在调用代码中递增数组的值。</span><span class="sxs-lookup"><span data-stu-id="c619a-122">Therefore, `replace` does not increment the values of array `n` in the calling code.</span></span>  
  
## <a name="compile-the-code"></a><span data-ttu-id="c619a-123">编译代码</span><span class="sxs-lookup"><span data-stu-id="c619a-123">Compile the code</span></span>  

 <span data-ttu-id="c619a-124">Visual Basic 中的默认值是按值传递参数。</span><span class="sxs-lookup"><span data-stu-id="c619a-124">The default in Visual Basic is to pass arguments by value.</span></span> <span data-ttu-id="c619a-125">但是，将 [ByVal](../../../language-reference/modifiers/byval.md) 或 [ByRef](../../../language-reference/modifiers/byref.md) 关键字用于每个声明的参数是一种好的编程做法。</span><span class="sxs-lookup"><span data-stu-id="c619a-125">However, it is good programming practice to include either the [ByVal](../../../language-reference/modifiers/byval.md) or [ByRef](../../../language-reference/modifiers/byref.md) keyword with every declared parameter.</span></span> <span data-ttu-id="c619a-126">这使代码更易于阅读。</span><span class="sxs-lookup"><span data-stu-id="c619a-126">This makes your code easier to read.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c619a-127">请参阅</span><span class="sxs-lookup"><span data-stu-id="c619a-127">See also</span></span>

- [<span data-ttu-id="c619a-128">过程</span><span class="sxs-lookup"><span data-stu-id="c619a-128">Procedures</span></span>](./index.md)
- [<span data-ttu-id="c619a-129">过程形参和实参</span><span class="sxs-lookup"><span data-stu-id="c619a-129">Procedure Parameters and Arguments</span></span>](./procedure-parameters-and-arguments.md)
- [<span data-ttu-id="c619a-130">如何：将参数传递给过程</span><span class="sxs-lookup"><span data-stu-id="c619a-130">How to: Pass Arguments to a Procedure</span></span>](./how-to-pass-arguments-to-a-procedure.md)
- [<span data-ttu-id="c619a-131">按值和按引用传递参数</span><span class="sxs-lookup"><span data-stu-id="c619a-131">Passing Arguments by Value and by Reference</span></span>](./passing-arguments-by-value-and-by-reference.md)
- [<span data-ttu-id="c619a-132">可修改和不可修改参数之间的差异</span><span class="sxs-lookup"><span data-stu-id="c619a-132">Differences Between Modifiable and Nonmodifiable Arguments</span></span>](./differences-between-modifiable-and-nonmodifiable-arguments.md)
- [<span data-ttu-id="c619a-133">通过值传递参数和通过引用传递参数之间的差异</span><span class="sxs-lookup"><span data-stu-id="c619a-133">Differences Between Passing an Argument By Value and By Reference</span></span>](./differences-between-passing-an-argument-by-value-and-by-reference.md)
- [<span data-ttu-id="c619a-134">如何：更改过程参数的值</span><span class="sxs-lookup"><span data-stu-id="c619a-134">How to: Change the Value of a Procedure Argument</span></span>](./how-to-change-the-value-of-a-procedure-argument.md)
- [<span data-ttu-id="c619a-135">如何：强制通过值传递参数</span><span class="sxs-lookup"><span data-stu-id="c619a-135">How to: Force an Argument to Be Passed by Value</span></span>](./how-to-force-an-argument-to-be-passed-by-value.md)
- [<span data-ttu-id="c619a-136">按位置和按名称传递自变量</span><span class="sxs-lookup"><span data-stu-id="c619a-136">Passing Arguments by Position and by Name</span></span>](./passing-arguments-by-position-and-by-name.md)
- [<span data-ttu-id="c619a-137">Value Types and Reference Types</span><span class="sxs-lookup"><span data-stu-id="c619a-137">Value Types and Reference Types</span></span>](../data-types/value-types-and-reference-types.md)
