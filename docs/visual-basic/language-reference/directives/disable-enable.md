---
description: '了解详细信息： #Disable 和 #Enable 指令 (Visual Basic) '
title: Enable 和 Disable 指令
ms.date: 01/28/2021
helpviewer_keywords:
- directives, enable
- directives, disable
- disable directive
ms.openlocfilehash: d600cc959639a3f70bca5678fbc81aae0806c9cc
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99797258"
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
- [如何禁止显示代码分析警告](../../../fundamentals/code-analysis/suppress-warnings.md)
