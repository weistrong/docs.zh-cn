---
description: 了解详细信息： DbConnection、DbCommand 和 DbException
title: DbConnection、DbCommand 和 DbException
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 58aab611-7e6f-4749-b983-28ab7ae87dbe
ms.openlocfilehash: b5cb748a8dd5fb06f2f5dc5ab0479a679b2cc07d
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99651270"
---
# <a name="dbconnection-dbcommand-and-dbexception"></a><span data-ttu-id="09a10-103">DbConnection、DbCommand 和 DbException</span><span class="sxs-lookup"><span data-stu-id="09a10-103">DbConnection, DbCommand and DbException</span></span>

<span data-ttu-id="09a10-104">创建了 <xref:System.Data.Common.DbProviderFactory> 和 <xref:System.Data.Common.DbConnection> 后，您便可以使用命令和数据读取器来从数据源检索数据。</span><span class="sxs-lookup"><span data-stu-id="09a10-104">Once you have created a <xref:System.Data.Common.DbProviderFactory> and a <xref:System.Data.Common.DbConnection>, you can then work with commands and data readers to retrieve data from the data source.</span></span>  
  
## <a name="retrieving-data-example"></a><span data-ttu-id="09a10-105">检索数据示例</span><span class="sxs-lookup"><span data-stu-id="09a10-105">Retrieving Data Example</span></span>  

 <span data-ttu-id="09a10-106">此示例将 `DbConnection` 对象用作参数。</span><span class="sxs-lookup"><span data-stu-id="09a10-106">This example takes a `DbConnection` object as an argument.</span></span> <span data-ttu-id="09a10-107">通过将 <xref:System.Data.Common.DbCommand> 设置为 SQL SELECT 语句，可创建 <xref:System.Data.Common.DbCommand.CommandText%2A> 以从类别表中选择数据。</span><span class="sxs-lookup"><span data-stu-id="09a10-107">A <xref:System.Data.Common.DbCommand> is created to select data from the Categories table by setting the <xref:System.Data.Common.DbCommand.CommandText%2A> to a SQL SELECT statement.</span></span> <span data-ttu-id="09a10-108">该代码假定数据源中存在类别表。</span><span class="sxs-lookup"><span data-stu-id="09a10-108">The code assumes that the Categories table exists at the data source.</span></span> <span data-ttu-id="09a10-109">打开连接并使用 <xref:System.Data.Common.DbDataReader> 检索数据。</span><span class="sxs-lookup"><span data-stu-id="09a10-109">The connection is opened and the data is retrieved using a <xref:System.Data.Common.DbDataReader>.</span></span>  
  
 [!code-csharp[DataWorks DbProviderFactories.DbCommandData#1](../../../../samples/snippets/csharp/VS_Snippets_ADO.NET/DataWorks DbProviderFactories.DbCommandData/CS/source.cs#1)]
 [!code-vb[DataWorks DbProviderFactories.DbCommandData#1](../../../../samples/snippets/visualbasic/VS_Snippets_ADO.NET/DataWorks DbProviderFactories.DbCommandData/VB/source.vb#1)]  
  
## <a name="executing-a-command-example"></a><span data-ttu-id="09a10-110">执行命令示例</span><span class="sxs-lookup"><span data-stu-id="09a10-110">Executing a Command Example</span></span>  

 <span data-ttu-id="09a10-111">此示例将 `DbConnection` 对象用作参数。</span><span class="sxs-lookup"><span data-stu-id="09a10-111">This example takes a `DbConnection` object as an argument.</span></span> <span data-ttu-id="09a10-112">如果 `DbConnection` 有效，则会打开该连接，并创建和执行 <xref:System.Data.Common.DbCommand>。</span><span class="sxs-lookup"><span data-stu-id="09a10-112">If the `DbConnection` is valid, the connection is opened and a <xref:System.Data.Common.DbCommand> is created and executed.</span></span> <span data-ttu-id="09a10-113">将 <xref:System.Data.Common.DbCommand.CommandText%2A> 设置为 SQL INSERT 语句，以执行插入到 Northwind 数据库类别表中的操作。</span><span class="sxs-lookup"><span data-stu-id="09a10-113">The <xref:System.Data.Common.DbCommand.CommandText%2A> is set to a SQL INSERT statement that performs an insert to the Categories table in the Northwind database.</span></span> <span data-ttu-id="09a10-114">该代码假定数据源中存在 Northwind 数据库，并且 INSERT 语句中使用的 SQL 语法对于指定提供程序有效。</span><span class="sxs-lookup"><span data-stu-id="09a10-114">The code assumes that the Northwind database exists at the data source, and that the SQL syntax used in the INSERT statement is valid for the specified provider.</span></span> <span data-ttu-id="09a10-115">数据源中发生的错误由 <xref:System.Data.Common.DbException> 代码块处理，其他所有异常在 <xref:System.Exception> 块中处理。</span><span class="sxs-lookup"><span data-stu-id="09a10-115">Errors occurring at the data source are handled by the <xref:System.Data.Common.DbException> code block, and all other exceptions are handled in the <xref:System.Exception> block.</span></span>  
  
 [!code-csharp[DataWorks DbProviderFactories.DbCommand#1](../../../../samples/snippets/csharp/VS_Snippets_ADO.NET/DataWorks DbProviderFactories.DbCommand/CS/source.cs#1)]
 [!code-vb[DataWorks DbProviderFactories.DbCommand#1](../../../../samples/snippets/visualbasic/VS_Snippets_ADO.NET/DataWorks DbProviderFactories.DbCommand/VB/source.vb#1)]  
  
## <a name="handling-data-errors-with-dbexception"></a><span data-ttu-id="09a10-116">使用 DbException 处理数据错误</span><span class="sxs-lookup"><span data-stu-id="09a10-116">Handling Data Errors with DbException</span></span>  

 <span data-ttu-id="09a10-117"><xref:System.Data.Common.DbException> 类是代表数据源引发的所有异常的基类。</span><span class="sxs-lookup"><span data-stu-id="09a10-117">The <xref:System.Data.Common.DbException> class is the base class for all exceptions thrown on behalf of a data source.</span></span> <span data-ttu-id="09a10-118">你可以在异常处理代码中使用该类来处理由各种提供程序引发的异常，而不必引用特定异常类。</span><span class="sxs-lookup"><span data-stu-id="09a10-118">You can use it in your exception handling code to handle exceptions thrown by different providers without having to reference a specific exception class.</span></span> <span data-ttu-id="09a10-119">下面的代码段演示如何使用 <xref:System.Data.Common.DbException> 来显示使用 <xref:System.Exception.GetType%2A>、<xref:System.Exception.Source%2A>、<xref:System.Runtime.InteropServices.ExternalException.ErrorCode%2A> 和 <xref:System.Exception.Message%2A> 属性的数据源返回的错误信息。</span><span class="sxs-lookup"><span data-stu-id="09a10-119">The following code fragment demonstrates how to use <xref:System.Data.Common.DbException> to display error information returned by the data source using <xref:System.Exception.GetType%2A>, <xref:System.Exception.Source%2A>, <xref:System.Runtime.InteropServices.ExternalException.ErrorCode%2A>, and <xref:System.Exception.Message%2A> properties.</span></span> <span data-ttu-id="09a10-120">输出将显示错误类型、指示提供程序名称的源、错误代码以及与错误相关的消息。</span><span class="sxs-lookup"><span data-stu-id="09a10-120">The output will display the type of error, the source indicating the provider name, an error code, and the message associated with the error.</span></span>  
  
```vb  
Try  
    ' Do work here.  
Catch ex As DbException  
    ' Display information about the exception.  
    Console.WriteLine("GetType: {0}", ex.GetType())  
    Console.WriteLine("Source: {0}", ex.Source)  
    Console.WriteLine("ErrorCode: {0}", ex.ErrorCode)  
    Console.WriteLine("Message: {0}", ex.Message)  
Finally  
    ' Perform cleanup here.  
End Try  
```  
  
```csharp  
try  
{  
    // Do work here.  
}  
catch (DbException ex)  
{  
    // Display information about the exception.  
    Console.WriteLine("GetType: {0}", ex.GetType());  
    Console.WriteLine("Source: {0}", ex.Source);  
    Console.WriteLine("ErrorCode: {0}", ex.ErrorCode);  
    Console.WriteLine("Message: {0}", ex.Message);  
}  
finally  
{  
    // Perform cleanup here.  
}  
```  
  
## <a name="see-also"></a><span data-ttu-id="09a10-121">另请参阅</span><span class="sxs-lookup"><span data-stu-id="09a10-121">See also</span></span>

- [<span data-ttu-id="09a10-122">DbProviderFactories</span><span class="sxs-lookup"><span data-stu-id="09a10-122">DbProviderFactories</span></span>](dbproviderfactories.md)
- [<span data-ttu-id="09a10-123">获取 DbProviderFactory</span><span class="sxs-lookup"><span data-stu-id="09a10-123">Obtaining a DbProviderFactory</span></span>](obtaining-a-dbproviderfactory.md)
- [<span data-ttu-id="09a10-124">使用 DbDataAdapter 修改数据</span><span class="sxs-lookup"><span data-stu-id="09a10-124">Modifying Data with a DbDataAdapter</span></span>](modifying-data-with-a-dbdataadapter.md)
- [<span data-ttu-id="09a10-125">ADO.NET 概述</span><span class="sxs-lookup"><span data-stu-id="09a10-125">ADO.NET Overview</span></span>](ado-net-overview.md)
