---
description: 详细了解：事件设计
title: 事件设计
ms.date: 10/22/2008
helpviewer_keywords:
- pre-events
- events [.NET Framework], design guidelines
- member design guidelines, events
- event handlers [.NET Framework], event design guidelines
- post-events
- signatures, event handling
ms.assetid: 67b3c6e2-6a8f-480d-a78f-ebeeaca1b95a
ms.openlocfilehash: d64bfb13792aa9d646560de844acddd9b7e188c0
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99642196"
---
# <a name="event-design"></a>事件设计

事件是最常用的回叫形式（“回叫”就是允许框架调入用户代码的构造）。 其他回叫机制包括采用委托的成员、虚拟成员和基于接口的插件。可用性调查中的数据显示，大多数开发人员更喜欢使用事件，而不是使用其他回叫机制。 事件与 Visual Studio 和多种语言完美集成。

 值得注意的是存在两组事件：在系统状态更改前引发的事件（称为前期事件），以及在状态更改后引发的事件（称为后期事件）。 前期事件的一个例子是 `Form.Closing`，它是在窗体关闭前引发的。 后期事件的一个例子是 `Form.Closed`，它是在窗体关闭后引发的。

 ✔️ 请对事件使用“raise”（引发）这个词，而不是使用“fire”（激发）或“trigger”（触发）。

 ✔️ 请使用 <xref:System.EventHandler%601?displayProperty=nameWithType>，而不是手动创建新的委托来用作事件处理程序。

 ✔️ 请考虑将 <xref:System.EventArgs> 的子类用作事件参数，除非你完全确信事件将永不需要将任何数据传递到事件处理方法（在此情况下，你可直接使用 `EventArgs` 类型）。

 如果你直接使用 `EventArgs` 来传递 API，则你永远无法在不破坏兼容性的情况下添加任何要与事件一起传递的数据。 如果你使用子类，则即使最开始完全为空，你也将能够在需要时向子类添加属性。

 ✔️ 请使用受保护的虚拟方法来引发每个事件。 这仅适用于非密封类上的非静态事件，不可用于结构、密封类和静态事件。

 此方法旨在使派生类能够处理使用替代项的事件。 对于处理派生类中的基类事件，替代操作更加灵活、更加快速，也更自然。 按照约定，方法的名称应以“On”开头，后跟事件的名称。

 派生类可选择不在其替代中调用方法的基础实现。 为此，请不要在为使基类正常工作而所需的方法中包含任何处理。

 ✔️ 请将一个参数传递给会引发事件的受保护的方法。

 该参数应被命名为 `e`，且其类型应为事件参数类。

 ❌ 在引发非静态事件时，请勿将 NULL 作为发送方传递。

 ✔️ 在引发静态事件时，请将 NULL 作为发送方传递。

 ❌ 在引发事件时，请勿将 NULL 作为事件数据参数传递。

 如果不想向事件处理方法传递任何数据，则应传递 `EventArgs.Empty`。 开发人员希望此参数不是 NULL。

 ✔️ 请考虑引发最终用户可取消的事件。 这仅适用于前期事件。

 使用 <xref:System.ComponentModel.CancelEventArgs?displayProperty=nameWithType> 或其子类作为事件参数，以允许最终用户取消事件。

### <a name="custom-event-handler-design"></a>自定义事件处理程序设计

 在有些情况下无法使用 `EventHandler<T>`，例如当框架需要与不支持泛型的较早版本的 CLR 一起使用时。 在这种情况下，你可能需要设计和开发自定义事件处理程序委托。

 ✔️ 请对事件处理程序使用返回类型 void。

 事件处理程序可调用多个事件处理方法，可能是对多个对象调用。 如果事件处理方法可返回值，则每个事件调用都有多个返回值。

 ✔️ 请使用 `object` 作为事件处理程序的第一个参数的类型，并将其称为 `sender`。

 ✔️ 请使用 <xref:System.EventArgs?displayProperty=nameWithType> 或其子类作为事件处理程序的第二个参数的类型，并将其称为 `e`。

 ❌ 事件处理程序上请勿带有两个以上的参数。

 *Portions © 2005, 2009 Microsoft Corporation 版权所有。保留所有权利。*

 *在 Pearson Education, Inc. 授权下，由 Addison-Wesley Professional 作为 Microsoft Windows 开发系列的一部分再版自 [Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619)（Framework 设计准则：可重用 .NET 库的约定、惯例和模式第 2 版），由 Krzysztof Cwalina 和 Brad Abrams 发布于 2008 年 10 月 22 日。*

## <a name="see-also"></a>请参阅

- [成员设计准则](member.md)
- [框架设计指南](index.md)
