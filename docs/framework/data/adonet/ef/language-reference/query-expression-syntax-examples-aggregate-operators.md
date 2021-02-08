---
description: 了解详细信息：查询表达式语法示例：聚合运算符
title: 查询表达式语法示例：聚合运算符
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: d729120c-4c1b-4f34-bbe9-33694fca2dde
ms.openlocfilehash: c0fd9c3faf770a00a54341cf3718c2dda91a4d7b
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99767929"
---
# <a name="query-expression-syntax-examples-aggregate-operators"></a><span data-ttu-id="1bec7-103">查询表达式语法示例：聚合运算符</span><span class="sxs-lookup"><span data-stu-id="1bec7-103">Query Expression Syntax Examples: Aggregate Operators</span></span>

<span data-ttu-id="1bec7-104">本主题中的示例演示如何使用 <xref:System.Linq.Enumerable.Average%2A> 、 <xref:System.Linq.Enumerable.Count%2A> 、 <xref:System.Linq.Enumerable.Max%2A> 、 <xref:System.Linq.Enumerable.Min%2A> 和 <xref:System.Linq.Enumerable.Sum%2A> 方法通过使用查询表达式语法来查询 [AdventureWorks 销售模型](https://github.com/Microsoft/sql-server-samples/releases/tag/adventureworks) 。</span><span class="sxs-lookup"><span data-stu-id="1bec7-104">The examples in this topic demonstrate how to use the <xref:System.Linq.Enumerable.Average%2A>, <xref:System.Linq.Enumerable.Count%2A>, <xref:System.Linq.Enumerable.Max%2A>, <xref:System.Linq.Enumerable.Min%2A>, and <xref:System.Linq.Enumerable.Sum%2A> methods to query the [AdventureWorks Sales Model](https://github.com/Microsoft/sql-server-samples/releases/tag/adventureworks) using query expression syntax.</span></span> <span data-ttu-id="1bec7-105">这些示例中使用的 AdventureWorks 销售模型从 AdventureWorks 示例数据库中的 Contact、Address、Product、SalesOrderHeader 和 SalesOrderDetail 等表生成。</span><span class="sxs-lookup"><span data-stu-id="1bec7-105">The AdventureWorks Sales Model used in these examples is built from the Contact, Address, Product, SalesOrderHeader, and SalesOrderDetail tables in the AdventureWorks sample database.</span></span>  
  
 <span data-ttu-id="1bec7-106">本主题中的示例使用以下 `using` / `Imports` 语句：</span><span class="sxs-lookup"><span data-stu-id="1bec7-106">The examples in this topic use the following `using`/`Imports` statements:</span></span>  
  
 [!code-csharp[DP L2E Examples#ImportsUsing](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DP L2E Examples/CS/Program.cs#importsusing)]
 [!code-vb[DP L2E Examples#ImportsUsing](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DP L2E Examples/VB/Module1.vb#importsusing)]  
  
## <a name="average"></a><span data-ttu-id="1bec7-107">平均值</span><span class="sxs-lookup"><span data-stu-id="1bec7-107">Average</span></span>  
  
### <a name="example"></a><span data-ttu-id="1bec7-108">示例</span><span class="sxs-lookup"><span data-stu-id="1bec7-108">Example</span></span>  

 <span data-ttu-id="1bec7-109">以下示例使用 <xref:System.Linq.Enumerable.Average%2A> 方法以查找每种样式的产品的平均标价。</span><span class="sxs-lookup"><span data-stu-id="1bec7-109">The following example uses the <xref:System.Linq.Enumerable.Average%2A> method to find the average list price of the products of each style.</span></span>  
  
 [!code-csharp[DP L2E Examples#Average2_MQ](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DP L2E Examples/CS/Program.cs#average2_mq)]
 [!code-vb[DP L2E Examples#Average2_MQ](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DP L2E Examples/VB/Module1.vb#average2_mq)]  
  
### <a name="example"></a><span data-ttu-id="1bec7-110">示例</span><span class="sxs-lookup"><span data-stu-id="1bec7-110">Example</span></span>  

 <span data-ttu-id="1bec7-111">以下示例使用 <xref:System.Linq.Enumerable.Average%2A> 以获取每个联系人 ID 的平均应付款总计。</span><span class="sxs-lookup"><span data-stu-id="1bec7-111">The following example uses <xref:System.Linq.Enumerable.Average%2A> to get the average total due for each contact ID.</span></span>  
  
 [!code-csharp[DP L2E Examples#AverageGrouped_MQ](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DP L2E Examples/CS/Program.cs#averagegrouped_mq)]
 [!code-vb[DP L2E Examples#AverageGrouped_MQ](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DP L2E Examples/VB/Module1.vb#averagegrouped_mq)]  
  
### <a name="example"></a><span data-ttu-id="1bec7-112">示例</span><span class="sxs-lookup"><span data-stu-id="1bec7-112">Example</span></span>  

 <span data-ttu-id="1bec7-113">以下示例使用 <xref:System.Linq.Enumerable.Average%2A> 以针对每个联系人获取具有平均应付款总计的订单。</span><span class="sxs-lookup"><span data-stu-id="1bec7-113">The following example uses <xref:System.Linq.Enumerable.Average%2A> to get the orders with the average total due for each contact.</span></span>  
  
 [!code-csharp[DP L2E Examples#AverageElements_MQ](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DP L2E Examples/CS/Program.cs#averageelements_mq)]
 [!code-vb[DP L2E Examples#AverageElements_MQ](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DP L2E Examples/VB/Module1.vb#averageelements_mq)]  
  
## <a name="count"></a><span data-ttu-id="1bec7-114">计数</span><span class="sxs-lookup"><span data-stu-id="1bec7-114">Count</span></span>  
  
### <a name="example"></a><span data-ttu-id="1bec7-115">示例</span><span class="sxs-lookup"><span data-stu-id="1bec7-115">Example</span></span>  

 <span data-ttu-id="1bec7-116">以下示例使用 <xref:System.Linq.Enumerable.Count%2A> 以返回联系人 ID 的列表和每个联系人 ID 所具有的订单数。</span><span class="sxs-lookup"><span data-stu-id="1bec7-116">The following example uses <xref:System.Linq.Enumerable.Count%2A> to return a list of contact IDs and how many orders each has.</span></span>  
  
 [!code-csharp[DP L2E Examples#CountNested](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DP L2E Examples/CS/Program.cs#countnested)]
 [!code-vb[DP L2E Examples#CountNested](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DP L2E Examples/VB/Module1.vb#countnested)]  
  
### <a name="example"></a><span data-ttu-id="1bec7-117">示例</span><span class="sxs-lookup"><span data-stu-id="1bec7-117">Example</span></span>  

 <span data-ttu-id="1bec7-118">以下示例按颜色对产品进行分组，并使用 <xref:System.Linq.Enumerable.Count%2A> 以返回每个颜色组中的产品数量。</span><span class="sxs-lookup"><span data-stu-id="1bec7-118">The following example groups products by color and uses <xref:System.Linq.Enumerable.Count%2A> to return the number of products in each color group.</span></span>  
  
 [!code-csharp[DP L2E Examples#CountGrouped](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DP L2E Examples/CS/Program.cs#countgrouped)]
 [!code-vb[DP L2E Examples#CountGrouped](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DP L2E Examples/VB/Module1.vb#countgrouped)]  
  
## <a name="max"></a><span data-ttu-id="1bec7-119">Max</span><span class="sxs-lookup"><span data-stu-id="1bec7-119">Max</span></span>  
  
### <a name="example"></a><span data-ttu-id="1bec7-120">示例</span><span class="sxs-lookup"><span data-stu-id="1bec7-120">Example</span></span>  

 <span data-ttu-id="1bec7-121">以下示例使用 <xref:System.Linq.Enumerable.Max%2A> 方法以获取每个联系人 ID 的最大应付款总计。</span><span class="sxs-lookup"><span data-stu-id="1bec7-121">The following example uses the <xref:System.Linq.Enumerable.Max%2A> method to get the largest total due for each contact ID.</span></span>  
  
 [!code-csharp[DP L2E Examples#MaxGrouped_MQ](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DP L2E Examples/CS/Program.cs#maxgrouped_mq)]
 [!code-vb[DP L2E Examples#MaxGrouped_MQ](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DP L2E Examples/VB/Module1.vb#maxgrouped_mq)]  
  
### <a name="example"></a><span data-ttu-id="1bec7-122">示例</span><span class="sxs-lookup"><span data-stu-id="1bec7-122">Example</span></span>  

 <span data-ttu-id="1bec7-123">以下示例使用 <xref:System.Linq.Enumerable.Max%2A> 方法以针对每个联系人 ID 获取具有最大应付款总计的订单。</span><span class="sxs-lookup"><span data-stu-id="1bec7-123">The following example uses the <xref:System.Linq.Enumerable.Max%2A> method to get the orders with the largest total due for each contact ID.</span></span>  
  
 [!code-csharp[DP L2E Examples#MaxElements_MQ](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DP L2E Examples/CS/Program.cs#maxelements_mq)]
 [!code-vb[DP L2E Examples#MaxElements_MQ](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DP L2E Examples/VB/Module1.vb#maxelements_mq)]  
  
## <a name="min"></a><span data-ttu-id="1bec7-124">Min</span><span class="sxs-lookup"><span data-stu-id="1bec7-124">Min</span></span>  
  
### <a name="example"></a><span data-ttu-id="1bec7-125">示例</span><span class="sxs-lookup"><span data-stu-id="1bec7-125">Example</span></span>  

 <span data-ttu-id="1bec7-126">以下示例使用 <xref:System.Linq.Enumerable.Min%2A> 方法以获取每个联系人 ID 的最小应付款总计。</span><span class="sxs-lookup"><span data-stu-id="1bec7-126">The following example uses the <xref:System.Linq.Enumerable.Min%2A> method to get the smallest total due for each contact ID.</span></span>  
  
 [!code-csharp[DP L2E Examples#MinGrouped_MQ](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DP L2E Examples/CS/Program.cs#mingrouped_mq)]
 [!code-vb[DP L2E Examples#MinGrouped_MQ](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DP L2E Examples/VB/Module1.vb#mingrouped_mq)]  
  
### <a name="example"></a><span data-ttu-id="1bec7-127">示例</span><span class="sxs-lookup"><span data-stu-id="1bec7-127">Example</span></span>  

 <span data-ttu-id="1bec7-128">以下示例使用 <xref:System.Linq.Enumerable.Min%2A> 方法以针对每个联系人获取具有最小应付款总计的订单。</span><span class="sxs-lookup"><span data-stu-id="1bec7-128">The following example uses the <xref:System.Linq.Enumerable.Min%2A> method to get the orders with the smallest total due for each contact.</span></span>  
  
 [!code-csharp[DP L2E Examples#MinElements_MQ](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DP L2E Examples/CS/Program.cs#minelements_mq)]
 [!code-vb[DP L2E Examples#MinElements_MQ](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DP L2E Examples/VB/Module1.vb#minelements_mq)]  
  
## <a name="sum"></a><span data-ttu-id="1bec7-129">Sum</span><span class="sxs-lookup"><span data-stu-id="1bec7-129">Sum</span></span>  
  
### <a name="example"></a><span data-ttu-id="1bec7-130">示例</span><span class="sxs-lookup"><span data-stu-id="1bec7-130">Example</span></span>  

 <span data-ttu-id="1bec7-131">以下示例使用 <xref:System.Linq.Enumerable.Sum%2A> 方法以获取每个联系人 ID 的应付款总计。</span><span class="sxs-lookup"><span data-stu-id="1bec7-131">The following example uses the <xref:System.Linq.Enumerable.Sum%2A> method to get the total due for each contact ID.</span></span>  
  
 [!code-csharp[DP L2E Examples#SumGrouped_MQ](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DP L2E Examples/CS/Program.cs#sumgrouped_mq)]
 [!code-vb[DP L2E Examples#SumGrouped_MQ](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DP L2E Examples/VB/Module1.vb#sumgrouped_mq)]  
  
## <a name="see-also"></a><span data-ttu-id="1bec7-132">请参阅</span><span class="sxs-lookup"><span data-stu-id="1bec7-132">See also</span></span>

- [<span data-ttu-id="1bec7-133">LINQ to Entities 中的查询</span><span class="sxs-lookup"><span data-stu-id="1bec7-133">Queries in LINQ to Entities</span></span>](queries-in-linq-to-entities.md)
