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
# <a name="disable-and-enable-directives-visual-basic"></a><span data-ttu-id="b564c-103">#Disable 和 #Enable 指令 (Visual Basic) </span><span class="sxs-lookup"><span data-stu-id="b564c-103">#Disable and #Enable directives (Visual Basic)</span></span>

<span data-ttu-id="b564c-104">`#Disable`和 `#Enable` 指令是 Visual Basic 源代码编译器指令。</span><span class="sxs-lookup"><span data-stu-id="b564c-104">The `#Disable` and `#Enable` directives are Visual Basic source code compiler directives.</span></span> <span data-ttu-id="b564c-105">它们用于为代码区域禁用和重新启用特定警告。</span><span class="sxs-lookup"><span data-stu-id="b564c-105">They are used to disable and re-enable specific warnings for regions of code.</span></span>

```vb
' Suppress warning about no awaits in this method.
#Disable Warning BC42356
    Async Function TestAsync() As Task
        Console.WriteLine("testing")
    End Function
#Enable Warning BC42356
```

<span data-ttu-id="b564c-106">你还可以禁用和启用以逗号分隔的警告代码列表。</span><span class="sxs-lookup"><span data-stu-id="b564c-106">You can also disable and enable a comma-separated list of warning codes.</span></span>

## <a name="see-also"></a><span data-ttu-id="b564c-107">请参阅</span><span class="sxs-lookup"><span data-stu-id="b564c-107">See also</span></span>

- [<span data-ttu-id="b564c-108">Visual Basic 语言参考</span><span class="sxs-lookup"><span data-stu-id="b564c-108">Visual Basic Language Reference</span></span>](../index.md)
- [<span data-ttu-id="b564c-109">如何禁止显示代码分析警告</span><span class="sxs-lookup"><span data-stu-id="b564c-109">How to suppress code analysis warnings</span></span>](../../../fundamentals/code-analysis/suppress-warnings.md)
