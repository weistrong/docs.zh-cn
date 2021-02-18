---
title: .NET 项目 SDK 概述
titleSuffix: ''
description: 了解 .NET 项目 SDK。
ms.date: 09/17/2020
ms.topic: conceptual
no-loc:
- EmbeddedResource
- Compile
- None
ms.openlocfilehash: e5a6d0a1c988818e507936b567fa0188675cedc3
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100432642"
---
# <a name="net-project-sdks"></a>.NET 项目 SDK

.NET Core 和 .NET 5.0 及更高版本项目与软件开发工具包 (SDK) 关联。 每个项目 SDK 都是一组 MSBuild [目标](/visualstudio/msbuild/msbuild-targets)和相关的[任务](/visualstudio/msbuild/msbuild-tasks)，它们负责编译、打包和发布代码。 引用项目 SDK 的项目有时称为“SDK 样式的项目”。

## <a name="available-sdks"></a>可用的 SDK

有以下 SDK 可用：

| ID | 描述 | 存储库|
| - | - | - |
| `Microsoft.NET.Sdk` | .NET SDK | <https://github.com/dotnet/sdk> |
| `Microsoft.NET.Sdk.Web` | .NET [Web SDK](/aspnet/core/razor-pages/web-sdk) | <https://github.com/dotnet/sdk> |
| `Microsoft.NET.Sdk.Razor` | .NET [Razor SDK](/aspnet/core/razor-pages/sdk) |
| `Microsoft.NET.Sdk.Worker` | .NET 辅助角色服务 SDK |
| `Microsoft.NET.Sdk.WindowsDesktop` | .NET [桌面 SDK](msbuild-props-desktop.md)，其中包括 Windows 窗体 (WinForms) 和 Windows Presentation Foundation (WPF)。\* | <https://github.com/dotnet/winforms> 和 <https://github.com/dotnet/wpf> |

.NET SDK 是 .NET 的基本 SDK。 其他 SDK 引用 .NET SDK，与其他 SDK 关联的项目具有所有可用的 .NET SDK 属性。 例如，Web SDK 依赖于 .NET SDK 和 Razor SDK。

你还可以创建自己的 SDK，并通过 NuGet 进行分发。

\* 从 .NET 5.0 开始，Windows 窗体和 Windows Presentation Foundation (WPF) 项目应指定 .NET SDK (`Microsoft.NET.Sdk`)，而不是 `Microsoft.NET.Sdk.WindowsDesktop`。 对于这些项目，将 `TargetFramework` 设置为 `net5.0-windows` 并将 `UseWPF` 或 `UseWindowsForms` 设置为 `true` 的操作会自动导入 Windows 桌面 SDK。 如果你的项目面向 .NET 5.0 或更高版本，并指定 `Microsoft.NET.Sdk.WindowsDesktop` SDK，则会收到生成警告 NETSDK1137。

## <a name="project-files"></a>项目文件

.NET 项目基于 [MSBuild](/visualstudio/msbuild/msbuild) 格式。 具有扩展名（如用于 C# 项目的 .csproj 和用于 F# 项目的 .fsproj）的项目文件都是 XML 格式的 。 MSBuild 项目文件的根元素是 [Project](/visualstudio/msbuild/project-element-msbuild) 元素。 `Project` 元素有一个可选的 `Sdk` 属性，该属性指定要使用的 SDK（和版本）。 若要使用 .NET 工具并构建你的代码，请将 `Sdk` 属性设置为[可用 SDK](#available-sdks) 表中的其中一个 ID。

```xml
<Project Sdk="Microsoft.NET.Sdk">
  ...
</Project>
```

若要指定来自 NuGet 的 SDK，请在名称末尾包含版本，或者在 global.json 文件中指定名称和版本。

```xml
<Project Sdk="MSBuild.Sdk.Extras/2.0.54">
  ...
</Project>
```

另一种指定 SDK 的方法是使用顶层 [Sdk](/visualstudio/msbuild/sdk-element-msbuild) 元素：

```xml
<Project>
  <Sdk Name="Microsoft.NET.Sdk" />
  ...
</Project>
```

以这些方式之一引用 SDK 可以极大地简化 .NET 的项目文件。 在评估项目时，MSBuild 在项目文件的顶部和底部分别为 `Sdk.props` 和 `Sdk.targets` 添加隐式导入。

```xml
<Project>
  <!-- Implicit top import -->
  <Import Project="Sdk.props" Sdk="Microsoft.NET.Sdk" />
  ...
  <!-- Implicit bottom import -->
  <Import Project="Sdk.targets" Sdk="Microsoft.NET.Sdk" />
</Project>
```

> [!TIP]
> 在 Windows 计算机上，Sdk.props 和 Sdk.targets 文件位于 %ProgramFiles%\dotnet\sdk\\[version]\Sdks\Microsoft.NET.Sdk\Sdk 文件夹中  。

### <a name="preprocess-the-project-file"></a>预处理项目文件

使用 `dotnet msbuild -preprocess` 命令，可以看到 MSBuild 在包含 SDK 及其目标之后所显示的完全扩展的项目。 [`dotnet msbuild`](../tools/dotnet-msbuild.md) 命令的[预处理](/visualstudio/msbuild/msbuild-command-line-reference#preprocess)开关显示导入的文件、文件源及其在生成中的参与情况，而无需实际生成项目。

如果项目有多个目标框架，请将命令的结果指定为 MSBuild 属性，使其仅侧重于框架之一。 例如：

`dotnet msbuild -property:TargetFramework=netcoreapp2.0 -preprocess:output.xml`

## <a name="default-includes-and-excludes"></a>默认包含和排除的内容

SDK 中定义了 [`Compile` 项](/visualstudio/msbuild/common-msbuild-project-items#compile)、[嵌入的资源](/visualstudio/msbuild/common-msbuild-project-items#embeddedresource)和 [`None` 项](/visualstudio/msbuild/common-msbuild-project-items#none)默认包含和排除的内容。 与非 SDK .NET 框架项目不同，你无需在项目文件中指定这些项，因为默认设置涵盖了最常见的用例。 此行为使得项目文件更小、更易于理解和手动编辑（如需要）。

下表显示在 .NET SDK 中包含和排除的元素和 [glob](https://en.wikipedia.org/wiki/Glob_(programming))：

| 元素           | 包含 glob                              | 排除 glob                                                  | 删除 glob              |
|-------------------|-------------------------------------------|---------------------------------------------------------------|--------------------------|
| Compile           | \*\*/\*.cs（或其他语言扩展名） | \*\*/\*.user;  \*\*/\*.\*proj;  \*\*/\*.sln;  \*\*/\*.vssscc  | 不可用                      |
| EmbeddedResource  | \*\*/\*.resx                              | \*\*/\*.user; \*\*/\*.\*proj; \*\*/\*.sln; \*\*/\*.vssscc     | 不可用                      |
| None              | \*\*/\*                                   | \*\*/\*.user; \*\*/\*.\*proj; \*\*/\*.sln; \*\*/\*.vssscc     | \*\*/\*.cs; \*\*/\*.resx |

> [!NOTE]
> 默认情况下，由 `$(BaseOutputPath)` 和 `$(BaseIntermediateOutputPath)` MSBuild 属性表示的 `./bin` 和 `./obj` 文件夹不包含在 glob 中。 排除由 [DefaultItemExcludes 属性](msbuild-props.md#defaultitemexcludes)表示。

.NET 桌面 SDK 对于 WPF 有更多包含和排除的内容。 有关详细信息，请参阅 [WPF 默认包含和排除的内容](msbuild-props-desktop.md#wpf-default-includes-and-excludes)。

### <a name="build-errors"></a>生成错误

如果在项目文件中显式定义这些项中的任何项，可能会出现类似于以下内容的“NETSDK1022”生成错误：

> 包含重复的“Compile”项。 默认情况下，.NET SDK 包括项目目录中的“Compile”项。 可从项目文件中删除这些项，或如果想要在项目文件中显式包括它们，则将“EnableDefaultCompileItems”属性设为“false”。

> 包含重复的“EmbeddedResource”项。 默认情况下，.NET SDK 包括项目目录中的“EmbeddedResource”项。 可从项目文件中删除这些项，或如果想要在项目文件中显式包括它们，则将“EnableDefaultEmbeddedResourceItems”属性设为“false”。

若要解决此错误，请执行以下操作之一：

- 删除与上表中列出的隐式项匹配的显式 `Compile`、`EmbeddedResource` 或 `None` 项。

- 若要禁用所有隐式文件包含，请将 [EnableDefaultItems 属性](msbuild-props.md#enabledefaultitems)设置为 `false`：

  ```xml
  <PropertyGroup>
    <EnableDefaultItems>false</EnableDefaultItems>
  </PropertyGroup>
  ```

  若要指定某些文件通过应用发布，仍可以使用相应的已知 MSBuild 机制来实现（例如 `Content` 元素）。

- 可选择仅禁用 `Compile`、`EmbeddedResource` 或 `None` glob，方法是将 [EnableDefaultCompileItems](msbuild-props.md#enabledefaultcompileitems)、[EnableDefaultEmbeddedResourceItems](msbuild-props.md#enabledefaultembeddedresourceitems) 或 [EnableDefaultNoneItems](msbuild-props.md#enabledefaultnoneitems) 属性设置为 `false`：

  ```xml
  <PropertyGroup>
    <EnableDefaultCompileItems>false</EnableDefaultCompileItems>
    <EnableDefaultEmbeddedResourceItems>false</EnableDefaultEmbeddedResourceItems>
    <EnableDefaultNoneItems>false</EnableDefaultNoneItems>
  </PropertyGroup>
  ```

  如果仅禁用 `Compile` glob，则 Visual Studio 中的解决方案资源管理器仍将 \*.cs 项显示为项目的一部分，并作为 `None` 项包含在内。 若要禁用隐式 `None` glob，请将 `EnableDefaultNoneItems` 也设置为 `false`。

## <a name="implicit-package-references"></a>隐式包引用

如果以 .NET Core 1.0 - 2.2 或 .NET Standard 1.0 - 2.0 为目标，则 .NET SDK 会添加对某些元包的隐式引用。 元包是一种基于框架的包，其中只包含对其他包的依赖项。 元包根据项目文件的 [TargetFramework](msbuild-props.md#targetframework) 或 [TargetFrameworks](msbuild-props.md#targetframeworks) 属性中指定的目标框架被隐式引用。

```xml
<PropertyGroup>
  <TargetFramework>netcoreapp2.1</TargetFramework>
</PropertyGroup>
```

```xml
<PropertyGroup>
  <TargetFrameworks>netcoreapp2.1;net462</TargetFrameworks>
</PropertyGroup>
```

如果需要，可以使用 [DisableImplicitFrameworkReferences](msbuild-props.md#disableimplicitframeworkreferences) 属性来禁用隐式包引用，并只添加对所需的框架或包的显式引用。

建议：

- 如果以 .NET Framework、.NET Core 1.0 - 2.2 或 .NET Standard 1.0 - 2.0 为目标，不要通过项目文件中的 `<PackageReference>` 项添加对 `Microsoft.NETCore.App` 或 `NETStandard.Library` 元包的显式引用。 对于 .NET Core 1.0 - 2.2 和 .NET Standard 1.0 - 2.0 项目，这些元包被隐式引用。 对于 .NET Framework 项目，如果在使用基于 .NET Standard 的 NuGet 包时需要任何版本的 `NETStandard.Library`，则 NuGet 会自动安装相应版本。
- 如果在以 .NET Core 1.0 - 2.2 为目标时需要特定版本的运行时，请在项目中使用 `<RuntimeFrameworkVersion>` 属性（例如，`1.0.4`），而不是引用元包。 例如，如果在使用[独立式部署](../deploying/index.md#publish-self-contained)，则可能需要特定补丁版本的 1.0.0 LTS 运行时。
- 如果在以 .NET Standard 1.0 - 2.0 为目标时需要特定版本的 `NETStandard.Library` 元包，则可以使用 `<NetStandardImplicitPackageVersion>` 属性，并设置所需的版本。

## <a name="build-events"></a>生成事件

在 SDK 样式的项目中，请使用名为 `PreBuild` 或 `PostBuild` 的 MSBuild 目标，并设置 `PreBuild` 的 `BeforeTargets` 属性或 `PostBuild` 的 `AfterTargets` 属性。

```xml
<Target Name="PreBuild" BeforeTargets="PreBuildEvent">
    <Exec Command="&quot;$(ProjectDir)PreBuildEvent.bat&quot; &quot;$(ProjectDir)..\&quot; &quot;$(ProjectDir)&quot; &quot;$(TargetDir)&quot;" />
</Target>

<Target Name="PostBuild" AfterTargets="PostBuildEvent">
   <Exec Command="echo Output written to $(TargetDir)" />
</Target>
```

> [!NOTE]
>
> - 可以为 MSBuild 目标使用任何名称。 但是，Visual Studio IDE 会识别 `PreBuild` 和 `PostBuild` 目标，因此通过使用这些名称，可以在 IDE 中编辑命令。
> - 不建议在 SDK 样式的项目中使用属性 `PreBuildEvent` 和 `PostBuildEvent`，因为无法解析 `$(ProjectDir)` 这样的宏。 例如，以下代码是不受支持的：
>
> ```xml
> <PropertyGroup>
>   <PreBuildEvent>"$(ProjectDir)PreBuildEvent.bat" "$(ProjectDir)..\" "$(ProjectDir)" "$(TargetDir)"</PreBuildEvent>
> </PropertyGroup>
> ```

## <a name="customize-the-build"></a>自定义生成

可以通过多种方式[自定义生成](/visualstudio/msbuild/customize-your-build)。 建议通过将属性作为参数传递给 [msbuild](/visualstudio/msbuild/msbuild-command-line-reference) 或 [dotnet](../tools/index.md) 命令来重写该属性。 还可以将属性添加到项目文件或 Directory.Build.props 文件中。 有关 .NET 项目的有用属性列表，请参见 [.NET SDK 项目的 MSBuild 参考](msbuild-props.md)。

### <a name="custom-targets"></a>自定义目标

.NET 项目可以打包自定义的 MSBuild 目标和属性，以供使用该包的项目使用。 如果要执行以下操作，请使用此类型的可扩展性：

- 扩展生成过程。
- 访问生成过程的工件，如生成的文件。
- 检查调用生成的配置。

通过在项目的生成文件夹中以 `<package_id>.targets` 或 `<package_id>.props`（例如 `Contoso.Utility.UsefulStuff.targets`）的形式放置文件，可以添加自定义生成目标或属性。

以下 XML 是 .csproj 文件中的一个片段，该文件指示 [`dotnet pack`](../tools/dotnet-pack.md) 命令打包的内容。 `<ItemGroup Label="dotnet pack instructions">` 元素将目标文件放入包内的生成文件夹中。 `<Target Name="CollectRuntimeOutputs" BeforeTargets="_GetPackageFiles">` 元素将程序集和 .json 文件放入生成文件夹 。

```xml
<Project Sdk="Microsoft.NET.Sdk">

  ...
  <ItemGroup Label="dotnet pack instructions">
    <Content Include="build\*.targets">
      <Pack>true</Pack>
      <PackagePath>build\</PackagePath>
    </Content>
  </ItemGroup>
  <Target Name="CollectRuntimeOutputs" BeforeTargets="_GetPackageFiles">
    <!-- Collect these items inside a target that runs after build but before packaging. -->
    <ItemGroup>
      <Content Include="$(OutputPath)\*.dll;$(OutputPath)\*.json">
        <Pack>true</Pack>
        <PackagePath>build\</PackagePath>
      </Content>
    </ItemGroup>
  </Target>
  ...

</Project>
```

若要在项目中使用自定义目标，请添加指向包及其版本的 `PackageReference` 元素。 与工具不同，自定义目标包包含在消费项目的依赖项闭包中。

你可以配置自定义目标的使用方式。 由于它是 MSBuild 目标，因此会依赖于给定的目标并在另一个目标后运行，也可使用 `dotnet msbuild -t:<target-name>` 命令手动调用。 若要提供更好的用户体验，可以合并基于项目的工具和自定义目标。 在此方案中，每个项目工具接受所需的任何参数，并将其转换为执行目标所需的 [`dotnet msbuild`](../tools/dotnet-msbuild.md) 调用。 有关此类协同作用的示例，请访问 [`dotnet-packer`](https://github.com/dotnet/MVPSummitHackathon2016/tree/master/dotnet-packer) 项目中的 [2016 年编程马拉松 MVP 峰会示例](https://github.com/dotnet/MVPSummitHackathon2016)存储库。

## <a name="see-also"></a>请参阅

- [安装 .NET Core](../install/index.yml)
- [如何使用 MSBuild 项目 SDK](/visualstudio/msbuild/how-to-use-project-sdk)
- [使用 NuGet 打包自定义 MSBuild 目标和属性](/nuget/create-packages/creating-a-package#include-msbuild-props-and-targets-in-a-package)
