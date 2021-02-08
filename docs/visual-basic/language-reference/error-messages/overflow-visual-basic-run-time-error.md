---
description: '了解详细信息：溢出 (Visual Basic Run-Time 错误) '
title: 溢出（Visual Basic 运行时错误）
ms.date: 07/20/2015
f1_keywords:
- vbrERRID_Overflow
ms.assetid: c6a23279-3086-412a-bcff-ff8ed2cb8c6f
ms.openlocfilehash: a01a8916e09f9278dbdf6d594c5ef84d63b04c51
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99795451"
---
# <a name="overflow-visual-basic-run-time-error"></a>溢出（Visual Basic 运行时错误）

如果尝试的赋值超出了赋值目标的限制，则会发生溢出。  
  
## <a name="to-correct-this-error"></a>更正此错误  
  
1. 请确保赋值、计算和数据类型转换的结果不太大，无法在此类型的值所允许的变量范围内表示，如果需要，可将值分配给可保存更大范围的值的类型变量。  
  
2. 请确保对属性的赋值符合它们所建立到的属性的范围。  
  
3. 请确保在转换为整数的计算中使用的数字没有大于整数的结果。  
  
## <a name="see-also"></a>请参阅

- <xref:System.Int32.MaxValue?displayProperty=nameWithType>
- <xref:System.Double.MaxValue?displayProperty=nameWithType>
- [数据类型](../data-types/index.md)
- [错误类型](../../programming-guide/language-features/error-types.md)
