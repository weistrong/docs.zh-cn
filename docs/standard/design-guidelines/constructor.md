---
description: 详细了解：构造函数设计
title: 构造函数设计
ms.date: 10/22/2008
helpviewer_keywords:
- member design guidelines, constructors
- constructors, design guidelines
- instance constructors
- type constructors
- virtual members
- constructors, types
- parameterless constructors
- static constructors
ms.assetid: b4496afe-5fa7-4bb0-85ca-70b0ef21e6fc
ms.openlocfilehash: 2a5c85e1dea3349f897c24fa5d40d73c6e1f9d7f
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99642313"
---
# <a name="constructor-design"></a><span data-ttu-id="66c99-103">构造函数设计</span><span class="sxs-lookup"><span data-stu-id="66c99-103">Constructor Design</span></span>

<span data-ttu-id="66c99-104">有两种类型的构造函数：类型构造函数和实例构造函数。</span><span class="sxs-lookup"><span data-stu-id="66c99-104">There are two kinds of constructors: type constructors and instance constructors.</span></span>

<span data-ttu-id="66c99-105">类型构造函数是静态的构造函数，在使用类型之前由 CLR 运行。</span><span class="sxs-lookup"><span data-stu-id="66c99-105">Type constructors are static and are run by the CLR before the type is used.</span></span> <span data-ttu-id="66c99-106">实例构造函数在创建类型的实例时运行。</span><span class="sxs-lookup"><span data-stu-id="66c99-106">Instance constructors run when an instance of a type is created.</span></span>

<span data-ttu-id="66c99-107">类型构造函数不能采用任何参数。</span><span class="sxs-lookup"><span data-stu-id="66c99-107">Type constructors cannot take any parameters.</span></span> <span data-ttu-id="66c99-108">而实例构造函数可以。</span><span class="sxs-lookup"><span data-stu-id="66c99-108">Instance constructors can.</span></span> <span data-ttu-id="66c99-109">不采用任何参数的实例构造函数通常称为无参数构造函数。</span><span class="sxs-lookup"><span data-stu-id="66c99-109">Instance constructors that don’t take any parameters are often called parameterless constructors.</span></span>

<span data-ttu-id="66c99-110">构造函数是创建类型的实例的最自然方式。</span><span class="sxs-lookup"><span data-stu-id="66c99-110">Constructors are the most natural way to create instances of a type.</span></span> <span data-ttu-id="66c99-111">大多数开发人员在考虑创建实例的替代方法（如工厂方法）之前，会搜索并尝试使用构造函数。</span><span class="sxs-lookup"><span data-stu-id="66c99-111">Most developers will search and try to use a constructor before they consider alternative ways of creating instances (such as factory methods).</span></span>

<span data-ttu-id="66c99-112">✔️ 请考虑提供简单的（理想情况下为默认设置）构造函数。</span><span class="sxs-lookup"><span data-stu-id="66c99-112">✔️ CONSIDER providing simple, ideally default, constructors.</span></span>

<span data-ttu-id="66c99-113">简单的构造函数包含的参数非常少，且所有参数均为基元或枚举。</span><span class="sxs-lookup"><span data-stu-id="66c99-113">A simple constructor has a very small number of parameters, and all parameters are primitives or enums.</span></span> <span data-ttu-id="66c99-114">此类简单的构造函数可提高框架的可用性。</span><span class="sxs-lookup"><span data-stu-id="66c99-114">Such simple constructors increase usability of the framework.</span></span>

<span data-ttu-id="66c99-115">✔️ 如果所需操作的语义没有直接映射到新实例的构造，或者如果遵循构造函数设计准则感觉不自然，请考虑使用静态工厂方法而不是构造函数。</span><span class="sxs-lookup"><span data-stu-id="66c99-115">✔️ CONSIDER using a static factory method instead of a constructor if the semantics of the desired operation do not map directly to the construction of a new instance, or if following the constructor design guidelines feels unnatural.</span></span>

<span data-ttu-id="66c99-116">✔️ 请务必使用构造函数参数作为设置主属性的快捷方式。</span><span class="sxs-lookup"><span data-stu-id="66c99-116">✔️ DO use constructor parameters as shortcuts for setting main properties.</span></span>

<span data-ttu-id="66c99-117">使用后跟一些属性集的空构造函数和使用带有多个参数的构造函数在语义上应该不存在任何差异。</span><span class="sxs-lookup"><span data-stu-id="66c99-117">There should be no difference in semantics between using the empty constructor followed by some property sets and using a constructor with multiple arguments.</span></span>

<span data-ttu-id="66c99-118">✔️ 如果构造函数参数只是用来设置属性，请务必对构造函数参数和属性使用相同的名称。</span><span class="sxs-lookup"><span data-stu-id="66c99-118">✔️ DO use the same name for constructor parameters and a property if the constructor parameters are used to simply set the property.</span></span>

<span data-ttu-id="66c99-119">此类参数和属性的唯一区别应该是大小写形式。</span><span class="sxs-lookup"><span data-stu-id="66c99-119">The only difference between such parameters and the properties should be casing.</span></span>

<span data-ttu-id="66c99-120">✔️ 在构造函数中执行最少的工作。</span><span class="sxs-lookup"><span data-stu-id="66c99-120">✔️ DO minimal work in the constructor.</span></span>

<span data-ttu-id="66c99-121">除了捕获构造函数参数外，构造函数不应执行太多工作。</span><span class="sxs-lookup"><span data-stu-id="66c99-121">Constructors should not do much work other than capture the constructor parameters.</span></span> <span data-ttu-id="66c99-122">任何其他处理的成本都应延迟到需要时再进行。</span><span class="sxs-lookup"><span data-stu-id="66c99-122">The cost of any other processing should be delayed until required.</span></span>

<span data-ttu-id="66c99-123">✔️ 在适当情况下，请务必从实例构造函数引发异常。</span><span class="sxs-lookup"><span data-stu-id="66c99-123">✔️ DO throw exceptions from instance constructors, if appropriate.</span></span>

<span data-ttu-id="66c99-124">✔️ 如果需要公共无参数构造函数，请务必在类中显式声明此类构造函数。</span><span class="sxs-lookup"><span data-stu-id="66c99-124">✔️ DO explicitly declare the public parameterless constructor in classes, if such a constructor is required.</span></span>

<span data-ttu-id="66c99-125">如果未针对某个类型显式声明任何构造函数，则许多语言（如 C#）将自动添加一个公共无参数构造函数。</span><span class="sxs-lookup"><span data-stu-id="66c99-125">If you don’t explicitly declare any constructors on a type, many languages (such as C#) will automatically add a public parameterless constructor.</span></span> <span data-ttu-id="66c99-126">（抽象类获取一个受保护的构造函数。）</span><span class="sxs-lookup"><span data-stu-id="66c99-126">(Abstract classes get a protected constructor.)</span></span>

<span data-ttu-id="66c99-127">向类添加参数化构造函数会阻止编译器添加无参数构造函数。</span><span class="sxs-lookup"><span data-stu-id="66c99-127">Adding a parameterized constructor to a class prevents the compiler from adding the parameterless constructor.</span></span> <span data-ttu-id="66c99-128">这通常会导致意外的中断性变更。</span><span class="sxs-lookup"><span data-stu-id="66c99-128">This often causes accidental breaking changes.</span></span>

<span data-ttu-id="66c99-129">❌ 请避免对结构显式定义无参数构造函数。</span><span class="sxs-lookup"><span data-stu-id="66c99-129">❌ AVOID explicitly defining parameterless constructors on structs.</span></span>

<span data-ttu-id="66c99-130">这样可以更快地创建数组，因为如果没有定义无参数构造函数，它就不必在数组的每个槽上运行。</span><span class="sxs-lookup"><span data-stu-id="66c99-130">This makes array creation faster, because if the parameterless constructor is not defined, it does not have to be run on every slot in the array.</span></span> <span data-ttu-id="66c99-131">请注意，由于此原因，包许多编译器（包括 C#）不允许结构具有无参数构造函数。</span><span class="sxs-lookup"><span data-stu-id="66c99-131">Note that many compilers, including C#, don’t allow structs to have parameterless constructors for this reason.</span></span>

<span data-ttu-id="66c99-132">❌ 请避免在对象的构造函数中对该对象调用虚拟成员。</span><span class="sxs-lookup"><span data-stu-id="66c99-132">❌ AVOID calling virtual members on an object inside its constructor.</span></span>

<span data-ttu-id="66c99-133">调用虚拟成员将导致调用派生度最高的替代，即使派生度最高的类型的构造函数尚未完全运行也是如此。</span><span class="sxs-lookup"><span data-stu-id="66c99-133">Calling a virtual member will cause the most derived override to be called, even if the constructor of the most derived type has not been fully run yet.</span></span>

## <a name="type-constructor-guidelines"></a><span data-ttu-id="66c99-134">类型构造函数指南</span><span class="sxs-lookup"><span data-stu-id="66c99-134">Type Constructor Guidelines</span></span>

<span data-ttu-id="66c99-135">✔️ 请务必使静态构造函数专用。</span><span class="sxs-lookup"><span data-stu-id="66c99-135">✔️ DO make static constructors private.</span></span>

<span data-ttu-id="66c99-136">静态构造函数（也称为类构造函数）用于初始化类型。</span><span class="sxs-lookup"><span data-stu-id="66c99-136">A static constructor, also called a class constructor, is used to initialize a type.</span></span> <span data-ttu-id="66c99-137">在创建第一个类型实例或调用该类型的任何静态成员之前，CLR 调用静态构造函数。</span><span class="sxs-lookup"><span data-stu-id="66c99-137">The CLR calls the static constructor before the first instance of the type is created or any static members on that type are called.</span></span> <span data-ttu-id="66c99-138">用户无法控制调用静态构造函数的时间。</span><span class="sxs-lookup"><span data-stu-id="66c99-138">The user has no control over when the static constructor is called.</span></span> <span data-ttu-id="66c99-139">如果静态构造函数不是专用的，则 CLR 以外的代码可以调用它。</span><span class="sxs-lookup"><span data-stu-id="66c99-139">If a static constructor is not private, it can be called by code other than the CLR.</span></span> <span data-ttu-id="66c99-140">根据构造函数中执行的操作，这可能导致意外行为。</span><span class="sxs-lookup"><span data-stu-id="66c99-140">Depending on the operations performed in the constructor, this can cause unexpected behavior.</span></span> <span data-ttu-id="66c99-141">C# 编译器会强制使静态构造函数专用。</span><span class="sxs-lookup"><span data-stu-id="66c99-141">The C# compiler forces static constructors to be private.</span></span>

<span data-ttu-id="66c99-142">❌ 请勿从静态构造函数引发异常。</span><span class="sxs-lookup"><span data-stu-id="66c99-142">❌ DO NOT throw exceptions from static constructors.</span></span>

<span data-ttu-id="66c99-143">如果从类型构造函数引发了一个异常，则该类型在当前应用程序域中不可用。</span><span class="sxs-lookup"><span data-stu-id="66c99-143">If an exception is thrown from a type constructor, the type is not usable in the current application domain.</span></span>

<span data-ttu-id="66c99-144">✔️ 请考虑使用静态构造函数以内联方式（而非显式地）初始化静态字段，因为运行时能够优化不具有显式定义的静态构造函数的类型的性能。</span><span class="sxs-lookup"><span data-stu-id="66c99-144">✔️ CONSIDER initializing static fields inline rather than explicitly using static constructors, because the runtime is able to optimize the performance of types that don’t have an explicitly defined static constructor.</span></span>

<span data-ttu-id="66c99-145">*Portions © 2005, 2009 Microsoft Corporation 版权所有。保留所有权利。*</span><span class="sxs-lookup"><span data-stu-id="66c99-145">*Portions © 2005, 2009 Microsoft Corporation. All rights reserved.*</span></span>

<span data-ttu-id="66c99-146">在 Pearson Education, Inc. 授权下，由 Addison-Wesley Professional 作为 Microsoft Windows 开发系列的一部分再版自 [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619)（Framework 设计准则：可重用 .NET 库的约定、惯例和模式第 2 版），由 Krzysztof Cwalina 和 Brad Abrams 发布于 2008 年 10 月 22 日。</span><span class="sxs-lookup"><span data-stu-id="66c99-146">*Reprinted by permission of Pearson Education, Inc. from [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) by Krzysztof Cwalina and Brad Abrams, published Oct 22, 2008 by Addison-Wesley Professional as part of the Microsoft Windows Development Series.*</span></span>

## <a name="see-also"></a><span data-ttu-id="66c99-147">请参阅</span><span class="sxs-lookup"><span data-stu-id="66c99-147">See also</span></span>

- [<span data-ttu-id="66c99-148">成员设计准则</span><span class="sxs-lookup"><span data-stu-id="66c99-148">Member Design Guidelines</span></span>](member.md)
- [<span data-ttu-id="66c99-149">框架设计指南</span><span class="sxs-lookup"><span data-stu-id="66c99-149">Framework Design Guidelines</span></span>](index.md)
