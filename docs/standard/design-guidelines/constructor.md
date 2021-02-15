---
description: 详细了解：构造函数设计
title: 构造函数设计
ms.date: 10/22/2008
helpviewer_keywords:
- member design guidelines, constructors
- constructors, design guidelines
- instance constructors
- type constructors
- virtual members
- constructors, types
- parameterless constructors
- static constructors
ms.assetid: b4496afe-5fa7-4bb0-85ca-70b0ef21e6fc
ms.openlocfilehash: 2a5c85e1dea3349f897c24fa5d40d73c6e1f9d7f
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99642313"
---
# <a name="constructor-design"></a>构造函数设计

有两种类型的构造函数：类型构造函数和实例构造函数。

类型构造函数是静态的构造函数，在使用类型之前由 CLR 运行。 实例构造函数在创建类型的实例时运行。

类型构造函数不能采用任何参数。 而实例构造函数可以。 不采用任何参数的实例构造函数通常称为无参数构造函数。

构造函数是创建类型的实例的最自然方式。 大多数开发人员在考虑创建实例的替代方法（如工厂方法）之前，会搜索并尝试使用构造函数。

✔️ 请考虑提供简单的（理想情况下为默认设置）构造函数。

简单的构造函数包含的参数非常少，且所有参数均为基元或枚举。 此类简单的构造函数可提高框架的可用性。

✔️ 如果所需操作的语义没有直接映射到新实例的构造，或者如果遵循构造函数设计准则感觉不自然，请考虑使用静态工厂方法而不是构造函数。

✔️ 请务必使用构造函数参数作为设置主属性的快捷方式。

使用后跟一些属性集的空构造函数和使用带有多个参数的构造函数在语义上应该不存在任何差异。

✔️ 如果构造函数参数只是用来设置属性，请务必对构造函数参数和属性使用相同的名称。

此类参数和属性的唯一区别应该是大小写形式。

✔️ 在构造函数中执行最少的工作。

除了捕获构造函数参数外，构造函数不应执行太多工作。 任何其他处理的成本都应延迟到需要时再进行。

✔️ 在适当情况下，请务必从实例构造函数引发异常。

✔️ 如果需要公共无参数构造函数，请务必在类中显式声明此类构造函数。

如果未针对某个类型显式声明任何构造函数，则许多语言（如 C#）将自动添加一个公共无参数构造函数。 （抽象类获取一个受保护的构造函数。）

向类添加参数化构造函数会阻止编译器添加无参数构造函数。 这通常会导致意外的中断性变更。

❌ 请避免对结构显式定义无参数构造函数。

这样可以更快地创建数组，因为如果没有定义无参数构造函数，它就不必在数组的每个槽上运行。 请注意，由于此原因，包许多编译器（包括 C#）不允许结构具有无参数构造函数。

❌ 请避免在对象的构造函数中对该对象调用虚拟成员。

调用虚拟成员将导致调用派生度最高的替代，即使派生度最高的类型的构造函数尚未完全运行也是如此。

## <a name="type-constructor-guidelines"></a>类型构造函数指南

✔️ 请务必使静态构造函数专用。

静态构造函数（也称为类构造函数）用于初始化类型。 在创建第一个类型实例或调用该类型的任何静态成员之前，CLR 调用静态构造函数。 用户无法控制调用静态构造函数的时间。 如果静态构造函数不是专用的，则 CLR 以外的代码可以调用它。 根据构造函数中执行的操作，这可能导致意外行为。 C# 编译器会强制使静态构造函数专用。

❌ 请勿从静态构造函数引发异常。

如果从类型构造函数引发了一个异常，则该类型在当前应用程序域中不可用。

✔️ 请考虑使用静态构造函数以内联方式（而非显式地）初始化静态字段，因为运行时能够优化不具有显式定义的静态构造函数的类型的性能。

*Portions © 2005, 2009 Microsoft Corporation 版权所有。保留所有权利。*

在 Pearson Education, Inc. 授权下，由 Addison-Wesley Professional 作为 Microsoft Windows 开发系列的一部分再版自 [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619)（Framework 设计准则：可重用 .NET 库的约定、惯例和模式第 2 版），由 Krzysztof Cwalina 和 Brad Abrams 发布于 2008 年 10 月 22 日。

## <a name="see-also"></a>请参阅

- [成员设计准则](member.md)
- [框架设计指南](index.md)
