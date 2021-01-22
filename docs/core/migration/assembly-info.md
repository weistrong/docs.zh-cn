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
# <a name="map-assemblyinfo-attributes-to-properties"></a><span data-ttu-id="8d264-103">将 AssemblyInfo 特性映射到属性</span><span class="sxs-lookup"><span data-stu-id="8d264-103">Map AssemblyInfo attributes to properties</span></span>

<span data-ttu-id="8d264-104">从 .NET Core 2.1 开始，通常存在于 .NET Core 2.0 及更早版本的 AssemblyInfo 文件中的[程序集特性](../../standard/assembly/set-attributes.md)会从 MSBuild 属性中自动生成。</span><span class="sxs-lookup"><span data-stu-id="8d264-104">[Assembly attributes](../../standard/assembly/set-attributes.md) that were typically present in an *AssemblyInfo* file in .NET Core 2.0 and earlier versions are automatically generated from MSBuild properties, starting in .NET Core 2.1.</span></span>

## <a name="properties-per-attribute"></a><span data-ttu-id="8d264-105">PropertiesPerAttribute</span><span class="sxs-lookup"><span data-stu-id="8d264-105">Properties per attribute</span></span>

<span data-ttu-id="8d264-106">如下表所示，每个特性都有一个相应的可控制其内容的属性，还有一个可以禁用其生成的属性：</span><span class="sxs-lookup"><span data-stu-id="8d264-106">As shown in the following table, each attribute has a corresponding property that controls its content and another that disables its generation:</span></span>

| <span data-ttu-id="8d264-107">属性</span><span class="sxs-lookup"><span data-stu-id="8d264-107">Attribute</span></span>                                                      | <span data-ttu-id="8d264-108">Property</span><span class="sxs-lookup"><span data-stu-id="8d264-108">Property</span></span>               | <span data-ttu-id="8d264-109">要禁用的属性</span><span class="sxs-lookup"><span data-stu-id="8d264-109">Property to disable</span></span>                             |
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

<span data-ttu-id="8d264-110">注意：</span><span class="sxs-lookup"><span data-stu-id="8d264-110">Notes:</span></span>

- <span data-ttu-id="8d264-111">`AssemblyVersion` 和 `FileVersion` 默认采用 `$(Version)` 的值而不带后缀。</span><span class="sxs-lookup"><span data-stu-id="8d264-111">`AssemblyVersion` and `FileVersion` default to the value of `$(Version)` without the suffix.</span></span> <span data-ttu-id="8d264-112">例如，如果 `$(Version)` 为 `1.2.3-beta.4`，则值将为 `1.2.3`。</span><span class="sxs-lookup"><span data-stu-id="8d264-112">For example, if `$(Version)` is `1.2.3-beta.4`, then the value would be `1.2.3`.</span></span>
- <span data-ttu-id="8d264-113">`InformationalVersion` 默认是 `$(Version)` 的值。</span><span class="sxs-lookup"><span data-stu-id="8d264-113">`InformationalVersion` defaults to the value of `$(Version)`.</span></span>
- <span data-ttu-id="8d264-114">如果存在 `$(SourceRevisionId)` 属性，则该属性会附加到 `InformationalVersion`。</span><span class="sxs-lookup"><span data-stu-id="8d264-114">If the `$(SourceRevisionId)` property is present, it's appended to `InformationalVersion`.</span></span> <span data-ttu-id="8d264-115">可以使用 `IncludeSourceRevisionInInformationalVersion` 禁用此行为。</span><span class="sxs-lookup"><span data-stu-id="8d264-115">You can disable this behavior using `IncludeSourceRevisionInInformationalVersion`.</span></span>
- <span data-ttu-id="8d264-116">`Copyright` 和 `Description` 属性也可用于 NuGet 元数据。</span><span class="sxs-lookup"><span data-stu-id="8d264-116">`Copyright` and `Description` properties are also used for NuGet metadata.</span></span>
- <span data-ttu-id="8d264-117">`Configuration`（默认值为 `Debug`）由所有 MSBuild 目标共享。</span><span class="sxs-lookup"><span data-stu-id="8d264-117">`Configuration`, which defaults to `Debug`, is shared with all MSBuild targets.</span></span> <span data-ttu-id="8d264-118">可以通过 `dotnet` 命令的 `--configuration` 选项对其进行设置，例如 [dotnet pack](../tools/dotnet-pack.md)。</span><span class="sxs-lookup"><span data-stu-id="8d264-118">You can set it via the `--configuration` option of `dotnet` commands, for example, [dotnet pack](../tools/dotnet-pack.md).</span></span>

## <a name="generateassemblyinfo"></a><span data-ttu-id="8d264-119">GenerateAssemblyInfo</span><span class="sxs-lookup"><span data-stu-id="8d264-119">GenerateAssemblyInfo</span></span>

<span data-ttu-id="8d264-120">一个布尔值，用于启用或禁用 AssemblyInfo 生成。</span><span class="sxs-lookup"><span data-stu-id="8d264-120">A Boolean that enables or disables the AssemblyInfo generation.</span></span> <span data-ttu-id="8d264-121">默认值为 `true`。</span><span class="sxs-lookup"><span data-stu-id="8d264-121">The default value is `true`.</span></span>

## <a name="generatedassemblyinfofile"></a><span data-ttu-id="8d264-122">GeneratedAssemblyInfoFile</span><span class="sxs-lookup"><span data-stu-id="8d264-122">GeneratedAssemblyInfoFile</span></span>

<span data-ttu-id="8d264-123">生成的程序集信息文件的相对路径或绝对路径。</span><span class="sxs-lookup"><span data-stu-id="8d264-123">The relative or absolute path of the generated assembly info file.</span></span> <span data-ttu-id="8d264-124">默认为 `$(IntermediateOutputPath)` (obj) 目录中名为 [project-name].AssemblyInfo.[cs|vb] 的文件 。</span><span class="sxs-lookup"><span data-stu-id="8d264-124">Defaults to a file named *[project-name].AssemblyInfo.[cs|vb]* in the `$(IntermediateOutputPath)` (*obj*) directory.</span></span>
