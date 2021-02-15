---
description: '了解详细信息：如何：查询字符串中的字符 (LINQ)  (Visual Basic) '
title: 如何：查询字符串中的字符 (LINQ)
ms.date: 07/20/2015
ms.assetid: 499ebbe0-746c-4235-9dba-ce722c12b50e
ms.openlocfilehash: bd8fabc06e88c83ae4e89079378ad67efb13c446
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100425745"
---
# <a name="how-to-query-for-characters-in-a-string-linq-visual-basic"></a><span data-ttu-id="d7a7f-103">如何：查询字符串中的字符 (LINQ)  (Visual Basic) </span><span class="sxs-lookup"><span data-stu-id="d7a7f-103">How to: Query for Characters in a String (LINQ) (Visual Basic)</span></span>

<span data-ttu-id="d7a7f-104">因为 <xref:System.String> 类可实现泛型 <xref:System.Collections.Generic.IEnumerable%601> 接口，因此任何字符串都可以字符序列的形式进行查询。</span><span class="sxs-lookup"><span data-stu-id="d7a7f-104">Because the <xref:System.String> class implements the generic <xref:System.Collections.Generic.IEnumerable%601> interface, any string can be queried as a sequence of characters.</span></span> <span data-ttu-id="d7a7f-105">但是，这不是 LINQ 的一般用法。</span><span class="sxs-lookup"><span data-stu-id="d7a7f-105">However, this is not a common use of LINQ.</span></span> <span data-ttu-id="d7a7f-106">对于复杂的模式匹配操作，请使用 <xref:System.Text.RegularExpressions.Regex> 类。</span><span class="sxs-lookup"><span data-stu-id="d7a7f-106">For complex pattern matching operations, use the <xref:System.Text.RegularExpressions.Regex> class.</span></span>

## <a name="example"></a><span data-ttu-id="d7a7f-107">示例</span><span class="sxs-lookup"><span data-stu-id="d7a7f-107">Example</span></span>

<span data-ttu-id="d7a7f-108">以下示例查询一个字符串以确定它所包含的数字数量。</span><span class="sxs-lookup"><span data-stu-id="d7a7f-108">The following example queries a string to determine the number of numeric digits it contains.</span></span> <span data-ttu-id="d7a7f-109">请注意，在第一次执行此查询后将“重用”此查询。</span><span class="sxs-lookup"><span data-stu-id="d7a7f-109">Note that the query is "reused" after it is executed the first time.</span></span> <span data-ttu-id="d7a7f-110">这是可能的，因为查询本身并不存储任何实际的结果。</span><span class="sxs-lookup"><span data-stu-id="d7a7f-110">This is possible because the query itself does not store any actual results.</span></span>

```vb
Class QueryAString

    Shared Sub Main()

        ' A string is an IEnumerable data source.
        Dim aString As String = "ABCDE99F-J74-12-89A"

        ' Select only those characters that are numbers
        Dim stringQuery = From ch In aString
                          Where Char.IsDigit(ch)
                          Select ch
        ' Execute the query
        For Each c As Char In stringQuery
            Console.Write(c & " ")
        Next

        ' Call the Count method on the existing query.
        Dim count As Integer = stringQuery.Count()
        Console.WriteLine(System.Environment.NewLine & "Count = " & count)

        ' Select all characters before the first '-'
        Dim stringQuery2 = aString.TakeWhile(Function(c) c <> "-")

        ' Execute the second query
        For Each ch In stringQuery2
            Console.Write(ch)
        Next

        Console.WriteLine(System.Environment.NewLine & "Press any key to exit")
        Console.ReadKey()
    End Sub
End Class
' Output:
' 9 9 7 4 1 2 8 9
' Count = 8
' ABCDE99F
```

## <a name="compile-the-code"></a><span data-ttu-id="d7a7f-111">编译代码</span><span class="sxs-lookup"><span data-stu-id="d7a7f-111">Compile the code</span></span>

<span data-ttu-id="d7a7f-112">使用 `Imports` System. Linq 命名空间的语句创建 Visual Basic 控制台应用程序项目。</span><span class="sxs-lookup"><span data-stu-id="d7a7f-112">Create a Visual Basic console application project, with an `Imports` statement for the System.Linq namespace.</span></span>

## <a name="see-also"></a><span data-ttu-id="d7a7f-113">请参阅</span><span class="sxs-lookup"><span data-stu-id="d7a7f-113">See also</span></span>

- [<span data-ttu-id="d7a7f-114">LINQ 和字符串 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="d7a7f-114">LINQ and Strings (Visual Basic)</span></span>](linq-and-strings.md)
- [<span data-ttu-id="d7a7f-115">如何将 LINQ 查询与正则表达式组合 (Visual Basic) </span><span class="sxs-lookup"><span data-stu-id="d7a7f-115">How to combine LINQ queries with regular expressions (Visual Basic)</span></span>](how-to-combine-linq-queries-with-regular-expressions.md)
