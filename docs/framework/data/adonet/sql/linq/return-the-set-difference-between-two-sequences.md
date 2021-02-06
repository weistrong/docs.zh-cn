---
description: 了解详细信息：返回两个序列之间的差集
title: 返回两个序列之间的差集
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 62efb546-c898-408f-af21-36e7c6fed217
ms.openlocfilehash: 6836195ac4e1ee678fd3e8089e7c341f7dd247e8
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99662972"
---
# <a name="return-the-set-difference-between-two-sequences"></a><span data-ttu-id="5c2e4-103">返回两个序列之间的差集</span><span class="sxs-lookup"><span data-stu-id="5c2e4-103">Return the Set Difference Between Two Sequences</span></span>

<span data-ttu-id="5c2e4-104">使用 <xref:System.Linq.Queryable.Except%2A> 运算符可返回两个序列之间的差集。</span><span class="sxs-lookup"><span data-stu-id="5c2e4-104">Use the <xref:System.Linq.Queryable.Except%2A> operator to return the set difference between two sequences.</span></span>  
  
## <a name="example"></a><span data-ttu-id="5c2e4-105">示例</span><span class="sxs-lookup"><span data-stu-id="5c2e4-105">Example</span></span>  

 <span data-ttu-id="5c2e4-106">此示例使用 <xref:System.Linq.Queryable.Except%2A> 返回 `Customers` 居住但不居住的所有国家/地区的序列 `Employees` 。</span><span class="sxs-lookup"><span data-stu-id="5c2e4-106">This example uses <xref:System.Linq.Queryable.Except%2A> to return a sequence of all countries/regions in which `Customers` live but in which no `Employees` live.</span></span>  
  
 [!code-csharp[DLinqQueryExamples#41](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqQueryExamples/cs/Program.cs#41)]
 [!code-vb[DLinqQueryExamples#41](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqQueryExamples/vb/Module1.vb#41)]  
  
 <span data-ttu-id="5c2e4-107">在 [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] 中，<xref:System.Linq.Queryable.Except%2A> 运算仅对集合而言是定义完善的。</span><span class="sxs-lookup"><span data-stu-id="5c2e4-107">In [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)], the <xref:System.Linq.Queryable.Except%2A> operation is well defined only on sets.</span></span> <span data-ttu-id="5c2e4-108">针对多重集的语义尚未定义。</span><span class="sxs-lookup"><span data-stu-id="5c2e4-108">The semantics for multisets is undefined.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5c2e4-109">请参阅</span><span class="sxs-lookup"><span data-stu-id="5c2e4-109">See also</span></span>

- [<span data-ttu-id="5c2e4-110">查询示例</span><span class="sxs-lookup"><span data-stu-id="5c2e4-110">Query Examples</span></span>](query-examples.md)
- [<span data-ttu-id="5c2e4-111">标准查询运算符转换</span><span class="sxs-lookup"><span data-stu-id="5c2e4-111">Standard Query Operator Translation</span></span>](standard-query-operator-translation.md)
