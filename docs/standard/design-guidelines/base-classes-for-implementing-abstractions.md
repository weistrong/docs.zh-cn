---
description: 详细了解：用于实现抽象的基类
title: 用于实现抽象的基类
ms.date: 10/22/2008
helpviewer_keywords:
- abstractions [.NET Framework]
- base classes, abstractions
ms.assetid: 37a2d9a4-9721-482a-a40f-eee2c1d97875
ms.openlocfilehash: 255891695583e36977663153b0ccac98b7fff4c6
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99642339"
---
# <a name="base-classes-for-implementing-abstractions"></a><span data-ttu-id="3b403-103">用于实现抽象的基类</span><span class="sxs-lookup"><span data-stu-id="3b403-103">Base Classes for Implementing Abstractions</span></span>

<span data-ttu-id="3b403-104">严格地说，当一个类派生出另一个类时，这个类就变成了基类。</span><span class="sxs-lookup"><span data-stu-id="3b403-104">Strictly speaking, a class becomes a base class when another class is derived from it.</span></span> <span data-ttu-id="3b403-105">然而，就本部分而言，基类是一个主要设计用来提供一个公共抽象或者让其他类通过继承来重用一些默认实现的类。</span><span class="sxs-lookup"><span data-stu-id="3b403-105">For the purpose of this section, however, a base class is a class designed mainly to provide a common abstraction or for other classes to reuse some default implementation though inheritance.</span></span> <span data-ttu-id="3b403-106">基类通常位于继承层次结构的中间 - 介于层次结构根的抽象与底部的几个自定义实现之间。</span><span class="sxs-lookup"><span data-stu-id="3b403-106">Base classes usually sit in the middle of inheritance hierarchies, between an abstraction at the root of a hierarchy and several custom implementations at the bottom.</span></span>

 <span data-ttu-id="3b403-107">它们充当用于实现抽象的实现帮助程序。</span><span class="sxs-lookup"><span data-stu-id="3b403-107">They serve as implementation helpers for implementing abstractions.</span></span> <span data-ttu-id="3b403-108">例如，框架对有序项集合的一种抽象是 <xref:System.Collections.Generic.IList%601> 接口。</span><span class="sxs-lookup"><span data-stu-id="3b403-108">For example, one of the Framework’s abstractions for ordered collections of items is the <xref:System.Collections.Generic.IList%601> interface.</span></span> <span data-ttu-id="3b403-109">实现 <xref:System.Collections.Generic.IList%601> 并不简单，因此框架提供了多个基类，如 <xref:System.Collections.ObjectModel.Collection%601> 和 <xref:System.Collections.ObjectModel.KeyedCollection%602>，它们充当用于实现自定义集合的帮助程序。</span><span class="sxs-lookup"><span data-stu-id="3b403-109">Implementing <xref:System.Collections.Generic.IList%601> is not trivial, and therefore the Framework provides several base classes, such as <xref:System.Collections.ObjectModel.Collection%601> and <xref:System.Collections.ObjectModel.KeyedCollection%602>, which serve as helpers for implementing custom collections.</span></span>

 <span data-ttu-id="3b403-110">基类本身通常不适合充当抽象，因为它们往往包含太多的实现。</span><span class="sxs-lookup"><span data-stu-id="3b403-110">Base classes are usually not suited to serve as abstractions by themselves, because they tend to contain too much implementation.</span></span> <span data-ttu-id="3b403-111">例如，`Collection<T>` 基类包含许多实现，这些实现与以下事实有关：它实现非泛型的 `IList` 接口（以便更好地与非泛型集合集成），并且它是存储在内存中某个字段中的项集合。</span><span class="sxs-lookup"><span data-stu-id="3b403-111">For example, the `Collection<T>` base class contains lots of implementation related to the fact that it implements the nongeneric `IList` interface (to integrate better with nongeneric collections) and to the fact that it is a collection of items stored in memory in one of its fields.</span></span>

 <span data-ttu-id="3b403-112">如前所述，基类可为需要实现抽象的用户提供十分宝贵的帮助，但同时它们也是一个很大的负担。</span><span class="sxs-lookup"><span data-stu-id="3b403-112">As previously discussed, base classes can provide invaluable help for users who need to implement abstractions, but at the same time they can be a significant liability.</span></span> <span data-ttu-id="3b403-113">它们增加了外围应用，加深了继承层次结构的深度，因此在概念上使框架复杂化。</span><span class="sxs-lookup"><span data-stu-id="3b403-113">They add surface area and increase the depth of inheritance hierarchies and so conceptually complicate the framework.</span></span> <span data-ttu-id="3b403-114">因此，只有当基类为框架的用户提供重要的价值时，才应该使用基类。</span><span class="sxs-lookup"><span data-stu-id="3b403-114">Therefore, base classes should be used only if they provide significant value to the users of the framework.</span></span> <span data-ttu-id="3b403-115">如果它们只为框架的实现者提供价值，就应该避免使用它们，在这种情况下，强烈推荐考虑委托给内部实现，而不是从基类继承。</span><span class="sxs-lookup"><span data-stu-id="3b403-115">They should be avoided if they provide value only to the implementers of the framework, in which case delegation to an internal implementation instead of inheritance from a base class should be strongly considered.</span></span>

 <span data-ttu-id="3b403-116">✔️ 请考虑使基类抽象，即使它们不包含任何抽象成员也是如此。</span><span class="sxs-lookup"><span data-stu-id="3b403-116">✔️ CONSIDER making base classes abstract even if they don’t contain any abstract members.</span></span> <span data-ttu-id="3b403-117">这清楚地向用户传达了该类专门为从其继承而设计。</span><span class="sxs-lookup"><span data-stu-id="3b403-117">This clearly communicates to the users that the class is designed solely to be inherited from.</span></span>

 <span data-ttu-id="3b403-118">✔️ 请考虑将基类置于与主流场景类型不同的命名空间中。</span><span class="sxs-lookup"><span data-stu-id="3b403-118">✔️ CONSIDER placing base classes in a separate namespace from the mainline scenario types.</span></span> <span data-ttu-id="3b403-119">根据定义，基类旨在用于高级扩展性场景，因此大多数用户对此不感兴趣。</span><span class="sxs-lookup"><span data-stu-id="3b403-119">By definition, base classes are intended for advanced extensibility scenarios and therefore are not interesting to the majority of users.</span></span>

 <span data-ttu-id="3b403-120">❌ 如果打算在公共 API 中使用基类，请避免用“Base”后缀来命名该类。</span><span class="sxs-lookup"><span data-stu-id="3b403-120">❌ AVOID naming base classes with a "Base" suffix if the class is intended for use in public APIs.</span></span>

 <span data-ttu-id="3b403-121">*Portions © 2005, 2009 Microsoft Corporation 版权所有。保留所有权利。*</span><span class="sxs-lookup"><span data-stu-id="3b403-121">*Portions © 2005, 2009 Microsoft Corporation. All rights reserved.*</span></span>

 <span data-ttu-id="3b403-122">在 Pearson Education, Inc. 授权下，由 Addison-Wesley Professional 作为 Microsoft Windows 开发系列的一部分再版自 [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619)（Framework 设计准则：可重用 .NET 库的约定、惯例和模式第 2 版），由 Krzysztof Cwalina 和 Brad Abrams 发布于 2008 年 10 月 22 日。</span><span class="sxs-lookup"><span data-stu-id="3b403-122">*Reprinted by permission of Pearson Education, Inc. from [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) by Krzysztof Cwalina and Brad Abrams, published Oct 22, 2008 by Addison-Wesley Professional as part of the Microsoft Windows Development Series.*</span></span>

## <a name="see-also"></a><span data-ttu-id="3b403-123">请参阅</span><span class="sxs-lookup"><span data-stu-id="3b403-123">See also</span></span>

- [<span data-ttu-id="3b403-124">框架设计指南</span><span class="sxs-lookup"><span data-stu-id="3b403-124">Framework Design Guidelines</span></span>](index.md)
- [<span data-ttu-id="3b403-125">扩展性设计</span><span class="sxs-lookup"><span data-stu-id="3b403-125">Designing for Extensibility</span></span>](designing-for-extensibility.md)
