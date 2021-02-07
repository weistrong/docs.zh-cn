---
description: 了解详细信息：在 ADO.NET 中连接到数据源
title: 连接数据源
deescription: Learn about Connection objects, used to connect to data sources in ADO.NET. The Connection object you choose depends on the type of data source.
ms.date: 03/30/2017
ms.assetid: 9abc3f92-1be3-4e1a-b360-762dc689650e
ms.openlocfilehash: 0bf66b9dc609a704cf89380e2376f50197e047a7
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99663880"
---
# <a name="connecting-to-a-data-source-in-adonet"></a>连接到 ADO.NET 中的数据源

在 ADO.NET 中，通过在连接字符串中提供必要的身份验证信息，使用 **连接** 对象连接到特定数据源。 你使用的 Connection 对象取决于数据源的类型。  
  
 随 .NET Framework 提供的每个 .NET Framework 数据提供程序都具有一个 <xref:System.Data.Common.DbConnection> 对象：适用于 OLE DB 的 .NET Framework 数据提供程序包括一个 <xref:System.Data.OleDb.OleDbConnection> 对象，适用于 SQL Server 的 .NET Framework 数据提供程序包括一个 <xref:System.Data.SqlClient.SqlConnection> 对象，适用于 ODBC 的 .NET Framework 数据提供程序包括一个 <xref:System.Data.Odbc.OdbcConnection> 对象，适用于 Oracle 的 .NET Framework 数据提供程序包括一个 <xref:System.Data.OracleClient.OracleConnection> 对象。  
  
## <a name="in-this-section"></a>本节内容  

 [建立连接](establishing-the-connection.md)\
 说明如何使用 Connection 对象与数据源建立连接。  
  
 [连接事件](connection-events.md)\
 说明如何使用 InfoMessage 事件从数据源中检索信息性消息。  
  
## <a name="see-also"></a>另请参阅

- [连接字符串](connection-strings.md)
- [连接池](connection-pooling.md)
- [命令和参数](commands-and-parameters.md)
- [DataAdapter 和 DataReader](dataadapters-and-datareaders.md)
- [事务和并发](transactions-and-concurrency.md)
- [ADO.NET 概述](ado-net-overview.md)
