---
description: '了解详细信息：如何：调用扩展方法 (Visual Basic) '
title: 如何：调用扩展方法
ms.date: 07/20/2015
helpviewer_keywords:
- calling extension methods [Visual Basic]
- extension methods [Visual Basic]
ms.assetid: df07750f-40f4-4c07-a79e-1113a27cfbea
ms.openlocfilehash: ec5217526eb0cb28d172ab917df08a8bfe87fe95
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100471378"
---
# <a name="how-to-call-an-extension-method-visual-basic"></a><span data-ttu-id="b92d6-103">如何：调用扩展方法 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="b92d6-103">How to: Call an Extension Method (Visual Basic)</span></span>

<span data-ttu-id="b92d6-104">扩展方法使你能够向现有类添加方法。</span><span class="sxs-lookup"><span data-stu-id="b92d6-104">Extension methods enable you to add methods to an existing class.</span></span> <span data-ttu-id="b92d6-105">在扩展方法被声明并引入作用域后，可以像它所扩展的类型的实例方法一样调用它。</span><span class="sxs-lookup"><span data-stu-id="b92d6-105">After an extension method is declared and brought into scope, you can call it like an instance method of the type that it extends.</span></span> <span data-ttu-id="b92d6-106">有关如何编写扩展方法的详细信息，请参阅 [如何：编写扩展方法](./how-to-write-an-extension-method.md)。</span><span class="sxs-lookup"><span data-stu-id="b92d6-106">For more information about how to write an extension method, see [How to: Write an Extension Method](./how-to-write-an-extension-method.md).</span></span>

 <span data-ttu-id="b92d6-107">下面的说明引用 extension 方法 `PrintAndPunctuate` ，该方法将显示调用它的字符串实例，然后在中为第二个参数发送任何值 `punc` 。</span><span class="sxs-lookup"><span data-stu-id="b92d6-107">The following instructions refer to extension method `PrintAndPunctuate`, which will display the string instance that invokes it, followed by whatever value is sent in for the second parameter, `punc`.</span></span>

```vb
Imports System.Runtime.CompilerServices

Module StringExtensions
    <Extension()>
    Public Sub PrintAndPunctuate(ByVal aString As String,
                                 ByVal punc As String)
        Console.WriteLine(aString & punc)
    End Sub

End Module
```

<span data-ttu-id="b92d6-108">调用方法时，该方法必须在范围内。</span><span class="sxs-lookup"><span data-stu-id="b92d6-108">The method must be in scope when it is called.</span></span>

### <a name="to-call-an-extension-method"></a><span data-ttu-id="b92d6-109">调用扩展方法</span><span class="sxs-lookup"><span data-stu-id="b92d6-109">To call an extension method</span></span>

1. <span data-ttu-id="b92d6-110">声明一个变量，该变量的数据类型为扩展方法的第一个参数。</span><span class="sxs-lookup"><span data-stu-id="b92d6-110">Declare a variable that has the data type of the first parameter of the extension method.</span></span> <span data-ttu-id="b92d6-111">对于 `PrintAndPunctuate` ，需要一个 <xref:System.String> 变量：</span><span class="sxs-lookup"><span data-stu-id="b92d6-111">For `PrintAndPunctuate`, you need a <xref:System.String> variable:</span></span>

    ```vb
    Dim example = "Ready"
    ```

2. <span data-ttu-id="b92d6-112">该变量将调用扩展方法，并且其值绑定到第一个参数 `aString` 。</span><span class="sxs-lookup"><span data-stu-id="b92d6-112">That variable will invoke the extension method, and its value is bound to the first parameter, `aString`.</span></span> <span data-ttu-id="b92d6-113">将显示下面的调用语句 `Ready?` 。</span><span class="sxs-lookup"><span data-stu-id="b92d6-113">The following calling statement will display `Ready?`.</span></span>

    ```vb
    example.PrintAndPunctuate("?")
    ```

     <span data-ttu-id="b92d6-114">请注意，对此扩展方法的调用看起来就像调用 <xref:System.String> 需要一个参数的任何一个实例方法：</span><span class="sxs-lookup"><span data-stu-id="b92d6-114">Notice that the call to this extension method looks just like a call to any one of the <xref:System.String> instance methods that require one parameter:</span></span>

    ```vb
    example.EndsWith("dy")
    example.IndexOf("R")
    ```

3. <span data-ttu-id="b92d6-115">声明另一个字符串变量并再次调用方法，以查看它是否适用于任何字符串。</span><span class="sxs-lookup"><span data-stu-id="b92d6-115">Declare another string variable and call the method again to see that it works with any string.</span></span>

    ```vb
    Dim example2 = " or not"
    example2.PrintAndPunctuate("!!!")
    ```

     <span data-ttu-id="b92d6-116">此时间的结果为： `or not!!!` 。</span><span class="sxs-lookup"><span data-stu-id="b92d6-116">The result this time is: `or not!!!`.</span></span>

## <a name="example"></a><span data-ttu-id="b92d6-117">示例</span><span class="sxs-lookup"><span data-stu-id="b92d6-117">Example</span></span>

 <span data-ttu-id="b92d6-118">下面的代码是创建和使用简单扩展方法的完整示例。</span><span class="sxs-lookup"><span data-stu-id="b92d6-118">The following code is a complete example of the creation and use of a simple extension method.</span></span>

```vb
Imports System.Runtime.CompilerServices
Imports ConsoleApplication1.StringExtensions

Module Module1

    Sub Main()

        Dim example = "Hello"
        example.PrintAndPunctuate(".")
        example.PrintAndPunctuate("!!!!")

        Dim example2 = "Goodbye"
        example2.PrintAndPunctuate("?")
    End Sub

    <Extension()>
    Public Sub PrintAndPunctuate(ByVal aString As String,
                                 ByVal punc As String)
        Console.WriteLine(aString & punc)
    End Sub
End Module

' Output:
' Hello.
' Hello!!!!
' Goodbye?
```

## <a name="see-also"></a><span data-ttu-id="b92d6-119">请参阅</span><span class="sxs-lookup"><span data-stu-id="b92d6-119">See also</span></span>

- [<span data-ttu-id="b92d6-120">如何：编写扩展方法</span><span class="sxs-lookup"><span data-stu-id="b92d6-120">How to: Write an Extension Method</span></span>](./how-to-write-an-extension-method.md)
- [<span data-ttu-id="b92d6-121">扩展方法</span><span class="sxs-lookup"><span data-stu-id="b92d6-121">Extension Methods</span></span>](./extension-methods.md)
- [<span data-ttu-id="b92d6-122">Visual Basic 中的范围</span><span class="sxs-lookup"><span data-stu-id="b92d6-122">Scope in Visual Basic</span></span>](../declared-elements/scope.md)
