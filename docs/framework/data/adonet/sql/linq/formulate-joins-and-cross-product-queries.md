---
description: 了解详细信息：构建联接和叉积查询
title: 构建联接和跨产品查询
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: d8072ede-0521-4670-9bec-1778ceeb875b
ms.openlocfilehash: 1adee3576d7b30d6ec9a9c4e920befcd21dd9e85
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99739113"
---
# <a name="formulate-joins-and-cross-product-queries"></a><span data-ttu-id="5bee2-103">构建联接和跨产品查询</span><span class="sxs-lookup"><span data-stu-id="5bee2-103">Formulate Joins and Cross-Product Queries</span></span>

<span data-ttu-id="5bee2-104">下面的示例演示如何组合来自多个表的结果。</span><span class="sxs-lookup"><span data-stu-id="5bee2-104">The following examples show how to combine results from multiple tables.</span></span>  
  
## <a name="example"></a><span data-ttu-id="5bee2-105">示例</span><span class="sxs-lookup"><span data-stu-id="5bee2-105">Example</span></span>  

 <span data-ttu-id="5bee2-106">下面的示例在 c ) # 中 Visual Basic (子句的子句中使用外键导航， `From` `from` 以选择伦敦的客户的所有订单。</span><span class="sxs-lookup"><span data-stu-id="5bee2-106">The following example uses foreign key navigation in the `From` clause in Visual Basic (`from` clause in C#) to select all orders for customers in London.</span></span>  
  
 [!code-csharp[DLinqQueryExamples#47](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqQueryExamples/cs/Program.cs#47)]
 [!code-vb[DLinqQueryExamples#47](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqQueryExamples/vb/Module1.vb#47)]  
  
## <a name="example"></a><span data-ttu-id="5bee2-107">示例</span><span class="sxs-lookup"><span data-stu-id="5bee2-107">Example</span></span>  

 <span data-ttu-id="5bee2-108">下面的示例在 c ) # 中 Visual Basic (子句的子句中使用外键导航， `Where` `where` 以筛选 `Products` 其 `Supplier` 在美国中的脱销。</span><span class="sxs-lookup"><span data-stu-id="5bee2-108">The following example uses foreign key navigation in the `Where` clause in Visual Basic (`where` clause in C#) to filter for out-of-stock `Products` whose `Supplier` is in the United States.</span></span>  
  
 [!code-csharp[DLinqQueryExamples#48](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqQueryExamples/cs/Program.cs#48)]
 [!code-vb[DLinqQueryExamples#48](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqQueryExamples/vb/Module1.vb#48)]  
  
## <a name="example"></a><span data-ttu-id="5bee2-109">示例</span><span class="sxs-lookup"><span data-stu-id="5bee2-109">Example</span></span>  

 <span data-ttu-id="5bee2-110">下面的示例在 c # 中 Visual Basic (子句的子句中使用外键导航 `From` `from` ，) 筛选西雅图中的员工并列出其区域。</span><span class="sxs-lookup"><span data-stu-id="5bee2-110">The following example uses foreign key navigation in the `From` clause in Visual Basic (`from` clause in C#) to filter for employees in Seattle and to list their territories.</span></span>  
  
 [!code-csharp[DLinqQueryExamples#49](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqQueryExamples/cs/Program.cs#49)]  
  
## <a name="example"></a><span data-ttu-id="5bee2-111">示例</span><span class="sxs-lookup"><span data-stu-id="5bee2-111">Example</span></span>  

 <span data-ttu-id="5bee2-112">下面的示例在 c ) # 中 Visual Basic (子句的子句中使用外键导航， `Select` `select` 以筛选一个雇员向另一个雇员报告的雇员对，并将两个雇员从同一个雇员 `City` 。</span><span class="sxs-lookup"><span data-stu-id="5bee2-112">The following example uses foreign key navigation in the `Select` clause in Visual Basic (`select` clause in C#) to filter for pairs of employees where one employee reports to the other and where both employees are from the same `City`.</span></span>  
  
 [!code-csharp[DLinqQueryExamples#50](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqQueryExamples/cs/Program.cs#50)]
 [!code-vb[DLinqQueryExamples#50](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqQueryExamples/vb/Module1.vb#50)]  
  
## <a name="example"></a><span data-ttu-id="5bee2-113">示例</span><span class="sxs-lookup"><span data-stu-id="5bee2-113">Example</span></span>  

 <span data-ttu-id="5bee2-114">以下 Visual Basic 示例查找所有客户和订单，确保订单与客户匹配，并保证对于该列表中的每个客户，都提供了联系人姓名。</span><span class="sxs-lookup"><span data-stu-id="5bee2-114">The following Visual Basic example looks for all customers and orders, makes sure that the orders are matched to customers, and guarantees that for every customer in that list, a contact name is provided.</span></span>  
  
 [!code-vb[DLinqQueryExamples#50v](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqQueryExamples/vb/Module1.vb#50v)]  
  
## <a name="example"></a><span data-ttu-id="5bee2-115">示例</span><span class="sxs-lookup"><span data-stu-id="5bee2-115">Example</span></span>  

 <span data-ttu-id="5bee2-116">下面的示例显式联接两个表并投影来自这两个表的结果。</span><span class="sxs-lookup"><span data-stu-id="5bee2-116">The following example explicitly joins two tables and projects results from both tables.</span></span>  
  
 [!code-csharp[DLinqQueryExamples#51](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqQueryExamples/cs/Program.cs#51)]
 [!code-vb[DLinqQueryExamples#51](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqQueryExamples/vb/Module1.vb#51)]  
  
## <a name="example"></a><span data-ttu-id="5bee2-117">示例</span><span class="sxs-lookup"><span data-stu-id="5bee2-117">Example</span></span>  

 <span data-ttu-id="5bee2-118">下面的示例显式联接三个表并投影来自其中各个表的结果。</span><span class="sxs-lookup"><span data-stu-id="5bee2-118">The following example explicitly joins three tables and projects results from each of them.</span></span>  
  
 [!code-csharp[DLinqQueryExamples#52](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqQueryExamples/cs/Program.cs#52)]
 [!code-vb[DLinqQueryExamples#52](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqQueryExamples/vb/Module1.vb#52)]  
  
## <a name="example"></a><span data-ttu-id="5bee2-119">示例</span><span class="sxs-lookup"><span data-stu-id="5bee2-119">Example</span></span>  

 <span data-ttu-id="5bee2-120">下面的示例演示如何通过使用 `LEFT OUTER JOIN` 实现 `DefaultIfEmpty()`。</span><span class="sxs-lookup"><span data-stu-id="5bee2-120">The following example shows how to achieve a `LEFT OUTER JOIN` by using `DefaultIfEmpty()`.</span></span> <span data-ttu-id="5bee2-121">如果对应的 `DefaultIfEmpty()` 没有 `Order`，则 `Employee` 方法将返回 null。</span><span class="sxs-lookup"><span data-stu-id="5bee2-121">The `DefaultIfEmpty()` method returns null when there is no `Order` for the `Employee`.</span></span>  
  
 [!code-csharp[DLinqQueryExamples#53](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqQueryExamples/cs/Program.cs#53)]
 [!code-vb[DLinqQueryExamples#53](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqQueryExamples/vb/Module1.vb#53)]  
  
## <a name="example"></a><span data-ttu-id="5bee2-122">示例</span><span class="sxs-lookup"><span data-stu-id="5bee2-122">Example</span></span>  

 <span data-ttu-id="5bee2-123">下面的示例投影通过联接获得的 `let` 表达式。</span><span class="sxs-lookup"><span data-stu-id="5bee2-123">The following example projects a `let` expression resulting from a join.</span></span>  
  
 [!code-csharp[DLinqQueryExamples#54](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqQueryExamples/cs/Program.cs#54)]
 [!code-vb[DLinqQueryExamples#54](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqQueryExamples/vb/Module1.vb#54)]  
  
## <a name="example"></a><span data-ttu-id="5bee2-124">示例</span><span class="sxs-lookup"><span data-stu-id="5bee2-124">Example</span></span>  

 <span data-ttu-id="5bee2-125">下面的示例显示了一个带有组合键的 `join`。</span><span class="sxs-lookup"><span data-stu-id="5bee2-125">The following example shows a `join` with a composite key.</span></span>  
  
 [!code-csharp[DLinqQueryExamples#55](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqQueryExamples/cs/Program.cs#55)]
 [!code-vb[DLinqQueryExamples#55](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqQueryExamples/vb/Module1.vb#55)]  
  
## <a name="example"></a><span data-ttu-id="5bee2-126">示例</span><span class="sxs-lookup"><span data-stu-id="5bee2-126">Example</span></span>  

 <span data-ttu-id="5bee2-127">下面的示例演示如何构造其中一端可以为 null、另一端不可以为 null 的 `join`。</span><span class="sxs-lookup"><span data-stu-id="5bee2-127">The following example shows how to construct a `join` where one side is nullable and the other is not.</span></span>  
  
 [!code-csharp[DLinqQueryExamples#56](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqQueryExamples/cs/Program.cs#56)]
 [!code-vb[DLinqQueryExamples#56](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqQueryExamples/vb/Module1.vb#56)]  
  
## <a name="see-also"></a><span data-ttu-id="5bee2-128">请参阅</span><span class="sxs-lookup"><span data-stu-id="5bee2-128">See also</span></span>

- [<span data-ttu-id="5bee2-129">查询示例</span><span class="sxs-lookup"><span data-stu-id="5bee2-129">Query Examples</span></span>](query-examples.md)
