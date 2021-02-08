---
description: '详细了解： Implements 子句 (Visual Basic) '
title: Implements 子句
ms.date: 07/20/2015
f1_keywords:
- vb.ImplementsClause
helpviewer_keywords:
- interface implementation [Visual Basic], reimplementation
- interface members [Visual Basic], reimplementation
- interface members [Visual Basic], Implements keyword
- interface members
- members [Visual Basic], reimplementation
- interface implementation [Visual Basic], Implements keyword
- interface members [Visual Basic], implementing
- Implements keyword [Visual Basic]
- Implements statement [Visual Basic], about Implements
- members [Visual Basic], implementing
- members [Visual Basic], Implements keyword
- reimplementation
ms.assetid: 5252cdf9-964d-4fc6-af0f-0449b7126b5a
ms.openlocfilehash: 360d8812a7c49d6462818246b1448e171dcd597f
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99768995"
---
# <a name="implements-clause-visual-basic"></a><span data-ttu-id="2ec06-103">Implements 子句 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="2ec06-103">Implements Clause (Visual Basic)</span></span>

<span data-ttu-id="2ec06-104">指示类或结构成员正在为接口中定义的成员提供实现。</span><span class="sxs-lookup"><span data-stu-id="2ec06-104">Indicates that a class or structure member is providing the implementation for a member defined in an interface.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="2ec06-105">备注</span><span class="sxs-lookup"><span data-stu-id="2ec06-105">Remarks</span></span>  

<span data-ttu-id="2ec06-106">`Implements`关键字与[Implements 语句](implements-statement.md)不同。</span><span class="sxs-lookup"><span data-stu-id="2ec06-106">The `Implements` keyword is not the same as the [Implements Statement](implements-statement.md).</span></span> <span data-ttu-id="2ec06-107">使用语句可以 `Implements` 指定类或结构实现一个或多个接口，然后，对于每个成员，使用 `Implements` 关键字指定它所实现的接口和成员。</span><span class="sxs-lookup"><span data-stu-id="2ec06-107">You use the `Implements` statement to specify that a class or structure implements one or more interfaces, and then for each member you use the `Implements` keyword to specify which interface and which member it implements.</span></span>

<span data-ttu-id="2ec06-108">如果类或结构实现了接口，则它必须紧跟在 `Implements` [类语句](class-statement.md) 或 [结构语句](structure-statement.md)之后的语句，并且必须实现该接口定义的所有成员。</span><span class="sxs-lookup"><span data-stu-id="2ec06-108">If a class or structure implements an interface, it must include the `Implements` statement immediately after the [Class Statement](class-statement.md) or [Structure Statement](structure-statement.md), and it must implement all the members defined by the interface.</span></span>

## <a name="reimplementation"></a><span data-ttu-id="2ec06-109">重新实现</span><span class="sxs-lookup"><span data-stu-id="2ec06-109">Reimplementation</span></span>  

<span data-ttu-id="2ec06-110">在派生类中，您可以重新实现基类已经实现的接口成员。</span><span class="sxs-lookup"><span data-stu-id="2ec06-110">In a derived class, you can reimplement an interface member that the base class has already implemented.</span></span> <span data-ttu-id="2ec06-111">这不同于在以下方面重写基类成员：</span><span class="sxs-lookup"><span data-stu-id="2ec06-111">This is different from overriding the base class member in the following respects:</span></span>

- <span data-ttu-id="2ec06-112">基类成员不需要是可 [重写](../modifiers/overridable.md) 的，而重新实现。</span><span class="sxs-lookup"><span data-stu-id="2ec06-112">The base class member does not need to be [Overridable](../modifiers/overridable.md) to be reimplemented.</span></span>
- <span data-ttu-id="2ec06-113">您可以使用其他名称重新实现该成员。</span><span class="sxs-lookup"><span data-stu-id="2ec06-113">You can reimplement the member with a different name.</span></span>

<span data-ttu-id="2ec06-114">`Implements`关键字可用于以下上下文：</span><span class="sxs-lookup"><span data-stu-id="2ec06-114">The `Implements` keyword can be used in the following contexts:</span></span>

- [<span data-ttu-id="2ec06-115">Event 语句</span><span class="sxs-lookup"><span data-stu-id="2ec06-115">Event Statement</span></span>](event-statement.md)
- [<span data-ttu-id="2ec06-116">Function 语句</span><span class="sxs-lookup"><span data-stu-id="2ec06-116">Function Statement</span></span>](function-statement.md)
- [<span data-ttu-id="2ec06-117">Property Statement</span><span class="sxs-lookup"><span data-stu-id="2ec06-117">Property Statement</span></span>](property-statement.md)
- [<span data-ttu-id="2ec06-118">Sub 语句</span><span class="sxs-lookup"><span data-stu-id="2ec06-118">Sub Statement</span></span>](sub-statement.md)  
  
## <a name="see-also"></a><span data-ttu-id="2ec06-119">请参阅</span><span class="sxs-lookup"><span data-stu-id="2ec06-119">See also</span></span>

- [<span data-ttu-id="2ec06-120">Implements 语句</span><span class="sxs-lookup"><span data-stu-id="2ec06-120">Implements Statement</span></span>](implements-statement.md)
- [<span data-ttu-id="2ec06-121">Interface 语句</span><span class="sxs-lookup"><span data-stu-id="2ec06-121">Interface Statement</span></span>](interface-statement.md)
- [<span data-ttu-id="2ec06-122">Class 语句</span><span class="sxs-lookup"><span data-stu-id="2ec06-122">Class Statement</span></span>](class-statement.md)
- [<span data-ttu-id="2ec06-123">Structure 语句</span><span class="sxs-lookup"><span data-stu-id="2ec06-123">Structure Statement</span></span>](structure-statement.md)
