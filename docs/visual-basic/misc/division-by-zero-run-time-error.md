---
description: '了解详细信息：除以零 (Visual Basic Run-Time 错误) '
title: 除数为零（Visual Basic 运行时错误）
ms.date: 07/20/2015
f1_keywords:
- vbrID11
ms.assetid: 5b9bc5d6-792e-48bc-a974-012e07ad95f3
ms.openlocfilehash: 50358e7ef24a0366d13145950282a3696173b6df
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100468585"
---
# <a name="division-by-zero-visual-basic-run-time-error"></a><span data-ttu-id="dc38a-103">除数为零（Visual Basic 运行时错误）</span><span class="sxs-lookup"><span data-stu-id="dc38a-103">Division by zero (Visual Basic Run-Time Error)</span></span>

<span data-ttu-id="dc38a-104">用作除数的表达式有一个值为零。</span><span class="sxs-lookup"><span data-stu-id="dc38a-104">An expression being used as a divisor has a value of zero.</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="dc38a-105">更正此错误</span><span class="sxs-lookup"><span data-stu-id="dc38a-105">To correct this error</span></span>  
  
1. <span data-ttu-id="dc38a-106">检查表达式中变量的拼写是否正确。</span><span class="sxs-lookup"><span data-stu-id="dc38a-106">Check the spelling of variables in the expression.</span></span> <span data-ttu-id="dc38a-107">拼写错误的变量名可能会隐式创建一个初始化为零的数值变量。</span><span class="sxs-lookup"><span data-stu-id="dc38a-107">A misspelled variable name can implicitly create a numeric variable that is initialized to zero.</span></span>  
  
2. <span data-ttu-id="dc38a-108">检查之前对表达式中的变量进行的操作，尤其是那些从其他过程作为参数传递给该过程的操作。</span><span class="sxs-lookup"><span data-stu-id="dc38a-108">Check previous operations on variables in the expression, especially those passed into the procedure as arguments from other procedures.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="dc38a-109">请参阅</span><span class="sxs-lookup"><span data-stu-id="dc38a-109">See also</span></span>

- [<span data-ttu-id="dc38a-110">按值和按引用传递参数</span><span class="sxs-lookup"><span data-stu-id="dc38a-110">Passing Arguments by Value and by Reference</span></span>](../programming-guide/language-features/procedures/passing-arguments-by-value-and-by-reference.md)
