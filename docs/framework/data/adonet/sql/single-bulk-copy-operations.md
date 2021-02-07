---
description: 了解详细信息：单次大容量复制操作
title: 单个批量复制操作
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 5e7ff0be-3f23-4996-a92c-bd54d65c3836
ms.openlocfilehash: f6b046fbd73ad798f3f9f117eea0b72f46e43b37
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99767474"
---
# <a name="single-bulk-copy-operations"></a><span data-ttu-id="46ef1-103">单个批量复制操作</span><span class="sxs-lookup"><span data-stu-id="46ef1-103">Single Bulk Copy Operations</span></span>

<span data-ttu-id="46ef1-104">执行 SQL Server 大容量复制操作的最简单方法是针对数据库执行单次操作。</span><span class="sxs-lookup"><span data-stu-id="46ef1-104">The simplest approach to performing a SQL Server bulk copy operation is to perform a single operation against a database.</span></span> <span data-ttu-id="46ef1-105">默认情况下，大容量复制操作作为独立的操作执行：复制操作以非事务的方式执行，不可对其进行回滚。</span><span class="sxs-lookup"><span data-stu-id="46ef1-105">By default, a bulk copy operation is performed as an isolated operation: the copy operation occurs in a non-transacted way, with no opportunity for rolling it back.</span></span>

> [!NOTE]
> <span data-ttu-id="46ef1-106">如果在发生错误时需要回滚全部或部分大容量复制，可以使用 <xref:System.Data.SqlClient.SqlBulkCopy> 托管的事务，或者在现有事务内执行大容量复制操作。</span><span class="sxs-lookup"><span data-stu-id="46ef1-106">If you need to roll back all or part of the bulk copy when an error occurs, you can either use a <xref:System.Data.SqlClient.SqlBulkCopy>-managed transaction, or perform the bulk copy operation within an existing transaction.</span></span> <span data-ttu-id="46ef1-107">如果连接在 System.Transactions 事务中（显式或隐式）登记，SqlBulkCopy 也将适用于  <xref:System.Transactions>  。</span><span class="sxs-lookup"><span data-stu-id="46ef1-107">**SqlBulkCopy** will also work with <xref:System.Transactions> if the connection is enlisted (implicitly or explicitly) into a **System.Transactions** transaction.</span></span>
>
> <span data-ttu-id="46ef1-108">有关详细信息，请参阅 [事务和大容量复制操作](transaction-and-bulk-copy-operations.md)。</span><span class="sxs-lookup"><span data-stu-id="46ef1-108">For more information, see [Transaction and Bulk Copy Operations](transaction-and-bulk-copy-operations.md).</span></span>

<span data-ttu-id="46ef1-109">执行大容量复制操作的常规步骤如下：</span><span class="sxs-lookup"><span data-stu-id="46ef1-109">The general steps for performing a bulk copy operation are as follows:</span></span>

1. <span data-ttu-id="46ef1-110">连接到源服务器并获取要复制的数据。</span><span class="sxs-lookup"><span data-stu-id="46ef1-110">Connect to the source server and obtain the data to be copied.</span></span> <span data-ttu-id="46ef1-111">如果可以从 <xref:System.Data.IDataReader> 或 <xref:System.Data.DataTable> 对象检索数据，那么数据也可以来自其他源。</span><span class="sxs-lookup"><span data-stu-id="46ef1-111">Data can also come from other sources, if it can be retrieved from an <xref:System.Data.IDataReader> or <xref:System.Data.DataTable> object.</span></span>

2. <span data-ttu-id="46ef1-112">连接到目标服务器（除非希望 SqlBulkCopy 为你建立连接  ）。</span><span class="sxs-lookup"><span data-stu-id="46ef1-112">Connect to the destination server (unless you want **SqlBulkCopy** to establish a connection for you).</span></span>

3. <span data-ttu-id="46ef1-113">创建 <xref:System.Data.SqlClient.SqlBulkCopy> 对象，设置任何必要的属性。</span><span class="sxs-lookup"><span data-stu-id="46ef1-113">Create a <xref:System.Data.SqlClient.SqlBulkCopy> object, setting any necessary properties.</span></span>

4. <span data-ttu-id="46ef1-114">设置 DestinationTableName 属性以指示执行批量插入操作的目标表  。</span><span class="sxs-lookup"><span data-stu-id="46ef1-114">Set the **DestinationTableName** property to indicate the target table for the bulk insert operation.</span></span>

5. <span data-ttu-id="46ef1-115">调用 WriteToServer 方法之一  。</span><span class="sxs-lookup"><span data-stu-id="46ef1-115">Call one of the **WriteToServer** methods.</span></span>

6. <span data-ttu-id="46ef1-116">可以选择更新属性并根据需要再次调用 WriteToServer  。</span><span class="sxs-lookup"><span data-stu-id="46ef1-116">Optionally, update properties and call **WriteToServer** again as necessary.</span></span>

7. <span data-ttu-id="46ef1-117">调用 <xref:System.Data.SqlClient.SqlBulkCopy.Close%2A>，或在 `Using` 语句中包装大容量复制操作。</span><span class="sxs-lookup"><span data-stu-id="46ef1-117">Call <xref:System.Data.SqlClient.SqlBulkCopy.Close%2A>, or wrap the bulk copy operations within a `Using` statement.</span></span>

> [!CAUTION]
> <span data-ttu-id="46ef1-118">我们建议使源列与目标列数据类型相匹配。</span><span class="sxs-lookup"><span data-stu-id="46ef1-118">We recommend that the source and target column data types match.</span></span> <span data-ttu-id="46ef1-119">如果数据类型不匹配，则 SqlBulkCopy 会尝试使用由  **部署的规则将每个源值转换为目标数据类型**<xref:System.Data.SqlClient.SqlParameter.Value%2A>。</span><span class="sxs-lookup"><span data-stu-id="46ef1-119">If the data types do not match, **SqlBulkCopy** attempts to convert each source value to the target data type, using the rules employed by <xref:System.Data.SqlClient.SqlParameter.Value%2A>.</span></span> <span data-ttu-id="46ef1-120">转换可能会影响性能，也可能会导致意外错误。</span><span class="sxs-lookup"><span data-stu-id="46ef1-120">Conversions can affect performance, and also can result in unexpected errors.</span></span> <span data-ttu-id="46ef1-121">例如，在多数情况下，`Double` 数据类型可转换为 `Decimal` 数据类型，但并非总是如此。</span><span class="sxs-lookup"><span data-stu-id="46ef1-121">For example, a `Double` data type can be converted to a `Decimal` data type most of the time, but not always.</span></span>

## <a name="example"></a><span data-ttu-id="46ef1-122">示例</span><span class="sxs-lookup"><span data-stu-id="46ef1-122">Example</span></span>

<span data-ttu-id="46ef1-123">下面的控制台应用程序演示了如何使用 <xref:System.Data.SqlClient.SqlBulkCopy> 类加载数据。</span><span class="sxs-lookup"><span data-stu-id="46ef1-123">The following console application demonstrates how to load data using the <xref:System.Data.SqlClient.SqlBulkCopy> class.</span></span> <span data-ttu-id="46ef1-124">在此示例中，<xref:System.Data.SqlClient.SqlDataReader> 用于将数据从 SQL Server AdventureWorks 数据库的 Production.Product 表复制到相同数据库的一个类似的表中   。</span><span class="sxs-lookup"><span data-stu-id="46ef1-124">In this example, a <xref:System.Data.SqlClient.SqlDataReader> is used to copy data from the **Production.Product** table in the SQL Server **AdventureWorks** database to a similar table in the same database.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="46ef1-125">除非已按照 [大容量复制示例设置](bulk-copy-example-setup.md)中所述创建了工作表，否则此示例将不会运行。</span><span class="sxs-lookup"><span data-stu-id="46ef1-125">This sample will not run unless you have created the work tables as described in [Bulk Copy Example Setup](bulk-copy-example-setup.md).</span></span> <span data-ttu-id="46ef1-126">提供此代码是为了演示仅使用 SqlBulkCopy 时的语法  。</span><span class="sxs-lookup"><span data-stu-id="46ef1-126">This code is provided to demonstrate the syntax for using **SqlBulkCopy** only.</span></span> <span data-ttu-id="46ef1-127">如果源表和目标表位于同一 SQL Server 实例中，可以更便捷地使用 Transact-SQL `INSERT … SELECT` 语句复制数据。</span><span class="sxs-lookup"><span data-stu-id="46ef1-127">If the source and destination tables are located in the same SQL Server instance, it is easier and faster to use a Transact-SQL `INSERT … SELECT` statement to copy the data.</span></span>

[!code-csharp[DataWorks BulkCopy.Single#1](../../../../../samples/snippets/csharp/VS_Snippets_ADO.NET/DataWorks BulkCopy.Single/CS/source.cs#1)]
[!code-vb[DataWorks BulkCopy.Single#1](../../../../../samples/snippets/visualbasic/VS_Snippets_ADO.NET/DataWorks BulkCopy.Single/VB/source.vb#1)]

## <a name="performing-a-bulk-copy-operation-using-transact-sql-and-the-command-class"></a><span data-ttu-id="46ef1-128">使用 Transact-SQL 和命令类执行批量复制操作</span><span class="sxs-lookup"><span data-stu-id="46ef1-128">Performing a Bulk Copy Operation Using Transact-SQL and the Command Class</span></span>

<span data-ttu-id="46ef1-129">下面的示例说明了如何使用 <xref:System.Data.SqlClient.SqlCommand.ExecuteNonQuery%2A> 方法执行 BULK INSERT 语句。</span><span class="sxs-lookup"><span data-stu-id="46ef1-129">The following example illustrates how to use the <xref:System.Data.SqlClient.SqlCommand.ExecuteNonQuery%2A> method to execute the BULK INSERT statement.</span></span>

> [!NOTE]
> <span data-ttu-id="46ef1-130">数据源的文件路径相对于服务器。</span><span class="sxs-lookup"><span data-stu-id="46ef1-130">The file path for the data source is relative to the server.</span></span> <span data-ttu-id="46ef1-131">服务器进程必须有权访问该路径，才能成功执行大容量复制操作。</span><span class="sxs-lookup"><span data-stu-id="46ef1-131">The server process must have access to that path in order for the bulk copy operation to succeed.</span></span>

```vb
Using connection As SqlConnection = New SqlConnection(connectionString)
Dim queryString As String = _
    "BULK INSERT Northwind.dbo.[Order Details] FROM " & _
    "'f:\mydata\data.tbl' WITH (FORMATFILE='f:\mydata\data.fmt' )"
connection.Open()
SqlCommand command = New SqlCommand(queryString, connection);

command.ExecuteNonQuery()
End Using
```

```csharp
using (SqlConnection connection = New SqlConnection(connectionString))
{
string queryString =  "BULK INSERT Northwind.dbo.[Order Details] " +
    "FROM 'f:\mydata\data.tbl' " +
    "WITH ( FORMATFILE='f:\mydata\data.fmt' )";
connection.Open();
SqlCommand command = new SqlCommand(queryString, connection);

command.ExecuteNonQuery();
}
```

## <a name="see-also"></a><span data-ttu-id="46ef1-132">请参阅</span><span class="sxs-lookup"><span data-stu-id="46ef1-132">See also</span></span>

- [<span data-ttu-id="46ef1-133">SQL Server 中的大容量复制操作</span><span class="sxs-lookup"><span data-stu-id="46ef1-133">Bulk Copy Operations in SQL Server</span></span>](bulk-copy-operations-in-sql-server.md)
- [<span data-ttu-id="46ef1-134">ADO.NET 概述</span><span class="sxs-lookup"><span data-stu-id="46ef1-134">ADO.NET Overview</span></span>](../ado-net-overview.md)
