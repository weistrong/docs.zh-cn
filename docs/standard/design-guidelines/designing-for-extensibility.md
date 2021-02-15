---
description: 详细了解：扩展性设计
title: 扩展性设计
ms.date: 10/22/2008
helpviewer_keywords:
- extending class libraries
- extensibility with class libraries in .NET Framework
- class library design guidelines [.NET Framework], extensibility
- class library extensibility [.NET Framework]
ms.assetid: 1cdb8740-871a-456c-9bd9-db96ca8d79b3
ms.openlocfilehash: 148ae25380698a5a1161fb9fbdd3cc60102e865d
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99642261"
---
# <a name="designing-for-extensibility"></a><span data-ttu-id="89a9a-103">扩展性设计</span><span class="sxs-lookup"><span data-stu-id="89a9a-103">Designing for Extensibility</span></span>

<span data-ttu-id="89a9a-104">设计框架的一个重要方面是确保框架的扩展性得到了仔细的考虑。</span><span class="sxs-lookup"><span data-stu-id="89a9a-104">One important aspect of designing a framework is making sure the extensibility of the framework has been carefully considered.</span></span> <span data-ttu-id="89a9a-105">这需要你了解与各种扩展性机制相关的成本和优势。</span><span class="sxs-lookup"><span data-stu-id="89a9a-105">This requires that you understand the costs and benefits associated with various extensibility mechanisms.</span></span> <span data-ttu-id="89a9a-106">本章可帮助你确定哪些扩展性机制（子类化、事件、虚拟成员、回调等）可最大程度地满足你的框架的要求。</span><span class="sxs-lookup"><span data-stu-id="89a9a-106">This chapter helps you decide which of the extensibility mechanisms—subclassing, events, virtual members, callbacks, and so on—can best meet the requirements of your framework.</span></span>  
  
 <span data-ttu-id="89a9a-107">可通过多种方式在框架中提供扩展性。</span><span class="sxs-lookup"><span data-stu-id="89a9a-107">There are many ways to allow extensibility in frameworks.</span></span> <span data-ttu-id="89a9a-108">它们从功能较弱但价格较低到功能强大但价格昂贵不等。</span><span class="sxs-lookup"><span data-stu-id="89a9a-108">They range from less powerful but less costly to very powerful but expensive.</span></span> <span data-ttu-id="89a9a-109">对于任何给定的扩展性要求，你应选择可满足要求的成本最低的扩展性机制。</span><span class="sxs-lookup"><span data-stu-id="89a9a-109">For any given extensibility requirement, you should choose the least costly extensibility mechanism that meets the requirements.</span></span> <span data-ttu-id="89a9a-110">请记住，通常可以在之后添加更多的扩展性，但是如果不引入中断性变更，你永远也无法删除它。</span><span class="sxs-lookup"><span data-stu-id="89a9a-110">Keep in mind that it’s usually possible to add more extensibility later, but you can never take it away without introducing breaking changes.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="89a9a-111">本节内容</span><span class="sxs-lookup"><span data-stu-id="89a9a-111">In This Section</span></span>  

 [<span data-ttu-id="89a9a-112">未密封类</span><span class="sxs-lookup"><span data-stu-id="89a9a-112">Unsealed Classes</span></span>](unsealed-classes.md)  
 [<span data-ttu-id="89a9a-113">受保护的成员</span><span class="sxs-lookup"><span data-stu-id="89a9a-113">Protected Members</span></span>](protected-members.md)  
 [<span data-ttu-id="89a9a-114">事件和回调</span><span class="sxs-lookup"><span data-stu-id="89a9a-114">Events and Callbacks</span></span>](events-and-callbacks.md)  
 [<span data-ttu-id="89a9a-115">虚拟成员</span><span class="sxs-lookup"><span data-stu-id="89a9a-115">Virtual Members</span></span>](virtual-members.md)  
 [<span data-ttu-id="89a9a-116">抽象（抽象类型和接口）</span><span class="sxs-lookup"><span data-stu-id="89a9a-116">Abstractions (Abstract Types and Interfaces)</span></span>](abstractions-abstract-types-and-interfaces.md)  
 [<span data-ttu-id="89a9a-117">用于实现抽象的基类</span><span class="sxs-lookup"><span data-stu-id="89a9a-117">Base Classes for Implementing Abstractions</span></span>](base-classes-for-implementing-abstractions.md)  
 [<span data-ttu-id="89a9a-118">密封</span><span class="sxs-lookup"><span data-stu-id="89a9a-118">Sealing</span></span>](sealing.md)  
 <span data-ttu-id="89a9a-119">*Portions © 2005, 2009 Microsoft Corporation 版权所有。保留所有权利。*</span><span class="sxs-lookup"><span data-stu-id="89a9a-119">*Portions © 2005, 2009 Microsoft Corporation. All rights reserved.*</span></span>  
  
 <span data-ttu-id="89a9a-120">在 Pearson Education, Inc. 授权下，由 Addison-Wesley Professional 作为 Microsoft Windows 开发系列的一部分再版自 [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619)（Framework 设计准则：可重用 .NET 库的约定、惯例和模式第 2 版），由 Krzysztof Cwalina 和 Brad Abrams 发布于 2008 年 10 月 22 日。</span><span class="sxs-lookup"><span data-stu-id="89a9a-120">*Reprinted by permission of Pearson Education, Inc. from [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) by Krzysztof Cwalina and Brad Abrams, published Oct 22, 2008 by Addison-Wesley Professional as part of the Microsoft Windows Development Series.*</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="89a9a-121">请参阅</span><span class="sxs-lookup"><span data-stu-id="89a9a-121">See also</span></span>

- [<span data-ttu-id="89a9a-122">框架设计指南</span><span class="sxs-lookup"><span data-stu-id="89a9a-122">Framework Design Guidelines</span></span>](index.md)
