---
title: 比较 ASP.NET MVC 和 ASP.NET Core 中的 Razor 使用情况
description: Razor 在 ASP.NET MVC 和 ASP.NET Core 之间有何区别？
author: ardalis
ms.date: 11/13/2020
ms.openlocfilehash: a9f7fa2e6b8c0c6bf61c743cf8c956b1ad09713c
ms.sourcegitcommit: 42d436ebc2a7ee02fc1848c7742bc7d80e13fc2f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/04/2021
ms.locfileid: "102401066"
---
# <a name="compare-razor-usage-in-aspnet-mvc-and-aspnet-core"></a><span data-ttu-id="7a90f-103">比较 ASP.NET MVC 和 ASP.NET Core 中的 Razor 使用情况</span><span class="sxs-lookup"><span data-stu-id="7a90f-103">Compare Razor usage in ASP.NET MVC and ASP.NET Core</span></span>

<span data-ttu-id="7a90f-104">Razor 的基本语法在 ASP.NET MVC 和 ASP.NET Core 之间没有明显变化。</span><span class="sxs-lookup"><span data-stu-id="7a90f-104">The basic syntax of Razor hasn't changed substantially between ASP.NET MVC and ASP.NET Core.</span></span> <span data-ttu-id="7a90f-105">但是，在迁移时，应考虑某些差异，如 [标记帮助](/aspnet/core/mvc/views/tag-helpers/intro) 程序和 Razor Pages 的引入。</span><span class="sxs-lookup"><span data-stu-id="7a90f-105">However, there are certain differences, such as the introduction of [Tag Helpers](/aspnet/core/mvc/views/tag-helpers/intro) and Razor Pages, that should be considered when migrating.</span></span> <span data-ttu-id="7a90f-106">如果应用大量使用自定义 Razor 功能，请参阅 [ASP.NET Core 的 Razor 语法参考](/aspnet/core/razor-pages) ，了解迁移到 ASP.NET Core 时可能需要进行哪些更改。</span><span class="sxs-lookup"><span data-stu-id="7a90f-106">If your app makes heavy use of custom Razor functionality, refer to the [Razor syntax reference for ASP.NET Core](/aspnet/core/razor-pages) to see what changes may be required when you migrate to ASP.NET Core.</span></span>

## <a name="tag-helpers"></a><span data-ttu-id="7a90f-107">标记帮助程序</span><span class="sxs-lookup"><span data-stu-id="7a90f-107">Tag Helpers</span></span>

<span data-ttu-id="7a90f-108">标记帮助程序使服务器端代码可以在 Razor 文件中参与创建和呈现 HTML 元素。</span><span class="sxs-lookup"><span data-stu-id="7a90f-108">Tag Helpers enable server-side code to participate in creating and rendering HTML elements in Razor files.</span></span> <span data-ttu-id="7a90f-109">与 HTML 帮助程序相比，它们提供了许多优点，应尽可能地用于替代 HTML 帮助器。</span><span class="sxs-lookup"><span data-stu-id="7a90f-109">They offer many advantages over HTML Helpers and should be used in place of HTML Helpers wherever possible.</span></span> <span data-ttu-id="7a90f-110">它们提供 HTML 友好的开发体验，因为它们看起来像标准 HTML，并且大多数设计用于编辑 HTML 的工具都将忽略这些体验。</span><span class="sxs-lookup"><span data-stu-id="7a90f-110">They provide an HTML-friendly development experience, since they look like standard HTML and are ignored by most tooling designed to edit HTML.</span></span> <span data-ttu-id="7a90f-111">在 _Visual Studio_ 中，有丰富的 IntelliSense 支持，可用于创建带有标记帮助程序的 HTML 和 Razor 标记。</span><span class="sxs-lookup"><span data-stu-id="7a90f-111">Within _Visual Studio_, there's rich IntelliSense support for creating HTML and Razor markup with Tag Helpers.</span></span> <span data-ttu-id="7a90f-112">标记帮助程序可以从 Razor 文件中的声明性标记提供简单或复杂的行为。</span><span class="sxs-lookup"><span data-stu-id="7a90f-112">Tag Helpers can provide simple or complex behavior from declarative markup in Razor files.</span></span>

## <a name="razor-pages"></a><span data-ttu-id="7a90f-113">Razor 页面</span><span class="sxs-lookup"><span data-stu-id="7a90f-113">Razor Pages</span></span>

<span data-ttu-id="7a90f-114">Razor Pages 提供对基于页面和窗体的应用的控制器、操作和视图的替代方法。</span><span class="sxs-lookup"><span data-stu-id="7a90f-114">Razor Pages offer an alternative to controllers, actions, and views for page- and form-based apps.</span></span> <span data-ttu-id="7a90f-115">[Razor Pages 与本章前面部分的 ASP.NET MVC 进行比较](./comparing-razor-pages-aspnet-mvc.md)。</span><span class="sxs-lookup"><span data-stu-id="7a90f-115">[Razor Pages were compared to ASP.NET MVC earlier in this chapter](./comparing-razor-pages-aspnet-mvc.md).</span></span>

## <a name="references"></a><span data-ttu-id="7a90f-116">参考</span><span class="sxs-lookup"><span data-stu-id="7a90f-116">References</span></span>

- [<span data-ttu-id="7a90f-117">从 ASP.NET MVC 迁移到 ASP.NET Core MVC：控制器和视图</span><span class="sxs-lookup"><span data-stu-id="7a90f-117">Migrate from ASP.NET MVC to ASP.NET Core MVC: Controllers and Views</span></span>](/aspnet/core/migration/mvc#migrate-controllers-and-views)
- [<span data-ttu-id="7a90f-118">ASP.NET Core 中的标记帮助程序</span><span class="sxs-lookup"><span data-stu-id="7a90f-118">Tag Helpers in ASP.NET Core</span></span>](/aspnet/core/mvc/views/tag-helpers/intro)
- [<span data-ttu-id="7a90f-119">ASP.NET Core 中的 Razor 页面介绍</span><span class="sxs-lookup"><span data-stu-id="7a90f-119">Introduction to Razor Pages in ASP.NET Core</span></span>](/aspnet/core/razor-pages)
- [<span data-ttu-id="7a90f-120">ASP.NET Core 的 Razor 语法参考</span><span class="sxs-lookup"><span data-stu-id="7a90f-120">Razor syntax reference for ASP.NET Core</span></span>](/aspnet/core/razor-pages)

>[!div class="step-by-step"]
><span data-ttu-id="7a90f-121">[上一页](controller-differences.md)
>[下一页](signalr-differences.md)</span><span class="sxs-lookup"><span data-stu-id="7a90f-121">[Previous](controller-differences.md)
[Next](signalr-differences.md)</span></span>
