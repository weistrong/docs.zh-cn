---
title: 迁移到 .NET 5 的示例
description: 演示如何将目标 .NET Framework 的示例应用程序迁移到 .NET 5。
ms.date: 01/19/2021
ms.openlocfilehash: 5b3743c68ee0426efffda6f999dffea788f493e9
ms.sourcegitcommit: bdbf6472de867a0a11aaa5b9384a2506c24f27d2
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/05/2021
ms.locfileid: "102206537"
---
# <a name="example-of-migrating-to-net"></a>迁移到 .NET 的示例

在本章中，我们提供了实用指导原则，可帮助你将现有应用程序从 .NET Framework 迁移到 .NET。

我们提供了一个结构良好的过程，你可以遵循此过程以及每个步骤要考虑的最重要事项。

接下来，我们记录了 WinForms 和 WPF 版本的示例桌面应用程序的分步迁移过程。

## <a name="migration-process-overview"></a>迁移过程概述

迁移过程包括四个顺序步骤：

1. **准备**：了解项目所需的依赖关系，了解这一点。 在此步骤中，您将使用当前项目，以简化迁移的启动点。

2. **迁移项目文件：** .net 项目使用的是新的 SDK 样式项目格式。 使用此格式创建一个新的项目文件，或更新必须使用 SDK 样式的项目文件。

3. **修复代码并生成：** 在 .NET 寻址 API 级别的 .NET Framework 与 .NET 之间的差异中生成代码。 如果需要，请将第三方包更新为支持 .NET 的包。

4. **运行和测试：** 可能存在直到运行时才会显示的差异。 因此，请不要忘记运行应用程序并测试一切是否按预期方式工作。

### <a name="preparation"></a>准备工作

#### <a name="migrate-packagesconfig-file"></a>迁移 packages.config 文件

在 .NET Framework 应用程序中，对外部包的所有引用都在 *packages.config* 文件中声明。 在 .NET 中，不再需要使用 *packages.config* 文件。 而应使用项目文件中的 [PackageReference](../../core/project-sdk/msbuild-props.md#packagereference) 属性来指定应用的 NuGet 包。

因此，您需要从一种格式转换为另一种格式。 您可以手动进行更新，采用 *packages.config* 文件中包含的依赖项并将其迁移到具有格式的项目文件 `PackageReference` 。 或者，你可以让 Visual Studio 为你完成工作：右键单击 *packages.config* 文件，然后选择 "将 **packages.config 迁移到 PackageReference** " 选项。

#### <a name="verify-every-dependency-compatibility-in-net"></a>验证 .NET 中的每个依赖项兼容性

迁移包引用后，必须检查每个引用的兼容性。 可以浏览应用程序在 [nuget.org](https://www.nuget.org/)上使用的每个 NuGet 包的依赖关系。如果包具有 .NET Standard 依赖项，则它将在 .NET 5.0 上运行，因为 .NET [支持](../../standard/net-standard.md#net-implementation-support) 所有版本的 .NET Standard。 下图显示了包的依赖项 `Castle.Windsor` ：

![城堡 Windsor 包的 NuGet 依赖项的屏幕截图](./media/example-migration-core/nuget-dependencies.png)

若要检查包兼容性，可以使用 <https://fuget.org> 提供有关版本和依赖项的更多详细信息的工具。

此项目可能引用了不支持 .NET 的较旧包版本，但你可能会发现支持它的较新版本。 因此，将包更新到较新版本通常是一种很好的建议。 但是，你应该考虑更新包版本会引入一些重大更改，这些更改将强制你更新代码。

如果找不到兼容的版本，会发生什么情况？ 如果你只是因为这种重大更改而不想更新包的版本怎么办？ 请不要担心，因为它可能依赖于 .NET 应用程序中 .NET Framework 包。 请不要忘记对其进行大量测试，因为如果外部包调用的 API 在 .NET 中不可用，则可能会导致运行时错误。 这非常适合于使用不会更新的旧包，并且你可以直接重定向到 .NET 中的工作。

#### <a name="check-for-api-compatibility"></a>检查是否有 API 兼容性

由于 .NET Framework 和 .NET 中的 API 图面类似但并不完全相同，因此必须检查哪些 Api 在 .NET 上可用，哪些不是。 可以使用 .NET 可移植性分析器工具来呈现 .NET 上所使用的 Api。 它查看应用的二进制级别，提取调用的所有 Api，然后列出目标框架上不可用的 Api ( 在此情况下) 的 .NET 5.0。

可以在以下位置找到有关此工具的详细信息：

<https://docs.microsoft.com/dotnet/standard/analyzers/portability-analyzer>

此工具的一个有趣方面是，它仅从您自己的代码，而不是不能更改的外部包的代码呈现差异。 请记住，您应该更新这些包中的大部分，以使它们可用于 .NET。

### <a name="migrate-with-try-convert-tool"></a>通过 Try 转换工具迁移

[试用转换](https://github.com/dotnet/try-convert/releases)工具是迁移项目的好方法。 它是一个全局工具，它尝试将项目文件从旧样式升级到新的 SDK 样式，并将适用的项目重定目标到 .NET 5。 安装完成后，可以运行以下命令：

```dotnetcli
try-convert -p "<path to your project file>"
```

或：

```dotnetcli
try-convert -w "<path to your solution>"
```

> [!NOTE]
> "Try-转换" 工具作为 [.Net 升级助手工具](https://aka.ms/dotnet-upgrade-assistant)的一部分自动运行。 请考虑运行完整的升级助手，而不只是尝试转换。

在该工具尝试转换后，在 Visual Studio 中重新加载文件以运行和测试。 由于你的项目的具体情况，可能无法尝试转换来执行转换。 在这种情况下，可以参考以下步骤。

#### <a name="migrate-manually"></a>手动迁移

1. 创建新的 .NET 项目

在大多数情况下，你需要将现有项目更新为新的 .NET 格式。 不过，您也可以创建一个新项目，同时保持旧项目。 更新旧项目的主要缺点是丢失设计器支持，这对你和你的开发团队可能很重要。 如果要继续使用设计器，则必须与旧 .NET 项目并行创建新的 .NET 项目并共享资产。 如果需要修改设计器中的 UI 元素，则可以切换到旧项目来执行该操作。 由于资源已链接，因此也会在 .NET 项目中对其进行更新。

适用于 .NET 的 [SDK 样式项目](../../core/project-sdk/msbuild-props.md) 比 .NET Framework 的项目格式简单得多。 除了前面提到的 `PackageReference` 条目，你无需执行更多操作。 新的项目格式 [包括默认情况下具有特定扩展名的文件](../../core/project-sdk/overview.md#default-includes-and-excludes)（如 `.cs` 和 `.xaml` 文件），而无需在项目文件中显式包含这些文件。

#### <a name="assemblyinfo-considerations"></a>AssemblyInfo 注意事项

特性是在 .NET 项目上自动生成的。 如果项目包含 *AssemblyInfo.cs* 文件，则会复制定义，这将导致编译冲突。 可以通过将以下条目添加到 .NET 项目文件来删除旧的 *AssemblyInfo.cs* 文件或禁用自动生成所：

```xml
<Project Sdk="Microsoft.NET.Sdk">
  <PropertyGroup>
    <GenerateAssemblyInfo>false</GenerateAssemblyInfo>
  </PropertyGroup>
</Project>
```

#### <a name="resources"></a>资源

嵌入资源会自动包含在内，但资源不会，因此需要将资源迁移到新的项目文件。

#### <a name="package-references"></a>包引用

通过将 **packages.config 迁移到 PackageReference** 选项，可以轻松地将外部包引用移动到前面提到的新格式。

#### <a name="update-package-references"></a>更新包引用

更新发现的兼容包版本，如前一部分中所示。

### <a name="fix-the-code-and-build"></a>修复代码和生成

#### <a name="microsoftwindowscompatibility"></a>Microsoft. 兼容

如果你的应用程序依赖于 .NET 中不可用的 Api （如注册表、Acl 或 WCF），则必须包含对包的引用 `Microsoft.Windows.Compatibility` 以添加这些特定于 Windows 的 api。 它们可在 .NET 中使用，但不会包含在内，因为它们不跨平台。

有一个名为 API Analyzer (<https://docs.microsoft.com/dotnet/standard/analyzers/api-analyzer>) 的工具，可帮助你识别与你的代码不兼容的 api。

#### <a name="use-if-directives"></a>使用 \# if 指令

如果在面向 .NET Framework 和 .NET 时需要不同的执行路径，则应使用编译常量。 向代码中添加一些 \# if 指令，以便为两个目标保留相同的基本代码。

#### <a name="technologies-not-available-on-net"></a>.NET 中不可用的技术

某些技术在 .NET 中不可用，例如：

* AppDomain
* 远程处理
* 代码访问安全性
* WCF 服务器
* Windows 工作流

这就是你在应用程序中使用这些技术时需要找一代的原因。 有关详细信息，请参阅 [.Net Core 和 .net 5 + 文章上的 .NET Framework 技术不可用](../../core/porting/net-framework-tech-unavailable.md) 。

#### <a name="regenerate-autogenerated-clients"></a>重新生成自动生成的客户端

如果应用程序使用自动生成的代码（例如 WCF 客户端），则可能需要重新生成此代码以面向 .NET。 有时，您可以找到某些缺少的引用，因为它们可能不包含在默认 .NET 程序集集的一部分中。 使用类似的工具 <https://apisof.net/> ，您可以轻松地找到缺少引用所在的程序集，并从 NuGet 添加该引用。

#### <a name="rolling-back-package-versions"></a>正在回滚包版本

作为一般规则，我们以前提到过，你可以更好地更新每个包版本，使其与 .NET 兼容。 但是，你可能会发现，面向的是更新的兼容版本的程序集不会付费。 如果更改成本不是可接受的，则可以考虑回滚包版本，保留 .NET Framework 使用的版本。 尽管它们可能不针对 .NET，但它们应该能够正常工作，除非它们调用了某些不受支持的 Api。

### <a name="run-and-test"></a>运行和测试

一旦您的应用程序生成无错误，就可以通过测试每个功能开始迁移的最后一步。

在最后一步中，你可以找到几个不同的问题，具体取决于你的应用程序的复杂性以及你使用的依赖项和 Api。

例如，如果使用配置文件 (*app.config*) ，则在运行时可能会发现一些错误，如配置部分不存在。 使用 `Microsoft.Extensions.Configuration` NuGet 程序包应修复该错误。

错误的另一个原因是使用 `BeginInvoke` 和方法， `EndInvoke` 因为它们在 .net 上不受支持。 .NET 不支持它们，因为它们依赖于远程处理，而 .NET 上并不存在。 若要解决此问题，请尝试 `await` 在可用) 或方法时使用关键字 (<xref:System.Threading.Tasks.Task.Run%2A?displayProperty=nameWithType> 。

你可以使用兼容性分析器来识别代码中的 Api 和代码模式，这可能会在运行时使用 .NET 引起问题。 <https://github.com/dotnet/platform-compat>在项目上，请参阅并使用 .NET API 分析器。

## <a name="migrating-a-windows-forms-application"></a>迁移 Windows 窗体应用程序

为了展示 Windows 窗体应用程序的完整迁移过程，我们选择了在中迁移可用的 eShop 示例应用程序 <https://github.com/dotnet-architecture/eShopModernizing/tree/master/eShopLegacyNTier/src/eShopWinForms> 。 可以在中找到迁移的完整结果 <https://github.com/dotnet-architecture/eShopModernizing/tree/master/eShopModernizedNTier/src/eShopWinForms> 。

此应用程序显示产品目录，并允许用户导航、筛选和搜索产品。 从体系结构的角度来看，应用依赖于充当后端数据库外观的外部 WCF 服务。

可以在下图中看到主应用程序窗口：

![主应用程序窗口](./media/example-migration-core/main-application-window.png)

如果打开 *.csproj* 项目文件，则可以看到如下所示的内容：

![.Csproj 文件内容的屏幕截图](./media/example-migration-core/csproj-file.png)

如前所述，.NET 项目具有更精简的样式，需要将项目结构迁移到新的 .NET SDK 样式。

在解决方案资源管理器中，右键单击 Windows 窗体项目，然后选择 "**卸载项目**" "  >  **编辑**"。

现在可以更新 .csproj 文件。 你将删除整个内容，并将其替换为以下代码：

```xml
<Project Sdk="Microsoft.NET.Sdk">
  <PropertyGroup>
    <OutputType>WinExe</OutputType>
    <TargetFramework>net5.0-windows</TargetFramework>
    <UseWindowsForms>true</UseWindowsForms>
    <GenerateAssemblyInfo>false</GenerateAssemblyInfo>
  </PropertyGroup>
</Project>
```

保存并重新加载项目。 你现在已经完成了项目文件的更新，并且项目面向 .NET。

如果此时编译项目，会发现一些与 WCF 客户端引用相关的错误。 由于此代码是自动生成的，因此必须将其重新生成为目标 .NET。

![Visual Studio 上的编译错误的屏幕截图](./media/example-migration-core/winforms-compilation-errors.png)

删除 *Reference.cs* 文件并生成新的服务客户端。

右键单击 **连接的服务** ，然后选择 " **添加连接的服务** " 选项。

![选中 "添加连接的服务" 选项的 "连接的服务" 菜单的屏幕截图](./media/example-migration-core/add-connected-service.png)

此时将打开 "连接的服务" 窗口。 选择 " **MICROSOFT WCF Web 服务** " 选项。

![连接的服务窗口的屏幕截图](./media/example-migration-core/connected-services-window.png)

如果你在此示例中的同一解决方案中有 WCF 服务，则可以选择 " **发现** " 选项，而不是指定服务 URL。

!["配置 WCF Web 服务引用" 窗口的屏幕截图](./media/example-migration-core/configure-wcf-reference.png)

找到该服务后，该工具将反映该服务实现的 API 协定。 将命名空间的名称更改为，如下 `eShopServiceReference` 图所示：

![屏幕截图 API 协定和命名空间已更改](./media/example-migration-core/api-contract-namespace.png)

选择 " **完成** " 按钮。 一段时间后，你将看到生成的代码。

应会看到三个自动生成的文件：

1. *入门*：指向 GitHub 的链接，以提供有关 WCF 的某些信息。
2. *ConnectedService.js*：用于连接到服务的配置参数。
3. *Reference.cs*：实际 WCF 客户端代码。

![包含三个自动生成的文件的解决方案资源管理器窗口的屏幕截图](./media/example-migration-core/autogenerated-files.png)

如果再次编译，则会看到多个错误来自 *Helper* 文件夹内的 *.cs* 文件。 此文件夹存在于 .NET Framework 版本中，但不包含在旧的 *.csproj* 中。 但对于新的 SDK 样式项目，默认情况下会包括项目文件位置下的每个代码文件。 也就是说，新的 .NET Core 项目会尝试编译 *Helper* 文件夹内的文件。 由于不需要此文件夹，因此可以安全地将其删除。

如果再次编译项目并执行它，将看不到产品图像。 问题在于，文件的路径略有变化。 若要解决此问题，需要在路径中添加另一个级别的深度，并在文件中进行更新 `CatalogView.cs` ：

```csharp
string image_name = Environment.CurrentDirectory + "\\..\\..\\Assets\\Images\\Catalog\\" + catalogItems.Picturefilename;
```

to

```csharp
string image_name = Environment.CurrentDirectory + "\\..\\..\\..\\Assets\\Images\\Catalog\\" + catalogItems.Picturefilename;
```

在此更改后，可以检查应用程序是否在 .NET Core 上按预期启动并运行。

## <a name="migrating-a-wpf-application"></a>迁移 WPF 应用程序

我们将使用 `Shop.ClassicWPF` 示例应用程序来执行迁移。 下图显示了迁移之前的应用程序的屏幕截图：

![迁移之前的示例应用](./media/example-migration-core/app-before-migration.png)

此应用程序使用本地 SQL Server Express 数据库来保存产品目录信息。 可以直接从 WPF 应用程序访问此数据库。

首先，必须将 *.csproj* 文件更新为 .net Core 应用程序使用的新 SDK 样式。 你将按照 Windows 窗体迁移中所述的相同步骤进行操作：卸载项目、打开 *.csproj* 文件、更新其内容，并重新加载项目。

在这种情况下，请删除 *.csproj* 文件的所有内容，并将其替换为以下代码：

```xml
 <Project Sdk="Microsoft.NET.Sdk">
  <PropertyGroup>
    <OutputType>WinExe</OutputType>
    <TargetFramework>net5.0-windows</TargetFramework>
    <UseWpf>true</UseWpf>
    <GenerateAssemblyInfo>false</GenerateAssemblyInfo>
  </PropertyGroup>
</Project>
```

如果重新加载并编译该项目，则会收到以下错误：

![Visual Studio 上的编译错误的屏幕截图](./media/example-migration-core/wpf-compilation-error.png)

由于已删除所有 *.csproj* 内容，因此你丢失了旧项目中的项目引用规范。 只需将此行添加到 *.csproj* 文件，即可包含项目引用：

```xml
<ItemGroup>
    <ProjectReference Include="..\\eShop.SqlProvider\\eShop.SqlProvider.csproj" />
<ItemGroup>
```

还可以通过右键单击 " **依赖项** " 节点并选择 " **添加项目引用**" 来让 Visual Studio 帮助你。 从解决方案中选择项目，然后单击 **"确定"**：

![选择了 eShop SqlProvider 项目的 "引用管理器" 对话框的屏幕截图](./media/example-migration-core/reference-manager.png)

添加缺少的项目引用后，应用程序将在 .NET 上按预期方式编译和运行。

>[!div class="step-by-step"]
>[上一页](windows-migration.md)
>[下一页](deploy-modern-applications.md)
