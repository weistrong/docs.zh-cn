---
description: 详细了解：扩展方法
title: 扩展方法
ms.date: 10/22/2008
ms.assetid: 5de945cb-88f4-49d7-b0e6-f098300cf357
ms.openlocfilehash: 2f71ec86252045687558bd61337164ac3afbcd20
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99642053"
---
# <a name="extension-methods"></a>扩展方法

扩展方法是一项语言功能，允许使用实例方法调用语法来调用静态方法。 这些方法必须至少采用一个参数，该参数表示方法要针对其操作的实例。

 定义此类扩展方法的类称为 sponsor 类，并且必须声明为静态。 若要使用扩展方法，必须导入用于定义 sponsor 类的命名空间。

 ❌ 请避免盲目地定义扩展方法，特别是对于不属于你的类型。

 如果你确实拥有某个类型的源代码，请考虑改用常规实例方法。 如果你没有某个类型的源代码，而你又想加一个方法，请务必要小心了。 自由地使用扩展方法可能会使那些未设计为具有这些方法的类型的 API 混杂在一起。

 ✔️ 请考虑在以下任何情况下使用扩展方法：

- 要提供与接口的每个实现相关的帮助程序功能（如果所述功能可根据核心接口进行编写）。 这是因为不能以其他方式将具体实现分配给接口。 例如，`LINQ to Objects` 运算符作为所有 <xref:System.Collections.Generic.IEnumerable%601> 类型的扩展方法实现。 因此，任何 `IEnumerable<>` 实现都自动启用了 LINQ。

- 当实例方法会引入对某个类型的依赖项，但此类依赖项会破坏依赖项管理规则时。 例如，从 <xref:System.String> 到 <xref:System.Uri?displayProperty=nameWithType> 的依赖项可能是不可取的，因此从依赖项管理的角度来看，返回 `System.Uri` 的 `String.ToUri()` 实例方法是错误的设计。 返回 `System.Uri` 的静态扩展方法 `Uri.ToUri(this string str)` 是一个更好的设计。

 ❌ 请避免针对 <xref:System.Object?displayProperty=nameWithType> 定义扩展方法。

 VB 用户将无法使用扩展方法语法对对象引用调用此类方法。 VB 不支持调用此类方法，因为在 VB 中，将引用声明为对象将强制对它的所有方法调用进行后期绑定（调用的实际成员是在运行时确定的），而对扩展方法的绑定是在编译时确定的（早期绑定）。

 请注意，本指南适用于存在相同绑定行为的其他语言，或者不支持扩展方法的其他语言。

 ❌ 请勿将扩展方法置于与扩展类型相同的命名空间中，除非它用于向接口添加方法或用于依赖项管理。

 ❌ 请避免使用相同的签名来定义两个或多个扩展方法（即使它们驻留在不同的命名空间中也是如此）。

 ✔️ 如果扩展类型是一个接口，并且在大多数或所有情况下都要使用扩展方法，请考虑在与扩展类型相同的命名空间中定义扩展方法。

 ❌ 请勿在通常与其他功能相关联的名称空间中定义实现某个功能的扩展方法。 而应在与扩展方法所属的功能关联的命名空间中定义这些方法。

 ❌ 请避免对专用于扩展方法的命名空间进行泛型命名（例如“Extension”）。 请改用描述性名称（例如“Routing”）。

 *Portions &copy; 2005, 2009 Microsoft Corporation。保留所有权利。*

 在 Pearson Education, Inc. 授权下，由 Addison-Wesley Professional 作为 Microsoft Windows 开发系列的一部分再版自 [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619)（Framework 设计准则：可重用 .NET 库的约定、惯例和模式第 2 版），由 Krzysztof Cwalina 和 Brad Abrams 发布于 2008 年 10 月 22 日。

## <a name="see-also"></a>请参阅

- [成员设计准则](member.md)
- [框架设计指南](index.md)
