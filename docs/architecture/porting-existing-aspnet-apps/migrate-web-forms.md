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
# <a name="strategies-for-migrating-aspnet-web-forms-apps"></a><span data-ttu-id="e43ae-103">有关迁移 ASP.NET Web Forms 应用的策略</span><span class="sxs-lookup"><span data-stu-id="e43ae-103">Strategies for migrating ASP.NET Web Forms apps</span></span>

<span data-ttu-id="e43ae-104">本书提供将大型 ASP.NET MVC 和 Web API 应用迁移到 .NET Core 的指南。</span><span class="sxs-lookup"><span data-stu-id="e43ae-104">This book offers guidance for migrating large ASP.NET MVC and Web API apps to .NET Core.</span></span> <span data-ttu-id="e43ae-105">其中一些 ASP.NET 应用还可能包括 Web Forms (*.aspx*) 必须解决的页面。</span><span class="sxs-lookup"><span data-stu-id="e43ae-105">Some of these ASP.NET apps may also include Web Forms (*.aspx*) pages that must be addressed.</span></span> <span data-ttu-id="e43ae-106">.NET Core (和 ASP.NET 网页) 不支持 ASP.NET Web 窗体。</span><span class="sxs-lookup"><span data-stu-id="e43ae-106">ASP.NET Web Forms isn't supported in .NET Core (nor are ASP.NET Web Pages).</span></span> <span data-ttu-id="e43ae-107">通常情况下，必须在迁移到 ASP.NET Core 时重写这些页的功能。</span><span class="sxs-lookup"><span data-stu-id="e43ae-107">Typically, the functionality of these pages must be rewritten when porting to ASP.NET Core.</span></span> <span data-ttu-id="e43ae-108">但是，可以在此类迁移之前或在此过程中应用某些策略，以帮助减少所需的整体工作量。</span><span class="sxs-lookup"><span data-stu-id="e43ae-108">There are, however, some strategies you can apply before or during such migration to help reduce the overall effort required.</span></span>

<span data-ttu-id="e43ae-109">Web 窗体将继续受到一段时间的支持。</span><span class="sxs-lookup"><span data-stu-id="e43ae-109">Web Forms will continue to be supported for quite some time.</span></span> <span data-ttu-id="e43ae-110">一种选择是在 ASP.NET 4.x 应用程序中保留此功能。</span><span class="sxs-lookup"><span data-stu-id="e43ae-110">One option may be to keep this functionality in an ASP.NET 4.x app.</span></span>

## <a name="separate-business-logic-and-other-concerns"></a><span data-ttu-id="e43ae-111">分隔业务逻辑和其他问题</span><span class="sxs-lookup"><span data-stu-id="e43ae-111">Separate business logic and other concerns</span></span>

<span data-ttu-id="e43ae-112">ASP.NET Web 窗体页中的代码越少，效果就越好。</span><span class="sxs-lookup"><span data-stu-id="e43ae-112">The less code in your ASP.NET Web Forms pages, the better.</span></span> <span data-ttu-id="e43ae-113">如果可能，请在单独的类中保留业务逻辑和其他问题，例如数据访问，理想情况下为单独的类库。</span><span class="sxs-lookup"><span data-stu-id="e43ae-113">When possible, keep business logic and other concerns like data access in separate classes, ideally in separate class libraries.</span></span> <span data-ttu-id="e43ae-114">这些类库可以移植到 .NET Standard 并由任何 ASP.NET Core 应用程序使用。</span><span class="sxs-lookup"><span data-stu-id="e43ae-114">These class libraries can be ported to .NET Standard and consumed by any ASP.NET Core app.</span></span>

## <a name="implement-client-behavior-and-web-apis"></a><span data-ttu-id="e43ae-115">实现客户端行为和 web Api</span><span class="sxs-lookup"><span data-stu-id="e43ae-115">Implement client behavior and web APIs</span></span>

<span data-ttu-id="e43ae-116">请考虑在 Web 窗体或浏览器中实现逻辑之间的选择，并提供 API 调用的帮助。</span><span class="sxs-lookup"><span data-stu-id="e43ae-116">Consider the choice between implementing logic in Web Forms or in the browser with the help of API calls.</span></span> <span data-ttu-id="e43ae-117">优选后者。</span><span class="sxs-lookup"><span data-stu-id="e43ae-117">Favor the latter.</span></span> <span data-ttu-id="e43ae-118">支持将 Api 迁移到 ASP.NET Core。</span><span class="sxs-lookup"><span data-stu-id="e43ae-118">Migrating APIs to ASP.NET Core is supported.</span></span> <span data-ttu-id="e43ae-119">客户端行为应独立于应用正在使用的服务器端堆栈。</span><span class="sxs-lookup"><span data-stu-id="e43ae-119">Client-side behavior should be independent of the server-side stack your app is using.</span></span> <span data-ttu-id="e43ae-120">使用此方法的好处是，提供更具响应能力的用户体验。</span><span class="sxs-lookup"><span data-stu-id="e43ae-120">Using this approach has the added benefit of providing a more responsive user experience.</span></span>

## <a name="consider-blazor"></a><span data-ttu-id="e43ae-121">请考虑 Blazor</span><span class="sxs-lookup"><span data-stu-id="e43ae-121">Consider Blazor</span></span>

<span data-ttu-id="e43ae-122">Blazor 使你能够用 c # 而不是 JavaScript 构建交互式 web Ui。</span><span class="sxs-lookup"><span data-stu-id="e43ae-122">Blazor lets you build interactive web UIs with C# instead of JavaScript.</span></span> <span data-ttu-id="e43ae-123">它可以在服务器上或使用 WebAssembly 在浏览器中运行。</span><span class="sxs-lookup"><span data-stu-id="e43ae-123">It can run on the server or in the browser using WebAssembly.</span></span> <span data-ttu-id="e43ae-124">ASP.NET Web 窗体应用程序可能会逐页面移植到 Blazor 应用。</span><span class="sxs-lookup"><span data-stu-id="e43ae-124">ASP.NET Web Forms apps may be ported page-by-page to Blazor apps.</span></span> <span data-ttu-id="e43ae-125">有关将 Web 窗体应用移植到 Blazor 的详细信息，请参阅 [Blazor for ASP.NET Web Forms 开发人员](https://devblogs.microsoft.com/aspnet/blazor-aspnet-webforms-ebook/)。</span><span class="sxs-lookup"><span data-stu-id="e43ae-125">For more information on porting Web Forms apps to Blazor, see [Blazor for ASP.NET Web Forms Developers](https://devblogs.microsoft.com/aspnet/blazor-aspnet-webforms-ebook/).</span></span> <span data-ttu-id="e43ae-126">此外，许多 Web 窗体控件已作为开放源代码社区项目（ [Blazor Web 窗体组件](https://fritzandfriends.github.io/BlazorWebFormsComponents/)）的一部分移植到 Blazor。</span><span class="sxs-lookup"><span data-stu-id="e43ae-126">In addition, many Web Forms controls have been ported to Blazor as part of an open-source community project, [Blazor Web Forms Components](https://fritzandfriends.github.io/BlazorWebFormsComponents/).</span></span> <span data-ttu-id="e43ae-127">使用这些组件，可以更轻松地将 Web 窗体页移植到 Blazor，即使它们使用内置 Web 窗体控件。</span><span class="sxs-lookup"><span data-stu-id="e43ae-127">With these components, you can more easily port Web Forms pages to Blazor even if they use the built-in Web Forms controls.</span></span>

## <a name="summary"></a><span data-ttu-id="e43ae-128">总结</span><span class="sxs-lookup"><span data-stu-id="e43ae-128">Summary</span></span>

<span data-ttu-id="e43ae-129">不支持直接从 ASP.NET Web 窗体迁移到 ASP.NET Core。</span><span class="sxs-lookup"><span data-stu-id="e43ae-129">Migrating directly from ASP.NET Web Forms to ASP.NET Core isn't supported.</span></span> <span data-ttu-id="e43ae-130">但是，有一些策略可使移动到 ASP.NET Core 变得更加容易。</span><span class="sxs-lookup"><span data-stu-id="e43ae-130">However, there are strategies to make moving to ASP.NET Core easier.</span></span> <span data-ttu-id="e43ae-131">可以通过以下方式将 Web 窗体功能迁移到 ASP.NET Core：</span><span class="sxs-lookup"><span data-stu-id="e43ae-131">You can migrate your Web Forms functionality to ASP.NET Core successfully by:</span></span>

* <span data-ttu-id="e43ae-132">使非 web 功能从项目中排除。</span><span class="sxs-lookup"><span data-stu-id="e43ae-132">Keeping non-web functionality out of your projects.</span></span>
* <span data-ttu-id="e43ae-133">尽可能使用 web Api。</span><span class="sxs-lookup"><span data-stu-id="e43ae-133">Using web APIs wherever possible.</span></span>
* <span data-ttu-id="e43ae-134">考虑使用 Blazor 作为更新式 UI 的选项。</span><span class="sxs-lookup"><span data-stu-id="e43ae-134">Considering Blazor as an option for a more modern UI.</span></span>

## <a name="references"></a><span data-ttu-id="e43ae-135">参考</span><span class="sxs-lookup"><span data-stu-id="e43ae-135">References</span></span>

- [<span data-ttu-id="e43ae-136">免费电子书： Blazor for ASP.NET Web Forms 开发人员</span><span class="sxs-lookup"><span data-stu-id="e43ae-136">Free e-book: Blazor for ASP.NET Web Forms Developers</span></span>](https://devblogs.microsoft.com/aspnet/blazor-aspnet-webforms-ebook/)
- [<span data-ttu-id="e43ae-137"> (社区项目的 Blazor Web 窗体组件) </span><span class="sxs-lookup"><span data-stu-id="e43ae-137">Blazor Web Forms Components (Community Project)</span></span>](https://fritzandfriends.github.io/BlazorWebFormsComponents/)

>[!div class="step-by-step"]
><span data-ttu-id="e43ae-138">[上一页](incremental-migration-strategies.md)
>[下一页](deployment-strategies.md)</span><span class="sxs-lookup"><span data-stu-id="e43ae-138">[Previous](incremental-migration-strategies.md)
[Next](deployment-strategies.md)</span></span>
