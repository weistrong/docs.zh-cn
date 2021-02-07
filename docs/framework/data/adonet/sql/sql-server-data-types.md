---
description: 了解详细信息： SQL Server 数据类型和 ADO.NET
title: SQL Server 数据类型和 ADO.NET
titleSuffix: ''
ms.date: 03/30/2017
ms.assetid: 81b43550-23e8-43bb-b460-7eb8ac825c33
ms.openlocfilehash: 841fa5864bf54b5e4fc4dc24dab64e6ac1435c7e
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99767292"
---
# <a name="sql-server-data-types-and-adonet"></a><span data-ttu-id="a2cd3-103">SQL Server 数据类型和 ADO.NET</span><span class="sxs-lookup"><span data-stu-id="a2cd3-103">SQL Server Data Types and ADO.NET</span></span>

<span data-ttu-id="a2cd3-104">SQL Server 和 .NET Framework 基于不同的类型系统，这可导致潜在的数据丢失。</span><span class="sxs-lookup"><span data-stu-id="a2cd3-104">SQL Server and the .NET Framework are based on different type systems, which can result in potential data loss.</span></span> <span data-ttu-id="a2cd3-105">为了保持数据的完整性，适用于 SQL Server 的 .NET Framework 数据提供程序 (<xref:System.Data.SqlClient>) 提供了用于处理 SQL Server 数据的类型化访问器方法。</span><span class="sxs-lookup"><span data-stu-id="a2cd3-105">To preserve data integrity, the .NET Framework Data Provider for SQL Server (<xref:System.Data.SqlClient>) provides typed accessor methods for working with SQL Server data.</span></span> <span data-ttu-id="a2cd3-106">可以使用 <xref:System.Data.SqlDbType> 类中的枚举来指定 <xref:System.Data.SqlClient.SqlParameter> 数据类型。</span><span class="sxs-lookup"><span data-stu-id="a2cd3-106">You can use the enumerations in the <xref:System.Data.SqlDbType> classes to specify <xref:System.Data.SqlClient.SqlParameter> data types.</span></span>  
  
 <span data-ttu-id="a2cd3-107">有关 SQL Server 和 .NET Framework 数据类型之间的数据类型映射的详细信息和表，请参阅 [SQL Server 数据类型映射](../sql-server-data-type-mappings.md)。</span><span class="sxs-lookup"><span data-stu-id="a2cd3-107">For more information and a table that describes the data type mappings between SQL Server and .NET Framework data types, see [SQL Server Data Type Mappings](../sql-server-data-type-mappings.md).</span></span>  
  
 <span data-ttu-id="a2cd3-108">SQL Server 2008 引入了新的数据类型，这些数据类型旨在满足企业使用日期和时间数据、结构化数据、半结构化数据和非结构化数据的需求。</span><span class="sxs-lookup"><span data-stu-id="a2cd3-108">SQL Server 2008 introduces new data types that are designed to meet business needs to work with date and time, structured, semi-structured, and unstructured data.</span></span> <span data-ttu-id="a2cd3-109">相关文档位于 SQL Server 2008 联机丛书中。</span><span class="sxs-lookup"><span data-stu-id="a2cd3-109">These are documented in SQL Server 2008 Books Online.</span></span>  
  
 <span data-ttu-id="a2cd3-110">可在应用程序中使用的 SQL Server 数据类型取决于使用的 SQL Server 版本。</span><span class="sxs-lookup"><span data-stu-id="a2cd3-110">The SQL Server data types that are available for use in your application depends on the version of SQL Server that you are using.</span></span> <span data-ttu-id="a2cd3-111">有关更多信息，请参见下表中的相关版本的 SQL Server 联机丛书。</span><span class="sxs-lookup"><span data-stu-id="a2cd3-111">For more information, see the relevant version of SQL Server Books Online in the following table.</span></span>  
  
 <span data-ttu-id="a2cd3-112">**SQL Server 文档**</span><span class="sxs-lookup"><span data-stu-id="a2cd3-112">**SQL Server documentation**</span></span>  
  
1. [<span data-ttu-id="a2cd3-113">数据类型 (Transact-SQL)</span><span class="sxs-lookup"><span data-stu-id="a2cd3-113">Data Types (Transact-SQL)</span></span>](/sql/t-sql/data-types/data-types-transact-sql)  
  
## <a name="in-this-section"></a><span data-ttu-id="a2cd3-114">本节内容</span><span class="sxs-lookup"><span data-stu-id="a2cd3-114">In This Section</span></span>  

 [<span data-ttu-id="a2cd3-115">SqlTypes 和数据集</span><span class="sxs-lookup"><span data-stu-id="a2cd3-115">SqlTypes and the DataSet</span></span>](sqltypes-and-the-dataset.md)  
 <span data-ttu-id="a2cd3-116">介绍对 `DataSet` 中 `SqlTypes` 的类型支持。</span><span class="sxs-lookup"><span data-stu-id="a2cd3-116">Describes type support for `SqlTypes` in the `DataSet`.</span></span>  
  
 [<span data-ttu-id="a2cd3-117">处理 Null 值</span><span class="sxs-lookup"><span data-stu-id="a2cd3-117">Handling Null Values</span></span>](handling-null-values.md)  
 <span data-ttu-id="a2cd3-118">演示如何处理 null 值和三值逻辑。</span><span class="sxs-lookup"><span data-stu-id="a2cd3-118">Demonstrates how to work with null values and three-valued logic.</span></span>  
  
 [<span data-ttu-id="a2cd3-119">比较 GUID 和 uniqueidentifier 值</span><span class="sxs-lookup"><span data-stu-id="a2cd3-119">Comparing GUID and uniqueidentifier Values</span></span>](comparing-guid-and-uniqueidentifier-values.md)  
 <span data-ttu-id="a2cd3-120">演示如何在 SQL Server 和 .NET Framework 中使用 GUID 和 uniqueidentifier 值。</span><span class="sxs-lookup"><span data-stu-id="a2cd3-120">Demonstrates how to work with GUID and uniqueidentifier values in SQL Server and the .NET Framework.</span></span>  
  
 [<span data-ttu-id="a2cd3-121">日期和时间数据</span><span class="sxs-lookup"><span data-stu-id="a2cd3-121">Date and Time Data</span></span>](date-and-time-data.md)  
 <span data-ttu-id="a2cd3-122">介绍如何使用在 SQL Server 2008 中引入的新的日期和时间数据类型。</span><span class="sxs-lookup"><span data-stu-id="a2cd3-122">Describes how to use the new date and time data types introduced in SQL Server 2008.</span></span>  
  
 [<span data-ttu-id="a2cd3-123">大型 UDT</span><span class="sxs-lookup"><span data-stu-id="a2cd3-123">Large UDTs</span></span>](large-udts.md)  
 <span data-ttu-id="a2cd3-124">演示如何通过 SQL Server 2008 中引入的大型值 UDT 检索数据。</span><span class="sxs-lookup"><span data-stu-id="a2cd3-124">Demonstrates how to retrieve data from large value UDTs introduced in SQL Server 2008.</span></span>  
  
 [<span data-ttu-id="a2cd3-125">SQL Server 中的 XML 数据</span><span class="sxs-lookup"><span data-stu-id="a2cd3-125">XML Data in SQL Server</span></span>](xml-data-in-sql-server.md)  
 <span data-ttu-id="a2cd3-126">介绍如何使用从 SQL Server 检索的 XML 数据。</span><span class="sxs-lookup"><span data-stu-id="a2cd3-126">Describes how to work with XML data retrieved from SQL Server.</span></span>  
  
## <a name="reference"></a><span data-ttu-id="a2cd3-127">参考</span><span class="sxs-lookup"><span data-stu-id="a2cd3-127">Reference</span></span>  

 <xref:System.Data.DataSet>  
 <span data-ttu-id="a2cd3-128">介绍 `DataSet` 类及其所有成员。</span><span class="sxs-lookup"><span data-stu-id="a2cd3-128">Describes the `DataSet` class and all of its members.</span></span>  
  
 <xref:System.Data.SqlTypes>  
 <span data-ttu-id="a2cd3-129">介绍 `SqlTypes` 命名空间及其所有成员。</span><span class="sxs-lookup"><span data-stu-id="a2cd3-129">Describes the `SqlTypes` namespace and all of its members.</span></span>  
  
 <xref:System.Data.SqlDbType>  
 <span data-ttu-id="a2cd3-130">介绍 `SqlDbType` 枚举及其所有成员。</span><span class="sxs-lookup"><span data-stu-id="a2cd3-130">Describes the `SqlDbType` enumeration and all of its members.</span></span>  
  
 <xref:System.Data.DbType>  
 <span data-ttu-id="a2cd3-131">介绍 `DbType` 枚举及其所有成员。</span><span class="sxs-lookup"><span data-stu-id="a2cd3-131">Describes the `DbType` enumeration and all of its members.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a2cd3-132">请参阅</span><span class="sxs-lookup"><span data-stu-id="a2cd3-132">See also</span></span>

- [<span data-ttu-id="a2cd3-133">SQL Server 数据类型映射</span><span class="sxs-lookup"><span data-stu-id="a2cd3-133">SQL Server Data Type Mappings</span></span>](../sql-server-data-type-mappings.md)
- [<span data-ttu-id="a2cd3-134">配置参数和参数数据类型</span><span class="sxs-lookup"><span data-stu-id="a2cd3-134">Configuring Parameters and Parameter Data Types</span></span>](../configuring-parameters-and-parameter-data-types.md)
- [<span data-ttu-id="a2cd3-135">表值参数</span><span class="sxs-lookup"><span data-stu-id="a2cd3-135">Table-Valued Parameters</span></span>](table-valued-parameters.md)
- [<span data-ttu-id="a2cd3-136">SQL Server 二进制和大值数据</span><span class="sxs-lookup"><span data-stu-id="a2cd3-136">SQL Server Binary and Large-Value Data</span></span>](sql-server-binary-and-large-value-data.md)
- [<span data-ttu-id="a2cd3-137">ADO.NET 概述</span><span class="sxs-lookup"><span data-stu-id="a2cd3-137">ADO.NET Overview</span></span>](../ado-net-overview.md)
