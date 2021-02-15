---
description: '了解有关详细信息，请参阅如何：创建在值中不更改的变量 (Visual Basic) '
title: 如何：创建固定值变量
ms.date: 07/20/2015
helpviewer_keywords:
- variables [Visual Basic], read-only
- variables [Visual Basic], constant value
ms.assetid: 86b59266-25df-4635-ae15-9b59c411d036
ms.openlocfilehash: 0392a27249de3bf604a73c8f8aaa16caf6f1c3e2
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100481930"
---
# <a name="how-to-create-a-variable-that-does-not-change-in-value-visual-basic"></a>如何：创建固定值变量 (Visual Basic)

不更改其值的变量的概念可能看似矛盾。 但在某些情况下，常量并不可行，并且具有固定值的变量很有用。 在这种情况下，可以使用 [ReadOnly](../../../language-reference/modifiers/readonly.md) 关键字定义成员变量。

在以下情况下，不能使用 [Const 语句](../../../language-reference/statements/const-statement.md) 来声明和分配常量值：

- `Const`语句不接受要使用的数据类型

- 在编译时不知道值

- 在编译时无法计算常量值

### <a name="to-create-a-variable-that-does-not-change-in-value"></a>创建在值中不变的变量

1. 在模块级别，用 [Dim 语句](../../../language-reference/statements/dim-statement.md)声明成员变量，并包括 [ReadOnly](../../../language-reference/modifiers/readonly.md) 关键字。

    ```vb
    Dim ReadOnly timeStarted
    ```

    `ReadOnly`只能在成员变量上指定。 这意味着必须在任何过程之外的模块级别定义变量。

2. 如果可以在编译时在单个语句中计算该值，请在语句中使用初始化子句 `Dim` 。 在 [As](../../../language-reference/statements/as-clause.md) 子句后跟一个等号 (`=`) ，后跟一个表达式。 确保编译器可以将此表达式计算为常数值。

    ```vb
    Dim ReadOnly timeStarted As Date = Now
    ```

    只能将一个值分配给一个 `ReadOnly` 变量。 完成此操作后，任何代码都不能更改其值。

    如果你不知道编译时的值，或在编译时不能在单个语句中计算该值，则仍可在构造函数中的运行时分配该值。 为此，必须 `ReadOnly` 在类或结构级别声明变量。 在该类或结构的构造函数中，计算变量的固定值，并将其分配给变量，然后再从构造函数返回。

## <a name="see-also"></a>请参阅

- [WriteOnly](../../../language-reference/modifiers/writeonly.md)
- [Const 语句](../../../language-reference/statements/const-statement.md)
