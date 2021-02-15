---
description: 详细了解：事件和回调
title: 事件和回调
ms.date: 10/22/2008
helpviewer_keywords:
- events [.NET Framework], extensibility
- methods [.NET Framework], callback
- callback methods
- callbacks
ms.assetid: 48b55c60-495f-4089-9396-97f9122bba7c
ms.openlocfilehash: 8a9049808ec0f7a490889ab1f17c4d8b8e8bd2b3
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99642144"
---
# <a name="events-and-callbacks"></a>事件和回调

回调是允许框架通过委托回调到用户代码的扩展点。 通常通过方法的参数将这些委托传递到框架。

 事件是回调的一种特例，它支持便捷且一致的语法，用于提供委托（事件处理程序）。 此外，Visual Studio 的语句完成和设计器还提供了有关使用基于事件的 API 的帮助。 （请参阅[事件设计](event.md)。）

 ✔️ 请考虑使用回调以允许用户提供要由框架执行的自定义代码。

 ✔️ 请考虑使用事件以允许用户自定义框架的行为，而无需理解面向对象的设计。

 ✔️ 请务必首选使用事件而非普通回调，因为它们对于更广泛的开发人员来说更熟悉，并且与 Visual Studio 语句完成进行了集成。

 ❌ 请避免在对性能敏感的 API 中使用回调。

 ✔️ 在使用回调定义 API 时，请务必使用新的 `Func<...>`、`Action<...>` 或 `Expression<...>` 类型，而不是自定义委托。

 `Func<...>` 和 `Action<...>` 表示泛型委托。 `Expression<...>` 表示函数定义，这些定义可进行编译并随后在运行时进行调用，但也可进行序列化并传递到远程进程。

 ✔️ 请务必衡量并了解使用 `Expression<...>`（而不是使用 `Func<...>` 和 `Action<...>` 委托）对性能的影响。

 `Expression<...>` 类型在大多数情况下在逻辑上等同于 `Func<...>` 和 `Action<...>` 委托。 它们之间的主要区别在于委托旨在用于本地流程场景，而表达式适用于在远程进程或计算机中对该表达式求值是有益的且可能的情况。

 ✔️ 请务必要明白，调用委托即表示你将执行任意代码，而这可能会对安全性、正确性和兼容性产生影响。

 *Portions &copy; 2005, 2009 Microsoft Corporation。保留所有权利。*

 在 Pearson Education, Inc. 授权下，由 Addison-Wesley Professional 作为 Microsoft Windows 开发系列的一部分再版自 [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619)（Framework 设计准则：可重用 .NET 库的约定、惯例和模式第 2 版），由 Krzysztof Cwalina 和 Brad Abrams 发布于 2008 年 10 月 22 日。

## <a name="see-also"></a>请参阅

- [扩展性设计](designing-for-extensibility.md)
- [框架设计指南](index.md)
