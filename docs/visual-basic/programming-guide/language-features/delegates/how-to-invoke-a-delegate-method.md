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
# <a name="how-to-invoke-a-delegate-method-visual-basic"></a><span data-ttu-id="d8eeb-103">如何：调用委托方法 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="d8eeb-103">How to: Invoke a Delegate Method (Visual Basic)</span></span>

<span data-ttu-id="d8eeb-104">此示例演示如何将方法与委托相关联，然后通过委托调用该方法。</span><span class="sxs-lookup"><span data-stu-id="d8eeb-104">This example shows how to associate a method with a delegate and then invoke that method through the delegate.</span></span>

### <a name="create-the-delegate-and-matching-procedures"></a><span data-ttu-id="d8eeb-105">创建委托和匹配过程</span><span class="sxs-lookup"><span data-stu-id="d8eeb-105">Create the delegate and matching procedures</span></span>

1. <span data-ttu-id="d8eeb-106">创建一个名为的委托 `MySubDelegate` 。</span><span class="sxs-lookup"><span data-stu-id="d8eeb-106">Create a delegate named `MySubDelegate`.</span></span>

    ```vb
    Delegate Sub MySubDelegate(ByVal x As Integer)
    ```

2. <span data-ttu-id="d8eeb-107">声明一个类，该类包含具有与委托相同的签名的方法。</span><span class="sxs-lookup"><span data-stu-id="d8eeb-107">Declare a class that contains a method with the same signature as the delegate.</span></span>

    ```vb
    Class class1
        Sub Sub1(ByVal x As Integer)
            MsgBox("The value of x is: " & CStr(x))
        End Sub
    End Class
    ```

3. <span data-ttu-id="d8eeb-108">定义一个方法，该方法通过调用内置方法来创建委托的实例并调用与该委托关联的方法 `Invoke` 。</span><span class="sxs-lookup"><span data-stu-id="d8eeb-108">Define a method that creates an instance of the delegate and invokes the method associated with the delegate by calling the built-in `Invoke` method.</span></span>

    ```vb
    Protected Sub DelegateTest()
        Dim c1 As New class1
        ' Create an instance of the delegate.
        Dim msd As MySubDelegate = AddressOf c1.Sub1
        ' Call the method.
        msd.Invoke(10)
    End Sub
    ```

## <a name="see-also"></a><span data-ttu-id="d8eeb-109">请参阅</span><span class="sxs-lookup"><span data-stu-id="d8eeb-109">See also</span></span>

- [<span data-ttu-id="d8eeb-110">Delegate 语句</span><span class="sxs-lookup"><span data-stu-id="d8eeb-110">Delegate Statement</span></span>](../../../language-reference/statements/delegate-statement.md)
- [<span data-ttu-id="d8eeb-111">委托</span><span class="sxs-lookup"><span data-stu-id="d8eeb-111">Delegates</span></span>](index.md)
- [<span data-ttu-id="d8eeb-112">事件</span><span class="sxs-lookup"><span data-stu-id="d8eeb-112">Events</span></span>](../events/index.md)
- [<span data-ttu-id="d8eeb-113">多线程应用程序</span><span class="sxs-lookup"><span data-stu-id="d8eeb-113">Multithreaded Applications</span></span>](../../../../standard/threading/using-threads-and-threading.md)
