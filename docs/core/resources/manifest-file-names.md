---
title: MSBuild 如何生成清单文件名
description: 介绍编译时 MSBuild 所生成资源清单文件名的名称的影响因素。
ms.date: 05/08/2020
ms.topic: conceptual
ms.openlocfilehash: 383bf6a077b0631e70ddaa4721b20e992127a73c
ms.sourcegitcommit: 488aced39b5f374bc0a139a4993616a54d15baf0
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/12/2020
ms.locfileid: "97866379"
---
# <a name="how-resource-manifest-files-are-named"></a>资源清单文件的命名方式

当 MSBuild 编译 .NET Core 项目时，文件扩展名为 .resx 的 XML 资源文件将转换为二进制 .resources 文件 。 该二进制文件会嵌入编译器的输出中，并且可以由 <xref:System.Resources.ResourceManager> 读取。 本文介绍 MSBuild 如何为每个 .resources 文件选择名称。

> [!TIP]
> 如果将资源项显式添加到项目文件中，并且 [.NET Core 的默认 include glob 也包含该项](../project-sdk/overview.md#default-compilation-includes)，则会出现生成错误。 要以资源文件的形式手动包含 `EmbeddedResource` 项，请将 `EnableDefaultEmbeddedResourceItems` 属性设置为 false。

## <a name="default-name"></a>默认名称

在 .NET Core 3.0 及更高版本中，同时满足以下两个条件时，将使用资源清单的默认名称：

- 资源文件未作为具有 `LogicalName`、`ManifestResourceName` 或 `DependentUpon` 元数据的 `EmbeddedResource` 项显式包含在项目文件中。
- 项目文件中未将 `EmbeddedResourceUseDependentUponConvention` 属性设置为 `false`。 默认情况下，此属性设置为 `true`。 有关详细信息，请参阅 [EmbeddedResourceUseDependentUponConvention](../project-sdk/msbuild-props.md#embeddedresourceusedependentuponconvention)。

如果资源文件与具有同一根文件名的源文件（.cs 或 .vb）并置，清单文件名便使用源文件中定义的第一种类型的全名 。 例如，如果 `MyNamespace.Form1` 是 Form1.cs 中定义的第一种类型，并且 Form1.cs 与 Form1.resx 并置，则该资源文件的生成清单名称是 MyNamespace.Form1.resources   。

## <a name="logicalname-metadata"></a>LogicalName 元数据

如果资源文件作为具有 `LogicalName` 元数据的 `EmbeddedResource` 项显式包含在项目文件中，则将 `LogicalName` 值用作清单名称。 `LogicalName` 优先于其他任何元数据或设置。

例如，以下项目文件片段中定义的资源文件的清单名称是 SomeName.resources。

```xml
<EmbeddedResource Include="X.resx" LogicalName="SomeName.resources" />
```

- 或 -

```xml
<EmbeddedResource Include="X.fr-FR.resx" LogicalName="SomeName.resources" />
```

## <a name="manifestresourcename-metadata"></a>ManifestResourceName 元数据

如果资源文件作为具有 `ManifestResourceName` 元数据（并且 `LogicalName` 不存在）的 `EmbeddedResource` 项显式包含在项目文件中，则 `ManifestResourceName` 值与文件扩展名 .resources 一起用作清单文件名。

例如，以下项目文件片段中定义的资源文件的清单名称是 SomeName.resources。

```xml
<EmbeddedResource Include="X.resx" ManifestResourceName="SomeName" />
```

以下项目文件片段中定义的资源文件的清单名称是 SomeName.fr-FR.resources。

```xml
<EmbeddedResource Include="X.fr-FR.resx" ManifestResourceName="SomeName.fr-FR" />
```

## <a name="dependentupon-metadata"></a>DependentUpon 元数据

如果资源文件作为具有 `DependentUpon` 元数据（并且 `LogicalName` 和 `ManifestResourceName` 不存在）的 `EmbeddedResource` 项显式包含在项目文件中，则将 `DependentUpon` 定义的源文件中的信息用于资源清单文件名。 具体来说，清单名称中会使用源文件中定义的第一种类型的名称，如下所示：*Namespace.Classname\[.Culture].resources*。

例如，在以下项目文件片段中定义的资源文件的清单名称是 Namespace.Classname.resources（其中 `Namespace.Classname` 是 MyTypes.cs 中定义的第一个类） 。

```xml
<EmbeddedResource Include="X.resx" DependentUpon="MyTypes.cs">
```

在以下项目文件片段中定义的资源文件的清单名称是 Namespace.Classname.fr-FR.resources（其中 `Namespace.Classname` 是 MyTypes.cs 中定义的第一个类） 。

```xml
<EmbeddedResource Include="X.fr-FR.resx" DependentUpon="MyTypes.cs">
```

## <a name="embeddedresourceusedependentuponconvention-property"></a>EmbeddedResourceUseDependentUponConvention 属性

如果在项目文件中将 `EmbeddedResourceUseDependentUponConvention` 设置为 `false`，则每个资源清单文件名都基于项目的根命名空间以及从项目根目录到 .resx 文件的相对路径。 更具体地说，生成的资源清单文件名是 *RootNamespace.RelativePathWithDotsForSlashes.\[Culture.]resources*。 这也是用于在低于 3.0 的 .NET Core 版本中生成清单名称的逻辑。

> [!NOTE]
>
> - 如果未定义 `RootNamespace`，则默认为项目名称。
> - 如果为项目文件中的 `EmbeddedResource` 项指定了 `LogicalName`、`ManifestResourceName` 或 `DependentUpon` 元数据，则该命名规则不适用于该资源文件。

## <a name="see-also"></a>另请参阅

- [清单资源的命名方式](https://gist.github.com/BenVillalobos/041673b9a73bec60fdc3bf0f86fae62a)
- [.NET Core SDK 项目的 MSBuild 属性](../project-sdk/msbuild-props.md)
- [MSBuild 中断性变更](../compatibility/msbuild.md)
