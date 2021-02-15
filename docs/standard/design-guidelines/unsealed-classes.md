---
description: 详细了解：未密封类
title: 未密封类
ms.date: 10/22/2008
helpviewer_keywords:
- classes [.NET Framework], unsealed
- unsealed classes
- inheritance, classes
ms.assetid: 9a3bd505-90f5-4053-9f0d-3cf5fa3d3ebf
ms.openlocfilehash: 6fe30c3a2ef8df6b983d857b9502805e90ab83dc
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99641819"
---
# <a name="unsealed-classes"></a><span data-ttu-id="d4fa1-103">未密封类</span><span class="sxs-lookup"><span data-stu-id="d4fa1-103">Unsealed Classes</span></span>

<span data-ttu-id="d4fa1-104">不能从密封类继承，密封类阻止了扩展性。</span><span class="sxs-lookup"><span data-stu-id="d4fa1-104">Sealed classes cannot be inherited from, and they prevent extensibility.</span></span> <span data-ttu-id="d4fa1-105">相比之下，可从其继承的类称为非密封类。</span><span class="sxs-lookup"><span data-stu-id="d4fa1-105">In contrast, classes that can be inherited from are called unsealed classes.</span></span>

 <span data-ttu-id="d4fa1-106">✔️ 请考虑使用未添加虚拟成员或受保护成员的非密封类，这是向框架提供廉价但非常受欢迎的扩展性的好方法。</span><span class="sxs-lookup"><span data-stu-id="d4fa1-106">✔️ CONSIDER using unsealed classes with no added virtual or protected members as a great way to provide inexpensive yet much appreciated extensibility to a framework.</span></span>

 <span data-ttu-id="d4fa1-107">开发人员通常希望从非密封类继承，以便添加便捷成员，如自定义构造函数、新方法或方法重载。</span><span class="sxs-lookup"><span data-stu-id="d4fa1-107">Developers often want to inherit from unsealed classes so as to add convenience members such as custom constructors, new methods, or method overloads.</span></span> <span data-ttu-id="d4fa1-108">例如，`System.Messaging.MessageQueue` 是非密封的，因此允许用户创建默认为特定队列路径的自定义队列，或者添加自定义方法来简化特定场景的 API。</span><span class="sxs-lookup"><span data-stu-id="d4fa1-108">For example,  `System.Messaging.MessageQueue` is unsealed and thus allows users to create custom queues that default to a particular queue path or to add custom methods that simplify the API for specific scenarios.</span></span>

 <span data-ttu-id="d4fa1-109">在大多数编程语言中，类是默认不密封的，这也是框架中对大多数类的推荐默认设置。</span><span class="sxs-lookup"><span data-stu-id="d4fa1-109">Classes are unsealed by default in most programming languages, and this is also the recommended default for most classes in frameworks.</span></span> <span data-ttu-id="d4fa1-110">非密封类型提供的扩展性很受框架用户的欢迎，并且由于与非密封类型相关联的测试成本相对较低，因此提供这种扩展性相当便宜。</span><span class="sxs-lookup"><span data-stu-id="d4fa1-110">The extensibility afforded by unsealed types is much appreciated by framework users and quite inexpensive to provide because of relatively low test costs associated with unsealed types.</span></span>

 <span data-ttu-id="d4fa1-111">*Portions © 2005, 2009 Microsoft Corporation 版权所有。保留所有权利。*</span><span class="sxs-lookup"><span data-stu-id="d4fa1-111">*Portions © 2005, 2009 Microsoft Corporation. All rights reserved.*</span></span>

 <span data-ttu-id="d4fa1-112">在 Pearson Education, Inc. 授权下，由 Addison-Wesley Professional 作为 Microsoft Windows 开发系列的一部分再版自 [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619)（Framework 设计准则：可重用 .NET 库的约定、惯例和模式第 2 版），由 Krzysztof Cwalina 和 Brad Abrams 发布于 2008 年 10 月 22 日。</span><span class="sxs-lookup"><span data-stu-id="d4fa1-112">*Reprinted by permission of Pearson Education, Inc. from [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) by Krzysztof Cwalina and Brad Abrams, published Oct 22, 2008 by Addison-Wesley Professional as part of the Microsoft Windows Development Series.*</span></span>

## <a name="see-also"></a><span data-ttu-id="d4fa1-113">请参阅</span><span class="sxs-lookup"><span data-stu-id="d4fa1-113">See also</span></span>

- [<span data-ttu-id="d4fa1-114">框架设计指南</span><span class="sxs-lookup"><span data-stu-id="d4fa1-114">Framework Design Guidelines</span></span>](index.md)
- [<span data-ttu-id="d4fa1-115">扩展性设计</span><span class="sxs-lookup"><span data-stu-id="d4fa1-115">Designing for Extensibility</span></span>](designing-for-extensibility.md)
- [<span data-ttu-id="d4fa1-116">密封</span><span class="sxs-lookup"><span data-stu-id="d4fa1-116">Sealing</span></span>](sealing.md)
