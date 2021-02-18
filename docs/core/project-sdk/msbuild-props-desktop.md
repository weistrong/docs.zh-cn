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
# <a name="msbuild-reference-for-net-desktop-sdk-projects"></a>.NET 桌面 SDK 项目的 MSBuild 参考

此页是有关用于通过 .NET 桌面 SDK 配置 Windows 窗体 (WinForms) 和 Windows Presentation Foundation (WPF) 项目的 MSBuild 属性和项的参考。

> [!NOTE]
> 本文介绍了 .NET SDK 的 MSBuild 属性的子集，因为它与桌面应用相关。 有关常用 .NET SDK 特定 MSBuild 属性的列表，请参见 [.NET SDK 项目的 MSBuild 参考](msbuild-props.md)。 有关通用 MSBuild 属性的列表，请参阅[通用 MSBuild 属性](/visualstudio/msbuild/common-msbuild-project-properties)。

## <a name="enable-net-desktop-sdk"></a>启用 .NET 桌面 SDK

若要使用 WinForms 或 WPF，请配置你的项目文件。

### <a name="net-50"></a>.NET 5.0

在 WinForms 或 WPF 项目的项目文件中指定以下设置：

- 将 .NET SDK `Microsoft.NET.Sdk` 作为目标。 有关详细信息，请参阅[项目文件](overview.md#project-files)。
- 将 [`TargetFramework`](msbuild-props.md#targetframework) 设置为 `net5.0-windows`。
- 添加 UI 框架属性（或两者，如果必要）：
  - 将 [`UseWPF`](#usewpf) 设置为 `true` 以导入并使用 WPF。
  - 将 [`UseWindowsForms`](#usewindowsforms) 设置为 `true` 以导入并使用 WinForms。
- （可选）将 `OutputType` 设置为 `WinExe`。 这将生成应用，而不是库。 若要生成库，请省略此属性。

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

### <a name="net-core-31"></a>.NET Core 3.1

在 WinForms 或 WPF 项目的项目文件中指定以下设置：

- 将 .NET SDK `Microsoft.NET.Sdk.WindowsDesktop` 作为目标。 有关详细信息，请参阅[项目文件](overview.md#project-files)。
- 将 [`TargetFramework`](msbuild-props.md#targetframework) 设置为 `netcoreapp3.1`。
- 添加 UI 框架属性（或两者，如果必要）：
  - 将 [`UseWPF`](#usewpf) 设置为 `true` 以导入并使用 WPF。
  - 将 [`UseWindowsForms`](#usewindowsforms) 设置为 `true` 以导入并使用 WinForms。
- （可选）将 `OutputType` 设置为 `WinExe`。 这将生成应用，而不是库。 若要生成库，请省略此属性。

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

## <a name="wpf-default-includes-and-excludes"></a>WPF 默认包含和排除的内容

SDK 项目定义一组规则，用于在项目中隐式包含或排除文件。 这些规则还自动设置文件的生成操作。 这与较旧的非 SDK .NET Framework 项目不同，后者没有默认的包含或排除规则。 .NET Framework 项目需要你显式声明要将哪些文件包含在项目中。

.NET 项目文件包括一组[标准规则](overview.md#default-includes-and-excludes)，用于自动处理文件。 WPF 项目添加了更多规则。

下表显示当 [`UseWPF`](#usewpf) 项目属性设置为 `true` 时在 .NET 桌面 SDK 中包含和排除哪些元素和 [glob](https://en.wikipedia.org/wiki/Glob_(programming))：

| 元素               | 包含 glob                 | 排除 glob                                                                                           | 删除 glob  |
|-----------------------|------------------------------|--------------------------------------------------------------------|--------------|
| ApplicationDefinition | App.xaml 或 Application.xaml | 不可用                                                                | 不可用          |
| Page                  | \*\*/\*.xaml                 | \*\*/\*.user; \*\*/\*.\*proj; \*\*/\*.sln; \*\*/\*.vssscc<br>*ApplicationDefinition* 定义的任何 XAML | 不可用          |
| None                  | 不可用                          | 不可用                                                                | \*\*/\*.xaml |

下面是所有项目类型的默认包含和排除设置。 有关详细信息，请参阅[默认的包括和排除](overview.md#default-includes-and-excludes)。

| 元素           | 包含 glob                              | 排除 glob                                                  | 删除 glob              |
|-------------------|-------------------------------------------|---------------------------------------------------------------|--------------------------|
| Compile           | \*\*/\*.cs；\*\*/\*.vb（或其他语言扩展名） | \*\*/\*.user;  \*\*/\*.\*proj;  \*\*/\*.sln;  \*\*/\*.vssscc  | 不可用          |
| EmbeddedResource  | \*\*/\*.resx                              | \*\*/\*.user; \*\*/\*.\*proj; \*\*/\*.sln; \*\*/\*.vssscc     | 不可用                      |
| None              | \*\*/\*                                   | \*\*/\*.user; \*\*/\*.\*proj; \*\*/\*.sln; \*\*/\*.vssscc     | \*\*/\*.cs; \*\*/\*.resx |

### <a name="errors-related-to-duplicate-items"></a>与“重复”项相关的错误

如果已将文件显式添加到项目，或让 XAML glob 自动将文件包含在项目中，则可能会收到以下错误之一：

* 包含重复的“ApplicationDefinition”项。
* 包含重复的“Page”项。

这些错误是隐式包含 glob 与你的设置冲突的结果。 要解决此问题，请将 [`EnableDefaultApplicationDefinition`](#enabledefaultapplicationdefinition) 或 [`EnableDefaultPageItems`](#enabledefaultpageitems) 设置为 `false`。 将这些值设置为 `false` 会恢复到以前 SDK 的行为，其中你必须在项目中显式定义默认 glob，或者显式定义要包括在项目中的文件。

可以通过将 [`EnableDefaultItems`](msbuild-props.md#enabledefaultitems) 属性设置为 `false` 来完全禁用所有隐式包含。

## <a name="wpf-settings"></a>WPF 设置

- [UseWPF](#usewpf)
- [EnableDefaultApplicationDefinition](#enabledefaultapplicationdefinition)
- [EnableDefaultPageItems](#enabledefaultpageitems)

有关非特定于 WPF 的项目设置的信息，请参阅 [.NET SDK 项目的 MSBuild 参考](msbuild-props.md)。

### <a name="usewpf"></a>UseWPF

`UseWPF` 属性控制是否包含对 WPF 库的引用。 这还会更改 MSBuild 管道，以便正确处理 WPF 项目和相关文件。 默认值为 `false`。 将 `UseWPF` 属性设置为 `true` 以启用 WPF 支持。 仅当启用了此属性时，才能将 Windows 平台作为目标。

```xml
<PropertyGroup>
  <UseWPF>true</UseWPF>
</PropertyGroup>
```

如果将此属性设置为 `true`，则 .NET 5.0+ 项目会自动导入 [.NET 桌面 SDK](#enable-net-desktop-sdk)。

.NET Core 3.1 项目需要将 [.NET 桌面 SDK](#enable-net-desktop-sdk) 显式设为目标才能使用此属性。

### <a name="enabledefaultapplicationdefinition"></a>EnableDefaultApplicationDefinition

`EnableDefaultApplicationDefinition` 属性控制是否在项目中隐式包含 `ApplicationDefinition` 项。 默认值为 `true`。 若要禁用隐式文件包含，请将 `EnableDefaultApplicationDefinition` 属性设置为 `false`。

```xml
<PropertyGroup>
  <EnableDefaultApplicationDefinition>false</EnableDefaultApplicationDefinition>
</PropertyGroup>
```

此属性要求将 [`EnableDefaultItems` 属性](msbuild-props.md#enabledefaultitems)设置为 `true`，这是默认设置。

### <a name="enabledefaultpageitems"></a>EnableDefaultPageItems

`EnableDefaultPageItems` 属性控制是否在项目中隐式包含 `Page` 项（即 _.xaml_ 文件）。 默认值为 `true`。 若要禁用隐式文件包含，请将 `EnableDefaultPageItems` 属性设置为 `false`。

```xml
<PropertyGroup>
  <EnableDefaultPageItems>false</EnableDefaultPageItems>
</PropertyGroup>
```

此属性要求将 [`EnableDefaultItems` 属性](msbuild-props.md#enabledefaultitems)设置为 `true`，这是默认设置。

## <a name="windows-forms-settings"></a>Windows 窗体设置

- [UseWindowsForms](#usewindowsforms)

有关非特定于 WinForms 的项目属性的信息，请参阅 [.NET SDK 项目的 MSBuild 参考](msbuild-props.md)。

### <a name="usewindowsforms"></a>UseWindowsForms

`UseWindowsForms` 属性控制应用程序是否构建为以 Windows 窗体作为目标。 此属性会更改 MSBuild 管道，以便正确处理 Windows 窗体项目和相关文件。 默认值为 `false`。 将 `UseWindowsForms` 属性设置为 `true` 可启用 Windows 窗体支持。 仅当启用了此设置时，才能将 Windows 平台作为目标。

```xml
<PropertyGroup>
  <UseWindowsForms>true</UseWindowsForms>
</PropertyGroup>
```

如果将此属性设置为 `true`，则 .NET 5.0+ 项目会自动导入 [.NET 桌面 SDK](#enable-net-desktop-sdk)。

.NET Core 3.1 项目需要将 [.NET 桌面 SDK](#enable-net-desktop-sdk) 显式设为目标才能使用此属性。

## <a name="shared-settings"></a>共享设置

- [DisableWinExeOutputInference](#disablewinexeoutputinference)

### <a name="disablewinexeoutputinference"></a>DisableWinExeOutputInference

适用于 .NET 5.0 SDK 及更高版本。

当应用的 `OutputType` 属性设置为 `Exe` 值时，如果该应用未从控制台运行，则将创建一个控制台窗口。 这通常不是所需的 Windows 桌面应用行为。 如果使用 `WinExe` 值，则不会创建控制台窗口。 从 .NET 5.0 SDK 开始，`Exe` 值会自动转换为 `WinExe`。

`DisableWinExeOutputInference` 属性会还原将 `Exe` 视为 `WinExe` 的行为。 将此值设置为 `true` 可还原 `OutputType` 属性值 `Exe` 的行为。 默认值为 `false`。

```xml
<PropertyGroup>
  <DisableWinExeOutputInference>true</DisableWinExeOutputInference>
</PropertyGroup>
```

## <a name="see-also"></a>请参阅

- [.NET 项目 SDK](overview.md)
- [.NET SDK 项目的 MSBuild 引用](msbuild-props.md)
- [MSBuild 架构引用](/visualstudio/msbuild/msbuild-project-file-schema-reference)
- [通用 MSBuild 属性](/visualstudio/msbuild/common-msbuild-project-properties)
- [自定义生成](/visualstudio/msbuild/customize-your-build)
