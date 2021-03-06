---
title: 迁移到 ASP.NET Core 时的部署方案
description: 在从 ASP.NET 迁移到 ASP.NET Core 时可以使用的不同部署方法的概述，允许并行和分阶段迁移。
author: ardalis
ms.date: 11/13/2020
ms.openlocfilehash: 589acd8c66baacc3aef5833dfaa24e2dcc5c1ee5
ms.sourcegitcommit: 42d436ebc2a7ee02fc1848c7742bc7d80e13fc2f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/04/2021
ms.locfileid: "102401084"
---
# <a name="deployment-scenarios-when-migrating-to-aspnet-core"></a>迁移到 ASP.NET Core 时的部署方案

[!INCLUDE [book-preview](../../../includes/book-preview.md)]

现有的 ASP.NET MVC 和 Web API 应用在 IIS 和 Windows 上运行。 当移植到 ASP.NET Core 时，大型应用可能需要分阶段或并行方法。 在前面的章节中，你了解了许多用于将大型 .NET Framework 应用迁移到几个阶段 ASP.NET Core 的策略。 在本章中，你将了解如何实现不同的部署方案，以便在迁移部分应用程序时需要在生产中维护原始应用程序。

## <a name="split-a-large-web-app"></a>拆分大型 web 应用

请考虑当前在单个网站上的 IIS 中承载的大型 web 应用的常见方案。 在大型应用程序中，功能分为不同的路由和/或目录。 该应用程序是 MVC 视图和 API 终结点的混合。 MVC 路由包含许多不同的路径，这些路径基于功能，并使用标准路由模板从应用程序的根开始 `/{controller}/{action}/{id?}` 。 API 终结点遵循类似的模式，但均位于根下 `/api` 。

假定迁移应用的任务已拆分，以便将 MVC 功能或 API 功能迁移到 ASP.NET Core 首先，如何使原始站点继续与运行其他位置的新 ASP.NET Core 应用进行无缝协作？ 系统的用户应继续查看在迁移之前执行的相同 Url，除非确实需要更改它们。

幸运的是，IIS 是一种功能丰富的 web 服务器，它有一段时间的两项功能是其 [URL 重写模块和应用程序请求路由](/iis/extensions/url-rewrite-module/reverse-proxy-with-url-rewrite-v2-and-application-request-routing)。 IIS 可以使用这些功能作为 [反向代理](/iis/extensions/url-rewrite-module/reverse-proxy-with-url-rewrite-v2-and-application-request-routing)，将客户端请求路由到相应的后端 web 应用。 若要将 IIS 配置为反向代理，请选中 "应用程序请求路由" 功能中的 " **启用代理** " 复选框，然后添加 URL 重写规则，如下所示：

```xml
<rule name="NetCoreProxy">
  <match url="(.*)> />
  <action type="Rewrite" url="http://servername/{R:1}" />
</rule>
```

作为反向代理，IIS 可以将与特定模式匹配的流量路由到完全独立的应用，这可能会在不同服务器上。

如果只使用 URL 重写模块 (或许与主机标头结合) ，则 IIS 可以轻松支持多个网站，每个网站可能运行不同版本的 .NET。 大型 web 应用可能部署为单个网站的集合，每个网站都响应不同的 IP 地址和/或主机标头，或者作为单个网站，其中的一个或多个子应用程序响应某些 URL 路径， (甚至不需要 URL 重写) 。

> [!IMPORTANT]
> 子域通常指域中前两个级别前面的部分。 例如，在域中 `api.contoso.com` ， `api` 是域的子域 `contoso.com` (它本身由 `contoso` 域名和 `.com` 顶级域或 TLD) 组成。 URL 路径引用跟在域名后面的 URL 部分（从开始） `/` 。 URL `https://contoso.com/api` 的路径为 `/api` 。

使用相同或不同的子域 (和域) 承载单个应用有一些优点和缺点。 Cookie 和应用内 [通信等功能可能需要](/aspnet/core/security/cors) 更多配置才能在分布式应用程序中正常工作。 但是，使用不同子域的应用可以更轻松地使用 DNS 将请求路由到完全不同的网络目标，因此可以更轻松地将其部署到多个不同的服务器 (虚拟或其他) ，而无需 IIS 作为反向代理。

在上述示例中，假定将 API 终结点指定为要移植到 ASP.NET Core 的应用程序的第一部分。 在这种情况下，将在 IIS 中创建一个新的 ASP.NET Core 应用程序，并将其作为单独的 web *应用程序* 承载在现有的 ASP.NET *MVC 网站中。* 由于它将作为原始网站的子网站添加并命名为 *api*，因此默认路由应该不会再以开头 `api/` 。 保留此项将导致其与窗体的 Url 匹配 `/api/api/endpoint` 。

图5-1 显示了 ASP.NET Core 2.1 *api* 应用如何作为现有 *DotNetMvcApp* 站点的一部分显示在 IIS 管理器中。

![在 .NET Framework 站点内显示 api 应用的 IIS 管理器](./media/Figure5-1.png)

**图 5-1**。 在 IIS 中通过 .NET Core 应用 .NET Framework 站点。

*DotNetMvcApp* 站点托管为在 .NET Framework 4.7.2 上运行的 MVC 5 应用。 它在集成模式下配置了自己的 IIS 应用池，并运行了 .NET CLR 版本4.0.30319。 *Api* 应用是在 .NET Framework 4.6.1 () 上运行的 ASP.NET Core 应用 `net461` 。 它已作为新的 IIS 应用添加到 *DotNetMvcApp* ，并配置为使用其自己的应用程序池。 它的应用程序池也在集成模式下运行，但配置为 **不使用托管代码** 的 .net CLR 版本，因为它将使用 [ASP.NET Core 模块](/aspnet/core/host-and-deploy/aspnet-core-module?preserve-view=true&view=aspnetcore-2.1)来执行。 ASP.NET Core 应用程序的版本就是一个示例。 还可将其配置为在 .NET Core 3.1 或 .NET 5.0 上运行。 但此时，它无法再以 .NET Framework 库为目标 (请参阅 [选择正确的 .Net Core 版本](choose-net-core-version.md)) 

以这种方式配置时，为正确路由 ASP.NET Core 应用的 Api 必须进行的唯一更改是将其默认路由模板从更改 `[Route("[api/controller]")]` 为 `[Route("[controller]")]` 。

另外，ASP.NET Core 应用可以是 IIS 中的另一个顶级网站。 在这种情况下，你可以将原始站点配置为使用重写规则 (使用 [URL 重写](https://www.iis.net/downloads/microsoft/url-rewrite)) ，如果路径以开头，则将重定向到另一个应用 `/api` 。 ASP.NET Core 应用可以为其路由使用不同的主机标头，以便它不会与主应用发生冲突，但仍可使用基于根的路由对请求做出响应。

例如，可以将图5-1 中使用的同一个 ASP.NET Core 应用部署到配置为 IIS 网站的另一个文件夹。 站点应使用配置的应用池，而 **不是托管代码**。 将其绑定配置为响应服务器上的唯一主机名，如 `api.contoso.com` 。 若要配置 URL 重写以重写请求匹配， `/api` 只需在 IIS 服务器上添加新的入站规则 (或单独的站点) 级别。 匹配模式 `^/api(.*)` 并指定的操作类型 `Rewrite` 和重写 URL `api.contoso.com/{R:1}` 。 `(.*)`在匹配模式和 `{R:1}` 重写 URL 中使用的组合将确保路径的其余部分与新的 url 一起使用。 实现此目的后，同一个 IIS 服务器上的单独站点可以共存于运行不同版本的 .NET，但它们可以作为一个 web 应用显示到 Internet。 图5-2 显示了 IIS 中在单独的网站上配置的重写规则。

![显示 URL 重写规则的 IIS 管理器，用于将子文件夹请求路由到单独的网站](./media/Figure5-2.png)

**图 5-2**。 重写规则，将子文件夹请求重写到另一个网站。

如果你的应用需要在不同的网站或 IIS 内的应用之间进行单一登录，请参阅有关 [如何在 ASP.NET 应用中共享身份验证 cookie](/aspnet/core/host-and-deploy/iis/) 的文档，以获取有关支持此方案的详细说明。

## <a name="summary"></a>总结

将大型应用程序从 .NET Framework 迁移到 ASP.NET Core 的常见方法是选择应用程序的各个部分逐个迁移。 当应用程序的每个部分都处于移植状态时，整个应用程序将保持运行且可用，并且它的一些部分在其原始配置中运行，其他部分在某些版本的 .NET Core 上运行。 通过使用这种方法，可以以增量方式执行大规模的应用迁移。 此方法通过提供更多的反馈，并减少了测试所涉及的总面区，从而限制了风险。 它还允许更快地实现 .NET Core 的优点，例如性能增加。 尽管不再需要在 IIS 上承载 ASP.NET Core 应用程序，但 IIS 仍是一个非常灵活且功能强大的 web 服务器，可将其配置为支持各种承载方案，这些方案涉及同一 IIS 实例上的 .NET Framework 和 ASP.NET Core 应用，甚至在不同服务器上承载。

## <a name="references"></a>参考

- [使用 IIS 在 Windows 上托管 ASP.NET Core](/aspnet/core/host-and-deploy/iis/)
- [URL 重写模块和应用程序请求路由](/iis/extensions/url-rewrite-module/reverse-proxy-with-url-rewrite-v2-and-application-request-routing)
- [URL 重写](https://www.iis.net/downloads/microsoft/url-rewrite)
- [ASP.NET Core 模块](/aspnet/core/host-and-deploy/aspnet-core-module?preserve-view=true&view=aspnetcore-2.1)
- [在 ASP.NET 应用中共享身份验证 cookie](/aspnet/core/host-and-deploy/iis/)
- [本节中使用的示例](https://github.com/ardalis/MigrateDotNetWithIIS)

>[!div class="step-by-step"]
>[上一页](more-migration-scenarios.md)
>[下一页](summary.md)
