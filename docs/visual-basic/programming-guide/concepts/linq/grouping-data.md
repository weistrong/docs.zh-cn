---
description: '了解详细信息：将数据分组 (Visual Basic) '
title: 数据分组
ms.date: 07/20/2015
ms.assetid: 8f3a0871-6958-4aef-8f6f-493e189fd57d
ms.openlocfilehash: fa6dbcc22c7d991d48775c3974cfc529840ef933
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100469794"
---
# <a name="grouping-data-visual-basic"></a><span data-ttu-id="6d7d3-103">将数据分组 (Visual Basic) </span><span class="sxs-lookup"><span data-stu-id="6d7d3-103">Grouping Data (Visual Basic)</span></span>

<span data-ttu-id="6d7d3-104">分组是指将数据分到不同的组，使每组中的元素拥有公共的属性。</span><span class="sxs-lookup"><span data-stu-id="6d7d3-104">Grouping refers to the operation of putting data into groups so that the elements in each group share a common attribute.</span></span>  
  
 <span data-ttu-id="6d7d3-105">下图演示了对字符序列进行分组的结果。</span><span class="sxs-lookup"><span data-stu-id="6d7d3-105">The following illustration shows the results of grouping a sequence of characters.</span></span> <span data-ttu-id="6d7d3-106">每个组的键是字符。</span><span class="sxs-lookup"><span data-stu-id="6d7d3-106">The key for each group is the character.</span></span>  
  
 ![关系图显示 LINQ 分组操作。](./media/grouping-data/linq-group-operation.png)  
  
 <span data-ttu-id="6d7d3-108">下一节列出了对数据元素进行分组的标准查询运算符方法。</span><span class="sxs-lookup"><span data-stu-id="6d7d3-108">The standard query operator methods that group data elements are listed in the following section.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="6d7d3-109">方法</span><span class="sxs-lookup"><span data-stu-id="6d7d3-109">Methods</span></span>  
  
|<span data-ttu-id="6d7d3-110">方法名</span><span class="sxs-lookup"><span data-stu-id="6d7d3-110">Method Name</span></span>|<span data-ttu-id="6d7d3-111">描述</span><span class="sxs-lookup"><span data-stu-id="6d7d3-111">Description</span></span>|<span data-ttu-id="6d7d3-112">Visual Basic 查询表达式语法</span><span class="sxs-lookup"><span data-stu-id="6d7d3-112">Visual Basic Query Expression Syntax</span></span>|<span data-ttu-id="6d7d3-113">详细信息</span><span class="sxs-lookup"><span data-stu-id="6d7d3-113">More Information</span></span>|  
|-----------------|-----------------|------------------------------------------|----------------------|  
|<span data-ttu-id="6d7d3-114">GroupBy</span><span class="sxs-lookup"><span data-stu-id="6d7d3-114">GroupBy</span></span>|<span data-ttu-id="6d7d3-115">对共享通用属性的元素进行分组。</span><span class="sxs-lookup"><span data-stu-id="6d7d3-115">Groups elements that share a common attribute.</span></span> <span data-ttu-id="6d7d3-116">每组由一个 <xref:System.Linq.IGrouping%602> 对象表示。</span><span class="sxs-lookup"><span data-stu-id="6d7d3-116">Each group is represented by an <xref:System.Linq.IGrouping%602> object.</span></span>|`Group … By … Into …`|<xref:System.Linq.Enumerable.GroupBy%2A?displayProperty=nameWithType><br /><br /> <xref:System.Linq.Queryable.GroupBy%2A?displayProperty=nameWithType>|  
|<span data-ttu-id="6d7d3-117">ToLookup</span><span class="sxs-lookup"><span data-stu-id="6d7d3-117">ToLookup</span></span>|<span data-ttu-id="6d7d3-118">将元素插入基于键选择器函数的 <xref:System.Linq.Lookup%602>（一种一对多字典）。</span><span class="sxs-lookup"><span data-stu-id="6d7d3-118">Inserts elements into a <xref:System.Linq.Lookup%602> (a one-to-many dictionary) based on a key selector function.</span></span>|<span data-ttu-id="6d7d3-119">不适用。</span><span class="sxs-lookup"><span data-stu-id="6d7d3-119">Not applicable.</span></span>|<xref:System.Linq.Enumerable.ToLookup%2A?displayProperty=nameWithType>|  
  
## <a name="query-expression-syntax-example"></a><span data-ttu-id="6d7d3-120">查询表达式语法示例</span><span class="sxs-lookup"><span data-stu-id="6d7d3-120">Query Expression Syntax Example</span></span>  

 <span data-ttu-id="6d7d3-121">下列代码示例根据奇偶性，使用 `Group By` 子句对列表中的整数进行分组。</span><span class="sxs-lookup"><span data-stu-id="6d7d3-121">The following code example uses the `Group By` clause to group integers in a list according to whether they are even or odd.</span></span>  
  
```vb  
Dim numbers As New System.Collections.Generic.List(Of Integer)(  
     New Integer() {35, 44, 200, 84, 3987, 4, 199, 329, 446, 208})  
  
Dim query = From number In numbers
            Group By Remainder = (number Mod 2) Into Group  
  
Dim sb As New System.Text.StringBuilder()  
For Each group In query  
    sb.AppendLine(If(group.Remainder = 0, vbCrLf & "Even numbers:", vbCrLf & "Odd numbers:"))  
    For Each num In group.Group  
        sb.AppendLine(num)  
    Next  
Next  
  
' Display the results.  
MsgBox(sb.ToString())  
  
' This code produces the following output:  
  
' Odd numbers:  
' 35  
' 3987  
' 199  
' 329  
  
' Even numbers:  
' 44  
' 200  
' 84  
' 4  
' 446  
' 208  
```  
  
## <a name="see-also"></a><span data-ttu-id="6d7d3-122">请参阅</span><span class="sxs-lookup"><span data-stu-id="6d7d3-122">See also</span></span>

- <xref:System.Linq>
- [<span data-ttu-id="6d7d3-123">标准查询运算符概述 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="6d7d3-123">Standard Query Operators Overview (Visual Basic)</span></span>](standard-query-operators-overview.md)
- [<span data-ttu-id="6d7d3-124">Group By 子句</span><span class="sxs-lookup"><span data-stu-id="6d7d3-124">Group By Clause</span></span>](../../../language-reference/queries/group-by-clause.md)
- [<span data-ttu-id="6d7d3-125">如何：按扩展名对文件进行分组 (LINQ)  (Visual Basic) </span><span class="sxs-lookup"><span data-stu-id="6d7d3-125">How to: Group Files by Extension (LINQ) (Visual Basic)</span></span>](how-to-group-files-by-extension-linq.md)
- [<span data-ttu-id="6d7d3-126">如何：使用组将一个文件拆分成多个文件 (LINQ)  (Visual Basic) </span><span class="sxs-lookup"><span data-stu-id="6d7d3-126">How to: Split a File Into Many Files by Using Groups (LINQ) (Visual Basic)</span></span>](how-to-split-a-file-into-many-files-by-using-groups-linq.md)
