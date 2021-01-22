---
title: AssemblyInfoProperties
description: 了解程序集特性以及它们如何与 .NET Core 2.1 及更高版本中的 MSBuild 属性相对应。
ms.topic: reference
ms.date: 01/08/2021
ms.openlocfilehash: a2c431b3fe3da428f21582624ca5f357887e2815
ms.sourcegitcommit: a4cecb7389f02c27e412b743f9189bd2a6dea4d6
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/14/2021
ms.locfileid: "98192871"
---
# <a name="map-assemblyinfo-attributes-to-properties"></a>将 AssemblyInfo 特性映射到属性

从 .NET Core 2.1 开始，通常存在于 .NET Core 2.0 及更早版本的 AssemblyInfo 文件中的[程序集特性](../../standard/assembly/set-attributes.md)会从 MSBuild 属性中自动生成。

## <a name="properties-per-attribute"></a>PropertiesPerAttribute

如下表所示，每个特性都有一个相应的可控制其内容的属性，还有一个可以禁用其生成的属性：

| 属性                                                      | Property               | 要禁用的属性                             |
|----------------------------------------------------------------|------------------------|-------------------------------------------------|
| <xref:System.Reflection.AssemblyCompanyAttribute>              | `Company`              | `GenerateAssemblyCompanyAttribute`              |
| <xref:System.Reflection.AssemblyConfigurationAttribute>        | `Configuration`        | `GenerateAssemblyConfigurationAttribute`        |
| <xref:System.Reflection.AssemblyCopyrightAttribute>            | `Copyright`            | `GenerateAssemblyCopyrightAttribute`            |
| <xref:System.Reflection.AssemblyDescriptionAttribute>          | `Description`          | `GenerateAssemblyDescriptionAttribute`          |
| <xref:System.Reflection.AssemblyFileVersionAttribute>          | `FileVersion`          | `GenerateAssemblyFileVersionAttribute`          |
| <xref:System.Reflection.AssemblyInformationalVersionAttribute> | `InformationalVersion` | `GenerateAssemblyInformationalVersionAttribute` |
| <xref:System.Reflection.AssemblyProductAttribute>              | `Product`              | `GenerateAssemblyProductAttribute`              |
| <xref:System.Reflection.AssemblyTitleAttribute>                | `AssemblyTitle`        | `GenerateAssemblyTitleAttribute`                |
| <xref:System.Reflection.AssemblyVersionAttribute>              | `AssemblyVersion`      | `GenerateAssemblyVersionAttribute`              |
| <xref:System.Resources.NeutralResourcesLanguageAttribute>      | `NeutralLanguage`      | `GenerateNeutralResourcesLanguageAttribute`     |

注意：

- `AssemblyVersion` 和 `FileVersion` 默认采用 `$(Version)` 的值而不带后缀。 例如，如果 `$(Version)` 为 `1.2.3-beta.4`，则值将为 `1.2.3`。
- `InformationalVersion` 默认是 `$(Version)` 的值。
- 如果存在 `$(SourceRevisionId)` 属性，则该属性会附加到 `InformationalVersion`。 可以使用 `IncludeSourceRevisionInInformationalVersion` 禁用此行为。
- `Copyright` 和 `Description` 属性也可用于 NuGet 元数据。
- `Configuration`（默认值为 `Debug`）由所有 MSBuild 目标共享。 可以通过 `dotnet` 命令的 `--configuration` 选项对其进行设置，例如 [dotnet pack](../tools/dotnet-pack.md)。

## <a name="generateassemblyinfo"></a>GenerateAssemblyInfo

一个布尔值，用于启用或禁用 AssemblyInfo 生成。 默认值为 `true`。

## <a name="generatedassemblyinfofile"></a>GeneratedAssemblyInfoFile

生成的程序集信息文件的相对路径或绝对路径。 默认为 `$(IntermediateOutputPath)` (obj) 目录中名为 [project-name].AssemblyInfo.[cs|vb] 的文件 。
