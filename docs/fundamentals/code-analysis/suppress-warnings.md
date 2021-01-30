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
# <a name="how-to-suppress-code-analysis-warnings"></a>如何取消显示代码分析警告

本文介绍了在生成 .NET 应用程序时可以禁止显示代码分析警告的各种方式。

> [!TIP]
> 如果使用 Visual Studio 作为开发环境，则 *灯泡* 菜单将提供一些选项，用于生成代码以取消警告。 有关详细信息，请参阅 [取消冲突](/visualstudio/code-quality/use-roslyn-analyzers?#suppress-violations)。

## <a name="disable-the-rule"></a>禁用规则

禁用导致此警告的代码分析规则后，将根据你) 使用的 [配置文件](configuration-files.md) 的范围，禁用整个文件或项目 (的规则。 若要禁用规则，请 `none` 在配置文件中将其严重性设置为。

```ini
[*.{cs,vb}]
dotnet_diagnostic.<rule-ID>.severity = none
```

有关规则严重性的详细信息，请参阅 [配置规则严重性](~/docs/fundamentals/code-analysis/configuration-options.md#severity-level)。

## <a name="use-a-preprocessor-directive"></a>使用预处理器指令

使用 [#pragma warning (c # ) ](../../csharp/language-reference/preprocessor-directives/preprocessor-pragma-warning.md) 或 [禁用 (Visual Basic) ](../../visual-basic/language-reference/directives/disable-enable.md) 指令来仅禁止显示特定代码行的警告。

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

## <a name="use-the-suppressmessageattribute"></a>使用 SuppressMessageAttribute

可以使用在 <xref:System.Diagnostics.CodeAnalysis.SuppressMessageAttribute> 源文件或全局禁止显示文件中禁止显示 (*GlobalSuppressions.cs* 或 *GlobalSuppressions*) 的警告。 此属性提供了一种在项目或文件的特定部分禁止显示警告的方法。

特性的两个必需的位置参数 <xref:System.Diagnostics.CodeAnalysis.SuppressMessageAttribute> 是规则和 *规则 ID* 的 *类别*。 下面的代码段传递 `"Usage"` 和 `"CA2200:Rethrow to preserve stack details"` 这些参数。

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

例如，如果将属性添加到全局禁止显示文件中，则会将抑制 [范围限定](xref:System.Diagnostics.CodeAnalysis.SuppressMessageAttribute.Scope) 为所需的级别 `"member"` 。 指定 API，应使用属性禁止显示警告 <xref:System.Diagnostics.CodeAnalysis.SuppressMessageAttribute.Target> 。

```csharp
[assembly: SuppressMessage("Usage", "CA2200:Rethrow to preserve stack details", Justification = "Not production code.", Scope = "member", Target = "~M:MyApp.Program.IngorableCharacters")]
```

若要取消编译器生成的代码中未映射到显式提供的用户源的警告，必须将禁止显示特性放置在全局禁止显示文件中。 例如，下面的代码针对编译器发出的构造函数禁止发生冲突：

```csharp
[module: SuppressMessage("Microsoft.Design", "CA1055:AbstractTypesDoNotHavePublicConstructors", Scope="member", Target="MyTools.Type..ctor()")]
```

## <a name="see-also"></a>请参阅

- [禁止冲突 (Visual Studio) ](/visualstudio/code-quality/use-roslyn-analyzers?#suppress-violations)
