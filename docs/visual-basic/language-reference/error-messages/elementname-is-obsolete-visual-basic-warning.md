---
description: '了解详细信息： BC40008： " <elementname> " 已过时 (Visual Basic 警告) '
title: “<elementname>”已过时（Visual Basic 警告）
ms.date: 07/20/2015
f1_keywords:
- vbc40008
- bc40008
helpviewer_keywords:
- BC40008
ms.assetid: 729e3eb5-76ac-4c55-9fdd-78350e0de55e
ms.openlocfilehash: 6fea3526f19b139af103f21ddd89f2272eb6eac5
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99796569"
---
# <a name="bc40008-elementname-is-obsolete-visual-basic-warning"></a>BC40008： " \<elementname> " 已过时 (Visual Basic 警告) 

语句试图访问编程元素，此元素已标记有 <xref:System.ObsoleteAttribute> 特性及将其视为警告的指令。

 可以通过将 <xref:System.ObsoleteAttribute> 应用于任意编程元素，将其标记为不再使用。 如果执行此操作，则可以将特性的 <xref:System.ObsoleteAttribute.IsError%2A> 属性设置为 `True` 或 `False`。 如果设置为 `True`，则编译器将尝试使用该元素的操作视为错误。 如果设置为 `False`，或将其默认为 `False`，则编译器会在有操作尝试使用该元素时发出警告。

 默认情况下，此消息是一个警告，因为 <xref:System.ObsoleteAttribute.IsError%2A> 的 <xref:System.ObsoleteAttribute> 属性为 `False`。 有关隐藏警告或将警告视为错误的详细信息，请参阅 [Configuring Warnings in Visual Basic](/visualstudio/ide/configuring-warnings-in-visual-basic)。

 **错误 ID：** BC40008

## <a name="to-correct-this-error"></a>更正此错误

- 确保源代码引用的元素名称拼写正确。

## <a name="see-also"></a>请参阅

- [属性概述](../../programming-guide/concepts/attributes/index.md)
