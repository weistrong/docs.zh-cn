---
description: 了解有关以下内容的详细信息： BC42110：不会推断变量 "" 的类型， <variablename> 因为它绑定到封闭范围中的某个字段
title: 无法推断出变量“<variablename>”的类型，因为它绑定到封闭范围中的某个字段
ms.date: 07/20/2015
f1_keywords:
- vbc42110
- bc42110
helpviewer_keywords:
- BC42110
ms.assetid: ef4442eb-08d1-434f-a03b-4aa2ed4e4414
ms.openlocfilehash: db31f1a6e87a2fd133f095e2fbdde7bc6bded97e
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99641234"
---
# <a name="bc42110-the-type-for-variable-variablename-will-not-be-inferred-because-it-is-bound-to-a-field-in-an-enclosing-scope"></a><span data-ttu-id="75c93-103">BC42110：不会推断变量 "" 的类型， \<variablename> 因为它绑定到封闭范围中的某个字段</span><span class="sxs-lookup"><span data-stu-id="75c93-103">BC42110: The type for variable '\<variablename>' will not be inferred because it is bound to a field in an enclosing scope</span></span>

<span data-ttu-id="75c93-104">不会推断变量 "" 的类型， \<variablename> 因为它绑定到封闭范围中的某个字段。</span><span class="sxs-lookup"><span data-stu-id="75c93-104">The type for variable '\<variablename>' will not be inferred because it is bound to a field in an enclosing scope.</span></span> <span data-ttu-id="75c93-105">更改 "" 的名称 \<variablename> ，或使用完全限定名称 (例如 "variablename" 或 "variablename" ) 。</span><span class="sxs-lookup"><span data-stu-id="75c93-105">Either change the name of '\<variablename>', or use the fully qualified name (for example, 'Me.variablename' or 'MyBase.variablename').</span></span>

<span data-ttu-id="75c93-106">代码中的循环控制变量与类的字段或其他封闭范围的名称相同。</span><span class="sxs-lookup"><span data-stu-id="75c93-106">A loop control variable in your code has the same name as a field of the class or other enclosing scope.</span></span> <span data-ttu-id="75c93-107">因为在没有子句的情况下使用控制变量 `As` ，它将绑定到封闭范围中的字段，并且编译器不会为其创建新的变量，也不会推断其类型。</span><span class="sxs-lookup"><span data-stu-id="75c93-107">Because the control variable is used without an `As` clause, it is bound to the field in the enclosing scope, and the compiler does not create a new variable for it or infer its type.</span></span>

<span data-ttu-id="75c93-108">在下面的示例中， `Index` 语句中的控制变量 `For` 绑定到 `Index` 类中的字段 `Customer` 。</span><span class="sxs-lookup"><span data-stu-id="75c93-108">In the following example, `Index`, the control variable in the `For` statement, is bound to the `Index` field in the `Customer` class.</span></span> <span data-ttu-id="75c93-109">编译器不会为控件变量创建新的变量，也不会 `Index` 推断其类型。</span><span class="sxs-lookup"><span data-stu-id="75c93-109">The compiler does not create a new variable for the control variable `Index` or infer its type.</span></span>

```vb
Class Customer

    ' The class has a field named Index.
    Private Index As Integer

    Sub Main()

    ' The following line will raise this warning.
        For Index = 1 To 10
            ' ...
        Next

    End Sub
End Class
```

<span data-ttu-id="75c93-110">默认情况下，此消息是一个警告。</span><span class="sxs-lookup"><span data-stu-id="75c93-110">By default, this message is a warning.</span></span> <span data-ttu-id="75c93-111">有关如何隐藏警告或如何将警告视为错误的信息，请参见 [Configuring Warnings in Visual Basic](/visualstudio/ide/configuring-warnings-in-visual-basic)。</span><span class="sxs-lookup"><span data-stu-id="75c93-111">For information about how to hide warnings or how to treat warnings as errors, see [Configuring Warnings in Visual Basic](/visualstudio/ide/configuring-warnings-in-visual-basic).</span></span>

<span data-ttu-id="75c93-112">**错误 ID：** BC42110</span><span class="sxs-lookup"><span data-stu-id="75c93-112">**Error ID:** BC42110</span></span>

## <a name="to-address-this-warning"></a><span data-ttu-id="75c93-113">解决此警告</span><span class="sxs-lookup"><span data-stu-id="75c93-113">To address this warning</span></span>

- <span data-ttu-id="75c93-114">将循环控制变量的名称更改为不属于类的字段名称的标识符，使该循环控制变量成为局部变量。</span><span class="sxs-lookup"><span data-stu-id="75c93-114">Make the loop control variable local by changing its name to an identifier that is not also the name of a field of the class.</span></span>

  ```vb
  For I = 1 To 10
  ```

- <span data-ttu-id="75c93-115">阐明循环控制变量是通过 `Me.` 在变量名称的前面加上前缀来绑定到类字段。</span><span class="sxs-lookup"><span data-stu-id="75c93-115">Clarify that the loop control variable binds to the class field by prefixing `Me.` to the variable name.</span></span>

  ```vb
  For Me.Index = 1 To 10
  ```

- <span data-ttu-id="75c93-116">使用 `As` 子句来指定循环控制变量的类型，而不是依赖于局部类型推理。</span><span class="sxs-lookup"><span data-stu-id="75c93-116">Instead of relying on local type inference, use an `As` clause to specify a type for the loop control variable.</span></span>

  ```vb
  For Index As Integer = 1 To 10
  ```

## <a name="example"></a><span data-ttu-id="75c93-117">示例</span><span class="sxs-lookup"><span data-stu-id="75c93-117">Example</span></span>

 <span data-ttu-id="75c93-118">下面的代码显示了前面的示例，其中的第一个更正是就地的。</span><span class="sxs-lookup"><span data-stu-id="75c93-118">The following code shows the earlier example with the first correction in place.</span></span>

```vb
Class Customer

    ' The class has a field named Index.
    Private Index As Integer

    Sub Main()

        For I = 1 To 10
            ' ...
        Next

    End Sub
End Class
```

## <a name="see-also"></a><span data-ttu-id="75c93-119">请参阅</span><span class="sxs-lookup"><span data-stu-id="75c93-119">See also</span></span>

- [<span data-ttu-id="75c93-120">Option Infer 语句</span><span class="sxs-lookup"><span data-stu-id="75c93-120">Option Infer Statement</span></span>](../statements/option-infer-statement.md)
- [<span data-ttu-id="75c93-121">For Each...Next 语句</span><span class="sxs-lookup"><span data-stu-id="75c93-121">For Each...Next Statement</span></span>](../statements/for-each-next-statement.md)
- [<span data-ttu-id="75c93-122">For...Next 语句</span><span class="sxs-lookup"><span data-stu-id="75c93-122">For...Next Statement</span></span>](../statements/for-next-statement.md)
- [<span data-ttu-id="75c93-123">如何：引用对象的当前实例</span><span class="sxs-lookup"><span data-stu-id="75c93-123">How to: Refer to the Current Instance of an Object</span></span>](../../programming-guide/language-features/variables/how-to-refer-to-the-current-instance-of-an-object.md)
- [<span data-ttu-id="75c93-124">局部类型推理</span><span class="sxs-lookup"><span data-stu-id="75c93-124">Local Type Inference</span></span>](../../programming-guide/language-features/variables/local-type-inference.md)
- [<span data-ttu-id="75c93-125">Me、My、MyBase 和 MyClass</span><span class="sxs-lookup"><span data-stu-id="75c93-125">Me, My, MyBase, and MyClass</span></span>](../../programming-guide/program-structure/me-my-mybase-and-myclass.md)
