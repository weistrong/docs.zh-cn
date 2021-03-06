---
title: 比较 ASP.NET MVC 和 ASP.NET Core 中的控制器
description: ASP.NET Core MVC 控制器与 ASP.NET MVC 5 和 Web API 2 控制器相似，但存在重要的差异。 本部分介绍从 ASP.NET MVC 和 Web API 2 到 ASP.NET Core 所需的端口的不同和步骤。
author: ardalis
ms.date: 11/13/2020
ms.openlocfilehash: 2c2b7b848162a6ab9901ac9f7779787e2cc994ce
ms.sourcegitcommit: 42d436ebc2a7ee02fc1848c7742bc7d80e13fc2f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/04/2021
ms.locfileid: "102401087"
---
# <a name="compare-controllers-in-aspnet-mvc-and-web-api-with-controllers-in-aspnet-core"></a><span data-ttu-id="79fef-104">将 ASP.NET MVC 和 Web API 中的控制器与 ASP.NET Core 中的控制器进行比较</span><span class="sxs-lookup"><span data-stu-id="79fef-104">Compare controllers in ASP.NET MVC and Web API with controllers in ASP.NET Core</span></span>

<span data-ttu-id="79fef-105">在 ASP.NET MVC 5 和 Web API 2 中，有两种不同 `Controller` 的基类型。</span><span class="sxs-lookup"><span data-stu-id="79fef-105">In ASP.NET MVC 5 and Web API 2, there were two different `Controller` base types.</span></span> <span data-ttu-id="79fef-106">继承自的 MVC 控制器 `Controller` ;从继承的 Web API 控制器 `ApiController` 。</span><span class="sxs-lookup"><span data-stu-id="79fef-106">MVC controllers inherited from `Controller`; Web API controllers inherited from `ApiController`.</span></span> <span data-ttu-id="79fef-107">在 ASP.NET Core 中，已合并此对象层次结构。</span><span class="sxs-lookup"><span data-stu-id="79fef-107">In ASP.NET Core, this object hierarchy has been merged.</span></span> <span data-ttu-id="79fef-108">建议 ASP.NET Core 中的 API 控制器继承 `ControllerBase` 并添加 `[ApiController]` 属性。</span><span class="sxs-lookup"><span data-stu-id="79fef-108">It's recommended that API controllers in ASP.NET Core inherit from `ControllerBase` and add the `[ApiController]` attribute.</span></span> <span data-ttu-id="79fef-109">基于标准视图的 MVC 控制器应从继承 `Controller` 。</span><span class="sxs-lookup"><span data-stu-id="79fef-109">Standard view-based MVC controllers should inherit from `Controller`.</span></span>

<span data-ttu-id="79fef-110">在这两个框架中，控制器都用于组织操作方法集。</span><span class="sxs-lookup"><span data-stu-id="79fef-110">In both frameworks, controllers are used to organize sets of action methods.</span></span> <span data-ttu-id="79fef-111">除了在操作级别，还可以在控制器级别应用筛选器和路由。</span><span class="sxs-lookup"><span data-stu-id="79fef-111">Filters and routes can be applied on a controller level in addition to at the action level.</span></span> <span data-ttu-id="79fef-112">通过使用 `Controller` 具有默认行为的自定义基类型和应用于它们的特性，可以进一步扩展这些约定。</span><span class="sxs-lookup"><span data-stu-id="79fef-112">These conventions can be extended further by using custom base `Controller` types with default behavior and attributes applied to them.</span></span>

<span data-ttu-id="79fef-113">在 ASP.NET MVC 中，不支持内容协商。</span><span class="sxs-lookup"><span data-stu-id="79fef-113">In ASP.NET MVC, content negotiation isn't supported.</span></span> <span data-ttu-id="79fef-114">ASP.NET Web API 2 支持内容协商，ASP.NET Core。</span><span class="sxs-lookup"><span data-stu-id="79fef-114">ASP.NET Web API 2 does support content negotiation, as does ASP.NET Core.</span></span> <span data-ttu-id="79fef-115">使用 [内容协商](/aspnet/core/web-api/advanced/formatting)，返回到请求的内容格式可由客户端提供的标头来确定，客户端提供该内容是为了接收内容的首选方式。</span><span class="sxs-lookup"><span data-stu-id="79fef-115">Using [content negotiation](/aspnet/core/web-api/advanced/formatting), the format of the content returned to a request can be determined by headers the client provides indicating its preferred manner of receiving the content.</span></span>

<span data-ttu-id="79fef-116">将 ASP.NET Web API 控制器迁移到 ASP.NET Core 时，需要更改一些组件（如果存在）。</span><span class="sxs-lookup"><span data-stu-id="79fef-116">When migrating ASP.NET Web API controllers to ASP.NET Core, a few components need to be changed if they exist.</span></span> <span data-ttu-id="79fef-117">其中包括对 `ApiController` 基类、 `System.Web.Http` 命名空间和接口的引用 `IHttpActionResult` 。</span><span class="sxs-lookup"><span data-stu-id="79fef-117">These include references to the `ApiController` base class, the `System.Web.Http` namespace, and the `IHttpActionResult` interface.</span></span> <span data-ttu-id="79fef-118">[有关如何迁移这些特定差异的建议](/aspnet/core/migration/webapi)，请参阅文档。</span><span class="sxs-lookup"><span data-stu-id="79fef-118">Refer to the [documentation for recommendations on how to migrate these specific differences](/aspnet/core/migration/webapi).</span></span> <span data-ttu-id="79fef-119">请注意，ASP.NET Core 中的 API 操作的首选返回类型为 `ActionResult<T>` 。</span><span class="sxs-lookup"><span data-stu-id="79fef-119">Note that the preferred return type for API actions in ASP.NET Core is `ActionResult<T>`.</span></span>

<span data-ttu-id="79fef-120">此外，ASP.NET Core 中 `[ChildActionOnly]` 不支持特性。</span><span class="sxs-lookup"><span data-stu-id="79fef-120">In addition, the `[ChildActionOnly]` attribute isn't supported in ASP.NET Core.</span></span> <span data-ttu-id="79fef-121">在 ASP.NET Core 中，可以使用 [视图组件](/aspnet/core/mvc/views/view-components)来实现类似功能。</span><span class="sxs-lookup"><span data-stu-id="79fef-121">In ASP.NET Core, similar functionality is achieved using [View Components](/aspnet/core/mvc/views/view-components).</span></span>

<span data-ttu-id="79fef-122">ASP.NET Core 包括两个新属性： [ConsumesAttribute](/dotnet/api/microsoft.aspnetcore.mvc.consumesattribute) 和 [ProducesAttribute](/dotnet/api/microsoft.aspnetcore.mvc.producesattribute)。</span><span class="sxs-lookup"><span data-stu-id="79fef-122">ASP.NET Core includes two new attributes: [ConsumesAttribute](/dotnet/api/microsoft.aspnetcore.mvc.consumesattribute) and [ProducesAttribute](/dotnet/api/microsoft.aspnetcore.mvc.producesattribute).</span></span> <span data-ttu-id="79fef-123">它们用于指定操作使用或生成的类型，这对于使用 [Swagger/OpenAPI](/aspnet/core/tutorials/web-api-help-pages-using-swagger)等工具进行路由和记录 API 非常有用。</span><span class="sxs-lookup"><span data-stu-id="79fef-123">These are used to specify the type an action consumes or produces, which can be helpful for routing and documenting the API using tools like [Swagger/OpenAPI](/aspnet/core/tutorials/web-api-help-pages-using-swagger).</span></span>

## <a name="references"></a><span data-ttu-id="79fef-124">参考</span><span class="sxs-lookup"><span data-stu-id="79fef-124">References</span></span>

- [<span data-ttu-id="79fef-125">设置 ASP.NET Core Web API 中响应数据的格式</span><span class="sxs-lookup"><span data-stu-id="79fef-125">Format response data in ASP.NET Core Web API</span></span>](/aspnet/core/web-api/advanced/formatting)
- [<span data-ttu-id="79fef-126">从 ASP.NET Web API 迁移到 ASP.NET Core</span><span class="sxs-lookup"><span data-stu-id="79fef-126">Migrate from ASP.NET Web API to ASP.NET Core</span></span>](/aspnet/core/migration/webapi)

>[!div class="step-by-step"]
><span data-ttu-id="79fef-127">[上一页](identity-differences.md)
>[下一页](razor-differences.md)</span><span class="sxs-lookup"><span data-stu-id="79fef-127">[Previous](identity-differences.md)
[Next](razor-differences.md)</span></span>
