---
description: 了解详细信息： BC42326：不会从此事件处理程序中移除 Lambda 表达式
title: 将不会从此事件处理程序中移除 Lambda 表达式
ms.date: 07/20/2015
f1_keywords:
- bc42326
- vbc42326
helpviewer_keywords:
- BC42326
ms.assetid: 63214dc6-0112-4245-8ebf-7c9e8f5a5782
ms.openlocfilehash: 6feb8733a6413caa564d2c930b4d35dc5697b4fe
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99795945"
---
# <a name="bc42326-lambda-expression-will-not-be-removed-from-this-event-handler"></a><span data-ttu-id="4537a-103">BC42326：不会从此事件处理程序中移除 Lambda 表达式</span><span class="sxs-lookup"><span data-stu-id="4537a-103">BC42326: Lambda expression will not be removed from this event handler</span></span>

<span data-ttu-id="4537a-104">Lambda 表达式将不会从此事件处理程序中移除。</span><span class="sxs-lookup"><span data-stu-id="4537a-104">Lambda expression will not be removed from this event handler.</span></span> <span data-ttu-id="4537a-105">将 lambda 表达式分配给一个变量，并使用该变量添加和移除该事件。</span><span class="sxs-lookup"><span data-stu-id="4537a-105">Assign the lambda expression to a variable and use the variable to add and remove the event.</span></span>

<span data-ttu-id="4537a-106">当 lambda 表达式与事件处理程序一起使用时，可能看不到预期的行为。</span><span class="sxs-lookup"><span data-stu-id="4537a-106">When lambda expressions are used with event handlers, you may not see the behavior you expect.</span></span> <span data-ttu-id="4537a-107">编译器会为每个 lambda 表达式定义生成新的方法，即使它们相同也是如此。</span><span class="sxs-lookup"><span data-stu-id="4537a-107">The compiler generates a new method for each lambda expression definition, even if they are identical.</span></span> <span data-ttu-id="4537a-108">因此，会显示以下代码 `False` 。</span><span class="sxs-lookup"><span data-stu-id="4537a-108">Therefore, the following code displays `False`.</span></span>

```vb
Module Module1

    Sub Main()
        Dim fun1 As ChangeInteger = Function(p As Integer) p + 1
        Dim fun2 As ChangeInteger = Function(p As Integer) p + 1
        Console.WriteLine(fun1 = fun2)
    End Sub

    Delegate Function ChangeInteger(ByVal x As Integer) As Integer

End Module
```

<span data-ttu-id="4537a-109">当 lambda 表达式与事件处理程序一起使用时，这可能会导致意外的结果。</span><span class="sxs-lookup"><span data-stu-id="4537a-109">When lambda expressions are used with event handlers, this may cause unexpected results.</span></span> <span data-ttu-id="4537a-110">在下面的示例中，语句不删除由添加的 lambda 表达式 `AddHandler` `RemoveHandler` 。</span><span class="sxs-lookup"><span data-stu-id="4537a-110">In the following example, the lambda expression added by `AddHandler` is not removed by the `RemoveHandler` statement.</span></span>

```vb
Module Module1

    Event ProcessInteger(ByVal x As Integer)

    Sub Main()

        ' The following line adds one listener to the event.
        AddHandler ProcessInteger, Function(m As Integer) m

        ' The following statement searches the current listeners
        ' for a match to remove. However, this lambda is not the same
        ' as the previous one, so nothing is removed.
        RemoveHandler ProcessInteger, Function(m As Integer) m

    End Sub
End Module
```

<span data-ttu-id="4537a-111">默认情况下，此消息是一个警告。</span><span class="sxs-lookup"><span data-stu-id="4537a-111">By default, this message is a warning.</span></span> <span data-ttu-id="4537a-112">有关如何隐藏警告或将警告视为错误的详细信息，请参阅 [Configuring Warnings in Visual Basic](/visualstudio/ide/configuring-warnings-in-visual-basic)。</span><span class="sxs-lookup"><span data-stu-id="4537a-112">For more information about how to hide warnings or treat warnings as errors, see [Configuring Warnings in Visual Basic](/visualstudio/ide/configuring-warnings-in-visual-basic).</span></span>

<span data-ttu-id="4537a-113">**错误 ID：** BC42326</span><span class="sxs-lookup"><span data-stu-id="4537a-113">**Error ID:** BC42326</span></span>

## <a name="to-correct-this-error"></a><span data-ttu-id="4537a-114">更正此错误</span><span class="sxs-lookup"><span data-stu-id="4537a-114">To correct this error</span></span>

<span data-ttu-id="4537a-115">若要避免此警告并删除 lambda 表达式，请将 lambda 表达式分配给一个变量，并在和语句中使用该变量 `AddHandler` `RemoveHandler` ，如下面的示例中所示。</span><span class="sxs-lookup"><span data-stu-id="4537a-115">To avoid the warning and remove the lambda expression, assign the lambda expression to a variable and use the variable in both the `AddHandler` and `RemoveHandler` statements, as shown in the following example.</span></span>

```vb
Module Module1

    Event ProcessInteger(ByVal x As Integer)

    Dim PrintHandler As ProcessIntegerEventHandler

    Sub Main()

        ' Assign the lambda expression to a variable.
        PrintHandler = Function(m As Integer) m

        ' Use the variable to add the listener.
        AddHandler ProcessInteger, PrintHandler

        ' Use the variable again when you want to remove the listener.
        RemoveHandler ProcessInteger, PrintHandler

    End Sub
End Module
```

## <a name="see-also"></a><span data-ttu-id="4537a-116">请参阅</span><span class="sxs-lookup"><span data-stu-id="4537a-116">See also</span></span>

- [<span data-ttu-id="4537a-117">Lambda 表达式</span><span class="sxs-lookup"><span data-stu-id="4537a-117">Lambda Expressions</span></span>](../../programming-guide/language-features/procedures/lambda-expressions.md)
- [<span data-ttu-id="4537a-118">宽松委托转换</span><span class="sxs-lookup"><span data-stu-id="4537a-118">Relaxed Delegate Conversion</span></span>](../../programming-guide/language-features/delegates/relaxed-delegate-conversion.md)
- [<span data-ttu-id="4537a-119">事件</span><span class="sxs-lookup"><span data-stu-id="4537a-119">Events</span></span>](../../programming-guide/language-features/events/index.md)
