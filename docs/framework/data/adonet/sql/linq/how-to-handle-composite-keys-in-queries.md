---
description: 了解有关详细信息，请参阅如何：处理查询中的复合键
title: 如何：处理查询中的复合键
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: ce2f14fd-1038-458a-91e3-a078c61f0d10
ms.openlocfilehash: 9d7c68495810bee6a383d98a75694e7cd24f1015
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99738866"
---
# <a name="how-to-handle-composite-keys-in-queries"></a><span data-ttu-id="a493d-103">如何：处理查询中的复合键</span><span class="sxs-lookup"><span data-stu-id="a493d-103">How to: Handle Composite Keys in Queries</span></span>

<span data-ttu-id="a493d-104">有些运算符只能带一个自变量。</span><span class="sxs-lookup"><span data-stu-id="a493d-104">Some operators can take only one argument.</span></span> <span data-ttu-id="a493d-105">如果您的参数必须包含数据库中的多个列，则您必须创建一个匿名类型来表示这种组合。</span><span class="sxs-lookup"><span data-stu-id="a493d-105">If your argument must include more than one column from the database, you must create an anonymous type to represent the combination.</span></span>  
  
## <a name="example"></a><span data-ttu-id="a493d-106">示例</span><span class="sxs-lookup"><span data-stu-id="a493d-106">Example</span></span>  

 <span data-ttu-id="a493d-107">下面的示例显示了调用 `GroupBy` 运算符的查询，此运算符只能带一个 `key` 自变量。</span><span class="sxs-lookup"><span data-stu-id="a493d-107">The following example shows a query that invokes the `GroupBy` operator, which can take only one `key` argument.</span></span>  
  
 [!code-csharp[DLinqCompositeKeys#1](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqCompositeKeys/cs/Program.cs#1)]
 [!code-vb[DLinqCompositeKeys#1](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqCompositeKeys/vb/Module1.vb#1)]  
  
## <a name="example"></a><span data-ttu-id="a493d-108">示例</span><span class="sxs-lookup"><span data-stu-id="a493d-108">Example</span></span>  

 <span data-ttu-id="a493d-109">联接也属于这种情况，如下例中所示：</span><span class="sxs-lookup"><span data-stu-id="a493d-109">The same situation pertains to joins, as in the following example:</span></span>  
  
 [!code-csharp[DLinqCompositeKeys#2](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqCompositeKeys/cs/Program.cs#2)]
 [!code-vb[DLinqCompositeKeys#2](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqCompositeKeys/vb/Module1.vb#2)]  
  
## <a name="see-also"></a><span data-ttu-id="a493d-110">请参阅</span><span class="sxs-lookup"><span data-stu-id="a493d-110">See also</span></span>

- [<span data-ttu-id="a493d-111">查询概念</span><span class="sxs-lookup"><span data-stu-id="a493d-111">Query Concepts</span></span>](query-concepts.md)
