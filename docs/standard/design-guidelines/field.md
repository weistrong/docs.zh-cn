---
description: 详细了解：字段设计
title: 字段设计
ms.date: 10/22/2008
helpviewer_keywords:
- fields, design guidelines
- read-only fields
- member design guidelines, fields
ms.assetid: 7cb4b0f3-7a10-4c93-b84d-733f7134fcf8
ms.openlocfilehash: 88df60c3050035221dc65429bbd543c71d5d69b3
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99642040"
---
# <a name="field-design"></a>字段设计

封装原则是面向对象的设计中最重要的概念之一。 此原则表明，存储在一个对象中的数据应只能由该对象访问。

 解释该原则的一个有效的方法是：应该设计一个类型，以便可以在不破坏代码的情况下对该类型的字段进行更改（名称或类型更改），而不是对该类型的成员进行更改。 此解释直接暗示了所有字段都必须是专用的。

 我们将常量和静态只读字段排除在这一严格限制之外，因为几乎从定义上来说，此类字段从来不需要更改。

 ❌ 请勿提供公共的或受保护的实例字段。

 应提供用于访问字段的属性，而不是将其设为公共或受保护。

 ✔️ 请务必对永远不会更改的常量使用常量字段。

 编译器会直接将常量字段的值直接刻录到调用代码中。 因此，如果没有破坏兼容性的风险，常量值永远不会更改。

 ✔️ 请务必对预定义的对象实例使用公共静态 `readonly` 字段。

 如果存在类型的预定义实例，请将它们声明为类型本身的公共只读静态字段。

 ❌ 请勿将可变类型的实例分配到 `readonly` 字段。

 可变类型是具有实例的类型，这些实例可在实例化后进行修改。 例如，数组、大多数集合和流都是可变类型，但 <xref:System.Int32?displayProperty=nameWithType>、<xref:System.Uri?displayProperty=nameWithType> 和 <xref:System.String?displayProperty=nameWithType> 都是不可变的。 引用类型字段的只读修饰符可防止替换存储在该字段中的实例，但不能防止通过调用更改实例的成员来修改字段的实例数据。

 *Portions © 2005, 2009 Microsoft Corporation 版权所有。保留所有权利。*

 在 Pearson Education, Inc. 授权下，由 Addison-Wesley Professional 作为 Microsoft Windows 开发系列的一部分再版自 [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619)（Framework 设计准则：可重用 .NET 库的约定、惯例和模式第 2 版），由 Krzysztof Cwalina 和 Brad Abrams 发布于 2008 年 10 月 22 日。

## <a name="see-also"></a>请参阅

- [成员设计准则](member.md)
- [框架设计指南](index.md)
