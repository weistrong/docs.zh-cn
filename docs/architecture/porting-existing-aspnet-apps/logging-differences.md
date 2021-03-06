---
title: 记录 ASP.NET MVC 和 ASP.NET Core 之间的差异
description: ASP.NET MVC 和 Web API 应用与 ASP.NET Core 应用之间有何不同？
author: ardalis
ms.date: 11/13/2020
ms.openlocfilehash: 0ad12463c8d13d13516ab027e56f809b67f713e4
ms.sourcegitcommit: 42d436ebc2a7ee02fc1848c7742bc7d80e13fc2f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/04/2021
ms.locfileid: "102401072"
---
# <a name="logging-differences-between-aspnet-mvc-and-aspnet-core"></a><span data-ttu-id="a93fe-103">记录 ASP.NET MVC 和 ASP.NET Core 之间的差异</span><span class="sxs-lookup"><span data-stu-id="a93fe-103">Logging differences between ASP.NET MVC and ASP.NET Core</span></span>

<span data-ttu-id="a93fe-104">应用程序日志记录提供重要的诊断信息，尤其是对于在生产环境中运行的应用。</span><span class="sxs-lookup"><span data-stu-id="a93fe-104">Application logging provides important diagnostic information, especially for apps running in production.</span></span> <span data-ttu-id="a93fe-105">ASP.NET Core 引入了一个新系统，用于向任何应用添加标准化日志记录。</span><span class="sxs-lookup"><span data-stu-id="a93fe-105">ASP.NET Core introduces a new system for adding standardized logging to any app.</span></span> <span data-ttu-id="a93fe-106">现有的 ASP.NET MVC 和 Web API 应用程序很可能会使用第三方日志记录解决方案，这些解决方案可能会继续 ASP.NET Core。</span><span class="sxs-lookup"><span data-stu-id="a93fe-106">Existing ASP.NET MVC and Web API apps most likely use third-party logging solutions, which likely continue to be supported on ASP.NET Core.</span></span>

## <a name="aspnet-mvc-logging"></a><span data-ttu-id="a93fe-107">ASP.NET MVC 日志记录</span><span class="sxs-lookup"><span data-stu-id="a93fe-107">ASP.NET MVC logging</span></span>

<span data-ttu-id="a93fe-108">ASP.NET MVC 和 Web API 应用中没有内置的日志记录解决方案。</span><span class="sxs-lookup"><span data-stu-id="a93fe-108">There's no built-in logging solution in ASP.NET MVC and Web API apps.</span></span> <span data-ttu-id="a93fe-109">而大多数应用程序都使用第三方日志记录解决方案，例如 [log4net](https://www.nuget.org/packages/log4net/)、 [NLog](https://www.nuget.org/packages/NLog/)或 [Serilog](https://www.nuget.org/packages/Serilog)。</span><span class="sxs-lookup"><span data-stu-id="a93fe-109">Instead, most apps use third-party logging solutions like [log4net](https://www.nuget.org/packages/log4net/), [NLog](https://www.nuget.org/packages/NLog/), or [Serilog](https://www.nuget.org/packages/Serilog).</span></span> <span data-ttu-id="a93fe-110">许多团队还选择滚动自己的日志记录解决方案。</span><span class="sxs-lookup"><span data-stu-id="a93fe-110">Many teams also choose to roll their own logging solution.</span></span> <span data-ttu-id="a93fe-111">日志记录框架通常支持多个 "接收器" (或目标或追加器) 用于日志输出，例如文本文件、数据库甚至是电子邮件。</span><span class="sxs-lookup"><span data-stu-id="a93fe-111">Logging frameworks typically support multiple "sinks" (or targets or appenders) for log output, such as text files, databases, or even emails.</span></span> <span data-ttu-id="a93fe-112">它们使用配置来确定哪些级别的系统将哪些日志消息路由到不同的接收器。</span><span class="sxs-lookup"><span data-stu-id="a93fe-112">They use configuration to determine which levels of log messages from which parts of the system are routed to different sinks.</span></span> <span data-ttu-id="a93fe-113">考虑如何将应用的日志记录迁移到 .NET Core 时，请查看在应用中执行和 [配置](configuration-differences.md) 日志记录的方式。</span><span class="sxs-lookup"><span data-stu-id="a93fe-113">When considering how to migrate an app's logging to .NET Core, review how logging is performed and [configured](configuration-differences.md) in the app.</span></span>

## <a name="aspnet-core-logging"></a><span data-ttu-id="a93fe-114">ASP.NET Core 日志记录</span><span class="sxs-lookup"><span data-stu-id="a93fe-114">ASP.NET Core logging</span></span>

<span data-ttu-id="a93fe-115">在 ASP.NET Core 中， [日志记录是一项内置功能](/aspnet/core/fundamentals/logging/) ，可在应用启动时进行配置和扩展。</span><span class="sxs-lookup"><span data-stu-id="a93fe-115">In ASP.NET Core, [logging is a built-in feature](/aspnet/core/fundamentals/logging/) that can be configured and extended when the app starts up.</span></span> <span data-ttu-id="a93fe-116">第三方记录器（包括上面提到的程序）可以与 ASP.NET Core 集成，以增强其功能。</span><span class="sxs-lookup"><span data-stu-id="a93fe-116">Third-party loggers, including those mentioned above, can be integrated with ASP.NET Core to enhance its functionality.</span></span>

<span data-ttu-id="a93fe-117">ASP.NET Core 日志记录使用类别和级别来控制要记录的内容和方式。</span><span class="sxs-lookup"><span data-stu-id="a93fe-117">ASP.NET Core logging uses categories and levels to control what is logged and how.</span></span> <span data-ttu-id="a93fe-118">类通常使用接口的实例 `ILogger<T>` ，类的类型用作泛型 `T` 类型。</span><span class="sxs-lookup"><span data-stu-id="a93fe-118">Classes typically use instances of the `ILogger<T>` interface, with the class's type used as the generic `T` type.</span></span> <span data-ttu-id="a93fe-119">在此方案中，该类的完全限定名称用作类别。</span><span class="sxs-lookup"><span data-stu-id="a93fe-119">In this scenario, the class's fully qualified name is used as the category.</span></span> <span data-ttu-id="a93fe-120">还可以使用自定义类别创建记录器 `ILoggerFactory` 。</span><span class="sxs-lookup"><span data-stu-id="a93fe-120">Loggers can also be created with a custom category using an `ILoggerFactory`.</span></span> <span data-ttu-id="a93fe-121">日志级别范围从最详细的 `Trace` 到最重要的 `Critical` 。</span><span class="sxs-lookup"><span data-stu-id="a93fe-121">Log levels range from the most detailed, `Trace`, to the most important, `Critical`.</span></span> <span data-ttu-id="a93fe-122">使用配置，应用可以指定每个类别 (的最小日志记录级别，每个类别包含) 的通配符。</span><span class="sxs-lookup"><span data-stu-id="a93fe-122">Using configuration, apps can specify what minimum level of logging should be included on a per-category (with wildcards) basis.</span></span>

<span data-ttu-id="a93fe-123">默认情况下，典型的日志记录配置可能会记录 `Information` 和以上信息，但仅限 `Warning` 或更高的 `Microsoft` 类别：</span><span class="sxs-lookup"><span data-stu-id="a93fe-123">A typical logging configuration could log `Information` and above information by default, but only `Warning` or above from `Microsoft`-prefixed categories:</span></span>

```json
{
  "Logging": {
    "LogLevel": {
      "Default": "Information",
      "Microsoft": "Warning"
    }
  }
}
```

<span data-ttu-id="a93fe-124">对 ASP.NET Core 中的日志记录的支持广泛而灵活。</span><span class="sxs-lookup"><span data-stu-id="a93fe-124">Support for logging in ASP.NET Core is extensive and flexible.</span></span> <span data-ttu-id="a93fe-125">有关更多详细信息，请 [参阅文档](/aspnet/core/fundamentals/logging/)。</span><span class="sxs-lookup"><span data-stu-id="a93fe-125">For more detailed information, [refer to the docs](/aspnet/core/fundamentals/logging/).</span></span>

## <a name="migrate-logging"></a><span data-ttu-id="a93fe-126">迁移日志记录</span><span class="sxs-lookup"><span data-stu-id="a93fe-126">Migrate logging</span></span>

<span data-ttu-id="a93fe-127">如何将 .NET Framework 应用的日志记录迁移到 .NET Core 取决于应用现在的日志记录方式。</span><span class="sxs-lookup"><span data-stu-id="a93fe-127">How you migrate your .NET Framework app's logging to .NET Core depends on how the app is logging now.</span></span> <span data-ttu-id="a93fe-128">如果使用的是第三方 NuGet 包，请参阅该程序包的升级文档。</span><span class="sxs-lookup"><span data-stu-id="a93fe-128">If it's using a third-party NuGet package, refer to the upgrade documentation for that package.</span></span> <span data-ttu-id="a93fe-129">最可能的升级路径将非常简单。</span><span class="sxs-lookup"><span data-stu-id="a93fe-129">Most likely the upgrade path will be fairly straightforward.</span></span> <span data-ttu-id="a93fe-130">如果要使用自己的日志记录解决方案，请执行以下操作之一：</span><span class="sxs-lookup"><span data-stu-id="a93fe-130">If you're using your own logging solution, take one of the following actions:</span></span>

1. <span data-ttu-id="a93fe-131">自行迁移日志记录解决方案</span><span class="sxs-lookup"><span data-stu-id="a93fe-131">Migrate the logging solution yourself</span></span>
1. <span data-ttu-id="a93fe-132">迁移到第三方日志记录解决方案</span><span class="sxs-lookup"><span data-stu-id="a93fe-132">Migrate to a third-party logging solution</span></span>
1. <span data-ttu-id="a93fe-133">在 ASP.NET Core 中使用内置日志记录支持</span><span class="sxs-lookup"><span data-stu-id="a93fe-133">Use the built-in logging support in ASP.NET Core</span></span>

<span data-ttu-id="a93fe-134">可以 `Microsoft.Extensions.Logging` 从 .NET Framework 应用引用包，只要它们使用的是 NuGet 4.3 或更高版本，并且在 .NET Framework 4.6.1 或更高版本上。</span><span class="sxs-lookup"><span data-stu-id="a93fe-134">You can reference the `Microsoft.Extensions.Logging` package from .NET Framework apps as long as they're using NuGet 4.3 or later and are on .NET Framework 4.6.1 or later.</span></span> <span data-ttu-id="a93fe-135">应用引用此包后，可以在将应用迁移到 .NET Core 之前，转换日志记录语句以使用新的扩展。</span><span class="sxs-lookup"><span data-stu-id="a93fe-135">Once your app has referenced this package, you can convert your logging statements to use the new extensions before migrating the app to .NET Core.</span></span> <span data-ttu-id="a93fe-136">这可以提供完整迁移的单步石头，因为应用程序可以继续在 .NET Framework 上运行，同时使用较新的扩展包进行日志记录。</span><span class="sxs-lookup"><span data-stu-id="a93fe-136">This can provide a stepping stone toward full migration, since the app can continue running on .NET Framework while logging using the newer extensions package.</span></span>

## <a name="references"></a><span data-ttu-id="a93fe-137">参考</span><span class="sxs-lookup"><span data-stu-id="a93fe-137">References</span></span>

- [<span data-ttu-id="a93fe-138">.NET Core 和 ASP.NET Core 中的日志记录</span><span class="sxs-lookup"><span data-stu-id="a93fe-138">Logging in .NET Core and ASP.NET Core</span></span>](/aspnet/core/fundamentals/logging/)
- [<span data-ttu-id="a93fe-139">Microsoft Extension. 日志记录 NuGet 包</span><span class="sxs-lookup"><span data-stu-id="a93fe-139">Microsoft.Extensions.Logging NuGet Package</span></span>](https://www.nuget.org/packages/microsoft.extensions.logging/)

>[!div class="step-by-step"]
><span data-ttu-id="a93fe-140">[上一页](middleware-modules-handlers.md)
>[下一页](routing-differences.md)</span><span class="sxs-lookup"><span data-stu-id="a93fe-140">[Previous](middleware-modules-handlers.md)
[Next](routing-differences.md)</span></span>
