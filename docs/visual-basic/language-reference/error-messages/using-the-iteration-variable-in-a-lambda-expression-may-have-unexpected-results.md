---
description: 了解详细信息： BC42324：在 lambda 表达式中使用迭代变量可能会产生意外的结果
title: 在 lambda 表达式中使用迭代变量可能会产生意外的结果
ms.date: 07/20/2015
f1_keywords:
- vbc42324
- bc42324
helpviewer_keywords:
- BC42324
ms.assetid: b5c2c4bd-3b2a-4a73-aaeb-55728eb03b68
ms.openlocfilehash: a21e33c9a8737642d4d0764e92b1fbb2213f9602
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99640870"
---
# <a name="bc42324-using-the-iteration-variable-in-a-lambda-expression-may-have-unexpected-results"></a><span data-ttu-id="f115f-103">BC42324：在 lambda 表达式中使用迭代变量可能会产生意外的结果</span><span class="sxs-lookup"><span data-stu-id="f115f-103">BC42324: Using the iteration variable in a lambda expression may have unexpected results</span></span>

<span data-ttu-id="f115f-104">在 lambda 表达式中使用迭代变量可能会产生意外的结果。</span><span class="sxs-lookup"><span data-stu-id="f115f-104">Using the iteration variable in a lambda expression may have unexpected results.</span></span> <span data-ttu-id="f115f-105">改为在循环内创建一个局部变量，并为其分配迭代变量的值。</span><span class="sxs-lookup"><span data-stu-id="f115f-105">Instead, create a local variable within the loop and assign it the value of the iteration variable.</span></span>

 <span data-ttu-id="f115f-106">如果在循环中声明的 lambda 表达式中使用循环迭代变量，则会出现此警告。</span><span class="sxs-lookup"><span data-stu-id="f115f-106">This warning appears when you use a loop iteration variable in a lambda expression that is declared inside the loop.</span></span> <span data-ttu-id="f115f-107">例如，下面的示例将导致出现警告。</span><span class="sxs-lookup"><span data-stu-id="f115f-107">For example, the following example causes the warning to appear.</span></span>

```vb
For i As Integer = 1 To 10
    ' The warning is given for the use of i.
    Dim exampleFunc As Func(Of Integer) = Function() i
Next
```

 <span data-ttu-id="f115f-108">下面的示例显示了可能出现的意外结果。</span><span class="sxs-lookup"><span data-stu-id="f115f-108">The following example shows the unexpected results that might occur.</span></span>

```vb
Module Module1
    Sub Main()
        Dim array1 As Func(Of Integer)() = New Func(Of Integer)(4) {}

        For i As Integer = 0 To 4
            array1(i) = Function() i
        Next

        For Each funcElement In array1
            System.Console.WriteLine(funcElement())
        Next

    End Sub
End Module
```

 <span data-ttu-id="f115f-109">`For`循环创建 lambda 表达式的数组，其中每个表达式都返回循环迭代变量的值 `i` 。</span><span class="sxs-lookup"><span data-stu-id="f115f-109">The `For` loop creates an array of lambda expressions, each of which returns the value of the loop iteration variable `i`.</span></span> <span data-ttu-id="f115f-110">当在循环中计算 lambda 表达式时 `For Each` ，可能会发现在循环中显示0、1、2、3和4的后续值 `i` `For` 。</span><span class="sxs-lookup"><span data-stu-id="f115f-110">When the lambda expressions are evaluated in the `For Each` loop, you might expect to see 0, 1, 2, 3, and 4 displayed, the successive values of `i` in the `For` loop.</span></span> <span data-ttu-id="f115f-111">相反，您将看到显示的五次的最终值 `i` ：</span><span class="sxs-lookup"><span data-stu-id="f115f-111">Instead, you see the final value of `i` displayed five times:</span></span>

 `5`

 `5`

 `5`

 `5`

 `5`

 <span data-ttu-id="f115f-112">默认情况下，此消息是一个警告。</span><span class="sxs-lookup"><span data-stu-id="f115f-112">By default, this message is a warning.</span></span> <span data-ttu-id="f115f-113">有关隐藏警告或将警告视为错误的详细信息，请参阅 [Configuring Warnings in Visual Basic](/visualstudio/ide/configuring-warnings-in-visual-basic)。</span><span class="sxs-lookup"><span data-stu-id="f115f-113">For more information about hiding warnings or treating warnings as errors, see [Configuring Warnings in Visual Basic](/visualstudio/ide/configuring-warnings-in-visual-basic).</span></span>

 <span data-ttu-id="f115f-114">**错误 ID：** BC42324</span><span class="sxs-lookup"><span data-stu-id="f115f-114">**Error ID:** BC42324</span></span>

## <a name="to-correct-this-error"></a><span data-ttu-id="f115f-115">更正此错误</span><span class="sxs-lookup"><span data-stu-id="f115f-115">To correct this error</span></span>

- <span data-ttu-id="f115f-116">将迭代变量的值分配给局部变量，并在 lambda 表达式中使用该局部变量。</span><span class="sxs-lookup"><span data-stu-id="f115f-116">Assign the value of the iteration variable to a local variable, and use the local variable in the lambda expression.</span></span>

```vb
Module Module1
    Sub Main()
        Dim array1 As Func(Of Integer)() = New Func(Of Integer)(4) {}

        For i As Integer = 0 To 4
            Dim j = i
            array1(i) = Function() j
        Next

        For Each funcElement In array1
            System.Console.WriteLine(funcElement())
        Next

    End Sub
End Module
```

## <a name="see-also"></a><span data-ttu-id="f115f-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="f115f-117">See also</span></span>

- [<span data-ttu-id="f115f-118">Lambda 表达式</span><span class="sxs-lookup"><span data-stu-id="f115f-118">Lambda Expressions</span></span>](../../programming-guide/language-features/procedures/lambda-expressions.md)
