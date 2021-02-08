---
description: 了解详细信息：按顺序对元素进行分组
title: 对序列中的元素进行分组
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 1d50c8b4-f550-4775-bbb6-eab6e874cb43
ms.openlocfilehash: bc9a4d042ed0edb090f0530ebb24d99a5390c882
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99786064"
---
# <a name="group-elements-in-a-sequence"></a><span data-ttu-id="d8e7c-103">对序列中的元素进行分组</span><span class="sxs-lookup"><span data-stu-id="d8e7c-103">Group Elements in a Sequence</span></span>

<span data-ttu-id="d8e7c-104"><xref:System.Linq.Enumerable.GroupBy%2A> 运算符用于对序列中的元素进行分组。</span><span class="sxs-lookup"><span data-stu-id="d8e7c-104">The <xref:System.Linq.Enumerable.GroupBy%2A> operator groups the elements of a sequence.</span></span> <span data-ttu-id="d8e7c-105">下面的示例使用 Northwind 数据库。</span><span class="sxs-lookup"><span data-stu-id="d8e7c-105">The following examples use the Northwind database.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="d8e7c-106"><xref:System.Linq.Enumerable.GroupBy%2A> 查询中的 Null 列值有时可能引发 <xref:System.InvalidOperationException>。</span><span class="sxs-lookup"><span data-stu-id="d8e7c-106">Null column values in <xref:System.Linq.Enumerable.GroupBy%2A> queries can sometimes throw an <xref:System.InvalidOperationException>.</span></span> <span data-ttu-id="d8e7c-107">有关详细信息，请参阅 [疑难解答](troubleshooting.md)的 "GroupBy InvalidOperationException" 部分。</span><span class="sxs-lookup"><span data-stu-id="d8e7c-107">For more information, see the "GroupBy InvalidOperationException" section of [Troubleshooting](troubleshooting.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="d8e7c-108">示例</span><span class="sxs-lookup"><span data-stu-id="d8e7c-108">Example</span></span>  

 <span data-ttu-id="d8e7c-109">下面的示例按照 `Products` 对 `CategoryID` 进行分区。</span><span class="sxs-lookup"><span data-stu-id="d8e7c-109">The following example partitions `Products` by `CategoryID`.</span></span>  
  
 [!code-csharp[DLinqQueryExamples#27](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqQueryExamples/cs/Program.cs#27)]
 [!code-vb[DLinqQueryExamples#27](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqQueryExamples/vb/Module1.vb#27)]  
  
## <a name="example"></a><span data-ttu-id="d8e7c-110">示例</span><span class="sxs-lookup"><span data-stu-id="d8e7c-110">Example</span></span>  

 <span data-ttu-id="d8e7c-111">下面的示例使用 <xref:System.Linq.Enumerable.Max%2A> 来查找每个 `CategoryID` 的最高单价。</span><span class="sxs-lookup"><span data-stu-id="d8e7c-111">The following example uses <xref:System.Linq.Enumerable.Max%2A> to find the maximum unit price for each `CategoryID`.</span></span>  
  
 [!code-csharp[DLinqQueryExamples#28](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqQueryExamples/cs/Program.cs#28)]
 [!code-vb[DLinqQueryExamples#28](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqQueryExamples/vb/Module1.vb#28)]  
  
## <a name="example"></a><span data-ttu-id="d8e7c-112">示例</span><span class="sxs-lookup"><span data-stu-id="d8e7c-112">Example</span></span>  

 <span data-ttu-id="d8e7c-113">下面的示例使用 Average 来查找每个 `UnitPrice` 的平均 `CategoryID`。</span><span class="sxs-lookup"><span data-stu-id="d8e7c-113">The following example uses Average to find the average `UnitPrice` for each `CategoryID`.</span></span>  
  
 [!code-csharp[DLinqQueryExamples#29](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqQueryExamples/cs/Program.cs#29)]
 [!code-vb[DLinqQueryExamples#29](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqQueryExamples/vb/Module1.vb#29)]  
  
## <a name="example"></a><span data-ttu-id="d8e7c-114">示例</span><span class="sxs-lookup"><span data-stu-id="d8e7c-114">Example</span></span>  

 <span data-ttu-id="d8e7c-115">下面的示例使用 <xref:System.Linq.Queryable.Sum%2A> 来查找每个 `UnitPrice` 的总 `CategoryID`。</span><span class="sxs-lookup"><span data-stu-id="d8e7c-115">The following example uses <xref:System.Linq.Queryable.Sum%2A> to find the total `UnitPrice` for each `CategoryID`.</span></span>  
  
 [!code-csharp[DLinqQueryExamples#30](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqQueryExamples/cs/Program.cs#30)]
 [!code-vb[DLinqQueryExamples#30](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqQueryExamples/vb/Module1.vb#30)]  
  
## <a name="example"></a><span data-ttu-id="d8e7c-116">示例</span><span class="sxs-lookup"><span data-stu-id="d8e7c-116">Example</span></span>  

 <span data-ttu-id="d8e7c-117">下面的示例使用 <xref:System.Linq.Queryable.Count%2A> 来查找每个 `Products` 中已停产 `CategoryID` 的数量。</span><span class="sxs-lookup"><span data-stu-id="d8e7c-117">The following example uses <xref:System.Linq.Queryable.Count%2A> to find the number of discontinued `Products` in each `CategoryID`.</span></span>  
  
 [!code-csharp[DLinqQueryExamples#31](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqQueryExamples/cs/Program.cs#31)]
 [!code-vb[DLinqQueryExamples#31](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqQueryExamples/vb/Module1.vb#31)]  
  
## <a name="example"></a><span data-ttu-id="d8e7c-118">示例</span><span class="sxs-lookup"><span data-stu-id="d8e7c-118">Example</span></span>  

 <span data-ttu-id="d8e7c-119">下面的示例使用后跟的 `where` 子句来查找至少包含 10 种产品的所有类别。</span><span class="sxs-lookup"><span data-stu-id="d8e7c-119">The following example uses a following `where` clause to find all categories that have at least 10 products.</span></span>  
  
 [!code-csharp[DLinqQueryExamples#32](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqQueryExamples/cs/Program.cs#32)]
 [!code-vb[DLinqQueryExamples#32](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqQueryExamples/vb/Module1.vb#32)]  
  
## <a name="example"></a><span data-ttu-id="d8e7c-120">示例</span><span class="sxs-lookup"><span data-stu-id="d8e7c-120">Example</span></span>  

 <span data-ttu-id="d8e7c-121">下面的示例按 `CategoryID` 和 `SupplierID` 对产品进行分组。</span><span class="sxs-lookup"><span data-stu-id="d8e7c-121">The following example groups products by `CategoryID` and `SupplierID`.</span></span>  
  
 [!code-csharp[DLinqQueryExamples#33](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqQueryExamples/cs/Program.cs#33)]
 [!code-vb[DLinqQueryExamples#33](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqQueryExamples/vb/Module1.vb#33)]  
  
## <a name="example"></a><span data-ttu-id="d8e7c-122">示例</span><span class="sxs-lookup"><span data-stu-id="d8e7c-122">Example</span></span>  

 <span data-ttu-id="d8e7c-123">下面的示例返回两个产品序列。</span><span class="sxs-lookup"><span data-stu-id="d8e7c-123">The following example returns two sequences of products.</span></span> <span data-ttu-id="d8e7c-124">第一个序列包含单价小于或等于 10 的产品。</span><span class="sxs-lookup"><span data-stu-id="d8e7c-124">The first sequence contains products with unit price less than or equal to 10.</span></span> <span data-ttu-id="d8e7c-125">第二个序列包含单价大于 10 的产品。</span><span class="sxs-lookup"><span data-stu-id="d8e7c-125">The second sequence contains products with unit price greater than 10.</span></span>  
  
 [!code-csharp[DLinqQueryExamples#34](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqQueryExamples/cs/Program.cs#34)]
 [!code-vb[DLinqQueryExamples#34](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqQueryExamples/vb/Module1.vb#34)]  
  
## <a name="example"></a><span data-ttu-id="d8e7c-126">示例</span><span class="sxs-lookup"><span data-stu-id="d8e7c-126">Example</span></span>  

 <span data-ttu-id="d8e7c-127"><xref:System.Linq.Queryable.GroupBy%2A> 运算符只能采用单个键自变量。</span><span class="sxs-lookup"><span data-stu-id="d8e7c-127">The <xref:System.Linq.Queryable.GroupBy%2A> operator can take only a single key argument.</span></span> <span data-ttu-id="d8e7c-128">如果您需要按多个键进行分组，则必须创建匿名类型，如下例所示：</span><span class="sxs-lookup"><span data-stu-id="d8e7c-128">If you need to group by more than one key, you must create an anonymous type, as in the following example:</span></span>  
  
 [!code-csharp[DLinqQueryExamples#35](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqQueryExamples/cs/Program.cs#35)]
 [!code-vb[DLinqQueryExamples#35](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqQueryExamples/vb/Module1.vb#35)]  
  
## <a name="see-also"></a><span data-ttu-id="d8e7c-129">请参阅</span><span class="sxs-lookup"><span data-stu-id="d8e7c-129">See also</span></span>

- [<span data-ttu-id="d8e7c-130">查询示例</span><span class="sxs-lookup"><span data-stu-id="d8e7c-130">Query Examples</span></span>](query-examples.md)
- [<span data-ttu-id="d8e7c-131">下载示例数据库</span><span class="sxs-lookup"><span data-stu-id="d8e7c-131">Downloading Sample Databases</span></span>](downloading-sample-databases.md)
