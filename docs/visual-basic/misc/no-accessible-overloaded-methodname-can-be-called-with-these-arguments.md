---
description: 了解更多相关信息：无法在 <methodname> 不进行收缩转换的情况下使用这些参数调用可访问的重载 ""
title: 必须进行收缩转换才能用这些参数调用可访问的重载“<methodname>”：
ms.date: 07/20/2015
f1_keywords:
- vbrAmbiguousMatch_NarrowingConversion1
ms.assetid: 2fdbadb9-8ef1-404a-a2ed-ce5f5e55cfcb
ms.openlocfilehash: ff70d43e5e5171055f631a6965b81b934bfb0b39
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100479174"
---
# <a name="no-accessible-overloaded-methodname-can-be-called-with-these-arguments-without-a-narrowing-conversion"></a><span data-ttu-id="a80b8-103">必须进行收缩转换才能用这些参数调用可访问的重载“\<methodname>”：</span><span class="sxs-lookup"><span data-stu-id="a80b8-103">No accessible overloaded '\<methodname>' can be called with these arguments without a narrowing conversion</span></span>

<span data-ttu-id="a80b8-104">调用了重载方法，但是方法不可与所提供的未进行收缩转换的参数列表相匹配。</span><span class="sxs-lookup"><span data-stu-id="a80b8-104">An overloaded method was called, but no method was matched with the list of provided arguments without a narrowing conversion.</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="a80b8-105">更正此错误</span><span class="sxs-lookup"><span data-stu-id="a80b8-105">To correct this error</span></span>  
  
1. <span data-ttu-id="a80b8-106">指定 `Option Strict Off`。</span><span class="sxs-lookup"><span data-stu-id="a80b8-106">Specify `Option Strict Off`.</span></span>  
  
2. <span data-ttu-id="a80b8-107">更改参数以匹配重载方法的其中一个签名。</span><span class="sxs-lookup"><span data-stu-id="a80b8-107">Change the arguments to match one of the signatures of the overloaded method.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a80b8-108">请参阅</span><span class="sxs-lookup"><span data-stu-id="a80b8-108">See also</span></span>

- [<span data-ttu-id="a80b8-109">按值和按引用传递参数</span><span class="sxs-lookup"><span data-stu-id="a80b8-109">Passing Arguments by Value and by Reference</span></span>](../programming-guide/language-features/procedures/passing-arguments-by-value-and-by-reference.md)
- [<span data-ttu-id="a80b8-110">Widening and Narrowing Conversions</span><span class="sxs-lookup"><span data-stu-id="a80b8-110">Widening and Narrowing Conversions</span></span>](../programming-guide/language-features/data-types/widening-and-narrowing-conversions.md)
