---
title: Microsoft.NET.Sdk 的 MSBuild 属性
description: .NET SDK 可以理解的 MSBuild 属性和项的引用。
ms.date: 02/14/2020
ms.topic: reference
ms.custom: updateeachrelease
ms.openlocfilehash: e140491c694291438fe1db7fd60d581ffed0319d
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99802666"
---
# <a name="msbuild-reference-for-net-sdk-projects"></a><span data-ttu-id="c4859-103">.NET SDK 项目的 MSBuild 引用</span><span class="sxs-lookup"><span data-stu-id="c4859-103">MSBuild reference for .NET SDK projects</span></span>

<span data-ttu-id="c4859-104">此页是对可用于配置 .NET 项目的 MSBuild 属性和项的引用。</span><span class="sxs-lookup"><span data-stu-id="c4859-104">This page is a reference for the MSBuild properties and items that you can use to configure .NET projects.</span></span>

> [!NOTE]
> <span data-ttu-id="c4859-105">此页面正在运行中，未列出 .NET SDK 的所有有用的 MSBuild 属性。</span><span class="sxs-lookup"><span data-stu-id="c4859-105">This page is a work in progress and does not list all of the useful MSBuild properties for the .NET SDK.</span></span> <span data-ttu-id="c4859-106">有关通用 MSBuild 属性的列表，请参阅[通用 MSBuild 属性](/visualstudio/msbuild/common-msbuild-project-properties)。</span><span class="sxs-lookup"><span data-stu-id="c4859-106">For a list of common MSBuild properties, see [Common MSBuild properties](/visualstudio/msbuild/common-msbuild-project-properties).</span></span>

## <a name="framework-properties"></a><span data-ttu-id="c4859-107">框架属性</span><span class="sxs-lookup"><span data-stu-id="c4859-107">Framework properties</span></span>

- [<span data-ttu-id="c4859-108">TargetFramework</span><span class="sxs-lookup"><span data-stu-id="c4859-108">TargetFramework</span></span>](#targetframework)
- [<span data-ttu-id="c4859-109">TargetFrameworks</span><span class="sxs-lookup"><span data-stu-id="c4859-109">TargetFrameworks</span></span>](#targetframeworks)
- [<span data-ttu-id="c4859-110">NetStandardImplicitPackageVersion</span><span class="sxs-lookup"><span data-stu-id="c4859-110">NetStandardImplicitPackageVersion</span></span>](#netstandardimplicitpackageversion)

### <a name="targetframework"></a><span data-ttu-id="c4859-111">TargetFramework</span><span class="sxs-lookup"><span data-stu-id="c4859-111">TargetFramework</span></span>

<span data-ttu-id="c4859-112">`TargetFramework` 属性指定应用的目标框架版本。</span><span class="sxs-lookup"><span data-stu-id="c4859-112">The `TargetFramework` property specifies the target framework version for the app.</span></span> <span data-ttu-id="c4859-113">有关有效的目标框架名字对象的列表，请参阅 [SDK 样式项目中的目标框架](../../standard/frameworks.md#supported-target-frameworks)。</span><span class="sxs-lookup"><span data-stu-id="c4859-113">For a list of valid target framework monikers, see [Target frameworks in SDK-style projects](../../standard/frameworks.md#supported-target-frameworks).</span></span>

```xml
<PropertyGroup>
  <TargetFramework>netcoreapp3.1</TargetFramework>
</PropertyGroup>
```

<span data-ttu-id="c4859-114">有关详细信息，请参阅 [SDK 样式项目中的目标框架](../../standard/frameworks.md)。</span><span class="sxs-lookup"><span data-stu-id="c4859-114">For more information, see [Target frameworks in SDK-style projects](../../standard/frameworks.md).</span></span>

### <a name="targetframeworks"></a><span data-ttu-id="c4859-115">TargetFrameworks</span><span class="sxs-lookup"><span data-stu-id="c4859-115">TargetFrameworks</span></span>

<span data-ttu-id="c4859-116">如果希望应用面向多个平台，请使用 `TargetFrameworks` 属性。</span><span class="sxs-lookup"><span data-stu-id="c4859-116">Use the `TargetFrameworks` property when you want your app to target multiple platforms.</span></span> <span data-ttu-id="c4859-117">有关有效的目标框架名字对象的列表，请参阅 [SDK 样式项目中的目标框架](../../standard/frameworks.md#supported-target-frameworks)。</span><span class="sxs-lookup"><span data-stu-id="c4859-117">For a list of valid target framework monikers, see [Target frameworks in SDK-style projects](../../standard/frameworks.md#supported-target-frameworks).</span></span>

> [!NOTE]
> <span data-ttu-id="c4859-118">如果指定了 `TargetFramework`（单数），则忽略此属性。</span><span class="sxs-lookup"><span data-stu-id="c4859-118">This property is ignored if `TargetFramework` (singular) is specified.</span></span>

```xml
<PropertyGroup>
  <TargetFrameworks>netcoreapp3.1;net462</TargetFrameworks>
</PropertyGroup>
```

<span data-ttu-id="c4859-119">有关详细信息，请参阅 [SDK 样式项目中的目标框架](../../standard/frameworks.md)。</span><span class="sxs-lookup"><span data-stu-id="c4859-119">For more information, see [Target frameworks in SDK-style projects](../../standard/frameworks.md).</span></span>

### <a name="netstandardimplicitpackageversion"></a><span data-ttu-id="c4859-120">NetStandardImplicitPackageVersion</span><span class="sxs-lookup"><span data-stu-id="c4859-120">NetStandardImplicitPackageVersion</span></span>

> [!NOTE]
> <span data-ttu-id="c4859-121">此属性仅适用于使用 `netstandard1.x` 的项目。</span><span class="sxs-lookup"><span data-stu-id="c4859-121">This property only applies to projects using `netstandard1.x`.</span></span> <span data-ttu-id="c4859-122">它不适用于使用 `netstandard2.x` 的项目。</span><span class="sxs-lookup"><span data-stu-id="c4859-122">It doesn't apply to projects that use `netstandard2.x`.</span></span>

<span data-ttu-id="c4859-123">如果要指定低于元包版本的框架版本，请使用 `NetStandardImplicitPackageVersion` 属性。</span><span class="sxs-lookup"><span data-stu-id="c4859-123">Use the `NetStandardImplicitPackageVersion` property when you want to specify a framework version that's lower than the metapackage version.</span></span> <span data-ttu-id="c4859-124">以下示例中的项目文件以 `netstandard1.3` 为目标，但使用 `NETStandard.Library` 的 1.6.0 版本。</span><span class="sxs-lookup"><span data-stu-id="c4859-124">The project file in the following example targets `netstandard1.3` but uses the 1.6.0 version of `NETStandard.Library`.</span></span>

```xml
<PropertyGroup>
  <TargetFramework>netstandard1.3</TargetFramework>
  <NetStandardImplicitPackageVersion>1.6.0</NetStandardImplicitPackageVersion>
</PropertyGroup>
```

## <a name="package-properties"></a><span data-ttu-id="c4859-125">包属性</span><span class="sxs-lookup"><span data-stu-id="c4859-125">Package properties</span></span>

<span data-ttu-id="c4859-126">可以指定 `PackageId`、`PackageVersion`、`PackageIcon`、`Title` 和 `Description` 等属性来描述通过项目创建的包。</span><span class="sxs-lookup"><span data-stu-id="c4859-126">You can specify properties such as `PackageId`, `PackageVersion`, `PackageIcon`, `Title`, and `Description` to describe the package that gets created from your project.</span></span> <span data-ttu-id="c4859-127">若要了解这些属性和其他属性，请参阅[包目标](/nuget/reference/msbuild-targets#pack-target)。</span><span class="sxs-lookup"><span data-stu-id="c4859-127">For information about these and other properties, see [pack target](/nuget/reference/msbuild-targets#pack-target).</span></span>

```xml
<PropertyGroup>
  ...
  <PackageId>ClassLibDotNetStandard</PackageId>
  <Version>1.0.0</Version>
  <Authors>John Doe</Authors>
  <Company>Contoso</Company>
</PropertyGroup>
```

## <a name="publish-properties-items-and-metadata"></a><span data-ttu-id="c4859-128">发布属性、项和元数据</span><span class="sxs-lookup"><span data-stu-id="c4859-128">Publish properties, items, and metadata</span></span>

- [<span data-ttu-id="c4859-129">AppendRuntimeIdentifierToOutputPath</span><span class="sxs-lookup"><span data-stu-id="c4859-129">AppendRuntimeIdentifierToOutputPath</span></span>](#appendruntimeidentifiertooutputpath)
- [<span data-ttu-id="c4859-130">AppendTargetFrameworkToOutputPath</span><span class="sxs-lookup"><span data-stu-id="c4859-130">AppendTargetFrameworkToOutputPath</span></span>](#appendtargetframeworktooutputpath)
- [<span data-ttu-id="c4859-131">CopyLocalLockFileAssemblies</span><span class="sxs-lookup"><span data-stu-id="c4859-131">CopyLocalLockFileAssemblies</span></span>](#copylocallockfileassemblies)
- [<span data-ttu-id="c4859-132">CopyToPublishDirectory</span><span class="sxs-lookup"><span data-stu-id="c4859-132">CopyToPublishDirectory</span></span>](#copytopublishdirectory)
- [<span data-ttu-id="c4859-133">LinkBase</span><span class="sxs-lookup"><span data-stu-id="c4859-133">LinkBase</span></span>](#linkbase)
- [<span data-ttu-id="c4859-134">PreserveCompilationContext</span><span class="sxs-lookup"><span data-stu-id="c4859-134">PreserveCompilationContext</span></span>](#preservecompilationcontext)
- [<span data-ttu-id="c4859-135">PreserveCompilationReferences</span><span class="sxs-lookup"><span data-stu-id="c4859-135">PreserveCompilationReferences</span></span>](#preservecompilationreferences)
- [<span data-ttu-id="c4859-136">RuntimeIdentifier</span><span class="sxs-lookup"><span data-stu-id="c4859-136">RuntimeIdentifier</span></span>](#runtimeidentifier)
- [<span data-ttu-id="c4859-137">RuntimeIdentifiers</span><span class="sxs-lookup"><span data-stu-id="c4859-137">RuntimeIdentifiers</span></span>](#runtimeidentifiers)
- [<span data-ttu-id="c4859-138">TrimmerRootAssembly</span><span class="sxs-lookup"><span data-stu-id="c4859-138">TrimmerRootAssembly</span></span>](#trimmerrootassembly)
- [<span data-ttu-id="c4859-139">UseAppHost</span><span class="sxs-lookup"><span data-stu-id="c4859-139">UseAppHost</span></span>](#useapphost)

### <a name="copytopublishdirectory"></a><span data-ttu-id="c4859-140">CopyToPublishDirectory</span><span class="sxs-lookup"><span data-stu-id="c4859-140">CopyToPublishDirectory</span></span>

<span data-ttu-id="c4859-141">MSBuild 项上的 `CopyToPublishDirectory` 元数据控制何时将项复制到发布目录。</span><span class="sxs-lookup"><span data-stu-id="c4859-141">The `CopyToPublishDirectory` metadata on an MSBuild item controls when the item is copied to the publish directory.</span></span> <span data-ttu-id="c4859-142">允许的值为 `PreserveNewest`（仅在项已更改时复制项）、`Always`（始终复制项）和 `Never`（从不复制项）。</span><span class="sxs-lookup"><span data-stu-id="c4859-142">Allowable values are `PreserveNewest`, which only copies the item if it has changed, `Always`, which always copies the item, and `Never`, which never copies the item.</span></span> <span data-ttu-id="c4859-143">从性能角度来看，`PreserveNewest` 更为可取，因为它可实现增量生成。</span><span class="sxs-lookup"><span data-stu-id="c4859-143">From a performance standpoint, `PreserveNewest` is preferable because it enables an incremental build.</span></span>

```xml
<ItemGroup>
  <None Update="appsettings.Development.json" CopyToOutputDirectory="PreserveNewest" CopyToPublishDirectory="PreserveNewest" />
</ItemGroup>
```

### <a name="linkbase"></a><span data-ttu-id="c4859-144">LinkBase</span><span class="sxs-lookup"><span data-stu-id="c4859-144">LinkBase</span></span>

<span data-ttu-id="c4859-145">对于项目目录及其子目录之外的项，发布目标使用项的[链接元数据](/visualstudio/msbuild/common-msbuild-item-metadata)来确定要将项复制到的位置。</span><span class="sxs-lookup"><span data-stu-id="c4859-145">For an item that's outside of the project directory and its subdirectories, the publish target uses the item's [Link metadata](/visualstudio/msbuild/common-msbuild-item-metadata) to determine where to copy the item to.</span></span> <span data-ttu-id="c4859-146">`Link` 还将确定项目树外的项在 Visual Studio 的“解决方案资源管理器”窗口中的显示方式。</span><span class="sxs-lookup"><span data-stu-id="c4859-146">`Link` also determines how items outside of the project tree are displayed in the Solution Explorer window of Visual Studio.</span></span>

<span data-ttu-id="c4859-147">如果没有为项目圆锥之外的项指定 `Link`，则默认为 `%(LinkBase)\%(RecursiveDir)%(Filename)%(Extension)`。</span><span class="sxs-lookup"><span data-stu-id="c4859-147">If `Link` is not specified for an item that's outside of the project cone, it defaults to `%(LinkBase)\%(RecursiveDir)%(Filename)%(Extension)`.</span></span> <span data-ttu-id="c4859-148">通过 `LinkBase`，可以为项目圆锥之外的项指定一个合理的基础文件夹。</span><span class="sxs-lookup"><span data-stu-id="c4859-148">`LinkBase` lets you specify a sensible base folder for items outside of the project cone.</span></span> <span data-ttu-id="c4859-149">基础文件夹下的文件夹层次结构通过 `RecursiveDir` 保留。</span><span class="sxs-lookup"><span data-stu-id="c4859-149">The folder hierarchy under the base folder is preserved via `RecursiveDir`.</span></span> <span data-ttu-id="c4859-150">如果未指定 `LinkBase`，则将从 `Link` 路径中省略它。</span><span class="sxs-lookup"><span data-stu-id="c4859-150">If `LinkBase` is not specified, it's omitted from the `Link` path.</span></span>

```xml
<ItemGroup>
  <Content Include="..\Extras\**\*.cs" LinkBase="Shared"/>
</ItemGroup>
```

<span data-ttu-id="c4859-151">下图显示通过上一个项 `Include` glob 包含的文件在解决方案资源管理器中的显示方式。</span><span class="sxs-lookup"><span data-stu-id="c4859-151">The following image shows how a file that's included via the previous item `Include` glob displays in Solution Explorer.</span></span>

:::image type="content" source="media/solution-explorer-linkbase.png" alt-text="解决方案资源管理器，显示具有 LinkBase 元数据的项。":::

### <a name="appendtargetframeworktooutputpath"></a><span data-ttu-id="c4859-153">AppendTargetFrameworkToOutputPath</span><span class="sxs-lookup"><span data-stu-id="c4859-153">AppendTargetFrameworkToOutputPath</span></span>

<span data-ttu-id="c4859-154">`AppendTargetFrameworkToOutputPath` 属性控制是否将[目标框架名字对象 (TFM)](../../standard/frameworks.md) 追加到输出路径（由 [OutputPath](/visualstudio/msbuild/common-msbuild-project-properties#list-of-common-properties-and-parameters) 定义）。</span><span class="sxs-lookup"><span data-stu-id="c4859-154">The `AppendTargetFrameworkToOutputPath` property controls whether the [target framework moniker (TFM)](../../standard/frameworks.md) is appended to the output path (which is defined by [OutputPath](/visualstudio/msbuild/common-msbuild-project-properties#list-of-common-properties-and-parameters)).</span></span> <span data-ttu-id="c4859-155">.NET SDK 会自动将目标框架以及运行时标识符（如果有）追加到输出路径。</span><span class="sxs-lookup"><span data-stu-id="c4859-155">The .NET SDK automatically appends the target framework and, if present, the runtime identifier to the output path.</span></span> <span data-ttu-id="c4859-156">将 `AppendTargetFrameworkToOutputPath` 设置为 `false` 可防止将 TFM 追加到输出路径。</span><span class="sxs-lookup"><span data-stu-id="c4859-156">Setting `AppendTargetFrameworkToOutputPath` to `false` prevents the TFM from being appended to the output path.</span></span> <span data-ttu-id="c4859-157">但是，如果输出路径中没有 TFM，则可能会发生多个生成项目相互覆盖的情况。</span><span class="sxs-lookup"><span data-stu-id="c4859-157">However, without the TFM in the output path, multiple build artifacts may overwrite each other.</span></span>

<span data-ttu-id="c4859-158">例如，对于 .NET 5.0 应用，输出路径将从 `bin\Debug\net5.0` 更改为 `bin\Debug`，并具有以下设置：</span><span class="sxs-lookup"><span data-stu-id="c4859-158">For example, for a .NET 5.0 app, the output path changes from `bin\Debug\net5.0` to `bin\Debug` with the following setting:</span></span>

```xml
<PropertyGroup>
  <AppendTargetFrameworkToOutputPath>false</AppendTargetFrameworkToOutputPath>
</PropertyGroup>
```

### <a name="appendruntimeidentifiertooutputpath"></a><span data-ttu-id="c4859-159">AppendRuntimeIdentifierToOutputPath</span><span class="sxs-lookup"><span data-stu-id="c4859-159">AppendRuntimeIdentifierToOutputPath</span></span>

<span data-ttu-id="c4859-160">`AppendRuntimeIdentifierToOutputPath` 属性控制是否将[运行时标识符 (RID)](../rid-catalog.md) 追加到输出路径。</span><span class="sxs-lookup"><span data-stu-id="c4859-160">The `AppendRuntimeIdentifierToOutputPath` property controls whether the [runtime identifier (RID)](../rid-catalog.md) is appended to the output path.</span></span> <span data-ttu-id="c4859-161">.NET SDK 会自动将目标框架以及运行时标识符（如果有）追加到输出路径。</span><span class="sxs-lookup"><span data-stu-id="c4859-161">The .NET SDK automatically appends the target framework and, if present, the runtime identifier to the output path.</span></span> <span data-ttu-id="c4859-162">将 `AppendRuntimeIdentifierToOutputPath` 设置为 `false` 可防止将 RID 追加到输出路径。</span><span class="sxs-lookup"><span data-stu-id="c4859-162">Setting `AppendRuntimeIdentifierToOutputPath` to `false` prevents the RID from being appended to the output path.</span></span>

<span data-ttu-id="c4859-163">例如，对于 .NET 5.0 应用和 RID `win10-x64`，输出路径将从 `bin\Debug\net5.0\win10-x64` 更改为 `bin\Debug\net5.0`，并具有以下设置：</span><span class="sxs-lookup"><span data-stu-id="c4859-163">For example, for a .NET 5.0 app and an RID of `win10-x64`, the output path changes from `bin\Debug\net5.0\win10-x64` to `bin\Debug\net5.0` with the following setting:</span></span>

```xml
<PropertyGroup>
  <AppendRuntimeIdentifierToOutputPath>false</AppendRuntimeIdentifierToOutputPath>
</PropertyGroup>
```

### <a name="copylocallockfileassemblies"></a><span data-ttu-id="c4859-164">CopyLocalLockFileAssemblies</span><span class="sxs-lookup"><span data-stu-id="c4859-164">CopyLocalLockFileAssemblies</span></span>

<span data-ttu-id="c4859-165">对于依赖于其他库的插件项目，`CopyLocalLockFileAssemblies` 属性非常有用。</span><span class="sxs-lookup"><span data-stu-id="c4859-165">The `CopyLocalLockFileAssemblies` property is useful for plugin projects that have dependencies on other libraries.</span></span> <span data-ttu-id="c4859-166">如果将此属性设置为 `true`，系统会将所有 NuGet 包依赖项复制到输出目录。</span><span class="sxs-lookup"><span data-stu-id="c4859-166">If you set this property to `true`, any NuGet package dependencies are copied to the output directory.</span></span> <span data-ttu-id="c4859-167">这意味着，可以使用 `dotnet build` 的输出在任何计算机上运行插件。</span><span class="sxs-lookup"><span data-stu-id="c4859-167">That means you can use the output of `dotnet build` to run your plugin on any machine.</span></span>

```xml
<PropertyGroup>
  <CopyLocalLockFileAssemblies>true</CopyLocalLockFileAssemblies>
</PropertyGroup>
```

> [!TIP]
> <span data-ttu-id="c4859-168">或者，可以使用 `dotnet publish` 发布类库。</span><span class="sxs-lookup"><span data-stu-id="c4859-168">Alternatively, you can use `dotnet publish` to publish the class library.</span></span> <span data-ttu-id="c4859-169">有关详细信息，请查看 [dotnet publish](../tools/dotnet-publish.md)。</span><span class="sxs-lookup"><span data-stu-id="c4859-169">For more information, see [dotnet publish](../tools/dotnet-publish.md).</span></span>

### <a name="preservecompilationcontext"></a><span data-ttu-id="c4859-170">PreserveCompilationContext</span><span class="sxs-lookup"><span data-stu-id="c4859-170">PreserveCompilationContext</span></span>

<span data-ttu-id="c4859-171">`PreserveCompilationContext` 属性允许已构建或已发布的应用程序在运行时使用与构建时使用的相同设置来编译更多代码。</span><span class="sxs-lookup"><span data-stu-id="c4859-171">The `PreserveCompilationContext` property allows a built or published application to compile more code at run time using the same settings that were used at build time.</span></span> <span data-ttu-id="c4859-172">在构建时引用的程序集将被复制到输出目录的 ref 子目录中。</span><span class="sxs-lookup"><span data-stu-id="c4859-172">The assemblies referenced at build time will be copied into the *ref* subdirectory of the output directory.</span></span> <span data-ttu-id="c4859-173">引用程序集的名称与传递给编译器的选项一起存储在应用程序的 .deps.json 文件中。</span><span class="sxs-lookup"><span data-stu-id="c4859-173">The names of the reference assemblies are stored in the application's *.deps.json* file along with the options passed to the compiler.</span></span> <span data-ttu-id="c4859-174">可使用 <xref:Microsoft.Extensions.DependencyModel.DependencyContext.CompileLibraries?displayProperty=nameWithType> 和 <xref:Microsoft.Extensions.DependencyModel.DependencyContext.CompilationOptions?displayProperty=nameWithType> 属性检索此信息。</span><span class="sxs-lookup"><span data-stu-id="c4859-174">You can retrieve this information using the <xref:Microsoft.Extensions.DependencyModel.DependencyContext.CompileLibraries?displayProperty=nameWithType> and <xref:Microsoft.Extensions.DependencyModel.DependencyContext.CompilationOptions?displayProperty=nameWithType> properties.</span></span>

<span data-ttu-id="c4859-175">此功能主要由 ASP.NET Core MVC 和 Razor Pages 在内部使用，以支持 Razor文件的运行时编译。</span><span class="sxs-lookup"><span data-stu-id="c4859-175">This functionality is mostly used internally by ASP.NET Core MVC and Razor pages to support run-time compilation of Razor files.</span></span>

```xml
<PropertyGroup>
  <PreserveCompilationContext>true</PreserveCompilationContext>
</PropertyGroup>
```

### <a name="preservecompilationreferences"></a><span data-ttu-id="c4859-176">PreserveCompilationReferences</span><span class="sxs-lookup"><span data-stu-id="c4859-176">PreserveCompilationReferences</span></span>

<span data-ttu-id="c4859-177">`PreserveCompilationReferences` 属性与 [PreserveCompilationContext](#preservecompilationcontext) 属性类似，只不过它仅将引用的程序集复制到发布目录，而不是 .deps.json 文件。</span><span class="sxs-lookup"><span data-stu-id="c4859-177">The `PreserveCompilationReferences` property is similar to the [PreserveCompilationContext](#preservecompilationcontext) property, except that it only copies the referenced assemblies to the publish directory, and not the *.deps.json* file.</span></span>

```xml
<PropertyGroup>
  <PreserveCompilationReferences>true</PreserveCompilationReferences>
</PropertyGroup>
```

<span data-ttu-id="c4859-178">有关详细信息，请参阅 [Razor SDK 属性](/aspnet/core/razor-pages/sdk#properties)。</span><span class="sxs-lookup"><span data-stu-id="c4859-178">For more information, see [Razor SDK properties](/aspnet/core/razor-pages/sdk#properties).</span></span>

### <a name="runtimeidentifier"></a><span data-ttu-id="c4859-179">RuntimeIdentifier</span><span class="sxs-lookup"><span data-stu-id="c4859-179">RuntimeIdentifier</span></span>

<span data-ttu-id="c4859-180">`RuntimeIdentifier` 属性可用于指定项目的单个[运行时标识符 (RID)](../rid-catalog.md)。</span><span class="sxs-lookup"><span data-stu-id="c4859-180">The `RuntimeIdentifier` property lets you specify a single [runtime identifier (RID)](../rid-catalog.md) for the project.</span></span> <span data-ttu-id="c4859-181">RID 支持发布独立部署。</span><span class="sxs-lookup"><span data-stu-id="c4859-181">The RID enables publishing a self-contained deployment.</span></span>

```xml
<PropertyGroup>
  <RuntimeIdentifier>ubuntu.16.04-x64</RuntimeIdentifier>
</PropertyGroup>
```

### <a name="runtimeidentifiers"></a><span data-ttu-id="c4859-182">RuntimeIdentifiers</span><span class="sxs-lookup"><span data-stu-id="c4859-182">RuntimeIdentifiers</span></span>

<span data-ttu-id="c4859-183">`RuntimeIdentifiers` 属性可用于指定项目的[运行时标识符 (RID)](../rid-catalog.md) 的列表（以分号分隔）。</span><span class="sxs-lookup"><span data-stu-id="c4859-183">The `RuntimeIdentifiers` property lets you specify a semicolon-delimited list of [runtime identifiers (RIDs)](../rid-catalog.md) for the project.</span></span> <span data-ttu-id="c4859-184">如果需要为多个运行时发布，请使用此属性。</span><span class="sxs-lookup"><span data-stu-id="c4859-184">Use this property if you need to publish for multiple runtimes.</span></span> <span data-ttu-id="c4859-185">`RuntimeIdentifiers` 在还原时使用，以确保图中有适当的资产。</span><span class="sxs-lookup"><span data-stu-id="c4859-185">`RuntimeIdentifiers` is used at restore time to ensure the right assets are in the graph.</span></span>

> [!TIP]
> <span data-ttu-id="c4859-186">`RuntimeIdentifier`（单数）可以在只需要一个运行时时提供更快的生成。</span><span class="sxs-lookup"><span data-stu-id="c4859-186">`RuntimeIdentifier` (singular) can provide faster builds when only a single runtime is required.</span></span>

```xml
<PropertyGroup>
  <RuntimeIdentifiers>win10-x64;osx.10.11-x64;ubuntu.16.04-x64</RuntimeIdentifiers>
</PropertyGroup>
```

### <a name="trimmerrootassembly"></a><span data-ttu-id="c4859-187">TrimmerRootAssembly</span><span class="sxs-lookup"><span data-stu-id="c4859-187">TrimmerRootAssembly</span></span>

<span data-ttu-id="c4859-188">`TrimmerRootAssembly` 项允许通过[修整](../deploying/trim-self-contained.md)排除程序集。</span><span class="sxs-lookup"><span data-stu-id="c4859-188">The `TrimmerRootAssembly` item lets you exclude an assembly from [*trimming*](../deploying/trim-self-contained.md).</span></span> <span data-ttu-id="c4859-189">修整是从打包的应用程序中删除运行时未使用部分的过程。</span><span class="sxs-lookup"><span data-stu-id="c4859-189">Trimming is the process of removing unused parts of the runtime from a packaged application.</span></span> <span data-ttu-id="c4859-190">在某些情况下，修整可能会错误地删除所需的引用。</span><span class="sxs-lookup"><span data-stu-id="c4859-190">In some cases, trimming might incorrectly remove required references.</span></span>

<span data-ttu-id="c4859-191">以下 XML 通过修整排除 `System.Security` 程序集。</span><span class="sxs-lookup"><span data-stu-id="c4859-191">The following XML excludes the `System.Security` assembly from trimming.</span></span>

```xml
<ItemGroup>
  <TrimmerRootAssembly Include="System.Security" />
</ItemGroup>
```

### <a name="useapphost"></a><span data-ttu-id="c4859-192">UseAppHost</span><span class="sxs-lookup"><span data-stu-id="c4859-192">UseAppHost</span></span>

<span data-ttu-id="c4859-193">`UseAppHost` 属性控制是否为部署创建本机可执行文件。</span><span class="sxs-lookup"><span data-stu-id="c4859-193">The `UseAppHost` property controls whether or not a native executable is created for a deployment.</span></span> <span data-ttu-id="c4859-194">自包含部署需要本机可执行文件。</span><span class="sxs-lookup"><span data-stu-id="c4859-194">A native executable is required for self-contained deployments.</span></span>

<span data-ttu-id="c4859-195">在 .NET Core3.0 及更高版本中，默认情况下会创建依赖于框架的可执行文件。</span><span class="sxs-lookup"><span data-stu-id="c4859-195">In .NET Core 3.0 and later versions, a framework-dependent executable is created by default.</span></span> <span data-ttu-id="c4859-196">将 `UseAppHost` 属性设置为 `false` 可禁用可执行文件的生成。</span><span class="sxs-lookup"><span data-stu-id="c4859-196">Set the `UseAppHost` property to `false` to disable generation of the executable.</span></span>

```xml
<PropertyGroup>
  <UseAppHost>false</UseAppHost>
</PropertyGroup>
```

<span data-ttu-id="c4859-197">有关部署的详细信息，请参阅 [.NET 应用程序部署](../deploying/index.md)。</span><span class="sxs-lookup"><span data-stu-id="c4859-197">For more information about deployment, see [.NET application deployment](../deploying/index.md).</span></span>

## <a name="compile-properties"></a><span data-ttu-id="c4859-198">编译属性</span><span class="sxs-lookup"><span data-stu-id="c4859-198">Compile properties</span></span>

- [<span data-ttu-id="c4859-199">EmbeddedResourceUseDependentUponConvention</span><span class="sxs-lookup"><span data-stu-id="c4859-199">EmbeddedResourceUseDependentUponConvention</span></span>](#embeddedresourceusedependentuponconvention)
- [<span data-ttu-id="c4859-200">LangVersion</span><span class="sxs-lookup"><span data-stu-id="c4859-200">LangVersion</span></span>](#langversion)

### <a name="embeddedresourceusedependentuponconvention"></a><span data-ttu-id="c4859-201">EmbeddedResourceUseDependentUponConvention</span><span class="sxs-lookup"><span data-stu-id="c4859-201">EmbeddedResourceUseDependentUponConvention</span></span>

<span data-ttu-id="c4859-202">`EmbeddedResourceUseDependentUponConvention` 属性定义了是否从与资源文件并置的源文件中的类型信息生成资源清单文件名。</span><span class="sxs-lookup"><span data-stu-id="c4859-202">The `EmbeddedResourceUseDependentUponConvention` property defines whether resource manifest file names are generated from type information in source files that are colocated with resource files.</span></span> <span data-ttu-id="c4859-203">例如，如果 Form1.resx 与 Form1.cs 位于同一文件夹中，并且 `EmbeddedResourceUseDependentUponConvention` 设置为 `true`，则生成的 .resources 文件将采用 Form1.cs 中定义的第一个类型的名称作为其文件名。</span><span class="sxs-lookup"><span data-stu-id="c4859-203">For example, if *Form1.resx* is in the same folder as *Form1.cs*, and `EmbeddedResourceUseDependentUponConvention` is set to `true`, the generated *.resources* file takes its name from the first type that's defined in *Form1.cs*.</span></span> <span data-ttu-id="c4859-204">例如，如果 Form1.cs 中定义的第一个类型为 `MyNamespace.Form1`，则生成的文件名为 MyNamespace.Form1.resources。</span><span class="sxs-lookup"><span data-stu-id="c4859-204">For example, if `MyNamespace.Form1` is the first type defined in *Form1.cs*, the generated file name is *MyNamespace.Form1.resources*.</span></span>

> [!NOTE]
> <span data-ttu-id="c4859-205">如果为 `EmbeddedResource` 项指定 `LogicalName`、`ManifestResourceName` 或 `DependentUpon` 元数据，则为该资源文件生成的清单文件名将改为基于该元数据。</span><span class="sxs-lookup"><span data-stu-id="c4859-205">If `LogicalName`, `ManifestResourceName`, or `DependentUpon` metadata is specified for an `EmbeddedResource` item, the generated manifest file name for that resource file is based on that metadata instead.</span></span>

<span data-ttu-id="c4859-206">默认情况下，在新的 .NET 项目中，此属性设置为 `true`。</span><span class="sxs-lookup"><span data-stu-id="c4859-206">By default, in a new .NET project, this property is set to `true`.</span></span> <span data-ttu-id="c4859-207">如果设置为 `false`，并且没有为项目文件中的 `EmbeddedResource` 项指定 `LogicalName`、`ManifestResourceName` 或 `DependentUpon` 元数据，则资源清单文件名将基于项目的根命名空间和 .resx 文件的相对文件路径。</span><span class="sxs-lookup"><span data-stu-id="c4859-207">If set to `false`, and no `LogicalName`, `ManifestResourceName`, or `DependentUpon` metadata is specified for the `EmbeddedResource` item in the project file, the resource manifest file name is based off the root namespace for the project and the relative file path to the *.resx* file.</span></span> <span data-ttu-id="c4859-208">有关详细信息，请参阅[资源清单文件的命名](../resources/manifest-file-names.md)。</span><span class="sxs-lookup"><span data-stu-id="c4859-208">For more information, see [How resource manifest files are named](../resources/manifest-file-names.md).</span></span>

```xml
<PropertyGroup>
  <EmbeddedResourceUseDependentUponConvention>true</EmbeddedResourceUseDependentUponConvention>
</PropertyGroup>
```

### <a name="langversion"></a><span data-ttu-id="c4859-209">LangVersion</span><span class="sxs-lookup"><span data-stu-id="c4859-209">LangVersion</span></span>

<span data-ttu-id="c4859-210">`LangVersion` 属性可用于指定特定的编程语言版本。</span><span class="sxs-lookup"><span data-stu-id="c4859-210">The `LangVersion` property lets you specify a specific programming language version.</span></span> <span data-ttu-id="c4859-211">例如，如果要访问 C# 预览功能，请将 `LangVersion` 设置为 `preview`。</span><span class="sxs-lookup"><span data-stu-id="c4859-211">For example, if you want access to C# preview features, set `LangVersion` to `preview`.</span></span>

```xml
<PropertyGroup>
  <LangVersion>preview</LangVersion>
</PropertyGroup>
```

<span data-ttu-id="c4859-212">有关详细信息，请参阅 [C# 语言版本控制](../../csharp/language-reference/configure-language-version.md#override-a-default)。</span><span class="sxs-lookup"><span data-stu-id="c4859-212">For more information, see [C# language versioning](../../csharp/language-reference/configure-language-version.md#override-a-default).</span></span>

## <a name="default-item-inclusion-properties"></a><span data-ttu-id="c4859-213">默认项包含属性</span><span class="sxs-lookup"><span data-stu-id="c4859-213">Default item inclusion properties</span></span>

- [<span data-ttu-id="c4859-214">DefaultExcludesInProjectFolder</span><span class="sxs-lookup"><span data-stu-id="c4859-214">DefaultExcludesInProjectFolder</span></span>](#defaultexcludesinprojectfolder)
- [<span data-ttu-id="c4859-215">DefaultItemExcludes</span><span class="sxs-lookup"><span data-stu-id="c4859-215">DefaultItemExcludes</span></span>](#defaultitemexcludes)
- [<span data-ttu-id="c4859-216">EnableDefaultCompileItems</span><span class="sxs-lookup"><span data-stu-id="c4859-216">EnableDefaultCompileItems</span></span>](#enabledefaultcompileitems)
- [<span data-ttu-id="c4859-217">EnableDefaultEmbeddedResourceItems</span><span class="sxs-lookup"><span data-stu-id="c4859-217">EnableDefaultEmbeddedResourceItems</span></span>](#enabledefaultembeddedresourceitems)
- [<span data-ttu-id="c4859-218">EnableDefaultItems</span><span class="sxs-lookup"><span data-stu-id="c4859-218">EnableDefaultItems</span></span>](#enabledefaultitems)
- [<span data-ttu-id="c4859-219">EnableDefaultNoneItems</span><span class="sxs-lookup"><span data-stu-id="c4859-219">EnableDefaultNoneItems</span></span>](#enabledefaultnoneitems)

<span data-ttu-id="c4859-220">有关详细信息，请参阅[默认的包括和排除](overview.md#default-includes-and-excludes)。</span><span class="sxs-lookup"><span data-stu-id="c4859-220">For more information, see [Default includes and excludes](overview.md#default-includes-and-excludes).</span></span>

### <a name="defaultitemexcludes"></a><span data-ttu-id="c4859-221">DefaultItemExcludes</span><span class="sxs-lookup"><span data-stu-id="c4859-221">DefaultItemExcludes</span></span>

<span data-ttu-id="c4859-222">使用 `DefaultItemExcludes` 属性定义需从“包括”、“排除”和“删除”glob 中排除的文件和文件夹的 glob 模式。</span><span class="sxs-lookup"><span data-stu-id="c4859-222">Use the `DefaultItemExcludes` property to define glob patterns for files and folders that should be excluded from the include, exclude, and remove globs.</span></span> <span data-ttu-id="c4859-223">默认情况下从 glob 模式中排除 ./bin 和 ./obj 文件夹 。</span><span class="sxs-lookup"><span data-stu-id="c4859-223">By default, the *./bin* and *./obj* folders are excluded from the glob patterns.</span></span>

```xml
<PropertyGroup>
  <DefaultItemExcludes>$(DefaultItemExcludes);**/*.myextension</DefaultItemExcludes>
</PropertyGroup>
```

### <a name="defaultexcludesinprojectfolder"></a><span data-ttu-id="c4859-224">DefaultExcludesInProjectFolder</span><span class="sxs-lookup"><span data-stu-id="c4859-224">DefaultExcludesInProjectFolder</span></span>

<span data-ttu-id="c4859-225">使用 `DefaultExcludesInProjectFolder` 属性定义项目文件夹中需要从“包括”、“排除”和“删除”glob 中排除的文件和文件夹的 glob 模式。</span><span class="sxs-lookup"><span data-stu-id="c4859-225">Use the `DefaultExcludesInProjectFolder` property to define glob patterns for files and folders in the project folder that should be excluded from the include, exclude, and remove globs.</span></span> <span data-ttu-id="c4859-226">默认情况下，从 glob 模式中排除以句点 (`.`) 开头的文件夹，如 .git 和 .vs。</span><span class="sxs-lookup"><span data-stu-id="c4859-226">By default, folders that start with a period (`.`), such as *.git* and *.vs*, are excluded from the glob patterns.</span></span>

<span data-ttu-id="c4859-227">此属性与 `DefaultItemExcludes` 属性非常相似，不同之处在于它只涉及项目文件夹中的文件和文件夹。</span><span class="sxs-lookup"><span data-stu-id="c4859-227">This property is very similar to the `DefaultItemExcludes` property, except that it only considers files and folders in the project folder.</span></span> <span data-ttu-id="c4859-228">如果 glob 模式会无意中将项目文件夹外部的项与相对路径进行匹配，请使用 `DefaultExcludesInProjectFolder` 属性，而不是 `DefaultItemExcludes` 属性。</span><span class="sxs-lookup"><span data-stu-id="c4859-228">When a glob pattern would unintentionally match items outside the project folder with a relative path, use the `DefaultExcludesInProjectFolder` property instead of the `DefaultItemExcludes` property.</span></span>

```xml
<PropertyGroup>
  <DefaultExcludesInProjectFolder>$(DefaultExcludesInProjectFolder);**/myprefix*/**</DefaultExcludesInProjectFolder>
</PropertyGroup>
```

### <a name="enabledefaultitems"></a><span data-ttu-id="c4859-229">EnableDefaultItems</span><span class="sxs-lookup"><span data-stu-id="c4859-229">EnableDefaultItems</span></span>

<span data-ttu-id="c4859-230">`EnableDefaultItems` 属性控制是否在项目中隐式包含编译项、嵌入的资源项和 `None` 项。</span><span class="sxs-lookup"><span data-stu-id="c4859-230">The `EnableDefaultItems` property controls whether compile items, embedded resource items, and `None` items are implicitly included in the project.</span></span> <span data-ttu-id="c4859-231">默认值为 `true`。</span><span class="sxs-lookup"><span data-stu-id="c4859-231">The default value is `true`.</span></span> <span data-ttu-id="c4859-232">若要禁用所有隐式文件包含，请将 `EnableDefaultItems` 属性设置为 `false`。</span><span class="sxs-lookup"><span data-stu-id="c4859-232">Set the `EnableDefaultItems` property to `false` to disable all implicit file inclusion.</span></span>

```xml
<PropertyGroup>
  <EnableDefaultItems>false</EnableDefaultItems>
</PropertyGroup>
```

### <a name="enabledefaultcompileitems"></a><span data-ttu-id="c4859-233">EnableDefaultCompileItems</span><span class="sxs-lookup"><span data-stu-id="c4859-233">EnableDefaultCompileItems</span></span>

<span data-ttu-id="c4859-234">`EnableDefaultCompileItems` 属性控制是否在项目中隐式包含编译项。</span><span class="sxs-lookup"><span data-stu-id="c4859-234">The `EnableDefaultCompileItems` property controls whether compile items are implicitly included in the project.</span></span> <span data-ttu-id="c4859-235">默认值为 `true`。</span><span class="sxs-lookup"><span data-stu-id="c4859-235">The default value is `true`.</span></span> <span data-ttu-id="c4859-236">将 `EnableDefaultCompileItems` 属性设置为 `false` 以禁用 \* .cs 和其他语言扩展文件的隐式包含。</span><span class="sxs-lookup"><span data-stu-id="c4859-236">Set the `EnableDefaultCompileItems` property to `false` to disable implicit inclusion of \*.cs and other language-extension files.</span></span>

```xml
<PropertyGroup>
  <EnableDefaultCompileItems>false</EnableDefaultCompileItems>
</PropertyGroup>
```

### <a name="enabledefaultembeddedresourceitems"></a><span data-ttu-id="c4859-237">EnableDefaultEmbeddedResourceItems</span><span class="sxs-lookup"><span data-stu-id="c4859-237">EnableDefaultEmbeddedResourceItems</span></span>

<span data-ttu-id="c4859-238">`EnableDefaultEmbeddedResourceItems` 属性控制是否在项目中隐式包含嵌入的资源项。</span><span class="sxs-lookup"><span data-stu-id="c4859-238">The `EnableDefaultEmbeddedResourceItems` property controls whether embedded resource items are implicitly included in the project.</span></span> <span data-ttu-id="c4859-239">默认值为 `true`。</span><span class="sxs-lookup"><span data-stu-id="c4859-239">The default value is `true`.</span></span> <span data-ttu-id="c4859-240">将 `EnableDefaultEmbeddedResourceItems` 属性设置为 `false` 以禁用嵌入的资源文件的隐式包含。</span><span class="sxs-lookup"><span data-stu-id="c4859-240">Set the `EnableDefaultEmbeddedResourceItems` property to `false` to disable implicit inclusion of embedded resource files.</span></span>

```xml
<PropertyGroup>
  <EnableDefaultEmbeddedResourceItems>false</EnableDefaultEmbeddedResourceItems>
</PropertyGroup>
```

### <a name="enabledefaultnoneitems"></a><span data-ttu-id="c4859-241">EnableDefaultNoneItems</span><span class="sxs-lookup"><span data-stu-id="c4859-241">EnableDefaultNoneItems</span></span>

<span data-ttu-id="c4859-242">`EnableDefaultNoneItems` 属性控制是否在项目中隐式包含 `None` 项（生成过程中未赋予角色的文件）。</span><span class="sxs-lookup"><span data-stu-id="c4859-242">The `EnableDefaultNoneItems` property controls whether `None` items (files that have no role in the build process) are implicitly included in the project.</span></span> <span data-ttu-id="c4859-243">默认值为 `true`。</span><span class="sxs-lookup"><span data-stu-id="c4859-243">The default value is `true`.</span></span> <span data-ttu-id="c4859-244">将 `EnableDefaultNoneItems` 属性设置为 `false` 以禁用 `None` 项的隐式包含。</span><span class="sxs-lookup"><span data-stu-id="c4859-244">Set the `EnableDefaultNoneItems` property to `false` to disable implicit inclusion of `None` items.</span></span>

```xml
<PropertyGroup>
  <EnableDefaultNoneItems>false</EnableDefaultNoneItems>
</PropertyGroup>
```

## <a name="code-analysis-properties"></a><span data-ttu-id="c4859-245">代码分析属性</span><span class="sxs-lookup"><span data-stu-id="c4859-245">Code analysis properties</span></span>

- [<span data-ttu-id="c4859-246">AnalysisLevel</span><span class="sxs-lookup"><span data-stu-id="c4859-246">AnalysisLevel</span></span>](#analysislevel)
- [<span data-ttu-id="c4859-247">AnalysisMode</span><span class="sxs-lookup"><span data-stu-id="c4859-247">AnalysisMode</span></span>](#analysismode)
- [<span data-ttu-id="c4859-248">CodeAnalysisTreatWarningsAsErrors</span><span class="sxs-lookup"><span data-stu-id="c4859-248">CodeAnalysisTreatWarningsAsErrors</span></span>](#codeanalysistreatwarningsaserrors)
- [<span data-ttu-id="c4859-249">EnableNETAnalyzers</span><span class="sxs-lookup"><span data-stu-id="c4859-249">EnableNETAnalyzers</span></span>](#enablenetanalyzers)
- [<span data-ttu-id="c4859-250">EnforceCodeStyleInBuild</span><span class="sxs-lookup"><span data-stu-id="c4859-250">EnforceCodeStyleInBuild</span></span>](#enforcecodestyleinbuild)

### <a name="analysislevel"></a><span data-ttu-id="c4859-251">AnalysisLevel</span><span class="sxs-lookup"><span data-stu-id="c4859-251">AnalysisLevel</span></span>

<span data-ttu-id="c4859-252">`AnalysisLevel` 属性可指定代码分析级别。</span><span class="sxs-lookup"><span data-stu-id="c4859-252">The `AnalysisLevel` property lets you specify a code analysis level.</span></span> <span data-ttu-id="c4859-253">例如，如果要访问预览代码分析器，请将 `AnalysisLevel` 设置为 `preview`。</span><span class="sxs-lookup"><span data-stu-id="c4859-253">For example, if you want access to preview code analyzers, set `AnalysisLevel` to `preview`.</span></span>

<span data-ttu-id="c4859-254">默认值：</span><span class="sxs-lookup"><span data-stu-id="c4859-254">Default value:</span></span>

- <span data-ttu-id="c4859-255">如果你的项目以 .NET 5.0 或更高版本为目标，或你添加了 [AnalysisMode](#analysismode) 属性，则默认值为 `latest`。</span><span class="sxs-lookup"><span data-stu-id="c4859-255">If your project targets .NET 5.0 or later, or if you've added the [AnalysisMode](#analysismode) property, the default value is `latest`.</span></span>
- <span data-ttu-id="c4859-256">否则，此属性被省略，除非你将它明确添加到项目文件中。</span><span class="sxs-lookup"><span data-stu-id="c4859-256">Otherwise, this property is omitted unless you explicitly add it to the project file.</span></span>

```xml
<PropertyGroup>
  <AnalysisLevel>preview</AnalysisLevel>
</PropertyGroup>
```

<span data-ttu-id="c4859-257">下表显示可用的选项。</span><span class="sxs-lookup"><span data-stu-id="c4859-257">The following table shows the available options.</span></span>

| <span data-ttu-id="c4859-258">值</span><span class="sxs-lookup"><span data-stu-id="c4859-258">Value</span></span> | <span data-ttu-id="c4859-259">含义</span><span class="sxs-lookup"><span data-stu-id="c4859-259">Meaning</span></span> |
|-|-|
| `latest` | <span data-ttu-id="c4859-260">使用已发布的最新版代码分析器。</span><span class="sxs-lookup"><span data-stu-id="c4859-260">The latest code analyzers that have been released are used.</span></span> <span data-ttu-id="c4859-261">这是默认值。</span><span class="sxs-lookup"><span data-stu-id="c4859-261">This is the default.</span></span> |
| `preview` | <span data-ttu-id="c4859-262">使用最新的代码分析器（即使它们处于预览状态）。</span><span class="sxs-lookup"><span data-stu-id="c4859-262">The latest code analyzers are used, even if they are in preview.</span></span> |
| `5.0` | <span data-ttu-id="c4859-263">即使有较新的规则可用，也会使用为 .NET 5.0 版本启用的规则集。</span><span class="sxs-lookup"><span data-stu-id="c4859-263">The set of rules that was enabled for the .NET 5.0 release is used, even if newer rules are available.</span></span> |
| `5` | <span data-ttu-id="c4859-264">即使有较新的规则可用，也会使用为 .NET 5.0 版本启用的规则集。</span><span class="sxs-lookup"><span data-stu-id="c4859-264">The set of rules that was enabled for the .NET 5.0 release is used, even if newer rules are available.</span></span> |

### <a name="analysismode"></a><span data-ttu-id="c4859-265">AnalysisMode</span><span class="sxs-lookup"><span data-stu-id="c4859-265">AnalysisMode</span></span>

<span data-ttu-id="c4859-266">从 .NET 5.0 开始，.NET SDK 附带了所有[“CA”代码质量规则](../../fundamentals/code-analysis/quality-rules/index.md)。</span><span class="sxs-lookup"><span data-stu-id="c4859-266">Starting with .NET 5.0, the .NET SDK ships with all of the ["CA" code quality rules](../../fundamentals/code-analysis/quality-rules/index.md).</span></span> <span data-ttu-id="c4859-267">默认情况下，只有[一些规则作为生成警告启用](../../fundamentals/code-analysis/overview.md#enabled-rules)。</span><span class="sxs-lookup"><span data-stu-id="c4859-267">By default, only [some rules are enabled](../../fundamentals/code-analysis/overview.md#enabled-rules) as build warnings.</span></span> <span data-ttu-id="c4859-268">`AnalysisMode` 属性允许自定义默认启用的一组规则。</span><span class="sxs-lookup"><span data-stu-id="c4859-268">The `AnalysisMode` property lets you customize the set of rules that are enabled by default.</span></span> <span data-ttu-id="c4859-269">可以切换到更主动的（选择退出）分析模式，也可以切换到更保守的（选择加入）分析模式。</span><span class="sxs-lookup"><span data-stu-id="c4859-269">You can either switch to a more aggressive (opt-out) analysis mode or a more conservative (opt-in) analysis mode.</span></span> <span data-ttu-id="c4859-270">例如，如果要作为生成警告默认启用所有规则，请将值设置为 `AllEnabledByDefault`。</span><span class="sxs-lookup"><span data-stu-id="c4859-270">For example, if you want to enable all rules by default as build warnings, set the value to `AllEnabledByDefault`.</span></span>

```xml
<PropertyGroup>
  <AnalysisMode>AllEnabledByDefault</AnalysisMode>
</PropertyGroup>
```

<span data-ttu-id="c4859-271">下表显示可用的选项。</span><span class="sxs-lookup"><span data-stu-id="c4859-271">The following table shows the available options.</span></span>

| <span data-ttu-id="c4859-272">值</span><span class="sxs-lookup"><span data-stu-id="c4859-272">Value</span></span> | <span data-ttu-id="c4859-273">含义</span><span class="sxs-lookup"><span data-stu-id="c4859-273">Meaning</span></span> |
|-|-|
| `Default` | <span data-ttu-id="c4859-274">默认模式，其中某些规则作为生成警告启用，某些规则作为 Visual Studio IDE 建议启用，其余规则被禁用。</span><span class="sxs-lookup"><span data-stu-id="c4859-274">Default mode, where certain rules are enabled as build warnings, certain rules are enabled as Visual Studio IDE suggestions, and the remainder are disabled.</span></span> |
| `AllEnabledByDefault` | <span data-ttu-id="c4859-275">主动或选择退出模式，默认情况下所有规则都作为生成警告启用。</span><span class="sxs-lookup"><span data-stu-id="c4859-275">Aggressive or opt-out mode, where all rules are enabled by default as build warnings.</span></span> <span data-ttu-id="c4859-276">可以选择[选择退出](../../fundamentals/code-analysis/configuration-options.md)各条规则，以禁用它们。</span><span class="sxs-lookup"><span data-stu-id="c4859-276">You can selectively [opt out](../../fundamentals/code-analysis/configuration-options.md) of individual rules to disable them.</span></span> |
| `AllDisabledByDefault` | <span data-ttu-id="c4859-277">保守或选择加入模式，默认情况下所有规则都处于禁用状态。</span><span class="sxs-lookup"><span data-stu-id="c4859-277">Conservative or opt-in mode, where all rules are disabled by default.</span></span> <span data-ttu-id="c4859-278">可以选择[选择加入](../../fundamentals/code-analysis/configuration-options.md)各条规则，以启用它们。</span><span class="sxs-lookup"><span data-stu-id="c4859-278">You can selectively [opt into](../../fundamentals/code-analysis/configuration-options.md) individual rules to enable them.</span></span> |

### <a name="codeanalysistreatwarningsaserrors"></a><span data-ttu-id="c4859-279">CodeAnalysisTreatWarningsAsErrors</span><span class="sxs-lookup"><span data-stu-id="c4859-279">CodeAnalysisTreatWarningsAsErrors</span></span>

<span data-ttu-id="c4859-280">`CodeAnalysisTreatWarningsAsErrors` 属性可配置是否应将代码质量分析警告 (CAxxxx) 视为警告并中断生成。</span><span class="sxs-lookup"><span data-stu-id="c4859-280">The `CodeAnalysisTreatWarningsAsErrors` property lets you configure whether code quality analysis warnings (CAxxxx) should be treated as warnings and break the build.</span></span> <span data-ttu-id="c4859-281">如果在生成项目时使用 `-warnaserror` 标志，则 [.NET 代码质量分析](../../fundamentals/code-analysis/overview.md#code-quality-analysis)警告也会被视为错误。</span><span class="sxs-lookup"><span data-stu-id="c4859-281">If you use the `-warnaserror` flag when you build your projects, [.NET code quality analysis](../../fundamentals/code-analysis/overview.md#code-quality-analysis) warnings are also treated as errors.</span></span> <span data-ttu-id="c4859-282">如果不希望将代码质量分析警告视为错误，可以在项目文件中将 `CodeAnalysisTreatWarningsAsErrors` MSBuild 属性设置为 `false`。</span><span class="sxs-lookup"><span data-stu-id="c4859-282">If you do not want code quality analysis warnings to be treated as errors, you can set the `CodeAnalysisTreatWarningsAsErrors` MSBuild property to `false` in your project file.</span></span>

```xml
<PropertyGroup>
  <CodeAnalysisTreatWarningsAsErrors>false</CodeAnalysisTreatWarningsAsErrors>
</PropertyGroup>
```

### <a name="enablenetanalyzers"></a><span data-ttu-id="c4859-283">EnableNETAnalyzers</span><span class="sxs-lookup"><span data-stu-id="c4859-283">EnableNETAnalyzers</span></span>

<span data-ttu-id="c4859-284">默认情况下，为面向 .NET 5.0 或更高版本的项目启用 [.NET 代码质量分析](../../fundamentals/code-analysis/overview.md#code-quality-analysis)。</span><span class="sxs-lookup"><span data-stu-id="c4859-284">[.NET code quality analysis](../../fundamentals/code-analysis/overview.md#code-quality-analysis) is enabled, by default, for projects that target .NET 5.0 or later.</span></span> <span data-ttu-id="c4859-285">可通过将 `EnableNETAnalyzers` 属性设置为 `true`，来为面向 .NET 早期版本的项目启用 .NET 代码分析。</span><span class="sxs-lookup"><span data-stu-id="c4859-285">You can enable .NET code analysis for projects that target earlier versions of .NET by setting the `EnableNETAnalyzers` property to `true`.</span></span> <span data-ttu-id="c4859-286">若要禁用任何项目中的代码分析，可将此属性设置为 `false`。</span><span class="sxs-lookup"><span data-stu-id="c4859-286">To disable code analysis in any project, set this property to `false`.</span></span>

```xml
<PropertyGroup>
  <EnableNETAnalyzers>true</EnableNETAnalyzers>
</PropertyGroup>
```

### <a name="enforcecodestyleinbuild"></a><span data-ttu-id="c4859-287">EnforceCodeStyleInBuild</span><span class="sxs-lookup"><span data-stu-id="c4859-287">EnforceCodeStyleInBuild</span></span>

> [!NOTE]
> <span data-ttu-id="c4859-288">此功能当前为实验性功能，可能会在 .NET 5 和 .NET 6 版本之间发生更改。</span><span class="sxs-lookup"><span data-stu-id="c4859-288">This feature is currently experimental and may change between the .NET 5 and .NET 6 releases.</span></span>

<span data-ttu-id="c4859-289">对于所有 .NET 项目的版本，[.NET 代码样式分析](../../fundamentals/code-analysis/overview.md#code-style-analysis)默认处于禁用状态。</span><span class="sxs-lookup"><span data-stu-id="c4859-289">[.NET code style analysis](../../fundamentals/code-analysis/overview.md#code-style-analysis) is disabled, by default, on build for all .NET projects.</span></span> <span data-ttu-id="c4859-290">通过将 `EnforceCodeStyleInBuild` 属性设置为 `true`，可以为 .NET 项目启用代码样式分析。</span><span class="sxs-lookup"><span data-stu-id="c4859-290">You can enable code style analysis for .NET projects by setting the `EnforceCodeStyleInBuild` property to `true`.</span></span>

```xml
<PropertyGroup>
  <EnforceCodeStyleInBuild>true</EnforceCodeStyleInBuild>
</PropertyGroup>
```

<span data-ttu-id="c4859-291">生成和报告违规时将执行[配置](../../fundamentals/code-analysis/overview.md#code-style-analysis)为警告或错误的所有代码样式规则。</span><span class="sxs-lookup"><span data-stu-id="c4859-291">All code style rules that are [configured](../../fundamentals/code-analysis/overview.md#code-style-analysis) to be warnings or errors will execute on build and report violations.</span></span>

## <a name="run-time-configuration-properties"></a><span data-ttu-id="c4859-292">运行时配置属性</span><span class="sxs-lookup"><span data-stu-id="c4859-292">Run-time configuration properties</span></span>

<span data-ttu-id="c4859-293">可以通过在应用的项目文件中指定 MSBuild 属性来配置某些运行时行为。</span><span class="sxs-lookup"><span data-stu-id="c4859-293">You can configure some run-time behaviors by specifying MSBuild properties in the project file of the app.</span></span> <span data-ttu-id="c4859-294">有关配置运行时行为的其他方法的信息，请参阅[运行时配置设置](../run-time-config/index.md)。</span><span class="sxs-lookup"><span data-stu-id="c4859-294">For information about other ways of configuring run-time behavior, see [Run-time configuration settings](../run-time-config/index.md).</span></span>

- [<span data-ttu-id="c4859-295">ConcurrentGarbageCollection</span><span class="sxs-lookup"><span data-stu-id="c4859-295">ConcurrentGarbageCollection</span></span>](#concurrentgarbagecollection)
- [<span data-ttu-id="c4859-296">InvariantGlobalization</span><span class="sxs-lookup"><span data-stu-id="c4859-296">InvariantGlobalization</span></span>](#invariantglobalization)
- [<span data-ttu-id="c4859-297">RetainVMGarbageCollection</span><span class="sxs-lookup"><span data-stu-id="c4859-297">RetainVMGarbageCollection</span></span>](#retainvmgarbagecollection)
- [<span data-ttu-id="c4859-298">ServerGarbageCollection</span><span class="sxs-lookup"><span data-stu-id="c4859-298">ServerGarbageCollection</span></span>](#servergarbagecollection)
- [<span data-ttu-id="c4859-299">ThreadPoolMaxThreads</span><span class="sxs-lookup"><span data-stu-id="c4859-299">ThreadPoolMaxThreads</span></span>](#threadpoolmaxthreads)
- [<span data-ttu-id="c4859-300">ThreadPoolMinThreads</span><span class="sxs-lookup"><span data-stu-id="c4859-300">ThreadPoolMinThreads</span></span>](#threadpoolminthreads)
- [<span data-ttu-id="c4859-301">TieredCompilation</span><span class="sxs-lookup"><span data-stu-id="c4859-301">TieredCompilation</span></span>](#tieredcompilation)
- [<span data-ttu-id="c4859-302">TieredCompilationQuickJit</span><span class="sxs-lookup"><span data-stu-id="c4859-302">TieredCompilationQuickJit</span></span>](#tieredcompilationquickjit)
- [<span data-ttu-id="c4859-303">TieredCompilationQuickJitForLoops</span><span class="sxs-lookup"><span data-stu-id="c4859-303">TieredCompilationQuickJitForLoops</span></span>](#tieredcompilationquickjitforloops)

### <a name="concurrentgarbagecollection"></a><span data-ttu-id="c4859-304">ConcurrentGarbageCollection</span><span class="sxs-lookup"><span data-stu-id="c4859-304">ConcurrentGarbageCollection</span></span>

<span data-ttu-id="c4859-305">`ConcurrentGarbageCollection` 属性配置是否启用 [后台（并发）垃圾回收](../../standard/garbage-collection/background-gc.md)。</span><span class="sxs-lookup"><span data-stu-id="c4859-305">The `ConcurrentGarbageCollection` property configures whether [background (concurrent) garbage collection](../../standard/garbage-collection/background-gc.md) is enabled.</span></span> <span data-ttu-id="c4859-306">将值设置为 `false` 以禁用后台垃圾回收。</span><span class="sxs-lookup"><span data-stu-id="c4859-306">Set the value to `false` to disable background garbage collection.</span></span> <span data-ttu-id="c4859-307">有关详细信息，请参阅[后台 GC](../run-time-config/garbage-collector.md#background-gc)。</span><span class="sxs-lookup"><span data-stu-id="c4859-307">For more information, see [Background GC](../run-time-config/garbage-collector.md#background-gc).</span></span>

```xml
<PropertyGroup>
  <ConcurrentGarbageCollection>false</ConcurrentGarbageCollection>
</PropertyGroup>
```

### <a name="invariantglobalization"></a><span data-ttu-id="c4859-308">InvariantGlobalization</span><span class="sxs-lookup"><span data-stu-id="c4859-308">InvariantGlobalization</span></span>

<span data-ttu-id="c4859-309">`InvariantGlobalization` 属性配置应用是否在全球化固定模式下运行，这意味着它无权访问特定于区域性的数据。</span><span class="sxs-lookup"><span data-stu-id="c4859-309">The `InvariantGlobalization` property configures whether the app runs in *globalization-invariant* mode, which means it doesn't have access to culture-specific data.</span></span> <span data-ttu-id="c4859-310">将值设置为 `true` 以在全球化固定模式下运行。</span><span class="sxs-lookup"><span data-stu-id="c4859-310">Set the value to `true` to run in globalization-invariant mode.</span></span> <span data-ttu-id="c4859-311">有关详细信息，请参阅[固定模式](../run-time-config/globalization.md#invariant-mode)。</span><span class="sxs-lookup"><span data-stu-id="c4859-311">For more information, see [Invariant mode](../run-time-config/globalization.md#invariant-mode).</span></span>

```xml
<PropertyGroup>
  <InvariantGlobalization>true</InvariantGlobalization>
</PropertyGroup>
```

### <a name="retainvmgarbagecollection"></a><span data-ttu-id="c4859-312">RetainVMGarbageCollection</span><span class="sxs-lookup"><span data-stu-id="c4859-312">RetainVMGarbageCollection</span></span>

<span data-ttu-id="c4859-313">`RetainVMGarbageCollection` 属性配置垃圾回收器，以将已删除的内存段放置在备用列表上供将来使用或释放它们。</span><span class="sxs-lookup"><span data-stu-id="c4859-313">The `RetainVMGarbageCollection` property configures the garbage collector to put deleted memory segments on a standby list for future use or release them.</span></span> <span data-ttu-id="c4859-314">将值设置为 `true` 会告知垃圾回收器将段放在备用列表上。</span><span class="sxs-lookup"><span data-stu-id="c4859-314">Setting the value to `true` tells the garbage collector to put the segments on a standby list.</span></span> <span data-ttu-id="c4859-315">有关详细信息，请参阅[保留 VM](../run-time-config/garbage-collector.md#retain-vm)。</span><span class="sxs-lookup"><span data-stu-id="c4859-315">For more information, see [Retain VM](../run-time-config/garbage-collector.md#retain-vm).</span></span>

```xml
<PropertyGroup>
  <RetainVMGarbageCollection>true</RetainVMGarbageCollection>
</PropertyGroup>
```

### <a name="servergarbagecollection"></a><span data-ttu-id="c4859-316">ServerGarbageCollection</span><span class="sxs-lookup"><span data-stu-id="c4859-316">ServerGarbageCollection</span></span>

<span data-ttu-id="c4859-317">`ServerGarbageCollection` 属性配置应用程序是使用[工作站垃圾回收还是服务器垃圾回收](../../standard/garbage-collection/workstation-server-gc.md)。</span><span class="sxs-lookup"><span data-stu-id="c4859-317">The `ServerGarbageCollection` property configures whether the application uses [workstation garbage collection or server garbage collection](../../standard/garbage-collection/workstation-server-gc.md).</span></span> <span data-ttu-id="c4859-318">将值设置为 `true` 以使用服务器垃圾回收。</span><span class="sxs-lookup"><span data-stu-id="c4859-318">Set the value to `true` to use server garbage collection.</span></span> <span data-ttu-id="c4859-319">有关详细信息，请参阅[工作站与服务器](../run-time-config/garbage-collector.md#workstation-vs-server)。</span><span class="sxs-lookup"><span data-stu-id="c4859-319">For more information, see [Workstation vs. server](../run-time-config/garbage-collector.md#workstation-vs-server).</span></span>

```xml
<PropertyGroup>
  <ServerGarbageCollection>true</ServerGarbageCollection>
</PropertyGroup>
```

### <a name="threadpoolmaxthreads"></a><span data-ttu-id="c4859-320">ThreadPoolMaxThreads</span><span class="sxs-lookup"><span data-stu-id="c4859-320">ThreadPoolMaxThreads</span></span>

<span data-ttu-id="c4859-321">`ThreadPoolMaxThreads` 属性配置工作线程池的最大线程数。</span><span class="sxs-lookup"><span data-stu-id="c4859-321">The `ThreadPoolMaxThreads` property configures the maximum number of threads for the worker thread pool.</span></span> <span data-ttu-id="c4859-322">有关详细信息，请参阅[最大线程数](../run-time-config/threading.md#maximum-threads)。</span><span class="sxs-lookup"><span data-stu-id="c4859-322">For more information, see [Maximum threads](../run-time-config/threading.md#maximum-threads).</span></span>

```xml
<PropertyGroup>
  <ThreadPoolMaxThreads>20</ThreadPoolMaxThreads>
</PropertyGroup>
```

### <a name="threadpoolminthreads"></a><span data-ttu-id="c4859-323">ThreadPoolMinThreads</span><span class="sxs-lookup"><span data-stu-id="c4859-323">ThreadPoolMinThreads</span></span>

<span data-ttu-id="c4859-324">`ThreadPoolMinThreads` 属性配置工作线程池的最小线程数。</span><span class="sxs-lookup"><span data-stu-id="c4859-324">The `ThreadPoolMinThreads` property configures the minimum number of threads for the worker thread pool.</span></span> <span data-ttu-id="c4859-325">有关详细信息，请参阅[最小线程数](../run-time-config/threading.md#minimum-threads)。</span><span class="sxs-lookup"><span data-stu-id="c4859-325">For more information, see [Minimum threads](../run-time-config/threading.md#minimum-threads).</span></span>

```xml
<PropertyGroup>
  <ThreadPoolMinThreads>4</ThreadPoolMinThreads>
</PropertyGroup>
```

### <a name="tieredcompilation"></a><span data-ttu-id="c4859-326">TieredCompilation</span><span class="sxs-lookup"><span data-stu-id="c4859-326">TieredCompilation</span></span>

<span data-ttu-id="c4859-327">`TieredCompilation` 属性配置实时 (JIT) 编译器是否使用[分层编译](../whats-new/dotnet-core-3-0.md#tiered-compilation)。</span><span class="sxs-lookup"><span data-stu-id="c4859-327">The `TieredCompilation` property configures whether the just-in-time (JIT) compiler uses [tiered compilation](../whats-new/dotnet-core-3-0.md#tiered-compilation).</span></span> <span data-ttu-id="c4859-328">将值设置为 `false` 以禁用分层编译。</span><span class="sxs-lookup"><span data-stu-id="c4859-328">Set the value to `false` to disable tiered compilation.</span></span> <span data-ttu-id="c4859-329">有关详细信息，请参阅[分层编译](../run-time-config/compilation.md#tiered-compilation)。</span><span class="sxs-lookup"><span data-stu-id="c4859-329">For more information, see [Tiered compilation](../run-time-config/compilation.md#tiered-compilation).</span></span>

```xml
<PropertyGroup>
  <TieredCompilation>false</TieredCompilation>
</PropertyGroup>
```

### <a name="tieredcompilationquickjit"></a><span data-ttu-id="c4859-330">TieredCompilationQuickJit</span><span class="sxs-lookup"><span data-stu-id="c4859-330">TieredCompilationQuickJit</span></span>

<span data-ttu-id="c4859-331">`TieredCompilationQuickJit` 属性配置 JIT 编译器是否使用快速 JIT。</span><span class="sxs-lookup"><span data-stu-id="c4859-331">The `TieredCompilationQuickJit` property configures whether the JIT compiler uses quick JIT.</span></span> <span data-ttu-id="c4859-332">将值设置为 `false` 以禁用快速 JIT。</span><span class="sxs-lookup"><span data-stu-id="c4859-332">Set the value to `false` to disable quick JIT.</span></span> <span data-ttu-id="c4859-333">有关详细信息，请参阅[快速 JIT](../run-time-config/compilation.md#quick-jit)。</span><span class="sxs-lookup"><span data-stu-id="c4859-333">For more information, see [Quick JIT](../run-time-config/compilation.md#quick-jit).</span></span>

```xml
<PropertyGroup>
  <TieredCompilationQuickJit>false</TieredCompilationQuickJit>
</PropertyGroup>
```

### <a name="tieredcompilationquickjitforloops"></a><span data-ttu-id="c4859-334">TieredCompilationQuickJitForLoops</span><span class="sxs-lookup"><span data-stu-id="c4859-334">TieredCompilationQuickJitForLoops</span></span>

<span data-ttu-id="c4859-335">`TieredCompilationQuickJitForLoops` 配置 JIT 编译器是否对包含循环的方法使用快速 JIT。</span><span class="sxs-lookup"><span data-stu-id="c4859-335">The `TieredCompilationQuickJitForLoops` property configures whether the JIT compiler uses quick JIT on methods that contain loops.</span></span> <span data-ttu-id="c4859-336">将值设置为 `true` 以对包含循环的方法启用快速 JIT。</span><span class="sxs-lookup"><span data-stu-id="c4859-336">Set the value to `true` to enable quick JIT on methods that contain loops.</span></span> <span data-ttu-id="c4859-337">有关详细信息，请参阅[适用于循环的快速 JIT](../run-time-config/compilation.md#quick-jit-for-loops)。</span><span class="sxs-lookup"><span data-stu-id="c4859-337">For more information, see [Quick JIT for loops](../run-time-config/compilation.md#quick-jit-for-loops).</span></span>

```xml
<PropertyGroup>
  <TieredCompilationQuickJitForLoops>true</TieredCompilationQuickJitForLoops>
</PropertyGroup>
```

## <a name="reference-properties-and-items"></a><span data-ttu-id="c4859-338">引用属性和项</span><span class="sxs-lookup"><span data-stu-id="c4859-338">Reference properties and items</span></span>

- [<span data-ttu-id="c4859-339">AssetTargetFallback</span><span class="sxs-lookup"><span data-stu-id="c4859-339">AssetTargetFallback</span></span>](#assettargetfallback)
- [<span data-ttu-id="c4859-340">DisableImplicitFrameworkReferences</span><span class="sxs-lookup"><span data-stu-id="c4859-340">DisableImplicitFrameworkReferences</span></span>](#disableimplicitframeworkreferences)
- [<span data-ttu-id="c4859-341">PackageReference</span><span class="sxs-lookup"><span data-stu-id="c4859-341">PackageReference</span></span>](#packagereference)
- [<span data-ttu-id="c4859-342">ProjectReference</span><span class="sxs-lookup"><span data-stu-id="c4859-342">ProjectReference</span></span>](#projectreference)
- [<span data-ttu-id="c4859-343">引用</span><span class="sxs-lookup"><span data-stu-id="c4859-343">Reference</span></span>](#reference)
- [<span data-ttu-id="c4859-344">与还原相关的属性</span><span class="sxs-lookup"><span data-stu-id="c4859-344">Restore-related properties</span></span>](#restore-related-properties)

### <a name="assettargetfallback"></a><span data-ttu-id="c4859-345">AssetTargetFallback</span><span class="sxs-lookup"><span data-stu-id="c4859-345">AssetTargetFallback</span></span>

<span data-ttu-id="c4859-346">使用 `AssetTargetFallback` 属性，可以为项目引用和 NuGet 包指定其他兼容的框架版本。</span><span class="sxs-lookup"><span data-stu-id="c4859-346">The `AssetTargetFallback` property lets you specify additional compatible framework versions for project references and NuGet packages.</span></span> <span data-ttu-id="c4859-347">例如，如果使用 `PackageReference` 指定包依赖项，但该包不包含与项目的 `TargetFramework` 兼容的资源，则可使用 `AssetTargetFallback` 属性。</span><span class="sxs-lookup"><span data-stu-id="c4859-347">For example, if you specify a package dependency using `PackageReference` but that package doesn't contain assets that are compatible with your projects's `TargetFramework`, the `AssetTargetFallback` property comes into play.</span></span> <span data-ttu-id="c4859-348">使用 `AssetTargetFallback` 中指定的每个目标框架重新检查引用包的兼容性。</span><span class="sxs-lookup"><span data-stu-id="c4859-348">The compatibility of the referenced package is rechecked using each target framework that's specified in `AssetTargetFallback`.</span></span> <span data-ttu-id="c4859-349">此属性替换已弃用的属性 `PackageTargetFallback`。</span><span class="sxs-lookup"><span data-stu-id="c4859-349">This property replaces the deprecated property `PackageTargetFallback`.</span></span>

<span data-ttu-id="c4859-350">可以将 `AssetTargetFallback` 属性设置为一个或多个[目标框架版本](../../standard/frameworks.md#supported-target-frameworks)。</span><span class="sxs-lookup"><span data-stu-id="c4859-350">You can set the `AssetTargetFallback` property to one or more [target framework versions](../../standard/frameworks.md#supported-target-frameworks).</span></span>

```xml
<PropertyGroup>
  <AssetTargetFallback>net461</AssetTargetFallback>
</PropertyGroup>
```

### <a name="disableimplicitframeworkreferences"></a><span data-ttu-id="c4859-351">DisableImplicitFrameworkReferences</span><span class="sxs-lookup"><span data-stu-id="c4859-351">DisableImplicitFrameworkReferences</span></span>

<span data-ttu-id="c4859-352">面向 .NET Core 3.0 及更高版本时，`DisableImplicitFrameworkReferences` 属性会控制隐式 `FrameworkReference` 项。</span><span class="sxs-lookup"><span data-stu-id="c4859-352">The `DisableImplicitFrameworkReferences` property controls implicit `FrameworkReference` items when targeting .NET Core 3.0 and later versions.</span></span> <span data-ttu-id="c4859-353">面向 .NET Core 2.1 或 .NET Standard 2.0 及早期版本时，该属性会控制元包中包的隐式 [PackageReference](#packagereference) 项。</span><span class="sxs-lookup"><span data-stu-id="c4859-353">When targeting .NET Core 2.1 or .NET Standard 2.0 and earlier versions, it controls implicit [PackageReference](#packagereference) items to packages in a metapackage.</span></span> <span data-ttu-id="c4859-354">（元包是一种基于框架的包，其中仅包含对其他包的依赖项。）在面向 .NET Framework 时，此属性还控制隐式引用，如 `System` 和 `System.Core`。</span><span class="sxs-lookup"><span data-stu-id="c4859-354">(A metapackage is a framework-based package that consist only of dependencies on other packages.) This property also controls implicit references such as `System` and `System.Core` when targeting .NET Framework.</span></span>

<span data-ttu-id="c4859-355">将此属性设置为 `true` 以禁用隐式 `FrameworkReference` 或 [PackageReference](#packagereference) 项。</span><span class="sxs-lookup"><span data-stu-id="c4859-355">Set this property to `true` to disable implicit `FrameworkReference` or [PackageReference](#packagereference) items.</span></span> <span data-ttu-id="c4859-356">如果将此属性设置为 `true`，则可以仅添加对所需框架或包的显式引用。</span><span class="sxs-lookup"><span data-stu-id="c4859-356">If you set this property to `true`, you can add explicit references to just the frameworks or packages you need.</span></span>

```xml
<PropertyGroup>
  <DisableImplicitFrameworkReferences>true</DisableImplicitFrameworkReferences>
</PropertyGroup>
```

### <a name="packagereference"></a><span data-ttu-id="c4859-357">PackageReference</span><span class="sxs-lookup"><span data-stu-id="c4859-357">PackageReference</span></span>

<span data-ttu-id="c4859-358">`PackageReference` 项定义了对 NuGet 包的引用。</span><span class="sxs-lookup"><span data-stu-id="c4859-358">The `PackageReference` item defines a reference to a NuGet package.</span></span>

<span data-ttu-id="c4859-359">`Include` 属性指定包 ID。</span><span class="sxs-lookup"><span data-stu-id="c4859-359">The `Include` attribute specifies the package ID.</span></span> <span data-ttu-id="c4859-360">`Version` 特性指定版本或版本范围。</span><span class="sxs-lookup"><span data-stu-id="c4859-360">The `Version` attribute specifies the version or version range.</span></span> <span data-ttu-id="c4859-361">若要了解如何指定最低版本、最高版本、范围或完全匹配，请参阅[版本范围](/nuget/concepts/package-versioning#version-ranges)。</span><span class="sxs-lookup"><span data-stu-id="c4859-361">For information about how to specify a minimum version, maximum version, range, or exact match, see [Version ranges](/nuget/concepts/package-versioning#version-ranges).</span></span> <span data-ttu-id="c4859-362">还可以将[资产特性](#asset-attributes)添加到包引用中。</span><span class="sxs-lookup"><span data-stu-id="c4859-362">You can also add [asset attributes](#asset-attributes) to a package reference.</span></span>

<span data-ttu-id="c4859-363">以下示例中的项目文件片段引用 [System.Runtime](https://www.nuget.org/packages/System.Runtime/) 包。</span><span class="sxs-lookup"><span data-stu-id="c4859-363">The project file snippet in the following example references the [System.Runtime](https://www.nuget.org/packages/System.Runtime/) package.</span></span>

```xml
<ItemGroup>
  <PackageReference Include="System.Runtime" Version="4.3.0" />
</ItemGroup>
```

<span data-ttu-id="c4859-364">有关详细信息，请参阅[项目文件中的包引用](/nuget/consume-packages/package-references-in-project-files)。</span><span class="sxs-lookup"><span data-stu-id="c4859-364">For more information, see [Package references in project files](/nuget/consume-packages/package-references-in-project-files).</span></span>

#### <a name="asset-attributes"></a><span data-ttu-id="c4859-365">资产特性</span><span class="sxs-lookup"><span data-stu-id="c4859-365">Asset attributes</span></span>

<span data-ttu-id="c4859-366">可以将 `IncludeAssets`、`ExcludeAssets` 和 `PrivateAssets` 元数据添加到包引用中。</span><span class="sxs-lookup"><span data-stu-id="c4859-366">The `IncludeAssets`, `ExcludeAssets`, and `PrivateAssets` metadata can be added to a package reference.</span></span>

| <span data-ttu-id="c4859-367">属性</span><span class="sxs-lookup"><span data-stu-id="c4859-367">Attribute</span></span> | <span data-ttu-id="c4859-368">描述</span><span class="sxs-lookup"><span data-stu-id="c4859-368">Description</span></span> |
| - | - |
| `IncludeAssets` | <span data-ttu-id="c4859-369">指定应使用 `<PackageReference>` 指定的包中的哪些资产。</span><span class="sxs-lookup"><span data-stu-id="c4859-369">Specifies which assets belonging to the package specified by `<PackageReference>` should be consumed.</span></span> <span data-ttu-id="c4859-370">默认情况下，包含所有包资产。</span><span class="sxs-lookup"><span data-stu-id="c4859-370">By default, all package assets are included.</span></span> |
| `ExcludeAssets`| <span data-ttu-id="c4859-371">指定不应使用 `<PackageReference>` 指定的包中的哪些资产。</span><span class="sxs-lookup"><span data-stu-id="c4859-371">Specifies which assets belonging to the package specified by `<PackageReference>` should not be consumed.</span></span> |
| `PrivateAssets` | <span data-ttu-id="c4859-372">指定应使用 `<PackageReference>` 指定的包中的哪些资产，但不得将这些资产传递到下一个项目。</span><span class="sxs-lookup"><span data-stu-id="c4859-372">Specifies which assets belonging to the package specified by `<PackageReference>` should be consumed but not flow to the next project.</span></span> <span data-ttu-id="c4859-373">不存在此特性时，`Analyzers`、`Build` 和 `ContentFiles` 资产默认为私有。</span><span class="sxs-lookup"><span data-stu-id="c4859-373">The `Analyzers`, `Build`, and `ContentFiles` assets are private by default when this attribute is not present.</span></span> |

<span data-ttu-id="c4859-374">这些属性可以包含以下一个或多个项，如果列出多个项，则用分号 `;` 进行分隔：</span><span class="sxs-lookup"><span data-stu-id="c4859-374">These attributes can contain one or more of the following items, separated by a semicolon `;` if more than one is listed:</span></span>

- <span data-ttu-id="c4859-375">`Compile` - 可对 lib 文件夹的内容进行编译  。</span><span class="sxs-lookup"><span data-stu-id="c4859-375">`Compile` – the contents of the *lib* folder are available to compile against.</span></span>
- <span data-ttu-id="c4859-376">`Runtime` - 分发 runtime 文件夹的内容  。</span><span class="sxs-lookup"><span data-stu-id="c4859-376">`Runtime` – the contents of the *runtime* folder are distributed.</span></span>
- <span data-ttu-id="c4859-377">`ContentFiles` - 使用 *contentfiles* 文件夹的内容。</span><span class="sxs-lookup"><span data-stu-id="c4859-377">`ContentFiles` – the contents of the *contentfiles* folder are used.</span></span>
- <span data-ttu-id="c4859-378">`Build` - 使用 build 文件夹中的属性/目标  。</span><span class="sxs-lookup"><span data-stu-id="c4859-378">`Build` – the props/targets in the *build* folder are used.</span></span>
- <span data-ttu-id="c4859-379">`Native` - 将本机资产内容复制到 output 文件夹  以供运行时使用。</span><span class="sxs-lookup"><span data-stu-id="c4859-379">`Native` – the contents from native assets are copied to the *output* folder for runtime.</span></span>
- <span data-ttu-id="c4859-380">`Analyzers` - 使用分析器。</span><span class="sxs-lookup"><span data-stu-id="c4859-380">`Analyzers` – the analyzers are used.</span></span>

<span data-ttu-id="c4859-381">此属性也可以包含：</span><span class="sxs-lookup"><span data-stu-id="c4859-381">Alternatively, the attribute can contain:</span></span>

- <span data-ttu-id="c4859-382">`None` - 不使用任何资产。</span><span class="sxs-lookup"><span data-stu-id="c4859-382">`None` – none of the assets are used.</span></span>
- <span data-ttu-id="c4859-383">`All` - 使用所有资产。</span><span class="sxs-lookup"><span data-stu-id="c4859-383">`All` – all assets are used.</span></span>

### <a name="projectreference"></a><span data-ttu-id="c4859-384">ProjectReference</span><span class="sxs-lookup"><span data-stu-id="c4859-384">ProjectReference</span></span>

<span data-ttu-id="c4859-385">`ProjectReference` 项定义对另一个项目的引用。</span><span class="sxs-lookup"><span data-stu-id="c4859-385">The `ProjectReference` item defines a reference to another project.</span></span> <span data-ttu-id="c4859-386">被引用的项目作为 NuGet 包依赖项添加，即它被视为与 `PackageReference` 相同。</span><span class="sxs-lookup"><span data-stu-id="c4859-386">The referenced project is added as a NuGet package dependency, that is, it's treated the same as a `PackageReference`.</span></span>

<span data-ttu-id="c4859-387">`Include` 特性指定项目路径。</span><span class="sxs-lookup"><span data-stu-id="c4859-387">The `Include` attribute specifies the path to the project.</span></span> <span data-ttu-id="c4859-388">还可以将下面的元数据添加到项目引用中：`IncludeAssets`、`ExcludeAssets` 和 `PrivateAssets`。</span><span class="sxs-lookup"><span data-stu-id="c4859-388">You can also add the following metadata to a project reference: `IncludeAssets`, `ExcludeAssets`, and `PrivateAssets`.</span></span>

<span data-ttu-id="c4859-389">以下示例中的项目文件片段引用名为 `Project2` 的项目。</span><span class="sxs-lookup"><span data-stu-id="c4859-389">The project file snippet in the following example references a project named `Project2`.</span></span>

```xml
<ItemGroup>
  <ProjectReference Include="..\Project2.csproj" />
</ItemGroup>
```

### <a name="reference"></a><span data-ttu-id="c4859-390">参考</span><span class="sxs-lookup"><span data-stu-id="c4859-390">Reference</span></span>

<span data-ttu-id="c4859-391">`Reference` 项定义对程序集文件的引用。</span><span class="sxs-lookup"><span data-stu-id="c4859-391">The `Reference` item defines a reference to an assembly file.</span></span>

<span data-ttu-id="c4859-392">`Include` 特性用于指定文件名，`HintPath` 元数据用于指定程序集路径。</span><span class="sxs-lookup"><span data-stu-id="c4859-392">The `Include` attribute specifies the name of the file, and the `HintPath` metadata specifies the path to the assembly.</span></span>

```xml
<ItemGroup>
  <Reference Include="MyAssembly">
    <HintPath>..\..\Assemblies\MyAssembly.dll</HintPath>
  </Reference>
</ItemGroup>
```

### <a name="restore-related-properties"></a><span data-ttu-id="c4859-393">与还原相关的属性</span><span class="sxs-lookup"><span data-stu-id="c4859-393">Restore-related properties</span></span>

<span data-ttu-id="c4859-394">还原被引用的包会安装它的所有直接依赖项，以及这些依赖项的全部依赖项。</span><span class="sxs-lookup"><span data-stu-id="c4859-394">Restoring a referenced package installs all of its direct dependencies and all the dependencies of those dependencies.</span></span> <span data-ttu-id="c4859-395">可以通过指定 `RestorePackagesPath` 和 `RestoreIgnoreFailedSources` 等属性来自定义包还原。</span><span class="sxs-lookup"><span data-stu-id="c4859-395">You can customize package restoration by specifying properties such as `RestorePackagesPath` and `RestoreIgnoreFailedSources`.</span></span> <span data-ttu-id="c4859-396">若要详细了解这些属性和其他属性，请参阅[还原目标](/nuget/reference/msbuild-targets#restore-target)。</span><span class="sxs-lookup"><span data-stu-id="c4859-396">For more information about these and other properties, see [restore target](/nuget/reference/msbuild-targets#restore-target).</span></span>

```xml
<PropertyGroup>
  <RestoreIgnoreFailedSource>true</RestoreIgnoreFailedSource>
</PropertyGroup>
```

## <a name="run-properties"></a><span data-ttu-id="c4859-397">运行属性</span><span class="sxs-lookup"><span data-stu-id="c4859-397">Run properties</span></span>

<span data-ttu-id="c4859-398">以下属性用于使用 [`dotnet run`](../tools/dotnet-run.md) 命令启动应用：</span><span class="sxs-lookup"><span data-stu-id="c4859-398">The following properties are used for launching an app with the [`dotnet run`](../tools/dotnet-run.md) command:</span></span>

- [<span data-ttu-id="c4859-399">RunArguments</span><span class="sxs-lookup"><span data-stu-id="c4859-399">RunArguments</span></span>](#runarguments)
- [<span data-ttu-id="c4859-400">RunWorkingDirectory</span><span class="sxs-lookup"><span data-stu-id="c4859-400">RunWorkingDirectory</span></span>](#runworkingdirectory)

### <a name="runarguments"></a><span data-ttu-id="c4859-401">RunArguments</span><span class="sxs-lookup"><span data-stu-id="c4859-401">RunArguments</span></span>

<span data-ttu-id="c4859-402">`RunArguments` 属性定义了在应用运行时向其传递的参数。</span><span class="sxs-lookup"><span data-stu-id="c4859-402">The `RunArguments` property defines the arguments that are passed to the app when it is run.</span></span>

```xml
<PropertyGroup>
  <RunArguments>-mode dryrun</RunArguments>
</PropertyGroup>
```

> [!TIP]
> <span data-ttu-id="c4859-403">可以使用 [`dotnet run` 的 `--` 选项](../tools/dotnet-run.md#options)来指定要传递到应用的其他参数。</span><span class="sxs-lookup"><span data-stu-id="c4859-403">You can specify additional arguments to be passed to the app by using the [`--` option for `dotnet run`](../tools/dotnet-run.md#options).</span></span>

### <a name="runworkingdirectory"></a><span data-ttu-id="c4859-404">RunWorkingDirectory</span><span class="sxs-lookup"><span data-stu-id="c4859-404">RunWorkingDirectory</span></span>

<span data-ttu-id="c4859-405">`RunWorkingDirectory` 属性定义要用于启动应用程序进程的工作目录。</span><span class="sxs-lookup"><span data-stu-id="c4859-405">The `RunWorkingDirectory` property defines the working directory for the application process to be started in.</span></span> <span data-ttu-id="c4859-406">它可以是绝对路径，也可以是相对于项目目录的路径。</span><span class="sxs-lookup"><span data-stu-id="c4859-406">It can be an absolute path or a path that's relative to the project directory.</span></span> <span data-ttu-id="c4859-407">如果未指定目录，`OutDir` 将用作工作目录。</span><span class="sxs-lookup"><span data-stu-id="c4859-407">If you don't specify a directory, `OutDir` is used as the working directory.</span></span>

```xml
<PropertyGroup>
  <RunWorkingDirectory>c:\temp</RunWorkingDirectory>
</PropertyGroup>
```

## <a name="hosting-properties"></a><span data-ttu-id="c4859-408">承载属性</span><span class="sxs-lookup"><span data-stu-id="c4859-408">Hosting properties</span></span>

- [<span data-ttu-id="c4859-409">EnableComHosting</span><span class="sxs-lookup"><span data-stu-id="c4859-409">EnableComHosting</span></span>](#enablecomhosting)
- [<span data-ttu-id="c4859-410">EnableDynamicLoading</span><span class="sxs-lookup"><span data-stu-id="c4859-410">EnableDynamicLoading</span></span>](#enabledynamicloading)

### <a name="enablecomhosting"></a><span data-ttu-id="c4859-411">EnableComHosting</span><span class="sxs-lookup"><span data-stu-id="c4859-411">EnableComHosting</span></span>

<span data-ttu-id="c4859-412">`EnableComHosting` 属性表示程序集提供了 COM 服务器。</span><span class="sxs-lookup"><span data-stu-id="c4859-412">The `EnableComHosting` property indicates that an assembly provides a COM server.</span></span> <span data-ttu-id="c4859-413">将 `EnableComHosting` 设置为 `true` 也表明 [EnableDynamicLoading](#enabledynamicloading) 为 `true`。</span><span class="sxs-lookup"><span data-stu-id="c4859-413">Setting the `EnableComHosting` to `true` also implies that [EnableDynamicLoading](#enabledynamicloading) is `true`.</span></span>

```xml
<PropertyGroup>
  <EnableComHosting>True</EnableComHosting>
</PropertyGroup>
```

<span data-ttu-id="c4859-414">有关详细信息，请参阅[向 COM 公开 .NET 组件](../native-interop/expose-components-to-com.md)。</span><span class="sxs-lookup"><span data-stu-id="c4859-414">For more information, see [Expose .NET components to COM](../native-interop/expose-components-to-com.md).</span></span>

### <a name="enabledynamicloading"></a><span data-ttu-id="c4859-415">EnableDynamicLoading</span><span class="sxs-lookup"><span data-stu-id="c4859-415">EnableDynamicLoading</span></span>

<span data-ttu-id="c4859-416">`EnableDynamicLoading` 属性指示程序集是动态加载的组件。</span><span class="sxs-lookup"><span data-stu-id="c4859-416">The `EnableDynamicLoading` property indicates that an assembly is a dynamically loaded component.</span></span> <span data-ttu-id="c4859-417">组件可以是 [COM 库](/windows/win32/com/the-component-object-model)，也可以是[在本机主机中使用的](../tutorials/netcore-hosting.md)非 COM 库。</span><span class="sxs-lookup"><span data-stu-id="c4859-417">The component could be a [COM library](/windows/win32/com/the-component-object-model) or a non-COM library that can be [used from a native host](../tutorials/netcore-hosting.md).</span></span> <span data-ttu-id="c4859-418">将此属性设置为 `true` 会产生以下结果：</span><span class="sxs-lookup"><span data-stu-id="c4859-418">Setting this property to `true` has the following effects:</span></span>

- <span data-ttu-id="c4859-419">生成 runtimeconfig.json 文件。</span><span class="sxs-lookup"><span data-stu-id="c4859-419">A *.runtimeconfig.json* file is generated.</span></span>
- <span data-ttu-id="c4859-420">[前滚](../whats-new/dotnet-core-3-0.md#major-version-runtime-roll-forward)设置为 `LatestMinor`。</span><span class="sxs-lookup"><span data-stu-id="c4859-420">[Roll forward](../whats-new/dotnet-core-3-0.md#major-version-runtime-roll-forward) is set to `LatestMinor`.</span></span>
- <span data-ttu-id="c4859-421">在本地复制 NuGet 引用。</span><span class="sxs-lookup"><span data-stu-id="c4859-421">NuGet references are copied locally.</span></span>

```xml
<PropertyGroup>
  <EnableDynamicLoading>true</EnableDynamicLoading>
</PropertyGroup>
```

## <a name="see-also"></a><span data-ttu-id="c4859-422">请参阅</span><span class="sxs-lookup"><span data-stu-id="c4859-422">See also</span></span>

- [<span data-ttu-id="c4859-423">MSBuild 架构引用</span><span class="sxs-lookup"><span data-stu-id="c4859-423">MSBuild schema reference</span></span>](/visualstudio/msbuild/msbuild-project-file-schema-reference)
- [<span data-ttu-id="c4859-424">通用 MSBuild 属性</span><span class="sxs-lookup"><span data-stu-id="c4859-424">Common MSBuild properties</span></span>](/visualstudio/msbuild/common-msbuild-project-properties)
- [<span data-ttu-id="c4859-425">NuGet 包的 MSBuild 属性</span><span class="sxs-lookup"><span data-stu-id="c4859-425">MSBuild properties for NuGet pack</span></span>](/nuget/reference/msbuild-targets#pack-target)
- [<span data-ttu-id="c4859-426">NuGet 还原的 MSBuild 属性</span><span class="sxs-lookup"><span data-stu-id="c4859-426">MSBuild properties for NuGet restore</span></span>](/nuget/reference/msbuild-targets#restore-properties)
- [<span data-ttu-id="c4859-427">自定义生成</span><span class="sxs-lookup"><span data-stu-id="c4859-427">Customize a build</span></span>](/visualstudio/msbuild/customize-your-build)
