---
description: 了解详细信息：确定序列中的任何元素是否满足条件
title: 确定序列中任何或所有元素是否满足某一条件
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 339ec145-826c-46d2-8cf2-3acd252cd072
ms.openlocfilehash: a46cf7e4e213eba830dc203f9266a408103cee80
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99786103"
---
# <a name="determine-if-any-or-all-elements-in-a-sequence-satisfy-a-condition"></a><span data-ttu-id="84510-103">确定序列中任何或所有元素是否满足某一条件</span><span class="sxs-lookup"><span data-stu-id="84510-103">Determine if Any or All Elements in a Sequence Satisfy a Condition</span></span>

<span data-ttu-id="84510-104">如果序列中的所有元素都满足某一项条件，则 <xref:System.Linq.Enumerable.All%2A> 运算符会返回 `true`。</span><span class="sxs-lookup"><span data-stu-id="84510-104">The <xref:System.Linq.Enumerable.All%2A> operator returns `true` if all elements in a sequence satisfy a condition.</span></span>  
  
 <span data-ttu-id="84510-105">如果序列中的任意一个元素满足某一项条件，则 <xref:System.Linq.Queryable.Any%2A> 运算符会返回 `true`。</span><span class="sxs-lookup"><span data-stu-id="84510-105">The <xref:System.Linq.Queryable.Any%2A> operator returns `true` if any element in a sequence satisfies a condition.</span></span>  
  
## <a name="example"></a><span data-ttu-id="84510-106">示例</span><span class="sxs-lookup"><span data-stu-id="84510-106">Example</span></span>  

 <span data-ttu-id="84510-107">下面的示例返回由至少下了一个订单的客户组成的序列。</span><span class="sxs-lookup"><span data-stu-id="84510-107">The following example returns a sequence of customers that have at least one order.</span></span> <span data-ttu-id="84510-108">`Where` / `where` `true` 如果给定的具有 any，则子句的计算结果为 `Customer` `Order` 。</span><span class="sxs-lookup"><span data-stu-id="84510-108">The `Where`/`where` clause evaluates to `true` if the given `Customer` has any `Order`.</span></span>  
  
 [!code-csharp[DLinqQueryExamples#37](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqQueryExamples/cs/Program.cs#37)]
 [!code-vb[DLinqQueryExamples#37](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqQueryExamples/vb/Module1.vb#37)]  
  
## <a name="example"></a><span data-ttu-id="84510-109">示例</span><span class="sxs-lookup"><span data-stu-id="84510-109">Example</span></span>  

 <span data-ttu-id="84510-110">下面的 Visual Basic 代码确定未下订单的客户的列表，并确保对于该列表中的每一位客户，都提供了联系人名称。</span><span class="sxs-lookup"><span data-stu-id="84510-110">The following Visual Basic code determines the list of customers who have not placed orders, and ensures that for every customer in that list, a contact name is provided.</span></span>  
  
 [!code-vb[DLinqQueryExamples#37v](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqQueryExamples/vb/Module1.vb#37v)]  
  
## <a name="example"></a><span data-ttu-id="84510-111">示例</span><span class="sxs-lookup"><span data-stu-id="84510-111">Example</span></span>  

 <span data-ttu-id="84510-112">下面的 C# 示例返回由订单包含以“C”开头的 `ShipCity` 的客户组成的序列。</span><span class="sxs-lookup"><span data-stu-id="84510-112">The following C# example returns a sequence of customers whose orders have a `ShipCity` beginning with "C".</span></span> <span data-ttu-id="84510-113">返回结果中还包括未下订单的客户。</span><span class="sxs-lookup"><span data-stu-id="84510-113">Also included in the return are customers who have no orders.</span></span> <span data-ttu-id="84510-114"> (按设计， <xref:System.Linq.Queryable.All%2A> 运算符 `true` 为空序列返回。在控制台输出中，使用运算符来消除未按订单的客户 ) 。 `Count`</span><span class="sxs-lookup"><span data-stu-id="84510-114">(By design, the <xref:System.Linq.Queryable.All%2A> operator returns `true` for an empty sequence.) Customers with no orders are eliminated in the console output by using the `Count` operator.</span></span>  
  
 [!code-csharp[DLinqQueryExamples#38](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqQueryExamples/cs/Program.cs#38)]  
  
## <a name="see-also"></a><span data-ttu-id="84510-115">请参阅</span><span class="sxs-lookup"><span data-stu-id="84510-115">See also</span></span>

- [<span data-ttu-id="84510-116">查询示例</span><span class="sxs-lookup"><span data-stu-id="84510-116">Query Examples</span></span>](query-examples.md)
