---
title: 将应用移植到 .NET Core 简介
description: 本章介绍了考虑将现有 ASP.NET 应用迁移到 .NET Core 的团队的注意事项列表。
author: ardalis
ms.date: 11/13/2020
ms.openlocfilehash: a346d1c693389cc4ca682b41a3b7fc094cfa5482
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "102400977"
---
# <a name="introduction-to-porting-apps-to-net-core"></a>将应用移植到 .NET Core 简介

[!INCLUDE [book-preview](../../../includes/book-preview.md)]

.NET Core 是 .NET Framework 的一种革新性步骤。 由于跨平台的支持与开发人员满意度相比，它提供了一种与从工作效率到性能之间的 .NET Framework 优势的主机。 ASP.NET Core 甚至还投票了 [2020 Stack Overflow 开发人员调查](https://insights.stackoverflow.com/survey/2020#technology-most-loved-dreaded-and-wanted-web-frameworks)中最喜欢的 web 框架。 很明显，需要考虑迁移。

请记住， [.Net Core 是 .net 的未来](https://devblogs.microsoft.com/dotnet/net-core-is-the-future-of-net/)，这一点很重要。 若要引言本文：

> 新应用程序应基于 .NET Core 构建。 .NET Core 是 .NET 的未来投资。 现有的应用程序可以安全地保留在 .NET Framework 上。 希望利用 .NET 中的新功能的现有应用应考虑迁移到 .NET Core。 随着我们计划未来的发展，我们将进一步为平台带来更多的功能。

但是，将应用程序升级到 ASP.NET Core 需要一些精力。 应根据业务价值和目标来权衡这一工作。 .NET Framework 的应用程序的生存期很长，而且可预见的未来，Windows 内置了支持。 确定迁移到 .NET Core 之前应考虑的一些问题是合适的吗？ 预期的优点是什么？ 权衡有哪些？ 涉及了多少工作量？ 这些明显的问题只是开始，但由于团队考虑到了如何使用目前和未来的应用程序来支持其客户需求，因此提供了一个很好的起点。

- 是否适合迁移到 .NET Core？
- 何时保持 .NET Framework？
- 应用程序的目标是否应作为步进石头 ASP.NET Core 2.1？
- 团队应如何选择合适的 .NET Core 版本作为目标？
- 对于大型应用的增量迁移，建议使用哪些策略？
- 移植到 .NET Core 时应考虑的部署策略是什么？
- 在哪里可以找到其他资源？

本介绍章节介绍了所有这些问题，并详细介绍了以后几章中更具体的技术注意事项。

## <a name="references"></a>参考

- [2020 Stack Overflow 开发人员调查最喜欢的 web 框架](https://insights.stackoverflow.com/survey/2020#technology-most-loved-dreaded-and-wanted-web-frameworks)
- [.Net Core 是 .NET 的未来](https://devblogs.microsoft.com/dotnet/net-core-is-the-future-of-net/)

>[!div class="step-by-step"]
>[上一页](index.md)
>[下一页](migration-considerations.md)
