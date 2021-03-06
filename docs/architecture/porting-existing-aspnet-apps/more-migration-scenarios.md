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
# <a name="more-migration-scenarios"></a>更多迁移方案

[!INCLUDE [book-preview](../../../includes/book-preview.md)]

本部分介绍了几种不同的 ASP.NET 应用方案，并提供了解决每个应用方案的特定方法。 你可以使用此部分来确定适用于你的应用程序的方案，并评估适用于你的应用程序及其宿主环境的哪些方法。

## <a name="migrate-aspnet-mvc-5-and-webapi-2-to-aspnet-core-mvc"></a>将 ASP.NET MVC 5 和 WebApi 2 迁移到 ASP.NET Core MVC

ASP.NET MVC 5 和 Web API 2 应用的常见方案是，这两个产品都安装在同一应用程序中。 这是一种支持的、对许多团队使用的相对常见方法，但由于这两种产品使用不同的抽象，因此需要执行一些冗余工作。 例如，设置 ASP.NET MVC 的路由是使用上的方法（ `RouteCollection` 如和）完成 `MapMvcAttributeRoutes()` 的 `MapRoute()` 。 但 ASP.NET Web API 2 路由由和等 `HttpConfiguration` 方法管理 `MapHttpAttributeRoutes()` `MapHttpRoute()` 。

此 `eShopLegacyMVC` 应用包括 ASP.NET MVC 和 WEB API，并在其文件夹中包含 `App_Start` 用于为两者设置路由的方法。 它还支持使用 Autofac 进行依赖关系注入，这还需要配置两组相似的工作：

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

当升级这些应用程序以使用 ASP.NET Core 时，这种重复的工作以及有时会造成混淆。 ASP.NET Core MVC 是一个统一框架，其中包含一组用于路由、筛选器和其他规则的规则。 依赖关系注入内置于 .NET Core 本身。 所有这些都可以在中进行配置 `Startup.cs` ，如示例中的应用程序中所示 `eShopPorted` 。

## <a name="migrate-httpresponsemessage-to-aspnet-core"></a>将 HttpResponseMessage 迁移到 ASP.NET Core

某些 ASP.NET Web API 应用可能具有返回的操作方法 `HttpResponseMessage` 。 ASP.NET Core 中不存在此类型。 下面是在 `Delete` 操作方法中使用的 `ResponseMessage` 帮助器方法的示例 `ApiController` ：

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

在 ASP.NET Core MVC 中，有可用于所有常见 HTTP 响应状态代码的帮助器方法，因此以上方法将移植到以下代码：

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

如果你发现需要返回不存在任何帮助程序的自定义状态代码，你始终可以使用 `return StatusCode(int statusCode)` 返回你喜欢的任何数值代码。

## <a name="migrate-content-negotiation-from-aspnet-web-api-to-aspnet-core"></a>将内容协商从 ASP.NET Web API 迁移到 ASP.NET Core

ASP.NET Web API 2 以本机方式支持 [内容协商](/aspnet/web-api/overview/formats-and-model-binding/content-negotiation) 。 该示例应用包含一个 `BrandsController` ，它通过在 XML 或 JSON 中列出其结果来演示此支持。 这取决于请求的 `Accept` 标头，并在包含或时进行 `application/xml` 更改 `application/json` 。

ASP.NET MVC 5 应用未内置内容协商支持。

内容协商比返回特定的编码类型更好，因为它更灵活，并使 API 可用于更多的客户端。 如果当前具有返回特定格式的操作方法，应考虑在将代码移植到 ASP.NET Core 时修改它们以返回支持内容协商的结果类型。

以下代码将返回 JSON 格式的数据，而不考虑客户端 `Accept` 标头内容：

```csharp
[HttpGet]
public ActionResult Index()
{
    return Json(new { Message = "Hello World!" });
}
```

如果使用了适当的[返回类型](/aspnet/core/web-api/action-return-types)， [ASP.NET Core MVC 将以本机方式支持内容协商](/aspnet/core/web-api/advanced/formatting)。 内容协商由 [ObjectResult] 实现，由控制器 helper 方法返回的状态代码特定操作结果返回。 在 ASP.NET Core MVC 和使用内容协商中实现的上一操作方法为：

```csharp
public IActionResult Index()
{
    return Ok(new { Message = "Hello World!"} );
}
```

这将默认返回 JSON 格式的数据。 [如果已使用适当的格式化程序配置了应用程序](/aspnet/core/web-api/advanced/formatting)，则将使用 XML 和其他格式。

## <a name="references"></a>参考

- [ASP.NET Web API 内容协商](/aspnet/web-api/overview/formats-and-model-binding/content-negotiation)
- [设置 ASP.NET Core Web API 中响应数据的格式](/aspnet/core/web-api/advanced/formatting)

>[!div class="step-by-step"]
>[上一页](example-migration-eshop.md)
>[下一页](deployment-scenarios.md)
