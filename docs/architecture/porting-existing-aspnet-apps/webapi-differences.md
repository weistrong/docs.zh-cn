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
# <a name="compare-aspnet-web-api-2-and-aspnet-core"></a><span data-ttu-id="0a3e3-103">比较 ASP.NET Web API 2 和 ASP.NET Core</span><span class="sxs-lookup"><span data-stu-id="0a3e3-103">Compare ASP.NET Web API 2 and ASP.NET Core</span></span>

<span data-ttu-id="0a3e3-104">ASP.NET Core 提供对 ASP.NET Web API 2 的迭代改进，但对于使用 Web API 2 的开发人员来说，应该很熟悉。</span><span class="sxs-lookup"><span data-stu-id="0a3e3-104">ASP.NET Core offers iterative improvements to ASP.NET Web API 2, but should feel familiar to developers who have used Web API 2.</span></span> <span data-ttu-id="0a3e3-105">ASP.NET Web API 2 与 ASP.NET MVC 一起开发和发运。</span><span class="sxs-lookup"><span data-stu-id="0a3e3-105">ASP.NET Web API 2 was developed and shipped alongside ASP.NET MVC.</span></span> <span data-ttu-id="0a3e3-106">这意味着，这两种方法具有类似但又不同的方法，如属性路由和依赖关系注入。</span><span class="sxs-lookup"><span data-stu-id="0a3e3-106">This meant the two approaches had similar-but-different approaches to things like attribute routing and dependency injection.</span></span> <span data-ttu-id="0a3e3-107">在 ASP.NET Core 中，MVC 和 Web Api 之间不再有任何区别。</span><span class="sxs-lookup"><span data-stu-id="0a3e3-107">In ASP.NET Core, there's no longer any distinction between MVC and Web APIs.</span></span> <span data-ttu-id="0a3e3-108">只有 ASP.NET MVC，它包括对基于视图的方案、API 终结点和 Razor Pages (和其他变体（如运行状况检查和 SignalR) ）的支持。</span><span class="sxs-lookup"><span data-stu-id="0a3e3-108">There's only ASP.NET MVC, which includes support for view-based scenarios, API endpoints, and Razor Pages (and other variations like health checks and SignalR).</span></span>

<span data-ttu-id="0a3e3-109">除了在 ASP.NET Core 中保持一致和统一外，在 .NET Core 中生成的 Api 比 ASP.NET Web API 2 上构建的 Api 更容易测试。</span><span class="sxs-lookup"><span data-stu-id="0a3e3-109">In addition to being consistent and unified within ASP.NET Core, APIs built in .NET Core are much easier to test than those built on ASP.NET Web API 2.</span></span> <span data-ttu-id="0a3e3-110">稍后我们将更详细地介绍这些 [差异](testing-differences.md) 。</span><span class="sxs-lookup"><span data-stu-id="0a3e3-110">We'll cover [testing differences](testing-differences.md) in more detail in a moment.</span></span> <span data-ttu-id="0a3e3-111">内置的支持在可创建的应用程序中承载 ASP.NET Core 应用程序，该程序可以创建一个用于 `HttpClient` 对应用程序进行内存中请求的应用程序，这在自动测试方面是一项巨大的好处。</span><span class="sxs-lookup"><span data-stu-id="0a3e3-111">The built-in support for hosting ASP.NET Core apps, in a test host that can create an `HttpClient` that makes in-memory requests to the app, is a huge benefit when it comes to automated testing.</span></span>

<span data-ttu-id="0a3e3-112">从 ASP.NET Web API 2 迁移到 ASP.NET Core 时，转换非常简单。</span><span class="sxs-lookup"><span data-stu-id="0a3e3-112">When migrating from ASP.NET Web API 2 to ASP.NET Core, the transition is straightforward.</span></span> <span data-ttu-id="0a3e3-113">如果有大的臃肿控制器，可以考虑使用 [ApiEndpoints](https://www.nuget.org/packages/Ardalis.ApiEndpoints/) NuGet 包的一种方法。</span><span class="sxs-lookup"><span data-stu-id="0a3e3-113">If you have large, bloated controllers, one approach you may consider to break them up is the use of the [Ardalis.ApiEndpoints](https://www.nuget.org/packages/Ardalis.ApiEndpoints/) NuGet packages.</span></span> <span data-ttu-id="0a3e3-114">此包将每个终结点分解为其自己的特定类，并根据需要关联的请求和响应类型。</span><span class="sxs-lookup"><span data-stu-id="0a3e3-114">This package breaks up each endpoint into its own specific class, with associated request and response types as appropriate.</span></span> <span data-ttu-id="0a3e3-115">这种方法具有与 [基于视图的代码组织 Razor Pages 提供的许多相同的优势](comparing-razor-pages-aspnet-mvc.md)。</span><span class="sxs-lookup"><span data-stu-id="0a3e3-115">This approach yields many of [the same benefits as Razor Pages offer over view-based code organization](comparing-razor-pages-aspnet-mvc.md).</span></span>

## <a name="references"></a><span data-ttu-id="0a3e3-116">参考</span><span class="sxs-lookup"><span data-stu-id="0a3e3-116">References</span></span>

- [<span data-ttu-id="0a3e3-117">从 ASP.NET Web API 迁移到 ASP.NET Core</span><span class="sxs-lookup"><span data-stu-id="0a3e3-117">Migrate from ASP.NET Web API to ASP.NET Core</span></span>](/aspnet/core/migration/webapi)
- [<span data-ttu-id="0a3e3-118">Ardalis. ApiEndpoints NuGet 包</span><span class="sxs-lookup"><span data-stu-id="0a3e3-118">Ardalis.ApiEndpoints NuGet package</span></span>](https://www.nuget.org/packages/Ardalis.ApiEndpoints/)

>[!div class="step-by-step"]
><span data-ttu-id="0a3e3-119">[上一页](comparing-razor-pages-aspnet-mvc.md)
>[下一页](authentication-differences.md)</span><span class="sxs-lookup"><span data-stu-id="0a3e3-119">[Previous](comparing-razor-pages-aspnet-mvc.md)
[Next](authentication-differences.md)</span></span>
