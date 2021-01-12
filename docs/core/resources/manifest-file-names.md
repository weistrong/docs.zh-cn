---
title: MSBuild 如何生成清单文件名
description: 介绍编译时 MSBuild 所生成资源清单文件名的名称的影响因素。
ms.date: 05/08/2020
ms.topic: conceptual
ms.openlocfilehash: 2e0461e34bbd7f8da35bea1db1913a32915c7117
ms.sourcegitcommit: 7ef96827b161ef3fcde75f79d839885632e26ef1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/07/2021
ms.locfileid: "97970676"
---
# <a name="how-resource-manifest-files-are-named"></a><span data-ttu-id="032b5-103">资源清单文件的命名方式</span><span class="sxs-lookup"><span data-stu-id="032b5-103">How resource manifest files are named</span></span>

<span data-ttu-id="032b5-104">当 MSBuild 编译 .NET Core 项目时，文件扩展名为 .resx 的 XML 资源文件将转换为二进制 .resources 文件 。</span><span class="sxs-lookup"><span data-stu-id="032b5-104">When MSBuild compiles a .NET Core project, XML resource files, which have the *.resx* file extension, are converted into binary *.resources* files.</span></span> <span data-ttu-id="032b5-105">该二进制文件会嵌入编译器的输出中，并且可以由 <xref:System.Resources.ResourceManager> 读取。</span><span class="sxs-lookup"><span data-stu-id="032b5-105">The binary files are embedded into the output of the compiler and can be read by the <xref:System.Resources.ResourceManager>.</span></span> <span data-ttu-id="032b5-106">本文介绍 MSBuild 如何为每个 .resources 文件选择名称。</span><span class="sxs-lookup"><span data-stu-id="032b5-106">This article describes how MSBuild chooses a name for each *.resources* file.</span></span>

> [!TIP]
> <span data-ttu-id="032b5-107">如果将资源项显式添加到项目文件中，并且 [.NET Core 的默认 include glob 也包含该项](../project-sdk/overview.md#default-includes-and-excludes)，则会出现生成错误。</span><span class="sxs-lookup"><span data-stu-id="032b5-107">If you explicitly add a resource item to your project file, and it's also [included with the default include globs for .NET Core](../project-sdk/overview.md#default-includes-and-excludes), you will get a build error.</span></span> <span data-ttu-id="032b5-108">要以资源文件的形式手动包含 `EmbeddedResource` 项，请将 `EnableDefaultEmbeddedResourceItems` 属性设置为 false。</span><span class="sxs-lookup"><span data-stu-id="032b5-108">To manually include resource files as `EmbeddedResource` items, set the `EnableDefaultEmbeddedResourceItems` property to false.</span></span>

## <a name="default-name"></a><span data-ttu-id="032b5-109">默认名称</span><span class="sxs-lookup"><span data-stu-id="032b5-109">Default name</span></span>

<span data-ttu-id="032b5-110">在 .NET Core 3.0 及更高版本中，同时满足以下两个条件时，将使用资源清单的默认名称：</span><span class="sxs-lookup"><span data-stu-id="032b5-110">In .NET Core 3.0 and later, the default name for a resource manifest is used when both of the following conditions are met:</span></span>

- <span data-ttu-id="032b5-111">资源文件未作为具有 `LogicalName`、`ManifestResourceName` 或 `DependentUpon` 元数据的 `EmbeddedResource` 项显式包含在项目文件中。</span><span class="sxs-lookup"><span data-stu-id="032b5-111">The resource file is not explicitly included in the project file as an `EmbeddedResource` item with `LogicalName`, `ManifestResourceName`, or `DependentUpon` metadata.</span></span>
- <span data-ttu-id="032b5-112">项目文件中未将 `EmbeddedResourceUseDependentUponConvention` 属性设置为 `false`。</span><span class="sxs-lookup"><span data-stu-id="032b5-112">The `EmbeddedResourceUseDependentUponConvention` property is not set to `false` in the project file.</span></span> <span data-ttu-id="032b5-113">默认情况下，此属性设置为 `true`。</span><span class="sxs-lookup"><span data-stu-id="032b5-113">By default, this property is set to `true`.</span></span> <span data-ttu-id="032b5-114">有关详细信息，请参阅 [EmbeddedResourceUseDependentUponConvention](../project-sdk/msbuild-props.md#embeddedresourceusedependentuponconvention)。</span><span class="sxs-lookup"><span data-stu-id="032b5-114">For more information, see [EmbeddedResourceUseDependentUponConvention](../project-sdk/msbuild-props.md#embeddedresourceusedependentuponconvention).</span></span>

<span data-ttu-id="032b5-115">如果资源文件与具有同一根文件名的源文件（.cs 或 .vb）并置，清单文件名便使用源文件中定义的第一种类型的全名 。</span><span class="sxs-lookup"><span data-stu-id="032b5-115">If the resource file is colocated with a source file (*.cs* or *.vb*) of the same root file name, the full name of the first type that's defined in the source file is used for the manifest file name.</span></span> <span data-ttu-id="032b5-116">例如，如果 `MyNamespace.Form1` 是 Form1.cs 中定义的第一种类型，并且 Form1.cs 与 Form1.resx 并置，则该资源文件的生成清单名称是 MyNamespace.Form1.resources   。</span><span class="sxs-lookup"><span data-stu-id="032b5-116">For example, if `MyNamespace.Form1` is the first type defined in *Form1.cs*, and *Form1.cs* is colocated with *Form1.resx*, the generated manifest name for that resource file is *MyNamespace.Form1.resources*.</span></span>

## <a name="logicalname-metadata"></a><span data-ttu-id="032b5-117">LogicalName 元数据</span><span class="sxs-lookup"><span data-stu-id="032b5-117">LogicalName metadata</span></span>

<span data-ttu-id="032b5-118">如果资源文件作为具有 `LogicalName` 元数据的 `EmbeddedResource` 项显式包含在项目文件中，则将 `LogicalName` 值用作清单名称。</span><span class="sxs-lookup"><span data-stu-id="032b5-118">If a resource file is explicitly included in the project file as an `EmbeddedResource` item with `LogicalName` metadata, the `LogicalName` value is used as the manifest name.</span></span> <span data-ttu-id="032b5-119">`LogicalName` 优先于其他任何元数据或设置。</span><span class="sxs-lookup"><span data-stu-id="032b5-119">`LogicalName` takes precedence over any other metadata or setting.</span></span>

<span data-ttu-id="032b5-120">例如，以下项目文件片段中定义的资源文件的清单名称是 SomeName.resources。</span><span class="sxs-lookup"><span data-stu-id="032b5-120">For example, the manifest name for the resource file that's defined in the following project file snippet is *SomeName.resources*.</span></span>

```xml
<EmbeddedResource Include="X.resx" LogicalName="SomeName.resources" />
```

<span data-ttu-id="032b5-121">- 或 -</span><span class="sxs-lookup"><span data-stu-id="032b5-121">-or-</span></span>

```xml
<EmbeddedResource Include="X.fr-FR.resx" LogicalName="SomeName.resources" />
```

## <a name="manifestresourcename-metadata"></a><span data-ttu-id="032b5-122">ManifestResourceName 元数据</span><span class="sxs-lookup"><span data-stu-id="032b5-122">ManifestResourceName metadata</span></span>

<span data-ttu-id="032b5-123">如果资源文件作为具有 `ManifestResourceName` 元数据（并且 `LogicalName` 不存在）的 `EmbeddedResource` 项显式包含在项目文件中，则 `ManifestResourceName` 值与文件扩展名 .resources 一起用作清单文件名。</span><span class="sxs-lookup"><span data-stu-id="032b5-123">If a resource file is explicitly included in the project file as an `EmbeddedResource` item with `ManifestResourceName` metadata (and `LogicalName` is absent), the `ManifestResourceName` value, combined with the file extension *.resources*, is used as the manifest file name.</span></span>

<span data-ttu-id="032b5-124">例如，以下项目文件片段中定义的资源文件的清单名称是 SomeName.resources。</span><span class="sxs-lookup"><span data-stu-id="032b5-124">For example, the manifest name for the resource file that's defined in the following project file snippet is *SomeName.resources*.</span></span>

```xml
<EmbeddedResource Include="X.resx" ManifestResourceName="SomeName" />
```

<span data-ttu-id="032b5-125">以下项目文件片段中定义的资源文件的清单名称是 SomeName.fr-FR.resources。</span><span class="sxs-lookup"><span data-stu-id="032b5-125">The manifest name for the resource file that's defined in the following project file snippet is *SomeName.fr-FR.resources*.</span></span>

```xml
<EmbeddedResource Include="X.fr-FR.resx" ManifestResourceName="SomeName.fr-FR" />
```

## <a name="dependentupon-metadata"></a><span data-ttu-id="032b5-126">DependentUpon 元数据</span><span class="sxs-lookup"><span data-stu-id="032b5-126">DependentUpon metadata</span></span>

<span data-ttu-id="032b5-127">如果资源文件作为具有 `DependentUpon` 元数据（并且 `LogicalName` 和 `ManifestResourceName` 不存在）的 `EmbeddedResource` 项显式包含在项目文件中，则将 `DependentUpon` 定义的源文件中的信息用于资源清单文件名。</span><span class="sxs-lookup"><span data-stu-id="032b5-127">If a resource file is explicitly included in the project file as an `EmbeddedResource` item with `DependentUpon` metadata (and `LogicalName` and `ManifestResourceName` are absent), information from the source file defined by `DependentUpon` is used for the resource manifest file name.</span></span> <span data-ttu-id="032b5-128">具体来说，清单名称中会使用源文件中定义的第一种类型的名称，如下所示：*Namespace.Classname\[.Culture].resources*。</span><span class="sxs-lookup"><span data-stu-id="032b5-128">Specifically, the name of the first type that's defined in the source file is used in the manifest name as follows: *Namespace.Classname\[.Culture].resources*.</span></span>

<span data-ttu-id="032b5-129">例如，在以下项目文件片段中定义的资源文件的清单名称是 Namespace.Classname.resources（其中 `Namespace.Classname` 是 MyTypes.cs 中定义的第一个类） 。</span><span class="sxs-lookup"><span data-stu-id="032b5-129">For example, the manifest name for the resource file that's defined in the following project file snippet is *Namespace.Classname.resources* (where `Namespace.Classname` is the first class that's defined in *MyTypes.cs*).</span></span>

```xml
<EmbeddedResource Include="X.resx" DependentUpon="MyTypes.cs">
```

<span data-ttu-id="032b5-130">在以下项目文件片段中定义的资源文件的清单名称是 Namespace.Classname.fr-FR.resources（其中 `Namespace.Classname` 是 MyTypes.cs 中定义的第一个类） 。</span><span class="sxs-lookup"><span data-stu-id="032b5-130">The manifest name for the resource file that's defined in the following project file snippet is *Namespace.Classname.fr-FR.resources* (where `Namespace.Classname` is the first class that's defined in *MyTypes.cs*).</span></span>

```xml
<EmbeddedResource Include="X.fr-FR.resx" DependentUpon="MyTypes.cs">
```

## <a name="embeddedresourceusedependentuponconvention-property"></a><span data-ttu-id="032b5-131">EmbeddedResourceUseDependentUponConvention 属性</span><span class="sxs-lookup"><span data-stu-id="032b5-131">EmbeddedResourceUseDependentUponConvention property</span></span>

<span data-ttu-id="032b5-132">如果在项目文件中将 `EmbeddedResourceUseDependentUponConvention` 设置为 `false`，则每个资源清单文件名都基于项目的根命名空间以及从项目根目录到 .resx 文件的相对路径。</span><span class="sxs-lookup"><span data-stu-id="032b5-132">If `EmbeddedResourceUseDependentUponConvention` is set to `false` in the project file, each resource manifest file name is based off the root namespace for the project and the relative path from the project root to the *.resx* file.</span></span> <span data-ttu-id="032b5-133">更具体地说，生成的资源清单文件名是 *RootNamespace.RelativePathWithDotsForSlashes.\[Culture.]resources*。</span><span class="sxs-lookup"><span data-stu-id="032b5-133">More specifically, the generated resource manifest file name is *RootNamespace.RelativePathWithDotsForSlashes.\[Culture.]resources*.</span></span> <span data-ttu-id="032b5-134">这也是用于在低于 3.0 的 .NET Core 版本中生成清单名称的逻辑。</span><span class="sxs-lookup"><span data-stu-id="032b5-134">This is also the logic used to generate manifest names in .NET Core versions prior to 3.0.</span></span>

> [!NOTE]
>
> - <span data-ttu-id="032b5-135">如果未定义 `RootNamespace`，则默认为项目名称。</span><span class="sxs-lookup"><span data-stu-id="032b5-135">If `RootNamespace` is not defined, it defaults to the project name.</span></span>
> - <span data-ttu-id="032b5-136">如果为项目文件中的 `EmbeddedResource` 项指定了 `LogicalName`、`ManifestResourceName` 或 `DependentUpon` 元数据，则该命名规则不适用于该资源文件。</span><span class="sxs-lookup"><span data-stu-id="032b5-136">If `LogicalName`, `ManifestResourceName`, or `DependentUpon` metadata is specified for an `EmbeddedResource` item in the project file, this naming rule does not apply to that resource file.</span></span>

## <a name="see-also"></a><span data-ttu-id="032b5-137">请参阅</span><span class="sxs-lookup"><span data-stu-id="032b5-137">See also</span></span>

- [<span data-ttu-id="032b5-138">清单资源的命名方式</span><span class="sxs-lookup"><span data-stu-id="032b5-138">How Manifest Resource Naming Works</span></span>](https://gist.github.com/BenVillalobos/041673b9a73bec60fdc3bf0f86fae62a)
- [<span data-ttu-id="032b5-139">.NET Core SDK 项目的 MSBuild 属性</span><span class="sxs-lookup"><span data-stu-id="032b5-139">MSBuild properties for .NET Core SDK projects</span></span>](../project-sdk/msbuild-props.md)
- [<span data-ttu-id="032b5-140">MSBuild 中断性变更</span><span class="sxs-lookup"><span data-stu-id="032b5-140">MSBuild breaking changes</span></span>](../compatibility/msbuild.md)
