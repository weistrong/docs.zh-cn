---
description: '了解有关以下内容的详细信息： Exit 语句 (Visual Basic) '
title: Exit 语句
ms.date: 07/20/2015
f1_keywords:
- vb.Exit
helpviewer_keywords:
- execution [Visual Basic], ending
- files [Visual Basic], closing
- programs [Visual Basic], quitting
- code, exiting
- Exit statement [Visual Basic]
- program termination
- execution [Visual Basic], stopping
ms.assetid: 760bfb32-5c3f-4bdb-a432-9a6001c92db7
ms.openlocfilehash: 54af7fbf908dbad829cf6f08bf442dfe85e35610
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99769114"
---
# <a name="exit-statement-visual-basic"></a>Exit 语句 (Visual Basic)

退出过程或块并将控制立即传输到过程调用或块定义后面的语句。

## <a name="syntax"></a>语法

```vb
Exit { Do | For | Function | Property | Select | Sub | Try | While }
```

## <a name="statements"></a>语句

 `Exit Do`  
 立即退出 `Do` 出现该循环的循环。 继续执行语句后面的语句 `Loop` 。 `Exit Do` 只能在循环内使用 `Do` 。 在嵌套循环内使用时 `Do` ， `Exit Do` 将退出最内层循环，并将控制转移到下一个更高的嵌套级别。

 `Exit For`  
 立即退出 `For` 出现该循环的循环。 继续执行语句后面的语句 `Next` 。 `Exit For` 只能在 `For` ... `Next` 或 `For Each` ... `Next` 循环内使用。 在嵌套循环内使用时 `For` ， `Exit For` 将退出最内层循环，并将控制转移到下一个更高的嵌套级别。

 `Exit Function`  
 会立即退出 `Function` 显示该过程。 继续执行调用过程的语句后面的语句 `Function` 。 `Exit Function` 只能在过程中使用 `Function` 。

 若要指定一个返回值，可以在语句前面的行上向函数名称赋值 `Exit Function` 。 若要分配返回值并在一个语句中退出函数，可以改为使用 [Return 语句](return-statement.md)。

 `Exit Property`  
 会立即退出 `Property` 显示该过程。 执行将继续执行调用过程的语句 `Property` ，即，语句请求或设置属性的值。 `Exit Property` 只能在属性的或过程内使用 `Get` `Set` 。

 若要在过程中指定返回值 `Get` ，可以在语句之前的行上将值分配给函数名称 `Exit Property` 。 若要分配返回值并 `Get` 在一个语句中退出该过程，可以改为使用 `Return` 语句。

 在 `Set` 过程中， `Exit Property` 语句与语句等效 `Return` 。

 `Exit Select`  
 立即退出 `Select Case` 出现它的块。 继续执行语句后面的语句 `End Select` 。 `Exit Select` 只能在语句内使用 `Select Case` 。

 `Exit Sub`  
 会立即退出 `Sub` 显示该过程。 继续执行调用过程的语句后面的语句 `Sub` 。 `Exit Sub` 只能在过程中使用 `Sub` 。

 在 `Sub` 过程中， `Exit Sub` 语句与语句等效 `Return` 。

 `Exit Try`  
 立即退出 `Try` `Catch` 出现它的或块。 `Finally`如果存在块，则继续执行，否则语句后跟语句后面的语句 `End Try` 。 `Exit Try` 只能在或块中使用 `Try` `Catch` ，不能在块内使用 `Finally` 。

 `Exit While`  
 立即退出 `While` 出现该循环的循环。 继续执行语句后面的语句 `End While` 。 `Exit While` 只能在循环内使用 `While` 。 在嵌套循环内使用时 `While` ，将 `Exit While` 控制转移到循环中的一个嵌套级别（发生时） `Exit While` 。

## <a name="remarks"></a>备注

不要将 `Exit` 语句与 `End` 语句混淆。 `Exit` 不定义语句的末尾。

## <a name="example"></a>示例

在下面的示例中，当变量大于100时，循环条件将停止循环 `index` 。 `If`但是，循环中的语句会导致语句在 `Exit Do` 索引变量大于10时停止循环。

[!code-vb[VbVbalrStatements#133](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStatements/VB/class10.vb#133)]

## <a name="example"></a>示例

下面的示例将返回值分配给函数名称 `myFunction` ，然后使用 `Exit Function` 从函数返回：

[!code-vb[VbVbalrStatements#23](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStatements/VB/Class1.vb#23)]

## <a name="example"></a>示例

下面的示例使用 [Return 语句](return-statement.md) 来分配返回值并退出函数：

[!code-vb[VbVbalrStatements#24](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStatements/VB/Class1.vb#24)]

## <a name="see-also"></a>请参阅

- [Continue 语句](continue-statement.md)
- [Do...Loop 语句](do-loop-statement.md)
- [End 语句](end-statement.md)
- [For Each...Next 语句](for-each-next-statement.md)
- [For...Next 语句](for-next-statement.md)
- [Function 语句](function-statement.md)
- [Return 语句](return-statement.md)
- [Stop 语句](stop-statement.md)
- [Sub 语句](sub-statement.md)
- [Try...Catch...Finally 语句](try-catch-finally-statement.md)
