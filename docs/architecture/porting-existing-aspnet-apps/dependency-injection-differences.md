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
# <a name="dependency-injection-differences-between-aspnet-mvc-and-aspnet-core"></a><span data-ttu-id="3dc14-103">ASP.NET MVC 和 ASP.NET Core 之间的依赖关系注入差异</span><span class="sxs-lookup"><span data-stu-id="3dc14-103">Dependency injection differences between ASP.NET MVC and ASP.NET Core</span></span>

<span data-ttu-id="3dc14-104">尽管依赖关系注入 (DI) 未内置于 ASP.NET MVC 或 Web API 中，但很多应用通过添加具有反转 (IOC) 容器的 NuGet 包来启用它。</span><span class="sxs-lookup"><span data-stu-id="3dc14-104">Although dependency injection (DI) isn't built into ASP.NET MVC or Web API, many apps enable it by adding a NuGet package with an inversion of control (IOC) container.</span></span> <span data-ttu-id="3dc14-105">对于依赖关系注入 (或反转) ，这些容器有时称为 DI 容器。</span><span class="sxs-lookup"><span data-stu-id="3dc14-105">These are sometimes referred to as DI containers, for dependency injection (or inversion).</span></span> <span data-ttu-id="3dc14-106">ASP.NET MVC 应用中使用的一些最常用的容器包括：</span><span class="sxs-lookup"><span data-stu-id="3dc14-106">Some of the most popular containers used in ASP.NET MVC apps include:</span></span>

- [<span data-ttu-id="3dc14-107">Autofac</span><span class="sxs-lookup"><span data-stu-id="3dc14-107">Autofac</span></span>](https://www.autofac.org/)
- [<span data-ttu-id="3dc14-108">Unity</span><span class="sxs-lookup"><span data-stu-id="3dc14-108">Unity</span></span>](https://unitycontainer.github.io/)
- [<span data-ttu-id="3dc14-109">Ninject</span><span class="sxs-lookup"><span data-stu-id="3dc14-109">Ninject</span></span>](http://www.ninject.org/)
- <span data-ttu-id="3dc14-110">[StructureMap](http://structuremap.github.io/) *(弃用)*</span><span class="sxs-lookup"><span data-stu-id="3dc14-110">[StructureMap](http://structuremap.github.io/) *(deprecated)*</span></span>
- [<span data-ttu-id="3dc14-111">城堡 Windsor</span><span class="sxs-lookup"><span data-stu-id="3dc14-111">Castle Windsor</span></span>](http://www.castleproject.org/projects/windsor/)

<span data-ttu-id="3dc14-112">如果你的 ASP.NET MVC 应用未使用 DI，你可能想要在 ASP.NET Core 中调查对 DI 的内置支持。</span><span class="sxs-lookup"><span data-stu-id="3dc14-112">If your ASP.NET MVC app isn't using DI, you will probably want to investigate the built-in support for DI in ASP.NET Core.</span></span> <span data-ttu-id="3dc14-113">DI 提升了应用中模块的松散耦合，实现了更好的可测试性，并遵循 [实体](https://www.weeklydevtips.com/episodes/047)等原则。</span><span class="sxs-lookup"><span data-stu-id="3dc14-113">DI promotes loose coupling of modules in your app and enables better testability and adherence to principles like [SOLID](https://www.weeklydevtips.com/episodes/047).</span></span>

<span data-ttu-id="3dc14-114">如果你的应用程序使用 DI，则最好的做法是查看你使用的容器是否支持 ASP.NET Core。</span><span class="sxs-lookup"><span data-stu-id="3dc14-114">If your app does use DI, then probably your best course of action is to see if the container you're using supports ASP.NET Core.</span></span> <span data-ttu-id="3dc14-115">如果是这样，您可以继续使用它，以及描述您的类型映射和生存期的自定义配置规则。</span><span class="sxs-lookup"><span data-stu-id="3dc14-115">If so, you may be able to continue using it and your custom configuration rules describing your type mappings and lifetimes.</span></span>

<span data-ttu-id="3dc14-116">无论采用哪种方式，都应考虑使用 ASP.NET Core 附带的 DI 的内置支持，因为它可能满足应用程序的需求。</span><span class="sxs-lookup"><span data-stu-id="3dc14-116">Either way, you should consider using the built-in support for DI that ships with ASP.NET Core, as it may meet your app's needs.</span></span>

## <a name="dependency-injection-in-aspnet-core"></a><span data-ttu-id="3dc14-117">ASP.NET Core 依赖注入</span><span class="sxs-lookup"><span data-stu-id="3dc14-117">Dependency injection in ASP.NET Core</span></span>

<span data-ttu-id="3dc14-118">ASP.NET Core 假定应用将使用 DI。</span><span class="sxs-lookup"><span data-stu-id="3dc14-118">ASP.NET Core assumes apps will use DI.</span></span> <span data-ttu-id="3dc14-119">它不只是内置于框架中，而是必需的，以便将对框架功能的支持引入 ASP.NET Core 应用。</span><span class="sxs-lookup"><span data-stu-id="3dc14-119">It's not just built into the framework, but is required in order to bring support for framework features into your ASP.NET Core apps.</span></span> <span data-ttu-id="3dc14-120">在应用程序启动中，将调用， `ConfigureServices` 该调用负责注册 DI 容器 (服务收集/服务提供程序) 可以创建并注入到应用中的所有类型。</span><span class="sxs-lookup"><span data-stu-id="3dc14-120">In app startup, a call is made to `ConfigureServices` which is responsible for registering all of the types that the DI container (service collection/service provider) can create and inject in the app.</span></span> <span data-ttu-id="3dc14-121">内置 ASP.NET Core 功能，如 Entity Framework Core、标识甚至是 MVC，只需在方法中将其配置为服务即可 `ConfigureServices` 。</span><span class="sxs-lookup"><span data-stu-id="3dc14-121">Built-in ASP.NET Core features like Entity Framework Core, Identity, and even MVC are brought into the app by configuring them as services in the `ConfigureServices` method.</span></span>

<span data-ttu-id="3dc14-122">除了使用默认实现外，应用程序还可以使用自定义容器。</span><span class="sxs-lookup"><span data-stu-id="3dc14-122">In addition to using the default implementation, apps can still use custom containers.</span></span> <span data-ttu-id="3dc14-123">本 [文档介绍如何替换默认的服务容器](../../core/extensions/dependency-injection-guidelines.md#default-service-container-replacement)。</span><span class="sxs-lookup"><span data-stu-id="3dc14-123">The [documentation covers how to replace the default service container](../../core/extensions/dependency-injection-guidelines.md#default-service-container-replacement).</span></span>

<span data-ttu-id="3dc14-124">DI 是 ASP.NET Core 的基础。</span><span class="sxs-lookup"><span data-stu-id="3dc14-124">DI is fundamental to ASP.NET Core.</span></span> <span data-ttu-id="3dc14-125">如果你的团队在此练习中尚未精通，则在迁移应用之前，你需要了解它。</span><span class="sxs-lookup"><span data-stu-id="3dc14-125">If your team isn't already well-versed in this practice, you'll want to understand it before porting your app.</span></span>

## <a name="references"></a><span data-ttu-id="3dc14-126">参考</span><span class="sxs-lookup"><span data-stu-id="3dc14-126">References</span></span>

- [<span data-ttu-id="3dc14-127">.NET 中的依赖项注入</span><span class="sxs-lookup"><span data-stu-id="3dc14-127">Dependency Injection in .NET</span></span>](../../core/extensions/dependency-injection.md)
- [<span data-ttu-id="3dc14-128">ASP.NET Core 中的依赖项注入</span><span class="sxs-lookup"><span data-stu-id="3dc14-128">Dependency Injection in ASP.NET Core</span></span>](/aspnet/core/fundamentals/dependency-injection)

>[!div class="step-by-step"]
><span data-ttu-id="3dc14-129">[上一页](serving-static-files.md)
>[下一页](middleware-modules-handlers.md)</span><span class="sxs-lookup"><span data-stu-id="3dc14-129">[Previous](serving-static-files.md)
[Next](middleware-modules-handlers.md)</span></span>
