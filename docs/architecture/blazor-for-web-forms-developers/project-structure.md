---
title: 应用的项目结构 Blazor
description: 了解 ASP.NET Web 窗体和项目的项目结构 Blazor 比较。
author: danroth27
ms.author: daroth
no-loc:
- Blazor
- WebAssembly
ms.date: 11/20/2020
ms.openlocfilehash: ba7113c88db728f30812821deaf7c06a80663d1f
ms.sourcegitcommit: a4cecb7389f02c27e412b743f9189bd2a6dea4d6
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/14/2021
ms.locfileid: "98189084"
---
# <a name="project-structure-for-no-locblazor-apps"></a><span data-ttu-id="23ecd-103">应用的项目结构 Blazor</span><span class="sxs-lookup"><span data-stu-id="23ecd-103">Project structure for Blazor apps</span></span>

<span data-ttu-id="23ecd-104">尽管它们有重要的项目结构差异，ASP.NET Web 窗体和 Blazor 共享许多类似的概念。</span><span class="sxs-lookup"><span data-stu-id="23ecd-104">Despite their significant project structure differences, ASP.NET Web Forms and Blazor share many similar concepts.</span></span> <span data-ttu-id="23ecd-105">在这里，我们将查看项目的结构 Blazor ，并将其与 ASP.NET Web 窗体项目进行比较。</span><span class="sxs-lookup"><span data-stu-id="23ecd-105">Here, we'll look at the structure of a Blazor project and compare it to an ASP.NET Web Forms project.</span></span>

<span data-ttu-id="23ecd-106">若要创建第一个 Blazor 应用，请按照[ Blazor 入门步骤](/aspnet/core/blazor/get-started)中的说明进行操作。</span><span class="sxs-lookup"><span data-stu-id="23ecd-106">To create your first Blazor app, follow the instructions in the [Blazor getting started steps](/aspnet/core/blazor/get-started).</span></span> <span data-ttu-id="23ecd-107">您可以按照说明创建 Blazor 服务器应用程序或 Blazor WebAssembly 在 ASP.NET Core 中托管的应用程序。</span><span class="sxs-lookup"><span data-stu-id="23ecd-107">You can follow the instructions to create either a Blazor Server app or a Blazor WebAssembly app hosted in ASP.NET Core.</span></span> <span data-ttu-id="23ecd-108">除了托管模型特定的逻辑外，这两个项目中的大多数代码都是相同的。</span><span class="sxs-lookup"><span data-stu-id="23ecd-108">Except for the hosting model-specific logic, most of the code in both projects is the same.</span></span>

## <a name="project-file"></a><span data-ttu-id="23ecd-109">项目文件</span><span class="sxs-lookup"><span data-stu-id="23ecd-109">Project file</span></span>

<span data-ttu-id="23ecd-110">Blazor 服务器应用是 .NET 项目。</span><span class="sxs-lookup"><span data-stu-id="23ecd-110">Blazor Server apps are .NET projects.</span></span> <span data-ttu-id="23ecd-111">服务器应用程序的项目文件与 Blazor 它一样简单：</span><span class="sxs-lookup"><span data-stu-id="23ecd-111">The project file for the Blazor Server app is about as simple as it can get:</span></span>

```xml
<Project Sdk="Microsoft.NET.Sdk.Web">

  <PropertyGroup>
    <TargetFramework>net5.0</TargetFramework>
  </PropertyGroup>

</Project>
```

<span data-ttu-id="23ecd-112">应用的项目文件 Blazor WebAssembly 看起来稍微多一些， (完全版本号可能因) 而异：</span><span class="sxs-lookup"><span data-stu-id="23ecd-112">The project file for a Blazor WebAssembly app looks slightly more involved (exact version numbers may vary):</span></span>

```xml
<Project Sdk="Microsoft.NET.Sdk.BlazorWebAssembly">

  <PropertyGroup>
    <TargetFramework>net5.0</TargetFramework>
  </PropertyGroup>

  <ItemGroup>
    <PackageReference Include="Microsoft.AspNetCore.Components.WebAssembly" Version="5.0.0" />
    <PackageReference Include="Microsoft.AspNetCore.Components.WebAssembly.DevServer" Version="5.0.0" PrivateAssets="all" />
    <PackageReference Include="System.Net.Http.Json" Version="5.0.0" />
  </ItemGroup>

</Project>
```

<span data-ttu-id="23ecd-113">BlazorWebAssembly项目目标 `Microsoft.NET.Sdk.BlazorWebAssembly` 而不是 `Microsoft.NET.Sdk.Web` sdk，因为它们在 WebAssembly 基于的 .net 运行时上的浏览器中运行。</span><span class="sxs-lookup"><span data-stu-id="23ecd-113">Blazor WebAssembly project targets `Microsoft.NET.Sdk.BlazorWebAssembly` instead of `Microsoft.NET.Sdk.Web` sdk because they run in the browser on a WebAssembly-based .NET runtime.</span></span> <span data-ttu-id="23ecd-114">不能像在服务器或开发人员计算机上那样将 .NET 安装到 web 浏览器中。</span><span class="sxs-lookup"><span data-stu-id="23ecd-114">You can't install .NET into a web browser like you can on a server or developer machine.</span></span> <span data-ttu-id="23ecd-115">因此，项目 Blazor 使用单独的包引用来引用框架。</span><span class="sxs-lookup"><span data-stu-id="23ecd-115">Consequently, the project references the Blazor framework using individual package references.</span></span>

<span data-ttu-id="23ecd-116">相比之下，默认的 ASP.NET Web 窗体项目在其 *.csproj* 文件中包含将近300行的 XML，其中的大多数行都显式列出了项目中的各种代码和内容文件。</span><span class="sxs-lookup"><span data-stu-id="23ecd-116">By comparison, a default ASP.NET Web Forms project includes almost 300 lines of XML in its *.csproj* file, most of which is explicitly listing the various code and content files in the project.</span></span> <span data-ttu-id="23ecd-117">随着 `.NET 5` `Blazor Server` 和应用程序的发布， `Blazor WebAssembly` 可以轻松共享一个统一的运行时。</span><span class="sxs-lookup"><span data-stu-id="23ecd-117">With the release of `.NET 5` both `Blazor Server` and `Blazor WebAssembly` app can easily share one unified runtime.</span></span>

<span data-ttu-id="23ecd-118">尽管它们是受支持的，但在 .NET 项目中各个程序集引用不太常见。</span><span class="sxs-lookup"><span data-stu-id="23ecd-118">Although they're supported, individual assembly references are less common in .NET projects.</span></span> <span data-ttu-id="23ecd-119">大多数项目依赖项都作为 NuGet 包引用处理。</span><span class="sxs-lookup"><span data-stu-id="23ecd-119">Most project dependencies are handled as NuGet package references.</span></span> <span data-ttu-id="23ecd-120">只需引用 .NET 项目中的顶级包依赖项。</span><span class="sxs-lookup"><span data-stu-id="23ecd-120">You only need to reference top-level package dependencies in .NET projects.</span></span> <span data-ttu-id="23ecd-121">自动包含可传递的依赖项。</span><span class="sxs-lookup"><span data-stu-id="23ecd-121">Transitive dependencies are included automatically.</span></span> <span data-ttu-id="23ecd-122">包引用使用元素添加到项目文件，而不是使用 ASP.NET Web 窗体项目中常见的 *packages.config* 文件来引用包 `<PackageReference>` 。</span><span class="sxs-lookup"><span data-stu-id="23ecd-122">Instead of using the *packages.config* file commonly found in ASP.NET Web Forms projects to reference packages, package references are added to the project file using the `<PackageReference>` element.</span></span>

```xml
<ItemGroup>
  <PackageReference Include="Newtonsoft.Json" Version="12.0.2" />
</ItemGroup>
```

## <a name="entry-point"></a><span data-ttu-id="23ecd-123">入口点</span><span class="sxs-lookup"><span data-stu-id="23ecd-123">Entry point</span></span>

<span data-ttu-id="23ecd-124">Blazor服务器应用的入口点是在 *Program.cs* 文件中定义的，如控制台应用中所示。</span><span class="sxs-lookup"><span data-stu-id="23ecd-124">The Blazor Server app's entry point is defined in the *Program.cs* file, as you would see in a Console app.</span></span> <span data-ttu-id="23ecd-125">当应用程序执行时，它将使用特定于 web 应用的默认值创建并运行 web 主机实例。</span><span class="sxs-lookup"><span data-stu-id="23ecd-125">When the app executes, it creates and runs a web host instance using defaults specific to web apps.</span></span> <span data-ttu-id="23ecd-126">Web 主机管理 Blazor 服务器应用程序的生命周期，并设置主机级服务。</span><span class="sxs-lookup"><span data-stu-id="23ecd-126">The web host manages the Blazor Server app's lifecycle and sets up host-level services.</span></span> <span data-ttu-id="23ecd-127">此类服务的示例包括配置、日志记录、依赖关系注入和 HTTP 服务器。</span><span class="sxs-lookup"><span data-stu-id="23ecd-127">Examples of such services are configuration, logging, dependency injection, and the HTTP server.</span></span> <span data-ttu-id="23ecd-128">此代码主要是样板化的，通常保持不变。</span><span class="sxs-lookup"><span data-stu-id="23ecd-128">This code is mostly boilerplate and is often left unchanged.</span></span>

```csharp
public class Program
{
    public static void Main(string[] args)
    {
        CreateHostBuilder(args).Build().Run();
    }

    public static IHostBuilder CreateHostBuilder(string[] args) =>
        Host.CreateDefaultBuilder(args)
            .ConfigureWebHostDefaults(webBuilder =>
            {
                webBuilder.UseStartup<Startup>();
            });
}
```

<span data-ttu-id="23ecd-129">BlazorWebAssembly应用还会在 *Program.cs* 中定义入口点。</span><span class="sxs-lookup"><span data-stu-id="23ecd-129">Blazor WebAssembly apps also define an entry point in *Program.cs*.</span></span> <span data-ttu-id="23ecd-130">代码看起来略有不同。</span><span class="sxs-lookup"><span data-stu-id="23ecd-130">The code looks slightly different.</span></span> <span data-ttu-id="23ecd-131">此代码类似于设置应用程序主机以向应用程序提供相同的主机级服务。</span><span class="sxs-lookup"><span data-stu-id="23ecd-131">The code is similar in that it's setting up the app host to provide the same host-level services to the app.</span></span> <span data-ttu-id="23ecd-132">WebAssembly不过，应用主机不会设置 HTTP 服务器，因为它是直接在浏览器中执行的。</span><span class="sxs-lookup"><span data-stu-id="23ecd-132">The WebAssembly app host doesn't, however, set up an HTTP server because it executes directly in the browser.</span></span>

<span data-ttu-id="23ecd-133">Blazor 应用有一个 `Startup` 类，而不是一个 *global.asax* 文件，用于定义应用的启动逻辑。</span><span class="sxs-lookup"><span data-stu-id="23ecd-133">Blazor apps have a `Startup` class instead of a *Global.asax* file to define the startup logic for the app.</span></span> <span data-ttu-id="23ecd-134">`Startup`类用于配置应用程序和任何特定于应用程序的服务。</span><span class="sxs-lookup"><span data-stu-id="23ecd-134">The `Startup` class is used to configure the app and any app-specific services.</span></span> <span data-ttu-id="23ecd-135">在 Blazor 服务器应用中， `Startup` 类用于为 Blazor 客户端浏览器和服务器之间使用的实时连接设置终结点。</span><span class="sxs-lookup"><span data-stu-id="23ecd-135">In the Blazor Server app, the `Startup` class is used to set up the endpoint for the real-time connection used by Blazor between the client browsers and the server.</span></span> <span data-ttu-id="23ecd-136">在 Blazor WebAssembly 应用程序中， `Startup` 类定义应用程序的根组件及其呈现位置。</span><span class="sxs-lookup"><span data-stu-id="23ecd-136">In the Blazor WebAssembly app, the `Startup` class defines the root components for the app and where they should be rendered.</span></span> <span data-ttu-id="23ecd-137">我们将深入了解 `Startup` [应用程序启动](./app-startup.md) 部分中的类。</span><span class="sxs-lookup"><span data-stu-id="23ecd-137">We'll take a deeper look at the `Startup` class in the [App startup](./app-startup.md) section.</span></span>

## <a name="static-files"></a><span data-ttu-id="23ecd-138">静态文件</span><span class="sxs-lookup"><span data-stu-id="23ecd-138">Static files</span></span>

<span data-ttu-id="23ecd-139">与 ASP.NET Web 窗体项目不同，项目中的所有文件都不能 Blazor 被请求为静态文件。</span><span class="sxs-lookup"><span data-stu-id="23ecd-139">Unlike ASP.NET Web Forms projects, not all files in a Blazor project can be requested as static files.</span></span> <span data-ttu-id="23ecd-140">只有 *wwwroot* 文件夹中的文件可通过 web 寻址。</span><span class="sxs-lookup"><span data-stu-id="23ecd-140">Only the files in the *wwwroot* folder are web-addressable.</span></span> <span data-ttu-id="23ecd-141">此文件夹被称为应用程序的 "web 根目录"。</span><span class="sxs-lookup"><span data-stu-id="23ecd-141">This folder is referred to the app's "web root".</span></span> <span data-ttu-id="23ecd-142">应用程序的 web 根目录之外的任何内容都 *无法* 进行 web 寻址。</span><span class="sxs-lookup"><span data-stu-id="23ecd-142">Anything outside of the app's web root *isn't* web-addressable.</span></span> <span data-ttu-id="23ecd-143">此设置提供了额外的安全级别，可防止在 web 上意外公开项目文件。</span><span class="sxs-lookup"><span data-stu-id="23ecd-143">This setup provides an additional level of security that prevents accidental exposing of project files over the web.</span></span>

## <a name="configuration"></a><span data-ttu-id="23ecd-144">Configuration</span><span class="sxs-lookup"><span data-stu-id="23ecd-144">Configuration</span></span>

<span data-ttu-id="23ecd-145">ASP.NET Web 窗体应用中的配置通常使用一个或多个 *web.config* 文件进行处理。</span><span class="sxs-lookup"><span data-stu-id="23ecd-145">Configuration in ASP.NET Web Forms apps is typically handled using one or more *web.config* files.</span></span> <span data-ttu-id="23ecd-146">Blazor 应用通常不会有 *web.config* 的文件。</span><span class="sxs-lookup"><span data-stu-id="23ecd-146">Blazor apps don't typically have *web.config* files.</span></span> <span data-ttu-id="23ecd-147">如果是这样，则在 IIS 上承载时，该文件仅用于配置 IIS 特定的设置。</span><span class="sxs-lookup"><span data-stu-id="23ecd-147">If they do, the file is only used to configure IIS-specific settings when hosted on IIS.</span></span> <span data-ttu-id="23ecd-148">相反， Blazor 服务器应用使用 ASP.NET Core 配置抽象 (Blazor WebAssembly 应用当前不支持相同的配置抽象，但这可能是将来) 中添加的一项功能。</span><span class="sxs-lookup"><span data-stu-id="23ecd-148">Instead, Blazor Server apps use the ASP.NET Core configuration abstractions (Blazor WebAssembly apps don't currently support the same configuration abstractions, but that may be a feature added in the future).</span></span> <span data-ttu-id="23ecd-149">例如，默认的 Blazor 服务器应用程序将 *appsettings.js上* 的设置。</span><span class="sxs-lookup"><span data-stu-id="23ecd-149">For example, the default Blazor Server app stores some settings in *appsettings.json*.</span></span>

```json
{
  "Logging": {
    "LogLevel": {
      "Default": "Information",
      "Microsoft": "Warning",
      "Microsoft.Hosting.Lifetime": "Information"
    }
  },
  "AllowedHosts": "*"
}
```

<span data-ttu-id="23ecd-150">有关配置的详细信息，请参阅 [配置](./config.md) 节 ASP.NET Core 项目。</span><span class="sxs-lookup"><span data-stu-id="23ecd-150">We'll learn more about configuration in ASP.NET Core projects in the [Configuration](./config.md) section.</span></span>

## <a name="razor-components"></a><span data-ttu-id="23ecd-151">Razor 组件</span><span class="sxs-lookup"><span data-stu-id="23ecd-151">Razor components</span></span>

<span data-ttu-id="23ecd-152">项目中的大多数文件 Blazor 都是 *razor* 文件。</span><span class="sxs-lookup"><span data-stu-id="23ecd-152">Most files in Blazor projects are *.razor* files.</span></span> <span data-ttu-id="23ecd-153">Razor 是一种基于 HTML 和 c # 的模板化语言，用于动态生成 web UI。</span><span class="sxs-lookup"><span data-stu-id="23ecd-153">Razor is a templating language based on HTML and C# that is used to dynamically generate web UI.</span></span> <span data-ttu-id="23ecd-154">*Razor* 文件定义构成应用程序的 UI 的组件。</span><span class="sxs-lookup"><span data-stu-id="23ecd-154">The *.razor* files define components that make up the UI of the app.</span></span> <span data-ttu-id="23ecd-155">大多数情况下，对于服务器和应用而言，组件是相同的 Blazor Blazor WebAssembly 。</span><span class="sxs-lookup"><span data-stu-id="23ecd-155">For the most part, the components are identical for both the Blazor Server and Blazor WebAssembly apps.</span></span> <span data-ttu-id="23ecd-156">中的组件 Blazor 类似于 ASP.NET Web 窗体中的用户控件。</span><span class="sxs-lookup"><span data-stu-id="23ecd-156">Components in Blazor are analogous to user controls in ASP.NET Web Forms.</span></span>

<span data-ttu-id="23ecd-157">生成项目时，每个 Razor 组件文件都将编译为 .NET 类。</span><span class="sxs-lookup"><span data-stu-id="23ecd-157">Each Razor component file is compiled into a .NET class when the project is built.</span></span> <span data-ttu-id="23ecd-158">生成的类捕获组件的状态、呈现逻辑、生命周期方法、事件处理程序和其他逻辑。</span><span class="sxs-lookup"><span data-stu-id="23ecd-158">The generated class captures the component's state, rendering logic, lifecycle methods, event handlers, and other logic.</span></span> <span data-ttu-id="23ecd-159">我们将在[构建可重复使用的 UI 组件 Blazor ](./components.md)部分介绍组件。</span><span class="sxs-lookup"><span data-stu-id="23ecd-159">We'll look at authoring components in the [Building reusable UI components with Blazor](./components.md) section.</span></span>

<span data-ttu-id="23ecd-160">*_Imports* 文件不是 razor 组件文件。</span><span class="sxs-lookup"><span data-stu-id="23ecd-160">The *_Imports.razor* files aren't Razor component files.</span></span> <span data-ttu-id="23ecd-161">相反，它们定义一组 Razor 指令以导入到同一文件夹及其子文件夹中的其他 *razor* 文件中。</span><span class="sxs-lookup"><span data-stu-id="23ecd-161">Instead, they define a set of Razor directives to import into other *.razor* files within the same folder and in its subfolders.</span></span> <span data-ttu-id="23ecd-162">例如， *_Imports razor* 文件是一种为 `using` 常用命名空间添加指令的常规方法：</span><span class="sxs-lookup"><span data-stu-id="23ecd-162">For example, a *_Imports.razor* file is a conventional way to add `using` directives for commonly used namespaces:</span></span>

```razor
@using System.Net.Http
@using Microsoft.AspNetCore.Authorization
@using Microsoft.AspNetCore.Components.Authorization
@using Microsoft.AspNetCore.Components.Forms
@using Microsoft.AspNetCore.Components.Routing
@using Microsoft.AspNetCore.Components.Web
@using Microsoft.JSInterop
@using BlazorApp1
@using BlazorApp1.Shared
```

## <a name="pages"></a><span data-ttu-id="23ecd-163">Pages</span><span class="sxs-lookup"><span data-stu-id="23ecd-163">Pages</span></span>

<span data-ttu-id="23ecd-164">应用中的页面位于何处 Blazor ？</span><span class="sxs-lookup"><span data-stu-id="23ecd-164">Where are the pages in the Blazor apps?</span></span> <span data-ttu-id="23ecd-165">Blazor 不为可寻址页面定义单独的文件扩展名，例如 ASP.NET Web Forms apps 中的 *.aspx* 文件。</span><span class="sxs-lookup"><span data-stu-id="23ecd-165">Blazor doesn't define a separate file extension for addressable pages, like the *.aspx* files in ASP.NET Web Forms apps.</span></span> <span data-ttu-id="23ecd-166">而是通过将路由分配给组件来定义页面。</span><span class="sxs-lookup"><span data-stu-id="23ecd-166">Instead, pages are defined by assigning routes to components.</span></span> <span data-ttu-id="23ecd-167">通常使用 `@page` Razor 指令分配路由。</span><span class="sxs-lookup"><span data-stu-id="23ecd-167">A route is typically assigned using the `@page` Razor directive.</span></span> <span data-ttu-id="23ecd-168">例如， `Counter` 在 *Pages/Counter* 文件中编写的组件定义了以下路由：</span><span class="sxs-lookup"><span data-stu-id="23ecd-168">For example, the `Counter` component authored in the *Pages/Counter.razor* file defines the following route:</span></span>

```razor
@page "/counter"
```

<span data-ttu-id="23ecd-169">中的路由 Blazor 处理客户端，而不是服务器上的。</span><span class="sxs-lookup"><span data-stu-id="23ecd-169">Routing in Blazor is handled client-side, not on the server.</span></span> <span data-ttu-id="23ecd-170">当用户在浏览器中导航时，会 Blazor 截获导航，然后用匹配的路由呈现组件。</span><span class="sxs-lookup"><span data-stu-id="23ecd-170">As the user navigates in the browser, Blazor intercepts the navigation and then renders the component with the matching route.</span></span>

<span data-ttu-id="23ecd-171">组件的文件位置目前不会推理组件路由，就像 *.aspx* 页面一样。</span><span class="sxs-lookup"><span data-stu-id="23ecd-171">The component routes aren't currently inferred by the component's file location like they are with *.aspx* pages.</span></span> <span data-ttu-id="23ecd-172">将来可能会添加此功能。</span><span class="sxs-lookup"><span data-stu-id="23ecd-172">This feature may be added in the future.</span></span> <span data-ttu-id="23ecd-173">必须在组件上显式指定每个路由。</span><span class="sxs-lookup"><span data-stu-id="23ecd-173">Each route must be specified explicitly on the component.</span></span> <span data-ttu-id="23ecd-174">在 " *页面* " 文件夹中存储可路由的组件无特殊含义，只是一种约定。</span><span class="sxs-lookup"><span data-stu-id="23ecd-174">Storing routable components in a *Pages* folder has no special meaning and is purely a convention.</span></span>

<span data-ttu-id="23ecd-175">在 Blazor " [页面"、"路由" 和 "布局](./pages-routing-layouts.md) " 部分的 "路由" 部分中，我们将更详细地介绍。</span><span class="sxs-lookup"><span data-stu-id="23ecd-175">We'll look in greater detail at routing in Blazor in the [Pages, routing, and layouts](./pages-routing-layouts.md) section.</span></span>

## <a name="layout"></a><span data-ttu-id="23ecd-176">布局</span><span class="sxs-lookup"><span data-stu-id="23ecd-176">Layout</span></span>

<span data-ttu-id="23ecd-177">在 ASP.NET Web 窗体应用程序中，使用 *母版页 ()* 来处理常见的页面布局。</span><span class="sxs-lookup"><span data-stu-id="23ecd-177">In ASP.NET Web Forms apps, a common page layout is handled using master pages (*Site.Master*).</span></span> <span data-ttu-id="23ecd-178">在 Blazor 应用程序中，将使用布局组件 (*Shared/MainLayout*) 来处理页面布局。</span><span class="sxs-lookup"><span data-stu-id="23ecd-178">In Blazor apps, the page layout is handled using layout components (*Shared/MainLayout.razor*).</span></span> <span data-ttu-id="23ecd-179">" [页面"、"路由" 和 "布局"](./pages-routing-layouts.md) 部分中将更详细地讨论布局组件。</span><span class="sxs-lookup"><span data-stu-id="23ecd-179">Layout components will be discussed in more detail in [Page, routing, and layouts](./pages-routing-layouts.md) section.</span></span>

## <a name="bootstrap-no-locblazor"></a><span data-ttu-id="23ecd-180">引导 Blazor</span><span class="sxs-lookup"><span data-stu-id="23ecd-180">Bootstrap Blazor</span></span>

<span data-ttu-id="23ecd-181">若要启动 Blazor ，应用必须：</span><span class="sxs-lookup"><span data-stu-id="23ecd-181">To bootstrap Blazor, the app must:</span></span>

- <span data-ttu-id="23ecd-182">指定在页面上的什么位置 (应呈现的 *app.config*) 。</span><span class="sxs-lookup"><span data-stu-id="23ecd-182">Specify where on the page the root component (*App.Razor*) should be rendered.</span></span>
- <span data-ttu-id="23ecd-183">添加相应的 Blazor 框架脚本。</span><span class="sxs-lookup"><span data-stu-id="23ecd-183">Add the corresponding Blazor framework script.</span></span>

<span data-ttu-id="23ecd-184">在 Blazor 服务器应用中，根组件的 "主机" 页在 *_Host.* # 文件中定义。</span><span class="sxs-lookup"><span data-stu-id="23ecd-184">In the Blazor Server app, the root component's host page is defined in the *_Host.cshtml* file.</span></span> <span data-ttu-id="23ecd-185">此文件定义了一个 Razor 页面，而不是一个组件。</span><span class="sxs-lookup"><span data-stu-id="23ecd-185">This file defines a Razor Page, not a component.</span></span> <span data-ttu-id="23ecd-186">Razor Pages 使用 Razor 语法来定义服务器可寻址页面，与 *.aspx* 页面非常类似。</span><span class="sxs-lookup"><span data-stu-id="23ecd-186">Razor Pages use Razor syntax to define a server-addressable page, very much like an *.aspx* page.</span></span> <span data-ttu-id="23ecd-187">`Html.RenderComponentAsync<TComponent>(RenderMode)`方法用于定义根级别组件的呈现位置。</span><span class="sxs-lookup"><span data-stu-id="23ecd-187">The `Html.RenderComponentAsync<TComponent>(RenderMode)` method is used to define where a root-level component should be rendered.</span></span> <span data-ttu-id="23ecd-188">`RenderMode`选项指示组件的呈现方式。</span><span class="sxs-lookup"><span data-stu-id="23ecd-188">The `RenderMode` option indicates the manner in which the component should be rendered.</span></span> <span data-ttu-id="23ecd-189">下表概述了支持的 `RenderMode` 选项。</span><span class="sxs-lookup"><span data-stu-id="23ecd-189">The following table outlines the supported `RenderMode` options.</span></span>

|<span data-ttu-id="23ecd-190">选项</span><span class="sxs-lookup"><span data-stu-id="23ecd-190">Option</span></span>                        |<span data-ttu-id="23ecd-191">说明</span><span class="sxs-lookup"><span data-stu-id="23ecd-191">Description</span></span>       |
|------------------------------|------------------|
|`RenderMode.Server`           |<span data-ttu-id="23ecd-192">建立与浏览器的连接后交互呈现</span><span class="sxs-lookup"><span data-stu-id="23ecd-192">Rendered interactively once a connection with the browser is established</span></span>|
|`RenderMode.ServerPrerendered`|<span data-ttu-id="23ecd-193">首先预呈现并以交互方式呈现</span><span class="sxs-lookup"><span data-stu-id="23ecd-193">First prerendered and then rendered interactively</span></span>|
|`RenderMode.Static`           |<span data-ttu-id="23ecd-194">呈现为静态内容</span><span class="sxs-lookup"><span data-stu-id="23ecd-194">Rendered as static content</span></span>|

<span data-ttu-id="23ecd-195">*_Framework/blazor.server.js* 的脚本引用与服务器建立实时连接，并处理所有用户交互和 UI 更新。</span><span class="sxs-lookup"><span data-stu-id="23ecd-195">The script reference to *_framework/blazor.server.js* establishes the real-time connection with the server and then deals with all user interactions and UI updates.</span></span>

```razor
@page "/"
@namespace BlazorApp1.Pages
@addTagHelper *, Microsoft.AspNetCore.Mvc.TagHelpers

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="utf-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>BlazorApp1</title>
    <base href="~/" />
    <link rel="stylesheet" href="css/bootstrap/bootstrap.min.css" />
    <link href="css/site.css" rel="stylesheet" />
</head>
<body>
    <app>
        @(await Html.RenderComponentAsync<App>(RenderMode.ServerPrerendered))
    </app>

    <script src="_framework/blazor.server.js"></script>
</body>
</html>
```

<span data-ttu-id="23ecd-196">在 Blazor WebAssembly 应用程序中，"主机" 页是 *wwwroot/index.html* 下的简单静态 HTML 文件。</span><span class="sxs-lookup"><span data-stu-id="23ecd-196">In the Blazor WebAssembly app, the host page is a simple static HTML file under *wwwroot/index.html*.</span></span> <span data-ttu-id="23ecd-197">`<div>`Id 为的元素 `app` 用于指示应呈现根组件的位置。</span><span class="sxs-lookup"><span data-stu-id="23ecd-197">The `<div>` element with id named `app` is used to indicate where the root component should be rendered.</span></span>

```html
<!DOCTYPE html>
<html>

<head>
    <meta charset="utf-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no" />
    <title>BlazorApp2</title>
    <base href="/" />
    <link href="css/bootstrap/bootstrap.min.css" rel="stylesheet" />
    <link href="css/app.css" rel="stylesheet" />
    <link href="blazor-web.styles.css" rel="stylesheet" />
</head>

<body>
    <div id="app">Loading...</div>

    <div id="blazor-error-ui">
        An unhandled error has occurred.
        <a href="" class="reload">Reload</a>
        <a class="dismiss">🗙</a>
    </div>
    <script src="_framework/blazor.webassembly.js"></script>
</body>

</html>

```

<span data-ttu-id="23ecd-198">在应用程序的方法中指定要呈现的根组件， `Program.Main` 以便通过依赖关系注入注册服务。</span><span class="sxs-lookup"><span data-stu-id="23ecd-198">The root component to render is specified in the app's `Program.Main` method with the flexibility to register services through dependency injection.</span></span> <span data-ttu-id="23ecd-199">有关详细信息，请参阅 [ASP.NET Core Blazor 依赖关系注入](/aspnet/core/blazor/fundamentals/dependency-injection?pivots=webassembly)。</span><span class="sxs-lookup"><span data-stu-id="23ecd-199">For more information, see [ASP.NET Core Blazor dependency injection](/aspnet/core/blazor/fundamentals/dependency-injection?pivots=webassembly).</span></span>

```csharp
public class Program
{
    public static async Task Main(string[] args)
    {
        var builder = WebAssemblyHostBuilder.CreateDefault(args);
        builder.RootComponents.Add<App>("#app");

        ....
        ....
    }
}
```

## <a name="build-output"></a><span data-ttu-id="23ecd-200">生成输出</span><span class="sxs-lookup"><span data-stu-id="23ecd-200">Build output</span></span>

<span data-ttu-id="23ecd-201">Blazor生成项目时，所有 Razor 组件和代码文件都将编译为一个程序集。</span><span class="sxs-lookup"><span data-stu-id="23ecd-201">When a Blazor project is built, all Razor component and code files are compiled into a single assembly.</span></span> <span data-ttu-id="23ecd-202">不同于 ASP.NET Web 窗体项目， Blazor 不支持 UI 逻辑的运行时编译。</span><span class="sxs-lookup"><span data-stu-id="23ecd-202">Unlike ASP.NET Web Forms projects, Blazor doesn't support runtime compilation of the UI logic.</span></span>

## <a name="run-the-app"></a><span data-ttu-id="23ecd-203">运行应用</span><span class="sxs-lookup"><span data-stu-id="23ecd-203">Run the app</span></span>

<span data-ttu-id="23ecd-204">若要运行 Blazor 服务器应用，请 `F5` 在 Visual Studio 中按。</span><span class="sxs-lookup"><span data-stu-id="23ecd-204">To run the Blazor Server app, press `F5` in Visual Studio.</span></span> <span data-ttu-id="23ecd-205">Blazor 应用不支持运行时编译。</span><span class="sxs-lookup"><span data-stu-id="23ecd-205">Blazor apps don't support runtime compilation.</span></span> <span data-ttu-id="23ecd-206">若要查看代码和组件标记更改的结果，请在附加调试器的情况下重新生成并重新启动应用。</span><span class="sxs-lookup"><span data-stu-id="23ecd-206">To see the results of code and component markup changes, rebuild and restart the app with the debugger attached.</span></span> <span data-ttu-id="23ecd-207">如果在没有调试器附加 () 的情况下运行 `Ctrl+F5` ，则 Visual Studio 会监视文件更改，并在进行更改后重新启动应用。</span><span class="sxs-lookup"><span data-stu-id="23ecd-207">If you run without the debugger attached (`Ctrl+F5`), Visual Studio watches for file changes and restarts the app as changes are made.</span></span> <span data-ttu-id="23ecd-208">进行更改后，手动刷新浏览器。</span><span class="sxs-lookup"><span data-stu-id="23ecd-208">You manually refresh the browser as changes are made.</span></span>

<span data-ttu-id="23ecd-209">若要运行 Blazor WebAssembly 应用，请选择以下方法之一：</span><span class="sxs-lookup"><span data-stu-id="23ecd-209">To run the Blazor WebAssembly app, choose one of the following approaches:</span></span>

- <span data-ttu-id="23ecd-210">使用开发服务器直接运行客户端项目。</span><span class="sxs-lookup"><span data-stu-id="23ecd-210">Run the client project directly using the development server.</span></span>
- <span data-ttu-id="23ecd-211">在将应用程序托管到 ASP.NET Core 时运行服务器项目。</span><span class="sxs-lookup"><span data-stu-id="23ecd-211">Run the server project when hosting the app with ASP.NET Core.</span></span>

<span data-ttu-id="23ecd-212">BlazorWebAssembly可在浏览器和 Visual Studio 中调试应用程序。有关详细信息，请参阅[调试 ASP.NET Core Blazor WebAssembly ](/aspnet/core/blazor/debug) 。</span><span class="sxs-lookup"><span data-stu-id="23ecd-212">Blazor WebAssembly apps can be debugged in both browser and Visual Studio.See [Debug ASP.NET Core Blazor WebAssembly](/aspnet/core/blazor/debug) for details.</span></span>

>[!div class="step-by-step"]
><span data-ttu-id="23ecd-213">[上一页](hosting-models.md)
>[下一页](app-startup.md)</span><span class="sxs-lookup"><span data-stu-id="23ecd-213">[Previous](hosting-models.md)
[Next](app-startup.md)</span></span>
