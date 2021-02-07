---
description: 了解详细信息：向数据集添加现有约束
title: 将现有约束添加到数据集
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 307d2809-208b-4cf8-b6a9-5d16f15fc16c
ms.openlocfilehash: cad0dd1bd16747a5e76e10784d00c14cd9aa8c2a
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99729567"
---
# <a name="adding-existing-constraints-to-a-dataset"></a><span data-ttu-id="6ddae-103">将现有约束添加到数据集</span><span class="sxs-lookup"><span data-stu-id="6ddae-103">Adding Existing Constraints to a DataSet</span></span>

<span data-ttu-id="6ddae-104">**DataAdapter** 的 **Fill** 方法 <xref:System.Data.DataSet> 只使用表中的列和数据源中的行填充; 虽然约束通常由数据源设置，但 **Fill** 方法默认情况下不会将此架构信息添加到 **数据集**。</span><span class="sxs-lookup"><span data-stu-id="6ddae-104">The **Fill** method of the **DataAdapter** fills a <xref:System.Data.DataSet> only with table columns and rows from a data source; though constraints are commonly set by the data source, the **Fill** method does not add this schema information to the **DataSet** by default.</span></span> <span data-ttu-id="6ddae-105">若要使用数据源中的现有主键约束信息来填充数据 **集**，可以调用 **dataadapter** 的 **FillSchema** 方法，或在调用 **Fill** 前将 **dataadapter** 的 **MissingSchemaAction** 属性设置为 **AddWithKey** 。</span><span class="sxs-lookup"><span data-stu-id="6ddae-105">To populate a **DataSet** with existing primary key constraint information from a data source, you can either call the **FillSchema** method of the **DataAdapter**, or set the **MissingSchemaAction** property of the **DataAdapter** to **AddWithKey** before calling **Fill**.</span></span> <span data-ttu-id="6ddae-106">这将确保 DataSet 中的主键约束反映数据源中的主键约束。</span><span class="sxs-lookup"><span data-stu-id="6ddae-106">This will ensure that primary key constraints in the **DataSet** reflect those at the data source.</span></span> <span data-ttu-id="6ddae-107">外键约束信息不包括在内，并且必须显式创建，如 [DataTable 约束](./dataset-datatable-dataview/datatable-constraints.md)中所示。</span><span class="sxs-lookup"><span data-stu-id="6ddae-107">Foreign key constraint information is not included and must be created explicitly, as shown in [DataTable Constraints](./dataset-datatable-dataview/datatable-constraints.md).</span></span>  
  
<span data-ttu-id="6ddae-108">如果在使用数据填充 DataSet 之前向其中添加架构信息，可以确保将主键约束与 DataSet 中的 <xref:System.Data.DataTable> 对象包含在一起 。</span><span class="sxs-lookup"><span data-stu-id="6ddae-108">Adding schema information to a **DataSet** before filling it with data ensures that primary key constraints are included with the <xref:System.Data.DataTable> objects in the **DataSet**.</span></span> <span data-ttu-id="6ddae-109">这样，当再次调用来填充 DataSet 时，将使用主键列信息将数据源中的新行与每个 DataTable 中的当前行相匹配，并使用数据源中的数据改写表中的当前数据 。</span><span class="sxs-lookup"><span data-stu-id="6ddae-109">As a result, when additional calls to fill the **DataSet** are made, the primary key column information is used to match new rows from the data source with current rows in each **DataTable**, and current data in the tables is overwritten with data from the data source.</span></span> <span data-ttu-id="6ddae-110">如果没有架构信息，来自数据源的新行将追加到 DataSet 中，从而导致重复的行。</span><span class="sxs-lookup"><span data-stu-id="6ddae-110">Without the schema information, the new rows from the data source are appended to the **DataSet**, resulting in duplicate rows.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="6ddae-111">如果数据源中的列被标识为自动递增、 **FillSchema** 方法或 **MissingSchemaAction** 为 **AddWithKey** 的 **Fill** 方法，则将创建一个 **自动增量** 属性设置为的 **DataColumn** `true` 。</span><span class="sxs-lookup"><span data-stu-id="6ddae-111">If a column in a data source is identified as auto-incrementing, the **FillSchema** method, or the **Fill** method with a **MissingSchemaAction** of **AddWithKey**, creates a **DataColumn** with an **AutoIncrement** property set to `true`.</span></span> <span data-ttu-id="6ddae-112">不过，你需要手动设置 AutoIncrementStep 和 AutoIncrementSeed 值 。</span><span class="sxs-lookup"><span data-stu-id="6ddae-112">However, you will need to set the **AutoIncrementStep** and **AutoIncrementSeed** values yourself.</span></span> <span data-ttu-id="6ddae-113">有关自动递增列的详细信息，请参阅 [创建自动增量列](./dataset-datatable-dataview/creating-autoincrement-columns.md)。</span><span class="sxs-lookup"><span data-stu-id="6ddae-113">For more information about auto-incrementing columns, see [Creating AutoIncrement Columns](./dataset-datatable-dataview/creating-autoincrement-columns.md).</span></span>  
  
<span data-ttu-id="6ddae-114">当使用 FillSchema 或将 MissingSchemaAction 设置为 AddWithKey 时，需要在数据源中进行额外的处理来确定主键列信息  。</span><span class="sxs-lookup"><span data-stu-id="6ddae-114">Using **FillSchema** or setting the **MissingSchemaAction** to **AddWithKey** requires extra processing at the data source to determine primary key column information.</span></span> <span data-ttu-id="6ddae-115">这一额外的处理可能会降低性能。</span><span class="sxs-lookup"><span data-stu-id="6ddae-115">This additional processing can hinder performance.</span></span> <span data-ttu-id="6ddae-116">如果主键信息在设计时已知，为了实现最佳性能，建议显式指定一个或多个主键列。</span><span class="sxs-lookup"><span data-stu-id="6ddae-116">If you know the primary key information at design time, we recommend that you explicitly specify the primary key column or columns in order to achieve optimal performance.</span></span> <span data-ttu-id="6ddae-117">有关显式设置表的主键信息的信息，请参阅 [定义主键](./dataset-datatable-dataview/defining-primary-keys.md)。</span><span class="sxs-lookup"><span data-stu-id="6ddae-117">For information about explicitly setting primary key information for a table, see [Defining Primary Keys](./dataset-datatable-dataview/defining-primary-keys.md).</span></span>
  
<span data-ttu-id="6ddae-118">下面的代码示例演示如何使用 **FillSchema** 将架构信息添加到 **数据集**：</span><span class="sxs-lookup"><span data-stu-id="6ddae-118">The following code example shows how to add schema information to a **DataSet** using **FillSchema**:</span></span>
  
```vb  
Dim custDataSet As New DataSet()  
  
custAdapter.FillSchema(custDataSet, SchemaType.Source, "Customers")  
custAdapter.Fill(custDataSet, "Customers")  
```  
  
```csharp  
var custDataSet = new DataSet();  
  
custAdapter.FillSchema(custDataSet, SchemaType.Source, "Customers");  
custAdapter.Fill(custDataSet, "Customers");  
```  
  
<span data-ttu-id="6ddae-119">下面的代码示例演示如何使用 **Fill** 方法的 **MissingSchemaAction. AddWithKey** 属性向 **数据集** 添加架构信息：</span><span class="sxs-lookup"><span data-stu-id="6ddae-119">The following code example shows how to add schema information to a **DataSet** using the **MissingSchemaAction.AddWithKey** property of the **Fill** method:</span></span>
  
```vb  
Dim custDataSet As New DataSet()  
  
custAdapter.MissingSchemaAction = MissingSchemaAction.AddWithKey  
custAdapter.Fill(custDataSet, "Customers")  
```  
  
```csharp  
var custDataSet = new DataSet();  
  
custAdapter.MissingSchemaAction = MissingSchemaAction.AddWithKey;  
custAdapter.Fill(custDataSet, "Customers");  
```  
  
## <a name="handling-multiple-result-sets"></a><span data-ttu-id="6ddae-120">处理多个结果集</span><span class="sxs-lookup"><span data-stu-id="6ddae-120">Handling multiple result sets</span></span>  

<span data-ttu-id="6ddae-121">如果 **DataAdapter** 遇到 **SelectCommand** 返回的多个结果集，它将在 **数据集中** 创建多个表。</span><span class="sxs-lookup"><span data-stu-id="6ddae-121">If the **DataAdapter** encounters multiple result sets returned from the **SelectCommand**, it will create multiple tables in the **DataSet**.</span></span> <span data-ttu-id="6ddae-122">将向这些表提供基于零的递增的默认名称 Table N，从“Table”开始，而不是从“Table0”开始。</span><span class="sxs-lookup"><span data-stu-id="6ddae-122">The tables will be given a zero-based incremental default name of **Table** *N*, starting with **Table** instead of "Table0".</span></span> <span data-ttu-id="6ddae-123">如果表名作为参数传递给 **FillSchema** 方法，则会为这些表指定从零 **开始的名称（从** **tablename** 开始，而不是 "TableName0 *"）。*</span><span class="sxs-lookup"><span data-stu-id="6ddae-123">If a table name is passed as an argument to the **FillSchema** method, the tables will be given a zero-based incremental name of **TableName** *N*, starting with **TableName** instead of "TableName0".</span></span>  
  
> [!NOTE]
> <span data-ttu-id="6ddae-124">如果对返回多个结果集的命令调用 **OleDbDataAdapter** 对象的 **FillSchema** 方法，则仅返回第一个结果集的架构信息。</span><span class="sxs-lookup"><span data-stu-id="6ddae-124">If the **FillSchema** method of the **OleDbDataAdapter** object is called for a command that returns multiple result sets, only the schema information from the first result set is returned.</span></span> <span data-ttu-id="6ddae-125">当使用 **OleDbDataAdapter** 返回多个结果集的架构信息时，建议您指定 **MissingSchemaAction** 的 **AddWithKey** ，并在调用 **Fill** 方法时获取架构信息。</span><span class="sxs-lookup"><span data-stu-id="6ddae-125">When returning schema information for multiple result sets using the **OleDbDataAdapter**, it is recommended that you specify a **MissingSchemaAction** of **AddWithKey** and obtain the schema information when calling the **Fill** method.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6ddae-126">另请参阅</span><span class="sxs-lookup"><span data-stu-id="6ddae-126">See also</span></span>

- [<span data-ttu-id="6ddae-127">DataAdapter 和 DataReader</span><span class="sxs-lookup"><span data-stu-id="6ddae-127">DataAdapters and DataReaders</span></span>](dataadapters-and-datareaders.md)
- [<span data-ttu-id="6ddae-128">数据集、数据表和数据视图</span><span class="sxs-lookup"><span data-stu-id="6ddae-128">DataSets, DataTables, and DataViews</span></span>](./dataset-datatable-dataview/index.md)
- [<span data-ttu-id="6ddae-129">在 ADO.NET 中检索和修改数据</span><span class="sxs-lookup"><span data-stu-id="6ddae-129">Retrieving and Modifying Data in ADO.NET</span></span>](retrieving-and-modifying-data.md)
- [<span data-ttu-id="6ddae-130">ADO.NET 概述</span><span class="sxs-lookup"><span data-stu-id="6ddae-130">ADO.NET Overview</span></span>](ado-net-overview.md)
