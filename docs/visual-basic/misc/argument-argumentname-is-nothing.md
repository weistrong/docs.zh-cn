---
description: 了解详细信息：参数 " <argumentname> " 为 Nothing
title: 参数“<argumentname>”为 Nothing
ms.date: 07/20/2015
f1_keywords:
- vbrArgument_InvalidNullValue1
ms.assetid: abbde904-c191-4911-8822-c9dd2f81d616
ms.openlocfilehash: a32426f8a0715f9fba07bc5617825ecdaeb565d1
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99700021"
---
# <a name="argument-argumentname-is-nothing"></a><span data-ttu-id="38475-103">参数“\<argumentname>”为 Nothing</span><span class="sxs-lookup"><span data-stu-id="38475-103">Argument '\<argumentname>' is Nothing</span></span>

<span data-ttu-id="38475-104">表达式包含 null 参数。</span><span class="sxs-lookup"><span data-stu-id="38475-104">An expression contains a null argument.</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="38475-105">更正此错误</span><span class="sxs-lookup"><span data-stu-id="38475-105">To correct this error</span></span>  
  
1. <span data-ttu-id="38475-106">检查表达式中参数的拼写是否正确。</span><span class="sxs-lookup"><span data-stu-id="38475-106">Check the spelling of arguments in the expression.</span></span> <span data-ttu-id="38475-107">拼写错误的变量名可能会隐式创建一个初始化为零的数值变量。</span><span class="sxs-lookup"><span data-stu-id="38475-107">A misspelled variable name can implicitly create a numeric variable that is initialized to zero.</span></span>  
  
2. <span data-ttu-id="38475-108">检查之前对表达式中的变量进行的操作，尤其是那些从其他过程作为参数传递给该过程的操作。</span><span class="sxs-lookup"><span data-stu-id="38475-108">Check previous operations on variables in the expression, especially those passed into the procedure as arguments from other procedures.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="38475-109">请参阅</span><span class="sxs-lookup"><span data-stu-id="38475-109">See also</span></span>

- [<span data-ttu-id="38475-110">按值和按引用传递参数</span><span class="sxs-lookup"><span data-stu-id="38475-110">Passing Arguments by Value and by Reference</span></span>](../programming-guide/language-features/procedures/passing-arguments-by-value-and-by-reference.md)
