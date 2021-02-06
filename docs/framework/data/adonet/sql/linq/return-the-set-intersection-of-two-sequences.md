---
description: 了解详细信息：返回两个序列的交集
title: 返回两个序列的交集
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: d09c344e-3548-4944-a3ed-051880e3f5b8
ms.openlocfilehash: 163e138761caadb73b6dc5d672c02353a88a2c22
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99662971"
---
# <a name="return-the-set-intersection-of-two-sequences"></a><span data-ttu-id="a640b-103">返回两个序列的交集</span><span class="sxs-lookup"><span data-stu-id="a640b-103">Return the Set Intersection of Two Sequences</span></span>

<span data-ttu-id="a640b-104">使用 <xref:System.Linq.Queryable.Intersect%2A> 运算符可返回两个序列的交集。</span><span class="sxs-lookup"><span data-stu-id="a640b-104">Use the <xref:System.Linq.Queryable.Intersect%2A> operator to return the set intersection of two sequences.</span></span>  
  
## <a name="example"></a><span data-ttu-id="a640b-105">示例</span><span class="sxs-lookup"><span data-stu-id="a640b-105">Example</span></span>  

 <span data-ttu-id="a640b-106">此示例使用 <xref:System.Linq.Queryable.Intersect%2A> 返回和居住的所有国家/地区的序列 `Customers` `Employees` 。</span><span class="sxs-lookup"><span data-stu-id="a640b-106">This example uses <xref:System.Linq.Queryable.Intersect%2A> to return a sequence of all countries/regions in which both `Customers` and `Employees` live.</span></span>  
  
 [!code-csharp[DLinqQueryExamples#42](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqQueryExamples/cs/Program.cs#42)]
 [!code-vb[DLinqQueryExamples#42](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqQueryExamples/vb/Module1.vb#42)]  
  
 <span data-ttu-id="a640b-107">在 [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] 中，<xref:System.Linq.Queryable.Intersect%2A> 运算仅对集合而言是定义完善的。</span><span class="sxs-lookup"><span data-stu-id="a640b-107">In [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)], the <xref:System.Linq.Queryable.Intersect%2A> operation is well defined only on sets.</span></span> <span data-ttu-id="a640b-108">针对多重集的语义尚未定义。</span><span class="sxs-lookup"><span data-stu-id="a640b-108">The semantics for multisets is undefined.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a640b-109">请参阅</span><span class="sxs-lookup"><span data-stu-id="a640b-109">See also</span></span>

- [<span data-ttu-id="a640b-110">查询示例</span><span class="sxs-lookup"><span data-stu-id="a640b-110">Query Examples</span></span>](query-examples.md)
- [<span data-ttu-id="a640b-111">标准查询运算符转换</span><span class="sxs-lookup"><span data-stu-id="a640b-111">Standard Query Operator Translation</span></span>](standard-query-operator-translation.md)
