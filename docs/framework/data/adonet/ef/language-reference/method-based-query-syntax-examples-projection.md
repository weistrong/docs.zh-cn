---
description: 了解详细信息： Method-Based 查询语法示例：投影
title: 基于方法的查询语法示例：投影
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 505491fa-5920-43ce-8a96-c25389e125d8
ms.openlocfilehash: ed4d53166f15f5a2b618ccae92b40fc07d370299
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99696654"
---
# <a name="method-based-query-syntax-examples-projection"></a><span data-ttu-id="e6978-103">基于方法的查询语法示例：投影</span><span class="sxs-lookup"><span data-stu-id="e6978-103">Method-Based Query Syntax Examples: Projection</span></span>

<span data-ttu-id="e6978-104">本主题中的示例演示如何使用 <xref:System.Linq.Enumerable.Select%2A> 和 <xref:System.Linq.Enumerable.SelectMany%2A> 方法通过基于方法的查询语法来查询 [AdventureWorks 销售模型](https://github.com/Microsoft/sql-server-samples/releases/tag/adventureworks) 。</span><span class="sxs-lookup"><span data-stu-id="e6978-104">The examples in this topic demonstrate how to use the <xref:System.Linq.Enumerable.Select%2A> and <xref:System.Linq.Enumerable.SelectMany%2A> methods to query the [AdventureWorks Sales Model](https://github.com/Microsoft/sql-server-samples/releases/tag/adventureworks) using method-based query syntax.</span></span> <span data-ttu-id="e6978-105">这些示例中使用的 AdventureWorks 销售模型从 AdventureWorks 示例数据库中的 Contact、Address、Product、SalesOrderHeader 和 SalesOrderDetail 等表生成。</span><span class="sxs-lookup"><span data-stu-id="e6978-105">The AdventureWorks Sales Model used in these examples is built from the Contact, Address, Product, SalesOrderHeader, and SalesOrderDetail tables in the AdventureWorks sample database.</span></span>  
  
 <span data-ttu-id="e6978-106">本主题中的示例使用以下 `using` / `Imports` 语句：</span><span class="sxs-lookup"><span data-stu-id="e6978-106">The examples in this topic use the following `using`/`Imports` statements:</span></span>  
  
 [!code-csharp[DP L2E Examples#ImportsUsing](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DP L2E Examples/CS/Program.cs#importsusing)]
 [!code-vb[DP L2E Examples#ImportsUsing](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DP L2E Examples/VB/Module1.vb#importsusing)]  
  
## <a name="select"></a><span data-ttu-id="e6978-107">Select</span><span class="sxs-lookup"><span data-stu-id="e6978-107">Select</span></span>  
  
### <a name="example"></a><span data-ttu-id="e6978-108">示例</span><span class="sxs-lookup"><span data-stu-id="e6978-108">Example</span></span>  

 <span data-ttu-id="e6978-109">以下示例使用 <xref:System.Linq.Queryable.Select%2A> 方法以将 `Product.Name` 和 `Product.ProductID` 属性投影到一系列匿名类型。</span><span class="sxs-lookup"><span data-stu-id="e6978-109">The following example uses the <xref:System.Linq.Queryable.Select%2A> method to project the `Product.Name` and `Product.ProductID` properties into a sequence of anonymous types.</span></span>  
  
 [!code-csharp[DP L2E Examples#SelectAnonymousTypes_MQ](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DP L2E Examples/CS/Program.cs#selectanonymoustypes_mq)]
 [!code-vb[DP L2E Examples#SelectAnonymousTypes_MQ](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DP L2E Examples/VB/Module1.vb#selectanonymoustypes_mq)]  
  
### <a name="example"></a><span data-ttu-id="e6978-110">示例</span><span class="sxs-lookup"><span data-stu-id="e6978-110">Example</span></span>  

 <span data-ttu-id="e6978-111">以下示例使用 <xref:System.Linq.Enumerable.Select%2A> 方法以只返回一系列产品名称。</span><span class="sxs-lookup"><span data-stu-id="e6978-111">The following example uses the <xref:System.Linq.Enumerable.Select%2A> method to return a sequence of only product names.</span></span>  
  
 [!code-csharp[DP L2E Examples#SelectSimple2_MQ](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DP L2E Examples/CS/Program.cs#selectsimple2_mq)]
 [!code-vb[DP L2E Examples#SelectSimple2_MQ](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DP L2E Examples/VB/Module1.vb#selectsimple2_mq)]  
  
## <a name="selectmany"></a><span data-ttu-id="e6978-112">SelectMany</span><span class="sxs-lookup"><span data-stu-id="e6978-112">SelectMany</span></span>  
  
### <a name="example"></a><span data-ttu-id="e6978-113">示例</span><span class="sxs-lookup"><span data-stu-id="e6978-113">Example</span></span>  

 <span data-ttu-id="e6978-114">以下示例使用 <xref:System.Linq.Enumerable.SelectMany%2A> 方法以选择 `TotalDue` 低于 500.00 的所有订单。</span><span class="sxs-lookup"><span data-stu-id="e6978-114">The following example uses the <xref:System.Linq.Enumerable.SelectMany%2A> method to select all orders where `TotalDue` is less than 500.00.</span></span>  
  
 [!code-csharp[DP L2E Examples#SelectManyCompoundFrom_MQ](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DP L2E Examples/CS/Program.cs#selectmanycompoundfrom_mq)]
 [!code-vb[DP L2E Examples#SelectManyCompoundFrom_MQ](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DP L2E Examples/VB/Module1.vb#selectmanycompoundfrom_mq)]  
  
### <a name="example"></a><span data-ttu-id="e6978-115">示例</span><span class="sxs-lookup"><span data-stu-id="e6978-115">Example</span></span>  

 <span data-ttu-id="e6978-116">以下示例使用 <xref:System.Linq.Enumerable.SelectMany%2A> 方法以选择在 2002 年 10 月 1 或此日期之后发出的所有订单。</span><span class="sxs-lookup"><span data-stu-id="e6978-116">The following example uses the <xref:System.Linq.Enumerable.SelectMany%2A> method to select all orders where the order was made on October 1, 2002 or later.</span></span>  
  
 [!code-csharp[DP L2E Examples#SelectManyCompoundFrom2_MQ](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DP L2E Examples/CS/Program.cs#selectmanycompoundfrom2_mq)]
 [!code-vb[DP L2E Examples#SelectManyCompoundFrom2_MQ](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DP L2E Examples/VB/Module1.vb#selectmanycompoundfrom2_mq)]  
  
## <a name="see-also"></a><span data-ttu-id="e6978-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="e6978-117">See also</span></span>

- [<span data-ttu-id="e6978-118">LINQ to Entities 中的查询</span><span class="sxs-lookup"><span data-stu-id="e6978-118">Queries in LINQ to Entities</span></span>](queries-in-linq-to-entities.md)
