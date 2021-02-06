---
description: 了解详细信息： Load 方法
title: 加载方法
ms.date: 03/30/2017
dev_langs:
- vb
ms.assetid: e22e5812-89c6-41f0-9302-bb899a46dbff
ms.openlocfilehash: a14008597d88ad4af93c3646998244d94b5561d7
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99651517"
---
# <a name="the-load-method"></a><span data-ttu-id="2af58-103">加载方法</span><span class="sxs-lookup"><span data-stu-id="2af58-103">The Load Method</span></span>

<span data-ttu-id="2af58-104">可以使用 <xref:System.Data.DataTable.Load%2A> 方法为 <xref:System.Data.DataTable> 加载数据源中行。</span><span class="sxs-lookup"><span data-stu-id="2af58-104">You can use the <xref:System.Data.DataTable.Load%2A> method to load a <xref:System.Data.DataTable> with rows from a data source.</span></span> <span data-ttu-id="2af58-105">这是一种重载方法，其最简单的形式是接受一个参数（ **DataReader**）。</span><span class="sxs-lookup"><span data-stu-id="2af58-105">This is an overloaded method which, in its simplest form, accepts a single parameter, a **DataReader**.</span></span> <span data-ttu-id="2af58-106">在此窗体中，它只是加载包含行的 **DataTable** 。</span><span class="sxs-lookup"><span data-stu-id="2af58-106">In this form, it simply loads the **DataTable** with rows.</span></span> <span data-ttu-id="2af58-107">还可以指定 **LoadOption** 参数，以控制数据添加到 **DataTable** 的方式。</span><span class="sxs-lookup"><span data-stu-id="2af58-107">Optionally, you can specify the **LoadOption** parameter to control how data is added to the **DataTable**.</span></span>  
  
 <span data-ttu-id="2af58-108">当 **DataTable** 已经包含数据行时， **LoadOption** 参数特别有用，因为它描述了如何将数据源中的传入数据与表中已有的数据组合在一起。</span><span class="sxs-lookup"><span data-stu-id="2af58-108">The **LoadOption** parameter is particularly useful in cases where the **DataTable** already contains rows of data, because it describes how incoming data from the data source will be combined with the data already in the table.</span></span> <span data-ttu-id="2af58-109">例如， **PreserveCurrentValues** (默认的) 指定在将行标记为 **添加** 到 **DataTable** 的情况下，将 **原始** 值或每一列设置为数据源中匹配行的内容。</span><span class="sxs-lookup"><span data-stu-id="2af58-109">For example, **PreserveCurrentValues** (the default) specifies that in cases where a row is marked as **Added** in the **DataTable**, the **Original** value or each column is set to the contents of the matching row from the data source.</span></span> <span data-ttu-id="2af58-110">**当前** 值将保留在添加行时分配的值，该行的 **RowState** 将设置为 "**已更改**"。</span><span class="sxs-lookup"><span data-stu-id="2af58-110">The **Current** value will retain the values assigned when the row was added, and the **RowState** of the row will be set to **Changed**.</span></span>  
  
 <span data-ttu-id="2af58-111">下表给出了对 <xref:System.Data.LoadOption> 枚举值的简要说明。</span><span class="sxs-lookup"><span data-stu-id="2af58-111">The following table gives a short description of the <xref:System.Data.LoadOption> enumeration values.</span></span>  
  
|<span data-ttu-id="2af58-112">LoadOption 值</span><span class="sxs-lookup"><span data-stu-id="2af58-112">LoadOption value</span></span>|<span data-ttu-id="2af58-113">说明</span><span class="sxs-lookup"><span data-stu-id="2af58-113">Description</span></span>|  
|----------------------|-----------------|  
|<span data-ttu-id="2af58-114">**OverwriteRow**</span><span class="sxs-lookup"><span data-stu-id="2af58-114">**OverwriteRow**</span></span>|<span data-ttu-id="2af58-115">如果传入行的 **PrimaryKey** 值与 **DataTable** 中已有行的值相同，则每列的 **原始** 值和 **当前** 值将替换为传入行中的值，并且 **RowState** 属性将设置为 " **未更改**"。</span><span class="sxs-lookup"><span data-stu-id="2af58-115">If incoming rows have the same **PrimaryKey** value as a row already in the **DataTable**, the **Original** and **Current** values of each column are replaced with the values in the incoming row, and the **RowState** property is set to **Unchanged**.</span></span><br /><br /> <span data-ttu-id="2af58-116">使用不 **变** 的 **RowState** 值添加了数据源中不存在于 **DataTable** 中的行。</span><span class="sxs-lookup"><span data-stu-id="2af58-116">Rows from the data source that do not already exist in the **DataTable** are added with a **RowState** value of **Unchanged**.</span></span><br /><br /> <span data-ttu-id="2af58-117">此选项实际上会刷新 **DataTable** 的内容，使其与数据源的内容相匹配。</span><span class="sxs-lookup"><span data-stu-id="2af58-117">This option in effect refreshes the contents of the **DataTable** so that it matches the contents of the data source.</span></span>|  
|<span data-ttu-id="2af58-118">**PreserveCurrentValues（默认值）**</span><span class="sxs-lookup"><span data-stu-id="2af58-118">**PreserveCurrentValues (default)**</span></span>|<span data-ttu-id="2af58-119">如果传入行的 **PrimaryKey** 值与 **DataTable** 中已有行的值相同，则将 **原始** 值设置为传入行的内容，并且不会更改 **当前** 值。</span><span class="sxs-lookup"><span data-stu-id="2af58-119">If incoming rows have the same **PrimaryKey** value as a row already in the **DataTable**, the **Original** value is set to the contents of the incoming row, and the **Current** value is not changed.</span></span><br /><br /> <span data-ttu-id="2af58-120">如果 **添加** 或 **修改** 了 **RowState** ，则将其设置为 "**已修改**"。</span><span class="sxs-lookup"><span data-stu-id="2af58-120">If the **RowState** is **Added** or **Modified**, it is set to **Modified**.</span></span><br /><br /> <span data-ttu-id="2af58-121">如果 **删除** 了 **RowState** ，则它将保持 **删除**。</span><span class="sxs-lookup"><span data-stu-id="2af58-121">If the **RowState** was **Deleted**, it remains **Deleted**.</span></span><br /><br /> <span data-ttu-id="2af58-122">添加了数据源中不存在于 **DataTable** 中的行，并将 **RowState** 设置为 " **未更改**"。</span><span class="sxs-lookup"><span data-stu-id="2af58-122">Rows from the data source that do not already exist in the **DataTable** are added, and the **RowState** is set to **Unchanged**.</span></span>|  
|<span data-ttu-id="2af58-123">**UpdateCurrentValues**</span><span class="sxs-lookup"><span data-stu-id="2af58-123">**UpdateCurrentValues**</span></span>|<span data-ttu-id="2af58-124">如果传入行的 **PrimaryKey** 值与 **DataTable** 中已有行的值相同，则将 **当前** 值复制到 **原始** 值，然后将 **当前** 值设置为传入行的内容。</span><span class="sxs-lookup"><span data-stu-id="2af58-124">If incoming rows have the same **PrimaryKey** value as the row already in the **DataTable**, the **Current** value is copied to the **Original** value, and the **Current** value is then set to the contents of the incoming row.</span></span><br /><br /> <span data-ttu-id="2af58-125">如果 **添加** 了 **DataTable** 中的 **RowState** ，则 **RowState** 将继续 **添加**。</span><span class="sxs-lookup"><span data-stu-id="2af58-125">If the **RowState** in the **DataTable** was **Added**, the **RowState** remains **Added**.</span></span> <span data-ttu-id="2af58-126">对于标记为 "**已修改**" 或 "**已删除**" 的行，将 **修改** **RowState** 。</span><span class="sxs-lookup"><span data-stu-id="2af58-126">For rows marked as **Modified** or **Deleted**, the **RowState** is **Modified**.</span></span><br /><br /> <span data-ttu-id="2af58-127">添加了数据源中不存在于 **DataTable** 中的行，并将 **RowState** 设置为 "已 **添加**"。</span><span class="sxs-lookup"><span data-stu-id="2af58-127">Rows from the data source that do not already exist in the **DataTable** are added, and the **RowState** is set to **Added**.</span></span>|  
  
 <span data-ttu-id="2af58-128">下面的示例使用 **Load** 方法为 **Northwind** 数据库中的员工显示生日列表。</span><span class="sxs-lookup"><span data-stu-id="2af58-128">The following sample uses the **Load** method to display a list of birthdays for the employees in the **Northwind** database.</span></span>  
  
```vb  
Private Sub LoadBirthdays(ByVal connectionString As String)  
    ' Assumes that connectionString is a valid connection string  
    ' to the Northwind database on SQL Server.  
    Dim queryString As String = _  
    "SELECT LastName, FirstName, BirthDate " & _  
      " FROM dbo.Employees " & _  
      "ORDER BY BirthDate, LastName, FirstName"  
  
    ' Open and fill a DataSet.
    Dim adapter As SqlDataAdapter = New SqlDataAdapter( _  
        queryString, connectionString)  
    Dim employees As New DataSet  
    adapter.Fill(employees, "Employees")  
  
    ' Create a SqlDataReader for use with the Load Method.  
    Dim reader As DataTableReader = employees.GetDataReader()  
  
    ' Create an instance of DataTable and assign the first  
    ' DataTable in the DataSet.Tables collection to it.  
    Dim dataTableEmp As DataTable = employees.Tables(0)  
  
    ' Fill the DataTable with data by calling Load and  
    ' passing the SqlDataReader.  
    dataTableEmp.Load(reader, LoadOption.OverwriteRow)  
  
    ' Loop through the rows collection and display the values  
    ' in the console window.  
    Dim employeeRow As DataRow  
    For Each employeeRow In dataTableEmp.Rows  
        Console.WriteLine("{0:MM\\dd\\yyyy}" & ControlChars.Tab & _  
          "{1}, {2}", _  
          employeeRow("BirthDate"), _  
          employeeRow("LastName"), _  
          employeeRow("FirstName"))  
    Next employeeRow  
  
    ' Keep the window opened to view the contents.  
    Console.ReadLine()  
End Sub  
```  
  
## <a name="see-also"></a><span data-ttu-id="2af58-129">请参阅</span><span class="sxs-lookup"><span data-stu-id="2af58-129">See also</span></span>

- [<span data-ttu-id="2af58-130">操作数据表中的数据</span><span class="sxs-lookup"><span data-stu-id="2af58-130">Manipulating Data in a DataTable</span></span>](manipulating-data-in-a-datatable.md)
- [<span data-ttu-id="2af58-131">ADO.NET 概述</span><span class="sxs-lookup"><span data-stu-id="2af58-131">ADO.NET Overview</span></span>](../ado-net-overview.md)
