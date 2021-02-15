---
description: '了解有关详细信息，请参阅如何：调用委托方法 (Visual Basic) '
title: 如何：调用委托方法
ms.date: 07/20/2015
ms.assetid: b56866ae-abf9-4a5a-a855-486359455e9c
ms.openlocfilehash: c5c20048969f2fef16b8b7f65e84a094a3f1cf9f
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100434467"
---
# <a name="how-to-invoke-a-delegate-method-visual-basic"></a>如何：调用委托方法 (Visual Basic)

此示例演示如何将方法与委托相关联，然后通过委托调用该方法。

### <a name="create-the-delegate-and-matching-procedures"></a>创建委托和匹配过程

1. 创建一个名为的委托 `MySubDelegate` 。

    ```vb
    Delegate Sub MySubDelegate(ByVal x As Integer)
    ```

2. 声明一个类，该类包含具有与委托相同的签名的方法。

    ```vb
    Class class1
        Sub Sub1(ByVal x As Integer)
            MsgBox("The value of x is: " & CStr(x))
        End Sub
    End Class
    ```

3. 定义一个方法，该方法通过调用内置方法来创建委托的实例并调用与该委托关联的方法 `Invoke` 。

    ```vb
    Protected Sub DelegateTest()
        Dim c1 As New class1
        ' Create an instance of the delegate.
        Dim msd As MySubDelegate = AddressOf c1.Sub1
        ' Call the method.
        msd.Invoke(10)
    End Sub
    ```

## <a name="see-also"></a>请参阅

- [Delegate 语句](../../../language-reference/statements/delegate-statement.md)
- [委托](index.md)
- [事件](../events/index.md)
- [多线程应用程序](../../../../standard/threading/using-threads-and-threading.md)
