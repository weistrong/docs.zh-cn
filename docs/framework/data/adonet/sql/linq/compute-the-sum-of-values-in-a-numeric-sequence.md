---
description: 了解详细信息：计算数值序列中值的和
title: 计算数值序列中值的和
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 24e335b0-984e-4825-8721-0a91b533b7c3
ms.openlocfilehash: c4eb066b9286335111d96d32437291da9ea2d49a
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99712540"
---
# <a name="compute-the-sum-of-values-in-a-numeric-sequence"></a><span data-ttu-id="e47ff-103">计算数值序列中值的和</span><span class="sxs-lookup"><span data-stu-id="e47ff-103">Compute the Sum of Values in a Numeric Sequence</span></span>

<span data-ttu-id="e47ff-104">使用 <xref:System.Linq.Enumerable.Sum%2A> 运算符可以计算序列中数值的和。</span><span class="sxs-lookup"><span data-stu-id="e47ff-104">Use the <xref:System.Linq.Enumerable.Sum%2A> operator to compute the sum of numeric values in a sequence.</span></span>  
  
 <span data-ttu-id="e47ff-105">请注意 `Sum` 中 [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] 运算符的以下特征：</span><span class="sxs-lookup"><span data-stu-id="e47ff-105">Note the following characteristics of the `Sum` operator in [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)]:</span></span>  
  
- <span data-ttu-id="e47ff-106">使用标准查询运算符中的聚合运算符 `Sum` 计算空序列或只包含 null 的序列时，所得结果为零。</span><span class="sxs-lookup"><span data-stu-id="e47ff-106">The Standard Query Operator aggregate operator `Sum` evaluates to zero for an empty sequence or a sequence that contains only nulls.</span></span> <span data-ttu-id="e47ff-107">在 [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] 中，SQL 的语义保持不变。</span><span class="sxs-lookup"><span data-stu-id="e47ff-107">In [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)], the semantics of SQL are left unchanged.</span></span> <span data-ttu-id="e47ff-108">因此，使用 `Sum` 计算空序列或只包含 null 的序列时，所得结果为 null 而非零。</span><span class="sxs-lookup"><span data-stu-id="e47ff-108">For this reason, `Sum` evaluates to null instead of to zero for an empty sequence or for a sequence that contains only nulls.</span></span>  
  
- <span data-ttu-id="e47ff-109">针对中间结果的 SQL 限制适用于 [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] 中的聚合。</span><span class="sxs-lookup"><span data-stu-id="e47ff-109">SQL limitations on intermediate results apply to aggregates in [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)].</span></span> <span data-ttu-id="e47ff-110">32 位整型量之和不是使用 64 位结果计算的，且在 [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] 转换 `Sum` 时可能会发生溢出。</span><span class="sxs-lookup"><span data-stu-id="e47ff-110">Sum of 32-bit integer quantities is not computed by using 64-bit results, and overflow can occur for the [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] translation of `Sum`.</span></span> <span data-ttu-id="e47ff-111">即使对于内存中的对应序列，标准查询运算符的实现不会造成溢出，仍存在这种可能性。</span><span class="sxs-lookup"><span data-stu-id="e47ff-111">This possibility exists even if the Standard Query Operator implementation does not cause an overflow for the corresponding in-memory sequence.</span></span>  
  
## <a name="example"></a><span data-ttu-id="e47ff-112">示例</span><span class="sxs-lookup"><span data-stu-id="e47ff-112">Example</span></span>  

 <span data-ttu-id="e47ff-113">下面的示例查找 `Order` 表中所有订单的总运费。</span><span class="sxs-lookup"><span data-stu-id="e47ff-113">The following example finds the total freight of all orders in the `Order` table.</span></span>  
  
 <span data-ttu-id="e47ff-114">如果您对 Northwind 示例数据库运行此查询，则输出为：`64942.6900`。</span><span class="sxs-lookup"><span data-stu-id="e47ff-114">If you run this query against the Northwind sample database, the output is: `64942.6900`.</span></span>  
  
 [!code-csharp[DLinqQueryExamples#12](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqQueryExamples/cs/Program.cs#12)]
 [!code-vb[DLinqQueryExamples#12](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqQueryExamples/vb/Module1.vb#12)]  
  
## <a name="example"></a><span data-ttu-id="e47ff-115">示例</span><span class="sxs-lookup"><span data-stu-id="e47ff-115">Example</span></span>  

 <span data-ttu-id="e47ff-116">下面的示例查找所有产品总的订购件数。</span><span class="sxs-lookup"><span data-stu-id="e47ff-116">The following example finds the total number of units on order for all products.</span></span>  
  
 <span data-ttu-id="e47ff-117">如果您对 Northwind 示例数据库运行此查询，则输出为：`780`。</span><span class="sxs-lookup"><span data-stu-id="e47ff-117">If you run this query against the Northwind sample database, the output is: `780`.</span></span>  
  
 <span data-ttu-id="e47ff-118">请注意，您必须对 `short` 类型（例如，`UnitsOnOrder`）进行强制转换，因为 `Sum` 没有 short 类型的重载。</span><span class="sxs-lookup"><span data-stu-id="e47ff-118">Note that you must cast `short` types (for example, `UnitsOnOrder`) because `Sum` has no overload for short types.</span></span>  
  
 [!code-csharp[DLinqQueryExamples#13](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqQueryExamples/cs/Program.cs#13)]
 [!code-vb[DLinqQueryExamples#13](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqQueryExamples/vb/Module1.vb#13)]  
  
## <a name="see-also"></a><span data-ttu-id="e47ff-119">请参阅</span><span class="sxs-lookup"><span data-stu-id="e47ff-119">See also</span></span>

- [<span data-ttu-id="e47ff-120">聚合查询</span><span class="sxs-lookup"><span data-stu-id="e47ff-120">Aggregate Queries</span></span>](aggregate-queries.md)
- [<span data-ttu-id="e47ff-121">下载示例数据库</span><span class="sxs-lookup"><span data-stu-id="e47ff-121">Downloading Sample Databases</span></span>](downloading-sample-databases.md)
