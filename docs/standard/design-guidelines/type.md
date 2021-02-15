---
description: 详细了解：类型设计准则
title: 类型设计准则
ms.date: 10/22/2008
helpviewer_keywords:
- type design guidelines
- type design guidelines, about type design guidelines
- class library design guidelines [.NET Framework], type design guidelines
- types [.NET Framework], design guidelines
ms.assetid: 6b49314e-8bba-43ea-97ca-4e0255812f95
ms.openlocfilehash: d2c193d41dda118558cc5e7541f7e2dfbaf1a369
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99641832"
---
# <a name="type-design-guidelines"></a><span data-ttu-id="70840-103">类型设计准则</span><span class="sxs-lookup"><span data-stu-id="70840-103">Type Design Guidelines</span></span>

<span data-ttu-id="70840-104">从 CLR 的角度来看，只有两种类型：引用类型和值类型，但为了讨论框架设计，我们将类型分成更多的逻辑组，每个逻辑组都有自己特定的设计规则。</span><span class="sxs-lookup"><span data-stu-id="70840-104">From the CLR perspective, there are only two categories of types—reference types and value types—but for the purpose of a discussion about framework design, we divide types into more logical groups, each with its own specific design rules.</span></span>

 <span data-ttu-id="70840-105">类是引用类型的常规用例。</span><span class="sxs-lookup"><span data-stu-id="70840-105">Classes are the general case of reference types.</span></span> <span data-ttu-id="70840-106">它们构成了大多数框架中的大部分类型。</span><span class="sxs-lookup"><span data-stu-id="70840-106">They make up the bulk of types in the majority of frameworks.</span></span> <span data-ttu-id="70840-107">类之所以受欢迎，是因为它们支持一组丰富的面向对象的功能以及它们的普遍适用性。</span><span class="sxs-lookup"><span data-stu-id="70840-107">Classes owe their popularity to the rich set of object-oriented features they support and to their general applicability.</span></span> <span data-ttu-id="70840-108">基类和抽象类是与扩展性相关的特殊逻辑组。</span><span class="sxs-lookup"><span data-stu-id="70840-108">Base classes and abstract classes are special logical groups related to extensibility.</span></span>

 <span data-ttu-id="70840-109">接口是可由引用类型和值类型实现的类型。</span><span class="sxs-lookup"><span data-stu-id="70840-109">Interfaces are types that can be implemented by both reference types and value types.</span></span> <span data-ttu-id="70840-110">因此，它们可充当引用类型和值类型的多态层次结构的根。</span><span class="sxs-lookup"><span data-stu-id="70840-110">They can thus serve as roots of polymorphic hierarchies of reference types and value types.</span></span> <span data-ttu-id="70840-111">此外，接口还可用于模拟多重继承，而这是 CLR 本机不支持的。</span><span class="sxs-lookup"><span data-stu-id="70840-111">In addition, interfaces can be used to simulate multiple inheritance, which is not natively supported by the CLR.</span></span>

 <span data-ttu-id="70840-112">结构是值类型的常规用例，应为小型简单类型保留，类似于语言基元。</span><span class="sxs-lookup"><span data-stu-id="70840-112">Structs are the general case of value types and should be reserved for small, simple types, similar to language primitives.</span></span>

 <span data-ttu-id="70840-113">枚举是值类型的一种特例，用于定义短值集，如星期几、控制台颜色等。</span><span class="sxs-lookup"><span data-stu-id="70840-113">Enums are a special case of value types used to define short sets of values, such as days of the week, console colors, and so on.</span></span>

 <span data-ttu-id="70840-114">静态类是旨在作为静态成员容器的类型。</span><span class="sxs-lookup"><span data-stu-id="70840-114">Static classes are types intended to be containers for static members.</span></span> <span data-ttu-id="70840-115">它们通常用于提供其他操作的快捷方式。</span><span class="sxs-lookup"><span data-stu-id="70840-115">They are commonly used to provide shortcuts to other operations.</span></span>

 <span data-ttu-id="70840-116">委托、异常、特性、数组和集合都是专用于特定用途的引用类型的特例，它们的设计和使用指南在本书的其他位置进行了讨论。</span><span class="sxs-lookup"><span data-stu-id="70840-116">Delegates, exceptions, attributes, arrays, and collections are all special cases of reference types intended for specific uses, and guidelines for their design and usage are discussed elsewhere in this book.</span></span>

 <span data-ttu-id="70840-117">✔️ 请务必确保每个类型都是一组定义完善的相关成员，而不只是一个随机的无关功能集合。</span><span class="sxs-lookup"><span data-stu-id="70840-117">✔️ DO ensure that each type is a well-defined set of related members, not just a random collection of unrelated functionality.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="70840-118">本节内容</span><span class="sxs-lookup"><span data-stu-id="70840-118">In This Section</span></span>

 <span data-ttu-id="70840-119">[在类和结构之间选择](choosing-between-class-and-struct.md) [抽象类设计](abstract-class.md) [静态类设计](static-class.md) [接口设计](interface.md) [结构设计](struct.md) [枚举设计](enum.md) [嵌套设计](nested-types.md) *Portions © 2005, 2009 Microsoft Corporation。保留所有权利。*</span><span class="sxs-lookup"><span data-stu-id="70840-119">[Choosing Between Class and Struct](choosing-between-class-and-struct.md) [Abstract Class Design](abstract-class.md) [Static Class Design](static-class.md) [Interface Design](interface.md) [Struct Design](struct.md) [Enum Design](enum.md) [Nested Types](nested-types.md) *Portions © 2005, 2009 Microsoft Corporation. All rights reserved.*</span></span>

 <span data-ttu-id="70840-120">在 Pearson Education, Inc. 授权下，由 Addison-Wesley Professional 作为 Microsoft Windows 开发系列的一部分再版自 [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619)（Framework 设计准则：可重用 .NET 库的约定、惯例和模式第 2 版），由 Krzysztof Cwalina 和 Brad Abrams 发布于 2008 年 10 月 22 日。</span><span class="sxs-lookup"><span data-stu-id="70840-120">*Reprinted by permission of Pearson Education, Inc. from [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) by Krzysztof Cwalina and Brad Abrams, published Oct 22, 2008 by Addison-Wesley Professional as part of the Microsoft Windows Development Series.*</span></span>

## <a name="see-also"></a><span data-ttu-id="70840-121">请参阅</span><span class="sxs-lookup"><span data-stu-id="70840-121">See also</span></span>

- [<span data-ttu-id="70840-122">框架设计指南</span><span class="sxs-lookup"><span data-stu-id="70840-122">Framework Design Guidelines</span></span>](index.md)
