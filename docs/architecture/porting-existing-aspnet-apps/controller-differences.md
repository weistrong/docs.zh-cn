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
# <a name="compare-controllers-in-aspnet-mvc-and-web-api-with-controllers-in-aspnet-core"></a>将 ASP.NET MVC 和 Web API 中的控制器与 ASP.NET Core 中的控制器进行比较

在 ASP.NET MVC 5 和 Web API 2 中，有两种不同 `Controller` 的基类型。 继承自的 MVC 控制器 `Controller` ;从继承的 Web API 控制器 `ApiController` 。 在 ASP.NET Core 中，已合并此对象层次结构。 建议 ASP.NET Core 中的 API 控制器继承 `ControllerBase` 并添加 `[ApiController]` 属性。 基于标准视图的 MVC 控制器应从继承 `Controller` 。

在这两个框架中，控制器都用于组织操作方法集。 除了在操作级别，还可以在控制器级别应用筛选器和路由。 通过使用 `Controller` 具有默认行为的自定义基类型和应用于它们的特性，可以进一步扩展这些约定。

在 ASP.NET MVC 中，不支持内容协商。 ASP.NET Web API 2 支持内容协商，ASP.NET Core。 使用 [内容协商](/aspnet/core/web-api/advanced/formatting)，返回到请求的内容格式可由客户端提供的标头来确定，客户端提供该内容是为了接收内容的首选方式。

将 ASP.NET Web API 控制器迁移到 ASP.NET Core 时，需要更改一些组件（如果存在）。 其中包括对 `ApiController` 基类、 `System.Web.Http` 命名空间和接口的引用 `IHttpActionResult` 。 [有关如何迁移这些特定差异的建议](/aspnet/core/migration/webapi)，请参阅文档。 请注意，ASP.NET Core 中的 API 操作的首选返回类型为 `ActionResult<T>` 。

此外，ASP.NET Core 中 `[ChildActionOnly]` 不支持特性。 在 ASP.NET Core 中，可以使用 [视图组件](/aspnet/core/mvc/views/view-components)来实现类似功能。

ASP.NET Core 包括两个新属性： [ConsumesAttribute](/dotnet/api/microsoft.aspnetcore.mvc.consumesattribute) 和 [ProducesAttribute](/dotnet/api/microsoft.aspnetcore.mvc.producesattribute)。 它们用于指定操作使用或生成的类型，这对于使用 [Swagger/OpenAPI](/aspnet/core/tutorials/web-api-help-pages-using-swagger)等工具进行路由和记录 API 非常有用。

## <a name="references"></a>参考

- [设置 ASP.NET Core Web API 中响应数据的格式](/aspnet/core/web-api/advanced/formatting)
- [从 ASP.NET Web API 迁移到 ASP.NET Core](/aspnet/core/migration/webapi)

>[!div class="step-by-step"]
>[上一页](identity-differences.md)
>[下一页](razor-differences.md)
