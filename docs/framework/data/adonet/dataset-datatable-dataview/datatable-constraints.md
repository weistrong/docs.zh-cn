---
description: 了解详细信息： DataTable 约束
title: 数据表约束
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 27c9f2fd-f64d-4b4e-bbf6-1d24f47067cb
ms.openlocfilehash: 0c712115fd87fefae3578b2f3fc0adfc416f412e
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99724903"
---
# <a name="datatable-constraints"></a><span data-ttu-id="71f63-103">数据表约束</span><span class="sxs-lookup"><span data-stu-id="71f63-103">DataTable Constraints</span></span>

<span data-ttu-id="71f63-104">为了维护数据的完整性，可以使用约束来对 <xref:System.Data.DataTable> 中的数据施加限制。</span><span class="sxs-lookup"><span data-stu-id="71f63-104">You can use constraints to enforce restrictions on the data in a <xref:System.Data.DataTable>, in order to maintain the integrity of the data.</span></span> <span data-ttu-id="71f63-105">约束是应用于某列或相关各列的自动规则，它决定了某行的值以某种方式更改时的操作过程。</span><span class="sxs-lookup"><span data-stu-id="71f63-105">A constraint is an automatic rule, applied to a column or related columns, that determines the course of action when the value of a row is somehow altered.</span></span> <span data-ttu-id="71f63-106">当 `System.Data.DataSet.EnforceConstraints` 的属性 <xref:System.Data.DataSet> 为 **true** 时，将强制实施约束。</span><span class="sxs-lookup"><span data-stu-id="71f63-106">Constraints are enforced when the `System.Data.DataSet.EnforceConstraints` property of the <xref:System.Data.DataSet> is **true**.</span></span> <span data-ttu-id="71f63-107">有关显示如何设置 `EnforceConstraints` 属性的代码示例，请参见 <xref:System.Data.DataSet.EnforceConstraints%2A> 参考主题。</span><span class="sxs-lookup"><span data-stu-id="71f63-107">For a code example that shows how to set the `EnforceConstraints` property, see the <xref:System.Data.DataSet.EnforceConstraints%2A> reference topic.</span></span>  
  
 <span data-ttu-id="71f63-108">ADO.NET 中有两种约束：<xref:System.Data.ForeignKeyConstraint> 和 <xref:System.Data.UniqueConstraint>。</span><span class="sxs-lookup"><span data-stu-id="71f63-108">There are two kinds of constraints in ADO.NET: the <xref:System.Data.ForeignKeyConstraint> and the <xref:System.Data.UniqueConstraint>.</span></span> <span data-ttu-id="71f63-109">默认情况下，通过将添加 <xref:System.Data.DataRelation> 到 **数据集**，可以在创建两个或多个表之间创建关系时自动创建这两个约束。</span><span class="sxs-lookup"><span data-stu-id="71f63-109">By default, both constraints are created automatically when you create a relationship between two or more tables by adding a <xref:System.Data.DataRelation> to the **DataSet**.</span></span> <span data-ttu-id="71f63-110">不过，您可以  =  在创建关系时指定 createConstraints **false** 来禁用此行为。</span><span class="sxs-lookup"><span data-stu-id="71f63-110">However, you can disable this behavior by specifying **createConstraints** = **false** when creating the relation.</span></span>  
  
## <a name="foreignkeyconstraint"></a><span data-ttu-id="71f63-111">ForeignKeyConstraint</span><span class="sxs-lookup"><span data-stu-id="71f63-111">ForeignKeyConstraint</span></span>  

 <span data-ttu-id="71f63-112">**ForeignKeyConstraint** 强制执行有关如何传播相关表的更新和删除的规则。</span><span class="sxs-lookup"><span data-stu-id="71f63-112">A **ForeignKeyConstraint** enforces rules about how updates and deletes to related tables are propagated.</span></span> <span data-ttu-id="71f63-113">例如，如果更新或删除了一个表的行中的值，并且在一个或多个相关表中也使用相同的值，则 **ForeignKeyConstraint** 将确定相关表中发生的情况。</span><span class="sxs-lookup"><span data-stu-id="71f63-113">For example, if a value in a row of one table is updated or deleted, and that same value is also used in one or more related tables, a **ForeignKeyConstraint** determines what happens in the related tables.</span></span>  
  
 <span data-ttu-id="71f63-114"><xref:System.Data.ForeignKeyConstraint.DeleteRule%2A>ForeignKeyConstraint 的和 <xref:System.Data.ForeignKeyConstraint.UpdateRule%2A> 属性定义用户尝试删除或更新相关表中的行时要执行的操作。</span><span class="sxs-lookup"><span data-stu-id="71f63-114">The <xref:System.Data.ForeignKeyConstraint.DeleteRule%2A> and <xref:System.Data.ForeignKeyConstraint.UpdateRule%2A> properties of the **ForeignKeyConstraint** define the action to be taken when the user attempts to delete or update a row in a related table.</span></span> <span data-ttu-id="71f63-115">下表描述了可用于 **ForeignKeyConstraint** 的 **DeleteRule** 和 **UpdateRule** 属性的不同设置。</span><span class="sxs-lookup"><span data-stu-id="71f63-115">The following table describes the different settings available for the **DeleteRule** and **UpdateRule** properties of the **ForeignKeyConstraint**.</span></span>  
  
|<span data-ttu-id="71f63-116">规则设置</span><span class="sxs-lookup"><span data-stu-id="71f63-116">Rule setting</span></span>|<span data-ttu-id="71f63-117">说明</span><span class="sxs-lookup"><span data-stu-id="71f63-117">Description</span></span>|  
|------------------|-----------------|  
|<span data-ttu-id="71f63-118">**Cascade**</span><span class="sxs-lookup"><span data-stu-id="71f63-118">**Cascade**</span></span>|<span data-ttu-id="71f63-119">删除或更新相关的行。</span><span class="sxs-lookup"><span data-stu-id="71f63-119">Delete or update related rows.</span></span>|  
|<span data-ttu-id="71f63-120">**SetNull**</span><span class="sxs-lookup"><span data-stu-id="71f63-120">**SetNull**</span></span>|<span data-ttu-id="71f63-121">将相关行中的值设置为 **DBNull**。</span><span class="sxs-lookup"><span data-stu-id="71f63-121">Set values in related rows to **DBNull**.</span></span>|  
|<span data-ttu-id="71f63-122">**SetDefault**</span><span class="sxs-lookup"><span data-stu-id="71f63-122">**SetDefault**</span></span>|<span data-ttu-id="71f63-123">将相关行中的值设置为默认值。</span><span class="sxs-lookup"><span data-stu-id="71f63-123">Set values in related rows to the default value.</span></span>|  
|<span data-ttu-id="71f63-124">**无**</span><span class="sxs-lookup"><span data-stu-id="71f63-124">**None**</span></span>|<span data-ttu-id="71f63-125">对相关行不执行任何操作。</span><span class="sxs-lookup"><span data-stu-id="71f63-125">Take no action on related rows.</span></span> <span data-ttu-id="71f63-126">这是默认设置。</span><span class="sxs-lookup"><span data-stu-id="71f63-126">This is the default.</span></span>|  
  
 <span data-ttu-id="71f63-127">**ForeignKeyConstraint** 可以限制并传播对相关列的更改。</span><span class="sxs-lookup"><span data-stu-id="71f63-127">A **ForeignKeyConstraint** can restrict, as well as propagate, changes to related columns.</span></span> <span data-ttu-id="71f63-128">根据为列的 **ForeignKeyConstraint** 设置的属性，如果 **DataSet** 的 **EnforceConstraints** 属性为 **true**，则对父行执行某些操作将导致异常。</span><span class="sxs-lookup"><span data-stu-id="71f63-128">Depending on the properties set for the **ForeignKeyConstraint** of a column, if the **EnforceConstraints** property of the **DataSet** is **true**, performing certain operations on the parent row will result in an exception.</span></span> <span data-ttu-id="71f63-129">例如，如果 **ForeignKeyConstraint** 的 **DeleteRule** 属性为 **None**，则如果父行具有任何子行，则不能将其删除。</span><span class="sxs-lookup"><span data-stu-id="71f63-129">For example, if the **DeleteRule** property of the **ForeignKeyConstraint** is **None**, a parent row cannot be deleted if it has any child rows.</span></span>  
  
 <span data-ttu-id="71f63-130">您可以使用 **ForeignKeyConstraint** 构造函数在单个列之间或列的数组之间创建外键约束。</span><span class="sxs-lookup"><span data-stu-id="71f63-130">You can create a foreign key constraint between single columns or between an array of columns by using the **ForeignKeyConstraint** constructor.</span></span> <span data-ttu-id="71f63-131">将生成的 **ForeignKeyConstraint** 对象传递给表的 **约束** 属性的 **Add** 方法，该属性是一个 **ConstraintCollection**。</span><span class="sxs-lookup"><span data-stu-id="71f63-131">Pass the resulting **ForeignKeyConstraint** object to the **Add** method of the table's **Constraints** property, which is a **ConstraintCollection**.</span></span> <span data-ttu-id="71f63-132">还可以将构造函数参数传递给 **ConstraintCollection** 的 **Add** 方法的几个重载，以创建 **ForeignKeyConstraint**。</span><span class="sxs-lookup"><span data-stu-id="71f63-132">You can also pass constructor arguments to several overloads of the **Add** method of a **ConstraintCollection** to create a **ForeignKeyConstraint**.</span></span>  
  
 <span data-ttu-id="71f63-133">当创建 **ForeignKeyConstraint** 时，可以将 **DeleteRule** 和 **UpdateRule** 值作为参数传递给构造函数，也可以将它们设置为属性，如以下示例所示 (其中 **DeleteRule** 值设置为 **None**) 。</span><span class="sxs-lookup"><span data-stu-id="71f63-133">When creating a **ForeignKeyConstraint**, you can pass the **DeleteRule** and **UpdateRule** values to the constructor as arguments, or you can set them as properties as in the following example (where the **DeleteRule** value is set to **None**).</span></span>  
  
```vb  
Dim custOrderFK As ForeignKeyConstraint = New ForeignKeyConstraint("CustOrderFK", _  
  custDS.Tables("CustTable").Columns("CustomerID"), _  
  custDS.Tables("OrdersTable").Columns("CustomerID"))  
custOrderFK.DeleteRule = Rule.None
' Cannot delete a customer value that has associated existing orders.  
custDS.Tables("OrdersTable").Constraints.Add(custOrderFK)  
```  
  
```csharp  
ForeignKeyConstraint custOrderFK = new ForeignKeyConstraint("CustOrderFK",  
  custDS.Tables["CustTable"].Columns["CustomerID"],
  custDS.Tables["OrdersTable"].Columns["CustomerID"]);  
custOrderFK.DeleteRule = Rule.None;
// Cannot delete a customer value that has associated existing orders.  
custDS.Tables["OrdersTable"].Constraints.Add(custOrderFK);  
```  
  
### <a name="acceptrejectrule"></a><span data-ttu-id="71f63-134">AcceptRejectRule</span><span class="sxs-lookup"><span data-stu-id="71f63-134">AcceptRejectRule</span></span>  

 <span data-ttu-id="71f63-135">可以使用 **AcceptChanges** 方法接受对行的更改，或使用 **DataSet**、 **DataTable** 或 **DataRow** 的 **RejectChanges** 方法取消对行的更改。</span><span class="sxs-lookup"><span data-stu-id="71f63-135">Changes to rows can be accepted using the **AcceptChanges** method or canceled using the **RejectChanges** method of the **DataSet**, **DataTable**, or **DataRow**.</span></span> <span data-ttu-id="71f63-136">当 **数据集** 包含 **ForeignKeyConstraints** 时，调用 **AcceptChanges** 或 **RejectChanges** 方法会强制执行 **AcceptRejectRule**。</span><span class="sxs-lookup"><span data-stu-id="71f63-136">When a **DataSet** contains **ForeignKeyConstraints**, invoking the **AcceptChanges** or **RejectChanges** methods enforces the **AcceptRejectRule**.</span></span> <span data-ttu-id="71f63-137">**ForeignKeyConstraint** 的 **AcceptRejectRule** 属性决定了对父行调用 **AcceptChanges** 或 **RejectChanges** 时要对子行执行的操作。</span><span class="sxs-lookup"><span data-stu-id="71f63-137">The **AcceptRejectRule** property of the **ForeignKeyConstraint** determines which action will be taken on the child rows when **AcceptChanges** or **RejectChanges** is called on the parent row.</span></span>  
  
 <span data-ttu-id="71f63-138">下表列出了 **AcceptRejectRule** 的可用设置。</span><span class="sxs-lookup"><span data-stu-id="71f63-138">The following table lists the available settings for the **AcceptRejectRule**.</span></span>  
  
|<span data-ttu-id="71f63-139">规则设置</span><span class="sxs-lookup"><span data-stu-id="71f63-139">Rule setting</span></span>|<span data-ttu-id="71f63-140">说明</span><span class="sxs-lookup"><span data-stu-id="71f63-140">Description</span></span>|  
|------------------|-----------------|  
|<span data-ttu-id="71f63-141">**Cascade**</span><span class="sxs-lookup"><span data-stu-id="71f63-141">**Cascade**</span></span>|<span data-ttu-id="71f63-142">接受或拒绝对子行的更改。</span><span class="sxs-lookup"><span data-stu-id="71f63-142">Accept or reject changes to child rows.</span></span>|  
|<span data-ttu-id="71f63-143">**无**</span><span class="sxs-lookup"><span data-stu-id="71f63-143">**None**</span></span>|<span data-ttu-id="71f63-144">对子行不执行任何操作。</span><span class="sxs-lookup"><span data-stu-id="71f63-144">Take no action on child rows.</span></span> <span data-ttu-id="71f63-145">这是默认设置。</span><span class="sxs-lookup"><span data-stu-id="71f63-145">This is the default.</span></span>|  
  
### <a name="example"></a><span data-ttu-id="71f63-146">示例</span><span class="sxs-lookup"><span data-stu-id="71f63-146">Example</span></span>  

 <span data-ttu-id="71f63-147">下面的示例创建一个 <xref:System.Data.ForeignKeyConstraint>，设置它的一些属性（包括 <xref:System.Data.ForeignKeyConstraint.AcceptRejectRule%2A>），并将它添加到 <xref:System.Data.ConstraintCollection> 对象的 <xref:System.Data.DataTable>。</span><span class="sxs-lookup"><span data-stu-id="71f63-147">The following example creates a <xref:System.Data.ForeignKeyConstraint>, sets several of its properties, including the <xref:System.Data.ForeignKeyConstraint.AcceptRejectRule%2A>, and adds it to the <xref:System.Data.ConstraintCollection> of a <xref:System.Data.DataTable> object.</span></span>  
  
 [!code-csharp[DataWorks Data.AcceptRejectRule#1](../../../../../samples/snippets/csharp/VS_Snippets_ADO.NET/DataWorks Data.AcceptRejectRule/CS/source.cs#1)]
 [!code-vb[DataWorks Data.AcceptRejectRule#1](../../../../../samples/snippets/visualbasic/VS_Snippets_ADO.NET/DataWorks Data.AcceptRejectRule/VB/source.vb#1)]  
  
## <a name="uniqueconstraint"></a><span data-ttu-id="71f63-148">UniqueConstraint</span><span class="sxs-lookup"><span data-stu-id="71f63-148">UniqueConstraint</span></span>  

 <span data-ttu-id="71f63-149">**UniqueConstraint** 对象（可分配给 **DataTable** 中的一列或一组列）确保指定的一列或多列中的所有数据对于每行都是唯一的。</span><span class="sxs-lookup"><span data-stu-id="71f63-149">The **UniqueConstraint** object, which can be assigned either to a single column or to an array of columns in a **DataTable**, ensures that all data in the specified column or columns is unique per row.</span></span> <span data-ttu-id="71f63-150">您可以使用 **UniqueConstraint** 构造函数创建列或列数组的唯一约束。</span><span class="sxs-lookup"><span data-stu-id="71f63-150">You can create a unique constraint for a column or array of columns by using the **UniqueConstraint** constructor.</span></span> <span data-ttu-id="71f63-151">将生成的 **UniqueConstraint** 对象传递给表的 **约束** 属性的 **Add** 方法，该属性是一个 **ConstraintCollection**。</span><span class="sxs-lookup"><span data-stu-id="71f63-151">Pass the resulting **UniqueConstraint** object to the **Add** method of the table's **Constraints** property, which is a **ConstraintCollection**.</span></span> <span data-ttu-id="71f63-152">还可以将构造函数参数传递给 **ConstraintCollection** 的 **Add** 方法的几个重载，以创建 **UniqueConstraint**。</span><span class="sxs-lookup"><span data-stu-id="71f63-152">You can also pass constructor arguments to several overloads of the **Add** method of a **ConstraintCollection** to create a **UniqueConstraint**.</span></span> <span data-ttu-id="71f63-153">为一列或多列创建 **UniqueConstraint** 时，可以选择指定列或列是否为主键。</span><span class="sxs-lookup"><span data-stu-id="71f63-153">When creating a **UniqueConstraint** for a column or columns, you can optionally specify whether the column or columns are a primary key.</span></span>  
  
 <span data-ttu-id="71f63-154">还可以通过将列的 **unique** 属性设置为 **true**，为列创建 unique 约束。</span><span class="sxs-lookup"><span data-stu-id="71f63-154">You can also create a unique constraint for a column by setting the **Unique** property of the column to **true**.</span></span> <span data-ttu-id="71f63-155">或者，将单个列的 **unique** 属性设置为 **false** 将删除任何可能存在的唯一约束。</span><span class="sxs-lookup"><span data-stu-id="71f63-155">Alternatively, setting the **Unique** property of a single column to **false** removes any unique constraint that may exist.</span></span> <span data-ttu-id="71f63-156">如果将一列或多列定义为表的主键，会自动为一个或多个指定的列创建唯一的约束。</span><span class="sxs-lookup"><span data-stu-id="71f63-156">Defining a column or columns as the primary key for a table will automatically create a unique constraint for the specified column or columns.</span></span> <span data-ttu-id="71f63-157">如果删除 **DataTable** 的 **PrimaryKey** 属性中的列，则会删除 **UniqueConstraint** 。</span><span class="sxs-lookup"><span data-stu-id="71f63-157">If you remove a column from the **PrimaryKey** property of a **DataTable**, the **UniqueConstraint** is removed.</span></span>  
  
 <span data-ttu-id="71f63-158">下面的示例为 **DataTable** 的两列创建 **UniqueConstraint** 。</span><span class="sxs-lookup"><span data-stu-id="71f63-158">The following example creates a **UniqueConstraint** for two columns of a **DataTable**.</span></span>  
  
```vb  
Dim custTable As DataTable = custDS.Tables("Customers")  
Dim custUnique As UniqueConstraint = _  
    New UniqueConstraint(New DataColumn()   {custTable.Columns("CustomerID"), _  
    custTable.Columns("CompanyName")})  
custDS.Tables("Customers").Constraints.Add(custUnique)  
```  
  
```csharp  
DataTable custTable = custDS.Tables["Customers"];  
UniqueConstraint custUnique = new UniqueConstraint(new DataColumn[]
    {custTable.Columns["CustomerID"],
    custTable.Columns["CompanyName"]});  
custDS.Tables["Customers"].Constraints.Add(custUnique);  
```  
  
## <a name="see-also"></a><span data-ttu-id="71f63-159">请参阅</span><span class="sxs-lookup"><span data-stu-id="71f63-159">See also</span></span>

- <xref:System.Data.DataRelation>
- <xref:System.Data.DataTable>
- <xref:System.Data.ForeignKeyConstraint>
- <xref:System.Data.UniqueConstraint>
- [<span data-ttu-id="71f63-160">数据表架构定义</span><span class="sxs-lookup"><span data-stu-id="71f63-160">DataTable Schema Definition</span></span>](datatable-schema-definition.md)
- [<span data-ttu-id="71f63-161">数据集、数据表和数据视图</span><span class="sxs-lookup"><span data-stu-id="71f63-161">DataSets, DataTables, and DataViews</span></span>](index.md)
- [<span data-ttu-id="71f63-162">ADO.NET 概述</span><span class="sxs-lookup"><span data-stu-id="71f63-162">ADO.NET Overview</span></span>](../ado-net-overview.md)
