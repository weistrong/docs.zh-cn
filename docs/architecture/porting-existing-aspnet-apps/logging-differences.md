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
# <a name="logging-differences-between-aspnet-mvc-and-aspnet-core"></a>记录 ASP.NET MVC 和 ASP.NET Core 之间的差异

应用程序日志记录提供重要的诊断信息，尤其是对于在生产环境中运行的应用。 ASP.NET Core 引入了一个新系统，用于向任何应用添加标准化日志记录。 现有的 ASP.NET MVC 和 Web API 应用程序很可能会使用第三方日志记录解决方案，这些解决方案可能会继续 ASP.NET Core。

## <a name="aspnet-mvc-logging"></a>ASP.NET MVC 日志记录

ASP.NET MVC 和 Web API 应用中没有内置的日志记录解决方案。 而大多数应用程序都使用第三方日志记录解决方案，例如 [log4net](https://www.nuget.org/packages/log4net/)、 [NLog](https://www.nuget.org/packages/NLog/)或 [Serilog](https://www.nuget.org/packages/Serilog)。 许多团队还选择滚动自己的日志记录解决方案。 日志记录框架通常支持多个 "接收器" (或目标或追加器) 用于日志输出，例如文本文件、数据库甚至是电子邮件。 它们使用配置来确定哪些级别的系统将哪些日志消息路由到不同的接收器。 考虑如何将应用的日志记录迁移到 .NET Core 时，请查看在应用中执行和 [配置](configuration-differences.md) 日志记录的方式。

## <a name="aspnet-core-logging"></a>ASP.NET Core 日志记录

在 ASP.NET Core 中， [日志记录是一项内置功能](/aspnet/core/fundamentals/logging/) ，可在应用启动时进行配置和扩展。 第三方记录器（包括上面提到的程序）可以与 ASP.NET Core 集成，以增强其功能。

ASP.NET Core 日志记录使用类别和级别来控制要记录的内容和方式。 类通常使用接口的实例 `ILogger<T>` ，类的类型用作泛型 `T` 类型。 在此方案中，该类的完全限定名称用作类别。 还可以使用自定义类别创建记录器 `ILoggerFactory` 。 日志级别范围从最详细的 `Trace` 到最重要的 `Critical` 。 使用配置，应用可以指定每个类别 (的最小日志记录级别，每个类别包含) 的通配符。

默认情况下，典型的日志记录配置可能会记录 `Information` 和以上信息，但仅限 `Warning` 或更高的 `Microsoft` 类别：

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

对 ASP.NET Core 中的日志记录的支持广泛而灵活。 有关更多详细信息，请 [参阅文档](/aspnet/core/fundamentals/logging/)。

## <a name="migrate-logging"></a>迁移日志记录

如何将 .NET Framework 应用的日志记录迁移到 .NET Core 取决于应用现在的日志记录方式。 如果使用的是第三方 NuGet 包，请参阅该程序包的升级文档。 最可能的升级路径将非常简单。 如果要使用自己的日志记录解决方案，请执行以下操作之一：

1. 自行迁移日志记录解决方案
1. 迁移到第三方日志记录解决方案
1. 在 ASP.NET Core 中使用内置日志记录支持

可以 `Microsoft.Extensions.Logging` 从 .NET Framework 应用引用包，只要它们使用的是 NuGet 4.3 或更高版本，并且在 .NET Framework 4.6.1 或更高版本上。 应用引用此包后，可以在将应用迁移到 .NET Core 之前，转换日志记录语句以使用新的扩展。 这可以提供完整迁移的单步石头，因为应用程序可以继续在 .NET Framework 上运行，同时使用较新的扩展包进行日志记录。

## <a name="references"></a>参考

- [.NET Core 和 ASP.NET Core 中的日志记录](/aspnet/core/fundamentals/logging/)
- [Microsoft Extension. 日志记录 NuGet 包](https://www.nuget.org/packages/microsoft.extensions.logging/)

>[!div class="step-by-step"]
>[上一页](middleware-modules-handlers.md)
>[下一页](routing-differences.md)
