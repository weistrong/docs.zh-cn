---
description: 详细了解：嵌套类型
title: 嵌套类型
ms.date: 10/22/2008
helpviewer_keywords:
- types, nested
- public nested types
- type design guidelines, nested types
- nested types
- members [.NET Framework], type
- class library design guidelines [.NET Framework], nested types
ms.assetid: 12feb7f0-b793-4d96-b090-42d6473bab8c
ms.openlocfilehash: 07d81827d67e50351f442ec15ca6cb18a63160fe
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99713372"
---
# <a name="nested-types"></a><span data-ttu-id="7a2b8-103">嵌套类型</span><span class="sxs-lookup"><span data-stu-id="7a2b8-103">Nested Types</span></span>

<span data-ttu-id="7a2b8-104">嵌套类型是在另一种类型（称为封闭类型）的范围内定义的类型。</span><span class="sxs-lookup"><span data-stu-id="7a2b8-104">A nested type is a type defined within the scope of another type, which is called the enclosing type.</span></span> <span data-ttu-id="7a2b8-105">嵌套类型可访问其封闭类型的所有成员。</span><span class="sxs-lookup"><span data-stu-id="7a2b8-105">A nested type has access to all members of its enclosing type.</span></span> <span data-ttu-id="7a2b8-106">例如，它可以访问在封闭类型中定义的专用字段，还可以访问在封闭类型的所有祖先类型中定义的受保护字段。</span><span class="sxs-lookup"><span data-stu-id="7a2b8-106">For example, it has access to private fields defined in the enclosing type and to protected fields defined in all ascendants of the enclosing type.</span></span>

 <span data-ttu-id="7a2b8-107">一般而言，应慎用嵌套类型。</span><span class="sxs-lookup"><span data-stu-id="7a2b8-107">In general, nested types should be used sparingly.</span></span> <span data-ttu-id="7a2b8-108">其原因有若干：</span><span class="sxs-lookup"><span data-stu-id="7a2b8-108">There are several reasons for this.</span></span> <span data-ttu-id="7a2b8-109">有些开发人员并不完全熟悉概念。</span><span class="sxs-lookup"><span data-stu-id="7a2b8-109">Some developers are not fully familiar with the concept.</span></span> <span data-ttu-id="7a2b8-110">例如，这些开发人员可能在声明嵌套类型的变量的语法方面遇到了问题。</span><span class="sxs-lookup"><span data-stu-id="7a2b8-110">These developers might, for example, have problems with the syntax of declaring variables of nested types.</span></span> <span data-ttu-id="7a2b8-111">嵌套类型也与其封闭类型紧密耦合，因此嵌套类型不适合用作通用类型。</span><span class="sxs-lookup"><span data-stu-id="7a2b8-111">Nested types are also very tightly coupled with their enclosing types, and as such are not suited to be general-purpose types.</span></span>

 <span data-ttu-id="7a2b8-112">嵌套类型最适合对其封闭类型的实现详细信息进行建模。</span><span class="sxs-lookup"><span data-stu-id="7a2b8-112">Nested types are best suited for modeling implementation details of their enclosing types.</span></span> <span data-ttu-id="7a2b8-113">最终用户应该很少需要声明嵌套类型的变量，也几乎永远不需要显式实例化嵌套类型。</span><span class="sxs-lookup"><span data-stu-id="7a2b8-113">The end user should rarely have to declare variables of a nested type and almost never should have to explicitly instantiate nested types.</span></span> <span data-ttu-id="7a2b8-114">例如，集合的枚举器可以是该集合的嵌套类型。</span><span class="sxs-lookup"><span data-stu-id="7a2b8-114">For example, the enumerator of a collection can be a nested type of that collection.</span></span> <span data-ttu-id="7a2b8-115">枚举器通常通过其封闭类型进行实例化，由于许多语言支持 foreach 语句，因此枚举器变量很少需要由最终用户声明。</span><span class="sxs-lookup"><span data-stu-id="7a2b8-115">Enumerators are usually instantiated by their enclosing type, and because many languages support the foreach statement, enumerator variables rarely have to be declared by the end user.</span></span>

 <span data-ttu-id="7a2b8-116">✔️ 当嵌套类型和其外部类型之间的 关系使得成员可访问性语义可取时，请务必使用嵌套类型。</span><span class="sxs-lookup"><span data-stu-id="7a2b8-116">✔️ DO use nested types when the relationship between the nested type and its outer type is such that member-accessibility semantics are desirable.</span></span>

 <span data-ttu-id="7a2b8-117">❌ 请勿使用公共嵌套类型作为逻辑分组构造；对此使用命名空间。</span><span class="sxs-lookup"><span data-stu-id="7a2b8-117">❌ DO NOT use public nested types as a logical grouping construct; use namespaces for this.</span></span>

 <span data-ttu-id="7a2b8-118">❌ 请避免使用公开暴露的嵌套类型。</span><span class="sxs-lookup"><span data-stu-id="7a2b8-118">❌ AVOID publicly exposed nested types.</span></span> <span data-ttu-id="7a2b8-119">对此，唯一的例外情况是：只需在很少的情况（如子类化或其他高级自定义场景）下声明嵌套类型的变量时。</span><span class="sxs-lookup"><span data-stu-id="7a2b8-119">The only exception to this is if variables of the nested type need to be declared only in rare scenarios such as subclassing or other advanced customization scenarios.</span></span>

 <span data-ttu-id="7a2b8-120">❌ 如果嵌套类型可能在包含类型之外被引用，则请勿使用该类型。</span><span class="sxs-lookup"><span data-stu-id="7a2b8-120">❌ DO NOT use nested types if the type is likely to be referenced outside of the containing type.</span></span>

 <span data-ttu-id="7a2b8-121">例如，一个传递给在类上定义的方法的枚举不应被定义为类中的嵌套类型。</span><span class="sxs-lookup"><span data-stu-id="7a2b8-121">For example, an enum passed to a method defined on a class should not be defined as a nested type in the class.</span></span>

 <span data-ttu-id="7a2b8-122">❌ 如果嵌套类型需要通过客户端代码进行实例化，则请勿使用该类型。</span><span class="sxs-lookup"><span data-stu-id="7a2b8-122">❌ DO NOT use nested types if they need to be instantiated by client code.</span></span>  <span data-ttu-id="7a2b8-123">如果某个类型具有公共构造函数，则它可能不应被嵌套。</span><span class="sxs-lookup"><span data-stu-id="7a2b8-123">If a type has a public constructor, it should probably not be nested.</span></span>

 <span data-ttu-id="7a2b8-124">如果某个类型可以被实例化，这似乎表明该类型在框架中有自己的位置（你可以创建它，使用它并销毁它，而不必使用外部类型），因此该类型不应被嵌套。</span><span class="sxs-lookup"><span data-stu-id="7a2b8-124">If a type can be instantiated, that seems to indicate the type has a place in the framework on its own (you can create it, work with it, and destroy it without ever using the outer type), and thus should not be nested.</span></span> <span data-ttu-id="7a2b8-125">如果内部类型与外部类型没有任何关系，则不应在外部类型之外广泛重用内部类型。</span><span class="sxs-lookup"><span data-stu-id="7a2b8-125">Inner types should not be widely reused outside of the outer type without any relationship whatsoever to the outer type.</span></span>

 <span data-ttu-id="7a2b8-126">❌ 请勿将嵌套类型定义为接口的成员。</span><span class="sxs-lookup"><span data-stu-id="7a2b8-126">❌ DO NOT define a nested type as a member of an interface.</span></span> <span data-ttu-id="7a2b8-127">许多语言不支持此类构造。</span><span class="sxs-lookup"><span data-stu-id="7a2b8-127">Many languages do not support such a construct.</span></span>

 <span data-ttu-id="7a2b8-128">*Portions © 2005, 2009 Microsoft Corporation 版权所有。保留所有权利。*</span><span class="sxs-lookup"><span data-stu-id="7a2b8-128">*Portions © 2005, 2009 Microsoft Corporation. All rights reserved.*</span></span>

 <span data-ttu-id="7a2b8-129">在 Pearson Education, Inc. 授权下，由 Addison-Wesley Professional 作为 Microsoft Windows 开发系列的一部分再版自 [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619)（Framework 设计准则：可重用 .NET 库的约定、惯例和模式第 2 版），由 Krzysztof Cwalina 和 Brad Abrams 发布于 2008 年 10 月 22 日。</span><span class="sxs-lookup"><span data-stu-id="7a2b8-129">*Reprinted by permission of Pearson Education, Inc. from [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) by Krzysztof Cwalina and Brad Abrams, published Oct 22, 2008 by Addison-Wesley Professional as part of the Microsoft Windows Development Series.*</span></span>

## <a name="see-also"></a><span data-ttu-id="7a2b8-130">请参阅</span><span class="sxs-lookup"><span data-stu-id="7a2b8-130">See also</span></span>

- [<span data-ttu-id="7a2b8-131">类型设计准则</span><span class="sxs-lookup"><span data-stu-id="7a2b8-131">Type Design Guidelines</span></span>](type.md)
- [<span data-ttu-id="7a2b8-132">框架设计指南</span><span class="sxs-lookup"><span data-stu-id="7a2b8-132">Framework Design Guidelines</span></span>](index.md)
