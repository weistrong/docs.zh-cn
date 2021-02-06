---
description: 了解详细信息：检索数据库架构信息
title: 检索数据库架构信息
ms.date: 03/30/2017
ms.assetid: 79038d52-f122-4fd4-9bfb-aaa22d6a114b
ms.openlocfilehash: 84ac94a72b23d0b1d6924600f2fd33b2a285eab8
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99663399"
---
# <a name="retrieving-database-schema-information"></a><span data-ttu-id="1b1cc-103">检索数据库架构信息</span><span class="sxs-lookup"><span data-stu-id="1b1cc-103">Retrieving Database Schema Information</span></span>

<span data-ttu-id="1b1cc-104">从数据库获取架构信息通过架构发现过程来完成。</span><span class="sxs-lookup"><span data-stu-id="1b1cc-104">Obtaining schema information from a database is accomplished with the process of schema discovery.</span></span> <span data-ttu-id="1b1cc-105">通过架构发现，应用程序可以请求托管提供程序查找并返回有关给定数据库的数据库架构（也称为元数据）名称的信息。</span><span class="sxs-lookup"><span data-stu-id="1b1cc-105">Schema discovery allows applications to request that managed providers find and return information about the database schema, also known as *metadata*, of a given database.</span></span> <span data-ttu-id="1b1cc-106">不同的数据库架构元素（例如表、列和存储过程）通过架构集合进行公开。</span><span class="sxs-lookup"><span data-stu-id="1b1cc-106">Different database schema elements such as tables, columns, and stored-procedures are exposed through schema collections.</span></span> <span data-ttu-id="1b1cc-107">每个架构集合包含所使用的提供程序特定的各种架构信息。</span><span class="sxs-lookup"><span data-stu-id="1b1cc-107">Each schema collection contains a variety of schema information specific to the provider being used.</span></span>  
  
 <span data-ttu-id="1b1cc-108">每个 .NET Framework 托管提供程序都实现 **连接** 类中的 **GetSchema** 方法， **GetSchema** 方法返回的架构信息采用的形式 <xref:System.Data.DataTable> 。</span><span class="sxs-lookup"><span data-stu-id="1b1cc-108">Each of the .NET Framework managed providers implement the **GetSchema** method in the **Connection** class, and the schema information that is returned from the **GetSchema** method comes in the form of a <xref:System.Data.DataTable>.</span></span> <span data-ttu-id="1b1cc-109">GetSchema 方法属于重载方法，提供可选的参数来指定要返回的架构集合以及限制返回的信息量。</span><span class="sxs-lookup"><span data-stu-id="1b1cc-109">The **GetSchema** method is an overloaded method that provides optional parameters for specifying the schema collection to return, and restricting the amount of information returned.</span></span>  
  
 <span data-ttu-id="1b1cc-110">用于 OLE DB、ODBC、Oracle 和 SqlClient 的 .NET Framework 数据提供程序提供了一个 **GetSchemaTable** 方法，该方法可返回描述 **DataReader** 的列元数据的 DataTable。</span><span class="sxs-lookup"><span data-stu-id="1b1cc-110">The .NET Framework Data Providers for OLE DB, ODBC, Oracle, and SqlClient provide a **GetSchemaTable** method that returns a DataTable describing the column metadata of the **DataReader**.</span></span>  
  
 <span data-ttu-id="1b1cc-111">适用于 OLE DB 的 .NET Framework 数据提供程序还使用 <xref:System.Data.OleDb.OleDbConnection.GetOleDbSchemaTable%2A> 对象的 <xref:System.Data.OleDb.OleDbConnection> 方法来公开架构信息。</span><span class="sxs-lookup"><span data-stu-id="1b1cc-111">The .NET Framework Data Provider for OLE DB also exposes schema information by using the <xref:System.Data.OleDb.OleDbConnection.GetOleDbSchemaTable%2A> method of the <xref:System.Data.OleDb.OleDbConnection> object.</span></span> <span data-ttu-id="1b1cc-112">作为参数， **GetOleDbSchemaTable** 采用 <xref:System.Data.OleDb.OleDbSchemaGuid> 标识要返回的架构信息的，以及对那些返回列的限制数组。</span><span class="sxs-lookup"><span data-stu-id="1b1cc-112">As arguments, **GetOleDbSchemaTable** takes an <xref:System.Data.OleDb.OleDbSchemaGuid> that identifies the schema information to return, and an array of restrictions on those returned columns.</span></span> <span data-ttu-id="1b1cc-113">**GetOleDbSchemaTable** 返回 <xref:System.Data.DataTable> 用请求的架构信息填充的。</span><span class="sxs-lookup"><span data-stu-id="1b1cc-113">**GetOleDbSchemaTable** returns a <xref:System.Data.DataTable> populated with the requested schema information.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="1b1cc-114">本节内容</span><span class="sxs-lookup"><span data-stu-id="1b1cc-114">In This Section</span></span>  

 [<span data-ttu-id="1b1cc-115">GetSchema 和架构集合</span><span class="sxs-lookup"><span data-stu-id="1b1cc-115">GetSchema and Schema Collections</span></span>](getschema-and-schema-collections.md)  
 <span data-ttu-id="1b1cc-116">描述 GetSchema 方法以及如何使用该方法从数据库检索和限制架构信息。</span><span class="sxs-lookup"><span data-stu-id="1b1cc-116">Describes the **GetSchema** method and how it can be used to retrieve and restrict schema information from a database.</span></span>  
  
 <span data-ttu-id="1b1cc-117">架构限制</span><span class="sxs-lookup"><span data-stu-id="1b1cc-117">Schema Restrictions</span></span>  
 <span data-ttu-id="1b1cc-118">描述可用于 GetSchema 的架构限制。</span><span class="sxs-lookup"><span data-stu-id="1b1cc-118">Describes schema restrictions that can be used with **GetSchema**.</span></span>  
  
 [<span data-ttu-id="1b1cc-119">公共架构集合</span><span class="sxs-lookup"><span data-stu-id="1b1cc-119">Common Schema Collections</span></span>](common-schema-collections.md)  
 <span data-ttu-id="1b1cc-120">描述所有 .NET Framework 托管提供程序均支持的所有通用架构集合。</span><span class="sxs-lookup"><span data-stu-id="1b1cc-120">Describes all of the common schema collections supported by all of the .NET Framework managed providers.</span></span>  
  
 [<span data-ttu-id="1b1cc-121">SQL Server 架构集合</span><span class="sxs-lookup"><span data-stu-id="1b1cc-121">SQL Server Schema Collections</span></span>](sql-server-schema-collections.md)  
 <span data-ttu-id="1b1cc-122">描述适用于 SQL Server 的 .NET Framework 提供程序支持的架构集合。</span><span class="sxs-lookup"><span data-stu-id="1b1cc-122">Describes the schema collection supported by the .NET Framework provider for SQL Server.</span></span>  
  
 [<span data-ttu-id="1b1cc-123">Oracle 架构集合</span><span class="sxs-lookup"><span data-stu-id="1b1cc-123">Oracle Schema Collections</span></span>](oracle-schema-collections.md)  
 <span data-ttu-id="1b1cc-124">描述适用于 Oracle 的 SQL Server .NET Framework 提供程序支持的架构集合。</span><span class="sxs-lookup"><span data-stu-id="1b1cc-124">Describes the schema collection supported by the .NET Framework provider for Oracle.</span></span>  
  
 [<span data-ttu-id="1b1cc-125">ODBC 架构集合</span><span class="sxs-lookup"><span data-stu-id="1b1cc-125">ODBC Schema Collections</span></span>](odbc-schema-collections.md)  
 <span data-ttu-id="1b1cc-126">描述 ODBC 驱动程序的架构集合。</span><span class="sxs-lookup"><span data-stu-id="1b1cc-126">Describes the schema collections for ODBC drivers.</span></span>  
  
 [<span data-ttu-id="1b1cc-127">OLE DB 架构集合</span><span class="sxs-lookup"><span data-stu-id="1b1cc-127">OLE DB Schema Collections</span></span>](ole-db-schema-collections.md)  
 <span data-ttu-id="1b1cc-128">描述 OLE DB 提供程序的架构集合。</span><span class="sxs-lookup"><span data-stu-id="1b1cc-128">Describes the schema collections for OLE DB providers.</span></span>  
  
## <a name="reference"></a><span data-ttu-id="1b1cc-129">参考</span><span class="sxs-lookup"><span data-stu-id="1b1cc-129">Reference</span></span>  

 <xref:System.Data.Common.DbConnection.GetSchema%2A>  
 <span data-ttu-id="1b1cc-130">描述 <xref:System.Data.Common.DbConnection> 类的 GetSchema 方法。</span><span class="sxs-lookup"><span data-stu-id="1b1cc-130">Describes the **GetSchema** method of the <xref:System.Data.Common.DbConnection> class.</span></span>  
  
 <xref:System.Data.Odbc.OdbcConnection.GetSchema%2A>  
 <span data-ttu-id="1b1cc-131">描述 <xref:System.Data.Odbc.OdbcConnection> 类的 GetSchema 方法。</span><span class="sxs-lookup"><span data-stu-id="1b1cc-131">Describes the **GetSchema** method of the <xref:System.Data.Odbc.OdbcConnection> class.</span></span>  
  
 <xref:System.Data.OleDb.OleDbConnection.GetSchema%2A>  
 <span data-ttu-id="1b1cc-132">描述 <xref:System.Data.OleDb.OleDbConnection> 类的 GetSchema 方法。</span><span class="sxs-lookup"><span data-stu-id="1b1cc-132">Describes the **GetSchema** method of the <xref:System.Data.OleDb.OleDbConnection> class.</span></span>  
  
 <xref:System.Data.OracleClient.OracleConnection.GetSchema%2A>  
 <span data-ttu-id="1b1cc-133">描述 <xref:System.Data.OracleClient.OracleConnection> 类的 GetSchema 方法。</span><span class="sxs-lookup"><span data-stu-id="1b1cc-133">Describes the **GetSchema** method of the <xref:System.Data.OracleClient.OracleConnection> class.</span></span>  
  
 <xref:System.Data.SqlClient.SqlConnection.GetSchema%2A>  
 <span data-ttu-id="1b1cc-134">描述 <xref:System.Data.SqlClient.SqlConnection> 类的 GetSchema 方法。</span><span class="sxs-lookup"><span data-stu-id="1b1cc-134">Describes the **GetSchema** method of the <xref:System.Data.SqlClient.SqlConnection> class.</span></span>  
  
 <xref:System.Data.Common.DbDataReader.GetSchemaTable%2A>  
 <span data-ttu-id="1b1cc-135">描述 <xref:System.Data.Common.DbDataReader> 类的 GetSchemaTable 方法。</span><span class="sxs-lookup"><span data-stu-id="1b1cc-135">Describes the **GetSchemaTable** method of the <xref:System.Data.Common.DbDataReader> class.</span></span>  
  
 <xref:System.Data.Odbc.OdbcDataReader.GetSchemaTable%2A>  
 <span data-ttu-id="1b1cc-136">描述 <xref:System.Data.Odbc.OdbcDataReader> 类的 GetSchemaTable 方法。</span><span class="sxs-lookup"><span data-stu-id="1b1cc-136">Describes the **GetSchemaTable** method of the <xref:System.Data.Odbc.OdbcDataReader> class.</span></span>  
  
 <xref:System.Data.OleDb.OleDbDataReader.GetSchemaTable%2A>  
 <span data-ttu-id="1b1cc-137">描述 <xref:System.Data.OleDb.OleDbDataReader> 类的 GetSchemaTable 方法。</span><span class="sxs-lookup"><span data-stu-id="1b1cc-137">Describes the **GetSchemaTable** method of the <xref:System.Data.OleDb.OleDbDataReader> class.</span></span>  
  
 <xref:System.Data.OracleClient.OracleDataReader.GetSchemaTable%2A>  
 <span data-ttu-id="1b1cc-138">描述 <xref:System.Data.OracleClient.OracleDataReader> 类的 GetSchemaTable 方法。</span><span class="sxs-lookup"><span data-stu-id="1b1cc-138">Describes the **GetSchemaTable** method of the <xref:System.Data.OracleClient.OracleDataReader> class.</span></span>  
  
 <xref:System.Data.SqlClient.SqlDataReader.GetSchemaTable%2A>  
 <span data-ttu-id="1b1cc-139">描述 <xref:System.Data.SqlClient.SqlDataReader> 类的 GetSchemaTable 方法。</span><span class="sxs-lookup"><span data-stu-id="1b1cc-139">Describes the **GetSchemaTable** method of the <xref:System.Data.SqlClient.SqlDataReader> class.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1b1cc-140">请参阅</span><span class="sxs-lookup"><span data-stu-id="1b1cc-140">See also</span></span>

- [<span data-ttu-id="1b1cc-141">在 ADO.NET 中检索和修改数据</span><span class="sxs-lookup"><span data-stu-id="1b1cc-141">Retrieving and Modifying Data in ADO.NET</span></span>](retrieving-and-modifying-data.md)
- [<span data-ttu-id="1b1cc-142">ADO.NET 概述</span><span class="sxs-lookup"><span data-stu-id="1b1cc-142">ADO.NET Overview</span></span>](ado-net-overview.md)
