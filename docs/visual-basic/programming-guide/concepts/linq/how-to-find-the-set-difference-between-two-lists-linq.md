---
description: '了解有关详细信息，请参阅如何：查找两个列表之间的差集 (LINQ)  (Visual Basic) '
title: 如何：查找两个列表之间的差集 (LINQ)
ms.date: 07/20/2015
ms.assetid: b5b25474-10a8-4df6-aab5-75621bb6b68e
ms.openlocfilehash: c877be03c3ff82d4be4814035a6401385d907e60
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100483685"
---
# <a name="how-to-find-the-set-difference-between-two-lists-linq-visual-basic"></a><span data-ttu-id="24e3e-103">如何：查找两个列表之间的差集 (LINQ)  (Visual Basic) </span><span class="sxs-lookup"><span data-stu-id="24e3e-103">How to: Find the Set Difference Between Two Lists (LINQ) (Visual Basic)</span></span>

<span data-ttu-id="24e3e-104">此示例演示如何使用 LINQ 对两个字符串列表进行比较，并输出那些位于 names1.txt 中但不在 names2.txt 中的行。</span><span class="sxs-lookup"><span data-stu-id="24e3e-104">This example shows how to use LINQ to compare two lists of strings and output those lines that are in names1.txt but not in names2.txt.</span></span>  
  
### <a name="to-create-the-data-files"></a><span data-ttu-id="24e3e-105">创建数据文件</span><span class="sxs-lookup"><span data-stu-id="24e3e-105">To create the data files</span></span>  
  
1. <span data-ttu-id="24e3e-106">将 names1.txt 和 names2.txt 复制到解决方案文件夹中，如 [如何：结合和比较字符串集合 (LINQ)  (Visual Basic ](how-to-combine-and-compare-string-collections-linq.md)) 。</span><span class="sxs-lookup"><span data-stu-id="24e3e-106">Copy names1.txt and names2.txt to your solution folder as shown in [How to: Combine and Compare String Collections (LINQ) (Visual Basic)](how-to-combine-and-compare-string-collections-linq.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="24e3e-107">示例</span><span class="sxs-lookup"><span data-stu-id="24e3e-107">Example</span></span>  
  
```vb  
Class CompareLists  
  
    Shared Sub Main()  
  
        ' Create the IEnumerable data sources.  
        Dim names1 As String() = System.IO.File.ReadAllLines("../../../names1.txt")  
        Dim names2 As String() = System.IO.File.ReadAllLines("../../../names2.txt")  
  
        ' Create the query. Note that method syntax must be used here.  
        Dim differenceQuery = names1.Except(names2)  
        Console.WriteLine("The following lines are in names1.txt but not names2.txt")  
  
        ' Execute the query.  
        For Each name As String In differenceQuery  
            Console.WriteLine(name)  
        Next  
  
        ' Keep console window open in debug mode.  
        Console.WriteLine("Press any key to exit.")  
        Console.ReadKey()  
    End Sub  
End Class  
' Output:  
' The following lines are in names1.txt but not names2.txt  
' Potra, Cristina  
' Noriega, Fabricio  
' Aw, Kam Foo  
' Toyoshima, Tim  
' Guy, Wey Yuan  
' Garcia, Debra  
```  
  
 <span data-ttu-id="24e3e-108">Visual Basic 中的某些类型的查询操作（例如 <xref:System.Linq.Enumerable.Except%2A> 、 <xref:System.Linq.Enumerable.Distinct%2A> 、 <xref:System.Linq.Enumerable.Union%2A> 和 <xref:System.Linq.Enumerable.Concat%2A> ）只能用基于方法的语法表示。</span><span class="sxs-lookup"><span data-stu-id="24e3e-108">Some types of query operations in Visual Basic, such as <xref:System.Linq.Enumerable.Except%2A>, <xref:System.Linq.Enumerable.Distinct%2A>, <xref:System.Linq.Enumerable.Union%2A>, and <xref:System.Linq.Enumerable.Concat%2A>, can only be expressed in method-based syntax.</span></span>  
  
## <a name="compile-the-code"></a><span data-ttu-id="24e3e-109">编译代码</span><span class="sxs-lookup"><span data-stu-id="24e3e-109">Compile the code</span></span>  

<span data-ttu-id="24e3e-110">使用 `Imports` System. Linq 命名空间的语句创建 Visual Basic 控制台应用程序项目。</span><span class="sxs-lookup"><span data-stu-id="24e3e-110">Create a Visual Basic console application project, with an `Imports` statement for the System.Linq namespace.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="24e3e-111">请参阅</span><span class="sxs-lookup"><span data-stu-id="24e3e-111">See also</span></span>

- [<span data-ttu-id="24e3e-112">LINQ 和字符串 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="24e3e-112">LINQ and Strings (Visual Basic)</span></span>](linq-and-strings.md)
