---
description: 详细了解：虚成员
title: 虚成员
ms.date: 10/22/2008
helpviewer_keywords:
- overridable members
- virtual members
- members [.NET Framework], virtual
ms.assetid: 8ff4eb97-0364-43ec-8a02-934b5cd94d19
ms.openlocfilehash: 7618686764fb3a24ef53e5168b871366b7ffb5bf
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99641780"
---
# <a name="virtual-members"></a>虚成员

可替代虚拟成员，从而更改子类的行为。 就它们提供的扩展性而言，它们与回调非常相似，但就执行性能和内存消耗而言，它们则更佳。 此外，在需要创建一种特殊的现有类型（专用化）的场景中，虚拟成员感觉更自然。

 虚拟成员的性能优于回调和事件，但并不比非虚拟方法好。

 虚拟成员的主要缺点是虚拟成员的行为只能在编译时进行修改。 而回调行为可在运行时进行修改。

 与回调（可能不止回调）一样，虚拟成员的设计、测试和维护成本很高，因为对虚拟成员的任何调用都可能以不可预测的方式被替代，并可能执行任意代码。 此外，通常还需要执行更多的工作以清楚地定义虚拟成员的协定，因此设计和记录这些成员的成本更高。

 ❌ 请勿使成员虚拟化，除非你有充分的理由这样做，并且知道与设计、测试和维护虚拟成员相关的所有成本。

 在不破坏兼容性的情况下，虚拟成员对可对其进行的更改不太宽容。 此外，它们比非虚拟成员慢，主要是因为对虚拟成员的调用没有内联。

 ✔️ 请考虑将扩展性限制在绝对必要的范围内。

 ✔️ 相对于虚拟成员的公共可访问性，请务必首选受保护的可访问性。 公共成员应通过调用受保护的虚拟成员提供扩展性（如需要）。

 类的公共成员应为该类的直接使用者提供正确的功能集。 虚拟成员设计为在子类中被替代，而受保护的可访问性是将所有虚拟扩展点的范围限定在可使用这些扩展点的位置的好方法。

 *Portions &copy; 2005, 2009 Microsoft Corporation。保留所有权利。*

 在 Pearson Education, Inc. 授权下，由 Addison-Wesley Professional 作为 Microsoft Windows 开发系列的一部分再版自 [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619)（Framework 设计准则：可重用 .NET 库的约定、惯例和模式第 2 版），由 Krzysztof Cwalina 和 Brad Abrams 发布于 2008 年 10 月 22 日。

## <a name="see-also"></a>请参阅

- [框架设计指南](index.md)
- [扩展性设计](designing-for-extensibility.md)
