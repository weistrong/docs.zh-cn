---
title: ASP.NET MVC 和 ASP.NET Core 之间的依赖关系注入差异
description: 了解依赖关系注入在 ASP.NET MVC 和 ASP.NET Core 中的工作原理，它们有何不同，以及如何从 ASP.NET MVC 迁移到 ASP.NET Core。
author: ardalis
ms.date: 11/13/2020
ms.openlocfilehash: aa1c7dd2f70e1a545352feb6560177bc6e2baa2d
ms.sourcegitcommit: 42d436ebc2a7ee02fc1848c7742bc7d80e13fc2f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/04/2021
ms.locfileid: "102401086"
---
# <a name="dependency-injection-differences-between-aspnet-mvc-and-aspnet-core"></a>ASP.NET MVC 和 ASP.NET Core 之间的依赖关系注入差异

尽管依赖关系注入 (DI) 未内置于 ASP.NET MVC 或 Web API 中，但很多应用通过添加具有反转 (IOC) 容器的 NuGet 包来启用它。 对于依赖关系注入 (或反转) ，这些容器有时称为 DI 容器。 ASP.NET MVC 应用中使用的一些最常用的容器包括：

- [Autofac](https://www.autofac.org/)
- [Unity](https://unitycontainer.github.io/)
- [Ninject](http://www.ninject.org/)
- [StructureMap](http://structuremap.github.io/) *(弃用)*
- [城堡 Windsor](http://www.castleproject.org/projects/windsor/)

如果你的 ASP.NET MVC 应用未使用 DI，你可能想要在 ASP.NET Core 中调查对 DI 的内置支持。 DI 提升了应用中模块的松散耦合，实现了更好的可测试性，并遵循 [实体](https://www.weeklydevtips.com/episodes/047)等原则。

如果你的应用程序使用 DI，则最好的做法是查看你使用的容器是否支持 ASP.NET Core。 如果是这样，您可以继续使用它，以及描述您的类型映射和生存期的自定义配置规则。

无论采用哪种方式，都应考虑使用 ASP.NET Core 附带的 DI 的内置支持，因为它可能满足应用程序的需求。

## <a name="dependency-injection-in-aspnet-core"></a>ASP.NET Core 依赖注入

ASP.NET Core 假定应用将使用 DI。 它不只是内置于框架中，而是必需的，以便将对框架功能的支持引入 ASP.NET Core 应用。 在应用程序启动中，将调用， `ConfigureServices` 该调用负责注册 DI 容器 (服务收集/服务提供程序) 可以创建并注入到应用中的所有类型。 内置 ASP.NET Core 功能，如 Entity Framework Core、标识甚至是 MVC，只需在方法中将其配置为服务即可 `ConfigureServices` 。

除了使用默认实现外，应用程序还可以使用自定义容器。 本 [文档介绍如何替换默认的服务容器](../../core/extensions/dependency-injection-guidelines.md#default-service-container-replacement)。

DI 是 ASP.NET Core 的基础。 如果你的团队在此练习中尚未精通，则在迁移应用之前，你需要了解它。

## <a name="references"></a>参考

- [.NET 中的依赖项注入](../../core/extensions/dependency-injection.md)
- [ASP.NET Core 中的依赖项注入](/aspnet/core/fundamentals/dependency-injection)

>[!div class="step-by-step"]
>[上一页](serving-static-files.md)
>[下一页](middleware-modules-handlers.md)
