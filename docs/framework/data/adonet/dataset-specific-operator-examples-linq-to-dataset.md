---
description: '了解详细信息： DataSet-Specific 运算符示例 (LINQ to DataSet) '
title: 数据集特定的运算符示例 (LINQ to DataSet)
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 8fdd64af-6ad0-46cd-91c8-dbe26620eeb1
ms.openlocfilehash: 2fd54453621ce180901aaf6fbb5b975067ad9831
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99651322"
---
# <a name="dataset-specific-operator-examples-linq-to-dataset"></a><span data-ttu-id="885fa-103">数据集特定的运算符示例 (LINQ to DataSet)</span><span class="sxs-lookup"><span data-stu-id="885fa-103">DataSet-Specific Operator Examples (LINQ to DataSet)</span></span>

<span data-ttu-id="885fa-104">本主题中的示例演示如何使用 <xref:System.Data.DataTableExtensions.CopyToDataTable%2A> 方法和 <xref:System.Data.DataRowComparer> 类。</span><span class="sxs-lookup"><span data-stu-id="885fa-104">The examples in this topic demonstrate how to use the <xref:System.Data.DataTableExtensions.CopyToDataTable%2A> method and the <xref:System.Data.DataRowComparer> class.</span></span>  
  
 <span data-ttu-id="885fa-105">在 `FillDataSet` 这些示例中使用的方法是在将 [数据加载到数据集](loading-data-into-a-dataset.md)时指定的。</span><span class="sxs-lookup"><span data-stu-id="885fa-105">The `FillDataSet` method used in these examples is specified in [Loading Data Into a DataSet](loading-data-into-a-dataset.md).</span></span>  
  
 <span data-ttu-id="885fa-106">本主题中的示例使用 AdventureWorks 示例数据库中的 Contact、Address、Product、SalesOrderHeader 和 SalesOrderDetail 表。</span><span class="sxs-lookup"><span data-stu-id="885fa-106">The examples in this topic use the Contact, Address, Product, SalesOrderHeader, and SalesOrderDetail tables in the AdventureWorks sample database.</span></span>  
  
 <span data-ttu-id="885fa-107">本主题中的示例使用以下 `using` / `Imports` 语句：</span><span class="sxs-lookup"><span data-stu-id="885fa-107">The examples in this topic use the following `using`/`Imports` statements:</span></span>  
  
 [!code-csharp[DP LINQ to DataSet Examples#ImportsUsing](../../../../samples/snippets/csharp/VS_Snippets_ADO.NET/DP LINQ to DataSet Examples/CS/Program.cs#importsusing)]
 [!code-vb[DP LINQ to DataSet Examples#ImportsUsing](../../../../samples/snippets/visualbasic/VS_Snippets_ADO.NET/DP LINQ to DataSet Examples/VB/Module1.vb#importsusing)]  
  
 <span data-ttu-id="885fa-108">有关详细信息，请参阅 [如何：在 Visual Studio 中创建 LINQ to DataSet 项目](how-to-create-a-linq-to-dataset-project-in-vs.md)。</span><span class="sxs-lookup"><span data-stu-id="885fa-108">For more information, see [How to: Create a LINQ to DataSet Project In Visual Studio](how-to-create-a-linq-to-dataset-project-in-vs.md).</span></span>  
  
## <a name="copytodatatable"></a><span data-ttu-id="885fa-109">CopyToDataTable</span><span class="sxs-lookup"><span data-stu-id="885fa-109">CopyToDataTable</span></span>  
  
### <a name="example"></a><span data-ttu-id="885fa-110">示例</span><span class="sxs-lookup"><span data-stu-id="885fa-110">Example</span></span>  

 <span data-ttu-id="885fa-111">此示例通过使用 <xref:System.Data.DataTable> 方法加载包含查询结果的 <xref:System.Data.DataTableExtensions.CopyToDataTable%2A>。</span><span class="sxs-lookup"><span data-stu-id="885fa-111">This example loads a <xref:System.Data.DataTable> with query results by using the <xref:System.Data.DataTableExtensions.CopyToDataTable%2A> method.</span></span>  
  
 [!code-csharp[DP LINQ to DataSet Examples#LoadDataTableWithQueryResults](../../../../samples/snippets/csharp/VS_Snippets_ADO.NET/DP LINQ to DataSet Examples/CS/Program.cs#loaddatatablewithqueryresults)]
 [!code-vb[DP LINQ to DataSet Examples#LoadDataTableWithQueryResults](../../../../samples/snippets/visualbasic/VS_Snippets_ADO.NET/DP LINQ to DataSet Examples/VB/Module1.vb#loaddatatablewithqueryresults)]  
  
## <a name="datarowcomparer"></a><span data-ttu-id="885fa-112">DataRowComparer</span><span class="sxs-lookup"><span data-stu-id="885fa-112">DataRowComparer</span></span>  
  
### <a name="example"></a><span data-ttu-id="885fa-113">示例</span><span class="sxs-lookup"><span data-stu-id="885fa-113">Example</span></span>  

 <span data-ttu-id="885fa-114">此示例通过使用 <xref:System.Data.DataRowComparer> 比较两个不同的数据行。</span><span class="sxs-lookup"><span data-stu-id="885fa-114">This example compares two different data rows by using <xref:System.Data.DataRowComparer>.</span></span>  
  
 [!code-csharp[DP LINQ to DataSet Examples#CompareDifferentDataRows](../../../../samples/snippets/csharp/VS_Snippets_ADO.NET/DP LINQ to DataSet Examples/CS/Program.cs#comparedifferentdatarows)]  
  
## <a name="see-also"></a><span data-ttu-id="885fa-115">请参阅</span><span class="sxs-lookup"><span data-stu-id="885fa-115">See also</span></span>

- [<span data-ttu-id="885fa-116">将数据加载到数据集中</span><span class="sxs-lookup"><span data-stu-id="885fa-116">Loading Data Into a DataSet</span></span>](loading-data-into-a-dataset.md)
- [<span data-ttu-id="885fa-117">LINQ to DataSet 示例</span><span class="sxs-lookup"><span data-stu-id="885fa-117">LINQ to DataSet Examples</span></span>](linq-to-dataset-examples.md)
