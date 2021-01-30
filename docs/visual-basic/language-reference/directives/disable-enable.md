---
title: Enable 和 Disable 指令
ms.date: 01/28/2021
helpviewer_keywords:
- directives, enable
- directives, disable
- disable directive
ms.openlocfilehash: 3104b25c903465f3a650304f477b25a74591c8ba
ms.sourcegitcommit: 68c9d9d9a97aab3b59d388914004b5474cf1dbd7
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/30/2021
ms.locfileid: "99217236"
---
# <a name="disable-and-enable-directives-visual-basic"></a>#Disable 和 #Enable 指令 (Visual Basic) 

`#Disable`和 `#Enable` 指令是 Visual Basic 源代码编译器指令。 它们用于为代码区域禁用和重新启用特定警告。

```vb
' Suppress warning about no awaits in this method.
#Disable Warning BC42356
    Async Function TestAsync() As Task
        Console.WriteLine("testing")
    End Function
#Enable Warning BC42356
```

你还可以禁用和启用以逗号分隔的警告代码列表。

## <a name="see-also"></a>请参阅

- [Visual Basic 语言参考](../index.md)
- [如何取消显示代码分析警告](../../../fundamentals/code-analysis/suppress-warnings.md)
