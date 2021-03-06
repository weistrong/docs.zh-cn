---
title: 在 ASP.NET MVC 和 ASP.NET Core 中提供静态文件
description: 与 IIS 上的 ASP.NET MVC 相比，配置 ASP.NET Core 中提供静态文件的支持涉及的内容是什么？
author: ardalis
ms.date: 11/13/2020
ms.openlocfilehash: 02f84a6985835502c24db8cc68db24c8de086b18
ms.sourcegitcommit: 42d436ebc2a7ee02fc1848c7742bc7d80e13fc2f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/04/2021
ms.locfileid: "102401060"
---
# <a name="serve-static-files-in-aspnet-mvc-and-aspnet-core"></a><span data-ttu-id="37740-103">在 ASP.NET MVC 和 ASP.NET Core 中提供静态文件</span><span class="sxs-lookup"><span data-stu-id="37740-103">Serve static files in ASP.NET MVC and ASP.NET Core</span></span>

<span data-ttu-id="37740-104">大多数 web 应用都涉及服务器端逻辑和静态文件的组合，必须按原样发送到客户端。</span><span class="sxs-lookup"><span data-stu-id="37740-104">Most web apps involve a combination of server-side logic and static files that must be sent to the client as-is.</span></span> <span data-ttu-id="37740-105">如何从 ASP.NET MVC 迁移到 ASP.NET Core 处理静态文件？</span><span class="sxs-lookup"><span data-stu-id="37740-105">How should your migration from ASP.NET MVC to ASP.NET Core handle serving static files?</span></span>

## <a name="host-static-files-in-aspnet-mvc"></a><span data-ttu-id="37740-106">在 ASP.NET MVC 中托管静态文件</span><span class="sxs-lookup"><span data-stu-id="37740-106">Host static files in ASP.NET MVC</span></span>

<span data-ttu-id="37740-107">IIS 托管的 ASP.NET MVC 应用程序通常会直接从应用程序中托管静态文件。</span><span class="sxs-lookup"><span data-stu-id="37740-107">ASP.NET MVC apps, hosted by IIS, typically host static files directly from the app.</span></span> <span data-ttu-id="37740-108">ASP.NET MVC 支持将静态文件与应在服务器上保持为私有的文件并行放置。</span><span class="sxs-lookup"><span data-stu-id="37740-108">ASP.NET MVC supports placing static files side by side with files that should be kept private on the server.</span></span> <span data-ttu-id="37740-109">IIS 和 ASP.NET 要求显式限制某些文件或文件扩展名，以在托管 ASP.NET 应用的文件夹中提供服务。</span><span class="sxs-lookup"><span data-stu-id="37740-109">IIS and ASP.NET require explicitly restricting certain files or file extensions from being served from the folder in which an ASP.NET app is hosted.</span></span>

<span data-ttu-id="37740-110">对于许多静态文件，使用内容交付网络 (CDN) 是一种很好的做法。</span><span class="sxs-lookup"><span data-stu-id="37740-110">For many static files, using a content delivery network (CDN) is a good practice.</span></span> <span data-ttu-id="37740-111">利用[静态内容宿主](/azure/architecture/patterns/static-content-hosting)，可以提高性能，同时减少应用服务器的负载和带宽。</span><span class="sxs-lookup"><span data-stu-id="37740-111">[Static content hosting](/azure/architecture/patterns/static-content-hosting) allows better performance while reducing load and bandwidth from app servers.</span></span>

## <a name="host-static-files-in-aspnet-core"></a><span data-ttu-id="37740-112">在 ASP.NET Core 中托管静态文件</span><span class="sxs-lookup"><span data-stu-id="37740-112">Host static files in ASP.NET Core</span></span>

<span data-ttu-id="37740-113">这可能是不可思议，但 ASP.NET Core 对静态文件没有内置支持。</span><span class="sxs-lookup"><span data-stu-id="37740-113">It may be surprising, but ASP.NET Core doesn't have built-in support for static files.</span></span> <span data-ttu-id="37740-114">此功能始终作为 ASP.NET 的一部分提供，由 IIS 启用，不是 ASP.NET Core 或其 Kestrel web 服务器所固有的。</span><span class="sxs-lookup"><span data-stu-id="37740-114">This feature that has always existed as just a part of ASP.NET, enabled by IIS, isn't intrinsic to ASP.NET Core or its Kestrel web server.</span></span> <span data-ttu-id="37740-115">若要从 ASP.NET Core 应用提供静态文件，必须配置 [静态文件中间件](/aspnet/core/fundamentals/static-files)。</span><span class="sxs-lookup"><span data-stu-id="37740-115">To serve static files from an ASP.NET Core app, you must configure [static files middleware](/aspnet/core/fundamentals/static-files).</span></span>

<span data-ttu-id="37740-116">在配置了静态文件中间件的情况下，ASP.NET Core 应用将为位于特定文件夹中的所有文件提供 (通常 */wwwroot*) 。</span><span class="sxs-lookup"><span data-stu-id="37740-116">With static files middleware configured, an ASP.NET Core app will serve all files located in a certain folder (typically */wwwroot*).</span></span> <span data-ttu-id="37740-117">应用程序或项目文件夹中的其他文件没有被服务器意外公开的风险。</span><span class="sxs-lookup"><span data-stu-id="37740-117">No other files in the app or project folder are at risk of being accidentally exposed by the server.</span></span> <span data-ttu-id="37740-118">不需要配置基于文件名或扩展的特殊限制，这与 IIS 的情况相同。</span><span class="sxs-lookup"><span data-stu-id="37740-118">No special restrictions based on file names or extensions need to be configured, as is the case with IIS.</span></span> <span data-ttu-id="37740-119">相反，开发人员在将文件放入 *wwwroot* 文件夹时，显式选择公开文件。</span><span class="sxs-lookup"><span data-stu-id="37740-119">Instead, developers explicitly choose to expose files publicly when they place them in the *wwwroot* folder.</span></span> <span data-ttu-id="37740-120">默认情况下，不共享此文件夹之外的文件。</span><span class="sxs-lookup"><span data-stu-id="37740-120">By default, files outside of this folder aren't shared.</span></span>

<span data-ttu-id="37740-121">因为对静态文件的支持使用中间件，所以任何其他中间件都可以作为同一请求管道的一部分应用。</span><span class="sxs-lookup"><span data-stu-id="37740-121">Because support for static files uses middleware, any other middleware can be applied as part of the same request pipeline.</span></span> <span data-ttu-id="37740-122">中间件的示例包括身份验证、缓存和压缩。</span><span class="sxs-lookup"><span data-stu-id="37740-122">Examples of middleware include authentication, caching, and compression.</span></span>

<span data-ttu-id="37740-123">当然，对于 ASP.NET Core 的应用程序，Cdn 仍是一个不错的选择，因为它们在 ASP.NET MVC 应用程序中使用的原因相同。</span><span class="sxs-lookup"><span data-stu-id="37740-123">Of course, CDNs remain a good choice for ASP.NET Core apps for all the same reasons they're used in ASP.NET MVC apps.</span></span> <span data-ttu-id="37740-124">作为准备迁移到 .NET Core 的一部分，如果你的应用程序可以通过使用 CDN 实现某些优点，则在迁移到 .NET Core 之前，最好将静态文件迁移到 CDN。</span><span class="sxs-lookup"><span data-stu-id="37740-124">As part of preparing to migrate to .NET Core, if there are benefits your app could realize from using a CDN, it would be good to move static files to a CDN before migrating to .NET Core.</span></span> <span data-ttu-id="37740-125">这样做可以减少静态资产的迁移工作总体范围。</span><span class="sxs-lookup"><span data-stu-id="37740-125">Doing so reduces the migration effort's overall scope for static assets.</span></span>

## <a name="references"></a><span data-ttu-id="37740-126">参考</span><span class="sxs-lookup"><span data-stu-id="37740-126">References</span></span>

- [<span data-ttu-id="37740-127">静态内容托管</span><span class="sxs-lookup"><span data-stu-id="37740-127">Static content hosting</span></span>](/azure/architecture/patterns/static-content-hosting)
- [<span data-ttu-id="37740-128">ASP.NET Core 中的静态文件</span><span class="sxs-lookup"><span data-stu-id="37740-128">Static files in ASP.NET Core</span></span>](/aspnet/core/fundamentals/static-files)

>[!div class="step-by-step"]
><span data-ttu-id="37740-129">[上一页](hosting-differences.md)
>[下一页](dependency-injection-differences.md)</span><span class="sxs-lookup"><span data-stu-id="37740-129">[Previous](hosting-differences.md)
[Next](dependency-injection-differences.md)</span></span>
