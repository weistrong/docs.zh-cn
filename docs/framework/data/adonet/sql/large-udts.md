---
description: 了解详细信息：大型 Udt
title: 大型 UDT
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 420ae24e-762b-4e09-b4c3-2112c470ee49
ms.openlocfilehash: e1a40330bb48d6320dc96533e764f1b856e0f410
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99663178"
---
# <a name="large-udts"></a><span data-ttu-id="9ed71-103">大型 UDT</span><span class="sxs-lookup"><span data-stu-id="9ed71-103">Large UDTs</span></span>

<span data-ttu-id="9ed71-104">用户定义类型 (UDT) 使开发人员可以通过在 SQL Server 数据库中存储公共语言运行时 (CLR) 对象来扩展服务器的标量类型系统。</span><span class="sxs-lookup"><span data-stu-id="9ed71-104">User-defined types (UDTs) allow a developer to extend the server's scalar type system by storing common language runtime (CLR) objects in a SQL Server database.</span></span> <span data-ttu-id="9ed71-105">UDT 可以包含多个元素，也可以具有多种行为，不同于传统的由单个 SQL Server 系统数据类型组成的别名数据类型。</span><span class="sxs-lookup"><span data-stu-id="9ed71-105">UDTs can contain multiple elements and can have behaviors, unlike the traditional alias data types, which consist of a single SQL Server system data type.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="9ed71-106">必须安装 .NET Framework 3.5 SP1（或更高版本）才能利用针对大型 UDT 增强的 SqlClient 支持。</span><span class="sxs-lookup"><span data-stu-id="9ed71-106">You must install the .NET Framework 3.5 SP1 (or later) to take advantage of the enhanced SqlClient support for large UDTs.</span></span>  
  
 <span data-ttu-id="9ed71-107">以前 UDT 的最大大小限制为 8 KB。</span><span class="sxs-lookup"><span data-stu-id="9ed71-107">Previously, UDTs were restricted to a maximum size of 8 kilobytes.</span></span> <span data-ttu-id="9ed71-108">在 SQL Server 2008 中，对于 <xref:Microsoft.SqlServer.Server.Format.UserDefined> 格式的 UDT，已不再进行此限制。</span><span class="sxs-lookup"><span data-stu-id="9ed71-108">In SQL Server 2008, this restriction has been removed for UDTs that have a format of <xref:Microsoft.SqlServer.Server.Format.UserDefined>.</span></span>  
  
 <span data-ttu-id="9ed71-109">有关用户定义类型的完整文档，请参见与您所使用的 SQL Server 版本对应的 SQL Server 联机丛书。</span><span class="sxs-lookup"><span data-stu-id="9ed71-109">For the complete documentation for user-defined types, see the version of SQL Server Books Online for the version of SQL Server you are using.</span></span>  
  
 <span data-ttu-id="9ed71-110">**SQL Server 文档**</span><span class="sxs-lookup"><span data-stu-id="9ed71-110">**SQL Server documentation**</span></span>  
  
1. [<span data-ttu-id="9ed71-111">CLR 用户定义的类型</span><span class="sxs-lookup"><span data-stu-id="9ed71-111">CLR User-Defined Types</span></span>](/sql/relational-databases/clr-integration-database-objects-user-defined-types/clr-user-defined-types)  
  
## <a name="retrieving-udt-schemas-using-getschema"></a><span data-ttu-id="9ed71-112">使用 GetSchema 检索 UDT 架构</span><span class="sxs-lookup"><span data-stu-id="9ed71-112">Retrieving UDT Schemas Using GetSchema</span></span>  

 <span data-ttu-id="9ed71-113"><xref:System.Data.SqlClient.SqlConnection> 的 <xref:System.Data.SqlClient.SqlConnection.GetSchema%2A> 方法在 <xref:System.Data.DataTable> 中返回数据库架构信息。</span><span class="sxs-lookup"><span data-stu-id="9ed71-113">The <xref:System.Data.SqlClient.SqlConnection.GetSchema%2A> method of <xref:System.Data.SqlClient.SqlConnection> returns database schema information in a <xref:System.Data.DataTable>.</span></span> <span data-ttu-id="9ed71-114">有关详细信息，请参阅 [SQL Server 架构集合](../sql-server-schema-collections.md)。</span><span class="sxs-lookup"><span data-stu-id="9ed71-114">For more information, see [SQL Server Schema Collections](../sql-server-schema-collections.md).</span></span>  
  
### <a name="getschematable-column-values-for-udts"></a><span data-ttu-id="9ed71-115">UDT 的 GetSchemaTable 列值</span><span class="sxs-lookup"><span data-stu-id="9ed71-115">GetSchemaTable Column Values for UDTs</span></span>  

 <span data-ttu-id="9ed71-116"><xref:System.Data.SqlClient.SqlDataReader> 的 <xref:System.Data.SqlClient.SqlDataReader.GetSchemaTable%2A> 方法返回描述列元数据的 <xref:System.Data.DataTable>。</span><span class="sxs-lookup"><span data-stu-id="9ed71-116">The <xref:System.Data.SqlClient.SqlDataReader.GetSchemaTable%2A> method of a <xref:System.Data.SqlClient.SqlDataReader> returns a <xref:System.Data.DataTable> that describes column metadata.</span></span> <span data-ttu-id="9ed71-117">下表描述了 SQL Server 2005 和 SQL Server 2008 之间大型 UDT 的列元数据的区别。</span><span class="sxs-lookup"><span data-stu-id="9ed71-117">The following table describes the differences in the column metadata for large UDTs between SQL Server 2005 and SQL Server 2008.</span></span>  
  
|<span data-ttu-id="9ed71-118">SqlDataReader 列</span><span class="sxs-lookup"><span data-stu-id="9ed71-118">SqlDataReader column</span></span>|<span data-ttu-id="9ed71-119">SQL Server 2005</span><span class="sxs-lookup"><span data-stu-id="9ed71-119">SQL Server 2005</span></span>|<span data-ttu-id="9ed71-120">SQL Server 2008 及更高版本</span><span class="sxs-lookup"><span data-stu-id="9ed71-120">SQL Server 2008 and later</span></span>|  
|--------------------------|---------------------|-------------------------------|  
|`ColumnSize`|<span data-ttu-id="9ed71-121">多种多样</span><span class="sxs-lookup"><span data-stu-id="9ed71-121">Varies</span></span>|<span data-ttu-id="9ed71-122">多种多样</span><span class="sxs-lookup"><span data-stu-id="9ed71-122">Varies</span></span>|  
|`NumericPrecision`|<span data-ttu-id="9ed71-123">255</span><span class="sxs-lookup"><span data-stu-id="9ed71-123">255</span></span>|<span data-ttu-id="9ed71-124">255</span><span class="sxs-lookup"><span data-stu-id="9ed71-124">255</span></span>|  
|`NumericScale`|<span data-ttu-id="9ed71-125">255</span><span class="sxs-lookup"><span data-stu-id="9ed71-125">255</span></span>|<span data-ttu-id="9ed71-126">255</span><span class="sxs-lookup"><span data-stu-id="9ed71-126">255</span></span>|  
|`DataType`|`Byte[]`|<span data-ttu-id="9ed71-127">UDT 实例</span><span class="sxs-lookup"><span data-stu-id="9ed71-127">UDT instance</span></span>|  
|`ProviderSpecificDataType`|`SqlTypes.SqlBinary`|<span data-ttu-id="9ed71-128">UDT 实例</span><span class="sxs-lookup"><span data-stu-id="9ed71-128">UDT instance</span></span>|  
|`ProviderType`|<span data-ttu-id="9ed71-129">21 (`SqlDbType.VarBinary`)</span><span class="sxs-lookup"><span data-stu-id="9ed71-129">21 (`SqlDbType.VarBinary`)</span></span>|<span data-ttu-id="9ed71-130">29 (`SqlDbType.Udt`)</span><span class="sxs-lookup"><span data-stu-id="9ed71-130">29 (`SqlDbType.Udt`)</span></span>|  
|`NonVersionedProviderType`|<span data-ttu-id="9ed71-131">29 (`SqlDbType.Udt`)</span><span class="sxs-lookup"><span data-stu-id="9ed71-131">29 (`SqlDbType.Udt`)</span></span>|<span data-ttu-id="9ed71-132">29 (`SqlDbType.Udt`)</span><span class="sxs-lookup"><span data-stu-id="9ed71-132">29 (`SqlDbType.Udt`)</span></span>|  
|`DataTypeName`|`SqlDbType.VarBinary`|<span data-ttu-id="9ed71-133">以 Database.SchemaName.TypeName 形式指定的由三部分组成的名称。</span><span class="sxs-lookup"><span data-stu-id="9ed71-133">The three part name specified as *Database.SchemaName.TypeName*.</span></span>|  
|`IsLong`|<span data-ttu-id="9ed71-134">多种多样</span><span class="sxs-lookup"><span data-stu-id="9ed71-134">Varies</span></span>|<span data-ttu-id="9ed71-135">多种多样</span><span class="sxs-lookup"><span data-stu-id="9ed71-135">Varies</span></span>|  
  
## <a name="sqldatareader-considerations"></a><span data-ttu-id="9ed71-136">SqlDataReader 注意事项</span><span class="sxs-lookup"><span data-stu-id="9ed71-136">SqlDataReader Considerations</span></span>  

 <span data-ttu-id="9ed71-137"><xref:System.Data.SqlClient.SqlDataReader> 在 SQL Server 2008 中已得到扩展，可支持检索大型 UDT 值。</span><span class="sxs-lookup"><span data-stu-id="9ed71-137">The <xref:System.Data.SqlClient.SqlDataReader> has been extended beginning in SQL Server 2008 to support retrieving large UDT values.</span></span> <span data-ttu-id="9ed71-138"><xref:System.Data.SqlClient.SqlDataReader> 处理多少 UDT 值取决于所使用的 SQL Server 版本以及连接字符串中指定的 `Type System Version`。</span><span class="sxs-lookup"><span data-stu-id="9ed71-138">How large UDT values are processed by a <xref:System.Data.SqlClient.SqlDataReader> depends on the version of SQL Server you are using, as well as on the `Type System Version` specified in the connection string.</span></span> <span data-ttu-id="9ed71-139">有关详细信息，请参阅 <xref:System.Data.SqlClient.SqlConnection.ConnectionString%2A>。</span><span class="sxs-lookup"><span data-stu-id="9ed71-139">For more information, see <xref:System.Data.SqlClient.SqlConnection.ConnectionString%2A>.</span></span>  
  
 <span data-ttu-id="9ed71-140">将 `Type System Version` 设置为 SQL Server 2005 时，以下 <xref:System.Data.SqlClient.SqlDataReader> 方法将返回 <xref:System.Data.SqlTypes.SqlBinary>，而不是 UDT：</span><span class="sxs-lookup"><span data-stu-id="9ed71-140">The following methods of <xref:System.Data.SqlClient.SqlDataReader> will return a <xref:System.Data.SqlTypes.SqlBinary> instead of a UDT when the `Type System Version` is set to SQL Server 2005:</span></span>  
  
- <xref:System.Data.SqlClient.SqlDataReader.GetProviderSpecificFieldType%2A>  
  
- <xref:System.Data.SqlClient.SqlDataReader.GetProviderSpecificValue%2A>  
  
- <xref:System.Data.SqlClient.SqlDataReader.GetProviderSpecificValues%2A>  
  
- <xref:System.Data.SqlClient.SqlDataReader.GetSqlValue%2A>  
  
- <xref:System.Data.SqlClient.SqlDataReader.GetSqlValues%2A>  
  
 <span data-ttu-id="9ed71-141">将 `Type System Version` 设置为 SQL Server 2005 时，以下方法将返回 `Byte[]` 的数组，而不是 UDT：</span><span class="sxs-lookup"><span data-stu-id="9ed71-141">The following methods will return an array of `Byte[]` instead of a UDT when the `Type System Version` is set to SQL Server 2005:</span></span>  
  
- <xref:System.Data.SqlClient.SqlDataReader.GetValue%2A>  
  
- <xref:System.Data.SqlClient.SqlDataReader.GetValues%2A>  
  
 <span data-ttu-id="9ed71-142">注意，未对当前版本的 ADO.NET 执行转换。</span><span class="sxs-lookup"><span data-stu-id="9ed71-142">Note that no conversions are made for the current version of ADO.NET.</span></span>  
  
## <a name="specifying-sqlparameters"></a><span data-ttu-id="9ed71-143">指定 SqlParameters</span><span class="sxs-lookup"><span data-stu-id="9ed71-143">Specifying SqlParameters</span></span>  

 <span data-ttu-id="9ed71-144">已扩展以下 <xref:System.Data.SqlClient.SqlParameter> 属性以适用于大型 UDT。</span><span class="sxs-lookup"><span data-stu-id="9ed71-144">The following <xref:System.Data.SqlClient.SqlParameter> properties have been extended to work with large UDTs.</span></span>  
  
|<span data-ttu-id="9ed71-145">SqlParameter 属性</span><span class="sxs-lookup"><span data-stu-id="9ed71-145">SqlParameter Property</span></span>|<span data-ttu-id="9ed71-146">说明</span><span class="sxs-lookup"><span data-stu-id="9ed71-146">Description</span></span>|  
|---------------------------|-----------------|  
|<xref:System.Data.SqlClient.SqlParameter.Value%2A>|<span data-ttu-id="9ed71-147">获取或设置表示参数值的对象。</span><span class="sxs-lookup"><span data-stu-id="9ed71-147">Gets or sets an object that represents the value of the parameter.</span></span> <span data-ttu-id="9ed71-148">默认值为 NULL。</span><span class="sxs-lookup"><span data-stu-id="9ed71-148">The default is null.</span></span> <span data-ttu-id="9ed71-149">此属性可以是 `SqlBinary`、`Byte[]` 或托管对象。</span><span class="sxs-lookup"><span data-stu-id="9ed71-149">The property can be `SqlBinary`, `Byte[]`, or a managed object.</span></span>|  
|<xref:System.Data.SqlClient.SqlParameter.SqlValue%2A>|<span data-ttu-id="9ed71-150">获取或设置表示参数值的对象。</span><span class="sxs-lookup"><span data-stu-id="9ed71-150">Gets or sets an object that represents the value of the parameter.</span></span> <span data-ttu-id="9ed71-151">默认值为 NULL。</span><span class="sxs-lookup"><span data-stu-id="9ed71-151">The default is null.</span></span> <span data-ttu-id="9ed71-152">此属性可以是 `SqlBinary`、`Byte[]` 或托管对象。</span><span class="sxs-lookup"><span data-stu-id="9ed71-152">The property can be `SqlBinary`, `Byte[]`, or a managed object.</span></span>|  
|<xref:System.Data.SqlClient.SqlParameter.Size%2A>|<span data-ttu-id="9ed71-153">获取或设置要解析的参数值的大小。</span><span class="sxs-lookup"><span data-stu-id="9ed71-153">Gets or sets the size of the parameter value to resolve.</span></span> <span data-ttu-id="9ed71-154">默认值为 0。</span><span class="sxs-lookup"><span data-stu-id="9ed71-154">The default value is 0.</span></span> <span data-ttu-id="9ed71-155">此属性可以是一个表示参数值大小的整数。</span><span class="sxs-lookup"><span data-stu-id="9ed71-155">The property can be an integer that represents the size of the parameter value.</span></span> <span data-ttu-id="9ed71-156">对于大型 UDT，此属性可以是 UDT 的实际大小，也可以是 -1，表示未知。</span><span class="sxs-lookup"><span data-stu-id="9ed71-156">For large UDTs, it can be the actual size of the UDT, or -1 for unknown.</span></span>|  
  
## <a name="retrieving-data-example"></a><span data-ttu-id="9ed71-157">检索数据示例</span><span class="sxs-lookup"><span data-stu-id="9ed71-157">Retrieving Data Example</span></span>  

 <span data-ttu-id="9ed71-158">下面的代码段演示如何检索大型 UDT 数据。</span><span class="sxs-lookup"><span data-stu-id="9ed71-158">The following code fragment demonstrates how to retrieve large UDT data.</span></span> <span data-ttu-id="9ed71-159">`connectionString` 变量假定到 SQL Server 数据库的连接有效，而 `commandString` 变量假定 SELECT 语句有效，其中主键列在最前面。</span><span class="sxs-lookup"><span data-stu-id="9ed71-159">The `connectionString` variable assumes a valid connection to a SQL Server database and the `commandString` variable assumes a valid SELECT statement with the primary key column listed first.</span></span>  
  
```csharp  
using (SqlConnection connection = new SqlConnection(
    connectionString, commandString))  
{  
  connection.Open();  
  SqlCommand command = new SqlCommand(commandString);  
  SqlDataReader reader = command.ExecuteReader();  
  while (reader.Read())  
  {  
    // Retrieve the value of the Primary Key column.  
    int id = reader.GetInt32(0);  
  
    // Retrieve the value of the UDT.  
    LargeUDT udt = (LargeUDT)reader[1];  
  
    // You can also use GetSqlValue and GetValue.  
    // LargeUDT udt = (LargeUDT)reader.GetSqlValue(1);  
    // LargeUDT udt = (LargeUDT)reader.GetValue(1);  
  
    Console.WriteLine(  
     "ID={0} LargeUDT={1}", id, udt);  
  }  
reader.close  
}  
```  
  
```vb  
Using connection As New SqlConnection( _  
    connectionString, commandString)  
    connection.Open()  
    Dim command As New SqlCommand(commandString, connection)  
    Dim reader As SqlDataReader  
    reader = command.ExecuteReader  
  
    While reader.Read()  
      ' Retrieve the value of the Primary Key column.  
      Dim id As Int32 = reader.GetInt32(0)  
  
      ' Retrieve the value of the UDT.  
      Dim udt As LargeUDT = CType(reader(1), LargeUDT)  
  
     ' You can also use GetSqlValue and GetValue.  
     ' Dim udt As LargeUDT = CType(reader.GetSqlValue(1), LargeUDT)  
     ' Dim udt As LargeUDT = CType(reader.GetValue(1), LargeUDT)  
  
      ' Print values.  
      Console.WriteLine("ID={0} LargeUDT={1}", id, udt)  
    End While  
    reader.Close()  
End Using  
```  
  
## <a name="see-also"></a><span data-ttu-id="9ed71-160">请参阅</span><span class="sxs-lookup"><span data-stu-id="9ed71-160">See also</span></span>

- [<span data-ttu-id="9ed71-161">配置参数和参数数据类型</span><span class="sxs-lookup"><span data-stu-id="9ed71-161">Configuring Parameters and Parameter Data Types</span></span>](../configuring-parameters-and-parameter-data-types.md)
- [<span data-ttu-id="9ed71-162">检索数据库架构信息</span><span class="sxs-lookup"><span data-stu-id="9ed71-162">Retrieving Database Schema Information</span></span>](../retrieving-database-schema-information.md)
- [<span data-ttu-id="9ed71-163">SQL Server 数据类型映射</span><span class="sxs-lookup"><span data-stu-id="9ed71-163">SQL Server Data Type Mappings</span></span>](../sql-server-data-type-mappings.md)
- [<span data-ttu-id="9ed71-164">SQL Server 二进制和大值数据</span><span class="sxs-lookup"><span data-stu-id="9ed71-164">SQL Server Binary and Large-Value Data</span></span>](sql-server-binary-and-large-value-data.md)
- [<span data-ttu-id="9ed71-165">ADO.NET 概述</span><span class="sxs-lookup"><span data-stu-id="9ed71-165">ADO.NET Overview</span></span>](../ado-net-overview.md)
