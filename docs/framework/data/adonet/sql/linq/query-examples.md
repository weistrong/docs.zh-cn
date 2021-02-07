---
description: 了解详细信息：查询示例
title: 查询示例
ms.date: 03/30/2017
ms.assetid: 137f8677-494c-4d49-95ce-c17742f2d01f
ms.openlocfilehash: 77eb5c475a4f84930bd760b34f48d3954083c892
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99695194"
---
# <a name="query-examples"></a><span data-ttu-id="c4073-103">查询示例</span><span class="sxs-lookup"><span data-stu-id="c4073-103">Query Examples</span></span>

<span data-ttu-id="c4073-104">本部分提供典型查询的 Visual Basic 和 c # 示例 [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] 。</span><span class="sxs-lookup"><span data-stu-id="c4073-104">This section provides Visual Basic and C# examples of typical [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] queries.</span></span> <span data-ttu-id="c4073-105">使用 Visual Studio 的开发人员可以在 "示例" 部分中提供的示例解决方案中找到更多示例。</span><span class="sxs-lookup"><span data-stu-id="c4073-105">Developers using Visual Studio can find many more examples in a sample solution available in the Samples section.</span></span> <span data-ttu-id="c4073-106">有关详细信息，请参阅 [示例](samples.md)。</span><span class="sxs-lookup"><span data-stu-id="c4073-106">For more information, see [Samples](samples.md).</span></span>  
  
> [!IMPORTANT]
> <span data-ttu-id="c4073-107">*db* 通常用于文档中的代码示例 [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] 。</span><span class="sxs-lookup"><span data-stu-id="c4073-107">*db* is often used in code examples in [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] documentation.</span></span> <span data-ttu-id="c4073-108">*db* 假定为 *Northwind* 类的一个实例，该类继承自 <xref:System.Data.Linq.DataContext> 。</span><span class="sxs-lookup"><span data-stu-id="c4073-108">*db* is assumed to be an instance of a *Northwind* class, which inherits from <xref:System.Data.Linq.DataContext>.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="c4073-109">本节内容</span><span class="sxs-lookup"><span data-stu-id="c4073-109">In This Section</span></span>  

 [<span data-ttu-id="c4073-110">聚合查询</span><span class="sxs-lookup"><span data-stu-id="c4073-110">Aggregate Queries</span></span>](aggregate-queries.md)  
 <span data-ttu-id="c4073-111">介绍如何使用 <xref:System.Linq.Enumerable.Average%2A>、<xref:System.Linq.Enumerable.Count%2A> 等。</span><span class="sxs-lookup"><span data-stu-id="c4073-111">Describes how to use <xref:System.Linq.Enumerable.Average%2A>, <xref:System.Linq.Enumerable.Count%2A>, and so forth.</span></span>  
  
 [<span data-ttu-id="c4073-112">返回序列中的第一个元素</span><span class="sxs-lookup"><span data-stu-id="c4073-112">Return the First Element in a Sequence</span></span>](return-the-first-element-in-a-sequence.md)  
 <span data-ttu-id="c4073-113">提供使用 <xref:System.Linq.Enumerable.First%2A> 的示例。</span><span class="sxs-lookup"><span data-stu-id="c4073-113">Provides examples of using <xref:System.Linq.Enumerable.First%2A>.</span></span>  
  
 [<span data-ttu-id="c4073-114">返回或跳过序列中的元素</span><span class="sxs-lookup"><span data-stu-id="c4073-114">Return Or Skip Elements in a Sequence</span></span>](return-or-skip-elements-in-a-sequence.md)  
 <span data-ttu-id="c4073-115">提供使用 <xref:System.Linq.Enumerable.Take%2A> 和 <xref:System.Linq.Enumerable.Skip%2A> 的示例。</span><span class="sxs-lookup"><span data-stu-id="c4073-115">Provides examples of using <xref:System.Linq.Enumerable.Take%2A> and <xref:System.Linq.Enumerable.Skip%2A>.</span></span>  
  
 [<span data-ttu-id="c4073-116">在序列中对元素进行排序</span><span class="sxs-lookup"><span data-stu-id="c4073-116">Sort Elements in a Sequence</span></span>](sort-elements-in-a-sequence.md)  
 <span data-ttu-id="c4073-117">提供使用 <xref:System.Linq.Enumerable.OrderBy%2A> 的示例。</span><span class="sxs-lookup"><span data-stu-id="c4073-117">Provides examples of using <xref:System.Linq.Enumerable.OrderBy%2A>.</span></span>  
  
 [<span data-ttu-id="c4073-118">对序列中的元素进行分组</span><span class="sxs-lookup"><span data-stu-id="c4073-118">Group Elements in a Sequence</span></span>](group-elements-in-a-sequence.md)  
 <span data-ttu-id="c4073-119">提供使用 <xref:System.Linq.Enumerable.GroupBy%2A> 的示例。</span><span class="sxs-lookup"><span data-stu-id="c4073-119">Provides examples of using <xref:System.Linq.Enumerable.GroupBy%2A>.</span></span>  
  
 [<span data-ttu-id="c4073-120">从序列中消除重复的元素</span><span class="sxs-lookup"><span data-stu-id="c4073-120">Eliminate Duplicate Elements from a Sequence</span></span>](eliminate-duplicate-elements-from-a-sequence.md)  
 <span data-ttu-id="c4073-121">提供使用 <xref:System.Linq.Enumerable.Distinct%2A> 的示例。</span><span class="sxs-lookup"><span data-stu-id="c4073-121">Provides examples of using <xref:System.Linq.Enumerable.Distinct%2A>.</span></span>  
  
 [<span data-ttu-id="c4073-122">确定序列中任何或所有元素是否满足某一条件</span><span class="sxs-lookup"><span data-stu-id="c4073-122">Determine if Any or All Elements in a Sequence Satisfy a Condition</span></span>](determine-if-any-or-all-elements-in-a-sequence-satisfy-a-condition.md)  
 <span data-ttu-id="c4073-123">提供使用 <xref:System.Linq.Enumerable.All%2A> 和 <xref:System.Linq.Enumerable.Any%2A> 的示例。</span><span class="sxs-lookup"><span data-stu-id="c4073-123">Provides examples of using <xref:System.Linq.Enumerable.All%2A> and <xref:System.Linq.Enumerable.Any%2A>.</span></span>  
  
 [<span data-ttu-id="c4073-124">连接两个序列</span><span class="sxs-lookup"><span data-stu-id="c4073-124">Concatenate Two Sequences</span></span>](concatenate-two-sequences.md)  
 <span data-ttu-id="c4073-125">提供使用 <xref:System.Linq.Enumerable.Concat%2A> 的示例。</span><span class="sxs-lookup"><span data-stu-id="c4073-125">Provides examples of using <xref:System.Linq.Enumerable.Concat%2A>.</span></span>  
  
 [<span data-ttu-id="c4073-126">返回两个序列之间的差集</span><span class="sxs-lookup"><span data-stu-id="c4073-126">Return the Set Difference Between Two Sequences</span></span>](return-the-set-difference-between-two-sequences.md)  
 <span data-ttu-id="c4073-127">提供使用 <xref:System.Linq.Enumerable.Except%2A> 的示例。</span><span class="sxs-lookup"><span data-stu-id="c4073-127">Provides examples of using <xref:System.Linq.Enumerable.Except%2A>.</span></span>  
  
 [<span data-ttu-id="c4073-128">返回两个序列的交集</span><span class="sxs-lookup"><span data-stu-id="c4073-128">Return the Set Intersection of Two Sequences</span></span>](return-the-set-intersection-of-two-sequences.md)  
 <span data-ttu-id="c4073-129">提供使用 <xref:System.Linq.Enumerable.Intersect%2A> 的示例。</span><span class="sxs-lookup"><span data-stu-id="c4073-129">Provides examples of using <xref:System.Linq.Enumerable.Intersect%2A>.</span></span>  
  
 [<span data-ttu-id="c4073-130">返回两个序列的并集</span><span class="sxs-lookup"><span data-stu-id="c4073-130">Return the Set Union of Two Sequences</span></span>](return-the-set-union-of-two-sequences.md)  
 <span data-ttu-id="c4073-131">提供使用 <xref:System.Linq.Enumerable.Union%2A> 的示例。</span><span class="sxs-lookup"><span data-stu-id="c4073-131">Provides examples of using <xref:System.Linq.Enumerable.Union%2A>.</span></span>  
  
 [<span data-ttu-id="c4073-132">将序列转换为数组</span><span class="sxs-lookup"><span data-stu-id="c4073-132">Convert a Sequence to an Array</span></span>](convert-a-sequence-to-an-array.md)  
 <span data-ttu-id="c4073-133">提供使用 <xref:System.Linq.Enumerable.ToArray%2A> 的示例。</span><span class="sxs-lookup"><span data-stu-id="c4073-133">Provides examples of using <xref:System.Linq.Enumerable.ToArray%2A>.</span></span>  
  
 [<span data-ttu-id="c4073-134">将某一序列转换为泛型列表</span><span class="sxs-lookup"><span data-stu-id="c4073-134">Convert a Sequence to a Generic List</span></span>](convert-a-sequence-to-a-generic-list.md)  
 <span data-ttu-id="c4073-135">提供使用 <xref:System.Linq.Enumerable.ToList%2A> 的示例。</span><span class="sxs-lookup"><span data-stu-id="c4073-135">Provides examples of using <xref:System.Linq.Enumerable.ToList%2A>.</span></span>  
  
 [<span data-ttu-id="c4073-136">将某一类型转换为泛型 IEnumerable</span><span class="sxs-lookup"><span data-stu-id="c4073-136">Convert a Type to a Generic IEnumerable</span></span>](convert-a-type-to-a-generic-ienumerable.md)  
 <span data-ttu-id="c4073-137">提供使用 <xref:System.Linq.Enumerable.AsEnumerable%2A> 的示例。</span><span class="sxs-lookup"><span data-stu-id="c4073-137">Provides examples of using <xref:System.Linq.Enumerable.AsEnumerable%2A>.</span></span>  
  
 [<span data-ttu-id="c4073-138">构建联接和跨产品查询</span><span class="sxs-lookup"><span data-stu-id="c4073-138">Formulate Joins and Cross-Product Queries</span></span>](formulate-joins-and-cross-product-queries.md)  
 <span data-ttu-id="c4073-139">提供在 `from`、`where` 和 `select` 子句中使用外键导航的示例。</span><span class="sxs-lookup"><span data-stu-id="c4073-139">Provides examples of using foreign-key navigation in the `from`, `where`, and `select` clauses.</span></span>  
  
 [<span data-ttu-id="c4073-140">构建投影</span><span class="sxs-lookup"><span data-stu-id="c4073-140">Formulate Projections</span></span>](formulate-projections.md)  
 <span data-ttu-id="c4073-141">提供 `select` 与其他功能合并的示例 (例如，将) 为窗体查询投影的 *匿名类型* 。</span><span class="sxs-lookup"><span data-stu-id="c4073-141">Provides examples of combining `select` with other features (for example, *anonymous types*) to form query projections.</span></span>  
  
## <a name="related-sections"></a><span data-ttu-id="c4073-142">相关章节</span><span class="sxs-lookup"><span data-stu-id="c4073-142">Related Sections</span></span>  

 [<span data-ttu-id="c4073-143">标准查询运算符概述 (C#)</span><span class="sxs-lookup"><span data-stu-id="c4073-143">Standard Query Operators Overview (C#)</span></span>](../../../../../csharp/programming-guide/concepts/linq/standard-query-operators-overview.md)  
 <span data-ttu-id="c4073-144">说明使用 c # 的标准查询运算符的概念。</span><span class="sxs-lookup"><span data-stu-id="c4073-144">Explains the concept of standard query operators using C#.</span></span>  
  
 [<span data-ttu-id="c4073-145">标准查询运算符概述 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="c4073-145">Standard Query Operators Overview (Visual Basic)</span></span>](../../../../../visual-basic/programming-guide/concepts/linq/standard-query-operators-overview.md)  
 <span data-ttu-id="c4073-146">介绍使用 Visual Basic 的标准查询运算符的概念。</span><span class="sxs-lookup"><span data-stu-id="c4073-146">Explains the concept of standard query operators using Visual Basic.</span></span>  
  
 [<span data-ttu-id="c4073-147">查询概念</span><span class="sxs-lookup"><span data-stu-id="c4073-147">Query Concepts</span></span>](query-concepts.md)  
 <span data-ttu-id="c4073-148">解释 [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] 如何使用适用于查询的概念。</span><span class="sxs-lookup"><span data-stu-id="c4073-148">Explains how [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] uses concepts that apply to queries.</span></span>  
  
 [<span data-ttu-id="c4073-149">编程指南</span><span class="sxs-lookup"><span data-stu-id="c4073-149">Programming Guide</span></span>](programming-guide.md)  
 <span data-ttu-id="c4073-150">提供用于访问一些主题的门户，这些主题解释了与 [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] 相关的编程概念。</span><span class="sxs-lookup"><span data-stu-id="c4073-150">Provides a portal to topics that explain programming concepts related to [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)].</span></span>
