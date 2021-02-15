---
description: 了解更多相关信息：无法 <methodname> 在不进行收缩转换的情况下使用这些参数调用可访问的重载 ""： <list>
title: 无 <methodname> 需收缩转换即可用这些参数调用可访问的重载 ""： <list>
ms.date: 07/20/2015
f1_keywords:
- vbrAmbiguousCall2
ms.assetid: 13b20ffa-9f02-4971-a3cb-e08b402fd971
ms.openlocfilehash: a802b420a01c1894feca2c61c0bfdbb7be5104f5
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100475703"
---
# <a name="no-accessible-overloaded-methodname-can-be-called-with-these-arguments-without-a-narrowing-conversion-list"></a><span data-ttu-id="2a870-103">无 \<methodname> 需收缩转换即可用这些参数调用可访问的重载 ""： \<list></span><span class="sxs-lookup"><span data-stu-id="2a870-103">No accessible overloaded '\<methodname>' can be called with these arguments without a narrowing conversion: \<list></span></span>

<span data-ttu-id="2a870-104">调用了重载方法，但是该方法必须进行缩放转换才能与提供的参数列表匹配。</span><span class="sxs-lookup"><span data-stu-id="2a870-104">An overloaded method was called, but the method cannot be matched with the list of provided arguments without a narrowing conversion.</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="2a870-105">更正此错误</span><span class="sxs-lookup"><span data-stu-id="2a870-105">To correct this error</span></span>  
  
1. <span data-ttu-id="2a870-106">指定 `Option Strict Off`。</span><span class="sxs-lookup"><span data-stu-id="2a870-106">Specify `Option Strict Off`.</span></span>
  
2. <span data-ttu-id="2a870-107">更改参数以匹配重载方法的签名。</span><span class="sxs-lookup"><span data-stu-id="2a870-107">Change the arguments to match a signature of the overloaded method.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2a870-108">请参阅</span><span class="sxs-lookup"><span data-stu-id="2a870-108">See also</span></span>

- [<span data-ttu-id="2a870-109">按值和按引用传递参数</span><span class="sxs-lookup"><span data-stu-id="2a870-109">Passing Arguments by Value and by Reference</span></span>](../programming-guide/language-features/procedures/passing-arguments-by-value-and-by-reference.md)
- [<span data-ttu-id="2a870-110">Widening and Narrowing Conversions</span><span class="sxs-lookup"><span data-stu-id="2a870-110">Widening and Narrowing Conversions</span></span>](../programming-guide/language-features/data-types/widening-and-narrowing-conversions.md)
