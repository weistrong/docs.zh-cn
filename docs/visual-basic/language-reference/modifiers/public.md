---
description: '了解详细信息：公用 (Visual Basic) '
title: 公共
ms.date: 07/20/2015
f1_keywords:
- vb.Public
helpviewer_keywords:
- Public keyword [Visual Basic]
- Public keyword [Visual Basic], syntax
- Public access modifier
ms.assetid: 284c9e1b-ed23-499b-9bc9-ad87c11485a5
ms.openlocfilehash: 1083ca877cf99917291523fe10f6561784ff06a2
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99700918"
---
# <a name="public-visual-basic"></a><span data-ttu-id="5fa80-103">Public (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="5fa80-103">Public (Visual Basic)</span></span>

<span data-ttu-id="5fa80-104">指定一个或多个已声明的编程元素不具有访问限制。</span><span class="sxs-lookup"><span data-stu-id="5fa80-104">Specifies that one or more declared programming elements have no access restrictions.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="5fa80-105">备注</span><span class="sxs-lookup"><span data-stu-id="5fa80-105">Remarks</span></span>  

 <span data-ttu-id="5fa80-106">如果要发布一个组件或一组组件（如类库），通常会希望与程序集互操作的任何代码都可以访问编程元素。</span><span class="sxs-lookup"><span data-stu-id="5fa80-106">If you are publishing a component or set of components, such as a class library, you usually want the programming elements to be accessible by any code that interoperates with your assembly.</span></span> <span data-ttu-id="5fa80-107">若要在某个元素上协商这种无限制的访问权限，可以使用对其进行声明 `Public` 。</span><span class="sxs-lookup"><span data-stu-id="5fa80-107">To confer such unlimited access on an element, you can declare it with `Public`.</span></span>  
  
 <span data-ttu-id="5fa80-108">当不需要限制对编程元素的访问权限时，公共访问是该元素的正常级别。</span><span class="sxs-lookup"><span data-stu-id="5fa80-108">Public access is the normal level for a programming element when you do not need to limit access to it.</span></span> <span data-ttu-id="5fa80-109">请注意，在接口、模块、类或结构中声明的元素的访问级别默认为（ `Public` 如果你未声明）。</span><span class="sxs-lookup"><span data-stu-id="5fa80-109">Note that the access level of an element declared within an interface, module, class, or structure defaults to `Public` if you do not declare it otherwise.</span></span>  
  
## <a name="rules"></a><span data-ttu-id="5fa80-110">规则</span><span class="sxs-lookup"><span data-stu-id="5fa80-110">Rules</span></span>  
  
- <span data-ttu-id="5fa80-111">**声明上下文。**</span><span class="sxs-lookup"><span data-stu-id="5fa80-111">**Declaration Context.**</span></span> <span data-ttu-id="5fa80-112">`Public`只能在模块、接口或命名空间级别使用。</span><span class="sxs-lookup"><span data-stu-id="5fa80-112">You can use `Public` only at module, interface, or namespace level.</span></span> <span data-ttu-id="5fa80-113">这意味着元素的声明上下文 `Public` 必须是源文件、命名空间、接口、模块、类或结构，不能是过程。</span><span class="sxs-lookup"><span data-stu-id="5fa80-113">This means the declaration context for a `Public` element must be a source file, namespace, interface, module, class, or structure, and cannot be a procedure.</span></span>  
  
## <a name="behavior"></a><span data-ttu-id="5fa80-114">行为</span><span class="sxs-lookup"><span data-stu-id="5fa80-114">Behavior</span></span>  
  
- <span data-ttu-id="5fa80-115">**访问级别。**</span><span class="sxs-lookup"><span data-stu-id="5fa80-115">**Access Level.**</span></span> <span data-ttu-id="5fa80-116">可以访问模块、类或结构的所有代码都可以访问其 `Public` 元素。</span><span class="sxs-lookup"><span data-stu-id="5fa80-116">All code that can access a module, class, or structure can access its `Public` elements.</span></span>  
  
- <span data-ttu-id="5fa80-117">**默认访问权限。**</span><span class="sxs-lookup"><span data-stu-id="5fa80-117">**Default Access.**</span></span> <span data-ttu-id="5fa80-118">过程中的局部变量默认为公共访问，您不能对其使用任何访问修饰符。</span><span class="sxs-lookup"><span data-stu-id="5fa80-118">Local variables inside a procedure default to public access, and you cannot use any access modifiers on them.</span></span>  
  
- <span data-ttu-id="5fa80-119">**访问修饰符。**</span><span class="sxs-lookup"><span data-stu-id="5fa80-119">**Access Modifiers.**</span></span> <span data-ttu-id="5fa80-120">指定访问级别的关键字称为 *访问修饰符*。</span><span class="sxs-lookup"><span data-stu-id="5fa80-120">The keywords that specify access level are called *access modifiers*.</span></span> <span data-ttu-id="5fa80-121">有关访问修饰符的比较，请参阅 [Visual Basic 中的访问级别](../../programming-guide/language-features/declared-elements/access-levels.md)。</span><span class="sxs-lookup"><span data-stu-id="5fa80-121">For a comparison of the access modifiers, see [Access levels in Visual Basic](../../programming-guide/language-features/declared-elements/access-levels.md).</span></span>  
  
 <span data-ttu-id="5fa80-122">`Public` 修饰符可用于下面的上下文中：</span><span class="sxs-lookup"><span data-stu-id="5fa80-122">The `Public` modifier can be used in these contexts:</span></span>  
  
 [<span data-ttu-id="5fa80-123">Class 语句</span><span class="sxs-lookup"><span data-stu-id="5fa80-123">Class Statement</span></span>](../statements/class-statement.md)  
  
 [<span data-ttu-id="5fa80-124">Const 语句</span><span class="sxs-lookup"><span data-stu-id="5fa80-124">Const Statement</span></span>](../statements/const-statement.md)  
  
 [<span data-ttu-id="5fa80-125">Declare Statement</span><span class="sxs-lookup"><span data-stu-id="5fa80-125">Declare Statement</span></span>](../statements/declare-statement.md)  
  
 [<span data-ttu-id="5fa80-126">Delegate 语句</span><span class="sxs-lookup"><span data-stu-id="5fa80-126">Delegate Statement</span></span>](../statements/delegate-statement.md)  
  
 [<span data-ttu-id="5fa80-127">Dim 语句</span><span class="sxs-lookup"><span data-stu-id="5fa80-127">Dim Statement</span></span>](../statements/dim-statement.md)  
  
 [<span data-ttu-id="5fa80-128">Enum 语句</span><span class="sxs-lookup"><span data-stu-id="5fa80-128">Enum Statement</span></span>](../statements/enum-statement.md)  
  
 [<span data-ttu-id="5fa80-129">Event 语句</span><span class="sxs-lookup"><span data-stu-id="5fa80-129">Event Statement</span></span>](../statements/event-statement.md)  
  
 [<span data-ttu-id="5fa80-130">Function 语句</span><span class="sxs-lookup"><span data-stu-id="5fa80-130">Function Statement</span></span>](../statements/function-statement.md)  
  
 [<span data-ttu-id="5fa80-131">Interface 语句</span><span class="sxs-lookup"><span data-stu-id="5fa80-131">Interface Statement</span></span>](../statements/interface-statement.md)  
  
 [<span data-ttu-id="5fa80-132">Module 语句</span><span class="sxs-lookup"><span data-stu-id="5fa80-132">Module Statement</span></span>](../statements/module-statement.md)  
  
 [<span data-ttu-id="5fa80-133">Operator Statement</span><span class="sxs-lookup"><span data-stu-id="5fa80-133">Operator Statement</span></span>](../statements/operator-statement.md)  
  
 [<span data-ttu-id="5fa80-134">Property Statement</span><span class="sxs-lookup"><span data-stu-id="5fa80-134">Property Statement</span></span>](../statements/property-statement.md)  
  
 [<span data-ttu-id="5fa80-135">Structure 语句</span><span class="sxs-lookup"><span data-stu-id="5fa80-135">Structure Statement</span></span>](../statements/structure-statement.md)  
  
 [<span data-ttu-id="5fa80-136">Sub 语句</span><span class="sxs-lookup"><span data-stu-id="5fa80-136">Sub Statement</span></span>](../statements/sub-statement.md)  
  
## <a name="see-also"></a><span data-ttu-id="5fa80-137">请参阅</span><span class="sxs-lookup"><span data-stu-id="5fa80-137">See also</span></span>

- [<span data-ttu-id="5fa80-138">Protected</span><span class="sxs-lookup"><span data-stu-id="5fa80-138">Protected</span></span>](protected.md)
- [<span data-ttu-id="5fa80-139">Friend</span><span class="sxs-lookup"><span data-stu-id="5fa80-139">Friend</span></span>](friend.md)
- [<span data-ttu-id="5fa80-140">专用</span><span class="sxs-lookup"><span data-stu-id="5fa80-140">Private</span></span>](private.md)
- [<span data-ttu-id="5fa80-141">Private Protected</span><span class="sxs-lookup"><span data-stu-id="5fa80-141">Private Protected</span></span>](private-protected.md)
- [<span data-ttu-id="5fa80-142">Protected Friend</span><span class="sxs-lookup"><span data-stu-id="5fa80-142">Protected Friend</span></span>](protected-friend.md)
- [<span data-ttu-id="5fa80-143">Visual Basic 中的访问级别</span><span class="sxs-lookup"><span data-stu-id="5fa80-143">Access levels in Visual Basic</span></span>](../../programming-guide/language-features/declared-elements/access-levels.md)
- [<span data-ttu-id="5fa80-144">过程</span><span class="sxs-lookup"><span data-stu-id="5fa80-144">Procedures</span></span>](../../programming-guide/language-features/procedures/index.md)
- [<span data-ttu-id="5fa80-145">结构</span><span class="sxs-lookup"><span data-stu-id="5fa80-145">Structures</span></span>](../../programming-guide/language-features/data-types/structures.md)
- [<span data-ttu-id="5fa80-146">对象和类</span><span class="sxs-lookup"><span data-stu-id="5fa80-146">Objects and Classes</span></span>](../../programming-guide/language-features/objects-and-classes/index.md)
