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
# <a name="how-to-sort-or-filter-text-data-by-any-word-or-field-linq-visual-basic"></a>如何：按任意词或字段对文本数据进行排序或筛选 (LINQ) (Visual Basic)

下面的示例演示如何按行中的任何字段对结构化文本（如以逗号分隔的值）行进行排序。 可以在运行时动态指定字段。 假定 scores.csv 中的字段表示学生的 ID 号，后跟一系列四个测试分数。

### <a name="to-create-a-file-that-contains-data"></a>创建包含数据的文件

从主题 " [如何：从不同文件中联接内容" (LINQ)  (Visual Basic ](how-to-join-content-from-dissimilar-files-linq.md)) 中复制 scores.csv 的数据，并将其保存到解决方案文件夹中。

## <a name="example"></a>示例

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

此示例还演示如何从函数返回查询变量。

## <a name="compile-the-code"></a>编译代码

使用 `Imports` System. Linq 命名空间的语句创建 Visual Basic 控制台应用程序项目。

## <a name="see-also"></a>请参阅

- [LINQ 和字符串 (Visual Basic)](linq-and-strings.md)
