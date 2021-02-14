---
description: '了解有关详细信息，请参阅如何：验证表示日期或时间的字符串 (Visual Basic) '
title: 如何：验证表示日期或时间的字符串
ms.date: 07/20/2015
helpviewer_keywords:
- strings [Visual Basic], validating
- String data type [Visual Basic], validation
ms.assetid: ae7d4b29-3436-4032-bdbf-4650eb1c8e19
ms.openlocfilehash: 4e9255717d1711d8e9839c218a78b359549d9eef
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100424250"
---
# <a name="how-to-validate-strings-that-represent-dates-or-times-visual-basic"></a>如何：验证表示日期或时间的字符串 (Visual Basic)

下面的代码示例设置一个 `Boolean` 值，该值指示字符串是否表示有效的日期或时间。  
  
## <a name="example"></a>示例  

 [!code-vb[VbVbcnRegEx#2](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnRegEx/VB/Class1.vb#2)]  
  
## <a name="compile-the-code"></a>编译代码  

 `("01/01/03")`将和替换为 `"9:30 PM"` 要验证的日期和时间。 您可以使用 `String` 变量或返回字符串的方法（如）将字符串替换为另一个硬编码字符串 `InputBox` 。  
  
## <a name="robust-programming"></a>可靠编程  

 使用此方法在尝试将转换为变量之前验证字符串 `String` `DateTime` 。 首先检查日期或时间，您可以避免在运行时生成异常。  
  
## <a name="see-also"></a>请参阅

- <xref:Microsoft.VisualBasic.Information.IsDate%2A>
- <xref:Microsoft.VisualBasic.Interaction.InputBox%2A>
- [验证字符串 (Visual Basic)](validating-strings.md)
