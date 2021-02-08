---
description: 了解详细信息：如何：在 DataContext 级别进行筛选
title: 如何：在 DataContext 级别进行筛选
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 15505cd7-0df2-427a-9f86-e0f96f60ee2e
ms.openlocfilehash: ffb287ac1ef8cc19044ec3d519e745f905fe213d
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99785973"
---
# <a name="how-to-filter-at-the-datacontext-level"></a><span data-ttu-id="e2930-103">如何：在 DataContext 级别进行筛选</span><span class="sxs-lookup"><span data-stu-id="e2930-103">How to: Filter at the DataContext Level</span></span>

<span data-ttu-id="e2930-104">您可以在 `EntitySets` 级别筛选 `DataContext`。</span><span class="sxs-lookup"><span data-stu-id="e2930-104">You can filter `EntitySets` at the `DataContext` level.</span></span> <span data-ttu-id="e2930-105">此类筛选器适用于用此 <xref:System.Data.Linq.DataContext> 实例执行的所有查询。</span><span class="sxs-lookup"><span data-stu-id="e2930-105">Such filters apply to all queries done with that <xref:System.Data.Linq.DataContext> instance.</span></span>  
  
## <a name="example"></a><span data-ttu-id="e2930-106">示例</span><span class="sxs-lookup"><span data-stu-id="e2930-106">Example</span></span>  

 <span data-ttu-id="e2930-107">在下面的示例中，使用 <xref:System.Data.Linq.DataLoadOptions.AssociateWith%28System.Linq.Expressions.LambdaExpression%29?displayProperty=nameWithType> 来筛选截至 `ShippedDate` 的客户的预加载订单。</span><span class="sxs-lookup"><span data-stu-id="e2930-107">In the following example, <xref:System.Data.Linq.DataLoadOptions.AssociateWith%28System.Linq.Expressions.LambdaExpression%29?displayProperty=nameWithType> is used to filter the pre-loaded orders for customers by `ShippedDate`.</span></span>  
  
 [!code-csharp[DLinqQueryConcepts#10](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqQueryConcepts/cs/Program.cs#10)]
 [!code-vb[DLinqQueryConcepts#10](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqQueryConcepts/vb/Module1.vb#10)]  
  
## <a name="see-also"></a><span data-ttu-id="e2930-108">请参阅</span><span class="sxs-lookup"><span data-stu-id="e2930-108">See also</span></span>

- [<span data-ttu-id="e2930-109">查询概念</span><span class="sxs-lookup"><span data-stu-id="e2930-109">Query Concepts</span></span>](query-concepts.md)
