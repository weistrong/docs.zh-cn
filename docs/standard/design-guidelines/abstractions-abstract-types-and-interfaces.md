---
description: 详细了解：抽象（抽象类型和接口）
title: 抽象（抽象类型和接口）
ms.date: 10/22/2008
helpviewer_keywords:
- interfaces [.NET Framework], abstract
- abstract interfaces [.NET Framework]
- abstract types [.NET Framework]
- types [.NET Framework], abstract
ms.assetid: 0a632bc7-9b03-44ee-8842-c82f88672a45
ms.openlocfilehash: 8dc82f004d655429e842c63fab4defff0fd74ab2
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99642432"
---
# <a name="abstractions-abstract-types-and-interfaces"></a>抽象（抽象类型和接口）

抽象是一种描述协定但不提供协定的完整实现的类型。 抽象通常作为抽象类或接口实现，并且它们附带一组定义明确的引用文档，其中描述了实现协定的类型所需的语义。 .NET Framework 中的一些最重要的抽象包括 <xref:System.IO.Stream>、<xref:System.Collections.Generic.IEnumerable%601> 和 <xref:System.Object>。

 你可实现支持抽象协定的具体类型并将此具体类型与使用该抽象的（针对该抽象操作的）框架 API 结合使用，从而扩展框架。

 很难设计一种能够经受时间考验、有意义且有用的抽象。 主要难点是获得正确的成员集，不能多也不能少。 如果一个抽象有太多的成员，它就会变得难以（甚至不可能）实现。 如果它的成员对于承诺的功能而言太少，则在许多令人感兴趣的场景中，它就变得毫无用处。

 框架中的抽象太多也会对框架的可用性产生负面影响。 如果不理解抽象如何融入具体实现及针对该抽象操作的 API 的大环境，通常就很难理解该抽象。 此外，抽象及其成员的名称都必然是抽象的，在没有首先理解它们更广泛的使用上下文的情况下，这通常使得它们难以理解、令人捉摸不透。

 不过，抽象提供极其强大的扩展性，这是其他扩展性机制所不能比拟的。 它们是插件、控制反转 (IoC)、管道等多个体系结构模式的核心。 它们对于框架的可测试性也极其重要。 良好的抽象使你可以出于单元测试的目的，剔除大量的依赖项。 总之，抽象是面向对象的新式框架所追求的丰富性的原因。

 ❌ 请勿提供抽象，除非通过开发一些具体实现及使用该抽象的 API 对它们进行了测试。

 ✔️ 设计抽象时，请务必要在抽象类和接口之间进行仔细地选择。

 ✔️ 考虑为抽象的具体实现提供引用测试。 此类测试应该允许用户测试其实现是否正确实现了协定。

 *Portions © 2005, 2009 Microsoft Corporation 版权所有。保留所有权利。*

 在 Pearson Education, Inc. 授权下，由 Addison-Wesley Professional 作为 Microsoft Windows 开发系列的一部分再版自 [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619)（Framework 设计准则：可重用 .NET 库的约定、惯例和模式第 2 版），由 Krzysztof Cwalina 和 Brad Abrams 发布于 2008 年 10 月 22 日。

## <a name="see-also"></a>请参阅

- [框架设计指南](index.md)
- [扩展性设计](designing-for-extensibility.md)
