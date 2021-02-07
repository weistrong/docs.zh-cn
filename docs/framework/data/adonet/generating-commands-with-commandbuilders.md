---
description: 了解更多：通过 Commandbuilder 生成命令
title: 使用 CommandBuilder 生成命令
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 6e3fb8b5-373b-4f9e-ab03-a22693df8e91
ms.openlocfilehash: 495312f57d497421182384eff23b621130447940
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99724097"
---
# <a name="generating-commands-with-commandbuilders"></a><span data-ttu-id="80c2e-103">使用 CommandBuilder 生成命令</span><span class="sxs-lookup"><span data-stu-id="80c2e-103">Generating Commands with CommandBuilders</span></span>

<span data-ttu-id="80c2e-104">如果在运行时动态指定 `SelectCommand` 属性（例如，通过接受用户提供的文本命令的查询工具），那么您可能无法在设计时指定适当的 `InsertCommand`、`UpdateCommand` 或 `DeleteCommand`。</span><span class="sxs-lookup"><span data-stu-id="80c2e-104">When the `SelectCommand` property is dynamically specified at run time, such as through a query tool that takes a textual command from the user, you may not be able to specify the appropriate `InsertCommand`, `UpdateCommand`, or `DeleteCommand` at design time.</span></span> <span data-ttu-id="80c2e-105">如果您的 <xref:System.Data.DataTable> 映射到单个数据库表或者是从单个数据库表中生成的，那么您可以利用 <xref:System.Data.Common.DbCommandBuilder> 对象来自动生成 `DeleteCommand` 的 `InsertCommand`、`UpdateCommand` 和 <xref:System.Data.Common.DbDataAdapter>。</span><span class="sxs-lookup"><span data-stu-id="80c2e-105">If your <xref:System.Data.DataTable> maps to or is generated from a single database table, you can take advantage of the <xref:System.Data.Common.DbCommandBuilder> object to automatically generate the `DeleteCommand`, `InsertCommand`, and `UpdateCommand` of the <xref:System.Data.Common.DbDataAdapter>.</span></span>  
  
 <span data-ttu-id="80c2e-106">为了能够自动生成命令，必须设置 `SelectCommand` 属性，这是最低要求。</span><span class="sxs-lookup"><span data-stu-id="80c2e-106">As a minimum requirement, you must set the `SelectCommand` property in order for automatic command generation to work.</span></span> <span data-ttu-id="80c2e-107">由 `SelectCommand` 属性检索的表架构确定自动生成的 INSERT、UPDATE 和 DELETE 语句的语法。</span><span class="sxs-lookup"><span data-stu-id="80c2e-107">The table schema retrieved by the `SelectCommand` property determines the syntax of the automatically generated INSERT, UPDATE, and DELETE statements.</span></span>  
  
 <span data-ttu-id="80c2e-108">为了返回构造 INSERT、UPDATE 和 DELETE SQL 命令所需的元数据，<xref:System.Data.Common.DbCommandBuilder> 必须执行 `SelectCommand`。</span><span class="sxs-lookup"><span data-stu-id="80c2e-108">The <xref:System.Data.Common.DbCommandBuilder> must execute the `SelectCommand` in order to return the metadata necessary to construct the INSERT, UPDATE, and DELETE SQL commands.</span></span> <span data-ttu-id="80c2e-109">因此，必须额外经历一次到数据源的过程，这可能会降低性能。</span><span class="sxs-lookup"><span data-stu-id="80c2e-109">As a result, an extra trip to the data source is necessary, and this can hinder performance.</span></span> <span data-ttu-id="80c2e-110">若要实现最佳性能，请显式指定命令而不是使用 <xref:System.Data.Common.DbCommandBuilder>。</span><span class="sxs-lookup"><span data-stu-id="80c2e-110">To achieve optimal performance, specify your commands explicitly rather than using the <xref:System.Data.Common.DbCommandBuilder>.</span></span>  
  
 <span data-ttu-id="80c2e-111">`SelectCommand` 还必须至少返回一个主键或唯一列。</span><span class="sxs-lookup"><span data-stu-id="80c2e-111">The `SelectCommand` must also return at least one primary key or unique column.</span></span> <span data-ttu-id="80c2e-112">如果不存在任何主键和唯一列，则会生成 `InvalidOperation` 异常，并且不会生成命令。</span><span class="sxs-lookup"><span data-stu-id="80c2e-112">If none are present, an `InvalidOperation` exception is generated, and the commands are not generated.</span></span>  
  
 <span data-ttu-id="80c2e-113">当与 `DataAdapter` 关联时，<xref:System.Data.Common.DbCommandBuilder> 会自动生成 `InsertCommand` 的 `UpdateCommand`、`DeleteCommand` 和 `DataAdapter` 属性（如果它们为空引用）。</span><span class="sxs-lookup"><span data-stu-id="80c2e-113">When associated with a `DataAdapter`, the <xref:System.Data.Common.DbCommandBuilder> automatically generates the `InsertCommand`, `UpdateCommand`, and `DeleteCommand` properties of the `DataAdapter` if they are null references.</span></span> <span data-ttu-id="80c2e-114">如果某个属性已存在 `Command`，则使用现有 `Command`。</span><span class="sxs-lookup"><span data-stu-id="80c2e-114">If a `Command` already exists for a property, the existing `Command` is used.</span></span>  
  
 <span data-ttu-id="80c2e-115">通过联接两个或更多个表来创建的数据库视图不会被视为单个数据库表。</span><span class="sxs-lookup"><span data-stu-id="80c2e-115">Database views that are created by joining two or more tables together are not considered a single database table.</span></span> <span data-ttu-id="80c2e-116">在这种情况下，您无法使用 <xref:System.Data.Common.DbCommandBuilder> 来自动生成命令；必须显式指定命令。</span><span class="sxs-lookup"><span data-stu-id="80c2e-116">In this instance you cannot use the <xref:System.Data.Common.DbCommandBuilder> to automatically generate commands; you must specify your commands explicitly.</span></span> <span data-ttu-id="80c2e-117">有关显式设置命令以将更新解析 `DataSet` 回数据源的信息，请参阅 [使用 Dataadapter 更新数据源](updating-data-sources-with-dataadapters.md)。</span><span class="sxs-lookup"><span data-stu-id="80c2e-117">For information about explicitly setting commands to resolve updates to a `DataSet` back to the data source, see [Updating Data Sources with DataAdapters](updating-data-sources-with-dataadapters.md).</span></span>  
  
 <span data-ttu-id="80c2e-118">您可能需要将输出参数映射回 `DataSet` 的更新行。</span><span class="sxs-lookup"><span data-stu-id="80c2e-118">You might want to map output parameters back to the updated row of a `DataSet`.</span></span> <span data-ttu-id="80c2e-119">一项常见的任务是从数据源中检索自动生成的标识字段或时间戳的值。</span><span class="sxs-lookup"><span data-stu-id="80c2e-119">One common task would be retrieving the value of an automatically generated identity field or time stamp from the data source.</span></span> <span data-ttu-id="80c2e-120">默认情况下，<xref:System.Data.Common.DbCommandBuilder> 不会将输出参数映射到更新行中的列。</span><span class="sxs-lookup"><span data-stu-id="80c2e-120">The <xref:System.Data.Common.DbCommandBuilder> will not map output parameters to columns in an updated row by default.</span></span> <span data-ttu-id="80c2e-121">在这种情况下，必须显式指定命令。</span><span class="sxs-lookup"><span data-stu-id="80c2e-121">In this instance you must specify your command explicitly.</span></span> <span data-ttu-id="80c2e-122">有关将自动生成的标识字段映射回插入行的列的示例，请参阅 [检索标识或自动编号值](retrieving-identity-or-autonumber-values.md)。</span><span class="sxs-lookup"><span data-stu-id="80c2e-122">For an example of mapping an automatically generated identity field back to a column of an inserted row, see [Retrieving Identity or Autonumber Values](retrieving-identity-or-autonumber-values.md).</span></span>  
  
## <a name="rules-for-automatically-generated-commands"></a><span data-ttu-id="80c2e-123">自动生成命令的规则</span><span class="sxs-lookup"><span data-stu-id="80c2e-123">Rules for Automatically Generated Commands</span></span>  

 <span data-ttu-id="80c2e-124">下表显示创建自动生成命令的规则。</span><span class="sxs-lookup"><span data-stu-id="80c2e-124">The following table shows the rules for how automatically generated commands are generated.</span></span>  
  
|<span data-ttu-id="80c2e-125">命令</span><span class="sxs-lookup"><span data-stu-id="80c2e-125">Command</span></span>|<span data-ttu-id="80c2e-126">规则</span><span class="sxs-lookup"><span data-stu-id="80c2e-126">Rule</span></span>|  
|-------------|----------|  
|`InsertCommand`|<span data-ttu-id="80c2e-127">在数据源处为表中所有 <xref:System.Data.DataRow.RowState%2A> 为 <xref:System.Data.DataRowState.Added> 的行插入一行。</span><span class="sxs-lookup"><span data-stu-id="80c2e-127">Inserts a row at the data source for all rows in the table with a <xref:System.Data.DataRow.RowState%2A> of <xref:System.Data.DataRowState.Added>.</span></span> <span data-ttu-id="80c2e-128">插入所有可更新列的值（但是不包括标识、表达式或时间戳等列）。</span><span class="sxs-lookup"><span data-stu-id="80c2e-128">Inserts values for all columns that are updateable (but not columns such as identities, expressions, or timestamps).</span></span>|  
|`UpdateCommand`|<span data-ttu-id="80c2e-129">在数据源处更新表中所有 `RowState` 为 <xref:System.Data.DataRowState.Modified> 的行。</span><span class="sxs-lookup"><span data-stu-id="80c2e-129">Updates rows at the data source for all rows in the table with a `RowState` of <xref:System.Data.DataRowState.Modified>.</span></span> <span data-ttu-id="80c2e-130">更新所有列的值，不可更新的列除外，例如标识列或表达式列。</span><span class="sxs-lookup"><span data-stu-id="80c2e-130">Updates the values of all columns except for columns that are not updateable, such as identities or expressions.</span></span> <span data-ttu-id="80c2e-131">更新符合以下条件的所有行：数据源中的列值匹配行的主键列值，并且数据源中的剩余列匹配行的原始值。</span><span class="sxs-lookup"><span data-stu-id="80c2e-131">Updates all rows where the column values at the data source match the primary key column values of the row, and where the remaining columns at the data source match the original values of the row.</span></span> <span data-ttu-id="80c2e-132">有关更多信息，请参见本主题后面的“更新和删除的开放式并发模型”。</span><span class="sxs-lookup"><span data-stu-id="80c2e-132">For more information, see "Optimistic Concurrency Model for Updates and Deletes," later in this topic.</span></span>|  
|`DeleteCommand`|<span data-ttu-id="80c2e-133">在数据源处删除表中所有 `RowState` 为 <xref:System.Data.DataRowState.Deleted> 的行。</span><span class="sxs-lookup"><span data-stu-id="80c2e-133">Deletes rows at the data source for all rows in the table with a `RowState` of <xref:System.Data.DataRowState.Deleted>.</span></span> <span data-ttu-id="80c2e-134">删除符合以下条件的所有行：列值匹配行的主键列值，并且数据源中的剩余列匹配行的原始值。</span><span class="sxs-lookup"><span data-stu-id="80c2e-134">Deletes all rows where the column values match the primary key column values of the row, and where the remaining columns at the data source match the original values of the row.</span></span> <span data-ttu-id="80c2e-135">有关更多信息，请参见本主题后面的“更新和删除的开放式并发模型”。</span><span class="sxs-lookup"><span data-stu-id="80c2e-135">For more information, see "Optimistic Concurrency Model for Updates and Deletes," later in this topic.</span></span>|  
  
## <a name="optimistic-concurrency-model-for-updates-and-deletes"></a><span data-ttu-id="80c2e-136">更新和删除的开放式并发模型</span><span class="sxs-lookup"><span data-stu-id="80c2e-136">Optimistic Concurrency Model for Updates and Deletes</span></span>  

 <span data-ttu-id="80c2e-137">自动为 UPDATE 和 DELETE 语句生成命令的逻辑基于 *开放式并发性*，即，记录未锁定，无法进行编辑，并可随时由其他用户或进程进行修改。</span><span class="sxs-lookup"><span data-stu-id="80c2e-137">The logic for generating commands automatically for UPDATE and DELETE statements is based on *optimistic concurrency*--that is, records are not locked for editing and can be modified by other users or processes at any time.</span></span> <span data-ttu-id="80c2e-138">由于在从 SELECT 语句中返回某记录之后但在发出 UPDATE 或 DELETE 语句之前，该记录可能已被修改，所以自动生成的 UPDATE 或 DELETE 语句包含一个 WHERE 子句，指定只有在行包含所有原始值并且尚未从数据源中删除时，才会更新该行。</span><span class="sxs-lookup"><span data-stu-id="80c2e-138">Because a record could have been modified after it was returned from the SELECT statement, but before the UPDATE or DELETE statement is issued, the automatically generated UPDATE or DELETE statement contains a WHERE clause, specifying that a row is only updated if it contains all original values and has not been deleted from the data source.</span></span> <span data-ttu-id="80c2e-139">这样做的目的是为了避免覆盖新数据。</span><span class="sxs-lookup"><span data-stu-id="80c2e-139">This is done to avoid overwriting new data.</span></span> <span data-ttu-id="80c2e-140">当自动生成的 UPDATE 命令试图更新已删除或不包含 <xref:System.Data.DataSet> 中原始值的行时，该命令不会影响任何记录，并且会引发 <xref:System.Data.DBConcurrencyException>。</span><span class="sxs-lookup"><span data-stu-id="80c2e-140">Where an automatically generated update attempts to update a row that has been deleted or that does not contain the original values found in the <xref:System.Data.DataSet>, the command does not affect any records, and a <xref:System.Data.DBConcurrencyException> is thrown.</span></span>  
  
 <span data-ttu-id="80c2e-141">如果要使 UPDATE 或 DELETE 在不考虑原始值的情况下完成，必须为 `UpdateCommand` 显式设置 `DataAdapter`，而不依赖自动命令生成。</span><span class="sxs-lookup"><span data-stu-id="80c2e-141">If you want the UPDATE or DELETE to complete regardless of original values, you must explicitly set the `UpdateCommand` for the `DataAdapter` and not rely on automatic command generation.</span></span>  
  
## <a name="limitations-of-automatic-command-generation-logic"></a><span data-ttu-id="80c2e-142">自动命令生成逻辑的限制</span><span class="sxs-lookup"><span data-stu-id="80c2e-142">Limitations of Automatic Command Generation Logic</span></span>  

 <span data-ttu-id="80c2e-143">自动命令生成存在以下限制。</span><span class="sxs-lookup"><span data-stu-id="80c2e-143">The following limitations apply to automatic command generation.</span></span>  
  
### <a name="unrelated-tables-only"></a><span data-ttu-id="80c2e-144">仅限于无关表</span><span class="sxs-lookup"><span data-stu-id="80c2e-144">Unrelated Tables Only</span></span>  

 <span data-ttu-id="80c2e-145">自动命令生成逻辑为独立表生成 INSERT、UPDATE 或 DELETE 语句，而不考虑与数据源中其他表的任何关系。</span><span class="sxs-lookup"><span data-stu-id="80c2e-145">The automatic command generation logic generates INSERT, UPDATE, or DELETE statements for stand-alone tables without taking into account any relationships to other tables at the data source.</span></span> <span data-ttu-id="80c2e-146">因此，在调用 `Update` 以提交对参与数据库中外键约束的列的更改时，可能会失败。</span><span class="sxs-lookup"><span data-stu-id="80c2e-146">As a result, you may encounter a failure when calling `Update` to submit changes for a column that participates in a foreign key constraint in the database.</span></span> <span data-ttu-id="80c2e-147">若要避免这一异常，请不要使用 <xref:System.Data.Common.DbCommandBuilder> 来更新参与外键约束的列，而应显式地指定用于执行该操作的语句。</span><span class="sxs-lookup"><span data-stu-id="80c2e-147">To avoid this exception, do not use the <xref:System.Data.Common.DbCommandBuilder> for updating columns involved in a foreign key constraint; instead, explicitly specify the statements used to perform the operation.</span></span>  
  
### <a name="table-and-column-names"></a><span data-ttu-id="80c2e-148">表名称和列名称</span><span class="sxs-lookup"><span data-stu-id="80c2e-148">Table and Column Names</span></span>  

 <span data-ttu-id="80c2e-149">如果列名称或表名称包含任何特殊字符（如空格、句点、问号或其他非字母数字字符），则即使这些字符用括号分隔，自动命令生成逻辑也可能会失败。</span><span class="sxs-lookup"><span data-stu-id="80c2e-149">Automatic command generation logic may fail if column names or table names contain any special characters, such as spaces, periods, quotation marks, or other nonalphanumeric characters, even if delimited by brackets.</span></span> <span data-ttu-id="80c2e-150">根据具体提供程序，通过设置 QuotePrefix 和 QuoteSuffix 参数，生成逻辑可以处理空格，但无法转义特殊字符。</span><span class="sxs-lookup"><span data-stu-id="80c2e-150">Depending on the provider, setting the QuotePrefix and QuoteSuffix parameters may allow the generation logic to process spaces, but it cannot escape special characters.</span></span> <span data-ttu-id="80c2e-151">支持格式为 catalog.schema.table 的完全限定表名。</span><span class="sxs-lookup"><span data-stu-id="80c2e-151">Fully qualified table names in the form of *catalog.schema.table* are supported.</span></span>  
  
## <a name="using-the-commandbuilder-to-automatically-generate-an-sql-statement"></a><span data-ttu-id="80c2e-152">使用 CommandBuilder 自动生成 SQL 语句</span><span class="sxs-lookup"><span data-stu-id="80c2e-152">Using the CommandBuilder to Automatically Generate an SQL Statement</span></span>  

 <span data-ttu-id="80c2e-153">若要为 `DataAdapter` 自动生成 SQL 语句，请先设置 `SelectCommand` 的 `DataAdapter` 属性，然后创建 `CommandBuilder` 对象，并将该对象指定为 `DataAdapter` 将自动为其生成 SQL 语句的 `CommandBuilder` 的自变量。</span><span class="sxs-lookup"><span data-stu-id="80c2e-153">To automatically generate SQL statements for a `DataAdapter`, first set the `SelectCommand` property of the `DataAdapter`, then create a `CommandBuilder` object, and specify as an argument the `DataAdapter` for which the `CommandBuilder` will automatically generate SQL statements.</span></span>  
  
```vb  
' Assumes that connection is a valid SqlConnection object
' inside of a Using block.  
Dim adapter As SqlDataAdapter = New SqlDataAdapter( _  
  "SELECT * FROM dbo.Customers", connection)  
Dim builder As SqlCommandBuilder = New SqlCommandBuilder(adapter)  
builder.QuotePrefix = "["  
builder.QuoteSuffix = "]"  
```  
  
```csharp  
// Assumes that connection is a valid SqlConnection object  
// inside of a using block.  
SqlDataAdapter adapter = new SqlDataAdapter(  
  "SELECT * FROM dbo.Customers", connection);  
SqlCommandBuilder builder = new SqlCommandBuilder(adapter);  
builder.QuotePrefix = "[";  
builder.QuoteSuffix = "]";  
```  
  
## <a name="modifying-the-selectcommand"></a><span data-ttu-id="80c2e-154">修改 SelectCommand</span><span class="sxs-lookup"><span data-stu-id="80c2e-154">Modifying the SelectCommand</span></span>  

 <span data-ttu-id="80c2e-155">如果您在自动生成 INSERT、UPDATE 或 DELETE 命令后修改 `CommandText` 的 `SelectCommand`，则可能会发生异常。</span><span class="sxs-lookup"><span data-stu-id="80c2e-155">If you modify the `CommandText` of the `SelectCommand` after the INSERT, UPDATE, or DELETE commands have been automatically generated, an exception may occur.</span></span> <span data-ttu-id="80c2e-156">如果修改后的 `SelectCommand.CommandText` 包含的架构信息与自动生成 INSERT、UPDATE 或 DELETE 命令时使用的 `SelectCommand.CommandText` 不一致，则以后对 `DataAdapter.Update` 方法的调用可能会试图访问 `SelectCommand` 所引用的当前表中已不存在的列，并且将会引发异常。</span><span class="sxs-lookup"><span data-stu-id="80c2e-156">If the modified `SelectCommand.CommandText` contains schema information that is inconsistent with the `SelectCommand.CommandText` used when the insert, update, or delete commands were automatically generated, future calls to the `DataAdapter.Update` method may attempt to access columns that no longer exist in the current table referenced by the `SelectCommand`, and an exception will be thrown.</span></span>  
  
 <span data-ttu-id="80c2e-157">可以通过调用 `CommandBuilder` 的 `RefreshSchema` 方法来刷新由 `CommandBuilder` 用于自动生成命令的架构信息。</span><span class="sxs-lookup"><span data-stu-id="80c2e-157">You can refresh the schema information used by the `CommandBuilder` to automatically generate commands by calling the `RefreshSchema` method of the `CommandBuilder`.</span></span>  
  
 <span data-ttu-id="80c2e-158">如果您想知道自动生成了哪个命令，可以使用 `GetInsertCommand` 对象的 `GetUpdateCommand`、`GetDeleteCommand` 和 `CommandBuilder` 方法并检查关联命令的 `CommandText` 属性，以获得对自动生成命令的引用。</span><span class="sxs-lookup"><span data-stu-id="80c2e-158">If you want to know what command was automatically generated, you can obtain a reference to the automatically generated commands by using the `GetInsertCommand`, `GetUpdateCommand`, and `GetDeleteCommand` methods of the `CommandBuilder` object and checking the `CommandText` property of the associated command.</span></span>  
  
 <span data-ttu-id="80c2e-159">以下代码示例向控制台写入已自动生成的更新命令。</span><span class="sxs-lookup"><span data-stu-id="80c2e-159">The following code example writes to the console the update command that was automatically generated.</span></span>  
  
```vb
Console.WriteLine(builder.GetUpdateCommand().CommandText)  
```

```csharp
Console.WriteLine(builder.GetUpdateCommand().CommandText);
```
  
 <span data-ttu-id="80c2e-160">下面的示例在 `Customers` 数据集中重新创建 `custDS` 表。</span><span class="sxs-lookup"><span data-stu-id="80c2e-160">The following example recreates the `Customers` table in the `custDS` dataset.</span></span> <span data-ttu-id="80c2e-161">然后调用 RefreshSchema 方法，使用此新列的信息来刷新自动生成的命令。</span><span class="sxs-lookup"><span data-stu-id="80c2e-161">The **RefreshSchema** method is called to refresh the automatically generated commands with this new column information.</span></span>  
  
```vb  
' Assumes an open SqlConnection and SqlDataAdapter inside of a Using block.  
adapter.SelectCommand.CommandText = _  
  "SELECT CustomerID, ContactName FROM dbo.Customers"  
builder.RefreshSchema()  
  
custDS.Tables.Remove(custDS.Tables("Customers"))  
adapter.Fill(custDS, "Customers")  
```  
  
```csharp  
// Assumes an open SqlConnection and SqlDataAdapter inside of a using block.  
adapter.SelectCommand.CommandText =
  "SELECT CustomerID, ContactName FROM dbo.Customers";  
builder.RefreshSchema();  
  
custDS.Tables.Remove(custDS.Tables["Customers"]);  
adapter.Fill(custDS, "Customers");  
```  
  
## <a name="see-also"></a><span data-ttu-id="80c2e-162">请参阅</span><span class="sxs-lookup"><span data-stu-id="80c2e-162">See also</span></span>

- [<span data-ttu-id="80c2e-163">命令和参数</span><span class="sxs-lookup"><span data-stu-id="80c2e-163">Commands and Parameters</span></span>](commands-and-parameters.md)
- [<span data-ttu-id="80c2e-164">执行命令</span><span class="sxs-lookup"><span data-stu-id="80c2e-164">Executing a Command</span></span>](executing-a-command.md)
- [<span data-ttu-id="80c2e-165">DbConnection、DbCommand 和 DbException</span><span class="sxs-lookup"><span data-stu-id="80c2e-165">DbConnection, DbCommand and DbException</span></span>](dbconnection-dbcommand-and-dbexception.md)
- [<span data-ttu-id="80c2e-166">ADO.NET 概述</span><span class="sxs-lookup"><span data-stu-id="80c2e-166">ADO.NET Overview</span></span>](ado-net-overview.md)
