---
description: 详细了解：未密封类
title: 未密封类
ms.date: 10/22/2008
helpviewer_keywords:
- classes [.NET Framework], unsealed
- unsealed classes
- inheritance, classes
ms.assetid: 9a3bd505-90f5-4053-9f0d-3cf5fa3d3ebf
ms.openlocfilehash: 6fe30c3a2ef8df6b983d857b9502805e90ab83dc
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99641819"
---
# <a name="unsealed-classes"></a>未密封类

不能从密封类继承，密封类阻止了扩展性。 相比之下，可从其继承的类称为非密封类。

 ✔️ 请考虑使用未添加虚拟成员或受保护成员的非密封类，这是向框架提供廉价但非常受欢迎的扩展性的好方法。

 开发人员通常希望从非密封类继承，以便添加便捷成员，如自定义构造函数、新方法或方法重载。 例如，`System.Messaging.MessageQueue` 是非密封的，因此允许用户创建默认为特定队列路径的自定义队列，或者添加自定义方法来简化特定场景的 API。

 在大多数编程语言中，类是默认不密封的，这也是框架中对大多数类的推荐默认设置。 非密封类型提供的扩展性很受框架用户的欢迎，并且由于与非密封类型相关联的测试成本相对较低，因此提供这种扩展性相当便宜。

 *Portions © 2005, 2009 Microsoft Corporation 版权所有。保留所有权利。*

 在 Pearson Education, Inc. 授权下，由 Addison-Wesley Professional 作为 Microsoft Windows 开发系列的一部分再版自 [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619)（Framework 设计准则：可重用 .NET 库的约定、惯例和模式第 2 版），由 Krzysztof Cwalina 和 Brad Abrams 发布于 2008 年 10 月 22 日。

## <a name="see-also"></a>请参阅

- [框架设计指南](index.md)
- [扩展性设计](designing-for-extensibility.md)
- [密封](sealing.md)
