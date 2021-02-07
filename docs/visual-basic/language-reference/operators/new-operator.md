---
description: '了解详细信息： New Operator (Visual Basic) '
title: New 运算符
ms.date: 07/20/2015
f1_keywords:
- vb.new
- vb.NewConstraint
helpviewer_keywords:
- constraints, Visual Basic generic types
- generics [Visual Basic], constraints
- constraints, New keyword [Visual Basic]
- New constraint
- New keyword [Visual Basic]
ms.assetid: d7d566d7-fe0e-4336-91f7-641a542de4d0
ms.openlocfilehash: f52dd7606127c7587173de8a78e618ceb3e4681d
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99665375"
---
# <a name="new-operator-visual-basic"></a><span data-ttu-id="bfedd-103">New 运算符 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="bfedd-103">New Operator (Visual Basic)</span></span>

<span data-ttu-id="bfedd-104">引入一个 `New` 子句，用于创建新的对象实例，指定类型参数上的构造函数约束，或将 `Sub` 过程标识为类构造函数。</span><span class="sxs-lookup"><span data-stu-id="bfedd-104">Introduces a `New` clause to create a new object instance, specifies a constructor constraint on a type parameter, or identifies a `Sub` procedure as a class constructor.</span></span>

## <a name="remarks"></a><span data-ttu-id="bfedd-105">备注</span><span class="sxs-lookup"><span data-stu-id="bfedd-105">Remarks</span></span>

<span data-ttu-id="bfedd-106">在声明或赋值语句中， `New` 子句必须指定一个已定义的类，可从中创建实例。</span><span class="sxs-lookup"><span data-stu-id="bfedd-106">In a declaration or assignment statement, a `New` clause must specify a defined class from which the instance can be created.</span></span> <span data-ttu-id="bfedd-107">这意味着，该类必须公开调用代码可以访问的一个或多个构造函数。</span><span class="sxs-lookup"><span data-stu-id="bfedd-107">This means that the class must expose one or more constructors that the calling code can access.</span></span>

<span data-ttu-id="bfedd-108">可 `New` 在声明语句或赋值语句中使用子句。</span><span class="sxs-lookup"><span data-stu-id="bfedd-108">You can use a `New` clause in a declaration statement or an assignment statement.</span></span> <span data-ttu-id="bfedd-109">当语句运行时，它将调用指定类的适当构造函数，同时传递您提供的任何自变量。</span><span class="sxs-lookup"><span data-stu-id="bfedd-109">When the statement runs, it calls the appropriate constructor of the specified class, passing any arguments you have supplied.</span></span> <span data-ttu-id="bfedd-110">下面的示例通过创建一个 `Customer` 具有两个构造函数的类的实例进行演示，其中一个构造函数不采用任何参数，另一个采用字符串参数：</span><span class="sxs-lookup"><span data-stu-id="bfedd-110">The following example demonstrates this by creating instances of a `Customer` class that has two constructors, one that takes no parameters and one that takes a string parameter:</span></span>

[!code-vb[VbVbalrKeywords#11](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrKeywords/VB/Class6.vb#11)]

<span data-ttu-id="bfedd-111">由于数组是类，因此 `New` 可以创建新的数组实例，如以下示例中所示：</span><span class="sxs-lookup"><span data-stu-id="bfedd-111">Since arrays are classes, `New` can create a new array instance, as shown in the following example:</span></span>

[!code-vb[VbVbalrKeywords#12](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrKeywords/VB/Class6.vb#12)]

<span data-ttu-id="bfedd-112"><xref:System.OutOfMemoryException>如果没有足够的内存来创建新的实例，则公共语言运行时 (CLR) 会引发错误。</span><span class="sxs-lookup"><span data-stu-id="bfedd-112">The common language runtime (CLR) throws an <xref:System.OutOfMemoryException> error if there is insufficient memory to create the new instance.</span></span>

> [!NOTE]
> <span data-ttu-id="bfedd-113">`New`关键字还用于类型参数列表，用于指定提供的类型必须公开可访问的无参数构造函数。</span><span class="sxs-lookup"><span data-stu-id="bfedd-113">The `New` keyword is also used in type parameter lists to specify that the supplied type must expose an accessible parameterless constructor.</span></span> <span data-ttu-id="bfedd-114">有关类型参数和约束的详细信息，请参阅 [Type List](../statements/type-list.md)。</span><span class="sxs-lookup"><span data-stu-id="bfedd-114">For more information about type parameters and constraints, see [Type List](../statements/type-list.md).</span></span>

<span data-ttu-id="bfedd-115">若要为类创建构造函数过程，请将过程的名称设置 `Sub` 为 `New` 关键字。</span><span class="sxs-lookup"><span data-stu-id="bfedd-115">To create a constructor procedure for a class, set the name of a `Sub` procedure to the `New` keyword.</span></span> <span data-ttu-id="bfedd-116">有关详细信息，请参阅 [对象生存期：如何创建和销毁对象](../../programming-guide/language-features/objects-and-classes/object-lifetime-how-objects-are-created-and-destroyed.md)。</span><span class="sxs-lookup"><span data-stu-id="bfedd-116">For more information, see [Object Lifetime: How Objects Are Created and Destroyed](../../programming-guide/language-features/objects-and-classes/object-lifetime-how-objects-are-created-and-destroyed.md).</span></span>

<span data-ttu-id="bfedd-117">`New` 关键字可用于以下上下文中：</span><span class="sxs-lookup"><span data-stu-id="bfedd-117">The `New` keyword can be used in these contexts:</span></span>

- [<span data-ttu-id="bfedd-118">Dim 语句</span><span class="sxs-lookup"><span data-stu-id="bfedd-118">Dim Statement</span></span>](../statements/dim-statement.md)
- [<span data-ttu-id="bfedd-119">个</span><span class="sxs-lookup"><span data-stu-id="bfedd-119">Of</span></span>](../statements/of-clause.md)
- [<span data-ttu-id="bfedd-120">Sub 语句</span><span class="sxs-lookup"><span data-stu-id="bfedd-120">Sub Statement</span></span>](../statements/sub-statement.md)

## <a name="see-also"></a><span data-ttu-id="bfedd-121">请参阅</span><span class="sxs-lookup"><span data-stu-id="bfedd-121">See also</span></span>

- <xref:System.OutOfMemoryException>
- [<span data-ttu-id="bfedd-122">关键字</span><span class="sxs-lookup"><span data-stu-id="bfedd-122">Keywords</span></span>](../keywords/index.md)
- [<span data-ttu-id="bfedd-123">Type List</span><span class="sxs-lookup"><span data-stu-id="bfedd-123">Type List</span></span>](../statements/type-list.md)
- [<span data-ttu-id="bfedd-124">Generic Types in Visual Basic</span><span class="sxs-lookup"><span data-stu-id="bfedd-124">Generic Types in Visual Basic</span></span>](../../programming-guide/language-features/data-types/generic-types.md)
- [<span data-ttu-id="bfedd-125">对象生存期：如何创建和销毁对象</span><span class="sxs-lookup"><span data-stu-id="bfedd-125">Object Lifetime: How Objects Are Created and Destroyed</span></span>](../../programming-guide/language-features/objects-and-classes/object-lifetime-how-objects-are-created-and-destroyed.md)
