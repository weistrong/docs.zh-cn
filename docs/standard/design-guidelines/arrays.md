---
description: 详细了解：数组
title: 数组
ms.date: 10/22/2008
helpviewer_keywords:
- class library design guidelines [.NET Framework], arrays
- arrays [.NET Framework], usage guidelines
- empty arrays
ms.assetid: 66a1b3d8-6f3f-4715-b235-e1ff95e32d8e
ms.openlocfilehash: 2d919d5e13a03ed1c5d090339f8f0fd9c1a79190
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99642431"
---
# <a name="arrays"></a>数组

✔️ 在公共 API 中，请务必首选使用集合而非数组。 [集合](guidelines-for-collections.md)部分提供有关如何在集合和数组之间进行选择的详细信息。

 ❌ 请勿使用只读数组字段。 该字段本身是只读的并且不能更改，但可以更改数组中的元素。

 ✔️ 请考虑使用交错数组而不是多维数组。

 交错数组是指所包含的元素也是数组的数组。 与多维数组相比，构成元素的数组可以是不同的大小，从而使某些数据集（例如稀疏矩阵）浪费的空间更少。 此外，CLR 优化了针对交错数组的索引操作，因此在某些情况下，它们可能会表现出更好的运行时性能。

 *Portions © 2005, 2009 Microsoft Corporation 版权所有。保留所有权利。*

 在 Pearson Education, Inc. 授权下，由 Addison-Wesley Professional 作为 Microsoft Windows 开发系列的一部分再版自 [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619)（Framework 设计准则：可重用 .NET 库的约定、惯例和模式第 2 版），由 Krzysztof Cwalina 和 Brad Abrams 发布于 2008 年 10 月 22 日。

## <a name="see-also"></a>请参阅

- <xref:System.Array>
- [框架设计指南](index.md)
- [使用准则](usage-guidelines.md)
