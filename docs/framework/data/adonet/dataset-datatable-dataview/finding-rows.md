---
description: 了解详细信息：查找行
title: 查找行
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 5da300e2-74c0-4d13-9202-fc20ed8212d8
ms.openlocfilehash: bf4752255945d5bbc0dd5551cd6e84c98fd78c3f
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99652466"
---
# <a name="finding-rows"></a><span data-ttu-id="0dd7d-103">查找行</span><span class="sxs-lookup"><span data-stu-id="0dd7d-103">Finding Rows</span></span>

<span data-ttu-id="0dd7d-104">可以使用 <xref:System.Data.DataView.Find%2A> 的 <xref:System.Data.DataView.FindRows%2A> 和 <xref:System.Data.DataView> 方法，根据排序关键字值搜索行。</span><span class="sxs-lookup"><span data-stu-id="0dd7d-104">You can search for rows according to their sort key values by using the <xref:System.Data.DataView.Find%2A> and <xref:System.Data.DataView.FindRows%2A> methods of the <xref:System.Data.DataView>.</span></span> <span data-ttu-id="0dd7d-105">**Find** 和 **FindRows** 方法中搜索值的区分大小写取决于基础的 **CaseSensitive** 属性 <xref:System.Data.DataTable> 。</span><span class="sxs-lookup"><span data-stu-id="0dd7d-105">The case sensitivity of search values in the **Find** and **FindRows** methods is determined by the **CaseSensitive** property of the underlying <xref:System.Data.DataTable>.</span></span> <span data-ttu-id="0dd7d-106">搜索值必须完全匹配现有排序关键字值才能返回结果。</span><span class="sxs-lookup"><span data-stu-id="0dd7d-106">Search values must match existing sort key values in their entirety in order to return a result.</span></span>  
  
 <span data-ttu-id="0dd7d-107">**Find** 方法返回一个整数，该整数包含与 <xref:System.Data.DataRowView> 搜索条件匹配的的索引。</span><span class="sxs-lookup"><span data-stu-id="0dd7d-107">The **Find** method returns an integer with the index of the <xref:System.Data.DataRowView> that matches the search criteria.</span></span> <span data-ttu-id="0dd7d-108">如果多行与搜索条件匹配，则仅返回第一个匹配 **DataRowView** 的索引。</span><span class="sxs-lookup"><span data-stu-id="0dd7d-108">If more than one row matches the search criteria, only the index of the first matching **DataRowView** is returned.</span></span> <span data-ttu-id="0dd7d-109">如果找不到匹配项， **Find** 将返回-1。</span><span class="sxs-lookup"><span data-stu-id="0dd7d-109">If no matches are found, **Find** returns -1.</span></span>  
  
 <span data-ttu-id="0dd7d-110">若要返回与多个行匹配的搜索结果，请使用 **FindRows** 方法。</span><span class="sxs-lookup"><span data-stu-id="0dd7d-110">To return search results that match multiple rows, use the **FindRows** method.</span></span> <span data-ttu-id="0dd7d-111">**FindRows** 的工作方式与 **Find** 方法相同，不同之处在于该方法返回的 **DataRowView** 数组引用 **DataView** 中的所有匹配行。</span><span class="sxs-lookup"><span data-stu-id="0dd7d-111">**FindRows** works just like the **Find** method, except that it returns a **DataRowView** array that references all matching rows in the **DataView**.</span></span> <span data-ttu-id="0dd7d-112">如果未找到匹配项， **DataRowView** 数组将为空。</span><span class="sxs-lookup"><span data-stu-id="0dd7d-112">If no matches are found, the **DataRowView** array will be empty.</span></span>  
  
 <span data-ttu-id="0dd7d-113">若要使用 **Find** 或 **FindRows** 方法，必须通过将 **ApplyDefaultSort** 设置为 **true** 或使用 **sort** 属性来指定排序顺序。</span><span class="sxs-lookup"><span data-stu-id="0dd7d-113">To use the **Find** or **FindRows** methods you must specify a sort order either by setting **ApplyDefaultSort** to **true** or by using the **Sort** property.</span></span> <span data-ttu-id="0dd7d-114">如果未指定排序顺序，则将引发异常。</span><span class="sxs-lookup"><span data-stu-id="0dd7d-114">If no sort order is specified, an exception is thrown.</span></span>  
  
 <span data-ttu-id="0dd7d-115">**Find** 和 **FindRows** 方法将值数组作为输入，其长度与排序顺序中的列数匹配。</span><span class="sxs-lookup"><span data-stu-id="0dd7d-115">The **Find** and **FindRows** methods take an array of values as input whose length matches the number of columns in the sort order.</span></span> <span data-ttu-id="0dd7d-116">在对单个列进行排序的情况下，可以传递单个值。</span><span class="sxs-lookup"><span data-stu-id="0dd7d-116">In the case of a sort on a single column, you can pass a single value.</span></span> <span data-ttu-id="0dd7d-117">对于包含多个列的排序顺序，可传递一个对象数组。</span><span class="sxs-lookup"><span data-stu-id="0dd7d-117">For sort orders containing multiple columns, you pass an array of objects.</span></span> <span data-ttu-id="0dd7d-118">请注意，对于多列排序，对象数组中的值必须与 **DataView** 的 **sort** 属性中指定的列顺序相匹配。</span><span class="sxs-lookup"><span data-stu-id="0dd7d-118">Note that for a sort on multiple columns, the values in the object array must match the order of the columns specified in the **Sort** property of the **DataView**.</span></span>  
  
 <span data-ttu-id="0dd7d-119">下面的代码示例演示了如何使用单列排序顺序对 **DataView** 调用 **Find** 方法。</span><span class="sxs-lookup"><span data-stu-id="0dd7d-119">The following code example shows the **Find** method being called against a **DataView** with a single column sort order.</span></span>  
  
```vb  
Dim custView As DataView = _  
  New DataView(custDS.Tables("Customers"), "", _  
  "CompanyName", DataViewRowState.CurrentRows)  
  
Dim rowIndex As Integer = custView.Find("The Cracker Box")  
  
If rowIndex = -1 Then  
  Console.WriteLine("No match found.")  
Else  
  Console.WriteLine("{0}, {1}", _  
    custView(rowIndex)("CustomerID").ToString(), _  
    custView(rowIndex)("CompanyName").ToString())  
End If  
```  
  
```csharp  
DataView custView = new DataView(custDS.Tables["Customers"], "",
  "CompanyName", DataViewRowState.CurrentRows);  
  
int rowIndex = custView.Find("The Cracker Box");  
  
if (rowIndex == -1)  
  Console.WriteLine("No match found.");  
else  
  Console.WriteLine("{0}, {1}",  
    custView[rowIndex]["CustomerID"].ToString(),  
    custView[rowIndex]["CompanyName"].ToString());  
```  
  
 <span data-ttu-id="0dd7d-120">如果 **Sort** 属性指定了多个列，则必须按照 **sort** 属性指定的顺序为每个列的搜索值传递对象数组，如下面的代码示例所示。</span><span class="sxs-lookup"><span data-stu-id="0dd7d-120">If your **Sort** property specifies multiple columns, you must pass an object array with the search values for each column in the order specified by the **Sort** property, as in the following code example.</span></span>  
  
```vb  
Dim custView As DataView = _  
  New DataView(custDS.Tables("Customers"), "", _  
  "CompanyName, ContactName", _  
  DataViewRowState.CurrentRows)  
  
Dim foundRows() As DataRowView = _  
  custView.FindRows(New object() {"The Cracker Box", "Liu Wong"})  
  
If foundRows.Length = 0 Then  
  Console.WriteLine("No match found.")  
Else  
  Dim myDRV As DataRowView  
  For Each myDRV In foundRows  
    Console.WriteLine("{0}, {1}", _  
      myDRV("CompanyName").ToString(), myDRV("ContactName").ToString())  
  Next  
End If  
```  
  
```csharp  
DataView custView = new DataView(custDS.Tables["Customers"], "",  
  "CompanyName, ContactName",  
  DataViewRowState.CurrentRows);  
  
DataRowView[] foundRows =
  custView.FindRows(new object[] {"The Cracker Box", "Liu Wong"});  
  
if (foundRows.Length == 0)  
  Console.WriteLine("No match found.");  
else  
  foreach (DataRowView myDRV in foundRows)  
    Console.WriteLine("{0}, {1}", myDRV["CompanyName"].ToString(),
      myDRV["ContactName"].ToString());  
```  
  
## <a name="see-also"></a><span data-ttu-id="0dd7d-121">请参阅</span><span class="sxs-lookup"><span data-stu-id="0dd7d-121">See also</span></span>

- <xref:System.Data.DataTable>
- <xref:System.Data.DataView>
- [<span data-ttu-id="0dd7d-122">DataView</span><span class="sxs-lookup"><span data-stu-id="0dd7d-122">DataViews</span></span>](dataviews.md)
- [<span data-ttu-id="0dd7d-123">ADO.NET 概述</span><span class="sxs-lookup"><span data-stu-id="0dd7d-123">ADO.NET Overview</span></span>](../ado-net-overview.md)
