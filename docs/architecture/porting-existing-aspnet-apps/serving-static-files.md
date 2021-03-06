---
title: 在 ASP.NET MVC 和 ASP.NET Core 中提供静态文件
description: 与 IIS 上的 ASP.NET MVC 相比，配置 ASP.NET Core 中提供静态文件的支持涉及的内容是什么？
author: ardalis
ms.date: 11/13/2020
ms.openlocfilehash: 02f84a6985835502c24db8cc68db24c8de086b18
ms.sourcegitcommit: 42d436ebc2a7ee02fc1848c7742bc7d80e13fc2f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/04/2021
ms.locfileid: "102401060"
---
# <a name="serve-static-files-in-aspnet-mvc-and-aspnet-core"></a>在 ASP.NET MVC 和 ASP.NET Core 中提供静态文件

大多数 web 应用都涉及服务器端逻辑和静态文件的组合，必须按原样发送到客户端。 如何从 ASP.NET MVC 迁移到 ASP.NET Core 处理静态文件？

## <a name="host-static-files-in-aspnet-mvc"></a>在 ASP.NET MVC 中托管静态文件

IIS 托管的 ASP.NET MVC 应用程序通常会直接从应用程序中托管静态文件。 ASP.NET MVC 支持将静态文件与应在服务器上保持为私有的文件并行放置。 IIS 和 ASP.NET 要求显式限制某些文件或文件扩展名，以在托管 ASP.NET 应用的文件夹中提供服务。

对于许多静态文件，使用内容交付网络 (CDN) 是一种很好的做法。 利用[静态内容宿主](/azure/architecture/patterns/static-content-hosting)，可以提高性能，同时减少应用服务器的负载和带宽。

## <a name="host-static-files-in-aspnet-core"></a>在 ASP.NET Core 中托管静态文件

这可能是不可思议，但 ASP.NET Core 对静态文件没有内置支持。 此功能始终作为 ASP.NET 的一部分提供，由 IIS 启用，不是 ASP.NET Core 或其 Kestrel web 服务器所固有的。 若要从 ASP.NET Core 应用提供静态文件，必须配置 [静态文件中间件](/aspnet/core/fundamentals/static-files)。

在配置了静态文件中间件的情况下，ASP.NET Core 应用将为位于特定文件夹中的所有文件提供 (通常 */wwwroot*) 。 应用程序或项目文件夹中的其他文件没有被服务器意外公开的风险。 不需要配置基于文件名或扩展的特殊限制，这与 IIS 的情况相同。 相反，开发人员在将文件放入 *wwwroot* 文件夹时，显式选择公开文件。 默认情况下，不共享此文件夹之外的文件。

因为对静态文件的支持使用中间件，所以任何其他中间件都可以作为同一请求管道的一部分应用。 中间件的示例包括身份验证、缓存和压缩。

当然，对于 ASP.NET Core 的应用程序，Cdn 仍是一个不错的选择，因为它们在 ASP.NET MVC 应用程序中使用的原因相同。 作为准备迁移到 .NET Core 的一部分，如果你的应用程序可以通过使用 CDN 实现某些优点，则在迁移到 .NET Core 之前，最好将静态文件迁移到 CDN。 这样做可以减少静态资产的迁移工作总体范围。

## <a name="references"></a>参考

- [静态内容托管](/azure/architecture/patterns/static-content-hosting)
- [ASP.NET Core 中的静态文件](/aspnet/core/fundamentals/static-files)

>[!div class="step-by-step"]
>[上一页](hosting-differences.md)
>[下一页](dependency-injection-differences.md)
