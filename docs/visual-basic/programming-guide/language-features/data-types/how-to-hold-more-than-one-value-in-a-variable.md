---
description: '了解有关详细信息，请参阅如何：在变量中保存多个值 (Visual Basic) '
title: 如何：在一个变量中保留多个值
ms.date: 07/20/2015
helpviewer_keywords:
- classes [Visual Basic], composite data types
- composite types [Visual Basic]
- composite data types [Visual Basic]
- data types [Visual Basic], composite
- arrays [Visual Basic], composite data types
- structures [Visual Basic], composite data types
- arrays [Visual Basic], compilation errors
- types [Visual Basic], composite
ms.assetid: 5fe0e558-aac2-4a40-b7f2-7cfea7336917
ms.openlocfilehash: 5248bc29f58cccf3b8ced95d3fba8f0d39033a83
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100483997"
---
# <a name="how-to-hold-more-than-one-value-in-a-variable-visual-basic"></a>如何：在一个变量中保存多个值 (Visual Basic)

如果将变量声明为 *复合数据类型*，则该变量包含多个值。

[复合数据类型](composite-data-types.md) 包括结构、数组和类。 复合数据类型的变量可以包含基本数据类型和其他复合类型的组合。 结构和类可以保存代码以及数据。

## <a name="to-hold-more-than-one-value-in-a-variable"></a>在一个变量中保存多个值

1. 确定要为变量使用哪种复合数据类型。

2. 如果尚未定义复合数据类型，请对其进行定义，使变量可以使用它。

    - 使用 [结构语句](../../../language-reference/statements/structure-statement.md)定义结构。

    - 定义带有 [Dim 语句](../../../language-reference/statements/dim-statement.md)的数组。

    - 使用 [类语句](../../../language-reference/statements/class-statement.md)定义类。

3. 使用语句声明变量 `Dim` 。

4. 使用子句的变量名称 `As` 。

5. 在关键字后跟 `As` 适当的复合数据类型的名称。

## <a name="see-also"></a>请参阅

- [数据类型](../../../language-reference/data-types/index.md)
- [类型字符](type-characters.md)
- [复合数据类型](composite-data-types.md)
- [结构](structures.md)
- [数组](../arrays/index.md)
- [对象和类](../objects-and-classes/index.md)
- [Value Types and Reference Types](value-types-and-reference-types.md)
