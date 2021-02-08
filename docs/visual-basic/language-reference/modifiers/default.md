---
description: '了解详细信息：默认 (Visual Basic) '
title: 默认
ms.date: 07/20/2015
f1_keywords:
- vb.Default
helpviewer_keywords:
- defaults, properties
- properties [Visual Basic], default
- default properties, in Visual Basic
- Default keyword [Visual Basic]
- default properties
ms.assetid: 45fce9b9-d212-4b2d-ab86-6e359b8b57af
ms.openlocfilehash: fe135df4f29ae3c4064c97d4f2789be7f4f3d8f9
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99774598"
---
# <a name="default-visual-basic"></a>Default (Visual Basic)

将属性标识为其类、结构或接口的默认属性。  
  
## <a name="remarks"></a>备注  

 类、结构或接口最多可以将其一个属性指定为 *默认属性*，前提是该属性至少采用一个参数。 如果代码在未指定成员的情况下对类或结构进行引用，则 Visual Basic 解析对默认属性的引用。  
  
 默认属性可能会减少源代码中的字符，但会使代码更难以阅读。 如果调用代码不熟悉你的类或结构，则当它对类或结构名称进行引用时，该引用是否访问类或结构本身，或者默认属性，则不能确定这一点。 这可能会导致编译器错误或细微的运行时逻辑错误。  
  
 通过始终使用 [Option Strict 语句](../statements/option-strict-statement.md) 将编译器类型检查设置为，可以在一定程度上减少默认属性错误的几率 `On` 。  
  
 如果打算在代码中使用预定义的类或结构，则必须确定它是否具有默认属性，如果是，则必须确定其名称。  
  
 由于这些缺点，你应考虑不要定义默认属性。 为实现代码可读性，还应考虑始终显式引用所有属性，甚至是默认属性。  
  
 `Default`可以在此上下文中使用修饰符：  
  
 [Property Statement](../statements/property-statement.md)  
  
## <a name="see-also"></a>请参阅

- [如何：在 Visual Basic 中声明和调用默认属性](../../programming-guide/language-features/procedures/how-to-declare-and-call-a-default-property.md)
- [关键字](../keywords/index.md)
