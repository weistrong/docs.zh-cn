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
# <a name="routing-differences-between-aspnet-mvc-and-aspnet-core"></a>ASP.NET MVC 和 ASP.NET Core 之间的路由差异

路由负责将传入浏览器请求映射到 (或 Razor Pages 处理程序) 的特定控制器操作。 本部分介绍了 ASP.NET MVC (和 Web API) 之间的路由与 ASP.NET Core (MVC、Razor Pages 和其他) 的不同之处。

## <a name="routing-in-aspnet-mvc-and-web-api"></a>ASP.NET MVC 和 Web API 中的路由

ASP.NET MVC 提供两种路由方法：

1. 路由表，路由表是可用于匹配传入请求和控制器操作的路由的集合。
1. 属性路由，它执行相同的功能，但通过装饰操作本身来实现，而不是编辑全局路由表。

## <a name="route-table"></a>路由表

在应用启动时配置路由表。 通常，静态方法调用用于配置全局路由集合，如下所示：

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

在前面的代码中，路由表由 `RouteCollection` 类型管理，后者用于向添加新路由 `MapRoute` 。 路由命名为，并包含路由字符串，其中可以包含控制器、操作、区域和其他占位符的参数。 如果应用遵循标准约定，则可以通过此单个默认路由处理其大部分操作，但使用其他路由配置此约定的任何例外。

### <a name="attribute-routing-in-aspnet-mvc"></a>ASP.NET MVC 中的属性路由

使用其操作定义的路由可能更易于发现和原因，而不是在外部位置定义的路由。 使用属性路由，单个操作方法可以使用属性定义其路由 `[Route]` ：

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

[ASP.NET MVC 5 中的属性路由](https://devblogs.microsoft.com/aspnet/attribute-routing-in-asp-net-mvc-5/) 还支持默认值和前缀，它们可添加到 (的控制器级别，并将应用于该控制器) 中的所有操作。 有关详细信息，请参阅文档。

设置属性路由要求在默认路由表配置中添加一行：

```csharp
routes.MapMvcAttributeRoutes();
```

属性路由可以利用路由约束（内置和自定义），并使用属性支持命名路由和区域 `[RouteArea]` 。 如果你的应用使用区域，你将需要通过另外添加一行来在路由注册代码中配置对它们的支持：

```csharp
routes.MapMvcAttributeRoutes();

AreaRegistration.RegisterAllAreas();
```

### <a name="attribute-routing-in-aspnet-web-api-2"></a>ASP.NET Web API 2 中的属性路由

[ASP.NET Web API 2 中的属性路由](/aspnet/web-api/overview/web-api-routing-and-actions/attribute-routing-in-web-api-2) 类似于 ASP.NET MVC 5 中的路由，但差别很小。 配置 Web API 2 通常在自己的类中完成，此类在应用程序启动过程中调用。 在此类中处理特性路由配置：

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

如前面的代码中所示，属性路由可能与 Web API 应用中基于约定的路由结合在一起。

除了属性路由外，ASP.NET Web API 根据 HTTP 方法 [选择要调用的操作](/aspnet/web-api/overview/web-api-routing-and-actions/routing-and-action-selection) (例如，GET 或 POST) 、 `{action}` 路由中的占位符 (if 任何) 和操作的参数。 在许多情况下，操作的名称将帮助确定是否匹配，因为使用 "Get" 或 "Post" 作为操作名称的前缀将用于匹配相应的 HTTP 方法。 或者，可以使用适当的 HTTP 方法特性修饰操作，如 `[HttpGet]` ，允许使用未以 http 方法为前缀的操作名称。

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

给定上述控制器，HTTP GET 请求可 `localhost:123/products/` 匹配该 `GetAll` 操作。 用于 `localhost:123/products?name=ardalis` 匹配操作的 HTTP GET 请求 `FindProductsByName` 。

## <a name="routing-in-aspnet-core-31"></a>ASP.NET Core 3.1 中的路由

在 ASP.NET Core 中，路由由路由中间件进行处理，中间件与操作或其他终结点的传入请求的 Url 相匹配。 控制器操作可以是逆路由或属性路由。 传统路由类似于 ASP.NET MVC 和 Web API 中使用的路由表方法。 无论是使用传统的、属性还是同时使用这两种方法，都需要将应用程序配置为使用路由中间件。 若要使用中间件，请将以下代码添加到 `Startup.Configure` 方法：

```csharp
app.UseRouting();
```

### <a name="conventional-routing"></a>传统路由

使用传统路由时，可以设置一个或多个约定，用于将传入 Url 与应用中的 *终结点* 进行匹配。 在 ASP.NET Core 中，这些终结点可以是控制器操作，如 ASP.NET MVC 或 Web API。 终结点也可以是 Razor Pages、运行状况检查或 SignalR 中心。 所有这些可路由功能的配置方式都类似于使用终结点：

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

除 `UseRouting`) 配置各种终结点（包括运行状况检查、控制器和 Razor Pages）外，还 (使用前面的代码。 对于控制器，以上配置指定默认路由约定，这是 `{controller}/{action}/{id?}` 自 ASP.NET MVC 的第一个版本以来建议的相当标准的模式。

### <a name="attribute-routing"></a>属性路由

ASP.NET Core 中的属性路由是在控制器中配置路由的首选方法。 如果要构建 Api，应将 `[ApiController]` 属性应用到控制器。 除此之外，此属性需要将属性路由用于此类控制器类中的操作。

ASP.NET Core 中的属性路由在 ASP.NET MVC 和 Web API 中的行为类似。 但除了支持特性之外， `[Route]` 还可以将路由信息指定为 HTTP 方法特性的一部分：

```csharp
[HttpGet("api/products/{id}")]
public async ActionResult<Product> Details(int id)
{
    // ...
}
```

与以前的版本一样，可以使用占位符指定默认路由，并将其添加到控制器类级别，甚至添加到基类中。 `[Route]`所有这些情况都使用同一属性。 例如，基本 API 控制器类可能如下所示：

```csharp
[Route("api/{controller}/{action}/{id?:int}")]
public abstract class BaseApiController : ControllerBase, IApiController
{
    // ...
}
```

使用此属性，从此类型继承的类将基于控制器名称、操作名称和可选整数参数将 Url 路由到操作 `id` 。

## <a name="references"></a>参考

- [ASP.NET MVC Routing Overview（ASP.NET MVC 路由概述）](/aspnet/mvc/overview/older-versions-1/controllers-and-routing/asp-net-mvc-routing-overview-cs)
- [ASP.NET MVC 5 中的属性路由](https://devblogs.microsoft.com/aspnet/attribute-routing-in-asp-net-mvc-5/)
- [ASP.NET Web API 2 中的属性路由](/aspnet/web-api/overview/web-api-routing-and-actions/attribute-routing-in-web-api-2)
- [ASP.NET Web API 中的路由和操作选择](/aspnet/web-api/overview/web-api-routing-and-actions/routing-and-action-selection)
- [ASP.NET Core 中的路由](/aspnet/core/fundamentals/routing)
- [路由到 ASP.NET Core MVC 中的控制器操作](/aspnet/core/mvc/controllers/routing)

>[!div class="step-by-step"]
>[上一页](configuration-differences.md)
>[下一页](comparing-razor-pages-aspnet-mvc.md)
