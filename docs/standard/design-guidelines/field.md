---
description: 详细了解：字段设计
title: 字段设计
ms.date: 10/22/2008
helpviewer_keywords:
- fields, design guidelines
- read-only fields
- member design guidelines, fields
ms.assetid: 7cb4b0f3-7a10-4c93-b84d-733f7134fcf8
ms.openlocfilehash: 88df60c3050035221dc65429bbd543c71d5d69b3
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99642040"
---
# <a name="field-design"></a><span data-ttu-id="0a3b0-103">字段设计</span><span class="sxs-lookup"><span data-stu-id="0a3b0-103">Field Design</span></span>

<span data-ttu-id="0a3b0-104">封装原则是面向对象的设计中最重要的概念之一。</span><span class="sxs-lookup"><span data-stu-id="0a3b0-104">The principle of encapsulation is one of the most important notions in object-oriented design.</span></span> <span data-ttu-id="0a3b0-105">此原则表明，存储在一个对象中的数据应只能由该对象访问。</span><span class="sxs-lookup"><span data-stu-id="0a3b0-105">This principle states that data stored inside an object should be accessible only to that object.</span></span>

 <span data-ttu-id="0a3b0-106">解释该原则的一个有效的方法是：应该设计一个类型，以便可以在不破坏代码的情况下对该类型的字段进行更改（名称或类型更改），而不是对该类型的成员进行更改。</span><span class="sxs-lookup"><span data-stu-id="0a3b0-106">A useful way to interpret the principle is to say that a type should be designed so that changes to fields of that type (name or type changes) can be made without breaking code other than for members of the type.</span></span> <span data-ttu-id="0a3b0-107">此解释直接暗示了所有字段都必须是专用的。</span><span class="sxs-lookup"><span data-stu-id="0a3b0-107">This interpretation immediately implies that all fields must be private.</span></span>

 <span data-ttu-id="0a3b0-108">我们将常量和静态只读字段排除在这一严格限制之外，因为几乎从定义上来说，此类字段从来不需要更改。</span><span class="sxs-lookup"><span data-stu-id="0a3b0-108">We exclude constant and static read-only fields from this strict restriction, because such fields, almost by definition, are never required to change.</span></span>

 <span data-ttu-id="0a3b0-109">❌ 请勿提供公共的或受保护的实例字段。</span><span class="sxs-lookup"><span data-stu-id="0a3b0-109">❌ DO NOT provide instance fields that are public or protected.</span></span>

 <span data-ttu-id="0a3b0-110">应提供用于访问字段的属性，而不是将其设为公共或受保护。</span><span class="sxs-lookup"><span data-stu-id="0a3b0-110">You should provide properties for accessing fields instead of making them public or protected.</span></span>

 <span data-ttu-id="0a3b0-111">✔️ 请务必对永远不会更改的常量使用常量字段。</span><span class="sxs-lookup"><span data-stu-id="0a3b0-111">✔️ DO use constant fields for constants that will never change.</span></span>

 <span data-ttu-id="0a3b0-112">编译器会直接将常量字段的值直接刻录到调用代码中。</span><span class="sxs-lookup"><span data-stu-id="0a3b0-112">The compiler burns the values of const fields directly into calling code.</span></span> <span data-ttu-id="0a3b0-113">因此，如果没有破坏兼容性的风险，常量值永远不会更改。</span><span class="sxs-lookup"><span data-stu-id="0a3b0-113">Therefore, const values can never be changed without the risk of breaking compatibility.</span></span>

 <span data-ttu-id="0a3b0-114">✔️ 请务必对预定义的对象实例使用公共静态 `readonly` 字段。</span><span class="sxs-lookup"><span data-stu-id="0a3b0-114">✔️ DO use public static `readonly` fields for predefined object instances.</span></span>

 <span data-ttu-id="0a3b0-115">如果存在类型的预定义实例，请将它们声明为类型本身的公共只读静态字段。</span><span class="sxs-lookup"><span data-stu-id="0a3b0-115">If there are predefined instances of the type, declare them as public read-only static fields of the type itself.</span></span>

 <span data-ttu-id="0a3b0-116">❌ 请勿将可变类型的实例分配到 `readonly` 字段。</span><span class="sxs-lookup"><span data-stu-id="0a3b0-116">❌ DO NOT assign instances of mutable types to `readonly` fields.</span></span>

 <span data-ttu-id="0a3b0-117">可变类型是具有实例的类型，这些实例可在实例化后进行修改。</span><span class="sxs-lookup"><span data-stu-id="0a3b0-117">A mutable type is a type with instances that can be modified after they are instantiated.</span></span> <span data-ttu-id="0a3b0-118">例如，数组、大多数集合和流都是可变类型，但 <xref:System.Int32?displayProperty=nameWithType>、<xref:System.Uri?displayProperty=nameWithType> 和 <xref:System.String?displayProperty=nameWithType> 都是不可变的。</span><span class="sxs-lookup"><span data-stu-id="0a3b0-118">For example, arrays, most collections, and streams are mutable types, but <xref:System.Int32?displayProperty=nameWithType>, <xref:System.Uri?displayProperty=nameWithType>, and <xref:System.String?displayProperty=nameWithType> are all immutable.</span></span> <span data-ttu-id="0a3b0-119">引用类型字段的只读修饰符可防止替换存储在该字段中的实例，但不能防止通过调用更改实例的成员来修改字段的实例数据。</span><span class="sxs-lookup"><span data-stu-id="0a3b0-119">The read-only modifier on a reference type field prevents the instance stored in the field from being replaced, but it does not prevent the field’s instance data from being modified by calling members changing the instance.</span></span>

 <span data-ttu-id="0a3b0-120">*Portions © 2005, 2009 Microsoft Corporation 版权所有。保留所有权利。*</span><span class="sxs-lookup"><span data-stu-id="0a3b0-120">*Portions © 2005, 2009 Microsoft Corporation. All rights reserved.*</span></span>

 <span data-ttu-id="0a3b0-121">在 Pearson Education, Inc. 授权下，由 Addison-Wesley Professional 作为 Microsoft Windows 开发系列的一部分再版自 [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619)（Framework 设计准则：可重用 .NET 库的约定、惯例和模式第 2 版），由 Krzysztof Cwalina 和 Brad Abrams 发布于 2008 年 10 月 22 日。</span><span class="sxs-lookup"><span data-stu-id="0a3b0-121">*Reprinted by permission of Pearson Education, Inc. from [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) by Krzysztof Cwalina and Brad Abrams, published Oct 22, 2008 by Addison-Wesley Professional as part of the Microsoft Windows Development Series.*</span></span>

## <a name="see-also"></a><span data-ttu-id="0a3b0-122">请参阅</span><span class="sxs-lookup"><span data-stu-id="0a3b0-122">See also</span></span>

- [<span data-ttu-id="0a3b0-123">成员设计准则</span><span class="sxs-lookup"><span data-stu-id="0a3b0-123">Member Design Guidelines</span></span>](member.md)
- [<span data-ttu-id="0a3b0-124">框架设计指南</span><span class="sxs-lookup"><span data-stu-id="0a3b0-124">Framework Design Guidelines</span></span>](index.md)
