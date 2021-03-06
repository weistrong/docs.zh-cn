---
title: 有关迁移 ASP.NET Web Forms 应用的策略
description: 团队可以使用哪些策略将 ASP.NET Web 窗体应用程序迁移到 .NET Core？
author: ardalis
ms.date: 11/13/2020
ms.openlocfilehash: 0b37a37f047de50c347313be14a2228838da6995
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "102401002"
---
# <a name="strategies-for-migrating-aspnet-web-forms-apps"></a>有关迁移 ASP.NET Web Forms 应用的策略

本书提供将大型 ASP.NET MVC 和 Web API 应用迁移到 .NET Core 的指南。 其中一些 ASP.NET 应用还可能包括 Web Forms (*.aspx*) 必须解决的页面。 .NET Core (和 ASP.NET 网页) 不支持 ASP.NET Web 窗体。 通常情况下，必须在迁移到 ASP.NET Core 时重写这些页的功能。 但是，可以在此类迁移之前或在此过程中应用某些策略，以帮助减少所需的整体工作量。

Web 窗体将继续受到一段时间的支持。 一种选择是在 ASP.NET 4.x 应用程序中保留此功能。

## <a name="separate-business-logic-and-other-concerns"></a>分隔业务逻辑和其他问题

ASP.NET Web 窗体页中的代码越少，效果就越好。 如果可能，请在单独的类中保留业务逻辑和其他问题，例如数据访问，理想情况下为单独的类库。 这些类库可以移植到 .NET Standard 并由任何 ASP.NET Core 应用程序使用。

## <a name="implement-client-behavior-and-web-apis"></a>实现客户端行为和 web Api

请考虑在 Web 窗体或浏览器中实现逻辑之间的选择，并提供 API 调用的帮助。 优选后者。 支持将 Api 迁移到 ASP.NET Core。 客户端行为应独立于应用正在使用的服务器端堆栈。 使用此方法的好处是，提供更具响应能力的用户体验。

## <a name="consider-blazor"></a>请考虑 Blazor

Blazor 使你能够用 c # 而不是 JavaScript 构建交互式 web Ui。 它可以在服务器上或使用 WebAssembly 在浏览器中运行。 ASP.NET Web 窗体应用程序可能会逐页面移植到 Blazor 应用。 有关将 Web 窗体应用移植到 Blazor 的详细信息，请参阅 [Blazor for ASP.NET Web Forms 开发人员](https://devblogs.microsoft.com/aspnet/blazor-aspnet-webforms-ebook/)。 此外，许多 Web 窗体控件已作为开放源代码社区项目（ [Blazor Web 窗体组件](https://fritzandfriends.github.io/BlazorWebFormsComponents/)）的一部分移植到 Blazor。 使用这些组件，可以更轻松地将 Web 窗体页移植到 Blazor，即使它们使用内置 Web 窗体控件。

## <a name="summary"></a>总结

不支持直接从 ASP.NET Web 窗体迁移到 ASP.NET Core。 但是，有一些策略可使移动到 ASP.NET Core 变得更加容易。 可以通过以下方式将 Web 窗体功能迁移到 ASP.NET Core：

* 使非 web 功能从项目中排除。
* 尽可能使用 web Api。
* 考虑使用 Blazor 作为更新式 UI 的选项。

## <a name="references"></a>参考

- [免费电子书： Blazor for ASP.NET Web Forms 开发人员](https://devblogs.microsoft.com/aspnet/blazor-aspnet-webforms-ebook/)
- [ (社区项目的 Blazor Web 窗体组件) ](https://fritzandfriends.github.io/BlazorWebFormsComponents/)

>[!div class="step-by-step"]
>[上一页](incremental-migration-strategies.md)
>[下一页](deployment-strategies.md)
