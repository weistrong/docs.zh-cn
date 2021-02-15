---
description: 详细了解：嵌套类型
title: 嵌套类型
ms.date: 10/22/2008
helpviewer_keywords:
- types, nested
- public nested types
- type design guidelines, nested types
- nested types
- members [.NET Framework], type
- class library design guidelines [.NET Framework], nested types
ms.assetid: 12feb7f0-b793-4d96-b090-42d6473bab8c
ms.openlocfilehash: 07d81827d67e50351f442ec15ca6cb18a63160fe
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99713372"
---
# <a name="nested-types"></a>嵌套类型

嵌套类型是在另一种类型（称为封闭类型）的范围内定义的类型。 嵌套类型可访问其封闭类型的所有成员。 例如，它可以访问在封闭类型中定义的专用字段，还可以访问在封闭类型的所有祖先类型中定义的受保护字段。

 一般而言，应慎用嵌套类型。 其原因有若干： 有些开发人员并不完全熟悉概念。 例如，这些开发人员可能在声明嵌套类型的变量的语法方面遇到了问题。 嵌套类型也与其封闭类型紧密耦合，因此嵌套类型不适合用作通用类型。

 嵌套类型最适合对其封闭类型的实现详细信息进行建模。 最终用户应该很少需要声明嵌套类型的变量，也几乎永远不需要显式实例化嵌套类型。 例如，集合的枚举器可以是该集合的嵌套类型。 枚举器通常通过其封闭类型进行实例化，由于许多语言支持 foreach 语句，因此枚举器变量很少需要由最终用户声明。

 ✔️ 当嵌套类型和其外部类型之间的 关系使得成员可访问性语义可取时，请务必使用嵌套类型。

 ❌ 请勿使用公共嵌套类型作为逻辑分组构造；对此使用命名空间。

 ❌ 请避免使用公开暴露的嵌套类型。 对此，唯一的例外情况是：只需在很少的情况（如子类化或其他高级自定义场景）下声明嵌套类型的变量时。

 ❌ 如果嵌套类型可能在包含类型之外被引用，则请勿使用该类型。

 例如，一个传递给在类上定义的方法的枚举不应被定义为类中的嵌套类型。

 ❌ 如果嵌套类型需要通过客户端代码进行实例化，则请勿使用该类型。  如果某个类型具有公共构造函数，则它可能不应被嵌套。

 如果某个类型可以被实例化，这似乎表明该类型在框架中有自己的位置（你可以创建它，使用它并销毁它，而不必使用外部类型），因此该类型不应被嵌套。 如果内部类型与外部类型没有任何关系，则不应在外部类型之外广泛重用内部类型。

 ❌ 请勿将嵌套类型定义为接口的成员。 许多语言不支持此类构造。

 *Portions © 2005, 2009 Microsoft Corporation 版权所有。保留所有权利。*

 在 Pearson Education, Inc. 授权下，由 Addison-Wesley Professional 作为 Microsoft Windows 开发系列的一部分再版自 [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619)（Framework 设计准则：可重用 .NET 库的约定、惯例和模式第 2 版），由 Krzysztof Cwalina 和 Brad Abrams 发布于 2008 年 10 月 22 日。

## <a name="see-also"></a>请参阅

- [类型设计准则](type.md)
- [框架设计指南](index.md)
