---
description: 详细了解：结构设计
title: 结构设计
ms.date: 10/22/2008
helpviewer_keywords:
- class library design guidelines [.NET Framework], structures
- deallocating structures
- allocating structures
- value types, structures
- structure design
- type design guidelines, structures
- structures [.NET Framework], design guidelines
ms.assetid: 1f48b2d8-608c-4be6-9ba4-d8f203ed9f9f
ms.openlocfilehash: a28dd3e452d22e61d95ec521fdbde6539e38ed78
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99641897"
---
# <a name="struct-design"></a>结构设计

常规用途值类型最常被称为结构，即其 C# 关键字。 本部分提供常规结构设计的准则。

 ❌ 请勿为结构提供无参数构造函数。

 若遵循此准则，便可创建结构数组，而不必对每个数组项运行该构造函数。 请注意，C# 不允许结构具有无参数构造函数。

 ❌ 请勿定义可变值类型。

 可变值类型有几个问题。 例如，当属性 getter 返回值类型时，调用方会收到一个副本。 由于该副本是隐式创建的，因此开发人员可能不会意识到他们正在改变副本，而不是原始值。 此外，某些语言（尤其是动态语言）在使用可变值类型方面存在问题，因为即使是本地变量，在被取消引用后，也会导致生成一个副本。

 ✔️ 请务必确保将所有实例数据设置为零、false 或 null（视情况而定）的状态有效。

 这可防止在创建结构数组时意外创建无效的实例。

 ✔️ 请务必在值类型上实现 <xref:System.IEquatable%601>。

 值类型上的 <xref:System.Object.Equals%2A?displayProperty=nameWithType> 方法会导致装箱，且其默认实现效率不高，因为它使用反射。 <xref:System.IEquatable%601.Equals%2A> 可具有更好的性能，并且可得到实施，这样就不会导致装箱。

 ❌ 请勿显式扩展 <xref:System.ValueType>。 事实上，大多数语言都禁止这样做。

 通常，结构可能非常有用，但只应用于不会频繁装箱的小型单个不可变值。

 *Portions © 2005, 2009 Microsoft Corporation 版权所有。保留所有权利。*

 在 Pearson Education, Inc. 授权下，由 Addison-Wesley Professional 作为 Microsoft Windows 开发系列的一部分再版自 [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619)（Framework 设计准则：可重用 .NET 库的约定、惯例和模式第 2 版），由 Krzysztof Cwalina 和 Brad Abrams 发布于 2008 年 10 月 22 日。

## <a name="see-also"></a>请参阅

- [类型设计准则](type.md)
- [框架设计指南](index.md)
- [在类和结构之间选择](choosing-between-class-and-struct.md)
