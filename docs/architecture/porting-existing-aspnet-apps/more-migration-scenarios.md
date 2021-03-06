---
title: 更多迁移方案
description: 本部分介绍将 .NET Framework 应用升级到 .NET Core/.NET 5 的其他迁移方案和技术。
author: ardalis
ms.date: 02/11/2021
ms.openlocfilehash: fa1b756d8852854e50127ae3e7443e2949cceaa8
ms.sourcegitcommit: 42d436ebc2a7ee02fc1848c7742bc7d80e13fc2f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/04/2021
ms.locfileid: "102401068"
---
# <a name="more-migration-scenarios"></a><span data-ttu-id="c8983-103">更多迁移方案</span><span class="sxs-lookup"><span data-stu-id="c8983-103">More migration scenarios</span></span>

[!INCLUDE [book-preview](../../../includes/book-preview.md)]

<span data-ttu-id="c8983-104">本部分介绍了几种不同的 ASP.NET 应用方案，并提供了解决每个应用方案的特定方法。</span><span class="sxs-lookup"><span data-stu-id="c8983-104">This section describes several different ASP.NET app scenarios, and offers specific techniques for solving each of them.</span></span> <span data-ttu-id="c8983-105">你可以使用此部分来确定适用于你的应用程序的方案，并评估适用于你的应用程序及其宿主环境的哪些方法。</span><span class="sxs-lookup"><span data-stu-id="c8983-105">You can use this section to identify scenarios applicable to your app, and evaluate which techniques will work for your app and its hosting environment.</span></span>

## <a name="migrate-aspnet-mvc-5-and-webapi-2-to-aspnet-core-mvc"></a><span data-ttu-id="c8983-106">将 ASP.NET MVC 5 和 WebApi 2 迁移到 ASP.NET Core MVC</span><span class="sxs-lookup"><span data-stu-id="c8983-106">Migrate ASP.NET MVC 5 and WebApi 2 to ASP.NET Core MVC</span></span>

<span data-ttu-id="c8983-107">ASP.NET MVC 5 和 Web API 2 应用的常见方案是，这两个产品都安装在同一应用程序中。</span><span class="sxs-lookup"><span data-stu-id="c8983-107">A common scenario in ASP.NET MVC 5 and Web API 2 apps was for both products to be installed in the same application.</span></span> <span data-ttu-id="c8983-108">这是一种支持的、对许多团队使用的相对常见方法，但由于这两种产品使用不同的抽象，因此需要执行一些冗余工作。</span><span class="sxs-lookup"><span data-stu-id="c8983-108">This is a supported and relatively common approach used by many teams, but because the two products use different abstractions, there is some redundant effort needed.</span></span> <span data-ttu-id="c8983-109">例如，设置 ASP.NET MVC 的路由是使用上的方法（ `RouteCollection` 如和）完成 `MapMvcAttributeRoutes()` 的 `MapRoute()` 。</span><span class="sxs-lookup"><span data-stu-id="c8983-109">For example, setting up routes for ASP.NET MVC is done using methods on `RouteCollection`, such as `MapMvcAttributeRoutes()` and `MapRoute()`.</span></span> <span data-ttu-id="c8983-110">但 ASP.NET Web API 2 路由由和等 `HttpConfiguration` 方法管理 `MapHttpAttributeRoutes()` `MapHttpRoute()` 。</span><span class="sxs-lookup"><span data-stu-id="c8983-110">But ASP.NET Web API 2 routing is managed with `HttpConfiguration` and methods like `MapHttpAttributeRoutes()` and `MapHttpRoute()`.</span></span>

<span data-ttu-id="c8983-111">此 `eShopLegacyMVC` 应用包括 ASP.NET MVC 和 WEB API，并在其文件夹中包含 `App_Start` 用于为两者设置路由的方法。</span><span class="sxs-lookup"><span data-stu-id="c8983-111">The `eShopLegacyMVC` app includes both ASP.NET MVC and Web API, and includes methods in its `App_Start` folder for setting up routes for both.</span></span> <span data-ttu-id="c8983-112">它还支持使用 Autofac 进行依赖关系注入，这还需要配置两组相似的工作：</span><span class="sxs-lookup"><span data-stu-id="c8983-112">It also supports dependency injection using Autofac, which also requires two sets of similar work to configure:</span></span>

```csharp
protected IContainer RegisterContainer()
{
    var builder = new ContainerBuilder();

    var thisAssembly = Assembly.GetExecutingAssembly();
    builder.RegisterControllers(thisAssembly);      // MVC controllers
    builder.RegisterApiControllers(thisAssembly);   // Web API controllers

    var mockData = bool.Parse(ConfigurationManager.AppSettings["UseMockData"]);
    builder.RegisterModule(new ApplicationModule(mockData));

    var container = builder.Build();

    // set mvc resolver
    DependencyResolver.SetResolver(new AutofacDependencyResolver(container));

    // set webapi resolver
    var resolver = new AutofacWebApiDependencyResolver(container);
    GlobalConfiguration.Configuration.DependencyResolver = resolver;

    return container;
}
```

<span data-ttu-id="c8983-113">当升级这些应用程序以使用 ASP.NET Core 时，这种重复的工作以及有时会造成混淆。</span><span class="sxs-lookup"><span data-stu-id="c8983-113">When upgrading these apps to use ASP.NET Core, this duplicate effort and the confusion that sometimes accompanies it is eliminated.</span></span> <span data-ttu-id="c8983-114">ASP.NET Core MVC 是一个统一框架，其中包含一组用于路由、筛选器和其他规则的规则。</span><span class="sxs-lookup"><span data-stu-id="c8983-114">ASP.NET Core MVC is a unified framework with one set of rules for routing, filters, and more.</span></span> <span data-ttu-id="c8983-115">依赖关系注入内置于 .NET Core 本身。</span><span class="sxs-lookup"><span data-stu-id="c8983-115">Dependency injection is built into .NET Core itself.</span></span> <span data-ttu-id="c8983-116">所有这些都可以在中进行配置 `Startup.cs` ，如示例中的应用程序中所示 `eShopPorted` 。</span><span class="sxs-lookup"><span data-stu-id="c8983-116">All of this can can be configured in `Startup.cs`, as is shown in the `eShopPorted` app in the sample.</span></span>

## <a name="migrate-httpresponsemessage-to-aspnet-core"></a><span data-ttu-id="c8983-117">将 HttpResponseMessage 迁移到 ASP.NET Core</span><span class="sxs-lookup"><span data-stu-id="c8983-117">Migrate HttpResponseMessage to ASP.NET Core</span></span>

<span data-ttu-id="c8983-118">某些 ASP.NET Web API 应用可能具有返回的操作方法 `HttpResponseMessage` 。</span><span class="sxs-lookup"><span data-stu-id="c8983-118">Some ASP.NET Web API apps may have action methods that return `HttpResponseMessage`.</span></span> <span data-ttu-id="c8983-119">ASP.NET Core 中不存在此类型。</span><span class="sxs-lookup"><span data-stu-id="c8983-119">This type does not exist in ASP.NET Core.</span></span> <span data-ttu-id="c8983-120">下面是在 `Delete` 操作方法中使用的 `ResponseMessage` 帮助器方法的示例 `ApiController` ：</span><span class="sxs-lookup"><span data-stu-id="c8983-120">Below is an example of its usage in a `Delete` action method, using the `ResponseMessage` helper method on the base `ApiController`:</span></span>

```csharp
// DELETE api/<controller>/5
[HttpDelete]
public IHttpActionResult Delete(int id)
{
    var brandToDelete = _service.GetCatalogBrands().FirstOrDefault(x => x.Id == id);
    if (brandToDelete == null)
    {
        return ResponseMessage(new HttpResponseMessage(HttpStatusCode.NotFound));
    }

    // demo only - don't actually delete
    return ResponseMessage(new HttpResponseMessage(HttpStatusCode.OK));
}
```

<span data-ttu-id="c8983-121">在 ASP.NET Core MVC 中，有可用于所有常见 HTTP 响应状态代码的帮助器方法，因此以上方法将移植到以下代码：</span><span class="sxs-lookup"><span data-stu-id="c8983-121">In ASP.NET Core MVC, there are helper methods available for all of the common HTTP response status codes, so the above method would be ported to the following code:</span></span>

```csharp
[HttpDelete("{id}")]
public IActionResult Delete(int id)
{
    var brandToDelete = _service.GetCatalogBrands().FirstOrDefault(x => x.Id == id);
    if (brandToDelete == null)
    {
        return NotFound();
    }

    // demo only - don't actually delete
    return Ok();
}
```

<span data-ttu-id="c8983-122">如果你发现需要返回不存在任何帮助程序的自定义状态代码，你始终可以使用 `return StatusCode(int statusCode)` 返回你喜欢的任何数值代码。</span><span class="sxs-lookup"><span data-stu-id="c8983-122">If you do find that you need to return a custom status code for which no helper exists, you can always use `return StatusCode(int statusCode)` to return any numeric code you like.</span></span>

## <a name="migrate-content-negotiation-from-aspnet-web-api-to-aspnet-core"></a><span data-ttu-id="c8983-123">将内容协商从 ASP.NET Web API 迁移到 ASP.NET Core</span><span class="sxs-lookup"><span data-stu-id="c8983-123">Migrate content negotiation from ASP.NET Web API to ASP.NET Core</span></span>

<span data-ttu-id="c8983-124">ASP.NET Web API 2 以本机方式支持 [内容协商](/aspnet/web-api/overview/formats-and-model-binding/content-negotiation) 。</span><span class="sxs-lookup"><span data-stu-id="c8983-124">ASP.NET Web API 2 supports [content negotiation](/aspnet/web-api/overview/formats-and-model-binding/content-negotiation) natively.</span></span> <span data-ttu-id="c8983-125">该示例应用包含一个 `BrandsController` ，它通过在 XML 或 JSON 中列出其结果来演示此支持。</span><span class="sxs-lookup"><span data-stu-id="c8983-125">The sample app includes a `BrandsController` that demonstrates this support by listing its results in either XML or JSON.</span></span> <span data-ttu-id="c8983-126">这取决于请求的 `Accept` 标头，并在包含或时进行 `application/xml` 更改 `application/json` 。</span><span class="sxs-lookup"><span data-stu-id="c8983-126">This is based on the request's `Accept` header, and changes when it includes `application/xml` or `application/json`.</span></span>

<span data-ttu-id="c8983-127">ASP.NET MVC 5 应用未内置内容协商支持。</span><span class="sxs-lookup"><span data-stu-id="c8983-127">ASP.NET MVC 5 apps do not have content negotiation support built in.</span></span>

<span data-ttu-id="c8983-128">内容协商比返回特定的编码类型更好，因为它更灵活，并使 API 可用于更多的客户端。</span><span class="sxs-lookup"><span data-stu-id="c8983-128">Content negotiation is preferable to returning a specific encoding type, as it is more flexible and makes the API available to a larger number of clients.</span></span> <span data-ttu-id="c8983-129">如果当前具有返回特定格式的操作方法，应考虑在将代码移植到 ASP.NET Core 时修改它们以返回支持内容协商的结果类型。</span><span class="sxs-lookup"><span data-stu-id="c8983-129">If you currently have action methods that return a specific format, you should consider modifying them to return a result type that supports content negotiation when you port the code to ASP.NET Core.</span></span>

<span data-ttu-id="c8983-130">以下代码将返回 JSON 格式的数据，而不考虑客户端 `Accept` 标头内容：</span><span class="sxs-lookup"><span data-stu-id="c8983-130">The following code returns data in JSON format regardless of client `Accept` header content:</span></span>

```csharp
[HttpGet]
public ActionResult Index()
{
    return Json(new { Message = "Hello World!" });
}
```

<span data-ttu-id="c8983-131">如果使用了适当的[返回类型](/aspnet/core/web-api/action-return-types)， [ASP.NET Core MVC 将以本机方式支持内容协商](/aspnet/core/web-api/advanced/formatting)。</span><span class="sxs-lookup"><span data-stu-id="c8983-131">[ASP.NET Core MVC supports content negotiation natively](/aspnet/core/web-api/advanced/formatting), provided an appropriate [return type](/aspnet/core/web-api/action-return-types) is used.</span></span> <span data-ttu-id="c8983-132">内容协商由 [ObjectResult] 实现，由控制器 helper 方法返回的状态代码特定操作结果返回。</span><span class="sxs-lookup"><span data-stu-id="c8983-132">Content negotiation is implemented by [ObjectResult] which is returned by the status code-specific action results returned by the controller helper methods.</span></span> <span data-ttu-id="c8983-133">在 ASP.NET Core MVC 和使用内容协商中实现的上一操作方法为：</span><span class="sxs-lookup"><span data-stu-id="c8983-133">The previous action method, implemented in ASP.NET Core MVC and using content negotiation, would be:</span></span>

```csharp
public IActionResult Index()
{
    return Ok(new { Message = "Hello World!"} );
}
```

<span data-ttu-id="c8983-134">这将默认返回 JSON 格式的数据。</span><span class="sxs-lookup"><span data-stu-id="c8983-134">This will default to returning the data in JSON format.</span></span> <span data-ttu-id="c8983-135">[如果已使用适当的格式化程序配置了应用程序](/aspnet/core/web-api/advanced/formatting)，则将使用 XML 和其他格式。</span><span class="sxs-lookup"><span data-stu-id="c8983-135">XML and other formats will be used [if the app has been configured with the appropriate formatter](/aspnet/core/web-api/advanced/formatting).</span></span>

## <a name="references"></a><span data-ttu-id="c8983-136">参考</span><span class="sxs-lookup"><span data-stu-id="c8983-136">References</span></span>

- [<span data-ttu-id="c8983-137">ASP.NET Web API 内容协商</span><span class="sxs-lookup"><span data-stu-id="c8983-137">ASP.NET Web API Content Negotiation</span></span>](/aspnet/web-api/overview/formats-and-model-binding/content-negotiation)
- [<span data-ttu-id="c8983-138">设置 ASP.NET Core Web API 中响应数据的格式</span><span class="sxs-lookup"><span data-stu-id="c8983-138">Format response data in ASP.NET Core Web API</span></span>](/aspnet/core/web-api/advanced/formatting)

>[!div class="step-by-step"]
><span data-ttu-id="c8983-139">[上一页](example-migration-eshop.md)
>[下一页](deployment-scenarios.md)</span><span class="sxs-lookup"><span data-stu-id="c8983-139">[Previous](example-migration-eshop.md)
[Next](deployment-scenarios.md)</span></span>
