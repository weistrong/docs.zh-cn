---
description: 了解详细信息：参数 "Life" 不能为零
title: 自变量“Life”不能为零
ms.date: 07/20/2015
f1_keywords:
- vbrFinancial_LifeNEZero
ms.assetid: c402da97-a2b2-4219-a83a-0cebbfdffef2
ms.openlocfilehash: e07c31ab73d6ad3f055adcbf7f4f67d48311c6cd
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100474871"
---
# <a name="argument-life-cannot-be-zero"></a><span data-ttu-id="6eafc-103">自变量“Life”不能为零</span><span class="sxs-lookup"><span data-stu-id="6eafc-103">Argument 'Life' cannot be zero</span></span>

<span data-ttu-id="6eafc-104">`Life`的参数（必须为指定资产的使用年限的长度的 `Double` ）无效。</span><span class="sxs-lookup"><span data-stu-id="6eafc-104">An argument for `Life`, which must be a `Double` that specifies the length of useful life of the asset, is not valid.</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="6eafc-105">更正此错误</span><span class="sxs-lookup"><span data-stu-id="6eafc-105">To correct this error</span></span>  
  
- <span data-ttu-id="6eafc-106">检查表达式中参数的拼写是否正确。</span><span class="sxs-lookup"><span data-stu-id="6eafc-106">Check the spelling of arguments in the expression.</span></span> <span data-ttu-id="6eafc-107">拼写错误的变量名可能会隐式创建一个初始化为零的数值变量。</span><span class="sxs-lookup"><span data-stu-id="6eafc-107">A misspelled variable name can implicitly create a numeric variable that is initialized to zero.</span></span>  
  
- <span data-ttu-id="6eafc-108">检查之前对表达式中的变量进行的操作，尤其是那些从其他过程作为参数传递给该过程的操作。</span><span class="sxs-lookup"><span data-stu-id="6eafc-108">Check previous operations on variables in the expression, especially those passed into the procedure as arguments from other procedures.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6eafc-109">请参阅</span><span class="sxs-lookup"><span data-stu-id="6eafc-109">See also</span></span>

- [<span data-ttu-id="6eafc-110">按值和按引用传递参数</span><span class="sxs-lookup"><span data-stu-id="6eafc-110">Passing Arguments by Value and by Reference</span></span>](../programming-guide/language-features/procedures/passing-arguments-by-value-and-by-reference.md)
