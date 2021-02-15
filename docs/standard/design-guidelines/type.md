---
description: 详细了解：类型设计准则
title: 类型设计准则
ms.date: 10/22/2008
helpviewer_keywords:
- type design guidelines
- type design guidelines, about type design guidelines
- class library design guidelines [.NET Framework], type design guidelines
- types [.NET Framework], design guidelines
ms.assetid: 6b49314e-8bba-43ea-97ca-4e0255812f95
ms.openlocfilehash: d2c193d41dda118558cc5e7541f7e2dfbaf1a369
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99641832"
---
# <a name="type-design-guidelines"></a>类型设计准则

从 CLR 的角度来看，只有两种类型：引用类型和值类型，但为了讨论框架设计，我们将类型分成更多的逻辑组，每个逻辑组都有自己特定的设计规则。

 类是引用类型的常规用例。 它们构成了大多数框架中的大部分类型。 类之所以受欢迎，是因为它们支持一组丰富的面向对象的功能以及它们的普遍适用性。 基类和抽象类是与扩展性相关的特殊逻辑组。

 接口是可由引用类型和值类型实现的类型。 因此，它们可充当引用类型和值类型的多态层次结构的根。 此外，接口还可用于模拟多重继承，而这是 CLR 本机不支持的。

 结构是值类型的常规用例，应为小型简单类型保留，类似于语言基元。

 枚举是值类型的一种特例，用于定义短值集，如星期几、控制台颜色等。

 静态类是旨在作为静态成员容器的类型。 它们通常用于提供其他操作的快捷方式。

 委托、异常、特性、数组和集合都是专用于特定用途的引用类型的特例，它们的设计和使用指南在本书的其他位置进行了讨论。

 ✔️ 请务必确保每个类型都是一组定义完善的相关成员，而不只是一个随机的无关功能集合。

## <a name="in-this-section"></a>本节内容

 [在类和结构之间选择](choosing-between-class-and-struct.md) [抽象类设计](abstract-class.md) [静态类设计](static-class.md) [接口设计](interface.md) [结构设计](struct.md) [枚举设计](enum.md) [嵌套设计](nested-types.md) *Portions © 2005, 2009 Microsoft Corporation。保留所有权利。*

 在 Pearson Education, Inc. 授权下，由 Addison-Wesley Professional 作为 Microsoft Windows 开发系列的一部分再版自 [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619)（Framework 设计准则：可重用 .NET 库的约定、惯例和模式第 2 版），由 Krzysztof Cwalina 和 Brad Abrams 发布于 2008 年 10 月 22 日。

## <a name="see-also"></a>请参阅

- [框架设计指南](index.md)
