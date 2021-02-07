---
description: '了解详细信息：重写 (Visual Basic) '
title: 替代
ms.date: 07/20/2015
f1_keywords:
- Overrides
- vb.Overrides
helpviewer_keywords:
- properties [Visual Basic], redefining
- procedures [Visual Basic], overriding
- procedures [Visual Basic], redefining
- overriding
- Overrides keyword [Visual Basic]
- overriding, Overrides keyword
- properties [Visual Basic], overriding
ms.assetid: 9f5e6144-ce10-465e-842b-1a8f8760af90
ms.openlocfilehash: d118bf4e366ff8f84806586dfc3977612ed6eff4
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99730442"
---
# <a name="overrides-visual-basic"></a><span data-ttu-id="b0e63-103">Overrides (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="b0e63-103">Overrides (Visual Basic)</span></span>

<span data-ttu-id="b0e63-104">指定某一属性或过程可重写从基类中继承的具有相同名称的属性或过程。</span><span class="sxs-lookup"><span data-stu-id="b0e63-104">Specifies that a property or procedure overrides an identically named property or procedure inherited from a base class.</span></span>

## <a name="rules"></a><span data-ttu-id="b0e63-105">规则</span><span class="sxs-lookup"><span data-stu-id="b0e63-105">Rules</span></span>

- <span data-ttu-id="b0e63-106">**声明上下文。**</span><span class="sxs-lookup"><span data-stu-id="b0e63-106">**Declaration Context.**</span></span> <span data-ttu-id="b0e63-107">`Overrides`只能在属性或过程声明语句中使用。</span><span class="sxs-lookup"><span data-stu-id="b0e63-107">You can use `Overrides` only in a property or procedure declaration statement.</span></span>

- <span data-ttu-id="b0e63-108">**组合修饰符。**</span><span class="sxs-lookup"><span data-stu-id="b0e63-108">**Combined Modifiers.**</span></span> <span data-ttu-id="b0e63-109">不能在 `Overrides` `Shadows` 同一声明中同时指定和或 `Shared` 。</span><span class="sxs-lookup"><span data-stu-id="b0e63-109">You cannot specify `Overrides` together with `Shadows` or `Shared` in the same declaration.</span></span> <span data-ttu-id="b0e63-110">由于重写元素是隐式可重写的，因此不能将 `Overridable` 与 `Overrides` 组合到一起。</span><span class="sxs-lookup"><span data-stu-id="b0e63-110">Because an overriding element is implicitly overridable, you cannot combine `Overridable` with `Overrides`.</span></span>

- <span data-ttu-id="b0e63-111">**匹配签名。**</span><span class="sxs-lookup"><span data-stu-id="b0e63-111">**Matching Signatures.**</span></span> <span data-ttu-id="b0e63-112">此声明的签名必须与它所重写的属性或过程的 *签名* 完全匹配。</span><span class="sxs-lookup"><span data-stu-id="b0e63-112">The signature of this declaration must exactly match the *signature* of the property or procedure that it overrides.</span></span> <span data-ttu-id="b0e63-113">这意味着参数列表必须具有相同数量的参数，并且排序顺序和数据类型都必须完全相同。</span><span class="sxs-lookup"><span data-stu-id="b0e63-113">This means the parameter lists must have the same number of parameters, in the same order, with the same data types.</span></span>

  <span data-ttu-id="b0e63-114">除签名外，重写的声明还必须完全匹配以下项：</span><span class="sxs-lookup"><span data-stu-id="b0e63-114">In addition to the signature, the overriding declaration must also exactly match the following:</span></span>

  - <span data-ttu-id="b0e63-115">访问级别</span><span class="sxs-lookup"><span data-stu-id="b0e63-115">The access level</span></span>

  - <span data-ttu-id="b0e63-116">返回类型（如有）</span><span class="sxs-lookup"><span data-stu-id="b0e63-116">The return type, if any</span></span>

- <span data-ttu-id="b0e63-117">**泛型签名。**</span><span class="sxs-lookup"><span data-stu-id="b0e63-117">**Generic Signatures.**</span></span> <span data-ttu-id="b0e63-118">对于泛型过程，签名包括类型参数的数量。</span><span class="sxs-lookup"><span data-stu-id="b0e63-118">For a generic procedure, the signature includes the number of type parameters.</span></span> <span data-ttu-id="b0e63-119">因此，重写的声明必须在这方面与基类版本匹配。</span><span class="sxs-lookup"><span data-stu-id="b0e63-119">Therefore, the overriding declaration must match the base class version in that respect as well.</span></span>

- <span data-ttu-id="b0e63-120">**附加匹配。**</span><span class="sxs-lookup"><span data-stu-id="b0e63-120">**Additional Matching.**</span></span> <span data-ttu-id="b0e63-121">除匹配基类版本的签名外，此声明还必须在以下方面与其匹配：</span><span class="sxs-lookup"><span data-stu-id="b0e63-121">In addition to matching the signature of the base class version, this declaration must also match it in the following respects:</span></span>

  - <span data-ttu-id="b0e63-122">访问级别修饰符 (如 [公用](public.md)) </span><span class="sxs-lookup"><span data-stu-id="b0e63-122">Access-level modifier (such as [Public](public.md))</span></span>

  - <span data-ttu-id="b0e63-123">将每个参数的机制传递 ([ByVal](byval.md) 或 [ByRef](byref.md)) </span><span class="sxs-lookup"><span data-stu-id="b0e63-123">Passing mechanism of each parameter ([ByVal](byval.md) or [ByRef](byref.md))</span></span>

  - <span data-ttu-id="b0e63-124">泛型过程的每个类型参数的约束列表</span><span class="sxs-lookup"><span data-stu-id="b0e63-124">Constraint lists on each type parameter of a generic procedure</span></span>

- <span data-ttu-id="b0e63-125">**隐藏和重写操作。**</span><span class="sxs-lookup"><span data-stu-id="b0e63-125">**Shadowing and Overriding.**</span></span> <span data-ttu-id="b0e63-126">隐藏和重写操作都可重新定义继承的元素，但这两种方法之间又具有很大的差异。</span><span class="sxs-lookup"><span data-stu-id="b0e63-126">Both shadowing and overriding redefine an inherited element, but there are significant differences between the two approaches.</span></span> <span data-ttu-id="b0e63-127">有关详细信息，请参阅 [Visual Basic 中的隐藏](../../programming-guide/language-features/declared-elements/shadowing.md)。</span><span class="sxs-lookup"><span data-stu-id="b0e63-127">For more information, see [Shadowing in Visual Basic](../../programming-guide/language-features/declared-elements/shadowing.md).</span></span>

<span data-ttu-id="b0e63-128">如果使用 `Overrides`，编译器将隐式添加 `Overloads`，以便库 API 更轻松地使用 C#。</span><span class="sxs-lookup"><span data-stu-id="b0e63-128">If you use `Overrides`, the compiler implicitly adds `Overloads` so that your library APIs work with C# more easily.</span></span>

<span data-ttu-id="b0e63-129">`Overrides` 修饰符可用于下面的上下文中：</span><span class="sxs-lookup"><span data-stu-id="b0e63-129">The `Overrides` modifier can be used in these contexts:</span></span>

- [<span data-ttu-id="b0e63-130">Function 语句</span><span class="sxs-lookup"><span data-stu-id="b0e63-130">Function Statement</span></span>](../statements/function-statement.md)

- [<span data-ttu-id="b0e63-131">Property Statement</span><span class="sxs-lookup"><span data-stu-id="b0e63-131">Property Statement</span></span>](../statements/property-statement.md)

- [<span data-ttu-id="b0e63-132">Sub 语句</span><span class="sxs-lookup"><span data-stu-id="b0e63-132">Sub Statement</span></span>](../statements/sub-statement.md)

## <a name="see-also"></a><span data-ttu-id="b0e63-133">请参阅</span><span class="sxs-lookup"><span data-stu-id="b0e63-133">See also</span></span>

- [<span data-ttu-id="b0e63-134">New</span><span class="sxs-lookup"><span data-stu-id="b0e63-134">MustOverride</span></span>](mustoverride.md)
- [<span data-ttu-id="b0e63-135">NotOverridable</span><span class="sxs-lookup"><span data-stu-id="b0e63-135">NotOverridable</span></span>](notoverridable.md)
- [<span data-ttu-id="b0e63-136">Overrides</span><span class="sxs-lookup"><span data-stu-id="b0e63-136">Overridable</span></span>](overridable.md)
- [<span data-ttu-id="b0e63-137">关键字</span><span class="sxs-lookup"><span data-stu-id="b0e63-137">Keywords</span></span>](../keywords/index.md)
- [<span data-ttu-id="b0e63-138">Visual Basic 中的隐藏</span><span class="sxs-lookup"><span data-stu-id="b0e63-138">Shadowing in Visual Basic</span></span>](../../programming-guide/language-features/declared-elements/shadowing.md)
- [<span data-ttu-id="b0e63-139">Generic Types in Visual Basic</span><span class="sxs-lookup"><span data-stu-id="b0e63-139">Generic Types in Visual Basic</span></span>](../../programming-guide/language-features/data-types/generic-types.md)
- [<span data-ttu-id="b0e63-140">Type List</span><span class="sxs-lookup"><span data-stu-id="b0e63-140">Type List</span></span>](../statements/type-list.md)
