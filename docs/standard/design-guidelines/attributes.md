---
description: 详细了解：特性
title: 特性
ms.date: 10/22/2008
helpviewer_keywords:
- attributes [.NET Framework], about
- class library design guidelines [.NET Framework], attributes
ms.assetid: ee0038ef-b247-4747-a650-3c5c5cd58d8b
ms.openlocfilehash: 1557ba0945da0c8498c67f70ba4a01dd0bbe432e
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99642417"
---
# <a name="attributes"></a><span data-ttu-id="e9c78-103">特性</span><span class="sxs-lookup"><span data-stu-id="e9c78-103">Attributes</span></span>

<span data-ttu-id="e9c78-104"><xref:System.Attribute?displayProperty=nameWithType> 是用于定义自定义特性的基类。</span><span class="sxs-lookup"><span data-stu-id="e9c78-104"><xref:System.Attribute?displayProperty=nameWithType> is a base class used to define custom attributes.</span></span>

 <span data-ttu-id="e9c78-105">特性是可添加到编程元素（如程序集、类型、成员和参数）的注释。</span><span class="sxs-lookup"><span data-stu-id="e9c78-105">Attributes are annotations that can be added to programming elements such as assemblies, types, members, and parameters.</span></span> <span data-ttu-id="e9c78-106">它们存储在程序集的元数据中，并且可在运行时使用反射 API 进行访问。</span><span class="sxs-lookup"><span data-stu-id="e9c78-106">They are stored in the metadata of the assembly and can be accessed at runtime using the reflection APIs.</span></span> <span data-ttu-id="e9c78-107">例如，框架定义了 <xref:System.ObsoleteAttribute>，可将其应用于类型或成员，以指示该类型或成员已弃用。</span><span class="sxs-lookup"><span data-stu-id="e9c78-107">For example, the Framework defines the <xref:System.ObsoleteAttribute>, which can be applied to a type or a member to indicate that the type or member has been deprecated.</span></span>

 <span data-ttu-id="e9c78-108">特性可具有一个或多个属性，这些属性包含与特性相关的其他数据。</span><span class="sxs-lookup"><span data-stu-id="e9c78-108">Attributes can have one or more properties that carry additional data related to the attribute.</span></span> <span data-ttu-id="e9c78-109">例如，`ObsoleteAttribute` 可能包含有关其中某个类型或成员已弃用的版本的其他信息，以及替换已过时 API 的新 API 的说明。</span><span class="sxs-lookup"><span data-stu-id="e9c78-109">For example, `ObsoleteAttribute` could carry additional information about the release in which a type or a member got deprecated and the description of the new APIs replacing the obsolete API.</span></span>

 <span data-ttu-id="e9c78-110">应用某个特性时，必须指定该特性的某些属性。</span><span class="sxs-lookup"><span data-stu-id="e9c78-110">Some properties of an attribute must be specified when the attribute is applied.</span></span> <span data-ttu-id="e9c78-111">它们被称为必需属性或必需参数，因为它们被表示为位置构造函数参数。</span><span class="sxs-lookup"><span data-stu-id="e9c78-111">These are referred to as the required properties or required arguments, because they are represented as positional constructor parameters.</span></span> <span data-ttu-id="e9c78-112">例如，<xref:System.Diagnostics.ConditionalAttribute> 的 <xref:System.Diagnostics.ConditionalAttribute.ConditionString%2A> 属性是一个必需属性。</span><span class="sxs-lookup"><span data-stu-id="e9c78-112">For example, the <xref:System.Diagnostics.ConditionalAttribute.ConditionString%2A> property of the <xref:System.Diagnostics.ConditionalAttribute> is a required property.</span></span>

 <span data-ttu-id="e9c78-113">在应用特性时不一定要指定的属性称为可选属性（或可选参数）。</span><span class="sxs-lookup"><span data-stu-id="e9c78-113">Properties that do not necessarily have to be specified when the attribute is applied are called optional properties (or optional arguments).</span></span> <span data-ttu-id="e9c78-114">它们由可设置的属性表示。</span><span class="sxs-lookup"><span data-stu-id="e9c78-114">They are represented by settable properties.</span></span> <span data-ttu-id="e9c78-115">应用某个特性时，编译器提供了特殊的语法来设置这些属性。</span><span class="sxs-lookup"><span data-stu-id="e9c78-115">Compilers provide special syntax to set these properties when an attribute is applied.</span></span> <span data-ttu-id="e9c78-116">例如，<xref:System.AttributeUsageAttribute.Inherited%2A?displayProperty=nameWithType> 属性表示一个可选参数。</span><span class="sxs-lookup"><span data-stu-id="e9c78-116">For example, the <xref:System.AttributeUsageAttribute.Inherited%2A?displayProperty=nameWithType> property represents an optional argument.</span></span>

 <span data-ttu-id="e9c78-117">✔️ 请务必使用后缀“Attribute”来命名自定义属性类。</span><span class="sxs-lookup"><span data-stu-id="e9c78-117">✔️ DO name custom attribute classes with the suffix "Attribute."</span></span>

 <span data-ttu-id="e9c78-118">✔️ 请务必将 <xref:System.AttributeUsageAttribute> 应用于自定义属性。</span><span class="sxs-lookup"><span data-stu-id="e9c78-118">✔️ DO apply the <xref:System.AttributeUsageAttribute> to custom attributes.</span></span>

 <span data-ttu-id="e9c78-119">✔️ 请务必提供可选参数的可设置属性。</span><span class="sxs-lookup"><span data-stu-id="e9c78-119">✔️ DO provide settable properties for optional arguments.</span></span>

 <span data-ttu-id="e9c78-120">✔️ 请务必提供必需参数的仅限获取属性。</span><span class="sxs-lookup"><span data-stu-id="e9c78-120">✔️ DO provide get-only properties for required arguments.</span></span>

 <span data-ttu-id="e9c78-121">✔️ 请务必提供构造函数参数来初始化对应于必需参数的属性。</span><span class="sxs-lookup"><span data-stu-id="e9c78-121">✔️ DO provide constructor parameters to initialize properties corresponding to required arguments.</span></span> <span data-ttu-id="e9c78-122">每个参数都应具有与相应属性相同的名称（但大小写不同）。</span><span class="sxs-lookup"><span data-stu-id="e9c78-122">Each parameter should have the same name (although with different casing) as the corresponding property.</span></span>

 <span data-ttu-id="e9c78-123">❌ 请避免提供构造函数参数来初始化对应于可选参数的属性。</span><span class="sxs-lookup"><span data-stu-id="e9c78-123">❌ AVOID providing constructor parameters to initialize properties corresponding to the optional arguments.</span></span>

 <span data-ttu-id="e9c78-124">换句话说，请勿包含可同时使用构造函数和 setter 设置的属性。</span><span class="sxs-lookup"><span data-stu-id="e9c78-124">In other words, do not have properties that can be set with both a constructor and a setter.</span></span> <span data-ttu-id="e9c78-125">此准则非常明确地说明了哪些参数是可选的，哪些参数是必需的，并避免了用两种方法来执行相同的操作。</span><span class="sxs-lookup"><span data-stu-id="e9c78-125">This guideline makes very explicit which arguments are optional and which are required, and avoids having two ways of doing the same thing.</span></span>

 <span data-ttu-id="e9c78-126">❌ 请避免重载自定义特性构造函数。</span><span class="sxs-lookup"><span data-stu-id="e9c78-126">❌ AVOID overloading custom attribute constructors.</span></span>

 <span data-ttu-id="e9c78-127">只具有一个构造函数，这清楚地告诉了用户哪些参数是必需的，哪些参数是可选的。</span><span class="sxs-lookup"><span data-stu-id="e9c78-127">Having only one constructor clearly communicates to the user which arguments are required and which are optional.</span></span>

 <span data-ttu-id="e9c78-128">✔️ 如果可能，请务必密封自定义特性类。</span><span class="sxs-lookup"><span data-stu-id="e9c78-128">✔️ DO seal custom attribute classes, if possible.</span></span> <span data-ttu-id="e9c78-129">这样可以更快地查找特性。</span><span class="sxs-lookup"><span data-stu-id="e9c78-129">This makes the look-up for the attribute faster.</span></span>

 <span data-ttu-id="e9c78-130">*Portions &copy; 2005, 2009 Microsoft Corporation。保留所有权利。*</span><span class="sxs-lookup"><span data-stu-id="e9c78-130">*Portions &copy; 2005, 2009 Microsoft Corporation. All rights reserved.*</span></span>

 <span data-ttu-id="e9c78-131">在 Pearson Education, Inc. 授权下，由 Addison-Wesley Professional 作为 Microsoft Windows 开发系列的一部分再版自 [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619)（Framework 设计准则：可重用 .NET 库的约定、惯例和模式第 2 版），由 Krzysztof Cwalina 和 Brad Abrams 发布于 2008 年 10 月 22 日。</span><span class="sxs-lookup"><span data-stu-id="e9c78-131">*Reprinted by permission of Pearson Education, Inc. from [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) by Krzysztof Cwalina and Brad Abrams, published Oct 22, 2008 by Addison-Wesley Professional as part of the Microsoft Windows Development Series.*</span></span>

## <a name="see-also"></a><span data-ttu-id="e9c78-132">请参阅</span><span class="sxs-lookup"><span data-stu-id="e9c78-132">See also</span></span>

- [<span data-ttu-id="e9c78-133">框架设计指南</span><span class="sxs-lookup"><span data-stu-id="e9c78-133">Framework Design Guidelines</span></span>](index.md)
- [<span data-ttu-id="e9c78-134">使用准则</span><span class="sxs-lookup"><span data-stu-id="e9c78-134">Usage Guidelines</span></span>](usage-guidelines.md)
