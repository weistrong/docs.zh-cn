---
title: 中断性变更：Razor：RazorEngine API 已标记为已过时
description: 了解 ASP.NET Core 6.0 中的中断性变更，其标题为：Razor：RazorEngine API 已标记为已过时
author: scottaddie
ms.author: scaddie
ms.date: 02/09/2021
ms.openlocfilehash: 173ff0ee5c062f050c967c6edc7bed333d1a2031
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100488193"
---
# <a name="razor-razorengine-apis-marked-obsolete"></a><span data-ttu-id="9a8e0-103">Razor：RazorEngine API 已标记为已过时</span><span class="sxs-lookup"><span data-stu-id="9a8e0-103">Razor: RazorEngine APIs marked obsolete</span></span>

<span data-ttu-id="9a8e0-104">与 Blazor 中的 <xref:Microsoft.AspNetCore.Razor.Language.RazorEngine> 类型相关的类型已标记为已过时。</span><span class="sxs-lookup"><span data-stu-id="9a8e0-104">Types related to the <xref:Microsoft.AspNetCore.Razor.Language.RazorEngine> type in Blazor have been marked as obsolete.</span></span>

## <a name="version-introduced"></a><span data-ttu-id="9a8e0-105">引入的版本</span><span class="sxs-lookup"><span data-stu-id="9a8e0-105">Version introduced</span></span>

<span data-ttu-id="9a8e0-106">6.0 预览版 1</span><span class="sxs-lookup"><span data-stu-id="9a8e0-106">6.0 Preview 1</span></span>

## <a name="old-behavior"></a><span data-ttu-id="9a8e0-107">旧行为</span><span class="sxs-lookup"><span data-stu-id="9a8e0-107">Old behavior</span></span>

<span data-ttu-id="9a8e0-108">`RazorEngine` API 未过时。</span><span class="sxs-lookup"><span data-stu-id="9a8e0-108">The `RazorEngine` APIs aren't obsolete.</span></span>

## <a name="new-behavior"></a><span data-ttu-id="9a8e0-109">新行为</span><span class="sxs-lookup"><span data-stu-id="9a8e0-109">New behavior</span></span>

<span data-ttu-id="9a8e0-110">`RazorEngine` API 已过时。</span><span class="sxs-lookup"><span data-stu-id="9a8e0-110">The `RazorEngine` APIs are obsolete.</span></span>

## <a name="reason-for-change"></a><span data-ttu-id="9a8e0-111">更改原因</span><span class="sxs-lookup"><span data-stu-id="9a8e0-111">Reason for change</span></span>

<span data-ttu-id="9a8e0-112">`RazorEngine` 类型已弃用，取而代之的是 <xref:Microsoft.AspNetCore.Razor.Language.RazorProjectEngine> 类型。</span><span class="sxs-lookup"><span data-stu-id="9a8e0-112">The `RazorEngine` type has been deprecated in favor of the <xref:Microsoft.AspNetCore.Razor.Language.RazorProjectEngine> type.</span></span>

## <a name="recommended-action"></a><span data-ttu-id="9a8e0-113">建议的操作</span><span class="sxs-lookup"><span data-stu-id="9a8e0-113">Recommended action</span></span>

<span data-ttu-id="9a8e0-114">将源代码从 `RazorEngine` 类型迁移到 `RazorProjectEngine` 类型。</span><span class="sxs-lookup"><span data-stu-id="9a8e0-114">Migrate source code from the `RazorEngine` type to the `RazorProjectEngine` type.</span></span>

## <a name="affected-apis"></a><span data-ttu-id="9a8e0-115">受影响的 API</span><span class="sxs-lookup"><span data-stu-id="9a8e0-115">Affected APIs</span></span>

- [<span data-ttu-id="9a8e0-116">Microsoft.AspNetCore.Mvc.Razor.Extensions.InjectDirective.Register</span><span class="sxs-lookup"><span data-stu-id="9a8e0-116">Microsoft.AspNetCore.Mvc.Razor.Extensions.InjectDirective.Register</span></span>](/dotnet/api/microsoft.aspnetcore.mvc.razor.extensions.injectdirective.register?view=aspnetcore-3.1&preserve-view=true)
- [<span data-ttu-id="9a8e0-117">Microsoft.AspNetCore.Mvc.Razor.Extensions.ModelDirective.Register</span><span class="sxs-lookup"><span data-stu-id="9a8e0-117">Microsoft.AspNetCore.Mvc.Razor.Extensions.ModelDirective.Register</span></span>](/dotnet/api/microsoft.aspnetcore.mvc.razor.extensions.namespacedirective.register?view=aspnetcore-2.2&preserve-view=true)
- [<span data-ttu-id="9a8e0-118">Microsoft.AspNetCore.Mvc.Razor.Extensions.PageDirective.Register</span><span class="sxs-lookup"><span data-stu-id="9a8e0-118">Microsoft.AspNetCore.Mvc.Razor.Extensions.PageDirective.Register</span></span>](/dotnet/api/microsoft.aspnetcore.mvc.razor.extensions.namespacedirective.register?view=aspnetcore-2.2&preserve-view=true)
- [<span data-ttu-id="9a8e0-119">Microsoft.AspNetCore.Razor.Language.Extensions.FunctionsDirective.Register</span><span class="sxs-lookup"><span data-stu-id="9a8e0-119">Microsoft.AspNetCore.Razor.Language.Extensions.FunctionsDirective.Register</span></span>](/dotnet/api/microsoft.aspnetcore.razor.language.extensions.functionsdirective.register?view=aspnetcore-3.0&preserve-view=true)
- [<span data-ttu-id="9a8e0-120">Microsoft.AspNetCore.Razor.Language.Extensions.InheritsDirective.Register</span><span class="sxs-lookup"><span data-stu-id="9a8e0-120">Microsoft.AspNetCore.Razor.Language.Extensions.InheritsDirective.Register</span></span>](/dotnet/api/microsoft.aspnetcore.razor.language.extensions.inheritsdirective.register?view=aspnetcore-3.0&preserve-view=true)
- [<span data-ttu-id="9a8e0-121">Microsoft.AspNetCore.Razor.Language.Extensions.SectionDirective.Register</span><span class="sxs-lookup"><span data-stu-id="9a8e0-121">Microsoft.AspNetCore.Razor.Language.Extensions.SectionDirective.Register</span></span>](/dotnet/api/microsoft.aspnetcore.razor.language.extensions.sectiondirective.register?view=aspnetcore-3.0&preserve-view=true)
- [<span data-ttu-id="9a8e0-122">Microsoft.AspNetCore.Razor.Language.IRazorEngineBuilder</span><span class="sxs-lookup"><span data-stu-id="9a8e0-122">Microsoft.AspNetCore.Razor.Language.IRazorEngineBuilder</span></span>](/dotnet/api/microsoft.aspnetcore.razor.language.irazorenginebuilder?view=aspnetcore-3.0&preserve-view=true)

<!--

## Category

ASP.NET Core

## Affected APIs

- `Overload:Microsoft.AspNetCore.Mvc.Razor.Extensions.InjectDirective.Register`
- `Overload:Microsoft.AspNetCore.Mvc.Razor.Extensions.ModelDirective.Register`
- `Overload:Microsoft.AspNetCore.Mvc.Razor.Extensions.PageDirective.Register`
- `Overload:Microsoft.AspNetCore.Razor.Language.Extensions.FunctionsDirective.Register`
- `Overload:Microsoft.AspNetCore.Razor.Language.Extensions.InheritsDirective.Register`
- `Overload:Microsoft.AspNetCore.Razor.Language.Extensions.SectionDirective.Register`
- `T:Microsoft.AspNetCore.Razor.Language.IRazorEngineBuilder`

-->
