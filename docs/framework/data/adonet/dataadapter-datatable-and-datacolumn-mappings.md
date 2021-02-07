---
description: 了解详细信息： DataAdapter DataTable 和 DataColumn 映射
title: DataAdapter 数据表和 DataColumn 映射
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: d023260a-a66a-4c39-b8f4-090cd130e730
ms.openlocfilehash: 25007925afa57dd0cb6e75f808444f1bfaeea9b1
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99739725"
---
# <a name="dataadapter-datatable-and-datacolumn-mappings"></a>DataAdapter 数据表和 DataColumn 映射

**DataAdapter** <xref:System.Data.Common.DataTableMapping> 在其 **TableMappings** 属性中包含零个或多个对象的集合。 **DataTableMapping** 提供了针对数据源的查询返回的数据与之间的主映射 <xref:System.Data.DataTable> 。 可以将 **DataTableMapping** 名称替换为将 **DataTable** 名称替换为 **DataAdapter** 的 **Fill** 方法。 以下示例为 Authors 表创建名为 AuthorsMapping 的 DataTableMapping  。  
  
```vb  
workAdapter.TableMappings.Add("AuthorsMapping", "Authors")  
```  
  
```csharp  
workAdapter.TableMappings.Add("AuthorsMapping", "Authors");  
```  
  
 DataTableMapping 使你能够使用 DataTable 中与数据库中的列名不同的列名 。 当该表被更新时，DataAdapter 将使用此映射来匹配列。  
  
 如果在调用 DataAdapter 的 Fill 或 Update 方法时未指定 TableName 或 DataTableMapping 名称，DataAdapter 将查找名为“Table”的 DataTableMapping      。 如果该 **DataTableMapping** 不存在，则 **DataTable** 的 **TableName** 为 "Table"。 可以通过创建名为“Table”的 DataTableMapping 来指定默认的 DataTableMapping 。  
  
 以下代码示例（从 <xref:System.Data.Common> 命名空间）创建一个 DataTableMapping 并通过将其命名为“Table”来使其成为指定 DataAdapter 的默认映射 。 然后，该示例将查询结果中第一个表（Northwind 数据库的 Customers 表）中的列映射到 <xref:System.Data.DataSet> 的 Northwind Customers 表中的一组更为易记的名称  。 对于未映射的列，将使用数据源中的列名称。  
  
```vb  
Dim mapping As DataTableMapping = _  
  adapter.TableMappings.Add("Table", "NorthwindCustomers")  
mapping.ColumnMappings.Add("CompanyName", "Company")  
mapping.ColumnMappings.Add("ContactName", "Contact")  
mapping.ColumnMappings.Add("PostalCode", "ZIPCode")  
  
adapter.Fill(custDS)  
```  
  
```csharp  
DataTableMapping mapping =
  adapter.TableMappings.Add("Table", "NorthwindCustomers");  
mapping.ColumnMappings.Add("CompanyName", "Company");  
mapping.ColumnMappings.Add("ContactName", "Contact");  
mapping.ColumnMappings.Add("PostalCode", "ZIPCode");  
  
adapter.Fill(custDS);  
```  
  
 在更为先进的情况下，可以决定需要使用相同的 DataAdapter 来支持为不同的表加载不同的映射。 为此，只需添加其他 **DataTableMapping** 对象。  
  
 当 Fill 方法以 DataSet 实例和 DataTableMapping 名称的形式进行传递时，如果存在具有该名称的映射，则使用该映射；否则将使用具有该名称的 DataTable   。  
  
 以下示例创建一个名称为 Customers 而 DataTable 名称为 BizTalkSchema 的 DataTableMapping   。 然后，该示例将 SELECT 语句所返回的行映射到 BizTalkSchema DataTable 。  
  
```vb  
Dim mapping As ITableMapping = _  
  adapter.TableMappings.Add("Customers", "BizTalkSchema")  
mapping.ColumnMappings.Add("CustomerID", "ClientID")  
mapping.ColumnMappings.Add("CompanyName", "ClientName")  
mapping.ColumnMappings.Add("ContactName", "Contact")  
mapping.ColumnMappings.Add("PostalCode", "ZIP")  
  
adapter.Fill(custDS, "Customers")  
```  
  
```csharp  
ITableMapping mapping =
  adapter.TableMappings.Add("Customers", "BizTalkSchema");  
mapping.ColumnMappings.Add("CustomerID", "ClientID");  
mapping.ColumnMappings.Add("CompanyName", "ClientName");  
mapping.ColumnMappings.Add("ContactName", "Contact");  
mapping.ColumnMappings.Add("PostalCode", "ZIP");  
  
adapter.Fill(custDS, "Customers");  
```  
  
> [!NOTE]
> 如果没有为列映射提供源列名称或者没有为表映射提供源表名称，则将自动生成默认名称。 如果没有为列映射提供源列，则从 **SourceColumn1** 开始，列映射的增量默认名称为 **SourceColumn** *N* 。 如果没有为表映射提供源表名称，则从 **SourceTable1** 开始为表映射提供增量默认名称 **SourceTable** *N*。  
  
> [!NOTE]
> 我们建议避免采用列映射的 SourceColumn N 的命名约定，或表映射的 SourceTable N 的命名约定，因为提供的名称可能会与 ColumnMappingCollection 中的现有默认列映射名称或 DataTableMappingCollection 中的现有默认表映射名称冲突 。 如果提供的名称已经存在，将引发异常。  
  
## <a name="handling-multiple-result-sets"></a>处理多个结果集  

 如果 SelectCommand 返回多个表，Fill 将自动使用递增值为 DataSet 中的表生成表名称，这些表名称从指定表名称开始（从 TableName1 开始），并以 TableName N 格式继续   。 可以使用表映射将自动生成的表名称映射到要为 DataSet 中的表指定的名称。 例如，对于返回两个表（Customers 和 Orders）的 SelectCommand，可对 Fill 发出以下调用   。  
  
```vb  
adapter.Fill(customersDataSet, "Customers")  
```  

```csharp  
adapter.Fill(customersDataSet, "Customers");  
```  

 DataSet 中创建了两个表：Customers 和 Customers1 。 可以使用表映射来确保第二个表名为 Orders 而不是 Customers1 。 若要完成此任务，请将 Customers1 的源表映射到 DataSet 表 Orders，如以下示例所示  。  
  
```vb  
adapter.TableMappings.Add("Customers1", "Orders")  
adapter.Fill(customersDataSet, "Customers")  
```  

```csharp  
adapter.TableMappings.Add("Customers1", "Orders");  
adapter.Fill(customersDataSet, "Customers");  
```
  
## <a name="see-also"></a>另请参阅

- [DataAdapter 和 DataReader](dataadapters-and-datareaders.md)
- [在 ADO.NET 中检索和修改数据](retrieving-and-modifying-data.md)
- [ADO.NET 概述](ado-net-overview.md)
