---
description: 详细了解：相等运算符
title: 相等运算符
ms.date: 10/22/2008
helpviewer_keywords:
- class library design guidelines [.NET Framework], Equals method
- class library design guidelines [.NET Framework], equality operator
- equality operator (==) [.NET Framework]
- Equals method
- == operator (equality) [.NET Framework]
ms.assetid: bc496a91-fefb-4ce0-ab4c-61f09964119a
ms.openlocfilehash: 8678ed1b4bc320f685cf7ae172f064b3dededd04
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99642235"
---
# <a name="equality-operators"></a><span data-ttu-id="220f1-103">相等运算符</span><span class="sxs-lookup"><span data-stu-id="220f1-103">Equality Operators</span></span>

<span data-ttu-id="220f1-104">本部分讨论重载相等运算符，并将 `operator==` 和 `operator!=` 视为相等运算符。</span><span class="sxs-lookup"><span data-stu-id="220f1-104">This section discusses overloading equality operators and refers to `operator==` and `operator!=` as equality operators.</span></span>

 <span data-ttu-id="220f1-105">❌ 请勿重载其中一个相等运算符而不重载另一个。</span><span class="sxs-lookup"><span data-stu-id="220f1-105">❌ DO NOT overload one of the equality operators and not the other.</span></span>

 <span data-ttu-id="220f1-106">✔️ 请务必确保 <xref:System.Object.Equals%2A?displayProperty=nameWithType> 和相等运算符具有完全相同的语义和相似的性能特征。</span><span class="sxs-lookup"><span data-stu-id="220f1-106">✔️ DO ensure that <xref:System.Object.Equals%2A?displayProperty=nameWithType> and the equality operators have exactly the same semantics and similar performance characteristics.</span></span>

 <span data-ttu-id="220f1-107">这通常意味着在重载相等运算符时，需要重写 `Object.Equals`。</span><span class="sxs-lookup"><span data-stu-id="220f1-107">This often means that `Object.Equals` needs to be overridden when the equality operators are overloaded.</span></span>

 <span data-ttu-id="220f1-108">❌ 请避免从相等运算符引发异常。</span><span class="sxs-lookup"><span data-stu-id="220f1-108">❌ AVOID throwing exceptions from equality operators.</span></span>

 <span data-ttu-id="220f1-109">例如，如果其中一个参数为 null，则返回 false，而不是引发 `NullReferenceException`。</span><span class="sxs-lookup"><span data-stu-id="220f1-109">For example, return false if one of the arguments is null instead of throwing `NullReferenceException`.</span></span>

## <a name="equality-operators-on-value-types"></a><span data-ttu-id="220f1-110">针对值类型的相等运算符</span><span class="sxs-lookup"><span data-stu-id="220f1-110">Equality Operators on Value Types</span></span>

 <span data-ttu-id="220f1-111">✔️ 如果相等性是有意义的，请务必对值类型重载相等运算符。</span><span class="sxs-lookup"><span data-stu-id="220f1-111">✔️ DO overload the equality operators on value types, if equality is meaningful.</span></span>

 <span data-ttu-id="220f1-112">在大多数编程语言中，值类型没有默认的 `operator==` 实现。</span><span class="sxs-lookup"><span data-stu-id="220f1-112">In most programming languages, there is no default implementation of `operator==` for value types.</span></span>

## <a name="equality-operators-on-reference-types"></a><span data-ttu-id="220f1-113">针对引用类型的相等运算符</span><span class="sxs-lookup"><span data-stu-id="220f1-113">Equality Operators on Reference Types</span></span>

 <span data-ttu-id="220f1-114">❌ 请避免对可变引用类型重载相等运算符。</span><span class="sxs-lookup"><span data-stu-id="220f1-114">❌ AVOID overloading equality operators on mutable reference types.</span></span>

 <span data-ttu-id="220f1-115">许多语言都具有用于引用类型的内置相等运算符。</span><span class="sxs-lookup"><span data-stu-id="220f1-115">Many languages have built-in equality operators for reference types.</span></span> <span data-ttu-id="220f1-116">内置运算符通常实现引用相等性，当默认行为更改为值相等性时，很多开发人员都感到很惊讶。</span><span class="sxs-lookup"><span data-stu-id="220f1-116">The built-in operators usually implement the reference equality, and many developers are surprised when the default behavior is changed to the value equality.</span></span>

 <span data-ttu-id="220f1-117">对于不可变的引用类型，此问题得到了缓解，因为不可变性使发现引用相等性和值相等性之间的差异变得更加困难。</span><span class="sxs-lookup"><span data-stu-id="220f1-117">This problem is mitigated for immutable reference types because immutability makes it much harder to notice the difference between reference equality and value equality.</span></span>

 <span data-ttu-id="220f1-118">❌ 请避免对引用类型重载相等运算符（如果实现的速度远远低于引用相等性的实现速度）。</span><span class="sxs-lookup"><span data-stu-id="220f1-118">❌ AVOID overloading equality operators on reference types if the implementation would be significantly slower than that of reference equality.</span></span>

 <span data-ttu-id="220f1-119">*Portions © 2005, 2009 Microsoft Corporation 版权所有。保留所有权利。*</span><span class="sxs-lookup"><span data-stu-id="220f1-119">*Portions © 2005, 2009 Microsoft Corporation. All rights reserved.*</span></span>

 <span data-ttu-id="220f1-120">在 Pearson Education, Inc. 授权下，由 Addison-Wesley Professional 作为 Microsoft Windows 开发系列的一部分再版自 [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619)（Framework 设计准则：可重用 .NET 库的约定、惯例和模式第 2 版），由 Krzysztof Cwalina 和 Brad Abrams 发布于 2008 年 10 月 22 日。</span><span class="sxs-lookup"><span data-stu-id="220f1-120">*Reprinted by permission of Pearson Education, Inc. from [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) by Krzysztof Cwalina and Brad Abrams, published Oct 22, 2008 by Addison-Wesley Professional as part of the Microsoft Windows Development Series.*</span></span>

## <a name="see-also"></a><span data-ttu-id="220f1-121">请参阅</span><span class="sxs-lookup"><span data-stu-id="220f1-121">See also</span></span>

- [<span data-ttu-id="220f1-122">框架设计指南</span><span class="sxs-lookup"><span data-stu-id="220f1-122">Framework Design Guidelines</span></span>](index.md)
- [<span data-ttu-id="220f1-123">使用准则</span><span class="sxs-lookup"><span data-stu-id="220f1-123">Usage Guidelines</span></span>](usage-guidelines.md)
