---
description: 了解更多相关信息： BC30686：默认属性访问在 <defaultpropertyname> 接口 "" 的继承接口成员 "" <interfacename1> 和接口 "" <defaultpropertyname> 的 "" 之间不明确<interfacename2>
title: 默认属性访问在接口“<defaultpropertyname>”的继承接口成员“<interfacename1>”和接口“<defaultpropertyname>”的“<interfacename2>”之间不明确
ms.date: 07/20/2015
f1_keywords:
- vbc30686
- bc30686
helpviewer_keywords:
- BC30686
ms.assetid: 784fefec-ef57-48cf-b960-957df419b439
ms.openlocfilehash: 5ae5e5b2dc7a61540e26d125e960d4755141d975
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99796647"
---
# <a name="bc30686-default-property-access-is-ambiguous-between-the-inherited-interface-members-defaultpropertyname-of-interface-interfacename1-and-defaultpropertyname-of-interface-interfacename2"></a>BC30686：默认属性访问在接口 "" 的继承接口成员 "" \<defaultpropertyname> \<interfacename1> 和 \<defaultpropertyname> 接口 "" 的 " \<interfacename2> " 之间不明确

接口继承自两个接口，每个接口都声明一个具有相同名称的默认属性。 编译器无法解析对此默认属性的访问，无需进行限定。 下面的示例阐释了这一点。

```vb
Public Interface Iface1
    Default Property prop(ByVal arg As Integer) As Integer
End Interface
Public Interface Iface2
    Default Property prop(ByVal arg As Integer) As Integer
End Interface
Public Interface Iface3
    Inherits Iface1, Iface2
End Interface
Public Class testClass
    Public Sub accessDefaultProperty()
        Dim testObj As Iface3
        Dim testInt As Integer = testObj(1)
    End Sub
End Class
```

指定时 `testObj(1)` ，编译器会尝试将其解析为默认属性。 不过，由于继承了接口，有两个可能的默认属性，因此编译器会发出此错误信号。

**错误 ID：** BC30686

## <a name="to-correct-this-error"></a>更正此错误

- 避免继承任何具有相同名称的成员。 在前面的示例中，如果 `testObj` 不需要的任何成员（例如），请按 `Iface2` 如下所示声明：

  ```vb
  Dim testObj As Iface1
  ```

  \- 或 -

- 在类中实现继承接口。 然后，可以用不同的名称实现每个继承的属性。 但是，其中只有一个可以是实现类的默认属性。 下面的示例阐释了这一点。

  ```vb
  Public Class useIface3
      Implements Iface3
      Default Public Property prop1(ByVal arg As Integer) As Integer Implements Iface1.prop
          ' Insert code to define Get and Set procedures for prop1.
      End Property
      Public Property prop2(ByVal arg As Integer) As Integer Implements Iface2.prop
          ' Insert code to define Get and Set procedures for prop2.
      End Property
  End Class
  ```

## <a name="see-also"></a>请参阅

- [接口](../../programming-guide/language-features/interfaces/index.md)
