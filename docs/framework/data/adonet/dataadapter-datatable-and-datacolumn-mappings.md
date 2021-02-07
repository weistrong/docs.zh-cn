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
# <a name="dataadapter-datatable-and-datacolumn-mappings"></a><span data-ttu-id="83f1a-103">DataAdapter 数据表和 DataColumn 映射</span><span class="sxs-lookup"><span data-stu-id="83f1a-103">DataAdapter DataTable and DataColumn Mappings</span></span>

<span data-ttu-id="83f1a-104">**DataAdapter** <xref:System.Data.Common.DataTableMapping> 在其 **TableMappings** 属性中包含零个或多个对象的集合。</span><span class="sxs-lookup"><span data-stu-id="83f1a-104">A **DataAdapter** contains a collection of zero or more <xref:System.Data.Common.DataTableMapping> objects in its **TableMappings** property.</span></span> <span data-ttu-id="83f1a-105">**DataTableMapping** 提供了针对数据源的查询返回的数据与之间的主映射 <xref:System.Data.DataTable> 。</span><span class="sxs-lookup"><span data-stu-id="83f1a-105">A **DataTableMapping** provides a master mapping between the data returned from a query against a data source, and a <xref:System.Data.DataTable>.</span></span> <span data-ttu-id="83f1a-106">可以将 **DataTableMapping** 名称替换为将 **DataTable** 名称替换为 **DataAdapter** 的 **Fill** 方法。</span><span class="sxs-lookup"><span data-stu-id="83f1a-106">The **DataTableMapping** name can be passed in place of the **DataTable** name to the **Fill** method of the **DataAdapter**.</span></span> <span data-ttu-id="83f1a-107">以下示例为 Authors 表创建名为 AuthorsMapping 的 DataTableMapping  。</span><span class="sxs-lookup"><span data-stu-id="83f1a-107">The following example creates a **DataTableMapping** named **AuthorsMapping** for the **Authors** table.</span></span>  
  
```vb  
workAdapter.TableMappings.Add("AuthorsMapping", "Authors")  
```  
  
```csharp  
workAdapter.TableMappings.Add("AuthorsMapping", "Authors");  
```  
  
 <span data-ttu-id="83f1a-108">DataTableMapping 使你能够使用 DataTable 中与数据库中的列名不同的列名 。</span><span class="sxs-lookup"><span data-stu-id="83f1a-108">A **DataTableMapping** enables you to use column names in a **DataTable** that are different from those in the database.</span></span> <span data-ttu-id="83f1a-109">当该表被更新时，DataAdapter 将使用此映射来匹配列。</span><span class="sxs-lookup"><span data-stu-id="83f1a-109">The **DataAdapter** uses the mapping to match the columns when the table is updated.</span></span>  
  
 <span data-ttu-id="83f1a-110">如果在调用 DataAdapter 的 Fill 或 Update 方法时未指定 TableName 或 DataTableMapping 名称，DataAdapter 将查找名为“Table”的 DataTableMapping      。</span><span class="sxs-lookup"><span data-stu-id="83f1a-110">If you do not specify a **TableName** or a **DataTableMapping** name when calling the **Fill** or **Update** method of the **DataAdapter**, the **DataAdapter** looks for a **DataTableMapping** named "Table".</span></span> <span data-ttu-id="83f1a-111">如果该 **DataTableMapping** 不存在，则 **DataTable** 的 **TableName** 为 "Table"。</span><span class="sxs-lookup"><span data-stu-id="83f1a-111">If that **DataTableMapping** does not exist, the **TableName** of the **DataTable** is "Table".</span></span> <span data-ttu-id="83f1a-112">可以通过创建名为“Table”的 DataTableMapping 来指定默认的 DataTableMapping 。</span><span class="sxs-lookup"><span data-stu-id="83f1a-112">You can specify a default **DataTableMapping** by creating a **DataTableMapping** with the name of "Table".</span></span>  
  
 <span data-ttu-id="83f1a-113">以下代码示例（从 <xref:System.Data.Common> 命名空间）创建一个 DataTableMapping 并通过将其命名为“Table”来使其成为指定 DataAdapter 的默认映射 。</span><span class="sxs-lookup"><span data-stu-id="83f1a-113">The following code example creates a **DataTableMapping** (from the <xref:System.Data.Common> namespace) and makes it the default mapping for the specified **DataAdapter** by naming it "Table".</span></span> <span data-ttu-id="83f1a-114">然后，该示例将查询结果中第一个表（Northwind 数据库的 Customers 表）中的列映射到 <xref:System.Data.DataSet> 的 Northwind Customers 表中的一组更为易记的名称  。</span><span class="sxs-lookup"><span data-stu-id="83f1a-114">The example then maps the columns from the first table in the query result (the **Customers** table of the **Northwind** database) to a set of more user-friendly names in the **Northwind Customers** table in the <xref:System.Data.DataSet>.</span></span> <span data-ttu-id="83f1a-115">对于未映射的列，将使用数据源中的列名称。</span><span class="sxs-lookup"><span data-stu-id="83f1a-115">For columns that are not mapped, the name of the column from the data source is used.</span></span>  
  
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
  
 <span data-ttu-id="83f1a-116">在更为先进的情况下，可以决定需要使用相同的 DataAdapter 来支持为不同的表加载不同的映射。</span><span class="sxs-lookup"><span data-stu-id="83f1a-116">In more advanced situations, you may decide that you want the same **DataAdapter** to support loading different tables with different mappings.</span></span> <span data-ttu-id="83f1a-117">为此，只需添加其他 **DataTableMapping** 对象。</span><span class="sxs-lookup"><span data-stu-id="83f1a-117">To do this, simply add additional **DataTableMapping** objects.</span></span>  
  
 <span data-ttu-id="83f1a-118">当 Fill 方法以 DataSet 实例和 DataTableMapping 名称的形式进行传递时，如果存在具有该名称的映射，则使用该映射；否则将使用具有该名称的 DataTable   。</span><span class="sxs-lookup"><span data-stu-id="83f1a-118">When the **Fill** method is passed an instance of a **DataSet** and a **DataTableMapping** name, if a mapping with that name exists it is used; otherwise, a **DataTable** with that name is used.</span></span>  
  
 <span data-ttu-id="83f1a-119">以下示例创建一个名称为 Customers 而 DataTable 名称为 BizTalkSchema 的 DataTableMapping   。</span><span class="sxs-lookup"><span data-stu-id="83f1a-119">The following examples create a **DataTableMapping** with a name of **Customers** and a **DataTable** name of **BizTalkSchema**.</span></span> <span data-ttu-id="83f1a-120">然后，该示例将 SELECT 语句所返回的行映射到 BizTalkSchema DataTable 。</span><span class="sxs-lookup"><span data-stu-id="83f1a-120">The example then maps the rows returned by the SELECT statement to the **BizTalkSchema** **DataTable**.</span></span>  
  
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
> <span data-ttu-id="83f1a-121">如果没有为列映射提供源列名称或者没有为表映射提供源表名称，则将自动生成默认名称。</span><span class="sxs-lookup"><span data-stu-id="83f1a-121">If a source column name is not supplied for a column mapping or a source table name is not supplied for a table mapping, default names will be automatically generated.</span></span> <span data-ttu-id="83f1a-122">如果没有为列映射提供源列，则从 **SourceColumn1** 开始，列映射的增量默认名称为 **SourceColumn** *N* 。</span><span class="sxs-lookup"><span data-stu-id="83f1a-122">If no source column is supplied for a column mapping, the column mapping is given an incremental default name of **SourceColumn** *N,* starting with **SourceColumn1**.</span></span> <span data-ttu-id="83f1a-123">如果没有为表映射提供源表名称，则从 **SourceTable1** 开始为表映射提供增量默认名称 **SourceTable** *N*。</span><span class="sxs-lookup"><span data-stu-id="83f1a-123">If no source table name is supplied for a table mapping, the table mapping is given an incremental default name of **SourceTable** *N*, starting with **SourceTable1**.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="83f1a-124">我们建议避免采用列映射的 SourceColumn N 的命名约定，或表映射的 SourceTable N 的命名约定，因为提供的名称可能会与 ColumnMappingCollection 中的现有默认列映射名称或 DataTableMappingCollection 中的现有默认表映射名称冲突 。</span><span class="sxs-lookup"><span data-stu-id="83f1a-124">We recommend that you avoid the naming convention of **SourceColumn** *N* for a column mapping, or **SourceTable** *N* for a table mapping, because the name you supply may conflict with an existing default column mapping name in the **ColumnMappingCollection** or table mapping name in the **DataTableMappingCollection**.</span></span> <span data-ttu-id="83f1a-125">如果提供的名称已经存在，将引发异常。</span><span class="sxs-lookup"><span data-stu-id="83f1a-125">If the supplied name already exists, an exception will be thrown.</span></span>  
  
## <a name="handling-multiple-result-sets"></a><span data-ttu-id="83f1a-126">处理多个结果集</span><span class="sxs-lookup"><span data-stu-id="83f1a-126">Handling Multiple Result Sets</span></span>  

 <span data-ttu-id="83f1a-127">如果 SelectCommand 返回多个表，Fill 将自动使用递增值为 DataSet 中的表生成表名称，这些表名称从指定表名称开始（从 TableName1 开始），并以 TableName N 格式继续   。</span><span class="sxs-lookup"><span data-stu-id="83f1a-127">If your **SelectCommand** returns multiple tables, **Fill** automatically generates table names with incremental values for the tables in the **DataSet**, starting with the specified table name and continuing on in the form **TableName** *N*, starting with **TableName1**.</span></span> <span data-ttu-id="83f1a-128">可以使用表映射将自动生成的表名称映射到要为 DataSet 中的表指定的名称。</span><span class="sxs-lookup"><span data-stu-id="83f1a-128">You can use table mappings to map the automatically generated table name to a name you want specified for the table in the **DataSet**.</span></span> <span data-ttu-id="83f1a-129">例如，对于返回两个表（Customers 和 Orders）的 SelectCommand，可对 Fill 发出以下调用   。</span><span class="sxs-lookup"><span data-stu-id="83f1a-129">For example, for a **SelectCommand** that returns two tables, **Customers** and **Orders**, issue the following call to **Fill**.</span></span>  
  
```vb  
adapter.Fill(customersDataSet, "Customers")  
```  

```csharp  
adapter.Fill(customersDataSet, "Customers");  
```  

 <span data-ttu-id="83f1a-130">DataSet 中创建了两个表：Customers 和 Customers1 。</span><span class="sxs-lookup"><span data-stu-id="83f1a-130">Two tables are created in the **DataSet**: **Customers** and **Customers1**.</span></span> <span data-ttu-id="83f1a-131">可以使用表映射来确保第二个表名为 Orders 而不是 Customers1 。</span><span class="sxs-lookup"><span data-stu-id="83f1a-131">You can use table mappings to ensure that the second table is named **Orders** instead of **Customers1**.</span></span> <span data-ttu-id="83f1a-132">若要完成此任务，请将 Customers1 的源表映射到 DataSet 表 Orders，如以下示例所示  。</span><span class="sxs-lookup"><span data-stu-id="83f1a-132">To do this, map the source table of **Customers1** to the **DataSet** table **Orders**, as shown in the following example.</span></span>  
  
```vb  
adapter.TableMappings.Add("Customers1", "Orders")  
adapter.Fill(customersDataSet, "Customers")  
```  

```csharp  
adapter.TableMappings.Add("Customers1", "Orders");  
adapter.Fill(customersDataSet, "Customers");  
```
  
## <a name="see-also"></a><span data-ttu-id="83f1a-133">另请参阅</span><span class="sxs-lookup"><span data-stu-id="83f1a-133">See also</span></span>

- [<span data-ttu-id="83f1a-134">DataAdapter 和 DataReader</span><span class="sxs-lookup"><span data-stu-id="83f1a-134">DataAdapters and DataReaders</span></span>](dataadapters-and-datareaders.md)
- [<span data-ttu-id="83f1a-135">在 ADO.NET 中检索和修改数据</span><span class="sxs-lookup"><span data-stu-id="83f1a-135">Retrieving and Modifying Data in ADO.NET</span></span>](retrieving-and-modifying-data.md)
- [<span data-ttu-id="83f1a-136">ADO.NET 概述</span><span class="sxs-lookup"><span data-stu-id="83f1a-136">ADO.NET Overview</span></span>](ado-net-overview.md)
