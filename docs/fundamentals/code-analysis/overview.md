---
title: .NET 中的代码分析
titleSuffix: ''
description: 了解 .NET SDK 中的源代码分析。
ms.date: 12/04/2020
ms.topic: overview
ms.custom: updateeachrelease
helpviewer_keywords:
- code analysis
- code analyzers
ms.openlocfilehash: efc440adb59da1ef9838ec5445d9c55544c14380
ms.sourcegitcommit: 68c9d9d9a97aab3b59d388914004b5474cf1dbd7
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/30/2021
ms.locfileid: "99216468"
---
# <a name="overview-of-net-source-code-analysis"></a><span data-ttu-id="a1a8e-103">.NET 源代码分析概述</span><span class="sxs-lookup"><span data-stu-id="a1a8e-103">Overview of .NET source code analysis</span></span>

<span data-ttu-id="a1a8e-104">.NET Compiler Platform (Roslyn) 分析器会检查 C# 或 Visual Basic 代码的代码质量和代码样式问题。</span><span class="sxs-lookup"><span data-stu-id="a1a8e-104">.NET compiler platform (Roslyn) analyzers inspect your C# or Visual Basic code for code quality and code style issues.</span></span> <span data-ttu-id="a1a8e-105">从 .NET 5.0 开始，这些分析器包含在 .NET SDK 中，无需单独安装。</span><span class="sxs-lookup"><span data-stu-id="a1a8e-105">Starting in .NET 5.0, these analyzers are included with the .NET SDK and you don't need to install them separately.</span></span> <span data-ttu-id="a1a8e-106">如果项目面向 .NET 5 或更高版本，则默认情况下启用代码分析。</span><span class="sxs-lookup"><span data-stu-id="a1a8e-106">If your project targets .NET 5 or later, code analysis is enabled by default.</span></span> <span data-ttu-id="a1a8e-107">如果你的项目面向不同的 .NET 实现（例如，.NET Core、.NET Standard 或 .NET Framework），则必须通过将 [EnableNETAnalyzers](../../core/project-sdk/msbuild-props.md#enablenetanalyzers) 属性设置为来手动启用代码分析 `true` 。</span><span class="sxs-lookup"><span data-stu-id="a1a8e-107">If your project target a different .NET implementation, for example, .NET Core, .NET Standard, or .NET Framework, you must manually enable code analysis by setting the [EnableNETAnalyzers](../../core/project-sdk/msbuild-props.md#enablenetanalyzers) property to `true`.</span></span>

<span data-ttu-id="a1a8e-108">如果不想移到 .NET 5 + SDK，或者想要使用基于 NuGet 包的模型，也可以在 [CodeAnalysis. NetAnalyzers NuGet 包](https://www.nuget.org/packages/Microsoft.CodeAnalysis.NetAnalyzers)中使用该分析器。</span><span class="sxs-lookup"><span data-stu-id="a1a8e-108">If you don't want to move to the .NET 5+ SDK or if you prefer a NuGet package-based model, the analyzers are also available in the [Microsoft.CodeAnalysis.NetAnalyzers NuGet package](https://www.nuget.org/packages/Microsoft.CodeAnalysis.NetAnalyzers).</span></span> <span data-ttu-id="a1a8e-109">对于按需版本更新，你可能更倾向于使用基于包的模型。</span><span class="sxs-lookup"><span data-stu-id="a1a8e-109">You might prefer a package-based model for on-demand version updates.</span></span>

> [!NOTE]
> <span data-ttu-id="a1a8e-110">.NET 分析器是不可知的。</span><span class="sxs-lookup"><span data-stu-id="a1a8e-110">.NET analyzers are target-framework agnostic.</span></span> <span data-ttu-id="a1a8e-111">也就是说，你的项目不需要面向特定的 .NET 实现。</span><span class="sxs-lookup"><span data-stu-id="a1a8e-111">That is, your project does not need to target a specific .NET implementation.</span></span> <span data-ttu-id="a1a8e-112">分析器适用于目标为的项目以及 `net5.0` 更早的 .net 版本，如 `netcoreapp3.1` 和 `net472` 。</span><span class="sxs-lookup"><span data-stu-id="a1a8e-112">The analyzers work for projects that target `net5.0` as well as earlier .NET versions, such as `netcoreapp3.1` and `net472`.</span></span>

<span data-ttu-id="a1a8e-113">如果分析器发现规则冲突，则会将其报告为建议、警告或错误，具体情况视每个规则的 [配置](configuration-options.md)方式而定。</span><span class="sxs-lookup"><span data-stu-id="a1a8e-113">If rule violations are found by an analyzer, they're reported as a suggestion, warning, or error, depending on how each rule is [configured](configuration-options.md).</span></span> <span data-ttu-id="a1a8e-114">代码分析冲突以前缀 "CA" 或 "IDE" 显示，以便将它们与编译器错误区分开来。</span><span class="sxs-lookup"><span data-stu-id="a1a8e-114">Code analysis violations appear with the prefix "CA" or "IDE" to differentiate them from compiler errors.</span></span>

## <a name="code-quality-analysis"></a><span data-ttu-id="a1a8e-115">代码质量分析</span><span class="sxs-lookup"><span data-stu-id="a1a8e-115">Code quality analysis</span></span>

<span data-ttu-id="a1a8e-116">*代码质量分析* ( "CAxxxx" ) 规则检查 c # 或 Visual Basic 代码以获得安全性、性能、设计和其他问题。</span><span class="sxs-lookup"><span data-stu-id="a1a8e-116">*Code quality analysis* ("CAxxxx") rules inspect your C# or Visual Basic code for security, performance, design and other issues.</span></span> <span data-ttu-id="a1a8e-117">默认情况下，对于面向 .NET 5.0 或更高版本的项目，分析处于启用状态。</span><span class="sxs-lookup"><span data-stu-id="a1a8e-117">Analysis is enabled, by default, for projects that target .NET 5.0 or later.</span></span> <span data-ttu-id="a1a8e-118">通过将 [EnableNETAnalyzers](../../core/project-sdk/msbuild-props.md#enablenetanalyzers) 属性设置为，可以对面向早期 .net 版本的项目启用代码分析 `true` 。</span><span class="sxs-lookup"><span data-stu-id="a1a8e-118">You can enable code analysis on projects that target earlier .NET versions by setting the [EnableNETAnalyzers](../../core/project-sdk/msbuild-props.md#enablenetanalyzers) property to `true`.</span></span> <span data-ttu-id="a1a8e-119">你还可以通过将设置为来对你的项目禁用代码分析 `EnableNETAnalyzers` `false` 。</span><span class="sxs-lookup"><span data-stu-id="a1a8e-119">You can also disable code analysis for your project by setting `EnableNETAnalyzers` to `false`.</span></span>

> [!TIP]
> <span data-ttu-id="a1a8e-120">如果使用 Visual Studio：</span><span class="sxs-lookup"><span data-stu-id="a1a8e-120">If you're using Visual Studio:</span></span>
>
> - <span data-ttu-id="a1a8e-121">许多分析器规则都有关联的代码修复程序，您可以应用这些 *修补程序* 来纠正此问题。</span><span class="sxs-lookup"><span data-stu-id="a1a8e-121">Many analyzer rules have associated *code fixes* that you can apply to correct the problem.</span></span> <span data-ttu-id="a1a8e-122">代码修复显示在灯泡图标菜单中。</span><span class="sxs-lookup"><span data-stu-id="a1a8e-122">Code fixes are shown in the light bulb icon menu.</span></span>
> - <span data-ttu-id="a1a8e-123">可以通过在解决方案资源管理器中右键单击项目，然后选择 "**属性**  >  " "**代码分析**" 选项卡 >**启用 .net 分析器** 来启用或禁用代码分析。</span><span class="sxs-lookup"><span data-stu-id="a1a8e-123">You can enable or disable code analysis by right-clicking on a project in Solution Explorer and selecting **Properties** > **Code Analysis** tab > **Enable .NET analyzers**.</span></span>

### <a name="enabled-rules"></a><span data-ttu-id="a1a8e-124">启用规则</span><span class="sxs-lookup"><span data-stu-id="a1a8e-124">Enabled rules</span></span>

<span data-ttu-id="a1a8e-125">默认情况下，在 .NET 5.0 中启用以下规则。</span><span class="sxs-lookup"><span data-stu-id="a1a8e-125">The following rules are enabled, by default, in .NET 5.0.</span></span>

| <span data-ttu-id="a1a8e-126">诊断 ID</span><span class="sxs-lookup"><span data-stu-id="a1a8e-126">Diagnostic ID</span></span> | <span data-ttu-id="a1a8e-127">类别</span><span class="sxs-lookup"><span data-stu-id="a1a8e-127">Category</span></span> | <span data-ttu-id="a1a8e-128">严重性</span><span class="sxs-lookup"><span data-stu-id="a1a8e-128">Severity</span></span> | <span data-ttu-id="a1a8e-129">说明</span><span class="sxs-lookup"><span data-stu-id="a1a8e-129">Description</span></span> |
| - | - | - | - |
| [<span data-ttu-id="a1a8e-130">CA1416</span><span class="sxs-lookup"><span data-stu-id="a1a8e-130">CA1416</span></span>](/visualstudio/code-quality/ca1416) | <span data-ttu-id="a1a8e-131">互操作性</span><span class="sxs-lookup"><span data-stu-id="a1a8e-131">Interoperability</span></span> | <span data-ttu-id="a1a8e-132">警告</span><span class="sxs-lookup"><span data-stu-id="a1a8e-132">Warning</span></span> | <span data-ttu-id="a1a8e-133">平台兼容性分析器</span><span class="sxs-lookup"><span data-stu-id="a1a8e-133">Platform compatibility analyzer</span></span> |
| [<span data-ttu-id="a1a8e-134">CA1417</span><span class="sxs-lookup"><span data-stu-id="a1a8e-134">CA1417</span></span>](/visualstudio/code-quality/ca1417) | <span data-ttu-id="a1a8e-135">互操作性</span><span class="sxs-lookup"><span data-stu-id="a1a8e-135">Interoperability</span></span> | <span data-ttu-id="a1a8e-136">警告</span><span class="sxs-lookup"><span data-stu-id="a1a8e-136">Warning</span></span> | <span data-ttu-id="a1a8e-137">不要 `OutAttribute` 在 P/invoke 的字符串参数上使用</span><span class="sxs-lookup"><span data-stu-id="a1a8e-137">Do not use `OutAttribute` on string parameters for P/Invokes</span></span> |
| [<span data-ttu-id="a1a8e-138">CA1831</span><span class="sxs-lookup"><span data-stu-id="a1a8e-138">CA1831</span></span>](/visualstudio/code-quality/ca1831) | <span data-ttu-id="a1a8e-139">性能</span><span class="sxs-lookup"><span data-stu-id="a1a8e-139">Performance</span></span> | <span data-ttu-id="a1a8e-140">警告</span><span class="sxs-lookup"><span data-stu-id="a1a8e-140">Warning</span></span> | <span data-ttu-id="a1a8e-141">`AsSpan`适当时使用字符串而不是基于范围的索引器</span><span class="sxs-lookup"><span data-stu-id="a1a8e-141">Use `AsSpan` instead of range-based indexers for string when appropriate</span></span> |
| [<span data-ttu-id="a1a8e-142">CA2013</span><span class="sxs-lookup"><span data-stu-id="a1a8e-142">CA2013</span></span>](/visualstudio/code-quality/ca2013) | <span data-ttu-id="a1a8e-143">可靠性</span><span class="sxs-lookup"><span data-stu-id="a1a8e-143">Reliability</span></span> | <span data-ttu-id="a1a8e-144">警告</span><span class="sxs-lookup"><span data-stu-id="a1a8e-144">Warning</span></span> | <span data-ttu-id="a1a8e-145">不要将 `ReferenceEquals` 与值类型一起使用</span><span class="sxs-lookup"><span data-stu-id="a1a8e-145">Do not use `ReferenceEquals` with value types</span></span> |
| [<span data-ttu-id="a1a8e-146">CA2014</span><span class="sxs-lookup"><span data-stu-id="a1a8e-146">CA2014</span></span>](/visualstudio/code-quality/ca2014) | <span data-ttu-id="a1a8e-147">可靠性</span><span class="sxs-lookup"><span data-stu-id="a1a8e-147">Reliability</span></span> | <span data-ttu-id="a1a8e-148">警告</span><span class="sxs-lookup"><span data-stu-id="a1a8e-148">Warning</span></span> | <span data-ttu-id="a1a8e-149">不要 `stackalloc` 在循环中使用</span><span class="sxs-lookup"><span data-stu-id="a1a8e-149">Do not use `stackalloc` in loops</span></span> |
| [<span data-ttu-id="a1a8e-150">CA2015</span><span class="sxs-lookup"><span data-stu-id="a1a8e-150">CA2015</span></span>](/visualstudio/code-quality/ca2015) | <span data-ttu-id="a1a8e-151">可靠性</span><span class="sxs-lookup"><span data-stu-id="a1a8e-151">Reliability</span></span> | <span data-ttu-id="a1a8e-152">警告</span><span class="sxs-lookup"><span data-stu-id="a1a8e-152">Warning</span></span> | <span data-ttu-id="a1a8e-153">不要定义派生自的类型的终结器 <xref:System.Buffers.MemoryManager%601></span><span class="sxs-lookup"><span data-stu-id="a1a8e-153">Do not define finalizers for types derived from <xref:System.Buffers.MemoryManager%601></span></span> |
| [<span data-ttu-id="a1a8e-154">CA2200</span><span class="sxs-lookup"><span data-stu-id="a1a8e-154">CA2200</span></span>](/visualstudio/code-quality/ca2200) | <span data-ttu-id="a1a8e-155">使用情况</span><span class="sxs-lookup"><span data-stu-id="a1a8e-155">Usage</span></span> | <span data-ttu-id="a1a8e-156">警告</span><span class="sxs-lookup"><span data-stu-id="a1a8e-156">Warning</span></span> | <span data-ttu-id="a1a8e-157">再次引发以保留堆栈详细信息</span><span class="sxs-lookup"><span data-stu-id="a1a8e-157">Rethrow to preserve stack details</span></span>
| [<span data-ttu-id="a1a8e-158">CA2247</span><span class="sxs-lookup"><span data-stu-id="a1a8e-158">CA2247</span></span>](/visualstudio/code-quality/ca2247) | <span data-ttu-id="a1a8e-159">使用情况</span><span class="sxs-lookup"><span data-stu-id="a1a8e-159">Usage</span></span> | <span data-ttu-id="a1a8e-160">警告</span><span class="sxs-lookup"><span data-stu-id="a1a8e-160">Warning</span></span> | <span data-ttu-id="a1a8e-161">传递给 TaskCompletionSource 构造函数的参数应为 <xref:System.Threading.Tasks.TaskCreationOptions> 枚举，而不是 <xref:System.Threading.Tasks.TaskContinuationOptions></span><span class="sxs-lookup"><span data-stu-id="a1a8e-161">Argument passed to TaskCompletionSource constructor should be <xref:System.Threading.Tasks.TaskCreationOptions> enum instead of <xref:System.Threading.Tasks.TaskContinuationOptions></span></span> |

<span data-ttu-id="a1a8e-162">你可以更改这些规则的严重性，以禁用这些规则或将它们提升为错误。</span><span class="sxs-lookup"><span data-stu-id="a1a8e-162">You can change the severity of these rules to disable them or elevate them to errors.</span></span> <span data-ttu-id="a1a8e-163">还可以 [启用更多规则](#enable-additional-rules)。</span><span class="sxs-lookup"><span data-stu-id="a1a8e-163">You can also [enable more rules](#enable-additional-rules).</span></span>

- <span data-ttu-id="a1a8e-164">有关每个 .NET SDK 版本附带的规则的列表，请参阅 [分析器版本](https://github.com/dotnet/roslyn-analyzers/blob/master/src/NetAnalyzers/Core/AnalyzerReleases.Shipped.md)。</span><span class="sxs-lookup"><span data-stu-id="a1a8e-164">For a list of rules that are included with each .NET SDK version, see [Analyzer releases](https://github.com/dotnet/roslyn-analyzers/blob/master/src/NetAnalyzers/Core/AnalyzerReleases.Shipped.md).</span></span>
- <span data-ttu-id="a1a8e-165">有关所有代码质量规则的列表，请参阅 [代码质量规则](quality-rules/index.md)。</span><span class="sxs-lookup"><span data-stu-id="a1a8e-165">For a list of all the code quality rules, see [Code quality rules](quality-rules/index.md).</span></span>

### <a name="enable-additional-rules"></a><span data-ttu-id="a1a8e-166">启用其他规则</span><span class="sxs-lookup"><span data-stu-id="a1a8e-166">Enable additional rules</span></span>

<span data-ttu-id="a1a8e-167">*分析模式* 是指预定义的代码分析配置，其中未启用任何、部分或全部规则。</span><span class="sxs-lookup"><span data-stu-id="a1a8e-167">*Analysis mode* refers to a predefined code analysis configuration where none, some, or all rules are enabled.</span></span> <span data-ttu-id="a1a8e-168">在默认分析模式下，仅将少量规则 [作为生成警告启用](#enabled-rules)。</span><span class="sxs-lookup"><span data-stu-id="a1a8e-168">In the default analysis mode, only a small number of rules are [enabled as build warnings](#enabled-rules).</span></span> <span data-ttu-id="a1a8e-169">可以通过在项目文件中设置 [AnalysisMode](../../core/project-sdk/msbuild-props.md#analysismode) 属性来更改项目的分析模式。</span><span class="sxs-lookup"><span data-stu-id="a1a8e-169">You can change the analysis mode for your project by setting the [AnalysisMode](../../core/project-sdk/msbuild-props.md#analysismode) property in the project file.</span></span> <span data-ttu-id="a1a8e-170">允许的值为：</span><span class="sxs-lookup"><span data-stu-id="a1a8e-170">The allowable values are:</span></span>

| <span data-ttu-id="a1a8e-171">值</span><span class="sxs-lookup"><span data-stu-id="a1a8e-171">Value</span></span> | <span data-ttu-id="a1a8e-172">说明</span><span class="sxs-lookup"><span data-stu-id="a1a8e-172">Description</span></span> |
| - | - |
| `AllDisabledByDefault` | <span data-ttu-id="a1a8e-173">这是最保守的模式。</span><span class="sxs-lookup"><span data-stu-id="a1a8e-173">This is the most conservative mode.</span></span> <span data-ttu-id="a1a8e-174">默认情况下，所有规则都处于禁用状态。</span><span class="sxs-lookup"><span data-stu-id="a1a8e-174">All rules are disabled by default.</span></span> <span data-ttu-id="a1a8e-175">可以选择[选择加入](configuration-options.md)各条规则，以启用它们。</span><span class="sxs-lookup"><span data-stu-id="a1a8e-175">You can selectively [opt into](configuration-options.md) individual rules to enable them.</span></span><br /><br />`<AnalysisMode>AllDisabledByDefault</AnalysisMode>` |
| `AllEnabledByDefault` | <span data-ttu-id="a1a8e-176">这是最严格的模式。</span><span class="sxs-lookup"><span data-stu-id="a1a8e-176">This is the most aggressive mode.</span></span> <span data-ttu-id="a1a8e-177">所有规则都作为生成警告启用。</span><span class="sxs-lookup"><span data-stu-id="a1a8e-177">All rules are enabled as build warnings.</span></span> <span data-ttu-id="a1a8e-178">您可以选择性地 [选择退出](configuration-options.md) 个别规则来禁用它们。</span><span class="sxs-lookup"><span data-stu-id="a1a8e-178">You can selectively [opt out of](configuration-options.md) individual rules to disable them.</span></span><br /><br />`<AnalysisMode>AllEnabledByDefault</AnalysisMode>` |
| `Default` | <span data-ttu-id="a1a8e-179">默认模式，其中有少量的规则作为警告启用，而其他规则仅作为 Visual Studio IDE 建议和相应的代码修复，而其余部分被完全禁用。</span><span class="sxs-lookup"><span data-stu-id="a1a8e-179">The default mode, where a handful of rules are enabled as warnings, others are enabled only as Visual Studio IDE suggestions with corresponding code fixes, and the rest are disabled completely.</span></span> <span data-ttu-id="a1a8e-180">你可以选择性地 [选择加入或退出](configuration-options.md) 单个规则来禁用它们。</span><span class="sxs-lookup"><span data-stu-id="a1a8e-180">You can selectively [opt into or out of](configuration-options.md) individual rules to disable them.</span></span><br /><br />`<AnalysisMode>Default</AnalysisMode>` |

<span data-ttu-id="a1a8e-181">若要查找每个可用规则的默认严重性以及是否在默认分析模式下启用规则，请参阅 [规则的完整列表](https://github.com/dotnet/roslyn-analyzers/blob/master/src/NetAnalyzers/Core/AnalyzerReleases.Shipped.md)。</span><span class="sxs-lookup"><span data-stu-id="a1a8e-181">To find the default severity for each available rule and whether or not the rule is enabled in the default analysis mode, see the [full list of rules](https://github.com/dotnet/roslyn-analyzers/blob/master/src/NetAnalyzers/Core/AnalyzerReleases.Shipped.md).</span></span>

### <a name="treat-warnings-as-errors"></a><span data-ttu-id="a1a8e-182">视警告为错误</span><span class="sxs-lookup"><span data-stu-id="a1a8e-182">Treat warnings as errors</span></span>

<span data-ttu-id="a1a8e-183">如果在 `-warnaserror` 生成项目时使用标志，则所有代码分析警告也被视为错误。</span><span class="sxs-lookup"><span data-stu-id="a1a8e-183">If you use the `-warnaserror` flag when you build your projects, all code analysis warnings are also treated as errors.</span></span> <span data-ttu-id="a1a8e-184">如果你不希望将代码质量警告 (CAxxxx) 在存在时被视为错误 `-warnaserror` ，可以 `CodeAnalysisTreatWarningsAsErrors` `false` 在项目文件中将 MSBuild 属性设置为。</span><span class="sxs-lookup"><span data-stu-id="a1a8e-184">If you do not want code quality warnings (CAxxxx) to be treated as errors in presence of `-warnaserror`, you can set the `CodeAnalysisTreatWarningsAsErrors` MSBuild property to `false` in your project file.</span></span>

```xml
<PropertyGroup>
  <CodeAnalysisTreatWarningsAsErrors>false</CodeAnalysisTreatWarningsAsErrors>
</PropertyGroup>
```

<span data-ttu-id="a1a8e-185">你仍会看到任何代码分析警告，但不会中断你的生成。</span><span class="sxs-lookup"><span data-stu-id="a1a8e-185">You'll still see any code analysis warnings, but they won't break your build.</span></span>

### <a name="latest-updates"></a><span data-ttu-id="a1a8e-186">最新更新</span><span class="sxs-lookup"><span data-stu-id="a1a8e-186">Latest updates</span></span>

<span data-ttu-id="a1a8e-187">默认情况下，升级到较新版本的 .NET SDK 时，你将获得最新的代码分析规则和默认规则严重性。</span><span class="sxs-lookup"><span data-stu-id="a1a8e-187">By default, you'll get the latest code analysis rules and default rule severities as you upgrade to newer versions of the .NET SDK.</span></span> <span data-ttu-id="a1a8e-188">如果不想要此行为，例如，如果想要确保没有启用或禁用任何新规则，可以通过以下方式之一来替代它：</span><span class="sxs-lookup"><span data-stu-id="a1a8e-188">If you don't want this behavior, for example, if you want to ensure that no new rules are enabled or disabled, you can override it in one of the following ways:</span></span>

- <span data-ttu-id="a1a8e-189">将 `AnalysisLevel` MSBuild 属性设置为一个特定值，以将警告锁定到该设置。</span><span class="sxs-lookup"><span data-stu-id="a1a8e-189">Set the `AnalysisLevel` MSBuild property to a specific value to lock the warnings to that set.</span></span> <span data-ttu-id="a1a8e-190">升级到较新的 SDK 时，仍然会获得这些警告的 bug 修复，但不会启用新的警告，并且不会禁用现有的警告。</span><span class="sxs-lookup"><span data-stu-id="a1a8e-190">When you upgrade to a newer SDK, you'll still get bug fixes for those warnings, but no new warnings will be enabled and no existing warnings will be disabled.</span></span> <span data-ttu-id="a1a8e-191">例如，若要将规则集锁定为版本5.0 的 .NET SDK 随附的规则集，请将以下条目添加到项目文件。</span><span class="sxs-lookup"><span data-stu-id="a1a8e-191">For example, to lock the set of rules to those that ship with version 5.0 of the .NET SDK, add the following entry to your project file.</span></span>

  ```xml
  <PropertyGroup>
    <AnalysisLevel>5.0</AnalysisLevel>
  </PropertyGroup>
  ```

  > [!TIP]
  > <span data-ttu-id="a1a8e-192">属性的默认值 `AnalysisLevel` 为 `latest` ，这意味着，当你移动到较新版本的 .net SDK 时，始终会获得最新的代码分析规则。</span><span class="sxs-lookup"><span data-stu-id="a1a8e-192">The default value for the `AnalysisLevel` property is `latest`, which means you always get the latest code analysis rules as you move to newer versions of the .NET SDK.</span></span>

  <span data-ttu-id="a1a8e-193">有关详细信息，以及要查看可能值的列表，请参阅 [AnalysisLevel](../../core/project-sdk/msbuild-props.md#analysislevel)。</span><span class="sxs-lookup"><span data-stu-id="a1a8e-193">For more information, and to see a list of possible values, see [AnalysisLevel](../../core/project-sdk/msbuild-props.md#analysislevel).</span></span>

- <span data-ttu-id="a1a8e-194">安装 [CodeAnalysis NetAnalyzers NuGet 包](https://github.com/dotnet/roslyn-analyzers#microsoftcodeanalysisnetanalyzers) 以将规则更新与 .net SDK 更新分离。</span><span class="sxs-lookup"><span data-stu-id="a1a8e-194">Install the [Microsoft.CodeAnalysis.NetAnalyzers NuGet package](https://github.com/dotnet/roslyn-analyzers#microsoftcodeanalysisnetanalyzers) to decouple rule updates from .NET SDK updates.</span></span> <span data-ttu-id="a1a8e-195">如果 SDK 包含的分析器程序集版本比 NuGet 包的版本新，则安装包将关闭内置 SDK 分析器并生成生成警告。</span><span class="sxs-lookup"><span data-stu-id="a1a8e-195">Installing the package turns off the built-in SDK analyzers and generates a build warning if the SDK contains a newer analyzer assembly version than that of the NuGet package.</span></span>

## <a name="code-style-analysis"></a><span data-ttu-id="a1a8e-196">代码样式分析</span><span class="sxs-lookup"><span data-stu-id="a1a8e-196">Code-style analysis</span></span>

<span data-ttu-id="a1a8e-197">*代码样式分析* ( "IDExxxx" ) 规则使你可以在基本代码中定义和维护一致的代码样式。</span><span class="sxs-lookup"><span data-stu-id="a1a8e-197">*Code-style analysis* ("IDExxxx") rules enable you to define and maintain consistent code style in your codebase.</span></span> <span data-ttu-id="a1a8e-198">默认启用设置为：</span><span class="sxs-lookup"><span data-stu-id="a1a8e-198">The default enablement settings are:</span></span>

- <span data-ttu-id="a1a8e-199">命令行生成：默认情况下，对命令行生成上的所有 .NET 项目禁用代码样式分析。</span><span class="sxs-lookup"><span data-stu-id="a1a8e-199">Command-line build: Code-style analysis is disabled, by default, for all .NET projects on command-line builds.</span></span>

  <span data-ttu-id="a1a8e-200">从 .NET 5.0 开始，可以在命令行和 Visual Studio 内部 [启用生成代码样式分析](#enable-on-build)。</span><span class="sxs-lookup"><span data-stu-id="a1a8e-200">Starting in .NET 5.0, you can [enable code-style analysis on build](#enable-on-build), both at the command line and inside Visual Studio.</span></span> <span data-ttu-id="a1a8e-201">代码样式冲突显示为带有 "IDE" 前缀的警告或错误。</span><span class="sxs-lookup"><span data-stu-id="a1a8e-201">Code style violations appear as warnings or errors with an "IDE" prefix.</span></span> <span data-ttu-id="a1a8e-202">这使您能够在生成时强制执行一致的代码样式。</span><span class="sxs-lookup"><span data-stu-id="a1a8e-202">This enables you to enforce consistent code styles at build time.</span></span>

- <span data-ttu-id="a1a8e-203">Visual studio：默认情况下，对于 Visual Studio 中的所有 .NET 项目，代码样式分析均为 [代码重构快速操作](/visualstudio/ide/code-generation-in-visual-studio)启用。</span><span class="sxs-lookup"><span data-stu-id="a1a8e-203">Visual Studio: Code-style analysis is enabled, by default, for all .NET projects inside Visual Studio as [code refactoring quick actions](/visualstudio/ide/code-generation-in-visual-studio).</span></span>

<span data-ttu-id="a1a8e-204">有关代码样式分析规则的完整列表，请参阅 [代码样式规则](style-rules/index.md)。</span><span class="sxs-lookup"><span data-stu-id="a1a8e-204">For a full list of code-style analysis rules, see [Code style rules](style-rules/index.md).</span></span>

### <a name="enable-on-build"></a><span data-ttu-id="a1a8e-205">启用生成时启用</span><span class="sxs-lookup"><span data-stu-id="a1a8e-205">Enable on build</span></span>

<span data-ttu-id="a1a8e-206">使用 .NET 5.0 SDK 和更高版本，可以在从命令行和 Visual Studio 生成时启用代码样式分析。</span><span class="sxs-lookup"><span data-stu-id="a1a8e-206">With the .NET 5.0 SDK and later versions, you can enable code-style analysis when building from the command-line and in Visual Studio.</span></span> <span data-ttu-id="a1a8e-207"> (然而，出于性能方面的原因，一些 [代码样式规则](https://github.com/dotnet/roslyn/blob/9f87b444da9c48a4d492b19f8337339056bf2b95/src/Analyzers/Core/Analyzers/EnforceOnBuildValues.cs#L95) 仍将仅适用于 VISUAL Studio IDE。 ) </span><span class="sxs-lookup"><span data-stu-id="a1a8e-207">(However, for performance reasons, [a handful of code-style rules](https://github.com/dotnet/roslyn/blob/9f87b444da9c48a4d492b19f8337339056bf2b95/src/Analyzers/Core/Analyzers/EnforceOnBuildValues.cs#L95) will still apply only in the Visual Studio IDE.)</span></span>

<span data-ttu-id="a1a8e-208">执行以下步骤可在生成时启用代码样式分析：</span><span class="sxs-lookup"><span data-stu-id="a1a8e-208">Follow these steps to enable code-style analysis on build:</span></span>

1. <span data-ttu-id="a1a8e-209">将 MSBuild 属性 [EnforceCodeStyleInBuild](../../core/project-sdk/msbuild-props.md#enforcecodestyleinbuild) 设置为 `true` 。</span><span class="sxs-lookup"><span data-stu-id="a1a8e-209">Set the MSBuild property [EnforceCodeStyleInBuild](../../core/project-sdk/msbuild-props.md#enforcecodestyleinbuild) to `true`.</span></span>

1. <span data-ttu-id="a1a8e-210">在 *editorconfig* 文件中， [配置](configuration-options.md) 希望在生成时运行的每个 "IDE" 代码样式规则（警告或错误）。</span><span class="sxs-lookup"><span data-stu-id="a1a8e-210">In an *.editorconfig* file, [configure](configuration-options.md) each "IDE" code style rule that you wish to run on build as a warning or an error.</span></span> <span data-ttu-id="a1a8e-211">例如：</span><span class="sxs-lookup"><span data-stu-id="a1a8e-211">For example:</span></span>

   ```ini
   [*.{cs,vb}]
   # IDE0040: Accessibility modifiers required (escalated to a build warning)
   dotnet_diagnostic.IDE0040.severity = warning
   ```

   <span data-ttu-id="a1a8e-212">或者，你可以将整个类别配置为警告或错误，默认情况下，你可以在不希望在生成时运行的那一类别中选择关闭规则。</span><span class="sxs-lookup"><span data-stu-id="a1a8e-212">Alternatively, you can configure an entire category to be a warning or error, by default, and then selectively turn off rules in that category that you don't want to run on build.</span></span> <span data-ttu-id="a1a8e-213">例如：</span><span class="sxs-lookup"><span data-stu-id="a1a8e-213">For example:</span></span>

   ```ini
   [*.{cs,vb}]

   # Default severity for analyzer diagnostics with category 'Style' (escalated to build warnings)
   dotnet_analyzer_diagnostic.category-Style.severity = warning

   # IDE0040: Accessibility modifiers required (disabled on build)
   dotnet_diagnostic.IDE0040.severity = silent
   ```

> [!NOTE]
> <span data-ttu-id="a1a8e-214">代码样式分析功能是实验性的，可能会在 .NET 5 和 .NET 6 版本之间发生更改。</span><span class="sxs-lookup"><span data-stu-id="a1a8e-214">The code-style analysis feature is experimental and may change between the .NET 5 and .NET 6 releases.</span></span>

## <a name="suppress-a-warning"></a><span data-ttu-id="a1a8e-215">禁止显示警告</span><span class="sxs-lookup"><span data-stu-id="a1a8e-215">Suppress a warning</span></span>

<span data-ttu-id="a1a8e-216">若要取消规则冲突，请 `none` 在 EditorConfig 文件中将该规则 ID 的严重性选项设置为。</span><span class="sxs-lookup"><span data-stu-id="a1a8e-216">To suppress a rule violation, set the severity option for that rule ID to `none` in an EditorConfig file.</span></span> <span data-ttu-id="a1a8e-217">例如：</span><span class="sxs-lookup"><span data-stu-id="a1a8e-217">For example:</span></span>

```ini
dotnet_diagnostic.CA1822.severity = none
```

<span data-ttu-id="a1a8e-218">Visual Studio 提供了其他方式来禁止显示代码分析规则中的警告。</span><span class="sxs-lookup"><span data-stu-id="a1a8e-218">Visual Studio provides additional ways to suppress warnings from code analysis rules.</span></span> <span data-ttu-id="a1a8e-219">有关详细信息，请参阅 [取消冲突](/visualstudio/code-quality/use-roslyn-analyzers#suppress-violations)。</span><span class="sxs-lookup"><span data-stu-id="a1a8e-219">For more information, see [Suppress violations](/visualstudio/code-quality/use-roslyn-analyzers#suppress-violations).</span></span>

<span data-ttu-id="a1a8e-220">有关规则严重性的详细信息，请参阅 [配置规则严重性](configuration-options.md#severity-level)。</span><span class="sxs-lookup"><span data-stu-id="a1a8e-220">For more information about rule severities, see [Configure rule severity](configuration-options.md#severity-level).</span></span>

## <a name="third-party-analyzers"></a><span data-ttu-id="a1a8e-221">第三方分析器</span><span class="sxs-lookup"><span data-stu-id="a1a8e-221">Third-party analyzers</span></span>

<span data-ttu-id="a1a8e-222">除了官方 .NET 分析器外，还可以安装第三方分析器，如 [StyleCop](https://www.nuget.org/packages/StyleCop.Analyzers/)、 [Roslynator](https://www.nuget.org/packages/Roslynator.Analyzers/)、 [XUnit 分析器](https://www.nuget.org/packages/xunit.analyzers/)和 [sonar.projectname Analyzer](https://www.nuget.org/packages/SonarAnalyzer.CSharp/)。</span><span class="sxs-lookup"><span data-stu-id="a1a8e-222">In addition to the official .NET analyzers, you can also install third party analyzers, such as [StyleCop](https://www.nuget.org/packages/StyleCop.Analyzers/), [Roslynator](https://www.nuget.org/packages/Roslynator.Analyzers/), [XUnit Analyzers](https://www.nuget.org/packages/xunit.analyzers/), and [Sonar Analyzer](https://www.nuget.org/packages/SonarAnalyzer.CSharp/).</span></span>

## <a name="see-also"></a><span data-ttu-id="a1a8e-223">请参阅</span><span class="sxs-lookup"><span data-stu-id="a1a8e-223">See also</span></span>

- [<span data-ttu-id="a1a8e-224">代码质量分析规则参考</span><span class="sxs-lookup"><span data-stu-id="a1a8e-224">Code quality analysis rule reference</span></span>](quality-rules/index.md)
- [<span data-ttu-id="a1a8e-225">代码样式分析规则引用</span><span class="sxs-lookup"><span data-stu-id="a1a8e-225">Code style analysis rule reference</span></span>](style-rules/index.md)
- [<span data-ttu-id="a1a8e-226">Visual Studio 中的代码分析</span><span class="sxs-lookup"><span data-stu-id="a1a8e-226">Code analysis in Visual Studio</span></span>](/visualstudio/code-quality/roslyn-analyzers-overview)
- [<span data-ttu-id="a1a8e-227">.NET 编译器平台 SDK</span><span class="sxs-lookup"><span data-stu-id="a1a8e-227">.NET Compiler Platform SDK</span></span>](../../csharp/roslyn-sdk/index.md)
- [<span data-ttu-id="a1a8e-228">教程：编写第一个分析器和代码修补程序</span><span class="sxs-lookup"><span data-stu-id="a1a8e-228">Tutorial: Write your first analyzer and code fix</span></span>](../../csharp/roslyn-sdk/tutorials/how-to-write-csharp-analyzer-code-fix.md)
