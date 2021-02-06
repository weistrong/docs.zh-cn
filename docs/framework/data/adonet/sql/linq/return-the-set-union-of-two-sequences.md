---
description: 了解详细信息：返回两个序列的并集
title: 返回两个序列的并集
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 8b8bd3cb-86d4-4a3b-9906-61f68726dd1f
ms.openlocfilehash: 5541316560c05712e22c54f706b02d868fadb381
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99662957"
---
# <a name="return-the-set-union-of-two-sequences"></a><span data-ttu-id="9ee67-103">返回两个序列的并集</span><span class="sxs-lookup"><span data-stu-id="9ee67-103">Return the Set Union of Two Sequences</span></span>

<span data-ttu-id="9ee67-104">使用 <xref:System.Linq.Queryable.Union%2A> 运算符可返回两个序列的并集。</span><span class="sxs-lookup"><span data-stu-id="9ee67-104">Use the <xref:System.Linq.Queryable.Union%2A> operator to return the set union of two sequences.</span></span>  
  
## <a name="example"></a><span data-ttu-id="9ee67-105">示例</span><span class="sxs-lookup"><span data-stu-id="9ee67-105">Example</span></span>  

 <span data-ttu-id="9ee67-106">此示例使用 <xref:System.Linq.Queryable.Union%2A> 返回有或的所有国家/地区的序列 `Customers` `Employees` 。</span><span class="sxs-lookup"><span data-stu-id="9ee67-106">This example uses <xref:System.Linq.Queryable.Union%2A> to return a sequence of all countries/regions in which there are either `Customers` or `Employees`.</span></span>  
  
 [!code-csharp[DLinqQueryExamples#43](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqQueryExamples/cs/Program.cs#43)]
 [!code-vb[DLinqQueryExamples#43](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqQueryExamples/vb/Module1.vb#43)]  
  
 <span data-ttu-id="9ee67-107">在中 [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] ， <xref:System.Linq.Queryable.Union%2A> 运算符是为多重集定义的，因为多重集的无序串联 (实际上是 [`UNION ALL`](/sql/t-sql/language-elements/set-operators-union-transact-sql) SQL) 中子句的结果。</span><span class="sxs-lookup"><span data-stu-id="9ee67-107">In [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)], the <xref:System.Linq.Queryable.Union%2A> operator is defined for multisets as the unordered concatenation of the multisets (effectively the result of the [`UNION ALL`](/sql/t-sql/language-elements/set-operators-union-transact-sql) clause in SQL).</span></span>

<span data-ttu-id="9ee67-108">有关详细信息和示例，请参阅 <xref:System.Linq.Queryable.Union%2A?displayProperty=nameWithType> 。</span><span class="sxs-lookup"><span data-stu-id="9ee67-108">For more info and examples, see <xref:System.Linq.Queryable.Union%2A?displayProperty=nameWithType>.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="9ee67-109">请参阅</span><span class="sxs-lookup"><span data-stu-id="9ee67-109">See also</span></span>

- [<span data-ttu-id="9ee67-110">查询示例</span><span class="sxs-lookup"><span data-stu-id="9ee67-110">Query Examples</span></span>](query-examples.md)
- [<span data-ttu-id="9ee67-111">标准查询运算符转换</span><span class="sxs-lookup"><span data-stu-id="9ee67-111">Standard Query Operator Translation</span></span>](standard-query-operator-translation.md)
