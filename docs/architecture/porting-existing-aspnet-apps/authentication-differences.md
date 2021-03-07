---
title: 比较 ASP.NET MVC 和 ASP.NET Core 之间的身份验证和授权
description: ASP.NET MVC 和 ASP.NET Core 之间的身份验证和授权差异的汇总。
author: ardalis
ms.date: 11/13/2020
ms.openlocfilehash: c8f3314186b7408e40d3a79cbc922a29eb75c5d2
ms.sourcegitcommit: 42d436ebc2a7ee02fc1848c7742bc7d80e13fc2f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/04/2021
ms.locfileid: "102401099"
---
# <a name="compare-authentication-and-authorization-between-aspnet-mvc-and-aspnet-core"></a>比较 ASP.NET MVC 和 ASP.NET Core 之间的身份验证和授权

在 ASP.NET MVC 5 中，在 *App_Start* 文件夹的 *Startup.Auth.cs* 中配置身份验证。 在 ASP.NET Core MVC 中，此配置发生在中 `Startup.cs` 。 使用添加到中的请求管道的中间件执行身份验证和授权 `ConfigureServices` ：

```csharp
// inside Startup.ConfigureServices

app.UseRouting();

app.UseAuthentication();
app.UseAuthorization();

app.UseEndpoints(endpoints =>
{
    endpoints.MapControllerRoute(
        name: "default",
        pattern: "{controller=Home}/{action=Index}/{id?}");
    endpoints.MapRazorPages();
});
```

在中间件管道中按适当的顺序添加身份验证中间件非常重要。 只有使其对中间件的请求才会受到影响。 例如，如果对的调用 `UseStaticFiles()` 放置在此处显示的代码上方，则不会受到身份验证和授权的保护。

在 ASP.NET MVC 和 Web API 中，应用通常使用属性引用当前用户 `ClaimsPrincipal.Current` 。 此属性未在 ASP.NET Core 中设置，并且应用中依赖于它的任何行为都需要通过[](/aspnet/core/migration/claimsprincipal-current)使用 `User` 上的属性 `ControllerBase` 或访问当前 `HttpContext` 并引用其 `User` 属性来从 ClaimsPrincipal 迁移。 如果这些解决方案都不是一个选项，则服务可以将用户作为参数请求，在这种情况下，必须从应用程序中的其他位置提供该用户，或者 `IHttpContextAccessor` 可以请求并使用来获取 `HttpContext` 。

## <a name="authorization"></a>授权

授权定义给定用户可以在应用中执行的操作。 它独立于身份验证，只涉及确定用户是谁。 ASP.NET Core 提供了一个简单的声明性角色，以及一个基于策略的丰富的授权模型。 指定资源需要授权通常与向 `[Authorize]` 操作或控制器添加属性一样简单。 如果要从 MVC 视图迁移到 Razor Pages，则在 [启动时配置 Razor Pages 时应指定授权约定](/aspnet/core/security/authorization/razor-pages-authorization)。

ASP.NET Core 中的授权可能与禁止匿名用户一样简单，但允许经过身份验证的用户。 或者，它可以扩展以支持基于角色的、基于声明的或基于策略的授权方法。 有关这些方法的详细信息，请参阅 [ASP.NET Core 中有关授权](/aspnet/core/security/authorization/introduction)的文档。 你可能会发现其中一个与当前的授权方法密切一致。

## <a name="references"></a>参考

- [ASP.NET MVC 的安全性、身份验证和授权](/aspnet/mvc/overview/security/)
- [将身份验证和标识迁移到 ASP.NET Core](/aspnet/mvc/overview/security/)
- [从 ClaimsPrincipal 迁移](/aspnet/core/migration/claimsprincipal-current)
- [ASP.NET Core 中的授权简介](/aspnet/core/security/authorization/introduction)

>[!div class="step-by-step"]
>[上一页](webapi-differences.md)
>[下一页](identity-differences.md)
