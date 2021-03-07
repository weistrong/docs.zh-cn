---
title: ASP.NET MVC 和 ASP.NET Core 之间的体系结构差异
description: 查看 ASP.NET 与 ASP.NET Core 之间的体系结构差异。
author: ardalis
ms.date: 11/13/2020
ms.openlocfilehash: 96477f2393482380eee9891e9b2dbbb6445e15bd
ms.sourcegitcommit: 42d436ebc2a7ee02fc1848c7742bc7d80e13fc2f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/04/2021
ms.locfileid: "102401100"
---
# <a name="architectural-differences-between-aspnet-mvc-and-aspnet-core"></a><span data-ttu-id="0caef-103">ASP.NET MVC 和 ASP.NET Core 之间的体系结构差异</span><span class="sxs-lookup"><span data-stu-id="0caef-103">Architectural differences between ASP.NET MVC and ASP.NET Core</span></span>

[!INCLUDE [book-preview](../../../includes/book-preview.md)]

<span data-ttu-id="0caef-104">.NET Framework 和 ASP.NET Core 上的 ASP.NET MVC 之间存在许多不同的体系结构差异。</span><span class="sxs-lookup"><span data-stu-id="0caef-104">There are many architectural differences between ASP.NET MVC on .NET Framework and ASP.NET Core.</span></span> <span data-ttu-id="0caef-105">当团队评估将 ASP.NET MVC 应用程序迁移到 ASP.NET Core 所涉及的工作时，必须广泛地了解这些差异。</span><span class="sxs-lookup"><span data-stu-id="0caef-105">It's important to have a broad understanding of these differences as teams evaluate the work involved in porting their ASP.NET MVC apps to ASP.NET Core.</span></span> <span data-ttu-id="0caef-106">本章介绍 ASP.NET Core 与 ASP.NET MVC 明显不同的各种方式。</span><span class="sxs-lookup"><span data-stu-id="0caef-106">This chapter looks at each of the ways in which ASP.NET Core differs substantially from ASP.NET MVC.</span></span>

## <a name="breaking-changes"></a><span data-ttu-id="0caef-107">中断性变更</span><span class="sxs-lookup"><span data-stu-id="0caef-107">Breaking changes</span></span>

<span data-ttu-id="0caef-108">.NET Core 是一种跨平台的 .NET Framework 重写。</span><span class="sxs-lookup"><span data-stu-id="0caef-108">.NET Core is a cross-platform rewrite of .NET Framework.</span></span> <span data-ttu-id="0caef-109">[这两个框架之间](../../core/compatibility/fx-core.md)存在很多重大更改。</span><span class="sxs-lookup"><span data-stu-id="0caef-109">There are many [breaking changes between the two frameworks](../../core/compatibility/fx-core.md).</span></span> <span data-ttu-id="0caef-110">以下各节介绍了如何设计和开发 ASP.NET MVC 和 ASP.NET Core 应用程序之间的具体差异。</span><span class="sxs-lookup"><span data-stu-id="0caef-110">The following sections identify specific differences between how ASP.NET MVC and ASP.NET Core apps are designed and developed.</span></span> <span data-ttu-id="0caef-111">请注意，还应查看相关文档，确定所使用的框架库可能需要更改。</span><span class="sxs-lookup"><span data-stu-id="0caef-111">Take care to also examine the documentation to determine which framework libraries you're using that may need to change.</span></span> <span data-ttu-id="0caef-112">在许多情况下，可以使用替代 NuGet 包来填充 .NET Framework 与 .NET Core 之间留下的任何空白。</span><span class="sxs-lookup"><span data-stu-id="0caef-112">In many cases, a replacement NuGet package exists to fill in any gaps left between .NET Framework and .NET Core.</span></span> <span data-ttu-id="0caef-113">在极少数情况下，可能需要找到第三方解决方案或实现新的自定义代码来解决不兼容问题。</span><span class="sxs-lookup"><span data-stu-id="0caef-113">In rare cases, you may need to find a third-party solution or implement new custom code to address incompatibilities.</span></span>

>[!div class="step-by-step"]
><span data-ttu-id="0caef-114">[上一页](additional-migration-resources.md)
>[下一页](app-startup-differences.md)</span><span class="sxs-lookup"><span data-stu-id="0caef-114">[Previous](additional-migration-resources.md)
[Next](app-startup-differences.md)</span></span>
