---
description: 了解详细信息：查询类型化数据集
title: 查询类型化数据集
ms.date: 08/15/2018
dev_langs:
- csharp
- vb
ms.assetid: ad712fa1-2baf-462a-b163-574cce6d376a
ms.openlocfilehash: 5bcf8bb587a0ed0eaca1bbe9b3a7d7143757780e
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99723694"
---
# <a name="query-typed-datasets"></a><span data-ttu-id="a8dfd-103">查询类型化数据集</span><span class="sxs-lookup"><span data-stu-id="a8dfd-103">Query typed DataSets</span></span>

<span data-ttu-id="a8dfd-104">如果在 <xref:System.Data.DataSet> 应用程序设计时已知的架构，则建议在使用 LINQ to DataSet 时使用类型化 <xref:System.Data.DataSet> 。</span><span class="sxs-lookup"><span data-stu-id="a8dfd-104">If the schema of the <xref:System.Data.DataSet> is known at application design time, we recommend that you use a typed <xref:System.Data.DataSet> when using LINQ to DataSet.</span></span> <span data-ttu-id="a8dfd-105">类型化 <xref:System.Data.DataSet> 是从 <xref:System.Data.DataSet> 中派生的类。</span><span class="sxs-lookup"><span data-stu-id="a8dfd-105">A typed <xref:System.Data.DataSet> is a class that derives from a <xref:System.Data.DataSet>.</span></span> <span data-ttu-id="a8dfd-106">因此，它继承 <xref:System.Data.DataSet> 的所有方法、事件和属性。</span><span class="sxs-lookup"><span data-stu-id="a8dfd-106">As such, it inherits all the methods, events, and properties of a <xref:System.Data.DataSet>.</span></span> <span data-ttu-id="a8dfd-107">此外，类型化 <xref:System.Data.DataSet> 还提供强类型方法、事件和属性。</span><span class="sxs-lookup"><span data-stu-id="a8dfd-107">Additionally, a typed <xref:System.Data.DataSet> provides strongly typed methods, events, and properties.</span></span> <span data-ttu-id="a8dfd-108">这意味着可以按名称而不使用基于集合的方法来访问表和列。</span><span class="sxs-lookup"><span data-stu-id="a8dfd-108">This means that you can access tables and columns by name, instead of using collection-based methods.</span></span> <span data-ttu-id="a8dfd-109">这可使查询更简单、更具可读性。</span><span class="sxs-lookup"><span data-stu-id="a8dfd-109">This makes queries simpler and more readable.</span></span> <span data-ttu-id="a8dfd-110">有关详细信息，请参阅 [类型化数据集](./dataset-datatable-dataview/typed-datasets.md)。</span><span class="sxs-lookup"><span data-stu-id="a8dfd-110">For more information, see [Typed DataSets](./dataset-datatable-dataview/typed-datasets.md).</span></span>

<span data-ttu-id="a8dfd-111">LINQ to DataSet 还支持对类型化进行查询 <xref:System.Data.DataSet> 。</span><span class="sxs-lookup"><span data-stu-id="a8dfd-111">LINQ to DataSet also supports querying over a typed <xref:System.Data.DataSet>.</span></span> <span data-ttu-id="a8dfd-112">对于类型化 <xref:System.Data.DataSet>，您不必使用泛型 <xref:System.Data.DataRowExtensions.Field%2A> 方法或 <xref:System.Data.DataRowExtensions.SetField%2A> 方法即可访问列数据。</span><span class="sxs-lookup"><span data-stu-id="a8dfd-112">With a typed <xref:System.Data.DataSet>, you do not have to use the generic <xref:System.Data.DataRowExtensions.Field%2A> method or <xref:System.Data.DataRowExtensions.SetField%2A> method to access column data.</span></span> <span data-ttu-id="a8dfd-113">由于 <xref:System.Data.DataSet> 中包括类型信息，因此属性名称在编译时可用。</span><span class="sxs-lookup"><span data-stu-id="a8dfd-113">Property names are available at compile time because the type information is included in the <xref:System.Data.DataSet>.</span></span> <span data-ttu-id="a8dfd-114">LINQ to DataSet 提供作为正确类型的列值的访问，以便在编译代码而不是在运行时捕获类型不匹配错误。</span><span class="sxs-lookup"><span data-stu-id="a8dfd-114">LINQ to DataSet provides access to column values as the correct type, so that type mismatch errors are caught when the code is compiled instead of at run time.</span></span>

<span data-ttu-id="a8dfd-115"><xref:System.Data.DataSet>必须先使用 Visual Studio 中的 **数据集设计器** 生成类，然后才能开始查询类型化的。</span><span class="sxs-lookup"><span data-stu-id="a8dfd-115">Before you can begin querying a typed <xref:System.Data.DataSet>, you must generate the class by using the **DataSet Designer** in Visual Studio.</span></span> <span data-ttu-id="a8dfd-116">有关详细信息，请参阅 [创建和配置数据集](/visualstudio/data-tools/create-and-configure-datasets-in-visual-studio)。</span><span class="sxs-lookup"><span data-stu-id="a8dfd-116">For more information, see [Create and configure DataSets](/visualstudio/data-tools/create-and-configure-datasets-in-visual-studio).</span></span>

## <a name="example"></a><span data-ttu-id="a8dfd-117">示例</span><span class="sxs-lookup"><span data-stu-id="a8dfd-117">Example</span></span>

<span data-ttu-id="a8dfd-118">下面的示例演示对类型化 <xref:System.Data.DataSet> 进行查询：</span><span class="sxs-lookup"><span data-stu-id="a8dfd-118">The following example shows a query over a typed <xref:System.Data.DataSet>:</span></span>

```csharp
var query = from o in orders
            where o.OnlineOrderFlag == true
            select new { o.SalesOrderID,
                         o.OrderDate,
                         o.SalesOrderNumber };

foreach(var order in query)
{
    Console.WriteLine("{0}\t{1:d}\t{2}",
      order.SalesOrderID,
      order.OrderDate,
      order.SalesOrderNumber);
}
```

```vb
Dim orders = ds.Tables("SalesOrderHeader")

Dim query = _
       From o In orders _
       Where o.OnlineOrderFlag = True _
       Select New {SalesOrderID := o.SalesOrderID, _
                   OrderDate := o.OrderDate, _
                   SalesOrderNumber := o.SalesOrderNumber}

For Each Dim onlineOrder In query
 Console.WriteLine("{0}\t{1:d}\t{2}", _
 onlineOrder.SalesOrderID, _
 onlineOrder.OrderDate, _
 onlineOrder.SalesOrderNumber)
Next
```

## <a name="see-also"></a><span data-ttu-id="a8dfd-119">请参阅</span><span class="sxs-lookup"><span data-stu-id="a8dfd-119">See also</span></span>

- [<span data-ttu-id="a8dfd-120">查询数据集</span><span class="sxs-lookup"><span data-stu-id="a8dfd-120">Querying DataSets</span></span>](querying-datasets-linq-to-dataset.md)
- [<span data-ttu-id="a8dfd-121">跨表查询</span><span class="sxs-lookup"><span data-stu-id="a8dfd-121">Cross-Table Queries</span></span>](cross-table-queries-linq-to-dataset.md)
- [<span data-ttu-id="a8dfd-122">单表查询</span><span class="sxs-lookup"><span data-stu-id="a8dfd-122">Single-Table Queries</span></span>](single-table-queries-linq-to-dataset.md)
