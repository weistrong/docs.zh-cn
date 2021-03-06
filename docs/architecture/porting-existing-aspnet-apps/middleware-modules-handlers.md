---
title: 将中间件与模块和处理程序进行比较
description: 本部分探讨了在为其请求处理管道定义中间件的 ASP.NET Core 应用中使用处理程序和模块的 ASP.NET 应用的结构差异。
author: ardalis
ms.date: 11/13/2020
ms.openlocfilehash: 040ae49d1307ef4dcc9dbf49b20544e9cd2bc913
ms.sourcegitcommit: 42d436ebc2a7ee02fc1848c7742bc7d80e13fc2f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/04/2021
ms.locfileid: "102401071"
---
# <a name="compare-middleware-to-modules-and-handlers"></a>将中间件与模块和处理程序进行比较

如果现有的 ASP.NET MVC 或 Web API 应用使用 OWIN/Katana，则很可能已熟悉中间件的概念并将其移植到 ASP.NET Core 应该非常简单。 但是，大多数 ASP.NET 应用依赖于 HTTP 模块和 HTTP 处理程序而不是中间件。 将这些迁移到 ASP.NET Core 需要额外的工作。

## <a name="aspnet-modules-and-handlers"></a>ASP.NET 模块和处理程序

[Http 模块和 http 处理程序](/troubleshoot/aspnet/http-modules-handlers) 是 ASP.NET 体系结构不可或缺的一部分。 处理请求时，每个请求由多个 HTTP 模块处理 (例如，身份验证模块和会话模块) 并由单个 HTTP 处理程序进行处理。 处理程序处理完请求后，请求会通过 HTTP 模块进行流处理。

如果你的应用使用的是自定义 HTTP 模块或 HTTP 处理程序，则需要计划将其迁移到 ASP.NET Core。 ASP.NET Core 中最可能的替换为中间件。

## <a name="aspnet-core-middleware"></a>ASP.NET Core 中间件

ASP.NET Core 在每个应用的方法中定义一个请求管道 `Configure` 。 此请求管道定义了应用如何处理传入的请求，以及管道中的每个方法调用下一个方法直到最终方法终止， *中间件* 的链终止并返回堆栈。 中间件可以面向所有请求，或者可以配置为仅根据请求的路径或其他因素映射到特定请求。 它可以在应用的方法中完全配置 `Configure` ，也可以在单独的类中实现。

使用 HTTP 模块的 ASP.NET MVC 应用程序中的行为可能最适用于 [自定义中间件](/aspnet/core/fundamentals/middleware/?preserve-view=true&view=aspnetcore-3.1)。 自定义 HTTP 处理程序可以替换为响应同一路径的自定义路由或终结点。

## <a name="references"></a>参考

- [ASP.NET HTTP 模块和 HTTP 处理程序](/troubleshoot/aspnet/http-modules-handlers)
- [ASP.NET Core 中间件](/aspnet/core/fundamentals/middleware/?preserve-view=true&view=aspnetcore-3.1)

>[!div class="step-by-step"]
>[上一页](dependency-injection-differences.md)
>[下一页](configuration-differences.md)
