---
description: 详细了解：密封
title: 密封
ms.date: 10/22/2008
helpviewer_keywords:
- limiting extensibility
- classes [.NET Framework], sealing
- preventing customization
- sealed classes
ms.assetid: cc42267f-bb7a-427a-845e-df97408528d4
ms.openlocfilehash: 94673f793aa7373e1076e13cbda900fba83786f6
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99731716"
---
# <a name="sealing"></a><span data-ttu-id="32b44-103">密封</span><span class="sxs-lookup"><span data-stu-id="32b44-103">Sealing</span></span>

<span data-ttu-id="32b44-104">面向对象的框架的一项功能是，开发人员可采用框架设计者无法预料的方式对其进行扩展和自定义。</span><span class="sxs-lookup"><span data-stu-id="32b44-104">One of the features of object-oriented frameworks is that developers can extend and customize them in ways unanticipated by the framework designers.</span></span> <span data-ttu-id="32b44-105">这是可扩展设计的强大之处，也是危险之处。</span><span class="sxs-lookup"><span data-stu-id="32b44-105">This is both the power and danger of extensible design.</span></span> <span data-ttu-id="32b44-106">因此，当你设计框架时，非常重要的一点是在需要时仔细设计以实现扩展性，而在有风险时限制扩展性。</span><span class="sxs-lookup"><span data-stu-id="32b44-106">When you design your framework, it is, therefore, very important to carefully design for extensibility when it is desired, and to limit extensibility when it is dangerous.</span></span>

 <span data-ttu-id="32b44-107">阻止扩展性的强大机制是密封的。</span><span class="sxs-lookup"><span data-stu-id="32b44-107">A powerful mechanism that prevents extensibility is sealing.</span></span> <span data-ttu-id="32b44-108">可以密封类或单个成员。</span><span class="sxs-lookup"><span data-stu-id="32b44-108">You can seal either the class or individual members.</span></span> <span data-ttu-id="32b44-109">密封一个类可防止用户从该类继承。</span><span class="sxs-lookup"><span data-stu-id="32b44-109">Sealing a class prevents users from inheriting from the class.</span></span> <span data-ttu-id="32b44-110">密封一个成员可防止用户替代特定成员。</span><span class="sxs-lookup"><span data-stu-id="32b44-110">Sealing a member prevents users from overriding a particular member.</span></span>

 <span data-ttu-id="32b44-111">❌ 若没有充分的理由，请勿密封类。</span><span class="sxs-lookup"><span data-stu-id="32b44-111">❌ DO NOT seal classes without having a good reason to do so.</span></span>

 <span data-ttu-id="32b44-112">因为想不出扩展性场景而密封类不是一个充分的理由。</span><span class="sxs-lookup"><span data-stu-id="32b44-112">Sealing a class because you cannot think of an extensibility scenario is not a good reason.</span></span> <span data-ttu-id="32b44-113">框架用户喜欢出于各种非显着性的原因而从类中继承，比如添加便捷成员。</span><span class="sxs-lookup"><span data-stu-id="32b44-113">Framework users like to inherit from classes for various nonobvious reasons, like adding convenience members.</span></span> <span data-ttu-id="32b44-114">有关用户要从某类型继承的非显着性原因的示例，请参阅[非密封类](unsealed-classes.md)。</span><span class="sxs-lookup"><span data-stu-id="32b44-114">See [Unsealed Classes](unsealed-classes.md) for examples of nonobvious reasons users want to inherit from a type.</span></span>

 <span data-ttu-id="32b44-115">密封一个类的充分理由包括：</span><span class="sxs-lookup"><span data-stu-id="32b44-115">Good reasons for sealing a class include the following:</span></span>

- <span data-ttu-id="32b44-116">类是一个静态类。</span><span class="sxs-lookup"><span data-stu-id="32b44-116">The class is a static class.</span></span> <span data-ttu-id="32b44-117">请参阅[静态类设计](static-class.md)。</span><span class="sxs-lookup"><span data-stu-id="32b44-117">See [Static Class Design](static-class.md).</span></span>

- <span data-ttu-id="32b44-118">类在继承的受保护成员中存储对安全性敏感的机密。</span><span class="sxs-lookup"><span data-stu-id="32b44-118">The class stores security-sensitive secrets in inherited protected members.</span></span>

- <span data-ttu-id="32b44-119">类继承许多虚拟成员，且单独密封它们的成本将超过使该类不密封的好处。</span><span class="sxs-lookup"><span data-stu-id="32b44-119">The class inherits many virtual members and the cost of sealing them individually would outweigh the benefits of leaving the class unsealed.</span></span>

- <span data-ttu-id="32b44-120">类是一个需要非常快速的运行时查找的特性。</span><span class="sxs-lookup"><span data-stu-id="32b44-120">The class is an attribute that requires very fast runtime look-up.</span></span> <span data-ttu-id="32b44-121">密封特性的性能水平略高于非密封特性。</span><span class="sxs-lookup"><span data-stu-id="32b44-121">Sealed attributes have slightly higher performance levels than unsealed ones.</span></span> <span data-ttu-id="32b44-122">请参阅[特性](attributes.md)。</span><span class="sxs-lookup"><span data-stu-id="32b44-122">See [Attributes](attributes.md).</span></span>

 <span data-ttu-id="32b44-123">❌ 请勿对密封类型声明受保护的成员或虚拟成员。</span><span class="sxs-lookup"><span data-stu-id="32b44-123">❌ DO NOT declare protected or virtual members on sealed types.</span></span>

 <span data-ttu-id="32b44-124">按照定义，不能从密封类型继承。</span><span class="sxs-lookup"><span data-stu-id="32b44-124">By definition, sealed types cannot be inherited from.</span></span> <span data-ttu-id="32b44-125">这意味着不能调用密封类型的受保护成员，也不能替代密封类型的虚拟方法。</span><span class="sxs-lookup"><span data-stu-id="32b44-125">This means that protected members on sealed types cannot be called, and virtual methods on sealed types cannot be overridden.</span></span>

 <span data-ttu-id="32b44-126">✔️ 请考虑密封你替代的成员。</span><span class="sxs-lookup"><span data-stu-id="32b44-126">✔️ CONSIDER sealing members that you override.</span></span>

 <span data-ttu-id="32b44-127">引入虚拟成员（如[虚拟成员](virtual-members.md)中所述）可能导致的问题也同样适用于替代（尽管程度稍低）。</span><span class="sxs-lookup"><span data-stu-id="32b44-127">Problems that can result from introducing virtual members (discussed in [Virtual Members](virtual-members.md)) apply to overrides as well, although to a slightly lesser degree.</span></span> <span data-ttu-id="32b44-128">密封替代可以使你从继承层次结构中的这一点开始就避免这些问题。</span><span class="sxs-lookup"><span data-stu-id="32b44-128">Sealing an override shields you from these problems starting from that point in the inheritance hierarchy.</span></span>

 <span data-ttu-id="32b44-129">*Portions © 2005, 2009 Microsoft Corporation 版权所有。保留所有权利。*</span><span class="sxs-lookup"><span data-stu-id="32b44-129">*Portions © 2005, 2009 Microsoft Corporation. All rights reserved.*</span></span>

 <span data-ttu-id="32b44-130">在 Pearson Education, Inc. 授权下，由 Addison-Wesley Professional 作为 Microsoft Windows 开发系列的一部分再版自 [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619)（Framework 设计准则：可重用 .NET 库的约定、惯例和模式第 2 版），由 Krzysztof Cwalina 和 Brad Abrams 发布于 2008 年 10 月 22 日。</span><span class="sxs-lookup"><span data-stu-id="32b44-130">*Reprinted by permission of Pearson Education, Inc. from [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) by Krzysztof Cwalina and Brad Abrams, published Oct 22, 2008 by Addison-Wesley Professional as part of the Microsoft Windows Development Series.*</span></span>

## <a name="see-also"></a><span data-ttu-id="32b44-131">请参阅</span><span class="sxs-lookup"><span data-stu-id="32b44-131">See also</span></span>

- [<span data-ttu-id="32b44-132">框架设计指南</span><span class="sxs-lookup"><span data-stu-id="32b44-132">Framework Design Guidelines</span></span>](index.md)
- [<span data-ttu-id="32b44-133">扩展性设计</span><span class="sxs-lookup"><span data-stu-id="32b44-133">Designing for Extensibility</span></span>](designing-for-extensibility.md)
- [<span data-ttu-id="32b44-134">未密封类</span><span class="sxs-lookup"><span data-stu-id="32b44-134">Unsealed Classes</span></span>](unsealed-classes.md)
