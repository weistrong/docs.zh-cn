---
description: '了解详细信息：单一数据类型 (Visual Basic) '
title: Single 数据类型
ms.date: 07/20/2015
f1_keywords:
- vb.Single
helpviewer_keywords:
- Single data type
- F literal type character [Visual Basic]
- trailing zeros
- real numbers
- literal type characters [Visual Basic], F
- trailing 0 characters [Visual Basic]
- identifier type characters [Visual Basic], !
- single-precision numbers
- '! identifier type character'
- 0 characters [Visual Basic], trailing
- data types [Visual Basic], assigning
- floating-point numbers [Visual Basic], Single data type
- numbers [Visual Basic], real
- zeros, trailing
- numbers [Visual Basic], floating point
ms.assetid: 224a2795-4cd5-496c-8f7a-a4f05a06d45d
ms.openlocfilehash: f30e21d3b2d2960a040609a9422ec71cc029f5be
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99792123"
---
# <a name="single-data-type-visual-basic"></a>Single 数据类型 (Visual Basic)

为正值，保留已签名的 IEEE 32 位 (4 个) 字节的单精度浮点数，范围为-3.4028235 E + 38 到-1.401298 E-45，表示负值，从 1.401298 E-45 到 3.4028235 E + 38。 单精度数字存储实数的近似值。  
  
## <a name="remarks"></a>备注  

 使用 `Single` 数据类型可包含不需要的完整数据宽度的浮点值 `Double` 。 在某些情况下，公共语言运行时可以将变量紧密地打包在 `Single` 一起，并节省内存消耗。  
  
 `Single` 的默认值为 0。  
  
## <a name="programming-tips"></a>编程提示  
  
- **Precision.** 使用浮点数时，请记住，它们在内存中不一定有精确的表示形式。 这可能会导致某些操作产生意外结果，如值比较和 `Mod` 运算符。 有关详细信息，请参阅 [数据类型疑难解答](../../programming-guide/language-features/data-types/troubleshooting-data-types.md)。  
  
- **扩大.** `Single`数据类型扩大到 `Double` 。 这意味着你可以转换 `Single` 为， `Double` 而不会遇到 <xref:System.OverflowException?displayProperty=nameWithType> 错误。  
  
- **尾随零。** 浮点数据类型不包含尾随0字符的任何内部表示形式。 例如，它们不区分4.2000 和4.2。 因此，在显示或打印浮点值时，不会出现尾随0字符。  
  
- **键入字符。** 将文本类型字符 `F` 追加到文本会将其强制转换为 `Single` 数据类型。 将标识符类型字符 `!` 追加到任何标识符会将其强制转换为 `Single`。  
  
- **Framework 类型。** .NET Framework 中的对应类型是 <xref:System.Single?displayProperty=nameWithType> 结构。  
  
## <a name="see-also"></a>请参阅

- <xref:System.Single?displayProperty=nameWithType>
- [数据类型](index.md)
- [Decimal 数据类型](decimal-data-type.md)
- [Double 数据类型](double-data-type.md)
- [Type Conversion Functions](../functions/type-conversion-functions.md)
- [转换摘要](../keywords/conversion-summary.md)
- [有效使用数据类型](../../programming-guide/language-features/data-types/efficient-use-of-data-types.md)
- [数据类型疑难解答](../../programming-guide/language-features/data-types/troubleshooting-data-types.md)
