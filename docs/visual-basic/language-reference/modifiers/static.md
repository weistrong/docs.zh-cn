---
description: '了解详细信息：静态 (Visual Basic) '
title: Static
ms.date: 07/20/2015
f1_keywords:
- vb.Static
helpviewer_keywords:
- static modifier
- Static keyword [Visual Basic]
ms.assetid: 19013910-4658-47b6-a22e-1744b527979e
ms.openlocfilehash: 03c2e3f64ac9052a0c604b8bc34782af16edbf34
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99700736"
---
# <a name="static-visual-basic"></a><span data-ttu-id="c1bff-103">Static (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="c1bff-103">Static (Visual Basic)</span></span>

<span data-ttu-id="c1bff-104">指定一个或多个已声明的局部变量将继续存在，并在其声明过程终止后保留其最新值。</span><span class="sxs-lookup"><span data-stu-id="c1bff-104">Specifies that one or more declared local variables are to continue to exist and retain their latest values after termination of the procedure in which they are declared.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="c1bff-105">备注</span><span class="sxs-lookup"><span data-stu-id="c1bff-105">Remarks</span></span>  

 <span data-ttu-id="c1bff-106">通常，过程停止后，过程中的局部变量将立即停止存在。</span><span class="sxs-lookup"><span data-stu-id="c1bff-106">Normally, a local variable in a procedure ceases to exist as soon as the procedure stops.</span></span> <span data-ttu-id="c1bff-107">静态变量将继续存在并保留其最新值。</span><span class="sxs-lookup"><span data-stu-id="c1bff-107">A static variable continues to exist and retains its most recent value.</span></span> <span data-ttu-id="c1bff-108">当你的代码下一次调用该过程时，不会重新初始化该变量，并且它仍保留你分配给它的最新值。</span><span class="sxs-lookup"><span data-stu-id="c1bff-108">The next time your code calls the procedure, the variable is not reinitialized, and it still holds the latest value that you assigned to it.</span></span> <span data-ttu-id="c1bff-109">静态变量在定义它的类或模块的生存期内继续存在。</span><span class="sxs-lookup"><span data-stu-id="c1bff-109">A static variable continues to exist for the lifetime of the class or module that it is defined in.</span></span>  
  
## <a name="rules"></a><span data-ttu-id="c1bff-110">规则</span><span class="sxs-lookup"><span data-stu-id="c1bff-110">Rules</span></span>  
  
- <span data-ttu-id="c1bff-111">**声明上下文。**</span><span class="sxs-lookup"><span data-stu-id="c1bff-111">**Declaration Context.**</span></span> <span data-ttu-id="c1bff-112">`Static`只能在本地变量上使用。</span><span class="sxs-lookup"><span data-stu-id="c1bff-112">You can use `Static` only on local variables.</span></span> <span data-ttu-id="c1bff-113">这意味着变量的声明上下文 `Static` 必须是过程中的过程或块，而不能是源文件、命名空间、类、结构或模块。</span><span class="sxs-lookup"><span data-stu-id="c1bff-113">This means the declaration context for a `Static` variable must be a procedure or a block in a procedure, and it cannot be a source file, namespace, class, structure, or module.</span></span>  
  
     <span data-ttu-id="c1bff-114">不能 `Static` 在结构过程内使用。</span><span class="sxs-lookup"><span data-stu-id="c1bff-114">You cannot use `Static` inside a structure procedure.</span></span>  
  
- <span data-ttu-id="c1bff-115">`Static`无法推断局部变量的数据类型。</span><span class="sxs-lookup"><span data-stu-id="c1bff-115">The data types of `Static` local variables cannot be inferred.</span></span> <span data-ttu-id="c1bff-116">有关详细信息，请参阅 [局部类型推理](../../programming-guide/language-features/variables/local-type-inference.md)。</span><span class="sxs-lookup"><span data-stu-id="c1bff-116">For more information, see [Local Type Inference](../../programming-guide/language-features/variables/local-type-inference.md).</span></span>  
  
- <span data-ttu-id="c1bff-117">**组合修饰符。**</span><span class="sxs-lookup"><span data-stu-id="c1bff-117">**Combined Modifiers.**</span></span> <span data-ttu-id="c1bff-118">不能 `Static` `ReadOnly` `Shadows` `Shared` 在同一声明中同时指定、或。</span><span class="sxs-lookup"><span data-stu-id="c1bff-118">You cannot specify `Static` together with `ReadOnly`, `Shadows`, or `Shared` in the same declaration.</span></span>  
  
## <a name="behavior"></a><span data-ttu-id="c1bff-119">行为</span><span class="sxs-lookup"><span data-stu-id="c1bff-119">Behavior</span></span>  

 <span data-ttu-id="c1bff-120">在过程中声明静态变量时 `Shared` ，只有一个静态变量副本可用于整个应用程序。</span><span class="sxs-lookup"><span data-stu-id="c1bff-120">When you declare a static variable in a `Shared` procedure, only one copy of the static variable is available for the whole application.</span></span> <span data-ttu-id="c1bff-121">`Shared`使用类名称调用过程，而不是指向类的实例的变量。</span><span class="sxs-lookup"><span data-stu-id="c1bff-121">You call a `Shared` procedure by using the class name, not a variable that points to an instance of the class.</span></span>  
  
 <span data-ttu-id="c1bff-122">如果在不存在的过程中声明静态变量 `Shared` ，则该类的每个实例只有一个变量副本。</span><span class="sxs-lookup"><span data-stu-id="c1bff-122">When you declare a static variable in a procedure that isn't `Shared`, only one copy of the variable is available for each instance of the class.</span></span> <span data-ttu-id="c1bff-123">使用指向类的特定实例的变量调用非共享过程。</span><span class="sxs-lookup"><span data-stu-id="c1bff-123">You call a non-shared procedure by using a variable that points to a specific instance of the class.</span></span>  
  
## <a name="example"></a><span data-ttu-id="c1bff-124">示例</span><span class="sxs-lookup"><span data-stu-id="c1bff-124">Example</span></span>  

 <span data-ttu-id="c1bff-125">以下示例演示了 `Static` 的用法。</span><span class="sxs-lookup"><span data-stu-id="c1bff-125">The following example demonstrates the use of `Static`.</span></span>  
  
 [!code-vb[VbVbalrKeywords#5](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrKeywords/VB/Class1.vb#5)]  
  
 <span data-ttu-id="c1bff-126">`Static`变量 `totalSales` 仅初始化为0次。</span><span class="sxs-lookup"><span data-stu-id="c1bff-126">The `Static` variable `totalSales` is initialized to 0 only one time.</span></span> <span data-ttu-id="c1bff-127">每次输入时 `updateSales` ， `totalSales` 仍然具有为其计算的最新值。</span><span class="sxs-lookup"><span data-stu-id="c1bff-127">Each time that you enter `updateSales`, `totalSales` still has the most recent value that you calculated for it.</span></span>  
  
 <span data-ttu-id="c1bff-128">`Static`可以在此上下文中使用修饰符：</span><span class="sxs-lookup"><span data-stu-id="c1bff-128">The `Static` modifier can be used in this context:</span></span>  
  
 [<span data-ttu-id="c1bff-129">Dim 语句</span><span class="sxs-lookup"><span data-stu-id="c1bff-129">Dim Statement</span></span>](../statements/dim-statement.md)  
  
## <a name="see-also"></a><span data-ttu-id="c1bff-130">请参阅</span><span class="sxs-lookup"><span data-stu-id="c1bff-130">See also</span></span>

- [<span data-ttu-id="c1bff-131">Shadows</span><span class="sxs-lookup"><span data-stu-id="c1bff-131">Shadows</span></span>](shadows.md)
- [<span data-ttu-id="c1bff-132">共享</span><span class="sxs-lookup"><span data-stu-id="c1bff-132">Shared</span></span>](shared.md)
- [<span data-ttu-id="c1bff-133">Visual Basic 中的生存期</span><span class="sxs-lookup"><span data-stu-id="c1bff-133">Lifetime in Visual Basic</span></span>](../../programming-guide/language-features/declared-elements/lifetime.md)
- [<span data-ttu-id="c1bff-134">变量声明</span><span class="sxs-lookup"><span data-stu-id="c1bff-134">Variable Declaration</span></span>](../../programming-guide/language-features/variables/variable-declaration.md)
- [<span data-ttu-id="c1bff-135">结构</span><span class="sxs-lookup"><span data-stu-id="c1bff-135">Structures</span></span>](../../programming-guide/language-features/data-types/structures.md)
- [<span data-ttu-id="c1bff-136">局部类型推理</span><span class="sxs-lookup"><span data-stu-id="c1bff-136">Local Type Inference</span></span>](../../programming-guide/language-features/variables/local-type-inference.md)
- [<span data-ttu-id="c1bff-137">对象和类</span><span class="sxs-lookup"><span data-stu-id="c1bff-137">Objects and Classes</span></span>](../../programming-guide/language-features/objects-and-classes/index.md)
