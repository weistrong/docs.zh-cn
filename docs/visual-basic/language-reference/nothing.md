---
description: '了解详细信息： Nothing 关键字 (Visual Basic) '
title: Nothing 关键字
ms.date: 07/20/2015
f1_keywords:
- Nothing
- vb.Nothing
helpviewer_keywords:
- Nothing keyword [Visual Basic]
- Nothing keyword [Visual Basic], syntax
ms.assetid: 06176e2d-bbf7-4a37-afaa-a86ad21ee99f
ms.openlocfilehash: c77f39c0a431dd05aabd24a235fb2dc88ea29e69
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99674722"
---
# <a name="nothing-keyword-visual-basic"></a>无关键字 (Visual Basic) 

表示任意数据类型的默认值。 对于引用类型，默认值为 `null` 引用。 对于值类型，默认值取决于值类型是否可以为 null。

> [!NOTE]
> 对于不可为 null 的值类型， `Nothing` Visual Basic 中的与 c # 中的不同 `null` 。 在 Visual Basic 中，如果将不可以为 null 的值类型的变量设置为 `Nothing` ，则该变量将设置为其声明的类型的默认值。 在 c # 中，如果将不可以为 null 的值类型的变量分配给 `null` ，则会发生编译时错误。

## <a name="remarks"></a>备注

`Nothing` 表示数据类型的默认值。 默认值取决于变量是值类型还是引用类型。

*值类型* 的变量直接包含其值。 值类型包括所有数值数据类型、 `Boolean` 、 `Char` 、 `Date` 、所有结构和所有枚举。 *引用类型* 的变量存储对内存中对象的实例的引用。 引用类型包括类、数组、委托和字符串。 有关详细信息，请参阅 [值类型和引用类型](../programming-guide/language-features/data-types/value-types-and-reference-types.md)。

如果变量是值类型，则的行为 `Nothing` 取决于变量是否为可为 null 的数据类型。 若要表示可以为 null 的值类型，请向 `?` 类型名称添加修饰符。 分配 `Nothing` 给可以为 null 的变量会将值设置为 `null` 。 有关详细信息和示例，请参阅 [可以为 null 的值类型](../programming-guide/language-features/data-types/nullable-value-types.md)。

如果变量是不可为 null 的值类型，则分配 `Nothing` 给它会将它设置为其声明类型的默认值。 如果该类型包含变量成员，则它们都设置为其默认值。 下面的示例对标量类型进行了说明。

[!code-vb[VbVbalrKeywords#7](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrKeywords/VB/Class2.vb#7)]

如果变量为引用类型，则 `Nothing` 为变量赋值会将其设置为 `null` 变量类型的引用。 设置为引用的变量 `null` 不与任何对象关联。 下面的示例演示这一操作：

[!code-vb[VbVbalrKeywords#8](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrKeywords/VB/class3.vb#8)]

当检查引用 (或可以为 null 的值类型) 变量是否为时 `null` ，请不要使用 `= Nothing` 或 `<> Nothing` 。 始终使用 `Is Nothing` 或 `IsNot Nothing` 。

对于 Visual Basic 中的字符串，空字符串等于 `Nothing` 。 因此， `"" = Nothing` 为 true。

下面的示例演示使用 `Is` 和运算符的比较 `IsNot` ：

[!code-vb[VbVbalrKeywords#9](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrKeywords/VB/Class4.vb#9)]

如果在不使用子句的情况下声明变量 `As` 并将其设置为 `Nothing` ，则该变量的类型为 `Object` 。 这是一个示例 `Dim something = Nothing` 。 当 `Option Strict` 处于打开 `Option Infer` 状态且处于关闭状态时，会发生编译时错误。

将分配 `Nothing` 给对象变量时，它将不再引用任何对象实例。 如果变量以前引用了某个实例，则将其设置为不 `Nothing` 会终止实例本身。 实例终止，仅在垃圾回收器 (GC) 检测到没有剩余活动引用后，才会释放与之关联的内存和系统资源。

`Nothing` 与对象不同 <xref:System.DBNull> ，后者表示未初始化的变量或不存在的数据库列。

## <a name="see-also"></a>请参阅

- [Dim 语句](./statements/dim-statement.md)
- [对象生存期：如何创建和销毁对象](../programming-guide/language-features/objects-and-classes/object-lifetime-how-objects-are-created-and-destroyed.md)
- [Visual Basic 中的生存期](../programming-guide/language-features/declared-elements/lifetime.md)
- [Is 运算符](./operators/is-operator.md)
- [IsNot 运算符](./operators/isnot-operator.md)
- [可以为 null 的值类型](../programming-guide/language-features/data-types/nullable-value-types.md)
