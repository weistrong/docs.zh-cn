---
description: 详细了解：结构设计
title: 结构设计
ms.date: 10/22/2008
helpviewer_keywords:
- class library design guidelines [.NET Framework], structures
- deallocating structures
- allocating structures
- value types, structures
- structure design
- type design guidelines, structures
- structures [.NET Framework], design guidelines
ms.assetid: 1f48b2d8-608c-4be6-9ba4-d8f203ed9f9f
ms.openlocfilehash: a28dd3e452d22e61d95ec521fdbde6539e38ed78
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99641897"
---
# <a name="struct-design"></a><span data-ttu-id="9d510-103">结构设计</span><span class="sxs-lookup"><span data-stu-id="9d510-103">Struct Design</span></span>

<span data-ttu-id="9d510-104">常规用途值类型最常被称为结构，即其 C# 关键字。</span><span class="sxs-lookup"><span data-stu-id="9d510-104">The general-purpose value type is most often referred to as a struct, its C# keyword.</span></span> <span data-ttu-id="9d510-105">本部分提供常规结构设计的准则。</span><span class="sxs-lookup"><span data-stu-id="9d510-105">This section provides guidelines for general struct design.</span></span>

 <span data-ttu-id="9d510-106">❌ 请勿为结构提供无参数构造函数。</span><span class="sxs-lookup"><span data-stu-id="9d510-106">❌ DO NOT provide a parameterless constructor for a struct.</span></span>

 <span data-ttu-id="9d510-107">若遵循此准则，便可创建结构数组，而不必对每个数组项运行该构造函数。</span><span class="sxs-lookup"><span data-stu-id="9d510-107">Following this guideline allows arrays of structs to be created without having to run the constructor on each item of the array.</span></span> <span data-ttu-id="9d510-108">请注意，C# 不允许结构具有无参数构造函数。</span><span class="sxs-lookup"><span data-stu-id="9d510-108">Notice that C# does not allow structs to have parameterless constructors.</span></span>

 <span data-ttu-id="9d510-109">❌ 请勿定义可变值类型。</span><span class="sxs-lookup"><span data-stu-id="9d510-109">❌ DO NOT define mutable value types.</span></span>

 <span data-ttu-id="9d510-110">可变值类型有几个问题。</span><span class="sxs-lookup"><span data-stu-id="9d510-110">Mutable value types have several problems.</span></span> <span data-ttu-id="9d510-111">例如，当属性 getter 返回值类型时，调用方会收到一个副本。</span><span class="sxs-lookup"><span data-stu-id="9d510-111">For example, when a property getter returns a value type, the caller receives a copy.</span></span> <span data-ttu-id="9d510-112">由于该副本是隐式创建的，因此开发人员可能不会意识到他们正在改变副本，而不是原始值。</span><span class="sxs-lookup"><span data-stu-id="9d510-112">Because the copy is created implicitly, developers might not be aware that they are mutating the copy, and not the original value.</span></span> <span data-ttu-id="9d510-113">此外，某些语言（尤其是动态语言）在使用可变值类型方面存在问题，因为即使是本地变量，在被取消引用后，也会导致生成一个副本。</span><span class="sxs-lookup"><span data-stu-id="9d510-113">Also, some languages (dynamic languages, in particular) have problems using mutable value types because even local variables, when dereferenced, cause a copy to be made.</span></span>

 <span data-ttu-id="9d510-114">✔️ 请务必确保将所有实例数据设置为零、false 或 null（视情况而定）的状态有效。</span><span class="sxs-lookup"><span data-stu-id="9d510-114">✔️ DO ensure that a state where all instance data is set to zero, false, or null (as appropriate) is valid.</span></span>

 <span data-ttu-id="9d510-115">这可防止在创建结构数组时意外创建无效的实例。</span><span class="sxs-lookup"><span data-stu-id="9d510-115">This prevents accidental creation of invalid instances when an array of the structs is created.</span></span>

 <span data-ttu-id="9d510-116">✔️ 请务必在值类型上实现 <xref:System.IEquatable%601>。</span><span class="sxs-lookup"><span data-stu-id="9d510-116">✔️ DO implement <xref:System.IEquatable%601> on value types.</span></span>

 <span data-ttu-id="9d510-117">值类型上的 <xref:System.Object.Equals%2A?displayProperty=nameWithType> 方法会导致装箱，且其默认实现效率不高，因为它使用反射。</span><span class="sxs-lookup"><span data-stu-id="9d510-117">The <xref:System.Object.Equals%2A?displayProperty=nameWithType> method on value types causes boxing, and its default implementation is not very efficient, because it uses reflection.</span></span> <span data-ttu-id="9d510-118"><xref:System.IEquatable%601.Equals%2A> 可具有更好的性能，并且可得到实施，这样就不会导致装箱。</span><span class="sxs-lookup"><span data-stu-id="9d510-118"><xref:System.IEquatable%601.Equals%2A> can have much better performance and can be implemented so that it will not cause boxing.</span></span>

 <span data-ttu-id="9d510-119">❌ 请勿显式扩展 <xref:System.ValueType>。</span><span class="sxs-lookup"><span data-stu-id="9d510-119">❌ DO NOT explicitly extend <xref:System.ValueType>.</span></span> <span data-ttu-id="9d510-120">事实上，大多数语言都禁止这样做。</span><span class="sxs-lookup"><span data-stu-id="9d510-120">In fact, most languages prevent this.</span></span>

 <span data-ttu-id="9d510-121">通常，结构可能非常有用，但只应用于不会频繁装箱的小型单个不可变值。</span><span class="sxs-lookup"><span data-stu-id="9d510-121">In general, structs can be very useful but should only be used for small, single, immutable values that will not be boxed frequently.</span></span>

 <span data-ttu-id="9d510-122">*Portions © 2005, 2009 Microsoft Corporation 版权所有。保留所有权利。*</span><span class="sxs-lookup"><span data-stu-id="9d510-122">*Portions © 2005, 2009 Microsoft Corporation. All rights reserved.*</span></span>

 <span data-ttu-id="9d510-123">在 Pearson Education, Inc. 授权下，由 Addison-Wesley Professional 作为 Microsoft Windows 开发系列的一部分再版自 [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619)（Framework 设计准则：可重用 .NET 库的约定、惯例和模式第 2 版），由 Krzysztof Cwalina 和 Brad Abrams 发布于 2008 年 10 月 22 日。</span><span class="sxs-lookup"><span data-stu-id="9d510-123">*Reprinted by permission of Pearson Education, Inc. from [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) by Krzysztof Cwalina and Brad Abrams, published Oct 22, 2008 by Addison-Wesley Professional as part of the Microsoft Windows Development Series.*</span></span>

## <a name="see-also"></a><span data-ttu-id="9d510-124">请参阅</span><span class="sxs-lookup"><span data-stu-id="9d510-124">See also</span></span>

- [<span data-ttu-id="9d510-125">类型设计准则</span><span class="sxs-lookup"><span data-stu-id="9d510-125">Type Design Guidelines</span></span>](type.md)
- [<span data-ttu-id="9d510-126">框架设计指南</span><span class="sxs-lookup"><span data-stu-id="9d510-126">Framework Design Guidelines</span></span>](index.md)
- [<span data-ttu-id="9d510-127">在类和结构之间选择</span><span class="sxs-lookup"><span data-stu-id="9d510-127">Choosing Between Class and Struct</span></span>](choosing-between-class-and-struct.md)
