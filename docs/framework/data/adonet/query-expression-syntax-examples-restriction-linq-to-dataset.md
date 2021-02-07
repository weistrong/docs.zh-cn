---
description: '了解详细信息：查询表达式语法示例：限制 (LINQ to DataSet) '
title: 查询表达式语法示例：限制 (LINQ to DataSet)
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 1daf42c2-c9f4-4cda-b291-7641b9c6d3fe
ms.openlocfilehash: 06ffaa782a02191be4c9568587824ec1767f1249
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99695978"
---
# <a name="query-expression-syntax-examples-restriction-linq-to-dataset"></a><span data-ttu-id="cab23-103">查询表达式语法示例：限制 (LINQ to DataSet)</span><span class="sxs-lookup"><span data-stu-id="cab23-103">Query Expression Syntax Examples: Restriction (LINQ to DataSet)</span></span>

<span data-ttu-id="cab23-104">本主题中的示例演示如何使用 <xref:System.Linq.Enumerable.Where%2A> 方法以便使用查询表达式语法来查询 <xref:System.Data.DataSet>。</span><span class="sxs-lookup"><span data-stu-id="cab23-104">The examples in this topic demonstrate how to use the <xref:System.Linq.Enumerable.Where%2A> method to query a <xref:System.Data.DataSet> using the query expression syntax.</span></span>  
  
 <span data-ttu-id="cab23-105">在 `FillDataSet` 这些示例中使用的方法是在将 [数据加载到数据集](loading-data-into-a-dataset.md)时指定的。</span><span class="sxs-lookup"><span data-stu-id="cab23-105">The `FillDataSet` method used in these examples is specified in [Loading Data Into a DataSet](loading-data-into-a-dataset.md).</span></span>  
  
 <span data-ttu-id="cab23-106">本主题中的示例使用 AdventureWorks 示例数据库中的 Contact、Address、Product、SalesOrderHeader 和 SalesOrderDetail 表。</span><span class="sxs-lookup"><span data-stu-id="cab23-106">The examples in this topic use the Contact, Address, Product, SalesOrderHeader, and SalesOrderDetail tables in the AdventureWorks sample database.</span></span>  
  
 <span data-ttu-id="cab23-107">本主题中的示例使用以下 `using` / `Imports` 语句：</span><span class="sxs-lookup"><span data-stu-id="cab23-107">The examples in this topic use the following `using`/`Imports` statements:</span></span>  
  
[!code-csharp[DP LINQ to DataSetExamples#ImportsUsing](../../../../samples/snippets/csharp/VS_Snippets_ADO.NET/DP LINQ to DataSet Examples/CS/Program.cs#importsusing)]
  
 <span data-ttu-id="cab23-108">有关详细信息，请参阅 [如何：在 Visual Studio 中创建 LINQ to DataSet 项目](how-to-create-a-linq-to-dataset-project-in-vs.md)。</span><span class="sxs-lookup"><span data-stu-id="cab23-108">For more information, see [How to: Create a LINQ to DataSet Project In Visual Studio](how-to-create-a-linq-to-dataset-project-in-vs.md).</span></span>  
  
## <a name="where"></a><span data-ttu-id="cab23-109">其中</span><span class="sxs-lookup"><span data-stu-id="cab23-109">Where</span></span>  
  
### <a name="example"></a><span data-ttu-id="cab23-110">示例</span><span class="sxs-lookup"><span data-stu-id="cab23-110">Example</span></span>  

 <span data-ttu-id="cab23-111">此示例返回所有联机订单。</span><span class="sxs-lookup"><span data-stu-id="cab23-111">This example returns all online orders.</span></span>  
  
 [!code-csharp[DP LINQ to DataSet Examples#Where1](../../../../samples/snippets/csharp/VS_Snippets_ADO.NET/DP LINQ to DataSet Examples/CS/Program.cs#where1)]  
 [!code-vb[DP LINQ to DataSet Examples#Where1](../../../../samples/snippets/visualbasic/VS_Snippets_ADO.NET/DP LINQ to DataSet Examples/VB/Module1.vb#where1)]
  
### <a name="example"></a><span data-ttu-id="cab23-112">示例</span><span class="sxs-lookup"><span data-stu-id="cab23-112">Example</span></span>  

 <span data-ttu-id="cab23-113">此示例返回订单数量大于 2 且小于 6 的订单。</span><span class="sxs-lookup"><span data-stu-id="cab23-113">This example returns the orders where the order quantity is greater than 2 and less than 6.</span></span>  
  
 [!code-csharp[DP LINQ to DataSet Examples#Where2](../../../../samples/snippets/csharp/VS_Snippets_ADO.NET/DP LINQ to DataSet Examples/CS/Program.cs#where2)]  
 [!code-vb[DP LINQ to DataSet Examples#Where2](../../../../samples/snippets/visualbasic/VS_Snippets_ADO.NET/DP LINQ to DataSet Examples/VB/Module1.vb#where2)]
  
### <a name="example"></a><span data-ttu-id="cab23-114">示例</span><span class="sxs-lookup"><span data-stu-id="cab23-114">Example</span></span>  

 <span data-ttu-id="cab23-115">此示例返回所有颜色为红色的产品。</span><span class="sxs-lookup"><span data-stu-id="cab23-115">This example returns all red colored products.</span></span>  
  
 [!code-csharp[DP LINQ to DataSet Examples#Where3](../../../../samples/snippets/csharp/VS_Snippets_ADO.NET/DP LINQ to DataSet Examples/CS/Program.cs#where3)]  
 [!code-vb[DP LINQ to DataSet Examples#Where3](../../../../samples/snippets/visualbasic/VS_Snippets_ADO.NET/DP LINQ to DataSet Examples/VB/Module1.vb#where3)]
  
### <a name="example"></a><span data-ttu-id="cab23-116">示例</span><span class="sxs-lookup"><span data-stu-id="cab23-116">Example</span></span>  

 <span data-ttu-id="cab23-117">此示例使用 <xref:System.Linq.Enumerable.Where%2A> 方法查找 2002 年 12 月 1 日之后达成的订单，然后使用 <xref:System.Data.DataRow.GetChildRows%2A> 方法获取每个订单的详细信息。</span><span class="sxs-lookup"><span data-stu-id="cab23-117">This example uses the <xref:System.Linq.Enumerable.Where%2A> method to find orders that were made after December 1, 2002 and then uses the <xref:System.Data.DataRow.GetChildRows%2A> method to get the details for each order.</span></span>  
  
 [!code-csharp[DP LINQ to DataSetExamples#WhereDrillDown](../../../../samples/snippets/csharp/VS_Snippets_ADO.NET/DP LINQ to DataSet Examples/CS/Program.cs#wheredrilldown)]
 [!code-vb[DP LINQ to DataSet Examples#WhereDrillDown](../../../../samples/snippets/visualbasic/VS_Snippets_ADO.NET/DP LINQ to DataSet Examples/VB/Module1.vb#wheredrilldown)]  
  
## <a name="see-also"></a><span data-ttu-id="cab23-118">请参阅</span><span class="sxs-lookup"><span data-stu-id="cab23-118">See also</span></span>

- [<span data-ttu-id="cab23-119">将数据加载到数据集中</span><span class="sxs-lookup"><span data-stu-id="cab23-119">Loading Data Into a DataSet</span></span>](loading-data-into-a-dataset.md)
- [<span data-ttu-id="cab23-120">LINQ to DataSet 示例</span><span class="sxs-lookup"><span data-stu-id="cab23-120">LINQ to DataSet Examples</span></span>](linq-to-dataset-examples.md)
- [<span data-ttu-id="cab23-121">标准查询运算符概述 (C#)</span><span class="sxs-lookup"><span data-stu-id="cab23-121">Standard Query Operators Overview (C#)</span></span>](../../../csharp/programming-guide/concepts/linq/standard-query-operators-overview.md)
- [<span data-ttu-id="cab23-122">标准查询运算符概述 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="cab23-122">Standard Query Operators Overview (Visual Basic)</span></span>](../../../visual-basic/programming-guide/concepts/linq/standard-query-operators-overview.md)
