---
description: 详细了解：接口设计
title: 接口设计
ms.date: 10/22/2008
helpviewer_keywords:
- interfaces [.NET Framework], design guidelines
- type design guidelines, interfaces
- class library design guidelines [.NET Framework], interfaces
ms.assetid: a016bd18-6710-4358-9438-9f190a295392
ms.openlocfilehash: 387f921f8bdbe6c6d398aa31dcc8a22c7da455f7
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99641975"
---
# <a name="interface-design"></a><span data-ttu-id="feb9c-103">接口设计</span><span class="sxs-lookup"><span data-stu-id="feb9c-103">Interface Design</span></span>

<span data-ttu-id="feb9c-104">虽然大多数 API 最好使用类和结构进行建模，但是在某些情况下，接口更合适或者是唯一的选择。</span><span class="sxs-lookup"><span data-stu-id="feb9c-104">Although most APIs are best modeled using classes and structs, there are cases in which interfaces are more appropriate or are the only option.</span></span>

 <span data-ttu-id="feb9c-105">CLR 不支持多重继承（例如，CLR 类不能从多个基类继承），但它允许类型实现一个或多个接口以及从基类继承。</span><span class="sxs-lookup"><span data-stu-id="feb9c-105">The CLR does not support multiple inheritance (i.e., CLR classes cannot inherit from more than one base class), but it does allow types to implement one or more interfaces in addition to inheriting from a base class.</span></span> <span data-ttu-id="feb9c-106">因此，接口常用于实现多重继承的效果。</span><span class="sxs-lookup"><span data-stu-id="feb9c-106">Therefore, interfaces are often used to achieve the effect of multiple inheritance.</span></span> <span data-ttu-id="feb9c-107">例如，<xref:System.IDisposable> 是一个接口，该接口允许类型独立于它们要参与的任何其他继承层次结构来支持可处置性。</span><span class="sxs-lookup"><span data-stu-id="feb9c-107">For example, <xref:System.IDisposable> is an interface that allows types to support disposability independent of any other inheritance hierarchy in which they want to participate.</span></span>

 <span data-ttu-id="feb9c-108">适合定义接口的另一种情况是创建可由多种类型（包括某些值类型）支持的通用接口。</span><span class="sxs-lookup"><span data-stu-id="feb9c-108">The other situation in which defining an interface is appropriate is in creating a common interface that can be supported by several types, including some value types.</span></span> <span data-ttu-id="feb9c-109">值类型不能从 <xref:System.ValueType> 以外的类型继承，但它们可以实现接口，因此，使用接口是提供通用基类型的唯一选择。</span><span class="sxs-lookup"><span data-stu-id="feb9c-109">Value types cannot inherit from types other than <xref:System.ValueType>, but they can implement interfaces, so using an interface is the only option in order to provide a common base type.</span></span>

 <span data-ttu-id="feb9c-110">✔️ 如果你需要使一些通用 API 可由包含值类型的类型集支持，请务必定义一个接口。</span><span class="sxs-lookup"><span data-stu-id="feb9c-110">✔️ DO define an interface if you need some common API to be supported by a set of types that includes value types.</span></span>

 <span data-ttu-id="feb9c-111">✔️ 如果你需要针对已从其他类型继承的类型支持一个接口的功能，请考虑定义该接口。</span><span class="sxs-lookup"><span data-stu-id="feb9c-111">✔️ CONSIDER defining an interface if you need to support its functionality on types that already inherit from some other type.</span></span>

 <span data-ttu-id="feb9c-112">❌ 请避免使用标记接口（没有成员的接口）。</span><span class="sxs-lookup"><span data-stu-id="feb9c-112">❌ AVOID using marker interfaces (interfaces with no members).</span></span>

 <span data-ttu-id="feb9c-113">如果你需要将一个类标记为具有特定的特征（标记），则通常使用自定义特性而不是接口。</span><span class="sxs-lookup"><span data-stu-id="feb9c-113">If you need to mark a class as having a specific characteristic (marker), in general, use a custom attribute rather than an interface.</span></span>

 <span data-ttu-id="feb9c-114">✔️ 请务必提供至少一种作为接口的实现的类型。</span><span class="sxs-lookup"><span data-stu-id="feb9c-114">✔️ DO provide at least one type that is an implementation of an interface.</span></span>

 <span data-ttu-id="feb9c-115">这样做有助于验证接口的设计。</span><span class="sxs-lookup"><span data-stu-id="feb9c-115">Doing this helps to validate the design of the interface.</span></span> <span data-ttu-id="feb9c-116">例如，<xref:System.Collections.Generic.List%601> 是 <xref:System.Collections.Generic.IList%601> 接口的一个实现。</span><span class="sxs-lookup"><span data-stu-id="feb9c-116">For example, <xref:System.Collections.Generic.List%601> is an implementation of the <xref:System.Collections.Generic.IList%601> interface.</span></span>

 <span data-ttu-id="feb9c-117">✔️ 请务必提供至少一个使用你定义的每个接口的 API（将接口用作参数的方法或类型化为接口的属性）。</span><span class="sxs-lookup"><span data-stu-id="feb9c-117">✔️ DO provide at least one API that consumes each interface you define (a method taking the interface as a parameter or a property typed as the interface).</span></span>

 <span data-ttu-id="feb9c-118">这样做有助于验证接口设计。</span><span class="sxs-lookup"><span data-stu-id="feb9c-118">Doing this helps to validate the interface design.</span></span> <span data-ttu-id="feb9c-119">例如，<xref:System.Collections.Generic.List%601.Sort%2A?displayProperty=nameWithType> 使用 <xref:System.Collections.Generic.IComparer%601?displayProperty=nameWithType> 接口。</span><span class="sxs-lookup"><span data-stu-id="feb9c-119">For example, <xref:System.Collections.Generic.List%601.Sort%2A?displayProperty=nameWithType> consumes the <xref:System.Collections.Generic.IComparer%601?displayProperty=nameWithType> interface.</span></span>

 <span data-ttu-id="feb9c-120">❌ 请勿将成员添加到之前已提供的接口。</span><span class="sxs-lookup"><span data-stu-id="feb9c-120">❌ DO NOT add members to an interface that has previously shipped.</span></span>

 <span data-ttu-id="feb9c-121">这样做会破坏接口的实现。</span><span class="sxs-lookup"><span data-stu-id="feb9c-121">Doing so would break implementations of the interface.</span></span> <span data-ttu-id="feb9c-122">你应该创建新的接口，以避免版本控制问题。</span><span class="sxs-lookup"><span data-stu-id="feb9c-122">You should create a new interface in order to avoid versioning problems.</span></span>

 <span data-ttu-id="feb9c-123">除了这些准则中所述的情况外，在设计托管代码可重用库时，通常应该选择类而不是接口。</span><span class="sxs-lookup"><span data-stu-id="feb9c-123">Except for the situations described in these guidelines, you should, in general, choose classes rather than interfaces in designing managed code reusable libraries.</span></span>

 <span data-ttu-id="feb9c-124">*Portions © 2005, 2009 Microsoft Corporation 版权所有。保留所有权利。*</span><span class="sxs-lookup"><span data-stu-id="feb9c-124">*Portions © 2005, 2009 Microsoft Corporation. All rights reserved.*</span></span>

 <span data-ttu-id="feb9c-125">在 Pearson Education, Inc. 授权下，由 Addison-Wesley Professional 作为 Microsoft Windows 开发系列的一部分再版自 [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619)（Framework 设计准则：可重用 .NET 库的约定、惯例和模式第 2 版），由 Krzysztof Cwalina 和 Brad Abrams 发布于 2008 年 10 月 22 日。</span><span class="sxs-lookup"><span data-stu-id="feb9c-125">*Reprinted by permission of Pearson Education, Inc. from [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) by Krzysztof Cwalina and Brad Abrams, published Oct 22, 2008 by Addison-Wesley Professional as part of the Microsoft Windows Development Series.*</span></span>

## <a name="see-also"></a><span data-ttu-id="feb9c-126">请参阅</span><span class="sxs-lookup"><span data-stu-id="feb9c-126">See also</span></span>

- [<span data-ttu-id="feb9c-127">类型设计准则</span><span class="sxs-lookup"><span data-stu-id="feb9c-127">Type Design Guidelines</span></span>](type.md)
- [<span data-ttu-id="feb9c-128">框架设计指南</span><span class="sxs-lookup"><span data-stu-id="feb9c-128">Framework Design Guidelines</span></span>](index.md)
