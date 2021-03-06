---
title: 比较 ASP.NET Web API 2 和 ASP.NET Core
description: ASP.NET Web API 2 应用和 ASP.NET Core 应用之间的 web Api 有何不同？
author: ardalis
ms.date: 11/13/2020
ms.openlocfilehash: 93aa917174bce24fdf924f6372312c3972473289
ms.sourcegitcommit: 42d436ebc2a7ee02fc1848c7742bc7d80e13fc2f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/04/2021
ms.locfileid: "102401054"
---
# <a name="compare-aspnet-web-api-2-and-aspnet-core"></a>比较 ASP.NET Web API 2 和 ASP.NET Core

ASP.NET Core 提供对 ASP.NET Web API 2 的迭代改进，但对于使用 Web API 2 的开发人员来说，应该很熟悉。 ASP.NET Web API 2 与 ASP.NET MVC 一起开发和发运。 这意味着，这两种方法具有类似但又不同的方法，如属性路由和依赖关系注入。 在 ASP.NET Core 中，MVC 和 Web Api 之间不再有任何区别。 只有 ASP.NET MVC，它包括对基于视图的方案、API 终结点和 Razor Pages (和其他变体（如运行状况检查和 SignalR) ）的支持。

除了在 ASP.NET Core 中保持一致和统一外，在 .NET Core 中生成的 Api 比 ASP.NET Web API 2 上构建的 Api 更容易测试。 稍后我们将更详细地介绍这些 [差异](testing-differences.md) 。 内置的支持在可创建的应用程序中承载 ASP.NET Core 应用程序，该程序可以创建一个用于 `HttpClient` 对应用程序进行内存中请求的应用程序，这在自动测试方面是一项巨大的好处。

从 ASP.NET Web API 2 迁移到 ASP.NET Core 时，转换非常简单。 如果有大的臃肿控制器，可以考虑使用 [ApiEndpoints](https://www.nuget.org/packages/Ardalis.ApiEndpoints/) NuGet 包的一种方法。 此包将每个终结点分解为其自己的特定类，并根据需要关联的请求和响应类型。 这种方法具有与 [基于视图的代码组织 Razor Pages 提供的许多相同的优势](comparing-razor-pages-aspnet-mvc.md)。

## <a name="references"></a>参考

- [从 ASP.NET Web API 迁移到 ASP.NET Core](/aspnet/core/migration/webapi)
- [Ardalis. ApiEndpoints NuGet 包](https://www.nuget.org/packages/Ardalis.ApiEndpoints/)

>[!div class="step-by-step"]
>[上一页](comparing-razor-pages-aspnet-mvc.md)
>[下一页](authentication-differences.md)
