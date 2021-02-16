---
description: '了解有关详细信息，请参阅如何：按任意词或字段对文本数据进行排序或筛选 (LINQ)  (Visual Basic) '
title: 如何：按任意词或字段对文本数据进行排序或筛选 (LINQ)
ms.date: 07/20/2015
ms.assetid: 9df137fe-335b-46e0-aecf-ea8a9eddd4e3
ms.openlocfilehash: 49fff8df58b41acf7c8a63b94e8d1c85eefec8ab
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100434922"
---
# <a name="how-to-sort-or-filter-text-data-by-any-word-or-field-linq-visual-basic"></a><span data-ttu-id="fe7cd-103">如何：按任意词或字段对文本数据进行排序或筛选 (LINQ) (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="fe7cd-103">How to: Sort or Filter Text Data by Any Word or Field (LINQ) (Visual Basic)</span></span>

<span data-ttu-id="fe7cd-104">下面的示例演示如何按行中的任何字段对结构化文本（如以逗号分隔的值）行进行排序。</span><span class="sxs-lookup"><span data-stu-id="fe7cd-104">The following example shows how to sort lines of structured text, such as comma-separated values, by any field in the line.</span></span> <span data-ttu-id="fe7cd-105">可以在运行时动态指定字段。</span><span class="sxs-lookup"><span data-stu-id="fe7cd-105">The field may be dynamically specified at runtime.</span></span> <span data-ttu-id="fe7cd-106">假定 scores.csv 中的字段表示学生的 ID 号，后跟一系列四个测试分数。</span><span class="sxs-lookup"><span data-stu-id="fe7cd-106">Assume that the fields in scores.csv represent a student's ID number, followed by a series of four test scores.</span></span>

### <a name="to-create-a-file-that-contains-data"></a><span data-ttu-id="fe7cd-107">创建包含数据的文件</span><span class="sxs-lookup"><span data-stu-id="fe7cd-107">To create a file that contains data</span></span>

<span data-ttu-id="fe7cd-108">从主题 " [如何：从不同文件中联接内容" (LINQ)  (Visual Basic ](how-to-join-content-from-dissimilar-files-linq.md)) 中复制 scores.csv 的数据，并将其保存到解决方案文件夹中。</span><span class="sxs-lookup"><span data-stu-id="fe7cd-108">Copy the scores.csv data from the topic [How to: Join Content from Dissimilar Files (LINQ) (Visual Basic)](how-to-join-content-from-dissimilar-files-linq.md) and save it to your solution folder.</span></span>

## <a name="example"></a><span data-ttu-id="fe7cd-109">示例</span><span class="sxs-lookup"><span data-stu-id="fe7cd-109">Example</span></span>

```vb
Class SortLines

    Shared Sub Main()
        Dim scores As String() = System.IO.File.ReadAllLines("../../../scores.csv")

        ' Change this to any value from 0 to 4
        Dim sortField As Integer = 1

        Console.WriteLine("Sorted highest to lowest by field " & sortField)

        ' Demonstrates how to return query from a method.
        ' The query is executed here.
        For Each str As String In SortQuery(scores, sortField)
            Console.WriteLine(str)
        Next

        ' Keep console window open in debug mode.
        Console.WriteLine("Press any key to exit.")
        Console.ReadKey()

    End Sub

    Shared Function SortQuery(
        ByVal source As IEnumerable(Of String),
        ByVal num As Integer) As IEnumerable(Of String)

        Dim scoreQuery = From line In source
                         Let fields = line.Split(New Char() {","})
                         Order By fields(num) Descending
                         Select line

        Return scoreQuery
    End Function
End Class
' Output:
' Sorted highest to lowest by field 1
' 116, 99, 86, 90, 94
' 120, 99, 82, 81, 79
' 111, 97, 92, 81, 60
' 114, 97, 89, 85, 82
' 121, 96, 85, 91, 60
' 122, 94, 92, 91, 91
' 117, 93, 92, 80, 87
' 118, 92, 90, 83, 78
' 113, 88, 94, 65, 91
' 112, 75, 84, 91, 39
' 119, 68, 79, 88, 92
' 115, 35, 72, 91, 70
```

<span data-ttu-id="fe7cd-110">此示例还演示如何从函数返回查询变量。</span><span class="sxs-lookup"><span data-stu-id="fe7cd-110">This example also demonstrates how to return a query variable from a Function.</span></span>

## <a name="compile-the-code"></a><span data-ttu-id="fe7cd-111">编译代码</span><span class="sxs-lookup"><span data-stu-id="fe7cd-111">Compile the code</span></span>

<span data-ttu-id="fe7cd-112">使用 `Imports` System. Linq 命名空间的语句创建 Visual Basic 控制台应用程序项目。</span><span class="sxs-lookup"><span data-stu-id="fe7cd-112">Create a Visual Basic console application project, with an `Imports` statement for the System.Linq namespace.</span></span>

## <a name="see-also"></a><span data-ttu-id="fe7cd-113">请参阅</span><span class="sxs-lookup"><span data-stu-id="fe7cd-113">See also</span></span>

- [<span data-ttu-id="fe7cd-114">LINQ 和字符串 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="fe7cd-114">LINQ and Strings (Visual Basic)</span></span>](linq-and-strings.md)
