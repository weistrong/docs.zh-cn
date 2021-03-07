---
title: ASP.NET MVC 和 ASP.NET Core 之间的应用启动差异
description: ASP.NET MVC 和 ASP.NET Core 在应用的启动方式上有很大差异。 了解重要的区别，以及如何从 ASP.NET MVC 迁移到 ASP.NET Core。
author: ardalis
ms.date: 11/13/2020
ms.openlocfilehash: eaf8d8fac42ddebbb944273b672666e0bd2b1a67
ms.sourcegitcommit: 42d436ebc2a7ee02fc1848c7742bc7d80e13fc2f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/04/2021
ms.locfileid: "102401101"
---
# <a name="app-startup-differences-between-aspnet-mvc-and-aspnet-core"></a>ASP.NET MVC 和 ASP.NET Core 之间的应用启动差异

ASP.NET MVC 应用程序完全位于 Internet Information Server (IIS) ，这是 Windows 操作系统上可用的主 web 服务器。 与 ASP.NET MVC 不同，ASP.NET Core 应用是可执行应用。 您可以使用从命令行运行它们 `dotnet run` 。 它们具有类似于所有 c # 程序的入口点方法，通常 `public static void Main()` 或类似的变体 (可能包含参数或 `async` 支持) 。 这可能是 ASP.NET Core 与 ASP.NET MVC 之间最大的体系结构差异，并且是允许 ASP.NET Core 在非 Windows 系统上运行的几个不同之处。

## <a name="aspnet-mvc-startup"></a>ASP.NET MVC 启动

在 IIS 中承载时，ASP.NET apps 依赖 IIS 来实例化某些对象并在请求到达时调用某些方法。 ASP.NET 创建从派生的 *global.asax* 文件的类的实例 `HttpApplication` 。 收到第一个请求时，在处理请求本身之前，ASP.NET 将调用 `Application_Start` *global.asax* 文件的类中的方法。 任何需要在 ASP.NET MVC 应用开始时运行的逻辑都可以添加到此方法中。

许多用于 ASP.NET MVC 和 Web API 的 NuGet 包使用 [WebActivator](https://github.com/davidebbo/WebActivator) 包，使其在应用启动期间运行一些代码。 按照约定，通常会将此代码添加到 *App_Start* 文件夹，并通过属性将其配置为在紧挨之前或之后运行 `Application_Start` 。

还可以通过 [ASP.NET MVC 使用适用于 .net (OWIN) 和 Project Katana 的开放 Web 接口](/aspnet/aspnet/overview/owin-and-katana/getting-started-with-owin-and-katana)。 执行此操作时，应用程序将包含一个 *Startup.cs* 文件，该文件负责设置请求中间件，其方式与 ASP.NET Core 行为方式非常类似。

如果你需要在 ASP.NET MVC 应用启动时运行代码，则它通常将使用以下方法之一。

## <a name="aspnet-core-startup"></a>ASP.NET Core 启动

如前所述，ASP.NET Core 应用是独立的程序。 这种情况下，它们通常包含一个 *Program.cs* 文件，其中包含应用程序的入口点。 此文件的典型示例如图2-1 所示。

```csharp
public class Program
{
    public static void Main(string[] args)
    {
        CreateHostBuilder(args).Build().Run();
    }

    public static IHostBuilder CreateHostBuilder(string[] args) =>
        Host.CreateDefaultBuilder(args)
            .ConfigureWebHostDefaults(webBuilder =>
            {
                webBuilder.UseStartup<Startup>();
            });
}
```

**图 2-1**. 典型 ASP.NET Core *Program.cs* 文件。

图2-1 中所示的代码为应用程序创建 *主机* ，生成应用程序并运行它。 ASP.NET Core 应用在由所示的配置的主机中运行 `IHostBuilder` 。 尽管可以使用完全配置 ASP.NET Core 应用程序，但这种 `IHostBuilder` 情况通常是在类中完成的 `Startup` 。

`Startup`类向宿主公开两个方法： `ConfigureServices` 和 `Configure` 。 `ConfigureServices`方法用于定义应用将使用的服务及其各自的生存期。 `Configure`方法用于定义如何通过设置由中间件组成的请求管道来处理对应用程序的每个请求。

除了与配置应用服务或请求管道相关的代码以外，应用程序可能还具有应用启动时必须运行的其他代码。 此类代码通常放置在 *Program.cs* 中或注册为 `IHostedService` ，这会在应用程序启动时由 [通用主机](/aspnet/core/fundamentals/host/generic-host?preserve-view=true&view=aspnetcore-3.1) 启动。

`IHostedService`接口只公开两个方法： `StartAsync` 和 `StopAsync` 。 在中注册接口， `ConfigureServices` 主机会执行其他工作，在 `StartAsync` 应用启动之前调用方法。

## <a name="porting-considerations"></a>移植注意事项

希望将其应用从 ASP.NET MVC 迁移到 ASP.NET Core 的团队需要确定在应用程序启动时运行的代码，并确定此类代码在其 ASP.NET Core 应用中的适当位置。 对于需要在应用程序启动时运行的自定义代码，尤其是异步代码，建议的方法通常是将此类代码放入 `IHostedService` 实现中。

## <a name="references"></a>参考

- [IIS 7 的 ASP.NET 应用程序生命周期概述](/previous-versions/aspnet/bb470252(v=vs.100))
- [IIS 5 和6的 ASP.NET 应用程序生命周期概述](/previous-versions/aspnet/ms178473(v=vs.100))
- [OWIN 和 Katana 入门](/aspnet/aspnet/overview/owin-and-katana/getting-started-with-owin-and-katana)
- [WebActivator](https://github.com/davidebbo/WebActivator)
- [ASP.NET Core 中的应用程序启动](/aspnet/core/fundamentals/startup?preserve-view=true&view=aspnetcore-3.1)
- [ASP.NET Core 中的 .NET 通用主机](/aspnet/core/fundamentals/host/generic-host?preserve-view=true&view=aspnetcore-3.1)
- [IHostedService](../microservices/multi-container-microservice-net-applications/background-tasks-with-ihostedservice.md)

>[!div class="step-by-step"]
>[上一页](architectural-differences.md)
>[下一页](hosting-differences.md)
