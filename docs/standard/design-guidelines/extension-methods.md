---
description: 详细了解：扩展方法
title: 扩展方法
ms.date: 10/22/2008
ms.assetid: 5de945cb-88f4-49d7-b0e6-f098300cf357
ms.openlocfilehash: 2f71ec86252045687558bd61337164ac3afbcd20
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99642053"
---
# <a name="extension-methods"></a><span data-ttu-id="e9f0b-103">扩展方法</span><span class="sxs-lookup"><span data-stu-id="e9f0b-103">Extension Methods</span></span>

<span data-ttu-id="e9f0b-104">扩展方法是一项语言功能，允许使用实例方法调用语法来调用静态方法。</span><span class="sxs-lookup"><span data-stu-id="e9f0b-104">Extension methods are a language feature that allows static methods to be called using instance method call syntax.</span></span> <span data-ttu-id="e9f0b-105">这些方法必须至少采用一个参数，该参数表示方法要针对其操作的实例。</span><span class="sxs-lookup"><span data-stu-id="e9f0b-105">These methods must take at least one parameter, which represents the instance the method is to operate on.</span></span>

 <span data-ttu-id="e9f0b-106">定义此类扩展方法的类称为 sponsor 类，并且必须声明为静态。</span><span class="sxs-lookup"><span data-stu-id="e9f0b-106">The class that defines such extension methods is referred to as the "sponsor" class, and it must be declared as static.</span></span> <span data-ttu-id="e9f0b-107">若要使用扩展方法，必须导入用于定义 sponsor 类的命名空间。</span><span class="sxs-lookup"><span data-stu-id="e9f0b-107">To use extension methods, one must import the namespace defining the sponsor class.</span></span>

 <span data-ttu-id="e9f0b-108">❌ 请避免盲目地定义扩展方法，特别是对于不属于你的类型。</span><span class="sxs-lookup"><span data-stu-id="e9f0b-108">❌ AVOID frivolously defining extension methods, especially on types you don't own.</span></span>

 <span data-ttu-id="e9f0b-109">如果你确实拥有某个类型的源代码，请考虑改用常规实例方法。</span><span class="sxs-lookup"><span data-stu-id="e9f0b-109">If you do own source code of a type, consider using regular instance methods instead.</span></span> <span data-ttu-id="e9f0b-110">如果你没有某个类型的源代码，而你又想加一个方法，请务必要小心了。</span><span class="sxs-lookup"><span data-stu-id="e9f0b-110">If you don't own, and you want to add a method, be very careful.</span></span> <span data-ttu-id="e9f0b-111">自由地使用扩展方法可能会使那些未设计为具有这些方法的类型的 API 混杂在一起。</span><span class="sxs-lookup"><span data-stu-id="e9f0b-111">Liberal use of extension methods has the potential of cluttering APIs of types that were not designed to have these methods.</span></span>

 <span data-ttu-id="e9f0b-112">✔️ 请考虑在以下任何情况下使用扩展方法：</span><span class="sxs-lookup"><span data-stu-id="e9f0b-112">✔️ CONSIDER using extension methods in any of the following scenarios:</span></span>

- <span data-ttu-id="e9f0b-113">要提供与接口的每个实现相关的帮助程序功能（如果所述功能可根据核心接口进行编写）。</span><span class="sxs-lookup"><span data-stu-id="e9f0b-113">To provide helper functionality relevant to every implementation of an interface, if said functionality can be written in terms of the core interface.</span></span> <span data-ttu-id="e9f0b-114">这是因为不能以其他方式将具体实现分配给接口。</span><span class="sxs-lookup"><span data-stu-id="e9f0b-114">This is because concrete implementations cannot otherwise be assigned to interfaces.</span></span> <span data-ttu-id="e9f0b-115">例如，`LINQ to Objects` 运算符作为所有 <xref:System.Collections.Generic.IEnumerable%601> 类型的扩展方法实现。</span><span class="sxs-lookup"><span data-stu-id="e9f0b-115">For example, the `LINQ to Objects` operators are implemented as extension methods for all <xref:System.Collections.Generic.IEnumerable%601> types.</span></span> <span data-ttu-id="e9f0b-116">因此，任何 `IEnumerable<>` 实现都自动启用了 LINQ。</span><span class="sxs-lookup"><span data-stu-id="e9f0b-116">Thus, any `IEnumerable<>` implementation is automatically LINQ-enabled.</span></span>

- <span data-ttu-id="e9f0b-117">当实例方法会引入对某个类型的依赖项，但此类依赖项会破坏依赖项管理规则时。</span><span class="sxs-lookup"><span data-stu-id="e9f0b-117">When an instance method would introduce a dependency on some type, but such a dependency would break dependency management rules.</span></span> <span data-ttu-id="e9f0b-118">例如，从 <xref:System.String> 到 <xref:System.Uri?displayProperty=nameWithType> 的依赖项可能是不可取的，因此从依赖项管理的角度来看，返回 `System.Uri` 的 `String.ToUri()` 实例方法是错误的设计。</span><span class="sxs-lookup"><span data-stu-id="e9f0b-118">For example, a dependency from <xref:System.String> to <xref:System.Uri?displayProperty=nameWithType> is probably not desirable, and so `String.ToUri()` instance method returning `System.Uri` would be the wrong design from a dependency management perspective.</span></span> <span data-ttu-id="e9f0b-119">返回 `System.Uri` 的静态扩展方法 `Uri.ToUri(this string str)` 是一个更好的设计。</span><span class="sxs-lookup"><span data-stu-id="e9f0b-119">A static extension method `Uri.ToUri(this string str)` returning `System.Uri` would be a much better design.</span></span>

 <span data-ttu-id="e9f0b-120">❌ 请避免针对 <xref:System.Object?displayProperty=nameWithType> 定义扩展方法。</span><span class="sxs-lookup"><span data-stu-id="e9f0b-120">❌ AVOID defining extension methods on <xref:System.Object?displayProperty=nameWithType>.</span></span>

 <span data-ttu-id="e9f0b-121">VB 用户将无法使用扩展方法语法对对象引用调用此类方法。</span><span class="sxs-lookup"><span data-stu-id="e9f0b-121">VB users will not be able to call such methods on object references using the extension method syntax.</span></span> <span data-ttu-id="e9f0b-122">VB 不支持调用此类方法，因为在 VB 中，将引用声明为对象将强制对它的所有方法调用进行后期绑定（调用的实际成员是在运行时确定的），而对扩展方法的绑定是在编译时确定的（早期绑定）。</span><span class="sxs-lookup"><span data-stu-id="e9f0b-122">VB does not support calling such methods because, in VB, declaring a reference as Object forces all method invocations on it to be late bound (actual member called is determined at runtime), while bindings to extension methods are determined at compile-time (early bound).</span></span>

 <span data-ttu-id="e9f0b-123">请注意，本指南适用于存在相同绑定行为的其他语言，或者不支持扩展方法的其他语言。</span><span class="sxs-lookup"><span data-stu-id="e9f0b-123">Note that the guideline applies to other languages where the same binding behavior is present, or where extension methods are not supported.</span></span>

 <span data-ttu-id="e9f0b-124">❌ 请勿将扩展方法置于与扩展类型相同的命名空间中，除非它用于向接口添加方法或用于依赖项管理。</span><span class="sxs-lookup"><span data-stu-id="e9f0b-124">❌ DO NOT put extension methods in the same namespace as the extended type unless it is for adding methods to interfaces or for dependency management.</span></span>

 <span data-ttu-id="e9f0b-125">❌ 请避免使用相同的签名来定义两个或多个扩展方法（即使它们驻留在不同的命名空间中也是如此）。</span><span class="sxs-lookup"><span data-stu-id="e9f0b-125">❌ AVOID defining two or more extension methods with the same signature, even if they reside in different namespaces.</span></span>

 <span data-ttu-id="e9f0b-126">✔️ 如果扩展类型是一个接口，并且在大多数或所有情况下都要使用扩展方法，请考虑在与扩展类型相同的命名空间中定义扩展方法。</span><span class="sxs-lookup"><span data-stu-id="e9f0b-126">✔️ CONSIDER defining extension methods in the same namespace as the extended type if the type is an interface and if the extension methods are meant to be used in most or all cases.</span></span>

 <span data-ttu-id="e9f0b-127">❌ 请勿在通常与其他功能相关联的名称空间中定义实现某个功能的扩展方法。</span><span class="sxs-lookup"><span data-stu-id="e9f0b-127">❌ DO NOT define extension methods implementing a feature in namespaces normally associated with other features.</span></span> <span data-ttu-id="e9f0b-128">而应在与扩展方法所属的功能关联的命名空间中定义这些方法。</span><span class="sxs-lookup"><span data-stu-id="e9f0b-128">Instead, define them in the namespace associated with the feature they belong to.</span></span>

 <span data-ttu-id="e9f0b-129">❌ 请避免对专用于扩展方法的命名空间进行泛型命名（例如“Extension”）。</span><span class="sxs-lookup"><span data-stu-id="e9f0b-129">❌ AVOID generic naming of namespaces dedicated to extension methods (e.g., "Extensions").</span></span> <span data-ttu-id="e9f0b-130">请改用描述性名称（例如“Routing”）。</span><span class="sxs-lookup"><span data-stu-id="e9f0b-130">Use a descriptive name (e.g., "Routing") instead.</span></span>

 <span data-ttu-id="e9f0b-131">*Portions &copy; 2005, 2009 Microsoft Corporation。保留所有权利。*</span><span class="sxs-lookup"><span data-stu-id="e9f0b-131">*Portions &copy; 2005, 2009 Microsoft Corporation. All rights reserved.*</span></span>

 <span data-ttu-id="e9f0b-132">在 Pearson Education, Inc. 授权下，由 Addison-Wesley Professional 作为 Microsoft Windows 开发系列的一部分再版自 [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619)（Framework 设计准则：可重用 .NET 库的约定、惯例和模式第 2 版），由 Krzysztof Cwalina 和 Brad Abrams 发布于 2008 年 10 月 22 日。</span><span class="sxs-lookup"><span data-stu-id="e9f0b-132">*Reprinted by permission of Pearson Education, Inc. from [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) by Krzysztof Cwalina and Brad Abrams, published Oct 22, 2008 by Addison-Wesley Professional as part of the Microsoft Windows Development Series.*</span></span>

## <a name="see-also"></a><span data-ttu-id="e9f0b-133">请参阅</span><span class="sxs-lookup"><span data-stu-id="e9f0b-133">See also</span></span>

- [<span data-ttu-id="e9f0b-134">成员设计准则</span><span class="sxs-lookup"><span data-stu-id="e9f0b-134">Member Design Guidelines</span></span>](member.md)
- [<span data-ttu-id="e9f0b-135">框架设计指南</span><span class="sxs-lookup"><span data-stu-id="e9f0b-135">Framework Design Guidelines</span></span>](index.md)
