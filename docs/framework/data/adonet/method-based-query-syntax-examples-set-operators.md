---
description: '了解详细信息： Method-Based 查询语法示例： Set Operators (LINQ to DataSet) '
title: 基于方法的查询语法示例：集运算符 (LINQ to DataSet)
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: fa93af15-28af-4b5e-846b-897308410edb
ms.openlocfilehash: 3a50c9793e3af6fdab08227b4789c4042dd64931
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99723745"
---
# <a name="method-based-query-syntax-examples-set-operators-linq-to-dataset"></a><span data-ttu-id="a63f2-103">基于方法的查询语法示例：集运算符 (LINQ to DataSet)</span><span class="sxs-lookup"><span data-stu-id="a63f2-103">Method-Based Query Syntax Examples: Set Operators (LINQ to DataSet)</span></span>

<span data-ttu-id="a63f2-104">本主题中的示例演示如何使用 <xref:System.Linq.Enumerable.Distinct%2A> 、 <xref:System.Linq.Enumerable.Except%2A> 、 <xref:System.Linq.Enumerable.Intersect%2A> 和 <xref:System.Linq.Enumerable.Union%2A> 运算符对数据行集执行基于值的比较运算。[将数据加载到数据集](loading-data-into-a-dataset.md) 。有关的详细信息，请参阅 [比较 datarow](comparing-datarows-linq-to-dataset.md) <xref:System.Data.DataRowComparer> 。</span><span class="sxs-lookup"><span data-stu-id="a63f2-104">The examples in this topic demonstrate how to use the <xref:System.Linq.Enumerable.Distinct%2A>, <xref:System.Linq.Enumerable.Except%2A>, <xref:System.Linq.Enumerable.Intersect%2A>, and <xref:System.Linq.Enumerable.Union%2A> operators to perform value-based comparison operations on sets of data rows.[Loading Data Into a DataSet](loading-data-into-a-dataset.md) See [Comparing DataRows](comparing-datarows-linq-to-dataset.md) for more information on <xref:System.Data.DataRowComparer>.</span></span>  
  
 <span data-ttu-id="a63f2-105">在 `FillDataSet` 这些示例中使用的方法是在将 [数据加载到数据集](loading-data-into-a-dataset.md)时指定的。</span><span class="sxs-lookup"><span data-stu-id="a63f2-105">The `FillDataSet` method used in these examples is specified in [Loading Data Into a DataSet](loading-data-into-a-dataset.md).</span></span>  
  
 <span data-ttu-id="a63f2-106">本主题中的示例使用 AdventureWorks 示例数据库中的 Contact、Address、Product、SalesOrderHeader 和 SalesOrderDetail 表。</span><span class="sxs-lookup"><span data-stu-id="a63f2-106">The examples in this topic use the Contact, Address, Product, SalesOrderHeader, and SalesOrderDetail tables in the AdventureWorks sample database.</span></span>  
  
 <span data-ttu-id="a63f2-107">本主题中的示例使用以下 `using` / `Imports` 语句：</span><span class="sxs-lookup"><span data-stu-id="a63f2-107">The examples in this topic use the following `using`/`Imports` statements:</span></span>  
  
 [!code-csharp[DP LINQ to DataSet Examples#ImportsUsing](../../../../samples/snippets/csharp/VS_Snippets_ADO.NET/DP LINQ to DataSet Examples/CS/Program.cs#importsusing)]
 [!code-vb[DP LINQ to DataSet Examples#ImportsUsing](../../../../samples/snippets/visualbasic/VS_Snippets_ADO.NET/DP LINQ to DataSet Examples/VB/Module1.vb#importsusing)]  
  
 <span data-ttu-id="a63f2-108">有关详细信息，请参阅 [如何：在 Visual Studio 中创建 LINQ to DataSet 项目](how-to-create-a-linq-to-dataset-project-in-vs.md)。</span><span class="sxs-lookup"><span data-stu-id="a63f2-108">For more information, see [How to: Create a LINQ to DataSet Project In Visual Studio](how-to-create-a-linq-to-dataset-project-in-vs.md).</span></span>  
  
## <a name="distinct"></a><span data-ttu-id="a63f2-109">Distinct</span><span class="sxs-lookup"><span data-stu-id="a63f2-109">Distinct</span></span>  
  
### <a name="example"></a><span data-ttu-id="a63f2-110">示例</span><span class="sxs-lookup"><span data-stu-id="a63f2-110">Example</span></span>  

 <span data-ttu-id="a63f2-111">此示例使用 <xref:System.Linq.Enumerable.Distinct%2A> 方法移除序列中的重复元素。</span><span class="sxs-lookup"><span data-stu-id="a63f2-111">This example uses the <xref:System.Linq.Enumerable.Distinct%2A> method to remove duplicate elements in a sequence.</span></span>  
  
 [!code-csharp[DP LINQ to DataSet Examples#DistinctRows](../../../../samples/snippets/csharp/VS_Snippets_ADO.NET/DP LINQ to DataSet Examples/CS/Program.cs#distinctrows)]
 [!code-vb[DP LINQ to DataSet Examples#DistinctRows](../../../../samples/snippets/visualbasic/VS_Snippets_ADO.NET/DP LINQ to DataSet Examples/VB/Module1.vb#distinctrows)]  
  
## <a name="except"></a><span data-ttu-id="a63f2-112">Except</span><span class="sxs-lookup"><span data-stu-id="a63f2-112">Except</span></span>  
  
### <a name="example"></a><span data-ttu-id="a63f2-113">示例</span><span class="sxs-lookup"><span data-stu-id="a63f2-113">Example</span></span>  

 <span data-ttu-id="a63f2-114">此示例使用 <xref:System.Linq.Enumerable.Except%2A> 方法返回出现在第一个表中但不出现在第二个表中的联系人。</span><span class="sxs-lookup"><span data-stu-id="a63f2-114">This example uses the <xref:System.Linq.Enumerable.Except%2A> method to return contacts that appear in the first table but not in the second.</span></span>  
  
 [!code-csharp[DP LINQ to DataSet Examples#Except2](../../../../samples/snippets/csharp/VS_Snippets_ADO.NET/DP LINQ to DataSet Examples/CS/Program.cs#except2)]
 [!code-vb[DP LINQ to DataSet Examples#Except2](../../../../samples/snippets/visualbasic/VS_Snippets_ADO.NET/DP LINQ to DataSet Examples/VB/Module1.vb#except2)]  
  
## <a name="intersect"></a><span data-ttu-id="a63f2-115">相交</span><span class="sxs-lookup"><span data-stu-id="a63f2-115">Intersect</span></span>  
  
### <a name="example"></a><span data-ttu-id="a63f2-116">示例</span><span class="sxs-lookup"><span data-stu-id="a63f2-116">Example</span></span>  

 <span data-ttu-id="a63f2-117">此示例使用 <xref:System.Linq.Enumerable.Intersect%2A> 方法返回同时出现在两个表中的联系人。</span><span class="sxs-lookup"><span data-stu-id="a63f2-117">This example uses the <xref:System.Linq.Enumerable.Intersect%2A> method to return contacts that appear in both tables.</span></span>  
  
 [!code-csharp[DP LINQ to DataSet Examples#Intersect2](../../../../samples/snippets/csharp/VS_Snippets_ADO.NET/DP LINQ to DataSet Examples/CS/Program.cs#intersect2)]
 [!code-vb[DP LINQ to DataSet Examples#Intersect2](../../../../samples/snippets/visualbasic/VS_Snippets_ADO.NET/DP LINQ to DataSet Examples/VB/Module1.vb#intersect2)]  
  
## <a name="union"></a><span data-ttu-id="a63f2-118">Union</span><span class="sxs-lookup"><span data-stu-id="a63f2-118">Union</span></span>  
  
### <a name="example"></a><span data-ttu-id="a63f2-119">示例</span><span class="sxs-lookup"><span data-stu-id="a63f2-119">Example</span></span>  

 <span data-ttu-id="a63f2-120">此示例使用 <xref:System.Linq.Enumerable.Union%2A> 方法返回这两个表的任一表中特有的联系人。</span><span class="sxs-lookup"><span data-stu-id="a63f2-120">This example uses the <xref:System.Linq.Enumerable.Union%2A> method to return unique contacts from either of the two tables.</span></span>  
  
 [!code-csharp[DP LINQ to DataSet Examples#Union2](../../../../samples/snippets/csharp/VS_Snippets_ADO.NET/DP LINQ to DataSet Examples/CS/Program.cs#union2)]
 [!code-vb[DP LINQ to DataSet Examples#Union2](../../../../samples/snippets/visualbasic/VS_Snippets_ADO.NET/DP LINQ to DataSet Examples/VB/Module1.vb#union2)]  
  
## <a name="see-also"></a><span data-ttu-id="a63f2-121">请参阅</span><span class="sxs-lookup"><span data-stu-id="a63f2-121">See also</span></span>

- [<span data-ttu-id="a63f2-122">将数据加载到数据集中</span><span class="sxs-lookup"><span data-stu-id="a63f2-122">Loading Data Into a DataSet</span></span>](loading-data-into-a-dataset.md)
- [<span data-ttu-id="a63f2-123">LINQ to DataSet 示例</span><span class="sxs-lookup"><span data-stu-id="a63f2-123">LINQ to DataSet Examples</span></span>](linq-to-dataset-examples.md)
- [<span data-ttu-id="a63f2-124">标准查询运算符概述 (C#)</span><span class="sxs-lookup"><span data-stu-id="a63f2-124">Standard Query Operators Overview (C#)</span></span>](../../../csharp/programming-guide/concepts/linq/standard-query-operators-overview.md)
- [<span data-ttu-id="a63f2-125">标准查询运算符概述 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="a63f2-125">Standard Query Operators Overview (Visual Basic)</span></span>](../../../visual-basic/programming-guide/concepts/linq/standard-query-operators-overview.md)
