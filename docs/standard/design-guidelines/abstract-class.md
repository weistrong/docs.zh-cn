---
description: 详细了解：抽象类设计
title: 抽象类设计
ms.date: 10/22/2008
helpviewer_keywords:
- type design guidelines, abstract classes
- abstract classes, design guidelines
- class library design guidelines [.NET Framework], classes
- classes [.NET Framework], abstract
- classes [.NET Framework], design guidelines
- type design guidelines, classes
ms.assetid: d3646e6d-5c1f-4922-8fb0-ec5effb30d60
ms.openlocfilehash: 5b1cd833bf43e5bf5731176243809393187e84d4
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99642456"
---
# <a name="abstract-class-design"></a>抽象类设计

❌ 请勿在抽象类型中定义公共或受保护的内部构造函数。

 只有在用户需要创建类型的实例时，构造函数才应该是公共的。 由于你无法创建抽象类型的实例，因此具有公共构造函数的抽象类型设计不正确，会引起用户的误解。

 ✔️ 请务必在抽象类中定义一个受保护的或内部的构造函数。

 受保护的构造函数更常见，在创建子类型时，它仅允许基类进行自己的初始化。

 内部构造函数可用于将抽象类的具体实现限制为定义该类的程序集。

 ✔️ 请务必提供至少一种从你交付的每个抽象类继承的具体类型。

 这样做有助于验证抽象类的设计。 例如，<xref:System.IO.FileStream?displayProperty=nameWithType> 是 <xref:System.IO.Stream?displayProperty=nameWithType> 抽象类的一个实现。

 *Portions © 2005, 2009 Microsoft Corporation 版权所有。保留所有权利。*

 在 Pearson Education, Inc. 授权下，由 Addison-Wesley Professional 作为 Microsoft Windows 开发系列的一部分再版自 [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619)（Framework 设计准则：可重用 .NET 库的约定、惯例和模式第 2 版），由 Krzysztof Cwalina 和 Brad Abrams 发布于 2008 年 10 月 22 日。

## <a name="see-also"></a>请参阅

- [类型设计准则](type.md)
- [框架设计指南](index.md)
