---
description: 详细了解：返回或跳过序列中的元素
title: 返回或跳过序列中的元素
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 81a31acd-e0f1-4bca-9a12-fa1ad5752374
ms.openlocfilehash: 6eba93562d4c6a8ffa4150453deed88844d4e297
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99695133"
---
# <a name="return-or-skip-elements-in-a-sequence"></a><span data-ttu-id="c10b9-103">返回或跳过序列中的元素</span><span class="sxs-lookup"><span data-stu-id="c10b9-103">Return Or Skip Elements in a Sequence</span></span>

<span data-ttu-id="c10b9-104">使用 <xref:System.Linq.Queryable.Take%2A> 运算符可返回序列中给定数目的元素，然后跳过其余元素。</span><span class="sxs-lookup"><span data-stu-id="c10b9-104">Use the <xref:System.Linq.Queryable.Take%2A> operator to return a given number of elements in a sequence and then skip over the remainder.</span></span>  
  
 <span data-ttu-id="c10b9-105">使用 <xref:System.Linq.Queryable.Skip%2A> 运算符可跳过序列中给定数目的元素，然后返回其余元素。</span><span class="sxs-lookup"><span data-stu-id="c10b9-105">Use the <xref:System.Linq.Queryable.Skip%2A> operator to skip over a given number of elements in a sequence and then return the remainder.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="c10b9-106"><xref:System.Linq.Enumerable.Take%2A> 和 <xref:System.Linq.Enumerable.Skip%2A> 用在针对 SQL Server 2000 的查询中时存在一定的限制。</span><span class="sxs-lookup"><span data-stu-id="c10b9-106"><xref:System.Linq.Enumerable.Take%2A> and <xref:System.Linq.Enumerable.Skip%2A> have certain limitations when they are used in queries against SQL Server 2000.</span></span> <span data-ttu-id="c10b9-107">有关详细信息，请参阅 [疑难解答](troubleshooting.md)中的 "跳过并使用 SQL Server 2000" 条目。</span><span class="sxs-lookup"><span data-stu-id="c10b9-107">For more information, see the "Skip and Take Exceptions in SQL Server 2000" entry in [Troubleshooting](troubleshooting.md).</span></span>  
  
 [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] <span data-ttu-id="c10b9-108">通过使用带有 SQL <xref:System.Linq.Queryable.Skip%2A> 子句的子查询来转换 `NOT EXISTS`。</span><span class="sxs-lookup"><span data-stu-id="c10b9-108">translates <xref:System.Linq.Queryable.Skip%2A> by using a subquery with the SQL `NOT EXISTS` clause.</span></span> <span data-ttu-id="c10b9-109">这种转换存在以下局限性：</span><span class="sxs-lookup"><span data-stu-id="c10b9-109">This translation has the following limitations:</span></span>  
  
- <span data-ttu-id="c10b9-110">自变量必须为集合。</span><span class="sxs-lookup"><span data-stu-id="c10b9-110">The argument must be a set.</span></span> <span data-ttu-id="c10b9-111">不支持多重集，即便为有序多重集也不例外。</span><span class="sxs-lookup"><span data-stu-id="c10b9-111">Multisets are not supported, even if ordered.</span></span>  
  
- <span data-ttu-id="c10b9-112">生成的查询可能要比为应用了 <xref:System.Linq.Queryable.Skip%2A> 的基查询生成的查询复杂得多。</span><span class="sxs-lookup"><span data-stu-id="c10b9-112">The generated query can be much more complex than the query generated for the base query on which <xref:System.Linq.Queryable.Skip%2A> is applied.</span></span> <span data-ttu-id="c10b9-113">这种复杂性可能会导致性能降低，甚至发生超时。</span><span class="sxs-lookup"><span data-stu-id="c10b9-113">This complexity can cause decrease in performance or even a time-out.</span></span>  
  
## <a name="example"></a><span data-ttu-id="c10b9-114">示例</span><span class="sxs-lookup"><span data-stu-id="c10b9-114">Example</span></span>  

 <span data-ttu-id="c10b9-115">下面的示例使用 `Take` 选择前五个受雇的 `Employees`。</span><span class="sxs-lookup"><span data-stu-id="c10b9-115">The following example uses `Take` to select the first five `Employees` hired.</span></span> <span data-ttu-id="c10b9-116">请注意，此集合首先按 `HireDate` 排序。</span><span class="sxs-lookup"><span data-stu-id="c10b9-116">Note that the collection is first sorted by `HireDate`.</span></span>  
  
 [!code-csharp[DLinqQueryExamples#16](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqQueryExamples/cs/Program.cs#16)]
 [!code-vb[DLinqQueryExamples#16](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqQueryExamples/vb/Module1.vb#16)]  
  
## <a name="example"></a><span data-ttu-id="c10b9-117">示例</span><span class="sxs-lookup"><span data-stu-id="c10b9-117">Example</span></span>  

 <span data-ttu-id="c10b9-118">下面的示例使用 <xref:System.Linq.Queryable.Skip%2A> 选择 10 种最贵的 `Products` 以外的所有产品。</span><span class="sxs-lookup"><span data-stu-id="c10b9-118">The following example uses <xref:System.Linq.Queryable.Skip%2A> to select all except the 10 most expensive `Products`.</span></span>  
  
 [!code-csharp[DLinqQueryExamples#17](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqQueryExamples/cs/Program.cs#17)]
 [!code-vb[DLinqQueryExamples#17](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqQueryExamples/vb/Module1.vb#17)]  
  
## <a name="example"></a><span data-ttu-id="c10b9-119">示例</span><span class="sxs-lookup"><span data-stu-id="c10b9-119">Example</span></span>  

 <span data-ttu-id="c10b9-120">下面的示例结合使用 <xref:System.Linq.Queryable.Skip%2A> 和 <xref:System.Linq.Queryable.Take%2A> 方法来跳过前 50 条记录，然后返回下 10 条记录。</span><span class="sxs-lookup"><span data-stu-id="c10b9-120">The following example combines the <xref:System.Linq.Queryable.Skip%2A> and <xref:System.Linq.Queryable.Take%2A> methods to skip the first 50 records and then return the next 10.</span></span>  
  
 [!code-csharp[DLinqQueryExamples#18](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqQueryExamples/cs/Program.cs#18)]
 [!code-vb[DLinqQueryExamples#18](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqQueryExamples/vb/Module1.vb#18)]  
  
 <span data-ttu-id="c10b9-121"><xref:System.Linq.Queryable.Take%2A> 和 <xref:System.Linq.Queryable.Skip%2A> 运算仅对有序集而言是定义完善的。</span><span class="sxs-lookup"><span data-stu-id="c10b9-121"><xref:System.Linq.Queryable.Take%2A> and <xref:System.Linq.Queryable.Skip%2A> operations are well defined only against ordered sets.</span></span> <span data-ttu-id="c10b9-122">未定义针对无序集或多重集的语义。</span><span class="sxs-lookup"><span data-stu-id="c10b9-122">The semantics for unordered sets or multisets is undefined.</span></span>  
  
 <span data-ttu-id="c10b9-123">由于 SQL 中的排序存在限制，因此 [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] 会设法将 <xref:System.Linq.Queryable.Take%2A> 或 <xref:System.Linq.Queryable.Skip%2A> 运算符的参数的排序操作移到相应运算符的结果中进行。</span><span class="sxs-lookup"><span data-stu-id="c10b9-123">Because of the limitations on ordering in SQL, [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] tries to move the ordering of the argument of the <xref:System.Linq.Queryable.Take%2A> or <xref:System.Linq.Queryable.Skip%2A> operator to the result of the operator.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="c10b9-124">SQL Server 2000 和 SQL Server 2005 的转换不同。</span><span class="sxs-lookup"><span data-stu-id="c10b9-124">Translation is different for SQL Server 2000 and SQL Server 2005.</span></span> <span data-ttu-id="c10b9-125">如果你计划将 <xref:System.Linq.Queryable.Skip%2A> 与查询结合使用，请使用 SQL Server 2005。</span><span class="sxs-lookup"><span data-stu-id="c10b9-125">If you plan to use <xref:System.Linq.Queryable.Skip%2A> with a query of any complexity, use SQL Server 2005.</span></span>  
  
 <span data-ttu-id="c10b9-126">对于 SQL Server 2000，请考虑以下 [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] 查询：</span><span class="sxs-lookup"><span data-stu-id="c10b9-126">Consider the following [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] query for SQL Server 2000:</span></span>  
  
 [!code-csharp[DLinqQueryExamples#19](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqQueryExamples/cs/Program.cs#19)]
 [!code-vb[DLinqQueryExamples#19](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqQueryExamples/vb/Module1.vb#19)]  
  
 [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] <span data-ttu-id="c10b9-127">将排序操作移到 SQL 代码的结尾进行，如下所示：</span><span class="sxs-lookup"><span data-stu-id="c10b9-127">moves the ordering to the end in the SQL code, as follows:</span></span>  
  
```sql
SELECT TOP 1 [t0].[CustomerID], [t0].[CompanyName],  
FROM [Customers] AS [t0]  
WHERE (NOT (EXISTS(  
    SELECT NULL AS [EMPTY]  
    FROM (  
        SELECT TOP 1 [t1].[CustomerID]  
        FROM [Customers] AS [t1]  
        WHERE [t1].[City] = @p0  
        ORDER BY [t1].[CustomerID]  
        ) AS [t2]  
    WHERE [t0].[CustomerID] = [t2].[CustomerID]  
    ))) AND ([t0].[City] = @p1)  
ORDER BY [t0].[CustomerID]  
```  
  
 <span data-ttu-id="c10b9-128">当 <xref:System.Linq.Queryable.Take%2A> 和 <xref:System.Linq.Queryable.Skip%2A> 链接在一起时，所有指定的排序都必须一致。</span><span class="sxs-lookup"><span data-stu-id="c10b9-128">When <xref:System.Linq.Queryable.Take%2A> and <xref:System.Linq.Queryable.Skip%2A> are chained together, all the specified ordering must be consistent.</span></span> <span data-ttu-id="c10b9-129">否则，结果将是不确定的。</span><span class="sxs-lookup"><span data-stu-id="c10b9-129">Otherwise, the results are undefined.</span></span>  
  
 <span data-ttu-id="c10b9-130">对于非负的、基于 SQL 规范的整型常量参数，<xref:System.Linq.Queryable.Take%2A> 和 <xref:System.Linq.Queryable.Skip%2A> 都是定义完善的。</span><span class="sxs-lookup"><span data-stu-id="c10b9-130">For non-negative, constant integral arguments based on the SQL specification, both <xref:System.Linq.Queryable.Take%2A> and <xref:System.Linq.Queryable.Skip%2A> are well-defined.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c10b9-131">请参阅</span><span class="sxs-lookup"><span data-stu-id="c10b9-131">See also</span></span>

- [<span data-ttu-id="c10b9-132">查询示例</span><span class="sxs-lookup"><span data-stu-id="c10b9-132">Query Examples</span></span>](query-examples.md)
- [<span data-ttu-id="c10b9-133">标准查询运算符转换</span><span class="sxs-lookup"><span data-stu-id="c10b9-133">Standard Query Operator Translation</span></span>](standard-query-operator-translation.md)
