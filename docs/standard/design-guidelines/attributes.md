---
description: 详细了解：特性
title: 特性
ms.date: 10/22/2008
helpviewer_keywords:
- attributes [.NET Framework], about
- class library design guidelines [.NET Framework], attributes
ms.assetid: ee0038ef-b247-4747-a650-3c5c5cd58d8b
ms.openlocfilehash: 1557ba0945da0c8498c67f70ba4a01dd0bbe432e
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99642417"
---
# <a name="attributes"></a>特性

<xref:System.Attribute?displayProperty=nameWithType> 是用于定义自定义特性的基类。

 特性是可添加到编程元素（如程序集、类型、成员和参数）的注释。 它们存储在程序集的元数据中，并且可在运行时使用反射 API 进行访问。 例如，框架定义了 <xref:System.ObsoleteAttribute>，可将其应用于类型或成员，以指示该类型或成员已弃用。

 特性可具有一个或多个属性，这些属性包含与特性相关的其他数据。 例如，`ObsoleteAttribute` 可能包含有关其中某个类型或成员已弃用的版本的其他信息，以及替换已过时 API 的新 API 的说明。

 应用某个特性时，必须指定该特性的某些属性。 它们被称为必需属性或必需参数，因为它们被表示为位置构造函数参数。 例如，<xref:System.Diagnostics.ConditionalAttribute> 的 <xref:System.Diagnostics.ConditionalAttribute.ConditionString%2A> 属性是一个必需属性。

 在应用特性时不一定要指定的属性称为可选属性（或可选参数）。 它们由可设置的属性表示。 应用某个特性时，编译器提供了特殊的语法来设置这些属性。 例如，<xref:System.AttributeUsageAttribute.Inherited%2A?displayProperty=nameWithType> 属性表示一个可选参数。

 ✔️ 请务必使用后缀“Attribute”来命名自定义属性类。

 ✔️ 请务必将 <xref:System.AttributeUsageAttribute> 应用于自定义属性。

 ✔️ 请务必提供可选参数的可设置属性。

 ✔️ 请务必提供必需参数的仅限获取属性。

 ✔️ 请务必提供构造函数参数来初始化对应于必需参数的属性。 每个参数都应具有与相应属性相同的名称（但大小写不同）。

 ❌ 请避免提供构造函数参数来初始化对应于可选参数的属性。

 换句话说，请勿包含可同时使用构造函数和 setter 设置的属性。 此准则非常明确地说明了哪些参数是可选的，哪些参数是必需的，并避免了用两种方法来执行相同的操作。

 ❌ 请避免重载自定义特性构造函数。

 只具有一个构造函数，这清楚地告诉了用户哪些参数是必需的，哪些参数是可选的。

 ✔️ 如果可能，请务必密封自定义特性类。 这样可以更快地查找特性。

 *Portions &copy; 2005, 2009 Microsoft Corporation。保留所有权利。*

 在 Pearson Education, Inc. 授权下，由 Addison-Wesley Professional 作为 Microsoft Windows 开发系列的一部分再版自 [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619)（Framework 设计准则：可重用 .NET 库的约定、惯例和模式第 2 版），由 Krzysztof Cwalina 和 Brad Abrams 发布于 2008 年 10 月 22 日。

## <a name="see-also"></a>请参阅

- [框架设计指南](index.md)
- [使用准则](usage-guidelines.md)
