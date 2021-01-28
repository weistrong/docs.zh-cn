---
ms.openlocfilehash: b26e346f7076a57aef8ae7587ab1222b4100a323
ms.sourcegitcommit: 7e42488c2f8f63f6d499b5f8fb1dec5bac9ad254
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/28/2021
ms.locfileid: "98957931"
---
## <a name="suppress-a-warning"></a>禁止显示警告

若要取消规则冲突，请 `none` 在 EditorConfig 文件中将特定规则 ID 的严重性选项设置为。 例如：

```ini
[*.{cs,vb}]
dotnet_diagnostic.CA1822.severity = none
```

Visual Studio 提供了其他方式来禁止显示代码分析规则中的警告。 有关详细信息，请参阅 [取消冲突](/visualstudio/code-quality/use-roslyn-analyzers#suppress-violations)。

有关规则严重性的详细信息，请参阅 [配置规则严重性](~/docs/fundamentals/code-analysis/configuration-options.md#severity-level)。
