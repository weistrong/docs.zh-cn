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
# <a name="compare-authentication-and-authorization-between-aspnet-mvc-and-aspnet-core"></a><span data-ttu-id="ade0b-103">比较 ASP.NET MVC 和 ASP.NET Core 之间的身份验证和授权</span><span class="sxs-lookup"><span data-stu-id="ade0b-103">Compare authentication and authorization between ASP.NET MVC and ASP.NET Core</span></span>

<span data-ttu-id="ade0b-104">在 ASP.NET MVC 5 中，在 *App_Start* 文件夹的 *Startup.Auth.cs* 中配置身份验证。</span><span class="sxs-lookup"><span data-stu-id="ade0b-104">In ASP.NET MVC 5, authentication is configured in *Startup.Auth.cs* in the *App_Start* folder.</span></span> <span data-ttu-id="ade0b-105">在 ASP.NET Core MVC 中，此配置发生在中 `Startup.cs` 。</span><span class="sxs-lookup"><span data-stu-id="ade0b-105">In ASP.NET Core MVC, this configuration occurs in `Startup.cs`.</span></span> <span data-ttu-id="ade0b-106">使用添加到中的请求管道的中间件执行身份验证和授权 `ConfigureServices` ：</span><span class="sxs-lookup"><span data-stu-id="ade0b-106">Authentication and authorization are performed using middleware added to the request pipeline in `ConfigureServices`:</span></span>

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

<span data-ttu-id="ade0b-107">在中间件管道中按适当的顺序添加身份验证中间件非常重要。</span><span class="sxs-lookup"><span data-stu-id="ade0b-107">It's important to add the auth middleware in the appropriate order in the middleware pipeline.</span></span> <span data-ttu-id="ade0b-108">只有使其对中间件的请求才会受到影响。</span><span class="sxs-lookup"><span data-stu-id="ade0b-108">Only requests that make it to the middleware will be impacted by it.</span></span> <span data-ttu-id="ade0b-109">例如，如果对的调用 `UseStaticFiles()` 放置在此处显示的代码上方，则不会受到身份验证和授权的保护。</span><span class="sxs-lookup"><span data-stu-id="ade0b-109">For instance, if a call to `UseStaticFiles()` was placed above the code shown here, it wouldn't be protected by authentication and authorization.</span></span>

<span data-ttu-id="ade0b-110">在 ASP.NET MVC 和 Web API 中，应用通常使用属性引用当前用户 `ClaimsPrincipal.Current` 。</span><span class="sxs-lookup"><span data-stu-id="ade0b-110">In ASP.NET MVC and Web API, apps often refer to the current user using the `ClaimsPrincipal.Current` property.</span></span> <span data-ttu-id="ade0b-111">此属性未在 ASP.NET Core 中设置，并且应用中依赖于它的任何行为都需要通过[](/aspnet/core/migration/claimsprincipal-current)使用 `User` 上的属性 `ControllerBase` 或访问当前 `HttpContext` 并引用其 `User` 属性来从 ClaimsPrincipal 迁移。</span><span class="sxs-lookup"><span data-stu-id="ade0b-111">This property isn't set in ASP.NET Core, and any behavior in your app that depends on it will need to [migrate from ClaimsPrincipal.Current](/aspnet/core/migration/claimsprincipal-current) by using the `User` property on `ControllerBase` or getting access to the current `HttpContext` and referencing its `User` property.</span></span> <span data-ttu-id="ade0b-112">如果这些解决方案都不是一个选项，则服务可以将用户作为参数请求，在这种情况下，必须从应用程序中的其他位置提供该用户，或者 `IHttpContextAccessor` 可以请求并使用来获取 `HttpContext` 。</span><span class="sxs-lookup"><span data-stu-id="ade0b-112">If neither of these solutions is an option, services can request the User as an argument, in which case it must be supplied from elsewhere in the app, or the `IHttpContextAccessor` can be requested and used to get the `HttpContext`.</span></span>

## <a name="authorization"></a><span data-ttu-id="ade0b-113">授权</span><span class="sxs-lookup"><span data-stu-id="ade0b-113">Authorization</span></span>

<span data-ttu-id="ade0b-114">授权定义给定用户可以在应用中执行的操作。</span><span class="sxs-lookup"><span data-stu-id="ade0b-114">Authorization defines what a given user can do within the app.</span></span> <span data-ttu-id="ade0b-115">它独立于身份验证，只涉及确定用户是谁。</span><span class="sxs-lookup"><span data-stu-id="ade0b-115">It's separate from authentication, which is concerned merely with identifying who the user is.</span></span> <span data-ttu-id="ade0b-116">ASP.NET Core 提供了一个简单的声明性角色，以及一个基于策略的丰富的授权模型。</span><span class="sxs-lookup"><span data-stu-id="ade0b-116">ASP.NET Core provides a simple, declarative role and a rich, policy-based model for authorization.</span></span> <span data-ttu-id="ade0b-117">指定资源需要授权通常与向 `[Authorize]` 操作或控制器添加属性一样简单。</span><span class="sxs-lookup"><span data-stu-id="ade0b-117">Specifying that a resource requires authorization is often as simple as adding the `[Authorize]` attribute to the action or controller.</span></span> <span data-ttu-id="ade0b-118">如果要从 MVC 视图迁移到 Razor Pages，则在 [启动时配置 Razor Pages 时应指定授权约定](/aspnet/core/security/authorization/razor-pages-authorization)。</span><span class="sxs-lookup"><span data-stu-id="ade0b-118">If you're migrating to Razor Pages from MVC views, you should [specify conventions for authorization when you configure Razor Pages in Startup](/aspnet/core/security/authorization/razor-pages-authorization).</span></span>

<span data-ttu-id="ade0b-119">ASP.NET Core 中的授权可能与禁止匿名用户一样简单，但允许经过身份验证的用户。</span><span class="sxs-lookup"><span data-stu-id="ade0b-119">Authorization in ASP.NET Core may be as simple as prohibiting anonymous users while allowing authenticated users.</span></span> <span data-ttu-id="ade0b-120">或者，它可以扩展以支持基于角色的、基于声明的或基于策略的授权方法。</span><span class="sxs-lookup"><span data-stu-id="ade0b-120">Or it can scale up to support role-based, claims-based, or policy-based authorization approaches.</span></span> <span data-ttu-id="ade0b-121">有关这些方法的详细信息，请参阅 [ASP.NET Core 中有关授权](/aspnet/core/security/authorization/introduction)的文档。</span><span class="sxs-lookup"><span data-stu-id="ade0b-121">For more information on these approaches, see the documentation on [authorization in ASP.NET Core](/aspnet/core/security/authorization/introduction).</span></span> <span data-ttu-id="ade0b-122">你可能会发现其中一个与当前的授权方法密切一致。</span><span class="sxs-lookup"><span data-stu-id="ade0b-122">You'll likely find that one of them is closely aligned with your current authorization approach.</span></span>

## <a name="references"></a><span data-ttu-id="ade0b-123">参考</span><span class="sxs-lookup"><span data-stu-id="ade0b-123">References</span></span>

- [<span data-ttu-id="ade0b-124">ASP.NET MVC 的安全性、身份验证和授权</span><span class="sxs-lookup"><span data-stu-id="ade0b-124">Security, Authentication, and Authorization with ASP.NET MVC</span></span>](/aspnet/mvc/overview/security/)
- [<span data-ttu-id="ade0b-125">将身份验证和标识迁移到 ASP.NET Core</span><span class="sxs-lookup"><span data-stu-id="ade0b-125">Migrate Authentication and Identity to ASP.NET Core</span></span>](/aspnet/mvc/overview/security/)
- [<span data-ttu-id="ade0b-126">从 ClaimsPrincipal 迁移</span><span class="sxs-lookup"><span data-stu-id="ade0b-126">Migrate from ClaimsPrincipal.Current</span></span>](/aspnet/core/migration/claimsprincipal-current)
- [<span data-ttu-id="ade0b-127">ASP.NET Core 中的授权简介</span><span class="sxs-lookup"><span data-stu-id="ade0b-127">Introduction to Authorization in ASP.NET Core</span></span>](/aspnet/core/security/authorization/introduction)

>[!div class="step-by-step"]
><span data-ttu-id="ade0b-128">[上一页](webapi-differences.md)
>[下一页](identity-differences.md)</span><span class="sxs-lookup"><span data-stu-id="ade0b-128">[Previous](webapi-differences.md)
[Next](identity-differences.md)</span></span>
