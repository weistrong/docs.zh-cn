---
description: 详细了解：扩展性设计
title: 扩展性设计
ms.date: 10/22/2008
helpviewer_keywords:
- extending class libraries
- extensibility with class libraries in .NET Framework
- class library design guidelines [.NET Framework], extensibility
- class library extensibility [.NET Framework]
ms.assetid: 1cdb8740-871a-456c-9bd9-db96ca8d79b3
ms.openlocfilehash: 148ae25380698a5a1161fb9fbdd3cc60102e865d
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99642261"
---
# <a name="designing-for-extensibility"></a>扩展性设计

设计框架的一个重要方面是确保框架的扩展性得到了仔细的考虑。 这需要你了解与各种扩展性机制相关的成本和优势。 本章可帮助你确定哪些扩展性机制（子类化、事件、虚拟成员、回调等）可最大程度地满足你的框架的要求。  
  
 可通过多种方式在框架中提供扩展性。 它们从功能较弱但价格较低到功能强大但价格昂贵不等。 对于任何给定的扩展性要求，你应选择可满足要求的成本最低的扩展性机制。 请记住，通常可以在之后添加更多的扩展性，但是如果不引入中断性变更，你永远也无法删除它。  
  
## <a name="in-this-section"></a>本节内容  

 [未密封类](unsealed-classes.md)  
 [受保护的成员](protected-members.md)  
 [事件和回调](events-and-callbacks.md)  
 [虚拟成员](virtual-members.md)  
 [抽象（抽象类型和接口）](abstractions-abstract-types-and-interfaces.md)  
 [用于实现抽象的基类](base-classes-for-implementing-abstractions.md)  
 [密封](sealing.md)  
 *Portions © 2005, 2009 Microsoft Corporation 版权所有。保留所有权利。*  
  
 在 Pearson Education, Inc. 授权下，由 Addison-Wesley Professional 作为 Microsoft Windows 开发系列的一部分再版自 [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619)（Framework 设计准则：可重用 .NET 库的约定、惯例和模式第 2 版），由 Krzysztof Cwalina 和 Brad Abrams 发布于 2008 年 10 月 22 日。  
  
## <a name="see-also"></a>请参阅

- [框架设计指南](index.md)
