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
# <a name="disable-and-enable-directives-visual-basic"></a><span data-ttu-id="ea283-102">#Disable 和 #Enable 指令 (Visual Basic) </span><span class="sxs-lookup"><span data-stu-id="ea283-102">#Disable and #Enable directives (Visual Basic)</span></span>

<span data-ttu-id="ea283-103">`#Disable`和 `#Enable` 指令是 Visual Basic 源代码编译器指令。</span><span class="sxs-lookup"><span data-stu-id="ea283-103">The `#Disable` and `#Enable` directives are Visual Basic source code compiler directives.</span></span> <span data-ttu-id="ea283-104">它们用于为代码区域禁用和重新启用特定警告。</span><span class="sxs-lookup"><span data-stu-id="ea283-104">They are used to disable and re-enable specific warnings for regions of code.</span></span>

```vb
' Suppress warning about no awaits in this method.
#Disable Warning BC42356
    Async Function TestAsync() As Task
        Console.WriteLine("testing")
    End Function
#Enable Warning BC42356
```

<span data-ttu-id="ea283-105">你还可以禁用和启用以逗号分隔的警告代码列表。</span><span class="sxs-lookup"><span data-stu-id="ea283-105">You can also disable and enable a comma-separated list of warning codes.</span></span>

## <a name="see-also"></a><span data-ttu-id="ea283-106">请参阅</span><span class="sxs-lookup"><span data-stu-id="ea283-106">See also</span></span>

- [<span data-ttu-id="ea283-107">Visual Basic 语言参考</span><span class="sxs-lookup"><span data-stu-id="ea283-107">Visual Basic Language Reference</span></span>](../index.md)
- [<span data-ttu-id="ea283-108">如何取消显示代码分析警告</span><span class="sxs-lookup"><span data-stu-id="ea283-108">How to suppress code analysis warnings</span></span>](../../../fundamentals/code-analysis/suppress-warnings.md)
