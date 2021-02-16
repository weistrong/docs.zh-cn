---
description: '了解有关详细信息，请参阅如何：引用对象的当前实例 (Visual Basic) '
title: 如何：引用对象的当前实例
ms.date: 07/20/2015
helpviewer_keywords:
- variables [Visual Basic], object
- objects [Visual Basic], referring to current instance
- instances [Visual Basic], referring to current
- current instance
- object variables [Visual Basic]
ms.assetid: 7f9b2c77-03cd-428f-adc2-b18070226e7c
ms.openlocfilehash: 84a52c9d0a8b1f588630b31d022490f37595850d
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100481735"
---
# <a name="how-to-refer-to-the-current-instance-of-an-object-visual-basic"></a>如何：引用对象的当前实例 (Visual Basic)

对象的 *当前实例* 是当前在其中执行代码的实例。  
  
 使用 `Me` 关键字引用当前实例。  
  
### <a name="to-refer-to-the-current-instance"></a>引用当前实例  
  
- 使用 `Me` 关键字，通常使用对象变量的名称。  
  
    ```vb  
    Me.ForeColor = System.Drawing.Color.Crimson  
    Me.Close()  
    ```  
  
     尽管 `Me` 的行为与对象变量类似，但不能对其进行声明或向其分配任何内容。 `Me` 始终引用当前实例。  
  
## <a name="see-also"></a>请参阅

- [对象变量](object-variables.md)
- [对象变量赋值](object-variable-assignment.md)
- [Me、My、MyBase 和 MyClass](../../program-structure/me-my-mybase-and-myclass.md)
