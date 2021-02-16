---
description: 详细了解：静态类设计
title: 静态类设计
ms.date: 10/22/2008
helpviewer_keywords:
- type design guidelines, static classes
- class library design guidelines [.NET Framework], classes
- classes [.NET Framework], static
- static classes [.NET Framework]
- classes [.NET Framework], design guidelines
- type design guidelines, classes
ms.assetid: d67c14d8-c4dd-443f-affb-4ccae677c9b6
ms.openlocfilehash: 16db470ab0975a5545617c9c5471d6ac157e688b
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99782463"
---
# <a name="static-class-design"></a>静态类设计

静态类定义为仅包含静态成员（除了从 <xref:System.Object?displayProperty=nameWithType> 继承的实例成员和可能的专用构造函数之外）的类。 某些语言为静态类提供内置支持。 在 C# 2.0 及更高版本中，将一个类声明为静态时，它是密封的、抽象的，并且不能替代或声明任何实例成员。

 静态类是纯面向对象的设计与简单性之间的折衷。 它们通常用于提供其他操作（如 <xref:System.IO.File?displayProperty=nameWithType>）的快捷方式、扩展方法的持有者或者无法为其确保完整的面向对象包装器的功能（如 <xref:System.Environment?displayProperty=nameWithType>）。

 ✔️ 请务必要少使用静态类。

 静态类应该只用作框架的面向对象核心的支持类。

 ❌ 请勿将静态类视为杂项桶。

 ❌ 请勿在静态类中声明或替代实例成员。

 ✔️ 如果你的编程语言没有对静态类的内置支持，请务必将静态类声明为密封的且抽象的，并添加一个专用实例构造函数。

 *Portions © 2005, 2009 Microsoft Corporation 版权所有。保留所有权利。*

 在 Pearson Education, Inc. 授权下，由 Addison-Wesley Professional 作为 Microsoft Windows 开发系列的一部分再版自 [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619)（Framework 设计准则：可重用 .NET 库的约定、惯例和模式第 2 版），由 Krzysztof Cwalina 和 Brad Abrams 发布于 2008 年 10 月 22 日。

## <a name="see-also"></a>请参阅

- [类型设计准则](type.md)
- [框架设计指南](index.md)
