---
title: dotnet new 命令
description: dotnet new 命令可根据指定模板新建 .NET 项目。
no-loc:
- Blazor
- WebAssembly
ms.date: 09/04/2020
ms.openlocfilehash: acaaf025555c46f720452b8c9d4f875b8656125a
ms.sourcegitcommit: b924ade6426cf61a4604c4e2ee54cb3592c29317
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/18/2021
ms.locfileid: "101096813"
---
# <a name="dotnet-new"></a><span data-ttu-id="63312-103">dotnet new</span><span class="sxs-lookup"><span data-stu-id="63312-103">dotnet new</span></span>

<span data-ttu-id="63312-104">本文适用于： ✔️ .NET Core 2.0 SDK 及更高版本</span><span class="sxs-lookup"><span data-stu-id="63312-104">**This article applies to:** ✔️ .NET Core 2.0 SDK and later versions</span></span>

## <a name="name"></a><span data-ttu-id="63312-105">“属性”</span><span class="sxs-lookup"><span data-stu-id="63312-105">Name</span></span>

<span data-ttu-id="63312-106">`dotnet new` - 根据指定的模板，创建新的项目、配置文件或解决方案。</span><span class="sxs-lookup"><span data-stu-id="63312-106">`dotnet new` - Creates a new project, configuration file, or solution based on the specified template.</span></span>

## <a name="synopsis"></a><span data-ttu-id="63312-107">摘要</span><span class="sxs-lookup"><span data-stu-id="63312-107">Synopsis</span></span>

```dotnetcli
dotnet new <TEMPLATE> [--dry-run] [--force] [-i|--install {PATH|NUGET_ID}]
    [-lang|--language {"C#"|"F#"|VB}] [-n|--name <OUTPUT_NAME>]
    [--nuget-source <SOURCE>] [-o|--output <OUTPUT_DIRECTORY>]
    [-u|--uninstall] [--update-apply] [--update-check] [Template options]

dotnet new <TEMPLATE> [-l|--list] [--type <TYPE>]

dotnet new -h|--help
```

## <a name="description"></a><span data-ttu-id="63312-108">描述</span><span class="sxs-lookup"><span data-stu-id="63312-108">Description</span></span>

<span data-ttu-id="63312-109">`dotnet new` 命令基于模板创建 .NET 项目或其他项目。</span><span class="sxs-lookup"><span data-stu-id="63312-109">The `dotnet new` command creates a .NET project or other artifacts based on a template.</span></span>

<span data-ttu-id="63312-110">命令调用[模板引擎](https://github.com/dotnet/templating)，以根据指定的模板和选项在磁盘上创建项目。</span><span class="sxs-lookup"><span data-stu-id="63312-110">The command calls the [template engine](https://github.com/dotnet/templating) to create the artifacts on disk based on the specified template and options.</span></span>

### <a name="implicit-restore"></a><span data-ttu-id="63312-111">隐式还原</span><span class="sxs-lookup"><span data-stu-id="63312-111">Implicit restore</span></span>

[!INCLUDE[dotnet restore note](~/includes/dotnet-restore-note.md)]

## <a name="arguments"></a><span data-ttu-id="63312-112">自变量</span><span class="sxs-lookup"><span data-stu-id="63312-112">Arguments</span></span>

- **`TEMPLATE`**

  <span data-ttu-id="63312-113">调用命令时要实例化的模板。</span><span class="sxs-lookup"><span data-stu-id="63312-113">The template to instantiate when the command is invoked.</span></span> <span data-ttu-id="63312-114">每个模板可能具有可传递的特定选项。</span><span class="sxs-lookup"><span data-stu-id="63312-114">Each template might have specific options you can pass.</span></span> <span data-ttu-id="63312-115">有关详细信息，请参阅[模板选项](#template-options)。</span><span class="sxs-lookup"><span data-stu-id="63312-115">For more information, see [Template options](#template-options).</span></span>

  <span data-ttu-id="63312-116">可以运行 `dotnet new --list` 或 `dotnet new -l` 以查看所有已安装模板的列表。</span><span class="sxs-lookup"><span data-stu-id="63312-116">You can run `dotnet new --list` or `dotnet new -l` to see a list of all installed templates.</span></span> <span data-ttu-id="63312-117">如果 `TEMPLATE` 值与返回表中的“模板”或“短名称”列中的文本不完全匹配，则会对这两列执行 substring 匹配。</span><span class="sxs-lookup"><span data-stu-id="63312-117">If the `TEMPLATE` value isn't an exact match on text in the **Templates** or **Short Name** column from the returned table, a substring match is performed on those two columns.</span></span>

  <span data-ttu-id="63312-118">从 .NET Core 3.0 SDK 开始，当你在以下情况下调用 `dotnet new` 命令时，CLI 将在 NuGet.org 中搜索模板：</span><span class="sxs-lookup"><span data-stu-id="63312-118">Starting with .NET Core 3.0 SDK, the CLI searches for templates in NuGet.org when you invoke the `dotnet new` command in the following conditions:</span></span>

  - <span data-ttu-id="63312-119">如果在调用 `dotnet new` 时 CLI 找不到模板匹配项，即使是部分匹配也不行。</span><span class="sxs-lookup"><span data-stu-id="63312-119">If the CLI can't find a template match when invoking `dotnet new`, not even partial.</span></span>
  - <span data-ttu-id="63312-120">如果有较新版本的模板可用。</span><span class="sxs-lookup"><span data-stu-id="63312-120">If there's a newer version of the template available.</span></span> <span data-ttu-id="63312-121">在这种情况下，将创建项目或工件，但 CLI 会就模板的更新版本发出警告。</span><span class="sxs-lookup"><span data-stu-id="63312-121">In this case, the project or artifact is created but the CLI warns you about an updated version of the template.</span></span>

  <span data-ttu-id="63312-122">下表显示随 .NET SDK 一起预安装的模板。</span><span class="sxs-lookup"><span data-stu-id="63312-122">The following table shows the templates that come pre-installed with the .NET SDK.</span></span> <span data-ttu-id="63312-123">模板的默认语言显示在括号内。</span><span class="sxs-lookup"><span data-stu-id="63312-123">The default language for the template is shown inside the brackets.</span></span> <span data-ttu-id="63312-124">单击短名称链接可查看特定的模板选项。</span><span class="sxs-lookup"><span data-stu-id="63312-124">Click on the short name link to see the specific template options.</span></span>

| <span data-ttu-id="63312-125">模板</span><span class="sxs-lookup"><span data-stu-id="63312-125">Templates</span></span>                                    | <span data-ttu-id="63312-126">短名称</span><span class="sxs-lookup"><span data-stu-id="63312-126">Short name</span></span>                        | <span data-ttu-id="63312-127">语言</span><span class="sxs-lookup"><span data-stu-id="63312-127">Language</span></span>     | <span data-ttu-id="63312-128">Tags</span><span class="sxs-lookup"><span data-stu-id="63312-128">Tags</span></span>                                  | <span data-ttu-id="63312-129">已引入</span><span class="sxs-lookup"><span data-stu-id="63312-129">Introduced</span></span> |
|----------------------------------------------|-----------------------------------|--------------|---------------------------------------|------------|
| <span data-ttu-id="63312-130">控制台应用程序</span><span class="sxs-lookup"><span data-stu-id="63312-130">Console Application</span></span>                          | [`console`](#console)             | <span data-ttu-id="63312-131">[C#]、F#、VB</span><span class="sxs-lookup"><span data-stu-id="63312-131">[C#], F#, VB</span></span> | <span data-ttu-id="63312-132">常用/控制台</span><span class="sxs-lookup"><span data-stu-id="63312-132">Common/Console</span></span>                        | <span data-ttu-id="63312-133">1.0</span><span class="sxs-lookup"><span data-stu-id="63312-133">1.0</span></span>        |
| <span data-ttu-id="63312-134">类库</span><span class="sxs-lookup"><span data-stu-id="63312-134">Class library</span></span>                                | [`classlib`](#classlib)           | <span data-ttu-id="63312-135">[C#]、F#、VB</span><span class="sxs-lookup"><span data-stu-id="63312-135">[C#], F#, VB</span></span> | <span data-ttu-id="63312-136">常用/库</span><span class="sxs-lookup"><span data-stu-id="63312-136">Common/Library</span></span>                        | <span data-ttu-id="63312-137">1.0</span><span class="sxs-lookup"><span data-stu-id="63312-137">1.0</span></span>        |
| <span data-ttu-id="63312-138">WPF 应用程序</span><span class="sxs-lookup"><span data-stu-id="63312-138">WPF Application</span></span>                              | [`wpf`](#wpf)                     | <span data-ttu-id="63312-139">[C#]、VB</span><span class="sxs-lookup"><span data-stu-id="63312-139">[C#], VB</span></span>     | <span data-ttu-id="63312-140">常用/WPF</span><span class="sxs-lookup"><span data-stu-id="63312-140">Common/WPF</span></span>                            | <span data-ttu-id="63312-141">3.0（对于 VB，则为 5.0）</span><span class="sxs-lookup"><span data-stu-id="63312-141">3.0 (5.0 for VB)</span></span>|
| <span data-ttu-id="63312-142">WPF 类库</span><span class="sxs-lookup"><span data-stu-id="63312-142">WPF Class library</span></span>                            | [`wpflib`](#wpf)                  | <span data-ttu-id="63312-143">[C#]、VB</span><span class="sxs-lookup"><span data-stu-id="63312-143">[C#], VB</span></span>     | <span data-ttu-id="63312-144">常用/WPF</span><span class="sxs-lookup"><span data-stu-id="63312-144">Common/WPF</span></span>                            | <span data-ttu-id="63312-145">3.0（对于 VB，则为 5.0）</span><span class="sxs-lookup"><span data-stu-id="63312-145">3.0 (5.0 for VB)</span></span>|
| <span data-ttu-id="63312-146">WPF 自定义控件库</span><span class="sxs-lookup"><span data-stu-id="63312-146">WPF Custom Control Library</span></span>                   | [`wpfcustomcontrollib`](#wpf)     | <span data-ttu-id="63312-147">[C#]、VB</span><span class="sxs-lookup"><span data-stu-id="63312-147">[C#], VB</span></span>     | <span data-ttu-id="63312-148">常用/WPF</span><span class="sxs-lookup"><span data-stu-id="63312-148">Common/WPF</span></span>                            | <span data-ttu-id="63312-149">3.0（对于 VB，则为 5.0）</span><span class="sxs-lookup"><span data-stu-id="63312-149">3.0 (5.0 for VB)</span></span>|
| <span data-ttu-id="63312-150">WPF 用户控件库</span><span class="sxs-lookup"><span data-stu-id="63312-150">WPF User Control Library</span></span>                     | [`wpfusercontrollib`](#wpf)       | <span data-ttu-id="63312-151">[C#]、VB</span><span class="sxs-lookup"><span data-stu-id="63312-151">[C#], VB</span></span>     | <span data-ttu-id="63312-152">常用/WPF</span><span class="sxs-lookup"><span data-stu-id="63312-152">Common/WPF</span></span>                            | <span data-ttu-id="63312-153">3.0（对于 VB，则为 5.0）</span><span class="sxs-lookup"><span data-stu-id="63312-153">3.0 (5.0 for VB)</span></span>|
| <span data-ttu-id="63312-154">Windows 窗体 (WinForms) 应用程序</span><span class="sxs-lookup"><span data-stu-id="63312-154">Windows Forms (WinForms) Application</span></span>         | [`winforms`](#winforms)           | <span data-ttu-id="63312-155">[C#]、VB</span><span class="sxs-lookup"><span data-stu-id="63312-155">[C#], VB</span></span>     | <span data-ttu-id="63312-156">常用/WinForms</span><span class="sxs-lookup"><span data-stu-id="63312-156">Common/WinForms</span></span>                       | <span data-ttu-id="63312-157">3.0（对于 VB，则为 5.0）</span><span class="sxs-lookup"><span data-stu-id="63312-157">3.0 (5.0 for VB)</span></span>|
| <span data-ttu-id="63312-158">Windows 窗体 (WinForms) 类库</span><span class="sxs-lookup"><span data-stu-id="63312-158">Windows Forms (WinForms) Class library</span></span>       | [`winformslib`](#winforms)        | <span data-ttu-id="63312-159">[C#]、VB</span><span class="sxs-lookup"><span data-stu-id="63312-159">[C#], VB</span></span>     | <span data-ttu-id="63312-160">常用/WinForms</span><span class="sxs-lookup"><span data-stu-id="63312-160">Common/WinForms</span></span>                       | <span data-ttu-id="63312-161">3.0（对于 VB，则为 5.0）</span><span class="sxs-lookup"><span data-stu-id="63312-161">3.0 (5.0 for VB)</span></span>|
| <span data-ttu-id="63312-162">Worker Service</span><span class="sxs-lookup"><span data-stu-id="63312-162">Worker Service</span></span>                               | [`worker`](#web-others)           | <span data-ttu-id="63312-163">[C#]</span><span class="sxs-lookup"><span data-stu-id="63312-163">[C#]</span></span>         | <span data-ttu-id="63312-164">常用/Worker/Web</span><span class="sxs-lookup"><span data-stu-id="63312-164">Common/Worker/Web</span></span>                     | <span data-ttu-id="63312-165">3.0</span><span class="sxs-lookup"><span data-stu-id="63312-165">3.0</span></span>        |
| <span data-ttu-id="63312-166">单元测试项目</span><span class="sxs-lookup"><span data-stu-id="63312-166">Unit Test Project</span></span>                            | [`mstest`](#test)                 | <span data-ttu-id="63312-167">[C#]、F#、VB</span><span class="sxs-lookup"><span data-stu-id="63312-167">[C#], F#, VB</span></span> | <span data-ttu-id="63312-168">测试/MSTest</span><span class="sxs-lookup"><span data-stu-id="63312-168">Test/MSTest</span></span>                           | <span data-ttu-id="63312-169">1.0</span><span class="sxs-lookup"><span data-stu-id="63312-169">1.0</span></span>        |
| <span data-ttu-id="63312-170">NUnit 3 测试项目</span><span class="sxs-lookup"><span data-stu-id="63312-170">NUnit 3 Test Project</span></span>                         | [`nunit`](#nunit)                 | <span data-ttu-id="63312-171">[C#]、F#、VB</span><span class="sxs-lookup"><span data-stu-id="63312-171">[C#], F#, VB</span></span> | <span data-ttu-id="63312-172">测试/NUnit</span><span class="sxs-lookup"><span data-stu-id="63312-172">Test/NUnit</span></span>                            | <span data-ttu-id="63312-173">2.1.400</span><span class="sxs-lookup"><span data-stu-id="63312-173">2.1.400</span></span>    |
| <span data-ttu-id="63312-174">NUnit 3 测试项</span><span class="sxs-lookup"><span data-stu-id="63312-174">NUnit 3 Test Item</span></span>                            | `nunit-test`                      | <span data-ttu-id="63312-175">[C#]、F#、VB</span><span class="sxs-lookup"><span data-stu-id="63312-175">[C#], F#, VB</span></span> | <span data-ttu-id="63312-176">测试/NUnit</span><span class="sxs-lookup"><span data-stu-id="63312-176">Test/NUnit</span></span>                            | <span data-ttu-id="63312-177">2.2</span><span class="sxs-lookup"><span data-stu-id="63312-177">2.2</span></span>        |
| <span data-ttu-id="63312-178">xUnit 测试项目</span><span class="sxs-lookup"><span data-stu-id="63312-178">xUnit Test Project</span></span>                           | [`xunit`](#test)                  | <span data-ttu-id="63312-179">[C#]、F#、VB</span><span class="sxs-lookup"><span data-stu-id="63312-179">[C#], F#, VB</span></span> | <span data-ttu-id="63312-180">测试/xUnit</span><span class="sxs-lookup"><span data-stu-id="63312-180">Test/xUnit</span></span>                            | <span data-ttu-id="63312-181">1.0</span><span class="sxs-lookup"><span data-stu-id="63312-181">1.0</span></span>        |
| <span data-ttu-id="63312-182">Razor 组件</span><span class="sxs-lookup"><span data-stu-id="63312-182">Razor Component</span></span>                              | `razorcomponent`                  | <span data-ttu-id="63312-183">[C#]</span><span class="sxs-lookup"><span data-stu-id="63312-183">[C#]</span></span>         | <span data-ttu-id="63312-184">Web/ASP.NET</span><span class="sxs-lookup"><span data-stu-id="63312-184">Web/ASP.NET</span></span>                           | <span data-ttu-id="63312-185">3.0</span><span class="sxs-lookup"><span data-stu-id="63312-185">3.0</span></span>        |
| <span data-ttu-id="63312-186">Razor 页</span><span class="sxs-lookup"><span data-stu-id="63312-186">Razor Page</span></span>                                   | [`page`](#page)                   | <span data-ttu-id="63312-187">[C#]</span><span class="sxs-lookup"><span data-stu-id="63312-187">[C#]</span></span>         | <span data-ttu-id="63312-188">Web/ASP.NET</span><span class="sxs-lookup"><span data-stu-id="63312-188">Web/ASP.NET</span></span>                           | <span data-ttu-id="63312-189">2.0</span><span class="sxs-lookup"><span data-stu-id="63312-189">2.0</span></span>        |
| <span data-ttu-id="63312-190">MVC ViewImports</span><span class="sxs-lookup"><span data-stu-id="63312-190">MVC ViewImports</span></span>                              | [`viewimports`](#namespace)       | <span data-ttu-id="63312-191">[C#]</span><span class="sxs-lookup"><span data-stu-id="63312-191">[C#]</span></span>         | <span data-ttu-id="63312-192">Web/ASP.NET</span><span class="sxs-lookup"><span data-stu-id="63312-192">Web/ASP.NET</span></span>                           | <span data-ttu-id="63312-193">2.0</span><span class="sxs-lookup"><span data-stu-id="63312-193">2.0</span></span>        |
| <span data-ttu-id="63312-194">MVC ViewStart</span><span class="sxs-lookup"><span data-stu-id="63312-194">MVC ViewStart</span></span>                                | `viewstart`                       | <span data-ttu-id="63312-195">[C#]</span><span class="sxs-lookup"><span data-stu-id="63312-195">[C#]</span></span>         | <span data-ttu-id="63312-196">Web/ASP.NET</span><span class="sxs-lookup"><span data-stu-id="63312-196">Web/ASP.NET</span></span>                           | <span data-ttu-id="63312-197">2.0</span><span class="sxs-lookup"><span data-stu-id="63312-197">2.0</span></span>        |
| <span data-ttu-id="63312-198">Blazor 服务器应用</span><span class="sxs-lookup"><span data-stu-id="63312-198">Blazor Server App</span></span>                            | [`blazorserver`](#blazorserver)   | <span data-ttu-id="63312-199">[C#]</span><span class="sxs-lookup"><span data-stu-id="63312-199">[C#]</span></span>         | <span data-ttu-id="63312-200">Web/Blazor</span><span class="sxs-lookup"><span data-stu-id="63312-200">Web/Blazor</span></span>                            | <span data-ttu-id="63312-201">3.0</span><span class="sxs-lookup"><span data-stu-id="63312-201">3.0</span></span>        |
| <span data-ttu-id="63312-202">Blazor WebAssembly 应用</span><span class="sxs-lookup"><span data-stu-id="63312-202">Blazor WebAssembly App</span></span>                       | [`blazorwasm`](#blazorwasm)       | <span data-ttu-id="63312-203">[C#]</span><span class="sxs-lookup"><span data-stu-id="63312-203">[C#]</span></span>         | <span data-ttu-id="63312-204">Web/Blazor/WebAssembly</span><span class="sxs-lookup"><span data-stu-id="63312-204">Web/Blazor/WebAssembly</span></span>                | <span data-ttu-id="63312-205">3.1.300</span><span class="sxs-lookup"><span data-stu-id="63312-205">3.1.300</span></span>    |
| <span data-ttu-id="63312-206">ASP.NET Core 空</span><span class="sxs-lookup"><span data-stu-id="63312-206">ASP.NET Core Empty</span></span>                           | [`web`](#web)                     | <span data-ttu-id="63312-207">[C#]，F#</span><span class="sxs-lookup"><span data-stu-id="63312-207">[C#], F#</span></span>     | <span data-ttu-id="63312-208">Web/空</span><span class="sxs-lookup"><span data-stu-id="63312-208">Web/Empty</span></span>                             | <span data-ttu-id="63312-209">1.0</span><span class="sxs-lookup"><span data-stu-id="63312-209">1.0</span></span>        |
| <span data-ttu-id="63312-210">ASP.NET Core Web 应用程序 (Model-View-Controller)</span><span class="sxs-lookup"><span data-stu-id="63312-210">ASP.NET Core Web App (Model-View-Controller)</span></span> | [`mvc`](#web-options)             | <span data-ttu-id="63312-211">[C#]，F#</span><span class="sxs-lookup"><span data-stu-id="63312-211">[C#], F#</span></span>     | <span data-ttu-id="63312-212">Web/MVC</span><span class="sxs-lookup"><span data-stu-id="63312-212">Web/MVC</span></span>                               | <span data-ttu-id="63312-213">1.0</span><span class="sxs-lookup"><span data-stu-id="63312-213">1.0</span></span>        |
| <span data-ttu-id="63312-214">ASP.NET Core Web 应用程序</span><span class="sxs-lookup"><span data-stu-id="63312-214">ASP.NET Core Web App</span></span>                         | [`webapp, razor`](#web-options)   | <span data-ttu-id="63312-215">[C#]</span><span class="sxs-lookup"><span data-stu-id="63312-215">[C#]</span></span>         | <span data-ttu-id="63312-216">Web/MVC/Razor Pages</span><span class="sxs-lookup"><span data-stu-id="63312-216">Web/MVC/Razor Pages</span></span>                   | <span data-ttu-id="63312-217">2.2、2.0</span><span class="sxs-lookup"><span data-stu-id="63312-217">2.2, 2.0</span></span>   |
| <span data-ttu-id="63312-218">含 Angular 的 ASP.NET Core</span><span class="sxs-lookup"><span data-stu-id="63312-218">ASP.NET Core with Angular</span></span>                    | [`angular`](#spa)                 | <span data-ttu-id="63312-219">[C#]</span><span class="sxs-lookup"><span data-stu-id="63312-219">[C#]</span></span>         | <span data-ttu-id="63312-220">Web/MVC/SPA</span><span class="sxs-lookup"><span data-stu-id="63312-220">Web/MVC/SPA</span></span>                           | <span data-ttu-id="63312-221">2.0</span><span class="sxs-lookup"><span data-stu-id="63312-221">2.0</span></span>        |
| <span data-ttu-id="63312-222">含 React.js 的 ASP.NET Core</span><span class="sxs-lookup"><span data-stu-id="63312-222">ASP.NET Core with React.js</span></span>                   | [`react`](#spa)                   | <span data-ttu-id="63312-223">[C#]</span><span class="sxs-lookup"><span data-stu-id="63312-223">[C#]</span></span>         | <span data-ttu-id="63312-224">Web/MVC/SPA</span><span class="sxs-lookup"><span data-stu-id="63312-224">Web/MVC/SPA</span></span>                           | <span data-ttu-id="63312-225">2.0</span><span class="sxs-lookup"><span data-stu-id="63312-225">2.0</span></span>        |
| <span data-ttu-id="63312-226">含 React.js 和 Redux 的 ASP.NET Core</span><span class="sxs-lookup"><span data-stu-id="63312-226">ASP.NET Core with React.js and Redux</span></span>         | [`reactredux`](#reactredux)       | <span data-ttu-id="63312-227">[C#]</span><span class="sxs-lookup"><span data-stu-id="63312-227">[C#]</span></span>         | <span data-ttu-id="63312-228">Web/MVC/SPA</span><span class="sxs-lookup"><span data-stu-id="63312-228">Web/MVC/SPA</span></span>                           | <span data-ttu-id="63312-229">2.0</span><span class="sxs-lookup"><span data-stu-id="63312-229">2.0</span></span>        |
| <span data-ttu-id="63312-230">Razor 类库</span><span class="sxs-lookup"><span data-stu-id="63312-230">Razor Class Library</span></span>                          | [`razorclasslib`](#razorclasslib) | <span data-ttu-id="63312-231">[C#]</span><span class="sxs-lookup"><span data-stu-id="63312-231">[C#]</span></span>         | <span data-ttu-id="63312-232">Web/Razor/库/Razor 类库</span><span class="sxs-lookup"><span data-stu-id="63312-232">Web/Razor/Library/Razor Class Library</span></span> | <span data-ttu-id="63312-233">2.1</span><span class="sxs-lookup"><span data-stu-id="63312-233">2.1</span></span>        |
| <span data-ttu-id="63312-234">ASP.NET Core Web API</span><span class="sxs-lookup"><span data-stu-id="63312-234">ASP.NET Core Web API</span></span>                         | [`webapi`](#webapi)               | <span data-ttu-id="63312-235">[C#]，F#</span><span class="sxs-lookup"><span data-stu-id="63312-235">[C#], F#</span></span>     | <span data-ttu-id="63312-236">Web/WebAPI</span><span class="sxs-lookup"><span data-stu-id="63312-236">Web/WebAPI</span></span>                            | <span data-ttu-id="63312-237">1.0</span><span class="sxs-lookup"><span data-stu-id="63312-237">1.0</span></span>        |
| <span data-ttu-id="63312-238">ASP.NET Core gRPC 服务</span><span class="sxs-lookup"><span data-stu-id="63312-238">ASP.NET Core gRPC Service</span></span>                    | [`grpc`](#web-others)             | <span data-ttu-id="63312-239">[C#]</span><span class="sxs-lookup"><span data-stu-id="63312-239">[C#]</span></span>         | <span data-ttu-id="63312-240">Web/gRPC</span><span class="sxs-lookup"><span data-stu-id="63312-240">Web/gRPC</span></span>                              | <span data-ttu-id="63312-241">3.0</span><span class="sxs-lookup"><span data-stu-id="63312-241">3.0</span></span>        |
| <span data-ttu-id="63312-242">dotnet gitignore 文件</span><span class="sxs-lookup"><span data-stu-id="63312-242">dotnet gitignore file</span></span>                        | `gitignore`                       |              | <span data-ttu-id="63312-243">配置</span><span class="sxs-lookup"><span data-stu-id="63312-243">Config</span></span>                                | <span data-ttu-id="63312-244">3.0</span><span class="sxs-lookup"><span data-stu-id="63312-244">3.0</span></span>        |
| <span data-ttu-id="63312-245">global.json 文件</span><span class="sxs-lookup"><span data-stu-id="63312-245">global.json file</span></span>                             | [`globaljson`](#globaljson)       |              | <span data-ttu-id="63312-246">配置</span><span class="sxs-lookup"><span data-stu-id="63312-246">Config</span></span>                                | <span data-ttu-id="63312-247">2.0</span><span class="sxs-lookup"><span data-stu-id="63312-247">2.0</span></span>        |
| <span data-ttu-id="63312-248">NuGet 配置</span><span class="sxs-lookup"><span data-stu-id="63312-248">NuGet Config</span></span>                                 | `nugetconfig`                     |              | <span data-ttu-id="63312-249">配置</span><span class="sxs-lookup"><span data-stu-id="63312-249">Config</span></span>                                | <span data-ttu-id="63312-250">1.0</span><span class="sxs-lookup"><span data-stu-id="63312-250">1.0</span></span>        |
| <span data-ttu-id="63312-251">Dotnet 本地工具清单文件</span><span class="sxs-lookup"><span data-stu-id="63312-251">Dotnet local tool manifest file</span></span>              | `tool-manifest`                   |              | <span data-ttu-id="63312-252">配置</span><span class="sxs-lookup"><span data-stu-id="63312-252">Config</span></span>                                | <span data-ttu-id="63312-253">3.0</span><span class="sxs-lookup"><span data-stu-id="63312-253">3.0</span></span>        |
| <span data-ttu-id="63312-254">Web 配置</span><span class="sxs-lookup"><span data-stu-id="63312-254">Web Config</span></span>                                   | `webconfig`                       |              | <span data-ttu-id="63312-255">配置</span><span class="sxs-lookup"><span data-stu-id="63312-255">Config</span></span>                                | <span data-ttu-id="63312-256">1.0</span><span class="sxs-lookup"><span data-stu-id="63312-256">1.0</span></span>        |
| <span data-ttu-id="63312-257">解决方案文件</span><span class="sxs-lookup"><span data-stu-id="63312-257">Solution File</span></span>                                | `sln`                             |              | <span data-ttu-id="63312-258">解决方案</span><span class="sxs-lookup"><span data-stu-id="63312-258">Solution</span></span>                              | <span data-ttu-id="63312-259">1.0</span><span class="sxs-lookup"><span data-stu-id="63312-259">1.0</span></span>        |
| <span data-ttu-id="63312-260">协议缓冲区文件</span><span class="sxs-lookup"><span data-stu-id="63312-260">Protocol Buffer File</span></span>                         | [`proto`](#namespace)             |              | <span data-ttu-id="63312-261">Web/gRPC</span><span class="sxs-lookup"><span data-stu-id="63312-261">Web/gRPC</span></span>                              | <span data-ttu-id="63312-262">3.0</span><span class="sxs-lookup"><span data-stu-id="63312-262">3.0</span></span>        |

## <a name="options"></a><span data-ttu-id="63312-263">选项</span><span class="sxs-lookup"><span data-stu-id="63312-263">Options</span></span>

- **`--dry-run`**

  <span data-ttu-id="63312-264">显示有关以下内容的摘要：给定命令运行导致模板创建时发生的情况。</span><span class="sxs-lookup"><span data-stu-id="63312-264">Displays a summary of what would happen if the given command were run if it would result in a template creation.</span></span> <span data-ttu-id="63312-265">自 .NET Core 2.2 SDK 起可用。</span><span class="sxs-lookup"><span data-stu-id="63312-265">Available since .NET Core 2.2 SDK.</span></span>

- **`--force`**

  <span data-ttu-id="63312-266">强制生成内容，即使会更改现有文件，也不例外。</span><span class="sxs-lookup"><span data-stu-id="63312-266">Forces content to be generated even if it would change existing files.</span></span> <span data-ttu-id="63312-267">当选择的模板将覆盖输出目录中的现有文件时，需要执行此操作。</span><span class="sxs-lookup"><span data-stu-id="63312-267">This is required when the template chosen would override existing files in the output directory.</span></span>

- **`-h|--help`**

  <span data-ttu-id="63312-268">打印命令帮助。</span><span class="sxs-lookup"><span data-stu-id="63312-268">Prints out help for the command.</span></span> <span data-ttu-id="63312-269">可针对 `dotnet new` 命令本身或任何模板调用它。</span><span class="sxs-lookup"><span data-stu-id="63312-269">It can be invoked for the `dotnet new` command itself or for any template.</span></span> <span data-ttu-id="63312-270">例如 `dotnet new mvc --help`。</span><span class="sxs-lookup"><span data-stu-id="63312-270">For example, `dotnet new mvc --help`.</span></span>

- **`-i|--install <PATH|NUGET_ID>`**

  <span data-ttu-id="63312-271">从提供的 `PATH` 或 `NUGET_ID` 安装模板包。</span><span class="sxs-lookup"><span data-stu-id="63312-271">Installs a template pack from the `PATH` or `NUGET_ID` provided.</span></span> <span data-ttu-id="63312-272">若要安装模板包的预发布版本，需要以 `<package-name>::<package-version>` 格式指定该版本。</span><span class="sxs-lookup"><span data-stu-id="63312-272">If you want to install a prerelease version of a template package, you need to specify the version in the format of `<package-name>::<package-version>`.</span></span> <span data-ttu-id="63312-273">默认情况下，`dotnet new` 为该版本传递 \*，它表示最新的稳定包版本。</span><span class="sxs-lookup"><span data-stu-id="63312-273">By default, `dotnet new` passes \* for the version, which represents the latest stable package version.</span></span> <span data-ttu-id="63312-274">请在[示例](#examples)部分查看示例。</span><span class="sxs-lookup"><span data-stu-id="63312-274">See an example in the [Examples](#examples) section.</span></span>
  
  <span data-ttu-id="63312-275">如果在运行此命令时已经安装了模板的某个版本，则该模板将更新到指定版本，如果没有指定版本，则将更新到最新的稳定版本。</span><span class="sxs-lookup"><span data-stu-id="63312-275">If a version of the template was already installed when you run this command, the template will be updated to the specified version, or to the latest stable version if no version was specified.</span></span>

  <span data-ttu-id="63312-276">若要了解如何创建自定义模板，请参阅 [dotnet new 自定义模板](custom-templates.md)。</span><span class="sxs-lookup"><span data-stu-id="63312-276">For information on creating custom templates, see [Custom templates for dotnet new](custom-templates.md).</span></span>

- **`-l|--list`**

  <span data-ttu-id="63312-277">列出包含指定名称的模板。</span><span class="sxs-lookup"><span data-stu-id="63312-277">Lists templates containing the specified name.</span></span> <span data-ttu-id="63312-278">如果未指定名称，则列出所有模板。</span><span class="sxs-lookup"><span data-stu-id="63312-278">If no name is specified, lists all templates.</span></span>

- **`-lang|--language {C#|F#|VB}`**

  <span data-ttu-id="63312-279">要创建的模板的语言。</span><span class="sxs-lookup"><span data-stu-id="63312-279">The language of the template to create.</span></span> <span data-ttu-id="63312-280">接受的语言因模板而异（请参阅[参数](#arguments)部分中的默认值）。</span><span class="sxs-lookup"><span data-stu-id="63312-280">The language accepted varies by the template (see defaults in the [arguments](#arguments) section).</span></span> <span data-ttu-id="63312-281">对于某些模板无效。</span><span class="sxs-lookup"><span data-stu-id="63312-281">Not valid for some templates.</span></span>

  > [!NOTE]
  > <span data-ttu-id="63312-282">某些 shell 将 `#` 解释为特殊字符。</span><span class="sxs-lookup"><span data-stu-id="63312-282">Some shells interpret `#` as a special character.</span></span> <span data-ttu-id="63312-283">在这些情况下，请将语言参数值括在引号中。</span><span class="sxs-lookup"><span data-stu-id="63312-283">In those cases, enclose the language parameter value in quotes.</span></span> <span data-ttu-id="63312-284">例如 `dotnet new console -lang "F#"`。</span><span class="sxs-lookup"><span data-stu-id="63312-284">For example, `dotnet new console -lang "F#"`.</span></span>

- **`-n|--name <OUTPUT_NAME>`**

  <span data-ttu-id="63312-285">所创建的输出的名称。</span><span class="sxs-lookup"><span data-stu-id="63312-285">The name for the created output.</span></span> <span data-ttu-id="63312-286">如果未指定名称，使用的是当前目录的名称。</span><span class="sxs-lookup"><span data-stu-id="63312-286">If no name is specified, the name of the current directory is used.</span></span>

- **`--nuget-source <SOURCE>`**

  <span data-ttu-id="63312-287">指定在安装期间要使用的 NuGet 源。</span><span class="sxs-lookup"><span data-stu-id="63312-287">Specifies a NuGet source to use during install.</span></span>

- **`-o|--output <OUTPUT_DIRECTORY>`**

  <span data-ttu-id="63312-288">用于放置生成的输出的位置。</span><span class="sxs-lookup"><span data-stu-id="63312-288">Location to place the generated output.</span></span> <span data-ttu-id="63312-289">默认为当前目录。</span><span class="sxs-lookup"><span data-stu-id="63312-289">The default is the current directory.</span></span>

- **`--type <TYPE>`**

  <span data-ttu-id="63312-290">根据可用类型筛选模板。</span><span class="sxs-lookup"><span data-stu-id="63312-290">Filters templates based on available types.</span></span> <span data-ttu-id="63312-291">预定义的值为 `project` 和 `item`。</span><span class="sxs-lookup"><span data-stu-id="63312-291">Predefined values are `project` and `item`.</span></span>

- **`-u|--uninstall [PATH|NUGET_ID]`**

  <span data-ttu-id="63312-292">在提供的 `PATH` 或 `NUGET_ID` 中卸载模板包。</span><span class="sxs-lookup"><span data-stu-id="63312-292">Uninstalls a template pack at the `PATH` or `NUGET_ID` provided.</span></span> <span data-ttu-id="63312-293">如果未指定 `<PATH|NUGET_ID>` 值，将显示所有当前安装的模板包及其关联的模板。</span><span class="sxs-lookup"><span data-stu-id="63312-293">When the `<PATH|NUGET_ID>` value isn't specified, all currently installed template packs and their associated templates are displayed.</span></span> <span data-ttu-id="63312-294">指定 `NUGET_ID` 时，请勿包含版本号。</span><span class="sxs-lookup"><span data-stu-id="63312-294">When specifying `NUGET_ID`, don't include the version number.</span></span>

  <span data-ttu-id="63312-295">如果未指定此选项的参数，该命令将列出已安装的模板及其详细信息。</span><span class="sxs-lookup"><span data-stu-id="63312-295">If you don't specify a parameter to this option, the command lists the installed templates and details about them.</span></span>

  > [!NOTE]
  > <span data-ttu-id="63312-296">若要使用 `PATH` 卸载模板，需要完全限定路径。</span><span class="sxs-lookup"><span data-stu-id="63312-296">To uninstall a template using a `PATH`, you need to fully qualify the path.</span></span> <span data-ttu-id="63312-297">例如，C:/Users/\<USER>/Documents/Templates/GarciaSoftware.ConsoleTemplate.CSharp 有效，但是包含文件夹中的 ./GarciaSoftware.ConsoleTemplate.CSharp 无效 。</span><span class="sxs-lookup"><span data-stu-id="63312-297">For example, *C:/Users/\<USER>/Documents/Templates/GarciaSoftware.ConsoleTemplate.CSharp* will work, but *./GarciaSoftware.ConsoleTemplate.CSharp* from the containing folder will not.</span></span>
  > <span data-ttu-id="63312-298">模板路径中不要包含最后的终止目录斜杠。</span><span class="sxs-lookup"><span data-stu-id="63312-298">Don't include a final terminating directory slash on your template path.</span></span>

- **`--update-apply`**

  <span data-ttu-id="63312-299">检查是否有可用于当前安装的模板包的更新并安装这些更新。</span><span class="sxs-lookup"><span data-stu-id="63312-299">Checks if there are updates available for the template packs that are currently installed and installs them.</span></span> <span data-ttu-id="63312-300">自 .NET Core 3.0 SDK 起可用。</span><span class="sxs-lookup"><span data-stu-id="63312-300">Available since .NET Core 3.0 SDK.</span></span>

- **`--update-check`**

  <span data-ttu-id="63312-301">检查是否有可用于当前安装的模板包的更新。</span><span class="sxs-lookup"><span data-stu-id="63312-301">Checks if there are updates available for the template packs that are currently installed.</span></span> <span data-ttu-id="63312-302">自 .NET Core 3.0 SDK 起可用。</span><span class="sxs-lookup"><span data-stu-id="63312-302">Available since .NET Core 3.0 SDK.</span></span>

## <a name="template-options"></a><span data-ttu-id="63312-303">模板选项</span><span class="sxs-lookup"><span data-stu-id="63312-303">Template options</span></span>

<span data-ttu-id="63312-304">每个项目模板都可能有附加选项。</span><span class="sxs-lookup"><span data-stu-id="63312-304">Each project template may have additional options available.</span></span> <span data-ttu-id="63312-305">核心模板有以下附加选项：</span><span class="sxs-lookup"><span data-stu-id="63312-305">The core templates have the following additional options:</span></span>

### `console`

- **`-f|--framework <FRAMEWORK>`**

  <span data-ttu-id="63312-306">指定目标[框架](../../standard/frameworks.md)。</span><span class="sxs-lookup"><span data-stu-id="63312-306">Specifies the [framework](../../standard/frameworks.md) to target.</span></span> <span data-ttu-id="63312-307">自 .NET Core 3.0 SDK 起可用。</span><span class="sxs-lookup"><span data-stu-id="63312-307">Available since .NET Core 3.0 SDK.</span></span>

  <span data-ttu-id="63312-308">下表根据所使用的 SDK 版本号列出了默认值：</span><span class="sxs-lookup"><span data-stu-id="63312-308">The following table lists the default values according to the SDK version number you're using:</span></span>

  | <span data-ttu-id="63312-309">SDK 版本</span><span class="sxs-lookup"><span data-stu-id="63312-309">SDK version</span></span> | <span data-ttu-id="63312-310">默认值</span><span class="sxs-lookup"><span data-stu-id="63312-310">Default value</span></span>   |
  |-------------|-----------------|
  | <span data-ttu-id="63312-311">5.0</span><span class="sxs-lookup"><span data-stu-id="63312-311">5.0</span></span>         | `net5.0`        |
  | <span data-ttu-id="63312-312">3.1</span><span class="sxs-lookup"><span data-stu-id="63312-312">3.1</span></span>         | `netcoreapp3.1` |
  | <span data-ttu-id="63312-313">3.0</span><span class="sxs-lookup"><span data-stu-id="63312-313">3.0</span></span>         | `netcoreapp3.0` |

- **`--langVersion <VERSION_NUMBER>`**

  <span data-ttu-id="63312-314">在已创建的项目文件中设置 `LangVersion` 属性。</span><span class="sxs-lookup"><span data-stu-id="63312-314">Sets the `LangVersion` property in the created project file.</span></span> <span data-ttu-id="63312-315">例如，使用 `--langVersion 7.3` 以使用 C# 7.3。</span><span class="sxs-lookup"><span data-stu-id="63312-315">For example, use `--langVersion 7.3` to use C# 7.3.</span></span> <span data-ttu-id="63312-316">不支持 F#。</span><span class="sxs-lookup"><span data-stu-id="63312-316">Not supported for F#.</span></span> <span data-ttu-id="63312-317">自 .NET Core 2.2 SDK 起可用。</span><span class="sxs-lookup"><span data-stu-id="63312-317">Available since .NET Core 2.2 SDK.</span></span>

  <span data-ttu-id="63312-318">有关默认的 C# 版本列表，请参阅[默认](../../csharp/language-reference/configure-language-version.md#defaults)。</span><span class="sxs-lookup"><span data-stu-id="63312-318">For a list of default C# versions, see [Defaults](../../csharp/language-reference/configure-language-version.md#defaults).</span></span>

- **`--no-restore`**

  <span data-ttu-id="63312-319">如已指定，则在项目创建期间不执行隐式还原。</span><span class="sxs-lookup"><span data-stu-id="63312-319">If specified, doesn't execute an implicit restore during project creation.</span></span> <span data-ttu-id="63312-320">自 .NET Core 2.2 SDK 起可用。</span><span class="sxs-lookup"><span data-stu-id="63312-320">Available since .NET Core 2.2 SDK.</span></span>

***

### `classlib`

- **`-f|--framework <FRAMEWORK>`**

  <span data-ttu-id="63312-321">指定目标[框架](../../standard/frameworks.md)。</span><span class="sxs-lookup"><span data-stu-id="63312-321">Specifies the [framework](../../standard/frameworks.md) to target.</span></span> <span data-ttu-id="63312-322">值：`net5.0` 或 `netcoreapp<version>`（若要创建 .NET 类库），或`netstandard<version>`（若要创建 .NET Standard 类库）。</span><span class="sxs-lookup"><span data-stu-id="63312-322">Values: `net5.0` or `netcoreapp<version>` to create a .NET Class Library or `netstandard<version>` to create a .NET Standard Class Library.</span></span> <span data-ttu-id="63312-323">.NET 5.0 SDK 的默认值是 `net5.0`。</span><span class="sxs-lookup"><span data-stu-id="63312-323">The default value for .NET 5.0 SDK is `net5.0`.</span></span>

- **`--langVersion <VERSION_NUMBER>`**

  <span data-ttu-id="63312-324">在已创建的项目文件中设置 `LangVersion` 属性。</span><span class="sxs-lookup"><span data-stu-id="63312-324">Sets the `LangVersion` property in the created project file.</span></span> <span data-ttu-id="63312-325">例如，使用 `--langVersion 7.3` 以使用 C# 7.3。</span><span class="sxs-lookup"><span data-stu-id="63312-325">For example, use `--langVersion 7.3` to use C# 7.3.</span></span> <span data-ttu-id="63312-326">不支持 F#。</span><span class="sxs-lookup"><span data-stu-id="63312-326">Not supported for F#.</span></span> <span data-ttu-id="63312-327">自 .NET Core 2.2 SDK 起可用。</span><span class="sxs-lookup"><span data-stu-id="63312-327">Available since .NET Core 2.2 SDK.</span></span>

  <span data-ttu-id="63312-328">有关默认的 C# 版本列表，请参阅[默认](../../csharp/language-reference/configure-language-version.md#defaults)。</span><span class="sxs-lookup"><span data-stu-id="63312-328">For a list of default C# versions, see [Defaults](../../csharp/language-reference/configure-language-version.md#defaults).</span></span>

- **`--no-restore`**

  <span data-ttu-id="63312-329">在项目创建期间不执行隐式还原。</span><span class="sxs-lookup"><span data-stu-id="63312-329">Doesn't execute an implicit restore during project creation.</span></span>

***

### <a name="wpf-wpflib-wpfcustomcontrollib-wpfusercontrollib"></a><a name="wpf"></a> <span data-ttu-id="63312-330">`wpf`, `wpflib`, `wpfcustomcontrollib`, `wpfusercontrollib`</span><span class="sxs-lookup"><span data-stu-id="63312-330">`wpf`, `wpflib`, `wpfcustomcontrollib`, `wpfusercontrollib`</span></span>

- **`-f|--framework <FRAMEWORK>`**

  <span data-ttu-id="63312-331">指定目标[框架](../../standard/frameworks.md)。</span><span class="sxs-lookup"><span data-stu-id="63312-331">Specifies the [framework](../../standard/frameworks.md) to target.</span></span> <span data-ttu-id="63312-332">默认值为 `net5.0`。</span><span class="sxs-lookup"><span data-stu-id="63312-332">The default value is `net5.0`.</span></span> <span data-ttu-id="63312-333">自 .NET Core 3.1 SDK 起可用。</span><span class="sxs-lookup"><span data-stu-id="63312-333">Available since .NET Core 3.1 SDK.</span></span>

- **`--langVersion <VERSION_NUMBER>`**

  <span data-ttu-id="63312-334">在已创建的项目文件中设置 `LangVersion` 属性。</span><span class="sxs-lookup"><span data-stu-id="63312-334">Sets the `LangVersion` property in the created project file.</span></span> <span data-ttu-id="63312-335">例如，使用 `--langVersion 7.3` 以使用 C# 7.3。</span><span class="sxs-lookup"><span data-stu-id="63312-335">For example, use `--langVersion 7.3` to use C# 7.3.</span></span>

  <span data-ttu-id="63312-336">有关默认的 C# 版本列表，请参阅[默认](../../csharp/language-reference/configure-language-version.md#defaults)。</span><span class="sxs-lookup"><span data-stu-id="63312-336">For a list of default C# versions, see [Defaults](../../csharp/language-reference/configure-language-version.md#defaults).</span></span>

- **`--no-restore`**

  <span data-ttu-id="63312-337">在项目创建期间不执行隐式还原。</span><span class="sxs-lookup"><span data-stu-id="63312-337">Doesn't execute an implicit restore during project creation.</span></span>

***

### <a name="winforms-winformslib"></a><a name="winforms"></a> <span data-ttu-id="63312-338">`winforms`, `winformslib`</span><span class="sxs-lookup"><span data-stu-id="63312-338">`winforms`, `winformslib`</span></span>

- **`--langVersion <VERSION_NUMBER>`**

  <span data-ttu-id="63312-339">在已创建的项目文件中设置 `LangVersion` 属性。</span><span class="sxs-lookup"><span data-stu-id="63312-339">Sets the `LangVersion` property in the created project file.</span></span> <span data-ttu-id="63312-340">例如，使用 `--langVersion 7.3` 以使用 C# 7.3。</span><span class="sxs-lookup"><span data-stu-id="63312-340">For example, use `--langVersion 7.3` to use C# 7.3.</span></span>

  <span data-ttu-id="63312-341">有关默认的 C# 版本列表，请参阅[默认](../../csharp/language-reference/configure-language-version.md#defaults)。</span><span class="sxs-lookup"><span data-stu-id="63312-341">For a list of default C# versions, see [Defaults](../../csharp/language-reference/configure-language-version.md#defaults).</span></span>

- **`--no-restore`**

  <span data-ttu-id="63312-342">在项目创建期间不执行隐式还原。</span><span class="sxs-lookup"><span data-stu-id="63312-342">Doesn't execute an implicit restore during project creation.</span></span>

***

### <a name="worker-grpc"></a><a name="web-others"></a> <span data-ttu-id="63312-343">`worker`, `grpc`</span><span class="sxs-lookup"><span data-stu-id="63312-343">`worker`, `grpc`</span></span>

- **`-f|--framework <FRAMEWORK>`**

  <span data-ttu-id="63312-344">指定目标[框架](../../standard/frameworks.md)。</span><span class="sxs-lookup"><span data-stu-id="63312-344">Specifies the [framework](../../standard/frameworks.md) to target.</span></span> <span data-ttu-id="63312-345">默认值为 `netcoreapp3.1`。</span><span class="sxs-lookup"><span data-stu-id="63312-345">The default value is `netcoreapp3.1`.</span></span> <span data-ttu-id="63312-346">自 .NET Core 3.1 SDK 起可用。</span><span class="sxs-lookup"><span data-stu-id="63312-346">Available since .NET Core 3.1 SDK.</span></span>

- **`--exclude-launch-settings`**

  <span data-ttu-id="63312-347">从生成的模板中排除 launchSettings.json。</span><span class="sxs-lookup"><span data-stu-id="63312-347">Excludes *launchSettings.json* from the generated template.</span></span>

- **`--no-restore`**

  <span data-ttu-id="63312-348">在项目创建期间不执行隐式还原。</span><span class="sxs-lookup"><span data-stu-id="63312-348">Doesn't execute an implicit restore during project creation.</span></span>

***

### <a name="mstest-xunit"></a><a name="test"></a> <span data-ttu-id="63312-349">`mstest`, `xunit`</span><span class="sxs-lookup"><span data-stu-id="63312-349">`mstest`, `xunit`</span></span>

- **`-f|--framework <FRAMEWORK>`**

  <span data-ttu-id="63312-350">指定目标[框架](../../standard/frameworks.md)。</span><span class="sxs-lookup"><span data-stu-id="63312-350">Specifies the [framework](../../standard/frameworks.md) to target.</span></span> <span data-ttu-id="63312-351">自 .NET Core 3.0 SDK 起可用的选项。</span><span class="sxs-lookup"><span data-stu-id="63312-351">Option available since .NET Core 3.0 SDK.</span></span>

  <span data-ttu-id="63312-352">下表根据所使用的 SDK 版本号列出了默认值：</span><span class="sxs-lookup"><span data-stu-id="63312-352">The following table lists the default values according to the SDK version number you're using:</span></span>

  | <span data-ttu-id="63312-353">SDK 版本</span><span class="sxs-lookup"><span data-stu-id="63312-353">SDK version</span></span> | <span data-ttu-id="63312-354">默认值</span><span class="sxs-lookup"><span data-stu-id="63312-354">Default value</span></span>   |
  |-------------|-----------------|
  | <span data-ttu-id="63312-355">5.0</span><span class="sxs-lookup"><span data-stu-id="63312-355">5.0</span></span>         | `net5.0`        |
  | <span data-ttu-id="63312-356">3.1</span><span class="sxs-lookup"><span data-stu-id="63312-356">3.1</span></span>         | `netcoreapp3.1` |
  | <span data-ttu-id="63312-357">3.0</span><span class="sxs-lookup"><span data-stu-id="63312-357">3.0</span></span>         | `netcoreapp3.0` |

- **`-p|--enable-pack`**

  <span data-ttu-id="63312-358">允许使用 [dotnet pack](dotnet-pack.md) 为项目打包。</span><span class="sxs-lookup"><span data-stu-id="63312-358">Enables packaging for the project using [dotnet pack](dotnet-pack.md).</span></span>

- **`--no-restore`**

  <span data-ttu-id="63312-359">在项目创建期间不执行隐式还原。</span><span class="sxs-lookup"><span data-stu-id="63312-359">Doesn't execute an implicit restore during project creation.</span></span>

***

### `nunit`

- **`-f|--framework <FRAMEWORK>`**

  <span data-ttu-id="63312-360">指定目标[框架](../../standard/frameworks.md)。</span><span class="sxs-lookup"><span data-stu-id="63312-360">Specifies the [framework](../../standard/frameworks.md) to target.</span></span>

  <span data-ttu-id="63312-361">下表根据所使用的 SDK 版本号列出了默认值：</span><span class="sxs-lookup"><span data-stu-id="63312-361">The following table lists the default values according to the SDK version number you're using:</span></span>

  | <span data-ttu-id="63312-362">SDK 版本</span><span class="sxs-lookup"><span data-stu-id="63312-362">SDK version</span></span> | <span data-ttu-id="63312-363">默认值</span><span class="sxs-lookup"><span data-stu-id="63312-363">Default value</span></span>   |
  |-------------|-----------------|
  | <span data-ttu-id="63312-364">5.0</span><span class="sxs-lookup"><span data-stu-id="63312-364">5.0</span></span>         | `net5.0`        |
  | <span data-ttu-id="63312-365">3.1</span><span class="sxs-lookup"><span data-stu-id="63312-365">3.1</span></span>         | `netcoreapp3.1` |
  | <span data-ttu-id="63312-366">3.0</span><span class="sxs-lookup"><span data-stu-id="63312-366">3.0</span></span>         | `netcoreapp3.0` |
  | <span data-ttu-id="63312-367">2.2</span><span class="sxs-lookup"><span data-stu-id="63312-367">2.2</span></span>         | `netcoreapp2.2` |
  | <span data-ttu-id="63312-368">2.1</span><span class="sxs-lookup"><span data-stu-id="63312-368">2.1</span></span>         | `netcoreapp2.1` |

- **`-p|--enable-pack`**

  <span data-ttu-id="63312-369">允许使用 [dotnet pack](dotnet-pack.md) 为项目打包。</span><span class="sxs-lookup"><span data-stu-id="63312-369">Enables packaging for the project using [dotnet pack](dotnet-pack.md).</span></span>

- **`--no-restore`**

  <span data-ttu-id="63312-370">在项目创建期间不执行隐式还原。</span><span class="sxs-lookup"><span data-stu-id="63312-370">Doesn't execute an implicit restore during project creation.</span></span>

***

### `page`

- **`-na|--namespace <NAMESPACE_NAME>`**

  <span data-ttu-id="63312-371">已生成代码的命名空间。</span><span class="sxs-lookup"><span data-stu-id="63312-371">Namespace for the generated code.</span></span> <span data-ttu-id="63312-372">默认值为 `MyApp.Namespace`。</span><span class="sxs-lookup"><span data-stu-id="63312-372">The default value is `MyApp.Namespace`.</span></span>

- **`-np|--no-pagemodel`**

  <span data-ttu-id="63312-373">创建不含 PageModel 的页。</span><span class="sxs-lookup"><span data-stu-id="63312-373">Creates the page without a PageModel.</span></span>

***

### <a name="viewimports-proto"></a><a name="namespace"></a> <span data-ttu-id="63312-374">`viewimports`, `proto`</span><span class="sxs-lookup"><span data-stu-id="63312-374">`viewimports`, `proto`</span></span>

- **`-na|--namespace <NAMESPACE_NAME>`**

  <span data-ttu-id="63312-375">已生成代码的命名空间。</span><span class="sxs-lookup"><span data-stu-id="63312-375">Namespace for the generated code.</span></span> <span data-ttu-id="63312-376">默认值为 `MyApp.Namespace`。</span><span class="sxs-lookup"><span data-stu-id="63312-376">The default value is `MyApp.Namespace`.</span></span>

***

### `blazorserver`

- **`-au|--auth <AUTHENTICATION_TYPE>`**

  <span data-ttu-id="63312-377">要使用的身份验证类型。</span><span class="sxs-lookup"><span data-stu-id="63312-377">The type of authentication to use.</span></span> <span data-ttu-id="63312-378">可能的值为：</span><span class="sxs-lookup"><span data-stu-id="63312-378">The possible values are:</span></span>

  - <span data-ttu-id="63312-379">`None` - 不进行身份验证（默认）。</span><span class="sxs-lookup"><span data-stu-id="63312-379">`None` - No authentication (Default).</span></span>
  - <span data-ttu-id="63312-380">`Individual` - 个人身份验证。</span><span class="sxs-lookup"><span data-stu-id="63312-380">`Individual` - Individual authentication.</span></span>
  - <span data-ttu-id="63312-381">`IndividualB2C` - 使用 Azure AD B2C 进行个人身份验证。</span><span class="sxs-lookup"><span data-stu-id="63312-381">`IndividualB2C` - Individual authentication with Azure AD B2C.</span></span>
  - <span data-ttu-id="63312-382">`SingleOrg` - 对一个租户进行组织身份验证。</span><span class="sxs-lookup"><span data-stu-id="63312-382">`SingleOrg` - Organizational authentication for a single tenant.</span></span>
  - <span data-ttu-id="63312-383">`MultiOrg` - 对多个租户进行组织身份验证。</span><span class="sxs-lookup"><span data-stu-id="63312-383">`MultiOrg` - Organizational authentication for multiple tenants.</span></span>
  - <span data-ttu-id="63312-384">`Windows` - Windows 身份验证。</span><span class="sxs-lookup"><span data-stu-id="63312-384">`Windows` - Windows authentication.</span></span>

- **`--aad-b2c-instance <INSTANCE>`**

  <span data-ttu-id="63312-385">要连接到的 Azure Active Directory B2C 实例。</span><span class="sxs-lookup"><span data-stu-id="63312-385">The Azure Active Directory B2C instance to connect to.</span></span> <span data-ttu-id="63312-386">与 `IndividualB2C` 身份验证结合使用。</span><span class="sxs-lookup"><span data-stu-id="63312-386">Use with `IndividualB2C` authentication.</span></span> <span data-ttu-id="63312-387">默认值为 `https://login.microsoftonline.com/tfp/`。</span><span class="sxs-lookup"><span data-stu-id="63312-387">The default value is `https://login.microsoftonline.com/tfp/`.</span></span>

- **`-ssp|--susi-policy-id <ID>`**

  <span data-ttu-id="63312-388">此项目的登录和注册策略 ID。</span><span class="sxs-lookup"><span data-stu-id="63312-388">The sign-in and sign-up policy ID for this project.</span></span> <span data-ttu-id="63312-389">与 `IndividualB2C` 身份验证结合使用。</span><span class="sxs-lookup"><span data-stu-id="63312-389">Use with `IndividualB2C` authentication.</span></span>

- **`-rp|--reset-password-policy-id <ID>`**

  <span data-ttu-id="63312-390">此项目的重置密码策略 ID。</span><span class="sxs-lookup"><span data-stu-id="63312-390">The reset password policy ID for this project.</span></span> <span data-ttu-id="63312-391">与 `IndividualB2C` 身份验证结合使用。</span><span class="sxs-lookup"><span data-stu-id="63312-391">Use with `IndividualB2C` authentication.</span></span>

- **`-ep|--edit-profile-policy-id <ID>`**

  <span data-ttu-id="63312-392">此项目的编辑配置文件策略 ID。</span><span class="sxs-lookup"><span data-stu-id="63312-392">The edit profile policy ID for this project.</span></span> <span data-ttu-id="63312-393">与 `IndividualB2C` 身份验证结合使用。</span><span class="sxs-lookup"><span data-stu-id="63312-393">Use with `IndividualB2C` authentication.</span></span>

- **`--aad-instance <INSTANCE>`**

  <span data-ttu-id="63312-394">要连接到的 Azure Active Directory 实例。</span><span class="sxs-lookup"><span data-stu-id="63312-394">The Azure Active Directory instance to connect to.</span></span> <span data-ttu-id="63312-395">与 `SingleOrg` 或 `MultiOrg` 身份验证结合使用。</span><span class="sxs-lookup"><span data-stu-id="63312-395">Use with `SingleOrg` or `MultiOrg` authentication.</span></span> <span data-ttu-id="63312-396">默认值为 `https://login.microsoftonline.com/`。</span><span class="sxs-lookup"><span data-stu-id="63312-396">The default value is `https://login.microsoftonline.com/`.</span></span>

- **`--client-id <ID>`**

  <span data-ttu-id="63312-397">此项目的客户端 ID。</span><span class="sxs-lookup"><span data-stu-id="63312-397">The Client ID for this project.</span></span> <span data-ttu-id="63312-398">与 `IndividualB2C`、`SingleOrg` 或 `MultiOrg` 身份验证结合使用。</span><span class="sxs-lookup"><span data-stu-id="63312-398">Use with `IndividualB2C`, `SingleOrg`, or `MultiOrg` authentication.</span></span> <span data-ttu-id="63312-399">默认值为 `11111111-1111-1111-11111111111111111`。</span><span class="sxs-lookup"><span data-stu-id="63312-399">The default value is `11111111-1111-1111-11111111111111111`.</span></span>

- **`--domain <DOMAIN>`**

  <span data-ttu-id="63312-400">目录租户的域。</span><span class="sxs-lookup"><span data-stu-id="63312-400">The domain for the directory tenant.</span></span> <span data-ttu-id="63312-401">与 `SingleOrg` 或 `IndividualB2C` 身份验证结合使用。</span><span class="sxs-lookup"><span data-stu-id="63312-401">Use with `SingleOrg` or `IndividualB2C` authentication.</span></span> <span data-ttu-id="63312-402">默认值为 `qualified.domain.name`。</span><span class="sxs-lookup"><span data-stu-id="63312-402">The default value is `qualified.domain.name`.</span></span>

- **`--tenant-id <ID>`**

  <span data-ttu-id="63312-403">要连接到的目录的 TenantId ID。</span><span class="sxs-lookup"><span data-stu-id="63312-403">The TenantId ID of the directory to connect to.</span></span> <span data-ttu-id="63312-404">与 `SingleOrg` 身份验证结合使用。</span><span class="sxs-lookup"><span data-stu-id="63312-404">Use with `SingleOrg` authentication.</span></span> <span data-ttu-id="63312-405">默认值为 `22222222-2222-2222-2222-222222222222`。</span><span class="sxs-lookup"><span data-stu-id="63312-405">The default value is `22222222-2222-2222-2222-222222222222`.</span></span>

- **`--callback-path <PATH>`**

  <span data-ttu-id="63312-406">重定向 URI 的应用程序基路径中的请求路径。</span><span class="sxs-lookup"><span data-stu-id="63312-406">The request path within the application's base path of the redirect URI.</span></span> <span data-ttu-id="63312-407">与 `SingleOrg` 或 `IndividualB2C` 身份验证结合使用。</span><span class="sxs-lookup"><span data-stu-id="63312-407">Use with `SingleOrg` or `IndividualB2C` authentication.</span></span> <span data-ttu-id="63312-408">默认值为 `/signin-oidc`。</span><span class="sxs-lookup"><span data-stu-id="63312-408">The default value is `/signin-oidc`.</span></span>

- **`-r|--org-read-access`**

  <span data-ttu-id="63312-409">允许此应用程序对目录进行读取访问。</span><span class="sxs-lookup"><span data-stu-id="63312-409">Allows this application read-access to the directory.</span></span> <span data-ttu-id="63312-410">仅适用于 `SingleOrg` 或 `MultiOrg` 身份验证。</span><span class="sxs-lookup"><span data-stu-id="63312-410">Only applies to `SingleOrg` or `MultiOrg` authentication.</span></span>

- **`--exclude-launch-settings`**

  <span data-ttu-id="63312-411">从生成的模板中排除 launchSettings.json。</span><span class="sxs-lookup"><span data-stu-id="63312-411">Excludes *launchSettings.json* from the generated template.</span></span>

- **`--no-https`**

  <span data-ttu-id="63312-412">关闭 HTTPS。</span><span class="sxs-lookup"><span data-stu-id="63312-412">Turns off HTTPS.</span></span> <span data-ttu-id="63312-413">此选项仅适用于 `Individual`、`IndividualB2C`、`SingleOrg` 和 `MultiOrg` 未用于 `--auth` 的情况。</span><span class="sxs-lookup"><span data-stu-id="63312-413">This option only applies if `Individual`, `IndividualB2C`, `SingleOrg`, or `MultiOrg` aren't being used for `--auth`.</span></span>

- **`-uld|--use-local-db`**

  <span data-ttu-id="63312-414">指定应使用 LocalDB，而不使用 SQLite。</span><span class="sxs-lookup"><span data-stu-id="63312-414">Specifies LocalDB should be used instead of SQLite.</span></span> <span data-ttu-id="63312-415">仅适用于 `Individual` 或 `IndividualB2C` 身份验证。</span><span class="sxs-lookup"><span data-stu-id="63312-415">Only applies to `Individual` or `IndividualB2C` authentication.</span></span>

- **`--no-restore`**

  <span data-ttu-id="63312-416">在项目创建期间不执行隐式还原。</span><span class="sxs-lookup"><span data-stu-id="63312-416">Doesn't execute an implicit restore during project creation.</span></span>

***

### `blazorwasm`

- **`-f|--framework <FRAMEWORK>`**

  <span data-ttu-id="63312-417">指定目标[框架](../../standard/frameworks.md)。</span><span class="sxs-lookup"><span data-stu-id="63312-417">Specifies the [framework](../../standard/frameworks.md) to target.</span></span>

  <span data-ttu-id="63312-418">下表根据所使用的 SDK 版本号列出了默认值：</span><span class="sxs-lookup"><span data-stu-id="63312-418">The following table lists the default values according to the SDK version number you're using:</span></span>

  | <span data-ttu-id="63312-419">SDK 版本</span><span class="sxs-lookup"><span data-stu-id="63312-419">SDK version</span></span> | <span data-ttu-id="63312-420">默认值</span><span class="sxs-lookup"><span data-stu-id="63312-420">Default value</span></span>   |
  |-------------|-----------------|
  | <span data-ttu-id="63312-421">5.0</span><span class="sxs-lookup"><span data-stu-id="63312-421">5.0</span></span>         | `net5.0`        |
  | <span data-ttu-id="63312-422">3.1</span><span class="sxs-lookup"><span data-stu-id="63312-422">3.1</span></span>         | `netcoreapp3.1` |

- **`--no-restore`**

  <span data-ttu-id="63312-423">在项目创建期间不执行隐式还原。</span><span class="sxs-lookup"><span data-stu-id="63312-423">Doesn't execute an implicit restore during project creation.</span></span>

- **`-ho|--hosted`**

  <span data-ttu-id="63312-424">包括 Blazor WebAssembly 应用的 ASP.NET Core 主机。</span><span class="sxs-lookup"><span data-stu-id="63312-424">Includes an ASP.NET Core host for the Blazor WebAssembly app.</span></span>

- **`-au|--auth <AUTHENTICATION_TYPE>`**

  <span data-ttu-id="63312-425">要使用的身份验证类型。</span><span class="sxs-lookup"><span data-stu-id="63312-425">The type of authentication to use.</span></span> <span data-ttu-id="63312-426">可能的值为：</span><span class="sxs-lookup"><span data-stu-id="63312-426">The possible values are:</span></span>

  - <span data-ttu-id="63312-427">`None` - 不进行身份验证（默认）。</span><span class="sxs-lookup"><span data-stu-id="63312-427">`None` - No authentication (Default).</span></span>
  - <span data-ttu-id="63312-428">`Individual` - 个人身份验证。</span><span class="sxs-lookup"><span data-stu-id="63312-428">`Individual` - Individual authentication.</span></span>
  - <span data-ttu-id="63312-429">`IndividualB2C` - 使用 Azure AD B2C 进行个人身份验证。</span><span class="sxs-lookup"><span data-stu-id="63312-429">`IndividualB2C` - Individual authentication with Azure AD B2C.</span></span>
  - <span data-ttu-id="63312-430">`SingleOrg` - 对一个租户进行组织身份验证。</span><span class="sxs-lookup"><span data-stu-id="63312-430">`SingleOrg` - Organizational authentication for a single tenant.</span></span>

- **`--authority <AUTHORITY>`**

  <span data-ttu-id="63312-431">OIDC 提供程序所属的机构。</span><span class="sxs-lookup"><span data-stu-id="63312-431">The authority of the OIDC provider.</span></span> <span data-ttu-id="63312-432">与 `Individual` 身份验证结合使用。</span><span class="sxs-lookup"><span data-stu-id="63312-432">Use with `Individual` authentication.</span></span> <span data-ttu-id="63312-433">默认值为 `https://login.microsoftonline.com/`。</span><span class="sxs-lookup"><span data-stu-id="63312-433">The default value is `https://login.microsoftonline.com/`.</span></span>

- **`--aad-b2c-instance <INSTANCE>`**

  <span data-ttu-id="63312-434">要连接到的 Azure Active Directory B2C 实例。</span><span class="sxs-lookup"><span data-stu-id="63312-434">The Azure Active Directory B2C instance to connect to.</span></span> <span data-ttu-id="63312-435">与 `IndividualB2C` 身份验证结合使用。</span><span class="sxs-lookup"><span data-stu-id="63312-435">Use with `IndividualB2C` authentication.</span></span> <span data-ttu-id="63312-436">默认值为 `https://aadB2CInstance.b2clogin.com/`。</span><span class="sxs-lookup"><span data-stu-id="63312-436">The default value is `https://aadB2CInstance.b2clogin.com/`.</span></span>

- **`-ssp|--susi-policy-id <ID>`**

  <span data-ttu-id="63312-437">此项目的登录和注册策略 ID。</span><span class="sxs-lookup"><span data-stu-id="63312-437">The sign-in and sign-up policy ID for this project.</span></span> <span data-ttu-id="63312-438">与 `IndividualB2C` 身份验证结合使用。</span><span class="sxs-lookup"><span data-stu-id="63312-438">Use with `IndividualB2C` authentication.</span></span>

- **`--aad-instance <INSTANCE>`**

  <span data-ttu-id="63312-439">要连接到的 Azure Active Directory 实例。</span><span class="sxs-lookup"><span data-stu-id="63312-439">The Azure Active Directory instance to connect to.</span></span> <span data-ttu-id="63312-440">与 `SingleOrg` 身份验证结合使用。</span><span class="sxs-lookup"><span data-stu-id="63312-440">Use with `SingleOrg` authentication.</span></span> <span data-ttu-id="63312-441">默认值为 `https://login.microsoftonline.com/`。</span><span class="sxs-lookup"><span data-stu-id="63312-441">The default value is `https://login.microsoftonline.com/`.</span></span>

- **`--client-id <ID>`**

  <span data-ttu-id="63312-442">此项目的客户端 ID。</span><span class="sxs-lookup"><span data-stu-id="63312-442">The Client ID for this project.</span></span> <span data-ttu-id="63312-443">在独立方案中与 `IndividualB2C`、`SingleOrg` 或 `Individual` 身份验证一起使用。</span><span class="sxs-lookup"><span data-stu-id="63312-443">Use with `IndividualB2C`, `SingleOrg`, or `Individual` authentication in standalone scenarios.</span></span> <span data-ttu-id="63312-444">默认值为 `33333333-3333-3333-33333333333333333`。</span><span class="sxs-lookup"><span data-stu-id="63312-444">The default value is `33333333-3333-3333-33333333333333333`.</span></span>

- **`--domain <DOMAIN>`**

  <span data-ttu-id="63312-445">目录租户的域。</span><span class="sxs-lookup"><span data-stu-id="63312-445">The domain for the directory tenant.</span></span> <span data-ttu-id="63312-446">与 `SingleOrg` 或 `IndividualB2C` 身份验证结合使用。</span><span class="sxs-lookup"><span data-stu-id="63312-446">Use with `SingleOrg` or `IndividualB2C` authentication.</span></span> <span data-ttu-id="63312-447">默认值为 `qualified.domain.name`。</span><span class="sxs-lookup"><span data-stu-id="63312-447">The default value is `qualified.domain.name`.</span></span>

- **`--app-id-uri <URI>`**

  <span data-ttu-id="63312-448">要调用的服务器 API 的应用 ID URI。</span><span class="sxs-lookup"><span data-stu-id="63312-448">The App ID Uri for the server API you want to call.</span></span> <span data-ttu-id="63312-449">与 `SingleOrg` 或 `IndividualB2C` 身份验证结合使用。</span><span class="sxs-lookup"><span data-stu-id="63312-449">Use with `SingleOrg` or `IndividualB2C` authentication.</span></span> <span data-ttu-id="63312-450">默认值为 `api.id.uri`。</span><span class="sxs-lookup"><span data-stu-id="63312-450">The default value is `api.id.uri`.</span></span>

- **`--api-client-id <ID>`**

  <span data-ttu-id="63312-451">服务器承载的 API 的客户端 ID。</span><span class="sxs-lookup"><span data-stu-id="63312-451">The Client ID for the API that the server hosts.</span></span> <span data-ttu-id="63312-452">与 `SingleOrg` 或 `IndividualB2C` 身份验证结合使用。</span><span class="sxs-lookup"><span data-stu-id="63312-452">Use with `SingleOrg` or `IndividualB2C` authentication.</span></span> <span data-ttu-id="63312-453">默认值为 `11111111-1111-1111-11111111111111111`。</span><span class="sxs-lookup"><span data-stu-id="63312-453">The default value is `11111111-1111-1111-11111111111111111`.</span></span>

- **`-s|--default-scope <SCOPE>`**

  <span data-ttu-id="63312-454">客户端为预配访问令牌所需请求的 API 作用域。</span><span class="sxs-lookup"><span data-stu-id="63312-454">The API scope the client needs to request to provision an access token.</span></span> <span data-ttu-id="63312-455">与 `SingleOrg` 或 `IndividualB2C` 身份验证结合使用。</span><span class="sxs-lookup"><span data-stu-id="63312-455">Use with `SingleOrg` or `IndividualB2C` authentication.</span></span> <span data-ttu-id="63312-456">默认值为 `user_impersonation`。</span><span class="sxs-lookup"><span data-stu-id="63312-456">The default value is `user_impersonation`.</span></span>

- **`--tenant-id <ID>`**

  <span data-ttu-id="63312-457">要连接到的目录的 TenantId ID。</span><span class="sxs-lookup"><span data-stu-id="63312-457">The TenantId ID of the directory to connect to.</span></span> <span data-ttu-id="63312-458">与 `SingleOrg` 身份验证结合使用。</span><span class="sxs-lookup"><span data-stu-id="63312-458">Use with `SingleOrg` authentication.</span></span> <span data-ttu-id="63312-459">默认值为 `22222222-2222-2222-2222-222222222222`。</span><span class="sxs-lookup"><span data-stu-id="63312-459">The default value is `22222222-2222-2222-2222-222222222222`.</span></span>

- **`-r|--org-read-access`**

  <span data-ttu-id="63312-460">允许此应用程序对目录进行读取访问。</span><span class="sxs-lookup"><span data-stu-id="63312-460">Allows this application read-access to the directory.</span></span> <span data-ttu-id="63312-461">仅适用于 `SingleOrg` 身份验证。</span><span class="sxs-lookup"><span data-stu-id="63312-461">Only applies to `SingleOrg` authentication.</span></span>

- **`--exclude-launch-settings`**

  <span data-ttu-id="63312-462">从生成的模板中排除 launchSettings.json。</span><span class="sxs-lookup"><span data-stu-id="63312-462">Excludes *launchSettings.json* from the generated template.</span></span>

- **`-p|--pwa`**

  <span data-ttu-id="63312-463">生成支持安装和脱机使用的渐进式 Web 应用程序 (PWA)。</span><span class="sxs-lookup"><span data-stu-id="63312-463">produces a Progressive Web Application (PWA) supporting installation and offline use.</span></span>

- **`--no-https`**

  <span data-ttu-id="63312-464">关闭 HTTPS。</span><span class="sxs-lookup"><span data-stu-id="63312-464">Turns off HTTPS.</span></span> <span data-ttu-id="63312-465">此选项仅适用于 `Individual`、`IndividualB2C` 和 `SingleOrg` 未用于 `--auth` 的情况。</span><span class="sxs-lookup"><span data-stu-id="63312-465">This option only applies if `Individual`, `IndividualB2C`, or `SingleOrg` aren't being used for `--auth`.</span></span>

- **`-uld|--use-local-db`**

  <span data-ttu-id="63312-466">指定应使用 LocalDB，而不使用 SQLite。</span><span class="sxs-lookup"><span data-stu-id="63312-466">Specifies LocalDB should be used instead of SQLite.</span></span> <span data-ttu-id="63312-467">仅适用于 `Individual` 或 `IndividualB2C` 身份验证。</span><span class="sxs-lookup"><span data-stu-id="63312-467">Only applies to `Individual` or `IndividualB2C` authentication.</span></span>

- **`--called-api-url <URL>`**

  <span data-ttu-id="63312-468">要从 Web 应用调用的 API 的 URL。</span><span class="sxs-lookup"><span data-stu-id="63312-468">URL of the API to call from the web app.</span></span> <span data-ttu-id="63312-469">仅适用于未指定 ASP.NET Core 主机的 `SingleOrg` 或 `IndividualB2C` 身份验证。</span><span class="sxs-lookup"><span data-stu-id="63312-469">Only applies to `SingleOrg` or `IndividualB2C` authentication without an ASP.NET Core host specified.</span></span> <span data-ttu-id="63312-470">默认值为 `https://graph.microsoft.com/v1.0/me`。</span><span class="sxs-lookup"><span data-stu-id="63312-470">The default value is `https://graph.microsoft.com/v1.0/me`.</span></span>

- **`--calls-graph`**

  <span data-ttu-id="63312-471">指定 Web 应用是否调用 Microsoft Graph。</span><span class="sxs-lookup"><span data-stu-id="63312-471">Specifies if the web app calls Microsoft Graph.</span></span> <span data-ttu-id="63312-472">仅适用于 `SingleOrg` 身份验证。</span><span class="sxs-lookup"><span data-stu-id="63312-472">Only applies to `SingleOrg` authentication.</span></span>

- **`--called-api-scopes <SCOPES>`**

  <span data-ttu-id="63312-473">为从 Web 应用调用 API 而请求的作用域。</span><span class="sxs-lookup"><span data-stu-id="63312-473">Scopes to request to call the API from the web app.</span></span> <span data-ttu-id="63312-474">仅适用于未指定 ASP.NET Core 主机的 `SingleOrg` 或 `IndividualB2C` 身份验证。</span><span class="sxs-lookup"><span data-stu-id="63312-474">Only applies to `SingleOrg` or `IndividualB2C` authentication without an ASP.NET Core host specified.</span></span> <span data-ttu-id="63312-475">默认值为 `user.read`。</span><span class="sxs-lookup"><span data-stu-id="63312-475">The default is `user.read`.</span></span>

***

### `web`

- **`--exclude-launch-settings`**

  <span data-ttu-id="63312-476">从生成的模板中排除 launchSettings.json。</span><span class="sxs-lookup"><span data-stu-id="63312-476">Excludes *launchSettings.json* from the generated template.</span></span>

- **`-f|--framework <FRAMEWORK>`**

  <span data-ttu-id="63312-477">指定目标[框架](../../standard/frameworks.md)。</span><span class="sxs-lookup"><span data-stu-id="63312-477">Specifies the [framework](../../standard/frameworks.md) to target.</span></span> <span data-ttu-id="63312-478">选项在 .NET Core 2.2 SDK 中不可用。</span><span class="sxs-lookup"><span data-stu-id="63312-478">Option not available in .NET Core 2.2 SDK.</span></span>

  <span data-ttu-id="63312-479">下表根据所使用的 SDK 版本号列出了默认值：</span><span class="sxs-lookup"><span data-stu-id="63312-479">The following table lists the default values according to the SDK version number you're using:</span></span>

  | <span data-ttu-id="63312-480">SDK 版本</span><span class="sxs-lookup"><span data-stu-id="63312-480">SDK version</span></span> | <span data-ttu-id="63312-481">默认值</span><span class="sxs-lookup"><span data-stu-id="63312-481">Default value</span></span>   |
  |-------------|-----------------|
  | <span data-ttu-id="63312-482">5.0</span><span class="sxs-lookup"><span data-stu-id="63312-482">5.0</span></span>         | `net5.0`        |
  | <span data-ttu-id="63312-483">3.1</span><span class="sxs-lookup"><span data-stu-id="63312-483">3.1</span></span>         | `netcoreapp3.1` |
  | <span data-ttu-id="63312-484">3.0</span><span class="sxs-lookup"><span data-stu-id="63312-484">3.0</span></span>         | `netcoreapp3.0` |
  | <span data-ttu-id="63312-485">2.1</span><span class="sxs-lookup"><span data-stu-id="63312-485">2.1</span></span>         | `netcoreapp2.1` |

- **`--no-restore`**

  <span data-ttu-id="63312-486">在项目创建期间不执行隐式还原。</span><span class="sxs-lookup"><span data-stu-id="63312-486">Doesn't execute an implicit restore during project creation.</span></span>

- **`--no-https`**

  <span data-ttu-id="63312-487">关闭 HTTPS。</span><span class="sxs-lookup"><span data-stu-id="63312-487">Turns off HTTPS.</span></span>

***

### <a name="mvc-webapp"></a><a name="web-options"></a> <span data-ttu-id="63312-488">`mvc`, `webapp`</span><span class="sxs-lookup"><span data-stu-id="63312-488">`mvc`, `webapp`</span></span>

- **`-au|--auth <AUTHENTICATION_TYPE>`**

  <span data-ttu-id="63312-489">要使用的身份验证类型。</span><span class="sxs-lookup"><span data-stu-id="63312-489">The type of authentication to use.</span></span> <span data-ttu-id="63312-490">可能的值为：</span><span class="sxs-lookup"><span data-stu-id="63312-490">The possible values are:</span></span>

  - <span data-ttu-id="63312-491">`None` - 不进行身份验证（默认）。</span><span class="sxs-lookup"><span data-stu-id="63312-491">`None` - No authentication (Default).</span></span>
  - <span data-ttu-id="63312-492">`Individual` - 个人身份验证。</span><span class="sxs-lookup"><span data-stu-id="63312-492">`Individual` - Individual authentication.</span></span>
  - <span data-ttu-id="63312-493">`IndividualB2C` - 使用 Azure AD B2C 进行个人身份验证。</span><span class="sxs-lookup"><span data-stu-id="63312-493">`IndividualB2C` - Individual authentication with Azure AD B2C.</span></span>
  - <span data-ttu-id="63312-494">`SingleOrg` - 对一个租户进行组织身份验证。</span><span class="sxs-lookup"><span data-stu-id="63312-494">`SingleOrg` - Organizational authentication for a single tenant.</span></span>
  - <span data-ttu-id="63312-495">`MultiOrg` - 对多个租户进行组织身份验证。</span><span class="sxs-lookup"><span data-stu-id="63312-495">`MultiOrg` - Organizational authentication for multiple tenants.</span></span>
  - <span data-ttu-id="63312-496">`Windows` - Windows 身份验证。</span><span class="sxs-lookup"><span data-stu-id="63312-496">`Windows` - Windows authentication.</span></span>

- **`--aad-b2c-instance <INSTANCE>`**

  <span data-ttu-id="63312-497">要连接到的 Azure Active Directory B2C 实例。</span><span class="sxs-lookup"><span data-stu-id="63312-497">The Azure Active Directory B2C instance to connect to.</span></span> <span data-ttu-id="63312-498">与 `IndividualB2C` 身份验证结合使用。</span><span class="sxs-lookup"><span data-stu-id="63312-498">Use with `IndividualB2C` authentication.</span></span> <span data-ttu-id="63312-499">默认值为 `https://login.microsoftonline.com/tfp/`。</span><span class="sxs-lookup"><span data-stu-id="63312-499">The default value is `https://login.microsoftonline.com/tfp/`.</span></span>

- **`-ssp|--susi-policy-id <ID>`**

  <span data-ttu-id="63312-500">此项目的登录和注册策略 ID。</span><span class="sxs-lookup"><span data-stu-id="63312-500">The sign-in and sign-up policy ID for this project.</span></span> <span data-ttu-id="63312-501">与 `IndividualB2C` 身份验证结合使用。</span><span class="sxs-lookup"><span data-stu-id="63312-501">Use with `IndividualB2C` authentication.</span></span>

- **`-rp|--reset-password-policy-id <ID>`**

  <span data-ttu-id="63312-502">此项目的重置密码策略 ID。</span><span class="sxs-lookup"><span data-stu-id="63312-502">The reset password policy ID for this project.</span></span> <span data-ttu-id="63312-503">与 `IndividualB2C` 身份验证结合使用。</span><span class="sxs-lookup"><span data-stu-id="63312-503">Use with `IndividualB2C` authentication.</span></span>

- **`-ep|--edit-profile-policy-id <ID>`**

  <span data-ttu-id="63312-504">此项目的编辑配置文件策略 ID。</span><span class="sxs-lookup"><span data-stu-id="63312-504">The edit profile policy ID for this project.</span></span> <span data-ttu-id="63312-505">与 `IndividualB2C` 身份验证结合使用。</span><span class="sxs-lookup"><span data-stu-id="63312-505">Use with `IndividualB2C` authentication.</span></span>

- **`--aad-instance <INSTANCE>`**

  <span data-ttu-id="63312-506">要连接到的 Azure Active Directory 实例。</span><span class="sxs-lookup"><span data-stu-id="63312-506">The Azure Active Directory instance to connect to.</span></span> <span data-ttu-id="63312-507">与 `SingleOrg` 或 `MultiOrg` 身份验证结合使用。</span><span class="sxs-lookup"><span data-stu-id="63312-507">Use with `SingleOrg` or `MultiOrg` authentication.</span></span> <span data-ttu-id="63312-508">默认值为 `https://login.microsoftonline.com/`。</span><span class="sxs-lookup"><span data-stu-id="63312-508">The default value is `https://login.microsoftonline.com/`.</span></span>

- **`--client-id <ID>`**

  <span data-ttu-id="63312-509">此项目的客户端 ID。</span><span class="sxs-lookup"><span data-stu-id="63312-509">The Client ID for this project.</span></span> <span data-ttu-id="63312-510">与 `IndividualB2C`、`SingleOrg` 或 `MultiOrg` 身份验证结合使用。</span><span class="sxs-lookup"><span data-stu-id="63312-510">Use with `IndividualB2C`, `SingleOrg`, or `MultiOrg` authentication.</span></span> <span data-ttu-id="63312-511">默认值为 `11111111-1111-1111-11111111111111111`。</span><span class="sxs-lookup"><span data-stu-id="63312-511">The default value is `11111111-1111-1111-11111111111111111`.</span></span>

- **`--domain <DOMAIN>`**

  <span data-ttu-id="63312-512">目录租户的域。</span><span class="sxs-lookup"><span data-stu-id="63312-512">The domain for the directory tenant.</span></span> <span data-ttu-id="63312-513">与 `SingleOrg` 或 `IndividualB2C` 身份验证结合使用。</span><span class="sxs-lookup"><span data-stu-id="63312-513">Use with `SingleOrg` or `IndividualB2C` authentication.</span></span> <span data-ttu-id="63312-514">默认值为 `qualified.domain.name`。</span><span class="sxs-lookup"><span data-stu-id="63312-514">The default value is `qualified.domain.name`.</span></span>

- **`--tenant-id <ID>`**

  <span data-ttu-id="63312-515">要连接到的目录的 TenantId ID。</span><span class="sxs-lookup"><span data-stu-id="63312-515">The TenantId ID of the directory to connect to.</span></span> <span data-ttu-id="63312-516">与 `SingleOrg` 身份验证结合使用。</span><span class="sxs-lookup"><span data-stu-id="63312-516">Use with `SingleOrg` authentication.</span></span> <span data-ttu-id="63312-517">默认值为 `22222222-2222-2222-2222-222222222222`。</span><span class="sxs-lookup"><span data-stu-id="63312-517">The default value is `22222222-2222-2222-2222-222222222222`.</span></span>

- **`--callback-path <PATH>`**

  <span data-ttu-id="63312-518">重定向 URI 的应用程序基路径中的请求路径。</span><span class="sxs-lookup"><span data-stu-id="63312-518">The request path within the application's base path of the redirect URI.</span></span> <span data-ttu-id="63312-519">与 `SingleOrg` 或 `IndividualB2C` 身份验证结合使用。</span><span class="sxs-lookup"><span data-stu-id="63312-519">Use with `SingleOrg` or `IndividualB2C` authentication.</span></span> <span data-ttu-id="63312-520">默认值为 `/signin-oidc`。</span><span class="sxs-lookup"><span data-stu-id="63312-520">The default value is `/signin-oidc`.</span></span>

- **`-r|--org-read-access`**

  <span data-ttu-id="63312-521">允许此应用程序对目录进行读取访问。</span><span class="sxs-lookup"><span data-stu-id="63312-521">Allows this application read-access to the directory.</span></span> <span data-ttu-id="63312-522">仅适用于 `SingleOrg` 或 `MultiOrg` 身份验证。</span><span class="sxs-lookup"><span data-stu-id="63312-522">Only applies to `SingleOrg` or `MultiOrg` authentication.</span></span>

- **`--exclude-launch-settings`**

  <span data-ttu-id="63312-523">从生成的模板中排除 launchSettings.json。</span><span class="sxs-lookup"><span data-stu-id="63312-523">Excludes *launchSettings.json* from the generated template.</span></span>

- **`--no-https`**

  <span data-ttu-id="63312-524">关闭 HTTPS。</span><span class="sxs-lookup"><span data-stu-id="63312-524">Turns off HTTPS.</span></span> <span data-ttu-id="63312-525">此选项仅适用于未使用 `Individual`、`IndividualB2C`、`SingleOrg` 和 `MultiOrg` 的情况。</span><span class="sxs-lookup"><span data-stu-id="63312-525">This option only applies if `Individual`, `IndividualB2C`, `SingleOrg`, or `MultiOrg` aren't being used.</span></span>

- **`-uld|--use-local-db`**

  <span data-ttu-id="63312-526">指定应使用 LocalDB，而不使用 SQLite。</span><span class="sxs-lookup"><span data-stu-id="63312-526">Specifies LocalDB should be used instead of SQLite.</span></span> <span data-ttu-id="63312-527">仅适用于 `Individual` 或 `IndividualB2C` 身份验证。</span><span class="sxs-lookup"><span data-stu-id="63312-527">Only applies to `Individual` or `IndividualB2C` authentication.</span></span>

- **`-f|--framework <FRAMEWORK>`**

  <span data-ttu-id="63312-528">指定目标[框架](../../standard/frameworks.md)。</span><span class="sxs-lookup"><span data-stu-id="63312-528">Specifies the [framework](../../standard/frameworks.md) to target.</span></span> <span data-ttu-id="63312-529">自 .NET Core 3.0 SDK 起可用的选项。</span><span class="sxs-lookup"><span data-stu-id="63312-529">Option available since .NET Core 3.0 SDK.</span></span>

  <span data-ttu-id="63312-530">下表根据所使用的 SDK 版本号列出了默认值：</span><span class="sxs-lookup"><span data-stu-id="63312-530">The following table lists the default values according to the SDK version number you're using:</span></span>

  | <span data-ttu-id="63312-531">SDK 版本</span><span class="sxs-lookup"><span data-stu-id="63312-531">SDK version</span></span> | <span data-ttu-id="63312-532">默认值</span><span class="sxs-lookup"><span data-stu-id="63312-532">Default value</span></span>   |
  |-------------|-----------------|
  | <span data-ttu-id="63312-533">5.0</span><span class="sxs-lookup"><span data-stu-id="63312-533">5.0</span></span>         | `net5.0`        |
  | <span data-ttu-id="63312-534">3.1</span><span class="sxs-lookup"><span data-stu-id="63312-534">3.1</span></span>         | `netcoreapp3.1` |
  | <span data-ttu-id="63312-535">3.0</span><span class="sxs-lookup"><span data-stu-id="63312-535">3.0</span></span>         | `netcoreapp3.0` |

- **`--no-restore`**

  <span data-ttu-id="63312-536">在项目创建期间不执行隐式还原。</span><span class="sxs-lookup"><span data-stu-id="63312-536">Doesn't execute an implicit restore during project creation.</span></span>

- **`--use-browserlink`**

  <span data-ttu-id="63312-537">在项目中添加 BrowserLink。</span><span class="sxs-lookup"><span data-stu-id="63312-537">Includes BrowserLink in the project.</span></span> <span data-ttu-id="63312-538">选项在 .NET Core 2.2 和 3.1 SDK 中不可用。</span><span class="sxs-lookup"><span data-stu-id="63312-538">Option not available in .NET Core 2.2 and 3.1 SDK.</span></span>

- **`-rrc|--razor-runtime-compilation`**

  <span data-ttu-id="63312-539">确定项目是否配置为在调试生成中使用 [Razor 运行时编译](/aspnet/core/mvc/views/view-compilation#runtime-compilation)。</span><span class="sxs-lookup"><span data-stu-id="63312-539">Determines if the project is configured to use [Razor runtime compilation](/aspnet/core/mvc/views/view-compilation#runtime-compilation) in Debug builds.</span></span> <span data-ttu-id="63312-540">自 .NET Core 3.1.201 SDK 起可用的选项。</span><span class="sxs-lookup"><span data-stu-id="63312-540">Option available since .NET Core 3.1.201 SDK.</span></span>

***

### <a name="angular-react"></a><a name="spa"></a> <span data-ttu-id="63312-541">`angular`, `react`</span><span class="sxs-lookup"><span data-stu-id="63312-541">`angular`, `react`</span></span>

- **`-au|--auth <AUTHENTICATION_TYPE>`**

  <span data-ttu-id="63312-542">要使用的身份验证类型。</span><span class="sxs-lookup"><span data-stu-id="63312-542">The type of authentication to use.</span></span> <span data-ttu-id="63312-543">自 .NET Core 3.0 SDK 起可用。</span><span class="sxs-lookup"><span data-stu-id="63312-543">Available since .NET Core 3.0 SDK.</span></span>
  
  <span data-ttu-id="63312-544">可能的值为：</span><span class="sxs-lookup"><span data-stu-id="63312-544">The possible values are:</span></span>

  - <span data-ttu-id="63312-545">`None` - 不进行身份验证（默认）。</span><span class="sxs-lookup"><span data-stu-id="63312-545">`None` - No authentication (Default).</span></span>
  - <span data-ttu-id="63312-546">`Individual` - 个人身份验证。</span><span class="sxs-lookup"><span data-stu-id="63312-546">`Individual` - Individual authentication.</span></span>

- **`--exclude-launch-settings`**

  <span data-ttu-id="63312-547">从生成的模板中排除 launchSettings.json。</span><span class="sxs-lookup"><span data-stu-id="63312-547">Excludes *launchSettings.json* from the generated template.</span></span>

- **`--no-restore`**

  <span data-ttu-id="63312-548">在项目创建期间不执行隐式还原。</span><span class="sxs-lookup"><span data-stu-id="63312-548">Doesn't execute an implicit restore during project creation.</span></span>

- **`--no-https`**

  <span data-ttu-id="63312-549">关闭 HTTPS。</span><span class="sxs-lookup"><span data-stu-id="63312-549">Turns off HTTPS.</span></span> <span data-ttu-id="63312-550">仅当身份验证为 `None` 时，此选项才适用。</span><span class="sxs-lookup"><span data-stu-id="63312-550">This option only applies if authentication is `None`.</span></span>

- **`-uld|--use-local-db`**

  <span data-ttu-id="63312-551">指定应使用 LocalDB，而不使用 SQLite。</span><span class="sxs-lookup"><span data-stu-id="63312-551">Specifies LocalDB should be used instead of SQLite.</span></span> <span data-ttu-id="63312-552">仅适用于 `Individual` 或 `IndividualB2C` 身份验证。</span><span class="sxs-lookup"><span data-stu-id="63312-552">Only applies to `Individual` or `IndividualB2C` authentication.</span></span> <span data-ttu-id="63312-553">自 .NET Core 3.0 SDK 起可用。</span><span class="sxs-lookup"><span data-stu-id="63312-553">Available since .NET Core 3.0 SDK.</span></span>

- **`-f|--framework <FRAMEWORK>`**

  <span data-ttu-id="63312-554">指定目标[框架](../../standard/frameworks.md)。</span><span class="sxs-lookup"><span data-stu-id="63312-554">Specifies the [framework](../../standard/frameworks.md) to target.</span></span> <span data-ttu-id="63312-555">选项在 .NET Core 2.2 SDK 中不可用。</span><span class="sxs-lookup"><span data-stu-id="63312-555">Option not available in .NET Core 2.2 SDK.</span></span>

  <span data-ttu-id="63312-556">下表根据所使用的 SDK 版本号列出了默认值：</span><span class="sxs-lookup"><span data-stu-id="63312-556">The following table lists the default values according to the SDK version number you're using:</span></span>

  | <span data-ttu-id="63312-557">SDK 版本</span><span class="sxs-lookup"><span data-stu-id="63312-557">SDK version</span></span> | <span data-ttu-id="63312-558">默认值</span><span class="sxs-lookup"><span data-stu-id="63312-558">Default value</span></span>   |
  |-------------|-----------------|
  | <span data-ttu-id="63312-559">5.0</span><span class="sxs-lookup"><span data-stu-id="63312-559">5.0</span></span>         | `net5.0`        |
  | <span data-ttu-id="63312-560">3.1</span><span class="sxs-lookup"><span data-stu-id="63312-560">3.1</span></span>         | `netcoreapp3.1` |
  | <span data-ttu-id="63312-561">3.0</span><span class="sxs-lookup"><span data-stu-id="63312-561">3.0</span></span>         | `netcoreapp3.0` |
  | <span data-ttu-id="63312-562">2.1</span><span class="sxs-lookup"><span data-stu-id="63312-562">2.1</span></span>         | `netcoreapp2.0` |

***

### `reactredux`

- **`--exclude-launch-settings`**

  <span data-ttu-id="63312-563">从生成的模板中排除 launchSettings.json。</span><span class="sxs-lookup"><span data-stu-id="63312-563">Excludes *launchSettings.json* from the generated template.</span></span>

- **`-f|--framework <FRAMEWORK>`**

  <span data-ttu-id="63312-564">指定目标[框架](../../standard/frameworks.md)。</span><span class="sxs-lookup"><span data-stu-id="63312-564">Specifies the [framework](../../standard/frameworks.md) to target.</span></span> <span data-ttu-id="63312-565">选项在 .NET Core 2.2 SDK 中不可用。</span><span class="sxs-lookup"><span data-stu-id="63312-565">Option not available in .NET Core 2.2 SDK.</span></span>

  <span data-ttu-id="63312-566">下表根据所使用的 SDK 版本号列出了默认值：</span><span class="sxs-lookup"><span data-stu-id="63312-566">The following table lists the default values according to the SDK version number you're using:</span></span>

  | <span data-ttu-id="63312-567">SDK 版本</span><span class="sxs-lookup"><span data-stu-id="63312-567">SDK version</span></span> | <span data-ttu-id="63312-568">默认值</span><span class="sxs-lookup"><span data-stu-id="63312-568">Default value</span></span>   |
  |-------------|-----------------|
  | <span data-ttu-id="63312-569">5.0</span><span class="sxs-lookup"><span data-stu-id="63312-569">5.0</span></span>         | `net5.0`        |
  | <span data-ttu-id="63312-570">3.1</span><span class="sxs-lookup"><span data-stu-id="63312-570">3.1</span></span>         | `netcoreapp3.1` |
  | <span data-ttu-id="63312-571">3.0</span><span class="sxs-lookup"><span data-stu-id="63312-571">3.0</span></span>         | `netcoreapp3.0` |
  | <span data-ttu-id="63312-572">2.1</span><span class="sxs-lookup"><span data-stu-id="63312-572">2.1</span></span>         | `netcoreapp2.0` |

- **`--no-restore`**

  <span data-ttu-id="63312-573">在项目创建期间不执行隐式还原。</span><span class="sxs-lookup"><span data-stu-id="63312-573">Doesn't execute an implicit restore during project creation.</span></span>

- **`--no-https`**

  <span data-ttu-id="63312-574">关闭 HTTPS。</span><span class="sxs-lookup"><span data-stu-id="63312-574">Turns off HTTPS.</span></span>

***

### `razorclasslib`

- **`--no-restore`**

  <span data-ttu-id="63312-575">在项目创建期间不执行隐式还原。</span><span class="sxs-lookup"><span data-stu-id="63312-575">Doesn't execute an implicit restore during project creation.</span></span>

- **`-s|--support-pages-and-views`**

  <span data-ttu-id="63312-576">除了将组件添加到此库以外，还支持添加传统的 Razor 页面和视图。</span><span class="sxs-lookup"><span data-stu-id="63312-576">Supports adding traditional Razor pages and Views in addition to components to this library.</span></span> <span data-ttu-id="63312-577">自 .NET Core 3.0 SDK 起可用。</span><span class="sxs-lookup"><span data-stu-id="63312-577">Available since .NET Core 3.0 SDK.</span></span>

***
  
### `webapi`

- **`-au|--auth <AUTHENTICATION_TYPE>`**

  <span data-ttu-id="63312-578">要使用的身份验证类型。</span><span class="sxs-lookup"><span data-stu-id="63312-578">The type of authentication to use.</span></span> <span data-ttu-id="63312-579">可能的值为：</span><span class="sxs-lookup"><span data-stu-id="63312-579">The possible values are:</span></span>

  - <span data-ttu-id="63312-580">`None` - 不进行身份验证（默认）。</span><span class="sxs-lookup"><span data-stu-id="63312-580">`None` - No authentication (Default).</span></span>
  - <span data-ttu-id="63312-581">`IndividualB2C` - 使用 Azure AD B2C 进行个人身份验证。</span><span class="sxs-lookup"><span data-stu-id="63312-581">`IndividualB2C` - Individual authentication with Azure AD B2C.</span></span>
  - <span data-ttu-id="63312-582">`SingleOrg` - 对一个租户进行组织身份验证。</span><span class="sxs-lookup"><span data-stu-id="63312-582">`SingleOrg` - Organizational authentication for a single tenant.</span></span>
  - <span data-ttu-id="63312-583">`Windows` - Windows 身份验证。</span><span class="sxs-lookup"><span data-stu-id="63312-583">`Windows` - Windows authentication.</span></span>

- **`--aad-b2c-instance <INSTANCE>`**

  <span data-ttu-id="63312-584">要连接到的 Azure Active Directory B2C 实例。</span><span class="sxs-lookup"><span data-stu-id="63312-584">The Azure Active Directory B2C instance to connect to.</span></span> <span data-ttu-id="63312-585">与 `IndividualB2C` 身份验证结合使用。</span><span class="sxs-lookup"><span data-stu-id="63312-585">Use with `IndividualB2C` authentication.</span></span> <span data-ttu-id="63312-586">默认值为 `https://login.microsoftonline.com/tfp/`。</span><span class="sxs-lookup"><span data-stu-id="63312-586">The default value is `https://login.microsoftonline.com/tfp/`.</span></span>

- **`-ssp|--susi-policy-id <ID>`**

  <span data-ttu-id="63312-587">此项目的登录和注册策略 ID。</span><span class="sxs-lookup"><span data-stu-id="63312-587">The sign-in and sign-up policy ID for this project.</span></span> <span data-ttu-id="63312-588">与 `IndividualB2C` 身份验证结合使用。</span><span class="sxs-lookup"><span data-stu-id="63312-588">Use with `IndividualB2C` authentication.</span></span>

- **`--aad-instance <INSTANCE>`**

  <span data-ttu-id="63312-589">要连接到的 Azure Active Directory 实例。</span><span class="sxs-lookup"><span data-stu-id="63312-589">The Azure Active Directory instance to connect to.</span></span> <span data-ttu-id="63312-590">与 `SingleOrg` 身份验证结合使用。</span><span class="sxs-lookup"><span data-stu-id="63312-590">Use with `SingleOrg` authentication.</span></span> <span data-ttu-id="63312-591">默认值为 `https://login.microsoftonline.com/`。</span><span class="sxs-lookup"><span data-stu-id="63312-591">The default value is `https://login.microsoftonline.com/`.</span></span>

- **`--client-id <ID>`**

  <span data-ttu-id="63312-592">此项目的客户端 ID。</span><span class="sxs-lookup"><span data-stu-id="63312-592">The Client ID for this project.</span></span> <span data-ttu-id="63312-593">与 `IndividualB2C` 或 `SingleOrg` 身份验证结合使用。</span><span class="sxs-lookup"><span data-stu-id="63312-593">Use with `IndividualB2C` or `SingleOrg` authentication.</span></span> <span data-ttu-id="63312-594">默认值为 `11111111-1111-1111-11111111111111111`。</span><span class="sxs-lookup"><span data-stu-id="63312-594">The default value is `11111111-1111-1111-11111111111111111`.</span></span>

- **`--domain <DOMAIN>`**

  <span data-ttu-id="63312-595">目录租户的域。</span><span class="sxs-lookup"><span data-stu-id="63312-595">The domain for the directory tenant.</span></span> <span data-ttu-id="63312-596">与 `IndividualB2C` 或 `SingleOrg` 身份验证结合使用。</span><span class="sxs-lookup"><span data-stu-id="63312-596">Use with `IndividualB2C` or `SingleOrg` authentication.</span></span> <span data-ttu-id="63312-597">默认值为 `qualified.domain.name`。</span><span class="sxs-lookup"><span data-stu-id="63312-597">The default value is `qualified.domain.name`.</span></span>

- **`--tenant-id <ID>`**

  <span data-ttu-id="63312-598">要连接到的目录的 TenantId ID。</span><span class="sxs-lookup"><span data-stu-id="63312-598">The TenantId ID of the directory to connect to.</span></span> <span data-ttu-id="63312-599">与 `SingleOrg` 身份验证结合使用。</span><span class="sxs-lookup"><span data-stu-id="63312-599">Use with `SingleOrg` authentication.</span></span> <span data-ttu-id="63312-600">默认值为 `22222222-2222-2222-2222-222222222222`。</span><span class="sxs-lookup"><span data-stu-id="63312-600">The default value is `22222222-2222-2222-2222-222222222222`.</span></span>

- **`-r|--org-read-access`**

  <span data-ttu-id="63312-601">允许此应用程序对目录进行读取访问。</span><span class="sxs-lookup"><span data-stu-id="63312-601">Allows this application read-access to the directory.</span></span> <span data-ttu-id="63312-602">仅适用于 `SingleOrg` 身份验证。</span><span class="sxs-lookup"><span data-stu-id="63312-602">Only applies to `SingleOrg` authentication.</span></span>

- **`--exclude-launch-settings`**

  <span data-ttu-id="63312-603">从生成的模板中排除 launchSettings.json。</span><span class="sxs-lookup"><span data-stu-id="63312-603">Excludes *launchSettings.json* from the generated template.</span></span>

- **`--no-https`**

  <span data-ttu-id="63312-604">关闭 HTTPS。</span><span class="sxs-lookup"><span data-stu-id="63312-604">Turns off HTTPS.</span></span> <span data-ttu-id="63312-605">`app.UseHsts` 和 `app.UseHttpsRedirection` 未添加到 `Startup.Configure` 中。</span><span class="sxs-lookup"><span data-stu-id="63312-605">`app.UseHsts` and `app.UseHttpsRedirection` aren't added to `Startup.Configure`.</span></span> <span data-ttu-id="63312-606">此选项仅适用于 `IndividualB2C` 或 `SingleOrg` 未用于身份验证的情况。</span><span class="sxs-lookup"><span data-stu-id="63312-606">This option only applies if `IndividualB2C` or `SingleOrg` aren't being used for authentication.</span></span>

- **`-uld|--use-local-db`**

  <span data-ttu-id="63312-607">指定应使用 LocalDB，而不使用 SQLite。</span><span class="sxs-lookup"><span data-stu-id="63312-607">Specifies LocalDB should be used instead of SQLite.</span></span> <span data-ttu-id="63312-608">仅适用于 `IndividualB2C` 身份验证。</span><span class="sxs-lookup"><span data-stu-id="63312-608">Only applies to `IndividualB2C` authentication.</span></span>

- **`-f|--framework <FRAMEWORK>`**

  <span data-ttu-id="63312-609">指定目标[框架](../../standard/frameworks.md)。</span><span class="sxs-lookup"><span data-stu-id="63312-609">Specifies the [framework](../../standard/frameworks.md) to target.</span></span> <span data-ttu-id="63312-610">选项在 .NET Core 2.2 SDK 中不可用。</span><span class="sxs-lookup"><span data-stu-id="63312-610">Option not available in .NET Core 2.2 SDK.</span></span>

  <span data-ttu-id="63312-611">下表根据所使用的 SDK 版本号列出了默认值：</span><span class="sxs-lookup"><span data-stu-id="63312-611">The following table lists the default values according to the SDK version number you're using:</span></span>

  | <span data-ttu-id="63312-612">SDK 版本</span><span class="sxs-lookup"><span data-stu-id="63312-612">SDK version</span></span> | <span data-ttu-id="63312-613">默认值</span><span class="sxs-lookup"><span data-stu-id="63312-613">Default value</span></span>   |
  |-------------|-----------------|
  | <span data-ttu-id="63312-614">5.0</span><span class="sxs-lookup"><span data-stu-id="63312-614">5.0</span></span>         | `net5.0`        |
  | <span data-ttu-id="63312-615">3.1</span><span class="sxs-lookup"><span data-stu-id="63312-615">3.1</span></span>         | `netcoreapp3.1` |
  | <span data-ttu-id="63312-616">3.0</span><span class="sxs-lookup"><span data-stu-id="63312-616">3.0</span></span>         | `netcoreapp3.0` |
  | <span data-ttu-id="63312-617">2.1</span><span class="sxs-lookup"><span data-stu-id="63312-617">2.1</span></span>         | `netcoreapp2.1` |

- **`--no-restore`**

  <span data-ttu-id="63312-618">在项目创建期间不执行隐式还原。</span><span class="sxs-lookup"><span data-stu-id="63312-618">Doesn't execute an implicit restore during project creation.</span></span>

***

### `globaljson`

- **`--sdk-version <VERSION_NUMBER>`**

  <span data-ttu-id="63312-619">指定要在 global.json 文件中使用的 .NET SDK 版本。</span><span class="sxs-lookup"><span data-stu-id="63312-619">Specifies the version of the .NET SDK to use in the *global.json* file.</span></span>

***

## <a name="examples"></a><span data-ttu-id="63312-620">示例</span><span class="sxs-lookup"><span data-stu-id="63312-620">Examples</span></span>

- <span data-ttu-id="63312-621">通过指定模板名称，创建 C# 控制台应用程序项目：</span><span class="sxs-lookup"><span data-stu-id="63312-621">Create a C# console application project by specifying the template name:</span></span>

  ```dotnetcli
  dotnet new "Console Application"
  ```

- <span data-ttu-id="63312-622">在当前目录中创建 F# 控制台应用程序项目：</span><span class="sxs-lookup"><span data-stu-id="63312-622">Create an F# console application project in the current directory:</span></span>

  ```dotnetcli
  dotnet new console -lang "F#"
  ```

- <span data-ttu-id="63312-623">在指定的目录中创建 .NET Standard 类库项目：</span><span class="sxs-lookup"><span data-stu-id="63312-623">Create a .NET Standard class library project in the specified directory:</span></span>

  ```dotnetcli
  dotnet new classlib -lang VB -o MyLibrary
  ```

- <span data-ttu-id="63312-624">在当前目录中新建没有设置身份验证的 ASP.NET Core C# MVC 项目：</span><span class="sxs-lookup"><span data-stu-id="63312-624">Create a new ASP.NET Core C# MVC project in the current directory with no authentication:</span></span>

  ```dotnetcli
  dotnet new mvc -au None
  ```

- <span data-ttu-id="63312-625">创建新的 xUnit 项目：</span><span class="sxs-lookup"><span data-stu-id="63312-625">Create a new xUnit project:</span></span>

  ```dotnetcli
  dotnet new xunit
  ```

- <span data-ttu-id="63312-626">列出可用于单页应用程序 (SPA) 模板的所有模板：</span><span class="sxs-lookup"><span data-stu-id="63312-626">List all templates available for Single Page Application (SPA) templates:</span></span>

  ```dotnetcli
  dotnet new spa -l
  ```

- <span data-ttu-id="63312-627">列出与“we”子字符串匹配的所有模板。</span><span class="sxs-lookup"><span data-stu-id="63312-627">List all templates matching the *we* substring.</span></span> <span data-ttu-id="63312-628">找不到完全匹配，因此子字符串匹配针对短名称和名称列运行。</span><span class="sxs-lookup"><span data-stu-id="63312-628">No exact match is found, so substring matching runs against both the short name and name columns.</span></span>

  ```dotnetcli
  dotnet new we -l
  ```

- <span data-ttu-id="63312-629">尝试调用与 ng 匹配的模板。</span><span class="sxs-lookup"><span data-stu-id="63312-629">Attempt to invoke the template matching *ng*.</span></span> <span data-ttu-id="63312-630">如果无法确定单个匹配项，请列出部分匹配项的模板。</span><span class="sxs-lookup"><span data-stu-id="63312-630">If a single match can't be determined, list the templates that are partial matches.</span></span>

  ```dotnetcli
  dotnet new ng
  ```

- <span data-ttu-id="63312-631">安装 ASP.NET Core 的 SPA 模板 2.0 版：</span><span class="sxs-lookup"><span data-stu-id="63312-631">Install version 2.0 of the SPA templates for ASP.NET Core:</span></span>

  ```dotnetcli
  dotnet new -i Microsoft.DotNet.Web.Spa.ProjectTemplates::2.0.0
  ```

- <span data-ttu-id="63312-632">列出已安装的模板及其详细信息，包括如何卸载它们：</span><span class="sxs-lookup"><span data-stu-id="63312-632">List the installed templates and details about them, including how to uninstall them:</span></span>

  ```dotnetcli
  dotnet new -u
  ```

- <span data-ttu-id="63312-633">在当前目录中创建 global.json，将 SDK 版本设置为 3.1.101：</span><span class="sxs-lookup"><span data-stu-id="63312-633">Create a *global.json* in the current directory setting the SDK version to 3.1.101:</span></span>

  ```dotnetcli
  dotnet new globaljson --sdk-version 3.1.101
  ```

## <a name="see-also"></a><span data-ttu-id="63312-634">请参阅</span><span class="sxs-lookup"><span data-stu-id="63312-634">See also</span></span>

- [<span data-ttu-id="63312-635">dotnet new 自定义模板</span><span class="sxs-lookup"><span data-stu-id="63312-635">Custom templates for dotnet new</span></span>](custom-templates.md)
- [<span data-ttu-id="63312-636">创建 dotnet new 自定义模板</span><span class="sxs-lookup"><span data-stu-id="63312-636">Create a custom template for dotnet new</span></span>](../tutorials/cli-templates-create-item-template.md)
- [<span data-ttu-id="63312-637">dotnet/dotnet-template-samples GitHub 存储库</span><span class="sxs-lookup"><span data-stu-id="63312-637">dotnet/dotnet-template-samples GitHub repo</span></span>](https://github.com/dotnet/dotnet-template-samples)
- [<span data-ttu-id="63312-638">dotnet new 可用模板</span><span class="sxs-lookup"><span data-stu-id="63312-638">Available templates for dotnet new</span></span>](https://github.com/dotnet/templating/wiki/Available-templates-for-dotnet-new)
