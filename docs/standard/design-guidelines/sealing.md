---
description: 详细了解：密封
title: 密封
ms.date: 10/22/2008
helpviewer_keywords:
- limiting extensibility
- classes [.NET Framework], sealing
- preventing customization
- sealed classes
ms.assetid: cc42267f-bb7a-427a-845e-df97408528d4
ms.openlocfilehash: 94673f793aa7373e1076e13cbda900fba83786f6
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99731716"
---
# <a name="sealing"></a>密封

面向对象的框架的一项功能是，开发人员可采用框架设计者无法预料的方式对其进行扩展和自定义。 这是可扩展设计的强大之处，也是危险之处。 因此，当你设计框架时，非常重要的一点是在需要时仔细设计以实现扩展性，而在有风险时限制扩展性。

 阻止扩展性的强大机制是密封的。 可以密封类或单个成员。 密封一个类可防止用户从该类继承。 密封一个成员可防止用户替代特定成员。

 ❌ 若没有充分的理由，请勿密封类。

 因为想不出扩展性场景而密封类不是一个充分的理由。 框架用户喜欢出于各种非显着性的原因而从类中继承，比如添加便捷成员。 有关用户要从某类型继承的非显着性原因的示例，请参阅[非密封类](unsealed-classes.md)。

 密封一个类的充分理由包括：

- 类是一个静态类。 请参阅[静态类设计](static-class.md)。

- 类在继承的受保护成员中存储对安全性敏感的机密。

- 类继承许多虚拟成员，且单独密封它们的成本将超过使该类不密封的好处。

- 类是一个需要非常快速的运行时查找的特性。 密封特性的性能水平略高于非密封特性。 请参阅[特性](attributes.md)。

 ❌ 请勿对密封类型声明受保护的成员或虚拟成员。

 按照定义，不能从密封类型继承。 这意味着不能调用密封类型的受保护成员，也不能替代密封类型的虚拟方法。

 ✔️ 请考虑密封你替代的成员。

 引入虚拟成员（如[虚拟成员](virtual-members.md)中所述）可能导致的问题也同样适用于替代（尽管程度稍低）。 密封替代可以使你从继承层次结构中的这一点开始就避免这些问题。

 *Portions © 2005, 2009 Microsoft Corporation 版权所有。保留所有权利。*

 在 Pearson Education, Inc. 授权下，由 Addison-Wesley Professional 作为 Microsoft Windows 开发系列的一部分再版自 [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619)（Framework 设计准则：可重用 .NET 库的约定、惯例和模式第 2 版），由 Krzysztof Cwalina 和 Brad Abrams 发布于 2008 年 10 月 22 日。

## <a name="see-also"></a>请参阅

- [框架设计指南](index.md)
- [扩展性设计](designing-for-extensibility.md)
- [未密封类](unsealed-classes.md)
