---
title: 总结
description: 将 ASP.NET MVC 和 Web API 2 应用程序移植到 ASP.NET Core 的一种总结和重要优势。
author: ardalis
ms.date: 12/16/2020
ms.openlocfilehash: 596ab8621008d1cdc16d841e8faede5f4a1fdd16
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "102400999"
---
# <a name="summary"></a>总结

[!INCLUDE [book-preview](../../../includes/book-preview.md)]

在本书中，你已获得所需的资源，以确定是否有必要将 .NET Framework 上运行的组织的现有应用程序移植到 ASP.NET Core 中。 您已经 [了解了在](migration-considerations.md) 迁移到 .net Core 时有何意义，以及在 .NET Framework 时保留应用)  (部分的需要。 .NET Core 版本及其功能与与 .NET Framework 的兼容性之间存在差异，并且你了解 [了如何为你的应用程序选择正确版本的 .Net core](choose-net-core-version.md)。

移植大型应用程序通常需要大量的风险和精力。 你学习了如何通过使用一个或多个 [增量迁移策略](incremental-migration-strategies.md) 以及用于在生产环境中运行部分迁移应用的多个 [部署策略](deployment-strategies.md) 来缓解此风险。

[ASP.NET 和 ASP.NET Core 之间存在很多不同的体系结构差异](architectural-differences.md)。 在第2章中，你了解了其中许多差异，以及它们如何与应用的迁移相关。 本章涵盖了从 [应用启动](app-startup-differences.md) 和低级别 [中间件](middleware-modules-handlers.md) 到高级 [控制器](controller-differences.md) 的所有内容，以及 [Web API 差异](webapi-differences.md) 和新功能，从而实现了更好的 [测试方案](testing-differences.md)。

大型应用程序通常由多个项目和包组成，并且依赖项可以发挥很大的作用，以确定迁移的难易程度。 [第3章](migrate-large-solutions.md) 帮助你 [确定迁移项目的顺序](identify-migration-sequence.md) ，以及 [如何了解和更新应用的依赖项](understand-update-dependencies.md)。 它还详细介绍 [了迁移应用程序，同时使其在生产环境中运行](strategies-migrating-in-production.md)。

[第4章介绍了如何将实际的 ASP.NET MVC 引用应用迁移到 ASP.NET Core](example-migration-eshop.md)。 本章包含了获取现有应用并将其移植到 ASP.NET Core 上运行所需的所有更改的详细细分。 如果你有关于迁移过程的特定问题及其一些更具体的详细信息，请参阅。

最后， [第5章针对 IIS 的特定部署方案](deployment-scenarios.md)。 你了解了如何使用现有的 IIS web 服务器来托管应用程序中已移植到 ASP.NET Core 的部分，同时保持应用程序的公共 Url 一致。 IIS 包含对 URL 重写和请求路由的强大支持，使其能够并行或在不同服务器上承载多个版本的站点，而不会更改应用公开的面向公众的 Url。

>[!div class="step-by-step"]
>[上一页](deployment-scenarios.md)
