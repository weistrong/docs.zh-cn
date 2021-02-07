---
description: '了解详细信息：组联接子句 (Visual Basic) '
title: Group Join 子句
ms.date: 07/20/2015
f1_keywords:
- vb.QueryGroupJoinIn
- vb.QueryGroupJoinOn
- vb.QueryGroupJoin
- vb.QueryGroupJoinInto
helpviewer_keywords:
- Group Join clause [Visual Basic]
- Group Join statement [Visual Basic]
- queries [Visual Basic], Group Join
ms.assetid: 37dbf79c-7b5c-421b-bbb7-dadfd2b92a1c
ms.openlocfilehash: 177dc2b41c923bc8c1ae0477c3905e8adad36fbe
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99700476"
---
# <a name="group-join-clause-visual-basic"></a><span data-ttu-id="ceefe-103">Group Join 子句 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="ceefe-103">Group Join Clause (Visual Basic)</span></span>

<span data-ttu-id="ceefe-104">将两个集合合并为单个分层集合。</span><span class="sxs-lookup"><span data-stu-id="ceefe-104">Combines two collections into a single hierarchical collection.</span></span> <span data-ttu-id="ceefe-105">联接运算基于匹配键。</span><span class="sxs-lookup"><span data-stu-id="ceefe-105">The join operation is based on matching keys.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ceefe-106">语法</span><span class="sxs-lookup"><span data-stu-id="ceefe-106">Syntax</span></span>  
  
```vb  
Group Join element [As type] In collection _  
  On key1 Equals key2 [ And key3 Equals key4 [... ] ] _  
  Into expressionList  
```  
  
## <a name="parts"></a><span data-ttu-id="ceefe-107">组成部分</span><span class="sxs-lookup"><span data-stu-id="ceefe-107">Parts</span></span>  
  
|<span data-ttu-id="ceefe-108">术语</span><span class="sxs-lookup"><span data-stu-id="ceefe-108">Term</span></span>|<span data-ttu-id="ceefe-109">定义</span><span class="sxs-lookup"><span data-stu-id="ceefe-109">Definition</span></span>|  
|---|---|  
|`element`|<span data-ttu-id="ceefe-110">必需。</span><span class="sxs-lookup"><span data-stu-id="ceefe-110">Required.</span></span> <span data-ttu-id="ceefe-111">要联接的集合的控件变量。</span><span class="sxs-lookup"><span data-stu-id="ceefe-111">The control variable for the collection being joined.</span></span>|  
|`type`|<span data-ttu-id="ceefe-112">可选。</span><span class="sxs-lookup"><span data-stu-id="ceefe-112">Optional.</span></span> <span data-ttu-id="ceefe-113">`element` 的类型。</span><span class="sxs-lookup"><span data-stu-id="ceefe-113">The type of `element`.</span></span> <span data-ttu-id="ceefe-114">如果未 `type` 指定，则 `element` 将从中推断出的类型 `collection` 。</span><span class="sxs-lookup"><span data-stu-id="ceefe-114">If no `type` is specified, the type of `element` is inferred from `collection`.</span></span>|  
|`collection`|<span data-ttu-id="ceefe-115">必需。</span><span class="sxs-lookup"><span data-stu-id="ceefe-115">Required.</span></span> <span data-ttu-id="ceefe-116">要与运算符左侧的集合组合的集合 `Group Join` 。</span><span class="sxs-lookup"><span data-stu-id="ceefe-116">The collection to combine with the collection that is on the left side of the `Group Join` operator.</span></span> <span data-ttu-id="ceefe-117">`Group Join`子句可以嵌套在子句中，也可以嵌套在 `Join` 另一 `Group Join` 子句中。</span><span class="sxs-lookup"><span data-stu-id="ceefe-117">A `Group Join` clause can be nested in a `Join` clause or in another `Group Join` clause.</span></span>|  
|<span data-ttu-id="ceefe-118">`key1` `Equals` `key2`</span><span class="sxs-lookup"><span data-stu-id="ceefe-118">`key1` `Equals` `key2`</span></span>|<span data-ttu-id="ceefe-119">必需。</span><span class="sxs-lookup"><span data-stu-id="ceefe-119">Required.</span></span> <span data-ttu-id="ceefe-120">标识要联接的集合的键。</span><span class="sxs-lookup"><span data-stu-id="ceefe-120">Identifies keys for the collections being joined.</span></span> <span data-ttu-id="ceefe-121">必须使用 `Equals` 运算符来比较要联接的集合中的键。</span><span class="sxs-lookup"><span data-stu-id="ceefe-121">You must use the `Equals` operator to compare keys from the collections being joined.</span></span> <span data-ttu-id="ceefe-122">可以通过使用 `And` 运算符来标识多个键，从而组合联接条件。</span><span class="sxs-lookup"><span data-stu-id="ceefe-122">You can combine join conditions by using the `And` operator to identify multiple keys.</span></span> <span data-ttu-id="ceefe-123">`key1`参数必须位于运算符左侧的集合中 `Join` 。</span><span class="sxs-lookup"><span data-stu-id="ceefe-123">The `key1` parameter must be from the collection on the left side of the `Join` operator.</span></span> <span data-ttu-id="ceefe-124">`key2`参数必须来自运算符右侧的集合 `Join` 。</span><span class="sxs-lookup"><span data-stu-id="ceefe-124">The `key2` parameter must be from the collection on the right side of the `Join` operator.</span></span><br /><br /> <span data-ttu-id="ceefe-125">联接条件中使用的键可以是包含集合中多个项的表达式。</span><span class="sxs-lookup"><span data-stu-id="ceefe-125">The keys used in the join condition can be expressions that include more than one item from the collection.</span></span> <span data-ttu-id="ceefe-126">但是，每个键表达式只能包含其各自集合中的项。</span><span class="sxs-lookup"><span data-stu-id="ceefe-126">However, each key expression can contain only items from its respective collection.</span></span>|  
|`expressionList`|<span data-ttu-id="ceefe-127">必需。</span><span class="sxs-lookup"><span data-stu-id="ceefe-127">Required.</span></span> <span data-ttu-id="ceefe-128">一个或多个表达式，用于标识集合中的元素组的聚合方式。</span><span class="sxs-lookup"><span data-stu-id="ceefe-128">One or more expressions that identify how the groups of elements from the collection are aggregated.</span></span> <span data-ttu-id="ceefe-129">若要标识分组结果的成员名称，请使用 `Group` 关键字 (`<alias> = Group`) 。</span><span class="sxs-lookup"><span data-stu-id="ceefe-129">To identify a member name for the grouped results, use the `Group` keyword (`<alias> = Group`).</span></span> <span data-ttu-id="ceefe-130">还可以包含聚合函数以将其应用于该组。</span><span class="sxs-lookup"><span data-stu-id="ceefe-130">You can also include aggregate functions to apply to the group.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="ceefe-131">备注</span><span class="sxs-lookup"><span data-stu-id="ceefe-131">Remarks</span></span>  

 <span data-ttu-id="ceefe-132">`Group Join`子句组合了两个集合，这些集合基于要联接的集合中的匹配键值。</span><span class="sxs-lookup"><span data-stu-id="ceefe-132">The `Group Join` clause combines two collections based on matching key values from the collections being joined.</span></span> <span data-ttu-id="ceefe-133">生成的集合可以包含一个成员，该成员引用第二个集合中与第一个集合中的键值相匹配的元素的集合。</span><span class="sxs-lookup"><span data-stu-id="ceefe-133">The resulting collection can contain a member that references a collection of elements from the second collection that match the key value from the first collection.</span></span> <span data-ttu-id="ceefe-134">还可以指定要应用于第二个集合中的分组元素的聚合函数。</span><span class="sxs-lookup"><span data-stu-id="ceefe-134">You can also specify aggregate functions to apply to the grouped elements from the second collection.</span></span> <span data-ttu-id="ceefe-135">有关聚合函数的信息，请参阅 [Aggregate 子句](aggregate-clause.md)。</span><span class="sxs-lookup"><span data-stu-id="ceefe-135">For information about aggregate functions, see [Aggregate Clause](aggregate-clause.md).</span></span>  
  
 <span data-ttu-id="ceefe-136">例如，考虑一个经理集合和一组雇员。</span><span class="sxs-lookup"><span data-stu-id="ceefe-136">Consider, for example, a collection of managers and a collection of employees.</span></span> <span data-ttu-id="ceefe-137">这两个集合中的元素都具有 ManagerID 属性，该属性标识向特定经理报告的员工。</span><span class="sxs-lookup"><span data-stu-id="ceefe-137">Elements from both collections have a ManagerID property that identifies the employees that report to a particular manager.</span></span> <span data-ttu-id="ceefe-138">联接操作的结果将包含具有匹配的 ManagerID 值的每个经理和员工的结果。</span><span class="sxs-lookup"><span data-stu-id="ceefe-138">The results from a join operation would contain a result for each manager and employee with a matching ManagerID value.</span></span> <span data-ttu-id="ceefe-139">操作的结果 `Group Join` 将包含管理器的完整列表。</span><span class="sxs-lookup"><span data-stu-id="ceefe-139">The results from a `Group Join` operation would contain the complete list of managers.</span></span> <span data-ttu-id="ceefe-140">每个管理器结果都有一个成员，该成员引用了与特定经理匹配的员工列表。</span><span class="sxs-lookup"><span data-stu-id="ceefe-140">Each manager result would have a member that referenced the list of employees that were a match for the specific manager.</span></span>  
  
 <span data-ttu-id="ceefe-141">由操作生成的集合 `Group Join` 可以包含子句中标识的集合中的任何值组合 `From` 和子句的子句中标识的表达式 `Into` `Group Join` 。</span><span class="sxs-lookup"><span data-stu-id="ceefe-141">The collection resulting from a `Group Join` operation can contain any combination of values from the collection identified in the `From` clause and the expressions identified in the `Into` clause of the `Group Join` clause.</span></span> <span data-ttu-id="ceefe-142">有关子句的有效表达式的详细信息 `Into` ，请参阅 [Aggregate 子句](aggregate-clause.md)。</span><span class="sxs-lookup"><span data-stu-id="ceefe-142">For more information about valid expressions for the `Into` clause, see [Aggregate Clause](aggregate-clause.md).</span></span>  
  
 <span data-ttu-id="ceefe-143">`Group Join`操作将返回位于运算符左侧标识的集合中的所有结果 `Group Join` 。</span><span class="sxs-lookup"><span data-stu-id="ceefe-143">A `Group Join` operation will return all results from the collection identified on the left side of the `Group Join` operator.</span></span> <span data-ttu-id="ceefe-144">即使要联接的集合中没有匹配项，也是如此。</span><span class="sxs-lookup"><span data-stu-id="ceefe-144">This is true even if there are no matches in the collection being joined.</span></span> <span data-ttu-id="ceefe-145">这类似于 `LEFT OUTER JOIN` SQL 中的。</span><span class="sxs-lookup"><span data-stu-id="ceefe-145">This is like a `LEFT OUTER JOIN` in SQL.</span></span>  
  
 <span data-ttu-id="ceefe-146">可以使用子句将 `Join` 集合合并为单个集合。</span><span class="sxs-lookup"><span data-stu-id="ceefe-146">You can use the `Join` clause to combine collections into a single collection.</span></span> <span data-ttu-id="ceefe-147">这等效于 `INNER JOIN` SQL 中的。</span><span class="sxs-lookup"><span data-stu-id="ceefe-147">This is equivalent to an `INNER JOIN` in SQL.</span></span>  
  
## <a name="example"></a><span data-ttu-id="ceefe-148">示例</span><span class="sxs-lookup"><span data-stu-id="ceefe-148">Example</span></span>  

 <span data-ttu-id="ceefe-149">下面的代码示例使用子句联接两个集合 `Group Join` 。</span><span class="sxs-lookup"><span data-stu-id="ceefe-149">The following code example joins two collections by using the `Group Join` clause.</span></span>  
  
 [!code-vb[VbSimpleQuerySamples#14](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbSimpleQuerySamples/VB/QuerySamples1.vb#14)]  
  
## <a name="see-also"></a><span data-ttu-id="ceefe-150">请参阅</span><span class="sxs-lookup"><span data-stu-id="ceefe-150">See also</span></span>

- [<span data-ttu-id="ceefe-151">Visual Basic 中的 LINQ 简介</span><span class="sxs-lookup"><span data-stu-id="ceefe-151">Introduction to LINQ in Visual Basic</span></span>](../../programming-guide/language-features/linq/introduction-to-linq.md)
- [<span data-ttu-id="ceefe-152">查询</span><span class="sxs-lookup"><span data-stu-id="ceefe-152">Queries</span></span>](index.md)
- [<span data-ttu-id="ceefe-153">Select 子句</span><span class="sxs-lookup"><span data-stu-id="ceefe-153">Select Clause</span></span>](select-clause.md)
- [<span data-ttu-id="ceefe-154">From 子句</span><span class="sxs-lookup"><span data-stu-id="ceefe-154">From Clause</span></span>](from-clause.md)
- [<span data-ttu-id="ceefe-155">Join 子句</span><span class="sxs-lookup"><span data-stu-id="ceefe-155">Join Clause</span></span>](join-clause.md)
- [<span data-ttu-id="ceefe-156">Where 子句</span><span class="sxs-lookup"><span data-stu-id="ceefe-156">Where Clause</span></span>](where-clause.md)
- [<span data-ttu-id="ceefe-157">Group By 子句</span><span class="sxs-lookup"><span data-stu-id="ceefe-157">Group By Clause</span></span>](group-by-clause.md)
