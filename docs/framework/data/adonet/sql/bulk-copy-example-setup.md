---
description: 了解详细信息：大容量复制示例设置
title: 批量复制示例设置
ms.date: 03/30/2017
ms.assetid: d4dde6ac-b8b6-4593-965a-635c8fb2dadb
ms.openlocfilehash: ae05dfa5f1ab19a3021b2b79ecd2bbee6a3ecae1
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99718546"
---
# <a name="bulk-copy-example-setup"></a><span data-ttu-id="d0cd0-103">批量复制示例设置</span><span class="sxs-lookup"><span data-stu-id="d0cd0-103">Bulk Copy Example Setup</span></span>

<span data-ttu-id="d0cd0-104"><xref:System.Data.SqlClient.SqlBulkCopy> 类可用于只将数据写入 SQL Server 表。</span><span class="sxs-lookup"><span data-stu-id="d0cd0-104">The <xref:System.Data.SqlClient.SqlBulkCopy> class can be used to write data only to SQL Server tables.</span></span> <span data-ttu-id="d0cd0-105">本主题中所示的代码示例使用 SQL Server 示例数据库 AdventureWorks  。</span><span class="sxs-lookup"><span data-stu-id="d0cd0-105">The code samples shown in this topic use the SQL Server sample database, **AdventureWorks**.</span></span> <span data-ttu-id="d0cd0-106">为避免改变现有表，代码示例将数据写入必须一开始就创建的表中。</span><span class="sxs-lookup"><span data-stu-id="d0cd0-106">To avoid altering the existing tables code samples write data to tables that you must create first.</span></span>  
  
 <span data-ttu-id="d0cd0-107">BulkCopyDemoMatchingColumns 表和 BulkCopyDemoDifferentColumns 表均基于 AdventureWorks Production.Products 表     。</span><span class="sxs-lookup"><span data-stu-id="d0cd0-107">The **BulkCopyDemoMatchingColumns** and **BulkCopyDemoDifferentColumns** tables are both based on the **AdventureWorks** **Production.Products** table.</span></span> <span data-ttu-id="d0cd0-108">在使用这些表的代码示例中，将数据从 Production.Products 表添加到其中一个示例表  。</span><span class="sxs-lookup"><span data-stu-id="d0cd0-108">In code samples that use these tables, data is added from the **Production.Products** table to one of these sample tables.</span></span> <span data-ttu-id="d0cd0-109">在该示例说明如何将列从源数据映射到目标表时，使用 BulkCopyDemoDifferentColumns 表；BulkCopyDemoMatchingColumns 适用于大多数其他示例   。</span><span class="sxs-lookup"><span data-stu-id="d0cd0-109">The **BulkCopyDemoDifferentColumns** table is used when the sample illustrates how to map columns from the source data to the destination table; **BulkCopyDemoMatchingColumns** is used for most other samples.</span></span>  
  
 <span data-ttu-id="d0cd0-110">多个代码示例演示如何使用一个 <xref:System.Data.SqlClient.SqlBulkCopy> 类写入多个表。</span><span class="sxs-lookup"><span data-stu-id="d0cd0-110">A few of the code samples demonstrate how to use one <xref:System.Data.SqlClient.SqlBulkCopy> class to write to multiple tables.</span></span> <span data-ttu-id="d0cd0-111">对于这些示例，BulkCopyDemoOrderHeader 和 BulkCopyDemoOrderDetail 表将用作目标表   。</span><span class="sxs-lookup"><span data-stu-id="d0cd0-111">For these samples, the **BulkCopyDemoOrderHeader** and **BulkCopyDemoOrderDetail** tables are used as the destination tables.</span></span> <span data-ttu-id="d0cd0-112">这些表基于 AdventureWorks 中的 Sales.SalesOrderHeader 和 Sales.SalesOrderDetail 表    。</span><span class="sxs-lookup"><span data-stu-id="d0cd0-112">These tables are based on the **Sales.SalesOrderHeader** and **Sales.SalesOrderDetail** tables in **AdventureWorks**.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="d0cd0-113">提供 SqlBulkCopy 代码示例是为了演示仅使用 SqlBulkCopy 时的语法   。</span><span class="sxs-lookup"><span data-stu-id="d0cd0-113">The **SqlBulkCopy** code samples are provided to demonstrate the syntax for using **SqlBulkCopy** only.</span></span> <span data-ttu-id="d0cd0-114">如果源表和目标表位于同一 SQL Server 实例中，可以更便捷地使用 Transact-SQL `INSERT … SELECT` 语句复制数据。</span><span class="sxs-lookup"><span data-stu-id="d0cd0-114">If the source and destination tables are located in the same SQL Server instance, it is easier and faster to use a Transact-SQL `INSERT … SELECT` statement to copy the data.</span></span>  
  
## <a name="table-setup"></a><span data-ttu-id="d0cd0-115">表设置</span><span class="sxs-lookup"><span data-stu-id="d0cd0-115">Table Setup</span></span>  

 <span data-ttu-id="d0cd0-116">若要创建正确运行代码示例所需的表，必须在 SQL Server 数据库中运行以下 Transact-SQL 语句。</span><span class="sxs-lookup"><span data-stu-id="d0cd0-116">To create the tables necessary for the code samples to run correctly, you must run the following Transact-SQL statements in a SQL Server database.</span></span>  
  
```sql
USE AdventureWorks  
  
IF EXISTS (SELECT * FROM dbo.sysobjects
 WHERE id = object_id(N'[dbo].[BulkCopyDemoMatchingColumns]')  
 AND OBJECTPROPERTY(id, N'IsUserTable') = 1)  
    DROP TABLE [dbo].[BulkCopyDemoMatchingColumns]  
  
CREATE TABLE [dbo].[BulkCopyDemoMatchingColumns]([ProductID] [int] IDENTITY(1,1) NOT NULL,  
    [Name] [nvarchar](50) NOT NULL,  
    [ProductNumber] [nvarchar](25) NOT NULL,  
 CONSTRAINT [PK_ProductID] PRIMARY KEY CLUSTERED  
(  
    [ProductID] ASC  
) ON [PRIMARY]) ON [PRIMARY]  
  
IF EXISTS (SELECT * FROM dbo.sysobjects
 WHERE id = object_id(N'[dbo].[BulkCopyDemoDifferentColumns]')  
 AND OBJECTPROPERTY(id, N'IsUserTable') = 1)  
    DROP TABLE [dbo].[BulkCopyDemoDifferentColumns]  
  
CREATE TABLE [dbo].[BulkCopyDemoDifferentColumns]([ProdID] [int] IDENTITY(1,1) NOT NULL,  
    [ProdNum] [nvarchar](25) NOT NULL,  
    [ProdName] [nvarchar](50) NOT NULL,  
 CONSTRAINT [PK_ProdID] PRIMARY KEY CLUSTERED  
(  
    [ProdID] ASC  
) ON [PRIMARY]) ON [PRIMARY]  
  
IF EXISTS (SELECT * FROM dbo.sysobjects
 WHERE id = object_id(N'[dbo].[BulkCopyDemoOrderHeader]')  
 AND OBJECTPROPERTY(id, N'IsUserTable') = 1)  
    DROP TABLE [dbo].[BulkCopyDemoOrderHeader]  
  
CREATE TABLE [dbo].[BulkCopyDemoOrderHeader]([SalesOrderID] [int] IDENTITY(1,1) NOT NULL,  
    [OrderDate] [datetime] NOT NULL,  
    [AccountNumber] [nvarchar](15) NULL,  
 CONSTRAINT [PK_SalesOrderID] PRIMARY KEY CLUSTERED  
(  
    [SalesOrderID] ASC  
) ON [PRIMARY]) ON [PRIMARY]  
  
IF EXISTS (SELECT * FROM dbo.sysobjects
 WHERE id = object_id(N'[dbo].[BulkCopyDemoOrderDetail]')  
 AND OBJECTPROPERTY(id, N'IsUserTable') = 1)  
    DROP TABLE [dbo].[BulkCopyDemoOrderDetail]  
  
CREATE TABLE [dbo].[BulkCopyDemoOrderDetail]([SalesOrderID] [int] NOT NULL,  
    [SalesOrderDetailID] [int] NOT NULL,  
    [OrderQty] [smallint] NOT NULL,  
    [ProductID] [int] NOT NULL,  
    [UnitPrice] [money] NOT NULL,  
 CONSTRAINT [PK_LineNumber] PRIMARY KEY CLUSTERED  
(  
    [SalesOrderID] ASC,  
    [SalesOrderDetailID] ASC  
) ON [PRIMARY]) ON [PRIMARY]  
```  
  
## <a name="see-also"></a><span data-ttu-id="d0cd0-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="d0cd0-117">See also</span></span>

- [<span data-ttu-id="d0cd0-118">SQL Server 中的大容量复制操作</span><span class="sxs-lookup"><span data-stu-id="d0cd0-118">Bulk Copy Operations in SQL Server</span></span>](bulk-copy-operations-in-sql-server.md)
- [<span data-ttu-id="d0cd0-119">ADO.NET 概述</span><span class="sxs-lookup"><span data-stu-id="d0cd0-119">ADO.NET Overview</span></span>](../ado-net-overview.md)
