---
description: '了解有关详细信息，请参阅如何：使用特性创建 C/c + + 联合 (Visual Basic) '
title: 如何：使用特性创建 C + + + 联合
ms.date: 07/20/2015
ms.assetid: 9352a7e4-c0da-4d07-aa14-55ed43736fcb
ms.openlocfilehash: 10717ec97efe866f4c3993cc26789f29d97b148a
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100437743"
---
# <a name="how-to-create-a-cc-union-by-using-attributes-visual-basic"></a>如何：使用特性创建 C/C++ 联合 (Visual Basic)

通过使用特性，可自定义结构在内存中的布局方式。 例如，可使用 `StructLayout(LayoutKind.Explicit)` 和 `FieldOffset` 特性在 C/C++ 中创建所谓的联合。

## <a name="example"></a>示例

在此代码段中，`TestUnion` 的所有字段均从内存中的同一位置开始。

```vb
' Add an Imports statement for System.Runtime.InteropServices.

<System.Runtime.InteropServices.StructLayout(
      System.Runtime.InteropServices.LayoutKind.Explicit)>
Structure TestUnion
    <System.Runtime.InteropServices.FieldOffset(0)>
    Public i As Integer

    <System.Runtime.InteropServices.FieldOffset(0)>
    Public d As Double

    <System.Runtime.InteropServices.FieldOffset(0)>
    Public c As Char

    <System.Runtime.InteropServices.FieldOffset(0)>
    Public b As Byte
End Structure
```

## <a name="example"></a>示例

下面是另一个示例，其中的字段从不同的显式设置位置开始。

```vb
' Add an Imports statement for System.Runtime.InteropServices.

 <System.Runtime.InteropServices.StructLayout(
      System.Runtime.InteropServices.LayoutKind.Explicit)>
Structure TestExplicit
     <System.Runtime.InteropServices.FieldOffset(0)>
     Public lg As Long

     <System.Runtime.InteropServices.FieldOffset(0)>
     Public i1 As Integer

     <System.Runtime.InteropServices.FieldOffset(4)>
     Public i2 As Integer

     <System.Runtime.InteropServices.FieldOffset(8)>
     Public d As Double

     <System.Runtime.InteropServices.FieldOffset(12)>
     Public c As Char

     <System.Runtime.InteropServices.FieldOffset(14)>
     Public b As Byte
 End Structure
```

两个整数字段 `i1` 和 `i2` 共享与 `lg` 相同的内存位置。 使用平台调用时，这种对结构布局的控制很有用。

## <a name="see-also"></a>请参阅

- <xref:System.Reflection>
- <xref:System.Attribute>
- [Visual Basic 编程指南](../../index.md)
- [特性](../../../../standard/attributes/index.md)
- [反射 (Visual Basic)](../reflection.md)
- [特性 (Visual Basic)](../../../language-reference/attributes.md)
- [创建自定义特性 (Visual Basic)](creating-custom-attributes.md)
- [使用反射访问特性 (Visual Basic)](accessing-attributes-by-using-reflection.md)
