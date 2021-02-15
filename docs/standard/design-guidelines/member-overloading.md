---
description: 详细了解：成员重载
title: 成员重载
ms.date: 10/22/2008
helpviewer_keywords:
- default arguments
- members [.NET Framework], overloaded
- member design guidelines [.NET Framework], overloading
- overloaded members
- signatures, members
ms.assetid: 964ba19e-8b94-4b5b-b1e3-5a0b531a0bb1
ms.openlocfilehash: d3a545bfec552686e55c9f713d58784497946819
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99641949"
---
# <a name="member-overloading"></a><span data-ttu-id="11b27-103">成员重载</span><span class="sxs-lookup"><span data-stu-id="11b27-103">Member Overloading</span></span>

<span data-ttu-id="11b27-104">成员重载意味着针对同一类型创建两个或多个成员，这些成员仅在参数的数量或类型上不同，但具有相同的名称。</span><span class="sxs-lookup"><span data-stu-id="11b27-104">Member overloading means creating two or more members on the same type that differ only in the number or type of parameters but have the same name.</span></span> <span data-ttu-id="11b27-105">例如，在以下示例中，重载了 `WriteLine` 方法：</span><span class="sxs-lookup"><span data-stu-id="11b27-105">For example, in the following, the `WriteLine` method is overloaded:</span></span>

```csharp
public static class Console {
    public void WriteLine();
    public void WriteLine(string value);
    public void WriteLine(bool value);
    ...
}
```

 <span data-ttu-id="11b27-106">由于只有方法、构造函数和索引属性可以有参数，因此只能重载这些成员。</span><span class="sxs-lookup"><span data-stu-id="11b27-106">Because only methods, constructors, and indexed properties can have parameters, only those members can be overloaded.</span></span>

 <span data-ttu-id="11b27-107">重载是提高可重用库的可用性、生产力和可读性的最重要方法之一。</span><span class="sxs-lookup"><span data-stu-id="11b27-107">Overloading is one of the most important techniques for improving usability, productivity, and readability of reusable libraries.</span></span> <span data-ttu-id="11b27-108">通过对参数数量进行重载，可提供更简单的构造函数和方法版本。</span><span class="sxs-lookup"><span data-stu-id="11b27-108">Overloading on the number of parameters makes it possible to provide simpler versions of constructors and methods.</span></span> <span data-ttu-id="11b27-109">通过对参数类型进行重载，可为那些针对不同类型的选定集执行相同操作的成员使用相同的成员名称。</span><span class="sxs-lookup"><span data-stu-id="11b27-109">Overloading on the parameter type makes it possible to use the same member name for members performing identical operations on a selected set of different types.</span></span>

 <span data-ttu-id="11b27-110">✔️ 请务必尝试使用描述性参数名称来指示较短重载使用的默认值。</span><span class="sxs-lookup"><span data-stu-id="11b27-110">✔️ DO try to use descriptive parameter names to indicate the default used by shorter overloads.</span></span>

 <span data-ttu-id="11b27-111">❌ 请避免在重载中随意改变参数名称。</span><span class="sxs-lookup"><span data-stu-id="11b27-111">❌ AVOID arbitrarily varying parameter names in overloads.</span></span> <span data-ttu-id="11b27-112">如果一个重载中的参数与另一个重载中的参数表示相同的输入，则这些参数应该具有相同的名称。</span><span class="sxs-lookup"><span data-stu-id="11b27-112">If a parameter in one overload represents the same input as a parameter in another overload, the parameters should have the same name.</span></span>

 <span data-ttu-id="11b27-113">❌ 请避免重载的成员中参数的顺序不一致。</span><span class="sxs-lookup"><span data-stu-id="11b27-113">❌ AVOID being inconsistent in the ordering of parameters in overloaded members.</span></span> <span data-ttu-id="11b27-114">在所有重载中，具有相同名称的参数应出现在相同的位置。</span><span class="sxs-lookup"><span data-stu-id="11b27-114">Parameters with the same name should appear in the same position in all overloads.</span></span>

 <span data-ttu-id="11b27-115">✔️ 请确保仅使最长的重载虚拟化（如果需要扩展性）。</span><span class="sxs-lookup"><span data-stu-id="11b27-115">✔️ DO make only the longest overload virtual (if extensibility is required).</span></span> <span data-ttu-id="11b27-116">较短的重载应直接调用较长的重载。</span><span class="sxs-lookup"><span data-stu-id="11b27-116">Shorter overloads should simply call through to a longer overload.</span></span>

 <span data-ttu-id="11b27-117">❌ 请勿使用 `ref` 或 `out` 修饰符来重载成员。</span><span class="sxs-lookup"><span data-stu-id="11b27-117">❌ DO NOT use `ref` or `out` modifiers to overload members.</span></span>

 <span data-ttu-id="11b27-118">某些语言无法像这样解析对重载的调用。</span><span class="sxs-lookup"><span data-stu-id="11b27-118">Some languages cannot resolve calls to overloads like this.</span></span> <span data-ttu-id="11b27-119">此外，此类重载通常具有完全不同的语义，可能不应该是重载，而应该是两种单独的方法。</span><span class="sxs-lookup"><span data-stu-id="11b27-119">In addition, such overloads usually have completely different semantics and probably should not be overloads but two separate methods instead.</span></span>

 <span data-ttu-id="11b27-120">❌ 请勿包含参数位于相同位置且类型相似但语义不同的重载。</span><span class="sxs-lookup"><span data-stu-id="11b27-120">❌ DO NOT have overloads with parameters at the same position and similar types yet with different semantics.</span></span>

 <span data-ttu-id="11b27-121">✔️ 请务必允许为可选参数传递 `null`。</span><span class="sxs-lookup"><span data-stu-id="11b27-121">✔️ DO  allow `null` to be passed for optional arguments.</span></span>

 <span data-ttu-id="11b27-122">✔️ 请务必使用成员重载，而不是使用默认参数定义成员。</span><span class="sxs-lookup"><span data-stu-id="11b27-122">✔️ DO use member overloading rather than defining members with default arguments.</span></span>

 <span data-ttu-id="11b27-123">默认参数不符合 CLS。</span><span class="sxs-lookup"><span data-stu-id="11b27-123">Default arguments are not CLS compliant.</span></span>

 <span data-ttu-id="11b27-124">*Portions © 2005, 2009 Microsoft Corporation 版权所有。保留所有权利。*</span><span class="sxs-lookup"><span data-stu-id="11b27-124">*Portions © 2005, 2009 Microsoft Corporation. All rights reserved.*</span></span>

 <span data-ttu-id="11b27-125">在 Pearson Education, Inc. 授权下，由 Addison-Wesley Professional 作为 Microsoft Windows 开发系列的一部分再版自 [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619)（Framework 设计准则：可重用 .NET 库的约定、惯例和模式第 2 版），由 Krzysztof Cwalina 和 Brad Abrams 发布于 2008 年 10 月 22 日。</span><span class="sxs-lookup"><span data-stu-id="11b27-125">*Reprinted by permission of Pearson Education, Inc. from [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) by Krzysztof Cwalina and Brad Abrams, published Oct 22, 2008 by Addison-Wesley Professional as part of the Microsoft Windows Development Series.*</span></span>

## <a name="see-also"></a><span data-ttu-id="11b27-126">请参阅</span><span class="sxs-lookup"><span data-stu-id="11b27-126">See also</span></span>

- [<span data-ttu-id="11b27-127">成员设计准则</span><span class="sxs-lookup"><span data-stu-id="11b27-127">Member Design Guidelines</span></span>](member.md)
- [<span data-ttu-id="11b27-128">框架设计指南</span><span class="sxs-lookup"><span data-stu-id="11b27-128">Framework Design Guidelines</span></span>](index.md)
