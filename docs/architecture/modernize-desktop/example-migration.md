---
title: 迁移到 .NET 5 的示例
description: 演示如何将目标 .NET Framework 的示例应用程序迁移到 .NET 5。
ms.date: 01/19/2021
ms.openlocfilehash: 39ecdfa639f4d68a4a8821da839f014c8de42ab0
ms.sourcegitcommit: 68c9d9d9a97aab3b59d388914004b5474cf1dbd7
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/30/2021
ms.locfileid: "99216260"
---
# <a name="example-of-migrating-to-net"></a><span data-ttu-id="a6bc1-103">迁移到 .NET 的示例</span><span class="sxs-lookup"><span data-stu-id="a6bc1-103">Example of migrating to .NET</span></span>

<span data-ttu-id="a6bc1-104">在本章中，我们提供了实用指导原则，可帮助你将现有应用程序从 .NET Framework 迁移到 .NET。</span><span class="sxs-lookup"><span data-stu-id="a6bc1-104">In this chapter, we present practical guidelines to help you perform a migration of your existing application from .NET Framework to .NET.</span></span>

<span data-ttu-id="a6bc1-105">我们提供了一个结构良好的过程，你可以遵循此过程以及每个步骤要考虑的最重要事项。</span><span class="sxs-lookup"><span data-stu-id="a6bc1-105">We present a well-structured process you can follow and the most important things to consider on each step.</span></span>

<span data-ttu-id="a6bc1-106">接下来，我们记录了 WinForms 和 WPF 版本的示例桌面应用程序的分步迁移过程。</span><span class="sxs-lookup"><span data-stu-id="a6bc1-106">We then document a step-by-step migration process for a sample desktop application, both from WinForms and WPF versions.</span></span>

## <a name="migration-process-overview"></a><span data-ttu-id="a6bc1-107">迁移过程概述</span><span class="sxs-lookup"><span data-stu-id="a6bc1-107">Migration process overview</span></span>

<span data-ttu-id="a6bc1-108">迁移过程包括四个顺序步骤：</span><span class="sxs-lookup"><span data-stu-id="a6bc1-108">The migration process consists of four sequential steps:</span></span>

1. <span data-ttu-id="a6bc1-109">**准备**：了解项目所需的依赖关系，了解这一点。</span><span class="sxs-lookup"><span data-stu-id="a6bc1-109">**Preparation**: Understand the dependencies the project has to have an idea of what's ahead.</span></span> <span data-ttu-id="a6bc1-110">在此步骤中，您将使用当前项目，以简化迁移的启动点。</span><span class="sxs-lookup"><span data-stu-id="a6bc1-110">In this step, you take the current project into a state that simplifies the startup point for the migration.</span></span>

2. <span data-ttu-id="a6bc1-111">**迁移项目文件：** .net 项目使用的是新的 SDK 样式项目格式。</span><span class="sxs-lookup"><span data-stu-id="a6bc1-111">**Migrate Project File:** .NET projects use the new SDK-style project format.</span></span> <span data-ttu-id="a6bc1-112">使用此格式创建一个新的项目文件，或更新必须使用 SDK 样式的项目文件。</span><span class="sxs-lookup"><span data-stu-id="a6bc1-112">Create a new project file with this format or update the one you have to use the SDK style.</span></span>

3. <span data-ttu-id="a6bc1-113">**修复代码并生成：** 在 .NET 寻址 API 级别的 .NET Framework 与 .NET 之间的差异中生成代码。</span><span class="sxs-lookup"><span data-stu-id="a6bc1-113">**Fix code and build:** Build the code in .NET addressing API-level differences between .NET Framework and .NET.</span></span> <span data-ttu-id="a6bc1-114">如果需要，请将第三方包更新为支持 .NET 的包。</span><span class="sxs-lookup"><span data-stu-id="a6bc1-114">If needed, update third-party packages to the ones that support .NET.</span></span>

4. <span data-ttu-id="a6bc1-115">**运行和测试：** 可能存在直到运行时才会显示的差异。</span><span class="sxs-lookup"><span data-stu-id="a6bc1-115">**Run and test:** There might be differences that don't show up until run time.</span></span> <span data-ttu-id="a6bc1-116">因此，请不要忘记运行应用程序并测试一切是否按预期方式工作。</span><span class="sxs-lookup"><span data-stu-id="a6bc1-116">So, don't forget to run the application and test that everything works as expected.</span></span>

### <a name="preparation"></a><span data-ttu-id="a6bc1-117">准备工作</span><span class="sxs-lookup"><span data-stu-id="a6bc1-117">Preparation</span></span>

#### <a name="migrate-packagesconfig-file"></a><span data-ttu-id="a6bc1-118">迁移 packages.config 文件</span><span class="sxs-lookup"><span data-stu-id="a6bc1-118">Migrate packages.config file</span></span>

<span data-ttu-id="a6bc1-119">在 .NET Framework 应用程序中，对外部包的所有引用都在 *packages.config* 文件中声明。</span><span class="sxs-lookup"><span data-stu-id="a6bc1-119">In a .NET Framework application, all references to external packages are declared in the *packages.config* file.</span></span> <span data-ttu-id="a6bc1-120">在 .NET 中，不再需要使用 *packages.config* 文件。</span><span class="sxs-lookup"><span data-stu-id="a6bc1-120">In .NET, there's no longer the need to use the *packages.config* file.</span></span> <span data-ttu-id="a6bc1-121">而应使用项目文件中的 [PackageReference](../../core/project-sdk/msbuild-props.md#packagereference) 属性来指定应用的 NuGet 包。</span><span class="sxs-lookup"><span data-stu-id="a6bc1-121">Instead, use the [PackageReference](../../core/project-sdk/msbuild-props.md#packagereference) property inside the project file to specify the NuGet packages for your app.</span></span>

<span data-ttu-id="a6bc1-122">因此，您需要从一种格式转换为另一种格式。</span><span class="sxs-lookup"><span data-stu-id="a6bc1-122">So, you need to transition from one format to another.</span></span> <span data-ttu-id="a6bc1-123">您可以手动进行更新，采用 *packages.config* 文件中包含的依赖项并将其迁移到具有格式的项目文件 `PackageReference` 。</span><span class="sxs-lookup"><span data-stu-id="a6bc1-123">You can do the update manually, taking the dependencies contained in the *packages.config* file and migrating them to the project file with the `PackageReference` format.</span></span> <span data-ttu-id="a6bc1-124">或者，你可以让 Visual Studio 为你完成工作：右键单击 *packages.config* 文件，然后选择 "将 **packages.config 迁移到 PackageReference** " 选项。</span><span class="sxs-lookup"><span data-stu-id="a6bc1-124">Or, you can let Visual Studio do the work for you: right-click on the *packages.config* file and select the **Migrate packages.config to PackageReference** option.</span></span>

#### <a name="verify-every-dependency-compatibility-in-net"></a><span data-ttu-id="a6bc1-125">验证 .NET 中的每个依赖项兼容性</span><span class="sxs-lookup"><span data-stu-id="a6bc1-125">Verify every dependency compatibility in .NET</span></span>

<span data-ttu-id="a6bc1-126">迁移包引用后，必须检查每个引用的兼容性。</span><span class="sxs-lookup"><span data-stu-id="a6bc1-126">Once you've migrated the package references, you must check each reference for compatibility.</span></span> <span data-ttu-id="a6bc1-127">可以浏览应用程序在 [nuget.org](https://www.nuget.org/)上使用的每个 NuGet 包的依赖关系。如果包具有 .NET Standard 依赖项，则它将在 .NET 5.0 上运行，因为 .NET [支持](../../standard/net-standard.md#net-implementation-support) 所有版本的 .NET Standard。</span><span class="sxs-lookup"><span data-stu-id="a6bc1-127">You can explore the dependencies of each NuGet package your application is using on [nuget.org](https://www.nuget.org/). If the package has .NET Standard dependencies, then it's going to work on .NET 5.0 because .NET [supports](../../standard/net-standard.md#net-implementation-support) all versions of .NET Standard.</span></span> <span data-ttu-id="a6bc1-128">下图显示了包的依赖项 `Castle.Windsor` ：</span><span class="sxs-lookup"><span data-stu-id="a6bc1-128">The following image shows the dependencies for the `Castle.Windsor` package:</span></span>

![城堡 Windsor 包的 NuGet 依赖项的屏幕截图](./media/example-migration-core/nuget-dependencies.png)

<span data-ttu-id="a6bc1-130">若要检查包兼容性，可以使用 <https://fuget.org> 提供有关版本和依赖项的更多详细信息的工具。</span><span class="sxs-lookup"><span data-stu-id="a6bc1-130">To check the package compatibility, you can use the tool <https://fuget.org> that offers a more detailed information about versions and dependencies.</span></span>

<span data-ttu-id="a6bc1-131">此项目可能引用了不支持 .NET 的较旧包版本，但你可能会发现支持它的较新版本。</span><span class="sxs-lookup"><span data-stu-id="a6bc1-131">Maybe the project is referencing older package versions that don't support .NET, but you might find newer versions that do support it.</span></span> <span data-ttu-id="a6bc1-132">因此，将包更新到较新版本通常是一种很好的建议。</span><span class="sxs-lookup"><span data-stu-id="a6bc1-132">So, updating packages to newer versions is generally a good recommendation.</span></span> <span data-ttu-id="a6bc1-133">但是，你应该考虑更新包版本会引入一些重大更改，这些更改将强制你更新代码。</span><span class="sxs-lookup"><span data-stu-id="a6bc1-133">However, you should consider that updating the package version can introduce some breaking changes that would force you to update your code.</span></span>

<span data-ttu-id="a6bc1-134">如果找不到兼容的版本，会发生什么情况？</span><span class="sxs-lookup"><span data-stu-id="a6bc1-134">What happens if you don't find a compatible version?</span></span> <span data-ttu-id="a6bc1-135">如果你只是因为这种重大更改而不想更新包的版本怎么办？</span><span class="sxs-lookup"><span data-stu-id="a6bc1-135">What if you just don't want to update the version of a package because of these breaking changes?</span></span> <span data-ttu-id="a6bc1-136">请不要担心，因为它可能依赖于 .NET 应用程序中 .NET Framework 包。</span><span class="sxs-lookup"><span data-stu-id="a6bc1-136">Don't worry because it's possible to depend on .NET Framework packages from a .NET application.</span></span> <span data-ttu-id="a6bc1-137">请不要忘记对其进行大量测试，因为如果外部包调用的 API 在 .NET 中不可用，则可能会导致运行时错误。</span><span class="sxs-lookup"><span data-stu-id="a6bc1-137">Don't forget to test it extensively because it can cause run-time errors if the external package calls an API that isn't available on .NET.</span></span> <span data-ttu-id="a6bc1-138">这非常适合于使用不会更新的旧包，并且你可以直接重定向到 .NET 中的工作。</span><span class="sxs-lookup"><span data-stu-id="a6bc1-138">This is great for when you're using an old package that isn't going to be updated and you can just retarget to work on the .NET.</span></span>

#### <a name="check-for-api-compatibility"></a><span data-ttu-id="a6bc1-139">检查是否有 API 兼容性</span><span class="sxs-lookup"><span data-stu-id="a6bc1-139">Check for API compatibility</span></span>

<span data-ttu-id="a6bc1-140">由于 .NET Framework 和 .NET 中的 API 图面类似但并不完全相同，因此必须检查哪些 Api 在 .NET 上可用，哪些不是。</span><span class="sxs-lookup"><span data-stu-id="a6bc1-140">Since the API surface in .NET Framework and .NET is similar but not identical, you must check which APIs are available on .NET and which aren't.</span></span> <span data-ttu-id="a6bc1-141">可以使用 .NET 可移植性分析器工具来呈现 .NET 上所使用的 Api。</span><span class="sxs-lookup"><span data-stu-id="a6bc1-141">You can use the .NET Portability Analyzer tool to surface APIs used that aren't present on .NET.</span></span> <span data-ttu-id="a6bc1-142">它查看应用的二进制级别，提取调用的所有 Api，然后列出目标框架上不可用的 Api ( 在此情况下) 的 .NET 5.0。</span><span class="sxs-lookup"><span data-stu-id="a6bc1-142">It looks at the binary level of your app, extracts all the APIs that are called, and then lists which APIs aren't available on your target framework (.NET 5.0 in this case).</span></span>

<span data-ttu-id="a6bc1-143">可以在以下位置找到有关此工具的详细信息：</span><span class="sxs-lookup"><span data-stu-id="a6bc1-143">You can find more information about this tool at:</span></span>

<https://docs.microsoft.com/dotnet/standard/analyzers/portability-analyzer>

<span data-ttu-id="a6bc1-144">此工具的一个有趣方面是，它仅从您自己的代码，而不是不能更改的外部包的代码呈现差异。</span><span class="sxs-lookup"><span data-stu-id="a6bc1-144">An interesting aspect of this tool is that it only surfaces the differences from your own code and not code from external packages, which you can't change.</span></span> <span data-ttu-id="a6bc1-145">请记住，您应该更新这些包中的大部分，以使它们可用于 .NET。</span><span class="sxs-lookup"><span data-stu-id="a6bc1-145">Remember you should have updated most of these packages to make them work with .NET.</span></span>

### <a name="migrate-with-try-convert-tool"></a><span data-ttu-id="a6bc1-146">通过 Try 转换工具迁移</span><span class="sxs-lookup"><span data-stu-id="a6bc1-146">Migrate with Try Convert tool</span></span>

<span data-ttu-id="a6bc1-147">[试用转换](https://github.com/dotnet/try-convert/releases)工具是迁移项目的好方法。</span><span class="sxs-lookup"><span data-stu-id="a6bc1-147">The [Try Convert](https://github.com/dotnet/try-convert/releases) tool is a great way to migrate a project.</span></span> <span data-ttu-id="a6bc1-148">它是一个全局工具，它尝试将项目文件从旧样式升级到新的 SDK 样式，并将适用的项目重定目标到 .NET 5。</span><span class="sxs-lookup"><span data-stu-id="a6bc1-148">It's a global tool that attempts to upgrade your project file from the old style to the new SDK style, and retargets applicable projects to .NET 5.</span></span> <span data-ttu-id="a6bc1-149">安装完成后，可以运行以下命令：</span><span class="sxs-lookup"><span data-stu-id="a6bc1-149">Once installed, you can run the following commands:</span></span>

```dotnetcli
try-convert -p "<path to your project file>"
```

<span data-ttu-id="a6bc1-150">或：</span><span class="sxs-lookup"><span data-stu-id="a6bc1-150">Or:</span></span>

```dotnetcli
try-convert -w "<path to your solution>"
```

<span data-ttu-id="a6bc1-151">在该工具尝试转换后，在 Visual Studio 中重新加载文件以运行和测试。</span><span class="sxs-lookup"><span data-stu-id="a6bc1-151">After the tool attempts the conversion, reload your files in Visual Studio to run and test.</span></span> <span data-ttu-id="a6bc1-152">由于你的项目的具体情况，可能无法尝试转换来执行转换。</span><span class="sxs-lookup"><span data-stu-id="a6bc1-152">There's a possibility that Try Convert won't be able to perform the conversion due to the specifics of your project.</span></span> <span data-ttu-id="a6bc1-153">在这种情况下，可以参考以下步骤。</span><span class="sxs-lookup"><span data-stu-id="a6bc1-153">In that case, you can refer the below steps.</span></span>

#### <a name="migrate-manually"></a><span data-ttu-id="a6bc1-154">手动迁移</span><span class="sxs-lookup"><span data-stu-id="a6bc1-154">Migrate manually</span></span>

1. <span data-ttu-id="a6bc1-155">创建新的 .NET 项目</span><span class="sxs-lookup"><span data-stu-id="a6bc1-155">Create the new .NET project</span></span>

<span data-ttu-id="a6bc1-156">在大多数情况下，你需要将现有项目更新为新的 .NET 格式。</span><span class="sxs-lookup"><span data-stu-id="a6bc1-156">In most cases, you'll want to update your existing project to the new .NET format.</span></span> <span data-ttu-id="a6bc1-157">不过，您也可以创建一个新项目，同时保持旧项目。</span><span class="sxs-lookup"><span data-stu-id="a6bc1-157">However, you can also create a new project while maintaining the old one.</span></span> <span data-ttu-id="a6bc1-158">更新旧项目的主要缺点是丢失设计器支持，这对你和你的开发团队可能很重要。</span><span class="sxs-lookup"><span data-stu-id="a6bc1-158">The main drawback from updating the old project is that you lose designer support, which may be important to you and your development team.</span></span> <span data-ttu-id="a6bc1-159">如果要继续使用设计器，则必须与旧 .NET 项目并行创建新的 .NET 项目并共享资产。</span><span class="sxs-lookup"><span data-stu-id="a6bc1-159">If you want to keep using the designer, you must create a new .NET project in parallel with the old one and share assets.</span></span> <span data-ttu-id="a6bc1-160">如果需要修改设计器中的 UI 元素，则可以切换到旧项目来执行该操作。</span><span class="sxs-lookup"><span data-stu-id="a6bc1-160">If you need to modify UI elements in the designer, you can switch to the old project to do that.</span></span> <span data-ttu-id="a6bc1-161">由于资源已链接，因此也会在 .NET 项目中对其进行更新。</span><span class="sxs-lookup"><span data-stu-id="a6bc1-161">And since assets are linked, they'll be updated in the .NET project as well.</span></span>

<span data-ttu-id="a6bc1-162">适用于 .NET 的 [SDK 样式项目](../../core/project-sdk/msbuild-props.md) 比 .NET Framework 的项目格式简单得多。</span><span class="sxs-lookup"><span data-stu-id="a6bc1-162">The [SDK-style project](../../core/project-sdk/msbuild-props.md) for .NET is a lot simpler than .NET Framework's project format.</span></span> <span data-ttu-id="a6bc1-163">除了前面提到的 `PackageReference` 条目，你无需执行更多操作。</span><span class="sxs-lookup"><span data-stu-id="a6bc1-163">Apart from the previously mentioned `PackageReference` entries, you won't need to do much more.</span></span> <span data-ttu-id="a6bc1-164">新的项目格式 [包括默认情况下具有特定扩展名的文件](../../core/project-sdk/overview.md#default-includes-and-excludes)（如 `.cs` 和 `.xaml` 文件），而无需在项目文件中显式包含这些文件。</span><span class="sxs-lookup"><span data-stu-id="a6bc1-164">The new project format [includes files with certain extensions by default](../../core/project-sdk/overview.md#default-includes-and-excludes), such as `.cs` and `.xaml` files, without the need to explicitly include them in the project file.</span></span>

#### <a name="assemblyinfo-considerations"></a><span data-ttu-id="a6bc1-165">AssemblyInfo 注意事项</span><span class="sxs-lookup"><span data-stu-id="a6bc1-165">AssemblyInfo considerations</span></span>

<span data-ttu-id="a6bc1-166">特性是在 .NET 项目上自动生成的。</span><span class="sxs-lookup"><span data-stu-id="a6bc1-166">Attributes are autogenerated on .NET projects.</span></span> <span data-ttu-id="a6bc1-167">如果项目包含 *AssemblyInfo.cs* 文件，则会复制定义，这将导致编译冲突。</span><span class="sxs-lookup"><span data-stu-id="a6bc1-167">If the project contains an *AssemblyInfo.cs* file, the definitions will be duplicated, which will cause compilation conflicts.</span></span> <span data-ttu-id="a6bc1-168">可以通过将以下条目添加到 .NET 项目文件来删除旧的 *AssemblyInfo.cs* 文件或禁用自动生成所：</span><span class="sxs-lookup"><span data-stu-id="a6bc1-168">You can delete the older *AssemblyInfo.cs* file or disable autogeneration by adding the following entry to the .NET project file:</span></span>

```xml
<Project Sdk="Microsoft.NET.Sdk">
  <PropertyGroup>
    <GenerateAssemblyInfo>false</GenerateAssemblyInfo>
  </PropertyGroup>
</Project>
```

#### <a name="resources"></a><span data-ttu-id="a6bc1-169">资源</span><span class="sxs-lookup"><span data-stu-id="a6bc1-169">Resources</span></span>

<span data-ttu-id="a6bc1-170">嵌入资源会自动包含在内，但资源不会，因此需要将资源迁移到新的项目文件。</span><span class="sxs-lookup"><span data-stu-id="a6bc1-170">Embedded resources are included automatically but resources aren't, so you need to migrate the resources to the new project file.</span></span>

#### <a name="package-references"></a><span data-ttu-id="a6bc1-171">包引用</span><span class="sxs-lookup"><span data-stu-id="a6bc1-171">Package references</span></span>

<span data-ttu-id="a6bc1-172">通过将 **packages.config 迁移到 PackageReference** 选项，可以轻松地将外部包引用移动到前面提到的新格式。</span><span class="sxs-lookup"><span data-stu-id="a6bc1-172">With the **Migrate packages.config to PackageReference** option, you can easily move your external package references to the new format as previously mentioned.</span></span>

#### <a name="update-package-references"></a><span data-ttu-id="a6bc1-173">更新包引用</span><span class="sxs-lookup"><span data-stu-id="a6bc1-173">Update package references</span></span>

<span data-ttu-id="a6bc1-174">更新发现的兼容包版本，如前一部分中所示。</span><span class="sxs-lookup"><span data-stu-id="a6bc1-174">Update the versions of the packages you've found to be compatible, as shown in the previous section.</span></span>

### <a name="fix-the-code-and-build"></a><span data-ttu-id="a6bc1-175">修复代码和生成</span><span class="sxs-lookup"><span data-stu-id="a6bc1-175">Fix the code and build</span></span>

#### <a name="microsoftwindowscompatibility"></a><span data-ttu-id="a6bc1-176">Microsoft. 兼容</span><span class="sxs-lookup"><span data-stu-id="a6bc1-176">Microsoft.Windows.Compatibility</span></span>

<span data-ttu-id="a6bc1-177">如果你的应用程序依赖于 .NET 中不可用的 Api （如注册表、Acl 或 WCF），则必须包含对包的引用 `Microsoft.Windows.Compatibility` 以添加这些特定于 Windows 的 api。</span><span class="sxs-lookup"><span data-stu-id="a6bc1-177">If your application depends on APIs that aren't available on .NET, such as Registry, ACLs, or WCF, you have to include a reference to the `Microsoft.Windows.Compatibility` package to add these Windows-specific APIs.</span></span> <span data-ttu-id="a6bc1-178">它们可在 .NET 中使用，但不会包含在内，因为它们不跨平台。</span><span class="sxs-lookup"><span data-stu-id="a6bc1-178">They work on .NET but aren't included as they aren't cross-platform.</span></span>

<span data-ttu-id="a6bc1-179">有一个名为 API Analyzer (<https://docs.microsoft.com/dotnet/standard/analyzers/api-analyzer>) 的工具，可帮助你识别与你的代码不兼容的 api。</span><span class="sxs-lookup"><span data-stu-id="a6bc1-179">There's a tool called API Analyzer (<https://docs.microsoft.com/dotnet/standard/analyzers/api-analyzer>) that helps you identify APIs that aren't compatible with your code.</span></span>

#### <a name="use-if-directives"></a><span data-ttu-id="a6bc1-180">使用 \# if 指令</span><span class="sxs-lookup"><span data-stu-id="a6bc1-180">Use \#if directives</span></span>

<span data-ttu-id="a6bc1-181">如果在面向 .NET Framework 和 .NET 时需要不同的执行路径，则应使用编译常量。</span><span class="sxs-lookup"><span data-stu-id="a6bc1-181">If you need different execution paths when targeting .NET Framework and .NET, you should use compilation constants.</span></span> <span data-ttu-id="a6bc1-182">向代码中添加一些 \# if 指令，以便为两个目标保留相同的基本代码。</span><span class="sxs-lookup"><span data-stu-id="a6bc1-182">Add some \#if directives to your code to keep the same code base for both targets.</span></span>

#### <a name="technologies-not-available-on-net"></a><span data-ttu-id="a6bc1-183">.NET 中不可用的技术</span><span class="sxs-lookup"><span data-stu-id="a6bc1-183">Technologies not available on .NET</span></span>

<span data-ttu-id="a6bc1-184">某些技术在 .NET 中不可用，例如：</span><span class="sxs-lookup"><span data-stu-id="a6bc1-184">Some technologies aren't available on .NET, such as:</span></span>

* <span data-ttu-id="a6bc1-185">AppDomain</span><span class="sxs-lookup"><span data-stu-id="a6bc1-185">AppDomains</span></span>
* <span data-ttu-id="a6bc1-186">远程处理</span><span class="sxs-lookup"><span data-stu-id="a6bc1-186">Remoting</span></span>
* <span data-ttu-id="a6bc1-187">代码访问安全性</span><span class="sxs-lookup"><span data-stu-id="a6bc1-187">Code Access Security</span></span>
* <span data-ttu-id="a6bc1-188">WCF 服务器</span><span class="sxs-lookup"><span data-stu-id="a6bc1-188">WCF Server</span></span>
* <span data-ttu-id="a6bc1-189">Windows 工作流</span><span class="sxs-lookup"><span data-stu-id="a6bc1-189">Windows Workflow</span></span>

<span data-ttu-id="a6bc1-190">这就是你在应用程序中使用这些技术时需要找一代的原因。</span><span class="sxs-lookup"><span data-stu-id="a6bc1-190">That's why you need to find a replacement for these technologies if you're using them in your application.</span></span> <span data-ttu-id="a6bc1-191">有关详细信息，请参阅 [.Net Core 和 .net 5 + 文章上的 .NET Framework 技术不可用](../../core/porting/net-framework-tech-unavailable.md) 。</span><span class="sxs-lookup"><span data-stu-id="a6bc1-191">For more information, see the [.NET Framework technologies unavailable on .NET Core and .NET 5+](../../core/porting/net-framework-tech-unavailable.md) article.</span></span>

#### <a name="regenerate-autogenerated-clients"></a><span data-ttu-id="a6bc1-192">重新生成自动生成的客户端</span><span class="sxs-lookup"><span data-stu-id="a6bc1-192">Regenerate autogenerated clients</span></span>

<span data-ttu-id="a6bc1-193">如果应用程序使用自动生成的代码（例如 WCF 客户端），则可能需要重新生成此代码以面向 .NET。</span><span class="sxs-lookup"><span data-stu-id="a6bc1-193">If your application uses autogenerated code, such as a WCF client, you may need to regenerate this code to target .NET.</span></span> <span data-ttu-id="a6bc1-194">有时，您可以找到某些缺少的引用，因为它们可能不包含在默认 .NET 程序集集的一部分中。</span><span class="sxs-lookup"><span data-stu-id="a6bc1-194">Sometimes, you can find some missing references since they may not be included as part of the default .NET assemblies set.</span></span> <span data-ttu-id="a6bc1-195">使用类似的工具 <https://apisof.net/> ，您可以轻松地找到缺少引用所在的程序集，并从 NuGet 添加该引用。</span><span class="sxs-lookup"><span data-stu-id="a6bc1-195">Using a tool like <https://apisof.net/>, you can easily locate the assembly the missing reference lives in and add it from NuGet.</span></span>

#### <a name="rolling-back-package-versions"></a><span data-ttu-id="a6bc1-196">正在回滚包版本</span><span class="sxs-lookup"><span data-stu-id="a6bc1-196">Rolling back package versions</span></span>

<span data-ttu-id="a6bc1-197">作为一般规则，我们以前提到过，你可以更好地更新每个包版本，使其与 .NET 兼容。</span><span class="sxs-lookup"><span data-stu-id="a6bc1-197">As a general rule, we've previously stated that you better update every single package version to be compatible with .NET.</span></span> <span data-ttu-id="a6bc1-198">但是，你可能会发现，面向的是更新的兼容版本的程序集不会付费。</span><span class="sxs-lookup"><span data-stu-id="a6bc1-198">However, you can find that targeting an updated and compatible version of an assembly just doesn't pay off.</span></span> <span data-ttu-id="a6bc1-199">如果更改成本不是可接受的，则可以考虑回滚包版本，保留 .NET Framework 使用的版本。</span><span class="sxs-lookup"><span data-stu-id="a6bc1-199">If the cost of change isn't acceptable, you can consider rolling back package versions keeping the ones you use on .NET Framework.</span></span> <span data-ttu-id="a6bc1-200">尽管它们可能不针对 .NET，但它们应该能够正常工作，除非它们调用了某些不受支持的 Api。</span><span class="sxs-lookup"><span data-stu-id="a6bc1-200">Although they may not be targeting .NET, they should work well unless they call some unsupported APIs.</span></span>

### <a name="run-and-test"></a><span data-ttu-id="a6bc1-201">运行和测试</span><span class="sxs-lookup"><span data-stu-id="a6bc1-201">Run and test</span></span>

<span data-ttu-id="a6bc1-202">一旦您的应用程序生成无错误，就可以通过测试每个功能开始迁移的最后一步。</span><span class="sxs-lookup"><span data-stu-id="a6bc1-202">Once you have your application building with no errors, you can start the last step of the migration by testing every functionality.</span></span>

<span data-ttu-id="a6bc1-203">在最后一步中，你可以找到几个不同的问题，具体取决于你的应用程序的复杂性以及你使用的依赖项和 Api。</span><span class="sxs-lookup"><span data-stu-id="a6bc1-203">In this final step, you can find several different issues depending on the complexity of your application and the dependencies and APIs you're using.</span></span>

<span data-ttu-id="a6bc1-204">例如，如果使用配置文件 (*app.config*) ，则在运行时可能会发现一些错误，如配置部分不存在。</span><span class="sxs-lookup"><span data-stu-id="a6bc1-204">For example, if you use configuration files (*app.config*), you may find some errors at run time like Configuration Sections not present.</span></span> <span data-ttu-id="a6bc1-205">使用 `Microsoft.Extensions.Configuration` NuGet 程序包应修复该错误。</span><span class="sxs-lookup"><span data-stu-id="a6bc1-205">Using the `Microsoft.Extensions.Configuration` NuGet package should fix that error.</span></span>

<span data-ttu-id="a6bc1-206">错误的另一个原因是使用 `BeginInvoke` 和方法， `EndInvoke` 因为它们在 .net 上不受支持。</span><span class="sxs-lookup"><span data-stu-id="a6bc1-206">Another reason for errors is the use of the `BeginInvoke` and `EndInvoke` methods because they aren't supported on .NET.</span></span> <span data-ttu-id="a6bc1-207">.NET 不支持它们，因为它们依赖于远程处理，而 .NET 上并不存在。</span><span class="sxs-lookup"><span data-stu-id="a6bc1-207">They aren't supported on .NET because they have a dependency on Remoting, which doesn't exist on .NET.</span></span> <span data-ttu-id="a6bc1-208">若要解决此问题，请尝试 `await` 在可用) 或方法时使用关键字 (<xref:System.Threading.Tasks.Task.Run%2A?displayProperty=nameWithType> 。</span><span class="sxs-lookup"><span data-stu-id="a6bc1-208">To solve this issue, try to use the `await` keyword (when available) or the <xref:System.Threading.Tasks.Task.Run%2A?displayProperty=nameWithType> method.</span></span>

<span data-ttu-id="a6bc1-209">你可以使用兼容性分析器来识别代码中的 Api 和代码模式，这可能会在运行时使用 .NET 引起问题。</span><span class="sxs-lookup"><span data-stu-id="a6bc1-209">You can use compatibility analyzers to let you identify APIs and code patterns in your code that can potentially cause problems at run time with .NET.</span></span> <span data-ttu-id="a6bc1-210"><https://github.com/dotnet/platform-compat>在项目上，请参阅并使用 .NET API 分析器。</span><span class="sxs-lookup"><span data-stu-id="a6bc1-210">Go to <https://github.com/dotnet/platform-compat> and use the .NET API analyzer on your project.</span></span>

## <a name="migrating-a-windows-forms-application"></a><span data-ttu-id="a6bc1-211">迁移 Windows 窗体应用程序</span><span class="sxs-lookup"><span data-stu-id="a6bc1-211">Migrating a Windows Forms application</span></span>

<span data-ttu-id="a6bc1-212">为了展示 Windows 窗体应用程序的完整迁移过程，我们选择了在中迁移可用的 eShop 示例应用程序 <https://github.com/dotnet-architecture/eShopModernizing/tree/master/eShopLegacyNTier/src/eShopWinForms> 。</span><span class="sxs-lookup"><span data-stu-id="a6bc1-212">To showcase a complete migration process of a Windows Forms application, we've chosen to migrate the eShop sample application available at <https://github.com/dotnet-architecture/eShopModernizing/tree/master/eShopLegacyNTier/src/eShopWinForms>.</span></span> <span data-ttu-id="a6bc1-213">可以在中找到迁移的完整结果 <https://github.com/dotnet-architecture/eShopModernizing/tree/master/eShopModernizedNTier/src/eShopWinForms> 。</span><span class="sxs-lookup"><span data-stu-id="a6bc1-213">You can find the complete result of the migration at <https://github.com/dotnet-architecture/eShopModernizing/tree/master/eShopModernizedNTier/src/eShopWinForms>.</span></span>

<span data-ttu-id="a6bc1-214">此应用程序显示产品目录，并允许用户导航、筛选和搜索产品。</span><span class="sxs-lookup"><span data-stu-id="a6bc1-214">This application shows a product catalog and allows the user to navigate, filter, and search for products.</span></span> <span data-ttu-id="a6bc1-215">从体系结构的角度来看，应用依赖于充当后端数据库外观的外部 WCF 服务。</span><span class="sxs-lookup"><span data-stu-id="a6bc1-215">From an architecture point of view, the app relies on an external WCF service that serves as a façade to a back-end database.</span></span>

<span data-ttu-id="a6bc1-216">可以在下图中看到主应用程序窗口：</span><span class="sxs-lookup"><span data-stu-id="a6bc1-216">You can see the main application window in the following picture:</span></span>

![主应用程序窗口](./media/example-migration-core/main-application-window.png)

<span data-ttu-id="a6bc1-218">如果打开 *.csproj* 项目文件，则可以看到如下所示的内容：</span><span class="sxs-lookup"><span data-stu-id="a6bc1-218">If you open the *.csproj* project file, you can see something like this:</span></span>

![.Csproj 文件内容的屏幕截图](./media/example-migration-core/csproj-file.png)

<span data-ttu-id="a6bc1-220">如前所述，.NET 项目具有更精简的样式，需要将项目结构迁移到新的 .NET SDK 样式。</span><span class="sxs-lookup"><span data-stu-id="a6bc1-220">As previously mentioned, .NET project has a more compact style and you need to migrate the project structure to the new .NET SDK style.</span></span>

<span data-ttu-id="a6bc1-221">在解决方案资源管理器中，右键单击 Windows 窗体项目，然后选择 "**卸载项目**" "  >  **编辑**"。</span><span class="sxs-lookup"><span data-stu-id="a6bc1-221">In the Solution Explorer, right click on the Windows Forms project and select **Unload Project** > **Edit**.</span></span>

<span data-ttu-id="a6bc1-222">现在可以更新 .csproj 文件。</span><span class="sxs-lookup"><span data-stu-id="a6bc1-222">Now you can update the .csproj file.</span></span> <span data-ttu-id="a6bc1-223">你将删除整个内容，并将其替换为以下代码：</span><span class="sxs-lookup"><span data-stu-id="a6bc1-223">You'll delete the entire content and replace it with the following code:</span></span>

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

<span data-ttu-id="a6bc1-224">保存并重新加载项目。</span><span class="sxs-lookup"><span data-stu-id="a6bc1-224">Save and reload the project.</span></span> <span data-ttu-id="a6bc1-225">你现在已经完成了项目文件的更新，并且项目面向 .NET。</span><span class="sxs-lookup"><span data-stu-id="a6bc1-225">You're now done updating the project file and the project is targeting the .NET.</span></span>

<span data-ttu-id="a6bc1-226">如果此时编译项目，会发现一些与 WCF 客户端引用相关的错误。</span><span class="sxs-lookup"><span data-stu-id="a6bc1-226">If you compile the project at this point, you'll find some errors related to the WCF client reference.</span></span> <span data-ttu-id="a6bc1-227">由于此代码是自动生成的，因此必须将其重新生成为目标 .NET。</span><span class="sxs-lookup"><span data-stu-id="a6bc1-227">Since this code is autogenerated, you must regenerate it to target .NET.</span></span>

![Visual Studio 上的编译错误的屏幕截图](./media/example-migration-core/winforms-compilation-errors.png)

<span data-ttu-id="a6bc1-229">删除 *Reference.cs* 文件并生成新的服务客户端。</span><span class="sxs-lookup"><span data-stu-id="a6bc1-229">Delete the *Reference.cs* file and generate a new Service Client.</span></span>

<span data-ttu-id="a6bc1-230">右键单击 **连接的服务** ，然后选择 " **添加连接的服务** " 选项。</span><span class="sxs-lookup"><span data-stu-id="a6bc1-230">Right-click on **Connected Services** and select the **Add Connected Service** option.</span></span>

![选中 "添加连接的服务" 选项的 "连接的服务" 菜单的屏幕截图](./media/example-migration-core/add-connected-service.png)

<span data-ttu-id="a6bc1-232">此时将打开 "连接的服务" 窗口。</span><span class="sxs-lookup"><span data-stu-id="a6bc1-232">The Connected Services window opens.</span></span> <span data-ttu-id="a6bc1-233">选择 " **MICROSOFT WCF Web 服务** " 选项。</span><span class="sxs-lookup"><span data-stu-id="a6bc1-233">Select the **Microsoft WCF Web Service** option.</span></span>

![连接的服务窗口的屏幕截图](./media/example-migration-core/connected-services-window.png)

<span data-ttu-id="a6bc1-235">如果你在此示例中的同一解决方案中有 WCF 服务，则可以选择 " **发现** " 选项，而不是指定服务 URL。</span><span class="sxs-lookup"><span data-stu-id="a6bc1-235">If you have the WCF Service in the same solution as we have in this example, you can select the **Discover** option instead of specifying a service URL.</span></span>

!["配置 WCF Web 服务引用" 窗口的屏幕截图](./media/example-migration-core/configure-wcf-reference.png)

<span data-ttu-id="a6bc1-237">找到该服务后，该工具将反映该服务实现的 API 协定。</span><span class="sxs-lookup"><span data-stu-id="a6bc1-237">Once the service is located, the tool reflects the API contract implemented by the service.</span></span> <span data-ttu-id="a6bc1-238">将命名空间的名称更改为，如下 `eShopServiceReference` 图所示：</span><span class="sxs-lookup"><span data-stu-id="a6bc1-238">Change the name of the namespace to be `eShopServiceReference` as shown in the following image:</span></span>

![屏幕截图 API 协定和命名空间已更改](./media/example-migration-core/api-contract-namespace.png)

<span data-ttu-id="a6bc1-240">选择 " **完成** " 按钮。</span><span class="sxs-lookup"><span data-stu-id="a6bc1-240">Select the **Finish** button.</span></span> <span data-ttu-id="a6bc1-241">一段时间后，你将看到生成的代码。</span><span class="sxs-lookup"><span data-stu-id="a6bc1-241">After a while, you'll see the generated code.</span></span>

<span data-ttu-id="a6bc1-242">应会看到三个自动生成的文件：</span><span class="sxs-lookup"><span data-stu-id="a6bc1-242">You should see three autogenerated files:</span></span>

1. <span data-ttu-id="a6bc1-243">*入门*：指向 GitHub 的链接，以提供有关 WCF 的某些信息。</span><span class="sxs-lookup"><span data-stu-id="a6bc1-243">*Getting Started*: a link to GitHub to provide some information on WCF.</span></span>
2. <span data-ttu-id="a6bc1-244">*ConnectedService.js*：用于连接到服务的配置参数。</span><span class="sxs-lookup"><span data-stu-id="a6bc1-244">*ConnectedService.json*: configuration parameters to connect to the service.</span></span>
3. <span data-ttu-id="a6bc1-245">*Reference.cs*：实际 WCF 客户端代码。</span><span class="sxs-lookup"><span data-stu-id="a6bc1-245">*Reference.cs*: the actual WCF client code.</span></span>

![包含三个自动生成的文件的解决方案资源管理器窗口的屏幕截图](./media/example-migration-core/autogenerated-files.png)

<span data-ttu-id="a6bc1-247">如果再次编译，则会看到多个错误来自 *Helper* 文件夹内的 *.cs* 文件。</span><span class="sxs-lookup"><span data-stu-id="a6bc1-247">If you compile again, you'll see many errors coming from *.cs* files inside the *Helper* folder.</span></span> <span data-ttu-id="a6bc1-248">此文件夹存在于 .NET Framework 版本中，但不包含在旧的 *.csproj* 中。</span><span class="sxs-lookup"><span data-stu-id="a6bc1-248">This folder was present in the .NET Framework version but not included in the old *.csproj*.</span></span> <span data-ttu-id="a6bc1-249">但对于新的 SDK 样式项目，默认情况下会包括项目文件位置下的每个代码文件。</span><span class="sxs-lookup"><span data-stu-id="a6bc1-249">But with the new SDK-style project, every code file present underneath the project file location is included by default.</span></span> <span data-ttu-id="a6bc1-250">也就是说，新的 .NET Core 项目会尝试编译 *Helper* 文件夹内的文件。</span><span class="sxs-lookup"><span data-stu-id="a6bc1-250">That is, the new .NET Core project tries to compile the files inside the *Helper* folder.</span></span> <span data-ttu-id="a6bc1-251">由于不需要此文件夹，因此可以安全地将其删除。</span><span class="sxs-lookup"><span data-stu-id="a6bc1-251">Since that folder isn't needed, you can safely delete it.</span></span>

<span data-ttu-id="a6bc1-252">如果再次编译项目并执行它，将看不到产品图像。</span><span class="sxs-lookup"><span data-stu-id="a6bc1-252">If you compile the project again and execute it, you won't see the product images.</span></span> <span data-ttu-id="a6bc1-253">问题在于，文件的路径略有变化。</span><span class="sxs-lookup"><span data-stu-id="a6bc1-253">The problem is that now the path to the files has slightly changed.</span></span> <span data-ttu-id="a6bc1-254">若要解决此问题，需要在路径中添加另一个级别的深度，并在文件中进行更新 `CatalogView.cs` ：</span><span class="sxs-lookup"><span data-stu-id="a6bc1-254">To fix this issue, you need to add another level of depth in the path, updating in the file `CatalogView.cs` the line:</span></span>

```csharp
string image_name = Environment.CurrentDirectory + "\\..\\..\\Assets\\Images\\Catalog\\" + catalogItems.Picturefilename;
```

<span data-ttu-id="a6bc1-255">设置为</span><span class="sxs-lookup"><span data-stu-id="a6bc1-255">to</span></span>

```csharp
string image_name = Environment.CurrentDirectory + "\\..\\..\\..\\Assets\\Images\\Catalog\\" + catalogItems.Picturefilename;
```

<span data-ttu-id="a6bc1-256">在此更改后，可以检查应用程序是否在 .NET Core 上按预期启动并运行。</span><span class="sxs-lookup"><span data-stu-id="a6bc1-256">After this change, you can check that the application launches and runs as expected on .NET Core.</span></span>

## <a name="migrating-a-wpf-application"></a><span data-ttu-id="a6bc1-257">迁移 WPF 应用程序</span><span class="sxs-lookup"><span data-stu-id="a6bc1-257">Migrating a WPF application</span></span>

<span data-ttu-id="a6bc1-258">我们将使用 `Shop.ClassicWPF` 示例应用程序来执行迁移。</span><span class="sxs-lookup"><span data-stu-id="a6bc1-258">We'll use the `Shop.ClassicWPF` sample application to perform the migration.</span></span> <span data-ttu-id="a6bc1-259">下图显示了迁移之前的应用程序的屏幕截图：</span><span class="sxs-lookup"><span data-stu-id="a6bc1-259">The following image shows a screenshot of the app before migration:</span></span>

![迁移之前的示例应用](./media/example-migration-core/app-before-migration.png)

<span data-ttu-id="a6bc1-261">此应用程序使用本地 SQL Server Express 数据库来保存产品目录信息。</span><span class="sxs-lookup"><span data-stu-id="a6bc1-261">This application uses a local SQL Server Express database to hold the product catalog information.</span></span> <span data-ttu-id="a6bc1-262">可以直接从 WPF 应用程序访问此数据库。</span><span class="sxs-lookup"><span data-stu-id="a6bc1-262">This database is accessed directly from the WPF application.</span></span>

<span data-ttu-id="a6bc1-263">首先，必须将 *.csproj* 文件更新为 .net Core 应用程序使用的新 SDK 样式。</span><span class="sxs-lookup"><span data-stu-id="a6bc1-263">First, you must update the *.csproj* file to the new SDK style used by .NET Core applications.</span></span> <span data-ttu-id="a6bc1-264">你将按照 Windows 窗体迁移中所述的相同步骤进行操作：卸载项目、打开 *.csproj* 文件、更新其内容，并重新加载项目。</span><span class="sxs-lookup"><span data-stu-id="a6bc1-264">You'll follow the same steps described in the Windows Forms migration: you'll unload the project, open the *.csproj* file, update its contents, and reload the project.</span></span>

<span data-ttu-id="a6bc1-265">在这种情况下，请删除 *.csproj* 文件的所有内容，并将其替换为以下代码：</span><span class="sxs-lookup"><span data-stu-id="a6bc1-265">In this case, delete all the content of the *.csproj* file and replace it with the following code:</span></span>

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

<span data-ttu-id="a6bc1-266">如果重新加载并编译该项目，则会收到以下错误：</span><span class="sxs-lookup"><span data-stu-id="a6bc1-266">If you reload the project and compile it, you'll get the following error:</span></span>

![Visual Studio 上的编译错误的屏幕截图](./media/example-migration-core/wpf-compilation-error.png)

<span data-ttu-id="a6bc1-268">由于已删除所有 *.csproj* 内容，因此你丢失了旧项目中的项目引用规范。</span><span class="sxs-lookup"><span data-stu-id="a6bc1-268">Since you've deleted all the *.csproj* contents, you've lost a project reference specification present in the old project.</span></span> <span data-ttu-id="a6bc1-269">只需将此行添加到 *.csproj* 文件，即可包含项目引用：</span><span class="sxs-lookup"><span data-stu-id="a6bc1-269">You just need to add this line to the *.csproj* file to include the project reference back:</span></span>

```xml
<ItemGroup>
    <ProjectReference Include="..\\eShop.SqlProvider\\eShop.SqlProvider.csproj" />
<ItemGroup>
```

<span data-ttu-id="a6bc1-270">还可以通过右键单击 " **依赖项** " 节点并选择 " **添加项目引用**" 来让 Visual Studio 帮助你。</span><span class="sxs-lookup"><span data-stu-id="a6bc1-270">You can also let Visual Studio help you by right-clicking on the **Dependencies** node and selecting **Add Project Reference**.</span></span> <span data-ttu-id="a6bc1-271">从解决方案中选择项目，然后单击 **"确定"**：</span><span class="sxs-lookup"><span data-stu-id="a6bc1-271">Select the project from the solution and click **OK**:</span></span>

![选择了 eShop SqlProvider 项目的 "引用管理器" 对话框的屏幕截图](./media/example-migration-core/reference-manager.png)

<span data-ttu-id="a6bc1-273">添加缺少的项目引用后，应用程序将在 .NET 上按预期方式编译和运行。</span><span class="sxs-lookup"><span data-stu-id="a6bc1-273">Once you add the missing project reference, the application compiles and runs as expected on .NET.</span></span>

>[!div class="step-by-step"]
><span data-ttu-id="a6bc1-274">[上一页](windows-migration.md)
>[下一页](deploy-modern-applications.md)</span><span class="sxs-lookup"><span data-stu-id="a6bc1-274">[Previous](windows-migration.md)
[Next](deploy-modern-applications.md)</span></span>
