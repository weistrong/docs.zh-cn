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
# <a name="app-startup-differences-between-aspnet-mvc-and-aspnet-core"></a><span data-ttu-id="1ba23-104">ASP.NET MVC 和 ASP.NET Core 之间的应用启动差异</span><span class="sxs-lookup"><span data-stu-id="1ba23-104">App startup differences between ASP.NET MVC and ASP.NET Core</span></span>

<span data-ttu-id="1ba23-105">ASP.NET MVC 应用程序完全位于 Internet Information Server (IIS) ，这是 Windows 操作系统上可用的主 web 服务器。</span><span class="sxs-lookup"><span data-stu-id="1ba23-105">ASP.NET MVC apps lived entirely within Internet Information Server (IIS), the primary web server available on Windows operating systems.</span></span> <span data-ttu-id="1ba23-106">与 ASP.NET MVC 不同，ASP.NET Core 应用是可执行应用。</span><span class="sxs-lookup"><span data-stu-id="1ba23-106">Unlike ASP.NET MVC, ASP.NET Core apps are executable apps.</span></span> <span data-ttu-id="1ba23-107">您可以使用从命令行运行它们 `dotnet run` 。</span><span class="sxs-lookup"><span data-stu-id="1ba23-107">You can run them from the command line, using `dotnet run`.</span></span> <span data-ttu-id="1ba23-108">它们具有类似于所有 c # 程序的入口点方法，通常 `public static void Main()` 或类似的变体 (可能包含参数或 `async` 支持) 。</span><span class="sxs-lookup"><span data-stu-id="1ba23-108">They have an entry point method like all C# programs, typically `public static void Main()` or a similar variation (perhaps with arguments or `async` support).</span></span> <span data-ttu-id="1ba23-109">这可能是 ASP.NET Core 与 ASP.NET MVC 之间最大的体系结构差异，并且是允许 ASP.NET Core 在非 Windows 系统上运行的几个不同之处。</span><span class="sxs-lookup"><span data-stu-id="1ba23-109">This is perhaps the biggest architectural difference between ASP.NET Core and ASP.NET MVC, and is one of several differences that allows ASP.NET Core to run on non-Windows systems.</span></span>

## <a name="aspnet-mvc-startup"></a><span data-ttu-id="1ba23-110">ASP.NET MVC 启动</span><span class="sxs-lookup"><span data-stu-id="1ba23-110">ASP.NET MVC Startup</span></span>

<span data-ttu-id="1ba23-111">在 IIS 中承载时，ASP.NET apps 依赖 IIS 来实例化某些对象并在请求到达时调用某些方法。</span><span class="sxs-lookup"><span data-stu-id="1ba23-111">Hosted within IIS, ASP.NET apps rely on IIS to instantiate certain objects and call certain methods when a request arrives.</span></span> <span data-ttu-id="1ba23-112">ASP.NET 创建从派生的 *global.asax* 文件的类的实例 `HttpApplication` 。</span><span class="sxs-lookup"><span data-stu-id="1ba23-112">ASP.NET creates an instance of the *Global.asax* file's class, which derives from `HttpApplication`.</span></span> <span data-ttu-id="1ba23-113">收到第一个请求时，在处理请求本身之前，ASP.NET 将调用 `Application_Start` *global.asax* 文件的类中的方法。</span><span class="sxs-lookup"><span data-stu-id="1ba23-113">When the first request is received, before handling the request itself, ASP.NET calls the `Application_Start` method in the *Global.asax* file's class.</span></span> <span data-ttu-id="1ba23-114">任何需要在 ASP.NET MVC 应用开始时运行的逻辑都可以添加到此方法中。</span><span class="sxs-lookup"><span data-stu-id="1ba23-114">Any logic that needs to run when the ASP.NET MVC app begins can be added to this method.</span></span>

<span data-ttu-id="1ba23-115">许多用于 ASP.NET MVC 和 Web API 的 NuGet 包使用 [WebActivator](https://github.com/davidebbo/WebActivator) 包，使其在应用启动期间运行一些代码。</span><span class="sxs-lookup"><span data-stu-id="1ba23-115">Many NuGet packages for ASP.NET MVC and Web API use the [WebActivator](https://github.com/davidebbo/WebActivator) package to let them run some code during app startup.</span></span> <span data-ttu-id="1ba23-116">按照约定，通常会将此代码添加到 *App_Start* 文件夹，并通过属性将其配置为在紧挨之前或之后运行 `Application_Start` 。</span><span class="sxs-lookup"><span data-stu-id="1ba23-116">By convention, this code would typically be added to an *App_Start* folder and would be configured via attribute to run either immediately before or just after `Application_Start`.</span></span>

<span data-ttu-id="1ba23-117">还可以通过 [ASP.NET MVC 使用适用于 .net (OWIN) 和 Project Katana 的开放 Web 接口](/aspnet/aspnet/overview/owin-and-katana/getting-started-with-owin-and-katana)。</span><span class="sxs-lookup"><span data-stu-id="1ba23-117">It's also possible to use the [Open Web Interface for .NET (OWIN) and Project Katana with ASP.NET MVC](/aspnet/aspnet/overview/owin-and-katana/getting-started-with-owin-and-katana).</span></span> <span data-ttu-id="1ba23-118">执行此操作时，应用程序将包含一个 *Startup.cs* 文件，该文件负责设置请求中间件，其方式与 ASP.NET Core 行为方式非常类似。</span><span class="sxs-lookup"><span data-stu-id="1ba23-118">When doing so, the app will include a *Startup.cs* file that is responsible for setting up request middleware in a way that's very similar to how ASP.NET Core behaves.</span></span>

<span data-ttu-id="1ba23-119">如果你需要在 ASP.NET MVC 应用启动时运行代码，则它通常将使用以下方法之一。</span><span class="sxs-lookup"><span data-stu-id="1ba23-119">If you need to run code when your ASP.NET MVC app starts up, it will typically use one of these approaches.</span></span>

## <a name="aspnet-core-startup"></a><span data-ttu-id="1ba23-120">ASP.NET Core 启动</span><span class="sxs-lookup"><span data-stu-id="1ba23-120">ASP.NET Core Startup</span></span>

<span data-ttu-id="1ba23-121">如前所述，ASP.NET Core 应用是独立的程序。</span><span class="sxs-lookup"><span data-stu-id="1ba23-121">As noted previously, ASP.NET Core apps are standalone programs.</span></span> <span data-ttu-id="1ba23-122">这种情况下，它们通常包含一个 *Program.cs* 文件，其中包含应用程序的入口点。</span><span class="sxs-lookup"><span data-stu-id="1ba23-122">As such, they typically include a *Program.cs* file containing the entry point for the app.</span></span> <span data-ttu-id="1ba23-123">此文件的典型示例如图2-1 所示。</span><span class="sxs-lookup"><span data-stu-id="1ba23-123">A typical example of this file is shown in Figure 2-1.</span></span>

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

<span data-ttu-id="1ba23-124">**图 2-1**.</span><span class="sxs-lookup"><span data-stu-id="1ba23-124">**Figure 2-1**.</span></span> <span data-ttu-id="1ba23-125">典型 ASP.NET Core *Program.cs* 文件。</span><span class="sxs-lookup"><span data-stu-id="1ba23-125">A typical ASP.NET Core *Program.cs* file.</span></span>

<span data-ttu-id="1ba23-126">图2-1 中所示的代码为应用程序创建 *主机* ，生成应用程序并运行它。</span><span class="sxs-lookup"><span data-stu-id="1ba23-126">The code shown in Figure 2-1 creates a *host* for the app, builds it, and runs it.</span></span> <span data-ttu-id="1ba23-127">ASP.NET Core 应用在由所示的配置的主机中运行 `IHostBuilder` 。</span><span class="sxs-lookup"><span data-stu-id="1ba23-127">The ASP.NET Core app runs within the host configured by the `IHostBuilder` shown.</span></span> <span data-ttu-id="1ba23-128">尽管可以使用完全配置 ASP.NET Core 应用程序，但这种 `IHostBuilder` 情况通常是在类中完成的 `Startup` 。</span><span class="sxs-lookup"><span data-stu-id="1ba23-128">While it's possible to completely configure an ASP.NET Core app using the `IHostBuilder`, typically the bulk of this work is done in a `Startup` class.</span></span>

<span data-ttu-id="1ba23-129">`Startup`类向宿主公开两个方法： `ConfigureServices` 和 `Configure` 。</span><span class="sxs-lookup"><span data-stu-id="1ba23-129">The `Startup` class exposes two methods to the host: `ConfigureServices` and `Configure`.</span></span> <span data-ttu-id="1ba23-130">`ConfigureServices`方法用于定义应用将使用的服务及其各自的生存期。</span><span class="sxs-lookup"><span data-stu-id="1ba23-130">The `ConfigureServices` method is used to define the services the app will use and their respective lifetimes.</span></span> <span data-ttu-id="1ba23-131">`Configure`方法用于定义如何通过设置由中间件组成的请求管道来处理对应用程序的每个请求。</span><span class="sxs-lookup"><span data-stu-id="1ba23-131">The `Configure` method is used to define how each request to the app will be handled by setting up a request pipeline composed of middleware.</span></span>

<span data-ttu-id="1ba23-132">除了与配置应用服务或请求管道相关的代码以外，应用程序可能还具有应用启动时必须运行的其他代码。</span><span class="sxs-lookup"><span data-stu-id="1ba23-132">In addition to code related to configuring the app's services or request pipeline, apps may have other code that must run when the app begins.</span></span> <span data-ttu-id="1ba23-133">此类代码通常放置在 *Program.cs* 中或注册为 `IHostedService` ，这会在应用程序启动时由 [通用主机](/aspnet/core/fundamentals/host/generic-host?preserve-view=true&view=aspnetcore-3.1) 启动。</span><span class="sxs-lookup"><span data-stu-id="1ba23-133">Such code is typically placed in *Program.cs* or registered as an `IHostedService`, which will be started by the [generic host](/aspnet/core/fundamentals/host/generic-host?preserve-view=true&view=aspnetcore-3.1) when the app starts.</span></span>

<span data-ttu-id="1ba23-134">`IHostedService`接口只公开两个方法： `StartAsync` 和 `StopAsync` 。</span><span class="sxs-lookup"><span data-stu-id="1ba23-134">The `IHostedService` interface just exposes two methods, `StartAsync` and `StopAsync`.</span></span> <span data-ttu-id="1ba23-135">在中注册接口， `ConfigureServices` 主机会执行其他工作，在 `StartAsync` 应用启动之前调用方法。</span><span class="sxs-lookup"><span data-stu-id="1ba23-135">You register the interface in `ConfigureServices` and the host does the rest, calling the `StartAsync` method before the app starts up.</span></span>

## <a name="porting-considerations"></a><span data-ttu-id="1ba23-136">移植注意事项</span><span class="sxs-lookup"><span data-stu-id="1ba23-136">Porting considerations</span></span>

<span data-ttu-id="1ba23-137">希望将其应用从 ASP.NET MVC 迁移到 ASP.NET Core 的团队需要确定在应用程序启动时运行的代码，并确定此类代码在其 ASP.NET Core 应用中的适当位置。</span><span class="sxs-lookup"><span data-stu-id="1ba23-137">Teams looking to migrate their apps from ASP.NET MVC to ASP.NET Core need to identify what code is being run when their app starts up and determine the appropriate location for such code in their ASP.NET Core app.</span></span> <span data-ttu-id="1ba23-138">对于需要在应用程序启动时运行的自定义代码，尤其是异步代码，建议的方法通常是将此类代码放入 `IHostedService` 实现中。</span><span class="sxs-lookup"><span data-stu-id="1ba23-138">For custom code needed to run when the app starts up, especially async code, the recommended approach is typically to put such code into `IHostedService` implementations.</span></span>

## <a name="references"></a><span data-ttu-id="1ba23-139">参考</span><span class="sxs-lookup"><span data-stu-id="1ba23-139">References</span></span>

- <span data-ttu-id="1ba23-140">[IIS 7 的 ASP.NET 应用程序生命周期概述](/previous-versions/aspnet/bb470252(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="1ba23-140">[ASP.NET Application Life Cycle Overview for IIS 7](/previous-versions/aspnet/bb470252(v=vs.100))</span></span>
- <span data-ttu-id="1ba23-141">[IIS 5 和6的 ASP.NET 应用程序生命周期概述](/previous-versions/aspnet/ms178473(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="1ba23-141">[ASP.NET Application Life Cycle Overview for IIS 5 and 6](/previous-versions/aspnet/ms178473(v=vs.100))</span></span>
- [<span data-ttu-id="1ba23-142">OWIN 和 Katana 入门</span><span class="sxs-lookup"><span data-stu-id="1ba23-142">Getting Started with OWIN and Katana</span></span>](/aspnet/aspnet/overview/owin-and-katana/getting-started-with-owin-and-katana)
- [<span data-ttu-id="1ba23-143">WebActivator</span><span class="sxs-lookup"><span data-stu-id="1ba23-143">WebActivator</span></span>](https://github.com/davidebbo/WebActivator)
- [<span data-ttu-id="1ba23-144">ASP.NET Core 中的应用程序启动</span><span class="sxs-lookup"><span data-stu-id="1ba23-144">App Startup in ASP.NET Core</span></span>](/aspnet/core/fundamentals/startup?preserve-view=true&view=aspnetcore-3.1)
- [<span data-ttu-id="1ba23-145">ASP.NET Core 中的 .NET 通用主机</span><span class="sxs-lookup"><span data-stu-id="1ba23-145">.NET Generic Host in ASP.NET Core</span></span>](/aspnet/core/fundamentals/host/generic-host?preserve-view=true&view=aspnetcore-3.1)
- [<span data-ttu-id="1ba23-146">IHostedService</span><span class="sxs-lookup"><span data-stu-id="1ba23-146">IHostedService</span></span>](../microservices/multi-container-microservice-net-applications/background-tasks-with-ihostedservice.md)

>[!div class="step-by-step"]
><span data-ttu-id="1ba23-147">[上一页](architectural-differences.md)
>[下一页](hosting-differences.md)</span><span class="sxs-lookup"><span data-stu-id="1ba23-147">[Previous](architectural-differences.md)
[Next](hosting-differences.md)</span></span>
