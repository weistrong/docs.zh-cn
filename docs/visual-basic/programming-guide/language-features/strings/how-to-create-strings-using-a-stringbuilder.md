---
description: 了解有关详细信息，请参阅如何：在 Visual Basic 中使用 StringBuilder 创建字符串
title: 如何：使用 StringBuilder 创建字符串
ms.date: 07/20/2015
helpviewer_keywords:
- StringBuilder class
- strings [Visual Basic], using StringBuilder
ms.assetid: 9c042880-aa16-432e-9ccb-cd00abda9ae3
ms.openlocfilehash: 6def32517f71ec3c2a7795c3395e3e572903ce1e
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100429814"
---
# <a name="how-to-create-strings-using-a-stringbuilder-in-visual-basic"></a>如何：在 Visual Basic 中使用 StringBuilder 创建字符串

此示例使用类从多个较小的字符串构造一个长字符串 <xref:System.Text.StringBuilder> 。 <xref:System.Text.StringBuilder>类比 `&=` 用于连接多个字符串的运算符更有效。

## <a name="example"></a>示例

下面的示例创建类的一个实例 <xref:System.Text.StringBuilder> ，将1000字符串追加到该实例，然后返回该实例的字符串表示形式：

 [!code-vb[VbVbalrStrings#70](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStrings/VB/Class2.vb#70)]

## <a name="see-also"></a>请参阅

- [使用 StringBuilder 类](../../../../standard/base-types/stringbuilder.md)
- [&= 运算符](../../../language-reference/operators/and-assignment-operator.md)
- [字符串](index.md)
- [新建字符串](../../../../standard/base-types/creating-new.md)
- [控制字符串](../../../../standard/base-types/best-practices-strings.md)
