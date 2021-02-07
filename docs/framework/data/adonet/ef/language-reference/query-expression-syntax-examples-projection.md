---
description: 了解详细信息：查询表达式语法示例：投影
title: 查询表达式语法示例：投影
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 079926c5-e6b5-4fb9-b4cf-9c63886dd626
ms.openlocfilehash: e14a84272cef03dca24df5d0f889b8aaa77e94d0
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99696004"
---
# <a name="query-expression-syntax-examples-projection"></a><span data-ttu-id="a4fc7-103">查询表达式语法示例：投影</span><span class="sxs-lookup"><span data-stu-id="a4fc7-103">Query Expression Syntax Examples: Projection</span></span>

<span data-ttu-id="a4fc7-104">本主题中的示例演示如何使用 `Select` 方法和 `From … From …` 关键字，通过使用查询表达式语法来查询 [AdventureWorks 销售模型](https://github.com/Microsoft/sql-server-samples/releases/tag/adventureworks) 。</span><span class="sxs-lookup"><span data-stu-id="a4fc7-104">The examples in this topic demonstrate how to use the `Select` method and the `From … From …` keywords to query the [AdventureWorks Sales Model](https://github.com/Microsoft/sql-server-samples/releases/tag/adventureworks) using query expression syntax.</span></span> <span data-ttu-id="a4fc7-105">`From … From …`与 `SelectMany` 方法等效，但前者基于查询。</span><span class="sxs-lookup"><span data-stu-id="a4fc7-105">`From … From …` is the query based equivalent of the `SelectMany` method.</span></span> <span data-ttu-id="a4fc7-106">这些示例中使用的 AdventureWorks 销售模型从 AdventureWorks 示例数据库中的 Contact、Address、Product、SalesOrderHeader 和 SalesOrderDetail 等表生成。</span><span class="sxs-lookup"><span data-stu-id="a4fc7-106">The AdventureWorks Sales model used in these examples is built from the Contact, Address, Product, SalesOrderHeader, and SalesOrderDetail tables in the AdventureWorks sample database.</span></span>  
  
 <span data-ttu-id="a4fc7-107">本主题中的示例使用以下 `using` / `Imports` 语句：</span><span class="sxs-lookup"><span data-stu-id="a4fc7-107">The examples in this topic use the following `using`/`Imports` statements:</span></span>  
  
 [!code-csharp[DP L2E Examples#ImportsUsing](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DP L2E Examples/CS/Program.cs#importsusing)]
 [!code-vb[DP L2E Examples#ImportsUsing](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DP L2E Examples/VB/Module1.vb#importsusing)]  
  
## <a name="select"></a><span data-ttu-id="a4fc7-108">Select</span><span class="sxs-lookup"><span data-stu-id="a4fc7-108">Select</span></span>  
  
### <a name="example"></a><span data-ttu-id="a4fc7-109">示例</span><span class="sxs-lookup"><span data-stu-id="a4fc7-109">Example</span></span>  

 <span data-ttu-id="a4fc7-110">以下示例使用 <xref:System.Linq.Enumerable.Select%2A> 方法以返回 `Product` 表中的所有行并显示产品名称。</span><span class="sxs-lookup"><span data-stu-id="a4fc7-110">The following example uses the <xref:System.Linq.Enumerable.Select%2A> method to return all the rows from the `Product` table and display the product names.</span></span>  
  
 [!code-csharp[DP L2E Examples#SelectSimple1](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DP L2E Examples/CS/Program.cs#selectsimple1)]
 [!code-vb[DP L2E Examples#SelectSimple1](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DP L2E Examples/VB/Module1.vb#selectsimple1)]  
  
### <a name="example"></a><span data-ttu-id="a4fc7-111">示例</span><span class="sxs-lookup"><span data-stu-id="a4fc7-111">Example</span></span>  

 <span data-ttu-id="a4fc7-112">以下示例使用 <xref:System.Linq.Enumerable.Select%2A> 以只返回一系列产品名称。</span><span class="sxs-lookup"><span data-stu-id="a4fc7-112">The following example uses <xref:System.Linq.Enumerable.Select%2A> to return a sequence of only product names.</span></span>  
  
 [!code-csharp[DP L2E Examples#SelectSimple2](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DP L2E Examples/CS/Program.cs#selectsimple2)]
 [!code-vb[DP L2E Examples#SelectSimple2](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DP L2E Examples/VB/Module1.vb#selectsimple2)]  
  
### <a name="example"></a><span data-ttu-id="a4fc7-113">示例</span><span class="sxs-lookup"><span data-stu-id="a4fc7-113">Example</span></span>  

 <span data-ttu-id="a4fc7-114">以下示例使用 <xref:System.Linq.Queryable.Select%2A> 方法以将 `Product.Name` 和 `Product.ProductID` 属性投影到一系列匿名类型。</span><span class="sxs-lookup"><span data-stu-id="a4fc7-114">The following example uses the <xref:System.Linq.Queryable.Select%2A> method to project the `Product.Name` and `Product.ProductID` properties into a sequence of anonymous types.</span></span>  
  
 [!code-csharp[DP L2E Examples#SelectAnonymousTypes](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DP L2E Examples/CS/Program.cs#selectanonymoustypes)]
 [!code-vb[DP L2E Examples#SelectAnonymousTypes](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DP L2E Examples/VB/Module1.vb#selectanonymoustypes)]  
  
## <a name="from--from--selectmany"></a><span data-ttu-id="a4fc7-115">从。。。</span><span class="sxs-lookup"><span data-stu-id="a4fc7-115">From …</span></span> <span data-ttu-id="a4fc7-116">从。。。</span><span class="sxs-lookup"><span data-stu-id="a4fc7-116">From …</span></span> <span data-ttu-id="a4fc7-117"> (SelectMany) </span><span class="sxs-lookup"><span data-stu-id="a4fc7-117">(SelectMany)</span></span>  
  
### <a name="example"></a><span data-ttu-id="a4fc7-118">示例</span><span class="sxs-lookup"><span data-stu-id="a4fc7-118">Example</span></span>  

 <span data-ttu-id="a4fc7-119">以下示例使用 `From … From …` （与 <xref:System.Linq.Enumerable.SelectMany%2A> 方法等效）以选择 `TotalDue` 低于 500.00 的所有订单。</span><span class="sxs-lookup"><span data-stu-id="a4fc7-119">The following example uses `From … From …` (the equivalent of the <xref:System.Linq.Enumerable.SelectMany%2A> method) to select all orders where `TotalDue` is less than 500.00.</span></span>  
  
 [!code-csharp[DP L2E Examples#SelectManyCompoundFrom](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DP L2E Examples/CS/Program.cs#selectmanycompoundfrom)]
 [!code-vb[DP L2E Examples#SelectManyCompoundFrom](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DP L2E Examples/VB/Module1.vb#selectmanycompoundfrom)]  
  
### <a name="example"></a><span data-ttu-id="a4fc7-120">示例</span><span class="sxs-lookup"><span data-stu-id="a4fc7-120">Example</span></span>  

 <span data-ttu-id="a4fc7-121">以下示例使用 `From … From …`（与 <xref:System.Linq.Enumerable.SelectMany%2A> 方法等效）以选择在 2002 年 10 月 1 或此日期之后发出的所有订单。</span><span class="sxs-lookup"><span data-stu-id="a4fc7-121">The following example uses `From … From …` (the equivalent of the <xref:System.Linq.Enumerable.SelectMany%2A> method) to select all orders where the order was made on October 1, 2002 or later.</span></span>  
  
 [!code-csharp[DP L2E Examples#SelectManyCompoundFrom2](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DP L2E Examples/CS/Program.cs#selectmanycompoundfrom2)]
 [!code-vb[DP L2E Examples#SelectManyCompoundFrom2](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DP L2E Examples/VB/Module1.vb#selectmanycompoundfrom2)]  
  
### <a name="example"></a><span data-ttu-id="a4fc7-122">示例</span><span class="sxs-lookup"><span data-stu-id="a4fc7-122">Example</span></span>  

 <span data-ttu-id="a4fc7-123">以下示例使用 `From … From …`（与 <xref:System.Linq.Enumerable.SelectMany%2A> 方法等效）以选择订单总计高于 10000.00 的所有订单并使用 `From` 赋值以避免两次请求总计。</span><span class="sxs-lookup"><span data-stu-id="a4fc7-123">The following example uses a `From … From …` (the equivalent of the <xref:System.Linq.Enumerable.SelectMany%2A> method) to select all orders where the order total is greater than 10000.00 and uses `From` assignment to avoid requesting the total twice.</span></span>  
  
 [!code-csharp[DP L2E Examples#SelectManyFromAssignment](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DP L2E Examples/CS/Program.cs#selectmanyfromassignment)]
 [!code-vb[DP L2E Examples#SelectManyFromAssignment](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DP L2E Examples/VB/Module1.vb#selectmanyfromassignment)]  
  
## <a name="see-also"></a><span data-ttu-id="a4fc7-124">请参阅</span><span class="sxs-lookup"><span data-stu-id="a4fc7-124">See also</span></span>

- [<span data-ttu-id="a4fc7-125">LINQ to Entities 中的查询</span><span class="sxs-lookup"><span data-stu-id="a4fc7-125">Queries in LINQ to Entities</span></span>](queries-in-linq-to-entities.md)
