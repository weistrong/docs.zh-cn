---
description: 详细了解：接口设计
title: 接口设计
ms.date: 10/22/2008
helpviewer_keywords:
- interfaces [.NET Framework], design guidelines
- type design guidelines, interfaces
- class library design guidelines [.NET Framework], interfaces
ms.assetid: a016bd18-6710-4358-9438-9f190a295392
ms.openlocfilehash: 387f921f8bdbe6c6d398aa31dcc8a22c7da455f7
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99641975"
---
# <a name="interface-design"></a>接口设计

虽然大多数 API 最好使用类和结构进行建模，但是在某些情况下，接口更合适或者是唯一的选择。

 CLR 不支持多重继承（例如，CLR 类不能从多个基类继承），但它允许类型实现一个或多个接口以及从基类继承。 因此，接口常用于实现多重继承的效果。 例如，<xref:System.IDisposable> 是一个接口，该接口允许类型独立于它们要参与的任何其他继承层次结构来支持可处置性。

 适合定义接口的另一种情况是创建可由多种类型（包括某些值类型）支持的通用接口。 值类型不能从 <xref:System.ValueType> 以外的类型继承，但它们可以实现接口，因此，使用接口是提供通用基类型的唯一选择。

 ✔️ 如果你需要使一些通用 API 可由包含值类型的类型集支持，请务必定义一个接口。

 ✔️ 如果你需要针对已从其他类型继承的类型支持一个接口的功能，请考虑定义该接口。

 ❌ 请避免使用标记接口（没有成员的接口）。

 如果你需要将一个类标记为具有特定的特征（标记），则通常使用自定义特性而不是接口。

 ✔️ 请务必提供至少一种作为接口的实现的类型。

 这样做有助于验证接口的设计。 例如，<xref:System.Collections.Generic.List%601> 是 <xref:System.Collections.Generic.IList%601> 接口的一个实现。

 ✔️ 请务必提供至少一个使用你定义的每个接口的 API（将接口用作参数的方法或类型化为接口的属性）。

 这样做有助于验证接口设计。 例如，<xref:System.Collections.Generic.List%601.Sort%2A?displayProperty=nameWithType> 使用 <xref:System.Collections.Generic.IComparer%601?displayProperty=nameWithType> 接口。

 ❌ 请勿将成员添加到之前已提供的接口。

 这样做会破坏接口的实现。 你应该创建新的接口，以避免版本控制问题。

 除了这些准则中所述的情况外，在设计托管代码可重用库时，通常应该选择类而不是接口。

 *Portions © 2005, 2009 Microsoft Corporation 版权所有。保留所有权利。*

 在 Pearson Education, Inc. 授权下，由 Addison-Wesley Professional 作为 Microsoft Windows 开发系列的一部分再版自 [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619)（Framework 设计准则：可重用 .NET 库的约定、惯例和模式第 2 版），由 Krzysztof Cwalina 和 Brad Abrams 发布于 2008 年 10 月 22 日。

## <a name="see-also"></a>请参阅

- [类型设计准则](type.md)
- [框架设计指南](index.md)
