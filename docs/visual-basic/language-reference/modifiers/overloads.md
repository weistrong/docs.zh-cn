---
description: '了解详细信息： (Visual Basic 重载) '
title: 重载
ms.date: 07/20/2015
f1_keywords:
- vb.Overloads
- Overloads
helpviewer_keywords:
- Overloads keyword [Visual Basic]
- hiding by signature
- Shadows keyword [Visual Basic]
- signature, hiding by
ms.assetid: 0c6820b8-25b2-4664-bc59-5ca93c99c042
ms.openlocfilehash: 7f0b440b537500595e465d8aabc7724671f3ae95
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99730507"
---
# <a name="overloads-visual-basic"></a><span data-ttu-id="e052b-103">Overloads (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="e052b-103">Overloads (Visual Basic)</span></span>

<span data-ttu-id="e052b-104">指定某一属性或过程重新声明一个或多个具有相同名称的现有属性或过程。</span><span class="sxs-lookup"><span data-stu-id="e052b-104">Specifies that a property or procedure redeclares one or more existing properties or procedures with the same name.</span></span>

## <a name="remarks"></a><span data-ttu-id="e052b-105">备注</span><span class="sxs-lookup"><span data-stu-id="e052b-105">Remarks</span></span>

<span data-ttu-id="e052b-106">*重载* 是为同一范围内的给定属性或过程名称提供多个定义的做法。</span><span class="sxs-lookup"><span data-stu-id="e052b-106">*Overloading* is the practice of supplying more than one definition for a given property or procedure name in the same scope.</span></span> <span data-ttu-id="e052b-107">重新声明具有不同签名的属性或过程有时称为 " *按签名隐藏*"。</span><span class="sxs-lookup"><span data-stu-id="e052b-107">Redeclaring a property or procedure with a different signature is sometimes called *hiding by signature*.</span></span>

## <a name="rules"></a><span data-ttu-id="e052b-108">规则</span><span class="sxs-lookup"><span data-stu-id="e052b-108">Rules</span></span>

- <span data-ttu-id="e052b-109">**声明上下文。**</span><span class="sxs-lookup"><span data-stu-id="e052b-109">**Declaration Context.**</span></span> <span data-ttu-id="e052b-110">`Overloads`只能在属性或过程声明语句中使用。</span><span class="sxs-lookup"><span data-stu-id="e052b-110">You can use `Overloads` only in a property or procedure declaration statement.</span></span>

- <span data-ttu-id="e052b-111">**组合修饰符。**</span><span class="sxs-lookup"><span data-stu-id="e052b-111">**Combined Modifiers.**</span></span> <span data-ttu-id="e052b-112">不能 `Overloads` 在同一过程声明中同时指定和 [阴影](shadows.md) 。</span><span class="sxs-lookup"><span data-stu-id="e052b-112">You cannot specify `Overloads` together with [Shadows](shadows.md) in the same procedure declaration.</span></span>

- <span data-ttu-id="e052b-113">**必需的差异。**</span><span class="sxs-lookup"><span data-stu-id="e052b-113">**Required Differences.**</span></span> <span data-ttu-id="e052b-114">此声明中的 *签名* 必须与它重载的每个属性或过程的签名不同。</span><span class="sxs-lookup"><span data-stu-id="e052b-114">The *signature* in this declaration must be different from the signature of every property or procedure that it overloads.</span></span> <span data-ttu-id="e052b-115">签名包含属性或过程名以及以下内容：</span><span class="sxs-lookup"><span data-stu-id="e052b-115">The signature comprises the property or procedure name together with the following:</span></span>

  - <span data-ttu-id="e052b-116">参数的数量</span><span class="sxs-lookup"><span data-stu-id="e052b-116">the number of parameters</span></span>

  - <span data-ttu-id="e052b-117">参数顺序</span><span class="sxs-lookup"><span data-stu-id="e052b-117">the order of the parameters</span></span>

  - <span data-ttu-id="e052b-118">参数的数据类型</span><span class="sxs-lookup"><span data-stu-id="e052b-118">the data types of the parameters</span></span>

  - <span data-ttu-id="e052b-119">类型参数的数量（针对泛型过程）</span><span class="sxs-lookup"><span data-stu-id="e052b-119">the number of type parameters (for a generic procedure)</span></span>

  - <span data-ttu-id="e052b-120">返回类型（仅针对转换运算符过程）</span><span class="sxs-lookup"><span data-stu-id="e052b-120">the return type (only for a conversion operator procedure)</span></span>

  <span data-ttu-id="e052b-121">所有重载都必须有相同的名称，但每个重载必须在上面的一个或多个方面与所有其他重载不同。</span><span class="sxs-lookup"><span data-stu-id="e052b-121">All overloads must have the same name, but each must differ from all the others in one or more of the preceding respects.</span></span> <span data-ttu-id="e052b-122">这使编译器在代码调用属性或过程时可以区分要使用哪个版本。</span><span class="sxs-lookup"><span data-stu-id="e052b-122">This allows the compiler to distinguish which version to use when code calls the property or procedure.</span></span>

- <span data-ttu-id="e052b-123">**不允许的差异。**</span><span class="sxs-lookup"><span data-stu-id="e052b-123">**Disallowed Differences.**</span></span> <span data-ttu-id="e052b-124">对于重载属性或过程而言，更改下面的一项或多项无效，因为它们不是签名的一部分：</span><span class="sxs-lookup"><span data-stu-id="e052b-124">Changing one or more of the following is not valid for overloading a property or procedure, because they are not part of the signature:</span></span>

  - <span data-ttu-id="e052b-125">它是否返回值（针对过程）</span><span class="sxs-lookup"><span data-stu-id="e052b-125">whether or not it returns a value (for a procedure)</span></span>

  - <span data-ttu-id="e052b-126">返回值的数据类型（除转换运算符之外）</span><span class="sxs-lookup"><span data-stu-id="e052b-126">the data type of the return value (except for a conversion operator)</span></span>

  - <span data-ttu-id="e052b-127">参数或类型参数的名称</span><span class="sxs-lookup"><span data-stu-id="e052b-127">the names of the parameters or type parameters</span></span>

  - <span data-ttu-id="e052b-128">对类型参数的约束（针对泛型过程）</span><span class="sxs-lookup"><span data-stu-id="e052b-128">the constraints on the type parameters (for a generic procedure)</span></span>

  - <span data-ttu-id="e052b-129">参数修饰符关键字（如 `ByRef` 或 `Optional`）</span><span class="sxs-lookup"><span data-stu-id="e052b-129">parameter modifier keywords (such as `ByRef` or `Optional`)</span></span>

  - <span data-ttu-id="e052b-130">属性或过程修饰符关键字（如 `Public` 或 `Shared`）</span><span class="sxs-lookup"><span data-stu-id="e052b-130">property or procedure modifier keywords (such as `Public` or `Shared`)</span></span>

- <span data-ttu-id="e052b-131">**可选修饰符。**</span><span class="sxs-lookup"><span data-stu-id="e052b-131">**Optional Modifier.**</span></span> <span data-ttu-id="e052b-132">在 `Overloads` 同一个类中定义多个重载属性或过程时，无需使用修饰符。</span><span class="sxs-lookup"><span data-stu-id="e052b-132">You do not have to use the `Overloads` modifier when you are defining multiple overloaded properties or procedures in the same class.</span></span> <span data-ttu-id="e052b-133">然而，如果在某个声明中使用 `Overloads`，则必须在所有的声明中使用它。</span><span class="sxs-lookup"><span data-stu-id="e052b-133">However, if you use `Overloads` in one of the declarations, you must use it in all of them.</span></span>

- <span data-ttu-id="e052b-134">**隐藏和重载。**</span><span class="sxs-lookup"><span data-stu-id="e052b-134">**Shadowing and Overloading.**</span></span> <span data-ttu-id="e052b-135">`Overloads` 还可用于在基类中隐藏现有成员或重载成员集。</span><span class="sxs-lookup"><span data-stu-id="e052b-135">`Overloads` can also be used to shadow an existing member, or set of overloaded members, in a base class.</span></span> <span data-ttu-id="e052b-136">以这种方式使用 `Overloads` 时，应使用与基类成员相同的名称和参数列表来声明属性或方法，并且不提供 `Shadows` 关键字。</span><span class="sxs-lookup"><span data-stu-id="e052b-136">When you use `Overloads` in this way, you declare the property or method with the same name and the same parameter list as the base class member, and you do not supply the `Shadows` keyword.</span></span>

<span data-ttu-id="e052b-137">如果使用 `Overrides`，编译器将隐式添加 `Overloads`，以便库 API 更轻松地使用 C#。</span><span class="sxs-lookup"><span data-stu-id="e052b-137">If you use `Overrides`, the compiler implicitly adds `Overloads` so that your library APIs work with C# more easily.</span></span>

<span data-ttu-id="e052b-138">`Overloads` 修饰符可用于下面的上下文中：</span><span class="sxs-lookup"><span data-stu-id="e052b-138">The `Overloads` modifier can be used in these contexts:</span></span>

- [<span data-ttu-id="e052b-139">Function 语句</span><span class="sxs-lookup"><span data-stu-id="e052b-139">Function Statement</span></span>](../statements/function-statement.md)

- [<span data-ttu-id="e052b-140">Operator Statement</span><span class="sxs-lookup"><span data-stu-id="e052b-140">Operator Statement</span></span>](../statements/operator-statement.md)

- [<span data-ttu-id="e052b-141">Property Statement</span><span class="sxs-lookup"><span data-stu-id="e052b-141">Property Statement</span></span>](../statements/property-statement.md)

- [<span data-ttu-id="e052b-142">Sub 语句</span><span class="sxs-lookup"><span data-stu-id="e052b-142">Sub Statement</span></span>](../statements/sub-statement.md)

## <a name="see-also"></a><span data-ttu-id="e052b-143">请参阅</span><span class="sxs-lookup"><span data-stu-id="e052b-143">See also</span></span>

- [<span data-ttu-id="e052b-144">Shadows</span><span class="sxs-lookup"><span data-stu-id="e052b-144">Shadows</span></span>](shadows.md)
- [<span data-ttu-id="e052b-145">过程重载</span><span class="sxs-lookup"><span data-stu-id="e052b-145">Procedure Overloading</span></span>](../../programming-guide/language-features/procedures/procedure-overloading.md)
- [<span data-ttu-id="e052b-146">Generic Types in Visual Basic</span><span class="sxs-lookup"><span data-stu-id="e052b-146">Generic Types in Visual Basic</span></span>](../../programming-guide/language-features/data-types/generic-types.md)
- [<span data-ttu-id="e052b-147">运算符过程</span><span class="sxs-lookup"><span data-stu-id="e052b-147">Operator Procedures</span></span>](../../programming-guide/language-features/procedures/operator-procedures.md)
- [<span data-ttu-id="e052b-148">如何：定义转换运算符</span><span class="sxs-lookup"><span data-stu-id="e052b-148">How to: Define a Conversion Operator</span></span>](../../programming-guide/language-features/procedures/how-to-define-a-conversion-operator.md)
