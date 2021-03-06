---
title: ASP.NET MVC 和 ASP.NET Core 之间的路由差异
description: 路由是如何定义的，它在运行时的 ASP.NET MVC 中如何工作？ ASP.NET Core 应用中的路由有何不同？
author: ardalis
ms.date: 11/13/2020
ms.openlocfilehash: d5c18948248f03a19c97461efe3df38a5be9360b
ms.sourcegitcommit: 42d436ebc2a7ee02fc1848c7742bc7d80e13fc2f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/04/2021
ms.locfileid: "102401065"
---
# <a name="routing-differences-between-aspnet-mvc-and-aspnet-core"></a><span data-ttu-id="83991-104">ASP.NET MVC 和 ASP.NET Core 之间的路由差异</span><span class="sxs-lookup"><span data-stu-id="83991-104">Routing differences between ASP.NET MVC and ASP.NET Core</span></span>

<span data-ttu-id="83991-105">路由负责将传入浏览器请求映射到 (或 Razor Pages 处理程序) 的特定控制器操作。</span><span class="sxs-lookup"><span data-stu-id="83991-105">Routing is responsible for mapping incoming browser requests to particular controller actions (or Razor Pages handlers).</span></span> <span data-ttu-id="83991-106">本部分介绍了 ASP.NET MVC (和 Web API) 之间的路由与 ASP.NET Core (MVC、Razor Pages 和其他) 的不同之处。</span><span class="sxs-lookup"><span data-stu-id="83991-106">This section covers how routing differs between ASP.NET MVC (and Web API) and ASP.NET Core (MVC, Razor Pages, and otherwise).</span></span>

## <a name="routing-in-aspnet-mvc-and-web-api"></a><span data-ttu-id="83991-107">ASP.NET MVC 和 Web API 中的路由</span><span class="sxs-lookup"><span data-stu-id="83991-107">Routing in ASP.NET MVC and Web API</span></span>

<span data-ttu-id="83991-108">ASP.NET MVC 提供两种路由方法：</span><span class="sxs-lookup"><span data-stu-id="83991-108">ASP.NET MVC offers two approaches to routing:</span></span>

1. <span data-ttu-id="83991-109">路由表，路由表是可用于匹配传入请求和控制器操作的路由的集合。</span><span class="sxs-lookup"><span data-stu-id="83991-109">The route table, which is a collection of routes that can be used to match incoming requests to controller actions.</span></span>
1. <span data-ttu-id="83991-110">属性路由，它执行相同的功能，但通过装饰操作本身来实现，而不是编辑全局路由表。</span><span class="sxs-lookup"><span data-stu-id="83991-110">Attribute routing, which performs the same function but is achieved by decorating the actions themselves, rather than editing a global route table.</span></span>

## <a name="route-table"></a><span data-ttu-id="83991-111">路由表</span><span class="sxs-lookup"><span data-stu-id="83991-111">Route table</span></span>

<span data-ttu-id="83991-112">在应用启动时配置路由表。</span><span class="sxs-lookup"><span data-stu-id="83991-112">The route table is configured when the app starts up.</span></span> <span data-ttu-id="83991-113">通常，静态方法调用用于配置全局路由集合，如下所示：</span><span class="sxs-lookup"><span data-stu-id="83991-113">Typically, a static method call is used to configure the global route collection, like so:</span></span>

```csharp
public class MvcApplication : System.Web.HttpApplication
{
    public static void RegisterRoutes(RouteCollection routes)
    {
        routes.IgnoreRoute("{resource}.axd/{*pathInfo}");
        routes.MapRoute(
            name: "Default",
            url: "{controller}/{action}/{id}",
            defaults: new { controller = "Home", action = "Index", id = "" },
            constraints: new { id = "\\d+" }
        );
    }

    protected void Application_Start()
    {
        RegisterRoutes(RouteTable.Routes);
    }
}
```

<span data-ttu-id="83991-114">在前面的代码中，路由表由 `RouteCollection` 类型管理，后者用于向添加新路由 `MapRoute` 。</span><span class="sxs-lookup"><span data-stu-id="83991-114">In the preceding code, the route table is managed by the `RouteCollection` type, which is used to add new routes with `MapRoute`.</span></span> <span data-ttu-id="83991-115">路由命名为，并包含路由字符串，其中可以包含控制器、操作、区域和其他占位符的参数。</span><span class="sxs-lookup"><span data-stu-id="83991-115">Routes are named and include a route string, which can include parameters for controllers, actions, areas, and other placeholders.</span></span> <span data-ttu-id="83991-116">如果应用遵循标准约定，则可以通过此单个默认路由处理其大部分操作，但使用其他路由配置此约定的任何例外。</span><span class="sxs-lookup"><span data-stu-id="83991-116">If an app follows a standard convention, most of its actions can be handled by this single default route, with any exceptions to this convention configured using additional routes.</span></span>

### <a name="attribute-routing-in-aspnet-mvc"></a><span data-ttu-id="83991-117">ASP.NET MVC 中的属性路由</span><span class="sxs-lookup"><span data-stu-id="83991-117">Attribute routing in ASP.NET MVC</span></span>

<span data-ttu-id="83991-118">使用其操作定义的路由可能更易于发现和原因，而不是在外部位置定义的路由。</span><span class="sxs-lookup"><span data-stu-id="83991-118">Routes that are defined with their actions may be easier to discover and reason about than routes defined in an external location.</span></span> <span data-ttu-id="83991-119">使用属性路由，单个操作方法可以使用属性定义其路由 `[Route]` ：</span><span class="sxs-lookup"><span data-stu-id="83991-119">Using attribute routing, an individual action method can have its route defined with a `[Route]` attribute:</span></span>

```csharp
public class ProductsController
{
    [Route("products")]
    public ActionResult Index()
    {
        return View();
    }

    [Route("products/{id}")]
    public ActionResult Details(int id)
    {
        return View();
    }
}
```

<span data-ttu-id="83991-120">[ASP.NET MVC 5 中的属性路由](https://devblogs.microsoft.com/aspnet/attribute-routing-in-asp-net-mvc-5/) 还支持默认值和前缀，它们可添加到 (的控制器级别，并将应用于该控制器) 中的所有操作。</span><span class="sxs-lookup"><span data-stu-id="83991-120">[Attribute routing in ASP.NET MVC 5](https://devblogs.microsoft.com/aspnet/attribute-routing-in-asp-net-mvc-5/) also supports defaults and prefixes, which can be added at the controller level (and which are applied to all actions within that controller).</span></span> <span data-ttu-id="83991-121">有关详细信息，请参阅文档。</span><span class="sxs-lookup"><span data-stu-id="83991-121">Refer to the documentation for details.</span></span>

<span data-ttu-id="83991-122">设置属性路由要求在默认路由表配置中添加一行：</span><span class="sxs-lookup"><span data-stu-id="83991-122">Setting up attribute routing requires adding one line to the default route table configuration:</span></span>

```csharp
routes.MapMvcAttributeRoutes();
```

<span data-ttu-id="83991-123">属性路由可以利用路由约束（内置和自定义），并使用属性支持命名路由和区域 `[RouteArea]` 。</span><span class="sxs-lookup"><span data-stu-id="83991-123">Attribute routing can take advantage of route constraints, both built-in and custom, and supports named routes and areas using the `[RouteArea]` attribute.</span></span> <span data-ttu-id="83991-124">如果你的应用使用区域，你将需要通过另外添加一行来在路由注册代码中配置对它们的支持：</span><span class="sxs-lookup"><span data-stu-id="83991-124">If your app uses areas, you'll need to configure support for them in your route registration code by adding one more line:</span></span>

```csharp
routes.MapMvcAttributeRoutes();

AreaRegistration.RegisterAllAreas();
```

### <a name="attribute-routing-in-aspnet-web-api-2"></a><span data-ttu-id="83991-125">ASP.NET Web API 2 中的属性路由</span><span class="sxs-lookup"><span data-stu-id="83991-125">Attribute routing in ASP.NET Web API 2</span></span>

<span data-ttu-id="83991-126">[ASP.NET Web API 2 中的属性路由](/aspnet/web-api/overview/web-api-routing-and-actions/attribute-routing-in-web-api-2) 类似于 ASP.NET MVC 5 中的路由，但差别很小。</span><span class="sxs-lookup"><span data-stu-id="83991-126">[Attribute routing in ASP.NET Web API 2](/aspnet/web-api/overview/web-api-routing-and-actions/attribute-routing-in-web-api-2) is similar to routing in ASP.NET MVC 5, with minor differences.</span></span> <span data-ttu-id="83991-127">配置 Web API 2 通常在自己的类中完成，此类在应用程序启动过程中调用。</span><span class="sxs-lookup"><span data-stu-id="83991-127">Configuring Web API 2 is typically done in its own class, which is called during app startup.</span></span> <span data-ttu-id="83991-128">在此类中处理特性路由配置：</span><span class="sxs-lookup"><span data-stu-id="83991-128">Attribute routing configuration is handled in this class:</span></span>

```csharp
public static class WebApiConfig
{
    public static void Register(HttpConfiguration config)
    {
        // Attribute routing.
        config.MapHttpAttributeRoutes();

        // Convention-based routing.
        config.Routes.MapHttpRoute(
            name: "DefaultApi",
            routeTemplate: "api/{controller}/{id}",
            defaults: new { id = RouteParameter.Optional }
        );
    }
}
```

<span data-ttu-id="83991-129">如前面的代码中所示，属性路由可能与 Web API 应用中基于约定的路由结合在一起。</span><span class="sxs-lookup"><span data-stu-id="83991-129">As shown in the preceding code, attribute routing may be combined with convention-based routing in Web API apps.</span></span>

<span data-ttu-id="83991-130">除了属性路由外，ASP.NET Web API 根据 HTTP 方法 [选择要调用的操作](/aspnet/web-api/overview/web-api-routing-and-actions/routing-and-action-selection) (例如，GET 或 POST) 、 `{action}` 路由中的占位符 (if 任何) 和操作的参数。</span><span class="sxs-lookup"><span data-stu-id="83991-130">In addition to attribute routing, [ASP.NET Web API chooses which action to call](/aspnet/web-api/overview/web-api-routing-and-actions/routing-and-action-selection) based on the HTTP method (for example, GET or POST), the `{action}` placeholder in a route (if any), and parameters of the action.</span></span> <span data-ttu-id="83991-131">在许多情况下，操作的名称将帮助确定是否匹配，因为使用 "Get" 或 "Post" 作为操作名称的前缀将用于匹配相应的 HTTP 方法。</span><span class="sxs-lookup"><span data-stu-id="83991-131">In many cases, the name of the action will help determine whether it's matched, since prefixing the action name with "Get" or "Post" is used to match the appropriate HTTP method to it.</span></span> <span data-ttu-id="83991-132">或者，可以使用适当的 HTTP 方法特性修饰操作，如 `[HttpGet]` ，允许使用未以 http 方法为前缀的操作名称。</span><span class="sxs-lookup"><span data-stu-id="83991-132">Alternatively, actions can be decorated with an appropriate HTTP method attribute, like `[HttpGet]`, allowing the use of action names that aren't prefixed with an HTTP method.</span></span>

```csharp
public class ProductsController : ApiController
{
    // matched by name and (lack of) parameters
    public IEnumerable<Product> GetAll() { }

    // matched by GET and string parameter
    [HttpGet]
    public IEnumerable<Product> FindProductsByName(string name) { }
}
```

<span data-ttu-id="83991-133">给定上述控制器，HTTP GET 请求可 `localhost:123/products/` 匹配该 `GetAll` 操作。</span><span class="sxs-lookup"><span data-stu-id="83991-133">Given the above controller, an HTTP GET request to `localhost:123/products/` matches the `GetAll` action.</span></span> <span data-ttu-id="83991-134">用于 `localhost:123/products?name=ardalis` 匹配操作的 HTTP GET 请求 `FindProductsByName` 。</span><span class="sxs-lookup"><span data-stu-id="83991-134">An HTTP GET request to `localhost:123/products?name=ardalis` matches the `FindProductsByName` action.</span></span>

## <a name="routing-in-aspnet-core-31"></a><span data-ttu-id="83991-135">ASP.NET Core 3.1 中的路由</span><span class="sxs-lookup"><span data-stu-id="83991-135">Routing in ASP.NET Core 3.1</span></span>

<span data-ttu-id="83991-136">在 ASP.NET Core 中，路由由路由中间件进行处理，中间件与操作或其他终结点的传入请求的 Url 相匹配。</span><span class="sxs-lookup"><span data-stu-id="83991-136">In ASP.NET Core, routing is handled by routing middleware, which matches the URLs of incoming requests to actions or other endpoints.</span></span> <span data-ttu-id="83991-137">控制器操作可以是逆路由或属性路由。</span><span class="sxs-lookup"><span data-stu-id="83991-137">Controller actions are either conventionally routed or attribute-routed.</span></span> <span data-ttu-id="83991-138">传统路由类似于 ASP.NET MVC 和 Web API 中使用的路由表方法。</span><span class="sxs-lookup"><span data-stu-id="83991-138">Conventional routing is similar to the route table approach used in ASP.NET MVC and Web API.</span></span> <span data-ttu-id="83991-139">无论是使用传统的、属性还是同时使用这两种方法，都需要将应用程序配置为使用路由中间件。</span><span class="sxs-lookup"><span data-stu-id="83991-139">Whether you're using conventional, attribute, or both, you need to configure your app to use the routing middleware.</span></span> <span data-ttu-id="83991-140">若要使用中间件，请将以下代码添加到 `Startup.Configure` 方法：</span><span class="sxs-lookup"><span data-stu-id="83991-140">To use the middleware, add the following code to your `Startup.Configure` method:</span></span>

```csharp
app.UseRouting();
```

### <a name="conventional-routing"></a><span data-ttu-id="83991-141">传统路由</span><span class="sxs-lookup"><span data-stu-id="83991-141">Conventional routing</span></span>

<span data-ttu-id="83991-142">使用传统路由时，可以设置一个或多个约定，用于将传入 Url 与应用中的 *终结点* 进行匹配。</span><span class="sxs-lookup"><span data-stu-id="83991-142">With conventional routing, you set up one or more conventions that will be used to match incoming URLs to *endpoints* in the app.</span></span> <span data-ttu-id="83991-143">在 ASP.NET Core 中，这些终结点可以是控制器操作，如 ASP.NET MVC 或 Web API。</span><span class="sxs-lookup"><span data-stu-id="83991-143">In ASP.NET Core, these endpoints may be controller actions, like in ASP.NET MVC or Web API.</span></span> <span data-ttu-id="83991-144">终结点也可以是 Razor Pages、运行状况检查或 SignalR 中心。</span><span class="sxs-lookup"><span data-stu-id="83991-144">The endpoints could also be Razor Pages, Health Checks, or SignalR hubs.</span></span> <span data-ttu-id="83991-145">所有这些可路由功能的配置方式都类似于使用终结点：</span><span class="sxs-lookup"><span data-stu-id="83991-145">All of these routable features are configured in a similar fashion using endpoints:</span></span>

```csharp
// in Startup.Configure()
app.UseEndpoints(endpoints =>
{
    endpoints.MapHealthChecks("/healthz").RequireAuthorization();
    endpoints.MapControllerRoute(
        name: "default",
        pattern: "{controller=Home}/{action=Index}/{id?}");
    endpoints.MapRazorPages();
});
```

<span data-ttu-id="83991-146">除 `UseRouting`) 配置各种终结点（包括运行状况检查、控制器和 Razor Pages）外，还 (使用前面的代码。</span><span class="sxs-lookup"><span data-stu-id="83991-146">The preceding code is used (in addition to `UseRouting`) to configure various endpoints, including Health Checks, controllers, and Razor Pages.</span></span> <span data-ttu-id="83991-147">对于控制器，以上配置指定默认路由约定，这是 `{controller}/{action}/{id?}` 自 ASP.NET MVC 的第一个版本以来建议的相当标准的模式。</span><span class="sxs-lookup"><span data-stu-id="83991-147">For controllers, the above configuration specifies a default routing convention, which is the fairly standard `{controller}/{action}/{id?}` pattern that's been recommended since the first versions of ASP.NET MVC.</span></span>

### <a name="attribute-routing"></a><span data-ttu-id="83991-148">属性路由</span><span class="sxs-lookup"><span data-stu-id="83991-148">Attribute routing</span></span>

<span data-ttu-id="83991-149">ASP.NET Core 中的属性路由是在控制器中配置路由的首选方法。</span><span class="sxs-lookup"><span data-stu-id="83991-149">Attribute routing in ASP.NET Core is the preferred approach for configuring routing in controllers.</span></span> <span data-ttu-id="83991-150">如果要构建 Api，应将 `[ApiController]` 属性应用到控制器。</span><span class="sxs-lookup"><span data-stu-id="83991-150">If you're building APIs, the `[ApiController]` attribute should be applied to your controllers.</span></span> <span data-ttu-id="83991-151">除此之外，此属性需要将属性路由用于此类控制器类中的操作。</span><span class="sxs-lookup"><span data-stu-id="83991-151">Among other things, this attribute requires the use of attribute routing for actions in such controller classes.</span></span>

<span data-ttu-id="83991-152">ASP.NET Core 中的属性路由在 ASP.NET MVC 和 Web API 中的行为类似。</span><span class="sxs-lookup"><span data-stu-id="83991-152">Attribute routing in ASP.NET Core behaves similarly in ASP.NET MVC and Web API.</span></span> <span data-ttu-id="83991-153">但除了支持特性之外， `[Route]` 还可以将路由信息指定为 HTTP 方法特性的一部分：</span><span class="sxs-lookup"><span data-stu-id="83991-153">In addition to supporting the `[Route]` attribute, however, route information can also be specified as part of the HTTP method attribute:</span></span>

```csharp
[HttpGet("api/products/{id}")]
public async ActionResult<Product> Details(int id)
{
    // ...
}
```

<span data-ttu-id="83991-154">与以前的版本一样，可以使用占位符指定默认路由，并将其添加到控制器类级别，甚至添加到基类中。</span><span class="sxs-lookup"><span data-stu-id="83991-154">As with previous versions, you can specify a default route with placeholders, and add this at the controller class level or even on a base class.</span></span> <span data-ttu-id="83991-155">`[Route]`所有这些情况都使用同一属性。</span><span class="sxs-lookup"><span data-stu-id="83991-155">You use the same `[Route]` attribute for all of these cases.</span></span> <span data-ttu-id="83991-156">例如，基本 API 控制器类可能如下所示：</span><span class="sxs-lookup"><span data-stu-id="83991-156">For example, a base API controller class might look like this:</span></span>

```csharp
[Route("api/{controller}/{action}/{id?:int}")]
public abstract class BaseApiController : ControllerBase, IApiController
{
    // ...
}
```

<span data-ttu-id="83991-157">使用此属性，从此类型继承的类将基于控制器名称、操作名称和可选整数参数将 Url 路由到操作 `id` 。</span><span class="sxs-lookup"><span data-stu-id="83991-157">Using this attribute, classes inheriting from this type would route URLs to actions based on the controller name, action name, and an optional integer `id` parameter.</span></span>

## <a name="references"></a><span data-ttu-id="83991-158">参考</span><span class="sxs-lookup"><span data-stu-id="83991-158">References</span></span>

- [<span data-ttu-id="83991-159">ASP.NET MVC Routing Overview（ASP.NET MVC 路由概述）</span><span class="sxs-lookup"><span data-stu-id="83991-159">ASP.NET MVC Routing Overview</span></span>](/aspnet/mvc/overview/older-versions-1/controllers-and-routing/asp-net-mvc-routing-overview-cs)
- [<span data-ttu-id="83991-160">ASP.NET MVC 5 中的属性路由</span><span class="sxs-lookup"><span data-stu-id="83991-160">Attribute Routing in ASP.NET MVC 5</span></span>](https://devblogs.microsoft.com/aspnet/attribute-routing-in-asp-net-mvc-5/)
- [<span data-ttu-id="83991-161">ASP.NET Web API 2 中的属性路由</span><span class="sxs-lookup"><span data-stu-id="83991-161">Attribute routing in ASP.NET Web API 2</span></span>](/aspnet/web-api/overview/web-api-routing-and-actions/attribute-routing-in-web-api-2)
- [<span data-ttu-id="83991-162">ASP.NET Web API 中的路由和操作选择</span><span class="sxs-lookup"><span data-stu-id="83991-162">Routing and Action Selection in ASP.NET Web API</span></span>](/aspnet/web-api/overview/web-api-routing-and-actions/routing-and-action-selection)
- [<span data-ttu-id="83991-163">ASP.NET Core 中的路由</span><span class="sxs-lookup"><span data-stu-id="83991-163">Routing in ASP.NET Core</span></span>](/aspnet/core/fundamentals/routing)
- [<span data-ttu-id="83991-164">路由到 ASP.NET Core MVC 中的控制器操作</span><span class="sxs-lookup"><span data-stu-id="83991-164">Routing to controller actions in ASP.NET Core MVC</span></span>](/aspnet/core/mvc/controllers/routing)

>[!div class="step-by-step"]
><span data-ttu-id="83991-165">[上一页](configuration-differences.md)
>[下一页](comparing-razor-pages-aspnet-mvc.md)</span><span class="sxs-lookup"><span data-stu-id="83991-165">[Previous](configuration-differences.md)
[Next](comparing-razor-pages-aspnet-mvc.md)</span></span>
