---
description: 了解详细信息：通过查询结果分页
title: 通过查询结果分页
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: fa360c46-e5f8-411e-a711-46997771133d
ms.openlocfilehash: ead2c74e19cfb81c83c7bf1e73b0c0d7a0a7cc67
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99672356"
---
# <a name="paging-through-a-query-result"></a><span data-ttu-id="e12ec-103">通过查询结果分页</span><span class="sxs-lookup"><span data-stu-id="e12ec-103">Paging Through a Query Result</span></span>

<span data-ttu-id="e12ec-104">查询结果分页是以较小数据子集（即页）的形式返回查询结果的过程。</span><span class="sxs-lookup"><span data-stu-id="e12ec-104">Paging through a query result is the process of returning the results of a query in smaller subsets of data, or pages.</span></span> <span data-ttu-id="e12ec-105">它通常用于以易于管理的小块形式向用户显示结果。</span><span class="sxs-lookup"><span data-stu-id="e12ec-105">This is a common practice for displaying results to a user in small, easy-to-manage chunks.</span></span>  
  
 <span data-ttu-id="e12ec-106">**DataAdapter** 通过 **Fill** 方法的重载提供仅返回一页数据的工具。</span><span class="sxs-lookup"><span data-stu-id="e12ec-106">The **DataAdapter** provides a facility for returning only a page of data, through overloads of the **Fill** method.</span></span> <span data-ttu-id="e12ec-107">但是，对于大量的查询结果，它可能并不是首选的分页方法，因为 DataAdapter 虽然仅使用所请求的记录来填充目标 <xref:System.Data.DataTable> 或 <xref:System.Data.DataSet>，但仍会使用返回整个查询的资源。</span><span class="sxs-lookup"><span data-stu-id="e12ec-107">However, this might not be the best choice for paging through large query results because, although the **DataAdapter** fills the target <xref:System.Data.DataTable> or <xref:System.Data.DataSet> with only the requested records, the resources to return the entire query are still used.</span></span> <span data-ttu-id="e12ec-108">若要在从数据源中返回一页数据时不使用返回整个查询的资源，请为查询指定附加条件，使返回的行数减少到只返回所需的行。</span><span class="sxs-lookup"><span data-stu-id="e12ec-108">To return a page of data from a data source without using the resources to return the entire query, specify additional criteria for your query that reduce the rows returned to only those required.</span></span>  
  
 <span data-ttu-id="e12ec-109">若要使用 **Fill** 方法返回数据页，请为数据页中的第一条记录指定 **startRecord** 参数，并为数据页中的记录数指定 **maxRecords** 参数。</span><span class="sxs-lookup"><span data-stu-id="e12ec-109">To use the **Fill** method to return a page of data, specify a **startRecord** parameter, for the first record in the page of data, and a **maxRecords** parameter, for the number of records in the page of data.</span></span>  
  
 <span data-ttu-id="e12ec-110">下面的代码示例演示如何使用 **Fill** 方法返回查询结果的第一页，其中页的大小为5条记录。</span><span class="sxs-lookup"><span data-stu-id="e12ec-110">The following code example shows how to use the **Fill** method to return the first page of a query result where the page size is five records.</span></span>  
  
```vb  
Dim currentIndex As Integer = 0  
Dim pageSize As Integer = 5  
  
Dim orderSQL As String = "SELECT * FROM dbo.Orders ORDER BY OrderID"  
' Assumes that connection is a valid SqlConnection object.  
Dim adapter As SqlDataAdapter = _  
  New SqlDataAdapter(orderSQL, connection)  
  
Dim dataSet As DataSet = New DataSet()  
adapter.Fill(dataSet, currentIndex, pageSize, "Orders")  
```  
  
```csharp  
int currentIndex = 0;  
int pageSize = 5;  
  
string orderSQL = "SELECT * FROM Orders ORDER BY OrderID";  
// Assumes that connection is a valid SqlConnection object.  
SqlDataAdapter adapter = new SqlDataAdapter(orderSQL, connection);  
  
DataSet dataSet = new DataSet();  
adapter.Fill(dataSet, currentIndex, pageSize, "Orders");  
```  
  
 <span data-ttu-id="e12ec-111">在上例中，DataSet 只填充了 5 个记录，但却返回了整个 Orders 表 。</span><span class="sxs-lookup"><span data-stu-id="e12ec-111">In the previous example, the **DataSet** is only filled with five records, but the entire **Orders** table is returned.</span></span> <span data-ttu-id="e12ec-112">若要用相同的五个记录填充 **数据集** ，但只返回5条记录，请在 SQL 语句中使用 TOP 和 WHERE 子句，如下面的代码示例所示。</span><span class="sxs-lookup"><span data-stu-id="e12ec-112">To fill the **DataSet** with those same five records, but only return five records, use the TOP and WHERE clauses in your SQL statement, as in the following code example.</span></span>  
  
```vb  
Dim pageSize As Integer = 5  
  
Dim orderSQL As String = "SELECT TOP " & pageSize & _  
  " * FROM Orders ORDER BY OrderID"  
Dim adapter As SqlDataAdapter = _  
  New SqlDataAdapter(orderSQL, connection)  
  
Dim dataSet As DataSet = New DataSet()  
adapter.Fill(dataSet, "Orders")
```  
  
```csharp  
int pageSize = 5;  
  
string orderSQL = "SELECT TOP " + pageSize +
  " * FROM Orders ORDER BY OrderID";  
SqlDataAdapter adapter = new SqlDataAdapter(orderSQL, connection);  
  
DataSet dataSet = new DataSet();  
adapter.Fill(dataSet, "Orders");  
```  
  
 <span data-ttu-id="e12ec-113">请注意，当以这种方式进行查询结果分页时，必须保留用于对行进行排序的唯一标识符，以便将唯一 ID 传递给用于返回下一页记录的命令，如以下代码示例所示。</span><span class="sxs-lookup"><span data-stu-id="e12ec-113">Note that, when paging through the query results in this way, you must preserve the unique identifier that orders the rows, in order to pass the unique ID to the command to return the next page of records, as shown in the following code example.</span></span>  
  
```vb  
Dim lastRecord As String = _  
  dataSet.Tables("Orders").Rows(pageSize - 1)("OrderID").ToString()  
```  
  
```csharp  
string lastRecord =
  dataSet.Tables["Orders"].Rows[pageSize - 1]["OrderID"].ToString();  
```  
  
 <span data-ttu-id="e12ec-114">若要使用 **Fill** 方法的重载返回 **startRecord** 和 **maxRecords** 参数的下一页记录，请将当前记录索引按页面大小递增，并填充表。</span><span class="sxs-lookup"><span data-stu-id="e12ec-114">To return the next page of records using the overload of the **Fill** method that takes the **startRecord** and **maxRecords** parameters, increment the current record index by the page size and fill the table.</span></span> <span data-ttu-id="e12ec-115">请记住，即使仅在 DataSet 中添加一页记录，数据库服务器仍会返回全部查询结果。</span><span class="sxs-lookup"><span data-stu-id="e12ec-115">Remember that the database server returns the entire query results even though only one page of records is added to the **DataSet**.</span></span> <span data-ttu-id="e12ec-116">在以下代码示例中，先清除表行，然后再用下一页数据填充这些表行。</span><span class="sxs-lookup"><span data-stu-id="e12ec-116">In the following code example, the table rows are cleared before they are filled with the next page of data.</span></span> <span data-ttu-id="e12ec-117">您可能需要在本地缓存中保留一定数量的返回行，以减少与数据库服务器的往返次数。</span><span class="sxs-lookup"><span data-stu-id="e12ec-117">You might want to preserve a certain number of returned rows in a local cache to reduce trips to the database server.</span></span>  
  
```vb  
currentIndex = currentIndex + pageSize  
  
dataSet.Tables("Orders").Rows.Clear()  
  
adapter.Fill(dataSet, currentIndex, pageSize, "Orders")  
```  
  
```csharp  
currentIndex += pageSize;  
  
dataSet.Tables["Orders"].Rows.Clear();  
  
adapter.Fill(dataSet, currentIndex, pageSize, "Orders");  
```  
  
 <span data-ttu-id="e12ec-118">若要返回下一页记录而不让数据库服务器返回整个查询，请指定对 SQL SELECT 语句的限制条件。</span><span class="sxs-lookup"><span data-stu-id="e12ec-118">To return the next page of records without having the database server return the entire query, specify restrictive criteria to the SELECT statement.</span></span> <span data-ttu-id="e12ec-119">由于上例保留了返回的最后一个记录，因此可以在 WHERE 子句中使用它来指定查询的起点，如以下代码示例所示。</span><span class="sxs-lookup"><span data-stu-id="e12ec-119">Because the preceding example preserved the last record returned, you can use it in the WHERE clause to specify a starting point for the query, as shown in the following code example.</span></span>  
  
```vb  
orderSQL = "SELECT TOP " & pageSize & _  
  " * FROM Orders WHERE OrderID > " & lastRecord & " ORDER BY OrderID"  
adapter.SelectCommand.CommandText = orderSQL  
  
dataSet.Tables("Orders").Rows.Clear()  
  
adapter.Fill(dataSet, "Orders")  
```  
  
```csharp  
orderSQL = "SELECT TOP " + pageSize +
  " * FROM Orders WHERE OrderID > " + lastRecord + " ORDER BY OrderID";  
adapter.SelectCommand.CommandText = orderSQL;  
  
dataSet.Tables["Orders"].Rows.Clear();  
  
adapter.Fill(dataSet, "Orders");  
```  
  
## <a name="see-also"></a><span data-ttu-id="e12ec-120">另请参阅</span><span class="sxs-lookup"><span data-stu-id="e12ec-120">See also</span></span>

- [<span data-ttu-id="e12ec-121">DataAdapter 和 DataReader</span><span class="sxs-lookup"><span data-stu-id="e12ec-121">DataAdapters and DataReaders</span></span>](dataadapters-and-datareaders.md)
- [<span data-ttu-id="e12ec-122">ADO.NET 概述</span><span class="sxs-lookup"><span data-stu-id="e12ec-122">ADO.NET Overview</span></span>](ado-net-overview.md)
