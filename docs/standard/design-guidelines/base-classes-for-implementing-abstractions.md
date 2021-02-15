---
description: 详细了解：用于实现抽象的基类
title: 用于实现抽象的基类
ms.date: 10/22/2008
helpviewer_keywords:
- abstractions [.NET Framework]
- base classes, abstractions
ms.assetid: 37a2d9a4-9721-482a-a40f-eee2c1d97875
ms.openlocfilehash: 255891695583e36977663153b0ccac98b7fff4c6
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99642339"
---
# <a name="base-classes-for-implementing-abstractions"></a>用于实现抽象的基类

严格地说，当一个类派生出另一个类时，这个类就变成了基类。 然而，就本部分而言，基类是一个主要设计用来提供一个公共抽象或者让其他类通过继承来重用一些默认实现的类。 基类通常位于继承层次结构的中间 - 介于层次结构根的抽象与底部的几个自定义实现之间。

 它们充当用于实现抽象的实现帮助程序。 例如，框架对有序项集合的一种抽象是 <xref:System.Collections.Generic.IList%601> 接口。 实现 <xref:System.Collections.Generic.IList%601> 并不简单，因此框架提供了多个基类，如 <xref:System.Collections.ObjectModel.Collection%601> 和 <xref:System.Collections.ObjectModel.KeyedCollection%602>，它们充当用于实现自定义集合的帮助程序。

 基类本身通常不适合充当抽象，因为它们往往包含太多的实现。 例如，`Collection<T>` 基类包含许多实现，这些实现与以下事实有关：它实现非泛型的 `IList` 接口（以便更好地与非泛型集合集成），并且它是存储在内存中某个字段中的项集合。

 如前所述，基类可为需要实现抽象的用户提供十分宝贵的帮助，但同时它们也是一个很大的负担。 它们增加了外围应用，加深了继承层次结构的深度，因此在概念上使框架复杂化。 因此，只有当基类为框架的用户提供重要的价值时，才应该使用基类。 如果它们只为框架的实现者提供价值，就应该避免使用它们，在这种情况下，强烈推荐考虑委托给内部实现，而不是从基类继承。

 ✔️ 请考虑使基类抽象，即使它们不包含任何抽象成员也是如此。 这清楚地向用户传达了该类专门为从其继承而设计。

 ✔️ 请考虑将基类置于与主流场景类型不同的命名空间中。 根据定义，基类旨在用于高级扩展性场景，因此大多数用户对此不感兴趣。

 ❌ 如果打算在公共 API 中使用基类，请避免用“Base”后缀来命名该类。

 *Portions © 2005, 2009 Microsoft Corporation 版权所有。保留所有权利。*

 在 Pearson Education, Inc. 授权下，由 Addison-Wesley Professional 作为 Microsoft Windows 开发系列的一部分再版自 [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619)（Framework 设计准则：可重用 .NET 库的约定、惯例和模式第 2 版），由 Krzysztof Cwalina 和 Brad Abrams 发布于 2008 年 10 月 22 日。

## <a name="see-also"></a>请参阅

- [框架设计指南](index.md)
- [扩展性设计](designing-for-extensibility.md)
