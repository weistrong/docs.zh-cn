---
description: 详细了解：中的对象变量 Visual Basic
title: 对象变量
ms.date: 07/20/2015
helpviewer_keywords:
- object variables [Visual Basic], about object variables
- variables [Visual Basic], object
- objects [Visual Basic], accessing
- object variables [Visual Basic]
ms.assetid: 6169a196-2b13-4ba5-a205-154bc1b87844
ms.openlocfilehash: 7c50dcbac32cdc841e513765d62f6ee711fc6049
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100478836"
---
# <a name="object-variables-in-visual-basic"></a>Visual Basic 中的对象变量

除了直接存储值以外，变量还可以引用对象。 将对象分配给变量的原因与将任何值分配给变量的原因相同：

- 变量名通常比访问对象本身所需的方法和属性的完整路径更短且更易于记忆。

- 使用引用对象的变量比通过所需的方法或属性重复访问对象本身更为有效。

- 在代码运行时，可以更改变量以引用其他对象。

## <a name="making-code-shorter"></a>使代码更短

可以使用对象变量缩短需要键入的代码。 下面的示例使用方法和属性的完整路径来访问 <xref:System.Windows.Forms.Control> 对象。

```vb
' Assume Me is a valid Form, or replace Me with a valid Form.
Me.ActiveForm.ActiveControl.Text = "Test"
Me.ActiveForm.ActiveControl.Location = New Point(100, 100)
Me.ActiveForm.ActiveControl.Show()
```

如果对控件使用对象变量，则可缩短此代码并加快执行速度。 应将对象变量声明为要分配给它的特定类 (`Control` 在此情况下) 。 将对象分配给变量后，可以将其视为与处理它所引用的对象完全相同。 可以设置或检索对象的属性或使用其任何方法。 下面的示例使用对象变量来简化前面的示例中的代码。

```vb
Dim ctrlActv As System.Windows.Forms.Control = Me.ActiveForm.ActiveControl
ctrlActv.Text = "Test"
ctrlActv.Location = New Point(100, 100)
ctrlActv.Show()
```

## <a name="see-also"></a>请参阅

- [变量声明](variable-declaration.md)
- [如何：加速访问具有长限定路径的对象](how-to-speed-up-access-to-an-object-with-a-long-qualification-path.md)
- [对象变量声明](object-variable-declaration.md)
- [对象变量赋值](object-variable-assignment.md)
- [对象变量值](object-variable-values.md)
