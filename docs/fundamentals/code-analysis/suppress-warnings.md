---
title: 禁止显示代码分析警告
description: 了解可以禁止显示 .NET 代码分析冲突的不同方式。
ms.date: 01/28/2021
dev_langs:
- CSharp
- VB
helpviewer_keywords:
- code analysis, suppress warnings
- suppress code analysis warnings
ms.openlocfilehash: b08e93089975a59fabfeb0daaf6a2a6454b2c7e8
ms.sourcegitcommit: 68c9d9d9a97aab3b59d388914004b5474cf1dbd7
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/30/2021
ms.locfileid: "99217260"
---
# <a name="how-to-suppress-code-analysis-warnings"></a><span data-ttu-id="71317-103">如何取消显示代码分析警告</span><span class="sxs-lookup"><span data-stu-id="71317-103">How to suppress code analysis warnings</span></span>

<span data-ttu-id="71317-104">本文介绍了在生成 .NET 应用程序时可以禁止显示代码分析警告的各种方式。</span><span class="sxs-lookup"><span data-stu-id="71317-104">This article covers the various ways you can suppress warnings from code analysis when you build your .NET app.</span></span>

> [!TIP]
> <span data-ttu-id="71317-105">如果使用 Visual Studio 作为开发环境，则 *灯泡* 菜单将提供一些选项，用于生成代码以取消警告。</span><span class="sxs-lookup"><span data-stu-id="71317-105">If you're using Visual Studio as your development environment, the *light bulb* menu provides options that generate the code to suppress warnings for you.</span></span> <span data-ttu-id="71317-106">有关详细信息，请参阅 [取消冲突](/visualstudio/code-quality/use-roslyn-analyzers?#suppress-violations)。</span><span class="sxs-lookup"><span data-stu-id="71317-106">For more information, see [Suppress violations](/visualstudio/code-quality/use-roslyn-analyzers?#suppress-violations).</span></span>

## <a name="disable-the-rule"></a><span data-ttu-id="71317-107">禁用规则</span><span class="sxs-lookup"><span data-stu-id="71317-107">Disable the rule</span></span>

<span data-ttu-id="71317-108">禁用导致此警告的代码分析规则后，将根据你) 使用的 [配置文件](configuration-files.md) 的范围，禁用整个文件或项目 (的规则。</span><span class="sxs-lookup"><span data-stu-id="71317-108">By disabling the code analysis rule that's causing the warning, you disable the rule for your entire file or project (depending on the scope of the [configuration file](configuration-files.md) that you use).</span></span> <span data-ttu-id="71317-109">若要禁用规则，请 `none` 在配置文件中将其严重性设置为。</span><span class="sxs-lookup"><span data-stu-id="71317-109">To disable the rule, set its severity to `none` in the configuration file.</span></span>

```ini
[*.{cs,vb}]
dotnet_diagnostic.<rule-ID>.severity = none
```

<span data-ttu-id="71317-110">有关规则严重性的详细信息，请参阅 [配置规则严重性](~/docs/fundamentals/code-analysis/configuration-options.md#severity-level)。</span><span class="sxs-lookup"><span data-stu-id="71317-110">For more information about rule severities, see [Configure rule severity](~/docs/fundamentals/code-analysis/configuration-options.md#severity-level).</span></span>

## <a name="use-a-preprocessor-directive"></a><span data-ttu-id="71317-111">使用预处理器指令</span><span class="sxs-lookup"><span data-stu-id="71317-111">Use a preprocessor directive</span></span>

<span data-ttu-id="71317-112">使用 [#pragma warning (c # ) ](../../csharp/language-reference/preprocessor-directives/preprocessor-pragma-warning.md) 或 [禁用 (Visual Basic) ](../../visual-basic/language-reference/directives/disable-enable.md) 指令来仅禁止显示特定代码行的警告。</span><span class="sxs-lookup"><span data-stu-id="71317-112">Use a [#pragma warning (C#)](../../csharp/language-reference/preprocessor-directives/preprocessor-pragma-warning.md) or [Disable (Visual Basic)](../../visual-basic/language-reference/directives/disable-enable.md) directive to suppress the warning for only a specific line of code.</span></span>

```csharp
    try { ... }
    catch (Exception e)
    {
#pragma warning disable CA2200 // Rethrow to preserve stack details
        throw e;
#pragma warning restore CA2200 // Rethrow to preserve stack details
    }
```

```vb
    Try
        ...
    Catch e As Exception
#Disable Warning CA2200 ' Rethrow to preserve stack details
        Throw e
#Enable Warning CA2200 ' Rethrow to preserve stack details
    End Try
```

## <a name="use-the-suppressmessageattribute"></a><span data-ttu-id="71317-113">使用 SuppressMessageAttribute</span><span class="sxs-lookup"><span data-stu-id="71317-113">Use the SuppressMessageAttribute</span></span>

<span data-ttu-id="71317-114">可以使用在 <xref:System.Diagnostics.CodeAnalysis.SuppressMessageAttribute> 源文件或全局禁止显示文件中禁止显示 (*GlobalSuppressions.cs* 或 *GlobalSuppressions*) 的警告。</span><span class="sxs-lookup"><span data-stu-id="71317-114">You can use a <xref:System.Diagnostics.CodeAnalysis.SuppressMessageAttribute> to suppress a warning either in the source file or in a global suppressions file for the project (*GlobalSuppressions.cs* or *GlobalSuppressions.vb*).</span></span> <span data-ttu-id="71317-115">此属性提供了一种在项目或文件的特定部分禁止显示警告的方法。</span><span class="sxs-lookup"><span data-stu-id="71317-115">This attribute provides a way to suppress a warning in only certain parts of your project or file.</span></span>

<span data-ttu-id="71317-116">特性的两个必需的位置参数 <xref:System.Diagnostics.CodeAnalysis.SuppressMessageAttribute> 是规则和 *规则 ID* 的 *类别*。</span><span class="sxs-lookup"><span data-stu-id="71317-116">The two required, positional parameters for the <xref:System.Diagnostics.CodeAnalysis.SuppressMessageAttribute> attribute are the *category* of the rule and the *rule ID*.</span></span> <span data-ttu-id="71317-117">下面的代码段传递 `"Usage"` 和 `"CA2200:Rethrow to preserve stack details"` 这些参数。</span><span class="sxs-lookup"><span data-stu-id="71317-117">The following code snippet passes `"Usage"` and `"CA2200:Rethrow to preserve stack details"` for these parameters.</span></span>

```csharp
[System.Diagnostics.CodeAnalysis.SuppressMessage("Usage", "CA2200:Rethrow to preserve stack details", Justification = "Not production code.")]
private static void IngorableCharacters()
{
    try
    {
        ...
    }
    catch (Exception e)
    {
        throw e;
    }
}
```

<span data-ttu-id="71317-118">例如，如果将属性添加到全局禁止显示文件中，则会将抑制 [范围限定](xref:System.Diagnostics.CodeAnalysis.SuppressMessageAttribute.Scope) 为所需的级别 `"member"` 。</span><span class="sxs-lookup"><span data-stu-id="71317-118">If you add the attribute to the global suppressions file, you [scope](xref:System.Diagnostics.CodeAnalysis.SuppressMessageAttribute.Scope) the suppression to the desired level, for example `"member"`.</span></span> <span data-ttu-id="71317-119">指定 API，应使用属性禁止显示警告 <xref:System.Diagnostics.CodeAnalysis.SuppressMessageAttribute.Target> 。</span><span class="sxs-lookup"><span data-stu-id="71317-119">You specify the API where the warning should be suppressed using the <xref:System.Diagnostics.CodeAnalysis.SuppressMessageAttribute.Target> property.</span></span>

```csharp
[assembly: SuppressMessage("Usage", "CA2200:Rethrow to preserve stack details", Justification = "Not production code.", Scope = "member", Target = "~M:MyApp.Program.IngorableCharacters")]
```

<span data-ttu-id="71317-120">若要取消编译器生成的代码中未映射到显式提供的用户源的警告，必须将禁止显示特性放置在全局禁止显示文件中。</span><span class="sxs-lookup"><span data-stu-id="71317-120">To suppress warnings for compiler-generated code that doesn't map to explicitly provided user source, you must put the suppression attribute in a global suppressions file.</span></span> <span data-ttu-id="71317-121">例如，下面的代码针对编译器发出的构造函数禁止发生冲突：</span><span class="sxs-lookup"><span data-stu-id="71317-121">For example, the following code suppresses a violation against a compiler-emitted constructor:</span></span>

```csharp
[module: SuppressMessage("Microsoft.Design", "CA1055:AbstractTypesDoNotHavePublicConstructors", Scope="member", Target="MyTools.Type..ctor()")]
```

## <a name="see-also"></a><span data-ttu-id="71317-122">请参阅</span><span class="sxs-lookup"><span data-stu-id="71317-122">See also</span></span>

- [<span data-ttu-id="71317-123">禁止冲突 (Visual Studio) </span><span class="sxs-lookup"><span data-stu-id="71317-123">Suppress violations (Visual Studio)</span></span>](/visualstudio/code-quality/use-roslyn-analyzers?#suppress-violations)
