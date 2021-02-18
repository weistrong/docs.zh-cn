---
title: Microsoft.NET.Sdk.Desktop 的 MSBuild 属性
description: 有关 .NET 桌面 SDK（其中包括 WPF 和 WinForms）可以理解的 MSBuild 属性和项的参考。
ms.date: 02/04/2021
ms.topic: reference
author: adegeo
ms.author: adegeo
ms.custom: updateeachrelease
no-loc:
- App.xaml
- Application.xaml
- ApplicationDefinition
- Page
- EmbeddedResource
- Compile
- None
ms.openlocfilehash: 6d1903558dd03776a72eb6ee56ddae09fb66615b
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100488202"
---
# <a name="msbuild-reference-for-net-desktop-sdk-projects"></a><span data-ttu-id="cb415-103">.NET 桌面 SDK 项目的 MSBuild 参考</span><span class="sxs-lookup"><span data-stu-id="cb415-103">MSBuild reference for .NET Desktop SDK projects</span></span>

<span data-ttu-id="cb415-104">此页是有关用于通过 .NET 桌面 SDK 配置 Windows 窗体 (WinForms) 和 Windows Presentation Foundation (WPF) 项目的 MSBuild 属性和项的参考。</span><span class="sxs-lookup"><span data-stu-id="cb415-104">This page is a reference for the MSBuild properties and items that you use to configure Windows Forms (WinForms) and Windows Presentation Foundation (WPF) projects with the .NET Desktop SDK.</span></span>

> [!NOTE]
> <span data-ttu-id="cb415-105">本文介绍了 .NET SDK 的 MSBuild 属性的子集，因为它与桌面应用相关。</span><span class="sxs-lookup"><span data-stu-id="cb415-105">This article documents a subset of the MSBuild properties for the .NET SDK as it relates to desktop apps.</span></span> <span data-ttu-id="cb415-106">有关常用 .NET SDK 特定 MSBuild 属性的列表，请参见 [.NET SDK 项目的 MSBuild 参考](msbuild-props.md)。</span><span class="sxs-lookup"><span data-stu-id="cb415-106">For a list of common .NET SDK-specific MSBuild properties, see [MSBuild reference for .NET SDK projects](msbuild-props.md).</span></span> <span data-ttu-id="cb415-107">有关通用 MSBuild 属性的列表，请参阅[通用 MSBuild 属性](/visualstudio/msbuild/common-msbuild-project-properties)。</span><span class="sxs-lookup"><span data-stu-id="cb415-107">For a list of common MSBuild properties, see [Common MSBuild properties](/visualstudio/msbuild/common-msbuild-project-properties).</span></span>

## <a name="enable-net-desktop-sdk"></a><span data-ttu-id="cb415-108">启用 .NET 桌面 SDK</span><span class="sxs-lookup"><span data-stu-id="cb415-108">Enable .NET Desktop SDK</span></span>

<span data-ttu-id="cb415-109">若要使用 WinForms 或 WPF，请配置你的项目文件。</span><span class="sxs-lookup"><span data-stu-id="cb415-109">To use WinForms or WPF, configure your project file.</span></span>

### <a name="net-50"></a><span data-ttu-id="cb415-110">.NET 5.0</span><span class="sxs-lookup"><span data-stu-id="cb415-110">.NET 5.0</span></span>

<span data-ttu-id="cb415-111">在 WinForms 或 WPF 项目的项目文件中指定以下设置：</span><span class="sxs-lookup"><span data-stu-id="cb415-111">Specify the following settings in the project file of your WinForms or WPF project:</span></span>

- <span data-ttu-id="cb415-112">将 .NET SDK `Microsoft.NET.Sdk` 作为目标。</span><span class="sxs-lookup"><span data-stu-id="cb415-112">Target the .NET SDK `Microsoft.NET.Sdk`.</span></span> <span data-ttu-id="cb415-113">有关详细信息，请参阅[项目文件](overview.md#project-files)。</span><span class="sxs-lookup"><span data-stu-id="cb415-113">For more information, see [Project files](overview.md#project-files).</span></span>
- <span data-ttu-id="cb415-114">将 [`TargetFramework`](msbuild-props.md#targetframework) 设置为 `net5.0-windows`。</span><span class="sxs-lookup"><span data-stu-id="cb415-114">Set [`TargetFramework`](msbuild-props.md#targetframework) to `net5.0-windows`.</span></span>
- <span data-ttu-id="cb415-115">添加 UI 框架属性（或两者，如果必要）：</span><span class="sxs-lookup"><span data-stu-id="cb415-115">Add a UI framework property (or both, if necessary):</span></span>
  - <span data-ttu-id="cb415-116">将 [`UseWPF`](#usewpf) 设置为 `true` 以导入并使用 WPF。</span><span class="sxs-lookup"><span data-stu-id="cb415-116">Set [`UseWPF`](#usewpf) to `true` to import and use WPF.</span></span>
  - <span data-ttu-id="cb415-117">将 [`UseWindowsForms`](#usewindowsforms) 设置为 `true` 以导入并使用 WinForms。</span><span class="sxs-lookup"><span data-stu-id="cb415-117">Set [`UseWindowsForms`](#usewindowsforms) to `true` to import and use WinForms.</span></span>
- <span data-ttu-id="cb415-118">（可选）将 `OutputType` 设置为 `WinExe`。</span><span class="sxs-lookup"><span data-stu-id="cb415-118">(Optional) Set `OutputType` to `WinExe`.</span></span> <span data-ttu-id="cb415-119">这将生成应用，而不是库。</span><span class="sxs-lookup"><span data-stu-id="cb415-119">This produces an app as opposed to a library.</span></span> <span data-ttu-id="cb415-120">若要生成库，请省略此属性。</span><span class="sxs-lookup"><span data-stu-id="cb415-120">To produce a library, omit this property.</span></span>

```xml
<Project Sdk="Microsoft.NET.Sdk">

  <PropertyGroup>
    <OutputType>WinExe</OutputType>
    <TargetFramework>net5.0-windows</TargetFramework>

    <UseWPF>true</UseWPF>
    <!-- and/or -->
    <UseWindowsForms>true</UseWindowsForms>
  </PropertyGroup>

</Project>
```

### <a name="net-core-31"></a><span data-ttu-id="cb415-121">.NET Core 3.1</span><span class="sxs-lookup"><span data-stu-id="cb415-121">.NET Core 3.1</span></span>

<span data-ttu-id="cb415-122">在 WinForms 或 WPF 项目的项目文件中指定以下设置：</span><span class="sxs-lookup"><span data-stu-id="cb415-122">Specify the following settings in the project file of your WinForms or WPF project:</span></span>

- <span data-ttu-id="cb415-123">将 .NET SDK `Microsoft.NET.Sdk.WindowsDesktop` 作为目标。</span><span class="sxs-lookup"><span data-stu-id="cb415-123">Target the .NET SDK `Microsoft.NET.Sdk.WindowsDesktop`.</span></span> <span data-ttu-id="cb415-124">有关详细信息，请参阅[项目文件](overview.md#project-files)。</span><span class="sxs-lookup"><span data-stu-id="cb415-124">For more information, see [Project files](overview.md#project-files).</span></span>
- <span data-ttu-id="cb415-125">将 [`TargetFramework`](msbuild-props.md#targetframework) 设置为 `netcoreapp3.1`。</span><span class="sxs-lookup"><span data-stu-id="cb415-125">Set [`TargetFramework`](msbuild-props.md#targetframework) to `netcoreapp3.1`.</span></span>
- <span data-ttu-id="cb415-126">添加 UI 框架属性（或两者，如果必要）：</span><span class="sxs-lookup"><span data-stu-id="cb415-126">Add a UI framework property (or both, if necessary):</span></span>
  - <span data-ttu-id="cb415-127">将 [`UseWPF`](#usewpf) 设置为 `true` 以导入并使用 WPF。</span><span class="sxs-lookup"><span data-stu-id="cb415-127">Set [`UseWPF`](#usewpf) to `true` to import and use WPF.</span></span>
  - <span data-ttu-id="cb415-128">将 [`UseWindowsForms`](#usewindowsforms) 设置为 `true` 以导入并使用 WinForms。</span><span class="sxs-lookup"><span data-stu-id="cb415-128">Set [`UseWindowsForms`](#usewindowsforms) to `true` to import and use WinForms.</span></span>
- <span data-ttu-id="cb415-129">（可选）将 `OutputType` 设置为 `WinExe`。</span><span class="sxs-lookup"><span data-stu-id="cb415-129">(Optional) Set `OutputType` to `WinExe`.</span></span> <span data-ttu-id="cb415-130">这将生成应用，而不是库。</span><span class="sxs-lookup"><span data-stu-id="cb415-130">This produces an app as opposed to a library.</span></span> <span data-ttu-id="cb415-131">若要生成库，请省略此属性。</span><span class="sxs-lookup"><span data-stu-id="cb415-131">To produce a library, omit this property.</span></span>

```xml
<Project Sdk="Microsoft.NET.Sdk.WindowsDesktop">

  <PropertyGroup>
    <OutputType>WinExe</OutputType>
    <TargetFramework>netcoreapp3.1</TargetFramework>

    <UseWPF>true</UseWPF>
    <!-- and/or -->
    <UseWindowsForms>true</UseWindowsForms>
  </PropertyGroup>

</Project>
```

## <a name="wpf-default-includes-and-excludes"></a><span data-ttu-id="cb415-132">WPF 默认包含和排除的内容</span><span class="sxs-lookup"><span data-stu-id="cb415-132">WPF default includes and excludes</span></span>

<span data-ttu-id="cb415-133">SDK 项目定义一组规则，用于在项目中隐式包含或排除文件。</span><span class="sxs-lookup"><span data-stu-id="cb415-133">SDK projects define a set of rules to implicitly include or exclude files from the project.</span></span> <span data-ttu-id="cb415-134">这些规则还自动设置文件的生成操作。</span><span class="sxs-lookup"><span data-stu-id="cb415-134">These rules also automatically set the file's build action.</span></span> <span data-ttu-id="cb415-135">这与较旧的非 SDK .NET Framework 项目不同，后者没有默认的包含或排除规则。</span><span class="sxs-lookup"><span data-stu-id="cb415-135">This is unlike the older non-SDK .NET Framework projects, which have no default include or exclude rules.</span></span> <span data-ttu-id="cb415-136">.NET Framework 项目需要你显式声明要将哪些文件包含在项目中。</span><span class="sxs-lookup"><span data-stu-id="cb415-136">.NET Framework projects require you to explicitly declare which files to include in the project.</span></span>

<span data-ttu-id="cb415-137">.NET 项目文件包括一组[标准规则](overview.md#default-includes-and-excludes)，用于自动处理文件。</span><span class="sxs-lookup"><span data-stu-id="cb415-137">.NET project files include a [standard set of rules](overview.md#default-includes-and-excludes) for automatically processing files.</span></span> <span data-ttu-id="cb415-138">WPF 项目添加了更多规则。</span><span class="sxs-lookup"><span data-stu-id="cb415-138">WPF projects add additional rules.</span></span>

<span data-ttu-id="cb415-139">下表显示当 [`UseWPF`](#usewpf) 项目属性设置为 `true` 时在 .NET 桌面 SDK 中包含和排除哪些元素和 [glob](https://en.wikipedia.org/wiki/Glob_(programming))：</span><span class="sxs-lookup"><span data-stu-id="cb415-139">The following table shows which elements and [globs](https://en.wikipedia.org/wiki/Glob_(programming)) are included and excluded in the .NET Desktop SDK when the [`UseWPF`](#usewpf) project property is set to `true`:</span></span>

| <span data-ttu-id="cb415-140">元素</span><span class="sxs-lookup"><span data-stu-id="cb415-140">Element</span></span>               | <span data-ttu-id="cb415-141">包含 glob</span><span class="sxs-lookup"><span data-stu-id="cb415-141">Include glob</span></span>                 | <span data-ttu-id="cb415-142">排除 glob</span><span class="sxs-lookup"><span data-stu-id="cb415-142">Exclude glob</span></span>                                                                                           | <span data-ttu-id="cb415-143">删除 glob</span><span class="sxs-lookup"><span data-stu-id="cb415-143">Remove glob</span></span>  |
|-----------------------|------------------------------|--------------------------------------------------------------------|--------------|
| ApplicationDefinition | <span data-ttu-id="cb415-144">App.xaml 或 Application.xaml</span><span class="sxs-lookup"><span data-stu-id="cb415-144">App.xaml or Application.xaml</span></span> | <span data-ttu-id="cb415-145">不可用</span><span class="sxs-lookup"><span data-stu-id="cb415-145">N/A</span></span>                                                                | <span data-ttu-id="cb415-146">不可用</span><span class="sxs-lookup"><span data-stu-id="cb415-146">N/A</span></span>          |
| Page                  | <span data-ttu-id="cb415-147">\*\*/\*.xaml</span><span class="sxs-lookup"><span data-stu-id="cb415-147">\*\*/\*.xaml</span></span>                 | <span data-ttu-id="cb415-148">\*\*/\*.user; \*\*/\*.\*proj; \*\*/\*.sln; \*\*/\*.vssscc</span><span class="sxs-lookup"><span data-stu-id="cb415-148">\*\*/\*.user; \*\*/\*.\*proj; \*\*/\*.sln; \*\*/\*.vssscc</span></span><br><span data-ttu-id="cb415-149">*ApplicationDefinition* 定义的任何 XAML</span><span class="sxs-lookup"><span data-stu-id="cb415-149">Any XAML defined by *ApplicationDefinition*</span></span> | <span data-ttu-id="cb415-150">不可用</span><span class="sxs-lookup"><span data-stu-id="cb415-150">N/A</span></span>          |
| None                  | <span data-ttu-id="cb415-151">不可用</span><span class="sxs-lookup"><span data-stu-id="cb415-151">N/A</span></span>                          | <span data-ttu-id="cb415-152">不可用</span><span class="sxs-lookup"><span data-stu-id="cb415-152">N/A</span></span>                                                                | <span data-ttu-id="cb415-153">\*\*/\*.xaml</span><span class="sxs-lookup"><span data-stu-id="cb415-153">\*\*/\*.xaml</span></span> |

<span data-ttu-id="cb415-154">下面是所有项目类型的默认包含和排除设置。</span><span class="sxs-lookup"><span data-stu-id="cb415-154">Here are the default include and exclude settings for all project types.</span></span> <span data-ttu-id="cb415-155">有关详细信息，请参阅[默认的包括和排除](overview.md#default-includes-and-excludes)。</span><span class="sxs-lookup"><span data-stu-id="cb415-155">For more information, see [Default includes and excludes](overview.md#default-includes-and-excludes).</span></span>

| <span data-ttu-id="cb415-156">元素</span><span class="sxs-lookup"><span data-stu-id="cb415-156">Element</span></span>           | <span data-ttu-id="cb415-157">包含 glob</span><span class="sxs-lookup"><span data-stu-id="cb415-157">Include glob</span></span>                              | <span data-ttu-id="cb415-158">排除 glob</span><span class="sxs-lookup"><span data-stu-id="cb415-158">Exclude glob</span></span>                                                  | <span data-ttu-id="cb415-159">删除 glob</span><span class="sxs-lookup"><span data-stu-id="cb415-159">Remove glob</span></span>              |
|-------------------|-------------------------------------------|---------------------------------------------------------------|--------------------------|
| Compile           | <span data-ttu-id="cb415-160">\*\*/\*.cs；\*\*/\*.vb（或其他语言扩展名）</span><span class="sxs-lookup"><span data-stu-id="cb415-160">\*\*/\*.cs; \*\*/\*.vb (or other language extensions)</span></span> | <span data-ttu-id="cb415-161">\*\*/\*.user;  \*\*/\*.\*proj;  \*\*/\*.sln;  \*\*/\*.vssscc</span><span class="sxs-lookup"><span data-stu-id="cb415-161">\*\*/\*.user;  \*\*/\*.\*proj;  \*\*/\*.sln;  \*\*/\*.vssscc</span></span>  | <span data-ttu-id="cb415-162">不可用</span><span class="sxs-lookup"><span data-stu-id="cb415-162">N/A</span></span>          |
| EmbeddedResource  | <span data-ttu-id="cb415-163">\*\*/\*.resx</span><span class="sxs-lookup"><span data-stu-id="cb415-163">\*\*/\*.resx</span></span>                              | <span data-ttu-id="cb415-164">\*\*/\*.user; \*\*/\*.\*proj; \*\*/\*.sln; \*\*/\*.vssscc</span><span class="sxs-lookup"><span data-stu-id="cb415-164">\*\*/\*.user; \*\*/\*.\*proj; \*\*/\*.sln; \*\*/\*.vssscc</span></span>     | <span data-ttu-id="cb415-165">不可用</span><span class="sxs-lookup"><span data-stu-id="cb415-165">N/A</span></span>                      |
| None              | \*\*/\*                                   | <span data-ttu-id="cb415-166">\*\*/\*.user; \*\*/\*.\*proj; \*\*/\*.sln; \*\*/\*.vssscc</span><span class="sxs-lookup"><span data-stu-id="cb415-166">\*\*/\*.user; \*\*/\*.\*proj; \*\*/\*.sln; \*\*/\*.vssscc</span></span>     | <span data-ttu-id="cb415-167">\*\*/\*.cs; \*\*/\*.resx</span><span class="sxs-lookup"><span data-stu-id="cb415-167">\*\*/\*.cs; \*\*/\*.resx</span></span> |

### <a name="errors-related-to-duplicate-items"></a><span data-ttu-id="cb415-168">与“重复”项相关的错误</span><span class="sxs-lookup"><span data-stu-id="cb415-168">Errors related to "duplicate" items</span></span>

<span data-ttu-id="cb415-169">如果已将文件显式添加到项目，或让 XAML glob 自动将文件包含在项目中，则可能会收到以下错误之一：</span><span class="sxs-lookup"><span data-stu-id="cb415-169">If you explicitly added files to your project, or have XAML globs to automatically include files in your project, you might get one of the following errors:</span></span>

* <span data-ttu-id="cb415-170">包含重复的“ApplicationDefinition”项。</span><span class="sxs-lookup"><span data-stu-id="cb415-170">Duplicate 'ApplicationDefinition' items were included.</span></span>
* <span data-ttu-id="cb415-171">包含重复的“Page”项。</span><span class="sxs-lookup"><span data-stu-id="cb415-171">Duplicate 'Page' items were included.</span></span>

<span data-ttu-id="cb415-172">这些错误是隐式包含 glob 与你的设置冲突的结果。</span><span class="sxs-lookup"><span data-stu-id="cb415-172">These errors are a result of the implicit *Include* globs conflicting with your settings.</span></span> <span data-ttu-id="cb415-173">要解决此问题，请将 [`EnableDefaultApplicationDefinition`](#enabledefaultapplicationdefinition) 或 [`EnableDefaultPageItems`](#enabledefaultpageitems) 设置为 `false`。</span><span class="sxs-lookup"><span data-stu-id="cb415-173">To work around this problem, set either [`EnableDefaultApplicationDefinition`](#enabledefaultapplicationdefinition) or [`EnableDefaultPageItems`](#enabledefaultpageitems) to `false`.</span></span> <span data-ttu-id="cb415-174">将这些值设置为 `false` 会恢复到以前 SDK 的行为，其中你必须在项目中显式定义默认 glob，或者显式定义要包括在项目中的文件。</span><span class="sxs-lookup"><span data-stu-id="cb415-174">Setting these values to `false` reverts to the behavior of previous SDKs where you had to explicitly define the default globs in your project, or explicitly define the files to include in the project.</span></span>

<span data-ttu-id="cb415-175">可以通过将 [`EnableDefaultItems`](msbuild-props.md#enabledefaultitems) 属性设置为 `false` 来完全禁用所有隐式包含。</span><span class="sxs-lookup"><span data-stu-id="cb415-175">You can completely disable all implicit includes by setting the [`EnableDefaultItems` property](msbuild-props.md#enabledefaultitems) to `false`.</span></span>

## <a name="wpf-settings"></a><span data-ttu-id="cb415-176">WPF 设置</span><span class="sxs-lookup"><span data-stu-id="cb415-176">WPF settings</span></span>

- [<span data-ttu-id="cb415-177">UseWPF</span><span class="sxs-lookup"><span data-stu-id="cb415-177">UseWPF</span></span>](#usewpf)
- [<span data-ttu-id="cb415-178">EnableDefaultApplicationDefinition</span><span class="sxs-lookup"><span data-stu-id="cb415-178">EnableDefaultApplicationDefinition</span></span>](#enabledefaultapplicationdefinition)
- [<span data-ttu-id="cb415-179">EnableDefaultPageItems</span><span class="sxs-lookup"><span data-stu-id="cb415-179">EnableDefaultPageItems</span></span>](#enabledefaultpageitems)

<span data-ttu-id="cb415-180">有关非特定于 WPF 的项目设置的信息，请参阅 [.NET SDK 项目的 MSBuild 参考](msbuild-props.md)。</span><span class="sxs-lookup"><span data-stu-id="cb415-180">For information about non-WPF-specific project settings, see [MSBuild reference for .NET SDK projects](msbuild-props.md).</span></span>

### <a name="usewpf"></a><span data-ttu-id="cb415-181">UseWPF</span><span class="sxs-lookup"><span data-stu-id="cb415-181">UseWPF</span></span>

<span data-ttu-id="cb415-182">`UseWPF` 属性控制是否包含对 WPF 库的引用。</span><span class="sxs-lookup"><span data-stu-id="cb415-182">The `UseWPF` property controls whether or not to include references to WPF libraries.</span></span> <span data-ttu-id="cb415-183">这还会更改 MSBuild 管道，以便正确处理 WPF 项目和相关文件。</span><span class="sxs-lookup"><span data-stu-id="cb415-183">This also alters the MSBuild pipeline to correctly process a WPF project and related files.</span></span> <span data-ttu-id="cb415-184">默认值为 `false`。</span><span class="sxs-lookup"><span data-stu-id="cb415-184">The default value is `false`.</span></span> <span data-ttu-id="cb415-185">将 `UseWPF` 属性设置为 `true` 以启用 WPF 支持。</span><span class="sxs-lookup"><span data-stu-id="cb415-185">Set the `UseWPF` property to `true` to enable WPF support.</span></span> <span data-ttu-id="cb415-186">仅当启用了此属性时，才能将 Windows 平台作为目标。</span><span class="sxs-lookup"><span data-stu-id="cb415-186">You can only target the Windows platform when this property is enabled.</span></span>

```xml
<PropertyGroup>
  <UseWPF>true</UseWPF>
</PropertyGroup>
```

<span data-ttu-id="cb415-187">如果将此属性设置为 `true`，则 .NET 5.0+ 项目会自动导入 [.NET 桌面 SDK](#enable-net-desktop-sdk)。</span><span class="sxs-lookup"><span data-stu-id="cb415-187">When this property is set to `true`, .NET 5.0+ projects will automatically import the [.NET Desktop SDK](#enable-net-desktop-sdk).</span></span>

<span data-ttu-id="cb415-188">.NET Core 3.1 项目需要将 [.NET 桌面 SDK](#enable-net-desktop-sdk) 显式设为目标才能使用此属性。</span><span class="sxs-lookup"><span data-stu-id="cb415-188">.NET Core 3.1 projects need to explicitly target the [.NET Desktop SDK](#enable-net-desktop-sdk) to use this property.</span></span>

### <a name="enabledefaultapplicationdefinition"></a><span data-ttu-id="cb415-189">EnableDefaultApplicationDefinition</span><span class="sxs-lookup"><span data-stu-id="cb415-189">EnableDefaultApplicationDefinition</span></span>

<span data-ttu-id="cb415-190">`EnableDefaultApplicationDefinition` 属性控制是否在项目中隐式包含 `ApplicationDefinition` 项。</span><span class="sxs-lookup"><span data-stu-id="cb415-190">The `EnableDefaultApplicationDefinition` property controls whether `ApplicationDefinition` items are implicitly included in the project.</span></span> <span data-ttu-id="cb415-191">默认值为 `true`。</span><span class="sxs-lookup"><span data-stu-id="cb415-191">The default value is `true`.</span></span> <span data-ttu-id="cb415-192">若要禁用隐式文件包含，请将 `EnableDefaultApplicationDefinition` 属性设置为 `false`。</span><span class="sxs-lookup"><span data-stu-id="cb415-192">Set the `EnableDefaultApplicationDefinition` property to `false` to disable the implicit file inclusion.</span></span>

```xml
<PropertyGroup>
  <EnableDefaultApplicationDefinition>false</EnableDefaultApplicationDefinition>
</PropertyGroup>
```

<span data-ttu-id="cb415-193">此属性要求将 [`EnableDefaultItems` 属性](msbuild-props.md#enabledefaultitems)设置为 `true`，这是默认设置。</span><span class="sxs-lookup"><span data-stu-id="cb415-193">This property requires that the [`EnableDefaultItems` property](msbuild-props.md#enabledefaultitems) property is set to `true`, which is the default setting.</span></span>

### <a name="enabledefaultpageitems"></a><span data-ttu-id="cb415-194">EnableDefaultPageItems</span><span class="sxs-lookup"><span data-stu-id="cb415-194">EnableDefaultPageItems</span></span>

<span data-ttu-id="cb415-195">`EnableDefaultPageItems` 属性控制是否在项目中隐式包含 `Page` 项（即 _.xaml_ 文件）。</span><span class="sxs-lookup"><span data-stu-id="cb415-195">The `EnableDefaultPageItems` property controls whether `Page` items, which are _.xaml_ files, are implicitly included in the project.</span></span> <span data-ttu-id="cb415-196">默认值为 `true`。</span><span class="sxs-lookup"><span data-stu-id="cb415-196">The default value is `true`.</span></span> <span data-ttu-id="cb415-197">若要禁用隐式文件包含，请将 `EnableDefaultPageItems` 属性设置为 `false`。</span><span class="sxs-lookup"><span data-stu-id="cb415-197">Set the `EnableDefaultPageItems` property to `false` to disable the implicit file inclusion.</span></span>

```xml
<PropertyGroup>
  <EnableDefaultPageItems>false</EnableDefaultPageItems>
</PropertyGroup>
```

<span data-ttu-id="cb415-198">此属性要求将 [`EnableDefaultItems` 属性](msbuild-props.md#enabledefaultitems)设置为 `true`，这是默认设置。</span><span class="sxs-lookup"><span data-stu-id="cb415-198">This property requires that the [`EnableDefaultItems` property](msbuild-props.md#enabledefaultitems) property is set to `true`, which is the default setting.</span></span>

## <a name="windows-forms-settings"></a><span data-ttu-id="cb415-199">Windows 窗体设置</span><span class="sxs-lookup"><span data-stu-id="cb415-199">Windows Forms settings</span></span>

- [<span data-ttu-id="cb415-200">UseWindowsForms</span><span class="sxs-lookup"><span data-stu-id="cb415-200">UseWindowsForms</span></span>](#usewindowsforms)

<span data-ttu-id="cb415-201">有关非特定于 WinForms 的项目属性的信息，请参阅 [.NET SDK 项目的 MSBuild 参考](msbuild-props.md)。</span><span class="sxs-lookup"><span data-stu-id="cb415-201">For information about non-WinForms-specific project properties, see [MSBuild reference for .NET SDK projects](msbuild-props.md).</span></span>

### <a name="usewindowsforms"></a><span data-ttu-id="cb415-202">UseWindowsForms</span><span class="sxs-lookup"><span data-stu-id="cb415-202">UseWindowsForms</span></span>

<span data-ttu-id="cb415-203">`UseWindowsForms` 属性控制应用程序是否构建为以 Windows 窗体作为目标。</span><span class="sxs-lookup"><span data-stu-id="cb415-203">The `UseWindowsForms` property controls whether or not your application is built to target Windows Forms.</span></span> <span data-ttu-id="cb415-204">此属性会更改 MSBuild 管道，以便正确处理 Windows 窗体项目和相关文件。</span><span class="sxs-lookup"><span data-stu-id="cb415-204">This property alters the MSBuild pipeline to correctly process a Windows Forms project and related files.</span></span> <span data-ttu-id="cb415-205">默认值为 `false`。</span><span class="sxs-lookup"><span data-stu-id="cb415-205">The default value is `false`.</span></span> <span data-ttu-id="cb415-206">将 `UseWindowsForms` 属性设置为 `true` 可启用 Windows 窗体支持。</span><span class="sxs-lookup"><span data-stu-id="cb415-206">Set the `UseWindowsForms` property to `true` to enable Windows Forms support.</span></span> <span data-ttu-id="cb415-207">仅当启用了此设置时，才能将 Windows 平台作为目标。</span><span class="sxs-lookup"><span data-stu-id="cb415-207">You can only target the Windows platform when this setting is enabled.</span></span>

```xml
<PropertyGroup>
  <UseWindowsForms>true</UseWindowsForms>
</PropertyGroup>
```

<span data-ttu-id="cb415-208">如果将此属性设置为 `true`，则 .NET 5.0+ 项目会自动导入 [.NET 桌面 SDK](#enable-net-desktop-sdk)。</span><span class="sxs-lookup"><span data-stu-id="cb415-208">When this property is set to `true`, .NET 5.0+ projects will automatically import the [.NET Desktop SDK](#enable-net-desktop-sdk).</span></span>

<span data-ttu-id="cb415-209">.NET Core 3.1 项目需要将 [.NET 桌面 SDK](#enable-net-desktop-sdk) 显式设为目标才能使用此属性。</span><span class="sxs-lookup"><span data-stu-id="cb415-209">.NET Core 3.1 projects need to explicitly target the [.NET Desktop SDK](#enable-net-desktop-sdk) to use this property.</span></span>

## <a name="shared-settings"></a><span data-ttu-id="cb415-210">共享设置</span><span class="sxs-lookup"><span data-stu-id="cb415-210">Shared settings</span></span>

- [<span data-ttu-id="cb415-211">DisableWinExeOutputInference</span><span class="sxs-lookup"><span data-stu-id="cb415-211">DisableWinExeOutputInference</span></span>](#disablewinexeoutputinference)

### <a name="disablewinexeoutputinference"></a><span data-ttu-id="cb415-212">DisableWinExeOutputInference</span><span class="sxs-lookup"><span data-stu-id="cb415-212">DisableWinExeOutputInference</span></span>

<span data-ttu-id="cb415-213">适用于 .NET 5.0 SDK 及更高版本。</span><span class="sxs-lookup"><span data-stu-id="cb415-213">Applies to .NET 5.0 SDK and later.</span></span>

<span data-ttu-id="cb415-214">当应用的 `OutputType` 属性设置为 `Exe` 值时，如果该应用未从控制台运行，则将创建一个控制台窗口。</span><span class="sxs-lookup"><span data-stu-id="cb415-214">When an app has the `Exe` value set for the `OutputType` property, a console window is created if the app isn't running from a console.</span></span> <span data-ttu-id="cb415-215">这通常不是所需的 Windows 桌面应用行为。</span><span class="sxs-lookup"><span data-stu-id="cb415-215">This is generally not the desired behavior of a Windows Desktop app.</span></span> <span data-ttu-id="cb415-216">如果使用 `WinExe` 值，则不会创建控制台窗口。</span><span class="sxs-lookup"><span data-stu-id="cb415-216">With the `WinExe` value, a console window isn't created.</span></span> <span data-ttu-id="cb415-217">从 .NET 5.0 SDK 开始，`Exe` 值会自动转换为 `WinExe`。</span><span class="sxs-lookup"><span data-stu-id="cb415-217">Starting with the .NET 5.0 SDK, the `Exe` value is automatically transformed to `WinExe`.</span></span>

<span data-ttu-id="cb415-218">`DisableWinExeOutputInference` 属性会还原将 `Exe` 视为 `WinExe` 的行为。</span><span class="sxs-lookup"><span data-stu-id="cb415-218">The `DisableWinExeOutputInference` property reverts the behavior of treating `Exe` as `WinExe`.</span></span> <span data-ttu-id="cb415-219">将此值设置为 `true` 可还原 `OutputType` 属性值 `Exe` 的行为。</span><span class="sxs-lookup"><span data-stu-id="cb415-219">Set this value to `true` to restore the behavior of the `OutputType` property value of `Exe`.</span></span> <span data-ttu-id="cb415-220">默认值为 `false`。</span><span class="sxs-lookup"><span data-stu-id="cb415-220">The default value is `false`.</span></span>

```xml
<PropertyGroup>
  <DisableWinExeOutputInference>true</DisableWinExeOutputInference>
</PropertyGroup>
```

## <a name="see-also"></a><span data-ttu-id="cb415-221">请参阅</span><span class="sxs-lookup"><span data-stu-id="cb415-221">See also</span></span>

- [<span data-ttu-id="cb415-222">.NET 项目 SDK</span><span class="sxs-lookup"><span data-stu-id="cb415-222">.NET project SDKs</span></span>](overview.md)
- [<span data-ttu-id="cb415-223">.NET SDK 项目的 MSBuild 引用</span><span class="sxs-lookup"><span data-stu-id="cb415-223">MSBuild reference for .NET SDK projects</span></span>](msbuild-props.md)
- [<span data-ttu-id="cb415-224">MSBuild 架构引用</span><span class="sxs-lookup"><span data-stu-id="cb415-224">MSBuild schema reference</span></span>](/visualstudio/msbuild/msbuild-project-file-schema-reference)
- [<span data-ttu-id="cb415-225">通用 MSBuild 属性</span><span class="sxs-lookup"><span data-stu-id="cb415-225">Common MSBuild properties</span></span>](/visualstudio/msbuild/common-msbuild-project-properties)
- [<span data-ttu-id="cb415-226">自定义生成</span><span class="sxs-lookup"><span data-stu-id="cb415-226">Customize a build</span></span>](/visualstudio/msbuild/customize-your-build)
