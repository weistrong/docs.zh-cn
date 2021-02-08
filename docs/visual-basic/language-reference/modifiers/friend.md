---
description: '了解有关以下内容的详细信息： Friend (Visual Basic) '
title: Friend
ms.date: 07/20/2015
f1_keywords:
- vb.Friend
helpviewer_keywords:
- Friend keyword [Visual Basic]
- Friend access modifier
- Friend keyword [Visual Basic], syntax
- Protected Friend keyword combination
- Friend keyword [Visual Basic], and Protected
ms.assetid: b664605e-1c79-4728-b996-aa59c50846bc
ms.openlocfilehash: ef2444555c05d6a4b24048316e282d269d4b7f1b
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99774585"
---
# <a name="friend-visual-basic"></a><span data-ttu-id="a12a5-103">Friend (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="a12a5-103">Friend (Visual Basic)</span></span>

<span data-ttu-id="a12a5-104">指定只能从包含其声明的程序集内部访问一个或多个已声明的编程元素。</span><span class="sxs-lookup"><span data-stu-id="a12a5-104">Specifies that one or more declared programming elements are accessible only from within the assembly that contains their declaration.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="a12a5-105">备注</span><span class="sxs-lookup"><span data-stu-id="a12a5-105">Remarks</span></span>  

 <span data-ttu-id="a12a5-106">在许多情况下，需要由整个程序集使用的编程元素（如类和结构），而不是由声明它们的组件使用。</span><span class="sxs-lookup"><span data-stu-id="a12a5-106">In many cases, you want programming elements such as classes and structures to be used by the entire assembly, not only by the component that declares them.</span></span> <span data-ttu-id="a12a5-107">不过，如果应用程序是专有) ，则可能不希望程序集外部的代码可以访问它们 (例如，。</span><span class="sxs-lookup"><span data-stu-id="a12a5-107">However, you might not want them to be accessible by code outside the assembly (for example, if the application is proprietary).</span></span> <span data-ttu-id="a12a5-108">如果要以这种方式限制对某个元素的访问，则可以使用修饰符来声明它 `Friend` 。</span><span class="sxs-lookup"><span data-stu-id="a12a5-108">If you want to limit access to an element in this way, you can declare it by using the `Friend` modifier.</span></span>  
  
 <span data-ttu-id="a12a5-109">编译为同一程序集的其他类、结构和模块中的代码可以访问 `Friend` 该程序集中的所有元素。</span><span class="sxs-lookup"><span data-stu-id="a12a5-109">Code in other classes, structures, and modules that are compiled to the same assembly can access all the `Friend` elements in that assembly.</span></span>  
  
 <span data-ttu-id="a12a5-110">`Friend` 访问通常是应用程序编程元素的首选级别， `Friend` 是接口、模块、类或结构的默认访问级别。</span><span class="sxs-lookup"><span data-stu-id="a12a5-110">`Friend` access is often the preferred level for an application's programming elements, and `Friend` is the default access level of an interface, a module, a class, or a structure.</span></span>  
  
 <span data-ttu-id="a12a5-111">`Friend`只能在模块、接口或命名空间级别使用。</span><span class="sxs-lookup"><span data-stu-id="a12a5-111">You can use `Friend` only at the module, interface, or namespace level.</span></span> <span data-ttu-id="a12a5-112">因此，元素的声明上下文 `Friend` 必须是源文件、命名空间、接口、模块、类或结构; 它不能是过程。</span><span class="sxs-lookup"><span data-stu-id="a12a5-112">Therefore, the declaration context for a `Friend` element must be a source file, a namespace, an interface, a module, a class, or a structure; it can't be a procedure.</span></span>  

> [!NOTE]
> <span data-ttu-id="a12a5-113">你还可以使用 [受保护的 Friend](protected-friend.md) 访问修饰符，使类成员可从该类、派生类和类定义的同一程序集中访问。</span><span class="sxs-lookup"><span data-stu-id="a12a5-113">You can also use the [Protected Friend](protected-friend.md) access modifier, which makes a class member accessible from within that class, from derived classes, and from the same assembly in which the class is defined.</span></span> <span data-ttu-id="a12a5-114">若要从同一程序集中的类和派生类中限制对成员的访问，请使用 [私有受保护](private-protected.md) 的访问修饰符。</span><span class="sxs-lookup"><span data-stu-id="a12a5-114">To restrict access to a member from within its class and from derived classes in the same assembly, you use the [Private Protected](private-protected.md) access modifier.</span></span>

 <span data-ttu-id="a12a5-115">有关 `Friend` 和其他访问修饰符的比较，请参阅 [Visual Basic 中的访问级别](../../programming-guide/language-features/declared-elements/access-levels.md)。</span><span class="sxs-lookup"><span data-stu-id="a12a5-115">For a comparison of `Friend` and the other access modifiers, see [Access levels in Visual Basic](../../programming-guide/language-features/declared-elements/access-levels.md).</span></span>  
  
> [!NOTE]
> <span data-ttu-id="a12a5-116">可以指定另一个程序集是友元程序集，该程序集允许其访问标记为的所有类型和成员 `Friend` 。</span><span class="sxs-lookup"><span data-stu-id="a12a5-116">You can specify that another assembly is a friend assembly, which allows it to access all types and members that are marked as `Friend`.</span></span> <span data-ttu-id="a12a5-117">有关详细信息，请参阅[友元程序集](../../../standard/assembly/friend.md)。</span><span class="sxs-lookup"><span data-stu-id="a12a5-117">For more information, see [Friend Assemblies](../../../standard/assembly/friend.md).</span></span>

## <a name="example"></a><span data-ttu-id="a12a5-118">示例</span><span class="sxs-lookup"><span data-stu-id="a12a5-118">Example</span></span>  

 <span data-ttu-id="a12a5-119">下面的类使用 `Friend` 修饰符允许同一程序集中的其他编程元素访问某些成员。</span><span class="sxs-lookup"><span data-stu-id="a12a5-119">The following class uses the `Friend` modifier to allow other programming elements within the same assembly to access certain members.</span></span>  
  
 [!code-vb[VbVbalrAccessModifiers#1](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/vbvbalraccessmodifiers/vb/class1.vb#1)]  
  
## <a name="usage"></a><span data-ttu-id="a12a5-120">使用情况</span><span class="sxs-lookup"><span data-stu-id="a12a5-120">Usage</span></span>  

 <span data-ttu-id="a12a5-121">可以 `Friend` 在以下上下文中使用修饰符：</span><span class="sxs-lookup"><span data-stu-id="a12a5-121">You can use the `Friend` modifier in these contexts:</span></span>  
  
 [<span data-ttu-id="a12a5-122">Class 语句</span><span class="sxs-lookup"><span data-stu-id="a12a5-122">Class Statement</span></span>](../statements/class-statement.md)  
  
 [<span data-ttu-id="a12a5-123">Const 语句</span><span class="sxs-lookup"><span data-stu-id="a12a5-123">Const Statement</span></span>](../statements/const-statement.md)  
  
 [<span data-ttu-id="a12a5-124">Declare Statement</span><span class="sxs-lookup"><span data-stu-id="a12a5-124">Declare Statement</span></span>](../statements/declare-statement.md)  
  
 [<span data-ttu-id="a12a5-125">Delegate 语句</span><span class="sxs-lookup"><span data-stu-id="a12a5-125">Delegate Statement</span></span>](../statements/delegate-statement.md)  
  
 [<span data-ttu-id="a12a5-126">Dim 语句</span><span class="sxs-lookup"><span data-stu-id="a12a5-126">Dim Statement</span></span>](../statements/dim-statement.md)  
  
 [<span data-ttu-id="a12a5-127">Enum 语句</span><span class="sxs-lookup"><span data-stu-id="a12a5-127">Enum Statement</span></span>](../statements/enum-statement.md)  
  
 [<span data-ttu-id="a12a5-128">Event 语句</span><span class="sxs-lookup"><span data-stu-id="a12a5-128">Event Statement</span></span>](../statements/event-statement.md)  
  
 [<span data-ttu-id="a12a5-129">Function 语句</span><span class="sxs-lookup"><span data-stu-id="a12a5-129">Function Statement</span></span>](../statements/function-statement.md)  
  
 [<span data-ttu-id="a12a5-130">Interface 语句</span><span class="sxs-lookup"><span data-stu-id="a12a5-130">Interface Statement</span></span>](../statements/interface-statement.md)  
  
 [<span data-ttu-id="a12a5-131">Module 语句</span><span class="sxs-lookup"><span data-stu-id="a12a5-131">Module Statement</span></span>](../statements/module-statement.md)  
  
 [<span data-ttu-id="a12a5-132">Property Statement</span><span class="sxs-lookup"><span data-stu-id="a12a5-132">Property Statement</span></span>](../statements/property-statement.md)  
  
 [<span data-ttu-id="a12a5-133">Structure 语句</span><span class="sxs-lookup"><span data-stu-id="a12a5-133">Structure Statement</span></span>](../statements/structure-statement.md)  
  
 [<span data-ttu-id="a12a5-134">Sub 语句</span><span class="sxs-lookup"><span data-stu-id="a12a5-134">Sub Statement</span></span>](../statements/sub-statement.md)  
  
## <a name="see-also"></a><span data-ttu-id="a12a5-135">请参阅</span><span class="sxs-lookup"><span data-stu-id="a12a5-135">See also</span></span>

- <xref:System.Runtime.CompilerServices.InternalsVisibleToAttribute>
- [<span data-ttu-id="a12a5-136">公共</span><span class="sxs-lookup"><span data-stu-id="a12a5-136">Public</span></span>](public.md)
- [<span data-ttu-id="a12a5-137">Protected</span><span class="sxs-lookup"><span data-stu-id="a12a5-137">Protected</span></span>](protected.md)
- [<span data-ttu-id="a12a5-138">专用</span><span class="sxs-lookup"><span data-stu-id="a12a5-138">Private</span></span>](private.md)
- [<span data-ttu-id="a12a5-139">Private Protected</span><span class="sxs-lookup"><span data-stu-id="a12a5-139">Private Protected</span></span>](./private-protected.md)
- [<span data-ttu-id="a12a5-140">Protected Friend</span><span class="sxs-lookup"><span data-stu-id="a12a5-140">Protected Friend</span></span>](./protected-friend.md)
- [<span data-ttu-id="a12a5-141">Visual Basic 中的访问级别</span><span class="sxs-lookup"><span data-stu-id="a12a5-141">Access levels in Visual Basic</span></span>](../../programming-guide/language-features/declared-elements/access-levels.md)
- [<span data-ttu-id="a12a5-142">过程</span><span class="sxs-lookup"><span data-stu-id="a12a5-142">Procedures</span></span>](../../programming-guide/language-features/procedures/index.md)
- [<span data-ttu-id="a12a5-143">结构</span><span class="sxs-lookup"><span data-stu-id="a12a5-143">Structures</span></span>](../../programming-guide/language-features/data-types/structures.md)
- [<span data-ttu-id="a12a5-144">对象和类</span><span class="sxs-lookup"><span data-stu-id="a12a5-144">Objects and Classes</span></span>](../../programming-guide/language-features/objects-and-classes/index.md)
