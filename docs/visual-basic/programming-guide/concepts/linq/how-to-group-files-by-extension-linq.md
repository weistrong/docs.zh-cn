---
description: '了解有关详细信息，请参阅如何：按扩展名对文件分组 (LINQ)  (Visual Basic) '
title: 如何：按扩展名对文件进行分组 (LINQ)
ms.date: 07/20/2015
ms.assetid: 904dc6d7-7162-4655-a7f4-5785d669bc5a
ms.openlocfilehash: 6736b4ff99d88f8e5b2b40aeb670d88589db02b1
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100472990"
---
# <a name="how-to-group-files-by-extension-linq-visual-basic"></a><span data-ttu-id="4369c-103">如何：按扩展名对文件进行分组 (LINQ)  (Visual Basic) </span><span class="sxs-lookup"><span data-stu-id="4369c-103">How to: Group Files by Extension (LINQ) (Visual Basic)</span></span>

<span data-ttu-id="4369c-104">本示例演示如何使用 LINQ 来执行高级分组和对文件或文件夹列表执行排序操作。</span><span class="sxs-lookup"><span data-stu-id="4369c-104">This example shows how LINQ can be used to perform advanced grouping and sorting operations on lists of files or folders.</span></span> <span data-ttu-id="4369c-105">它还演示如何使用 <xref:System.Linq.Enumerable.Skip%2A> 和 <xref:System.Linq.Enumerable.Take%2A> 方法在控制台窗口中对输出进行分页。</span><span class="sxs-lookup"><span data-stu-id="4369c-105">It also shows how to page output in the console window by using the <xref:System.Linq.Enumerable.Skip%2A> and <xref:System.Linq.Enumerable.Take%2A> methods.</span></span>  
  
## <a name="example"></a><span data-ttu-id="4369c-106">示例</span><span class="sxs-lookup"><span data-stu-id="4369c-106">Example</span></span>  

 <span data-ttu-id="4369c-107">下面的查询演示如何按文件扩展名对指定的目录树的内容进行分组。</span><span class="sxs-lookup"><span data-stu-id="4369c-107">The following query shows how to group the contents of a specified directory tree by the file name extension.</span></span>  
  
```vb  
Module GroupByExtension  
    Public Sub Main()  
  
        ' Root folder to query, along with all subfolders.  
        Dim startFolder As String = "C:\program files\Microsoft Visual Studio 9.0\VB\"  
  
        ' Used in WriteLine() to skip over startfolder in output lines.  
        Dim rootLength As Integer = startFolder.Length  
  
        'Take a snapshot of the folder contents  
        Dim dir As New System.IO.DirectoryInfo(startFolder)  
        Dim fileList = dir.GetFiles("*.*", System.IO.SearchOption.AllDirectories)  
  
        ' Create the query.  
        Dim queryGroupByExt = From file In fileList _  
                          Group By file.Extension.ToLower() Into fileGroup = Group _  
                          Order By ToLower _  
                          Select fileGroup  
  
        ' Execute the query. By storing the result we can  
        ' page the display with good performance.  
        Dim groupByExtList = queryGroupByExt.ToList()  
  
        ' Display one group at a time. If the number of
        ' entries is greater than the number of lines  
        ' in the console window, then page the output.  
        Dim trimLength = startFolder.Length  
        PageOutput(groupByExtList, trimLength)  
  
    End Sub  
  
    ' Pages console display for large query results. No more than one group per page.  
    ' This sub specifically works with group queries of FileInfo objects  
    ' but can be modified for any type.  
    Sub PageOutput(ByVal groupQuery, ByVal charsToSkip)  
  
        ' "3" = 1 line for extension key + 1 for "Press any key" + 1 for input cursor.  
        Dim numLines As Integer = Console.WindowHeight - 3  
        ' Flag to indicate whether there are more results to display  
        Dim goAgain As Boolean = True  
  
        For Each fg As IEnumerable(Of System.IO.FileInfo) In groupQuery  
            ' Start a new extension at the top of a page.  
            Dim currentLine As Integer = 0  
  
            Do While (currentLine < fg.Count())  
                Console.Clear()  
                Console.WriteLine(fg(0).Extension)  
  
                ' Get the next page of results  
                ' No more than one filename per page  
                Dim resultPage = From file In fg _  
                                Skip currentLine Take numLines  
  
                ' Execute the query. Trim the display output.  
                For Each line In resultPage  
                    Console.WriteLine(vbTab & line.FullName.Substring(charsToSkip))  
                Next  
  
                ' Advance the current position  
                currentLine = numLines + currentLine  
  
                ' Give the user a chance to break out of the loop  
                Console.WriteLine("Press any key for next page or the 'End' key to exit.")  
                Dim key As ConsoleKey = Console.ReadKey().Key  
                If key = ConsoleKey.End Then  
                    goAgain = False  
                    Exit For  
                End If  
            Loop  
        Next  
    End Sub  
End Module  
```  
  
 <span data-ttu-id="4369c-108">此程序的输出可能很长，具体取决于本地文件系统的详细信息和 `startFolder` 的设置。</span><span class="sxs-lookup"><span data-stu-id="4369c-108">The output from this program can be long, depending on the details of the local file system and what the `startFolder` is set to.</span></span> <span data-ttu-id="4369c-109">为了能够查看所有结果，此示例演示如何对结果进行分页。</span><span class="sxs-lookup"><span data-stu-id="4369c-109">To enable viewing of all results, this example shows how to page through results.</span></span> <span data-ttu-id="4369c-110">相同的方法适用于 Windows 和 Web 应用程序。</span><span class="sxs-lookup"><span data-stu-id="4369c-110">The same techniques can be applied to Windows and Web applications.</span></span> <span data-ttu-id="4369c-111">请注意，由于代码对组中的项进行分页，因此需要使用 `For Each` 循环。</span><span class="sxs-lookup"><span data-stu-id="4369c-111">Notice that because the code pages the items in a group, a nested `For Each` loop is required.</span></span> <span data-ttu-id="4369c-112">此外，还有一些其他逻辑用于计算列表中的当前位置，以及使用户能够停止分页并退出程序。</span><span class="sxs-lookup"><span data-stu-id="4369c-112">There is also some additional logic to compute the current position in the list, and to enable the user to stop paging and exit the program.</span></span> <span data-ttu-id="4369c-113">在此特定情况下，根据原始查询的缓存结果运行分页查询。</span><span class="sxs-lookup"><span data-stu-id="4369c-113">In this particular case, the paging query is run against the cached results from the original query.</span></span> <span data-ttu-id="4369c-114">在其他上下文中，如 LINQ to SQL，则不需要此类缓存。</span><span class="sxs-lookup"><span data-stu-id="4369c-114">In other contexts, such as LINQ to SQL, such caching is not required.</span></span>  
  
## <a name="compile-the-code"></a><span data-ttu-id="4369c-115">编译代码</span><span class="sxs-lookup"><span data-stu-id="4369c-115">Compile the code</span></span>  

<span data-ttu-id="4369c-116">使用 `Imports` System. Linq 命名空间的语句创建 Visual Basic 控制台应用程序项目。</span><span class="sxs-lookup"><span data-stu-id="4369c-116">Create a Visual Basic console application project, with an `Imports` statement for the System.Linq namespace.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="4369c-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="4369c-117">See also</span></span>

- [<span data-ttu-id="4369c-118">LINQ to Objects (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="4369c-118">LINQ to Objects (Visual Basic)</span></span>](linq-to-objects.md)
- [<span data-ttu-id="4369c-119">LINQ 和文件目录 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="4369c-119">LINQ and File Directories (Visual Basic)</span></span>](linq-and-file-directories.md)
