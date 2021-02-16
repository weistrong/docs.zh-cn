---
description: 详细了解：异常引发
title: 异常引发
ms.date: 10/22/2008
helpviewer_keywords:
- exceptions, throwing
- explicitly throwing exceptions
- throwing exceptions, design guidelines
ms.assetid: 5388e02b-52f5-460e-a2b5-eeafe60eeebe
ms.openlocfilehash: b1cf7a4eecc32a9f76ea06c47dd6c16d3afe5470
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99642131"
---
# <a name="exception-throwing"></a>异常引发

本部分中所述的异常引发准则要求对执行失败的含义有一个很好的定义。 每当一个成员无法执行它旨在要执行的操作（成员名称所指的操作）时，执行失败就会发生。 例如，如果 `OpenFile` 方法不能将打开的文件句柄返回给调用方，这将被视为执行失败。

 大多数开发人员已经习惯将异常用于使用错误（例如被零除或空引用）。 在框架中，异常用于所有错误情况，包括执行错误。

 ❌ 请勿返回错误代码。

 异常是在框架中报告错误的主要方法。

 ✔️ 请务必通过引发异常来报告执行失败。

 ✔️ 在代码遇到无法安全地进行进一步执行的情况时，请考虑通过调用 `System.Environment.FailFast`（.NET Framework 2.0 功能）来终止进程，而不是引发一个异常。

 ❌ 如果可能，请勿对正常控制流使用异常。

 除了可能出现争用条件的系统故障和操作之外，框架设计者还应设计 API，使用户能够编写不引发异常的代码。 例如，你可提供一种在调用成员之前检查前置条件的方法，使用户可以编写不引发异常的代码。

 用于检查另一个成员的前置条件的成员通常称为测试者，而实际执行该工作的成员称为执行者。

 在某些情况下，“测试者-执行者”模式可能会产生不可接受的性能开销。 在此类情况下，应考虑使用所谓的“尝试-分析”模式（有关详细信息，请参阅[异常和性能](exceptions-and-performance.md)）。

 ✔️ 请考虑引发异常对性能的影响。 每秒 100 次以上的引发率可能会显著影响大多数应用程序的性能。

 ✔️ 请务必记录所有由可公开调用的成员因违反成员协定（而不是系统故障）而引发的异常，并将它们视为你协定的一部分。

 作为协定一部分的异常不应从一个版本更改为下一个版本（即不应更改异常类型，也不应添加新异常）。

 ❌ 请勿包含可基于某些选项引发或不引发的公共成员。

 ❌ 请勿包含将异常作为返回值或 `out` 参数返回的公共成员。

 从公共 API 返回异常，而不是引发异常，这会使基于异常的错误报告的许多好处无法实现。

 ✔️ 请考虑使用异常生成器方法。

 从不同的位置引发相同的异常是很常见的情况。 若要避免代码膨胀，请使用创建异常并初始化其属性的帮助程序方法。

 此外，引发异常的成员不会被内联。 将 throw 语句移动到生成器中可能会允许该成员内联。

 ❌ 请勿从异常筛选器块中引发异常。

 当异常筛选器引发一个异常时，CLR 将捕获该异常，并且筛选器将返回 false。 此行为与筛选器显式执行并返回 false 是无法区分的，因此很难进行调试。

 ❌ 请避免从 finally 块显式引发异常。 由于调用引发的方法而隐式引发的异常是可以接受的。

 *Portions © 2005, 2009 Microsoft Corporation 版权所有。保留所有权利。*

 在 Pearson Education, Inc. 授权下，由 Addison-Wesley Professional 作为 Microsoft Windows 开发系列的一部分再版自 [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619)（Framework 设计准则：可重用 .NET 库的约定、惯例和模式第 2 版），由 Krzysztof Cwalina 和 Brad Abrams 发布于 2008 年 10 月 22 日。

## <a name="see-also"></a>请参阅

- [框架设计指南](index.md)
- [异常设计准则](exceptions.md)
