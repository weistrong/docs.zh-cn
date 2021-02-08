---
description: '详细了解： MustOverride (Visual Basic) '
title: New
ms.date: 07/20/2015
f1_keywords:
- vb.MustOverride
- MustOverride
helpviewer_keywords:
- virtual elements [Visual Basic], pure
- elements [Visual Basic], pure virtual
- properties [Visual Basic], redefining
- procedures [Visual Basic], overriding
- overriding, MustOverride keyword
- procedures [Visual Basic], redefining
- pure virtual elements [Visual Basic]
- MustOverride keyword [Visual Basic]
- properties [Visual Basic], overriding
ms.assetid: 6e9d9ad6-bb64-433f-b32b-3ef84293bf96
ms.openlocfilehash: df7200a7f7ec4bfda34765747d6318bc50a38dd1
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99774520"
---
# <a name="mustoverride-visual-basic"></a>MustOverride (Visual Basic)

指定在此类中未实现的属性或过程，并且在使用之前必须在派生类中重写该属性或过程。  
  
## <a name="remarks"></a>备注  

 `MustOverride`只能在属性或过程声明语句中使用。 指定的属性或过程 `MustOverride` 必须是类的成员，并且该类必须标记为 [MustInherit](mustinherit.md)。  
  
## <a name="rules"></a>规则  
  
- **不完整声明。** 如果指定 `MustOverride` ，则不会为属性或过程提供任何其他代码行，甚至不为 `End Function` 、或语句提供任何代码行 `End Property` `End Sub` 。  
  
- **组合修饰符。** 不能 `MustOverride` `NotOverridable` `Overridable` `Shared` 在同一声明中同时指定、或。  
  
- **隐藏和重写操作。** 隐藏和重写操作都可重新定义继承的元素，但这两种方法之间又具有很大的差异。 有关详细信息，请参阅 [Visual Basic 中的隐藏](../../programming-guide/language-features/declared-elements/shadowing.md)。  
  
- **替代条款。** 除了在重写中外，不能使用的元素有时称为 *纯虚拟* 元素。  
  
 `MustOverride` 修饰符可用于下面的上下文中：  
  
 [Function 语句](../statements/function-statement.md)  
  
 [Property Statement](../statements/property-statement.md)  
  
 [Sub 语句](../statements/sub-statement.md)  
  
## <a name="see-also"></a>请参阅

- [NotOverridable](notoverridable.md)
- [Overrides](overridable.md)
- [替代](overrides.md)
- [MustInherit](mustinherit.md)
- [关键字](../keywords/index.md)
- [Visual Basic 中的隐藏](../../programming-guide/language-features/declared-elements/shadowing.md)
