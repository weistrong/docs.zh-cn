---
description: '了解详细信息： (Visual Basic 的 Sub 过程) '
title: Sub 过程
ms.date: 07/20/2015
helpviewer_keywords:
- Sub procedures [Visual Basic], about Sub procedures
- statement blocks
- Sub procedures [Visual Basic], calling
- procedures [Visual Basic], calling
- Sub procedures [Visual Basic], syntax
- Sub procedures
- procedures [Visual Basic], Sub
- syntax [Visual Basic], Sub procedures
ms.assetid: 6a0a4958-ed0a-4d3d-8d31-0772c82bda58
ms.openlocfilehash: fe9d26fb2d18fbd29820af7aca96b826d7b45d0b
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100466505"
---
# <a name="sub-procedures-visual-basic"></a>Sub 过程 (Visual Basic) 

`Sub`过程是由和语句括起来的一系列 Visual Basic `Sub` 语句 `End Sub` 。 此 `Sub` 过程执行一个任务，然后将控制权返回给调用代码，但它不会将值返回给调用代码。

每次调用该过程时，都会执行其语句，从语句后面的第一个可执行语句开始， `Sub` 到遇到的第一个 `End Sub` 、 `Exit Sub` 或 `Return` 语句结束。

您可以 `Sub` 在模块、类和结构中定义过程。 默认情况下，它是 `Public` ，这意味着您可以从应用程序中可以访问您定义它的模块、类或结构的任何位置调用它。 术语 *方法* 描述了 `Sub` `Function` 从其定义模块、类或结构外部访问的或过程。 有关详细信息，请参阅[过程](./index.md)。

`Sub`过程可以采用由调用代码传递给它的参数，如常量、变量或表达式。

## <a name="declaration-syntax"></a>声明语法

声明过程的语法如下所示 `Sub` ：

```vb
[modifiers] Sub SubName[(parameterList)]
    ' Statements of the Sub procedure.
End Sub
```

`modifiers`可以指定访问级别以及有关重载、重写、共享和隐藏的信息。 有关详细信息，请参阅 [Sub 语句](../../../language-reference/statements/sub-statement.md)。

## <a name="parameter-declaration"></a>参数声明

声明每个过程参数的方式与声明变量的方式类似，即指定参数名称和数据类型。 还可以指定传递机制，并指定参数是可选的还是参数数组。

参数列表中每个参数的语法如下所示：

```vb
[Optional] [ByVal | ByRef] [ParamArray] parameterName As DataType
```

如果该参数是可选的，则还必须提供默认值作为其声明的一部分。 指定默认值的语法如下所示：

```vb
Optional [ByVal | ByRef]  parameterName As DataType = defaultValue
```

### <a name="parameters-as-local-variables"></a>参数作为局部变量

当控件传递给过程时，每个参数都被视为局部变量。 这意味着其生存期与过程的生存期相同，其作用域为整个过程。

## <a name="calling-syntax"></a>调用语法

`Sub`使用独立调用语句显式调用过程。 不能通过在表达式中使用其名称来调用它。 必须为所有非可选参数提供值，并且必须将参数列表括在括号中。 如果未提供任何参数，则可以选择省略括号。 关键字的使用 `Call` 是可选的，但不建议使用。

对过程的调用语法如下所示 `Sub` ：

```vb
[Call] SubName[(argumentlist)]
```

可以 `Sub` 从定义方法的类的外部调用该方法。 首先，必须使用 `New` 关键字创建类的实例，或调用返回类的实例的方法。 有关详细信息，请参阅 [New 运算符](../../../language-reference/operators/new-operator.md)。 然后，可以使用以下语法对 `Sub` 实例对象调用方法：

```vb
object.MethodName[(argumentList)]
```

### <a name="illustration-of-declaration-and-call"></a>声明和调用的插图

以下 `Sub` 过程告知计算机操作员应用程序将要执行的任务，还会显示时间戳。 应用程序只需 `tellOperator` 从不同位置进行调用，而不是在每个任务开始时都重复此代码。 每个调用都在参数中传递一个字符串 `task` ，该字符串标识要启动的任务。

[!code-vb[VbVbcnProcedures#2](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnProcedures/VB/Class1.vb#2)]

下面的示例演示对的典型调用 `tellOperator` 。

[!code-vb[VbVbcnProcedures#3](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnProcedures/VB/Class1.vb#3)]

## <a name="see-also"></a>请参阅

- [过程](./index.md)
- [Function 过程](./function-procedures.md)
- [Property 过程](./property-procedures.md)
- [运算符过程](./operator-procedures.md)
- [过程形参和实参](./procedure-parameters-and-arguments.md)
- [Sub 语句](../../../language-reference/statements/sub-statement.md)
- [如何：调用不返回值的过程](./how-to-call-a-procedure-that-does-not-return-a-value.md)
- [如何：在 Visual Basic 中调用事件处理程序](./how-to-call-an-event-handler.md)
