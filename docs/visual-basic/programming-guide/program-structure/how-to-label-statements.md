---
description: '了解有关详细信息，请参阅如何：标记语句 (Visual Basic) '
title: 如何：标记语句
ms.date: 07/20/2015
helpviewer_keywords:
- colons (:)
- statements [Visual Basic], labels
- ': separator character'
- Visual Basic code, labeling statements
ms.assetid: 38f1ff43-2054-42cb-963b-1998e60c6ed4
ms.openlocfilehash: 4efb320dad7d52f6e9b94f6e6f81730f94b5966b
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100433247"
---
# <a name="how-to-label-statements-visual-basic"></a>如何：标记语句 (Visual Basic)

语句块由用冒号分隔的代码行组成。 以标识字符串或整数开头的代码行称为 " *标记*"。 语句标签用于标记代码行，以将其标识为与等语句一起使用 `On Error Goto` 。

标签可以是有效 Visual Basic 标识符（如标识编程元素的标识符），也可以是整数文本。 标签必须出现在源代码行的开头，并且必须后跟一个冒号，而不考虑它是否后跟同一行中的语句。

编译器通过检查行首是否与任何已定义的标识符匹配来标识标签。 如果不是，编译器将假定它是一个标签。

标签具有自己的声明空间，不会干扰其他标识符。 标签的范围是方法的主体。 标签声明优先于任何不明确的情况。

> [!NOTE]
> 标签只能用于方法中的可执行语句。

## <a name="to-label-a-line-of-code"></a>为代码行添加标签

在源代码行的开头放置一个标识符，后跟一个冒号。

例如，以下代码行分别标记有 `Jump` 和 `120` ：

[!code-vb[VbVbalrStatements#708](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStatements/VB/Class1.vb#708)]

## <a name="see-also"></a>请参阅

- [语句](../language-features/statements.md)
- [Declared Element Names](../language-features/declared-elements/declared-element-names.md)
- [程序结构和代码约定](program-structure-and-code-conventions.md)
