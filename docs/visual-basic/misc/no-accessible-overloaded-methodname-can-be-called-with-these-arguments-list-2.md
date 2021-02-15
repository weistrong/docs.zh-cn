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
# <a name="no-accessible-overloaded-methodname-can-be-called-with-these-arguments-without-a-narrowing-conversion-list"></a>无 \<methodname> 需收缩转换即可用这些参数调用可访问的重载 ""： \<list>

调用了重载方法，但是该方法必须进行缩放转换才能与提供的参数列表匹配。  
  
## <a name="to-correct-this-error"></a>更正此错误  
  
1. 指定 `Option Strict Off`。
  
2. 更改参数以匹配重载方法的签名。  
  
## <a name="see-also"></a>请参阅

- [按值和按引用传递参数](../programming-guide/language-features/procedures/passing-arguments-by-value-and-by-reference.md)
- [Widening and Narrowing Conversions](../programming-guide/language-features/data-types/widening-and-narrowing-conversions.md)
