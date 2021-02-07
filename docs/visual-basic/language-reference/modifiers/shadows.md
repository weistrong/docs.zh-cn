---
description: '了解详细信息：阴影 (Visual Basic) '
title: Shadows
ms.date: 07/20/2015
f1_keywords:
- vb.Shadows
- shadows
helpviewer_keywords:
- shadowing
- duplicate names [Visual Basic]
- scope [Visual Basic], shadowing
- Shadows keyword [Visual Basic]
- names [Visual Basic], shadowing
ms.assetid: 6bf687cd-0544-4797-b51b-911125ec57c6
ms.openlocfilehash: 4a455a78c36e15db977936b81c22e7a5b03d107e
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99700840"
---
# <a name="shadows-visual-basic"></a><span data-ttu-id="5714c-103">Shadows (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="5714c-103">Shadows (Visual Basic)</span></span>

<span data-ttu-id="5714c-104">指定已声明的编程元素重新声明并隐藏基类中具有相同名称的元素或重载元素集。</span><span class="sxs-lookup"><span data-stu-id="5714c-104">Specifies that a declared programming element redeclares and hides an identically named element, or set of overloaded elements, in a base class.</span></span>

## <a name="remarks"></a><span data-ttu-id="5714c-105">备注</span><span class="sxs-lookup"><span data-stu-id="5714c-105">Remarks</span></span>

<span data-ttu-id="5714c-106">隐藏 (（也称为 *按) 名称隐藏* ）的主要目的是保留类成员的定义。</span><span class="sxs-lookup"><span data-stu-id="5714c-106">The main purpose of shadowing (which is also known as *hiding by name*) is to preserve the definition of your class members.</span></span> <span data-ttu-id="5714c-107">基类可能会发生更改，该更改将创建一个与已定义的元素同名的元素。</span><span class="sxs-lookup"><span data-stu-id="5714c-107">The base class might undergo a change that creates an element with the same name as one you have already defined.</span></span> <span data-ttu-id="5714c-108">如果发生这种情况， `Shadows` 修饰符会强制通过类的引用解析为你定义的成员而不是新的基类元素。</span><span class="sxs-lookup"><span data-stu-id="5714c-108">If this happens, the `Shadows` modifier forces references through your class to be resolved to the member you defined, instead of to the new base class element.</span></span>

<span data-ttu-id="5714c-109">隐藏和重写操作都可重新定义继承的元素，但这两种方法之间又具有很大的差异。</span><span class="sxs-lookup"><span data-stu-id="5714c-109">Both shadowing and overriding redefine an inherited element, but there are significant differences between the two approaches.</span></span> <span data-ttu-id="5714c-110">有关详细信息，请参阅 [Visual Basic 中的隐藏](../../programming-guide/language-features/declared-elements/shadowing.md)。</span><span class="sxs-lookup"><span data-stu-id="5714c-110">For more information, see [Shadowing in Visual Basic](../../programming-guide/language-features/declared-elements/shadowing.md).</span></span>

## <a name="rules"></a><span data-ttu-id="5714c-111">规则</span><span class="sxs-lookup"><span data-stu-id="5714c-111">Rules</span></span>

- <span data-ttu-id="5714c-112">**声明上下文。**</span><span class="sxs-lookup"><span data-stu-id="5714c-112">**Declaration Context.**</span></span> <span data-ttu-id="5714c-113">只能 `Shadows` 在类级别使用。</span><span class="sxs-lookup"><span data-stu-id="5714c-113">You can use `Shadows` only at class level.</span></span> <span data-ttu-id="5714c-114">这意味着元素的声明上下文 `Shadows` 必须是类，且不能是源文件、命名空间、接口、模块、结构或过程。</span><span class="sxs-lookup"><span data-stu-id="5714c-114">This means the declaration context for a `Shadows` element must be a class, and cannot be a source file, namespace, interface, module, structure, or procedure.</span></span>

  <span data-ttu-id="5714c-115">只能在单个声明语句中声明一个隐藏元素。</span><span class="sxs-lookup"><span data-stu-id="5714c-115">You can declare only one shadowing element in a single declaration statement.</span></span>

- <span data-ttu-id="5714c-116">**组合修饰符。**</span><span class="sxs-lookup"><span data-stu-id="5714c-116">**Combined Modifiers.**</span></span> <span data-ttu-id="5714c-117">不能 `Shadows` `Overloads` `Overrides` `Static` 在同一声明中同时指定、或。</span><span class="sxs-lookup"><span data-stu-id="5714c-117">You cannot specify `Shadows` together with `Overloads`, `Overrides`, or `Static` in the same declaration.</span></span>

- <span data-ttu-id="5714c-118">**元素类型。**</span><span class="sxs-lookup"><span data-stu-id="5714c-118">**Element Types.**</span></span> <span data-ttu-id="5714c-119">可以与任何其他类型一起隐藏任何类型的已声明元素。</span><span class="sxs-lookup"><span data-stu-id="5714c-119">You can shadow any kind of declared element with any other kind.</span></span> <span data-ttu-id="5714c-120">如果使用另一个属性或过程来隐藏属性或过程，则参数和返回类型不必与基类属性或过程中的相同。</span><span class="sxs-lookup"><span data-stu-id="5714c-120">If you shadow a property or procedure with another property or procedure, the parameters and the return type do not have to match those in the base class property or procedure.</span></span>

- <span data-ttu-id="5714c-121">**访问.**</span><span class="sxs-lookup"><span data-stu-id="5714c-121">**Accessing.**</span></span> <span data-ttu-id="5714c-122">通常，基类中隐藏的元素在隐藏它的派生类中不可用。</span><span class="sxs-lookup"><span data-stu-id="5714c-122">The shadowed element in the base class is normally unavailable from within the derived class that shadows it.</span></span> <span data-ttu-id="5714c-123">不过，请注意以下事项。</span><span class="sxs-lookup"><span data-stu-id="5714c-123">However, the following considerations apply.</span></span>

  - <span data-ttu-id="5714c-124">如果不能从引用它的代码访问隐藏元素，则会将引用解析为隐藏的元素。</span><span class="sxs-lookup"><span data-stu-id="5714c-124">If the shadowing element is not accessible from the code referring to it, the reference is resolved to the shadowed element.</span></span> <span data-ttu-id="5714c-125">例如，如果某个 `Private` 元素隐藏了一个基类元素，则没有访问该元素的权限的代码将 `Private` 改为访问该基类元素。</span><span class="sxs-lookup"><span data-stu-id="5714c-125">For example, if a `Private` element shadows a base class element, code that does not have permission to access the `Private` element accesses the base class element instead.</span></span>

  - <span data-ttu-id="5714c-126">如果隐藏元素，仍然可以通过使用基类的类型声明的对象访问隐藏的元素。</span><span class="sxs-lookup"><span data-stu-id="5714c-126">If you shadow an element, you can still access the shadowed element through an object declared with the type of the base class.</span></span> <span data-ttu-id="5714c-127">你还可以通过来访问它 `MyBase` 。</span><span class="sxs-lookup"><span data-stu-id="5714c-127">You can also access it through `MyBase`.</span></span>

<span data-ttu-id="5714c-128">`Shadows` 修饰符可用于下面的上下文中：</span><span class="sxs-lookup"><span data-stu-id="5714c-128">The `Shadows` modifier can be used in these contexts:</span></span>

- [<span data-ttu-id="5714c-129">Class 语句</span><span class="sxs-lookup"><span data-stu-id="5714c-129">Class Statement</span></span>](../statements/class-statement.md)

- [<span data-ttu-id="5714c-130">Const 语句</span><span class="sxs-lookup"><span data-stu-id="5714c-130">Const Statement</span></span>](../statements/const-statement.md)

- [<span data-ttu-id="5714c-131">Declare Statement</span><span class="sxs-lookup"><span data-stu-id="5714c-131">Declare Statement</span></span>](../statements/declare-statement.md)

- [<span data-ttu-id="5714c-132">Delegate 语句</span><span class="sxs-lookup"><span data-stu-id="5714c-132">Delegate Statement</span></span>](../statements/delegate-statement.md)

- [<span data-ttu-id="5714c-133">Dim 语句</span><span class="sxs-lookup"><span data-stu-id="5714c-133">Dim Statement</span></span>](../statements/dim-statement.md)

- [<span data-ttu-id="5714c-134">Enum 语句</span><span class="sxs-lookup"><span data-stu-id="5714c-134">Enum Statement</span></span>](../statements/enum-statement.md)

- [<span data-ttu-id="5714c-135">Event 语句</span><span class="sxs-lookup"><span data-stu-id="5714c-135">Event Statement</span></span>](../statements/event-statement.md)

- [<span data-ttu-id="5714c-136">Function 语句</span><span class="sxs-lookup"><span data-stu-id="5714c-136">Function Statement</span></span>](../statements/function-statement.md)

- [<span data-ttu-id="5714c-137">Interface 语句</span><span class="sxs-lookup"><span data-stu-id="5714c-137">Interface Statement</span></span>](../statements/interface-statement.md)

- [<span data-ttu-id="5714c-138">Property Statement</span><span class="sxs-lookup"><span data-stu-id="5714c-138">Property Statement</span></span>](../statements/property-statement.md)

- [<span data-ttu-id="5714c-139">Structure 语句</span><span class="sxs-lookup"><span data-stu-id="5714c-139">Structure Statement</span></span>](../statements/structure-statement.md)

- [<span data-ttu-id="5714c-140">Sub 语句</span><span class="sxs-lookup"><span data-stu-id="5714c-140">Sub Statement</span></span>](../statements/sub-statement.md)

## <a name="see-also"></a><span data-ttu-id="5714c-141">请参阅</span><span class="sxs-lookup"><span data-stu-id="5714c-141">See also</span></span>

- [<span data-ttu-id="5714c-142">共享</span><span class="sxs-lookup"><span data-stu-id="5714c-142">Shared</span></span>](shared.md)
- [<span data-ttu-id="5714c-143">静态</span><span class="sxs-lookup"><span data-stu-id="5714c-143">Static</span></span>](static.md)
- [<span data-ttu-id="5714c-144">专用</span><span class="sxs-lookup"><span data-stu-id="5714c-144">Private</span></span>](private.md)
- [<span data-ttu-id="5714c-145">Me、My、MyBase 和 MyClass</span><span class="sxs-lookup"><span data-stu-id="5714c-145">Me, My, MyBase, and MyClass</span></span>](../../programming-guide/program-structure/me-my-mybase-and-myclass.md)
- [<span data-ttu-id="5714c-146">继承基础知识</span><span class="sxs-lookup"><span data-stu-id="5714c-146">Inheritance Basics</span></span>](../../programming-guide/language-features/objects-and-classes/inheritance-basics.md)
- [<span data-ttu-id="5714c-147">New</span><span class="sxs-lookup"><span data-stu-id="5714c-147">MustOverride</span></span>](mustoverride.md)
- [<span data-ttu-id="5714c-148">NotOverridable</span><span class="sxs-lookup"><span data-stu-id="5714c-148">NotOverridable</span></span>](notoverridable.md)
- [<span data-ttu-id="5714c-149">重载</span><span class="sxs-lookup"><span data-stu-id="5714c-149">Overloads</span></span>](overloads.md)
- [<span data-ttu-id="5714c-150">Overrides</span><span class="sxs-lookup"><span data-stu-id="5714c-150">Overridable</span></span>](overridable.md)
- [<span data-ttu-id="5714c-151">替代</span><span class="sxs-lookup"><span data-stu-id="5714c-151">Overrides</span></span>](overrides.md)
- [<span data-ttu-id="5714c-152">Visual Basic 中的隐藏</span><span class="sxs-lookup"><span data-stu-id="5714c-152">Shadowing in Visual Basic</span></span>](../../programming-guide/language-features/declared-elements/shadowing.md)
