---
ms.openlocfilehash: b26e346f7076a57aef8ae7587ab1222b4100a323
ms.sourcegitcommit: 7e42488c2f8f63f6d499b5f8fb1dec5bac9ad254
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/28/2021
ms.locfileid: "98957931"
---
## <a name="suppress-a-warning"></a><span data-ttu-id="56272-101">禁止显示警告</span><span class="sxs-lookup"><span data-stu-id="56272-101">Suppress a warning</span></span>

<span data-ttu-id="56272-102">若要取消规则冲突，请 `none` 在 EditorConfig 文件中将特定规则 ID 的严重性选项设置为。</span><span class="sxs-lookup"><span data-stu-id="56272-102">To suppress a rule violation, set the severity option for the specific rule ID to `none` in an EditorConfig file.</span></span> <span data-ttu-id="56272-103">例如：</span><span class="sxs-lookup"><span data-stu-id="56272-103">For example:</span></span>

```ini
[*.{cs,vb}]
dotnet_diagnostic.CA1822.severity = none
```

<span data-ttu-id="56272-104">Visual Studio 提供了其他方式来禁止显示代码分析规则中的警告。</span><span class="sxs-lookup"><span data-stu-id="56272-104">Visual Studio provides additional ways to suppress warnings from code analysis rules.</span></span> <span data-ttu-id="56272-105">有关详细信息，请参阅 [取消冲突](/visualstudio/code-quality/use-roslyn-analyzers#suppress-violations)。</span><span class="sxs-lookup"><span data-stu-id="56272-105">For more information, see [Suppress violations](/visualstudio/code-quality/use-roslyn-analyzers#suppress-violations).</span></span>

<span data-ttu-id="56272-106">有关规则严重性的详细信息，请参阅 [配置规则严重性](~/docs/fundamentals/code-analysis/configuration-options.md#severity-level)。</span><span class="sxs-lookup"><span data-stu-id="56272-106">For more information about rule severities, see [Configure rule severity](~/docs/fundamentals/code-analysis/configuration-options.md#severity-level).</span></span>
